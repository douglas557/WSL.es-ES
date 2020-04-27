---
title: Instalación de WSL 2
description: Instrucciones de instalación de WSL 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, subsistema de windows para linux, subsistemawindows, ubuntu, debian, suse, windows 10, instalación
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 7c031b1348a77e1dac967fae5e4df772e10a9084
ms.sourcegitcommit: 39d3a2f0f4184eaec8d8fec740aff800e8ea9ac7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/24/2020
ms.locfileid: "80256348"
---
# <a name="installation-instructions-for-wsl-2"></a>Instrucciones de instalación de WSL 2

Puedes ver el vídeo siguiente o leer este artículo para obtener información sobre cómo instalar WSL 2. 

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Learn-how-to-install-WSL-2/player]

Para instalar y empezar a usar WSL 2, sigue estos pasos:

> WSL 2 solo está disponible en las compilaciones 18917 o posteriores de Windows 10.

- Asegúrate de tener WSL instalado (puedes encontrar instrucciones para hacerlo [aquí](./install-win10.md)) y de que estás ejecutando Windows 10, **compilación 18917** o posterior.
   - Para asegurarte de que estás usando la compilación 18917 o posterior, únete [al programa de Windows Insider](https://insider.windows.com/en-us/) y selecciona el anillo "rápido" o el anillo "lento". 
   - Para comprobar la versión de Windows, abre el símbolo del sistema y ejecuta el comando `ver`.
- Habilitación del componente opcional "Plataforma de máquina virtual"
- Establecimiento de una distribución que respaldará WSL 2 mediante la línea de comandos
- Comprobación de qué versiones de WSL están usando las distribuciones

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a>Habilitación del componente opcional "Plataforma de máquina virtual" y comprobación de la habilitación de WSL

Tendrás que asegurarse de tener instalados los componentes opcionales Subsistema de Windows para Linux y Plataforma de máquina virtual. Para hacerlo ejecuta el siguiente comando en PowerShell: 

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

Reinicia el equipo para finalizar la instalación de ambos componentes.


## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a>Establecimiento de una distribución que respaldará WSL 2 mediante la línea de comandos

Si no tienes una distribución de Linux instalada, consulta la página de documentación [Instalación en Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) para obtener instrucciones sobre cómo instalar una. 

Para establecer un distribución, ejecuta: 

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

Para comprobar qué versiones de WSL está usando cada distribución, usa el siguiente comando (disponible solamente en la compilación 18917 o posterior de Windows):

`wsl --list --verbose` o `wsl -l -v`

La distribución que has elegido anteriormente debería mostrar ahora un "2" en la columna "version" (versión). Ahora que ya has completado los pasos, puedes empezar a usar tu distribución de WSL 2. 

## <a name="troubleshooting"></a>Solución de problemas: 

A continuación se muestran errores relacionados con la instalación de WSL 2 y las correcciones sugeridas. Consulta la [página de solución de problemas de WSL](troubleshooting.md) para ver otros errores generales de WSL y sus soluciones.

* **Error en la instalación 0x80070003 o 0x80370102**
    * Asegúrate de que la virtualización está habilitada dentro del BIOS del equipo. Las instrucciones sobre cómo hacerlo variarán de un equipo a otro y lo más probable es que esta característica esté en opciones relacionadas con la CPU.
   
* **Error al intentar actualizar: `Invalid command line option: wsl --set-version Ubuntu 2`**
    * Asegúrate de que tienes el Subsistema de Windows para Linux habilitado y de que estás usando la compilación 18917 de Windows o posterior. Para habilitar WSL, ejecuta este comando en un símbolo del sistema de PowerShell con privilegios de administrador: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`. Puedes encontrar las instrucciones de instalación de WSL completas [aquí](./install-win10.md).

* **La operación solicitada no se pudo completar debido a una limitación del sistema de disco virtual. Los archivos de disco duro virtual deben estar sin comprimir y sin cifrar y no deben ser dispersos.**
    * Consulta el [subproceso #4103 sobre WSL en Github](https://github.com/microsoft/WSL/issues/4103), en el que se realiza el seguimiento de este problema para obtener información actualizada.

* **El término 'wsl' no se reconoce como nombre de cmdlet, función, archivo de script o programa ejecutable.** 
    * Asegúrate de que el [componente opcional del Subsistema de Windows para Linux esté instalado](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled).<br> Además, si usas un dispositivo Arm64 y ejecutas este comando desde PowerShell, recibirás este error. En su lugar, ejecuta `wsl.exe` desde [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6) o el símbolo del sistema. 
