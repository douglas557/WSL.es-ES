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
ms.openlocfilehash: b92c20bad50d0c58da05bb0c8f26a69d4c0b2970
ms.sourcegitcommit: 050f6095e92469b903db8ddf9356df5b22b21804
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/03/2019
ms.locfileid: "71910304"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="18a43-105">Notas de la versión del subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="18a43-105">Release Notes for Windows Subsystem for Linux</span></span>

## <a name="build-18995"></a><span data-ttu-id="18a43-106">Compilación 18995</span><span class="sxs-lookup"><span data-stu-id="18a43-106">Build 18995</span></span>
<span data-ttu-id="18a43-107">Para obtener información general de Windows sobre la compilación 18995, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/).</span><span class="sxs-lookup"><span data-stu-id="18a43-107">For general Windows information on build 18995 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/).</span></span>

* <span data-ttu-id="18a43-108">[WSL2] Corrección de un problema que provocaba que los montajes DrvFs dejaran de funcionar después de que se interrumpiera una operación (por ejemplo, Ctrl-C) [GH 4377]</span><span class="sxs-lookup"><span data-stu-id="18a43-108">[WSL2] Fix an issue where DrvFs mounts stopped working after an operation was interrupted (e.g. ctrl-c) [GH 4377]</span></span>
* <span data-ttu-id="18a43-109">[WSL2] Corrección del control de mensajes hvsocket muy grandes [GH 4105]</span><span class="sxs-lookup"><span data-stu-id="18a43-109">[WSL2] Fix handling of very large hvsocket messages [GH 4105]</span></span>
* <span data-ttu-id="18a43-110">[WSL2] Corrección de un problema con la interoperabilidad cuando stdin es un archivo [GH 4475]</span><span class="sxs-lookup"><span data-stu-id="18a43-110">[WSL2] Fix issue with interop when stdin is a file [GH 4475]</span></span>
* <span data-ttu-id="18a43-111">[WSL2] Corrección de un bloqueo de servicio cuando se encontraba un estado de red inesperado [GH 4474]</span><span class="sxs-lookup"><span data-stu-id="18a43-111">[WSL2] Fix service crash when unexpected network state is encountered [GH 4474]</span></span>
* <span data-ttu-id="18a43-112">[WSL2] Consulta del nombre de distribución desde el servidor de interoperabilidad si el proceso actual no tiene la variable de entorno</span><span class="sxs-lookup"><span data-stu-id="18a43-112">[WSL2] Query the distro name from the interop server if the current process does not have the environment variable</span></span>
* <span data-ttu-id="18a43-113">[WSL2] Corrección de un problema con la interoperabilidad cuando stdin es un archivo</span><span class="sxs-lookup"><span data-stu-id="18a43-113">[WSL2] Fix issue with interop whe stdin is a file</span></span>
* <span data-ttu-id="18a43-114">[WSL2] Actualización de la versión del kernel de Linux a 4.19.72</span><span class="sxs-lookup"><span data-stu-id="18a43-114">[WSL2] Update Linux kernel version to 4.19.72</span></span>
* <span data-ttu-id="18a43-115">[WSL2] Agrega la capacidad de especificar parámetros adicionales de línea de comandos de kernel mediante .wslconfig</span><span class="sxs-lookup"><span data-stu-id="18a43-115">[WSL2] Add ability to specify additional kernel command line parameters via .wslconfig</span></span>
```
[wsl2]
kernelCommandLine = <string> # Additional kernel command line arguments

```

## <a name="build-18990"></a><span data-ttu-id="18a43-116">Compilación 18990</span><span class="sxs-lookup"><span data-stu-id="18a43-116">Build 18990</span></span>
<span data-ttu-id="18a43-117">Para obtener información general de Windows sobre la compilación 18990, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/).</span><span class="sxs-lookup"><span data-stu-id="18a43-117">For general Windows information on build 18990 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/).</span></span>

* <span data-ttu-id="18a43-118">Mejorar el rendimiento de los listados de directorios en \\\\wsl$</span><span class="sxs-lookup"><span data-stu-id="18a43-118">Improve the performance for directory listings in \\\\wsl$</span></span>
* <span data-ttu-id="18a43-119">[WSL2] Insertar entropía de arranque adicional [GH 4416]</span><span class="sxs-lookup"><span data-stu-id="18a43-119">[WSL2] Inject additional boot entropy [GH 4416]</span></span>
* <span data-ttu-id="18a43-120">[WSL2] Corrección para la interoperabilidad de Windows al usar su/sudo [GH 4465]</span><span class="sxs-lookup"><span data-stu-id="18a43-120">[WSL2] Fix for Windows interop when using su / sudo [GH 4465]</span></span>


## <a name="build-18980"></a><span data-ttu-id="18a43-121">Compilación 18980</span><span class="sxs-lookup"><span data-stu-id="18a43-121">Build 18980</span></span>
<span data-ttu-id="18a43-122">Para obtener información general de Windows sobre la compilación 18980, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).</span><span class="sxs-lookup"><span data-stu-id="18a43-122">For general Windows information on build 18980 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).</span></span>

* <span data-ttu-id="18a43-123">Corrige la lectura de los vínculos simbólicos que deniegan FILE_READ_DATA.</span><span class="sxs-lookup"><span data-stu-id="18a43-123">Fix reading symlinks that deny FILE_READ_DATA.</span></span> <span data-ttu-id="18a43-124">Esto incluye todos los vínculos simbólicos que crea Windows para la compatibilidad con versiones anteriores, como "C:\Document and Settings" y un conjunto de vínculos simbólicos en el directorio de perfil del usuario.</span><span class="sxs-lookup"><span data-stu-id="18a43-124">This includes all the symlinks Windows creates for backwards compatibility such as "C:\Document and Settings" and a bunch of symlinks in the user profile directory</span></span>
* <span data-ttu-id="18a43-125">Hace que el estado inesperado del sistema de archivos no sea irrecuperable [GH 4334, 4305]</span><span class="sxs-lookup"><span data-stu-id="18a43-125">Make unexpected filesystem state non-fatal [GH 4334, 4305]</span></span>
* <span data-ttu-id="18a43-126">[WSL2] Agrega compatibilidad para arm64 si tu CPU/firmware admite virtualización</span><span class="sxs-lookup"><span data-stu-id="18a43-126">[WSL2] Add support for arm64 if your CPU / firmware supports virtualization</span></span>
* <span data-ttu-id="18a43-127">[WSL2] Permite a los usuarios sin privilegios ver el registro del kernel</span><span class="sxs-lookup"><span data-stu-id="18a43-127">[WSL2] Allow unprivileged users to view kernel log</span></span>
* <span data-ttu-id="18a43-128">[WSL2] Corrige la retransmisión de salida cuando se han cerrado los sockets stdout/stderr [GH 4375]</span><span class="sxs-lookup"><span data-stu-id="18a43-128">[WSL2] Fix output relay when stdout / stderr sockets have been closed [GH 4375]</span></span>
* <span data-ttu-id="18a43-129">[WSL2] Compatibilidad con la batería y el adaptador de AC</span><span class="sxs-lookup"><span data-stu-id="18a43-129">[WSL2] Support battery and AC adapter passthrough</span></span>
* <span data-ttu-id="18a43-130">[WSL2] Actualización del kernel de Linux a 4.19.67</span><span class="sxs-lookup"><span data-stu-id="18a43-130">[WSL2] Update Linux kernel to 4.19.67</span></span>
* <span data-ttu-id="18a43-131">Adición de la capacidad de establecer el nombre de usuario predeterminado en /etc/WSL.conf:</span><span class="sxs-lookup"><span data-stu-id="18a43-131">Add the ability to set default username in /etc/wsl.conf:</span></span>
```
[user]
default=<string>
```

## <a name="build-18975"></a><span data-ttu-id="18a43-132">Compilación 18975</span><span class="sxs-lookup"><span data-stu-id="18a43-132">Build 18975</span></span>
<span data-ttu-id="18a43-133">Para obtener información general de Windows sobre la compilación 18975,visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).</span><span class="sxs-lookup"><span data-stu-id="18a43-133">For general Windows information on build 18975 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).</span></span>

* <span data-ttu-id="18a43-134">[WSL2] Se han corregido varios problemas de confiabilidad de localhost [GH 4340]</span><span class="sxs-lookup"><span data-stu-id="18a43-134">[WSL2] Fixed a number of localhost reliability issues [GH 4340]</span></span>

## <a name="build-18970"></a><span data-ttu-id="18a43-135">Compilación 18970</span><span class="sxs-lookup"><span data-stu-id="18a43-135">Build 18970</span></span>
<span data-ttu-id="18a43-136">Para obtener información general de Windows sobre la compilación 18970, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).</span><span class="sxs-lookup"><span data-stu-id="18a43-136">For general Windows information on build 18970 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).</span></span>

* <span data-ttu-id="18a43-137">[WSL2] Sincronización de la hora con la hora del host cuando el sistema se reanuda desde el estado de suspensión [GH 4245]</span><span class="sxs-lookup"><span data-stu-id="18a43-137">[WSL2] Sync time with host time when system resumes from sleep state [GH 4245]</span></span>
* <span data-ttu-id="18a43-138">[WSL2] Crea vínculos simbólicos de NT en volúmenes de Windows cuando sea posible.</span><span class="sxs-lookup"><span data-stu-id="18a43-138">[WSL2] Create NT symlinks on the Windows volumes when possible.</span></span>
* <span data-ttu-id="18a43-139">[WSL2] Crea distribuciones en los espacios de nombres UTS, IPC, PID y Mount.</span><span class="sxs-lookup"><span data-stu-id="18a43-139">[WSL2] Create distros in UTS, IPC, PID, and Mount namespaces.</span></span>
* <span data-ttu-id="18a43-140">[WSL2] Corrección de retransmisión de puerto localhost cuando el servidor se enlaza a localhost directamente [GH 4353]</span><span class="sxs-lookup"><span data-stu-id="18a43-140">[WSL2] Fix localhost port relay when server binds to localhost directly [GH 4353]</span></span>
* <span data-ttu-id="18a43-141">[WSL2] Corrección de interoperabilidad cuando se redirige la salida [GH 4337]</span><span class="sxs-lookup"><span data-stu-id="18a43-141">[WSL2] Fix interop when output is redirected [GH 4337]</span></span>
* <span data-ttu-id="18a43-142">[WSL2] Compatibilidad con la traducción de vínculos simbólicos de NT absolutos.</span><span class="sxs-lookup"><span data-stu-id="18a43-142">[WSL2] Support translating absolute NT symlinks.</span></span>
* <span data-ttu-id="18a43-143">[WSL2] Actualización del kernel a 4.19.59</span><span class="sxs-lookup"><span data-stu-id="18a43-143">[WSL2] Update kernel to 4.19.59</span></span>
* <span data-ttu-id="18a43-144">[WSL2] Definición correcta de la máscara de subred para eth0.</span><span class="sxs-lookup"><span data-stu-id="18a43-144">[WSL2] Properly set subnet mask for eth0.</span></span>
* <span data-ttu-id="18a43-145">[WSL2] Cambio de la lógica para interrumpir el bucle de trabajo de la consola cuando se señale el evento de salida.</span><span class="sxs-lookup"><span data-stu-id="18a43-145">[WSL2] Change logic to break out of console worker loop when exit event is signaled.</span></span>
* <span data-ttu-id="18a43-146">[WSL2] Expulsión del VHD de distribución cuando la  distribución no está en ejecución.</span><span class="sxs-lookup"><span data-stu-id="18a43-146">[WSL2] Eject distribution vhd when the distro is not running.</span></span>
* <span data-ttu-id="18a43-147">[WSL2] Corrección de la biblioteca de análisis de configuración para controlar correctamente los valores vacíos.</span><span class="sxs-lookup"><span data-stu-id="18a43-147">[WSL2] Fix config parsing library to correctly handle empty values.</span></span>
* <span data-ttu-id="18a43-148">[WSL2] Compatibilidad con el escritorio de Docker al crear montajes de distribución cruzados.</span><span class="sxs-lookup"><span data-stu-id="18a43-148">[WSL2] Support Docker Desktop by creating cross distro mounts.</span></span> <span data-ttu-id="18a43-149">Un distribución puede participar en este comportamiento si se agrega la siguiente línea al archivo /etc/wsl.conf:</span><span class="sxs-lookup"><span data-stu-id="18a43-149">A distro can opt-in to this behavior by adding the following line to the /etc/wsl.conf file:</span></span>
```
[automount]
crossDistro = true
```

## <a name="build-18945"></a><span data-ttu-id="18a43-150">Compilación 18945</span><span class="sxs-lookup"><span data-stu-id="18a43-150">Build 18945</span></span>
<span data-ttu-id="18a43-151">Para obtener información general de Windows sobre la compilación 18945, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span><span class="sxs-lookup"><span data-stu-id="18a43-151">For general Windows information on build 18945 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-152">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-152">WSL</span></span>
* <span data-ttu-id="18a43-153">[WSL2] Permite que se acceda a los sockets TCP de escucha en WSL2 desde el host mediante localhost:port</span><span class="sxs-lookup"><span data-stu-id="18a43-153">[WSL2] Allow listening tcp sockets in WSL2 to be accessible from the host by using localhost:port</span></span>
* <span data-ttu-id="18a43-154">[WSL2] Correcciones de errores de instalación/conversión y diagnósticos adicionales para un seguimiento de los problemas futuros [GH 4105]</span><span class="sxs-lookup"><span data-stu-id="18a43-154">[WSL2] Fixes for install / conversion failures and additional diagnostics to track down future issues [GH 4105]</span></span> 
* <span data-ttu-id="18a43-155">[WSL2] Mejora la capacidad de diagnóstico de los problemas de red de WSL2</span><span class="sxs-lookup"><span data-stu-id="18a43-155">[WSL2] Improve diagnosability of WSL2 network issues</span></span>
* <span data-ttu-id="18a43-156">[WSL2] Actualización de la versión del kernel a 4.19.55</span><span class="sxs-lookup"><span data-stu-id="18a43-156">[WSL2] Update kernel version to 4.19.55</span></span>
* <span data-ttu-id="18a43-157">[WSL2] Actualización del kernel con las opciones de configuración necesarias para Docker [GH 4165]</span><span class="sxs-lookup"><span data-stu-id="18a43-157">[WSL2] Update kernel with config options required for docker [GH 4165]</span></span>
* <span data-ttu-id="18a43-158">[WSL2] Aumento del número de CPU asignadas a la VM de utilidad ligera para que sea el mismo que el host (se ha limitado previamente a 8 por CONFIG_NR_CPUS en la configuración del kernel) [GH 4137]</span><span class="sxs-lookup"><span data-stu-id="18a43-158">[WSL2] Increase the number of CPUs assigned to the lightweight utility VM to be the same as the host (was previously capped at 8 by CONFIG_NR_CPUS in the kernel config) [GH 4137]</span></span>
* <span data-ttu-id="18a43-159">[WSL2] Creación de un archivo de intercambio para la VM ligera WSL2</span><span class="sxs-lookup"><span data-stu-id="18a43-159">[WSL2] Create a swap file for the WSL2 lightweight VM</span></span>
* <span data-ttu-id="18a43-160">[WSL2] Permite que los montajes de usuarios sean visibles a través de la distribución \\\\wsl$\\ (por ejemplo, sshfs) [GH 4172]</span><span class="sxs-lookup"><span data-stu-id="18a43-160">[WSL2] Allow user mounts to be visible via \\\\wsl$\\distro (for example sshfs) [GH 4172]</span></span>
* <span data-ttu-id="18a43-161">[WSL2] Mejora el rendimiento del sistema de archivos 9p</span><span class="sxs-lookup"><span data-stu-id="18a43-161">[WSL2] Improve 9p filesystem performance</span></span>
* <span data-ttu-id="18a43-162">[WSL2] Asegura que la ACL de VHD no crezca sin límite [GH 4126]</span><span class="sxs-lookup"><span data-stu-id="18a43-162">[WSL2] Ensure vhd ACL does not grow unbounded [GH 4126]</span></span>
* <span data-ttu-id="18a43-163">[WSL2] Actualización de la configuración de kernel para admitir squashfs y xt_conntrack [GH 4107, 4123]</span><span class="sxs-lookup"><span data-stu-id="18a43-163">[WSL2] Update kernel config to support squashfs and xt_conntrack [GH 4107, 4123]</span></span>
* <span data-ttu-id="18a43-164">[WSL2] Corrección para la opción interop.enabled /etc/wsl.conf [GH 4140]</span><span class="sxs-lookup"><span data-stu-id="18a43-164">[WSL2] Fix for interop.enabled /etc/wsl.conf option [GH 4140]</span></span>
* <span data-ttu-id="18a43-165">[WSL2] Devuelve ENOTSUP si el sistema de archivos no es compatible con EA</span><span class="sxs-lookup"><span data-stu-id="18a43-165">[WSL2] Return ENOTSUP if the file system does not support EAs</span></span>
* <span data-ttu-id="18a43-166">[WSL2] Corrección de CopyFile colgado con \\\\wsl$</span><span class="sxs-lookup"><span data-stu-id="18a43-166">[WSL2] Fix CopyFile hang with \\\\wsl$</span></span>
* <span data-ttu-id="18a43-167">Cambio del valor predeterminado de umask a 0022 y adición de la configuración de filesystem.umask a /etc/wsl.conf</span><span class="sxs-lookup"><span data-stu-id="18a43-167">Switch default umask to 0022 and add filesystem.umask setting to /etc/wsl.conf</span></span>
* <span data-ttu-id="18a43-168">Corrección de wslpath para resolver correctamente los vínculos simbólicos, esto se retomó en 19h1 [GH 4078]</span><span class="sxs-lookup"><span data-stu-id="18a43-168">Fix wslpath to properly resolve symlinks, this was regressed in 19h1 [GH 4078]</span></span>
* <span data-ttu-id="18a43-169">Introducción del archivo %UserProfile%\\.wslconfig para ajustar la configuración de WSL2</span><span class="sxs-lookup"><span data-stu-id="18a43-169">Introduce %UserProfile%\\.wslconfig file for tweaking WSL2 settings</span></span>
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

## <a name="build-18917"></a><span data-ttu-id="18a43-170">Compilación 18917</span><span class="sxs-lookup"><span data-stu-id="18a43-170">Build 18917</span></span>
<span data-ttu-id="18a43-171">Para obtener información general de Windows sobre la compilación 18917, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span><span class="sxs-lookup"><span data-stu-id="18a43-171">For general Windows information on build 18917 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-172">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-172">WSL</span></span>
* <span data-ttu-id="18a43-173">¡WSL 2 ya está disponible!</span><span class="sxs-lookup"><span data-stu-id="18a43-173">WSL 2 is now available!</span></span> <span data-ttu-id="18a43-174">Consulta el [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) para más detalles.</span><span class="sxs-lookup"><span data-stu-id="18a43-174">Please see [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) for more details.</span></span>
* <span data-ttu-id="18a43-175">Corrección de una regresión en la que iniciar procesos de Windows a través de vínculos simbólicos no funcionaba correctamente [GH 3999]</span><span class="sxs-lookup"><span data-stu-id="18a43-175">Fix a regression where launching Windows processes via symlinks did not work correctly [GH 3999]</span></span>
* <span data-ttu-id="18a43-176">Agrega las opciones wsl.exe --list --verbose, wsl.exe --list --quiet y wsl.exe --import --version a wsl.exe</span><span class="sxs-lookup"><span data-stu-id="18a43-176">Add wsl.exe --list --verbose, wsl.exe --list --quiet, and wsl.exe --import --version options to wsl.exe</span></span>
* <span data-ttu-id="18a43-177">Agrega la opción wsl.exe --shutdown</span><span class="sxs-lookup"><span data-stu-id="18a43-177">Add wsl.exe --shutdown option</span></span>
* <span data-ttu-id="18a43-178">Plan 9: Permite abrir un directorio para escribir en él correctamente</span><span class="sxs-lookup"><span data-stu-id="18a43-178">Plan 9: Allow opening a directory for write to succeed</span></span>

## <a name="build-18890"></a><span data-ttu-id="18a43-179">Compilación 18890</span><span class="sxs-lookup"><span data-stu-id="18a43-179">Build 18890</span></span>
<span data-ttu-id="18a43-180">Para obtener información general de Windows sobre la compilación 18890, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span><span class="sxs-lookup"><span data-stu-id="18a43-180">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-181">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-181">WSL</span></span>
* <span data-ttu-id="18a43-182">Pérdida de socket sin bloqueo [GH 2913]</span><span class="sxs-lookup"><span data-stu-id="18a43-182">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="18a43-183">La entrada de EOF en el terminal puede bloquear lecturas posteriores [GH 3421]</span><span class="sxs-lookup"><span data-stu-id="18a43-183">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="18a43-184">Actualización del encabezado de resolv.conf para hacer referencia a wsl.conf [descrito en GH 3928]</span><span class="sxs-lookup"><span data-stu-id="18a43-184">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="18a43-185">Interbloqueo en código de eliminación de epoll [GH 3922]</span><span class="sxs-lookup"><span data-stu-id="18a43-185">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="18a43-186">Control de espacios de los argumentos en -import y -export [GH 3932]</span><span class="sxs-lookup"><span data-stu-id="18a43-186">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="18a43-187">La extensión de los archivos de mmap no funciona correctamente [GH 3939]</span><span class="sxs-lookup"><span data-stu-id="18a43-187">Extending mmap’d files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="18a43-188">Corrección del problema de funcionamiento del acceso a ARM64 \\\\wsl$</span><span class="sxs-lookup"><span data-stu-id="18a43-188">Fix issue with ARM64 \\\\wsl$ access not working properly</span></span>
* <span data-ttu-id="18a43-189">Agrega el mejor icono predeterminado para wsl.exe</span><span class="sxs-lookup"><span data-stu-id="18a43-189">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="18a43-190">Compilación 18342</span><span class="sxs-lookup"><span data-stu-id="18a43-190">Build 18342</span></span>
<span data-ttu-id="18a43-191">Para obtener información general de Windows sobre la compilación 18342, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span><span class="sxs-lookup"><span data-stu-id="18a43-191">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-192">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-192">WSL</span></span>
* <span data-ttu-id="18a43-193">Hemos agregado la posibilidad de que los usuarios accedan a los archivos de Linux en una distribución de WSL desde Windows.</span><span class="sxs-lookup"><span data-stu-id="18a43-193">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="18a43-194">Se puede acceder a estos archivos a través de la línea de comandos; también las aplicaciones de Windows, como el explorador de archivos, VSCode, etc., pueden interactuar con estos archivos.</span><span class="sxs-lookup"><span data-stu-id="18a43-194">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="18a43-195">Para acceder a los archivos, ve a \\\\wsl$\\<nombre_de_distribución>, o consulta la lista de las distribuciones en ejecución en \\\\wsl$</span><span class="sxs-lookup"><span data-stu-id="18a43-195">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="18a43-196">Agrega etiquetas de información de CPU adicionales y corregir valores de Cpus_allowed[_list] [GH 2234]</span><span class="sxs-lookup"><span data-stu-id="18a43-196">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="18a43-197">Compatibilidad con exec desde un subproceso no líder [GH 3800]</span><span class="sxs-lookup"><span data-stu-id="18a43-197">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="18a43-198">Trata errores de actualización de la configuración como no irrecuperables [GH 3785]</span><span class="sxs-lookup"><span data-stu-id="18a43-198">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="18a43-199">Actualización de binfmt para administrar correctamente los desplazamientos [GH 3768]</span><span class="sxs-lookup"><span data-stu-id="18a43-199">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="18a43-200">Habilita la asignación de unidades de red para Plan 9 [GH 3854]</span><span class="sxs-lookup"><span data-stu-id="18a43-200">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="18a43-201">Compatibilidad con traducción de rutas de acceso Windows -> Linux y Linux -> Windows para montajes de enlace</span><span class="sxs-lookup"><span data-stu-id="18a43-201">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="18a43-202">Crea secciones de solo lectura para asignaciones en archivos abiertos de solo lectura</span><span class="sxs-lookup"><span data-stu-id="18a43-202">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="18a43-203">Compilación 18334</span><span class="sxs-lookup"><span data-stu-id="18a43-203">Build 18334</span></span>
<span data-ttu-id="18a43-204">Para obtener información general de Windows sobre la compilación 18334, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span><span class="sxs-lookup"><span data-stu-id="18a43-204">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-205">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-205">WSL</span></span>
* <span data-ttu-id="18a43-206">Rediseña el modo en que se asigna la zona horaria de Windows a una zona horaria de Linux [GH 3747]</span><span class="sxs-lookup"><span data-stu-id="18a43-206">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="18a43-207">Corrección de pérdidas de memoria y adición de nuevas funciones de traducción de cadenas [GH 3746]</span><span class="sxs-lookup"><span data-stu-id="18a43-207">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="18a43-208">SIGCONT en un grupo de subprocesos sin subprocesos es no-op [alvent 3741]</span><span class="sxs-lookup"><span data-stu-id="18a43-208">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="18a43-209">Muestra correctamente los descriptores de archivo de socket y epoll en /proc/self/fd</span><span class="sxs-lookup"><span data-stu-id="18a43-209">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="18a43-210">Compilación 18305</span><span class="sxs-lookup"><span data-stu-id="18a43-210">Build 18305</span></span>
<span data-ttu-id="18a43-211">Para obtener información general de Windows sobre la compilación 18305, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span><span class="sxs-lookup"><span data-stu-id="18a43-211">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-212">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-212">WSL</span></span>
* <span data-ttu-id="18a43-213">pthreads pierden acceso a los archivos cuando sale el subproceso principal [GH 3589]</span><span class="sxs-lookup"><span data-stu-id="18a43-213">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="18a43-214">TIOCSCTTY debe omitir el parámetro "force", a menos que sea necesario [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="18a43-214">TIOCSCTTY should ignore the “force” parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="18a43-215">Mejoras en la línea de comandos de wsl.exe y adición de la funcionalidad de importación y exportación.</span><span class="sxs-lookup"><span data-stu-id="18a43-215">wsl.exe command line improvements and addition of import / export functionality.</span></span>
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

## <a name="build-18277"></a><span data-ttu-id="18a43-216">Compilación 18277</span><span class="sxs-lookup"><span data-stu-id="18a43-216">Build 18277</span></span>
<span data-ttu-id="18a43-217">Para obtener información general de Windows sobre la compilación 18277, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span><span class="sxs-lookup"><span data-stu-id="18a43-217">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-218">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-218">WSL</span></span>
* <span data-ttu-id="18a43-219">Corrección del error "Interfaz no compatible" que se presentó en la compilación 18272 [GH 3645]</span><span class="sxs-lookup"><span data-stu-id="18a43-219">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="18a43-220">Omite la marca MNT_FORCE para la llamada del sistema umount [GH 3605]</span><span class="sxs-lookup"><span data-stu-id="18a43-220">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="18a43-221">Cambia la interoperabilidad de WSL para usar la API de CreatePseudoConsole oficial</span><span class="sxs-lookup"><span data-stu-id="18a43-221">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="18a43-222">No mantiene ningún valor de tiempo de espera cuando se reinicia FUTEX_WAIT</span><span class="sxs-lookup"><span data-stu-id="18a43-222">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="18a43-223">Compilación 18272</span><span class="sxs-lookup"><span data-stu-id="18a43-223">Build 18272</span></span>
<span data-ttu-id="18a43-224">Para obtener información general de Windows sobre la compilación 18272, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span><span class="sxs-lookup"><span data-stu-id="18a43-224">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-225">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-225">WSL</span></span>
* <span data-ttu-id="18a43-226">**ADVERTENCIA:** Hay un problema en esta compilación que hace que WSL sea inoperable.</span><span class="sxs-lookup"><span data-stu-id="18a43-226">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="18a43-227">Al intentar iniciar la distribución, verás el error "Interfaz no compatible".</span><span class="sxs-lookup"><span data-stu-id="18a43-227">When trying to launch your distribution you will see a “No such interface supported” error.</span></span> <span data-ttu-id="18a43-228">El problema se ha solucionado y estará en la compilación del modo anticipado de Insider de la próxima semana.</span><span class="sxs-lookup"><span data-stu-id="18a43-228">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="18a43-229">Si has instalado esta compilación, puedes revertir a la compilación anterior de Windows mediante "Volver a la versión anterior de Windows 10" en Configuración-> Actualización y seguridad > Recuperación.</span><span class="sxs-lookup"><span data-stu-id="18a43-229">If you've installed this build you can roll back to the previous Windows build using “Go back to the previous version of Windows 10” in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="18a43-230">Compilación 18267</span><span class="sxs-lookup"><span data-stu-id="18a43-230">Build 18267</span></span>
<span data-ttu-id="18a43-231">Para obtener información general de Windows sobre la compilación 18267, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span><span class="sxs-lookup"><span data-stu-id="18a43-231">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-232">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-232">WSL</span></span>
* <span data-ttu-id="18a43-233">Corrección del problema por el que un proceso inerte no podía recogerse y permanecía de manera indefinida.</span><span class="sxs-lookup"><span data-stu-id="18a43-233">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="18a43-234">WslRegisterDistribution se bloquea si el mensaje de error supera la longitud máxima [GH 3592]</span><span class="sxs-lookup"><span data-stu-id="18a43-234">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="18a43-235">Permite que fsync se complete correctamente para los archivos de solo lectura en DrvFs [GH 3556]</span><span class="sxs-lookup"><span data-stu-id="18a43-235">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="18a43-236">Asegúrate de que los directorios /bin y /sbin existan antes de crear los vínculos simbólicos en ellos [GH 3584]</span><span class="sxs-lookup"><span data-stu-id="18a43-236">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="18a43-237">Se agregó un mecanismo de tiempo de espera de finalización de instancias para las instancias de WSL.</span><span class="sxs-lookup"><span data-stu-id="18a43-237">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="18a43-238">El tiempo de espera está establecido actualmente en 15 segundos, por lo que la instancia finalizará 15 segundos después de que termine el último proceso de WSL.</span><span class="sxs-lookup"><span data-stu-id="18a43-238">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="18a43-239">Para finalizar una distribución de inmediato, usa:</span><span class="sxs-lookup"><span data-stu-id="18a43-239">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="18a43-240">Compilación 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="18a43-240">Build 17763 (1809)</span></span>
<span data-ttu-id="18a43-241">Para obtener información general de Windows sobre la compilación 17763, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span><span class="sxs-lookup"><span data-stu-id="18a43-241">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-242">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-242">WSL</span></span>
* <span data-ttu-id="18a43-243">Comprobación de permisos de la llamada del sistema setpriority demasiado estricta para cambiar la misma prioridad de subprocesos [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="18a43-243">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="18a43-244">Asegúrate de que se use el tiempo de interrupción no sesgado para el tiempo de arranque para evitar que se devuelvan valores negativos para clock_gettime (CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="18a43-244">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="18a43-245">Controla los vínculos simbólicos en el intérprete binfmt de WSL [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="18a43-245">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="18a43-246">Mejor control de la limpieza de descriptores de archivo del líder del grupo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="18a43-246">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="18a43-247">Cambia WSL para usar KeQueryInterruptTimePrecise en lugar de KeQueryPerformanceCounter para evitar el desbordamiento [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="18a43-247">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="18a43-248">Ptrace attach puede producir un valor de devolución incorrecto de las llamadas del sistema [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="18a43-248">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="18a43-249">Corrección de varios problemas relacionados con AF_UNIX [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="18a43-249">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="18a43-250">Corrección del problema que podía provocar un error de interoperabilidad de WSL si el directorio de trabajo actual tiene menos de 5 caracteres de longitud [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="18a43-250">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="18a43-251">Evita las conexiones de bucle invertido con error con retraso de un segundo a puertos no existentes [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="18a43-251">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="18a43-252">Agrega el archivo de código auxiliar /proc/sys/fs/file-max [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="18a43-252">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="18a43-253">Información más precisa sobre el ámbito IPV6.</span><span class="sxs-lookup"><span data-stu-id="18a43-253">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="18a43-254">Compatibilidad con PR_SET_PTRACER [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="18a43-254">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="18a43-255">El sistema de archivos de canalización borra accidentalmente el evento epoll desencadenado por el borde [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="18a43-255">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="18a43-256">El ejecutable de Win32 iniciado mediante el vínculo simbólico de NTFS no respeta el nombre del vínculo simbólico [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="18a43-256">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="18a43-257">Compatibilidad mejorada con zombie [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="18a43-257">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="18a43-258">Agrega entradas de wsl.conf para controlar el comportamiento de interoperabilidad de Windows [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="18a43-258">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="18a43-259">La corrección para getsockname no siempre devuelve el tipo de familia de socket de UNIX [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="18a43-259">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="18a43-260">Agrega compatibilidad para TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="18a43-260">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="18a43-261">Los sockets sin bloqueo en el proceso de conexión deben devolver EAGAIN para los intentos de escritura [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="18a43-261">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="18a43-262">Compatibilidad con la interoperabilidad en VHD montados [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="18a43-262">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="18a43-263">Corrección del problema de comprobación de permisos en la carpeta raíz [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="18a43-263">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="18a43-264">Compatibilidad limitada para los ioctl de teclado TTY KDGKBTYPE, KDGKBMODE y KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="18a43-264">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="18a43-265">Las aplicaciones de interfaz de usuario de Windows deben ejecutarse incluso cuando se inician en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="18a43-265">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="18a43-266">Agrega la opción wsl -u o --user [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="18a43-266">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="18a43-267">Corrección de problemas de inicio de WSL cuando el inicio rápido está habilitado [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="18a43-267">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="18a43-268">Los sockets de UNIX deben conservar las credenciales del mismo nivel desconectadas [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="18a43-268">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="18a43-269">Sockets de UNIX sin bloqueo con error de manera indefinida con EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="18a43-269">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="18a43-270">case=off es el nuevo tipo de montaje drvfs predeterminado [GH 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="18a43-270">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="18a43-271">Consulta el [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) para más información.</span><span class="sxs-lookup"><span data-stu-id="18a43-271">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="18a43-272">Agrega wslconfig/terminate para detener las distribuciones en ejecución.</span><span class="sxs-lookup"><span data-stu-id="18a43-272">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="18a43-273">Corrección del problema con las entradas del menú contextual del shell de WSL que no controlan correctamente las rutas de acceso con espacios.</span><span class="sxs-lookup"><span data-stu-id="18a43-273">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="18a43-274">Expone la distinción de mayúsculas y minúsculas por directorio como atributo extendido</span><span class="sxs-lookup"><span data-stu-id="18a43-274">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="18a43-275">ARM64: Emula las operaciones de mantenimiento de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="18a43-275">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="18a43-276">Resuelve un [problema de dotnet](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="18a43-276">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="18a43-277">DrvFs: solo caracteres con escape eliminado en el intervalo privado que corresponden a un carácter de escape.</span><span class="sxs-lookup"><span data-stu-id="18a43-277">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="18a43-278">Corrección error de desviación por uno en la validación de longitud del intérprete del analizador ELF [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="18a43-278">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="18a43-279">Temporizadores absolutos de WSL con una hora en el pasado no se activan [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="18a43-279">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="18a43-280">Asegúrate de que los puntos de reanálisis recién creados se muestren como tales en el directorio principal.</span><span class="sxs-lookup"><span data-stu-id="18a43-280">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="18a43-281">Crea de forma atómica directorios con distinción entre mayúsculas y minúsculas en DrvFs.</span><span class="sxs-lookup"><span data-stu-id="18a43-281">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="18a43-282">Se ha corregido un problema adicional en el que las operaciones de varios subprocesos podían devolver ENOENT, aunque el archivo existiese.</span><span class="sxs-lookup"><span data-stu-id="18a43-282">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="18a43-283">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="18a43-283">[GH 2712]</span></span>
* <span data-ttu-id="18a43-284">Se corrigió un error de inicio de WSL cuando UMCI está habilitado.</span><span class="sxs-lookup"><span data-stu-id="18a43-284">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="18a43-285">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="18a43-285">[GH 3020]</span></span>
* <span data-ttu-id="18a43-286">Agrega el menú contextual del explorador para iniciar WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="18a43-286">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="18a43-287">Para usar, mantén presionada la tecla Mayús y haz clic con el botón derecho en una ventana del explorador.</span><span class="sxs-lookup"><span data-stu-id="18a43-287">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="18a43-288">Corrección del comportamiento de no bloqueo de sockets de UNIX [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="18a43-288">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="18a43-289">Corrección del comando NETLINK que se bloquea, tal como se muestra en GH 2026.</span><span class="sxs-lookup"><span data-stu-id="18a43-289">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="18a43-290">Agrega compatibilidad para las marcas de propagación de montaje [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="18a43-290">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="18a43-291">Corrección del problema de truncamiento que no provoca eventos inotify [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="18a43-291">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="18a43-292">Agrega la opción --exec a wsl.exe para invocar un solo binario sin un shell.</span><span class="sxs-lookup"><span data-stu-id="18a43-292">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="18a43-293">Agrega la opción --distribution a wsl.exe para seleccionar una distribución específica.</span><span class="sxs-lookup"><span data-stu-id="18a43-293">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="18a43-294">Compatibilidad limitada para dmesg.</span><span class="sxs-lookup"><span data-stu-id="18a43-294">Limited support for dmesg.</span></span> <span data-ttu-id="18a43-295">Ahora, las aplicaciones pueden registrarse en dmesg.</span><span class="sxs-lookup"><span data-stu-id="18a43-295">Applications can now log to dmesg.</span></span> <span data-ttu-id="18a43-296">El controlador WSL registra información limitada en dmesg.</span><span class="sxs-lookup"><span data-stu-id="18a43-296">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="18a43-297">En el futuro, esto puede extenderse para llevar a cabo otros diagnósticos e información del controlador.</span><span class="sxs-lookup"><span data-stu-id="18a43-297">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="18a43-298">Nota: dmesg se admite actualmente a través de la interfaz de dispositivo `/dev/kmsg`.</span><span class="sxs-lookup"><span data-stu-id="18a43-298">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="18a43-299">Aún no se admite la interfaz syscall `syslog`.</span><span class="sxs-lookup"><span data-stu-id="18a43-299">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="18a43-300">Y, por lo tanto, algunas de las opciones de la línea de comandos de `dmesg`, como `-S` y `-C`, no funcionan.</span><span class="sxs-lookup"><span data-stu-id="18a43-300">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="18a43-301">Cambia el gid y el modo de dispositivos serie predeterminados para que coincidan con los nativos [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="18a43-301">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="18a43-302">DrvFs ahora admite atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="18a43-302">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="18a43-303">Nota: DrvFs tiene algunas limitaciones en cuanto al nombre de los atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="18a43-303">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="18a43-304">No se permiten algunos caracteres (como "/", ":" y "\*"), y los nombres de atributos extendidos no distinguen mayúsculas de minúsculas en DrvFs</span><span class="sxs-lookup"><span data-stu-id="18a43-304">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="18a43-305">Compilación 18252 (saltar)</span><span class="sxs-lookup"><span data-stu-id="18a43-305">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="18a43-306">Para obtener información general de Windows sobre la compilación 18252, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span><span class="sxs-lookup"><span data-stu-id="18a43-306">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-307">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-307">WSL</span></span>
* <span data-ttu-id="18a43-308">Traslado de los binarios init y bsdtar fuera del archivo dll lxssmanager y a una carpeta de herramientas independiente</span><span class="sxs-lookup"><span data-stu-id="18a43-308">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="18a43-309">Corrección de la carrera en torno al cierre del descriptor de archivo cuando se usa CLONE_FILES</span><span class="sxs-lookup"><span data-stu-id="18a43-309">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="18a43-310">Controla campos opcionales en /proc/pid/mountinfo al traducir rutas de DrvFs</span><span class="sxs-lookup"><span data-stu-id="18a43-310">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="18a43-311">Permite que DrvFs mknod se complete correctamente sin compatibilidad con metadatos para S_IFREG</span><span class="sxs-lookup"><span data-stu-id="18a43-311">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="18a43-312">Los archivos de solo lectura creados en DrvFs deben tener el atributo readonly establecido [GH 3411]</span><span class="sxs-lookup"><span data-stu-id="18a43-312">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="18a43-313">Agrega el asistente /sbin/mount.drvfs para controlar el montaje de DrvFs</span><span class="sxs-lookup"><span data-stu-id="18a43-313">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="18a43-314">Usa el cambio de nombre de POSIX en DrvFs.</span><span class="sxs-lookup"><span data-stu-id="18a43-314">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="18a43-315">Permite la traducción de rutas de acceso en volúmenes sin un GUID de volumen.</span><span class="sxs-lookup"><span data-stu-id="18a43-315">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="18a43-316">Compilación 17738 (rápida)</span><span class="sxs-lookup"><span data-stu-id="18a43-316">Build 17738 (Fast)</span></span>
<span data-ttu-id="18a43-317">Para obtener información general de Windows sobre la compilación 17738, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span><span class="sxs-lookup"><span data-stu-id="18a43-317">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-318">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-318">WSL</span></span>
* <span data-ttu-id="18a43-319">Comprobación de permisos de la llamada del sistema setpriority demasiado estricta para cambiar la misma prioridad de subprocesos [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="18a43-319">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="18a43-320">Asegúrate de que se use el tiempo de interrupción no sesgado para el tiempo de arranque para evitar que se devuelvan valores negativos para clock_gettime (CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="18a43-320">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="18a43-321">Controla los vínculos simbólicos en el intérprete binfmt de WSL [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="18a43-321">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="18a43-322">Mejor control de la limpieza de descriptores de archivo del líder del grupo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="18a43-322">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="18a43-323">Compilación 17728 (rápida)</span><span class="sxs-lookup"><span data-stu-id="18a43-323">Build 17728 (Fast)</span></span>
<span data-ttu-id="18a43-324">Para obtener información general de Windows sobre la compilación 17728, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span><span class="sxs-lookup"><span data-stu-id="18a43-324">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-325">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-325">WSL</span></span>
* <span data-ttu-id="18a43-326">Cambia WSL para usar KeQueryInterruptTimePrecise en lugar de KeQueryPerformanceCounter para evitar el desbordamiento [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="18a43-326">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="18a43-327">Ptrace attach puede producir un valor de devolución incorrecto de las llamadas del sistema [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="18a43-327">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="18a43-328">Corrección de varios problemas relacionados con AF_UNIX [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="18a43-328">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="18a43-329">Corrección del problema que podía provocar un error de interoperabilidad de WSL si el directorio de trabajo actual tiene menos de 5 caracteres de longitud [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="18a43-329">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="18a43-330">Compilación 18204 (saltar)</span><span class="sxs-lookup"><span data-stu-id="18a43-330">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="18a43-331">Para obtener información general de Windows sobre la compilación 18204, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="18a43-331">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-332">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-332">WSL</span></span>
* <span data-ttu-id="18a43-333">El sistema de archivos de canalización borra accidentalmente el evento epoll desencadenado por el borde [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="18a43-333">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="18a43-334">El ejecutable de Win32 iniciado mediante el vínculo simbólico de NTFS no respeta el nombre del vínculo simbólico [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="18a43-334">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="18a43-335">Compilación 17723 (rápida)</span><span class="sxs-lookup"><span data-stu-id="18a43-335">Build 17723 (Fast)</span></span>
<span data-ttu-id="18a43-336">Para obtener información general de Windows sobre la compilación 17723, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="18a43-336">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-337">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-337">WSL</span></span>
* <span data-ttu-id="18a43-338">Evita las conexiones de bucle invertido con error con retraso de un segundo a puertos no existentes [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="18a43-338">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="18a43-339">Agrega el archivo de código auxiliar /proc/sys/fs/file-max [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="18a43-339">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="18a43-340">Información más precisa sobre el ámbito IPV6.</span><span class="sxs-lookup"><span data-stu-id="18a43-340">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="18a43-341">Compatibilidad con PR_SET_PTRACER [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="18a43-341">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="18a43-342">El sistema de archivos de canalización borra accidentalmente el evento epoll desencadenado por el borde [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="18a43-342">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="18a43-343">El ejecutable de Win32 iniciado mediante el vínculo simbólico de NTFS no respeta el nombre del vínculo simbólico [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="18a43-343">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="18a43-344">Compilación 17713</span><span class="sxs-lookup"><span data-stu-id="18a43-344">Build 17713</span></span>
<span data-ttu-id="18a43-345">Para obtener información general de Windows sobre la compilación 17713, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span><span class="sxs-lookup"><span data-stu-id="18a43-345">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-346">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-346">WSL</span></span>
* <span data-ttu-id="18a43-347">Compatibilidad mejorada con zombie [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="18a43-347">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="18a43-348">Agrega entradas de wsl.conf para controlar el comportamiento de interoperabilidad de Windows [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="18a43-348">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="18a43-349">La corrección para getsockname no siempre devuelve el tipo de familia de socket de UNIX [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="18a43-349">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="18a43-350">Agrega compatibilidad para TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="18a43-350">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="18a43-351">Los sockets sin bloqueo en el proceso de conexión deben devolver EAGAIN para los intentos de escritura [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="18a43-351">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="18a43-352">Compatibilidad con la interoperabilidad en VHD montados [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="18a43-352">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="18a43-353">Corrección del problema de comprobación de permisos en la carpeta raíz [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="18a43-353">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="18a43-354">Compatibilidad limitada para los ioctl de teclado TTY KDGKBTYPE, KDGKBMODE y KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="18a43-354">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="18a43-355">Las aplicaciones de interfaz de usuario de Windows deben ejecutarse incluso cuando se inician en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="18a43-355">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="18a43-356">Compilación 17704</span><span class="sxs-lookup"><span data-stu-id="18a43-356">Build 17704</span></span>
<span data-ttu-id="18a43-357">Para obtener información general de Windows sobre la compilación 17704, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span><span class="sxs-lookup"><span data-stu-id="18a43-357">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-358">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-358">WSL</span></span>
* <span data-ttu-id="18a43-359">Agrega la opción wsl -u o --user [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="18a43-359">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="18a43-360">Corrección de problemas de inicio de WSL cuando el inicio rápido está habilitado [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="18a43-360">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="18a43-361">Los sockets de UNIX deben conservar las credenciales del mismo nivel desconectadas [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="18a43-361">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="18a43-362">Sockets de UNIX sin bloqueo con error de manera indefinida con EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="18a43-362">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="18a43-363">case=off es el nuevo tipo de montaje drvfs predeterminado [GH 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="18a43-363">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="18a43-364">Consulta el [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) para más información.</span><span class="sxs-lookup"><span data-stu-id="18a43-364">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="18a43-365">Agrega wslconfig/terminate para detener las distribuciones en ejecución.</span><span class="sxs-lookup"><span data-stu-id="18a43-365">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="18a43-366">Compilación 17692</span><span class="sxs-lookup"><span data-stu-id="18a43-366">Build 17692</span></span>
<span data-ttu-id="18a43-367">Para obtener información general de Windows sobre la compilación 17692, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span><span class="sxs-lookup"><span data-stu-id="18a43-367">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-368">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-368">WSL</span></span>
* <span data-ttu-id="18a43-369">Corrección del problema con las entradas del menú contextual del shell de WSL que no controlan correctamente las rutas de acceso con espacios.</span><span class="sxs-lookup"><span data-stu-id="18a43-369">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="18a43-370">Expone la distinción de mayúsculas y minúsculas por directorio como atributo extendido</span><span class="sxs-lookup"><span data-stu-id="18a43-370">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="18a43-371">ARM64: Emula las operaciones de mantenimiento de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="18a43-371">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="18a43-372">Resuelve un [problema de dotnet](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="18a43-372">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="18a43-373">DrvFs: solo caracteres con escape eliminado en el intervalo privado que corresponden a un carácter de escape.</span><span class="sxs-lookup"><span data-stu-id="18a43-373">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="18a43-374">Compilación 17686</span><span class="sxs-lookup"><span data-stu-id="18a43-374">Build 17686</span></span>
<span data-ttu-id="18a43-375">Para obtener información general de Windows sobre la compilación 17686, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span><span class="sxs-lookup"><span data-stu-id="18a43-375">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-376">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-376">WSL</span></span>
* <span data-ttu-id="18a43-377">Corrección error de desviación por uno en la validación de longitud del intérprete del analizador ELF [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="18a43-377">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="18a43-378">Temporizadores absolutos de WSL con una hora en el pasado no se activan [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="18a43-378">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="18a43-379">Asegúrate de que los puntos de reanálisis recién creados se muestren como tales en el directorio principal.</span><span class="sxs-lookup"><span data-stu-id="18a43-379">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="18a43-380">Crea de forma atómica directorios con distinción entre mayúsculas y minúsculas en DrvFs.</span><span class="sxs-lookup"><span data-stu-id="18a43-380">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="18a43-381">Compilación 17677</span><span class="sxs-lookup"><span data-stu-id="18a43-381">Build 17677</span></span>
<span data-ttu-id="18a43-382">Para obtener información general de Windows sobre la compilación 17677, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span><span class="sxs-lookup"><span data-stu-id="18a43-382">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-383">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-383">WSL</span></span>
* <span data-ttu-id="18a43-384">Se ha corregido un problema adicional en el que las operaciones de varios subprocesos podían devolver ENOENT, aunque el archivo existiese.</span><span class="sxs-lookup"><span data-stu-id="18a43-384">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="18a43-385">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="18a43-385">[GH 2712]</span></span>
* <span data-ttu-id="18a43-386">Se corrigió un error de inicio de WSL cuando UMCI está habilitado.</span><span class="sxs-lookup"><span data-stu-id="18a43-386">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="18a43-387">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="18a43-387">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="18a43-388">Compilación 17666</span><span class="sxs-lookup"><span data-stu-id="18a43-388">Build 17666</span></span>
<span data-ttu-id="18a43-389">Para obtener información general de Windows sobre la compilación 17666, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span><span class="sxs-lookup"><span data-stu-id="18a43-389">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-390">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-390">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="18a43-391">ADVERTENCIA: Hay un problema que impide que WSL se ejecute en algunos conjuntos de chips AMD [GH 3134].</span><span class="sxs-lookup"><span data-stu-id="18a43-391">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="18a43-392">Hay una corrección lista y en camino en la rama de compilación de Insider.</span><span class="sxs-lookup"><span data-stu-id="18a43-392">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="18a43-393">Agrega el menú contextual del explorador para iniciar WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="18a43-393">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="18a43-394">Para usar, mantén presionada la tecla Mayús y haz clic con el botón derecho en una ventana del explorador.</span><span class="sxs-lookup"><span data-stu-id="18a43-394">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="18a43-395">Corrección del comportamiento de no bloqueo de sockets de Unix [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="18a43-395">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="18a43-396">Corrección del comando NETLINK que se bloquea, tal como se muestra en GH 2026.</span><span class="sxs-lookup"><span data-stu-id="18a43-396">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="18a43-397">Agrega compatibilidad para las marcas de propagación de montaje [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="18a43-397">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="18a43-398">Corrección del problema de truncamiento que no provoca eventos inotify [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="18a43-398">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="18a43-399">Agrega la opción --exec a wsl.exe para invocar un solo binario sin un shell.</span><span class="sxs-lookup"><span data-stu-id="18a43-399">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="18a43-400">Agrega la opción --distribution a wsl.exe para seleccionar una distribución específica.</span><span class="sxs-lookup"><span data-stu-id="18a43-400">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="18a43-401">Compilación 17655 (saltar)</span><span class="sxs-lookup"><span data-stu-id="18a43-401">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="18a43-402">Para obtener información general de Windows sobre la compilación 17655, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="18a43-402">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-403">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-403">WSL</span></span>
* <span data-ttu-id="18a43-404">Compatibilidad limitada para dmesg.</span><span class="sxs-lookup"><span data-stu-id="18a43-404">Limited support for dmesg.</span></span> <span data-ttu-id="18a43-405">Ahora, las aplicaciones pueden registrarse en dmesg.</span><span class="sxs-lookup"><span data-stu-id="18a43-405">Applications can now log to dmesg.</span></span> <span data-ttu-id="18a43-406">El controlador WSL registra información limitada en dmesg.</span><span class="sxs-lookup"><span data-stu-id="18a43-406">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="18a43-407">En el futuro, esto puede extenderse para llevar a cabo otros diagnósticos e información del controlador.</span><span class="sxs-lookup"><span data-stu-id="18a43-407">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="18a43-408">Nota: dmesg se admite actualmente a través de la interfaz de dispositivo `/dev/kmsg`.</span><span class="sxs-lookup"><span data-stu-id="18a43-408">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="18a43-409">Aún no se admite la interfaz sycall `syslog`.</span><span class="sxs-lookup"><span data-stu-id="18a43-409">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="18a43-410">Y, por lo tanto, algunas de las opciones de la línea de comandos de `dmesg`, como `-S` y `-C`, no funcionan.</span><span class="sxs-lookup"><span data-stu-id="18a43-410">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="18a43-411">Se ha corregido un problema en el que las operaciones de varios subprocesos podían devolver ENOENT, aunque el archivo existiese.</span><span class="sxs-lookup"><span data-stu-id="18a43-411">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="18a43-412">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="18a43-412">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="18a43-413">Compilación 17639 (saltar)</span><span class="sxs-lookup"><span data-stu-id="18a43-413">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="18a43-414">Para obtener información general de Windows sobre la compilación 17639, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="18a43-414">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-415">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-415">WSL</span></span>
* <span data-ttu-id="18a43-416">Cambia el gid y el modo de dispositivos serie predeterminados para que coincidan con los nativos [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="18a43-416">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="18a43-417">DrvFs ahora admite atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="18a43-417">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="18a43-418">Nota: DrvFs tiene algunas limitaciones en cuanto al nombre de los atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="18a43-418">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="18a43-419">En particular, no se permiten algunos caracteres (como "/", ":" y "\*"), y los nombres de atributos extendidos no distinguen mayúsculas de minúsculas en DrvFs</span><span class="sxs-lookup"><span data-stu-id="18a43-419">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="18a43-420">Compilación 17133 (rápida)</span><span class="sxs-lookup"><span data-stu-id="18a43-420">Build 17133 (Fast)</span></span>
<span data-ttu-id="18a43-421">Para obtener información general de Windows sobre la compilación 17133, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="18a43-421">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-422">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-422">WSL</span></span>
* <span data-ttu-id="18a43-423">Corrección de un bloqueo en WSL.</span><span class="sxs-lookup"><span data-stu-id="18a43-423">Fix for hang in WSL.</span></span> <span data-ttu-id="18a43-424">[GH 3039, 3034]</span><span class="sxs-lookup"><span data-stu-id="18a43-424">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="18a43-425">Compilación 17128 (rápida)</span><span class="sxs-lookup"><span data-stu-id="18a43-425">Build 17128 (Fast)</span></span>
<span data-ttu-id="18a43-426">Para obtener información general de Windows sobre la compilación 17128, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="18a43-426">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-427">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-427">WSL</span></span>
* <span data-ttu-id="18a43-428">Ninguno</span><span class="sxs-lookup"><span data-stu-id="18a43-428">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="18a43-429">Compilación 17627 (saltar)</span><span class="sxs-lookup"><span data-stu-id="18a43-429">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="18a43-430">Para obtener información general de Windows sobre la compilación 17627, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="18a43-430">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-431">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-431">WSL</span></span>
* <span data-ttu-id="18a43-432">Agrega compatibilidad para las operaciones compatibles con pi de Futex.</span><span class="sxs-lookup"><span data-stu-id="18a43-432">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="18a43-433">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="18a43-433">[GH 1006]</span></span>
    * <span data-ttu-id="18a43-434">Ten en cuenta que las prioridades no son actualmente una característica admitida de WSL, por lo que hay limitaciones, pero el uso estándar debería estar desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="18a43-434">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="18a43-435">Compatibilidad con el Firewall de Windows para los procesos de WSL.</span><span class="sxs-lookup"><span data-stu-id="18a43-435">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="18a43-436">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="18a43-436">[GH 1852]</span></span>
    * <span data-ttu-id="18a43-437">Por ejemplo, para permitir que el proceso de Python de WSL escuche en cualquier puerto, use el cmd de Windows con privilegios elevados: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span><span class="sxs-lookup"><span data-stu-id="18a43-437">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="18a43-438">Para más información sobre cómo agregar reglas de firewall, consulte el [vínculo](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span><span class="sxs-lookup"><span data-stu-id="18a43-438">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="18a43-439">Respeta el shell predeterminado del usuario al usar wsl.exe.</span><span class="sxs-lookup"><span data-stu-id="18a43-439">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="18a43-440">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="18a43-440">[GH 2372]</span></span>
* <span data-ttu-id="18a43-441">Informa de todas las interfaces de red como Ethernet.</span><span class="sxs-lookup"><span data-stu-id="18a43-441">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="18a43-442">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="18a43-442">[GH 2996]</span></span>
* <span data-ttu-id="18a43-443">Mejor control del archivo /etc/passwd dañado.</span><span class="sxs-lookup"><span data-stu-id="18a43-443">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="18a43-444">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="18a43-444">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="18a43-445">Console</span><span class="sxs-lookup"><span data-stu-id="18a43-445">Console</span></span>
* <span data-ttu-id="18a43-446">Sin correcciones.</span><span class="sxs-lookup"><span data-stu-id="18a43-446">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-447">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-447">LTP Results:</span></span>
<span data-ttu-id="18a43-448">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="18a43-448">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="18a43-449">Compilación 17618 (saltar)</span><span class="sxs-lookup"><span data-stu-id="18a43-449">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="18a43-450">Para obtener información general de Windows sobre la compilación 17618, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="18a43-450">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-451">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-451">WSL</span></span>
* <span data-ttu-id="18a43-452">Presenta la funcionalidad de pseudoconsola para la interoperabilidad de NT [GH 988, 1366, 1433, 1542, 2370, 2406].</span><span class="sxs-lookup"><span data-stu-id="18a43-452">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="18a43-453">El mecanismo de instalación heredado (lxrun.exe) está en desuso.</span><span class="sxs-lookup"><span data-stu-id="18a43-453">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="18a43-454">El mecanismo admitido para la instalación de distribuciones es a través de Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="18a43-454">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="18a43-455">Console</span><span class="sxs-lookup"><span data-stu-id="18a43-455">Console</span></span>
* <span data-ttu-id="18a43-456">Sin correcciones.</span><span class="sxs-lookup"><span data-stu-id="18a43-456">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-457">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-457">LTP Results:</span></span>
<span data-ttu-id="18a43-458">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="18a43-458">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="18a43-459">Compilación 17110</span><span class="sxs-lookup"><span data-stu-id="18a43-459">Build 17110</span></span>
<span data-ttu-id="18a43-460">Para obtener información general de Windows sobre la compilación 17110, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span><span class="sxs-lookup"><span data-stu-id="18a43-460">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-461">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-461">WSL</span></span>
* <span data-ttu-id="18a43-462">Permite que/init finalice desde Windows [GH 2928].</span><span class="sxs-lookup"><span data-stu-id="18a43-462">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="18a43-463">DrvFs ahora usa la distinción de mayúsculas y minúsculas por directorio de manera predeterminada (equivalente a la opción de montaje "case=dir").</span><span class="sxs-lookup"><span data-stu-id="18a43-463">DrvFs now uses per-directory case sensitivity by default (equivalent to the “case=dir” mount option).</span></span>
    * <span data-ttu-id="18a43-464">El uso de "case=force" (el comportamiento anterior) requiere el establecimiento de una clave del Registro.</span><span class="sxs-lookup"><span data-stu-id="18a43-464">Using “case=force” (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="18a43-465">Ejecuta el siguiente comando para habilitar "case=force" si necesitas usarlo: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span><span class="sxs-lookup"><span data-stu-id="18a43-465">Run the following command to enable “case=force” if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="18a43-466">Si tienes directorios existentes creados con WSL en una versión anterior de Windows que deben distinguir entre mayúsculas y minúsculas, usa fsutil.exe para marcarlos con distinción de mayúsculas y minúsculas:fsutil.exe file setcasesensitiveinfo <path> enable</span><span class="sxs-lookup"><span data-stu-id="18a43-466">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="18a43-467">La llamada del sistema uname devuelve cadenas de finalización NULL.</span><span class="sxs-lookup"><span data-stu-id="18a43-467">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="18a43-468">Console</span><span class="sxs-lookup"><span data-stu-id="18a43-468">Console</span></span>
* <span data-ttu-id="18a43-469">Sin correcciones.</span><span class="sxs-lookup"><span data-stu-id="18a43-469">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-470">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-470">LTP Results:</span></span>
<span data-ttu-id="18a43-471">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="18a43-471">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="18a43-472">Compilación 17107</span><span class="sxs-lookup"><span data-stu-id="18a43-472">Build 17107</span></span>
<span data-ttu-id="18a43-473">Para obtener información general de Windows sobre la compilación 17107, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span><span class="sxs-lookup"><span data-stu-id="18a43-473">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-474">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-474">WSL</span></span>
* <span data-ttu-id="18a43-475">Compatibilidad con TCSETSF y TCSETSW en los puntos de conexión de master pty [GH 2552].</span><span class="sxs-lookup"><span data-stu-id="18a43-475">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="18a43-476">Iniciar procesos de interoperabilidad simultáneos puede dar lugar a EINVAL [GH 2813].</span><span class="sxs-lookup"><span data-stu-id="18a43-476">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="18a43-477">Corrección de PTRACE_ATTACH para mostrar el estado de seguimiento adecuado en /proc/pid/status.</span><span class="sxs-lookup"><span data-stu-id="18a43-477">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="18a43-478">Corrección de la carrera en la que los procesos de corta duración clonados con las marcas CLEARTID y SETTID podrían salir sin borrar la dirección de TID.</span><span class="sxs-lookup"><span data-stu-id="18a43-478">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="18a43-479">Muestra un mensaje al actualizar los directorios del sistema de archivos de Linux al pasar de una compilación anterior a 17093.</span><span class="sxs-lookup"><span data-stu-id="18a43-479">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="18a43-480">Para más detalles sobre los cambios del sistema de archivos de 17093, consulta las notas de la versión de [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span><span class="sxs-lookup"><span data-stu-id="18a43-480">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="18a43-481">Console</span><span class="sxs-lookup"><span data-stu-id="18a43-481">Console</span></span>
* <span data-ttu-id="18a43-482">Sin correcciones.</span><span class="sxs-lookup"><span data-stu-id="18a43-482">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-483">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-483">LTP Results:</span></span>
<span data-ttu-id="18a43-484">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="18a43-484">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="18a43-485">Compilación 17101</span><span class="sxs-lookup"><span data-stu-id="18a43-485">Build 17101</span></span>
<span data-ttu-id="18a43-486">Para obtener información general de Windows sobre la compilación 17101, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="18a43-486">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-487">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-487">WSL</span></span>
* <span data-ttu-id="18a43-488">Compatibilidad con signalfd.</span><span class="sxs-lookup"><span data-stu-id="18a43-488">Support for signalfd.</span></span> <span data-ttu-id="18a43-489">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="18a43-489">[GH 129]</span></span>
* <span data-ttu-id="18a43-490">Admite nombres de archivo que contienen caracteres NTFS no válidos mediante su codificación como caracteres Unicode privados.</span><span class="sxs-lookup"><span data-stu-id="18a43-490">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="18a43-491">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="18a43-491">[GH 1514]</span></span>
* <span data-ttu-id="18a43-492">El montaje automático se revertirá al modo de solo lectura cuando no se admita la escritura.</span><span class="sxs-lookup"><span data-stu-id="18a43-492">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="18a43-493">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="18a43-493">[GH 2603]</span></span>
* <span data-ttu-id="18a43-494">Permite pegar los pares suplentes Unicode (como los caracteres emoji).</span><span class="sxs-lookup"><span data-stu-id="18a43-494">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="18a43-495">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="18a43-495">[GH 2765]</span></span>
* <span data-ttu-id="18a43-496">Los pseudoarchivos en /proc y /sys deben devolver los valores read ready y write ready de select, poll, epoll, etc. [GH 2838]</span><span class="sxs-lookup"><span data-stu-id="18a43-496">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="18a43-497">Corrección de un problema que podría hacer que el servicio pudiera entrar en un bucle infinito cuando el Registro se haya alterado o esté dañado.</span><span class="sxs-lookup"><span data-stu-id="18a43-497">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="18a43-498">Corrección de los mensajes de netlink para trabajar con la versión más reciente (de nivel superior 4.14) de iproute2.</span><span class="sxs-lookup"><span data-stu-id="18a43-498">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="18a43-499">Console</span><span class="sxs-lookup"><span data-stu-id="18a43-499">Console</span></span>
* <span data-ttu-id="18a43-500">Sin correcciones.</span><span class="sxs-lookup"><span data-stu-id="18a43-500">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-501">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-501">LTP Results:</span></span>
<span data-ttu-id="18a43-502">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="18a43-502">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="18a43-503">Compilación 17093</span><span class="sxs-lookup"><span data-stu-id="18a43-503">Build 17093</span></span>
<span data-ttu-id="18a43-504">Para obtener información general de Windows sobre la compilación 17093, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span><span class="sxs-lookup"><span data-stu-id="18a43-504">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="18a43-505">Importante:</span><span class="sxs-lookup"><span data-stu-id="18a43-505">Important:</span></span>
<span data-ttu-id="18a43-506">Al iniciar WSL por primera vez después de actualizar a esta compilación, tiene que hacer algún trabajo para actualizar los directorios del sistema de archivos de Linux.</span><span class="sxs-lookup"><span data-stu-id="18a43-506">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="18a43-507">Esto puede tardar varios minutos, por lo que es posible que WSL se inicie lentamente.</span><span class="sxs-lookup"><span data-stu-id="18a43-507">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="18a43-508">Esto solo debería ocurrir una vez por cada distribución que haya instalado desde Store.</span><span class="sxs-lookup"><span data-stu-id="18a43-508">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="18a43-509">Compatibilidad mejorada de distinción de mayúsculas y minúsculas en DrvFs.</span><span class="sxs-lookup"><span data-stu-id="18a43-509">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="18a43-510">DrvFs admite ahora la distinción de mayúsculas y minúsculas por directorio.</span><span class="sxs-lookup"><span data-stu-id="18a43-510">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="18a43-511">Se trata de una nueva marca que se puede establecer en los directorios para indicar que todas las operaciones de esos directorios deben tratarse como con distinción de mayúsculas y minúsculas, lo que permite que las aplicaciones de Windows abran correctamente archivos que solo difieren en mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="18a43-511">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="18a43-512">DrvFs tiene nuevas opciones de montaje que controlan la distinción de mayúsculas y minúsculas por directorio.</span><span class="sxs-lookup"><span data-stu-id="18a43-512">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="18a43-513">case=force: todos los directorios se tratan con distinción de mayúsculas y minúsculas (excepto la raíz de la unidad).</span><span class="sxs-lookup"><span data-stu-id="18a43-513">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="18a43-514">Los nuevos directorios creados con WSL se marcan con distinción de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="18a43-514">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="18a43-515">Este es el comportamiento heredado, excepto para marcar los nuevos directorios que distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="18a43-515">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="18a43-516">case=dir: solo los directorios con la marca de distinción de mayúsculas y minúsculas por directorio se tratan como que distinguen mayúsculas de minúsculas; los otros directorios no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="18a43-516">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="18a43-517">Los nuevos directorios creados con WSL se marcan con distinción de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="18a43-517">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="18a43-518">case=off: solo los directorios con la marca de distinción de mayúsculas y minúsculas por directorio se tratan como que distinguen mayúsculas de minúsculas; los otros directorios no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="18a43-518">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="18a43-519">Los nuevos directorios creados con WSL se marcan como sin distinción de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="18a43-519">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="18a43-520">Nota: Los directorios creados por WSL en versiones anteriores no tienen esta marca establecida, por lo que no se tratará como con distinción entre mayúsculas y minúsculas si usas la opción "case=dir".</span><span class="sxs-lookup"><span data-stu-id="18a43-520">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the “case=dir” option.</span></span> <span data-ttu-id="18a43-521">Próximamente se presentará una manera de establecer esta marca en los directorios existentes.</span><span class="sxs-lookup"><span data-stu-id="18a43-521">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="18a43-522">Ejemplo de montaje con estas opciones (en el caso de las unidades existentes, primero debes desmontar antes de poder montar con distintas opciones): sudo mount -t drvfs C: /mnt/c -o case=dir</span><span class="sxs-lookup"><span data-stu-id="18a43-522">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="18a43-523">Por ahora, case=force sigue siendo la opción predeterminada.</span><span class="sxs-lookup"><span data-stu-id="18a43-523">For now, case=force is still the default option.</span></span> <span data-ttu-id="18a43-524">Se cambiará a case=dir en el futuro.</span><span class="sxs-lookup"><span data-stu-id="18a43-524">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="18a43-525">Ahora puedes usar barras diagonales en las rutas de acceso de Windows al montar DrvFs, por ejemplo: sudo mount -t drvfs //server/share /mnt/share</span><span class="sxs-lookup"><span data-stu-id="18a43-525">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="18a43-526">WSL ahora procesa el archivo /etc/fstab durante el inicio de la instancia [GH 2636].</span><span class="sxs-lookup"><span data-stu-id="18a43-526">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="18a43-527">Esto se hace antes de montar automáticamente las unidades de DrvFs; las unidades que ya se hayan montado mediante fstab no se volverán a montar automáticamente, lo que te permite cambiar el punto de montaje para unidades específicas.</span><span class="sxs-lookup"><span data-stu-id="18a43-527">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="18a43-528">Este comportamiento se puede desactivar mediante wsl.conf.</span><span class="sxs-lookup"><span data-stu-id="18a43-528">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="18a43-529">Los archivos mount, mountinfo y mountstats de /proc convierten correctamente en caracteres especiales, como barras diagonales inversas y espacios [GH 2799]</span><span class="sxs-lookup"><span data-stu-id="18a43-529">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="18a43-530">Los archivos especiales creados con DrvFs, como los vínculos simbólicos de WSL, o fifos y sockets cuando los metadatos están habilitados, ahora se pueden copiar y mover desde Windows.</span><span class="sxs-lookup"><span data-stu-id="18a43-530">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="18a43-531">WSL es más configurable con wsl.conf</span><span class="sxs-lookup"><span data-stu-id="18a43-531">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="18a43-532">Hemos agregado un método para que configures automáticamente cierta funcionalidad en WSL que se aplicará cada vez que inicies el subsistema.</span><span class="sxs-lookup"><span data-stu-id="18a43-532">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="18a43-533">Esto incluye opciones de montaje automático y configuración de red.</span><span class="sxs-lookup"><span data-stu-id="18a43-533">This includes automount options and network configuration.</span></span> <span data-ttu-id="18a43-534">Obtén más información en la publicación de blog en https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="18a43-534">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="af_unix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="18a43-535">AF_UNIX permite conexiones de socket entre procesos de Linux en procesos nativos de WSL y Windows</span><span class="sxs-lookup"><span data-stu-id="18a43-535">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="18a43-536">Las aplicaciones de WSL y Windows ahora pueden comunicarse entre sí a través de sockets de Unix.</span><span class="sxs-lookup"><span data-stu-id="18a43-536">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="18a43-537">Imagina que quieres ejecutar un servicio en Windows y hacer que esté disponible para las aplicaciones de WSL y Windows.</span><span class="sxs-lookup"><span data-stu-id="18a43-537">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="18a43-538">Ahora, eso es posible con los sockets de Unix.</span><span class="sxs-lookup"><span data-stu-id="18a43-538">Now, that’s possible with Unix sockets.</span></span> <span data-ttu-id="18a43-539">Lee más en nuestra publicación de blog en https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="18a43-539">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-540">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-540">WSL</span></span>
* <span data-ttu-id="18a43-541">Compatibilidad de mmap() con MAP_NORESERVE [GH 121, 2784]</span><span class="sxs-lookup"><span data-stu-id="18a43-541">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="18a43-542">Compatibilidad con CLONE_PTRACE y CLONE_UNTRACED [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="18a43-542">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="18a43-543">Controla la señal de terminación no SIGCHLD en el clon [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="18a43-543">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="18a43-544">Código auxiliar /proc/sys/fs/inotify/max_user_instances y /proc/sys/fs/inotify/max_user_watches [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="18a43-544">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="18a43-545">Error al cargar binarios de ELF que contienen encabezados de carga con desplazamientos distintos de cero [GH 1884]</span><span class="sxs-lookup"><span data-stu-id="18a43-545">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="18a43-546">Se eliminan los bytes de página finales al cargar imágenes.</span><span class="sxs-lookup"><span data-stu-id="18a43-546">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="18a43-547">Reduce los casos en los que execve finaliza el proceso de forma silenciosa</span><span class="sxs-lookup"><span data-stu-id="18a43-547">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="18a43-548">Console</span><span class="sxs-lookup"><span data-stu-id="18a43-548">Console</span></span>
* <span data-ttu-id="18a43-549">Sin correcciones.</span><span class="sxs-lookup"><span data-stu-id="18a43-549">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-550">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-550">LTP Results:</span></span>
<span data-ttu-id="18a43-551">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="18a43-551">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="18a43-552">Compilación 17083</span><span class="sxs-lookup"><span data-stu-id="18a43-552">Build 17083</span></span>
<span data-ttu-id="18a43-553">Para obtener información general de Windows sobre la compilación 17083, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="18a43-553">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-554">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-554">WSL</span></span>
* <span data-ttu-id="18a43-555">Se ha corregido la comprobación de errores relacionada con epoll [GH 2798, 2801, 2857]</span><span class="sxs-lookup"><span data-stu-id="18a43-555">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="18a43-556">Se han corregido bloqueos al desactivar ASLR [GH 1185, 2870]</span><span class="sxs-lookup"><span data-stu-id="18a43-556">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="18a43-557">Asegúrate de que las operaciones de mmap aparezcan como atómicas [GH 2732]</span><span class="sxs-lookup"><span data-stu-id="18a43-557">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="18a43-558">Console</span><span class="sxs-lookup"><span data-stu-id="18a43-558">Console</span></span>
* <span data-ttu-id="18a43-559">Sin correcciones.</span><span class="sxs-lookup"><span data-stu-id="18a43-559">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-560">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-560">LTP Results:</span></span>
<span data-ttu-id="18a43-561">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="18a43-561">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="18a43-562">Compilación 17074</span><span class="sxs-lookup"><span data-stu-id="18a43-562">Build 17074</span></span>
<span data-ttu-id="18a43-563">Para obtener información general de Windows sobre la compilación 17074, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span><span class="sxs-lookup"><span data-stu-id="18a43-563">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-564">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-564">WSL</span></span>
* <span data-ttu-id="18a43-565">Se ha corregido el formato de almacenamiento de los metadatos de DrvFs [GH 2777]</span><span class="sxs-lookup"><span data-stu-id="18a43-565">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="18a43-566">**Importante:** Los metadatos de DrvFs creados antes de esta compilación no se mostrarán correctamente o no se mostrarán en absoluto.</span><span class="sxs-lookup"><span data-stu-id="18a43-566">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="18a43-567">Para corregir los archivos afectados, usa chmod y chown para volver a aplicar los metadatos.</span><span class="sxs-lookup"><span data-stu-id="18a43-567">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="18a43-568">Se ha corregido un problema con varias señales y llamadas del sistema reiniciables.</span><span class="sxs-lookup"><span data-stu-id="18a43-568">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="18a43-569">Console</span><span class="sxs-lookup"><span data-stu-id="18a43-569">Console</span></span>
* <span data-ttu-id="18a43-570">Sin correcciones.</span><span class="sxs-lookup"><span data-stu-id="18a43-570">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-571">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-571">LTP Results:</span></span>
<span data-ttu-id="18a43-572">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="18a43-572">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="18a43-573">Compilación 17063</span><span class="sxs-lookup"><span data-stu-id="18a43-573">Build 17063</span></span>
<span data-ttu-id="18a43-574">Para obtener información general de Windows sobre la compilación 17063, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span><span class="sxs-lookup"><span data-stu-id="18a43-574">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="18a43-575">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-575">WSL</span></span>
* <span data-ttu-id="18a43-576">DrvFs admite metadatos de Linux adicionales.</span><span class="sxs-lookup"><span data-stu-id="18a43-576">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="18a43-577">Esto permite establecer el propietario y el modo de los archivos con chmod/chown, y también la creación de archivos especiales, como fifos, sockets de Unix y archivos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18a43-577">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="18a43-578">Esta opción está deshabilitada de forma predeterminada, ya que sigue siendo experimental.</span><span class="sxs-lookup"><span data-stu-id="18a43-578">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="18a43-579">**Nota:**  Se ha corregido un error en el formato de metadatos usado por DrvFs.</span><span class="sxs-lookup"><span data-stu-id="18a43-579">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="18a43-580">Si bien los metadatos funcionan en esta compilación para experimentación, las compilaciones futuras no leerán correctamente los metadatos creados por esta compilación.</span><span class="sxs-lookup"><span data-stu-id="18a43-580">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="18a43-581">Es posible que tengas que actualizar manualmente el propietario de los archivos modificados, y se tendrán que volver a crear los dispositivos con un identificador de dispositivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="18a43-581">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="18a43-582">Para habilitar, monta DrvFs con la opción de metadatos (para habilitarlo en un montaje existente, primero debes desmontarlo):</span><span class="sxs-lookup"><span data-stu-id="18a43-582">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="18a43-583">Los permisos de Linux se agregan como metadatos adicionales al archivo; no afectan a los permisos de Windows.</span><span class="sxs-lookup"><span data-stu-id="18a43-583">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="18a43-584">Recuerda que la edición de un archivo mediante un editor de Windows puede quitar los metadatos.</span><span class="sxs-lookup"><span data-stu-id="18a43-584">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="18a43-585">En este caso, el archivo volverá a sus permisos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="18a43-585">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="18a43-586">Se han agregado opciones de montaje a DrvFs para controlar archivos sin metadatos.</span><span class="sxs-lookup"><span data-stu-id="18a43-586">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="18a43-587">uid: el identificador de usuario que se usa para el propietario de todos los archivos.</span><span class="sxs-lookup"><span data-stu-id="18a43-587">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="18a43-588">gid: el identificador de grupo que se usa para el propietario de todos los archivos.</span><span class="sxs-lookup"><span data-stu-id="18a43-588">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="18a43-589">umask: máscara octal de permisos que se van a excluir para todos los archivos y directorios.</span><span class="sxs-lookup"><span data-stu-id="18a43-589">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="18a43-590">fmask: máscara octal de permisos que se van a excluir para todos los archivos normales.</span><span class="sxs-lookup"><span data-stu-id="18a43-590">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="18a43-591">dmask: máscara octal de permisos que se van a excluir para todos los directorios.</span><span class="sxs-lookup"><span data-stu-id="18a43-591">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="18a43-592">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="18a43-592">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="18a43-593">Combina con la opción de metadatos para especificar los permisos predeterminados para los archivos sin metadatos.</span><span class="sxs-lookup"><span data-stu-id="18a43-593">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="18a43-594">Se presentó una nueva variable de entorno, `WSLENV`, para configurar cómo fluyen las variables de entorno entre WSL y Win32.</span><span class="sxs-lookup"><span data-stu-id="18a43-594">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="18a43-595">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="18a43-595">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="18a43-596">`WSLENV` es una lista de variables de entorno delimitadas por signos de dos puntos que se puede incluir al iniciar procesos de WSL desde Win32, o procesos de Win32 desde WSL.</span><span class="sxs-lookup"><span data-stu-id="18a43-596">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="18a43-597">Cada variable puede tener como sufijo una barra diagonal seguida de marcas para especificar cómo se va a traducir.</span><span class="sxs-lookup"><span data-stu-id="18a43-597">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="18a43-598">p: El valor es una ruta de acceso que se debe traducir entre las rutas de acceso de WSL y las rutas de acceso de Win32.</span><span class="sxs-lookup"><span data-stu-id="18a43-598">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="18a43-599">l: El valor es una lista de rutas de acceso.</span><span class="sxs-lookup"><span data-stu-id="18a43-599">l: The value is a list of paths.</span></span> <span data-ttu-id="18a43-600">En WSL, se trata de una lista delimitada por signos de dos puntos.</span><span class="sxs-lookup"><span data-stu-id="18a43-600">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="18a43-601">En Win32, se trata de una lista delimitada por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="18a43-601">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="18a43-602">u: Solo se debe incluir el valor al invocar WSL desde Win32</span><span class="sxs-lookup"><span data-stu-id="18a43-602">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="18a43-603">w: Solo se debe incluir el valor al invocar Win32 desde WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-603">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="18a43-604">Puedes establecer `WSLENV` en. bashrc o en el entorno de Windows personalizado para el usuario.</span><span class="sxs-lookup"><span data-stu-id="18a43-604">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="18a43-605">drvfs monta correctamente las marcas de tiempo de conservación desde tar, cp -p (GH 1939)</span><span class="sxs-lookup"><span data-stu-id="18a43-605">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="18a43-606">Los vínculos simbólicos de drvfs informan el tamaño correcto (GH 2641)</span><span class="sxs-lookup"><span data-stu-id="18a43-606">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="18a43-607">La lectura/escritura funciona para tamaños de E/S muy grandes (GH 2653)</span><span class="sxs-lookup"><span data-stu-id="18a43-607">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="18a43-608">waitpid funciona con identificadores de grupo de procesos (GH 2534)</span><span class="sxs-lookup"><span data-stu-id="18a43-608">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="18a43-609">Rendimiento de mmap significativamente mejorado para regiones de reserva grandes; mejora el rendimiento de ghc (GH 1671)</span><span class="sxs-lookup"><span data-stu-id="18a43-609">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="18a43-610">Compatibilidad de personality con READ_IMPLIES_EXEC; corrige maxima y clisp (GH 1185)</span><span class="sxs-lookup"><span data-stu-id="18a43-610">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="18a43-611">mprotect admite PROT_GROWSDOWN; corrige clisp (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="18a43-611">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="18a43-612">Correcciones de errores de página en modo de sobreconfirmación; corrige sbcl (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="18a43-612">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="18a43-613">clone admite más combinaciones de marcas</span><span class="sxs-lookup"><span data-stu-id="18a43-613">clone supports more flags combinations</span></span>
* <span data-ttu-id="18a43-614">Compatibilidad con select/epoll de archivos de epoll (antes de una no-op).</span><span class="sxs-lookup"><span data-stu-id="18a43-614">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="18a43-615">Notifica a ptrace de llamadas del sistema sin implementar.</span><span class="sxs-lookup"><span data-stu-id="18a43-615">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="18a43-616">Omite las interfaces que no están listas al generar los servidores de nombres resolv.conf [GH 2694]</span><span class="sxs-lookup"><span data-stu-id="18a43-616">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="18a43-617">Enumera las interfaces de red sin dirección física.</span><span class="sxs-lookup"><span data-stu-id="18a43-617">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="18a43-618">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="18a43-618">[GH 2685]</span></span>
* <span data-ttu-id="18a43-619">Mejoras y correcciones de errores adicionales.</span><span class="sxs-lookup"><span data-stu-id="18a43-619">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="18a43-620">Herramientas de Linux disponibles para desarrolladores en Windows</span><span class="sxs-lookup"><span data-stu-id="18a43-620">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="18a43-621">La cadena de herramientas de la línea de comandos de Windows incluye bsdtar (tar) y curl.</span><span class="sxs-lookup"><span data-stu-id="18a43-621">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="18a43-622">Lee [este blog](https://aka.ms/tarcurlwindows) para más información acerca de cómo agregar estas dos nuevas herramientas y ver cómo dan forma a la experiencia de los desarrolladores en Windows.</span><span class="sxs-lookup"><span data-stu-id="18a43-622">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they’re shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="18a43-623">`AF_UNIX` está disponible en el SDK de Windows Insider (17061+).</span><span class="sxs-lookup"><span data-stu-id="18a43-623">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="18a43-624">Lee [este blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) para más información sobre `AF_UNIX` y cómo pueden usarlo los desarrolladores de Windows.</span><span class="sxs-lookup"><span data-stu-id="18a43-624">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="18a43-625">Console</span><span class="sxs-lookup"><span data-stu-id="18a43-625">Console</span></span>
* <span data-ttu-id="18a43-626">Sin correcciones.</span><span class="sxs-lookup"><span data-stu-id="18a43-626">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-627">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-627">LTP Results:</span></span>
<span data-ttu-id="18a43-628">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="18a43-628">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="18a43-629">Compilación 17046</span><span class="sxs-lookup"><span data-stu-id="18a43-629">Build 17046</span></span>

<span data-ttu-id="18a43-630">Para obtener información general de Windows sobre la compilación 17046, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span><span class="sxs-lookup"><span data-stu-id="18a43-630">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="18a43-631">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-631">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="18a43-632">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-632">WSL</span></span>
- <span data-ttu-id="18a43-633">Permite que los procesos se ejecuten sin un terminal activo.</span><span class="sxs-lookup"><span data-stu-id="18a43-633">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="18a43-634">[GH 709, 1007, 1511, 2252, 2391, etc.]</span><span class="sxs-lookup"><span data-stu-id="18a43-634">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="18a43-635">Mejor compatibilidad con CLONE_VFORK y CLONE_VM.</span><span class="sxs-lookup"><span data-stu-id="18a43-635">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="18a43-636">[GH 1878, 2615]</span><span class="sxs-lookup"><span data-stu-id="18a43-636">[GH 1878, 2615]</span></span>
- <span data-ttu-id="18a43-637">Omite los controladores de filtro TDI para las operaciones de red de WSL.</span><span class="sxs-lookup"><span data-stu-id="18a43-637">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="18a43-638">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="18a43-638">[GH 1554]</span></span>
- <span data-ttu-id="18a43-639">DrvFs crea vínculos simbólicos de NT cuando se cumplen determinadas condiciones.</span><span class="sxs-lookup"><span data-stu-id="18a43-639">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="18a43-640">[GH 353, 1475, 2602]</span><span class="sxs-lookup"><span data-stu-id="18a43-640">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="18a43-641">El destino del vínculo debe ser relativo, no debe cruzar ningún punto de montaje ni vínculo simbólico, y debe existir.</span><span class="sxs-lookup"><span data-stu-id="18a43-641">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="18a43-642">El usuario debe tener SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (esto normalmente requiere que inicies wsl.exe con privilegios elevados), a menos que esté activado el modo de desarrollador.</span><span class="sxs-lookup"><span data-stu-id="18a43-642">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="18a43-643">En todas las demás situaciones, DrvFs todavía crea vínculos simbólicos de WSL.</span><span class="sxs-lookup"><span data-stu-id="18a43-643">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="18a43-644">Permite ejecutar instancias de WSL con privilegios elevados y no elevados simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="18a43-644">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="18a43-645">Compatibilidad con /proc/sys/kernel/yama/ptrace_scope</span><span class="sxs-lookup"><span data-stu-id="18a43-645">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="18a43-646">Agrega wslpath para realizar conversiones de rutas de acceso de WSL<->Windows.</span><span class="sxs-lookup"><span data-stu-id="18a43-646">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="18a43-647">[GH 522, 1243, 1834, 2327, etc.]</span><span class="sxs-lookup"><span data-stu-id="18a43-647">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a><span data-ttu-id="18a43-648">Console</span><span class="sxs-lookup"><span data-stu-id="18a43-648">Console</span></span>
- <span data-ttu-id="18a43-649">Sin correcciones.</span><span class="sxs-lookup"><span data-stu-id="18a43-649">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-650">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-650">LTP Results:</span></span>
<span data-ttu-id="18a43-651">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="18a43-651">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="18a43-652">Compilación 17040</span><span class="sxs-lookup"><span data-stu-id="18a43-652">Build 17040</span></span>

<span data-ttu-id="18a43-653">Para obtener información general de Windows sobre la compilación 17040, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span><span class="sxs-lookup"><span data-stu-id="18a43-653">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-654">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-654">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="18a43-655">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-655">WSL</span></span>
- <span data-ttu-id="18a43-656">No hay correcciones desde 17035.</span><span class="sxs-lookup"><span data-stu-id="18a43-656">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="18a43-657">Console</span><span class="sxs-lookup"><span data-stu-id="18a43-657">Console</span></span>
- <span data-ttu-id="18a43-658">No hay correcciones desde 17035.</span><span class="sxs-lookup"><span data-stu-id="18a43-658">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-659">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-659">LTP Results:</span></span>
<span data-ttu-id="18a43-660">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="18a43-660">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="18a43-661">Compilación 17035</span><span class="sxs-lookup"><span data-stu-id="18a43-661">Build 17035</span></span>

<span data-ttu-id="18a43-662">Para obtener información general de Windows sobre la compilación 17035, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span><span class="sxs-lookup"><span data-stu-id="18a43-662">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-663">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-663">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="18a43-664">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-664">WSL</span></span>
- <span data-ttu-id="18a43-665">En ocasiones, el acceso a los archivos de DrvFs puede producir errores con EINVAL.</span><span class="sxs-lookup"><span data-stu-id="18a43-665">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="18a43-666">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="18a43-666">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="18a43-667">Console</span><span class="sxs-lookup"><span data-stu-id="18a43-667">Console</span></span>
- <span data-ttu-id="18a43-668">Algo de pérdida de color al insertar o eliminar líneas en modo VT.</span><span class="sxs-lookup"><span data-stu-id="18a43-668">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-669">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-669">LTP Results:</span></span>
<span data-ttu-id="18a43-670">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="18a43-670">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="18a43-671">Compilación 17025</span><span class="sxs-lookup"><span data-stu-id="18a43-671">Build 17025</span></span>

<span data-ttu-id="18a43-672">Para obtener información general de Windows sobre la compilación 17025, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span><span class="sxs-lookup"><span data-stu-id="18a43-672">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-673">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-673">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="18a43-674">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-674">WSL</span></span>
- <span data-ttu-id="18a43-675">Inicia procesos iniciales en un nuevo grupo de procesos en primer plano [GH 1653, 2510].</span><span class="sxs-lookup"><span data-stu-id="18a43-675">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="18a43-676">Correcciones de entrega de SIGHUP [GH 2496].</span><span class="sxs-lookup"><span data-stu-id="18a43-676">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="18a43-677">Genera un nombre de puente virtual predeterminado si no se proporciona ninguno [GH 2497].</span><span class="sxs-lookup"><span data-stu-id="18a43-677">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="18a43-678">Implementa /proc/sys/kernel/random/boot_id [GH 2518].</span><span class="sxs-lookup"><span data-stu-id="18a43-678">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="18a43-679">Más correcciones de la canalización stdout/stderr de interoperabilidad.</span><span class="sxs-lookup"><span data-stu-id="18a43-679">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="18a43-680">Llamada del sistema syncfs de código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="18a43-680">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="18a43-681">Console</span><span class="sxs-lookup"><span data-stu-id="18a43-681">Console</span></span>
- <span data-ttu-id="18a43-682">Corrección de la traducción de VT de entrada para consolas de terceros [GH 111]</span><span class="sxs-lookup"><span data-stu-id="18a43-682">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-683">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-683">LTP Results:</span></span>
<span data-ttu-id="18a43-684">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="18a43-684">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="18a43-685">Compilación 17017</span><span class="sxs-lookup"><span data-stu-id="18a43-685">Build 17017</span></span>

<span data-ttu-id="18a43-686">Para obtener información general de Windows sobre la compilación 17017, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span><span class="sxs-lookup"><span data-stu-id="18a43-686">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-687">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-687">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="18a43-688">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-688">WSL</span></span>
- <span data-ttu-id="18a43-689">Omite los encabezados de programa ELF vacíos [GH 330].</span><span class="sxs-lookup"><span data-stu-id="18a43-689">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="18a43-690">Permite que LxssManager cree instancias de WSL para usuarios no interactivos (compatibilidad con ssh y tareas programadas) [GH 777, 1602].</span><span class="sxs-lookup"><span data-stu-id="18a43-690">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="18a43-691">Compatibilidad con escenarios de WSL->Win32->WSL ("inicio") [GH 1228].</span><span class="sxs-lookup"><span data-stu-id="18a43-691">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="18a43-692">Compatibilidad limitada para la terminación de las aplicaciones de consola que se invocan a través de la interoperabilidad [GH 1614].</span><span class="sxs-lookup"><span data-stu-id="18a43-692">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="18a43-693">Compatibilidad con las opciones de montaje para devpts [GH 1948].</span><span class="sxs-lookup"><span data-stu-id="18a43-693">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="18a43-694">Inicio de bloqueo secundario de Ptrace [GH 2333].</span><span class="sxs-lookup"><span data-stu-id="18a43-694">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="18a43-695">Faltan algunos eventos de EPOLLET [GH 2462].</span><span class="sxs-lookup"><span data-stu-id="18a43-695">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="18a43-696">Devuelve más datos para PTRACE_GETSIGINFO.</span><span class="sxs-lookup"><span data-stu-id="18a43-696">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="18a43-697">Getdents con lseek proporciona resultados incorrectos.</span><span class="sxs-lookup"><span data-stu-id="18a43-697">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="18a43-698">Corrección de algunos bloqueos de la aplicación de interoperabilidad de Win32, en espera de la entrada en una canalización que no tiene más datos.</span><span class="sxs-lookup"><span data-stu-id="18a43-698">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="18a43-699">Compatibilidad de O_ASYNC con archivos tty/pty.</span><span class="sxs-lookup"><span data-stu-id="18a43-699">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="18a43-700">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-700">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="18a43-701">Console</span><span class="sxs-lookup"><span data-stu-id="18a43-701">Console</span></span>
- <span data-ttu-id="18a43-702">No hay cambios relacionados con la consola en esta versión.</span><span class="sxs-lookup"><span data-stu-id="18a43-702">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-703">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-703">LTP Results:</span></span>
<span data-ttu-id="18a43-704">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="18a43-704">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="18a43-705">Actualización Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="18a43-705">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="18a43-706">Compilación 16288</span><span class="sxs-lookup"><span data-stu-id="18a43-706">Build 16288</span></span>

<span data-ttu-id="18a43-707">Para obtener información general de Windows sobre la compilación 16288, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span><span class="sxs-lookup"><span data-stu-id="18a43-707">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-708">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-708">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="18a43-709">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-709">WSL</span></span>
- <span data-ttu-id="18a43-710">Inicializa y notifica correctamente uid, gid y mode para los descriptores de archivo de socket [GH 2490]</span><span class="sxs-lookup"><span data-stu-id="18a43-710">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="18a43-711">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-711">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="18a43-712">Console</span><span class="sxs-lookup"><span data-stu-id="18a43-712">Console</span></span>
- <span data-ttu-id="18a43-713">No hay cambios relacionados con la consola en esta versión.</span><span class="sxs-lookup"><span data-stu-id="18a43-713">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-714">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-714">LTP Results:</span></span>
<span data-ttu-id="18a43-715">Sin cambios desde 16273</span><span class="sxs-lookup"><span data-stu-id="18a43-715">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="18a43-716">Compilación 16278</span><span class="sxs-lookup"><span data-stu-id="18a43-716">Build 16278</span></span>

<span data-ttu-id="18a43-717">Para obtener información general de Windows sobre la compilación 162738, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span><span class="sxs-lookup"><span data-stu-id="18a43-717">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-718">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-718">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="18a43-719">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-719">WSL</span></span>
- <span data-ttu-id="18a43-720">Anula explícitamente la asignación de las vistas asignadas de secciones basadas en archivos al anular el estado de LX MM [GH 2415]</span><span class="sxs-lookup"><span data-stu-id="18a43-720">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="18a43-721">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-721">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="18a43-722">Console</span><span class="sxs-lookup"><span data-stu-id="18a43-722">Console</span></span>
- <span data-ttu-id="18a43-723">No hay cambios relacionados con la consola en esta versión.</span><span class="sxs-lookup"><span data-stu-id="18a43-723">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-724">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-724">LTP Results:</span></span>
<span data-ttu-id="18a43-725">Sin cambios desde 16273</span><span class="sxs-lookup"><span data-stu-id="18a43-725">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="18a43-726">Compilación 16275</span><span class="sxs-lookup"><span data-stu-id="18a43-726">Build 16275</span></span>

<span data-ttu-id="18a43-727">Para obtener información general de Windows sobre la compilación 162735, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span><span class="sxs-lookup"><span data-stu-id="18a43-727">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-728">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-728">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="18a43-729">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-729">WSL</span></span>
- <span data-ttu-id="18a43-730">No hay cambios relacionados con WSL en esta versión.</span><span class="sxs-lookup"><span data-stu-id="18a43-730">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="18a43-731">Console</span><span class="sxs-lookup"><span data-stu-id="18a43-731">Console</span></span>
- <span data-ttu-id="18a43-732">No hay cambios relacionados con la consola en esta versión.</span><span class="sxs-lookup"><span data-stu-id="18a43-732">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-733">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-733">LTP Results:</span></span>
<span data-ttu-id="18a43-734">Sin cambios desde 16273</span><span class="sxs-lookup"><span data-stu-id="18a43-734">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="18a43-735">Compilación 16273</span><span class="sxs-lookup"><span data-stu-id="18a43-735">Build 16273</span></span>

<span data-ttu-id="18a43-736">Para obtener información general de Windows sobre la compilación 16273, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span><span class="sxs-lookup"><span data-stu-id="18a43-736">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-737">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-737">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="18a43-738">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-738">WSL</span></span>
- <span data-ttu-id="18a43-739">Se ha corregido un problema por el que DrvFs a veces indicaba un tipo de archivo incorrecto para los directorios [GH 2392]</span><span class="sxs-lookup"><span data-stu-id="18a43-739">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="18a43-740">Permite la creación de sockets NETLINK_KOBJECT_UEVENT para desbloquear programas que usan UEVENT [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span><span class="sxs-lookup"><span data-stu-id="18a43-740">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="18a43-741">Agrega compatibilidad para conexión sin bloqueo [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span><span class="sxs-lookup"><span data-stu-id="18a43-741">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="18a43-742">Implementa la marca de llamada del sistema de clon CLONE_FS [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="18a43-742">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="18a43-743">Corrección de problemas relativos a la falta de control de tabulaciones o comillas correctamente en la interoperabilidad de NT [GH 1625, 2164]</span><span class="sxs-lookup"><span data-stu-id="18a43-743">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="18a43-744">Resuelve el error de acceso denegado al intentar volver a iniciar instancias de WSL [GH 651, 2095]</span><span class="sxs-lookup"><span data-stu-id="18a43-744">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="18a43-745">Implementa las operaciones de Futex FUTEX_REQUEUE y FUTEX_CMP_REQUEUE [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="18a43-745">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="18a43-746">Corrección de permisos para varios archivos de SysFs [GH 2214]</span><span class="sxs-lookup"><span data-stu-id="18a43-746">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="18a43-747">Corrección del bloqueo de pila de Haskell durante la instalación [GH 2290]</span><span class="sxs-lookup"><span data-stu-id="18a43-747">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="18a43-748">Implementa las marcas binfmt_misc "C", "O" y "P" [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="18a43-748">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="18a43-749">Agrega /proc/sys/kernel /shmmax /shmmni y /threads-max [GH 1753]</span><span class="sxs-lookup"><span data-stu-id="18a43-749">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="18a43-750">Agrega compatibilidad parcial para la llamada del sistema ioprio_set [GH 498]</span><span class="sxs-lookup"><span data-stu-id="18a43-750">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="18a43-751">Código auxiliar SO_REUSEPORT y agrega compatibilidad para SO_PASSCRED para sockets de netlink [GH 69]</span><span class="sxs-lookup"><span data-stu-id="18a43-751">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="18a43-752">Devuelve distintos códigos de error de RegisterDistribuiton si se está instalando o desinstalando actualmente una distribución.</span><span class="sxs-lookup"><span data-stu-id="18a43-752">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="18a43-753">Permite la anulación del registro de distribuciones de WSL parcialmente instaladas a través de wslconfig.exe</span><span class="sxs-lookup"><span data-stu-id="18a43-753">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="18a43-754">Corrección de bloqueo de prueba de socket de Python desde UDP::msg_peek</span><span class="sxs-lookup"><span data-stu-id="18a43-754">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="18a43-755">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-755">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="18a43-756">Console</span><span class="sxs-lookup"><span data-stu-id="18a43-756">Console</span></span>
- <span data-ttu-id="18a43-757">No hay cambios relacionados con la consola en esta versión.</span><span class="sxs-lookup"><span data-stu-id="18a43-757">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-758">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-758">LTP Results:</span></span>
<span data-ttu-id="18a43-759">Total de pruebas: 1904</span><span class="sxs-lookup"><span data-stu-id="18a43-759">Total Tests: 1904</span></span><br/>
<span data-ttu-id="18a43-760">Total de pruebas omitidas: 209</span><span class="sxs-lookup"><span data-stu-id="18a43-760">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="18a43-761">Total de errores: 229</span><span class="sxs-lookup"><span data-stu-id="18a43-761">Total Failures: 229</span></span><br/>
[<span data-ttu-id="18a43-762">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="18a43-762">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="18a43-763">Compilación 16257</span><span class="sxs-lookup"><span data-stu-id="18a43-763">Build 16257</span></span>

<span data-ttu-id="18a43-764">Para obtener información general de Windows sobre la compilación 16257, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span><span class="sxs-lookup"><span data-stu-id="18a43-764">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-765">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-765">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="18a43-766">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-766">WSL</span></span>
- <span data-ttu-id="18a43-767">Implementa la llamada del sistema prlimit64</span><span class="sxs-lookup"><span data-stu-id="18a43-767">Implement prlimit64 system call</span></span>
- <span data-ttu-id="18a43-768">Agrega compatibilidad con ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="18a43-768">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="18a43-769">Código auxiliar de MSG_MORE para sockets TCP [GH 2351]</span><span class="sxs-lookup"><span data-stu-id="18a43-769">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="18a43-770">Corrección del comportamiento del vector auxiliar de AT_EXECFN no válido [GH 2133]</span><span class="sxs-lookup"><span data-stu-id="18a43-770">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="18a43-771">Corrección del comportamiento de copiar y pegar para consola/tty, y agrega un mejor control de búfer completo [GH 2204, 2131]</span><span class="sxs-lookup"><span data-stu-id="18a43-771">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="18a43-772">Establece AT_SECURE en vector auxiliar para los programas set-user-ID y set-group-ID [GH 2031]</span><span class="sxs-lookup"><span data-stu-id="18a43-772">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="18a43-773">El punto de conexión maestro de psuedoterminal no controla TIOCPGRP [GH 1063]</span><span class="sxs-lookup"><span data-stu-id="18a43-773">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="18a43-774">La corrección de lseek hace rebobinar directorios en LxFs [GH 2310]</span><span class="sxs-lookup"><span data-stu-id="18a43-774">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="18a43-775">/dev/ptmx se bloquea después de un uso pesado [GH 1882]</span><span class="sxs-lookup"><span data-stu-id="18a43-775">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="18a43-776">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-776">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="18a43-777">Console</span><span class="sxs-lookup"><span data-stu-id="18a43-777">Console</span></span>
- <span data-ttu-id="18a43-778">Corrección para líneas horizontales o guiones bajos en todas partes [GH 2168]</span><span class="sxs-lookup"><span data-stu-id="18a43-778">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="18a43-779">Corrección para el orden de procesamiento cambiado hace que NPM sea más difícil de cerrar [GH 2170]</span><span class="sxs-lookup"><span data-stu-id="18a43-779">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="18a43-780">Se ha agregado la nueva combinación de colores: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="18a43-780">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-781">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-781">LTP Results:</span></span>
<span data-ttu-id="18a43-782">Sin cambios desde 16251</span><span class="sxs-lookup"><span data-stu-id="18a43-782">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="18a43-783">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="18a43-783">Syscall Support</span></span>
<span data-ttu-id="18a43-784">A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="18a43-784">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="18a43-785">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="18a43-785">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="18a43-786">Problemas conocidos</span><span class="sxs-lookup"><span data-stu-id="18a43-786">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[<span data-ttu-id="18a43-787">Problema de GitHub 2392: WSL no reconoce carpetas de Windows…</span><span class="sxs-lookup"><span data-stu-id="18a43-787">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="18a43-788">En la compilación 16257, WSL tiene problemas al enumerar archivos o carpetas de Windows a través de `/mnt/c/...`.</span><span class="sxs-lookup"><span data-stu-id="18a43-788">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="18a43-789">Este problema se ha corregido y debe publicarse en la compilación de Insider durante la semana que comienza el 14/8/2017.</span><span class="sxs-lookup"><span data-stu-id="18a43-789">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="18a43-790">Compilación 16251</span><span class="sxs-lookup"><span data-stu-id="18a43-790">Build 16251</span></span>

<span data-ttu-id="18a43-791">Para obtener información general de Windows sobre la compilación 16251, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span><span class="sxs-lookup"><span data-stu-id="18a43-791">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-792">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-792">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="18a43-793">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-793">WSL</span></span>
- <span data-ttu-id="18a43-794">Quita la etiqueta beta del componente opcional de WSL, consulta la [publicación de blog](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) para más información.</span><span class="sxs-lookup"><span data-stu-id="18a43-794">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="18a43-795">Inicializa correctamente el uid y gid del conjunto guardado para los archivos binarios set-user-ID y set-group-ID en ejecución [GH 962, 1415, 2072]</span><span class="sxs-lookup"><span data-stu-id="18a43-795">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="18a43-796">Se ha agregado compatibilidad con ptrace PTRACE_O_TRACEEXIT [GH 555]</span><span class="sxs-lookup"><span data-stu-id="18a43-796">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="18a43-797">Se ha agregado compatibilidad con ptrace PTRACE_GETFPREGS y PTRACE_GETREGSET con NT_FPREGSET [GH 555]</span><span class="sxs-lookup"><span data-stu-id="18a43-797">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="18a43-798">Se ha corregido ptrace para que se detenga en las señales omitidas</span><span class="sxs-lookup"><span data-stu-id="18a43-798">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="18a43-799">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-799">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="18a43-800">Console</span><span class="sxs-lookup"><span data-stu-id="18a43-800">Console</span></span>
- <span data-ttu-id="18a43-801">No hay cambios relacionados con la consola en esta versión.</span><span class="sxs-lookup"><span data-stu-id="18a43-801">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-802">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-802">LTP Results:</span></span>
<span data-ttu-id="18a43-803">Número de pruebas superadas: 768</span><span class="sxs-lookup"><span data-stu-id="18a43-803">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="18a43-804">Número de pruebas no superadas: 244</span><span class="sxs-lookup"><span data-stu-id="18a43-804">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="18a43-805">Número de pruebas omitidas: 96</span><span class="sxs-lookup"><span data-stu-id="18a43-805">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="18a43-806">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="18a43-806">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="18a43-807">Compilación 16241</span><span class="sxs-lookup"><span data-stu-id="18a43-807">Build 16241</span></span>

<span data-ttu-id="18a43-808">Para obtener información general de Windows sobre la compilación 16241, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span><span class="sxs-lookup"><span data-stu-id="18a43-808">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-809">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-809">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="18a43-810">WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-810">WSL</span></span>
- <span data-ttu-id="18a43-811">No hay cambios relacionados con WSL en esta versión.</span><span class="sxs-lookup"><span data-stu-id="18a43-811">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="18a43-812">Console</span><span class="sxs-lookup"><span data-stu-id="18a43-812">Console</span></span>
- <span data-ttu-id="18a43-813">Corrección para la generación de un carácter equivocado para DEC de líneas cruzadas, que se notificó originalmente [aquí](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span><span class="sxs-lookup"><span data-stu-id="18a43-813">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="18a43-814">Corrección para cuando no se muestre texto de salida en la página de códigos 65001 (utf8)</span><span class="sxs-lookup"><span data-stu-id="18a43-814">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="18a43-815">No transfieras los cambios hechos en los valores RGB de un color a otras partes de la paleta en el cambio de selección.</span><span class="sxs-lookup"><span data-stu-id="18a43-815">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="18a43-816">Esto hará que la hoja de propiedades de la consola sea mucho más fácil de usar.</span><span class="sxs-lookup"><span data-stu-id="18a43-816">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="18a43-817">Ctrl+S no parece funcionar correctamente</span><span class="sxs-lookup"><span data-stu-id="18a43-817">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="18a43-818">Un-Bold/-Dim totalmente ausentes de los códigos de escape de ANSI [GH 2174]</span><span class="sxs-lookup"><span data-stu-id="18a43-818">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="18a43-819">La consola no admite correctamente los temas de color VIM [GH 1706]</span><span class="sxs-lookup"><span data-stu-id="18a43-819">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="18a43-820">No se pueden pegar caracteres determinados [GH 2149]</span><span class="sxs-lookup"><span data-stu-id="18a43-820">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="18a43-821">El cambio de tamaño de reflujo interactúa de forma extraña con el cambio de tamaño de una ventana de Bash cuando el contenido está en la línea de comandos/edición [GH ConEmu 1123]</span><span class="sxs-lookup"><span data-stu-id="18a43-821">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="18a43-822">Ctrl-L deja la pantalla desfasada [GH 1978]</span><span class="sxs-lookup"><span data-stu-id="18a43-822">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="18a43-823">Error de representación de consola al mostrar VT en HDPI [GH 1907]</span><span class="sxs-lookup"><span data-stu-id="18a43-823">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="18a43-824">Los caracteres Japansese parecen extraños con el carácter Unicode U+30FB [GH 2146]</span><span class="sxs-lookup"><span data-stu-id="18a43-824">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="18a43-825">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-825">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="18a43-826">Compilación 16237</span><span class="sxs-lookup"><span data-stu-id="18a43-826">Build 16237</span></span>

<span data-ttu-id="18a43-827">Para obtener información general de Windows sobre la compilación 16237, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span><span class="sxs-lookup"><span data-stu-id="18a43-827">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-828">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-828">Fixed</span></span>
- <span data-ttu-id="18a43-829">Usa atributos predeterminados para archivos sin EA en lxfs (root, root, 0000)</span><span class="sxs-lookup"><span data-stu-id="18a43-829">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="18a43-830">Se ha agregado compatibilidad para distribuciones que usan atributos extendidos</span><span class="sxs-lookup"><span data-stu-id="18a43-830">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="18a43-831">Corrección del relleno de las entradas devueltas por getdents y getdents64</span><span class="sxs-lookup"><span data-stu-id="18a43-831">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="18a43-832">Corrección de la comprobación de permisos para la llamada del sistema shmctl SHM_STAT [GH 2068]</span><span class="sxs-lookup"><span data-stu-id="18a43-832">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="18a43-833">Se ha corregido el estado inicial incorrecto de epoll para ttys [GH 2231]</span><span class="sxs-lookup"><span data-stu-id="18a43-833">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="18a43-834">Corrección de readdir de DrvFs que no devuelve todas las entradas [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="18a43-834">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="18a43-835">Corrección de readdir de LxFs cuando los archivos están desvinculados [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="18a43-835">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="18a43-836">Permite que los archivos drvfs no vinculados se vuelvan a abrir a través de procfs</span><span class="sxs-lookup"><span data-stu-id="18a43-836">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="18a43-837">Se ha agregado la invalidación de la clave del Registro global para deshabilitar las características de WSL (interoperabilidad/montaje de unidades)</span><span class="sxs-lookup"><span data-stu-id="18a43-837">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="18a43-838">Corrección del recuento incorrecto de bloques en "stat" para DrvFs (y LxFs) [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="18a43-838">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="18a43-839">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-839">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="18a43-840">Compilación 16232</span><span class="sxs-lookup"><span data-stu-id="18a43-840">Build 16232</span></span>

<span data-ttu-id="18a43-841">Para obtener información general de Windows sobre la compilación 16232, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span><span class="sxs-lookup"><span data-stu-id="18a43-841">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-842">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-842">Fixed</span></span>
- <span data-ttu-id="18a43-843">No hay cambios relacionados con WSL en esta versión.</span><span class="sxs-lookup"><span data-stu-id="18a43-843">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="18a43-844">Compilación 16226</span><span class="sxs-lookup"><span data-stu-id="18a43-844">Build 16226</span></span>

<span data-ttu-id="18a43-845">Para obtener información general de Windows sobre la compilación 16226, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span><span class="sxs-lookup"><span data-stu-id="18a43-845">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-846">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-846">Fixed</span></span>
- <span data-ttu-id="18a43-847">Compatibilidad con llamadas del sistema relacionadas con xattr (getxattr, setxattr, listxattr, removexattr).</span><span class="sxs-lookup"><span data-stu-id="18a43-847">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="18a43-848">Compatibilidad con security.capablity xattr.</span><span class="sxs-lookup"><span data-stu-id="18a43-848">security.capablity xattr support.</span></span>
- <span data-ttu-id="18a43-849">Compatibilidad mejorada con determinados sistemas de archivos y filtros, incluidos los servidores SMB que no son de MS.</span><span class="sxs-lookup"><span data-stu-id="18a43-849">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="18a43-850">[GH 1952]</span><span class="sxs-lookup"><span data-stu-id="18a43-850">[GH #1952]</span></span>
- <span data-ttu-id="18a43-851">Compatibilidad mejorada para los marcadores de posición de OneDrive, los marcadores de posición de GVFS y los archivos comprimidos del sistema operativo compacto.</span><span class="sxs-lookup"><span data-stu-id="18a43-851">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="18a43-852">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-852">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="18a43-853">Compilación 16215</span><span class="sxs-lookup"><span data-stu-id="18a43-853">Build 16215</span></span>

<span data-ttu-id="18a43-854">Para obtener información general de Windows sobre la compilación 16215, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span><span class="sxs-lookup"><span data-stu-id="18a43-854">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-855">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-855">Fixed</span></span>
- <span data-ttu-id="18a43-856">WSL ya no requiere el modo de desarrollador.</span><span class="sxs-lookup"><span data-stu-id="18a43-856">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="18a43-857">Compatibilidad con uniones de directorios en drvfs.</span><span class="sxs-lookup"><span data-stu-id="18a43-857">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="18a43-858">Controla la desinstalación de paquetes appx de distribución de WSL.</span><span class="sxs-lookup"><span data-stu-id="18a43-858">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="18a43-859">Actualiza procfs para mostrar las asignaciones privadas y compartidas.</span><span class="sxs-lookup"><span data-stu-id="18a43-859">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="18a43-860">Agrega la capacidad de wslconfig.exe de limpiar las distribuciones que están parcialmente instaladas o desinstaladas.</span><span class="sxs-lookup"><span data-stu-id="18a43-860">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="18a43-861">Se ha agregado compatibilidad para IP_MTU_DISCOVER para sockets TCP.</span><span class="sxs-lookup"><span data-stu-id="18a43-861">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="18a43-862">[GH 1639, 2115, 2205]</span><span class="sxs-lookup"><span data-stu-id="18a43-862">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="18a43-863">Inferencia de la familia de protocolos para rutas a AF_INADDR.</span><span class="sxs-lookup"><span data-stu-id="18a43-863">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="18a43-864">Mejoras en los dispositivos serie [GH 1929].</span><span class="sxs-lookup"><span data-stu-id="18a43-864">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="18a43-865">Compilación 16199</span><span class="sxs-lookup"><span data-stu-id="18a43-865">Build 16199</span></span>

<span data-ttu-id="18a43-866">Para obtener información general de Windows sobre la compilación 16199, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span><span class="sxs-lookup"><span data-stu-id="18a43-866">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-867">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-867">Fixed</span></span>
- <span data-ttu-id="18a43-868">No hay cambios relacionados con WSL en estas versiones.</span><span class="sxs-lookup"><span data-stu-id="18a43-868">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="18a43-869">Compilación 16193</span><span class="sxs-lookup"><span data-stu-id="18a43-869">Build 16193</span></span>

<span data-ttu-id="18a43-870">Para obtener información general de Windows sobre la compilación 16193, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span><span class="sxs-lookup"><span data-stu-id="18a43-870">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-871">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-871">Fixed</span></span>
- <span data-ttu-id="18a43-872">Condición de carrera entre el envío de SIGCONT y un grupo de subprocesos de terminación [GH 1973]</span><span class="sxs-lookup"><span data-stu-id="18a43-872">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="18a43-873">Cambia dispositivos tty y pty para notificar FILE_DEVICE_NAMED_PIPE en lugar de FILE_DEVICE_CONSOLE [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="18a43-873">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="18a43-874">Corrección de SSH para IP_OPTIONS</span><span class="sxs-lookup"><span data-stu-id="18a43-874">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="18a43-875">Se ha cambiado el montaje de DrvFs al demonio de inicialización [GH 1862, 1968, 1767, 1933]</span><span class="sxs-lookup"><span data-stu-id="18a43-875">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="18a43-876">Se ha agregado compatibilidad en DrvFs para los siguientes vínculos simbólicos de NT.</span><span class="sxs-lookup"><span data-stu-id="18a43-876">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="18a43-877">Compilación 16184</span><span class="sxs-lookup"><span data-stu-id="18a43-877">Build 16184</span></span>

<span data-ttu-id="18a43-878">Para obtener información general de Windows sobre la compilación 16184, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span><span class="sxs-lookup"><span data-stu-id="18a43-878">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-879">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-879">Fixed</span></span>
- <span data-ttu-id="18a43-880">Se ha quitado la tarea de mantenimiento de paquetes APT (lxrun.exe /update)</span><span class="sxs-lookup"><span data-stu-id="18a43-880">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="18a43-881">Se ha corregido la salida que no se muestra en los procesos de Windows en node.js [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="18a43-881">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="18a43-882">Relaja los requisitos de alineación en lxcore [GH 1794]</span><span class="sxs-lookup"><span data-stu-id="18a43-882">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="18a43-883">Se ha corregido el control de la marca AT_EMPTY_PATH en un número de llamadas del sistema.</span><span class="sxs-lookup"><span data-stu-id="18a43-883">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="18a43-884">Se ha corregido el problema por el que la eliminación de archivos DrvFs con identificadores abiertos hace que el archivo muestre un comportamiento indefinido [GH 544, 966, 1357, 1535, 1615]</span><span class="sxs-lookup"><span data-stu-id="18a43-884">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="18a43-885">/etc/hosts heredará ahora entradas del archivo de hosts de Windows (%windir%\system32\drivers\etc\hosts) [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="18a43-885">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="18a43-886">Compilación 16179</span><span class="sxs-lookup"><span data-stu-id="18a43-886">Build 16179</span></span>

<span data-ttu-id="18a43-887">Para obtener información general de Windows sobre la compilación 16179, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span><span class="sxs-lookup"><span data-stu-id="18a43-887">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-888">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-888">Fixed</span></span>
- <span data-ttu-id="18a43-889">Sin cambios en WSL esta semana.</span><span class="sxs-lookup"><span data-stu-id="18a43-889">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="18a43-890">Compilación 16176</span><span class="sxs-lookup"><span data-stu-id="18a43-890">Build 16176</span></span>

<span data-ttu-id="18a43-891">Para obtener información general de Windows sobre la compilación 16176, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span><span class="sxs-lookup"><span data-stu-id="18a43-891">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-892">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-892">Fixed</span></span>

- [<span data-ttu-id="18a43-893">Se ha habilitado la compatibilidad serie</span><span class="sxs-lookup"><span data-stu-id="18a43-893">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="18a43-894">Se ha agregado la opción de socket de IP IP_OPTIONS [GH 1116]</span><span class="sxs-lookup"><span data-stu-id="18a43-894">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="18a43-895">Se ha implementado la función pwritev (al cargar el archivo en nginx/PHP-FPM) [GH 1506]</span><span class="sxs-lookup"><span data-stu-id="18a43-895">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="18a43-896">Se han agregado opciones de socket IP IP_MULTICAST_IF e IPV6_MULTICAST_IF [GH 990]</span><span class="sxs-lookup"><span data-stu-id="18a43-896">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="18a43-897">Compatibilidad con la opción de socket IP_MULTICAST_LOOP e IPV6_MULTICAST_LOOP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="18a43-897">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="18a43-898">Se ha agregado la opción de socket IP(V6)_MTU para el nodo de aplicaciones, traceroute, dig, nslookup, host</span><span class="sxs-lookup"><span data-stu-id="18a43-898">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="18a43-899">Se ha agregado la opción de socket de IP IPV6_UNICAST_HOPS</span><span class="sxs-lookup"><span data-stu-id="18a43-899">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="18a43-900">Mejoras del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="18a43-900">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="18a43-901">Permite el montaje de rutas UNC</span><span class="sxs-lookup"><span data-stu-id="18a43-901">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="18a43-902">Habilita la compatibilidad con CDFS en drvfs</span><span class="sxs-lookup"><span data-stu-id="18a43-902">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="18a43-903">Controla correctamente los permisos para los sistemas de archivos de red en drvfs</span><span class="sxs-lookup"><span data-stu-id="18a43-903">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="18a43-904">Agrega compatibilidad para unidades remotas a drvfs</span><span class="sxs-lookup"><span data-stu-id="18a43-904">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="18a43-905">Habilita la compatibilidad con CDFS en drvfs</span><span class="sxs-lookup"><span data-stu-id="18a43-905">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="18a43-906">Mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-906">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-907">Resultados de LTP</span><span class="sxs-lookup"><span data-stu-id="18a43-907">LTP Results</span></span>
<span data-ttu-id="18a43-908">Sin cambios desde 15042</span><span class="sxs-lookup"><span data-stu-id="18a43-908">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="18a43-909">Compilación 16170</span><span class="sxs-lookup"><span data-stu-id="18a43-909">Build 16170</span></span>

<span data-ttu-id="18a43-910">Para obtener información general de Windows sobre la compilación 16170, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span><span class="sxs-lookup"><span data-stu-id="18a43-910">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="18a43-911">Hemos lanzado una nueva [publicación de blog](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) en la que se describen nuestros esfuerzos para probar WSL.</span><span class="sxs-lookup"><span data-stu-id="18a43-911">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="18a43-912">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-912">Fixed</span></span>

- <span data-ttu-id="18a43-913">Compatibilidad para la opción de socket IP_ADD_MEMBERSHIP y IPV6_ADD_MEMBERSHIP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="18a43-913">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="18a43-914">Agrega compatibilidad para PTRACE_OLDSETOPTIONS.</span><span class="sxs-lookup"><span data-stu-id="18a43-914">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="18a43-915">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="18a43-915">[GH 1692]</span></span>
- <span data-ttu-id="18a43-916">Mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-916">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-917">Resultados de LTP</span><span class="sxs-lookup"><span data-stu-id="18a43-917">LTP Results</span></span>
<span data-ttu-id="18a43-918">Sin cambios desde 15042</span><span class="sxs-lookup"><span data-stu-id="18a43-918">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="18a43-919">Compilación 15046 a Windows 10 Creators Update</span><span class="sxs-lookup"><span data-stu-id="18a43-919">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="18a43-920">No hay más correcciones o características de WSL planeadas para su inclusión en Windows 10 Creators Update.</span><span class="sxs-lookup"><span data-stu-id="18a43-920">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="18a43-921">Las notas de la versión de WSL se reanudarán en las próximas semanas para las adiciones destinadas a la siguiente actualización principal de Windows.</span><span class="sxs-lookup"><span data-stu-id="18a43-921">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="18a43-922">Para obtener información general de Windows sobre la compilación 15046 y futuras publicaciones de Insider, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span><span class="sxs-lookup"><span data-stu-id="18a43-922">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="18a43-923">Compilación 15042</span><span class="sxs-lookup"><span data-stu-id="18a43-923">Build 15042</span></span>

<span data-ttu-id="18a43-924">Para obtener información general de Windows sobre la compilación 15042, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span><span class="sxs-lookup"><span data-stu-id="18a43-924">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-925">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-925">Fixed</span></span>

- <span data-ttu-id="18a43-926">Corrección para un interbloqueo al quitar una ruta de acceso que termina en ".."</span><span class="sxs-lookup"><span data-stu-id="18a43-926">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="18a43-927">Se ha corregido un problema por el que FIONBIO no devuelve 0 en caso correcto [GH 1683]</span><span class="sxs-lookup"><span data-stu-id="18a43-927">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="18a43-928">Se ha corregido un problema con lecturas de longitud cero de sockets de datagramas de inet</span><span class="sxs-lookup"><span data-stu-id="18a43-928">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="18a43-929">Corrección del posible interbloqueo debido a la condición de carrera en la búsqueda de inode de drvfs [GH 1675]</span><span class="sxs-lookup"><span data-stu-id="18a43-929">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="18a43-930">Se ha ampliado la compatibilidad con los datos suplementarios de los sockets de Unix; SCM_CREDENTIALS y SCM_RIGHTS [GH 514, 613, 1326]</span><span class="sxs-lookup"><span data-stu-id="18a43-930">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="18a43-931">Mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-931">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-932">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-932">LTP Results:</span></span>
<span data-ttu-id="18a43-933">Número de pruebas superadas: 737</span><span class="sxs-lookup"><span data-stu-id="18a43-933">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="18a43-934">Número de no superadas (error, omitidas, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="18a43-934">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="18a43-935">Compilación 15031</span><span class="sxs-lookup"><span data-stu-id="18a43-935">Build 15031</span></span>

<span data-ttu-id="18a43-936">Para obtener información general de Windows sobre la compilación 15031, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span><span class="sxs-lookup"><span data-stu-id="18a43-936">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-937">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-937">Fixed</span></span>

- <span data-ttu-id="18a43-938">Se ha corregido un error en el que el time(2) se comportaba incorrectamente de manera esporádica.</span><span class="sxs-lookup"><span data-stu-id="18a43-938">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="18a43-939">Se ha corregido un problema donde las llamadas del sistema de \*SIGPROCMASK podían dañar la máscara de señal.</span><span class="sxs-lookup"><span data-stu-id="18a43-939">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="18a43-940">Ahora, devuelva la longitud completa de la línea de comandos en la notificación de creación del proceso de WSL.</span><span class="sxs-lookup"><span data-stu-id="18a43-940">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="18a43-941">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="18a43-941">[GH 1632]</span></span>
- <span data-ttu-id="18a43-942">WSL ahora informa de la salida del subproceso a través de ptrace para bloqueos de GDB.</span><span class="sxs-lookup"><span data-stu-id="18a43-942">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="18a43-943">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="18a43-943">[GH 1196]</span></span>
- <span data-ttu-id="18a43-944">Se ha corregido un error en el que ptys se bloqueaba después de una gran E/S de tmux</span><span class="sxs-lookup"><span data-stu-id="18a43-944">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="18a43-945">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="18a43-945">[GH 1358]</span></span>
- <span data-ttu-id="18a43-946">Se ha corregido la validación del tiempo de espera en muchas llamadas del sistema (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span><span class="sxs-lookup"><span data-stu-id="18a43-946">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="18a43-947">Se ha agregado compatibilidad con eventfd EFD_SEMAPHORE [GH 452]</span><span class="sxs-lookup"><span data-stu-id="18a43-947">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="18a43-948">Mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-948">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-949">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-949">LTP Results:</span></span>
<span data-ttu-id="18a43-950">Número de pruebas superadas: 737</span><span class="sxs-lookup"><span data-stu-id="18a43-950">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="18a43-951">Número de no superadas (error, omitidas, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="18a43-951">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="18a43-952">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="18a43-952">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="18a43-953">Compilación 15025</span><span class="sxs-lookup"><span data-stu-id="18a43-953">Build 15025</span></span>

<span data-ttu-id="18a43-954">Para obtener información general de Windows sobre la compilación 15025, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span><span class="sxs-lookup"><span data-stu-id="18a43-954">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-955">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-955">Fixed</span></span>

- <span data-ttu-id="18a43-956">Corrección del error que dañó grep 2.27 [GH 1578]</span><span class="sxs-lookup"><span data-stu-id="18a43-956">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="18a43-957">Se ha implementado la marca EFD_SEMAPHORE para la llamada del sistema eventfd2 [GH 452]</span><span class="sxs-lookup"><span data-stu-id="18a43-957">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="18a43-958">Se ha implementado /proc/[pid]/net/ipv6_route [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="18a43-958">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="18a43-959">Compatibilidad de E/S controlada por señal para sockets de secuencia de Unix [GH 393, 68]</span><span class="sxs-lookup"><span data-stu-id="18a43-959">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="18a43-960">Compatibilidad con F_GETPIPE_SZ y F_SETPIPE_SZ [GH 1012]</span><span class="sxs-lookup"><span data-stu-id="18a43-960">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="18a43-961">Implementa la llamada del sistema recvmmsg() [GH 1531]</span><span class="sxs-lookup"><span data-stu-id="18a43-961">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="18a43-962">Se ha corregido un error en el que epoll_wait() no esperaba [GH 1609]</span><span class="sxs-lookup"><span data-stu-id="18a43-962">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="18a43-963">Implementa /proc/version_signature</span><span class="sxs-lookup"><span data-stu-id="18a43-963">Implement /proc/version_signature</span></span>
- <span data-ttu-id="18a43-964">La llamada del sistema Tee ahora devuelve un error si ambos descriptores de archivo hacen referencia a la misma canalización</span><span class="sxs-lookup"><span data-stu-id="18a43-964">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="18a43-965">Se ha implementado el comportamiento correcto de SO_PEERCRED para sockets de Unix</span><span class="sxs-lookup"><span data-stu-id="18a43-965">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="18a43-966">Se ha corregido el control de parámetros no válidos de llamada del sistema tkill</span><span class="sxs-lookup"><span data-stu-id="18a43-966">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="18a43-967">Cambios para aumentar el rendimiento de drvfs</span><span class="sxs-lookup"><span data-stu-id="18a43-967">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="18a43-968">Corrección menor para el bloqueo de E/S de Ruby</span><span class="sxs-lookup"><span data-stu-id="18a43-968">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="18a43-969">Se ha corregido recvmsg() que devuelve EINVAL para la marca MSG_DONTWAIT para sockets inet [GH 1296]</span><span class="sxs-lookup"><span data-stu-id="18a43-969">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="18a43-970">Mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-970">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-971">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-971">LTP Results:</span></span>
<span data-ttu-id="18a43-972">Número de pruebas superadas: 732</span><span class="sxs-lookup"><span data-stu-id="18a43-972">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="18a43-973">Número de no superadas (error, omitidas, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="18a43-973">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="18a43-974">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="18a43-974">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="18a43-975">Compilación 15019</span><span class="sxs-lookup"><span data-stu-id="18a43-975">Build 15019</span></span>

<span data-ttu-id="18a43-976">Para obtener información general de Windows sobre la compilación 15019, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span><span class="sxs-lookup"><span data-stu-id="18a43-976">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-977">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-977">Fixed</span></span>

- <span data-ttu-id="18a43-978">Se ha corregido un error que informaba incorrectamente del uso de CPU en procfs para herramientas como htop (GH 823, 945, 971)</span><span class="sxs-lookup"><span data-stu-id="18a43-978">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="18a43-979">Al llamar a open() con O_TRUNC en un archivo existente inotify ahora genera IN_MODIFY antes de IN_OPEN</span><span class="sxs-lookup"><span data-stu-id="18a43-979">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="18a43-980">Correcciones para el SO_ERROR de sockets de Unix getsockopt para habilitar postgress [GH 61, 1354]</span><span class="sxs-lookup"><span data-stu-id="18a43-980">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="18a43-981">Implementa /proc/sys/net/core/somaxconn para el lenguaje GO</span><span class="sxs-lookup"><span data-stu-id="18a43-981">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="18a43-982">La tarea en segundo plano de actualización del paquete apt-get ahora se ejecuta oculta de la vista</span><span class="sxs-lookup"><span data-stu-id="18a43-982">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="18a43-983">Borra el ámbito de IPv6 localhost (error de Spring-Framework (Java)).</span><span class="sxs-lookup"><span data-stu-id="18a43-983">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="18a43-984">Mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-984">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-985">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-985">LTP Results:</span></span>
<span data-ttu-id="18a43-986">Número de pruebas superadas: 714</span><span class="sxs-lookup"><span data-stu-id="18a43-986">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="18a43-987">Número de no superadas (error, omitidas, etc.): 249</span><span class="sxs-lookup"><span data-stu-id="18a43-987">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="18a43-988">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="18a43-988">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="18a43-989">Compilación 15014</span><span class="sxs-lookup"><span data-stu-id="18a43-989">Build 15014</span></span>

<span data-ttu-id="18a43-990">Para obtener información general de Windows sobre la compilación 15014, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="18a43-990">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-991">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-991">Fixed</span></span>

- <span data-ttu-id="18a43-992">Ctrl + C ahora funciona según lo previsto</span><span class="sxs-lookup"><span data-stu-id="18a43-992">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="18a43-993">htop y ps auxw ahora muestran el uso de recursos correcto (GH 516)</span><span class="sxs-lookup"><span data-stu-id="18a43-993">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="18a43-994">Traducción básica de excepciones de NT a señales.</span><span class="sxs-lookup"><span data-stu-id="18a43-994">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="18a43-995">(GH 513)</span><span class="sxs-lookup"><span data-stu-id="18a43-995">(GH #513)</span></span>
- <span data-ttu-id="18a43-996">fallocate ahora genera el error ENOSPC cuando se está quedando sin espacio en lugar de EINVAL (GH 1571)</span><span class="sxs-lookup"><span data-stu-id="18a43-996">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="18a43-997">Se ha agregado/proc/sys/kernel/sem.</span><span class="sxs-lookup"><span data-stu-id="18a43-997">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="18a43-998">Se han implementado las llamadas del sistema semop y semtimedop</span><span class="sxs-lookup"><span data-stu-id="18a43-998">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="18a43-999">Se han corregido errores de nslookup con la opción de socket IP_RECVTOS e IPV6_RECVTCLASS (GH 69)</span><span class="sxs-lookup"><span data-stu-id="18a43-999">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="18a43-1000">Compatibilidad con las opciones de socket IP_RECVTTL e IPV6_RECVHOPLIMIT</span><span class="sxs-lookup"><span data-stu-id="18a43-1000">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="18a43-1001">Mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-1001">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-1002">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-1002">LTP Results:</span></span>
<span data-ttu-id="18a43-1003">Número de pruebas superadas: 709</span><span class="sxs-lookup"><span data-stu-id="18a43-1003">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="18a43-1004">Número de no superadas (error, omitidas, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="18a43-1004">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="18a43-1005">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="18a43-1005">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="18a43-1006">Resumen de llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="18a43-1006">Syscall Summary</span></span>
<span data-ttu-id="18a43-1007">Total de llamadas del sistema: 384</span><span class="sxs-lookup"><span data-stu-id="18a43-1007">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="18a43-1008">Total implementado: 235</span><span class="sxs-lookup"><span data-stu-id="18a43-1008">Total Implemented: 235</span></span> </br>
<span data-ttu-id="18a43-1009">Total de procesos con stub: 22</span><span class="sxs-lookup"><span data-stu-id="18a43-1009">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="18a43-1010">Total no implementado: 127</span><span class="sxs-lookup"><span data-stu-id="18a43-1010">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="18a43-1011">Desglose detallado</span><span class="sxs-lookup"><span data-stu-id="18a43-1011">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="18a43-1012">Compilación 15007</span><span class="sxs-lookup"><span data-stu-id="18a43-1012">Build 15007</span></span>

<span data-ttu-id="18a43-1013">Para obtener información general de Windows sobre la compilación 15007, visita el [blog de Windows]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span><span class="sxs-lookup"><span data-stu-id="18a43-1013">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="18a43-1014">Problema conocido</span><span class="sxs-lookup"><span data-stu-id="18a43-1014">Known Issue</span></span>

- <span data-ttu-id="18a43-1015">Hay un error conocido en el que la consola no reconoce algunas entradas Ctrl + <key>.</span><span class="sxs-lookup"><span data-stu-id="18a43-1015">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="18a43-1016">Esto incluye el comando Ctrl-C, que actuará como una presión normal de "c".</span><span class="sxs-lookup"><span data-stu-id="18a43-1016">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="18a43-1017">Solución: Asigna una tecla alternativa a Ctrl+C.</span><span class="sxs-lookup"><span data-stu-id="18a43-1017">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="18a43-1018">Por ejemplo, para asignar Ctrl+K a Ctrl+C, haz lo siguiente: `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="18a43-1018">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="18a43-1019">Esta asignación es por terminal y tendrá que hacerse *cada* vez que se inicie Bash.</span><span class="sxs-lookup"><span data-stu-id="18a43-1019">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="18a43-1020">Los usuarios pueden explorar la opción para incluirlo en su `.bashrc`</span><span class="sxs-lookup"><span data-stu-id="18a43-1020">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="18a43-1021">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-1021">Fixed</span></span>

- <span data-ttu-id="18a43-1022">Se ha corregido el problema que hacía que la ejecución de WSL consumiera el 100 % de un núcleo de CPU.</span><span class="sxs-lookup"><span data-stu-id="18a43-1022">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="18a43-1023">Ahora se admite la opción de socket IP_PKTINFO, IPV6_RECVPKTINFO.</span><span class="sxs-lookup"><span data-stu-id="18a43-1023">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="18a43-1024">(GH 851, 987)</span><span class="sxs-lookup"><span data-stu-id="18a43-1024">(GH #851, 987)</span></span>
- <span data-ttu-id="18a43-1025">Trunca la dirección física de la interfaz de red a 16 bytes en lxcore (GH 1452, 1414, 1343, 468, 308)</span><span class="sxs-lookup"><span data-stu-id="18a43-1025">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="18a43-1026">Mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-1026">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-1027">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-1027">LTP Results:</span></span>
<span data-ttu-id="18a43-1028">Número de pruebas superadas: 709</span><span class="sxs-lookup"><span data-stu-id="18a43-1028">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="18a43-1029">Número de no superadas (error, omitidas, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="18a43-1029">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="18a43-1030">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="18a43-1030">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="18a43-1031">Compilación 15002</span><span class="sxs-lookup"><span data-stu-id="18a43-1031">Build 15002</span></span>

<span data-ttu-id="18a43-1032">Para obtener información general de Windows sobre la compilación 15002, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span><span class="sxs-lookup"><span data-stu-id="18a43-1032">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="18a43-1033">Problema conocido</span><span class="sxs-lookup"><span data-stu-id="18a43-1033">Known Issue</span></span>

<span data-ttu-id="18a43-1034">Dos problemas conocidos:</span><span class="sxs-lookup"><span data-stu-id="18a43-1034">Two known issues:</span></span>
- <span data-ttu-id="18a43-1035">Hay un error conocido en el que la consola no reconoce algunas entradas Ctrl + <key>.</span><span class="sxs-lookup"><span data-stu-id="18a43-1035">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="18a43-1036">Esto incluye el comando Ctrl-C, que actuará como una presión normal de "c".</span><span class="sxs-lookup"><span data-stu-id="18a43-1036">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="18a43-1037">Solución: Asigna una tecla alternativa a Ctrl+C.</span><span class="sxs-lookup"><span data-stu-id="18a43-1037">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="18a43-1038">Por ejemplo, para asignar Ctrl+K a Ctrl+C, haz lo siguiente: `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="18a43-1038">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="18a43-1039">Esta asignación es por terminal y tendrá que hacerse *cada* vez que se inicie Bash.</span><span class="sxs-lookup"><span data-stu-id="18a43-1039">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="18a43-1040">Los usuarios pueden explorar la opción para incluirlo en su `.bashrc`</span><span class="sxs-lookup"><span data-stu-id="18a43-1040">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="18a43-1041">Mientras se ejecuta WSL, un subproceso del sistema consumirá el 100 % de un núcleo de CPU.</span><span class="sxs-lookup"><span data-stu-id="18a43-1041">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="18a43-1042">La raíz de esto se ha solucionado y corregido internamente.</span><span class="sxs-lookup"><span data-stu-id="18a43-1042">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="18a43-1043">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-1043">Fixed</span></span>

- <span data-ttu-id="18a43-1044">Todas las sesiones de Bash ahora deben crearse en el mismo nivel de permiso.</span><span class="sxs-lookup"><span data-stu-id="18a43-1044">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="18a43-1045">Se bloquearán los intentos de iniciar una sesión en un nivel diferente.</span><span class="sxs-lookup"><span data-stu-id="18a43-1045">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="18a43-1046">Esto significa que las consolas de administrador y que no son de administración no se pueden ejecutarse al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="18a43-1046">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="18a43-1047">(GH 626)</span><span class="sxs-lookup"><span data-stu-id="18a43-1047">(GH #626)</span></span>
<br/>
- <span data-ttu-id="18a43-1048">Se han implementado los siguientes mensajes NETLINK_ROUTE (requiere el administrador de Windows)</span><span class="sxs-lookup"><span data-stu-id="18a43-1048">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="18a43-1049">RTM_NEWADDR (admite `ip addr add`)</span><span class="sxs-lookup"><span data-stu-id="18a43-1049">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="18a43-1050">RTM_NEWROUTE (admite `ip route add`)</span><span class="sxs-lookup"><span data-stu-id="18a43-1050">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="18a43-1051">RTM_DELADDR (admite `ip addr del`)</span><span class="sxs-lookup"><span data-stu-id="18a43-1051">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="18a43-1052">RTM_DELROUTE (admite `ip route del`)</span><span class="sxs-lookup"><span data-stu-id="18a43-1052">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="18a43-1053">La comprobación de tareas programadas para actualizar los paquetes ya no se ejecutará en una conexión de uso medido (GH 1371)</span><span class="sxs-lookup"><span data-stu-id="18a43-1053">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="18a43-1054">Se ha corregido un error en el que la canalización se bloquea, es decir, bash -c "ls -alR /" | bash -c "cat" (GH 1214)</span><span class="sxs-lookup"><span data-stu-id="18a43-1054">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="18a43-1055">Se ha implementado la opción de socket TCP_KEEPCNT (GH 843)</span><span class="sxs-lookup"><span data-stu-id="18a43-1055">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="18a43-1056">Se ha implementado la opción de socket IP_MTU_DISCOVER INET (GH 720, 717, 170, 69)</span><span class="sxs-lookup"><span data-stu-id="18a43-1056">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="18a43-1057">Se ha quitado la funcionalidad heredada para ejecutar archivos binarios de NT desde init con búsqueda de rutas de NT.</span><span class="sxs-lookup"><span data-stu-id="18a43-1057">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="18a43-1058">(GH 1325)</span><span class="sxs-lookup"><span data-stu-id="18a43-1058">(GH #1325)</span></span>
- <span data-ttu-id="18a43-1059">Corrección del modo de /dev/kmsg para permitir el acceso de lectura de grupo/otro (0644) (GH 1321)</span><span class="sxs-lookup"><span data-stu-id="18a43-1059">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="18a43-1060">Se ha implementado /proc/sys/kernel/random/boot_id [GH 1092].</span><span class="sxs-lookup"><span data-stu-id="18a43-1060">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="18a43-1061">Se ha corregido el error en el que la hora de inicio del proceso se mostraba como el año 2432 (GH 974)</span><span class="sxs-lookup"><span data-stu-id="18a43-1061">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="18a43-1062">Se ha cambiado la variable de entorno TERM predeterminada a xterm-256color (GH 1446)</span><span class="sxs-lookup"><span data-stu-id="18a43-1062">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="18a43-1063">Se ha modificado la forma en que se calcula la confirmación del proceso durante la bifurcación del proceso.</span><span class="sxs-lookup"><span data-stu-id="18a43-1063">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="18a43-1064">(GH 1286)</span><span class="sxs-lookup"><span data-stu-id="18a43-1064">(GH #1286)</span></span>
- <span data-ttu-id="18a43-1065">Se ha implementado /proc/sys/vm/overcommit_memory.</span><span class="sxs-lookup"><span data-stu-id="18a43-1065">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="18a43-1066">(GH 1286)</span><span class="sxs-lookup"><span data-stu-id="18a43-1066">(GH #1286)</span></span>
- <span data-ttu-id="18a43-1067">Se ha implementado el archivo /proc/net/route (GH 69)</span><span class="sxs-lookup"><span data-stu-id="18a43-1067">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="18a43-1068">Se ha corregido el error en el que el nombre de acceso directo se localizaba incorrectamente (GH 696)</span><span class="sxs-lookup"><span data-stu-id="18a43-1068">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="18a43-1069">Se ha corregido la lógica de análisis de elf que valida incorrectamente los encabezados de programa debe ser menor que (o igual a) PATH_MAX.</span><span class="sxs-lookup"><span data-stu-id="18a43-1069">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="18a43-1070">(GH 1048)</span><span class="sxs-lookup"><span data-stu-id="18a43-1070">(GH #1048)</span></span>
- <span data-ttu-id="18a43-1071">Se ha implementado la devolución de llamada de statfs para procfs, sysfs, cgroupfs y binfmtfs (GH 1378)</span><span class="sxs-lookup"><span data-stu-id="18a43-1071">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="18a43-1072">Se han corregido ventanas de AptPackageIndexUpdate que no se cierran (GH 1184, también se describe en GH 1193).</span><span class="sxs-lookup"><span data-stu-id="18a43-1072">Fixed AptPackageIndexUpdate windows that won’t close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="18a43-1073">Se ha agregado compatibilidad con la personalidad de ASLR ADDR_NO_RANDOMIZE.</span><span class="sxs-lookup"><span data-stu-id="18a43-1073">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="18a43-1074">(GH 1148, 1128)</span><span class="sxs-lookup"><span data-stu-id="18a43-1074">(GH #1148, 1128)</span></span>
- <span data-ttu-id="18a43-1075">Se han mejorado PTRACE_GETSIGINFO, SIGSEGV para los seguimientos de la pila gdb adecuados durante AV (GH 875)</span><span class="sxs-lookup"><span data-stu-id="18a43-1075">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="18a43-1076">Ya no se produce un error en el análisis de elf para los archivos binarios de patchelf.</span><span class="sxs-lookup"><span data-stu-id="18a43-1076">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="18a43-1077">(GH 471)</span><span class="sxs-lookup"><span data-stu-id="18a43-1077">(GH #471)</span></span>
- <span data-ttu-id="18a43-1078">DNS de VPN propagado a/etc/resolv.conf (GH 416, 1350)</span><span class="sxs-lookup"><span data-stu-id="18a43-1078">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="18a43-1079">Mejoras en el cierre de TCP para la transferencia de datos más confiable.</span><span class="sxs-lookup"><span data-stu-id="18a43-1079">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="18a43-1080">(GH 610, 616, 1025, 1335)</span><span class="sxs-lookup"><span data-stu-id="18a43-1080">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="18a43-1081">Ahora devuelve el código de error correcto cuando se abran demasiados archivos (EMFILE).</span><span class="sxs-lookup"><span data-stu-id="18a43-1081">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="18a43-1082">(GH 1126, 2090)</span><span class="sxs-lookup"><span data-stu-id="18a43-1082">(GH #1126, 2090)</span></span>
- <span data-ttu-id="18a43-1083">El registro de auditoría de Windows ahora informa el nombre de la imagen en la creación del proceso de auditoría.</span><span class="sxs-lookup"><span data-stu-id="18a43-1083">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="18a43-1084">Ahora se producen errores leves al iniciar bash.exe desde una ventana de Bash</span><span class="sxs-lookup"><span data-stu-id="18a43-1084">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="18a43-1085">Se ha agregado un mensaje de error cuando interop no puede acceder a un directorio de trabajo en LxFs (es decir, notepad.exe .bashrc)</span><span class="sxs-lookup"><span data-stu-id="18a43-1085">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="18a43-1086">Se ha corregido un problema en el que la ruta de acceso de Windows se truncaba en WSL</span><span class="sxs-lookup"><span data-stu-id="18a43-1086">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="18a43-1087">Mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-1087">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-1088">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-1088">LTP Results:</span></span>
<span data-ttu-id="18a43-1089">Número de pruebas superadas: 690</span><span class="sxs-lookup"><span data-stu-id="18a43-1089">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="18a43-1090">Número de no superadas (error, omitidas, etc.): 274</span><span class="sxs-lookup"><span data-stu-id="18a43-1090">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="18a43-1091">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="18a43-1091">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="18a43-1092">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="18a43-1092">Syscall Support</span></span>
<span data-ttu-id="18a43-1093">A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="18a43-1093">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="18a43-1094">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="18a43-1094">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="18a43-1095">Compilación 14986</span><span class="sxs-lookup"><span data-stu-id="18a43-1095">Build 14986</span></span>

<span data-ttu-id="18a43-1096">Para obtener información general de Windows sobre la compilación 14986, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span><span class="sxs-lookup"><span data-stu-id="18a43-1096">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-1097">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-1097">Fixed</span></span>

- <span data-ttu-id="18a43-1098">Se han corregido comprobaciones de error con IOCTL de NetLink y Pty</span><span class="sxs-lookup"><span data-stu-id="18a43-1098">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="18a43-1099">La versión del kernel ahora informa 4.4.0-43 por coherencia con Xenial</span><span class="sxs-lookup"><span data-stu-id="18a43-1099">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="18a43-1100">Bash.exe ahora se inicia cuando la entrada se dirige a "nul" (GH 1259)</span><span class="sxs-lookup"><span data-stu-id="18a43-1100">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="18a43-1101">Los identificadores de subproceso ahora se han declarado correctamente en procfs (GH 967)</span><span class="sxs-lookup"><span data-stu-id="18a43-1101">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="18a43-1102">Las marcas IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR ahora se admiten en inotify_add_watch() (GH 1280)</span><span class="sxs-lookup"><span data-stu-id="18a43-1102">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="18a43-1103">Implementa timer_create y llamadas del sistema relacionadas.</span><span class="sxs-lookup"><span data-stu-id="18a43-1103">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="18a43-1104">Esto habilita la compatibilidad con GHC (GH 307)</span><span class="sxs-lookup"><span data-stu-id="18a43-1104">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="18a43-1105">Se ha corregido un problema en el que ping devolvía una hora de 0,000 ms (GH 1296)</span><span class="sxs-lookup"><span data-stu-id="18a43-1105">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="18a43-1106">Devuelve el código de error correcto cuando se abran demasiados archivos.</span><span class="sxs-lookup"><span data-stu-id="18a43-1106">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="18a43-1107">Se ha corregido un problema en WSL donde la solicitud de NetLink de datos de la interfaz de red generaba un error con EINVAL si la dirección de hardware de la interfaz es de 32 bytes (por ejemplo, la interfaz Teredo)</span><span class="sxs-lookup"><span data-stu-id="18a43-1107">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="18a43-1108">Ten en cuenta que la utilidad "ip" de Linux contiene un error en el que se bloqueará si WSL informa de una dirección de hardware de 32 bytes.</span><span class="sxs-lookup"><span data-stu-id="18a43-1108">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="18a43-1109">Se trata de un error en "ip", no en WSL.</span><span class="sxs-lookup"><span data-stu-id="18a43-1109">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="18a43-1110">La utilidad "ip" codifica de forma rígida la longitud del búfer de cadena usado para imprimir la dirección de hardware, y el búfer es demasiado pequeño para imprimir una dirección de hardware de 32 bytes.</span><span class="sxs-lookup"><span data-stu-id="18a43-1110">The “ip” utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="18a43-1111">Mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-1111">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-1112">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-1112">LTP Results:</span></span>
<span data-ttu-id="18a43-1113">Número de pruebas superadas: 669</span><span class="sxs-lookup"><span data-stu-id="18a43-1113">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="18a43-1114">Número de no superadas (error, omitidas, etc.): 258</span><span class="sxs-lookup"><span data-stu-id="18a43-1114">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="18a43-1115">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="18a43-1115">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="18a43-1116">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="18a43-1116">Syscall Support</span></span>
<span data-ttu-id="18a43-1117">A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="18a43-1117">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="18a43-1118">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="18a43-1118">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="18a43-1119">Compilación 14971</span><span class="sxs-lookup"><span data-stu-id="18a43-1119">Build 14971</span></span>

<span data-ttu-id="18a43-1120">Para obtener información general de Windows sobre la compilación 14971, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="18a43-1120">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-1121">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-1121">Fixed</span></span>

 - <span data-ttu-id="18a43-1122">Debido a circunstancias más allá de nuestro control, no hay ninguna actualización en esta compilación para el subsistema de Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="18a43-1122">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="18a43-1123">Las actualizaciones programadas regularmente se reanudarán en la próxima versión.</span><span class="sxs-lookup"><span data-stu-id="18a43-1123">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-1124">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-1124">LTP Results:</span></span>
<span data-ttu-id="18a43-1125">Sin cambios desde 14965</span><span class="sxs-lookup"><span data-stu-id="18a43-1125">Unchanged from 14965</span></span> </br>
<span data-ttu-id="18a43-1126">Número de pruebas superadas: 664</span><span class="sxs-lookup"><span data-stu-id="18a43-1126">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="18a43-1127">Número de no superadas (error, omitidas, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="18a43-1127">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="18a43-1128">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="18a43-1128">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="18a43-1129">Compilación 14965</span><span class="sxs-lookup"><span data-stu-id="18a43-1129">Build 14965</span></span>

<span data-ttu-id="18a43-1130">Para obtener información general de Windows sobre la compilación 14965, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="18a43-1130">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-1131">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-1131">Fixed</span></span>

- <span data-ttu-id="18a43-1132">Compatibilidad con RTM_GETLINK y RTM_GETADDR del protocolo NETLINK_ROUTE de sockets de Netlink (GH 468)</span><span class="sxs-lookup"><span data-stu-id="18a43-1132">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="18a43-1133">Habilita los comandos ifconfig e ip para la enumeración de red</span><span class="sxs-lookup"><span data-stu-id="18a43-1133">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="18a43-1134">Puede encontrar más información en la [publicación de blog sobre redes WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span><span class="sxs-lookup"><span data-stu-id="18a43-1134">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="18a43-1135">/sbin está ahora en la ruta de acceso del usuario de manera predeterminada</span><span class="sxs-lookup"><span data-stu-id="18a43-1135">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="18a43-1136">La ruta de acceso de usuario de NT ahora se anexa a la ruta de acceso de WSL de manera predeterminada (es decir, ahora puedes escribir notepad.exe sin agregar System32 a la ruta de acceso de Linux)</span><span class="sxs-lookup"><span data-stu-id="18a43-1136">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="18a43-1137">Se ha agregado compatibilidad para /proc/sys/kernel/cap_last_cap</span><span class="sxs-lookup"><span data-stu-id="18a43-1137">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="18a43-1138">Los archivos binarios de NT ahora se pueden iniciar desde WSL cuando el directorio de trabajo actual contiene caracteres que no son ANSI (GH 1254)</span><span class="sxs-lookup"><span data-stu-id="18a43-1138">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="18a43-1139">Permite el apagado en el socket de flujo Unix desconectado.</span><span class="sxs-lookup"><span data-stu-id="18a43-1139">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="18a43-1140">Se ha agregado compatibilidad para PR_GET_PDEATHSIG.</span><span class="sxs-lookup"><span data-stu-id="18a43-1140">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="18a43-1141">Se ha agregado compatibilidad para CLONE_PARENT</span><span class="sxs-lookup"><span data-stu-id="18a43-1141">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="18a43-1142">Se ha corregido un error en el que la canalización se bloquea, es decir, bash -c "ls -alR /" | bash -c "cat" (GH 1214)</span><span class="sxs-lookup"><span data-stu-id="18a43-1142">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="18a43-1143">Controla las solicitudes para conectarse al terminal actual.</span><span class="sxs-lookup"><span data-stu-id="18a43-1143">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="18a43-1144">Marca /proc/<pid>/oom_score_adj como grabable.</span><span class="sxs-lookup"><span data-stu-id="18a43-1144">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="18a43-1145">Agrega la carpeta/sys/fs/cgroup.</span><span class="sxs-lookup"><span data-stu-id="18a43-1145">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="18a43-1146">sched_setaffinity debe devolver el número de máscara de bits de afinidad</span><span class="sxs-lookup"><span data-stu-id="18a43-1146">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="18a43-1147">Corrige la lógica de validación de ELF que presupone incorrectamente que las rutas de intérprete deben tener menos de 64 caracteres de longitud.</span><span class="sxs-lookup"><span data-stu-id="18a43-1147">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="18a43-1148">(GH 743)</span><span class="sxs-lookup"><span data-stu-id="18a43-1148">(GH #743)</span></span>
- <span data-ttu-id="18a43-1149">Los descriptores de archivos abiertos pueden mantener abierta la ventana de la consola (GH 1187)</span><span class="sxs-lookup"><span data-stu-id="18a43-1149">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="18a43-1150">Se ha corregido el error en el que no se podía completar rename() con la barra diagonal final en el nombre de destino (GH 1008)</span><span class="sxs-lookup"><span data-stu-id="18a43-1150">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="18a43-1151">Implementa el archivo /proc/net/dev</span><span class="sxs-lookup"><span data-stu-id="18a43-1151">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="18a43-1152">Se han corregido los pings de 0,000 ms debido a la resolución del temporizador.</span><span class="sxs-lookup"><span data-stu-id="18a43-1152">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="18a43-1153">Se ha implementado /proc/self/environ (GH 730)</span><span class="sxs-lookup"><span data-stu-id="18a43-1153">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="18a43-1154">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-1154">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-1155">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-1155">LTP Results:</span></span>
<span data-ttu-id="18a43-1156">Número de pruebas superadas: 664</span><span class="sxs-lookup"><span data-stu-id="18a43-1156">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="18a43-1157">Número de no superadas (error, omitidas, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="18a43-1157">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="18a43-1158">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="18a43-1158">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="18a43-1159">Compilación 14959</span><span class="sxs-lookup"><span data-stu-id="18a43-1159">Build 14959</span></span>

<span data-ttu-id="18a43-1160">Para obtener información general de Windows sobre la compilación 14959, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span><span class="sxs-lookup"><span data-stu-id="18a43-1160">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-1161">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-1161">Fixed</span></span>

- <span data-ttu-id="18a43-1162">Se ha mejorado la notificación del proceso PICO para Windows.</span><span class="sxs-lookup"><span data-stu-id="18a43-1162">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="18a43-1163">Encuentra información adicional en el [blog de WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span><span class="sxs-lookup"><span data-stu-id="18a43-1163">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="18a43-1164">Se ha mejorado la estabilidad de interoperabilidad con Windows</span><span class="sxs-lookup"><span data-stu-id="18a43-1164">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="18a43-1165">Se ha corregido el error 0x80070057 al iniciar bash.exe cuando Protección de datos de empresa (EDP) está habilitado</span><span class="sxs-lookup"><span data-stu-id="18a43-1165">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="18a43-1166">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-1166">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-1167">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-1167">LTP Results:</span></span>
<span data-ttu-id="18a43-1168">Número de pruebas superadas: 665</span><span class="sxs-lookup"><span data-stu-id="18a43-1168">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="18a43-1169">Número de no superadas (error, omitidas, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="18a43-1169">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="18a43-1170">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="18a43-1170">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="18a43-1171">Compilación 14955</span><span class="sxs-lookup"><span data-stu-id="18a43-1171">Build 14955</span></span>

<span data-ttu-id="18a43-1172">Para obtener información general de Windows sobre la compilación 14955, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span><span class="sxs-lookup"><span data-stu-id="18a43-1172">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-1173">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-1173">Fixed</span></span>

 - <span data-ttu-id="18a43-1174">Debido a circunstancias más allá de nuestro control, no hay ninguna actualización en esta compilación para el subsistema de Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="18a43-1174">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="18a43-1175">Las actualizaciones programadas regularmente se reanudarán en la próxima versión.</span><span class="sxs-lookup"><span data-stu-id="18a43-1175">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-1176">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-1176">LTP Results:</span></span>
<span data-ttu-id="18a43-1177">Número de pruebas superadas: 665</span><span class="sxs-lookup"><span data-stu-id="18a43-1177">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="18a43-1178">Número de no superadas (error, omitidas, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="18a43-1178">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="18a43-1179">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="18a43-1179">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="18a43-1180">Compilación 14951</span><span class="sxs-lookup"><span data-stu-id="18a43-1180">Build 14951</span></span>

<span data-ttu-id="18a43-1181">Para obtener información general de Windows sobre la compilación 14951, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="18a43-1181">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="18a43-1182">Nueva característica: Interoperabilidad de Windows/Ubuntu</span><span class="sxs-lookup"><span data-stu-id="18a43-1182">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="18a43-1183">Ahora se pueden invocar archivos binarios de Windows directamente desde la línea de comandos de WSL.</span><span class="sxs-lookup"><span data-stu-id="18a43-1183">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="18a43-1184">Esto da a los usuarios la capacidad de interactuar con el entorno y el sistema Windows de una manera que antes no era posible.</span><span class="sxs-lookup"><span data-stu-id="18a43-1184">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="18a43-1185">Como ejemplo rápido, ahora es posible que los usuarios ejecuten los siguientes comandos:</span><span class="sxs-lookup"><span data-stu-id="18a43-1185">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="18a43-1186">Puedes encontrar más información en:</span><span class="sxs-lookup"><span data-stu-id="18a43-1186">More information can be found at:</span></span>

- [<span data-ttu-id="18a43-1187">Blog del equipo de WSL para Interop</span><span class="sxs-lookup"><span data-stu-id="18a43-1187">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="18a43-1188">Documentación de interoperabilidad de MSDN</span><span class="sxs-lookup"><span data-stu-id="18a43-1188">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="18a43-1189">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-1189">Fixed</span></span>

- <span data-ttu-id="18a43-1190">Ubuntu 16.04 (Xenial) ahora se instala para todas las instancias nuevas de WSL.</span><span class="sxs-lookup"><span data-stu-id="18a43-1190">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="18a43-1191">Los usuarios con instancias existentes de 14.04 (Trusty) no se actualizarán automáticamente.</span><span class="sxs-lookup"><span data-stu-id="18a43-1191">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="18a43-1192">Ahora se muestra la configuración regional establecida durante la instalación</span><span class="sxs-lookup"><span data-stu-id="18a43-1192">Locale set during install is now displayed</span></span>
- <span data-ttu-id="18a43-1193">Mejoras del terminal, que incluido un error en el que la redirección de un proceso de WSL a un archivo no siempre funciona</span><span class="sxs-lookup"><span data-stu-id="18a43-1193">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="18a43-1194">La duración de la consola debe estar asociada a la duración de bash.exe</span><span class="sxs-lookup"><span data-stu-id="18a43-1194">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="18a43-1195">El tamaño de la ventana de la consola debe usar un tamaño visible, no el tamaño del búfer</span><span class="sxs-lookup"><span data-stu-id="18a43-1195">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="18a43-1196">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-1196">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-1197">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-1197">LTP Results:</span></span>
<span data-ttu-id="18a43-1198">Número de pruebas superadas: 665</span><span class="sxs-lookup"><span data-stu-id="18a43-1198">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="18a43-1199">Número de no superadas (error, omitidas, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="18a43-1199">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="18a43-1200">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="18a43-1200">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="18a43-1201">Compilación 14946</span><span class="sxs-lookup"><span data-stu-id="18a43-1201">Build 14946</span></span>

<span data-ttu-id="18a43-1202">Para obtener información general de Windows sobre la compilación 14946, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span><span class="sxs-lookup"><span data-stu-id="18a43-1202">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-1203">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-1203">Fixed</span></span>

- <span data-ttu-id="18a43-1204">Se ha corregido un problema que impedía la creación de cuentas de usuario de WSL para los usuarios con nombres de usuario de NT que contienen espacios o comillas.</span><span class="sxs-lookup"><span data-stu-id="18a43-1204">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="18a43-1205">Cambia VolFs y DrvFs para que devuelvan 0 para el recuento de vínculos de directorio en stat</span><span class="sxs-lookup"><span data-stu-id="18a43-1205">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="18a43-1206">Compatibilidad con la opción de socket IPV6_MULTICAST_HOPS.</span><span class="sxs-lookup"><span data-stu-id="18a43-1206">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="18a43-1207">Limite a un único bucle de E/S de la consola por tty.</span><span class="sxs-lookup"><span data-stu-id="18a43-1207">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="18a43-1208">Por ejemplo, el comando siguiente es posible:</span><span class="sxs-lookup"><span data-stu-id="18a43-1208">Example: the following command is possible:</span></span>
  - <span data-ttu-id="18a43-1209">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span><span class="sxs-lookup"><span data-stu-id="18a43-1209">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="18a43-1210">Reemplaza espacios con tabulaciones en/proc/cpuinfo (GH 1115)</span><span class="sxs-lookup"><span data-stu-id="18a43-1210">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="18a43-1211">DrvFs aparece ahora en mountinfo con un nombre que coincide con el volumen de Windows montado</span><span class="sxs-lookup"><span data-stu-id="18a43-1211">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="18a43-1212">/home y /root ahora aparecen en mountinfo con los nombres correctos</span><span class="sxs-lookup"><span data-stu-id="18a43-1212">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="18a43-1213">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-1213">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-1214">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-1214">LTP Results:</span></span>
<span data-ttu-id="18a43-1215">Número de pruebas superadas: 665</span><span class="sxs-lookup"><span data-stu-id="18a43-1215">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="18a43-1216">Número de no superadas (error, omitidas, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="18a43-1216">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="18a43-1217">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="18a43-1217">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="18a43-1218">Compilación 14942</span><span class="sxs-lookup"><span data-stu-id="18a43-1218">Build 14942</span></span>

<span data-ttu-id="18a43-1219">Para obtener información general de Windows sobre la compilación 14942, visita el [blog de Windows](https://aka.ms/onefourninefourtwoooooo).</span><span class="sxs-lookup"><span data-stu-id="18a43-1219">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-1220">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-1220">Fixed</span></span>

- <span data-ttu-id="18a43-1221">Un número de comprobaciones de error direccionadas, incluido el bloqueo de red "ATTEMPTED EXECUTE OF NOEXECUTE MEMORY" que bloqueaba SSH</span><span class="sxs-lookup"><span data-stu-id="18a43-1221">A number of bugchecks addressed, including the “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” networking crash which was blocking SSH</span></span>
- <span data-ttu-id="18a43-1222">Ahora se incluye la compatibilidad de inotifiy con las notificaciones generadas desde aplicaciones Windows en DrvFs</span><span class="sxs-lookup"><span data-stu-id="18a43-1222">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="18a43-1223">Implementa TCP_KEEPIDLE y TCP_KEEPINTVL para mongod.</span><span class="sxs-lookup"><span data-stu-id="18a43-1223">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="18a43-1224">(GH 695)</span><span class="sxs-lookup"><span data-stu-id="18a43-1224">(GH #695)</span></span>
- <span data-ttu-id="18a43-1225">Implementa la llamada del sistema pivot_root</span><span class="sxs-lookup"><span data-stu-id="18a43-1225">Implement the pivot_root system call</span></span>
- <span data-ttu-id="18a43-1226">Implementa la opción de socket para SO_DONTROUTE</span><span class="sxs-lookup"><span data-stu-id="18a43-1226">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="18a43-1227">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-1227">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="18a43-1228">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-1228">LTP Results:</span></span>
<span data-ttu-id="18a43-1229">Número de pruebas superadas: 665</span><span class="sxs-lookup"><span data-stu-id="18a43-1229">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="18a43-1230">Número de no superadas (error, omitidas, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="18a43-1230">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="18a43-1231">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="18a43-1231">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="18a43-1232">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="18a43-1232">Syscall Support</span></span>
<span data-ttu-id="18a43-1233">A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="18a43-1233">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="18a43-1234">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="18a43-1234">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="18a43-1235">Compilación 14936</span><span class="sxs-lookup"><span data-stu-id="18a43-1235">Build 14936</span></span>

<span data-ttu-id="18a43-1236">Para obtener información general de Windows sobre la compilación 14936, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="18a43-1236">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="18a43-1237">Nota: WSL instalará Ubuntu versión 16.04 (Xenial) en lugar de Ubuntu 14.04 (Trusty) en una próxima versión.</span><span class="sxs-lookup"><span data-stu-id="18a43-1237">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="18a43-1238">Este cambio se aplicará a los usuarios de Insider que instalen nuevas instancias (lxrun.exe /install o a la primera ejecución de bash.exe).</span><span class="sxs-lookup"><span data-stu-id="18a43-1238">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="18a43-1239">Las instancias existentes con Trusty no se actualizarán automáticamente.</span><span class="sxs-lookup"><span data-stu-id="18a43-1239">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="18a43-1240">Los usuarios pueden actualizar su imagen de Trusty a Xenial con el comando do-release-upgrade.</span><span class="sxs-lookup"><span data-stu-id="18a43-1240">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="18a43-1241">Problema conocido</span><span class="sxs-lookup"><span data-stu-id="18a43-1241">Known Issue</span></span>
<span data-ttu-id="18a43-1242">WSL está experimentando un problema con algunas implementaciones de sockets.</span><span class="sxs-lookup"><span data-stu-id="18a43-1242">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="18a43-1243">La comprobación de errores se manifiesta como bloqueo con el error "ATTEMPTED EXECUTE OF NOEXECUTE MEMORY".</span><span class="sxs-lookup"><span data-stu-id="18a43-1243">The bugcheck manifests itself as a crash with the error “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”.</span></span>  <span data-ttu-id="18a43-1244">La manifestación más común de este problema es un bloqueo cuando se usa ssh.</span><span class="sxs-lookup"><span data-stu-id="18a43-1244">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="18a43-1245">La causa principal se ha corregido en las compilaciones internas y se enviará a los usuarios de Insider lo antes posible.</span><span class="sxs-lookup"><span data-stu-id="18a43-1245">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="18a43-1246">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-1246">Fixed</span></span>

- <span data-ttu-id="18a43-1247">Se ha implementado la llamada del sistema chroot</span><span class="sxs-lookup"><span data-stu-id="18a43-1247">Implemented the chroot system call</span></span>
- <span data-ttu-id="18a43-1248">Mejoras en inotify, ~~incluida la compatibilidad con las notificaciones generadas desde aplicaciones Windows en DrvFs~~</span><span class="sxs-lookup"><span data-stu-id="18a43-1248">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="18a43-1249">Corrección: La compatibilidad de inotify con los cambios que se originan en aplicaciones Windows no está disponible en este momento.</span><span class="sxs-lookup"><span data-stu-id="18a43-1249">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="18a43-1250">El enlace de sockets a IPV6::<port n> ahora admite IPV6_V6ONLY (GH 68, 157, 393, 460, 674, 740, 982, 996)</span><span class="sxs-lookup"><span data-stu-id="18a43-1250">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="18a43-1251">Se ha implementado el comportamiento de WNOWAIT para la llamada del sistema waitid (GH 638)</span><span class="sxs-lookup"><span data-stu-id="18a43-1251">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="18a43-1252">Compatibilidad con las opciones de socket de IP IP_HDRINCL e IP_TTL</span><span class="sxs-lookup"><span data-stu-id="18a43-1252">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="18a43-1253">read() de longitud cero debe volver inmediatamente (GH 975)</span><span class="sxs-lookup"><span data-stu-id="18a43-1253">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="18a43-1254">Controla correctamente los nombres de archivo y los prefijos de nombre de archivo que no incluyen un terminador NULL en un archivo .tar.</span><span class="sxs-lookup"><span data-stu-id="18a43-1254">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="18a43-1255">Compatibilidad de epoll para /dev/null</span><span class="sxs-lookup"><span data-stu-id="18a43-1255">epoll support for /dev/null</span></span>
- <span data-ttu-id="18a43-1256">Corrección del origen de hora de /dev/alarm</span><span class="sxs-lookup"><span data-stu-id="18a43-1256">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="18a43-1257">bash -c ahora puede redirigir a un archivo</span><span class="sxs-lookup"><span data-stu-id="18a43-1257">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="18a43-1258">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-1258">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-1259">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-1259">LTP Results:</span></span>
<span data-ttu-id="18a43-1260">Número de pruebas superadas: 664</span><span class="sxs-lookup"><span data-stu-id="18a43-1260">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="18a43-1261">Número de no superadas (error, omitidas, etc.): 264</span><span class="sxs-lookup"><span data-stu-id="18a43-1261">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="18a43-1262">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="18a43-1262">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="18a43-1263">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="18a43-1263">Syscall Support</span></span>
<span data-ttu-id="18a43-1264">A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="18a43-1264">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="18a43-1265">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="18a43-1265">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="18a43-1266">Compilación 14931</span><span class="sxs-lookup"><span data-stu-id="18a43-1266">Build 14931</span></span>

<span data-ttu-id="18a43-1267">Para obtener información general de Windows sobre la compilación 14931, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="18a43-1267">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-1268">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-1268">Fixed</span></span>

 - <span data-ttu-id="18a43-1269">Debido a circunstancias más allá de nuestro control, no hay ninguna actualización en esta compilación para el subsistema de Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="18a43-1269">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="18a43-1270">Las actualizaciones programadas regularmente se reanudarán en la próxima versión.</span><span class="sxs-lookup"><span data-stu-id="18a43-1270">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="18a43-1271">Compilación 14926</span><span class="sxs-lookup"><span data-stu-id="18a43-1271">Build 14926</span></span>

<span data-ttu-id="18a43-1272">Para obtener información general de Windows sobre la compilación 14926, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="18a43-1272">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-1273">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-1273">Fixed</span></span>

- <span data-ttu-id="18a43-1274">Ping ahora funciona en consolas que no tienen privilegios de administrador</span><span class="sxs-lookup"><span data-stu-id="18a43-1274">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="18a43-1275">Ahora también se admite Ping6, sin privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="18a43-1275">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="18a43-1276">Compatibilidad de inotify con archivos modificados a través de WSL.</span><span class="sxs-lookup"><span data-stu-id="18a43-1276">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="18a43-1277">(GH 216)</span><span class="sxs-lookup"><span data-stu-id="18a43-1277">(GH #216)</span></span>
  - <span data-ttu-id="18a43-1278">Marcas admitidas:</span><span class="sxs-lookup"><span data-stu-id="18a43-1278">Flags supported:</span></span>
    - <span data-ttu-id="18a43-1279">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="18a43-1279">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="18a43-1280">Eventos de inotify_add_watch: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="18a43-1280">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="18a43-1281">Atributos de inotify_add_watch: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="18a43-1281">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="18a43-1282">Salida de lectura: LX_IN_ISDIR, LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="18a43-1282">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="18a43-1283">Problema conocido: La modificación de archivos desde aplicaciones de Windows no genera ningún evento</span><span class="sxs-lookup"><span data-stu-id="18a43-1283">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="18a43-1284">El socket de Unix ahora es compatible con SCM_CREDENTIALS</span><span class="sxs-lookup"><span data-stu-id="18a43-1284">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="18a43-1285">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="18a43-1285">LTP Results:</span></span>
<span data-ttu-id="18a43-1286">Número de pruebas superadas: 651</span><span class="sxs-lookup"><span data-stu-id="18a43-1286">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="18a43-1287">Número de no superadas (error, omitidas, etc.): 258</span><span class="sxs-lookup"><span data-stu-id="18a43-1287">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="18a43-1288">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="18a43-1288">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="18a43-1289">Compilación 14915</span><span class="sxs-lookup"><span data-stu-id="18a43-1289">Build 14915</span></span>

<span data-ttu-id="18a43-1290">Para obtener información general de Windows sobre la compilación 14915, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="18a43-1290">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-1291">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-1291">Fixed</span></span>
-  <span data-ttu-id="18a43-1292">Socketpair para sockets de datagramas de Unix (GH 262)</span><span class="sxs-lookup"><span data-stu-id="18a43-1292">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="18a43-1293">Compatibilidad con el socket de Unix para SO_REUSEADDR</span><span class="sxs-lookup"><span data-stu-id="18a43-1293">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="18a43-1294">Compatibilidad con el socket de Unix para SO_BROADCAST (GH 568)</span><span class="sxs-lookup"><span data-stu-id="18a43-1294">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="18a43-1295">Compatibilidad con el socket de Unix para SOCK_SEQPACKET (GH 758, 546)</span><span class="sxs-lookup"><span data-stu-id="18a43-1295">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="18a43-1296">Adición de compatibilidad para socket de datagramas de Unix send, recv y shutdown</span><span class="sxs-lookup"><span data-stu-id="18a43-1296">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="18a43-1297">Corrección de comprobación de errores debido a la validación de parámetros mmap no válida para direcciones no fijas.</span><span class="sxs-lookup"><span data-stu-id="18a43-1297">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="18a43-1298">(GH 847)</span><span class="sxs-lookup"><span data-stu-id="18a43-1298">(GH #847)</span></span>
- <span data-ttu-id="18a43-1299">Compatibilidad para suspender o reanudar los estados del terminal</span><span class="sxs-lookup"><span data-stu-id="18a43-1299">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="18a43-1300">Compatibilidad para TIOCPKT ioctl para desbloquear la utilidad de pantalla (GH 774)</span><span class="sxs-lookup"><span data-stu-id="18a43-1300">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="18a43-1301">Problema conocido: Las teclas de función no funcionan</span><span class="sxs-lookup"><span data-stu-id="18a43-1301">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="18a43-1302">Se ha corregido una carrera en TimerFd que podía hacer que LxpTimerFdWorkerRoutine accediera a un miembro liberado "ReaderReady" (GH 814)</span><span class="sxs-lookup"><span data-stu-id="18a43-1302">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="18a43-1303">Habilita la compatibilidad con llamadas del sistema reiniciables para futex, poll y clock_nanosleep</span><span class="sxs-lookup"><span data-stu-id="18a43-1303">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="18a43-1304">Se ha agregado compatibilidad con montaje de enlace</span><span class="sxs-lookup"><span data-stu-id="18a43-1304">Added bind mount support</span></span>
- <span data-ttu-id="18a43-1305">Compatibilidad para dejar de compartir el espacio de nombres de montaje</span><span class="sxs-lookup"><span data-stu-id="18a43-1305">unshare for mount namespace support</span></span>
    - <span data-ttu-id="18a43-1306">Problema conocido: Al crear un nuevo espacio de nombres de montaje con `unshare(CLONE_NEWNS)`, el directorio de trabajo actual continuará señalando al espacio de nombres anterior</span><span class="sxs-lookup"><span data-stu-id="18a43-1306">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="18a43-1307">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-1307">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="18a43-1308">Compilación 14905</span><span class="sxs-lookup"><span data-stu-id="18a43-1308">Build 14905</span></span>

<span data-ttu-id="18a43-1309">Para obtener información general de Windows sobre la compilación 14905, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span><span class="sxs-lookup"><span data-stu-id="18a43-1309">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-1310">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-1310">Fixed</span></span>
- <span data-ttu-id="18a43-1311">Ahora se admiten llamadas del sistema reiniciables (GH 349, GH 520)</span><span class="sxs-lookup"><span data-stu-id="18a43-1311">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="18a43-1312">Los vínculos simbólicos a directorios que terminan en / ahora están operativos (GH 650)</span><span class="sxs-lookup"><span data-stu-id="18a43-1312">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="18a43-1313">Se ha implementado RNDGETENTCNT ioctl para /dev/random</span><span class="sxs-lookup"><span data-stu-id="18a43-1313">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="18a43-1314">Se han implementado los archivos /proc/[pid]/mounts, /proc/[pid]/mountinfo y /proc/[pid]/mountstats</span><span class="sxs-lookup"><span data-stu-id="18a43-1314">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="18a43-1315">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-1315">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="18a43-1316">Compilación 14901</span><span class="sxs-lookup"><span data-stu-id="18a43-1316">Build 14901</span></span>
<span data-ttu-id="18a43-1317">Primera compilación de Insider para la versión posterior a la Actualización de aniversario de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="18a43-1317">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="18a43-1318">Para obtener información general de Windows sobre la compilación 14901, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="18a43-1318">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-1319">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-1319">Fixed</span></span>
- <span data-ttu-id="18a43-1320">Se ha corregido un problema de barra diagonal final</span><span class="sxs-lookup"><span data-stu-id="18a43-1320">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="18a43-1321">Ahora funcionan los comandos como `$ mv a/c/ a/b/`</span><span class="sxs-lookup"><span data-stu-id="18a43-1321">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="18a43-1322">Al instalar ahora se pregunta si la configuración regional de Ubuntu debe establecerse en la configuración regional de Windows</span><span class="sxs-lookup"><span data-stu-id="18a43-1322">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="18a43-1323">Compatibilidad de procfs para la carpeta ns</span><span class="sxs-lookup"><span data-stu-id="18a43-1323">Procfs support for ns folder</span></span>
- <span data-ttu-id="18a43-1324">Se ha agregado mount y unmount para los sistemas de archivos tmpfs, procfs y sysfs</span><span class="sxs-lookup"><span data-stu-id="18a43-1324">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="18a43-1325">Corrección de la firma ABI mknod[at] de 32 bits</span><span class="sxs-lookup"><span data-stu-id="18a43-1325">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="18a43-1326">Los sockets de Unix se movieron al modelo dispatch</span><span class="sxs-lookup"><span data-stu-id="18a43-1326">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="18a43-1327">Se debe respetar el tamaño del búfer de recepción del socket de INET mediante setsockopt</span><span class="sxs-lookup"><span data-stu-id="18a43-1327">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="18a43-1328">Implementa la marca de mensaje de recepción de socket de Unix MSG_CMSG_CLOEXEC</span><span class="sxs-lookup"><span data-stu-id="18a43-1328">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="18a43-1329">Redirección de canalización stdin/stdout de proceso de Linux (GH 2)</span><span class="sxs-lookup"><span data-stu-id="18a43-1329">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="18a43-1330">Permite la canalización de comandos bash -c en CMD.</span><span class="sxs-lookup"><span data-stu-id="18a43-1330">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="18a43-1331">Ejemplo:  >dir | bash -c "grep foo"</span><span class="sxs-lookup"><span data-stu-id="18a43-1331">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="18a43-1332">Bash ahora se puede instalar en sistemas con varios archivos de página (GH 538, 358)</span><span class="sxs-lookup"><span data-stu-id="18a43-1332">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="18a43-1333">El tamaño predeterminado del búfer del socket de INET debe coincidir con el de la configuración predeterminada de Ubuntu</span><span class="sxs-lookup"><span data-stu-id="18a43-1333">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="18a43-1334">Alinea las llamadas del sistema xattr con listxattr</span><span class="sxs-lookup"><span data-stu-id="18a43-1334">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="18a43-1335">Solo se devuelven interfaces con una dirección IPv4 válida de SIOCGIFCONF</span><span class="sxs-lookup"><span data-stu-id="18a43-1335">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="18a43-1336">Corrección de la acción predeterminada de la señal cuando se inserta por ptrace</span><span class="sxs-lookup"><span data-stu-id="18a43-1336">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="18a43-1337">Implementa /proc/sys/vm/min_free_kbytes</span><span class="sxs-lookup"><span data-stu-id="18a43-1337">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="18a43-1338">Usa valores de registro de contexto de equipo al restaurar el contexto en sigreturn</span><span class="sxs-lookup"><span data-stu-id="18a43-1338">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="18a43-1339">Esto resuelve el problema por el que java y javac se bloqueaban para algunos usuarios</span><span class="sxs-lookup"><span data-stu-id="18a43-1339">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="18a43-1340">Implementa /proc/sys/kernel/hostname</span><span class="sxs-lookup"><span data-stu-id="18a43-1340">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="18a43-1341">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="18a43-1341">Syscall Support</span></span>
<span data-ttu-id="18a43-1342">A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="18a43-1342">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="18a43-1343">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="18a43-1343">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="18a43-1344">Compilación 14388 para la Actualización de aniversario de Windows 10</span><span class="sxs-lookup"><span data-stu-id="18a43-1344">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="18a43-1345">Para obtener información general de Windows sobre la compilación 14388, visita el [blog de Windows](https://aka.ms/14388wip).</span><span class="sxs-lookup"><span data-stu-id="18a43-1345">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="18a43-1346">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-1346">Fixed</span></span>
- <span data-ttu-id="18a43-1347">Correcciones para prepararse para la Actualización de aniversario de Windows 10 el 2/8</span><span class="sxs-lookup"><span data-stu-id="18a43-1347">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="18a43-1348">Puedes encontrar más información sobre WSL en la Actualización de aniversario en nuestro [blog](https://blogs.msdn.microsoft.com/wsl/)</span><span class="sxs-lookup"><span data-stu-id="18a43-1348">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="18a43-1349">Compilación 14376</span><span class="sxs-lookup"><span data-stu-id="18a43-1349">Build 14376</span></span>
<span data-ttu-id="18a43-1350">Para obtener información general de Windows sobre la compilación 14376, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="18a43-1350">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="18a43-1351">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-1351">Fixed</span></span>
- <span data-ttu-id="18a43-1352">Se quitaron algunas instancias en las que apt-get se bloquea (GH 493)</span><span class="sxs-lookup"><span data-stu-id="18a43-1352">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="18a43-1353">Se ha corregido un problema por el que los montajes vacíos no se controlaban correctamente</span><span class="sxs-lookup"><span data-stu-id="18a43-1353">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="18a43-1354">Se ha corregido un problema por el que ramdisks no se montaban correctamente</span><span class="sxs-lookup"><span data-stu-id="18a43-1354">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="18a43-1355">Cambio en la aceptación de sockets de Unix para admitir marcas (GH parcial 451)</span><span class="sxs-lookup"><span data-stu-id="18a43-1355">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="18a43-1356">Se ha corregido la pantalla azul relacionada con la red común</span><span class="sxs-lookup"><span data-stu-id="18a43-1356">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="18a43-1357">Se ha corregido la pantalla azul al acceder a /proc/[pid]/task (GH 523)</span><span class="sxs-lookup"><span data-stu-id="18a43-1357">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="18a43-1358">Se ha corregido un uso elevado de la CPU en algunos escenarios de pty (GH 488, 504)</span><span class="sxs-lookup"><span data-stu-id="18a43-1358">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="18a43-1359">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-1359">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="18a43-1360">Compilación 14371</span><span class="sxs-lookup"><span data-stu-id="18a43-1360">Build 14371</span></span>
<span data-ttu-id="18a43-1361">Para obtener información general de Windows sobre la compilación 14371, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="18a43-1361">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="18a43-1362">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-1362">Fixed</span></span>
- <span data-ttu-id="18a43-1363">Se ha corregido la carrera de tiempo con SIGCHLD y wait() al usar ptrace</span><span class="sxs-lookup"><span data-stu-id="18a43-1363">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="18a43-1364">Se han corregido comportamientos cuando las rutas de acceso tienen una / final (GH 432)</span><span class="sxs-lookup"><span data-stu-id="18a43-1364">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="18a43-1365">Se ha corregido un problema con el error de cambio de nombre o desvinculación debido a identificadores abiertos a elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="18a43-1365">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="18a43-1366">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-1366">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="18a43-1367">Compilación 14366</span><span class="sxs-lookup"><span data-stu-id="18a43-1367">Build 14366</span></span>
<span data-ttu-id="18a43-1368">Para obtener información general de Windows sobre la compilación 14366, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span><span class="sxs-lookup"><span data-stu-id="18a43-1368">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="18a43-1369">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-1369">Fixed</span></span>
- <span data-ttu-id="18a43-1370">Corrección en la creación de archivos mediante vínculos simbólicos</span><span class="sxs-lookup"><span data-stu-id="18a43-1370">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="18a43-1371">Se ha agregado listxattr para Python (GH 385)</span><span class="sxs-lookup"><span data-stu-id="18a43-1371">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="18a43-1372">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-1372">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="18a43-1373">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="18a43-1373">Syscall Support</span></span>
-   <span data-ttu-id="18a43-1374">A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="18a43-1374">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="18a43-1375">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="18a43-1375">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="18a43-1376">Compilación 14361</span><span class="sxs-lookup"><span data-stu-id="18a43-1376">Build 14361</span></span>
<span data-ttu-id="18a43-1377">Para obtener información general de Windows sobre la compilación 14361, visita el [blog de Windows](https://aka.ms/wip14361).</span><span class="sxs-lookup"><span data-stu-id="18a43-1377">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="18a43-1378">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-1378">Fixed</span></span>
- <span data-ttu-id="18a43-1379">DrvFs ahora distingue entre mayúsculas y minúsculas cuando se ejecuta en Bash en Ubuntu en Windows.</span><span class="sxs-lookup"><span data-stu-id="18a43-1379">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="18a43-1380">Los usuarios pueden usar case.txt y CASE.TXT en sus unidades de /mnt/c</span><span class="sxs-lookup"><span data-stu-id="18a43-1380">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="18a43-1381">La distinción de mayúsculas y minúsculas solo se admite en Bash en Ubuntu en Windows.</span><span class="sxs-lookup"><span data-stu-id="18a43-1381">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="18a43-1382">Fuera de Bash, NTFS notificará los archivos correctamente, pero puede producirse un comportamiento inesperado al interactuar con los archivos de Windows.</span><span class="sxs-lookup"><span data-stu-id="18a43-1382">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="18a43-1383">La raíz de cada volumen (es decir, /mnt/c) no distingue entre mayúsculas y minúsculas</span><span class="sxs-lookup"><span data-stu-id="18a43-1383">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="18a43-1384">Puedes encontrar más información sobre cómo controlar estos archivos en Windows [aquí](https://support.microsoft.com/en-us/kb/100625).</span><span class="sxs-lookup"><span data-stu-id="18a43-1384">More information on handling these files in Windows can be found [here](https://support.microsoft.com/en-us/kb/100625).</span></span>
- <span data-ttu-id="18a43-1385">Compatibilidad con pty/tty considerablemente mejorada.</span><span class="sxs-lookup"><span data-stu-id="18a43-1385">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="18a43-1386">Ahora se admiten aplicaciones como TMUX (GH 40)</span><span class="sxs-lookup"><span data-stu-id="18a43-1386">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="18a43-1387">Se ha corregido el problema de instalación por el que las cuentas de usuario no siempre se creaban</span><span class="sxs-lookup"><span data-stu-id="18a43-1387">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="18a43-1388">Se ha optimizado la estructura de argumentos de línea de comandos que permite una lista de argumentos extremadamente larga.</span><span class="sxs-lookup"><span data-stu-id="18a43-1388">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="18a43-1389">(GH 153)</span><span class="sxs-lookup"><span data-stu-id="18a43-1389">(GH #153)</span></span>
- <span data-ttu-id="18a43-1390">Ahora puedes usar delete y chmod en archivos read_only de DrvFs</span><span class="sxs-lookup"><span data-stu-id="18a43-1390">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="18a43-1391">Se han corregido algunas instancias en las que el terminal se bloquea en la desconexión (GH 43)</span><span class="sxs-lookup"><span data-stu-id="18a43-1391">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="18a43-1392">chmod y chown ahora funcionan en dispositivos tty</span><span class="sxs-lookup"><span data-stu-id="18a43-1392">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="18a43-1393">Permite la conexión a 0.0.0.0 y :: como localhost (GH 388)</span><span class="sxs-lookup"><span data-stu-id="18a43-1393">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="18a43-1394">Sendmsg/recvmsg ahora controlan una longitud de vector de E/S > 1 (GH parcial 376)</span><span class="sxs-lookup"><span data-stu-id="18a43-1394">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="18a43-1395">Los usuarios ahora pueden dejar de participar en archivos de hosts generados automáticamente (GH 398)</span><span class="sxs-lookup"><span data-stu-id="18a43-1395">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="18a43-1396">La configuración regional de Linux se ajusta automáticamente con la configuración regional de NT durante la instalación (GH 11)</span><span class="sxs-lookup"><span data-stu-id="18a43-1396">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="18a43-1397">Se ha agregado el archivo /proc/sys/vm/swappiness (GH 306)</span><span class="sxs-lookup"><span data-stu-id="18a43-1397">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="18a43-1398">strace ahora se cierra correctamente</span><span class="sxs-lookup"><span data-stu-id="18a43-1398">strace now exits correctly</span></span>
- <span data-ttu-id="18a43-1399">Permite que las canalizaciones se vuelvan a abrir a través de /proc/self/fd (GH 222)</span><span class="sxs-lookup"><span data-stu-id="18a43-1399">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="18a43-1400">Oculta directorios en %LOCALAPPDATA%\lxss de DrvFs (GH 270)</span><span class="sxs-lookup"><span data-stu-id="18a43-1400">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="18a43-1401">Mejor control de bash.exe ~.</span><span class="sxs-lookup"><span data-stu-id="18a43-1401">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="18a43-1402">Ahora se admiten comandos como "bash ~-c ls" (GH 467)</span><span class="sxs-lookup"><span data-stu-id="18a43-1402">Commands like “bash ~ -c ls” now supported (GH #467)</span></span>
- <span data-ttu-id="18a43-1403">Ahora, los sockets notifican las lecturas de epoll disponibles durante el cierre (GH 271)</span><span class="sxs-lookup"><span data-stu-id="18a43-1403">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="18a43-1404">lxrun /uninstall funciona mejor para eliminar archivos y carpetas</span><span class="sxs-lookup"><span data-stu-id="18a43-1404">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="18a43-1405">Se ha corregido ps -f (GH 246)</span><span class="sxs-lookup"><span data-stu-id="18a43-1405">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="18a43-1406">Se ha mejorado la compatibilidad con aplicaciones X11, como xEmacs (GH 481)</span><span class="sxs-lookup"><span data-stu-id="18a43-1406">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="18a43-1407">Se ha actualizado el tamaño inicial de la pila de subprocesos para que coincida con la configuración predeterminada de Ubuntu, y se notifica el tamaño correctamente a la llamada del sistema get_rlimit (GH 172, 258)</span><span class="sxs-lookup"><span data-stu-id="18a43-1407">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="18a43-1408">Se ha mejorado la notificación de nombres de imagen de proceso PICO (por ejemplo, para auditoría)</span><span class="sxs-lookup"><span data-stu-id="18a43-1408">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="18a43-1409">Se ha implementado el comando /proc/mountinfo para df</span><span class="sxs-lookup"><span data-stu-id="18a43-1409">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="18a43-1410">Se ha corregido el código de error de vínculo simbólico para el nombre secundario .</span><span class="sxs-lookup"><span data-stu-id="18a43-1410">Fixed symlink error code for child name .</span></span> <span data-ttu-id="18a43-1411">y ..</span><span class="sxs-lookup"><span data-stu-id="18a43-1411">and ..</span></span>
- <span data-ttu-id="18a43-1412">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-1412">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="18a43-1413">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="18a43-1413">Syscall Support</span></span>
<span data-ttu-id="18a43-1414">A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="18a43-1414">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="18a43-1415">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="18a43-1415">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="18a43-1416">Compilación 14352</span><span class="sxs-lookup"><span data-stu-id="18a43-1416">Build 14352</span></span>
<span data-ttu-id="18a43-1417">Para obtener información general de Windows sobre la compilación 14352, visita el [blog de Windows](https://aka.ms/wip14352).</span><span class="sxs-lookup"><span data-stu-id="18a43-1417">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="18a43-1418">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-1418">Fixed</span></span>
- <span data-ttu-id="18a43-1419">Se ha corregido un problema en el que los archivos grandes no se descargaban o se creaban correctamente.</span><span class="sxs-lookup"><span data-stu-id="18a43-1419">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="18a43-1420">Esto debe desbloquear npm y otros escenarios (GH 3, GH 313)</span><span class="sxs-lookup"><span data-stu-id="18a43-1420">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="18a43-1421">Se han quitado algunas instancias en las que los sockets se bloquean</span><span class="sxs-lookup"><span data-stu-id="18a43-1421">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="18a43-1422">Se han corregido algunos errores de ptrace</span><span class="sxs-lookup"><span data-stu-id="18a43-1422">Corrected some ptrace errors</span></span>
- <span data-ttu-id="18a43-1423">Se ha corregido un problema con WSL que permite nombres de archivo de más de 255 caracteres</span><span class="sxs-lookup"><span data-stu-id="18a43-1423">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="18a43-1424">Se ha mejorado la compatibilidad con caracteres distintos del inglés</span><span class="sxs-lookup"><span data-stu-id="18a43-1424">Improved support for non-English characters</span></span>
- <span data-ttu-id="18a43-1425">Agrega datos de zona horaria de Windows actuales y los establece como valores predeterminados</span><span class="sxs-lookup"><span data-stu-id="18a43-1425">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="18a43-1426">Id. de dispositivo único para cada punto de montaje (corrección de jre, GH 49)</span><span class="sxs-lookup"><span data-stu-id="18a43-1426">Unique device id’s for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="18a43-1427">Corrige el problema con rutas de acceso que contienen "."</span><span class="sxs-lookup"><span data-stu-id="18a43-1427">Correct issue with paths containing “.”</span></span> <span data-ttu-id="18a43-1428">y ".."</span><span class="sxs-lookup"><span data-stu-id="18a43-1428">and “..”</span></span>
- <span data-ttu-id="18a43-1429">Se ha agregado compatibilidad con Fifo (GH 71)</span><span class="sxs-lookup"><span data-stu-id="18a43-1429">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="18a43-1430">Se ha actualizado el formato de resolv.conf para que coincida con el formato nativo de Ubuntu</span><span class="sxs-lookup"><span data-stu-id="18a43-1430">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="18a43-1431">Algunas limpiezas de procfs</span><span class="sxs-lookup"><span data-stu-id="18a43-1431">Some procfs cleanup</span></span>
- <span data-ttu-id="18a43-1432">Se ha habilitado ping para consolas de administrador (GH 18)</span><span class="sxs-lookup"><span data-stu-id="18a43-1432">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="18a43-1433">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="18a43-1433">Syscall Support</span></span>
<span data-ttu-id="18a43-1434">A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="18a43-1434">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="18a43-1435">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="18a43-1435">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="18a43-1436">Compilación 14342</span><span class="sxs-lookup"><span data-stu-id="18a43-1436">Build 14342</span></span>
<span data-ttu-id="18a43-1437">Para obtener información general de Windows sobre la compilación 14342, visita el [blog de Windows](https://aka.ms/wip14342).</span><span class="sxs-lookup"><span data-stu-id="18a43-1437">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="18a43-1438">Puedes encontrar información sobre VolFs y DriveFs en el [blog de WSL](https://blogs.msdn.microsoft.com/wsl).</span><span class="sxs-lookup"><span data-stu-id="18a43-1438">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="18a43-1439">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-1439">Fixed</span></span>
- <span data-ttu-id="18a43-1440">Se ha corregido el problema de instalación cuando el usuario de Windows tenía caracteres Unicode en el nombre de usuario</span><span class="sxs-lookup"><span data-stu-id="18a43-1440">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="18a43-1441">La solución alternativa de apt-get update udev en las preguntas más frecuentes se proporciona ahora de forma predeterminada en la primera ejecución</span><span class="sxs-lookup"><span data-stu-id="18a43-1441">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="18a43-1442">Vínculos simbólicos habilitados en directorios DriveFs (/mnt/<drive>)</span><span class="sxs-lookup"><span data-stu-id="18a43-1442">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="18a43-1443">Los vínculos simbólicos ahora funcionan entre DriveFs y VolFs</span><span class="sxs-lookup"><span data-stu-id="18a43-1443">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="18a43-1444">Se ha solucionado el problema de análisis de ruta de acceso de nivel superior:ls .// funcionará ahora como se espera</span><span class="sxs-lookup"><span data-stu-id="18a43-1444">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="18a43-1445">La instalación de npm en DriveFs y las opciones -g ahora funcionan</span><span class="sxs-lookup"><span data-stu-id="18a43-1445">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="18a43-1446">Se ha corregido un problema que impedía que el servidor PHP se iniciara</span><span class="sxs-lookup"><span data-stu-id="18a43-1446">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="18a43-1447">Se han actualizado los valores de entorno predeterminados, como $PATH para que coincidan con Ubuntu nativo</span><span class="sxs-lookup"><span data-stu-id="18a43-1447">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="18a43-1448">Se ha agregado una tarea de mantenimiento semanal en Windows para actualizar la caché de paquetes apt</span><span class="sxs-lookup"><span data-stu-id="18a43-1448">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="18a43-1449">Se ha corregido un problema con la validación de encabezado de ELF, WSL ahora es compatible con todas las opciones de Melkor</span><span class="sxs-lookup"><span data-stu-id="18a43-1449">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="18a43-1450">El shell Zsh funciona</span><span class="sxs-lookup"><span data-stu-id="18a43-1450">Zsh shell is functional</span></span>
- <span data-ttu-id="18a43-1451">Ahora se admiten los binarios de Go precompilados</span><span class="sxs-lookup"><span data-stu-id="18a43-1451">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="18a43-1452">Indicar bash.exe en la primera ejecución ahora se localiza correctamente</span><span class="sxs-lookup"><span data-stu-id="18a43-1452">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="18a43-1453">/proc/meminfo ahora devuelve la información correcta</span><span class="sxs-lookup"><span data-stu-id="18a43-1453">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="18a43-1454">Ahora se admiten sockets en VFS</span><span class="sxs-lookup"><span data-stu-id="18a43-1454">Sockets now supported in VFS</span></span>
- <span data-ttu-id="18a43-1455">/dev ahora se monta como tempfs</span><span class="sxs-lookup"><span data-stu-id="18a43-1455">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="18a43-1456">Ahora se admite Fifo</span><span class="sxs-lookup"><span data-stu-id="18a43-1456">Fifo now supported</span></span>
- <span data-ttu-id="18a43-1457">Los sistemas de varios núcleos ahora se muestran correctamente en /proc/cpuinfo</span><span class="sxs-lookup"><span data-stu-id="18a43-1457">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="18a43-1458">Mejoras adicionales y mensajes de error que se descargan durante la primera ejecución</span><span class="sxs-lookup"><span data-stu-id="18a43-1458">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="18a43-1459">Mejoras de llamadas del sistema y corrección de errores.</span><span class="sxs-lookup"><span data-stu-id="18a43-1459">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="18a43-1460">Lista de llamadas del sistema admitidas a continuación.</span><span class="sxs-lookup"><span data-stu-id="18a43-1460">Supported syscall list below.</span></span>
- <span data-ttu-id="18a43-1461">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-1461">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="18a43-1462">Problemas conocidos</span><span class="sxs-lookup"><span data-stu-id="18a43-1462">Known Issues</span></span>
- <span data-ttu-id="18a43-1463">No se resuelve ".."</span><span class="sxs-lookup"><span data-stu-id="18a43-1463">Not resolving ‘..’</span></span> <span data-ttu-id="18a43-1464">correctamente en DriveFs en algunos casos</span><span class="sxs-lookup"><span data-stu-id="18a43-1464">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="18a43-1465">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="18a43-1465">Syscall Support</span></span>
<span data-ttu-id="18a43-1466">A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="18a43-1466">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="18a43-1467">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="18a43-1467">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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

## <a name="build-14332"></a><span data-ttu-id="18a43-1468">Compilación 14332</span><span class="sxs-lookup"><span data-stu-id="18a43-1468">Build 14332</span></span>

<span data-ttu-id="18a43-1469">Para obtener información general de Windows sobre la compilación 14332, visita el [blog de Windows](https://aka.ms/wip14332).</span><span class="sxs-lookup"><span data-stu-id="18a43-1469">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="18a43-1470">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-1470">Fixed</span></span>
- <span data-ttu-id="18a43-1471">Mejor generación de resolv.conf, incluida la priorización de entradas de DNS</span><span class="sxs-lookup"><span data-stu-id="18a43-1471">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="18a43-1472">Problema con el movimiento de archivos y directorios entre unidades /mnt y no /mnt</span><span class="sxs-lookup"><span data-stu-id="18a43-1472">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="18a43-1473">Los archivos tar ahora se pueden crear con vínculos simbólicos</span><span class="sxs-lookup"><span data-stu-id="18a43-1473">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="18a43-1474">Se ha agregado el directorio predeterminado /run/lock en la creación de instancias</span><span class="sxs-lookup"><span data-stu-id="18a43-1474">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="18a43-1475">Actualiza /dev/null para que devuelva la información de estadísticas correcta</span><span class="sxs-lookup"><span data-stu-id="18a43-1475">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="18a43-1476">Errores adicionales al descargar durante la primera ejecución</span><span class="sxs-lookup"><span data-stu-id="18a43-1476">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="18a43-1477">Mejoras de llamadas del sistema y corrección de errores.</span><span class="sxs-lookup"><span data-stu-id="18a43-1477">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="18a43-1478">Lista de llamadas del sistema admitidas a continuación.</span><span class="sxs-lookup"><span data-stu-id="18a43-1478">Supported syscall list below.</span></span>
- <span data-ttu-id="18a43-1479">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-1479">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="18a43-1480">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="18a43-1480">Syscall Support</span></span>
<span data-ttu-id="18a43-1481">A continuación se muestra la nueva llamada del sistema que tiene alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="18a43-1481">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="18a43-1482">La llamada del sistema de esta lista se admite en al menos un escenario, pero puede que no se admita todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="18a43-1482">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="18a43-1483">Compilación 14328</span><span class="sxs-lookup"><span data-stu-id="18a43-1483">Build 14328</span></span>

<span data-ttu-id="18a43-1484">Para obtener información general de Windows sobre la compilación 14332, visita el [blog de Windows](https://aka.ms/wip14328).</span><span class="sxs-lookup"><span data-stu-id="18a43-1484">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="18a43-1485">Nuevas características</span><span class="sxs-lookup"><span data-stu-id="18a43-1485">New Features</span></span>
* <span data-ttu-id="18a43-1486">Ahora admite usuarios de Linux.</span><span class="sxs-lookup"><span data-stu-id="18a43-1486">Now support Linux users.</span></span>  <span data-ttu-id="18a43-1487">Al instalar Bash en Ubuntu en Windows, se solicitará la creación de un usuario de Linux.</span><span class="sxs-lookup"><span data-stu-id="18a43-1487">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="18a43-1488">Para más información, visita https://aka.ms/wslusers.</span><span class="sxs-lookup"><span data-stu-id="18a43-1488">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="18a43-1489">El nombre de host ahora se establece en el nombre del equipo de Windows, ya no más en @localhost</span><span class="sxs-lookup"><span data-stu-id="18a43-1489">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="18a43-1490">Para más información sobre la compilación 14328, visita: https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="18a43-1490">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="18a43-1491">Fijo</span><span class="sxs-lookup"><span data-stu-id="18a43-1491">Fixed</span></span>
* <span data-ttu-id="18a43-1492">Mejoras de vínculos simbólicos para archivos que no son /mnt/<drive></span><span class="sxs-lookup"><span data-stu-id="18a43-1492">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="18a43-1493">La instalación de npm ahora funciona</span><span class="sxs-lookup"><span data-stu-id="18a43-1493">npm install now works</span></span>
    * <span data-ttu-id="18a43-1494">jdk / jre ahora se puede instalar con las instrucciones que se encuentran [aquí](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span><span class="sxs-lookup"><span data-stu-id="18a43-1494">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="18a43-1495">Problema conocido: los vínculos simbólicos no funcionan para los montajes de Windows.</span><span class="sxs-lookup"><span data-stu-id="18a43-1495">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="18a43-1496">La funcionalidad estará disponible en una compilación posterior</span><span class="sxs-lookup"><span data-stu-id="18a43-1496">Functionality will be available in a later build</span></span>
* <span data-ttu-id="18a43-1497">top y htop ahora se muestran</span><span class="sxs-lookup"><span data-stu-id="18a43-1497">top and htop now display</span></span>
* <span data-ttu-id="18a43-1498">Mensajes de error adicionales para algunos errores de instalación</span><span class="sxs-lookup"><span data-stu-id="18a43-1498">Additional error messages for some install failures</span></span>
* <span data-ttu-id="18a43-1499">Mejoras de llamadas del sistema y corrección de errores.</span><span class="sxs-lookup"><span data-stu-id="18a43-1499">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="18a43-1500">Lista de llamadas del sistema admitidas a continuación.</span><span class="sxs-lookup"><span data-stu-id="18a43-1500">Supported syscall list below.</span></span>
* <span data-ttu-id="18a43-1501">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="18a43-1501">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="18a43-1502">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="18a43-1502">Syscall Support</span></span>
<span data-ttu-id="18a43-1503">A continuación hay una lista de llamadas del sistema que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="18a43-1503">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="18a43-1504">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="18a43-1504">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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
