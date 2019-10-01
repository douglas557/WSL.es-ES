---
title: Material de referencia de comandos del subsistema de Windows para Linux
description: Lista de comandos que administran el subsistema de Windows para Linux
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, subsistemawindows, ubuntu
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: d74a6926fd797f2e1ede0fd5d8d080d0f1ce3f6b
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269842"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a>Material de referencia de comandos del subsistema de Windows para Linux

La mejor manera de interactuar con el subsistema de Windows para Linux es usar el comando `wsl.exe`. 


## `wsl.exe`

A continuación, se muestra una lista con todas las opciones cuando se usa `wsl.exe` a partir de la versión 1903 de Windows.

Con `wsl [Argument] [Options...] [CommandLine]`

### <a name="arguments-for-running-linux-binaries"></a>Argumentos para la ejecución de archivos binarios de Linux

* **Sin argumentos**

  Si no se proporciona ninguna línea de comandos, wsl.exe inicia el shell predeterminado.

* **--exec, -e \<CommandLine>**
  
  Ejecuta el comando especificado sin usar el shell de Linux predeterminado.

* **--**
  
  Pasa el resto de la línea de comandos como está.

Los comandos anteriores también aceptan las siguientes opciones:

* **--distribution, -d \<Distro>**

  Ejecuta la distribución especificada.

* **--user, -u \<UserName>**

  Ejecuta como el usuario especificado.

### <a name="arguments-for-managing-windows-subsystem-for-linux"></a>Argumentos para administrar el subsistema de Windows para Linux

* **--export \<Distro> \<FileName>**
  
  Exporta la distribución a un archivo tar. El nombre de archivo puede ser - para la salida estándar.

* **--import \<Distro> \<InstallLocation> \<FileName>**
  
  Importa el archivo tar especificado como una nueva distribución. El nombre de archivo puede ser - para la entrada estándar.

* **--list, -l [Options]**
  
  Enumera distribuciones.

  Opciones:
  * **--all**
      
    Enumera todas las distribuciones, incluidas aquellas que se están instalando o desinstalando actualmente.

  * **--running**
      
    Enumera solo las distribuciones que están actualmente en ejecución.

* **--set-default, -s \<Distro>**
  
  Establece la distribución como predeterminada.

* **--terminate, -t \<Distro>**
  
  Finaliza la distribución especificada.

* **--unregister \<Distro>**
  
  Anula el registro de la distribución.
   
* **--help** Muestra información de uso.

## <a name="additional-commands"></a>Comandos adicionales

También hay comando históricos para interactuar con el subsistema de Windows para Linux. Su funcionalidad se incluye en `wsl.exe`, pero siguen estando disponibles para su uso. 

### `wslconfig.exe`

Este comando te permite configurar la distribución de WSL. A continuación, se muestra una lista de sus opciones.

Con `wslconfig [Argument] [Options...]`

#### <a name="arguments"></a>Arguments
* **/l, /list [Options]**
  
  Enumera las distribuciones registradas.
  
  Opciones:
    * **/all**
    
      Opcionalmente, enumera todas las distribuciones, incluidas aquellas que se están instalando o desinstalando actualmente.

    * **/running**
      
      Enumera solo las distribuciones que están actualmente en ejecución.

* **/s, /setdefault \<Distro>**
  
  Establece la distribución como predeterminada.

* **/t, /terminate \<Distro>**
  
  Finaliza la distribución.

* **/u, /unregister \<Distro>**
  
  Anula el registro de la distribución.
   
* **/upgrade \<Distro>**
  
  Actualiza la distribución al formato del sistema de archivos de WslFs.

### `bash.exe`

Este comando se usa para iniciar un shell de Bash. A continuación, se muestran las opciones que se pueden usar con este comando.

Con `bash [Options...]`

* **No se ha especificado ninguna opción**
  
  Inicia el shell de Bash en el directorio actual. Si el shell de Bash no se instala automáticamente, se ejecuta `lxrun /install`.

* **~**
  
  `bash ~` inicia el shell de Bash en el directorio particular del usuario.  Similar a la ejecución de `cd ~`.

* **-c "\<command>"**
  
  Ejecuta el comando, imprime la salida y vuelve a salir del símbolo del sistema de Windows.
    
  Ejemplo: `bash -c "ls"`.

## <a name="deprecated-commands"></a>Comandos en desuso

`lxrun.exe` fue el primer comando usado para instalar y administrar el subsistema de Windows para Linux. Está en desuso desde la versión 1803 de Windows 10 y versiones posteriores.

El comando `lxrun.exe` se puede usar para interactuar con el [subsistema de Windows para Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directamente.  Estos comandos se instalan en el directorio `\Windows\System32` y se pueden ejecutar en un símbolo del sistema de Windows o en PowerShell.

| Comando                     | Descripción                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | El comando lxrun se usa para administrar la instancia de WSL. |
| `lxrun /install`            | Inicia el proceso de descarga e instalación. <br/> **/y** se puede agregar para omitir todos los mensajes.  El mensaje de confirmación se acepta automáticamente y el usuario predeterminado se establece en raíz.          |
| `lxrun /uninstall`          | Desinstala y elimina la imagen de Ubuntu.  De manera predeterminada, no se quita el directorio particular de Ubuntu del usuario. <br/> **/y** se puede agregar para aceptar automáticamente el mensaje de confirmación. <br/>**/full** desinstala y elimina el directorio particular de Ubuntu del usuario.         |
| `lxrun /setdefaultuser <userName>`     | Establece el valor predeterminado de Bash en el usuario de Ubuntu. Solicitará una contraseña si el usuario especificado no existe.  Para obtener más información, visita https://aka.ms/wslusers. <br/> **/y** omite la solicitud de confirmación de la contraseña.  El usuario se creará sin contraseña.|
| `lxrun /update`            | Actualiza el índice de paquetes del subsistema.          |
