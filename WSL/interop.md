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
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063253"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a><span data-ttu-id="e0147-103">Subsistema de Windows para la interoperabilidad de Linux con Windows</span><span class="sxs-lookup"><span data-stu-id="e0147-103">Windows Subsystem for Linux interoperability with Windows</span></span>

> **<span data-ttu-id="e0147-104">Actualizado para Fall Creators Update.</span><span class="sxs-lookup"><span data-stu-id="e0147-104">Updated for Fall Creators Update.</span></span>**  
<span data-ttu-id="e0147-105">Si ejecuta Creators Update o actualización de aniversario, vaya a la [la sección actualización de aniversario decreadores/](interop.md#creators-update-and-anniversary-update).</span><span class="sxs-lookup"><span data-stu-id="e0147-105">If you're running Creators Update or Anniversary Update, jump to the [Creators/Anniversary Update section](interop.md#creators-update-and-anniversary-update).</span></span>

<span data-ttu-id="e0147-106">El subsistema de Windows para Linux (WSL) mejora continuamente la integración entre Windows y Linux.</span><span class="sxs-lookup"><span data-stu-id="e0147-106">The Windows Subsystem for Linux (WSL) is continuously improving integration between Windows and Linux.</span></span>  <span data-ttu-id="e0147-107">Se puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e0147-107">You can:</span></span>

1. <span data-ttu-id="e0147-108">Invocación de los archivos binarios de Windows desde la consola de Linux.</span><span class="sxs-lookup"><span data-stu-id="e0147-108">Invoke Windows binaries from the Linux console.</span></span>
1. <span data-ttu-id="e0147-109">Invocación de los archivos binarios de Linux desde una consola de Windows.</span><span class="sxs-lookup"><span data-stu-id="e0147-109">Invoke Linux binaries from a Windows console.</span></span>
1. <span data-ttu-id="e0147-110">**Las compilaciones de Windows Insiders 17063 +** comparten las mismas variables de entorno entre Windows y Linux.</span><span class="sxs-lookup"><span data-stu-id="e0147-110">**Windows Insiders Builds 17063+** Share environment variables between Linux and Windows.</span></span>

<span data-ttu-id="e0147-111">Esto ofrece una experiencia sin problemas entre Windows y WSL.</span><span class="sxs-lookup"><span data-stu-id="e0147-111">This delivers a seamless experience between Windows and WSL.</span></span>  <span data-ttu-id="e0147-112">Los detalles técnicos están en el [WSL blog](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span><span class="sxs-lookup"><span data-stu-id="e0147-112">Technical details are on the [WSL blog](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span></span>

## <a name="run-linux-tools-from-a-windows-command-line"></a><span data-ttu-id="e0147-113">Ejecutar herramientas de Linux desde una línea de comandos de Windows</span><span class="sxs-lookup"><span data-stu-id="e0147-113">Run Linux tools from a Windows command line</span></span>

<span data-ttu-id="e0147-114">Ejecutar archivos binarios de Linux desde la línea de comandos de Windows (CMD o PowerShell) mediante `wsl.exe <command>`.</span><span class="sxs-lookup"><span data-stu-id="e0147-114">Run Linux binaries from the Windows Command Prompt (CMD or PowerShell) using `wsl.exe <command>`.</span></span>

<span data-ttu-id="e0147-115">Archivos binarios que se invoca de esta manera:</span><span class="sxs-lookup"><span data-stu-id="e0147-115">Binaries invoked in this way:</span></span>

1. <span data-ttu-id="e0147-116">Use el mismo directorio de trabajo como el actual mensaje CMD o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e0147-116">Use the same working directory as the current CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="e0147-117">Ejecutar como usuario WSL predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e0147-117">Run as the WSL default user.</span></span>
1. <span data-ttu-id="e0147-118">Tener los mismos derechos administrativos de Windows como el proceso de llamada y el terminal.</span><span class="sxs-lookup"><span data-stu-id="e0147-118">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="e0147-119">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="e0147-119">For example:</span></span>

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

<span data-ttu-id="e0147-120">El siguiente comando de Linux `wsl.exe` se administra como cualquier comando que se ejecute en WSL.</span><span class="sxs-lookup"><span data-stu-id="e0147-120">The Linux command following `wsl.exe` is handled like any command run in WSL.</span></span>  <span data-ttu-id="e0147-121">Funcionará como sudo, la canalización y redirección de archivos.</span><span class="sxs-lookup"><span data-stu-id="e0147-121">Things such as sudo, piping, and file redirection work.</span></span>

<span data-ttu-id="e0147-122">Ejemplo de uso de sudo:</span><span class="sxs-lookup"><span data-stu-id="e0147-122">Example using sudo:</span></span>

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

<span data-ttu-id="e0147-123">Ejemplos de combinación de comandos WSL y Windows:</span><span class="sxs-lookup"><span data-stu-id="e0147-123">Examples mixing WSL and Windows commands:</span></span>

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

<span data-ttu-id="e0147-124">Los comandos que se pasan a `wsl.exe` se reenvían al proceso WSL sin ninguna modificación.</span><span class="sxs-lookup"><span data-stu-id="e0147-124">The commands passed into `wsl.exe` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="e0147-125">Las rutas de acceso de archivo deben especificarse en el formato WSL.</span><span class="sxs-lookup"><span data-stu-id="e0147-125">File paths must be specified in the WSL format.</span></span>

<span data-ttu-id="e0147-126">Ejemplo con las rutas de acceso:</span><span class="sxs-lookup"><span data-stu-id="e0147-126">Example with paths:</span></span>

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a><span data-ttu-id="e0147-127">Ejecutar herramientas de Windows desde WSL</span><span class="sxs-lookup"><span data-stu-id="e0147-127">Run Windows tools from WSL</span></span>

<span data-ttu-id="e0147-128">WSL puede invocar los archivos binarios de Windows directamente desde la línea de comandos WSL mediante `[binary name].exe`.</span><span class="sxs-lookup"><span data-stu-id="e0147-128">WSL can invoke Windows binaries directly from the WSL command line using `[binary name].exe`.</span></span>  <span data-ttu-id="e0147-129">Por ejemplo: `notepad.exe`.</span><span class="sxs-lookup"><span data-stu-id="e0147-129">For example, `notepad.exe`.</span></span>  <span data-ttu-id="e0147-130">Para facilitar la ejecución de los archivos ejecutables de Windows, la ruta de acceso de Windows se incluye en el sistema operativo Linux `$PATH` en Fall Creators Update.</span><span class="sxs-lookup"><span data-stu-id="e0147-130">To make Windows executables easier to run, Windows path is included in the Linux `$PATH` in Fall Creators Update.</span></span>

<span data-ttu-id="e0147-131">Las aplicaciones se ejecutan de esta forma tienen las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="e0147-131">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="e0147-132">Conservar el directorio de trabajo como el símbolo del sistema de WSL (la mayor parte, las excepciones se explican a continuación).</span><span class="sxs-lookup"><span data-stu-id="e0147-132">Retain the working directory as the WSL command prompt (for the most part -- exceptions are explained below).</span></span>
1. <span data-ttu-id="e0147-133">Tener los mismos derechos de permiso que el proceso WSL.</span><span class="sxs-lookup"><span data-stu-id="e0147-133">Have the same permission rights as the WSL process.</span></span>
1. <span data-ttu-id="e0147-134">Ejecutar como el usuario de Windows activo.</span><span class="sxs-lookup"><span data-stu-id="e0147-134">Run as the active Windows user.</span></span>
1. <span data-ttu-id="e0147-135">Aparecen en el Administrador de tareas de Windows como si se ejecuta directamente desde el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="e0147-135">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="e0147-136">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="e0147-136">Example:</span></span>

``` BASH
$ notepad.exe
```

<span data-ttu-id="e0147-137">Archivos ejecutables de Windows para ejecutar en WSL se administran de forma similar ejecutables nativos de Linux--tuberías redirecciones e incluso procesamiento en segundo plano trabajo según lo previsto.</span><span class="sxs-lookup"><span data-stu-id="e0147-137">Windows executables run in WSL are handled similarly to native Linux executables -- piping, redirects, and even backgrounding work as expected.</span></span>

<span data-ttu-id="e0147-138">Ejemplos de uso de canalizaciones:</span><span class="sxs-lookup"><span data-stu-id="e0147-138">Examples using pipes:</span></span>

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

<span data-ttu-id="e0147-139">Ejemplo de uso de comandos de Windows y WSL mixtos:</span><span class="sxs-lookup"><span data-stu-id="e0147-139">Example using mixed Windows and WSL commands:</span></span>

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

<span data-ttu-id="e0147-140">Archivos binarios de Windows deben incluir la extensión de archivo, coincidir con el caso de archivo y se pueda ejecutar.</span><span class="sxs-lookup"><span data-stu-id="e0147-140">Windows binaries must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="e0147-141">Incluidos los ejecutables no procesar por lotes las secuencias de comandos.</span><span class="sxs-lookup"><span data-stu-id="e0147-141">Non-executables including batch scripts.</span></span>  <span data-ttu-id="e0147-142">Al igual que los comandos nativos de CMD `dir` se pueden ejecutar con `cmd.exe /C` comando.</span><span class="sxs-lookup"><span data-stu-id="e0147-142">CMD native commands like `dir` can be run with `cmd.exe /C` command.</span></span>

<span data-ttu-id="e0147-143">Ejemplos:</span><span class="sxs-lookup"><span data-stu-id="e0147-143">Examples:</span></span>

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

<span data-ttu-id="e0147-144">Los parámetros se pasan a los binarios de Windows sin modificar.</span><span class="sxs-lookup"><span data-stu-id="e0147-144">Parameters are passed to the Windows binary unmodified.</span></span>

<span data-ttu-id="e0147-145">Por ejemplo, se abren los siguientes comandos `C:\temp\foo.txt` en `notepad.exe`:</span><span class="sxs-lookup"><span data-stu-id="e0147-145">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="e0147-146">Modificación de archivos ubicados en VolFs (no en archivos `/mnt/<x>`) con un Windows no se admite la aplicación en WSL.</span><span class="sxs-lookup"><span data-stu-id="e0147-146">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application in WSL is not supported.</span></span>

<span data-ttu-id="e0147-147">De forma predeterminada, WSL intenta mantener el directorio de trabajo de la Windows binario como el directorio actual de WSL, pero se revertirá en el directorio de la creación de instancia si el directorio de trabajo se encuentra en VolFs.</span><span class="sxs-lookup"><span data-stu-id="e0147-147">By default, WSL tries to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="e0147-148">Como ejemplo; `wsl.exe` inicialmente se inicia desde `C:\temp` y se cambia el directorio WSL actual a la página principal del usuario.</span><span class="sxs-lookup"><span data-stu-id="e0147-148">As an example; `wsl.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="e0147-149">Cuando `notepad.exe` se llama desde el directorio del usuario principal, WSL se revierte automáticamente a `C:\temp` como el directorio de trabajo notepad.exe:</span><span class="sxs-lookup"><span data-stu-id="e0147-149">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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

## <a name="share-environment-variables-between-windows-and-wsl"></a><span data-ttu-id="e0147-150">Variables de entorno del recurso compartido entre Windows y WSL</span><span class="sxs-lookup"><span data-stu-id="e0147-150">Share environment variables between Windows and WSL</span></span>

> <span data-ttu-id="e0147-151">Está disponible en las compilaciones de Windows Insider 17063 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="e0147-151">Available in Windows Insider builds 17063 and later.</span></span>

<span data-ttu-id="e0147-152">Antes de 17063, fue sólo variable de entorno de Windows que puede tener acceso WSL `PATH` (por lo que también puede iniciar archivos ejecutables de Win32 en WSL).</span><span class="sxs-lookup"><span data-stu-id="e0147-152">Prior to 17063, only Windows environment variable that WSL could access was `PATH` (so you could launch Win32 executables from under WSL).</span></span>

<span data-ttu-id="e0147-153">A partir de 17063, WSL y Windows comparten `WSLENV`, una variable de entorno especiales creada para superar las distribuciones de Windows y Linux que se ejecutan en WSL.</span><span class="sxs-lookup"><span data-stu-id="e0147-153">Starting in 17063, WSL and Windows share `WSLENV`, a special environment variable created to bridge Windows and Linux distros running on WSL.</span></span>

<span data-ttu-id="e0147-154">Propiedades de `WSLENV`:</span><span class="sxs-lookup"><span data-stu-id="e0147-154">Properties of `WSLENV`:</span></span>

* <span data-ttu-id="e0147-155">Que es compartido; existe en entornos tanto Windows como WSL.</span><span class="sxs-lookup"><span data-stu-id="e0147-155">It is shared; it exists in both Windows and WSL environments.</span></span>
* <span data-ttu-id="e0147-156">Es una lista de variables de entorno para compartir entre Windows y WSL.</span><span class="sxs-lookup"><span data-stu-id="e0147-156">It is a list of environment variables to share between Windows and WSL.</span></span>
* <span data-ttu-id="e0147-157">Pueden dar formato a las variables de entorno para que funcione bien en Windows y WSL.</span><span class="sxs-lookup"><span data-stu-id="e0147-157">It can format environment variables to work well in Windows and WSL.</span></span>

<span data-ttu-id="e0147-158">Hay cuatro indicadores en `WSLENV` para influir en cómo se traduce esa variable de entorno.</span><span class="sxs-lookup"><span data-stu-id="e0147-158">There are four flags available in `WSLENV` to influence how that environment variable is translated.</span></span>

`WSLENV` <span data-ttu-id="e0147-159">indicadores:</span><span class="sxs-lookup"><span data-stu-id="e0147-159">flags:</span></span>

* `/p` <span data-ttu-id="e0147-160">: convierte la ruta de acceso entre las rutas de acceso de estilo WSL/Linux y las rutas de acceso de Win32.</span><span class="sxs-lookup"><span data-stu-id="e0147-160">- translates the path between WSL/Linux style paths and Win32 paths.</span></span>
* `/l` <span data-ttu-id="e0147-161">-indica que la variable de entorno es una lista de rutas de acceso.</span><span class="sxs-lookup"><span data-stu-id="e0147-161">- indicates the environment variable is a list of paths.</span></span>
* `/u` <span data-ttu-id="e0147-162">-indica que esta variable de entorno solo se debe incluir cuando se ejecuta WSL desde Win32.</span><span class="sxs-lookup"><span data-stu-id="e0147-162">- indicates that this environment variable should only be included when running WSL from Win32.</span></span>
* `/w` <span data-ttu-id="e0147-163">-indica que esta variable de entorno solo se debe incluir cuando se ejecuta Win32 desde WSL.</span><span class="sxs-lookup"><span data-stu-id="e0147-163">- indicates that this environment variable should only be included when running Win32 from WSL.</span></span>

<span data-ttu-id="e0147-164">Las marcas se pueden combinar según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="e0147-164">Flags can be combined as needed.</span></span>

## <a name="disable-interop"></a><span data-ttu-id="e0147-165">Deshabilitar la interoperabilidad</span><span class="sxs-lookup"><span data-stu-id="e0147-165">Disable Interop</span></span>

<span data-ttu-id="e0147-166">Los usuarios pueden deshabilitar la capacidad de ejecutar los archivos binarios de Windows en una sola sesión WSL ejecutando el siguiente comando como raíz:</span><span class="sxs-lookup"><span data-stu-id="e0147-166">Users may disable the ability to run Windows binaries for a single WSL session by running the following command as root:</span></span>

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="e0147-167">Para volver a habilitar Windows archivos binarios de salir de todas las sesiones WSL y vuelva a ejecutan bash.exe o lo ejecutan el siguiente comando como raíz:</span><span class="sxs-lookup"><span data-stu-id="e0147-167">To reenable Windows binaries either exit all WSL sessions and re-run bash.exe or run the following command as root:</span></span>

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="e0147-168">Deshabilitación de interoperabilidad no se conservará entre sesiones WSL: interoperabilidad volverá a activarse cuando se inicia una nueva sesión.</span><span class="sxs-lookup"><span data-stu-id="e0147-168">Disabling interop will not persist between WSL sessions -- interop will be enabled again when a new session is launched.</span></span>

## <a name="creators-update-and-anniversary-update"></a><span data-ttu-id="e0147-169">Creators Update y actualización de aniversario</span><span class="sxs-lookup"><span data-stu-id="e0147-169">Creators Update and Anniversary Update</span></span>

<span data-ttu-id="e0147-170">Aunque el otoño interoperabilidad experiencia previa Creators Update es similar a las experiencias más recientes de interoperabilidad, hay un handfull de las principales diferencias.</span><span class="sxs-lookup"><span data-stu-id="e0147-170">While the interop experience pre-Fall Creators Update is similar to more recent interop experiences, there are a handfull of major differences.</span></span>

<span data-ttu-id="e0147-171">Para resumir:</span><span class="sxs-lookup"><span data-stu-id="e0147-171">To summarize:</span></span>

* `bash.exe` <span data-ttu-id="e0147-172">se ha desusado y se reemplazan con `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="e0147-172">has been deprecated and replaced with `wsl.exe`.</span></span>
* `-c` <span data-ttu-id="e0147-173">opción para ejecutar un comando único no es necesario con `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="e0147-173">option for running a single command isn't needed with `wsl.exe`.</span></span>
* <span data-ttu-id="e0147-174">Ruta de acceso de Windows se incluye en el WSL</span><span class="sxs-lookup"><span data-stu-id="e0147-174">Windows path is included in the WSL</span></span> `$PATH`

<span data-ttu-id="e0147-175">Se ha modificado el proceso de deshabilitar la interoperabilidad.</span><span class="sxs-lookup"><span data-stu-id="e0147-175">The process for disabling interop is unchanged.</span></span>

### <a name="invoking-wsl-from-the-windows-command-line"></a><span data-ttu-id="e0147-176">Invocar WSL desde la línea de comandos de Windows</span><span class="sxs-lookup"><span data-stu-id="e0147-176">Invoking WSL from the Windows Command Line</span></span>

<span data-ttu-id="e0147-177">Los archivos binarios de Linux se pueden invocar desde el símbolo del sistema de Windows o desde PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e0147-177">Linux binaries can be invoked from the Windows Command Prompt or from PowerShell.</span></span>  <span data-ttu-id="e0147-178">Los archivos binarios que se invoca de esta manera tienen las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="e0147-178">Binaries invoked in this way have the following properties:</span></span>

1. <span data-ttu-id="e0147-179">Use el mismo directorio de trabajo como el símbolo del sistema CMD o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e0147-179">Use the same working directory as the CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="e0147-180">Ejecutar como usuario WSL predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e0147-180">Run as the WSL default user.</span></span>
1. <span data-ttu-id="e0147-181">Tener los mismos derechos administrativos de Windows como el proceso de llamada y el terminal.</span><span class="sxs-lookup"><span data-stu-id="e0147-181">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="e0147-182">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="e0147-182">Example:</span></span>

```console
C:\temp> bash -c "ls -la"
```

<span data-ttu-id="e0147-183">Comandos de Linux denominados de esta manera se administran como cualquier otra aplicación de Windows.</span><span class="sxs-lookup"><span data-stu-id="e0147-183">Linux commands called in this way are handled like any other Windows application.</span></span>  <span data-ttu-id="e0147-184">Cosas como entrada, la canalización y redirección de archivos funcionan según lo previsto.</span><span class="sxs-lookup"><span data-stu-id="e0147-184">Things such as input, piping, and file redirection work as expected.</span></span>

<span data-ttu-id="e0147-185">Ejemplos:</span><span class="sxs-lookup"><span data-stu-id="e0147-185">Examples:</span></span>

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

<span data-ttu-id="e0147-186">Los comandos WSL pasan `bash -c` se reenvían al proceso WSL sin ninguna modificación.</span><span class="sxs-lookup"><span data-stu-id="e0147-186">The WSL commands passed into `bash -c` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="e0147-187">Las rutas de acceso de archivo deben especificarse en el formato WSL y debe tener cuidado para escapar caracteres pertinentes.</span><span class="sxs-lookup"><span data-stu-id="e0147-187">File paths must be specified in the WSL format and care must be taken to escape relevant characters.</span></span> <span data-ttu-id="e0147-188">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="e0147-188">Example:</span></span>

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a><span data-ttu-id="e0147-189">Invocación de los archivos binarios de Windows de WSL</span><span class="sxs-lookup"><span data-stu-id="e0147-189">Invoking Windows binaries from WSL</span></span>

<span data-ttu-id="e0147-190">El subsistema de Windows para Linux puede invocar directamente desde la línea de comandos WSL archivos binarios de Windows.</span><span class="sxs-lookup"><span data-stu-id="e0147-190">The Windows Subsystem for Linux can invoke Windows binaries directly from the WSL command line.</span></span>  <span data-ttu-id="e0147-191">Las aplicaciones se ejecutan de esta forma tienen las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="e0147-191">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="e0147-192">Conservar el directorio de trabajo como el símbolo WSL, excepto en el escenario que se explica más adelante.</span><span class="sxs-lookup"><span data-stu-id="e0147-192">Retain the working directory as the WSL command prompt except in the scenario explained below.</span></span>
1. <span data-ttu-id="e0147-193">Tiene los mismos derechos de permiso que el `bash.exe` proceso.</span><span class="sxs-lookup"><span data-stu-id="e0147-193">Have the same permission rights as the `bash.exe` process.</span></span> 
1. <span data-ttu-id="e0147-194">Ejecutar como el usuario de Windows activo.</span><span class="sxs-lookup"><span data-stu-id="e0147-194">Run as the active Windows user.</span></span>
1. <span data-ttu-id="e0147-195">Aparecen en el Administrador de tareas de Windows como si se ejecuta directamente desde el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="e0147-195">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="e0147-196">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="e0147-196">Example:</span></span>

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

<span data-ttu-id="e0147-197">En WSL, estos ejecutables se tratan como ejecutables nativos de Linux.</span><span class="sxs-lookup"><span data-stu-id="e0147-197">In WSL, these executables are handled similar to native Linux executables.</span></span>  <span data-ttu-id="e0147-198">Esto significa agregar directorios a la ruta de acceso de Linux y se canaliza entre works comandos según lo previsto.</span><span class="sxs-lookup"><span data-stu-id="e0147-198">This means adding directories to the Linux path and piping between commands works as expected.</span></span>  <span data-ttu-id="e0147-199">Ejemplos:</span><span class="sxs-lookup"><span data-stu-id="e0147-199">Examples:</span></span>

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

<span data-ttu-id="e0147-200">El archivo binario de Windows debe incluir la extensión de archivo, coincide con el caso de archivo y se pueda ejecutar.</span><span class="sxs-lookup"><span data-stu-id="e0147-200">The Windows binary must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="e0147-201">Archivos ejecutables no incluidos por lotes de scripts y comandos como `dir` se pueden ejecutar con `/mnt/c/Windows/System32/cmd.exe /C` comando.</span><span class="sxs-lookup"><span data-stu-id="e0147-201">Non-executables including batch scripts and command like `dir` can be run with `/mnt/c/Windows/System32/cmd.exe /C` command.</span></span>

<span data-ttu-id="e0147-202">Ejemplos:</span><span class="sxs-lookup"><span data-stu-id="e0147-202">Examples:</span></span>

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

<span data-ttu-id="e0147-203">Los parámetros se pasan a los binarios de Windows sin modificar.</span><span class="sxs-lookup"><span data-stu-id="e0147-203">Parameters are passed to the Windows binary unmodified.</span></span>  

<span data-ttu-id="e0147-204">Por ejemplo, se abren los siguientes comandos `C:\temp\foo.txt` en `notepad.exe`:</span><span class="sxs-lookup"><span data-stu-id="e0147-204">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="e0147-205">Modificación de archivos ubicados en VolFs (no en archivos `/mnt/<x>`) con un Windows no se admite la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e0147-205">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application is not supported.</span></span>  <span data-ttu-id="e0147-206">De forma predeterminada, WSL intenta mantener el directorio de trabajo de la Windows binario como el directorio actual de WSL, pero se revertirá en el directorio de la creación de instancia si el directorio de trabajo se encuentra en VolFs.</span><span class="sxs-lookup"><span data-stu-id="e0147-206">By default, WSL attempts to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="e0147-207">Como ejemplo; `bash.exe` inicialmente se inicia desde `C:\temp` y se cambia el directorio WSL actual a la página principal del usuario.</span><span class="sxs-lookup"><span data-stu-id="e0147-207">As an example; `bash.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="e0147-208">Cuando `notepad.exe` se llama desde el directorio del usuario principal, WSL se revierte automáticamente a `C:\temp` como el directorio de trabajo notepad.exe:</span><span class="sxs-lookup"><span data-stu-id="e0147-208">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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
