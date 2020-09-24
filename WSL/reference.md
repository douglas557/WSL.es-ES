---
title: Material de referencia de comandos del subsistema de Windows para Linux
description: Vea una lista de comandos que administran el Subsistema de Windows para Linux, como argumentos para ejecutar comandos de Linux.
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, subsistemawindows, ubuntu
ms.date: 09/15/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 6f98cb7b238e4b38c1a931a0e77e419efbcc319d
ms.sourcegitcommit: ba3399a5ffeffd23551315acd04ea6848d30693b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/17/2020
ms.locfileid: "90719174"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a>Material de referencia de comandos del subsistema de Windows para Linux

La mejor manera de interactuar con el subsistema de Windows para Linux es usar el comando `wsl.exe`.

## <a name="set-wsl-2-as-your-default-version"></a>Definición de WSL 2 como versión predeterminada

Ejecuta el siguiente comando en PowerShell para establecer WSL 2 como versión predeterminada al instalar una nueva distribución de Linux:

```powershell
wsl --set-default-version 2
```

## <a name="set-your-distribution-version-to-wsl-1-or-wsl-2"></a>Definición de la versión de la distribución en WSL 1 o WSL 2

Para comprobar la versión de WSL asignada a cada una de las distribuciones de Linux que tienes instaladas, abre la línea de comandos de PowerShell y escribe el comando (solo disponible en [Windows, compilación 19041 o posterior](ms-settings:windowsupdate)) `wsl -l -v`.

```bash
wsl --list --verbose
```

Para establecer que una distribución esté respaldada por una de las dos versiones de WSL, ejecuta:

```bash
wsl --set-version <distribution name> <versionNumber>
```

Asegúrate de reemplazar `<distribution name>` por el nombre real de tu distribución, y `<versionNumber>` por el número "1" o "2". Puedes volver a cambiar a WSL 1 en cualquier momento; para ello, ejecuta el mismo comando que antes, pero reemplaza "2" por "1".

Además, si quieres que WSL 2 sea la arquitectura predeterminada, puedes hacerlo con este comando:

```bash
wsl --set-default-version 2
```

De este modo, se establecerá la versión de cualquier nueva distribución instalada en WSL 2.

## `wsl.exe`

A continuación, se muestra una lista con todas las opciones cuando se usa `wsl.exe` a partir de la versión 1903 de Windows.

Con `wsl [Argument] [Options...] [CommandLine]`

### <a name="arguments-for-running-linux-commands"></a>Argumentos para la ejecución de comandos de Linux

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

#### <a name="arguments"></a>Argumentos

* **/l, /list [Options]**
  
  Enumera las distribuciones registradas.
  
Opciones:

* **/all**: opcionalmente, enumera todas las distribuciones, incluidas aquellas que se están instalando o desinstalando.

* **/running**: enumera solo las distribuciones que se encuentran en ejecución actualmente.

* **/s, /setdefault \<Distro>** : establece la distribución como predeterminada.

* **/t, /terminate \<Distro>** : finaliza la distribución.

* **/u, /unregister \<Distro>** : anula el registro de la distribución.

* **/upgrade \<Distro>** : actualiza la distribución al formato del sistema de archivos de WslFs.

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

El comando `lxrun.exe` se puede usar para interactuar con el subsistema de Windows para Linux (WSL) directamente.  Estos comandos se instalan en el directorio `\Windows\System32` y se pueden ejecutar en un símbolo del sistema de Windows o en PowerShell.

| Comando                     | Descripción                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | El comando lxrun se usa para administrar la instancia de WSL. |
| `lxrun /install`            | Inicia el proceso de descarga e instalación. <br/> **/y** se puede agregar para omitir todos los mensajes.  El mensaje de confirmación se acepta automáticamente y el usuario predeterminado se establece en raíz.          |
| `lxrun /uninstall`          | Desinstala y elimina la imagen de Ubuntu.  De manera predeterminada, no se quita el directorio particular de Ubuntu del usuario. <br/> **/y** se puede agregar para aceptar automáticamente el mensaje de confirmación. <br/>**/full** desinstala y elimina el directorio particular de Ubuntu del usuario.         |
| `lxrun /setdefaultuser <userName>`     | Establece el valor predeterminado de Bash en el usuario de Ubuntu. Solicitará una contraseña si el usuario especificado no existe.  Para obtener más información, visita https://aka.ms/wslusers. <br/> **/y** omite la solicitud de confirmación de la contraseña.  El usuario se creará sin contraseña.|
| `lxrun /update`            | Actualiza el índice de paquetes del subsistema.          |
