---
title: Instalación de WSL 2
description: Instrucciones de instalación de WSL 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, subsistema de windows para linux, subsistemawindows, ubuntu, debian, suse, windows 10, instalación
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 3ad180ecc9deaa1566e9870700b26f82f631c7f1
ms.sourcegitcommit: 9ad7a54668f39677e9660186e4f5172ea2597e2b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/16/2019
ms.locfileid: "68246863"
---
# <a name="installation-instructions-for-wsl-2"></a>Instrucciones de instalación de WSL 2

Para instalar y empezar a usar WSL 2, sigue estos pasos:

- Habilitación del componente opcional "Plataforma de máquina virtual"
- Establecimiento de una distribución que respaldará WSL 2 mediante la línea de comandos
- Comprobación de qué versiones de WSL están usando las distribuciones

Ten en cuenta que deberás usar la compilación 18917 de Windows 10 o posterior para utilizar WSL 2 y que deberás tener WSL ya instalado (puedes encontrar instrucciones para ello [aquí](./install-win10.md)). 

## <a name="enable-the-virtual-machine-platform-optional-component"></a>Habilitación del componente opcional "Plataforma de máquina virtual"

Abre PowerShell como administrador y ejecuta:

`Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform`

Una vez habilitados estos cambios, deberás reiniciar el equipo.

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a>Establecimiento de una distribución que respaldará WSL 2 mediante la línea de comandos

En PowerShell, ejecuta:

`wsl --set-version <Distro> 2`

Asegúrate de reemplazar `<Distro>` por el nombre real de tu distribución. (Puedes encontrarlo con el comando: `wsl -l`). Puedes volver a cambiar a WSL 1 en cualquier momento; para ello, ejecuta el mismo comando que antes, pero reemplaza "2" por "1".

Además, si quieres que WSL 2 sea la arquitectura predeterminada, puedes hacerlo con este comando:

`wsl --set-default-version 2`

Esto hará que las nuevas distribuciones que instales se inicialicen como distribución de WSL 2.

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a>Comprobación final de qué versiones de WSL están usando las distribuciones

Para comprobar qué versiones de WSL está usando cada distribución, usa el siguiente comando:

`wsl --list --verbose` o `wsl -l -v`

La distribución que has elegido anteriormente debería mostrar ahora un "2" en la columna "version" (versión). Ahora que ya has completado los pasos, puedes empezar a usar tu distribución de WSL 2. 

## <a name="troubleshooting"></a>Solución de problemas: 

A continuación se muestran errores relacionados con la instalación de WSL 2 y las correcciones sugeridas. Consulta la [página de solución de problemas de WSL](troubleshooting.md) para ver otros errores generales de WSL y sus soluciones.

* **Error en la instalación 0x80070003 o 0x80370102**
    * Asegúrate de que la virtualización está habilitada dentro del BIOS del equipo. Las instrucciones sobre cómo hacerlo variarán de un equipo a otro y lo más probable es que esta característica esté en opciones relacionadas con la CPU.
   
* **Error al intentar actualizar: `Invalid command line option: wsl --set-version Ubuntu 2`**
    * Asegúrate de que tienes el Subsistema de Windows para Linux habilitado y de que estás usando la compilación 18917 de Windows o posterior. Para habilitar WSL, ejecuta este comando en un símbolo del sistema de PowerShell con privilegios de administrador: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`. Puedes encontrar las instrucciones de instalación de WSL completas [aquí](./install-win10.md).