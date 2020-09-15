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
# <a name="release-notes-for-windows-subsystem-for-linux-kernel"></a><span data-ttu-id="ea24f-105">Notas de la versión del Subsistema de Windows para el kernel de Linux</span><span class="sxs-lookup"><span data-stu-id="ea24f-105">Release Notes for Windows Subsystem for Linux kernel</span></span>

<span data-ttu-id="ea24f-106">Hemos agregado compatibilidad con distribuciones de WSL 2, [que usan un kernel de Linux completo](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/).</span><span class="sxs-lookup"><span data-stu-id="ea24f-106">We've added support for WSL 2 distributions, [which use a full Linux kernel](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/).</span></span> <span data-ttu-id="ea24f-107">Este kernel de Linux es de código abierto y su código fuente está disponible en el repositorio [WSL2-Linux-Kernel](https://github.com/microsoft/WSL2-Linux-Kernel).</span><span class="sxs-lookup"><span data-stu-id="ea24f-107">This Linux kernel is open source, with its source code available at the [WSL2-Linux-Kernel](https://github.com/microsoft/WSL2-Linux-Kernel) repository.</span></span> <span data-ttu-id="ea24f-108">Este kernel de Linux se entrega al equipo a través de Microsoft Update, y sigue una programación de versiones independiente del Subsistema de Windows para Linux, que se entrega como parte de la imagen de Windows.</span><span class="sxs-lookup"><span data-stu-id="ea24f-108">This Linux kernel is delivered to your machine via Microsoft Update, and follows a separate release schedule to the Windows Subsystem for Linux which is delivered as part of the Windows image.</span></span>

## <a name="419128-microsoft-standard"></a><span data-ttu-id="ea24f-109">4.19.128-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="ea24f-109">4.19.128-microsoft-standard</span></span>
<span data-ttu-id="ea24f-110">*Fecha de lanzamiento*: versión preliminar y disponible a través de la instalación manual</span><span class="sxs-lookup"><span data-stu-id="ea24f-110">*Release Date*: Prerelease and available via manual install</span></span>

<span data-ttu-id="ea24f-111">[Vínculo a la versión oficial de GitHub](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.128-microsoft-standard).</span><span class="sxs-lookup"><span data-stu-id="ea24f-111">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.128-microsoft-standard).</span></span>

* <span data-ttu-id="ea24f-112">Versión estable de 4.19.128</span><span class="sxs-lookup"><span data-stu-id="ea24f-112">This is a stable release of 4.19.128</span></span>
* <span data-ttu-id="ea24f-113">Corrección de los daños en la memoria IOCTL del controlador dxgkrnl</span><span class="sxs-lookup"><span data-stu-id="ea24f-113">Fix dxgkrnl driver IOCTL memory corruption</span></span>

## <a name="419121-microsoft-standard"></a><span data-ttu-id="ea24f-114">4.19.121-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="ea24f-114">4.19.121-microsoft-standard</span></span>
<span data-ttu-id="ea24f-115">*Fecha de lanzamiento*: Versión preliminar</span><span class="sxs-lookup"><span data-stu-id="ea24f-115">*Release Date*: Prerelease</span></span>

<span data-ttu-id="ea24f-116">[Vínculo a la versión oficial de GitHub](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.121-microsoft-standard).</span><span class="sxs-lookup"><span data-stu-id="ea24f-116">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.121-microsoft-standard).</span></span>

* <span data-ttu-id="ea24f-117">Controladores: hv: vmbus: hook up dxgkrnl</span><span class="sxs-lookup"><span data-stu-id="ea24f-117">Drivers: hv: vmbus: hook up dxgkrnl</span></span>
* <span data-ttu-id="ea24f-118">Se ha agregado compatibilidad para el proceso de GPU</span><span class="sxs-lookup"><span data-stu-id="ea24f-118">Added support for GPU Compute</span></span>

## <a name="419104-microsoft-standard"></a><span data-ttu-id="ea24f-119">4.19.104-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="ea24f-119">4.19.104-microsoft-standard</span></span>
<span data-ttu-id="ea24f-120">*Fecha de lanzamiento*: 09/06/2020</span><span class="sxs-lookup"><span data-stu-id="ea24f-120">*Release Date*: 06/09/2020</span></span> 

<span data-ttu-id="ea24f-121">[Vínculo a la versión oficial de GitHub](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.104-microsoft-standard).</span><span class="sxs-lookup"><span data-stu-id="ea24f-121">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.104-microsoft-standard).</span></span>

* <span data-ttu-id="ea24f-122">Actualización de la configuración de WSL para 4.19.104</span><span class="sxs-lookup"><span data-stu-id="ea24f-122">Update WSL config for 4.19.104</span></span>

## <a name="41984-microsoft-standard"></a><span data-ttu-id="ea24f-123">4.19.84-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="ea24f-123">4.19.84-microsoft-standard</span></span>
<span data-ttu-id="ea24f-124">*Fecha de lanzamiento*: 12/11/2019</span><span class="sxs-lookup"><span data-stu-id="ea24f-124">*Release Date*: 11/12/2019</span></span> 

<span data-ttu-id="ea24f-125">[Vínculo a la versión oficial de GitHub](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.84-microsoft-standard).</span><span class="sxs-lookup"><span data-stu-id="ea24f-125">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.84-microsoft-standard).</span></span>

* <span data-ttu-id="ea24f-126">Versión estable de 4.19.84</span><span class="sxs-lookup"><span data-stu-id="ea24f-126">This is the 4.19.84 stable release</span></span>

