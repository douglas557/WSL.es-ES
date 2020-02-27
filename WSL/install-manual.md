---
title: Descargar manualmente el subsistema de Windows para Linux (WSL) distribuciones
description: Instrucciones sobre cómo descargar manualmente el subsistema de Windows para distribuciones de Linux.
keywords: BashOnWindows, bash, WSL, Windows, subsistema de Windows para Linux, WSL, subsistema de Windows, distribución, Ubuntu, openSUSE, SLES, Debian, Kali
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: aa0b42748115045105bb4e6eae91493bfee11d09
ms.sourcegitcommit: 467b6c8e9716d1a60dbf9f7658fd9579da365b58
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/26/2020
ms.locfileid: "77624929"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a><span data-ttu-id="6f395-104">Descargar manualmente el subsistema de Windows para paquetes distribución de Linux</span><span class="sxs-lookup"><span data-stu-id="6f395-104">Manually download Windows Subsystem for Linux distro packages</span></span>

<span data-ttu-id="6f395-105">Hay varios escenarios en los que es posible que no pueda (o desee) instalar WSL Linux distribuciones a través de la Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="6f395-105">There are several scenarios in which you may not be able (or want) to, install WSL Linux distros via the Microsoft Store.</span></span> <span data-ttu-id="6f395-106">En concreto, es posible que esté ejecutando una SKU de sistema operativo de escritorio de Windows Server o de mantenimiento a largo plazo (LTSC) que no admita Microsoft Store, o que sus administradores o directivas de red corporativa no permitan el uso de Microsoft Store en su entorno.</span><span class="sxs-lookup"><span data-stu-id="6f395-106">Specifically, you may be running a Windows Server or Long-Term Servicing (LTSC) desktop OS SKU that doesn't support Microsoft Store, or your corporate network policies and/or admins to not permit Microsoft Store usage in your environment.</span></span>

<span data-ttu-id="6f395-107">En estos casos, aunque WSL está disponible, ¿cómo se descarga e instala Linux distribuciones en WSL si no se puede acceder a la tienda?</span><span class="sxs-lookup"><span data-stu-id="6f395-107">In these cases, while WSL itself is available, how do you download and install Linux distros in WSL if you can't access the store?</span></span>

> <span data-ttu-id="6f395-108">Nota: los **entornos de Shell de línea de comandos, incluidos cmd, PowerShell y Linux/WSL distribuciones, no se pueden ejecutar en el modo Windows 10 S**.</span><span class="sxs-lookup"><span data-stu-id="6f395-108">Note: **Command-line shell environments including Cmd, PowerShell, and Linux/WSL distros are not permitted to run on Windows 10 S Mode**.</span></span> <span data-ttu-id="6f395-109">Esta restricción existe con el fin de garantizar la integridad y los objetivos de seguridad que ofrece el modo S: lea [esta entrada](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="6f395-109">This restriction exists in order to ensure the integrity and safety goals that S Mode delivers: Read [this post](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) for more information.</span></span>

## <a name="downloading-distros"></a><span data-ttu-id="6f395-110">Descarga de distribuciones</span><span class="sxs-lookup"><span data-stu-id="6f395-110">Downloading distros</span></span>

<span data-ttu-id="6f395-111">Si la aplicación Microsoft Store no está disponible, puede descargar e instalar manualmente Linux distribuciones haciendo clic en estos vínculos:</span><span class="sxs-lookup"><span data-stu-id="6f395-111">If the Microsoft Store app is not available, you can download and manually install Linux distros by clicking these links:</span></span>
<!-- * [Ubuntu 18.04](https://aka.ms/wsl-ubuntu-1804)
* [Ubuntu 18.04 ARM](https://aka.ms/wsl-ubuntu-1804-arm) -->
* <span data-ttu-id="6f395-112">Ubuntu 18,04</span><span class="sxs-lookup"><span data-stu-id="6f395-112">Ubuntu 18.04</span></span>
* <span data-ttu-id="6f395-113">ARM de Ubuntu 18,04</span><span class="sxs-lookup"><span data-stu-id="6f395-113">Ubuntu 18.04 ARM</span></span>
* [<span data-ttu-id="6f395-114">Ubuntu 16,04</span><span class="sxs-lookup"><span data-stu-id="6f395-114">Ubuntu 16.04</span></span>](https://aka.ms/wsl-ubuntu-1604)
* [<span data-ttu-id="6f395-115">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="6f395-115">Debian GNU/Linux</span></span>](https://aka.ms/wsl-debian-gnulinux)
* [<span data-ttu-id="6f395-116">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="6f395-116">Kali Linux</span></span>](https://aka.ms/wsl-kali-linux-new)
* [<span data-ttu-id="6f395-117">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="6f395-117">OpenSUSE Leap 42</span></span>](https://aka.ms/wsl-opensuse-42)
* [<span data-ttu-id="6f395-118">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="6f395-118">SUSE Linux Enterprise Server 12</span></span>](https://aka.ms/wsl-sles-12)
* [<span data-ttu-id="6f395-119">Fedora Remix for WSL</span><span class="sxs-lookup"><span data-stu-id="6f395-119">Fedora Remix for WSL</span></span>](https://github.com/WhitewaterFoundry/WSLFedoraRemix/releases/)

<span data-ttu-id="6f395-120">Esto hará que los paquetes de `<distro>.appx` se descarguen en una carpeta de su elección.</span><span class="sxs-lookup"><span data-stu-id="6f395-120">This will cause the `<distro>.appx` packages to download to a folder of your choosing.</span></span> <span data-ttu-id="6f395-121">Siga las [instrucciones de instalación](#installing-your-distro) para instalar los distribución descargados.</span><span class="sxs-lookup"><span data-stu-id="6f395-121">Follow the [installation instructions](#installing-your-distro) to install your downloaded distro(s).</span></span>

## <a name="downloading-distros-via-the-command-line"></a><span data-ttu-id="6f395-122">Descarga de distribuciones a través de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="6f395-122">Downloading distros via the command line</span></span>
<span data-ttu-id="6f395-123">Si lo prefiere, también puede descargar los distribución preferidos a través de la línea de comandos:</span><span class="sxs-lookup"><span data-stu-id="6f395-123">If you prefer, you can also download your preferred distro(s) via the command line:</span></span>

 ### <a name="download-using-powershell"></a><span data-ttu-id="6f395-124">Descargar con PowerShell</span><span class="sxs-lookup"><span data-stu-id="6f395-124">Download using PowerShell</span></span>
 <span data-ttu-id="6f395-125">Para descargar distribuciones con PowerShell, use el cmdlet [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) .</span><span class="sxs-lookup"><span data-stu-id="6f395-125">To download distros using PowerShell, use the [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) cmdlet.</span></span> <span data-ttu-id="6f395-126">A continuación se muestra una instrucción de ejemplo para descargar ubuntu 16,04.</span><span class="sxs-lookup"><span data-stu-id="6f395-126">Here's a sample instruction to download Ubuntu 16.04.</span></span>

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> <span data-ttu-id="6f395-127">Si la descarga tarda mucho tiempo, desactive la barra de progreso estableciendo `$ProgressPreference = 'SilentlyContinue'`</span><span class="sxs-lookup"><span data-stu-id="6f395-127">If the download is taking a long time, turn off the progress bar by setting `$ProgressPreference = 'SilentlyContinue'`</span></span>

### <a name="download-using-curl"></a><span data-ttu-id="6f395-128">Descargar mediante rizo</span><span class="sxs-lookup"><span data-stu-id="6f395-128">Download using curl</span></span>
<span data-ttu-id="6f395-129">La actualización de Spring 2018 de Windows 10 (o posterior) incluye la popular [utilidad de línea de comandos de rizo](https://curl.haxx.se/) con la que puede invocar solicitudes web (es decir, HTTP GET, post, Put, etc.) desde la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="6f395-129">Windows 10 Spring 2018 Update (or later) includes the popular [curl command-line utility](https://curl.haxx.se/) with which you can invoke web requests (i.e. HTTP GET, POST, PUT, etc. commands) from the command line.</span></span> <span data-ttu-id="6f395-130">Puede usar `curl.exe` para descargar el distribuciones anterior:</span><span class="sxs-lookup"><span data-stu-id="6f395-130">You can use `curl.exe` to download the above distros:</span></span>

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

<span data-ttu-id="6f395-131">En el ejemplo anterior, se ejecuta `curl.exe` (no solo `curl`) para asegurarse de que, en PowerShell, se invoca el ejecutable de rizo real, no el alias de rizo de PowerShell para [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6) .</span><span class="sxs-lookup"><span data-stu-id="6f395-131">In the above example, `curl.exe` is executed (not just `curl`) to ensure that, in PowerShell, the real curl executable is invoked, not the PowerShell curl alias for [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)</span></span>

> <span data-ttu-id="6f395-132">Nota: el uso de `curl` podría ser preferible si tiene que invocar o crear scripts de pasos de descarga con el shell de CMD o `.bat` / scripts `.cmd`.</span><span class="sxs-lookup"><span data-stu-id="6f395-132">Note: Using `curl` might be preferable if you have to invoke/script download steps using Cmd shell and/or `.bat` / `.cmd` scripts.</span></span>

## <a name="installing-your-distro"></a><span data-ttu-id="6f395-133">Instalación de distribución</span><span class="sxs-lookup"><span data-stu-id="6f395-133">Installing your distro</span></span>
<span data-ttu-id="6f395-134">Si usa Windows 10, puede instalar el distribución con PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6f395-134">If you're using Windows 10 you can install your distro with PowerShell.</span></span> <span data-ttu-id="6f395-135">Simplemente vaya a la carpeta que contiene el distribución descargado de arriba y, en ese directorio, ejecute el siguiente comando, donde `app_name` es el nombre del archivo distribución. appx.</span><span class="sxs-lookup"><span data-stu-id="6f395-135">Simply navigate to folder containing the distro downloaded from above, and in that directory run the following command where `app_name` is the name of your distro .appx file.</span></span>  
```Powershell
Add-AppxPackage .\app_name.appx
```

<span data-ttu-id="6f395-136">Si usa Windows Server, puede encontrar las instrucciones de instalación en la página de documentación de [Windows Server](install-on-server.md) .</span><span class="sxs-lookup"><span data-stu-id="6f395-136">If you are using Windows server you can find the install instructions on the [Windows Server](install-on-server.md) documentation page.</span></span>

<span data-ttu-id="6f395-137">Una vez instalado el distribución, consulte la página [pasos de inicialización](initialize-distro.md) para inicializar el nuevo distribución.</span><span class="sxs-lookup"><span data-stu-id="6f395-137">Once your distro is installed please refer to the [Initialization Steps](initialize-distro.md) page to initialize your new distro.</span></span>
