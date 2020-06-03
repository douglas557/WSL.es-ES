---
title: Instalar el Subsistema de Windows para Linux (WSL) en Windows 10
description: Instrucciones de instalación para el Subsistema de Windows para Linux en Windows 10.
keywords: BashOnWindows, bash, wsl, wsl2, windows, subsistema de windows para linux, windowssubsystem, ubuntu, debian, suse, windows 10, instalación
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 6ed12ba9d63d3f4038b67489035e13113a372928
ms.sourcegitcommit: 9f12e168b80775cd967f22f97376e51043c3667e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/02/2020
ms.locfileid: "84301206"
---
# <a name="install-windows-subsystem-for-linux"></a><span data-ttu-id="f1bdc-104">Instalación del Subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="f1bdc-104">Install Windows Subsystem for Linux</span></span>

<span data-ttu-id="f1bdc-105">La siguiente guía recorrerá los pasos necesarios para instalar el Subsistema de Windows para Linux (WSL) en un equipo que ejecuta Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f1bdc-105">The following guide will walk through the steps required to install the Windows Subsystem for Linux (WSL) on a computer running Windows 10.</span></span>

## <a name="enable-the-windows-subsystem-for-linux-optional-feature"></a><span data-ttu-id="f1bdc-106">Habilitación de la característica opcional Subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="f1bdc-106">Enable the Windows Subsystem for Linux optional feature</span></span>

<span data-ttu-id="f1bdc-107">Antes de instalar una distribución de Linux, debes habilitar la característica opcional "Subsistema de Windows para Linux" en Windows 10:</span><span class="sxs-lookup"><span data-stu-id="f1bdc-107">Before installing a Linux distribution, you must enable the "Windows Subsystem for Linux" optional feature on Windows 10:</span></span>

1. <span data-ttu-id="f1bdc-108">Abre PowerShell como administrador y escribe este script:</span><span class="sxs-lookup"><span data-stu-id="f1bdc-108">Open PowerShell as Administrator and enter this script:</span></span>

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

1. <span data-ttu-id="f1bdc-109">Reinicia el equipo cuando se te solicite.</span><span class="sxs-lookup"><span data-stu-id="f1bdc-109">Restart your computer when prompted.</span></span>

## <a name="install-a-linux-distribution"></a><span data-ttu-id="f1bdc-110">Instalación de una distribución de Linux</span><span class="sxs-lookup"><span data-stu-id="f1bdc-110">Install a Linux distribution</span></span>

<span data-ttu-id="f1bdc-111">Existen tres maneras de descargar e instalar tus distribuciones de Linux preferidas:</span><span class="sxs-lookup"><span data-stu-id="f1bdc-111">There are three ways to download and install your preferred Linux distribution(s):</span></span>

- <span data-ttu-id="f1bdc-112">Descargarlas e instalarlas de Microsoft Store (ver la información que hay a continuación).</span><span class="sxs-lookup"><span data-stu-id="f1bdc-112">Download and install from the Microsoft Store (see below)</span></span>
- [<span data-ttu-id="f1bdc-113">Descargarlas e instalarlas manualmente desde la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="f1bdc-113">Download and manually install from command line</span></span>](install-manual.md)
- [<span data-ttu-id="f1bdc-114">Instalar en Windows Server</span><span class="sxs-lookup"><span data-stu-id="f1bdc-114">Install on Windows Server</span></span>](install-on-server.md)

### <a name="install-from-the-microsoft-store"></a><span data-ttu-id="f1bdc-115">Descargar desde Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="f1bdc-115">Install from the Microsoft Store</span></span>

<span data-ttu-id="f1bdc-116">Las distribuciones de Linux se pueden instalar desde Microsoft Store en Windows 10 (compilación 16215 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="f1bdc-116">Linux distributions can be installed from the Microsoft Store on Windows 10 (Build 16215+).</span></span>

> [!NOTE]
> <span data-ttu-id="f1bdc-117">Sigue estos pasos para [comprobar el número de compilación de Windows 10](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="f1bdc-117">Follow these steps to [check your Windows 10 build number](troubleshooting.md#check-your-build-number).</span></span>

1. <span data-ttu-id="f1bdc-118">Abre Microsoft Store y elige tu distribución de Linux favorita.</span><span class="sxs-lookup"><span data-stu-id="f1bdc-118">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![Vista de las distribuciones de Linux en Microsoft Store](media/store.png)

    <span data-ttu-id="f1bdc-120">En los vínculos siguientes se abrirá la página de Microsoft Store para cada distribución:</span><span class="sxs-lookup"><span data-stu-id="f1bdc-120">The following links will open the Microsoft store page for each distribution:</span></span>

    - [<span data-ttu-id="f1bdc-121">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="f1bdc-121">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [<span data-ttu-id="f1bdc-122">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="f1bdc-122">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [<span data-ttu-id="f1bdc-123">OpenSUSE Leap 15</span><span class="sxs-lookup"><span data-stu-id="f1bdc-123">OpenSUSE Leap 15</span></span>](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    - [<span data-ttu-id="f1bdc-124">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="f1bdc-124">OpenSUSE Leap 42</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    - [<span data-ttu-id="f1bdc-125">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="f1bdc-125">SUSE Linux Enterprise Server 12</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    - [<span data-ttu-id="f1bdc-126">SUSE Linux Enterprise Server 15</span><span class="sxs-lookup"><span data-stu-id="f1bdc-126">SUSE Linux Enterprise Server 15</span></span>](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    - [<span data-ttu-id="f1bdc-127">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="f1bdc-127">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [<span data-ttu-id="f1bdc-128">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="f1bdc-128">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [<span data-ttu-id="f1bdc-129">Fedora Remix for WSL</span><span class="sxs-lookup"><span data-stu-id="f1bdc-129">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [<span data-ttu-id="f1bdc-130">Pengwin</span><span class="sxs-lookup"><span data-stu-id="f1bdc-130">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [<span data-ttu-id="f1bdc-131">Pengwin Enterprise</span><span class="sxs-lookup"><span data-stu-id="f1bdc-131">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [<span data-ttu-id="f1bdc-132">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="f1bdc-132">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

1. <span data-ttu-id="f1bdc-133">Selecciona "Obtener" y, una vez finalizada la descarga de la distribución, selecciona "Iniciar".</span><span class="sxs-lookup"><span data-stu-id="f1bdc-133">Select "Get" and once the distribution has finished downloading, select "Launch".</span></span>

    ![Vista de las distribuciones de Linux en Microsoft Store](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="f1bdc-135">Completar la inicialización de la distribución</span><span class="sxs-lookup"><span data-stu-id="f1bdc-135">Complete initialization of your distro</span></span>

<span data-ttu-id="f1bdc-136">Después de iniciar la distribución de Linux, sigue las instrucciones en pantalla para inicializarla.</span><span class="sxs-lookup"><span data-stu-id="f1bdc-136">After launching your Linux distribution, follow the onscreen instructions to initialize your distro.</span></span>

> [!NOTE]
> <span data-ttu-id="f1bdc-137">En Windows Server, inicia la distribución mediante el archivo ejecutable (`<distro>.exe`) en la carpeta de instalación.</span><span class="sxs-lookup"><span data-stu-id="f1bdc-137">For Windows Server, launch your distribution using the executable, `<distro>.exe`, in the installation folder.</span></span>

<span data-ttu-id="f1bdc-138">La primera vez que se ejecute una distribución recién instalada, se abrirá una ventana de consola y se te pedirá que esperes un minuto o dos para que se complete la instalación.</span><span class="sxs-lookup"><span data-stu-id="f1bdc-138">The first time a newly installed distribution runs, a console window will open and you'll be asked to wait for a minute or two for the installation to complete.</span></span> <span data-ttu-id="f1bdc-139">Durante esta fase final de la instalación, los archivos de la distribución se descomprimen y almacenan en el equipo, listos para usarse.</span><span class="sxs-lookup"><span data-stu-id="f1bdc-139">During this final stage of installation, the distro's files are de-compressed and stored on your PC, ready for use.</span></span> <span data-ttu-id="f1bdc-140">Esta acción puede tardar aproximadamente un minuto o más en función del rendimiento de los dispositivos de almacenamiento del equipo.</span><span class="sxs-lookup"><span data-stu-id="f1bdc-140">This may take around a minute or more depending on the performance of your PC's storage devices.</span></span> <span data-ttu-id="f1bdc-141">Esta fase de instalación inicial solo es necesaria cuando una distribución se instala sin problemas; todos los inicios futuros deben tardar menos de un segundo.</span><span class="sxs-lookup"><span data-stu-id="f1bdc-141">This initial installation phase is only required when a distro is clean-installed - all future launches should take less than a second.</span></span>

## <a name="set-up-a-new-linux-user-account"></a><span data-ttu-id="f1bdc-142">Configuración de una nueva cuenta de usuario de Linux</span><span class="sxs-lookup"><span data-stu-id="f1bdc-142">Set up a new Linux user account</span></span>

<span data-ttu-id="f1bdc-143">Una vez completada la instalación, se te pedirá que crees una nueva cuenta de usuario (y su contraseña).</span><span class="sxs-lookup"><span data-stu-id="f1bdc-143">Once installation is complete, you will be prompted to create a new user account (and its password).</span></span>

![Desempaquetado de Ubuntu en la consola de Windows](media/UbuntuInstall.png)

<span data-ttu-id="f1bdc-145">Esta cuenta de usuario es para el usuario normal sin privilegios de administrador con el que se iniciará sesión de manera predeterminada al iniciar una distribución.</span><span class="sxs-lookup"><span data-stu-id="f1bdc-145">This user account is for the normal non-admin user that you'll be logged-in as by default when launching a distribution.</span></span> <span data-ttu-id="f1bdc-146">Puedes elegir cualquier nombre de usuario y contraseña: no tienen ninguna relación con el nombre de usuario de Windows.</span><span class="sxs-lookup"><span data-stu-id="f1bdc-146">You can choose any username and password you wish - they have no bearing on your Windows username.</span></span>

<span data-ttu-id="f1bdc-147">Cuando abras una nueva instancia de distribución, no se te pedirá la contraseña, pero, **si elevas un proceso mediante `sudo`, tendrás que escribir la contraseña**, por lo que debes asegurarte de elegir una contraseña que puedas recordar fácilmente.</span><span class="sxs-lookup"><span data-stu-id="f1bdc-147">When you open a new distro instance, you won't be prompted for your password, but **if you elevate a process using `sudo`, you will need to enter your password**, so make sure you choose a password you can easily remember!</span></span> <span data-ttu-id="f1bdc-148">Para obtener más información, consulta la página de [Soporte del usuario](user-support.md).</span><span class="sxs-lookup"><span data-stu-id="f1bdc-148">See the [User Support](user-support.md) page for more info.</span></span>

## <a name="update--upgrade-packages"></a><span data-ttu-id="f1bdc-149">Actualización de paquetes</span><span class="sxs-lookup"><span data-stu-id="f1bdc-149">Update & upgrade packages</span></span>

<span data-ttu-id="f1bdc-150">La mayoría de las distribuciones incluyen un catálogo de paquetes vacío o mínimo.</span><span class="sxs-lookup"><span data-stu-id="f1bdc-150">Most distributions ship with an empty or minimal package catalog.</span></span> <span data-ttu-id="f1bdc-151">Se recomienda encarecidamente actualizar periódicamente el catálogo de paquetes, así como actualizar los paquetes instalados con tu administrador de paquetes preferido de la distribución.</span><span class="sxs-lookup"><span data-stu-id="f1bdc-151">We strongly recommend regularly updating your package catalog and upgrading your installed packages using your distro's preferred package manager.</span></span> <span data-ttu-id="f1bdc-152">Para Debian y Ubuntu, usa apt:</span><span class="sxs-lookup"><span data-stu-id="f1bdc-152">For Debian/Ubuntu, use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

<span data-ttu-id="f1bdc-153">Windows no actualiza automáticamente las distribuciones de Linux.</span><span class="sxs-lookup"><span data-stu-id="f1bdc-153">Windows does not automatically update or upgrade your Linux distro(s).</span></span> <span data-ttu-id="f1bdc-154">Se trata de una tarea que la mayoría de los usuarios de Linux prefieren controlar por sí mismos.</span><span class="sxs-lookup"><span data-stu-id="f1bdc-154">This is a task that the most Linux users prefer to control themselves.</span></span>

<span data-ttu-id="f1bdc-155">Disfruta con la nueva distribución de Linux en WSL.</span><span class="sxs-lookup"><span data-stu-id="f1bdc-155">Enjoy using your new Linux distro on WSL!</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="f1bdc-156">Solucionar problemas</span><span class="sxs-lookup"><span data-stu-id="f1bdc-156">Troubleshooting</span></span>

<span data-ttu-id="f1bdc-157">A continuación, se muestran errores de instalación relacionados y las correcciones sugeridas.</span><span class="sxs-lookup"><span data-stu-id="f1bdc-157">Below are related installation errors and suggested fixes.</span></span> <span data-ttu-id="f1bdc-158">Consulta la [página de solución de problemas de WSL](troubleshooting.md) para ver otros errores generales y sus soluciones.</span><span class="sxs-lookup"><span data-stu-id="f1bdc-158">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

### <a name="installation-failed-with-error-0x8007007e"></a><span data-ttu-id="f1bdc-159">Error 0x8007007e en la instalación</span><span class="sxs-lookup"><span data-stu-id="f1bdc-159">Installation failed with error 0x8007007e</span></span>

<span data-ttu-id="f1bdc-160">Este error se produce cuando el sistema no es compatible con Linux de Store.</span><span class="sxs-lookup"><span data-stu-id="f1bdc-160">This error occurs when your system doesn't support Linux from the store.</span></span>  <span data-ttu-id="f1bdc-161">Asegúrese de que:</span><span class="sxs-lookup"><span data-stu-id="f1bdc-161">Make sure that:</span></span>

- <span data-ttu-id="f1bdc-162">Estás ejecutando la compilación 16215 de Windows o una posterior.</span><span class="sxs-lookup"><span data-stu-id="f1bdc-162">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="f1bdc-163">[Comprueba el número de compilación](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="f1bdc-163">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
- <span data-ttu-id="f1bdc-164">El componente opcional del subsistema de Windows para Linux está habilitado y se ha reiniciado el equipo.</span><span class="sxs-lookup"><span data-stu-id="f1bdc-164">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="f1bdc-165">[Asegúrate de que WSL está habilitado](troubleshooting.md#confirm-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="f1bdc-165">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>

### <a name="installation-failed-with-error-0x80070003"></a><span data-ttu-id="f1bdc-166">Error 0x80070003 en la instalación</span><span class="sxs-lookup"><span data-stu-id="f1bdc-166">Installation failed with error 0x80070003</span></span>

<span data-ttu-id="f1bdc-167">El Subsistema de Windows para Linux solo se ejecuta en la unidad del sistema (normalmente se trata de la unidad `C:`).</span><span class="sxs-lookup"><span data-stu-id="f1bdc-167">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="f1bdc-168">Asegúrate de que las distribuciones se almacenan en la unidad del sistema:</span><span class="sxs-lookup"><span data-stu-id="f1bdc-168">Make sure that distros are stored on your system drive:</span></span>

- <span data-ttu-id="f1bdc-169">Abre **Configuración** -> **Almacenamiento** -> **Más opciones de almacenamiento: Cambia la ubicación en que se guarda el nuevo contenido**</span><span class="sxs-lookup"><span data-stu-id="f1bdc-169">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**</span></span>
  
    ![Imagen de la configuración del sistema para instalar aplicaciones en la unidad C:](media/AppStorage.png)

### <a name="wslregisterdistribution-failed-with-error-0x8007019e"></a><span data-ttu-id="f1bdc-171">Error 0x8007019e de WslRegisterDistribution</span><span class="sxs-lookup"><span data-stu-id="f1bdc-171">WslRegisterDistribution failed with error 0x8007019e</span></span>

<span data-ttu-id="f1bdc-172">El componente opcional del Subsistema de Windows para Linux no está habilitado:</span><span class="sxs-lookup"><span data-stu-id="f1bdc-172">The Windows Subsystem for Linux optional component is not enabled:</span></span>

- <span data-ttu-id="f1bdc-173">Abre el **Panel de control** -> **Programas y características** -> **Activa o desactiva la característica de Windows** -> Selecciona el **Subsistema de Windows para Linux** o usa el cmdlet de PowerShell mencionado al comienzo de este artículo.</span><span class="sxs-lookup"><span data-stu-id="f1bdc-173">Open **Control Panel** -> **Programs and Features** -> **Turn Windows Feature on or off** -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the begining of this article.</span></span>
