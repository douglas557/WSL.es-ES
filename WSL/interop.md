---
title: Interoperabilidad de Windows con Linux
description: Describe la interoperabilidad de Windows con las distribuciones de Linux que se ejecuta en el subsistema de Windows para Linux.
author: scooley
ms.author: scooley
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.openlocfilehash: 5dcfe0987ecb6615fbe1ab67d178679ac6ad9317
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063253"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a>Subsistema de Windows para la interoperabilidad de Linux con Windows

> **Actualizado para Fall Creators Update.**  
Si ejecuta Creators Update o actualización de aniversario, vaya a la [la sección actualización de aniversario decreadores/](interop.md#creators-update-and-anniversary-update).

El subsistema de Windows para Linux (WSL) mejora continuamente la integración entre Windows y Linux.  Se puede hacer lo siguiente:

1. Invocación de los archivos binarios de Windows desde la consola de Linux.
1. Invocación de los archivos binarios de Linux desde una consola de Windows.
1. **Las compilaciones de Windows Insiders 17063 +** comparten las mismas variables de entorno entre Windows y Linux.

Esto ofrece una experiencia sin problemas entre Windows y WSL.  Los detalles técnicos están en el [WSL blog](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).

## <a name="run-linux-tools-from-a-windows-command-line"></a>Ejecutar herramientas de Linux desde una línea de comandos de Windows

Ejecutar archivos binarios de Linux desde la línea de comandos de Windows (CMD o PowerShell) mediante `wsl.exe <command>`.

Archivos binarios que se invoca de esta manera:

1. Use el mismo directorio de trabajo como el actual mensaje CMD o PowerShell.
1. Ejecutar como usuario WSL predeterminado.
1. Tener los mismos derechos administrativos de Windows como el proceso de llamada y el terminal.

Por ejemplo:

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

El siguiente comando de Linux `wsl.exe` se administra como cualquier comando que se ejecute en WSL.  Funcionará como sudo, la canalización y redirección de archivos.

Ejemplo de uso de sudo:

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

Ejemplos de combinación de comandos WSL y Windows:

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

Los comandos que se pasan a `wsl.exe` se reenvían al proceso WSL sin ninguna modificación.  Las rutas de acceso de archivo deben especificarse en el formato WSL.

Ejemplo con las rutas de acceso:

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a>Ejecutar herramientas de Windows desde WSL

WSL puede invocar los archivos binarios de Windows directamente desde la línea de comandos WSL mediante `[binary name].exe`.  Por ejemplo: `notepad.exe`.  Para facilitar la ejecución de los archivos ejecutables de Windows, la ruta de acceso de Windows se incluye en el sistema operativo Linux `$PATH` en Fall Creators Update.

Las aplicaciones se ejecutan de esta forma tienen las siguientes propiedades:

1. Conservar el directorio de trabajo como el símbolo del sistema de WSL (la mayor parte, las excepciones se explican a continuación).
1. Tener los mismos derechos de permiso que el proceso WSL.
1. Ejecutar como el usuario de Windows activo.
1. Aparecen en el Administrador de tareas de Windows como si se ejecuta directamente desde el símbolo del sistema.

Por ejemplo:

``` BASH
$ notepad.exe
```

Archivos ejecutables de Windows para ejecutar en WSL se administran de forma similar ejecutables nativos de Linux--tuberías redirecciones e incluso procesamiento en segundo plano trabajo según lo previsto.

Ejemplos de uso de canalizaciones:

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

Ejemplo de uso de comandos de Windows y WSL mixtos:

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

Archivos binarios de Windows deben incluir la extensión de archivo, coincidir con el caso de archivo y se pueda ejecutar.  Incluidos los ejecutables no procesar por lotes las secuencias de comandos.  Al igual que los comandos nativos de CMD `dir` se pueden ejecutar con `cmd.exe /C` comando.

Ejemplos:

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

Los parámetros se pasan a los binarios de Windows sin modificar.

Por ejemplo, se abren los siguientes comandos `C:\temp\foo.txt` en `notepad.exe`:

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

Modificación de archivos ubicados en VolFs (no en archivos `/mnt/<x>`) con un Windows no se admite la aplicación en WSL.

De forma predeterminada, WSL intenta mantener el directorio de trabajo de la Windows binario como el directorio actual de WSL, pero se revertirá en el directorio de la creación de instancia si el directorio de trabajo se encuentra en VolFs.

Como ejemplo; `wsl.exe` inicialmente se inicia desde `C:\temp` y se cambia el directorio WSL actual a la página principal del usuario.  Cuando `notepad.exe` se llama desde el directorio del usuario principal, WSL se revierte automáticamente a `C:\temp` como el directorio de trabajo notepad.exe:

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

## <a name="share-environment-variables-between-windows-and-wsl"></a>Variables de entorno del recurso compartido entre Windows y WSL

> Está disponible en las compilaciones de Windows Insider 17063 y versiones posteriores.

Antes de 17063, fue sólo variable de entorno de Windows que puede tener acceso WSL `PATH` (por lo que también puede iniciar archivos ejecutables de Win32 en WSL).

A partir de 17063, WSL y Windows comparten `WSLENV`, una variable de entorno especiales creada para superar las distribuciones de Windows y Linux que se ejecutan en WSL.

Propiedades de `WSLENV`:

* Que es compartido; existe en entornos tanto Windows como WSL.
* Es una lista de variables de entorno para compartir entre Windows y WSL.
* Pueden dar formato a las variables de entorno para que funcione bien en Windows y WSL.

Hay cuatro indicadores en `WSLENV` para influir en cómo se traduce esa variable de entorno.

`WSLENV` indicadores:

* `/p` : convierte la ruta de acceso entre las rutas de acceso de estilo WSL/Linux y las rutas de acceso de Win32.
* `/l` -indica que la variable de entorno es una lista de rutas de acceso.
* `/u` -indica que esta variable de entorno solo se debe incluir cuando se ejecuta WSL desde Win32.
* `/w` -indica que esta variable de entorno solo se debe incluir cuando se ejecuta Win32 desde WSL.

Las marcas se pueden combinar según sea necesario.

## <a name="disable-interop"></a>Deshabilitar la interoperabilidad

Los usuarios pueden deshabilitar la capacidad de ejecutar los archivos binarios de Windows en una sola sesión WSL ejecutando el siguiente comando como raíz:

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

Para volver a habilitar Windows archivos binarios de salir de todas las sesiones WSL y vuelva a ejecutan bash.exe o lo ejecutan el siguiente comando como raíz:

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

Deshabilitación de interoperabilidad no se conservará entre sesiones WSL: interoperabilidad volverá a activarse cuando se inicia una nueva sesión.

## <a name="creators-update-and-anniversary-update"></a>Creators Update y actualización de aniversario

Aunque el otoño interoperabilidad experiencia previa Creators Update es similar a las experiencias más recientes de interoperabilidad, hay un handfull de las principales diferencias.

Para resumir:

* `bash.exe` se ha desusado y se reemplazan con `wsl.exe`.
* `-c` opción para ejecutar un comando único no es necesario con `wsl.exe`.
* Ruta de acceso de Windows se incluye en el WSL `$PATH`

Se ha modificado el proceso de deshabilitar la interoperabilidad.

### <a name="invoking-wsl-from-the-windows-command-line"></a>Invocar WSL desde la línea de comandos de Windows

Los archivos binarios de Linux se pueden invocar desde el símbolo del sistema de Windows o desde PowerShell.  Los archivos binarios que se invoca de esta manera tienen las siguientes propiedades:

1. Use el mismo directorio de trabajo como el símbolo del sistema CMD o PowerShell.
1. Ejecutar como usuario WSL predeterminado.
1. Tener los mismos derechos administrativos de Windows como el proceso de llamada y el terminal.

Por ejemplo:

```console
C:\temp> bash -c "ls -la"
```

Comandos de Linux denominados de esta manera se administran como cualquier otra aplicación de Windows.  Cosas como entrada, la canalización y redirección de archivos funcionan según lo previsto.

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

Los comandos WSL pasan `bash -c` se reenvían al proceso WSL sin ninguna modificación.  Las rutas de acceso de archivo deben especificarse en el formato WSL y debe tener cuidado para escapar caracteres pertinentes. Por ejemplo:

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a>Invocación de los archivos binarios de Windows de WSL

El subsistema de Windows para Linux puede invocar directamente desde la línea de comandos WSL archivos binarios de Windows.  Las aplicaciones se ejecutan de esta forma tienen las siguientes propiedades:

1. Conservar el directorio de trabajo como el símbolo WSL, excepto en el escenario que se explica más adelante.
1. Tiene los mismos derechos de permiso que el `bash.exe` proceso. 
1. Ejecutar como el usuario de Windows activo.
1. Aparecen en el Administrador de tareas de Windows como si se ejecuta directamente desde el símbolo del sistema.

Por ejemplo:

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

En WSL, estos ejecutables se tratan como ejecutables nativos de Linux.  Esto significa agregar directorios a la ruta de acceso de Linux y se canaliza entre works comandos según lo previsto.  Ejemplos:

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

El archivo binario de Windows debe incluir la extensión de archivo, coincide con el caso de archivo y se pueda ejecutar.  Archivos ejecutables no incluidos por lotes de scripts y comandos como `dir` se pueden ejecutar con `/mnt/c/Windows/System32/cmd.exe /C` comando.

Ejemplos:

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

Los parámetros se pasan a los binarios de Windows sin modificar.  

Por ejemplo, se abren los siguientes comandos `C:\temp\foo.txt` en `notepad.exe`:

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

Modificación de archivos ubicados en VolFs (no en archivos `/mnt/<x>`) con un Windows no se admite la aplicación.  De forma predeterminada, WSL intenta mantener el directorio de trabajo de la Windows binario como el directorio actual de WSL, pero se revertirá en el directorio de la creación de instancia si el directorio de trabajo se encuentra en VolFs.

Como ejemplo; `bash.exe` inicialmente se inicia desde `C:\temp` y se cambia el directorio WSL actual a la página principal del usuario.  Cuando `notepad.exe` se llama desde el directorio del usuario principal, WSL se revierte automáticamente a `C:\temp` como el directorio de trabajo notepad.exe:

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
