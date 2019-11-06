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
ms.openlocfilehash: 63c0e14dab73faf7f835e9ae1eb23eb490b13c44
ms.sourcegitcommit: 48ca05ce1ac8bf35408af3bc2a2b92a43adba0af
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/30/2019
ms.locfileid: "73166662"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="12a55-105">Notas de la versión del subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="12a55-105">Release Notes for Windows Subsystem for Linux</span></span>

## <a name="build-19013"></a><span data-ttu-id="12a55-106">Compilación 19013</span><span class="sxs-lookup"><span data-stu-id="12a55-106">Build 19013</span></span>
<span data-ttu-id="12a55-107">Para obtener información general de Windows sobre la compilación 19013, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/10/29/announcing-windows-10-insider-preview-build-19013/).</span><span class="sxs-lookup"><span data-stu-id="12a55-107">For general Windows information on build 19013 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/29/announcing-windows-10-insider-preview-build-19013/).</span></span>

* <span data-ttu-id="12a55-108">[WSL2] Mejora del rendimiento de memoria de la VM de la utilidad WSL.</span><span class="sxs-lookup"><span data-stu-id="12a55-108">[WSL2] Improve memory performance of WSL utility VM.</span></span> <span data-ttu-id="12a55-109">La memoria que ya no esté en uso se liberará de nuevo al host.</span><span class="sxs-lookup"><span data-stu-id="12a55-109">Memory that is no longer in use will be freed back to the host.</span></span>
* <span data-ttu-id="12a55-110">[WSL2] Actualización de la versión del kernel a 4.19.79.</span><span class="sxs-lookup"><span data-stu-id="12a55-110">[WSL2] Update kernel version to 4.19.79.</span></span> <span data-ttu-id="12a55-111">(Adición de CONFIG_HIGH_RES_TIMERS, CONFIG_TASK_XACCT, CONFIG_TASK_IO_ACCOUNTING, CONFIG_SCHED_HRTICK y CONFIG_BRIDGE_VLAN_FILTERING).</span><span class="sxs-lookup"><span data-stu-id="12a55-111">(add CONFIG_HIGH_RES_TIMERS, CONFIG_TASK_XACCT, CONFIG_TASK_IO_ACCOUNTING, CONFIG_SCHED_HRTICK, and CONFIG_BRIDGE_VLAN_FILTERING).</span></span>
* <span data-ttu-id="12a55-112">[WSL2] Corrección de la retransmisión de entrada para controlar los casos en los que stdin es un identificador de canalización que no está cerrado [GH 4424].</span><span class="sxs-lookup"><span data-stu-id="12a55-112">[WSL2] Fix input relay to handle cases where stdin is a pipe handle that is not closed [GH 4424]</span></span>
* <span data-ttu-id="12a55-113">Comprobación de que \\\\wsl$ no distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="12a55-113">Make the check for \\\\wsl$ case-insensitive.</span></span>
```
[wsl2]
pageReporting = <bool>    # Enable or disable the free memory page reporting feature (default true).
idleThreshold = <integer> # Set the idle threshold for memory compaction, 0 disables the feature (default 1).
```

## <a name="build-19002"></a><span data-ttu-id="12a55-114">Compilación 19002</span><span class="sxs-lookup"><span data-stu-id="12a55-114">Build 19002</span></span>
<span data-ttu-id="12a55-115">Para obtener información general de Windows sobre la compilación 19002, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/10/17/announcing-windows-10-insider-preview-build-19002/).</span><span class="sxs-lookup"><span data-stu-id="12a55-115">For general Windows information on build 19002 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/17/announcing-windows-10-insider-preview-build-19002/).</span></span>

* <span data-ttu-id="12a55-116">[WSL] Corrección de un problema con el control de algunos caracteres Unicode: https://github.com/microsoft/terminal/issues/2770</span><span class="sxs-lookup"><span data-stu-id="12a55-116">[WSL] Fix issue with handling of some Unicode characters: https://github.com/microsoft/terminal/issues/2770</span></span>
* <span data-ttu-id="12a55-117">[WSL] Corrección de casos poco frecuentes en los que se podría anular el registro de distribuciones si se iniciaban inmediatamente después de una actualización de una compilación a otra.</span><span class="sxs-lookup"><span data-stu-id="12a55-117">[WSL] Fix rare cases where distros could be unregistered if launched immediately after a build-to-build upgrade.</span></span>
* <span data-ttu-id="12a55-118">[WSL] Corrección de un problema leve por el que wsl.exe se apagaba cuando no se cancelaban los temporizadores de inactividad de la instancia.</span><span class="sxs-lookup"><span data-stu-id="12a55-118">[WSL] Fix minor issue with wsl.exe --shutdown where instance idle timers were not cancelled.</span></span>

## <a name="build-18995"></a><span data-ttu-id="12a55-119">Compilación 18995</span><span class="sxs-lookup"><span data-stu-id="12a55-119">Build 18995</span></span>
<span data-ttu-id="12a55-120">Para obtener información general de Windows sobre la compilación 18995, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/).</span><span class="sxs-lookup"><span data-stu-id="12a55-120">For general Windows information on build 18995 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/).</span></span>

* <span data-ttu-id="12a55-121">[WSL2] Corrección de un problema que provocaba que los montajes DrvFs dejaran de funcionar después de que se interrumpiera una operación (por ejemplo, Ctrl-C) [GH 4377]</span><span class="sxs-lookup"><span data-stu-id="12a55-121">[WSL2] Fix an issue where DrvFs mounts stopped working after an operation was interrupted (e.g. ctrl-c) [GH 4377]</span></span>
* <span data-ttu-id="12a55-122">[WSL2] Corrección del control de mensajes hvsocket muy grandes [GH 4105]</span><span class="sxs-lookup"><span data-stu-id="12a55-122">[WSL2] Fix handling of very large hvsocket messages [GH 4105]</span></span>
* <span data-ttu-id="12a55-123">[WSL2] Corrección de un problema con la interoperabilidad cuando stdin es un archivo [GH 4475]</span><span class="sxs-lookup"><span data-stu-id="12a55-123">[WSL2] Fix issue with interop when stdin is a file [GH 4475]</span></span>
* <span data-ttu-id="12a55-124">[WSL2] Corrección de un bloqueo de servicio cuando se encontraba un estado de red inesperado [GH 4474]</span><span class="sxs-lookup"><span data-stu-id="12a55-124">[WSL2] Fix service crash when unexpected network state is encountered [GH 4474]</span></span>
* <span data-ttu-id="12a55-125">[WSL2] Consulta del nombre de distribución desde el servidor de interoperabilidad si el proceso actual no tiene la variable de entorno</span><span class="sxs-lookup"><span data-stu-id="12a55-125">[WSL2] Query the distro name from the interop server if the current process does not have the environment variable</span></span>
* <span data-ttu-id="12a55-126">[WSL2] Corrección de un problema con la interoperabilidad cuando stdin es un archivo</span><span class="sxs-lookup"><span data-stu-id="12a55-126">[WSL2] Fix issue with interop whe stdin is a file</span></span>
* <span data-ttu-id="12a55-127">[WSL2] Actualización de la versión del kernel de Linux a 4.19.72</span><span class="sxs-lookup"><span data-stu-id="12a55-127">[WSL2] Update Linux kernel version to 4.19.72</span></span>
* <span data-ttu-id="12a55-128">[WSL2] Agrega la capacidad de especificar parámetros adicionales de línea de comandos de kernel mediante .wslconfig</span><span class="sxs-lookup"><span data-stu-id="12a55-128">[WSL2] Add ability to specify additional kernel command line parameters via .wslconfig</span></span>
```
[wsl2]
kernelCommandLine = <string> # Additional kernel command line arguments
```

## <a name="build-18990"></a><span data-ttu-id="12a55-129">Compilación 18990</span><span class="sxs-lookup"><span data-stu-id="12a55-129">Build 18990</span></span>
<span data-ttu-id="12a55-130">Para obtener información general de Windows sobre la compilación 18990, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/).</span><span class="sxs-lookup"><span data-stu-id="12a55-130">For general Windows information on build 18990 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/).</span></span>

* <span data-ttu-id="12a55-131">Mejorar el rendimiento de los listados de directorios en \\\\wsl$</span><span class="sxs-lookup"><span data-stu-id="12a55-131">Improve the performance for directory listings in \\\\wsl$</span></span>
* <span data-ttu-id="12a55-132">[WSL2] Insertar entropía de arranque adicional [GH 4416]</span><span class="sxs-lookup"><span data-stu-id="12a55-132">[WSL2] Inject additional boot entropy [GH 4416]</span></span>
* <span data-ttu-id="12a55-133">[WSL2] Corrección para la interoperabilidad de Windows al usar su/sudo [GH 4465]</span><span class="sxs-lookup"><span data-stu-id="12a55-133">[WSL2] Fix for Windows interop when using su / sudo [GH 4465]</span></span>

## <a name="build-18980"></a><span data-ttu-id="12a55-134">Compilación 18980</span><span class="sxs-lookup"><span data-stu-id="12a55-134">Build 18980</span></span>
<span data-ttu-id="12a55-135">Para obtener información general de Windows sobre la compilación 18980, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).</span><span class="sxs-lookup"><span data-stu-id="12a55-135">For general Windows information on build 18980 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).</span></span>

* <span data-ttu-id="12a55-136">Corrige la lectura de los vínculos simbólicos que deniegan FILE_READ_DATA.</span><span class="sxs-lookup"><span data-stu-id="12a55-136">Fix reading symlinks that deny FILE_READ_DATA.</span></span> <span data-ttu-id="12a55-137">Esto incluye todos los vínculos simbólicos que crea Windows para la compatibilidad con versiones anteriores, como "C:\Document and Settings" y un conjunto de vínculos simbólicos en el directorio de perfil del usuario.</span><span class="sxs-lookup"><span data-stu-id="12a55-137">This includes all the symlinks Windows creates for backwards compatibility such as "C:\Document and Settings" and a bunch of symlinks in the user profile directory</span></span>
* <span data-ttu-id="12a55-138">Hace que el estado inesperado del sistema de archivos no sea irrecuperable [GH 4334, 4305]</span><span class="sxs-lookup"><span data-stu-id="12a55-138">Make unexpected filesystem state non-fatal [GH 4334, 4305]</span></span>
* <span data-ttu-id="12a55-139">[WSL2] Agrega compatibilidad para arm64 si tu CPU/firmware admite virtualización</span><span class="sxs-lookup"><span data-stu-id="12a55-139">[WSL2] Add support for arm64 if your CPU / firmware supports virtualization</span></span>
* <span data-ttu-id="12a55-140">[WSL2] Permite a los usuarios sin privilegios ver el registro del kernel</span><span class="sxs-lookup"><span data-stu-id="12a55-140">[WSL2] Allow unprivileged users to view kernel log</span></span>
* <span data-ttu-id="12a55-141">[WSL2] Corrige la retransmisión de salida cuando se han cerrado los sockets stdout/stderr [GH 4375]</span><span class="sxs-lookup"><span data-stu-id="12a55-141">[WSL2] Fix output relay when stdout / stderr sockets have been closed [GH 4375]</span></span>
* <span data-ttu-id="12a55-142">[WSL2] Compatibilidad con la batería y el adaptador de AC</span><span class="sxs-lookup"><span data-stu-id="12a55-142">[WSL2] Support battery and AC adapter passthrough</span></span>
* <span data-ttu-id="12a55-143">[WSL2] Actualización del kernel de Linux a 4.19.67</span><span class="sxs-lookup"><span data-stu-id="12a55-143">[WSL2] Update Linux kernel to 4.19.67</span></span>
* <span data-ttu-id="12a55-144">Adición de la capacidad de establecer el nombre de usuario predeterminado en /etc/WSL.conf:</span><span class="sxs-lookup"><span data-stu-id="12a55-144">Add the ability to set default username in /etc/wsl.conf:</span></span>
```
[user]
default=<string>
```

## <a name="build-18975"></a><span data-ttu-id="12a55-145">Compilación 18975</span><span class="sxs-lookup"><span data-stu-id="12a55-145">Build 18975</span></span>
<span data-ttu-id="12a55-146">Para obtener información general de Windows sobre la compilación 18975,visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).</span><span class="sxs-lookup"><span data-stu-id="12a55-146">For general Windows information on build 18975 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).</span></span>

* <span data-ttu-id="12a55-147">[WSL2] Se han corregido varios problemas de confiabilidad de localhost [GH 4340]</span><span class="sxs-lookup"><span data-stu-id="12a55-147">[WSL2] Fixed a number of localhost reliability issues [GH 4340]</span></span>

## <a name="build-18970"></a><span data-ttu-id="12a55-148">Compilación 18970</span><span class="sxs-lookup"><span data-stu-id="12a55-148">Build 18970</span></span>
<span data-ttu-id="12a55-149">Para obtener información general de Windows sobre la compilación 18970, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).</span><span class="sxs-lookup"><span data-stu-id="12a55-149">For general Windows information on build 18970 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).</span></span>

* <span data-ttu-id="12a55-150">[WSL2] Sincronización de la hora con la hora del host cuando el sistema se reanuda desde el estado de suspensión [GH 4245]</span><span class="sxs-lookup"><span data-stu-id="12a55-150">[WSL2] Sync time with host time when system resumes from sleep state [GH 4245]</span></span>
* <span data-ttu-id="12a55-151">[WSL2] Crea vínculos simbólicos de NT en volúmenes de Windows cuando sea posible.</span><span class="sxs-lookup"><span data-stu-id="12a55-151">[WSL2] Create NT symlinks on the Windows volumes when possible.</span></span>
* <span data-ttu-id="12a55-152">[WSL2] Crea distribuciones en los espacios de nombres UTS, IPC, PID y Mount.</span><span class="sxs-lookup"><span data-stu-id="12a55-152">[WSL2] Create distros in UTS, IPC, PID, and Mount namespaces.</span></span>
* <span data-ttu-id="12a55-153">[WSL2] Corrección de retransmisión de puerto localhost cuando el servidor se enlaza a localhost directamente [GH 4353]</span><span class="sxs-lookup"><span data-stu-id="12a55-153">[WSL2] Fix localhost port relay when server binds to localhost directly [GH 4353]</span></span>
* <span data-ttu-id="12a55-154">[WSL2] Corrección de interoperabilidad cuando se redirige la salida [GH 4337]</span><span class="sxs-lookup"><span data-stu-id="12a55-154">[WSL2] Fix interop when output is redirected [GH 4337]</span></span>
* <span data-ttu-id="12a55-155">[WSL2] Compatibilidad con la traducción de vínculos simbólicos de NT absolutos.</span><span class="sxs-lookup"><span data-stu-id="12a55-155">[WSL2] Support translating absolute NT symlinks.</span></span>
* <span data-ttu-id="12a55-156">[WSL2] Actualización del kernel a 4.19.59</span><span class="sxs-lookup"><span data-stu-id="12a55-156">[WSL2] Update kernel to 4.19.59</span></span>
* <span data-ttu-id="12a55-157">[WSL2] Definición correcta de la máscara de subred para eth0.</span><span class="sxs-lookup"><span data-stu-id="12a55-157">[WSL2] Properly set subnet mask for eth0.</span></span>
* <span data-ttu-id="12a55-158">[WSL2] Cambio de la lógica para interrumpir el bucle de trabajo de la consola cuando se señale el evento de salida.</span><span class="sxs-lookup"><span data-stu-id="12a55-158">[WSL2] Change logic to break out of console worker loop when exit event is signaled.</span></span>
* <span data-ttu-id="12a55-159">[WSL2] Expulsión del VHD de distribución cuando la  distribución no está en ejecución.</span><span class="sxs-lookup"><span data-stu-id="12a55-159">[WSL2] Eject distribution vhd when the distro is not running.</span></span>
* <span data-ttu-id="12a55-160">[WSL2] Corrección de la biblioteca de análisis de configuración para controlar correctamente los valores vacíos.</span><span class="sxs-lookup"><span data-stu-id="12a55-160">[WSL2] Fix config parsing library to correctly handle empty values.</span></span>
* <span data-ttu-id="12a55-161">[WSL2] Compatibilidad con el escritorio de Docker al crear montajes de distribución cruzados.</span><span class="sxs-lookup"><span data-stu-id="12a55-161">[WSL2] Support Docker Desktop by creating cross distro mounts.</span></span> <span data-ttu-id="12a55-162">Un distribución puede participar en este comportamiento si se agrega la siguiente línea al archivo /etc/wsl.conf:</span><span class="sxs-lookup"><span data-stu-id="12a55-162">A distro can opt-in to this behavior by adding the following line to the /etc/wsl.conf file:</span></span>
```
[automount]
crossDistro = true
```

## <a name="build-18945"></a><span data-ttu-id="12a55-163">Compilación 18945</span><span class="sxs-lookup"><span data-stu-id="12a55-163">Build 18945</span></span>
<span data-ttu-id="12a55-164">Para obtener información general de Windows sobre la compilación 18945, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span><span class="sxs-lookup"><span data-stu-id="12a55-164">For general Windows information on build 18945 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-165">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-165">WSL</span></span>
* <span data-ttu-id="12a55-166">[WSL2] Permite que se acceda a los sockets TCP de escucha en WSL2 desde el host mediante localhost:port</span><span class="sxs-lookup"><span data-stu-id="12a55-166">[WSL2] Allow listening tcp sockets in WSL2 to be accessible from the host by using localhost:port</span></span>
* <span data-ttu-id="12a55-167">[WSL2] Correcciones de errores de instalación/conversión y diagnósticos adicionales para un seguimiento de los problemas futuros [GH 4105]</span><span class="sxs-lookup"><span data-stu-id="12a55-167">[WSL2] Fixes for install / conversion failures and additional diagnostics to track down future issues [GH 4105]</span></span> 
* <span data-ttu-id="12a55-168">[WSL2] Mejora la capacidad de diagnóstico de los problemas de red de WSL2</span><span class="sxs-lookup"><span data-stu-id="12a55-168">[WSL2] Improve diagnosability of WSL2 network issues</span></span>
* <span data-ttu-id="12a55-169">[WSL2] Actualización de la versión del kernel a 4.19.55</span><span class="sxs-lookup"><span data-stu-id="12a55-169">[WSL2] Update kernel version to 4.19.55</span></span>
* <span data-ttu-id="12a55-170">[WSL2] Actualización del kernel con las opciones de configuración necesarias para Docker [GH 4165]</span><span class="sxs-lookup"><span data-stu-id="12a55-170">[WSL2] Update kernel with config options required for docker [GH 4165]</span></span>
* <span data-ttu-id="12a55-171">[WSL2] Aumento del número de CPU asignadas a la VM de utilidad ligera para que sea el mismo que el host (se ha limitado previamente a 8 por CONFIG_NR_CPUS en la configuración del kernel) [GH 4137]</span><span class="sxs-lookup"><span data-stu-id="12a55-171">[WSL2] Increase the number of CPUs assigned to the lightweight utility VM to be the same as the host (was previously capped at 8 by CONFIG_NR_CPUS in the kernel config) [GH 4137]</span></span>
* <span data-ttu-id="12a55-172">[WSL2] Creación de un archivo de intercambio para la VM ligera WSL2</span><span class="sxs-lookup"><span data-stu-id="12a55-172">[WSL2] Create a swap file for the WSL2 lightweight VM</span></span>
* <span data-ttu-id="12a55-173">[WSL2] Permite que los montajes de usuarios sean visibles a través de la distribución \\\\wsl$\\ (por ejemplo, sshfs) [GH 4172]</span><span class="sxs-lookup"><span data-stu-id="12a55-173">[WSL2] Allow user mounts to be visible via \\\\wsl$\\distro (for example sshfs) [GH 4172]</span></span>
* <span data-ttu-id="12a55-174">[WSL2] Mejora el rendimiento del sistema de archivos 9p</span><span class="sxs-lookup"><span data-stu-id="12a55-174">[WSL2] Improve 9p filesystem performance</span></span>
* <span data-ttu-id="12a55-175">[WSL2] Asegura que la ACL de VHD no crezca sin límite [GH 4126]</span><span class="sxs-lookup"><span data-stu-id="12a55-175">[WSL2] Ensure vhd ACL does not grow unbounded [GH 4126]</span></span>
* <span data-ttu-id="12a55-176">[WSL2] Actualización de la configuración de kernel para admitir squashfs y xt_conntrack [GH 4107, 4123]</span><span class="sxs-lookup"><span data-stu-id="12a55-176">[WSL2] Update kernel config to support squashfs and xt_conntrack [GH 4107, 4123]</span></span>
* <span data-ttu-id="12a55-177">[WSL2] Corrección para la opción interop.enabled /etc/wsl.conf [GH 4140]</span><span class="sxs-lookup"><span data-stu-id="12a55-177">[WSL2] Fix for interop.enabled /etc/wsl.conf option [GH 4140]</span></span>
* <span data-ttu-id="12a55-178">[WSL2] Devuelve ENOTSUP si el sistema de archivos no es compatible con EA</span><span class="sxs-lookup"><span data-stu-id="12a55-178">[WSL2] Return ENOTSUP if the file system does not support EAs</span></span>
* <span data-ttu-id="12a55-179">[WSL2] Corrección de CopyFile colgado con \\\\wsl$</span><span class="sxs-lookup"><span data-stu-id="12a55-179">[WSL2] Fix CopyFile hang with \\\\wsl$</span></span>
* <span data-ttu-id="12a55-180">Cambio del valor predeterminado de umask a 0022 y adición de la configuración de filesystem.umask a /etc/wsl.conf</span><span class="sxs-lookup"><span data-stu-id="12a55-180">Switch default umask to 0022 and add filesystem.umask setting to /etc/wsl.conf</span></span>
* <span data-ttu-id="12a55-181">Corrección de wslpath para resolver correctamente los vínculos simbólicos, esto se retomó en 19h1 [GH 4078]</span><span class="sxs-lookup"><span data-stu-id="12a55-181">Fix wslpath to properly resolve symlinks, this was regressed in 19h1 [GH 4078]</span></span>
* <span data-ttu-id="12a55-182">Introducción del archivo %UserProfile%\\.wslconfig para ajustar la configuración de WSL2</span><span class="sxs-lookup"><span data-stu-id="12a55-182">Introduce %UserProfile%\\.wslconfig file for tweaking WSL2 settings</span></span>
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

## <a name="build-18917"></a><span data-ttu-id="12a55-183">Compilación 18917</span><span class="sxs-lookup"><span data-stu-id="12a55-183">Build 18917</span></span>
<span data-ttu-id="12a55-184">Para obtener información general de Windows sobre la compilación 18917, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span><span class="sxs-lookup"><span data-stu-id="12a55-184">For general Windows information on build 18917 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-185">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-185">WSL</span></span>
* <span data-ttu-id="12a55-186">¡WSL 2 ya está disponible!</span><span class="sxs-lookup"><span data-stu-id="12a55-186">WSL 2 is now available!</span></span> <span data-ttu-id="12a55-187">Consulta el [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) para más detalles.</span><span class="sxs-lookup"><span data-stu-id="12a55-187">Please see [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) for more details.</span></span>
* <span data-ttu-id="12a55-188">Corrección de una regresión en la que iniciar procesos de Windows a través de vínculos simbólicos no funcionaba correctamente [GH 3999]</span><span class="sxs-lookup"><span data-stu-id="12a55-188">Fix a regression where launching Windows processes via symlinks did not work correctly [GH 3999]</span></span>
* <span data-ttu-id="12a55-189">Agrega las opciones wsl.exe --list --verbose, wsl.exe --list --quiet y wsl.exe --import --version a wsl.exe</span><span class="sxs-lookup"><span data-stu-id="12a55-189">Add wsl.exe --list --verbose, wsl.exe --list --quiet, and wsl.exe --import --version options to wsl.exe</span></span>
* <span data-ttu-id="12a55-190">Agrega la opción wsl.exe --shutdown</span><span class="sxs-lookup"><span data-stu-id="12a55-190">Add wsl.exe --shutdown option</span></span>
* <span data-ttu-id="12a55-191">Plan 9: Permite abrir un directorio para escribir en él correctamente</span><span class="sxs-lookup"><span data-stu-id="12a55-191">Plan 9: Allow opening a directory for write to succeed</span></span>

## <a name="build-18890"></a><span data-ttu-id="12a55-192">Compilación 18890</span><span class="sxs-lookup"><span data-stu-id="12a55-192">Build 18890</span></span>
<span data-ttu-id="12a55-193">Para obtener información general de Windows sobre la compilación 18890, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span><span class="sxs-lookup"><span data-stu-id="12a55-193">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-194">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-194">WSL</span></span>
* <span data-ttu-id="12a55-195">Pérdida de socket sin bloqueo [GH 2913]</span><span class="sxs-lookup"><span data-stu-id="12a55-195">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="12a55-196">La entrada de EOF en el terminal puede bloquear lecturas posteriores [GH 3421]</span><span class="sxs-lookup"><span data-stu-id="12a55-196">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="12a55-197">Actualización del encabezado de resolv.conf para hacer referencia a wsl.conf [descrito en GH 3928]</span><span class="sxs-lookup"><span data-stu-id="12a55-197">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="12a55-198">Interbloqueo en código de eliminación de epoll [GH 3922]</span><span class="sxs-lookup"><span data-stu-id="12a55-198">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="12a55-199">Control de espacios de los argumentos en -import y -export [GH 3932]</span><span class="sxs-lookup"><span data-stu-id="12a55-199">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="12a55-200">La extensión de los archivos de mmap no funciona correctamente [GH 3939]</span><span class="sxs-lookup"><span data-stu-id="12a55-200">Extending mmap’d files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="12a55-201">Corrección del problema de funcionamiento del acceso a ARM64 \\\\wsl$</span><span class="sxs-lookup"><span data-stu-id="12a55-201">Fix issue with ARM64 \\\\wsl$ access not working properly</span></span>
* <span data-ttu-id="12a55-202">Agrega el mejor icono predeterminado para wsl.exe</span><span class="sxs-lookup"><span data-stu-id="12a55-202">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="12a55-203">Compilación 18342</span><span class="sxs-lookup"><span data-stu-id="12a55-203">Build 18342</span></span>
<span data-ttu-id="12a55-204">Para obtener información general de Windows sobre la compilación 18342, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span><span class="sxs-lookup"><span data-stu-id="12a55-204">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-205">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-205">WSL</span></span>
* <span data-ttu-id="12a55-206">Hemos agregado la posibilidad de que los usuarios accedan a los archivos de Linux en una distribución de WSL desde Windows.</span><span class="sxs-lookup"><span data-stu-id="12a55-206">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="12a55-207">Se puede acceder a estos archivos a través de la línea de comandos; también las aplicaciones de Windows, como el explorador de archivos, VSCode, etc., pueden interactuar con estos archivos.</span><span class="sxs-lookup"><span data-stu-id="12a55-207">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="12a55-208">Para acceder a los archivos, ve a \\\\wsl$\\<nombre_de_distribución>, o consulta la lista de las distribuciones en ejecución en \\\\wsl$</span><span class="sxs-lookup"><span data-stu-id="12a55-208">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="12a55-209">Agrega etiquetas de información de CPU adicionales y corregir valores de Cpus_allowed[_list] [GH 2234]</span><span class="sxs-lookup"><span data-stu-id="12a55-209">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="12a55-210">Compatibilidad con exec desde un subproceso no líder [GH 3800]</span><span class="sxs-lookup"><span data-stu-id="12a55-210">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="12a55-211">Trata errores de actualización de la configuración como no irrecuperables [GH 3785]</span><span class="sxs-lookup"><span data-stu-id="12a55-211">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="12a55-212">Actualización de binfmt para administrar correctamente los desplazamientos [GH 3768]</span><span class="sxs-lookup"><span data-stu-id="12a55-212">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="12a55-213">Habilita la asignación de unidades de red para Plan 9 [GH 3854]</span><span class="sxs-lookup"><span data-stu-id="12a55-213">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="12a55-214">Compatibilidad con traducción de rutas de acceso Windows -> Linux y Linux -> Windows para montajes de enlace</span><span class="sxs-lookup"><span data-stu-id="12a55-214">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="12a55-215">Crea secciones de solo lectura para asignaciones en archivos abiertos de solo lectura</span><span class="sxs-lookup"><span data-stu-id="12a55-215">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="12a55-216">Compilación 18334</span><span class="sxs-lookup"><span data-stu-id="12a55-216">Build 18334</span></span>
<span data-ttu-id="12a55-217">Para obtener información general de Windows sobre la compilación 18334, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span><span class="sxs-lookup"><span data-stu-id="12a55-217">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-218">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-218">WSL</span></span>
* <span data-ttu-id="12a55-219">Rediseña el modo en que se asigna la zona horaria de Windows a una zona horaria de Linux [GH 3747]</span><span class="sxs-lookup"><span data-stu-id="12a55-219">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="12a55-220">Corrección de pérdidas de memoria y adición de nuevas funciones de traducción de cadenas [GH 3746]</span><span class="sxs-lookup"><span data-stu-id="12a55-220">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="12a55-221">SIGCONT en un grupo de subprocesos sin subprocesos es no-op [alvent 3741]</span><span class="sxs-lookup"><span data-stu-id="12a55-221">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="12a55-222">Muestra correctamente los descriptores de archivo de socket y epoll en /proc/self/fd</span><span class="sxs-lookup"><span data-stu-id="12a55-222">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="12a55-223">Compilación 18305</span><span class="sxs-lookup"><span data-stu-id="12a55-223">Build 18305</span></span>
<span data-ttu-id="12a55-224">Para obtener información general de Windows sobre la compilación 18305, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span><span class="sxs-lookup"><span data-stu-id="12a55-224">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-225">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-225">WSL</span></span>
* <span data-ttu-id="12a55-226">pthreads pierden acceso a los archivos cuando sale el subproceso principal [GH 3589]</span><span class="sxs-lookup"><span data-stu-id="12a55-226">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="12a55-227">TIOCSCTTY debe omitir el parámetro "force", a menos que sea necesario [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="12a55-227">TIOCSCTTY should ignore the “force” parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="12a55-228">Mejoras en la línea de comandos de wsl.exe y adición de la funcionalidad de importación y exportación.</span><span class="sxs-lookup"><span data-stu-id="12a55-228">wsl.exe command line improvements and addition of import / export functionality.</span></span>
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

## <a name="build-18277"></a><span data-ttu-id="12a55-229">Compilación 18277</span><span class="sxs-lookup"><span data-stu-id="12a55-229">Build 18277</span></span>
<span data-ttu-id="12a55-230">Para obtener información general de Windows sobre la compilación 18277, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span><span class="sxs-lookup"><span data-stu-id="12a55-230">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-231">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-231">WSL</span></span>
* <span data-ttu-id="12a55-232">Corrección del error "Interfaz no compatible" que se presentó en la compilación 18272 [GH 3645]</span><span class="sxs-lookup"><span data-stu-id="12a55-232">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="12a55-233">Omite la marca MNT_FORCE para la llamada del sistema umount [GH 3605]</span><span class="sxs-lookup"><span data-stu-id="12a55-233">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="12a55-234">Cambia la interoperabilidad de WSL para usar la API de CreatePseudoConsole oficial</span><span class="sxs-lookup"><span data-stu-id="12a55-234">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="12a55-235">No mantiene ningún valor de tiempo de espera cuando se reinicia FUTEX_WAIT</span><span class="sxs-lookup"><span data-stu-id="12a55-235">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="12a55-236">Compilación 18272</span><span class="sxs-lookup"><span data-stu-id="12a55-236">Build 18272</span></span>
<span data-ttu-id="12a55-237">Para obtener información general de Windows sobre la compilación 18272, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span><span class="sxs-lookup"><span data-stu-id="12a55-237">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-238">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-238">WSL</span></span>
* <span data-ttu-id="12a55-239">**ADVERTENCIA:** Hay un problema en esta compilación que hace que WSL sea inoperable.</span><span class="sxs-lookup"><span data-stu-id="12a55-239">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="12a55-240">Al intentar iniciar la distribución, verás el error "Interfaz no compatible".</span><span class="sxs-lookup"><span data-stu-id="12a55-240">When trying to launch your distribution you will see a “No such interface supported” error.</span></span> <span data-ttu-id="12a55-241">El problema se ha solucionado y estará en la compilación del modo anticipado de Insider de la próxima semana.</span><span class="sxs-lookup"><span data-stu-id="12a55-241">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="12a55-242">Si has instalado esta compilación, puedes revertir a la compilación anterior de Windows mediante "Volver a la versión anterior de Windows 10" en Configuración-> Actualización y seguridad > Recuperación.</span><span class="sxs-lookup"><span data-stu-id="12a55-242">If you've installed this build you can roll back to the previous Windows build using “Go back to the previous version of Windows 10” in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="12a55-243">Compilación 18267</span><span class="sxs-lookup"><span data-stu-id="12a55-243">Build 18267</span></span>
<span data-ttu-id="12a55-244">Para obtener información general de Windows sobre la compilación 18267, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span><span class="sxs-lookup"><span data-stu-id="12a55-244">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-245">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-245">WSL</span></span>
* <span data-ttu-id="12a55-246">Corrección del problema por el que un proceso inerte no podía recogerse y permanecía de manera indefinida.</span><span class="sxs-lookup"><span data-stu-id="12a55-246">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="12a55-247">WslRegisterDistribution se bloquea si el mensaje de error supera la longitud máxima [GH 3592]</span><span class="sxs-lookup"><span data-stu-id="12a55-247">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="12a55-248">Permite que fsync se complete correctamente para los archivos de solo lectura en DrvFs [GH 3556]</span><span class="sxs-lookup"><span data-stu-id="12a55-248">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="12a55-249">Asegúrate de que los directorios /bin y /sbin existan antes de crear los vínculos simbólicos en ellos [GH 3584]</span><span class="sxs-lookup"><span data-stu-id="12a55-249">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="12a55-250">Se agregó un mecanismo de tiempo de espera de finalización de instancias para las instancias de WSL.</span><span class="sxs-lookup"><span data-stu-id="12a55-250">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="12a55-251">El tiempo de espera está establecido actualmente en 15 segundos, por lo que la instancia finalizará 15 segundos después de que termine el último proceso de WSL.</span><span class="sxs-lookup"><span data-stu-id="12a55-251">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="12a55-252">Para finalizar una distribución de inmediato, usa:</span><span class="sxs-lookup"><span data-stu-id="12a55-252">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="12a55-253">Compilación 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="12a55-253">Build 17763 (1809)</span></span>
<span data-ttu-id="12a55-254">Para obtener información general de Windows sobre la compilación 17763, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span><span class="sxs-lookup"><span data-stu-id="12a55-254">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-255">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-255">WSL</span></span>
* <span data-ttu-id="12a55-256">Comprobación de permisos de la llamada del sistema setpriority demasiado estricta para cambiar la misma prioridad de subprocesos [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="12a55-256">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="12a55-257">Asegúrate de que se use el tiempo de interrupción no sesgado para el tiempo de arranque para evitar que se devuelvan valores negativos para clock_gettime (CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="12a55-257">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="12a55-258">Controla los vínculos simbólicos en el intérprete binfmt de WSL [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="12a55-258">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="12a55-259">Mejor control de la limpieza de descriptores de archivo del líder del grupo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="12a55-259">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="12a55-260">Cambia WSL para usar KeQueryInterruptTimePrecise en lugar de KeQueryPerformanceCounter para evitar el desbordamiento [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="12a55-260">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="12a55-261">Ptrace attach puede producir un valor de devolución incorrecto de las llamadas del sistema [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="12a55-261">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="12a55-262">Corrección de varios problemas relacionados con AF_UNIX [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="12a55-262">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="12a55-263">Corrección del problema que podía provocar un error de interoperabilidad de WSL si el directorio de trabajo actual tiene menos de 5 caracteres de longitud [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="12a55-263">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="12a55-264">Evita las conexiones de bucle invertido con error con retraso de un segundo a puertos no existentes [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="12a55-264">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="12a55-265">Agrega el archivo de código auxiliar /proc/sys/fs/file-max [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="12a55-265">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="12a55-266">Información más precisa sobre el ámbito IPV6.</span><span class="sxs-lookup"><span data-stu-id="12a55-266">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="12a55-267">Compatibilidad con PR_SET_PTRACER [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="12a55-267">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="12a55-268">El sistema de archivos de canalización borra accidentalmente el evento epoll desencadenado por el borde [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="12a55-268">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="12a55-269">El ejecutable de Win32 iniciado mediante el vínculo simbólico de NTFS no respeta el nombre del vínculo simbólico [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="12a55-269">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="12a55-270">Compatibilidad mejorada con zombie [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="12a55-270">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="12a55-271">Agrega entradas de wsl.conf para controlar el comportamiento de interoperabilidad de Windows [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="12a55-271">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="12a55-272">La corrección para getsockname no siempre devuelve el tipo de familia de socket de UNIX [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="12a55-272">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="12a55-273">Agrega compatibilidad para TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="12a55-273">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="12a55-274">Los sockets sin bloqueo en el proceso de conexión deben devolver EAGAIN para los intentos de escritura [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="12a55-274">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="12a55-275">Compatibilidad con la interoperabilidad en VHD montados [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="12a55-275">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="12a55-276">Corrección del problema de comprobación de permisos en la carpeta raíz [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="12a55-276">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="12a55-277">Compatibilidad limitada para los ioctl de teclado TTY KDGKBTYPE, KDGKBMODE y KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="12a55-277">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="12a55-278">Las aplicaciones de interfaz de usuario de Windows deben ejecutarse incluso cuando se inician en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="12a55-278">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="12a55-279">Agrega la opción wsl -u o --user [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="12a55-279">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="12a55-280">Corrección de problemas de inicio de WSL cuando el inicio rápido está habilitado [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="12a55-280">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="12a55-281">Los sockets de UNIX deben conservar las credenciales del mismo nivel desconectadas [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="12a55-281">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="12a55-282">Sockets de UNIX sin bloqueo con error de manera indefinida con EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="12a55-282">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="12a55-283">case=off es el nuevo tipo de montaje drvfs predeterminado [GH 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="12a55-283">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="12a55-284">Consulta el [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) para más información.</span><span class="sxs-lookup"><span data-stu-id="12a55-284">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="12a55-285">Agrega wslconfig/terminate para detener las distribuciones en ejecución.</span><span class="sxs-lookup"><span data-stu-id="12a55-285">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="12a55-286">Corrección del problema con las entradas del menú contextual del shell de WSL que no controlan correctamente las rutas de acceso con espacios.</span><span class="sxs-lookup"><span data-stu-id="12a55-286">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="12a55-287">Expone la distinción de mayúsculas y minúsculas por directorio como atributo extendido</span><span class="sxs-lookup"><span data-stu-id="12a55-287">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="12a55-288">ARM64: Emula las operaciones de mantenimiento de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="12a55-288">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="12a55-289">Resuelve un [problema de dotnet](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="12a55-289">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="12a55-290">DrvFs: solo caracteres con escape eliminado en el intervalo privado que corresponden a un carácter de escape.</span><span class="sxs-lookup"><span data-stu-id="12a55-290">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="12a55-291">Corrección error de desviación por uno en la validación de longitud del intérprete del analizador ELF [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="12a55-291">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="12a55-292">Temporizadores absolutos de WSL con una hora en el pasado no se activan [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="12a55-292">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="12a55-293">Asegúrate de que los puntos de reanálisis recién creados se muestren como tales en el directorio principal.</span><span class="sxs-lookup"><span data-stu-id="12a55-293">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="12a55-294">Crea de forma atómica directorios con distinción entre mayúsculas y minúsculas en DrvFs.</span><span class="sxs-lookup"><span data-stu-id="12a55-294">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="12a55-295">Se ha corregido un problema adicional en el que las operaciones de varios subprocesos podían devolver ENOENT, aunque el archivo existiese.</span><span class="sxs-lookup"><span data-stu-id="12a55-295">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="12a55-296">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="12a55-296">[GH 2712]</span></span>
* <span data-ttu-id="12a55-297">Se corrigió un error de inicio de WSL cuando UMCI está habilitado.</span><span class="sxs-lookup"><span data-stu-id="12a55-297">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="12a55-298">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="12a55-298">[GH 3020]</span></span>
* <span data-ttu-id="12a55-299">Agrega el menú contextual del explorador para iniciar WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="12a55-299">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="12a55-300">Para usar, mantén presionada la tecla Mayús y haz clic con el botón derecho en una ventana del explorador.</span><span class="sxs-lookup"><span data-stu-id="12a55-300">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="12a55-301">Corrección del comportamiento de no bloqueo de sockets de UNIX [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="12a55-301">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="12a55-302">Corrección del comando NETLINK que se bloquea, tal como se muestra en GH 2026.</span><span class="sxs-lookup"><span data-stu-id="12a55-302">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="12a55-303">Agrega compatibilidad para las marcas de propagación de montaje [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="12a55-303">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="12a55-304">Corrección del problema de truncamiento que no provoca eventos inotify [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="12a55-304">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="12a55-305">Agrega la opción --exec a wsl.exe para invocar un solo binario sin un shell.</span><span class="sxs-lookup"><span data-stu-id="12a55-305">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="12a55-306">Agrega la opción --distribution a wsl.exe para seleccionar una distribución específica.</span><span class="sxs-lookup"><span data-stu-id="12a55-306">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="12a55-307">Compatibilidad limitada para dmesg.</span><span class="sxs-lookup"><span data-stu-id="12a55-307">Limited support for dmesg.</span></span> <span data-ttu-id="12a55-308">Ahora, las aplicaciones pueden registrarse en dmesg.</span><span class="sxs-lookup"><span data-stu-id="12a55-308">Applications can now log to dmesg.</span></span> <span data-ttu-id="12a55-309">El controlador WSL registra información limitada en dmesg.</span><span class="sxs-lookup"><span data-stu-id="12a55-309">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="12a55-310">En el futuro, esto puede extenderse para llevar a cabo otros diagnósticos e información del controlador.</span><span class="sxs-lookup"><span data-stu-id="12a55-310">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="12a55-311">Nota: dmesg se admite actualmente a través de la interfaz de dispositivo `/dev/kmsg`.</span><span class="sxs-lookup"><span data-stu-id="12a55-311">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="12a55-312">Aún no se admite la interfaz syscall `syslog`.</span><span class="sxs-lookup"><span data-stu-id="12a55-312">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="12a55-313">Y, por lo tanto, algunas de las opciones de la línea de comandos de `dmesg`, como `-S` y `-C`, no funcionan.</span><span class="sxs-lookup"><span data-stu-id="12a55-313">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="12a55-314">Cambia el gid y el modo de dispositivos serie predeterminados para que coincidan con los nativos [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="12a55-314">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="12a55-315">DrvFs ahora admite atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="12a55-315">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="12a55-316">Nota: DrvFs tiene algunas limitaciones en cuanto al nombre de los atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="12a55-316">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="12a55-317">No se permiten algunos caracteres (como "/", ":" y "\*"), y los nombres de atributos extendidos no distinguen mayúsculas de minúsculas en DrvFs</span><span class="sxs-lookup"><span data-stu-id="12a55-317">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="12a55-318">Compilación 18252 (saltar)</span><span class="sxs-lookup"><span data-stu-id="12a55-318">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="12a55-319">Para obtener información general de Windows sobre la compilación 18252, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span><span class="sxs-lookup"><span data-stu-id="12a55-319">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-320">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-320">WSL</span></span>
* <span data-ttu-id="12a55-321">Traslado de los binarios init y bsdtar fuera del archivo dll lxssmanager y a una carpeta de herramientas independiente</span><span class="sxs-lookup"><span data-stu-id="12a55-321">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="12a55-322">Corrección de la carrera en torno al cierre del descriptor de archivo cuando se usa CLONE_FILES</span><span class="sxs-lookup"><span data-stu-id="12a55-322">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="12a55-323">Controla campos opcionales en /proc/pid/mountinfo al traducir rutas de DrvFs</span><span class="sxs-lookup"><span data-stu-id="12a55-323">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="12a55-324">Permite que DrvFs mknod se complete correctamente sin compatibilidad con metadatos para S_IFREG</span><span class="sxs-lookup"><span data-stu-id="12a55-324">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="12a55-325">Los archivos de solo lectura creados en DrvFs deben tener el atributo readonly establecido [GH 3411]</span><span class="sxs-lookup"><span data-stu-id="12a55-325">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="12a55-326">Agrega el asistente /sbin/mount.drvfs para controlar el montaje de DrvFs</span><span class="sxs-lookup"><span data-stu-id="12a55-326">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="12a55-327">Usa el cambio de nombre de POSIX en DrvFs.</span><span class="sxs-lookup"><span data-stu-id="12a55-327">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="12a55-328">Permite la traducción de rutas de acceso en volúmenes sin un GUID de volumen.</span><span class="sxs-lookup"><span data-stu-id="12a55-328">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="12a55-329">Compilación 17738 (rápida)</span><span class="sxs-lookup"><span data-stu-id="12a55-329">Build 17738 (Fast)</span></span>
<span data-ttu-id="12a55-330">Para obtener información general de Windows sobre la compilación 17738, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span><span class="sxs-lookup"><span data-stu-id="12a55-330">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-331">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-331">WSL</span></span>
* <span data-ttu-id="12a55-332">Comprobación de permisos de la llamada del sistema setpriority demasiado estricta para cambiar la misma prioridad de subprocesos [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="12a55-332">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="12a55-333">Asegúrate de que se use el tiempo de interrupción no sesgado para el tiempo de arranque para evitar que se devuelvan valores negativos para clock_gettime (CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="12a55-333">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="12a55-334">Controla los vínculos simbólicos en el intérprete binfmt de WSL [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="12a55-334">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="12a55-335">Mejor control de la limpieza de descriptores de archivo del líder del grupo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="12a55-335">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="12a55-336">Compilación 17728 (rápida)</span><span class="sxs-lookup"><span data-stu-id="12a55-336">Build 17728 (Fast)</span></span>
<span data-ttu-id="12a55-337">Para obtener información general de Windows sobre la compilación 17728, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span><span class="sxs-lookup"><span data-stu-id="12a55-337">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-338">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-338">WSL</span></span>
* <span data-ttu-id="12a55-339">Cambia WSL para usar KeQueryInterruptTimePrecise en lugar de KeQueryPerformanceCounter para evitar el desbordamiento [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="12a55-339">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="12a55-340">Ptrace attach puede producir un valor de devolución incorrecto de las llamadas del sistema [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="12a55-340">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="12a55-341">Corrección de varios problemas relacionados con AF_UNIX [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="12a55-341">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="12a55-342">Corrección del problema que podía provocar un error de interoperabilidad de WSL si el directorio de trabajo actual tiene menos de 5 caracteres de longitud [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="12a55-342">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="12a55-343">Compilación 18204 (saltar)</span><span class="sxs-lookup"><span data-stu-id="12a55-343">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="12a55-344">Para obtener información general de Windows sobre la compilación 18204, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="12a55-344">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-345">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-345">WSL</span></span>
* <span data-ttu-id="12a55-346">El sistema de archivos de canalización borra accidentalmente el evento epoll desencadenado por el borde [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="12a55-346">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="12a55-347">El ejecutable de Win32 iniciado mediante el vínculo simbólico de NTFS no respeta el nombre del vínculo simbólico [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="12a55-347">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="12a55-348">Compilación 17723 (rápida)</span><span class="sxs-lookup"><span data-stu-id="12a55-348">Build 17723 (Fast)</span></span>
<span data-ttu-id="12a55-349">Para obtener información general de Windows sobre la compilación 17723, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="12a55-349">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-350">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-350">WSL</span></span>
* <span data-ttu-id="12a55-351">Evita las conexiones de bucle invertido con error con retraso de un segundo a puertos no existentes [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="12a55-351">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="12a55-352">Agrega el archivo de código auxiliar /proc/sys/fs/file-max [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="12a55-352">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="12a55-353">Información más precisa sobre el ámbito IPV6.</span><span class="sxs-lookup"><span data-stu-id="12a55-353">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="12a55-354">Compatibilidad con PR_SET_PTRACER [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="12a55-354">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="12a55-355">El sistema de archivos de canalización borra accidentalmente el evento epoll desencadenado por el borde [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="12a55-355">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="12a55-356">El ejecutable de Win32 iniciado mediante el vínculo simbólico de NTFS no respeta el nombre del vínculo simbólico [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="12a55-356">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="12a55-357">Compilación 17713</span><span class="sxs-lookup"><span data-stu-id="12a55-357">Build 17713</span></span>
<span data-ttu-id="12a55-358">Para obtener información general de Windows sobre la compilación 17713, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span><span class="sxs-lookup"><span data-stu-id="12a55-358">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-359">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-359">WSL</span></span>
* <span data-ttu-id="12a55-360">Compatibilidad mejorada con zombie [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="12a55-360">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="12a55-361">Agrega entradas de wsl.conf para controlar el comportamiento de interoperabilidad de Windows [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="12a55-361">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="12a55-362">La corrección para getsockname no siempre devuelve el tipo de familia de socket de UNIX [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="12a55-362">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="12a55-363">Agrega compatibilidad para TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="12a55-363">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="12a55-364">Los sockets sin bloqueo en el proceso de conexión deben devolver EAGAIN para los intentos de escritura [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="12a55-364">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="12a55-365">Compatibilidad con la interoperabilidad en VHD montados [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="12a55-365">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="12a55-366">Corrección del problema de comprobación de permisos en la carpeta raíz [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="12a55-366">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="12a55-367">Compatibilidad limitada para los ioctl de teclado TTY KDGKBTYPE, KDGKBMODE y KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="12a55-367">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="12a55-368">Las aplicaciones de interfaz de usuario de Windows deben ejecutarse incluso cuando se inician en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="12a55-368">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="12a55-369">Compilación 17704</span><span class="sxs-lookup"><span data-stu-id="12a55-369">Build 17704</span></span>
<span data-ttu-id="12a55-370">Para obtener información general de Windows sobre la compilación 17704, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span><span class="sxs-lookup"><span data-stu-id="12a55-370">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-371">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-371">WSL</span></span>
* <span data-ttu-id="12a55-372">Agrega la opción wsl -u o --user [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="12a55-372">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="12a55-373">Corrección de problemas de inicio de WSL cuando el inicio rápido está habilitado [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="12a55-373">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="12a55-374">Los sockets de UNIX deben conservar las credenciales del mismo nivel desconectadas [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="12a55-374">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="12a55-375">Sockets de UNIX sin bloqueo con error de manera indefinida con EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="12a55-375">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="12a55-376">case=off es el nuevo tipo de montaje drvfs predeterminado [GH 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="12a55-376">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="12a55-377">Consulta el [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) para más información.</span><span class="sxs-lookup"><span data-stu-id="12a55-377">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="12a55-378">Agrega wslconfig/terminate para detener las distribuciones en ejecución.</span><span class="sxs-lookup"><span data-stu-id="12a55-378">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="12a55-379">Compilación 17692</span><span class="sxs-lookup"><span data-stu-id="12a55-379">Build 17692</span></span>
<span data-ttu-id="12a55-380">Para obtener información general de Windows sobre la compilación 17692, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span><span class="sxs-lookup"><span data-stu-id="12a55-380">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-381">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-381">WSL</span></span>
* <span data-ttu-id="12a55-382">Corrección del problema con las entradas del menú contextual del shell de WSL que no controlan correctamente las rutas de acceso con espacios.</span><span class="sxs-lookup"><span data-stu-id="12a55-382">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="12a55-383">Expone la distinción de mayúsculas y minúsculas por directorio como atributo extendido</span><span class="sxs-lookup"><span data-stu-id="12a55-383">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="12a55-384">ARM64: Emula las operaciones de mantenimiento de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="12a55-384">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="12a55-385">Resuelve un [problema de dotnet](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="12a55-385">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="12a55-386">DrvFs: solo caracteres con escape eliminado en el intervalo privado que corresponden a un carácter de escape.</span><span class="sxs-lookup"><span data-stu-id="12a55-386">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="12a55-387">Compilación 17686</span><span class="sxs-lookup"><span data-stu-id="12a55-387">Build 17686</span></span>
<span data-ttu-id="12a55-388">Para obtener información general de Windows sobre la compilación 17686, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span><span class="sxs-lookup"><span data-stu-id="12a55-388">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-389">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-389">WSL</span></span>
* <span data-ttu-id="12a55-390">Corrección error de desviación por uno en la validación de longitud del intérprete del analizador ELF [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="12a55-390">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="12a55-391">Temporizadores absolutos de WSL con una hora en el pasado no se activan [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="12a55-391">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="12a55-392">Asegúrate de que los puntos de reanálisis recién creados se muestren como tales en el directorio principal.</span><span class="sxs-lookup"><span data-stu-id="12a55-392">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="12a55-393">Crea de forma atómica directorios con distinción entre mayúsculas y minúsculas en DrvFs.</span><span class="sxs-lookup"><span data-stu-id="12a55-393">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="12a55-394">Compilación 17677</span><span class="sxs-lookup"><span data-stu-id="12a55-394">Build 17677</span></span>
<span data-ttu-id="12a55-395">Para obtener información general de Windows sobre la compilación 17677, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span><span class="sxs-lookup"><span data-stu-id="12a55-395">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-396">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-396">WSL</span></span>
* <span data-ttu-id="12a55-397">Se ha corregido un problema adicional en el que las operaciones de varios subprocesos podían devolver ENOENT, aunque el archivo existiese.</span><span class="sxs-lookup"><span data-stu-id="12a55-397">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="12a55-398">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="12a55-398">[GH 2712]</span></span>
* <span data-ttu-id="12a55-399">Se corrigió un error de inicio de WSL cuando UMCI está habilitado.</span><span class="sxs-lookup"><span data-stu-id="12a55-399">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="12a55-400">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="12a55-400">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="12a55-401">Compilación 17666</span><span class="sxs-lookup"><span data-stu-id="12a55-401">Build 17666</span></span>
<span data-ttu-id="12a55-402">Para obtener información general de Windows sobre la compilación 17666, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span><span class="sxs-lookup"><span data-stu-id="12a55-402">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-403">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-403">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="12a55-404">ADVERTENCIA: Hay un problema que impide que WSL se ejecute en algunos conjuntos de chips AMD [GH 3134].</span><span class="sxs-lookup"><span data-stu-id="12a55-404">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="12a55-405">Hay una corrección lista y en camino en la rama de compilación de Insider.</span><span class="sxs-lookup"><span data-stu-id="12a55-405">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="12a55-406">Agrega el menú contextual del explorador para iniciar WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="12a55-406">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="12a55-407">Para usar, mantén presionada la tecla Mayús y haz clic con el botón derecho en una ventana del explorador.</span><span class="sxs-lookup"><span data-stu-id="12a55-407">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="12a55-408">Corrección del comportamiento de no bloqueo de sockets de Unix [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="12a55-408">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="12a55-409">Corrección del comando NETLINK que se bloquea, tal como se muestra en GH 2026.</span><span class="sxs-lookup"><span data-stu-id="12a55-409">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="12a55-410">Agrega compatibilidad para las marcas de propagación de montaje [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="12a55-410">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="12a55-411">Corrección del problema de truncamiento que no provoca eventos inotify [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="12a55-411">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="12a55-412">Agrega la opción --exec a wsl.exe para invocar un solo binario sin un shell.</span><span class="sxs-lookup"><span data-stu-id="12a55-412">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="12a55-413">Agrega la opción --distribution a wsl.exe para seleccionar una distribución específica.</span><span class="sxs-lookup"><span data-stu-id="12a55-413">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="12a55-414">Compilación 17655 (saltar)</span><span class="sxs-lookup"><span data-stu-id="12a55-414">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="12a55-415">Para obtener información general de Windows sobre la compilación 17655, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="12a55-415">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-416">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-416">WSL</span></span>
* <span data-ttu-id="12a55-417">Compatibilidad limitada para dmesg.</span><span class="sxs-lookup"><span data-stu-id="12a55-417">Limited support for dmesg.</span></span> <span data-ttu-id="12a55-418">Ahora, las aplicaciones pueden registrarse en dmesg.</span><span class="sxs-lookup"><span data-stu-id="12a55-418">Applications can now log to dmesg.</span></span> <span data-ttu-id="12a55-419">El controlador WSL registra información limitada en dmesg.</span><span class="sxs-lookup"><span data-stu-id="12a55-419">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="12a55-420">En el futuro, esto puede extenderse para llevar a cabo otros diagnósticos e información del controlador.</span><span class="sxs-lookup"><span data-stu-id="12a55-420">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="12a55-421">Nota: dmesg se admite actualmente a través de la interfaz de dispositivo `/dev/kmsg`.</span><span class="sxs-lookup"><span data-stu-id="12a55-421">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="12a55-422">Aún no se admite la interfaz sycall `syslog`.</span><span class="sxs-lookup"><span data-stu-id="12a55-422">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="12a55-423">Y, por lo tanto, algunas de las opciones de la línea de comandos de `dmesg`, como `-S` y `-C`, no funcionan.</span><span class="sxs-lookup"><span data-stu-id="12a55-423">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="12a55-424">Se ha corregido un problema en el que las operaciones de varios subprocesos podían devolver ENOENT, aunque el archivo existiese.</span><span class="sxs-lookup"><span data-stu-id="12a55-424">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="12a55-425">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="12a55-425">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="12a55-426">Compilación 17639 (saltar)</span><span class="sxs-lookup"><span data-stu-id="12a55-426">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="12a55-427">Para obtener información general de Windows sobre la compilación 17639, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="12a55-427">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-428">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-428">WSL</span></span>
* <span data-ttu-id="12a55-429">Cambia el gid y el modo de dispositivos serie predeterminados para que coincidan con los nativos [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="12a55-429">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="12a55-430">DrvFs ahora admite atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="12a55-430">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="12a55-431">Nota: DrvFs tiene algunas limitaciones en cuanto al nombre de los atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="12a55-431">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="12a55-432">En particular, no se permiten algunos caracteres (como "/", ":" y "\*"), y los nombres de atributos extendidos no distinguen mayúsculas de minúsculas en DrvFs</span><span class="sxs-lookup"><span data-stu-id="12a55-432">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="12a55-433">Compilación 17133 (rápida)</span><span class="sxs-lookup"><span data-stu-id="12a55-433">Build 17133 (Fast)</span></span>
<span data-ttu-id="12a55-434">Para obtener información general de Windows sobre la compilación 17133, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="12a55-434">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-435">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-435">WSL</span></span>
* <span data-ttu-id="12a55-436">Corrección de un bloqueo en WSL.</span><span class="sxs-lookup"><span data-stu-id="12a55-436">Fix for hang in WSL.</span></span> <span data-ttu-id="12a55-437">[GH 3039, 3034]</span><span class="sxs-lookup"><span data-stu-id="12a55-437">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="12a55-438">Compilación 17128 (rápida)</span><span class="sxs-lookup"><span data-stu-id="12a55-438">Build 17128 (Fast)</span></span>
<span data-ttu-id="12a55-439">Para obtener información general de Windows sobre la compilación 17128, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="12a55-439">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-440">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-440">WSL</span></span>
* <span data-ttu-id="12a55-441">Ninguno</span><span class="sxs-lookup"><span data-stu-id="12a55-441">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="12a55-442">Compilación 17627 (saltar)</span><span class="sxs-lookup"><span data-stu-id="12a55-442">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="12a55-443">Para obtener información general de Windows sobre la compilación 17627, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="12a55-443">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-444">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-444">WSL</span></span>
* <span data-ttu-id="12a55-445">Agrega compatibilidad para las operaciones compatibles con pi de Futex.</span><span class="sxs-lookup"><span data-stu-id="12a55-445">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="12a55-446">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="12a55-446">[GH 1006]</span></span>
    * <span data-ttu-id="12a55-447">Ten en cuenta que las prioridades no son actualmente una característica admitida de WSL, por lo que hay limitaciones, pero el uso estándar debería estar desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="12a55-447">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="12a55-448">Compatibilidad con el Firewall de Windows para los procesos de WSL.</span><span class="sxs-lookup"><span data-stu-id="12a55-448">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="12a55-449">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="12a55-449">[GH 1852]</span></span>
    * <span data-ttu-id="12a55-450">Por ejemplo, para permitir que el proceso de Python de WSL escuche en cualquier puerto, use el cmd de Windows con privilegios elevados: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span><span class="sxs-lookup"><span data-stu-id="12a55-450">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="12a55-451">Para más información sobre cómo agregar reglas de firewall, consulte el [vínculo](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span><span class="sxs-lookup"><span data-stu-id="12a55-451">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="12a55-452">Respeta el shell predeterminado del usuario al usar wsl.exe.</span><span class="sxs-lookup"><span data-stu-id="12a55-452">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="12a55-453">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="12a55-453">[GH 2372]</span></span>
* <span data-ttu-id="12a55-454">Informa de todas las interfaces de red como Ethernet.</span><span class="sxs-lookup"><span data-stu-id="12a55-454">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="12a55-455">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="12a55-455">[GH 2996]</span></span>
* <span data-ttu-id="12a55-456">Mejor control del archivo /etc/passwd dañado.</span><span class="sxs-lookup"><span data-stu-id="12a55-456">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="12a55-457">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="12a55-457">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="12a55-458">Console</span><span class="sxs-lookup"><span data-stu-id="12a55-458">Console</span></span>
* <span data-ttu-id="12a55-459">Sin correcciones.</span><span class="sxs-lookup"><span data-stu-id="12a55-459">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-460">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-460">LTP Results:</span></span>
<span data-ttu-id="12a55-461">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="12a55-461">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="12a55-462">Compilación 17618 (saltar)</span><span class="sxs-lookup"><span data-stu-id="12a55-462">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="12a55-463">Para obtener información general de Windows sobre la compilación 17618, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="12a55-463">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-464">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-464">WSL</span></span>
* <span data-ttu-id="12a55-465">Presenta la funcionalidad de pseudoconsola para la interoperabilidad de NT [GH 988, 1366, 1433, 1542, 2370, 2406].</span><span class="sxs-lookup"><span data-stu-id="12a55-465">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="12a55-466">El mecanismo de instalación heredado (lxrun.exe) está en desuso.</span><span class="sxs-lookup"><span data-stu-id="12a55-466">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="12a55-467">El mecanismo admitido para la instalación de distribuciones es a través de Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="12a55-467">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="12a55-468">Console</span><span class="sxs-lookup"><span data-stu-id="12a55-468">Console</span></span>
* <span data-ttu-id="12a55-469">Sin correcciones.</span><span class="sxs-lookup"><span data-stu-id="12a55-469">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-470">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-470">LTP Results:</span></span>
<span data-ttu-id="12a55-471">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="12a55-471">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="12a55-472">Compilación 17110</span><span class="sxs-lookup"><span data-stu-id="12a55-472">Build 17110</span></span>
<span data-ttu-id="12a55-473">Para obtener información general de Windows sobre la compilación 17110, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span><span class="sxs-lookup"><span data-stu-id="12a55-473">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-474">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-474">WSL</span></span>
* <span data-ttu-id="12a55-475">Permite que/init finalice desde Windows [GH 2928].</span><span class="sxs-lookup"><span data-stu-id="12a55-475">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="12a55-476">DrvFs ahora usa la distinción de mayúsculas y minúsculas por directorio de manera predeterminada (equivalente a la opción de montaje "case=dir").</span><span class="sxs-lookup"><span data-stu-id="12a55-476">DrvFs now uses per-directory case sensitivity by default (equivalent to the “case=dir” mount option).</span></span>
    * <span data-ttu-id="12a55-477">El uso de "case=force" (el comportamiento anterior) requiere el establecimiento de una clave del Registro.</span><span class="sxs-lookup"><span data-stu-id="12a55-477">Using “case=force” (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="12a55-478">Ejecuta el siguiente comando para habilitar "case=force" si necesitas usarlo: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span><span class="sxs-lookup"><span data-stu-id="12a55-478">Run the following command to enable “case=force” if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="12a55-479">Si tienes directorios existentes creados con WSL en una versión anterior de Windows que deben distinguir entre mayúsculas y minúsculas, usa fsutil.exe para marcarlos con distinción de mayúsculas y minúsculas:fsutil.exe file setcasesensitiveinfo <path> enable</span><span class="sxs-lookup"><span data-stu-id="12a55-479">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="12a55-480">La llamada del sistema uname devuelve cadenas de finalización NULL.</span><span class="sxs-lookup"><span data-stu-id="12a55-480">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="12a55-481">Console</span><span class="sxs-lookup"><span data-stu-id="12a55-481">Console</span></span>
* <span data-ttu-id="12a55-482">Sin correcciones.</span><span class="sxs-lookup"><span data-stu-id="12a55-482">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-483">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-483">LTP Results:</span></span>
<span data-ttu-id="12a55-484">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="12a55-484">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="12a55-485">Compilación 17107</span><span class="sxs-lookup"><span data-stu-id="12a55-485">Build 17107</span></span>
<span data-ttu-id="12a55-486">Para obtener información general de Windows sobre la compilación 17107, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span><span class="sxs-lookup"><span data-stu-id="12a55-486">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-487">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-487">WSL</span></span>
* <span data-ttu-id="12a55-488">Compatibilidad con TCSETSF y TCSETSW en los puntos de conexión de master pty [GH 2552].</span><span class="sxs-lookup"><span data-stu-id="12a55-488">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="12a55-489">Iniciar procesos de interoperabilidad simultáneos puede dar lugar a EINVAL [GH 2813].</span><span class="sxs-lookup"><span data-stu-id="12a55-489">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="12a55-490">Corrección de PTRACE_ATTACH para mostrar el estado de seguimiento adecuado en /proc/pid/status.</span><span class="sxs-lookup"><span data-stu-id="12a55-490">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="12a55-491">Corrección de la carrera en la que los procesos de corta duración clonados con las marcas CLEARTID y SETTID podrían salir sin borrar la dirección de TID.</span><span class="sxs-lookup"><span data-stu-id="12a55-491">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="12a55-492">Muestra un mensaje al actualizar los directorios del sistema de archivos de Linux al pasar de una compilación anterior a 17093.</span><span class="sxs-lookup"><span data-stu-id="12a55-492">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="12a55-493">Para más detalles sobre los cambios del sistema de archivos de 17093, consulta las notas de la versión de [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span><span class="sxs-lookup"><span data-stu-id="12a55-493">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="12a55-494">Console</span><span class="sxs-lookup"><span data-stu-id="12a55-494">Console</span></span>
* <span data-ttu-id="12a55-495">Sin correcciones.</span><span class="sxs-lookup"><span data-stu-id="12a55-495">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-496">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-496">LTP Results:</span></span>
<span data-ttu-id="12a55-497">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="12a55-497">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="12a55-498">Compilación 17101</span><span class="sxs-lookup"><span data-stu-id="12a55-498">Build 17101</span></span>
<span data-ttu-id="12a55-499">Para obtener información general de Windows sobre la compilación 17101, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="12a55-499">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-500">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-500">WSL</span></span>
* <span data-ttu-id="12a55-501">Compatibilidad con signalfd.</span><span class="sxs-lookup"><span data-stu-id="12a55-501">Support for signalfd.</span></span> <span data-ttu-id="12a55-502">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="12a55-502">[GH 129]</span></span>
* <span data-ttu-id="12a55-503">Admite nombres de archivo que contienen caracteres NTFS no válidos mediante su codificación como caracteres Unicode privados.</span><span class="sxs-lookup"><span data-stu-id="12a55-503">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="12a55-504">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="12a55-504">[GH 1514]</span></span>
* <span data-ttu-id="12a55-505">El montaje automático se revertirá al modo de solo lectura cuando no se admita la escritura.</span><span class="sxs-lookup"><span data-stu-id="12a55-505">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="12a55-506">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="12a55-506">[GH 2603]</span></span>
* <span data-ttu-id="12a55-507">Permite pegar los pares suplentes Unicode (como los caracteres emoji).</span><span class="sxs-lookup"><span data-stu-id="12a55-507">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="12a55-508">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="12a55-508">[GH 2765]</span></span>
* <span data-ttu-id="12a55-509">Los pseudoarchivos en /proc y /sys deben devolver los valores read ready y write ready de select, poll, epoll, etc. [GH 2838]</span><span class="sxs-lookup"><span data-stu-id="12a55-509">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="12a55-510">Corrección de un problema que podría hacer que el servicio pudiera entrar en un bucle infinito cuando el Registro se haya alterado o esté dañado.</span><span class="sxs-lookup"><span data-stu-id="12a55-510">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="12a55-511">Corrección de los mensajes de netlink para trabajar con la versión más reciente (de nivel superior 4.14) de iproute2.</span><span class="sxs-lookup"><span data-stu-id="12a55-511">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="12a55-512">Console</span><span class="sxs-lookup"><span data-stu-id="12a55-512">Console</span></span>
* <span data-ttu-id="12a55-513">Sin correcciones.</span><span class="sxs-lookup"><span data-stu-id="12a55-513">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-514">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-514">LTP Results:</span></span>
<span data-ttu-id="12a55-515">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="12a55-515">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="12a55-516">Compilación 17093</span><span class="sxs-lookup"><span data-stu-id="12a55-516">Build 17093</span></span>
<span data-ttu-id="12a55-517">Para obtener información general de Windows sobre la compilación 17093, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span><span class="sxs-lookup"><span data-stu-id="12a55-517">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="12a55-518">Importante:</span><span class="sxs-lookup"><span data-stu-id="12a55-518">Important:</span></span>
<span data-ttu-id="12a55-519">Al iniciar WSL por primera vez después de actualizar a esta compilación, tiene que hacer algún trabajo para actualizar los directorios del sistema de archivos de Linux.</span><span class="sxs-lookup"><span data-stu-id="12a55-519">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="12a55-520">Esto puede tardar varios minutos, por lo que es posible que WSL se inicie lentamente.</span><span class="sxs-lookup"><span data-stu-id="12a55-520">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="12a55-521">Esto solo debería ocurrir una vez por cada distribución que haya instalado desde Store.</span><span class="sxs-lookup"><span data-stu-id="12a55-521">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="12a55-522">Compatibilidad mejorada de distinción de mayúsculas y minúsculas en DrvFs.</span><span class="sxs-lookup"><span data-stu-id="12a55-522">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="12a55-523">DrvFs admite ahora la distinción de mayúsculas y minúsculas por directorio.</span><span class="sxs-lookup"><span data-stu-id="12a55-523">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="12a55-524">Se trata de una nueva marca que se puede establecer en los directorios para indicar que todas las operaciones de esos directorios deben tratarse como con distinción de mayúsculas y minúsculas, lo que permite que las aplicaciones de Windows abran correctamente archivos que solo difieren en mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="12a55-524">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="12a55-525">DrvFs tiene nuevas opciones de montaje que controlan la distinción de mayúsculas y minúsculas por directorio.</span><span class="sxs-lookup"><span data-stu-id="12a55-525">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="12a55-526">case=force: todos los directorios se tratan con distinción de mayúsculas y minúsculas (excepto la raíz de la unidad).</span><span class="sxs-lookup"><span data-stu-id="12a55-526">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="12a55-527">Los nuevos directorios creados con WSL se marcan con distinción de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="12a55-527">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="12a55-528">Este es el comportamiento heredado, excepto para marcar los nuevos directorios que distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="12a55-528">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="12a55-529">case=dir: solo los directorios con la marca de distinción de mayúsculas y minúsculas por directorio se tratan como que distinguen mayúsculas de minúsculas; los otros directorios no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="12a55-529">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="12a55-530">Los nuevos directorios creados con WSL se marcan con distinción de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="12a55-530">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="12a55-531">case=off: solo los directorios con la marca de distinción de mayúsculas y minúsculas por directorio se tratan como que distinguen mayúsculas de minúsculas; los otros directorios no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="12a55-531">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="12a55-532">Los nuevos directorios creados con WSL se marcan como sin distinción de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="12a55-532">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="12a55-533">Nota: Los directorios creados por WSL en versiones anteriores no tienen esta marca establecida, por lo que no se tratará como con distinción entre mayúsculas y minúsculas si usas la opción "case=dir".</span><span class="sxs-lookup"><span data-stu-id="12a55-533">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the “case=dir” option.</span></span> <span data-ttu-id="12a55-534">Próximamente se presentará una manera de establecer esta marca en los directorios existentes.</span><span class="sxs-lookup"><span data-stu-id="12a55-534">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="12a55-535">Ejemplo de montaje con estas opciones (en el caso de las unidades existentes, primero debes desmontar antes de poder montar con distintas opciones): sudo mount -t drvfs C: /mnt/c -o case=dir</span><span class="sxs-lookup"><span data-stu-id="12a55-535">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="12a55-536">Por ahora, case=force sigue siendo la opción predeterminada.</span><span class="sxs-lookup"><span data-stu-id="12a55-536">For now, case=force is still the default option.</span></span> <span data-ttu-id="12a55-537">Se cambiará a case=dir en el futuro.</span><span class="sxs-lookup"><span data-stu-id="12a55-537">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="12a55-538">Ahora puedes usar barras diagonales en las rutas de acceso de Windows al montar DrvFs, por ejemplo: sudo mount -t drvfs //server/share /mnt/share</span><span class="sxs-lookup"><span data-stu-id="12a55-538">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="12a55-539">WSL ahora procesa el archivo /etc/fstab durante el inicio de la instancia [GH 2636].</span><span class="sxs-lookup"><span data-stu-id="12a55-539">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="12a55-540">Esto se hace antes de montar automáticamente las unidades de DrvFs; las unidades que ya se hayan montado mediante fstab no se volverán a montar automáticamente, lo que te permite cambiar el punto de montaje para unidades específicas.</span><span class="sxs-lookup"><span data-stu-id="12a55-540">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="12a55-541">Este comportamiento se puede desactivar mediante wsl.conf.</span><span class="sxs-lookup"><span data-stu-id="12a55-541">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="12a55-542">Los archivos mount, mountinfo y mountstats de /proc convierten correctamente en caracteres especiales, como barras diagonales inversas y espacios [GH 2799]</span><span class="sxs-lookup"><span data-stu-id="12a55-542">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="12a55-543">Los archivos especiales creados con DrvFs, como los vínculos simbólicos de WSL, o fifos y sockets cuando los metadatos están habilitados, ahora se pueden copiar y mover desde Windows.</span><span class="sxs-lookup"><span data-stu-id="12a55-543">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="12a55-544">WSL es más configurable con wsl.conf</span><span class="sxs-lookup"><span data-stu-id="12a55-544">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="12a55-545">Hemos agregado un método para que configures automáticamente cierta funcionalidad en WSL que se aplicará cada vez que inicies el subsistema.</span><span class="sxs-lookup"><span data-stu-id="12a55-545">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="12a55-546">Esto incluye opciones de montaje automático y configuración de red.</span><span class="sxs-lookup"><span data-stu-id="12a55-546">This includes automount options and network configuration.</span></span> <span data-ttu-id="12a55-547">Obtén más información en la publicación de blog en https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="12a55-547">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="af_unix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="12a55-548">AF_UNIX permite conexiones de socket entre procesos de Linux en procesos nativos de WSL y Windows</span><span class="sxs-lookup"><span data-stu-id="12a55-548">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="12a55-549">Las aplicaciones de WSL y Windows ahora pueden comunicarse entre sí a través de sockets de Unix.</span><span class="sxs-lookup"><span data-stu-id="12a55-549">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="12a55-550">Imagina que quieres ejecutar un servicio en Windows y hacer que esté disponible para las aplicaciones de WSL y Windows.</span><span class="sxs-lookup"><span data-stu-id="12a55-550">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="12a55-551">Ahora, eso es posible con los sockets de Unix.</span><span class="sxs-lookup"><span data-stu-id="12a55-551">Now, that’s possible with Unix sockets.</span></span> <span data-ttu-id="12a55-552">Lee más en nuestra publicación de blog en https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="12a55-552">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-553">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-553">WSL</span></span>
* <span data-ttu-id="12a55-554">Compatibilidad de mmap() con MAP_NORESERVE [GH 121, 2784]</span><span class="sxs-lookup"><span data-stu-id="12a55-554">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="12a55-555">Compatibilidad con CLONE_PTRACE y CLONE_UNTRACED [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="12a55-555">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="12a55-556">Controla la señal de terminación no SIGCHLD en el clon [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="12a55-556">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="12a55-557">Código auxiliar /proc/sys/fs/inotify/max_user_instances y /proc/sys/fs/inotify/max_user_watches [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="12a55-557">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="12a55-558">Error al cargar binarios de ELF que contienen encabezados de carga con desplazamientos distintos de cero [GH 1884]</span><span class="sxs-lookup"><span data-stu-id="12a55-558">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="12a55-559">Se eliminan los bytes de página finales al cargar imágenes.</span><span class="sxs-lookup"><span data-stu-id="12a55-559">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="12a55-560">Reduce los casos en los que execve finaliza el proceso de forma silenciosa</span><span class="sxs-lookup"><span data-stu-id="12a55-560">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="12a55-561">Console</span><span class="sxs-lookup"><span data-stu-id="12a55-561">Console</span></span>
* <span data-ttu-id="12a55-562">Sin correcciones.</span><span class="sxs-lookup"><span data-stu-id="12a55-562">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-563">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-563">LTP Results:</span></span>
<span data-ttu-id="12a55-564">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="12a55-564">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="12a55-565">Compilación 17083</span><span class="sxs-lookup"><span data-stu-id="12a55-565">Build 17083</span></span>
<span data-ttu-id="12a55-566">Para obtener información general de Windows sobre la compilación 17083, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="12a55-566">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-567">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-567">WSL</span></span>
* <span data-ttu-id="12a55-568">Se ha corregido la comprobación de errores relacionada con epoll [GH 2798, 2801, 2857]</span><span class="sxs-lookup"><span data-stu-id="12a55-568">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="12a55-569">Se han corregido bloqueos al desactivar ASLR [GH 1185, 2870]</span><span class="sxs-lookup"><span data-stu-id="12a55-569">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="12a55-570">Asegúrate de que las operaciones de mmap aparezcan como atómicas [GH 2732]</span><span class="sxs-lookup"><span data-stu-id="12a55-570">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="12a55-571">Console</span><span class="sxs-lookup"><span data-stu-id="12a55-571">Console</span></span>
* <span data-ttu-id="12a55-572">Sin correcciones.</span><span class="sxs-lookup"><span data-stu-id="12a55-572">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-573">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-573">LTP Results:</span></span>
<span data-ttu-id="12a55-574">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="12a55-574">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="12a55-575">Compilación 17074</span><span class="sxs-lookup"><span data-stu-id="12a55-575">Build 17074</span></span>
<span data-ttu-id="12a55-576">Para obtener información general de Windows sobre la compilación 17074, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span><span class="sxs-lookup"><span data-stu-id="12a55-576">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-577">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-577">WSL</span></span>
* <span data-ttu-id="12a55-578">Se ha corregido el formato de almacenamiento de los metadatos de DrvFs [GH 2777]</span><span class="sxs-lookup"><span data-stu-id="12a55-578">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="12a55-579">**Importante:** Los metadatos de DrvFs creados antes de esta compilación no se mostrarán correctamente o no se mostrarán en absoluto.</span><span class="sxs-lookup"><span data-stu-id="12a55-579">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="12a55-580">Para corregir los archivos afectados, usa chmod y chown para volver a aplicar los metadatos.</span><span class="sxs-lookup"><span data-stu-id="12a55-580">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="12a55-581">Se ha corregido un problema con varias señales y llamadas del sistema reiniciables.</span><span class="sxs-lookup"><span data-stu-id="12a55-581">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="12a55-582">Console</span><span class="sxs-lookup"><span data-stu-id="12a55-582">Console</span></span>
* <span data-ttu-id="12a55-583">Sin correcciones.</span><span class="sxs-lookup"><span data-stu-id="12a55-583">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-584">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-584">LTP Results:</span></span>
<span data-ttu-id="12a55-585">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="12a55-585">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="12a55-586">Compilación 17063</span><span class="sxs-lookup"><span data-stu-id="12a55-586">Build 17063</span></span>
<span data-ttu-id="12a55-587">Para obtener información general de Windows sobre la compilación 17063, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span><span class="sxs-lookup"><span data-stu-id="12a55-587">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="12a55-588">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-588">WSL</span></span>
* <span data-ttu-id="12a55-589">DrvFs admite metadatos de Linux adicionales.</span><span class="sxs-lookup"><span data-stu-id="12a55-589">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="12a55-590">Esto permite establecer el propietario y el modo de los archivos con chmod/chown, y también la creación de archivos especiales, como fifos, sockets de Unix y archivos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12a55-590">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="12a55-591">Esta opción está deshabilitada de forma predeterminada, ya que sigue siendo experimental.</span><span class="sxs-lookup"><span data-stu-id="12a55-591">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="12a55-592">**Nota:**  Se ha corregido un error en el formato de metadatos usado por DrvFs.</span><span class="sxs-lookup"><span data-stu-id="12a55-592">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="12a55-593">Si bien los metadatos funcionan en esta compilación para experimentación, las compilaciones futuras no leerán correctamente los metadatos creados por esta compilación.</span><span class="sxs-lookup"><span data-stu-id="12a55-593">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="12a55-594">Es posible que tengas que actualizar manualmente el propietario de los archivos modificados, y se tendrán que volver a crear los dispositivos con un identificador de dispositivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="12a55-594">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="12a55-595">Para habilitar, monta DrvFs con la opción de metadatos (para habilitarlo en un montaje existente, primero debes desmontarlo):</span><span class="sxs-lookup"><span data-stu-id="12a55-595">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="12a55-596">Los permisos de Linux se agregan como metadatos adicionales al archivo; no afectan a los permisos de Windows.</span><span class="sxs-lookup"><span data-stu-id="12a55-596">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="12a55-597">Recuerda que la edición de un archivo mediante un editor de Windows puede quitar los metadatos.</span><span class="sxs-lookup"><span data-stu-id="12a55-597">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="12a55-598">En este caso, el archivo volverá a sus permisos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="12a55-598">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="12a55-599">Se han agregado opciones de montaje a DrvFs para controlar archivos sin metadatos.</span><span class="sxs-lookup"><span data-stu-id="12a55-599">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="12a55-600">uid: el identificador de usuario que se usa para el propietario de todos los archivos.</span><span class="sxs-lookup"><span data-stu-id="12a55-600">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="12a55-601">gid: el identificador de grupo que se usa para el propietario de todos los archivos.</span><span class="sxs-lookup"><span data-stu-id="12a55-601">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="12a55-602">umask: máscara octal de permisos que se van a excluir para todos los archivos y directorios.</span><span class="sxs-lookup"><span data-stu-id="12a55-602">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="12a55-603">fmask: máscara octal de permisos que se van a excluir para todos los archivos normales.</span><span class="sxs-lookup"><span data-stu-id="12a55-603">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="12a55-604">dmask: máscara octal de permisos que se van a excluir para todos los directorios.</span><span class="sxs-lookup"><span data-stu-id="12a55-604">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="12a55-605">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="12a55-605">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="12a55-606">Combina con la opción de metadatos para especificar los permisos predeterminados para los archivos sin metadatos.</span><span class="sxs-lookup"><span data-stu-id="12a55-606">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="12a55-607">Se presentó una nueva variable de entorno, `WSLENV`, para configurar cómo fluyen las variables de entorno entre WSL y Win32.</span><span class="sxs-lookup"><span data-stu-id="12a55-607">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="12a55-608">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="12a55-608">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="12a55-609">`WSLENV` es una lista de variables de entorno delimitadas por signos de dos puntos que se puede incluir al iniciar procesos de WSL desde Win32, o procesos de Win32 desde WSL.</span><span class="sxs-lookup"><span data-stu-id="12a55-609">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="12a55-610">Cada variable puede tener como sufijo una barra diagonal seguida de marcas para especificar cómo se va a traducir.</span><span class="sxs-lookup"><span data-stu-id="12a55-610">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="12a55-611">p: El valor es una ruta de acceso que se debe traducir entre las rutas de acceso de WSL y las rutas de acceso de Win32.</span><span class="sxs-lookup"><span data-stu-id="12a55-611">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="12a55-612">l: El valor es una lista de rutas de acceso.</span><span class="sxs-lookup"><span data-stu-id="12a55-612">l: The value is a list of paths.</span></span> <span data-ttu-id="12a55-613">En WSL, se trata de una lista delimitada por signos de dos puntos.</span><span class="sxs-lookup"><span data-stu-id="12a55-613">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="12a55-614">En Win32, se trata de una lista delimitada por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="12a55-614">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="12a55-615">u: Solo se debe incluir el valor al invocar WSL desde Win32</span><span class="sxs-lookup"><span data-stu-id="12a55-615">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="12a55-616">w: Solo se debe incluir el valor al invocar Win32 desde WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-616">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="12a55-617">Puedes establecer `WSLENV` en. bashrc o en el entorno de Windows personalizado para el usuario.</span><span class="sxs-lookup"><span data-stu-id="12a55-617">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="12a55-618">drvfs monta correctamente las marcas de tiempo de conservación desde tar, cp -p (GH 1939)</span><span class="sxs-lookup"><span data-stu-id="12a55-618">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="12a55-619">Los vínculos simbólicos de drvfs informan el tamaño correcto (GH 2641)</span><span class="sxs-lookup"><span data-stu-id="12a55-619">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="12a55-620">La lectura/escritura funciona para tamaños de E/S muy grandes (GH 2653)</span><span class="sxs-lookup"><span data-stu-id="12a55-620">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="12a55-621">waitpid funciona con identificadores de grupo de procesos (GH 2534)</span><span class="sxs-lookup"><span data-stu-id="12a55-621">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="12a55-622">Rendimiento de mmap significativamente mejorado para regiones de reserva grandes; mejora el rendimiento de ghc (GH 1671)</span><span class="sxs-lookup"><span data-stu-id="12a55-622">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="12a55-623">Compatibilidad de personality con READ_IMPLIES_EXEC; corrige maxima y clisp (GH 1185)</span><span class="sxs-lookup"><span data-stu-id="12a55-623">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="12a55-624">mprotect admite PROT_GROWSDOWN; corrige clisp (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="12a55-624">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="12a55-625">Correcciones de errores de página en modo de sobreconfirmación; corrige sbcl (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="12a55-625">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="12a55-626">clone admite más combinaciones de marcas</span><span class="sxs-lookup"><span data-stu-id="12a55-626">clone supports more flags combinations</span></span>
* <span data-ttu-id="12a55-627">Compatibilidad con select/epoll de archivos de epoll (antes de una no-op).</span><span class="sxs-lookup"><span data-stu-id="12a55-627">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="12a55-628">Notifica a ptrace de llamadas del sistema sin implementar.</span><span class="sxs-lookup"><span data-stu-id="12a55-628">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="12a55-629">Omite las interfaces que no están listas al generar los servidores de nombres resolv.conf [GH 2694]</span><span class="sxs-lookup"><span data-stu-id="12a55-629">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="12a55-630">Enumera las interfaces de red sin dirección física.</span><span class="sxs-lookup"><span data-stu-id="12a55-630">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="12a55-631">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="12a55-631">[GH 2685]</span></span>
* <span data-ttu-id="12a55-632">Mejoras y correcciones de errores adicionales.</span><span class="sxs-lookup"><span data-stu-id="12a55-632">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="12a55-633">Herramientas de Linux disponibles para desarrolladores en Windows</span><span class="sxs-lookup"><span data-stu-id="12a55-633">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="12a55-634">La cadena de herramientas de la línea de comandos de Windows incluye bsdtar (tar) y curl.</span><span class="sxs-lookup"><span data-stu-id="12a55-634">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="12a55-635">Lee [este blog](https://aka.ms/tarcurlwindows) para más información acerca de cómo agregar estas dos nuevas herramientas y ver cómo dan forma a la experiencia de los desarrolladores en Windows.</span><span class="sxs-lookup"><span data-stu-id="12a55-635">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they’re shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="12a55-636">`AF_UNIX` está disponible en el SDK de Windows Insider (17061+).</span><span class="sxs-lookup"><span data-stu-id="12a55-636">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="12a55-637">Lee [este blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) para más información sobre `AF_UNIX` y cómo pueden usarlo los desarrolladores de Windows.</span><span class="sxs-lookup"><span data-stu-id="12a55-637">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="12a55-638">Console</span><span class="sxs-lookup"><span data-stu-id="12a55-638">Console</span></span>
* <span data-ttu-id="12a55-639">Sin correcciones.</span><span class="sxs-lookup"><span data-stu-id="12a55-639">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-640">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-640">LTP Results:</span></span>
<span data-ttu-id="12a55-641">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="12a55-641">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="12a55-642">Compilación 17046</span><span class="sxs-lookup"><span data-stu-id="12a55-642">Build 17046</span></span>

<span data-ttu-id="12a55-643">Para obtener información general de Windows sobre la compilación 17046, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span><span class="sxs-lookup"><span data-stu-id="12a55-643">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="12a55-644">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-644">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="12a55-645">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-645">WSL</span></span>
- <span data-ttu-id="12a55-646">Permite que los procesos se ejecuten sin un terminal activo.</span><span class="sxs-lookup"><span data-stu-id="12a55-646">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="12a55-647">[GH 709, 1007, 1511, 2252, 2391, etc.]</span><span class="sxs-lookup"><span data-stu-id="12a55-647">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="12a55-648">Mejor compatibilidad con CLONE_VFORK y CLONE_VM.</span><span class="sxs-lookup"><span data-stu-id="12a55-648">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="12a55-649">[GH 1878, 2615]</span><span class="sxs-lookup"><span data-stu-id="12a55-649">[GH 1878, 2615]</span></span>
- <span data-ttu-id="12a55-650">Omite los controladores de filtro TDI para las operaciones de red de WSL.</span><span class="sxs-lookup"><span data-stu-id="12a55-650">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="12a55-651">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="12a55-651">[GH 1554]</span></span>
- <span data-ttu-id="12a55-652">DrvFs crea vínculos simbólicos de NT cuando se cumplen determinadas condiciones.</span><span class="sxs-lookup"><span data-stu-id="12a55-652">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="12a55-653">[GH 353, 1475, 2602]</span><span class="sxs-lookup"><span data-stu-id="12a55-653">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="12a55-654">El destino del vínculo debe ser relativo, no debe cruzar ningún punto de montaje ni vínculo simbólico, y debe existir.</span><span class="sxs-lookup"><span data-stu-id="12a55-654">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="12a55-655">El usuario debe tener SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (esto normalmente requiere que inicies wsl.exe con privilegios elevados), a menos que esté activado el modo de desarrollador.</span><span class="sxs-lookup"><span data-stu-id="12a55-655">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="12a55-656">En todas las demás situaciones, DrvFs todavía crea vínculos simbólicos de WSL.</span><span class="sxs-lookup"><span data-stu-id="12a55-656">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="12a55-657">Permite ejecutar instancias de WSL con privilegios elevados y no elevados simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="12a55-657">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="12a55-658">Compatibilidad con /proc/sys/kernel/yama/ptrace_scope</span><span class="sxs-lookup"><span data-stu-id="12a55-658">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="12a55-659">Agrega wslpath para realizar conversiones de rutas de acceso de WSL<->Windows.</span><span class="sxs-lookup"><span data-stu-id="12a55-659">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="12a55-660">[GH 522, 1243, 1834, 2327, etc.]</span><span class="sxs-lookup"><span data-stu-id="12a55-660">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a><span data-ttu-id="12a55-661">Console</span><span class="sxs-lookup"><span data-stu-id="12a55-661">Console</span></span>
- <span data-ttu-id="12a55-662">Sin correcciones.</span><span class="sxs-lookup"><span data-stu-id="12a55-662">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-663">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-663">LTP Results:</span></span>
<span data-ttu-id="12a55-664">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="12a55-664">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="12a55-665">Compilación 17040</span><span class="sxs-lookup"><span data-stu-id="12a55-665">Build 17040</span></span>

<span data-ttu-id="12a55-666">Para obtener información general de Windows sobre la compilación 17040, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span><span class="sxs-lookup"><span data-stu-id="12a55-666">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-667">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-667">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="12a55-668">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-668">WSL</span></span>
- <span data-ttu-id="12a55-669">No hay correcciones desde 17035.</span><span class="sxs-lookup"><span data-stu-id="12a55-669">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="12a55-670">Console</span><span class="sxs-lookup"><span data-stu-id="12a55-670">Console</span></span>
- <span data-ttu-id="12a55-671">No hay correcciones desde 17035.</span><span class="sxs-lookup"><span data-stu-id="12a55-671">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-672">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-672">LTP Results:</span></span>
<span data-ttu-id="12a55-673">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="12a55-673">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="12a55-674">Compilación 17035</span><span class="sxs-lookup"><span data-stu-id="12a55-674">Build 17035</span></span>

<span data-ttu-id="12a55-675">Para obtener información general de Windows sobre la compilación 17035, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span><span class="sxs-lookup"><span data-stu-id="12a55-675">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-676">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-676">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="12a55-677">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-677">WSL</span></span>
- <span data-ttu-id="12a55-678">En ocasiones, el acceso a los archivos de DrvFs puede producir errores con EINVAL.</span><span class="sxs-lookup"><span data-stu-id="12a55-678">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="12a55-679">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="12a55-679">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="12a55-680">Console</span><span class="sxs-lookup"><span data-stu-id="12a55-680">Console</span></span>
- <span data-ttu-id="12a55-681">Algo de pérdida de color al insertar o eliminar líneas en modo VT.</span><span class="sxs-lookup"><span data-stu-id="12a55-681">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-682">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-682">LTP Results:</span></span>
<span data-ttu-id="12a55-683">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="12a55-683">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="12a55-684">Compilación 17025</span><span class="sxs-lookup"><span data-stu-id="12a55-684">Build 17025</span></span>

<span data-ttu-id="12a55-685">Para obtener información general de Windows sobre la compilación 17025, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span><span class="sxs-lookup"><span data-stu-id="12a55-685">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-686">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-686">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="12a55-687">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-687">WSL</span></span>
- <span data-ttu-id="12a55-688">Inicia procesos iniciales en un nuevo grupo de procesos en primer plano [GH 1653, 2510].</span><span class="sxs-lookup"><span data-stu-id="12a55-688">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="12a55-689">Correcciones de entrega de SIGHUP [GH 2496].</span><span class="sxs-lookup"><span data-stu-id="12a55-689">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="12a55-690">Genera un nombre de puente virtual predeterminado si no se proporciona ninguno [GH 2497].</span><span class="sxs-lookup"><span data-stu-id="12a55-690">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="12a55-691">Implementa /proc/sys/kernel/random/boot_id [GH 2518].</span><span class="sxs-lookup"><span data-stu-id="12a55-691">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="12a55-692">Más correcciones de la canalización stdout/stderr de interoperabilidad.</span><span class="sxs-lookup"><span data-stu-id="12a55-692">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="12a55-693">Llamada del sistema syncfs de código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="12a55-693">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="12a55-694">Console</span><span class="sxs-lookup"><span data-stu-id="12a55-694">Console</span></span>
- <span data-ttu-id="12a55-695">Corrección de la traducción de VT de entrada para consolas de terceros [GH 111]</span><span class="sxs-lookup"><span data-stu-id="12a55-695">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-696">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-696">LTP Results:</span></span>
<span data-ttu-id="12a55-697">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="12a55-697">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="12a55-698">Compilación 17017</span><span class="sxs-lookup"><span data-stu-id="12a55-698">Build 17017</span></span>

<span data-ttu-id="12a55-699">Para obtener información general de Windows sobre la compilación 17017, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span><span class="sxs-lookup"><span data-stu-id="12a55-699">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-700">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-700">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="12a55-701">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-701">WSL</span></span>
- <span data-ttu-id="12a55-702">Omite los encabezados de programa ELF vacíos [GH 330].</span><span class="sxs-lookup"><span data-stu-id="12a55-702">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="12a55-703">Permite que LxssManager cree instancias de WSL para usuarios no interactivos (compatibilidad con ssh y tareas programadas) [GH 777, 1602].</span><span class="sxs-lookup"><span data-stu-id="12a55-703">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="12a55-704">Compatibilidad con escenarios de WSL->Win32->WSL ("inicio") [GH 1228].</span><span class="sxs-lookup"><span data-stu-id="12a55-704">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="12a55-705">Compatibilidad limitada para la terminación de las aplicaciones de consola que se invocan a través de la interoperabilidad [GH 1614].</span><span class="sxs-lookup"><span data-stu-id="12a55-705">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="12a55-706">Compatibilidad con las opciones de montaje para devpts [GH 1948].</span><span class="sxs-lookup"><span data-stu-id="12a55-706">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="12a55-707">Inicio de bloqueo secundario de Ptrace [GH 2333].</span><span class="sxs-lookup"><span data-stu-id="12a55-707">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="12a55-708">Faltan algunos eventos de EPOLLET [GH 2462].</span><span class="sxs-lookup"><span data-stu-id="12a55-708">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="12a55-709">Devuelve más datos para PTRACE_GETSIGINFO.</span><span class="sxs-lookup"><span data-stu-id="12a55-709">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="12a55-710">Getdents con lseek proporciona resultados incorrectos.</span><span class="sxs-lookup"><span data-stu-id="12a55-710">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="12a55-711">Corrección de algunos bloqueos de la aplicación de interoperabilidad de Win32, en espera de la entrada en una canalización que no tiene más datos.</span><span class="sxs-lookup"><span data-stu-id="12a55-711">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="12a55-712">Compatibilidad de O_ASYNC con archivos tty/pty.</span><span class="sxs-lookup"><span data-stu-id="12a55-712">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="12a55-713">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-713">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="12a55-714">Console</span><span class="sxs-lookup"><span data-stu-id="12a55-714">Console</span></span>
- <span data-ttu-id="12a55-715">No hay cambios relacionados con la consola en esta versión.</span><span class="sxs-lookup"><span data-stu-id="12a55-715">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-716">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-716">LTP Results:</span></span>
<span data-ttu-id="12a55-717">Pruebas en curso.</span><span class="sxs-lookup"><span data-stu-id="12a55-717">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="12a55-718">Actualización Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="12a55-718">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="12a55-719">Compilación 16288</span><span class="sxs-lookup"><span data-stu-id="12a55-719">Build 16288</span></span>

<span data-ttu-id="12a55-720">Para obtener información general de Windows sobre la compilación 16288, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span><span class="sxs-lookup"><span data-stu-id="12a55-720">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-721">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-721">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="12a55-722">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-722">WSL</span></span>
- <span data-ttu-id="12a55-723">Inicializa y notifica correctamente uid, gid y mode para los descriptores de archivo de socket [GH 2490]</span><span class="sxs-lookup"><span data-stu-id="12a55-723">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="12a55-724">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-724">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="12a55-725">Console</span><span class="sxs-lookup"><span data-stu-id="12a55-725">Console</span></span>
- <span data-ttu-id="12a55-726">No hay cambios relacionados con la consola en esta versión.</span><span class="sxs-lookup"><span data-stu-id="12a55-726">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-727">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-727">LTP Results:</span></span>
<span data-ttu-id="12a55-728">Sin cambios desde 16273</span><span class="sxs-lookup"><span data-stu-id="12a55-728">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="12a55-729">Compilación 16278</span><span class="sxs-lookup"><span data-stu-id="12a55-729">Build 16278</span></span>

<span data-ttu-id="12a55-730">Para obtener información general de Windows sobre la compilación 162738, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span><span class="sxs-lookup"><span data-stu-id="12a55-730">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-731">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-731">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="12a55-732">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-732">WSL</span></span>
- <span data-ttu-id="12a55-733">Anula explícitamente la asignación de las vistas asignadas de secciones basadas en archivos al anular el estado de LX MM [GH 2415]</span><span class="sxs-lookup"><span data-stu-id="12a55-733">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="12a55-734">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-734">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="12a55-735">Console</span><span class="sxs-lookup"><span data-stu-id="12a55-735">Console</span></span>
- <span data-ttu-id="12a55-736">No hay cambios relacionados con la consola en esta versión.</span><span class="sxs-lookup"><span data-stu-id="12a55-736">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-737">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-737">LTP Results:</span></span>
<span data-ttu-id="12a55-738">Sin cambios desde 16273</span><span class="sxs-lookup"><span data-stu-id="12a55-738">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="12a55-739">Compilación 16275</span><span class="sxs-lookup"><span data-stu-id="12a55-739">Build 16275</span></span>

<span data-ttu-id="12a55-740">Para obtener información general de Windows sobre la compilación 162735, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span><span class="sxs-lookup"><span data-stu-id="12a55-740">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-741">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-741">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="12a55-742">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-742">WSL</span></span>
- <span data-ttu-id="12a55-743">No hay cambios relacionados con WSL en esta versión.</span><span class="sxs-lookup"><span data-stu-id="12a55-743">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="12a55-744">Console</span><span class="sxs-lookup"><span data-stu-id="12a55-744">Console</span></span>
- <span data-ttu-id="12a55-745">No hay cambios relacionados con la consola en esta versión.</span><span class="sxs-lookup"><span data-stu-id="12a55-745">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-746">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-746">LTP Results:</span></span>
<span data-ttu-id="12a55-747">Sin cambios desde 16273</span><span class="sxs-lookup"><span data-stu-id="12a55-747">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="12a55-748">Compilación 16273</span><span class="sxs-lookup"><span data-stu-id="12a55-748">Build 16273</span></span>

<span data-ttu-id="12a55-749">Para obtener información general de Windows sobre la compilación 16273, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span><span class="sxs-lookup"><span data-stu-id="12a55-749">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-750">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-750">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="12a55-751">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-751">WSL</span></span>
- <span data-ttu-id="12a55-752">Se ha corregido un problema por el que DrvFs a veces indicaba un tipo de archivo incorrecto para los directorios [GH 2392]</span><span class="sxs-lookup"><span data-stu-id="12a55-752">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="12a55-753">Permite la creación de sockets NETLINK_KOBJECT_UEVENT para desbloquear programas que usan UEVENT [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span><span class="sxs-lookup"><span data-stu-id="12a55-753">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="12a55-754">Agrega compatibilidad para conexión sin bloqueo [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span><span class="sxs-lookup"><span data-stu-id="12a55-754">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="12a55-755">Implementa la marca de llamada del sistema de clon CLONE_FS [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="12a55-755">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="12a55-756">Corrección de problemas relativos a la falta de control de tabulaciones o comillas correctamente en la interoperabilidad de NT [GH 1625, 2164]</span><span class="sxs-lookup"><span data-stu-id="12a55-756">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="12a55-757">Resuelve el error de acceso denegado al intentar volver a iniciar instancias de WSL [GH 651, 2095]</span><span class="sxs-lookup"><span data-stu-id="12a55-757">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="12a55-758">Implementa las operaciones de Futex FUTEX_REQUEUE y FUTEX_CMP_REQUEUE [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="12a55-758">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="12a55-759">Corrección de permisos para varios archivos de SysFs [GH 2214]</span><span class="sxs-lookup"><span data-stu-id="12a55-759">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="12a55-760">Corrección del bloqueo de pila de Haskell durante la instalación [GH 2290]</span><span class="sxs-lookup"><span data-stu-id="12a55-760">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="12a55-761">Implementa las marcas binfmt_misc "C", "O" y "P" [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="12a55-761">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="12a55-762">Agrega /proc/sys/kernel /shmmax /shmmni y /threads-max [GH 1753]</span><span class="sxs-lookup"><span data-stu-id="12a55-762">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="12a55-763">Agrega compatibilidad parcial para la llamada del sistema ioprio_set [GH 498]</span><span class="sxs-lookup"><span data-stu-id="12a55-763">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="12a55-764">Código auxiliar SO_REUSEPORT y agrega compatibilidad para SO_PASSCRED para sockets de netlink [GH 69]</span><span class="sxs-lookup"><span data-stu-id="12a55-764">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="12a55-765">Devuelve distintos códigos de error de RegisterDistribuiton si se está instalando o desinstalando actualmente una distribución.</span><span class="sxs-lookup"><span data-stu-id="12a55-765">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="12a55-766">Permite la anulación del registro de distribuciones de WSL parcialmente instaladas a través de wslconfig.exe</span><span class="sxs-lookup"><span data-stu-id="12a55-766">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="12a55-767">Corrección de bloqueo de prueba de socket de Python desde UDP::msg_peek</span><span class="sxs-lookup"><span data-stu-id="12a55-767">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="12a55-768">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-768">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="12a55-769">Console</span><span class="sxs-lookup"><span data-stu-id="12a55-769">Console</span></span>
- <span data-ttu-id="12a55-770">No hay cambios relacionados con la consola en esta versión.</span><span class="sxs-lookup"><span data-stu-id="12a55-770">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-771">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-771">LTP Results:</span></span>
<span data-ttu-id="12a55-772">Total de pruebas: 1904</span><span class="sxs-lookup"><span data-stu-id="12a55-772">Total Tests: 1904</span></span><br/>
<span data-ttu-id="12a55-773">Total de pruebas omitidas: 209</span><span class="sxs-lookup"><span data-stu-id="12a55-773">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="12a55-774">Total de errores: 229</span><span class="sxs-lookup"><span data-stu-id="12a55-774">Total Failures: 229</span></span><br/>
[<span data-ttu-id="12a55-775">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="12a55-775">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="12a55-776">Compilación 16257</span><span class="sxs-lookup"><span data-stu-id="12a55-776">Build 16257</span></span>

<span data-ttu-id="12a55-777">Para obtener información general de Windows sobre la compilación 16257, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span><span class="sxs-lookup"><span data-stu-id="12a55-777">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-778">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-778">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="12a55-779">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-779">WSL</span></span>
- <span data-ttu-id="12a55-780">Implementa la llamada del sistema prlimit64</span><span class="sxs-lookup"><span data-stu-id="12a55-780">Implement prlimit64 system call</span></span>
- <span data-ttu-id="12a55-781">Agrega compatibilidad con ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="12a55-781">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="12a55-782">Código auxiliar de MSG_MORE para sockets TCP [GH 2351]</span><span class="sxs-lookup"><span data-stu-id="12a55-782">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="12a55-783">Corrección del comportamiento del vector auxiliar de AT_EXECFN no válido [GH 2133]</span><span class="sxs-lookup"><span data-stu-id="12a55-783">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="12a55-784">Corrección del comportamiento de copiar y pegar para consola/tty, y agrega un mejor control de búfer completo [GH 2204, 2131]</span><span class="sxs-lookup"><span data-stu-id="12a55-784">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="12a55-785">Establece AT_SECURE en vector auxiliar para los programas set-user-ID y set-group-ID [GH 2031]</span><span class="sxs-lookup"><span data-stu-id="12a55-785">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="12a55-786">El punto de conexión maestro de psuedoterminal no controla TIOCPGRP [GH 1063]</span><span class="sxs-lookup"><span data-stu-id="12a55-786">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="12a55-787">La corrección de lseek hace rebobinar directorios en LxFs [GH 2310]</span><span class="sxs-lookup"><span data-stu-id="12a55-787">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="12a55-788">/dev/ptmx se bloquea después de un uso pesado [GH 1882]</span><span class="sxs-lookup"><span data-stu-id="12a55-788">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="12a55-789">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-789">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="12a55-790">Console</span><span class="sxs-lookup"><span data-stu-id="12a55-790">Console</span></span>
- <span data-ttu-id="12a55-791">Corrección para líneas horizontales o guiones bajos en todas partes [GH 2168]</span><span class="sxs-lookup"><span data-stu-id="12a55-791">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="12a55-792">Corrección para el orden de procesamiento cambiado hace que NPM sea más difícil de cerrar [GH 2170]</span><span class="sxs-lookup"><span data-stu-id="12a55-792">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="12a55-793">Se ha agregado la nueva combinación de colores: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="12a55-793">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-794">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-794">LTP Results:</span></span>
<span data-ttu-id="12a55-795">Sin cambios desde 16251</span><span class="sxs-lookup"><span data-stu-id="12a55-795">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="12a55-796">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="12a55-796">Syscall Support</span></span>
<span data-ttu-id="12a55-797">A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="12a55-797">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="12a55-798">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="12a55-798">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="12a55-799">Problemas conocidos</span><span class="sxs-lookup"><span data-stu-id="12a55-799">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[<span data-ttu-id="12a55-800">Problema de GitHub 2392: WSL no reconoce carpetas de Windows…</span><span class="sxs-lookup"><span data-stu-id="12a55-800">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="12a55-801">En la compilación 16257, WSL tiene problemas al enumerar archivos o carpetas de Windows a través de `/mnt/c/...`.</span><span class="sxs-lookup"><span data-stu-id="12a55-801">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="12a55-802">Este problema se ha corregido y debe publicarse en la compilación de Insider durante la semana que comienza el 14/8/2017.</span><span class="sxs-lookup"><span data-stu-id="12a55-802">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="12a55-803">Compilación 16251</span><span class="sxs-lookup"><span data-stu-id="12a55-803">Build 16251</span></span>

<span data-ttu-id="12a55-804">Para obtener información general de Windows sobre la compilación 16251, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span><span class="sxs-lookup"><span data-stu-id="12a55-804">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-805">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-805">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="12a55-806">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-806">WSL</span></span>
- <span data-ttu-id="12a55-807">Quita la etiqueta beta del componente opcional de WSL, consulta la [publicación de blog](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) para más información.</span><span class="sxs-lookup"><span data-stu-id="12a55-807">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="12a55-808">Inicializa correctamente el uid y gid del conjunto guardado para los archivos binarios set-user-ID y set-group-ID en ejecución [GH 962, 1415, 2072]</span><span class="sxs-lookup"><span data-stu-id="12a55-808">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="12a55-809">Se ha agregado compatibilidad con ptrace PTRACE_O_TRACEEXIT [GH 555]</span><span class="sxs-lookup"><span data-stu-id="12a55-809">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="12a55-810">Se ha agregado compatibilidad con ptrace PTRACE_GETFPREGS y PTRACE_GETREGSET con NT_FPREGSET [GH 555]</span><span class="sxs-lookup"><span data-stu-id="12a55-810">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="12a55-811">Se ha corregido ptrace para que se detenga en las señales omitidas</span><span class="sxs-lookup"><span data-stu-id="12a55-811">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="12a55-812">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-812">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="12a55-813">Console</span><span class="sxs-lookup"><span data-stu-id="12a55-813">Console</span></span>
- <span data-ttu-id="12a55-814">No hay cambios relacionados con la consola en esta versión.</span><span class="sxs-lookup"><span data-stu-id="12a55-814">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-815">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-815">LTP Results:</span></span>
<span data-ttu-id="12a55-816">Número de pruebas superadas: 768</span><span class="sxs-lookup"><span data-stu-id="12a55-816">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="12a55-817">Número de pruebas no superadas: 244</span><span class="sxs-lookup"><span data-stu-id="12a55-817">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="12a55-818">Número de pruebas omitidas: 96</span><span class="sxs-lookup"><span data-stu-id="12a55-818">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="12a55-819">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="12a55-819">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="12a55-820">Compilación 16241</span><span class="sxs-lookup"><span data-stu-id="12a55-820">Build 16241</span></span>

<span data-ttu-id="12a55-821">Para obtener información general de Windows sobre la compilación 16241, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span><span class="sxs-lookup"><span data-stu-id="12a55-821">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-822">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-822">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="12a55-823">WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-823">WSL</span></span>
- <span data-ttu-id="12a55-824">No hay cambios relacionados con WSL en esta versión.</span><span class="sxs-lookup"><span data-stu-id="12a55-824">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="12a55-825">Console</span><span class="sxs-lookup"><span data-stu-id="12a55-825">Console</span></span>
- <span data-ttu-id="12a55-826">Corrección para la generación de un carácter equivocado para DEC de líneas cruzadas, que se notificó originalmente [aquí](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span><span class="sxs-lookup"><span data-stu-id="12a55-826">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="12a55-827">Corrección para cuando no se muestre texto de salida en la página de códigos 65001 (utf8)</span><span class="sxs-lookup"><span data-stu-id="12a55-827">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="12a55-828">No transfieras los cambios hechos en los valores RGB de un color a otras partes de la paleta en el cambio de selección.</span><span class="sxs-lookup"><span data-stu-id="12a55-828">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="12a55-829">Esto hará que la hoja de propiedades de la consola sea mucho más fácil de usar.</span><span class="sxs-lookup"><span data-stu-id="12a55-829">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="12a55-830">Ctrl+S no parece funcionar correctamente</span><span class="sxs-lookup"><span data-stu-id="12a55-830">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="12a55-831">Un-Bold/-Dim totalmente ausentes de los códigos de escape de ANSI [GH 2174]</span><span class="sxs-lookup"><span data-stu-id="12a55-831">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="12a55-832">La consola no admite correctamente los temas de color VIM [GH 1706]</span><span class="sxs-lookup"><span data-stu-id="12a55-832">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="12a55-833">No se pueden pegar caracteres determinados [GH 2149]</span><span class="sxs-lookup"><span data-stu-id="12a55-833">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="12a55-834">El cambio de tamaño de reflujo interactúa de forma extraña con el cambio de tamaño de una ventana de Bash cuando el contenido está en la línea de comandos/edición [GH ConEmu 1123]</span><span class="sxs-lookup"><span data-stu-id="12a55-834">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="12a55-835">Ctrl-L deja la pantalla desfasada [GH 1978]</span><span class="sxs-lookup"><span data-stu-id="12a55-835">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="12a55-836">Error de representación de consola al mostrar VT en HDPI [GH 1907]</span><span class="sxs-lookup"><span data-stu-id="12a55-836">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="12a55-837">Los caracteres Japansese parecen extraños con el carácter Unicode U+30FB [GH 2146]</span><span class="sxs-lookup"><span data-stu-id="12a55-837">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="12a55-838">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-838">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="12a55-839">Compilación 16237</span><span class="sxs-lookup"><span data-stu-id="12a55-839">Build 16237</span></span>

<span data-ttu-id="12a55-840">Para obtener información general de Windows sobre la compilación 16237, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span><span class="sxs-lookup"><span data-stu-id="12a55-840">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-841">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-841">Fixed</span></span>
- <span data-ttu-id="12a55-842">Usa atributos predeterminados para archivos sin EA en lxfs (root, root, 0000)</span><span class="sxs-lookup"><span data-stu-id="12a55-842">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="12a55-843">Se ha agregado compatibilidad para distribuciones que usan atributos extendidos</span><span class="sxs-lookup"><span data-stu-id="12a55-843">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="12a55-844">Corrección del relleno de las entradas devueltas por getdents y getdents64</span><span class="sxs-lookup"><span data-stu-id="12a55-844">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="12a55-845">Corrección de la comprobación de permisos para la llamada del sistema shmctl SHM_STAT [GH 2068]</span><span class="sxs-lookup"><span data-stu-id="12a55-845">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="12a55-846">Se ha corregido el estado inicial incorrecto de epoll para ttys [GH 2231]</span><span class="sxs-lookup"><span data-stu-id="12a55-846">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="12a55-847">Corrección de readdir de DrvFs que no devuelve todas las entradas [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="12a55-847">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="12a55-848">Corrección de readdir de LxFs cuando los archivos están desvinculados [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="12a55-848">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="12a55-849">Permite que los archivos drvfs no vinculados se vuelvan a abrir a través de procfs</span><span class="sxs-lookup"><span data-stu-id="12a55-849">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="12a55-850">Se ha agregado la invalidación de la clave del Registro global para deshabilitar las características de WSL (interoperabilidad/montaje de unidades)</span><span class="sxs-lookup"><span data-stu-id="12a55-850">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="12a55-851">Corrección del recuento incorrecto de bloques en "stat" para DrvFs (y LxFs) [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="12a55-851">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="12a55-852">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-852">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="12a55-853">Compilación 16232</span><span class="sxs-lookup"><span data-stu-id="12a55-853">Build 16232</span></span>

<span data-ttu-id="12a55-854">Para obtener información general de Windows sobre la compilación 16232, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span><span class="sxs-lookup"><span data-stu-id="12a55-854">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-855">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-855">Fixed</span></span>
- <span data-ttu-id="12a55-856">No hay cambios relacionados con WSL en esta versión.</span><span class="sxs-lookup"><span data-stu-id="12a55-856">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="12a55-857">Compilación 16226</span><span class="sxs-lookup"><span data-stu-id="12a55-857">Build 16226</span></span>

<span data-ttu-id="12a55-858">Para obtener información general de Windows sobre la compilación 16226, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span><span class="sxs-lookup"><span data-stu-id="12a55-858">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-859">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-859">Fixed</span></span>
- <span data-ttu-id="12a55-860">Compatibilidad con llamadas del sistema relacionadas con xattr (getxattr, setxattr, listxattr, removexattr).</span><span class="sxs-lookup"><span data-stu-id="12a55-860">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="12a55-861">Compatibilidad con security.capablity xattr.</span><span class="sxs-lookup"><span data-stu-id="12a55-861">security.capablity xattr support.</span></span>
- <span data-ttu-id="12a55-862">Compatibilidad mejorada con determinados sistemas de archivos y filtros, incluidos los servidores SMB que no son de MS.</span><span class="sxs-lookup"><span data-stu-id="12a55-862">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="12a55-863">[GH 1952]</span><span class="sxs-lookup"><span data-stu-id="12a55-863">[GH #1952]</span></span>
- <span data-ttu-id="12a55-864">Compatibilidad mejorada para los marcadores de posición de OneDrive, los marcadores de posición de GVFS y los archivos comprimidos del sistema operativo compacto.</span><span class="sxs-lookup"><span data-stu-id="12a55-864">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="12a55-865">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-865">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="12a55-866">Compilación 16215</span><span class="sxs-lookup"><span data-stu-id="12a55-866">Build 16215</span></span>

<span data-ttu-id="12a55-867">Para obtener información general de Windows sobre la compilación 16215, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span><span class="sxs-lookup"><span data-stu-id="12a55-867">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-868">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-868">Fixed</span></span>
- <span data-ttu-id="12a55-869">WSL ya no requiere el modo de desarrollador.</span><span class="sxs-lookup"><span data-stu-id="12a55-869">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="12a55-870">Compatibilidad con uniones de directorios en drvfs.</span><span class="sxs-lookup"><span data-stu-id="12a55-870">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="12a55-871">Controla la desinstalación de paquetes appx de distribución de WSL.</span><span class="sxs-lookup"><span data-stu-id="12a55-871">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="12a55-872">Actualiza procfs para mostrar las asignaciones privadas y compartidas.</span><span class="sxs-lookup"><span data-stu-id="12a55-872">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="12a55-873">Agrega la capacidad de wslconfig.exe de limpiar las distribuciones que están parcialmente instaladas o desinstaladas.</span><span class="sxs-lookup"><span data-stu-id="12a55-873">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="12a55-874">Se ha agregado compatibilidad para IP_MTU_DISCOVER para sockets TCP.</span><span class="sxs-lookup"><span data-stu-id="12a55-874">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="12a55-875">[GH 1639, 2115, 2205]</span><span class="sxs-lookup"><span data-stu-id="12a55-875">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="12a55-876">Inferencia de la familia de protocolos para rutas a AF_INADDR.</span><span class="sxs-lookup"><span data-stu-id="12a55-876">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="12a55-877">Mejoras en los dispositivos serie [GH 1929].</span><span class="sxs-lookup"><span data-stu-id="12a55-877">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="12a55-878">Compilación 16199</span><span class="sxs-lookup"><span data-stu-id="12a55-878">Build 16199</span></span>

<span data-ttu-id="12a55-879">Para obtener información general de Windows sobre la compilación 16199, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span><span class="sxs-lookup"><span data-stu-id="12a55-879">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-880">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-880">Fixed</span></span>
- <span data-ttu-id="12a55-881">No hay cambios relacionados con WSL en estas versiones.</span><span class="sxs-lookup"><span data-stu-id="12a55-881">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="12a55-882">Compilación 16193</span><span class="sxs-lookup"><span data-stu-id="12a55-882">Build 16193</span></span>

<span data-ttu-id="12a55-883">Para obtener información general de Windows sobre la compilación 16193, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span><span class="sxs-lookup"><span data-stu-id="12a55-883">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-884">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-884">Fixed</span></span>
- <span data-ttu-id="12a55-885">Condición de carrera entre el envío de SIGCONT y un grupo de subprocesos de terminación [GH 1973]</span><span class="sxs-lookup"><span data-stu-id="12a55-885">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="12a55-886">Cambia dispositivos tty y pty para notificar FILE_DEVICE_NAMED_PIPE en lugar de FILE_DEVICE_CONSOLE [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="12a55-886">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="12a55-887">Corrección de SSH para IP_OPTIONS</span><span class="sxs-lookup"><span data-stu-id="12a55-887">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="12a55-888">Se ha cambiado el montaje de DrvFs al demonio de inicialización [GH 1862, 1968, 1767, 1933]</span><span class="sxs-lookup"><span data-stu-id="12a55-888">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="12a55-889">Se ha agregado compatibilidad en DrvFs para los siguientes vínculos simbólicos de NT.</span><span class="sxs-lookup"><span data-stu-id="12a55-889">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="12a55-890">Compilación 16184</span><span class="sxs-lookup"><span data-stu-id="12a55-890">Build 16184</span></span>

<span data-ttu-id="12a55-891">Para obtener información general de Windows sobre la compilación 16184, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span><span class="sxs-lookup"><span data-stu-id="12a55-891">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-892">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-892">Fixed</span></span>
- <span data-ttu-id="12a55-893">Se ha quitado la tarea de mantenimiento de paquetes APT (lxrun.exe /update)</span><span class="sxs-lookup"><span data-stu-id="12a55-893">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="12a55-894">Se ha corregido la salida que no se muestra en los procesos de Windows en node.js [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="12a55-894">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="12a55-895">Relaja los requisitos de alineación en lxcore [GH 1794]</span><span class="sxs-lookup"><span data-stu-id="12a55-895">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="12a55-896">Se ha corregido el control de la marca AT_EMPTY_PATH en un número de llamadas del sistema.</span><span class="sxs-lookup"><span data-stu-id="12a55-896">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="12a55-897">Se ha corregido el problema por el que la eliminación de archivos DrvFs con identificadores abiertos hace que el archivo muestre un comportamiento indefinido [GH 544, 966, 1357, 1535, 1615]</span><span class="sxs-lookup"><span data-stu-id="12a55-897">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="12a55-898">/etc/hosts heredará ahora entradas del archivo de hosts de Windows (%windir%\system32\drivers\etc\hosts) [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="12a55-898">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="12a55-899">Compilación 16179</span><span class="sxs-lookup"><span data-stu-id="12a55-899">Build 16179</span></span>

<span data-ttu-id="12a55-900">Para obtener información general de Windows sobre la compilación 16179, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span><span class="sxs-lookup"><span data-stu-id="12a55-900">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-901">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-901">Fixed</span></span>
- <span data-ttu-id="12a55-902">Sin cambios en WSL esta semana.</span><span class="sxs-lookup"><span data-stu-id="12a55-902">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="12a55-903">Compilación 16176</span><span class="sxs-lookup"><span data-stu-id="12a55-903">Build 16176</span></span>

<span data-ttu-id="12a55-904">Para obtener información general de Windows sobre la compilación 16176, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span><span class="sxs-lookup"><span data-stu-id="12a55-904">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-905">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-905">Fixed</span></span>

- [<span data-ttu-id="12a55-906">Se ha habilitado la compatibilidad serie</span><span class="sxs-lookup"><span data-stu-id="12a55-906">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="12a55-907">Se ha agregado la opción de socket de IP IP_OPTIONS [GH 1116]</span><span class="sxs-lookup"><span data-stu-id="12a55-907">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="12a55-908">Se ha implementado la función pwritev (al cargar el archivo en nginx/PHP-FPM) [GH 1506]</span><span class="sxs-lookup"><span data-stu-id="12a55-908">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="12a55-909">Se han agregado opciones de socket IP IP_MULTICAST_IF e IPV6_MULTICAST_IF [GH 990]</span><span class="sxs-lookup"><span data-stu-id="12a55-909">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="12a55-910">Compatibilidad con la opción de socket IP_MULTICAST_LOOP e IPV6_MULTICAST_LOOP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="12a55-910">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="12a55-911">Se ha agregado la opción de socket IP(V6)_MTU para el nodo de aplicaciones, traceroute, dig, nslookup, host</span><span class="sxs-lookup"><span data-stu-id="12a55-911">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="12a55-912">Se ha agregado la opción de socket de IP IPV6_UNICAST_HOPS</span><span class="sxs-lookup"><span data-stu-id="12a55-912">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="12a55-913">Mejoras del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="12a55-913">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="12a55-914">Permite el montaje de rutas UNC</span><span class="sxs-lookup"><span data-stu-id="12a55-914">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="12a55-915">Habilita la compatibilidad con CDFS en drvfs</span><span class="sxs-lookup"><span data-stu-id="12a55-915">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="12a55-916">Controla correctamente los permisos para los sistemas de archivos de red en drvfs</span><span class="sxs-lookup"><span data-stu-id="12a55-916">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="12a55-917">Agrega compatibilidad para unidades remotas a drvfs</span><span class="sxs-lookup"><span data-stu-id="12a55-917">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="12a55-918">Habilita la compatibilidad con CDFS en drvfs</span><span class="sxs-lookup"><span data-stu-id="12a55-918">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="12a55-919">Mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-919">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-920">Resultados de LTP</span><span class="sxs-lookup"><span data-stu-id="12a55-920">LTP Results</span></span>
<span data-ttu-id="12a55-921">Sin cambios desde 15042</span><span class="sxs-lookup"><span data-stu-id="12a55-921">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="12a55-922">Compilación 16170</span><span class="sxs-lookup"><span data-stu-id="12a55-922">Build 16170</span></span>

<span data-ttu-id="12a55-923">Para obtener información general de Windows sobre la compilación 16170, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span><span class="sxs-lookup"><span data-stu-id="12a55-923">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="12a55-924">Hemos lanzado una nueva [publicación de blog](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) en la que se describen nuestros esfuerzos para probar WSL.</span><span class="sxs-lookup"><span data-stu-id="12a55-924">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="12a55-925">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-925">Fixed</span></span>

- <span data-ttu-id="12a55-926">Compatibilidad para la opción de socket IP_ADD_MEMBERSHIP y IPV6_ADD_MEMBERSHIP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="12a55-926">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="12a55-927">Agrega compatibilidad para PTRACE_OLDSETOPTIONS.</span><span class="sxs-lookup"><span data-stu-id="12a55-927">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="12a55-928">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="12a55-928">[GH 1692]</span></span>
- <span data-ttu-id="12a55-929">Mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-929">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-930">Resultados de LTP</span><span class="sxs-lookup"><span data-stu-id="12a55-930">LTP Results</span></span>
<span data-ttu-id="12a55-931">Sin cambios desde 15042</span><span class="sxs-lookup"><span data-stu-id="12a55-931">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="12a55-932">Compilación 15046 a Windows 10 Creators Update</span><span class="sxs-lookup"><span data-stu-id="12a55-932">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="12a55-933">No hay más correcciones o características de WSL planeadas para su inclusión en Windows 10 Creators Update.</span><span class="sxs-lookup"><span data-stu-id="12a55-933">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="12a55-934">Las notas de la versión de WSL se reanudarán en las próximas semanas para las adiciones destinadas a la siguiente actualización principal de Windows.</span><span class="sxs-lookup"><span data-stu-id="12a55-934">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="12a55-935">Para obtener información general de Windows sobre la compilación 15046 y futuras publicaciones de Insider, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span><span class="sxs-lookup"><span data-stu-id="12a55-935">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="12a55-936">Compilación 15042</span><span class="sxs-lookup"><span data-stu-id="12a55-936">Build 15042</span></span>

<span data-ttu-id="12a55-937">Para obtener información general de Windows sobre la compilación 15042, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span><span class="sxs-lookup"><span data-stu-id="12a55-937">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-938">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-938">Fixed</span></span>

- <span data-ttu-id="12a55-939">Corrección para un interbloqueo al quitar una ruta de acceso que termina en ".."</span><span class="sxs-lookup"><span data-stu-id="12a55-939">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="12a55-940">Se ha corregido un problema por el que FIONBIO no devuelve 0 en caso correcto [GH 1683]</span><span class="sxs-lookup"><span data-stu-id="12a55-940">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="12a55-941">Se ha corregido un problema con lecturas de longitud cero de sockets de datagramas de inet</span><span class="sxs-lookup"><span data-stu-id="12a55-941">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="12a55-942">Corrección del posible interbloqueo debido a la condición de carrera en la búsqueda de inode de drvfs [GH 1675]</span><span class="sxs-lookup"><span data-stu-id="12a55-942">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="12a55-943">Se ha ampliado la compatibilidad con los datos suplementarios de los sockets de Unix; SCM_CREDENTIALS y SCM_RIGHTS [GH 514, 613, 1326]</span><span class="sxs-lookup"><span data-stu-id="12a55-943">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="12a55-944">Mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-944">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-945">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-945">LTP Results:</span></span>
<span data-ttu-id="12a55-946">Número de pruebas superadas: 737</span><span class="sxs-lookup"><span data-stu-id="12a55-946">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="12a55-947">Número de no superadas (error, omitidas, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="12a55-947">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="12a55-948">Compilación 15031</span><span class="sxs-lookup"><span data-stu-id="12a55-948">Build 15031</span></span>

<span data-ttu-id="12a55-949">Para obtener información general de Windows sobre la compilación 15031, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span><span class="sxs-lookup"><span data-stu-id="12a55-949">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-950">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-950">Fixed</span></span>

- <span data-ttu-id="12a55-951">Se ha corregido un error en el que el time(2) se comportaba incorrectamente de manera esporádica.</span><span class="sxs-lookup"><span data-stu-id="12a55-951">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="12a55-952">Se ha corregido un problema donde las llamadas del sistema de \*SIGPROCMASK podían dañar la máscara de señal.</span><span class="sxs-lookup"><span data-stu-id="12a55-952">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="12a55-953">Ahora, devuelva la longitud completa de la línea de comandos en la notificación de creación del proceso de WSL.</span><span class="sxs-lookup"><span data-stu-id="12a55-953">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="12a55-954">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="12a55-954">[GH 1632]</span></span>
- <span data-ttu-id="12a55-955">WSL ahora informa de la salida del subproceso a través de ptrace para bloqueos de GDB.</span><span class="sxs-lookup"><span data-stu-id="12a55-955">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="12a55-956">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="12a55-956">[GH 1196]</span></span>
- <span data-ttu-id="12a55-957">Se ha corregido un error en el que ptys se bloqueaba después de una gran E/S de tmux</span><span class="sxs-lookup"><span data-stu-id="12a55-957">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="12a55-958">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="12a55-958">[GH 1358]</span></span>
- <span data-ttu-id="12a55-959">Se ha corregido la validación del tiempo de espera en muchas llamadas del sistema (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span><span class="sxs-lookup"><span data-stu-id="12a55-959">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="12a55-960">Se ha agregado compatibilidad con eventfd EFD_SEMAPHORE [GH 452]</span><span class="sxs-lookup"><span data-stu-id="12a55-960">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="12a55-961">Mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-961">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-962">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-962">LTP Results:</span></span>
<span data-ttu-id="12a55-963">Número de pruebas superadas: 737</span><span class="sxs-lookup"><span data-stu-id="12a55-963">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="12a55-964">Número de no superadas (error, omitidas, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="12a55-964">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="12a55-965">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="12a55-965">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="12a55-966">Compilación 15025</span><span class="sxs-lookup"><span data-stu-id="12a55-966">Build 15025</span></span>

<span data-ttu-id="12a55-967">Para obtener información general de Windows sobre la compilación 15025, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span><span class="sxs-lookup"><span data-stu-id="12a55-967">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-968">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-968">Fixed</span></span>

- <span data-ttu-id="12a55-969">Corrección del error que dañó grep 2.27 [GH 1578]</span><span class="sxs-lookup"><span data-stu-id="12a55-969">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="12a55-970">Se ha implementado la marca EFD_SEMAPHORE para la llamada del sistema eventfd2 [GH 452]</span><span class="sxs-lookup"><span data-stu-id="12a55-970">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="12a55-971">Se ha implementado /proc/[pid]/net/ipv6_route [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="12a55-971">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="12a55-972">Compatibilidad de E/S controlada por señal para sockets de secuencia de Unix [GH 393, 68]</span><span class="sxs-lookup"><span data-stu-id="12a55-972">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="12a55-973">Compatibilidad con F_GETPIPE_SZ y F_SETPIPE_SZ [GH 1012]</span><span class="sxs-lookup"><span data-stu-id="12a55-973">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="12a55-974">Implementa la llamada del sistema recvmmsg() [GH 1531]</span><span class="sxs-lookup"><span data-stu-id="12a55-974">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="12a55-975">Se ha corregido un error en el que epoll_wait() no esperaba [GH 1609]</span><span class="sxs-lookup"><span data-stu-id="12a55-975">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="12a55-976">Implementa /proc/version_signature</span><span class="sxs-lookup"><span data-stu-id="12a55-976">Implement /proc/version_signature</span></span>
- <span data-ttu-id="12a55-977">La llamada del sistema Tee ahora devuelve un error si ambos descriptores de archivo hacen referencia a la misma canalización</span><span class="sxs-lookup"><span data-stu-id="12a55-977">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="12a55-978">Se ha implementado el comportamiento correcto de SO_PEERCRED para sockets de Unix</span><span class="sxs-lookup"><span data-stu-id="12a55-978">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="12a55-979">Se ha corregido el control de parámetros no válidos de llamada del sistema tkill</span><span class="sxs-lookup"><span data-stu-id="12a55-979">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="12a55-980">Cambios para aumentar el rendimiento de drvfs</span><span class="sxs-lookup"><span data-stu-id="12a55-980">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="12a55-981">Corrección menor para el bloqueo de E/S de Ruby</span><span class="sxs-lookup"><span data-stu-id="12a55-981">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="12a55-982">Se ha corregido recvmsg() que devuelve EINVAL para la marca MSG_DONTWAIT para sockets inet [GH 1296]</span><span class="sxs-lookup"><span data-stu-id="12a55-982">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="12a55-983">Mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-983">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-984">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-984">LTP Results:</span></span>
<span data-ttu-id="12a55-985">Número de pruebas superadas: 732</span><span class="sxs-lookup"><span data-stu-id="12a55-985">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="12a55-986">Número de no superadas (error, omitidas, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="12a55-986">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="12a55-987">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="12a55-987">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="12a55-988">Compilación 15019</span><span class="sxs-lookup"><span data-stu-id="12a55-988">Build 15019</span></span>

<span data-ttu-id="12a55-989">Para obtener información general de Windows sobre la compilación 15019, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span><span class="sxs-lookup"><span data-stu-id="12a55-989">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-990">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-990">Fixed</span></span>

- <span data-ttu-id="12a55-991">Se ha corregido un error que informaba incorrectamente del uso de CPU en procfs para herramientas como htop (GH 823, 945, 971)</span><span class="sxs-lookup"><span data-stu-id="12a55-991">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="12a55-992">Al llamar a open() con O_TRUNC en un archivo existente inotify ahora genera IN_MODIFY antes de IN_OPEN</span><span class="sxs-lookup"><span data-stu-id="12a55-992">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="12a55-993">Correcciones para el SO_ERROR de sockets de Unix getsockopt para habilitar postgress [GH 61, 1354]</span><span class="sxs-lookup"><span data-stu-id="12a55-993">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="12a55-994">Implementa /proc/sys/net/core/somaxconn para el lenguaje GO</span><span class="sxs-lookup"><span data-stu-id="12a55-994">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="12a55-995">La tarea en segundo plano de actualización del paquete apt-get ahora se ejecuta oculta de la vista</span><span class="sxs-lookup"><span data-stu-id="12a55-995">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="12a55-996">Borra el ámbito de IPv6 localhost (error de Spring-Framework (Java)).</span><span class="sxs-lookup"><span data-stu-id="12a55-996">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="12a55-997">Mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-997">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-998">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-998">LTP Results:</span></span>
<span data-ttu-id="12a55-999">Número de pruebas superadas: 714</span><span class="sxs-lookup"><span data-stu-id="12a55-999">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="12a55-1000">Número de no superadas (error, omitidas, etc.): 249</span><span class="sxs-lookup"><span data-stu-id="12a55-1000">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="12a55-1001">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="12a55-1001">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="12a55-1002">Compilación 15014</span><span class="sxs-lookup"><span data-stu-id="12a55-1002">Build 15014</span></span>

<span data-ttu-id="12a55-1003">Para obtener información general de Windows sobre la compilación 15014, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="12a55-1003">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-1004">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-1004">Fixed</span></span>

- <span data-ttu-id="12a55-1005">Ctrl + C ahora funciona según lo previsto</span><span class="sxs-lookup"><span data-stu-id="12a55-1005">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="12a55-1006">htop y ps auxw ahora muestran el uso de recursos correcto (GH 516)</span><span class="sxs-lookup"><span data-stu-id="12a55-1006">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="12a55-1007">Traducción básica de excepciones de NT a señales.</span><span class="sxs-lookup"><span data-stu-id="12a55-1007">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="12a55-1008">(GH 513)</span><span class="sxs-lookup"><span data-stu-id="12a55-1008">(GH #513)</span></span>
- <span data-ttu-id="12a55-1009">fallocate ahora genera el error ENOSPC cuando se está quedando sin espacio en lugar de EINVAL (GH 1571)</span><span class="sxs-lookup"><span data-stu-id="12a55-1009">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="12a55-1010">Se ha agregado/proc/sys/kernel/sem.</span><span class="sxs-lookup"><span data-stu-id="12a55-1010">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="12a55-1011">Se han implementado las llamadas del sistema semop y semtimedop</span><span class="sxs-lookup"><span data-stu-id="12a55-1011">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="12a55-1012">Se han corregido errores de nslookup con la opción de socket IP_RECVTOS e IPV6_RECVTCLASS (GH 69)</span><span class="sxs-lookup"><span data-stu-id="12a55-1012">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="12a55-1013">Compatibilidad con las opciones de socket IP_RECVTTL e IPV6_RECVHOPLIMIT</span><span class="sxs-lookup"><span data-stu-id="12a55-1013">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="12a55-1014">Mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-1014">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-1015">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-1015">LTP Results:</span></span>
<span data-ttu-id="12a55-1016">Número de pruebas superadas: 709</span><span class="sxs-lookup"><span data-stu-id="12a55-1016">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="12a55-1017">Número de no superadas (error, omitidas, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="12a55-1017">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="12a55-1018">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="12a55-1018">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="12a55-1019">Resumen de llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="12a55-1019">Syscall Summary</span></span>
<span data-ttu-id="12a55-1020">Total de llamadas del sistema: 384</span><span class="sxs-lookup"><span data-stu-id="12a55-1020">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="12a55-1021">Total implementado: 235</span><span class="sxs-lookup"><span data-stu-id="12a55-1021">Total Implemented: 235</span></span> </br>
<span data-ttu-id="12a55-1022">Total de procesos con stub: 22</span><span class="sxs-lookup"><span data-stu-id="12a55-1022">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="12a55-1023">Total no implementado: 127</span><span class="sxs-lookup"><span data-stu-id="12a55-1023">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="12a55-1024">Desglose detallado</span><span class="sxs-lookup"><span data-stu-id="12a55-1024">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="12a55-1025">Compilación 15007</span><span class="sxs-lookup"><span data-stu-id="12a55-1025">Build 15007</span></span>

<span data-ttu-id="12a55-1026">Para obtener información general de Windows sobre la compilación 15007, visita el [blog de Windows]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span><span class="sxs-lookup"><span data-stu-id="12a55-1026">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="12a55-1027">Problema conocido</span><span class="sxs-lookup"><span data-stu-id="12a55-1027">Known Issue</span></span>

- <span data-ttu-id="12a55-1028">Hay un error conocido en el que la consola no reconoce algunas entradas Ctrl + <key>.</span><span class="sxs-lookup"><span data-stu-id="12a55-1028">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="12a55-1029">Esto incluye el comando Ctrl-C, que actuará como una presión normal de "c".</span><span class="sxs-lookup"><span data-stu-id="12a55-1029">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="12a55-1030">Solución: Asigna una tecla alternativa a Ctrl+C.</span><span class="sxs-lookup"><span data-stu-id="12a55-1030">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="12a55-1031">Por ejemplo, para asignar Ctrl+K a Ctrl+C, haz lo siguiente: `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="12a55-1031">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="12a55-1032">Esta asignación es por terminal y tendrá que hacerse *cada* vez que se inicie Bash.</span><span class="sxs-lookup"><span data-stu-id="12a55-1032">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="12a55-1033">Los usuarios pueden explorar la opción para incluirlo en su `.bashrc`</span><span class="sxs-lookup"><span data-stu-id="12a55-1033">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="12a55-1034">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-1034">Fixed</span></span>

- <span data-ttu-id="12a55-1035">Se ha corregido el problema que hacía que la ejecución de WSL consumiera el 100 % de un núcleo de CPU.</span><span class="sxs-lookup"><span data-stu-id="12a55-1035">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="12a55-1036">Ahora se admite la opción de socket IP_PKTINFO, IPV6_RECVPKTINFO.</span><span class="sxs-lookup"><span data-stu-id="12a55-1036">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="12a55-1037">(GH 851, 987)</span><span class="sxs-lookup"><span data-stu-id="12a55-1037">(GH #851, 987)</span></span>
- <span data-ttu-id="12a55-1038">Trunca la dirección física de la interfaz de red a 16 bytes en lxcore (GH 1452, 1414, 1343, 468, 308)</span><span class="sxs-lookup"><span data-stu-id="12a55-1038">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="12a55-1039">Mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-1039">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-1040">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-1040">LTP Results:</span></span>
<span data-ttu-id="12a55-1041">Número de pruebas superadas: 709</span><span class="sxs-lookup"><span data-stu-id="12a55-1041">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="12a55-1042">Número de no superadas (error, omitidas, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="12a55-1042">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="12a55-1043">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="12a55-1043">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="12a55-1044">Compilación 15002</span><span class="sxs-lookup"><span data-stu-id="12a55-1044">Build 15002</span></span>

<span data-ttu-id="12a55-1045">Para obtener información general de Windows sobre la compilación 15002, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span><span class="sxs-lookup"><span data-stu-id="12a55-1045">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="12a55-1046">Problema conocido</span><span class="sxs-lookup"><span data-stu-id="12a55-1046">Known Issue</span></span>

<span data-ttu-id="12a55-1047">Dos problemas conocidos:</span><span class="sxs-lookup"><span data-stu-id="12a55-1047">Two known issues:</span></span>
- <span data-ttu-id="12a55-1048">Hay un error conocido en el que la consola no reconoce algunas entradas Ctrl + <key>.</span><span class="sxs-lookup"><span data-stu-id="12a55-1048">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="12a55-1049">Esto incluye el comando Ctrl-C, que actuará como una presión normal de "c".</span><span class="sxs-lookup"><span data-stu-id="12a55-1049">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="12a55-1050">Solución: Asigna una tecla alternativa a Ctrl+C.</span><span class="sxs-lookup"><span data-stu-id="12a55-1050">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="12a55-1051">Por ejemplo, para asignar Ctrl+K a Ctrl+C, haz lo siguiente: `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="12a55-1051">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="12a55-1052">Esta asignación es por terminal y tendrá que hacerse *cada* vez que se inicie Bash.</span><span class="sxs-lookup"><span data-stu-id="12a55-1052">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="12a55-1053">Los usuarios pueden explorar la opción para incluirlo en su `.bashrc`</span><span class="sxs-lookup"><span data-stu-id="12a55-1053">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="12a55-1054">Mientras se ejecuta WSL, un subproceso del sistema consumirá el 100 % de un núcleo de CPU.</span><span class="sxs-lookup"><span data-stu-id="12a55-1054">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="12a55-1055">La raíz de esto se ha solucionado y corregido internamente.</span><span class="sxs-lookup"><span data-stu-id="12a55-1055">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="12a55-1056">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-1056">Fixed</span></span>

- <span data-ttu-id="12a55-1057">Todas las sesiones de Bash ahora deben crearse en el mismo nivel de permiso.</span><span class="sxs-lookup"><span data-stu-id="12a55-1057">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="12a55-1058">Se bloquearán los intentos de iniciar una sesión en un nivel diferente.</span><span class="sxs-lookup"><span data-stu-id="12a55-1058">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="12a55-1059">Esto significa que las consolas de administrador y que no son de administración no se pueden ejecutarse al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="12a55-1059">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="12a55-1060">(GH 626)</span><span class="sxs-lookup"><span data-stu-id="12a55-1060">(GH #626)</span></span>
<br/>
- <span data-ttu-id="12a55-1061">Se han implementado los siguientes mensajes NETLINK_ROUTE (requiere el administrador de Windows)</span><span class="sxs-lookup"><span data-stu-id="12a55-1061">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="12a55-1062">RTM_NEWADDR (admite `ip addr add`)</span><span class="sxs-lookup"><span data-stu-id="12a55-1062">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="12a55-1063">RTM_NEWROUTE (admite `ip route add`)</span><span class="sxs-lookup"><span data-stu-id="12a55-1063">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="12a55-1064">RTM_DELADDR (admite `ip addr del`)</span><span class="sxs-lookup"><span data-stu-id="12a55-1064">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="12a55-1065">RTM_DELROUTE (admite `ip route del`)</span><span class="sxs-lookup"><span data-stu-id="12a55-1065">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="12a55-1066">La comprobación de tareas programadas para actualizar los paquetes ya no se ejecutará en una conexión de uso medido (GH 1371)</span><span class="sxs-lookup"><span data-stu-id="12a55-1066">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="12a55-1067">Se ha corregido un error en el que la canalización se bloquea, es decir, bash -c "ls -alR /" | bash -c "cat" (GH 1214)</span><span class="sxs-lookup"><span data-stu-id="12a55-1067">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="12a55-1068">Se ha implementado la opción de socket TCP_KEEPCNT (GH 843)</span><span class="sxs-lookup"><span data-stu-id="12a55-1068">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="12a55-1069">Se ha implementado la opción de socket IP_MTU_DISCOVER INET (GH 720, 717, 170, 69)</span><span class="sxs-lookup"><span data-stu-id="12a55-1069">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="12a55-1070">Se ha quitado la funcionalidad heredada para ejecutar archivos binarios de NT desde init con búsqueda de rutas de NT.</span><span class="sxs-lookup"><span data-stu-id="12a55-1070">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="12a55-1071">(GH 1325)</span><span class="sxs-lookup"><span data-stu-id="12a55-1071">(GH #1325)</span></span>
- <span data-ttu-id="12a55-1072">Corrección del modo de /dev/kmsg para permitir el acceso de lectura de grupo/otro (0644) (GH 1321)</span><span class="sxs-lookup"><span data-stu-id="12a55-1072">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="12a55-1073">Se ha implementado /proc/sys/kernel/random/boot_id [GH 1092].</span><span class="sxs-lookup"><span data-stu-id="12a55-1073">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="12a55-1074">Se ha corregido el error en el que la hora de inicio del proceso se mostraba como el año 2432 (GH 974)</span><span class="sxs-lookup"><span data-stu-id="12a55-1074">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="12a55-1075">Se ha cambiado la variable de entorno TERM predeterminada a xterm-256color (GH 1446)</span><span class="sxs-lookup"><span data-stu-id="12a55-1075">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="12a55-1076">Se ha modificado la forma en que se calcula la confirmación del proceso durante la bifurcación del proceso.</span><span class="sxs-lookup"><span data-stu-id="12a55-1076">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="12a55-1077">(GH 1286)</span><span class="sxs-lookup"><span data-stu-id="12a55-1077">(GH #1286)</span></span>
- <span data-ttu-id="12a55-1078">Se ha implementado /proc/sys/vm/overcommit_memory.</span><span class="sxs-lookup"><span data-stu-id="12a55-1078">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="12a55-1079">(GH 1286)</span><span class="sxs-lookup"><span data-stu-id="12a55-1079">(GH #1286)</span></span>
- <span data-ttu-id="12a55-1080">Se ha implementado el archivo /proc/net/route (GH 69)</span><span class="sxs-lookup"><span data-stu-id="12a55-1080">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="12a55-1081">Se ha corregido el error en el que el nombre de acceso directo se localizaba incorrectamente (GH 696)</span><span class="sxs-lookup"><span data-stu-id="12a55-1081">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="12a55-1082">Se ha corregido la lógica de análisis de elf que valida incorrectamente los encabezados de programa debe ser menor que (o igual a) PATH_MAX.</span><span class="sxs-lookup"><span data-stu-id="12a55-1082">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="12a55-1083">(GH 1048)</span><span class="sxs-lookup"><span data-stu-id="12a55-1083">(GH #1048)</span></span>
- <span data-ttu-id="12a55-1084">Se ha implementado la devolución de llamada de statfs para procfs, sysfs, cgroupfs y binfmtfs (GH 1378)</span><span class="sxs-lookup"><span data-stu-id="12a55-1084">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="12a55-1085">Se han corregido ventanas de AptPackageIndexUpdate que no se cierran (GH 1184, también se describe en GH 1193).</span><span class="sxs-lookup"><span data-stu-id="12a55-1085">Fixed AptPackageIndexUpdate windows that won’t close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="12a55-1086">Se ha agregado compatibilidad con la personalidad de ASLR ADDR_NO_RANDOMIZE.</span><span class="sxs-lookup"><span data-stu-id="12a55-1086">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="12a55-1087">(GH 1148, 1128)</span><span class="sxs-lookup"><span data-stu-id="12a55-1087">(GH #1148, 1128)</span></span>
- <span data-ttu-id="12a55-1088">Se han mejorado PTRACE_GETSIGINFO, SIGSEGV para los seguimientos de la pila gdb adecuados durante AV (GH 875)</span><span class="sxs-lookup"><span data-stu-id="12a55-1088">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="12a55-1089">Ya no se produce un error en el análisis de elf para los archivos binarios de patchelf.</span><span class="sxs-lookup"><span data-stu-id="12a55-1089">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="12a55-1090">(GH 471)</span><span class="sxs-lookup"><span data-stu-id="12a55-1090">(GH #471)</span></span>
- <span data-ttu-id="12a55-1091">DNS de VPN propagado a/etc/resolv.conf (GH 416, 1350)</span><span class="sxs-lookup"><span data-stu-id="12a55-1091">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="12a55-1092">Mejoras en el cierre de TCP para la transferencia de datos más confiable.</span><span class="sxs-lookup"><span data-stu-id="12a55-1092">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="12a55-1093">(GH 610, 616, 1025, 1335)</span><span class="sxs-lookup"><span data-stu-id="12a55-1093">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="12a55-1094">Ahora devuelve el código de error correcto cuando se abran demasiados archivos (EMFILE).</span><span class="sxs-lookup"><span data-stu-id="12a55-1094">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="12a55-1095">(GH 1126, 2090)</span><span class="sxs-lookup"><span data-stu-id="12a55-1095">(GH #1126, 2090)</span></span>
- <span data-ttu-id="12a55-1096">El registro de auditoría de Windows ahora informa el nombre de la imagen en la creación del proceso de auditoría.</span><span class="sxs-lookup"><span data-stu-id="12a55-1096">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="12a55-1097">Ahora se producen errores leves al iniciar bash.exe desde una ventana de Bash</span><span class="sxs-lookup"><span data-stu-id="12a55-1097">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="12a55-1098">Se ha agregado un mensaje de error cuando interop no puede acceder a un directorio de trabajo en LxFs (es decir, notepad.exe .bashrc)</span><span class="sxs-lookup"><span data-stu-id="12a55-1098">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="12a55-1099">Se ha corregido un problema en el que la ruta de acceso de Windows se truncaba en WSL</span><span class="sxs-lookup"><span data-stu-id="12a55-1099">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="12a55-1100">Mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-1100">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-1101">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-1101">LTP Results:</span></span>
<span data-ttu-id="12a55-1102">Número de pruebas superadas: 690</span><span class="sxs-lookup"><span data-stu-id="12a55-1102">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="12a55-1103">Número de no superadas (error, omitidas, etc.): 274</span><span class="sxs-lookup"><span data-stu-id="12a55-1103">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="12a55-1104">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="12a55-1104">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="12a55-1105">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="12a55-1105">Syscall Support</span></span>
<span data-ttu-id="12a55-1106">A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="12a55-1106">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="12a55-1107">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="12a55-1107">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="12a55-1108">Compilación 14986</span><span class="sxs-lookup"><span data-stu-id="12a55-1108">Build 14986</span></span>

<span data-ttu-id="12a55-1109">Para obtener información general de Windows sobre la compilación 14986, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span><span class="sxs-lookup"><span data-stu-id="12a55-1109">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-1110">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-1110">Fixed</span></span>

- <span data-ttu-id="12a55-1111">Se han corregido comprobaciones de error con IOCTL de NetLink y Pty</span><span class="sxs-lookup"><span data-stu-id="12a55-1111">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="12a55-1112">La versión del kernel ahora informa 4.4.0-43 por coherencia con Xenial</span><span class="sxs-lookup"><span data-stu-id="12a55-1112">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="12a55-1113">Bash.exe ahora se inicia cuando la entrada se dirige a "nul" (GH 1259)</span><span class="sxs-lookup"><span data-stu-id="12a55-1113">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="12a55-1114">Los identificadores de subproceso ahora se han declarado correctamente en procfs (GH 967)</span><span class="sxs-lookup"><span data-stu-id="12a55-1114">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="12a55-1115">Las marcas IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR ahora se admiten en inotify_add_watch() (GH 1280)</span><span class="sxs-lookup"><span data-stu-id="12a55-1115">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="12a55-1116">Implementa timer_create y llamadas del sistema relacionadas.</span><span class="sxs-lookup"><span data-stu-id="12a55-1116">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="12a55-1117">Esto habilita la compatibilidad con GHC (GH 307)</span><span class="sxs-lookup"><span data-stu-id="12a55-1117">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="12a55-1118">Se ha corregido un problema en el que ping devolvía una hora de 0,000 ms (GH 1296)</span><span class="sxs-lookup"><span data-stu-id="12a55-1118">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="12a55-1119">Devuelve el código de error correcto cuando se abran demasiados archivos.</span><span class="sxs-lookup"><span data-stu-id="12a55-1119">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="12a55-1120">Se ha corregido un problema en WSL donde la solicitud de NetLink de datos de la interfaz de red generaba un error con EINVAL si la dirección de hardware de la interfaz es de 32 bytes (por ejemplo, la interfaz Teredo)</span><span class="sxs-lookup"><span data-stu-id="12a55-1120">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="12a55-1121">Ten en cuenta que la utilidad "ip" de Linux contiene un error en el que se bloqueará si WSL informa de una dirección de hardware de 32 bytes.</span><span class="sxs-lookup"><span data-stu-id="12a55-1121">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="12a55-1122">Se trata de un error en "ip", no en WSL.</span><span class="sxs-lookup"><span data-stu-id="12a55-1122">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="12a55-1123">La utilidad "ip" codifica de forma rígida la longitud del búfer de cadena usado para imprimir la dirección de hardware, y el búfer es demasiado pequeño para imprimir una dirección de hardware de 32 bytes.</span><span class="sxs-lookup"><span data-stu-id="12a55-1123">The “ip” utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="12a55-1124">Mejoras y correcciones adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-1124">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-1125">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-1125">LTP Results:</span></span>
<span data-ttu-id="12a55-1126">Número de pruebas superadas: 669</span><span class="sxs-lookup"><span data-stu-id="12a55-1126">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="12a55-1127">Número de no superadas (error, omitidas, etc.): 258</span><span class="sxs-lookup"><span data-stu-id="12a55-1127">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="12a55-1128">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="12a55-1128">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="12a55-1129">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="12a55-1129">Syscall Support</span></span>
<span data-ttu-id="12a55-1130">A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="12a55-1130">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="12a55-1131">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="12a55-1131">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="12a55-1132">Compilación 14971</span><span class="sxs-lookup"><span data-stu-id="12a55-1132">Build 14971</span></span>

<span data-ttu-id="12a55-1133">Para obtener información general de Windows sobre la compilación 14971, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="12a55-1133">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-1134">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-1134">Fixed</span></span>

 - <span data-ttu-id="12a55-1135">Debido a circunstancias más allá de nuestro control, no hay ninguna actualización en esta compilación para el subsistema de Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="12a55-1135">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="12a55-1136">Las actualizaciones programadas regularmente se reanudarán en la próxima versión.</span><span class="sxs-lookup"><span data-stu-id="12a55-1136">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-1137">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-1137">LTP Results:</span></span>
<span data-ttu-id="12a55-1138">Sin cambios desde 14965</span><span class="sxs-lookup"><span data-stu-id="12a55-1138">Unchanged from 14965</span></span> </br>
<span data-ttu-id="12a55-1139">Número de pruebas superadas: 664</span><span class="sxs-lookup"><span data-stu-id="12a55-1139">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="12a55-1140">Número de no superadas (error, omitidas, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="12a55-1140">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="12a55-1141">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="12a55-1141">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="12a55-1142">Compilación 14965</span><span class="sxs-lookup"><span data-stu-id="12a55-1142">Build 14965</span></span>

<span data-ttu-id="12a55-1143">Para obtener información general de Windows sobre la compilación 14965, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="12a55-1143">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-1144">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-1144">Fixed</span></span>

- <span data-ttu-id="12a55-1145">Compatibilidad con RTM_GETLINK y RTM_GETADDR del protocolo NETLINK_ROUTE de sockets de Netlink (GH 468)</span><span class="sxs-lookup"><span data-stu-id="12a55-1145">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="12a55-1146">Habilita los comandos ifconfig e ip para la enumeración de red</span><span class="sxs-lookup"><span data-stu-id="12a55-1146">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="12a55-1147">Puede encontrar más información en la [publicación de blog sobre redes WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span><span class="sxs-lookup"><span data-stu-id="12a55-1147">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="12a55-1148">/sbin está ahora en la ruta de acceso del usuario de manera predeterminada</span><span class="sxs-lookup"><span data-stu-id="12a55-1148">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="12a55-1149">La ruta de acceso de usuario de NT ahora se anexa a la ruta de acceso de WSL de manera predeterminada (es decir, ahora puedes escribir notepad.exe sin agregar System32 a la ruta de acceso de Linux)</span><span class="sxs-lookup"><span data-stu-id="12a55-1149">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="12a55-1150">Se ha agregado compatibilidad para /proc/sys/kernel/cap_last_cap</span><span class="sxs-lookup"><span data-stu-id="12a55-1150">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="12a55-1151">Los archivos binarios de NT ahora se pueden iniciar desde WSL cuando el directorio de trabajo actual contiene caracteres que no son ANSI (GH 1254)</span><span class="sxs-lookup"><span data-stu-id="12a55-1151">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="12a55-1152">Permite el apagado en el socket de flujo Unix desconectado.</span><span class="sxs-lookup"><span data-stu-id="12a55-1152">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="12a55-1153">Se ha agregado compatibilidad para PR_GET_PDEATHSIG.</span><span class="sxs-lookup"><span data-stu-id="12a55-1153">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="12a55-1154">Se ha agregado compatibilidad para CLONE_PARENT</span><span class="sxs-lookup"><span data-stu-id="12a55-1154">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="12a55-1155">Se ha corregido un error en el que la canalización se bloquea, es decir, bash -c "ls -alR /" | bash -c "cat" (GH 1214)</span><span class="sxs-lookup"><span data-stu-id="12a55-1155">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="12a55-1156">Controla las solicitudes para conectarse al terminal actual.</span><span class="sxs-lookup"><span data-stu-id="12a55-1156">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="12a55-1157">Marca /proc/<pid>/oom_score_adj como grabable.</span><span class="sxs-lookup"><span data-stu-id="12a55-1157">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="12a55-1158">Agrega la carpeta/sys/fs/cgroup.</span><span class="sxs-lookup"><span data-stu-id="12a55-1158">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="12a55-1159">sched_setaffinity debe devolver el número de máscara de bits de afinidad</span><span class="sxs-lookup"><span data-stu-id="12a55-1159">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="12a55-1160">Corrige la lógica de validación de ELF que presupone incorrectamente que las rutas de intérprete deben tener menos de 64 caracteres de longitud.</span><span class="sxs-lookup"><span data-stu-id="12a55-1160">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="12a55-1161">(GH 743)</span><span class="sxs-lookup"><span data-stu-id="12a55-1161">(GH #743)</span></span>
- <span data-ttu-id="12a55-1162">Los descriptores de archivos abiertos pueden mantener abierta la ventana de la consola (GH 1187)</span><span class="sxs-lookup"><span data-stu-id="12a55-1162">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="12a55-1163">Se ha corregido el error en el que no se podía completar rename() con la barra diagonal final en el nombre de destino (GH 1008)</span><span class="sxs-lookup"><span data-stu-id="12a55-1163">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="12a55-1164">Implementa el archivo /proc/net/dev</span><span class="sxs-lookup"><span data-stu-id="12a55-1164">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="12a55-1165">Se han corregido los pings de 0,000 ms debido a la resolución del temporizador.</span><span class="sxs-lookup"><span data-stu-id="12a55-1165">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="12a55-1166">Se ha implementado /proc/self/environ (GH 730)</span><span class="sxs-lookup"><span data-stu-id="12a55-1166">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="12a55-1167">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-1167">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-1168">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-1168">LTP Results:</span></span>
<span data-ttu-id="12a55-1169">Número de pruebas superadas: 664</span><span class="sxs-lookup"><span data-stu-id="12a55-1169">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="12a55-1170">Número de no superadas (error, omitidas, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="12a55-1170">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="12a55-1171">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="12a55-1171">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="12a55-1172">Compilación 14959</span><span class="sxs-lookup"><span data-stu-id="12a55-1172">Build 14959</span></span>

<span data-ttu-id="12a55-1173">Para obtener información general de Windows sobre la compilación 14959, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span><span class="sxs-lookup"><span data-stu-id="12a55-1173">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-1174">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-1174">Fixed</span></span>

- <span data-ttu-id="12a55-1175">Se ha mejorado la notificación del proceso PICO para Windows.</span><span class="sxs-lookup"><span data-stu-id="12a55-1175">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="12a55-1176">Encuentra información adicional en el [blog de WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span><span class="sxs-lookup"><span data-stu-id="12a55-1176">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="12a55-1177">Se ha mejorado la estabilidad de interoperabilidad con Windows</span><span class="sxs-lookup"><span data-stu-id="12a55-1177">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="12a55-1178">Se ha corregido el error 0x80070057 al iniciar bash.exe cuando Protección de datos de empresa (EDP) está habilitado</span><span class="sxs-lookup"><span data-stu-id="12a55-1178">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="12a55-1179">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-1179">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-1180">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-1180">LTP Results:</span></span>
<span data-ttu-id="12a55-1181">Número de pruebas superadas: 665</span><span class="sxs-lookup"><span data-stu-id="12a55-1181">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="12a55-1182">Número de no superadas (error, omitidas, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="12a55-1182">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="12a55-1183">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="12a55-1183">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="12a55-1184">Compilación 14955</span><span class="sxs-lookup"><span data-stu-id="12a55-1184">Build 14955</span></span>

<span data-ttu-id="12a55-1185">Para obtener información general de Windows sobre la compilación 14955, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span><span class="sxs-lookup"><span data-stu-id="12a55-1185">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-1186">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-1186">Fixed</span></span>

 - <span data-ttu-id="12a55-1187">Debido a circunstancias más allá de nuestro control, no hay ninguna actualización en esta compilación para el subsistema de Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="12a55-1187">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="12a55-1188">Las actualizaciones programadas regularmente se reanudarán en la próxima versión.</span><span class="sxs-lookup"><span data-stu-id="12a55-1188">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-1189">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-1189">LTP Results:</span></span>
<span data-ttu-id="12a55-1190">Número de pruebas superadas: 665</span><span class="sxs-lookup"><span data-stu-id="12a55-1190">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="12a55-1191">Número de no superadas (error, omitidas, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="12a55-1191">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="12a55-1192">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="12a55-1192">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="12a55-1193">Compilación 14951</span><span class="sxs-lookup"><span data-stu-id="12a55-1193">Build 14951</span></span>

<span data-ttu-id="12a55-1194">Para obtener información general de Windows sobre la compilación 14951, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="12a55-1194">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="12a55-1195">Nueva característica: Interoperabilidad de Windows/Ubuntu</span><span class="sxs-lookup"><span data-stu-id="12a55-1195">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="12a55-1196">Ahora se pueden invocar archivos binarios de Windows directamente desde la línea de comandos de WSL.</span><span class="sxs-lookup"><span data-stu-id="12a55-1196">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="12a55-1197">Esto da a los usuarios la capacidad de interactuar con el entorno y el sistema Windows de una manera que antes no era posible.</span><span class="sxs-lookup"><span data-stu-id="12a55-1197">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="12a55-1198">Como ejemplo rápido, ahora es posible que los usuarios ejecuten los siguientes comandos:</span><span class="sxs-lookup"><span data-stu-id="12a55-1198">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="12a55-1199">Puedes encontrar más información en:</span><span class="sxs-lookup"><span data-stu-id="12a55-1199">More information can be found at:</span></span>

- [<span data-ttu-id="12a55-1200">Blog del equipo de WSL para Interop</span><span class="sxs-lookup"><span data-stu-id="12a55-1200">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="12a55-1201">Documentación de interoperabilidad de MSDN</span><span class="sxs-lookup"><span data-stu-id="12a55-1201">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="12a55-1202">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-1202">Fixed</span></span>

- <span data-ttu-id="12a55-1203">Ubuntu 16.04 (Xenial) ahora se instala para todas las instancias nuevas de WSL.</span><span class="sxs-lookup"><span data-stu-id="12a55-1203">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="12a55-1204">Los usuarios con instancias existentes de 14.04 (Trusty) no se actualizarán automáticamente.</span><span class="sxs-lookup"><span data-stu-id="12a55-1204">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="12a55-1205">Ahora se muestra la configuración regional establecida durante la instalación</span><span class="sxs-lookup"><span data-stu-id="12a55-1205">Locale set during install is now displayed</span></span>
- <span data-ttu-id="12a55-1206">Mejoras del terminal, que incluido un error en el que la redirección de un proceso de WSL a un archivo no siempre funciona</span><span class="sxs-lookup"><span data-stu-id="12a55-1206">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="12a55-1207">La duración de la consola debe estar asociada a la duración de bash.exe</span><span class="sxs-lookup"><span data-stu-id="12a55-1207">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="12a55-1208">El tamaño de la ventana de la consola debe usar un tamaño visible, no el tamaño del búfer</span><span class="sxs-lookup"><span data-stu-id="12a55-1208">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="12a55-1209">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-1209">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-1210">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-1210">LTP Results:</span></span>
<span data-ttu-id="12a55-1211">Número de pruebas superadas: 665</span><span class="sxs-lookup"><span data-stu-id="12a55-1211">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="12a55-1212">Número de no superadas (error, omitidas, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="12a55-1212">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="12a55-1213">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="12a55-1213">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="12a55-1214">Compilación 14946</span><span class="sxs-lookup"><span data-stu-id="12a55-1214">Build 14946</span></span>

<span data-ttu-id="12a55-1215">Para obtener información general de Windows sobre la compilación 14946, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span><span class="sxs-lookup"><span data-stu-id="12a55-1215">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-1216">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-1216">Fixed</span></span>

- <span data-ttu-id="12a55-1217">Se ha corregido un problema que impedía la creación de cuentas de usuario de WSL para los usuarios con nombres de usuario de NT que contienen espacios o comillas.</span><span class="sxs-lookup"><span data-stu-id="12a55-1217">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="12a55-1218">Cambia VolFs y DrvFs para que devuelvan 0 para el recuento de vínculos de directorio en stat</span><span class="sxs-lookup"><span data-stu-id="12a55-1218">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="12a55-1219">Compatibilidad con la opción de socket IPV6_MULTICAST_HOPS.</span><span class="sxs-lookup"><span data-stu-id="12a55-1219">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="12a55-1220">Limite a un único bucle de E/S de la consola por tty.</span><span class="sxs-lookup"><span data-stu-id="12a55-1220">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="12a55-1221">Por ejemplo, el comando siguiente es posible:</span><span class="sxs-lookup"><span data-stu-id="12a55-1221">Example: the following command is possible:</span></span>
  - <span data-ttu-id="12a55-1222">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span><span class="sxs-lookup"><span data-stu-id="12a55-1222">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="12a55-1223">Reemplaza espacios con tabulaciones en/proc/cpuinfo (GH 1115)</span><span class="sxs-lookup"><span data-stu-id="12a55-1223">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="12a55-1224">DrvFs aparece ahora en mountinfo con un nombre que coincide con el volumen de Windows montado</span><span class="sxs-lookup"><span data-stu-id="12a55-1224">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="12a55-1225">/home y /root ahora aparecen en mountinfo con los nombres correctos</span><span class="sxs-lookup"><span data-stu-id="12a55-1225">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="12a55-1226">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-1226">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-1227">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-1227">LTP Results:</span></span>
<span data-ttu-id="12a55-1228">Número de pruebas superadas: 665</span><span class="sxs-lookup"><span data-stu-id="12a55-1228">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="12a55-1229">Número de no superadas (error, omitidas, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="12a55-1229">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="12a55-1230">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="12a55-1230">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="12a55-1231">Compilación 14942</span><span class="sxs-lookup"><span data-stu-id="12a55-1231">Build 14942</span></span>

<span data-ttu-id="12a55-1232">Para obtener información general de Windows sobre la compilación 14942, visita el [blog de Windows](https://aka.ms/onefourninefourtwoooooo).</span><span class="sxs-lookup"><span data-stu-id="12a55-1232">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-1233">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-1233">Fixed</span></span>

- <span data-ttu-id="12a55-1234">Un número de comprobaciones de error direccionadas, incluido el bloqueo de red "ATTEMPTED EXECUTE OF NOEXECUTE MEMORY" que bloqueaba SSH</span><span class="sxs-lookup"><span data-stu-id="12a55-1234">A number of bugchecks addressed, including the “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” networking crash which was blocking SSH</span></span>
- <span data-ttu-id="12a55-1235">Ahora se incluye la compatibilidad de inotifiy con las notificaciones generadas desde aplicaciones Windows en DrvFs</span><span class="sxs-lookup"><span data-stu-id="12a55-1235">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="12a55-1236">Implementa TCP_KEEPIDLE y TCP_KEEPINTVL para mongod.</span><span class="sxs-lookup"><span data-stu-id="12a55-1236">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="12a55-1237">(GH 695)</span><span class="sxs-lookup"><span data-stu-id="12a55-1237">(GH #695)</span></span>
- <span data-ttu-id="12a55-1238">Implementa la llamada del sistema pivot_root</span><span class="sxs-lookup"><span data-stu-id="12a55-1238">Implement the pivot_root system call</span></span>
- <span data-ttu-id="12a55-1239">Implementa la opción de socket para SO_DONTROUTE</span><span class="sxs-lookup"><span data-stu-id="12a55-1239">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="12a55-1240">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-1240">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="12a55-1241">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-1241">LTP Results:</span></span>
<span data-ttu-id="12a55-1242">Número de pruebas superadas: 665</span><span class="sxs-lookup"><span data-stu-id="12a55-1242">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="12a55-1243">Número de no superadas (error, omitidas, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="12a55-1243">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="12a55-1244">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="12a55-1244">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="12a55-1245">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="12a55-1245">Syscall Support</span></span>
<span data-ttu-id="12a55-1246">A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="12a55-1246">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="12a55-1247">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="12a55-1247">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="12a55-1248">Compilación 14936</span><span class="sxs-lookup"><span data-stu-id="12a55-1248">Build 14936</span></span>

<span data-ttu-id="12a55-1249">Para obtener información general de Windows sobre la compilación 14936, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="12a55-1249">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="12a55-1250">Nota: WSL instalará Ubuntu versión 16.04 (Xenial) en lugar de Ubuntu 14.04 (Trusty) en una próxima versión.</span><span class="sxs-lookup"><span data-stu-id="12a55-1250">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="12a55-1251">Este cambio se aplicará a los usuarios de Insider que instalen nuevas instancias (lxrun.exe /install o a la primera ejecución de bash.exe).</span><span class="sxs-lookup"><span data-stu-id="12a55-1251">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="12a55-1252">Las instancias existentes con Trusty no se actualizarán automáticamente.</span><span class="sxs-lookup"><span data-stu-id="12a55-1252">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="12a55-1253">Los usuarios pueden actualizar su imagen de Trusty a Xenial con el comando do-release-upgrade.</span><span class="sxs-lookup"><span data-stu-id="12a55-1253">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="12a55-1254">Problema conocido</span><span class="sxs-lookup"><span data-stu-id="12a55-1254">Known Issue</span></span>
<span data-ttu-id="12a55-1255">WSL está experimentando un problema con algunas implementaciones de sockets.</span><span class="sxs-lookup"><span data-stu-id="12a55-1255">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="12a55-1256">La comprobación de errores se manifiesta como bloqueo con el error "ATTEMPTED EXECUTE OF NOEXECUTE MEMORY".</span><span class="sxs-lookup"><span data-stu-id="12a55-1256">The bugcheck manifests itself as a crash with the error “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”.</span></span>  <span data-ttu-id="12a55-1257">La manifestación más común de este problema es un bloqueo cuando se usa ssh.</span><span class="sxs-lookup"><span data-stu-id="12a55-1257">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="12a55-1258">La causa principal se ha corregido en las compilaciones internas y se enviará a los usuarios de Insider lo antes posible.</span><span class="sxs-lookup"><span data-stu-id="12a55-1258">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="12a55-1259">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-1259">Fixed</span></span>

- <span data-ttu-id="12a55-1260">Se ha implementado la llamada del sistema chroot</span><span class="sxs-lookup"><span data-stu-id="12a55-1260">Implemented the chroot system call</span></span>
- <span data-ttu-id="12a55-1261">Mejoras en inotify, ~~incluida la compatibilidad con las notificaciones generadas desde aplicaciones Windows en DrvFs~~</span><span class="sxs-lookup"><span data-stu-id="12a55-1261">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="12a55-1262">Corrección: La compatibilidad de inotify con los cambios que se originan en aplicaciones Windows no está disponible en este momento.</span><span class="sxs-lookup"><span data-stu-id="12a55-1262">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="12a55-1263">El enlace de sockets a IPV6::<port n> ahora admite IPV6_V6ONLY (GH 68, 157, 393, 460, 674, 740, 982, 996)</span><span class="sxs-lookup"><span data-stu-id="12a55-1263">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="12a55-1264">Se ha implementado el comportamiento de WNOWAIT para la llamada del sistema waitid (GH 638)</span><span class="sxs-lookup"><span data-stu-id="12a55-1264">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="12a55-1265">Compatibilidad con las opciones de socket de IP IP_HDRINCL e IP_TTL</span><span class="sxs-lookup"><span data-stu-id="12a55-1265">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="12a55-1266">read() de longitud cero debe volver inmediatamente (GH 975)</span><span class="sxs-lookup"><span data-stu-id="12a55-1266">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="12a55-1267">Controla correctamente los nombres de archivo y los prefijos de nombre de archivo que no incluyen un terminador NULL en un archivo .tar.</span><span class="sxs-lookup"><span data-stu-id="12a55-1267">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="12a55-1268">Compatibilidad de epoll para /dev/null</span><span class="sxs-lookup"><span data-stu-id="12a55-1268">epoll support for /dev/null</span></span>
- <span data-ttu-id="12a55-1269">Corrección del origen de hora de /dev/alarm</span><span class="sxs-lookup"><span data-stu-id="12a55-1269">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="12a55-1270">bash -c ahora puede redirigir a un archivo</span><span class="sxs-lookup"><span data-stu-id="12a55-1270">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="12a55-1271">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-1271">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-1272">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-1272">LTP Results:</span></span>
<span data-ttu-id="12a55-1273">Número de pruebas superadas: 664</span><span class="sxs-lookup"><span data-stu-id="12a55-1273">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="12a55-1274">Número de no superadas (error, omitidas, etc.): 264</span><span class="sxs-lookup"><span data-stu-id="12a55-1274">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="12a55-1275">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="12a55-1275">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="12a55-1276">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="12a55-1276">Syscall Support</span></span>
<span data-ttu-id="12a55-1277">A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="12a55-1277">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="12a55-1278">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="12a55-1278">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="12a55-1279">Compilación 14931</span><span class="sxs-lookup"><span data-stu-id="12a55-1279">Build 14931</span></span>

<span data-ttu-id="12a55-1280">Para obtener información general de Windows sobre la compilación 14931, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="12a55-1280">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-1281">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-1281">Fixed</span></span>

 - <span data-ttu-id="12a55-1282">Debido a circunstancias más allá de nuestro control, no hay ninguna actualización en esta compilación para el subsistema de Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="12a55-1282">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="12a55-1283">Las actualizaciones programadas regularmente se reanudarán en la próxima versión.</span><span class="sxs-lookup"><span data-stu-id="12a55-1283">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="12a55-1284">Compilación 14926</span><span class="sxs-lookup"><span data-stu-id="12a55-1284">Build 14926</span></span>

<span data-ttu-id="12a55-1285">Para obtener información general de Windows sobre la compilación 14926, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="12a55-1285">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-1286">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-1286">Fixed</span></span>

- <span data-ttu-id="12a55-1287">Ping ahora funciona en consolas que no tienen privilegios de administrador</span><span class="sxs-lookup"><span data-stu-id="12a55-1287">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="12a55-1288">Ahora también se admite Ping6, sin privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="12a55-1288">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="12a55-1289">Compatibilidad de inotify con archivos modificados a través de WSL.</span><span class="sxs-lookup"><span data-stu-id="12a55-1289">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="12a55-1290">(GH 216)</span><span class="sxs-lookup"><span data-stu-id="12a55-1290">(GH #216)</span></span>
  - <span data-ttu-id="12a55-1291">Marcas admitidas:</span><span class="sxs-lookup"><span data-stu-id="12a55-1291">Flags supported:</span></span>
    - <span data-ttu-id="12a55-1292">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="12a55-1292">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="12a55-1293">Eventos de inotify_add_watch: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="12a55-1293">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="12a55-1294">Atributos de inotify_add_watch: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="12a55-1294">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="12a55-1295">Salida de lectura: LX_IN_ISDIR, LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="12a55-1295">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="12a55-1296">Problema conocido: La modificación de archivos desde aplicaciones de Windows no genera ningún evento</span><span class="sxs-lookup"><span data-stu-id="12a55-1296">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="12a55-1297">El socket de Unix ahora es compatible con SCM_CREDENTIALS</span><span class="sxs-lookup"><span data-stu-id="12a55-1297">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="12a55-1298">Resultados de LTP:</span><span class="sxs-lookup"><span data-stu-id="12a55-1298">LTP Results:</span></span>
<span data-ttu-id="12a55-1299">Número de pruebas superadas: 651</span><span class="sxs-lookup"><span data-stu-id="12a55-1299">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="12a55-1300">Número de no superadas (error, omitidas, etc.): 258</span><span class="sxs-lookup"><span data-stu-id="12a55-1300">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="12a55-1301">Registros de ejecución de pruebas de LTP</span><span class="sxs-lookup"><span data-stu-id="12a55-1301">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="12a55-1302">Compilación 14915</span><span class="sxs-lookup"><span data-stu-id="12a55-1302">Build 14915</span></span>

<span data-ttu-id="12a55-1303">Para obtener información general de Windows sobre la compilación 14915, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="12a55-1303">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-1304">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-1304">Fixed</span></span>
-  <span data-ttu-id="12a55-1305">Socketpair para sockets de datagramas de Unix (GH 262)</span><span class="sxs-lookup"><span data-stu-id="12a55-1305">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="12a55-1306">Compatibilidad con el socket de Unix para SO_REUSEADDR</span><span class="sxs-lookup"><span data-stu-id="12a55-1306">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="12a55-1307">Compatibilidad con el socket de Unix para SO_BROADCAST (GH 568)</span><span class="sxs-lookup"><span data-stu-id="12a55-1307">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="12a55-1308">Compatibilidad con el socket de Unix para SOCK_SEQPACKET (GH 758, 546)</span><span class="sxs-lookup"><span data-stu-id="12a55-1308">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="12a55-1309">Adición de compatibilidad para socket de datagramas de Unix send, recv y shutdown</span><span class="sxs-lookup"><span data-stu-id="12a55-1309">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="12a55-1310">Corrección de comprobación de errores debido a la validación de parámetros mmap no válida para direcciones no fijas.</span><span class="sxs-lookup"><span data-stu-id="12a55-1310">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="12a55-1311">(GH 847)</span><span class="sxs-lookup"><span data-stu-id="12a55-1311">(GH #847)</span></span>
- <span data-ttu-id="12a55-1312">Compatibilidad para suspender o reanudar los estados del terminal</span><span class="sxs-lookup"><span data-stu-id="12a55-1312">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="12a55-1313">Compatibilidad para TIOCPKT ioctl para desbloquear la utilidad de pantalla (GH 774)</span><span class="sxs-lookup"><span data-stu-id="12a55-1313">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="12a55-1314">Problema conocido: Las teclas de función no funcionan</span><span class="sxs-lookup"><span data-stu-id="12a55-1314">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="12a55-1315">Se ha corregido una carrera en TimerFd que podía hacer que LxpTimerFdWorkerRoutine accediera a un miembro liberado "ReaderReady" (GH 814)</span><span class="sxs-lookup"><span data-stu-id="12a55-1315">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="12a55-1316">Habilita la compatibilidad con llamadas del sistema reiniciables para futex, poll y clock_nanosleep</span><span class="sxs-lookup"><span data-stu-id="12a55-1316">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="12a55-1317">Se ha agregado compatibilidad con montaje de enlace</span><span class="sxs-lookup"><span data-stu-id="12a55-1317">Added bind mount support</span></span>
- <span data-ttu-id="12a55-1318">Compatibilidad para dejar de compartir el espacio de nombres de montaje</span><span class="sxs-lookup"><span data-stu-id="12a55-1318">unshare for mount namespace support</span></span>
    - <span data-ttu-id="12a55-1319">Problema conocido: Al crear un nuevo espacio de nombres de montaje con `unshare(CLONE_NEWNS)`, el directorio de trabajo actual continuará señalando al espacio de nombres anterior</span><span class="sxs-lookup"><span data-stu-id="12a55-1319">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="12a55-1320">Mejoras y correcciones de errores adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-1320">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="12a55-1321">Compilación 14905</span><span class="sxs-lookup"><span data-stu-id="12a55-1321">Build 14905</span></span>

<span data-ttu-id="12a55-1322">Para obtener información general de Windows sobre la compilación 14905, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span><span class="sxs-lookup"><span data-stu-id="12a55-1322">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-1323">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-1323">Fixed</span></span>
- <span data-ttu-id="12a55-1324">Ahora se admiten llamadas del sistema reiniciables (GH 349, GH 520)</span><span class="sxs-lookup"><span data-stu-id="12a55-1324">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="12a55-1325">Los vínculos simbólicos a directorios que terminan en / ahora están operativos (GH 650)</span><span class="sxs-lookup"><span data-stu-id="12a55-1325">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="12a55-1326">Se ha implementado RNDGETENTCNT ioctl para /dev/random</span><span class="sxs-lookup"><span data-stu-id="12a55-1326">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="12a55-1327">Se han implementado los archivos /proc/[pid]/mounts, /proc/[pid]/mountinfo y /proc/[pid]/mountstats</span><span class="sxs-lookup"><span data-stu-id="12a55-1327">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="12a55-1328">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-1328">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="12a55-1329">Compilación 14901</span><span class="sxs-lookup"><span data-stu-id="12a55-1329">Build 14901</span></span>
<span data-ttu-id="12a55-1330">Primera compilación de Insider para la versión posterior a la Actualización de aniversario de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="12a55-1330">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="12a55-1331">Para obtener información general de Windows sobre la compilación 14901, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="12a55-1331">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-1332">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-1332">Fixed</span></span>
- <span data-ttu-id="12a55-1333">Se ha corregido un problema de barra diagonal final</span><span class="sxs-lookup"><span data-stu-id="12a55-1333">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="12a55-1334">Ahora funcionan los comandos como `$ mv a/c/ a/b/`</span><span class="sxs-lookup"><span data-stu-id="12a55-1334">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="12a55-1335">Al instalar ahora se pregunta si la configuración regional de Ubuntu debe establecerse en la configuración regional de Windows</span><span class="sxs-lookup"><span data-stu-id="12a55-1335">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="12a55-1336">Compatibilidad de procfs para la carpeta ns</span><span class="sxs-lookup"><span data-stu-id="12a55-1336">Procfs support for ns folder</span></span>
- <span data-ttu-id="12a55-1337">Se ha agregado mount y unmount para los sistemas de archivos tmpfs, procfs y sysfs</span><span class="sxs-lookup"><span data-stu-id="12a55-1337">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="12a55-1338">Corrección de la firma ABI mknod[at] de 32 bits</span><span class="sxs-lookup"><span data-stu-id="12a55-1338">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="12a55-1339">Los sockets de Unix se movieron al modelo dispatch</span><span class="sxs-lookup"><span data-stu-id="12a55-1339">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="12a55-1340">Se debe respetar el tamaño del búfer de recepción del socket de INET mediante setsockopt</span><span class="sxs-lookup"><span data-stu-id="12a55-1340">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="12a55-1341">Implementa la marca de mensaje de recepción de socket de Unix MSG_CMSG_CLOEXEC</span><span class="sxs-lookup"><span data-stu-id="12a55-1341">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="12a55-1342">Redirección de canalización stdin/stdout de proceso de Linux (GH 2)</span><span class="sxs-lookup"><span data-stu-id="12a55-1342">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="12a55-1343">Permite la canalización de comandos bash -c en CMD.</span><span class="sxs-lookup"><span data-stu-id="12a55-1343">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="12a55-1344">Ejemplo:  >dir | bash -c "grep foo"</span><span class="sxs-lookup"><span data-stu-id="12a55-1344">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="12a55-1345">Bash ahora se puede instalar en sistemas con varios archivos de página (GH 538, 358)</span><span class="sxs-lookup"><span data-stu-id="12a55-1345">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="12a55-1346">El tamaño predeterminado del búfer del socket de INET debe coincidir con el de la configuración predeterminada de Ubuntu</span><span class="sxs-lookup"><span data-stu-id="12a55-1346">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="12a55-1347">Alinea las llamadas del sistema xattr con listxattr</span><span class="sxs-lookup"><span data-stu-id="12a55-1347">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="12a55-1348">Solo se devuelven interfaces con una dirección IPv4 válida de SIOCGIFCONF</span><span class="sxs-lookup"><span data-stu-id="12a55-1348">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="12a55-1349">Corrección de la acción predeterminada de la señal cuando se inserta por ptrace</span><span class="sxs-lookup"><span data-stu-id="12a55-1349">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="12a55-1350">Implementa /proc/sys/vm/min_free_kbytes</span><span class="sxs-lookup"><span data-stu-id="12a55-1350">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="12a55-1351">Usa valores de registro de contexto de equipo al restaurar el contexto en sigreturn</span><span class="sxs-lookup"><span data-stu-id="12a55-1351">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="12a55-1352">Esto resuelve el problema por el que java y javac se bloqueaban para algunos usuarios</span><span class="sxs-lookup"><span data-stu-id="12a55-1352">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="12a55-1353">Implementa /proc/sys/kernel/hostname</span><span class="sxs-lookup"><span data-stu-id="12a55-1353">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="12a55-1354">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="12a55-1354">Syscall Support</span></span>
<span data-ttu-id="12a55-1355">A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="12a55-1355">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="12a55-1356">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="12a55-1356">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="12a55-1357">Compilación 14388 para la Actualización de aniversario de Windows 10</span><span class="sxs-lookup"><span data-stu-id="12a55-1357">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="12a55-1358">Para obtener información general de Windows sobre la compilación 14388, visita el [blog de Windows](https://aka.ms/14388wip).</span><span class="sxs-lookup"><span data-stu-id="12a55-1358">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="12a55-1359">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-1359">Fixed</span></span>
- <span data-ttu-id="12a55-1360">Correcciones para prepararse para la Actualización de aniversario de Windows 10 el 2/8</span><span class="sxs-lookup"><span data-stu-id="12a55-1360">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="12a55-1361">Puedes encontrar más información sobre WSL en la Actualización de aniversario en nuestro [blog](https://blogs.msdn.microsoft.com/wsl/)</span><span class="sxs-lookup"><span data-stu-id="12a55-1361">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="12a55-1362">Compilación 14376</span><span class="sxs-lookup"><span data-stu-id="12a55-1362">Build 14376</span></span>
<span data-ttu-id="12a55-1363">Para obtener información general de Windows sobre la compilación 14376, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="12a55-1363">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="12a55-1364">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-1364">Fixed</span></span>
- <span data-ttu-id="12a55-1365">Se quitaron algunas instancias en las que apt-get se bloquea (GH 493)</span><span class="sxs-lookup"><span data-stu-id="12a55-1365">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="12a55-1366">Se ha corregido un problema por el que los montajes vacíos no se controlaban correctamente</span><span class="sxs-lookup"><span data-stu-id="12a55-1366">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="12a55-1367">Se ha corregido un problema por el que ramdisks no se montaban correctamente</span><span class="sxs-lookup"><span data-stu-id="12a55-1367">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="12a55-1368">Cambio en la aceptación de sockets de Unix para admitir marcas (GH parcial 451)</span><span class="sxs-lookup"><span data-stu-id="12a55-1368">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="12a55-1369">Se ha corregido la pantalla azul relacionada con la red común</span><span class="sxs-lookup"><span data-stu-id="12a55-1369">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="12a55-1370">Se ha corregido la pantalla azul al acceder a /proc/[pid]/task (GH 523)</span><span class="sxs-lookup"><span data-stu-id="12a55-1370">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="12a55-1371">Se ha corregido un uso elevado de la CPU en algunos escenarios de pty (GH 488, 504)</span><span class="sxs-lookup"><span data-stu-id="12a55-1371">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="12a55-1372">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-1372">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="12a55-1373">Compilación 14371</span><span class="sxs-lookup"><span data-stu-id="12a55-1373">Build 14371</span></span>
<span data-ttu-id="12a55-1374">Para obtener información general de Windows sobre la compilación 14371, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="12a55-1374">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="12a55-1375">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-1375">Fixed</span></span>
- <span data-ttu-id="12a55-1376">Se ha corregido la carrera de tiempo con SIGCHLD y wait() al usar ptrace</span><span class="sxs-lookup"><span data-stu-id="12a55-1376">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="12a55-1377">Se han corregido comportamientos cuando las rutas de acceso tienen una / final (GH 432)</span><span class="sxs-lookup"><span data-stu-id="12a55-1377">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="12a55-1378">Se ha corregido un problema con el error de cambio de nombre o desvinculación debido a identificadores abiertos a elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="12a55-1378">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="12a55-1379">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-1379">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="12a55-1380">Compilación 14366</span><span class="sxs-lookup"><span data-stu-id="12a55-1380">Build 14366</span></span>
<span data-ttu-id="12a55-1381">Para obtener información general de Windows sobre la compilación 14366, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span><span class="sxs-lookup"><span data-stu-id="12a55-1381">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="12a55-1382">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-1382">Fixed</span></span>
- <span data-ttu-id="12a55-1383">Corrección en la creación de archivos mediante vínculos simbólicos</span><span class="sxs-lookup"><span data-stu-id="12a55-1383">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="12a55-1384">Se ha agregado listxattr para Python (GH 385)</span><span class="sxs-lookup"><span data-stu-id="12a55-1384">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="12a55-1385">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-1385">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="12a55-1386">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="12a55-1386">Syscall Support</span></span>
-   <span data-ttu-id="12a55-1387">A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="12a55-1387">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="12a55-1388">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="12a55-1388">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="12a55-1389">Compilación 14361</span><span class="sxs-lookup"><span data-stu-id="12a55-1389">Build 14361</span></span>
<span data-ttu-id="12a55-1390">Para obtener información general de Windows sobre la compilación 14361, visita el [blog de Windows](https://aka.ms/wip14361).</span><span class="sxs-lookup"><span data-stu-id="12a55-1390">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="12a55-1391">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-1391">Fixed</span></span>
- <span data-ttu-id="12a55-1392">DrvFs ahora distingue entre mayúsculas y minúsculas cuando se ejecuta en Bash en Ubuntu en Windows.</span><span class="sxs-lookup"><span data-stu-id="12a55-1392">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="12a55-1393">Los usuarios pueden usar case.txt y CASE.TXT en sus unidades de /mnt/c</span><span class="sxs-lookup"><span data-stu-id="12a55-1393">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="12a55-1394">La distinción de mayúsculas y minúsculas solo se admite en Bash en Ubuntu en Windows.</span><span class="sxs-lookup"><span data-stu-id="12a55-1394">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="12a55-1395">Fuera de Bash, NTFS notificará los archivos correctamente, pero puede producirse un comportamiento inesperado al interactuar con los archivos de Windows.</span><span class="sxs-lookup"><span data-stu-id="12a55-1395">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="12a55-1396">La raíz de cada volumen (es decir, /mnt/c) no distingue entre mayúsculas y minúsculas</span><span class="sxs-lookup"><span data-stu-id="12a55-1396">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="12a55-1397">Puedes encontrar más información sobre cómo controlar estos archivos en Windows [aquí](https://support.microsoft.com/en-us/kb/100625).</span><span class="sxs-lookup"><span data-stu-id="12a55-1397">More information on handling these files in Windows can be found [here](https://support.microsoft.com/en-us/kb/100625).</span></span>
- <span data-ttu-id="12a55-1398">Compatibilidad con pty/tty considerablemente mejorada.</span><span class="sxs-lookup"><span data-stu-id="12a55-1398">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="12a55-1399">Ahora se admiten aplicaciones como TMUX (GH 40)</span><span class="sxs-lookup"><span data-stu-id="12a55-1399">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="12a55-1400">Se ha corregido el problema de instalación por el que las cuentas de usuario no siempre se creaban</span><span class="sxs-lookup"><span data-stu-id="12a55-1400">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="12a55-1401">Se ha optimizado la estructura de argumentos de línea de comandos que permite una lista de argumentos extremadamente larga.</span><span class="sxs-lookup"><span data-stu-id="12a55-1401">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="12a55-1402">(GH 153)</span><span class="sxs-lookup"><span data-stu-id="12a55-1402">(GH #153)</span></span>
- <span data-ttu-id="12a55-1403">Ahora puedes usar delete y chmod en archivos read_only de DrvFs</span><span class="sxs-lookup"><span data-stu-id="12a55-1403">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="12a55-1404">Se han corregido algunas instancias en las que el terminal se bloquea en la desconexión (GH 43)</span><span class="sxs-lookup"><span data-stu-id="12a55-1404">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="12a55-1405">chmod y chown ahora funcionan en dispositivos tty</span><span class="sxs-lookup"><span data-stu-id="12a55-1405">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="12a55-1406">Permite la conexión a 0.0.0.0 y :: como localhost (GH 388)</span><span class="sxs-lookup"><span data-stu-id="12a55-1406">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="12a55-1407">Sendmsg/recvmsg ahora controlan una longitud de vector de E/S > 1 (GH parcial 376)</span><span class="sxs-lookup"><span data-stu-id="12a55-1407">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="12a55-1408">Los usuarios ahora pueden dejar de participar en archivos de hosts generados automáticamente (GH 398)</span><span class="sxs-lookup"><span data-stu-id="12a55-1408">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="12a55-1409">La configuración regional de Linux se ajusta automáticamente con la configuración regional de NT durante la instalación (GH 11)</span><span class="sxs-lookup"><span data-stu-id="12a55-1409">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="12a55-1410">Se ha agregado el archivo /proc/sys/vm/swappiness (GH 306)</span><span class="sxs-lookup"><span data-stu-id="12a55-1410">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="12a55-1411">strace ahora se cierra correctamente</span><span class="sxs-lookup"><span data-stu-id="12a55-1411">strace now exits correctly</span></span>
- <span data-ttu-id="12a55-1412">Permite que las canalizaciones se vuelvan a abrir a través de /proc/self/fd (GH 222)</span><span class="sxs-lookup"><span data-stu-id="12a55-1412">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="12a55-1413">Oculta directorios en %LOCALAPPDATA%\lxss de DrvFs (GH 270)</span><span class="sxs-lookup"><span data-stu-id="12a55-1413">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="12a55-1414">Mejor control de bash.exe ~.</span><span class="sxs-lookup"><span data-stu-id="12a55-1414">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="12a55-1415">Ahora se admiten comandos como "bash ~-c ls" (GH 467)</span><span class="sxs-lookup"><span data-stu-id="12a55-1415">Commands like “bash ~ -c ls” now supported (GH #467)</span></span>
- <span data-ttu-id="12a55-1416">Ahora, los sockets notifican las lecturas de epoll disponibles durante el cierre (GH 271)</span><span class="sxs-lookup"><span data-stu-id="12a55-1416">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="12a55-1417">lxrun /uninstall funciona mejor para eliminar archivos y carpetas</span><span class="sxs-lookup"><span data-stu-id="12a55-1417">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="12a55-1418">Se ha corregido ps -f (GH 246)</span><span class="sxs-lookup"><span data-stu-id="12a55-1418">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="12a55-1419">Se ha mejorado la compatibilidad con aplicaciones X11, como xEmacs (GH 481)</span><span class="sxs-lookup"><span data-stu-id="12a55-1419">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="12a55-1420">Se ha actualizado el tamaño inicial de la pila de subprocesos para que coincida con la configuración predeterminada de Ubuntu, y se notifica el tamaño correctamente a la llamada del sistema get_rlimit (GH 172, 258)</span><span class="sxs-lookup"><span data-stu-id="12a55-1420">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="12a55-1421">Se ha mejorado la notificación de nombres de imagen de proceso PICO (por ejemplo, para auditoría)</span><span class="sxs-lookup"><span data-stu-id="12a55-1421">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="12a55-1422">Se ha implementado el comando /proc/mountinfo para df</span><span class="sxs-lookup"><span data-stu-id="12a55-1422">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="12a55-1423">Se ha corregido el código de error de vínculo simbólico para el nombre secundario .</span><span class="sxs-lookup"><span data-stu-id="12a55-1423">Fixed symlink error code for child name .</span></span> <span data-ttu-id="12a55-1424">y ..</span><span class="sxs-lookup"><span data-stu-id="12a55-1424">and ..</span></span>
- <span data-ttu-id="12a55-1425">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-1425">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="12a55-1426">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="12a55-1426">Syscall Support</span></span>
<span data-ttu-id="12a55-1427">A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="12a55-1427">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="12a55-1428">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="12a55-1428">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="12a55-1429">Compilación 14352</span><span class="sxs-lookup"><span data-stu-id="12a55-1429">Build 14352</span></span>
<span data-ttu-id="12a55-1430">Para obtener información general de Windows sobre la compilación 14352, visita el [blog de Windows](https://aka.ms/wip14352).</span><span class="sxs-lookup"><span data-stu-id="12a55-1430">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="12a55-1431">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-1431">Fixed</span></span>
- <span data-ttu-id="12a55-1432">Se ha corregido un problema en el que los archivos grandes no se descargaban o se creaban correctamente.</span><span class="sxs-lookup"><span data-stu-id="12a55-1432">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="12a55-1433">Esto debe desbloquear npm y otros escenarios (GH 3, GH 313)</span><span class="sxs-lookup"><span data-stu-id="12a55-1433">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="12a55-1434">Se han quitado algunas instancias en las que los sockets se bloquean</span><span class="sxs-lookup"><span data-stu-id="12a55-1434">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="12a55-1435">Se han corregido algunos errores de ptrace</span><span class="sxs-lookup"><span data-stu-id="12a55-1435">Corrected some ptrace errors</span></span>
- <span data-ttu-id="12a55-1436">Se ha corregido un problema con WSL que permite nombres de archivo de más de 255 caracteres</span><span class="sxs-lookup"><span data-stu-id="12a55-1436">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="12a55-1437">Se ha mejorado la compatibilidad con caracteres distintos del inglés</span><span class="sxs-lookup"><span data-stu-id="12a55-1437">Improved support for non-English characters</span></span>
- <span data-ttu-id="12a55-1438">Agrega datos de zona horaria de Windows actuales y los establece como valores predeterminados</span><span class="sxs-lookup"><span data-stu-id="12a55-1438">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="12a55-1439">Id. de dispositivo único para cada punto de montaje (corrección de jre, GH 49)</span><span class="sxs-lookup"><span data-stu-id="12a55-1439">Unique device id’s for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="12a55-1440">Corrige el problema con rutas de acceso que contienen "."</span><span class="sxs-lookup"><span data-stu-id="12a55-1440">Correct issue with paths containing “.”</span></span> <span data-ttu-id="12a55-1441">y ".."</span><span class="sxs-lookup"><span data-stu-id="12a55-1441">and “..”</span></span>
- <span data-ttu-id="12a55-1442">Se ha agregado compatibilidad con Fifo (GH 71)</span><span class="sxs-lookup"><span data-stu-id="12a55-1442">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="12a55-1443">Se ha actualizado el formato de resolv.conf para que coincida con el formato nativo de Ubuntu</span><span class="sxs-lookup"><span data-stu-id="12a55-1443">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="12a55-1444">Algunas limpiezas de procfs</span><span class="sxs-lookup"><span data-stu-id="12a55-1444">Some procfs cleanup</span></span>
- <span data-ttu-id="12a55-1445">Se ha habilitado ping para consolas de administrador (GH 18)</span><span class="sxs-lookup"><span data-stu-id="12a55-1445">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="12a55-1446">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="12a55-1446">Syscall Support</span></span>
<span data-ttu-id="12a55-1447">A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="12a55-1447">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="12a55-1448">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="12a55-1448">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="12a55-1449">Compilación 14342</span><span class="sxs-lookup"><span data-stu-id="12a55-1449">Build 14342</span></span>
<span data-ttu-id="12a55-1450">Para obtener información general de Windows sobre la compilación 14342, visita el [blog de Windows](https://aka.ms/wip14342).</span><span class="sxs-lookup"><span data-stu-id="12a55-1450">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="12a55-1451">Puedes encontrar información sobre VolFs y DriveFs en el [blog de WSL](https://blogs.msdn.microsoft.com/wsl).</span><span class="sxs-lookup"><span data-stu-id="12a55-1451">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="12a55-1452">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-1452">Fixed</span></span>
- <span data-ttu-id="12a55-1453">Se ha corregido el problema de instalación cuando el usuario de Windows tenía caracteres Unicode en el nombre de usuario</span><span class="sxs-lookup"><span data-stu-id="12a55-1453">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="12a55-1454">La solución alternativa de apt-get update udev en las preguntas más frecuentes se proporciona ahora de forma predeterminada en la primera ejecución</span><span class="sxs-lookup"><span data-stu-id="12a55-1454">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="12a55-1455">Vínculos simbólicos habilitados en directorios DriveFs (/mnt/<drive>)</span><span class="sxs-lookup"><span data-stu-id="12a55-1455">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="12a55-1456">Los vínculos simbólicos ahora funcionan entre DriveFs y VolFs</span><span class="sxs-lookup"><span data-stu-id="12a55-1456">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="12a55-1457">Se ha solucionado el problema de análisis de ruta de acceso de nivel superior:ls .// funcionará ahora como se espera</span><span class="sxs-lookup"><span data-stu-id="12a55-1457">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="12a55-1458">La instalación de npm en DriveFs y las opciones -g ahora funcionan</span><span class="sxs-lookup"><span data-stu-id="12a55-1458">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="12a55-1459">Se ha corregido un problema que impedía que el servidor PHP se iniciara</span><span class="sxs-lookup"><span data-stu-id="12a55-1459">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="12a55-1460">Se han actualizado los valores de entorno predeterminados, como $PATH para que coincidan con Ubuntu nativo</span><span class="sxs-lookup"><span data-stu-id="12a55-1460">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="12a55-1461">Se ha agregado una tarea de mantenimiento semanal en Windows para actualizar la caché de paquetes apt</span><span class="sxs-lookup"><span data-stu-id="12a55-1461">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="12a55-1462">Se ha corregido un problema con la validación de encabezado de ELF, WSL ahora es compatible con todas las opciones de Melkor</span><span class="sxs-lookup"><span data-stu-id="12a55-1462">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="12a55-1463">El shell Zsh funciona</span><span class="sxs-lookup"><span data-stu-id="12a55-1463">Zsh shell is functional</span></span>
- <span data-ttu-id="12a55-1464">Ahora se admiten los binarios de Go precompilados</span><span class="sxs-lookup"><span data-stu-id="12a55-1464">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="12a55-1465">Indicar bash.exe en la primera ejecución ahora se localiza correctamente</span><span class="sxs-lookup"><span data-stu-id="12a55-1465">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="12a55-1466">/proc/meminfo ahora devuelve la información correcta</span><span class="sxs-lookup"><span data-stu-id="12a55-1466">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="12a55-1467">Ahora se admiten sockets en VFS</span><span class="sxs-lookup"><span data-stu-id="12a55-1467">Sockets now supported in VFS</span></span>
- <span data-ttu-id="12a55-1468">/dev ahora se monta como tempfs</span><span class="sxs-lookup"><span data-stu-id="12a55-1468">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="12a55-1469">Ahora se admite Fifo</span><span class="sxs-lookup"><span data-stu-id="12a55-1469">Fifo now supported</span></span>
- <span data-ttu-id="12a55-1470">Los sistemas de varios núcleos ahora se muestran correctamente en /proc/cpuinfo</span><span class="sxs-lookup"><span data-stu-id="12a55-1470">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="12a55-1471">Mejoras adicionales y mensajes de error que se descargan durante la primera ejecución</span><span class="sxs-lookup"><span data-stu-id="12a55-1471">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="12a55-1472">Mejoras de llamadas del sistema y corrección de errores.</span><span class="sxs-lookup"><span data-stu-id="12a55-1472">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="12a55-1473">Lista de llamadas del sistema admitidas a continuación.</span><span class="sxs-lookup"><span data-stu-id="12a55-1473">Supported syscall list below.</span></span>
- <span data-ttu-id="12a55-1474">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-1474">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="12a55-1475">Problemas conocidos</span><span class="sxs-lookup"><span data-stu-id="12a55-1475">Known Issues</span></span>
- <span data-ttu-id="12a55-1476">No se resuelve ".."</span><span class="sxs-lookup"><span data-stu-id="12a55-1476">Not resolving ‘..’</span></span> <span data-ttu-id="12a55-1477">correctamente en DriveFs en algunos casos</span><span class="sxs-lookup"><span data-stu-id="12a55-1477">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="12a55-1478">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="12a55-1478">Syscall Support</span></span>
<span data-ttu-id="12a55-1479">A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="12a55-1479">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="12a55-1480">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="12a55-1480">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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

## <a name="build-14332"></a><span data-ttu-id="12a55-1481">Compilación 14332</span><span class="sxs-lookup"><span data-stu-id="12a55-1481">Build 14332</span></span>

<span data-ttu-id="12a55-1482">Para obtener información general de Windows sobre la compilación 14332, visita el [blog de Windows](https://aka.ms/wip14332).</span><span class="sxs-lookup"><span data-stu-id="12a55-1482">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="12a55-1483">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-1483">Fixed</span></span>
- <span data-ttu-id="12a55-1484">Mejor generación de resolv.conf, incluida la priorización de entradas de DNS</span><span class="sxs-lookup"><span data-stu-id="12a55-1484">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="12a55-1485">Problema con el movimiento de archivos y directorios entre unidades /mnt y no /mnt</span><span class="sxs-lookup"><span data-stu-id="12a55-1485">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="12a55-1486">Los archivos tar ahora se pueden crear con vínculos simbólicos</span><span class="sxs-lookup"><span data-stu-id="12a55-1486">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="12a55-1487">Se ha agregado el directorio predeterminado /run/lock en la creación de instancias</span><span class="sxs-lookup"><span data-stu-id="12a55-1487">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="12a55-1488">Actualiza /dev/null para que devuelva la información de estadísticas correcta</span><span class="sxs-lookup"><span data-stu-id="12a55-1488">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="12a55-1489">Errores adicionales al descargar durante la primera ejecución</span><span class="sxs-lookup"><span data-stu-id="12a55-1489">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="12a55-1490">Mejoras de llamadas del sistema y corrección de errores.</span><span class="sxs-lookup"><span data-stu-id="12a55-1490">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="12a55-1491">Lista de llamadas del sistema admitidas a continuación.</span><span class="sxs-lookup"><span data-stu-id="12a55-1491">Supported syscall list below.</span></span>
- <span data-ttu-id="12a55-1492">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-1492">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="12a55-1493">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="12a55-1493">Syscall Support</span></span>
<span data-ttu-id="12a55-1494">A continuación se muestra la nueva llamada del sistema que tiene alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="12a55-1494">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="12a55-1495">La llamada del sistema de esta lista se admite en al menos un escenario, pero puede que no se admita todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="12a55-1495">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="12a55-1496">Compilación 14328</span><span class="sxs-lookup"><span data-stu-id="12a55-1496">Build 14328</span></span>

<span data-ttu-id="12a55-1497">Para obtener información general de Windows sobre la compilación 14332, visita el [blog de Windows](https://aka.ms/wip14328).</span><span class="sxs-lookup"><span data-stu-id="12a55-1497">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="12a55-1498">Nuevas características</span><span class="sxs-lookup"><span data-stu-id="12a55-1498">New Features</span></span>
* <span data-ttu-id="12a55-1499">Ahora admite usuarios de Linux.</span><span class="sxs-lookup"><span data-stu-id="12a55-1499">Now support Linux users.</span></span>  <span data-ttu-id="12a55-1500">Al instalar Bash en Ubuntu en Windows, se solicitará la creación de un usuario de Linux.</span><span class="sxs-lookup"><span data-stu-id="12a55-1500">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="12a55-1501">Para más información, visita https://aka.ms/wslusers.</span><span class="sxs-lookup"><span data-stu-id="12a55-1501">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="12a55-1502">El nombre de host ahora se establece en el nombre del equipo de Windows, ya no más en @localhost</span><span class="sxs-lookup"><span data-stu-id="12a55-1502">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="12a55-1503">Para más información sobre la compilación 14328, visita: https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="12a55-1503">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="12a55-1504">Fijo</span><span class="sxs-lookup"><span data-stu-id="12a55-1504">Fixed</span></span>
* <span data-ttu-id="12a55-1505">Mejoras de vínculos simbólicos para archivos que no son /mnt/<drive></span><span class="sxs-lookup"><span data-stu-id="12a55-1505">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="12a55-1506">La instalación de npm ahora funciona</span><span class="sxs-lookup"><span data-stu-id="12a55-1506">npm install now works</span></span>
    * <span data-ttu-id="12a55-1507">jdk / jre ahora se puede instalar con las instrucciones que se encuentran [aquí](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span><span class="sxs-lookup"><span data-stu-id="12a55-1507">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="12a55-1508">Problema conocido: los vínculos simbólicos no funcionan para los montajes de Windows.</span><span class="sxs-lookup"><span data-stu-id="12a55-1508">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="12a55-1509">La funcionalidad estará disponible en una compilación posterior</span><span class="sxs-lookup"><span data-stu-id="12a55-1509">Functionality will be available in a later build</span></span>
* <span data-ttu-id="12a55-1510">top y htop ahora se muestran</span><span class="sxs-lookup"><span data-stu-id="12a55-1510">top and htop now display</span></span>
* <span data-ttu-id="12a55-1511">Mensajes de error adicionales para algunos errores de instalación</span><span class="sxs-lookup"><span data-stu-id="12a55-1511">Additional error messages for some install failures</span></span>
* <span data-ttu-id="12a55-1512">Mejoras de llamadas del sistema y corrección de errores.</span><span class="sxs-lookup"><span data-stu-id="12a55-1512">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="12a55-1513">Lista de llamadas del sistema admitidas a continuación.</span><span class="sxs-lookup"><span data-stu-id="12a55-1513">Supported syscall list below.</span></span>
* <span data-ttu-id="12a55-1514">Correcciones de errores y mejoras adicionales</span><span class="sxs-lookup"><span data-stu-id="12a55-1514">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="12a55-1515">Compatibilidad con llamadas del sistema</span><span class="sxs-lookup"><span data-stu-id="12a55-1515">Syscall Support</span></span>
<span data-ttu-id="12a55-1516">A continuación hay una lista de llamadas del sistema que tienen alguna implementación en WSL.</span><span class="sxs-lookup"><span data-stu-id="12a55-1516">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="12a55-1517">Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.</span><span class="sxs-lookup"><span data-stu-id="12a55-1517">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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
