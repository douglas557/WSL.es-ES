---
title: Instalación de WSL 2
description: Instrucciones de instalación de WSL 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, subsistema de windows para linux, subsistemawindows, ubuntu, debian, suse, windows 10, instalación
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 7c031b1348a77e1dac967fae5e4df772e10a9084
ms.sourcegitcommit: 0a001ada2131f80dd77b114fc14f2fde43c947ad
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/25/2020
ms.locfileid: "80256348"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="bbbd5-104">Instrucciones de instalación de WSL 2</span><span class="sxs-lookup"><span data-stu-id="bbbd5-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="bbbd5-105">Puedes ver el vídeo siguiente o leer este artículo para obtener información sobre cómo instalar WSL 2.</span><span class="sxs-lookup"><span data-stu-id="bbbd5-105">You can watch the video below, or read on in this article to learn how to install WSL2.</span></span> 

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Learn-how-to-install-WSL-2/player]

<span data-ttu-id="bbbd5-106">Para instalar y empezar a usar WSL 2, sigue estos pasos:</span><span class="sxs-lookup"><span data-stu-id="bbbd5-106">To install and start using WSL 2 complete the following steps:</span></span>

> <span data-ttu-id="bbbd5-107">WSL 2 solo está disponible en las compilaciones 18917 o posteriores de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="bbbd5-107">WSL 2 is only available in Windows 10 builds 18917 or higher</span></span>

- <span data-ttu-id="bbbd5-108">Asegúrate de tener WSL instalado (puedes encontrar instrucciones para hacerlo [aquí](./install-win10.md)) y de que estás ejecutando Windows 10, **compilación 18917** o posterior.</span><span class="sxs-lookup"><span data-stu-id="bbbd5-108">Ensure that you have WSL installed (you can find instructions to do so [here](./install-win10.md)) and that you are running Windows 10 **build 18917** or higher</span></span>
   - <span data-ttu-id="bbbd5-109">Para asegurarte de que estás usando la compilación 18917 o posterior, únete [al programa de Windows Insider](https://insider.windows.com/en-us/) y selecciona el anillo "rápido" o el anillo "lento".</span><span class="sxs-lookup"><span data-stu-id="bbbd5-109">To make sure you are using build 18917 or higher please join [the Windows Insider Program](https://insider.windows.com/en-us/) and select the 'Fast' ring or the 'Slow' ring.</span></span> 
   - <span data-ttu-id="bbbd5-110">Para comprobar la versión de Windows, abre el símbolo del sistema y ejecuta el comando `ver`.</span><span class="sxs-lookup"><span data-stu-id="bbbd5-110">You can check your Windows version by opening Command Prompt and running the `ver` command.</span></span>
- <span data-ttu-id="bbbd5-111">Habilitación del componente opcional "Plataforma de máquina virtual"</span><span class="sxs-lookup"><span data-stu-id="bbbd5-111">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="bbbd5-112">Establecimiento de una distribución que respaldará WSL 2 mediante la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="bbbd5-112">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="bbbd5-113">Comprobación de qué versiones de WSL están usando las distribuciones</span><span class="sxs-lookup"><span data-stu-id="bbbd5-113">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a><span data-ttu-id="bbbd5-114">Habilitación del componente opcional "Plataforma de máquina virtual" y comprobación de la habilitación de WSL</span><span class="sxs-lookup"><span data-stu-id="bbbd5-114">Enable the 'Virtual Machine Platform' optional component and make sure WSL is enabled</span></span>

<span data-ttu-id="bbbd5-115">Tendrás que asegurarse de tener instalados los componentes opcionales Subsistema de Windows para Linux y Plataforma de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bbbd5-115">You will need to make sure that you have both the Windows Subsystem for Linux and the Virtual Machine Platform optional components installed.</span></span> <span data-ttu-id="bbbd5-116">Para hacerlo ejecuta el siguiente comando en PowerShell:</span><span class="sxs-lookup"><span data-stu-id="bbbd5-116">You can do that by running the following command in PowerShell:</span></span> 

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

<span data-ttu-id="bbbd5-117">Reinicia el equipo para finalizar la instalación de ambos componentes.</span><span class="sxs-lookup"><span data-stu-id="bbbd5-117">Please restart your machine to finish installing both components.</span></span>


## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="bbbd5-118">Establecimiento de una distribución que respaldará WSL 2 mediante la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="bbbd5-118">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="bbbd5-119">Si no tienes una distribución de Linux instalada, consulta la página de documentación [Instalación en Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) para obtener instrucciones sobre cómo instalar una.</span><span class="sxs-lookup"><span data-stu-id="bbbd5-119">If you do not have a Linux distro installed, please refer to the [Install on Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) docs page for instructions on installing one.</span></span> 

<span data-ttu-id="bbbd5-120">Para establecer un distribución, ejecuta:</span><span class="sxs-lookup"><span data-stu-id="bbbd5-120">To set a distro please run:</span></span> 

```
wsl --set-version <Distro> 2
```

<span data-ttu-id="bbbd5-121">Asegúrate de reemplazar `<Distro>` por el nombre real de tu distribución.</span><span class="sxs-lookup"><span data-stu-id="bbbd5-121">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="bbbd5-122">(Puedes encontrarlo con el comando: `wsl -l`).</span><span class="sxs-lookup"><span data-stu-id="bbbd5-122">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="bbbd5-123">Puedes volver a cambiar a WSL 1 en cualquier momento; para ello, ejecuta el mismo comando que antes, pero reemplaza "2" por "1".</span><span class="sxs-lookup"><span data-stu-id="bbbd5-123">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="bbbd5-124">Además, si quieres que WSL 2 sea la arquitectura predeterminada, puedes hacerlo con este comando:</span><span class="sxs-lookup"><span data-stu-id="bbbd5-124">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

```
wsl --set-default-version 2
```

<span data-ttu-id="bbbd5-125">Esto hará que las nuevas distribuciones que instales se inicialicen como distribución de WSL 2.</span><span class="sxs-lookup"><span data-stu-id="bbbd5-125">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="bbbd5-126">Comprobación final de qué versiones de WSL están usando las distribuciones</span><span class="sxs-lookup"><span data-stu-id="bbbd5-126">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="bbbd5-127">Para comprobar qué versiones de WSL está usando cada distribución, usa el siguiente comando (disponible solamente en la compilación 18917 o posterior de Windows):</span><span class="sxs-lookup"><span data-stu-id="bbbd5-127">To verify what versions of WSL each distro is using use the following command (only available in Windows Build 18917 or higher):</span></span>

<span data-ttu-id="bbbd5-128">`wsl --list --verbose` o `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="bbbd5-128">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="bbbd5-129">La distribución que has elegido anteriormente debería mostrar ahora un "2" en la columna "version" (versión).</span><span class="sxs-lookup"><span data-stu-id="bbbd5-129">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="bbbd5-130">Ahora que ya has completado los pasos, puedes empezar a usar tu distribución de WSL 2.</span><span class="sxs-lookup"><span data-stu-id="bbbd5-130">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 

## <a name="troubleshooting"></a><span data-ttu-id="bbbd5-131">Solución de problemas:</span><span class="sxs-lookup"><span data-stu-id="bbbd5-131">Troubleshooting:</span></span> 

<span data-ttu-id="bbbd5-132">A continuación se muestran errores relacionados con la instalación de WSL 2 y las correcciones sugeridas.</span><span class="sxs-lookup"><span data-stu-id="bbbd5-132">Below are related errors and suggested fixes when installing WSL 2.</span></span> <span data-ttu-id="bbbd5-133">Consulta la [página de solución de problemas de WSL](troubleshooting.md) para ver otros errores generales de WSL y sus soluciones.</span><span class="sxs-lookup"><span data-stu-id="bbbd5-133">Please refer to the [WSL troubleshooting page](troubleshooting.md) for other general WSL errors and their solutions.</span></span>

* <span data-ttu-id="bbbd5-134">**Error en la instalación 0x80070003 o 0x80370102**</span><span class="sxs-lookup"><span data-stu-id="bbbd5-134">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
    * <span data-ttu-id="bbbd5-135">Asegúrate de que la virtualización está habilitada dentro del BIOS del equipo.</span><span class="sxs-lookup"><span data-stu-id="bbbd5-135">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="bbbd5-136">Las instrucciones sobre cómo hacerlo variarán de un equipo a otro y lo más probable es que esta característica esté en opciones relacionadas con la CPU.</span><span class="sxs-lookup"><span data-stu-id="bbbd5-136">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>
   
* <span data-ttu-id="bbbd5-137">**Error al intentar actualizar: `Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="bbbd5-137">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
    * <span data-ttu-id="bbbd5-138">Asegúrate de que tienes el Subsistema de Windows para Linux habilitado y de que estás usando la compilación 18917 de Windows o posterior.</span><span class="sxs-lookup"><span data-stu-id="bbbd5-138">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18917 or higher.</span></span> <span data-ttu-id="bbbd5-139">Para habilitar WSL, ejecuta este comando en un símbolo del sistema de PowerShell con privilegios de administrador: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span><span class="sxs-lookup"><span data-stu-id="bbbd5-139">To enable WSL run this command in a Powershell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="bbbd5-140">Puedes encontrar las instrucciones de instalación de WSL completas [aquí](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="bbbd5-140">You can find the full WSL install instructions [here](./install-win10.md).</span></span>

* <span data-ttu-id="bbbd5-141">**La operación solicitada no se pudo completar debido a una limitación del sistema de disco virtual. Los archivos de disco duro virtual deben estar sin comprimir y sin cifrar y no deben ser dispersos.**</span><span class="sxs-lookup"><span data-stu-id="bbbd5-141">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span></span>
    * <span data-ttu-id="bbbd5-142">Consulta el [subproceso #4103 sobre WSL en Github](https://github.com/microsoft/WSL/issues/4103), en el que se realiza el seguimiento de este problema para obtener información actualizada.</span><span class="sxs-lookup"><span data-stu-id="bbbd5-142">Please check [WSL Github thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span></span>

* <span data-ttu-id="bbbd5-143">**El término 'wsl' no se reconoce como nombre de cmdlet, función, archivo de script o programa ejecutable.**</span><span class="sxs-lookup"><span data-stu-id="bbbd5-143">**The term 'wsl' is not recognized as the name of a cmdlet, function, script file, or operable program.**</span></span> 
    * <span data-ttu-id="bbbd5-144">Asegúrate de que el [componente opcional del Subsistema de Windows para Linux esté instalado](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="bbbd5-144">Ensure that the [Windows Subsystem for Linux Optional Component is installed](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled).</span></span><br> <span data-ttu-id="bbbd5-145">Además, si usas un dispositivo Arm64 y ejecutas este comando desde PowerShell, recibirás este error.</span><span class="sxs-lookup"><span data-stu-id="bbbd5-145">Additionally, if you are using an Arm64 device and running this command from PowerShell, you will receive this error.</span></span> <span data-ttu-id="bbbd5-146">En su lugar, ejecuta `wsl.exe` desde [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6) o el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="bbbd5-146">Instead run `wsl.exe` from [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6), or Command Prompt.</span></span> 
