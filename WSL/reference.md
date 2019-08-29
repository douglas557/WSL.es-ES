---
title: Referencia de comandos de subsistema de Windows para Linux
description: Lista de comandos que administran el subsistema de Windows para Linux
keywords: BashOnWindows, bash, WSL, Windows, subsistema de Windows para Linux, windowssubsystem, Ubuntu
author: scooley
ms.author: scooley
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: edd4b8216a25f519e36b8b99b626b0a4315f6039
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122741"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a>Referencia de comandos para el subsistema de Windows para Linux

La mejor manera de interactuar con el subsistema de Windows para Linux es usar el `wsl.exe` comando. 


## `wsl.exe`

A continuación se muestra una lista con todas las `wsl.exe` opciones cuando se usa a partir de la versión 1903 de Windows.

Utilizan`wsl [Argument] [Options...] [CommandLine]`

### <a name="arguments-for-running-linux-binaries"></a>Argumentos para la ejecución de archivos binarios de Linux

* **Sin argumentos**

  Si no se proporciona ninguna línea de comandos, WSL. exe inicia el shell predeterminado.

* **--exec,-e \<línea de comandos >**
  
  Ejecute el comando especificado sin usar el shell de Linux predeterminado.

* **--**
  
  Pase el resto de la línea de comandos tal y como está.

Los comandos anteriores también aceptan las siguientes opciones:

* **--Distribution, \<-d distribución >**

  Ejecutar la distribución especificada.

* **--usuario,-u \<nombre de usuario >**

  Ejecutar como el usuario especificado.

### <a name="arguments-for-managing-windows-subsystem-for-linux"></a>Argumentos para administrar el subsistema de Windows para Linux

* **--export \<distribución > \<nombre de archivo >**
  
  Exporta la distribución a un archivo tar. El nombre de archivo puede ser-para la salida estándar.

* **--Import \<distribución > \<installLocation > \<nombreDeArchivo >**
  
  Importa el archivo tar especificado como una nueva distribución. El nombre de archivo puede ser-para la entrada estándar.

* **--List,-l [opciones]**
  
  Muestra las distribuciones.

  Opciones:
  * **--todos**
      
    Enumerar todas las distribuciones, incluidas las distribuciones que se están instalando o desinstalando actualmente.

  * **--en ejecución**
      
    Muestra solo las distribuciones que se están ejecutando actualmente.

* **--set-default,-s \<distribución >**
  
  Establece la distribución como valor predeterminado.

* **--Terminate,- \<t distribución >**
  
  Finaliza la distribución especificada.

* **--anular \<el registro de distribución >**
  
  Anula el registro de la distribución.
   
* **--Help** Mostrar información de uso.

## <a name="additional-commands"></a>Comandos adicionales

También hay comandos históricos para interactuar con el subsistema de Windows para Linux. Su funcionalidad se incluye en `wsl.exe`, pero siguen estando disponibles para su uso. 

### `wslconfig.exe`

Este comando le permite configurar la distribución de WSL. A continuación se muestra una lista de sus opciones.

Utilizan`wslconfig [Argument] [Options...]`

#### <a name="arguments"></a>Argumentos
* **/l,/list [opciones]**
  
  Muestra las distribuciones registradas.
  
  Opciones:
    * **/All**
    
      Opcionalmente, puede enumerar todas las distribuciones, incluidas las distribuciones que se están instalando o desinstalando.

    * **/running**
      
      Muestra solo las distribuciones que se están ejecutando actualmente.

* **/s,/setDefault \<distribución >**
  
  Establece la distribución como valor predeterminado.

* **/t,/Terminate. \<distribución >**
  
  Finaliza la distribución.

* **/u,/unregister \<distribución >**
  
  Anula el registro de la distribución.
   
* **/Upgrade \<distribución >**
  
  Actualiza la distribución al formato del sistema de archivos WslFs.

### `bash.exe`

Este comando se usa para iniciar un shell de Bash. A continuación se muestran las opciones que puede usar con este comando.

Utilizan`bash [Options...]`

* **No se ha especificado ninguna opción**
  
  Inicia el shell de bash en el directorio actual. Si el shell de Bash no se instala automáticamente, se ejecuta`lxrun /install`

* **~**
  
  `bash ~`inicia el shell de bash en el directorio principal del usuario.  Similar a Running `cd ~`.

* **-c "\<> de comandos"**
  
  Ejecuta el comando, imprime la salida y vuelve a salir del símbolo del sistema de Windows.
    
  Ejemplo: `bash -c "ls"`.

## <a name="deprecated-commands"></a>Comandos desusados

`lxrun.exe` Fue el primer comando que se usaba para instalar y administrar el subsistema de Windows para Linux. Está en desuso a partir de Windows 10 1803 y versiones posteriores.

El comando `lxrun.exe` se puede usar para interactuar directamente con el subsistema [de Windows para Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) .  Estos comandos se instalan en `\Windows\System32` el directorio y se pueden ejecutar en un símbolo del sistema de Windows o en PowerShell.

| Comando                     | Descripción                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | El comando lxrun se usa para administrar la instancia de WSL. |
| `lxrun /install`            | Inicia el proceso de descarga e instalación. <br/> se puede agregar **/y** para omitir todos los mensajes.  El mensaje de confirmación se acepta automáticamente y el usuario predeterminado se establece en root.          |
| `lxrun /uninstall`          | Desinstala y elimina la imagen de Ubuntu.  De forma predeterminada, no se quita el directorio de inicio de Ubuntu del usuario. <br/> se puede agregar **/y** para aceptar automáticamente el mensaje de confirmación. <br/>**/Full** desinstala y elimina el directorio principal de Ubuntu del usuario.         |
| `lxrun /setdefaultuser <userName>`     | Establece el valor predeterminado de bash en el usuario de Ubuntu. Solicitará una contraseña si el usuario especificado no existe.  Para obtener más información, https://aka.ms/wslusers visite:. <br/> **/y** Omite promping para la contraseña.  El usuario se creará sin una contraseña.|
| `lxrun /update`            | Actualiza el índice de paquetes del subsistema.          |
