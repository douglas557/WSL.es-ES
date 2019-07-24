---
title: Instalar o quitar en la actualización de aniversario de Windows 10 o en Creators Update
description: Instrucciones de instalación y desinstalación de la versión de distribución de la actualización de aniversario de Windows 10
keywords: BashOnWindows, bash, WSL, Windows, subsistema de Windows para Linux, windowssubsystem, Ubuntu, Debian, SuSE, Windows 10, heredado, beta, instalar, quitar, desinstalar, desinstalar, eliminar, desusado
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 0d8fdabd61fadbfc58549a220ead23585a3d3656
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499265"
---
# <a name="guide-to-install-or-uninstall-windows-subsystem-for-linux-on-windows-10-anniversary-update-and-creators-update"></a><span data-ttu-id="a9205-104">Guía para instalar o desinstalar el subsistema de Windows para Linux en la actualización de aniversario de Windows 10 y Creators Update</span><span class="sxs-lookup"><span data-stu-id="a9205-104">Guide to install or uninstall Windows Subsystem for Linux on Windows 10 Anniversary Update and Creators Update</span></span> 

<span data-ttu-id="a9205-105">Si está ejecutando Windows 10 Creators Update o una versión posterior, [siga las instrucciones de instalación de Windows 10](install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="a9205-105">If you're running Windows 10 Creators Update or later, please [follow the Windows 10 installation instructions](install-win10.md).</span></span>

<span data-ttu-id="a9205-106"><strong><em><span style="color: #f28014">Las siguientes instrucciones son para los usuarios que ejecutan la actualización de aniversario de Windows 10 o Windows 10 Creators Update.</span></em></strong></span><span class="sxs-lookup"><span data-stu-id="a9205-106"><strong><em><span style="color: #f28014">The following instructions are for users running Windows 10 Anniversary Update or Windows 10 Creators Update</span></em></strong></span></span>

<span data-ttu-id="a9205-107">Antes de Windows 10 Fall Creators Update (versión 1709), WSL se lanzó como una característica beta e instaló una única instancia de Ubuntu cuando se ejecutó por primera vez "bash en Ubuntu en Windows" (o bash. exe).</span><span class="sxs-lookup"><span data-stu-id="a9205-107">Prior to Windows 10 Fall Creators Update (version 1709), WSL was released as a beta feature and installed a single Ubuntu instance when "Bash on Ubuntu on Windows" (or Bash.exe) was first run.</span></span>

> <span data-ttu-id="a9205-108">Aunque puede usar WSL en versiones anteriores de Windows 10, esta versión beta "Legacy distribución" ahora se considera obsoleta.</span><span class="sxs-lookup"><span data-stu-id="a9205-108">While you CAN use WSL on earlier Windows 10 releases, this beta "legacy distro" is now considered obsolete.</span></span> <span data-ttu-id="a9205-109">Le recomendamos encarecidamente que ejecute la versión más reciente de Windows 10 disponible.</span><span class="sxs-lookup"><span data-stu-id="a9205-109">We strongly encourage you to run the most recent version of Windows 10 available.</span></span> <span data-ttu-id="a9205-110">Cada nueva versión de Windows 10 incluye muchos cientos de correcciones y mejoras en WSL por sí solo, lo que permite que haya más aplicaciones y herramientas de Linux que se ejecuten correctamente en WSL.</span><span class="sxs-lookup"><span data-stu-id="a9205-110">Each new Windows 10 release includes many hundreds of fixes and improvements in WSL alone, allowing ever more Linux tools and apps to run correctly on WSL.</span></span>

<span data-ttu-id="a9205-111">Si no puede actualizar a Fall Creators Update o posterior, siga estos pasos para habilitar y usar WSL:</span><span class="sxs-lookup"><span data-stu-id="a9205-111">If you cannot upgrade to Fall Creators Update or later, follow the steps below to enable and use WSL:</span></span>

1. <span data-ttu-id="a9205-112">Activar el modo de desarrollador para ejecutar WSL en la actualización de aniversario de Windows 10 o en Creators Update, debe habilitar el modo de Desarrollador:</span><span class="sxs-lookup"><span data-stu-id="a9205-112">Turn on Developer Mode  To run WSL on Windows 10 Anniversary Update or Creators Update, you must enable Developer Mode:</span></span>

    <span data-ttu-id="a9205-113">Abrir **configuración** -> **actualizar y seguridad** -> **para desarrolladores**</span><span class="sxs-lookup"><span data-stu-id="a9205-113">Open **Settings** -> **Update and Security** -> **For developers**</span></span>

    <span data-ttu-id="a9205-114">Seleccionar el botón de radio modo de desarrollador</span><span class="sxs-lookup"><span data-stu-id="a9205-114">Select the Developer Mode radio button</span></span>  
    ![Habilitar el modo de desarrollador](media/updateAndSecurity.png)

    > <span data-ttu-id="a9205-116">El requisito de habilitar el modo de desarrollador se [quitó en Windows 10 Fall Creators Update](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)</span><span class="sxs-lookup"><span data-stu-id="a9205-116">The requirement to enable Developer Mode was [removed in Windows 10 Fall Creators Update](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)</span></span>

1. <span data-ttu-id="a9205-117">Abra un símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="a9205-117">Open a command prompt.</span></span>  <span data-ttu-id="a9205-118">Escriba `bash` y presione Entrar</span><span class="sxs-lookup"><span data-stu-id="a9205-118">Type `bash` and hit enter</span></span>

    <span data-ttu-id="a9205-119">La primera vez que ejecute bash en Ubuntu en Windows, se le pedirá que acepte la licencia de Canonical.</span><span class="sxs-lookup"><span data-stu-id="a9205-119">The first time you run Bash on Ubuntu on Windows, you'll be prompted to accept Canonical's license.</span></span> <span data-ttu-id="a9205-120">Una vez aceptado, WSL descargará e instalará la instancia de Ubuntu en el equipo y se agregará un acceso directo "Bash on Ubuntu on Windows" al menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="a9205-120">Once accepted, WSL will download and install the Ubuntu instance onto your machine, and a "Bash on Ubuntu on Windows" shortcut will be added to your start menu.</span></span>

    ![Preguntar para instalar Ubuntu](media/bashShellInstall.png)

    <span data-ttu-id="a9205-122">La primera vez que ejecute bash en Ubuntu en Windows, se le pedirá que cree un nombre de usuario y una contraseña de UNIX.</span><span class="sxs-lookup"><span data-stu-id="a9205-122">The first time you run Bash on Ubuntu on Windows, you will be prompted to create a UNIX username and password.</span></span> <span data-ttu-id="a9205-123">Siga las [instrucciones de la nueva instancia de distribución](initialize-distro.md) para completar la instalación.</span><span class="sxs-lookup"><span data-stu-id="a9205-123">Follow the [new distro instance instructions](initialize-distro.md) to complete your installation</span></span>

1. <span data-ttu-id="a9205-124">Inicie un nuevo shell de Ubuntu:</span><span class="sxs-lookup"><span data-stu-id="a9205-124">Launch a new Ubuntu shell by either:</span></span>
    * <span data-ttu-id="a9205-125">Ejecutar `bash` desde un símbolo del sistema</span><span class="sxs-lookup"><span data-stu-id="a9205-125">Running `bash` from a command-prompt</span></span>
    * <span data-ttu-id="a9205-126">Hacer clic en el acceso directo del menú Inicio "Bash on Ubuntu on Windows"</span><span class="sxs-lookup"><span data-stu-id="a9205-126">Clicking the start menu "Bash on Ubuntu on Windows" shortcut</span></span>

    
## <a name="uninstallingremoving-the-legacy-distro"></a><span data-ttu-id="a9205-127">Desinstalación/eliminación del distribución heredado</span><span class="sxs-lookup"><span data-stu-id="a9205-127">Uninstalling/Removing the legacy distro</span></span>
<span data-ttu-id="a9205-128">Si actualiza a Windows 10 Fall Creators Update desde una versión anterior de Windows 10 en la que instaló WSL, el distribución existente permanecerá intacto.</span><span class="sxs-lookup"><span data-stu-id="a9205-128">If you upgrade to Windows 10 Fall Creators Update from an earlier Windows 10 release upon which you installed WSL, your existing distro will remain intact.</span></span> <span data-ttu-id="a9205-129">Sin embargo, le recomendamos ENCARECIdamente que instale una nueva tienda (distribución ASAP) y migre los archivos, los datos, etc. que sean necesarios de su distribución heredado a la nueva distribución.</span><span class="sxs-lookup"><span data-stu-id="a9205-129">However, we STRONGLY encourage you to install a new Store-delivered distro ASAP, and migrate any necessary files, data, etc. from your legacy distro to your new distro.</span></span>

<span data-ttu-id="a9205-130">Para quitar el distribución heredado de la máquina, ejecute lo siguiente desde una línea de comandos o una instancia de PowerShell:</span><span class="sxs-lookup"><span data-stu-id="a9205-130">To remove the legacy distro from your machine, run the following from a Command Line or PowerShell instance:</span></span>

```console
wsl --unregister Legacy
```

<span data-ttu-id="a9205-131">Si no usa la versión 1903 o posterior de Windows, es posible que deba ejecutar `wslconfig /u Legacy` o `lxrun /uninstall /full` en su lugar.</span><span class="sxs-lookup"><span data-stu-id="a9205-131">If you are not using Windows Version 1903 or higher, you may need to run `wslconfig /u Legacy` or `lxrun /uninstall /full` instead.</span></span> 

### <a name="manually-deleting-the-legacy-distro"></a><span data-ttu-id="a9205-132">Eliminar manualmente el distribución heredado</span><span class="sxs-lookup"><span data-stu-id="a9205-132">Manually deleting the legacy distro</span></span>
<span data-ttu-id="a9205-133">Si lo desea, puede eliminar manualmente la instancia heredada.</span><span class="sxs-lookup"><span data-stu-id="a9205-133">If you wish, you can manually delete your legacy instance.</span></span> <span data-ttu-id="a9205-134">Esto puede ser necesario si se producen problemas al desinstalar el distribución heredado `lxrun.exe`mediante o si se ejecuta Windows 10 Spring 2018 Update (o una versión posterior) que no `lxrun.exe`se distribuyen con.</span><span class="sxs-lookup"><span data-stu-id="a9205-134">This may be required if you encounter issues uninstalling the legacy distro using `lxrun.exe`, or are running Windows 10 Spring 2018 Update (or later) which do not ship with `lxrun.exe`.</span></span>

<span data-ttu-id="a9205-135">Para forzar la eliminación de la distribución de WSL heredada, elimine la `%localappdata%\lxss\` carpeta (y todo su subcontenido) mediante el explorador de archivos de Windows o la línea de comandos:</span><span class="sxs-lookup"><span data-stu-id="a9205-135">To forcefully delete your legacy WSL distro, delete the `%localappdata%\lxss\` folder (and all it's sub-contents) using Windows' File Explorer, or the command-line:</span></span>

<span data-ttu-id="a9205-136">Con PowerShell</span><span class="sxs-lookup"><span data-stu-id="a9205-136">Using PowerShell</span></span>
```powershell
rm -Recurse $env:localappdata/lxss/
```

<span data-ttu-id="a9205-137">Mediante cmd:</span><span class="sxs-lookup"><span data-stu-id="a9205-137">Using Cmd:</span></span>
```console
DEL /S %localappdata%\lxss\
```
