---
title: Actualización del kernel de Linux en WSL 2
description: Instrucciones sobre cómo actualizar el kernel de Linux en WSL 2 manualmente
keywords: wsl, windows, kernel de linux, subsistema de windows para linux, kernel
ms.date: 03/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 7bf2ef606d0bd23083f323117348aeea87c52b10
ms.sourcegitcommit: f1996541005ae126ef379d8aebfe1abfcccb9ac9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/25/2020
ms.locfileid: "91238805"
---
# <a name="updating-the-wsl-2-linux-kernel"></a><span data-ttu-id="0ea96-104">Actualización del kernel de Linux en WSL 2</span><span class="sxs-lookup"><span data-stu-id="0ea96-104">Updating the WSL 2 Linux kernel</span></span>

<span data-ttu-id="0ea96-105">Para actualizar manualmente el kernel de Linux dentro de WSL 2, sigue estos pasos.</span><span class="sxs-lookup"><span data-stu-id="0ea96-105">To manually update the Linux kernel inside of WSL 2 please follow these steps.</span></span>

> [!NOTE] 
> <span data-ttu-id="0ea96-106">Si el instalador no encuentra WSL 1, haz clic con el botón derecho en el instalador de actualizaciones del kernel de Linux, presiona "Desinstalar" y, luego, vuelve a ejecutar el instalador.</span><span class="sxs-lookup"><span data-stu-id="0ea96-106">If the installer can't find WSL 1, right-click the Linux kernel update installer and press "Uninstall", then rerun the installer.</span></span>

## <a name="download-the-linux-kernel-update-package"></a><span data-ttu-id="0ea96-107">Descarga del paquete de actualización del kernel de Linux</span><span class="sxs-lookup"><span data-stu-id="0ea96-107">Download the Linux kernel update package</span></span>

<span data-ttu-id="0ea96-108">Descarga el paquete de actualización [más reciente del kernel de Linux en WSL 2](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) para máquinas x64.</span><span class="sxs-lookup"><span data-stu-id="0ea96-108">Please [download the latest WSL2 Linux kernel](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) update package for x64 machines.</span></span>

> [!NOTE]
> <span data-ttu-id="0ea96-109">Si estás usando una máquina ARM64, descarga el [paquete ARM64](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="0ea96-109">If you're using an ARM64 machine, please download the [ARM64 package](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) instead.</span></span>

## <a name="install-the-linux-kernel-update-package"></a><span data-ttu-id="0ea96-110">Instalación del paquete de actualización del kernel de Linux</span><span class="sxs-lookup"><span data-stu-id="0ea96-110">Install the Linux kernel update package</span></span>

<span data-ttu-id="0ea96-111">Para instalar el paquete de actualización del kernel de Linux:</span><span class="sxs-lookup"><span data-stu-id="0ea96-111">To install the Linux kernel update package:</span></span>

  1. <span data-ttu-id="0ea96-112">Ejecuta el paquete de actualización que descargaste en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="0ea96-112">Run the update package downloaded in the previous step.</span></span>

  2. <span data-ttu-id="0ea96-113">Se te pedirán permisos elevados, selecciona "Sí" para aprobar esta instalación.</span><span class="sxs-lookup"><span data-stu-id="0ea96-113">You will be prompted for elevated permissions, select ‘yes’ to approve this installation.</span></span>

  3. <span data-ttu-id="0ea96-114">Una vez que se complete la instalación, estarás listo para empezar a usar WSL2.</span><span class="sxs-lookup"><span data-stu-id="0ea96-114">Once the installation is complete, you are ready to begin using WSL2!</span></span>

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a><span data-ttu-id="0ea96-115">Planes futuros para actualizar el kernel de Linux en WSL2</span><span class="sxs-lookup"><span data-stu-id="0ea96-115">Future plans for updating the WSL2 Linux kernel</span></span>

<span data-ttu-id="0ea96-116">Para obtener más información, consulta el artículo [cambios en la actualización del kernel de Linux en WSL2](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004), disponible en el [blog de la línea de comandos de Windows](https://aka.ms/cliblog).</span><span class="sxs-lookup"><span data-stu-id="0ea96-116">For more information, read the article [changes to updating the WSL2 Linux kernel](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004), available on the [Windows Command Line Blog](https://aka.ms/cliblog).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="0ea96-117">Solucionar problemas</span><span class="sxs-lookup"><span data-stu-id="0ea96-117">Troubleshooting</span></span>

### <a name="this-update-only-applies-to-machines-with-the-windows-subsystem-for-linux"></a><span data-ttu-id="0ea96-118">Esta actualización solo se aplica a las máquinas con el subsistema de Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="0ea96-118">This update only applies to machines with the Windows Subsystem for Linux</span></span>
<span data-ttu-id="0ea96-119">Para instalar el kernel de MSI, se requiere WSL y debe habilitarse primero.</span><span class="sxs-lookup"><span data-stu-id="0ea96-119">To install MSI kernel, WSL is required and should be enabled first.</span></span> <span data-ttu-id="0ea96-120">Si se produce un error, verá el mensaje: `This update only applies to machines with the Windows Subsystem for Linux`.</span><span class="sxs-lookup"><span data-stu-id="0ea96-120">If it fails, it you will see the message: `This update only applies to machines with the Windows Subsystem for Linux`.</span></span> 

<span data-ttu-id="0ea96-121">Hay tres posibles motivos para ver este mensaje:</span><span class="sxs-lookup"><span data-stu-id="0ea96-121">There are three possible reason you see this message:</span></span>

1. <span data-ttu-id="0ea96-122">Todavía tiene una versión antigua de Windows que no es compatible con WSL 2.</span><span class="sxs-lookup"><span data-stu-id="0ea96-122">You are still in old version of Windows which doesn't support WSL 2.</span></span> <span data-ttu-id="0ea96-123">Compruebe los [requisitos de WSL 2](https://docs.microsoft.com/windows/wsl/install-win10#update-to-wsl-2) y actualice para usar WSL 2.</span><span class="sxs-lookup"><span data-stu-id="0ea96-123">Please check the [WSL 2 requirements](https://docs.microsoft.com/windows/wsl/install-win10#update-to-wsl-2) and upgrade to use WSL 2.</span></span> 
2. <span data-ttu-id="0ea96-124">`Windows Subsystem for Linux` no está habilitado.</span><span class="sxs-lookup"><span data-stu-id="0ea96-124">`Windows Subsystem for Linux` is not enabled.</span></span> <span data-ttu-id="0ea96-125">Siga la [Guía de instalación del Subsistema de Windows para Linux](https://docs.microsoft.com/windows/wsl/install-win10).</span><span class="sxs-lookup"><span data-stu-id="0ea96-125">Please follow the [Windows Subsystem for Linux Installation Guide](https://docs.microsoft.com/windows/wsl/install-win10).</span></span>
3. <span data-ttu-id="0ea96-126">Una vez que haya habilitado `Windows Subsystem for Linux`, es necesario reiniciar el equipo e intentarlo de nuevo.</span><span class="sxs-lookup"><span data-stu-id="0ea96-126">After you enabled `Windows Subsystem for Linux`, a reboot is required to take into effect, please reboot your machine and try again.</span></span>

### `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`

<span data-ttu-id="0ea96-127">Cada vez que falta el kernel en %SystemRoot%\system32\lxss\tools\, puede que se encuentre con el error anterior.</span><span class="sxs-lookup"><span data-stu-id="0ea96-127">Each time kernel is missing in %SystemRoot%\system32\lxss\tools\, you may run into the above error.</span></span>

<span data-ttu-id="0ea96-128">Estas son algunas formas posibles de resolverlo:</span><span class="sxs-lookup"><span data-stu-id="0ea96-128">Here are some possible ways to resolve it:</span></span>

1. <span data-ttu-id="0ea96-129">Instale el kernel de Linux manualmente siguiendo las instrucciones de esta página.</span><span class="sxs-lookup"><span data-stu-id="0ea96-129">Install the Linux kernel manually following the instructions on this page.</span></span>
2. <span data-ttu-id="0ea96-130">Desinstale MSI desde "Agregar o quitar programas" e instálelo de nuevo.</span><span class="sxs-lookup"><span data-stu-id="0ea96-130">Uninstall the MSI from 'Add or Remove Programs', and install it again.</span></span>