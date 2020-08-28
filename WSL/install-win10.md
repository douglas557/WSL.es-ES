---
title: Instalar el Subsistema de Windows para Linux (WSL) en Windows 10
description: Obtenga información sobre cómo instalar el Subsistema de Windows para Linux en Windows 10. Windows 10 debe actualizarse a la versión 2004, compilación 19041 o posterior.
keywords: BashOnWindows, bash, wsl, wsl2, windows, subsistema de windows para linux, subsistemawindows, ubuntu, debian, suse, windows 10, instalación, instalar, habilitación, habilitar, WSL2, versión 2
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 23c72c0e82c90c23fc0406b56dbf8accad0e39df
ms.sourcegitcommit: fb79750bd71d6ebaed5203b3de71ba85a67227b1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2020
ms.locfileid: "88866165"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="1fd79-105">Guía de instalación del Subsistema de Windows para Linux para Windows 10</span><span class="sxs-lookup"><span data-stu-id="1fd79-105">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="1fd79-106">Instalar el Subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="1fd79-106">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="1fd79-107">Antes de instalar distribuciones de Linux en Windows, debes habilitar la característica opcional "Subsistema de Windows para Linux".</span><span class="sxs-lookup"><span data-stu-id="1fd79-107">Before installing any Linux distributions on Windows, you must enable the "Windows Subsystem for Linux" optional feature.</span></span>

<span data-ttu-id="1fd79-108">Abre PowerShell como administrador y ejecuta:</span><span class="sxs-lookup"><span data-stu-id="1fd79-108">Open PowerShell as Administrator and run:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

<span data-ttu-id="1fd79-109">Para instalar solo WSL 1, debes reiniciar la máquina ahora y pasar a la sección [Instalación de la distribución de Linux que quieras](./install-win10.md#install-your-linux-distribution-of-choice). De lo contrario, espera a que se reinicie y avanza para actualizar a WSL 2.</span><span class="sxs-lookup"><span data-stu-id="1fd79-109">To only install WSL 1, you should now restart your machine and move on to [Install your Linux distribution of choice](./install-win10.md#install-your-linux-distribution-of-choice), otherwise wait to restart and move on to update to WSL 2.</span></span> <span data-ttu-id="1fd79-110">Obtén más información sobre la [Comparación de WSL 2 con WSL 1](./compare-versions.md).</span><span class="sxs-lookup"><span data-stu-id="1fd79-110">Read more about [Comparing WSL 2 and WSL 1](./compare-versions.md).</span></span>

## <a name="update-to-wsl-2"></a><span data-ttu-id="1fd79-111">Actualización a WSL 2</span><span class="sxs-lookup"><span data-stu-id="1fd79-111">Update to WSL 2</span></span>

<span data-ttu-id="1fd79-112">Para actualizar a WSL 2, debe cumplir los siguientes criterios:</span><span class="sxs-lookup"><span data-stu-id="1fd79-112">To update to WSL 2, you must meet the following criteria:</span></span>

- <span data-ttu-id="1fd79-113">Ejecutar Windows 10, [actualizado a la versión 1903 o posterior](ms-settings:windowsupdate), **compilación 18362** o posterior.</span><span class="sxs-lookup"><span data-stu-id="1fd79-113">Running Windows 10, [updated to version 1903 or higher](ms-settings:windowsupdate), **Build 18362** or higher.</span></span>

- <span data-ttu-id="1fd79-114">Para comprobar la versión de Windows, selecciona la **tecla del logotipo de Windows + R**, escribe **winver** y selecciona **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="1fd79-114">Check your Windows version by selecting the **Windows logo key + R**, type **winver**, select **OK**.</span></span> <span data-ttu-id="1fd79-115">(También puedes escribir el comando `ver` en el símbolo del sistema de Windows).</span><span class="sxs-lookup"><span data-stu-id="1fd79-115">(Or enter the `ver` command in Windows Command Prompt).</span></span> <span data-ttu-id="1fd79-116">[Actualice a la versión más reciente de Windows](ms-settings:windowsupdate) si su compilación es anterior a la 18361.</span><span class="sxs-lookup"><span data-stu-id="1fd79-116">Please [update to the latest Windows version](ms-settings:windowsupdate) if your build is lower than 18361.</span></span> <span data-ttu-id="1fd79-117">[Obtén el Asistente de Windows Update](https://www.microsoft.com/software-download/windows10).</span><span class="sxs-lookup"><span data-stu-id="1fd79-117">[Get Windows Update Assistant](https://www.microsoft.com/software-download/windows10).</span></span>

### <a name="enable-the-virtual-machine-platform-optional-component"></a><span data-ttu-id="1fd79-118">Habilitación del componente opcional "Plataforma de máquina virtual"</span><span class="sxs-lookup"><span data-stu-id="1fd79-118">Enable the 'Virtual Machine Platform' optional component</span></span>

<span data-ttu-id="1fd79-119">Antes de instalar WSL 2, tienes que habilitar la característica opcional "Plataforma de máquina virtual".</span><span class="sxs-lookup"><span data-stu-id="1fd79-119">Before installing WSL 2, you must enable the "Virtual Machine Platform" optional feature.</span></span>

<span data-ttu-id="1fd79-120">Abre PowerShell como administrador y ejecuta:</span><span class="sxs-lookup"><span data-stu-id="1fd79-120">Open PowerShell as Administrator and run:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

<span data-ttu-id="1fd79-121">**Reinicia** la máquina para completar la instalación de WSL y la actualización a WSL 2.</span><span class="sxs-lookup"><span data-stu-id="1fd79-121">**Restart** your machine to complete the WSL install and update to WSL 2.</span></span>

### <a name="set-wsl-2-as-your-default-version"></a><span data-ttu-id="1fd79-122">Definición de WSL 2 como versión predeterminada</span><span class="sxs-lookup"><span data-stu-id="1fd79-122">Set WSL 2 as your default version</span></span>

<span data-ttu-id="1fd79-123">Abra PowerShell como Administrador y ejecute este comando para establecer WSL 2 como versión predeterminada al instalar una nueva distribución de Linux:</span><span class="sxs-lookup"><span data-stu-id="1fd79-123">Open PowerShell as Administrator and run this command to set WSL 2 as the default version when installing a new Linux distribution:</span></span>

```powershell
wsl --set-default-version 2
```

<span data-ttu-id="1fd79-124">Es posible que vea este mensaje después de ejecutar el comando: `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`.</span><span class="sxs-lookup"><span data-stu-id="1fd79-124">You might see this message after running that command: `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`.</span></span> <span data-ttu-id="1fd79-125">Siga el vínculo ([https://aka.ms/wsl2kernel](https://aka.ms/wsl2kernel)) e instale MSI desde esa página en nuestra documentación para instalar un kernel de Linux en la máquina para que lo use WSL 2.</span><span class="sxs-lookup"><span data-stu-id="1fd79-125">Please follow the link ([https://aka.ms/wsl2kernel](https://aka.ms/wsl2kernel)) and install the MSI from that page on our documentation to install a Linux kernel on your machine for WSL 2 to use.</span></span> <span data-ttu-id="1fd79-126">Una vez instalado el kernel, vuelva a ejecutar el comando, que debería completarse correctamente sin mostrar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="1fd79-126">Once you have the kernel installed, please run the command again and it should complete successfully without showing the message.</span></span> 

> [!NOTE]
> <span data-ttu-id="1fd79-127">La actualización de WSL 1 a WSL 2 puede tardar varios minutos en completarse, en función del tamaño de la distribución de destino.</span><span class="sxs-lookup"><span data-stu-id="1fd79-127">The update from WSL 1 to WSL 2 may take several minutes to complete depending on the size of your targeted distribution.</span></span> <span data-ttu-id="1fd79-128">Si ejecuta una instalación anterior (heredada) de WSL 1 de la Actualización de aniversario de Windows 10 o de Creators Update, es posible que se produzca un error de actualización.</span><span class="sxs-lookup"><span data-stu-id="1fd79-128">If you are running an older (legacy) installation of WSL 1 from Windows 10 Anniversary Update or Creators Update, you may encounter an update error.</span></span> <span data-ttu-id="1fd79-129">Siga estas instrucciones para [desinstalar y quitar las distribuciones heredadas](https://docs.microsoft.com/windows/wsl/install-legacy#uninstallingremoving-the-legacy-distro).</span><span class="sxs-lookup"><span data-stu-id="1fd79-129">Follow these instructions to [uninstall and remove any legacy distributions](https://docs.microsoft.com/windows/wsl/install-legacy#uninstallingremoving-the-legacy-distro).</span></span> 
>
> <span data-ttu-id="1fd79-130">Si `wsl --set-default-version` resulta en un comando no válido, especifique `wsl --help`.</span><span class="sxs-lookup"><span data-stu-id="1fd79-130">If `wsl --set-default-version` results as an invalid command, enter `wsl --help`.</span></span> <span data-ttu-id="1fd79-131">Si `--set-default-version` no aparece, significa que el sistema operativo no lo admite y debe actualizar a la versión 1903, compilación 18362 o posterior.</span><span class="sxs-lookup"><span data-stu-id="1fd79-131">If the `--set-default-version` is not listed, it means that your OS doesn't support it and you need to update to version 1903, Build 18362 or higher.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="1fd79-132">Instalación de la distribución de Linux que quieras</span><span class="sxs-lookup"><span data-stu-id="1fd79-132">Install your Linux distribution of choice</span></span>

1. <span data-ttu-id="1fd79-133">Abre [Microsoft Store](https://aka.ms/wslstore) y selecciona tu distribución de Linux favorita.</span><span class="sxs-lookup"><span data-stu-id="1fd79-133">Open the [Microsoft Store](https://aka.ms/wslstore) and select your favorite Linux distribution.</span></span>

    ![Vista de las distribuciones de Linux en Microsoft Store](media/store.png)

    <span data-ttu-id="1fd79-135">En los vínculos siguientes se abrirá la página de Microsoft Store para cada distribución:</span><span class="sxs-lookup"><span data-stu-id="1fd79-135">The following links will open the Microsoft store page for each distribution:</span></span>

    - [<span data-ttu-id="1fd79-136">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="1fd79-136">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [<span data-ttu-id="1fd79-137">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="1fd79-137">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [<span data-ttu-id="1fd79-138">Ubuntu 20.04 LTS</span><span class="sxs-lookup"><span data-stu-id="1fd79-138">Ubuntu 20.04 LTS</span></span>](https://www.microsoft.com/store/apps/9n6svws3rx71)
    - [<span data-ttu-id="1fd79-139">OpenSUSE Leap 15.1</span><span class="sxs-lookup"><span data-stu-id="1fd79-139">openSUSE Leap 15.1</span></span>](https://www.microsoft.com/store/apps/9NJFZK00FGKV)
    - [<span data-ttu-id="1fd79-140">SUSE Linux Enterprise Server 12 SP5</span><span class="sxs-lookup"><span data-stu-id="1fd79-140">SUSE Linux Enterprise Server 12 SP5</span></span>](https://www.microsoft.com/store/apps/9MZ3D1TRP8T1)
    - [<span data-ttu-id="1fd79-141">SUSE Linux Enterprise Server 15 SP1</span><span class="sxs-lookup"><span data-stu-id="1fd79-141">SUSE Linux Enterprise Server 15 SP1</span></span>](https://www.microsoft.com/store/apps/9PN498VPMF3Z)
    - [<span data-ttu-id="1fd79-142">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="1fd79-142">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [<span data-ttu-id="1fd79-143">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="1fd79-143">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [<span data-ttu-id="1fd79-144">Fedora Remix for WSL</span><span class="sxs-lookup"><span data-stu-id="1fd79-144">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [<span data-ttu-id="1fd79-145">Pengwin</span><span class="sxs-lookup"><span data-stu-id="1fd79-145">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [<span data-ttu-id="1fd79-146">Pengwin Enterprise</span><span class="sxs-lookup"><span data-stu-id="1fd79-146">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [<span data-ttu-id="1fd79-147">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="1fd79-147">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

2. <span data-ttu-id="1fd79-148">En la página de la distribución, selecciona "Obtener".</span><span class="sxs-lookup"><span data-stu-id="1fd79-148">From the distribution's page, select "Get".</span></span>

    ![Distribuciones de Linux en Microsoft Store](media/UbuntuStore.png)

## <a name="set-up-a-new-distribution"></a><span data-ttu-id="1fd79-150">Configuración de una nueva distribución</span><span class="sxs-lookup"><span data-stu-id="1fd79-150">Set up a new distribution</span></span>

<span data-ttu-id="1fd79-151">La primera vez que inicies una distribución de Linux recién instalada, se abrirá una ventana de la consola y se te pedirá que esperes un minuto o dos para que los archivos se descompriman y se almacenen en tu equipo.</span><span class="sxs-lookup"><span data-stu-id="1fd79-151">The first time you launch a newly installed Linux distribution, a console window will open and you'll be asked to wait for a minute or two for files to de-compress and be stored on your PC.</span></span> <span data-ttu-id="1fd79-152">Todos los inicios posteriores deberían tardar menos de un segundo en completarse.</span><span class="sxs-lookup"><span data-stu-id="1fd79-152">All future launches should take less than a second.</span></span>

<span data-ttu-id="1fd79-153">Tendrás que [crear una cuenta de usuario y una contraseña para la nueva distribución de Linux](./user-support.md).</span><span class="sxs-lookup"><span data-stu-id="1fd79-153">You will then need to [create a user account and password for your new Linux distribution](./user-support.md).</span></span>

![Desempaquetado de Ubuntu en la consola de Windows](media/UbuntuInstall.png)

## <a name="set-your-distribution-version-to-wsl-1-or-wsl-2"></a><span data-ttu-id="1fd79-155">Definición de la versión de la distribución en WSL 1 o WSL 2</span><span class="sxs-lookup"><span data-stu-id="1fd79-155">Set your distribution version to WSL 1 or WSL 2</span></span>

<span data-ttu-id="1fd79-156">Para comprobar la versión de WSL asignada a cada una de las distribuciones de Linux que tienes instaladas, abre la línea de comandos de PowerShell y escribe el comando (solo disponible en [Windows, compilación 18362 o posterior](ms-settings:windowsupdate)): `wsl -l -v`.</span><span class="sxs-lookup"><span data-stu-id="1fd79-156">You can check the WSL version assigned to each of the Linux distributions you have installed by opening the PowerShell command line and entering the command (only available in [Windows Build 18362 or higher](ms-settings:windowsupdate)): `wsl -l -v`</span></span>

```powershell
wsl --list --verbose
```

<span data-ttu-id="1fd79-157">Para establecer que una distribución esté respaldada por una de las dos versiones de WSL, ejecuta:</span><span class="sxs-lookup"><span data-stu-id="1fd79-157">To set a distribution to be backed by either version of WSL please run:</span></span>

```powershell
wsl --set-version <distribution name> <versionNumber>
```

<span data-ttu-id="1fd79-158">Asegúrate de reemplazar `<distribution name>` por el nombre real de tu distribución, y `<versionNumber>` por el número "1" o "2".</span><span class="sxs-lookup"><span data-stu-id="1fd79-158">Make sure to replace `<distribution name>` with the actual name of your distribution and `<versionNumber>` with the number '1' or '2'.</span></span> <span data-ttu-id="1fd79-159">Puedes volver a cambiar a WSL 1 en cualquier momento; para ello, ejecuta el mismo comando que antes, pero reemplaza "2" por "1".</span><span class="sxs-lookup"><span data-stu-id="1fd79-159">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="1fd79-160">Además, si quieres que WSL 2 sea la arquitectura predeterminada, puedes hacerlo con este comando:</span><span class="sxs-lookup"><span data-stu-id="1fd79-160">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

```powershell
wsl --set-default-version 2
```

<span data-ttu-id="1fd79-161">De este modo, se establecerá la versión de cualquier nueva distribución instalada en WSL 2.</span><span class="sxs-lookup"><span data-stu-id="1fd79-161">This will set the version of any new distribution installed to WSL 2.</span></span>

## <a name="troubleshooting-installation"></a><span data-ttu-id="1fd79-162">Solución de problemas de instalación</span><span class="sxs-lookup"><span data-stu-id="1fd79-162">Troubleshooting installation</span></span>

<span data-ttu-id="1fd79-163">A continuación, se muestran errores relacionados y las correcciones sugeridas.</span><span class="sxs-lookup"><span data-stu-id="1fd79-163">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="1fd79-164">Consulta la [página de solución de problemas de WSL](troubleshooting.md) para ver otros errores generales y sus soluciones.</span><span class="sxs-lookup"><span data-stu-id="1fd79-164">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

- <span data-ttu-id="1fd79-165">**Error 0x80070003 en la instalación**</span><span class="sxs-lookup"><span data-stu-id="1fd79-165">**Installation failed with error 0x80070003**</span></span>
  - <span data-ttu-id="1fd79-166">El Subsistema de Windows para Linux solo se ejecuta en la unidad del sistema (normalmente se trata de la unidad `C:`).</span><span class="sxs-lookup"><span data-stu-id="1fd79-166">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="1fd79-167">Asegúrate de que las distribuciones estén almacenadas en la unidad del sistema:</span><span class="sxs-lookup"><span data-stu-id="1fd79-167">Make sure that distributions are stored on your system drive:</span></span>  
  - <span data-ttu-id="1fd79-168">Abre **Configuración** -> **Almacenamiento** -> **Más opciones de almacenamiento: Cambia el lugar donde se guarda el nuevo contenido**
    ![Imagen de la configuración del sistema para instalar aplicaciones en la unidad C:](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="1fd79-168">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>

- <span data-ttu-id="1fd79-169">**Error 0x8007019e de WslRegisterDistribution**</span><span class="sxs-lookup"><span data-stu-id="1fd79-169">**WslRegisterDistribution failed with error 0x8007019e**</span></span>
  - <span data-ttu-id="1fd79-170">El componente opcional del Subsistema de Windows para Linux no está habilitado:</span><span class="sxs-lookup"><span data-stu-id="1fd79-170">The Windows Subsystem for Linux optional component is not enabled:</span></span>
  - <span data-ttu-id="1fd79-171">Abre el **Panel de control** -> **Programas y características** -> **Activa o desactiva la característica de Windows** -> Selecciona **Subsistema de Windows para Linux** o usa el cmdlet de PowerShell mencionado al comienzo de este artículo.</span><span class="sxs-lookup"><span data-stu-id="1fd79-171">Open **Control Panel** -> **Programs and Features** -> **Turn Windows Feature on or off** -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the beginning of this article.</span></span>

- <span data-ttu-id="1fd79-172">**Error en la instalación 0x80070003 o 0x80370102**</span><span class="sxs-lookup"><span data-stu-id="1fd79-172">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
  - <span data-ttu-id="1fd79-173">Asegúrate de que la virtualización está habilitada dentro del BIOS del equipo.</span><span class="sxs-lookup"><span data-stu-id="1fd79-173">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="1fd79-174">Las instrucciones sobre cómo hacerlo variarán de un equipo a otro y lo más probable es que esta característica esté en opciones relacionadas con la CPU.</span><span class="sxs-lookup"><span data-stu-id="1fd79-174">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>

- <span data-ttu-id="1fd79-175">**Error al intentar actualizar: `Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="1fd79-175">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
  - <span data-ttu-id="1fd79-176">Asegúrese de que tiene el Subsistema de Windows para Linux habilitado y de que usa la compilación 18362 de Windows o posterior.</span><span class="sxs-lookup"><span data-stu-id="1fd79-176">Enure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18362 or higher.</span></span> <span data-ttu-id="1fd79-177">Para habilitar WSL, ejecute este comando en un símbolo del sistema de PowerShell con privilegios de administrador: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span><span class="sxs-lookup"><span data-stu-id="1fd79-177">To enable WSL run this command in a PowerShell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span>

- <span data-ttu-id="1fd79-178">**La operación solicitada no se pudo completar debido a una limitación del sistema de disco virtual. Los archivos de disco duro virtual deben estar sin comprimir y sin cifrar y no deben ser dispersos.**</span><span class="sxs-lookup"><span data-stu-id="1fd79-178">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span></span>
  - <span data-ttu-id="1fd79-179">Anule la selección de la casilla "Compress contents" ("Comprimir contenido") (y también la de "Cifrar los contenidos" si está activada). Para ello, abra la carpeta de perfil de la distribución de Linux.</span><span class="sxs-lookup"><span data-stu-id="1fd79-179">Deselect “Compress contents” (as well as “Encrypt contents” if that’s checked) by opening the profile folder for your Linux distribution.</span></span> <span data-ttu-id="1fd79-180">Debe encontrarse en una carpeta del sistema de archivos de Windows, como `USERPROFILE%\AppData\Local\Packages\CanonicalGroupLimited...`.</span><span class="sxs-lookup"><span data-stu-id="1fd79-180">It should be located in a folder on your Windows file system, something like: `USERPROFILE%\AppData\Local\Packages\CanonicalGroupLimited...`</span></span>
  - <span data-ttu-id="1fd79-181">En este perfil de distribución de Linux, debe haber una carpeta denominada LocalState.</span><span class="sxs-lookup"><span data-stu-id="1fd79-181">In this Linux distro profile, there should be a LocalState folder.</span></span> <span data-ttu-id="1fd79-182">Haga clic con el botón derecho en ella para mostrar un menú de opciones.</span><span class="sxs-lookup"><span data-stu-id="1fd79-182">Right-click this folder to display a menu of options.</span></span> <span data-ttu-id="1fd79-183">Seleccione Propiedades > Opciones avanzadas y, a continuación, asegúrese de que las casillas "Comprimir contenido para ahorrar espacio en disco" y "Cifrar contenido para proteger datos" no estén seleccionadas (activadas).</span><span class="sxs-lookup"><span data-stu-id="1fd79-183">Select Properties > Advanced and then ensure that the “Compress contents to save disk space” and “Encrypt contents to secure data” checkboxes are unselected (not checked).</span></span> <span data-ttu-id="1fd79-184">Si se le pregunta si quiere aplicar esto solo a la carpeta actual o a todas las subcarpetas y archivos, seleccione "solo esta carpeta", ya que solo quiere borrar la marca de compresión.</span><span class="sxs-lookup"><span data-stu-id="1fd79-184">If you are asked whether to apply this to just to the current folder or to all subfolders and files, select “just this folder” because you are only clearing the compress flag.</span></span> <span data-ttu-id="1fd79-185">A continuación, el comando `wsl –set-version` debería funcionar.</span><span class="sxs-lookup"><span data-stu-id="1fd79-185">After this, the `wsl –set-version` command should work.</span></span>

![Captura de pantalla de la configuración de la propiedad de distribución de WSL](media/troubleshooting-virtualdisk-compress.png)

> [!NOTE]
> <span data-ttu-id="1fd79-187">En mi caso, la carpeta LocalState de la distribución de Ubuntu 18.04 se encontraba en C:\Users\<my-user-name>\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu18.04onWindows_79rhkp1fndgsc.</span><span class="sxs-lookup"><span data-stu-id="1fd79-187">In my case, the LocalState folder for my Ubuntu 18.04 distribution was located at C:\Users\<my-user-name>\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu18.04onWindows_79rhkp1fndgsc</span></span>
>
> <span data-ttu-id="1fd79-188">Consulte el [subproceso n.º 4103 de la documentación sobre WSL en GitHub](https://github.com/microsoft/WSL/issues/4103), en el que se realiza el seguimiento de este problema para obtener información actualizada.</span><span class="sxs-lookup"><span data-stu-id="1fd79-188">Check [WSL Docs GitHub thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span></span>

- <span data-ttu-id="1fd79-189">**El término 'wsl' no se reconoce como nombre de cmdlet, función, archivo de script o programa ejecutable.**</span><span class="sxs-lookup"><span data-stu-id="1fd79-189">**The term 'wsl' is not recognized as the name of a cmdlet, function, script file, or operable program.**</span></span>
  - <span data-ttu-id="1fd79-190">Asegúrate de que el [componente opcional del Subsistema de Windows para Linux esté instalado](./install-win10.md#enable-the-virtual-machine-platform-optional-component).</span><span class="sxs-lookup"><span data-stu-id="1fd79-190">Ensure that the [Windows Subsystem for Linux Optional Component is installed](./install-win10.md#enable-the-virtual-machine-platform-optional-component).</span></span> <span data-ttu-id="1fd79-191">Además, si usa un dispositivo ARM64 y ejecuta este comando desde PowerShell, recibirá este error.</span><span class="sxs-lookup"><span data-stu-id="1fd79-191">Additionally, if you are using an ARM64 device and running this command from PowerShell, you will receive this error.</span></span> <span data-ttu-id="1fd79-192">En su lugar, ejecuta `wsl.exe` desde [PowerShell Core](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6) o el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="1fd79-192">Instead run `wsl.exe` from [PowerShell Core](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6), or Command Prompt.</span></span>
