---
title: Descarga manual de distribuciones del Subsistema de Windows para Linux (WSL)
description: Instrucciones sobre cómo descargar manualmente distribuciones del Subsistema de Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, WSL, subsistema de windows, distribución, ubuntu, openSUSE, SLES, debian, kali
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 37d8ad589d0108534c27137614a005c0c0ac55bc
ms.sourcegitcommit: 0a001ada2131f80dd77b114fc14f2fde43c947ad
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/25/2020
ms.locfileid: "80256378"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a><span data-ttu-id="0ed6e-104">Descarga manual de paquetes de distribuciones del subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="0ed6e-104">Manually download Windows Subsystem for Linux distro packages</span></span>

<span data-ttu-id="0ed6e-105">Hay varios escenarios en los que quizás no podrás (o no querrás) instalar distribuciones WSL Linux a través de Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="0ed6e-105">There are several scenarios in which you may not be able (or want) to, install WSL Linux distros via the Microsoft Store.</span></span> <span data-ttu-id="0ed6e-106">En concreto, es posible que estés ejecutando una SKU de sistema operativo de escritorio de Windows Server o de mantenimiento a largo plazo (LTSC) que no sea compatible Microsoft Store, o que tus administradores o directivas de red corporativa no permitan el uso de Microsoft Store en tu entorno.</span><span class="sxs-lookup"><span data-stu-id="0ed6e-106">Specifically, you may be running a Windows Server or Long-Term Servicing (LTSC) desktop OS SKU that doesn't support Microsoft Store, or your corporate network policies and/or admins to not permit Microsoft Store usage in your environment.</span></span>

<span data-ttu-id="0ed6e-107">En estos casos, aunque WSL esté disponible, ¿cómo se descargan e instalan las distribuciones de Linux en WSL si no se puede acceder a Microsoft Store?</span><span class="sxs-lookup"><span data-stu-id="0ed6e-107">In these cases, while WSL itself is available, how do you download and install Linux distros in WSL if you can't access the store?</span></span>

> <span data-ttu-id="0ed6e-108">Nota: **Los entornos de shell de línea de comandos, incluidos Cmd, PowerShell y las distribuciones de Linux/WSL, no se pueden ejecutar en modo Windows 10 S**.</span><span class="sxs-lookup"><span data-stu-id="0ed6e-108">Note: **Command-line shell environments including Cmd, PowerShell, and Linux/WSL distros are not permitted to run on Windows 10 S Mode**.</span></span> <span data-ttu-id="0ed6e-109">Esta restricción existe con el fin de garantizar la integridad y los objetivos de seguridad que ofrece el modo S: Lee [esta publicación](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="0ed6e-109">This restriction exists in order to ensure the integrity and safety goals that S Mode delivers: Read [this post](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) for more information.</span></span>

## <a name="downloading-distros"></a><span data-ttu-id="0ed6e-110">Descarga de distribuciones</span><span class="sxs-lookup"><span data-stu-id="0ed6e-110">Downloading distros</span></span>

<span data-ttu-id="0ed6e-111">Si la aplicación Microsoft Store no está disponible, puedes descargar e instalar manualmente distribuciones de Linux a través de estos vínculos:</span><span class="sxs-lookup"><span data-stu-id="0ed6e-111">If the Microsoft Store app is not available, you can download and manually install Linux distros by clicking these links:</span></span>
* [<span data-ttu-id="0ed6e-112">Ubuntu 18.04</span><span class="sxs-lookup"><span data-stu-id="0ed6e-112">Ubuntu 18.04</span></span>](https://aka.ms/wsl-ubuntu-1804)
* [<span data-ttu-id="0ed6e-113">Ubuntu 18.04 ARM</span><span class="sxs-lookup"><span data-stu-id="0ed6e-113">Ubuntu 18.04 ARM</span></span>](https://aka.ms/wsl-ubuntu-1804-arm)
* [<span data-ttu-id="0ed6e-114">Ubuntu 16.04</span><span class="sxs-lookup"><span data-stu-id="0ed6e-114">Ubuntu 16.04</span></span>](https://aka.ms/wsl-ubuntu-1604)
* [<span data-ttu-id="0ed6e-115">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="0ed6e-115">Debian GNU/Linux</span></span>](https://aka.ms/wsl-debian-gnulinux)
* [<span data-ttu-id="0ed6e-116">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="0ed6e-116">Kali Linux</span></span>](https://aka.ms/wsl-kali-linux-new)
* [<span data-ttu-id="0ed6e-117">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="0ed6e-117">OpenSUSE Leap 42</span></span>](https://aka.ms/wsl-opensuse-42)
* [<span data-ttu-id="0ed6e-118">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="0ed6e-118">SUSE Linux Enterprise Server 12</span></span>](https://aka.ms/wsl-sles-12)
* [<span data-ttu-id="0ed6e-119">Fedora Remix for WSL</span><span class="sxs-lookup"><span data-stu-id="0ed6e-119">Fedora Remix for WSL</span></span>](https://github.com/WhitewaterFoundry/WSLFedoraRemix/releases/)

<span data-ttu-id="0ed6e-120">Al hacerlo, los paquetes de `<distro>.appx` se descargarán en una carpeta de tu elección.</span><span class="sxs-lookup"><span data-stu-id="0ed6e-120">This will cause the `<distro>.appx` packages to download to a folder of your choosing.</span></span> <span data-ttu-id="0ed6e-121">Sigue las [instrucciones de instalación](#installing-your-distro) para instalar las distribuciones descargadas.</span><span class="sxs-lookup"><span data-stu-id="0ed6e-121">Follow the [installation instructions](#installing-your-distro) to install your downloaded distro(s).</span></span>

## <a name="downloading-distros-via-the-command-line"></a><span data-ttu-id="0ed6e-122">Descarga de distribuciones a través de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="0ed6e-122">Downloading distros via the command line</span></span>
<span data-ttu-id="0ed6e-123">Si lo prefieres, también puedes descargar tus distribuciones preferidas a través de la línea de comandos:</span><span class="sxs-lookup"><span data-stu-id="0ed6e-123">If you prefer, you can also download your preferred distro(s) via the command line:</span></span>

 ### <a name="download-using-powershell"></a><span data-ttu-id="0ed6e-124">Descarga con PowerShell</span><span class="sxs-lookup"><span data-stu-id="0ed6e-124">Download using PowerShell</span></span>
 <span data-ttu-id="0ed6e-125">Para descargar distribuciones con PowerShell, usa el cmdlet [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest).</span><span class="sxs-lookup"><span data-stu-id="0ed6e-125">To download distros using PowerShell, use the [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) cmdlet.</span></span> <span data-ttu-id="0ed6e-126">A continuación se muestra una instrucción de ejemplo para descargar Ubuntu 16.04.</span><span class="sxs-lookup"><span data-stu-id="0ed6e-126">Here's a sample instruction to download Ubuntu 16.04.</span></span>

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> <span data-ttu-id="0ed6e-127">Si la descarga tarda mucho tiempo, establece `$ProgressPreference = 'SilentlyContinue'` para desactivar la barra de progreso.</span><span class="sxs-lookup"><span data-stu-id="0ed6e-127">If the download is taking a long time, turn off the progress bar by setting `$ProgressPreference = 'SilentlyContinue'`</span></span>

### <a name="download-using-curl"></a><span data-ttu-id="0ed6e-128">Descarga mediante curl</span><span class="sxs-lookup"><span data-stu-id="0ed6e-128">Download using curl</span></span>
<span data-ttu-id="0ed6e-129">Windows 10 Spring 2018 Update (o posterior) incluye la popular [utilidad de línea de comandos curl](https://curl.haxx.se/), con la que puedes invocar solicitudes web (como los comandos HTTP GET, POST, PUT, etc.) desde la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="0ed6e-129">Windows 10 Spring 2018 Update (or later) includes the popular [curl command-line utility](https://curl.haxx.se/) with which you can invoke web requests (i.e. HTTP GET, POST, PUT, etc. commands) from the command line.</span></span> <span data-ttu-id="0ed6e-130">Puedes usar `curl.exe` para descargar las distribuciones anteriores:</span><span class="sxs-lookup"><span data-stu-id="0ed6e-130">You can use `curl.exe` to download the above distros:</span></span>

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

<span data-ttu-id="0ed6e-131">En el ejemplo anterior, se ejecuta `curl.exe` (no solo `curl`) para garantizar que, en PowerShell, se invoque el ejecutable de curl real, no el alias de curl de PowerShell para [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6).</span><span class="sxs-lookup"><span data-stu-id="0ed6e-131">In the above example, `curl.exe` is executed (not just `curl`) to ensure that, in PowerShell, the real curl executable is invoked, not the PowerShell curl alias for [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)</span></span>

> <span data-ttu-id="0ed6e-132">Nota: El uso de `curl` podría ser preferible si tienes que invocar o crear scripts de pasos de descarga con el shell de Cmd o los scripts `.bat` / `.cmd`.</span><span class="sxs-lookup"><span data-stu-id="0ed6e-132">Note: Using `curl` might be preferable if you have to invoke/script download steps using Cmd shell and/or `.bat` / `.cmd` scripts.</span></span>

## <a name="installing-your-distro"></a><span data-ttu-id="0ed6e-133">Instalación de la distribución</span><span class="sxs-lookup"><span data-stu-id="0ed6e-133">Installing your distro</span></span>
<span data-ttu-id="0ed6e-134">Si usas Windows 10, puedes instalar la distribución con PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0ed6e-134">If you're using Windows 10 you can install your distro with PowerShell.</span></span> <span data-ttu-id="0ed6e-135">Solo tienes que ir a la carpeta que contiene la distribución descargada de arriba y, en ese directorio, ejecutar el siguiente comando, donde `app_name` es el nombre del archivo .appx de la distribución.</span><span class="sxs-lookup"><span data-stu-id="0ed6e-135">Simply navigate to folder containing the distro downloaded from above, and in that directory run the following command where `app_name` is the name of your distro .appx file.</span></span>  
```Powershell
Add-AppxPackage .\app_name.appx
```

<span data-ttu-id="0ed6e-136">Si usas Windows Server, puedes encontrar las instrucciones de instalación en la página de documentación de [Windows Server](install-on-server.md).</span><span class="sxs-lookup"><span data-stu-id="0ed6e-136">If you are using Windows server you can find the install instructions on the [Windows Server](install-on-server.md) documentation page.</span></span>

<span data-ttu-id="0ed6e-137">Una vez instalada la distribución, consulta la página de [pasos de inicialización](initialize-distro.md) para inicializar la nueva distribución.</span><span class="sxs-lookup"><span data-stu-id="0ed6e-137">Once your distro is installed please refer to the [Initialization Steps](initialize-distro.md) page to initialize your new distro.</span></span>
