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
# <a name="updating-the-wsl-2-linux-kernel"></a><span data-ttu-id="18799-104">Actualización del kernel de Linux en WSL 2</span><span class="sxs-lookup"><span data-stu-id="18799-104">Updating the WSL 2 Linux kernel</span></span>

<span data-ttu-id="18799-105">Para actualizar manualmente el kernel de Linux dentro de WSL 2, sigue estos pasos.</span><span class="sxs-lookup"><span data-stu-id="18799-105">To manually update the Linux kernel inside of WSL 2 please follow these steps.</span></span>

> [!NOTE] 
> <span data-ttu-id="18799-106">Si el instalador no encuentra WSL 1, haz clic con el botón derecho en el instalador de actualizaciones del kernel de Linux, presiona "Desinstalar" y, luego, vuelve a ejecutar el instalador.</span><span class="sxs-lookup"><span data-stu-id="18799-106">If the installer can't find WSL 1, right-click the Linux kernel update installer and press "Uninstall", then rerun the installer.</span></span>

## <a name="download-the-linux-kernel-update-package"></a><span data-ttu-id="18799-107">Descarga del paquete de actualización del kernel de Linux</span><span class="sxs-lookup"><span data-stu-id="18799-107">Download the Linux kernel update package</span></span>

<span data-ttu-id="18799-108">Descarga el paquete de actualización [más reciente del kernel de Linux en WSL 2](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) para máquinas x64.</span><span class="sxs-lookup"><span data-stu-id="18799-108">Please [download the latest WSL2 Linux kernel](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) update package for x64 machines.</span></span>

> [!NOTE]
> <span data-ttu-id="18799-109">Si estás usando una máquina ARM64, descarga el [paquete ARM64](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="18799-109">If you're using an ARM64 machine, please download the [ARM64 package](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) instead.</span></span>

## <a name="install-the-linux-kernel-update-package"></a><span data-ttu-id="18799-110">Instalación del paquete de actualización del kernel de Linux</span><span class="sxs-lookup"><span data-stu-id="18799-110">Install the Linux kernel update package</span></span>

<span data-ttu-id="18799-111">Para instalar el paquete de actualización del kernel de Linux:</span><span class="sxs-lookup"><span data-stu-id="18799-111">To install the Linux kernel update package:</span></span>

  1. <span data-ttu-id="18799-112">Ejecuta el paquete de actualización que descargaste en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="18799-112">Run the update package downloaded in the previous step.</span></span>

  2. <span data-ttu-id="18799-113">Se te pedirán permisos elevados, selecciona "Sí" para aprobar esta instalación.</span><span class="sxs-lookup"><span data-stu-id="18799-113">You will be prompted for elevated permissions, select ‘yes’ to approve this installation.</span></span>

  3. <span data-ttu-id="18799-114">Una vez que se complete la instalación, estarás listo para empezar a usar WSL2.</span><span class="sxs-lookup"><span data-stu-id="18799-114">Once the installation is complete, you are ready to begin using WSL2!</span></span>

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a><span data-ttu-id="18799-115">Planes futuros para actualizar el kernel de Linux en WSL2</span><span class="sxs-lookup"><span data-stu-id="18799-115">Future plans for updating the WSL2 Linux kernel</span></span>

<span data-ttu-id="18799-116">Para obtener más información, consulta el artículo [cambios en la actualización del kernel de Linux en WSL2](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004), disponible en el [blog de la línea de comandos de Windows](https://aka.ms/cliblog).</span><span class="sxs-lookup"><span data-stu-id="18799-116">For more information, read the article [changes to updating the WSL2 Linux kernel](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004), available on the [Windows Command Line Blog](https://aka.ms/cliblog).</span></span>
