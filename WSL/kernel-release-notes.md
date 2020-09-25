---
title: Notas de la versión del Subsistema de Windows para el kernel de Linux
description: Notas de la versión del subsistema de Windows para Linux.  Se actualiza mensualmente.
keywords: notas de la versión, wsl, windows, subsistema de windows para linux, windowssubsystem, ubuntu, kernel
ms.date: 06/09/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: eb93135355384013b93b4b5c4af03a582280febf
ms.sourcegitcommit: ba3399a5ffeffd23551315acd04ea6848d30693b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/17/2020
ms.locfileid: "90719124"
---
# <a name="release-notes-for-windows-subsystem-for-linux-kernel"></a>Notas de la versión del Subsistema de Windows para el kernel de Linux

Hemos agregado compatibilidad con distribuciones de WSL 2, [que usan un kernel de Linux completo](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/). Este kernel de Linux es de código abierto y su código fuente está disponible en el repositorio [WSL2-Linux-Kernel](https://github.com/microsoft/WSL2-Linux-Kernel). Este kernel de Linux se entrega al equipo a través de Microsoft Update, y sigue una programación de versiones independiente del Subsistema de Windows para Linux, que se entrega como parte de la imagen de Windows.

## <a name="419128-microsoft-standard"></a>4.19.128-microsoft-standard
*Fecha de lanzamiento*: 15/09/2020

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

