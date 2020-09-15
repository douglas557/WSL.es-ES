---
title: Instalar el Subsistema de Windows para Linux (WSL) en Windows 10
description: Obtenga información sobre cómo instalar el Subsistema de Windows para Linux en Windows 10. Windows 10 debe actualizarse a la versión 2004, compilación 19041 o posterior.
keywords: BashOnWindows, bash, wsl, wsl2, windows, subsistema de windows para linux, subsistemawindows, ubuntu, debian, suse, windows 10, instalación, instalar, habilitación, habilitar, WSL2, versión 2
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 50b434e288ba90173875cf5e7cd5fe9e6c3d8a16
ms.sourcegitcommit: 498592fa4b09015be3ee9a8913e5e3cf755de24b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "89559295"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="00f82-105">Guía de instalación del Subsistema de Windows para Linux para Windows 10</span><span class="sxs-lookup"><span data-stu-id="00f82-105">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="00f82-106">Instalar el Subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="00f82-106">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="00f82-107">Antes de instalar distribuciones de Linux en Windows, debes habilitar la característica opcional "Subsistema de Windows para Linux".</span><span class="sxs-lookup"><span data-stu-id="00f82-107">Before installing any Linux distributions on Windows, you must enable the "Windows Subsystem for Linux" optional feature.</span></span>

<span data-ttu-id="00f82-108">Abre PowerShell como administrador y ejecuta:</span><span class="sxs-lookup"><span data-stu-id="00f82-108">Open PowerShell as Administrator and run:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

<span data-ttu-id="00f82-109">Para instalar solo WSL 1, debes reiniciar la máquina ahora y pasar a la sección [Instalación de la distribución de Linux que quieras](./install-win10.md#install-your-linux-distribution-of-choice). De lo contrario, espera a que se reinicie y avanza para actualizar a WSL 2.</span><span class="sxs-lookup"><span data-stu-id="00f82-109">To only install WSL 1, you should now restart your machine and move on to [Install your Linux distribution of choice](./install-win10.md#install-your-linux-distribution-of-choice), otherwise wait to restart and move on to update to WSL 2.</span></span> <span data-ttu-id="00f82-110">Obtén más información sobre la [Comparación de WSL 2 con WSL 1](./compare-versions.md).</span><span class="sxs-lookup"><span data-stu-id="00f82-110">Read more about [Comparing WSL 2 and WSL 1](./compare-versions.md).</span></span>

## <a name="update-to-wsl-2"></a><span data-ttu-id="00f82-111">Actualización a WSL 2</span><span class="sxs-lookup"><span data-stu-id="00f82-111">Update to WSL 2</span></span>

<span data-ttu-id="00f82-112">Para actualizar a WSL 2, debe cumplir los siguientes criterios:</span><span class="sxs-lookup"><span data-stu-id="00f82-112">To update to WSL 2, you must meet the following criteria:</span></span>

- <span data-ttu-id="00f82-113">Ejecutar Windows 10, [actualizado a la versión 1903 o posterior](ms-settings:windowsupdate), **compilación 18362** o posterior para sistemas x64.</span><span class="sxs-lookup"><span data-stu-id="00f82-113">Running Windows 10, [updated to version 1903 or higher](ms-settings:windowsupdate), **Build 18362** or higher for x64 systems.</span></span>
   - <span data-ttu-id="00f82-114">Si tiene la versión 1903 o 1909 de Windows 10, asegúrese de que el número de compilación menor es 1049 o superior.</span><span class="sxs-lookup"><span data-stu-id="00f82-114">If you are on Windows 10 version 1903 or 1909 make sure your minor build number is 1049 or higher.</span></span> <span data-ttu-id="00f82-115">Consulte las [instrucciones de solución de problemas completas aquí](https://docs.microsoft.com/windows/wsl/troubleshooting#im-on-windows-10-version-1903-and-i-still-do-not-see-options-for-wsl-2).</span><span class="sxs-lookup"><span data-stu-id="00f82-115">See [full troubleshooting instructions here](https://docs.microsoft.com/windows/wsl/troubleshooting#im-on-windows-10-version-1903-and-i-still-do-not-see-options-for-wsl-2)</span></span>
- <span data-ttu-id="00f82-116">Ejecutar Windows 10, actualizado a la versión 2004 o posterior, **compilación 19041**, para sistemas ARM64.</span><span class="sxs-lookup"><span data-stu-id="00f82-116">Running Windows 10, updated to version 2004 or higher, **build 19041**, for ARM64 systems.</span></span>
- <span data-ttu-id="00f82-117">Tenga en cuenta que, si se encuentra en Windows 10, versión 1903 o 1909, deberá asegurarse de que tiene la corrección compatible adecuada. Se pueden encontrar instrucciones [aquí](https://devblogs.microsoft.com/commandline/wsl-2-support-is-coming-to-windows-10-versions-1903-and-1909/#how-do-i-get-it).</span><span class="sxs-lookup"><span data-stu-id="00f82-117">Please note if you are on Windows 10 version 1903 or 1909 you will need to ensure that you have the proper backport, instructions can be [found here](https://devblogs.microsoft.com/commandline/wsl-2-support-is-coming-to-windows-10-versions-1903-and-1909/#how-do-i-get-it).</span></span> 

- <span data-ttu-id="00f82-118">Para comprobar la versión de Windows, selecciona la **tecla del logotipo de Windows + R**, escribe **winver** y selecciona **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="00f82-118">Check your Windows version by selecting the **Windows logo key + R**, type **winver**, select **OK**.</span></span> <span data-ttu-id="00f82-119">(También puedes escribir el comando `ver` en el símbolo del sistema de Windows).</span><span class="sxs-lookup"><span data-stu-id="00f82-119">(Or enter the `ver` command in Windows Command Prompt).</span></span> <span data-ttu-id="00f82-120">[Actualice a la versión más reciente de Windows](ms-settings:windowsupdate) si su compilación es anterior a la 18361.</span><span class="sxs-lookup"><span data-stu-id="00f82-120">Please [update to the latest Windows version](ms-settings:windowsupdate) if your build is lower than 18361.</span></span> <span data-ttu-id="00f82-121">[Obtén el Asistente de Windows Update](https://www.microsoft.com/software-download/windows10).</span><span class="sxs-lookup"><span data-stu-id="00f82-121">[Get Windows Update Assistant](https://www.microsoft.com/software-download/windows10).</span></span>

### <a name="enable-the-virtual-machine-platform-optional-component"></a><span data-ttu-id="00f82-122">Habilitación del componente opcional "Plataforma de máquina virtual"</span><span class="sxs-lookup"><span data-stu-id="00f82-122">Enable the 'Virtual Machine Platform' optional component</span></span>

<span data-ttu-id="00f82-123">Antes de instalar WSL 2, tienes que habilitar la característica opcional "Plataforma de máquina virtual".</span><span class="sxs-lookup"><span data-stu-id="00f82-123">Before installing WSL 2, you must enable the "Virtual Machine Platform" optional feature.</span></span>

<span data-ttu-id="00f82-124">Abre PowerShell como administrador y ejecuta:</span><span class="sxs-lookup"><span data-stu-id="00f82-124">Open PowerShell as Administrator and run:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

<span data-ttu-id="00f82-125">**Reinicia** la máquina para completar la instalación de WSL y la actualización a WSL 2.</span><span class="sxs-lookup"><span data-stu-id="00f82-125">**Restart** your machine to complete the WSL install and update to WSL 2.</span></span>

### <a name="set-wsl-2-as-your-default-version"></a><span data-ttu-id="00f82-126">Definición de WSL 2 como versión predeterminada</span><span class="sxs-lookup"><span data-stu-id="00f82-126">Set WSL 2 as your default version</span></span>

<span data-ttu-id="00f82-127">Abra PowerShell como Administrador y ejecute este comando para establecer WSL 2 como versión predeterminada al instalar una nueva distribución de Linux:</span><span class="sxs-lookup"><span data-stu-id="00f82-127">Open PowerShell as Administrator and run this command to set WSL 2 as the default version when installing a new Linux distribution:</span></span>

```powershell
wsl --set-default-version 2
```

<span data-ttu-id="00f82-128">Es posible que vea este mensaje después de ejecutar el comando: `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`.</span><span class="sxs-lookup"><span data-stu-id="00f82-128">You might see this message after running that command: `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`.</span></span> <span data-ttu-id="00f82-129">Siga el vínculo ([https://aka.ms/wsl2kernel](https://aka.ms/wsl2kernel)) e instale MSI desde esa página en nuestra documentación para instalar un kernel de Linux en la máquina para que lo use WSL 2.</span><span class="sxs-lookup"><span data-stu-id="00f82-129">Please follow the link ([https://aka.ms/wsl2kernel](https://aka.ms/wsl2kernel)) and install the MSI from that page on our documentation to install a Linux kernel on your machine for WSL 2 to use.</span></span> <span data-ttu-id="00f82-130">Una vez instalado el kernel, vuelva a ejecutar el comando, que debería completarse correctamente sin mostrar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="00f82-130">Once you have the kernel installed, please run the command again and it should complete successfully without showing the message.</span></span> 

> [!NOTE]
> <span data-ttu-id="00f82-131">La actualización de WSL 1 a WSL 2 puede tardar varios minutos en completarse, en función del tamaño de la distribución de destino.</span><span class="sxs-lookup"><span data-stu-id="00f82-131">The update from WSL 1 to WSL 2 may take several minutes to complete depending on the size of your targeted distribution.</span></span> <span data-ttu-id="00f82-132">Si ejecuta una instalación anterior (heredada) de WSL 1 de la Actualización de aniversario de Windows 10 o de Creators Update, es posible que se produzca un error de actualización.</span><span class="sxs-lookup"><span data-stu-id="00f82-132">If you are running an older (legacy) installation of WSL 1 from Windows 10 Anniversary Update or Creators Update, you may encounter an update error.</span></span> <span data-ttu-id="00f82-133">Siga estas instrucciones para [desinstalar y quitar las distribuciones heredadas](https://docs.microsoft.com/windows/wsl/install-legacy#uninstallingremoving-the-legacy-distro).</span><span class="sxs-lookup"><span data-stu-id="00f82-133">Follow these instructions to [uninstall and remove any legacy distributions](https://docs.microsoft.com/windows/wsl/install-legacy#uninstallingremoving-the-legacy-distro).</span></span> 
>
> <span data-ttu-id="00f82-134">Si `wsl --set-default-version` resulta en un comando no válido, especifique `wsl --help`.</span><span class="sxs-lookup"><span data-stu-id="00f82-134">If `wsl --set-default-version` results as an invalid command, enter `wsl --help`.</span></span> <span data-ttu-id="00f82-135">Si `--set-default-version` no aparece, significa que el sistema operativo no lo admite y debe actualizar a la versión 1903, compilación 18362 o posterior.</span><span class="sxs-lookup"><span data-stu-id="00f82-135">If the `--set-default-version` is not listed, it means that your OS doesn't support it and you need to update to version 1903, Build 18362 or higher.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="00f82-136">Instalación de la distribución de Linux que quieras</span><span class="sxs-lookup"><span data-stu-id="00f82-136">Install your Linux distribution of choice</span></span>

1. <span data-ttu-id="00f82-137">Abre [Microsoft Store](https://aka.ms/wslstore) y selecciona tu distribución de Linux favorita.</span><span class="sxs-lookup"><span data-stu-id="00f82-137">Open the [Microsoft Store](https://aka.ms/wslstore) and select your favorite Linux distribution.</span></span>

    ![Vista de las distribuciones de Linux en Microsoft Store](media/store.png)

    <span data-ttu-id="00f82-139">En los vínculos siguientes se abrirá la página de Microsoft Store para cada distribución:</span><span class="sxs-lookup"><span data-stu-id="00f82-139">The following links will open the Microsoft store page for each distribution:</span></span>

    - [<span data-ttu-id="00f82-140">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="00f82-140">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [<span data-ttu-id="00f82-141">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="00f82-141">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [<span data-ttu-id="00f82-142">Ubuntu 20.04 LTS</span><span class="sxs-lookup"><span data-stu-id="00f82-142">Ubuntu 20.04 LTS</span></span>](https://www.microsoft.com/store/apps/9n6svws3rx71)
    - [<span data-ttu-id="00f82-143">OpenSUSE Leap 15.1</span><span class="sxs-lookup"><span data-stu-id="00f82-143">openSUSE Leap 15.1</span></span>](https://www.microsoft.com/store/apps/9NJFZK00FGKV)
    - [<span data-ttu-id="00f82-144">SUSE Linux Enterprise Server 12 SP5</span><span class="sxs-lookup"><span data-stu-id="00f82-144">SUSE Linux Enterprise Server 12 SP5</span></span>](https://www.microsoft.com/store/apps/9MZ3D1TRP8T1)
    - [<span data-ttu-id="00f82-145">SUSE Linux Enterprise Server 15 SP1</span><span class="sxs-lookup"><span data-stu-id="00f82-145">SUSE Linux Enterprise Server 15 SP1</span></span>](https://www.microsoft.com/store/apps/9PN498VPMF3Z)
    - [<span data-ttu-id="00f82-146">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="00f82-146">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [<span data-ttu-id="00f82-147">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="00f82-147">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [<span data-ttu-id="00f82-148">Fedora Remix for WSL</span><span class="sxs-lookup"><span data-stu-id="00f82-148">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [<span data-ttu-id="00f82-149">Pengwin</span><span class="sxs-lookup"><span data-stu-id="00f82-149">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [<span data-ttu-id="00f82-150">Pengwin Enterprise</span><span class="sxs-lookup"><span data-stu-id="00f82-150">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [<span data-ttu-id="00f82-151">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="00f82-151">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

2. <span data-ttu-id="00f82-152">En la página de la distribución, selecciona "Obtener".</span><span class="sxs-lookup"><span data-stu-id="00f82-152">From the distribution's page, select "Get".</span></span>

    ![Distribuciones de Linux en Microsoft Store](media/UbuntuStore.png)

## <a name="set-up-a-new-distribution"></a><span data-ttu-id="00f82-154">Configuración de una nueva distribución</span><span class="sxs-lookup"><span data-stu-id="00f82-154">Set up a new distribution</span></span>

<span data-ttu-id="00f82-155">La primera vez que inicies una distribución de Linux recién instalada, se abrirá una ventana de la consola y se te pedirá que esperes un minuto o dos para que los archivos se descompriman y se almacenen en tu equipo.</span><span class="sxs-lookup"><span data-stu-id="00f82-155">The first time you launch a newly installed Linux distribution, a console window will open and you'll be asked to wait for a minute or two for files to de-compress and be stored on your PC.</span></span> <span data-ttu-id="00f82-156">Todos los inicios posteriores deberían tardar menos de un segundo en completarse.</span><span class="sxs-lookup"><span data-stu-id="00f82-156">All future launches should take less than a second.</span></span>

<span data-ttu-id="00f82-157">Tendrás que [crear una cuenta de usuario y una contraseña para la nueva distribución de Linux](./user-support.md).</span><span class="sxs-lookup"><span data-stu-id="00f82-157">You will then need to [create a user account and password for your new Linux distribution](./user-support.md).</span></span>

![Desempaquetado de Ubuntu en la consola de Windows](media/UbuntuInstall.png)

## <a name="set-your-distribution-version-to-wsl-1-or-wsl-2"></a><span data-ttu-id="00f82-159">Definición de la versión de la distribución en WSL 1 o WSL 2</span><span class="sxs-lookup"><span data-stu-id="00f82-159">Set your distribution version to WSL 1 or WSL 2</span></span>

<span data-ttu-id="00f82-160">Para comprobar la versión de WSL asignada a cada una de las distribuciones de Linux que tienes instaladas, abre la línea de comandos de PowerShell y escribe el comando (solo disponible en [Windows, compilación 18362 o posterior](ms-settings:windowsupdate)): `wsl -l -v`.</span><span class="sxs-lookup"><span data-stu-id="00f82-160">You can check the WSL version assigned to each of the Linux distributions you have installed by opening the PowerShell command line and entering the command (only available in [Windows Build 18362 or higher](ms-settings:windowsupdate)): `wsl -l -v`</span></span>

```powershell
wsl --list --verbose
```

<span data-ttu-id="00f82-161">Para establecer que una distribución esté respaldada por una de las dos versiones de WSL, ejecuta:</span><span class="sxs-lookup"><span data-stu-id="00f82-161">To set a distribution to be backed by either version of WSL please run:</span></span>

```powershell
wsl --set-version <distribution name> <versionNumber>
```

<span data-ttu-id="00f82-162">Asegúrate de reemplazar `<distribution name>` por el nombre real de tu distribución, y `<versionNumber>` por el número "1" o "2".</span><span class="sxs-lookup"><span data-stu-id="00f82-162">Make sure to replace `<distribution name>` with the actual name of your distribution and `<versionNumber>` with the number '1' or '2'.</span></span> <span data-ttu-id="00f82-163">Puedes volver a cambiar a WSL 1 en cualquier momento; para ello, ejecuta el mismo comando que antes, pero reemplaza "2" por "1".</span><span class="sxs-lookup"><span data-stu-id="00f82-163">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="00f82-164">Además, si quieres que WSL 2 sea la arquitectura predeterminada, puedes hacerlo con este comando:</span><span class="sxs-lookup"><span data-stu-id="00f82-164">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

```powershell
wsl --set-default-version 2
```

<span data-ttu-id="00f82-165">De este modo, se establecerá la versión de cualquier nueva distribución instalada en WSL 2.</span><span class="sxs-lookup"><span data-stu-id="00f82-165">This will set the version of any new distribution installed to WSL 2.</span></span>

## <a name="troubleshooting-installation"></a><span data-ttu-id="00f82-166">Solución de problemas de instalación</span><span class="sxs-lookup"><span data-stu-id="00f82-166">Troubleshooting installation</span></span>

<span data-ttu-id="00f82-167">A continuación, se muestran errores relacionados y las correcciones sugeridas.</span><span class="sxs-lookup"><span data-stu-id="00f82-167">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="00f82-168">Consulta la [página de solución de problemas de WSL](troubleshooting.md) para ver otros errores generales y sus soluciones.</span><span class="sxs-lookup"><span data-stu-id="00f82-168">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

- <span data-ttu-id="00f82-169">**Error 0x80070003 en la instalación**</span><span class="sxs-lookup"><span data-stu-id="00f82-169">**Installation failed with error 0x80070003**</span></span>
  - <span data-ttu-id="00f82-170">El Subsistema de Windows para Linux solo se ejecuta en la unidad del sistema (normalmente se trata de la unidad `C:`).</span><span class="sxs-lookup"><span data-stu-id="00f82-170">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="00f82-171">Asegúrate de que las distribuciones estén almacenadas en la unidad del sistema:</span><span class="sxs-lookup"><span data-stu-id="00f82-171">Make sure that distributions are stored on your system drive:</span></span>  
  - <span data-ttu-id="00f82-172">Abre **Configuración** -> **Almacenamiento** -> **Más opciones de almacenamiento: Cambia el lugar donde se guarda el nuevo contenido**
    ![Imagen de la configuración del sistema para instalar aplicaciones en la unidad C:](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="00f82-172">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>

- <span data-ttu-id="00f82-173">**Error 0x8007019e de WslRegisterDistribution**</span><span class="sxs-lookup"><span data-stu-id="00f82-173">**WslRegisterDistribution failed with error 0x8007019e**</span></span>
  - <span data-ttu-id="00f82-174">El componente opcional del Subsistema de Windows para Linux no está habilitado:</span><span class="sxs-lookup"><span data-stu-id="00f82-174">The Windows Subsystem for Linux optional component is not enabled:</span></span>
  - <span data-ttu-id="00f82-175">Abre el **Panel de control** -> **Programas y características** -> **Activa o desactiva la característica de Windows** -> Selecciona **Subsistema de Windows para Linux** o usa el cmdlet de PowerShell mencionado al comienzo de este artículo.</span><span class="sxs-lookup"><span data-stu-id="00f82-175">Open **Control Panel** -> **Programs and Features** -> **Turn Windows Feature on or off** -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the beginning of this article.</span></span>

- <span data-ttu-id="00f82-176">**Error en la instalación 0x80070003 o 0x80370102**</span><span class="sxs-lookup"><span data-stu-id="00f82-176">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
  - <span data-ttu-id="00f82-177">Asegúrate de que la virtualización está habilitada dentro del BIOS del equipo.</span><span class="sxs-lookup"><span data-stu-id="00f82-177">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="00f82-178">Las instrucciones sobre cómo hacerlo variarán de un equipo a otro y lo más probable es que esta característica esté en opciones relacionadas con la CPU.</span><span class="sxs-lookup"><span data-stu-id="00f82-178">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>

- <span data-ttu-id="00f82-179">**Error al intentar actualizar: `Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="00f82-179">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
  - <span data-ttu-id="00f82-180">Asegúrese de que tiene el Subsistema de Windows para Linux habilitado y de que usa la compilación 18362 de Windows o posterior.</span><span class="sxs-lookup"><span data-stu-id="00f82-180">Enure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18362 or higher.</span></span> <span data-ttu-id="00f82-181">Para habilitar WSL, ejecute este comando en un símbolo del sistema de PowerShell con privilegios de administrador: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span><span class="sxs-lookup"><span data-stu-id="00f82-181">To enable WSL run this command in a PowerShell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span>

- <span data-ttu-id="00f82-182">**La operación solicitada no se pudo completar debido a una limitación del sistema de disco virtual. Los archivos de disco duro virtual deben estar sin comprimir y sin cifrar y no deben ser dispersos.**</span><span class="sxs-lookup"><span data-stu-id="00f82-182">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span></span>
  - <span data-ttu-id="00f82-183">Anule la selección de la casilla "Compress contents" ("Comprimir contenido") (y también la de "Cifrar los contenidos" si está activada). Para ello, abra la carpeta de perfil de la distribución de Linux.</span><span class="sxs-lookup"><span data-stu-id="00f82-183">Deselect “Compress contents” (as well as “Encrypt contents” if that’s checked) by opening the profile folder for your Linux distribution.</span></span> <span data-ttu-id="00f82-184">Debe encontrarse en una carpeta del sistema de archivos de Windows, como `USERPROFILE%\AppData\Local\Packages\CanonicalGroupLimited...`.</span><span class="sxs-lookup"><span data-stu-id="00f82-184">It should be located in a folder on your Windows file system, something like: `USERPROFILE%\AppData\Local\Packages\CanonicalGroupLimited...`</span></span>
  - <span data-ttu-id="00f82-185">En este perfil de distribución de Linux, debe haber una carpeta denominada LocalState.</span><span class="sxs-lookup"><span data-stu-id="00f82-185">In this Linux distro profile, there should be a LocalState folder.</span></span> <span data-ttu-id="00f82-186">Haga clic con el botón derecho en ella para mostrar un menú de opciones.</span><span class="sxs-lookup"><span data-stu-id="00f82-186">Right-click this folder to display a menu of options.</span></span> <span data-ttu-id="00f82-187">Seleccione Propiedades > Opciones avanzadas y, a continuación, asegúrese de que las casillas "Comprimir contenido para ahorrar espacio en disco" y "Cifrar contenido para proteger datos" no estén seleccionadas (activadas).</span><span class="sxs-lookup"><span data-stu-id="00f82-187">Select Properties > Advanced and then ensure that the “Compress contents to save disk space” and “Encrypt contents to secure data” checkboxes are unselected (not checked).</span></span> <span data-ttu-id="00f82-188">Si se le pregunta si quiere aplicar esto solo a la carpeta actual o a todas las subcarpetas y archivos, seleccione "solo esta carpeta", ya que solo quiere borrar la marca de compresión.</span><span class="sxs-lookup"><span data-stu-id="00f82-188">If you are asked whether to apply this to just to the current folder or to all subfolders and files, select “just this folder” because you are only clearing the compress flag.</span></span> <span data-ttu-id="00f82-189">A continuación, el comando `wsl --set-version` debería funcionar.</span><span class="sxs-lookup"><span data-stu-id="00f82-189">After this, the `wsl --set-version` command should work.</span></span>

![Captura de pantalla de la configuración de la propiedad de distribución de WSL](media/troubleshooting-virtualdisk-compress.png)

> [!NOTE]
> <span data-ttu-id="00f82-191">En mi caso, la carpeta LocalState de la distribución de Ubuntu 18.04 se encontraba en C:\Users\<my-user-name>\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu18.04onWindows_79rhkp1fndgsc.</span><span class="sxs-lookup"><span data-stu-id="00f82-191">In my case, the LocalState folder for my Ubuntu 18.04 distribution was located at C:\Users\<my-user-name>\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu18.04onWindows_79rhkp1fndgsc</span></span>
>
> <span data-ttu-id="00f82-192">Consulte el [subproceso n.º 4103 de la documentación sobre WSL en GitHub](https://github.com/microsoft/WSL/issues/4103), en el que se realiza el seguimiento de este problema para obtener información actualizada.</span><span class="sxs-lookup"><span data-stu-id="00f82-192">Check [WSL Docs GitHub thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span></span>

- <span data-ttu-id="00f82-193">**El término 'wsl' no se reconoce como nombre de cmdlet, función, archivo de script o programa ejecutable.**</span><span class="sxs-lookup"><span data-stu-id="00f82-193">**The term 'wsl' is not recognized as the name of a cmdlet, function, script file, or operable program.**</span></span>
  - <span data-ttu-id="00f82-194">Asegúrate de que el [componente opcional del Subsistema de Windows para Linux esté instalado](./install-win10.md#enable-the-virtual-machine-platform-optional-component).</span><span class="sxs-lookup"><span data-stu-id="00f82-194">Ensure that the [Windows Subsystem for Linux Optional Component is installed](./install-win10.md#enable-the-virtual-machine-platform-optional-component).</span></span> <span data-ttu-id="00f82-195">Además, si usa un dispositivo ARM64 y ejecuta este comando desde PowerShell, recibirá este error.</span><span class="sxs-lookup"><span data-stu-id="00f82-195">Additionally, if you are using an ARM64 device and running this command from PowerShell, you will receive this error.</span></span> <span data-ttu-id="00f82-196">En su lugar, ejecuta `wsl.exe` desde [PowerShell Core](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6) o el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="00f82-196">Instead run `wsl.exe` from [PowerShell Core](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6), or Command Prompt.</span></span>
