---
title: Instalación del subsistema Linux en Windows Server
description: Instrucciones de instalación del subsistema Linux en Windows Server.
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, subsistemawindows, ubuntu, windows server
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: ebcd7f6b10d2b734b1f2a66f64a5e3292855bcf4
ms.sourcegitcommit: 5d3898772851e6ac9a310f219cc0d71278f95d22
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/10/2020
ms.locfileid: "84671025"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="ffb17-104">Guía de instalación de Windows Server</span><span class="sxs-lookup"><span data-stu-id="ffb17-104">Windows Server Installation Guide</span></span>

<span data-ttu-id="ffb17-105">El Subsistema de Windows para Linux está disponible para su instalación en Windows Server 2019 (versión 1709) y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="ffb17-105">The Windows Subsystem for Linux is available for installation on Windows Server 2019 (version 1709) and later.</span></span> <span data-ttu-id="ffb17-106">En esta guía se describen los pasos necesarios para habilitar WSL en tu máquina.</span><span class="sxs-lookup"><span data-stu-id="ffb17-106">This guide will walk through the steps of enabling WSL on your machine.</span></span>

## <a name="enable-the-windows-subsystem-for-linux"></a><span data-ttu-id="ffb17-107">Habilitación del Subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="ffb17-107">Enable the Windows Subsystem for Linux</span></span>

<span data-ttu-id="ffb17-108">Para poder ejecutar distribuciones de Linux en Windows, debes habilitar la característica opcional "Subsistema de Windows para Linux" y reiniciar.</span><span class="sxs-lookup"><span data-stu-id="ffb17-108">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

<span data-ttu-id="ffb17-109">Abre PowerShell como administrador y ejecuta:</span><span class="sxs-lookup"><span data-stu-id="ffb17-109">Open PowerShell as Administrator and run:</span></span>

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

```

## <a name="download-a-linux-distribution"></a><span data-ttu-id="ffb17-110">Descarga de una distribución de Linux</span><span class="sxs-lookup"><span data-stu-id="ffb17-110">Download a Linux distribution</span></span>

<span data-ttu-id="ffb17-111">Sigue [estas instrucciones](install-manual.md) para descargar su distribución de Linux favorita.</span><span class="sxs-lookup"><span data-stu-id="ffb17-111">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distribution"></a><span data-ttu-id="ffb17-112">Extracción e instalación de una distribución de Linux</span><span class="sxs-lookup"><span data-stu-id="ffb17-112">Extract and install a Linux distribution</span></span>

<span data-ttu-id="ffb17-113">Ahora que has descargado una distribución de Linux, para extraer su contenido e instalarlo manualmente, sigue estos pasos:</span><span class="sxs-lookup"><span data-stu-id="ffb17-113">Now that you've downloaded a Linux distribution, in order to extract its contents and manually install, follow these steps:</span></span>

1. <span data-ttu-id="ffb17-114">Extrae el contenido del paquete `<distro>.appx` mediante PowerShell:</span><span class="sxs-lookup"><span data-stu-id="ffb17-114">Extract the `<distro>.appx` package's contents, using PowerShell:</span></span>

    ```powershell
    Rename-Item .\Ubuntu.appx .\Ubuntu.zip
    Expand-Archive .\Ubuntu.zip .\Ubuntu
    ```

2. <span data-ttu-id="ffb17-115">Ejecuta la aplicación del iniciador de la distribución en la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="ffb17-115">Run the distribution launcher application in the target folder.</span></span> <span data-ttu-id="ffb17-116">Normalmente, el iniciador se denomina `<distro>.exe` (por ejemplo, `ubuntu.exe`).</span><span class="sxs-lookup"><span data-stu-id="ffb17-116">The launcher is typically named `<distro>.exe` (for example, `ubuntu.exe`).</span></span>

    ![Distribución de Ubuntu ampliada en Windows Server](media/server-appx-expand.png)

> [!CAUTION]
> <span data-ttu-id="ffb17-118">**Error 0x8007007e en la instalación**: Si recibes este error, significa que tu sistema no es compatible con WSL.</span><span class="sxs-lookup"><span data-stu-id="ffb17-118">**Installation failed with error 0x8007007e**: If you receive this error, then your system doesn't support WSL.</span></span> <span data-ttu-id="ffb17-119">Asegúrate de que estás ejecutando la compilación 16215 de Windows o una posterior.</span><span class="sxs-lookup"><span data-stu-id="ffb17-119">Ensure that you're running Windows build 16215 or later.</span></span> <span data-ttu-id="ffb17-120">[Comprueba el número de compilación](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="ffb17-120">[Check your build](troubleshooting.md#check-your-build-number).</span></span> <span data-ttu-id="ffb17-121">Además, [confirma que WSL esté habilitado](troubleshooting.md#confirm-wsl-is-enabled) y que el equipo se haya reiniciado después de haber habilitado la característica.</span><span class="sxs-lookup"><span data-stu-id="ffb17-121">Also check to [confirm that WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled) and your computer was restarted after the feature was enabled.</span></span>  

<span data-ttu-id="ffb17-122">3. Agrega la ruta de acceso de la distribución a la variable de entorno PATH de Windows (`C:\Users\Administrator\Ubuntu` en este ejemplo) mediante PowerShell:</span><span class="sxs-lookup"><span data-stu-id="ffb17-122">3.Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), using PowerShell:</span></span>

```powershell
$userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
[System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
```

<span data-ttu-id="ffb17-123">Ahora puedes escribir `<distro>.exe` para iniciar la distribución desde cualquier ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="ffb17-123">You can now launch your distribution from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="ffb17-124">Por ejemplo: `ubuntu.exe`.</span><span class="sxs-lookup"><span data-stu-id="ffb17-124">For example: `ubuntu.exe`.</span></span>

<span data-ttu-id="ffb17-125">Ahora que está instalada, debes [inicializar la nueva instancia de la distribución](initialize-distro.md) antes de usarla.</span><span class="sxs-lookup"><span data-stu-id="ffb17-125">Now that it is installed, you must [initialize your new distribution instance](initialize-distro.md) before using it.</span></span>
