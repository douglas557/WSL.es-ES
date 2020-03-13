---
title: Actualización del kernel de Linux de WSL 2
description: Instrucciones sobre cómo actualizar el kernel de Linux de WSL 2 manualmente
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, subsistemawindows, ubuntu, wsl.conf, wslconfig
ms.date: 03/12/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: edc7ea35d8ebe0c71488763017cde2bb45c53b6d
ms.sourcegitcommit: 8795e1c4c5d2efdc8a9c78af05fb7be3ac1eef3d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/12/2020
ms.locfileid: "79138194"
---
# <a name="updating-the-wsl-2-linux-kernel"></a>Actualización del kernel de Linux de WSL 2

Para actualizar manualmente el kernel de Linux dentro de WSL 2, siga estos pasos. 

## <a name="download-the-linux-kernel-update-package"></a>Descargar el paquete de actualización del kernel de Linux

Haga clic en [este vínculo](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) para descargar el paquete de actualización del kernel de Linux de WSL2 más reciente para las máquinas AMD64.

> [!NOTE] Si está usando un equipo ARM64, descargue [este paquete](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) en su lugar.

## <a name="install-the-linux-kernel-update-package"></a>Instalación del paquete de actualización del kernel de Linux

Para instalar el paquete de actualización del kernel de Linux:
    1. Ejecute el paquete de actualización descargado en el paso anterior.
    2. Se le pedirán permisos elevados, seleccione "sí" para aprobar esta instalación.
    3. Una vez completada la instalación, estará listo para empezar a usar WSL2.

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a>Planes futuros para actualizar el kernel de Linux de WSL2

Para obtener más información sobre estos cambios, lea [esta entrada de blog](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004) en el blog de la [línea de comandos de Windows](https://aka.ms/cliblog).