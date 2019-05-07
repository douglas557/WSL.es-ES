---
title: Notas de la versión para el subsistema de Windows para Linux
description: Notas de la versión para el subsistema de Windows para Linux.  Se actualiza semanalmente.
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, windowssubsystem, ubuntu
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.openlocfilehash: 2567e68ca0e9897a7b7bc7315760b81ff4923c1a
ms.sourcegitcommit: 8c74868b8d8ff0106e15e4bce5e8337642883ec1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/01/2019
ms.locfileid: "64988264"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a>Notas de la versión para el subsistema de Windows para Linux

## <a name="build-18890"></a>Compilación 18890
Para Windows general, visite información sobre las compilación 18890 el [blog Windows](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).

### <a name="wsl"></a>WSL
* Pérdida de socket de no bloqueo [GH 2913]
* Entrada EOF al terminal puede bloquear las lecturas subsiguientes [GH 3421]
* Actualizar resolv.conf encabezado para hacer referencia a wsl.conf [descritos en GH 3928]
* Interbloqueo en epoll eliminar código [GH 3922]
* Controlar los espacios en los argumentos--importar y – exportar [GH 3932]
* Archivos de extensión mmap no funciona correctamente [GH 3939]
* Solución de problemas con ARM64 \\acceso de $ wsl no funciona correctamente
* Agregar una mejor icono predeterminado para wsl.exe

## <a name="build-18342"></a>Compilación 18342
Para Windows general, visite información sobre las compilación 18342 el [blog Windows](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).

### <a name="wsl"></a>WSL
* Hemos agregado la capacidad de los usuarios tener acceso a los archivos de Linux en una distribución de WSL desde Windows. Estos archivos pueden obtenerse a través de la línea de comandos, además de aplicaciones de Windows, como el Explorador de archivos, VSCode, etc. puede interactuar con estos archivos. Acceder a los archivos, vaya a \\ \\wsl$\\< distro_name >, o ver una lista de distribuciones en ejecución, vaya a \\ \\wsl$
* Agregar etiquetas de información adicionales de CPU y corregir los valores de Cpus_allowed [_lista] [GH 2234]
* Admite la ejecución del subproceso que no sean líder [GH 3800]
* Tratar errores de actualización de configuración como recuperable [GH 3785]
* Actualizar binfmt para controlar correctamente los desplazamientos [GH 3768]
* Habilitar asignación las unidades de red para planear 9 [GH 3854]
* Linux -> el soporte técnico de Windows y Linux -> traducción de la ruta de acceso de Windows para montajes de enlace
* Crear secciones de solo lectura para las asignaciones en los archivos abiertos de solo lectura

## <a name="build-18334"></a>Compilación 18334
Para Windows general, visite información sobre las compilación 18334 el [blog Windows](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).

### <a name="wsl"></a>WSL
* Diseñar la forma en que la zona horaria de Windows se asigna a una zona horaria de Linux [GH 3747]
* Corregir las pérdidas de memoria y agregar nuevas funciones de conversión de cadena [GH 3746]
* SIGCONT en un threadgroup sin subprocesos es una operación inefectiva [GH 3741] 
* Mostrar correctamente los descriptores de archivo de socket y epoll en /proc/self/fd

## <a name="build-18305"></a>Compilación 18305
Para Windows general, visite información sobre las compilación 18305 el [blog Windows](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).

### <a name="wsl"></a>WSL
* pthreads perder el acceso a los archivos cuando el subproceso principal finaliza [GH 3589]
* TIOCSCTTY debe omitir el parámetro "force" a menos que sea necesario [GH 3652]
* mejoras de la línea de comandos de wsl.exe y adición de importación / exportación de funcionalidad.
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
Para Windows general, visite información sobre las compilación 18277 el [blog Windows](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).

### <a name="wsl"></a>WSL
* Corregir el error "no se admite dicha interfaz" introducido en la compilación 18272 [GH 3645]
* Omitir el indicador MNT_FORCE para umount syscall [GH 3605]
* Cambie la interoperabilidad WSL para usar la API CreatePseudoConsole oficial
* No mantener ningún valor de tiempo de espera cuando se reinicia FUTEX_WAIT

## <a name="build-18272"></a>Compilación 18272
Para Windows general, visite información sobre las compilación 18272 el [blog Windows](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).

### <a name="wsl"></a>WSL
* **ADVERTENCIA:** Hay un problema en esta compilación que hace WSL no funciona. Al intentar iniciar la distribución verá un error "No se admite dicha interfaz". El problema se ha corregido y estará en la compilación de Insider rápida de la próxima semana. Si ha instalado esta compilación puede revertir a la compilación anterior de Windows mediante "Ir a la versión anterior de Windows 10" en Configuración -> actualización de & seguridad -> recuperación.

## <a name="build-18267"></a>Compilación 18267
Para Windows general información en la compilación 18267, visite la [blog Windows](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).

### <a name="wsl"></a>WSL
* Corregir el problema donde el proceso inerte no puede ser reaped y permanecer indefinidamente.
* WslRegisterDistribution se bloquea si el mensaje de error supera la longitud máxima [GH 3592]
* Permitir fsync para archivos de solo lectura en DrvFs [GH 3556]
* Asegúrese de que existen los directorios /bin y/sbin antes de crear vínculos simbólicos dentro de [GH 3584]
* Agregar un mecanismo de tiempo de espera de finalización de instancia para las instancias WSL. Actualmente, el tiempo de espera se establece en 15 segundos, lo que significa que la instancia cerrará en 15 segundos después de que salga el último proceso WSL. Para finalizar una distribución de inmediato, use:
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a>Compilar 17763 (1809)
Para Windows general, visite información sobre las compilación 17763 el [blog Windows](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).

### <a name="wsl"></a>WSL
* Comprobación de permisos de syscall SetPriority demasiado estricto para cambiar la misma prioridad de subproceso [GH 1838]
* Garantizar que el tiempo de interrupción no sesgada se usa durante el tiempo de arranque para evitar la devolución de los valores negativos para clock_gettime(CLOCK_BOOTTIME) [GH 3434]
* Controlar los vínculos simbólicos en el intérprete WSL binfmt [GH 3424]
* Un mejor control de limpieza del descriptor de archivo de threadgroup líder.
* Cambiar WSL usar KeQueryInterruptTimePrecise en lugar de KeQueryPerformanceCounter del núcleo para evitar el desbordamiento [GH 3252]
* Ptrace adjuntar se puede hacer que el valor devuelto incorrecto de llamadas del sistema [GH 1731]
* Revisión relacionada con varios AF_UNIX emite [GH 3371]
* Corregir el problema que podría provocar la interoperabilidad WSL para producir un error si el directorio de trabajo actual es menor que 5 caracteres de longitud [GH 3379]
* Evitar un retraso segundo errores en las conexiones de bucle invertido para puertos inexistente [GH 3286]
* Add /proc/sys/fs/file-max stub file [GH 2893]
* Información más precisa del ámbito de IPV6.
* Soporte técnico PR_SET_PTRACER [GH 3053]
* Sistema de archivos de canalización borrado accidentalmente epoll edge desencadenadas por eventos [GH 3276]
* Ejecutable de Win32 iniciada a través de vínculos simbólicos NTFS no respeta el nombre de vínculo simbólico [GH 2909]
* Mejorado soporte inerte [GH 1353]
* Agregar entradas wsl.conf para controlar el comportamiento de interoperabilidad de Windows [GH 1493]
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* Corrección de getsockname no siempre devuelve el tipo de familia de socket de UNIX [GH 1774]
* Agregar compatibilidad para TIOCSTI [GH 1863]
* Sockets de no bloqueo en el proceso de conexión deben devolver EAGAIN para intentos de escritura [GH 2846]
* Admitir la interoperabilidad en los discos duros virtuales montados [GH 3246, 3291]
* Corregir el problema en la carpeta raíz [GH 3304] la comprobación de permiso
* Compatibilidad limitada para TTY teclado IOCTL KDGKBTYPE, KDGKBMODE y KDSKBMODE.
* Incluso cuando se inicia en segundo plano, deben ejecutar las aplicaciones de interfaz de usuario de Windows.
* Agregue la opción -u o--usuario wsl [GH 1203]
* Solucionar problemas de inicio WSL cuando se habilita el inicio rápido [GH 2576]
* Sockets de UNIX necesitan conservar las credenciales de desconectada del mismo nivel [GH 3183]
* Sockets de Unix sin bloqueo presentan indefinidamente EAGAIN [GH 3191]
* caso = off es el nuevo drvfs predeterminada montar tipo [GH 2937, 3212, 3328]
    * Consulte [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) para obtener más información.
* Agregar wslconfig / terminate para detener la ejecución de las distribuciones.
* Corregir el problema con el contexto del shell WSL entradas de menú que no administren correctamente las rutas de acceso con espacios.
* Exponer entre mayúsculas y minúsculas por directorio como un atributo extendido
* ARM64: Emular las operaciones de mantenimiento de caché. Resolver [dotnet problema](https://github.com/dotnet/core/issues/1561).
* DrvFs: unescape solo caracteres del intervalo privado que corresponden a un carácter de escape.
* Corregir el error de off a uno en la validación de longitud de intérprete de ELF analizador [GH 3154]
* Los temporizadores en absoluto con un tiempo en el pasado WSL no activan [GH 3091]
* Asegúrese de recién puntos de reanálisis creado se muestran como tal en el directorio primario.
* Crear atómicamente directorios distingue mayúsculas de minúsculas en DrvFs.
* Se corrigió un problema adicional que podrían devolver operaciones multiproceso ENOENT aunque exista el archivo. [GH 2712]
* WSL fijo iniciar un error cuando se habilita UMCI. [GH 3020]
* Agregar el menú contextual del explorador para iniciar WSL [GH 437, 603, 1836]. Para usar, mantenga presionada la tecla MAYÚS y haga doble clic en una ventana del explorador.
* Corregir el comportamiento de no bloqueo del socket de Unix [GH 2822, 3100]
* Corrección de francesa comando NETLINK notificados en 2026 GH.
* Agregar compatibilidad con marcadores de propagación de montaje [GH 2911].
* Corregir el problema con truncate que no producen inotify eventos [GH 2978].
* Agregue--opción exec para wsl.exe invocar un solo archivo binario sin un shell.
* Agregar: opción de distribución para wsl.exe seleccionar una distribución específica.
* Compatibilidad limitada con dmesg. Las aplicaciones ahora pueden iniciar en dmesg. Controlador WSL registra información limitada a dmesg. En el futuro, esto puede ampliarse para llevar a cabo otros información/diagnósticos desde el controlador.
    * Nota: dmesg actualmente se admite a través de la `/dev/kmsg` la interfaz de dispositivo. `syslog` interfaz syscall aún no se admite. Y, por lo tanto, algunos de los `dmesg` opciones de línea de comandos tales como `-S`, `-C` no funcionan.
* Cambiar el gid de forma predeterminada y el modo de dispositivos serie para que coincida con nativo [GH 3042]
* DrvFs ahora es compatible con atributos extendidos.
    * Nota: DrvFs tiene algunas limitaciones en el nombre de los atributos extendidos. Algunos caracteres (como '/', ':' y '\*') no están permitidos y extendido los nombres de atributo no distinguen mayúsculas de minúsculas en DrvFs

## <a name="build-18252-skip-ahead"></a>Compilación 18252 (Saltar adelante)
Para Windows general, visite información sobre las compilación 18252 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).

### <a name="wsl"></a>WSL
* Mover los archivos binarios de init y bsdtar lxssmanager dll y a una carpeta de herramientas independientes
* Corregir la carrera en torno a cerrar el descriptor de archivo cuando se usa CLONE_FILES
* Administrar campos opcionales en /proc/pid/mountinfo al traducir las rutas de acceso DrvFs
* Permitir DrvFs mknod se realice correctamente sin compatibilidad con metadatos para S_IFREG
* Archivos de solo lectura creados en DrvFs deben tener el atributo de solo lectura establezca [GH 3411]
* Agregar aplicación auxiliar /sbin/mount.drvfs para controlar el montaje DrvFs
* Use el cambio de nombre POSIX de DrvFs.
* Permitir traducción de la ruta de acceso en los volúmenes sin un GUID de volumen.

## <a name="build-17738-fast"></a>Compilar 17738 (Fast)
Para Windows general, visite información sobre las compilación 17738 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).

### <a name="wsl"></a>WSL
* Comprobación de permisos de syscall SetPriority demasiado estricto para cambiar la misma prioridad de subproceso [GH 1838]
* Garantizar que el tiempo de interrupción no sesgada se usa durante el tiempo de arranque para evitar la devolución de los valores negativos para clock_gettime(CLOCK_BOOTTIME) [GH 3434]
* Controlar los vínculos simbólicos en el intérprete WSL binfmt [GH 3424]
* Un mejor control de limpieza del descriptor de archivo de threadgroup líder.

## <a name="build-17728-fast"></a>Compilar 17728 (Fast)
Para Windows general, visite información sobre las compilación 17728 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).

### <a name="wsl"></a>WSL
* Cambiar WSL usar KeQueryInterruptTimePrecise en lugar de KeQueryPerformanceCounter del núcleo para evitar el desbordamiento [GH 3252]
* Ptrace adjuntar se puede hacer que el valor devuelto incorrecto de llamadas del sistema [GH 1731]
* Revisión relacionada con un número de AF_UNIX emite [GH 3371]
* Corregir el problema que podría provocar la interoperabilidad WSL para producir un error si el directorio de trabajo actual es menor que 5 caracteres de longitud [GH 3379]

## <a name="build-18204-skip-ahead"></a>Compilación 18204 (Saltar adelante)
Para Windows general, visite información sobre las compilación 18204 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).

### <a name="wsl"></a>WSL
* Canalizar inadvertenly filesystem borrar epoll edge desencadenadas por eventos [GH 3276]
* Ejecutable de Win32 iniciada a través de vínculos simbólicos NTFS no respeta el nombre de vínculo simbólico [GH 2909]

## <a name="build-17723-fast"></a>Compilar 17723 (Fast)
Para Windows general, visite información sobre las compilación 17723 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).

### <a name="wsl"></a>WSL
* Evitar un retraso segundo errores en las conexiones de bucle invertido para puertos inexistente [GH 3286]
* Add /proc/sys/fs/file-max stub file [GH 2893]
* Información más precisa del ámbito de IPV6.
* Soporte técnico PR_SET_PTRACER [GH 3053]
* Canalizar inadvertenly filesystem borrar epoll edge desencadenadas por eventos [GH 3276]
* Ejecutable de Win32 iniciada a través de vínculos simbólicos NTFS no respeta el nombre de vínculo simbólico [GH 2909]

## <a name="build-17713"></a>Compilación 17713
Para Windows general, visite información sobre las compilación 17713 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).

### <a name="wsl"></a>WSL
* Mejorado soporte inerte [GH 1353]
* Agregar entradas wsl.conf para controlar el comportamiento de interoperabilidad de Windows [GH 1493]
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* Corrección de getsockname no siempre devuelve el tipo de familia de socket de UNIX [GH 1774]
* Agregar compatibilidad para TIOCSTI [GH 1863]
* Sockets de no bloqueo en el proceso de conexión deben devolver EAGAIN para intentos de escritura [GH 2846]
* Admitir la interoperabilidad en los discos duros virtuales montados [GH 3246, 3291]
* Corregir el problema en la carpeta raíz [GH 3304] la comprobación de permiso
* Compatibilidad limitada para TTY teclado IOCTL KDGKBTYPE, KDGKBMODE y KDSKBMODE.
* Incluso cuando se inicia en segundo plano, deben ejecutar las aplicaciones de interfaz de usuario de Windows.

## <a name="build-17704"></a>Compilación 17704
Para Windows general, visite información sobre las compilación 17704 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).

### <a name="wsl"></a>WSL
* Agregue la opción -u o--usuario wsl [GH 1203]
* Solucionar problemas de inicio WSL cuando se habilita el inicio rápido [GH 2576]
* Sockets de UNIX necesitan conservar las credenciales de desconectada del mismo nivel [GH 3183]
* Sockets de Unix sin bloqueo presentan indefinidamente EAGAIN [GH 3191]
* caso = off es el nuevo drvfs predeterminada montar tipo [GH 2937, 3212, 3328]
    * Consulte [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) para obtener más información.
* Agregar wslconfig / terminate para detener la ejecución de las distribuciones.

## <a name="build-17692"></a>Compilación 17692
Para Windows general, visite información sobre las compilación 17692 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).

### <a name="wsl"></a>WSL
* Corregir el problema con el contexto del shell WSL entradas de menú que no administren correctamente las rutas de acceso con espacios.
* Exponer entre mayúsculas y minúsculas por directorio como un atributo extendido
* ARM64: Emular las operaciones de mantenimiento de caché. Resolver [dotnet problema](https://github.com/dotnet/core/issues/1561).
* DrvFs: unescape solo caracteres del intervalo privado que corresponden a un carácter de escape.

## <a name="build-17686"></a>Compilación 17686
Para Windows general, visite información sobre las compilación 17686 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).

### <a name="wsl"></a>WSL
* Corregir el error de off a uno en la validación de longitud de intérprete de ELF analizador [GH 3154]
* Los temporizadores en absoluto con un tiempo en el pasado WSL no activan [GH 3091]
* Asegúrese de recién puntos de reanálisis creado se muestran como tal en el directorio primario.
* Crear atómicamente directorios distingue mayúsculas de minúsculas en DrvFs.

## <a name="build-17677"></a>Compilación 17677
Para Windows general, visite información sobre las compilación 17677 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).

### <a name="wsl"></a>WSL
* Se corrigió un problema adicional que podrían devolver operaciones multiproceso ENOENT aunque exista el archivo. [GH 2712]
* WSL fijo iniciar un error cuando se habilita UMCI. [GH 3020]

## <a name="build-17666"></a>Compilación 17666
Para Windows general, visite información sobre las compilación 17666 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).

### <a name="wsl"></a>WSL
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a>ADVERTENCIA: Hay un problema que impedía WSL desde que se ejecutan en algunos conjuntos de chips AMD [GH 3134]. Una corrección está listo y realizando su camino hacia la rama de compilación de Insider.
* Agregar el menú contextual del explorador para iniciar WSL [GH 437, 603, 1836]. Para usar con el botón secundario en una ventana del explorador y a la espera.
* Corregir el comportamiento de no bloqueo del socket de unix [GH 2822, 3100]
* Corrección de francesa comando NETLINK notificados en 2026 GH.
* Agregar compatibilidad con marcadores de propagación de montaje [GH 2911].
* Corregir el problema con truncate que no producen inotify eventos [GH 2978].
* Agregue--opción exec para wsl.exe invocar un solo archivo binario sin un shell.
* Agregar: opción de distribución para wsl.exe seleccionar una distribución específica.

## <a name="build-17655-skip-ahead"></a>Compilación 17655 (Saltar adelante)
Para Windows general, visite información sobre las compilación 17655 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).

### <a name="wsl"></a>WSL
* Compatibilidad limitada con dmesg. Las aplicaciones ahora pueden iniciar en dmesg. Controlador WSL registra información limitada a dmesg. En el futuro, esto puede ampliarse para llevar a cabo otros información/diagnósticos desde el controlador.
    * Nota: dmesg actualmente se admite a través de la `/dev/kmsg` la interfaz de dispositivo. `syslog` aún no se admite la interfaz sycall. Y, por lo tanto, algunos de los `dmesg` opciones de línea de comandos tales como `-S`, `-C` no funcionan.
* Se ha corregido un problema donde podrían devolver operaciones multiproceso ENOENT aunque exista el archivo. [GH 2712]

## <a name="build-17639-skip-ahead"></a>Compilación 17639 (Saltar adelante)
Para Windows general, visite información sobre las compilación 17639 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).

### <a name="wsl"></a>WSL
* Cambiar el gid de forma predeterminada y el modo de dispositivos serie para que coincida con nativo [GH 3042]
* DrvFs ahora es compatible con atributos extendidos.
    * Nota: DrvFs tiene algunas limitaciones en el nombre de los atributos extendidos. En concreto, algunos caracteres (como '/', ':' y '\*') no están permitidos y extendido los nombres de atributo no distinguen mayúsculas de minúsculas en DrvFs

## <a name="build-17133-fast"></a>Compilar 17133 (Fast)
Para Windows general, visite información sobre las compilación 17133 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).

### <a name="wsl"></a>WSL
* Corrección de bloqueo en WSL. [GH 3039, 3034]

## <a name="build-17128-fast"></a>Compilar 17128 (Fast)
Para Windows general, visite información sobre las compilación 17128 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).

### <a name="wsl"></a>WSL
* Ninguno

## <a name="build-17627-skip-ahead"></a>Compilación 17627 (Saltar adelante)
Para Windows general, visite información sobre las compilación 17627 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).

### <a name="wsl"></a>WSL
* Agregar compatibilidad para las operaciones basadas en la pi futex. [GH 1006]
    * Tenga en cuenta que las prioridades no son actualmente una característica WSL admitida por lo que existen limitaciones, pero debe desbloquearse uso estándar.
* Compatibilidad con el firewall de Windows para los procesos WSL. [GH 1852]
    * Por ejemplo, para permitir el WSL python procesa para que escuche en cualquier puerto, utilice el cmd de Windows con privilegios elevados: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```
    * Para obtener más información sobre cómo agregar reglas de firewall, consulte [vínculo](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)
* Respetar el shell predeterminado del usuario cuando se usa wsl.exe. [GH 2372]
* Informe todas las interfaces de red como ethernet. [GH 2996]
* Un mejor control del archivo/etc/passwd dañado. [GH 3001]

### <a name="console"></a>Console
* No hay correcciones.

### <a name="ltp-results"></a>LTP resultados:
Las pruebas en curso.

## <a name="build-17618-skip-ahead"></a>Compilación 17618 (Saltar adelante)
Para Windows general, visite información sobre las compilación 17618 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).

### <a name="wsl"></a>WSL
* Introducir pseudoconsole funcionalidad para la interoperabilidad de NT [GH 988, 1366, 1433, 1542, 2370, 2406].
* El mecanismo de instalación heredada (lxrun.exe) ha quedado obsoleto. El mecanismo compatible para la instalación de las distribuciones es a través de la Microsoft Store.

### <a name="console"></a>Console
* No hay correcciones.

### <a name="ltp-results"></a>LTP resultados:
Las pruebas en curso.

## <a name="build-17110"></a>Compilación 17110
Para Windows general, visite información sobre las compilación 17110 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).

### <a name="wsl"></a>WSL
* Permitir /init terminar de Windows [GH 2928].
* DrvFs utiliza mayúsculas y minúsculas por directorio de forma predeterminada (equivalente a la "caso = dir" opción de montaje).
    * Uso de "caso = force" (el comportamiento anterior) requiere establecer una clave del registro. Ejecute el siguiente comando para habilitar "caso = force" Si necesita usarlo: reg agregar HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1
    * Si tiene directorios existentes creados con WSL en una versión anterior de Windows que deben estar entre mayúsculas y minúsculas, usar fsutil.exe para marcarlos como con diferenciación entre mayúsculas y minúsculas: fsutil.exe archivo setcasesensitiveinfo <path> habilitar
* Finalizar cadenas devueltos desde la syscall uname con NULL.

### <a name="console"></a>Console
* No hay correcciones.

### <a name="ltp-results"></a>LTP resultados:
Las pruebas en curso.

## <a name="build-17107"></a>Compilación 17107
Para Windows general, visite información sobre las compilación 17107 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).

### <a name="wsl"></a>WSL
* Admite TCSETSF y TCSETSW en los puntos de conexión maestro pty [GH 2552].
* A partir de procesos simultáneos de interoperabilidad puede dar lugar a EINVAL [GH 2813].
* Corregir PTRACE_ATTACH para mostrar el estado de seguimiento adecuado en /proc/pid/status.
* Anticipación de corrección donde los procesos de corta duración clonados con marcas de la CLEARTID y SETTID pudo salir sin borrar la dirección TID.
* Mostrar un mensaje al actualizar los directorios de sistema de archivos de Linux al pasar de una compilación anterior a 17093. Para obtener más detalles sobre los cambios del sistema de 17093 archivo, vea las notas de [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).

### <a name="console"></a>Console
* No hay correcciones.

### <a name="ltp-results"></a>LTP resultados:
Las pruebas en curso.

## <a name="build-17101"></a>Compilación 17101
Para Windows general, visite información sobre las compilación 17101 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).

### <a name="wsl"></a>WSL
* Compatibilidad con signalfd. [GH 129]
* Admite nombres de archivo que contiene caracteres no válidos de NTFS mediante su codificación como privados caracteres Unicode. [GH 1514]
* Montaje automático retrocederá a solo lectura cuando no se admite la escritura. [GH 2603]
* Permitir el pegado de los pares suplentes de Unicode (como emoji caracteres). [GH 2765]
* Archivos pseudo /proc y PF deben devolver leer y escribir listo desde select, sondeo, epoll, et al [GH 2838]
* Se corrige el problema que podría provocar que el servicio entrar en bucle infinito cuando el registro ha sido alterado o está dañado.
* Corregir mensajes netlink para trabajar con la versión más reciente de (dirección ascendente 4.14) de iproute2.

### <a name="console"></a>Console
* No hay correcciones.

### <a name="ltp-results"></a>LTP resultados:
Las pruebas en curso.

## <a name="build-17093"></a>Compilación 17093
Para Windows general, visite información sobre las compilación 17093 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).

#### <a name="important"></a>Importante:
Al iniciar WSL por primera vez después de actualizar a esta compilación, debe realizar algún trabajo de actualización de los directorios de sistema de archivos de Linux. Esto puede tardar varios minutos, por lo que puede parecer WSL que iniciarse lentamente. Esto solo debería ocurrir una vez para cada distribución haya instalado desde la tienda.
* Soporte mejorado para mayúsculas y minúsculas en DrvFs.
    * DrvFs ahora es compatible con mayúsculas y minúsculas por directorio. Se trata de una nueva marca que se puede establecer en los directorios para indicar que todas las operaciones en estos directorios deben tratarse como distingue mayúsculas de minúsculas, lo que permite que incluso las aplicaciones de Windows abrir correctamente los archivos que difieran solo por caso.
    * DrvFs tiene nuevas opciones de montaje, control de mayúsculas y minúsculas en una base por directorio
        * caso = force: todos los directorios se distinguen mayúsculas de minúsculas (excepto la raíz de la unidad). Nuevos directorios creados con WSL se marcan como distingue mayúsculas de minúsculas. Este es el comportamiento heredado excepto para marcar los nuevos directorios distingue mayúsculas de minúsculas.
        * caso = dir: solo los directorios con el indicador de mayúsculas y minúsculas por directorio se distinguen mayúsculas de minúsculas; otros directorios distinguen mayúsculas de minúsculas. Nuevos directorios creados con WSL se marcan como distingue mayúsculas de minúsculas.
        * caso = desactivada: solo los directorios con el indicador de mayúsculas y minúsculas por directorio se distinguen mayúsculas de minúsculas; otros directorios distinguen mayúsculas de minúsculas. Nuevos directorios creados con WSL se marcan como no distingue mayúsculas de minúsculas.
    * Nota: los directorios creados por WSL en versiones anteriores no tienen esta marca establecida, por lo que no se tratará como distingue mayúsculas de minúsculas si usa el "caso = dir" opción. Una manera de establecer esta marca en los directorios existentes estará disponible próximamente.
    * Ejemplo de montaje con estas opciones (las unidades de existente, debe primero desmonte antes de que se puede montar con diferentes opciones): sudo mount -t drvfs C:/mnt/c -o caso = dir
    * Por ahora, caso = forzar sigue siendo la opción predeterminada. Esto se cambiará al caso = dir en el futuro.
* Ahora puede usar barras diagonales en las rutas de acceso de Windows al montar DrvFs, p. ej.: -t drvfs //server/share /mnt/share de montaje de sudo
* WSL ahora procesa el archivo/etc/fstab durante el inicio de instancia [GH 2636].
    * Esto se realiza automáticamente montar unidades de DrvFs; las unidades que ya se han montado por fstab no se volverá a montar automáticamente, lo que le permite cambiar el punto de montaje para unidades específicas.
    * Este comportamiento se puede desactivar mediante wsl.conf.
* Los archivos de montaje, mountinfo y mountstats en /proc correctamente caracteres especiales como espacios [GH 2799] y barras diagonales inversas de escape
* Archivos especiales que se crean con DrvFs como vínculos simbólicos de WSL, o fifos y sockets cuando están habilitados los metadatos, ahora pueden copiarse y mover de Windows.

#### <a name="wsl-is-more-configurable-with-wslconf"></a>Es más configurable con wsl.conf WSL
Se ha agregado un método para que configure automáticamente cierta funcionalidad en WSL que se aplicarán cada vez que inicie el subsistema. Esto incluye las opciones de montaje automático y la configuración de red. Obtenga más información en nuestro blog en: https://aka.ms/wslconf

#### <a name="afunix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a>AF_UNIX permite las conexiones de socket entre los procesos de Linux en WSL y procesos nativos de Windows
Las aplicaciones de Windows y de WSL ahora pueden comunicarse entre sí a través de sockets de Unix. Imagine que desea ejecutar un servicio en Windows y que esté disponible para las aplicaciones de Windows y WSL. Ahora, que es posible con sockets de Unix. Leer más información en nuestro blog post en https://aka.ms/afunixinterop

### <a name="wsl"></a>WSL
* Compatibilidad con mmap() con MAP_NORESERVE [GH 121, 2784 error]
* Admitir CLONE_PTRACE y CLONE_UNTRACED [GH 121, 2781]
* Controlar la señal de finalización no SIGCHLD en clon [GH 121, 2781]
* Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]
* Error al cargar los archivos binarios de ELF que contienen encabezados de carga con desplazamientos distinto de cero [GH 1884]
* Cero out finales bytes de la página al cargar imágenes.
* Reducir los casos donde execve finaliza en modo silencioso el proceso

### <a name="console"></a>Console
* No hay correcciones.

### <a name="ltp-results"></a>LTP resultados:
Las pruebas en curso.

## <a name="build-17083"></a>Compilación 17083
Para Windows general, visite información sobre las compilación 17083 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).

### <a name="wsl"></a>WSL
* Fijo comprobación de errores relacionados con epoll [GH 2798, 2801, 2857]
* Fijo se bloquea cuando la desactivación de ASLR [GH 1185, 2870]
* Asegúrese de operaciones mmap aparecen atómicas [GH 2732]

### <a name="console"></a>Console
* No hay correcciones.

### <a name="ltp-results"></a>LTP resultados:
Las pruebas en curso.

## <a name="build-17074"></a>Compilación 17074
Para Windows general, visite información sobre las compilación 17074 el [Blog Windows](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).

### <a name="wsl"></a>WSL
* Formato de almacenamiento fijo de metadatos DrvFs [GH 2777] </br>
**Importante:** Metadatos de DrvFs creados antes de que esta compilación se mostrará incorrectamente o no admitirlo. Para corregir los archivos afectados, use chmod y chown para volver a aplicar los metadatos.
* Se corrigió un problema con varias señales y syscalls reiniciables.

### <a name="console"></a>Console
* No hay correcciones.

### <a name="ltp-results"></a>LTP resultados:
Las pruebas en curso.

## <a name="build-17063"></a>Compilación 17063
Para Windows general, visite información sobre las compilación 17063 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).

### <a name="wsl"></a>WSL
* DrvFs admite metadatos adicionales de Linux. Esto permite establecer el propietario y el modo de archivos mediante chmod/chown y también la creación de archivos especiales como fifos, sockets de unix y los archivos del dispositivo. Esto está deshabilitada de forma predeterminada por ahora, ya que es todavía experimental.
**Nota:**  Se ha corregido un error en el formato de metadatos utilizado por DrvFs. Aunque los metadatos funciona en esta compilación para la experimentación, compilaciones futuras no leerá correctamente metadatos creados por esta compilación.  Es posible que deba actualizar manualmente el propietario de los archivos modificados y los dispositivos con un identificador de dispositivo personalizada tendrán que volver a crear.

  Para habilitar DrvFs de montaje con la opción de metadatos (para habilitarla en un montaje existente, debe primero desmontarla):

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  Permisos de Linux se agregan como metadatos adicionales en el archivo; no afectan a los permisos de Windows.  Recuerde, edición de un archivo con un editor de Windows puede quitar los metadatos. En este caso, el archivo volverá a sus permisos predeterminados.

* Opciones de montaje se ha agregado a DrvFs para controlar los archivos sin metadatos.
  * UID: el identificador de usuario usado para el propietario de todos los archivos.
  * GID: el identificador de grupo usado para el propietario de todos los archivos.
  * umask: una máscara de permisos que se van a excluir para todos los archivos y directorios octal.
  * fMask: una máscara de permisos para excluir todos los archivos normales octal.
  * dmask: una máscara de permisos para excluir todos los directorios octal.

  Por ejemplo:
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  Combinar con la opción de metadatos para especificar los permisos predeterminados para los archivos sin metadatos.

* Introdujo una nueva variable de entorno, `WSLENV`, para configurar cómo fluyen las variables de entorno entre WSL y Win32.

  Por ejemplo:

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  `WSLENV` es una lista delimitada por signos de variables de entorno que se pueden incluir, al iniciar los procesos WSL de Win32 o Win32 de WSL.  Cada variable puede tener el sufijo con una barra diagonal seguida de marcadores que especifican cómo se traduce.
  * p: El valor es una ruta de acceso que se debe traducir entre las rutas de acceso WSL y rutas de acceso de Win32.
  * l: El valor es una lista de rutas de acceso. En WSL, es una lista delimitada por dos puntos. En Win32, es una lista delimitada por punto y coma.
  * u: El valor sólo debe incluir al invocar WSL de Win32
  * w: El valor sólo debe incluir al invocar Win32 de WSL

  Puede establecer `WSLENV` en .bashrc o en el entorno de Windows personalizadas para el usuario.

* montajes drvfs conserva correctamente las marcas de tiempo desde el archivo tar, cp -p (GH 1939)
* vínculos simbólicos drvfs informa del tamaño correcto (GH 2641)
* lectura/escritura funciona para los tamaños de E/S muy grandes (GH 2653)
* waitpid funciona con identificadores (GH 2534) del grupo de proceso
* significativamente mmap mejor rendimiento para las regiones de gran tamaño de reserva; mejora el rendimiento ghc (GH 1671)
* admite la personalidad de READ_IMPLIES_EXEC; máximos de correcciones y clisp (GH 1185)
* mprotect admite PROT_GROWSDOWN; correcciones clisp (GH 1128)
* sobrecarga de correcciones de errores de página en modo; correcciones sbcl (GH 1128)
* clon es compatible con varias combinaciones de marcas
* Compatibilidad con select/epoll de archivos epoll (previamente una operación inefectiva).
* Notificar ptrace de syscall no implementada.
* Omitir las interfaces que no están activos cuando se generan los servidores de nombres resolv.conf [GH 2694]
* Enumerar las interfaces de red con ninguna dirección física. [GH 2685]
* Mejoras y correcciones de errores adicionales.

### <a name="linux-tools-available-to-developers-on-windows"></a>Herramientas de Linux disponibles para los desarrolladores en Windows

* Cadena de herramientas de línea de comandos de Windows incluye bsdtar (tar) y curl.
  Lectura [este blog](https://aka.ms/tarcurlwindows) para obtener más información sobre la adición de estas dos nuevas herramientas y ver cómo está dando forma a la experiencia del desarrollador de Windows.

*   `AF_UNIX` está disponible en el SDK de Windows Insider (17061 +).
  Lectura [este blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) para obtener más información acerca de `AF_UNIX` y cómo pueden usar los desarrolladores en Windows.

### <a name="console"></a>Console
* No hay correcciones.

### <a name="ltp-results"></a>LTP resultados:
Las pruebas en curso.


## <a name="build-17046"></a>Compilación 17046

Para Windows general, visite información sobre las compilación 17046 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).

### <a name="fixed"></a>Fijo
#### <a name="wsl"></a>WSL
- Permitir que los procesos se ejecuten sin un terminal activo. [GH 709, 1007, 1511, 2252, 2391, et al.]
- Una mejor compatibilidad con CLONE_VFORK y CLONE_VM. [GH 1878, 2615]
- Omitir los controladores del filtro TDI de WSL las operaciones de red. [GH 1554]
- DrvFs crea vínculos simbólicos de NT cuando se cumplen ciertas condiciones. [GH 353, 1475, 2602]
    - El destino de vínculo debe ser relativo, no debe ocupar los puntos de montaje o vínculos simbólicos y debe existir.
    - El usuario debe tener SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (Esto normalmente requiere que se inicie con privilegios elevados wsl.exe), a menos que el modo de programador está activado.
    - En el resto de situaciones, DrvFs sigue creando vínculos simbólicos WSL.
- Permitir que se ejecuten con privilegios elevados y sin privilegios elevados instancias WSL simultáneamente.
- Support /proc/sys/kernel/yama/ptrace_scope
- Agregar wslpath para hacer WSL <> – conversiones de ruta de acceso de Windows. [GH 522, 1243, 1834, 2327, et al.]
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

### <a name="ltp-results"></a>LTP resultados:
Las pruebas en curso.


## <a name="build-17040"></a>Compilación 17040

Para Windows general, visite información sobre las compilación 17040 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).<br/>


### <a name="fixed"></a>Fijo
#### <a name="wsl"></a>WSL
- No hay correcciones desde 17035.

#### <a name="console"></a>Console
- No hay correcciones desde 17035.

### <a name="ltp-results"></a>LTP resultados:
Las pruebas en curso.

## <a name="build-17035"></a>Compilación 17035

Para Windows general, visite información sobre las compilación 17035 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).<br/>


### <a name="fixed"></a>Fijo
#### <a name="wsl"></a>WSL
- Acceso a archivos en DrvFs podría no funcionar ocasionalmente con EINVAL. [GH 2448]

#### <a name="console"></a>Console
- Alguna pérdida de color al insertar o eliminar líneas en el modo de VT.

### <a name="ltp-results"></a>LTP resultados:
Las pruebas en curso.

## <a name="build-17025"></a>Compilación 17025

Para Windows general, visite información sobre las compilación 17025 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).<br/>


### <a name="fixed"></a>Fijo
#### <a name="wsl"></a>WSL
- Iniciar procesos iniciales en un nuevo grupo de proceso [GH 1653, 2510] de primer plano.
- Entrega SIGHUP corrige [GH 2496].
- Generar nombre de puente virtual predeterminado si proporciona ninguno [GH 2497].
- Implement /proc/sys/kernel/random/boot_id [GH 2518].
- Corrige la canalización de stdout y stderr más interoperabilidad.
- Código auxiliar syncfs llamada del sistema.

#### <a name="console"></a>Console
- Corregir traducción de VT entrada para las consolas de terceros [GH 111]

### <a name="ltp-results"></a>LTP resultados:
Las pruebas en curso.

## <a name="build-17017"></a>Compilación 17017

Para Windows general, visite información sobre las compilación 17017 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).<br/>


### <a name="fixed"></a>Fijo
#### <a name="wsl"></a>WSL
- Omitir los encabezados ELF programa [GH 330] estén vacíos.
- Permitir LxssManager crear instancias WSL para los usuarios no interactivos (ssh y programado la compatibilidad con la tarea) [GH 777, 1602].
- Compatibilidad con WSL -> Win32 -> [GH 1228] de escenarios de WSL ("origen").
- Compatibilidad limitada para la terminación de las aplicaciones de consola que se invoca a través de interoperabilidad [GH 1614].
- Compatibilidad con las opciones de montaje para devpts [GH 1948].
- Ptrace bloqueo inicio secundarios [GH 2333].
- EPOLLET faltan algunos eventos [GH 2462].
- Devolver más datos para PTRACE_GETSIGINFO.
- Getdents con lseek ofrece resultados incorrectos.
- Corregir algunos bloqueos de aplicación de interoperabilidad de Win32, esperando una entrada en una canalización que no tiene ningún dato más.
- Compatibilidad con archivos tty/pty O_ASYNC.
- Otras mejoras y correcciones de errores

#### <a name="console"></a>Console
- Ninguna consola otros cambios relacionados en esta versión.

### <a name="ltp-results"></a>LTP resultados:
Las pruebas en curso.

## <a name="fall-creators-update"></a>Fall Creators Update

## <a name="build-16288"></a>Compilación 16288

Para Windows general, visite información sobre las compilación 16288 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).<br/>


### <a name="fixed"></a>Fijo
#### <a name="wsl"></a>WSL
- Inicializar correctamente y notificar uid, gid y el modo de descriptores de archivo socket [GH 2490]
- Otras mejoras y correcciones de errores

#### <a name="console"></a>Console
- Ninguna consola otros cambios relacionados en esta versión.

### <a name="ltp-results"></a>LTP resultados:
Ningún cambio desde 16273

## <a name="build-16278"></a>Compilación 16278

Para Windows general, visite información sobre las compilación 162738 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).<br/>


### <a name="fixed"></a>Fijo
#### <a name="wsl"></a>WSL
- Anular la asignación de vistas asignadas de secciones del archivo de seguridad explícitamente al destruir el estado LX MM [GH 2415]
- Otras mejoras y correcciones de errores

#### <a name="console"></a>Console
- Ninguna consola otros cambios relacionados en esta versión.

### <a name="ltp-results"></a>LTP resultados:
Ningún cambio desde 16273

## <a name="build-16275"></a>Compilación 16275

Para Windows general, visite información sobre las compilación 162735 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).<br/>


### <a name="fixed"></a>Fijo
#### <a name="wsl"></a>WSL
- No hay WSL otros cambios relacionados en esta versión.

#### <a name="console"></a>Console
- Ninguna consola otros cambios relacionados en esta versión.

### <a name="ltp-results"></a>LTP resultados:
Ningún cambio desde 16273

## <a name="build-16273"></a>Compilación 16273

Para Windows general, visite información sobre las compilación 16273 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).<br/>


### <a name="fixed"></a>Fijo
#### <a name="wsl"></a>WSL
- Se ha corregido un problema donde DrvFs notifican a veces, el tipo de archivo incorrecto para los directorios [GH 2392]
- Permitir la creación de sockets NETLINK_KOBJECT_UEVENT para desbloquear los programas que uevent uso [GH 1121, 2293, 2242, 2295, 2235, 648, 637]
- Agregar compatibilidad para la conexión de no bloqueo [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]
- Implemente CLONE_FS clonar el indicador de llamada del sistema [GH 2242]
- Solucionar problemas con respecto al control de no tabulaciones o comillas correctamente en la interoperabilidad de NT [GH 1625, 2164]
- Resolver errores cuando se intenta volver a iniciar WSL instancias [GH 651, 2095] ha denegado el acceso
- Implementar futex FUTEX_REQUEUE y FUTEX_CMP_REQUEUE operaciones [GH 2242]
- Corrija los permisos para los distintos archivos SysFs [GH 2214]
- Corregir el bloqueo de la pila de Haskell durante la instalación [GH 2290]
- Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]
- Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]
- Agregar compatibilidad parcial con la llamada del sistema ioprio_set [GH 498]
- Código auxiliar SO_REUSEPORT & Agregar compatibilidad con SO_PASSCRED de netlink sockets [69 GH]
- Devolver códigos de error diferentes de RegisterDistribuiton si una distribución actualmente se está instalado o desinstalado.
- Permitir anulación del registro de las distribuciones de WSL parcialmente instaladas a través de wslconfig.exe
- Corregir la falta de respuesta de python socket ensayo desde udp::msg_peek
- Otras mejoras y correcciones de errores

#### <a name="console"></a>Console
- Ninguna consola otros cambios relacionados en esta versión.

### <a name="ltp-results"></a>LTP resultados:
Total de pruebas: 1904<br/>
Pruebas de omitidos totales: 209<br/>
Número total de errores: 229<br/>
[Los registros de ejecución de pruebas LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a>Compilación 16257

Para Windows general, visite información sobre las compilación 16257 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).<br/>


### <a name="fixed"></a>Fijo
#### <a name="wsl"></a>WSL
- Implementar prlimit64 llamada del sistema
- Agregar compatibilidad para ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]
- Código auxiliar MSG_MORE para los sockets TCP [GH 2351]
- Corregir comportamiento no válido de vector auxiliar AT_EXECFN [GH 2133]
- Corregir el comportamiento de copiar y pegar para consola/tty y agregar mejor búfer lleno de control [GH 2204, 2131]
- Establecer AT_SECURE en vector auxiliar para programas de Id. de usuario de conjunto y set-group-ID [GH 2031]
- Psuedo terminal punto de conexión principal no se controla TIOCPGRP [GH 1063]
- Corrección lseek hace para rebobinar directorios en LxFs [GH 2310]
- /dev/ptmx locks up after heavy usage [GH 1882]
- Otras mejoras y correcciones de errores

#### <a name="console"></a>Console
- Corrección para horizontal líneas o caracteres de subrayado en todas partes [GH 2168]
- Corrección del error por orden de proceso cambiado NPM hacen más difícil cerrar [GH 2170]
- Agrega la nueva combinación de colores: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/

### <a name="ltp-results"></a>LTP resultados:
Ningún cambio desde 16251

### <a name="syscall-support"></a>Soporte técnico de syscall
A continuación se muestran una lista de nuevas o mejoradas syscalls que tienen alguna implementación en WSL. Las llamadas en esta lista se admiten en al menos un escenario, pero es posible que no dispone de todos los parámetros compatibles en este momento.

`prlimit64`<br/>

### <a name="known-issues"></a>Problemas conocidos
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[GitHub Issue 2392: Carpetas de Windows no reconoce WSL...](https://github.com/Microsoft/BashOnWindows/issues/2392)
En la compilación 16257, WSL tiene problemas al enumerar los archivos o carpetas de Windows a través de `/mnt/c/...`.
Este problema se ha corregido y deberían liberarse en Insider durante la semana del 14/8/2017.

<br/>

## <a name="build-16251"></a>Compilación 16251

Para Windows general, visite información sobre las compilación 16251 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).<br/>


### <a name="fixed"></a>Fijo
#### <a name="wsl"></a>WSL
- Quitar la etiqueta a la versión beta de componente opcional de WSL, consulte [entrada de blog](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) para obtener más información.
- Inicializar correctamente el conjunto guardado uid y gid de Id. de usuario de conjunto y el Id. de grupo de conjunto de archivos binarios en exec [GH 962, 1415, 2072]
- Se agregó compatibilidad para ptrace PTRACE_O_TRACEEXIT [GH 555]
- Ha agregado compatibilidad con ptrace PTRACE_GETFPREGS y PTRACE_GETREGSET con NT_FPREGSET [GH 555]
- Se ha corregido ptrace detener en omite las señales
- Otras mejoras y correcciones de errores

#### <a name="console"></a>Console
- Ninguna consola otros cambios relacionados en esta versión.

### <a name="ltp-results"></a>LTP resultados:
Número de pruebas superadas: 768</br>
Número de pruebas no superadas: 244</br>
Número de pruebas omitidas: 96</br>
[Los registros de ejecución de pruebas LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a>Compilación 16241

Para Windows general, visite información sobre las compilación 16241 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).<br/>


### <a name="fixed"></a>Fijo
#### <a name="wsl"></a>WSL
- No hay WSL otros cambios relacionados en esta versión.

#### <a name="console"></a>Console
- Corrección para generar el carácter incorrecto para las líneas de cruce DEC, notifican originalmente [aquí](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)
- Corrección para ningún texto de salida que se muestra en la página de códigos 65001 (utf8)
- No se transfieren los cambios realizados en los valores RGB de un color a otras partes de la paleta de cambio de selección. Esto hará que la hoja de propiedades de la consola mucho más fáciles de usar.
- CTRL + S parece no funcionar correctamente
- Sin negrita /-Dim completamente está ausente de códigos de escape ANSI [GH 2174]
- Consola correctamente no es compatible con temas de color Vim [GH 1706]
- No se puede pegar el juego de caracteres determinado [GH 2149]
- Cambio de tamaño de reflujo forma extraña interactúa con el tamaño de una ventana de bash al material está en la línea de comando/Editar [GH ConEmu 1123]
- CTRL-L deja la pantalla desfasada [GH 1978]
- Errores de representación de consola al mostrar VT en HDPI [GH 1907]
- Caracteres Japansese parezca extraños con el carácter Unicode U + 30FB [GH 2146]
- Otras mejoras y correcciones de errores

</br>

## <a name="build-16237"></a>Compilación 16237

Para Windows general, visite información sobre las compilación 16237 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).<br/>


### <a name="fixed"></a>Fijo
- Utilice los atributos predeterminados para los archivos sin EAs de lxfs (raíz, raíz, 0000)
- Se agregó compatibilidad para las distribuciones que usan los atributos extendidos
- Relleno de corrección para las entradas devueltas por getdents y getdents64
- Corregir la comprobación de permisos para la llamada del sistema SHM_STAT shmctl [GH 2068]
- Estado fijo epoll inicial incorrecto para los TTY [GH 2231]
- Corregir readdir DrvFs no devuelve todas las entradas [GH 2077]
- Corregir LxFs readdir cuando hay archivos desvincula [GH 2077]
- Permitir que los archivos no vinculados drvfs abrirse de nuevo a través de procfs
- Agrega el reemplazo de la clave del registro global para deshabilitar las características WSL (interoperabilidad / montaje de unidad)
- Corregir el recuento de bloque incorrecta en "DO" DrvFs (y LxFs) [GH 1894]
- Otras mejoras y correcciones de errores

</br>

## <a name="build-16232"></a>Compilación 16232

Para Windows general, visite información sobre las compilación 16232 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).<br/>


### <a name="fixed"></a>Fijo
- No hay WSL otros cambios relacionados en esta versión.

</br>

## <a name="build-16226"></a>Compilación 16226

Para Windows general, visite información sobre las compilación 16226 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).<br/>


### <a name="fixed"></a>Fijo
- xattr relacionados con la compatibilidad de syscall (getxattr, setxattr, listxattr, removexattr).
- soporte técnico de xattr Security.capablity.
- Compatibilidad mejorada con ciertos sistemas de archivos y filtros, incluidos los servidores SMB que no son MS. [GH #1952]
- Compatibilidad mejorada para los marcadores de posición de OneDrive, los marcadores de posición GVFS y OS Compact archivos comprimidos.
- Otras mejoras y correcciones de errores

</br>

## <a name="build-16215"></a>Compilación 16215

Para Windows general, visite información sobre las compilación 16215 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).<br/>


### <a name="fixed"></a>Fijo
- WSL ya no requiere el modo de programador.
- Admite a las uniones de directorio en drvfs.
- Controlar la desinstalación de paquetes appx de distribución de WSL.
- Actualización procfs mostrar privada y compartir asignaciones.
- Agregue capacidad para wslconfig.exe limpiar las distribuciones que se instalan o desinstalan de parcialmente.
- Se agregó compatibilidad para IP_MTU_DISCOVER para los sockets TCP. [GH 1639, 2115, 2205]
- Inferir la familia de protocolos para que las rutas AF_INADDR.
- Mejoras de dispositivo en serie [GH 1929].

</br>

## <a name="build-16199"></a>Compilación 16199

Para Windows general, visite información sobre las compilación 16199 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).<br/>


### <a name="fixed"></a>Fijo
- No hay WSL otros cambios relacionados en estas versiones.

</br>

## <a name="build-16193"></a>Compilación 16193

Para Windows general, visite información sobre las compilación 16193 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).<br/>


### <a name="fixed"></a>Fijo
- Condición de carrera entre el envío SIGCONT y un threadgroup terminación [GH 1973]
- cambiar dispositivos tty y pty al informe FILE_DEVICE_NAMED_PIPE en lugar de FILE_DEVICE_CONSOLE [GH 1840]
- Corrección SSH para IP_OPTIONS
- Mover DrvFs montaje a init daemon [GH 1862, 1968, 1767, 1933]
- Se agregó compatibilidad en DrvFs para seguir los vínculos simbólicos de NT.

</br>

## <a name="build-16184"></a>Compilación 16184

Para Windows general, visite información sobre las compilación 16184 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).<br/>


### <a name="fixed"></a>Fijo
- Quita la tarea de mantenimiento de paquetes apt (lxrun.exe /update)
- Salida con formato fijo no aparece en de los procesos de Windows en node.js [GH 1840]
- Relaje los requisitos de alineación en lxcore [GH 1794]
- Se corrigió el control de la marca AT_EMPTY_PATH en un número de llamadas del sistema.
- Se corrigió un problema donde eliminando archivos DrvFs con identificadores abiertos hará que el archivo de un comportamiento indefinido [GH 544,966,1357,1535,1615]
- / etcetera/hosts heredarán las entradas del archivo de hosts de Windows (% windir%\system32\drivers\etc\hosts) [GH 1495]

</br>

## <a name="build-16179"></a>Compilación 16179

Para Windows general, visite información sobre las compilación 16179 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).<br/>


### <a name="fixed"></a>Fijo
- No hay cambios WSL esta semana.

</br>

## <a name="build-16176"></a>Compilación 16176

Para Windows general, visite información sobre las compilación 16176 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).<br/>


### <a name="fixed"></a>Fijo

- [Habilita la compatibilidad con puerto serie](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- Opción de socket IP se ha agregado IP_OPTIONS [GH 1116]
- Implementa la función pwritev (al cargar el archivo a nginx/PHP-FPM) [GH 1506]
- Se han agregado opciones de socket IP IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]
- Soporte técnico para la opción de socket IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]
- Se ha agregado la opción de socket _MTU IP (V6) para el nodo aplicaciones, traceroute, investigue, nslookup, host
- Opción de socket IP se ha agregado IPV6_UNICAST_HOPS
- [Mejoras del sistema de archivos](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * Permite el montaje de las rutas de acceso UNC
    * Habilitar la compatibilidad con CDFS en drvfs
    * Controlar correctamente los permisos para los sistemas de archivos de red en drvfs
    * Agregar compatibilidad para unidades remotas a drvfs
    * Habilitar FAT admitir en drvfs
- Mejoras y correcciones adicionales

### <a name="ltp-results"></a>LTP resultados
Ningún cambio desde 15042

</br>

## <a name="build-16170"></a>Compilación 16170

Para Windows general, visite información sobre las compilación 16170 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).<br/>

Hemos lanzado una nueva [entrada de blog](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discutir nuestros esfuerzos para probar WSL.

### <a name="fixed"></a>Fijo

- Socket de compatibilidad con la opción IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]
- Agregar compatibilidad con PTRACE_OLDSETOPTIONS. [GH 1692]
- Las mejoras y correcciones adicionales

### <a name="ltp-results"></a>LTP resultados
Ningún cambio desde 15042

</br>

## <a name="build-15046-to-windows-10-creators-update"></a>Compilar 15046 a Windows 10 Creators Update
Hay más no WSL correcciones o las características planeadas para su inclusión en Windows 10 Creators Update. Notas de WSL se reanudación en las próximas semanas para adiciones destinadas a la siguiente actualización principal de Windows. Para Windows general información sobre la compilación 15046 y especialista en futuras versiones visita la [Blog Windows](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/). <br/><br/>
 <br/>

## <a name="build-15042"></a>Compilación 15042

Para Windows general, visite información sobre las compilación 15042 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).<br/>


### <a name="fixed"></a>Fijo

- Corrección de un interbloqueo cuando se quita una ruta de acceso que terminen en ".."
- Se ha corregido un problema donde FIONBIO no devuelve 0 si se ejecuta correctamente [GH 1683]
- Se corrigió un problema con lecturas de longitud cero de sockets de datagrama inet
- Corregir posibles interbloqueos debido a la condición de carrera en la búsqueda de inode drvfs [GH 1675]
- Compatibilidad ampliada para datos auxiliares de socket de unix; SCM_CREDENTIALS y SCM_RIGHTS [GH 514, 613, 1326]
- Las mejoras y correcciones adicionales

### <a name="ltp-results"></a>LTP resultados:
Número de paso de prueba: 737</br>
Número de paso de no (por error, omitido, etcetera...): 255

</br>

## <a name="build-15031"></a>Compilación 15031

Para Windows general, visite información sobre las compilación 15031 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).<br/>


### <a name="fixed"></a>Fijo

- Se ha corregido un error donde se comportará incorrectamente esporádicamente time(2).
- Se ha corregido y emitir where * SIGPROCMASK syscalls podría dañar la máscara de señal.
- Longitud de línea de comandos completa se devuelven ahora en la notificación de la creación del proceso WSL. [GH 1632]
- WSL ahora informa salir del subproceso a través de ptrace GDB bloqueos. [GH 1196]
- Se corrigió el error donde ptys dejaba de responder después tmux mucha E/S. [GH 1358]
- Validación de tiempo de espera fijo muchas llamadas del sistema (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)
- Se ha agregado eventfd EFD_SEMAPHORE soporte [GH 452]
- Las mejoras y correcciones adicionales

### <a name="ltp-results"></a>LTP resultados:
Número de paso de prueba: 737</br>
Número de paso de no (por error, omitido, etcetera...): 255 </br>
[Los registros de ejecución de pruebas LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a>Compilación 15025

Para Windows general, visite información sobre las compilación 15025 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).<br/>


### <a name="fixed"></a>Fijo

- Corrección de errores que grep roto 2,27 [GH 1578]
- Marca EFD_SEMAPHORE implementada para eventfd2 syscall [GH 452]
- Implemented /proc/[pid]/net/ipv6_route [GH 1608]
- Señal controlado por compatibilidad con E/S sockets de secuencias de unix [GH 393, 68]
- Admitir F_GETPIPE_SZ y F_SETPIPE_SZ [GH 1012]
- Implement recvmmsg() syscall [GH 1531]
- Se corrigió el error donde epoll_wait() no estaba esperando [GH 1609]
- Implement /proc/version_signature
- Tee syscall ahora devuelve un error si ambos descriptores de archivo hace referencia a la misma canalización
- Implementa el comportamiento correcto para SO_PEERCRED para sockets de Unix
- Control de parámetros no válidos de syscall tkill fijo
- Cambios para aumentar la preformace de drvfs
- Revisión secundaria para el bloqueo de E/S de Ruby
- Fijo recvmsg() devolver EINVAL para el indicador MSG_DONTWAIT para sockets inet [GH 1296]
- Las mejoras y correcciones adicionales

### <a name="ltp-results"></a>LTP resultados:
Número de paso de prueba: 732</br>
Número de paso de no (por error, omitido, etcetera...): 255 </br>
[Los registros de ejecución de pruebas LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a>Compilación 15019

Para Windows general, visite información sobre las compilación 15019 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).<br/>


### <a name="fixed"></a>Fijo

- Se corrigió el error que se informaba incorrectamente de uso de CPU en procfs para herramientas como htop (GH 823, 945, 971)
- Al llamar a open() con O_TRUNC en un archivo inotify genera ahora IN_MODIFY antes IN_OPEN
- Correcciones de socket de unix getsockopt SO_ERROR para habilitar postgress [GH 61, 1354]
- Implementar /proc/sys/net/core/somaxconn para el lenguaje GO
- Tarea en segundo plano de actualización de paquetes APT-get ahora se ejecuta oculto de la vista
- Ámbito clara para el host local de ipv6 (error Spring-Framework(Java)).
- Las mejoras y correcciones adicionales

### <a name="ltp-results"></a>LTP resultados:
Número de paso de prueba: 714 </br>
Número de paso de no (por error, omitido, etcetera...): 249 </br>
[Los registros de ejecución de pruebas LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a>Compilación 15014

Para Windows general, visite información sobre las compilación 15014 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).<br/>


### <a name="fixed"></a>Fijo

- CTRL + C ahora funciona según lo previsto
- htop y ps auxw ahora mostrar correcto uso de recursos (GH #516)
- Traducción básica de excepciones de NT a las señales. (GH 513 #)
- fallocate ahora produce ENOSPC cuando se está quedando sin espacio en lugar de EINVAL (GH #1571)
- Se ha agregado /proc/sys/kernel/sem.
- Llamadas al sistema semop y semtimedop implementadas
- Errores de nslookup fijo con la opción de socket IP_RECVTOS & IPV6_RECVTCLASS (GH 69)
- Compatibilidad con las opciones de socket IP_RECVTTL y IPV6_RECVHOPLIMIT
- Las mejoras y correcciones adicionales

### <a name="ltp-results"></a>LTP resultados:
Número de paso de prueba: 709 </br>
Número de paso de no (por error, omitido, etcetera...): 255 </br>
[Los registros de ejecución de pruebas LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a>Resumen de syscall
Syscall total: 384 </br>
Total implementado: 235 </br>
Total que se procesó con stub: 22 </br>
Total sin implementar: 127 </br>
[Desglose detallado](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a>Compilación 15007

Para Windows general, visite información sobre las compilación 15007 el [Blog Windows]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).<br/>


### <a name="known-issue"></a>Problema conocido

- Hay un problema conocido en la consola no reconoce algunos Ctrl + <key> entrada.  Esto incluye el comando ctrl-c que actuará como una pulsación de tecla 'c' normal.

  - Solución: Asignar una clave alternativa a Ctrl + C. Por ejemplo, para asignar Ctrl + K para Ctrl + C lo: `stty intr \^k`.  Esta asignación es por terminal y tendrá que realizarse *cada* bash de tiempo se inicia. Los usuarios pueden explorar la opción para incluir esto en su `.bashrc`

### <a name="fixed"></a>Fijo

- Se ha corregido el problema donde ejecutando WSL consumiría 100% de un núcleo de CPU
- Opción IP_PKTINFO, IPV6_RECVPKTINFO ahora admitidos de socket. (GH #851, 987)
- Truncar la dirección física de interfaz de red a lxcore de 16 bytes (# GH 1452, 1414, 1343, 468, 308)
- Las mejoras y correcciones adicionales

### <a name="ltp-results"></a>LTP resultados:
Número de paso de prueba: 709 </br>
Número de paso de no (por error, omitido, etcetera...): 255 </br>
[Los registros de ejecución de pruebas LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a>Compilación 15002

Para Windows general, visite información sobre las compilación 15002 el [Blog Windows](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).<br/>


### <a name="known-issue"></a>Problema conocido

Dos problemas conocidos:
- Hay un problema conocido en la consola no reconoce algunos Ctrl + <key> entrada.  Esto incluye el comando ctrl-c que actuará como una pulsación de tecla 'c' normal.

  - Solución: Asignar una clave alternativa a Ctrl + C. Por ejemplo, para asignar Ctrl + K para Ctrl + C lo: `stty intr \^k`.  Esta asignación es por terminal y tendrá que realizarse *cada* bash de tiempo se inicia. Los usuarios pueden explorar la opción para incluir esto en su `.bashrc`

- Mientras se está ejecutando WSL un subproceso del sistema consume el 100% de un núcleo de CPU.  Abordar la causa raíz y se ha corregido internamente.

### <a name="fixed"></a>Fijo

- Todas las sesiones de bash ahora deben crearse en el mismo nivel de permiso.  Se bloqueará al intentar iniciar una sesión en un nivel diferente.  Esto significa que las consolas de administrador y que no es administrador no se pueden ejecutar al mismo tiempo. (GH 626 #)
<br/>
- Implementa los siguientes mensajes NETLINK_ROUTE (requiere un administrador de Windows)
     - RTM_NEWADDR (admite `ip addr add`)
     - RTM_NEWROUTE (admite `ip route add`)
     - RTM_DELADDR (admite `ip addr del`)
     - RTM_DELROUTE (admite `ip route del`)
- Comprobación de paquetes para actualizar de tarea programada ya no se ejecutará en una conexión de uso medido (GH #1371)
- Se ha corregido error donde canalización obtiene; es decir, bloqueada bash - c "ls - alR /" | Bash -c "cat" (GH #1214)
- Opción de socket TCP_KEEPCNT implementada (GH #843)
- Opción de socket IP_MTU_DISCOVER INET implementada (720 de # GH, 717, 170, 69)
- Quita la funcionalidad heredada para ejecutar los archivos binarios de NT de init con búsqueda de ruta de acceso de NT. (GH 1325 #)
- Corregir el modo de/dev/kmsg para permitir el acceso de lectura de grupo / otro (0644) (GH #1321)
- /Proc/sys/kernel/random/uuid implementada (GH #1092)
- Se ha corregido el error que mostraba el tiempo de inicio de proceso como año 2432 (GH #974)
- Variable de entorno de término predeterminado se ha cambiado a xterm-256color (GH #1446)
- Modificado la forma en que el proceso de confirmación se calcula durante la bifurcación de proceso. (GH 1286 #)
- Implemented /proc/sys/vm/overcommit_memory. (GH 1286 #)
- Archivo implementado /proc/net/route (GH #69)
- Error corregido donde estaba incorrectamente el nombre de método abreviado localizado (GH #696)
- Elf fijo lógica que se está validando incorrectamente los encabezados del programa de análisis debe ser menor que (o igual que) PATH_MAX. (GH 1048 #)
- Devolución de llamada implementada statfs procfs, sysfs, cgroupfs y binfmtfs (GH #1378)
- Windows AptPackageIndexUpdate fija que no se cierran (1184 de # de GH, también se describen en GH #1193)
- Personalidad ASLR se ha agregado compatibilidad con ADDR_NO_RANDOMIZE. (GH #1148, 1128)
- PTRACE_GETSIGINFO mejorada, SIGSEGV para seguimientos de pila gdb adecuado durante AV (GH #875)
- ELF análisis ya no se produce un error para los binarios de patchelf. (GH 471 #)
- VPN DNS se propaguen a /etc/resolv.conf (GH #416, 1350)
- Cierre las mejoras de TCP para la transferencia de datos más confiable. (GH #610, 616, 1025, 1335)
- Ahora un resultado correcto de código de error cuando hay demasiados archivos abierto (EMFILE). (GH #1126, 2090)
- Auditoría de Windows ahora informes de registro de nombre de la imagen en el proceso de creación la auditoría.
- Ahora se producirá un error al iniciar bash.exe desde dentro de una ventana de bash
- Mensaje de error se ha agregado al interoperabilidad no puede tener acceso a un directorio de trabajo en LxFs (es decir, notepad.exe .bashrc)
- Se corrigió un problema donde se ha truncado la ruta de acceso de Windows en WSL
- Las mejoras y correcciones adicionales

### <a name="ltp-results"></a>LTP resultados:
Número de paso de prueba: 690 </br>
Número de paso de no (por error, omitido, etcetera...): 274 </br>
[Los registros de ejecución de pruebas LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a>Soporte técnico de syscall
A continuación se muestran una lista de nuevas o mejoradas syscalls que tienen alguna implementación en WSL. Las llamadas en esta lista se admiten en al menos un escenario, pero es posible que no dispone de todos los parámetros compatibles en este momento.

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a>Compilación 14986

Para Windows general, visite información sobre las compilación 14986 el [Blog Windows](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).<br/>


### <a name="fixed"></a>Fijo

- Fijo verificaciones de error con Netlink y Pty IOCTL
- Versión del kernel ahora informa 4.4.0-43 para mantener la coherencia con Xenial
- Bash.exe ahora se inicia cuando la entrada se dirige a ' nul:' (GH #1259)
- Id. de subproceso notifica ahora correctamente en procfs (GH #967)
- IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | Marcas IN_ISDIR ahora se admiten en inotify_add_watch() (GH #1280)
- Implemente timer_create y las llamadas del sistema relacionadas.  Esto permite el uso GHC (GH #307)
- Se corrigió un problema donde ping devolvió una hora de 0.000ms (GH #1296)
- Devuelve el código de error correcto cuando hay demasiados archivos abiertos.
- Se corrigió un problema en WSL donde Netlink solicitud de datos de la interfaz de red produciría un error con EINVAL si la dirección de hardware de la interfaz es 32 bytes (por ejemplo, la interfaz Teredo)
   - Tenga en cuenta que la utilidad de Linux "ip" contiene un error que bloqueará si WSL informa de una dirección de hardware de 32 bytes. Se trata de un error en la "ip", no WSL. La "ip" utilidad codifica la longitud del búfer de cadena se usa para imprimir la dirección de hardware, y ese búfer es demasiado pequeño para imprimir una dirección de hardware de 32 bytes.
- Las mejoras y correcciones adicionales

### <a name="ltp-results"></a>LTP resultados:
Número de paso de prueba: 669 </br>
Número de paso de no (por error, omitido, etcetera...): 258 </br>
[Los registros de ejecución de pruebas LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a>Soporte técnico de syscall
A continuación se muestran una lista de nuevas o mejoradas syscalls que tienen alguna implementación en WSL. Las llamadas en esta lista se admiten en al menos un escenario, pero es posible que no dispone de todos los parámetros compatibles en este momento.

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a>Compilación 14971

Para Windows general, visite información sobre las compilación 14971 el [Blog Windows](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).<br/>


### <a name="fixed"></a>Fijo

 - Debido a circunstancias fuera de nuestro control no hay ninguna actualización en esta compilación para el subsistema de Windows para Linux.  Las actualizaciones programadas regularmente se reanudarán en la próxima versión.

### <a name="ltp-results"></a>LTP resultados:
No ha cambiado desde 14965 </br>
Número de paso de prueba: 664 </br>
Número de paso de no (por error, omitido, etcetera...): 263 </br>
[Los registros de ejecución de pruebas LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a>Compilación 14965

Para Windows general, visite información sobre las compilación 14965 el [Blog Windows](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).<br/>


### <a name="fixed"></a>Fijo

- Compatibilidad con Netlink sockets del protocolo NETLINK_ROUTE RTM_GETLINK y RTM_GETADDR (GH #468)
  - Permite que los comandos ifconfig y la dirección ip para la enumeración de red
  - Puede encontrar más información en nuestra [entrada de blog de redes de WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).

- / sbin ahora está en la ruta de acceso de forma predeterminada
- Ruta de acceso de usuario de NT anexada a la ruta de acceso WSL ahora de forma predeterminada (es decir, ahora puede escribir notepad.exe sin agregar System32 a la ruta de acceso de Linux)
- Se agregó compatibilidad para /proc/sys/kernel/cap_last_cap
- Los archivos binarios de NT ahora se puede iniciar desde WSL cuando el directorio de trabajo actual contiene caracteres que no sean ansi (GH #1254)
- Permitir apagado en el socket de secuencia de unix sin conexión.
- Se agregó compatibilidad para PR_GET_PDEATHSIG.
- Se agregó compatibilidad para CLONE_PARENT
- Se ha corregido error donde canalización obtiene; es decir, bloqueada bash - c "ls - alR /" | Bash -c "cat" (GH #1214)
- Controlar las solicitudes para conectarse al terminal actual.
- Marcar/proc /<pid>/oom_score_adj como de escritura.
- Agregar carpeta /sys/fs/cgroup.
- sched_setaffinity debe devolver el número de máscara de bits de afinidad
- Corregir la lógica de validación de ELF que incorrectamente se supone que las rutas de acceso del intérprete deben ser inferior a 64 caracteres. (GH 743 #)
- Descriptores de archivo abiertos pueden mantener abierta la ventana Consola (GH #1187)
- Error de Fixeed donde no se pudo rename() con barra diagonal en el nombre de destino (GH #1008) final
- Implementar archivo /proc/net/dev
- Hace ping 0.000ms fijo debido a la resolución del temporizador.
- /Proc/self/environ implementada (GH #730)
- Las mejoras y correcciones de errores adicionales

### <a name="ltp-results"></a>LTP resultados:
Número de paso de prueba: 664 </br>
Número de paso de no (por error, omitido, etcetera...): 263 </br>
[Los registros de ejecución de pruebas LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a>Compilación 14959

Para Windows general, visite información sobre las compilación 14959 el [Blog Windows](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).<br/>


### <a name="fixed"></a>Fijo

- Notificación de proceso de Pico mejorada para Windows.  Encontrar información adicional en el [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).
- Estabilidad mejorada con la interoperabilidad de Windows
- Se ha corregido errores 0 x 80070057 al iniciar bash.exe cuando está habilitada la protección de datos de empresa (EDP)
- Las mejoras y correcciones de errores adicionales

### <a name="ltp-results"></a>LTP resultados:
Número de paso de prueba: 665 </br>
Número de paso de no (por error, omitido, etcetera...): 263 </br>
[Los registros de ejecución de pruebas LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a>Compilación 14955

Para Windows general, visite información sobre las compilación 14955 el [Blog Windows](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).<br/>


### <a name="fixed"></a>Fijo

 - Debido a circunstancias fuera de nuestro control no hay ninguna actualización en esta compilación para el subsistema de Windows para Linux.  Las actualizaciones programadas regularmente se reanudarán en la próxima versión.

### <a name="ltp-results"></a>LTP resultados:
Número de paso de prueba: 665 </br>
Número de paso de no (por error, omitido, etcetera...): 263 </br>
[Los registros de ejecución de pruebas LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a>Compilación 14951

Para Windows general, visite información sobre las compilación 14951 el [Blog Windows](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).<br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a>Nueva característica: Windows o Ubuntu interoperabilidad
Los archivos binarios de Windows ahora se pueden invocar directamente desde la línea de comandos WSL.  Esto ofrece a los usuarios la capacidad de interactuar con su entorno de Windows y del sistema de forma que no ha sido posible.  Un ejemplo rápido, es posible que los usuarios ejecutar los comandos siguientes:

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

Puede encontrar más información en:

- [Blog del equipo de WSL para la interoperabilidad](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [Documentación de MSDN sobre interoperabilidad](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a>Fijo

- Ubuntu 16.04 (Xenial) ahora se instala para todas las instancias nuevas de WSL.  Los usuarios con las instancias existentes 14.04 (Trusty) no se actualizará automáticamente.
- Ahora se muestra la configuración regional establecida durante la instalación
- Las mejoras de Terminal incluidos errores donde redirige un proceso WSL a un archivo no siempre funcionan
- Duración de la consola debería se vincula a bash.exe
- Tamaño de la ventana de consola debe usar tamaño visible, no el tamaño de búfer
- Las mejoras y correcciones de errores adicionales

### <a name="ltp-results"></a>LTP resultados:
Número de paso de prueba: 665 </br>
Número de paso de no (por error, omitido, etcetera...): 263 </br>
[Los registros de ejecución de pruebas LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a>Compilación 14946

Para Windows general, visite información sobre las compilación 14946 el [Blog Windows](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).<br/>


### <a name="fixed"></a>Fijo

- Se corrigió un problema que impedía la creación de cuentas de usuario WSL para los usuarios con los nombres de usuario de NT que contienen espacios o comillas. 
- Cambiar VolFs y DrvFs para devolver 0 para el recuento de vínculos del directorio de stat
- Admite la opción de socket IPV6_MULTICAST_HOPS.
- Limitar el bucle de E/S por tty a una única consola. Ejemplo: el siguiente comando es posible:
  - bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"

- Reemplace los espacios por fichas en /proc/cpuinfo (GH #1115)
- DrvFs aparece ahora en mountinfo con un nombre que coincida con el volumen montado de Windows
- / Home/root aparecerán y en mountinfo con nombres correctos
- Las mejoras y correcciones de errores adicionales

### <a name="ltp-results"></a>LTP resultados:
Número de paso de prueba: 665 </br>
Número de paso de no (por error, omitido, etcetera...): 263 </br>
[Los registros de ejecución de pruebas LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a>Compilación 14942

Para Windows general, visite información sobre las compilación 14942 el [Blog Windows](https://aka.ms/onefourninefourtwoooooo).<br/>


### <a name="fixed"></a>Fijo

- Un número de verificaciones de error dirigido, incluida la "ha INTENTADO ejecutar de NOEXECUTE memoria" redes de bloqueo que bloqueaba SSH
- compatibilidad con inotifiy notificaciones generadas a partir de las aplicaciones de Windows en DrvFs ahora está en
- Implementar TCP_KEEPIDLE y TCP_KEEPINTVL para mongod. (GH #695)
- Implementar la llamada de sistema pivot_root
- Implementar la opción de socket para SO_DONTROUTE
- Las mejoras y correcciones de errores adicionales


### <a name="ltp-results"></a>LTP resultados:
Número de paso de prueba: 665 </br>
Número de paso de no (por error, omitido, etcetera...): 263 </br>
[Los registros de ejecución de pruebas LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a>Soporte técnico de syscall
A continuación se muestran una lista de nuevas o mejoradas syscalls que tienen alguna implementación en WSL. Las llamadas en esta lista se admiten en al menos un escenario, pero es posible que no dispone de todos los parámetros compatibles en este momento.

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a>Compilación 14936

Para Windows general, visite información sobre las compilación 14936 el [Blog Windows](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).<br/>


Nota: WSL instalará Ubuntu versión 16.04 (Xenial) en lugar de Ubuntu 14.04 (furgoneta) en una próxima versión.  Este cambio se aplicará a Insider instalar instancias nuevas (lxrun.exe /install o la primera ejecución de bash.exe).  Las instancias existentes con furgoneta no se actualizará automáticamente. Los usuarios pueden actualizar su imagen leal a Xenial mediante el comando de actualización de versión de hacer.

### <a name="known-issue"></a>Problema conocido
WSL está experimentando un problema con algunas implementaciones de socket.  La comprobación de errores se manifiesta como un bloqueo con el error "Ha INTENTADO ejecutar NOEXECUTE memoria insuficiente".  La manifestación más común de este problema es un bloqueo al usar ssh.  La causa raíz se ha corregido en las compilaciones internas y se insertará en Insider lo antes posible.

### <a name="fixed"></a>Fijo

- Implementa la llamada del sistema chroot
- Mejoras en inotify ~~incluida la compatibilidad con las notificaciones generadas desde aplicaciones de Windows en DrvFs~~
  - Corrección: Inotify compatibilidad con los cambios que se originan desde las aplicaciones de Windows no está disponibles en este momento.
- Enlace a IPV6 de socket::<port n> ahora admite IPV6_V6ONLY (68 de # GH, #157, 393 #, #460, 674 #, #740, 982 #, #996)
- Comportamiento WNOWAIT para waitid systemcall implementa (GH #638)
- Compatibilidad con las opciones de socket IP IP_HDRINCL y IP_TTL
- Se debe devolver inmediatamente read() de longitud cero (GH #975)
- Controlar correctamente los prefijos de nombres de archivo y nombre de archivo que no incluyen un terminador NULL en un archivo .tar.
- compatibilidad con epoll/dev/null
- Corregir el origen de hora /dev/alarm
- Bash -c ahora se puede redirigir a un archivo
- Las mejoras y correcciones de errores adicionales

### <a name="ltp-results"></a>LTP resultados:
Número de paso de prueba: 664 </br>
Número de paso de no (por error, omitido, etcetera...): 264 </br>
[Los registros de ejecución de pruebas LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a>Soporte técnico de syscall
A continuación se muestran una lista de nuevas o mejoradas syscalls que tienen alguna implementación en WSL. Las llamadas en esta lista se admiten en al menos un escenario, pero es posible que no dispone de todos los parámetros compatibles en este momento.

`chroot`<br/>
<br/>

## <a name="build-14931"></a>Compilación 14931

Para Windows general, visite información sobre las compilación 14931 el [Blog Windows](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).<br/>


### <a name="fixed"></a>Fijo

 - Debido a circunstancias fuera de nuestro control no hay ninguna actualización en esta compilación para el subsistema de Windows para Linux.  Las actualizaciones programadas regularmente se reanudación en la próxima versión.

<br/>

## <a name="build-14926"></a>Compilación 14926

Para Windows general, visite información sobre las compilación 14926 el [Blog Windows](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).<br/>


### <a name="fixed"></a>Fijo

- Ping funciona ahora en las consolas que no tienen privilegios de administrador
- Ping6 ahora admitidos, también sin privilegios de administrador
- Inotify compatibilidad con los archivos modificados a través de WSL. (GH #216)
  - Marcas compatibles:
    - inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK
    - inotify_add_watch eventos: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF
    - inotify_add_watch atributos: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR
    - leer la salida: LX_IN_ISDIR, LX_IN_IGNORED
  - Problema conocido: Modificar archivos de aplicaciones de Windows no genera ningún evento
- Socket de UNIX es compatible ahora con SCM_CREDENTIALS

### <a name="ltp-results"></a>LTP resultados:
Número de paso de prueba: 651 </br>
Número de paso de no (por error, omitido, etcetera...): 258 </br>
[Los registros de ejecución de pruebas LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a>Compilación 14915

Para Windows general, visite información sobre las compilación 14915 el [Blog Windows](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).<br/>


### <a name="fixed"></a>Fijo
-  Socketpair para sockets de datagramas de unix (GH #262)
- Soporte técnico de socket de UNIX para SO_REUSEADDR
- Soporte técnico de socket de UNIX para SO_BROADCAST (GH #568)
- Soporte técnico de socket de UNIX para SOCK_SEQPACKET (GH 758 #, #546)
- Agregar compatibilidad para el envío de socket de datagrama de unix, recepción y de cierre
- Corregir la comprobación de errores debido a la validación de parámetros mmap no válido para las direcciones no fija. (GH #847)
- Soporte técnico para suspender y reanudar de Estados de terminales
- Compatibilidad con TIOCPKT ioctl desbloquear la utilidad de la pantalla (GH #774)
    - Problema conocido: Teclas de función no operativos
- Se ha corregido una carrera en TimerFd que podría provocar que un miembro liberado 'ReaderReady' LxpTimerFdWorkerRoutine (GH #814) tengan acceso a
- Habilitar la compatibilidad del sistema reiniciable llamada futex, sondeos y clock_nanosleep
- Un enlace se ha agregado compatibilidad de montaje
- dejar de compartir compatibilidad con el espacio de nombres de montaje
    - Problema conocido: Al crear un nuevo espacio de nombres de montaje con `unshare(CLONE_NEWNS)` seguirá el directorio de trabajo actual para que apunte al espacio de nombres anterior
- Otras mejoras y correcciones de errores

<br/>

## <a name="build-14905"></a>Compilación 14905

Para Windows general, visite información sobre las compilación 14905 el [Blog Windows](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).<br/>


### <a name="fixed"></a>Fijo
- Admite el sistema reiniciable llamadas ahora están (GH #349, GH #520)
- Vínculos simbólicos a directorios termina en / ahora operativa (GH #650)
- Implementado ioctl RNDGETENTCNT para/dev/Random
- Implementa el archivo/proc / [pid] / monta/proc / [pid] / mountinfo y/proc / [pid] / mountstats archivos
- Las mejoras y correcciones de errores adicionales

</br>

## <a name="build-14901"></a>Compilación 14901
Primera Insider de compilación para la entrada de la versión de Windows 10 Anniversary Update.

Para Windows general, visite información sobre las compilación 14901 el [Blog Windows](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).<br/>


### <a name="fixed"></a>Fijo
- Se corrigió un problema barra diagonal final
    - Los comandos como `$ mv a/c/ a/b/` trabajar ahora
- Instalación pide ahora si se debe establecer la configuración regional de Ubuntu para la configuración regional de Windows
- Compatibilidad con procfs carpeta ns
- Agrega montaje y desmontaje para tmpfs, procfs y sistemas de archivos sysfs
- Corregir mknod [arroba] firma ABI de 32 bits
- Sockets de UNIX se mueven en el modelo de envío
- Tamaño del búfer INET socket recv establecer mediante setsockopt debe admitirse.
- Socket de unix MSG_CMSG_CLOEXEC implemente recibir mensaje la marca
- Redirección de stdin y stdout canalización de proceso de Linux (GH #2)
    - Permite que la canalización de comandos - c de bash de CMD.  Ejemplo: > dir | Bash -c "foo grep"
- Bash ahora se puede instalar en sistemas con varios archivos de paginación (538 GH #, #358)
- Tamaño de búfer predeterminado INET Socket debe coincidir con la del programa de instalación de Ubuntu predeterminado
- Alinear xattr syscalls a listxattr
- Devolver solo las interfaces con una dirección IPv4 válida de SIOCGIFCONF
- Corregir la acción predeterminada de señal cuando ptrace insertado
- implement /proc/sys/vm/min_free_kbytes
- Use los valores de registro de contexto de equipo cuando se restaura el contexto en sigreturn
    - Esto resuelve el problema donde estaban francesa java y javac para algunos usuarios
- Implement /proc/sys/kernel/hostname

### <a name="syscall-support"></a>Soporte técnico de syscall
A continuación se muestran una lista de nuevas o mejoradas syscalls que tienen alguna implementación en WSL. Las llamadas en esta lista se admiten en al menos un escenario, pero es posible que no dispone de todos los parámetros compatibles en este momento.

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a>Compilar 14388 a Windows 10 Anniversary Update
Para Windows general, visite información sobre las compilación 14388 el [Blog Windows](https://aka.ms/14388wip). <br/>

### <a name="fixed"></a>Fijo
- Correcciones para prepararse para la actualización de aniversario de Windows 10 en 8/2
  - Puede encontrar más información acerca de WSL en la actualización de aniversario en nuestra [blog](https://blogs.msdn.microsoft.com/wsl/)

<br/>

## <a name="build-14376"></a>Compilación 14376
Para Windows general, visite información sobre las compilación 14376 el [Blog Windows](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/). <br/>

### <a name="fixed"></a>Fijo
- Quitar algunas instancias que apt-get bloquea (GH #493)
- Se ha corregido un problema donde montajes vacíos no se controlan correctamente
- Se ha corregido un problema donde ramdisks no se han montado correctamente
- La aceptación del socket de unix de cambio para que admita indicadores (parcial GH #451)
- Fijo red comunes relacionados con la pantalla azul
- Se ha corregido la pantalla azul al obtener acceso a [pid] / proc / / (GH #523) de tareas
- Uso de CPU elevado fija para algunos escenarios de pty (488 GH #, #504)
- Las mejoras y correcciones de errores adicionales

<br/>

## <a name="build-14371"></a>Compilación 14371
Para Windows general, visite información sobre las compilación 14371 el [Blog Windows](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/). <br/>

### <a name="fixed"></a>Fijo
- Se ha corregido la carrera de temporización con SIGCHLD y wait() al usar ptrace
- Se ha corregido un comportamiento determinado cuando las rutas de acceso tienen un carácter final / (GH #432)
- Se corrigió un problema con el cambio de nombre o desvincular errores debido a los identificadores abiertos en los elementos secundarios
- Las mejoras y correcciones de errores adicionales

<br/>

## <a name="build-14366"></a>Compilación 14366
Para Windows general, visite información sobre las compilación 14366 el [Blog Windows](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/). <br/>

### <a name="fixed"></a>Fijo
- Corregir en la creación de archivos a través de vínculos simbólicos
-   Se ha agregado listxattr para Python (GH 385)
-   Las mejoras y correcciones de errores adicionales

### <a name="syscall-support"></a>Soporte técnico de syscall
-   A continuación se muestran una lista de nuevas o mejoradas syscalls que tienen alguna implementación en WSL. Las llamadas en esta lista se admiten en al menos un escenario, pero es posible que no dispone de todos los parámetros compatibles en este momento.

`listxattr`<br/>
<br/>

## <a name="build-14361"></a>Compilación 14361
Para Windows general información en la compilación 14361, visite la [Blog Windows](https://aka.ms/wip14361). <br/>

### <a name="fixed"></a>Fijo
- DrvFs ahora distingue mayúsculas de minúsculas cuando se ejecuta en Bash en Ubuntu en Windows.
  - Los usuarios mayo case.txt y CASE. Las unidades de TXT en su/mnt/c
  - Mayúsculas y minúsculas sólo se admiten en Bash en Ubuntu en Windows. Cuando fuera de Bash NTFS notificará los archivos correctamente, pero puede producirse un comportamiento inesperado, interactuar con los archivos de Windows.
  - La raíz de cada volumen (es decir, /mnt/c) no distingue mayúsculas de minúsculas
  - Puede encontrar más información sobre cómo administrar estos archivos en Windows [aquí](https://support.microsoft.com/en-us/kb/100625).
- Mejorado en gran medida pty / tty soporte.  Aplicaciones como TMUX ahora admiten (GH 40 de #)
- Problema de instalación fijo donde no siempre crean cuentas de usuario
- Lo que permite una lista de argumentos demasiado largas de línea de comandos arg estructura optimizada. (GH #153)
- Ahora se puede eliminar y chmod archivos read_only desde DrvFs
- Se ha corregido algunas instancias donde los bloqueos en terminal desconexión (GH #43)
- chmod y chown ahora funcionan en dispositivos de tty
- Permitir la conexión a 0.0.0.0 y:: como localhost (GH 388)
- Sendmsg/recvmsg controlan ahora una longitud del vector de E/S de > 1 (parcial GH #376)
- Los usuarios pueden ahora participar del archivo de hosts generada automáticamente (GH 398 de #)
- Configuración regional de Linux con la configuración regional de NT hace coincidir automáticamente durante la instalación (GH #11)
- Agrega el archivo /proc/sys/vm/swappiness (GH #306)
- strace ahora se cierra correctamente
- Permitir que las canalizaciones volver a abrirse mediante /proc/self/fd (GH #222)
- Ocultar directorios bajo %LOCALAPPDATA%\lxss desde DrvFs (GH #270)
- Mejor control de bash.exe ~.  Comandos como "bash ~ ls - c" ahora admite (GH #467)
- Sockets notifican epoll lectura disponible durante el cierre (GH #271)
- lxrun / uninstall hace un mejor trabajo eliminando los archivos y carpetas
- Corregido ps -f (GH #246)
- Compatibilidad mejorada para x11 aplicaciones como xEmacs (GH #481)
- Actualiza el tamaño de pila del subproceso inicial para que coincida con la configuración predeterminada de Ubuntu e informar el tamaño correctamente a la syscall get_rlimit (172 GH #, #258)
- Informe mejorado de los nombres de imagen de proceso de pico (por ejemplo, para la auditoría)
- /Proc/mountinfo implementada para el comando df
- Se ha corregido el código de error de vínculo simbólico para el nombre del elemento secundario. y...
- Las mejoras y correcciones de errores de mejoras adicionales

### <a name="syscall-support"></a>Soporte técnico de syscall
A continuación se muestran una lista de nuevas o mejoradas syscalls que tienen alguna implementación en WSL. Las llamadas en esta lista se admiten en al menos un escenario, pero es posible que no dispone de todos los parámetros compatibles en este momento.

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a>Compilación 14352
Para Windows general, visite información sobre las compilación 14352 el [Blog Windows](https://aka.ms/wip14352).<br/>


### <a name="fixed"></a>Fijo
- Se corrigió un problema donde los archivos grandes no se han descargado / creado correctamente.  Esto debe desbloquear npm y otros escenarios (3 GH, GH #313)
- Quitar algunas instancias donde sockets de bloqueo
- Corregir algunos errores ptrace
- Se corrigió un problema con WSL que permite a los nombres de archivo más de 255 caracteres
- Compatibilidad mejorada para los caracteres no válidos
- Agregar datos de zona horaria de Windows actuales y establecer como predeterminado
- Identificador de dispositivo único para cada punto de montaje (corrección de jre – GH #49)
- Corregir el problema con las rutas que contengan "." y ".."
- Se ha agregado compatibilidad de Fifo (GH #71)
- Formato actualizado de resolv.conf para que coincida con el formato nativo de Ubuntu
- Alguna limpieza procfs
- Ping habilitado para las consolas de administrador (GH #18)

### <a name="syscall-support"></a>Soporte técnico de syscall
A continuación se muestran una lista de nuevas o mejoradas syscalls que tienen alguna implementación en WSL. Las llamadas en esta lista se admiten en al menos un escenario, pero es posible que no dispone de todos los parámetros compatibles en este momento.

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a>Compilación 14342
Para Windows general de información sobre compilación 14342 el [Blog Windows](https://aka.ms/wip14342). <br/>

Puede encontrar información sobre VolFs y DriveFs en el [WSL Blog](https://blogs.msdn.microsoft.com/wsl). <br/>

### <a name="fixed"></a>Fijo
- Se ha corregido el problema de instalación cuando el usuario de Windows tuvo caracteres Unicode en el nombre de usuario
- Ahora se proporciona la solución de udev de actualización de apt-get en las preguntas más frecuentes de forma predeterminada en la primera ejecución
- Habilita los vínculos simbólicos en DriveFs (/ mnt /<drive>) directorios
- Los vínculos simbólicos ahora funcionan entre DriveFs y VolFs
- Ruta direccionada de nivel superior al analizar el problema: ls. / / ahora funcionará según lo esperado
- instalar NPM en DriveFs y ahora trabaja las opciones -g
- Se corrigió un problema impide que el servidor PHP iniciar
- Valores de entorno actualizado de forma predeterminada, como $PATH para más cercano que coincida con Ubuntu nativo
- Agrega una tarea de mantenimiento semanal en Windows para actualizar la caché de paquetes apt
- Se ha corregido el problema con la validación del encabezado de ELF, WSL ahora es compatible con todas las opciones de Melkor
- Shell Zsh es funcional
- Ahora se admiten los binarios precompilados de Go
- Preguntar en Bash.exe primero ejecute ahora se traduce correctamente
- /proc/meminfo ahora devuelve la información correcta
- Sockets, que ahora se admiten en VFS
- / dev ahora está montado como tempfs
- FIFO admitidos ahora
- Sistemas de varios núcleos ahora muestran correctamente en/proc/cpuinfo
- Mejoras adicionales y mensajes de error de descarga durante la primera ejecución
- Syscall mejoras y correcciones de errores. Syscall compatible la lista siguiente.
- Las mejoras y correcciones de errores adicionales

### <a name="known-issues"></a>Problemas conocidos
- No resolver '..' correctamente en DriveFs en algunos casos

### <a name="syscall-support"></a>Soporte técnico de syscall
A continuación se muestran una lista de nuevas o mejoradas syscalls que tienen alguna implementación en WSL. Las llamadas en esta lista se admiten en al menos un escenario, pero es posible que no dispone de todos los parámetros compatibles en este momento.

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

Para Windows general, visite información sobre las compilación 14332 el [Blog Windows](https://aka.ms/wip14332). <br/>


### <a name="fixed"></a>Fijo
- Mejor generación de resolv.conf incluidos dando prioridad a las entradas de DNS
- Problema con el traslado de archivos y directorios entre/mnt y no- / mnt unidades
- Ahora se pueden crear los archivos tar con vínculos simbólicos
- Directorio de /run/lock predeterminada se ha agregado en la creación de instancias
- Actualizar/dev/null para devolver la información de estadísticas correcta
- Errores adicionales cuando se descargan durante la primera ejecución
- Syscall mejoras y correcciones de errores. Syscall compatible la lista siguiente.
- Las mejoras y correcciones de errores de mejoras adicionales

### <a name="syscall-support"></a>Soporte técnico de syscall
A continuación es el nuevo syscall que tiene alguna implementación en WSL. La syscall en esta lista es compatible con al menos un escenario, pero es posible que no dispone de todos los parámetros compatibles en este momento.

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a>Compilación 14328

Para Windows general, visite información sobre las compilación 14332 el [Blog Windows](https://aka.ms/wip14328). <br/>


### <a name="new-features"></a>Nuevas características
* Admite ahora los usuarios de Linux.  Instalación de Bash en Ubuntu en Windows solicitará para la creación de un usuario de Linux.  Para obtener más información, visite https://aka.ms/wslusers
* Nombre de host se establece ahora en el nombre del equipo Windows, no hay más @localhost
* Para obtener más información sobre compilación 14328, visite: https://aka.ms/wip14328

### <a name="fixed"></a>Fijo
* Mejoras de vínculo simbólico para que no es/mnt /<drive> archivos
    * NPM install ahora funciona
    * JDK / jre ahora instalable con instrucciones que encontrará [aquí](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).
    * problema conocido: los vínculos simbólicos no funcionan para Windows monta.  Funcionalidad estará disponible en una compilación posterior
* parte superior y htop se muestran ahora
* Mensajes de error adicionales para algunos errores de la instalación
* Syscall mejoras y correcciones de errores.  Syscall compatible la lista siguiente.
* Las mejoras y correcciones de errores de mejoras adicionales

### <a name="syscall-support"></a>Soporte técnico de syscall
A continuación es una lista de llamadas que tienen alguna implementación en WSL.  Syscall en esta lista se admite en al menos un escenario, pero es posible que no dispone de todos los parámetros compatibles en este momento.

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
