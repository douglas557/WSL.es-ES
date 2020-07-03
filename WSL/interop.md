---
title: Interoperabilidad de Windows con Linux
description: Describe la interoperabilidad de Windows con distribuciones de Linux que se ejecutan en el subsistema de Windows para Linux.
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 2a9b6c8ac65fe28e029ada7f86475c44220a93fe
ms.sourcegitcommit: cb8a61e7de08b1c18622fc78bc5dfa38786e921a
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/10/2020
ms.locfileid: "84663138"
---
# <a name="windows-interoperability-with-linux"></a><span data-ttu-id="d3dd8-103">Interoperabilidad de Windows con Linux</span><span class="sxs-lookup"><span data-stu-id="d3dd8-103">Windows interoperability with Linux</span></span>

<span data-ttu-id="d3dd8-104">El subsistema de Windows para Linux (WSL) está mejorando continuamente la integración entre Windows y Linux.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-104">The Windows Subsystem for Linux (WSL) is continuously improving integration between Windows and Linux.</span></span>  <span data-ttu-id="d3dd8-105">Se puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d3dd8-105">You can:</span></span>

* <span data-ttu-id="d3dd8-106">Ejecuta las herramientas de Windows (por ejemplo, notepad.exe) desde una línea de comandos de Linux (por ejemplo, Ubuntu).</span><span class="sxs-lookup"><span data-stu-id="d3dd8-106">Run Windows tools (ie. notepad.exe) from a Linux command line (ie. Ubuntu).</span></span>
* <span data-ttu-id="d3dd8-107">Ejecuta herramientas de Linux (por ejemplo, grep) desde una línea de comandos de Windows (por ejemplo, PowerShell).</span><span class="sxs-lookup"><span data-stu-id="d3dd8-107">Run Linux tools (ie. grep) from a Windows command line (ie. PowerShell).</span></span>
* <span data-ttu-id="d3dd8-108">Comparte las variables de entorno entre Linux y Windows.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-108">Share environment variables between Linux and Windows.</span></span> <span data-ttu-id="d3dd8-109">(Compilación 17063 o posterior)</span><span class="sxs-lookup"><span data-stu-id="d3dd8-109">(Build 17063+)</span></span>

> [!NOTE]
> <span data-ttu-id="d3dd8-110">Si ejecutas Creators Update (octubre de 2017, compilación 16299) o la Actualización de aniversario (agosto de 2016, compilación 14393), ve a las [versiones anteriores de Windows 10](#earlier-versions-of-windows-10).</span><span class="sxs-lookup"><span data-stu-id="d3dd8-110">If you're running Creators Update (Oct 2017, Build 16299) or Anniversary Update (Aug 2016, Build 14393), jump to the [Earlier versions of Windows 10](#earlier-versions-of-windows-10).</span></span>

## <a name="run-linux-tools-from-a-windows-command-line"></a><span data-ttu-id="d3dd8-111">Ejecución de herramientas de Linux desde una línea de comandos de Windows</span><span class="sxs-lookup"><span data-stu-id="d3dd8-111">Run Linux tools from a Windows command line</span></span>

<span data-ttu-id="d3dd8-112">Ejecuta los archivos binarios de Linux desde el símbolo del sistema de Windows (CMD) o PowerShell mediante `wsl <command>` (o `wsl.exe <command>`).</span><span class="sxs-lookup"><span data-stu-id="d3dd8-112">Run Linux binaries from the Windows Command Prompt (CMD) or PowerShell using `wsl <command>` (or `wsl.exe <command>`).</span></span>

<span data-ttu-id="d3dd8-113">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="d3dd8-113">For example:</span></span>

```powershell
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

<span data-ttu-id="d3dd8-114">Los archivos binarios se invocan de esta manera:</span><span class="sxs-lookup"><span data-stu-id="d3dd8-114">Binaries invoked in this way:</span></span>

* <span data-ttu-id="d3dd8-115">Usan el mismo directorio de trabajo que el símbolo del sistema actual de CMD o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-115">Use the same working directory as the current CMD or PowerShell prompt.</span></span>
* <span data-ttu-id="d3dd8-116">Se ejecutan como usuario predeterminado de WSL.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-116">Run as the WSL default user.</span></span>
* <span data-ttu-id="d3dd8-117">Tienen los mismos derechos administrativos de Windows que el terminal y el proceso de llamada.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-117">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="d3dd8-118">El comando de Linux que sigue a `wsl` (o `wsl.exe`) se controla como cualquier comando que se ejecute en WSL.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-118">The Linux command following `wsl` (or `wsl.exe`) is handled like any command run in WSL.</span></span>  <span data-ttu-id="d3dd8-119">Funcionan cosas como sudo, canalizaciones y redireccionamientos de archivos.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-119">Things such as sudo, piping, and file redirection work.</span></span>

<span data-ttu-id="d3dd8-120">Ejemplo de uso de sudo para actualizar la distribución de Linux predeterminada:</span><span class="sxs-lookup"><span data-stu-id="d3dd8-120">Example using sudo to update your default Linux distribution:</span></span>

```powershell
C:\temp> wsl sudo apt-get update
```

<span data-ttu-id="d3dd8-121">Después de ejecutar este comando, se mostrará el nombre de usuario predeterminado de la distribución de Linux y se te pedirá la contraseña.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-121">Your default Linux distribution user name will be listed after running this command and you will be asked for your password.</span></span> <span data-ttu-id="d3dd8-122">Después de escribir la contraseña correctamente, la distribución descargará las actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-122">After entering your password correctly, your distribution will download updates.</span></span>

## <a name="mixing-linux-and-windows-commands"></a><span data-ttu-id="d3dd8-123">Combinación de comandos de Windows y Linux</span><span class="sxs-lookup"><span data-stu-id="d3dd8-123">Mixing Linux and Windows commands</span></span>

<span data-ttu-id="d3dd8-124">Estos son algunos ejemplos de la combinación de comandos de Linux y Windows mediante PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-124">Here are a few examples of mixing Linux and Windows commands using PowerShell.</span></span>

<span data-ttu-id="d3dd8-125">Para usar el comando de Linux `ls -la` para enumerar archivos y el comando de PowerShell `findstr` para filtrar los resultados de las palabras que contienen "git", combina los comandos siguientes:</span><span class="sxs-lookup"><span data-stu-id="d3dd8-125">To use the Linux command `ls -la` to list files and the PowerShell command `findstr` to filter the results for words containing "git", combine the commands:</span></span>

```powershell
wsl ls -la | findstr "git"
```

<span data-ttu-id="d3dd8-126">Para usar el comando de PowerShell `dir` para enumerar archivos y el comando de Linux `grep` para filtrar los resultados de las palabras que contienen "git", combina los comandos siguientes:</span><span class="sxs-lookup"><span data-stu-id="d3dd8-126">To use the PowerShell command `dir` to list files and the Linux command `grep` to filter the results for words containing "git", combine the commands:</span></span>

```powershell
C:\temp> dir | wsl grep git
```

<span data-ttu-id="d3dd8-127">Para usar el comando de Linux `ls -la` para enumerar archivos y el comando de PowerShell `> out.txt` para imprimir esa lista en un archivo de texto denominado "out.txt", combina los comandos siguientes:</span><span class="sxs-lookup"><span data-stu-id="d3dd8-127">To use the Linux command `ls -la` to list files and the PowerShell command `> out.txt` to print that list to a text file named "out.txt", combine the commands:</span></span>

```powershell
C:\temp> wsl ls -la > out.txt
```

<span data-ttu-id="d3dd8-128">Los comandos pasados a `wsl.exe` se reenvían al proceso de WSL sin modificaciones.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-128">The commands passed into `wsl.exe` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="d3dd8-129">Las rutas de acceso de archivo deben especificarse en el formato de WSL.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-129">File paths must be specified in the WSL format.</span></span>

<span data-ttu-id="d3dd8-130">Para usar el comando de Linux `ls -la` para enumerar los archivos de la ruta de acceso del sistema de archivos de Linux `/proc/cpuinfo` mediante PowerShell, utiliza el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="d3dd8-130">To use the Linux command `ls -la` to list files in the `/proc/cpuinfo` Linux file system path, using PowerShell:</span></span>

```powershell
C:\temp> wsl ls -la /proc/cpuinfo
```

<span data-ttu-id="d3dd8-131">Para usar el comando de Linux `ls -la` para enumerar los archivos de la ruta de acceso del sistema de archivos de Windows `C:\Program Files` mediante PowerShell, utiliza el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="d3dd8-131">To use the Linux command `ls -la` to list files in the `C:\Program Files` Windows file system path, using PowerShell:</span></span>

```powershell
C:\temp> wsl ls -la "/mnt/c/Program Files"
```

## <a name="run-windows-tools-from-linux"></a><span data-ttu-id="d3dd8-132">Ejecución de herramientas de Windows desde Linux</span><span class="sxs-lookup"><span data-stu-id="d3dd8-132">Run Windows tools from Linux</span></span>

<span data-ttu-id="d3dd8-133">WSL puede ejecutar herramientas de Windows directamente desde la línea de comandos de WSL mediante `[tool-name].exe`.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-133">WSL can run Windows tools directly from the WSL command line using `[tool-name].exe`.</span></span>  <span data-ttu-id="d3dd8-134">Por ejemplo, `notepad.exe`.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-134">For example, `notepad.exe`.</span></span>

<!-- Craig - could you help add a section with an example here to explain this scenario: "To access your Linux files using a Windows tool, use `\\wsl$\<distroName>\'` as the file path." Currently it I can just enter `notepad.exe foo.txt` and it seems to work fine, so explaining a situation where the file path is needed would be helpful. -->

<span data-ttu-id="d3dd8-135">Las aplicaciones que se ejecutan de esta manera tienen las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="d3dd8-135">Applications run this way have the following properties:</span></span>

* <span data-ttu-id="d3dd8-136">Conservan el directorio de trabajo como el símbolo del sistema de WSL (en la mayoría de los casos; las excepciones se explican a continuación).</span><span class="sxs-lookup"><span data-stu-id="d3dd8-136">Retain the working directory as the WSL command prompt (for the most part -- exceptions are explained below).</span></span>
* <span data-ttu-id="d3dd8-137">Tienen los mismos derechos de permiso que el proceso de WSL.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-137">Have the same permission rights as the WSL process.</span></span>
* <span data-ttu-id="d3dd8-138">Se ejecutan como el usuario activo de Windows.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-138">Run as the active Windows user.</span></span>
* <span data-ttu-id="d3dd8-139">Aparecen en el administrador de tareas de Windows como si se ejecutaran directamente desde el símbolo del sistema de CMD.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-139">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="d3dd8-140">Los archivos ejecutables de Windows que se ejecutan en WSL se administran de forma similar a los ejecutables nativos de Linux; las canalizaciones, los redireccionamientos e incluso los procesos en segundo plano funcionan según lo previsto.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-140">Windows executables run in WSL are handled similarly to native Linux executables -- piping, redirects, and even backgrounding work as expected.</span></span>

<span data-ttu-id="d3dd8-141">Para ejecutar la herramientas de Windows `ipconfig.exe`, usa la herramienta de Linux `grep` para filtrar los resultados de "IPv4", y usa la herramienta de Linux `cut` para quitar los campos de columna. Desde una distribución de Linux (por ejemplo, Ubuntu), escribe lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d3dd8-141">To run the Windows tool `ipconfig.exe`, use the Linux tool `grep` to filter the "IPv4" results, and use the Linux tool `cut` to remove the column fields, from a Linux distribution (for example, Ubuntu) enter:</span></span>

```bash
ipconfig.exe | grep IPv4 | cut -d: -f2
```

<span data-ttu-id="d3dd8-142">Vamos a probar un ejemplo de combinación de comandos de Windows y Linux.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-142">Let's try an example mixing Windows and Linux commands.</span></span> <span data-ttu-id="d3dd8-143">Abre tu distribución de Linux (por ejemplo, Ubuntu) y crea el archivo de texto `touch foo.txt`.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-143">Open your Linux distribution (ie. Ubuntu) and create a text file: `touch foo.txt`.</span></span> <span data-ttu-id="d3dd8-144">Ahora usa el comando de Linux `ls -la` para enumerar los archivos directos y sus detalles de creación, además de la herramienta de Windows PowerShell `findstr.exe` para filtrar los resultados, de modo que solo se muestre el archivo `foo.txt` en los resultados:</span><span class="sxs-lookup"><span data-stu-id="d3dd8-144">Now use the Linux command `ls -la` to list the direct files and their creation details, plus the Windows PowerShell tool `findstr.exe` to filter the results so only your `foo.txt` file shows in the results:</span></span>

```bash
ls -la | findstr.exe foo.txt
```

<span data-ttu-id="d3dd8-145">Las herramientas de Windows deben incluir la extensión de archivo, coincidir con el caso del archivo y ser ejecutables.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-145">Windows tools must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="d3dd8-146">Los no ejecutables, incluidos los scripts por lotes y</span><span class="sxs-lookup"><span data-stu-id="d3dd8-146">Non-executables including batch scripts.</span></span>  <span data-ttu-id="d3dd8-147">comandos nativos de CMD como `dir`, se pueden ejecutar con el comando `cmd.exe /C`.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-147">CMD native commands like `dir` can be run with `cmd.exe /C` command.</span></span>

<span data-ttu-id="d3dd8-148">Por ejemplo, para enumerar el contenido del directorio C:\ del sistema de archivos de Windows, escribe:</span><span class="sxs-lookup"><span data-stu-id="d3dd8-148">For example, list the contents of your Windows files system C:\ directory, by entering:</span></span>

```bash
cmd.exe /C dir
```

<span data-ttu-id="d3dd8-149">O bien usa el comando `ping` para enviar una solicitud de eco al sitio web microsoft.com:</span><span class="sxs-lookup"><span data-stu-id="d3dd8-149">Or use the `ping` command to send an echo request to the microsoft.com website:</span></span>

```bash
ping.exe www.microsoft.com
```

<span data-ttu-id="d3dd8-150">Los parámetros se pasan al archivo binario de Windows sin modificar.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-150">Parameters are passed to the Windows binary unmodified.</span></span> <span data-ttu-id="d3dd8-151">Por ejemplo, el siguiente comando abrirá `C:\temp\foo.txt` en `notepad.exe`:</span><span class="sxs-lookup"><span data-stu-id="d3dd8-151">As an example, the following command will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

```bash
notepad.exe "C:\temp\foo.txt"
```

<span data-ttu-id="d3dd8-152">También funcionará lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d3dd8-152">This will also work:</span></span>

```bash
notepad.exe C:\\temp\\foo.txt
```

## <a name="share-environment-variables-between-windows-and-wsl"></a><span data-ttu-id="d3dd8-153">Uso compartido de variables de entorno entre Windows y WSL</span><span class="sxs-lookup"><span data-stu-id="d3dd8-153">Share environment variables between Windows and WSL</span></span>

<span data-ttu-id="d3dd8-154">WSL y Windows comparten `WSLENV`, una variable de entorno especial creada para unir las distribuciones de Windows y Linux que se ejecutan en WSL.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-154">WSL and Windows share a special environment variable, `WSLENV`, created to bridge Windows and Linux distributions running on WSL.</span></span>

<span data-ttu-id="d3dd8-155">Propiedades de la variable `WSLENV`:</span><span class="sxs-lookup"><span data-stu-id="d3dd8-155">Properties of `WSLENV` variable:</span></span>

* <span data-ttu-id="d3dd8-156">Se comparte; existe en entornos de Windows y WSL.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-156">It is shared; it exists in both Windows and WSL environments.</span></span>
* <span data-ttu-id="d3dd8-157">Se trata de una lista de variables de entorno que se pueden compartir entre Windows y WSL.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-157">It is a list of environment variables to share between Windows and WSL.</span></span>
* <span data-ttu-id="d3dd8-158">Puede formatear variables de entorno para que funcionen correctamente en Windows y WSL.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-158">It can format environment variables to work well in Windows and WSL.</span></span>
* <span data-ttu-id="d3dd8-159">Puede ayudar en el flujo entre WSL y Win32.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-159">It can assist in the flow between WSL and Win32.</span></span>

> [!NOTE]
> <span data-ttu-id="d3dd8-160">Antes de la versión 17063, la única variable de entorno de Windows a la que podía tener acceso WSL era `PATH`, por lo que se podían iniciar ejecutables de Win32 desde WSL.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-160">Prior to 17063, only Windows environment variable that WSL could access was `PATH` (so you could launch Win32 executables from under WSL).</span></span> <span data-ttu-id="d3dd8-161">A partir de 17063, `WSLENV` comienza a ser compatible.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-161">Starting in 17063, `WSLENV` begins being supported.</span></span>

## <a name="wslenv-flags"></a><span data-ttu-id="d3dd8-162">Marcas de WSLENV</span><span class="sxs-lookup"><span data-stu-id="d3dd8-162">WSLENV flags</span></span>

<span data-ttu-id="d3dd8-163">Hay cuatro marcas disponibles en `WSLENV` que pueden influir en la forma en que se traduce la variable de entorno.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-163">There are four flags available in `WSLENV` to influence how the environment variable is translated.</span></span>

<span data-ttu-id="d3dd8-164">Marcas `WSLENV`:</span><span class="sxs-lookup"><span data-stu-id="d3dd8-164">`WSLENV` flags:</span></span>

* <span data-ttu-id="d3dd8-165">`/p`: traduce la ruta de acceso entre las rutas de acceso de estilo de WSL/Linux y las rutas de acceso de Win32.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-165">`/p` - translates the path between WSL/Linux style paths and Win32 paths.</span></span>
* <span data-ttu-id="d3dd8-166">`/l`: indica que la variable de entorno es una lista de rutas de acceso.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-166">`/l` - indicates the environment variable is a list of paths.</span></span>
* <span data-ttu-id="d3dd8-167">`/u`: indica que esta variable de entorno solo debe incluirse al ejecutar WSL desde Win32.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-167">`/u` - indicates that this environment variable should only be included when running WSL from Win32.</span></span>
* <span data-ttu-id="d3dd8-168">`/w`: indica que esta variable de entorno solo debe incluirse al ejecutar Win32 desde WSL.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-168">`/w` - indicates that this environment variable should only be included when running Win32 from WSL.</span></span>

<span data-ttu-id="d3dd8-169">Las marcas se pueden combinar según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-169">Flags can be combined as needed.</span></span>

<span data-ttu-id="d3dd8-170">[Obtenga más información sobre WSLENV](https://devblogs.microsoft.com/commandline/share-environment-vars-between-wsl-and-windows/), incluidas las preguntas más frecuentes y ejemplos de configuración del valor de WSLENV en una concatenación de otras variables de entorno predefinidas, cada una con una barra diagonal como sufijo seguida de marcas para especificar cómo se debe traducir el valor y pasar las variables con un script.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-170">[Read more about WSLENV](https://devblogs.microsoft.com/commandline/share-environment-vars-between-wsl-and-windows/), including FAQs and examples of setting the value of WSLENV to a concatenation of other pre-defined environment vars, each suffixed with a slash followed by flags to specify how the value should be translated and passing variables with a script.</span></span> <span data-ttu-id="d3dd8-171">En este artículo también se incluye un ejemplo para configurar un entorno de desarrollo con el [lenguaje de programación Go](https://golang.org/), configurado para compartir una variable GOPATH entre WSL y Win32.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-171">This article also includes an example for setting up a dev environment with the [Go programming language](https://golang.org/), configured to share a GOPATH between WSL and Win32.</span></span>

## <a name="disable-interoperability"></a><span data-ttu-id="d3dd8-172">Deshabilitación de la interoperabilidad</span><span class="sxs-lookup"><span data-stu-id="d3dd8-172">Disable interoperability</span></span>

<span data-ttu-id="d3dd8-173">Los usuarios pueden deshabilitar la capacidad de ejecutar herramientas de Windows para una única sesión de WSL mediante la ejecución del siguiente comando como raíz:</span><span class="sxs-lookup"><span data-stu-id="d3dd8-173">Users may disable the ability to run Windows tools for a single WSL session by running the following command as root:</span></span>

```bash
echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="d3dd8-174">Para volver a habilitar los archivos binarios de Windows, sal de todas las sesiones de WSL y vuelve a ejecutar bash.exe o ejecuta el siguiente comando como raíz:</span><span class="sxs-lookup"><span data-stu-id="d3dd8-174">To re-enable Windows binaries, exit all WSL sessions and re-run bash.exe or run the following command as root:</span></span>

```bash
echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="d3dd8-175">La deshabilitación de la interoperabilidad no se conservará entre sesiones de WSL: la interoperabilidad se habilitará de nuevo cuando se inicie una nueva sesión.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-175">Disabling interop will not persist between WSL sessions -- interop will be enabled again when a new session is launched.</span></span>

## <a name="earlier-versions-of-windows-10"></a><span data-ttu-id="d3dd8-176">Versiones anteriores de Windows 10</span><span class="sxs-lookup"><span data-stu-id="d3dd8-176">Earlier versions of Windows 10</span></span>

<span data-ttu-id="d3dd8-177">Hay varias diferencias para los comandos de interoperabilidad en las versiones anteriores de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-177">There are several differences for the interoperability commands on earlier Windows 10 versions.</span></span> <span data-ttu-id="d3dd8-178">Si ejecutas una versión de Creators Update (octubre de 2017, compilación 16299) o la Actualización de aniversario (agosto de 2016, compilación 14393) de Windows 10, te recomendamos [actualizar a la versión más reciente de Windows](ms-settings:windowsupdate). Pero si esto no es posible, a continuación describimos algunas de las diferencias en la interoperabilidad.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-178">If you're running a Creators Update (Oct 2017, Build 16299), or Anniversary Update (Aug 2016, Build 14393) version of Windows 10, we recommend you [update to the latest Windows version](ms-settings:windowsupdate), but if that's not possible, we have outlined some of the interop differences below.</span></span>

<span data-ttu-id="d3dd8-179">Resumen:</span><span class="sxs-lookup"><span data-stu-id="d3dd8-179">Summary:</span></span>

* <span data-ttu-id="d3dd8-180">`bash.exe` se ha reemplazado por `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-180">`bash.exe` has been replaced with `wsl.exe`.</span></span>
* <span data-ttu-id="d3dd8-181">La opción `-c` para ejecutar un único comando no es necesaria con `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-181">`-c` option for running a single command isn't needed with `wsl.exe`.</span></span>
* <span data-ttu-id="d3dd8-182">La ruta de acceso de Windows se incluye en `$PATH` de WSL.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-182">Windows path is included in the WSL `$PATH`.</span></span>
* <span data-ttu-id="d3dd8-183">El proceso para deshabilitar la interoperabilidad no ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-183">The process for disabling interop is unchanged.</span></span>

<span data-ttu-id="d3dd8-184">Los comandos de Linux se pueden ejecutar desde el símbolo del sistema de Windows o desde PowerShell, pero para las primeras versiones de Windows, puede que tengas que usar el comando `bash`.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-184">Linux commands can be run from the Windows Command Prompt or from PowerShell, but for early Windows versions, you man need to use the `bash` command.</span></span> <span data-ttu-id="d3dd8-185">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="d3dd8-185">For example:</span></span>

```powershell
C:\temp> bash -c "ls -la"
```

<span data-ttu-id="d3dd8-186">Cosas como las entradas, las canalizaciones y los redireccionamientos de archivos funcionan según lo esperado.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-186">Things such as input, piping, and file redirection work as expected.</span></span>

<span data-ttu-id="d3dd8-187">Los comandos de WSL pasados a `bash -c` se reenvían al proceso de WSL sin modificaciones.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-187">The WSL commands passed into `bash -c` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="d3dd8-188">Las rutas de acceso de archivo deben especificarse en el formato de WSL y se debe tener cuidado al escapar caracteres relevantes.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-188">File paths must be specified in the WSL format and care must be taken to escape relevant characters.</span></span> <span data-ttu-id="d3dd8-189">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="d3dd8-189">Example:</span></span>

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
```

<span data-ttu-id="d3dd8-190">O bien...</span><span class="sxs-lookup"><span data-stu-id="d3dd8-190">Or...</span></span>

```powershell
C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
```

<span data-ttu-id="d3dd8-191">Al llamar a una herramienta de Windows desde una distribución de WSL en una versión anterior de Windows 10, deberás especificar la ruta de acceso del directorio.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-191">When calling a Windows tool from a WSL distribution in an earlier version of Windows 10, you will need to specify the directory path.</span></span> <span data-ttu-id="d3dd8-192">Por ejemplo, desde la línea de comandos de WSL, escribe:</span><span class="sxs-lookup"><span data-stu-id="d3dd8-192">For example, from your WSL command line, enter:</span></span>

```bash
/mnt/c/Windows/System32/notepad.exe
```

<span data-ttu-id="d3dd8-193">En WSL, estos ejecutables se tratan de forma similar a los ejecutables nativos de Linux.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-193">In WSL, these executables are handled similar to native Linux executables.</span></span>  <span data-ttu-id="d3dd8-194">Esto significa que la adición de directorios a la ruta de acceso de Linux y la canalización entre comandos funciona según lo previsto.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-194">This means adding directories to the Linux path and piping between commands works as expected.</span></span>  <span data-ttu-id="d3dd8-195">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="d3dd8-195">For example:</span></span>

```bash
export PATH=$PATH:/mnt/c/Windows/System32
```
<span data-ttu-id="d3dd8-196">O bien</span><span class="sxs-lookup"><span data-stu-id="d3dd8-196">Or</span></span>

```bash
ipconfig.exe | grep IPv4 | cut -d: -f2
```

<span data-ttu-id="d3dd8-197">El archivo binario de Windows debe incluir la extensión de archivo, coincidir con el caso del archivo y ser ejecutable.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-197">The Windows binary must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="d3dd8-198">Los no ejecutables, incluidos los scripts por lotes y comandos como `dir`, se pueden ejecutar con el comando `/mnt/c/Windows/System32/cmd.exe /C`.</span><span class="sxs-lookup"><span data-stu-id="d3dd8-198">Non-executables including batch scripts and command like `dir` can be run with `/mnt/c/Windows/System32/cmd.exe /C` command.</span></span> <span data-ttu-id="d3dd8-199">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="d3dd8-199">For example:</span></span>

```bash
/mnt/c/Windows/System32/cmd.exe /C dir
```

## <a name="additional-resources"></a><span data-ttu-id="d3dd8-200">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="d3dd8-200">Additional resources</span></span>

* [<span data-ttu-id="d3dd8-201">Entrada de blog de WSL sobre la interoperabilidad, de 2016</span><span class="sxs-lookup"><span data-stu-id="d3dd8-201">WSL blog post on interoperability from 2016</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)
