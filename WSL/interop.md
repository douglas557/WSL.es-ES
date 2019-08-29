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
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a><span data-ttu-id="4c07b-103">Windows Subsystem for Linux Interoperability with Windows</span><span class="sxs-lookup"><span data-stu-id="4c07b-103">Windows Subsystem for Linux interoperability with Windows</span></span>

> <span data-ttu-id="4c07b-104">**Actualizado para Fall Creators Update.**</span><span class="sxs-lookup"><span data-stu-id="4c07b-104">**Updated for Fall Creators Update.**</span></span>  
<span data-ttu-id="4c07b-105">Si está ejecutando Creators Update o actualización de aniversario, vaya a la [sección Creators/actualización de aniversario](interop.md#creators-update-and-anniversary-update).</span><span class="sxs-lookup"><span data-stu-id="4c07b-105">If you're running Creators Update or Anniversary Update, jump to the [Creators/Anniversary Update section](interop.md#creators-update-and-anniversary-update).</span></span>

<span data-ttu-id="4c07b-106">El subsistema de Windows para Linux (WSL) está mejorando continuamente la integración entre Windows y Linux.</span><span class="sxs-lookup"><span data-stu-id="4c07b-106">The Windows Subsystem for Linux (WSL) is continuously improving integration between Windows and Linux.</span></span>  <span data-ttu-id="4c07b-107">Puede:</span><span class="sxs-lookup"><span data-stu-id="4c07b-107">You can:</span></span>

1. <span data-ttu-id="4c07b-108">Invocar archivos binarios de Windows desde la consola de Linux.</span><span class="sxs-lookup"><span data-stu-id="4c07b-108">Invoke Windows binaries from the Linux console.</span></span>
1. <span data-ttu-id="4c07b-109">Invocar archivos binarios de Linux desde una consola de Windows.</span><span class="sxs-lookup"><span data-stu-id="4c07b-109">Invoke Linux binaries from a Windows console.</span></span>
1. <span data-ttu-id="4c07b-110">Compilaciones de **Windows Insider 17063 +** Compartir variables de entorno entre Linux y Windows.</span><span class="sxs-lookup"><span data-stu-id="4c07b-110">**Windows Insiders Builds 17063+** Share environment variables between Linux and Windows.</span></span>

<span data-ttu-id="4c07b-111">Esto ofrece una experiencia perfecta entre Windows y WSL.</span><span class="sxs-lookup"><span data-stu-id="4c07b-111">This delivers a seamless experience between Windows and WSL.</span></span>  <span data-ttu-id="4c07b-112">Los detalles técnicos se encuentran en el [blog de WSL](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span><span class="sxs-lookup"><span data-stu-id="4c07b-112">Technical details are on the [WSL blog](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span></span>

## <a name="run-linux-tools-from-a-windows-command-line"></a><span data-ttu-id="4c07b-113">Ejecutar herramientas de Linux desde una línea de comandos de Windows</span><span class="sxs-lookup"><span data-stu-id="4c07b-113">Run Linux tools from a Windows command line</span></span>

<span data-ttu-id="4c07b-114">Ejecute los archivos binarios de Linux desde el símbolo del sistema de Windows ( `wsl.exe <command>`CMD o PowerShell) mediante.</span><span class="sxs-lookup"><span data-stu-id="4c07b-114">Run Linux binaries from the Windows Command Prompt (CMD or PowerShell) using `wsl.exe <command>`.</span></span>

<span data-ttu-id="4c07b-115">Los archivos binarios se invocan de esta manera:</span><span class="sxs-lookup"><span data-stu-id="4c07b-115">Binaries invoked in this way:</span></span>

1. <span data-ttu-id="4c07b-116">Use el mismo directorio de trabajo que el símbolo del sistema actual de CMD o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4c07b-116">Use the same working directory as the current CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="4c07b-117">Ejecute como el usuario predeterminado WSL.</span><span class="sxs-lookup"><span data-stu-id="4c07b-117">Run as the WSL default user.</span></span>
1. <span data-ttu-id="4c07b-118">Tener los mismos derechos administrativos de Windows que el proceso de llamada y el terminal.</span><span class="sxs-lookup"><span data-stu-id="4c07b-118">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="4c07b-119">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="4c07b-119">For example:</span></span>

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

<span data-ttu-id="4c07b-120">El comando de Linux `wsl.exe` siguiente se controla como cualquier comando que se ejecute en WSL.</span><span class="sxs-lookup"><span data-stu-id="4c07b-120">The Linux command following `wsl.exe` is handled like any command run in WSL.</span></span>  <span data-ttu-id="4c07b-121">Cosas como sudo, piping y redirección de archivos funcionan.</span><span class="sxs-lookup"><span data-stu-id="4c07b-121">Things such as sudo, piping, and file redirection work.</span></span>

<span data-ttu-id="4c07b-122">Ejemplo de uso de sudo:</span><span class="sxs-lookup"><span data-stu-id="4c07b-122">Example using sudo:</span></span>

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

<span data-ttu-id="4c07b-123">Ejemplos de combinación de WSL y comandos de Windows:</span><span class="sxs-lookup"><span data-stu-id="4c07b-123">Examples mixing WSL and Windows commands:</span></span>

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

<span data-ttu-id="4c07b-124">Los comandos pasados `wsl.exe` a se reenvían al proceso WSL sin modificarlos.</span><span class="sxs-lookup"><span data-stu-id="4c07b-124">The commands passed into `wsl.exe` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="4c07b-125">Las rutas de acceso de archivo deben especificarse en el formato WSL.</span><span class="sxs-lookup"><span data-stu-id="4c07b-125">File paths must be specified in the WSL format.</span></span>

<span data-ttu-id="4c07b-126">Ejemplo con rutas de acceso:</span><span class="sxs-lookup"><span data-stu-id="4c07b-126">Example with paths:</span></span>

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a><span data-ttu-id="4c07b-127">Ejecutar herramientas de Windows desde WSL</span><span class="sxs-lookup"><span data-stu-id="4c07b-127">Run Windows tools from WSL</span></span>

<span data-ttu-id="4c07b-128">WSL puede invocar archivos binarios de Windows directamente desde la línea `[binary name].exe`de comandos de WSL mediante.</span><span class="sxs-lookup"><span data-stu-id="4c07b-128">WSL can invoke Windows binaries directly from the WSL command line using `[binary name].exe`.</span></span>  <span data-ttu-id="4c07b-129">Por ejemplo: `notepad.exe`.</span><span class="sxs-lookup"><span data-stu-id="4c07b-129">For example, `notepad.exe`.</span></span>  <span data-ttu-id="4c07b-130">Para facilitar la ejecución de archivos ejecutables de Windows, la ruta de acceso `$PATH` de Windows se incluye en Linux in Fall Creators Update.</span><span class="sxs-lookup"><span data-stu-id="4c07b-130">To make Windows executables easier to run, Windows path is included in the Linux `$PATH` in Fall Creators Update.</span></span>

<span data-ttu-id="4c07b-131">Las aplicaciones que se ejecutan de esta manera tienen las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="4c07b-131">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="4c07b-132">Conserve el directorio de trabajo como el símbolo del sistema de WSL (en la mayoría de los casos, las excepciones se explican a continuación).</span><span class="sxs-lookup"><span data-stu-id="4c07b-132">Retain the working directory as the WSL command prompt (for the most part -- exceptions are explained below).</span></span>
1. <span data-ttu-id="4c07b-133">Tienen los mismos derechos de permiso que el proceso WSL.</span><span class="sxs-lookup"><span data-stu-id="4c07b-133">Have the same permission rights as the WSL process.</span></span>
1. <span data-ttu-id="4c07b-134">Ejecute como el usuario activo de Windows.</span><span class="sxs-lookup"><span data-stu-id="4c07b-134">Run as the active Windows user.</span></span>
1. <span data-ttu-id="4c07b-135">Aparecen en el administrador de tareas de Windows como si se ejecutaran directamente desde el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="4c07b-135">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="4c07b-136">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="4c07b-136">Example:</span></span>

``` BASH
$ notepad.exe
```

<span data-ttu-id="4c07b-137">Los ejecutables de Windows que se ejecutan en WSL se administran de forma similar a los ejecutables nativos de Linux: canalización, redireccionamiento e incluso trabajo de fondo según lo previsto.</span><span class="sxs-lookup"><span data-stu-id="4c07b-137">Windows executables run in WSL are handled similarly to native Linux executables -- piping, redirects, and even backgrounding work as expected.</span></span>

<span data-ttu-id="4c07b-138">Ejemplos de uso de canalizaciones:</span><span class="sxs-lookup"><span data-stu-id="4c07b-138">Examples using pipes:</span></span>

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

<span data-ttu-id="4c07b-139">Ejemplo de uso de ventanas mixtas y comandos WSL:</span><span class="sxs-lookup"><span data-stu-id="4c07b-139">Example using mixed Windows and WSL commands:</span></span>

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

<span data-ttu-id="4c07b-140">Los archivos binarios de Windows deben incluir la extensión de archivo, coincidir con el caso del archivo y ser ejecutable.</span><span class="sxs-lookup"><span data-stu-id="4c07b-140">Windows binaries must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="4c07b-141">No ejecutables, incluidos scripts por lotes.</span><span class="sxs-lookup"><span data-stu-id="4c07b-141">Non-executables including batch scripts.</span></span>  <span data-ttu-id="4c07b-142">Los comandos nativos de `dir` cmd como pueden ejecutarse con `cmd.exe /C` el comando.</span><span class="sxs-lookup"><span data-stu-id="4c07b-142">CMD native commands like `dir` can be run with `cmd.exe /C` command.</span></span>

<span data-ttu-id="4c07b-143">Ejemplos:</span><span class="sxs-lookup"><span data-stu-id="4c07b-143">Examples:</span></span>

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

<span data-ttu-id="4c07b-144">Los parámetros se pasan al binario de Windows sin modificar.</span><span class="sxs-lookup"><span data-stu-id="4c07b-144">Parameters are passed to the Windows binary unmodified.</span></span>

<span data-ttu-id="4c07b-145">Por ejemplo, los siguientes comandos se abrirán `C:\temp\foo.txt` en `notepad.exe`:</span><span class="sxs-lookup"><span data-stu-id="4c07b-145">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="4c07b-146">No se admite la modificación de archivos ubicados en VolFs `/mnt/<x>`(archivos no bajo) con una aplicación de Windows en WSL.</span><span class="sxs-lookup"><span data-stu-id="4c07b-146">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application in WSL is not supported.</span></span>

<span data-ttu-id="4c07b-147">De forma predeterminada, WSL intenta mantener el directorio de trabajo del archivo binario de Windows como el directorio WSL actual, pero revertirá en el directorio de creación de la instancia si el directorio de trabajo se encuentra en VolFs.</span><span class="sxs-lookup"><span data-stu-id="4c07b-147">By default, WSL tries to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="4c07b-148">Por ejemplo: se inicia inicialmente desde `C:\temp` y el directorio WSL actual se cambia a la Página principal del usuario. `wsl.exe`</span><span class="sxs-lookup"><span data-stu-id="4c07b-148">As an example; `wsl.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="4c07b-149">Cuando `notepad.exe` se llama a desde el directorio particular del usuario, WSL se revierte automáticamente `C:\temp` a como el directorio de trabajo del Bloc de notas. exe:</span><span class="sxs-lookup"><span data-stu-id="4c07b-149">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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

## <a name="share-environment-variables-between-windows-and-wsl"></a><span data-ttu-id="4c07b-150">Compartir variables de entorno entre Windows y WSL</span><span class="sxs-lookup"><span data-stu-id="4c07b-150">Share environment variables between Windows and WSL</span></span>

> <span data-ttu-id="4c07b-151">Disponible en las compilaciones de Windows Insider 17063 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4c07b-151">Available in Windows Insider builds 17063 and later.</span></span>

<span data-ttu-id="4c07b-152">Antes de 17063, solo podía tener acceso a la variable de entorno `PATH` de Windows a la que WSL podía tener acceso (por lo que podía iniciar archivos ejecutables de Win32 desde en WSL).</span><span class="sxs-lookup"><span data-stu-id="4c07b-152">Prior to 17063, only Windows environment variable that WSL could access was `PATH` (so you could launch Win32 executables from under WSL).</span></span>

<span data-ttu-id="4c07b-153">A partir de 17063, WSL y Windows `WSLENV`Share, una variable de entorno especial que se crea para el puente entre Windows y Linux distribuciones que se ejecuta en WSL.</span><span class="sxs-lookup"><span data-stu-id="4c07b-153">Starting in 17063, WSL and Windows share `WSLENV`, a special environment variable created to bridge Windows and Linux distros running on WSL.</span></span>

<span data-ttu-id="4c07b-154">Propiedades de `WSLENV`:</span><span class="sxs-lookup"><span data-stu-id="4c07b-154">Properties of `WSLENV`:</span></span>

* <span data-ttu-id="4c07b-155">Está compartida; existe en entornos Windows y WSL.</span><span class="sxs-lookup"><span data-stu-id="4c07b-155">It is shared; it exists in both Windows and WSL environments.</span></span>
* <span data-ttu-id="4c07b-156">Se trata de una lista de variables de entorno que se pueden compartir entre Windows y WSL.</span><span class="sxs-lookup"><span data-stu-id="4c07b-156">It is a list of environment variables to share between Windows and WSL.</span></span>
* <span data-ttu-id="4c07b-157">Puede dar formato a las variables de entorno para que funcionen bien en Windows y WSL.</span><span class="sxs-lookup"><span data-stu-id="4c07b-157">It can format environment variables to work well in Windows and WSL.</span></span>

<span data-ttu-id="4c07b-158">Hay cuatro marcas disponibles en para `WSLENV` influir en la forma en que se traduce esa variable de entorno.</span><span class="sxs-lookup"><span data-stu-id="4c07b-158">There are four flags available in `WSLENV` to influence how that environment variable is translated.</span></span>

<span data-ttu-id="4c07b-159">`WSLENV`marcas</span><span class="sxs-lookup"><span data-stu-id="4c07b-159">`WSLENV` flags:</span></span>

* <span data-ttu-id="4c07b-160">`/p`: traduce la ruta de acceso entre las rutas de acceso de estilo de WSL/Linux y las rutas de acceso de Win32.</span><span class="sxs-lookup"><span data-stu-id="4c07b-160">`/p` - translates the path between WSL/Linux style paths and Win32 paths.</span></span>
* <span data-ttu-id="4c07b-161">`/l`: indica que la variable de entorno es una lista de rutas de acceso.</span><span class="sxs-lookup"><span data-stu-id="4c07b-161">`/l` - indicates the environment variable is a list of paths.</span></span>
* <span data-ttu-id="4c07b-162">`/u`: indica que esta variable de entorno solo debe incluirse al ejecutar WSL desde Win32.</span><span class="sxs-lookup"><span data-stu-id="4c07b-162">`/u` - indicates that this environment variable should only be included when running WSL from Win32.</span></span>
* <span data-ttu-id="4c07b-163">`/w`: indica que esta variable de entorno solo debe incluirse cuando se ejecute Win32 desde WSL.</span><span class="sxs-lookup"><span data-stu-id="4c07b-163">`/w` - indicates that this environment variable should only be included when running Win32 from WSL.</span></span>

<span data-ttu-id="4c07b-164">Las marcas se pueden combinar según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="4c07b-164">Flags can be combined as needed.</span></span>

## <a name="disable-interop"></a><span data-ttu-id="4c07b-165">Deshabilitar interoperabilidad</span><span class="sxs-lookup"><span data-stu-id="4c07b-165">Disable Interop</span></span>

<span data-ttu-id="4c07b-166">Los usuarios pueden deshabilitar la capacidad de ejecutar archivos binarios de Windows para una única sesión de WSL mediante la ejecución del siguiente comando como raíz:</span><span class="sxs-lookup"><span data-stu-id="4c07b-166">Users may disable the ability to run Windows binaries for a single WSL session by running the following command as root:</span></span>

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="4c07b-167">Para volver a habilitar los archivos binarios de Windows, salga de todas las sesiones de WSL y vuelva a ejecutar bash. exe o ejecute el siguiente comando como raíz:</span><span class="sxs-lookup"><span data-stu-id="4c07b-167">To reenable Windows binaries either exit all WSL sessions and re-run bash.exe or run the following command as root:</span></span>

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="4c07b-168">La deshabilitación de la interoperabilidad no se conservará entre sesiones de WSL: la interoperabilidad se habilitará de nuevo cuando se inicie una nueva sesión.</span><span class="sxs-lookup"><span data-stu-id="4c07b-168">Disabling interop will not persist between WSL sessions -- interop will be enabled again when a new session is launched.</span></span>

## <a name="creators-update-and-anniversary-update"></a><span data-ttu-id="4c07b-169">Creators Update y actualización de aniversario</span><span class="sxs-lookup"><span data-stu-id="4c07b-169">Creators Update and Anniversary Update</span></span>

<span data-ttu-id="4c07b-170">Aunque la experiencia de interoperabilidad de los creadores de la actualización es similar a las experiencias de interoperabilidad más recientes, hay algunas diferencias importantes.</span><span class="sxs-lookup"><span data-stu-id="4c07b-170">While the interop experience pre-Fall Creators Update is similar to more recent interop experiences, there are a handful of major differences.</span></span>

<span data-ttu-id="4c07b-171">En Resumen:</span><span class="sxs-lookup"><span data-stu-id="4c07b-171">To summarize:</span></span>

* <span data-ttu-id="4c07b-172">`bash.exe`ha quedado en desuso y se ha `wsl.exe`reemplazado por.</span><span class="sxs-lookup"><span data-stu-id="4c07b-172">`bash.exe` has been deprecated and replaced with `wsl.exe`.</span></span>
* <span data-ttu-id="4c07b-173">`-c`la opción para ejecutar un único comando no es `wsl.exe`necesaria con.</span><span class="sxs-lookup"><span data-stu-id="4c07b-173">`-c` option for running a single command isn't needed with `wsl.exe`.</span></span>
* <span data-ttu-id="4c07b-174">La ruta de acceso de Windows se incluye en WSL`$PATH`</span><span class="sxs-lookup"><span data-stu-id="4c07b-174">Windows path is included in the WSL `$PATH`</span></span>

<span data-ttu-id="4c07b-175">El proceso para deshabilitar la interoperabilidad no ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="4c07b-175">The process for disabling interop is unchanged.</span></span>

### <a name="invoking-wsl-from-the-windows-command-line"></a><span data-ttu-id="4c07b-176">Invocar WSL desde la línea de comandos de Windows</span><span class="sxs-lookup"><span data-stu-id="4c07b-176">Invoking WSL from the Windows Command Line</span></span>

<span data-ttu-id="4c07b-177">Los archivos binarios de Linux se pueden invocar desde el símbolo del sistema de Windows o desde PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4c07b-177">Linux binaries can be invoked from the Windows Command Prompt or from PowerShell.</span></span>  <span data-ttu-id="4c07b-178">Los archivos binarios que se invocan de esta manera tienen las propiedades siguientes:</span><span class="sxs-lookup"><span data-stu-id="4c07b-178">Binaries invoked in this way have the following properties:</span></span>

1. <span data-ttu-id="4c07b-179">Use el mismo directorio de trabajo que el símbolo del sistema de CMD o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4c07b-179">Use the same working directory as the CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="4c07b-180">Ejecute como el usuario predeterminado WSL.</span><span class="sxs-lookup"><span data-stu-id="4c07b-180">Run as the WSL default user.</span></span>
1. <span data-ttu-id="4c07b-181">Tener los mismos derechos administrativos de Windows que el proceso de llamada y el terminal.</span><span class="sxs-lookup"><span data-stu-id="4c07b-181">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="4c07b-182">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="4c07b-182">Example:</span></span>

```console
C:\temp> bash -c "ls -la"
```

<span data-ttu-id="4c07b-183">Los comandos de Linux a los que se llama de esta manera se administran como cualquier otra aplicación de Windows.</span><span class="sxs-lookup"><span data-stu-id="4c07b-183">Linux commands called in this way are handled like any other Windows application.</span></span>  <span data-ttu-id="4c07b-184">Cosas como la entrada, la canalización y el redireccionamiento de archivos funcionan según lo previsto.</span><span class="sxs-lookup"><span data-stu-id="4c07b-184">Things such as input, piping, and file redirection work as expected.</span></span>

<span data-ttu-id="4c07b-185">Ejemplos:</span><span class="sxs-lookup"><span data-stu-id="4c07b-185">Examples:</span></span>

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

<span data-ttu-id="4c07b-186">Los comandos de WSL que `bash -c` se pasan a se reenvían al proceso WSL sin modificarlos.</span><span class="sxs-lookup"><span data-stu-id="4c07b-186">The WSL commands passed into `bash -c` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="4c07b-187">Las rutas de acceso de archivo deben especificarse en el formato WSL y se debe tener cuidado para escapar caracteres relevantes.</span><span class="sxs-lookup"><span data-stu-id="4c07b-187">File paths must be specified in the WSL format and care must be taken to escape relevant characters.</span></span> <span data-ttu-id="4c07b-188">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="4c07b-188">Example:</span></span>

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a><span data-ttu-id="4c07b-189">Invocar archivos binarios de Windows desde WSL</span><span class="sxs-lookup"><span data-stu-id="4c07b-189">Invoking Windows binaries from WSL</span></span>

<span data-ttu-id="4c07b-190">El subsistema de Windows para Linux puede invocar archivos binarios de Windows directamente desde la línea de comandos de WSL.</span><span class="sxs-lookup"><span data-stu-id="4c07b-190">The Windows Subsystem for Linux can invoke Windows binaries directly from the WSL command line.</span></span>  <span data-ttu-id="4c07b-191">Las aplicaciones que se ejecutan de esta manera tienen las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="4c07b-191">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="4c07b-192">Conserve el directorio de trabajo como el símbolo del sistema de WSL, excepto en el escenario que se explica a continuación.</span><span class="sxs-lookup"><span data-stu-id="4c07b-192">Retain the working directory as the WSL command prompt except in the scenario explained below.</span></span>
1. <span data-ttu-id="4c07b-193">Tener los mismos derechos de permiso que `bash.exe` el proceso.</span><span class="sxs-lookup"><span data-stu-id="4c07b-193">Have the same permission rights as the `bash.exe` process.</span></span> 
1. <span data-ttu-id="4c07b-194">Ejecute como el usuario activo de Windows.</span><span class="sxs-lookup"><span data-stu-id="4c07b-194">Run as the active Windows user.</span></span>
1. <span data-ttu-id="4c07b-195">Aparecen en el administrador de tareas de Windows como si se ejecutaran directamente desde el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="4c07b-195">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="4c07b-196">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="4c07b-196">Example:</span></span>

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

<span data-ttu-id="4c07b-197">En WSL, estos ejecutables se tratan de forma similar a los ejecutables nativos de Linux.</span><span class="sxs-lookup"><span data-stu-id="4c07b-197">In WSL, these executables are handled similar to native Linux executables.</span></span>  <span data-ttu-id="4c07b-198">Esto significa que la adición de directorios a la ruta de acceso de Linux y la canalización entre comandos funciona según lo previsto.</span><span class="sxs-lookup"><span data-stu-id="4c07b-198">This means adding directories to the Linux path and piping between commands works as expected.</span></span>  <span data-ttu-id="4c07b-199">Ejemplos:</span><span class="sxs-lookup"><span data-stu-id="4c07b-199">Examples:</span></span>

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

<span data-ttu-id="4c07b-200">El binario de Windows debe incluir la extensión de archivo, coincidir con el caso del archivo y ser ejecutable.</span><span class="sxs-lookup"><span data-stu-id="4c07b-200">The Windows binary must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="4c07b-201">Los no ejecutables, incluidos los scripts `dir` por lotes y el `/mnt/c/Windows/System32/cmd.exe /C` comando like, se pueden ejecutar con el comando.</span><span class="sxs-lookup"><span data-stu-id="4c07b-201">Non-executables including batch scripts and command like `dir` can be run with `/mnt/c/Windows/System32/cmd.exe /C` command.</span></span>

<span data-ttu-id="4c07b-202">Ejemplos:</span><span class="sxs-lookup"><span data-stu-id="4c07b-202">Examples:</span></span>

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

<span data-ttu-id="4c07b-203">Los parámetros se pasan al binario de Windows sin modificar.</span><span class="sxs-lookup"><span data-stu-id="4c07b-203">Parameters are passed to the Windows binary unmodified.</span></span>  

<span data-ttu-id="4c07b-204">Por ejemplo, los siguientes comandos se abrirán `C:\temp\foo.txt` en `notepad.exe`:</span><span class="sxs-lookup"><span data-stu-id="4c07b-204">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="4c07b-205">No se admite la modificación de archivos ubicados en VolFs `/mnt/<x>`(archivos no bajo) con una aplicación de Windows.</span><span class="sxs-lookup"><span data-stu-id="4c07b-205">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application is not supported.</span></span>  <span data-ttu-id="4c07b-206">De forma predeterminada, WSL intenta mantener el directorio de trabajo del archivo binario de Windows como el directorio WSL actual, pero revertirá en el directorio de creación de la instancia si el directorio de trabajo se encuentra en VolFs.</span><span class="sxs-lookup"><span data-stu-id="4c07b-206">By default, WSL attempts to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="4c07b-207">Por ejemplo: se inicia inicialmente desde `C:\temp` y el directorio WSL actual se cambia a la Página principal del usuario. `bash.exe`</span><span class="sxs-lookup"><span data-stu-id="4c07b-207">As an example; `bash.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="4c07b-208">Cuando `notepad.exe` se llama a desde el directorio particular del usuario, WSL se revierte automáticamente `C:\temp` a como el directorio de trabajo del Bloc de notas. exe:</span><span class="sxs-lookup"><span data-stu-id="4c07b-208">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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
