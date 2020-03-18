---
title: Actualización del kernel de Linux en WSL 2
description: Instrucciones sobre cómo actualizar el kernel de Linux en WSL 2 manualmente
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, subsistemawindows, ubuntu, wsl.conf, wslconfig
ms.date: 03/12/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.localizationpriority: high
ms.custom: seodec18
ms.openlocfilehash: f7fce13c2acc65e3afa2cc56873e40bc55a460bc
ms.sourcegitcommit: 506272bd7fc1cbda7e32146d54a8bdd02af3e0c4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/13/2020
ms.locfileid: "79319715"
---
# <a name="updating-the-wsl-2-linux-kernel"></a><span data-ttu-id="f3169-104">Actualización del kernel de Linux en WSL 2</span><span class="sxs-lookup"><span data-stu-id="f3169-104">Updating the WSL 2 Linux kernel</span></span>

<span data-ttu-id="f3169-105">Para actualizar manualmente el kernel de Linux dentro de WSL 2, sigue estos pasos.</span><span class="sxs-lookup"><span data-stu-id="f3169-105">To manually update the Linux kernel inside of WSL 2 please follow these steps.</span></span> 

## <a name="download-the-linux-kernel-update-package"></a><span data-ttu-id="f3169-106">Descarga del paquete de actualización del kernel de Linux</span><span class="sxs-lookup"><span data-stu-id="f3169-106">Download the Linux kernel update package</span></span>

<span data-ttu-id="f3169-107">Haz clic en [este vínculo](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) para descargar el paquete de actualización más reciente del kernel de Linux en WSL2 para máquinas AMD64.</span><span class="sxs-lookup"><span data-stu-id="f3169-107">Please click on [this link](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) to download the latest WSL2 Linux kernel update package for AMD64 machines.</span></span>

> [!NOTE] 
> <span data-ttu-id="f3169-108">Si está usando una máquinas ARM64, descarga [este paquete](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="f3169-108">If you're using an ARM64 machine, please download [this package](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) instead.</span></span>

## <a name="install-the-linux-kernel-update-package"></a><span data-ttu-id="f3169-109">Instalación del paquete de actualización del kernel de Linux</span><span class="sxs-lookup"><span data-stu-id="f3169-109">Install the Linux kernel update package</span></span>

<span data-ttu-id="f3169-110">Para instalar el paquete de actualización del kernel de Linux:</span><span class="sxs-lookup"><span data-stu-id="f3169-110">To install the Linux kernel update package:</span></span>

    1. <span data-ttu-id="f3169-111">Ejecuta el paquete de actualización que descargaste en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="f3169-111">Run the update package downloaded in the previous step.</span></span>
    2. <span data-ttu-id="f3169-112">Se te pedirán permisos elevados, selecciona "Sí" para aprobar esta instalación.</span><span class="sxs-lookup"><span data-stu-id="f3169-112">You will be prompted for elevated permissions, select ‘yes’ to approve this installation.</span></span>
    3. <span data-ttu-id="f3169-113">Una vez que se complete la instalación, estarás listo para empezar a usar WSL2.</span><span class="sxs-lookup"><span data-stu-id="f3169-113">Once the installation is complete, you are ready to begin using WSL2!</span></span>

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a><span data-ttu-id="f3169-114">Planes futuros para actualizar el kernel de Linux en WSL2</span><span class="sxs-lookup"><span data-stu-id="f3169-114">Future plans for updating the WSL2 Linux kernel</span></span>

<span data-ttu-id="f3169-115">Para más información sobre estos cambios, lee [esta entrada de blog](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004) en el [blog de la línea de comandos de Windows](https://aka.ms/cliblog).</span><span class="sxs-lookup"><span data-stu-id="f3169-115">For more info on these changes, please read [this blog post](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004) on the [Windows Command Line Blog](https://aka.ms/cliblog).</span></span>
