---
title: Interoperabilidad de Windows con Linux
description: Describe la interoperabilidad de Windows con distribuciones de Linux que se ejecutan en el subsistema de Windows para Linux.
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: f8b0150c044f5011b84e80cac4befd752c4dc552
ms.sourcegitcommit: 39d3a2f0f4184eaec8d8fec740aff800e8ea9ac7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/24/2020
ms.locfileid: "71269805"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a><span data-ttu-id="9f8a3-103">Interoperabilidad del subsistema de Windows para Linux con Windows</span><span class="sxs-lookup"><span data-stu-id="9f8a3-103">Windows Subsystem for Linux interoperability with Windows</span></span>

> <span data-ttu-id="9f8a3-104">**Actualización de Fall Creators Update**.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-104">**Updated for Fall Creators Update.**</span></span>  
<span data-ttu-id="9f8a3-105">Si estás ejecutando Creators Update o la Actualización de aniversario, ve a la [sección Creators Update/Actualización de aniversario](interop.md#creators-update-and-anniversary-update).</span><span class="sxs-lookup"><span data-stu-id="9f8a3-105">If you're running Creators Update or Anniversary Update, jump to the [Creators/Anniversary Update section](interop.md#creators-update-and-anniversary-update).</span></span>

<span data-ttu-id="9f8a3-106">El subsistema de Windows para Linux (WSL) está mejorando continuamente la integración entre Windows y Linux.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-106">The Windows Subsystem for Linux (WSL) is continuously improving integration between Windows and Linux.</span></span>  <span data-ttu-id="9f8a3-107">Se puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9f8a3-107">You can:</span></span>

1. <span data-ttu-id="9f8a3-108">Invocar archivos binarios de Windows desde la consola de Linux.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-108">Invoke Windows binaries from the Linux console.</span></span>
1. <span data-ttu-id="9f8a3-109">Invocar archivos binarios de Linux desde la consola de Windows.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-109">Invoke Linux binaries from a Windows console.</span></span>
1. <span data-ttu-id="9f8a3-110">**Compilaciones 17063 y posteriores de Windows Insider**: compartir variables de entorno entre Linux y Windows.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-110">**Windows Insiders Builds 17063+** Share environment variables between Linux and Windows.</span></span>

<span data-ttu-id="9f8a3-111">Esto ofrece una experiencia perfecta entre Windows y WSL.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-111">This delivers a seamless experience between Windows and WSL.</span></span>  <span data-ttu-id="9f8a3-112">Los detalles técnicos se encuentran en el [blog de WSL](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span><span class="sxs-lookup"><span data-stu-id="9f8a3-112">Technical details are on the [WSL blog](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span></span>

## <a name="run-linux-tools-from-a-windows-command-line"></a><span data-ttu-id="9f8a3-113">Ejecución de herramientas de Linux desde una línea de comandos de Windows</span><span class="sxs-lookup"><span data-stu-id="9f8a3-113">Run Linux tools from a Windows command line</span></span>

<span data-ttu-id="9f8a3-114">Ejecuta los archivos binarios de Linux desde el símbolo del sistema de Windows (CMD o PowerShell) mediante `wsl.exe <command>`.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-114">Run Linux binaries from the Windows Command Prompt (CMD or PowerShell) using `wsl.exe <command>`.</span></span>

<span data-ttu-id="9f8a3-115">Los archivos binarios se invocan de esta manera:</span><span class="sxs-lookup"><span data-stu-id="9f8a3-115">Binaries invoked in this way:</span></span>

1. <span data-ttu-id="9f8a3-116">Usan el mismo directorio de trabajo que el símbolo del sistema actual de CMD o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-116">Use the same working directory as the current CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="9f8a3-117">Se ejecutan como usuario predeterminado de WSL.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-117">Run as the WSL default user.</span></span>
1. <span data-ttu-id="9f8a3-118">Tienen los mismos derechos administrativos de Windows que el terminal y el proceso de llamada.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-118">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="9f8a3-119">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="9f8a3-119">For example:</span></span>

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

<span data-ttu-id="9f8a3-120">El comando de Linux `wsl.exe` siguiente se controla como cualquier comando que se ejecute en WSL.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-120">The Linux command following `wsl.exe` is handled like any command run in WSL.</span></span>  <span data-ttu-id="9f8a3-121">Funcionan cosas como sudo, canalizaciones y redireccionamientos de archivos.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-121">Things such as sudo, piping, and file redirection work.</span></span>

<span data-ttu-id="9f8a3-122">Ejemplo con sudo:</span><span class="sxs-lookup"><span data-stu-id="9f8a3-122">Example using sudo:</span></span>

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

<span data-ttu-id="9f8a3-123">Ejemplos de combinación de comandos de Windows y WSL:</span><span class="sxs-lookup"><span data-stu-id="9f8a3-123">Examples mixing WSL and Windows commands:</span></span>

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

<span data-ttu-id="9f8a3-124">Los comandos pasados a `wsl.exe` se reenvían al proceso de WSL sin modificaciones.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-124">The commands passed into `wsl.exe` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="9f8a3-125">Las rutas de acceso de archivo deben especificarse en el formato de WSL.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-125">File paths must be specified in the WSL format.</span></span>

<span data-ttu-id="9f8a3-126">Ejemplo con rutas de acceso:</span><span class="sxs-lookup"><span data-stu-id="9f8a3-126">Example with paths:</span></span>

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a><span data-ttu-id="9f8a3-127">Ejecución de herramientas de Windows desde WSL</span><span class="sxs-lookup"><span data-stu-id="9f8a3-127">Run Windows tools from WSL</span></span>

<span data-ttu-id="9f8a3-128">WSL puede invocar archivos binarios de Windows directamente desde la línea de comandos de WSL mediante `[binary name].exe`.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-128">WSL can invoke Windows binaries directly from the WSL command line using `[binary name].exe`.</span></span>  <span data-ttu-id="9f8a3-129">Por ejemplo, `notepad.exe`.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-129">For example, `notepad.exe`.</span></span>  <span data-ttu-id="9f8a3-130">Para facilitar la ejecución de archivos ejecutables de Windows, la ruta de acceso de Windows se incluye en `$PATH` de Linux en Fall Creators Update.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-130">To make Windows executables easier to run, Windows path is included in the Linux `$PATH` in Fall Creators Update.</span></span>

<span data-ttu-id="9f8a3-131">Las aplicaciones que se ejecutan de esta manera tienen las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="9f8a3-131">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="9f8a3-132">Conservan el directorio de trabajo como el símbolo del sistema de WSL (en la mayoría de los casos; las excepciones se explican a continuación).</span><span class="sxs-lookup"><span data-stu-id="9f8a3-132">Retain the working directory as the WSL command prompt (for the most part -- exceptions are explained below).</span></span>
1. <span data-ttu-id="9f8a3-133">Tienen los mismos derechos de permiso que el proceso de WSL.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-133">Have the same permission rights as the WSL process.</span></span>
1. <span data-ttu-id="9f8a3-134">Se ejecutan como el usuario activo de Windows.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-134">Run as the active Windows user.</span></span>
1. <span data-ttu-id="9f8a3-135">Aparecen en el administrador de tareas de Windows como si se ejecutaran directamente desde el símbolo del sistema de CMD.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-135">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="9f8a3-136">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="9f8a3-136">Example:</span></span>

``` BASH
$ notepad.exe
```

<span data-ttu-id="9f8a3-137">Los archivos ejecutables de Windows que se ejecutan en WSL se administran de forma similar a los ejecutables nativos de Linux; las canalizaciones, los redireccionamientos e incluso los procesos en segundo plano funcionan según lo previsto.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-137">Windows executables run in WSL are handled similarly to native Linux executables -- piping, redirects, and even backgrounding work as expected.</span></span>

<span data-ttu-id="9f8a3-138">Ejemplos con canalizaciones:</span><span class="sxs-lookup"><span data-stu-id="9f8a3-138">Examples using pipes:</span></span>

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

<span data-ttu-id="9f8a3-139">Ejemplo con comandos de WSL y Windows combinados:</span><span class="sxs-lookup"><span data-stu-id="9f8a3-139">Example using mixed Windows and WSL commands:</span></span>

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

<span data-ttu-id="9f8a3-140">Los archivos binarios de Windows deben incluir la extensión de archivo, coincidir con el caso del archivo y ser ejecutables.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-140">Windows binaries must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="9f8a3-141">Los no ejecutables, incluidos los scripts por lotes y</span><span class="sxs-lookup"><span data-stu-id="9f8a3-141">Non-executables including batch scripts.</span></span>  <span data-ttu-id="9f8a3-142">comandos nativos de CMD como `dir`, se pueden ejecutar con el comando `cmd.exe /C`.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-142">CMD native commands like `dir` can be run with `cmd.exe /C` command.</span></span>

<span data-ttu-id="9f8a3-143">Ejemplos:</span><span class="sxs-lookup"><span data-stu-id="9f8a3-143">Examples:</span></span>

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

<span data-ttu-id="9f8a3-144">Los parámetros se pasan al archivo binario de Windows sin modificar.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-144">Parameters are passed to the Windows binary unmodified.</span></span>

<span data-ttu-id="9f8a3-145">Por ejemplo, los siguientes comandos abrirán `C:\temp\foo.txt` en `notepad.exe`:</span><span class="sxs-lookup"><span data-stu-id="9f8a3-145">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="9f8a3-146">No se admite la modificación de archivos ubicados en VolFs (archivos que no están en `/mnt/<x>`) con una aplicación de Windows en WSL.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-146">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application in WSL is not supported.</span></span>

<span data-ttu-id="9f8a3-147">De manera predeterminada, WSL intenta mantener el directorio de trabajo del archivo binario de Windows como directorio de WSL actual, pero recurrirá al directorio de creación de la instancia si el directorio de trabajo se encuentra en VolFs.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-147">By default, WSL tries to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="9f8a3-148">Por ejemplo: en un principio, `wsl.exe` se inicia desde `C:\temp` y el directorio de WSL actual se cambia a la página principal del usuario.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-148">As an example; `wsl.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="9f8a3-149">Cuando `notepad.exe` se llama desde el directorio particular del usuario, WSL recurre automáticamente a `C:\temp` como directorio de trabajo de notepad.exe:</span><span class="sxs-lookup"><span data-stu-id="9f8a3-149">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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

## <a name="share-environment-variables-between-windows-and-wsl"></a><span data-ttu-id="9f8a3-150">Uso compartido de variables de entorno entre Windows y WSL</span><span class="sxs-lookup"><span data-stu-id="9f8a3-150">Share environment variables between Windows and WSL</span></span>

> <span data-ttu-id="9f8a3-151">Disponible en compilaciones 17063 de Windows Insider y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-151">Available in Windows Insider builds 17063 and later.</span></span>

<span data-ttu-id="9f8a3-152">Antes de la versión 17063, la única variable de entorno de Windows a la que podía tener acceso WSL era `PATH`, por lo que se podían iniciar ejecutables de Win32 desde WSL.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-152">Prior to 17063, only Windows environment variable that WSL could access was `PATH` (so you could launch Win32 executables from under WSL).</span></span>

<span data-ttu-id="9f8a3-153">A partir de la versión 17063, WSL y Windows comparten `WSLENV`, una variable de entorno especial creada para unir las distribuciones de Windows y Linux que se ejecutan en WSL.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-153">Starting in 17063, WSL and Windows share `WSLENV`, a special environment variable created to bridge Windows and Linux distros running on WSL.</span></span>

<span data-ttu-id="9f8a3-154">Propiedades de `WSLENV`:</span><span class="sxs-lookup"><span data-stu-id="9f8a3-154">Properties of `WSLENV`:</span></span>

* <span data-ttu-id="9f8a3-155">Se comparte; existe en entornos de Windows y WSL.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-155">It is shared; it exists in both Windows and WSL environments.</span></span>
* <span data-ttu-id="9f8a3-156">Se trata de una lista de variables de entorno que se pueden compartir entre Windows y WSL.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-156">It is a list of environment variables to share between Windows and WSL.</span></span>
* <span data-ttu-id="9f8a3-157">Puede formatear variables de entorno para que funcionen correctamente en Windows y WSL.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-157">It can format environment variables to work well in Windows and WSL.</span></span>

<span data-ttu-id="9f8a3-158">Hay cuatro marcas disponibles en `WSLENV` que pueden influir en la forma en que se traduce esa variable de entorno.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-158">There are four flags available in `WSLENV` to influence how that environment variable is translated.</span></span>

<span data-ttu-id="9f8a3-159">Marcas `WSLENV`:</span><span class="sxs-lookup"><span data-stu-id="9f8a3-159">`WSLENV` flags:</span></span>

* <span data-ttu-id="9f8a3-160">`/p`: traduce la ruta de acceso entre las rutas de acceso de estilo de WSL/Linux y las rutas de acceso de Win32.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-160">`/p` - translates the path between WSL/Linux style paths and Win32 paths.</span></span>
* <span data-ttu-id="9f8a3-161">`/l`: indica que la variable de entorno es una lista de rutas de acceso.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-161">`/l` - indicates the environment variable is a list of paths.</span></span>
* <span data-ttu-id="9f8a3-162">`/u`: indica que esta variable de entorno solo debe incluirse al ejecutar WSL desde Win32.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-162">`/u` - indicates that this environment variable should only be included when running WSL from Win32.</span></span>
* <span data-ttu-id="9f8a3-163">`/w`: indica que esta variable de entorno solo debe incluirse al ejecutar Win32 desde WSL.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-163">`/w` - indicates that this environment variable should only be included when running Win32 from WSL.</span></span>

<span data-ttu-id="9f8a3-164">Las marcas se pueden combinar según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-164">Flags can be combined as needed.</span></span>

## <a name="disable-interop"></a><span data-ttu-id="9f8a3-165">Deshabilitación de la interoperabilidad</span><span class="sxs-lookup"><span data-stu-id="9f8a3-165">Disable Interop</span></span>

<span data-ttu-id="9f8a3-166">Los usuarios pueden deshabilitar la capacidad de ejecutar archivos binarios de Windows para una única sesión de WSL mediante la ejecución del siguiente comando como raíz:</span><span class="sxs-lookup"><span data-stu-id="9f8a3-166">Users may disable the ability to run Windows binaries for a single WSL session by running the following command as root:</span></span>

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="9f8a3-167">Para volver a habilitar los archivos binarios de Windows, sal de todas las sesiones de WSL y vuelve a ejecutar bash.exe o ejecuta el siguiente comando como raíz:</span><span class="sxs-lookup"><span data-stu-id="9f8a3-167">To reenable Windows binaries either exit all WSL sessions and re-run bash.exe or run the following command as root:</span></span>

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="9f8a3-168">La deshabilitación de la interoperabilidad no se conservará entre sesiones de WSL: la interoperabilidad se habilitará de nuevo cuando se inicie una nueva sesión.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-168">Disabling interop will not persist between WSL sessions -- interop will be enabled again when a new session is launched.</span></span>

## <a name="creators-update-and-anniversary-update"></a><span data-ttu-id="9f8a3-169">Creators Update y Actualización de aniversario</span><span class="sxs-lookup"><span data-stu-id="9f8a3-169">Creators Update and Anniversary Update</span></span>

<span data-ttu-id="9f8a3-170">Aunque la experiencia de interoperabilidad previa a la actualización Fall Creators Update es similar a las experiencias de interoperabilidad más recientes, hay algunas diferencias importantes.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-170">While the interop experience pre-Fall Creators Update is similar to more recent interop experiences, there are a handful of major differences.</span></span>

<span data-ttu-id="9f8a3-171">En resumen:</span><span class="sxs-lookup"><span data-stu-id="9f8a3-171">To summarize:</span></span>

* <span data-ttu-id="9f8a3-172">`bash.exe` ha quedado en desuso y se ha reemplazado por `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-172">`bash.exe` has been deprecated and replaced with `wsl.exe`.</span></span>
* <span data-ttu-id="9f8a3-173">La opción `-c` para ejecutar un único comando no es necesaria con `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-173">`-c` option for running a single command isn't needed with `wsl.exe`.</span></span>
* <span data-ttu-id="9f8a3-174">La ruta de acceso de Windows se incluye en `$PATH` de WSL.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-174">Windows path is included in the WSL `$PATH`</span></span>

<span data-ttu-id="9f8a3-175">El proceso para deshabilitar la interoperabilidad no ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-175">The process for disabling interop is unchanged.</span></span>

### <a name="invoking-wsl-from-the-windows-command-line"></a><span data-ttu-id="9f8a3-176">Invocación de WSL desde la línea de comandos de Windows</span><span class="sxs-lookup"><span data-stu-id="9f8a3-176">Invoking WSL from the Windows Command Line</span></span>

<span data-ttu-id="9f8a3-177">Los archivos binarios de Linux se pueden invocar desde el símbolo del sistema de Windows o desde PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-177">Linux binaries can be invoked from the Windows Command Prompt or from PowerShell.</span></span>  <span data-ttu-id="9f8a3-178">Los archivos binarios que se invocan de esta manera tienen las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="9f8a3-178">Binaries invoked in this way have the following properties:</span></span>

1. <span data-ttu-id="9f8a3-179">Usan el mismo directorio de trabajo que el símbolo del sistema de CMD o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-179">Use the same working directory as the CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="9f8a3-180">Se ejecutan como usuario predeterminado de WSL.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-180">Run as the WSL default user.</span></span>
1. <span data-ttu-id="9f8a3-181">Tienen los mismos derechos administrativos de Windows que el terminal y el proceso de llamada.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-181">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="9f8a3-182">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="9f8a3-182">Example:</span></span>

```console
C:\temp> bash -c "ls -la"
```

<span data-ttu-id="9f8a3-183">Los comandos de Linux a los que se llama de esta manera se administran como cualquier otra aplicación de Windows.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-183">Linux commands called in this way are handled like any other Windows application.</span></span>  <span data-ttu-id="9f8a3-184">Cosas como las entradas, las canalizaciones y los redireccionamientos de archivos funcionan según lo esperado.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-184">Things such as input, piping, and file redirection work as expected.</span></span>

<span data-ttu-id="9f8a3-185">Ejemplos:</span><span class="sxs-lookup"><span data-stu-id="9f8a3-185">Examples:</span></span>

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

<span data-ttu-id="9f8a3-186">Los comandos de WSL pasados a `bash -c` se reenvían al proceso de WSL sin modificaciones.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-186">The WSL commands passed into `bash -c` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="9f8a3-187">Las rutas de acceso de archivo deben especificarse en el formato de WSL y se debe tener cuidado al escapar caracteres relevantes.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-187">File paths must be specified in the WSL format and care must be taken to escape relevant characters.</span></span> <span data-ttu-id="9f8a3-188">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="9f8a3-188">Example:</span></span>

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a><span data-ttu-id="9f8a3-189">Invocación de archivos binarios de Windows desde WSL</span><span class="sxs-lookup"><span data-stu-id="9f8a3-189">Invoking Windows binaries from WSL</span></span>

<span data-ttu-id="9f8a3-190">El subsistema de Windows para Linux puede invocar archivos binarios de Windows directamente desde la línea de comandos de WSL.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-190">The Windows Subsystem for Linux can invoke Windows binaries directly from the WSL command line.</span></span>  <span data-ttu-id="9f8a3-191">Las aplicaciones que se ejecutan de esta manera tienen las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="9f8a3-191">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="9f8a3-192">Conservan el directorio de trabajo como el símbolo del sistema de WSL, excepto en el escenario que se explica a continuación.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-192">Retain the working directory as the WSL command prompt except in the scenario explained below.</span></span>
1. <span data-ttu-id="9f8a3-193">Tienen los mismos derechos de permiso que el proceso de `bash.exe`.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-193">Have the same permission rights as the `bash.exe` process.</span></span> 
1. <span data-ttu-id="9f8a3-194">Se ejecutan como el usuario activo de Windows.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-194">Run as the active Windows user.</span></span>
1. <span data-ttu-id="9f8a3-195">Aparecen en el administrador de tareas de Windows como si se ejecutaran directamente desde el símbolo del sistema de CMD.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-195">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="9f8a3-196">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="9f8a3-196">Example:</span></span>

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

<span data-ttu-id="9f8a3-197">En WSL, estos ejecutables se tratan de forma similar a los ejecutables nativos de Linux.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-197">In WSL, these executables are handled similar to native Linux executables.</span></span>  <span data-ttu-id="9f8a3-198">Esto significa que la adición de directorios a la ruta de acceso de Linux y la canalización entre comandos funciona según lo previsto.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-198">This means adding directories to the Linux path and piping between commands works as expected.</span></span>  <span data-ttu-id="9f8a3-199">Ejemplos:</span><span class="sxs-lookup"><span data-stu-id="9f8a3-199">Examples:</span></span>

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

<span data-ttu-id="9f8a3-200">El archivo binario de Windows debe incluir la extensión de archivo, coincidir con el caso del archivo y ser ejecutable.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-200">The Windows binary must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="9f8a3-201">Los no ejecutables, incluidos los scripts por lotes y comandos como `dir`, se pueden ejecutar con el comando `/mnt/c/Windows/System32/cmd.exe /C`.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-201">Non-executables including batch scripts and command like `dir` can be run with `/mnt/c/Windows/System32/cmd.exe /C` command.</span></span>

<span data-ttu-id="9f8a3-202">Ejemplos:</span><span class="sxs-lookup"><span data-stu-id="9f8a3-202">Examples:</span></span>

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

<span data-ttu-id="9f8a3-203">Los parámetros se pasan al archivo binario de Windows sin modificar.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-203">Parameters are passed to the Windows binary unmodified.</span></span>  

<span data-ttu-id="9f8a3-204">Por ejemplo, los siguientes comandos abrirán `C:\temp\foo.txt` en `notepad.exe`:</span><span class="sxs-lookup"><span data-stu-id="9f8a3-204">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="9f8a3-205">No se admite la modificación de archivos ubicados en VolFs (archivos que no están en `/mnt/<x>`) con una aplicación de Windows.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-205">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application is not supported.</span></span>  <span data-ttu-id="9f8a3-206">De manera predeterminada, WSL intenta mantener el directorio de trabajo del archivo binario de Windows como directorio de WSL actual, pero recurrirá al directorio de creación de la instancia si el directorio de trabajo se encuentra en VolFs.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-206">By default, WSL attempts to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="9f8a3-207">Por ejemplo: en un principio, `bash.exe` se inicia desde `C:\temp` y el directorio de WSL actual se cambia a la página principal del usuario.</span><span class="sxs-lookup"><span data-stu-id="9f8a3-207">As an example; `bash.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="9f8a3-208">Cuando `notepad.exe` se llama desde el directorio particular del usuario, WSL recurre automáticamente a `C:\temp` como directorio de trabajo de notepad.exe:</span><span class="sxs-lookup"><span data-stu-id="9f8a3-208">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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
