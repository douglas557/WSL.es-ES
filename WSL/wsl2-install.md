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
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="6ebd7-104">Instrucciones de instalación de WSL 2</span><span class="sxs-lookup"><span data-stu-id="6ebd7-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="6ebd7-105">Para instalar y empezar a usar 2 WSL complete los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="6ebd7-105">To install and start using WSL 2 complete the following steps:</span></span>

- <span data-ttu-id="6ebd7-106">Habilitar el componente opcional 'Plataforma de máquina Virtual'</span><span class="sxs-lookup"><span data-stu-id="6ebd7-106">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="6ebd7-107">Establezca una distribución estar respaldados por 2 WSL mediante la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="6ebd7-107">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="6ebd7-108">Compruebe lo que usa las versiones de sus distribuciones WSL</span><span class="sxs-lookup"><span data-stu-id="6ebd7-108">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component"></a><span data-ttu-id="6ebd7-109">Habilitar el componente opcional 'Plataforma de máquina Virtual'</span><span class="sxs-lookup"><span data-stu-id="6ebd7-109">Enable the 'Virtual Machine Platform' optional component</span></span>

<span data-ttu-id="6ebd7-110">Abra PowerShell como administrador y ejecute:</span><span class="sxs-lookup"><span data-stu-id="6ebd7-110">Open PowerShell as an Administrator and run:</span></span>

`Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform`

<span data-ttu-id="6ebd7-111">Después de que estos cambios se habilitan deberá reiniciar el equipo.</span><span class="sxs-lookup"><span data-stu-id="6ebd7-111">After these changes are enabled you will need to restart your computer.</span></span>

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="6ebd7-112">Establezca una distribución estar respaldados por 2 WSL mediante la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="6ebd7-112">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="6ebd7-113">En la ejecución de PowerShell:</span><span class="sxs-lookup"><span data-stu-id="6ebd7-113">In PowerShell run:</span></span>

`wsl --set-version <Distro> 2`

<span data-ttu-id="6ebd7-114">y no olvide reemplazar `<Distro>` con el nombre real de su distribución.</span><span class="sxs-lookup"><span data-stu-id="6ebd7-114">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="6ebd7-115">(Puede encontrar estos elementos con el comando: `wsl -l`).</span><span class="sxs-lookup"><span data-stu-id="6ebd7-115">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="6ebd7-116">Puede cambiar a 1 WSL en cualquier momento mediante la ejecución del mismo comando que antes, pero reemplazando ' 2' con ' 1'.</span><span class="sxs-lookup"><span data-stu-id="6ebd7-116">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="6ebd7-117">Además, si desea realizar la arquitectura predeterminada de WSL 2 puede hacerlo con este comando:</span><span class="sxs-lookup"><span data-stu-id="6ebd7-117">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

`wsl --set-default-version 2`

<span data-ttu-id="6ebd7-118">Esto hará que cualquier inicializarse distribución nueva que se instala como una distribución de WSL 2.</span><span class="sxs-lookup"><span data-stu-id="6ebd7-118">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="6ebd7-119">Finalizar con la comprobación de que utiliza versiones de la distribución WSL</span><span class="sxs-lookup"><span data-stu-id="6ebd7-119">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="6ebd7-120">Para comprobar qué versiones de WSL está usando cada distribución utilizan el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="6ebd7-120">To verify what versions of WSL each distro is using use the following command:</span></span>

<span data-ttu-id="6ebd7-121">`wsl --list --verbose` o `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="6ebd7-121">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="6ebd7-122">La distribución que eligió anteriormente debe mostrar ahora '2' en la columna 'version'.</span><span class="sxs-lookup"><span data-stu-id="6ebd7-122">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="6ebd7-123">Ahora que haya terminado no dude en empezar a usar la distribución de WSL 2.</span><span class="sxs-lookup"><span data-stu-id="6ebd7-123">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 