---
title: Notas de la versión para el subsistema de Windows para Linux
description: Notas de la versión para el subsistema de Windows para Linux.  Se actualiza semanalmente.
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, windowssubsystem, ubuntu
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.openlocfilehash: 3eee7ff6d1f8302e98cde84fccabf5d9113c83f2
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063633"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="058f0-105">Notas de la versión para el subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="058f0-105">Release Notes for Windows Subsystem for Linux</span></span>

## <a name="build-18342"></a><span data-ttu-id="058f0-106">Compilación 18342</span><span class="sxs-lookup"><span data-stu-id="058f0-106">Build 18342</span></span>
<span data-ttu-id="058f0-107">Para Windows general, visite información sobre las compilación 18342 el [blog Windows](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span><span class="sxs-lookup"><span data-stu-id="058f0-107">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="058f0-108">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-108">WSL</span></span>
* <span data-ttu-id="058f0-109">Hemos agregado la capacidad de los usuarios tener acceso a los archivos de Linux en una distribución de WSL desde Windows.</span><span class="sxs-lookup"><span data-stu-id="058f0-109">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="058f0-110">Estos archivos pueden obtenerse a través de la línea de comandos, además de aplicaciones de Windows, como el Explorador de archivos, VSCode, etc. puede interactuar con estos archivos.</span><span class="sxs-lookup"><span data-stu-id="058f0-110">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="058f0-111">Acceder a los archivos, vaya a \\ \\wsl$\\< distro_name >, o ver una lista de distribuciones en ejecución, vaya a \\ \\wsl$</span><span class="sxs-lookup"><span data-stu-id="058f0-111">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="058f0-112">Agregar etiquetas de información adicionales de CPU y corregir los valores de Cpus_allowed [_lista] [GH 2234]</span><span class="sxs-lookup"><span data-stu-id="058f0-112">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="058f0-113">Admite la ejecución del subproceso que no sean líder [GH 3800]</span><span class="sxs-lookup"><span data-stu-id="058f0-113">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="058f0-114">Tratar errores de actualización de configuración como recuperable [GH 3785]</span><span class="sxs-lookup"><span data-stu-id="058f0-114">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="058f0-115">Actualizar binfmt para controlar correctamente los desplazamientos [GH 3768]</span><span class="sxs-lookup"><span data-stu-id="058f0-115">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="058f0-116">Habilitar asignación las unidades de red para planear 9 [GH 3854]</span><span class="sxs-lookup"><span data-stu-id="058f0-116">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="058f0-117">Linux -> el soporte técnico de Windows y Linux -> traducción de la ruta de acceso de Windows para montajes de enlace</span><span class="sxs-lookup"><span data-stu-id="058f0-117">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="058f0-118">Crear secciones de solo lectura para las asignaciones en los archivos abiertos de solo lectura</span><span class="sxs-lookup"><span data-stu-id="058f0-118">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="058f0-119">Compilación 18334</span><span class="sxs-lookup"><span data-stu-id="058f0-119">Build 18334</span></span>
<span data-ttu-id="058f0-120">Para Windows general, visite información sobre las compilación 18334 el [blog Windows](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span><span class="sxs-lookup"><span data-stu-id="058f0-120">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="058f0-121">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-121">WSL</span></span>
* <span data-ttu-id="058f0-122">Diseñar la forma en que la zona horaria de Windows se asigna a una zona horaria de Linux [GH 3747]</span><span class="sxs-lookup"><span data-stu-id="058f0-122">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="058f0-123">Corregir las pérdidas de memoria y agregar nuevas funciones de conversión de cadena [GH 3746]</span><span class="sxs-lookup"><span data-stu-id="058f0-123">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="058f0-124">SIGCONT en un threadgroup sin subprocesos es una operación inefectiva [GH 3741]</span><span class="sxs-lookup"><span data-stu-id="058f0-124">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="058f0-125">Mostrar correctamente los descriptores de archivo de socket y epoll en /proc/self/fd</span><span class="sxs-lookup"><span data-stu-id="058f0-125">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="058f0-126">Compilación 18305</span><span class="sxs-lookup"><span data-stu-id="058f0-126">Build 18305</span></span>
<span data-ttu-id="058f0-127">Para Windows general, visite información sobre las compilación 18305 el [blog Windows](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span><span class="sxs-lookup"><span data-stu-id="058f0-127">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="058f0-128">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-128">WSL</span></span>
* <span data-ttu-id="058f0-129">pthreads perder el acceso a los archivos cuando el subproceso principal finaliza [GH 3589]</span><span class="sxs-lookup"><span data-stu-id="058f0-129">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="058f0-130">TIOCSCTTY debe omitir el parámetro "force" a menos que sea necesario [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="058f0-130">TIOCSCTTY should ignore the “force” parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="058f0-131">mejoras de la línea de comandos de wsl.exe y adición de importación / exportación de funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="058f0-131">wsl.exe command line improvements and addition of import / export functionality.</span></span>
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

## <a name="build-18277"></a><span data-ttu-id="058f0-132">Compilación 18277</span><span class="sxs-lookup"><span data-stu-id="058f0-132">Build 18277</span></span>
<span data-ttu-id="058f0-133">Para Windows general, visite información sobre las compilación 18277 el [blog Windows](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span><span class="sxs-lookup"><span data-stu-id="058f0-133">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="058f0-134">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-134">WSL</span></span>
* <span data-ttu-id="058f0-135">Corregir el error "no se admite dicha interfaz" introducido en la compilación 18272 [GH 3645]</span><span class="sxs-lookup"><span data-stu-id="058f0-135">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="058f0-136">Omitir el indicador MNT_FORCE para umount syscall [GH 3605]</span><span class="sxs-lookup"><span data-stu-id="058f0-136">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="058f0-137">Cambie la interoperabilidad WSL para usar la API CreatePseudoConsole oficial</span><span class="sxs-lookup"><span data-stu-id="058f0-137">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="058f0-138">No mantener ningún valor de tiempo de espera cuando se reinicia FUTEX_WAIT</span><span class="sxs-lookup"><span data-stu-id="058f0-138">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="058f0-139">Compilación 18272</span><span class="sxs-lookup"><span data-stu-id="058f0-139">Build 18272</span></span>
<span data-ttu-id="058f0-140">Para Windows general, visite información sobre las compilación 18272 el [blog Windows](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span><span class="sxs-lookup"><span data-stu-id="058f0-140">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="058f0-141">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-141">WSL</span></span>
* <span data-ttu-id="058f0-142">**ADVERTENCIA:** Hay un problema en esta compilación que hace WSL no funciona.</span><span class="sxs-lookup"><span data-stu-id="058f0-142">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="058f0-143">Al intentar iniciar la distribución verá un error "No se admite dicha interfaz".</span><span class="sxs-lookup"><span data-stu-id="058f0-143">When trying to launch your distribution you will see a “No such interface supported” error.</span></span> <span data-ttu-id="058f0-144">El problema se ha corregido y estará en la compilación de Insider rápida de la próxima semana.</span><span class="sxs-lookup"><span data-stu-id="058f0-144">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="058f0-145">Si ha instalado esta compilación puede revertir a la compilación anterior de Windows mediante "Ir a la versión anterior de Windows 10" en Configuración -> actualización de & seguridad -> recuperación.</span><span class="sxs-lookup"><span data-stu-id="058f0-145">If you've installed this build you can roll back to the previous Windows build using “Go back to the previous version of Windows 10” in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="058f0-146">Compilación 18267</span><span class="sxs-lookup"><span data-stu-id="058f0-146">Build 18267</span></span>
<span data-ttu-id="058f0-147">Para Windows general información en la compilación 18267, visite la [blog Windows](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span><span class="sxs-lookup"><span data-stu-id="058f0-147">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="058f0-148">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-148">WSL</span></span>
* <span data-ttu-id="058f0-149">Corregir el problema donde el proceso inerte no puede ser reaped y permanecer indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="058f0-149">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="058f0-150">WslRegisterDistribution se bloquea si el mensaje de error supera la longitud máxima [GH 3592]</span><span class="sxs-lookup"><span data-stu-id="058f0-150">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="058f0-151">Permitir fsync para archivos de solo lectura en DrvFs [GH 3556]</span><span class="sxs-lookup"><span data-stu-id="058f0-151">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="058f0-152">Asegúrese de que existen los directorios /bin y/sbin antes de crear vínculos simbólicos dentro de [GH 3584]</span><span class="sxs-lookup"><span data-stu-id="058f0-152">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="058f0-153">Agregar un mecanismo de tiempo de espera de finalización de instancia para las instancias WSL.</span><span class="sxs-lookup"><span data-stu-id="058f0-153">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="058f0-154">Actualmente, el tiempo de espera se establece en 15 segundos, lo que significa que la instancia cerrará en 15 segundos después de que salga el último proceso WSL.</span><span class="sxs-lookup"><span data-stu-id="058f0-154">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="058f0-155">Para finalizar una distribución de inmediato, use:</span><span class="sxs-lookup"><span data-stu-id="058f0-155">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="058f0-156">Compilar 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="058f0-156">Build 17763 (1809)</span></span>
<span data-ttu-id="058f0-157">Para Windows general, visite información sobre las compilación 17763 el [blog Windows](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span><span class="sxs-lookup"><span data-stu-id="058f0-157">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="058f0-158">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-158">WSL</span></span>
* <span data-ttu-id="058f0-159">Comprobación de permisos de syscall SetPriority demasiado estricto para cambiar la misma prioridad de subproceso [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="058f0-159">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="058f0-160">Garantizar que el tiempo de interrupción no sesgada se usa durante el tiempo de arranque para evitar la devolución de los valores negativos para clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="058f0-160">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="058f0-161">Controlar los vínculos simbólicos en el intérprete WSL binfmt [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="058f0-161">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="058f0-162">Un mejor control de limpieza del descriptor de archivo de threadgroup líder.</span><span class="sxs-lookup"><span data-stu-id="058f0-162">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="058f0-163">Cambiar WSL usar KeQueryInterruptTimePrecise en lugar de KeQueryPerformanceCounter del núcleo para evitar el desbordamiento [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="058f0-163">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="058f0-164">Ptrace adjuntar se puede hacer que el valor devuelto incorrecto de llamadas del sistema [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="058f0-164">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="058f0-165">Revisión relacionada con varios AF_UNIX emite [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="058f0-165">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="058f0-166">Corregir el problema que podría provocar la interoperabilidad WSL para producir un error si el directorio de trabajo actual es menor que 5 caracteres de longitud [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="058f0-166">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="058f0-167">Evitar un retraso segundo errores en las conexiones de bucle invertido para puertos inexistente [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="058f0-167">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="058f0-168">Add /proc/sys/fs/file-max stub file [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="058f0-168">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="058f0-169">Información más precisa del ámbito de IPV6.</span><span class="sxs-lookup"><span data-stu-id="058f0-169">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="058f0-170">Soporte técnico PR_SET_PTRACER [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="058f0-170">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="058f0-171">Sistema de archivos de canalización borrado accidentalmente epoll edge desencadenadas por eventos [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="058f0-171">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="058f0-172">Ejecutable de Win32 iniciada a través de vínculos simbólicos NTFS no respeta el nombre de vínculo simbólico [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="058f0-172">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="058f0-173">Mejorado soporte inerte [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="058f0-173">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="058f0-174">Agregar entradas wsl.conf para controlar el comportamiento de interoperabilidad de Windows [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="058f0-174">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="058f0-175">Corrección de getsockname no siempre devuelve el tipo de familia de socket de UNIX [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="058f0-175">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="058f0-176">Agregar compatibilidad para TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="058f0-176">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="058f0-177">Sockets de no bloqueo en el proceso de conexión deben devolver EAGAIN para intentos de escritura [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="058f0-177">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="058f0-178">Admitir la interoperabilidad en los discos duros virtuales montados [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="058f0-178">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="058f0-179">Corregir el problema en la carpeta raíz [GH 3304] la comprobación de permiso</span><span class="sxs-lookup"><span data-stu-id="058f0-179">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="058f0-180">Compatibilidad limitada para TTY teclado IOCTL KDGKBTYPE, KDGKBMODE y KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="058f0-180">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="058f0-181">Incluso cuando se inicia en segundo plano, deben ejecutar las aplicaciones de interfaz de usuario de Windows.</span><span class="sxs-lookup"><span data-stu-id="058f0-181">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="058f0-182">Agregue la opción -u o--usuario wsl [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="058f0-182">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="058f0-183">Solucionar problemas de inicio WSL cuando se habilita el inicio rápido [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="058f0-183">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="058f0-184">Sockets de UNIX necesitan conservar las credenciales de desconectada del mismo nivel [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="058f0-184">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="058f0-185">Sockets de Unix sin bloqueo presentan indefinidamente EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="058f0-185">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="058f0-186">caso = off es el nuevo drvfs predeterminada montar tipo [GH 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="058f0-186">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="058f0-187">Consulte [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="058f0-187">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="058f0-188">Agregar wslconfig / terminate para detener la ejecución de las distribuciones.</span><span class="sxs-lookup"><span data-stu-id="058f0-188">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="058f0-189">Corregir el problema con el contexto del shell WSL entradas de menú que no administren correctamente las rutas de acceso con espacios.</span><span class="sxs-lookup"><span data-stu-id="058f0-189">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="058f0-190">Exponer entre mayúsculas y minúsculas por directorio como un atributo extendido</span><span class="sxs-lookup"><span data-stu-id="058f0-190">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="058f0-191">ARM64: Emular las operaciones de mantenimiento de caché.</span><span class="sxs-lookup"><span data-stu-id="058f0-191">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="058f0-192">Resolver [dotnet problema](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="058f0-192">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="058f0-193">DrvFs: unescape solo caracteres del intervalo privado que corresponden a un carácter de escape.</span><span class="sxs-lookup"><span data-stu-id="058f0-193">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="058f0-194">Corregir el error de off a uno en la validación de longitud de intérprete de ELF analizador [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="058f0-194">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="058f0-195">Los temporizadores en absoluto con un tiempo en el pasado WSL no activan [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="058f0-195">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="058f0-196">Asegúrese de recién puntos de reanálisis creado se muestran como tal en el directorio primario.</span><span class="sxs-lookup"><span data-stu-id="058f0-196">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="058f0-197">Crear atómicamente directorios distingue mayúsculas de minúsculas en DrvFs.</span><span class="sxs-lookup"><span data-stu-id="058f0-197">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="058f0-198">Se corrigió un problema adicional que podrían devolver operaciones multiproceso ENOENT aunque exista el archivo.</span><span class="sxs-lookup"><span data-stu-id="058f0-198">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="058f0-199">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="058f0-199">[GH 2712]</span></span>
* <span data-ttu-id="058f0-200">WSL fijo iniciar un error cuando se habilita UMCI.</span><span class="sxs-lookup"><span data-stu-id="058f0-200">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="058f0-201">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="058f0-201">[GH 3020]</span></span>
* <span data-ttu-id="058f0-202">Agregar el menú contextual del explorador para iniciar WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="058f0-202">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="058f0-203">Para usar, mantenga presionada la tecla MAYÚS y haga doble clic en una ventana del explorador.</span><span class="sxs-lookup"><span data-stu-id="058f0-203">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="058f0-204">Corregir el comportamiento de no bloqueo del socket de Unix [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="058f0-204">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="058f0-205">Corrección de francesa comando NETLINK notificados en 2026 GH.</span><span class="sxs-lookup"><span data-stu-id="058f0-205">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="058f0-206">Agregar compatibilidad con marcadores de propagación de montaje [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="058f0-206">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="058f0-207">Corregir el problema con truncate que no producen inotify eventos [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="058f0-207">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="058f0-208">Agregue--opción exec para wsl.exe invocar un solo archivo binario sin un shell.</span><span class="sxs-lookup"><span data-stu-id="058f0-208">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="058f0-209">Agregar: opción de distribución para wsl.exe seleccionar una distribución específica.</span><span class="sxs-lookup"><span data-stu-id="058f0-209">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="058f0-210">Compatibilidad limitada con dmesg.</span><span class="sxs-lookup"><span data-stu-id="058f0-210">Limited support for dmesg.</span></span> <span data-ttu-id="058f0-211">Las aplicaciones ahora pueden iniciar en dmesg.</span><span class="sxs-lookup"><span data-stu-id="058f0-211">Applications can now log to dmesg.</span></span> <span data-ttu-id="058f0-212">Controlador WSL registra información limitada a dmesg.</span><span class="sxs-lookup"><span data-stu-id="058f0-212">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="058f0-213">En el futuro, esto puede ampliarse para llevar a cabo otros información/diagnósticos desde el controlador.</span><span class="sxs-lookup"><span data-stu-id="058f0-213">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="058f0-214">Nota: dmesg actualmente se admite a través de la `/dev/kmsg` la interfaz de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="058f0-214">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> `syslog` <span data-ttu-id="058f0-215">interfaz syscall aún no se admite.</span><span class="sxs-lookup"><span data-stu-id="058f0-215">syscall interface is not yet supported.</span></span> <span data-ttu-id="058f0-216">Y, por lo tanto, algunos de los `dmesg` opciones de línea de comandos tales como `-S`, `-C` no funcionan.</span><span class="sxs-lookup"><span data-stu-id="058f0-216">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="058f0-217">Cambiar el gid de forma predeterminada y el modo de dispositivos serie para que coincida con nativo [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="058f0-217">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="058f0-218">DrvFs ahora es compatible con atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="058f0-218">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="058f0-219">Nota: DrvFs tiene algunas limitaciones en el nombre de los atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="058f0-219">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="058f0-220">Algunos caracteres (como '/', ':' y '\*') no están permitidos y extendido los nombres de atributo no distinguen mayúsculas de minúsculas en DrvFs</span><span class="sxs-lookup"><span data-stu-id="058f0-220">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="058f0-221">Compilación 18252 (Saltar adelante)</span><span class="sxs-lookup"><span data-stu-id="058f0-221">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="058f0-222">Para Windows general, visite información sobre las compilación 18252 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span><span class="sxs-lookup"><span data-stu-id="058f0-222">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="058f0-223">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-223">WSL</span></span>
* <span data-ttu-id="058f0-224">Mover los archivos binarios de init y bsdtar lxssmanager dll y a una carpeta de herramientas independientes</span><span class="sxs-lookup"><span data-stu-id="058f0-224">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="058f0-225">Corregir la carrera en torno a cerrar el descriptor de archivo cuando se usa CLONE_FILES</span><span class="sxs-lookup"><span data-stu-id="058f0-225">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="058f0-226">Administrar campos opcionales en /proc/pid/mountinfo al traducir las rutas de acceso DrvFs</span><span class="sxs-lookup"><span data-stu-id="058f0-226">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="058f0-227">Permitir DrvFs mknod se realice correctamente sin compatibilidad con metadatos para S_IFREG</span><span class="sxs-lookup"><span data-stu-id="058f0-227">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="058f0-228">Archivos de solo lectura creados en DrvFs deben tener el atributo de solo lectura establezca [GH 3411]</span><span class="sxs-lookup"><span data-stu-id="058f0-228">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="058f0-229">Agregar aplicación auxiliar /sbin/mount.drvfs para controlar el montaje DrvFs</span><span class="sxs-lookup"><span data-stu-id="058f0-229">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="058f0-230">Use el cambio de nombre POSIX de DrvFs.</span><span class="sxs-lookup"><span data-stu-id="058f0-230">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="058f0-231">Permitir traducción de la ruta de acceso en los volúmenes sin un GUID de volumen.</span><span class="sxs-lookup"><span data-stu-id="058f0-231">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="058f0-232">Compilar 17738 (Fast)</span><span class="sxs-lookup"><span data-stu-id="058f0-232">Build 17738 (Fast)</span></span>
<span data-ttu-id="058f0-233">Para Windows general, visite información sobre las compilación 17738 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span><span class="sxs-lookup"><span data-stu-id="058f0-233">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="058f0-234">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-234">WSL</span></span>
* <span data-ttu-id="058f0-235">Comprobación de permisos de syscall SetPriority demasiado estricto para cambiar la misma prioridad de subproceso [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="058f0-235">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="058f0-236">Garantizar que el tiempo de interrupción no sesgada se usa durante el tiempo de arranque para evitar la devolución de los valores negativos para clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="058f0-236">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="058f0-237">Controlar los vínculos simbólicos en el intérprete WSL binfmt [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="058f0-237">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="058f0-238">Un mejor control de limpieza del descriptor de archivo de threadgroup líder.</span><span class="sxs-lookup"><span data-stu-id="058f0-238">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="058f0-239">Compilar 17728 (Fast)</span><span class="sxs-lookup"><span data-stu-id="058f0-239">Build 17728 (Fast)</span></span>
<span data-ttu-id="058f0-240">Para Windows general, visite información sobre las compilación 17728 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span><span class="sxs-lookup"><span data-stu-id="058f0-240">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="058f0-241">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-241">WSL</span></span>
* <span data-ttu-id="058f0-242">Cambiar WSL usar KeQueryInterruptTimePrecise en lugar de KeQueryPerformanceCounter del núcleo para evitar el desbordamiento [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="058f0-242">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="058f0-243">Ptrace adjuntar se puede hacer que el valor devuelto incorrecto de llamadas del sistema [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="058f0-243">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="058f0-244">Revisión relacionada con un número de AF_UNIX emite [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="058f0-244">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="058f0-245">Corregir el problema que podría provocar la interoperabilidad WSL para producir un error si el directorio de trabajo actual es menor que 5 caracteres de longitud [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="058f0-245">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="058f0-246">Compilación 18204 (Saltar adelante)</span><span class="sxs-lookup"><span data-stu-id="058f0-246">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="058f0-247">Para Windows general, visite información sobre las compilación 18204 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="058f0-247">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="058f0-248">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-248">WSL</span></span>
* <span data-ttu-id="058f0-249">Canalizar inadvertenly filesystem borrar epoll edge desencadenadas por eventos [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="058f0-249">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="058f0-250">Ejecutable de Win32 iniciada a través de vínculos simbólicos NTFS no respeta el nombre de vínculo simbólico [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="058f0-250">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="058f0-251">Compilar 17723 (Fast)</span><span class="sxs-lookup"><span data-stu-id="058f0-251">Build 17723 (Fast)</span></span>
<span data-ttu-id="058f0-252">Para Windows general, visite información sobre las compilación 17723 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="058f0-252">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="058f0-253">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-253">WSL</span></span>
* <span data-ttu-id="058f0-254">Evitar un retraso segundo errores en las conexiones de bucle invertido para puertos inexistente [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="058f0-254">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="058f0-255">Add /proc/sys/fs/file-max stub file [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="058f0-255">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="058f0-256">Información más precisa del ámbito de IPV6.</span><span class="sxs-lookup"><span data-stu-id="058f0-256">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="058f0-257">Soporte técnico PR_SET_PTRACER [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="058f0-257">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="058f0-258">Canalizar inadvertenly filesystem borrar epoll edge desencadenadas por eventos [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="058f0-258">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="058f0-259">Ejecutable de Win32 iniciada a través de vínculos simbólicos NTFS no respeta el nombre de vínculo simbólico [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="058f0-259">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="058f0-260">Compilación 17713</span><span class="sxs-lookup"><span data-stu-id="058f0-260">Build 17713</span></span>
<span data-ttu-id="058f0-261">Para Windows general, visite información sobre las compilación 17713 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span><span class="sxs-lookup"><span data-stu-id="058f0-261">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="058f0-262">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-262">WSL</span></span>
* <span data-ttu-id="058f0-263">Mejorado soporte inerte [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="058f0-263">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="058f0-264">Agregar entradas wsl.conf para controlar el comportamiento de interoperabilidad de Windows [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="058f0-264">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="058f0-265">Corrección de getsockname no siempre devuelve el tipo de familia de socket de UNIX [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="058f0-265">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="058f0-266">Agregar compatibilidad para TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="058f0-266">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="058f0-267">Sockets de no bloqueo en el proceso de conexión deben devolver EAGAIN para intentos de escritura [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="058f0-267">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="058f0-268">Admitir la interoperabilidad en los discos duros virtuales montados [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="058f0-268">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="058f0-269">Corregir el problema en la carpeta raíz [GH 3304] la comprobación de permiso</span><span class="sxs-lookup"><span data-stu-id="058f0-269">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="058f0-270">Compatibilidad limitada para TTY teclado IOCTL KDGKBTYPE, KDGKBMODE y KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="058f0-270">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="058f0-271">Incluso cuando se inicia en segundo plano, deben ejecutar las aplicaciones de interfaz de usuario de Windows.</span><span class="sxs-lookup"><span data-stu-id="058f0-271">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="058f0-272">Compilación 17704</span><span class="sxs-lookup"><span data-stu-id="058f0-272">Build 17704</span></span>
<span data-ttu-id="058f0-273">Para Windows general, visite información sobre las compilación 17704 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span><span class="sxs-lookup"><span data-stu-id="058f0-273">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="058f0-274">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-274">WSL</span></span>
* <span data-ttu-id="058f0-275">Agregue la opción -u o--usuario wsl [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="058f0-275">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="058f0-276">Solucionar problemas de inicio WSL cuando se habilita el inicio rápido [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="058f0-276">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="058f0-277">Sockets de UNIX necesitan conservar las credenciales de desconectada del mismo nivel [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="058f0-277">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="058f0-278">Sockets de Unix sin bloqueo presentan indefinidamente EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="058f0-278">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="058f0-279">caso = off es el nuevo drvfs predeterminada montar tipo [GH 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="058f0-279">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="058f0-280">Consulte [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="058f0-280">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="058f0-281">Agregar wslconfig / terminate para detener la ejecución de las distribuciones.</span><span class="sxs-lookup"><span data-stu-id="058f0-281">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="058f0-282">Compilación 17692</span><span class="sxs-lookup"><span data-stu-id="058f0-282">Build 17692</span></span>
<span data-ttu-id="058f0-283">Para Windows general, visite información sobre las compilación 17692 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span><span class="sxs-lookup"><span data-stu-id="058f0-283">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="058f0-284">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-284">WSL</span></span>
* <span data-ttu-id="058f0-285">Corregir el problema con el contexto del shell WSL entradas de menú que no administren correctamente las rutas de acceso con espacios.</span><span class="sxs-lookup"><span data-stu-id="058f0-285">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="058f0-286">Exponer entre mayúsculas y minúsculas por directorio como un atributo extendido</span><span class="sxs-lookup"><span data-stu-id="058f0-286">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="058f0-287">ARM64: Emular las operaciones de mantenimiento de caché.</span><span class="sxs-lookup"><span data-stu-id="058f0-287">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="058f0-288">Resolver [dotnet problema](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="058f0-288">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="058f0-289">DrvFs: unescape solo caracteres del intervalo privado que corresponden a un carácter de escape.</span><span class="sxs-lookup"><span data-stu-id="058f0-289">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="058f0-290">Compilación 17686</span><span class="sxs-lookup"><span data-stu-id="058f0-290">Build 17686</span></span>
<span data-ttu-id="058f0-291">Para Windows general, visite información sobre las compilación 17686 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span><span class="sxs-lookup"><span data-stu-id="058f0-291">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="058f0-292">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-292">WSL</span></span>
* <span data-ttu-id="058f0-293">Corregir el error de off a uno en la validación de longitud de intérprete de ELF analizador [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="058f0-293">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="058f0-294">Los temporizadores en absoluto con un tiempo en el pasado WSL no activan [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="058f0-294">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="058f0-295">Asegúrese de recién puntos de reanálisis creado se muestran como tal en el directorio primario.</span><span class="sxs-lookup"><span data-stu-id="058f0-295">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="058f0-296">Crear atómicamente directorios distingue mayúsculas de minúsculas en DrvFs.</span><span class="sxs-lookup"><span data-stu-id="058f0-296">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="058f0-297">Compilación 17677</span><span class="sxs-lookup"><span data-stu-id="058f0-297">Build 17677</span></span>
<span data-ttu-id="058f0-298">Para Windows general, visite información sobre las compilación 17677 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span><span class="sxs-lookup"><span data-stu-id="058f0-298">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="058f0-299">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-299">WSL</span></span>
* <span data-ttu-id="058f0-300">Se corrigió un problema adicional que podrían devolver operaciones multiproceso ENOENT aunque exista el archivo.</span><span class="sxs-lookup"><span data-stu-id="058f0-300">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="058f0-301">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="058f0-301">[GH 2712]</span></span>
* <span data-ttu-id="058f0-302">WSL fijo iniciar un error cuando se habilita UMCI.</span><span class="sxs-lookup"><span data-stu-id="058f0-302">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="058f0-303">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="058f0-303">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="058f0-304">Compilación 17666</span><span class="sxs-lookup"><span data-stu-id="058f0-304">Build 17666</span></span>
<span data-ttu-id="058f0-305">Para Windows general, visite información sobre las compilación 17666 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span><span class="sxs-lookup"><span data-stu-id="058f0-305">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="058f0-306">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-306">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="058f0-307">ADVERTENCIA: Hay un problema que impedía WSL desde que se ejecutan en algunos conjuntos de chips AMD [GH 3134].</span><span class="sxs-lookup"><span data-stu-id="058f0-307">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="058f0-308">Una corrección está listo y realizando su camino hacia la rama de compilación de Insider.</span><span class="sxs-lookup"><span data-stu-id="058f0-308">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="058f0-309">Agregar el menú contextual del explorador para iniciar WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="058f0-309">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="058f0-310">Para usar con el botón secundario en una ventana del explorador y a la espera.</span><span class="sxs-lookup"><span data-stu-id="058f0-310">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="058f0-311">Corregir el comportamiento de no bloqueo del socket de unix [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="058f0-311">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="058f0-312">Corrección de francesa comando NETLINK notificados en 2026 GH.</span><span class="sxs-lookup"><span data-stu-id="058f0-312">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="058f0-313">Agregar compatibilidad con marcadores de propagación de montaje [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="058f0-313">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="058f0-314">Corregir el problema con truncate que no producen inotify eventos [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="058f0-314">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="058f0-315">Agregue--opción exec para wsl.exe invocar un solo archivo binario sin un shell.</span><span class="sxs-lookup"><span data-stu-id="058f0-315">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="058f0-316">Agregar: opción de distribución para wsl.exe seleccionar una distribución específica.</span><span class="sxs-lookup"><span data-stu-id="058f0-316">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="058f0-317">Compilación 17655 (Saltar adelante)</span><span class="sxs-lookup"><span data-stu-id="058f0-317">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="058f0-318">Para Windows general, visite información sobre las compilación 17655 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="058f0-318">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="058f0-319">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-319">WSL</span></span>
* <span data-ttu-id="058f0-320">Compatibilidad limitada con dmesg.</span><span class="sxs-lookup"><span data-stu-id="058f0-320">Limited support for dmesg.</span></span> <span data-ttu-id="058f0-321">Las aplicaciones ahora pueden iniciar en dmesg.</span><span class="sxs-lookup"><span data-stu-id="058f0-321">Applications can now log to dmesg.</span></span> <span data-ttu-id="058f0-322">Controlador WSL registra información limitada a dmesg.</span><span class="sxs-lookup"><span data-stu-id="058f0-322">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="058f0-323">En el futuro, esto puede ampliarse para llevar a cabo otros información/diagnósticos desde el controlador.</span><span class="sxs-lookup"><span data-stu-id="058f0-323">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="058f0-324">Nota: dmesg actualmente se admite a través de la `/dev/kmsg` la interfaz de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="058f0-324">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> `syslog` <span data-ttu-id="058f0-325">aún no se admite la interfaz sycall.</span><span class="sxs-lookup"><span data-stu-id="058f0-325">sycall interface is not yet supported.</span></span> <span data-ttu-id="058f0-326">Y, por lo tanto, algunos de los `dmesg` opciones de línea de comandos tales como `-S`, `-C` no funcionan.</span><span class="sxs-lookup"><span data-stu-id="058f0-326">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="058f0-327">Se ha corregido un problema donde podrían devolver operaciones multiproceso ENOENT aunque exista el archivo.</span><span class="sxs-lookup"><span data-stu-id="058f0-327">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="058f0-328">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="058f0-328">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="058f0-329">Compilación 17639 (Saltar adelante)</span><span class="sxs-lookup"><span data-stu-id="058f0-329">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="058f0-330">Para Windows general, visite información sobre las compilación 17639 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="058f0-330">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="058f0-331">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-331">WSL</span></span>
* <span data-ttu-id="058f0-332">Cambiar el gid de forma predeterminada y el modo de dispositivos serie para que coincida con nativo [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="058f0-332">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="058f0-333">DrvFs ahora es compatible con atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="058f0-333">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="058f0-334">Nota: DrvFs tiene algunas limitaciones en el nombre de los atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="058f0-334">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="058f0-335">En concreto, algunos caracteres (como '/', ':' y '\*') no están permitidos y extendido los nombres de atributo no distinguen mayúsculas de minúsculas en DrvFs</span><span class="sxs-lookup"><span data-stu-id="058f0-335">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="058f0-336">Compilar 17133 (Fast)</span><span class="sxs-lookup"><span data-stu-id="058f0-336">Build 17133 (Fast)</span></span>
<span data-ttu-id="058f0-337">Para Windows general, visite información sobre las compilación 17133 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="058f0-337">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="058f0-338">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-338">WSL</span></span>
* <span data-ttu-id="058f0-339">Corrección de bloqueo en WSL.</span><span class="sxs-lookup"><span data-stu-id="058f0-339">Fix for hang in WSL.</span></span> <span data-ttu-id="058f0-340">[GH 3039, 3034]</span><span class="sxs-lookup"><span data-stu-id="058f0-340">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="058f0-341">Compilar 17128 (Fast)</span><span class="sxs-lookup"><span data-stu-id="058f0-341">Build 17128 (Fast)</span></span>
<span data-ttu-id="058f0-342">Para Windows general, visite información sobre las compilación 17128 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="058f0-342">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="058f0-343">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-343">WSL</span></span>
* <span data-ttu-id="058f0-344">Ninguno</span><span class="sxs-lookup"><span data-stu-id="058f0-344">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="058f0-345">Compilación 17627 (Saltar adelante)</span><span class="sxs-lookup"><span data-stu-id="058f0-345">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="058f0-346">Para Windows general, visite información sobre las compilación 17627 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="058f0-346">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="058f0-347">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-347">WSL</span></span>
* <span data-ttu-id="058f0-348">Agregar compatibilidad para las operaciones basadas en la pi futex.</span><span class="sxs-lookup"><span data-stu-id="058f0-348">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="058f0-349">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="058f0-349">[GH 1006]</span></span>
    * <span data-ttu-id="058f0-350">Tenga en cuenta que las prioridades no son actualmente una característica WSL admitida por lo que existen limitaciones, pero debe desbloquearse uso estándar.</span><span class="sxs-lookup"><span data-stu-id="058f0-350">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="058f0-351">Compatibilidad con el firewall de Windows para los procesos WSL.</span><span class="sxs-lookup"><span data-stu-id="058f0-351">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="058f0-352">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="058f0-352">[GH 1852]</span></span>
    * <span data-ttu-id="058f0-353">Por ejemplo, para permitir el WSL python procesa para que escuche en cualquier puerto, utilice el cmd de Windows con privilegios elevados:</span><span class="sxs-lookup"><span data-stu-id="058f0-353">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd:</span></span>
```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```
    * <span data-ttu-id="058f0-354">Para obtener más información sobre cómo agregar reglas de firewall, consulte [vínculo](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span><span class="sxs-lookup"><span data-stu-id="058f0-354">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="058f0-355">Respetar el shell predeterminado del usuario cuando se usa wsl.exe.</span><span class="sxs-lookup"><span data-stu-id="058f0-355">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="058f0-356">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="058f0-356">[GH 2372]</span></span>
* <span data-ttu-id="058f0-357">Informe todas las interfaces de red como ethernet.</span><span class="sxs-lookup"><span data-stu-id="058f0-357">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="058f0-358">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="058f0-358">[GH 2996]</span></span>
* <span data-ttu-id="058f0-359">Un mejor control del archivo/etc/passwd dañado.</span><span class="sxs-lookup"><span data-stu-id="058f0-359">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="058f0-360">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="058f0-360">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="058f0-361">Console</span><span class="sxs-lookup"><span data-stu-id="058f0-361">Console</span></span>
* <span data-ttu-id="058f0-362">No hay correcciones.</span><span class="sxs-lookup"><span data-stu-id="058f0-362">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-363">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-363">LTP Results:</span></span>
<span data-ttu-id="058f0-364">Las pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="058f0-364">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="058f0-365">Compilación 17618 (Saltar adelante)</span><span class="sxs-lookup"><span data-stu-id="058f0-365">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="058f0-366">Para Windows general, visite información sobre las compilación 17618 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="058f0-366">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="058f0-367">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-367">WSL</span></span>
* <span data-ttu-id="058f0-368">Introducir pseudoconsole funcionalidad para la interoperabilidad de NT [GH 988, 1366, 1433, 1542, 2370, 2406].</span><span class="sxs-lookup"><span data-stu-id="058f0-368">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="058f0-369">El mecanismo de instalación heredada (lxrun.exe) ha quedado obsoleto.</span><span class="sxs-lookup"><span data-stu-id="058f0-369">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="058f0-370">El mecanismo compatible para la instalación de las distribuciones es a través de la Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="058f0-370">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="058f0-371">Console</span><span class="sxs-lookup"><span data-stu-id="058f0-371">Console</span></span>
* <span data-ttu-id="058f0-372">No hay correcciones.</span><span class="sxs-lookup"><span data-stu-id="058f0-372">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-373">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-373">LTP Results:</span></span>
<span data-ttu-id="058f0-374">Las pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="058f0-374">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="058f0-375">Compilación 17110</span><span class="sxs-lookup"><span data-stu-id="058f0-375">Build 17110</span></span>
<span data-ttu-id="058f0-376">Para Windows general, visite información sobre las compilación 17110 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span><span class="sxs-lookup"><span data-stu-id="058f0-376">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="058f0-377">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-377">WSL</span></span>
* <span data-ttu-id="058f0-378">Permitir /init terminar de Windows [GH 2928].</span><span class="sxs-lookup"><span data-stu-id="058f0-378">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="058f0-379">DrvFs utiliza mayúsculas y minúsculas por directorio de forma predeterminada (equivalente a la "caso = dir" opción de montaje).</span><span class="sxs-lookup"><span data-stu-id="058f0-379">DrvFs now uses per-directory case sensitivity by default (equivalent to the “case=dir” mount option).</span></span>
    * <span data-ttu-id="058f0-380">Uso de "caso = force" (el comportamiento anterior) requiere establecer una clave del registro.</span><span class="sxs-lookup"><span data-stu-id="058f0-380">Using “case=force” (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="058f0-381">Ejecute el siguiente comando para habilitar "caso = force" Si necesita usarlo: reg agregar HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span><span class="sxs-lookup"><span data-stu-id="058f0-381">Run the following command to enable “case=force” if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="058f0-382">Si tiene directorios existentes creados con WSL en una versión anterior de Windows que deben estar entre mayúsculas y minúsculas, usar fsutil.exe para marcarlos como con diferenciación entre mayúsculas y minúsculas: fsutil.exe archivo setcasesensitiveinfo <path> habilitar</span><span class="sxs-lookup"><span data-stu-id="058f0-382">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="058f0-383">Finalizar cadenas devueltos desde la syscall uname con NULL.</span><span class="sxs-lookup"><span data-stu-id="058f0-383">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="058f0-384">Console</span><span class="sxs-lookup"><span data-stu-id="058f0-384">Console</span></span>
* <span data-ttu-id="058f0-385">No hay correcciones.</span><span class="sxs-lookup"><span data-stu-id="058f0-385">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-386">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-386">LTP Results:</span></span>
<span data-ttu-id="058f0-387">Las pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="058f0-387">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="058f0-388">Compilación 17107</span><span class="sxs-lookup"><span data-stu-id="058f0-388">Build 17107</span></span>
<span data-ttu-id="058f0-389">Para Windows general, visite información sobre las compilación 17107 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span><span class="sxs-lookup"><span data-stu-id="058f0-389">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="058f0-390">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-390">WSL</span></span>
* <span data-ttu-id="058f0-391">Admite TCSETSF y TCSETSW en los puntos de conexión maestro pty [GH 2552].</span><span class="sxs-lookup"><span data-stu-id="058f0-391">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="058f0-392">A partir de procesos simultáneos de interoperabilidad puede dar lugar a EINVAL [GH 2813].</span><span class="sxs-lookup"><span data-stu-id="058f0-392">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="058f0-393">Corregir PTRACE_ATTACH para mostrar el estado de seguimiento adecuado en /proc/pid/status.</span><span class="sxs-lookup"><span data-stu-id="058f0-393">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="058f0-394">Anticipación de corrección donde los procesos de corta duración clonados con marcas de la CLEARTID y SETTID pudo salir sin borrar la dirección TID.</span><span class="sxs-lookup"><span data-stu-id="058f0-394">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="058f0-395">Mostrar un mensaje al actualizar los directorios de sistema de archivos de Linux al pasar de una compilación anterior a 17093.</span><span class="sxs-lookup"><span data-stu-id="058f0-395">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="058f0-396">Para obtener más detalles sobre los cambios del sistema de 17093 archivo, vea las notas de [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span><span class="sxs-lookup"><span data-stu-id="058f0-396">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="058f0-397">Console</span><span class="sxs-lookup"><span data-stu-id="058f0-397">Console</span></span>
* <span data-ttu-id="058f0-398">No hay correcciones.</span><span class="sxs-lookup"><span data-stu-id="058f0-398">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-399">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-399">LTP Results:</span></span>
<span data-ttu-id="058f0-400">Las pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="058f0-400">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="058f0-401">Compilación 17101</span><span class="sxs-lookup"><span data-stu-id="058f0-401">Build 17101</span></span>
<span data-ttu-id="058f0-402">Para Windows general, visite información sobre las compilación 17101 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="058f0-402">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="058f0-403">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-403">WSL</span></span>
* <span data-ttu-id="058f0-404">Compatibilidad con signalfd.</span><span class="sxs-lookup"><span data-stu-id="058f0-404">Support for signalfd.</span></span> <span data-ttu-id="058f0-405">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="058f0-405">[GH 129]</span></span>
* <span data-ttu-id="058f0-406">Admite nombres de archivo que contiene caracteres no válidos de NTFS mediante su codificación como privados caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="058f0-406">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="058f0-407">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="058f0-407">[GH 1514]</span></span>
* <span data-ttu-id="058f0-408">Montaje automático retrocederá a solo lectura cuando no se admite la escritura.</span><span class="sxs-lookup"><span data-stu-id="058f0-408">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="058f0-409">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="058f0-409">[GH 2603]</span></span>
* <span data-ttu-id="058f0-410">Permitir el pegado de los pares suplentes de Unicode (como emoji caracteres).</span><span class="sxs-lookup"><span data-stu-id="058f0-410">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="058f0-411">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="058f0-411">[GH 2765]</span></span>
* <span data-ttu-id="058f0-412">Archivos pseudo /proc y PF deben devolver leer y escribir listo desde select, sondeo, epoll, et al [GH 2838]</span><span class="sxs-lookup"><span data-stu-id="058f0-412">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="058f0-413">Se corrige el problema que podría provocar que el servicio entrar en bucle infinito cuando el registro ha sido alterado o está dañado.</span><span class="sxs-lookup"><span data-stu-id="058f0-413">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="058f0-414">Corregir mensajes netlink para trabajar con la versión más reciente de (dirección ascendente 4.14) de iproute2.</span><span class="sxs-lookup"><span data-stu-id="058f0-414">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="058f0-415">Console</span><span class="sxs-lookup"><span data-stu-id="058f0-415">Console</span></span>
* <span data-ttu-id="058f0-416">No hay correcciones.</span><span class="sxs-lookup"><span data-stu-id="058f0-416">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-417">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-417">LTP Results:</span></span>
<span data-ttu-id="058f0-418">Las pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="058f0-418">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="058f0-419">Compilación 17093</span><span class="sxs-lookup"><span data-stu-id="058f0-419">Build 17093</span></span>
<span data-ttu-id="058f0-420">Para Windows general, visite información sobre las compilación 17093 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span><span class="sxs-lookup"><span data-stu-id="058f0-420">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="058f0-421">Importante:</span><span class="sxs-lookup"><span data-stu-id="058f0-421">Important:</span></span>
<span data-ttu-id="058f0-422">Al iniciar WSL por primera vez después de actualizar a esta compilación, debe realizar algún trabajo de actualización de los directorios de sistema de archivos de Linux.</span><span class="sxs-lookup"><span data-stu-id="058f0-422">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="058f0-423">Esto puede tardar varios minutos, por lo que puede parecer WSL que iniciarse lentamente.</span><span class="sxs-lookup"><span data-stu-id="058f0-423">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="058f0-424">Esto solo debería ocurrir una vez para cada distribución haya instalado desde la tienda.</span><span class="sxs-lookup"><span data-stu-id="058f0-424">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="058f0-425">Soporte mejorado para mayúsculas y minúsculas en DrvFs.</span><span class="sxs-lookup"><span data-stu-id="058f0-425">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="058f0-426">DrvFs ahora es compatible con mayúsculas y minúsculas por directorio.</span><span class="sxs-lookup"><span data-stu-id="058f0-426">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="058f0-427">Se trata de una nueva marca que se puede establecer en los directorios para indicar que todas las operaciones en estos directorios deben tratarse como distingue mayúsculas de minúsculas, lo que permite que incluso las aplicaciones de Windows abrir correctamente los archivos que difieran solo por caso.</span><span class="sxs-lookup"><span data-stu-id="058f0-427">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="058f0-428">DrvFs tiene nuevas opciones de montaje, control de mayúsculas y minúsculas en una base por directorio</span><span class="sxs-lookup"><span data-stu-id="058f0-428">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="058f0-429">caso = force: todos los directorios se distinguen mayúsculas de minúsculas (excepto la raíz de la unidad).</span><span class="sxs-lookup"><span data-stu-id="058f0-429">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="058f0-430">Nuevos directorios creados con WSL se marcan como distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="058f0-430">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="058f0-431">Este es el comportamiento heredado excepto para marcar los nuevos directorios distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="058f0-431">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="058f0-432">caso = dir: solo los directorios con el indicador de mayúsculas y minúsculas por directorio se distinguen mayúsculas de minúsculas; otros directorios distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="058f0-432">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="058f0-433">Nuevos directorios creados con WSL se marcan como distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="058f0-433">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="058f0-434">caso = desactivada: solo los directorios con el indicador de mayúsculas y minúsculas por directorio se distinguen mayúsculas de minúsculas; otros directorios distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="058f0-434">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="058f0-435">Nuevos directorios creados con WSL se marcan como no distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="058f0-435">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="058f0-436">Nota: los directorios creados por WSL en versiones anteriores no tienen esta marca establecida, por lo que no se tratará como distingue mayúsculas de minúsculas si usa el "caso = dir" opción.</span><span class="sxs-lookup"><span data-stu-id="058f0-436">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the “case=dir” option.</span></span> <span data-ttu-id="058f0-437">Una manera de establecer esta marca en los directorios existentes estará disponible próximamente.</span><span class="sxs-lookup"><span data-stu-id="058f0-437">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="058f0-438">Ejemplo de montaje con estas opciones (las unidades de existente, debe primero desmonte antes de que se puede montar con diferentes opciones): sudo mount -t drvfs C:/mnt/c -o caso = dir</span><span class="sxs-lookup"><span data-stu-id="058f0-438">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="058f0-439">Por ahora, caso = forzar sigue siendo la opción predeterminada.</span><span class="sxs-lookup"><span data-stu-id="058f0-439">For now, case=force is still the default option.</span></span> <span data-ttu-id="058f0-440">Esto se cambiará al caso = dir en el futuro.</span><span class="sxs-lookup"><span data-stu-id="058f0-440">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="058f0-441">Ahora puede usar barras diagonales en las rutas de acceso de Windows al montar DrvFs, p. ej.: -t drvfs //server/share /mnt/share de montaje de sudo</span><span class="sxs-lookup"><span data-stu-id="058f0-441">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="058f0-442">WSL ahora procesa el archivo/etc/fstab durante el inicio de instancia [GH 2636].</span><span class="sxs-lookup"><span data-stu-id="058f0-442">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="058f0-443">Esto se realiza automáticamente montar unidades de DrvFs; las unidades que ya se han montado por fstab no se volverá a montar automáticamente, lo que le permite cambiar el punto de montaje para unidades específicas.</span><span class="sxs-lookup"><span data-stu-id="058f0-443">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="058f0-444">Este comportamiento se puede desactivar mediante wsl.conf.</span><span class="sxs-lookup"><span data-stu-id="058f0-444">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="058f0-445">Los archivos de montaje, mountinfo y mountstats en /proc correctamente caracteres especiales como espacios [GH 2799] y barras diagonales inversas de escape</span><span class="sxs-lookup"><span data-stu-id="058f0-445">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="058f0-446">Archivos especiales que se crean con DrvFs como vínculos simbólicos de WSL, o fifos y sockets cuando están habilitados los metadatos, ahora pueden copiarse y mover de Windows.</span><span class="sxs-lookup"><span data-stu-id="058f0-446">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="058f0-447">Es más configurable con wsl.conf WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-447">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="058f0-448">Se ha agregado un método para que configure automáticamente cierta funcionalidad en WSL que se aplicarán cada vez que inicie el subsistema.</span><span class="sxs-lookup"><span data-stu-id="058f0-448">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="058f0-449">Esto incluye las opciones de montaje automático y la configuración de red.</span><span class="sxs-lookup"><span data-stu-id="058f0-449">This includes automount options and network configuration.</span></span> <span data-ttu-id="058f0-450">Obtenga más información en nuestro blog en: https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="058f0-450">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="afunix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="058f0-451">AF_UNIX permite las conexiones de socket entre los procesos de Linux en WSL y procesos nativos de Windows</span><span class="sxs-lookup"><span data-stu-id="058f0-451">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="058f0-452">Las aplicaciones de Windows y de WSL ahora pueden comunicarse entre sí a través de sockets de Unix.</span><span class="sxs-lookup"><span data-stu-id="058f0-452">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="058f0-453">Imagine que desea ejecutar un servicio en Windows y que esté disponible para las aplicaciones de Windows y WSL.</span><span class="sxs-lookup"><span data-stu-id="058f0-453">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="058f0-454">Ahora, que es posible con sockets de Unix.</span><span class="sxs-lookup"><span data-stu-id="058f0-454">Now, that’s possible with Unix sockets.</span></span> <span data-ttu-id="058f0-455">Leer más información en nuestro blog post en https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="058f0-455">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="058f0-456">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-456">WSL</span></span>
* <span data-ttu-id="058f0-457">Compatibilidad con mmap() con MAP_NORESERVE [GH 121, 2784 error]</span><span class="sxs-lookup"><span data-stu-id="058f0-457">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="058f0-458">Admitir CLONE_PTRACE y CLONE_UNTRACED [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="058f0-458">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="058f0-459">Controlar la señal de finalización no SIGCHLD en clon [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="058f0-459">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="058f0-460">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="058f0-460">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="058f0-461">Error al cargar los archivos binarios de ELF que contienen encabezados de carga con desplazamientos distinto de cero [GH 1884]</span><span class="sxs-lookup"><span data-stu-id="058f0-461">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="058f0-462">Cero out finales bytes de la página al cargar imágenes.</span><span class="sxs-lookup"><span data-stu-id="058f0-462">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="058f0-463">Reducir los casos donde execve finaliza en modo silencioso el proceso</span><span class="sxs-lookup"><span data-stu-id="058f0-463">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="058f0-464">Console</span><span class="sxs-lookup"><span data-stu-id="058f0-464">Console</span></span>
* <span data-ttu-id="058f0-465">No hay correcciones.</span><span class="sxs-lookup"><span data-stu-id="058f0-465">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-466">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-466">LTP Results:</span></span>
<span data-ttu-id="058f0-467">Las pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="058f0-467">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="058f0-468">Compilación 17083</span><span class="sxs-lookup"><span data-stu-id="058f0-468">Build 17083</span></span>
<span data-ttu-id="058f0-469">Para Windows general, visite información sobre las compilación 17083 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="058f0-469">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="058f0-470">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-470">WSL</span></span>
* <span data-ttu-id="058f0-471">Fijo comprobación de errores relacionados con epoll [GH 2798, 2801, 2857]</span><span class="sxs-lookup"><span data-stu-id="058f0-471">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="058f0-472">Fijo se bloquea cuando la desactivación de ASLR [GH 1185, 2870]</span><span class="sxs-lookup"><span data-stu-id="058f0-472">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="058f0-473">Asegúrese de operaciones mmap aparecen atómicas [GH 2732]</span><span class="sxs-lookup"><span data-stu-id="058f0-473">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="058f0-474">Console</span><span class="sxs-lookup"><span data-stu-id="058f0-474">Console</span></span>
* <span data-ttu-id="058f0-475">No hay correcciones.</span><span class="sxs-lookup"><span data-stu-id="058f0-475">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-476">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-476">LTP Results:</span></span>
<span data-ttu-id="058f0-477">Las pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="058f0-477">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="058f0-478">Compilación 17074</span><span class="sxs-lookup"><span data-stu-id="058f0-478">Build 17074</span></span>
<span data-ttu-id="058f0-479">Para Windows general, visite información sobre las compilación 17074 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span><span class="sxs-lookup"><span data-stu-id="058f0-479">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="058f0-480">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-480">WSL</span></span>
* <span data-ttu-id="058f0-481">Formato de almacenamiento fijo de metadatos DrvFs [GH 2777]</span><span class="sxs-lookup"><span data-stu-id="058f0-481">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="058f0-482">**Importante:** Metadatos de DrvFs creados antes de que esta compilación se mostrará incorrectamente o no admitirlo.</span><span class="sxs-lookup"><span data-stu-id="058f0-482">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="058f0-483">Para corregir los archivos afectados, use chmod y chown para volver a aplicar los metadatos.</span><span class="sxs-lookup"><span data-stu-id="058f0-483">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="058f0-484">Se corrigió un problema con varias señales y syscalls reiniciables.</span><span class="sxs-lookup"><span data-stu-id="058f0-484">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="058f0-485">Console</span><span class="sxs-lookup"><span data-stu-id="058f0-485">Console</span></span>
* <span data-ttu-id="058f0-486">No hay correcciones.</span><span class="sxs-lookup"><span data-stu-id="058f0-486">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-487">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-487">LTP Results:</span></span>
<span data-ttu-id="058f0-488">Las pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="058f0-488">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="058f0-489">Compilación 17063</span><span class="sxs-lookup"><span data-stu-id="058f0-489">Build 17063</span></span>
<span data-ttu-id="058f0-490">Para Windows general, visite información sobre las compilación 17063 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span><span class="sxs-lookup"><span data-stu-id="058f0-490">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="058f0-491">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-491">WSL</span></span>
* <span data-ttu-id="058f0-492">DrvFs admite metadatos adicionales de Linux.</span><span class="sxs-lookup"><span data-stu-id="058f0-492">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="058f0-493">Esto permite establecer el propietario y el modo de archivos mediante chmod/chown y también la creación de archivos especiales como fifos, sockets de unix y los archivos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="058f0-493">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="058f0-494">Esto está deshabilitada de forma predeterminada por ahora, ya que es todavía experimental.</span><span class="sxs-lookup"><span data-stu-id="058f0-494">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="058f0-495">**Nota:**  Se ha corregido un error en el formato de metadatos utilizado por DrvFs.</span><span class="sxs-lookup"><span data-stu-id="058f0-495">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="058f0-496">Aunque los metadatos funciona en esta compilación para la experimentación, compilaciones futuras no leerá correctamente metadatos creados por esta compilación.</span><span class="sxs-lookup"><span data-stu-id="058f0-496">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="058f0-497">Es posible que deba actualizar manualmente el propietario de los archivos modificados y los dispositivos con un identificador de dispositivo personalizada tendrán que volver a crear.</span><span class="sxs-lookup"><span data-stu-id="058f0-497">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="058f0-498">Para habilitar DrvFs de montaje con la opción de metadatos (para habilitarla en un montaje existente, debe primero desmontarla):</span><span class="sxs-lookup"><span data-stu-id="058f0-498">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="058f0-499">Permisos de Linux se agregan como metadatos adicionales en el archivo; no afectan a los permisos de Windows.</span><span class="sxs-lookup"><span data-stu-id="058f0-499">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="058f0-500">Recuerde, edición de un archivo con un editor de Windows puede quitar los metadatos.</span><span class="sxs-lookup"><span data-stu-id="058f0-500">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="058f0-501">En este caso, el archivo volverá a sus permisos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="058f0-501">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="058f0-502">Opciones de montaje se ha agregado a DrvFs para controlar los archivos sin metadatos.</span><span class="sxs-lookup"><span data-stu-id="058f0-502">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="058f0-503">UID: el identificador de usuario usado para el propietario de todos los archivos.</span><span class="sxs-lookup"><span data-stu-id="058f0-503">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="058f0-504">GID: el identificador de grupo usado para el propietario de todos los archivos.</span><span class="sxs-lookup"><span data-stu-id="058f0-504">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="058f0-505">umask: una máscara de permisos que se van a excluir para todos los archivos y directorios octal.</span><span class="sxs-lookup"><span data-stu-id="058f0-505">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="058f0-506">fMask: una máscara de permisos para excluir todos los archivos normales octal.</span><span class="sxs-lookup"><span data-stu-id="058f0-506">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="058f0-507">dmask: una máscara de permisos para excluir todos los directorios octal.</span><span class="sxs-lookup"><span data-stu-id="058f0-507">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="058f0-508">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="058f0-508">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="058f0-509">Combinar con la opción de metadatos para especificar los permisos predeterminados para los archivos sin metadatos.</span><span class="sxs-lookup"><span data-stu-id="058f0-509">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="058f0-510">Introdujo una nueva variable de entorno, `WSLENV`, para configurar cómo fluyen las variables de entorno entre WSL y Win32.</span><span class="sxs-lookup"><span data-stu-id="058f0-510">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="058f0-511">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="058f0-511">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  `WSLENV` <span data-ttu-id="058f0-512">es una lista delimitada por signos de variables de entorno que se pueden incluir, al iniciar los procesos WSL de Win32 o Win32 de WSL.</span><span class="sxs-lookup"><span data-stu-id="058f0-512">is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="058f0-513">Cada variable puede tener el sufijo con una barra diagonal seguida de marcadores que especifican cómo se traduce.</span><span class="sxs-lookup"><span data-stu-id="058f0-513">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="058f0-514">p: El valor es una ruta de acceso que se debe traducir entre las rutas de acceso WSL y rutas de acceso de Win32.</span><span class="sxs-lookup"><span data-stu-id="058f0-514">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="058f0-515">l: El valor es una lista de rutas de acceso.</span><span class="sxs-lookup"><span data-stu-id="058f0-515">l: The value is a list of paths.</span></span> <span data-ttu-id="058f0-516">En WSL, es una lista delimitada por dos puntos.</span><span class="sxs-lookup"><span data-stu-id="058f0-516">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="058f0-517">En Win32, es una lista delimitada por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="058f0-517">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="058f0-518">u: El valor sólo debe incluir al invocar WSL de Win32</span><span class="sxs-lookup"><span data-stu-id="058f0-518">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="058f0-519">w: El valor sólo debe incluir al invocar Win32 de WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-519">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="058f0-520">Puede establecer `WSLENV` en .bashrc o en el entorno de Windows personalizadas para el usuario.</span><span class="sxs-lookup"><span data-stu-id="058f0-520">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="058f0-521">montajes drvfs conserva correctamente las marcas de tiempo desde el archivo tar, cp -p (GH 1939)</span><span class="sxs-lookup"><span data-stu-id="058f0-521">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="058f0-522">vínculos simbólicos drvfs informa del tamaño correcto (GH 2641)</span><span class="sxs-lookup"><span data-stu-id="058f0-522">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="058f0-523">lectura/escritura funciona para los tamaños de E/S muy grandes (GH 2653)</span><span class="sxs-lookup"><span data-stu-id="058f0-523">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="058f0-524">waitpid funciona con identificadores (GH 2534) del grupo de proceso</span><span class="sxs-lookup"><span data-stu-id="058f0-524">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="058f0-525">significativamente mmap mejor rendimiento para las regiones de gran tamaño de reserva; mejora el rendimiento ghc (GH 1671)</span><span class="sxs-lookup"><span data-stu-id="058f0-525">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="058f0-526">admite la personalidad de READ_IMPLIES_EXEC; máximos de correcciones y clisp (GH 1185)</span><span class="sxs-lookup"><span data-stu-id="058f0-526">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="058f0-527">mprotect admite PROT_GROWSDOWN; correcciones clisp (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="058f0-527">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="058f0-528">sobrecarga de correcciones de errores de página en modo; correcciones sbcl (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="058f0-528">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="058f0-529">clon es compatible con varias combinaciones de marcas</span><span class="sxs-lookup"><span data-stu-id="058f0-529">clone supports more flags combinations</span></span>
* <span data-ttu-id="058f0-530">Compatibilidad con select/epoll de archivos epoll (previamente una operación inefectiva).</span><span class="sxs-lookup"><span data-stu-id="058f0-530">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="058f0-531">Notificar ptrace de syscall no implementada.</span><span class="sxs-lookup"><span data-stu-id="058f0-531">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="058f0-532">Omitir las interfaces que no están activos cuando se generan los servidores de nombres resolv.conf [GH 2694]</span><span class="sxs-lookup"><span data-stu-id="058f0-532">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="058f0-533">Enumerar las interfaces de red con ninguna dirección física.</span><span class="sxs-lookup"><span data-stu-id="058f0-533">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="058f0-534">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="058f0-534">[GH 2685]</span></span>
* <span data-ttu-id="058f0-535">Mejoras y correcciones de errores adicionales.</span><span class="sxs-lookup"><span data-stu-id="058f0-535">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="058f0-536">Herramientas de Linux disponibles para los desarrolladores en Windows</span><span class="sxs-lookup"><span data-stu-id="058f0-536">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="058f0-537">Cadena de herramientas de línea de comandos de Windows incluye bsdtar (tar) y curl.</span><span class="sxs-lookup"><span data-stu-id="058f0-537">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="058f0-538">Lectura [este blog](https://aka.ms/tarcurlwindows) para obtener más información sobre la adición de estas dos nuevas herramientas y ver cómo está dando forma a la experiencia del desarrollador de Windows.</span><span class="sxs-lookup"><span data-stu-id="058f0-538">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they’re shaping the developer experience on Windows.</span></span>

*   `AF_UNIX` <span data-ttu-id="058f0-539">está disponible en el SDK de Windows Insider (17061 +).</span><span class="sxs-lookup"><span data-stu-id="058f0-539">is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="058f0-540">Lectura [este blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) para obtener más información acerca de `AF_UNIX` y cómo pueden usar los desarrolladores en Windows.</span><span class="sxs-lookup"><span data-stu-id="058f0-540">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="058f0-541">Console</span><span class="sxs-lookup"><span data-stu-id="058f0-541">Console</span></span>
* <span data-ttu-id="058f0-542">No hay correcciones.</span><span class="sxs-lookup"><span data-stu-id="058f0-542">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-543">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-543">LTP Results:</span></span>
<span data-ttu-id="058f0-544">Las pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="058f0-544">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="058f0-545">Compilación 17046</span><span class="sxs-lookup"><span data-stu-id="058f0-545">Build 17046</span></span>

<span data-ttu-id="058f0-546">Para Windows general, visite información sobre las compilación 17046 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span><span class="sxs-lookup"><span data-stu-id="058f0-546">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="058f0-547">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-547">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="058f0-548">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-548">WSL</span></span>
- <span data-ttu-id="058f0-549">Permitir que los procesos se ejecuten sin un terminal activo.</span><span class="sxs-lookup"><span data-stu-id="058f0-549">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="058f0-550">[GH 709, 1007, 1511, 2252, 2391, et al.]</span><span class="sxs-lookup"><span data-stu-id="058f0-550">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="058f0-551">Una mejor compatibilidad con CLONE_VFORK y CLONE_VM.</span><span class="sxs-lookup"><span data-stu-id="058f0-551">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="058f0-552">[GH 1878, 2615]</span><span class="sxs-lookup"><span data-stu-id="058f0-552">[GH 1878, 2615]</span></span>
- <span data-ttu-id="058f0-553">Omitir los controladores del filtro TDI de WSL las operaciones de red.</span><span class="sxs-lookup"><span data-stu-id="058f0-553">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="058f0-554">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="058f0-554">[GH 1554]</span></span>
- <span data-ttu-id="058f0-555">DrvFs crea vínculos simbólicos de NT cuando se cumplen ciertas condiciones.</span><span class="sxs-lookup"><span data-stu-id="058f0-555">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="058f0-556">[GH 353, 1475, 2602]</span><span class="sxs-lookup"><span data-stu-id="058f0-556">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="058f0-557">El destino de vínculo debe ser relativo, no debe ocupar los puntos de montaje o vínculos simbólicos y debe existir.</span><span class="sxs-lookup"><span data-stu-id="058f0-557">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="058f0-558">El usuario debe tener SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (Esto normalmente requiere que se inicie con privilegios elevados wsl.exe), a menos que el modo de programador está activado.</span><span class="sxs-lookup"><span data-stu-id="058f0-558">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="058f0-559">En el resto de situaciones, DrvFs sigue creando vínculos simbólicos WSL.</span><span class="sxs-lookup"><span data-stu-id="058f0-559">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="058f0-560">Permitir que se ejecuten con privilegios elevados y sin privilegios elevados instancias WSL simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="058f0-560">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="058f0-561">Support /proc/sys/kernel/yama/ptrace_scope</span><span class="sxs-lookup"><span data-stu-id="058f0-561">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="058f0-562">Agregar wslpath para hacer WSL <> – conversiones de ruta de acceso de Windows.</span><span class="sxs-lookup"><span data-stu-id="058f0-562">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="058f0-563">[GH 522, 1243, 1834, 2327, et al.]</span><span class="sxs-lookup"><span data-stu-id="058f0-563">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a><span data-ttu-id="058f0-564">Console</span><span class="sxs-lookup"><span data-stu-id="058f0-564">Console</span></span>
- <span data-ttu-id="058f0-565">No hay correcciones.</span><span class="sxs-lookup"><span data-stu-id="058f0-565">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-566">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-566">LTP Results:</span></span>
<span data-ttu-id="058f0-567">Las pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="058f0-567">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="058f0-568">Compilación 17040</span><span class="sxs-lookup"><span data-stu-id="058f0-568">Build 17040</span></span>

<span data-ttu-id="058f0-569">Para Windows general, visite información sobre las compilación 17040 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span><span class="sxs-lookup"><span data-stu-id="058f0-569">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-570">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-570">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="058f0-571">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-571">WSL</span></span>
- <span data-ttu-id="058f0-572">No hay correcciones desde 17035.</span><span class="sxs-lookup"><span data-stu-id="058f0-572">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="058f0-573">Console</span><span class="sxs-lookup"><span data-stu-id="058f0-573">Console</span></span>
- <span data-ttu-id="058f0-574">No hay correcciones desde 17035.</span><span class="sxs-lookup"><span data-stu-id="058f0-574">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-575">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-575">LTP Results:</span></span>
<span data-ttu-id="058f0-576">Las pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="058f0-576">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="058f0-577">Compilación 17035</span><span class="sxs-lookup"><span data-stu-id="058f0-577">Build 17035</span></span>

<span data-ttu-id="058f0-578">Para Windows general, visite información sobre las compilación 17035 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span><span class="sxs-lookup"><span data-stu-id="058f0-578">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-579">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-579">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="058f0-580">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-580">WSL</span></span>
- <span data-ttu-id="058f0-581">Acceso a archivos en DrvFs podría no funcionar ocasionalmente con EINVAL.</span><span class="sxs-lookup"><span data-stu-id="058f0-581">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="058f0-582">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="058f0-582">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="058f0-583">Console</span><span class="sxs-lookup"><span data-stu-id="058f0-583">Console</span></span>
- <span data-ttu-id="058f0-584">Alguna pérdida de color al insertar o eliminar líneas en el modo de VT.</span><span class="sxs-lookup"><span data-stu-id="058f0-584">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-585">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-585">LTP Results:</span></span>
<span data-ttu-id="058f0-586">Las pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="058f0-586">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="058f0-587">Compilación 17025</span><span class="sxs-lookup"><span data-stu-id="058f0-587">Build 17025</span></span>

<span data-ttu-id="058f0-588">Para Windows general, visite información sobre las compilación 17025 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span><span class="sxs-lookup"><span data-stu-id="058f0-588">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-589">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-589">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="058f0-590">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-590">WSL</span></span>
- <span data-ttu-id="058f0-591">Iniciar procesos iniciales en un nuevo grupo de proceso [GH 1653, 2510] de primer plano.</span><span class="sxs-lookup"><span data-stu-id="058f0-591">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="058f0-592">Entrega SIGHUP corrige [GH 2496].</span><span class="sxs-lookup"><span data-stu-id="058f0-592">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="058f0-593">Generar nombre de puente virtual predeterminado si proporciona ninguno [GH 2497].</span><span class="sxs-lookup"><span data-stu-id="058f0-593">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="058f0-594">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span><span class="sxs-lookup"><span data-stu-id="058f0-594">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="058f0-595">Corrige la canalización de stdout y stderr más interoperabilidad.</span><span class="sxs-lookup"><span data-stu-id="058f0-595">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="058f0-596">Código auxiliar syncfs llamada del sistema.</span><span class="sxs-lookup"><span data-stu-id="058f0-596">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="058f0-597">Console</span><span class="sxs-lookup"><span data-stu-id="058f0-597">Console</span></span>
- <span data-ttu-id="058f0-598">Corregir traducción de VT entrada para las consolas de terceros [GH 111]</span><span class="sxs-lookup"><span data-stu-id="058f0-598">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-599">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-599">LTP Results:</span></span>
<span data-ttu-id="058f0-600">Las pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="058f0-600">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="058f0-601">Compilación 17017</span><span class="sxs-lookup"><span data-stu-id="058f0-601">Build 17017</span></span>

<span data-ttu-id="058f0-602">Para Windows general, visite información sobre las compilación 17017 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span><span class="sxs-lookup"><span data-stu-id="058f0-602">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-603">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-603">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="058f0-604">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-604">WSL</span></span>
- <span data-ttu-id="058f0-605">Omitir los encabezados ELF programa [GH 330] estén vacíos.</span><span class="sxs-lookup"><span data-stu-id="058f0-605">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="058f0-606">Permitir LxssManager crear instancias WSL para los usuarios no interactivos (ssh y programado la compatibilidad con la tarea) [GH 777, 1602].</span><span class="sxs-lookup"><span data-stu-id="058f0-606">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="058f0-607">Compatibilidad con WSL -> Win32 -> [GH 1228] de escenarios de WSL ("origen").</span><span class="sxs-lookup"><span data-stu-id="058f0-607">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="058f0-608">Compatibilidad limitada para la terminación de las aplicaciones de consola que se invoca a través de interoperabilidad [GH 1614].</span><span class="sxs-lookup"><span data-stu-id="058f0-608">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="058f0-609">Compatibilidad con las opciones de montaje para devpts [GH 1948].</span><span class="sxs-lookup"><span data-stu-id="058f0-609">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="058f0-610">Ptrace bloqueo inicio secundarios [GH 2333].</span><span class="sxs-lookup"><span data-stu-id="058f0-610">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="058f0-611">EPOLLET faltan algunos eventos [GH 2462].</span><span class="sxs-lookup"><span data-stu-id="058f0-611">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="058f0-612">Devolver más datos para PTRACE_GETSIGINFO.</span><span class="sxs-lookup"><span data-stu-id="058f0-612">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="058f0-613">Getdents con lseek ofrece resultados incorrectos.</span><span class="sxs-lookup"><span data-stu-id="058f0-613">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="058f0-614">Corregir algunos bloqueos de aplicación de interoperabilidad de Win32, esperando una entrada en una canalización que no tiene ningún dato más.</span><span class="sxs-lookup"><span data-stu-id="058f0-614">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="058f0-615">Compatibilidad con archivos tty/pty O_ASYNC.</span><span class="sxs-lookup"><span data-stu-id="058f0-615">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="058f0-616">Otras mejoras y correcciones de errores</span><span class="sxs-lookup"><span data-stu-id="058f0-616">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="058f0-617">Console</span><span class="sxs-lookup"><span data-stu-id="058f0-617">Console</span></span>
- <span data-ttu-id="058f0-618">Ninguna consola otros cambios relacionados en esta versión.</span><span class="sxs-lookup"><span data-stu-id="058f0-618">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-619">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-619">LTP Results:</span></span>
<span data-ttu-id="058f0-620">Las pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="058f0-620">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="058f0-621">Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="058f0-621">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="058f0-622">Compilación 16288</span><span class="sxs-lookup"><span data-stu-id="058f0-622">Build 16288</span></span>

<span data-ttu-id="058f0-623">Para Windows general, visite información sobre las compilación 16288 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span><span class="sxs-lookup"><span data-stu-id="058f0-623">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-624">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-624">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="058f0-625">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-625">WSL</span></span>
- <span data-ttu-id="058f0-626">Inicializar correctamente y notificar uid, gid y el modo de descriptores de archivo socket [GH 2490]</span><span class="sxs-lookup"><span data-stu-id="058f0-626">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="058f0-627">Otras mejoras y correcciones de errores</span><span class="sxs-lookup"><span data-stu-id="058f0-627">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="058f0-628">Console</span><span class="sxs-lookup"><span data-stu-id="058f0-628">Console</span></span>
- <span data-ttu-id="058f0-629">Ninguna consola otros cambios relacionados en esta versión.</span><span class="sxs-lookup"><span data-stu-id="058f0-629">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-630">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-630">LTP Results:</span></span>
<span data-ttu-id="058f0-631">Ningún cambio desde 16273</span><span class="sxs-lookup"><span data-stu-id="058f0-631">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="058f0-632">Compilación 16278</span><span class="sxs-lookup"><span data-stu-id="058f0-632">Build 16278</span></span>

<span data-ttu-id="058f0-633">Para Windows general, visite información sobre las compilación 162738 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span><span class="sxs-lookup"><span data-stu-id="058f0-633">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-634">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-634">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="058f0-635">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-635">WSL</span></span>
- <span data-ttu-id="058f0-636">Anular la asignación de vistas asignadas de secciones del archivo de seguridad explícitamente al destruir el estado LX MM [GH 2415]</span><span class="sxs-lookup"><span data-stu-id="058f0-636">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="058f0-637">Otras mejoras y correcciones de errores</span><span class="sxs-lookup"><span data-stu-id="058f0-637">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="058f0-638">Console</span><span class="sxs-lookup"><span data-stu-id="058f0-638">Console</span></span>
- <span data-ttu-id="058f0-639">Ninguna consola otros cambios relacionados en esta versión.</span><span class="sxs-lookup"><span data-stu-id="058f0-639">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-640">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-640">LTP Results:</span></span>
<span data-ttu-id="058f0-641">Ningún cambio desde 16273</span><span class="sxs-lookup"><span data-stu-id="058f0-641">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="058f0-642">Compilación 16275</span><span class="sxs-lookup"><span data-stu-id="058f0-642">Build 16275</span></span>

<span data-ttu-id="058f0-643">Para Windows general, visite información sobre las compilación 162735 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span><span class="sxs-lookup"><span data-stu-id="058f0-643">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-644">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-644">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="058f0-645">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-645">WSL</span></span>
- <span data-ttu-id="058f0-646">No hay WSL otros cambios relacionados en esta versión.</span><span class="sxs-lookup"><span data-stu-id="058f0-646">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="058f0-647">Console</span><span class="sxs-lookup"><span data-stu-id="058f0-647">Console</span></span>
- <span data-ttu-id="058f0-648">Ninguna consola otros cambios relacionados en esta versión.</span><span class="sxs-lookup"><span data-stu-id="058f0-648">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-649">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-649">LTP Results:</span></span>
<span data-ttu-id="058f0-650">Ningún cambio desde 16273</span><span class="sxs-lookup"><span data-stu-id="058f0-650">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="058f0-651">Compilación 16273</span><span class="sxs-lookup"><span data-stu-id="058f0-651">Build 16273</span></span>

<span data-ttu-id="058f0-652">Para Windows general, visite información sobre las compilación 16273 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span><span class="sxs-lookup"><span data-stu-id="058f0-652">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-653">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-653">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="058f0-654">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-654">WSL</span></span>
- <span data-ttu-id="058f0-655">Se ha corregido un problema donde DrvFs notifican a veces, el tipo de archivo incorrecto para los directorios [GH 2392]</span><span class="sxs-lookup"><span data-stu-id="058f0-655">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="058f0-656">Permitir la creación de sockets NETLINK_KOBJECT_UEVENT para desbloquear los programas que uevent uso [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span><span class="sxs-lookup"><span data-stu-id="058f0-656">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="058f0-657">Agregar compatibilidad para la conexión de no bloqueo [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span><span class="sxs-lookup"><span data-stu-id="058f0-657">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="058f0-658">Implemente CLONE_FS clonar el indicador de llamada del sistema [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="058f0-658">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="058f0-659">Solucionar problemas con respecto al control de no tabulaciones o comillas correctamente en la interoperabilidad de NT [GH 1625, 2164]</span><span class="sxs-lookup"><span data-stu-id="058f0-659">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="058f0-660">Resolver errores cuando se intenta volver a iniciar WSL instancias [GH 651, 2095] ha denegado el acceso</span><span class="sxs-lookup"><span data-stu-id="058f0-660">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="058f0-661">Implementar futex FUTEX_REQUEUE y FUTEX_CMP_REQUEUE operaciones [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="058f0-661">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="058f0-662">Corrija los permisos para los distintos archivos SysFs [GH 2214]</span><span class="sxs-lookup"><span data-stu-id="058f0-662">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="058f0-663">Corregir el bloqueo de la pila de Haskell durante la instalación [GH 2290]</span><span class="sxs-lookup"><span data-stu-id="058f0-663">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="058f0-664">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="058f0-664">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="058f0-665">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span><span class="sxs-lookup"><span data-stu-id="058f0-665">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="058f0-666">Agregar compatibilidad parcial con la llamada del sistema ioprio_set [GH 498]</span><span class="sxs-lookup"><span data-stu-id="058f0-666">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="058f0-667">Código auxiliar SO_REUSEPORT & Agregar compatibilidad con SO_PASSCRED de netlink sockets [69 GH]</span><span class="sxs-lookup"><span data-stu-id="058f0-667">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="058f0-668">Devolver códigos de error diferentes de RegisterDistribuiton si una distribución actualmente se está instalado o desinstalado.</span><span class="sxs-lookup"><span data-stu-id="058f0-668">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="058f0-669">Permitir anulación del registro de las distribuciones de WSL parcialmente instaladas a través de wslconfig.exe</span><span class="sxs-lookup"><span data-stu-id="058f0-669">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="058f0-670">Corregir la falta de respuesta de python socket ensayo desde udp::msg_peek</span><span class="sxs-lookup"><span data-stu-id="058f0-670">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="058f0-671">Otras mejoras y correcciones de errores</span><span class="sxs-lookup"><span data-stu-id="058f0-671">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="058f0-672">Console</span><span class="sxs-lookup"><span data-stu-id="058f0-672">Console</span></span>
- <span data-ttu-id="058f0-673">Ninguna consola otros cambios relacionados en esta versión.</span><span class="sxs-lookup"><span data-stu-id="058f0-673">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-674">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-674">LTP Results:</span></span>
<span data-ttu-id="058f0-675">Total de pruebas: 1904</span><span class="sxs-lookup"><span data-stu-id="058f0-675">Total Tests: 1904</span></span><br/>
<span data-ttu-id="058f0-676">Pruebas de omitidos totales: 209</span><span class="sxs-lookup"><span data-stu-id="058f0-676">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="058f0-677">Número total de errores: 229</span><span class="sxs-lookup"><span data-stu-id="058f0-677">Total Failures: 229</span></span><br/>
[<span data-ttu-id="058f0-678">Los registros de ejecución de pruebas LTP</span><span class="sxs-lookup"><span data-stu-id="058f0-678">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="058f0-679">Compilación 16257</span><span class="sxs-lookup"><span data-stu-id="058f0-679">Build 16257</span></span>

<span data-ttu-id="058f0-680">Para Windows general, visite información sobre las compilación 16257 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span><span class="sxs-lookup"><span data-stu-id="058f0-680">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-681">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-681">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="058f0-682">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-682">WSL</span></span>
- <span data-ttu-id="058f0-683">Implementar prlimit64 llamada del sistema</span><span class="sxs-lookup"><span data-stu-id="058f0-683">Implement prlimit64 system call</span></span>
- <span data-ttu-id="058f0-684">Agregar compatibilidad para ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="058f0-684">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="058f0-685">Código auxiliar MSG_MORE para los sockets TCP [GH 2351]</span><span class="sxs-lookup"><span data-stu-id="058f0-685">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="058f0-686">Corregir comportamiento no válido de vector auxiliar AT_EXECFN [GH 2133]</span><span class="sxs-lookup"><span data-stu-id="058f0-686">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="058f0-687">Corregir el comportamiento de copiar y pegar para consola/tty y agregar mejor búfer lleno de control [GH 2204, 2131]</span><span class="sxs-lookup"><span data-stu-id="058f0-687">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="058f0-688">Establecer AT_SECURE en vector auxiliar para programas de Id. de usuario de conjunto y set-group-ID [GH 2031]</span><span class="sxs-lookup"><span data-stu-id="058f0-688">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="058f0-689">Psuedo terminal punto de conexión principal no se controla TIOCPGRP [GH 1063]</span><span class="sxs-lookup"><span data-stu-id="058f0-689">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="058f0-690">Corrección lseek hace para rebobinar directorios en LxFs [GH 2310]</span><span class="sxs-lookup"><span data-stu-id="058f0-690">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="058f0-691">/dev/ptmx locks up after heavy usage [GH 1882]</span><span class="sxs-lookup"><span data-stu-id="058f0-691">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="058f0-692">Otras mejoras y correcciones de errores</span><span class="sxs-lookup"><span data-stu-id="058f0-692">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="058f0-693">Console</span><span class="sxs-lookup"><span data-stu-id="058f0-693">Console</span></span>
- <span data-ttu-id="058f0-694">Corrección para horizontal líneas o caracteres de subrayado en todas partes [GH 2168]</span><span class="sxs-lookup"><span data-stu-id="058f0-694">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="058f0-695">Corrección del error por orden de proceso cambiado NPM hacen más difícil cerrar [GH 2170]</span><span class="sxs-lookup"><span data-stu-id="058f0-695">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="058f0-696">Agrega la nueva combinación de colores: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="058f0-696">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-697">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-697">LTP Results:</span></span>
<span data-ttu-id="058f0-698">Ningún cambio desde 16251</span><span class="sxs-lookup"><span data-stu-id="058f0-698">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="058f0-699">Soporte técnico de syscall</span><span class="sxs-lookup"><span data-stu-id="058f0-699">Syscall Support</span></span>
<span data-ttu-id="058f0-700">A continuación se muestran una lista de nuevas o mejoradas syscalls que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="058f0-700">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="058f0-701">Las llamadas en esta lista se admiten en al menos un escenario, pero es posible que no dispone de todos los parámetros compatibles en este momento.</span><span class="sxs-lookup"><span data-stu-id="058f0-701">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="058f0-702">Problemas conocidos</span><span class="sxs-lookup"><span data-stu-id="058f0-702">Known Issues</span></span>
#### [<a name="github-issue-2392-windows-folders-not-recognized-by-wsl-"></a><span data-ttu-id="058f0-703">GitHub Issue 2392: Carpetas de Windows no reconoce WSL...</span><span class="sxs-lookup"><span data-stu-id="058f0-703">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="058f0-704">En la compilación 16257, WSL tiene problemas al enumerar los archivos o carpetas de Windows a través de `/mnt/c/...`.</span><span class="sxs-lookup"><span data-stu-id="058f0-704">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="058f0-705">Este problema se ha corregido y deberían liberarse en Insider durante la semana del 14/8/2017.</span><span class="sxs-lookup"><span data-stu-id="058f0-705">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="058f0-706">Compilación 16251</span><span class="sxs-lookup"><span data-stu-id="058f0-706">Build 16251</span></span>

<span data-ttu-id="058f0-707">Para Windows general, visite información sobre las compilación 16251 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span><span class="sxs-lookup"><span data-stu-id="058f0-707">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-708">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-708">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="058f0-709">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-709">WSL</span></span>
- <span data-ttu-id="058f0-710">Quitar la etiqueta a la versión beta de componente opcional de WSL, consulte [entrada de blog](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="058f0-710">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="058f0-711">Inicializar correctamente el conjunto guardado uid y gid de Id. de usuario de conjunto y el Id. de grupo de conjunto de archivos binarios en exec [GH 962, 1415, 2072]</span><span class="sxs-lookup"><span data-stu-id="058f0-711">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="058f0-712">Se agregó compatibilidad para ptrace PTRACE_O_TRACEEXIT [GH 555]</span><span class="sxs-lookup"><span data-stu-id="058f0-712">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="058f0-713">Ha agregado compatibilidad con ptrace PTRACE_GETFPREGS y PTRACE_GETREGSET con NT_FPREGSET [GH 555]</span><span class="sxs-lookup"><span data-stu-id="058f0-713">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="058f0-714">Se ha corregido ptrace detener en omite las señales</span><span class="sxs-lookup"><span data-stu-id="058f0-714">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="058f0-715">Otras mejoras y correcciones de errores</span><span class="sxs-lookup"><span data-stu-id="058f0-715">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="058f0-716">Console</span><span class="sxs-lookup"><span data-stu-id="058f0-716">Console</span></span>
- <span data-ttu-id="058f0-717">Ninguna consola otros cambios relacionados en esta versión.</span><span class="sxs-lookup"><span data-stu-id="058f0-717">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-718">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-718">LTP Results:</span></span>
<span data-ttu-id="058f0-719">Número de pruebas superadas: 768</span><span class="sxs-lookup"><span data-stu-id="058f0-719">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="058f0-720">Número de pruebas no superadas: 244</span><span class="sxs-lookup"><span data-stu-id="058f0-720">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="058f0-721">Número de pruebas omitidas: 96</span><span class="sxs-lookup"><span data-stu-id="058f0-721">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="058f0-722">Los registros de ejecución de pruebas LTP</span><span class="sxs-lookup"><span data-stu-id="058f0-722">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="058f0-723">Compilación 16241</span><span class="sxs-lookup"><span data-stu-id="058f0-723">Build 16241</span></span>

<span data-ttu-id="058f0-724">Para Windows general, visite información sobre las compilación 16241 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span><span class="sxs-lookup"><span data-stu-id="058f0-724">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-725">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-725">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="058f0-726">WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-726">WSL</span></span>
- <span data-ttu-id="058f0-727">No hay WSL otros cambios relacionados en esta versión.</span><span class="sxs-lookup"><span data-stu-id="058f0-727">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="058f0-728">Console</span><span class="sxs-lookup"><span data-stu-id="058f0-728">Console</span></span>
- <span data-ttu-id="058f0-729">Corrección para generar el carácter incorrecto para las líneas de cruce DEC, notifican originalmente [aquí](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span><span class="sxs-lookup"><span data-stu-id="058f0-729">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="058f0-730">Corrección para ningún texto de salida que se muestra en la página de códigos 65001 (utf8)</span><span class="sxs-lookup"><span data-stu-id="058f0-730">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="058f0-731">No se transfieren los cambios realizados en los valores RGB de un color a otras partes de la paleta de cambio de selección.</span><span class="sxs-lookup"><span data-stu-id="058f0-731">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="058f0-732">Esto hará que la hoja de propiedades de la consola mucho más fáciles de usar.</span><span class="sxs-lookup"><span data-stu-id="058f0-732">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="058f0-733">CTRL + S parece no funcionar correctamente</span><span class="sxs-lookup"><span data-stu-id="058f0-733">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="058f0-734">Sin negrita /-Dim completamente está ausente de códigos de escape ANSI [GH 2174]</span><span class="sxs-lookup"><span data-stu-id="058f0-734">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="058f0-735">Consola correctamente no es compatible con temas de color Vim [GH 1706]</span><span class="sxs-lookup"><span data-stu-id="058f0-735">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="058f0-736">No se puede pegar el juego de caracteres determinado [GH 2149]</span><span class="sxs-lookup"><span data-stu-id="058f0-736">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="058f0-737">Cambio de tamaño de reflujo forma extraña interactúa con el tamaño de una ventana de bash al material está en la línea de comando/Editar [GH ConEmu 1123]</span><span class="sxs-lookup"><span data-stu-id="058f0-737">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="058f0-738">CTRL-L deja la pantalla desfasada [GH 1978]</span><span class="sxs-lookup"><span data-stu-id="058f0-738">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="058f0-739">Errores de representación de consola al mostrar VT en HDPI [GH 1907]</span><span class="sxs-lookup"><span data-stu-id="058f0-739">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="058f0-740">Caracteres Japansese parezca extraños con el carácter Unicode U + 30FB [GH 2146]</span><span class="sxs-lookup"><span data-stu-id="058f0-740">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="058f0-741">Otras mejoras y correcciones de errores</span><span class="sxs-lookup"><span data-stu-id="058f0-741">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="058f0-742">Compilación 16237</span><span class="sxs-lookup"><span data-stu-id="058f0-742">Build 16237</span></span>

<span data-ttu-id="058f0-743">Para Windows general, visite información sobre las compilación 16237 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span><span class="sxs-lookup"><span data-stu-id="058f0-743">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-744">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-744">Fixed</span></span>
- <span data-ttu-id="058f0-745">Utilice los atributos predeterminados para los archivos sin EAs de lxfs (raíz, raíz, 0000)</span><span class="sxs-lookup"><span data-stu-id="058f0-745">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="058f0-746">Se agregó compatibilidad para las distribuciones que usan los atributos extendidos</span><span class="sxs-lookup"><span data-stu-id="058f0-746">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="058f0-747">Relleno de corrección para las entradas devueltas por getdents y getdents64</span><span class="sxs-lookup"><span data-stu-id="058f0-747">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="058f0-748">Corregir la comprobación de permisos para la llamada del sistema SHM_STAT shmctl [GH 2068]</span><span class="sxs-lookup"><span data-stu-id="058f0-748">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="058f0-749">Estado fijo epoll inicial incorrecto para los TTY [GH 2231]</span><span class="sxs-lookup"><span data-stu-id="058f0-749">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="058f0-750">Corregir readdir DrvFs no devuelve todas las entradas [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="058f0-750">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="058f0-751">Corregir LxFs readdir cuando hay archivos desvincula [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="058f0-751">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="058f0-752">Permitir que los archivos no vinculados drvfs abrirse de nuevo a través de procfs</span><span class="sxs-lookup"><span data-stu-id="058f0-752">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="058f0-753">Agrega el reemplazo de la clave del registro global para deshabilitar las características WSL (interoperabilidad / montaje de unidad)</span><span class="sxs-lookup"><span data-stu-id="058f0-753">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="058f0-754">Corregir el recuento de bloque incorrecta en "DO" DrvFs (y LxFs) [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="058f0-754">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="058f0-755">Otras mejoras y correcciones de errores</span><span class="sxs-lookup"><span data-stu-id="058f0-755">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="058f0-756">Compilación 16232</span><span class="sxs-lookup"><span data-stu-id="058f0-756">Build 16232</span></span>

<span data-ttu-id="058f0-757">Para Windows general, visite información sobre las compilación 16232 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span><span class="sxs-lookup"><span data-stu-id="058f0-757">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-758">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-758">Fixed</span></span>
- <span data-ttu-id="058f0-759">No hay WSL otros cambios relacionados en esta versión.</span><span class="sxs-lookup"><span data-stu-id="058f0-759">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="058f0-760">Compilación 16226</span><span class="sxs-lookup"><span data-stu-id="058f0-760">Build 16226</span></span>

<span data-ttu-id="058f0-761">Para Windows general, visite información sobre las compilación 16226 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span><span class="sxs-lookup"><span data-stu-id="058f0-761">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-762">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-762">Fixed</span></span>
- <span data-ttu-id="058f0-763">xattr relacionados con la compatibilidad de syscall (getxattr, setxattr, listxattr, removexattr).</span><span class="sxs-lookup"><span data-stu-id="058f0-763">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="058f0-764">soporte técnico de xattr Security.capablity.</span><span class="sxs-lookup"><span data-stu-id="058f0-764">security.capablity xattr support.</span></span>
- <span data-ttu-id="058f0-765">Compatibilidad mejorada con ciertos sistemas de archivos y filtros, incluidos los servidores SMB que no son MS.</span><span class="sxs-lookup"><span data-stu-id="058f0-765">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="058f0-766">[GH #1952]</span><span class="sxs-lookup"><span data-stu-id="058f0-766">[GH #1952]</span></span>
- <span data-ttu-id="058f0-767">Compatibilidad mejorada para los marcadores de posición de OneDrive, los marcadores de posición GVFS y OS Compact archivos comprimidos.</span><span class="sxs-lookup"><span data-stu-id="058f0-767">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="058f0-768">Otras mejoras y correcciones de errores</span><span class="sxs-lookup"><span data-stu-id="058f0-768">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="058f0-769">Compilación 16215</span><span class="sxs-lookup"><span data-stu-id="058f0-769">Build 16215</span></span>

<span data-ttu-id="058f0-770">Para Windows general, visite información sobre las compilación 16215 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span><span class="sxs-lookup"><span data-stu-id="058f0-770">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-771">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-771">Fixed</span></span>
- <span data-ttu-id="058f0-772">WSL ya no requiere el modo de programador.</span><span class="sxs-lookup"><span data-stu-id="058f0-772">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="058f0-773">Admite a las uniones de directorio en drvfs.</span><span class="sxs-lookup"><span data-stu-id="058f0-773">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="058f0-774">Controlar la desinstalación de paquetes appx de distribución de WSL.</span><span class="sxs-lookup"><span data-stu-id="058f0-774">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="058f0-775">Actualización procfs mostrar privada y compartir asignaciones.</span><span class="sxs-lookup"><span data-stu-id="058f0-775">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="058f0-776">Agregue capacidad para wslconfig.exe limpiar las distribuciones que se instalan o desinstalan de parcialmente.</span><span class="sxs-lookup"><span data-stu-id="058f0-776">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="058f0-777">Se agregó compatibilidad para IP_MTU_DISCOVER para los sockets TCP.</span><span class="sxs-lookup"><span data-stu-id="058f0-777">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="058f0-778">[GH 1639, 2115, 2205]</span><span class="sxs-lookup"><span data-stu-id="058f0-778">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="058f0-779">Inferir la familia de protocolos para que las rutas AF_INADDR.</span><span class="sxs-lookup"><span data-stu-id="058f0-779">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="058f0-780">Mejoras de dispositivo en serie [GH 1929].</span><span class="sxs-lookup"><span data-stu-id="058f0-780">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="058f0-781">Compilación 16199</span><span class="sxs-lookup"><span data-stu-id="058f0-781">Build 16199</span></span>

<span data-ttu-id="058f0-782">Para Windows general, visite información sobre las compilación 16199 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span><span class="sxs-lookup"><span data-stu-id="058f0-782">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-783">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-783">Fixed</span></span>
- <span data-ttu-id="058f0-784">No hay WSL otros cambios relacionados en estas versiones.</span><span class="sxs-lookup"><span data-stu-id="058f0-784">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="058f0-785">Compilación 16193</span><span class="sxs-lookup"><span data-stu-id="058f0-785">Build 16193</span></span>

<span data-ttu-id="058f0-786">Para Windows general, visite información sobre las compilación 16193 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span><span class="sxs-lookup"><span data-stu-id="058f0-786">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-787">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-787">Fixed</span></span>
- <span data-ttu-id="058f0-788">Condición de carrera entre el envío SIGCONT y un threadgroup terminación [GH 1973]</span><span class="sxs-lookup"><span data-stu-id="058f0-788">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="058f0-789">cambiar dispositivos tty y pty al informe FILE_DEVICE_NAMED_PIPE en lugar de FILE_DEVICE_CONSOLE [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="058f0-789">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="058f0-790">Corrección SSH para IP_OPTIONS</span><span class="sxs-lookup"><span data-stu-id="058f0-790">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="058f0-791">Mover DrvFs montaje a init daemon [GH 1862, 1968, 1767, 1933]</span><span class="sxs-lookup"><span data-stu-id="058f0-791">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="058f0-792">Se agregó compatibilidad en DrvFs para seguir los vínculos simbólicos de NT.</span><span class="sxs-lookup"><span data-stu-id="058f0-792">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="058f0-793">Compilación 16184</span><span class="sxs-lookup"><span data-stu-id="058f0-793">Build 16184</span></span>

<span data-ttu-id="058f0-794">Para Windows general, visite información sobre las compilación 16184 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span><span class="sxs-lookup"><span data-stu-id="058f0-794">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-795">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-795">Fixed</span></span>
- <span data-ttu-id="058f0-796">Quita la tarea de mantenimiento de paquetes apt (lxrun.exe /update)</span><span class="sxs-lookup"><span data-stu-id="058f0-796">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="058f0-797">Salida con formato fijo no aparece en de los procesos de Windows en node.js [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="058f0-797">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="058f0-798">Relaje los requisitos de alineación en lxcore [GH 1794]</span><span class="sxs-lookup"><span data-stu-id="058f0-798">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="058f0-799">Se corrigió el control de la marca AT_EMPTY_PATH en un número de llamadas del sistema.</span><span class="sxs-lookup"><span data-stu-id="058f0-799">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="058f0-800">Se corrigió un problema donde eliminando archivos DrvFs con identificadores abiertos hará que el archivo de un comportamiento indefinido [GH 544,966,1357,1535,1615]</span><span class="sxs-lookup"><span data-stu-id="058f0-800">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="058f0-801">/ etcetera/hosts heredarán las entradas del archivo de hosts de Windows (% windir%\system32\drivers\etc\hosts) [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="058f0-801">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="058f0-802">Compilación 16179</span><span class="sxs-lookup"><span data-stu-id="058f0-802">Build 16179</span></span>

<span data-ttu-id="058f0-803">Para Windows general, visite información sobre las compilación 16179 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span><span class="sxs-lookup"><span data-stu-id="058f0-803">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-804">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-804">Fixed</span></span>
- <span data-ttu-id="058f0-805">No hay cambios WSL esta semana.</span><span class="sxs-lookup"><span data-stu-id="058f0-805">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="058f0-806">Compilación 16176</span><span class="sxs-lookup"><span data-stu-id="058f0-806">Build 16176</span></span>

<span data-ttu-id="058f0-807">Para Windows general, visite información sobre las compilación 16176 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span><span class="sxs-lookup"><span data-stu-id="058f0-807">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-808">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-808">Fixed</span></span>

- [<span data-ttu-id="058f0-809">Habilita la compatibilidad con puerto serie</span><span class="sxs-lookup"><span data-stu-id="058f0-809">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="058f0-810">Opción de socket IP se ha agregado IP_OPTIONS [GH 1116]</span><span class="sxs-lookup"><span data-stu-id="058f0-810">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="058f0-811">Implementa la función pwritev (al cargar el archivo a nginx/PHP-FPM) [GH 1506]</span><span class="sxs-lookup"><span data-stu-id="058f0-811">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="058f0-812">Se han agregado opciones de socket IP IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span><span class="sxs-lookup"><span data-stu-id="058f0-812">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="058f0-813">Soporte técnico para la opción de socket IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="058f0-813">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="058f0-814">Se ha agregado la opción de socket _MTU IP (V6) para el nodo aplicaciones, traceroute, investigue, nslookup, host</span><span class="sxs-lookup"><span data-stu-id="058f0-814">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="058f0-815">Opción de socket IP se ha agregado IPV6_UNICAST_HOPS</span><span class="sxs-lookup"><span data-stu-id="058f0-815">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="058f0-816">Mejoras del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="058f0-816">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="058f0-817">Permite el montaje de las rutas de acceso UNC</span><span class="sxs-lookup"><span data-stu-id="058f0-817">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="058f0-818">Habilitar la compatibilidad con CDFS en drvfs</span><span class="sxs-lookup"><span data-stu-id="058f0-818">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="058f0-819">Controlar correctamente los permisos para los sistemas de archivos de red en drvfs</span><span class="sxs-lookup"><span data-stu-id="058f0-819">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="058f0-820">Agregar compatibilidad para unidades remotas a drvfs</span><span class="sxs-lookup"><span data-stu-id="058f0-820">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="058f0-821">Habilitar FAT admitir en drvfs</span><span class="sxs-lookup"><span data-stu-id="058f0-821">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="058f0-822">Mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="058f0-822">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-823">LTP resultados</span><span class="sxs-lookup"><span data-stu-id="058f0-823">LTP Results</span></span>
<span data-ttu-id="058f0-824">Ningún cambio desde 15042</span><span class="sxs-lookup"><span data-stu-id="058f0-824">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="058f0-825">Compilación 16170</span><span class="sxs-lookup"><span data-stu-id="058f0-825">Build 16170</span></span>

<span data-ttu-id="058f0-826">Para Windows general, visite información sobre las compilación 16170 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span><span class="sxs-lookup"><span data-stu-id="058f0-826">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="058f0-827">Hemos lanzado una nueva [entrada de blog](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discutir nuestros esfuerzos para probar WSL.</span><span class="sxs-lookup"><span data-stu-id="058f0-827">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="058f0-828">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-828">Fixed</span></span>

- <span data-ttu-id="058f0-829">Socket de compatibilidad con la opción IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="058f0-829">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="058f0-830">Agregar compatibilidad con PTRACE_OLDSETOPTIONS.</span><span class="sxs-lookup"><span data-stu-id="058f0-830">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="058f0-831">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="058f0-831">[GH 1692]</span></span>
- <span data-ttu-id="058f0-832">Las mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="058f0-832">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-833">LTP resultados</span><span class="sxs-lookup"><span data-stu-id="058f0-833">LTP Results</span></span>
<span data-ttu-id="058f0-834">Ningún cambio desde 15042</span><span class="sxs-lookup"><span data-stu-id="058f0-834">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="058f0-835">Compilar 15046 a Windows 10 Creators Update</span><span class="sxs-lookup"><span data-stu-id="058f0-835">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="058f0-836">Hay más no WSL correcciones o las características planeadas para su inclusión en Windows 10 Creators Update.</span><span class="sxs-lookup"><span data-stu-id="058f0-836">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="058f0-837">Notas de WSL se reanudación en las próximas semanas para adiciones destinadas a la siguiente actualización principal de Windows.</span><span class="sxs-lookup"><span data-stu-id="058f0-837">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="058f0-838">Para Windows general información sobre la compilación 15046 y especialista en futuras versiones visita la [Blog Windows](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span><span class="sxs-lookup"><span data-stu-id="058f0-838">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="058f0-839">Compilación 15042</span><span class="sxs-lookup"><span data-stu-id="058f0-839">Build 15042</span></span>

<span data-ttu-id="058f0-840">Para Windows general, visite información sobre las compilación 15042 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span><span class="sxs-lookup"><span data-stu-id="058f0-840">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-841">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-841">Fixed</span></span>

- <span data-ttu-id="058f0-842">Corrección de un interbloqueo cuando se quita una ruta de acceso que terminen en ".."</span><span class="sxs-lookup"><span data-stu-id="058f0-842">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="058f0-843">Se ha corregido un problema donde FIONBIO no devuelve 0 si se ejecuta correctamente [GH 1683]</span><span class="sxs-lookup"><span data-stu-id="058f0-843">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="058f0-844">Se corrigió un problema con lecturas de longitud cero de sockets de datagrama inet</span><span class="sxs-lookup"><span data-stu-id="058f0-844">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="058f0-845">Corregir posibles interbloqueos debido a la condición de carrera en la búsqueda de inode drvfs [GH 1675]</span><span class="sxs-lookup"><span data-stu-id="058f0-845">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="058f0-846">Compatibilidad ampliada para datos auxiliares de socket de unix; SCM_CREDENTIALS y SCM_RIGHTS [GH 514, 613, 1326]</span><span class="sxs-lookup"><span data-stu-id="058f0-846">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="058f0-847">Las mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="058f0-847">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-848">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-848">LTP Results:</span></span>
<span data-ttu-id="058f0-849">Número de paso de prueba: 737</span><span class="sxs-lookup"><span data-stu-id="058f0-849">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="058f0-850">Número de paso de no (por error, omitido, etcetera...): 255</span><span class="sxs-lookup"><span data-stu-id="058f0-850">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="058f0-851">Compilación 15031</span><span class="sxs-lookup"><span data-stu-id="058f0-851">Build 15031</span></span>

<span data-ttu-id="058f0-852">Para Windows general, visite información sobre las compilación 15031 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span><span class="sxs-lookup"><span data-stu-id="058f0-852">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-853">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-853">Fixed</span></span>

- <span data-ttu-id="058f0-854">Se ha corregido un error donde se comportará incorrectamente esporádicamente time(2).</span><span class="sxs-lookup"><span data-stu-id="058f0-854">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="058f0-855">Se ha corregido y emitir where \* SIGPROCMASK syscalls podría dañar la máscara de señal.</span><span class="sxs-lookup"><span data-stu-id="058f0-855">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="058f0-856">Longitud de línea de comandos completa se devuelven ahora en la notificación de la creación del proceso WSL.</span><span class="sxs-lookup"><span data-stu-id="058f0-856">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="058f0-857">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="058f0-857">[GH 1632]</span></span>
- <span data-ttu-id="058f0-858">WSL ahora informa salir del subproceso a través de ptrace GDB bloqueos.</span><span class="sxs-lookup"><span data-stu-id="058f0-858">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="058f0-859">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="058f0-859">[GH 1196]</span></span>
- <span data-ttu-id="058f0-860">Se corrigió el error donde ptys dejaba de responder después tmux mucha E/S.</span><span class="sxs-lookup"><span data-stu-id="058f0-860">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="058f0-861">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="058f0-861">[GH 1358]</span></span>
- <span data-ttu-id="058f0-862">Validación de tiempo de espera fijo muchas llamadas del sistema (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span><span class="sxs-lookup"><span data-stu-id="058f0-862">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="058f0-863">Se ha agregado eventfd EFD_SEMAPHORE soporte [GH 452]</span><span class="sxs-lookup"><span data-stu-id="058f0-863">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="058f0-864">Las mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="058f0-864">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-865">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-865">LTP Results:</span></span>
<span data-ttu-id="058f0-866">Número de paso de prueba: 737</span><span class="sxs-lookup"><span data-stu-id="058f0-866">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="058f0-867">Número de paso de no (por error, omitido, etcetera...): 255</span><span class="sxs-lookup"><span data-stu-id="058f0-867">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="058f0-868">Los registros de ejecución de pruebas LTP</span><span class="sxs-lookup"><span data-stu-id="058f0-868">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="058f0-869">Compilación 15025</span><span class="sxs-lookup"><span data-stu-id="058f0-869">Build 15025</span></span>

<span data-ttu-id="058f0-870">Para Windows general, visite información sobre las compilación 15025 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span><span class="sxs-lookup"><span data-stu-id="058f0-870">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-871">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-871">Fixed</span></span>

- <span data-ttu-id="058f0-872">Corrección de errores que grep roto 2,27 [GH 1578]</span><span class="sxs-lookup"><span data-stu-id="058f0-872">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="058f0-873">Marca EFD_SEMAPHORE implementada para eventfd2 syscall [GH 452]</span><span class="sxs-lookup"><span data-stu-id="058f0-873">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="058f0-874">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="058f0-874">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="058f0-875">Señal controlado por compatibilidad con E/S sockets de secuencias de unix [GH 393, 68]</span><span class="sxs-lookup"><span data-stu-id="058f0-875">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="058f0-876">Admitir F_GETPIPE_SZ y F_SETPIPE_SZ [GH 1012]</span><span class="sxs-lookup"><span data-stu-id="058f0-876">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="058f0-877">Implement recvmmsg() syscall [GH 1531]</span><span class="sxs-lookup"><span data-stu-id="058f0-877">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="058f0-878">Se corrigió el error donde epoll_wait() no estaba esperando [GH 1609]</span><span class="sxs-lookup"><span data-stu-id="058f0-878">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="058f0-879">Implement /proc/version_signature</span><span class="sxs-lookup"><span data-stu-id="058f0-879">Implement /proc/version_signature</span></span>
- <span data-ttu-id="058f0-880">Tee syscall ahora devuelve un error si ambos descriptores de archivo hace referencia a la misma canalización</span><span class="sxs-lookup"><span data-stu-id="058f0-880">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="058f0-881">Implementa el comportamiento correcto para SO_PEERCRED para sockets de Unix</span><span class="sxs-lookup"><span data-stu-id="058f0-881">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="058f0-882">Control de parámetros no válidos de syscall tkill fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-882">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="058f0-883">Cambios para aumentar la preformace de drvfs</span><span class="sxs-lookup"><span data-stu-id="058f0-883">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="058f0-884">Revisión secundaria para el bloqueo de E/S de Ruby</span><span class="sxs-lookup"><span data-stu-id="058f0-884">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="058f0-885">Fijo recvmsg() devolver EINVAL para el indicador MSG_DONTWAIT para sockets inet [GH 1296]</span><span class="sxs-lookup"><span data-stu-id="058f0-885">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="058f0-886">Las mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="058f0-886">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-887">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-887">LTP Results:</span></span>
<span data-ttu-id="058f0-888">Número de paso de prueba: 732</span><span class="sxs-lookup"><span data-stu-id="058f0-888">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="058f0-889">Número de paso de no (por error, omitido, etcetera...): 255</span><span class="sxs-lookup"><span data-stu-id="058f0-889">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="058f0-890">Los registros de ejecución de pruebas LTP</span><span class="sxs-lookup"><span data-stu-id="058f0-890">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="058f0-891">Compilación 15019</span><span class="sxs-lookup"><span data-stu-id="058f0-891">Build 15019</span></span>

<span data-ttu-id="058f0-892">Para Windows general, visite información sobre las compilación 15019 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span><span class="sxs-lookup"><span data-stu-id="058f0-892">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-893">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-893">Fixed</span></span>

- <span data-ttu-id="058f0-894">Se corrigió el error que se informaba incorrectamente de uso de CPU en procfs para herramientas como htop (GH 823, 945, 971)</span><span class="sxs-lookup"><span data-stu-id="058f0-894">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="058f0-895">Al llamar a open() con O_TRUNC en un archivo inotify genera ahora IN_MODIFY antes IN_OPEN</span><span class="sxs-lookup"><span data-stu-id="058f0-895">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="058f0-896">Correcciones de socket de unix getsockopt SO_ERROR para habilitar postgress [GH 61, 1354]</span><span class="sxs-lookup"><span data-stu-id="058f0-896">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="058f0-897">Implementar /proc/sys/net/core/somaxconn para el lenguaje GO</span><span class="sxs-lookup"><span data-stu-id="058f0-897">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="058f0-898">Tarea en segundo plano de actualización de paquetes APT-get ahora se ejecuta oculto de la vista</span><span class="sxs-lookup"><span data-stu-id="058f0-898">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="058f0-899">Ámbito clara para el host local de ipv6 (error Spring-Framework(Java)).</span><span class="sxs-lookup"><span data-stu-id="058f0-899">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="058f0-900">Las mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="058f0-900">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-901">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-901">LTP Results:</span></span>
<span data-ttu-id="058f0-902">Número de paso de prueba: 714</span><span class="sxs-lookup"><span data-stu-id="058f0-902">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="058f0-903">Número de paso de no (por error, omitido, etcetera...): 249</span><span class="sxs-lookup"><span data-stu-id="058f0-903">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="058f0-904">Los registros de ejecución de pruebas LTP</span><span class="sxs-lookup"><span data-stu-id="058f0-904">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="058f0-905">Compilación 15014</span><span class="sxs-lookup"><span data-stu-id="058f0-905">Build 15014</span></span>

<span data-ttu-id="058f0-906">Para Windows general, visite información sobre las compilación 15014 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="058f0-906">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-907">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-907">Fixed</span></span>

- <span data-ttu-id="058f0-908">CTRL + C ahora funciona según lo previsto</span><span class="sxs-lookup"><span data-stu-id="058f0-908">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="058f0-909">htop y ps auxw ahora mostrar correcto uso de recursos (GH #516)</span><span class="sxs-lookup"><span data-stu-id="058f0-909">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="058f0-910">Traducción básica de excepciones de NT a las señales.</span><span class="sxs-lookup"><span data-stu-id="058f0-910">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="058f0-911">(GH 513 #)</span><span class="sxs-lookup"><span data-stu-id="058f0-911">(GH #513)</span></span>
- <span data-ttu-id="058f0-912">fallocate ahora produce ENOSPC cuando se está quedando sin espacio en lugar de EINVAL (GH #1571)</span><span class="sxs-lookup"><span data-stu-id="058f0-912">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="058f0-913">Se ha agregado /proc/sys/kernel/sem.</span><span class="sxs-lookup"><span data-stu-id="058f0-913">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="058f0-914">Llamadas al sistema semop y semtimedop implementadas</span><span class="sxs-lookup"><span data-stu-id="058f0-914">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="058f0-915">Errores de nslookup fijo con la opción de socket IP_RECVTOS & IPV6_RECVTCLASS (GH 69)</span><span class="sxs-lookup"><span data-stu-id="058f0-915">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="058f0-916">Compatibilidad con las opciones de socket IP_RECVTTL y IPV6_RECVHOPLIMIT</span><span class="sxs-lookup"><span data-stu-id="058f0-916">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="058f0-917">Las mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="058f0-917">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-918">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-918">LTP Results:</span></span>
<span data-ttu-id="058f0-919">Número de paso de prueba: 709</span><span class="sxs-lookup"><span data-stu-id="058f0-919">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="058f0-920">Número de paso de no (por error, omitido, etcetera...): 255</span><span class="sxs-lookup"><span data-stu-id="058f0-920">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="058f0-921">Los registros de ejecución de pruebas LTP</span><span class="sxs-lookup"><span data-stu-id="058f0-921">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="058f0-922">Resumen de syscall</span><span class="sxs-lookup"><span data-stu-id="058f0-922">Syscall Summary</span></span>
<span data-ttu-id="058f0-923">Syscall total: 384</span><span class="sxs-lookup"><span data-stu-id="058f0-923">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="058f0-924">Total implementado: 235</span><span class="sxs-lookup"><span data-stu-id="058f0-924">Total Implemented: 235</span></span> </br>
<span data-ttu-id="058f0-925">Total que se procesó con stub: 22</span><span class="sxs-lookup"><span data-stu-id="058f0-925">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="058f0-926">Total sin implementar: 127</span><span class="sxs-lookup"><span data-stu-id="058f0-926">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="058f0-927">Desglose detallado</span><span class="sxs-lookup"><span data-stu-id="058f0-927">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="058f0-928">Compilación 15007</span><span class="sxs-lookup"><span data-stu-id="058f0-928">Build 15007</span></span>

<span data-ttu-id="058f0-929">Para Windows general, visite información sobre las compilación 15007 el [Blog Windows]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span><span class="sxs-lookup"><span data-stu-id="058f0-929">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="058f0-930">Problema conocido</span><span class="sxs-lookup"><span data-stu-id="058f0-930">Known Issue</span></span>

- <span data-ttu-id="058f0-931">Hay un problema conocido en la consola no reconoce algunos Ctrl + <key> entrada.</span><span class="sxs-lookup"><span data-stu-id="058f0-931">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="058f0-932">Esto incluye el comando ctrl-c que actuará como una pulsación de tecla 'c' normal.</span><span class="sxs-lookup"><span data-stu-id="058f0-932">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="058f0-933">Solución: Asignar una clave alternativa a Ctrl + C.</span><span class="sxs-lookup"><span data-stu-id="058f0-933">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="058f0-934">Por ejemplo, para asignar Ctrl + K para Ctrl + C lo: `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="058f0-934">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="058f0-935">Esta asignación es por terminal y tendrá que realizarse *cada* bash de tiempo se inicia.</span><span class="sxs-lookup"><span data-stu-id="058f0-935">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="058f0-936">Los usuarios pueden explorar la opción para incluir esto en su</span><span class="sxs-lookup"><span data-stu-id="058f0-936">Users can explore the option to include this in their</span></span> `.bashrc`

### <a name="fixed"></a><span data-ttu-id="058f0-937">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-937">Fixed</span></span>

- <span data-ttu-id="058f0-938">Se ha corregido el problema donde ejecutando WSL consumiría 100% de un núcleo de CPU</span><span class="sxs-lookup"><span data-stu-id="058f0-938">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="058f0-939">Opción IP_PKTINFO, IPV6_RECVPKTINFO ahora admitidos de socket.</span><span class="sxs-lookup"><span data-stu-id="058f0-939">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="058f0-940">(GH #851, 987)</span><span class="sxs-lookup"><span data-stu-id="058f0-940">(GH #851, 987)</span></span>
- <span data-ttu-id="058f0-941">Truncar la dirección física de interfaz de red a lxcore de 16 bytes (# GH 1452, 1414, 1343, 468, 308)</span><span class="sxs-lookup"><span data-stu-id="058f0-941">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="058f0-942">Las mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="058f0-942">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-943">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-943">LTP Results:</span></span>
<span data-ttu-id="058f0-944">Número de paso de prueba: 709</span><span class="sxs-lookup"><span data-stu-id="058f0-944">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="058f0-945">Número de paso de no (por error, omitido, etcetera...): 255</span><span class="sxs-lookup"><span data-stu-id="058f0-945">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="058f0-946">Los registros de ejecución de pruebas LTP</span><span class="sxs-lookup"><span data-stu-id="058f0-946">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="058f0-947">Compilación 15002</span><span class="sxs-lookup"><span data-stu-id="058f0-947">Build 15002</span></span>

<span data-ttu-id="058f0-948">Para Windows general, visite información sobre las compilación 15002 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span><span class="sxs-lookup"><span data-stu-id="058f0-948">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="058f0-949">Problema conocido</span><span class="sxs-lookup"><span data-stu-id="058f0-949">Known Issue</span></span>

<span data-ttu-id="058f0-950">Dos problemas conocidos:</span><span class="sxs-lookup"><span data-stu-id="058f0-950">Two known issues:</span></span>
- <span data-ttu-id="058f0-951">Hay un problema conocido en la consola no reconoce algunos Ctrl + <key> entrada.</span><span class="sxs-lookup"><span data-stu-id="058f0-951">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="058f0-952">Esto incluye el comando ctrl-c que actuará como una pulsación de tecla 'c' normal.</span><span class="sxs-lookup"><span data-stu-id="058f0-952">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="058f0-953">Solución: Asignar una clave alternativa a Ctrl + C.</span><span class="sxs-lookup"><span data-stu-id="058f0-953">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="058f0-954">Por ejemplo, para asignar Ctrl + K para Ctrl + C lo: `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="058f0-954">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="058f0-955">Esta asignación es por terminal y tendrá que realizarse *cada* bash de tiempo se inicia.</span><span class="sxs-lookup"><span data-stu-id="058f0-955">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="058f0-956">Los usuarios pueden explorar la opción para incluir esto en su</span><span class="sxs-lookup"><span data-stu-id="058f0-956">Users can explore the option to include this in their</span></span> `.bashrc`

- <span data-ttu-id="058f0-957">Mientras se está ejecutando WSL un subproceso del sistema consume el 100% de un núcleo de CPU.</span><span class="sxs-lookup"><span data-stu-id="058f0-957">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="058f0-958">Abordar la causa raíz y se ha corregido internamente.</span><span class="sxs-lookup"><span data-stu-id="058f0-958">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="058f0-959">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-959">Fixed</span></span>

- <span data-ttu-id="058f0-960">Todas las sesiones de bash ahora deben crearse en el mismo nivel de permiso.</span><span class="sxs-lookup"><span data-stu-id="058f0-960">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="058f0-961">Se bloqueará al intentar iniciar una sesión en un nivel diferente.</span><span class="sxs-lookup"><span data-stu-id="058f0-961">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="058f0-962">Esto significa que las consolas de administrador y que no es administrador no se pueden ejecutar al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="058f0-962">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="058f0-963">(GH 626 #)</span><span class="sxs-lookup"><span data-stu-id="058f0-963">(GH #626)</span></span>
<br/>
- <span data-ttu-id="058f0-964">Implementa los siguientes mensajes NETLINK_ROUTE (requiere un administrador de Windows)</span><span class="sxs-lookup"><span data-stu-id="058f0-964">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="058f0-965">RTM_NEWADDR (admite `ip addr add`)</span><span class="sxs-lookup"><span data-stu-id="058f0-965">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="058f0-966">RTM_NEWROUTE (admite `ip route add`)</span><span class="sxs-lookup"><span data-stu-id="058f0-966">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="058f0-967">RTM_DELADDR (admite `ip addr del`)</span><span class="sxs-lookup"><span data-stu-id="058f0-967">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="058f0-968">RTM_DELROUTE (admite `ip route del`)</span><span class="sxs-lookup"><span data-stu-id="058f0-968">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="058f0-969">Comprobación de paquetes para actualizar de tarea programada ya no se ejecutará en una conexión de uso medido (GH #1371)</span><span class="sxs-lookup"><span data-stu-id="058f0-969">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="058f0-970">Se ha corregido error donde canalización obtiene; es decir, bloqueada bash - c "ls - alR /" | Bash -c "cat" (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="058f0-970">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="058f0-971">Opción de socket TCP_KEEPCNT implementada (GH #843)</span><span class="sxs-lookup"><span data-stu-id="058f0-971">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="058f0-972">Opción de socket IP_MTU_DISCOVER INET implementada (720 de # GH, 717, 170, 69)</span><span class="sxs-lookup"><span data-stu-id="058f0-972">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="058f0-973">Quita la funcionalidad heredada para ejecutar los archivos binarios de NT de init con búsqueda de ruta de acceso de NT.</span><span class="sxs-lookup"><span data-stu-id="058f0-973">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="058f0-974">(GH 1325 #)</span><span class="sxs-lookup"><span data-stu-id="058f0-974">(GH #1325)</span></span>
- <span data-ttu-id="058f0-975">Corregir el modo de/dev/kmsg para permitir el acceso de lectura de grupo / otro (0644) (GH #1321)</span><span class="sxs-lookup"><span data-stu-id="058f0-975">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="058f0-976">/Proc/sys/kernel/random/uuid implementada (GH #1092)</span><span class="sxs-lookup"><span data-stu-id="058f0-976">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="058f0-977">Se ha corregido el error que mostraba el tiempo de inicio de proceso como año 2432 (GH #974)</span><span class="sxs-lookup"><span data-stu-id="058f0-977">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="058f0-978">Variable de entorno de término predeterminado se ha cambiado a xterm-256color (GH #1446)</span><span class="sxs-lookup"><span data-stu-id="058f0-978">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="058f0-979">Modificado la forma en que el proceso de confirmación se calcula durante la bifurcación de proceso.</span><span class="sxs-lookup"><span data-stu-id="058f0-979">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="058f0-980">(GH 1286 #)</span><span class="sxs-lookup"><span data-stu-id="058f0-980">(GH #1286)</span></span>
- <span data-ttu-id="058f0-981">Implemented /proc/sys/vm/overcommit_memory.</span><span class="sxs-lookup"><span data-stu-id="058f0-981">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="058f0-982">(GH 1286 #)</span><span class="sxs-lookup"><span data-stu-id="058f0-982">(GH #1286)</span></span>
- <span data-ttu-id="058f0-983">Archivo implementado /proc/net/route (GH #69)</span><span class="sxs-lookup"><span data-stu-id="058f0-983">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="058f0-984">Error corregido donde estaba incorrectamente el nombre de método abreviado localizado (GH #696)</span><span class="sxs-lookup"><span data-stu-id="058f0-984">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="058f0-985">Elf fijo lógica que se está validando incorrectamente los encabezados del programa de análisis debe ser menor que (o igual que) PATH_MAX.</span><span class="sxs-lookup"><span data-stu-id="058f0-985">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="058f0-986">(GH 1048 #)</span><span class="sxs-lookup"><span data-stu-id="058f0-986">(GH #1048)</span></span>
- <span data-ttu-id="058f0-987">Devolución de llamada implementada statfs procfs, sysfs, cgroupfs y binfmtfs (GH #1378)</span><span class="sxs-lookup"><span data-stu-id="058f0-987">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="058f0-988">Windows AptPackageIndexUpdate fija que no se cierran (1184 de # de GH, también se describen en GH #1193)</span><span class="sxs-lookup"><span data-stu-id="058f0-988">Fixed AptPackageIndexUpdate windows that won’t close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="058f0-989">Personalidad ASLR se ha agregado compatibilidad con ADDR_NO_RANDOMIZE.</span><span class="sxs-lookup"><span data-stu-id="058f0-989">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="058f0-990">(GH #1148, 1128)</span><span class="sxs-lookup"><span data-stu-id="058f0-990">(GH #1148, 1128)</span></span>
- <span data-ttu-id="058f0-991">PTRACE_GETSIGINFO mejorada, SIGSEGV para seguimientos de pila gdb adecuado durante AV (GH #875)</span><span class="sxs-lookup"><span data-stu-id="058f0-991">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="058f0-992">ELF análisis ya no se produce un error para los binarios de patchelf.</span><span class="sxs-lookup"><span data-stu-id="058f0-992">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="058f0-993">(GH 471 #)</span><span class="sxs-lookup"><span data-stu-id="058f0-993">(GH #471)</span></span>
- <span data-ttu-id="058f0-994">VPN DNS se propaguen a /etc/resolv.conf (GH #416, 1350)</span><span class="sxs-lookup"><span data-stu-id="058f0-994">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="058f0-995">Cierre las mejoras de TCP para la transferencia de datos más confiable.</span><span class="sxs-lookup"><span data-stu-id="058f0-995">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="058f0-996">(GH #610, 616, 1025, 1335)</span><span class="sxs-lookup"><span data-stu-id="058f0-996">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="058f0-997">Ahora un resultado correcto de código de error cuando hay demasiados archivos abierto (EMFILE).</span><span class="sxs-lookup"><span data-stu-id="058f0-997">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="058f0-998">(GH #1126, 2090)</span><span class="sxs-lookup"><span data-stu-id="058f0-998">(GH #1126, 2090)</span></span>
- <span data-ttu-id="058f0-999">Auditoría de Windows ahora informes de registro de nombre de la imagen en el proceso de creación la auditoría.</span><span class="sxs-lookup"><span data-stu-id="058f0-999">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="058f0-1000">Ahora se producirá un error al iniciar bash.exe desde dentro de una ventana de bash</span><span class="sxs-lookup"><span data-stu-id="058f0-1000">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="058f0-1001">Mensaje de error se ha agregado al interoperabilidad no puede tener acceso a un directorio de trabajo en LxFs (es decir, notepad.exe .bashrc)</span><span class="sxs-lookup"><span data-stu-id="058f0-1001">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="058f0-1002">Se corrigió un problema donde se ha truncado la ruta de acceso de Windows en WSL</span><span class="sxs-lookup"><span data-stu-id="058f0-1002">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="058f0-1003">Las mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="058f0-1003">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-1004">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-1004">LTP Results:</span></span>
<span data-ttu-id="058f0-1005">Número de paso de prueba: 690</span><span class="sxs-lookup"><span data-stu-id="058f0-1005">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="058f0-1006">Número de paso de no (por error, omitido, etcetera...): 274</span><span class="sxs-lookup"><span data-stu-id="058f0-1006">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="058f0-1007">Los registros de ejecución de pruebas LTP</span><span class="sxs-lookup"><span data-stu-id="058f0-1007">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="058f0-1008">Soporte técnico de syscall</span><span class="sxs-lookup"><span data-stu-id="058f0-1008">Syscall Support</span></span>
<span data-ttu-id="058f0-1009">A continuación se muestran una lista de nuevas o mejoradas syscalls que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="058f0-1009">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="058f0-1010">Las llamadas en esta lista se admiten en al menos un escenario, pero es posible que no dispone de todos los parámetros compatibles en este momento.</span><span class="sxs-lookup"><span data-stu-id="058f0-1010">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="058f0-1011">Compilación 14986</span><span class="sxs-lookup"><span data-stu-id="058f0-1011">Build 14986</span></span>

<span data-ttu-id="058f0-1012">Para Windows general, visite información sobre las compilación 14986 el [Blog Windows](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span><span class="sxs-lookup"><span data-stu-id="058f0-1012">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-1013">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-1013">Fixed</span></span>

- <span data-ttu-id="058f0-1014">Fijo verificaciones de error con Netlink y Pty IOCTL</span><span class="sxs-lookup"><span data-stu-id="058f0-1014">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="058f0-1015">Versión del kernel ahora informa 4.4.0-43 para mantener la coherencia con Xenial</span><span class="sxs-lookup"><span data-stu-id="058f0-1015">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="058f0-1016">Bash.exe ahora se inicia cuando la entrada se dirige a ' nul:' (GH #1259)</span><span class="sxs-lookup"><span data-stu-id="058f0-1016">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="058f0-1017">Id. de subproceso notifica ahora correctamente en procfs (GH #967)</span><span class="sxs-lookup"><span data-stu-id="058f0-1017">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="058f0-1018">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | Marcas IN_ISDIR ahora se admiten en inotify_add_watch() (GH #1280)</span><span class="sxs-lookup"><span data-stu-id="058f0-1018">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="058f0-1019">Implemente timer_create y las llamadas del sistema relacionadas.</span><span class="sxs-lookup"><span data-stu-id="058f0-1019">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="058f0-1020">Esto permite el uso GHC (GH #307)</span><span class="sxs-lookup"><span data-stu-id="058f0-1020">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="058f0-1021">Se corrigió un problema donde ping devolvió una hora de 0.000ms (GH #1296)</span><span class="sxs-lookup"><span data-stu-id="058f0-1021">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="058f0-1022">Devuelve el código de error correcto cuando hay demasiados archivos abiertos.</span><span class="sxs-lookup"><span data-stu-id="058f0-1022">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="058f0-1023">Se corrigió un problema en WSL donde Netlink solicitud de datos de la interfaz de red produciría un error con EINVAL si la dirección de hardware de la interfaz es 32 bytes (por ejemplo, la interfaz Teredo)</span><span class="sxs-lookup"><span data-stu-id="058f0-1023">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="058f0-1024">Tenga en cuenta que la utilidad de Linux "ip" contiene un error que bloqueará si WSL informa de una dirección de hardware de 32 bytes.</span><span class="sxs-lookup"><span data-stu-id="058f0-1024">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="058f0-1025">Se trata de un error en la "ip", no WSL.</span><span class="sxs-lookup"><span data-stu-id="058f0-1025">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="058f0-1026">La "ip" utilidad codifica la longitud del búfer de cadena se usa para imprimir la dirección de hardware, y ese búfer es demasiado pequeño para imprimir una dirección de hardware de 32 bytes.</span><span class="sxs-lookup"><span data-stu-id="058f0-1026">The “ip” utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="058f0-1027">Las mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="058f0-1027">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-1028">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-1028">LTP Results:</span></span>
<span data-ttu-id="058f0-1029">Número de paso de prueba: 669</span><span class="sxs-lookup"><span data-stu-id="058f0-1029">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="058f0-1030">Número de paso de no (por error, omitido, etcetera...): 258</span><span class="sxs-lookup"><span data-stu-id="058f0-1030">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="058f0-1031">Los registros de ejecución de pruebas LTP</span><span class="sxs-lookup"><span data-stu-id="058f0-1031">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="058f0-1032">Soporte técnico de syscall</span><span class="sxs-lookup"><span data-stu-id="058f0-1032">Syscall Support</span></span>
<span data-ttu-id="058f0-1033">A continuación se muestran una lista de nuevas o mejoradas syscalls que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="058f0-1033">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="058f0-1034">Las llamadas en esta lista se admiten en al menos un escenario, pero es posible que no dispone de todos los parámetros compatibles en este momento.</span><span class="sxs-lookup"><span data-stu-id="058f0-1034">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="058f0-1035">Compilación 14971</span><span class="sxs-lookup"><span data-stu-id="058f0-1035">Build 14971</span></span>

<span data-ttu-id="058f0-1036">Para Windows general, visite información sobre las compilación 14971 el [Blog Windows](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="058f0-1036">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-1037">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-1037">Fixed</span></span>

 - <span data-ttu-id="058f0-1038">Debido a circunstancias fuera de nuestro control no hay ninguna actualización en esta compilación para el subsistema de Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="058f0-1038">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="058f0-1039">Las actualizaciones programadas regularmente se reanudarán en la próxima versión.</span><span class="sxs-lookup"><span data-stu-id="058f0-1039">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-1040">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-1040">LTP Results:</span></span>
<span data-ttu-id="058f0-1041">No ha cambiado desde 14965</span><span class="sxs-lookup"><span data-stu-id="058f0-1041">Unchanged from 14965</span></span> </br>
<span data-ttu-id="058f0-1042">Número de paso de prueba: 664</span><span class="sxs-lookup"><span data-stu-id="058f0-1042">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="058f0-1043">Número de paso de no (por error, omitido, etcetera...): 263</span><span class="sxs-lookup"><span data-stu-id="058f0-1043">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="058f0-1044">Los registros de ejecución de pruebas LTP</span><span class="sxs-lookup"><span data-stu-id="058f0-1044">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="058f0-1045">Compilación 14965</span><span class="sxs-lookup"><span data-stu-id="058f0-1045">Build 14965</span></span>

<span data-ttu-id="058f0-1046">Para Windows general, visite información sobre las compilación 14965 el [Blog Windows](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="058f0-1046">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-1047">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-1047">Fixed</span></span>

- <span data-ttu-id="058f0-1048">Compatibilidad con Netlink sockets del protocolo NETLINK_ROUTE RTM_GETLINK y RTM_GETADDR (GH #468)</span><span class="sxs-lookup"><span data-stu-id="058f0-1048">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="058f0-1049">Permite que los comandos ifconfig y la dirección ip para la enumeración de red</span><span class="sxs-lookup"><span data-stu-id="058f0-1049">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="058f0-1050">Puede encontrar más información en nuestra [entrada de blog de redes de WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span><span class="sxs-lookup"><span data-stu-id="058f0-1050">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="058f0-1051">/ sbin ahora está en la ruta de acceso de forma predeterminada</span><span class="sxs-lookup"><span data-stu-id="058f0-1051">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="058f0-1052">Ruta de acceso de usuario de NT anexada a la ruta de acceso WSL ahora de forma predeterminada (es decir, ahora puede escribir notepad.exe sin agregar System32 a la ruta de acceso de Linux)</span><span class="sxs-lookup"><span data-stu-id="058f0-1052">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="058f0-1053">Se agregó compatibilidad para /proc/sys/kernel/cap_last_cap</span><span class="sxs-lookup"><span data-stu-id="058f0-1053">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="058f0-1054">Los archivos binarios de NT ahora se puede iniciar desde WSL cuando el directorio de trabajo actual contiene caracteres que no sean ansi (GH #1254)</span><span class="sxs-lookup"><span data-stu-id="058f0-1054">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="058f0-1055">Permitir apagado en el socket de secuencia de unix sin conexión.</span><span class="sxs-lookup"><span data-stu-id="058f0-1055">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="058f0-1056">Se agregó compatibilidad para PR_GET_PDEATHSIG.</span><span class="sxs-lookup"><span data-stu-id="058f0-1056">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="058f0-1057">Se agregó compatibilidad para CLONE_PARENT</span><span class="sxs-lookup"><span data-stu-id="058f0-1057">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="058f0-1058">Se ha corregido error donde canalización obtiene; es decir, bloqueada bash - c "ls - alR /" | Bash -c "cat" (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="058f0-1058">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="058f0-1059">Controlar las solicitudes para conectarse al terminal actual.</span><span class="sxs-lookup"><span data-stu-id="058f0-1059">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="058f0-1060">Marcar/proc /<pid>/oom_score_adj como de escritura.</span><span class="sxs-lookup"><span data-stu-id="058f0-1060">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="058f0-1061">Agregar carpeta /sys/fs/cgroup.</span><span class="sxs-lookup"><span data-stu-id="058f0-1061">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="058f0-1062">sched_setaffinity debe devolver el número de máscara de bits de afinidad</span><span class="sxs-lookup"><span data-stu-id="058f0-1062">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="058f0-1063">Corregir la lógica de validación de ELF que incorrectamente se supone que las rutas de acceso del intérprete deben ser inferior a 64 caracteres.</span><span class="sxs-lookup"><span data-stu-id="058f0-1063">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="058f0-1064">(GH 743 #)</span><span class="sxs-lookup"><span data-stu-id="058f0-1064">(GH #743)</span></span>
- <span data-ttu-id="058f0-1065">Descriptores de archivo abiertos pueden mantener abierta la ventana Consola (GH #1187)</span><span class="sxs-lookup"><span data-stu-id="058f0-1065">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="058f0-1066">Error de Fixeed donde no se pudo rename() con barra diagonal en el nombre de destino (GH #1008) final</span><span class="sxs-lookup"><span data-stu-id="058f0-1066">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="058f0-1067">Implementar archivo /proc/net/dev</span><span class="sxs-lookup"><span data-stu-id="058f0-1067">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="058f0-1068">Hace ping 0.000ms fijo debido a la resolución del temporizador.</span><span class="sxs-lookup"><span data-stu-id="058f0-1068">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="058f0-1069">/Proc/self/environ implementada (GH #730)</span><span class="sxs-lookup"><span data-stu-id="058f0-1069">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="058f0-1070">Las mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="058f0-1070">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-1071">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-1071">LTP Results:</span></span>
<span data-ttu-id="058f0-1072">Número de paso de prueba: 664</span><span class="sxs-lookup"><span data-stu-id="058f0-1072">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="058f0-1073">Número de paso de no (por error, omitido, etcetera...): 263</span><span class="sxs-lookup"><span data-stu-id="058f0-1073">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="058f0-1074">Los registros de ejecución de pruebas LTP</span><span class="sxs-lookup"><span data-stu-id="058f0-1074">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="058f0-1075">Compilación 14959</span><span class="sxs-lookup"><span data-stu-id="058f0-1075">Build 14959</span></span>

<span data-ttu-id="058f0-1076">Para Windows general, visite información sobre las compilación 14959 el [Blog Windows](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span><span class="sxs-lookup"><span data-stu-id="058f0-1076">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-1077">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-1077">Fixed</span></span>

- <span data-ttu-id="058f0-1078">Notificación de proceso de Pico mejorada para Windows.</span><span class="sxs-lookup"><span data-stu-id="058f0-1078">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="058f0-1079">Encontrar información adicional en el [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span><span class="sxs-lookup"><span data-stu-id="058f0-1079">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="058f0-1080">Estabilidad mejorada con la interoperabilidad de Windows</span><span class="sxs-lookup"><span data-stu-id="058f0-1080">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="058f0-1081">Se ha corregido errores 0 x 80070057 al iniciar bash.exe cuando está habilitada la protección de datos de empresa (EDP)</span><span class="sxs-lookup"><span data-stu-id="058f0-1081">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="058f0-1082">Las mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="058f0-1082">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-1083">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-1083">LTP Results:</span></span>
<span data-ttu-id="058f0-1084">Número de paso de prueba: 665</span><span class="sxs-lookup"><span data-stu-id="058f0-1084">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="058f0-1085">Número de paso de no (por error, omitido, etcetera...): 263</span><span class="sxs-lookup"><span data-stu-id="058f0-1085">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="058f0-1086">Los registros de ejecución de pruebas LTP</span><span class="sxs-lookup"><span data-stu-id="058f0-1086">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="058f0-1087">Compilación 14955</span><span class="sxs-lookup"><span data-stu-id="058f0-1087">Build 14955</span></span>

<span data-ttu-id="058f0-1088">Para Windows general, visite información sobre las compilación 14955 el [Blog Windows](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span><span class="sxs-lookup"><span data-stu-id="058f0-1088">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-1089">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-1089">Fixed</span></span>

 - <span data-ttu-id="058f0-1090">Debido a circunstancias fuera de nuestro control no hay ninguna actualización en esta compilación para el subsistema de Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="058f0-1090">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="058f0-1091">Las actualizaciones programadas regularmente se reanudarán en la próxima versión.</span><span class="sxs-lookup"><span data-stu-id="058f0-1091">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-1092">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-1092">LTP Results:</span></span>
<span data-ttu-id="058f0-1093">Número de paso de prueba: 665</span><span class="sxs-lookup"><span data-stu-id="058f0-1093">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="058f0-1094">Número de paso de no (por error, omitido, etcetera...): 263</span><span class="sxs-lookup"><span data-stu-id="058f0-1094">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="058f0-1095">Los registros de ejecución de pruebas LTP</span><span class="sxs-lookup"><span data-stu-id="058f0-1095">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="058f0-1096">Compilación 14951</span><span class="sxs-lookup"><span data-stu-id="058f0-1096">Build 14951</span></span>

<span data-ttu-id="058f0-1097">Para Windows general, visite información sobre las compilación 14951 el [Blog Windows](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="058f0-1097">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="058f0-1098">Nueva característica: Windows o Ubuntu interoperabilidad</span><span class="sxs-lookup"><span data-stu-id="058f0-1098">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="058f0-1099">Los archivos binarios de Windows ahora se pueden invocar directamente desde la línea de comandos WSL.</span><span class="sxs-lookup"><span data-stu-id="058f0-1099">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="058f0-1100">Esto ofrece a los usuarios la capacidad de interactuar con su entorno de Windows y del sistema de forma que no ha sido posible.</span><span class="sxs-lookup"><span data-stu-id="058f0-1100">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="058f0-1101">Un ejemplo rápido, es posible que los usuarios ejecutar los comandos siguientes:</span><span class="sxs-lookup"><span data-stu-id="058f0-1101">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="058f0-1102">Puede encontrar más información en:</span><span class="sxs-lookup"><span data-stu-id="058f0-1102">More information can be found at:</span></span>

- [<span data-ttu-id="058f0-1103">Blog del equipo de WSL para la interoperabilidad</span><span class="sxs-lookup"><span data-stu-id="058f0-1103">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="058f0-1104">Documentación de MSDN sobre interoperabilidad</span><span class="sxs-lookup"><span data-stu-id="058f0-1104">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="058f0-1105">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-1105">Fixed</span></span>

- <span data-ttu-id="058f0-1106">Ubuntu 16.04 (Xenial) ahora se instala para todas las instancias nuevas de WSL.</span><span class="sxs-lookup"><span data-stu-id="058f0-1106">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="058f0-1107">Los usuarios con las instancias existentes 14.04 (Trusty) no se actualizará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="058f0-1107">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="058f0-1108">Ahora se muestra la configuración regional establecida durante la instalación</span><span class="sxs-lookup"><span data-stu-id="058f0-1108">Locale set during install is now displayed</span></span>
- <span data-ttu-id="058f0-1109">Las mejoras de Terminal incluidos errores donde redirige un proceso WSL a un archivo no siempre funcionan</span><span class="sxs-lookup"><span data-stu-id="058f0-1109">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="058f0-1110">Duración de la consola debería se vincula a bash.exe</span><span class="sxs-lookup"><span data-stu-id="058f0-1110">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="058f0-1111">Tamaño de la ventana de consola debe usar tamaño visible, no el tamaño de búfer</span><span class="sxs-lookup"><span data-stu-id="058f0-1111">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="058f0-1112">Las mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="058f0-1112">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-1113">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-1113">LTP Results:</span></span>
<span data-ttu-id="058f0-1114">Número de paso de prueba: 665</span><span class="sxs-lookup"><span data-stu-id="058f0-1114">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="058f0-1115">Número de paso de no (por error, omitido, etcetera...): 263</span><span class="sxs-lookup"><span data-stu-id="058f0-1115">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="058f0-1116">Los registros de ejecución de pruebas LTP</span><span class="sxs-lookup"><span data-stu-id="058f0-1116">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="058f0-1117">Compilación 14946</span><span class="sxs-lookup"><span data-stu-id="058f0-1117">Build 14946</span></span>

<span data-ttu-id="058f0-1118">Para Windows general, visite información sobre las compilación 14946 el [Blog Windows](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span><span class="sxs-lookup"><span data-stu-id="058f0-1118">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-1119">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-1119">Fixed</span></span>

- <span data-ttu-id="058f0-1120">Se corrigió un problema que impedía la creación de cuentas de usuario WSL para los usuarios con los nombres de usuario de NT que contienen espacios o comillas.</span><span class="sxs-lookup"><span data-stu-id="058f0-1120">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="058f0-1121">Cambiar VolFs y DrvFs para devolver 0 para el recuento de vínculos del directorio de stat</span><span class="sxs-lookup"><span data-stu-id="058f0-1121">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="058f0-1122">Admite la opción de socket IPV6_MULTICAST_HOPS.</span><span class="sxs-lookup"><span data-stu-id="058f0-1122">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="058f0-1123">Limitar el bucle de E/S por tty a una única consola.</span><span class="sxs-lookup"><span data-stu-id="058f0-1123">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="058f0-1124">Ejemplo: el siguiente comando es posible:</span><span class="sxs-lookup"><span data-stu-id="058f0-1124">Example: the following command is possible:</span></span>
  - <span data-ttu-id="058f0-1125">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span><span class="sxs-lookup"><span data-stu-id="058f0-1125">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="058f0-1126">Reemplace los espacios por fichas en /proc/cpuinfo (GH #1115)</span><span class="sxs-lookup"><span data-stu-id="058f0-1126">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="058f0-1127">DrvFs aparece ahora en mountinfo con un nombre que coincida con el volumen montado de Windows</span><span class="sxs-lookup"><span data-stu-id="058f0-1127">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="058f0-1128">/ Home/root aparecerán y en mountinfo con nombres correctos</span><span class="sxs-lookup"><span data-stu-id="058f0-1128">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="058f0-1129">Las mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="058f0-1129">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-1130">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-1130">LTP Results:</span></span>
<span data-ttu-id="058f0-1131">Número de paso de prueba: 665</span><span class="sxs-lookup"><span data-stu-id="058f0-1131">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="058f0-1132">Número de paso de no (por error, omitido, etcetera...): 263</span><span class="sxs-lookup"><span data-stu-id="058f0-1132">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="058f0-1133">Los registros de ejecución de pruebas LTP</span><span class="sxs-lookup"><span data-stu-id="058f0-1133">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="058f0-1134">Compilación 14942</span><span class="sxs-lookup"><span data-stu-id="058f0-1134">Build 14942</span></span>

<span data-ttu-id="058f0-1135">Para Windows general, visite información sobre las compilación 14942 el [Blog Windows](https://aka.ms/onefourninefourtwoooooo).</span><span class="sxs-lookup"><span data-stu-id="058f0-1135">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-1136">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-1136">Fixed</span></span>

- <span data-ttu-id="058f0-1137">Un número de verificaciones de error dirigido, incluida la "ha INTENTADO ejecutar de NOEXECUTE memoria" redes de bloqueo que bloqueaba SSH</span><span class="sxs-lookup"><span data-stu-id="058f0-1137">A number of bugchecks addressed, including the “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” networking crash which was blocking SSH</span></span>
- <span data-ttu-id="058f0-1138">compatibilidad con inotifiy notificaciones generadas a partir de las aplicaciones de Windows en DrvFs ahora está en</span><span class="sxs-lookup"><span data-stu-id="058f0-1138">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="058f0-1139">Implementar TCP_KEEPIDLE y TCP_KEEPINTVL para mongod.</span><span class="sxs-lookup"><span data-stu-id="058f0-1139">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="058f0-1140">(GH #695)</span><span class="sxs-lookup"><span data-stu-id="058f0-1140">(GH #695)</span></span>
- <span data-ttu-id="058f0-1141">Implementar la llamada de sistema pivot_root</span><span class="sxs-lookup"><span data-stu-id="058f0-1141">Implement the pivot_root system call</span></span>
- <span data-ttu-id="058f0-1142">Implementar la opción de socket para SO_DONTROUTE</span><span class="sxs-lookup"><span data-stu-id="058f0-1142">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="058f0-1143">Las mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="058f0-1143">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="058f0-1144">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-1144">LTP Results:</span></span>
<span data-ttu-id="058f0-1145">Número de paso de prueba: 665</span><span class="sxs-lookup"><span data-stu-id="058f0-1145">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="058f0-1146">Número de paso de no (por error, omitido, etcetera...): 263</span><span class="sxs-lookup"><span data-stu-id="058f0-1146">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="058f0-1147">Los registros de ejecución de pruebas LTP</span><span class="sxs-lookup"><span data-stu-id="058f0-1147">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="058f0-1148">Soporte técnico de syscall</span><span class="sxs-lookup"><span data-stu-id="058f0-1148">Syscall Support</span></span>
<span data-ttu-id="058f0-1149">A continuación se muestran una lista de nuevas o mejoradas syscalls que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="058f0-1149">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="058f0-1150">Las llamadas en esta lista se admiten en al menos un escenario, pero es posible que no dispone de todos los parámetros compatibles en este momento.</span><span class="sxs-lookup"><span data-stu-id="058f0-1150">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="058f0-1151">Compilación 14936</span><span class="sxs-lookup"><span data-stu-id="058f0-1151">Build 14936</span></span>

<span data-ttu-id="058f0-1152">Para Windows general, visite información sobre las compilación 14936 el [Blog Windows](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="058f0-1152">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="058f0-1153">Nota: WSL instalará Ubuntu versión 16.04 (Xenial) en lugar de Ubuntu 14.04 (furgoneta) en una próxima versión.</span><span class="sxs-lookup"><span data-stu-id="058f0-1153">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="058f0-1154">Este cambio se aplicará a Insider instalar instancias nuevas (lxrun.exe /install o la primera ejecución de bash.exe).</span><span class="sxs-lookup"><span data-stu-id="058f0-1154">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="058f0-1155">Las instancias existentes con furgoneta no se actualizará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="058f0-1155">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="058f0-1156">Los usuarios pueden actualizar su imagen leal a Xenial mediante el comando de actualización de versión de hacer.</span><span class="sxs-lookup"><span data-stu-id="058f0-1156">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="058f0-1157">Problema conocido</span><span class="sxs-lookup"><span data-stu-id="058f0-1157">Known Issue</span></span>
<span data-ttu-id="058f0-1158">WSL está experimentando un problema con algunas implementaciones de socket.</span><span class="sxs-lookup"><span data-stu-id="058f0-1158">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="058f0-1159">La comprobación de errores se manifiesta como un bloqueo con el error "Ha INTENTADO ejecutar NOEXECUTE memoria insuficiente".</span><span class="sxs-lookup"><span data-stu-id="058f0-1159">The bugcheck manifests itself as a crash with the error “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”.</span></span>  <span data-ttu-id="058f0-1160">La manifestación más común de este problema es un bloqueo al usar ssh.</span><span class="sxs-lookup"><span data-stu-id="058f0-1160">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="058f0-1161">La causa raíz se ha corregido en las compilaciones internas y se insertará en Insider lo antes posible.</span><span class="sxs-lookup"><span data-stu-id="058f0-1161">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="058f0-1162">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-1162">Fixed</span></span>

- <span data-ttu-id="058f0-1163">Implementa la llamada del sistema chroot</span><span class="sxs-lookup"><span data-stu-id="058f0-1163">Implemented the chroot system call</span></span>
- <span data-ttu-id="058f0-1164">Mejoras en inotify ~~incluida la compatibilidad con las notificaciones generadas desde aplicaciones de Windows en DrvFs~~</span><span class="sxs-lookup"><span data-stu-id="058f0-1164">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="058f0-1165">Corrección: Inotify compatibilidad con los cambios que se originan desde las aplicaciones de Windows no está disponibles en este momento.</span><span class="sxs-lookup"><span data-stu-id="058f0-1165">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="058f0-1166">Enlace a IPV6 de socket::<port n> ahora admite IPV6_V6ONLY (68 de # GH, #157, 393 #, #460, 674 #, #740, 982 #, #996)</span><span class="sxs-lookup"><span data-stu-id="058f0-1166">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="058f0-1167">Comportamiento WNOWAIT para waitid systemcall implementa (GH #638)</span><span class="sxs-lookup"><span data-stu-id="058f0-1167">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="058f0-1168">Compatibilidad con las opciones de socket IP IP_HDRINCL y IP_TTL</span><span class="sxs-lookup"><span data-stu-id="058f0-1168">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="058f0-1169">Se debe devolver inmediatamente read() de longitud cero (GH #975)</span><span class="sxs-lookup"><span data-stu-id="058f0-1169">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="058f0-1170">Controlar correctamente los prefijos de nombres de archivo y nombre de archivo que no incluyen un terminador NULL en un archivo .tar.</span><span class="sxs-lookup"><span data-stu-id="058f0-1170">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="058f0-1171">compatibilidad con epoll/dev/null</span><span class="sxs-lookup"><span data-stu-id="058f0-1171">epoll support for /dev/null</span></span>
- <span data-ttu-id="058f0-1172">Corregir el origen de hora /dev/alarm</span><span class="sxs-lookup"><span data-stu-id="058f0-1172">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="058f0-1173">Bash -c ahora se puede redirigir a un archivo</span><span class="sxs-lookup"><span data-stu-id="058f0-1173">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="058f0-1174">Las mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="058f0-1174">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-1175">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-1175">LTP Results:</span></span>
<span data-ttu-id="058f0-1176">Número de paso de prueba: 664</span><span class="sxs-lookup"><span data-stu-id="058f0-1176">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="058f0-1177">Número de paso de no (por error, omitido, etcetera...): 264</span><span class="sxs-lookup"><span data-stu-id="058f0-1177">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="058f0-1178">Los registros de ejecución de pruebas LTP</span><span class="sxs-lookup"><span data-stu-id="058f0-1178">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="058f0-1179">Soporte técnico de syscall</span><span class="sxs-lookup"><span data-stu-id="058f0-1179">Syscall Support</span></span>
<span data-ttu-id="058f0-1180">A continuación se muestran una lista de nuevas o mejoradas syscalls que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="058f0-1180">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="058f0-1181">Las llamadas en esta lista se admiten en al menos un escenario, pero es posible que no dispone de todos los parámetros compatibles en este momento.</span><span class="sxs-lookup"><span data-stu-id="058f0-1181">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="058f0-1182">Compilación 14931</span><span class="sxs-lookup"><span data-stu-id="058f0-1182">Build 14931</span></span>

<span data-ttu-id="058f0-1183">Para Windows general, visite información sobre las compilación 14931 el [Blog Windows](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="058f0-1183">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-1184">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-1184">Fixed</span></span>

 - <span data-ttu-id="058f0-1185">Debido a circunstancias fuera de nuestro control no hay ninguna actualización en esta compilación para el subsistema de Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="058f0-1185">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="058f0-1186">Las actualizaciones programadas regularmente se reanudación en la próxima versión.</span><span class="sxs-lookup"><span data-stu-id="058f0-1186">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="058f0-1187">Compilación 14926</span><span class="sxs-lookup"><span data-stu-id="058f0-1187">Build 14926</span></span>

<span data-ttu-id="058f0-1188">Para Windows general, visite información sobre las compilación 14926 el [Blog Windows](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="058f0-1188">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-1189">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-1189">Fixed</span></span>

- <span data-ttu-id="058f0-1190">Ping funciona ahora en las consolas que no tienen privilegios de administrador</span><span class="sxs-lookup"><span data-stu-id="058f0-1190">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="058f0-1191">Ping6 ahora admitidos, también sin privilegios de administrador</span><span class="sxs-lookup"><span data-stu-id="058f0-1191">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="058f0-1192">Inotify compatibilidad con los archivos modificados a través de WSL.</span><span class="sxs-lookup"><span data-stu-id="058f0-1192">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="058f0-1193">(GH #216)</span><span class="sxs-lookup"><span data-stu-id="058f0-1193">(GH #216)</span></span>
  - <span data-ttu-id="058f0-1194">Marcas compatibles:</span><span class="sxs-lookup"><span data-stu-id="058f0-1194">Flags supported:</span></span>
    - <span data-ttu-id="058f0-1195">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="058f0-1195">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="058f0-1196">inotify_add_watch eventos: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="058f0-1196">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="058f0-1197">inotify_add_watch atributos: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="058f0-1197">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="058f0-1198">leer la salida: LX_IN_ISDIR, LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="058f0-1198">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="058f0-1199">Problema conocido: Modificar archivos de aplicaciones de Windows no genera ningún evento</span><span class="sxs-lookup"><span data-stu-id="058f0-1199">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="058f0-1200">Socket de UNIX es compatible ahora con SCM_CREDENTIALS</span><span class="sxs-lookup"><span data-stu-id="058f0-1200">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="058f0-1201">LTP resultados:</span><span class="sxs-lookup"><span data-stu-id="058f0-1201">LTP Results:</span></span>
<span data-ttu-id="058f0-1202">Número de paso de prueba: 651</span><span class="sxs-lookup"><span data-stu-id="058f0-1202">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="058f0-1203">Número de paso de no (por error, omitido, etcetera...): 258</span><span class="sxs-lookup"><span data-stu-id="058f0-1203">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="058f0-1204">Los registros de ejecución de pruebas LTP</span><span class="sxs-lookup"><span data-stu-id="058f0-1204">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="058f0-1205">Compilación 14915</span><span class="sxs-lookup"><span data-stu-id="058f0-1205">Build 14915</span></span>

<span data-ttu-id="058f0-1206">Para Windows general, visite información sobre las compilación 14915 el [Blog Windows](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="058f0-1206">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-1207">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-1207">Fixed</span></span>
-  <span data-ttu-id="058f0-1208">Socketpair para sockets de datagramas de unix (GH #262)</span><span class="sxs-lookup"><span data-stu-id="058f0-1208">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="058f0-1209">Soporte técnico de socket de UNIX para SO_REUSEADDR</span><span class="sxs-lookup"><span data-stu-id="058f0-1209">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="058f0-1210">Soporte técnico de socket de UNIX para SO_BROADCAST (GH #568)</span><span class="sxs-lookup"><span data-stu-id="058f0-1210">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="058f0-1211">Soporte técnico de socket de UNIX para SOCK_SEQPACKET (GH 758 #, #546)</span><span class="sxs-lookup"><span data-stu-id="058f0-1211">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="058f0-1212">Agregar compatibilidad para el envío de socket de datagrama de unix, recepción y de cierre</span><span class="sxs-lookup"><span data-stu-id="058f0-1212">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="058f0-1213">Corregir la comprobación de errores debido a la validación de parámetros mmap no válido para las direcciones no fija.</span><span class="sxs-lookup"><span data-stu-id="058f0-1213">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="058f0-1214">(GH #847)</span><span class="sxs-lookup"><span data-stu-id="058f0-1214">(GH #847)</span></span>
- <span data-ttu-id="058f0-1215">Soporte técnico para suspender y reanudar de Estados de terminales</span><span class="sxs-lookup"><span data-stu-id="058f0-1215">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="058f0-1216">Compatibilidad con TIOCPKT ioctl desbloquear la utilidad de la pantalla (GH #774)</span><span class="sxs-lookup"><span data-stu-id="058f0-1216">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="058f0-1217">Problema conocido: Teclas de función no operativos</span><span class="sxs-lookup"><span data-stu-id="058f0-1217">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="058f0-1218">Se ha corregido una carrera en TimerFd que podría provocar que un miembro liberado 'ReaderReady' LxpTimerFdWorkerRoutine (GH #814) tengan acceso a</span><span class="sxs-lookup"><span data-stu-id="058f0-1218">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="058f0-1219">Habilitar la compatibilidad del sistema reiniciable llamada futex, sondeos y clock_nanosleep</span><span class="sxs-lookup"><span data-stu-id="058f0-1219">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="058f0-1220">Un enlace se ha agregado compatibilidad de montaje</span><span class="sxs-lookup"><span data-stu-id="058f0-1220">Added bind mount support</span></span>
- <span data-ttu-id="058f0-1221">dejar de compartir compatibilidad con el espacio de nombres de montaje</span><span class="sxs-lookup"><span data-stu-id="058f0-1221">unshare for mount namespace support</span></span>
    - <span data-ttu-id="058f0-1222">Problema conocido: Al crear un nuevo espacio de nombres de montaje con `unshare(CLONE_NEWNS)` seguirá el directorio de trabajo actual para que apunte al espacio de nombres anterior</span><span class="sxs-lookup"><span data-stu-id="058f0-1222">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="058f0-1223">Otras mejoras y correcciones de errores</span><span class="sxs-lookup"><span data-stu-id="058f0-1223">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="058f0-1224">Compilación 14905</span><span class="sxs-lookup"><span data-stu-id="058f0-1224">Build 14905</span></span>

<span data-ttu-id="058f0-1225">Para Windows general, visite información sobre las compilación 14905 el [Blog Windows](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span><span class="sxs-lookup"><span data-stu-id="058f0-1225">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-1226">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-1226">Fixed</span></span>
- <span data-ttu-id="058f0-1227">Admite el sistema reiniciable llamadas ahora están (GH #349, GH #520)</span><span class="sxs-lookup"><span data-stu-id="058f0-1227">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="058f0-1228">Vínculos simbólicos a directorios termina en / ahora operativa (GH #650)</span><span class="sxs-lookup"><span data-stu-id="058f0-1228">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="058f0-1229">Implementado ioctl RNDGETENTCNT para/dev/Random</span><span class="sxs-lookup"><span data-stu-id="058f0-1229">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="058f0-1230">Implementa el archivo/proc / [pid] / monta/proc / [pid] / mountinfo y/proc / [pid] / mountstats archivos</span><span class="sxs-lookup"><span data-stu-id="058f0-1230">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="058f0-1231">Las mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="058f0-1231">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="058f0-1232">Compilación 14901</span><span class="sxs-lookup"><span data-stu-id="058f0-1232">Build 14901</span></span>
<span data-ttu-id="058f0-1233">Primera Insider de compilación para la entrada de la versión de Windows 10 Anniversary Update.</span><span class="sxs-lookup"><span data-stu-id="058f0-1233">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="058f0-1234">Para Windows general, visite información sobre las compilación 14901 el [Blog Windows](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="058f0-1234">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-1235">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-1235">Fixed</span></span>
- <span data-ttu-id="058f0-1236">Se corrigió un problema barra diagonal final</span><span class="sxs-lookup"><span data-stu-id="058f0-1236">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="058f0-1237">Los comandos como `$ mv a/c/ a/b/` trabajar ahora</span><span class="sxs-lookup"><span data-stu-id="058f0-1237">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="058f0-1238">Instalación pide ahora si se debe establecer la configuración regional de Ubuntu para la configuración regional de Windows</span><span class="sxs-lookup"><span data-stu-id="058f0-1238">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="058f0-1239">Compatibilidad con procfs carpeta ns</span><span class="sxs-lookup"><span data-stu-id="058f0-1239">Procfs support for ns folder</span></span>
- <span data-ttu-id="058f0-1240">Agrega montaje y desmontaje para tmpfs, procfs y sistemas de archivos sysfs</span><span class="sxs-lookup"><span data-stu-id="058f0-1240">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="058f0-1241">Corregir mknod [arroba] firma ABI de 32 bits</span><span class="sxs-lookup"><span data-stu-id="058f0-1241">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="058f0-1242">Sockets de UNIX se mueven en el modelo de envío</span><span class="sxs-lookup"><span data-stu-id="058f0-1242">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="058f0-1243">Tamaño del búfer INET socket recv establecer mediante setsockopt debe admitirse.</span><span class="sxs-lookup"><span data-stu-id="058f0-1243">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="058f0-1244">Socket de unix MSG_CMSG_CLOEXEC implemente recibir mensaje la marca</span><span class="sxs-lookup"><span data-stu-id="058f0-1244">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="058f0-1245">Redirección de stdin y stdout canalización de proceso de Linux (GH #2)</span><span class="sxs-lookup"><span data-stu-id="058f0-1245">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="058f0-1246">Permite que la canalización de comandos - c de bash de CMD.</span><span class="sxs-lookup"><span data-stu-id="058f0-1246">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="058f0-1247">Ejemplo: > dir | Bash -c "foo grep"</span><span class="sxs-lookup"><span data-stu-id="058f0-1247">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="058f0-1248">Bash ahora se puede instalar en sistemas con varios archivos de paginación (538 GH #, #358)</span><span class="sxs-lookup"><span data-stu-id="058f0-1248">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="058f0-1249">Tamaño de búfer predeterminado INET Socket debe coincidir con la del programa de instalación de Ubuntu predeterminado</span><span class="sxs-lookup"><span data-stu-id="058f0-1249">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="058f0-1250">Alinear xattr syscalls a listxattr</span><span class="sxs-lookup"><span data-stu-id="058f0-1250">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="058f0-1251">Devolver solo las interfaces con una dirección IPv4 válida de SIOCGIFCONF</span><span class="sxs-lookup"><span data-stu-id="058f0-1251">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="058f0-1252">Corregir la acción predeterminada de señal cuando ptrace insertado</span><span class="sxs-lookup"><span data-stu-id="058f0-1252">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="058f0-1253">implement /proc/sys/vm/min_free_kbytes</span><span class="sxs-lookup"><span data-stu-id="058f0-1253">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="058f0-1254">Use los valores de registro de contexto de equipo cuando se restaura el contexto en sigreturn</span><span class="sxs-lookup"><span data-stu-id="058f0-1254">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="058f0-1255">Esto resuelve el problema donde estaban francesa java y javac para algunos usuarios</span><span class="sxs-lookup"><span data-stu-id="058f0-1255">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="058f0-1256">Implement /proc/sys/kernel/hostname</span><span class="sxs-lookup"><span data-stu-id="058f0-1256">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="058f0-1257">Soporte técnico de syscall</span><span class="sxs-lookup"><span data-stu-id="058f0-1257">Syscall Support</span></span>
<span data-ttu-id="058f0-1258">A continuación se muestran una lista de nuevas o mejoradas syscalls que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="058f0-1258">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="058f0-1259">Las llamadas en esta lista se admiten en al menos un escenario, pero es posible que no dispone de todos los parámetros compatibles en este momento.</span><span class="sxs-lookup"><span data-stu-id="058f0-1259">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="058f0-1260">Compilar 14388 a Windows 10 Anniversary Update</span><span class="sxs-lookup"><span data-stu-id="058f0-1260">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="058f0-1261">Para Windows general, visite información sobre las compilación 14388 el [Blog Windows](https://aka.ms/14388wip).</span><span class="sxs-lookup"><span data-stu-id="058f0-1261">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="058f0-1262">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-1262">Fixed</span></span>
- <span data-ttu-id="058f0-1263">Correcciones para prepararse para la actualización de aniversario de Windows 10 en 8/2</span><span class="sxs-lookup"><span data-stu-id="058f0-1263">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="058f0-1264">Puede encontrar más información acerca de WSL en la actualización de aniversario en nuestra [blog](https://blogs.msdn.microsoft.com/wsl/)</span><span class="sxs-lookup"><span data-stu-id="058f0-1264">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="058f0-1265">Compilación 14376</span><span class="sxs-lookup"><span data-stu-id="058f0-1265">Build 14376</span></span>
<span data-ttu-id="058f0-1266">Para Windows general, visite información sobre las compilación 14376 el [Blog Windows](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="058f0-1266">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="058f0-1267">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-1267">Fixed</span></span>
- <span data-ttu-id="058f0-1268">Quitar algunas instancias que apt-get bloquea (GH #493)</span><span class="sxs-lookup"><span data-stu-id="058f0-1268">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="058f0-1269">Se ha corregido un problema donde montajes vacíos no se controlan correctamente</span><span class="sxs-lookup"><span data-stu-id="058f0-1269">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="058f0-1270">Se ha corregido un problema donde ramdisks no se han montado correctamente</span><span class="sxs-lookup"><span data-stu-id="058f0-1270">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="058f0-1271">La aceptación del socket de unix de cambio para que admita indicadores (parcial GH #451)</span><span class="sxs-lookup"><span data-stu-id="058f0-1271">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="058f0-1272">Fijo red comunes relacionados con la pantalla azul</span><span class="sxs-lookup"><span data-stu-id="058f0-1272">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="058f0-1273">Se ha corregido la pantalla azul al obtener acceso a [pid] / proc / / (GH #523) de tareas</span><span class="sxs-lookup"><span data-stu-id="058f0-1273">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="058f0-1274">Uso de CPU elevado fija para algunos escenarios de pty (488 GH #, #504)</span><span class="sxs-lookup"><span data-stu-id="058f0-1274">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="058f0-1275">Las mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="058f0-1275">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="058f0-1276">Compilación 14371</span><span class="sxs-lookup"><span data-stu-id="058f0-1276">Build 14371</span></span>
<span data-ttu-id="058f0-1277">Para Windows general, visite información sobre las compilación 14371 el [Blog Windows](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="058f0-1277">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="058f0-1278">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-1278">Fixed</span></span>
- <span data-ttu-id="058f0-1279">Se ha corregido la carrera de temporización con SIGCHLD y wait() al usar ptrace</span><span class="sxs-lookup"><span data-stu-id="058f0-1279">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="058f0-1280">Se ha corregido un comportamiento determinado cuando las rutas de acceso tienen un carácter final / (GH #432)</span><span class="sxs-lookup"><span data-stu-id="058f0-1280">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="058f0-1281">Se corrigió un problema con el cambio de nombre o desvincular errores debido a los identificadores abiertos en los elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="058f0-1281">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="058f0-1282">Las mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="058f0-1282">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="058f0-1283">Compilación 14366</span><span class="sxs-lookup"><span data-stu-id="058f0-1283">Build 14366</span></span>
<span data-ttu-id="058f0-1284">Para Windows general, visite información sobre las compilación 14366 el [Blog Windows](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span><span class="sxs-lookup"><span data-stu-id="058f0-1284">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="058f0-1285">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-1285">Fixed</span></span>
- <span data-ttu-id="058f0-1286">Corregir en la creación de archivos a través de vínculos simbólicos</span><span class="sxs-lookup"><span data-stu-id="058f0-1286">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="058f0-1287">Se ha agregado listxattr para Python (GH 385)</span><span class="sxs-lookup"><span data-stu-id="058f0-1287">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="058f0-1288">Las mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="058f0-1288">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="058f0-1289">Soporte técnico de syscall</span><span class="sxs-lookup"><span data-stu-id="058f0-1289">Syscall Support</span></span>
-   <span data-ttu-id="058f0-1290">A continuación se muestran una lista de nuevas o mejoradas syscalls que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="058f0-1290">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="058f0-1291">Las llamadas en esta lista se admiten en al menos un escenario, pero es posible que no dispone de todos los parámetros compatibles en este momento.</span><span class="sxs-lookup"><span data-stu-id="058f0-1291">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="058f0-1292">Compilación 14361</span><span class="sxs-lookup"><span data-stu-id="058f0-1292">Build 14361</span></span>
<span data-ttu-id="058f0-1293">Para Windows general información en la compilación 14361, visite la [Blog Windows](https://aka.ms/wip14361).</span><span class="sxs-lookup"><span data-stu-id="058f0-1293">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="058f0-1294">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-1294">Fixed</span></span>
- <span data-ttu-id="058f0-1295">DrvFs ahora distingue mayúsculas de minúsculas cuando se ejecuta en Bash en Ubuntu en Windows.</span><span class="sxs-lookup"><span data-stu-id="058f0-1295">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="058f0-1296">Los usuarios mayo case.txt y CASE. Las unidades de TXT en su/mnt/c</span><span class="sxs-lookup"><span data-stu-id="058f0-1296">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="058f0-1297">Mayúsculas y minúsculas sólo se admiten en Bash en Ubuntu en Windows.</span><span class="sxs-lookup"><span data-stu-id="058f0-1297">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="058f0-1298">Cuando fuera de Bash NTFS notificará los archivos correctamente, pero puede producirse un comportamiento inesperado, interactuar con los archivos de Windows.</span><span class="sxs-lookup"><span data-stu-id="058f0-1298">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="058f0-1299">La raíz de cada volumen (es decir, /mnt/c) no distingue mayúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="058f0-1299">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="058f0-1300">Puede encontrar más información sobre cómo administrar estos archivos en Windows [aquí](https://support.microsoft.com/en-us/kb/100625).</span><span class="sxs-lookup"><span data-stu-id="058f0-1300">More information on handling these files in Windows can be found [here](https://support.microsoft.com/en-us/kb/100625).</span></span>
- <span data-ttu-id="058f0-1301">Mejorado en gran medida pty / tty soporte.</span><span class="sxs-lookup"><span data-stu-id="058f0-1301">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="058f0-1302">Aplicaciones como TMUX ahora admiten (GH 40 de #)</span><span class="sxs-lookup"><span data-stu-id="058f0-1302">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="058f0-1303">Problema de instalación fijo donde no siempre crean cuentas de usuario</span><span class="sxs-lookup"><span data-stu-id="058f0-1303">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="058f0-1304">Lo que permite una lista de argumentos demasiado largas de línea de comandos arg estructura optimizada.</span><span class="sxs-lookup"><span data-stu-id="058f0-1304">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="058f0-1305">(GH #153)</span><span class="sxs-lookup"><span data-stu-id="058f0-1305">(GH #153)</span></span>
- <span data-ttu-id="058f0-1306">Ahora se puede eliminar y chmod archivos read_only desde DrvFs</span><span class="sxs-lookup"><span data-stu-id="058f0-1306">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="058f0-1307">Se ha corregido algunas instancias donde los bloqueos en terminal desconexión (GH #43)</span><span class="sxs-lookup"><span data-stu-id="058f0-1307">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="058f0-1308">chmod y chown ahora funcionan en dispositivos de tty</span><span class="sxs-lookup"><span data-stu-id="058f0-1308">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="058f0-1309">Permitir la conexión a 0.0.0.0 y:: como localhost (GH 388)</span><span class="sxs-lookup"><span data-stu-id="058f0-1309">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="058f0-1310">Sendmsg/recvmsg controlan ahora una longitud del vector de E/S de > 1 (parcial GH #376)</span><span class="sxs-lookup"><span data-stu-id="058f0-1310">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="058f0-1311">Los usuarios pueden ahora participar del archivo de hosts generada automáticamente (GH 398 de #)</span><span class="sxs-lookup"><span data-stu-id="058f0-1311">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="058f0-1312">Configuración regional de Linux con la configuración regional de NT hace coincidir automáticamente durante la instalación (GH #11)</span><span class="sxs-lookup"><span data-stu-id="058f0-1312">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="058f0-1313">Agrega el archivo /proc/sys/vm/swappiness (GH #306)</span><span class="sxs-lookup"><span data-stu-id="058f0-1313">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="058f0-1314">strace ahora se cierra correctamente</span><span class="sxs-lookup"><span data-stu-id="058f0-1314">strace now exits correctly</span></span>
- <span data-ttu-id="058f0-1315">Permitir que las canalizaciones volver a abrirse mediante /proc/self/fd (GH #222)</span><span class="sxs-lookup"><span data-stu-id="058f0-1315">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="058f0-1316">Ocultar directorios bajo %LOCALAPPDATA%\lxss desde DrvFs (GH #270)</span><span class="sxs-lookup"><span data-stu-id="058f0-1316">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="058f0-1317">Mejor control de bash.exe ~.</span><span class="sxs-lookup"><span data-stu-id="058f0-1317">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="058f0-1318">Comandos como "bash ~ ls - c" ahora admite (GH #467)</span><span class="sxs-lookup"><span data-stu-id="058f0-1318">Commands like “bash ~ -c ls” now supported (GH #467)</span></span>
- <span data-ttu-id="058f0-1319">Sockets notifican epoll lectura disponible durante el cierre (GH #271)</span><span class="sxs-lookup"><span data-stu-id="058f0-1319">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="058f0-1320">lxrun / uninstall hace un mejor trabajo eliminando los archivos y carpetas</span><span class="sxs-lookup"><span data-stu-id="058f0-1320">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="058f0-1321">Corregido ps -f (GH #246)</span><span class="sxs-lookup"><span data-stu-id="058f0-1321">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="058f0-1322">Compatibilidad mejorada para x11 aplicaciones como xEmacs (GH #481)</span><span class="sxs-lookup"><span data-stu-id="058f0-1322">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="058f0-1323">Actualiza el tamaño de pila del subproceso inicial para que coincida con la configuración predeterminada de Ubuntu e informar el tamaño correctamente a la syscall get_rlimit (172 GH #, #258)</span><span class="sxs-lookup"><span data-stu-id="058f0-1323">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="058f0-1324">Informe mejorado de los nombres de imagen de proceso de pico (por ejemplo, para la auditoría)</span><span class="sxs-lookup"><span data-stu-id="058f0-1324">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="058f0-1325">/Proc/mountinfo implementada para el comando df</span><span class="sxs-lookup"><span data-stu-id="058f0-1325">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="058f0-1326">Se ha corregido el código de error de vínculo simbólico para el nombre del elemento secundario.</span><span class="sxs-lookup"><span data-stu-id="058f0-1326">Fixed symlink error code for child name .</span></span> <span data-ttu-id="058f0-1327">y...</span><span class="sxs-lookup"><span data-stu-id="058f0-1327">and ..</span></span>
- <span data-ttu-id="058f0-1328">Las mejoras y correcciones de errores de mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="058f0-1328">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="058f0-1329">Soporte técnico de syscall</span><span class="sxs-lookup"><span data-stu-id="058f0-1329">Syscall Support</span></span>
<span data-ttu-id="058f0-1330">A continuación se muestran una lista de nuevas o mejoradas syscalls que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="058f0-1330">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="058f0-1331">Las llamadas en esta lista se admiten en al menos un escenario, pero es posible que no dispone de todos los parámetros compatibles en este momento.</span><span class="sxs-lookup"><span data-stu-id="058f0-1331">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="058f0-1332">Compilación 14352</span><span class="sxs-lookup"><span data-stu-id="058f0-1332">Build 14352</span></span>
<span data-ttu-id="058f0-1333">Para Windows general, visite información sobre las compilación 14352 el [Blog Windows](https://aka.ms/wip14352).</span><span class="sxs-lookup"><span data-stu-id="058f0-1333">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="058f0-1334">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-1334">Fixed</span></span>
- <span data-ttu-id="058f0-1335">Se corrigió un problema donde los archivos grandes no se han descargado / creado correctamente.</span><span class="sxs-lookup"><span data-stu-id="058f0-1335">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="058f0-1336">Esto debe desbloquear npm y otros escenarios (3 GH, GH #313)</span><span class="sxs-lookup"><span data-stu-id="058f0-1336">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="058f0-1337">Quitar algunas instancias donde sockets de bloqueo</span><span class="sxs-lookup"><span data-stu-id="058f0-1337">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="058f0-1338">Corregir algunos errores ptrace</span><span class="sxs-lookup"><span data-stu-id="058f0-1338">Corrected some ptrace errors</span></span>
- <span data-ttu-id="058f0-1339">Se corrigió un problema con WSL que permite a los nombres de archivo más de 255 caracteres</span><span class="sxs-lookup"><span data-stu-id="058f0-1339">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="058f0-1340">Compatibilidad mejorada para los caracteres no válidos</span><span class="sxs-lookup"><span data-stu-id="058f0-1340">Improved support for non-English characters</span></span>
- <span data-ttu-id="058f0-1341">Agregar datos de zona horaria de Windows actuales y establecer como predeterminado</span><span class="sxs-lookup"><span data-stu-id="058f0-1341">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="058f0-1342">Identificador de dispositivo único para cada punto de montaje (corrección de jre – GH #49)</span><span class="sxs-lookup"><span data-stu-id="058f0-1342">Unique device id’s for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="058f0-1343">Corregir el problema con las rutas que contengan "."</span><span class="sxs-lookup"><span data-stu-id="058f0-1343">Correct issue with paths containing “.”</span></span> <span data-ttu-id="058f0-1344">y ".."</span><span class="sxs-lookup"><span data-stu-id="058f0-1344">and “..”</span></span>
- <span data-ttu-id="058f0-1345">Se ha agregado compatibilidad de Fifo (GH #71)</span><span class="sxs-lookup"><span data-stu-id="058f0-1345">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="058f0-1346">Formato actualizado de resolv.conf para que coincida con el formato nativo de Ubuntu</span><span class="sxs-lookup"><span data-stu-id="058f0-1346">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="058f0-1347">Alguna limpieza procfs</span><span class="sxs-lookup"><span data-stu-id="058f0-1347">Some procfs cleanup</span></span>
- <span data-ttu-id="058f0-1348">Ping habilitado para las consolas de administrador (GH #18)</span><span class="sxs-lookup"><span data-stu-id="058f0-1348">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="058f0-1349">Soporte técnico de syscall</span><span class="sxs-lookup"><span data-stu-id="058f0-1349">Syscall Support</span></span>
<span data-ttu-id="058f0-1350">A continuación se muestran una lista de nuevas o mejoradas syscalls que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="058f0-1350">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="058f0-1351">Las llamadas en esta lista se admiten en al menos un escenario, pero es posible que no dispone de todos los parámetros compatibles en este momento.</span><span class="sxs-lookup"><span data-stu-id="058f0-1351">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="058f0-1352">Compilación 14342</span><span class="sxs-lookup"><span data-stu-id="058f0-1352">Build 14342</span></span>
<span data-ttu-id="058f0-1353">Para Windows general de información sobre compilación 14342 el [Blog Windows](https://aka.ms/wip14342).</span><span class="sxs-lookup"><span data-stu-id="058f0-1353">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="058f0-1354">Puede encontrar información sobre VolFs y DriveFs en el [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span><span class="sxs-lookup"><span data-stu-id="058f0-1354">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="058f0-1355">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-1355">Fixed</span></span>
- <span data-ttu-id="058f0-1356">Se ha corregido el problema de instalación cuando el usuario de Windows tuvo caracteres Unicode en el nombre de usuario</span><span class="sxs-lookup"><span data-stu-id="058f0-1356">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="058f0-1357">Ahora se proporciona la solución de udev de actualización de apt-get en las preguntas más frecuentes de forma predeterminada en la primera ejecución</span><span class="sxs-lookup"><span data-stu-id="058f0-1357">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="058f0-1358">Habilita los vínculos simbólicos en DriveFs (/ mnt /<drive>) directorios</span><span class="sxs-lookup"><span data-stu-id="058f0-1358">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="058f0-1359">Los vínculos simbólicos ahora funcionan entre DriveFs y VolFs</span><span class="sxs-lookup"><span data-stu-id="058f0-1359">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="058f0-1360">Ruta direccionada de nivel superior al analizar el problema: ls. / / ahora funcionará según lo esperado</span><span class="sxs-lookup"><span data-stu-id="058f0-1360">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="058f0-1361">instalar NPM en DriveFs y ahora trabaja las opciones -g</span><span class="sxs-lookup"><span data-stu-id="058f0-1361">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="058f0-1362">Se corrigió un problema impide que el servidor PHP iniciar</span><span class="sxs-lookup"><span data-stu-id="058f0-1362">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="058f0-1363">Valores de entorno actualizado de forma predeterminada, como $PATH para más cercano que coincida con Ubuntu nativo</span><span class="sxs-lookup"><span data-stu-id="058f0-1363">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="058f0-1364">Agrega una tarea de mantenimiento semanal en Windows para actualizar la caché de paquetes apt</span><span class="sxs-lookup"><span data-stu-id="058f0-1364">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="058f0-1365">Se ha corregido el problema con la validación del encabezado de ELF, WSL ahora es compatible con todas las opciones de Melkor</span><span class="sxs-lookup"><span data-stu-id="058f0-1365">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="058f0-1366">Shell Zsh es funcional</span><span class="sxs-lookup"><span data-stu-id="058f0-1366">Zsh shell is functional</span></span>
- <span data-ttu-id="058f0-1367">Ahora se admiten los binarios precompilados de Go</span><span class="sxs-lookup"><span data-stu-id="058f0-1367">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="058f0-1368">Preguntar en Bash.exe primero ejecute ahora se traduce correctamente</span><span class="sxs-lookup"><span data-stu-id="058f0-1368">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="058f0-1369">/proc/meminfo ahora devuelve la información correcta</span><span class="sxs-lookup"><span data-stu-id="058f0-1369">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="058f0-1370">Sockets, que ahora se admiten en VFS</span><span class="sxs-lookup"><span data-stu-id="058f0-1370">Sockets now supported in VFS</span></span>
- <span data-ttu-id="058f0-1371">/ dev ahora está montado como tempfs</span><span class="sxs-lookup"><span data-stu-id="058f0-1371">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="058f0-1372">FIFO admitidos ahora</span><span class="sxs-lookup"><span data-stu-id="058f0-1372">Fifo now supported</span></span>
- <span data-ttu-id="058f0-1373">Sistemas de varios núcleos ahora muestran correctamente en/proc/cpuinfo</span><span class="sxs-lookup"><span data-stu-id="058f0-1373">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="058f0-1374">Mejoras adicionales y mensajes de error de descarga durante la primera ejecución</span><span class="sxs-lookup"><span data-stu-id="058f0-1374">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="058f0-1375">Syscall mejoras y correcciones de errores.</span><span class="sxs-lookup"><span data-stu-id="058f0-1375">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="058f0-1376">Syscall compatible la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="058f0-1376">Supported syscall list below.</span></span>
- <span data-ttu-id="058f0-1377">Las mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="058f0-1377">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="058f0-1378">Problemas conocidos</span><span class="sxs-lookup"><span data-stu-id="058f0-1378">Known Issues</span></span>
- <span data-ttu-id="058f0-1379">No resolver '..'</span><span class="sxs-lookup"><span data-stu-id="058f0-1379">Not resolving ‘..’</span></span> <span data-ttu-id="058f0-1380">correctamente en DriveFs en algunos casos</span><span class="sxs-lookup"><span data-stu-id="058f0-1380">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="058f0-1381">Soporte técnico de syscall</span><span class="sxs-lookup"><span data-stu-id="058f0-1381">Syscall Support</span></span>
<span data-ttu-id="058f0-1382">A continuación se muestran una lista de nuevas o mejoradas syscalls que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="058f0-1382">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="058f0-1383">Las llamadas en esta lista se admiten en al menos un escenario, pero es posible que no dispone de todos los parámetros compatibles en este momento.</span><span class="sxs-lookup"><span data-stu-id="058f0-1383">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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

## <a name="build-14332"></a><span data-ttu-id="058f0-1384">Compilación 14332</span><span class="sxs-lookup"><span data-stu-id="058f0-1384">Build 14332</span></span>

<span data-ttu-id="058f0-1385">Para Windows general, visite información sobre las compilación 14332 el [Blog Windows](https://aka.ms/wip14332).</span><span class="sxs-lookup"><span data-stu-id="058f0-1385">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="058f0-1386">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-1386">Fixed</span></span>
- <span data-ttu-id="058f0-1387">Mejor generación de resolv.conf incluidos dando prioridad a las entradas de DNS</span><span class="sxs-lookup"><span data-stu-id="058f0-1387">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="058f0-1388">Problema con el traslado de archivos y directorios entre/mnt y no- / mnt unidades</span><span class="sxs-lookup"><span data-stu-id="058f0-1388">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="058f0-1389">Ahora se pueden crear los archivos tar con vínculos simbólicos</span><span class="sxs-lookup"><span data-stu-id="058f0-1389">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="058f0-1390">Directorio de /run/lock predeterminada se ha agregado en la creación de instancias</span><span class="sxs-lookup"><span data-stu-id="058f0-1390">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="058f0-1391">Actualizar/dev/null para devolver la información de estadísticas correcta</span><span class="sxs-lookup"><span data-stu-id="058f0-1391">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="058f0-1392">Errores adicionales cuando se descargan durante la primera ejecución</span><span class="sxs-lookup"><span data-stu-id="058f0-1392">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="058f0-1393">Syscall mejoras y correcciones de errores.</span><span class="sxs-lookup"><span data-stu-id="058f0-1393">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="058f0-1394">Syscall compatible la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="058f0-1394">Supported syscall list below.</span></span>
- <span data-ttu-id="058f0-1395">Las mejoras y correcciones de errores de mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="058f0-1395">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="058f0-1396">Soporte técnico de syscall</span><span class="sxs-lookup"><span data-stu-id="058f0-1396">Syscall Support</span></span>
<span data-ttu-id="058f0-1397">A continuación es el nuevo syscall que tiene alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="058f0-1397">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="058f0-1398">La syscall en esta lista es compatible con al menos un escenario, pero es posible que no dispone de todos los parámetros compatibles en este momento.</span><span class="sxs-lookup"><span data-stu-id="058f0-1398">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="058f0-1399">Compilación 14328</span><span class="sxs-lookup"><span data-stu-id="058f0-1399">Build 14328</span></span>

<span data-ttu-id="058f0-1400">Para Windows general, visite información sobre las compilación 14332 el [Blog Windows](https://aka.ms/wip14328).</span><span class="sxs-lookup"><span data-stu-id="058f0-1400">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="058f0-1401">Nuevas características</span><span class="sxs-lookup"><span data-stu-id="058f0-1401">New Features</span></span>
* <span data-ttu-id="058f0-1402">Admite ahora los usuarios de Linux.</span><span class="sxs-lookup"><span data-stu-id="058f0-1402">Now support Linux users.</span></span>  <span data-ttu-id="058f0-1403">Instalación de Bash en Ubuntu en Windows solicitará para la creación de un usuario de Linux.</span><span class="sxs-lookup"><span data-stu-id="058f0-1403">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="058f0-1404">Para obtener más información, visite https://aka.ms/wslusers</span><span class="sxs-lookup"><span data-stu-id="058f0-1404">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="058f0-1405">Nombre de host se establece ahora en el nombre del equipo Windows, no hay más @localhost</span><span class="sxs-lookup"><span data-stu-id="058f0-1405">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="058f0-1406">Para obtener más información sobre compilación 14328, visite: https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="058f0-1406">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="058f0-1407">Fijo</span><span class="sxs-lookup"><span data-stu-id="058f0-1407">Fixed</span></span>
* <span data-ttu-id="058f0-1408">Mejoras de vínculo simbólico para que no es/mnt /<drive> archivos</span><span class="sxs-lookup"><span data-stu-id="058f0-1408">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="058f0-1409">NPM install ahora funciona</span><span class="sxs-lookup"><span data-stu-id="058f0-1409">npm install now works</span></span>
    * <span data-ttu-id="058f0-1410">JDK / jre ahora instalable con instrucciones que encontrará [aquí](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span><span class="sxs-lookup"><span data-stu-id="058f0-1410">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="058f0-1411">problema conocido: los vínculos simbólicos no funcionan para Windows monta.</span><span class="sxs-lookup"><span data-stu-id="058f0-1411">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="058f0-1412">Funcionalidad estará disponible en una compilación posterior</span><span class="sxs-lookup"><span data-stu-id="058f0-1412">Functionality will be available in a later build</span></span>
* <span data-ttu-id="058f0-1413">parte superior y htop se muestran ahora</span><span class="sxs-lookup"><span data-stu-id="058f0-1413">top and htop now display</span></span>
* <span data-ttu-id="058f0-1414">Mensajes de error adicionales para algunos errores de la instalación</span><span class="sxs-lookup"><span data-stu-id="058f0-1414">Additional error messages for some install failures</span></span>
* <span data-ttu-id="058f0-1415">Syscall mejoras y correcciones de errores.</span><span class="sxs-lookup"><span data-stu-id="058f0-1415">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="058f0-1416">Syscall compatible la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="058f0-1416">Supported syscall list below.</span></span>
* <span data-ttu-id="058f0-1417">Las mejoras y correcciones de errores de mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="058f0-1417">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="058f0-1418">Soporte técnico de syscall</span><span class="sxs-lookup"><span data-stu-id="058f0-1418">Syscall Support</span></span>
<span data-ttu-id="058f0-1419">A continuación es una lista de llamadas que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="058f0-1419">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="058f0-1420">Syscall en esta lista se admite en al menos un escenario, pero es posible que no dispone de todos los parámetros compatibles en este momento.</span><span class="sxs-lookup"><span data-stu-id="058f0-1420">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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
