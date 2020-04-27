---
title: Material de referencia de comandos del subsistema de Windows para Linux
description: Lista de comandos que administran el subsistema de Windows para Linux
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, subsistemawindows, ubuntu
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: d74a6926fd797f2e1ede0fd5d8d080d0f1ce3f6b
ms.sourcegitcommit: 39d3a2f0f4184eaec8d8fec740aff800e8ea9ac7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/24/2020
ms.locfileid: "71269842"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="ddf2d-104">Material de referencia de comandos del subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="ddf2d-104">Command Reference for Windows Subsystem for Linux</span></span>

<span data-ttu-id="ddf2d-105">La mejor manera de interactuar con el subsistema de Windows para Linux es usar el comando `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-105">The best way to interact with the Windows Subsystem for Linux is to use the `wsl.exe` command.</span></span> 


## `wsl.exe`

<span data-ttu-id="ddf2d-106">A continuación, se muestra una lista con todas las opciones cuando se usa `wsl.exe` a partir de la versión 1903 de Windows.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-106">Below is a list containing all options when using `wsl.exe` as of Windows Version 1903.</span></span>

<span data-ttu-id="ddf2d-107">Con `wsl [Argument] [Options...] [CommandLine]`</span><span class="sxs-lookup"><span data-stu-id="ddf2d-107">Using: `wsl [Argument] [Options...] [CommandLine]`</span></span>

### <a name="arguments-for-running-linux-binaries"></a><span data-ttu-id="ddf2d-108">Argumentos para la ejecución de archivos binarios de Linux</span><span class="sxs-lookup"><span data-stu-id="ddf2d-108">Arguments for running Linux binaries</span></span>

* <span data-ttu-id="ddf2d-109">**Sin argumentos**</span><span class="sxs-lookup"><span data-stu-id="ddf2d-109">**Without arguments**</span></span>

  <span data-ttu-id="ddf2d-110">Si no se proporciona ninguna línea de comandos, wsl.exe inicia el shell predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-110">If no command line is provided, wsl.exe launches the default shell.</span></span>

* <span data-ttu-id="ddf2d-111">**--exec, -e \<CommandLine>**</span><span class="sxs-lookup"><span data-stu-id="ddf2d-111">**--exec, -e \<CommandLine>**</span></span>
  
  <span data-ttu-id="ddf2d-112">Ejecuta el comando especificado sin usar el shell de Linux predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-112">Execute the specified command without using the default Linux shell.</span></span>

* **--**
  
  <span data-ttu-id="ddf2d-113">Pasa el resto de la línea de comandos como está.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-113">Pass the remaining command line as is.</span></span>

<span data-ttu-id="ddf2d-114">Los comandos anteriores también aceptan las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="ddf2d-114">The above commands also accept the following options:</span></span>

* <span data-ttu-id="ddf2d-115">**--distribution, -d \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="ddf2d-115">**--distribution, -d \<Distro>**</span></span>

  <span data-ttu-id="ddf2d-116">Ejecuta la distribución especificada.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-116">Run the specified distribution.</span></span>

* <span data-ttu-id="ddf2d-117">**--user, -u \<UserName>**</span><span class="sxs-lookup"><span data-stu-id="ddf2d-117">**--user, -u \<UserName>**</span></span>

  <span data-ttu-id="ddf2d-118">Ejecuta como el usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-118">Run as the specified user.</span></span>

### <a name="arguments-for-managing-windows-subsystem-for-linux"></a><span data-ttu-id="ddf2d-119">Argumentos para administrar el subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="ddf2d-119">Arguments for managing Windows Subsystem for Linux</span></span>

* <span data-ttu-id="ddf2d-120">**--export \<Distro> \<FileName>**</span><span class="sxs-lookup"><span data-stu-id="ddf2d-120">**--export \<Distro> \<FileName>**</span></span>
  
  <span data-ttu-id="ddf2d-121">Exporta la distribución a un archivo tar.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-121">Exports the distribution to a tar file.</span></span> <span data-ttu-id="ddf2d-122">El nombre de archivo puede ser - para la salida estándar.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-122">The filename can be - for standard output.</span></span>

* <span data-ttu-id="ddf2d-123">**--import \<Distro> \<InstallLocation> \<FileName>**</span><span class="sxs-lookup"><span data-stu-id="ddf2d-123">**--import \<Distro> \<InstallLocation> \<FileName>**</span></span>
  
  <span data-ttu-id="ddf2d-124">Importa el archivo tar especificado como una nueva distribución.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-124">Imports the specified tar file as a new distribution.</span></span> <span data-ttu-id="ddf2d-125">El nombre de archivo puede ser - para la entrada estándar.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-125">The filename can be - for standard input.</span></span>

* <span data-ttu-id="ddf2d-126">**--list, -l [Options]**</span><span class="sxs-lookup"><span data-stu-id="ddf2d-126">**--list, -l [Options]**</span></span>
  
  <span data-ttu-id="ddf2d-127">Enumera distribuciones.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-127">Lists distributions.</span></span>

  <span data-ttu-id="ddf2d-128">Opciones:</span><span class="sxs-lookup"><span data-stu-id="ddf2d-128">Options:</span></span>
  * <span data-ttu-id="ddf2d-129">**--all**</span><span class="sxs-lookup"><span data-stu-id="ddf2d-129">**--all**</span></span>
      
    <span data-ttu-id="ddf2d-130">Enumera todas las distribuciones, incluidas aquellas que se están instalando o desinstalando actualmente.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-130">List all distributions, including distributions that are currently being installed or uninstalled.</span></span>

  * <span data-ttu-id="ddf2d-131">**--running**</span><span class="sxs-lookup"><span data-stu-id="ddf2d-131">**--running**</span></span>
      
    <span data-ttu-id="ddf2d-132">Enumera solo las distribuciones que están actualmente en ejecución.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-132">List only distributions that are currently running.</span></span>

* <span data-ttu-id="ddf2d-133">**--set-default, -s \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="ddf2d-133">**--set-default, -s \<Distro>**</span></span>
  
  <span data-ttu-id="ddf2d-134">Establece la distribución como predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-134">Sets the distribution as the default.</span></span>

* <span data-ttu-id="ddf2d-135">**--terminate, -t \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="ddf2d-135">**--terminate, -t \<Distro>**</span></span>
  
  <span data-ttu-id="ddf2d-136">Finaliza la distribución especificada.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-136">Terminates the specified distribution.</span></span>

* <span data-ttu-id="ddf2d-137">**--unregister \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="ddf2d-137">**--unregister \<Distro>**</span></span>
  
  <span data-ttu-id="ddf2d-138">Anula el registro de la distribución.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-138">Unregisters the distribution.</span></span>
   
* <span data-ttu-id="ddf2d-139">**--help** Muestra información de uso.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-139">**--help** Display usage information.</span></span>

## <a name="additional-commands"></a><span data-ttu-id="ddf2d-140">Comandos adicionales</span><span class="sxs-lookup"><span data-stu-id="ddf2d-140">Additional Commands</span></span>

<span data-ttu-id="ddf2d-141">También hay comando históricos para interactuar con el subsistema de Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-141">There are also historic commands to interact with the Windows Subsystem for Linux.</span></span> <span data-ttu-id="ddf2d-142">Su funcionalidad se incluye en `wsl.exe`, pero siguen estando disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-142">Their functionality is encompassed within `wsl.exe`, but they are still available for use.</span></span> 

### `wslconfig.exe`

<span data-ttu-id="ddf2d-143">Este comando te permite configurar la distribución de WSL.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-143">This command lets you configure your WSL distribution.</span></span> <span data-ttu-id="ddf2d-144">A continuación, se muestra una lista de sus opciones.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-144">Below is a list of its options.</span></span>

<span data-ttu-id="ddf2d-145">Con `wslconfig [Argument] [Options...]`</span><span class="sxs-lookup"><span data-stu-id="ddf2d-145">Using: `wslconfig [Argument] [Options...]`</span></span>

#### <a name="arguments"></a><span data-ttu-id="ddf2d-146">Arguments</span><span class="sxs-lookup"><span data-stu-id="ddf2d-146">Arguments</span></span>
* <span data-ttu-id="ddf2d-147">**/l, /list [Options]**</span><span class="sxs-lookup"><span data-stu-id="ddf2d-147">**/l, /list [Options]**</span></span>
  
  <span data-ttu-id="ddf2d-148">Enumera las distribuciones registradas.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-148">Lists registered distributions.</span></span>
  
  <span data-ttu-id="ddf2d-149">Opciones:</span><span class="sxs-lookup"><span data-stu-id="ddf2d-149">Options:</span></span>
    * <span data-ttu-id="ddf2d-150">**/all**</span><span class="sxs-lookup"><span data-stu-id="ddf2d-150">**/all**</span></span>
    
      <span data-ttu-id="ddf2d-151">Opcionalmente, enumera todas las distribuciones, incluidas aquellas que se están instalando o desinstalando actualmente.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-151">Optionally list all distributions, including distributions that are currently being installed or uninstalled.</span></span>

    * <span data-ttu-id="ddf2d-152">**/running**</span><span class="sxs-lookup"><span data-stu-id="ddf2d-152">**/running**</span></span>
      
      <span data-ttu-id="ddf2d-153">Enumera solo las distribuciones que están actualmente en ejecución.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-153">List only distributions that are currently running.</span></span>

* <span data-ttu-id="ddf2d-154">**/s, /setdefault \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="ddf2d-154">**/s, /setdefault \<Distro>**</span></span>
  
  <span data-ttu-id="ddf2d-155">Establece la distribución como predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-155">Sets the distribution as the default.</span></span>

* <span data-ttu-id="ddf2d-156">**/t, /terminate \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="ddf2d-156">**/t, /terminate \<Distro>**</span></span>
  
  <span data-ttu-id="ddf2d-157">Finaliza la distribución.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-157">Terminates the distribution.</span></span>

* <span data-ttu-id="ddf2d-158">**/u, /unregister \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="ddf2d-158">**/u, /unregister \<Distro>**</span></span>
  
  <span data-ttu-id="ddf2d-159">Anula el registro de la distribución.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-159">Unregisters the distribution.</span></span>
   
* <span data-ttu-id="ddf2d-160">**/upgrade \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="ddf2d-160">**/upgrade \<Distro>**</span></span>
  
  <span data-ttu-id="ddf2d-161">Actualiza la distribución al formato del sistema de archivos de WslFs.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-161">Upgrades the distribution to the WslFs file system format.</span></span>

### `bash.exe`

<span data-ttu-id="ddf2d-162">Este comando se usa para iniciar un shell de Bash.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-162">This command is used to start a bash shell.</span></span> <span data-ttu-id="ddf2d-163">A continuación, se muestran las opciones que se pueden usar con este comando.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-163">Below are the options you can use with this command.</span></span>

<span data-ttu-id="ddf2d-164">Con `bash [Options...]`</span><span class="sxs-lookup"><span data-stu-id="ddf2d-164">Using: `bash [Options...]`</span></span>

* <span data-ttu-id="ddf2d-165">**No se ha especificado ninguna opción**</span><span class="sxs-lookup"><span data-stu-id="ddf2d-165">**No Option given**</span></span>
  
  <span data-ttu-id="ddf2d-166">Inicia el shell de Bash en el directorio actual.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-166">Launches the Bash shell in the current directory.</span></span> <span data-ttu-id="ddf2d-167">Si el shell de Bash no se instala automáticamente, se ejecuta `lxrun /install`.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-167">If the Bash shell is not installed automatically runs `lxrun /install`</span></span>

* **~**
  
  <span data-ttu-id="ddf2d-168">`bash ~` inicia el shell de Bash en el directorio particular del usuario.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-168">`bash ~` launches the bash shell into the user's home directory.</span></span>  <span data-ttu-id="ddf2d-169">Similar a la ejecución de `cd ~`.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-169">Similar to running `cd ~`.</span></span>

* <span data-ttu-id="ddf2d-170">**-c "\<command>"**</span><span class="sxs-lookup"><span data-stu-id="ddf2d-170">**-c "\<command>"**</span></span>
  
  <span data-ttu-id="ddf2d-171">Ejecuta el comando, imprime la salida y vuelve a salir del símbolo del sistema de Windows.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-171">Runs the command, prints the output and exits back to the Windows command prompt.</span></span>
    
  <span data-ttu-id="ddf2d-172">Ejemplo: `bash -c "ls"`.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-172">Example:  `bash -c "ls"`.</span></span>

## <a name="deprecated-commands"></a><span data-ttu-id="ddf2d-173">Comandos en desuso</span><span class="sxs-lookup"><span data-stu-id="ddf2d-173">Deprecated Commands</span></span>

<span data-ttu-id="ddf2d-174">`lxrun.exe` fue el primer comando usado para instalar y administrar el subsistema de Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-174">The `lxrun.exe` was the first command used to install and manage the Windows Subsystem for Linux.</span></span> <span data-ttu-id="ddf2d-175">Está en desuso desde la versión 1803 de Windows 10 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-175">It is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="ddf2d-176">El comando `lxrun.exe` se puede usar para interactuar con el [subsistema de Windows para Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directamente.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-176">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="ddf2d-177">Estos comandos se instalan en el directorio `\Windows\System32` y se pueden ejecutar en un símbolo del sistema de Windows o en PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-177">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

| <span data-ttu-id="ddf2d-178">Comando</span><span class="sxs-lookup"><span data-stu-id="ddf2d-178">Command</span></span>                     | <span data-ttu-id="ddf2d-179">Descripción</span><span class="sxs-lookup"><span data-stu-id="ddf2d-179">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="ddf2d-180">El comando lxrun se usa para administrar la instancia de WSL.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-180">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="ddf2d-181">Inicia el proceso de descarga e instalación.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-181">Starts the download and install process.</span></span> <br/> <span data-ttu-id="ddf2d-182">**/y** se puede agregar para omitir todos los mensajes.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-182">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="ddf2d-183">El mensaje de confirmación se acepta automáticamente y el usuario predeterminado se establece en raíz.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-183">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="ddf2d-184">Desinstala y elimina la imagen de Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-184">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="ddf2d-185">De manera predeterminada, no se quita el directorio particular de Ubuntu del usuario.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-185">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="ddf2d-186">**/y** se puede agregar para aceptar automáticamente el mensaje de confirmación.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-186">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="ddf2d-187">**/full** desinstala y elimina el directorio particular de Ubuntu del usuario.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-187">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="ddf2d-188">Establece el valor predeterminado de Bash en el usuario de Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-188">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="ddf2d-189">Solicitará una contraseña si el usuario especificado no existe.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-189">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="ddf2d-190">Para obtener más información, visita https://aka.ms/wslusers.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-190">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="ddf2d-191">**/y** omite la solicitud de confirmación de la contraseña.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-191">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="ddf2d-192">El usuario se creará sin contraseña.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-192">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="ddf2d-193">Actualiza el índice de paquetes del subsistema.</span><span class="sxs-lookup"><span data-stu-id="ddf2d-193">Updates the subsystem's package index</span></span>          |
