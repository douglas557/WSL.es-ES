---
title: Material de referencia de comandos del subsistema de Windows para Linux
description: Vea una lista de comandos que administran el Subsistema de Windows para Linux, como argumentos para ejecutar comandos de Linux.
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, subsistemawindows, ubuntu
ms.date: 07/31/2017
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: fc5c9e06c597092a3790ba7f9eb06054a33450c1
ms.sourcegitcommit: fb79750bd71d6ebaed5203b3de71ba85a67227b1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2020
ms.locfileid: "88866136"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="19bcd-104">Material de referencia de comandos del subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="19bcd-104">Command Reference for Windows Subsystem for Linux</span></span>

<span data-ttu-id="19bcd-105">La mejor manera de interactuar con el subsistema de Windows para Linux es usar el comando `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="19bcd-105">The best way to interact with the Windows Subsystem for Linux is to use the `wsl.exe` command.</span></span>

## <a name="set-wsl-2-as-your-default-version"></a><span data-ttu-id="19bcd-106">Definición de WSL 2 como versión predeterminada</span><span class="sxs-lookup"><span data-stu-id="19bcd-106">Set WSL 2 as your default version</span></span>

<span data-ttu-id="19bcd-107">Ejecuta el siguiente comando en PowerShell para establecer WSL 2 como versión predeterminada al instalar una nueva distribución de Linux:</span><span class="sxs-lookup"><span data-stu-id="19bcd-107">Run the following command in Powershell to set WSL 2 as the default version when installing a new Linux distribution:</span></span>

```powershell
wsl --set-default-version 2
```

## <a name="set-your-distribution-version-to-wsl-1-or-wsl-2"></a><span data-ttu-id="19bcd-108">Definición de la versión de la distribución en WSL 1 o WSL 2</span><span class="sxs-lookup"><span data-stu-id="19bcd-108">Set your distribution version to WSL 1 or WSL 2</span></span>

<span data-ttu-id="19bcd-109">Para comprobar la versión de WSL asignada a cada una de las distribuciones de Linux que tienes instaladas, abre la línea de comandos de PowerShell y escribe el comando (solo disponible en [Windows, compilación 19041 o posterior](ms-settings:windowsupdate)) `wsl -l -v`.</span><span class="sxs-lookup"><span data-stu-id="19bcd-109">You can check the WSL version assigned to each of the Linux distributions you have installed by opening the PowerShell command line and entering the command (only available in [Windows Build 19041 or higher](ms-settings:windowsupdate)): `wsl -l -v`</span></span>

```bash
wsl --list --verbose
```

<span data-ttu-id="19bcd-110">Para establecer que una distribución esté respaldada por una de las dos versiones de WSL, ejecuta:</span><span class="sxs-lookup"><span data-stu-id="19bcd-110">To set a distribution to be backed by either version of WSL please run:</span></span>

```bash
wsl --set-version <distribution name> <versionNumber>
```

<span data-ttu-id="19bcd-111">Asegúrate de reemplazar `<distribution name>` por el nombre real de tu distribución, y `<versionNumber>` por el número "1" o "2".</span><span class="sxs-lookup"><span data-stu-id="19bcd-111">Make sure to replace `<distribution name>` with the actual name of your distribution and `<versionNumber>` with the number '1' or '2'.</span></span> <span data-ttu-id="19bcd-112">Puedes volver a cambiar a WSL 1 en cualquier momento; para ello, ejecuta el mismo comando que antes, pero reemplaza "2" por "1".</span><span class="sxs-lookup"><span data-stu-id="19bcd-112">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="19bcd-113">Además, si quieres que WSL 2 sea la arquitectura predeterminada, puedes hacerlo con este comando:</span><span class="sxs-lookup"><span data-stu-id="19bcd-113">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

```bash
wsl --set-default-version 2
```

<span data-ttu-id="19bcd-114">De este modo, se establecerá la versión de cualquier nueva distribución instalada en WSL 2.</span><span class="sxs-lookup"><span data-stu-id="19bcd-114">This will set the version of any new distribution installed to WSL 2.</span></span>

## `wsl.exe`

<span data-ttu-id="19bcd-115">A continuación, se muestra una lista con todas las opciones cuando se usa `wsl.exe` a partir de la versión 1903 de Windows.</span><span class="sxs-lookup"><span data-stu-id="19bcd-115">Below is a list containing all options when using `wsl.exe` as of Windows Version 1903.</span></span>

<span data-ttu-id="19bcd-116">Con `wsl [Argument] [Options...] [CommandLine]`</span><span class="sxs-lookup"><span data-stu-id="19bcd-116">Using: `wsl [Argument] [Options...] [CommandLine]`</span></span>

### <a name="arguments-for-running-linux-commands"></a><span data-ttu-id="19bcd-117">Argumentos para la ejecución de comandos de Linux</span><span class="sxs-lookup"><span data-stu-id="19bcd-117">Arguments for running Linux commands</span></span>

* <span data-ttu-id="19bcd-118">**Sin argumentos**</span><span class="sxs-lookup"><span data-stu-id="19bcd-118">**Without arguments**</span></span>

  <span data-ttu-id="19bcd-119">Si no se proporciona ninguna línea de comandos, wsl.exe inicia el shell predeterminado.</span><span class="sxs-lookup"><span data-stu-id="19bcd-119">If no command line is provided, wsl.exe launches the default shell.</span></span>

* <span data-ttu-id="19bcd-120">**--exec, -e \<CommandLine>**</span><span class="sxs-lookup"><span data-stu-id="19bcd-120">**--exec, -e \<CommandLine>**</span></span>
  
  <span data-ttu-id="19bcd-121">Ejecuta el comando especificado sin usar el shell de Linux predeterminado.</span><span class="sxs-lookup"><span data-stu-id="19bcd-121">Execute the specified command without using the default Linux shell.</span></span>

* **--**
  
  <span data-ttu-id="19bcd-122">Pasa el resto de la línea de comandos como está.</span><span class="sxs-lookup"><span data-stu-id="19bcd-122">Pass the remaining command line as is.</span></span>

<span data-ttu-id="19bcd-123">Los comandos anteriores también aceptan las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="19bcd-123">The above commands also accept the following options:</span></span>

* <span data-ttu-id="19bcd-124">**--distribution, -d \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="19bcd-124">**--distribution, -d \<Distro>**</span></span>

  <span data-ttu-id="19bcd-125">Ejecuta la distribución especificada.</span><span class="sxs-lookup"><span data-stu-id="19bcd-125">Run the specified distribution.</span></span>

* <span data-ttu-id="19bcd-126">**--user, -u \<UserName>**</span><span class="sxs-lookup"><span data-stu-id="19bcd-126">**--user, -u \<UserName>**</span></span>

  <span data-ttu-id="19bcd-127">Ejecuta como el usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="19bcd-127">Run as the specified user.</span></span>

### <a name="arguments-for-managing-windows-subsystem-for-linux"></a><span data-ttu-id="19bcd-128">Argumentos para administrar el subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="19bcd-128">Arguments for managing Windows Subsystem for Linux</span></span>

* <span data-ttu-id="19bcd-129">**--export \<Distro> \<FileName>**</span><span class="sxs-lookup"><span data-stu-id="19bcd-129">**--export \<Distro> \<FileName>**</span></span>
  
  <span data-ttu-id="19bcd-130">Exporta la distribución a un archivo tar.</span><span class="sxs-lookup"><span data-stu-id="19bcd-130">Exports the distribution to a tar file.</span></span> <span data-ttu-id="19bcd-131">El nombre de archivo puede ser - para la salida estándar.</span><span class="sxs-lookup"><span data-stu-id="19bcd-131">The filename can be - for standard output.</span></span>

* <span data-ttu-id="19bcd-132">**--import \<Distro> \<InstallLocation> \<FileName>**</span><span class="sxs-lookup"><span data-stu-id="19bcd-132">**--import \<Distro> \<InstallLocation> \<FileName>**</span></span>
  
  <span data-ttu-id="19bcd-133">Importa el archivo tar especificado como una nueva distribución.</span><span class="sxs-lookup"><span data-stu-id="19bcd-133">Imports the specified tar file as a new distribution.</span></span> <span data-ttu-id="19bcd-134">El nombre de archivo puede ser - para la entrada estándar.</span><span class="sxs-lookup"><span data-stu-id="19bcd-134">The filename can be - for standard input.</span></span>

* <span data-ttu-id="19bcd-135">**--list, -l [Options]**</span><span class="sxs-lookup"><span data-stu-id="19bcd-135">**--list, -l [Options]**</span></span>
  
  <span data-ttu-id="19bcd-136">Enumera distribuciones.</span><span class="sxs-lookup"><span data-stu-id="19bcd-136">Lists distributions.</span></span>

  <span data-ttu-id="19bcd-137">Opciones:</span><span class="sxs-lookup"><span data-stu-id="19bcd-137">Options:</span></span>
  * <span data-ttu-id="19bcd-138">**--all**</span><span class="sxs-lookup"><span data-stu-id="19bcd-138">**--all**</span></span>

    <span data-ttu-id="19bcd-139">Enumera todas las distribuciones, incluidas aquellas que se están instalando o desinstalando actualmente.</span><span class="sxs-lookup"><span data-stu-id="19bcd-139">List all distributions, including distributions that are currently being installed or uninstalled.</span></span>

  * <span data-ttu-id="19bcd-140">**--running**</span><span class="sxs-lookup"><span data-stu-id="19bcd-140">**--running**</span></span>

    <span data-ttu-id="19bcd-141">Enumera solo las distribuciones que están actualmente en ejecución.</span><span class="sxs-lookup"><span data-stu-id="19bcd-141">List only distributions that are currently running.</span></span>

* <span data-ttu-id="19bcd-142">**--set-default, -s \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="19bcd-142">**--set-default, -s \<Distro>**</span></span>
  
  <span data-ttu-id="19bcd-143">Establece la distribución como predeterminada.</span><span class="sxs-lookup"><span data-stu-id="19bcd-143">Sets the distribution as the default.</span></span>

* <span data-ttu-id="19bcd-144">**--terminate, -t \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="19bcd-144">**--terminate, -t \<Distro>**</span></span>
  
  <span data-ttu-id="19bcd-145">Finaliza la distribución especificada.</span><span class="sxs-lookup"><span data-stu-id="19bcd-145">Terminates the specified distribution.</span></span>

* <span data-ttu-id="19bcd-146">**--unregister \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="19bcd-146">**--unregister \<Distro>**</span></span>
  
  <span data-ttu-id="19bcd-147">Anula el registro de la distribución.</span><span class="sxs-lookup"><span data-stu-id="19bcd-147">Un-register the distribution.</span></span>

* <span data-ttu-id="19bcd-148">**--help** Muestra información de uso.</span><span class="sxs-lookup"><span data-stu-id="19bcd-148">**--help** Display usage information.</span></span>

## <a name="additional-commands"></a><span data-ttu-id="19bcd-149">Comandos adicionales</span><span class="sxs-lookup"><span data-stu-id="19bcd-149">Additional Commands</span></span>

<span data-ttu-id="19bcd-150">También hay comando históricos para interactuar con el subsistema de Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="19bcd-150">There are also historic commands to interact with the Windows Subsystem for Linux.</span></span> <span data-ttu-id="19bcd-151">Su funcionalidad se incluye en `wsl.exe`, pero siguen estando disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="19bcd-151">Their functionality is encompassed within `wsl.exe`, but they are still available for use.</span></span>

### `wslconfig.exe`

<span data-ttu-id="19bcd-152">Este comando te permite configurar la distribución de WSL.</span><span class="sxs-lookup"><span data-stu-id="19bcd-152">This command lets you configure your WSL distribution.</span></span> <span data-ttu-id="19bcd-153">A continuación, se muestra una lista de sus opciones.</span><span class="sxs-lookup"><span data-stu-id="19bcd-153">Below is a list of its options.</span></span>

<span data-ttu-id="19bcd-154">Con `wslconfig [Argument] [Options...]`</span><span class="sxs-lookup"><span data-stu-id="19bcd-154">Using: `wslconfig [Argument] [Options...]`</span></span>

#### <a name="arguments"></a><span data-ttu-id="19bcd-155">Argumentos</span><span class="sxs-lookup"><span data-stu-id="19bcd-155">Arguments</span></span>

* <span data-ttu-id="19bcd-156">**/l, /list [Options]**</span><span class="sxs-lookup"><span data-stu-id="19bcd-156">**/l, /list [Options]**</span></span>
  
  <span data-ttu-id="19bcd-157">Enumera las distribuciones registradas.</span><span class="sxs-lookup"><span data-stu-id="19bcd-157">Lists registered distributions.</span></span>
  
<span data-ttu-id="19bcd-158">Opciones:</span><span class="sxs-lookup"><span data-stu-id="19bcd-158">Options:</span></span>

* <span data-ttu-id="19bcd-159">**/all**: opcionalmente, enumera todas las distribuciones, incluidas aquellas que se están instalando o desinstalando.</span><span class="sxs-lookup"><span data-stu-id="19bcd-159">**/all** Optionally list all distributions, including distributions that are currently being installed or uninstalled.</span></span>

* <span data-ttu-id="19bcd-160">**/running**: enumera solo las distribuciones que se encuentran en ejecución actualmente.</span><span class="sxs-lookup"><span data-stu-id="19bcd-160">**/running** List only distributions that are currently running.</span></span>

* <span data-ttu-id="19bcd-161">**/s, /setdefault \<Distro>** : establece la distribución como predeterminada.</span><span class="sxs-lookup"><span data-stu-id="19bcd-161">**/s, /setdefault \<Distro>** Sets the distribution as the default.</span></span>

* <span data-ttu-id="19bcd-162">**/t, /terminate \<Distro>** : finaliza la distribución.</span><span class="sxs-lookup"><span data-stu-id="19bcd-162">**/t, /terminate \<Distro>** Terminates the distribution.</span></span>

* <span data-ttu-id="19bcd-163">**/u, /unregister \<Distro>** : anula el registro de la distribución.</span><span class="sxs-lookup"><span data-stu-id="19bcd-163">**/u, /unregister \<Distro>** Un-registers the distribution.</span></span>

* <span data-ttu-id="19bcd-164">**/upgrade \<Distro>** : actualiza la distribución al formato del sistema de archivos de WslFs.</span><span class="sxs-lookup"><span data-stu-id="19bcd-164">**/upgrade \<Distro>** Upgrades the distribution to the WslFs file system format.</span></span>

### `bash.exe`

<span data-ttu-id="19bcd-165">Este comando se usa para iniciar un shell de Bash.</span><span class="sxs-lookup"><span data-stu-id="19bcd-165">This command is used to start a bash shell.</span></span> <span data-ttu-id="19bcd-166">A continuación, se muestran las opciones que se pueden usar con este comando.</span><span class="sxs-lookup"><span data-stu-id="19bcd-166">Below are the options you can use with this command.</span></span>

<span data-ttu-id="19bcd-167">Con `bash [Options...]`</span><span class="sxs-lookup"><span data-stu-id="19bcd-167">Using: `bash [Options...]`</span></span>

* <span data-ttu-id="19bcd-168">**No se ha especificado ninguna opción**</span><span class="sxs-lookup"><span data-stu-id="19bcd-168">**No Option given**</span></span>
  
  <span data-ttu-id="19bcd-169">Inicia el shell de Bash en el directorio actual.</span><span class="sxs-lookup"><span data-stu-id="19bcd-169">Launches the Bash shell in the current directory.</span></span> <span data-ttu-id="19bcd-170">Si el shell de Bash no se instala automáticamente, se ejecuta `lxrun /install`.</span><span class="sxs-lookup"><span data-stu-id="19bcd-170">If the Bash shell is not installed automatically runs `lxrun /install`</span></span>

* **~**
  
  <span data-ttu-id="19bcd-171">`bash ~` inicia el shell de Bash en el directorio particular del usuario.</span><span class="sxs-lookup"><span data-stu-id="19bcd-171">`bash ~` launches the bash shell into the user's home directory.</span></span>  <span data-ttu-id="19bcd-172">Similar a la ejecución de `cd ~`.</span><span class="sxs-lookup"><span data-stu-id="19bcd-172">Similar to running `cd ~`.</span></span>

* <span data-ttu-id="19bcd-173">**-c "\<command>"**</span><span class="sxs-lookup"><span data-stu-id="19bcd-173">**-c "\<command>"**</span></span>
  
  <span data-ttu-id="19bcd-174">Ejecuta el comando, imprime la salida y vuelve a salir del símbolo del sistema de Windows.</span><span class="sxs-lookup"><span data-stu-id="19bcd-174">Runs the command, prints the output and exits back to the Windows command prompt.</span></span>

  <span data-ttu-id="19bcd-175">Ejemplo: `bash -c "ls"`.</span><span class="sxs-lookup"><span data-stu-id="19bcd-175">Example:  `bash -c "ls"`.</span></span>

## <a name="deprecated-commands"></a><span data-ttu-id="19bcd-176">Comandos en desuso</span><span class="sxs-lookup"><span data-stu-id="19bcd-176">Deprecated Commands</span></span>

<span data-ttu-id="19bcd-177">`lxrun.exe` fue el primer comando usado para instalar y administrar el subsistema de Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="19bcd-177">The `lxrun.exe` was the first command used to install and manage the Windows Subsystem for Linux.</span></span> <span data-ttu-id="19bcd-178">Está en desuso desde la versión 1803 de Windows 10 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="19bcd-178">It is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="19bcd-179">El comando `lxrun.exe` se puede usar para interactuar con el [subsistema de Windows para Linux (WSL)](https://msdn.microsoft.com/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directamente.</span><span class="sxs-lookup"><span data-stu-id="19bcd-179">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="19bcd-180">Estos comandos se instalan en el directorio `\Windows\System32` y se pueden ejecutar en un símbolo del sistema de Windows o en PowerShell.</span><span class="sxs-lookup"><span data-stu-id="19bcd-180">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

| <span data-ttu-id="19bcd-181">Comando</span><span class="sxs-lookup"><span data-stu-id="19bcd-181">Command</span></span>                     | <span data-ttu-id="19bcd-182">Descripción</span><span class="sxs-lookup"><span data-stu-id="19bcd-182">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="19bcd-183">El comando lxrun se usa para administrar la instancia de WSL.</span><span class="sxs-lookup"><span data-stu-id="19bcd-183">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="19bcd-184">Inicia el proceso de descarga e instalación.</span><span class="sxs-lookup"><span data-stu-id="19bcd-184">Starts the download and install process.</span></span> <br/> <span data-ttu-id="19bcd-185">**/y** se puede agregar para omitir todos los mensajes.</span><span class="sxs-lookup"><span data-stu-id="19bcd-185">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="19bcd-186">El mensaje de confirmación se acepta automáticamente y el usuario predeterminado se establece en raíz.</span><span class="sxs-lookup"><span data-stu-id="19bcd-186">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="19bcd-187">Desinstala y elimina la imagen de Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="19bcd-187">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="19bcd-188">De manera predeterminada, no se quita el directorio particular de Ubuntu del usuario.</span><span class="sxs-lookup"><span data-stu-id="19bcd-188">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="19bcd-189">**/y** se puede agregar para aceptar automáticamente el mensaje de confirmación.</span><span class="sxs-lookup"><span data-stu-id="19bcd-189">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="19bcd-190">**/full** desinstala y elimina el directorio particular de Ubuntu del usuario.</span><span class="sxs-lookup"><span data-stu-id="19bcd-190">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="19bcd-191">Establece el valor predeterminado de Bash en el usuario de Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="19bcd-191">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="19bcd-192">Solicitará una contraseña si el usuario especificado no existe.</span><span class="sxs-lookup"><span data-stu-id="19bcd-192">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="19bcd-193">Para obtener más información, visita https://aka.ms/wslusers.</span><span class="sxs-lookup"><span data-stu-id="19bcd-193">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="19bcd-194">**/y** omite la solicitud de confirmación de la contraseña.</span><span class="sxs-lookup"><span data-stu-id="19bcd-194">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="19bcd-195">El usuario se creará sin contraseña.</span><span class="sxs-lookup"><span data-stu-id="19bcd-195">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="19bcd-196">Actualiza el índice de paquetes del subsistema.</span><span class="sxs-lookup"><span data-stu-id="19bcd-196">Updates the subsystem's package index</span></span>          |
