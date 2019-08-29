---
title: Interoperabilidad de Windows con Linux
description: Describe la interoperabilidad de Windows con distribuciones de Linux que se ejecutan en el subsistema de Windows para Linux.
author: scooley
ms.author: scooley
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 3f3df3337ece75d7af77313f5fc55eb4e18e31cb
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122730"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a>Windows Subsystem for Linux Interoperability with Windows

> **Actualizado para Fall Creators Update.**  
Si está ejecutando Creators Update o actualización de aniversario, vaya a la [sección Creators/actualización de aniversario](interop.md#creators-update-and-anniversary-update).

El subsistema de Windows para Linux (WSL) está mejorando continuamente la integración entre Windows y Linux.  Puede:

1. Invocar archivos binarios de Windows desde la consola de Linux.
1. Invocar archivos binarios de Linux desde una consola de Windows.
1. Compilaciones de **Windows Insider 17063 +** Compartir variables de entorno entre Linux y Windows.

Esto ofrece una experiencia perfecta entre Windows y WSL.  Los detalles técnicos se encuentran en el [blog de WSL](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).

## <a name="run-linux-tools-from-a-windows-command-line"></a>Ejecutar herramientas de Linux desde una línea de comandos de Windows

Ejecute los archivos binarios de Linux desde el símbolo del sistema de Windows ( `wsl.exe <command>`CMD o PowerShell) mediante.

Los archivos binarios se invocan de esta manera:

1. Use el mismo directorio de trabajo que el símbolo del sistema actual de CMD o PowerShell.
1. Ejecute como el usuario predeterminado WSL.
1. Tener los mismos derechos administrativos de Windows que el proceso de llamada y el terminal.

Por ejemplo:

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

El comando de Linux `wsl.exe` siguiente se controla como cualquier comando que se ejecute en WSL.  Cosas como sudo, piping y redirección de archivos funcionan.

Ejemplo de uso de sudo:

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

Ejemplos de combinación de WSL y comandos de Windows:

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

Los comandos pasados `wsl.exe` a se reenvían al proceso WSL sin modificarlos.  Las rutas de acceso de archivo deben especificarse en el formato WSL.

Ejemplo con rutas de acceso:

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a>Ejecutar herramientas de Windows desde WSL

WSL puede invocar archivos binarios de Windows directamente desde la línea `[binary name].exe`de comandos de WSL mediante.  Por ejemplo: `notepad.exe`.  Para facilitar la ejecución de archivos ejecutables de Windows, la ruta de acceso `$PATH` de Windows se incluye en Linux in Fall Creators Update.

Las aplicaciones que se ejecutan de esta manera tienen las siguientes propiedades:

1. Conserve el directorio de trabajo como el símbolo del sistema de WSL (en la mayoría de los casos, las excepciones se explican a continuación).
1. Tienen los mismos derechos de permiso que el proceso WSL.
1. Ejecute como el usuario activo de Windows.
1. Aparecen en el administrador de tareas de Windows como si se ejecutaran directamente desde el símbolo del sistema.

Ejemplo:

``` BASH
$ notepad.exe
```

Los ejecutables de Windows que se ejecutan en WSL se administran de forma similar a los ejecutables nativos de Linux: canalización, redireccionamiento e incluso trabajo de fondo según lo previsto.

Ejemplos de uso de canalizaciones:

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

Ejemplo de uso de ventanas mixtas y comandos WSL:

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

Los archivos binarios de Windows deben incluir la extensión de archivo, coincidir con el caso del archivo y ser ejecutable.  No ejecutables, incluidos scripts por lotes.  Los comandos nativos de `dir` cmd como pueden ejecutarse con `cmd.exe /C` el comando.

Ejemplos:

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

Los parámetros se pasan al binario de Windows sin modificar.

Por ejemplo, los siguientes comandos se abrirán `C:\temp\foo.txt` en `notepad.exe`:

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

No se admite la modificación de archivos ubicados en VolFs `/mnt/<x>`(archivos no bajo) con una aplicación de Windows en WSL.

De forma predeterminada, WSL intenta mantener el directorio de trabajo del archivo binario de Windows como el directorio WSL actual, pero revertirá en el directorio de creación de la instancia si el directorio de trabajo se encuentra en VolFs.

Por ejemplo: se inicia inicialmente desde `C:\temp` y el directorio WSL actual se cambia a la Página principal del usuario. `wsl.exe`  Cuando `notepad.exe` se llama a desde el directorio particular del usuario, WSL se revierte automáticamente `C:\temp` a como el directorio de trabajo del Bloc de notas. exe:

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

## <a name="share-environment-variables-between-windows-and-wsl"></a>Compartir variables de entorno entre Windows y WSL

> Disponible en las compilaciones de Windows Insider 17063 y versiones posteriores.

Antes de 17063, solo podía tener acceso a la variable de entorno `PATH` de Windows a la que WSL podía tener acceso (por lo que podía iniciar archivos ejecutables de Win32 desde en WSL).

A partir de 17063, WSL y Windows `WSLENV`Share, una variable de entorno especial que se crea para el puente entre Windows y Linux distribuciones que se ejecuta en WSL.

Propiedades de `WSLENV`:

* Está compartida; existe en entornos Windows y WSL.
* Se trata de una lista de variables de entorno que se pueden compartir entre Windows y WSL.
* Puede dar formato a las variables de entorno para que funcionen bien en Windows y WSL.

Hay cuatro marcas disponibles en para `WSLENV` influir en la forma en que se traduce esa variable de entorno.

`WSLENV`marcas

* `/p`: traduce la ruta de acceso entre las rutas de acceso de estilo de WSL/Linux y las rutas de acceso de Win32.
* `/l`: indica que la variable de entorno es una lista de rutas de acceso.
* `/u`: indica que esta variable de entorno solo debe incluirse al ejecutar WSL desde Win32.
* `/w`: indica que esta variable de entorno solo debe incluirse cuando se ejecute Win32 desde WSL.

Las marcas se pueden combinar según sea necesario.

## <a name="disable-interop"></a>Deshabilitar interoperabilidad

Los usuarios pueden deshabilitar la capacidad de ejecutar archivos binarios de Windows para una única sesión de WSL mediante la ejecución del siguiente comando como raíz:

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

Para volver a habilitar los archivos binarios de Windows, salga de todas las sesiones de WSL y vuelva a ejecutar bash. exe o ejecute el siguiente comando como raíz:

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

La deshabilitación de la interoperabilidad no se conservará entre sesiones de WSL: la interoperabilidad se habilitará de nuevo cuando se inicie una nueva sesión.

## <a name="creators-update-and-anniversary-update"></a>Creators Update y actualización de aniversario

Aunque la experiencia de interoperabilidad de los creadores de la actualización es similar a las experiencias de interoperabilidad más recientes, hay algunas diferencias importantes.

En Resumen:

* `bash.exe`ha quedado en desuso y se ha `wsl.exe`reemplazado por.
* `-c`la opción para ejecutar un único comando no es `wsl.exe`necesaria con.
* La ruta de acceso de Windows se incluye en WSL`$PATH`

El proceso para deshabilitar la interoperabilidad no ha cambiado.

### <a name="invoking-wsl-from-the-windows-command-line"></a>Invocar WSL desde la línea de comandos de Windows

Los archivos binarios de Linux se pueden invocar desde el símbolo del sistema de Windows o desde PowerShell.  Los archivos binarios que se invocan de esta manera tienen las propiedades siguientes:

1. Use el mismo directorio de trabajo que el símbolo del sistema de CMD o PowerShell.
1. Ejecute como el usuario predeterminado WSL.
1. Tener los mismos derechos administrativos de Windows que el proceso de llamada y el terminal.

Ejemplo:

```console
C:\temp> bash -c "ls -la"
```

Los comandos de Linux a los que se llama de esta manera se administran como cualquier otra aplicación de Windows.  Cosas como la entrada, la canalización y el redireccionamiento de archivos funcionan según lo previsto.

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

Los comandos de WSL que `bash -c` se pasan a se reenvían al proceso WSL sin modificarlos.  Las rutas de acceso de archivo deben especificarse en el formato WSL y se debe tener cuidado para escapar caracteres relevantes. Ejemplo:

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a>Invocar archivos binarios de Windows desde WSL

El subsistema de Windows para Linux puede invocar archivos binarios de Windows directamente desde la línea de comandos de WSL.  Las aplicaciones que se ejecutan de esta manera tienen las siguientes propiedades:

1. Conserve el directorio de trabajo como el símbolo del sistema de WSL, excepto en el escenario que se explica a continuación.
1. Tener los mismos derechos de permiso que `bash.exe` el proceso. 
1. Ejecute como el usuario activo de Windows.
1. Aparecen en el administrador de tareas de Windows como si se ejecutaran directamente desde el símbolo del sistema.

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

El binario de Windows debe incluir la extensión de archivo, coincidir con el caso del archivo y ser ejecutable.  Los no ejecutables, incluidos los scripts `dir` por lotes y el `/mnt/c/Windows/System32/cmd.exe /C` comando like, se pueden ejecutar con el comando.

Ejemplos:

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

Los parámetros se pasan al binario de Windows sin modificar.  

Por ejemplo, los siguientes comandos se abrirán `C:\temp\foo.txt` en `notepad.exe`:

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

No se admite la modificación de archivos ubicados en VolFs `/mnt/<x>`(archivos no bajo) con una aplicación de Windows.  De forma predeterminada, WSL intenta mantener el directorio de trabajo del archivo binario de Windows como el directorio WSL actual, pero revertirá en el directorio de creación de la instancia si el directorio de trabajo se encuentra en VolFs.

Por ejemplo: se inicia inicialmente desde `C:\temp` y el directorio WSL actual se cambia a la Página principal del usuario. `bash.exe`  Cuando `notepad.exe` se llama a desde el directorio particular del usuario, WSL se revierte automáticamente `C:\temp` a como el directorio de trabajo del Bloc de notas. exe:

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
