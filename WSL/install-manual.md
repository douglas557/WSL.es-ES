---
title: Descargar manualmente el subsistema de Windows para las distribuciones de Linux (WSL)
description: Instrucciones sobre cómo descargar manualmente el subsistema de Windows para las distribuciones de Linux.
keywords: BashOnWindows, bash, wsl, windows, el subsistema de windows para linux, WSL, subsistema de windows, distribución, ubuntu, openSUSE, SLES, debian, kali
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: be1c1331183317d4f970696464110b9968208d21
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063573"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a><span data-ttu-id="aa8e6-104">Descargar manualmente el subsistema de Windows para los paquetes de distribución de Linux</span><span class="sxs-lookup"><span data-stu-id="aa8e6-104">Manually download Windows Subsystem for Linux distro packages</span></span>

<span data-ttu-id="aa8e6-105">Hay varios escenarios en los que puede no ser capaz de (o desee) para instalar las distribuciones de Linux de WSL a través de la Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="aa8e6-105">There are several scenarios in which you may not be able (or want) to, install WSL Linux distros via the Microsoft Store.</span></span> <span data-ttu-id="aa8e6-106">En concreto, puede que esté ejecutando un servidor de Windows o la SKU del sistema operativo que no es compatible con Microsoft Store, o sus directivas de red corporativa y/o los administradores para no permitir el uso de Microsoft Store en su entorno de escritorio de mantenimiento a largo plazo (LTSB/LTSC).</span><span class="sxs-lookup"><span data-stu-id="aa8e6-106">Specifically, you may be running a Windows Server or Long-Term Servicing (LTSB/LTSC) desktop OS SKU that doesn't support Microsoft Store, or your corporate network policies and/or admins to not permit Microsoft Store usage in your environment.</span></span>

<span data-ttu-id="aa8e6-107">En estos casos, mientras que WSL sí está disponible, ¿cómo descargar e instalar distribuciones de Linux en WSL si no se puede obtener acceso al almacén?</span><span class="sxs-lookup"><span data-stu-id="aa8e6-107">In these cases, while WSL itself is available, how do you download and install Linux distros in WSL if you can't access the store?</span></span>

> <span data-ttu-id="aa8e6-108">Nota: **Entornos de shell de línea de comandos, incluidos las distribuciones de Linux/WSL, Cmd y PowerShell no se pueden ejecutar en modo de Windows 10 S**.</span><span class="sxs-lookup"><span data-stu-id="aa8e6-108">Note: **Command-line shell environments including Cmd, PowerShell, and Linux/WSL distros are not permitted to run on Windows 10 S Mode**.</span></span> <span data-ttu-id="aa8e6-109">Esta restricción existe con el fin de garantizar los objetivos de integridad y seguridad que ofrece el modo S: Lectura [esta publicación](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="aa8e6-109">This restriction exists in order to ensure the integrity and safety goals that S Mode delivers: Read [this post](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) for more information.</span></span>

## <a name="downloading-distros"></a><span data-ttu-id="aa8e6-110">Descarga de distribuciones</span><span class="sxs-lookup"><span data-stu-id="aa8e6-110">Downloading distros</span></span>

<span data-ttu-id="aa8e6-111">Si la aplicación de Microsoft Store no está disponible, puede descargar e instalar manualmente las distribuciones de Linux, haga clic en estos vínculos:</span><span class="sxs-lookup"><span data-stu-id="aa8e6-111">If the Microsoft Store app is not available, you can download and manually install Linux distros by clicking these links:</span></span>
* [<span data-ttu-id="aa8e6-112">Ubuntu 18.04</span><span class="sxs-lookup"><span data-stu-id="aa8e6-112">Ubuntu 18.04</span></span>](https://aka.ms/wsl-ubuntu-1804)
* [<span data-ttu-id="aa8e6-113">Ubuntu 18.04 ARM</span><span class="sxs-lookup"><span data-stu-id="aa8e6-113">Ubuntu 18.04 ARM</span></span>](https://aka.ms/wsl-ubuntu-1804-arm)
* [<span data-ttu-id="aa8e6-114">Ubuntu 16.04</span><span class="sxs-lookup"><span data-stu-id="aa8e6-114">Ubuntu 16.04</span></span>](https://aka.ms/wsl-ubuntu-1604)
* [<span data-ttu-id="aa8e6-115">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="aa8e6-115">Debian GNU/Linux</span></span>](https://aka.ms/wsl-debian-gnulinux)
* [<span data-ttu-id="aa8e6-116">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="aa8e6-116">Kali Linux</span></span>](https://aka.ms/wsl-kali-linux)
* [<span data-ttu-id="aa8e6-117">OpenSUSE</span><span class="sxs-lookup"><span data-stu-id="aa8e6-117">OpenSUSE</span></span>](https://aka.ms/wsl-opensuse-42)
* [<span data-ttu-id="aa8e6-118">SLES</span><span class="sxs-lookup"><span data-stu-id="aa8e6-118">SLES</span></span>](https://aka.ms/wsl-sles-12)

<span data-ttu-id="aa8e6-119">Esto hará que el `<distro>.appx` paquetes para descargar en una carpeta de su elección.</span><span class="sxs-lookup"><span data-stu-id="aa8e6-119">This will cause the `<distro>.appx` packages to download to a folder of your choosing.</span></span> <span data-ttu-id="aa8e6-120">Siga el [las instrucciones de instalación](#installing-your-distro) para instalar su distro(s) descargado.</span><span class="sxs-lookup"><span data-stu-id="aa8e6-120">Follow the [installation instructions](#installing-your-distro) to install your downloaded distro(s).</span></span>

## <a name="downloading-distros-via-the-command-line"></a><span data-ttu-id="aa8e6-121">Distribuciones de descarga a través de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="aa8e6-121">Downloading distros via the command line</span></span>
<span data-ttu-id="aa8e6-122">Si lo prefiere, también puede descargar el distro(s) preferida a través de la línea de comandos:</span><span class="sxs-lookup"><span data-stu-id="aa8e6-122">If you prefer, you can also download your preferred distro(s) via the command line:</span></span>

 ### <a name="download-using-powershell"></a><span data-ttu-id="aa8e6-123">Descargar mediante PowerShell</span><span class="sxs-lookup"><span data-stu-id="aa8e6-123">Download using PowerShell</span></span>
 <span data-ttu-id="aa8e6-124">Para descargar las distribuciones con PowerShell, use el [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa8e6-124">To download distros using PowerShell, use the [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) cmdlet.</span></span> <span data-ttu-id="aa8e6-125">Aquí es una instrucción de ejemplo para descargar Ubuntu 16.04.</span><span class="sxs-lookup"><span data-stu-id="aa8e6-125">Here's a sample instruction to download Ubuntu 16.04.</span></span>

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> <span data-ttu-id="aa8e6-126">Si la descarga tarda mucho tiempo, desactive la barra de progreso estableciendo</span><span class="sxs-lookup"><span data-stu-id="aa8e6-126">If the download is taking a long time, turn off the progress bar by setting</span></span> `$ProgressPreference = 'SilentlyContinue'`

### <a name="download-using-curl"></a><span data-ttu-id="aa8e6-127">Descargar mediante curl</span><span class="sxs-lookup"><span data-stu-id="aa8e6-127">Download using curl</span></span>
<span data-ttu-id="aa8e6-128">Actualización de Windows 10 Spring 2018 (o posterior) incluye el popular [curl utilidad de línea de comandos](https://curl.haxx.se/) con el que puede invocar las solicitudes de web (es decir, HTTP GET, POST, PUT, comandos etc.) desde la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="aa8e6-128">Windows 10 Spring 2018 Update (or later) includes the popular [curl command-line utility](https://curl.haxx.se/) with which you can invoke web requests (i.e. HTTP GET, POST, PUT, etc. commands) from the command line.</span></span> <span data-ttu-id="aa8e6-129">Puede usar `curl.exe` para descargar las distribuciones anteriores:</span><span class="sxs-lookup"><span data-stu-id="aa8e6-129">You can use `curl.exe` to download the above distros:</span></span>

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

<span data-ttu-id="aa8e6-130">En el ejemplo anterior, `curl.exe` se ejecuta (no solo `curl`) garantizar que, en PowerShell, el archivo ejecutable de curl real se invoca, no la curl de PowerShell alias de [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)</span><span class="sxs-lookup"><span data-stu-id="aa8e6-130">In the above example, `curl.exe` is executed (not just `curl`) to ensure that, in PowerShell, the real curl executable is invoked, not the PowerShell curl alias for [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)</span></span>

> <span data-ttu-id="aa8e6-131">Nota: Uso de `curl` podría ser preferible si tiene que invocar comandos o mediante el shell de Cmd de pasos de descarga o `.bat`  /  `.cmd` secuencias de comandos.</span><span class="sxs-lookup"><span data-stu-id="aa8e6-131">Note: Using `curl` might be preferable if you have to invoke/script download steps using Cmd shell and/or `.bat` / `.cmd` scripts.</span></span>

## <a name="installing-your-distro"></a><span data-ttu-id="aa8e6-132">Instalación de la distribución</span><span class="sxs-lookup"><span data-stu-id="aa8e6-132">Installing your distro</span></span>
<span data-ttu-id="aa8e6-133">Para obtener instrucciones sobre cómo instalar su distro(s) descargado, consulte el [Windows Desktop](install-win10.md) o [Windows Server](install-on-server.md) instrucciones de instalación.</span><span class="sxs-lookup"><span data-stu-id="aa8e6-133">For instructions on how to install your downloaded distro(s), please refer to the [Windows Desktop](install-win10.md) or [Windows Server](install-on-server.md) installation instructions.</span></span>
