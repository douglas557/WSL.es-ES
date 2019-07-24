---
title: Inicialización de un nuevo distribución de WSL Linux
description: Después de instalar una distribución de Linux para WSL, complete la inicialización siguiendo estos sencillos pasos.
keywords: BashOnWindows, bash, WSL, Windows, subsistema de Windows para Linux, windowssubsystem, Ubuntu, Debian, SuSE, Windows 10
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 30cb1de0a01fd46bc434061cd36794f4ece77e4b
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499298"
---
# <a name="initializing-a-newly-installed-distro"></a><span data-ttu-id="852da-104">Inicialización de un distribución recién instalado</span><span class="sxs-lookup"><span data-stu-id="852da-104">Initializing a newly installed distro</span></span>
<span data-ttu-id="852da-105">Una vez que se haya descargado e instalado el distribución, deberá completar la inicialización del nuevo distribución:</span><span class="sxs-lookup"><span data-stu-id="852da-105">Once your distro has been downloaded and installed, you'll need to complete initialization of the new distro:</span></span>

## <a name="launch-a-distro"></a><span data-ttu-id="852da-106">Inicio de un distribución</span><span class="sxs-lookup"><span data-stu-id="852da-106">Launch a distro</span></span>
<span data-ttu-id="852da-107">Para completar la inicialización del distribución recién instalado, inicie una nueva instancia de.</span><span class="sxs-lookup"><span data-stu-id="852da-107">To complete the initialization of your newly installed distro, launch a new instance.</span></span> <span data-ttu-id="852da-108">Para ello, haga clic en el botón "iniciar" en la aplicación Microsoft Store o inicie el distribución desde el menú Inicio:</span><span class="sxs-lookup"><span data-stu-id="852da-108">You can do this by clicking the "launch" button in the Microsoft Store app, or launching the distro from the Start menu:</span></span>

> <span data-ttu-id="852da-109">Sugerencia: Es posible que quiera anclar el distribuciones que se usa con más frecuencia en el menú Inicio o en la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="852da-109">Tip: You might want to pin your most frequently used distros to your Start menu, and/or to your taskbar!</span></span>

![Iniciar distribuciones desde el menú Inicio](media/start-menu.png)

> <span data-ttu-id="852da-111">En Windows Server, puede iniciar el archivo ejecutable `<distro>.exe` del iniciador de distribución desde la carpeta de instalación de distribución.</span><span class="sxs-lookup"><span data-stu-id="852da-111">On Windows Server, you can launch your distro's launcher executable `<distro>.exe` from the distro installation folder.</span></span>

<span data-ttu-id="852da-112">La primera vez que se ejecuta un distribución recién instalado, se abrirá una ventana de consola y se le pedirá que espere un minuto o dos para que se complete la instalación.</span><span class="sxs-lookup"><span data-stu-id="852da-112">The first time a newly installed distro runs, a Console window will open, and you'll be asked to wait for a minute or two for the installation to complete.</span></span>

> <span data-ttu-id="852da-113">Durante esta fase final de la instalación, los archivos del distribución se descomprimen y almacenan en el equipo, listos para usarse.</span><span class="sxs-lookup"><span data-stu-id="852da-113">During this final stage of installation, the distro's files are de-compressed and stored on your PC, ready for use.</span></span> <span data-ttu-id="852da-114">Esto puede tardar aproximadamente un minuto o más en función del rendimiento de los dispositivos de almacenamiento de su equipo.</span><span class="sxs-lookup"><span data-stu-id="852da-114">This may take around a minute or more depending on the performance of your PC's storage devices.</span></span> <span data-ttu-id="852da-115">Esta fase de instalación inicial solo es necesaria cuando un distribución está instalado sin problemas; todos los lanzamientos futuros deben tardar menos de un segundo.</span><span class="sxs-lookup"><span data-stu-id="852da-115">This initial installation phase is only required when a distro is clean-installed - all future launches should take less than a second.</span></span>

## <a name="setting-up-a-new-linux-user-account"></a><span data-ttu-id="852da-116">Configuración de una nueva cuenta de usuario de Linux</span><span class="sxs-lookup"><span data-stu-id="852da-116">Setting up a new Linux user account</span></span>

<span data-ttu-id="852da-117">Una vez completada la instalación, se le pedirá que cree una nueva cuenta de usuario (y su contraseña).</span><span class="sxs-lookup"><span data-stu-id="852da-117">Once installation is complete, you will be prompted to create a new user account (and its password).</span></span> 

![Desempaquetar Ubuntu en la consola de Windows](media/UbuntuInstall.png)

<span data-ttu-id="852da-119">Esta cuenta de usuario es para el usuario normal sin privilegios de administrador en el que se iniciará sesión como de forma predeterminada al iniciar un distribución.</span><span class="sxs-lookup"><span data-stu-id="852da-119">This user account is for the normal non-admin user that you'll be logged-in as by default when launching a distro.</span></span>

> <span data-ttu-id="852da-120">Puede elegir cualquier nombre de usuario y contraseña que desee: no tienen ninguna relación con el nombre de usuario de Windows.</span><span class="sxs-lookup"><span data-stu-id="852da-120">You can choose any username and password you wish - they have no bearing on your Windows username.</span></span> 

<span data-ttu-id="852da-121">Cuando abra una nueva instancia de distribución, no se le pedirá la contraseña, pero **si eleva un proceso mediante `sudo`, tendrá que escribir la contraseña**, por lo que debe asegurarse de elegir una contraseña que pueda recordar fácilmente.</span><span class="sxs-lookup"><span data-stu-id="852da-121">When you open a new distro instance, you won't be prompted for your password, but **if you elevate a process using `sudo`, you will need to enter your password**, so make sure you choose a password you can easily remember!</span></span> <span data-ttu-id="852da-122">Para obtener más información, consulte la página de [soporte técnico del usuario](user-support.md) .</span><span class="sxs-lookup"><span data-stu-id="852da-122">See the [User Support](user-support.md) page for more info.</span></span>

## <a name="update--upgrade-your-distros-packages"></a><span data-ttu-id="852da-123">Actualizar & actualizar los paquetes de distribución</span><span class="sxs-lookup"><span data-stu-id="852da-123">Update & upgrade your distro's packages</span></span>

<span data-ttu-id="852da-124">La mayoría de distribuciones se distribuye con un catálogo de paquetes vacío o mínimo.</span><span class="sxs-lookup"><span data-stu-id="852da-124">Most distros ship with an empty/minimal package catalog.</span></span> <span data-ttu-id="852da-125">Se recomienda encarecidamente actualizar el catálogo de paquetes y actualizar los paquetes instalados con el administrador de paquetes preferido de su distribución.</span><span class="sxs-lookup"><span data-stu-id="852da-125">We strongly recommend regularly updating your package catalog, and upgrading your installed packages using your distro's preferred package manager.</span></span> <span data-ttu-id="852da-126">En Debian/Ubuntu, se usa apt:</span><span class="sxs-lookup"><span data-stu-id="852da-126">On Debian/Ubuntu, you use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

> <span data-ttu-id="852da-127">Windows no actualiza ni actualiza automáticamente los distribución de Linux: Se trata de una tarea que los usuarios de Linux prefieren controlar.</span><span class="sxs-lookup"><span data-stu-id="852da-127">Windows does not automatically update or upgrade your Linux distro(s): This is a task that the Linux users prefer to control themselves.</span></span>

<span data-ttu-id="852da-128">¡Has terminado!</span><span class="sxs-lookup"><span data-stu-id="852da-128">You're done!</span></span> <span data-ttu-id="852da-129">Disfrute con el nuevo distribución de Linux en WSL.</span><span class="sxs-lookup"><span data-stu-id="852da-129">Enjoy using your new Linux distro on WSL!</span></span> <span data-ttu-id="852da-130">Para obtener más información sobre WSL, revise los otros [documentos de WSL](https://aka.ms/wsldocs)o la página de recursos de aprendizaje de [WSL](https://aka.ms/learnwsl).</span><span class="sxs-lookup"><span data-stu-id="852da-130">To learn more about WSL, review the other [WSL docs](https://aka.ms/wsldocs), or the [WSL learning resources page](https://aka.ms/learnwsl).</span></span>

![Disfrute del uso de Linux en WSL](media/linux-on-wsl.png)

## <a name="troubleshooting"></a><span data-ttu-id="852da-132">Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="852da-132">Troubleshooting</span></span>

<span data-ttu-id="852da-133">A continuación se muestran los errores relacionados y las correcciones sugeridas.</span><span class="sxs-lookup"><span data-stu-id="852da-133">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="852da-134">Consulte la [Página de solución de problemas de WSL](troubleshooting.md) para ver otros errores comunes y sus soluciones.</span><span class="sxs-lookup"><span data-stu-id="852da-134">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

> <span data-ttu-id="852da-135">Error **0x8007007e en la instalación** Este error se produce cuando el sistema no es compatible con Linux desde la tienda.</span><span class="sxs-lookup"><span data-stu-id="852da-135">**Installation failed with error 0x8007007e** This error occurs when your system doesn't support Linux from the store.</span></span>  <span data-ttu-id="852da-136">Asegúrese de que:</span><span class="sxs-lookup"><span data-stu-id="852da-136">Make sure that:</span></span>
> * <span data-ttu-id="852da-137">Está ejecutando Windows Build 16215 o posterior.</span><span class="sxs-lookup"><span data-stu-id="852da-137">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="852da-138">[Compruebe la compilación](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="852da-138">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
> * <span data-ttu-id="852da-139">El componente opcional de subsistema de Windows para Linux está habilitado y el equipo se ha reiniciado.</span><span class="sxs-lookup"><span data-stu-id="852da-139">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="852da-140">[Asegúrese de que WSL está habilitado](troubleshooting.md#confirm-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="852da-140">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
