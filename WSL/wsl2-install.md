---
title: Instalación de WSL 2
description: Instrucciones de instalación de WSL 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, subsistema de windows para linux, subsistemawindows, ubuntu, debian, suse, windows 10, instalación
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: e3593aaf0e1c176cbeec2d3ba7d8eca1ede6b1ec
ms.sourcegitcommit: d74fab7469f4e589ab0bf4418be575381a3f72a0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2019
ms.locfileid: "73240364"
---
# <a name="installation-instructions-for-wsl-2"></a>Instrucciones de instalación de WSL 2

Para instalar y empezar a usar WSL 2, sigue estos pasos:

> WSL 2 solo está disponible en las compilaciones 18917 o posteriores de Windows 10.

- Asegúrese de que ha instalado WSL (puede encontrar instrucciones para hacerlo [aquí](./install-win10.md)) y de que está ejecutando Windows 10 **Build 18917** o superior.
   - Para asegurarse de que está usando la compilación 18917 o posterior, únase [al programa Windows Insider](https://insider.windows.com/en-us/) y seleccione el anillo "rápido". 
   - Para comprobar la versión de Windows, abra el símbolo del sistema y ejecute el comando `ver`.
- Habilitación del componente opcional "Plataforma de máquina virtual"
- Establecimiento de una distribución que respaldará WSL 2 mediante la línea de comandos
- Comprobación de qué versiones de WSL están usando las distribuciones

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a>Habilite el componente opcional "plataforma de máquina virtual" y asegúrese de que WSL está habilitado.

Abre PowerShell como administrador y ejecuta:

```powershell
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform
```

Así se asegurará de que se instalan los componentes opcionales de la plataforma de máquina virtual y el subsistema de Windows para Linux. Después de ejecutar estos comandos, deberá reiniciar el equipo. 

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a>Establecimiento de una distribución que respaldará WSL 2 mediante la línea de comandos

En PowerShell, ejecuta:

`wsl --set-version <Distro> 2`

Asegúrate de reemplazar `<Distro>` por el nombre real de tu distribución. (Puedes encontrarlo con el comando: `wsl -l`). Puedes volver a cambiar a WSL 1 en cualquier momento; para ello, ejecuta el mismo comando que antes, pero reemplaza "2" por "1".

Además, si quieres que WSL 2 sea la arquitectura predeterminada, puedes hacerlo con este comando:

`wsl --set-default-version 2`

Esto hará que las nuevas distribuciones que instales se inicialicen como distribución de WSL 2.

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a>Comprobación final de qué versiones de WSL están usando las distribuciones

Para comprobar qué versiones de WSL usa cada distribución, use el siguiente comando (solo disponible en Windows compilación 18917 o posterior):

`wsl --list --verbose` o `wsl -l -v`

La distribución que has elegido anteriormente debería mostrar ahora un "2" en la columna "version" (versión). Ahora que ya has completado los pasos, puedes empezar a usar tu distribución de WSL 2. 

## <a name="troubleshooting"></a>Solución de problemas: 

A continuación se muestran errores relacionados con la instalación de WSL 2 y las correcciones sugeridas. Consulta la [página de solución de problemas de WSL](troubleshooting.md) para ver otros errores generales de WSL y sus soluciones.

* **Error en la instalación 0x80070003 o 0x80370102**
    * Asegúrate de que la virtualización está habilitada dentro del BIOS del equipo. Las instrucciones sobre cómo hacerlo variarán de un equipo a otro y lo más probable es que esta característica esté en opciones relacionadas con la CPU.
   
* **Error al intentar actualizar: `Invalid command line option: wsl --set-version Ubuntu 2`**
    * Asegúrate de que tienes el Subsistema de Windows para Linux habilitado y de que estás usando la compilación 18917 de Windows o posterior. Para habilitar WSL, ejecuta este comando en un símbolo del sistema de PowerShell con privilegios de administrador: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`. Puedes encontrar las instrucciones de instalación de WSL completas [aquí](./install-win10.md).

* **No se pudo completar la operación solicitada debido a una limitación del sistema de disco virtual. Los archivos de disco duro virtual deben estar sin comprimir y sin cifrar y no deben ser dispersos.**
    * Consulte [WSL GitHub thread #4103](https://github.com/microsoft/WSL/issues/4103) en el que se realiza el seguimiento de este problema para obtener información actualizada.