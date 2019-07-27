---
title: Notas de la versión para el subsistema de Windows para Linux
description: Notas de la versión para el subsistema de Windows para Linux.  Actualizado semanalmente.
keywords: BashOnWindows, bash, WSL, Windows, subsistema de Windows para Linux, windowssubsystem, Ubuntu
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.openlocfilehash: c262ddb359507c1654f0089050bfd15ec16402f9
ms.sourcegitcommit: 44da0f435986598e6067e36ddca9369d27064793
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/26/2019
ms.locfileid: "68523781"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="96e30-105">Notas de la versión para el subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="96e30-105">Release Notes for Windows Subsystem for Linux</span></span>


## <a name="build-18945"></a><span data-ttu-id="96e30-106">Compilación 18945</span><span class="sxs-lookup"><span data-stu-id="96e30-106">Build 18945</span></span>
<span data-ttu-id="96e30-107">Para obtener información general sobre Windows sobre la compilación 18945, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span><span class="sxs-lookup"><span data-stu-id="96e30-107">For general Windows information on build 18945 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-108">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-108">WSL</span></span>
* <span data-ttu-id="96e30-109">[WSL2] Permitir que los Sockets TCP de escucha en WSL2 sean accesibles desde el host mediante localhost: Puerto</span><span class="sxs-lookup"><span data-stu-id="96e30-109">[WSL2] Allow listening tcp sockets in WSL2 to be accessible from the host by using localhost:port</span></span>
* <span data-ttu-id="96e30-110">[WSL2] Correcciones de errores de instalación/conversión y diagnósticos adicionales para realizar un seguimiento de los problemas futuros [alvent 4105]</span><span class="sxs-lookup"><span data-stu-id="96e30-110">[WSL2] Fixes for install / conversion failures and additional diagnostics to track down future issues [GH 4105]</span></span> 
* <span data-ttu-id="96e30-111">[WSL2] Mejorar la capacidad de diagnóstico de los problemas de red de WSL2</span><span class="sxs-lookup"><span data-stu-id="96e30-111">[WSL2] Improve diagnosability of WSL2 network issues</span></span>
* <span data-ttu-id="96e30-112">[WSL2] Actualización de la versión de kernel a 4.19.55</span><span class="sxs-lookup"><span data-stu-id="96e30-112">[WSL2] Update kernel version to 4.19.55</span></span>
* <span data-ttu-id="96e30-113">[WSL2] Actualización del kernel con las opciones de configuración necesarias para Docker [alvent 4165]</span><span class="sxs-lookup"><span data-stu-id="96e30-113">[WSL2] Update kernel with config options required for docker [GH 4165]</span></span>
* <span data-ttu-id="96e30-114">[WSL2] Aumente el número de CPU asignadas a la máquina virtual de utilidad ligera para que sea la misma que el host (se ha limitado previamente a 8 por CONFIG_NR_CPUS en la configuración del kernel) [alvent 4137]</span><span class="sxs-lookup"><span data-stu-id="96e30-114">[WSL2] Increase the number of CPUs assigned to the lightweight utility VM to be the same as the host (was previously capped at 8 by CONFIG_NR_CPUS in the kernel config) [GH 4137]</span></span>
* <span data-ttu-id="96e30-115">[WSL2] Creación de un archivo de intercambio para la máquina virtual ligera WSL2</span><span class="sxs-lookup"><span data-stu-id="96e30-115">[WSL2] Create a swap file for the WSL2 lightweight VM</span></span>
* <span data-ttu-id="96e30-116">[WSL2] Permitir que los montajes de usuarios sean \\visibles a\\través \\de WSL $ distribución (por ejemplo, sshfs) [alvent 4172]</span><span class="sxs-lookup"><span data-stu-id="96e30-116">[WSL2] Allow user mounts to be visible via \\\\wsl$\\distro (for example sshfs) [GH 4172]</span></span>
* <span data-ttu-id="96e30-117">[WSL2] Mejorar el rendimiento del sistema de archivos 9P</span><span class="sxs-lookup"><span data-stu-id="96e30-117">[WSL2] Improve 9p filesystem performance</span></span>
* <span data-ttu-id="96e30-118">[WSL2] Asegúrese de que la ACL de VHD no crezca sin límite [alvent 4126]</span><span class="sxs-lookup"><span data-stu-id="96e30-118">[WSL2] Ensure vhd ACL does not grow unbounded [GH 4126]</span></span>
* <span data-ttu-id="96e30-119">[WSL2] Actualizar configuración de kernel para admitir squashfs y xt_conntrack [alvent 4107, 4123]</span><span class="sxs-lookup"><span data-stu-id="96e30-119">[WSL2] Update kernel config to support squashfs and xt_conntrack [GH 4107, 4123]</span></span>
* <span data-ttu-id="96e30-120">[WSL2] Corrección para Interop. Enabled/etc/WSL.conf (opción) [alvent 4140]</span><span class="sxs-lookup"><span data-stu-id="96e30-120">[WSL2] Fix for interop.enabled /etc/wsl.conf option [GH 4140]</span></span>
* <span data-ttu-id="96e30-121">[WSL2] Devuelve ENOTSUP si el sistema de archivos no es compatible con EAs</span><span class="sxs-lookup"><span data-stu-id="96e30-121">[WSL2] Return ENOTSUP if the file system does not support EAs</span></span>
* <span data-ttu-id="96e30-122">[WSL2] Corregir CopyFile Hang with \\ \\WSL $</span><span class="sxs-lookup"><span data-stu-id="96e30-122">[WSL2] Fix CopyFile hang with \\\\wsl$</span></span>
* <span data-ttu-id="96e30-123">Cambie el valor predeterminado de umask a 0022 y agregue la configuración de filesystem. umask a/etc/WSL.conf</span><span class="sxs-lookup"><span data-stu-id="96e30-123">Switch default umask to 0022 and add filesystem.umask setting to /etc/wsl.conf</span></span>
* <span data-ttu-id="96e30-124">Corrección de wslpath para resolver correctamente los vínculos simbólicos, esto se retomó en 19h1 [alvent 4078]</span><span class="sxs-lookup"><span data-stu-id="96e30-124">Fix wslpath to properly resolve symlinks, this was regressed in 19h1 [GH 4078]</span></span>
* <span data-ttu-id="96e30-125">Introduzca el archivo%\.userprofile% wslconfig para ajustar la configuración de WSL2</span><span class="sxs-lookup"><span data-stu-id="96e30-125">Introduce %UserProfile%\.wslconfig file for tweaking WSL2 settings</span></span>
```
[wsl2]
kernel=<path>              # An absolute Windows path to a custom Linux kernel.
memory=<size>              # How much memory to assign to the WSL2 VM.
processors=<number>        # How many processors to assign to the WSL2 VM.
swap=<size>                # How much swap space to add to the WSL2 VM. 0 for no swap file.
swapFile=<path>            # An absolute Windows path to the swap vhd.
localhostForwarding=<bool> # Boolean specifying if ports bound to wildcard or localhost in the WSL2 VM should be connectable from the host via localhost:port (default true).

# <path> entries must be absolute Windows paths with escaped backslashes, for example C:\\Users\\Ben\\kernel
# <size> entries must be size followed by unit, for example 8GB or 512MB
```

## <a name="build-18917"></a><span data-ttu-id="96e30-126">Compilación 18917</span><span class="sxs-lookup"><span data-stu-id="96e30-126">Build 18917</span></span>
<span data-ttu-id="96e30-127">Para obtener información general sobre Windows sobre la compilación 18917, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span><span class="sxs-lookup"><span data-stu-id="96e30-127">For general Windows information on build 18917 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-128">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-128">WSL</span></span>
* <span data-ttu-id="96e30-129">WSL 2 ya está disponible.</span><span class="sxs-lookup"><span data-stu-id="96e30-129">WSL 2 is now available!</span></span> <span data-ttu-id="96e30-130">Consulte el [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="96e30-130">Please see [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) for more details.</span></span>
* <span data-ttu-id="96e30-131">Corregir una regresión en la que el inicio de procesos de Windows a través de vínculos simbólicos no funcionaba correctamente [alvent 3999]</span><span class="sxs-lookup"><span data-stu-id="96e30-131">Fix a regression where launching Windows processes via symlinks did not work correctly [GH 3999]</span></span>
* <span data-ttu-id="96e30-132">Agregue WSL. exe--List--verbose, WSL. exe--List--Quiet y WSL. exe--Import--version Options to WSL. exe</span><span class="sxs-lookup"><span data-stu-id="96e30-132">Add wsl.exe --list --verbose, wsl.exe --list --quiet, and wsl.exe --import --version options to wsl.exe</span></span>
* <span data-ttu-id="96e30-133">Agregar WSL. exe: opción Shutdown</span><span class="sxs-lookup"><span data-stu-id="96e30-133">Add wsl.exe --shutdown option</span></span>
* <span data-ttu-id="96e30-134">Plan 9: Permitir abrir un directorio para escribir en él correctamente</span><span class="sxs-lookup"><span data-stu-id="96e30-134">Plan 9: Allow opening a directory for write to succeed</span></span>

## <a name="build-18890"></a><span data-ttu-id="96e30-135">Compilación 18890</span><span class="sxs-lookup"><span data-stu-id="96e30-135">Build 18890</span></span>
<span data-ttu-id="96e30-136">Para obtener información general sobre Windows sobre la compilación 18890, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span><span class="sxs-lookup"><span data-stu-id="96e30-136">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-137">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-137">WSL</span></span>
* <span data-ttu-id="96e30-138">Pérdida de socket sin bloqueo [alvent 2913]</span><span class="sxs-lookup"><span data-stu-id="96e30-138">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="96e30-139">La entrada de EOF en el terminal puede bloquear lecturas posteriores [alvent 3421]</span><span class="sxs-lookup"><span data-stu-id="96e30-139">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="96e30-140">Actualice el encabezado resolv. conf para hacer referencia a WSL. conf [descrito en alvent 3928]</span><span class="sxs-lookup"><span data-stu-id="96e30-140">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="96e30-141">Interbloqueo en epoll eliminar código [alvent 3922]</span><span class="sxs-lookup"><span data-stu-id="96e30-141">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="96e30-142">Controlar los espacios de los argumentos en--Import y – Export [alvent 3932]</span><span class="sxs-lookup"><span data-stu-id="96e30-142">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="96e30-143">La extensión de los archivos de mmap no funciona correctamente [alvent 3939]</span><span class="sxs-lookup"><span data-stu-id="96e30-143">Extending mmap’d files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="96e30-144">Corrección del problema con \\ARM64 WSL $ Access no funciona correctamente</span><span class="sxs-lookup"><span data-stu-id="96e30-144">Fix issue with ARM64 \\wsl$ access not working properly</span></span>
* <span data-ttu-id="96e30-145">Agregar el mejor icono predeterminado para WSL. exe</span><span class="sxs-lookup"><span data-stu-id="96e30-145">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="96e30-146">Compilación 18342</span><span class="sxs-lookup"><span data-stu-id="96e30-146">Build 18342</span></span>
<span data-ttu-id="96e30-147">Para obtener información general sobre Windows sobre la compilación 18342, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span><span class="sxs-lookup"><span data-stu-id="96e30-147">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-148">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-148">WSL</span></span>
* <span data-ttu-id="96e30-149">Hemos agregado la posibilidad de que los usuarios accedan a los archivos de Linux en un WSL distribución desde Windows.</span><span class="sxs-lookup"><span data-stu-id="96e30-149">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="96e30-150">Se puede tener acceso a estos archivos a través de la línea de comandos y también las aplicaciones de Windows, como el explorador de archivos, VSCode, etc. pueden interactuar con estos archivos.</span><span class="sxs-lookup"><span data-stu-id="96e30-150">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="96e30-151">Para acceder a los archivos, vaya \\a \\WSL\\$ < distro_name >, o consulte la lista de las distribuciones en ejecución \\navegando a \\WSL $</span><span class="sxs-lookup"><span data-stu-id="96e30-151">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="96e30-152">Agregar etiquetas de información de CPU adicionales y corregir valores de Cpus_allowed [_list] [alvent 2234]</span><span class="sxs-lookup"><span data-stu-id="96e30-152">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="96e30-153">Compatibilidad con Exec desde un subproceso no líder [alvent 3800]</span><span class="sxs-lookup"><span data-stu-id="96e30-153">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="96e30-154">Tratar errores de actualización de la configuración como no graves [al3785]</span><span class="sxs-lookup"><span data-stu-id="96e30-154">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="96e30-155">Actualización de binfmt para administrar correctamente los desplazamientos [alvent 3768]</span><span class="sxs-lookup"><span data-stu-id="96e30-155">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="96e30-156">Habilitar la asignación de unidades de red para el Plan 9 [alvent 3854]</span><span class="sxs-lookup"><span data-stu-id="96e30-156">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="96e30-157">Compatibilidad con Windows-> Linux y Linux-> la traducción de rutas de acceso de Windows para montajes de BIND</span><span class="sxs-lookup"><span data-stu-id="96e30-157">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="96e30-158">Crear secciones de solo lectura para asignaciones en archivos abiertos de solo lectura</span><span class="sxs-lookup"><span data-stu-id="96e30-158">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="96e30-159">Compilación 18334</span><span class="sxs-lookup"><span data-stu-id="96e30-159">Build 18334</span></span>
<span data-ttu-id="96e30-160">Para obtener información general sobre Windows sobre la compilación 18334, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span><span class="sxs-lookup"><span data-stu-id="96e30-160">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-161">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-161">WSL</span></span>
* <span data-ttu-id="96e30-162">Rediseño del modo en que se asigna la zona horaria de Windows a una zona horaria de Linux [alvent 3747]</span><span class="sxs-lookup"><span data-stu-id="96e30-162">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="96e30-163">Corregir pérdidas de memoria y agregar nuevas funciones de traducción de cadenas [alvent 3746]</span><span class="sxs-lookup"><span data-stu-id="96e30-163">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="96e30-164">SIGCONT en un elemento threadgroup sin subprocesos es una operación no operativa [alvent 3741]</span><span class="sxs-lookup"><span data-stu-id="96e30-164">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="96e30-165">Mostrar correctamente los descriptores de archivo de socket y epoll en/proc/Self/FD</span><span class="sxs-lookup"><span data-stu-id="96e30-165">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="96e30-166">Compilación 18305</span><span class="sxs-lookup"><span data-stu-id="96e30-166">Build 18305</span></span>
<span data-ttu-id="96e30-167">Para obtener información general sobre Windows sobre la compilación 18305, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span><span class="sxs-lookup"><span data-stu-id="96e30-167">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-168">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-168">WSL</span></span>
* <span data-ttu-id="96e30-169">pthreads perder el acceso a los archivos cuando el subproceso principal sale [alvent 3589]</span><span class="sxs-lookup"><span data-stu-id="96e30-169">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="96e30-170">TIOCSCTTY debe omitir el parámetro "Force" a menos que sea necesario [alvent 3652]</span><span class="sxs-lookup"><span data-stu-id="96e30-170">TIOCSCTTY should ignore the “force” parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="96e30-171">mejoras en la línea de comandos de WSL. exe y la adición de la funcionalidad de importación y exportación.</span><span class="sxs-lookup"><span data-stu-id="96e30-171">wsl.exe command line improvements and addition of import / export functionality.</span></span>
```
Usage: wsl.exe [Argument] [Options...] [CommandLine]

Arguments to run Linux binaries:

    If no command line is provided, wsl.exe launches the default shell.

    --exec, -e <CommandLine>
        Execute the specified command without using the default Linux shell.

    --
        Pass the remaining command line as is.

Options:
    --distribution, -d <DistributionName>
        Run the specified distribution.

    --user, -u <UserName>
        Run as the specified user.

Arguments to manage Windows Subsystem for Linux:

    --export <DistributionName> <FileName>
        Exports the distribution to a tar file.
        The filename can be - for standard output.

    --import <DistributionName> <InstallLocation> <FileName>
        Imports the specified tar file as a new distribution.
        The filename can be - for standard input.

    --list, -l [Options]
        Lists distributions.

        Options:
            --all
                List all distributions, including distributions that are currently
                being installed or uninstalled.

            --running
                List only distributions that are currently running.

    -setdefault, -s <DistributionName>
        Sets the distribution as the default.

    --terminate, -t <DistributionName>
        Terminates the distribution.

    --unregister <DistributionName>
        Unregisters the distribution.

    --upgrade <DistributionName>
        Upgrades the distribution to the WslFs file system format.

    --help
        Display usage information.
```

## <a name="build-18277"></a><span data-ttu-id="96e30-172">Compilación 18277</span><span class="sxs-lookup"><span data-stu-id="96e30-172">Build 18277</span></span>
<span data-ttu-id="96e30-173">Para obtener información general sobre Windows sobre la compilación 18277, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span><span class="sxs-lookup"><span data-stu-id="96e30-173">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-174">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-174">WSL</span></span>
* <span data-ttu-id="96e30-175">Corrección del error "no se admite esta interfaz" que se presentó en la compilación 18272 [alvent 3645]</span><span class="sxs-lookup"><span data-stu-id="96e30-175">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="96e30-176">Omitir la marca MNT_FORCE para umount syscall [alvent 3605]</span><span class="sxs-lookup"><span data-stu-id="96e30-176">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="96e30-177">Cambiar la interoperabilidad de WSL para usar la API de CreatePseudoConsole oficial</span><span class="sxs-lookup"><span data-stu-id="96e30-177">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="96e30-178">No mantener ningún valor de tiempo de espera cuando se reinicie FUTEX_WAIT</span><span class="sxs-lookup"><span data-stu-id="96e30-178">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="96e30-179">Compilación 18272</span><span class="sxs-lookup"><span data-stu-id="96e30-179">Build 18272</span></span>
<span data-ttu-id="96e30-180">Para obtener información general sobre Windows sobre la compilación 18272, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span><span class="sxs-lookup"><span data-stu-id="96e30-180">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-181">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-181">WSL</span></span>
* <span data-ttu-id="96e30-182">**ATENCIÓN** Hay un problema en esta compilación que hace que WSL sea inoperable.</span><span class="sxs-lookup"><span data-stu-id="96e30-182">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="96e30-183">Al intentar iniciar la distribución, verá el error "no se admite dicha interfaz".</span><span class="sxs-lookup"><span data-stu-id="96e30-183">When trying to launch your distribution you will see a “No such interface supported” error.</span></span> <span data-ttu-id="96e30-184">El problema se ha solucionado y estará en la compilación rápida de Insider de la semana siguiente.</span><span class="sxs-lookup"><span data-stu-id="96e30-184">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="96e30-185">Si ha instalado esta compilación, puede revertir a la compilación anterior de Windows mediante "volver a la versión anterior de Windows 10" en Configuración-> actualización & la recuperación de > de seguridad.</span><span class="sxs-lookup"><span data-stu-id="96e30-185">If you've installed this build you can roll back to the previous Windows build using “Go back to the previous version of Windows 10” in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="96e30-186">Compilación 18267</span><span class="sxs-lookup"><span data-stu-id="96e30-186">Build 18267</span></span>
<span data-ttu-id="96e30-187">Para obtener información general sobre Windows sobre la compilación 18267, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span><span class="sxs-lookup"><span data-stu-id="96e30-187">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-188">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-188">WSL</span></span>
* <span data-ttu-id="96e30-189">Corrija el problema en el que el proceso inerte no se puede obtener y permanecer indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="96e30-189">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="96e30-190">WslRegisterDistribution se bloquea si el mensaje de error supera la longitud máxima [alvent 3592]</span><span class="sxs-lookup"><span data-stu-id="96e30-190">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="96e30-191">Permitir que fsync se realice correctamente para los archivos de solo lectura en DrvFs [alvent 3556]</span><span class="sxs-lookup"><span data-stu-id="96e30-191">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="96e30-192">Asegúrese de que los directorios/Bin y/sbin existen antes de crear los vínculos simbólicos dentro de [alvent 3584]</span><span class="sxs-lookup"><span data-stu-id="96e30-192">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="96e30-193">Se agregó un mecanismo de tiempo de espera de finalización de instancia para las instancias de WSL.</span><span class="sxs-lookup"><span data-stu-id="96e30-193">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="96e30-194">El tiempo de espera está establecido actualmente en 15 segundos, lo que significa que la instancia finalizará 15 segundos después de que termine el último proceso WSL.</span><span class="sxs-lookup"><span data-stu-id="96e30-194">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="96e30-195">Para finalizar una distribución inmediatamente, use:</span><span class="sxs-lookup"><span data-stu-id="96e30-195">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="96e30-196">Compilación 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="96e30-196">Build 17763 (1809)</span></span>
<span data-ttu-id="96e30-197">Para obtener información general sobre Windows sobre la compilación 17763, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span><span class="sxs-lookup"><span data-stu-id="96e30-197">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-198">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-198">WSL</span></span>
* <span data-ttu-id="96e30-199">SetPriority syscall Permission check Too STRICT para cambiar la misma prioridad de subprocesos [alvent 1838]</span><span class="sxs-lookup"><span data-stu-id="96e30-199">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="96e30-200">Asegúrese de que el tiempo de interrupción no sesgado se usa para el tiempo de arranque para evitar que se devuelvan valores negativos para clock_gettime (CLOCK_BOOTTIME) [alvent 3434]</span><span class="sxs-lookup"><span data-stu-id="96e30-200">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="96e30-201">Controlar los vínculos simbólicos en el intérprete WSL binfmt [alvent 3424]</span><span class="sxs-lookup"><span data-stu-id="96e30-201">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="96e30-202">Mejor control de la limpieza de descriptores de archivo de elemento threadgroup Leader.</span><span class="sxs-lookup"><span data-stu-id="96e30-202">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="96e30-203">Cambiar WSL para usar KeQueryInterruptTimePrecise en lugar de KeQueryPerformanceCounter para evitar el desbordamiento [alvent 3252]</span><span class="sxs-lookup"><span data-stu-id="96e30-203">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="96e30-204">Ptrace Attach puede producir un valor de devolución incorrecto de las llamadas del sistema [alvent 1731]</span><span class="sxs-lookup"><span data-stu-id="96e30-204">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="96e30-205">Corrección de varios problemas relacionados con AF_UNIX [alvent 3371]</span><span class="sxs-lookup"><span data-stu-id="96e30-205">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="96e30-206">Corregir el problema que podría provocar un error de interoperabilidad de WSL si el directorio de trabajo actual tiene menos de 5 caracteres de longitud [alvent 3379]</span><span class="sxs-lookup"><span data-stu-id="96e30-206">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="96e30-207">Evitar el retraso de un segundo error en las conexiones de bucle invertido a puertos no existentes [alvent 3286]</span><span class="sxs-lookup"><span data-stu-id="96e30-207">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="96e30-208">Agregar archivo de código auxiliar de/proc/sys/FS/File-Max [alvent 2893]</span><span class="sxs-lookup"><span data-stu-id="96e30-208">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="96e30-209">Información más precisa sobre el ámbito IPV6.</span><span class="sxs-lookup"><span data-stu-id="96e30-209">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="96e30-210">Compatibilidad con PR_SET_PTRACER [alvent 3053]</span><span class="sxs-lookup"><span data-stu-id="96e30-210">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="96e30-211">El sistema de archivos de canalización borra accidentalmente el evento epoll desencadenado por el borde [alvent 3276]</span><span class="sxs-lookup"><span data-stu-id="96e30-211">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="96e30-212">El ejecutable de Win32 iniciado mediante el symlink de NTFS no respeta el nombre de symlink [alvent 2909]</span><span class="sxs-lookup"><span data-stu-id="96e30-212">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="96e30-213">Compatibilidad mejorada con Zombie [alvent 1353]</span><span class="sxs-lookup"><span data-stu-id="96e30-213">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="96e30-214">Agregar entradas WSL. conf para controlar el comportamiento de interoperabilidad de Windows [alvent 1493]</span><span class="sxs-lookup"><span data-stu-id="96e30-214">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="96e30-215">Corrección para getsockname no Always devolviendo siempre el tipo de familia de sockets UNIX [alvent 1774]</span><span class="sxs-lookup"><span data-stu-id="96e30-215">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="96e30-216">Agregar compatibilidad para TIOCSTI [alvent 1863]</span><span class="sxs-lookup"><span data-stu-id="96e30-216">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="96e30-217">Los sockets sin bloqueo en el proceso de conexión deben devolver EAGAIN para los intentos de escritura [alvent 2846]</span><span class="sxs-lookup"><span data-stu-id="96e30-217">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="96e30-218">Compatibilidad con la interoperabilidad en VHD montados [alvent 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="96e30-218">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="96e30-219">Corregir el problema de comprobación de permisos en la carpeta raíz [alvent 3304]</span><span class="sxs-lookup"><span data-stu-id="96e30-219">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="96e30-220">Compatibilidad limitada para los ioctl de teclado TTY KDGKBTYPE, KDGKBMODE y KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="96e30-220">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="96e30-221">Las aplicaciones de interfaz de usuario de Windows deben ejecutarse incluso cuando se inician en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="96e30-221">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="96e30-222">Agregar WSL-u o--User Option [alvent 1203]</span><span class="sxs-lookup"><span data-stu-id="96e30-222">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="96e30-223">Corregir problemas de inicio de WSL cuando se habilita el inicio rápido [alvent 2576]</span><span class="sxs-lookup"><span data-stu-id="96e30-223">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="96e30-224">Los sockets de UNIX deben conservar las credenciales del mismo nivel desconectadas [alvent 3183]</span><span class="sxs-lookup"><span data-stu-id="96e30-224">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="96e30-225">Sockets de UNIX sin bloqueo con error indefinidamente con EAGAIN [alvent 3191]</span><span class="sxs-lookup"><span data-stu-id="96e30-225">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="96e30-226">Case = OFF es el nuevo tipo de montaje drvfs predeterminado [alvent 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="96e30-226">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="96e30-227">Consulte el [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="96e30-227">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="96e30-228">Agregue wslconfig/Terminate. para detener las distribuciones en ejecución.</span><span class="sxs-lookup"><span data-stu-id="96e30-228">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="96e30-229">Corrija el problema con las entradas del menú contextual del shell de WSL que no controlan correctamente las rutas de acceso con espacios.</span><span class="sxs-lookup"><span data-stu-id="96e30-229">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="96e30-230">Exponer la distinción de mayúsculas y minúsculas por directorio como atributo extendido</span><span class="sxs-lookup"><span data-stu-id="96e30-230">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="96e30-231">ARM64 Emular las operaciones de mantenimiento de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="96e30-231">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="96e30-232">Resolver el [problema dotnet](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="96e30-232">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="96e30-233">DrvFs: solo caracteres de escape en el intervalo privado que corresponden a un carácter de escape.</span><span class="sxs-lookup"><span data-stu-id="96e30-233">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="96e30-234">Error de corrección de errores en la validación de longitud del intérprete del analizador ELF [alvent 3154]</span><span class="sxs-lookup"><span data-stu-id="96e30-234">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="96e30-235">WSL los temporizadores absolutos con una hora en el pasado no se activan [alvent 3091]</span><span class="sxs-lookup"><span data-stu-id="96e30-235">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="96e30-236">Asegúrese de que los puntos de reanálisis recién creados se muestran como tales en el directorio principal.</span><span class="sxs-lookup"><span data-stu-id="96e30-236">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="96e30-237">Cree de forma atómica directorios con distinción entre mayúsculas y minúsculas en DrvFs.</span><span class="sxs-lookup"><span data-stu-id="96e30-237">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="96e30-238">Se ha corregido un problema adicional en el que las operaciones multiproceso podían devolver ENOENT, aunque el archivo exista.</span><span class="sxs-lookup"><span data-stu-id="96e30-238">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="96e30-239">[ALVENT 2712]</span><span class="sxs-lookup"><span data-stu-id="96e30-239">[GH 2712]</span></span>
* <span data-ttu-id="96e30-240">Se corrigió un error de inicio de WSL cuando UMCI está habilitado.</span><span class="sxs-lookup"><span data-stu-id="96e30-240">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="96e30-241">[ALVENT 3020]</span><span class="sxs-lookup"><span data-stu-id="96e30-241">[GH 3020]</span></span>
* <span data-ttu-id="96e30-242">Agregue el menú contextual del explorador para iniciar WSL [alvent 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="96e30-242">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="96e30-243">Para usar, mantenga presionada la tecla Mayús y haga clic con el botón derecho en una ventana del explorador.</span><span class="sxs-lookup"><span data-stu-id="96e30-243">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="96e30-244">Corregir el comportamiento de no bloqueo de sockets de UNIX [alvent 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="96e30-244">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="96e30-245">Corrija el comando de NETLINK de bloqueo, tal como se muestra en alvent 2026.</span><span class="sxs-lookup"><span data-stu-id="96e30-245">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="96e30-246">Agregue compatibilidad para los marcadores de propagación de montaje [alvent 2911].</span><span class="sxs-lookup"><span data-stu-id="96e30-246">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="96e30-247">Corrección del problema con TRUNCATE no provocando eventos de inotify [alvent 2978].</span><span class="sxs-lookup"><span data-stu-id="96e30-247">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="96e30-248">Agregue la opción--exec de WSL. exe para invocar un solo binario sin un shell.</span><span class="sxs-lookup"><span data-stu-id="96e30-248">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="96e30-249">Add--Distribution Option para WSL. exe para seleccionar un distribución específico.</span><span class="sxs-lookup"><span data-stu-id="96e30-249">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="96e30-250">Compatibilidad limitada para dmesg.</span><span class="sxs-lookup"><span data-stu-id="96e30-250">Limited support for dmesg.</span></span> <span data-ttu-id="96e30-251">Ahora, las aplicaciones pueden iniciar sesión en dmesg.</span><span class="sxs-lookup"><span data-stu-id="96e30-251">Applications can now log to dmesg.</span></span> <span data-ttu-id="96e30-252">El controlador WSL registra información limitada en dmesg.</span><span class="sxs-lookup"><span data-stu-id="96e30-252">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="96e30-253">En el futuro, esto puede extenderse para llevar a cabo otros diagnósticos e información del controlador.</span><span class="sxs-lookup"><span data-stu-id="96e30-253">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="96e30-254">Nota: dmesg se admite actualmente a través `/dev/kmsg` de la interfaz de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="96e30-254">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="96e30-255">`syslog`la interfaz syscall todavía no se admite.</span><span class="sxs-lookup"><span data-stu-id="96e30-255">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="96e30-256">Y, por lo tanto, algunas `dmesg` de las opciones de la `-S`línea `-C` de comandos, como, no funcionan.</span><span class="sxs-lookup"><span data-stu-id="96e30-256">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="96e30-257">Cambiar el GID y el modo de dispositivos serie predeterminados para que coincidan con el nativo [alvent 3042]</span><span class="sxs-lookup"><span data-stu-id="96e30-257">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="96e30-258">DrvFs ahora admite atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="96e30-258">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="96e30-259">Nota: DrvFs tiene algunas limitaciones en cuanto al nombre de los atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="96e30-259">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="96e30-260">Algunos caracteres (como '/', ': ' y '\*') no están permitidos, y los nombres de atributos extendidos no distinguen mayúsculas de minúsculas en DrvFs</span><span class="sxs-lookup"><span data-stu-id="96e30-260">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="96e30-261">Compilación 18252 (omitir)</span><span class="sxs-lookup"><span data-stu-id="96e30-261">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="96e30-262">Para obtener información general sobre Windows sobre la compilación 18252, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span><span class="sxs-lookup"><span data-stu-id="96e30-262">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-263">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-263">WSL</span></span>
* <span data-ttu-id="96e30-264">Traslado de los binarios init y bsdtar fuera del archivo dll de lxssmanager y a una carpeta de herramientas independiente</span><span class="sxs-lookup"><span data-stu-id="96e30-264">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="96e30-265">Corregir la carrera en torno al cierre del descriptor de archivo cuando se usa CLONE_FILES</span><span class="sxs-lookup"><span data-stu-id="96e30-265">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="96e30-266">Controlar campos opcionales en/proc/PID/mountinfo al traducir rutas de DrvFs</span><span class="sxs-lookup"><span data-stu-id="96e30-266">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="96e30-267">Permita que DrvFs mknod se realice correctamente sin compatibilidad con metadatos para S_IFREG</span><span class="sxs-lookup"><span data-stu-id="96e30-267">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="96e30-268">Los archivos ReadOnly creados en DrvFs deben tener el conjunto de atributos ReadOnly [alvent 3411]</span><span class="sxs-lookup"><span data-stu-id="96e30-268">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="96e30-269">Incorporación de la aplicación auxiliar de/sbin/Mount.drvfs para controlar el montaje de DrvFs</span><span class="sxs-lookup"><span data-stu-id="96e30-269">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="96e30-270">Use el cambio de nombre de POSIX en DrvFs.</span><span class="sxs-lookup"><span data-stu-id="96e30-270">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="96e30-271">Permitir traducción de rutas de acceso en volúmenes sin un GUID de volumen.</span><span class="sxs-lookup"><span data-stu-id="96e30-271">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="96e30-272">Compilación 17738 (rápida)</span><span class="sxs-lookup"><span data-stu-id="96e30-272">Build 17738 (Fast)</span></span>
<span data-ttu-id="96e30-273">Para obtener información general sobre Windows sobre la compilación 17738, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span><span class="sxs-lookup"><span data-stu-id="96e30-273">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-274">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-274">WSL</span></span>
* <span data-ttu-id="96e30-275">SetPriority syscall Permission check Too STRICT para cambiar la misma prioridad de subprocesos [alvent 1838]</span><span class="sxs-lookup"><span data-stu-id="96e30-275">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="96e30-276">Asegúrese de que el tiempo de interrupción no sesgado se usa para el tiempo de arranque para evitar que se devuelvan valores negativos para clock_gettime (CLOCK_BOOTTIME) [alvent 3434]</span><span class="sxs-lookup"><span data-stu-id="96e30-276">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="96e30-277">Controlar los vínculos simbólicos en el intérprete WSL binfmt [alvent 3424]</span><span class="sxs-lookup"><span data-stu-id="96e30-277">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="96e30-278">Mejor control de la limpieza de descriptores de archivo de elemento threadgroup Leader.</span><span class="sxs-lookup"><span data-stu-id="96e30-278">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="96e30-279">Compilación 17728 (rápida)</span><span class="sxs-lookup"><span data-stu-id="96e30-279">Build 17728 (Fast)</span></span>
<span data-ttu-id="96e30-280">Para obtener información general sobre Windows sobre la compilación 17728, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span><span class="sxs-lookup"><span data-stu-id="96e30-280">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-281">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-281">WSL</span></span>
* <span data-ttu-id="96e30-282">Cambiar WSL para usar KeQueryInterruptTimePrecise en lugar de KeQueryPerformanceCounter para evitar el desbordamiento [alvent 3252]</span><span class="sxs-lookup"><span data-stu-id="96e30-282">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="96e30-283">Ptrace Attach puede producir un valor de devolución incorrecto de las llamadas del sistema [alvent 1731]</span><span class="sxs-lookup"><span data-stu-id="96e30-283">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="96e30-284">Corrección de varios problemas relacionados con AF_UNIX [alvent 3371]</span><span class="sxs-lookup"><span data-stu-id="96e30-284">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="96e30-285">Corregir el problema que podría provocar un error de interoperabilidad de WSL si el directorio de trabajo actual tiene menos de 5 caracteres de longitud [alvent 3379]</span><span class="sxs-lookup"><span data-stu-id="96e30-285">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="96e30-286">Compilación 18204 (omitir)</span><span class="sxs-lookup"><span data-stu-id="96e30-286">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="96e30-287">Para obtener información general sobre Windows sobre la compilación 18204, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="96e30-287">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-288">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-288">WSL</span></span>
* <span data-ttu-id="96e30-289">Canalización del sistema de archivos de canalización inadvertenly borrar el borde desencadenador de epoll [alvent 3276]</span><span class="sxs-lookup"><span data-stu-id="96e30-289">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="96e30-290">El ejecutable de Win32 iniciado mediante el symlink de NTFS no respeta el nombre de symlink [alvent 2909]</span><span class="sxs-lookup"><span data-stu-id="96e30-290">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="96e30-291">Compilación 17723 (rápida)</span><span class="sxs-lookup"><span data-stu-id="96e30-291">Build 17723 (Fast)</span></span>
<span data-ttu-id="96e30-292">Para obtener información general sobre Windows sobre la compilación 17723, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="96e30-292">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-293">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-293">WSL</span></span>
* <span data-ttu-id="96e30-294">Evitar el retraso de un segundo error en las conexiones de bucle invertido a puertos no existentes [alvent 3286]</span><span class="sxs-lookup"><span data-stu-id="96e30-294">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="96e30-295">Agregar archivo de código auxiliar de/proc/sys/FS/File-Max [alvent 2893]</span><span class="sxs-lookup"><span data-stu-id="96e30-295">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="96e30-296">Información más precisa sobre el ámbito IPV6.</span><span class="sxs-lookup"><span data-stu-id="96e30-296">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="96e30-297">Compatibilidad con PR_SET_PTRACER [alvent 3053]</span><span class="sxs-lookup"><span data-stu-id="96e30-297">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="96e30-298">Canalización del sistema de archivos de canalización inadvertenly borrar el borde desencadenador de epoll [alvent 3276]</span><span class="sxs-lookup"><span data-stu-id="96e30-298">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="96e30-299">El ejecutable de Win32 iniciado mediante el symlink de NTFS no respeta el nombre de symlink [alvent 2909]</span><span class="sxs-lookup"><span data-stu-id="96e30-299">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="96e30-300">Compilación 17713</span><span class="sxs-lookup"><span data-stu-id="96e30-300">Build 17713</span></span>
<span data-ttu-id="96e30-301">Para obtener información general sobre Windows sobre la compilación 17713, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span><span class="sxs-lookup"><span data-stu-id="96e30-301">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-302">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-302">WSL</span></span>
* <span data-ttu-id="96e30-303">Compatibilidad mejorada con Zombie [alvent 1353]</span><span class="sxs-lookup"><span data-stu-id="96e30-303">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="96e30-304">Agregar entradas WSL. conf para controlar el comportamiento de interoperabilidad de Windows [alvent 1493]</span><span class="sxs-lookup"><span data-stu-id="96e30-304">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="96e30-305">Corrección para getsockname no Always devolviendo siempre el tipo de familia de sockets UNIX [alvent 1774]</span><span class="sxs-lookup"><span data-stu-id="96e30-305">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="96e30-306">Agregar compatibilidad para TIOCSTI [alvent 1863]</span><span class="sxs-lookup"><span data-stu-id="96e30-306">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="96e30-307">Los sockets sin bloqueo en el proceso de conexión deben devolver EAGAIN para los intentos de escritura [alvent 2846]</span><span class="sxs-lookup"><span data-stu-id="96e30-307">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="96e30-308">Compatibilidad con la interoperabilidad en VHD montados [alvent 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="96e30-308">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="96e30-309">Corregir el problema de comprobación de permisos en la carpeta raíz [alvent 3304]</span><span class="sxs-lookup"><span data-stu-id="96e30-309">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="96e30-310">Compatibilidad limitada para los ioctl de teclado TTY KDGKBTYPE, KDGKBMODE y KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="96e30-310">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="96e30-311">Las aplicaciones de interfaz de usuario de Windows deben ejecutarse incluso cuando se inician en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="96e30-311">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="96e30-312">Compilación 17704</span><span class="sxs-lookup"><span data-stu-id="96e30-312">Build 17704</span></span>
<span data-ttu-id="96e30-313">Para obtener información general sobre Windows sobre la compilación 17704, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span><span class="sxs-lookup"><span data-stu-id="96e30-313">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-314">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-314">WSL</span></span>
* <span data-ttu-id="96e30-315">Agregar WSL-u o--User Option [alvent 1203]</span><span class="sxs-lookup"><span data-stu-id="96e30-315">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="96e30-316">Corregir problemas de inicio de WSL cuando se habilita el inicio rápido [alvent 2576]</span><span class="sxs-lookup"><span data-stu-id="96e30-316">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="96e30-317">Los sockets de UNIX deben conservar las credenciales del mismo nivel desconectadas [alvent 3183]</span><span class="sxs-lookup"><span data-stu-id="96e30-317">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="96e30-318">Sockets de UNIX sin bloqueo con error indefinidamente con EAGAIN [alvent 3191]</span><span class="sxs-lookup"><span data-stu-id="96e30-318">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="96e30-319">Case = OFF es el nuevo tipo de montaje drvfs predeterminado [alvent 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="96e30-319">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="96e30-320">Consulte el [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="96e30-320">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="96e30-321">Agregue wslconfig/Terminate. para detener las distribuciones en ejecución.</span><span class="sxs-lookup"><span data-stu-id="96e30-321">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="96e30-322">Compilación 17692</span><span class="sxs-lookup"><span data-stu-id="96e30-322">Build 17692</span></span>
<span data-ttu-id="96e30-323">Para obtener información general sobre Windows sobre la compilación 17692, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span><span class="sxs-lookup"><span data-stu-id="96e30-323">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-324">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-324">WSL</span></span>
* <span data-ttu-id="96e30-325">Corrija el problema con las entradas del menú contextual del shell de WSL que no controlan correctamente las rutas de acceso con espacios.</span><span class="sxs-lookup"><span data-stu-id="96e30-325">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="96e30-326">Exponer la distinción de mayúsculas y minúsculas por directorio como atributo extendido</span><span class="sxs-lookup"><span data-stu-id="96e30-326">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="96e30-327">ARM64 Emular las operaciones de mantenimiento de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="96e30-327">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="96e30-328">Resolver el [problema dotnet](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="96e30-328">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="96e30-329">DrvFs: solo caracteres de escape en el intervalo privado que corresponden a un carácter de escape.</span><span class="sxs-lookup"><span data-stu-id="96e30-329">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="96e30-330">Compilación 17686</span><span class="sxs-lookup"><span data-stu-id="96e30-330">Build 17686</span></span>
<span data-ttu-id="96e30-331">Para obtener información general sobre Windows sobre la compilación 17686, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span><span class="sxs-lookup"><span data-stu-id="96e30-331">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-332">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-332">WSL</span></span>
* <span data-ttu-id="96e30-333">Error de corrección de errores en la validación de longitud del intérprete del analizador ELF [alvent 3154]</span><span class="sxs-lookup"><span data-stu-id="96e30-333">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="96e30-334">WSL los temporizadores absolutos con una hora en el pasado no se activan [alvent 3091]</span><span class="sxs-lookup"><span data-stu-id="96e30-334">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="96e30-335">Asegúrese de que los puntos de reanálisis recién creados se muestran como tales en el directorio principal.</span><span class="sxs-lookup"><span data-stu-id="96e30-335">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="96e30-336">Cree de forma atómica directorios con distinción entre mayúsculas y minúsculas en DrvFs.</span><span class="sxs-lookup"><span data-stu-id="96e30-336">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="96e30-337">Compilación 17677</span><span class="sxs-lookup"><span data-stu-id="96e30-337">Build 17677</span></span>
<span data-ttu-id="96e30-338">Para obtener información general sobre Windows sobre la compilación 17677, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span><span class="sxs-lookup"><span data-stu-id="96e30-338">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-339">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-339">WSL</span></span>
* <span data-ttu-id="96e30-340">Se ha corregido un problema adicional en el que las operaciones multiproceso podían devolver ENOENT, aunque el archivo exista.</span><span class="sxs-lookup"><span data-stu-id="96e30-340">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="96e30-341">[ALVENT 2712]</span><span class="sxs-lookup"><span data-stu-id="96e30-341">[GH 2712]</span></span>
* <span data-ttu-id="96e30-342">Se corrigió un error de inicio de WSL cuando UMCI está habilitado.</span><span class="sxs-lookup"><span data-stu-id="96e30-342">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="96e30-343">[ALVENT 3020]</span><span class="sxs-lookup"><span data-stu-id="96e30-343">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="96e30-344">Compilación 17666</span><span class="sxs-lookup"><span data-stu-id="96e30-344">Build 17666</span></span>
<span data-ttu-id="96e30-345">Para obtener información general sobre Windows sobre la compilación 17666, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span><span class="sxs-lookup"><span data-stu-id="96e30-345">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-346">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-346">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="96e30-347">ADVERTENCIA: Hay un problema que impide que WSL se ejecute en algunos chipsets AMD [alvent 3134].</span><span class="sxs-lookup"><span data-stu-id="96e30-347">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="96e30-348">Una corrección está lista y se convierte en la rama de compilación Insider.</span><span class="sxs-lookup"><span data-stu-id="96e30-348">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="96e30-349">Agregue el menú contextual del explorador para iniciar WSL [alvent 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="96e30-349">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="96e30-350">Para usar Mayús y hacer clic con el botón derecho en una ventana del explorador.</span><span class="sxs-lookup"><span data-stu-id="96e30-350">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="96e30-351">Corregir el comportamiento de no bloqueo de sockets de UNIX [alvent 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="96e30-351">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="96e30-352">Corrija el comando de NETLINK de bloqueo, tal como se muestra en alvent 2026.</span><span class="sxs-lookup"><span data-stu-id="96e30-352">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="96e30-353">Agregue compatibilidad para los marcadores de propagación de montaje [alvent 2911].</span><span class="sxs-lookup"><span data-stu-id="96e30-353">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="96e30-354">Corrección del problema con TRUNCATE no provocando eventos de inotify [alvent 2978].</span><span class="sxs-lookup"><span data-stu-id="96e30-354">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="96e30-355">Agregue la opción--exec de WSL. exe para invocar un solo binario sin un shell.</span><span class="sxs-lookup"><span data-stu-id="96e30-355">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="96e30-356">Add--Distribution Option para WSL. exe para seleccionar un distribución específico.</span><span class="sxs-lookup"><span data-stu-id="96e30-356">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="96e30-357">Compilación 17655 (omitir)</span><span class="sxs-lookup"><span data-stu-id="96e30-357">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="96e30-358">Para obtener información general sobre Windows sobre la compilación 17655, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="96e30-358">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-359">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-359">WSL</span></span>
* <span data-ttu-id="96e30-360">Compatibilidad limitada para dmesg.</span><span class="sxs-lookup"><span data-stu-id="96e30-360">Limited support for dmesg.</span></span> <span data-ttu-id="96e30-361">Ahora, las aplicaciones pueden iniciar sesión en dmesg.</span><span class="sxs-lookup"><span data-stu-id="96e30-361">Applications can now log to dmesg.</span></span> <span data-ttu-id="96e30-362">El controlador WSL registra información limitada en dmesg.</span><span class="sxs-lookup"><span data-stu-id="96e30-362">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="96e30-363">En el futuro, esto puede extenderse para llevar a cabo otros diagnósticos e información del controlador.</span><span class="sxs-lookup"><span data-stu-id="96e30-363">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="96e30-364">Nota: dmesg se admite actualmente a través `/dev/kmsg` de la interfaz de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="96e30-364">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="96e30-365">`syslog`la interfaz sycall todavía no se admite.</span><span class="sxs-lookup"><span data-stu-id="96e30-365">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="96e30-366">Y, por lo tanto, algunas `dmesg` de las opciones de la `-S`línea `-C` de comandos, como, no funcionan.</span><span class="sxs-lookup"><span data-stu-id="96e30-366">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="96e30-367">Se corrigió un problema en el que las operaciones multiproceso podían devolver ENOENT aunque el archivo exista.</span><span class="sxs-lookup"><span data-stu-id="96e30-367">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="96e30-368">[ALVENT 2712]</span><span class="sxs-lookup"><span data-stu-id="96e30-368">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="96e30-369">Compilación 17639 (omitir)</span><span class="sxs-lookup"><span data-stu-id="96e30-369">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="96e30-370">Para obtener información general sobre Windows sobre la compilación 17639, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="96e30-370">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-371">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-371">WSL</span></span>
* <span data-ttu-id="96e30-372">Cambiar el GID y el modo de dispositivos serie predeterminados para que coincidan con el nativo [alvent 3042]</span><span class="sxs-lookup"><span data-stu-id="96e30-372">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="96e30-373">DrvFs ahora admite atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="96e30-373">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="96e30-374">Nota: DrvFs tiene algunas limitaciones en cuanto al nombre de los atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="96e30-374">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="96e30-375">En concreto, algunos caracteres (como '/', ': ' y '\*') no están permitidos, y los nombres de atributos extendidos no distinguen mayúsculas de minúsculas en DrvFs</span><span class="sxs-lookup"><span data-stu-id="96e30-375">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="96e30-376">Compilación 17133 (rápida)</span><span class="sxs-lookup"><span data-stu-id="96e30-376">Build 17133 (Fast)</span></span>
<span data-ttu-id="96e30-377">Para obtener información general sobre Windows sobre la compilación 17133, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="96e30-377">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-378">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-378">WSL</span></span>
* <span data-ttu-id="96e30-379">Corrección de bloqueo en WSL.</span><span class="sxs-lookup"><span data-stu-id="96e30-379">Fix for hang in WSL.</span></span> <span data-ttu-id="96e30-380">[ALVENT 3039, 3034]</span><span class="sxs-lookup"><span data-stu-id="96e30-380">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="96e30-381">Compilación 17128 (rápida)</span><span class="sxs-lookup"><span data-stu-id="96e30-381">Build 17128 (Fast)</span></span>
<span data-ttu-id="96e30-382">Para obtener información general sobre Windows sobre la compilación 17128, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="96e30-382">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-383">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-383">WSL</span></span>
* <span data-ttu-id="96e30-384">None</span><span class="sxs-lookup"><span data-stu-id="96e30-384">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="96e30-385">Compilación 17627 (omitir)</span><span class="sxs-lookup"><span data-stu-id="96e30-385">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="96e30-386">Para obtener información general sobre Windows sobre la compilación 17627, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="96e30-386">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-387">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-387">WSL</span></span>
* <span data-ttu-id="96e30-388">Agregue compatibilidad para las operaciones compatibles con PI de Futex.</span><span class="sxs-lookup"><span data-stu-id="96e30-388">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="96e30-389">[ALVENT 1006]</span><span class="sxs-lookup"><span data-stu-id="96e30-389">[GH 1006]</span></span>
    * <span data-ttu-id="96e30-390">Tenga en cuenta que las prioridades no son actualmente una característica WSL admitida, por lo que hay limitaciones, pero el uso estándar debe estar desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="96e30-390">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="96e30-391">Compatibilidad con el Firewall de Windows para los procesos de WSL.</span><span class="sxs-lookup"><span data-stu-id="96e30-391">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="96e30-392">[ALVENT 1852]</span><span class="sxs-lookup"><span data-stu-id="96e30-392">[GH 1852]</span></span>
    * <span data-ttu-id="96e30-393">Por ejemplo, para permitir que el proceso de Python de WSL escuche en cualquier puerto, use el cmd de Windows con privilegios elevados:```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span><span class="sxs-lookup"><span data-stu-id="96e30-393">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="96e30-394">Para obtener más información sobre cómo agregar reglas de firewall, consulte [Link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span><span class="sxs-lookup"><span data-stu-id="96e30-394">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="96e30-395">Respetar el shell predeterminado del usuario cuando se usa WSL. exe.</span><span class="sxs-lookup"><span data-stu-id="96e30-395">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="96e30-396">[ALVENT 2372]</span><span class="sxs-lookup"><span data-stu-id="96e30-396">[GH 2372]</span></span>
* <span data-ttu-id="96e30-397">Informe de todas las interfaces de red como Ethernet.</span><span class="sxs-lookup"><span data-stu-id="96e30-397">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="96e30-398">[ALVENT 2996]</span><span class="sxs-lookup"><span data-stu-id="96e30-398">[GH 2996]</span></span>
* <span data-ttu-id="96e30-399">Mejor control del archivo/etc/passwd dañado.</span><span class="sxs-lookup"><span data-stu-id="96e30-399">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="96e30-400">[ALVENT 3001]</span><span class="sxs-lookup"><span data-stu-id="96e30-400">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="96e30-401">Console</span><span class="sxs-lookup"><span data-stu-id="96e30-401">Console</span></span>
* <span data-ttu-id="96e30-402">No hay correcciones.</span><span class="sxs-lookup"><span data-stu-id="96e30-402">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-403">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-403">LTP Results:</span></span>
<span data-ttu-id="96e30-404">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="96e30-404">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="96e30-405">Compilación 17618 (omitir)</span><span class="sxs-lookup"><span data-stu-id="96e30-405">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="96e30-406">Para obtener información general sobre Windows sobre la compilación 17618, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="96e30-406">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-407">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-407">WSL</span></span>
* <span data-ttu-id="96e30-408">Introduzca la funcionalidad de pseudoconsole para la interoperabilidad de NT [alvent 988, 1366, 1433, 1542, 2370, 2406].</span><span class="sxs-lookup"><span data-stu-id="96e30-408">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="96e30-409">El mecanismo de instalación heredado (lxrun. exe) está en desuso.</span><span class="sxs-lookup"><span data-stu-id="96e30-409">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="96e30-410">El mecanismo compatible para la instalación de distribuciones se realiza a través de la Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="96e30-410">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="96e30-411">Console</span><span class="sxs-lookup"><span data-stu-id="96e30-411">Console</span></span>
* <span data-ttu-id="96e30-412">No hay correcciones.</span><span class="sxs-lookup"><span data-stu-id="96e30-412">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-413">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-413">LTP Results:</span></span>
<span data-ttu-id="96e30-414">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="96e30-414">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="96e30-415">Compilación 17110</span><span class="sxs-lookup"><span data-stu-id="96e30-415">Build 17110</span></span>
<span data-ttu-id="96e30-416">Para obtener información general sobre Windows sobre la compilación 17110, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span><span class="sxs-lookup"><span data-stu-id="96e30-416">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-417">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-417">WSL</span></span>
* <span data-ttu-id="96e30-418">Permitir que/init termine de Windows [alvent 2928].</span><span class="sxs-lookup"><span data-stu-id="96e30-418">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="96e30-419">DrvFs Now usa la distinción de mayúsculas y minúsculas por directorio de forma predeterminada (equivalente a la opción de montaje "Case = dir").</span><span class="sxs-lookup"><span data-stu-id="96e30-419">DrvFs now uses per-directory case sensitivity by default (equivalent to the “case=dir” mount option).</span></span>
    * <span data-ttu-id="96e30-420">El uso de "Case = Force" (el comportamiento anterior) requiere el establecimiento de una clave del registro.</span><span class="sxs-lookup"><span data-stu-id="96e30-420">Using “case=force” (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="96e30-421">Ejecute el siguiente comando para habilitar "Case = Force" Si necesita usarlo: REG Add HKLM\SYSTEM\CurrentControlSet\Services\lxss/v DrvFsAllowForceCaseSensitivity/t REG_DWORD/d 1</span><span class="sxs-lookup"><span data-stu-id="96e30-421">Run the following command to enable “case=force” if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="96e30-422">Si tiene directorios existentes creados con WSL en una versión anterior de Windows que deben distinguir entre mayúsculas y minúsculas, use fsutil. exe para marcarlos con distinción de mayúsculas y <path> minúsculas: fsutil. exe File setcasesensitiveinfo enable</span><span class="sxs-lookup"><span data-stu-id="96e30-422">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="96e30-423">Cadenas de finalización NULAs devueltas por el syscall de uname.</span><span class="sxs-lookup"><span data-stu-id="96e30-423">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="96e30-424">Console</span><span class="sxs-lookup"><span data-stu-id="96e30-424">Console</span></span>
* <span data-ttu-id="96e30-425">No hay correcciones.</span><span class="sxs-lookup"><span data-stu-id="96e30-425">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-426">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-426">LTP Results:</span></span>
<span data-ttu-id="96e30-427">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="96e30-427">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="96e30-428">Compilación 17107</span><span class="sxs-lookup"><span data-stu-id="96e30-428">Build 17107</span></span>
<span data-ttu-id="96e30-429">Para obtener información general sobre Windows sobre la compilación 17107, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span><span class="sxs-lookup"><span data-stu-id="96e30-429">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-430">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-430">WSL</span></span>
* <span data-ttu-id="96e30-431">Compatibilidad con TCSETSF y TCSETSW en los puntos de conexión de Master PTY [alvent 2552].</span><span class="sxs-lookup"><span data-stu-id="96e30-431">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="96e30-432">Iniciar procesos de interoperabilidad simultáneos puede dar lugar a EINVAL [alvent 2813].</span><span class="sxs-lookup"><span data-stu-id="96e30-432">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="96e30-433">Corrección de PTRACE_ATTACH para mostrar el estado de seguimiento adecuado en/proc/PID/status.</span><span class="sxs-lookup"><span data-stu-id="96e30-433">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="96e30-434">Corregir la carrera en la que los procesos de corta duración clonados con las marcas CLEARTID y SETTID podrían salir sin borrar la dirección de TID.</span><span class="sxs-lookup"><span data-stu-id="96e30-434">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="96e30-435">Mostrar un mensaje al actualizar los directorios del sistema de archivos de Linux al pasar de una compilación anterior a la 17093.</span><span class="sxs-lookup"><span data-stu-id="96e30-435">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="96e30-436">Para obtener más detalles sobre los cambios del sistema de archivos 17093, consulte las notas de la versión de [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span><span class="sxs-lookup"><span data-stu-id="96e30-436">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="96e30-437">Console</span><span class="sxs-lookup"><span data-stu-id="96e30-437">Console</span></span>
* <span data-ttu-id="96e30-438">No hay correcciones.</span><span class="sxs-lookup"><span data-stu-id="96e30-438">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-439">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-439">LTP Results:</span></span>
<span data-ttu-id="96e30-440">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="96e30-440">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="96e30-441">Compilación 17101</span><span class="sxs-lookup"><span data-stu-id="96e30-441">Build 17101</span></span>
<span data-ttu-id="96e30-442">Para obtener información general sobre Windows sobre la compilación 17101, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="96e30-442">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-443">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-443">WSL</span></span>
* <span data-ttu-id="96e30-444">Compatibilidad con signalfd.</span><span class="sxs-lookup"><span data-stu-id="96e30-444">Support for signalfd.</span></span> <span data-ttu-id="96e30-445">[ALVENT 129]</span><span class="sxs-lookup"><span data-stu-id="96e30-445">[GH 129]</span></span>
* <span data-ttu-id="96e30-446">Admita nombres de archivo que contengan caracteres NTFS no válidos mediante su codificación como caracteres Unicode privados.</span><span class="sxs-lookup"><span data-stu-id="96e30-446">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="96e30-447">[ALVENT 1514]</span><span class="sxs-lookup"><span data-stu-id="96e30-447">[GH 1514]</span></span>
* <span data-ttu-id="96e30-448">El montaje automático se reservará en modo de solo lectura cuando no se admita la escritura.</span><span class="sxs-lookup"><span data-stu-id="96e30-448">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="96e30-449">[ALVENT 2603]</span><span class="sxs-lookup"><span data-stu-id="96e30-449">[GH 2603]</span></span>
* <span data-ttu-id="96e30-450">Permite pegar los pares suplentes Unicode (como los caracteres emoji).</span><span class="sxs-lookup"><span data-stu-id="96e30-450">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="96e30-451">[ALVENT 2765]</span><span class="sxs-lookup"><span data-stu-id="96e30-451">[GH 2765]</span></span>
* <span data-ttu-id="96e30-452">Los pseudo archivos de/proc y/sys deben devolver lectura y escritura listas para seleccionar, sondeo, epoll, et al. [alvent 2838]</span><span class="sxs-lookup"><span data-stu-id="96e30-452">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="96e30-453">Corrija el problema que podría hacer que el servicio pudiera entrar en un bucle infinito cuando el registro se haya alterado o esté dañado.</span><span class="sxs-lookup"><span data-stu-id="96e30-453">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="96e30-454">Corrija los mensajes de NetLink para trabajar con la versión más reciente (de nivel superior 4,14) de iproute2.</span><span class="sxs-lookup"><span data-stu-id="96e30-454">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="96e30-455">Console</span><span class="sxs-lookup"><span data-stu-id="96e30-455">Console</span></span>
* <span data-ttu-id="96e30-456">No hay correcciones.</span><span class="sxs-lookup"><span data-stu-id="96e30-456">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-457">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-457">LTP Results:</span></span>
<span data-ttu-id="96e30-458">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="96e30-458">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="96e30-459">Compilación 17093</span><span class="sxs-lookup"><span data-stu-id="96e30-459">Build 17093</span></span>
<span data-ttu-id="96e30-460">Para obtener información general sobre Windows sobre la compilación 17093, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span><span class="sxs-lookup"><span data-stu-id="96e30-460">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="96e30-461">Importante:</span><span class="sxs-lookup"><span data-stu-id="96e30-461">Important:</span></span>
<span data-ttu-id="96e30-462">Al iniciar WSL por primera vez después de actualizar a esta compilación, debe realizar algún trabajo al actualizar los directorios del sistema de archivos de Linux.</span><span class="sxs-lookup"><span data-stu-id="96e30-462">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="96e30-463">Esto puede tardar varios minutos, por lo que es posible que WSL se inicie lentamente.</span><span class="sxs-lookup"><span data-stu-id="96e30-463">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="96e30-464">Esto solo debería ocurrir una vez por cada distribución que haya instalado desde la tienda.</span><span class="sxs-lookup"><span data-stu-id="96e30-464">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="96e30-465">Compatibilidad mejorada de distinción de mayúsculas y minúsculas en DrvFs.</span><span class="sxs-lookup"><span data-stu-id="96e30-465">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="96e30-466">DrvFs admite ahora la distinción de mayúsculas y minúsculas por directorio.</span><span class="sxs-lookup"><span data-stu-id="96e30-466">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="96e30-467">Se trata de una nueva marca que se puede establecer en directorios para indicar que todas las operaciones de esos directorios deben tratarse como con distinción de mayúsculas y minúsculas, lo que permite que las aplicaciones de Windows abran archivos que solo difieren en mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="96e30-467">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="96e30-468">DrvFs tiene nuevas opciones de montaje que controlan la distinción de mayúsculas y minúsculas por directorio.</span><span class="sxs-lookup"><span data-stu-id="96e30-468">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="96e30-469">Case = Force: todos los directorios se tratan con distinción de mayúsculas y minúsculas (excepto la raíz de la unidad).</span><span class="sxs-lookup"><span data-stu-id="96e30-469">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="96e30-470">Los nuevos directorios creados con WSL se marcan con distinción de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="96e30-470">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="96e30-471">Este es el comportamiento heredado excepto para marcar los nuevos directorios que distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="96e30-471">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="96e30-472">Case = dir: solo los directorios con la marca de distinción de mayúsculas y minúsculas por directorio se tratan como distinguir mayúsculas de minúsculas; otros directorios no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="96e30-472">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="96e30-473">Los nuevos directorios creados con WSL se marcan con distinción de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="96e30-473">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="96e30-474">Case = OFF: solo los directorios con la marca de distinción de mayúsculas y minúsculas por directorio se tratan como distinguir mayúsculas de minúsculas; otros directorios no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="96e30-474">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="96e30-475">Los nuevos directorios creados con WSL se marcan como no distinguir mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="96e30-475">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="96e30-476">Nota: los directorios creados por WSL en versiones anteriores no tienen esta marca establecida, por lo que no se tratará como distinción entre mayúsculas y minúsculas si usa la opción "Case = dir".</span><span class="sxs-lookup"><span data-stu-id="96e30-476">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the “case=dir” option.</span></span> <span data-ttu-id="96e30-477">Próximamente se establecerá una manera de establecer esta marca en los directorios existentes.</span><span class="sxs-lookup"><span data-stu-id="96e30-477">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="96e30-478">Ejemplo de montaje con estas opciones (en el caso de las unidades existentes, primero debe desmontar antes de poder montar con distintas opciones): sudo mount-t drvfs C:/mnt/c-o Case = dir</span><span class="sxs-lookup"><span data-stu-id="96e30-478">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="96e30-479">Por ahora, Case = Force sigue siendo la opción predeterminada.</span><span class="sxs-lookup"><span data-stu-id="96e30-479">For now, case=force is still the default option.</span></span> <span data-ttu-id="96e30-480">Se cambiará a case = dir en el futuro.</span><span class="sxs-lookup"><span data-stu-id="96e30-480">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="96e30-481">Ahora puede usar barras diagonales en las rutas de acceso de Windows al montar DrvFs, por ejemplo: sudo mount-t DrvFs//Server/SHARE/mnt/share</span><span class="sxs-lookup"><span data-stu-id="96e30-481">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="96e30-482">WSL ahora procesa el archivo/etc/fstab durante el inicio de la instancia [alvent 2636].</span><span class="sxs-lookup"><span data-stu-id="96e30-482">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="96e30-483">Esto se hace antes de montar automáticamente las unidades de DrvFs; las unidades que ya se hayan montado mediante fstab no se volverán a montar automáticamente, lo que le permitirá cambiar el punto de montaje para unidades específicas.</span><span class="sxs-lookup"><span data-stu-id="96e30-483">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="96e30-484">Este comportamiento se puede desactivar mediante WSL. conf.</span><span class="sxs-lookup"><span data-stu-id="96e30-484">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="96e30-485">Los archivos Mount, mountinfo y mountstats de/proc convierten correctamente en caracteres especiales, como barras diagonales inversas y espacios [alvent 2799]</span><span class="sxs-lookup"><span data-stu-id="96e30-485">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="96e30-486">Los archivos especiales creados con DrvFs, como los vínculos simbólicos de WSL, o FIFO y Sockets cuando se habilitan los metadatos, ahora se pueden copiar y pasar de Windows.</span><span class="sxs-lookup"><span data-stu-id="96e30-486">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="96e30-487">WSL es más configurable con WSL. conf</span><span class="sxs-lookup"><span data-stu-id="96e30-487">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="96e30-488">Hemos agregado un método para que configure automáticamente ciertas funciones en WSL que se aplicarán cada vez que inicie el subsistema.</span><span class="sxs-lookup"><span data-stu-id="96e30-488">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="96e30-489">Esto incluye opciones de montaje automático y configuración de red.</span><span class="sxs-lookup"><span data-stu-id="96e30-489">This includes automount options and network configuration.</span></span> <span data-ttu-id="96e30-490">Obtenga más información en la entrada de blog en: https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="96e30-490">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="afunix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="96e30-491">AF_UNIX permite conexiones de socket entre procesos de Linux en WSL y procesos nativos de Windows</span><span class="sxs-lookup"><span data-stu-id="96e30-491">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="96e30-492">Las aplicaciones de WSL y Windows ahora pueden comunicarse entre sí a través de sockets de Unix.</span><span class="sxs-lookup"><span data-stu-id="96e30-492">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="96e30-493">Imagine que quiere ejecutar un servicio en Windows y hacer que esté disponible para las aplicaciones de Windows y WSL.</span><span class="sxs-lookup"><span data-stu-id="96e30-493">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="96e30-494">Ahora, eso es posible con los sockets de Unix.</span><span class="sxs-lookup"><span data-stu-id="96e30-494">Now, that’s possible with Unix sockets.</span></span> <span data-ttu-id="96e30-495">Lea más en nuestra entrada de blog en https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="96e30-495">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-496">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-496">WSL</span></span>
* <span data-ttu-id="96e30-497">Compatibilidad con mmap () con MAP_NORESERVE [alvent 121, 2784]</span><span class="sxs-lookup"><span data-stu-id="96e30-497">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="96e30-498">Compatibilidad con CLONE_PTRACE y CLONE_UNTRACED [alvent 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="96e30-498">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="96e30-499">Controlar la señal de terminación no SIGCHLD en el clon [alvent 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="96e30-499">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="96e30-500">Stub/proc/sys/FS/inotify/max_user_instances y/proc/sys/FS/inotify/max_user_watches [alvent 1705]</span><span class="sxs-lookup"><span data-stu-id="96e30-500">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="96e30-501">Error al cargar binarios de ELF que contienen encabezados de carga con desplazamientos distintos de cero [alvent 1884]</span><span class="sxs-lookup"><span data-stu-id="96e30-501">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="96e30-502">Cero bytes de página finales al cargar imágenes.</span><span class="sxs-lookup"><span data-stu-id="96e30-502">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="96e30-503">Reducir los casos en los que execve finaliza el proceso de forma silenciosa</span><span class="sxs-lookup"><span data-stu-id="96e30-503">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="96e30-504">Console</span><span class="sxs-lookup"><span data-stu-id="96e30-504">Console</span></span>
* <span data-ttu-id="96e30-505">No hay correcciones.</span><span class="sxs-lookup"><span data-stu-id="96e30-505">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-506">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-506">LTP Results:</span></span>
<span data-ttu-id="96e30-507">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="96e30-507">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="96e30-508">Compilación 17083</span><span class="sxs-lookup"><span data-stu-id="96e30-508">Build 17083</span></span>
<span data-ttu-id="96e30-509">Para obtener información general sobre Windows sobre la compilación 17083, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="96e30-509">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-510">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-510">WSL</span></span>
* <span data-ttu-id="96e30-511">Se corrigió la BugCheck relacionada con epoll [alvent 2798, 2801, 2857]</span><span class="sxs-lookup"><span data-stu-id="96e30-511">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="96e30-512">Se han corregido bloqueos al desactivar ASLR [alvent 1185, 2870]</span><span class="sxs-lookup"><span data-stu-id="96e30-512">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="96e30-513">Asegurarse de que las operaciones de mmap aparecen atómicas [alvent 2732]</span><span class="sxs-lookup"><span data-stu-id="96e30-513">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="96e30-514">Console</span><span class="sxs-lookup"><span data-stu-id="96e30-514">Console</span></span>
* <span data-ttu-id="96e30-515">No hay correcciones.</span><span class="sxs-lookup"><span data-stu-id="96e30-515">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-516">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-516">LTP Results:</span></span>
<span data-ttu-id="96e30-517">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="96e30-517">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="96e30-518">Compilación 17074</span><span class="sxs-lookup"><span data-stu-id="96e30-518">Build 17074</span></span>
<span data-ttu-id="96e30-519">Para obtener información general sobre Windows sobre la compilación 17074, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span><span class="sxs-lookup"><span data-stu-id="96e30-519">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-520">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-520">WSL</span></span>
* <span data-ttu-id="96e30-521">Formato de almacenamiento fijo de los metadatos de DrvFs [alvent 2777]</span><span class="sxs-lookup"><span data-stu-id="96e30-521">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="96e30-522">**Importante:** Los metadatos de DrvFs creados antes de esta compilación no se mostrarán correctamente o no se mostrarán en absoluto.</span><span class="sxs-lookup"><span data-stu-id="96e30-522">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="96e30-523">Para corregir los archivos afectados, use chmod y chown para volver a aplicar los metadatos.</span><span class="sxs-lookup"><span data-stu-id="96e30-523">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="96e30-524">Se corrigió un problema con varias señales y llamadas syscall reiniciables.</span><span class="sxs-lookup"><span data-stu-id="96e30-524">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="96e30-525">Console</span><span class="sxs-lookup"><span data-stu-id="96e30-525">Console</span></span>
* <span data-ttu-id="96e30-526">No hay correcciones.</span><span class="sxs-lookup"><span data-stu-id="96e30-526">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-527">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-527">LTP Results:</span></span>
<span data-ttu-id="96e30-528">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="96e30-528">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="96e30-529">Compilación 17063</span><span class="sxs-lookup"><span data-stu-id="96e30-529">Build 17063</span></span>
<span data-ttu-id="96e30-530">Para obtener información general sobre Windows sobre la compilación 17063, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span><span class="sxs-lookup"><span data-stu-id="96e30-530">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="96e30-531">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-531">WSL</span></span>
* <span data-ttu-id="96e30-532">DrvFs admite metadatos de Linux adicionales.</span><span class="sxs-lookup"><span data-stu-id="96e30-532">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="96e30-533">Esto permite establecer el propietario y el modo de los archivos con chmod/chown y también la creación de archivos especiales como FIFO, sockets de UNIX y archivos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="96e30-533">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="96e30-534">Esta opción está deshabilitada de forma predeterminada ya que sigue siendo experimental.</span><span class="sxs-lookup"><span data-stu-id="96e30-534">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="96e30-535">**Nota:**  Se corrigió un error en el formato de metadatos usado por DrvFs.</span><span class="sxs-lookup"><span data-stu-id="96e30-535">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="96e30-536">Aunque los metadatos funcionan en esta compilación para experimentación, las compilaciones futuras no leerán correctamente los metadatos creados por esta compilación.</span><span class="sxs-lookup"><span data-stu-id="96e30-536">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="96e30-537">Es posible que tenga que actualizar manualmente el propietario de los archivos modificados y se tendrán que volver a crear los dispositivos con un identificador de dispositivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="96e30-537">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="96e30-538">Para habilitar, Monte DrvFs con la opción de metadatos (para habilitarlo en un montaje existente, primero debe desmontarlo):</span><span class="sxs-lookup"><span data-stu-id="96e30-538">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="96e30-539">Los permisos de Linux se agregan como metadatos adicionales al archivo; no afectan a los permisos de Windows.</span><span class="sxs-lookup"><span data-stu-id="96e30-539">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="96e30-540">Recuerde que la edición de un archivo mediante un editor de Windows puede quitar los metadatos.</span><span class="sxs-lookup"><span data-stu-id="96e30-540">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="96e30-541">En este caso, el archivo volverá a sus permisos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="96e30-541">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="96e30-542">Se han agregado opciones de montaje a DrvFs para controlar archivos sin metadatos.</span><span class="sxs-lookup"><span data-stu-id="96e30-542">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="96e30-543">UID: el identificador de usuario que se usa para el propietario de todos los archivos.</span><span class="sxs-lookup"><span data-stu-id="96e30-543">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="96e30-544">GID: el identificador de grupo que se usa para el propietario de todos los archivos.</span><span class="sxs-lookup"><span data-stu-id="96e30-544">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="96e30-545">umask: máscara octal de permisos que se van a excluir para todos los archivos y directorios.</span><span class="sxs-lookup"><span data-stu-id="96e30-545">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="96e30-546">fMask: máscara octal de permisos que se van a excluir para todos los archivos normales.</span><span class="sxs-lookup"><span data-stu-id="96e30-546">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="96e30-547">dmask: máscara octal de permisos que se van a excluir para todos los directorios.</span><span class="sxs-lookup"><span data-stu-id="96e30-547">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="96e30-548">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="96e30-548">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="96e30-549">Combine con la opción de metadatos para especificar los permisos predeterminados para los archivos sin metadatos.</span><span class="sxs-lookup"><span data-stu-id="96e30-549">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="96e30-550">Presentó una nueva variable de entorno `WSLENV`,, para configurar cómo fluyen las variables de entorno entre WSL y Win32.</span><span class="sxs-lookup"><span data-stu-id="96e30-550">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="96e30-551">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="96e30-551">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="96e30-552">`WSLENV`es una lista delimitada por signos de dos puntos de variables de entorno que se puede incluir al iniciar procesos de WSL desde los procesos Win32 o Win32 desde WSL.</span><span class="sxs-lookup"><span data-stu-id="96e30-552">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="96e30-553">Cada variable puede tener como sufijo una barra diagonal seguida de marcas para especificar cómo se va a traducir.</span><span class="sxs-lookup"><span data-stu-id="96e30-553">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="96e30-554">m El valor es una ruta de acceso que se debe traducir entre las rutas de acceso de WSL y las rutas de acceso de Win32.</span><span class="sxs-lookup"><span data-stu-id="96e30-554">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="96e30-555">CG El valor es una lista de rutas de acceso.</span><span class="sxs-lookup"><span data-stu-id="96e30-555">l: The value is a list of paths.</span></span> <span data-ttu-id="96e30-556">En WSL, se trata de una lista delimitada por signos de dos puntos.</span><span class="sxs-lookup"><span data-stu-id="96e30-556">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="96e30-557">En Win32, se trata de una lista delimitada por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="96e30-557">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="96e30-558">5\.50 Solo se debe incluir el valor al invocar WSL desde Win32</span><span class="sxs-lookup"><span data-stu-id="96e30-558">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="96e30-559">con Solo se debe incluir el valor al invocar a Win32 desde WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-559">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="96e30-560">Puede establecer `WSLENV` en. bashrc o en el entorno de Windows personalizado para el usuario.</span><span class="sxs-lookup"><span data-stu-id="96e30-560">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="96e30-561">los montajes de drvfs conservan correctamente las marcas de tiempo de tar, CP-p (alvent 1939)</span><span class="sxs-lookup"><span data-stu-id="96e30-561">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="96e30-562">los vínculos simbólicos de drvfs informan del tamaño correcto (alvent 2641)</span><span class="sxs-lookup"><span data-stu-id="96e30-562">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="96e30-563">lectura/escritura funciona para tamaños de e/s muy grandes (alvent 2653)</span><span class="sxs-lookup"><span data-stu-id="96e30-563">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="96e30-564">waitpid funciona con identificadores de grupo de procesos (alvent 2534)</span><span class="sxs-lookup"><span data-stu-id="96e30-564">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="96e30-565">rendimiento mmap significativamente mejorado para regiones de reserva grande; mejora el rendimiento de GHC (alvent 1671)</span><span class="sxs-lookup"><span data-stu-id="96e30-565">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="96e30-566">la personalidad es compatible con READ_IMPLIES_EXEC; correcciones y CLISP (alvent 1185)</span><span class="sxs-lookup"><span data-stu-id="96e30-566">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="96e30-567">mprotect admite PROT_GROWSDOWN; corrige CLISP (alvent 1128)</span><span class="sxs-lookup"><span data-stu-id="96e30-567">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="96e30-568">correcciones de errores de página en modo de sobreconfirmación; corrige SBCL (alvent 1128)</span><span class="sxs-lookup"><span data-stu-id="96e30-568">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="96e30-569">Clone admite más combinaciones de marcas</span><span class="sxs-lookup"><span data-stu-id="96e30-569">clone supports more flags combinations</span></span>
* <span data-ttu-id="96e30-570">Compatibilidad con Select/epoll de archivos de epoll (antes de una operación no operativa).</span><span class="sxs-lookup"><span data-stu-id="96e30-570">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="96e30-571">Notificar a ptrace de llamadas syscall no implementado.</span><span class="sxs-lookup"><span data-stu-id="96e30-571">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="96e30-572">Omitir las interfaces que no están al generar los servidores de nombres resolv. conf [alvent 2694]</span><span class="sxs-lookup"><span data-stu-id="96e30-572">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="96e30-573">Enumerar las interfaces de red sin dirección física.</span><span class="sxs-lookup"><span data-stu-id="96e30-573">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="96e30-574">[ALVENT 2685]</span><span class="sxs-lookup"><span data-stu-id="96e30-574">[GH 2685]</span></span>
* <span data-ttu-id="96e30-575">Correcciones de errores adicionales y mejoras.</span><span class="sxs-lookup"><span data-stu-id="96e30-575">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="96e30-576">Herramientas de Linux disponibles para desarrolladores en Windows</span><span class="sxs-lookup"><span data-stu-id="96e30-576">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="96e30-577">La cadena de herramientas de la línea de comandos de Windows incluye bsdtar (tar) y rizo.</span><span class="sxs-lookup"><span data-stu-id="96e30-577">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="96e30-578">Lea [este blog](https://aka.ms/tarcurlwindows) para obtener más información acerca de cómo agregar estas dos nuevas herramientas y ver cómo están dando forma a la experiencia del Desarrollador en Windows.</span><span class="sxs-lookup"><span data-stu-id="96e30-578">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they’re shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="96e30-579">`AF_UNIX`está disponible en el SDK de Windows Insider (17061 +).</span><span class="sxs-lookup"><span data-stu-id="96e30-579">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="96e30-580">Lea [este blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) para obtener más información `AF_UNIX` sobre y cómo los desarrolladores de Windows pueden usarlo.</span><span class="sxs-lookup"><span data-stu-id="96e30-580">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="96e30-581">Console</span><span class="sxs-lookup"><span data-stu-id="96e30-581">Console</span></span>
* <span data-ttu-id="96e30-582">No hay correcciones.</span><span class="sxs-lookup"><span data-stu-id="96e30-582">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-583">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-583">LTP Results:</span></span>
<span data-ttu-id="96e30-584">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="96e30-584">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="96e30-585">Compilación 17046</span><span class="sxs-lookup"><span data-stu-id="96e30-585">Build 17046</span></span>

<span data-ttu-id="96e30-586">Para obtener información general sobre Windows sobre la compilación 17046, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span><span class="sxs-lookup"><span data-stu-id="96e30-586">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="96e30-587">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-587">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="96e30-588">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-588">WSL</span></span>
- <span data-ttu-id="96e30-589">Permite que los procesos se ejecuten sin un terminal activo.</span><span class="sxs-lookup"><span data-stu-id="96e30-589">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="96e30-590">[Alvent 709, 1007, 1511, 2252, 2391, et al.]</span><span class="sxs-lookup"><span data-stu-id="96e30-590">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="96e30-591">Mejor compatibilidad con CLONE_VFORK y CLONE_VM.</span><span class="sxs-lookup"><span data-stu-id="96e30-591">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="96e30-592">[ALVENT 1878, 2615]</span><span class="sxs-lookup"><span data-stu-id="96e30-592">[GH 1878, 2615]</span></span>
- <span data-ttu-id="96e30-593">Omita los controladores de filtro TDI para las operaciones de red de WSL.</span><span class="sxs-lookup"><span data-stu-id="96e30-593">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="96e30-594">[ALVENT 1554]</span><span class="sxs-lookup"><span data-stu-id="96e30-594">[GH 1554]</span></span>
- <span data-ttu-id="96e30-595">DrvFs crea vínculos simbólicos NT cuando se cumplen determinadas condiciones.</span><span class="sxs-lookup"><span data-stu-id="96e30-595">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="96e30-596">[ALVENT 353, 1475, 2602]</span><span class="sxs-lookup"><span data-stu-id="96e30-596">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="96e30-597">El destino del vínculo debe ser relativo, no debe cruzar ningún punto de montaje o vínculos simbólicos, y debe existir.</span><span class="sxs-lookup"><span data-stu-id="96e30-597">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="96e30-598">El usuario debe tener SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (esto normalmente requiere que inicie WSL. exe con privilegios elevados), a menos que esté activado el modo de desarrollador.</span><span class="sxs-lookup"><span data-stu-id="96e30-598">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="96e30-599">En todas las demás situaciones, DrvFs todavía crea vínculos simbólicos de WSL.</span><span class="sxs-lookup"><span data-stu-id="96e30-599">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="96e30-600">Permite ejecutar instancias de WSL con privilegios elevados y no elevados simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="96e30-600">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="96e30-601">Compatibilidad con/proc/sys/kernel/Yama/ptrace_scope</span><span class="sxs-lookup"><span data-stu-id="96e30-601">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="96e30-602">Agregue wslpath para realizar conversiones de rutas de acceso de Windows de WSL <->.</span><span class="sxs-lookup"><span data-stu-id="96e30-602">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="96e30-603">[Alvent 522, 1243, 1834, 2327, et al.]</span><span class="sxs-lookup"><span data-stu-id="96e30-603">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a><span data-ttu-id="96e30-604">Console</span><span class="sxs-lookup"><span data-stu-id="96e30-604">Console</span></span>
- <span data-ttu-id="96e30-605">No hay correcciones.</span><span class="sxs-lookup"><span data-stu-id="96e30-605">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-606">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-606">LTP Results:</span></span>
<span data-ttu-id="96e30-607">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="96e30-607">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="96e30-608">Compilación 17040</span><span class="sxs-lookup"><span data-stu-id="96e30-608">Build 17040</span></span>

<span data-ttu-id="96e30-609">Para obtener información general sobre Windows sobre la compilación 17040, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span><span class="sxs-lookup"><span data-stu-id="96e30-609">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-610">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-610">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="96e30-611">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-611">WSL</span></span>
- <span data-ttu-id="96e30-612">No hay correcciones desde 17035.</span><span class="sxs-lookup"><span data-stu-id="96e30-612">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="96e30-613">Console</span><span class="sxs-lookup"><span data-stu-id="96e30-613">Console</span></span>
- <span data-ttu-id="96e30-614">No hay correcciones desde 17035.</span><span class="sxs-lookup"><span data-stu-id="96e30-614">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-615">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-615">LTP Results:</span></span>
<span data-ttu-id="96e30-616">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="96e30-616">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="96e30-617">Compilación 17035</span><span class="sxs-lookup"><span data-stu-id="96e30-617">Build 17035</span></span>

<span data-ttu-id="96e30-618">Para obtener información general sobre Windows sobre la compilación 17035, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span><span class="sxs-lookup"><span data-stu-id="96e30-618">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-619">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-619">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="96e30-620">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-620">WSL</span></span>
- <span data-ttu-id="96e30-621">En ocasiones, el acceso a los archivos de DrvFs podría producir errores con EINVAL.</span><span class="sxs-lookup"><span data-stu-id="96e30-621">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="96e30-622">[ALVENT 2448]</span><span class="sxs-lookup"><span data-stu-id="96e30-622">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="96e30-623">Console</span><span class="sxs-lookup"><span data-stu-id="96e30-623">Console</span></span>
- <span data-ttu-id="96e30-624">Pérdida de color al insertar o eliminar líneas en modo VT.</span><span class="sxs-lookup"><span data-stu-id="96e30-624">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-625">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-625">LTP Results:</span></span>
<span data-ttu-id="96e30-626">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="96e30-626">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="96e30-627">Compilación 17025</span><span class="sxs-lookup"><span data-stu-id="96e30-627">Build 17025</span></span>

<span data-ttu-id="96e30-628">Para obtener información general sobre Windows sobre la compilación 17025, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span><span class="sxs-lookup"><span data-stu-id="96e30-628">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-629">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-629">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="96e30-630">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-630">WSL</span></span>
- <span data-ttu-id="96e30-631">Iniciar procesos iniciales en un nuevo grupo de procesos en primer plano [alvent 1653, 2510].</span><span class="sxs-lookup"><span data-stu-id="96e30-631">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="96e30-632">Correcciones de entrega de SIGHUP [alvent 2496].</span><span class="sxs-lookup"><span data-stu-id="96e30-632">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="96e30-633">Generar nombre de puente virtual predeterminado si no se proporciona ninguno [alvent 2497].</span><span class="sxs-lookup"><span data-stu-id="96e30-633">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="96e30-634">Implementar/proc/sys/kernel/Random/boot_id [al2518].</span><span class="sxs-lookup"><span data-stu-id="96e30-634">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="96e30-635">Más correcciones de la canalización stdout/stderr de interoperabilidad.</span><span class="sxs-lookup"><span data-stu-id="96e30-635">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="96e30-636">Llamada del sistema syncfs de stub.</span><span class="sxs-lookup"><span data-stu-id="96e30-636">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="96e30-637">Console</span><span class="sxs-lookup"><span data-stu-id="96e30-637">Console</span></span>
- <span data-ttu-id="96e30-638">Corrección de la traducción de VT de entrada para consolas de terceros [alvent 111]</span><span class="sxs-lookup"><span data-stu-id="96e30-638">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-639">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-639">LTP Results:</span></span>
<span data-ttu-id="96e30-640">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="96e30-640">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="96e30-641">Compilación 17017</span><span class="sxs-lookup"><span data-stu-id="96e30-641">Build 17017</span></span>

<span data-ttu-id="96e30-642">Para obtener información general sobre Windows sobre la compilación 17017, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span><span class="sxs-lookup"><span data-stu-id="96e30-642">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-643">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-643">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="96e30-644">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-644">WSL</span></span>
- <span data-ttu-id="96e30-645">Omitir los encabezados de programa ELF vacíos [alvent 330].</span><span class="sxs-lookup"><span data-stu-id="96e30-645">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="96e30-646">Permita que LxssManager Cree instancias de WSL para usuarios no interactivos (SSH y soporte de tareas programadas) [alvent 777, 1602].</span><span class="sxs-lookup"><span data-stu-id="96e30-646">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="96e30-647">Compatibilidad con escenarios de WSL-> Win32-> WSL ("Inicio") [alvent 1228].</span><span class="sxs-lookup"><span data-stu-id="96e30-647">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="96e30-648">Compatibilidad limitada para la terminación de las aplicaciones de consola que se invocan a través de la interoperabilidad [alvent 1614].</span><span class="sxs-lookup"><span data-stu-id="96e30-648">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="96e30-649">Compatibilidad con las opciones de montaje para devpts [alvent 1948].</span><span class="sxs-lookup"><span data-stu-id="96e30-649">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="96e30-650">Inicio de bloqueo secundario de ptrace [alvent 2333].</span><span class="sxs-lookup"><span data-stu-id="96e30-650">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="96e30-651">EPOLLET faltan algunos eventos [alvent 2462].</span><span class="sxs-lookup"><span data-stu-id="96e30-651">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="96e30-652">Devolver más datos para PTRACE_GETSIGINFO.</span><span class="sxs-lookup"><span data-stu-id="96e30-652">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="96e30-653">Getdents con lseek proporciona resultados incorrectos.</span><span class="sxs-lookup"><span data-stu-id="96e30-653">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="96e30-654">Corrección de bloqueo de la aplicación de interoperabilidad Win32, esperando la entrada en una canalización que no tiene más datos.</span><span class="sxs-lookup"><span data-stu-id="96e30-654">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="96e30-655">Compatibilidad de O_ASYNC con archivos TTY/PTY.</span><span class="sxs-lookup"><span data-stu-id="96e30-655">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="96e30-656">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-656">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="96e30-657">Console</span><span class="sxs-lookup"><span data-stu-id="96e30-657">Console</span></span>
- <span data-ttu-id="96e30-658">No hay cambios relacionados con la consola en esta versión.</span><span class="sxs-lookup"><span data-stu-id="96e30-658">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-659">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-659">LTP Results:</span></span>
<span data-ttu-id="96e30-660">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="96e30-660">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="96e30-661">Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="96e30-661">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="96e30-662">Compilación 16288</span><span class="sxs-lookup"><span data-stu-id="96e30-662">Build 16288</span></span>

<span data-ttu-id="96e30-663">Para obtener información general sobre Windows sobre la compilación 16288, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span><span class="sxs-lookup"><span data-stu-id="96e30-663">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-664">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-664">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="96e30-665">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-665">WSL</span></span>
- <span data-ttu-id="96e30-666">Inicializar y notificar correctamente UID, GID y el modo para los descriptores de archivo de socket [alvent 2490]</span><span class="sxs-lookup"><span data-stu-id="96e30-666">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="96e30-667">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-667">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="96e30-668">Console</span><span class="sxs-lookup"><span data-stu-id="96e30-668">Console</span></span>
- <span data-ttu-id="96e30-669">No hay cambios relacionados con la consola en esta versión.</span><span class="sxs-lookup"><span data-stu-id="96e30-669">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-670">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-670">LTP Results:</span></span>
<span data-ttu-id="96e30-671">Sin cambios desde 16273</span><span class="sxs-lookup"><span data-stu-id="96e30-671">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="96e30-672">Compilación 16278</span><span class="sxs-lookup"><span data-stu-id="96e30-672">Build 16278</span></span>

<span data-ttu-id="96e30-673">Para obtener información general sobre Windows sobre la compilación 162738, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span><span class="sxs-lookup"><span data-stu-id="96e30-673">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-674">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-674">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="96e30-675">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-675">WSL</span></span>
- <span data-ttu-id="96e30-676">Anular explícitamente las vistas asignadas de las secciones respaldadas por archivos al desplazar hacia abajo el estado LX MM [alvent 2415]</span><span class="sxs-lookup"><span data-stu-id="96e30-676">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="96e30-677">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-677">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="96e30-678">Console</span><span class="sxs-lookup"><span data-stu-id="96e30-678">Console</span></span>
- <span data-ttu-id="96e30-679">No hay cambios relacionados con la consola en esta versión.</span><span class="sxs-lookup"><span data-stu-id="96e30-679">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-680">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-680">LTP Results:</span></span>
<span data-ttu-id="96e30-681">Sin cambios desde 16273</span><span class="sxs-lookup"><span data-stu-id="96e30-681">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="96e30-682">Compilación 16275</span><span class="sxs-lookup"><span data-stu-id="96e30-682">Build 16275</span></span>

<span data-ttu-id="96e30-683">Para obtener información general sobre Windows sobre la compilación 162735, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span><span class="sxs-lookup"><span data-stu-id="96e30-683">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-684">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-684">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="96e30-685">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-685">WSL</span></span>
- <span data-ttu-id="96e30-686">No hay ningún cambio relacionado con WSL en esta versión.</span><span class="sxs-lookup"><span data-stu-id="96e30-686">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="96e30-687">Console</span><span class="sxs-lookup"><span data-stu-id="96e30-687">Console</span></span>
- <span data-ttu-id="96e30-688">No hay cambios relacionados con la consola en esta versión.</span><span class="sxs-lookup"><span data-stu-id="96e30-688">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-689">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-689">LTP Results:</span></span>
<span data-ttu-id="96e30-690">Sin cambios desde 16273</span><span class="sxs-lookup"><span data-stu-id="96e30-690">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="96e30-691">Compilación 16273</span><span class="sxs-lookup"><span data-stu-id="96e30-691">Build 16273</span></span>

<span data-ttu-id="96e30-692">Para obtener información general sobre Windows sobre la compilación 16273, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span><span class="sxs-lookup"><span data-stu-id="96e30-692">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-693">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-693">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="96e30-694">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-694">WSL</span></span>
- <span data-ttu-id="96e30-695">Se ha corregido un problema por el que DrvFs a veces indicó un tipo de archivo incorrecto para los directorios [alvent 2392]</span><span class="sxs-lookup"><span data-stu-id="96e30-695">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="96e30-696">Permitir la creación de NETLINK_KOBJECT_UEVENT Sockets para desbloquear programas que usan UEVENT [al1121, 2293, 2242, 2295, 2235, 648, 637]</span><span class="sxs-lookup"><span data-stu-id="96e30-696">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="96e30-697">Agregar compatibilidad para conexión sin bloqueo [alvent 903, 1391, 1584, 1585, 1829, 2290, 2314]</span><span class="sxs-lookup"><span data-stu-id="96e30-697">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="96e30-698">Implementación de la marca de llamada del sistema Clone CLONE_FS [alvent 2242]</span><span class="sxs-lookup"><span data-stu-id="96e30-698">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="96e30-699">Corregir los problemas que no controlan las tabulaciones o comillas correctamente en la interoperabilidad de NT [alvent 1625, 2164]</span><span class="sxs-lookup"><span data-stu-id="96e30-699">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="96e30-700">Resolver el error de acceso denegado al intentar volver a iniciar instancias de WSL [alvent 651, 2095]</span><span class="sxs-lookup"><span data-stu-id="96e30-700">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="96e30-701">Implementación de las operaciones de Futex FUTEX_REQUEUE y FUTEX_CMP_REQUEUE [alvent 2242]</span><span class="sxs-lookup"><span data-stu-id="96e30-701">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="96e30-702">Corrección de permisos para varios archivos de SysFs [alvent 2214]</span><span class="sxs-lookup"><span data-stu-id="96e30-702">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="96e30-703">Corregir bloqueo de pila de Haskell durante la instalación [alvent 2290]</span><span class="sxs-lookup"><span data-stu-id="96e30-703">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="96e30-704">Implementar marcas binfmt_misc ' C ' ' O ' y ' P ' [alvent 2103]</span><span class="sxs-lookup"><span data-stu-id="96e30-704">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="96e30-705">Add/proc/sys/kernel/SHMMAX/shmmni &/threads-Max [alvent 1753]</span><span class="sxs-lookup"><span data-stu-id="96e30-705">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="96e30-706">Agregar compatibilidad parcial para llamada del sistema ioprio_set [alvent 498]</span><span class="sxs-lookup"><span data-stu-id="96e30-706">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="96e30-707">Stub SO_REUSEPORT & agregar compatibilidad para SO_PASSCRED para Sockets de NetLink [alvent 69]</span><span class="sxs-lookup"><span data-stu-id="96e30-707">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="96e30-708">Devolver distintos códigos de error de RegisterDistribuiton si se está instalando o desinstalando actualmente una distribución.</span><span class="sxs-lookup"><span data-stu-id="96e30-708">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="96e30-709">Permitir la anulación del registro de distribuciones de WSL parcialmente instaladas a través de wslconfig. exe</span><span class="sxs-lookup"><span data-stu-id="96e30-709">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="96e30-710">Corrección de bloqueo de prueba de socket de Python de UDP:: msg_peek</span><span class="sxs-lookup"><span data-stu-id="96e30-710">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="96e30-711">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-711">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="96e30-712">Console</span><span class="sxs-lookup"><span data-stu-id="96e30-712">Console</span></span>
- <span data-ttu-id="96e30-713">No hay cambios relacionados con la consola en esta versión.</span><span class="sxs-lookup"><span data-stu-id="96e30-713">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-714">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-714">LTP Results:</span></span>
<span data-ttu-id="96e30-715">Total de pruebas: 1904</span><span class="sxs-lookup"><span data-stu-id="96e30-715">Total Tests: 1904</span></span><br/>
<span data-ttu-id="96e30-716">Total de pruebas omitidas: 209</span><span class="sxs-lookup"><span data-stu-id="96e30-716">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="96e30-717">Total de errores: 229</span><span class="sxs-lookup"><span data-stu-id="96e30-717">Total Failures: 229</span></span><br/>
[<span data-ttu-id="96e30-718">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="96e30-718">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="96e30-719">Compilación 16257</span><span class="sxs-lookup"><span data-stu-id="96e30-719">Build 16257</span></span>

<span data-ttu-id="96e30-720">Para obtener información general sobre Windows sobre la compilación 16257, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span><span class="sxs-lookup"><span data-stu-id="96e30-720">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-721">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-721">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="96e30-722">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-722">WSL</span></span>
- <span data-ttu-id="96e30-723">Implementar llamada del sistema prlimit64</span><span class="sxs-lookup"><span data-stu-id="96e30-723">Implement prlimit64 system call</span></span>
- <span data-ttu-id="96e30-724">Incorporación de compatibilidad con ulimit-n (setrlimit RLIMIT_NOFILE) [alvent 1688]</span><span class="sxs-lookup"><span data-stu-id="96e30-724">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="96e30-725">MSG_MORE de código auxiliar para Sockets TCP [alvent 2351]</span><span class="sxs-lookup"><span data-stu-id="96e30-725">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="96e30-726">Corregir el comportamiento del vector auxiliar de AT_EXECFN no válido [alvent 2133]</span><span class="sxs-lookup"><span data-stu-id="96e30-726">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="96e30-727">Corregir el comportamiento de copiar y pegar para consola/TTY y agregar un mejor control de búfer completo [alvent 2204, 2131]</span><span class="sxs-lookup"><span data-stu-id="96e30-727">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="96e30-728">Establecer AT_SECURE en Vector auxiliar para los programas set-User-ID y set-Group-ID [alvent 2031]</span><span class="sxs-lookup"><span data-stu-id="96e30-728">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="96e30-729">Psuedo: el extremo maestro de terminal no controla TIOCPGRP [alvent 1063]</span><span class="sxs-lookup"><span data-stu-id="96e30-729">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="96e30-730">Corrección de lseek hace para rebobinar directorios en LxFs [alvent 2310]</span><span class="sxs-lookup"><span data-stu-id="96e30-730">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="96e30-731">/dev/ptmx se bloquea después del uso intensivo [alvent 1882]</span><span class="sxs-lookup"><span data-stu-id="96e30-731">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="96e30-732">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-732">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="96e30-733">Console</span><span class="sxs-lookup"><span data-stu-id="96e30-733">Console</span></span>
- <span data-ttu-id="96e30-734">Corrección para líneas horizontales o guiones bajos en todas partes [alvent 2168]</span><span class="sxs-lookup"><span data-stu-id="96e30-734">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="96e30-735">Corrección para el orden de procesamiento cambiado haciendo que NPM sea más difícil de cerrar [alvent 2170]</span><span class="sxs-lookup"><span data-stu-id="96e30-735">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="96e30-736">Se ha agregado la nueva combinación de colores: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="96e30-736">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-737">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-737">LTP Results:</span></span>
<span data-ttu-id="96e30-738">Sin cambios desde 16251</span><span class="sxs-lookup"><span data-stu-id="96e30-738">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="96e30-739">Compatibilidad con syscall</span><span class="sxs-lookup"><span data-stu-id="96e30-739">Syscall Support</span></span>
<span data-ttu-id="96e30-740">A continuación se muestra una lista de llamadas syscall nuevos o mejorados que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="96e30-740">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="96e30-741">Los llamadas syscall de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="96e30-741">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="96e30-742">Problemas conocidos</span><span class="sxs-lookup"><span data-stu-id="96e30-742">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[<span data-ttu-id="96e30-743">Problema de GitHub 2392: Carpetas de Windows no reconocidas por WSL...</span><span class="sxs-lookup"><span data-stu-id="96e30-743">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="96e30-744">En la compilación 16257, WSL tiene problemas al enumerar archivos o carpetas de `/mnt/c/...`Windows a través de.</span><span class="sxs-lookup"><span data-stu-id="96e30-744">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="96e30-745">Este problema se ha corregido y debe publicarse en la compilación Insider durante la semana que comienza a las 8/14/2017.</span><span class="sxs-lookup"><span data-stu-id="96e30-745">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="96e30-746">Compilación 16251</span><span class="sxs-lookup"><span data-stu-id="96e30-746">Build 16251</span></span>

<span data-ttu-id="96e30-747">Para obtener información general sobre Windows sobre la compilación 16251, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span><span class="sxs-lookup"><span data-stu-id="96e30-747">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-748">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-748">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="96e30-749">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-749">WSL</span></span>
- <span data-ttu-id="96e30-750">Quitar la etiqueta beta del componente opcional WSL, consulte la [entrada de blog](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="96e30-750">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="96e30-751">Inicialice correctamente el UID y el GID del conjunto guardado para los archivos Set-User-ID y set-Group-ID en exec [alvent 962, 1415, 2072]</span><span class="sxs-lookup"><span data-stu-id="96e30-751">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="96e30-752">Se agregó compatibilidad con ptrace PTRACE_O_TRACEEXIT [alvent 555]</span><span class="sxs-lookup"><span data-stu-id="96e30-752">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="96e30-753">Se ha agregado compatibilidad con ptrace PTRACE_GETFPREGS y PTRACE_GETREGSET con NT_FPREGSET [alvent 555]</span><span class="sxs-lookup"><span data-stu-id="96e30-753">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="96e30-754">Se corrigió ptrace para que se detenga en las señales omitidas</span><span class="sxs-lookup"><span data-stu-id="96e30-754">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="96e30-755">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-755">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="96e30-756">Console</span><span class="sxs-lookup"><span data-stu-id="96e30-756">Console</span></span>
- <span data-ttu-id="96e30-757">No hay cambios relacionados con la consola en esta versión.</span><span class="sxs-lookup"><span data-stu-id="96e30-757">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-758">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-758">LTP Results:</span></span>
<span data-ttu-id="96e30-759">Número de pruebas superadas: 768</span><span class="sxs-lookup"><span data-stu-id="96e30-759">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="96e30-760">Número de pruebas con errores: 244</span><span class="sxs-lookup"><span data-stu-id="96e30-760">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="96e30-761">Número de pruebas omitidas: 96</span><span class="sxs-lookup"><span data-stu-id="96e30-761">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="96e30-762">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="96e30-762">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="96e30-763">Compilación 16241</span><span class="sxs-lookup"><span data-stu-id="96e30-763">Build 16241</span></span>

<span data-ttu-id="96e30-764">Para obtener información general sobre Windows sobre la compilación 16241, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span><span class="sxs-lookup"><span data-stu-id="96e30-764">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-765">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-765">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="96e30-766">WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-766">WSL</span></span>
- <span data-ttu-id="96e30-767">No hay ningún cambio relacionado con WSL en esta versión.</span><span class="sxs-lookup"><span data-stu-id="96e30-767">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="96e30-768">Console</span><span class="sxs-lookup"><span data-stu-id="96e30-768">Console</span></span>
- <span data-ttu-id="96e30-769">Corrección para la generación de un carácter equivocado para las líneas de paso DEC, que se inscribió originalmente [aquí](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span><span class="sxs-lookup"><span data-stu-id="96e30-769">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="96e30-770">Corrección para que no se muestre texto de salida en la página de códigos 65001 (UTF8)</span><span class="sxs-lookup"><span data-stu-id="96e30-770">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="96e30-771">No transfiera los cambios realizados en los valores RGB de un color a otras partes de la paleta en el cambio de selección.</span><span class="sxs-lookup"><span data-stu-id="96e30-771">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="96e30-772">Esto hará que la hoja de propiedades de la consola sea mucho más fácil de usar.</span><span class="sxs-lookup"><span data-stu-id="96e30-772">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="96e30-773">No parece que Ctrl + S funcione correctamente</span><span class="sxs-lookup"><span data-stu-id="96e30-773">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="96e30-774">No mostrar en negrita/-atenuar completamente desde códigos de escape ANSI [alvent 2174]</span><span class="sxs-lookup"><span data-stu-id="96e30-774">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="96e30-775">La consola no admite correctamente los temas de color VIM [alvent 1706]</span><span class="sxs-lookup"><span data-stu-id="96e30-775">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="96e30-776">No se pueden pegar caracteres determinados [alvent 2149]</span><span class="sxs-lookup"><span data-stu-id="96e30-776">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="96e30-777">El cambio de tamaño de reflujo interactúa de forma extraña con el cambio de tamaño de una ventana de Bash cuando el contenido está en la línea de comandos/edición [alConEmu 1123]</span><span class="sxs-lookup"><span data-stu-id="96e30-777">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="96e30-778">Ctrl-L deja la pantalla desfasada [alvent 1978]</span><span class="sxs-lookup"><span data-stu-id="96e30-778">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="96e30-779">Error de representación de consola al mostrar VT en HDPI [alvent 1907]</span><span class="sxs-lookup"><span data-stu-id="96e30-779">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="96e30-780">Los caracteres Japansese parecen extraños con el carácter Unicode U + 30FB [alvent 2146]</span><span class="sxs-lookup"><span data-stu-id="96e30-780">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="96e30-781">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-781">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="96e30-782">Compilación 16237</span><span class="sxs-lookup"><span data-stu-id="96e30-782">Build 16237</span></span>

<span data-ttu-id="96e30-783">Para obtener información general sobre Windows sobre la compilación 16237, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span><span class="sxs-lookup"><span data-stu-id="96e30-783">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-784">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-784">Fixed</span></span>
- <span data-ttu-id="96e30-785">Usar atributos predeterminados para archivos sin EAs en lxfs (raíz, raíz, 0000)</span><span class="sxs-lookup"><span data-stu-id="96e30-785">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="96e30-786">Compatibilidad agregada para distribuciones que usan atributos extendidos</span><span class="sxs-lookup"><span data-stu-id="96e30-786">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="96e30-787">Corregir el relleno de las entradas devueltas por getdents y getdents64</span><span class="sxs-lookup"><span data-stu-id="96e30-787">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="96e30-788">Corrección de los permisos comprobación de la llamada del sistema shmctl SHM_STAT [alvent 2068]</span><span class="sxs-lookup"><span data-stu-id="96e30-788">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="96e30-789">Se corrigió el estado inicial incorrecto de epoll para ttys [alvent 2231]</span><span class="sxs-lookup"><span data-stu-id="96e30-789">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="96e30-790">Fix DrvFs readdir no devuelve todas las entradas [alvent 2077]</span><span class="sxs-lookup"><span data-stu-id="96e30-790">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="96e30-791">Corregir LxFs readdir cuando los archivos están desvinculados [alvent 2077]</span><span class="sxs-lookup"><span data-stu-id="96e30-791">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="96e30-792">Permitir que los archivos drvfs no vinculados se vuelvan a abrir a través de procfs</span><span class="sxs-lookup"><span data-stu-id="96e30-792">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="96e30-793">Se ha agregado la invalidación de la clave del registro global para deshabilitar las características de WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-793">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="96e30-794">Corrección del recuento incorrecto de bloques en "stat" para DrvFs (y LxFs) [alvent 1894]</span><span class="sxs-lookup"><span data-stu-id="96e30-794">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="96e30-795">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-795">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="96e30-796">Compilación 16232</span><span class="sxs-lookup"><span data-stu-id="96e30-796">Build 16232</span></span>

<span data-ttu-id="96e30-797">Para obtener información general sobre Windows sobre la compilación 16232, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span><span class="sxs-lookup"><span data-stu-id="96e30-797">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-798">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-798">Fixed</span></span>
- <span data-ttu-id="96e30-799">No hay ningún cambio relacionado con WSL en esta versión.</span><span class="sxs-lookup"><span data-stu-id="96e30-799">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="96e30-800">Compilación 16226</span><span class="sxs-lookup"><span data-stu-id="96e30-800">Build 16226</span></span>

<span data-ttu-id="96e30-801">Para obtener información general sobre Windows sobre la compilación 16226, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span><span class="sxs-lookup"><span data-stu-id="96e30-801">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-802">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-802">Fixed</span></span>
- <span data-ttu-id="96e30-803">xattr relacionado con llamadas syscall (getxattr, setxattr, listxattr, removexattr).</span><span class="sxs-lookup"><span data-stu-id="96e30-803">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="96e30-804">compatibilidad con Security. capablity xattr.</span><span class="sxs-lookup"><span data-stu-id="96e30-804">security.capablity xattr support.</span></span>
- <span data-ttu-id="96e30-805">Compatibilidad mejorada con determinados sistemas de archivos y filtros, incluidos los servidores SMB que no son de MS.</span><span class="sxs-lookup"><span data-stu-id="96e30-805">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="96e30-806">[ALVENT #1952]</span><span class="sxs-lookup"><span data-stu-id="96e30-806">[GH #1952]</span></span>
- <span data-ttu-id="96e30-807">Compatibilidad mejorada para los marcadores de posición de OneDrive, los marcadores de posición de GVFS y los archivos comprimidos del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="96e30-807">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="96e30-808">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-808">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="96e30-809">Compilación 16215</span><span class="sxs-lookup"><span data-stu-id="96e30-809">Build 16215</span></span>

<span data-ttu-id="96e30-810">Para obtener información general sobre Windows sobre la compilación 16215, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span><span class="sxs-lookup"><span data-stu-id="96e30-810">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-811">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-811">Fixed</span></span>
- <span data-ttu-id="96e30-812">WSL ya no requiere el modo de desarrollador.</span><span class="sxs-lookup"><span data-stu-id="96e30-812">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="96e30-813">Compatibilidad con uniones de directorios en drvfs.</span><span class="sxs-lookup"><span data-stu-id="96e30-813">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="96e30-814">Controla la desinstalación de paquetes appx de distribución de WSL.</span><span class="sxs-lookup"><span data-stu-id="96e30-814">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="96e30-815">Actualice procfs para mostrar las asignaciones privadas y compartidas.</span><span class="sxs-lookup"><span data-stu-id="96e30-815">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="96e30-816">Agregar la capacidad de wslconfig. exe para limpiar las distribuciones que se instalan o desinstalan parcialmente.</span><span class="sxs-lookup"><span data-stu-id="96e30-816">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="96e30-817">Compatibilidad agregada para IP_MTU_DISCOVER para Sockets TCP.</span><span class="sxs-lookup"><span data-stu-id="96e30-817">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="96e30-818">[ALVENT 1639, 2115, 2205]</span><span class="sxs-lookup"><span data-stu-id="96e30-818">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="96e30-819">Inferencia de la familia de protocolos para rutas a AF_INADDR.</span><span class="sxs-lookup"><span data-stu-id="96e30-819">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="96e30-820">Mejoras en los dispositivos serie [alvent 1929].</span><span class="sxs-lookup"><span data-stu-id="96e30-820">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="96e30-821">Compilación 16199</span><span class="sxs-lookup"><span data-stu-id="96e30-821">Build 16199</span></span>

<span data-ttu-id="96e30-822">Para obtener información general sobre Windows sobre la compilación 16199, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span><span class="sxs-lookup"><span data-stu-id="96e30-822">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-823">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-823">Fixed</span></span>
- <span data-ttu-id="96e30-824">No hay ningún cambio relacionado con WSL en estas versiones.</span><span class="sxs-lookup"><span data-stu-id="96e30-824">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="96e30-825">Compilación 16193</span><span class="sxs-lookup"><span data-stu-id="96e30-825">Build 16193</span></span>

<span data-ttu-id="96e30-826">Para obtener información general sobre Windows sobre la compilación 16193, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span><span class="sxs-lookup"><span data-stu-id="96e30-826">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-827">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-827">Fixed</span></span>
- <span data-ttu-id="96e30-828">Condición de carrera entre el envío de SIGCONT y un elemento threadgroup de terminación [alvent 1973]</span><span class="sxs-lookup"><span data-stu-id="96e30-828">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="96e30-829">cambiar los dispositivos TTY y PTY a Report FILE_DEVICE_NAMED_PIPE en lugar de FILE_DEVICE_CONSOLE [alvent 1840]</span><span class="sxs-lookup"><span data-stu-id="96e30-829">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="96e30-830">Corrección de SSH para IP_OPTIONS</span><span class="sxs-lookup"><span data-stu-id="96e30-830">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="96e30-831">Se ha cambiado el montaje de DrvFs al demonio de inicialización [alvent 1862, 1968, 1767, 1933]</span><span class="sxs-lookup"><span data-stu-id="96e30-831">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="96e30-832">Se agregó compatibilidad en DrvFs para los siguientes vínculos simbólicos de NT.</span><span class="sxs-lookup"><span data-stu-id="96e30-832">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="96e30-833">Compilación 16184</span><span class="sxs-lookup"><span data-stu-id="96e30-833">Build 16184</span></span>

<span data-ttu-id="96e30-834">Para obtener información general sobre Windows sobre la compilación 16184, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span><span class="sxs-lookup"><span data-stu-id="96e30-834">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-835">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-835">Fixed</span></span>
- <span data-ttu-id="96e30-836">Tarea de mantenimiento de paquetes APT quitada (lxrun. exe/Update)</span><span class="sxs-lookup"><span data-stu-id="96e30-836">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="96e30-837">Salida corregida que no se muestra en los procesos de Windows en node. js [alvent 1840]</span><span class="sxs-lookup"><span data-stu-id="96e30-837">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="96e30-838">Relajar los requisitos de alineación en lxcore [alvent 1794]</span><span class="sxs-lookup"><span data-stu-id="96e30-838">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="96e30-839">Control corregido de la marca AT_EMPTY_PATH en un número de llamadas del sistema.</span><span class="sxs-lookup"><span data-stu-id="96e30-839">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="96e30-840">Problema corregido en el que la eliminación de archivos DrvFs con identificadores abiertos hará que el archivo muestre un comportamiento indefinido [alvent 544, 966, 1357, 1535, 1615]</span><span class="sxs-lookup"><span data-stu-id="96e30-840">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="96e30-841">/etc/hosts heredará ahora entradas del archivo de hosts de Windows (%windir%\system32\drivers\etc\hosts) [alvent 1495]</span><span class="sxs-lookup"><span data-stu-id="96e30-841">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="96e30-842">Compilación 16179</span><span class="sxs-lookup"><span data-stu-id="96e30-842">Build 16179</span></span>

<span data-ttu-id="96e30-843">Para obtener información general sobre Windows sobre la compilación 16179, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span><span class="sxs-lookup"><span data-stu-id="96e30-843">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-844">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-844">Fixed</span></span>
- <span data-ttu-id="96e30-845">No WSL cambia esta semana.</span><span class="sxs-lookup"><span data-stu-id="96e30-845">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="96e30-846">Compilación 16176</span><span class="sxs-lookup"><span data-stu-id="96e30-846">Build 16176</span></span>

<span data-ttu-id="96e30-847">Para obtener información general sobre Windows sobre la compilación 16176, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span><span class="sxs-lookup"><span data-stu-id="96e30-847">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-848">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-848">Fixed</span></span>

- [<span data-ttu-id="96e30-849">Compatibilidad con serialización habilitada</span><span class="sxs-lookup"><span data-stu-id="96e30-849">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="96e30-850">Opción de socket de IP agregada IP_OPTIONS [alvent 1116]</span><span class="sxs-lookup"><span data-stu-id="96e30-850">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="96e30-851">Función pwritev implementada (al cargar el archivo en nginx/PHP-FPM) [alvent 1506]</span><span class="sxs-lookup"><span data-stu-id="96e30-851">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="96e30-852">Se han agregado opciones de socket IP IP_MULTICAST_IF & IPV6_MULTICAST_IF [alvent 990]</span><span class="sxs-lookup"><span data-stu-id="96e30-852">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="96e30-853">Compatibilidad con la opción de socket IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [alvent 1678]</span><span class="sxs-lookup"><span data-stu-id="96e30-853">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="96e30-854">Se ha agregado la opción de socket _MTU de IP (V6) para el nodo de aplicaciones, traceroute, Dig, nslookup, host</span><span class="sxs-lookup"><span data-stu-id="96e30-854">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="96e30-855">Opción de socket de IP agregada IPV6_UNICAST_HOPS</span><span class="sxs-lookup"><span data-stu-id="96e30-855">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="96e30-856">Mejoras del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="96e30-856">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="96e30-857">Permitir el montaje de rutas UNC</span><span class="sxs-lookup"><span data-stu-id="96e30-857">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="96e30-858">Habilitar la compatibilidad con CDFS en drvfs</span><span class="sxs-lookup"><span data-stu-id="96e30-858">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="96e30-859">Administrar correctamente los permisos para los sistemas de archivos de red en drvfs</span><span class="sxs-lookup"><span data-stu-id="96e30-859">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="96e30-860">Agregar compatibilidad para unidades remotas a drvfs</span><span class="sxs-lookup"><span data-stu-id="96e30-860">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="96e30-861">Habilitar la compatibilidad con FAT en drvfs</span><span class="sxs-lookup"><span data-stu-id="96e30-861">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="96e30-862">Correcciones y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-862">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-863">Resultados de LTP</span><span class="sxs-lookup"><span data-stu-id="96e30-863">LTP Results</span></span>
<span data-ttu-id="96e30-864">No hay cambios desde 15042</span><span class="sxs-lookup"><span data-stu-id="96e30-864">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="96e30-865">Compilación 16170</span><span class="sxs-lookup"><span data-stu-id="96e30-865">Build 16170</span></span>

<span data-ttu-id="96e30-866">Para obtener información general sobre Windows sobre la compilación 16170, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span><span class="sxs-lookup"><span data-stu-id="96e30-866">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="96e30-867">Hemos publicado una nueva [entrada de blog](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) en la que se describen nuestros esfuerzos para probar WSL.</span><span class="sxs-lookup"><span data-stu-id="96e30-867">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="96e30-868">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-868">Fixed</span></span>

- <span data-ttu-id="96e30-869">Support socket Option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [alvent 1678]</span><span class="sxs-lookup"><span data-stu-id="96e30-869">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="96e30-870">Agregar compatibilidad para PTRACE_OLDSETOPTIONS.</span><span class="sxs-lookup"><span data-stu-id="96e30-870">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="96e30-871">[ALVENT 1692]</span><span class="sxs-lookup"><span data-stu-id="96e30-871">[GH 1692]</span></span>
- <span data-ttu-id="96e30-872">Correcciones y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-872">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-873">Resultados de LTP</span><span class="sxs-lookup"><span data-stu-id="96e30-873">LTP Results</span></span>
<span data-ttu-id="96e30-874">No hay cambios desde 15042</span><span class="sxs-lookup"><span data-stu-id="96e30-874">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="96e30-875">Compilación 15046 a Windows 10 Creators Update</span><span class="sxs-lookup"><span data-stu-id="96e30-875">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="96e30-876">No hay más correcciones de WSL o características planeadas para su inclusión en la actualización de Creators en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="96e30-876">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="96e30-877">Las notas de la versión de WSL se reanudarán en las próximas semanas para las adiciones destinadas al siguiente Windows Update principal.</span><span class="sxs-lookup"><span data-stu-id="96e30-877">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="96e30-878">Para obtener información general sobre Windows sobre la compilación 15046 y futuras versiones de Insider, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span><span class="sxs-lookup"><span data-stu-id="96e30-878">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="96e30-879">Compilación 15042</span><span class="sxs-lookup"><span data-stu-id="96e30-879">Build 15042</span></span>

<span data-ttu-id="96e30-880">Para obtener información general sobre Windows sobre la compilación 15042, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span><span class="sxs-lookup"><span data-stu-id="96e30-880">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-881">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-881">Fixed</span></span>

- <span data-ttu-id="96e30-882">Corrección para un interbloqueo al quitar una ruta de acceso que termina en ".."</span><span class="sxs-lookup"><span data-stu-id="96e30-882">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="96e30-883">Se corrigió un problema por el que FIONBIO no devuelve 0 en caso de éxito [alvent 1683]</span><span class="sxs-lookup"><span data-stu-id="96e30-883">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="96e30-884">Problema corregido con lecturas de longitud cero de sockets de datagramas de inet</span><span class="sxs-lookup"><span data-stu-id="96e30-884">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="96e30-885">Corrección del posible interbloqueo debido a la condición de carrera en la búsqueda de inode de drvfs [alvent 1675]</span><span class="sxs-lookup"><span data-stu-id="96e30-885">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="96e30-886">Compatibilidad ampliada con los datos suplementarios de los sockets de UNIX; SCM_CREDENTIALS y SCM_RIGHTS [alvent 514, 613, 1326]</span><span class="sxs-lookup"><span data-stu-id="96e30-886">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="96e30-887">Correcciones y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-887">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-888">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-888">LTP Results:</span></span>
<span data-ttu-id="96e30-889">Número de pruebas superadas: 737</span><span class="sxs-lookup"><span data-stu-id="96e30-889">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="96e30-890">Número de pasos no superados (error, omitido, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="96e30-890">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="96e30-891">Compilación 15031</span><span class="sxs-lookup"><span data-stu-id="96e30-891">Build 15031</span></span>

<span data-ttu-id="96e30-892">Para obtener información general sobre Windows sobre la compilación 15031, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span><span class="sxs-lookup"><span data-stu-id="96e30-892">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-893">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-893">Fixed</span></span>

- <span data-ttu-id="96e30-894">Se corrigió un error en el que el tiempo (2) se comportó de manera esporádica.</span><span class="sxs-lookup"><span data-stu-id="96e30-894">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="96e30-895">Problema corregido, donde \* SIGPROCMASK llamadas syscall podría dañar la máscara de señal.</span><span class="sxs-lookup"><span data-stu-id="96e30-895">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="96e30-896">Ahora, devuelva la longitud completa de la línea de comandos en la notificación de creación del proceso WSL.</span><span class="sxs-lookup"><span data-stu-id="96e30-896">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="96e30-897">[ALVENT 1632]</span><span class="sxs-lookup"><span data-stu-id="96e30-897">[GH 1632]</span></span>
- <span data-ttu-id="96e30-898">WSL Now informa de la salida del subproceso a través de ptrace para que GDB se bloquee.</span><span class="sxs-lookup"><span data-stu-id="96e30-898">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="96e30-899">[ALVENT 1196]</span><span class="sxs-lookup"><span data-stu-id="96e30-899">[GH 1196]</span></span>
- <span data-ttu-id="96e30-900">Se corrigió un error en el que ptys se bloquease después de una gran tmux de e/s</span><span class="sxs-lookup"><span data-stu-id="96e30-900">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="96e30-901">[ALVENT 1358]</span><span class="sxs-lookup"><span data-stu-id="96e30-901">[GH 1358]</span></span>
- <span data-ttu-id="96e30-902">Se ha corregido la validación del tiempo de espera en muchas llamadas del sistema (Futex, SEMTIMEDOP, ppoll, sigtimedwait, itimer, timer_create)</span><span class="sxs-lookup"><span data-stu-id="96e30-902">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="96e30-903">Compatibilidad con eventfd EFD_SEMAPHORE agregada [alvent 452]</span><span class="sxs-lookup"><span data-stu-id="96e30-903">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="96e30-904">Correcciones y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-904">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-905">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-905">LTP Results:</span></span>
<span data-ttu-id="96e30-906">Número de pruebas superadas: 737</span><span class="sxs-lookup"><span data-stu-id="96e30-906">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="96e30-907">Número de pasos no superados (error, omitido, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="96e30-907">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="96e30-908">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="96e30-908">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="96e30-909">Compilación 15025</span><span class="sxs-lookup"><span data-stu-id="96e30-909">Build 15025</span></span>

<span data-ttu-id="96e30-910">Para obtener información general sobre Windows sobre la compilación 15025, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span><span class="sxs-lookup"><span data-stu-id="96e30-910">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-911">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-911">Fixed</span></span>

- <span data-ttu-id="96e30-912">Corrección del error que dañó grep 2,27 [alvent 1578]</span><span class="sxs-lookup"><span data-stu-id="96e30-912">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="96e30-913">Marca EFD_SEMAPHORE implementada para eventfd2 syscall [alvent 452]</span><span class="sxs-lookup"><span data-stu-id="96e30-913">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="96e30-914">Implementado/proc/[PID]/net/ipv6_route [alvent 1608]</span><span class="sxs-lookup"><span data-stu-id="96e30-914">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="96e30-915">Compatibilidad de e/s controlada por señal para Sockets de secuencia de UNIX [alvent 393, 68]</span><span class="sxs-lookup"><span data-stu-id="96e30-915">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="96e30-916">Compatibilidad con F_GETPIPE_SZ y F_SETPIPE_SZ [alvent 1012]</span><span class="sxs-lookup"><span data-stu-id="96e30-916">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="96e30-917">Implementar recvmmsg () syscall [alvent 1531]</span><span class="sxs-lookup"><span data-stu-id="96e30-917">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="96e30-918">Se corrigió un error en el que epoll_wait () no esperaba [alvent 1609]</span><span class="sxs-lookup"><span data-stu-id="96e30-918">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="96e30-919">Implementación de/proc/version_signature</span><span class="sxs-lookup"><span data-stu-id="96e30-919">Implement /proc/version_signature</span></span>
- <span data-ttu-id="96e30-920">Tee syscall ahora devuelve un error si ambos descriptores de archivo hacen referencia a la misma canalización</span><span class="sxs-lookup"><span data-stu-id="96e30-920">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="96e30-921">Se implementó el comportamiento correcto de SO_PEERCRED para Sockets de UNIX</span><span class="sxs-lookup"><span data-stu-id="96e30-921">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="96e30-922">Control de parámetros no válidos de tkill de syscall corregidos</span><span class="sxs-lookup"><span data-stu-id="96e30-922">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="96e30-923">Cambios para aumentar el Preformace de drvfs</span><span class="sxs-lookup"><span data-stu-id="96e30-923">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="96e30-924">Corrección secundaria para el bloqueo de e/s de Ruby</span><span class="sxs-lookup"><span data-stu-id="96e30-924">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="96e30-925">Fixed recvmsg () que devuelve EINVAL para la marca MSG_DONTWAIT para Sockets inet [alvent 1296]</span><span class="sxs-lookup"><span data-stu-id="96e30-925">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="96e30-926">Correcciones y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-926">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-927">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-927">LTP Results:</span></span>
<span data-ttu-id="96e30-928">Número de pruebas superadas: 732</span><span class="sxs-lookup"><span data-stu-id="96e30-928">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="96e30-929">Número de pasos no superados (error, omitido, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="96e30-929">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="96e30-930">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="96e30-930">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="96e30-931">Compilación 15019</span><span class="sxs-lookup"><span data-stu-id="96e30-931">Build 15019</span></span>

<span data-ttu-id="96e30-932">Para obtener información general sobre Windows sobre la compilación 15019, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span><span class="sxs-lookup"><span data-stu-id="96e30-932">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-933">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-933">Fixed</span></span>

- <span data-ttu-id="96e30-934">Se corrigió un error que informaba incorrectamente del uso de CPU en procfs para herramientas como htop (alvent 823, 945, 971)</span><span class="sxs-lookup"><span data-stu-id="96e30-934">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="96e30-935">Al llamar a Open () con O_TRUNC en un archivo existente inotify ahora genera IN_MODIFY antes de IN_OPEN</span><span class="sxs-lookup"><span data-stu-id="96e30-935">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="96e30-936">Correcciones para el SO_ERROR de sockets de UNIX getsockopt para habilitar Postgress [alvent 61, 1354]</span><span class="sxs-lookup"><span data-stu-id="96e30-936">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="96e30-937">Implementación de/proc/sys/net/Core/somaxconn para el lenguaje GO</span><span class="sxs-lookup"><span data-stu-id="96e30-937">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="96e30-938">Apt: la tarea en segundo plano actualizar paquete se ejecuta ahora oculta desde la vista</span><span class="sxs-lookup"><span data-stu-id="96e30-938">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="96e30-939">Borrar el ámbito de IPv6 localhost (error de la plataforma de Spring Framework (Java)).</span><span class="sxs-lookup"><span data-stu-id="96e30-939">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="96e30-940">Correcciones y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-940">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-941">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-941">LTP Results:</span></span>
<span data-ttu-id="96e30-942">Número de pruebas superadas: 714</span><span class="sxs-lookup"><span data-stu-id="96e30-942">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="96e30-943">Número de pasos no superados (error, omitido, etc.): 249</span><span class="sxs-lookup"><span data-stu-id="96e30-943">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="96e30-944">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="96e30-944">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="96e30-945">Compilación 15014</span><span class="sxs-lookup"><span data-stu-id="96e30-945">Build 15014</span></span>

<span data-ttu-id="96e30-946">Para obtener información general sobre Windows sobre la compilación 15014, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="96e30-946">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-947">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-947">Fixed</span></span>

- <span data-ttu-id="96e30-948">Ctrl + C ahora funciona según lo previsto</span><span class="sxs-lookup"><span data-stu-id="96e30-948">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="96e30-949">htop y PS auxw ahora muestran el uso de recursos correcto (alvent #516)</span><span class="sxs-lookup"><span data-stu-id="96e30-949">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="96e30-950">Traducción básica de las excepciones de NT a las señales.</span><span class="sxs-lookup"><span data-stu-id="96e30-950">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="96e30-951">(ALVENT #513)</span><span class="sxs-lookup"><span data-stu-id="96e30-951">(GH #513)</span></span>
- <span data-ttu-id="96e30-952">fallocate Now genera ENOSPC cuando se está quedando sin espacio en lugar de EINVAL (alvent #1571)</span><span class="sxs-lookup"><span data-stu-id="96e30-952">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="96e30-953">Agregado/proc/sys/kernel/SEM.</span><span class="sxs-lookup"><span data-stu-id="96e30-953">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="96e30-954">Llamadas del sistema semop y semtimedop implementadas</span><span class="sxs-lookup"><span data-stu-id="96e30-954">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="96e30-955">Se corrigieron errores de nslookup con la opción de socket IP_RECVTOS & IPV6_RECVTCLASS (alvent 69)</span><span class="sxs-lookup"><span data-stu-id="96e30-955">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="96e30-956">Compatibilidad con las opciones de socket IP_RECVTTL y IPV6_RECVHOPLIMIT</span><span class="sxs-lookup"><span data-stu-id="96e30-956">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="96e30-957">Correcciones y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-957">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-958">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-958">LTP Results:</span></span>
<span data-ttu-id="96e30-959">Número de pruebas superadas: 709</span><span class="sxs-lookup"><span data-stu-id="96e30-959">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="96e30-960">Número de pasos no superados (error, omitido, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="96e30-960">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="96e30-961">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="96e30-961">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="96e30-962">Resumen de syscall</span><span class="sxs-lookup"><span data-stu-id="96e30-962">Syscall Summary</span></span>
<span data-ttu-id="96e30-963">Llamadas syscall total: 384</span><span class="sxs-lookup"><span data-stu-id="96e30-963">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="96e30-964">Total implementado: 235</span><span class="sxs-lookup"><span data-stu-id="96e30-964">Total Implemented: 235</span></span> </br>
<span data-ttu-id="96e30-965">Total de stubs: 22</span><span class="sxs-lookup"><span data-stu-id="96e30-965">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="96e30-966">Total no implementado: 127</span><span class="sxs-lookup"><span data-stu-id="96e30-966">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="96e30-967">Desglose detallado</span><span class="sxs-lookup"><span data-stu-id="96e30-967">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="96e30-968">Compilación 15007</span><span class="sxs-lookup"><span data-stu-id="96e30-968">Build 15007</span></span>

<span data-ttu-id="96e30-969">Para obtener información general sobre Windows sobre la compilación 15007, visite el [blog de Windows]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span><span class="sxs-lookup"><span data-stu-id="96e30-969">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="96e30-970">Problema conocido</span><span class="sxs-lookup"><span data-stu-id="96e30-970">Known Issue</span></span>

- <span data-ttu-id="96e30-971">Hay un error conocido en el que la consola no reconoce algunas teclas Ctrl <key> + Input.</span><span class="sxs-lookup"><span data-stu-id="96e30-971">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="96e30-972">Esto incluye el comando Ctrl-c, que actuará como una KeyPress normal "c".</span><span class="sxs-lookup"><span data-stu-id="96e30-972">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="96e30-973">Solución: Asigne una tecla alternativa a Ctrl + C.</span><span class="sxs-lookup"><span data-stu-id="96e30-973">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="96e30-974">Por ejemplo, para asignar CTRL + K a Ctrl + C, haga `stty intr \^k`lo siguiente:.</span><span class="sxs-lookup"><span data-stu-id="96e30-974">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="96e30-975">Esta asignación es por terminal y tendrá que realizarse *cada* vez que se inicie bash.</span><span class="sxs-lookup"><span data-stu-id="96e30-975">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="96e30-976">Los usuarios pueden explorar la opción para incluirlo en su`.bashrc`</span><span class="sxs-lookup"><span data-stu-id="96e30-976">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="96e30-977">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-977">Fixed</span></span>

- <span data-ttu-id="96e30-978">Se corrigió el problema que hacía que la ejecución de WSL consumiera 100% de un núcleo de CPU.</span><span class="sxs-lookup"><span data-stu-id="96e30-978">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="96e30-979">Ahora se admite la opción de socket IP_PKTINFO, IPV6_RECVPKTINFO.</span><span class="sxs-lookup"><span data-stu-id="96e30-979">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="96e30-980">(ALVENT #851, 987)</span><span class="sxs-lookup"><span data-stu-id="96e30-980">(GH #851, 987)</span></span>
- <span data-ttu-id="96e30-981">Truncar dirección física de la interfaz de red a 16 bytes en lxcore (alvent #1452, 1414, 1343, 468, 308)</span><span class="sxs-lookup"><span data-stu-id="96e30-981">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="96e30-982">Correcciones y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-982">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-983">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-983">LTP Results:</span></span>
<span data-ttu-id="96e30-984">Número de pruebas superadas: 709</span><span class="sxs-lookup"><span data-stu-id="96e30-984">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="96e30-985">Número de pasos no superados (error, omitido, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="96e30-985">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="96e30-986">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="96e30-986">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="96e30-987">Compilación 15002</span><span class="sxs-lookup"><span data-stu-id="96e30-987">Build 15002</span></span>

<span data-ttu-id="96e30-988">Para obtener información general sobre Windows sobre la compilación 15002, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span><span class="sxs-lookup"><span data-stu-id="96e30-988">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="96e30-989">Problema conocido</span><span class="sxs-lookup"><span data-stu-id="96e30-989">Known Issue</span></span>

<span data-ttu-id="96e30-990">Dos problemas conocidos:</span><span class="sxs-lookup"><span data-stu-id="96e30-990">Two known issues:</span></span>
- <span data-ttu-id="96e30-991">Hay un error conocido en el que la consola no reconoce algunas teclas Ctrl <key> + Input.</span><span class="sxs-lookup"><span data-stu-id="96e30-991">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="96e30-992">Esto incluye el comando Ctrl-c, que actuará como una KeyPress normal "c".</span><span class="sxs-lookup"><span data-stu-id="96e30-992">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="96e30-993">Solución: Asigne una tecla alternativa a Ctrl + C.</span><span class="sxs-lookup"><span data-stu-id="96e30-993">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="96e30-994">Por ejemplo, para asignar CTRL + K a Ctrl + C, haga `stty intr \^k`lo siguiente:.</span><span class="sxs-lookup"><span data-stu-id="96e30-994">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="96e30-995">Esta asignación es por terminal y tendrá que realizarse *cada* vez que se inicie bash.</span><span class="sxs-lookup"><span data-stu-id="96e30-995">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="96e30-996">Los usuarios pueden explorar la opción para incluirlo en su`.bashrc`</span><span class="sxs-lookup"><span data-stu-id="96e30-996">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="96e30-997">Mientras se ejecuta WSL, un subproceso del sistema consumirá el 100% de un núcleo de CPU.</span><span class="sxs-lookup"><span data-stu-id="96e30-997">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="96e30-998">La causa raíz se ha solucionado y corregido internamente.</span><span class="sxs-lookup"><span data-stu-id="96e30-998">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="96e30-999">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-999">Fixed</span></span>

- <span data-ttu-id="96e30-1000">Todas las sesiones de Bash deben crearse ahora en el mismo nivel de permiso.</span><span class="sxs-lookup"><span data-stu-id="96e30-1000">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="96e30-1001">Se bloqueará el intento de iniciar una sesión en un nivel diferente.</span><span class="sxs-lookup"><span data-stu-id="96e30-1001">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="96e30-1002">Esto significa que las consolas de administrador y que no son de administración no se pueden ejecutar al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="96e30-1002">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="96e30-1003">(ALVENT #626)</span><span class="sxs-lookup"><span data-stu-id="96e30-1003">(GH #626)</span></span>
<br/>
- <span data-ttu-id="96e30-1004">Se implementaron los siguientes mensajes NETLINK_ROUTE (requiere el administrador de Windows)</span><span class="sxs-lookup"><span data-stu-id="96e30-1004">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="96e30-1005">RTM_NEWADDR (admite `ip addr add`)</span><span class="sxs-lookup"><span data-stu-id="96e30-1005">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="96e30-1006">RTM_NEWROUTE (admite `ip route add`)</span><span class="sxs-lookup"><span data-stu-id="96e30-1006">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="96e30-1007">RTM_DELADDR (admite `ip addr del`)</span><span class="sxs-lookup"><span data-stu-id="96e30-1007">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="96e30-1008">RTM_DELROUTE (admite `ip route del`)</span><span class="sxs-lookup"><span data-stu-id="96e30-1008">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="96e30-1009">La comprobación de tareas programadas para actualizar los paquetes ya no se ejecutará en una conexión de uso medido (alvent #1371)</span><span class="sxs-lookup"><span data-stu-id="96e30-1009">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="96e30-1010">Se corrigió un error en el que la canalización se bloquea, es decir, bash-c "LS-alR/" | Bash-c "gato" (alvent #1214)</span><span class="sxs-lookup"><span data-stu-id="96e30-1010">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="96e30-1011">Opción de socket TCP_KEEPCNT implementada (alvent #843)</span><span class="sxs-lookup"><span data-stu-id="96e30-1011">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="96e30-1012">Opción de socket INET de IP_MTU_DISCOVER implementada (alvent #720, 717, 170, 69)</span><span class="sxs-lookup"><span data-stu-id="96e30-1012">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="96e30-1013">Se ha quitado la funcionalidad heredada para ejecutar archivos binarios de NT desde init con búsqueda de rutas NT.</span><span class="sxs-lookup"><span data-stu-id="96e30-1013">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="96e30-1014">(ALVENT #1325)</span><span class="sxs-lookup"><span data-stu-id="96e30-1014">(GH #1325)</span></span>
- <span data-ttu-id="96e30-1015">Modo de corrección de/dev/KMSG para permitir el acceso de lectura de grupo/otro (0644) (alvent #1321)</span><span class="sxs-lookup"><span data-stu-id="96e30-1015">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="96e30-1016">/Proc/sys/kernel/Random/UUID implementado (alvent #1092)</span><span class="sxs-lookup"><span data-stu-id="96e30-1016">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="96e30-1017">Error corregido en el que la hora de inicio del proceso se mostraba como año 2432 (alvent #974)</span><span class="sxs-lookup"><span data-stu-id="96e30-1017">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="96e30-1018">Variable de entorno de término predeterminado conmutada a xterm-256color (alvent #1446)</span><span class="sxs-lookup"><span data-stu-id="96e30-1018">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="96e30-1019">Se modificó la forma en que se calcula la confirmación del proceso durante la bifurcación del proceso.</span><span class="sxs-lookup"><span data-stu-id="96e30-1019">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="96e30-1020">(ALVENT #1286)</span><span class="sxs-lookup"><span data-stu-id="96e30-1020">(GH #1286)</span></span>
- <span data-ttu-id="96e30-1021">/Proc/sys/VM/overcommit_memory. implementado</span><span class="sxs-lookup"><span data-stu-id="96e30-1021">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="96e30-1022">(ALVENT #1286)</span><span class="sxs-lookup"><span data-stu-id="96e30-1022">(GH #1286)</span></span>
- <span data-ttu-id="96e30-1023">Archivo/proc/net/Route implementado (alvent #69)</span><span class="sxs-lookup"><span data-stu-id="96e30-1023">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="96e30-1024">Error corregido en el que el nombre de acceso directo se ha localizado incorrectamente (alvent #696)</span><span class="sxs-lookup"><span data-stu-id="96e30-1024">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="96e30-1025">La lógica de análisis de Elf corregida que valida incorrectamente los encabezados de programa debe ser menor que (o igual a) PATH_MAX.</span><span class="sxs-lookup"><span data-stu-id="96e30-1025">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="96e30-1026">(ALVENT #1048)</span><span class="sxs-lookup"><span data-stu-id="96e30-1026">(GH #1048)</span></span>
- <span data-ttu-id="96e30-1027">Devolución de llamada de statfs implementada para procfs, sysfs, cgroupfs y binfmtfs (alvent #1378)</span><span class="sxs-lookup"><span data-stu-id="96e30-1027">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="96e30-1028">Se han corregido ventanas de AptPackageIndexUpdate que no se cierran (alvent #1184, también se describe en alvent #1193).</span><span class="sxs-lookup"><span data-stu-id="96e30-1028">Fixed AptPackageIndexUpdate windows that won’t close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="96e30-1029">Se ha agregado compatibilidad con la ADDR_NO_RANDOMIZE de ASLR.</span><span class="sxs-lookup"><span data-stu-id="96e30-1029">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="96e30-1030">(ALVENT #1148, 1128)</span><span class="sxs-lookup"><span data-stu-id="96e30-1030">(GH #1148, 1128)</span></span>
- <span data-ttu-id="96e30-1031">Se ha mejorado PTRACE_GETSIGINFO, SIGSEGV, para los seguimientos de la pila gdb adecuados durante el AV (alvent #875)</span><span class="sxs-lookup"><span data-stu-id="96e30-1031">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="96e30-1032">Ya no se produce un error en el análisis de ELF para los archivos binarios de patchelf.</span><span class="sxs-lookup"><span data-stu-id="96e30-1032">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="96e30-1033">(ALVENT #471)</span><span class="sxs-lookup"><span data-stu-id="96e30-1033">(GH #471)</span></span>
- <span data-ttu-id="96e30-1034">DNS de VPN propagado a/etc/resolv.conf (alvent #416, 1350)</span><span class="sxs-lookup"><span data-stu-id="96e30-1034">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="96e30-1035">Mejoras en el cierre de TCP para la transferencia de datos más confiable.</span><span class="sxs-lookup"><span data-stu-id="96e30-1035">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="96e30-1036">(ALVENT #610, 616, 1025, 1335)</span><span class="sxs-lookup"><span data-stu-id="96e30-1036">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="96e30-1037">Ahora, devuelva el código de error correcto cuando se abran demasiados archivos (EMFILE).</span><span class="sxs-lookup"><span data-stu-id="96e30-1037">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="96e30-1038">(ALVENT #1126, 2090)</span><span class="sxs-lookup"><span data-stu-id="96e30-1038">(GH #1126, 2090)</span></span>
- <span data-ttu-id="96e30-1039">El registro de auditoría de Windows ahora informa del nombre de la imagen en el proceso de creación de auditoría.</span><span class="sxs-lookup"><span data-stu-id="96e30-1039">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="96e30-1040">Ahora se produce un error correctamente al iniciar bash. exe desde una ventana de Bash.</span><span class="sxs-lookup"><span data-stu-id="96e30-1040">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="96e30-1041">Mensaje de error agregado cuando Interop no puede obtener acceso a un directorio de trabajo en LxFs (es decir, Notepad. exe. bashrc)</span><span class="sxs-lookup"><span data-stu-id="96e30-1041">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="96e30-1042">Se corrigió un problema en el que la ruta de acceso de Windows se truncó en WSL</span><span class="sxs-lookup"><span data-stu-id="96e30-1042">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="96e30-1043">Correcciones y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-1043">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-1044">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-1044">LTP Results:</span></span>
<span data-ttu-id="96e30-1045">Número de pruebas superadas: 690</span><span class="sxs-lookup"><span data-stu-id="96e30-1045">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="96e30-1046">Número de pasos no superados (error, omitido, etc.): 274</span><span class="sxs-lookup"><span data-stu-id="96e30-1046">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="96e30-1047">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="96e30-1047">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="96e30-1048">Compatibilidad con syscall</span><span class="sxs-lookup"><span data-stu-id="96e30-1048">Syscall Support</span></span>
<span data-ttu-id="96e30-1049">A continuación se muestra una lista de llamadas syscall nuevos o mejorados que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="96e30-1049">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="96e30-1050">Los llamadas syscall de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="96e30-1050">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="96e30-1051">Compilación 14986</span><span class="sxs-lookup"><span data-stu-id="96e30-1051">Build 14986</span></span>

<span data-ttu-id="96e30-1052">Para obtener información general sobre Windows sobre la compilación 14986, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span><span class="sxs-lookup"><span data-stu-id="96e30-1052">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-1053">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-1053">Fixed</span></span>

- <span data-ttu-id="96e30-1054">Se corrigió bugchecks con NetLink y el ioctl de PTY</span><span class="sxs-lookup"><span data-stu-id="96e30-1054">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="96e30-1055">La versión del kernel ahora informa a 4.4.0-43 por coherencia con Xenial</span><span class="sxs-lookup"><span data-stu-id="96e30-1055">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="96e30-1056">Bash. exe ahora se inicia cuando la entrada se dirige a ' NUL: ' (alvent #1259)</span><span class="sxs-lookup"><span data-stu-id="96e30-1056">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="96e30-1057">Los identificadores de subproceso ahora se han declarado correctamente en procfs (alvent #967)</span><span class="sxs-lookup"><span data-stu-id="96e30-1057">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="96e30-1058">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | Las marcas de IN_ISDIR ahora se admiten en inotify_add_watch () (alvent #1280)</span><span class="sxs-lookup"><span data-stu-id="96e30-1058">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="96e30-1059">Implemente timer_create y las llamadas del sistema relacionadas.</span><span class="sxs-lookup"><span data-stu-id="96e30-1059">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="96e30-1060">Esto habilita la compatibilidad con GHC (alvent #307)</span><span class="sxs-lookup"><span data-stu-id="96e30-1060">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="96e30-1061">Se corrigió un problema en el que ping devolvió una hora de 0,000 MS (alvent #1296)</span><span class="sxs-lookup"><span data-stu-id="96e30-1061">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="96e30-1062">Devuelve el código de error correcto cuando se abren demasiados archivos.</span><span class="sxs-lookup"><span data-stu-id="96e30-1062">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="96e30-1063">Se corrigió un problema en WSL donde la solicitud de NetLink de datos de la interfaz de red generaba un error con EINVAL si la dirección de hardware de la interfaz es de 32 bytes (por ejemplo, la interfaz Teredo)</span><span class="sxs-lookup"><span data-stu-id="96e30-1063">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="96e30-1064">Tenga en cuenta que la utilidad "IP" de Linux contiene un error en el que se bloqueará si WSL informa de una dirección de hardware de 32 bytes.</span><span class="sxs-lookup"><span data-stu-id="96e30-1064">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="96e30-1065">Se trata de un error en "IP", no en WSL.</span><span class="sxs-lookup"><span data-stu-id="96e30-1065">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="96e30-1066">La utilidad "IP" codifica de forma rígida la longitud del búfer de cadena usado para imprimir la dirección de hardware y el búfer es demasiado pequeño para imprimir una dirección de hardware de 32 bytes.</span><span class="sxs-lookup"><span data-stu-id="96e30-1066">The “ip” utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="96e30-1067">Correcciones y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-1067">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-1068">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-1068">LTP Results:</span></span>
<span data-ttu-id="96e30-1069">Número de pruebas superadas: 669</span><span class="sxs-lookup"><span data-stu-id="96e30-1069">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="96e30-1070">Número de pasos no superados (error, omitido, etc.): 258</span><span class="sxs-lookup"><span data-stu-id="96e30-1070">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="96e30-1071">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="96e30-1071">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="96e30-1072">Compatibilidad con syscall</span><span class="sxs-lookup"><span data-stu-id="96e30-1072">Syscall Support</span></span>
<span data-ttu-id="96e30-1073">A continuación se muestra una lista de llamadas syscall nuevos o mejorados que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="96e30-1073">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="96e30-1074">Los llamadas syscall de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="96e30-1074">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="96e30-1075">Compilación 14971</span><span class="sxs-lookup"><span data-stu-id="96e30-1075">Build 14971</span></span>

<span data-ttu-id="96e30-1076">Para obtener información general sobre Windows sobre la compilación 14971, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="96e30-1076">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-1077">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-1077">Fixed</span></span>

 - <span data-ttu-id="96e30-1078">Debido a circunstancias más allá de nuestro control, no hay ninguna actualización en esta compilación para el subsistema de Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="96e30-1078">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="96e30-1079">Las actualizaciones programadas regularmente se reanudarán en la próxima versión.</span><span class="sxs-lookup"><span data-stu-id="96e30-1079">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-1080">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-1080">LTP Results:</span></span>
<span data-ttu-id="96e30-1081">Sin cambios desde 14965</span><span class="sxs-lookup"><span data-stu-id="96e30-1081">Unchanged from 14965</span></span> </br>
<span data-ttu-id="96e30-1082">Número de pruebas superadas: 664</span><span class="sxs-lookup"><span data-stu-id="96e30-1082">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="96e30-1083">Número de pasos no superados (error, omitido, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="96e30-1083">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="96e30-1084">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="96e30-1084">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="96e30-1085">Compilación 14965</span><span class="sxs-lookup"><span data-stu-id="96e30-1085">Build 14965</span></span>

<span data-ttu-id="96e30-1086">Para obtener información general sobre Windows sobre la compilación 14965, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="96e30-1086">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-1087">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-1087">Fixed</span></span>

- <span data-ttu-id="96e30-1088">Compatibilidad con RTM_GETLINK y RTM_GETADDR del protocolo NetLink Sockets NETLINK_ROUTE (alvent #468)</span><span class="sxs-lookup"><span data-stu-id="96e30-1088">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="96e30-1089">Habilita los comandos ifconfig y IP para la enumeración de red</span><span class="sxs-lookup"><span data-stu-id="96e30-1089">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="96e30-1090">Puede encontrar más información en nuestra [entrada de blog sobre redes de WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span><span class="sxs-lookup"><span data-stu-id="96e30-1090">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="96e30-1091">/sbin está ahora en la ruta de acceso del usuario de forma predeterminada</span><span class="sxs-lookup"><span data-stu-id="96e30-1091">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="96e30-1092">La ruta de acceso de usuario de NT ahora se anexa a la ruta de acceso de WSL de forma predeterminada (es decir, ahora puede escribir Notepad. exe sin agregar system32 a la ruta de acceso de Linux)</span><span class="sxs-lookup"><span data-stu-id="96e30-1092">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="96e30-1093">Compatibilidad agregada para/proc/sys/kernel/cap_last_cap</span><span class="sxs-lookup"><span data-stu-id="96e30-1093">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="96e30-1094">Los archivos binarios de NT ahora se pueden iniciar desde WSL cuando el directorio de trabajo actual contiene caracteres que no son ANSI (alvent #1254)</span><span class="sxs-lookup"><span data-stu-id="96e30-1094">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="96e30-1095">Permita el apagado en el socket de flujo UNIX desconectado.</span><span class="sxs-lookup"><span data-stu-id="96e30-1095">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="96e30-1096">Compatibilidad agregada para PR_GET_PDEATHSIG.</span><span class="sxs-lookup"><span data-stu-id="96e30-1096">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="96e30-1097">Compatibilidad agregada para CLONE_PARENT</span><span class="sxs-lookup"><span data-stu-id="96e30-1097">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="96e30-1098">Se corrigió un error en el que la canalización se bloquea, es decir, bash-c "LS-alR/" | Bash-c "gato" (alvent #1214)</span><span class="sxs-lookup"><span data-stu-id="96e30-1098">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="96e30-1099">Controle las solicitudes para conectarse al terminal actual.</span><span class="sxs-lookup"><span data-stu-id="96e30-1099">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="96e30-1100">Marque/proc/<pid>/oom_score_adj como grabable.</span><span class="sxs-lookup"><span data-stu-id="96e30-1100">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="96e30-1101">Agregue la carpeta/sys/FS/cgroup.</span><span class="sxs-lookup"><span data-stu-id="96e30-1101">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="96e30-1102">sched_setaffinity debe devolver el número de máscara de bits de afinidad</span><span class="sxs-lookup"><span data-stu-id="96e30-1102">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="96e30-1103">Corregir la lógica de validación de ELF que presupone incorrectamente que las rutas de intérprete deben tener menos de 64 caracteres de longitud.</span><span class="sxs-lookup"><span data-stu-id="96e30-1103">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="96e30-1104">(ALVENT #743)</span><span class="sxs-lookup"><span data-stu-id="96e30-1104">(GH #743)</span></span>
- <span data-ttu-id="96e30-1105">Los descriptores de archivo abiertos pueden mantener abierta la ventana de consola (alvent #1187)</span><span class="sxs-lookup"><span data-stu-id="96e30-1105">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="96e30-1106">Error de Fixeed en el que se produjo un error al cambiar el nombre () con la barra diagonal final en el nombre de destino (alvent #1008)</span><span class="sxs-lookup"><span data-stu-id="96e30-1106">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="96e30-1107">Implementar el archivo/proc/net/dev</span><span class="sxs-lookup"><span data-stu-id="96e30-1107">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="96e30-1108">Se ha corregido 0,000 MS ping debido a la resolución del temporizador.</span><span class="sxs-lookup"><span data-stu-id="96e30-1108">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="96e30-1109">/Proc/Self/ENVIRON implementado (alvent #730)</span><span class="sxs-lookup"><span data-stu-id="96e30-1109">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="96e30-1110">Correcciones y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-1110">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-1111">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-1111">LTP Results:</span></span>
<span data-ttu-id="96e30-1112">Número de pruebas superadas: 664</span><span class="sxs-lookup"><span data-stu-id="96e30-1112">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="96e30-1113">Número de pasos no superados (error, omitido, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="96e30-1113">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="96e30-1114">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="96e30-1114">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="96e30-1115">Compilación 14959</span><span class="sxs-lookup"><span data-stu-id="96e30-1115">Build 14959</span></span>

<span data-ttu-id="96e30-1116">Para obtener información general sobre Windows sobre la compilación 14959, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span><span class="sxs-lookup"><span data-stu-id="96e30-1116">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-1117">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-1117">Fixed</span></span>

- <span data-ttu-id="96e30-1118">Notificación de proceso pico mejorada para Windows.</span><span class="sxs-lookup"><span data-stu-id="96e30-1118">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="96e30-1119">Encontrará información adicional en el [blog de WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span><span class="sxs-lookup"><span data-stu-id="96e30-1119">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="96e30-1120">Estabilidad mejorada con la interoperabilidad de Windows</span><span class="sxs-lookup"><span data-stu-id="96e30-1120">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="96e30-1121">Se corrigió el error 0x80070057 al iniciar bash. exe cuando está habilitada la protección de datos empresariales (este)</span><span class="sxs-lookup"><span data-stu-id="96e30-1121">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="96e30-1122">Correcciones y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-1122">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-1123">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-1123">LTP Results:</span></span>
<span data-ttu-id="96e30-1124">Número de pruebas superadas: 665</span><span class="sxs-lookup"><span data-stu-id="96e30-1124">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="96e30-1125">Número de pasos no superados (error, omitido, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="96e30-1125">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="96e30-1126">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="96e30-1126">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="96e30-1127">Compilación 14955</span><span class="sxs-lookup"><span data-stu-id="96e30-1127">Build 14955</span></span>

<span data-ttu-id="96e30-1128">Para obtener información general sobre Windows sobre la compilación 14955, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span><span class="sxs-lookup"><span data-stu-id="96e30-1128">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-1129">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-1129">Fixed</span></span>

 - <span data-ttu-id="96e30-1130">Debido a circunstancias más allá de nuestro control, no hay ninguna actualización en esta compilación para el subsistema de Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="96e30-1130">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="96e30-1131">Las actualizaciones programadas regularmente se reanudarán en la próxima versión.</span><span class="sxs-lookup"><span data-stu-id="96e30-1131">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-1132">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-1132">LTP Results:</span></span>
<span data-ttu-id="96e30-1133">Número de pruebas superadas: 665</span><span class="sxs-lookup"><span data-stu-id="96e30-1133">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="96e30-1134">Número de pasos no superados (error, omitido, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="96e30-1134">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="96e30-1135">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="96e30-1135">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="96e30-1136">Compilación 14951</span><span class="sxs-lookup"><span data-stu-id="96e30-1136">Build 14951</span></span>

<span data-ttu-id="96e30-1137">Para obtener información general sobre Windows sobre la compilación 14951, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="96e30-1137">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="96e30-1138">Nueva característica: Interoperabilidad con Windows/Ubuntu</span><span class="sxs-lookup"><span data-stu-id="96e30-1138">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="96e30-1139">Los archivos binarios de Windows ahora se pueden invocar directamente desde la línea de comandos de WSL.</span><span class="sxs-lookup"><span data-stu-id="96e30-1139">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="96e30-1140">Esto proporciona a los usuarios la capacidad de interactuar con el entorno y el sistema Windows de una manera que no se haya podido realizar.</span><span class="sxs-lookup"><span data-stu-id="96e30-1140">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="96e30-1141">Como ejemplo rápido, ahora es posible que los usuarios ejecuten los siguientes comandos:</span><span class="sxs-lookup"><span data-stu-id="96e30-1141">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="96e30-1142">Puede encontrar más información en:</span><span class="sxs-lookup"><span data-stu-id="96e30-1142">More information can be found at:</span></span>

- [<span data-ttu-id="96e30-1143">Blog del equipo de WSL para Interop</span><span class="sxs-lookup"><span data-stu-id="96e30-1143">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="96e30-1144">Documentación de interoperabilidad de MSDN</span><span class="sxs-lookup"><span data-stu-id="96e30-1144">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="96e30-1145">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-1145">Fixed</span></span>

- <span data-ttu-id="96e30-1146">Ubuntu 16,04 (Xenial) ya está instalado para todas las instancias nuevas de WSL.</span><span class="sxs-lookup"><span data-stu-id="96e30-1146">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="96e30-1147">Los usuarios con instancias existentes de 14,04 (Trusty) no se actualizarán automáticamente.</span><span class="sxs-lookup"><span data-stu-id="96e30-1147">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="96e30-1148">La configuración regional establecida durante la instalación se muestra ahora</span><span class="sxs-lookup"><span data-stu-id="96e30-1148">Locale set during install is now displayed</span></span>
- <span data-ttu-id="96e30-1149">Mejoras de terminal que incluyen un error en el que la redirección de un proceso WSL a un archivo no siempre funciona</span><span class="sxs-lookup"><span data-stu-id="96e30-1149">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="96e30-1150">La duración de la consola debe estar asociada a la duración de Bash. exe</span><span class="sxs-lookup"><span data-stu-id="96e30-1150">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="96e30-1151">El tamaño de la ventana de la consola debe usar un tamaño visible, no el tamaño del búfer</span><span class="sxs-lookup"><span data-stu-id="96e30-1151">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="96e30-1152">Correcciones y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-1152">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-1153">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-1153">LTP Results:</span></span>
<span data-ttu-id="96e30-1154">Número de pruebas superadas: 665</span><span class="sxs-lookup"><span data-stu-id="96e30-1154">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="96e30-1155">Número de pasos no superados (error, omitido, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="96e30-1155">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="96e30-1156">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="96e30-1156">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="96e30-1157">Compilación 14946</span><span class="sxs-lookup"><span data-stu-id="96e30-1157">Build 14946</span></span>

<span data-ttu-id="96e30-1158">Para obtener información general sobre Windows sobre la compilación 14946, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span><span class="sxs-lookup"><span data-stu-id="96e30-1158">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-1159">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-1159">Fixed</span></span>

- <span data-ttu-id="96e30-1160">Se corrigió un problema que impedía la creación de cuentas de usuario de WSL para los usuarios con nombres de usuario NT que contienen espacios o comillas.</span><span class="sxs-lookup"><span data-stu-id="96e30-1160">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="96e30-1161">Cambie VolFs y DrvFs para que devuelva 0 para el recuento de vínculos de directorio en STAT</span><span class="sxs-lookup"><span data-stu-id="96e30-1161">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="96e30-1162">Compatibilidad con la opción de socket IPV6_MULTICAST_HOPS.</span><span class="sxs-lookup"><span data-stu-id="96e30-1162">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="96e30-1163">Limite a un bucle de e/s de consola única por TTY.</span><span class="sxs-lookup"><span data-stu-id="96e30-1163">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="96e30-1164">Ejemplo: el siguiente comando es posible:</span><span class="sxs-lookup"><span data-stu-id="96e30-1164">Example: the following command is possible:</span></span>
  - <span data-ttu-id="96e30-1165">Bash-c "datos de Eco" | Bash-c "ssh user@example.com " cat > foo. txt ' "</span><span class="sxs-lookup"><span data-stu-id="96e30-1165">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="96e30-1166">reemplazar espacios con pestañas en/proc/cpuinfo (alvent #1115)</span><span class="sxs-lookup"><span data-stu-id="96e30-1166">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="96e30-1167">DrvFs aparece ahora en mountinfo con un nombre que coincide con el volumen de Windows montado</span><span class="sxs-lookup"><span data-stu-id="96e30-1167">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="96e30-1168">/Home y/root ahora aparecen en mountinfo con los nombres correctos</span><span class="sxs-lookup"><span data-stu-id="96e30-1168">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="96e30-1169">Correcciones y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-1169">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-1170">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-1170">LTP Results:</span></span>
<span data-ttu-id="96e30-1171">Número de pruebas superadas: 665</span><span class="sxs-lookup"><span data-stu-id="96e30-1171">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="96e30-1172">Número de pasos no superados (error, omitido, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="96e30-1172">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="96e30-1173">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="96e30-1173">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="96e30-1174">Compilación 14942</span><span class="sxs-lookup"><span data-stu-id="96e30-1174">Build 14942</span></span>

<span data-ttu-id="96e30-1175">Para obtener información general sobre Windows sobre la compilación 14942, visite el [blog de Windows](https://aka.ms/onefourninefourtwoooooo).</span><span class="sxs-lookup"><span data-stu-id="96e30-1175">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-1176">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-1176">Fixed</span></span>

- <span data-ttu-id="96e30-1177">Un número de bugchecks direccionado, incluido el bloqueo de red "intento de ejecución de memoria noexecute" que bloqueaba SSH</span><span class="sxs-lookup"><span data-stu-id="96e30-1177">A number of bugchecks addressed, including the “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” networking crash which was blocking SSH</span></span>
- <span data-ttu-id="96e30-1178">la compatibilidad de inotifiy con las notificaciones generadas desde aplicaciones Windows en DrvFs ahora está en</span><span class="sxs-lookup"><span data-stu-id="96e30-1178">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="96e30-1179">Implemente TCP_KEEPIDLE y TCP_KEEPINTVL para mongod.</span><span class="sxs-lookup"><span data-stu-id="96e30-1179">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="96e30-1180">(ALVENT #695)</span><span class="sxs-lookup"><span data-stu-id="96e30-1180">(GH #695)</span></span>
- <span data-ttu-id="96e30-1181">Implementar la llamada del sistema pivot_root</span><span class="sxs-lookup"><span data-stu-id="96e30-1181">Implement the pivot_root system call</span></span>
- <span data-ttu-id="96e30-1182">Opción de implementación de socket para SO_DONTROUTE</span><span class="sxs-lookup"><span data-stu-id="96e30-1182">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="96e30-1183">Correcciones y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-1183">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="96e30-1184">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-1184">LTP Results:</span></span>
<span data-ttu-id="96e30-1185">Número de pruebas superadas: 665</span><span class="sxs-lookup"><span data-stu-id="96e30-1185">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="96e30-1186">Número de pasos no superados (error, omitido, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="96e30-1186">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="96e30-1187">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="96e30-1187">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="96e30-1188">Compatibilidad con syscall</span><span class="sxs-lookup"><span data-stu-id="96e30-1188">Syscall Support</span></span>
<span data-ttu-id="96e30-1189">A continuación se muestra una lista de llamadas syscall nuevos o mejorados que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="96e30-1189">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="96e30-1190">Los llamadas syscall de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="96e30-1190">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="96e30-1191">Compilación 14936</span><span class="sxs-lookup"><span data-stu-id="96e30-1191">Build 14936</span></span>

<span data-ttu-id="96e30-1192">Para obtener información general sobre Windows sobre la compilación 14936, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="96e30-1192">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="96e30-1193">Nota: WSL instalará Ubuntu versión 16,04 (Xenial) en lugar de Ubuntu 14,04 (Trusty) en una próxima versión.</span><span class="sxs-lookup"><span data-stu-id="96e30-1193">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="96e30-1194">Este cambio se aplicará a la instalación de instancias nuevas (lxrun. exe/Install o a la primera ejecución de Bash. exe).</span><span class="sxs-lookup"><span data-stu-id="96e30-1194">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="96e30-1195">Las instancias existentes con confianza no se actualizarán automáticamente.</span><span class="sxs-lookup"><span data-stu-id="96e30-1195">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="96e30-1196">Los usuarios pueden actualizar su imagen de confianza a Xenial mediante el comando do-Release-upgrade.</span><span class="sxs-lookup"><span data-stu-id="96e30-1196">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="96e30-1197">Problema conocido</span><span class="sxs-lookup"><span data-stu-id="96e30-1197">Known Issue</span></span>
<span data-ttu-id="96e30-1198">WSL está experimentando un problema con algunas implementaciones de Sockets.</span><span class="sxs-lookup"><span data-stu-id="96e30-1198">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="96e30-1199">La comprobación de errores se manifiesta como un bloqueo con el error "intento de ejecución de la memoria noexecute".</span><span class="sxs-lookup"><span data-stu-id="96e30-1199">The bugcheck manifests itself as a crash with the error “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”.</span></span>  <span data-ttu-id="96e30-1200">La manifestación más común de este problema es un bloqueo cuando se usa SSH.</span><span class="sxs-lookup"><span data-stu-id="96e30-1200">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="96e30-1201">La causa principal se ha corregido en las compilaciones internas y se insertará en la parte más temprana de la oportunidad.</span><span class="sxs-lookup"><span data-stu-id="96e30-1201">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="96e30-1202">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-1202">Fixed</span></span>

- <span data-ttu-id="96e30-1203">Implementación de la llamada del sistema chroot</span><span class="sxs-lookup"><span data-stu-id="96e30-1203">Implemented the chroot system call</span></span>
- <span data-ttu-id="96e30-1204">Mejoras en inotify ~~, incluida la compatibilidad con notificaciones generadas desde aplicaciones Windows en DrvFs~~</span><span class="sxs-lookup"><span data-stu-id="96e30-1204">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="96e30-1205">Corregir La compatibilidad de inotify con los cambios que se originan en aplicaciones Windows no están disponibles en este momento.</span><span class="sxs-lookup"><span data-stu-id="96e30-1205">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="96e30-1206">Enlace de socket a IPv6:<port n> : ahora admite IPV6_V6ONLY (alvent #68, #157, #393, #460, #674, #740, #982, #996)</span><span class="sxs-lookup"><span data-stu-id="96e30-1206">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="96e30-1207">Comportamiento de WNOWAIT para waitid systemcall implementado (alvent #638)</span><span class="sxs-lookup"><span data-stu-id="96e30-1207">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="96e30-1208">Compatibilidad con las opciones de socket de IP IP_HDRINCL y IP_TTL</span><span class="sxs-lookup"><span data-stu-id="96e30-1208">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="96e30-1209">La lectura de longitud cero () debe volver inmediatamente (alvent #975)</span><span class="sxs-lookup"><span data-stu-id="96e30-1209">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="96e30-1210">Administrar correctamente los nombres de archivo y los prefijos de nombre de archivo que no incluyen un terminador NULL en un archivo. tar.</span><span class="sxs-lookup"><span data-stu-id="96e30-1210">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="96e30-1211">compatibilidad con epoll para/dev/null</span><span class="sxs-lookup"><span data-stu-id="96e30-1211">epoll support for /dev/null</span></span>
- <span data-ttu-id="96e30-1212">Corregir origen de hora de/dev/Alarm</span><span class="sxs-lookup"><span data-stu-id="96e30-1212">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="96e30-1213">Bash-c ahora puede redirigir a un archivo</span><span class="sxs-lookup"><span data-stu-id="96e30-1213">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="96e30-1214">Correcciones y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-1214">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-1215">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-1215">LTP Results:</span></span>
<span data-ttu-id="96e30-1216">Número de pruebas superadas: 664</span><span class="sxs-lookup"><span data-stu-id="96e30-1216">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="96e30-1217">Número de pasos no superados (error, omitido, etc.): 264</span><span class="sxs-lookup"><span data-stu-id="96e30-1217">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="96e30-1218">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="96e30-1218">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="96e30-1219">Compatibilidad con syscall</span><span class="sxs-lookup"><span data-stu-id="96e30-1219">Syscall Support</span></span>
<span data-ttu-id="96e30-1220">A continuación se muestra una lista de llamadas syscall nuevos o mejorados que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="96e30-1220">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="96e30-1221">Los llamadas syscall de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="96e30-1221">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="96e30-1222">Compilación 14931</span><span class="sxs-lookup"><span data-stu-id="96e30-1222">Build 14931</span></span>

<span data-ttu-id="96e30-1223">Para obtener información general sobre Windows sobre la compilación 14931, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="96e30-1223">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-1224">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-1224">Fixed</span></span>

 - <span data-ttu-id="96e30-1225">Debido a circunstancias más allá de nuestro control, no hay ninguna actualización en esta compilación para el subsistema de Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="96e30-1225">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="96e30-1226">Las actualizaciones programadas regularmente se reanudarán en la próxima versión.</span><span class="sxs-lookup"><span data-stu-id="96e30-1226">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="96e30-1227">Compilación 14926</span><span class="sxs-lookup"><span data-stu-id="96e30-1227">Build 14926</span></span>

<span data-ttu-id="96e30-1228">Para obtener información general sobre Windows sobre la compilación 14926, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="96e30-1228">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-1229">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-1229">Fixed</span></span>

- <span data-ttu-id="96e30-1230">Ping Now funciona en consolas que no tienen privilegios de administrador</span><span class="sxs-lookup"><span data-stu-id="96e30-1230">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="96e30-1231">También se admite Ping6, sin privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="96e30-1231">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="96e30-1232">Compatibilidad de inotify con archivos modificados a través de WSL.</span><span class="sxs-lookup"><span data-stu-id="96e30-1232">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="96e30-1233">(ALVENT #216)</span><span class="sxs-lookup"><span data-stu-id="96e30-1233">(GH #216)</span></span>
  - <span data-ttu-id="96e30-1234">Marcas admitidas:</span><span class="sxs-lookup"><span data-stu-id="96e30-1234">Flags supported:</span></span>
    - <span data-ttu-id="96e30-1235">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="96e30-1235">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="96e30-1236">eventos de inotify_add_watch: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="96e30-1236">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="96e30-1237">atributos inotify_add_watch: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="96e30-1237">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="96e30-1238">salida de lectura: LX_IN_ISDIR, LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="96e30-1238">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="96e30-1239">Problema conocido: La modificación de archivos desde aplicaciones Windows no genera ningún evento</span><span class="sxs-lookup"><span data-stu-id="96e30-1239">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="96e30-1240">El socket de UNIX ahora es compatible con SCM_CREDENTIALS</span><span class="sxs-lookup"><span data-stu-id="96e30-1240">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="96e30-1241">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="96e30-1241">LTP Results:</span></span>
<span data-ttu-id="96e30-1242">Número de pruebas superadas: 651</span><span class="sxs-lookup"><span data-stu-id="96e30-1242">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="96e30-1243">Número de pasos no superados (error, omitido, etc.): 258</span><span class="sxs-lookup"><span data-stu-id="96e30-1243">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="96e30-1244">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="96e30-1244">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="96e30-1245">Compilación 14915</span><span class="sxs-lookup"><span data-stu-id="96e30-1245">Build 14915</span></span>

<span data-ttu-id="96e30-1246">Para obtener información general sobre Windows sobre la compilación 14915, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="96e30-1246">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-1247">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-1247">Fixed</span></span>
-  <span data-ttu-id="96e30-1248">Socketpair para Sockets de datagramas UNIX (alvent #262)</span><span class="sxs-lookup"><span data-stu-id="96e30-1248">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="96e30-1249">Compatibilidad con el socket de UNIX para SO_REUSEADDR</span><span class="sxs-lookup"><span data-stu-id="96e30-1249">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="96e30-1250">Compatibilidad con el socket de UNIX para SO_BROADCAST (alvent #568)</span><span class="sxs-lookup"><span data-stu-id="96e30-1250">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="96e30-1251">Compatibilidad con el socket de UNIX para SOCK_SEQPACKET (alvent #758, #546)</span><span class="sxs-lookup"><span data-stu-id="96e30-1251">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="96e30-1252">Adición de compatibilidad para el envío, recepción y cierre de sockets de datagramas de UNIX</span><span class="sxs-lookup"><span data-stu-id="96e30-1252">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="96e30-1253">Corrección de BugCheck debido a la validación de parámetros mmap no válidos para direcciones no fijas.</span><span class="sxs-lookup"><span data-stu-id="96e30-1253">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="96e30-1254">(ALVENT #847)</span><span class="sxs-lookup"><span data-stu-id="96e30-1254">(GH #847)</span></span>
- <span data-ttu-id="96e30-1255">Compatibilidad para suspender o reanudar los Estados de terminal</span><span class="sxs-lookup"><span data-stu-id="96e30-1255">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="96e30-1256">Compatibilidad con TIOCPKT ioctl para desbloquear la utilidad de pantalla (alvent #774)</span><span class="sxs-lookup"><span data-stu-id="96e30-1256">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="96e30-1257">Problema conocido: Teclas de función no operativas</span><span class="sxs-lookup"><span data-stu-id="96e30-1257">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="96e30-1258">Se corrigió una carrera en TimerFd que podía hacer que un miembro liberado ' ReaderReady ' estuviera accesible para LxpTimerFdWorkerRoutine (alvent #814)</span><span class="sxs-lookup"><span data-stu-id="96e30-1258">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="96e30-1259">Habilitar la compatibilidad con llamadas del sistema reiniciables para Futex, Poll y clock_nanosleep</span><span class="sxs-lookup"><span data-stu-id="96e30-1259">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="96e30-1260">Compatibilidad con montaje de enlace agregado</span><span class="sxs-lookup"><span data-stu-id="96e30-1260">Added bind mount support</span></span>
- <span data-ttu-id="96e30-1261">dejar de compartir la compatibilidad con el espacio de nombres Mount</span><span class="sxs-lookup"><span data-stu-id="96e30-1261">unshare for mount namespace support</span></span>
    - <span data-ttu-id="96e30-1262">Problema conocido: Al crear un nuevo espacio de nombres `unshare(CLONE_NEWNS)` de montaje con el directorio de trabajo actual, continuará señalando al espacio de nombres anterior</span><span class="sxs-lookup"><span data-stu-id="96e30-1262">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="96e30-1263">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-1263">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="96e30-1264">Compilación 14905</span><span class="sxs-lookup"><span data-stu-id="96e30-1264">Build 14905</span></span>

<span data-ttu-id="96e30-1265">Para obtener información general sobre Windows sobre la compilación 14905, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span><span class="sxs-lookup"><span data-stu-id="96e30-1265">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-1266">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-1266">Fixed</span></span>
- <span data-ttu-id="96e30-1267">Ahora se admiten llamadas del sistema reiniciables (alvent #349, alvent #520)</span><span class="sxs-lookup"><span data-stu-id="96e30-1267">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="96e30-1268">Vínculos simbólicos a directorios que terminan en/ahora operativo (alvent #650)</span><span class="sxs-lookup"><span data-stu-id="96e30-1268">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="96e30-1269">RNDGETENTCNT ioctl implementado para/dev/random</span><span class="sxs-lookup"><span data-stu-id="96e30-1269">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="96e30-1270">Se implementaron los archivos/proc/[PID]/mounts,/proc/[PID]/mountinfo y/proc/[PID]/mountstats</span><span class="sxs-lookup"><span data-stu-id="96e30-1270">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="96e30-1271">Correcciones y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-1271">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="96e30-1272">Compilación 14901</span><span class="sxs-lookup"><span data-stu-id="96e30-1272">Build 14901</span></span>
<span data-ttu-id="96e30-1273">Primera compilación Insider para la versión posterior de la actualización de aniversario de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="96e30-1273">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="96e30-1274">Para obtener información general sobre Windows sobre la compilación 14901, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="96e30-1274">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-1275">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-1275">Fixed</span></span>
- <span data-ttu-id="96e30-1276">Problema de barra diagonal final corregida</span><span class="sxs-lookup"><span data-stu-id="96e30-1276">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="96e30-1277">Comandos como `$ mv a/c/ a/b/` Now Work</span><span class="sxs-lookup"><span data-stu-id="96e30-1277">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="96e30-1278">Al instalar ahora se le pregunta si la configuración regional de Ubuntu debe establecerse en configuración regional de Windows.</span><span class="sxs-lookup"><span data-stu-id="96e30-1278">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="96e30-1279">Compatibilidad con procfs para la carpeta NS</span><span class="sxs-lookup"><span data-stu-id="96e30-1279">Procfs support for ns folder</span></span>
- <span data-ttu-id="96e30-1280">Se ha agregado el montaje y el desmontaje de los sistemas de archivos tmpfs, procfs y sysfs</span><span class="sxs-lookup"><span data-stu-id="96e30-1280">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="96e30-1281">Fix mknod [at] firma ABI de 32 bits</span><span class="sxs-lookup"><span data-stu-id="96e30-1281">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="96e30-1282">Los sockets Unix se movieron al modelo Dispatch</span><span class="sxs-lookup"><span data-stu-id="96e30-1282">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="96e30-1283">Se debe respetar el tamaño del búfer de recepción del socket de INET mediante el valor de la memoria</span><span class="sxs-lookup"><span data-stu-id="96e30-1283">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="96e30-1284">Implementar la marca de mensaje de recepción de socket Unix MSG_CMSG_CLOEXEC</span><span class="sxs-lookup"><span data-stu-id="96e30-1284">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="96e30-1285">Redirección de canalización stdin/stdout de proceso de Linux (alvent #2)</span><span class="sxs-lookup"><span data-stu-id="96e30-1285">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="96e30-1286">Permite la canalización de comandos Bash-c en CMD.</span><span class="sxs-lookup"><span data-stu-id="96e30-1286">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="96e30-1287">Ejemplo: > dir | Bash-c "grep foo"</span><span class="sxs-lookup"><span data-stu-id="96e30-1287">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="96e30-1288">Bash ahora se puede instalar en sistemas con varios webfilesystems (alvent #538, #358)</span><span class="sxs-lookup"><span data-stu-id="96e30-1288">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="96e30-1289">El tamaño predeterminado del búfer del socket de INET debe coincidir con el de la configuración predeterminada de Ubuntu</span><span class="sxs-lookup"><span data-stu-id="96e30-1289">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="96e30-1290">Alinee xattr llamadas syscall con listxattr</span><span class="sxs-lookup"><span data-stu-id="96e30-1290">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="96e30-1291">Solo se devuelven interfaces con una dirección IPv4 válida de SIOCGIFCONF</span><span class="sxs-lookup"><span data-stu-id="96e30-1291">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="96e30-1292">Corregir la acción predeterminada de la señal cuando se inserta por ptrace</span><span class="sxs-lookup"><span data-stu-id="96e30-1292">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="96e30-1293">implementación de/proc/sys/VM/min_free_kbytes</span><span class="sxs-lookup"><span data-stu-id="96e30-1293">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="96e30-1294">Usar valores de registro de contexto de equipo al restaurar el contexto en sigreturn</span><span class="sxs-lookup"><span data-stu-id="96e30-1294">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="96e30-1295">Esto resuelve el problema por el que Java y javac estaban bloqueados para algunos usuarios</span><span class="sxs-lookup"><span data-stu-id="96e30-1295">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="96e30-1296">Implementación de/proc/sys/kernel/hostname</span><span class="sxs-lookup"><span data-stu-id="96e30-1296">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="96e30-1297">Compatibilidad con syscall</span><span class="sxs-lookup"><span data-stu-id="96e30-1297">Syscall Support</span></span>
<span data-ttu-id="96e30-1298">A continuación se muestra una lista de llamadas syscall nuevos o mejorados que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="96e30-1298">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="96e30-1299">Los llamadas syscall de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="96e30-1299">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="96e30-1300">Compilación 14388 a actualización de aniversario de Windows 10</span><span class="sxs-lookup"><span data-stu-id="96e30-1300">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="96e30-1301">Para obtener información general sobre Windows sobre la compilación 14388, visite el [blog de Windows](https://aka.ms/14388wip).</span><span class="sxs-lookup"><span data-stu-id="96e30-1301">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="96e30-1302">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-1302">Fixed</span></span>
- <span data-ttu-id="96e30-1303">Correcciones para preparar la actualización de aniversario de Windows 10 en 8/2</span><span class="sxs-lookup"><span data-stu-id="96e30-1303">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="96e30-1304">Puede encontrar más información sobre WSL en la actualización de aniversario en nuestro [blog](https://blogs.msdn.microsoft.com/wsl/) .</span><span class="sxs-lookup"><span data-stu-id="96e30-1304">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="96e30-1305">Compilación 14376</span><span class="sxs-lookup"><span data-stu-id="96e30-1305">Build 14376</span></span>
<span data-ttu-id="96e30-1306">Para obtener información general sobre Windows sobre la compilación 14376, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="96e30-1306">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="96e30-1307">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-1307">Fixed</span></span>
- <span data-ttu-id="96e30-1308">Se quitaron algunas instancias en las que apt-get se bloquea (alvent #493)</span><span class="sxs-lookup"><span data-stu-id="96e30-1308">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="96e30-1309">Se corrigió un problema por el que los montajes vacíos no se controlaban correctamente</span><span class="sxs-lookup"><span data-stu-id="96e30-1309">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="96e30-1310">Se corrigió un problema por el que los ramdisk no se montaron correctamente</span><span class="sxs-lookup"><span data-stu-id="96e30-1310">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="96e30-1311">Cambiar aceptación de socket de UNIX a marcas de compatibilidad (alvent parciales #451)</span><span class="sxs-lookup"><span data-stu-id="96e30-1311">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="96e30-1312">Pantalla desazul relacionada con la red común fija</span><span class="sxs-lookup"><span data-stu-id="96e30-1312">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="96e30-1313">Se corrigió la pantalla azul al obtener acceso a/proc/[PID]/secuencias (alvent #523)</span><span class="sxs-lookup"><span data-stu-id="96e30-1313">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="96e30-1314">Se corrigió un uso elevado de la CPU en algunos escenarios de PTY (alvent #488, #504)</span><span class="sxs-lookup"><span data-stu-id="96e30-1314">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="96e30-1315">Correcciones y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-1315">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="96e30-1316">Compilación 14371</span><span class="sxs-lookup"><span data-stu-id="96e30-1316">Build 14371</span></span>
<span data-ttu-id="96e30-1317">Para obtener información general sobre Windows sobre la compilación 14371, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="96e30-1317">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="96e30-1318">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-1318">Fixed</span></span>
- <span data-ttu-id="96e30-1319">Se corrigió la carrera de tiempo con SIGCHLD y wait () al usar ptrace</span><span class="sxs-lookup"><span data-stu-id="96e30-1319">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="96e30-1320">Corrección de un comportamiento cuando las rutas de acceso tienen una o varias #432</span><span class="sxs-lookup"><span data-stu-id="96e30-1320">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="96e30-1321">Se corrigió un problema con el error de cambio de nombre o desvinculación debido a identificadores abiertos a elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="96e30-1321">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="96e30-1322">Correcciones y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-1322">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="96e30-1323">Compilación 14366</span><span class="sxs-lookup"><span data-stu-id="96e30-1323">Build 14366</span></span>
<span data-ttu-id="96e30-1324">Para obtener información general sobre Windows sobre la compilación 14366, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span><span class="sxs-lookup"><span data-stu-id="96e30-1324">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="96e30-1325">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-1325">Fixed</span></span>
- <span data-ttu-id="96e30-1326">Corrección en la creación de archivos mediante vínculos simbólicos</span><span class="sxs-lookup"><span data-stu-id="96e30-1326">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="96e30-1327">Se ha agregado listxattr para Python (alvent 385)</span><span class="sxs-lookup"><span data-stu-id="96e30-1327">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="96e30-1328">Correcciones y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-1328">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="96e30-1329">Compatibilidad con syscall</span><span class="sxs-lookup"><span data-stu-id="96e30-1329">Syscall Support</span></span>
-   <span data-ttu-id="96e30-1330">A continuación se muestra una lista de llamadas syscall nuevos o mejorados que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="96e30-1330">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="96e30-1331">Los llamadas syscall de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="96e30-1331">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="96e30-1332">Compilación 14361</span><span class="sxs-lookup"><span data-stu-id="96e30-1332">Build 14361</span></span>
<span data-ttu-id="96e30-1333">Para obtener información general sobre Windows sobre la compilación 14361, visite el [blog de Windows](https://aka.ms/wip14361).</span><span class="sxs-lookup"><span data-stu-id="96e30-1333">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="96e30-1334">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-1334">Fixed</span></span>
- <span data-ttu-id="96e30-1335">DrvFs ahora distingue entre mayúsculas y minúsculas cuando se ejecuta en bash en Ubuntu en Windows.</span><span class="sxs-lookup"><span data-stu-id="96e30-1335">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="96e30-1336">Los usuarios pueden Case. txt y CASE. TXT en sus unidades de/mnt/c</span><span class="sxs-lookup"><span data-stu-id="96e30-1336">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="96e30-1337">La distinción de mayúsculas y minúsculas solo se admite en bash en Ubuntu en Windows.</span><span class="sxs-lookup"><span data-stu-id="96e30-1337">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="96e30-1338">Cuando esté fuera de Bash, NTFS notificará los archivos correctamente, pero puede producirse un comportamiento inesperado que interactúe con los archivos de Windows.</span><span class="sxs-lookup"><span data-stu-id="96e30-1338">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="96e30-1339">La raíz de cada volumen (es decir,/mnt/c) no distingue entre mayúsculas y minúsculas</span><span class="sxs-lookup"><span data-stu-id="96e30-1339">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="96e30-1340">Puede encontrar más información sobre el control de estos archivos en Windows [aquí](https://support.microsoft.com/en-us/kb/100625).</span><span class="sxs-lookup"><span data-stu-id="96e30-1340">More information on handling these files in Windows can be found [here](https://support.microsoft.com/en-us/kb/100625).</span></span>
- <span data-ttu-id="96e30-1341">Compatibilidad con PTY/TTY considerablemente mejorada.</span><span class="sxs-lookup"><span data-stu-id="96e30-1341">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="96e30-1342">Ahora se admiten aplicaciones como TMUX (alvent #40)</span><span class="sxs-lookup"><span data-stu-id="96e30-1342">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="96e30-1343">Se corrigió el problema de instalación de las cuentas de usuario que no siempre se han creado</span><span class="sxs-lookup"><span data-stu-id="96e30-1343">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="96e30-1344">Estructura de argumentos de línea de comandos optimizada que permite una lista de argumentos extremadamente larga.</span><span class="sxs-lookup"><span data-stu-id="96e30-1344">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="96e30-1345">(ALVENT #153)</span><span class="sxs-lookup"><span data-stu-id="96e30-1345">(GH #153)</span></span>
- <span data-ttu-id="96e30-1346">Ahora puede eliminar y chmod archivos READ_ONLY de DrvFs</span><span class="sxs-lookup"><span data-stu-id="96e30-1346">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="96e30-1347">Se corrigieron algunos casos en los que el terminal se bloquea en la desconexión (alvent #43)</span><span class="sxs-lookup"><span data-stu-id="96e30-1347">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="96e30-1348">chmod y chown ahora funcionan en dispositivos TTY</span><span class="sxs-lookup"><span data-stu-id="96e30-1348">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="96e30-1349">Permitir la conexión a 0.0.0.0 y:: como localhost (alvent #388)</span><span class="sxs-lookup"><span data-stu-id="96e30-1349">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="96e30-1350">Sendmsg/recvmsg ahora administra una longitud de vector de e/s de > 1 (#376 parciales)</span><span class="sxs-lookup"><span data-stu-id="96e30-1350">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="96e30-1351">Los usuarios ahora pueden dejar de participar en el archivo de hosts generados automáticamente (alvent #398)</span><span class="sxs-lookup"><span data-stu-id="96e30-1351">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="96e30-1352">Coincidencia automática de la configuración regional de Linux con la configuración regional de NT durante la instalación (alvent #11)</span><span class="sxs-lookup"><span data-stu-id="96e30-1352">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="96e30-1353">Se ha agregado el archivo/proc/sys/vm/swappiness (alvent #306)</span><span class="sxs-lookup"><span data-stu-id="96e30-1353">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="96e30-1354">strace ahora se cierra correctamente</span><span class="sxs-lookup"><span data-stu-id="96e30-1354">strace now exits correctly</span></span>
- <span data-ttu-id="96e30-1355">Permitir que las canalizaciones se vuelvan a abrir a través de/proc/Self/FD (alvent #222)</span><span class="sxs-lookup"><span data-stu-id="96e30-1355">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="96e30-1356">Ocultar directorios en%LOCALAPPDATA%\lxss de DrvFs (alvent #270)</span><span class="sxs-lookup"><span data-stu-id="96e30-1356">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="96e30-1357">Mejor control de Bash. exe ~.</span><span class="sxs-lookup"><span data-stu-id="96e30-1357">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="96e30-1358">Ahora se admiten comandos como "Bash ~-c LS" (alvent #467)</span><span class="sxs-lookup"><span data-stu-id="96e30-1358">Commands like “bash ~ -c ls” now supported (GH #467)</span></span>
- <span data-ttu-id="96e30-1359">Ahora, los sockets notifican a epoll Read disponibles durante el cierre (alvent #271)</span><span class="sxs-lookup"><span data-stu-id="96e30-1359">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="96e30-1360">lxrun/Uninstall mejora el trabajo de eliminación de archivos y carpetas</span><span class="sxs-lookup"><span data-stu-id="96e30-1360">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="96e30-1361">Se corrigió PS-f (alvent #246)</span><span class="sxs-lookup"><span data-stu-id="96e30-1361">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="96e30-1362">Compatibilidad mejorada con aplicaciones X11 como xEmacs (alvent #481)</span><span class="sxs-lookup"><span data-stu-id="96e30-1362">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="96e30-1363">Se ha actualizado el tamaño inicial de la pila de subprocesos para que coincida con la configuración predeterminada de Ubuntu y se notifica el tamaño correctamente a get_rlimit syscall (alvent #172, #258)</span><span class="sxs-lookup"><span data-stu-id="96e30-1363">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="96e30-1364">Informes mejorados de nombres de imagen de proceso pico (por ejemplo, para auditoría)</span><span class="sxs-lookup"><span data-stu-id="96e30-1364">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="96e30-1365">Comando implementado/proc/mountinfo para DF</span><span class="sxs-lookup"><span data-stu-id="96e30-1365">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="96e30-1366">Código de error de symlink fijo para el nombre secundario.</span><span class="sxs-lookup"><span data-stu-id="96e30-1366">Fixed symlink error code for child name .</span></span> <span data-ttu-id="96e30-1367">y.</span><span class="sxs-lookup"><span data-stu-id="96e30-1367">and ..</span></span>
- <span data-ttu-id="96e30-1368">Mejoras correcciones y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-1368">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="96e30-1369">Compatibilidad con syscall</span><span class="sxs-lookup"><span data-stu-id="96e30-1369">Syscall Support</span></span>
<span data-ttu-id="96e30-1370">A continuación se muestra una lista de llamadas syscall nuevos o mejorados que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="96e30-1370">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="96e30-1371">Los llamadas syscall de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="96e30-1371">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="96e30-1372">Compilación 14352</span><span class="sxs-lookup"><span data-stu-id="96e30-1372">Build 14352</span></span>
<span data-ttu-id="96e30-1373">Para obtener información general sobre Windows sobre la compilación 14352, visite el [blog de Windows](https://aka.ms/wip14352).</span><span class="sxs-lookup"><span data-stu-id="96e30-1373">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="96e30-1374">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-1374">Fixed</span></span>
- <span data-ttu-id="96e30-1375">Se corrigió un problema en el que los archivos grandes no se descargaron o se crearon correctamente.</span><span class="sxs-lookup"><span data-stu-id="96e30-1375">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="96e30-1376">Esto debe desbloquear NPM y otros escenarios (alvent #3, alvent #313)</span><span class="sxs-lookup"><span data-stu-id="96e30-1376">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="96e30-1377">Se quitaron algunas instancias en las que los sockets no responden</span><span class="sxs-lookup"><span data-stu-id="96e30-1377">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="96e30-1378">Se corrigieron algunos errores de ptrace</span><span class="sxs-lookup"><span data-stu-id="96e30-1378">Corrected some ptrace errors</span></span>
- <span data-ttu-id="96e30-1379">Problema corregido con WSL que permite nombres de archivo de más de 255 caracteres</span><span class="sxs-lookup"><span data-stu-id="96e30-1379">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="96e30-1380">Compatibilidad mejorada para caracteres que no están en inglés</span><span class="sxs-lookup"><span data-stu-id="96e30-1380">Improved support for non-English characters</span></span>
- <span data-ttu-id="96e30-1381">Agregar datos de zona horaria de Windows actuales y establecer como valores predeterminados</span><span class="sxs-lookup"><span data-stu-id="96e30-1381">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="96e30-1382">ID. de dispositivo único para cada punto de montaje (corrección de JRE – alvent #49)</span><span class="sxs-lookup"><span data-stu-id="96e30-1382">Unique device id’s for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="96e30-1383">Corregir el problema con las rutas de acceso que contienen "."</span><span class="sxs-lookup"><span data-stu-id="96e30-1383">Correct issue with paths containing “.”</span></span> <span data-ttu-id="96e30-1384">y ".."</span><span class="sxs-lookup"><span data-stu-id="96e30-1384">and “..”</span></span>
- <span data-ttu-id="96e30-1385">Compatibilidad con FIFO agregada (alvent #71)</span><span class="sxs-lookup"><span data-stu-id="96e30-1385">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="96e30-1386">Formato actualizado de resolv. conf para que coincida con el formato Ubuntu nativo</span><span class="sxs-lookup"><span data-stu-id="96e30-1386">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="96e30-1387">Algunas limpiezas de procfs</span><span class="sxs-lookup"><span data-stu-id="96e30-1387">Some procfs cleanup</span></span>
- <span data-ttu-id="96e30-1388">Habilitación del ping para consolas de administrador (alvent #18)</span><span class="sxs-lookup"><span data-stu-id="96e30-1388">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="96e30-1389">Compatibilidad con syscall</span><span class="sxs-lookup"><span data-stu-id="96e30-1389">Syscall Support</span></span>
<span data-ttu-id="96e30-1390">A continuación se muestra una lista de llamadas syscall nuevos o mejorados que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="96e30-1390">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="96e30-1391">Los llamadas syscall de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="96e30-1391">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="96e30-1392">Compilación 14342</span><span class="sxs-lookup"><span data-stu-id="96e30-1392">Build 14342</span></span>
<span data-ttu-id="96e30-1393">Para obtener información general sobre Windows sobre la compilación 14342 el [blog de Windows](https://aka.ms/wip14342).</span><span class="sxs-lookup"><span data-stu-id="96e30-1393">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="96e30-1394">Puede encontrar información sobre VolFs y DriveFs en el [blog de WSL](https://blogs.msdn.microsoft.com/wsl).</span><span class="sxs-lookup"><span data-stu-id="96e30-1394">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="96e30-1395">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-1395">Fixed</span></span>
- <span data-ttu-id="96e30-1396">Se corrigió el problema de instalación cuando el usuario de Windows tenía caracteres Unicode en el nombre de usuario</span><span class="sxs-lookup"><span data-stu-id="96e30-1396">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="96e30-1397">La solución de udev de actualización apt-get en las preguntas más frecuentes se proporciona ahora de forma predeterminada en la primera ejecución.</span><span class="sxs-lookup"><span data-stu-id="96e30-1397">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="96e30-1398">Vínculos simbólicos habilitados en<drive>directorios DriveFs (/mnt/)</span><span class="sxs-lookup"><span data-stu-id="96e30-1398">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="96e30-1399">Los vínculos simbólicos funcionan ahora entre DriveFs y VolFs</span><span class="sxs-lookup"><span data-stu-id="96e30-1399">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="96e30-1400">Problema de análisis de ruta de acceso de nivel superior solucionado: LS.//funcionará ahora como se esperaba</span><span class="sxs-lookup"><span data-stu-id="96e30-1400">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="96e30-1401">la instalación de NPM en DriveFs y las opciones-g ahora funcionan</span><span class="sxs-lookup"><span data-stu-id="96e30-1401">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="96e30-1402">Se corrigió un problema que impide que se inicie el servidor PHP</span><span class="sxs-lookup"><span data-stu-id="96e30-1402">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="96e30-1403">Valores de entorno predeterminados actualizados, como $PATH para que coincidan con Ubuntu nativo</span><span class="sxs-lookup"><span data-stu-id="96e30-1403">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="96e30-1404">Se ha agregado una tarea de mantenimiento semanal en Windows para actualizar la caché de paquetes apt</span><span class="sxs-lookup"><span data-stu-id="96e30-1404">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="96e30-1405">Problema corregido con la validación de encabezado de ELF, WSL ahora es compatible con todas las opciones de Melkor</span><span class="sxs-lookup"><span data-stu-id="96e30-1405">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="96e30-1406">El shell de zsh es funcional</span><span class="sxs-lookup"><span data-stu-id="96e30-1406">Zsh shell is functional</span></span>
- <span data-ttu-id="96e30-1407">Ahora se admiten los binarios de go precompilados</span><span class="sxs-lookup"><span data-stu-id="96e30-1407">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="96e30-1408">Preguntar en bash. exe la primera ejecución ahora está localizada correctamente</span><span class="sxs-lookup"><span data-stu-id="96e30-1408">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="96e30-1409">/proc/meminfo Now devuelve la información correcta</span><span class="sxs-lookup"><span data-stu-id="96e30-1409">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="96e30-1410">Sockets admitidos ahora en VFS</span><span class="sxs-lookup"><span data-stu-id="96e30-1410">Sockets now supported in VFS</span></span>
- <span data-ttu-id="96e30-1411">/dev ahora montado como tempfs</span><span class="sxs-lookup"><span data-stu-id="96e30-1411">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="96e30-1412">Ahora se admite FIFO</span><span class="sxs-lookup"><span data-stu-id="96e30-1412">Fifo now supported</span></span>
- <span data-ttu-id="96e30-1413">Los sistemas de varios núcleos ahora se muestran correctamente en/proc/cpuinfo</span><span class="sxs-lookup"><span data-stu-id="96e30-1413">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="96e30-1414">Mejoras adicionales y mensajes de error que se descargan durante la primera ejecución</span><span class="sxs-lookup"><span data-stu-id="96e30-1414">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="96e30-1415">Mejoras de syscall y correcciones.</span><span class="sxs-lookup"><span data-stu-id="96e30-1415">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="96e30-1416">Lista de syscall admitida a continuación.</span><span class="sxs-lookup"><span data-stu-id="96e30-1416">Supported syscall list below.</span></span>
- <span data-ttu-id="96e30-1417">Correcciones y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-1417">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="96e30-1418">Problemas conocidos</span><span class="sxs-lookup"><span data-stu-id="96e30-1418">Known Issues</span></span>
- <span data-ttu-id="96e30-1419">No se resuelve '.. '</span><span class="sxs-lookup"><span data-stu-id="96e30-1419">Not resolving ‘..’</span></span> <span data-ttu-id="96e30-1420">correctamente en DriveFs en algunos casos</span><span class="sxs-lookup"><span data-stu-id="96e30-1420">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="96e30-1421">Compatibilidad con syscall</span><span class="sxs-lookup"><span data-stu-id="96e30-1421">Syscall Support</span></span>
<span data-ttu-id="96e30-1422">A continuación se muestra una lista de llamadas syscall nuevos o mejorados que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="96e30-1422">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="96e30-1423">Los llamadas syscall de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="96e30-1423">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FCHOWNAT`<br/>
`GETEUID`<br/>
`GETGID`<br/>
`GETRESUID`<br/>
`GETXATTR`<br/>
`PTRACE`<br/>
`SETGID`<br/>
`SETGROUPS`<br/>
`SETHOSTNAME`<br/>
`SETXATTR`<br/>
<br/>

## <a name="build-14332"></a><span data-ttu-id="96e30-1424">Compilación 14332</span><span class="sxs-lookup"><span data-stu-id="96e30-1424">Build 14332</span></span>

<span data-ttu-id="96e30-1425">Para obtener información general sobre Windows sobre la compilación 14332, visite el [blog de Windows](https://aka.ms/wip14332).</span><span class="sxs-lookup"><span data-stu-id="96e30-1425">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="96e30-1426">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-1426">Fixed</span></span>
- <span data-ttu-id="96e30-1427">Mejor generación de resolv. conf, incluida la priorización de entradas DNS</span><span class="sxs-lookup"><span data-stu-id="96e30-1427">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="96e30-1428">Problema con el traslado de archivos y directorios entre las unidades de/mnt y no/mnt</span><span class="sxs-lookup"><span data-stu-id="96e30-1428">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="96e30-1429">Los archivos tar ahora se pueden crear con vínculos simbólicos</span><span class="sxs-lookup"><span data-stu-id="96e30-1429">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="96e30-1430">Se agregó el directorio/Run/Lock predeterminado en la creación de la instancia</span><span class="sxs-lookup"><span data-stu-id="96e30-1430">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="96e30-1431">Actualice/dev/null para que devuelva la información de estadísticas correcta</span><span class="sxs-lookup"><span data-stu-id="96e30-1431">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="96e30-1432">Errores adicionales al descargar durante la primera ejecución</span><span class="sxs-lookup"><span data-stu-id="96e30-1432">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="96e30-1433">Mejoras de syscall y correcciones.</span><span class="sxs-lookup"><span data-stu-id="96e30-1433">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="96e30-1434">Lista de syscall admitida a continuación.</span><span class="sxs-lookup"><span data-stu-id="96e30-1434">Supported syscall list below.</span></span>
- <span data-ttu-id="96e30-1435">Mejoras correcciones y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-1435">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="96e30-1436">Compatibilidad con syscall</span><span class="sxs-lookup"><span data-stu-id="96e30-1436">Syscall Support</span></span>
<span data-ttu-id="96e30-1437">A continuación se muestra el nuevo syscall que tiene alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="96e30-1437">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="96e30-1438">El syscall de esta lista se admite en al menos un escenario, pero es posible que no tenga todos los parámetros admitidos en este momento.</span><span class="sxs-lookup"><span data-stu-id="96e30-1438">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="96e30-1439">Compilación 14328</span><span class="sxs-lookup"><span data-stu-id="96e30-1439">Build 14328</span></span>

<span data-ttu-id="96e30-1440">Para obtener información general sobre Windows sobre la compilación 14332, visite el [blog de Windows](https://aka.ms/wip14328).</span><span class="sxs-lookup"><span data-stu-id="96e30-1440">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="96e30-1441">Nuevas características</span><span class="sxs-lookup"><span data-stu-id="96e30-1441">New Features</span></span>
* <span data-ttu-id="96e30-1442">Ahora admite usuarios de Linux.</span><span class="sxs-lookup"><span data-stu-id="96e30-1442">Now support Linux users.</span></span>  <span data-ttu-id="96e30-1443">Al instalar bash en Ubuntu en Windows, se solicitará la creación de un usuario de Linux.</span><span class="sxs-lookup"><span data-stu-id="96e30-1443">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="96e30-1444">Para obtener más información, visite https://aka.ms/wslusers</span><span class="sxs-lookup"><span data-stu-id="96e30-1444">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="96e30-1445">El nombre de host ahora está establecido en el nombre del equipo de Windows, no más@localhost</span><span class="sxs-lookup"><span data-stu-id="96e30-1445">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="96e30-1446">Para obtener más información sobre la compilación 14328, visite: https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="96e30-1446">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="96e30-1447">Corregido</span><span class="sxs-lookup"><span data-stu-id="96e30-1447">Fixed</span></span>
* <span data-ttu-id="96e30-1448">Mejoras de symlink para archivos<drive> no/mnt/</span><span class="sxs-lookup"><span data-stu-id="96e30-1448">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="96e30-1449">la instalación de NPM funciona ahora</span><span class="sxs-lookup"><span data-stu-id="96e30-1449">npm install now works</span></span>
    * <span data-ttu-id="96e30-1450">JDK/JRE ahora se instala mediante las instrucciones que se encuentran [aquí](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span><span class="sxs-lookup"><span data-stu-id="96e30-1450">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="96e30-1451">problema conocido: los vínculos simbólicos no funcionan para los montajes de Windows.</span><span class="sxs-lookup"><span data-stu-id="96e30-1451">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="96e30-1452">La funcionalidad estará disponible en una compilación posterior</span><span class="sxs-lookup"><span data-stu-id="96e30-1452">Functionality will be available in a later build</span></span>
* <span data-ttu-id="96e30-1453">Top y htop ahora se muestran</span><span class="sxs-lookup"><span data-stu-id="96e30-1453">top and htop now display</span></span>
* <span data-ttu-id="96e30-1454">Mensajes de error adicionales para algunos errores de instalación</span><span class="sxs-lookup"><span data-stu-id="96e30-1454">Additional error messages for some install failures</span></span>
* <span data-ttu-id="96e30-1455">Mejoras de syscall y correcciones.</span><span class="sxs-lookup"><span data-stu-id="96e30-1455">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="96e30-1456">Lista de syscall admitida a continuación.</span><span class="sxs-lookup"><span data-stu-id="96e30-1456">Supported syscall list below.</span></span>
* <span data-ttu-id="96e30-1457">Mejoras correcciones y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="96e30-1457">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="96e30-1458">Compatibilidad con syscall</span><span class="sxs-lookup"><span data-stu-id="96e30-1458">Syscall Support</span></span>
<span data-ttu-id="96e30-1459">A continuación se muestra una lista de llamadas syscall que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="96e30-1459">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="96e30-1460">Llamadas syscall en esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="96e30-1460">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`ACCEPT`<br/>
`ACCEPT4`<br/>
`ACCESS`<br/>
`ALARM`<br/>
`ARCH_PRCTL`<br/>
`BIND`<br/>
`BRK`<br/>
`CAPGET`<br/>
`CAPSET`<br/>
`CHDIR`<br/>
`CHMOD`<br/>
`CHOWN`<br/>
`CLOCK_GETRES`<br/>
`CLOCK_GETTIME`<br/>
`CLOCK_NANOSLEEP`<br/>
`CLONE`<br/>
`CLOSE`<br/>
`CONNECT`<br/>
`CREAT`<br/>
`DUP`<br/>
`DUP2`<br/>
`DUP3`<br/>
`EPOLL_CREATE`<br/>
`EPOLL_CREATE1`<br/>
`EPOLL_CTL`<br/>
`EPOLL_WAIT`<br/>
`EVENTFD`<br/>
`EVENTFD2`<br/>
`EXECVE`<br/>
`EXIT`<br/>
`EXIT_GROUP`<br/>
`FACCESSAT`<br/>
`FADVISE64`<br/>
`FCHDIR`<br/>
`FCHMOD`<br/>
`FCHMODAT`<br/>
`FCHOWN`<br/>
`FCHOWNAT`<br/>
`FCNTL64`<br/>
`FDATASYNC`<br/>
`FLOCK`<br/>
`FORK`<br/>
`FSETXATTR`<br/>
`FSTAT64`<br/>
`FSTATAT64`<br/>
`FSTATFS64`<br/>
`FSYNC`<br/>
`FTRUNCATE`<br/>
`FTRUNCATE64`<br/>
`FUTEX`<br/>
`GETCPU`<br/>
`GETCWD`<br/>
`GETDENTS`<br/>
`GETDENTS64`<br/>
`GETEGID`<br/>
`GETEGID16`<br/>
`GETEUID`<br/>
`GETEUID16`<br/>
`GETGID`<br/>
`GETGID16`<br/>
`GETGROUPS`<br/>
`GETPEERNAME`<br/>
`GETPGID`<br/>
`GETPGRP`<br/>
`GETPID`<br/>
`GETPPID`<br/>
`GETPRIORITY`<br/>
`GETRESGID`<br/>
`GETRESGID16`<br/>
`GETRESUID`<br/>
`GETRESUID16`<br/>
`GETRLIMIT`<br/>
`GETRUSAGE`<br/>
`GETSID`<br/>
`GETSOCKNAME`<br/>
`GETSOCKOPT`<br/>
`GETTID`<br/>
`GETTIMEOFDAY`<br/>
`GETUID`<br/>
`GETUID16`<br/>
`GETXATTR`<br/>
`GET_ROBUST_LIST`<br/>
`GET_THREAD_AREA`<br/>
`INOTIFY_ADD_WATCH`<br/>
`INOTIFY_INIT`<br/>
`INOTIFY_RM_WATCH`<br/>
`IOCTL`<br/>
`IOPRIO_GET`<br/>
`IOPRIO_SET`<br/>
`KEYCTL`<br/>
`KILL`<br/>
`LCHOWN`<br/>
`LINK`<br/>
`LINKAT`<br/>
`LISTEN`<br/>
`LLSEEK`<br/>
`LSEEK`<br/>
`LSTAT64`<br/>
`MADVISE`<br/>
`MKDIR`<br/>
`MKDIRAT`<br/>
`MKNOD`<br/>
`MLOCK`<br/>
`MMAP`<br/>
`MMAP2`<br/>
`MOUNT`<br/>
`MPROTECT`<br/>
`MREMAP`<br/>
`MSYNC`<br/>
`MUNLOCK`<br/>
`MUNMAP`<br/>
`NANOSLEEP`<br/>
`NEWUNAME`<br/>
`OPEN`<br/>
`OPENAT`<br/>
`PAUSE`<br/>
`PERF_EVENT_OPEN`<br/>
`PERSONALITY`<br/>
`PIPE`<br/>
`PIPE2`<br/>
`POLL`<br/>
`PPOLL`<br/>
`PRCTL`<br/>
`PREAD64`<br/>
`PROCESS_VM_READV`<br/>
`PROCESS_VM_WRITEV`<br/>
`PSELECT6`<br/>
`PTRACE`<br/>
`PWRITE64`<br/>
`READ`<br/>
`READLINK`<br/>
`READV`<br/>
`REBOOT`<br/>
`RECV`<br/>
`RECVFROM`<br/>
`RECVMSG`<br/>
`RENAME`<br/>
`RMDIR`<br/>
`RT_SIGACTION`<br/>
`RT_SIGPENDING`<br/>
`RT_SIGPROCMASK`<br/>
`RT_SIGRETURN`<br/>
`RT_SIGSUSPEND`<br/>
`RT_SIGTIMEDWAIT`<br/>
`SCHED_GETAFFINITY`<br/>
`SCHED_GETPARAM`<br/>
`SCHED_GETSCHEDULER`<br/>
`SCHED_GET_PRIORITY_MAX`<br/>
`SCHED_GET_PRIORITY_MIN`<br/>
`SCHED_SETAFFINITY`<br/>
`SCHED_SETPARAM`<br/>
`SCHED_SETSCHEDULER`<br/>
`SCHED_YIELD`<br/>
`SELECT`<br/>
`SEND`<br/>
`SENDMMSG`<br/>
`SENDMSG`<br/>
`SENDTO`<br/>
`SETDOMAINNAME`<br/>
`SETGID`<br/>
`SETGROUPS`<br/>
`SETHOSTNAME`<br/>
`SETITIMER`<br/>
`SETPGID`<br/>
`SETPRIORITY`<br/>
`SETREGID`<br/>
`SETRESGID`<br/>
`SETRESUID`<br/>
`SETREUID`<br/>
`SETRLIMIT`<br/>
`SETSID`<br/>
`SETSOCKOPT`<br/>
`SETTIMEOFDAY`<br/>
`SETUID`<br/>
`SETXATTR`<br/>
`SET_ROBUST_LIST`<br/>
`SET_THREAD_AREA`<br/>
`SET_TID_ADDRESS`<br/>
`SHUTDOWN`<br/>
`SIGACTION`<br/>
`SIGALTSTACK`<br/>
`SIGPENDING`<br/>
`SIGPROCMASK`<br/>
`SIGRETURN`<br/>
`SIGSUSPEND`<br/>
`SOCKET`<br/>
`SOCKETCALL`<br/>
`SOCKETPAIR`<br/>
`SPLICE`<br/>
`STAT64`<br/>
`STATFS64`<br/>
`SYMLINK`<br/>
`SYMLINKAT`<br/>
`SYNC`<br/>
`SYSINFO`<br/>
`TEE`<br/>
`TGKILL`<br/>
`TIME`<br/>
`TIMERFD_CREATE`<br/>
`TIMERFD_GETTIME`<br/>
`TIMERFD_SETTIME`<br/>
`TIMES`<br/>
`TKILL`<br/>
`TRUNCATE`<br/>
`TRUNCATE64`<br/>
`UMASK`<br/>
`UMOUNT`<br/>
`UMOUNT2`<br/>
`UNLINK`<br/>
`UNLINKAT`<br/>
`UNSHARE`<br/>
`UTIME`<br/>
`UTIMENSAT`<br/>
`UTIMES`<br/>
`VFORK`<br/>
`WAIT4`<br/>
`WAITPID`<br/>
`WRITE`<br/>
`WRITEV`<br/>
