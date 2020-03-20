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
ms.openlocfilehash: 31bf975afb202a6cfd9a2879cff29a77b2969fce
ms.sourcegitcommit: 7069b8d452308c32cc7fa31d1158fcb130d42e06
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/01/2020
ms.locfileid: "76911709"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a>Notas de la versión del subsistema de Windows para Linux

## <a name="build-19555"></a>Compilación 19555
Para obtener información general de Windows sobre la compilación 19555, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2020/01/30/announcing-windows-10-insider-preview-build-19555/).

* [WSL2] Uso de un grupo de memoria para limitar la cantidad de memoria que usan las operaciones de instalación y conversión [GH 4669]
* Inclusión de wsl.exe cuando el componente opcional del Subsistema de Windows para Linux no esté habilitado para mejorar la detectabilidad de características.
* Cambio de wsl.exe para imprimir el texto de ayuda si el componente opcional WSL no está instalado
* Corrección de la condición de carrera al crear instancias
* Creación de un archivo wslclient.dll que contiene toda la funcionalidad de la línea de comandos
* Prevención de bloqueos durante la detención del servicio LxssManagerUser
* Corrección del error rápido de wslapi.dll cuando el parámetro distroName es NULL

## <a name="build-19041"></a>Compilación 19041
Para obtener información general de Windows sobre la compilación 19041, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/12/10/announcing-windows-10-insider-preview-build-19041/).

* [WSL2] Eliminación de la máscara de señal antes de iniciar los procesos
* [WSL2] Actualización del kernel de Linux a la versión 4.19.84
* Control de la creación de symlink /etc/resolv.conf cuando symlink no es relativo

## <a name="build-19028"></a>Compilación 19028
Para obtener información general de Windows sobre la compilación 19028, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/11/19/announcing-windows-10-insider-preview-build-19028/).

* [WSL2] Actualización del kernel de Linux a la versión 4.19.81.
* [WSL2] Cambiar el permiso predeterminado de/dev/net/tun a 0666 [GH 4629].
* [WSL2] Ajustar la cantidad predeterminada de memoria asignada a la VM de Linux para que el 80 % sea parte de la memoria del host.
* [WSL2] Corrección del servidor de interoperabilidad para controlar las solicitudes con tiempo de espera, para que los autores de llamadas incorrectas no puedan bloquear el servidor.

## <a name="build-19018"></a>Compilación 19018
Para obtener información general de Windows sobre la compilación 19018, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/11/05/announcing-windows-10-insider-preview-build-19018/).

* [WSL2] Uso de la caché = mmap como valor predeterminado para los montajes de 9p a fin de corregir las aplicaciones dotnet
* [WSL2] Correcciones para la retransmisión de localhost [GH 4340]
* [WSL2] Introducción de un montaje tmpfs compartido de distribución transversal para compartir el estado entre distribuciones
* Corrección de la restauración de la unidad de red persistente para \\\\wsl$

## <a name="build-19013"></a>Compilación 19013
Para obtener información general de Windows sobre la compilación 19013, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/10/29/announcing-windows-10-insider-preview-build-19013/).

* [WSL2] Mejora del rendimiento de memoria de la VM de la utilidad WSL. La memoria que ya no esté en uso se liberará de nuevo al host.
* [WSL2] Actualización de la versión del kernel a 4.19.79. (Adición de CONFIG_HIGH_RES_TIMERS, CONFIG_TASK_XACCT, CONFIG_TASK_IO_ACCOUNTING, CONFIG_SCHED_HRTICK y CONFIG_BRIDGE_VLAN_FILTERING).
* [WSL2] Corrección de la retransmisión de entrada para controlar los casos en los que stdin es un identificador de canalización que no está cerrado [GH 4424].
* Comprobación de que \\\\wsl$ no distingue mayúsculas de minúsculas.
```
[wsl2]
pageReporting = <bool>    # Enable or disable the free memory page reporting feature (default true).
idleThreshold = <integer> # Set the idle threshold for memory compaction, 0 disables the feature (default 1).
```

## <a name="build-19002"></a>Compilación 19002
Para obtener información general de Windows sobre la compilación 19002, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/10/17/announcing-windows-10-insider-preview-build-19002/).

* [WSL] Corrección de un problema con el control de algunos caracteres Unicode: https://github.com/microsoft/terminal/issues/2770
* [WSL] Corrección de casos poco frecuentes en los que se podría anular el registro de distribuciones si se iniciaban inmediatamente después de una actualización de una compilación a otra.
* [WSL] Corrección de un problema leve por el que wsl.exe se apagaba cuando no se cancelaban los temporizadores de inactividad de la instancia.

## <a name="build-18995"></a>Compilación 18995
Para obtener información general de Windows sobre la compilación 18995, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/).

* [WSL2] Corrección de un problema que provocaba que los montajes DrvFs dejaran de funcionar después de que se interrumpiera una operación (por ejemplo, Ctrl-C) [GH 4377]
* [WSL2] Corrección del control de mensajes hvsocket muy grandes [GH 4105]
* [WSL2] Corrección de un problema con la interoperabilidad cuando stdin es un archivo [GH 4475]
* [WSL2] Corrección de un bloqueo de servicio cuando se encontraba un estado de red inesperado [GH 4474]
* [WSL2] Consulta del nombre de distribución desde el servidor de interoperabilidad si el proceso actual no tiene la variable de entorno
* [WSL2] Corrección de un problema con la interoperabilidad cuando stdin es un archivo
* [WSL2] Actualización de la versión del kernel de Linux a 4.19.72
* [WSL2] Agrega la capacidad de especificar parámetros adicionales de línea de comandos de kernel mediante .wslconfig
```
[wsl2]
kernelCommandLine = <string> # Additional kernel command line arguments
```

## <a name="build-18990"></a>Compilación 18990
Para obtener información general de Windows sobre la compilación 18990, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/).

* Mejorar el rendimiento de los listados de directorios en \\\\wsl$
* [WSL2] Insertar entropía de arranque adicional [GH 4416]
* [WSL2] Corrección para la interoperabilidad de Windows al usar su/sudo [GH 4465]

## <a name="build-18980"></a>Compilación 18980
Para obtener información general de Windows sobre la compilación 18980, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).

* Corrige la lectura de los vínculos simbólicos que deniegan FILE_READ_DATA. Esto incluye todos los vínculos simbólicos que crea Windows para la compatibilidad con versiones anteriores, como "C:\Document and Settings" y un conjunto de vínculos simbólicos en el directorio de perfil del usuario.
* Hace que el estado inesperado del sistema de archivos no sea irrecuperable [GH 4334, 4305]
* [WSL2] Agrega compatibilidad para arm64 si tu CPU/firmware admite virtualización
* [WSL2] Permite a los usuarios sin privilegios ver el registro del kernel
* [WSL2] Corrige la retransmisión de salida cuando se han cerrado los sockets stdout/stderr [GH 4375]
* [WSL2] Compatibilidad con la batería y el adaptador de AC
* [WSL2] Actualización del kernel de Linux a 4.19.67
* Adición de la capacidad de establecer el nombre de usuario predeterminado en /etc/WSL.conf:
```
[user]
default=<string>
```

## <a name="build-18975"></a>Compilación 18975
Para obtener información general de Windows sobre la compilación 18975,visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).

* [WSL2] Se han corregido varios problemas de confiabilidad de localhost [GH 4340]

## <a name="build-18970"></a>Compilación 18970
Para obtener información general de Windows sobre la compilación 18970, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).

* [WSL2] Sincronización de la hora con la hora del host cuando el sistema se reanuda desde el estado de suspensión [GH 4245]
* [WSL2] Crea vínculos simbólicos de NT en volúmenes de Windows cuando sea posible.
* [WSL2] Crea distribuciones en los espacios de nombres UTS, IPC, PID y Mount.
* [WSL2] Corrección de retransmisión de puerto localhost cuando el servidor se enlaza a localhost directamente [GH 4353]
* [WSL2] Corrección de interoperabilidad cuando se redirige la salida [GH 4337]
* [WSL2] Compatibilidad con la traducción de vínculos simbólicos de NT absolutos.
* [WSL2] Actualización del kernel a 4.19.59
* [WSL2] Definición correcta de la máscara de subred para eth0.
* [WSL2] Cambio de la lógica para interrumpir el bucle de trabajo de la consola cuando se señale el evento de salida.
* [WSL2] Expulsión del VHD de distribución cuando la  distribución no está en ejecución.
* [WSL2] Corrección de la biblioteca de análisis de configuración para controlar correctamente los valores vacíos.
* [WSL2] Compatibilidad con el escritorio de Docker al crear montajes de distribución cruzados. Un distribución puede participar en este comportamiento si se agrega la siguiente línea al archivo /etc/wsl.conf:
```
[automount]
crossDistro = true
```

## <a name="build-18945"></a>Compilación 18945
Para obtener información general de Windows sobre la compilación 18945, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).

### <a name="wsl"></a>WSL
* [WSL2] Permite que se acceda a los sockets TCP de escucha en WSL2 desde el host mediante localhost:port
* [WSL2] Correcciones de errores de instalación/conversión y diagnósticos adicionales para un seguimiento de los problemas futuros [GH 4105] 
* [WSL2] Mejora la capacidad de diagnóstico de los problemas de red de WSL2
* [WSL2] Actualización de la versión del kernel a 4.19.55
* [WSL2] Actualización del kernel con las opciones de configuración necesarias para Docker [GH 4165]
* [WSL2] Aumento del número de CPU asignadas a la VM de utilidad ligera para que sea el mismo que el host (se ha limitado previamente a 8 por CONFIG_NR_CPUS en la configuración del kernel) [GH 4137]
* [WSL2] Creación de un archivo de intercambio para la VM ligera WSL2
* [WSL2] Permite que los montajes de usuarios sean visibles a través de la distribución \\\\wsl$\\ (por ejemplo, sshfs) [GH 4172]
* [WSL2] Mejora el rendimiento del sistema de archivos 9p
* [WSL2] Asegura que la ACL de VHD no crezca sin límite [GH 4126]
* [WSL2] Actualización de la configuración de kernel para admitir squashfs y xt_conntrack [GH 4107, 4123]
* [WSL2] Corrección para la opción interop.enabled /etc/wsl.conf [GH 4140]
* [WSL2] Devuelve ENOTSUP si el sistema de archivos no es compatible con EA
* [WSL2] Corrección de CopyFile colgado con \\\\wsl$
* Cambio del valor predeterminado de umask a 0022 y adición de la configuración de filesystem.umask a /etc/wsl.conf
* Corrección de wslpath para resolver correctamente los vínculos simbólicos, esto se retomó en 19h1 [GH 4078]
* Introducción del archivo %UserProfile%\\.wslconfig para ajustar la configuración de WSL2
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

## <a name="build-18917"></a>Compilación 18917
Para obtener información general de Windows sobre la compilación 18917, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).

### <a name="wsl"></a>WSL
* ¡WSL 2 ya está disponible! Consulta el [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) para más detalles.
* Corrección de una regresión en la que iniciar procesos de Windows a través de vínculos simbólicos no funcionaba correctamente [GH 3999]
* Agrega las opciones wsl.exe --list --verbose, wsl.exe --list --quiet y wsl.exe --import --version a wsl.exe
* Agrega la opción wsl.exe --shutdown
* Plan 9: Permite abrir un directorio para escribir en él correctamente

## <a name="build-18890"></a>Compilación 18890
Para obtener información general de Windows sobre la compilación 18890, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).

### <a name="wsl"></a>WSL
* Pérdida de socket sin bloqueo [GH 2913]
* La entrada de EOF en el terminal puede bloquear lecturas posteriores [GH 3421]
* Actualización del encabezado de resolv.conf para hacer referencia a wsl.conf [descrito en GH 3928]
* Interbloqueo en código de eliminación de epoll [GH 3922]
* Control de espacios de los argumentos en -import y -export [GH 3932]
* La extensión de los archivos de mmap no funciona correctamente [GH 3939]
* Corrección del problema de funcionamiento del acceso a ARM64 \\\\wsl$
* Agrega el mejor icono predeterminado para wsl.exe

## <a name="build-18342"></a>Compilación 18342
Para obtener información general de Windows sobre la compilación 18342, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).

### <a name="wsl"></a>WSL
* Hemos agregado la posibilidad de que los usuarios accedan a los archivos de Linux en una distribución de WSL desde Windows. Se puede acceder a estos archivos a través de la línea de comandos; también las aplicaciones de Windows, como el explorador de archivos, VSCode, etc., pueden interactuar con estos archivos. Para acceder a los archivos, ve a \\\\wsl$\\<nombre_de_distribución>, o consulta la lista de las distribuciones en ejecución en \\\\wsl$
* Agrega etiquetas de información de CPU adicionales y corregir valores de Cpus_allowed[_list] [GH 2234]
* Compatibilidad con exec desde un subproceso no líder [GH 3800]
* Trata errores de actualización de la configuración como no irrecuperables [GH 3785]
* Actualización de binfmt para administrar correctamente los desplazamientos [GH 3768]
* Habilita la asignación de unidades de red para Plan 9 [GH 3854]
* Compatibilidad con traducción de rutas de acceso Windows -> Linux y Linux -> Windows para montajes de enlace
* Crea secciones de solo lectura para asignaciones en archivos abiertos de solo lectura

## <a name="build-18334"></a>Compilación 18334
Para obtener información general de Windows sobre la compilación 18334, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).

### <a name="wsl"></a>WSL
* Rediseña el modo en que se asigna la zona horaria de Windows a una zona horaria de Linux [GH 3747]
* Corrección de pérdidas de memoria y adición de nuevas funciones de traducción de cadenas [GH 3746]
* SIGCONT en un grupo de subprocesos sin subprocesos es no-op [alvent 3741] 
* Muestra correctamente los descriptores de archivo de socket y epoll en /proc/self/fd

## <a name="build-18305"></a>Compilación 18305
Para obtener información general de Windows sobre la compilación 18305, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).

### <a name="wsl"></a>WSL
* pthreads pierden acceso a los archivos cuando sale el subproceso principal [GH 3589]
* TIOCSCTTY debe omitir el parámetro "force", a menos que sea necesario [GH 3652]
* Mejoras en la línea de comandos de wsl.exe y adición de la funcionalidad de importación y exportación.
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

## <a name="build-18277"></a>Compilación 18277
Para obtener información general de Windows sobre la compilación 18277, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).

### <a name="wsl"></a>WSL
* Corrección del error "Interfaz no compatible" que se presentó en la compilación 18272 [GH 3645]
* Omite la marca MNT_FORCE para la llamada del sistema umount [GH 3605]
* Cambia la interoperabilidad de WSL para usar la API de CreatePseudoConsole oficial
* No mantiene ningún valor de tiempo de espera cuando se reinicia FUTEX_WAIT

## <a name="build-18272"></a>Compilación 18272
Para obtener información general de Windows sobre la compilación 18272, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).

### <a name="wsl"></a>WSL
* **ADVERTENCIA:** Hay un problema en esta compilación que hace que WSL sea inoperable. Al intentar iniciar la distribución, verás el error "Interfaz no compatible". El problema se ha solucionado y estará en la compilación del modo anticipado de Insider de la próxima semana. Si has instalado esta compilación, puedes revertir a la compilación anterior de Windows mediante "Volver a la versión anterior de Windows 10" en Configuración-> Actualización y seguridad > Recuperación.

## <a name="build-18267"></a>Compilación 18267
Para obtener información general de Windows sobre la compilación 18267, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).

### <a name="wsl"></a>WSL
* Corrección del problema por el que un proceso inerte no podía recogerse y permanecía de manera indefinida.
* WslRegisterDistribution se bloquea si el mensaje de error supera la longitud máxima [GH 3592]
* Permite que fsync se complete correctamente para los archivos de solo lectura en DrvFs [GH 3556]
* Asegúrate de que los directorios /bin y /sbin existan antes de crear los vínculos simbólicos en ellos [GH 3584]
* Se agregó un mecanismo de tiempo de espera de finalización de instancias para las instancias de WSL. El tiempo de espera está establecido actualmente en 15 segundos, por lo que la instancia finalizará 15 segundos después de que termine el último proceso de WSL. Para finalizar una distribución de inmediato, usa:
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a>Compilación 17763 (1809)
Para obtener información general de Windows sobre la compilación 17763, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).

### <a name="wsl"></a>WSL
* Comprobación de permisos de la llamada del sistema setpriority demasiado estricta para cambiar la misma prioridad de subprocesos [GH 1838]
* Asegúrate de que se use el tiempo de interrupción no sesgado para el tiempo de arranque para evitar que se devuelvan valores negativos para clock_gettime (CLOCK_BOOTTIME) [GH 3434]
* Controla los vínculos simbólicos en el intérprete binfmt de WSL [GH 3424]
* Mejor control de la limpieza de descriptores de archivo del líder del grupo de subprocesos.
* Cambia WSL para usar KeQueryInterruptTimePrecise en lugar de KeQueryPerformanceCounter para evitar el desbordamiento [GH 3252]
* Ptrace attach puede producir un valor de devolución incorrecto de las llamadas del sistema [GH 1731]
* Corrección de varios problemas relacionados con AF_UNIX [GH 3371]
* Corrección del problema que podía provocar un error de interoperabilidad de WSL si el directorio de trabajo actual tiene menos de 5 caracteres de longitud [GH 3379]
* Evita las conexiones de bucle invertido con error con retraso de un segundo a puertos no existentes [GH 3286]
* Agrega el archivo de código auxiliar /proc/sys/fs/file-max [GH 2893]
* Información más precisa sobre el ámbito IPV6.
* Compatibilidad con PR_SET_PTRACER [GH 3053]
* El sistema de archivos de canalización borra accidentalmente el evento epoll desencadenado por el borde [GH 3276]
* El ejecutable de Win32 iniciado mediante el vínculo simbólico de NTFS no respeta el nombre del vínculo simbólico [GH 2909]
* Compatibilidad mejorada con zombie [GH 1353]
* Agrega entradas de wsl.conf para controlar el comportamiento de interoperabilidad de Windows [GH 1493]
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* La corrección para getsockname no siempre devuelve el tipo de familia de socket de UNIX [GH 1774]
* Agrega compatibilidad para TIOCSTI [GH 1863]
* Los sockets sin bloqueo en el proceso de conexión deben devolver EAGAIN para los intentos de escritura [GH 2846]
* Compatibilidad con la interoperabilidad en VHD montados [GH 3246, 3291]
* Corrección del problema de comprobación de permisos en la carpeta raíz [GH 3304]
* Compatibilidad limitada para los ioctl de teclado TTY KDGKBTYPE, KDGKBMODE y KDSKBMODE.
* Las aplicaciones de interfaz de usuario de Windows deben ejecutarse incluso cuando se inician en segundo plano.
* Agrega la opción wsl -u o --user [GH 1203]
* Corrección de problemas de inicio de WSL cuando el inicio rápido está habilitado [GH 2576]
* Los sockets de UNIX deben conservar las credenciales del mismo nivel desconectadas [GH 3183]
* Sockets de UNIX sin bloqueo con error de manera indefinida con EAGAIN [GH 3191]
* case=off es el nuevo tipo de montaje drvfs predeterminado [GH 2937, 3212, 3328]
    * Consulta el [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) para más información.
* Agrega wslconfig/terminate para detener las distribuciones en ejecución.
* Corrección del problema con las entradas del menú contextual del shell de WSL que no controlan correctamente las rutas de acceso con espacios.
* Expone la distinción de mayúsculas y minúsculas por directorio como atributo extendido
* ARM64: Emula las operaciones de mantenimiento de la memoria caché. Resuelve un [problema de dotnet](https://github.com/dotnet/core/issues/1561).
* DrvFs: solo caracteres con escape eliminado en el intervalo privado que corresponden a un carácter de escape.
* Corrección error de desviación por uno en la validación de longitud del intérprete del analizador ELF [GH 3154]
* Temporizadores absolutos de WSL con una hora en el pasado no se activan [GH 3091]
* Asegúrate de que los puntos de reanálisis recién creados se muestren como tales en el directorio principal.
* Crea de forma atómica directorios con distinción entre mayúsculas y minúsculas en DrvFs.
* Se ha corregido un problema adicional en el que las operaciones de varios subprocesos podían devolver ENOENT, aunque el archivo existiese. [GH 2712]
* Se corrigió un error de inicio de WSL cuando UMCI está habilitado. [GH 3020]
* Agrega el menú contextual del explorador para iniciar WSL [GH 437, 603, 1836]. Para usar, mantén presionada la tecla Mayús y haz clic con el botón derecho en una ventana del explorador.
* Corrección del comportamiento de no bloqueo de sockets de UNIX [GH 2822, 3100]
* Corrección del comando NETLINK que se bloquea, tal como se muestra en GH 2026.
* Agrega compatibilidad para las marcas de propagación de montaje [GH 2911].
* Corrección del problema de truncamiento que no provoca eventos inotify [GH 2978].
* Agrega la opción --exec a wsl.exe para invocar un solo binario sin un shell.
* Agrega la opción --distribution a wsl.exe para seleccionar una distribución específica.
* Compatibilidad limitada para dmesg. Ahora, las aplicaciones pueden registrarse en dmesg. El controlador WSL registra información limitada en dmesg. En el futuro, esto puede extenderse para llevar a cabo otros diagnósticos e información del controlador.
    * Nota: dmesg se admite actualmente a través de la interfaz de dispositivo `/dev/kmsg`. Aún no se admite la interfaz syscall `syslog`. Y, por lo tanto, algunas de las opciones de la línea de comandos de `dmesg`, como `-S` y `-C`, no funcionan.
* Cambia el gid y el modo de dispositivos serie predeterminados para que coincidan con los nativos [GH 3042]
* DrvFs ahora admite atributos extendidos.
    * Nota: DrvFs tiene algunas limitaciones en cuanto al nombre de los atributos extendidos. No se permiten algunos caracteres (como "/", ":" y "\*"), y los nombres de atributos extendidos no distinguen mayúsculas de minúsculas en DrvFs

## <a name="build-18252-skip-ahead"></a>Compilación 18252 (saltar)
Para obtener información general de Windows sobre la compilación 18252, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).

### <a name="wsl"></a>WSL
* Traslado de los binarios init y bsdtar fuera del archivo dll lxssmanager y a una carpeta de herramientas independiente
* Corrección de la carrera en torno al cierre del descriptor de archivo cuando se usa CLONE_FILES
* Controla campos opcionales en /proc/pid/mountinfo al traducir rutas de DrvFs
* Permite que DrvFs mknod se complete correctamente sin compatibilidad con metadatos para S_IFREG
* Los archivos de solo lectura creados en DrvFs deben tener el atributo readonly establecido [GH 3411]
* Agrega el asistente /sbin/mount.drvfs para controlar el montaje de DrvFs
* Usa el cambio de nombre de POSIX en DrvFs.
* Permite la traducción de rutas de acceso en volúmenes sin un GUID de volumen.

## <a name="build-17738-fast"></a>Compilación 17738 (rápida)
Para obtener información general de Windows sobre la compilación 17738, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).

### <a name="wsl"></a>WSL
* Comprobación de permisos de la llamada del sistema setpriority demasiado estricta para cambiar la misma prioridad de subprocesos [GH 1838]
* Asegúrate de que se use el tiempo de interrupción no sesgado para el tiempo de arranque para evitar que se devuelvan valores negativos para clock_gettime (CLOCK_BOOTTIME) [GH 3434]
* Controla los vínculos simbólicos en el intérprete binfmt de WSL [GH 3424]
* Mejor control de la limpieza de descriptores de archivo del líder del grupo de subprocesos.

## <a name="build-17728-fast"></a>Compilación 17728 (rápida)
Para obtener información general de Windows sobre la compilación 17728, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).

### <a name="wsl"></a>WSL
* Cambia WSL para usar KeQueryInterruptTimePrecise en lugar de KeQueryPerformanceCounter para evitar el desbordamiento [GH 3252]
* Ptrace attach puede producir un valor de devolución incorrecto de las llamadas del sistema [GH 1731]
* Corrección de varios problemas relacionados con AF_UNIX [GH 3371]
* Corrección del problema que podía provocar un error de interoperabilidad de WSL si el directorio de trabajo actual tiene menos de 5 caracteres de longitud [GH 3379]

## <a name="build-18204-skip-ahead"></a>Compilación 18204 (saltar)
Para obtener información general de Windows sobre la compilación 18204, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).

### <a name="wsl"></a>WSL
* El sistema de archivos de canalización borra accidentalmente el evento epoll desencadenado por el borde [GH 3276]
* El ejecutable de Win32 iniciado mediante el vínculo simbólico de NTFS no respeta el nombre del vínculo simbólico [GH 2909]

## <a name="build-17723-fast"></a>Compilación 17723 (rápida)
Para obtener información general de Windows sobre la compilación 17723, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).

### <a name="wsl"></a>WSL
* Evita las conexiones de bucle invertido con error con retraso de un segundo a puertos no existentes [GH 3286]
* Agrega el archivo de código auxiliar /proc/sys/fs/file-max [GH 2893]
* Información más precisa sobre el ámbito IPV6.
* Compatibilidad con PR_SET_PTRACER [GH 3053]
* El sistema de archivos de canalización borra accidentalmente el evento epoll desencadenado por el borde [GH 3276]
* El ejecutable de Win32 iniciado mediante el vínculo simbólico de NTFS no respeta el nombre del vínculo simbólico [GH 2909]

## <a name="build-17713"></a>Compilación 17713
Para obtener información general de Windows sobre la compilación 17713, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).

### <a name="wsl"></a>WSL
* Compatibilidad mejorada con zombie [GH 1353]
* Agrega entradas de wsl.conf para controlar el comportamiento de interoperabilidad de Windows [GH 1493]
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* La corrección para getsockname no siempre devuelve el tipo de familia de socket de UNIX [GH 1774]
* Agrega compatibilidad para TIOCSTI [GH 1863]
* Los sockets sin bloqueo en el proceso de conexión deben devolver EAGAIN para los intentos de escritura [GH 2846]
* Compatibilidad con la interoperabilidad en VHD montados [GH 3246, 3291]
* Corrección del problema de comprobación de permisos en la carpeta raíz [GH 3304]
* Compatibilidad limitada para los ioctl de teclado TTY KDGKBTYPE, KDGKBMODE y KDSKBMODE.
* Las aplicaciones de interfaz de usuario de Windows deben ejecutarse incluso cuando se inician en segundo plano.

## <a name="build-17704"></a>Compilación 17704
Para obtener información general de Windows sobre la compilación 17704, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).

### <a name="wsl"></a>WSL
* Agrega la opción wsl -u o --user [GH 1203]
* Corrección de problemas de inicio de WSL cuando el inicio rápido está habilitado [GH 2576]
* Los sockets de UNIX deben conservar las credenciales del mismo nivel desconectadas [GH 3183]
* Sockets de UNIX sin bloqueo con error de manera indefinida con EAGAIN [GH 3191]
* case=off es el nuevo tipo de montaje drvfs predeterminado [GH 2937, 3212, 3328]
    * Consulta el [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) para más información.
* Agrega wslconfig/terminate para detener las distribuciones en ejecución.

## <a name="build-17692"></a>Compilación 17692
Para obtener información general de Windows sobre la compilación 17692, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).

### <a name="wsl"></a>WSL
* Corrección del problema con las entradas del menú contextual del shell de WSL que no controlan correctamente las rutas de acceso con espacios.
* Expone la distinción de mayúsculas y minúsculas por directorio como atributo extendido
* ARM64: Emula las operaciones de mantenimiento de la memoria caché. Resuelve un [problema de dotnet](https://github.com/dotnet/core/issues/1561).
* DrvFs: solo caracteres con escape eliminado en el intervalo privado que corresponden a un carácter de escape.

## <a name="build-17686"></a>Compilación 17686
Para obtener información general de Windows sobre la compilación 17686, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).

### <a name="wsl"></a>WSL
* Corrección error de desviación por uno en la validación de longitud del intérprete del analizador ELF [GH 3154]
* Temporizadores absolutos de WSL con una hora en el pasado no se activan [GH 3091]
* Asegúrate de que los puntos de reanálisis recién creados se muestren como tales en el directorio principal.
* Crea de forma atómica directorios con distinción entre mayúsculas y minúsculas en DrvFs.

## <a name="build-17677"></a>Compilación 17677
Para obtener información general de Windows sobre la compilación 17677, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).

### <a name="wsl"></a>WSL
* Se ha corregido un problema adicional en el que las operaciones de varios subprocesos podían devolver ENOENT, aunque el archivo existiese. [GH 2712]
* Se corrigió un error de inicio de WSL cuando UMCI está habilitado. [GH 3020]

## <a name="build-17666"></a>Compilación 17666
Para obtener información general de Windows sobre la compilación 17666, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).

### <a name="wsl"></a>WSL
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a>ADVERTENCIA: Hay un problema que impide que WSL se ejecute en algunos conjuntos de chips AMD [GH 3134]. Hay una corrección lista y en camino en la rama de compilación de Insider.
* Agrega el menú contextual del explorador para iniciar WSL [GH 437, 603, 1836]. Para usar, mantén presionada la tecla Mayús y haz clic con el botón derecho en una ventana del explorador.
* Corrección del comportamiento de no bloqueo de sockets de Unix [GH 2822, 3100]
* Corrección del comando NETLINK que se bloquea, tal como se muestra en GH 2026.
* Agrega compatibilidad para las marcas de propagación de montaje [GH 2911].
* Corrección del problema de truncamiento que no provoca eventos inotify [GH 2978].
* Agrega la opción --exec a wsl.exe para invocar un solo binario sin un shell.
* Agrega la opción --distribution a wsl.exe para seleccionar una distribución específica.

## <a name="build-17655-skip-ahead"></a>Compilación 17655 (saltar)
Para obtener información general de Windows sobre la compilación 17655, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).

### <a name="wsl"></a>WSL
* Compatibilidad limitada para dmesg. Ahora, las aplicaciones pueden registrarse en dmesg. El controlador WSL registra información limitada en dmesg. En el futuro, esto puede extenderse para llevar a cabo otros diagnósticos e información del controlador.
    * Nota: dmesg se admite actualmente a través de la interfaz de dispositivo `/dev/kmsg`. Aún no se admite la interfaz sycall `syslog`. Y, por lo tanto, algunas de las opciones de la línea de comandos de `dmesg`, como `-S` y `-C`, no funcionan.
* Se ha corregido un problema en el que las operaciones de varios subprocesos podían devolver ENOENT, aunque el archivo existiese. [GH 2712]

## <a name="build-17639-skip-ahead"></a>Compilación 17639 (saltar)
Para obtener información general de Windows sobre la compilación 17639, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).

### <a name="wsl"></a>WSL
* Cambia el gid y el modo de dispositivos serie predeterminados para que coincidan con los nativos [GH 3042]
* DrvFs ahora admite atributos extendidos.
    * Nota: DrvFs tiene algunas limitaciones en cuanto al nombre de los atributos extendidos. En particular, no se permiten algunos caracteres (como "/", ":" y "\*"), y los nombres de atributos extendidos no distinguen mayúsculas de minúsculas en DrvFs

## <a name="build-17133-fast"></a>Compilación 17133 (rápida)
Para obtener información general de Windows sobre la compilación 17133, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).

### <a name="wsl"></a>WSL
* Corrección de un bloqueo en WSL. [GH 3039, 3034]

## <a name="build-17128-fast"></a>Compilación 17128 (rápida)
Para obtener información general de Windows sobre la compilación 17128, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).

### <a name="wsl"></a>WSL
* Ninguno

## <a name="build-17627-skip-ahead"></a>Compilación 17627 (saltar)
Para obtener información general de Windows sobre la compilación 17627, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).

### <a name="wsl"></a>WSL
* Agrega compatibilidad para las operaciones compatibles con pi de Futex. [GH 1006]
    * Ten en cuenta que las prioridades no son actualmente una característica admitida de WSL, por lo que hay limitaciones, pero el uso estándar debería estar desbloqueado.
* Compatibilidad con el Firewall de Windows para los procesos de WSL. [GH 1852]
    * Por ejemplo, para permitir que el proceso de Python de WSL escuche en cualquier puerto, use el cmd de Windows con privilegios elevados: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```
    * Para más información sobre cómo agregar reglas de firewall, consulte el [vínculo](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)
* Respeta el shell predeterminado del usuario al usar wsl.exe. [GH 2372]
* Informa de todas las interfaces de red como Ethernet. [GH 2996]
* Mejor control del archivo /etc/passwd dañado. [GH 3001]

### <a name="console"></a>Consola
* Sin correcciones.

### <a name="ltp-results"></a>Resultados de LTP:
Pruebas en curso.

## <a name="build-17618-skip-ahead"></a>Compilación 17618 (saltar)
Para obtener información general de Windows sobre la compilación 17618, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).

### <a name="wsl"></a>WSL
* Presenta la funcionalidad de pseudoconsola para la interoperabilidad de NT [GH 988, 1366, 1433, 1542, 2370, 2406].
* El mecanismo de instalación heredado (lxrun.exe) está en desuso. El mecanismo admitido para la instalación de distribuciones es a través de Microsoft Store.

### <a name="console"></a>Consola
* Sin correcciones.

### <a name="ltp-results"></a>Resultados de LTP:
Pruebas en curso.

## <a name="build-17110"></a>Compilación 17110
Para obtener información general de Windows sobre la compilación 17110, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).

### <a name="wsl"></a>WSL
* Permite que/init finalice desde Windows [GH 2928].
* DrvFs ahora usa la distinción de mayúsculas y minúsculas por directorio de manera predeterminada (equivalente a la opción de montaje "case=dir").
    * El uso de "case=force" (el comportamiento anterior) requiere el establecimiento de una clave del Registro. Ejecuta el siguiente comando para habilitar "case=force" si necesitas usarlo: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1
    * Si tienes directorios existentes creados con WSL en una versión anterior de Windows que deben distinguir entre mayúsculas y minúsculas, usa fsutil.exe para marcarlos con distinción de mayúsculas y minúsculas:fsutil.exe file setcasesensitiveinfo <path> enable
* La llamada del sistema uname devuelve cadenas de finalización NULL.

### <a name="console"></a>Consola
* Sin correcciones.

### <a name="ltp-results"></a>Resultados de LTP:
Pruebas en curso.

## <a name="build-17107"></a>Compilación 17107
Para obtener información general de Windows sobre la compilación 17107, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).

### <a name="wsl"></a>WSL
* Compatibilidad con TCSETSF y TCSETSW en los puntos de conexión de master pty [GH 2552].
* Iniciar procesos de interoperabilidad simultáneos puede dar lugar a EINVAL [GH 2813].
* Corrección de PTRACE_ATTACH para mostrar el estado de seguimiento adecuado en /proc/pid/status.
* Corrección de la carrera en la que los procesos de corta duración clonados con las marcas CLEARTID y SETTID podrían salir sin borrar la dirección de TID.
* Muestra un mensaje al actualizar los directorios del sistema de archivos de Linux al pasar de una compilación anterior a 17093. Para más detalles sobre los cambios del sistema de archivos de 17093, consulta las notas de la versión de [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).

### <a name="console"></a>Consola
* Sin correcciones.

### <a name="ltp-results"></a>Resultados de LTP:
Pruebas en curso.

## <a name="build-17101"></a>Compilación 17101
Para obtener información general de Windows sobre la compilación 17101, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).

### <a name="wsl"></a>WSL
* Compatibilidad con signalfd. [GH 129]
* Admite nombres de archivo que contienen caracteres NTFS no válidos mediante su codificación como caracteres Unicode privados. [GH 1514]
* El montaje automático se revertirá al modo de solo lectura cuando no se admita la escritura. [GH 2603]
* Permite pegar los pares suplentes Unicode (como los caracteres emoji). [GH 2765]
* Los pseudoarchivos en /proc y /sys deben devolver los valores read ready y write ready de select, poll, epoll, etc. [GH 2838]
* Corrección de un problema que podría hacer que el servicio pudiera entrar en un bucle infinito cuando el Registro se haya alterado o esté dañado.
* Corrección de los mensajes de netlink para trabajar con la versión más reciente (de nivel superior 4.14) de iproute2.

### <a name="console"></a>Consola
* Sin correcciones.

### <a name="ltp-results"></a>Resultados de LTP:
Pruebas en curso.

## <a name="build-17093"></a>Compilación 17093
Para obtener información general de Windows sobre la compilación 17093, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).

#### <a name="important"></a>Importante:
Al iniciar WSL por primera vez después de actualizar a esta compilación, tiene que hacer algún trabajo para actualizar los directorios del sistema de archivos de Linux. Esto puede tardar varios minutos, por lo que es posible que WSL se inicie lentamente. Esto solo debería ocurrir una vez por cada distribución que haya instalado desde Store.
* Compatibilidad mejorada de distinción de mayúsculas y minúsculas en DrvFs.
    * DrvFs admite ahora la distinción de mayúsculas y minúsculas por directorio. Se trata de una nueva marca que se puede establecer en los directorios para indicar que todas las operaciones de esos directorios deben tratarse como con distinción de mayúsculas y minúsculas, lo que permite que las aplicaciones de Windows abran correctamente archivos que solo difieren en mayúsculas y minúsculas.
    * DrvFs tiene nuevas opciones de montaje que controlan la distinción de mayúsculas y minúsculas por directorio.
        * case=force: todos los directorios se tratan con distinción de mayúsculas y minúsculas (excepto la raíz de la unidad). Los nuevos directorios creados con WSL se marcan con distinción de mayúsculas y minúsculas. Este es el comportamiento heredado, excepto para marcar los nuevos directorios que distinguen mayúsculas de minúsculas.
        * case=dir: solo los directorios con la marca de distinción de mayúsculas y minúsculas por directorio se tratan como que distinguen mayúsculas de minúsculas; los otros directorios no distinguen mayúsculas de minúsculas. Los nuevos directorios creados con WSL se marcan con distinción de mayúsculas y minúsculas.
        * case=off: solo los directorios con la marca de distinción de mayúsculas y minúsculas por directorio se tratan como que distinguen mayúsculas de minúsculas; los otros directorios no distinguen mayúsculas de minúsculas. Los nuevos directorios creados con WSL se marcan como sin distinción de mayúsculas y minúsculas.
    * Nota: Los directorios creados por WSL en versiones anteriores no tienen esta marca establecida, por lo que no se tratará como con distinción entre mayúsculas y minúsculas si usas la opción "case=dir". Próximamente se presentará una manera de establecer esta marca en los directorios existentes.
    * Ejemplo de montaje con estas opciones (en el caso de las unidades existentes, primero debes desmontar antes de poder montar con distintas opciones): sudo mount -t drvfs C: /mnt/c -o case=dir
    * Por ahora, case=force sigue siendo la opción predeterminada. Se cambiará a case=dir en el futuro.
* Ahora puedes usar barras diagonales en las rutas de acceso de Windows al montar DrvFs, por ejemplo: sudo mount -t drvfs //server/share /mnt/share
* WSL ahora procesa el archivo /etc/fstab durante el inicio de la instancia [GH 2636].
    * Esto se hace antes de montar automáticamente las unidades de DrvFs; las unidades que ya se hayan montado mediante fstab no se volverán a montar automáticamente, lo que te permite cambiar el punto de montaje para unidades específicas.
    * Este comportamiento se puede desactivar mediante wsl.conf.
* Los archivos mount, mountinfo y mountstats de /proc convierten correctamente en caracteres especiales, como barras diagonales inversas y espacios [GH 2799]
* Los archivos especiales creados con DrvFs, como los vínculos simbólicos de WSL, o fifos y sockets cuando los metadatos están habilitados, ahora se pueden copiar y mover desde Windows.

#### <a name="wsl-is-more-configurable-with-wslconf"></a>WSL es más configurable con wsl.conf
Hemos agregado un método para que configures automáticamente cierta funcionalidad en WSL que se aplicará cada vez que inicies el subsistema. Esto incluye opciones de montaje automático y configuración de red. Obtén más información en la publicación de blog en https://aka.ms/wslconf

#### <a name="af_unix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a>AF_UNIX permite conexiones de socket entre procesos de Linux en procesos nativos de WSL y Windows
Las aplicaciones de WSL y Windows ahora pueden comunicarse entre sí a través de sockets de Unix. Imagina que quieres ejecutar un servicio en Windows y hacer que esté disponible para las aplicaciones de WSL y Windows. Ahora, eso es posible con los sockets de Unix. Lee más en nuestra publicación de blog en https://aka.ms/afunixinterop

### <a name="wsl"></a>WSL
* Compatibilidad de mmap() con MAP_NORESERVE [GH 121, 2784]
* Compatibilidad con CLONE_PTRACE y CLONE_UNTRACED [GH 121, 2781]
* Controla la señal de terminación no SIGCHLD en el clon [GH 121, 2781]
* Código auxiliar /proc/sys/fs/inotify/max_user_instances y /proc/sys/fs/inotify/max_user_watches [GH 1705]
* Error al cargar binarios de ELF que contienen encabezados de carga con desplazamientos distintos de cero [GH 1884]
* Se eliminan los bytes de página finales al cargar imágenes.
* Reduce los casos en los que execve finaliza el proceso de forma silenciosa

### <a name="console"></a>Consola
* Sin correcciones.

### <a name="ltp-results"></a>Resultados de LTP:
Pruebas en curso.

## <a name="build-17083"></a>Compilación 17083
Para obtener información general de Windows sobre la compilación 17083, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).

### <a name="wsl"></a>WSL
* Se ha corregido la comprobación de errores relacionada con epoll [GH 2798, 2801, 2857]
* Se han corregido bloqueos al desactivar ASLR [GH 1185, 2870]
* Asegúrate de que las operaciones de mmap aparezcan como atómicas [GH 2732]

### <a name="console"></a>Consola
* Sin correcciones.

### <a name="ltp-results"></a>Resultados de LTP:
Pruebas en curso.

## <a name="build-17074"></a>Compilación 17074
Para obtener información general de Windows sobre la compilación 17074, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).

### <a name="wsl"></a>WSL
* Se ha corregido el formato de almacenamiento de los metadatos de DrvFs [GH 2777] </br>
**Importante:** Los metadatos de DrvFs creados antes de esta compilación no se mostrarán correctamente o no se mostrarán en absoluto. Para corregir los archivos afectados, usa chmod y chown para volver a aplicar los metadatos.
* Se ha corregido un problema con varias señales y llamadas del sistema reiniciables.

### <a name="console"></a>Consola
* Sin correcciones.

### <a name="ltp-results"></a>Resultados de LTP:
Pruebas en curso.

## <a name="build-17063"></a>Compilación 17063
Para obtener información general de Windows sobre la compilación 17063, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).

### <a name="wsl"></a>WSL
* DrvFs admite metadatos de Linux adicionales. Esto permite establecer el propietario y el modo de los archivos con chmod/chown, y también la creación de archivos especiales, como fifos, sockets de Unix y archivos de dispositivo. Esta opción está deshabilitada de forma predeterminada, ya que sigue siendo experimental.
**Nota:**  Se ha corregido un error en el formato de metadatos usado por DrvFs. Si bien los metadatos funcionan en esta compilación para experimentación, las compilaciones futuras no leerán correctamente los metadatos creados por esta compilación.  Es posible que tengas que actualizar manualmente el propietario de los archivos modificados, y se tendrán que volver a crear los dispositivos con un identificador de dispositivo personalizado.

  Para habilitar, monta DrvFs con la opción de metadatos (para habilitarlo en un montaje existente, primero debes desmontarlo):

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  Los permisos de Linux se agregan como metadatos adicionales al archivo; no afectan a los permisos de Windows.  Recuerda que la edición de un archivo mediante un editor de Windows puede quitar los metadatos. En este caso, el archivo volverá a sus permisos predeterminados.

* Se han agregado opciones de montaje a DrvFs para controlar archivos sin metadatos.
  * uid: el identificador de usuario que se usa para el propietario de todos los archivos.
  * gid: el identificador de grupo que se usa para el propietario de todos los archivos.
  * umask: máscara octal de permisos que se van a excluir para todos los archivos y directorios.
  * fmask: máscara octal de permisos que se van a excluir para todos los archivos normales.
  * dmask: máscara octal de permisos que se van a excluir para todos los directorios.

  Por ejemplo:
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  Combina con la opción de metadatos para especificar los permisos predeterminados para los archivos sin metadatos.

* Se presentó una nueva variable de entorno, `WSLENV`, para configurar cómo fluyen las variables de entorno entre WSL y Win32.

  Por ejemplo:

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  `WSLENV` es una lista de variables de entorno delimitadas por signos de dos puntos que se puede incluir al iniciar procesos de WSL desde Win32, o procesos de Win32 desde WSL.  Cada variable puede tener como sufijo una barra diagonal seguida de marcas para especificar cómo se va a traducir.
  * p: El valor es una ruta de acceso que se debe traducir entre las rutas de acceso de WSL y las rutas de acceso de Win32.
  * l: El valor es una lista de rutas de acceso. En WSL, se trata de una lista delimitada por signos de dos puntos. En Win32, se trata de una lista delimitada por punto y coma.
  * u: Solo se debe incluir el valor al invocar WSL desde Win32
  * w: Solo se debe incluir el valor al invocar Win32 desde WSL

  Puedes establecer `WSLENV` en. bashrc o en el entorno de Windows personalizado para el usuario.

* drvfs monta correctamente las marcas de tiempo de conservación desde tar, cp -p (GH 1939)
* Los vínculos simbólicos de drvfs informan el tamaño correcto (GH 2641)
* La lectura/escritura funciona para tamaños de E/S muy grandes (GH 2653)
* waitpid funciona con identificadores de grupo de procesos (GH 2534)
* Rendimiento de mmap significativamente mejorado para regiones de reserva grandes; mejora el rendimiento de ghc (GH 1671)
* Compatibilidad de personality con READ_IMPLIES_EXEC; corrige maxima y clisp (GH 1185)
* mprotect admite PROT_GROWSDOWN; corrige clisp (GH 1128)
* Correcciones de errores de página en modo de sobreconfirmación; corrige sbcl (GH 1128)
* clone admite más combinaciones de marcas
* Compatibilidad con select/epoll de archivos de epoll (antes de una no-op).
* Notifica a ptrace de llamadas del sistema sin implementar.
* Omite las interfaces que no están listas al generar los servidores de nombres resolv.conf [GH 2694]
* Enumera las interfaces de red sin dirección física. [GH 2685]
* Mejoras y correcciones de errores adicionales.

### <a name="linux-tools-available-to-developers-on-windows"></a>Herramientas de Linux disponibles para desarrolladores en Windows

* La cadena de herramientas de la línea de comandos de Windows incluye bsdtar (tar) y curl.
  Lee [este blog](https://aka.ms/tarcurlwindows) para más información acerca de cómo agregar estas dos nuevas herramientas y ver cómo dan forma a la experiencia de los desarrolladores en Windows.

*   `AF_UNIX` está disponible en el SDK de Windows Insider (17061+).
  Lee [este blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) para más información sobre `AF_UNIX` y cómo pueden usarlo los desarrolladores de Windows.

### <a name="console"></a>Consola
* Sin correcciones.

### <a name="ltp-results"></a>Resultados de LTP:
Pruebas en curso.


## <a name="build-17046"></a>Compilación 17046

Para obtener información general de Windows sobre la compilación 17046, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).

### <a name="fixed"></a>Fijo
#### <a name="wsl"></a>WSL
- Permite que los procesos se ejecuten sin un terminal activo. [GH 709, 1007, 1511, 2252, 2391, etc.]
- Mejor compatibilidad con CLONE_VFORK y CLONE_VM. [GH 1878, 2615]
- Omite los controladores de filtro TDI para las operaciones de red de WSL. [GH 1554]
- DrvFs crea vínculos simbólicos de NT cuando se cumplen determinadas condiciones. [GH 353, 1475, 2602]
    - El destino del vínculo debe ser relativo, no debe cruzar ningún punto de montaje ni vínculo simbólico, y debe existir.
    - El usuario debe tener SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (esto normalmente requiere que inicies wsl.exe con privilegios elevados), a menos que esté activado el modo de desarrollador.
    - En todas las demás situaciones, DrvFs todavía crea vínculos simbólicos de WSL.
- Permite ejecutar instancias de WSL con privilegios elevados y no elevados simultáneamente.
- Compatibilidad con /proc/sys/kernel/yama/ptrace_scope
- Agrega wslpath para realizar conversiones de rutas de acceso de WSL<->Windows. [GH 522, 1243, 1834, 2327, etc.]
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a>Consola
- Sin correcciones.

### <a name="ltp-results"></a>Resultados de LTP:
Pruebas en curso.


## <a name="build-17040"></a>Compilación 17040

Para obtener información general de Windows sobre la compilación 17040, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).<br/>


### <a name="fixed"></a>Fijo
#### <a name="wsl"></a>WSL
- No hay correcciones desde 17035.

#### <a name="console"></a>Consola
- No hay correcciones desde 17035.

### <a name="ltp-results"></a>Resultados de LTP:
Pruebas en curso.

## <a name="build-17035"></a>Compilación 17035

Para obtener información general de Windows sobre la compilación 17035, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).<br/>


### <a name="fixed"></a>Fijo
#### <a name="wsl"></a>WSL
- En ocasiones, el acceso a los archivos de DrvFs puede producir errores con EINVAL. [GH 2448]

#### <a name="console"></a>Consola
- Algo de pérdida de color al insertar o eliminar líneas en modo VT.

### <a name="ltp-results"></a>Resultados de LTP:
Pruebas en curso.

## <a name="build-17025"></a>Compilación 17025

Para obtener información general de Windows sobre la compilación 17025, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).<br/>


### <a name="fixed"></a>Fijo
#### <a name="wsl"></a>WSL
- Inicia procesos iniciales en un nuevo grupo de procesos en primer plano [GH 1653, 2510].
- Correcciones de entrega de SIGHUP [GH 2496].
- Genera un nombre de puente virtual predeterminado si no se proporciona ninguno [GH 2497].
- Implementa /proc/sys/kernel/random/boot_id [GH 2518].
- Más correcciones de la canalización stdout/stderr de interoperabilidad.
- Llamada del sistema syncfs de código auxiliar.

#### <a name="console"></a>Consola
- Corrección de la traducción de VT de entrada para consolas de terceros [GH 111]

### <a name="ltp-results"></a>Resultados de LTP:
Pruebas en curso.

## <a name="build-17017"></a>Compilación 17017

Para obtener información general de Windows sobre la compilación 17017, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).<br/>


### <a name="fixed"></a>Fijo
#### <a name="wsl"></a>WSL
- Omite los encabezados de programa ELF vacíos [GH 330].
- Permite que LxssManager cree instancias de WSL para usuarios no interactivos (compatibilidad con ssh y tareas programadas) [GH 777, 1602].
- Compatibilidad con escenarios de WSL->Win32->WSL ("inicio") [GH 1228].
- Compatibilidad limitada para la terminación de las aplicaciones de consola que se invocan a través de la interoperabilidad [GH 1614].
- Compatibilidad con las opciones de montaje para devpts [GH 1948].
- Inicio de bloqueo secundario de Ptrace [GH 2333].
- Faltan algunos eventos de EPOLLET [GH 2462].
- Devuelve más datos para PTRACE_GETSIGINFO.
- Getdents con lseek proporciona resultados incorrectos.
- Corrección de algunos bloqueos de la aplicación de interoperabilidad de Win32, en espera de la entrada en una canalización que no tiene más datos.
- Compatibilidad de O_ASYNC con archivos tty/pty.
- Mejoras y correcciones de errores adicionales

#### <a name="console"></a>Consola
- No hay cambios relacionados con la consola en esta versión.

### <a name="ltp-results"></a>Resultados de LTP:
Pruebas en curso.

## <a name="fall-creators-update"></a>Actualización Fall Creators Update

## <a name="build-16288"></a>Compilación 16288

Para obtener información general de Windows sobre la compilación 16288, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).<br/>


### <a name="fixed"></a>Fijo
#### <a name="wsl"></a>WSL
- Inicializa y notifica correctamente uid, gid y mode para los descriptores de archivo de socket [GH 2490]
- Mejoras y correcciones de errores adicionales

#### <a name="console"></a>Consola
- No hay cambios relacionados con la consola en esta versión.

### <a name="ltp-results"></a>Resultados de LTP:
Sin cambios desde 16273

## <a name="build-16278"></a>Compilación 16278

Para obtener información general de Windows sobre la compilación 162738, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).<br/>


### <a name="fixed"></a>Fijo
#### <a name="wsl"></a>WSL
- Anula explícitamente la asignación de las vistas asignadas de secciones basadas en archivos al anular el estado de LX MM [GH 2415]
- Mejoras y correcciones de errores adicionales

#### <a name="console"></a>Consola
- No hay cambios relacionados con la consola en esta versión.

### <a name="ltp-results"></a>Resultados de LTP:
Sin cambios desde 16273

## <a name="build-16275"></a>Compilación 16275

Para obtener información general de Windows sobre la compilación 162735, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).<br/>


### <a name="fixed"></a>Fijo
#### <a name="wsl"></a>WSL
- No hay cambios relacionados con WSL en esta versión.

#### <a name="console"></a>Consola
- No hay cambios relacionados con la consola en esta versión.

### <a name="ltp-results"></a>Resultados de LTP:
Sin cambios desde 16273

## <a name="build-16273"></a>Compilación 16273

Para obtener información general de Windows sobre la compilación 16273, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).<br/>


### <a name="fixed"></a>Fijo
#### <a name="wsl"></a>WSL
- Se ha corregido un problema por el que DrvFs a veces indicaba un tipo de archivo incorrecto para los directorios [GH 2392]
- Permite la creación de sockets NETLINK_KOBJECT_UEVENT para desbloquear programas que usan UEVENT [GH 1121, 2293, 2242, 2295, 2235, 648, 637]
- Agrega compatibilidad para conexión sin bloqueo [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]
- Implementa la marca de llamada del sistema de clon CLONE_FS [GH 2242]
- Corrección de problemas relativos a la falta de control de tabulaciones o comillas correctamente en la interoperabilidad de NT [GH 1625, 2164]
- Resuelve el error de acceso denegado al intentar volver a iniciar instancias de WSL [GH 651, 2095]
- Implementa las operaciones de Futex FUTEX_REQUEUE y FUTEX_CMP_REQUEUE [GH 2242]
- Corrección de permisos para varios archivos de SysFs [GH 2214]
- Corrección del bloqueo de pila de Haskell durante la instalación [GH 2290]
- Implementa las marcas binfmt_misc "C", "O" y "P" [GH 2103]
- Agrega /proc/sys/kernel /shmmax /shmmni y /threads-max [GH 1753]
- Agrega compatibilidad parcial para la llamada del sistema ioprio_set [GH 498]
- Código auxiliar SO_REUSEPORT y agrega compatibilidad para SO_PASSCRED para sockets de netlink [GH 69]
- Devuelve distintos códigos de error de RegisterDistribuiton si se está instalando o desinstalando actualmente una distribución.
- Permite la anulación del registro de distribuciones de WSL parcialmente instaladas a través de wslconfig.exe
- Corrección de bloqueo de prueba de socket de Python desde UDP::msg_peek
- Mejoras y correcciones de errores adicionales

#### <a name="console"></a>Consola
- No hay cambios relacionados con la consola en esta versión.

### <a name="ltp-results"></a>Resultados de LTP:
Total de pruebas: 1904<br/>
Total de pruebas omitidas: 209<br/>
Total de errores: 229<br/>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a>Compilación 16257

Para obtener información general de Windows sobre la compilación 16257, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).<br/>


### <a name="fixed"></a>Fijo
#### <a name="wsl"></a>WSL
- Implementa la llamada del sistema prlimit64
- Agrega compatibilidad con ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]
- Código auxiliar de MSG_MORE para sockets TCP [GH 2351]
- Corrección del comportamiento del vector auxiliar de AT_EXECFN no válido [GH 2133]
- Corrección del comportamiento de copiar y pegar para consola/tty, y agrega un mejor control de búfer completo [GH 2204, 2131]
- Establece AT_SECURE en vector auxiliar para los programas set-user-ID y set-group-ID [GH 2031]
- El punto de conexión maestro de psuedoterminal no controla TIOCPGRP [GH 1063]
- La corrección de lseek hace rebobinar directorios en LxFs [GH 2310]
- /dev/ptmx se bloquea después de un uso pesado [GH 1882]
- Mejoras y correcciones de errores adicionales

#### <a name="console"></a>Consola
- Corrección para líneas horizontales o guiones bajos en todas partes [GH 2168]
- Corrección para el orden de procesamiento cambiado hace que NPM sea más difícil de cerrar [GH 2170]
- Se ha agregado la nueva combinación de colores: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/

### <a name="ltp-results"></a>Resultados de LTP:
Sin cambios desde 16251

### <a name="syscall-support"></a>Compatibilidad con llamadas del sistema
A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL. Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.

`prlimit64`<br/>

### <a name="known-issues"></a>Problemas conocidos
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-"></a>[Problema de GitHub 2392: WSL no reconoce carpetas de Windows…](https://github.com/Microsoft/BashOnWindows/issues/2392)
En la compilación 16257, WSL tiene problemas al enumerar archivos o carpetas de Windows a través de `/mnt/c/...`.
Este problema se ha corregido y debe publicarse en la compilación de Insider durante la semana que comienza el 14/8/2017.

<br/>

## <a name="build-16251"></a>Compilación 16251

Para obtener información general de Windows sobre la compilación 16251, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).<br/>


### <a name="fixed"></a>Fijo
#### <a name="wsl"></a>WSL
- Quita la etiqueta beta del componente opcional de WSL, consulta la [publicación de blog](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) para más información.
- Inicializa correctamente el uid y gid del conjunto guardado para los archivos binarios set-user-ID y set-group-ID en ejecución [GH 962, 1415, 2072]
- Se ha agregado compatibilidad con ptrace PTRACE_O_TRACEEXIT [GH 555]
- Se ha agregado compatibilidad con ptrace PTRACE_GETFPREGS y PTRACE_GETREGSET con NT_FPREGSET [GH 555]
- Se ha corregido ptrace para que se detenga en las señales omitidas
- Mejoras y correcciones de errores adicionales

#### <a name="console"></a>Consola
- No hay cambios relacionados con la consola en esta versión.

### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 768</br>
Número de pruebas no superadas: 244</br>
Número de pruebas omitidas: 96</br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a>Compilación 16241

Para obtener información general de Windows sobre la compilación 16241, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).<br/>


### <a name="fixed"></a>Fijo
#### <a name="wsl"></a>WSL
- No hay cambios relacionados con WSL en esta versión.

#### <a name="console"></a>Consola
- Corrección para la generación de un carácter equivocado para DEC de líneas cruzadas, que se notificó originalmente [aquí](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)
- Corrección para cuando no se muestre texto de salida en la página de códigos 65001 (utf8)
- No transfieras los cambios hechos en los valores RGB de un color a otras partes de la paleta en el cambio de selección. Esto hará que la hoja de propiedades de la consola sea mucho más fácil de usar.
- Ctrl+S no parece funcionar correctamente
- Un-Bold/-Dim totalmente ausentes de los códigos de escape de ANSI [GH 2174]
- La consola no admite correctamente los temas de color VIM [GH 1706]
- No se pueden pegar caracteres determinados [GH 2149]
- El cambio de tamaño de reflujo interactúa de forma extraña con el cambio de tamaño de una ventana de Bash cuando el contenido está en la línea de comandos/edición [GH ConEmu 1123]
- Ctrl-L deja la pantalla desfasada [GH 1978]
- Error de representación de consola al mostrar VT en HDPI [GH 1907]
- Los caracteres Japansese parecen extraños con el carácter Unicode U+30FB [GH 2146]
- Mejoras y correcciones de errores adicionales

</br>

## <a name="build-16237"></a>Compilación 16237

Para obtener información general de Windows sobre la compilación 16237, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).<br/>


### <a name="fixed"></a>Fijo
- Usa atributos predeterminados para archivos sin EA en lxfs (root, root, 0000)
- Se ha agregado compatibilidad para distribuciones que usan atributos extendidos
- Corrección del relleno de las entradas devueltas por getdents y getdents64
- Corrección de la comprobación de permisos para la llamada del sistema shmctl SHM_STAT [GH 2068]
- Se ha corregido el estado inicial incorrecto de epoll para ttys [GH 2231]
- Corrección de readdir de DrvFs que no devuelve todas las entradas [GH 2077]
- Corrección de readdir de LxFs cuando los archivos están desvinculados [GH 2077]
- Permite que los archivos drvfs no vinculados se vuelvan a abrir a través de procfs
- Se ha agregado la invalidación de la clave del Registro global para deshabilitar las características de WSL (interoperabilidad/montaje de unidades)
- Corrección del recuento incorrecto de bloques en "stat" para DrvFs (y LxFs) [GH 1894]
- Mejoras y correcciones de errores adicionales

</br>

## <a name="build-16232"></a>Compilación 16232

Para obtener información general de Windows sobre la compilación 16232, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).<br/>


### <a name="fixed"></a>Fijo
- No hay cambios relacionados con WSL en esta versión.

</br>

## <a name="build-16226"></a>Compilación 16226

Para obtener información general de Windows sobre la compilación 16226, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).<br/>


### <a name="fixed"></a>Fijo
- Compatibilidad con llamadas del sistema relacionadas con xattr (getxattr, setxattr, listxattr, removexattr).
- Compatibilidad con security.capablity xattr.
- Compatibilidad mejorada con determinados sistemas de archivos y filtros, incluidos los servidores SMB que no son de MS. [GH 1952]
- Compatibilidad mejorada para los marcadores de posición de OneDrive, los marcadores de posición de GVFS y los archivos comprimidos del sistema operativo compacto.
- Mejoras y correcciones de errores adicionales

</br>

## <a name="build-16215"></a>Compilación 16215

Para obtener información general de Windows sobre la compilación 16215, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).<br/>


### <a name="fixed"></a>Fijo
- WSL ya no requiere el modo de desarrollador.
- Compatibilidad con uniones de directorios en drvfs.
- Controla la desinstalación de paquetes appx de distribución de WSL.
- Actualiza procfs para mostrar las asignaciones privadas y compartidas.
- Agrega la capacidad de wslconfig.exe de limpiar las distribuciones que están parcialmente instaladas o desinstaladas.
- Se ha agregado compatibilidad para IP_MTU_DISCOVER para sockets TCP. [GH 1639, 2115, 2205]
- Inferencia de la familia de protocolos para rutas a AF_INADDR.
- Mejoras en los dispositivos serie [GH 1929].

</br>

## <a name="build-16199"></a>Compilación 16199

Para obtener información general de Windows sobre la compilación 16199, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).<br/>


### <a name="fixed"></a>Fijo
- No hay cambios relacionados con WSL en estas versiones.

</br>

## <a name="build-16193"></a>Compilación 16193

Para obtener información general de Windows sobre la compilación 16193, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).<br/>


### <a name="fixed"></a>Fijo
- Condición de carrera entre el envío de SIGCONT y un grupo de subprocesos de terminación [GH 1973]
- Cambia dispositivos tty y pty para notificar FILE_DEVICE_NAMED_PIPE en lugar de FILE_DEVICE_CONSOLE [GH 1840]
- Corrección de SSH para IP_OPTIONS
- Se ha cambiado el montaje de DrvFs al demonio de inicialización [GH 1862, 1968, 1767, 1933]
- Se ha agregado compatibilidad en DrvFs para los siguientes vínculos simbólicos de NT.

</br>

## <a name="build-16184"></a>Compilación 16184

Para obtener información general de Windows sobre la compilación 16184, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).<br/>


### <a name="fixed"></a>Fijo
- Se ha quitado la tarea de mantenimiento de paquetes APT (lxrun.exe /update)
- Se ha corregido la salida que no se muestra en los procesos de Windows en node.js [GH 1840]
- Relaja los requisitos de alineación en lxcore [GH 1794]
- Se ha corregido el control de la marca AT_EMPTY_PATH en un número de llamadas del sistema.
- Se ha corregido el problema por el que la eliminación de archivos DrvFs con identificadores abiertos hace que el archivo muestre un comportamiento indefinido [GH 544, 966, 1357, 1535, 1615]
- /etc/hosts heredará ahora entradas del archivo de hosts de Windows (%windir%\system32\drivers\etc\hosts) [GH 1495]

</br>

## <a name="build-16179"></a>Compilación 16179

Para obtener información general de Windows sobre la compilación 16179, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).<br/>


### <a name="fixed"></a>Fijo
- Sin cambios en WSL esta semana.

</br>

## <a name="build-16176"></a>Compilación 16176

Para obtener información general de Windows sobre la compilación 16176, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).<br/>


### <a name="fixed"></a>Fijo

- [Se ha habilitado la compatibilidad serie](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- Se ha agregado la opción de socket de IP IP_OPTIONS [GH 1116]
- Se ha implementado la función pwritev (al cargar el archivo en nginx/PHP-FPM) [GH 1506]
- Se han agregado opciones de socket IP IP_MULTICAST_IF e IPV6_MULTICAST_IF [GH 990]
- Compatibilidad con la opción de socket IP_MULTICAST_LOOP e IPV6_MULTICAST_LOOP [GH 1678]
- Se ha agregado la opción de socket IP(V6)_MTU para el nodo de aplicaciones, traceroute, dig, nslookup, host
- Se ha agregado la opción de socket de IP IPV6_UNICAST_HOPS
- [Mejoras del sistema de archivos](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * Permite el montaje de rutas UNC
    * Habilita la compatibilidad con CDFS en drvfs
    * Controla correctamente los permisos para los sistemas de archivos de red en drvfs
    * Agrega compatibilidad para unidades remotas a drvfs
    * Habilita la compatibilidad con CDFS en drvfs
- Mejoras y correcciones adicionales

### <a name="ltp-results"></a>Resultados de LTP
Sin cambios desde 15042

</br>

## <a name="build-16170"></a>Compilación 16170

Para obtener información general de Windows sobre la compilación 16170, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).<br/>

Hemos lanzado una nueva [publicación de blog](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) en la que se describen nuestros esfuerzos para probar WSL.

### <a name="fixed"></a>Fijo

- Compatibilidad para la opción de socket IP_ADD_MEMBERSHIP y IPV6_ADD_MEMBERSHIP [GH 1678]
- Agrega compatibilidad para PTRACE_OLDSETOPTIONS. [GH 1692]
- Mejoras y correcciones adicionales

### <a name="ltp-results"></a>Resultados de LTP
Sin cambios desde 15042

</br>

## <a name="build-15046-to-windows-10-creators-update"></a>Compilación 15046 a Windows 10 Creators Update
No hay más correcciones o características de WSL planeadas para su inclusión en Windows 10 Creators Update. Las notas de la versión de WSL se reanudarán en las próximas semanas para las adiciones destinadas a la siguiente actualización principal de Windows. Para obtener información general de Windows sobre la compilación 15046 y futuras publicaciones de Insider, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/). <br/><br/>
 <br/>

## <a name="build-15042"></a>Compilación 15042

Para obtener información general de Windows sobre la compilación 15042, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).<br/>


### <a name="fixed"></a>Fijo

- Corrección para un interbloqueo al quitar una ruta de acceso que termina en ".."
- Se ha corregido un problema por el que FIONBIO no devuelve 0 en caso correcto [GH 1683]
- Se ha corregido un problema con lecturas de longitud cero de sockets de datagramas de inet
- Corrección del posible interbloqueo debido a la condición de carrera en la búsqueda de inode de drvfs [GH 1675]
- Se ha ampliado la compatibilidad con los datos suplementarios de los sockets de Unix; SCM_CREDENTIALS y SCM_RIGHTS [GH 514, 613, 1326]
- Mejoras y correcciones adicionales

### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 737</br>
Número de no superadas (error, omitidas, etc.): 255

</br>

## <a name="build-15031"></a>Compilación 15031

Para obtener información general de Windows sobre la compilación 15031, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).<br/>


### <a name="fixed"></a>Fijo

- Se ha corregido un error en el que el time(2) se comportaba incorrectamente de manera esporádica.
- Se ha corregido un problema donde las llamadas del sistema de *SIGPROCMASK podían dañar la máscara de señal.
- Ahora, devuelva la longitud completa de la línea de comandos en la notificación de creación del proceso de WSL. [GH 1632]
- WSL ahora informa de la salida del subproceso a través de ptrace para bloqueos de GDB. [GH 1196]
- Se ha corregido un error en el que ptys se bloqueaba después de una gran E/S de tmux [GH 1358]
- Se ha corregido la validación del tiempo de espera en muchas llamadas del sistema (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)
- Se ha agregado compatibilidad con eventfd EFD_SEMAPHORE [GH 452]
- Mejoras y correcciones adicionales

### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 737</br>
Número de no superadas (error, omitidas, etc.): 255 </br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a>Compilación 15025

Para obtener información general de Windows sobre la compilación 15025, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).<br/>


### <a name="fixed"></a>Fijo

- Corrección del error que dañó grep 2.27 [GH 1578]
- Se ha implementado la marca EFD_SEMAPHORE para la llamada del sistema eventfd2 [GH 452]
- Se ha implementado /proc/[pid]/net/ipv6_route [GH 1608]
- Compatibilidad de E/S controlada por señal para sockets de secuencia de Unix [GH 393, 68]
- Compatibilidad con F_GETPIPE_SZ y F_SETPIPE_SZ [GH 1012]
- Implementa la llamada del sistema recvmmsg() [GH 1531]
- Se ha corregido un error en el que epoll_wait() no esperaba [GH 1609]
- Implementa /proc/version_signature
- La llamada del sistema Tee ahora devuelve un error si ambos descriptores de archivo hacen referencia a la misma canalización
- Se ha implementado el comportamiento correcto de SO_PEERCRED para sockets de Unix
- Se ha corregido el control de parámetros no válidos de llamada del sistema tkill
- Cambios para aumentar el rendimiento de drvfs
- Corrección menor para el bloqueo de E/S de Ruby
- Se ha corregido recvmsg() que devuelve EINVAL para la marca MSG_DONTWAIT para sockets inet [GH 1296]
- Mejoras y correcciones adicionales

### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 732</br>
Número de no superadas (error, omitidas, etc.): 255 </br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a>Compilación 15019

Para obtener información general de Windows sobre la compilación 15019, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).<br/>


### <a name="fixed"></a>Fijo

- Se ha corregido un error que informaba incorrectamente del uso de CPU en procfs para herramientas como htop (GH 823, 945, 971)
- Al llamar a open() con O_TRUNC en un archivo existente inotify ahora genera IN_MODIFY antes de IN_OPEN
- Correcciones para el SO_ERROR de sockets de Unix getsockopt para habilitar postgress [GH 61, 1354]
- Implementa /proc/sys/net/core/somaxconn para el lenguaje GO
- La tarea en segundo plano de actualización del paquete apt-get ahora se ejecuta oculta de la vista
- Borra el ámbito de IPv6 localhost (error de Spring-Framework (Java)).
- Mejoras y correcciones adicionales

### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 714 </br>
Número de no superadas (error, omitidas, etc.): 249 </br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a>Compilación 15014

Para obtener información general de Windows sobre la compilación 15014, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).<br/>


### <a name="fixed"></a>Fijo

- Ctrl + C ahora funciona según lo previsto
- htop y ps auxw ahora muestran el uso de recursos correcto (GH 516)
- Traducción básica de excepciones de NT a señales. (GH 513)
- fallocate ahora genera el error ENOSPC cuando se está quedando sin espacio en lugar de EINVAL (GH 1571)
- Se ha agregado/proc/sys/kernel/sem.
- Se han implementado las llamadas del sistema semop y semtimedop
- Se han corregido errores de nslookup con la opción de socket IP_RECVTOS e IPV6_RECVTCLASS (GH 69)
- Compatibilidad con las opciones de socket IP_RECVTTL e IPV6_RECVHOPLIMIT
- Mejoras y correcciones adicionales

### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 709 </br>
Número de no superadas (error, omitidas, etc.): 255 </br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a>Resumen de llamadas del sistema
Total de llamadas del sistema: 384 </br>
Total implementado: 235 </br>
Total de procesos con stub: 22 </br>
Total no implementado: 127 </br>
[Desglose detallado](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a>Compilación 15007

Para obtener información general de Windows sobre la compilación 15007, visita el [blog de Windows]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).<br/>


### <a name="known-issue"></a>Problema conocido

- Hay un error conocido en el que la consola no reconoce algunas entradas Ctrl + <key>.  Esto incluye el comando Ctrl-C, que actuará como una presión normal de "c".

  - Solución: Asigna una tecla alternativa a Ctrl+C. Por ejemplo, para asignar Ctrl+K a Ctrl+C, haz lo siguiente: `stty intr \^k`.  Esta asignación es por terminal y tendrá que hacerse *cada* vez que se inicie Bash. Los usuarios pueden explorar la opción para incluirlo en su `.bashrc`

### <a name="fixed"></a>Fijo

- Se ha corregido el problema que hacía que la ejecución de WSL consumiera el 100 % de un núcleo de CPU.
- Ahora se admite la opción de socket IP_PKTINFO, IPV6_RECVPKTINFO. (GH 851, 987)
- Trunca la dirección física de la interfaz de red a 16 bytes en lxcore (GH 1452, 1414, 1343, 468, 308)
- Mejoras y correcciones adicionales

### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 709 </br>
Número de no superadas (error, omitidas, etc.): 255 </br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a>Compilación 15002

Para obtener información general de Windows sobre la compilación 15002, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).<br/>


### <a name="known-issue"></a>Problema conocido

Dos problemas conocidos:
- Hay un error conocido en el que la consola no reconoce algunas entradas Ctrl + <key>.  Esto incluye el comando Ctrl-C, que actuará como una presión normal de "c".

  - Solución: Asigna una tecla alternativa a Ctrl+C. Por ejemplo, para asignar Ctrl+K a Ctrl+C, haz lo siguiente: `stty intr \^k`.  Esta asignación es por terminal y tendrá que hacerse *cada* vez que se inicie Bash. Los usuarios pueden explorar la opción para incluirlo en su `.bashrc`

- Mientras se ejecuta WSL, un subproceso del sistema consumirá el 100 % de un núcleo de CPU.  La raíz de esto se ha solucionado y corregido internamente.

### <a name="fixed"></a>Fijo

- Todas las sesiones de Bash ahora deben crearse en el mismo nivel de permiso.  Se bloquearán los intentos de iniciar una sesión en un nivel diferente.  Esto significa que las consolas de administrador y que no son de administración no se pueden ejecutarse al mismo tiempo. (GH 626)
<br/>
- Se han implementado los siguientes mensajes NETLINK_ROUTE (requiere el administrador de Windows)
     - RTM_NEWADDR (admite `ip addr add`)
     - RTM_NEWROUTE (admite `ip route add`)
     - RTM_DELADDR (admite `ip addr del`)
     - RTM_DELROUTE (admite `ip route del`)
- La comprobación de tareas programadas para actualizar los paquetes ya no se ejecutará en una conexión de uso medido (GH 1371)
- Se ha corregido un error en el que la canalización se bloquea, es decir, bash -c "ls -alR /" | bash -c "cat" (GH 1214)
- Se ha implementado la opción de socket TCP_KEEPCNT (GH 843)
- Se ha implementado la opción de socket IP_MTU_DISCOVER INET (GH 720, 717, 170, 69)
- Se ha quitado la funcionalidad heredada para ejecutar archivos binarios de NT desde init con búsqueda de rutas de NT. (GH 1325)
- Corrección del modo de /dev/kmsg para permitir el acceso de lectura de grupo/otro (0644) (GH 1321)
- Se ha implementado /proc/sys/kernel/random/boot_id [GH 1092].
- Se ha corregido el error en el que la hora de inicio del proceso se mostraba como el año 2432 (GH 974)
- Se ha cambiado la variable de entorno TERM predeterminada a xterm-256color (GH 1446)
- Se ha modificado la forma en que se calcula la confirmación del proceso durante la bifurcación del proceso. (GH 1286)
- Se ha implementado /proc/sys/vm/overcommit_memory. (GH 1286)
- Se ha implementado el archivo /proc/net/route (GH 69)
- Se ha corregido el error en el que el nombre de acceso directo se localizaba incorrectamente (GH 696)
- Se ha corregido la lógica de análisis de elf que valida incorrectamente los encabezados de programa debe ser menor que (o igual a) PATH_MAX. (GH 1048)
- Se ha implementado la devolución de llamada de statfs para procfs, sysfs, cgroupfs y binfmtfs (GH 1378)
- Se han corregido ventanas de AptPackageIndexUpdate que no se cierran (GH 1184, también se describe en GH 1193).
- Se ha agregado compatibilidad con la personalidad de ASLR ADDR_NO_RANDOMIZE. (GH 1148, 1128)
- Se han mejorado PTRACE_GETSIGINFO, SIGSEGV para los seguimientos de la pila gdb adecuados durante AV (GH 875)
- Ya no se produce un error en el análisis de elf para los archivos binarios de patchelf. (GH 471)
- DNS de VPN propagado a/etc/resolv.conf (GH 416, 1350)
- Mejoras en el cierre de TCP para la transferencia de datos más confiable. (GH 610, 616, 1025, 1335)
- Ahora devuelve el código de error correcto cuando se abran demasiados archivos (EMFILE). (GH 1126, 2090)
- El registro de auditoría de Windows ahora informa el nombre de la imagen en la creación del proceso de auditoría.
- Ahora se producen errores leves al iniciar bash.exe desde una ventana de Bash
- Se ha agregado un mensaje de error cuando interop no puede acceder a un directorio de trabajo en LxFs (es decir, notepad.exe .bashrc)
- Se ha corregido un problema en el que la ruta de acceso de Windows se truncaba en WSL
- Mejoras y correcciones adicionales

### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 690 </br>
Número de no superadas (error, omitidas, etc.): 274 </br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a>Compatibilidad con llamadas del sistema
A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL. Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a>Compilación 14986

Para obtener información general de Windows sobre la compilación 14986, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).<br/>


### <a name="fixed"></a>Fijo

- Se han corregido comprobaciones de error con IOCTL de NetLink y Pty
- La versión del kernel ahora informa 4.4.0-43 por coherencia con Xenial
- Bash.exe ahora se inicia cuando la entrada se dirige a "nul" (GH 1259)
- Los identificadores de subproceso ahora se han declarado correctamente en procfs (GH 967)
- Las marcas IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR ahora se admiten en inotify_add_watch() (GH 1280)
- Implementa timer_create y llamadas del sistema relacionadas.  Esto habilita la compatibilidad con GHC (GH 307)
- Se ha corregido un problema en el que ping devolvía una hora de 0,000 ms (GH 1296)
- Devuelve el código de error correcto cuando se abran demasiados archivos.
- Se ha corregido un problema en WSL donde la solicitud de NetLink de datos de la interfaz de red generaba un error con EINVAL si la dirección de hardware de la interfaz es de 32 bytes (por ejemplo, la interfaz Teredo)
   - Ten en cuenta que la utilidad "ip" de Linux contiene un error en el que se bloqueará si WSL informa de una dirección de hardware de 32 bytes. Se trata de un error en "ip", no en WSL. La utilidad "ip" codifica de forma rígida la longitud del búfer de cadena usado para imprimir la dirección de hardware, y el búfer es demasiado pequeño para imprimir una dirección de hardware de 32 bytes.
- Mejoras y correcciones adicionales

### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 669 </br>
Número de no superadas (error, omitidas, etc.): 258 </br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a>Compatibilidad con llamadas del sistema
A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL. Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a>Compilación 14971

Para obtener información general de Windows sobre la compilación 14971, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).<br/>


### <a name="fixed"></a>Fijo

 - Debido a circunstancias más allá de nuestro control, no hay ninguna actualización en esta compilación para el subsistema de Windows para Linux.  Las actualizaciones programadas regularmente se reanudarán en la próxima versión.

### <a name="ltp-results"></a>Resultados de LTP:
Sin cambios desde 14965 </br>
Número de pruebas superadas: 664 </br>
Número de no superadas (error, omitidas, etc.): 263 </br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a>Compilación 14965

Para obtener información general de Windows sobre la compilación 14965, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).<br/>


### <a name="fixed"></a>Fijo

- Compatibilidad con RTM_GETLINK y RTM_GETADDR del protocolo NETLINK_ROUTE de sockets de Netlink (GH 468)
  - Habilita los comandos ifconfig e ip para la enumeración de red
  - Puede encontrar más información en la [publicación de blog sobre redes WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).

- /sbin está ahora en la ruta de acceso del usuario de manera predeterminada
- La ruta de acceso de usuario de NT ahora se anexa a la ruta de acceso de WSL de manera predeterminada (es decir, ahora puedes escribir notepad.exe sin agregar System32 a la ruta de acceso de Linux)
- Se ha agregado compatibilidad para /proc/sys/kernel/cap_last_cap
- Los archivos binarios de NT ahora se pueden iniciar desde WSL cuando el directorio de trabajo actual contiene caracteres que no son ANSI (GH 1254)
- Permite el apagado en el socket de flujo Unix desconectado.
- Se ha agregado compatibilidad para PR_GET_PDEATHSIG.
- Se ha agregado compatibilidad para CLONE_PARENT
- Se ha corregido un error en el que la canalización se bloquea, es decir, bash -c "ls -alR /" | bash -c "cat" (GH 1214)
- Controla las solicitudes para conectarse al terminal actual.
- Marca /proc/<pid>/oom_score_adj como grabable.
- Agrega la carpeta/sys/fs/cgroup.
- sched_setaffinity debe devolver el número de máscara de bits de afinidad
- Corrige la lógica de validación de ELF que presupone incorrectamente que las rutas de intérprete deben tener menos de 64 caracteres de longitud. (GH 743)
- Los descriptores de archivos abiertos pueden mantener abierta la ventana de la consola (GH 1187)
- Se ha corregido el error en el que no se podía completar rename() con la barra diagonal final en el nombre de destino (GH 1008)
- Implementa el archivo /proc/net/dev
- Se han corregido los pings de 0,000 ms debido a la resolución del temporizador.
- Se ha implementado /proc/self/environ (GH 730)
- Correcciones de errores y mejoras adicionales

### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 664 </br>
Número de no superadas (error, omitidas, etc.): 263 </br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a>Compilación 14959

Para obtener información general de Windows sobre la compilación 14959, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).<br/>


### <a name="fixed"></a>Fijo

- Se ha mejorado la notificación del proceso PICO para Windows.  Encuentra información adicional en el [blog de WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).
- Se ha mejorado la estabilidad de interoperabilidad con Windows
- Se ha corregido el error 0x80070057 al iniciar bash.exe cuando Protección de datos de empresa (EDP) está habilitado
- Correcciones de errores y mejoras adicionales

### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 665 </br>
Número de no superadas (error, omitidas, etc.): 263 </br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a>Compilación 14955

Para obtener información general de Windows sobre la compilación 14955, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).<br/>


### <a name="fixed"></a>Fijo

 - Debido a circunstancias más allá de nuestro control, no hay ninguna actualización en esta compilación para el subsistema de Windows para Linux.  Las actualizaciones programadas regularmente se reanudarán en la próxima versión.

### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 665 </br>
Número de no superadas (error, omitidas, etc.): 263 </br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a>Compilación 14951

Para obtener información general de Windows sobre la compilación 14951, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).<br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a>Nueva característica: Interoperabilidad de Windows/Ubuntu
Ahora se pueden invocar archivos binarios de Windows directamente desde la línea de comandos de WSL.  Esto da a los usuarios la capacidad de interactuar con el entorno y el sistema Windows de una manera que antes no era posible.  Como ejemplo rápido, ahora es posible que los usuarios ejecuten los siguientes comandos:

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

Puedes encontrar más información en:

- [Blog del equipo de WSL para Interop](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [Documentación de interoperabilidad de MSDN](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a>Fijo

- Ubuntu 16.04 (Xenial) ahora se instala para todas las instancias nuevas de WSL.  Los usuarios con instancias existentes de 14.04 (Trusty) no se actualizarán automáticamente.
- Ahora se muestra la configuración regional establecida durante la instalación
- Mejoras del terminal, que incluido un error en el que la redirección de un proceso de WSL a un archivo no siempre funciona
- La duración de la consola debe estar asociada a la duración de bash.exe
- El tamaño de la ventana de la consola debe usar un tamaño visible, no el tamaño del búfer
- Correcciones de errores y mejoras adicionales

### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 665 </br>
Número de no superadas (error, omitidas, etc.): 263 </br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a>Compilación 14946

Para obtener información general de Windows sobre la compilación 14946, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).<br/>


### <a name="fixed"></a>Fijo

- Se ha corregido un problema que impedía la creación de cuentas de usuario de WSL para los usuarios con nombres de usuario de NT que contienen espacios o comillas. 
- Cambia VolFs y DrvFs para que devuelvan 0 para el recuento de vínculos de directorio en stat
- Compatibilidad con la opción de socket IPV6_MULTICAST_HOPS.
- Limite a un único bucle de E/S de la consola por tty. Por ejemplo, el comando siguiente es posible:
  - bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"

- Reemplaza espacios con tabulaciones en/proc/cpuinfo (GH 1115)
- DrvFs aparece ahora en mountinfo con un nombre que coincide con el volumen de Windows montado
- /home y /root ahora aparecen en mountinfo con los nombres correctos
- Correcciones de errores y mejoras adicionales

### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 665 </br>
Número de no superadas (error, omitidas, etc.): 263 </br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a>Compilación 14942

Para obtener información general de Windows sobre la compilación 14942, visita el [blog de Windows](https://aka.ms/onefourninefourtwoooooo).<br/>


### <a name="fixed"></a>Fijo

- Un número de comprobaciones de error direccionadas, incluido el bloqueo de red "ATTEMPTED EXECUTE OF NOEXECUTE MEMORY" que bloqueaba SSH
- Ahora se incluye la compatibilidad de inotifiy con las notificaciones generadas desde aplicaciones Windows en DrvFs
- Implementa TCP_KEEPIDLE y TCP_KEEPINTVL para mongod. (GH 695)
- Implementa la llamada del sistema pivot_root
- Implementa la opción de socket para SO_DONTROUTE
- Correcciones de errores y mejoras adicionales


### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 665 </br>
Número de no superadas (error, omitidas, etc.): 263 </br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a>Compatibilidad con llamadas del sistema
A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL. Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a>Compilación 14936

Para obtener información general de Windows sobre la compilación 14936, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).<br/>


Nota: WSL instalará Ubuntu versión 16.04 (Xenial) en lugar de Ubuntu 14.04 (Trusty) en una próxima versión.  Este cambio se aplicará a los usuarios de Insider que instalen nuevas instancias (lxrun.exe /install o a la primera ejecución de bash.exe).  Las instancias existentes con Trusty no se actualizarán automáticamente. Los usuarios pueden actualizar su imagen de Trusty a Xenial con el comando do-release-upgrade.

### <a name="known-issue"></a>Problema conocido
WSL está experimentando un problema con algunas implementaciones de sockets.  La comprobación de errores se manifiesta como bloqueo con el error "ATTEMPTED EXECUTE OF NOEXECUTE MEMORY".  La manifestación más común de este problema es un bloqueo cuando se usa ssh.  La causa principal se ha corregido en las compilaciones internas y se enviará a los usuarios de Insider lo antes posible.

### <a name="fixed"></a>Fijo

- Se ha implementado la llamada del sistema chroot
- Mejoras en inotify, ~~incluida la compatibilidad con las notificaciones generadas desde aplicaciones Windows en DrvFs~~
  - Corrección: La compatibilidad de inotify con los cambios que se originan en aplicaciones Windows no está disponible en este momento.
- El enlace de sockets a IPV6::<port n> ahora admite IPV6_V6ONLY (GH 68, 157, 393, 460, 674, 740, 982, 996)
- Se ha implementado el comportamiento de WNOWAIT para la llamada del sistema waitid (GH 638)
- Compatibilidad con las opciones de socket de IP IP_HDRINCL e IP_TTL
- read() de longitud cero debe volver inmediatamente (GH 975)
- Controla correctamente los nombres de archivo y los prefijos de nombre de archivo que no incluyen un terminador NULL en un archivo .tar.
- Compatibilidad de epoll para /dev/null
- Corrección del origen de hora de /dev/alarm
- bash -c ahora puede redirigir a un archivo
- Correcciones de errores y mejoras adicionales

### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 664 </br>
Número de no superadas (error, omitidas, etc.): 264 </br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a>Compatibilidad con llamadas del sistema
A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL. Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.

`chroot`<br/>
<br/>

## <a name="build-14931"></a>Compilación 14931

Para obtener información general de Windows sobre la compilación 14931, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).<br/>


### <a name="fixed"></a>Fijo

 - Debido a circunstancias más allá de nuestro control, no hay ninguna actualización en esta compilación para el subsistema de Windows para Linux.  Las actualizaciones programadas regularmente se reanudarán en la próxima versión.

<br/>

## <a name="build-14926"></a>Compilación 14926

Para obtener información general de Windows sobre la compilación 14926, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).<br/>


### <a name="fixed"></a>Fijo

- Ping ahora funciona en consolas que no tienen privilegios de administrador
- Ahora también se admite Ping6, sin privilegios de administrador.
- Compatibilidad de inotify con archivos modificados a través de WSL. (GH 216)
  - Marcas admitidas:
    - inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK
    - Eventos de inotify_add_watch: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF
    - Atributos de inotify_add_watch: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR
    - Salida de lectura: LX_IN_ISDIR, LX_IN_IGNORED
  - Problema conocido: La modificación de archivos desde aplicaciones de Windows no genera ningún evento
- El socket de Unix ahora es compatible con SCM_CREDENTIALS

### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 651 </br>
Número de no superadas (error, omitidas, etc.): 258 </br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a>Compilación 14915

Para obtener información general de Windows sobre la compilación 14915, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).<br/>


### <a name="fixed"></a>Fijo
-  Socketpair para sockets de datagramas de Unix (GH 262)
- Compatibilidad con el socket de Unix para SO_REUSEADDR
- Compatibilidad con el socket de Unix para SO_BROADCAST (GH 568)
- Compatibilidad con el socket de Unix para SOCK_SEQPACKET (GH 758, 546)
- Adición de compatibilidad para socket de datagramas de Unix send, recv y shutdown
- Corrección de comprobación de errores debido a la validación de parámetros mmap no válida para direcciones no fijas. (GH 847)
- Compatibilidad para suspender o reanudar los estados del terminal
- Compatibilidad para TIOCPKT ioctl para desbloquear la utilidad de pantalla (GH 774)
    - Problema conocido: Las teclas de función no funcionan
- Se ha corregido una carrera en TimerFd que podía hacer que LxpTimerFdWorkerRoutine accediera a un miembro liberado "ReaderReady" (GH 814)
- Habilita la compatibilidad con llamadas del sistema reiniciables para futex, poll y clock_nanosleep
- Se ha agregado compatibilidad con montaje de enlace
- Compatibilidad para dejar de compartir el espacio de nombres de montaje
    - Problema conocido: Al crear un nuevo espacio de nombres de montaje con `unshare(CLONE_NEWNS)`, el directorio de trabajo actual continuará señalando al espacio de nombres anterior
- Mejoras y correcciones de errores adicionales

<br/>

## <a name="build-14905"></a>Compilación 14905

Para obtener información general de Windows sobre la compilación 14905, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).<br/>


### <a name="fixed"></a>Fijo
- Ahora se admiten llamadas del sistema reiniciables (GH 349, GH 520)
- Los vínculos simbólicos a directorios que terminan en / ahora están operativos (GH 650)
- Se ha implementado RNDGETENTCNT ioctl para /dev/random
- Se han implementado los archivos /proc/[pid]/mounts, /proc/[pid]/mountinfo y /proc/[pid]/mountstats
- Correcciones de errores y mejoras adicionales

</br>

## <a name="build-14901"></a>Compilación 14901
Primera compilación de Insider para la versión posterior a la Actualización de aniversario de Windows 10.

Para obtener información general de Windows sobre la compilación 14901, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).<br/>


### <a name="fixed"></a>Fijo
- Se ha corregido un problema de barra diagonal final
    - Ahora funcionan los comandos como `$ mv a/c/ a/b/`
- Al instalar ahora se pregunta si la configuración regional de Ubuntu debe establecerse en la configuración regional de Windows
- Compatibilidad de procfs para la carpeta ns
- Se ha agregado mount y unmount para los sistemas de archivos tmpfs, procfs y sysfs
- Corrección de la firma ABI mknod[at] de 32 bits
- Los sockets de Unix se movieron al modelo dispatch
- Se debe respetar el tamaño del búfer de recepción del socket de INET mediante setsockopt
- Implementa la marca de mensaje de recepción de socket de Unix MSG_CMSG_CLOEXEC
- Redirección de canalización stdin/stdout de proceso de Linux (GH 2)
    - Permite la canalización de comandos bash -c en CMD.  Ejemplo:  >dir | bash -c "grep foo"
- Bash ahora se puede instalar en sistemas con varios archivos de página (GH 538, 358)
- El tamaño predeterminado del búfer del socket de INET debe coincidir con el de la configuración predeterminada de Ubuntu
- Alinea las llamadas del sistema xattr con listxattr
- Solo se devuelven interfaces con una dirección IPv4 válida de SIOCGIFCONF
- Corrección de la acción predeterminada de la señal cuando se inserta por ptrace
- Implementa /proc/sys/vm/min_free_kbytes
- Usa valores de registro de contexto de equipo al restaurar el contexto en sigreturn
    - Esto resuelve el problema por el que java y javac se bloqueaban para algunos usuarios
- Implementa /proc/sys/kernel/hostname

### <a name="syscall-support"></a>Compatibilidad con llamadas del sistema
A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL. Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a>Compilación 14388 para la Actualización de aniversario de Windows 10
Para obtener información general de Windows sobre la compilación 14388, visita el [blog de Windows](https://aka.ms/14388wip). <br/>

### <a name="fixed"></a>Fijo
- Correcciones para prepararse para la Actualización de aniversario de Windows 10 el 2/8
  - Puedes encontrar más información sobre WSL en la Actualización de aniversario en nuestro [blog](https://blogs.msdn.microsoft.com/wsl/)

<br/>

## <a name="build-14376"></a>Compilación 14376
Para obtener información general de Windows sobre la compilación 14376, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/). <br/>

### <a name="fixed"></a>Fijo
- Se quitaron algunas instancias en las que apt-get se bloquea (GH 493)
- Se ha corregido un problema por el que los montajes vacíos no se controlaban correctamente
- Se ha corregido un problema por el que ramdisks no se montaban correctamente
- Cambio en la aceptación de sockets de Unix para admitir marcas (GH parcial 451)
- Se ha corregido la pantalla azul relacionada con la red común
- Se ha corregido la pantalla azul al acceder a /proc/[pid]/task (GH 523)
- Se ha corregido un uso elevado de la CPU en algunos escenarios de pty (GH 488, 504)
- Correcciones de errores y mejoras adicionales

<br/>

## <a name="build-14371"></a>Compilación 14371
Para obtener información general de Windows sobre la compilación 14371, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/). <br/>

### <a name="fixed"></a>Fijo
- Se ha corregido la carrera de tiempo con SIGCHLD y wait() al usar ptrace
- Se han corregido comportamientos cuando las rutas de acceso tienen una / final (GH 432)
- Se ha corregido un problema con el error de cambio de nombre o desvinculación debido a identificadores abiertos a elementos secundarios
- Correcciones de errores y mejoras adicionales

<br/>

## <a name="build-14366"></a>Compilación 14366
Para obtener información general de Windows sobre la compilación 14366, visita el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/). <br/>

### <a name="fixed"></a>Fijo
- Corrección en la creación de archivos mediante vínculos simbólicos
-   Se ha agregado listxattr para Python (GH 385)
-   Correcciones de errores y mejoras adicionales

### <a name="syscall-support"></a>Compatibilidad con llamadas del sistema
-   A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL. Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.

`listxattr`<br/>
<br/>

## <a name="build-14361"></a>Compilación 14361
Para obtener información general de Windows sobre la compilación 14361, visita el [blog de Windows](https://aka.ms/wip14361). <br/>

### <a name="fixed"></a>Fijo
- DrvFs ahora distingue entre mayúsculas y minúsculas cuando se ejecuta en Bash en Ubuntu en Windows.
  - Los usuarios pueden usar case.txt y CASE.TXT en sus unidades de /mnt/c
  - La distinción de mayúsculas y minúsculas solo se admite en Bash en Ubuntu en Windows. Fuera de Bash, NTFS notificará los archivos correctamente, pero puede producirse un comportamiento inesperado al interactuar con los archivos de Windows.
  - La raíz de cada volumen (es decir, /mnt/c) no distingue entre mayúsculas y minúsculas
  - Puedes encontrar más información sobre cómo controlar estos archivos en Windows [aquí](https://support.microsoft.com/en-us/kb/100625).
- Compatibilidad con pty/tty considerablemente mejorada.  Ahora se admiten aplicaciones como TMUX (GH 40)
- Se ha corregido el problema de instalación por el que las cuentas de usuario no siempre se creaban
- Se ha optimizado la estructura de argumentos de línea de comandos que permite una lista de argumentos extremadamente larga. (GH 153)
- Ahora puedes usar delete y chmod en archivos read_only de DrvFs
- Se han corregido algunas instancias en las que el terminal se bloquea en la desconexión (GH 43)
- chmod y chown ahora funcionan en dispositivos tty
- Permite la conexión a 0.0.0.0 y :: como localhost (GH 388)
- Sendmsg/recvmsg ahora controlan una longitud de vector de E/S > 1 (GH parcial 376)
- Los usuarios ahora pueden dejar de participar en archivos de hosts generados automáticamente (GH 398)
- La configuración regional de Linux se ajusta automáticamente con la configuración regional de NT durante la instalación (GH 11)
- Se ha agregado el archivo /proc/sys/vm/swappiness (GH 306)
- strace ahora se cierra correctamente
- Permite que las canalizaciones se vuelvan a abrir a través de /proc/self/fd (GH 222)
- Oculta directorios en %LOCALAPPDATA%\lxss de DrvFs (GH 270)
- Mejor control de bash.exe ~.  Ahora se admiten comandos como "bash ~-c ls" (GH 467)
- Ahora, los sockets notifican las lecturas de epoll disponibles durante el cierre (GH 271)
- lxrun /uninstall funciona mejor para eliminar archivos y carpetas
- Se ha corregido ps -f (GH 246)
- Se ha mejorado la compatibilidad con aplicaciones X11, como xEmacs (GH 481)
- Se ha actualizado el tamaño inicial de la pila de subprocesos para que coincida con la configuración predeterminada de Ubuntu, y se notifica el tamaño correctamente a la llamada del sistema get_rlimit (GH 172, 258)
- Se ha mejorado la notificación de nombres de imagen de proceso PICO (por ejemplo, para auditoría)
- Se ha implementado el comando /proc/mountinfo para df
- Se ha corregido el código de error de vínculo simbólico para el nombre secundario . y .
- Correcciones de errores y mejoras adicionales

### <a name="syscall-support"></a>Compatibilidad con llamadas del sistema
A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL. Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a>Compilación 14352
Para obtener información general de Windows sobre la compilación 14352, visita el [blog de Windows](https://aka.ms/wip14352).<br/>


### <a name="fixed"></a>Fijo
- Se ha corregido un problema en el que los archivos grandes no se descargaban o se creaban correctamente.  Esto debe desbloquear npm y otros escenarios (GH 3, GH 313)
- Se han quitado algunas instancias en las que los sockets se bloquean
- Se han corregido algunos errores de ptrace
- Se ha corregido un problema con WSL que permite nombres de archivo de más de 255 caracteres
- Se ha mejorado la compatibilidad con caracteres distintos del inglés
- Agrega datos de zona horaria de Windows actuales y los establece como valores predeterminados
- Id. de dispositivo único para cada punto de montaje (corrección de jre, GH 49)
- Corrige el problema con rutas de acceso que contienen "." y ".."
- Se ha agregado compatibilidad con Fifo (GH 71)
- Se ha actualizado el formato de resolv.conf para que coincida con el formato nativo de Ubuntu
- Algunas limpiezas de procfs
- Se ha habilitado ping para consolas de administrador (GH 18)

### <a name="syscall-support"></a>Compatibilidad con llamadas del sistema
A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL. Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a>Compilación 14342
Para obtener información general de Windows sobre la compilación 14342, visita el [blog de Windows](https://aka.ms/wip14342). <br/>

Puedes encontrar información sobre VolFs y DriveFs en el [blog de WSL](https://blogs.msdn.microsoft.com/wsl). <br/>

### <a name="fixed"></a>Fijo
- Se ha corregido el problema de instalación cuando el usuario de Windows tenía caracteres Unicode en el nombre de usuario
- La solución alternativa de apt-get update udev en las preguntas más frecuentes se proporciona ahora de forma predeterminada en la primera ejecución
- Vínculos simbólicos habilitados en directorios DriveFs (/mnt/<drive>)
- Los vínculos simbólicos ahora funcionan entre DriveFs y VolFs
- Se ha solucionado el problema de análisis de ruta de acceso de nivel superior:ls .// funcionará ahora como se espera
- La instalación de npm en DriveFs y las opciones -g ahora funcionan
- Se ha corregido un problema que impedía que el servidor PHP se iniciara
- Se han actualizado los valores de entorno predeterminados, como $PATH para que coincidan con Ubuntu nativo
- Se ha agregado una tarea de mantenimiento semanal en Windows para actualizar la caché de paquetes apt
- Se ha corregido un problema con la validación de encabezado de ELF, WSL ahora es compatible con todas las opciones de Melkor
- El shell Zsh funciona
- Ahora se admiten los binarios de Go precompilados
- Indicar bash.exe en la primera ejecución ahora se localiza correctamente
- /proc/meminfo ahora devuelve la información correcta
- Ahora se admiten sockets en VFS
- /dev ahora se monta como tempfs
- Ahora se admite Fifo
- Los sistemas de varios núcleos ahora se muestran correctamente en /proc/cpuinfo
- Mejoras adicionales y mensajes de error que se descargan durante la primera ejecución
- Mejoras de llamadas del sistema y corrección de errores. Lista de llamadas del sistema admitidas a continuación.
- Correcciones de errores y mejoras adicionales

### <a name="known-issues"></a>Problemas conocidos
- No se resuelve ".." correctamente en DriveFs en algunos casos

### <a name="syscall-support"></a>Compatibilidad con llamadas del sistema
A continuación se muestra una lista de llamadas del sistema nuevas o mejoradas que tienen alguna implementación en WSL. Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.

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

## <a name="build-14332"></a>Compilación 14332

Para obtener información general de Windows sobre la compilación 14332, visita el [blog de Windows](https://aka.ms/wip14332). <br/>


### <a name="fixed"></a>Fijo
- Mejor generación de resolv.conf, incluida la priorización de entradas de DNS
- Problema con el movimiento de archivos y directorios entre unidades /mnt y no /mnt
- Los archivos tar ahora se pueden crear con vínculos simbólicos
- Se ha agregado el directorio predeterminado /run/lock en la creación de instancias
- Actualiza /dev/null para que devuelva la información de estadísticas correcta
- Errores adicionales al descargar durante la primera ejecución
- Mejoras de llamadas del sistema y corrección de errores. Lista de llamadas del sistema admitidas a continuación.
- Correcciones de errores y mejoras adicionales

### <a name="syscall-support"></a>Compatibilidad con llamadas del sistema
A continuación se muestra la nueva llamada del sistema que tiene alguna implementación en WSL. La llamada del sistema de esta lista se admite en al menos un escenario, pero puede que no se admita todos los parámetros en este momento.

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a>Compilación 14328

Para obtener información general de Windows sobre la compilación 14332, visita el [blog de Windows](https://aka.ms/wip14328). <br/>


### <a name="new-features"></a>Nuevas características
* Ahora admite usuarios de Linux.  Al instalar Bash en Ubuntu en Windows, se solicitará la creación de un usuario de Linux.  Para más información, visita https://aka.ms/wslusers.
* El nombre de host ahora se establece en el nombre del equipo de Windows, ya no más en @localhost
* Para más información sobre la compilación 14328, visita: https://aka.ms/wip14328

### <a name="fixed"></a>Fijo
* Mejoras de vínculos simbólicos para archivos que no son /mnt/<drive>
    * La instalación de npm ahora funciona
    * jdk / jre ahora se puede instalar con las instrucciones que se encuentran [aquí](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).
    * Problema conocido: los vínculos simbólicos no funcionan para los montajes de Windows.  La funcionalidad estará disponible en una compilación posterior
* top y htop ahora se muestran
* Mensajes de error adicionales para algunos errores de instalación
* Mejoras de llamadas del sistema y corrección de errores.  Lista de llamadas del sistema admitidas a continuación.
* Correcciones de errores y mejoras adicionales

### <a name="syscall-support"></a>Compatibilidad con llamadas del sistema
A continuación hay una lista de llamadas del sistema que tienen alguna implementación en WSL.  Las llamadas del sistema de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.

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
