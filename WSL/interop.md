---
title: Interoperabilidad de Windows con Linux
description: Describe la interoperabilidad de Windows con distribuciones de Linux que se ejecutan en el subsistema de Windows para Linux.
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: f8b0150c044f5011b84e80cac4befd752c4dc552
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269805"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a>Interoperabilidad del subsistema de Windows para Linux con Windows

> **Actualización de Fall Creators Update**.  
Si estás ejecutando Creators Update o la Actualización de aniversario, ve a la [sección Creators Update/Actualización de aniversario](interop.md#creators-update-and-anniversary-update).

El subsistema de Windows para Linux (WSL) está mejorando continuamente la integración entre Windows y Linux.  Se puede hacer lo siguiente:

1. Invocar archivos binarios de Windows desde la consola de Linux.
1. Invocar archivos binarios de Linux desde la consola de Windows.
1. **Compilaciones 17063 y posteriores de Windows Insider**: compartir variables de entorno entre Linux y Windows.

Esto ofrece una experiencia perfecta entre Windows y WSL.  Los detalles técnicos se encuentran en el [blog de WSL](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).

## <a name="run-linux-tools-from-a-windows-command-line"></a>Ejecución de herramientas de Linux desde una línea de comandos de Windows

Ejecuta los archivos binarios de Linux desde el símbolo del sistema de Windows (CMD o PowerShell) mediante `wsl.exe <command>`.

Los archivos binarios se invocan de esta manera:

1. Usan el mismo directorio de trabajo que el símbolo del sistema actual de CMD o PowerShell.
1. Se ejecutan como usuario predeterminado de WSL.
1. Tienen los mismos derechos administrativos de Windows que el terminal y el proceso de llamada.

Por ejemplo:

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

El comando de Linux `wsl.exe` siguiente se controla como cualquier comando que se ejecute en WSL.  Funcionan cosas como sudo, canalizaciones y redireccionamientos de archivos.

Ejemplo con sudo:

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

Ejemplos de combinación de comandos de Windows y WSL:

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

Los comandos pasados a `wsl.exe` se reenvían al proceso de WSL sin modificaciones.  Las rutas de acceso de archivo deben especificarse en el formato de WSL.

Ejemplo con rutas de acceso:

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a>Ejecución de herramientas de Windows desde WSL

WSL puede invocar archivos binarios de Windows directamente desde la línea de comandos de WSL mediante `[binary name].exe`.  Por ejemplo, `notepad.exe`.  Para facilitar la ejecución de archivos ejecutables de Windows, la ruta de acceso de Windows se incluye en `$PATH` de Linux en Fall Creators Update.

Las aplicaciones que se ejecutan de esta manera tienen las siguientes propiedades:

1. Conservan el directorio de trabajo como el símbolo del sistema de WSL (en la mayoría de los casos; las excepciones se explican a continuación).
1. Tienen los mismos derechos de permiso que el proceso de WSL.
1. Se ejecutan como el usuario activo de Windows.
1. Aparecen en el administrador de tareas de Windows como si se ejecutaran directamente desde el símbolo del sistema de CMD.

Ejemplo:

``` BASH
$ notepad.exe
```

Los archivos ejecutables de Windows que se ejecutan en WSL se administran de forma similar a los ejecutables nativos de Linux; las canalizaciones, los redireccionamientos e incluso los procesos en segundo plano funcionan según lo previsto.

Ejemplos con canalizaciones:

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

Ejemplo con comandos de WSL y Windows combinados:

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

Los archivos binarios de Windows deben incluir la extensión de archivo, coincidir con el caso del archivo y ser ejecutables.  Los no ejecutables, incluidos los scripts por lotes y  comandos nativos de CMD como `dir`, se pueden ejecutar con el comando `cmd.exe /C`.

Ejemplos:

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

Los parámetros se pasan al archivo binario de Windows sin modificar.

Por ejemplo, los siguientes comandos abrirán `C:\temp\foo.txt` en `notepad.exe`:

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

No se admite la modificación de archivos ubicados en VolFs (archivos que no están en `/mnt/<x>`) con una aplicación de Windows en WSL.

De manera predeterminada, WSL intenta mantener el directorio de trabajo del archivo binario de Windows como directorio de WSL actual, pero recurrirá al directorio de creación de la instancia si el directorio de trabajo se encuentra en VolFs.

Por ejemplo: en un principio, `wsl.exe` se inicia desde `C:\temp` y el directorio de WSL actual se cambia a la página principal del usuario.  Cuando `notepad.exe` se llama desde el directorio particular del usuario, WSL recurre automáticamente a `C:\temp` como directorio de trabajo de notepad.exe:

``` BASH
C:\temp> wsl
/mnt/c/temp/$ cd ~
~$ notepad.exe foo.txt
~$ ls | grep foo.txt
~$ exit

exit
C:\temp>dir | findstr foo.txt
09/27/2016  02:15 PM                14 foo.txt
```

## <a name="share-environment-variables-between-windows-and-wsl"></a>Uso compartido de variables de entorno entre Windows y WSL

> Disponible en compilaciones 17063 de Windows Insider y versiones posteriores.

Antes de la versión 17063, la única variable de entorno de Windows a la que podía tener acceso WSL era `PATH`, por lo que se podían iniciar ejecutables de Win32 desde WSL.

A partir de la versión 17063, WSL y Windows comparten `WSLENV`, una variable de entorno especial creada para unir las distribuciones de Windows y Linux que se ejecutan en WSL.

Propiedades de `WSLENV`:

* Se comparte; existe en entornos de Windows y WSL.
* Se trata de una lista de variables de entorno que se pueden compartir entre Windows y WSL.
* Puede formatear variables de entorno para que funcionen correctamente en Windows y WSL.

Hay cuatro marcas disponibles en `WSLENV` que pueden influir en la forma en que se traduce esa variable de entorno.

Marcas `WSLENV`:

* `/p`: traduce la ruta de acceso entre las rutas de acceso de estilo de WSL/Linux y las rutas de acceso de Win32.
* `/l`: indica que la variable de entorno es una lista de rutas de acceso.
* `/u`: indica que esta variable de entorno solo debe incluirse al ejecutar WSL desde Win32.
* `/w`: indica que esta variable de entorno solo debe incluirse al ejecutar Win32 desde WSL.

Las marcas se pueden combinar según sea necesario.

## <a name="disable-interop"></a>Deshabilitación de la interoperabilidad

Los usuarios pueden deshabilitar la capacidad de ejecutar archivos binarios de Windows para una única sesión de WSL mediante la ejecución del siguiente comando como raíz:

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

Para volver a habilitar los archivos binarios de Windows, sal de todas las sesiones de WSL y vuelve a ejecutar bash.exe o ejecuta el siguiente comando como raíz:

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

La deshabilitación de la interoperabilidad no se conservará entre sesiones de WSL: la interoperabilidad se habilitará de nuevo cuando se inicie una nueva sesión.

## <a name="creators-update-and-anniversary-update"></a>Creators Update y Actualización de aniversario

Aunque la experiencia de interoperabilidad previa a la actualización Fall Creators Update es similar a las experiencias de interoperabilidad más recientes, hay algunas diferencias importantes.

En resumen:

* `bash.exe` ha quedado en desuso y se ha reemplazado por `wsl.exe`.
* La opción `-c` para ejecutar un único comando no es necesaria con `wsl.exe`.
* La ruta de acceso de Windows se incluye en `$PATH` de WSL.

El proceso para deshabilitar la interoperabilidad no ha cambiado.

### <a name="invoking-wsl-from-the-windows-command-line"></a>Invocación de WSL desde la línea de comandos de Windows

Los archivos binarios de Linux se pueden invocar desde el símbolo del sistema de Windows o desde PowerShell.  Los archivos binarios que se invocan de esta manera tienen las siguientes propiedades:

1. Usan el mismo directorio de trabajo que el símbolo del sistema de CMD o PowerShell.
1. Se ejecutan como usuario predeterminado de WSL.
1. Tienen los mismos derechos administrativos de Windows que el terminal y el proceso de llamada.

Ejemplo:

```console
C:\temp> bash -c "ls -la"
```

Los comandos de Linux a los que se llama de esta manera se administran como cualquier otra aplicación de Windows.  Cosas como las entradas, las canalizaciones y los redireccionamientos de archivos funcionan según lo esperado.

Ejemplos:

```console
C:\temp>bash -c "sudo apt-get update"
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

```console
C:\temp> bash -c "ls -la" | findstr foo
C:\temp> dir | bash -c "grep foo"
C:\temp> bash -c "ls -la" > out.txt
```

Los comandos de WSL pasados a `bash -c` se reenvían al proceso de WSL sin modificaciones.  Las rutas de acceso de archivo deben especificarse en el formato de WSL y se debe tener cuidado al escapar caracteres relevantes. Ejemplo:

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a>Invocación de archivos binarios de Windows desde WSL

El subsistema de Windows para Linux puede invocar archivos binarios de Windows directamente desde la línea de comandos de WSL.  Las aplicaciones que se ejecutan de esta manera tienen las siguientes propiedades:

1. Conservan el directorio de trabajo como el símbolo del sistema de WSL, excepto en el escenario que se explica a continuación.
1. Tienen los mismos derechos de permiso que el proceso de `bash.exe`. 
1. Se ejecutan como el usuario activo de Windows.
1. Aparecen en el administrador de tareas de Windows como si se ejecutaran directamente desde el símbolo del sistema de CMD.

Ejemplo:

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

En WSL, estos ejecutables se tratan de forma similar a los ejecutables nativos de Linux.  Esto significa que la adición de directorios a la ruta de acceso de Linux y la canalización entre comandos funciona según lo previsto.  Ejemplos:

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

El archivo binario de Windows debe incluir la extensión de archivo, coincidir con el caso del archivo y ser ejecutable.  Los no ejecutables, incluidos los scripts por lotes y comandos como `dir`, se pueden ejecutar con el comando `/mnt/c/Windows/System32/cmd.exe /C`.

Ejemplos:

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

Los parámetros se pasan al archivo binario de Windows sin modificar.  

Por ejemplo, los siguientes comandos abrirán `C:\temp\foo.txt` en `notepad.exe`:

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

No se admite la modificación de archivos ubicados en VolFs (archivos que no están en `/mnt/<x>`) con una aplicación de Windows.  De manera predeterminada, WSL intenta mantener el directorio de trabajo del archivo binario de Windows como directorio de WSL actual, pero recurrirá al directorio de creación de la instancia si el directorio de trabajo se encuentra en VolFs.

Por ejemplo: en un principio, `bash.exe` se inicia desde `C:\temp` y el directorio de WSL actual se cambia a la página principal del usuario.  Cuando `notepad.exe` se llama desde el directorio particular del usuario, WSL recurre automáticamente a `C:\temp` como directorio de trabajo de notepad.exe:

``` BASH
C:\temp> bash
/mnt/c/temp/$ cd ~
~$ notepad.exe foo.txt
~$ ls | grep foo.txt
~$ exit
exit

C:\temp> dir | findstr foo.txt
09/27/2016  02:15 PM                14 foo.txt
```
