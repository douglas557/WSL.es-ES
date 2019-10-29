---
title: Instalación de WSL 2
description: Instrucciones de instalación de WSL 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, subsistema de windows para linux, subsistemawindows, ubuntu, debian, suse, windows 10, instalación
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: d4ce22fda7baea77c0a8d3d7101d0ab09b78e8f8
ms.sourcegitcommit: d110e2bbcd92438781453137ba0ab747cddb28e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2019
ms.locfileid: "72998249"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="7e6c6-104">Instrucciones de instalación de WSL 2</span><span class="sxs-lookup"><span data-stu-id="7e6c6-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="7e6c6-105">Para instalar y empezar a usar WSL 2, sigue estos pasos:</span><span class="sxs-lookup"><span data-stu-id="7e6c6-105">To install and start using WSL 2 complete the following steps:</span></span>

> <span data-ttu-id="7e6c6-106">WSL 2 solo está disponible en las compilaciones 18917 o posteriores de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7e6c6-106">WSL 2 is only available in Windows 10 builds 18917 or higher</span></span>

- <span data-ttu-id="7e6c6-107">Asegúrese de que ha instalado WSL (puede encontrar instrucciones para hacerlo [aquí](./install-win10.md)) y de que está ejecutando Windows 10 **Build 18917** o superior.</span><span class="sxs-lookup"><span data-stu-id="7e6c6-107">Ensure that you have WSL installed (you can find instructions to do so [here](./install-win10.md)) and that you are running Windows 10 **build 18917** or higher</span></span>
   - <span data-ttu-id="7e6c6-108">Para asegurarse de que está usando la compilación 18917 o posterior, únase [al programa Windows Insider](https://insider.windows.com/en-us/) y seleccione el anillo "rápido".</span><span class="sxs-lookup"><span data-stu-id="7e6c6-108">To make sure you are using build 18917 or higher please join [the Windows Insider Program](https://insider.windows.com/en-us/) and select the 'Fast' ring.</span></span> 
   - <span data-ttu-id="7e6c6-109">Para comprobar la versión de Windows, abra el símbolo del sistema y ejecute el comando `ver`.</span><span class="sxs-lookup"><span data-stu-id="7e6c6-109">You can check your Windows version by opening Command Prompt and running the `ver` command.</span></span>
- <span data-ttu-id="7e6c6-110">Habilitación del componente opcional "Plataforma de máquina virtual"</span><span class="sxs-lookup"><span data-stu-id="7e6c6-110">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="7e6c6-111">Establecimiento de una distribución que respaldará WSL 2 mediante la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="7e6c6-111">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="7e6c6-112">Comprobación de qué versiones de WSL están usando las distribuciones</span><span class="sxs-lookup"><span data-stu-id="7e6c6-112">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a><span data-ttu-id="7e6c6-113">Habilite el componente opcional "plataforma de máquina virtual" y asegúrese de que WSL está habilitado.</span><span class="sxs-lookup"><span data-stu-id="7e6c6-113">Enable the 'Virtual Machine Platform' optional component and make sure WSL is enabled</span></span>

<span data-ttu-id="7e6c6-114">Abre PowerShell como administrador y ejecuta:</span><span class="sxs-lookup"><span data-stu-id="7e6c6-114">Open PowerShell as an Administrator and run:</span></span>

```powershell
Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

<span data-ttu-id="7e6c6-115">Así se asegurará de que se instalan los componentes opcionales de la plataforma de máquina virtual y el subsistema de Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="7e6c6-115">This will make sure that both the Virtual Machine Platform and Windows Subsystem for Linux optional components are installed.</span></span> <span data-ttu-id="7e6c6-116">Después de ejecutar estos comandos, deberá reiniciar el equipo.</span><span class="sxs-lookup"><span data-stu-id="7e6c6-116">After you've run these commands you'll need to restart your computer.</span></span> 

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="7e6c6-117">Establecimiento de una distribución que respaldará WSL 2 mediante la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="7e6c6-117">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="7e6c6-118">En PowerShell, ejecuta:</span><span class="sxs-lookup"><span data-stu-id="7e6c6-118">In PowerShell run:</span></span>

`wsl --set-version <Distro> 2`

<span data-ttu-id="7e6c6-119">Asegúrate de reemplazar `<Distro>` por el nombre real de tu distribución.</span><span class="sxs-lookup"><span data-stu-id="7e6c6-119">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="7e6c6-120">(Puedes encontrarlo con el comando: `wsl -l`).</span><span class="sxs-lookup"><span data-stu-id="7e6c6-120">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="7e6c6-121">Puedes volver a cambiar a WSL 1 en cualquier momento; para ello, ejecuta el mismo comando que antes, pero reemplaza "2" por "1".</span><span class="sxs-lookup"><span data-stu-id="7e6c6-121">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="7e6c6-122">Además, si quieres que WSL 2 sea la arquitectura predeterminada, puedes hacerlo con este comando:</span><span class="sxs-lookup"><span data-stu-id="7e6c6-122">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

`wsl --set-default-version 2`

<span data-ttu-id="7e6c6-123">Esto hará que las nuevas distribuciones que instales se inicialicen como distribución de WSL 2.</span><span class="sxs-lookup"><span data-stu-id="7e6c6-123">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="7e6c6-124">Comprobación final de qué versiones de WSL están usando las distribuciones</span><span class="sxs-lookup"><span data-stu-id="7e6c6-124">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="7e6c6-125">Para comprobar qué versiones de WSL usa cada distribución, use el siguiente comando (solo disponible en Windows compilación 18917 o posterior):</span><span class="sxs-lookup"><span data-stu-id="7e6c6-125">To verify what versions of WSL each distro is using use the following command (only available in Windows Build 18917 or higher):</span></span>

<span data-ttu-id="7e6c6-126">`wsl --list --verbose` o `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="7e6c6-126">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="7e6c6-127">La distribución que has elegido anteriormente debería mostrar ahora un "2" en la columna "version" (versión).</span><span class="sxs-lookup"><span data-stu-id="7e6c6-127">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="7e6c6-128">Ahora que ya has completado los pasos, puedes empezar a usar tu distribución de WSL 2.</span><span class="sxs-lookup"><span data-stu-id="7e6c6-128">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 

## <a name="troubleshooting"></a><span data-ttu-id="7e6c6-129">Solución de problemas:</span><span class="sxs-lookup"><span data-stu-id="7e6c6-129">Troubleshooting:</span></span> 

<span data-ttu-id="7e6c6-130">A continuación se muestran errores relacionados con la instalación de WSL 2 y las correcciones sugeridas.</span><span class="sxs-lookup"><span data-stu-id="7e6c6-130">Below are related errors and suggested fixes when installing WSL 2.</span></span> <span data-ttu-id="7e6c6-131">Consulta la [página de solución de problemas de WSL](troubleshooting.md) para ver otros errores generales de WSL y sus soluciones.</span><span class="sxs-lookup"><span data-stu-id="7e6c6-131">Please refer to the [WSL troubleshooting page](troubleshooting.md) for other general WSL errors and their solutions.</span></span>

* <span data-ttu-id="7e6c6-132">**Error en la instalación 0x80070003 o 0x80370102**</span><span class="sxs-lookup"><span data-stu-id="7e6c6-132">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
    * <span data-ttu-id="7e6c6-133">Asegúrate de que la virtualización está habilitada dentro del BIOS del equipo.</span><span class="sxs-lookup"><span data-stu-id="7e6c6-133">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="7e6c6-134">Las instrucciones sobre cómo hacerlo variarán de un equipo a otro y lo más probable es que esta característica esté en opciones relacionadas con la CPU.</span><span class="sxs-lookup"><span data-stu-id="7e6c6-134">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>
   
* <span data-ttu-id="7e6c6-135">**Error al intentar actualizar: `Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="7e6c6-135">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
    * <span data-ttu-id="7e6c6-136">Asegúrate de que tienes el Subsistema de Windows para Linux habilitado y de que estás usando la compilación 18917 de Windows o posterior.</span><span class="sxs-lookup"><span data-stu-id="7e6c6-136">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18917 or higher.</span></span> <span data-ttu-id="7e6c6-137">Para habilitar WSL, ejecuta este comando en un símbolo del sistema de PowerShell con privilegios de administrador: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span><span class="sxs-lookup"><span data-stu-id="7e6c6-137">To enable WSL run this command in a Powershell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="7e6c6-138">Puedes encontrar las instrucciones de instalación de WSL completas [aquí](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="7e6c6-138">You can find the full WSL install instructions [here](./install-win10.md).</span></span>

* <span data-ttu-id="7e6c6-139">**No se pudo completar la operación solicitada debido a una limitación del sistema de disco virtual. Los archivos de disco duro virtual deben estar sin comprimir y sin cifrar y no deben ser dispersos.**</span><span class="sxs-lookup"><span data-stu-id="7e6c6-139">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span></span>
    * <span data-ttu-id="7e6c6-140">Consulte [WSL GitHub thread #4103](https://github.com/microsoft/WSL/issues/4103) en el que se realiza el seguimiento de este problema para obtener información actualizada.</span><span class="sxs-lookup"><span data-stu-id="7e6c6-140">Please check [WSL Github thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span></span>