---
title: Cuenta de usuario de Linux y permisos
description: Referencia de las cuentas de usuario y la administración de permisos con el subsistema de Windows para Linux.
keywords: BashOnWindows, bash, WSL, Windows, subsistema de Windows para Linux, windowssubsystem, Ubuntu, cuentas de usuario
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.openlocfilehash: 0d00b43d059e72edd4e2a5b9591c29441f461fca
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/14/2019
ms.locfileid: "67040826"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a><span data-ttu-id="7adbc-104">Cuentas de usuario y permisos para el subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="7adbc-104">User Accounts and Permissions for Windows Subsystem for Linux</span></span>

<span data-ttu-id="7adbc-105">La creación de un usuario de Linux es el primer paso para configurar una nueva distribución de Linux en WSL.</span><span class="sxs-lookup"><span data-stu-id="7adbc-105">Creating your Linux user is the first step in setting up a new Linux distribution on WSL.</span></span>  <span data-ttu-id="7adbc-106">La primera cuenta de usuario que cree se configura automáticamente con unos cuantos atributos especiales:</span><span class="sxs-lookup"><span data-stu-id="7adbc-106">The first user account you create is automatically configured with a few special attributes:</span></span>

1. <span data-ttu-id="7adbc-107">Es el usuario predeterminado: inicia sesión automáticamente en el inicio.</span><span class="sxs-lookup"><span data-stu-id="7adbc-107">It is your default user -- it signs-in automatically on launch.</span></span>
1. <span data-ttu-id="7adbc-108">De forma predeterminada, es administrador de Linux (un miembro del grupo sudo).</span><span class="sxs-lookup"><span data-stu-id="7adbc-108">It is Linux administrator (a member of the sudo group) by default.</span></span>

<span data-ttu-id="7adbc-109">Cada distribución de Linux que se ejecuta en el subsistema de Windows para Linux tiene sus propias cuentas de usuario y contraseñas de Linux.</span><span class="sxs-lookup"><span data-stu-id="7adbc-109">Each Linux distribution running on the Windows Subsystem for Linux has its own Linux user accounts and passwords.</span></span>  <span data-ttu-id="7adbc-110">Tendrá que configurar una cuenta de usuario de Linux cada vez que agregue una distribución, reinstale o restablezca.</span><span class="sxs-lookup"><span data-stu-id="7adbc-110">You will have to configure a Linux user account any time you add a distribution, reinstall, or reset.</span></span>  <span data-ttu-id="7adbc-111">Las cuentas de usuario de Linux no solo son independientes por distribución, sino que también son independientes de la cuenta de usuario de Windows.</span><span class="sxs-lookup"><span data-stu-id="7adbc-111">Linux user accounts are not only independent per distribution, they are also independent from your Windows user account.</span></span>

## <a name="resetting-your-linux-password"></a><span data-ttu-id="7adbc-112">Restablecimiento de la contraseña de Linux</span><span class="sxs-lookup"><span data-stu-id="7adbc-112">Resetting your Linux password</span></span>

<span data-ttu-id="7adbc-113">Si tiene acceso a su cuenta de usuario de Linux y conoce la contraseña actual, cámbiela con las herramientas de restablecimiento de contraseñas de Linux de esa `passwd`distribución, lo que es más probable.</span><span class="sxs-lookup"><span data-stu-id="7adbc-113">If you have access to your Linux user account and know your current password, change it using Linux password reset tools of that distribution -- most likely `passwd`.</span></span>

<span data-ttu-id="7adbc-114">Si no es una opción, dependiendo de la distribución, es posible que pueda restablecer la contraseña restableciendo el usuario predeterminado.</span><span class="sxs-lookup"><span data-stu-id="7adbc-114">If that's not an option, depending on the distribution, you may be able to reset your password by resetting the default user.</span></span>

<span data-ttu-id="7adbc-115">WSL ofrece una etiqueta de usuario predeterminada para identificar la cuenta de usuario que inicia sesión automáticamente al iniciar un WSL.</span><span class="sxs-lookup"><span data-stu-id="7adbc-115">WSL offers a default user tag to identify which user account automatically logs in when you start a WSL.</span></span>  <span data-ttu-id="7adbc-116">Dado que muchas distribuciones incluyen comandos para establecer el usuario predeterminado en raíz y también un usuario raíz sin contraseña establecida, cambiar el usuario predeterminado a raíz es una herramienta útil para cosas como el restablecimiento de contraseñas.</span><span class="sxs-lookup"><span data-stu-id="7adbc-116">Since many distributions include commands to set the default user to root and also a root user with no password set, changing the default user to root is a handy tool for things like password reset.</span></span>

### <a name="for-creators-update-and-earlier"></a><span data-ttu-id="7adbc-117">Para Creators Update y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="7adbc-117">For Creators Update and earlier</span></span>
<span data-ttu-id="7adbc-118">Si está ejecutando Windows 10 Creators Update o una versión anterior, puede cambiar el usuario de Bash predeterminado mediante la ejecución de los siguientes comandos:</span><span class="sxs-lookup"><span data-stu-id="7adbc-118">If you're running Windows 10 Creators update or earlier, you can change the default Bash user by running the following commands:</span></span>

1. <span data-ttu-id="7adbc-119">Cambie el usuario predeterminado a `root`:</span><span class="sxs-lookup"><span data-stu-id="7adbc-119">Change the default user to `root`:</span></span>

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. <span data-ttu-id="7adbc-120">Ejecute `bash.exe` para iniciar sesión ahora `root`como:</span><span class="sxs-lookup"><span data-stu-id="7adbc-120">Run `bash.exe` to now login as `root`:</span></span>

    ```console
    C:\> bash.exe
    ```

1. <span data-ttu-id="7adbc-121">Restablezca la contraseña con el comando de contraseña de la distribución y cierre la consola de Linux:</span><span class="sxs-lookup"><span data-stu-id="7adbc-121">Reset your password using the distribution's password command, and close the Linux Console:</span></span>

    ```BASH
    $ passwd username
    $ exit
    ```

1. <span data-ttu-id="7adbc-122">En Windows CMD, restablezca el usuario predeterminado de nuevo a su cuenta de usuario de Linux normal:</span><span class="sxs-lookup"><span data-stu-id="7adbc-122">From Windows CMD, reset your default user back to your normal Linux user account:</span></span>

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a><span data-ttu-id="7adbc-123">Para Fall Creators Update y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="7adbc-123">For Fall Creators Update and later</span></span>
<span data-ttu-id="7adbc-124">Para ver qué comandos están disponibles para una distribución determinada, ejecute `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="7adbc-124">To see what commands are available for a particular distribution, run `[distro.exe] /?`.</span></span>
    
<span data-ttu-id="7adbc-125">Por ejemplo, con Ubuntu instalado:</span><span class="sxs-lookup"><span data-stu-id="7adbc-125">For example, with Ubuntu installed:</span></span>

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

<span data-ttu-id="7adbc-126">Instrucciones paso a paso con Ubuntu:</span><span class="sxs-lookup"><span data-stu-id="7adbc-126">Step by step instructions using Ubuntu:</span></span>

1. <span data-ttu-id="7adbc-127">Abrir CMD</span><span class="sxs-lookup"><span data-stu-id="7adbc-127">Open CMD</span></span>
1. <span data-ttu-id="7adbc-128">Establezca el usuario de Linux predeterminado `root`en:</span><span class="sxs-lookup"><span data-stu-id="7adbc-128">Set the default Linux user to `root`:</span></span>

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. <span data-ttu-id="7adbc-129">Inicie la distribución de Linux`ubuntu`().</span><span class="sxs-lookup"><span data-stu-id="7adbc-129">Launch your Linux distribution (`ubuntu`).</span></span>  <span data-ttu-id="7adbc-130">Iniciará sesión automáticamente como `root`:</span><span class="sxs-lookup"><span data-stu-id="7adbc-130">You will automatically login as `root`:</span></span>

1. <span data-ttu-id="7adbc-131">Restablezca la contraseña con el `passwd` comando:</span><span class="sxs-lookup"><span data-stu-id="7adbc-131">Reset your password using the `passwd` command:</span></span>

    ```BASH
    $ passwd username
    ```

1. <span data-ttu-id="7adbc-132">En Windows CMD, restablezca el usuario predeterminado de nuevo a su cuenta de usuario de Linux normal.</span><span class="sxs-lookup"><span data-stu-id="7adbc-132">From Windows CMD, reset your default user back to your normal Linux user account.</span></span>

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a><span data-ttu-id="7adbc-133">Permisos</span><span class="sxs-lookup"><span data-stu-id="7adbc-133">Permissions</span></span>

<span data-ttu-id="7adbc-134">Hay dos conceptos importantes que se deben tener en cuenta cuando se trata de permisos en WSL:</span><span class="sxs-lookup"><span data-stu-id="7adbc-134">There are two important concepts to keep in mind when it comes to permissions in WSL:</span></span>

1. <span data-ttu-id="7adbc-135">El modelo de permisos de Windows rige los derechos de un proceso en los recursos de Windows</span><span class="sxs-lookup"><span data-stu-id="7adbc-135">The Windows permission model governs a process' rights to Windows resources</span></span>
2. <span data-ttu-id="7adbc-136">El modelo de permisos de Linux controla los derechos de un proceso para los recursos de Linux</span><span class="sxs-lookup"><span data-stu-id="7adbc-136">The Linux permission model controls a process' rights to Linux resources</span></span>

<span data-ttu-id="7adbc-137">Al ejecutar Linux en WSL, Linux tendrá los mismos permisos de Windows que el proceso que lo inicia.</span><span class="sxs-lookup"><span data-stu-id="7adbc-137">When running Linux on WSL, Linux will have the same Windows permissions as the process that launches it.</span></span> <span data-ttu-id="7adbc-138">Linux puede iniciarse en uno de los dos niveles de permiso:</span><span class="sxs-lookup"><span data-stu-id="7adbc-138">Linux can be launched in one of two permission levels:</span></span>

* <span data-ttu-id="7adbc-139">Normal (no elevado): Linux se ejecuta con los permisos del usuario que ha iniciado sesión</span><span class="sxs-lookup"><span data-stu-id="7adbc-139">Normal (non-elevated): Linux runs with the permissions of the logged-in user</span></span>
* <span data-ttu-id="7adbc-140">Elevado/administrador: Linux se ejecuta con permisos elevados o de administrador de Windows</span><span class="sxs-lookup"><span data-stu-id="7adbc-140">Elevated/admin: Linux runs with elevated/admin Windows permissions</span></span>

> <span data-ttu-id="7adbc-141">Dado que los procesos elevados pueden tener acceso a la configuración de todo el sistema y los datos protegidos o modificarlos (y, por consiguiente, dañarlos), **Evite** el inicio de procesos elevados a menos que sea absolutamente necesario-si son aplicaciones o herramientas de Windows o Linux/ visto!</span><span class="sxs-lookup"><span data-stu-id="7adbc-141">Because elevated processes can access/modify (and therefore damage) system-wide settings and system-wide/protected data, **AVOID** launching elevated processes unless you absolutely have to - whether they're Windows or Linux applications/tools/shells!</span></span>

<span data-ttu-id="7adbc-142">Los permisos de Windows anteriores son independientes de los permisos de una instancia de Linux: Los "privilegios raíz" de Linux solo afectan a los derechos del usuario en el entorno de Linux & sistema de archivos; no tienen ningún impacto en los privilegios de Windows concedidos.</span><span class="sxs-lookup"><span data-stu-id="7adbc-142">The above Windows permissions are independent of the permissions within a Linux instance: Linux "Root privileges" only impact the user’s rights within the Linux environment & filesystem; they have no impact on the Windows privileges granted.</span></span> <span data-ttu-id="7adbc-143">Por lo tanto, la ejecución de un proceso de Linux como `sudo`raíz (por ejemplo, Via) solo concede derechos de administrador de procesos en el entorno de Linux.</span><span class="sxs-lookup"><span data-stu-id="7adbc-143">Thus, running a Linux process as root (e.g. via `sudo`) only grants that process admin rights within the Linux environment.</span></span>

<span data-ttu-id="7adbc-144">**Ejemplo:**   </span><span class="sxs-lookup"><span data-stu-id="7adbc-144">**Example:**  </span></span>  
<span data-ttu-id="7adbc-145">Una sesión de bash con privilegios de administrador de `cd /mnt/c/Users/Administrator` Windows puede tener acceso mientras que una sesión de Bash sin privilegios de administrador verá el error "Permiso denegado".</span><span class="sxs-lookup"><span data-stu-id="7adbc-145">A Bash session with Windows admin privileges may access `cd /mnt/c/Users/Administrator` while a Bash session without admin privileges would see a "Permission Denied" error.</span></span>

<span data-ttu-id="7adbc-146">En Linux, al `sudo cd /mnt/c/Users/Administrator` escribir no se concederá acceso al directorio del administrador, ya que Windows administra los permisos dentro de Windows.</span><span class="sxs-lookup"><span data-stu-id="7adbc-146">In Linux, typing `sudo cd /mnt/c/Users/Administrator` will not grant access to the Administrator’s directory since permissions within Windows are managed by Windows.</span></span>

<span data-ttu-id="7adbc-147">El modelo de permisos de Linux es importante en el entorno de Linux, donde el usuario tiene permisos basados en el usuario actual de Linux.</span><span class="sxs-lookup"><span data-stu-id="7adbc-147">The Linux permission model is important when inside the Linux environment where the user has permissions based on the current Linux user.</span></span>

<span data-ttu-id="7adbc-148">**Ejemplo:**</span><span class="sxs-lookup"><span data-stu-id="7adbc-148">**Example:**</span></span>  
<span data-ttu-id="7adbc-149">Se puede ejecutar `sudo apt update`un usuario del grupo sudo.</span><span class="sxs-lookup"><span data-stu-id="7adbc-149">A user in the sudo group may run `sudo apt update`.</span></span>
