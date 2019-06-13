---
title: Instalación de WSL 2
description: Instrucciones de instalación de WSL 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, el subsistema de windows para linux, windowssubsystem, ubuntu, debian, suse, windows 10, instalar
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 2af43a046333fc8c7b4142cdc5077cdfbf29fea7
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038085"
---
# <a name="installation-instructions-for-wsl-2"></a>Instrucciones de instalación de WSL 2

Para instalar y empezar a usar 2 WSL complete los pasos siguientes:

- Habilitar el componente opcional 'Plataforma de máquina Virtual'
- Establezca una distribución estar respaldados por 2 WSL mediante la línea de comandos
- Compruebe lo que usa las versiones de sus distribuciones WSL

## <a name="enable-the-virtual-machine-platform-optional-component"></a>Habilitar el componente opcional 'Plataforma de máquina Virtual'

Abra PowerShell como administrador y ejecute:

`Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform`

Después de que estos cambios se habilitan deberá reiniciar el equipo.

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a>Establezca una distribución estar respaldados por 2 WSL mediante la línea de comandos

En la ejecución de PowerShell:

`wsl --set-version <Distro> 2`

y no olvide reemplazar `<Distro>` con el nombre real de su distribución. (Puede encontrar estos elementos con el comando: `wsl -l`). Puede cambiar a 1 WSL en cualquier momento mediante la ejecución del mismo comando que antes, pero reemplazando ' 2' con ' 1'.

Además, si desea realizar la arquitectura predeterminada de WSL 2 puede hacerlo con este comando:

`wsl --set-default-version 2`

Esto hará que cualquier inicializarse distribución nueva que se instala como una distribución de WSL 2.

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a>Finalizar con la comprobación de que utiliza versiones de la distribución WSL

Para comprobar qué versiones de WSL está usando cada distribución utilizan el siguiente comando:

`wsl --list --verbose` o `wsl -l -v`

La distribución que eligió anteriormente debe mostrar ahora '2' en la columna 'version'. Ahora que haya terminado no dude en empezar a usar la distribución de WSL 2. 