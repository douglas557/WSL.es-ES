---
title: Instalación del subsistema Linux en Windows Server
description: Instrucciones de instalación del subsistema Linux en Windows Server.
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, subsistemawindows, ubuntu, windows server
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: 51a2e3f3443ed9b1ba3d8ab79977f22839ee0283
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269779"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="d96ca-104">Guía de instalación de Windows Server</span><span class="sxs-lookup"><span data-stu-id="d96ca-104">Windows Server Installation Guide</span></span>

> <span data-ttu-id="d96ca-105">Se aplica a Windows Server 2019 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="d96ca-105">Applies to Windows Server 2019 and later</span></span>

<span data-ttu-id="d96ca-106">En //Build2017, Microsoft anunció que el Subsistema de Windows para Linux estará [disponible en Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).</span><span class="sxs-lookup"><span data-stu-id="d96ca-106">At //Build2017, Microsoft announced that Windows Subsystem for Linux will be [available on Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).</span></span>  <span data-ttu-id="d96ca-107">Estas instrucciones te guiarán en la ejecución del Subsistema de Windows para Linux en Windows Server 1709 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d96ca-107">These instructions walk through running the Windows Subsystem for Linux on Windows Server 1709 and later.</span></span>

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="d96ca-108">Habilitación del Subsistema de Windows para Linux (WSL)</span><span class="sxs-lookup"><span data-stu-id="d96ca-108">Enable the Windows Subsystem for Linux (WSL)</span></span>

<span data-ttu-id="d96ca-109">Para poder ejecutar distribuciones de Linux en Windows, debes habilitar la característica opcional "Subsistema de Windows para Linux" y reiniciar.</span><span class="sxs-lookup"><span data-stu-id="d96ca-109">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

1. <span data-ttu-id="d96ca-110">Abre PowerShell como administrador y ejecuta:</span><span class="sxs-lookup"><span data-stu-id="d96ca-110">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="d96ca-111">Reinicia el equipo cuando se te solicite.</span><span class="sxs-lookup"><span data-stu-id="d96ca-111">Restart your computer when prompted.</span></span> <span data-ttu-id="d96ca-112">**Este reinicio es necesario** para garantizar que WSL pueda iniciar un entorno de ejecución de confianza.</span><span class="sxs-lookup"><span data-stu-id="d96ca-112">**This reboot is required** in order to ensure that WSL can initiate a trusted execution environment.</span></span>

## <a name="download-a-linux-distro"></a><span data-ttu-id="d96ca-113">Descarga de un distribución de Linux</span><span class="sxs-lookup"><span data-stu-id="d96ca-113">Download a Linux distro</span></span>

<span data-ttu-id="d96ca-114">Sigue [estas instrucciones](install-manual.md) para descargar su distribución de Linux favorita.</span><span class="sxs-lookup"><span data-stu-id="d96ca-114">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distro"></a><span data-ttu-id="d96ca-115">Extracción e instalación de una distribución de Linux</span><span class="sxs-lookup"><span data-stu-id="d96ca-115">Extract and install a Linux distro</span></span>
<span data-ttu-id="d96ca-116">Ahora que has descargado una distribución, extrae su contenido e instala manualmente la distribución:</span><span class="sxs-lookup"><span data-stu-id="d96ca-116">Now that you've downloaded a distro, extract its contents and manually install the distro:</span></span>

1. <span data-ttu-id="d96ca-117">Extrae el contenido del paquete de `<distro>.appx`, por ejemplo, mediante PowerShell:</span><span class="sxs-lookup"><span data-stu-id="d96ca-117">Extract the `<distro>.appx` package's contents, e.g. using PowerShell:</span></span>

    ```powershell
    Rename-Item ./Ubuntu.appx ./Ubuntu.zip
    Expand-Archive ./Ubuntu.zip ./Ubuntu
    ```

2. <span data-ttu-id="d96ca-118">Ejecuta el iniciador de distribuciones para completar la instalación y ejecute la aplicación del iniciador de distribuciones en la carpeta de destino, denominada `<distro>.exe`.</span><span class="sxs-lookup"><span data-stu-id="d96ca-118">Run the distro launcher To complete installation, run the distro launcher application in the target folder, named `<distro>.exe`.</span></span> <span data-ttu-id="d96ca-119">Por ejemplo: `ubuntu.exe`, etc.</span><span class="sxs-lookup"><span data-stu-id="d96ca-119">For example: `ubuntu.exe`, etc.</span></span>

    ![Distribución de Ubuntu ampliada en Windows Server](media/server-appx-expand.png)

    > <span data-ttu-id="d96ca-121">**Solución de problemas**</span><span class="sxs-lookup"><span data-stu-id="d96ca-121">**Troubleshooting**</span></span>
    > * <span data-ttu-id="d96ca-122">**Error 0x8007007e en la instalación**: Este error se produce cuando el sistema no es compatible con WSL.</span><span class="sxs-lookup"><span data-stu-id="d96ca-122">**Installation failed with error 0x8007007e**: This error occurs when your system doesn't support WSL.</span></span> <span data-ttu-id="d96ca-123">Asegúrese de que:</span><span class="sxs-lookup"><span data-stu-id="d96ca-123">Make sure that:</span></span>
    >   * <span data-ttu-id="d96ca-124">Estás ejecutando la compilación 16215 de Windows o una posterior.</span><span class="sxs-lookup"><span data-stu-id="d96ca-124">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="d96ca-125">[Comprueba el número de compilación](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="d96ca-125">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
    >   * <span data-ttu-id="d96ca-126">El componente opcional del subsistema de Windows para Linux está habilitado y se ha reiniciado el equipo.</span><span class="sxs-lookup"><span data-stu-id="d96ca-126">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="d96ca-127">[Asegúrate de que WSL está habilitado](troubleshooting.md#confirm-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="d96ca-127">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
    
3. <span data-ttu-id="d96ca-128">Agrega la ruta de acceso de distribución a la variable de entorno PATH de Windows (`C:\Users\Administrator\Ubuntu` en este ejemplo), por ejemplo, mediante PowerShell:</span><span class="sxs-lookup"><span data-stu-id="d96ca-128">Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), e.g. using Powershell:</span></span>
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    <span data-ttu-id="d96ca-129">Ahora puedes escribir `<distro>.exe` para iniciar la distribución desde cualquier ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="d96ca-129">You can now launch your distro from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="d96ca-130">Por ejemplo: `ubuntu.exe`</span><span class="sxs-lookup"><span data-stu-id="d96ca-130">For example: `ubuntu.exe`</span></span>

<span data-ttu-id="d96ca-131">Ahora que está instalada la distribución de Linux, debes [inicializar la nueva instancia de la distribución](initialize-distro.md) antes de usarla.</span><span class="sxs-lookup"><span data-stu-id="d96ca-131">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) before using your distro.</span></span>
