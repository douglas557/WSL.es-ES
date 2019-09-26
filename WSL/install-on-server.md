---
title: Instalación del subsistema Linux en Windows Server
description: Instrucciones de instalación para el subsistema Linux en Windows Server.
keywords: BashOnWindows, bash, WSL, Windows, subsistema de Windows para Linux, windowssubsystem, Ubuntu, Windows Server
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: 51a2e3f3443ed9b1ba3d8ab79977f22839ee0283
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269779"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="3dbf2-104">Guía de instalación de Windows Server</span><span class="sxs-lookup"><span data-stu-id="3dbf2-104">Windows Server Installation Guide</span></span>

> <span data-ttu-id="3dbf2-105">Se aplica a Windows Server 2019 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="3dbf2-105">Applies to Windows Server 2019 and later</span></span>

<span data-ttu-id="3dbf2-106">En//Build2017, Microsoft anunció que el subsistema de Windows para Linux estará [disponible en Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).</span><span class="sxs-lookup"><span data-stu-id="3dbf2-106">At //Build2017, Microsoft announced that Windows Subsystem for Linux will be [available on Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).</span></span>  <span data-ttu-id="3dbf2-107">Estas instrucciones le guían en la ejecución del subsistema de Windows para Linux en Windows Server 1709 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="3dbf2-107">These instructions walk through running the Windows Subsystem for Linux on Windows Server 1709 and later.</span></span>

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="3dbf2-108">Habilitación del subsistema de Windows para Linux (WSL)</span><span class="sxs-lookup"><span data-stu-id="3dbf2-108">Enable the Windows Subsystem for Linux (WSL)</span></span>

<span data-ttu-id="3dbf2-109">Antes de poder ejecutar Linux distribuciones en Windows, debe habilitar la característica opcional "subsistema de Windows para Linux" y reiniciar.</span><span class="sxs-lookup"><span data-stu-id="3dbf2-109">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

1. <span data-ttu-id="3dbf2-110">Abra PowerShell como administrador y ejecute:</span><span class="sxs-lookup"><span data-stu-id="3dbf2-110">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="3dbf2-111">Reinicie el equipo cuando se le solicite.</span><span class="sxs-lookup"><span data-stu-id="3dbf2-111">Restart your computer when prompted.</span></span> <span data-ttu-id="3dbf2-112">**Este reinicio es necesario** para asegurarse de que WSL pueda iniciar un entorno de ejecución de confianza.</span><span class="sxs-lookup"><span data-stu-id="3dbf2-112">**This reboot is required** in order to ensure that WSL can initiate a trusted execution environment.</span></span>

## <a name="download-a-linux-distro"></a><span data-ttu-id="3dbf2-113">Descarga de un distribución de Linux</span><span class="sxs-lookup"><span data-stu-id="3dbf2-113">Download a Linux distro</span></span>

<span data-ttu-id="3dbf2-114">Siga [estas instrucciones](install-manual.md) para descargar su distribución de Linux favorita.</span><span class="sxs-lookup"><span data-stu-id="3dbf2-114">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distro"></a><span data-ttu-id="3dbf2-115">Extracción e instalación de un distribución de Linux</span><span class="sxs-lookup"><span data-stu-id="3dbf2-115">Extract and install a Linux distro</span></span>
<span data-ttu-id="3dbf2-116">Ahora que ha descargado un distribución, extraiga su contenido e instale manualmente el distribución:</span><span class="sxs-lookup"><span data-stu-id="3dbf2-116">Now that you've downloaded a distro, extract its contents and manually install the distro:</span></span>

1. <span data-ttu-id="3dbf2-117">Extraiga el `<distro>.appx` contenido del paquete, por ejemplo, mediante PowerShell:</span><span class="sxs-lookup"><span data-stu-id="3dbf2-117">Extract the `<distro>.appx` package's contents, e.g. using PowerShell:</span></span>

    ```powershell
    Rename-Item ./Ubuntu.appx ./Ubuntu.zip
    Expand-Archive ./Ubuntu.zip ./Ubuntu
    ```

2. <span data-ttu-id="3dbf2-118">Ejecute el iniciador de distribución para completar la instalación, ejecute la aplicación del iniciador de distribución `<distro>.exe`en la carpeta de destino, denominada.</span><span class="sxs-lookup"><span data-stu-id="3dbf2-118">Run the distro launcher To complete installation, run the distro launcher application in the target folder, named `<distro>.exe`.</span></span> <span data-ttu-id="3dbf2-119">Por ejemplo: `ubuntu.exe`, etc.</span><span class="sxs-lookup"><span data-stu-id="3dbf2-119">For example: `ubuntu.exe`, etc.</span></span>

    ![Se amplió Ubuntu distribución en Windows Server](media/server-appx-expand.png)

    > <span data-ttu-id="3dbf2-121">**Solución de problemas**</span><span class="sxs-lookup"><span data-stu-id="3dbf2-121">**Troubleshooting**</span></span>
    > * <span data-ttu-id="3dbf2-122">**No se pudo realizar la instalación. error 0x8007007e**: Este error se produce cuando el sistema no es compatible con WSL.</span><span class="sxs-lookup"><span data-stu-id="3dbf2-122">**Installation failed with error 0x8007007e**: This error occurs when your system doesn't support WSL.</span></span> <span data-ttu-id="3dbf2-123">Asegúrese de que:</span><span class="sxs-lookup"><span data-stu-id="3dbf2-123">Make sure that:</span></span>
    >   * <span data-ttu-id="3dbf2-124">Está ejecutando Windows Build 16215 o posterior.</span><span class="sxs-lookup"><span data-stu-id="3dbf2-124">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="3dbf2-125">[Compruebe la compilación](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="3dbf2-125">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
    >   * <span data-ttu-id="3dbf2-126">El componente opcional de subsistema de Windows para Linux está habilitado y el equipo se ha reiniciado.</span><span class="sxs-lookup"><span data-stu-id="3dbf2-126">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="3dbf2-127">[Asegúrese de que WSL está habilitado](troubleshooting.md#confirm-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="3dbf2-127">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
    
3. <span data-ttu-id="3dbf2-128">Agregue la ruta de acceso de distribución a la ruta`C:\Users\Administrator\Ubuntu` de acceso del entorno de Windows (en este ejemplo), por ejemplo, con PowerShell:</span><span class="sxs-lookup"><span data-stu-id="3dbf2-128">Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), e.g. using Powershell:</span></span>
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    <span data-ttu-id="3dbf2-129">Ahora puede iniciar el distribución desde cualquier ruta de acceso escribiendo `<distro>.exe`.</span><span class="sxs-lookup"><span data-stu-id="3dbf2-129">You can now launch your distro from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="3dbf2-130">Por ejemplo: `ubuntu.exe`</span><span class="sxs-lookup"><span data-stu-id="3dbf2-130">For example: `ubuntu.exe`</span></span>

<span data-ttu-id="3dbf2-131">Ahora que está instalado el distribución de Linux, debe [inicializar la nueva instancia de distribución](initialize-distro.md) antes de usar su distribución.</span><span class="sxs-lookup"><span data-stu-id="3dbf2-131">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) before using your distro.</span></span>
