---
title: Actualización del kernel de Linux en WSL 2
description: Instrucciones sobre cómo actualizar el kernel de Linux en WSL 2 manualmente
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, subsistemawindows, ubuntu, wsl.conf, wslconfig
ms.date: 03/12/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.localizationpriority: high
ms.custom: seodec18
ms.openlocfilehash: a1a2f23fb05c426f80878e12e82026a96c71354e
ms.sourcegitcommit: 39d3a2f0f4184eaec8d8fec740aff800e8ea9ac7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/24/2020
ms.locfileid: "79447744"
---
# <a name="updating-the-wsl-2-linux-kernel"></a>Actualización del kernel de Linux en WSL 2

Para actualizar manualmente el kernel de Linux dentro de WSL 2, sigue estos pasos. 

## <a name="download-the-linux-kernel-update-package"></a>Descarga del paquete de actualización del kernel de Linux

Haz clic en [este vínculo](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) para descargar el paquete de actualización más reciente del kernel de Linux en WSL 2 para máquinas x64.

> [!NOTE] 
> Si está usando una máquinas ARM64, descarga [este paquete](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) en su lugar.

## <a name="install-the-linux-kernel-update-package"></a>Instalación del paquete de actualización del kernel de Linux

Para instalar el paquete de actualización del kernel de Linux:

    1. Ejecuta el paquete de actualización que descargaste en el paso anterior.
    2. Se te pedirán permisos elevados, selecciona "Sí" para aprobar esta instalación.
    3. Una vez que se complete la instalación, estarás listo para empezar a usar WSL2.

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a>Planes futuros para actualizar el kernel de Linux en WSL2

Para más información sobre estos cambios, lee [esta entrada de blog](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004) en el [blog de la línea de comandos de Windows](https://aka.ms/cliblog).
