---
title: Instalación de WSL 2
description: Instrucciones de instalación de WSL 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, subsistema de windows para linux, subsistemawindows, ubuntu, debian, suse, windows 10, instalación
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 3ad180ecc9deaa1566e9870700b26f82f631c7f1
ms.sourcegitcommit: 9ad7a54668f39677e9660186e4f5172ea2597e2b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/16/2019
ms.locfileid: "68246863"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="191cc-104">Instrucciones de instalación de WSL 2</span><span class="sxs-lookup"><span data-stu-id="191cc-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="191cc-105">Para instalar y empezar a usar WSL 2, sigue estos pasos:</span><span class="sxs-lookup"><span data-stu-id="191cc-105">To install and start using WSL 2 complete the following steps:</span></span>

- <span data-ttu-id="191cc-106">Habilitación del componente opcional "Plataforma de máquina virtual"</span><span class="sxs-lookup"><span data-stu-id="191cc-106">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="191cc-107">Establecimiento de una distribución que respaldará WSL 2 mediante la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="191cc-107">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="191cc-108">Comprobación de qué versiones de WSL están usando las distribuciones</span><span class="sxs-lookup"><span data-stu-id="191cc-108">Verify what versions of WSL your distros are using</span></span>

<span data-ttu-id="191cc-109">Ten en cuenta que deberás usar la compilación 18917 de Windows 10 o posterior para utilizar WSL 2 y que deberás tener WSL ya instalado (puedes encontrar instrucciones para ello [aquí](./install-win10.md)).</span><span class="sxs-lookup"><span data-stu-id="191cc-109">Please note that you'll need to be running Windows 10 build 18917 or higher to use WSL 2, and that you will need to have WSL already installed (you can find instructions to do so [here](./install-win10.md)).</span></span> 

## <a name="enable-the-virtual-machine-platform-optional-component"></a><span data-ttu-id="191cc-110">Habilitación del componente opcional "Plataforma de máquina virtual"</span><span class="sxs-lookup"><span data-stu-id="191cc-110">Enable the 'Virtual Machine Platform' optional component</span></span>

<span data-ttu-id="191cc-111">Abre PowerShell como administrador y ejecuta:</span><span class="sxs-lookup"><span data-stu-id="191cc-111">Open PowerShell as an Administrator and run:</span></span>

`Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform`

<span data-ttu-id="191cc-112">Una vez habilitados estos cambios, deberás reiniciar el equipo.</span><span class="sxs-lookup"><span data-stu-id="191cc-112">After these changes are enabled you will need to restart your computer.</span></span>

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="191cc-113">Establecimiento de una distribución que respaldará WSL 2 mediante la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="191cc-113">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="191cc-114">En PowerShell, ejecuta:</span><span class="sxs-lookup"><span data-stu-id="191cc-114">In PowerShell run:</span></span>

`wsl --set-version <Distro> 2`

<span data-ttu-id="191cc-115">Asegúrate de reemplazar `<Distro>` por el nombre real de tu distribución.</span><span class="sxs-lookup"><span data-stu-id="191cc-115">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="191cc-116">(Puedes encontrarlo con el comando: `wsl -l`).</span><span class="sxs-lookup"><span data-stu-id="191cc-116">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="191cc-117">Puedes volver a cambiar a WSL 1 en cualquier momento; para ello, ejecuta el mismo comando que antes, pero reemplaza "2" por "1".</span><span class="sxs-lookup"><span data-stu-id="191cc-117">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="191cc-118">Además, si quieres que WSL 2 sea la arquitectura predeterminada, puedes hacerlo con este comando:</span><span class="sxs-lookup"><span data-stu-id="191cc-118">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

`wsl --set-default-version 2`

<span data-ttu-id="191cc-119">Esto hará que las nuevas distribuciones que instales se inicialicen como distribución de WSL 2.</span><span class="sxs-lookup"><span data-stu-id="191cc-119">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="191cc-120">Comprobación final de qué versiones de WSL están usando las distribuciones</span><span class="sxs-lookup"><span data-stu-id="191cc-120">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="191cc-121">Para comprobar qué versiones de WSL está usando cada distribución, usa el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="191cc-121">To verify what versions of WSL each distro is using use the following command:</span></span>

<span data-ttu-id="191cc-122">`wsl --list --verbose` o `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="191cc-122">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="191cc-123">La distribución que has elegido anteriormente debería mostrar ahora un "2" en la columna "version" (versión).</span><span class="sxs-lookup"><span data-stu-id="191cc-123">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="191cc-124">Ahora que ya has completado los pasos, puedes empezar a usar tu distribución de WSL 2.</span><span class="sxs-lookup"><span data-stu-id="191cc-124">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 

## <a name="troubleshooting"></a><span data-ttu-id="191cc-125">Solución de problemas:</span><span class="sxs-lookup"><span data-stu-id="191cc-125">Troubleshooting:</span></span> 

<span data-ttu-id="191cc-126">A continuación se muestran errores relacionados con la instalación de WSL 2 y las correcciones sugeridas.</span><span class="sxs-lookup"><span data-stu-id="191cc-126">Below are related errors and suggested fixes when installing WSL 2.</span></span> <span data-ttu-id="191cc-127">Consulta la [página de solución de problemas de WSL](troubleshooting.md) para ver otros errores generales de WSL y sus soluciones.</span><span class="sxs-lookup"><span data-stu-id="191cc-127">Please refer to the [WSL troubleshooting page](troubleshooting.md) for other general WSL errors and their solutions.</span></span>

* <span data-ttu-id="191cc-128">**Error en la instalación 0x80070003 o 0x80370102**</span><span class="sxs-lookup"><span data-stu-id="191cc-128">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
    * <span data-ttu-id="191cc-129">Asegúrate de que la virtualización está habilitada dentro del BIOS del equipo.</span><span class="sxs-lookup"><span data-stu-id="191cc-129">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="191cc-130">Las instrucciones sobre cómo hacerlo variarán de un equipo a otro y lo más probable es que esta característica esté en opciones relacionadas con la CPU.</span><span class="sxs-lookup"><span data-stu-id="191cc-130">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>
   
* <span data-ttu-id="191cc-131">**Error al intentar actualizar: `Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="191cc-131">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
    * <span data-ttu-id="191cc-132">Asegúrate de que tienes el Subsistema de Windows para Linux habilitado y de que estás usando la compilación 18917 de Windows o posterior.</span><span class="sxs-lookup"><span data-stu-id="191cc-132">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18917 or higher.</span></span> <span data-ttu-id="191cc-133">Para habilitar WSL, ejecuta este comando en un símbolo del sistema de PowerShell con privilegios de administrador: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span><span class="sxs-lookup"><span data-stu-id="191cc-133">To enable WSL run this command in a Powershell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="191cc-134">Puedes encontrar las instrucciones de instalación de WSL completas [aquí](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="191cc-134">You can find the full WSL install instructions [here](./install-win10.md).</span></span>