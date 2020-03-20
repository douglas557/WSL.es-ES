---
title: Permisos de archivo
description: Descripción de cómo WSL determina los permisos de archivo en Windows
keywords: BashOnWindows, bash, WSL, wsl2, Windows, subsistema de Windows para Linux, windowssubsystem, Ubuntu, Debian, SuSE, Windows 10, archivo, permisos
ms.date: 01/14/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 4566fc86cf14df986bde80cf3a6cfb9267b23308
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520864"
---
# <a name="file-permissions-for-wsl"></a>Permisos de archivo para WSL

En esta página se detalla cómo se interpretan los permisos de archivo de Linux en el subsistema de Windows para Linux, especialmente cuando se tiene acceso a recursos dentro de Windows en el sistema de archivos NT. En esta documentación se supone un conocimiento básico de la [estructura de permisos del sistema de archivos de Linux](https://wiki.archlinux.org/index.php/File_permissions_and_attributes) . <!--TODO: Double check that it's okay to add these links--> y el [comando umask](https://en.wikipedia.org/wiki/Umask).

Al acceder a los archivos de Windows desde WSL, los permisos de archivo se calculan a partir de los permisos de Windows o se leen de los metadatos que WSL ha agregado al archivo. Estos metadatos no están habilitados de forma predeterminada. 

## <a name="wsl-metadata-on-windows-files"></a>Metadatos de WSL en archivos de Windows

Cuando se habilitan los metadatos como una opción de montaje en WSL, se pueden agregar e interpretar atributos extendidos en archivos de Windows NT para proporcionar los permisos del sistema de archivos de Linux. 

WSL puede agregar cuatro atributos extendidos NTFS:

| Nombre del atributo | Descripción |
| --- | --- |
| $LXUID | IDENTIFICADOR del propietario del usuario |
| $LXGID | IDENTIFICADOR del propietario del grupo |
| $LXMOD | Modo de archivo (permisos de sistema de archivos octales y tipo; por ejemplo: 0777) |
| $LXDEV | Dispositivo, si es un archivo de dispositivo |

Además, cualquier archivo que no sea un archivo o directorio normal (por ejemplo, vínculos simbólicos, FIFO, dispositivos de bloque, sockets de UNIX y dispositivos de caracteres) también tiene un [punto de análisis](https://docs.microsoft.com/en-us/windows/win32/fileio/reparse-points)de NTFS. Esto hace que sea mucho más rápido determinar el tipo de archivo en un directorio determinado sin tener que consultar sus atributos extendidos. 
<!-- TODO: For the blog include ONeDrive detail -->

## <a name="file-access-scenarios"></a>Escenarios de acceso a archivos

A continuación se muestra una descripción de cómo se determinan los permisos al obtener acceso a los archivos de diferentes maneras con el subsistema de Windows para Linux.

### <a name="accessing-files-in-the-windows-drive-file-system-drvfs-from-linux"></a>Acceso a archivos en el sistema de archivos de unidad de Windows (DrvFS) desde Linux

Estos escenarios se producen cuando se accede a los archivos de Windows desde WSL, lo que es más probable a través de `/mnt/c`. 

#### <a name="reading-file-permissions-from-an-existing-windows-file"></a>Leer los permisos de archivo de un archivo de Windows existente

El resultado depende de si el archivo ya tiene metadatos existentes.

##### <a name="the-file-does-not-have-metadata-default"></a>**El archivo no tiene metadatos (valor predeterminado)**

Si el archivo no tiene metadatos asociados a él, trasladaremos los permisos vigentes del usuario de Windows a los bits de lectura/escritura/ejecución y los establecería como el mismo valor para usuario, grupo y otros. Por ejemplo, si su cuenta de usuario de Windows tiene acceso de lectura y ejecución pero no tiene acceso de escritura al archivo, se mostrará como `r-x` para usuario, grupo y otros. Si el archivo tiene el atributo "solo lectura" establecido en Windows, no se concede acceso de escritura en Linux.

##### <a name="the-file-has-metadata"></a>El archivo tiene metadatos

Si el archivo tiene metadatos, simplemente usamos esos valores de metadatos en lugar de traducir los permisos efectivos del usuario de Windows.

#### <a name="changing-file-permissions-on-an-existing-windows-file-using-chmod"></a>Cambiar los permisos de archivo en un archivo de Windows existente con chmod

El resultado depende de si el archivo ya tiene metadatos existentes.

##### <a name="the-file-does-not-have-metadata-default"></a>**El archivo no tiene metadatos (valor predeterminado)**

Chmod solo tendrá un efecto, si quita todos los atributos de escritura de un archivo, se establecerá el atributo ' Read Only ' en el archivo de Windows, ya que se trata del mismo comportamiento que CIFS (sistema de archivos de Internet común), que es el cliente SMB (bloque de mensajes del servidor) en Linux.

##### <a name="the-file-has-metadata"></a>El archivo tiene metadatos

Chmod cambiará o agregará metadatos en función de los metadatos ya existentes del archivo. 

Tenga en cuenta que no puede dar más acceso a lo que tiene en Windows, aunque los metadatos indiquen que es el caso. Por ejemplo, puede establecer los metadatos para mostrar que tiene permisos de escritura en un archivo mediante `chmod 777`, pero si intentó tener acceso a ese archivo, todavía no podrá escribir en él. Esto se debe a la interoperabilidad, ya que los comandos de lectura o escritura de los archivos de Windows se enrutan a través de los permisos de usuario de Windows.

#### <a name="creating-a-file-in-drivefs"></a>Crear un archivo en DriveFS

El resultado depende de si se habilitan los metadatos.

##### <a name="metadata-is-not-enabled-default"></a>Los metadatos no están habilitados (valor predeterminado)

Los permisos de Windows del archivo recién creado serán los mismos que si creara el archivo en Windows sin un descriptor de seguridad específico, heredará los permisos del elemento primario. 

##### <a name="metadata-is-enabled"></a>Los metadatos están habilitados

Los bits de permiso del archivo se establecen para seguir los umask de Linux y el archivo se guardará con metadatos.

#### <a name="which-linux-user-and-linux-group-owns-the-file"></a>¿Qué grupo de usuarios de Linux y Linux posee el archivo? 

El resultado depende de si el archivo ya tiene metadatos existentes.

##### <a name="the-file-does-not-have-metadata-default"></a>**El archivo no tiene metadatos (valor predeterminado)**
En el escenario predeterminado, al montar las unidades de Windows de forma predeterminada, especificamos que el identificador de usuario (UID) de cualquier archivo se establece en el identificador de usuario del usuario de WSL y el identificador de grupo (GID) se establece en el identificador de grupo principal del usuario de WSL. 

##### <a name="the-file-has-metadata"></a>El archivo tiene metadatos

El UID y el GID especificados en los metadatos se aplican como el propietario del usuario y el propietario del grupo del archivo. 

### <a name="accessing-linux-files-from-windows-using-wsl"></a>Acceso a archivos de Linux desde Windows con `\\wsl$`

El acceso a los archivos de Linux a través de `\\wsl$` usará el usuario predeterminado de su WSL distribución. Por lo tanto, cualquier aplicación de Windows que tenga acceso a archivos de Linux tendrá los mismos permisos que el usuario predeterminado.

#### <a name="creating-a-new-file"></a>Crear un nuevo archivo

El valor predeterminado de umask se aplica al crear un nuevo archivo dentro de un distribución de WSL desde Windows. El valor predeterminado de umask es `022`, o en otras palabras permite todos los permisos excepto los permisos de escritura para grupos y otros. 

### <a name="accessing-files-in-the-linux-root-file-system-from-linux"></a>Acceso a los archivos del sistema de archivos raíz de Linux desde Linux

Los archivos creados, modificados o a los que se tiene acceso en el sistema de archivos raíz de Linux siguen las convenciones estándar de Linux, como la aplicación de umask a un archivo recién creado.

## <a name="configuring-file-permissions"></a>Configuración de permisos de archivo

Puede configurar los permisos de archivo dentro de las unidades de Windows mediante las opciones de montaje de WSL. conf. Las opciones de montaje permiten establecer `umask`, `dmask` y `fmask` las máscaras de permisos. El `umask` se aplica a todos los archivos, el `dmask` se aplica solo a los directorios y el `fmask` se aplica solo a los archivos. Estas máscaras de permisos se colocan a continuación a través de una operación OR lógica cuando se aplican a archivos, por ejemplo: Si tiene un valor `umask` de `023` y un valor `fmask` de `022`, se `023`la máscara de permisos resultante para los archivos. 

Consulte la página del documento sobre la [Administración de distribuciones de Linux](./wsl-config.md) para obtener instrucciones sobre cómo hacerlo.
<!-- TODO: Add # to the link-->

