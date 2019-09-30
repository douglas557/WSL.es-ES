---
title: Notas de la versión del subsistema de Windows para Linux
description: Notas de la versión del subsistema de Windows para Linux.  Actualizado semanalmente.
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, subsistemawindows, ubuntu
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 9dfd4704eee537c053d874d6fcee47b70efbc33c
ms.sourcegitcommit: 212d3e0092dbc584a8422de47599a4ce46f0f016
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/11/2019
ms.locfileid: "70902423"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="b32b8-105">Notas de la versión del subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="b32b8-105">Release Notes for Windows Subsystem for Linux</span></span>

## <a name="build-18980"></a><span data-ttu-id="b32b8-106">Compilación 18980</span><span class="sxs-lookup"><span data-stu-id="b32b8-106">Build 18980</span></span>
<span data-ttu-id="b32b8-107">Para obtener información general de Windows sobre la compilación 18980, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-107">For general Windows information on build 18980 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).</span></span>

* <span data-ttu-id="b32b8-108">Corrige la lectura de los vínculos simbólicos que deniegan FILE_READ_DATA.</span><span class="sxs-lookup"><span data-stu-id="b32b8-108">Fix reading symlinks that deny FILE_READ_DATA.</span></span> <span data-ttu-id="b32b8-109">Esto incluye todos los vínculos simbólicos que crea Windows para la compatibilidad con versiones anteriores, como "C:\Document and Settings" y un conjunto de vínculos simbólicos en el directorio de perfil del usuario.</span><span class="sxs-lookup"><span data-stu-id="b32b8-109">This includes all the symlinks Windows creates for backwards compatibility such as "C:\Document and Settings" and a bunch of symlinks in the user profile directory</span></span>
* <span data-ttu-id="b32b8-110">Hace que el estado inesperado del sistema de archivos no sea irrecuperable [GH 4334, 4305]</span><span class="sxs-lookup"><span data-stu-id="b32b8-110">Make unexpected filesystem state non-fatal [GH 4334, 4305]</span></span>
* <span data-ttu-id="b32b8-111">[WSL2] Agrega compatibilidad para arm64 si tu CPU/firmware admite virtualización</span><span class="sxs-lookup"><span data-stu-id="b32b8-111">[WSL2] Add support for arm64 if your CPU / firmware supports virtualization</span></span>
* <span data-ttu-id="b32b8-112">[WSL2] Permite a los usuarios sin privilegios ver el registro del kernel</span><span class="sxs-lookup"><span data-stu-id="b32b8-112">[WSL2] Allow unprivileged users to view kernel log</span></span>
* <span data-ttu-id="b32b8-113">[WSL2] Corrige la retransmisión de salida cuando se han cerrado los sockets stdout/stderr [GH 4375]</span><span class="sxs-lookup"><span data-stu-id="b32b8-113">[WSL2] Fix output relay when stdout / stderr sockets have been closed [GH 4375]</span></span>
* <span data-ttu-id="b32b8-114">[WSL2] Compatibilidad con la batería y el adaptador de AC</span><span class="sxs-lookup"><span data-stu-id="b32b8-114">[WSL2] Support battery and AC adapter passthrough</span></span>
* <span data-ttu-id="b32b8-115">[WSL2] Actualización del kernel de Linux a 4.19.67</span><span class="sxs-lookup"><span data-stu-id="b32b8-115">[WSL2] Update Linux kernel to 4.19.67</span></span>
* <span data-ttu-id="b32b8-116">Adición de la capacidad de establecer el nombre de usuario predeterminado en /etc/WSL.conf:</span><span class="sxs-lookup"><span data-stu-id="b32b8-116">Add the ability to set default username in /etc/wsl.conf:</span></span>
```
[user]
default=root
```

## <a name="build-18975"></a><span data-ttu-id="b32b8-117">Compilación 18975</span><span class="sxs-lookup"><span data-stu-id="b32b8-117">Build 18975</span></span>
<span data-ttu-id="b32b8-118">Para obtener información general de Windows sobre la compilación 18975,visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-118">For general Windows information on build 18975 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).</span></span>

* <span data-ttu-id="b32b8-119">[WSL2] Se han corregido varios problemas de confiabilidad de localhost [GH 4340]</span><span class="sxs-lookup"><span data-stu-id="b32b8-119">[WSL2] Fixed a number of localhost reliability issues [GH 4340]</span></span>

## <a name="build-18970"></a><span data-ttu-id="b32b8-120">Compilación 18970</span><span class="sxs-lookup"><span data-stu-id="b32b8-120">Build 18970</span></span>
<span data-ttu-id="b32b8-121">Para obtener información general de Windows sobre la compilación 18970, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-121">For general Windows information on build 18970 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).</span></span>

* <span data-ttu-id="b32b8-122">[WSL2] Sincronización de la hora con la hora del host cuando el sistema se reanuda desde el estado de suspensión [GH 4245]</span><span class="sxs-lookup"><span data-stu-id="b32b8-122">[WSL2] Sync time with host time when system resumes from sleep state [GH 4245]</span></span>
* <span data-ttu-id="b32b8-123">[WSL2] Crea vínculos simbólicos de NT en volúmenes de Windows cuando sea posible.</span><span class="sxs-lookup"><span data-stu-id="b32b8-123">[WSL2] Create NT symlinks on the Windows volumes when possible.</span></span>
* <span data-ttu-id="b32b8-124">[WSL2] Crea distribuciones en los espacios de nombres UTS, IPC, PID y Mount.</span><span class="sxs-lookup"><span data-stu-id="b32b8-124">[WSL2] Create distros in UTS, IPC, PID, and Mount namespaces.</span></span>
* <span data-ttu-id="b32b8-125">[WSL2] Corrección de retransmisión de puerto localhost cuando el servidor se enlaza a localhost directamente [GH 4353]</span><span class="sxs-lookup"><span data-stu-id="b32b8-125">[WSL2] Fix localhost port relay when server binds to localhost directly [GH 4353]</span></span>
* <span data-ttu-id="b32b8-126">[WSL2] Corrección de interoperabilidad cuando se redirige la salida [GH 4337]</span><span class="sxs-lookup"><span data-stu-id="b32b8-126">[WSL2] Fix interop when output is redirected [GH 4337]</span></span>
* <span data-ttu-id="b32b8-127">[WSL2] Compatibilidad con la traducción de vínculos simbólicos de NT absolutos.</span><span class="sxs-lookup"><span data-stu-id="b32b8-127">[WSL2] Support translating absolute NT symlinks.</span></span>
* <span data-ttu-id="b32b8-128">[WSL2] Actualización del kernel a 4.19.59</span><span class="sxs-lookup"><span data-stu-id="b32b8-128">[WSL2] Update kernel to 4.19.59</span></span>
* <span data-ttu-id="b32b8-129">[WSL2] Definición correcta de la máscara de subred para eth0.</span><span class="sxs-lookup"><span data-stu-id="b32b8-129">[WSL2] Properly set subnet mask for eth0.</span></span>
* <span data-ttu-id="b32b8-130">[WSL2] Cambio de la lógica para interrumpir el bucle de trabajo de la consola cuando se señale el evento de salida.</span><span class="sxs-lookup"><span data-stu-id="b32b8-130">[WSL2] Change logic to break out of console worker loop when exit event is signaled.</span></span>
* <span data-ttu-id="b32b8-131">[WSL2] Expulsión del VHD de distribución cuando la  distribución no está en ejecución.</span><span class="sxs-lookup"><span data-stu-id="b32b8-131">[WSL2] Eject distribution vhd when the distro is not running.</span></span>
* <span data-ttu-id="b32b8-132">[WSL2] Corrección de la biblioteca de análisis de configuración para controlar correctamente los valores vacíos.</span><span class="sxs-lookup"><span data-stu-id="b32b8-132">[WSL2] Fix config parsing library to correctly handle empty values.</span></span>
* <span data-ttu-id="b32b8-133">[WSL2] Compatibilidad con el escritorio de Docker al crear montajes de distribución cruzados.</span><span class="sxs-lookup"><span data-stu-id="b32b8-133">[WSL2] Support Docker Desktop by creating cross distro mounts.</span></span> <span data-ttu-id="b32b8-134">Un distribución puede participar en este comportamiento si se agrega la siguiente línea al archivo /etc/wsl.conf:</span><span class="sxs-lookup"><span data-stu-id="b32b8-134">A distro can opt-in to this behavior by adding the following line to the /etc/wsl.conf file:</span></span>
```
[automount]
crossDistro = true
```

## <a name="build-18945"></a><span data-ttu-id="b32b8-135">Compilación 18945</span><span class="sxs-lookup"><span data-stu-id="b32b8-135">Build 18945</span></span>
<span data-ttu-id="b32b8-136">Para obtener información general de Windows sobre la compilación 18945, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-136">For general Windows information on build 18945 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-137">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-137">WSL</span></span>
* <span data-ttu-id="b32b8-138">[WSL2] Permite que se acceda a los sockets TCP de escucha en WSL2 desde el host mediante localhost:port</span><span class="sxs-lookup"><span data-stu-id="b32b8-138">[WSL2] Allow listening tcp sockets in WSL2 to be accessible from the host by using localhost:port</span></span>
* <span data-ttu-id="b32b8-139">[WSL2] Correcciones de errores de instalación/conversión y diagnósticos adicionales para un seguimiento de los problemas futuros [GH 4105]</span><span class="sxs-lookup"><span data-stu-id="b32b8-139">[WSL2] Fixes for install / conversion failures and additional diagnostics to track down future issues [GH 4105]</span></span> 
* <span data-ttu-id="b32b8-140">[WSL2] Mejora la capacidad de diagnóstico de los problemas de red de WSL2</span><span class="sxs-lookup"><span data-stu-id="b32b8-140">[WSL2] Improve diagnosability of WSL2 network issues</span></span>
* <span data-ttu-id="b32b8-141">[WSL2] Actualización de la versión del kernel a 4.19.55</span><span class="sxs-lookup"><span data-stu-id="b32b8-141">[WSL2] Update kernel version to 4.19.55</span></span>
* <span data-ttu-id="b32b8-142">[WSL2] Actualización del kernel con las opciones de configuración necesarias para Docker [GH 4165]</span><span class="sxs-lookup"><span data-stu-id="b32b8-142">[WSL2] Update kernel with config options required for docker [GH 4165]</span></span>
* <span data-ttu-id="b32b8-143">[WSL2] Aumento del número de CPU asignadas a la VM de utilidad ligera para que sea el mismo que el host (se ha limitado previamente a 8 por CONFIG_NR_CPUS en la configuración del kernel) [GH 4137]</span><span class="sxs-lookup"><span data-stu-id="b32b8-143">[WSL2] Increase the number of CPUs assigned to the lightweight utility VM to be the same as the host (was previously capped at 8 by CONFIG_NR_CPUS in the kernel config) [GH 4137]</span></span>
* <span data-ttu-id="b32b8-144">[WSL2] Creación de un archivo de intercambio para la VM ligera WSL2</span><span class="sxs-lookup"><span data-stu-id="b32b8-144">[WSL2] Create a swap file for the WSL2 lightweight VM</span></span>
* <span data-ttu-id="b32b8-145">[WSL2] Permite que los montajes de usuarios sean visibles a través de la distribución \\\\wsl$\\ (por ejemplo, sshfs) [GH 4172]</span><span class="sxs-lookup"><span data-stu-id="b32b8-145">[WSL2] Allow user mounts to be visible via \\\\wsl$\\distro (for example sshfs) [GH 4172]</span></span>
* <span data-ttu-id="b32b8-146">[WSL2] Mejora el rendimiento del sistema de archivos 9p</span><span class="sxs-lookup"><span data-stu-id="b32b8-146">[WSL2] Improve 9p filesystem performance</span></span>
* <span data-ttu-id="b32b8-147">[WSL2] Asegura que la ACL de VHD no crezca sin límite [GH 4126]</span><span class="sxs-lookup"><span data-stu-id="b32b8-147">[WSL2] Ensure vhd ACL does not grow unbounded [GH 4126]</span></span>
* <span data-ttu-id="b32b8-148">[WSL2] Actualización de la configuración de kernel para admitir squashfs y xt_conntrack [GH 4107, 4123]</span><span class="sxs-lookup"><span data-stu-id="b32b8-148">[WSL2] Update kernel config to support squashfs and xt_conntrack [GH 4107, 4123]</span></span>
* <span data-ttu-id="b32b8-149">[WSL2] Corrección para la opción interop.enabled /etc/wsl.conf [GH 4140]</span><span class="sxs-lookup"><span data-stu-id="b32b8-149">[WSL2] Fix for interop.enabled /etc/wsl.conf option [GH 4140]</span></span>
* <span data-ttu-id="b32b8-150">[WSL2] Devuelve ENOTSUP si el sistema de archivos no es compatible con EA</span><span class="sxs-lookup"><span data-stu-id="b32b8-150">[WSL2] Return ENOTSUP if the file system does not support EAs</span></span>
* <span data-ttu-id="b32b8-151">[WSL2] Corrección de CopyFile colgado con \\\\wsl$</span><span class="sxs-lookup"><span data-stu-id="b32b8-151">[WSL2] Fix CopyFile hang with \\\\wsl$</span></span>
* <span data-ttu-id="b32b8-152">Cambio del valor predeterminado de umask a 0022 y adición de la configuración de filesystem.umask a /etc/wsl.conf</span><span class="sxs-lookup"><span data-stu-id="b32b8-152">Switch default umask to 0022 and add filesystem.umask setting to /etc/wsl.conf</span></span>
* <span data-ttu-id="b32b8-153">Corrección de wslpath para resolver correctamente los vínculos simbólicos, esto se retomó en 19h1 [GH 4078]</span><span class="sxs-lookup"><span data-stu-id="b32b8-153">Fix wslpath to properly resolve symlinks, this was regressed in 19h1 [GH 4078]</span></span>
* <span data-ttu-id="b32b8-154">Introducción del archivo %UserProfile%\\.wslconfig para ajustar la configuración de WSL2</span><span class="sxs-lookup"><span data-stu-id="b32b8-154">Introduce %UserProfile%\\.wslconfig file for tweaking WSL2 settings</span></span>
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

## <a name="build-18917"></a><span data-ttu-id="b32b8-155">Compilación 18917</span><span class="sxs-lookup"><span data-stu-id="b32b8-155">Build 18917</span></span>
<span data-ttu-id="b32b8-156">Para obtener información general de Windows sobre la compilación 18917, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-156">For general Windows information on build 18917 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-157">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-157">WSL</span></span>
* <span data-ttu-id="b32b8-158">¡WSL 2 ya está disponible!</span><span class="sxs-lookup"><span data-stu-id="b32b8-158">WSL 2 is now available!</span></span> <span data-ttu-id="b32b8-159">Consulta el [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) para más detalles.</span><span class="sxs-lookup"><span data-stu-id="b32b8-159">Please see [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) for more details.</span></span>
* <span data-ttu-id="b32b8-160">Corrección de una regresión en la que iniciar procesos de Windows a través de vínculos simbólicos no funcionaba correctamente [GH 3999]</span><span class="sxs-lookup"><span data-stu-id="b32b8-160">Fix a regression where launching Windows processes via symlinks did not work correctly [GH 3999]</span></span>
* <span data-ttu-id="b32b8-161">Agrega las opciones wsl.exe --list --verbose, wsl.exe --list --quiet y wsl.exe --import --version a wsl.exe</span><span class="sxs-lookup"><span data-stu-id="b32b8-161">Add wsl.exe --list --verbose, wsl.exe --list --quiet, and wsl.exe --import --version options to wsl.exe</span></span>
* <span data-ttu-id="b32b8-162">Agrega la opción wsl.exe --shutdown</span><span class="sxs-lookup"><span data-stu-id="b32b8-162">Add wsl.exe --shutdown option</span></span>
* <span data-ttu-id="b32b8-163">Plan 9: Permite abrir un directorio para escribir en él correctamente</span><span class="sxs-lookup"><span data-stu-id="b32b8-163">Plan 9: Allow opening a directory for write to succeed</span></span>

## <a name="build-18890"></a><span data-ttu-id="b32b8-164">Compilación 18890</span><span class="sxs-lookup"><span data-stu-id="b32b8-164">Build 18890</span></span>
<span data-ttu-id="b32b8-165">Para obtener información general de Windows sobre la compilación 18890, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-165">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-166">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-166">WSL</span></span>
* <span data-ttu-id="b32b8-167">Pérdida de socket sin bloqueo [GH 2913]</span><span class="sxs-lookup"><span data-stu-id="b32b8-167">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="b32b8-168">La entrada de EOF en el terminal puede bloquear lecturas posteriores [GH 3421]</span><span class="sxs-lookup"><span data-stu-id="b32b8-168">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="b32b8-169">Actualización del encabezado de resolv.conf para hacer referencia a wsl.conf [descrito en GH 3928]</span><span class="sxs-lookup"><span data-stu-id="b32b8-169">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="b32b8-170">Interbloqueo en código de eliminación de epoll [GH 3922]</span><span class="sxs-lookup"><span data-stu-id="b32b8-170">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="b32b8-171">Control de espacios de los argumentos en -import y -export [GH 3932]</span><span class="sxs-lookup"><span data-stu-id="b32b8-171">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="b32b8-172">La extensión de los archivos de mmap no funciona correctamente [GH 3939]</span><span class="sxs-lookup"><span data-stu-id="b32b8-172">Extending mmap’d files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="b32b8-173">Corrección del problema por el que el acceso a ARM64 \\wsl$ no funciona correctamente</span><span class="sxs-lookup"><span data-stu-id="b32b8-173">Fix issue with ARM64 \\wsl$ access not working properly</span></span>
* <span data-ttu-id="b32b8-174">Agrega el mejor icono predeterminado para wsl.exe</span><span class="sxs-lookup"><span data-stu-id="b32b8-174">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="b32b8-175">Compilación 18342</span><span class="sxs-lookup"><span data-stu-id="b32b8-175">Build 18342</span></span>
<span data-ttu-id="b32b8-176">Para obtener información general de Windows sobre la compilación 18342, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-176">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-177">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-177">WSL</span></span>
* <span data-ttu-id="b32b8-178">Hemos agregado la posibilidad de que los usuarios accedan a los archivos de Linux en una distribución de WSL desde Windows.</span><span class="sxs-lookup"><span data-stu-id="b32b8-178">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="b32b8-179">Se puede acceder a estos archivos a través de la línea de comandos; también las aplicaciones de Windows, como el explorador de archivos, VSCode, etc., pueden interactuar con estos archivos.</span><span class="sxs-lookup"><span data-stu-id="b32b8-179">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="b32b8-180">Para acceder a los archivos, ve a \\\\wsl$\\<nombre_de_distribución>, o consulta la lista de las distribuciones en ejecución en \\\\wsl$</span><span class="sxs-lookup"><span data-stu-id="b32b8-180">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="b32b8-181">Agrega etiquetas de información de CPU adicionales y corregir valores de Cpus_allowed[_list] [GH 2234]</span><span class="sxs-lookup"><span data-stu-id="b32b8-181">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="b32b8-182">Compatibilidad con exec desde un subproceso no líder [GH 3800]</span><span class="sxs-lookup"><span data-stu-id="b32b8-182">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="b32b8-183">Trata errores de actualización de la configuración como no irrecuperables [GH 3785]</span><span class="sxs-lookup"><span data-stu-id="b32b8-183">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="b32b8-184">Actualización de binfmt para administrar correctamente los desplazamientos [GH 3768]</span><span class="sxs-lookup"><span data-stu-id="b32b8-184">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="b32b8-185">Habilita la asignación de unidades de red para Plan 9 [GH 3854]</span><span class="sxs-lookup"><span data-stu-id="b32b8-185">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="b32b8-186">Compatibilidad con traducción de rutas de acceso Windows -> Linux y Linux -> Windows para montajes de enlace</span><span class="sxs-lookup"><span data-stu-id="b32b8-186">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="b32b8-187">Crea secciones de solo lectura para asignaciones en archivos abiertos de solo lectura</span><span class="sxs-lookup"><span data-stu-id="b32b8-187">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="b32b8-188">Compilación 18334</span><span class="sxs-lookup"><span data-stu-id="b32b8-188">Build 18334</span></span>
<span data-ttu-id="b32b8-189">Para obtener información general de Windows sobre la compilación 18334, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-189">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-190">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-190">WSL</span></span>
* <span data-ttu-id="b32b8-191">Rediseña el modo en que se asigna la zona horaria de Windows a una zona horaria de Linux [GH 3747]</span><span class="sxs-lookup"><span data-stu-id="b32b8-191">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="b32b8-192">Corrección de pérdidas de memoria y adición de nuevas funciones de traducción de cadenas [GH 3746]</span><span class="sxs-lookup"><span data-stu-id="b32b8-192">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="b32b8-193">SIGCONT en un grupo de subprocesos sin subprocesos es no-op [alvent 3741]</span><span class="sxs-lookup"><span data-stu-id="b32b8-193">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="b32b8-194">Muestra correctamente los descriptores de archivo de socket y epoll en /proc/self/fd</span><span class="sxs-lookup"><span data-stu-id="b32b8-194">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="b32b8-195">Compilación 18305</span><span class="sxs-lookup"><span data-stu-id="b32b8-195">Build 18305</span></span>
<span data-ttu-id="b32b8-196">Para obtener información general de Windows sobre la compilación 18305, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-196">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-197">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-197">WSL</span></span>
* <span data-ttu-id="b32b8-198">pthreads pierden acceso a los archivos cuando sale el subproceso principal [GH 3589]</span><span class="sxs-lookup"><span data-stu-id="b32b8-198">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="b32b8-199">TIOCSCTTY debe omitir el parámetro "force", a menos que sea necesario [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="b32b8-199">TIOCSCTTY should ignore the “force” parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="b32b8-200">Mejoras en la línea de comandos de wsl.exe y adición de la funcionalidad de importación y exportación.</span><span class="sxs-lookup"><span data-stu-id="b32b8-200">wsl.exe command line improvements and addition of import / export functionality.</span></span>
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

## <a name="build-18277"></a><span data-ttu-id="b32b8-201">Compilación 18277</span><span class="sxs-lookup"><span data-stu-id="b32b8-201">Build 18277</span></span>
<span data-ttu-id="b32b8-202">Para obtener información general de Windows sobre la compilación 18277, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-202">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-203">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-203">WSL</span></span>
* <span data-ttu-id="b32b8-204">Corrección del error "Interfaz no compatible" que se presentó en la compilación 18272 [GH 3645]</span><span class="sxs-lookup"><span data-stu-id="b32b8-204">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="b32b8-205">Omite la marca MNT_FORCE para la llamada del sistema umount [GH 3605]</span><span class="sxs-lookup"><span data-stu-id="b32b8-205">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="b32b8-206">Cambia la interoperabilidad de WSL para usar la API de CreatePseudoConsole oficial</span><span class="sxs-lookup"><span data-stu-id="b32b8-206">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="b32b8-207">No mantiene ningún valor de tiempo de espera cuando se reinicia FUTEX_WAIT</span><span class="sxs-lookup"><span data-stu-id="b32b8-207">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="b32b8-208">Compilación 18272</span><span class="sxs-lookup"><span data-stu-id="b32b8-208">Build 18272</span></span>
<span data-ttu-id="b32b8-209">Para obtener información general de Windows sobre la compilación 18272, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-209">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-210">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-210">WSL</span></span>
* <span data-ttu-id="b32b8-211">**ADVERTENCIA:** Hay un problema en esta compilación que hace que WSL sea inoperable.</span><span class="sxs-lookup"><span data-stu-id="b32b8-211">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="b32b8-212">Al intentar iniciar la distribución, verás el error "Interfaz no compatible".</span><span class="sxs-lookup"><span data-stu-id="b32b8-212">When trying to launch your distribution you will see a “No such interface supported” error.</span></span> <span data-ttu-id="b32b8-213">El problema se ha solucionado y estará en la compilación del modo anticipado de Insider de la próxima semana.</span><span class="sxs-lookup"><span data-stu-id="b32b8-213">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="b32b8-214">Si has instalado esta compilación, puedes revertir a la compilación anterior de Windows mediante "Volver a la versión anterior de Windows 10" en Configuración-> Actualización y seguridad > Recuperación.</span><span class="sxs-lookup"><span data-stu-id="b32b8-214">If you've installed this build you can roll back to the previous Windows build using “Go back to the previous version of Windows 10” in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="b32b8-215">Compilación 18267</span><span class="sxs-lookup"><span data-stu-id="b32b8-215">Build 18267</span></span>
<span data-ttu-id="b32b8-216">Para obtener información general de Windows sobre la compilación 18267, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-216">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-217">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-217">WSL</span></span>
* <span data-ttu-id="b32b8-218">Corrección del problema por el que un proceso inerte no podía recogerse y permanecía de manera indefinida.</span><span class="sxs-lookup"><span data-stu-id="b32b8-218">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="b32b8-219">WslRegisterDistribution se bloquea si el mensaje de error supera la longitud máxima [GH 3592]</span><span class="sxs-lookup"><span data-stu-id="b32b8-219">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="b32b8-220">Permite que fsync se complete correctamente para los archivos de solo lectura en DrvFs [GH 3556]</span><span class="sxs-lookup"><span data-stu-id="b32b8-220">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="b32b8-221">Asegúrate de que los directorios /bin y /sbin existan antes de crear los vínculos simbólicos en ellos [GH 3584]</span><span class="sxs-lookup"><span data-stu-id="b32b8-221">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="b32b8-222">Se agregó un mecanismo de tiempo de espera de finalización de instancias para las instancias de WSL.</span><span class="sxs-lookup"><span data-stu-id="b32b8-222">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="b32b8-223">El tiempo de espera está establecido actualmente en 15 segundos, por lo que la instancia finalizará 15 segundos después de que termine el último proceso de WSL.</span><span class="sxs-lookup"><span data-stu-id="b32b8-223">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="b32b8-224">Para finalizar una distribución de inmediato, usa:</span><span class="sxs-lookup"><span data-stu-id="b32b8-224">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="b32b8-225">Compilación 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="b32b8-225">Build 17763 (1809)</span></span>
<span data-ttu-id="b32b8-226">Para obtener información general de Windows sobre la compilación 17763, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-226">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-227">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-227">WSL</span></span>
* <span data-ttu-id="b32b8-228">Comprobación de permisos de la llamada del sistema setpriority demasiado estricta para cambiar la misma prioridad de subprocesos [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="b32b8-228">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="b32b8-229">Asegúrate de que se use el tiempo de interrupción no sesgado para el tiempo de arranque para evitar que se devuelvan valores negativos para clock_gettime (CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="b32b8-229">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="b32b8-230">Controla los vínculos simbólicos en el intérprete binfmt de WSL [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="b32b8-230">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="b32b8-231">Mejor control de la limpieza de descriptores de archivo del líder del grupo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="b32b8-231">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="b32b8-232">Cambia WSL para usar KeQueryInterruptTimePrecise en lugar de KeQueryPerformanceCounter para evitar el desbordamiento [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="b32b8-232">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="b32b8-233">Ptrace attach puede producir un valor de devolución incorrecto de las llamadas del sistema [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="b32b8-233">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="b32b8-234">Corrección de varios problemas relacionados con AF_UNIX [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="b32b8-234">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="b32b8-235">Corrección del problema que podía provocar un error de interoperabilidad de WSL si el directorio de trabajo actual tiene menos de 5 caracteres de longitud [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="b32b8-235">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="b32b8-236">Evita las conexiones de bucle invertido con error con retraso de un segundo a puertos no existentes [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="b32b8-236">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="b32b8-237">Agrega el archivo de código auxiliar /proc/sys/fs/file-max [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="b32b8-237">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="b32b8-238">Información más precisa sobre el ámbito IPV6.</span><span class="sxs-lookup"><span data-stu-id="b32b8-238">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="b32b8-239">Compatibilidad con PR_SET_PTRACER [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="b32b8-239">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="b32b8-240">El sistema de archivos de canalización borra accidentalmente el evento epoll desencadenado por el borde [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="b32b8-240">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="b32b8-241">El ejecutable de Win32 iniciado mediante el vínculo simbólico de NTFS no respeta el nombre del vínculo simbólico [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="b32b8-241">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="b32b8-242">Compatibilidad mejorada con zombie [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="b32b8-242">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="b32b8-243">Agrega entradas de wsl.conf para controlar el comportamiento de interoperabilidad de Windows [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="b32b8-243">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="b32b8-244">La corrección para getsockname no siempre devuelve el tipo de familia de socket de UNIX [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="b32b8-244">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="b32b8-245">Agrega compatibilidad para TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="b32b8-245">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="b32b8-246">Los sockets sin bloqueo en el proceso de conexión deben devolver EAGAIN para los intentos de escritura [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="b32b8-246">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="b32b8-247">Compatibilidad con la interoperabilidad en VHD montados [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="b32b8-247">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="b32b8-248">Corrección del problema de comprobación de permisos en la carpeta raíz [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="b32b8-248">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="b32b8-249">Compatibilidad limitada para los ioctl de teclado TTY KDGKBTYPE, KDGKBMODE y KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="b32b8-249">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="b32b8-250">Las aplicaciones de interfaz de usuario de Windows deben ejecutarse incluso cuando se inician en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="b32b8-250">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="b32b8-251">Agrega la opción wsl -u o --user [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="b32b8-251">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="b32b8-252">Corrección de problemas de inicio de WSL cuando el inicio rápido está habilitado [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="b32b8-252">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="b32b8-253">Los sockets de UNIX deben conservar las credenciales del mismo nivel desconectadas [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="b32b8-253">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="b32b8-254">Sockets de UNIX sin bloqueo con error de manera indefinida con EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="b32b8-254">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="b32b8-255">case=off es el nuevo tipo de montaje drvfs predeterminado [GH 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="b32b8-255">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="b32b8-256">Consulta el [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) para más información.</span><span class="sxs-lookup"><span data-stu-id="b32b8-256">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="b32b8-257">Agrega wslconfig/terminate para detener las distribuciones en ejecución.</span><span class="sxs-lookup"><span data-stu-id="b32b8-257">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="b32b8-258">Corrección del problema con las entradas del menú contextual del shell de WSL que no controlan correctamente las rutas de acceso con espacios.</span><span class="sxs-lookup"><span data-stu-id="b32b8-258">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="b32b8-259">Expone la distinción de mayúsculas y minúsculas por directorio como atributo extendido</span><span class="sxs-lookup"><span data-stu-id="b32b8-259">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="b32b8-260">ARM64: Emula las operaciones de mantenimiento de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="b32b8-260">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="b32b8-261">Resuelve un [problema de dotnet](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="b32b8-261">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="b32b8-262">DrvFs: solo caracteres con escape eliminado en el intervalo privado que corresponden a un carácter de escape.</span><span class="sxs-lookup"><span data-stu-id="b32b8-262">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="b32b8-263">Corrección error de desviación por uno en la validación de longitud del intérprete del analizador ELF [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="b32b8-263">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="b32b8-264">Temporizadores absolutos de WSL con una hora en el pasado no se activan [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="b32b8-264">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="b32b8-265">Asegúrate de que los puntos de reanálisis recién creados se muestren como tales en el directorio principal.</span><span class="sxs-lookup"><span data-stu-id="b32b8-265">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="b32b8-266">Crea de forma atómica directorios con distinción entre mayúsculas y minúsculas en DrvFs.</span><span class="sxs-lookup"><span data-stu-id="b32b8-266">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="b32b8-267">Se ha corregido un problema adicional en el que las operaciones de varios subprocesos podían devolver ENOENT, aunque el archivo existiese.</span><span class="sxs-lookup"><span data-stu-id="b32b8-267">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="b32b8-268">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="b32b8-268">[GH 2712]</span></span>
* <span data-ttu-id="b32b8-269">Se corrigió un error de inicio de WSL cuando UMCI está habilitado.</span><span class="sxs-lookup"><span data-stu-id="b32b8-269">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="b32b8-270">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="b32b8-270">[GH 3020]</span></span>
* <span data-ttu-id="b32b8-271">Agrega el menú contextual del explorador para iniciar WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="b32b8-271">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="b32b8-272">Para usar, mantén presionada la tecla Mayús y haz clic con el botón derecho en una ventana del explorador.</span><span class="sxs-lookup"><span data-stu-id="b32b8-272">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="b32b8-273">Corrección del comportamiento de no bloqueo de sockets de UNIX [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="b32b8-273">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="b32b8-274">Corrección del comando NETLINK que se bloquea, tal como se muestra en GH 2026.</span><span class="sxs-lookup"><span data-stu-id="b32b8-274">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="b32b8-275">Agrega compatibilidad para las marcas de propagación de montaje [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="b32b8-275">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="b32b8-276">Corrección del problema de truncamiento que no provoca eventos inotify [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="b32b8-276">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="b32b8-277">Agrega la opción --exec a wsl.exe para invocar un solo binario sin un shell.</span><span class="sxs-lookup"><span data-stu-id="b32b8-277">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="b32b8-278">Agrega la opción --distribution a wsl.exe para seleccionar una distribución específica.</span><span class="sxs-lookup"><span data-stu-id="b32b8-278">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="b32b8-279">Compatibilidad limitada para dmesg.</span><span class="sxs-lookup"><span data-stu-id="b32b8-279">Limited support for dmesg.</span></span> <span data-ttu-id="b32b8-280">Ahora, las aplicaciones pueden registrarse en dmesg.</span><span class="sxs-lookup"><span data-stu-id="b32b8-280">Applications can now log to dmesg.</span></span> <span data-ttu-id="b32b8-281">El controlador WSL registra información limitada en dmesg.</span><span class="sxs-lookup"><span data-stu-id="b32b8-281">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="b32b8-282">En el futuro, esto puede extenderse para llevar a cabo otros diagnósticos e información del controlador.</span><span class="sxs-lookup"><span data-stu-id="b32b8-282">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="b32b8-283">Nota: dmesg se admite actualmente a través de la interfaz de dispositivo `/dev/kmsg`.</span><span class="sxs-lookup"><span data-stu-id="b32b8-283">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="b32b8-284">Aún no se admite la interfaz syscall `syslog`.</span><span class="sxs-lookup"><span data-stu-id="b32b8-284">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="b32b8-285">Y, por lo tanto, algunas de las opciones de la línea de comandos de `dmesg`, como `-S` y `-C`, no funcionan.</span><span class="sxs-lookup"><span data-stu-id="b32b8-285">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="b32b8-286">Cambia el gid y el modo de dispositivos serie predeterminados para que coincidan con los nativos [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="b32b8-286">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="b32b8-287">DrvFs ahora admite atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="b32b8-287">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="b32b8-288">Nota: DrvFs tiene algunas limitaciones en cuanto al nombre de los atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="b32b8-288">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="b32b8-289">No se permiten algunos caracteres (como "/", ":" y "\*"), y los nombres de atributos extendidos no distinguen mayúsculas de minúsculas en DrvFs</span><span class="sxs-lookup"><span data-stu-id="b32b8-289">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="b32b8-290">Compilación 18252 (saltar)</span><span class="sxs-lookup"><span data-stu-id="b32b8-290">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="b32b8-291">Para obtener información general de Windows sobre la compilación 18252, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-291">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-292">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-292">WSL</span></span>
* <span data-ttu-id="b32b8-293">Traslado de los binarios init y bsdtar fuera del archivo dll lxssmanager y a una carpeta de herramientas independiente</span><span class="sxs-lookup"><span data-stu-id="b32b8-293">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="b32b8-294">Corrección de la carrera en torno al cierre del descriptor de archivo cuando se usa CLONE_FILES</span><span class="sxs-lookup"><span data-stu-id="b32b8-294">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="b32b8-295">Controla campos opcionales en /proc/pid/mountinfo al traducir rutas de DrvFs</span><span class="sxs-lookup"><span data-stu-id="b32b8-295">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="b32b8-296">Permite que DrvFs mknod se complete correctamente sin compatibilidad con metadatos para S_IFREG</span><span class="sxs-lookup"><span data-stu-id="b32b8-296">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="b32b8-297">Los archivos de solo lectura creados en DrvFs deben tener el atributo readonly establecido [GH 3411]</span><span class="sxs-lookup"><span data-stu-id="b32b8-297">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="b32b8-298">Agrega el asistente /sbin/mount.drvfs para controlar el montaje de DrvFs</span><span class="sxs-lookup"><span data-stu-id="b32b8-298">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="b32b8-299">Usa el cambio de nombre de POSIX en DrvFs.</span><span class="sxs-lookup"><span data-stu-id="b32b8-299">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="b32b8-300">Permite la traducción de rutas de acceso en volúmenes sin un GUID de volumen.</span><span class="sxs-lookup"><span data-stu-id="b32b8-300">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="b32b8-301">Compilación 17738 (rápida)</span><span class="sxs-lookup"><span data-stu-id="b32b8-301">Build 17738 (Fast)</span></span>
<span data-ttu-id="b32b8-302">Para obtener información general de Windows sobre la compilación 17738, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-302">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-303">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-303">WSL</span></span>
* <span data-ttu-id="b32b8-304">Comprobación de permisos de la llamada del sistema setpriority demasiado estricta para cambiar la misma prioridad de subprocesos [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="b32b8-304">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="b32b8-305">Asegúrate de que se use el tiempo de interrupción no sesgado para el tiempo de arranque para evitar que se devuelvan valores negativos para clock_gettime (CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="b32b8-305">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="b32b8-306">Controla los vínculos simbólicos en el intérprete binfmt de WSL [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="b32b8-306">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="b32b8-307">Mejor control de la limpieza de descriptores de archivo del líder del grupo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="b32b8-307">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="b32b8-308">Compilación 17728 (rápida)</span><span class="sxs-lookup"><span data-stu-id="b32b8-308">Build 17728 (Fast)</span></span>
<span data-ttu-id="b32b8-309">Para obtener información general de Windows sobre la compilación 17728, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-309">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-310">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-310">WSL</span></span>
* <span data-ttu-id="b32b8-311">Cambia WSL para usar KeQueryInterruptTimePrecise en lugar de KeQueryPerformanceCounter para evitar el desbordamiento [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="b32b8-311">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="b32b8-312">Ptrace attach puede producir un valor de devolución incorrecto de las llamadas del sistema [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="b32b8-312">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="b32b8-313">Corrección de varios problemas relacionados con AF_UNIX [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="b32b8-313">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="b32b8-314">Corrección del problema que podía provocar un error de interoperabilidad de WSL si el directorio de trabajo actual tiene menos de 5 caracteres de longitud [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="b32b8-314">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="b32b8-315">Compilación 18204 (saltar)</span><span class="sxs-lookup"><span data-stu-id="b32b8-315">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="b32b8-316">Para obtener información general de Windows sobre la compilación 18204, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-316">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-317">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-317">WSL</span></span>
* <span data-ttu-id="b32b8-318">El sistema de archivos de canalización borra accidentalmente el evento epoll desencadenado por el borde [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="b32b8-318">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="b32b8-319">El ejecutable de Win32 iniciado mediante el vínculo simbólico de NTFS no respeta el nombre del vínculo simbólico [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="b32b8-319">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="b32b8-320">Compilación 17723 (rápida)</span><span class="sxs-lookup"><span data-stu-id="b32b8-320">Build 17723 (Fast)</span></span>
<span data-ttu-id="b32b8-321">Para obtener información general de Windows sobre la compilación 17723, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-321">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-322">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-322">WSL</span></span>
* <span data-ttu-id="b32b8-323">Evita las conexiones de bucle invertido con error con retraso de un segundo a puertos no existentes [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="b32b8-323">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="b32b8-324">Agrega el archivo de código auxiliar /proc/sys/fs/file-max [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="b32b8-324">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="b32b8-325">Información más precisa sobre el ámbito IPV6.</span><span class="sxs-lookup"><span data-stu-id="b32b8-325">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="b32b8-326">Compatibilidad con PR_SET_PTRACER [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="b32b8-326">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="b32b8-327">El sistema de archivos de canalización borra accidentalmente el evento epoll desencadenado por el borde [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="b32b8-327">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="b32b8-328">El ejecutable de Win32 iniciado mediante el vínculo simbólico de NTFS no respeta el nombre del vínculo simbólico [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="b32b8-328">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="b32b8-329">Compilación 17713</span><span class="sxs-lookup"><span data-stu-id="b32b8-329">Build 17713</span></span>
<span data-ttu-id="b32b8-330">Para obtener información general de Windows sobre la compilación 17713, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-330">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-331">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-331">WSL</span></span>
* <span data-ttu-id="b32b8-332">Compatibilidad mejorada con zombie [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="b32b8-332">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="b32b8-333">Agrega entradas de wsl.conf para controlar el comportamiento de interoperabilidad de Windows [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="b32b8-333">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="b32b8-334">La corrección para getsockname no siempre devuelve el tipo de familia de socket de UNIX [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="b32b8-334">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="b32b8-335">Agrega compatibilidad para TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="b32b8-335">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="b32b8-336">Los sockets sin bloqueo en el proceso de conexión deben devolver EAGAIN para los intentos de escritura [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="b32b8-336">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="b32b8-337">Compatibilidad con la interoperabilidad en VHD montados [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="b32b8-337">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="b32b8-338">Corrección del problema de comprobación de permisos en la carpeta raíz [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="b32b8-338">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="b32b8-339">Compatibilidad limitada para los ioctl de teclado TTY KDGKBTYPE, KDGKBMODE y KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="b32b8-339">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="b32b8-340">Las aplicaciones de interfaz de usuario de Windows deben ejecutarse incluso cuando se inician en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="b32b8-340">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="b32b8-341">Compilación 17704</span><span class="sxs-lookup"><span data-stu-id="b32b8-341">Build 17704</span></span>
<span data-ttu-id="b32b8-342">Para obtener información general de Windows sobre la compilación 17704, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-342">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-343">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-343">WSL</span></span>
* <span data-ttu-id="b32b8-344">Agrega la opción wsl -u o --user [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="b32b8-344">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="b32b8-345">Corrección de problemas de inicio de WSL cuando el inicio rápido está habilitado [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="b32b8-345">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="b32b8-346">Los sockets de UNIX deben conservar las credenciales del mismo nivel desconectadas [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="b32b8-346">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="b32b8-347">Sockets de UNIX sin bloqueo con error de manera indefinida con EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="b32b8-347">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="b32b8-348">case=off es el nuevo tipo de montaje drvfs predeterminado [GH 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="b32b8-348">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="b32b8-349">Consulta el [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) para más información.</span><span class="sxs-lookup"><span data-stu-id="b32b8-349">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="b32b8-350">Agrega wslconfig/terminate para detener las distribuciones en ejecución.</span><span class="sxs-lookup"><span data-stu-id="b32b8-350">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="b32b8-351">Compilación 17692</span><span class="sxs-lookup"><span data-stu-id="b32b8-351">Build 17692</span></span>
<span data-ttu-id="b32b8-352">Para obtener información general de Windows sobre la compilación 17692, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span><span class="sxs-lookup"><span data-stu-id="b32b8-352">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-353">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-353">WSL</span></span>
* <span data-ttu-id="b32b8-354">Corrección del problema con las entradas del menú contextual del shell de WSL que no controlan correctamente las rutas de acceso con espacios.</span><span class="sxs-lookup"><span data-stu-id="b32b8-354">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="b32b8-355">Expone la distinción de mayúsculas y minúsculas por directorio como atributo extendido</span><span class="sxs-lookup"><span data-stu-id="b32b8-355">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="b32b8-356">ARM64: Emula las operaciones de mantenimiento de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="b32b8-356">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="b32b8-357">Resuelve un [problema de dotnet](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="b32b8-357">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="b32b8-358">DrvFs: solo caracteres con escape eliminado en el intervalo privado que corresponden a un carácter de escape.</span><span class="sxs-lookup"><span data-stu-id="b32b8-358">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="b32b8-359">Compilación 17686</span><span class="sxs-lookup"><span data-stu-id="b32b8-359">Build 17686</span></span>
<span data-ttu-id="b32b8-360">Para obtener información general de Windows sobre la compilación 17686, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span><span class="sxs-lookup"><span data-stu-id="b32b8-360">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-361">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-361">WSL</span></span>
* <span data-ttu-id="b32b8-362">Corrección error de desviación por uno en la validación de longitud del intérprete del analizador ELF [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="b32b8-362">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="b32b8-363">Temporizadores absolutos de WSL con una hora en el pasado no se activan [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="b32b8-363">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="b32b8-364">Asegúrate de que los puntos de reanálisis recién creados se muestren como tales en el directorio principal.</span><span class="sxs-lookup"><span data-stu-id="b32b8-364">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="b32b8-365">Crea de forma atómica directorios con distinción entre mayúsculas y minúsculas en DrvFs.</span><span class="sxs-lookup"><span data-stu-id="b32b8-365">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="b32b8-366">Compilación 17677</span><span class="sxs-lookup"><span data-stu-id="b32b8-366">Build 17677</span></span>
<span data-ttu-id="b32b8-367">Para obtener información general de Windows sobre la compilación 17677, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-367">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-368">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-368">WSL</span></span>
* <span data-ttu-id="b32b8-369">Se ha corregido un problema adicional en el que las operaciones de varios subprocesos podían devolver ENOENT, aunque el archivo existiese.</span><span class="sxs-lookup"><span data-stu-id="b32b8-369">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="b32b8-370">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="b32b8-370">[GH 2712]</span></span>
* <span data-ttu-id="b32b8-371">Se corrigió un error de inicio de WSL cuando UMCI está habilitado.</span><span class="sxs-lookup"><span data-stu-id="b32b8-371">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="b32b8-372">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="b32b8-372">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="b32b8-373">Compilación 17666</span><span class="sxs-lookup"><span data-stu-id="b32b8-373">Build 17666</span></span>
<span data-ttu-id="b32b8-374">Para obtener información general de Windows sobre la compilación 17666, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-374">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-375">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-375">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="b32b8-376">ADVERTENCIA: Hay un problema que impide que WSL se ejecute en algunos conjuntos de chips AMD [GH 3134].</span><span class="sxs-lookup"><span data-stu-id="b32b8-376">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="b32b8-377">Hay una corrección lista y en camino en la rama de compilación de Insider.</span><span class="sxs-lookup"><span data-stu-id="b32b8-377">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="b32b8-378">Agrega el menú contextual del explorador para iniciar WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="b32b8-378">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="b32b8-379">Para usar, mantén presionada la tecla Mayús y haz clic con el botón derecho en una ventana del explorador.</span><span class="sxs-lookup"><span data-stu-id="b32b8-379">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="b32b8-380">Corrección del comportamiento de no bloqueo de sockets de Unix [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="b32b8-380">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="b32b8-381">Corrección del comando NETLINK que se bloquea, tal como se muestra en GH 2026.</span><span class="sxs-lookup"><span data-stu-id="b32b8-381">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="b32b8-382">Agrega compatibilidad para las marcas de propagación de montaje [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="b32b8-382">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="b32b8-383">Corrección del problema de truncamiento que no provoca eventos inotify [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="b32b8-383">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="b32b8-384">Agrega la opción --exec a wsl.exe para invocar un solo binario sin un shell.</span><span class="sxs-lookup"><span data-stu-id="b32b8-384">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="b32b8-385">Agrega la opción --distribution a wsl.exe para seleccionar una distribución específica.</span><span class="sxs-lookup"><span data-stu-id="b32b8-385">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="b32b8-386">Compilación 17655 (saltar)</span><span class="sxs-lookup"><span data-stu-id="b32b8-386">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="b32b8-387">Para obtener información general de Windows sobre la compilación 17655, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-387">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-388">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-388">WSL</span></span>
* <span data-ttu-id="b32b8-389">Compatibilidad limitada para dmesg.</span><span class="sxs-lookup"><span data-stu-id="b32b8-389">Limited support for dmesg.</span></span> <span data-ttu-id="b32b8-390">Ahora, las aplicaciones pueden registrarse en dmesg.</span><span class="sxs-lookup"><span data-stu-id="b32b8-390">Applications can now log to dmesg.</span></span> <span data-ttu-id="b32b8-391">El controlador WSL registra información limitada en dmesg.</span><span class="sxs-lookup"><span data-stu-id="b32b8-391">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="b32b8-392">En el futuro, esto puede extenderse para llevar a cabo otros diagnósticos e información del controlador.</span><span class="sxs-lookup"><span data-stu-id="b32b8-392">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="b32b8-393">Nota: dmesg se admite actualmente a través de la interfaz de dispositivo `/dev/kmsg`.</span><span class="sxs-lookup"><span data-stu-id="b32b8-393">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="b32b8-394">Aún no se admite la interfaz sycall `syslog`.</span><span class="sxs-lookup"><span data-stu-id="b32b8-394">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="b32b8-395">Y, por lo tanto, algunas de las opciones de la línea de comandos de `dmesg`, como `-S` y `-C`, no funcionan.</span><span class="sxs-lookup"><span data-stu-id="b32b8-395">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="b32b8-396">Se ha corregido un problema en el que las operaciones de varios subprocesos podían devolver ENOENT, aunque el archivo existiese.</span><span class="sxs-lookup"><span data-stu-id="b32b8-396">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="b32b8-397">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="b32b8-397">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="b32b8-398">Compilación 17639 (saltar)</span><span class="sxs-lookup"><span data-stu-id="b32b8-398">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="b32b8-399">Para obtener información general de Windows sobre la compilación 17639, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-399">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-400">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-400">WSL</span></span>
* <span data-ttu-id="b32b8-401">Cambia el gid y el modo de dispositivos serie predeterminados para que coincidan con los nativos [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="b32b8-401">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="b32b8-402">DrvFs ahora admite atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="b32b8-402">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="b32b8-403">Nota: DrvFs tiene algunas limitaciones en cuanto al nombre de los atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="b32b8-403">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="b32b8-404">En particular, no se permiten algunos caracteres (como "/", ":" y "\*"), y los nombres de atributos extendidos no distinguen mayúsculas de minúsculas en DrvFs</span><span class="sxs-lookup"><span data-stu-id="b32b8-404">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="b32b8-405">Compilación 17133 (rápida)</span><span class="sxs-lookup"><span data-stu-id="b32b8-405">Build 17133 (Fast)</span></span>
<span data-ttu-id="b32b8-406">Para obtener información general de Windows sobre la compilación 17133, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-406">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-407">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-407">WSL</span></span>
* <span data-ttu-id="b32b8-408">Corrección de un bloqueo en WSL.</span><span class="sxs-lookup"><span data-stu-id="b32b8-408">Fix for hang in WSL.</span></span> <span data-ttu-id="b32b8-409">[GH 3039, 3034]</span><span class="sxs-lookup"><span data-stu-id="b32b8-409">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="b32b8-410">Compilación 17128 (rápida)</span><span class="sxs-lookup"><span data-stu-id="b32b8-410">Build 17128 (Fast)</span></span>
<span data-ttu-id="b32b8-411">Para obtener información general de Windows sobre la compilación 17128, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-411">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-412">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-412">WSL</span></span>
* <span data-ttu-id="b32b8-413">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b32b8-413">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="b32b8-414">Compilación 17627 (saltar)</span><span class="sxs-lookup"><span data-stu-id="b32b8-414">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="b32b8-415">Para obtener información general de Windows sobre la compilación 17627, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-415">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-416">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-416">WSL</span></span>
* <span data-ttu-id="b32b8-417">Agrega compatibilidad para las operaciones compatibles con pi de Futex.</span><span class="sxs-lookup"><span data-stu-id="b32b8-417">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="b32b8-418">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="b32b8-418">[GH 1006]</span></span>
    * <span data-ttu-id="b32b8-419">Ten en cuenta que las prioridades no son actualmente una característica admitida de WSL, por lo que hay limitaciones, pero el uso estándar debería estar desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="b32b8-419">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="b32b8-420">Compatibilidad con el Firewall de Windows para los procesos de WSL.</span><span class="sxs-lookup"><span data-stu-id="b32b8-420">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="b32b8-421">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="b32b8-421">[GH 1852]</span></span>
    * <span data-ttu-id="b32b8-422">Por ejemplo, para permitir que el proceso de Python de WSL escuche en cualquier puerto, use el cmd de Windows con privilegios elevados: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span><span class="sxs-lookup"><span data-stu-id="b32b8-422">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="b32b8-423">Para más información sobre cómo agregar reglas de firewall, consulte el [vínculo](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span><span class="sxs-lookup"><span data-stu-id="b32b8-423">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="b32b8-424">Respeta el shell predeterminado del usuario al usar wsl.exe.</span><span class="sxs-lookup"><span data-stu-id="b32b8-424">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="b32b8-425">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="b32b8-425">[GH 2372]</span></span>
* <span data-ttu-id="b32b8-426">Informa de todas las interfaces de red como Ethernet.</span><span class="sxs-lookup"><span data-stu-id="b32b8-426">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="b32b8-427">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="b32b8-427">[GH 2996]</span></span>
* <span data-ttu-id="b32b8-428">Mejor control del archivo /etc/passwd dañado.</span><span class="sxs-lookup"><span data-stu-id="b32b8-428">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="b32b8-429">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="b32b8-429">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="b32b8-430">Console</span><span class="sxs-lookup"><span data-stu-id="b32b8-430">Console</span></span>
* <span data-ttu-id="b32b8-431">Sin correcciones.</span><span class="sxs-lookup"><span data-stu-id="b32b8-431">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-432">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-432">LTP Results:</span></span>
<span data-ttu-id="b32b8-433">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="b32b8-433">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="b32b8-434">Compilación 17618 (saltar)</span><span class="sxs-lookup"><span data-stu-id="b32b8-434">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="b32b8-435">Para obtener información general de Windows sobre la compilación 17618, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-435">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-436">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-436">WSL</span></span>
* <span data-ttu-id="b32b8-437">Presenta la funcionalidad de pseudoconsola para la interoperabilidad de NT [GH 988, 1366, 1433, 1542, 2370, 2406].</span><span class="sxs-lookup"><span data-stu-id="b32b8-437">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="b32b8-438">El mecanismo de instalación heredado (lxrun.exe) está en desuso.</span><span class="sxs-lookup"><span data-stu-id="b32b8-438">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="b32b8-439">El mecanismo admitido para la instalación de distribuciones es a través de Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="b32b8-439">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="b32b8-440">Console</span><span class="sxs-lookup"><span data-stu-id="b32b8-440">Console</span></span>
* <span data-ttu-id="b32b8-441">Sin correcciones.</span><span class="sxs-lookup"><span data-stu-id="b32b8-441">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-442">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-442">LTP Results:</span></span>
<span data-ttu-id="b32b8-443">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="b32b8-443">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="b32b8-444">Compilación 17110</span><span class="sxs-lookup"><span data-stu-id="b32b8-444">Build 17110</span></span>
<span data-ttu-id="b32b8-445">Para obtener información general de Windows sobre la compilación 17110, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-445">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-446">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-446">WSL</span></span>
* <span data-ttu-id="b32b8-447">Permite que/init finalice desde Windows [GH 2928].</span><span class="sxs-lookup"><span data-stu-id="b32b8-447">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="b32b8-448">DrvFs ahora usa la distinción de mayúsculas y minúsculas por directorio de manera predeterminada (equivalente a la opción de montaje "case=dir").</span><span class="sxs-lookup"><span data-stu-id="b32b8-448">DrvFs now uses per-directory case sensitivity by default (equivalent to the “case=dir” mount option).</span></span>
    * <span data-ttu-id="b32b8-449">El uso de "case=force" (el comportamiento anterior) requiere el establecimiento de una clave del Registro.</span><span class="sxs-lookup"><span data-stu-id="b32b8-449">Using “case=force” (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="b32b8-450">Ejecuta el siguiente comando para habilitar "case=force" si necesitas usarlo: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span><span class="sxs-lookup"><span data-stu-id="b32b8-450">Run the following command to enable “case=force” if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="b32b8-451">Si tienes directorios existentes creados con WSL en una versión anterior de Windows que deben distinguir entre mayúsculas y minúsculas, usa fsutil.exe para marcarlos con distinción de mayúsculas y minúsculas:fsutil.exe file setcasesensitiveinfo <path> enable</span><span class="sxs-lookup"><span data-stu-id="b32b8-451">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="b32b8-452">La llamada del sistema uname devuelve cadenas de finalización NULL.</span><span class="sxs-lookup"><span data-stu-id="b32b8-452">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="b32b8-453">Console</span><span class="sxs-lookup"><span data-stu-id="b32b8-453">Console</span></span>
* <span data-ttu-id="b32b8-454">Sin correcciones.</span><span class="sxs-lookup"><span data-stu-id="b32b8-454">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-455">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-455">LTP Results:</span></span>
<span data-ttu-id="b32b8-456">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="b32b8-456">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="b32b8-457">Compilación 17107</span><span class="sxs-lookup"><span data-stu-id="b32b8-457">Build 17107</span></span>
<span data-ttu-id="b32b8-458">Para obtener información general de Windows sobre la compilación 17107, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-458">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-459">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-459">WSL</span></span>
* <span data-ttu-id="b32b8-460">Compatibilidad con TCSETSF y TCSETSW en los puntos de conexión de master pty [GH 2552].</span><span class="sxs-lookup"><span data-stu-id="b32b8-460">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="b32b8-461">Iniciar procesos de interoperabilidad simultáneos puede dar lugar a EINVAL [GH 2813].</span><span class="sxs-lookup"><span data-stu-id="b32b8-461">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="b32b8-462">Corrección de PTRACE_ATTACH para mostrar el estado de seguimiento adecuado en /proc/pid/status.</span><span class="sxs-lookup"><span data-stu-id="b32b8-462">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="b32b8-463">Corrección de la carrera en la que los procesos de corta duración clonados con las marcas CLEARTID y SETTID podrían salir sin borrar la dirección de TID.</span><span class="sxs-lookup"><span data-stu-id="b32b8-463">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="b32b8-464">Muestra un mensaje al actualizar los directorios del sistema de archivos de Linux al pasar de una compilación anterior a 17093.</span><span class="sxs-lookup"><span data-stu-id="b32b8-464">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="b32b8-465">Para más detalles sobre los cambios del sistema de archivos de 17093, consulta las notas de la versión de [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span><span class="sxs-lookup"><span data-stu-id="b32b8-465">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="b32b8-466">Console</span><span class="sxs-lookup"><span data-stu-id="b32b8-466">Console</span></span>
* <span data-ttu-id="b32b8-467">Sin correcciones.</span><span class="sxs-lookup"><span data-stu-id="b32b8-467">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-468">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-468">LTP Results:</span></span>
<span data-ttu-id="b32b8-469">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="b32b8-469">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="b32b8-470">Compilación 17101</span><span class="sxs-lookup"><span data-stu-id="b32b8-470">Build 17101</span></span>
<span data-ttu-id="b32b8-471">Para obtener información general de Windows sobre la compilación 17101, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-471">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-472">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-472">WSL</span></span>
* <span data-ttu-id="b32b8-473">Compatibilidad con signalfd.</span><span class="sxs-lookup"><span data-stu-id="b32b8-473">Support for signalfd.</span></span> <span data-ttu-id="b32b8-474">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="b32b8-474">[GH 129]</span></span>
* <span data-ttu-id="b32b8-475">Admite nombres de archivo que contienen caracteres NTFS no válidos mediante su codificación como caracteres Unicode privados.</span><span class="sxs-lookup"><span data-stu-id="b32b8-475">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="b32b8-476">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="b32b8-476">[GH 1514]</span></span>
* <span data-ttu-id="b32b8-477">El montaje automático se revertirá al modo de solo lectura cuando no se admita la escritura.</span><span class="sxs-lookup"><span data-stu-id="b32b8-477">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="b32b8-478">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="b32b8-478">[GH 2603]</span></span>
* <span data-ttu-id="b32b8-479">Permite pegar los pares suplentes Unicode (como los caracteres emoji).</span><span class="sxs-lookup"><span data-stu-id="b32b8-479">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="b32b8-480">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="b32b8-480">[GH 2765]</span></span>
* <span data-ttu-id="b32b8-481">Los pseudoarchivos en /proc y /sys deben devolver los valores read ready y write ready de select, poll, epoll, etc. [GH 2838]</span><span class="sxs-lookup"><span data-stu-id="b32b8-481">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="b32b8-482">Corrección de un problema que podría hacer que el servicio pudiera entrar en un bucle infinito cuando el Registro se haya alterado o esté dañado.</span><span class="sxs-lookup"><span data-stu-id="b32b8-482">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="b32b8-483">Corrección de los mensajes de netlink para trabajar con la versión más reciente (de nivel superior 4.14) de iproute2.</span><span class="sxs-lookup"><span data-stu-id="b32b8-483">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="b32b8-484">Console</span><span class="sxs-lookup"><span data-stu-id="b32b8-484">Console</span></span>
* <span data-ttu-id="b32b8-485">Sin correcciones.</span><span class="sxs-lookup"><span data-stu-id="b32b8-485">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-486">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-486">LTP Results:</span></span>
<span data-ttu-id="b32b8-487">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="b32b8-487">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="b32b8-488">Compilación 17093</span><span class="sxs-lookup"><span data-stu-id="b32b8-488">Build 17093</span></span>
<span data-ttu-id="b32b8-489">Para obtener información general de Windows sobre la compilación 17093, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-489">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="b32b8-490">Importante:</span><span class="sxs-lookup"><span data-stu-id="b32b8-490">Important:</span></span>
<span data-ttu-id="b32b8-491">Al iniciar WSL por primera vez después de actualizar a esta compilación, tiene que hacer algún trabajo para actualizar los directorios del sistema de archivos de Linux.</span><span class="sxs-lookup"><span data-stu-id="b32b8-491">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="b32b8-492">Esto puede tardar varios minutos, por lo que es posible que WSL se inicie lentamente.</span><span class="sxs-lookup"><span data-stu-id="b32b8-492">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="b32b8-493">Esto solo debería ocurrir una vez por cada distribución que haya instalado desde Store.</span><span class="sxs-lookup"><span data-stu-id="b32b8-493">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="b32b8-494">Compatibilidad mejorada de distinción de mayúsculas y minúsculas en DrvFs.</span><span class="sxs-lookup"><span data-stu-id="b32b8-494">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="b32b8-495">DrvFs admite ahora la distinción de mayúsculas y minúsculas por directorio.</span><span class="sxs-lookup"><span data-stu-id="b32b8-495">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="b32b8-496">Se trata de una nueva marca que se puede establecer en los directorios para indicar que todas las operaciones de esos directorios deben tratarse como con distinción de mayúsculas y minúsculas, lo que permite que las aplicaciones de Windows abran correctamente archivos que solo difieren en mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b32b8-496">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="b32b8-497">DrvFs tiene nuevas opciones de montaje que controlan la distinción de mayúsculas y minúsculas por directorio.</span><span class="sxs-lookup"><span data-stu-id="b32b8-497">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="b32b8-498">case=force: todos los directorios se tratan con distinción de mayúsculas y minúsculas (excepto la raíz de la unidad).</span><span class="sxs-lookup"><span data-stu-id="b32b8-498">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="b32b8-499">Los nuevos directorios creados con WSL se marcan con distinción de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b32b8-499">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="b32b8-500">Este es el comportamiento heredado, excepto para marcar los nuevos directorios que distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b32b8-500">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="b32b8-501">case=dir: solo los directorios con la marca de distinción de mayúsculas y minúsculas por directorio se tratan como que distinguen mayúsculas de minúsculas; los otros directorios no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b32b8-501">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="b32b8-502">Los nuevos directorios creados con WSL se marcan con distinción de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b32b8-502">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="b32b8-503">case=off: solo los directorios con la marca de distinción de mayúsculas y minúsculas por directorio se tratan como que distinguen mayúsculas de minúsculas; los otros directorios no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b32b8-503">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="b32b8-504">Los nuevos directorios creados con WSL se marcan como sin distinción de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b32b8-504">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="b32b8-505">Nota: Los directorios creados por WSL en versiones anteriores no tienen esta marca establecida, por lo que no se tratará como con distinción entre mayúsculas y minúsculas si usas la opción "case=dir".</span><span class="sxs-lookup"><span data-stu-id="b32b8-505">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the “case=dir” option.</span></span> <span data-ttu-id="b32b8-506">Próximamente se presentará una manera de establecer esta marca en los directorios existentes.</span><span class="sxs-lookup"><span data-stu-id="b32b8-506">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="b32b8-507">Ejemplo de montaje con estas opciones (en el caso de las unidades existentes, primero debes desmontar antes de poder montar con distintas opciones): sudo mount -t drvfs C: /mnt/c -o case=dir</span><span class="sxs-lookup"><span data-stu-id="b32b8-507">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="b32b8-508">Por ahora, case=force sigue siendo la opción predeterminada.</span><span class="sxs-lookup"><span data-stu-id="b32b8-508">For now, case=force is still the default option.</span></span> <span data-ttu-id="b32b8-509">Se cambiará a case=dir en el futuro.</span><span class="sxs-lookup"><span data-stu-id="b32b8-509">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="b32b8-510">Ahora puedes usar barras diagonales en las rutas de acceso de Windows al montar DrvFs, por ejemplo: sudo mount -t drvfs //server/share /mnt/share</span><span class="sxs-lookup"><span data-stu-id="b32b8-510">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="b32b8-511">WSL ahora procesa el archivo /etc/fstab durante el inicio de la instancia [GH 2636].</span><span class="sxs-lookup"><span data-stu-id="b32b8-511">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="b32b8-512">Esto se hace antes de montar automáticamente las unidades de DrvFs; las unidades que ya se hayan montado mediante fstab no se volverán a montar automáticamente, lo que te permite cambiar el punto de montaje para unidades específicas.</span><span class="sxs-lookup"><span data-stu-id="b32b8-512">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="b32b8-513">Este comportamiento se puede desactivar mediante wsl.conf.</span><span class="sxs-lookup"><span data-stu-id="b32b8-513">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="b32b8-514">Los archivos mount, mountinfo y mountstats de /proc convierten correctamente en caracteres especiales, como barras diagonales inversas y espacios [GH 2799]</span><span class="sxs-lookup"><span data-stu-id="b32b8-514">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="b32b8-515">Los archivos especiales creados con DrvFs, como los vínculos simbólicos de WSL, o fifos y sockets cuando los metadatos están habilitados, ahora se pueden copiar y mover desde Windows.</span><span class="sxs-lookup"><span data-stu-id="b32b8-515">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="b32b8-516">WSL es más configurable con wsl.conf</span><span class="sxs-lookup"><span data-stu-id="b32b8-516">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="b32b8-517">Hemos agregado un método para que configures automáticamente cierta funcionalidad en WSL que se aplicará cada vez que inicies el subsistema.</span><span class="sxs-lookup"><span data-stu-id="b32b8-517">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="b32b8-518">Esto incluye opciones de montaje automático y configuración de red.</span><span class="sxs-lookup"><span data-stu-id="b32b8-518">This includes automount options and network configuration.</span></span> <span data-ttu-id="b32b8-519">Obtén más información en la publicación de blog en https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="b32b8-519">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="af_unix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="b32b8-520">AF_UNIX permite conexiones de socket entre procesos de Linux en procesos nativos de WSL y Windows</span><span class="sxs-lookup"><span data-stu-id="b32b8-520">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="b32b8-521">Las aplicaciones de WSL y Windows ahora pueden comunicarse entre sí a través de sockets de Unix.</span><span class="sxs-lookup"><span data-stu-id="b32b8-521">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="b32b8-522">Imagina que quieres ejecutar un servicio en Windows y hacer que esté disponible para las aplicaciones de WSL y Windows.</span><span class="sxs-lookup"><span data-stu-id="b32b8-522">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="b32b8-523">Ahora, eso es posible con los sockets de Unix.</span><span class="sxs-lookup"><span data-stu-id="b32b8-523">Now, that’s possible with Unix sockets.</span></span> <span data-ttu-id="b32b8-524">Lee más en nuestra publicación de blog en https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="b32b8-524">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-525">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-525">WSL</span></span>
* <span data-ttu-id="b32b8-526">Compatibilidad de mmap() con MAP_NORESERVE [GH 121, 2784]</span><span class="sxs-lookup"><span data-stu-id="b32b8-526">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="b32b8-527">Compatibilidad con CLONE_PTRACE y CLONE_UNTRACED [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="b32b8-527">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="b32b8-528">Controla la señal de terminación no SIGCHLD en el clon [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="b32b8-528">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="b32b8-529">Código auxiliar /proc/sys/fs/inotify/max_user_instances y /proc/sys/fs/inotify/max_user_watches [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="b32b8-529">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="b32b8-530">Error al cargar binarios de ELF que contienen encabezados de carga con desplazamientos distintos de cero [GH 1884]</span><span class="sxs-lookup"><span data-stu-id="b32b8-530">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="b32b8-531">Se eliminan los bytes de página finales al cargar imágenes.</span><span class="sxs-lookup"><span data-stu-id="b32b8-531">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="b32b8-532">Reduce los casos en los que execve finaliza el proceso de forma silenciosa</span><span class="sxs-lookup"><span data-stu-id="b32b8-532">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="b32b8-533">Console</span><span class="sxs-lookup"><span data-stu-id="b32b8-533">Console</span></span>
* <span data-ttu-id="b32b8-534">Sin correcciones.</span><span class="sxs-lookup"><span data-stu-id="b32b8-534">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-535">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-535">LTP Results:</span></span>
<span data-ttu-id="b32b8-536">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="b32b8-536">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="b32b8-537">Compilación 17083</span><span class="sxs-lookup"><span data-stu-id="b32b8-537">Build 17083</span></span>
<span data-ttu-id="b32b8-538">Para obtener información general de Windows sobre la compilación 17083, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-538">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-539">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-539">WSL</span></span>
* <span data-ttu-id="b32b8-540">Se ha corregido la comprobación de errores relacionada con epoll [GH 2798, 2801, 2857]</span><span class="sxs-lookup"><span data-stu-id="b32b8-540">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="b32b8-541">Se han corregido bloqueos al desactivar ASLR [GH 1185, 2870]</span><span class="sxs-lookup"><span data-stu-id="b32b8-541">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="b32b8-542">Asegúrate de que las operaciones de mmap aparezcan como atómicas [GH 2732]</span><span class="sxs-lookup"><span data-stu-id="b32b8-542">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="b32b8-543">Console</span><span class="sxs-lookup"><span data-stu-id="b32b8-543">Console</span></span>
* <span data-ttu-id="b32b8-544">Sin correcciones.</span><span class="sxs-lookup"><span data-stu-id="b32b8-544">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-545">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-545">LTP Results:</span></span>
<span data-ttu-id="b32b8-546">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="b32b8-546">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="b32b8-547">Compilación 17074</span><span class="sxs-lookup"><span data-stu-id="b32b8-547">Build 17074</span></span>
<span data-ttu-id="b32b8-548">Para obtener información general de Windows sobre la compilación 17074, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-548">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-549">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-549">WSL</span></span>
* <span data-ttu-id="b32b8-550">Se ha corregido el formato de almacenamiento de los metadatos de DrvFs [GH 2777]</span><span class="sxs-lookup"><span data-stu-id="b32b8-550">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="b32b8-551">**Importante:** Los metadatos de DrvFs creados antes de esta compilación no se mostrarán correctamente o no se mostrarán en absoluto.</span><span class="sxs-lookup"><span data-stu-id="b32b8-551">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="b32b8-552">Para corregir los archivos afectados, usa chmod y chown para volver a aplicar los metadatos.</span><span class="sxs-lookup"><span data-stu-id="b32b8-552">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="b32b8-553">Se ha corregido un problema con varias señales y llamadas del sistema reiniciables.</span><span class="sxs-lookup"><span data-stu-id="b32b8-553">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="b32b8-554">Console</span><span class="sxs-lookup"><span data-stu-id="b32b8-554">Console</span></span>
* <span data-ttu-id="b32b8-555">Sin correcciones.</span><span class="sxs-lookup"><span data-stu-id="b32b8-555">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-556">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-556">LTP Results:</span></span>
<span data-ttu-id="b32b8-557">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="b32b8-557">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="b32b8-558">Compilación 17063</span><span class="sxs-lookup"><span data-stu-id="b32b8-558">Build 17063</span></span>
<span data-ttu-id="b32b8-559">Para obtener información general de Windows sobre la compilación 17063, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-559">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="b32b8-560">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-560">WSL</span></span>
* <span data-ttu-id="b32b8-561">DrvFs admite metadatos de Linux adicionales.</span><span class="sxs-lookup"><span data-stu-id="b32b8-561">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="b32b8-562">Esto permite establecer el propietario y el modo de los archivos con chmod/chown, y también la creación de archivos especiales, como fifos, sockets de Unix y archivos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b32b8-562">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="b32b8-563">Esta opción está deshabilitada de forma predeterminada, ya que sigue siendo experimental.</span><span class="sxs-lookup"><span data-stu-id="b32b8-563">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="b32b8-564">**Nota:**  Se ha corregido un error en el formato de metadatos usado por DrvFs.</span><span class="sxs-lookup"><span data-stu-id="b32b8-564">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="b32b8-565">Si bien los metadatos funcionan en esta compilación para experimentación, las compilaciones futuras no leerán correctamente los metadatos creados por esta compilación.</span><span class="sxs-lookup"><span data-stu-id="b32b8-565">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="b32b8-566">Es posible que tengas que actualizar manualmente el propietario de los archivos modificados, y se tendrán que volver a crear los dispositivos con un identificador de dispositivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="b32b8-566">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="b32b8-567">Para habilitar, monta DrvFs con la opción de metadatos (para habilitarlo en un montaje existente, primero debes desmontarlo):</span><span class="sxs-lookup"><span data-stu-id="b32b8-567">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="b32b8-568">Los permisos de Linux se agregan como metadatos adicionales al archivo; no afectan a los permisos de Windows.</span><span class="sxs-lookup"><span data-stu-id="b32b8-568">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="b32b8-569">Recuerda que la edición de un archivo mediante un editor de Windows puede quitar los metadatos.</span><span class="sxs-lookup"><span data-stu-id="b32b8-569">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="b32b8-570">En este caso, el archivo volverá a sus permisos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="b32b8-570">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="b32b8-571">Se han agregado opciones de montaje a DrvFs para controlar archivos sin metadatos.</span><span class="sxs-lookup"><span data-stu-id="b32b8-571">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="b32b8-572">uid: el identificador de usuario que se usa para el propietario de todos los archivos.</span><span class="sxs-lookup"><span data-stu-id="b32b8-572">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="b32b8-573">gid: el identificador de grupo que se usa para el propietario de todos los archivos.</span><span class="sxs-lookup"><span data-stu-id="b32b8-573">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="b32b8-574">umask: máscara octal de permisos que se van a excluir para todos los archivos y directorios.</span><span class="sxs-lookup"><span data-stu-id="b32b8-574">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="b32b8-575">fmask: máscara octal de permisos que se van a excluir para todos los archivos normales.</span><span class="sxs-lookup"><span data-stu-id="b32b8-575">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="b32b8-576">dmask: máscara octal de permisos que se van a excluir para todos los directorios.</span><span class="sxs-lookup"><span data-stu-id="b32b8-576">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="b32b8-577">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="b32b8-577">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="b32b8-578">Combina con la opción de metadatos para especificar los permisos predeterminados para los archivos sin metadatos.</span><span class="sxs-lookup"><span data-stu-id="b32b8-578">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="b32b8-579">Se presentó una nueva variable de entorno, `WSLENV`, para configurar cómo fluyen las variables de entorno entre WSL y Win32.</span><span class="sxs-lookup"><span data-stu-id="b32b8-579">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="b32b8-580">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="b32b8-580">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="b32b8-581">`WSLENV` es una lista de variables de entorno delimitadas por signos de dos puntos que se puede incluir al iniciar procesos de WSL desde Win32, o procesos de Win32 desde WSL.</span><span class="sxs-lookup"><span data-stu-id="b32b8-581">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="b32b8-582">Cada variable puede tener como sufijo una barra diagonal seguida de marcas para especificar cómo se va a traducir.</span><span class="sxs-lookup"><span data-stu-id="b32b8-582">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="b32b8-583">p: El valor es una ruta de acceso que se debe traducir entre las rutas de acceso de WSL y las rutas de acceso de Win32.</span><span class="sxs-lookup"><span data-stu-id="b32b8-583">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="b32b8-584">l: El valor es una lista de rutas de acceso.</span><span class="sxs-lookup"><span data-stu-id="b32b8-584">l: The value is a list of paths.</span></span> <span data-ttu-id="b32b8-585">En WSL, se trata de una lista delimitada por signos de dos puntos.</span><span class="sxs-lookup"><span data-stu-id="b32b8-585">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="b32b8-586">En Win32, se trata de una lista delimitada por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="b32b8-586">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="b32b8-587">u: Solo se debe incluir el valor al invocar WSL desde Win32</span><span class="sxs-lookup"><span data-stu-id="b32b8-587">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="b32b8-588">w: Solo se debe incluir el valor al invocar Win32 desde WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-588">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="b32b8-589">Puedes establecer `WSLENV` en. bashrc o en el entorno de Windows personalizado para el usuario.</span><span class="sxs-lookup"><span data-stu-id="b32b8-589">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="b32b8-590">drvfs monta correctamente las marcas de tiempo de conservación desde tar, cp -p (GH 1939)</span><span class="sxs-lookup"><span data-stu-id="b32b8-590">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="b32b8-591">Los vínculos simbólicos de drvfs informan el tamaño correcto (GH 2641)</span><span class="sxs-lookup"><span data-stu-id="b32b8-591">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="b32b8-592">La lectura/escritura funciona para tamaños de E/S muy grandes (GH 2653)</span><span class="sxs-lookup"><span data-stu-id="b32b8-592">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="b32b8-593">waitpid funciona con identificadores de grupo de procesos (GH 2534)</span><span class="sxs-lookup"><span data-stu-id="b32b8-593">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="b32b8-594">Rendimiento de mmap significativamente mejorado para regiones de reserva grandes; mejora el rendimiento de ghc (GH 1671)</span><span class="sxs-lookup"><span data-stu-id="b32b8-594">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="b32b8-595">Compatibilidad de personality con READ_IMPLIES_EXEC; corrige maxima y clisp (GH 1185)</span><span class="sxs-lookup"><span data-stu-id="b32b8-595">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="b32b8-596">mprotect admite PROT_GROWSDOWN; corrige clisp (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="b32b8-596">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="b32b8-597">Correcciones de errores de página en modo de sobreconfirmación; corrige sbcl (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="b32b8-597">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="b32b8-598">clone admite más combinaciones de marcas</span><span class="sxs-lookup"><span data-stu-id="b32b8-598">clone supports more flags combinations</span></span>
* <span data-ttu-id="b32b8-599">Compatibilidad con select/epoll de archivos de epoll (antes de una no-op).</span><span class="sxs-lookup"><span data-stu-id="b32b8-599">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="b32b8-600">Notifica a ptrace de llamadas del sistema sin implementar.</span><span class="sxs-lookup"><span data-stu-id="b32b8-600">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="b32b8-601">Omite las interfaces que no están listas al generar los servidores de nombres resolv.conf [GH 2694]</span><span class="sxs-lookup"><span data-stu-id="b32b8-601">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="b32b8-602">Enumera las interfaces de red sin dirección física.</span><span class="sxs-lookup"><span data-stu-id="b32b8-602">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="b32b8-603">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="b32b8-603">[GH 2685]</span></span>
* <span data-ttu-id="b32b8-604">Mejoras y correcciones de errores adicionales.</span><span class="sxs-lookup"><span data-stu-id="b32b8-604">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="b32b8-605">Herramientas de Linux disponibles para desarrolladores en Windows</span><span class="sxs-lookup"><span data-stu-id="b32b8-605">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="b32b8-606">La cadena de herramientas de la línea de comandos de Windows incluye bsdtar (tar) y curl.</span><span class="sxs-lookup"><span data-stu-id="b32b8-606">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="b32b8-607">Lee [este blog](https://aka.ms/tarcurlwindows) para más información acerca de cómo agregar estas dos nuevas herramientas y ver cómo dan forma a la experiencia de los desarrolladores en Windows.</span><span class="sxs-lookup"><span data-stu-id="b32b8-607">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they’re shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="b32b8-608">`AF_UNIX` está disponible en el SDK de Windows Insider (17061+).</span><span class="sxs-lookup"><span data-stu-id="b32b8-608">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="b32b8-609">Lee [este blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) para más información sobre `AF_UNIX` y cómo pueden usarlo los desarrolladores de Windows.</span><span class="sxs-lookup"><span data-stu-id="b32b8-609">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="b32b8-610">Console</span><span class="sxs-lookup"><span data-stu-id="b32b8-610">Console</span></span>
* <span data-ttu-id="b32b8-611">Sin correcciones.</span><span class="sxs-lookup"><span data-stu-id="b32b8-611">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-612">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-612">LTP Results:</span></span>
<span data-ttu-id="b32b8-613">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="b32b8-613">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="b32b8-614">Compilación 17046</span><span class="sxs-lookup"><span data-stu-id="b32b8-614">Build 17046</span></span>

<span data-ttu-id="b32b8-615">Para obtener información general de Windows sobre la compilación 17046, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span><span class="sxs-lookup"><span data-stu-id="b32b8-615">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="b32b8-616">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-616">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b32b8-617">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-617">WSL</span></span>
- <span data-ttu-id="b32b8-618">Permite que los procesos se ejecuten sin un terminal activo.</span><span class="sxs-lookup"><span data-stu-id="b32b8-618">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="b32b8-619">[GH 709, 1007, 1511, 2252, 2391, etc.]</span><span class="sxs-lookup"><span data-stu-id="b32b8-619">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="b32b8-620">Mejor compatibilidad con CLONE_VFORK y CLONE_VM.</span><span class="sxs-lookup"><span data-stu-id="b32b8-620">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="b32b8-621">[GH 1878, 2615]</span><span class="sxs-lookup"><span data-stu-id="b32b8-621">[GH 1878, 2615]</span></span>
- <span data-ttu-id="b32b8-622">Omite los controladores de filtro TDI para las operaciones de red de WSL.</span><span class="sxs-lookup"><span data-stu-id="b32b8-622">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="b32b8-623">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="b32b8-623">[GH 1554]</span></span>
- <span data-ttu-id="b32b8-624">DrvFs crea vínculos simbólicos de NT cuando se cumplen determinadas condiciones.</span><span class="sxs-lookup"><span data-stu-id="b32b8-624">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="b32b8-625">[GH 353, 1475, 2602]</span><span class="sxs-lookup"><span data-stu-id="b32b8-625">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="b32b8-626">El destino del vínculo debe ser relativo, no debe cruzar ningún punto de montaje ni vínculo simbólico, y debe existir.</span><span class="sxs-lookup"><span data-stu-id="b32b8-626">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="b32b8-627">El usuario debe tener SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (esto normalmente requiere que inicies wsl.exe con privilegios elevados), a menos que esté activado el modo de desarrollador.</span><span class="sxs-lookup"><span data-stu-id="b32b8-627">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="b32b8-628">En todas las demás situaciones, DrvFs todavía crea vínculos simbólicos de WSL.</span><span class="sxs-lookup"><span data-stu-id="b32b8-628">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="b32b8-629">Permite ejecutar instancias de WSL con privilegios elevados y no elevados simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="b32b8-629">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="b32b8-630">Compatibilidad con /proc/sys/kernel/yama/ptrace_scope</span><span class="sxs-lookup"><span data-stu-id="b32b8-630">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="b32b8-631">Agrega wslpath para realizar conversiones de rutas de acceso de WSL<->Windows.</span><span class="sxs-lookup"><span data-stu-id="b32b8-631">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="b32b8-632">[GH 522, 1243, 1834, 2327, etc.]</span><span class="sxs-lookup"><span data-stu-id="b32b8-632">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a><span data-ttu-id="b32b8-633">Console</span><span class="sxs-lookup"><span data-stu-id="b32b8-633">Console</span></span>
- <span data-ttu-id="b32b8-634">Sin correcciones.</span><span class="sxs-lookup"><span data-stu-id="b32b8-634">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-635">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-635">LTP Results:</span></span>
<span data-ttu-id="b32b8-636">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="b32b8-636">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="b32b8-637">Compilación 17040</span><span class="sxs-lookup"><span data-stu-id="b32b8-637">Build 17040</span></span>

<span data-ttu-id="b32b8-638">Para obtener información general de Windows sobre la compilación 17040, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span><span class="sxs-lookup"><span data-stu-id="b32b8-638">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-639">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-639">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b32b8-640">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-640">WSL</span></span>
- <span data-ttu-id="b32b8-641">No hay correcciones desde 17035.</span><span class="sxs-lookup"><span data-stu-id="b32b8-641">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="b32b8-642">Console</span><span class="sxs-lookup"><span data-stu-id="b32b8-642">Console</span></span>
- <span data-ttu-id="b32b8-643">No hay correcciones desde 17035.</span><span class="sxs-lookup"><span data-stu-id="b32b8-643">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-644">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-644">LTP Results:</span></span>
<span data-ttu-id="b32b8-645">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="b32b8-645">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="b32b8-646">Compilación 17035</span><span class="sxs-lookup"><span data-stu-id="b32b8-646">Build 17035</span></span>

<span data-ttu-id="b32b8-647">Para obtener información general de Windows sobre la compilación 17035, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span><span class="sxs-lookup"><span data-stu-id="b32b8-647">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-648">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-648">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b32b8-649">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-649">WSL</span></span>
- <span data-ttu-id="b32b8-650">En ocasiones, el acceso a los archivos de DrvFs puede producir errores con EINVAL.</span><span class="sxs-lookup"><span data-stu-id="b32b8-650">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="b32b8-651">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="b32b8-651">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="b32b8-652">Console</span><span class="sxs-lookup"><span data-stu-id="b32b8-652">Console</span></span>
- <span data-ttu-id="b32b8-653">Algo de pérdida de color al insertar o eliminar líneas en modo VT.</span><span class="sxs-lookup"><span data-stu-id="b32b8-653">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-654">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-654">LTP Results:</span></span>
<span data-ttu-id="b32b8-655">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="b32b8-655">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="b32b8-656">Compilación 17025</span><span class="sxs-lookup"><span data-stu-id="b32b8-656">Build 17025</span></span>

<span data-ttu-id="b32b8-657">Para obtener información general de Windows sobre la compilación 17025, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span><span class="sxs-lookup"><span data-stu-id="b32b8-657">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-658">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-658">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b32b8-659">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-659">WSL</span></span>
- <span data-ttu-id="b32b8-660">Inicia procesos iniciales en un nuevo grupo de procesos en primer plano [GH 1653, 2510].</span><span class="sxs-lookup"><span data-stu-id="b32b8-660">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="b32b8-661">Correcciones de entrega de SIGHUP [GH 2496].</span><span class="sxs-lookup"><span data-stu-id="b32b8-661">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="b32b8-662">Genera un nombre de puente virtual predeterminado si no se proporciona ninguno [GH 2497].</span><span class="sxs-lookup"><span data-stu-id="b32b8-662">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="b32b8-663">Implementa /proc/sys/kernel/random/boot_id [GH 2518].</span><span class="sxs-lookup"><span data-stu-id="b32b8-663">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="b32b8-664">Más correcciones de la canalización stdout/stderr de interoperabilidad.</span><span class="sxs-lookup"><span data-stu-id="b32b8-664">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="b32b8-665">Llamada del sistema syncfs de código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="b32b8-665">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="b32b8-666">Console</span><span class="sxs-lookup"><span data-stu-id="b32b8-666">Console</span></span>
- <span data-ttu-id="b32b8-667">Corrección de la traducción de VT de entrada para consolas de terceros [GH 111]</span><span class="sxs-lookup"><span data-stu-id="b32b8-667">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-668">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-668">LTP Results:</span></span>
<span data-ttu-id="b32b8-669">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="b32b8-669">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="b32b8-670">Compilación 17017</span><span class="sxs-lookup"><span data-stu-id="b32b8-670">Build 17017</span></span>

<span data-ttu-id="b32b8-671">Para obtener información general de Windows sobre la compilación 17017, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span><span class="sxs-lookup"><span data-stu-id="b32b8-671">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-672">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-672">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b32b8-673">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-673">WSL</span></span>
- <span data-ttu-id="b32b8-674">Omite los encabezados de programa ELF vacíos [GH 330].</span><span class="sxs-lookup"><span data-stu-id="b32b8-674">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="b32b8-675">Permite que LxssManager cree instancias de WSL para usuarios no interactivos (compatibilidad con ssh y tareas programadas) [GH 777, 1602].</span><span class="sxs-lookup"><span data-stu-id="b32b8-675">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="b32b8-676">Compatibilidad con escenarios de WSL->Win32->WSL ("inicio") [GH 1228].</span><span class="sxs-lookup"><span data-stu-id="b32b8-676">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="b32b8-677">Compatibilidad limitada para la terminación de las aplicaciones de consola que se invocan a través de la interoperabilidad [GH 1614].</span><span class="sxs-lookup"><span data-stu-id="b32b8-677">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="b32b8-678">Compatibilidad con las opciones de montaje para devpts [GH 1948].</span><span class="sxs-lookup"><span data-stu-id="b32b8-678">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="b32b8-679">Inicio de bloqueo secundario de Ptrace [GH 2333].</span><span class="sxs-lookup"><span data-stu-id="b32b8-679">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="b32b8-680">Faltan algunos eventos de EPOLLET [GH 2462].</span><span class="sxs-lookup"><span data-stu-id="b32b8-680">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="b32b8-681">Devuelve más datos para PTRACE_GETSIGINFO.</span><span class="sxs-lookup"><span data-stu-id="b32b8-681">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="b32b8-682">Getdents con lseek proporciona resultados incorrectos.</span><span class="sxs-lookup"><span data-stu-id="b32b8-682">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="b32b8-683">Corrección de algunos bloqueos de la aplicación de interoperabilidad de Win32, en espera de la entrada en una canalización que no tiene más datos.</span><span class="sxs-lookup"><span data-stu-id="b32b8-683">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="b32b8-684">Compatibilidad de O_ASYNC con archivos tty/pty.</span><span class="sxs-lookup"><span data-stu-id="b32b8-684">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="b32b8-685">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-685">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="b32b8-686">Console</span><span class="sxs-lookup"><span data-stu-id="b32b8-686">Console</span></span>
- <span data-ttu-id="b32b8-687">No hay cambios relacionados con la consola en esta versión.</span><span class="sxs-lookup"><span data-stu-id="b32b8-687">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-688">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-688">LTP Results:</span></span>
<span data-ttu-id="b32b8-689">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="b32b8-689">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="b32b8-690">Actualización Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="b32b8-690">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="b32b8-691">Compilación 16288</span><span class="sxs-lookup"><span data-stu-id="b32b8-691">Build 16288</span></span>

<span data-ttu-id="b32b8-692">Para obtener información general de Windows sobre la compilación 16288, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-692">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-693">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-693">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b32b8-694">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-694">WSL</span></span>
- <span data-ttu-id="b32b8-695">Inicializa y notifica correctamente uid, gid y mode para los descriptores de archivo de socket [GH 2490]</span><span class="sxs-lookup"><span data-stu-id="b32b8-695">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="b32b8-696">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-696">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="b32b8-697">Console</span><span class="sxs-lookup"><span data-stu-id="b32b8-697">Console</span></span>
- <span data-ttu-id="b32b8-698">No hay cambios relacionados con la consola en esta versión.</span><span class="sxs-lookup"><span data-stu-id="b32b8-698">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-699">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-699">LTP Results:</span></span>
<span data-ttu-id="b32b8-700">Sin cambios desde 16273</span><span class="sxs-lookup"><span data-stu-id="b32b8-700">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="b32b8-701">Compilación 16278</span><span class="sxs-lookup"><span data-stu-id="b32b8-701">Build 16278</span></span>

<span data-ttu-id="b32b8-702">Para obtener información general de Windows sobre la compilación 162738, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-702">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-703">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-703">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b32b8-704">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-704">WSL</span></span>
- <span data-ttu-id="b32b8-705">Anula explícitamente la asignación de las vistas asignadas de secciones basadas en archivos al anular el estado de LX MM [GH 2415]</span><span class="sxs-lookup"><span data-stu-id="b32b8-705">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="b32b8-706">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-706">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="b32b8-707">Console</span><span class="sxs-lookup"><span data-stu-id="b32b8-707">Console</span></span>
- <span data-ttu-id="b32b8-708">No hay cambios relacionados con la consola en esta versión.</span><span class="sxs-lookup"><span data-stu-id="b32b8-708">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-709">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-709">LTP Results:</span></span>
<span data-ttu-id="b32b8-710">Sin cambios desde 16273</span><span class="sxs-lookup"><span data-stu-id="b32b8-710">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="b32b8-711">Compilación 16275</span><span class="sxs-lookup"><span data-stu-id="b32b8-711">Build 16275</span></span>

<span data-ttu-id="b32b8-712">Para obtener información general de Windows sobre la compilación 162735, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-712">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-713">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-713">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b32b8-714">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-714">WSL</span></span>
- <span data-ttu-id="b32b8-715">No hay cambios relacionados con WSL en esta versión.</span><span class="sxs-lookup"><span data-stu-id="b32b8-715">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="b32b8-716">Console</span><span class="sxs-lookup"><span data-stu-id="b32b8-716">Console</span></span>
- <span data-ttu-id="b32b8-717">No hay cambios relacionados con la consola en esta versión.</span><span class="sxs-lookup"><span data-stu-id="b32b8-717">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-718">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-718">LTP Results:</span></span>
<span data-ttu-id="b32b8-719">Sin cambios desde 16273</span><span class="sxs-lookup"><span data-stu-id="b32b8-719">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="b32b8-720">Compilación 16273</span><span class="sxs-lookup"><span data-stu-id="b32b8-720">Build 16273</span></span>

<span data-ttu-id="b32b8-721">Para obtener información general de Windows sobre la compilación 16273, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-721">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-722">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-722">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b32b8-723">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-723">WSL</span></span>
- <span data-ttu-id="b32b8-724">Se ha corregido un problema por el que DrvFs a veces indicaba un tipo de archivo incorrecto para los directorios [GH 2392]</span><span class="sxs-lookup"><span data-stu-id="b32b8-724">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="b32b8-725">Permite la creación de sockets NETLINK_KOBJECT_UEVENT para desbloquear programas que usan UEVENT [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span><span class="sxs-lookup"><span data-stu-id="b32b8-725">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="b32b8-726">Agrega compatibilidad para conexión sin bloqueo [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span><span class="sxs-lookup"><span data-stu-id="b32b8-726">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="b32b8-727">Implementa la marca de llamada del sistema de clon CLONE_FS [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="b32b8-727">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="b32b8-728">Corrección de problemas relativos a la falta de control de tabulaciones o comillas correctamente en la interoperabilidad de NT [GH 1625, 2164]</span><span class="sxs-lookup"><span data-stu-id="b32b8-728">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="b32b8-729">Resuelve el error de acceso denegado al intentar volver a iniciar instancias de WSL [GH 651, 2095]</span><span class="sxs-lookup"><span data-stu-id="b32b8-729">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="b32b8-730">Implementa las operaciones de Futex FUTEX_REQUEUE y FUTEX_CMP_REQUEUE [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="b32b8-730">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="b32b8-731">Corrección de permisos para varios archivos de SysFs [GH 2214]</span><span class="sxs-lookup"><span data-stu-id="b32b8-731">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="b32b8-732">Corrección del bloqueo de pila de Haskell durante la instalación [GH 2290]</span><span class="sxs-lookup"><span data-stu-id="b32b8-732">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="b32b8-733">Implementa las marcas binfmt_misc "C", "O" y "P" [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="b32b8-733">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="b32b8-734">Agrega /proc/sys/kernel /shmmax /shmmni y /threads-max [GH 1753]</span><span class="sxs-lookup"><span data-stu-id="b32b8-734">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="b32b8-735">Agrega compatibilidad parcial para la llamada del sistema ioprio_set [GH 498]</span><span class="sxs-lookup"><span data-stu-id="b32b8-735">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="b32b8-736">Código auxiliar SO_REUSEPORT y agrega compatibilidad para SO_PASSCRED para sockets de netlink [GH 69]</span><span class="sxs-lookup"><span data-stu-id="b32b8-736">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="b32b8-737">Devuelve distintos códigos de error de RegisterDistribuiton si se está instalando o desinstalando actualmente una distribución.</span><span class="sxs-lookup"><span data-stu-id="b32b8-737">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="b32b8-738">Permite la anulación del registro de distribuciones de WSL parcialmente instaladas a través de wslconfig.exe</span><span class="sxs-lookup"><span data-stu-id="b32b8-738">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="b32b8-739">Corrección de bloqueo de prueba de socket de Python desde UDP::msg_peek</span><span class="sxs-lookup"><span data-stu-id="b32b8-739">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="b32b8-740">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-740">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="b32b8-741">Console</span><span class="sxs-lookup"><span data-stu-id="b32b8-741">Console</span></span>
- <span data-ttu-id="b32b8-742">No hay cambios relacionados con la consola en esta versión.</span><span class="sxs-lookup"><span data-stu-id="b32b8-742">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-743">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-743">LTP Results:</span></span>
<span data-ttu-id="b32b8-744">Total de pruebas: 1904</span><span class="sxs-lookup"><span data-stu-id="b32b8-744">Total Tests: 1904</span></span><br/>
<span data-ttu-id="b32b8-745">Total de pruebas omitidas: 209</span><span class="sxs-lookup"><span data-stu-id="b32b8-745">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="b32b8-746">Total de errores: 229</span><span class="sxs-lookup"><span data-stu-id="b32b8-746">Total Failures: 229</span></span><br/>
[<span data-ttu-id="b32b8-747">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="b32b8-747">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="b32b8-748">Compilación 16257</span><span class="sxs-lookup"><span data-stu-id="b32b8-748">Build 16257</span></span>

<span data-ttu-id="b32b8-749">Para obtener información general de Windows sobre la compilación 16257, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-749">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-750">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-750">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b32b8-751">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-751">WSL</span></span>
- <span data-ttu-id="b32b8-752">Implementa la llamada del sistema prlimit64</span><span class="sxs-lookup"><span data-stu-id="b32b8-752">Implement prlimit64 system call</span></span>
- <span data-ttu-id="b32b8-753">Agrega compatibilidad con ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="b32b8-753">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="b32b8-754">Código auxiliar de MSG_MORE para sockets TCP [GH 2351]</span><span class="sxs-lookup"><span data-stu-id="b32b8-754">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="b32b8-755">Corrección del comportamiento del vector auxiliar de AT_EXECFN no válido [GH 2133]</span><span class="sxs-lookup"><span data-stu-id="b32b8-755">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="b32b8-756">Corrección del comportamiento de copiar y pegar para consola/tty, y agrega un mejor control de búfer completo [GH 2204, 2131]</span><span class="sxs-lookup"><span data-stu-id="b32b8-756">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="b32b8-757">Establece AT_SECURE en vector auxiliar para los programas set-user-ID y set-group-ID [GH 2031]</span><span class="sxs-lookup"><span data-stu-id="b32b8-757">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="b32b8-758">El punto de conexión maestro de psuedoterminal no controla TIOCPGRP [GH 1063]</span><span class="sxs-lookup"><span data-stu-id="b32b8-758">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="b32b8-759">La corrección de lseek hace rebobinar directorios en LxFs [GH 2310]</span><span class="sxs-lookup"><span data-stu-id="b32b8-759">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="b32b8-760">/dev/ptmx se bloquea después de un uso pesado [GH 1882]</span><span class="sxs-lookup"><span data-stu-id="b32b8-760">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="b32b8-761">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-761">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="b32b8-762">Console</span><span class="sxs-lookup"><span data-stu-id="b32b8-762">Console</span></span>
- <span data-ttu-id="b32b8-763">Corrección para líneas horizontales o guiones bajos en todas partes [GH 2168]</span><span class="sxs-lookup"><span data-stu-id="b32b8-763">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="b32b8-764">Corrección para el orden de procesamiento cambiado hace que NPM sea más difícil de cerrar [GH 2170]</span><span class="sxs-lookup"><span data-stu-id="b32b8-764">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="b32b8-765">Se ha agregado la nueva combinación de colores: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="b32b8-765">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-766">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-766">LTP Results:</span></span>
<span data-ttu-id="b32b8-767">Sin cambios desde 16251</span><span class="sxs-lookup"><span data-stu-id="b32b8-767">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="b32b8-768">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="b32b8-768">Syscall Support</span></span>
<span data-ttu-id="b32b8-769">A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="b32b8-769">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b32b8-770">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="b32b8-770">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="b32b8-771">Problemas conocidos</span><span class="sxs-lookup"><span data-stu-id="b32b8-771">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[<span data-ttu-id="b32b8-772">Problema de GitHub 2392: WSL no reconoce carpetas de Windows…</span><span class="sxs-lookup"><span data-stu-id="b32b8-772">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="b32b8-773">En la compilación 16257, WSL tiene problemas al enumerar archivos o carpetas de Windows a través de `/mnt/c/...`.</span><span class="sxs-lookup"><span data-stu-id="b32b8-773">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="b32b8-774">Este problema se ha corregido y debe publicarse en la compilación de Insider durante la semana que comienza el 14/8/2017.</span><span class="sxs-lookup"><span data-stu-id="b32b8-774">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="b32b8-775">Compilación 16251</span><span class="sxs-lookup"><span data-stu-id="b32b8-775">Build 16251</span></span>

<span data-ttu-id="b32b8-776">Para obtener información general de Windows sobre la compilación 16251, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-776">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-777">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-777">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b32b8-778">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-778">WSL</span></span>
- <span data-ttu-id="b32b8-779">Quita la etiqueta beta del componente opcional de WSL, consulta la [publicación de blog](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) para más información.</span><span class="sxs-lookup"><span data-stu-id="b32b8-779">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="b32b8-780">Inicializa correctamente el uid y gid del conjunto guardado para los archivos binarios set-user-ID y set-group-ID en ejecución [GH 962, 1415, 2072]</span><span class="sxs-lookup"><span data-stu-id="b32b8-780">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="b32b8-781">Se ha agregado compatibilidad con ptrace PTRACE_O_TRACEEXIT [GH 555]</span><span class="sxs-lookup"><span data-stu-id="b32b8-781">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="b32b8-782">Se ha agregado compatibilidad con ptrace PTRACE_GETFPREGS y PTRACE_GETREGSET con NT_FPREGSET [GH 555]</span><span class="sxs-lookup"><span data-stu-id="b32b8-782">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="b32b8-783">Se ha corregido ptrace para que se detenga en las señales omitidas</span><span class="sxs-lookup"><span data-stu-id="b32b8-783">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="b32b8-784">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-784">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="b32b8-785">Console</span><span class="sxs-lookup"><span data-stu-id="b32b8-785">Console</span></span>
- <span data-ttu-id="b32b8-786">No hay cambios relacionados con la consola en esta versión.</span><span class="sxs-lookup"><span data-stu-id="b32b8-786">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-787">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-787">LTP Results:</span></span>
<span data-ttu-id="b32b8-788">Número de pruebas superadas: 768</span><span class="sxs-lookup"><span data-stu-id="b32b8-788">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="b32b8-789">Número de pruebas no superadas: 244</span><span class="sxs-lookup"><span data-stu-id="b32b8-789">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="b32b8-790">Número de pruebas omitidas: 96</span><span class="sxs-lookup"><span data-stu-id="b32b8-790">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="b32b8-791">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="b32b8-791">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="b32b8-792">Compilación 16241</span><span class="sxs-lookup"><span data-stu-id="b32b8-792">Build 16241</span></span>

<span data-ttu-id="b32b8-793">Para obtener información general de Windows sobre la compilación 16241, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-793">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-794">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-794">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="b32b8-795">WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-795">WSL</span></span>
- <span data-ttu-id="b32b8-796">No hay cambios relacionados con WSL en esta versión.</span><span class="sxs-lookup"><span data-stu-id="b32b8-796">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="b32b8-797">Console</span><span class="sxs-lookup"><span data-stu-id="b32b8-797">Console</span></span>
- <span data-ttu-id="b32b8-798">Corrección para la generación de un carácter equivocado para DEC de líneas de paso, que se notificó originalmente aquí</span><span class="sxs-lookup"><span data-stu-id="b32b8-798">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="b32b8-799">Corrección para cuando no se muestre texto de salida en la página de códigos 65001 (utf8)</span><span class="sxs-lookup"><span data-stu-id="b32b8-799">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="b32b8-800">No transfieras los cambios hechos en los valores RGB de un color a otras partes de la paleta en el cambio de selección.</span><span class="sxs-lookup"><span data-stu-id="b32b8-800">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="b32b8-801">Esto hará que la hoja de propiedades de la consola sea mucho más fácil de usar.</span><span class="sxs-lookup"><span data-stu-id="b32b8-801">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="b32b8-802">Ctrl+S no parece funcionar correctamente</span><span class="sxs-lookup"><span data-stu-id="b32b8-802">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="b32b8-803">Un-Bold/-Dim totalmente ausentes de los códigos de escape de ANSI [GH 2174]</span><span class="sxs-lookup"><span data-stu-id="b32b8-803">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="b32b8-804">La consola no admite correctamente los temas de color VIM [GH 1706]</span><span class="sxs-lookup"><span data-stu-id="b32b8-804">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="b32b8-805">No se pueden pegar caracteres determinados [GH 2149]</span><span class="sxs-lookup"><span data-stu-id="b32b8-805">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="b32b8-806">El cambio de tamaño de reflujo interactúa de forma extraña con el cambio de tamaño de una ventana de Bash cuando el contenido está en la línea de comandos/edición [GH ConEmu 1123]</span><span class="sxs-lookup"><span data-stu-id="b32b8-806">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="b32b8-807">Ctrl-L deja la pantalla desfasada [GH 1978]</span><span class="sxs-lookup"><span data-stu-id="b32b8-807">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="b32b8-808">Error de representación de consola al mostrar VT en HDPI [GH 1907]</span><span class="sxs-lookup"><span data-stu-id="b32b8-808">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="b32b8-809">Los caracteres Japansese parecen extraños con el carácter Unicode U+30FB [GH 2146]</span><span class="sxs-lookup"><span data-stu-id="b32b8-809">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="b32b8-810">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-810">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="b32b8-811">Compilación 16237</span><span class="sxs-lookup"><span data-stu-id="b32b8-811">Build 16237</span></span>

<span data-ttu-id="b32b8-812">Para obtener información general de Windows sobre la compilación 16237, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-812">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-813">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-813">Fixed</span></span>
- <span data-ttu-id="b32b8-814">Usa atributos predeterminados para archivos sin EA en lxfs (root, root, 0000)</span><span class="sxs-lookup"><span data-stu-id="b32b8-814">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="b32b8-815">Se ha agregado compatibilidad para distribuciones que usan atributos extendidos</span><span class="sxs-lookup"><span data-stu-id="b32b8-815">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="b32b8-816">Corrección del relleno de las entradas devueltas por getdents y getdents64</span><span class="sxs-lookup"><span data-stu-id="b32b8-816">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="b32b8-817">Corrección de la comprobación de permisos para la llamada del sistema shmctl SHM_STAT [GH 2068]</span><span class="sxs-lookup"><span data-stu-id="b32b8-817">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="b32b8-818">Se ha corregido el estado inicial incorrecto de epoll para ttys [GH 2231]</span><span class="sxs-lookup"><span data-stu-id="b32b8-818">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="b32b8-819">Corrección de readdir de DrvFs que no devuelve todas las entradas [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="b32b8-819">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="b32b8-820">Corrección de readdir de LxFs cuando los archivos están desvinculados [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="b32b8-820">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="b32b8-821">Permite que los archivos drvfs no vinculados se vuelvan a abrir a través de procfs</span><span class="sxs-lookup"><span data-stu-id="b32b8-821">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="b32b8-822">Se ha agregado la invalidación de la clave del Registro global para deshabilitar las características de WSL (interoperabilidad/montaje de unidades)</span><span class="sxs-lookup"><span data-stu-id="b32b8-822">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="b32b8-823">Corrección del recuento incorrecto de bloques en "stat" para DrvFs (y LxFs) [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="b32b8-823">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="b32b8-824">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-824">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="b32b8-825">Compilación 16232</span><span class="sxs-lookup"><span data-stu-id="b32b8-825">Build 16232</span></span>

<span data-ttu-id="b32b8-826">Para obtener información general de Windows sobre la compilación 16232, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-826">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-827">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-827">Fixed</span></span>
- <span data-ttu-id="b32b8-828">No hay cambios relacionados con WSL en esta versión.</span><span class="sxs-lookup"><span data-stu-id="b32b8-828">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="b32b8-829">Compilación 16226</span><span class="sxs-lookup"><span data-stu-id="b32b8-829">Build 16226</span></span>

<span data-ttu-id="b32b8-830">Para obtener información general de Windows sobre la compilación 16226, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-830">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-831">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-831">Fixed</span></span>
- <span data-ttu-id="b32b8-832">Compatibilidad con llamadas del sistema relacionadas con xattr (getxattr, setxattr, listxattr, removexattr).</span><span class="sxs-lookup"><span data-stu-id="b32b8-832">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="b32b8-833">Compatibilidad con security.capablity xattr.</span><span class="sxs-lookup"><span data-stu-id="b32b8-833">security.capablity xattr support.</span></span>
- <span data-ttu-id="b32b8-834">Compatibilidad mejorada con determinados sistemas de archivos y filtros, incluidos los servidores SMB que no son de MS.</span><span class="sxs-lookup"><span data-stu-id="b32b8-834">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="b32b8-835">[GH 1952]</span><span class="sxs-lookup"><span data-stu-id="b32b8-835">[GH #1952]</span></span>
- <span data-ttu-id="b32b8-836">Compatibilidad mejorada para los marcadores de posición de OneDrive, los marcadores de posición de GVFS y los archivos comprimidos del sistema operativo compacto.</span><span class="sxs-lookup"><span data-stu-id="b32b8-836">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="b32b8-837">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-837">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="b32b8-838">Compilación 16215</span><span class="sxs-lookup"><span data-stu-id="b32b8-838">Build 16215</span></span>

<span data-ttu-id="b32b8-839">Para obtener información general de Windows sobre la compilación 16215, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-839">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-840">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-840">Fixed</span></span>
- <span data-ttu-id="b32b8-841">WSL ya no requiere el modo de desarrollador.</span><span class="sxs-lookup"><span data-stu-id="b32b8-841">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="b32b8-842">Compatibilidad con uniones de directorios en drvfs.</span><span class="sxs-lookup"><span data-stu-id="b32b8-842">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="b32b8-843">Controla la desinstalación de paquetes appx de distribución de WSL.</span><span class="sxs-lookup"><span data-stu-id="b32b8-843">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="b32b8-844">Actualiza procfs para mostrar las asignaciones privadas y compartidas.</span><span class="sxs-lookup"><span data-stu-id="b32b8-844">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="b32b8-845">Agrega la capacidad de wslconfig.exe de limpiar las distribuciones que están parcialmente instaladas o desinstaladas.</span><span class="sxs-lookup"><span data-stu-id="b32b8-845">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="b32b8-846">Se ha agregado compatibilidad para IP_MTU_DISCOVER para sockets TCP.</span><span class="sxs-lookup"><span data-stu-id="b32b8-846">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="b32b8-847">[GH 1639, 2115, 2205]</span><span class="sxs-lookup"><span data-stu-id="b32b8-847">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="b32b8-848">Inferencia de la familia de protocolos para rutas a AF_INADDR.</span><span class="sxs-lookup"><span data-stu-id="b32b8-848">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="b32b8-849">Mejoras en los dispositivos serie [GH 1929].</span><span class="sxs-lookup"><span data-stu-id="b32b8-849">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="b32b8-850">Compilación 16199</span><span class="sxs-lookup"><span data-stu-id="b32b8-850">Build 16199</span></span>

<span data-ttu-id="b32b8-851">Para obtener información general de Windows sobre la compilación 16199, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-851">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-852">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-852">Fixed</span></span>
- <span data-ttu-id="b32b8-853">No hay cambios relacionados con WSL en estas versiones.</span><span class="sxs-lookup"><span data-stu-id="b32b8-853">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="b32b8-854">Compilación 16193</span><span class="sxs-lookup"><span data-stu-id="b32b8-854">Build 16193</span></span>

<span data-ttu-id="b32b8-855">Para obtener información general de Windows sobre la compilación 16193, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-855">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-856">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-856">Fixed</span></span>
- <span data-ttu-id="b32b8-857">Condición de carrera entre el envío de SIGCONT y un grupo de subprocesos de terminación [GH 1973]</span><span class="sxs-lookup"><span data-stu-id="b32b8-857">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="b32b8-858">Cambia dispositivos tty y pty para notificar FILE_DEVICE_NAMED_PIPE en lugar de FILE_DEVICE_CONSOLE [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="b32b8-858">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="b32b8-859">Corrección de SSH para IP_OPTIONS</span><span class="sxs-lookup"><span data-stu-id="b32b8-859">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="b32b8-860">Se ha cambiado el montaje de DrvFs al demonio de inicialización [GH 1862, 1968, 1767, 1933]</span><span class="sxs-lookup"><span data-stu-id="b32b8-860">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="b32b8-861">Se ha agregado compatibilidad en DrvFs para los siguientes vínculos simbólicos de NT.</span><span class="sxs-lookup"><span data-stu-id="b32b8-861">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="b32b8-862">Compilación 16184</span><span class="sxs-lookup"><span data-stu-id="b32b8-862">Build 16184</span></span>

<span data-ttu-id="b32b8-863">Para obtener información general de Windows sobre la compilación 16184, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-863">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-864">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-864">Fixed</span></span>
- <span data-ttu-id="b32b8-865">Se ha quitado la tarea de mantenimiento de paquetes APT (lxrun.exe /update)</span><span class="sxs-lookup"><span data-stu-id="b32b8-865">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="b32b8-866">Se ha corregido la salida que no se muestra en los procesos de Windows en node.js [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="b32b8-866">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="b32b8-867">Relaja los requisitos de alineación en lxcore [GH 1794]</span><span class="sxs-lookup"><span data-stu-id="b32b8-867">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="b32b8-868">Se ha corregido el control de la marca AT_EMPTY_PATH en un número de llamadas del sistema.</span><span class="sxs-lookup"><span data-stu-id="b32b8-868">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="b32b8-869">Se ha corregido el problema por el que la eliminación de archivos DrvFs con identificadores abiertos hace que el archivo muestre un comportamiento indefinido [GH 544, 966, 1357, 1535, 1615]</span><span class="sxs-lookup"><span data-stu-id="b32b8-869">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="b32b8-870">/etc/hosts heredará ahora entradas del archivo de hosts de Windows (%windir%\system32\drivers\etc\hosts) [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="b32b8-870">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="b32b8-871">Compilación 16179</span><span class="sxs-lookup"><span data-stu-id="b32b8-871">Build 16179</span></span>

<span data-ttu-id="b32b8-872">Para obtener información general de Windows sobre la compilación 16179, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-872">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-873">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-873">Fixed</span></span>
- <span data-ttu-id="b32b8-874">Sin cambios en WSL esta semana.</span><span class="sxs-lookup"><span data-stu-id="b32b8-874">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="b32b8-875">Compilación 16176</span><span class="sxs-lookup"><span data-stu-id="b32b8-875">Build 16176</span></span>

<span data-ttu-id="b32b8-876">Para obtener información general de Windows sobre la compilación 16176, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-876">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-877">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-877">Fixed</span></span>

- [<span data-ttu-id="b32b8-878">Se ha habilitado la compatibilidad serie</span><span class="sxs-lookup"><span data-stu-id="b32b8-878">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="b32b8-879">Se ha agregado la opción de socket de IP IP_OPTIONS [GH 1116]</span><span class="sxs-lookup"><span data-stu-id="b32b8-879">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="b32b8-880">Se ha implementado la función pwritev (al cargar el archivo en nginx/PHP-FPM) [GH 1506]</span><span class="sxs-lookup"><span data-stu-id="b32b8-880">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="b32b8-881">Se han agregado opciones de socket IP IP_MULTICAST_IF e IPV6_MULTICAST_IF [GH 990]</span><span class="sxs-lookup"><span data-stu-id="b32b8-881">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="b32b8-882">Compatibilidad con la opción de socket IP_MULTICAST_LOOP e IPV6_MULTICAST_LOOP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="b32b8-882">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="b32b8-883">Se ha agregado la opción de socket IP(V6)_MTU para el nodo de aplicaciones, traceroute, dig, nslookup, host</span><span class="sxs-lookup"><span data-stu-id="b32b8-883">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="b32b8-884">Se ha agregado la opción de socket de IP IPV6_UNICAST_HOPS</span><span class="sxs-lookup"><span data-stu-id="b32b8-884">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="b32b8-885">Mejoras del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="b32b8-885">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="b32b8-886">Permite el montaje de rutas UNC</span><span class="sxs-lookup"><span data-stu-id="b32b8-886">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="b32b8-887">Habilita la compatibilidad con CDFS en drvfs</span><span class="sxs-lookup"><span data-stu-id="b32b8-887">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="b32b8-888">Controla correctamente los permisos para los sistemas de archivos de red en drvfs</span><span class="sxs-lookup"><span data-stu-id="b32b8-888">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="b32b8-889">Agrega compatibilidad para unidades remotas a drvfs</span><span class="sxs-lookup"><span data-stu-id="b32b8-889">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="b32b8-890">Habilita la compatibilidad con CDFS en drvfs</span><span class="sxs-lookup"><span data-stu-id="b32b8-890">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="b32b8-891">Mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-891">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-892">Resultados de LTP</span><span class="sxs-lookup"><span data-stu-id="b32b8-892">LTP Results</span></span>
<span data-ttu-id="b32b8-893">Sin cambios desde 15042</span><span class="sxs-lookup"><span data-stu-id="b32b8-893">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="b32b8-894">Compilación 16170</span><span class="sxs-lookup"><span data-stu-id="b32b8-894">Build 16170</span></span>

<span data-ttu-id="b32b8-895">Para obtener información general de Windows sobre la compilación 16170, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-895">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="b32b8-896">Hemos lanzado una nueva [publicación de blog](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) en la que se describen nuestros esfuerzos para probar WSL.</span><span class="sxs-lookup"><span data-stu-id="b32b8-896">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="b32b8-897">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-897">Fixed</span></span>

- <span data-ttu-id="b32b8-898">Compatibilidad para la opción de socket IP_ADD_MEMBERSHIP y IPV6_ADD_MEMBERSHIP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="b32b8-898">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="b32b8-899">Agrega compatibilidad para PTRACE_OLDSETOPTIONS.</span><span class="sxs-lookup"><span data-stu-id="b32b8-899">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="b32b8-900">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="b32b8-900">[GH 1692]</span></span>
- <span data-ttu-id="b32b8-901">Mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-901">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-902">Resultados de LTP</span><span class="sxs-lookup"><span data-stu-id="b32b8-902">LTP Results</span></span>
<span data-ttu-id="b32b8-903">Sin cambios desde 15042</span><span class="sxs-lookup"><span data-stu-id="b32b8-903">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="b32b8-904">Compilación 15046 a Windows 10 Creators Update</span><span class="sxs-lookup"><span data-stu-id="b32b8-904">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="b32b8-905">No hay más correcciones o características de WSL planeadas para su inclusión en Windows 10 Creators Update.</span><span class="sxs-lookup"><span data-stu-id="b32b8-905">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="b32b8-906">Las notas de la versión de WSL se reanudarán en las próximas semanas para las adiciones destinadas a la siguiente actualización principal de Windows.</span><span class="sxs-lookup"><span data-stu-id="b32b8-906">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="b32b8-907">Para obtener información general de Windows sobre la compilación 15046 y futuras publicaciones de Insider, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-907">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="b32b8-908">Compilación 15042</span><span class="sxs-lookup"><span data-stu-id="b32b8-908">Build 15042</span></span>

<span data-ttu-id="b32b8-909">Para obtener información general de Windows sobre la compilación 15042, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-909">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-910">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-910">Fixed</span></span>

- <span data-ttu-id="b32b8-911">Corrección para un interbloqueo al quitar una ruta de acceso que termina en ".."</span><span class="sxs-lookup"><span data-stu-id="b32b8-911">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="b32b8-912">Se ha corregido un problema por el que FIONBIO no devuelve 0 en caso correcto [GH 1683]</span><span class="sxs-lookup"><span data-stu-id="b32b8-912">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="b32b8-913">Se ha corregido un problema con lecturas de longitud cero de sockets de datagramas de inet</span><span class="sxs-lookup"><span data-stu-id="b32b8-913">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="b32b8-914">Corrección del posible interbloqueo debido a la condición de carrera en la búsqueda de inode de drvfs [GH 1675]</span><span class="sxs-lookup"><span data-stu-id="b32b8-914">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="b32b8-915">Se ha ampliado la compatibilidad con los datos suplementarios de los sockets de Unix; SCM_CREDENTIALS y SCM_RIGHTS [GH 514, 613, 1326]</span><span class="sxs-lookup"><span data-stu-id="b32b8-915">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="b32b8-916">Mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-916">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-917">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-917">LTP Results:</span></span>
<span data-ttu-id="b32b8-918">Número de pruebas superadas: 737</span><span class="sxs-lookup"><span data-stu-id="b32b8-918">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="b32b8-919">Número de no superadas (error, omitidas, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="b32b8-919">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="b32b8-920">Compilación 15031</span><span class="sxs-lookup"><span data-stu-id="b32b8-920">Build 15031</span></span>

<span data-ttu-id="b32b8-921">Para obtener información general de Windows sobre la compilación 15031, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-921">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-922">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-922">Fixed</span></span>

- <span data-ttu-id="b32b8-923">Se ha corregido un error en el que el time(2) se comportaba incorrectamente de manera esporádica.</span><span class="sxs-lookup"><span data-stu-id="b32b8-923">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="b32b8-924">Se ha corregido un problema donde las llamadas del sistema de \*SIGPROCMASK podían dañar la máscara de señal.</span><span class="sxs-lookup"><span data-stu-id="b32b8-924">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="b32b8-925">Ahora, devuelva la longitud completa de la línea de comandos en la notificación de creación del proceso de WSL.</span><span class="sxs-lookup"><span data-stu-id="b32b8-925">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="b32b8-926">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="b32b8-926">[GH 1632]</span></span>
- <span data-ttu-id="b32b8-927">WSL ahora informa de la salida del subproceso a través de ptrace para bloqueos de GDB.</span><span class="sxs-lookup"><span data-stu-id="b32b8-927">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="b32b8-928">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="b32b8-928">[GH 1196]</span></span>
- <span data-ttu-id="b32b8-929">Se ha corregido un error en el que ptys se bloqueaba después de una gran E/S de tmux</span><span class="sxs-lookup"><span data-stu-id="b32b8-929">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="b32b8-930">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="b32b8-930">[GH 1358]</span></span>
- <span data-ttu-id="b32b8-931">Se ha corregido la validación del tiempo de espera en muchas llamadas del sistema (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span><span class="sxs-lookup"><span data-stu-id="b32b8-931">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="b32b8-932">Se ha agregado compatibilidad con eventfd EFD_SEMAPHORE [GH 452]</span><span class="sxs-lookup"><span data-stu-id="b32b8-932">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="b32b8-933">Mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-933">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-934">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-934">LTP Results:</span></span>
<span data-ttu-id="b32b8-935">Número de pruebas superadas: 737</span><span class="sxs-lookup"><span data-stu-id="b32b8-935">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="b32b8-936">Número de no superadas (error, omitidas, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="b32b8-936">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="b32b8-937">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="b32b8-937">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="b32b8-938">Compilación 15025</span><span class="sxs-lookup"><span data-stu-id="b32b8-938">Build 15025</span></span>

<span data-ttu-id="b32b8-939">Para obtener información general de Windows sobre la compilación 15025, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-939">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-940">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-940">Fixed</span></span>

- <span data-ttu-id="b32b8-941">Corrección del error que dañó grep 2.27 [GH 1578]</span><span class="sxs-lookup"><span data-stu-id="b32b8-941">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="b32b8-942">Se ha implementado la marca EFD_SEMAPHORE para la llamada del sistema eventfd2 [GH 452]</span><span class="sxs-lookup"><span data-stu-id="b32b8-942">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="b32b8-943">Se ha implementado /proc/[pid]/net/ipv6_route [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="b32b8-943">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="b32b8-944">Compatibilidad de E/S controlada por señal para sockets de secuencia de Unix [GH 393, 68]</span><span class="sxs-lookup"><span data-stu-id="b32b8-944">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="b32b8-945">Compatibilidad con F_GETPIPE_SZ y F_SETPIPE_SZ [GH 1012]</span><span class="sxs-lookup"><span data-stu-id="b32b8-945">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="b32b8-946">Implementa la llamada del sistema recvmmsg() [GH 1531]</span><span class="sxs-lookup"><span data-stu-id="b32b8-946">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="b32b8-947">Se ha corregido un error en el que epoll_wait() no esperaba [GH 1609]</span><span class="sxs-lookup"><span data-stu-id="b32b8-947">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="b32b8-948">Implementa /proc/version_signature</span><span class="sxs-lookup"><span data-stu-id="b32b8-948">Implement /proc/version_signature</span></span>
- <span data-ttu-id="b32b8-949">La llamada del sistema Tee ahora devuelve un error si ambos descriptores de archivo hacen referencia a la misma canalización</span><span class="sxs-lookup"><span data-stu-id="b32b8-949">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="b32b8-950">Se ha implementado el comportamiento correcto de SO_PEERCRED para sockets de Unix</span><span class="sxs-lookup"><span data-stu-id="b32b8-950">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="b32b8-951">Se ha corregido el control de parámetros no válidos de llamada del sistema tkill</span><span class="sxs-lookup"><span data-stu-id="b32b8-951">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="b32b8-952">Cambios para aumentar el rendimiento de drvfs</span><span class="sxs-lookup"><span data-stu-id="b32b8-952">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="b32b8-953">Corrección menor para el bloqueo de E/S de Ruby</span><span class="sxs-lookup"><span data-stu-id="b32b8-953">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="b32b8-954">Se ha corregido recvmsg() que devuelve EINVAL para la marca MSG_DONTWAIT para sockets inet [GH 1296]</span><span class="sxs-lookup"><span data-stu-id="b32b8-954">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="b32b8-955">Mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-955">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-956">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-956">LTP Results:</span></span>
<span data-ttu-id="b32b8-957">Número de pruebas superadas: 732</span><span class="sxs-lookup"><span data-stu-id="b32b8-957">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="b32b8-958">Número de no superadas (error, omitidas, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="b32b8-958">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="b32b8-959">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="b32b8-959">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="b32b8-960">Compilación 15019</span><span class="sxs-lookup"><span data-stu-id="b32b8-960">Build 15019</span></span>

<span data-ttu-id="b32b8-961">Para obtener información general de Windows sobre la compilación 15019, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-961">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-962">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-962">Fixed</span></span>

- <span data-ttu-id="b32b8-963">Se ha corregido un error que informaba incorrectamente del uso de CPU en procfs para herramientas como htop (GH 823, 945, 971)</span><span class="sxs-lookup"><span data-stu-id="b32b8-963">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="b32b8-964">Al llamar a open() con O_TRUNC en un archivo existente inotify ahora genera IN_MODIFY antes de IN_OPEN</span><span class="sxs-lookup"><span data-stu-id="b32b8-964">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="b32b8-965">Correcciones para el SO_ERROR de sockets de Unix getsockopt para habilitar postgress [GH 61, 1354]</span><span class="sxs-lookup"><span data-stu-id="b32b8-965">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="b32b8-966">Implementa /proc/sys/net/core/somaxconn para el lenguaje GO</span><span class="sxs-lookup"><span data-stu-id="b32b8-966">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="b32b8-967">La tarea en segundo plano de actualización del paquete apt-get ahora se ejecuta oculta de la vista</span><span class="sxs-lookup"><span data-stu-id="b32b8-967">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="b32b8-968">Borra el ámbito de IPv6 localhost (error de Spring-Framework (Java)).</span><span class="sxs-lookup"><span data-stu-id="b32b8-968">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="b32b8-969">Mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-969">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-970">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-970">LTP Results:</span></span>
<span data-ttu-id="b32b8-971">Número de pruebas superadas: 714</span><span class="sxs-lookup"><span data-stu-id="b32b8-971">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="b32b8-972">Número de no superadas (error, omitidas, etc.): 249</span><span class="sxs-lookup"><span data-stu-id="b32b8-972">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="b32b8-973">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="b32b8-973">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="b32b8-974">Compilación 15014</span><span class="sxs-lookup"><span data-stu-id="b32b8-974">Build 15014</span></span>

<span data-ttu-id="b32b8-975">Para obtener información general de Windows sobre la compilación 15014, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="b32b8-975">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-976">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-976">Fixed</span></span>

- <span data-ttu-id="b32b8-977">Ctrl + C ahora funciona según lo previsto</span><span class="sxs-lookup"><span data-stu-id="b32b8-977">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="b32b8-978">htop y ps auxw ahora muestran el uso de recursos correcto (GH 516)</span><span class="sxs-lookup"><span data-stu-id="b32b8-978">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="b32b8-979">Traducción básica de excepciones de NT a señales.</span><span class="sxs-lookup"><span data-stu-id="b32b8-979">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="b32b8-980">(GH 513)</span><span class="sxs-lookup"><span data-stu-id="b32b8-980">(GH #513)</span></span>
- <span data-ttu-id="b32b8-981">fallocate ahora genera el error ENOSPC cuando se está quedando sin espacio en lugar de EINVAL (GH 1571)</span><span class="sxs-lookup"><span data-stu-id="b32b8-981">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="b32b8-982">Se ha agregado/proc/sys/kernel/sem.</span><span class="sxs-lookup"><span data-stu-id="b32b8-982">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="b32b8-983">Se han implementado las llamadas del sistema semop y semtimedop</span><span class="sxs-lookup"><span data-stu-id="b32b8-983">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="b32b8-984">Se han corregido errores de nslookup con la opción de socket IP_RECVTOS e IPV6_RECVTCLASS (GH 69)</span><span class="sxs-lookup"><span data-stu-id="b32b8-984">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="b32b8-985">Compatibilidad con las opciones de socket IP_RECVTTL e IPV6_RECVHOPLIMIT</span><span class="sxs-lookup"><span data-stu-id="b32b8-985">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="b32b8-986">Mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-986">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-987">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-987">LTP Results:</span></span>
<span data-ttu-id="b32b8-988">Número de pruebas superadas: 709</span><span class="sxs-lookup"><span data-stu-id="b32b8-988">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="b32b8-989">Número de no superadas (error, omitidas, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="b32b8-989">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="b32b8-990">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="b32b8-990">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="b32b8-991">Resumen de llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="b32b8-991">Syscall Summary</span></span>
<span data-ttu-id="b32b8-992">Total de llamadas del sistema: 384</span><span class="sxs-lookup"><span data-stu-id="b32b8-992">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="b32b8-993">Total implementado: 235</span><span class="sxs-lookup"><span data-stu-id="b32b8-993">Total Implemented: 235</span></span> </br>
<span data-ttu-id="b32b8-994">Total de procesos con stub: 22</span><span class="sxs-lookup"><span data-stu-id="b32b8-994">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="b32b8-995">Total no implementado: 127</span><span class="sxs-lookup"><span data-stu-id="b32b8-995">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="b32b8-996">Desglose detallado</span><span class="sxs-lookup"><span data-stu-id="b32b8-996">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="b32b8-997">Compilación 15007</span><span class="sxs-lookup"><span data-stu-id="b32b8-997">Build 15007</span></span>

<span data-ttu-id="b32b8-998">Para obtener información general de Windows sobre la compilación 15007, visita el [blog de Windows]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span><span class="sxs-lookup"><span data-stu-id="b32b8-998">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="b32b8-999">Problema conocido</span><span class="sxs-lookup"><span data-stu-id="b32b8-999">Known Issue</span></span>

- <span data-ttu-id="b32b8-1000">Hay un error conocido en el que la consola no reconoce algunas entradas Ctrl + <key>.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1000">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="b32b8-1001">Esto incluye el comando Ctrl-C, que actuará como una presión normal de "c".</span><span class="sxs-lookup"><span data-stu-id="b32b8-1001">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="b32b8-1002">Solución: Asigna una tecla alternativa a Ctrl+C.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1002">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="b32b8-1003">Por ejemplo, para asignar Ctrl+K a Ctrl+C, haz lo siguiente: `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1003">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="b32b8-1004">Esta asignación es por terminal y tendrá que hacerse *cada* vez que se inicie Bash.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1004">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="b32b8-1005">Los usuarios pueden explorar la opción para incluirlo en su `.bashrc`</span><span class="sxs-lookup"><span data-stu-id="b32b8-1005">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="b32b8-1006">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-1006">Fixed</span></span>

- <span data-ttu-id="b32b8-1007">Se ha corregido el problema que hacía que la ejecución de WSL consumiera el 100 % de un núcleo de CPU.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1007">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="b32b8-1008">Ahora se admite la opción de socket IP_PKTINFO, IPV6_RECVPKTINFO.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1008">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="b32b8-1009">(GH 851, 987)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1009">(GH #851, 987)</span></span>
- <span data-ttu-id="b32b8-1010">Trunca la dirección física de la interfaz de red a 16 bytes en lxcore (GH 1452, 1414, 1343, 468, 308)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1010">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="b32b8-1011">Mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-1011">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-1012">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-1012">LTP Results:</span></span>
<span data-ttu-id="b32b8-1013">Número de pruebas superadas: 709</span><span class="sxs-lookup"><span data-stu-id="b32b8-1013">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="b32b8-1014">Número de no superadas (error, omitidas, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="b32b8-1014">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="b32b8-1015">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="b32b8-1015">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="b32b8-1016">Compilación 15002</span><span class="sxs-lookup"><span data-stu-id="b32b8-1016">Build 15002</span></span>

<span data-ttu-id="b32b8-1017">Para obtener información general de Windows sobre la compilación 15002, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-1017">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="b32b8-1018">Problema conocido</span><span class="sxs-lookup"><span data-stu-id="b32b8-1018">Known Issue</span></span>

<span data-ttu-id="b32b8-1019">Dos problemas conocidos:</span><span class="sxs-lookup"><span data-stu-id="b32b8-1019">Two known issues:</span></span>
- <span data-ttu-id="b32b8-1020">Hay un error conocido en el que la consola no reconoce algunas entradas Ctrl + <key>.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1020">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="b32b8-1021">Esto incluye el comando Ctrl-C, que actuará como una presión normal de "c".</span><span class="sxs-lookup"><span data-stu-id="b32b8-1021">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="b32b8-1022">Solución: Asigna una tecla alternativa a Ctrl+C.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1022">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="b32b8-1023">Por ejemplo, para asignar Ctrl+K a Ctrl+C, haz lo siguiente: `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1023">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="b32b8-1024">Esta asignación es por terminal y tendrá que hacerse *cada* vez que se inicie Bash.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1024">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="b32b8-1025">Los usuarios pueden explorar la opción para incluirlo en su `.bashrc`</span><span class="sxs-lookup"><span data-stu-id="b32b8-1025">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="b32b8-1026">Mientras se ejecuta WSL, un subproceso del sistema consumirá el 100 % de un núcleo de CPU.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1026">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="b32b8-1027">La raíz de esto se ha solucionado y corregido internamente.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1027">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="b32b8-1028">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-1028">Fixed</span></span>

- <span data-ttu-id="b32b8-1029">Todas las sesiones de Bash ahora deben crearse en el mismo nivel de permiso.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1029">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="b32b8-1030">Se bloquearán los intentos de iniciar una sesión en un nivel diferente.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1030">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="b32b8-1031">Esto significa que las consolas de administrador y que no son de administración no se pueden ejecutarse al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1031">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="b32b8-1032">(GH 626)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1032">(GH #626)</span></span>
<br/>
- <span data-ttu-id="b32b8-1033">Se han implementado los siguientes mensajes NETLINK_ROUTE (requiere el administrador de Windows)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1033">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="b32b8-1034">RTM_NEWADDR (admite `ip addr add`)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1034">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="b32b8-1035">RTM_NEWROUTE (admite `ip route add`)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1035">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="b32b8-1036">RTM_DELADDR (admite `ip addr del`)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1036">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="b32b8-1037">RTM_DELROUTE (admite `ip route del`)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1037">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="b32b8-1038">La comprobación de tareas programadas para actualizar los paquetes ya no se ejecutará en una conexión de uso medido (GH 1371)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1038">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="b32b8-1039">Se ha corregido un error en el que la canalización se bloquea, es decir, bash -c "ls -alR /" | bash -c "cat" (GH 1214)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1039">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="b32b8-1040">Se ha implementado la opción de socket TCP_KEEPCNT (GH 843)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1040">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="b32b8-1041">Se ha implementado la opción de socket IP_MTU_DISCOVER INET (GH 720, 717, 170, 69)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1041">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="b32b8-1042">Se ha quitado la funcionalidad heredada para ejecutar archivos binarios de NT desde init con búsqueda de rutas de NT.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1042">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="b32b8-1043">(GH 1325)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1043">(GH #1325)</span></span>
- <span data-ttu-id="b32b8-1044">Corrección del modo de /dev/kmsg para permitir el acceso de lectura de grupo/otro (0644) (GH 1321)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1044">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="b32b8-1045">Se ha implementado /proc/sys/kernel/random/boot_id [GH 1092].</span><span class="sxs-lookup"><span data-stu-id="b32b8-1045">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="b32b8-1046">Se ha corregido el error en el que la hora de inicio del proceso se mostraba como el año 2432 (GH 974)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1046">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="b32b8-1047">Se ha cambiado la variable de entorno TERM predeterminada a xterm-256color (GH 1446)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1047">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="b32b8-1048">Se ha modificado la forma en que se calcula la confirmación del proceso durante la bifurcación del proceso.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1048">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="b32b8-1049">(GH 1286)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1049">(GH #1286)</span></span>
- <span data-ttu-id="b32b8-1050">Se ha implementado /proc/sys/vm/overcommit_memory.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1050">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="b32b8-1051">(GH 1286)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1051">(GH #1286)</span></span>
- <span data-ttu-id="b32b8-1052">Se ha implementado el archivo /proc/net/route (GH 69)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1052">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="b32b8-1053">Se ha corregido el error en el que el nombre de acceso directo se localizaba incorrectamente (GH 696)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1053">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="b32b8-1054">Se ha corregido la lógica de análisis de elf que valida incorrectamente los encabezados de programa debe ser menor que (o igual a) PATH_MAX.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1054">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="b32b8-1055">(GH 1048)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1055">(GH #1048)</span></span>
- <span data-ttu-id="b32b8-1056">Se ha implementado la devolución de llamada de statfs para procfs, sysfs, cgroupfs y binfmtfs (GH 1378)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1056">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="b32b8-1057">Se han corregido ventanas de AptPackageIndexUpdate que no se cierran (GH 1184, también se describe en GH 1193).</span><span class="sxs-lookup"><span data-stu-id="b32b8-1057">Fixed AptPackageIndexUpdate windows that won’t close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="b32b8-1058">Se ha agregado compatibilidad con la personalidad de ASLR ADDR_NO_RANDOMIZE.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1058">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="b32b8-1059">(GH 1148, 1128)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1059">(GH #1148, 1128)</span></span>
- <span data-ttu-id="b32b8-1060">Se han mejorado PTRACE_GETSIGINFO, SIGSEGV para los seguimientos de la pila gdb adecuados durante AV (GH 875)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1060">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="b32b8-1061">Ya no se produce un error en el análisis de elf para los archivos binarios de patchelf.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1061">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="b32b8-1062">(GH 471)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1062">(GH #471)</span></span>
- <span data-ttu-id="b32b8-1063">DNS de VPN propagado a/etc/resolv.conf (GH 416, 1350)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1063">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="b32b8-1064">Mejoras en el cierre de TCP para la transferencia de datos más confiable.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1064">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="b32b8-1065">(GH 610, 616, 1025, 1335)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1065">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="b32b8-1066">Ahora devuelve el código de error correcto cuando se abran demasiados archivos (EMFILE).</span><span class="sxs-lookup"><span data-stu-id="b32b8-1066">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="b32b8-1067">(GH 1126, 2090)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1067">(GH #1126, 2090)</span></span>
- <span data-ttu-id="b32b8-1068">El registro de auditoría de Windows ahora informa el nombre de la imagen en la creación del proceso de auditoría.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1068">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="b32b8-1069">Ahora se producen errores leves al iniciar bash.exe desde una ventana de Bash</span><span class="sxs-lookup"><span data-stu-id="b32b8-1069">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="b32b8-1070">Se ha agregado un mensaje de error cuando interop no puede acceder a un directorio de trabajo en LxFs (es decir, notepad.exe .bashrc)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1070">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="b32b8-1071">Se ha corregido un problema en el que la ruta de acceso de Windows se truncaba en WSL</span><span class="sxs-lookup"><span data-stu-id="b32b8-1071">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="b32b8-1072">Mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-1072">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-1073">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-1073">LTP Results:</span></span>
<span data-ttu-id="b32b8-1074">Número de pruebas superadas: 690</span><span class="sxs-lookup"><span data-stu-id="b32b8-1074">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="b32b8-1075">Número de no superadas (error, omitidas, etc.): 274</span><span class="sxs-lookup"><span data-stu-id="b32b8-1075">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="b32b8-1076">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="b32b8-1076">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="b32b8-1077">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="b32b8-1077">Syscall Support</span></span>
<span data-ttu-id="b32b8-1078">A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1078">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b32b8-1079">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1079">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="b32b8-1080">Compilación 14986</span><span class="sxs-lookup"><span data-stu-id="b32b8-1080">Build 14986</span></span>

<span data-ttu-id="b32b8-1081">Para obtener información general de Windows sobre la compilación 14986, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-1081">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-1082">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-1082">Fixed</span></span>

- <span data-ttu-id="b32b8-1083">Se han corregido comprobaciones de error con IOCTL de NetLink y Pty</span><span class="sxs-lookup"><span data-stu-id="b32b8-1083">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="b32b8-1084">La versión del kernel ahora informa 4.4.0-43 por coherencia con Xenial</span><span class="sxs-lookup"><span data-stu-id="b32b8-1084">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="b32b8-1085">Bash.exe ahora se inicia cuando la entrada se dirige a "nul" (GH 1259)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1085">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="b32b8-1086">Los identificadores de subproceso ahora se han declarado correctamente en procfs (GH 967)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1086">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="b32b8-1087">Las marcas IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR ahora se admiten en inotify_add_watch() (GH 1280)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1087">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="b32b8-1088">Implementa timer_create y llamadas del sistema relacionadas.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1088">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="b32b8-1089">Esto habilita la compatibilidad con GHC (GH 307)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1089">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="b32b8-1090">Se ha corregido un problema en el que ping devolvía una hora de 0,000 ms (GH 1296)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1090">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="b32b8-1091">Devuelve el código de error correcto cuando se abran demasiados archivos.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1091">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="b32b8-1092">Se ha corregido un problema en WSL donde la solicitud de NetLink de datos de la interfaz de red generaba un error con EINVAL si la dirección de hardware de la interfaz es de 32 bytes (por ejemplo, la interfaz Teredo)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1092">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="b32b8-1093">Ten en cuenta que la utilidad "ip" de Linux contiene un error en el que se bloqueará si WSL informa de una dirección de hardware de 32 bytes.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1093">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="b32b8-1094">Se trata de un error en "ip", no en WSL.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1094">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="b32b8-1095">La utilidad "ip" codifica de forma rígida la longitud del búfer de cadena usado para imprimir la dirección de hardware, y el búfer es demasiado pequeño para imprimir una dirección de hardware de 32 bytes.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1095">The “ip” utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="b32b8-1096">Mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-1096">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-1097">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-1097">LTP Results:</span></span>
<span data-ttu-id="b32b8-1098">Número de pruebas superadas: 669</span><span class="sxs-lookup"><span data-stu-id="b32b8-1098">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="b32b8-1099">Número de no superadas (error, omitidas, etc.): 258</span><span class="sxs-lookup"><span data-stu-id="b32b8-1099">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="b32b8-1100">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="b32b8-1100">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="b32b8-1101">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="b32b8-1101">Syscall Support</span></span>
<span data-ttu-id="b32b8-1102">A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1102">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b32b8-1103">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1103">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="b32b8-1104">Compilación 14971</span><span class="sxs-lookup"><span data-stu-id="b32b8-1104">Build 14971</span></span>

<span data-ttu-id="b32b8-1105">Para obtener información general de Windows sobre la compilación 14971, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-1105">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-1106">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-1106">Fixed</span></span>

 - <span data-ttu-id="b32b8-1107">Debido a circunstancias más allá de nuestro control, no hay ninguna actualización en esta compilación para el subsistema de Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1107">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="b32b8-1108">Las actualizaciones programadas regularmente se reanudarán en la próxima versión.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1108">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-1109">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-1109">LTP Results:</span></span>
<span data-ttu-id="b32b8-1110">Sin cambios desde 14965</span><span class="sxs-lookup"><span data-stu-id="b32b8-1110">Unchanged from 14965</span></span> </br>
<span data-ttu-id="b32b8-1111">Número de pruebas superadas: 664</span><span class="sxs-lookup"><span data-stu-id="b32b8-1111">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="b32b8-1112">Número de no superadas (error, omitidas, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="b32b8-1112">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="b32b8-1113">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="b32b8-1113">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="b32b8-1114">Compilación 14965</span><span class="sxs-lookup"><span data-stu-id="b32b8-1114">Build 14965</span></span>

<span data-ttu-id="b32b8-1115">Para obtener información general de Windows sobre la compilación 14965, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-1115">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-1116">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-1116">Fixed</span></span>

- <span data-ttu-id="b32b8-1117">Compatibilidad con RTM_GETLINK y RTM_GETADDR del protocolo NETLINK_ROUTE de sockets de Netlink (GH 468)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1117">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="b32b8-1118">Habilita los comandos ifconfig e ip para la enumeración de red</span><span class="sxs-lookup"><span data-stu-id="b32b8-1118">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="b32b8-1119">Puede encontrar más información en la [publicación de blog sobre redes WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-1119">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="b32b8-1120">/sbin está ahora en la ruta de acceso del usuario de manera predeterminada</span><span class="sxs-lookup"><span data-stu-id="b32b8-1120">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="b32b8-1121">La ruta de acceso de usuario de NT ahora se anexa a la ruta de acceso de WSL de manera predeterminada (es decir, ahora puedes escribir notepad.exe sin agregar System32 a la ruta de acceso de Linux)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1121">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="b32b8-1122">Se ha agregado compatibilidad para /proc/sys/kernel/cap_last_cap</span><span class="sxs-lookup"><span data-stu-id="b32b8-1122">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="b32b8-1123">Los archivos binarios de NT ahora se pueden iniciar desde WSL cuando el directorio de trabajo actual contiene caracteres que no son ANSI (GH 1254)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1123">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="b32b8-1124">Permite el apagado en el socket de flujo Unix desconectado.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1124">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="b32b8-1125">Se ha agregado compatibilidad para PR_GET_PDEATHSIG.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1125">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="b32b8-1126">Se ha agregado compatibilidad para CLONE_PARENT</span><span class="sxs-lookup"><span data-stu-id="b32b8-1126">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="b32b8-1127">Se ha corregido un error en el que la canalización se bloquea, es decir, bash -c "ls -alR /" | bash -c "cat" (GH 1214)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1127">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="b32b8-1128">Controla las solicitudes para conectarse al terminal actual.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1128">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="b32b8-1129">Marca /proc/<pid>/oom_score_adj como grabable.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1129">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="b32b8-1130">Agrega la carpeta/sys/fs/cgroup.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1130">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="b32b8-1131">sched_setaffinity debe devolver el número de máscara de bits de afinidad</span><span class="sxs-lookup"><span data-stu-id="b32b8-1131">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="b32b8-1132">Corrige la lógica de validación de ELF que presupone incorrectamente que las rutas de intérprete deben tener menos de 64 caracteres de longitud.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1132">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="b32b8-1133">(GH 743)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1133">(GH #743)</span></span>
- <span data-ttu-id="b32b8-1134">Los descriptores de archivos abiertos pueden mantener abierta la ventana de la consola (GH 1187)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1134">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="b32b8-1135">Se ha corregido el error en el que no se podía completar rename() con la barra diagonal final en el nombre de destino (GH 1008)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1135">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="b32b8-1136">Implementa el archivo /proc/net/dev</span><span class="sxs-lookup"><span data-stu-id="b32b8-1136">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="b32b8-1137">Se han corregido los pings de 0,000 ms debido a la resolución del temporizador.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1137">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="b32b8-1138">Se ha implementado /proc/self/environ (GH 730)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1138">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="b32b8-1139">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-1139">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-1140">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-1140">LTP Results:</span></span>
<span data-ttu-id="b32b8-1141">Número de pruebas superadas: 664</span><span class="sxs-lookup"><span data-stu-id="b32b8-1141">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="b32b8-1142">Número de no superadas (error, omitidas, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="b32b8-1142">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="b32b8-1143">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="b32b8-1143">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="b32b8-1144">Compilación 14959</span><span class="sxs-lookup"><span data-stu-id="b32b8-1144">Build 14959</span></span>

<span data-ttu-id="b32b8-1145">Para obtener información general de Windows sobre la compilación 14959, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span><span class="sxs-lookup"><span data-stu-id="b32b8-1145">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-1146">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-1146">Fixed</span></span>

- <span data-ttu-id="b32b8-1147">Se ha mejorado la notificación del proceso PICO para Windows.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1147">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="b32b8-1148">Encuentra información adicional en el [blog de WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-1148">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="b32b8-1149">Se ha mejorado la estabilidad de interoperabilidad con Windows</span><span class="sxs-lookup"><span data-stu-id="b32b8-1149">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="b32b8-1150">Se ha corregido el error 0x80070057 al iniciar bash.exe cuando Protección de datos de empresa (EDP) está habilitado</span><span class="sxs-lookup"><span data-stu-id="b32b8-1150">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="b32b8-1151">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-1151">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-1152">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-1152">LTP Results:</span></span>
<span data-ttu-id="b32b8-1153">Número de pruebas superadas: 665</span><span class="sxs-lookup"><span data-stu-id="b32b8-1153">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="b32b8-1154">Número de no superadas (error, omitidas, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="b32b8-1154">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="b32b8-1155">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="b32b8-1155">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="b32b8-1156">Compilación 14955</span><span class="sxs-lookup"><span data-stu-id="b32b8-1156">Build 14955</span></span>

<span data-ttu-id="b32b8-1157">Para obtener información general de Windows sobre la compilación 14955, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span><span class="sxs-lookup"><span data-stu-id="b32b8-1157">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-1158">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-1158">Fixed</span></span>

 - <span data-ttu-id="b32b8-1159">Debido a circunstancias más allá de nuestro control, no hay ninguna actualización en esta compilación para el subsistema de Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1159">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="b32b8-1160">Las actualizaciones programadas regularmente se reanudarán en la próxima versión.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1160">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-1161">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-1161">LTP Results:</span></span>
<span data-ttu-id="b32b8-1162">Número de pruebas superadas: 665</span><span class="sxs-lookup"><span data-stu-id="b32b8-1162">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="b32b8-1163">Número de no superadas (error, omitidas, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="b32b8-1163">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="b32b8-1164">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="b32b8-1164">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="b32b8-1165">Compilación 14951</span><span class="sxs-lookup"><span data-stu-id="b32b8-1165">Build 14951</span></span>

<span data-ttu-id="b32b8-1166">Para obtener información general de Windows sobre la compilación 14951, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-1166">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="b32b8-1167">Nueva característica: Interoperabilidad de Windows/Ubuntu</span><span class="sxs-lookup"><span data-stu-id="b32b8-1167">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="b32b8-1168">Ahora se pueden invocar archivos binarios de Windows directamente desde la línea de comandos de WSL.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1168">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="b32b8-1169">Esto da a los usuarios la capacidad de interactuar con el entorno y el sistema Windows de una manera que antes no era posible.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1169">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="b32b8-1170">Como ejemplo rápido, ahora es posible que los usuarios ejecuten los siguientes comandos:</span><span class="sxs-lookup"><span data-stu-id="b32b8-1170">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="b32b8-1171">Puedes encontrar más información en:</span><span class="sxs-lookup"><span data-stu-id="b32b8-1171">More information can be found at:</span></span>

- [<span data-ttu-id="b32b8-1172">Blog del equipo de WSL para Interop</span><span class="sxs-lookup"><span data-stu-id="b32b8-1172">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="b32b8-1173">Documentación de interoperabilidad de MSDN</span><span class="sxs-lookup"><span data-stu-id="b32b8-1173">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="b32b8-1174">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-1174">Fixed</span></span>

- <span data-ttu-id="b32b8-1175">Ubuntu 16.04 (Xenial) ahora se instala para todas las instancias nuevas de WSL.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1175">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="b32b8-1176">Los usuarios con instancias existentes de 14.04 (Trusty) no se actualizarán automáticamente.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1176">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="b32b8-1177">Ahora se muestra la configuración regional establecida durante la instalación</span><span class="sxs-lookup"><span data-stu-id="b32b8-1177">Locale set during install is now displayed</span></span>
- <span data-ttu-id="b32b8-1178">Mejoras del terminal, que incluido un error en el que la redirección de un proceso de WSL a un archivo no siempre funciona</span><span class="sxs-lookup"><span data-stu-id="b32b8-1178">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="b32b8-1179">La duración de la consola debe estar asociada a la duración de bash.exe</span><span class="sxs-lookup"><span data-stu-id="b32b8-1179">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="b32b8-1180">El tamaño de la ventana de la consola debe usar un tamaño visible, no el tamaño del búfer</span><span class="sxs-lookup"><span data-stu-id="b32b8-1180">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="b32b8-1181">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-1181">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-1182">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-1182">LTP Results:</span></span>
<span data-ttu-id="b32b8-1183">Número de pruebas superadas: 665</span><span class="sxs-lookup"><span data-stu-id="b32b8-1183">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="b32b8-1184">Número de no superadas (error, omitidas, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="b32b8-1184">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="b32b8-1185">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="b32b8-1185">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="b32b8-1186">Compilación 14946</span><span class="sxs-lookup"><span data-stu-id="b32b8-1186">Build 14946</span></span>

<span data-ttu-id="b32b8-1187">Para obtener información general de Windows sobre la compilación 14946, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span><span class="sxs-lookup"><span data-stu-id="b32b8-1187">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-1188">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-1188">Fixed</span></span>

- <span data-ttu-id="b32b8-1189">Se ha corregido un problema que impedía la creación de cuentas de usuario de WSL para los usuarios con nombres de usuario de NT que contienen espacios o comillas.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1189">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="b32b8-1190">Cambia VolFs y DrvFs para que devuelvan 0 para el recuento de vínculos de directorio en stat</span><span class="sxs-lookup"><span data-stu-id="b32b8-1190">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="b32b8-1191">Compatibilidad con la opción de socket IPV6_MULTICAST_HOPS.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1191">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="b32b8-1192">Limite a un único bucle de E/S de la consola por tty.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1192">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="b32b8-1193">Por ejemplo, el comando siguiente es posible:</span><span class="sxs-lookup"><span data-stu-id="b32b8-1193">Example: the following command is possible:</span></span>
  - <span data-ttu-id="b32b8-1194">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span><span class="sxs-lookup"><span data-stu-id="b32b8-1194">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="b32b8-1195">Reemplaza espacios con tabulaciones en/proc/cpuinfo (GH 1115)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1195">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="b32b8-1196">DrvFs aparece ahora en mountinfo con un nombre que coincide con el volumen de Windows montado</span><span class="sxs-lookup"><span data-stu-id="b32b8-1196">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="b32b8-1197">/home y /root ahora aparecen en mountinfo con los nombres correctos</span><span class="sxs-lookup"><span data-stu-id="b32b8-1197">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="b32b8-1198">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-1198">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-1199">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-1199">LTP Results:</span></span>
<span data-ttu-id="b32b8-1200">Número de pruebas superadas: 665</span><span class="sxs-lookup"><span data-stu-id="b32b8-1200">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="b32b8-1201">Número de no superadas (error, omitidas, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="b32b8-1201">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="b32b8-1202">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="b32b8-1202">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="b32b8-1203">Compilación 14942</span><span class="sxs-lookup"><span data-stu-id="b32b8-1203">Build 14942</span></span>

<span data-ttu-id="b32b8-1204">Para obtener información general de Windows sobre la compilación 14942, visita el [blog de Windows](https://aka.ms/onefourninefourtwoooooo).</span><span class="sxs-lookup"><span data-stu-id="b32b8-1204">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-1205">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-1205">Fixed</span></span>

- <span data-ttu-id="b32b8-1206">Un número de comprobaciones de error direccionadas, incluido el bloqueo de red "ATTEMPTED EXECUTE OF NOEXECUTE MEMORY" que bloqueaba SSH</span><span class="sxs-lookup"><span data-stu-id="b32b8-1206">A number of bugchecks addressed, including the “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” networking crash which was blocking SSH</span></span>
- <span data-ttu-id="b32b8-1207">Ahora se incluye la compatibilidad de inotifiy con las notificaciones generadas desde aplicaciones Windows en DrvFs</span><span class="sxs-lookup"><span data-stu-id="b32b8-1207">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="b32b8-1208">Implementa TCP_KEEPIDLE y TCP_KEEPINTVL para mongod.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1208">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="b32b8-1209">(GH 695)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1209">(GH #695)</span></span>
- <span data-ttu-id="b32b8-1210">Implementa la llamada del sistema pivot_root</span><span class="sxs-lookup"><span data-stu-id="b32b8-1210">Implement the pivot_root system call</span></span>
- <span data-ttu-id="b32b8-1211">Implementa la opción de socket para SO_DONTROUTE</span><span class="sxs-lookup"><span data-stu-id="b32b8-1211">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="b32b8-1212">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-1212">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="b32b8-1213">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-1213">LTP Results:</span></span>
<span data-ttu-id="b32b8-1214">Número de pruebas superadas: 665</span><span class="sxs-lookup"><span data-stu-id="b32b8-1214">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="b32b8-1215">Número de no superadas (error, omitidas, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="b32b8-1215">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="b32b8-1216">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="b32b8-1216">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="b32b8-1217">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="b32b8-1217">Syscall Support</span></span>
<span data-ttu-id="b32b8-1218">A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1218">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b32b8-1219">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1219">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="b32b8-1220">Compilación 14936</span><span class="sxs-lookup"><span data-stu-id="b32b8-1220">Build 14936</span></span>

<span data-ttu-id="b32b8-1221">Para obtener información general de Windows sobre la compilación 14936, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-1221">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="b32b8-1222">Nota: WSL instalará Ubuntu versión 16.04 (Xenial) en lugar de Ubuntu 14.04 (Trusty) en una próxima versión.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1222">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="b32b8-1223">Este cambio se aplicará a los usuarios de Insider que instalen nuevas instancias (lxrun.exe /install o a la primera ejecución de bash.exe).</span><span class="sxs-lookup"><span data-stu-id="b32b8-1223">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="b32b8-1224">Las instancias existentes con Trusty no se actualizarán automáticamente.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1224">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="b32b8-1225">Los usuarios pueden actualizar su imagen de Trusty a Xenial con el comando do-release-upgrade.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1225">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="b32b8-1226">Problema conocido</span><span class="sxs-lookup"><span data-stu-id="b32b8-1226">Known Issue</span></span>
<span data-ttu-id="b32b8-1227">WSL está experimentando un problema con algunas implementaciones de sockets.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1227">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="b32b8-1228">La comprobación de errores se manifiesta como bloqueo con el error "ATTEMPTED EXECUTE OF NOEXECUTE MEMORY".</span><span class="sxs-lookup"><span data-stu-id="b32b8-1228">The bugcheck manifests itself as a crash with the error “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”.</span></span>  <span data-ttu-id="b32b8-1229">La manifestación más común de este problema es un bloqueo cuando se usa ssh.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1229">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="b32b8-1230">La causa principal se ha corregido en las compilaciones internas y se enviará a los usuarios de Insider lo antes posible.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1230">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="b32b8-1231">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-1231">Fixed</span></span>

- <span data-ttu-id="b32b8-1232">Se ha implementado la llamada del sistema chroot</span><span class="sxs-lookup"><span data-stu-id="b32b8-1232">Implemented the chroot system call</span></span>
- <span data-ttu-id="b32b8-1233">Mejoras en inotify, ~~incluida la compatibilidad con las notificaciones generadas desde aplicaciones Windows en DrvFs~~</span><span class="sxs-lookup"><span data-stu-id="b32b8-1233">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="b32b8-1234">Corrección: La compatibilidad de inotify con los cambios que se originan en aplicaciones Windows no está disponible en este momento.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1234">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="b32b8-1235">El enlace de sockets a IPV6::<port n> ahora admite IPV6_V6ONLY (GH 68, 157, 393, 460, 674, 740, 982, 996)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1235">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="b32b8-1236">Se ha implementado el comportamiento de WNOWAIT para la llamada del sistema waitid (GH 638)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1236">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="b32b8-1237">Compatibilidad con las opciones de socket de IP IP_HDRINCL e IP_TTL</span><span class="sxs-lookup"><span data-stu-id="b32b8-1237">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="b32b8-1238">read() de longitud cero debe volver inmediatamente (GH 975)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1238">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="b32b8-1239">Controla correctamente los nombres de archivo y los prefijos de nombre de archivo que no incluyen un terminador NULL en un archivo .tar.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1239">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="b32b8-1240">Compatibilidad de epoll para /dev/null</span><span class="sxs-lookup"><span data-stu-id="b32b8-1240">epoll support for /dev/null</span></span>
- <span data-ttu-id="b32b8-1241">Corrección del origen de hora de /dev/alarm</span><span class="sxs-lookup"><span data-stu-id="b32b8-1241">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="b32b8-1242">bash -c ahora puede redirigir a un archivo</span><span class="sxs-lookup"><span data-stu-id="b32b8-1242">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="b32b8-1243">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-1243">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-1244">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-1244">LTP Results:</span></span>
<span data-ttu-id="b32b8-1245">Número de pruebas superadas: 664</span><span class="sxs-lookup"><span data-stu-id="b32b8-1245">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="b32b8-1246">Número de no superadas (error, omitidas, etc.): 264</span><span class="sxs-lookup"><span data-stu-id="b32b8-1246">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="b32b8-1247">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="b32b8-1247">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="b32b8-1248">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="b32b8-1248">Syscall Support</span></span>
<span data-ttu-id="b32b8-1249">A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1249">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b32b8-1250">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1250">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="b32b8-1251">Compilación 14931</span><span class="sxs-lookup"><span data-stu-id="b32b8-1251">Build 14931</span></span>

<span data-ttu-id="b32b8-1252">Para obtener información general de Windows sobre la compilación 14931, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-1252">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-1253">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-1253">Fixed</span></span>

 - <span data-ttu-id="b32b8-1254">Debido a circunstancias más allá de nuestro control, no hay ninguna actualización en esta compilación para el subsistema de Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1254">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="b32b8-1255">Las actualizaciones programadas regularmente se reanudarán en la próxima versión.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1255">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="b32b8-1256">Compilación 14926</span><span class="sxs-lookup"><span data-stu-id="b32b8-1256">Build 14926</span></span>

<span data-ttu-id="b32b8-1257">Para obtener información general de Windows sobre la compilación 14926, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-1257">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-1258">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-1258">Fixed</span></span>

- <span data-ttu-id="b32b8-1259">Ping ahora funciona en consolas que no tienen privilegios de administrador</span><span class="sxs-lookup"><span data-stu-id="b32b8-1259">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="b32b8-1260">Ahora también se admite Ping6, sin privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1260">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="b32b8-1261">Compatibilidad de inotify con archivos modificados a través de WSL.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1261">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="b32b8-1262">(GH 216)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1262">(GH #216)</span></span>
  - <span data-ttu-id="b32b8-1263">Marcas admitidas:</span><span class="sxs-lookup"><span data-stu-id="b32b8-1263">Flags supported:</span></span>
    - <span data-ttu-id="b32b8-1264">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="b32b8-1264">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="b32b8-1265">Eventos de inotify_add_watch: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="b32b8-1265">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="b32b8-1266">Atributos de inotify_add_watch: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="b32b8-1266">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="b32b8-1267">Salida de lectura: LX_IN_ISDIR, LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="b32b8-1267">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="b32b8-1268">Problema conocido: La modificación de archivos desde aplicaciones de Windows no genera ningún evento</span><span class="sxs-lookup"><span data-stu-id="b32b8-1268">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="b32b8-1269">El socket de Unix ahora es compatible con SCM_CREDENTIALS</span><span class="sxs-lookup"><span data-stu-id="b32b8-1269">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="b32b8-1270">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="b32b8-1270">LTP Results:</span></span>
<span data-ttu-id="b32b8-1271">Número de pruebas superadas: 651</span><span class="sxs-lookup"><span data-stu-id="b32b8-1271">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="b32b8-1272">Número de no superadas (error, omitidas, etc.): 258</span><span class="sxs-lookup"><span data-stu-id="b32b8-1272">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="b32b8-1273">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="b32b8-1273">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="b32b8-1274">Compilación 14915</span><span class="sxs-lookup"><span data-stu-id="b32b8-1274">Build 14915</span></span>

<span data-ttu-id="b32b8-1275">Para obtener información general de Windows sobre la compilación 14915, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="b32b8-1275">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-1276">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-1276">Fixed</span></span>
-  <span data-ttu-id="b32b8-1277">Socketpair para sockets de datagramas de Unix (GH 262)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1277">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="b32b8-1278">Compatibilidad con el socket de Unix para SO_REUSEADDR</span><span class="sxs-lookup"><span data-stu-id="b32b8-1278">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="b32b8-1279">Compatibilidad con el socket de Unix para SO_BROADCAST (GH 568)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1279">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="b32b8-1280">Compatibilidad con el socket de Unix para SOCK_SEQPACKET (GH 758, 546)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1280">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="b32b8-1281">Adición de compatibilidad para socket de datagramas de Unix send, recv y shutdown</span><span class="sxs-lookup"><span data-stu-id="b32b8-1281">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="b32b8-1282">Corrección de comprobación de errores debido a la validación de parámetros mmap no válida para direcciones no fijas.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1282">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="b32b8-1283">(GH 847)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1283">(GH #847)</span></span>
- <span data-ttu-id="b32b8-1284">Compatibilidad para suspender o reanudar los estados del terminal</span><span class="sxs-lookup"><span data-stu-id="b32b8-1284">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="b32b8-1285">Compatibilidad para TIOCPKT ioctl para desbloquear la utilidad de pantalla (GH 774)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1285">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="b32b8-1286">Problema conocido: Las teclas de función no funcionan</span><span class="sxs-lookup"><span data-stu-id="b32b8-1286">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="b32b8-1287">Se ha corregido una carrera en TimerFd que podía hacer que LxpTimerFdWorkerRoutine accediera a un miembro liberado "ReaderReady" (GH 814)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1287">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="b32b8-1288">Habilita la compatibilidad con llamadas del sistema reiniciables para futex, poll y clock_nanosleep</span><span class="sxs-lookup"><span data-stu-id="b32b8-1288">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="b32b8-1289">Se ha agregado compatibilidad con montaje de enlace</span><span class="sxs-lookup"><span data-stu-id="b32b8-1289">Added bind mount support</span></span>
- <span data-ttu-id="b32b8-1290">Compatibilidad para dejar de compartir el espacio de nombres de montaje</span><span class="sxs-lookup"><span data-stu-id="b32b8-1290">unshare for mount namespace support</span></span>
    - <span data-ttu-id="b32b8-1291">Problema conocido: Al crear un nuevo espacio de nombres de montaje con `unshare(CLONE_NEWNS)`, el directorio de trabajo actual continuará señalando al espacio de nombres anterior</span><span class="sxs-lookup"><span data-stu-id="b32b8-1291">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="b32b8-1292">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-1292">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="b32b8-1293">Compilación 14905</span><span class="sxs-lookup"><span data-stu-id="b32b8-1293">Build 14905</span></span>

<span data-ttu-id="b32b8-1294">Para obtener información general de Windows sobre la compilación 14905, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-1294">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-1295">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-1295">Fixed</span></span>
- <span data-ttu-id="b32b8-1296">Ahora se admiten llamadas del sistema reiniciables (GH 349, GH 520)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1296">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="b32b8-1297">Los vínculos simbólicos a directorios que terminan en / ahora están operativos (GH 650)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1297">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="b32b8-1298">Se ha implementado RNDGETENTCNT ioctl para /dev/random</span><span class="sxs-lookup"><span data-stu-id="b32b8-1298">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="b32b8-1299">Se han implementado los archivos /proc/[pid]/mounts, /proc/[pid]/mountinfo y /proc/[pid]/mountstats</span><span class="sxs-lookup"><span data-stu-id="b32b8-1299">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="b32b8-1300">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-1300">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="b32b8-1301">Compilación 14901</span><span class="sxs-lookup"><span data-stu-id="b32b8-1301">Build 14901</span></span>
<span data-ttu-id="b32b8-1302">Primera compilación de Insider para la versión posterior a la Actualización de aniversario de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1302">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="b32b8-1303">Para obtener información general de Windows sobre la compilación 14901, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-1303">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-1304">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-1304">Fixed</span></span>
- <span data-ttu-id="b32b8-1305">Se ha corregido un problema de barra diagonal final</span><span class="sxs-lookup"><span data-stu-id="b32b8-1305">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="b32b8-1306">Ahora funcionan los comandos como `$ mv a/c/ a/b/`</span><span class="sxs-lookup"><span data-stu-id="b32b8-1306">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="b32b8-1307">Al instalar ahora se pregunta si la configuración regional de Ubuntu debe establecerse en la configuración regional de Windows</span><span class="sxs-lookup"><span data-stu-id="b32b8-1307">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="b32b8-1308">Compatibilidad de procfs para la carpeta ns</span><span class="sxs-lookup"><span data-stu-id="b32b8-1308">Procfs support for ns folder</span></span>
- <span data-ttu-id="b32b8-1309">Se ha agregado mount y unmount para los sistemas de archivos tmpfs, procfs y sysfs</span><span class="sxs-lookup"><span data-stu-id="b32b8-1309">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="b32b8-1310">Corrección de la firma ABI mknod[at] de 32 bits</span><span class="sxs-lookup"><span data-stu-id="b32b8-1310">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="b32b8-1311">Los sockets de Unix se movieron al modelo dispatch</span><span class="sxs-lookup"><span data-stu-id="b32b8-1311">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="b32b8-1312">Se debe respetar el tamaño del búfer de recepción del socket de INET mediante setsockopt</span><span class="sxs-lookup"><span data-stu-id="b32b8-1312">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="b32b8-1313">Implementa la marca de mensaje de recepción de socket de Unix MSG_CMSG_CLOEXEC</span><span class="sxs-lookup"><span data-stu-id="b32b8-1313">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="b32b8-1314">Redirección de canalización stdin/stdout de proceso de Linux (GH 2)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1314">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="b32b8-1315">Permite la canalización de comandos bash -c en CMD.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1315">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="b32b8-1316">Ejemplo:  >dir | bash -c "grep foo"</span><span class="sxs-lookup"><span data-stu-id="b32b8-1316">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="b32b8-1317">Bash ahora se puede instalar en sistemas con varios archivos de página (GH 538, 358)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1317">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="b32b8-1318">El tamaño predeterminado del búfer del socket de INET debe coincidir con el de la configuración predeterminada de Ubuntu</span><span class="sxs-lookup"><span data-stu-id="b32b8-1318">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="b32b8-1319">Alinea las llamadas del sistema xattr con listxattr</span><span class="sxs-lookup"><span data-stu-id="b32b8-1319">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="b32b8-1320">Solo se devuelven interfaces con una dirección IPv4 válida de SIOCGIFCONF</span><span class="sxs-lookup"><span data-stu-id="b32b8-1320">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="b32b8-1321">Corrección de la acción predeterminada de la señal cuando se inserta por ptrace</span><span class="sxs-lookup"><span data-stu-id="b32b8-1321">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="b32b8-1322">Implementa /proc/sys/vm/min_free_kbytes</span><span class="sxs-lookup"><span data-stu-id="b32b8-1322">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="b32b8-1323">Usa valores de registro de contexto de equipo al restaurar el contexto en sigreturn</span><span class="sxs-lookup"><span data-stu-id="b32b8-1323">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="b32b8-1324">Esto resuelve el problema por el que java y javac se bloqueaban para algunos usuarios</span><span class="sxs-lookup"><span data-stu-id="b32b8-1324">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="b32b8-1325">Implementa /proc/sys/kernel/hostname</span><span class="sxs-lookup"><span data-stu-id="b32b8-1325">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="b32b8-1326">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="b32b8-1326">Syscall Support</span></span>
<span data-ttu-id="b32b8-1327">A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1327">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b32b8-1328">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1328">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="b32b8-1329">Compilación 14388 para la Actualización de aniversario de Windows 10</span><span class="sxs-lookup"><span data-stu-id="b32b8-1329">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="b32b8-1330">Para obtener información general de Windows sobre la compilación 14388, visita el [blog de Windows](https://aka.ms/14388wip).</span><span class="sxs-lookup"><span data-stu-id="b32b8-1330">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="b32b8-1331">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-1331">Fixed</span></span>
- <span data-ttu-id="b32b8-1332">Correcciones para prepararse para la Actualización de aniversario de Windows 10 el 2/8</span><span class="sxs-lookup"><span data-stu-id="b32b8-1332">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="b32b8-1333">Puedes encontrar más información sobre WSL en la Actualización de aniversario en nuestro [blog](https://blogs.msdn.microsoft.com/wsl/)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1333">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="b32b8-1334">Compilación 14376</span><span class="sxs-lookup"><span data-stu-id="b32b8-1334">Build 14376</span></span>
<span data-ttu-id="b32b8-1335">Para obtener información general de Windows sobre la compilación 14376, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-1335">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="b32b8-1336">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-1336">Fixed</span></span>
- <span data-ttu-id="b32b8-1337">Se quitaron algunas instancias en las que apt-get se bloquea (GH 493)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1337">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="b32b8-1338">Se ha corregido un problema por el que los montajes vacíos no se controlaban correctamente</span><span class="sxs-lookup"><span data-stu-id="b32b8-1338">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="b32b8-1339">Se ha corregido un problema por el que ramdisks no se montaban correctamente</span><span class="sxs-lookup"><span data-stu-id="b32b8-1339">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="b32b8-1340">Cambio en la aceptación de sockets de Unix para admitir marcas (GH parcial 451)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1340">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="b32b8-1341">Se ha corregido la pantalla azul relacionada con la red común</span><span class="sxs-lookup"><span data-stu-id="b32b8-1341">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="b32b8-1342">Se ha corregido la pantalla azul al acceder a /proc/[pid]/task (GH 523)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1342">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="b32b8-1343">Se ha corregido un uso elevado de la CPU en algunos escenarios de pty (GH 488, 504)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1343">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="b32b8-1344">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-1344">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="b32b8-1345">Compilación 14371</span><span class="sxs-lookup"><span data-stu-id="b32b8-1345">Build 14371</span></span>
<span data-ttu-id="b32b8-1346">Para obtener información general de Windows sobre la compilación 14371, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-1346">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="b32b8-1347">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-1347">Fixed</span></span>
- <span data-ttu-id="b32b8-1348">Se ha corregido la carrera de tiempo con SIGCHLD y wait() al usar ptrace</span><span class="sxs-lookup"><span data-stu-id="b32b8-1348">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="b32b8-1349">Se han corregido comportamientos cuando las rutas de acceso tienen una / final (GH 432)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1349">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="b32b8-1350">Se ha corregido un problema con el error de cambio de nombre o desvinculación debido a identificadores abiertos a elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b32b8-1350">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="b32b8-1351">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-1351">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="b32b8-1352">Compilación 14366</span><span class="sxs-lookup"><span data-stu-id="b32b8-1352">Build 14366</span></span>
<span data-ttu-id="b32b8-1353">Para obtener información general de Windows sobre la compilación 14366, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span><span class="sxs-lookup"><span data-stu-id="b32b8-1353">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="b32b8-1354">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-1354">Fixed</span></span>
- <span data-ttu-id="b32b8-1355">Corrección en la creación de archivos mediante vínculos simbólicos</span><span class="sxs-lookup"><span data-stu-id="b32b8-1355">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="b32b8-1356">Se ha agregado listxattr para Python (GH 385)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1356">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="b32b8-1357">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-1357">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="b32b8-1358">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="b32b8-1358">Syscall Support</span></span>
-   <span data-ttu-id="b32b8-1359">A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1359">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b32b8-1360">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1360">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="b32b8-1361">Compilación 14361</span><span class="sxs-lookup"><span data-stu-id="b32b8-1361">Build 14361</span></span>
<span data-ttu-id="b32b8-1362">Para obtener información general de Windows sobre la compilación 14361, visita el [blog de Windows](https://aka.ms/wip14361).</span><span class="sxs-lookup"><span data-stu-id="b32b8-1362">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="b32b8-1363">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-1363">Fixed</span></span>
- <span data-ttu-id="b32b8-1364">DrvFs ahora distingue entre mayúsculas y minúsculas cuando se ejecuta en Bash en Ubuntu en Windows.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1364">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="b32b8-1365">Los usuarios pueden usar case.txt y CASE.TXT en sus unidades de /mnt/c</span><span class="sxs-lookup"><span data-stu-id="b32b8-1365">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="b32b8-1366">La distinción de mayúsculas y minúsculas solo se admite en Bash en Ubuntu en Windows.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1366">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="b32b8-1367">Fuera de Bash, NTFS notificará los archivos correctamente, pero puede producirse un comportamiento inesperado al interactuar con los archivos de Windows.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1367">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="b32b8-1368">La raíz de cada volumen (es decir, /mnt/c) no distingue entre mayúsculas y minúsculas</span><span class="sxs-lookup"><span data-stu-id="b32b8-1368">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="b32b8-1369">Puedes encontrar más información sobre cómo controlar estos archivos en Windows [aquí](https://support.microsoft.com/en-us/kb/100625).</span><span class="sxs-lookup"><span data-stu-id="b32b8-1369">More information on handling these files in Windows can be found [here](https://support.microsoft.com/en-us/kb/100625).</span></span>
- <span data-ttu-id="b32b8-1370">Compatibilidad con pty/tty considerablemente mejorada.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1370">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="b32b8-1371">Ahora se admiten aplicaciones como TMUX (GH 40)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1371">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="b32b8-1372">Se ha corregido el problema de instalación por el que las cuentas de usuario no siempre se creaban</span><span class="sxs-lookup"><span data-stu-id="b32b8-1372">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="b32b8-1373">Se ha optimizado la estructura de argumentos de línea de comandos que permite una lista de argumentos extremadamente larga.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1373">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="b32b8-1374">(GH 153)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1374">(GH #153)</span></span>
- <span data-ttu-id="b32b8-1375">Ahora puedes usar delete y chmod en archivos read_only de DrvFs</span><span class="sxs-lookup"><span data-stu-id="b32b8-1375">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="b32b8-1376">Se han corregido algunas instancias en las que el terminal se bloquea en la desconexión (GH 43)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1376">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="b32b8-1377">chmod y chown ahora funcionan en dispositivos tty</span><span class="sxs-lookup"><span data-stu-id="b32b8-1377">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="b32b8-1378">Permite la conexión a 0.0.0.0 y :: como localhost (GH 388)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1378">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="b32b8-1379">Sendmsg/recvmsg ahora controlan una longitud de vector de E/S > 1 (GH parcial 376)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1379">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="b32b8-1380">Los usuarios ahora pueden dejar de participar en archivos de hosts generados automáticamente (GH 398)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1380">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="b32b8-1381">La configuración regional de Linux se ajusta automáticamente con la configuración regional de NT durante la instalación (GH 11)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1381">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="b32b8-1382">Se ha agregado el archivo /proc/sys/vm/swappiness (GH 306)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1382">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="b32b8-1383">strace ahora se cierra correctamente</span><span class="sxs-lookup"><span data-stu-id="b32b8-1383">strace now exits correctly</span></span>
- <span data-ttu-id="b32b8-1384">Permite que las canalizaciones se vuelvan a abrir a través de /proc/self/fd (GH 222)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1384">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="b32b8-1385">Oculta directorios en %LOCALAPPDATA%\lxss de DrvFs (GH 270)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1385">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="b32b8-1386">Mejor control de bash.exe ~.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1386">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="b32b8-1387">Ahora se admiten comandos como "bash ~-c ls" (GH 467)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1387">Commands like “bash ~ -c ls” now supported (GH #467)</span></span>
- <span data-ttu-id="b32b8-1388">Ahora, los sockets notifican las lecturas de epoll disponibles durante el cierre (GH 271)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1388">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="b32b8-1389">lxrun /uninstall funciona mejor para eliminar archivos y carpetas</span><span class="sxs-lookup"><span data-stu-id="b32b8-1389">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="b32b8-1390">Se ha corregido ps -f (GH 246)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1390">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="b32b8-1391">Se ha mejorado la compatibilidad con aplicaciones X11, como xEmacs (GH 481)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1391">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="b32b8-1392">Se ha actualizado el tamaño inicial de la pila de subprocesos para que coincida con la configuración predeterminada de Ubuntu, y se notifica el tamaño correctamente a la llamada del sistema get_rlimit (GH 172, 258)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1392">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="b32b8-1393">Se ha mejorado la notificación de nombres de imagen de proceso PICO (por ejemplo, para auditoría)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1393">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="b32b8-1394">Se ha implementado el comando /proc/mountinfo para df</span><span class="sxs-lookup"><span data-stu-id="b32b8-1394">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="b32b8-1395">Se ha corregido el código de error de vínculo simbólico para el nombre secundario .</span><span class="sxs-lookup"><span data-stu-id="b32b8-1395">Fixed symlink error code for child name .</span></span> <span data-ttu-id="b32b8-1396">y ..</span><span class="sxs-lookup"><span data-stu-id="b32b8-1396">and ..</span></span>
- <span data-ttu-id="b32b8-1397">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-1397">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="b32b8-1398">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="b32b8-1398">Syscall Support</span></span>
<span data-ttu-id="b32b8-1399">A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1399">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b32b8-1400">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1400">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="b32b8-1401">Compilación 14352</span><span class="sxs-lookup"><span data-stu-id="b32b8-1401">Build 14352</span></span>
<span data-ttu-id="b32b8-1402">Para obtener información general de Windows sobre la compilación 14352, visita el [blog de Windows](https://aka.ms/wip14352).</span><span class="sxs-lookup"><span data-stu-id="b32b8-1402">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-1403">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-1403">Fixed</span></span>
- <span data-ttu-id="b32b8-1404">Se ha corregido un problema en el que los archivos grandes no se descargaban o se creaban correctamente.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1404">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="b32b8-1405">Esto debe desbloquear npm y otros escenarios (GH 3, GH 313)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1405">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="b32b8-1406">Se han quitado algunas instancias en las que los sockets se bloquean</span><span class="sxs-lookup"><span data-stu-id="b32b8-1406">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="b32b8-1407">Se han corregido algunos errores de ptrace</span><span class="sxs-lookup"><span data-stu-id="b32b8-1407">Corrected some ptrace errors</span></span>
- <span data-ttu-id="b32b8-1408">Se ha corregido un problema con WSL que permite nombres de archivo de más de 255 caracteres</span><span class="sxs-lookup"><span data-stu-id="b32b8-1408">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="b32b8-1409">Se ha mejorado la compatibilidad con caracteres distintos del inglés</span><span class="sxs-lookup"><span data-stu-id="b32b8-1409">Improved support for non-English characters</span></span>
- <span data-ttu-id="b32b8-1410">Agrega datos de zona horaria de Windows actuales y los establece como valores predeterminados</span><span class="sxs-lookup"><span data-stu-id="b32b8-1410">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="b32b8-1411">Id. de dispositivo único para cada punto de montaje (corrección de jre, GH 49)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1411">Unique device id’s for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="b32b8-1412">Corrige el problema con rutas de acceso que contienen "."</span><span class="sxs-lookup"><span data-stu-id="b32b8-1412">Correct issue with paths containing “.”</span></span> <span data-ttu-id="b32b8-1413">y ".."</span><span class="sxs-lookup"><span data-stu-id="b32b8-1413">and “..”</span></span>
- <span data-ttu-id="b32b8-1414">Se ha agregado compatibilidad con Fifo (GH 71)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1414">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="b32b8-1415">Se ha actualizado el formato de resolv.conf para que coincida con el formato nativo de Ubuntu</span><span class="sxs-lookup"><span data-stu-id="b32b8-1415">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="b32b8-1416">Algunas limpiezas de procfs</span><span class="sxs-lookup"><span data-stu-id="b32b8-1416">Some procfs cleanup</span></span>
- <span data-ttu-id="b32b8-1417">Se ha habilitado ping para consolas de administrador (GH 18)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1417">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="b32b8-1418">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="b32b8-1418">Syscall Support</span></span>
<span data-ttu-id="b32b8-1419">A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1419">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b32b8-1420">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1420">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="b32b8-1421">Compilación 14342</span><span class="sxs-lookup"><span data-stu-id="b32b8-1421">Build 14342</span></span>
<span data-ttu-id="b32b8-1422">Para obtener información general de Windows sobre la compilación 14342, visita el [blog de Windows](https://aka.ms/wip14342).</span><span class="sxs-lookup"><span data-stu-id="b32b8-1422">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="b32b8-1423">Puedes encontrar información sobre VolFs y DriveFs en el [blog de WSL](https://blogs.msdn.microsoft.com/wsl).</span><span class="sxs-lookup"><span data-stu-id="b32b8-1423">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="b32b8-1424">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-1424">Fixed</span></span>
- <span data-ttu-id="b32b8-1425">Se ha corregido el problema de instalación cuando el usuario de Windows tenía caracteres Unicode en el nombre de usuario</span><span class="sxs-lookup"><span data-stu-id="b32b8-1425">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="b32b8-1426">La solución alternativa de apt-get update udev en las preguntas más frecuentes se proporciona ahora de forma predeterminada en la primera ejecución</span><span class="sxs-lookup"><span data-stu-id="b32b8-1426">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="b32b8-1427">Vínculos simbólicos habilitados en directorios DriveFs (/mnt/<drive>)</span><span class="sxs-lookup"><span data-stu-id="b32b8-1427">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="b32b8-1428">Los vínculos simbólicos ahora funcionan entre DriveFs y VolFs</span><span class="sxs-lookup"><span data-stu-id="b32b8-1428">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="b32b8-1429">Se ha solucionado el problema de análisis de ruta de acceso de nivel superior:ls .// funcionará ahora como se espera</span><span class="sxs-lookup"><span data-stu-id="b32b8-1429">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="b32b8-1430">La instalación de npm en DriveFs y las opciones -g ahora funcionan</span><span class="sxs-lookup"><span data-stu-id="b32b8-1430">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="b32b8-1431">Se ha corregido un problema que impedía que el servidor PHP se iniciara</span><span class="sxs-lookup"><span data-stu-id="b32b8-1431">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="b32b8-1432">Se han actualizado los valores de entorno predeterminados, como $PATH para que coincidan con Ubuntu nativo</span><span class="sxs-lookup"><span data-stu-id="b32b8-1432">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="b32b8-1433">Se ha agregado una tarea de mantenimiento semanal en Windows para actualizar la caché de paquetes apt</span><span class="sxs-lookup"><span data-stu-id="b32b8-1433">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="b32b8-1434">Se ha corregido un problema con la validación de encabezado de ELF, WSL ahora es compatible con todas las opciones de Melkor</span><span class="sxs-lookup"><span data-stu-id="b32b8-1434">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="b32b8-1435">El shell Zsh funciona</span><span class="sxs-lookup"><span data-stu-id="b32b8-1435">Zsh shell is functional</span></span>
- <span data-ttu-id="b32b8-1436">Ahora se admiten los binarios de Go precompilados</span><span class="sxs-lookup"><span data-stu-id="b32b8-1436">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="b32b8-1437">Indicar bash.exe en la primera ejecución ahora se localiza correctamente</span><span class="sxs-lookup"><span data-stu-id="b32b8-1437">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="b32b8-1438">/proc/meminfo ahora devuelve la información correcta</span><span class="sxs-lookup"><span data-stu-id="b32b8-1438">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="b32b8-1439">Ahora se admiten sockets en VFS</span><span class="sxs-lookup"><span data-stu-id="b32b8-1439">Sockets now supported in VFS</span></span>
- <span data-ttu-id="b32b8-1440">/dev ahora se monta como tempfs</span><span class="sxs-lookup"><span data-stu-id="b32b8-1440">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="b32b8-1441">Ahora se admite Fifo</span><span class="sxs-lookup"><span data-stu-id="b32b8-1441">Fifo now supported</span></span>
- <span data-ttu-id="b32b8-1442">Los sistemas de varios núcleos ahora se muestran correctamente en /proc/cpuinfo</span><span class="sxs-lookup"><span data-stu-id="b32b8-1442">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="b32b8-1443">Mejoras adicionales y mensajes de error que se descargan durante la primera ejecución</span><span class="sxs-lookup"><span data-stu-id="b32b8-1443">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="b32b8-1444">Mejoras de llamadas del sistema y corrección de errores.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1444">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="b32b8-1445">Lista de llamadas del sistema admitidas a continuación.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1445">Supported syscall list below.</span></span>
- <span data-ttu-id="b32b8-1446">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-1446">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="b32b8-1447">Problemas conocidos</span><span class="sxs-lookup"><span data-stu-id="b32b8-1447">Known Issues</span></span>
- <span data-ttu-id="b32b8-1448">No se resuelve ".."</span><span class="sxs-lookup"><span data-stu-id="b32b8-1448">Not resolving ‘..’</span></span> <span data-ttu-id="b32b8-1449">correctamente en DriveFs en algunos casos</span><span class="sxs-lookup"><span data-stu-id="b32b8-1449">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="b32b8-1450">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="b32b8-1450">Syscall Support</span></span>
<span data-ttu-id="b32b8-1451">A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1451">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="b32b8-1452">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1452">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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

## <a name="build-14332"></a><span data-ttu-id="b32b8-1453">Compilación 14332</span><span class="sxs-lookup"><span data-stu-id="b32b8-1453">Build 14332</span></span>

<span data-ttu-id="b32b8-1454">Para obtener información general de Windows sobre la compilación 14332, visita el [blog de Windows](https://aka.ms/wip14332).</span><span class="sxs-lookup"><span data-stu-id="b32b8-1454">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="b32b8-1455">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-1455">Fixed</span></span>
- <span data-ttu-id="b32b8-1456">Mejor generación de resolv.conf, incluida la priorización de entradas de DNS</span><span class="sxs-lookup"><span data-stu-id="b32b8-1456">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="b32b8-1457">Problema con el movimiento de archivos y directorios entre unidades /mnt y no /mnt</span><span class="sxs-lookup"><span data-stu-id="b32b8-1457">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="b32b8-1458">Los archivos tar ahora se pueden crear con vínculos simbólicos</span><span class="sxs-lookup"><span data-stu-id="b32b8-1458">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="b32b8-1459">Se ha agregado el directorio predeterminado /run/lock en la creación de instancias</span><span class="sxs-lookup"><span data-stu-id="b32b8-1459">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="b32b8-1460">Actualiza /dev/null para que devuelva la información de estadísticas correcta</span><span class="sxs-lookup"><span data-stu-id="b32b8-1460">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="b32b8-1461">Errores adicionales al descargar durante la primera ejecución</span><span class="sxs-lookup"><span data-stu-id="b32b8-1461">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="b32b8-1462">Mejoras de llamadas del sistema y corrección de errores.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1462">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="b32b8-1463">Lista de llamadas del sistema admitidas a continuación.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1463">Supported syscall list below.</span></span>
- <span data-ttu-id="b32b8-1464">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-1464">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="b32b8-1465">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="b32b8-1465">Syscall Support</span></span>
<span data-ttu-id="b32b8-1466">A continuación se muestra la nueva llamada del sistema que tiene alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1466">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="b32b8-1467">La llamada del sistema de esta lista se admite en al menos un escenario, pero puede que no se admita todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1467">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="b32b8-1468">Compilación 14328</span><span class="sxs-lookup"><span data-stu-id="b32b8-1468">Build 14328</span></span>

<span data-ttu-id="b32b8-1469">Para obtener información general de Windows sobre la compilación 14332, visita el [blog de Windows](https://aka.ms/wip14328).</span><span class="sxs-lookup"><span data-stu-id="b32b8-1469">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="b32b8-1470">Nuevas características</span><span class="sxs-lookup"><span data-stu-id="b32b8-1470">New Features</span></span>
* <span data-ttu-id="b32b8-1471">Ahora admite usuarios de Linux.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1471">Now support Linux users.</span></span>  <span data-ttu-id="b32b8-1472">Al instalar Bash en Ubuntu en Windows, se solicitará la creación de un usuario de Linux.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1472">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="b32b8-1473">Para más información, visita https://aka.ms/wslusers.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1473">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="b32b8-1474">El nombre de host ahora se establece en el nombre del equipo de Windows, ya no más en @localhost</span><span class="sxs-lookup"><span data-stu-id="b32b8-1474">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="b32b8-1475">Para más información sobre la compilación 14328, visita: https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="b32b8-1475">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="b32b8-1476">Fijo</span><span class="sxs-lookup"><span data-stu-id="b32b8-1476">Fixed</span></span>
* <span data-ttu-id="b32b8-1477">Mejoras de vínculos simbólicos para archivos que no son /mnt/<drive></span><span class="sxs-lookup"><span data-stu-id="b32b8-1477">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="b32b8-1478">La instalación de npm ahora funciona</span><span class="sxs-lookup"><span data-stu-id="b32b8-1478">npm install now works</span></span>
    * <span data-ttu-id="b32b8-1479">jdk / jre ahora se puede instalar con las instrucciones que se encuentran [aquí](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span><span class="sxs-lookup"><span data-stu-id="b32b8-1479">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="b32b8-1480">Problema conocido: los vínculos simbólicos no funcionan para los montajes de Windows.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1480">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="b32b8-1481">La funcionalidad estará disponible en una compilación posterior</span><span class="sxs-lookup"><span data-stu-id="b32b8-1481">Functionality will be available in a later build</span></span>
* <span data-ttu-id="b32b8-1482">top y htop ahora se muestran</span><span class="sxs-lookup"><span data-stu-id="b32b8-1482">top and htop now display</span></span>
* <span data-ttu-id="b32b8-1483">Mensajes de error adicionales para algunos errores de instalación</span><span class="sxs-lookup"><span data-stu-id="b32b8-1483">Additional error messages for some install failures</span></span>
* <span data-ttu-id="b32b8-1484">Mejoras de llamadas del sistema y corrección de errores.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1484">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="b32b8-1485">Lista de llamadas del sistema admitidas a continuación.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1485">Supported syscall list below.</span></span>
* <span data-ttu-id="b32b8-1486">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="b32b8-1486">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="b32b8-1487">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="b32b8-1487">Syscall Support</span></span>
<span data-ttu-id="b32b8-1488">A continuación hay una lista de llamadas del sistema que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1488">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="b32b8-1489">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="b32b8-1489">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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
