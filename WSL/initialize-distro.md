---
title: Inicializar una nueva distribución de Linux de WSL
description: Después de instalar una distribución de Linux para WSL, completar la inicialización siguiendo estos sencillos pasos
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, windowssubsystem, ubuntu, debian, suse, windows 10
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 7f1ce521b248c873fa7f81c6363eb506c0363fed
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2019
ms.locfileid: "59902052"
---
# <a name="initializing-a-newly-installed-distro"></a><span data-ttu-id="1ad1e-104">Inicializar una distribución recién instalada</span><span class="sxs-lookup"><span data-stu-id="1ad1e-104">Initializing a newly installed distro</span></span>
<span data-ttu-id="1ad1e-105">Una vez que se ha descargado e instalado la distribución, deberá completar la inicialización de la distribución de nuevo:</span><span class="sxs-lookup"><span data-stu-id="1ad1e-105">Once your distro has been downloaded and installed, you'll need to complete initialization of the new distro:</span></span>

## <a name="launch-a-distro"></a><span data-ttu-id="1ad1e-106">Iniciar una distribución</span><span class="sxs-lookup"><span data-stu-id="1ad1e-106">Launch a distro</span></span>
<span data-ttu-id="1ad1e-107">Para completar la inicialización de la distribución recién instalada, inicie una nueva instancia.</span><span class="sxs-lookup"><span data-stu-id="1ad1e-107">To complete the initialization of your newly installed distro, launch a new instance.</span></span> <span data-ttu-id="1ad1e-108">Puede hacerlo haciendo clic con el botón "iniciar" en la aplicación de Windows Store o iniciando la distribución en el menú Inicio:</span><span class="sxs-lookup"><span data-stu-id="1ad1e-108">You can do this by clicking the "launch" button in the Windows Store app, or launching the distro from the Start menu:</span></span>

> <span data-ttu-id="1ad1e-109">Sugerencia: Es posible que desea anclar sus distribuciones utilizadas con frecuencia al menú Inicio o en la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="1ad1e-109">Tip: You might want to pin your most frequently used distros to your Start menu, and/or to your taskbar!</span></span>

![Iniciar distribuciones desde el menú Inicio](media/start-menu.png)

> <span data-ttu-id="1ad1e-111">En Windows Server, puede iniciar el selector de la distribución ejecutable `<distro>.exe` desde la carpeta de instalación de distribución.</span><span class="sxs-lookup"><span data-stu-id="1ad1e-111">On Windows Server, you can launch your distro's launcher executable `<distro>.exe` from the distro installation folder.</span></span>

<span data-ttu-id="1ad1e-112">La primera vez que ejecuta una distribución recién instalada, una consola se abrirá la ventana, y le pedirá que espere un minuto o dos para que se complete la instalación.</span><span class="sxs-lookup"><span data-stu-id="1ad1e-112">The first time a newly installed distro runs, a Console window will open, and you'll be asked to wait for a minute or two for the installation to complete.</span></span>

> <span data-ttu-id="1ad1e-113">Durante esta fase final de la instalación, los archivos de la distribución están anular comprimidos y almacenados en su PC, listo para su uso.</span><span class="sxs-lookup"><span data-stu-id="1ad1e-113">During this final stage of installation, the distro's files are de-compressed and stored on your PC, ready for use.</span></span> <span data-ttu-id="1ad1e-114">Esta operación puede tardar alrededor de un minuto o más dependiendo del rendimiento de los dispositivos de almacenamiento de su PC.</span><span class="sxs-lookup"><span data-stu-id="1ad1e-114">This may take around a minute or more depending on the performance of your PC's storage devices.</span></span> <span data-ttu-id="1ad1e-115">Esta fase inicial de la instalación sólo es necesario cuando una distribución es la instalación completa de todas las versiones futuras tardará menos de un segundo.</span><span class="sxs-lookup"><span data-stu-id="1ad1e-115">This initial installation phase is only required when a distro is clean-installed - all future launches should take less than a second.</span></span>

## <a name="setting-up-a-new-linux-user-account"></a><span data-ttu-id="1ad1e-116">Configurar una nueva cuenta de usuario de Linux</span><span class="sxs-lookup"><span data-stu-id="1ad1e-116">Setting up a new Linux user account</span></span>

<span data-ttu-id="1ad1e-117">Una vez completada la instalación, se le pedirá que cree una nueva cuenta de usuario (y su contraseña).</span><span class="sxs-lookup"><span data-stu-id="1ad1e-117">Once installation is complete, you will be prompted to create a new user account (and its password).</span></span> 

![Ubuntu desempaquetar en la consola de Windows](media/UbuntuInstall.png)

<span data-ttu-id="1ad1e-119">Esta cuenta de usuario es para el usuario no administrador normal que se convertirá ha iniciado sesión como de forma predeterminada al iniciar una distribución.</span><span class="sxs-lookup"><span data-stu-id="1ad1e-119">This user account is for the normal non-admin user that you'll be logged-in as by default when launching a distro.</span></span>

> <span data-ttu-id="1ad1e-120">Puede elegir cualquier nombre de usuario y contraseña que desee: no tiene ningún efecto en su nombre de usuario de Windows.</span><span class="sxs-lookup"><span data-stu-id="1ad1e-120">You can choose any username and password you wish - they have no bearing on your Windows username.</span></span> 

<span data-ttu-id="1ad1e-121">Cuando se abre una nueva instancia de la distribución, no se le pedirán la contraseña, pero **si elevar un proceso usando `sudo`, tendrá que escribir la contraseña**, por lo que asegúrese de que elige una contraseña que pueda recordar fácilmente!</span><span class="sxs-lookup"><span data-stu-id="1ad1e-121">When you open a new distro instance, you won't be prompted for your password, but **if you elevate a process using `sudo`, you will need to enter your password**, so make sure you choose a password you can easily remember!</span></span> <span data-ttu-id="1ad1e-122">Consulte la [soporte técnico de usuario](user-support.md) página para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="1ad1e-122">See the [User Support](user-support.md) page for more info.</span></span>

## <a name="update--upgrade-your-distros-packages"></a><span data-ttu-id="1ad1e-123">Actualizar & actualizar los paquetes de la distribución</span><span class="sxs-lookup"><span data-stu-id="1ad1e-123">Update & upgrade your distro's packages</span></span>

<span data-ttu-id="1ad1e-124">La mayoría de las distribuciones se distribuyen con un catálogo de paquete mínimo/vacío.</span><span class="sxs-lookup"><span data-stu-id="1ad1e-124">Most distros ship with an empty/minimal package catalog.</span></span> <span data-ttu-id="1ad1e-125">Se recomienda encarecidamente actualizar con regularidad el catálogo de paquetes y actualizar los paquetes instalados con el Administrador de paquetes preferido de su distribución.</span><span class="sxs-lookup"><span data-stu-id="1ad1e-125">We strongly recommend regularly updating your package catalog, and upgrading your installed packages using your distro's preferred package manager.</span></span> <span data-ttu-id="1ad1e-126">En Debian y Ubuntu, usa apt:</span><span class="sxs-lookup"><span data-stu-id="1ad1e-126">On Debian/Ubuntu, you use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

> <span data-ttu-id="1ad1e-127">Windows no actualizar automáticamente ni actualizar su distro(s) Linux: Esta es una tarea que prefieren los usuarios de Linux para controlar a sí mismos.</span><span class="sxs-lookup"><span data-stu-id="1ad1e-127">Windows does not automatically update or upgrade your Linux distro(s): This is a task that the Linux users prefer to control themselves.</span></span>

<span data-ttu-id="1ad1e-128">¡Has terminado!</span><span class="sxs-lookup"><span data-stu-id="1ad1e-128">You're done!</span></span> <span data-ttu-id="1ad1e-129">Disfrute de uso de la nueva distribución de Linux en WSL.</span><span class="sxs-lookup"><span data-stu-id="1ad1e-129">Enjoy using your new Linux distro on WSL!</span></span> <span data-ttu-id="1ad1e-130">Para obtener más información acerca de WSL, revise el otro [docs WSL](https://aka.ms/wsldocs), o el [WSL página de recursos de aprendizaje](https://aka.ms/learnwsl).</span><span class="sxs-lookup"><span data-stu-id="1ad1e-130">To learn more about WSL, review the other [WSL docs](https://aka.ms/wsldocs), or the [WSL learning resources page](https://aka.ms/learnwsl).</span></span>

![Disfrute con Linux en WSL](media/linux-on-wsl.png)

## <a name="troubleshooting"></a><span data-ttu-id="1ad1e-132">Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="1ad1e-132">Troubleshooting</span></span>

<span data-ttu-id="1ad1e-133">A continuación se muestran errores relacionados y correcciones sugeridas.</span><span class="sxs-lookup"><span data-stu-id="1ad1e-133">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="1ad1e-134">Hacer referencia a la [página de solución de problemas de WSL](troubleshooting.md) para otros errores comunes y sus soluciones.</span><span class="sxs-lookup"><span data-stu-id="1ad1e-134">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

> <span data-ttu-id="1ad1e-135">**Error de instalación 0x8007007e** este error se produce cuando el sistema no es compatible con Linux desde el almacén.</span><span class="sxs-lookup"><span data-stu-id="1ad1e-135">**Installation failed with error 0x8007007e** This error occurs when your system doesn't support Linux from the store.</span></span>  <span data-ttu-id="1ad1e-136">Asegúrese de que:</span><span class="sxs-lookup"><span data-stu-id="1ad1e-136">Make sure that:</span></span>
> * <span data-ttu-id="1ad1e-137">Ya está ejecutando Windows compilación 16215 o posterior.</span><span class="sxs-lookup"><span data-stu-id="1ad1e-137">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="1ad1e-138">[Comprobar la compilación](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="1ad1e-138">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
> * <span data-ttu-id="1ad1e-139">El subsistema de Windows para el componente opcional de Linux está habilitado y ha reiniciado el equipo.</span><span class="sxs-lookup"><span data-stu-id="1ad1e-139">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="1ad1e-140">[Asegúrese de que está habilitado WSL](troubleshooting.md#confirm-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="1ad1e-140">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
