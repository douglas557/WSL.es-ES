---
title: Instalar o quitar en Windows 10 Anniversary Update o Creators Update
description: Instrucciones de instalación y desinstalación para el heredado, la distribución beta en Windows 10 Anniversary Update o Creators Update
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, windowssubsystem, ubuntu, debian, suse, windows 10, heredado, beta, instalar, quitar, desinstalar, desinstalar, eliminación, en desuso
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: fbb5bdc401a013b0853774cff6ad2dc84a36e412
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040838"
---
# <a name="guide-to-install-or-uninstall-windows-subsystem-for-linux-on-windows-10-anniversary-update-and-creators-update"></a><span data-ttu-id="b476b-104">Guía para instalar o desinstalar el subsistema de Windows para Linux en Windows 10 Anniversary Update y Creators Update</span><span class="sxs-lookup"><span data-stu-id="b476b-104">Guide to install or uninstall Windows Subsystem for Linux on Windows 10 Anniversary Update and Creators Update</span></span> 

<span data-ttu-id="b476b-105">Si está ejecutando Windows 10 Creators Update o posterior, por favor, [siga las instrucciones de instalación de Windows 10](install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="b476b-105">If you're running Windows 10 Creators Update or later, please [follow the Windows 10 installation instructions](install-win10.md).</span></span>

<span data-ttu-id="b476b-106"><strong><em><span style="color: #f28014">Las instrucciones siguientes sirven para usuarios que ejecutan Windows 10 Anniversary Update o Windows 10 Creators Update</span></em></strong></span><span class="sxs-lookup"><span data-stu-id="b476b-106"><strong><em><span style="color: #f28014">The following instructions are for users running Windows 10 Anniversary Update or Windows 10 Creators Update</span></em></strong></span></span>

<span data-ttu-id="b476b-107">Antes de Windows 10 Fall Creators Update (versión 1709), WSL se lanzó como característica beta e instala una sola instancia de Ubuntu cuando "Bash en Ubuntu en Windows" (o Bash.exe) se ejecuta en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="b476b-107">Prior to Windows 10 Fall Creators Update (version 1709), WSL was released as a beta feature and installed a single Ubuntu instance when "Bash on Ubuntu on Windows" (or Bash.exe) was first run.</span></span>

> <span data-ttu-id="b476b-108">Aunque puede usar WSL en versiones anteriores de Windows 10, esta versión beta "distribución heredada" ahora se considera obsoleta.</span><span class="sxs-lookup"><span data-stu-id="b476b-108">While you CAN use WSL on earlier Windows 10 releases, this beta "legacy distro" is now considered obsolete.</span></span> <span data-ttu-id="b476b-109">Se recomienda encarecidamente ejecutar la versión más reciente de Windows 10 disponibles.</span><span class="sxs-lookup"><span data-stu-id="b476b-109">We strongly encourage you to run the most recent version of Windows 10 available.</span></span> <span data-ttu-id="b476b-110">Cada nueva versión de Windows 10 incluye muchos cientos de correcciones y mejoras en WSL por sí solo, lo que permite más herramientas de Linux y aplicaciones se ejecuten correctamente en WSL.</span><span class="sxs-lookup"><span data-stu-id="b476b-110">Each new Windows 10 release includes many hundreds of fixes and improvements in WSL alone, allowing ever more Linux tools and apps to run correctly on WSL.</span></span>

<span data-ttu-id="b476b-111">Si no se puede actualizar a Fall Creators Update o posterior, siga los pasos siguientes para habilitar y usar WSL:</span><span class="sxs-lookup"><span data-stu-id="b476b-111">If you cannot upgrade to Fall Creators Update or later, follow the steps below to enable and use WSL:</span></span>

1. <span data-ttu-id="b476b-112">Activar el modo de desarrollador para ejecutarse WSL en Windows 10 Anniversary Update o Creators Update, debe habilitar el modo de programador:</span><span class="sxs-lookup"><span data-stu-id="b476b-112">Turn on Developer Mode  To run WSL on Windows 10 Anniversary Update or Creators Update, you must enable Developer Mode:</span></span>

    <span data-ttu-id="b476b-113">Abra **configuración** -> **actualización y seguridad** -> **para desarrolladores**</span><span class="sxs-lookup"><span data-stu-id="b476b-113">Open **Settings** -> **Update and Security** -> **For developers**</span></span>

    <span data-ttu-id="b476b-114">Seleccione el botón de radio del modo de programador</span><span class="sxs-lookup"><span data-stu-id="b476b-114">Select the Developer Mode radio button</span></span>  
    ![Habilitar el modo de desarrollador](media/updateAndSecurity.png)

    > <span data-ttu-id="b476b-116">El requisito para habilitar el modo de programador era [quitado en Windows 10 Fall Creators Update](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)</span><span class="sxs-lookup"><span data-stu-id="b476b-116">The requirement to enable Developer Mode was [removed in Windows 10 Fall Creators Update](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)</span></span>

1. <span data-ttu-id="b476b-117">Abra un símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="b476b-117">Open a command prompt.</span></span>  <span data-ttu-id="b476b-118">Tipo `bash` y presione ENTRAR</span><span class="sxs-lookup"><span data-stu-id="b476b-118">Type `bash` and hit enter</span></span>

    <span data-ttu-id="b476b-119">La primera vez que ejecuta Bash en Ubuntu en Windows, se pedirá que acepte la licencia de Canonical.</span><span class="sxs-lookup"><span data-stu-id="b476b-119">The first time you run Bash on Ubuntu on Windows, you'll be prompted to accept Canonical's license.</span></span> <span data-ttu-id="b476b-120">Una vez aceptado, WSL descargará e instalará la instancia de Ubuntu en su máquina y se agregará un acceso directo de "Bash en Ubuntu en Windows" en el menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="b476b-120">Once accepted, WSL will download and install the Ubuntu instance onto your machine, and a "Bash on Ubuntu on Windows" shortcut will be added to your start menu.</span></span>

    ![Símbolo del sistema para la instalación de Ubuntu](media/bashShellInstall.png)

    <span data-ttu-id="b476b-122">La primera vez que ejecuta Bash en Ubuntu en Windows, se le indicará que cree un nombre de usuario de UNIX y una contraseña.</span><span class="sxs-lookup"><span data-stu-id="b476b-122">The first time you run Bash on Ubuntu on Windows, you will be prompted to create a UNIX username and password.</span></span> <span data-ttu-id="b476b-123">Siga el [nuevas instrucciones de la instancia de distribución](initialize-distro.md) para completar la instalación</span><span class="sxs-lookup"><span data-stu-id="b476b-123">Follow the [new distro instance instructions](initialize-distro.md) to complete your installation</span></span>

1. <span data-ttu-id="b476b-124">Iniciar un nuevo shell de Ubuntu, ya sea:</span><span class="sxs-lookup"><span data-stu-id="b476b-124">Launch a new Ubuntu shell by either:</span></span>
    * <span data-ttu-id="b476b-125">Ejecutando `bash` desde un símbolo</span><span class="sxs-lookup"><span data-stu-id="b476b-125">Running `bash` from a command-prompt</span></span>
    * <span data-ttu-id="b476b-126">Al hacer clic en el acceso directo "Bash en Ubuntu en Windows" del menú Inicio</span><span class="sxs-lookup"><span data-stu-id="b476b-126">Clicking the start menu "Bash on Ubuntu on Windows" shortcut</span></span>

    
## <a name="uninstallingremoving-the-legacy-distro"></a><span data-ttu-id="b476b-127">Desinstalando o quitando la distribución heredada</span><span class="sxs-lookup"><span data-stu-id="b476b-127">Uninstalling/Removing the legacy distro</span></span>
<span data-ttu-id="b476b-128">Si actualiza desde una versión anterior de Windows 10 en el que instaló WSL para Windows 10 Fall Creators Update, la distribución existente permanecerá intacta.</span><span class="sxs-lookup"><span data-stu-id="b476b-128">If you upgrade to Windows 10 Fall Creators Update from an earlier Windows 10 release upon which you installed WSL, your existing distro will remain intact.</span></span> <span data-ttu-id="b476b-129">Sin embargo, nos FUERTEMENTE recomienda instalar una distribución nueva entrega de Store ASAP y migrar los archivos necesarios, datos, etc. de su distribución heredada a la distribución nuevo.</span><span class="sxs-lookup"><span data-stu-id="b476b-129">However, we STRONGLY encourage you to install a new Store-delivered distro ASAP, and migrate any necessary files, data, etc. from your legacy distro to your new distro.</span></span>

<span data-ttu-id="b476b-130">Para quitar la distribución heredada de la máquina, ejecute lo siguiente desde una instancia de la línea de comandos o PowerShell:</span><span class="sxs-lookup"><span data-stu-id="b476b-130">To remove the legacy distro from your machine, run the following from a Command Line or PowerShell instance:</span></span>

```console
lxrun /uninstall /full
```

### <a name="manually-deleting-the-legacy-distro"></a><span data-ttu-id="b476b-131">Eliminación manual de la distribución heredada</span><span class="sxs-lookup"><span data-stu-id="b476b-131">Manually deleting the legacy distro</span></span>
<span data-ttu-id="b476b-132">Si lo desea, puede eliminar manualmente la instancia antigua.</span><span class="sxs-lookup"><span data-stu-id="b476b-132">If you wish, you can manually delete your legacy instance.</span></span> <span data-ttu-id="b476b-133">Esto puede ser necesario si tiene problemas al desinstalar la distribución heredada utilizando `lxrun.exe`, o se está ejecutando Windows 10 Spring 2018 Update (o posterior) que no se suministran con `lxrun.exe`.</span><span class="sxs-lookup"><span data-stu-id="b476b-133">This may be required if you encounter issues uninstalling the legacy distro using `lxrun.exe`, or are running Windows 10 Spring 2018 Update (or later) which do not ship with `lxrun.exe`.</span></span>

<span data-ttu-id="b476b-134">Para forzar la eliminación de la distribución WSL heredada, eliminar el `%localappdata%\lxss\` carpeta (y todos los de subcontenido) mediante el Explorador de archivos de Windows o la línea de comandos:</span><span class="sxs-lookup"><span data-stu-id="b476b-134">To forcefully delete your legacy WSL distro, delete the `%localappdata%\lxss\` folder (and all it's sub-contents) using Windows' File Explorer, or the command-line:</span></span>

<span data-ttu-id="b476b-135">Con PowerShell</span><span class="sxs-lookup"><span data-stu-id="b476b-135">Using PowerShell</span></span>
```powershell
rm -Recurse $env:localappdata/lxss/
```

<span data-ttu-id="b476b-136">Uso de Cmd:</span><span class="sxs-lookup"><span data-stu-id="b476b-136">Using Cmd:</span></span>
```console
DEL /S %localappdata%\lxss\
```
