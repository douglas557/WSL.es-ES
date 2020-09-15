---
title: Notas de la versión del Subsistema de Windows para el kernel de Linux
description: Notas de la versión del subsistema de Windows para Linux.  Se actualiza mensualmente.
keywords: notas de la versión, wsl, windows, subsistema de windows para linux, windowssubsystem, ubuntu, kernel
ms.date: 06/09/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 32b65bcde3df01b25f0361493a172e754e78e101
ms.sourcegitcommit: 43d4056eefe0c71ecd9a0fbd5a7a58dd18fa9829
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "89615545"
---
# <a name="release-notes-for-windows-subsystem-for-linux-kernel"></a>Notas de la versión del Subsistema de Windows para el kernel de Linux

Hemos agregado compatibilidad con distribuciones de WSL 2, [que usan un kernel de Linux completo](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/). Este kernel de Linux es de código abierto y su código fuente está disponible en el repositorio [WSL2-Linux-Kernel](https://github.com/microsoft/WSL2-Linux-Kernel). Este kernel de Linux se entrega al equipo a través de Microsoft Update, y sigue una programación de versiones independiente del Subsistema de Windows para Linux, que se entrega como parte de la imagen de Windows.

## <a name="419128-microsoft-standard"></a>4.19.128-microsoft-standard
*Fecha de lanzamiento*: versión preliminar y disponible a través de la instalación manual

[Vínculo a la versión oficial de GitHub](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.128-microsoft-standard).

* Versión estable de 4.19.128
* Corrección de los daños en la memoria IOCTL del controlador dxgkrnl

## <a name="419121-microsoft-standard"></a>4.19.121-microsoft-standard
*Fecha de lanzamiento*: Versión preliminar

[Vínculo a la versión oficial de GitHub](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.121-microsoft-standard).

* Controladores: hv: vmbus: hook up dxgkrnl
* Se ha agregado compatibilidad para el proceso de GPU

## <a name="419104-microsoft-standard"></a>4.19.104-microsoft-standard
*Fecha de lanzamiento*: 09/06/2020 

[Vínculo a la versión oficial de GitHub](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.104-microsoft-standard).

* Actualización de la configuración de WSL para 4.19.104

## <a name="41984-microsoft-standard"></a>4.19.84-microsoft-standard
*Fecha de lanzamiento*: 12/11/2019 

[Vínculo a la versión oficial de GitHub](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.84-microsoft-standard).

* Versión estable de 4.19.84

