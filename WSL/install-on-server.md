---
title: Instalación del subsistema Linux en Windows Server
description: Instrucciones de instalación del subsistema Linux en Windows Server.
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, subsistemawindows, ubuntu, windows server
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 86fd7de0ef45af760f46bb2a18932f513b813609
ms.sourcegitcommit: 1b6191351bbf9e95f3c28fc67abe4bf1bcfd3336
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2020
ms.locfileid: "83270889"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="95581-104">Guía de instalación de Windows Server</span><span class="sxs-lookup"><span data-stu-id="95581-104">Windows Server Installation Guide</span></span>

<span data-ttu-id="95581-105">El Subsistema de Windows para Linux está disponible para su instalación en Windows Server 2019 (versión 1709) y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="95581-105">The Windows Subsystem for Linux is available for installation on Windows Server 2019 (version 1709) and later.</span></span> <span data-ttu-id="95581-106">En esta guía se describen los pasos necesarios para habilitar WSL en tu máquina.</span><span class="sxs-lookup"><span data-stu-id="95581-106">This guide will walk through the steps of enabling WSL on your machine.</span></span>

## <a name="enable-the-windows-subsystem-for-linux"></a><span data-ttu-id="95581-107">Habilitación del Subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="95581-107">Enable the Windows Subsystem for Linux</span></span>

<span data-ttu-id="95581-108">Para poder ejecutar distribuciones de Linux en Windows, debes habilitar la característica opcional "Subsistema de Windows para Linux" y reiniciar.</span><span class="sxs-lookup"><span data-stu-id="95581-108">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

<span data-ttu-id="95581-109">Abre PowerShell como administrador y ejecuta:</span><span class="sxs-lookup"><span data-stu-id="95581-109">Open PowerShell as Administrator and run:</span></span>

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

```

<span data-ttu-id="95581-110">**Si buscas obtener una compatibilidad completa con las llamadas del sistema y un mayor rendimiento de E/S, lee la documentación que hay a continuación para instalar WSL 2.**</span><span class="sxs-lookup"><span data-stu-id="95581-110">**If you're looking for 100% system call compatibility and faster IO performance, read below to install WSL 2!**</span></span>

<span data-ttu-id="95581-111">WSL 2 solo está disponible en Windows 10, versión 2004, compilación 19041 o posteriores.</span><span class="sxs-lookup"><span data-stu-id="95581-111">WSL 2 is only available in Windows 10, Version 2004, Build 19041 or higher.</span></span> <span data-ttu-id="95581-112">Tendrás que [actualizar la versión de Windows](ms-settings:windowsupdate) y [unirte al programa Windows Insider](https://insider.windows.com/insidersigninboth/) en el anillo "Versión preliminar" hasta el lanzamiento de la versión pública a finales de mayo.</span><span class="sxs-lookup"><span data-stu-id="95581-112">You will need to [update your Windows version](ms-settings:windowsupdate) and [join the Windows Insider program](https://insider.windows.com/insidersigninboth/) on the "Release Preview" ring until the public release in late May.</span></span>

<span data-ttu-id="95581-113">**Si continúas con WSL 1, reinicia la máquina cuando se te pida y sigue con la instalación [aquí](./install-on-server.md#download-a-linux-distribution)** .</span><span class="sxs-lookup"><span data-stu-id="95581-113">**If continuing with WSL 1, restart your machine when prompted and continue with installation [here](./install-on-server.md#download-a-linux-distribution)**</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component"></a><span data-ttu-id="95581-114">Habilitación del componente opcional Plataforma de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="95581-114">Enable the Virtual Machine Platform optional component</span></span>

<span data-ttu-id="95581-115">Asegúrate de que el componente opcional "Plataforma de máquina virtual" esté instalado.</span><span class="sxs-lookup"><span data-stu-id="95581-115">Ensure the 'Virtual Machine Platform' optional component is installed.</span></span> <span data-ttu-id="95581-116">Para hacerlo ejecuta el siguiente comando en PowerShell:</span><span class="sxs-lookup"><span data-stu-id="95581-116">You can do that by running the following command in PowerShell:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

## <a name="download-a-linux-distribution"></a><span data-ttu-id="95581-117">Descarga de una distribución de Linux</span><span class="sxs-lookup"><span data-stu-id="95581-117">Download a Linux distribution</span></span>

<span data-ttu-id="95581-118">Sigue [estas instrucciones](install-manual.md) para descargar su distribución de Linux favorita.</span><span class="sxs-lookup"><span data-stu-id="95581-118">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distribution"></a><span data-ttu-id="95581-119">Extracción e instalación de una distribución de Linux</span><span class="sxs-lookup"><span data-stu-id="95581-119">Extract and install a Linux distribution</span></span>

<span data-ttu-id="95581-120">Ahora que has descargado una distribución de Linux, para extraer su contenido e instalarlo manualmente, sigue estos pasos:</span><span class="sxs-lookup"><span data-stu-id="95581-120">Now that you've downloaded a Linux distribution, in order to extract its contents and manually install, follow these steps:</span></span>

1. <span data-ttu-id="95581-121">Extrae el contenido del paquete `<distro>.appx` mediante PowerShell:</span><span class="sxs-lookup"><span data-stu-id="95581-121">Extract the `<distro>.appx` package's contents, using PowerShell:</span></span>

    ```powershell
    Rename-Item .\Ubuntu.appx .\Ubuntu.zip
    Expand-Archive .\Ubuntu.zip .\Ubuntu
    ```

2. <span data-ttu-id="95581-122">Ejecuta la aplicación del iniciador de la distribución en la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="95581-122">Run the distribution launcher application in the target folder.</span></span> <span data-ttu-id="95581-123">Normalmente, el iniciador se denomina `<distro>.exe` (por ejemplo, `ubuntu.exe`).</span><span class="sxs-lookup"><span data-stu-id="95581-123">The launcher is typically named `<distro>.exe` (for example, `ubuntu.exe`).</span></span>

    ![Distribución de Ubuntu ampliada en Windows Server](media/server-appx-expand.png)

> [!CAUTION]
> <span data-ttu-id="95581-125">**Error 0x8007007e en la instalación**: Si recibes este error, significa que tu sistema no es compatible con WSL.</span><span class="sxs-lookup"><span data-stu-id="95581-125">**Installation failed with error 0x8007007e**: If you receive this error, then your system doesn't support WSL.</span></span> <span data-ttu-id="95581-126">Asegúrate de que estás ejecutando la compilación 16215 de Windows o una posterior.</span><span class="sxs-lookup"><span data-stu-id="95581-126">Ensure that you're running Windows build 16215 or later.</span></span> <span data-ttu-id="95581-127">[Comprueba el número de compilación](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="95581-127">[Check your build](troubleshooting.md#check-your-build-number).</span></span> <span data-ttu-id="95581-128">Además, [confirma que WSL esté habilitado](troubleshooting.md#confirm-wsl-is-enabled) y que el equipo se haya reiniciado después de haber habilitado la característica.</span><span class="sxs-lookup"><span data-stu-id="95581-128">Also check to [confirm that WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled) and your computer was restarted after the feature was enabled.</span></span>  

<span data-ttu-id="95581-129">3. Agrega la ruta de acceso de la distribución a la variable de entorno PATH de Windows (`C:\Users\Administrator\Ubuntu` en este ejemplo) mediante PowerShell:</span><span class="sxs-lookup"><span data-stu-id="95581-129">3.Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), using PowerShell:</span></span>

```powershell
$userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
[System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
```

<span data-ttu-id="95581-130">Ahora puedes escribir `<distro>.exe` para iniciar la distribución desde cualquier ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="95581-130">You can now launch your distribution from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="95581-131">Por ejemplo: `ubuntu.exe`.</span><span class="sxs-lookup"><span data-stu-id="95581-131">For example: `ubuntu.exe`.</span></span>

<span data-ttu-id="95581-132">Ahora que está instalada, debes [inicializar la nueva instancia de la distribución](initialize-distro.md) antes de usarla.</span><span class="sxs-lookup"><span data-stu-id="95581-132">Now that it is installed, you must [initialize your new distribution instance](initialize-distro.md) before using it.</span></span>
