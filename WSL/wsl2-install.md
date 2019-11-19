---
title: Instalación de WSL 2
description: Instrucciones de instalación de WSL 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, subsistema de windows para linux, subsistemawindows, ubuntu, debian, suse, windows 10, instalación
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 91994f3a075436c022acb9dadeea072142687b72
ms.sourcegitcommit: cf6d8e277ed3102f8f879b9f39ba0966d4ea6135
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2019
ms.locfileid: "74164337"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="db4f7-104">Instrucciones de instalación de WSL 2</span><span class="sxs-lookup"><span data-stu-id="db4f7-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="db4f7-105">Para instalar y empezar a usar WSL 2, sigue estos pasos:</span><span class="sxs-lookup"><span data-stu-id="db4f7-105">To install and start using WSL 2 complete the following steps:</span></span>

> <span data-ttu-id="db4f7-106">WSL 2 solo está disponible en las compilaciones 18917 o posteriores de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="db4f7-106">WSL 2 is only available in Windows 10 builds 18917 or higher</span></span>

- <span data-ttu-id="db4f7-107">Asegúrese de que ha instalado WSL (puede encontrar instrucciones para hacerlo [aquí](./install-win10.md)) y de que está ejecutando Windows 10 **Build 18917** o superior.</span><span class="sxs-lookup"><span data-stu-id="db4f7-107">Ensure that you have WSL installed (you can find instructions to do so [here](./install-win10.md)) and that you are running Windows 10 **build 18917** or higher</span></span>
   - <span data-ttu-id="db4f7-108">Para asegurarse de que está usando la compilación 18917 o posterior, únase [al programa Windows Insider](https://insider.windows.com/en-us/) y seleccione el anillo "rápido".</span><span class="sxs-lookup"><span data-stu-id="db4f7-108">To make sure you are using build 18917 or higher please join [the Windows Insider Program](https://insider.windows.com/en-us/) and select the 'Fast' ring.</span></span> 
   - <span data-ttu-id="db4f7-109">Para comprobar la versión de Windows, abra el símbolo del sistema y ejecute el comando `ver`.</span><span class="sxs-lookup"><span data-stu-id="db4f7-109">You can check your Windows version by opening Command Prompt and running the `ver` command.</span></span>
- <span data-ttu-id="db4f7-110">Habilitación del componente opcional "Plataforma de máquina virtual"</span><span class="sxs-lookup"><span data-stu-id="db4f7-110">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="db4f7-111">Establecimiento de una distribución que respaldará WSL 2 mediante la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="db4f7-111">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="db4f7-112">Comprobación de qué versiones de WSL están usando las distribuciones</span><span class="sxs-lookup"><span data-stu-id="db4f7-112">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a><span data-ttu-id="db4f7-113">Habilite el componente opcional "plataforma de máquina virtual" y asegúrese de que WSL está habilitado.</span><span class="sxs-lookup"><span data-stu-id="db4f7-113">Enable the 'Virtual Machine Platform' optional component and make sure WSL is enabled</span></span>

<span data-ttu-id="db4f7-114">Para habilitar el componente "plataforma de máquina virtual", abra PowerShell como administrador y ejecute el comando siguiente.</span><span class="sxs-lookup"><span data-stu-id="db4f7-114">To enable the 'Virtual Machine Platform' component open PowerShell as an administrator and run the command below.</span></span> <span data-ttu-id="db4f7-115">Si va a instalar WSL por primera vez, seleccione "no" cuando se le solicite un reinicio, ya que tendrá que reiniciar el equipo después de instalar el componente opcional "subsistema de Windows para Linux".</span><span class="sxs-lookup"><span data-stu-id="db4f7-115">If you are installing WSL for the first time then select 'No' when prompted for a restart, as you will need to restart your machine anyway after installing the 'Windows Subsystem for Linux' optional component.</span></span>

```powershell
Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform
```

<span data-ttu-id="db4f7-116">También debe asegurarse de que está habilitado el componente opcional de subsistema de Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="db4f7-116">You will also need to make sure that the Windows Subsystem for Linux optional component is enabled.</span></span> <span data-ttu-id="db4f7-117">Para ello, ejecute el siguiente comando desde una ventana de PowerShell con privilegios de administrador:</span><span class="sxs-lookup"><span data-stu-id="db4f7-117">You can do this by running the following command from a PowerShell window with administrator privileges:</span></span> 

```powershell
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

<span data-ttu-id="db4f7-118">Reinicie el equipo para finalizar la instalación de ambos componentes.</span><span class="sxs-lookup"><span data-stu-id="db4f7-118">Please restart your machine to finish installing both components.</span></span>


## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="db4f7-119">Establecimiento de una distribución que respaldará WSL 2 mediante la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="db4f7-119">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="db4f7-120">Si no tiene instalado un distribución de Linux, consulte la página de documentos [instalar en Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) para obtener instrucciones sobre cómo instalar uno.</span><span class="sxs-lookup"><span data-stu-id="db4f7-120">If you do not have a Linux distro installed, please refer to the [Install on Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) docs page for instructions on installing one.</span></span> 

<span data-ttu-id="db4f7-121">En PowerShell, ejecuta:</span><span class="sxs-lookup"><span data-stu-id="db4f7-121">In PowerShell run:</span></span>

`wsl --set-version <Distro> 2`

<span data-ttu-id="db4f7-122">Asegúrate de reemplazar `<Distro>` por el nombre real de tu distribución.</span><span class="sxs-lookup"><span data-stu-id="db4f7-122">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="db4f7-123">(Puedes encontrarlo con el comando: `wsl -l`).</span><span class="sxs-lookup"><span data-stu-id="db4f7-123">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="db4f7-124">Puedes volver a cambiar a WSL 1 en cualquier momento; para ello, ejecuta el mismo comando que antes, pero reemplaza "2" por "1".</span><span class="sxs-lookup"><span data-stu-id="db4f7-124">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="db4f7-125">Además, si quieres que WSL 2 sea la arquitectura predeterminada, puedes hacerlo con este comando:</span><span class="sxs-lookup"><span data-stu-id="db4f7-125">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

`wsl --set-default-version 2`

<span data-ttu-id="db4f7-126">Esto hará que las nuevas distribuciones que instales se inicialicen como distribución de WSL 2.</span><span class="sxs-lookup"><span data-stu-id="db4f7-126">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="db4f7-127">Comprobación final de qué versiones de WSL están usando las distribuciones</span><span class="sxs-lookup"><span data-stu-id="db4f7-127">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="db4f7-128">Para comprobar qué versiones de WSL usa cada distribución, use el siguiente comando (solo disponible en Windows compilación 18917 o posterior):</span><span class="sxs-lookup"><span data-stu-id="db4f7-128">To verify what versions of WSL each distro is using use the following command (only available in Windows Build 18917 or higher):</span></span>

<span data-ttu-id="db4f7-129">`wsl --list --verbose` o `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="db4f7-129">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="db4f7-130">La distribución que has elegido anteriormente debería mostrar ahora un "2" en la columna "version" (versión).</span><span class="sxs-lookup"><span data-stu-id="db4f7-130">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="db4f7-131">Ahora que ya has completado los pasos, puedes empezar a usar tu distribución de WSL 2.</span><span class="sxs-lookup"><span data-stu-id="db4f7-131">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 

## <a name="troubleshooting"></a><span data-ttu-id="db4f7-132">Solución de problemas:</span><span class="sxs-lookup"><span data-stu-id="db4f7-132">Troubleshooting:</span></span> 

<span data-ttu-id="db4f7-133">A continuación se muestran errores relacionados con la instalación de WSL 2 y las correcciones sugeridas.</span><span class="sxs-lookup"><span data-stu-id="db4f7-133">Below are related errors and suggested fixes when installing WSL 2.</span></span> <span data-ttu-id="db4f7-134">Consulta la [página de solución de problemas de WSL](troubleshooting.md) para ver otros errores generales de WSL y sus soluciones.</span><span class="sxs-lookup"><span data-stu-id="db4f7-134">Please refer to the [WSL troubleshooting page](troubleshooting.md) for other general WSL errors and their solutions.</span></span>

* <span data-ttu-id="db4f7-135">**Error en la instalación 0x80070003 o 0x80370102**</span><span class="sxs-lookup"><span data-stu-id="db4f7-135">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
    * <span data-ttu-id="db4f7-136">Asegúrate de que la virtualización está habilitada dentro del BIOS del equipo.</span><span class="sxs-lookup"><span data-stu-id="db4f7-136">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="db4f7-137">Las instrucciones sobre cómo hacerlo variarán de un equipo a otro y lo más probable es que esta característica esté en opciones relacionadas con la CPU.</span><span class="sxs-lookup"><span data-stu-id="db4f7-137">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>
   
* <span data-ttu-id="db4f7-138">**Error al intentar actualizar: `Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="db4f7-138">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
    * <span data-ttu-id="db4f7-139">Asegúrate de que tienes el Subsistema de Windows para Linux habilitado y de que estás usando la compilación 18917 de Windows o posterior.</span><span class="sxs-lookup"><span data-stu-id="db4f7-139">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18917 or higher.</span></span> <span data-ttu-id="db4f7-140">Para habilitar WSL, ejecuta este comando en un símbolo del sistema de PowerShell con privilegios de administrador: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span><span class="sxs-lookup"><span data-stu-id="db4f7-140">To enable WSL run this command in a Powershell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="db4f7-141">Puedes encontrar las instrucciones de instalación de WSL completas [aquí](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="db4f7-141">You can find the full WSL install instructions [here](./install-win10.md).</span></span>

* <span data-ttu-id="db4f7-142">**No se pudo completar la operación solicitada debido a una limitación del sistema de disco virtual. Los archivos de disco duro virtual deben estar sin comprimir y sin cifrar y no deben ser dispersos.**</span><span class="sxs-lookup"><span data-stu-id="db4f7-142">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span></span>
    * <span data-ttu-id="db4f7-143">Consulte [WSL GitHub thread #4103](https://github.com/microsoft/WSL/issues/4103) en el que se realiza el seguimiento de este problema para obtener información actualizada.</span><span class="sxs-lookup"><span data-stu-id="db4f7-143">Please check [WSL Github thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span></span>