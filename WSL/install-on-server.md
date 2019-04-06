---
title: Instale el subsistema de Linux en Windows Server
description: Instrucciones de instalación para el subsistema de Linux en Windows Server.
keywords: BashOnWindows, bash, wsl, windows, el subsistema de windows para linux, windowssubsystem, ubuntu, windows server
author: scooley
ms.author: scooley
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: c0b8af08a06428ebd292b8c6b9b275726988bdbe
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063623"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="b0c77-104">Guía de instalación de Windows Server</span><span class="sxs-lookup"><span data-stu-id="b0c77-104">Windows Server Installation Guide</span></span>

> <span data-ttu-id="b0c77-105">Se aplica a Windows Server 2019 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="b0c77-105">Applies to Windows Server 2019 and later</span></span>

<span data-ttu-id="b0c77-106">En / / Build2017, Microsoft anunció que el subsistema de Windows para Linux será [disponible en Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).</span><span class="sxs-lookup"><span data-stu-id="b0c77-106">At //Build2017, Microsoft announced that Windows Subsystem for Linux will be [available on Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).</span></span>  <span data-ttu-id="b0c77-107">Estas instrucciones se recorra ejecuta el subsistema de Windows para Linux en Windows Server 1709 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b0c77-107">These instructions walk through running the Windows Subsystem for Linux on Windows Server 1709 and later.</span></span>

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="b0c77-108">Habilitar el subsistema Windows para Linux (WSL)</span><span class="sxs-lookup"><span data-stu-id="b0c77-108">Enable the Windows Subsystem for Linux (WSL)</span></span>

<span data-ttu-id="b0c77-109">Antes de poder ejecutar las distribuciones de Linux en Windows, debe habilitar la característica opcional "Subsistema de Windows para Linux" y reinicie.</span><span class="sxs-lookup"><span data-stu-id="b0c77-109">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

1. <span data-ttu-id="b0c77-110">Abra PowerShell como administrador y ejecute:</span><span class="sxs-lookup"><span data-stu-id="b0c77-110">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="b0c77-111">Reinicie el equipo cuando se le solicite.</span><span class="sxs-lookup"><span data-stu-id="b0c77-111">Restart your computer when prompted.</span></span> <span data-ttu-id="b0c77-112">**Este reinicio es necesario** con el fin de asegurarse de que WSL puede iniciar un entorno de ejecución de confianza.</span><span class="sxs-lookup"><span data-stu-id="b0c77-112">**This reboot is required** in order to ensure that WSL can initiate a trusted execution environment.</span></span>

## <a name="download-a-linux-distro"></a><span data-ttu-id="b0c77-113">Descargue una distribución de Linux</span><span class="sxs-lookup"><span data-stu-id="b0c77-113">Download a Linux distro</span></span>

<span data-ttu-id="b0c77-114">Siga [estas instrucciones](install-manual.md) para descargar la distribución de Linux favorita.</span><span class="sxs-lookup"><span data-stu-id="b0c77-114">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distro"></a><span data-ttu-id="b0c77-115">Extraer e instalar una distribución de Linux</span><span class="sxs-lookup"><span data-stu-id="b0c77-115">Extract and install a Linux distro</span></span>
<span data-ttu-id="b0c77-116">Ahora que ha descargado una distribución, extraiga el contenido e instalar manualmente la distribución:</span><span class="sxs-lookup"><span data-stu-id="b0c77-116">Now that you've downloaded a distro, extract its contents and manually install the distro:</span></span>

1. <span data-ttu-id="b0c77-117">Extraer el `<distro>.appx` contenido del paquete, por ejemplo, mediante PowerShell:</span><span class="sxs-lookup"><span data-stu-id="b0c77-117">Extract the `<distro>.appx` package's contents, e.g. using PowerShell:</span></span>

    ```powershell
    Rename-Item ~/Ubuntu.appx ~/Ubuntu.zip
    Expand-Archive ~/Ubuntu.zip ~/Ubuntu
    ```

2. <span data-ttu-id="b0c77-118">Ejecute el iniciador de distribución para completar la instalación, ejecute la aplicación de selector de distribución en la carpeta de destino, denominado `<distro>.exe`.</span><span class="sxs-lookup"><span data-stu-id="b0c77-118">Run the distro launcher To complete installation, run the distro launcher application in the target folder, named `<distro>.exe`.</span></span> <span data-ttu-id="b0c77-119">Por ejemplo: `ubuntu.exe`, etcetera.</span><span class="sxs-lookup"><span data-stu-id="b0c77-119">For example: `ubuntu.exe`, etc.</span></span>

    ![Distribución de Ubuntu expandida en Windows Server](media/server-appx-expand.png)

    > **<span data-ttu-id="b0c77-121">Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="b0c77-121">Troubleshooting</span></span>**
    > * <span data-ttu-id="b0c77-122">**Error de instalación 0x8007007e**: Este error se produce cuando el sistema no admite WSL.</span><span class="sxs-lookup"><span data-stu-id="b0c77-122">**Installation failed with error 0x8007007e**: This error occurs when your system doesn't support WSL.</span></span> <span data-ttu-id="b0c77-123">Asegúrese de que:</span><span class="sxs-lookup"><span data-stu-id="b0c77-123">Make sure that:</span></span>
    >   * <span data-ttu-id="b0c77-124">Ya está ejecutando Windows compilación 16215 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b0c77-124">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="b0c77-125">[Comprobar la compilación](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="b0c77-125">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
    >   * <span data-ttu-id="b0c77-126">El subsistema de Windows para el componente opcional de Linux está habilitado y ha reiniciado el equipo.</span><span class="sxs-lookup"><span data-stu-id="b0c77-126">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="b0c77-127">[Asegúrese de que está habilitado WSL](troubleshooting.md#confirm-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="b0c77-127">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
    
3. <span data-ttu-id="b0c77-128">Agregar la ruta de acceso de distribución a la ruta de acceso de entorno de Windows (`C:\Users\Administrator\Ubuntu` en este ejemplo), por ejemplo, mediante Powershell:</span><span class="sxs-lookup"><span data-stu-id="b0c77-128">Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), e.g. using Powershell:</span></span>
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + "C:\Users\Administrator\Ubuntu", "User")
    ```
    <span data-ttu-id="b0c77-129">Ahora puede iniciar la distribución de cualquier ruta de acceso escribiendo `<distro>.exe`.</span><span class="sxs-lookup"><span data-stu-id="b0c77-129">You can now launch your distro from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="b0c77-130">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="b0c77-130">For example:</span></span> `ubuntu.exe`

<span data-ttu-id="b0c77-131">Ahora que está instalada la distribución de Linux, debe [inicializar la nueva instancia de la distribución](initialize-distro.md) antes de usar la distribución.</span><span class="sxs-lookup"><span data-stu-id="b0c77-131">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) before using your distro.</span></span>
