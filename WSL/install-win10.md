---
title: Instalar el Subsistema de Windows para Linux (WSL) en Windows 10
description: Instrucciones de instalación para el Subsistema de Windows para Linux en Windows 10.
keywords: BashOnWindows, bash, wsl, wsl2, windows, subsistema de windows para linux, subsistemawindows, ubuntu, debian, suse, windows 10, instalación, instalar, habilitación, habilitar, WSL2, versión 2
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 0f59fda8aa093487f09c1817acf47bd88eaae8cc
ms.sourcegitcommit: f1b049a1276782d4f2754f46a8d2025b598a0784
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/24/2020
ms.locfileid: "85336098"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="057b5-104">Guía de instalación del Subsistema de Windows para Linux para Windows 10</span><span class="sxs-lookup"><span data-stu-id="057b5-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="057b5-105">Instalar el Subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="057b5-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="057b5-106">Antes de instalar distribuciones de Linux en Windows, debes habilitar la característica opcional "Subsistema de Windows para Linux".</span><span class="sxs-lookup"><span data-stu-id="057b5-106">Before installing any Linux distributions on Windows, you must enable the "Windows Subsystem for Linux" optional feature.</span></span>

<span data-ttu-id="057b5-107">Abre PowerShell como administrador y ejecuta:</span><span class="sxs-lookup"><span data-stu-id="057b5-107">Open PowerShell as Administrator and run:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

<span data-ttu-id="057b5-108">Para instalar solo WSL 1, debes reiniciar la máquina ahora y pasar a la sección [Instalación de la distribución de Linux que quieras](./install-win10.md#install-your-linux-distribution-of-choice). De lo contrario, espera a que se reinicie y avanza para actualizar a WSL 2.</span><span class="sxs-lookup"><span data-stu-id="057b5-108">To only install WSL 1, you should now restart your machine and move on to [Install your Linux distribution of choice](./install-win10.md#install-your-linux-distribution-of-choice), otherwise wait to restart and move on to update to WSL 2.</span></span> <span data-ttu-id="057b5-109">Obtén más información sobre la [Comparación de WSL 2 con WSL 1](./compare-versions.md).</span><span class="sxs-lookup"><span data-stu-id="057b5-109">Read more about [Comparing WSL 2 and WSL 1](./compare-versions.md).</span></span>

## <a name="update-to-wsl-2"></a><span data-ttu-id="057b5-110">Actualización a WSL 2</span><span class="sxs-lookup"><span data-stu-id="057b5-110">Update to WSL 2</span></span>

<span data-ttu-id="057b5-111">Para actualizar a WSL 2, debe cumplir los siguientes criterios:</span><span class="sxs-lookup"><span data-stu-id="057b5-111">To update to WSL 2, you must meet the following criteria:</span></span>

- <span data-ttu-id="057b5-112">Ejecutar Windows 10, [actualizado a la versión 2004](ms-settings:windowsupdate), **compilación 19041** o posterior.</span><span class="sxs-lookup"><span data-stu-id="057b5-112">Running Windows 10, [updated to version 2004](ms-settings:windowsupdate), **Build 19041** or higher.</span></span>

- <span data-ttu-id="057b5-113">Para comprobar la versión de Windows, selecciona la **tecla del logotipo de Windows + R**, escribe **winver** y selecciona **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="057b5-113">Check your Windows version by selecting the **Windows logo key + R**, type **winver**, select **OK**.</span></span> <span data-ttu-id="057b5-114">(También puedes escribir el comando `ver` en el símbolo del sistema de Windows).</span><span class="sxs-lookup"><span data-stu-id="057b5-114">(Or enter the `ver` command in Windows Command Prompt).</span></span> <span data-ttu-id="057b5-115">[Actualiza a la versión más reciente de Windows](ms-settings:windowsupdate) si la compilación es anterior a la 19041.</span><span class="sxs-lookup"><span data-stu-id="057b5-115">Please [update to the latest Windows version](ms-settings:windowsupdate) if your build is lower than 19041.</span></span> <span data-ttu-id="057b5-116">[Obtén el Asistente de Windows Update](https://www.microsoft.com/software-download/windows10).</span><span class="sxs-lookup"><span data-stu-id="057b5-116">[Get Windows Update Assistant](https://www.microsoft.com/software-download/windows10).</span></span>

### <a name="enable-the-virtual-machine-platform-optional-component"></a><span data-ttu-id="057b5-117">Habilitación del componente opcional "Plataforma de máquina virtual"</span><span class="sxs-lookup"><span data-stu-id="057b5-117">Enable the 'Virtual Machine Platform' optional component</span></span>

<span data-ttu-id="057b5-118">Antes de instalar WSL 2, tienes que habilitar la característica opcional "Plataforma de máquina virtual".</span><span class="sxs-lookup"><span data-stu-id="057b5-118">Before installing WSL 2, you must enable the "Virtual Machine Platform" optional feature.</span></span>

<span data-ttu-id="057b5-119">Abre PowerShell como administrador y ejecuta:</span><span class="sxs-lookup"><span data-stu-id="057b5-119">Open PowerShell as Administrator and run:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

<span data-ttu-id="057b5-120">**Reinicia** la máquina para completar la instalación de WSL y la actualización a WSL 2.</span><span class="sxs-lookup"><span data-stu-id="057b5-120">**Restart** your machine to complete the WSL install and update to WSL 2.</span></span>

### <a name="set-wsl-2-as-your-default-version"></a><span data-ttu-id="057b5-121">Definición de WSL 2 como versión predeterminada</span><span class="sxs-lookup"><span data-stu-id="057b5-121">Set WSL 2 as your default version</span></span>

<span data-ttu-id="057b5-122">Ejecute el siguiente comando en PowerShell para establecer WSL 2 como versión predeterminada al instalar una nueva distribución de Linux:</span><span class="sxs-lookup"><span data-stu-id="057b5-122">Run the following command in PowerShell to set WSL 2 as the default version when installing a new Linux distribution:</span></span>

```powershell
wsl --set-default-version 2
```

<span data-ttu-id="057b5-123">Es posible que vea este mensaje después de ejecutar el comando: `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`.</span><span class="sxs-lookup"><span data-stu-id="057b5-123">You might see this message after running that command: `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`.</span></span> <span data-ttu-id="057b5-124">Siga el vínculo ([https://aka.ms/wsl2kernel](https://aka.ms/wsl2kernel)) e instale MSI desde esa página en nuestra documentación para instalar un kernel de Linux en la máquina para que lo use WSL 2.</span><span class="sxs-lookup"><span data-stu-id="057b5-124">Please follow the link ([https://aka.ms/wsl2kernel](https://aka.ms/wsl2kernel)) and install the MSI from that page on our documentation to install a Linux kernel on your machine for WSL 2 to use.</span></span> <span data-ttu-id="057b5-125">Una vez instalado el kernel, vuelva a ejecutar el comando, que debería completarse correctamente sin mostrar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="057b5-125">Once you have the kernel installed, please run the command again and it should complete successfully without showing the message.</span></span> 

> [!NOTE]
> <span data-ttu-id="057b5-126">La actualización de WSL 1 a WSL 2 puede tardar varios minutos en completarse, en función del tamaño de la distribución de destino.</span><span class="sxs-lookup"><span data-stu-id="057b5-126">The update from WSL 1 to WSL 2 may take several minutes to complete depending on the size of your targeted distribution.</span></span> <span data-ttu-id="057b5-127">Si ejecuta una instalación anterior (heredada) de WSL 1 de la Actualización de aniversario de Windows 10 o de Creators Update, es posible que se produzca un error de actualización.</span><span class="sxs-lookup"><span data-stu-id="057b5-127">If you are running an older (legacy) installation of WSL 1 from Windows 10 Anniversary Update or Creators Update, you may encounter an update error.</span></span> <span data-ttu-id="057b5-128">Siga estas instrucciones para [desinstalar y quitar las distribuciones heredadas](https://docs.microsoft.com/windows/wsl/install-legacy#uninstallingremoving-the-legacy-distro).</span><span class="sxs-lookup"><span data-stu-id="057b5-128">Follow these instructions to [uninstall and remove any legacy distributions](https://docs.microsoft.com/windows/wsl/install-legacy#uninstallingremoving-the-legacy-distro).</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="057b5-129">Instalación de la distribución de Linux que quieras</span><span class="sxs-lookup"><span data-stu-id="057b5-129">Install your Linux distribution of choice</span></span>

1. <span data-ttu-id="057b5-130">Abre [Microsoft Store](https://aka.ms/wslstore) y selecciona tu distribución de Linux favorita.</span><span class="sxs-lookup"><span data-stu-id="057b5-130">Open the [Microsoft Store](https://aka.ms/wslstore) and select your favorite Linux distribution.</span></span>

    ![Vista de las distribuciones de Linux en Microsoft Store](media/store.png)

    <span data-ttu-id="057b5-132">En los vínculos siguientes se abrirá la página de Microsoft Store para cada distribución:</span><span class="sxs-lookup"><span data-stu-id="057b5-132">The following links will open the Microsoft store page for each distribution:</span></span>

    - [<span data-ttu-id="057b5-133">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="057b5-133">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [<span data-ttu-id="057b5-134">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="057b5-134">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [<span data-ttu-id="057b5-135">Ubuntu 20.04 LTS</span><span class="sxs-lookup"><span data-stu-id="057b5-135">Ubuntu 20.04 LTS</span></span>](https://www.microsoft.com/store/apps/9n6svws3rx71)
    - [<span data-ttu-id="057b5-136">OpenSUSE Leap 15.1</span><span class="sxs-lookup"><span data-stu-id="057b5-136">openSUSE Leap 15.1</span></span>](https://www.microsoft.com/store/apps/9NJFZK00FGKV)
    - [<span data-ttu-id="057b5-137">SUSE Linux Enterprise Server 12 SP5</span><span class="sxs-lookup"><span data-stu-id="057b5-137">SUSE Linux Enterprise Server 12 SP5</span></span>](https://www.microsoft.com/store/apps/9MZ3D1TRP8T1)
    - [<span data-ttu-id="057b5-138">SUSE Linux Enterprise Server 15 SP1</span><span class="sxs-lookup"><span data-stu-id="057b5-138">SUSE Linux Enterprise Server 15 SP1</span></span>](https://www.microsoft.com/store/apps/9PN498VPMF3Z)
    - [<span data-ttu-id="057b5-139">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="057b5-139">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [<span data-ttu-id="057b5-140">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="057b5-140">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [<span data-ttu-id="057b5-141">Fedora Remix for WSL</span><span class="sxs-lookup"><span data-stu-id="057b5-141">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [<span data-ttu-id="057b5-142">Pengwin</span><span class="sxs-lookup"><span data-stu-id="057b5-142">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [<span data-ttu-id="057b5-143">Pengwin Enterprise</span><span class="sxs-lookup"><span data-stu-id="057b5-143">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [<span data-ttu-id="057b5-144">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="057b5-144">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

2. <span data-ttu-id="057b5-145">En la página de la distribución, selecciona "Obtener".</span><span class="sxs-lookup"><span data-stu-id="057b5-145">From the distribution's page, select "Get".</span></span>

    ![Distribuciones de Linux en Microsoft Store](media/UbuntuStore.png)

## <a name="set-up-a-new-distribution"></a><span data-ttu-id="057b5-147">Configuración de una nueva distribución</span><span class="sxs-lookup"><span data-stu-id="057b5-147">Set up a new distribution</span></span>

<span data-ttu-id="057b5-148">La primera vez que inicies una distribución de Linux recién instalada, se abrirá una ventana de la consola y se te pedirá que esperes un minuto o dos para que los archivos se descompriman y se almacenen en tu equipo.</span><span class="sxs-lookup"><span data-stu-id="057b5-148">The first time you launch a newly installed Linux distribution, a console window will open and you'll be asked to wait for a minute or two for files to de-compress and be stored on your PC.</span></span> <span data-ttu-id="057b5-149">Todos los inicios posteriores deberían tardar menos de un segundo en completarse.</span><span class="sxs-lookup"><span data-stu-id="057b5-149">All future launches should take less than a second.</span></span>

<span data-ttu-id="057b5-150">Tendrás que [crear una cuenta de usuario y una contraseña para la nueva distribución de Linux](./user-support.md).</span><span class="sxs-lookup"><span data-stu-id="057b5-150">You will then need to [create a user account and password for your new Linux distribution](./user-support.md).</span></span>

![Desempaquetado de Ubuntu en la consola de Windows](media/UbuntuInstall.png)

## <a name="set-your-distribution-version-to-wsl-1-or-wsl-2"></a><span data-ttu-id="057b5-152">Definición de la versión de la distribución en WSL 1 o WSL 2</span><span class="sxs-lookup"><span data-stu-id="057b5-152">Set your distribution version to WSL 1 or WSL 2</span></span>

<span data-ttu-id="057b5-153">Para comprobar la versión de WSL asignada a cada una de las distribuciones de Linux que tienes instaladas, abre la línea de comandos de PowerShell y escribe el comando (solo disponible en [Windows, compilación 19041 o posterior](ms-settings:windowsupdate)) `wsl -l -v`.</span><span class="sxs-lookup"><span data-stu-id="057b5-153">You can check the WSL version assigned to each of the Linux distributions you have installed by opening the PowerShell command line and entering the command (only available in [Windows Build 19041 or higher](ms-settings:windowsupdate)): `wsl -l -v`</span></span>

```powershell
wsl --list --verbose
```

<span data-ttu-id="057b5-154">Para establecer que una distribución esté respaldada por una de las dos versiones de WSL, ejecuta:</span><span class="sxs-lookup"><span data-stu-id="057b5-154">To set a distribution to be backed by either version of WSL please run:</span></span>

```powershell
wsl --set-version <distribution name> <versionNumber>
```

<span data-ttu-id="057b5-155">Asegúrate de reemplazar `<distribution name>` por el nombre real de tu distribución, y `<versionNumber>` por el número "1" o "2".</span><span class="sxs-lookup"><span data-stu-id="057b5-155">Make sure to replace `<distribution name>` with the actual name of your distribution and `<versionNumber>` with the number '1' or '2'.</span></span> <span data-ttu-id="057b5-156">Puedes volver a cambiar a WSL 1 en cualquier momento; para ello, ejecuta el mismo comando que antes, pero reemplaza "2" por "1".</span><span class="sxs-lookup"><span data-stu-id="057b5-156">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="057b5-157">Además, si quieres que WSL 2 sea la arquitectura predeterminada, puedes hacerlo con este comando:</span><span class="sxs-lookup"><span data-stu-id="057b5-157">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

```powershell
wsl --set-default-version 2
```

<span data-ttu-id="057b5-158">De este modo, se establecerá la versión de cualquier nueva distribución instalada en WSL 2.</span><span class="sxs-lookup"><span data-stu-id="057b5-158">This will set the version of any new distribution installed to WSL 2.</span></span>

## <a name="troubleshooting-installation"></a><span data-ttu-id="057b5-159">Solución de problemas de instalación</span><span class="sxs-lookup"><span data-stu-id="057b5-159">Troubleshooting installation</span></span>

<span data-ttu-id="057b5-160">A continuación, se muestran errores relacionados y las correcciones sugeridas.</span><span class="sxs-lookup"><span data-stu-id="057b5-160">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="057b5-161">Consulta la [página de solución de problemas de WSL](troubleshooting.md) para ver otros errores generales y sus soluciones.</span><span class="sxs-lookup"><span data-stu-id="057b5-161">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

- <span data-ttu-id="057b5-162">**Error 0x80070003 en la instalación**</span><span class="sxs-lookup"><span data-stu-id="057b5-162">**Installation failed with error 0x80070003**</span></span>
  - <span data-ttu-id="057b5-163">El Subsistema de Windows para Linux solo se ejecuta en la unidad del sistema (normalmente se trata de la unidad `C:`).</span><span class="sxs-lookup"><span data-stu-id="057b5-163">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="057b5-164">Asegúrate de que las distribuciones estén almacenadas en la unidad del sistema:</span><span class="sxs-lookup"><span data-stu-id="057b5-164">Make sure that distributions are stored on your system drive:</span></span>  
  - <span data-ttu-id="057b5-165">Abre **Configuración** -> **Almacenamiento** -> **Más opciones de almacenamiento: Cambia el lugar donde se guarda el nuevo contenido**
    ![Imagen de la configuración del sistema para instalar aplicaciones en la unidad C:](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="057b5-165">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>

- <span data-ttu-id="057b5-166">**Error 0x8007019e de WslRegisterDistribution**</span><span class="sxs-lookup"><span data-stu-id="057b5-166">**WslRegisterDistribution failed with error 0x8007019e**</span></span>
  - <span data-ttu-id="057b5-167">El componente opcional del Subsistema de Windows para Linux no está habilitado:</span><span class="sxs-lookup"><span data-stu-id="057b5-167">The Windows Subsystem for Linux optional component is not enabled:</span></span>
  - <span data-ttu-id="057b5-168">Abre el **Panel de control** -> **Programas y características** -> **Activa o desactiva la característica de Windows** -> Selecciona **Subsistema de Windows para Linux** o usa el cmdlet de PowerShell mencionado al comienzo de este artículo.</span><span class="sxs-lookup"><span data-stu-id="057b5-168">Open **Control Panel** -> **Programs and Features** -> **Turn Windows Feature on or off** -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the beginning of this article.</span></span>

- <span data-ttu-id="057b5-169">**Error en la instalación 0x80070003 o 0x80370102**</span><span class="sxs-lookup"><span data-stu-id="057b5-169">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
  - <span data-ttu-id="057b5-170">Asegúrate de que la virtualización está habilitada dentro del BIOS del equipo.</span><span class="sxs-lookup"><span data-stu-id="057b5-170">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="057b5-171">Las instrucciones sobre cómo hacerlo variarán de un equipo a otro y lo más probable es que esta característica esté en opciones relacionadas con la CPU.</span><span class="sxs-lookup"><span data-stu-id="057b5-171">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>

- <span data-ttu-id="057b5-172">**Error al intentar actualizar: `Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="057b5-172">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
  - <span data-ttu-id="057b5-173">Asegúrate de que tienes el Subsistema de Windows para Linux habilitado y de que estás usando la compilación 19041 de Windows o posterior.</span><span class="sxs-lookup"><span data-stu-id="057b5-173">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 19041 or higher.</span></span> <span data-ttu-id="057b5-174">Para habilitar WSL, ejecute este comando en un símbolo del sistema de PowerShell con privilegios de administrador: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span><span class="sxs-lookup"><span data-stu-id="057b5-174">To enable WSL run this command in a PowerShell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="057b5-175">Puedes encontrar las instrucciones de instalación de WSL completas [aquí](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="057b5-175">You can find the full WSL install instructions [here](./install-win10.md).</span></span>

- <span data-ttu-id="057b5-176">**La operación solicitada no se pudo completar debido a una limitación del sistema de disco virtual. Los archivos de disco duro virtual deben estar sin comprimir y sin cifrar y no deben ser dispersos.**</span><span class="sxs-lookup"><span data-stu-id="057b5-176">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span></span>
  - <span data-ttu-id="057b5-177">Consulte el [subproceso #4103 sobre WSL en GitHub](https://github.com/microsoft/WSL/issues/4103), en el que se realiza el seguimiento de este problema para obtener información actualizada.</span><span class="sxs-lookup"><span data-stu-id="057b5-177">Please check [WSL GitHub thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span></span>

- <span data-ttu-id="057b5-178">**El término 'wsl' no se reconoce como nombre de cmdlet, función, archivo de script o programa ejecutable.**</span><span class="sxs-lookup"><span data-stu-id="057b5-178">**The term 'wsl' is not recognized as the name of a cmdlet, function, script file, or operable program.**</span></span>
  - <span data-ttu-id="057b5-179">Asegúrate de que el [componente opcional del Subsistema de Windows para Linux esté instalado](./install-win10.md#enable-the-virtual-machine-platform-optional-component).</span><span class="sxs-lookup"><span data-stu-id="057b5-179">Ensure that the [Windows Subsystem for Linux Optional Component is installed](./install-win10.md#enable-the-virtual-machine-platform-optional-component).</span></span> <span data-ttu-id="057b5-180">Además, si usa un dispositivo ARM64 y ejecuta este comando desde PowerShell, recibirá este error.</span><span class="sxs-lookup"><span data-stu-id="057b5-180">Additionally, if you are using an ARM64 device and running this command from PowerShell, you will receive this error.</span></span> <span data-ttu-id="057b5-181">En su lugar, ejecuta `wsl.exe` desde [PowerShell Core](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6) o el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="057b5-181">Instead run `wsl.exe` from [PowerShell Core](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6), or Command Prompt.</span></span>
