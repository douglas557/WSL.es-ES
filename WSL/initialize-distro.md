---
title: Inicialización de una nueva distribución de WSL Linux
description: Después de instalar una distribución de Linux para WSL, sigue estos sencillos pasos para completar la inicialización.
keywords: BashOnWindows, bash, wsl, wsl2, windows, subsistema de windows para linux, windowssubsystem, ubuntu, debian, suse, windows 10
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: c33d349a6d39c325b079ccbf7ed6350bed796e33
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269590"
---
# <a name="initializing-a-newly-installed-distro"></a><span data-ttu-id="4176c-104">Inicialización de una distribución recién instalada</span><span class="sxs-lookup"><span data-stu-id="4176c-104">Initializing a newly installed distro</span></span>
<span data-ttu-id="4176c-105">Una vez que se haya descargado e instalado la distribución, deberás completar la inicialización de la nueva distribución:</span><span class="sxs-lookup"><span data-stu-id="4176c-105">Once your distro has been downloaded and installed, you'll need to complete initialization of the new distro:</span></span>

## <a name="launch-a-distro"></a><span data-ttu-id="4176c-106">Inicio de una distribución</span><span class="sxs-lookup"><span data-stu-id="4176c-106">Launch a distro</span></span>
<span data-ttu-id="4176c-107">Para completar la inicialización de la distribución recién instalada, inicia una nueva instancia.</span><span class="sxs-lookup"><span data-stu-id="4176c-107">To complete the initialization of your newly installed distro, launch a new instance.</span></span> <span data-ttu-id="4176c-108">Para ello, haz clic en el botón "Iniciar" en la aplicación Microsoft Store o inicia la distribución desde el menú Inicio:</span><span class="sxs-lookup"><span data-stu-id="4176c-108">You can do this by clicking the "launch" button in the Microsoft Store app, or launching the distro from the Start menu:</span></span>

> <span data-ttu-id="4176c-109">Sugerencia: Es posible que quieras anclar las distribuciones que se usan con más frecuencia en el menú Inicio o en la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="4176c-109">Tip: You might want to pin your most frequently used distros to your Start menu, and/or to your taskbar!</span></span>

![Inicio de las distribuciones desde el menú Inicio](media/start-menu.png)

> <span data-ttu-id="4176c-111">En Windows Server, puedes iniciar el archivo ejecutable `<distro>.exe` del iniciador de distribuciones desde la carpeta de instalación de distribuciones.</span><span class="sxs-lookup"><span data-stu-id="4176c-111">On Windows Server, you can launch your distro's launcher executable `<distro>.exe` from the distro installation folder.</span></span>

<span data-ttu-id="4176c-112">La primera vez que se ejecute una distribución recién instalada, se abrirá una ventana de consola y se te pedirá que esperes un minuto o dos para que se complete la instalación.</span><span class="sxs-lookup"><span data-stu-id="4176c-112">The first time a newly installed distro runs, a Console window will open, and you'll be asked to wait for a minute or two for the installation to complete.</span></span>

> <span data-ttu-id="4176c-113">Durante esta fase final de la instalación, los archivos de la distribución se descomprimen y almacenan en el equipo, listos para usarse.</span><span class="sxs-lookup"><span data-stu-id="4176c-113">During this final stage of installation, the distro's files are de-compressed and stored on your PC, ready for use.</span></span> <span data-ttu-id="4176c-114">Esta acción puede tardar aproximadamente un minuto o más en función del rendimiento de los dispositivos de almacenamiento del equipo.</span><span class="sxs-lookup"><span data-stu-id="4176c-114">This may take around a minute or more depending on the performance of your PC's storage devices.</span></span> <span data-ttu-id="4176c-115">Esta fase de instalación inicial solo es necesaria cuando una distribución se instala sin problemas; todos los inicios futuros deben tardar menos de un segundo.</span><span class="sxs-lookup"><span data-stu-id="4176c-115">This initial installation phase is only required when a distro is clean-installed - all future launches should take less than a second.</span></span>

## <a name="setting-up-a-new-linux-user-account"></a><span data-ttu-id="4176c-116">Configuración de una nueva cuenta de usuario de Linux</span><span class="sxs-lookup"><span data-stu-id="4176c-116">Setting up a new Linux user account</span></span>

<span data-ttu-id="4176c-117">Una vez completada la instalación, se te pedirá que crees una nueva cuenta de usuario (y su contraseña).</span><span class="sxs-lookup"><span data-stu-id="4176c-117">Once installation is complete, you will be prompted to create a new user account (and its password).</span></span> 

![Desempaquetado de Ubuntu en la consola de Windows](media/UbuntuInstall.png)

<span data-ttu-id="4176c-119">Esta cuenta de usuario es para el usuario normal sin privilegios de administrador según el que se iniciará sesión de manera predeterminada al iniciar una distribución.</span><span class="sxs-lookup"><span data-stu-id="4176c-119">This user account is for the normal non-admin user that you'll be logged-in as by default when launching a distro.</span></span>

> <span data-ttu-id="4176c-120">Puedes elegir cualquier nombre de usuario y contraseña: no tienen ninguna relación con el nombre de usuario de Windows.</span><span class="sxs-lookup"><span data-stu-id="4176c-120">You can choose any username and password you wish - they have no bearing on your Windows username.</span></span> 

<span data-ttu-id="4176c-121">Cuando abras una nueva instancia de distribución, no se te pedirá la contraseña, pero, **si elevas un proceso mediante `sudo`, tendrás que escribir la contraseña**, por lo que debes asegurarte de elegir una contraseña que puedas recordar fácilmente.</span><span class="sxs-lookup"><span data-stu-id="4176c-121">When you open a new distro instance, you won't be prompted for your password, but **if you elevate a process using `sudo`, you will need to enter your password**, so make sure you choose a password you can easily remember!</span></span> <span data-ttu-id="4176c-122">Para obtener más información, consulta la página de [Soporte del usuario](user-support.md).</span><span class="sxs-lookup"><span data-stu-id="4176c-122">See the [User Support](user-support.md) page for more info.</span></span>

## <a name="update--upgrade-your-distros-packages"></a><span data-ttu-id="4176c-123">Actualización de los paquetes de la distribución</span><span class="sxs-lookup"><span data-stu-id="4176c-123">Update & upgrade your distro's packages</span></span>

<span data-ttu-id="4176c-124">La mayoría de distribuciones se distribuyen con un catálogo de paquetes vacío o mínimo.</span><span class="sxs-lookup"><span data-stu-id="4176c-124">Most distros ship with an empty/minimal package catalog.</span></span> <span data-ttu-id="4176c-125">Se recomienda encarecidamente actualizar periódicamente el catálogo de paquetes, así como actualizar los paquetes instalados con el administrador de paquetes preferido de la distribución.</span><span class="sxs-lookup"><span data-stu-id="4176c-125">We strongly recommend regularly updating your package catalog, and upgrading your installed packages using your distro's preferred package manager.</span></span> <span data-ttu-id="4176c-126">En Debian y Ubuntu, se usa apt:</span><span class="sxs-lookup"><span data-stu-id="4176c-126">On Debian/Ubuntu, you use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

> <span data-ttu-id="4176c-127">Windows no se actualiza automáticamente ni actualiza las distribuciones de Linux: Se trata de una tarea que los usuarios de Linux prefieren controlar.</span><span class="sxs-lookup"><span data-stu-id="4176c-127">Windows does not automatically update or upgrade your Linux distro(s): This is a task that the Linux users prefer to control themselves.</span></span>

<span data-ttu-id="4176c-128">Has terminado.</span><span class="sxs-lookup"><span data-stu-id="4176c-128">You're done!</span></span> <span data-ttu-id="4176c-129">Disfruta con la nueva distribución de Linux en WSL.</span><span class="sxs-lookup"><span data-stu-id="4176c-129">Enjoy using your new Linux distro on WSL!</span></span> <span data-ttu-id="4176c-130">Para obtener más información sobre WSL, revisa los otros [documentos de WSL](https://aka.ms/wsldocs) o la [página de recursos de aprendizaje de WSL](https://aka.ms/learnwsl).</span><span class="sxs-lookup"><span data-stu-id="4176c-130">To learn more about WSL, review the other [WSL docs](https://aka.ms/wsldocs), or the [WSL learning resources page](https://aka.ms/learnwsl).</span></span>

![Disfruta del uso de Linux en WSL.](media/linux-on-wsl.png)

## <a name="troubleshooting"></a><span data-ttu-id="4176c-132">Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="4176c-132">Troubleshooting</span></span>

<span data-ttu-id="4176c-133">A continuación, se muestran errores relacionados y las correcciones sugeridas.</span><span class="sxs-lookup"><span data-stu-id="4176c-133">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="4176c-134">Consulta la [página de solución de problemas de WSL](troubleshooting.md) para ver otros errores generales y sus soluciones.</span><span class="sxs-lookup"><span data-stu-id="4176c-134">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

> <span data-ttu-id="4176c-135">**Error 0x8007007e en la instalación**: este error se produce cuando el sistema no es compatible con Linux desde Store.</span><span class="sxs-lookup"><span data-stu-id="4176c-135">**Installation failed with error 0x8007007e** This error occurs when your system doesn't support Linux from the store.</span></span>  <span data-ttu-id="4176c-136">Asegúrese de que:</span><span class="sxs-lookup"><span data-stu-id="4176c-136">Make sure that:</span></span>
> * <span data-ttu-id="4176c-137">Estás ejecutando la compilación 16215 de Windows o una posterior.</span><span class="sxs-lookup"><span data-stu-id="4176c-137">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="4176c-138">[Comprueba el número de compilación](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="4176c-138">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
> * <span data-ttu-id="4176c-139">El componente opcional del subsistema de Windows para Linux está habilitado y se ha reiniciado el equipo.</span><span class="sxs-lookup"><span data-stu-id="4176c-139">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="4176c-140">[Asegúrate de que WSL está habilitado](troubleshooting.md#confirm-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="4176c-140">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
