---
title: Actualización del kernel de Linux en WSL 2
description: Instrucciones sobre cómo actualizar el kernel de Linux en WSL 2 manualmente
keywords: wsl, windows, kernel de linux, subsistema de windows para linux, kernel
ms.date: 03/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 1628bea2f1bae590928b055425413e5b085dffef
ms.sourcegitcommit: 90f7caeefe886bf6c0ba2b90c1b56b5f9795ad1b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/28/2020
ms.locfileid: "84153051"
---
# <a name="updating-the-wsl-2-linux-kernel"></a>Actualización del kernel de Linux en WSL 2

Para actualizar manualmente el kernel de Linux dentro de WSL 2, sigue estos pasos.

> [!NOTE] 
> Si el instalador no encuentra WSL 1, haz clic con el botón derecho en el instalador de actualizaciones del kernel de Linux, presiona "Desinstalar" y, luego, vuelve a ejecutar el instalador.

## <a name="download-the-linux-kernel-update-package"></a>Descarga del paquete de actualización del kernel de Linux

Descarga el paquete de actualización [más reciente del kernel de Linux en WSL 2](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) para máquinas x64.

> [!NOTE]
> Si estás usando una máquina ARM64, descarga el [paquete ARM64](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) en su lugar.

## <a name="install-the-linux-kernel-update-package"></a>Instalación del paquete de actualización del kernel de Linux

Para instalar el paquete de actualización del kernel de Linux:

  1. Ejecuta el paquete de actualización que descargaste en el paso anterior.

  2. Se te pedirán permisos elevados, selecciona "Sí" para aprobar esta instalación.

  3. Una vez que se complete la instalación, estarás listo para empezar a usar WSL2.

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a>Planes futuros para actualizar el kernel de Linux en WSL2

Para obtener más información, consulta el artículo [cambios en la actualización del kernel de Linux en WSL2](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004), disponible en el [blog de la línea de comandos de Windows](https://aka.ms/cliblog).
