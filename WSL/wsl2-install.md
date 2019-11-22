---
title: Instalación de WSL 2
description: Instrucciones de instalación de WSL 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, subsistema de windows para linux, subsistemawindows, ubuntu, debian, suse, windows 10, instalación
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: a53e6a986813809d0c355b80b3fe3028adb21375
ms.sourcegitcommit: 73f4cc6ac9482ea9727f3cda0ec5c3572e164256
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2019
ms.locfileid: "74309047"
---
# <a name="installation-instructions-for-wsl-2"></a>Instrucciones de instalación de WSL 2

Para instalar y empezar a usar WSL 2, sigue estos pasos:

> WSL 2 is only available in Windows 10 builds 18917 or higher

- Ensure that you have WSL installed (you can find instructions to do so [here](./install-win10.md)) and that you are running Windows 10 **build 18917** or higher
   - To make sure you are using build 18917 or higher please join [the Windows Insider Program](https://insider.windows.com/en-us/) and select the 'Fast' ring. 
   - You can check your Windows version by opening Command Prompt and running the `ver` command.
- Habilitación del componente opcional "Plataforma de máquina virtual"
- Establecimiento de una distribución que respaldará WSL 2 mediante la línea de comandos
- Comprobación de qué versiones de WSL están usando las distribuciones

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a>Enable the 'Virtual Machine Platform' optional component and make sure WSL is enabled

You will need to make sure that you have both the Windows Subsystem for Linux and the Virtual Machine Platform optional components installed. You can do that by running the following command in PowerShell: 

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

Please restart your machine to finish installing both components.


## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a>Establecimiento de una distribución que respaldará WSL 2 mediante la línea de comandos

If you do not have a Linux distro installed, please refer to the [Install on Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) docs page for instructions on installing one. 

To set a distro please run: 

```
wsl --set-version <Distro> 2
```

Asegúrate de reemplazar `<Distro>` por el nombre real de tu distribución. (Puedes encontrarlo con el comando: `wsl -l`). Puedes volver a cambiar a WSL 1 en cualquier momento; para ello, ejecuta el mismo comando que antes, pero reemplaza "2" por "1".

Además, si quieres que WSL 2 sea la arquitectura predeterminada, puedes hacerlo con este comando:

```
wsl --set-default-version 2
```

Esto hará que las nuevas distribuciones que instales se inicialicen como distribución de WSL 2.

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a>Comprobación final de qué versiones de WSL están usando las distribuciones

To verify what versions of WSL each distro is using use the following command (only available in Windows Build 18917 or higher):

`wsl --list --verbose` o `wsl -l -v`

La distribución que has elegido anteriormente debería mostrar ahora un "2" en la columna "version" (versión). Ahora que ya has completado los pasos, puedes empezar a usar tu distribución de WSL 2. 

## <a name="troubleshooting"></a>Solución de problemas: 

A continuación se muestran errores relacionados con la instalación de WSL 2 y las correcciones sugeridas. Consulta la [página de solución de problemas de WSL](troubleshooting.md) para ver otros errores generales de WSL y sus soluciones.

* **Error en la instalación 0x80070003 o 0x80370102**
    * Asegúrate de que la virtualización está habilitada dentro del BIOS del equipo. Las instrucciones sobre cómo hacerlo variarán de un equipo a otro y lo más probable es que esta característica esté en opciones relacionadas con la CPU.
   
* **Error al intentar actualizar: `Invalid command line option: wsl --set-version Ubuntu 2`**
    * Asegúrate de que tienes el Subsistema de Windows para Linux habilitado y de que estás usando la compilación 18917 de Windows o posterior. Para habilitar WSL, ejecuta este comando en un símbolo del sistema de PowerShell con privilegios de administrador: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`. Puedes encontrar las instrucciones de instalación de WSL completas [aquí](./install-win10.md).

* **The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**
    * Please check [WSL Github thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.

* **The term 'wsl' is not recognized as the name of a cmdlet, function, script file, or operable program.** 
    * Ensure that the [Windows Subsystem for Linux Optional Component is installed](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled).<br> Additionally, if you are using an Arm64 device and running this command from PowerShell, you will receive this error. Instead run `wsl.exe` from [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6), or Command Prompt. 
