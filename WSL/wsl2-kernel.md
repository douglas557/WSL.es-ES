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
# <a name="updating-the-wsl-2-linux-kernel"></a><span data-ttu-id="b2509-104">Actualización del kernel de Linux de WSL 2</span><span class="sxs-lookup"><span data-stu-id="b2509-104">Updating the WSL 2 Linux kernel</span></span>

<span data-ttu-id="b2509-105">Para actualizar manualmente el kernel de Linux dentro de WSL 2, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="b2509-105">To manually update the Linux kernel inside of WSL 2 please follow these steps.</span></span> 

## <a name="download-the-linux-kernel-update-package"></a><span data-ttu-id="b2509-106">Descargar el paquete de actualización del kernel de Linux</span><span class="sxs-lookup"><span data-stu-id="b2509-106">Download the Linux kernel update package</span></span>

<span data-ttu-id="b2509-107">Haga clic en [este vínculo](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) para descargar el paquete de actualización del kernel de Linux de WSL2 más reciente para las máquinas AMD64.</span><span class="sxs-lookup"><span data-stu-id="b2509-107">Please click on [this link](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) to download the latest WSL2 Linux kernel update package for AMD64 machines.</span></span>

> [!NOTE] <span data-ttu-id="b2509-108">Si está usando un equipo ARM64, descargue [este paquete](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="b2509-108">if you're using an ARM64 machine, please download [this package](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) instead.</span></span>

## <a name="install-the-linux-kernel-update-package"></a><span data-ttu-id="b2509-109">Instalación del paquete de actualización del kernel de Linux</span><span class="sxs-lookup"><span data-stu-id="b2509-109">Install the Linux kernel update package</span></span>

<span data-ttu-id="b2509-110">Para instalar el paquete de actualización del kernel de Linux:</span><span class="sxs-lookup"><span data-stu-id="b2509-110">To install the Linux kernel update package:</span></span>
    1. <span data-ttu-id="b2509-111">Ejecute el paquete de actualización descargado en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="b2509-111">Run the update package downloaded in the previous step.</span></span>
    2. <span data-ttu-id="b2509-112">Se le pedirán permisos elevados, seleccione "sí" para aprobar esta instalación.</span><span class="sxs-lookup"><span data-stu-id="b2509-112">You will be prompted for elevated permissions, select ‘yes’ to approve this installation.</span></span>
    3. <span data-ttu-id="b2509-113">Una vez completada la instalación, estará listo para empezar a usar WSL2.</span><span class="sxs-lookup"><span data-stu-id="b2509-113">Once the installation is complete, you are ready to begin using WSL2!</span></span>

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a><span data-ttu-id="b2509-114">Planes futuros para actualizar el kernel de Linux de WSL2</span><span class="sxs-lookup"><span data-stu-id="b2509-114">Future plans for updating the WSL2 Linux kernel</span></span>

<span data-ttu-id="b2509-115">Para obtener más información sobre estos cambios, lea [esta entrada de blog](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004) en el blog de la [línea de comandos de Windows](https://aka.ms/cliblog).</span><span class="sxs-lookup"><span data-stu-id="b2509-115">For more info on these changes, please read [this blog post](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004) on the [Windows Command Line Blog](https://aka.ms/cliblog).</span></span>