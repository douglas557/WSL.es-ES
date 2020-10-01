---
title: Permisos de archivo
description: Descripción de cómo WSL determina los permisos de archivo en Windows
keywords: BashOnWindows, bash, wsl, wsl2, windows, subsistema de windows para linux, subsistemawindows, ubuntu, debian, suse, windows 10, archivo, permisos
ms.date: 01/14/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.localizationpriority: high
ms.openlocfilehash: 3de8553baf616ee8d5d45f0738615f83df952942
ms.sourcegitcommit: b15b847b87d29a40de4a1517315949bce9c7a3d5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "91413226"
---
# <a name="file-permissions-for-wsl"></a>Permisos de archivo para WSL

En esta página se detalla cómo se interpretan los permisos de archivo de Linux en el Subsistema de Windows para Linux, en especial al acceder a recursos dentro de Windows en el sistema de archivos NT. En esta documentación se supone que tienes un conocimiento básico de la [estructura de permisos del sistema de archivos de Linux](https://wiki.archlinux.org/index.php/File_permissions_and_attributes) y del [comando umask](https://en.wikipedia.org/wiki/Umask).

Al acceder a los archivos de Windows desde WSL, los permisos de archivo se calculan a partir de los permisos de Windows o se leen de los metadatos que WSL ha agregado al archivo. Estos metadatos no están habilitados de forma predeterminada.

## <a name="wsl-metadata-on-windows-files"></a>Metadatos de WSL en archivos de Windows

Cuando los metadatos están habilitados como opción de montaje en WSL, se pueden agregar e interpretar atributos extendidos en archivos de Windows NT para proporcionar los permisos del sistema de archivos de Linux.

WSL puede agregar cuatro atributos extendidos de NTFS:

| Nombre del atributo | Descripción |
| --- | --- |
| $LXUID | Id. del propietario del usuario |
| $LXGID | Id. del propietario del grupo |
| $LXMOD | Modo de archivo (octales y tipo de permisos de sistemas de archivos; por ejemplo: 0777) |
| $LXDEV | Dispositivo, si es un archivo de dispositivo |

Además, cualquier archivo que no sea un archivo o directorio normal (por ejemplo, vínculos simbólicos, FIFO [PEPS], dispositivos de bloques, sockets de UNIX y dispositivos de caracteres) también tiene un [punto de repetición de análisis](/windows/win32/fileio/reparse-points) de NTFS. De este modo, es mucho más rápido determinar el tipo de archivo en un directorio específico sin tener que consultar sus atributos extendidos.

## <a name="file-access-scenarios"></a>Escenarios de acceso a archivos

A continuación, se muestra una descripción de cómo se determinan los permisos al acceder a los archivos de diferentes maneras con el Subsistema de Windows para Linux.

### <a name="accessing-files-in-the-windows-drive-file-system-drvfs-from-linux"></a>Acceso a archivos en el sistema de archivos de la unidad de Windows (DrvFS) desde Linux

Estos escenarios se producen cuando accedes a los archivos de Windows desde WSL, más probablemente a través de `/mnt/c`.

#### <a name="reading-file-permissions-from-an-existing-windows-file"></a>Lectura de los permisos de un archivo de Windows existente

El resultado depende de si el archivo ya tiene metadatos.

##### <a name="drvfs-file-does-not-have-metadata-default"></a>El archivo DrvFS no tiene metadatos (valor predeterminado)

Si el archivo no tiene metadatos asociados, convertimos los permisos vigentes del usuario de Windows en bits de lectura, escritura o ejecución, y los establecemos en el mismo valor para el usuario, el grupo y otros. Por ejemplo, si tu cuenta de usuario de Windows tiene acceso de lectura y ejecución, pero no tiene acceso de escritura al archivo, se mostrará como `r-x` para el usuario, el grupo y otros. Si el archivo tiene el atributo "Solo lectura" establecido en Windows, no concederemos el acceso de escritura en Linux.

##### <a name="the-file-has-metadata"></a>El archivo tiene metadatos

Si el archivo tiene metadatos, simplemente usamos esos valores de metadatos en lugar de convertir los permisos vigentes del usuario de Windows.

#### <a name="changing-file-permissions-on-an-existing-windows-file-using-chmod"></a>Cambio de los permisos de archivo de un archivo de Windows existente mediante chmod

El resultado depende de si el archivo ya tiene metadatos existentes.

##### <a name="chmod-file-does-not-have-metadata-default"></a>El archivo chmod no tiene metadatos (valor predeterminado)

Chmod solo tendrá un efecto. Si quitas todos los atributos de escritura de un archivo, se establecerá el atributo "Solo lectura" en el archivo de Windows, ya que se trata del mismo comportamiento de CIFS (Sistema de archivos de Internet común), que es el cliente SMB (Bloque de mensajes del servidor) en Linux.

##### <a name="chmod-file-has-metadata"></a>El archivo chmod tiene metadatos

Chmod cambiará o agregará metadatos en función de los metadatos ya existentes del archivo. 

Ten en cuenta que no puedes concederte un mayor acceso del que tienes en Windows, aunque los metadatos indiquen lo contrario. Por ejemplo, podrías establecer los metadatos para mostrar que tienes permisos de escritura en un archivo mediante `chmod 777`, pero si intentas acceder a ese archivo, tampoco podrás escribir en él. Esto se debe a la interoperabilidad, ya que los comandos de lectura o escritura en los archivos de Windows se enrutan a través de los permisos de usuario de Windows.

#### <a name="creating-a-file-in-drivefs"></a>Creación de un archivo en DriveFS

El resultado depende de si los metadatos están habilitados.

##### <a name="metadata-is-not-enabled-default"></a>Los metadatos no están habilitados (valor predeterminado)

Los permisos de Windows del archivo recién creado serán los mismos que si creas el archivo en Windows sin un descriptor de seguridad específico. Este heredará los permisos del elemento primario.

##### <a name="metadata-is-enabled"></a>Los metadatos están habilitados

Los bits de permiso del archivo se establecen para seguir el comando umask de Linux, y el archivo se guardará con metadatos.

#### <a name="which-linux-user-and-linux-group-owns-the-file"></a>¿Qué usuario y grupo de Linux son propietarios del archivo? 

El resultado depende de si el archivo ya tiene metadatos existentes.

##### <a name="user-file-does-not-have-metadata-default"></a>El archivo de usuario no tiene metadatos (valor predeterminado)

En el escenario predeterminado, al montar las unidades de Windows de forma automática, especificamos que el identificador de usuario (UID) de cualquier archivo se establece en el identificador del usuario de WSL, y el identificador de grupo (GID) se establece en el identificador de grupo principal del usuario de WSL.

##### <a name="user-file-has-metadata"></a>El archivo de usuario tiene metadatos

El UID y el GID especificados en los metadatos se aplican como propietario del usuario y del grupo del archivo.

### <a name="accessing-linux-files-from-windows-using-wsl"></a>Acceso a archivos de Linux desde Windows mediante `\\wsl$`

El acceso a los archivos de Linux a través de `\\wsl$` usará el usuario predeterminado de la distribución de WSL. Por lo tanto, cualquier aplicación de Windows que acceda a archivos de Linux tendrá los mismos permisos que el usuario predeterminado.

#### <a name="creating-a-new-file"></a>Creación de un archivo nuevo

El valor de umask predeterminado se aplica al crear un nuevo archivo dentro de una distribución de WSL desde Windows. Dicho valor es `022` o, en otras palabras, permite todos los permisos excepto los de escritura para grupos y otros. 

### <a name="accessing-files-in-the-linux-root-file-system-from-linux"></a>Acceso a archivos en el sistema de archivos raíz de Linux desde Linux

Los archivos creados, modificados o a los que se accede en el sistema de archivos raíz de Linux siguen las convenciones estándar de Linux, como la aplicación de umask a un archivo recién creado.

## <a name="configuring-file-permissions"></a>Configuración de permisos de archivo

Puedes configurar los permisos de archivo dentro de las unidades de Windows mediante las opciones de montaje de wsl.conf. Las opciones de montaje te permiten establecer las máscaras de permisos `umask`, `dmask` y `fmask`. `umask` se aplica a todos los archivos, `dmask` se aplica solo a los directorios y `fmask` se aplica solo a los archivos. Luego, estas máscaras de permisos se someten a una operación OR lógica cuando se aplican a archivos, por ejemplo: Si tienes un valor de `umask` de `023` y uno de `fmask` de `022`, la máscara de permisos resultante para los archivos será `023`.

Consulte el artículo [Configuración de las opciones de inicio por distribución con wslconf](./wsl-config.md#configure-per-distro-launch-settings-with-wslconf) para obtener instrucciones sobre cómo hacerlo.