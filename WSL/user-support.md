---
title: Permisos y la cuenta de usuario de Linux
description: Referencia de las cuentas de usuario y la administración de permisos con el subsistema de Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, windowssubsystem, ubuntu, cuentas de usuario
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.openlocfilehash: 0d00b43d059e72edd4e2a5b9591c29441f461fca
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040826"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a><span data-ttu-id="1a8fe-104">Las cuentas de usuario y los permisos para el subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="1a8fe-104">User Accounts and Permissions for Windows Subsystem for Linux</span></span>

<span data-ttu-id="1a8fe-105">Creación de su usuario de Linux es el primer paso para configurar una nueva distribución de Linux en WSL.</span><span class="sxs-lookup"><span data-stu-id="1a8fe-105">Creating your Linux user is the first step in setting up a new Linux distribution on WSL.</span></span>  <span data-ttu-id="1a8fe-106">La primera cuenta de usuario que cree se configura automáticamente con unos cuantos atributos especiales:</span><span class="sxs-lookup"><span data-stu-id="1a8fe-106">The first user account you create is automatically configured with a few special attributes:</span></span>

1. <span data-ttu-id="1a8fe-107">Es el usuario de forma predeterminada, inicia sesión automáticamente en el inicio.</span><span class="sxs-lookup"><span data-stu-id="1a8fe-107">It is your default user -- it signs-in automatically on launch.</span></span>
1. <span data-ttu-id="1a8fe-108">Es el Administrador de Linux (un miembro del grupo de sudo) de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1a8fe-108">It is Linux administrator (a member of the sudo group) by default.</span></span>

<span data-ttu-id="1a8fe-109">Cada distribución de Linux que se ejecuta en el subsistema de Windows para Linux tiene sus propias cuentas de usuario de Linux y las contraseñas.</span><span class="sxs-lookup"><span data-stu-id="1a8fe-109">Each Linux distribution running on the Windows Subsystem for Linux has its own Linux user accounts and passwords.</span></span>  <span data-ttu-id="1a8fe-110">Tendrá que configurar cada vez que agregue una distribución, vuelva a instalar o restablecimiento de una cuenta de usuario de Linux.</span><span class="sxs-lookup"><span data-stu-id="1a8fe-110">You will have to configure a Linux user account any time you add a distribution, reinstall, or reset.</span></span>  <span data-ttu-id="1a8fe-111">Cuentas de usuario de Linux no sólo son independientes por cada distribución, también son independientes de la cuenta de usuario de Windows.</span><span class="sxs-lookup"><span data-stu-id="1a8fe-111">Linux user accounts are not only independent per distribution, they are also independent from your Windows user account.</span></span>

## <a name="resetting-your-linux-password"></a><span data-ttu-id="1a8fe-112">Al restablecer la contraseña de Linux</span><span class="sxs-lookup"><span data-stu-id="1a8fe-112">Resetting your Linux password</span></span>

<span data-ttu-id="1a8fe-113">Si conoce la contraseña actual, cambiarla y tener acceso a su cuenta de usuario de Linux con Linux de restablecimiento de contraseña herramientas de distribución--probablemente `passwd`.</span><span class="sxs-lookup"><span data-stu-id="1a8fe-113">If you have access to your Linux user account and know your current password, change it using Linux password reset tools of that distribution -- most likely `passwd`.</span></span>

<span data-ttu-id="1a8fe-114">Si es no es una opción, dependiendo de la distribución, puede restablecer la contraseña, restablecer el usuario predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1a8fe-114">If that's not an option, depending on the distribution, you may be able to reset your password by resetting the default user.</span></span>

<span data-ttu-id="1a8fe-115">WSL proporciona una etiqueta de usuario predeterminada para identificar automáticamente la cuenta de usuario que inicia sesión cuando se inicia un WSL.</span><span class="sxs-lookup"><span data-stu-id="1a8fe-115">WSL offers a default user tag to identify which user account automatically logs in when you start a WSL.</span></span>  <span data-ttu-id="1a8fe-116">Puesto que muchas distribuciones incluyen los comandos para establecer el usuario predeterminado en la raíz y también un usuario raíz con ninguna contraseña establecida, cambiar el usuario predeterminado para la raíz es una herramienta útil para tareas como el restablecimiento de contraseña.</span><span class="sxs-lookup"><span data-stu-id="1a8fe-116">Since many distributions include commands to set the default user to root and also a root user with no password set, changing the default user to root is a handy tool for things like password reset.</span></span>

### <a name="for-creators-update-and-earlier"></a><span data-ttu-id="1a8fe-117">Creators Update y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="1a8fe-117">For Creators Update and earlier</span></span>
<span data-ttu-id="1a8fe-118">Si está ejecutando Windows 10 Creators update o versiones anteriores, puede cambiar el usuario de Bash predeterminado mediante la ejecución de los siguientes comandos:</span><span class="sxs-lookup"><span data-stu-id="1a8fe-118">If you're running Windows 10 Creators update or earlier, you can change the default Bash user by running the following commands:</span></span>

1. <span data-ttu-id="1a8fe-119">Cambiar el usuario predeterminado para `root`:</span><span class="sxs-lookup"><span data-stu-id="1a8fe-119">Change the default user to `root`:</span></span>

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. <span data-ttu-id="1a8fe-120">Ejecute `bash.exe` para iniciar sesión ahora como `root`:</span><span class="sxs-lookup"><span data-stu-id="1a8fe-120">Run `bash.exe` to now login as `root`:</span></span>

    ```console
    C:\> bash.exe
    ```

1. <span data-ttu-id="1a8fe-121">Restablecer su contraseña mediante el comando de contraseña de la distribución y cierre la consola de Linux:</span><span class="sxs-lookup"><span data-stu-id="1a8fe-121">Reset your password using the distribution's password command, and close the Linux Console:</span></span>

    ```BASH
    $ passwd username
    $ exit
    ```

1. <span data-ttu-id="1a8fe-122">Desde CMD de Windows, restablecer el usuario predeterminado en su cuenta de usuario de Linux normal:</span><span class="sxs-lookup"><span data-stu-id="1a8fe-122">From Windows CMD, reset your default user back to your normal Linux user account:</span></span>

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a><span data-ttu-id="1a8fe-123">Para la actualización Fall Creators Update y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="1a8fe-123">For Fall Creators Update and later</span></span>
<span data-ttu-id="1a8fe-124">Para ver qué comandos están disponibles para una distribución particular, ejecute `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="1a8fe-124">To see what commands are available for a particular distribution, run `[distro.exe] /?`.</span></span>
    
<span data-ttu-id="1a8fe-125">Por ejemplo, con Ubuntu instalado:</span><span class="sxs-lookup"><span data-stu-id="1a8fe-125">For example, with Ubuntu installed:</span></span>

```console
C:\> ubuntu.exe /?

Launches or configures a linux distribution.

Usage:
    <no args>
      - Launches the distro's default behavior. By default, this launches your default shell.

    run <command line>
      - Run the given command line in that distro, using the default configuration.
      - Everything after `run ` is passed to the linux LaunchProcess cal

    config [setting [value]]
      - Configure certain settings for this distro.
      - Settings are any of the following (by default)
        - `--default-user <username>`: Set the default user for this distro to <username>

    clean
      - Uninstalls the distro. The appx remains on your machine. This can be
        useful for "factory resetting" your instance. This removes the linux
        filesystem from the disk, but not the app from your PC, so you don't
        need to redownload the entire tar.gz again.

    help
      - Print this usage message.
```

<span data-ttu-id="1a8fe-126">Instrucciones paso a paso con Ubuntu:</span><span class="sxs-lookup"><span data-stu-id="1a8fe-126">Step by step instructions using Ubuntu:</span></span>

1. <span data-ttu-id="1a8fe-127">Abra CMD</span><span class="sxs-lookup"><span data-stu-id="1a8fe-127">Open CMD</span></span>
1. <span data-ttu-id="1a8fe-128">Establece el usuario de Linux de forma predeterminada en `root`:</span><span class="sxs-lookup"><span data-stu-id="1a8fe-128">Set the default Linux user to `root`:</span></span>

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. <span data-ttu-id="1a8fe-129">Inicie la distribución de Linux (`ubuntu`).</span><span class="sxs-lookup"><span data-stu-id="1a8fe-129">Launch your Linux distribution (`ubuntu`).</span></span>  <span data-ttu-id="1a8fe-130">Configurará automáticamente como el inicio de sesión `root`:</span><span class="sxs-lookup"><span data-stu-id="1a8fe-130">You will automatically login as `root`:</span></span>

1. <span data-ttu-id="1a8fe-131">Restablecer su contraseña mediante el `passwd` comando:</span><span class="sxs-lookup"><span data-stu-id="1a8fe-131">Reset your password using the `passwd` command:</span></span>

    ```BASH
    $ passwd username
    ```

1. <span data-ttu-id="1a8fe-132">Desde CMD de Windows, restablecer el usuario predeterminado a su cuenta de usuario de Linux normal.</span><span class="sxs-lookup"><span data-stu-id="1a8fe-132">From Windows CMD, reset your default user back to your normal Linux user account.</span></span>

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a><span data-ttu-id="1a8fe-133">Permisos</span><span class="sxs-lookup"><span data-stu-id="1a8fe-133">Permissions</span></span>

<span data-ttu-id="1a8fe-134">Hay dos conceptos importantes a tener en cuenta cuando se trata de permisos en WSL:</span><span class="sxs-lookup"><span data-stu-id="1a8fe-134">There are two important concepts to keep in mind when it comes to permissions in WSL:</span></span>

1. <span data-ttu-id="1a8fe-135">El modelo de permisos de Windows controla los derechos de un proceso a los recursos de Windows</span><span class="sxs-lookup"><span data-stu-id="1a8fe-135">The Windows permission model governs a process' rights to Windows resources</span></span>
2. <span data-ttu-id="1a8fe-136">El modelo de permisos de Linux controla los derechos de un proceso a los recursos de Linux</span><span class="sxs-lookup"><span data-stu-id="1a8fe-136">The Linux permission model controls a process' rights to Linux resources</span></span>

<span data-ttu-id="1a8fe-137">Cuando se ejecuta Linux en WSL, Linux tendrán los mismos permisos de Windows que el proceso que lo inicia.</span><span class="sxs-lookup"><span data-stu-id="1a8fe-137">When running Linux on WSL, Linux will have the same Windows permissions as the process that launches it.</span></span> <span data-ttu-id="1a8fe-138">Linux se puede iniciar en uno de dos niveles de permisos:</span><span class="sxs-lookup"><span data-stu-id="1a8fe-138">Linux can be launched in one of two permission levels:</span></span>

* <span data-ttu-id="1a8fe-139">Normal (sin privilegios elevados): Linux se ejecuta con los permisos del usuario que inició sesión</span><span class="sxs-lookup"><span data-stu-id="1a8fe-139">Normal (non-elevated): Linux runs with the permissions of the logged-in user</span></span>
* <span data-ttu-id="1a8fe-140">Administración/con privilegios elevados: Linux se ejecuta con permisos de administrador con permisos elevados/Windows</span><span class="sxs-lookup"><span data-stu-id="1a8fe-140">Elevated/admin: Linux runs with elevated/admin Windows permissions</span></span>

> <span data-ttu-id="1a8fe-141">Porque los procesos elevados pueden acceso o modificar (y, por tanto, dañar)-wide y proteger el sistema de datos y la configuración de todo el sistema **Evite** iniciar procesos con privilegios elevados a menos que sea absolutamente necesario - ya sean Windows o Linux ¡aplicaciones/tools/shells!</span><span class="sxs-lookup"><span data-stu-id="1a8fe-141">Because elevated processes can access/modify (and therefore damage) system-wide settings and system-wide/protected data, **AVOID** launching elevated processes unless you absolutely have to - whether they're Windows or Linux applications/tools/shells!</span></span>

<span data-ttu-id="1a8fe-142">Los permisos de Windows anteriores son independientes de los permisos dentro de una instancia de Linux: "Privilegios de raíz" de Linux afecten solo a los derechos del usuario dentro del entorno de Linux & del sistema de archivos; no tienen ningún impacto en los privilegios de Windows concedidos.</span><span class="sxs-lookup"><span data-stu-id="1a8fe-142">The above Windows permissions are independent of the permissions within a Linux instance: Linux "Root privileges" only impact the user’s rights within the Linux environment & filesystem; they have no impact on the Windows privileges granted.</span></span> <span data-ttu-id="1a8fe-143">Por lo tanto, que se ejecuta un proceso de Linux como raíz (por ejemplo, mediante `sudo`) solo concede que procesan los derechos de administrador en el entorno de Linux.</span><span class="sxs-lookup"><span data-stu-id="1a8fe-143">Thus, running a Linux process as root (e.g. via `sudo`) only grants that process admin rights within the Linux environment.</span></span>

<span data-ttu-id="1a8fe-144">**Ejemplo:**   </span><span class="sxs-lookup"><span data-stu-id="1a8fe-144">**Example:**  </span></span>  
<span data-ttu-id="1a8fe-145">Puede tener acceso una sesión de Bash con privilegios de administrador de Windows `cd /mnt/c/Users/Administrator` mientras una sesión de Bash sin privilegios de Administrador vería un error "Permiso denegado".</span><span class="sxs-lookup"><span data-stu-id="1a8fe-145">A Bash session with Windows admin privileges may access `cd /mnt/c/Users/Administrator` while a Bash session without admin privileges would see a "Permission Denied" error.</span></span>

<span data-ttu-id="1a8fe-146">En Linux, escriba `sudo cd /mnt/c/Users/Administrator` no concederá acceso al directorio del administrador porque los permisos dentro de Windows administrados por Windows.</span><span class="sxs-lookup"><span data-stu-id="1a8fe-146">In Linux, typing `sudo cd /mnt/c/Users/Administrator` will not grant access to the Administrator’s directory since permissions within Windows are managed by Windows.</span></span>

<span data-ttu-id="1a8fe-147">El modelo de permisos de Linux es importante cuando se encuentra dentro del entorno de Linux donde el usuario tenga permisos en función del usuario actual de Linux.</span><span class="sxs-lookup"><span data-stu-id="1a8fe-147">The Linux permission model is important when inside the Linux environment where the user has permissions based on the current Linux user.</span></span>

<span data-ttu-id="1a8fe-148">**Ejemplo:**</span><span class="sxs-lookup"><span data-stu-id="1a8fe-148">**Example:**</span></span>  
<span data-ttu-id="1a8fe-149">Puede ejecutar un usuario en el grupo de sudo `sudo apt update`.</span><span class="sxs-lookup"><span data-stu-id="1a8fe-149">A user in the sudo group may run `sudo apt update`.</span></span>
