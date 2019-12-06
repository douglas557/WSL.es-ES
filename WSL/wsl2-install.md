---
title: Instalación de WSL 2
description: Instrucciones de instalación de WSL 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, subsistema de windows para linux, subsistemawindows, ubuntu, debian, suse, windows 10, instalación
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 65c0440a95637708881c00558cba6c7985f89ec0
ms.sourcegitcommit: 522af20edfba4d4a9e429327389967a83e6d1156
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/06/2019
ms.locfileid: "74881374"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="85782-104">Instrucciones de instalación de WSL 2</span><span class="sxs-lookup"><span data-stu-id="85782-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="85782-105">Para instalar y empezar a usar WSL 2, sigue estos pasos:</span><span class="sxs-lookup"><span data-stu-id="85782-105">To install and start using WSL 2 complete the following steps:</span></span>

> <span data-ttu-id="85782-106">WSL 2 solo está disponible en las compilaciones 18917 o posteriores de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="85782-106">WSL 2 is only available in Windows 10 builds 18917 or higher</span></span>

- <span data-ttu-id="85782-107">Asegúrese de que ha instalado WSL (puede encontrar instrucciones para hacerlo [aquí](./install-win10.md)) y de que está ejecutando Windows 10 **Build 18917** o superior.</span><span class="sxs-lookup"><span data-stu-id="85782-107">Ensure that you have WSL installed (you can find instructions to do so [here](./install-win10.md)) and that you are running Windows 10 **build 18917** or higher</span></span>
   - <span data-ttu-id="85782-108">Para asegurarse de que está usando la compilación 18917 o posterior, únase [al programa Windows Insider](https://insider.windows.com/en-us/) y seleccione el anillo "rápido" o el anillo "lento".</span><span class="sxs-lookup"><span data-stu-id="85782-108">To make sure you are using build 18917 or higher please join [the Windows Insider Program](https://insider.windows.com/en-us/) and select the 'Fast' ring or the 'Slow' ring.</span></span> 
   - <span data-ttu-id="85782-109">Para comprobar la versión de Windows, abra el símbolo del sistema y ejecute el comando `ver`.</span><span class="sxs-lookup"><span data-stu-id="85782-109">You can check your Windows version by opening Command Prompt and running the `ver` command.</span></span>
- <span data-ttu-id="85782-110">Habilitación del componente opcional "Plataforma de máquina virtual"</span><span class="sxs-lookup"><span data-stu-id="85782-110">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="85782-111">Establecimiento de una distribución que respaldará WSL 2 mediante la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="85782-111">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="85782-112">Comprobación de qué versiones de WSL están usando las distribuciones</span><span class="sxs-lookup"><span data-stu-id="85782-112">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a><span data-ttu-id="85782-113">Habilite el componente opcional "plataforma de máquina virtual" y asegúrese de que WSL está habilitado.</span><span class="sxs-lookup"><span data-stu-id="85782-113">Enable the 'Virtual Machine Platform' optional component and make sure WSL is enabled</span></span>

<span data-ttu-id="85782-114">Tendrá que asegurarse de que tiene instalados los componentes opcionales del subsistema de Windows para Linux y de la plataforma de máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="85782-114">You will need to make sure that you have both the Windows Subsystem for Linux and the Virtual Machine Platform optional components installed.</span></span> <span data-ttu-id="85782-115">Puede hacerlo mediante la ejecución del siguiente comando en PowerShell:</span><span class="sxs-lookup"><span data-stu-id="85782-115">You can do that by running the following command in PowerShell:</span></span> 

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

<span data-ttu-id="85782-116">Reinicie el equipo para finalizar la instalación de ambos componentes.</span><span class="sxs-lookup"><span data-stu-id="85782-116">Please restart your machine to finish installing both components.</span></span>


## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="85782-117">Establecimiento de una distribución que respaldará WSL 2 mediante la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="85782-117">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="85782-118">Si no tiene instalado un distribución de Linux, consulte la página de documentos [instalar en Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) para obtener instrucciones sobre cómo instalar uno.</span><span class="sxs-lookup"><span data-stu-id="85782-118">If you do not have a Linux distro installed, please refer to the [Install on Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) docs page for instructions on installing one.</span></span> 

<span data-ttu-id="85782-119">Para establecer un distribución, ejecute:</span><span class="sxs-lookup"><span data-stu-id="85782-119">To set a distro please run:</span></span> 

```
wsl --set-version <Distro> 2
```

<span data-ttu-id="85782-120">Asegúrate de reemplazar `<Distro>` por el nombre real de tu distribución.</span><span class="sxs-lookup"><span data-stu-id="85782-120">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="85782-121">(Puedes encontrarlo con el comando: `wsl -l`).</span><span class="sxs-lookup"><span data-stu-id="85782-121">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="85782-122">Puedes volver a cambiar a WSL 1 en cualquier momento; para ello, ejecuta el mismo comando que antes, pero reemplaza "2" por "1".</span><span class="sxs-lookup"><span data-stu-id="85782-122">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="85782-123">Además, si quieres que WSL 2 sea la arquitectura predeterminada, puedes hacerlo con este comando:</span><span class="sxs-lookup"><span data-stu-id="85782-123">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

```
wsl --set-default-version 2
```

<span data-ttu-id="85782-124">Esto hará que las nuevas distribuciones que instales se inicialicen como distribución de WSL 2.</span><span class="sxs-lookup"><span data-stu-id="85782-124">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="85782-125">Comprobación final de qué versiones de WSL están usando las distribuciones</span><span class="sxs-lookup"><span data-stu-id="85782-125">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="85782-126">Para comprobar qué versiones de WSL usa cada distribución, use el siguiente comando (solo disponible en Windows compilación 18917 o posterior):</span><span class="sxs-lookup"><span data-stu-id="85782-126">To verify what versions of WSL each distro is using use the following command (only available in Windows Build 18917 or higher):</span></span>

<span data-ttu-id="85782-127">`wsl --list --verbose` o `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="85782-127">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="85782-128">La distribución que has elegido anteriormente debería mostrar ahora un "2" en la columna "version" (versión).</span><span class="sxs-lookup"><span data-stu-id="85782-128">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="85782-129">Ahora que ya has completado los pasos, puedes empezar a usar tu distribución de WSL 2.</span><span class="sxs-lookup"><span data-stu-id="85782-129">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 

## <a name="troubleshooting"></a><span data-ttu-id="85782-130">Solución de problemas:</span><span class="sxs-lookup"><span data-stu-id="85782-130">Troubleshooting:</span></span> 

<span data-ttu-id="85782-131">A continuación se muestran errores relacionados con la instalación de WSL 2 y las correcciones sugeridas.</span><span class="sxs-lookup"><span data-stu-id="85782-131">Below are related errors and suggested fixes when installing WSL 2.</span></span> <span data-ttu-id="85782-132">Consulta la [página de solución de problemas de WSL](troubleshooting.md) para ver otros errores generales de WSL y sus soluciones.</span><span class="sxs-lookup"><span data-stu-id="85782-132">Please refer to the [WSL troubleshooting page](troubleshooting.md) for other general WSL errors and their solutions.</span></span>

* <span data-ttu-id="85782-133">**Error en la instalación 0x80070003 o 0x80370102**</span><span class="sxs-lookup"><span data-stu-id="85782-133">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
    * <span data-ttu-id="85782-134">Asegúrate de que la virtualización está habilitada dentro del BIOS del equipo.</span><span class="sxs-lookup"><span data-stu-id="85782-134">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="85782-135">Las instrucciones sobre cómo hacerlo variarán de un equipo a otro y lo más probable es que esta característica esté en opciones relacionadas con la CPU.</span><span class="sxs-lookup"><span data-stu-id="85782-135">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>
   
* <span data-ttu-id="85782-136">**Error al intentar actualizar: `Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="85782-136">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
    * <span data-ttu-id="85782-137">Asegúrate de que tienes el Subsistema de Windows para Linux habilitado y de que estás usando la compilación 18917 de Windows o posterior.</span><span class="sxs-lookup"><span data-stu-id="85782-137">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18917 or higher.</span></span> <span data-ttu-id="85782-138">Para habilitar WSL, ejecuta este comando en un símbolo del sistema de PowerShell con privilegios de administrador: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span><span class="sxs-lookup"><span data-stu-id="85782-138">To enable WSL run this command in a Powershell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="85782-139">Puedes encontrar las instrucciones de instalación de WSL completas [aquí](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="85782-139">You can find the full WSL install instructions [here](./install-win10.md).</span></span>

* <span data-ttu-id="85782-140">**No se pudo completar la operación solicitada debido a una limitación del sistema de disco virtual. Los archivos de disco duro virtual deben estar sin comprimir y sin cifrar y no deben ser dispersos.**</span><span class="sxs-lookup"><span data-stu-id="85782-140">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span></span>
    * <span data-ttu-id="85782-141">Consulte [WSL GitHub thread #4103](https://github.com/microsoft/WSL/issues/4103) en el que se realiza el seguimiento de este problema para obtener información actualizada.</span><span class="sxs-lookup"><span data-stu-id="85782-141">Please check [WSL Github thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span></span>

* <span data-ttu-id="85782-142">**El término ' WSL ' no se reconoce como nombre de un cmdlet, función, archivo de script o programa ejecutable.**</span><span class="sxs-lookup"><span data-stu-id="85782-142">**The term 'wsl' is not recognized as the name of a cmdlet, function, script file, or operable program.**</span></span> 
    * <span data-ttu-id="85782-143">Asegúrese de que [está instalado el componente opcional de subsistema de Windows para Linux](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="85782-143">Ensure that the [Windows Subsystem for Linux Optional Component is installed](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled).</span></span><br> <span data-ttu-id="85782-144">Además, si usa un dispositivo Arm64 y ejecuta este comando desde PowerShell, recibirá este error.</span><span class="sxs-lookup"><span data-stu-id="85782-144">Additionally, if you are using an Arm64 device and running this command from PowerShell, you will receive this error.</span></span> <span data-ttu-id="85782-145">En su lugar, ejecute `wsl.exe` desde [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6)o el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="85782-145">Instead run `wsl.exe` from [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6), or Command Prompt.</span></span> 
