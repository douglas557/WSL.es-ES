---
title: Notas de la versión para el subsistema de Windows para Linux
description: Notas de la versión para el subsistema de Windows para Linux.  Actualizado semanalmente.
keywords: BashOnWindows, bash, WSL, Windows, subsistema de Windows para Linux, windowssubsystem, Ubuntu
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.openlocfilehash: e2d9d5fc70c173e9b516ab7af01599b623b40b39
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/14/2019
ms.locfileid: "67042424"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a>Notas de la versión para el subsistema de Windows para Linux


## <a name="build-18917"></a>Compilación 18917
Para obtener información general sobre Windows sobre la compilación 18917, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).

### <a name="wsl"></a>WSL
* WSL 2 ya está disponible. Consulte el [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) para obtener más detalles.
* Corregir una regresión en la que el inicio de procesos de Windows a través de vínculos simbólicos no funcionaba correctamente [alvent 3999]
* Agregue WSL. exe--List--verbose, WSL. exe--List--Quiet y WSL. exe--Import--version Options to WSL. exe
* Agregar WSL. exe: opción Shutdown
* Plan 9: Permitir abrir un directorio para escribir en él correctamente

## <a name="build-18890"></a>Compilación 18890
Para obtener información general sobre Windows sobre la compilación 18890, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).

### <a name="wsl"></a>WSL
* Pérdida de socket sin bloqueo [alvent 2913]
* La entrada de EOF en el terminal puede bloquear lecturas posteriores [alvent 3421]
* Actualice el encabezado resolv. conf para hacer referencia a WSL. conf [descrito en alvent 3928]
* Interbloqueo en epoll eliminar código [alvent 3922]
* Controlar los espacios de los argumentos en--Import y – Export [alvent 3932]
* La extensión de los archivos de mmap no funciona correctamente [alvent 3939]
* Corrección del problema con \\ARM64 WSL $ Access no funciona correctamente
* Agregar el mejor icono predeterminado para WSL. exe

## <a name="build-18342"></a>Compilación 18342
Para obtener información general sobre Windows sobre la compilación 18342, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).

### <a name="wsl"></a>WSL
* Hemos agregado la posibilidad de que los usuarios accedan a los archivos de Linux en un WSL distribución desde Windows. Se puede tener acceso a estos archivos a través de la línea de comandos y también las aplicaciones de Windows, como el explorador de archivos, VSCode, etc. pueden interactuar con estos archivos. Para acceder a los archivos, vaya \\a \\WSL\\$ < distro_name >, o consulte la lista de las distribuciones en ejecución \\navegando a \\WSL $
* Agregar etiquetas de información de CPU adicionales y corregir valores de Cpus_allowed [_list] [alvent 2234]
* Compatibilidad con Exec desde un subproceso no líder [alvent 3800]
* Tratar errores de actualización de la configuración como no graves [al3785]
* Actualización de binfmt para administrar correctamente los desplazamientos [alvent 3768]
* Habilitar la asignación de unidades de red para el Plan 9 [alvent 3854]
* Compatibilidad con Windows-> Linux y Linux-> la traducción de rutas de acceso de Windows para montajes de BIND
* Crear secciones de solo lectura para asignaciones en archivos abiertos de solo lectura

## <a name="build-18334"></a>Compilación 18334
Para obtener información general sobre Windows sobre la compilación 18334, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).

### <a name="wsl"></a>WSL
* Rediseño del modo en que se asigna la zona horaria de Windows a una zona horaria de Linux [alvent 3747]
* Corregir pérdidas de memoria y agregar nuevas funciones de traducción de cadenas [alvent 3746]
* SIGCONT en un elemento threadgroup sin subprocesos es una operación no operativa [alvent 3741] 
* Mostrar correctamente los descriptores de archivo de socket y epoll en/proc/Self/FD

## <a name="build-18305"></a>Compilación 18305
Para obtener información general sobre Windows sobre la compilación 18305, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).

### <a name="wsl"></a>WSL
* pthreads perder el acceso a los archivos cuando el subproceso principal sale [alvent 3589]
* TIOCSCTTY debe omitir el parámetro "Force" a menos que sea necesario [alvent 3652]
* mejoras en la línea de comandos de WSL. exe y la adición de la funcionalidad de importación y exportación.
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
Para obtener información general sobre Windows sobre la compilación 18277, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).

### <a name="wsl"></a>WSL
* Corrección del error "no se admite esta interfaz" que se presentó en la compilación 18272 [alvent 3645]
* Omitir la marca MNT_FORCE para umount syscall [alvent 3605]
* Cambiar la interoperabilidad de WSL para usar la API de CreatePseudoConsole oficial
* No mantener ningún valor de tiempo de espera cuando se reinicie FUTEX_WAIT

## <a name="build-18272"></a>Compilación 18272
Para obtener información general sobre Windows sobre la compilación 18272, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).

### <a name="wsl"></a>WSL
* **ATENCIÓN** Hay un problema en esta compilación que hace que WSL sea inoperable. Al intentar iniciar la distribución, verá el error "no se admite dicha interfaz". El problema se ha solucionado y estará en la compilación rápida de Insider de la semana siguiente. Si ha instalado esta compilación, puede revertir a la compilación anterior de Windows mediante "volver a la versión anterior de Windows 10" en Configuración-> actualización & la recuperación de > de seguridad.

## <a name="build-18267"></a>Compilación 18267
Para obtener información general sobre Windows sobre la compilación 18267, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).

### <a name="wsl"></a>WSL
* Corrija el problema en el que el proceso inerte no se puede obtener y permanecer indefinidamente.
* WslRegisterDistribution se bloquea si el mensaje de error supera la longitud máxima [alvent 3592]
* Permitir que fsync se realice correctamente para los archivos de solo lectura en DrvFs [alvent 3556]
* Asegúrese de que los directorios/Bin y/sbin existen antes de crear los vínculos simbólicos dentro de [alvent 3584]
* Se agregó un mecanismo de tiempo de espera de finalización de instancia para las instancias de WSL. El tiempo de espera está establecido actualmente en 15 segundos, lo que significa que la instancia finalizará 15 segundos después de que termine el último proceso WSL. Para finalizar una distribución inmediatamente, use:
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a>Compilación 17763 (1809)
Para obtener información general sobre Windows sobre la compilación 17763, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).

### <a name="wsl"></a>WSL
* SetPriority syscall Permission check Too STRICT para cambiar la misma prioridad de subprocesos [alvent 1838]
* Asegúrese de que el tiempo de interrupción no sesgado se usa para el tiempo de arranque para evitar que se devuelvan valores negativos para clock_gettime (CLOCK_BOOTTIME) [alvent 3434]
* Controlar los vínculos simbólicos en el intérprete WSL binfmt [alvent 3424]
* Mejor control de la limpieza de descriptores de archivo de elemento threadgroup Leader.
* Cambiar WSL para usar KeQueryInterruptTimePrecise en lugar de KeQueryPerformanceCounter para evitar el desbordamiento [alvent 3252]
* Ptrace Attach puede producir un valor de devolución incorrecto de las llamadas del sistema [alvent 1731]
* Corrección de varios problemas relacionados con AF_UNIX [alvent 3371]
* Corregir el problema que podría provocar un error de interoperabilidad de WSL si el directorio de trabajo actual tiene menos de 5 caracteres de longitud [alvent 3379]
* Evitar el retraso de un segundo error en las conexiones de bucle invertido a puertos no existentes [alvent 3286]
* Agregar archivo de código auxiliar de/proc/sys/FS/File-Max [alvent 2893]
* Información más precisa sobre el ámbito IPV6.
* Compatibilidad con PR_SET_PTRACER [alvent 3053]
* El sistema de archivos de canalización borra accidentalmente el evento epoll desencadenado por el borde [alvent 3276]
* El ejecutable de Win32 iniciado mediante el symlink de NTFS no respeta el nombre de symlink [alvent 2909]
* Compatibilidad mejorada con Zombie [alvent 1353]
* Agregar entradas WSL. conf para controlar el comportamiento de interoperabilidad de Windows [alvent 1493]
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* Corrección para getsockname no Always devolviendo siempre el tipo de familia de sockets UNIX [alvent 1774]
* Agregar compatibilidad para TIOCSTI [alvent 1863]
* Los sockets sin bloqueo en el proceso de conexión deben devolver EAGAIN para los intentos de escritura [alvent 2846]
* Compatibilidad con la interoperabilidad en VHD montados [alvent 3246, 3291]
* Corregir el problema de comprobación de permisos en la carpeta raíz [alvent 3304]
* Compatibilidad limitada para los ioctl de teclado TTY KDGKBTYPE, KDGKBMODE y KDSKBMODE.
* Las aplicaciones de interfaz de usuario de Windows deben ejecutarse incluso cuando se inician en segundo plano.
* Agregar WSL-u o--User Option [alvent 1203]
* Corregir problemas de inicio de WSL cuando se habilita el inicio rápido [alvent 2576]
* Los sockets de UNIX deben conservar las credenciales del mismo nivel desconectadas [alvent 3183]
* Sockets de UNIX sin bloqueo con error indefinidamente con EAGAIN [alvent 3191]
* Case = OFF es el nuevo tipo de montaje drvfs predeterminado [alvent 2937, 3212, 3328]
    * Consulte el [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) para obtener más información.
* Agregue wslconfig/Terminate. para detener las distribuciones en ejecución.
* Corrija el problema con las entradas del menú contextual del shell de WSL que no controlan correctamente las rutas de acceso con espacios.
* Exponer la distinción de mayúsculas y minúsculas por directorio como atributo extendido
* ARM64 Emular las operaciones de mantenimiento de la memoria caché. Resolver el [problema dotnet](https://github.com/dotnet/core/issues/1561).
* DrvFs: solo caracteres de escape en el intervalo privado que corresponden a un carácter de escape.
* Error de corrección de errores en la validación de longitud del intérprete del analizador ELF [alvent 3154]
* WSL los temporizadores absolutos con una hora en el pasado no se activan [alvent 3091]
* Asegúrese de que los puntos de reanálisis recién creados se muestran como tales en el directorio principal.
* Cree de forma atómica directorios con distinción entre mayúsculas y minúsculas en DrvFs.
* Se ha corregido un problema adicional en el que las operaciones multiproceso podían devolver ENOENT, aunque el archivo exista. [ALVENT 2712]
* Se corrigió un error de inicio de WSL cuando UMCI está habilitado. [ALVENT 3020]
* Agregue el menú contextual del explorador para iniciar WSL [alvent 437, 603, 1836]. Para usar, mantenga presionada la tecla Mayús y haga clic con el botón derecho en una ventana del explorador.
* Corregir el comportamiento de no bloqueo de sockets de UNIX [alvent 2822, 3100]
* Corrija el comando de NETLINK de bloqueo, tal como se muestra en alvent 2026.
* Agregue compatibilidad para los marcadores de propagación de montaje [alvent 2911].
* Corrección del problema con TRUNCATE no provocando eventos de inotify [alvent 2978].
* Agregue la opción--exec de WSL. exe para invocar un solo binario sin un shell.
* Add--Distribution Option para WSL. exe para seleccionar un distribución específico.
* Compatibilidad limitada para dmesg. Ahora, las aplicaciones pueden iniciar sesión en dmesg. El controlador WSL registra información limitada en dmesg. En el futuro, esto puede extenderse para llevar a cabo otros diagnósticos e información del controlador.
    * Nota: dmesg se admite actualmente a través `/dev/kmsg` de la interfaz de dispositivo. `syslog`la interfaz syscall todavía no se admite. Y, por lo tanto, algunas `dmesg` de las opciones de la `-S`línea `-C` de comandos, como, no funcionan.
* Cambiar el GID y el modo de dispositivos serie predeterminados para que coincidan con el nativo [alvent 3042]
* DrvFs ahora admite atributos extendidos.
    * Nota: DrvFs tiene algunas limitaciones en cuanto al nombre de los atributos extendidos. Algunos caracteres (como '/', ': ' y '\*') no están permitidos, y los nombres de atributos extendidos no distinguen mayúsculas de minúsculas en DrvFs

## <a name="build-18252-skip-ahead"></a>Compilación 18252 (omitir)
Para obtener información general sobre Windows sobre la compilación 18252, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).

### <a name="wsl"></a>WSL
* Traslado de los binarios init y bsdtar fuera del archivo dll de lxssmanager y a una carpeta de herramientas independiente
* Corregir la carrera en torno al cierre del descriptor de archivo cuando se usa CLONE_FILES
* Controlar campos opcionales en/proc/PID/mountinfo al traducir rutas de DrvFs
* Permita que DrvFs mknod se realice correctamente sin compatibilidad con metadatos para S_IFREG
* Los archivos ReadOnly creados en DrvFs deben tener el conjunto de atributos ReadOnly [alvent 3411]
* Incorporación de la aplicación auxiliar de/sbin/Mount.drvfs para controlar el montaje de DrvFs
* Use el cambio de nombre de POSIX en DrvFs.
* Permitir traducción de rutas de acceso en volúmenes sin un GUID de volumen.

## <a name="build-17738-fast"></a>Compilación 17738 (rápida)
Para obtener información general sobre Windows sobre la compilación 17738, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).

### <a name="wsl"></a>WSL
* SetPriority syscall Permission check Too STRICT para cambiar la misma prioridad de subprocesos [alvent 1838]
* Asegúrese de que el tiempo de interrupción no sesgado se usa para el tiempo de arranque para evitar que se devuelvan valores negativos para clock_gettime (CLOCK_BOOTTIME) [alvent 3434]
* Controlar los vínculos simbólicos en el intérprete WSL binfmt [alvent 3424]
* Mejor control de la limpieza de descriptores de archivo de elemento threadgroup Leader.

## <a name="build-17728-fast"></a>Compilación 17728 (rápida)
Para obtener información general sobre Windows sobre la compilación 17728, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).

### <a name="wsl"></a>WSL
* Cambiar WSL para usar KeQueryInterruptTimePrecise en lugar de KeQueryPerformanceCounter para evitar el desbordamiento [alvent 3252]
* Ptrace Attach puede producir un valor de devolución incorrecto de las llamadas del sistema [alvent 1731]
* Corrección de varios problemas relacionados con AF_UNIX [alvent 3371]
* Corregir el problema que podría provocar un error de interoperabilidad de WSL si el directorio de trabajo actual tiene menos de 5 caracteres de longitud [alvent 3379]

## <a name="build-18204-skip-ahead"></a>Compilación 18204 (omitir)
Para obtener información general sobre Windows sobre la compilación 18204, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).

### <a name="wsl"></a>WSL
* Canalización del sistema de archivos de canalización inadvertenly borrar el borde desencadenador de epoll [alvent 3276]
* El ejecutable de Win32 iniciado mediante el symlink de NTFS no respeta el nombre de symlink [alvent 2909]

## <a name="build-17723-fast"></a>Compilación 17723 (rápida)
Para obtener información general sobre Windows sobre la compilación 17723, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).

### <a name="wsl"></a>WSL
* Evitar el retraso de un segundo error en las conexiones de bucle invertido a puertos no existentes [alvent 3286]
* Agregar archivo de código auxiliar de/proc/sys/FS/File-Max [alvent 2893]
* Información más precisa sobre el ámbito IPV6.
* Compatibilidad con PR_SET_PTRACER [alvent 3053]
* Canalización del sistema de archivos de canalización inadvertenly borrar el borde desencadenador de epoll [alvent 3276]
* El ejecutable de Win32 iniciado mediante el symlink de NTFS no respeta el nombre de symlink [alvent 2909]

## <a name="build-17713"></a>Compilación 17713
Para obtener información general sobre Windows sobre la compilación 17713, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).

### <a name="wsl"></a>WSL
* Compatibilidad mejorada con Zombie [alvent 1353]
* Agregar entradas WSL. conf para controlar el comportamiento de interoperabilidad de Windows [alvent 1493]
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* Corrección para getsockname no Always devolviendo siempre el tipo de familia de sockets UNIX [alvent 1774]
* Agregar compatibilidad para TIOCSTI [alvent 1863]
* Los sockets sin bloqueo en el proceso de conexión deben devolver EAGAIN para los intentos de escritura [alvent 2846]
* Compatibilidad con la interoperabilidad en VHD montados [alvent 3246, 3291]
* Corregir el problema de comprobación de permisos en la carpeta raíz [alvent 3304]
* Compatibilidad limitada para los ioctl de teclado TTY KDGKBTYPE, KDGKBMODE y KDSKBMODE.
* Las aplicaciones de interfaz de usuario de Windows deben ejecutarse incluso cuando se inician en segundo plano.

## <a name="build-17704"></a>Compilación 17704
Para obtener información general sobre Windows sobre la compilación 17704, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).

### <a name="wsl"></a>WSL
* Agregar WSL-u o--User Option [alvent 1203]
* Corregir problemas de inicio de WSL cuando se habilita el inicio rápido [alvent 2576]
* Los sockets de UNIX deben conservar las credenciales del mismo nivel desconectadas [alvent 3183]
* Sockets de UNIX sin bloqueo con error indefinidamente con EAGAIN [alvent 3191]
* Case = OFF es el nuevo tipo de montaje drvfs predeterminado [alvent 2937, 3212, 3328]
    * Consulte el [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) para obtener más información.
* Agregue wslconfig/Terminate. para detener las distribuciones en ejecución.

## <a name="build-17692"></a>Compilación 17692
Para obtener información general sobre Windows sobre la compilación 17692, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).

### <a name="wsl"></a>WSL
* Corrija el problema con las entradas del menú contextual del shell de WSL que no controlan correctamente las rutas de acceso con espacios.
* Exponer la distinción de mayúsculas y minúsculas por directorio como atributo extendido
* ARM64 Emular las operaciones de mantenimiento de la memoria caché. Resolver el [problema dotnet](https://github.com/dotnet/core/issues/1561).
* DrvFs: solo caracteres de escape en el intervalo privado que corresponden a un carácter de escape.

## <a name="build-17686"></a>Compilación 17686
Para obtener información general sobre Windows sobre la compilación 17686, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).

### <a name="wsl"></a>WSL
* Error de corrección de errores en la validación de longitud del intérprete del analizador ELF [alvent 3154]
* WSL los temporizadores absolutos con una hora en el pasado no se activan [alvent 3091]
* Asegúrese de que los puntos de reanálisis recién creados se muestran como tales en el directorio principal.
* Cree de forma atómica directorios con distinción entre mayúsculas y minúsculas en DrvFs.

## <a name="build-17677"></a>Compilación 17677
Para obtener información general sobre Windows sobre la compilación 17677, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).

### <a name="wsl"></a>WSL
* Se ha corregido un problema adicional en el que las operaciones multiproceso podían devolver ENOENT, aunque el archivo exista. [ALVENT 2712]
* Se corrigió un error de inicio de WSL cuando UMCI está habilitado. [ALVENT 3020]

## <a name="build-17666"></a>Compilación 17666
Para obtener información general sobre Windows sobre la compilación 17666, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).

### <a name="wsl"></a>WSL
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a>ADVERTENCIA: Hay un problema que impide que WSL se ejecute en algunos chipsets AMD [alvent 3134]. Una corrección está lista y se convierte en la rama de compilación Insider.
* Agregue el menú contextual del explorador para iniciar WSL [alvent 437, 603, 1836]. Para usar Mayús y hacer clic con el botón derecho en una ventana del explorador.
* Corregir el comportamiento de no bloqueo de sockets de UNIX [alvent 2822, 3100]
* Corrija el comando de NETLINK de bloqueo, tal como se muestra en alvent 2026.
* Agregue compatibilidad para los marcadores de propagación de montaje [alvent 2911].
* Corrección del problema con TRUNCATE no provocando eventos de inotify [alvent 2978].
* Agregue la opción--exec de WSL. exe para invocar un solo binario sin un shell.
* Add--Distribution Option para WSL. exe para seleccionar un distribución específico.

## <a name="build-17655-skip-ahead"></a>Compilación 17655 (omitir)
Para obtener información general sobre Windows sobre la compilación 17655, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).

### <a name="wsl"></a>WSL
* Compatibilidad limitada para dmesg. Ahora, las aplicaciones pueden iniciar sesión en dmesg. El controlador WSL registra información limitada en dmesg. En el futuro, esto puede extenderse para llevar a cabo otros diagnósticos e información del controlador.
    * Nota: dmesg se admite actualmente a través `/dev/kmsg` de la interfaz de dispositivo. `syslog`la interfaz sycall todavía no se admite. Y, por lo tanto, algunas `dmesg` de las opciones de la `-S`línea `-C` de comandos, como, no funcionan.
* Se corrigió un problema en el que las operaciones multiproceso podían devolver ENOENT aunque el archivo exista. [ALVENT 2712]

## <a name="build-17639-skip-ahead"></a>Compilación 17639 (omitir)
Para obtener información general sobre Windows sobre la compilación 17639, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).

### <a name="wsl"></a>WSL
* Cambiar el GID y el modo de dispositivos serie predeterminados para que coincidan con el nativo [alvent 3042]
* DrvFs ahora admite atributos extendidos.
    * Nota: DrvFs tiene algunas limitaciones en cuanto al nombre de los atributos extendidos. En concreto, algunos caracteres (como '/', ': ' y '\*') no están permitidos, y los nombres de atributos extendidos no distinguen mayúsculas de minúsculas en DrvFs

## <a name="build-17133-fast"></a>Compilación 17133 (rápida)
Para obtener información general sobre Windows sobre la compilación 17133, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).

### <a name="wsl"></a>WSL
* Corrección de bloqueo en WSL. [ALVENT 3039, 3034]

## <a name="build-17128-fast"></a>Compilación 17128 (rápida)
Para obtener información general sobre Windows sobre la compilación 17128, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).

### <a name="wsl"></a>WSL
* None

## <a name="build-17627-skip-ahead"></a>Compilación 17627 (omitir)
Para obtener información general sobre Windows sobre la compilación 17627, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).

### <a name="wsl"></a>WSL
* Agregue compatibilidad para las operaciones compatibles con PI de Futex. [ALVENT 1006]
    * Tenga en cuenta que las prioridades no son actualmente una característica WSL admitida, por lo que hay limitaciones, pero el uso estándar debe estar desbloqueado.
* Compatibilidad con el Firewall de Windows para los procesos de WSL. [ALVENT 1852]
    * Por ejemplo, para permitir que el proceso de Python de WSL escuche en cualquier puerto, use el cmd de Windows con privilegios elevados:```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```
    * Para obtener más información sobre cómo agregar reglas de firewall, consulte [Link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)
* Respetar el shell predeterminado del usuario cuando se usa WSL. exe. [ALVENT 2372]
* Informe de todas las interfaces de red como Ethernet. [ALVENT 2996]
* Mejor control del archivo/etc/passwd dañado. [ALVENT 3001]

### <a name="console"></a>Console
* No hay correcciones.

### <a name="ltp-results"></a>Resultados de LTP:
Pruebas en curso.

## <a name="build-17618-skip-ahead"></a>Compilación 17618 (omitir)
Para obtener información general sobre Windows sobre la compilación 17618, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).

### <a name="wsl"></a>WSL
* Introduzca la funcionalidad de pseudoconsole para la interoperabilidad de NT [alvent 988, 1366, 1433, 1542, 2370, 2406].
* El mecanismo de instalación heredado (lxrun. exe) está en desuso. El mecanismo compatible para la instalación de distribuciones se realiza a través de la Microsoft Store.

### <a name="console"></a>Console
* No hay correcciones.

### <a name="ltp-results"></a>Resultados de LTP:
Pruebas en curso.

## <a name="build-17110"></a>Compilación 17110
Para obtener información general sobre Windows sobre la compilación 17110, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).

### <a name="wsl"></a>WSL
* Permitir que/init termine de Windows [alvent 2928].
* DrvFs Now usa la distinción de mayúsculas y minúsculas por directorio de forma predeterminada (equivalente a la opción de montaje "Case = dir").
    * El uso de "Case = Force" (el comportamiento anterior) requiere el establecimiento de una clave del registro. Ejecute el siguiente comando para habilitar "Case = Force" Si necesita usarlo: REG Add HKLM\SYSTEM\CurrentControlSet\Services\lxss/v DrvFsAllowForceCaseSensitivity/t REG_DWORD/d 1
    * Si tiene directorios existentes creados con WSL en una versión anterior de Windows que deben distinguir entre mayúsculas y minúsculas, use fsutil. exe para marcarlos con distinción de mayúsculas y <path> minúsculas: fsutil. exe File setcasesensitiveinfo enable
* Cadenas de finalización NULAs devueltas por el syscall de uname.

### <a name="console"></a>Console
* No hay correcciones.

### <a name="ltp-results"></a>Resultados de LTP:
Pruebas en curso.

## <a name="build-17107"></a>Compilación 17107
Para obtener información general sobre Windows sobre la compilación 17107, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).

### <a name="wsl"></a>WSL
* Compatibilidad con TCSETSF y TCSETSW en los puntos de conexión de Master PTY [alvent 2552].
* Iniciar procesos de interoperabilidad simultáneos puede dar lugar a EINVAL [alvent 2813].
* Corrección de PTRACE_ATTACH para mostrar el estado de seguimiento adecuado en/proc/PID/status.
* Corregir la carrera en la que los procesos de corta duración clonados con las marcas CLEARTID y SETTID podrían salir sin borrar la dirección de TID.
* Mostrar un mensaje al actualizar los directorios del sistema de archivos de Linux al pasar de una compilación anterior a la 17093. Para obtener más detalles sobre los cambios del sistema de archivos 17093, consulte las notas de la versión de [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).

### <a name="console"></a>Console
* No hay correcciones.

### <a name="ltp-results"></a>Resultados de LTP:
Pruebas en curso.

## <a name="build-17101"></a>Compilación 17101
Para obtener información general sobre Windows sobre la compilación 17101, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).

### <a name="wsl"></a>WSL
* Compatibilidad con signalfd. [ALVENT 129]
* Admita nombres de archivo que contengan caracteres NTFS no válidos mediante su codificación como caracteres Unicode privados. [ALVENT 1514]
* El montaje automático se reservará en modo de solo lectura cuando no se admita la escritura. [ALVENT 2603]
* Permite pegar los pares suplentes Unicode (como los caracteres emoji). [ALVENT 2765]
* Los pseudo archivos de/proc y/sys deben devolver lectura y escritura listas para seleccionar, sondeo, epoll, et al. [alvent 2838]
* Corrija el problema que podría hacer que el servicio pudiera entrar en un bucle infinito cuando el registro se haya alterado o esté dañado.
* Corrija los mensajes de NetLink para trabajar con la versión más reciente (de nivel superior 4,14) de iproute2.

### <a name="console"></a>Console
* No hay correcciones.

### <a name="ltp-results"></a>Resultados de LTP:
Pruebas en curso.

## <a name="build-17093"></a>Compilación 17093
Para obtener información general sobre Windows sobre la compilación 17093, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).

#### <a name="important"></a>Importante:
Al iniciar WSL por primera vez después de actualizar a esta compilación, debe realizar algún trabajo al actualizar los directorios del sistema de archivos de Linux. Esto puede tardar varios minutos, por lo que es posible que WSL se inicie lentamente. Esto solo debería ocurrir una vez por cada distribución que haya instalado desde la tienda.
* Compatibilidad mejorada de distinción de mayúsculas y minúsculas en DrvFs.
    * DrvFs admite ahora la distinción de mayúsculas y minúsculas por directorio. Se trata de una nueva marca que se puede establecer en directorios para indicar que todas las operaciones de esos directorios deben tratarse como con distinción de mayúsculas y minúsculas, lo que permite que las aplicaciones de Windows abran archivos que solo difieren en mayúsculas y minúsculas.
    * DrvFs tiene nuevas opciones de montaje que controlan la distinción de mayúsculas y minúsculas por directorio.
        * Case = Force: todos los directorios se tratan con distinción de mayúsculas y minúsculas (excepto la raíz de la unidad). Los nuevos directorios creados con WSL se marcan con distinción de mayúsculas y minúsculas. Este es el comportamiento heredado excepto para marcar los nuevos directorios que distinguen mayúsculas de minúsculas.
        * Case = dir: solo los directorios con la marca de distinción de mayúsculas y minúsculas por directorio se tratan como distinguir mayúsculas de minúsculas; otros directorios no distinguen mayúsculas de minúsculas. Los nuevos directorios creados con WSL se marcan con distinción de mayúsculas y minúsculas.
        * Case = OFF: solo los directorios con la marca de distinción de mayúsculas y minúsculas por directorio se tratan como distinguir mayúsculas de minúsculas; otros directorios no distinguen mayúsculas de minúsculas. Los nuevos directorios creados con WSL se marcan como no distinguir mayúsculas de minúsculas.
    * Nota: los directorios creados por WSL en versiones anteriores no tienen esta marca establecida, por lo que no se tratará como distinción entre mayúsculas y minúsculas si usa la opción "Case = dir". Próximamente se establecerá una manera de establecer esta marca en los directorios existentes.
    * Ejemplo de montaje con estas opciones (en el caso de las unidades existentes, primero debe desmontar antes de poder montar con distintas opciones): sudo mount-t drvfs C:/mnt/c-o Case = dir
    * Por ahora, Case = Force sigue siendo la opción predeterminada. Se cambiará a case = dir en el futuro.
* Ahora puede usar barras diagonales en las rutas de acceso de Windows al montar DrvFs, por ejemplo: sudo mount-t DrvFs//Server/SHARE/mnt/share
* WSL ahora procesa el archivo/etc/fstab durante el inicio de la instancia [alvent 2636].
    * Esto se hace antes de montar automáticamente las unidades de DrvFs; las unidades que ya se hayan montado mediante fstab no se volverán a montar automáticamente, lo que le permitirá cambiar el punto de montaje para unidades específicas.
    * Este comportamiento se puede desactivar mediante WSL. conf.
* Los archivos Mount, mountinfo y mountstats de/proc convierten correctamente en caracteres especiales, como barras diagonales inversas y espacios [alvent 2799]
* Los archivos especiales creados con DrvFs, como los vínculos simbólicos de WSL, o FIFO y Sockets cuando se habilitan los metadatos, ahora se pueden copiar y pasar de Windows.

#### <a name="wsl-is-more-configurable-with-wslconf"></a>WSL es más configurable con WSL. conf
Hemos agregado un método para que configure automáticamente ciertas funciones en WSL que se aplicarán cada vez que inicie el subsistema. Esto incluye opciones de montaje automático y configuración de red. Obtenga más información en la entrada de blog en: https://aka.ms/wslconf

#### <a name="afunix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a>AF_UNIX permite conexiones de socket entre procesos de Linux en WSL y procesos nativos de Windows
Las aplicaciones de WSL y Windows ahora pueden comunicarse entre sí a través de sockets de Unix. Imagine que quiere ejecutar un servicio en Windows y hacer que esté disponible para las aplicaciones de Windows y WSL. Ahora, eso es posible con los sockets de Unix. Lea más en nuestra entrada de blog en https://aka.ms/afunixinterop

### <a name="wsl"></a>WSL
* Compatibilidad con mmap () con MAP_NORESERVE [alvent 121, 2784]
* Compatibilidad con CLONE_PTRACE y CLONE_UNTRACED [alvent 121, 2781]
* Controlar la señal de terminación no SIGCHLD en el clon [alvent 121, 2781]
* Stub/proc/sys/FS/inotify/max_user_instances y/proc/sys/FS/inotify/max_user_watches [alvent 1705]
* Error al cargar binarios de ELF que contienen encabezados de carga con desplazamientos distintos de cero [alvent 1884]
* Cero bytes de página finales al cargar imágenes.
* Reducir los casos en los que execve finaliza el proceso de forma silenciosa

### <a name="console"></a>Console
* No hay correcciones.

### <a name="ltp-results"></a>Resultados de LTP:
Pruebas en curso.

## <a name="build-17083"></a>Compilación 17083
Para obtener información general sobre Windows sobre la compilación 17083, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).

### <a name="wsl"></a>WSL
* Se corrigió la BugCheck relacionada con epoll [alvent 2798, 2801, 2857]
* Se han corregido bloqueos al desactivar ASLR [alvent 1185, 2870]
* Asegurarse de que las operaciones de mmap aparecen atómicas [alvent 2732]

### <a name="console"></a>Console
* No hay correcciones.

### <a name="ltp-results"></a>Resultados de LTP:
Pruebas en curso.

## <a name="build-17074"></a>Compilación 17074
Para obtener información general sobre Windows sobre la compilación 17074, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).

### <a name="wsl"></a>WSL
* Formato de almacenamiento fijo de los metadatos de DrvFs [alvent 2777] </br>
**Importante:** Los metadatos de DrvFs creados antes de esta compilación no se mostrarán correctamente o no se mostrarán en absoluto. Para corregir los archivos afectados, use chmod y chown para volver a aplicar los metadatos.
* Se corrigió un problema con varias señales y llamadas syscall reiniciables.

### <a name="console"></a>Console
* No hay correcciones.

### <a name="ltp-results"></a>Resultados de LTP:
Pruebas en curso.

## <a name="build-17063"></a>Compilación 17063
Para obtener información general sobre Windows sobre la compilación 17063, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).

### <a name="wsl"></a>WSL
* DrvFs admite metadatos de Linux adicionales. Esto permite establecer el propietario y el modo de los archivos con chmod/chown y también la creación de archivos especiales como FIFO, sockets de UNIX y archivos de dispositivo. Esta opción está deshabilitada de forma predeterminada ya que sigue siendo experimental.
**Nota:**  Se corrigió un error en el formato de metadatos usado por DrvFs. Aunque los metadatos funcionan en esta compilación para experimentación, las compilaciones futuras no leerán correctamente los metadatos creados por esta compilación.  Es posible que tenga que actualizar manualmente el propietario de los archivos modificados y se tendrán que volver a crear los dispositivos con un identificador de dispositivo personalizado.

  Para habilitar, Monte DrvFs con la opción de metadatos (para habilitarlo en un montaje existente, primero debe desmontarlo):

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  Los permisos de Linux se agregan como metadatos adicionales al archivo; no afectan a los permisos de Windows.  Recuerde que la edición de un archivo mediante un editor de Windows puede quitar los metadatos. En este caso, el archivo volverá a sus permisos predeterminados.

* Se han agregado opciones de montaje a DrvFs para controlar archivos sin metadatos.
  * UID: el identificador de usuario que se usa para el propietario de todos los archivos.
  * GID: el identificador de grupo que se usa para el propietario de todos los archivos.
  * umask: máscara octal de permisos que se van a excluir para todos los archivos y directorios.
  * fMask: máscara octal de permisos que se van a excluir para todos los archivos normales.
  * dmask: máscara octal de permisos que se van a excluir para todos los directorios.

  Por ejemplo:
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  Combine con la opción de metadatos para especificar los permisos predeterminados para los archivos sin metadatos.

* Presentó una nueva variable de entorno `WSLENV`,, para configurar cómo fluyen las variables de entorno entre WSL y Win32.

  Por ejemplo:

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  `WSLENV`es una lista delimitada por signos de dos puntos de variables de entorno que se puede incluir al iniciar procesos de WSL desde los procesos Win32 o Win32 desde WSL.  Cada variable puede tener como sufijo una barra diagonal seguida de marcas para especificar cómo se va a traducir.
  * m El valor es una ruta de acceso que se debe traducir entre las rutas de acceso de WSL y las rutas de acceso de Win32.
  * CG El valor es una lista de rutas de acceso. En WSL, se trata de una lista delimitada por signos de dos puntos. En Win32, se trata de una lista delimitada por punto y coma.
  * 5\.50 Solo se debe incluir el valor al invocar WSL desde Win32
  * con Solo se debe incluir el valor al invocar a Win32 desde WSL

  Puede establecer `WSLENV` en. bashrc o en el entorno de Windows personalizado para el usuario.

* los montajes de drvfs conservan correctamente las marcas de tiempo de tar, CP-p (alvent 1939)
* los vínculos simbólicos de drvfs informan del tamaño correcto (alvent 2641)
* lectura/escritura funciona para tamaños de e/s muy grandes (alvent 2653)
* waitpid funciona con identificadores de grupo de procesos (alvent 2534)
* rendimiento mmap significativamente mejorado para regiones de reserva grande; mejora el rendimiento de GHC (alvent 1671)
* la personalidad es compatible con READ_IMPLIES_EXEC; correcciones y CLISP (alvent 1185)
* mprotect admite PROT_GROWSDOWN; corrige CLISP (alvent 1128)
* correcciones de errores de página en modo de sobreconfirmación; corrige SBCL (alvent 1128)
* Clone admite más combinaciones de marcas
* Compatibilidad con Select/epoll de archivos de epoll (antes de una operación no operativa).
* Notificar a ptrace de llamadas syscall no implementado.
* Omitir las interfaces que no están al generar los servidores de nombres resolv. conf [alvent 2694]
* Enumerar las interfaces de red sin dirección física. [ALVENT 2685]
* Correcciones de errores adicionales y mejoras.

### <a name="linux-tools-available-to-developers-on-windows"></a>Herramientas de Linux disponibles para desarrolladores en Windows

* La cadena de herramientas de la línea de comandos de Windows incluye bsdtar (tar) y rizo.
  Lea [este blog](https://aka.ms/tarcurlwindows) para obtener más información acerca de cómo agregar estas dos nuevas herramientas y ver cómo están dando forma a la experiencia del Desarrollador en Windows.

*   `AF_UNIX`está disponible en el SDK de Windows Insider (17061 +).
  Lea [este blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) para obtener más información `AF_UNIX` sobre y cómo los desarrolladores de Windows pueden usarlo.

### <a name="console"></a>Console
* No hay correcciones.

### <a name="ltp-results"></a>Resultados de LTP:
Pruebas en curso.


## <a name="build-17046"></a>Compilación 17046

Para obtener información general sobre Windows sobre la compilación 17046, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).

### <a name="fixed"></a>Corregido
#### <a name="wsl"></a>WSL
- Permite que los procesos se ejecuten sin un terminal activo. [Alvent 709, 1007, 1511, 2252, 2391, et al.]
- Mejor compatibilidad con CLONE_VFORK y CLONE_VM. [ALVENT 1878, 2615]
- Omita los controladores de filtro TDI para las operaciones de red de WSL. [ALVENT 1554]
- DrvFs crea vínculos simbólicos NT cuando se cumplen determinadas condiciones. [ALVENT 353, 1475, 2602]
    - El destino del vínculo debe ser relativo, no debe cruzar ningún punto de montaje o vínculos simbólicos, y debe existir.
    - El usuario debe tener SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (esto normalmente requiere que inicie WSL. exe con privilegios elevados), a menos que esté activado el modo de desarrollador.
    - En todas las demás situaciones, DrvFs todavía crea vínculos simbólicos de WSL.
- Permite ejecutar instancias de WSL con privilegios elevados y no elevados simultáneamente.
- Compatibilidad con/proc/sys/kernel/Yama/ptrace_scope
- Agregue wslpath para realizar conversiones de rutas de acceso de Windows de WSL <->. [Alvent 522, 1243, 1834, 2327, et al.]
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a>Console
- No hay correcciones.

### <a name="ltp-results"></a>Resultados de LTP:
Pruebas en curso.


## <a name="build-17040"></a>Compilación 17040

Para obtener información general sobre Windows sobre la compilación 17040, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).<br/>


### <a name="fixed"></a>Corregido
#### <a name="wsl"></a>WSL
- No hay correcciones desde 17035.

#### <a name="console"></a>Console
- No hay correcciones desde 17035.

### <a name="ltp-results"></a>Resultados de LTP:
Pruebas en curso.

## <a name="build-17035"></a>Compilación 17035

Para obtener información general sobre Windows sobre la compilación 17035, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).<br/>


### <a name="fixed"></a>Corregido
#### <a name="wsl"></a>WSL
- En ocasiones, el acceso a los archivos de DrvFs podría producir errores con EINVAL. [ALVENT 2448]

#### <a name="console"></a>Console
- Pérdida de color al insertar o eliminar líneas en modo VT.

### <a name="ltp-results"></a>Resultados de LTP:
Pruebas en curso.

## <a name="build-17025"></a>Compilación 17025

Para obtener información general sobre Windows sobre la compilación 17025, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).<br/>


### <a name="fixed"></a>Corregido
#### <a name="wsl"></a>WSL
- Iniciar procesos iniciales en un nuevo grupo de procesos en primer plano [alvent 1653, 2510].
- Correcciones de entrega de SIGHUP [alvent 2496].
- Generar nombre de puente virtual predeterminado si no se proporciona ninguno [alvent 2497].
- Implementar/proc/sys/kernel/Random/boot_id [al2518].
- Más correcciones de la canalización stdout/stderr de interoperabilidad.
- Llamada del sistema syncfs de stub.

#### <a name="console"></a>Console
- Corrección de la traducción de VT de entrada para consolas de terceros [alvent 111]

### <a name="ltp-results"></a>Resultados de LTP:
Pruebas en curso.

## <a name="build-17017"></a>Compilación 17017

Para obtener información general sobre Windows sobre la compilación 17017, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).<br/>


### <a name="fixed"></a>Corregido
#### <a name="wsl"></a>WSL
- Omitir los encabezados de programa ELF vacíos [alvent 330].
- Permita que LxssManager Cree instancias de WSL para usuarios no interactivos (SSH y soporte de tareas programadas) [alvent 777, 1602].
- Compatibilidad con escenarios de WSL-> Win32-> WSL ("Inicio") [alvent 1228].
- Compatibilidad limitada para la terminación de las aplicaciones de consola que se invocan a través de la interoperabilidad [alvent 1614].
- Compatibilidad con las opciones de montaje para devpts [alvent 1948].
- Inicio de bloqueo secundario de ptrace [alvent 2333].
- EPOLLET faltan algunos eventos [alvent 2462].
- Devolver más datos para PTRACE_GETSIGINFO.
- Getdents con lseek proporciona resultados incorrectos.
- Corrección de bloqueo de la aplicación de interoperabilidad Win32, esperando la entrada en una canalización que no tiene más datos.
- Compatibilidad de O_ASYNC con archivos TTY/PTY.
- Mejoras y correcciones de errores adicionales

#### <a name="console"></a>Console
- No hay cambios relacionados con la consola en esta versión.

### <a name="ltp-results"></a>Resultados de LTP:
Pruebas en curso.

## <a name="fall-creators-update"></a>Fall Creators Update

## <a name="build-16288"></a>Compilación 16288

Para obtener información general sobre Windows sobre la compilación 16288, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).<br/>


### <a name="fixed"></a>Corregido
#### <a name="wsl"></a>WSL
- Inicializar y notificar correctamente UID, GID y el modo para los descriptores de archivo de socket [alvent 2490]
- Mejoras y correcciones de errores adicionales

#### <a name="console"></a>Console
- No hay cambios relacionados con la consola en esta versión.

### <a name="ltp-results"></a>Resultados de LTP:
Sin cambios desde 16273

## <a name="build-16278"></a>Compilación 16278

Para obtener información general sobre Windows sobre la compilación 162738, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).<br/>


### <a name="fixed"></a>Corregido
#### <a name="wsl"></a>WSL
- Anular explícitamente las vistas asignadas de las secciones respaldadas por archivos al desplazar hacia abajo el estado LX MM [alvent 2415]
- Mejoras y correcciones de errores adicionales

#### <a name="console"></a>Console
- No hay cambios relacionados con la consola en esta versión.

### <a name="ltp-results"></a>Resultados de LTP:
Sin cambios desde 16273

## <a name="build-16275"></a>Compilación 16275

Para obtener información general sobre Windows sobre la compilación 162735, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).<br/>


### <a name="fixed"></a>Corregido
#### <a name="wsl"></a>WSL
- No hay ningún cambio relacionado con WSL en esta versión.

#### <a name="console"></a>Console
- No hay cambios relacionados con la consola en esta versión.

### <a name="ltp-results"></a>Resultados de LTP:
Sin cambios desde 16273

## <a name="build-16273"></a>Compilación 16273

Para obtener información general sobre Windows sobre la compilación 16273, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).<br/>


### <a name="fixed"></a>Corregido
#### <a name="wsl"></a>WSL
- Se ha corregido un problema por el que DrvFs a veces indicó un tipo de archivo incorrecto para los directorios [alvent 2392]
- Permitir la creación de NETLINK_KOBJECT_UEVENT Sockets para desbloquear programas que usan UEVENT [al1121, 2293, 2242, 2295, 2235, 648, 637]
- Agregar compatibilidad para conexión sin bloqueo [alvent 903, 1391, 1584, 1585, 1829, 2290, 2314]
- Implementación de la marca de llamada del sistema Clone CLONE_FS [alvent 2242]
- Corregir los problemas que no controlan las tabulaciones o comillas correctamente en la interoperabilidad de NT [alvent 1625, 2164]
- Resolver el error de acceso denegado al intentar volver a iniciar instancias de WSL [alvent 651, 2095]
- Implementación de las operaciones de Futex FUTEX_REQUEUE y FUTEX_CMP_REQUEUE [alvent 2242]
- Corrección de permisos para varios archivos de SysFs [alvent 2214]
- Corregir bloqueo de pila de Haskell durante la instalación [alvent 2290]
- Implementar marcas binfmt_misc ' C ' ' O ' y ' P ' [alvent 2103]
- Add/proc/sys/kernel/SHMMAX/shmmni &/threads-Max [alvent 1753]
- Agregar compatibilidad parcial para llamada del sistema ioprio_set [alvent 498]
- Stub SO_REUSEPORT & agregar compatibilidad para SO_PASSCRED para Sockets de NetLink [alvent 69]
- Devolver distintos códigos de error de RegisterDistribuiton si se está instalando o desinstalando actualmente una distribución.
- Permitir la anulación del registro de distribuciones de WSL parcialmente instaladas a través de wslconfig. exe
- Corrección de bloqueo de prueba de socket de Python de UDP:: msg_peek
- Mejoras y correcciones de errores adicionales

#### <a name="console"></a>Console
- No hay cambios relacionados con la consola en esta versión.

### <a name="ltp-results"></a>Resultados de LTP:
Total de pruebas: 1904<br/>
Total de pruebas omitidas: 209<br/>
Total de errores: 229<br/>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a>Compilación 16257

Para obtener información general sobre Windows sobre la compilación 16257, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).<br/>


### <a name="fixed"></a>Corregido
#### <a name="wsl"></a>WSL
- Implementar llamada del sistema prlimit64
- Incorporación de compatibilidad con ulimit-n (setrlimit RLIMIT_NOFILE) [alvent 1688]
- MSG_MORE de código auxiliar para Sockets TCP [alvent 2351]
- Corregir el comportamiento del vector auxiliar de AT_EXECFN no válido [alvent 2133]
- Corregir el comportamiento de copiar y pegar para consola/TTY y agregar un mejor control de búfer completo [alvent 2204, 2131]
- Establecer AT_SECURE en Vector auxiliar para los programas set-User-ID y set-Group-ID [alvent 2031]
- Psuedo: el extremo maestro de terminal no controla TIOCPGRP [alvent 1063]
- Corrección de lseek hace para rebobinar directorios en LxFs [alvent 2310]
- /dev/ptmx se bloquea después del uso intensivo [alvent 1882]
- Mejoras y correcciones de errores adicionales

#### <a name="console"></a>Console
- Corrección para líneas horizontales o guiones bajos en todas partes [alvent 2168]
- Corrección para el orden de procesamiento cambiado haciendo que NPM sea más difícil de cerrar [alvent 2170]
- Se ha agregado la nueva combinación de colores: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/

### <a name="ltp-results"></a>Resultados de LTP:
Sin cambios desde 16251

### <a name="syscall-support"></a>Compatibilidad con syscall
A continuación se muestra una lista de llamadas syscall nuevos o mejorados que tienen alguna implementación en WSL. Los llamadas syscall de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.

`prlimit64`<br/>

### <a name="known-issues"></a>Problemas conocidos
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[Problema de GitHub 2392: Carpetas de Windows no reconocidas por WSL...](https://github.com/Microsoft/BashOnWindows/issues/2392)
En la compilación 16257, WSL tiene problemas al enumerar archivos o carpetas de `/mnt/c/...`Windows a través de.
Este problema se ha corregido y debe publicarse en la compilación Insider durante la semana que comienza a las 8/14/2017.

<br/>

## <a name="build-16251"></a>Compilación 16251

Para obtener información general sobre Windows sobre la compilación 16251, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).<br/>


### <a name="fixed"></a>Corregido
#### <a name="wsl"></a>WSL
- Quitar la etiqueta beta del componente opcional WSL, consulte la [entrada de blog](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) para obtener más información.
- Inicialice correctamente el UID y el GID del conjunto guardado para los archivos Set-User-ID y set-Group-ID en exec [alvent 962, 1415, 2072]
- Se agregó compatibilidad con ptrace PTRACE_O_TRACEEXIT [alvent 555]
- Se ha agregado compatibilidad con ptrace PTRACE_GETFPREGS y PTRACE_GETREGSET con NT_FPREGSET [alvent 555]
- Se corrigió ptrace para que se detenga en las señales omitidas
- Mejoras y correcciones de errores adicionales

#### <a name="console"></a>Console
- No hay cambios relacionados con la consola en esta versión.

### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 768</br>
Número de pruebas con errores: 244</br>
Número de pruebas omitidas: 96</br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a>Compilación 16241

Para obtener información general sobre Windows sobre la compilación 16241, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).<br/>


### <a name="fixed"></a>Corregido
#### <a name="wsl"></a>WSL
- No hay ningún cambio relacionado con WSL en esta versión.

#### <a name="console"></a>Console
- Corrección para la generación de un carácter equivocado para las líneas de paso DEC, que se inscribió originalmente [aquí](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)
- Corrección para que no se muestre texto de salida en la página de códigos 65001 (UTF8)
- No transfiera los cambios realizados en los valores RGB de un color a otras partes de la paleta en el cambio de selección. Esto hará que la hoja de propiedades de la consola sea mucho más fácil de usar.
- No parece que Ctrl + S funcione correctamente
- No mostrar en negrita/-atenuar completamente desde códigos de escape ANSI [alvent 2174]
- La consola no admite correctamente los temas de color VIM [alvent 1706]
- No se pueden pegar caracteres determinados [alvent 2149]
- El cambio de tamaño de reflujo interactúa de forma extraña con el cambio de tamaño de una ventana de Bash cuando el contenido está en la línea de comandos/edición [alConEmu 1123]
- Ctrl-L deja la pantalla desfasada [alvent 1978]
- Error de representación de consola al mostrar VT en HDPI [alvent 1907]
- Los caracteres Japansese parecen extraños con el carácter Unicode U + 30FB [alvent 2146]
- Mejoras y correcciones de errores adicionales

</br>

## <a name="build-16237"></a>Compilación 16237

Para obtener información general sobre Windows sobre la compilación 16237, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).<br/>


### <a name="fixed"></a>Corregido
- Usar atributos predeterminados para archivos sin EAs en lxfs (raíz, raíz, 0000)
- Compatibilidad agregada para distribuciones que usan atributos extendidos
- Corregir el relleno de las entradas devueltas por getdents y getdents64
- Corrección de los permisos comprobación de la llamada del sistema shmctl SHM_STAT [alvent 2068]
- Se corrigió el estado inicial incorrecto de epoll para ttys [alvent 2231]
- Fix DrvFs readdir no devuelve todas las entradas [alvent 2077]
- Corregir LxFs readdir cuando los archivos están desvinculados [alvent 2077]
- Permitir que los archivos drvfs no vinculados se vuelvan a abrir a través de procfs
- Se ha agregado la invalidación de la clave del registro global para deshabilitar las características de WSL
- Corrección del recuento incorrecto de bloques en "stat" para DrvFs (y LxFs) [alvent 1894]
- Mejoras y correcciones de errores adicionales

</br>

## <a name="build-16232"></a>Compilación 16232

Para obtener información general sobre Windows sobre la compilación 16232, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).<br/>


### <a name="fixed"></a>Corregido
- No hay ningún cambio relacionado con WSL en esta versión.

</br>

## <a name="build-16226"></a>Compilación 16226

Para obtener información general sobre Windows sobre la compilación 16226, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).<br/>


### <a name="fixed"></a>Corregido
- xattr relacionado con llamadas syscall (getxattr, setxattr, listxattr, removexattr).
- compatibilidad con Security. capablity xattr.
- Compatibilidad mejorada con determinados sistemas de archivos y filtros, incluidos los servidores SMB que no son de MS. [ALVENT #1952]
- Compatibilidad mejorada para los marcadores de posición de OneDrive, los marcadores de posición de GVFS y los archivos comprimidos del sistema operativo.
- Mejoras y correcciones de errores adicionales

</br>

## <a name="build-16215"></a>Compilación 16215

Para obtener información general sobre Windows sobre la compilación 16215, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).<br/>


### <a name="fixed"></a>Corregido
- WSL ya no requiere el modo de desarrollador.
- Compatibilidad con uniones de directorios en drvfs.
- Controla la desinstalación de paquetes appx de distribución de WSL.
- Actualice procfs para mostrar las asignaciones privadas y compartidas.
- Agregar la capacidad de wslconfig. exe para limpiar las distribuciones que se instalan o desinstalan parcialmente.
- Compatibilidad agregada para IP_MTU_DISCOVER para Sockets TCP. [ALVENT 1639, 2115, 2205]
- Inferencia de la familia de protocolos para rutas a AF_INADDR.
- Mejoras en los dispositivos serie [alvent 1929].

</br>

## <a name="build-16199"></a>Compilación 16199

Para obtener información general sobre Windows sobre la compilación 16199, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).<br/>


### <a name="fixed"></a>Corregido
- No hay ningún cambio relacionado con WSL en estas versiones.

</br>

## <a name="build-16193"></a>Compilación 16193

Para obtener información general sobre Windows sobre la compilación 16193, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).<br/>


### <a name="fixed"></a>Corregido
- Condición de carrera entre el envío de SIGCONT y un elemento threadgroup de terminación [alvent 1973]
- cambiar los dispositivos TTY y PTY a Report FILE_DEVICE_NAMED_PIPE en lugar de FILE_DEVICE_CONSOLE [alvent 1840]
- Corrección de SSH para IP_OPTIONS
- Se ha cambiado el montaje de DrvFs al demonio de inicialización [alvent 1862, 1968, 1767, 1933]
- Se agregó compatibilidad en DrvFs para los siguientes vínculos simbólicos de NT.

</br>

## <a name="build-16184"></a>Compilación 16184

Para obtener información general sobre Windows sobre la compilación 16184, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).<br/>


### <a name="fixed"></a>Corregido
- Tarea de mantenimiento de paquetes APT quitada (lxrun. exe/Update)
- Salida corregida que no se muestra en los procesos de Windows en node. js [alvent 1840]
- Relajar los requisitos de alineación en lxcore [alvent 1794]
- Control corregido de la marca AT_EMPTY_PATH en un número de llamadas del sistema.
- Problema corregido en el que la eliminación de archivos DrvFs con identificadores abiertos hará que el archivo muestre un comportamiento indefinido [alvent 544, 966, 1357, 1535, 1615]
- /etc/hosts heredará ahora entradas del archivo de hosts de Windows (%windir%\system32\drivers\etc\hosts) [alvent 1495]

</br>

## <a name="build-16179"></a>Compilación 16179

Para obtener información general sobre Windows sobre la compilación 16179, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).<br/>


### <a name="fixed"></a>Corregido
- No WSL cambia esta semana.

</br>

## <a name="build-16176"></a>Compilación 16176

Para obtener información general sobre Windows sobre la compilación 16176, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).<br/>


### <a name="fixed"></a>Corregido

- [Compatibilidad con serialización habilitada](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- Opción de socket de IP agregada IP_OPTIONS [alvent 1116]
- Función pwritev implementada (al cargar el archivo en nginx/PHP-FPM) [alvent 1506]
- Se han agregado opciones de socket IP IP_MULTICAST_IF & IPV6_MULTICAST_IF [alvent 990]
- Compatibilidad con la opción de socket IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [alvent 1678]
- Se ha agregado la opción de socket _MTU de IP (V6) para el nodo de aplicaciones, traceroute, Dig, nslookup, host
- Opción de socket de IP agregada IPV6_UNICAST_HOPS
- [Mejoras del sistema de archivos](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * Permitir el montaje de rutas UNC
    * Habilitar la compatibilidad con CDFS en drvfs
    * Administrar correctamente los permisos para los sistemas de archivos de red en drvfs
    * Agregar compatibilidad para unidades remotas a drvfs
    * Habilitar la compatibilidad con FAT en drvfs
- Correcciones y mejoras adicionales

### <a name="ltp-results"></a>Resultados de LTP
No hay cambios desde 15042

</br>

## <a name="build-16170"></a>Compilación 16170

Para obtener información general sobre Windows sobre la compilación 16170, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).<br/>

Hemos publicado una nueva [entrada de blog](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) en la que se describen nuestros esfuerzos para probar WSL.

### <a name="fixed"></a>Corregido

- Support socket Option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [alvent 1678]
- Agregar compatibilidad para PTRACE_OLDSETOPTIONS. [ALVENT 1692]
- Correcciones y mejoras adicionales

### <a name="ltp-results"></a>Resultados de LTP
No hay cambios desde 15042

</br>

## <a name="build-15046-to-windows-10-creators-update"></a>Compilación 15046 a Windows 10 Creators Update
No hay más correcciones de WSL o características planeadas para su inclusión en la actualización de Creators en Windows 10. Las notas de la versión de WSL se reanudarán en las próximas semanas para las adiciones destinadas al siguiente Windows Update principal. Para obtener información general sobre Windows sobre la compilación 15046 y futuras versiones de Insider, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/). <br/><br/>
 <br/>

## <a name="build-15042"></a>Compilación 15042

Para obtener información general sobre Windows sobre la compilación 15042, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).<br/>


### <a name="fixed"></a>Corregido

- Corrección para un interbloqueo al quitar una ruta de acceso que termina en ".."
- Se corrigió un problema por el que FIONBIO no devuelve 0 en caso de éxito [alvent 1683]
- Problema corregido con lecturas de longitud cero de sockets de datagramas de inet
- Corrección del posible interbloqueo debido a la condición de carrera en la búsqueda de inode de drvfs [alvent 1675]
- Compatibilidad ampliada con los datos suplementarios de los sockets de UNIX; SCM_CREDENTIALS y SCM_RIGHTS [alvent 514, 613, 1326]
- Correcciones y mejoras adicionales

### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 737</br>
Número de pasos no superados (error, omitido, etc.): 255

</br>

## <a name="build-15031"></a>Compilación 15031

Para obtener información general sobre Windows sobre la compilación 15031, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).<br/>


### <a name="fixed"></a>Corregido

- Se corrigió un error en el que el tiempo (2) se comportó de manera esporádica.
- Problema corregido, donde * SIGPROCMASK llamadas syscall podría dañar la máscara de señal.
- Ahora, devuelva la longitud completa de la línea de comandos en la notificación de creación del proceso WSL. [ALVENT 1632]
- WSL Now informa de la salida del subproceso a través de ptrace para que GDB se bloquee. [ALVENT 1196]
- Se corrigió un error en el que ptys se bloquease después de una gran tmux de e/s [ALVENT 1358]
- Se ha corregido la validación del tiempo de espera en muchas llamadas del sistema (Futex, SEMTIMEDOP, ppoll, sigtimedwait, itimer, timer_create)
- Compatibilidad con eventfd EFD_SEMAPHORE agregada [alvent 452]
- Correcciones y mejoras adicionales

### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 737</br>
Número de pasos no superados (error, omitido, etc.): 255 </br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a>Compilación 15025

Para obtener información general sobre Windows sobre la compilación 15025, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).<br/>


### <a name="fixed"></a>Corregido

- Corrección del error que dañó grep 2,27 [alvent 1578]
- Marca EFD_SEMAPHORE implementada para eventfd2 syscall [alvent 452]
- Implementado/proc/[PID]/net/ipv6_route [alvent 1608]
- Compatibilidad de e/s controlada por señal para Sockets de secuencia de UNIX [alvent 393, 68]
- Compatibilidad con F_GETPIPE_SZ y F_SETPIPE_SZ [alvent 1012]
- Implementar recvmmsg () syscall [alvent 1531]
- Se corrigió un error en el que epoll_wait () no esperaba [alvent 1609]
- Implementación de/proc/version_signature
- Tee syscall ahora devuelve un error si ambos descriptores de archivo hacen referencia a la misma canalización
- Se implementó el comportamiento correcto de SO_PEERCRED para Sockets de UNIX
- Control de parámetros no válidos de tkill de syscall corregidos
- Cambios para aumentar el Preformace de drvfs
- Corrección secundaria para el bloqueo de e/s de Ruby
- Fixed recvmsg () que devuelve EINVAL para la marca MSG_DONTWAIT para Sockets inet [alvent 1296]
- Correcciones y mejoras adicionales

### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 732</br>
Número de pasos no superados (error, omitido, etc.): 255 </br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a>Compilación 15019

Para obtener información general sobre Windows sobre la compilación 15019, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).<br/>


### <a name="fixed"></a>Corregido

- Se corrigió un error que informaba incorrectamente del uso de CPU en procfs para herramientas como htop (alvent 823, 945, 971)
- Al llamar a Open () con O_TRUNC en un archivo existente inotify ahora genera IN_MODIFY antes de IN_OPEN
- Correcciones para el SO_ERROR de sockets de UNIX getsockopt para habilitar Postgress [alvent 61, 1354]
- Implementación de/proc/sys/net/Core/somaxconn para el lenguaje GO
- Apt: la tarea en segundo plano actualizar paquete se ejecuta ahora oculta desde la vista
- Borrar el ámbito de IPv6 localhost (error de la plataforma de Spring Framework (Java)).
- Correcciones y mejoras adicionales

### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 714 </br>
Número de pasos no superados (error, omitido, etc.): 249 </br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a>Compilación 15014

Para obtener información general sobre Windows sobre la compilación 15014, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).<br/>


### <a name="fixed"></a>Corregido

- Ctrl + C ahora funciona según lo previsto
- htop y PS auxw ahora muestran el uso de recursos correcto (alvent #516)
- Traducción básica de las excepciones de NT a las señales. (ALVENT #513)
- fallocate Now genera ENOSPC cuando se está quedando sin espacio en lugar de EINVAL (alvent #1571)
- Agregado/proc/sys/kernel/SEM.
- Llamadas del sistema semop y semtimedop implementadas
- Se corrigieron errores de nslookup con la opción de socket IP_RECVTOS & IPV6_RECVTCLASS (alvent 69)
- Compatibilidad con las opciones de socket IP_RECVTTL y IPV6_RECVHOPLIMIT
- Correcciones y mejoras adicionales

### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 709 </br>
Número de pasos no superados (error, omitido, etc.): 255 </br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a>Resumen de syscall
Llamadas syscall total: 384 </br>
Total implementado: 235 </br>
Total de stubs: 22 </br>
Total no implementado: 127 </br>
[Desglose detallado](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a>Compilación 15007

Para obtener información general sobre Windows sobre la compilación 15007, visite el [blog de Windows]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).<br/>


### <a name="known-issue"></a>Problema conocido

- Hay un error conocido en el que la consola no reconoce algunas teclas Ctrl <key> + Input.  Esto incluye el comando Ctrl-c, que actuará como una KeyPress normal "c".

  - Solución: Asigne una tecla alternativa a Ctrl + C. Por ejemplo, para asignar CTRL + K a Ctrl + C, haga `stty intr \^k`lo siguiente:.  Esta asignación es por terminal y tendrá que realizarse *cada* vez que se inicie bash. Los usuarios pueden explorar la opción para incluirlo en su`.bashrc`

### <a name="fixed"></a>Corregido

- Se corrigió el problema que hacía que la ejecución de WSL consumiera 100% de un núcleo de CPU.
- Ahora se admite la opción de socket IP_PKTINFO, IPV6_RECVPKTINFO. (ALVENT #851, 987)
- Truncar dirección física de la interfaz de red a 16 bytes en lxcore (alvent #1452, 1414, 1343, 468, 308)
- Correcciones y mejoras adicionales

### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 709 </br>
Número de pasos no superados (error, omitido, etc.): 255 </br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a>Compilación 15002

Para obtener información general sobre Windows sobre la compilación 15002, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).<br/>


### <a name="known-issue"></a>Problema conocido

Dos problemas conocidos:
- Hay un error conocido en el que la consola no reconoce algunas teclas Ctrl <key> + Input.  Esto incluye el comando Ctrl-c, que actuará como una KeyPress normal "c".

  - Solución: Asigne una tecla alternativa a Ctrl + C. Por ejemplo, para asignar CTRL + K a Ctrl + C, haga `stty intr \^k`lo siguiente:.  Esta asignación es por terminal y tendrá que realizarse *cada* vez que se inicie bash. Los usuarios pueden explorar la opción para incluirlo en su`.bashrc`

- Mientras se ejecuta WSL, un subproceso del sistema consumirá el 100% de un núcleo de CPU.  La causa raíz se ha solucionado y corregido internamente.

### <a name="fixed"></a>Corregido

- Todas las sesiones de Bash deben crearse ahora en el mismo nivel de permiso.  Se bloqueará el intento de iniciar una sesión en un nivel diferente.  Esto significa que las consolas de administrador y que no son de administración no se pueden ejecutar al mismo tiempo. (ALVENT #626)
<br/>
- Se implementaron los siguientes mensajes NETLINK_ROUTE (requiere el administrador de Windows)
     - RTM_NEWADDR (admite `ip addr add`)
     - RTM_NEWROUTE (admite `ip route add`)
     - RTM_DELADDR (admite `ip addr del`)
     - RTM_DELROUTE (admite `ip route del`)
- La comprobación de tareas programadas para actualizar los paquetes ya no se ejecutará en una conexión de uso medido (alvent #1371)
- Se corrigió un error en el que la canalización se bloquea, es decir, bash-c "LS-alR/" | Bash-c "gato" (alvent #1214)
- Opción de socket TCP_KEEPCNT implementada (alvent #843)
- Opción de socket INET de IP_MTU_DISCOVER implementada (alvent #720, 717, 170, 69)
- Se ha quitado la funcionalidad heredada para ejecutar archivos binarios de NT desde init con búsqueda de rutas NT. (ALVENT #1325)
- Modo de corrección de/dev/KMSG para permitir el acceso de lectura de grupo/otro (0644) (alvent #1321)
- /Proc/sys/kernel/Random/UUID implementado (alvent #1092)
- Error corregido en el que la hora de inicio del proceso se mostraba como año 2432 (alvent #974)
- Variable de entorno de término predeterminado conmutada a xterm-256color (alvent #1446)
- Se modificó la forma en que se calcula la confirmación del proceso durante la bifurcación del proceso. (ALVENT #1286)
- /Proc/sys/VM/overcommit_memory. implementado (ALVENT #1286)
- Archivo/proc/net/Route implementado (alvent #69)
- Error corregido en el que el nombre de acceso directo se ha localizado incorrectamente (alvent #696)
- La lógica de análisis de Elf corregida que valida incorrectamente los encabezados de programa debe ser menor que (o igual a) PATH_MAX. (ALVENT #1048)
- Devolución de llamada de statfs implementada para procfs, sysfs, cgroupfs y binfmtfs (alvent #1378)
- Se han corregido ventanas de AptPackageIndexUpdate que no se cierran (alvent #1184, también se describe en alvent #1193).
- Se ha agregado compatibilidad con la ADDR_NO_RANDOMIZE de ASLR. (ALVENT #1148, 1128)
- Se ha mejorado PTRACE_GETSIGINFO, SIGSEGV, para los seguimientos de la pila gdb adecuados durante el AV (alvent #875)
- Ya no se produce un error en el análisis de ELF para los archivos binarios de patchelf. (ALVENT #471)
- DNS de VPN propagado a/etc/resolv.conf (alvent #416, 1350)
- Mejoras en el cierre de TCP para la transferencia de datos más confiable. (ALVENT #610, 616, 1025, 1335)
- Ahora, devuelva el código de error correcto cuando se abran demasiados archivos (EMFILE). (ALVENT #1126, 2090)
- El registro de auditoría de Windows ahora informa del nombre de la imagen en el proceso de creación de auditoría.
- Ahora se produce un error correctamente al iniciar bash. exe desde una ventana de Bash.
- Mensaje de error agregado cuando Interop no puede obtener acceso a un directorio de trabajo en LxFs (es decir, Notepad. exe. bashrc)
- Se corrigió un problema en el que la ruta de acceso de Windows se truncó en WSL
- Correcciones y mejoras adicionales

### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 690 </br>
Número de pasos no superados (error, omitido, etc.): 274 </br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a>Compatibilidad con syscall
A continuación se muestra una lista de llamadas syscall nuevos o mejorados que tienen alguna implementación en WSL. Los llamadas syscall de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a>Compilación 14986

Para obtener información general sobre Windows sobre la compilación 14986, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).<br/>


### <a name="fixed"></a>Corregido

- Se corrigió bugchecks con NetLink y el ioctl de PTY
- La versión del kernel ahora informa a 4.4.0-43 por coherencia con Xenial
- Bash. exe ahora se inicia cuando la entrada se dirige a ' NUL: ' (alvent #1259)
- Los identificadores de subproceso ahora se han declarado correctamente en procfs (alvent #967)
- IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | Las marcas de IN_ISDIR ahora se admiten en inotify_add_watch () (alvent #1280)
- Implemente timer_create y las llamadas del sistema relacionadas.  Esto habilita la compatibilidad con GHC (alvent #307)
- Se corrigió un problema en el que ping devolvió una hora de 0,000 MS (alvent #1296)
- Devuelve el código de error correcto cuando se abren demasiados archivos.
- Se corrigió un problema en WSL donde la solicitud de NetLink de datos de la interfaz de red generaba un error con EINVAL si la dirección de hardware de la interfaz es de 32 bytes (por ejemplo, la interfaz Teredo)
   - Tenga en cuenta que la utilidad "IP" de Linux contiene un error en el que se bloqueará si WSL informa de una dirección de hardware de 32 bytes. Se trata de un error en "IP", no en WSL. La utilidad "IP" codifica de forma rígida la longitud del búfer de cadena usado para imprimir la dirección de hardware y el búfer es demasiado pequeño para imprimir una dirección de hardware de 32 bytes.
- Correcciones y mejoras adicionales

### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 669 </br>
Número de pasos no superados (error, omitido, etc.): 258 </br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a>Compatibilidad con syscall
A continuación se muestra una lista de llamadas syscall nuevos o mejorados que tienen alguna implementación en WSL. Los llamadas syscall de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a>Compilación 14971

Para obtener información general sobre Windows sobre la compilación 14971, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).<br/>


### <a name="fixed"></a>Corregido

 - Debido a circunstancias más allá de nuestro control, no hay ninguna actualización en esta compilación para el subsistema de Windows para Linux.  Las actualizaciones programadas regularmente se reanudarán en la próxima versión.

### <a name="ltp-results"></a>Resultados de LTP:
Sin cambios desde 14965 </br>
Número de pruebas superadas: 664 </br>
Número de pasos no superados (error, omitido, etc.): 263 </br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a>Compilación 14965

Para obtener información general sobre Windows sobre la compilación 14965, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).<br/>


### <a name="fixed"></a>Corregido

- Compatibilidad con RTM_GETLINK y RTM_GETADDR del protocolo NetLink Sockets NETLINK_ROUTE (alvent #468)
  - Habilita los comandos ifconfig y IP para la enumeración de red
  - Puede encontrar más información en nuestra [entrada de blog sobre redes de WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).

- /sbin está ahora en la ruta de acceso del usuario de forma predeterminada
- La ruta de acceso de usuario de NT ahora se anexa a la ruta de acceso de WSL de forma predeterminada (es decir, ahora puede escribir Notepad. exe sin agregar system32 a la ruta de acceso de Linux)
- Compatibilidad agregada para/proc/sys/kernel/cap_last_cap
- Los archivos binarios de NT ahora se pueden iniciar desde WSL cuando el directorio de trabajo actual contiene caracteres que no son ANSI (alvent #1254)
- Permita el apagado en el socket de flujo UNIX desconectado.
- Compatibilidad agregada para PR_GET_PDEATHSIG.
- Compatibilidad agregada para CLONE_PARENT
- Se corrigió un error en el que la canalización se bloquea, es decir, bash-c "LS-alR/" | Bash-c "gato" (alvent #1214)
- Controle las solicitudes para conectarse al terminal actual.
- Marque/proc/<pid>/oom_score_adj como grabable.
- Agregue la carpeta/sys/FS/cgroup.
- sched_setaffinity debe devolver el número de máscara de bits de afinidad
- Corregir la lógica de validación de ELF que presupone incorrectamente que las rutas de intérprete deben tener menos de 64 caracteres de longitud. (ALVENT #743)
- Los descriptores de archivo abiertos pueden mantener abierta la ventana de consola (alvent #1187)
- Error de Fixeed en el que se produjo un error al cambiar el nombre () con la barra diagonal final en el nombre de destino (alvent #1008)
- Implementar el archivo/proc/net/dev
- Se ha corregido 0,000 MS ping debido a la resolución del temporizador.
- /Proc/Self/ENVIRON implementado (alvent #730)
- Correcciones y mejoras adicionales

### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 664 </br>
Número de pasos no superados (error, omitido, etc.): 263 </br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a>Compilación 14959

Para obtener información general sobre Windows sobre la compilación 14959, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).<br/>


### <a name="fixed"></a>Corregido

- Notificación de proceso pico mejorada para Windows.  Encontrará información adicional en el [blog de WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).
- Estabilidad mejorada con la interoperabilidad de Windows
- Se corrigió el error 0x80070057 al iniciar bash. exe cuando está habilitada la protección de datos empresariales (este)
- Correcciones y mejoras adicionales

### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 665 </br>
Número de pasos no superados (error, omitido, etc.): 263 </br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a>Compilación 14955

Para obtener información general sobre Windows sobre la compilación 14955, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).<br/>


### <a name="fixed"></a>Corregido

 - Debido a circunstancias más allá de nuestro control, no hay ninguna actualización en esta compilación para el subsistema de Windows para Linux.  Las actualizaciones programadas regularmente se reanudarán en la próxima versión.

### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 665 </br>
Número de pasos no superados (error, omitido, etc.): 263 </br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a>Compilación 14951

Para obtener información general sobre Windows sobre la compilación 14951, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).<br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a>Nueva característica: Interoperabilidad con Windows/Ubuntu
Los archivos binarios de Windows ahora se pueden invocar directamente desde la línea de comandos de WSL.  Esto proporciona a los usuarios la capacidad de interactuar con el entorno y el sistema Windows de una manera que no se haya podido realizar.  Como ejemplo rápido, ahora es posible que los usuarios ejecuten los siguientes comandos:

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

Puede encontrar más información en:

- [Blog del equipo de WSL para Interop](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [Documentación de interoperabilidad de MSDN](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a>Corregido

- Ubuntu 16,04 (Xenial) ya está instalado para todas las instancias nuevas de WSL.  Los usuarios con instancias existentes de 14,04 (Trusty) no se actualizarán automáticamente.
- La configuración regional establecida durante la instalación se muestra ahora
- Mejoras de terminal que incluyen un error en el que la redirección de un proceso WSL a un archivo no siempre funciona
- La duración de la consola debe estar asociada a la duración de Bash. exe
- El tamaño de la ventana de la consola debe usar un tamaño visible, no el tamaño del búfer
- Correcciones y mejoras adicionales

### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 665 </br>
Número de pasos no superados (error, omitido, etc.): 263 </br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a>Compilación 14946

Para obtener información general sobre Windows sobre la compilación 14946, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).<br/>


### <a name="fixed"></a>Corregido

- Se corrigió un problema que impedía la creación de cuentas de usuario de WSL para los usuarios con nombres de usuario NT que contienen espacios o comillas. 
- Cambie VolFs y DrvFs para que devuelva 0 para el recuento de vínculos de directorio en STAT
- Compatibilidad con la opción de socket IPV6_MULTICAST_HOPS.
- Limite a un bucle de e/s de consola única por TTY. Ejemplo: el siguiente comando es posible:
  - Bash-c "datos de Eco" | Bash-c "ssh user@example.com " cat > foo. txt ' "

- reemplazar espacios con pestañas en/proc/cpuinfo (alvent #1115)
- DrvFs aparece ahora en mountinfo con un nombre que coincide con el volumen de Windows montado
- /Home y/root ahora aparecen en mountinfo con los nombres correctos
- Correcciones y mejoras adicionales

### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 665 </br>
Número de pasos no superados (error, omitido, etc.): 263 </br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a>Compilación 14942

Para obtener información general sobre Windows sobre la compilación 14942, visite el [blog de Windows](https://aka.ms/onefourninefourtwoooooo).<br/>


### <a name="fixed"></a>Corregido

- Un número de bugchecks direccionado, incluido el bloqueo de red "intento de ejecución de memoria noexecute" que bloqueaba SSH
- la compatibilidad de inotifiy con las notificaciones generadas desde aplicaciones Windows en DrvFs ahora está en
- Implemente TCP_KEEPIDLE y TCP_KEEPINTVL para mongod. (ALVENT #695)
- Implementar la llamada del sistema pivot_root
- Opción de implementación de socket para SO_DONTROUTE
- Correcciones y mejoras adicionales


### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 665 </br>
Número de pasos no superados (error, omitido, etc.): 263 </br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a>Compatibilidad con syscall
A continuación se muestra una lista de llamadas syscall nuevos o mejorados que tienen alguna implementación en WSL. Los llamadas syscall de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a>Compilación 14936

Para obtener información general sobre Windows sobre la compilación 14936, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).<br/>


Nota: WSL instalará Ubuntu versión 16,04 (Xenial) en lugar de Ubuntu 14,04 (Trusty) en una próxima versión.  Este cambio se aplicará a la instalación de instancias nuevas (lxrun. exe/Install o a la primera ejecución de Bash. exe).  Las instancias existentes con confianza no se actualizarán automáticamente. Los usuarios pueden actualizar su imagen de confianza a Xenial mediante el comando do-Release-upgrade.

### <a name="known-issue"></a>Problema conocido
WSL está experimentando un problema con algunas implementaciones de Sockets.  La comprobación de errores se manifiesta como un bloqueo con el error "intento de ejecución de la memoria noexecute".  La manifestación más común de este problema es un bloqueo cuando se usa SSH.  La causa principal se ha corregido en las compilaciones internas y se insertará en la parte más temprana de la oportunidad.

### <a name="fixed"></a>Corregido

- Implementación de la llamada del sistema chroot
- Mejoras en inotify ~~, incluida la compatibilidad con notificaciones generadas desde aplicaciones Windows en DrvFs~~
  - Corregir La compatibilidad de inotify con los cambios que se originan en aplicaciones Windows no están disponibles en este momento.
- Enlace de socket a IPv6:<port n> : ahora admite IPV6_V6ONLY (alvent #68, #157, #393, #460, #674, #740, #982, #996)
- Comportamiento de WNOWAIT para waitid systemcall implementado (alvent #638)
- Compatibilidad con las opciones de socket de IP IP_HDRINCL y IP_TTL
- La lectura de longitud cero () debe volver inmediatamente (alvent #975)
- Administrar correctamente los nombres de archivo y los prefijos de nombre de archivo que no incluyen un terminador NULL en un archivo. tar.
- compatibilidad con epoll para/dev/null
- Corregir origen de hora de/dev/Alarm
- Bash-c ahora puede redirigir a un archivo
- Correcciones y mejoras adicionales

### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 664 </br>
Número de pasos no superados (error, omitido, etc.): 264 </br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a>Compatibilidad con syscall
A continuación se muestra una lista de llamadas syscall nuevos o mejorados que tienen alguna implementación en WSL. Los llamadas syscall de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.

`chroot`<br/>
<br/>

## <a name="build-14931"></a>Compilación 14931

Para obtener información general sobre Windows sobre la compilación 14931, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).<br/>


### <a name="fixed"></a>Corregido

 - Debido a circunstancias más allá de nuestro control, no hay ninguna actualización en esta compilación para el subsistema de Windows para Linux.  Las actualizaciones programadas regularmente se reanudarán en la próxima versión.

<br/>

## <a name="build-14926"></a>Compilación 14926

Para obtener información general sobre Windows sobre la compilación 14926, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).<br/>


### <a name="fixed"></a>Corregido

- Ping Now funciona en consolas que no tienen privilegios de administrador
- También se admite Ping6, sin privilegios de administrador.
- Compatibilidad de inotify con archivos modificados a través de WSL. (ALVENT #216)
  - Marcas admitidas:
    - inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK
    - eventos de inotify_add_watch: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF
    - atributos inotify_add_watch: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR
    - salida de lectura: LX_IN_ISDIR, LX_IN_IGNORED
  - Problema conocido: La modificación de archivos desde aplicaciones Windows no genera ningún evento
- El socket de UNIX ahora es compatible con SCM_CREDENTIALS

### <a name="ltp-results"></a>Resultados de LTP:
Número de pruebas superadas: 651 </br>
Número de pasos no superados (error, omitido, etc.): 258 </br>
[Registros de ejecución de pruebas de LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a>Compilación 14915

Para obtener información general sobre Windows sobre la compilación 14915, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).<br/>


### <a name="fixed"></a>Corregido
-  Socketpair para Sockets de datagramas UNIX (alvent #262)
- Compatibilidad con el socket de UNIX para SO_REUSEADDR
- Compatibilidad con el socket de UNIX para SO_BROADCAST (alvent #568)
- Compatibilidad con el socket de UNIX para SOCK_SEQPACKET (alvent #758, #546)
- Adición de compatibilidad para el envío, recepción y cierre de sockets de datagramas de UNIX
- Corrección de BugCheck debido a la validación de parámetros mmap no válidos para direcciones no fijas. (ALVENT #847)
- Compatibilidad para suspender o reanudar los Estados de terminal
- Compatibilidad con TIOCPKT ioctl para desbloquear la utilidad de pantalla (alvent #774)
    - Problema conocido: Teclas de función no operativas
- Se corrigió una carrera en TimerFd que podía hacer que un miembro liberado ' ReaderReady ' estuviera accesible para LxpTimerFdWorkerRoutine (alvent #814)
- Habilitar la compatibilidad con llamadas del sistema reiniciables para Futex, Poll y clock_nanosleep
- Compatibilidad con montaje de enlace agregado
- dejar de compartir la compatibilidad con el espacio de nombres Mount
    - Problema conocido: Al crear un nuevo espacio de nombres `unshare(CLONE_NEWNS)` de montaje con el directorio de trabajo actual, continuará señalando al espacio de nombres anterior
- Mejoras y correcciones de errores adicionales

<br/>

## <a name="build-14905"></a>Compilación 14905

Para obtener información general sobre Windows sobre la compilación 14905, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).<br/>


### <a name="fixed"></a>Corregido
- Ahora se admiten llamadas del sistema reiniciables (alvent #349, alvent #520)
- Vínculos simbólicos a directorios que terminan en/ahora operativo (alvent #650)
- RNDGETENTCNT ioctl implementado para/dev/random
- Se implementaron los archivos/proc/[PID]/mounts,/proc/[PID]/mountinfo y/proc/[PID]/mountstats
- Correcciones y mejoras adicionales

</br>

## <a name="build-14901"></a>Compilación 14901
Primera compilación Insider para la versión posterior de la actualización de aniversario de Windows 10.

Para obtener información general sobre Windows sobre la compilación 14901, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).<br/>


### <a name="fixed"></a>Corregido
- Problema de barra diagonal final corregida
    - Comandos como `$ mv a/c/ a/b/` Now Work
- Al instalar ahora se le pregunta si la configuración regional de Ubuntu debe establecerse en configuración regional de Windows.
- Compatibilidad con procfs para la carpeta NS
- Se ha agregado el montaje y el desmontaje de los sistemas de archivos tmpfs, procfs y sysfs
- Fix mknod [at] firma ABI de 32 bits
- Los sockets Unix se movieron al modelo Dispatch
- Se debe respetar el tamaño del búfer de recepción del socket de INET mediante el valor de la memoria
- Implementar la marca de mensaje de recepción de socket Unix MSG_CMSG_CLOEXEC
- Redirección de canalización stdin/stdout de proceso de Linux (alvent #2)
    - Permite la canalización de comandos Bash-c en CMD.  Ejemplo: > dir | Bash-c "grep foo"
- Bash ahora se puede instalar en sistemas con varios webfilesystems (alvent #538, #358)
- El tamaño predeterminado del búfer del socket de INET debe coincidir con el de la configuración predeterminada de Ubuntu
- Alinee xattr llamadas syscall con listxattr
- Solo se devuelven interfaces con una dirección IPv4 válida de SIOCGIFCONF
- Corregir la acción predeterminada de la señal cuando se inserta por ptrace
- implementación de/proc/sys/VM/min_free_kbytes
- Usar valores de registro de contexto de equipo al restaurar el contexto en sigreturn
    - Esto resuelve el problema por el que Java y javac estaban bloqueados para algunos usuarios
- Implementación de/proc/sys/kernel/hostname

### <a name="syscall-support"></a>Compatibilidad con syscall
A continuación se muestra una lista de llamadas syscall nuevos o mejorados que tienen alguna implementación en WSL. Los llamadas syscall de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a>Compilación 14388 a actualización de aniversario de Windows 10
Para obtener información general sobre Windows sobre la compilación 14388, visite el [blog de Windows](https://aka.ms/14388wip). <br/>

### <a name="fixed"></a>Corregido
- Correcciones para preparar la actualización de aniversario de Windows 10 en 8/2
  - Puede encontrar más información sobre WSL en la actualización de aniversario en nuestro [blog](https://blogs.msdn.microsoft.com/wsl/) .

<br/>

## <a name="build-14376"></a>Compilación 14376
Para obtener información general sobre Windows sobre la compilación 14376, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/). <br/>

### <a name="fixed"></a>Corregido
- Se quitaron algunas instancias en las que apt-get se bloquea (alvent #493)
- Se corrigió un problema por el que los montajes vacíos no se controlaban correctamente
- Se corrigió un problema por el que los ramdisk no se montaron correctamente
- Cambiar aceptación de socket de UNIX a marcas de compatibilidad (alvent parciales #451)
- Pantalla desazul relacionada con la red común fija
- Se corrigió la pantalla azul al obtener acceso a/proc/[PID]/secuencias (alvent #523)
- Se corrigió un uso elevado de la CPU en algunos escenarios de PTY (alvent #488, #504)
- Correcciones y mejoras adicionales

<br/>

## <a name="build-14371"></a>Compilación 14371
Para obtener información general sobre Windows sobre la compilación 14371, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/). <br/>

### <a name="fixed"></a>Corregido
- Se corrigió la carrera de tiempo con SIGCHLD y wait () al usar ptrace
- Corrección de un comportamiento cuando las rutas de acceso tienen una o varias #432
- Se corrigió un problema con el error de cambio de nombre o desvinculación debido a identificadores abiertos a elementos secundarios
- Correcciones y mejoras adicionales

<br/>

## <a name="build-14366"></a>Compilación 14366
Para obtener información general sobre Windows sobre la compilación 14366, visite el [blog de Windows](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/). <br/>

### <a name="fixed"></a>Corregido
- Corrección en la creación de archivos mediante vínculos simbólicos
-   Se ha agregado listxattr para Python (alvent 385)
-   Correcciones y mejoras adicionales

### <a name="syscall-support"></a>Compatibilidad con syscall
-   A continuación se muestra una lista de llamadas syscall nuevos o mejorados que tienen alguna implementación en WSL. Los llamadas syscall de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.

`listxattr`<br/>
<br/>

## <a name="build-14361"></a>Compilación 14361
Para obtener información general sobre Windows sobre la compilación 14361, visite el [blog de Windows](https://aka.ms/wip14361). <br/>

### <a name="fixed"></a>Corregido
- DrvFs ahora distingue entre mayúsculas y minúsculas cuando se ejecuta en bash en Ubuntu en Windows.
  - Los usuarios pueden Case. txt y CASE. TXT en sus unidades de/mnt/c
  - La distinción de mayúsculas y minúsculas solo se admite en bash en Ubuntu en Windows. Cuando esté fuera de Bash, NTFS notificará los archivos correctamente, pero puede producirse un comportamiento inesperado que interactúe con los archivos de Windows.
  - La raíz de cada volumen (es decir,/mnt/c) no distingue entre mayúsculas y minúsculas
  - Puede encontrar más información sobre el control de estos archivos en Windows [aquí](https://support.microsoft.com/en-us/kb/100625).
- Compatibilidad con PTY/TTY considerablemente mejorada.  Ahora se admiten aplicaciones como TMUX (alvent #40)
- Se corrigió el problema de instalación de las cuentas de usuario que no siempre se han creado
- Estructura de argumentos de línea de comandos optimizada que permite una lista de argumentos extremadamente larga. (ALVENT #153)
- Ahora puede eliminar y chmod archivos READ_ONLY de DrvFs
- Se corrigieron algunos casos en los que el terminal se bloquea en la desconexión (alvent #43)
- chmod y chown ahora funcionan en dispositivos TTY
- Permitir la conexión a 0.0.0.0 y:: como localhost (alvent #388)
- Sendmsg/recvmsg ahora administra una longitud de vector de e/s de > 1 (#376 parciales)
- Los usuarios ahora pueden dejar de participar en el archivo de hosts generados automáticamente (alvent #398)
- Coincidencia automática de la configuración regional de Linux con la configuración regional de NT durante la instalación (alvent #11)
- Se ha agregado el archivo/proc/sys/vm/swappiness (alvent #306)
- strace ahora se cierra correctamente
- Permitir que las canalizaciones se vuelvan a abrir a través de/proc/Self/FD (alvent #222)
- Ocultar directorios en%LOCALAPPDATA%\lxss de DrvFs (alvent #270)
- Mejor control de Bash. exe ~.  Ahora se admiten comandos como "Bash ~-c LS" (alvent #467)
- Ahora, los sockets notifican a epoll Read disponibles durante el cierre (alvent #271)
- lxrun/Uninstall mejora el trabajo de eliminación de archivos y carpetas
- Se corrigió PS-f (alvent #246)
- Compatibilidad mejorada con aplicaciones X11 como xEmacs (alvent #481)
- Se ha actualizado el tamaño inicial de la pila de subprocesos para que coincida con la configuración predeterminada de Ubuntu y se notifica el tamaño correctamente a get_rlimit syscall (alvent #172, #258)
- Informes mejorados de nombres de imagen de proceso pico (por ejemplo, para auditoría)
- Comando implementado/proc/mountinfo para DF
- Código de error de symlink fijo para el nombre secundario. y.
- Mejoras correcciones y mejoras adicionales

### <a name="syscall-support"></a>Compatibilidad con syscall
A continuación se muestra una lista de llamadas syscall nuevos o mejorados que tienen alguna implementación en WSL. Los llamadas syscall de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a>Compilación 14352
Para obtener información general sobre Windows sobre la compilación 14352, visite el [blog de Windows](https://aka.ms/wip14352).<br/>


### <a name="fixed"></a>Corregido
- Se corrigió un problema en el que los archivos grandes no se descargaron o se crearon correctamente.  Esto debe desbloquear NPM y otros escenarios (alvent #3, alvent #313)
- Se quitaron algunas instancias en las que los sockets no responden
- Se corrigieron algunos errores de ptrace
- Problema corregido con WSL que permite nombres de archivo de más de 255 caracteres
- Compatibilidad mejorada para caracteres que no están en inglés
- Agregar datos de zona horaria de Windows actuales y establecer como valores predeterminados
- ID. de dispositivo único para cada punto de montaje (corrección de JRE – alvent #49)
- Corregir el problema con las rutas de acceso que contienen "." y ".."
- Compatibilidad con FIFO agregada (alvent #71)
- Formato actualizado de resolv. conf para que coincida con el formato Ubuntu nativo
- Algunas limpiezas de procfs
- Habilitación del ping para consolas de administrador (alvent #18)

### <a name="syscall-support"></a>Compatibilidad con syscall
A continuación se muestra una lista de llamadas syscall nuevos o mejorados que tienen alguna implementación en WSL. Los llamadas syscall de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a>Compilación 14342
Para obtener información general sobre Windows sobre la compilación 14342 el [blog de Windows](https://aka.ms/wip14342). <br/>

Puede encontrar información sobre VolFs y DriveFs en el [blog de WSL](https://blogs.msdn.microsoft.com/wsl). <br/>

### <a name="fixed"></a>Corregido
- Se corrigió el problema de instalación cuando el usuario de Windows tenía caracteres Unicode en el nombre de usuario
- La solución de udev de actualización apt-get en las preguntas más frecuentes se proporciona ahora de forma predeterminada en la primera ejecución.
- Vínculos simbólicos habilitados en<drive>directorios DriveFs (/mnt/)
- Los vínculos simbólicos funcionan ahora entre DriveFs y VolFs
- Problema de análisis de ruta de acceso de nivel superior solucionado: LS.//funcionará ahora como se esperaba
- la instalación de NPM en DriveFs y las opciones-g ahora funcionan
- Se corrigió un problema que impide que se inicie el servidor PHP
- Valores de entorno predeterminados actualizados, como $PATH para que coincidan con Ubuntu nativo
- Se ha agregado una tarea de mantenimiento semanal en Windows para actualizar la caché de paquetes apt
- Problema corregido con la validación de encabezado de ELF, WSL ahora es compatible con todas las opciones de Melkor
- El shell de zsh es funcional
- Ahora se admiten los binarios de go precompilados
- Preguntar en bash. exe la primera ejecución ahora está localizada correctamente
- /proc/meminfo Now devuelve la información correcta
- Sockets admitidos ahora en VFS
- /dev ahora montado como tempfs
- Ahora se admite FIFO
- Los sistemas de varios núcleos ahora se muestran correctamente en/proc/cpuinfo
- Mejoras adicionales y mensajes de error que se descargan durante la primera ejecución
- Mejoras de syscall y correcciones. Lista de syscall admitida a continuación.
- Correcciones y mejoras adicionales

### <a name="known-issues"></a>Problemas conocidos
- No se resuelve '.. ' correctamente en DriveFs en algunos casos

### <a name="syscall-support"></a>Compatibilidad con syscall
A continuación se muestra una lista de llamadas syscall nuevos o mejorados que tienen alguna implementación en WSL. Los llamadas syscall de esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.

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

Para obtener información general sobre Windows sobre la compilación 14332, visite el [blog de Windows](https://aka.ms/wip14332). <br/>


### <a name="fixed"></a>Corregido
- Mejor generación de resolv. conf, incluida la priorización de entradas DNS
- Problema con el traslado de archivos y directorios entre las unidades de/mnt y no/mnt
- Los archivos tar ahora se pueden crear con vínculos simbólicos
- Se agregó el directorio/Run/Lock predeterminado en la creación de la instancia
- Actualice/dev/null para que devuelva la información de estadísticas correcta
- Errores adicionales al descargar durante la primera ejecución
- Mejoras de syscall y correcciones. Lista de syscall admitida a continuación.
- Mejoras correcciones y mejoras adicionales

### <a name="syscall-support"></a>Compatibilidad con syscall
A continuación se muestra el nuevo syscall que tiene alguna implementación en WSL. El syscall de esta lista se admite en al menos un escenario, pero es posible que no tenga todos los parámetros admitidos en este momento.

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a>Compilación 14328

Para obtener información general sobre Windows sobre la compilación 14332, visite el [blog de Windows](https://aka.ms/wip14328). <br/>


### <a name="new-features"></a>Nuevas características
* Ahora admite usuarios de Linux.  Al instalar bash en Ubuntu en Windows, se solicitará la creación de un usuario de Linux.  Para obtener más información, visite https://aka.ms/wslusers
* El nombre de host ahora está establecido en el nombre del equipo de Windows, no más@localhost
* Para obtener más información sobre la compilación 14328, visite: https://aka.ms/wip14328

### <a name="fixed"></a>Corregido
* Mejoras de symlink para archivos<drive> no/mnt/
    * la instalación de NPM funciona ahora
    * JDK/JRE ahora se instala mediante las instrucciones que se encuentran [aquí](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).
    * problema conocido: los vínculos simbólicos no funcionan para los montajes de Windows.  La funcionalidad estará disponible en una compilación posterior
* Top y htop ahora se muestran
* Mensajes de error adicionales para algunos errores de instalación
* Mejoras de syscall y correcciones.  Lista de syscall admitida a continuación.
* Mejoras correcciones y mejoras adicionales

### <a name="syscall-support"></a>Compatibilidad con syscall
A continuación se muestra una lista de llamadas syscall que tienen alguna implementación en WSL.  Llamadas syscall en esta lista se admiten en al menos un escenario, pero puede que no se admitan todos los parámetros en este momento.

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
