---
title: Referencia de comandos de subsistema de Windows para Linux
description: Lista de comandos que administran el subsistema de Windows para Linux
keywords: BashOnWindows, bash, WSL, Windows, subsistema de Windows para Linux, windowssubsystem, Ubuntu
author: scooley
ms.author: scooley
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.openlocfilehash: 018b02b43e859476f7ee38f54df8efa0ca0e652b
ms.sourcegitcommit: 62c49d435a91f2e390c3c495f3e09e62b5ada13c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2019
ms.locfileid: "69578840"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="f9e58-104">Referencia de comandos para el subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="f9e58-104">Command Reference for Windows Subsystem for Linux</span></span>

<span data-ttu-id="f9e58-105">La mejor manera de interactuar con el subsistema de Windows para Linux es usar el `wsl.exe` comando.</span><span class="sxs-lookup"><span data-stu-id="f9e58-105">The best way to interact with the Windows Subsystem for Linux is to use the `wsl.exe` command.</span></span> 


## `wsl.exe`

<span data-ttu-id="f9e58-106">A continuación se muestra una lista con todas las `wsl.exe` opciones cuando se usa a partir de la versión 1903 de Windows.</span><span class="sxs-lookup"><span data-stu-id="f9e58-106">Below is a list containing all options when using `wsl.exe` as of Windows Version 1903.</span></span>

<span data-ttu-id="f9e58-107">Utilizan`wsl [Argument] [Options...] [CommandLine]`</span><span class="sxs-lookup"><span data-stu-id="f9e58-107">Using: `wsl [Argument] [Options...] [CommandLine]`</span></span>

### <a name="arguments-for-running-linux-binaries"></a><span data-ttu-id="f9e58-108">Argumentos para la ejecución de archivos binarios de Linux</span><span class="sxs-lookup"><span data-stu-id="f9e58-108">Arguments for running Linux binaries</span></span>

* <span data-ttu-id="f9e58-109">**Sin argumentos**</span><span class="sxs-lookup"><span data-stu-id="f9e58-109">**Without arguments**</span></span>

  <span data-ttu-id="f9e58-110">Si no se proporciona ninguna línea de comandos, WSL. exe inicia el shell predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f9e58-110">If no command line is provided, wsl.exe launches the default shell.</span></span>

* <span data-ttu-id="f9e58-111">**--exec,-e \<línea de comandos >**</span><span class="sxs-lookup"><span data-stu-id="f9e58-111">**--exec, -e \<CommandLine>**</span></span>
  
  <span data-ttu-id="f9e58-112">Ejecute el comando especificado sin usar el shell de Linux predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f9e58-112">Execute the specified command without using the default Linux shell.</span></span>

* **--**
  
  <span data-ttu-id="f9e58-113">Pase el resto de la línea de comandos tal y como está.</span><span class="sxs-lookup"><span data-stu-id="f9e58-113">Pass the remaining command line as is.</span></span>

<span data-ttu-id="f9e58-114">Los comandos anteriores también aceptan las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="f9e58-114">The above commands also accept the following options:</span></span>

* <span data-ttu-id="f9e58-115">**--Distribution, \<-d distribución >**</span><span class="sxs-lookup"><span data-stu-id="f9e58-115">**--distribution, -d \<Distro>**</span></span>

  <span data-ttu-id="f9e58-116">Ejecutar la distribución especificada.</span><span class="sxs-lookup"><span data-stu-id="f9e58-116">Run the specified distribution.</span></span>

* <span data-ttu-id="f9e58-117">**--usuario,-u \<nombre de usuario >**</span><span class="sxs-lookup"><span data-stu-id="f9e58-117">**--user, -u \<UserName>**</span></span>

  <span data-ttu-id="f9e58-118">Ejecutar como el usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="f9e58-118">Run as the specified user.</span></span>

### <a name="arguments-for-managing-windows-subsystem-for-linux"></a><span data-ttu-id="f9e58-119">Argumentos para administrar el subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="f9e58-119">Arguments for managing Windows Subsystem for Linux</span></span>

* <span data-ttu-id="f9e58-120">**--export \<distribución > \<nombre de archivo >**</span><span class="sxs-lookup"><span data-stu-id="f9e58-120">**--export \<Distro> \<FileName>**</span></span>
  
  <span data-ttu-id="f9e58-121">Exporta la distribución a un archivo tar.</span><span class="sxs-lookup"><span data-stu-id="f9e58-121">Exports the distribution to a tar file.</span></span> <span data-ttu-id="f9e58-122">El nombre de archivo puede ser-para la salida estándar.</span><span class="sxs-lookup"><span data-stu-id="f9e58-122">The filename can be - for standard output.</span></span>

* <span data-ttu-id="f9e58-123">**--Import \<distribución > \<installLocation > \<nombreDeArchivo >**</span><span class="sxs-lookup"><span data-stu-id="f9e58-123">**--import \<Distro> \<InstallLocation> \<FileName>**</span></span>
  
  <span data-ttu-id="f9e58-124">Importa el archivo tar especificado como una nueva distribución.</span><span class="sxs-lookup"><span data-stu-id="f9e58-124">Imports the specified tar file as a new distribution.</span></span> <span data-ttu-id="f9e58-125">El nombre de archivo puede ser-para la entrada estándar.</span><span class="sxs-lookup"><span data-stu-id="f9e58-125">The filename can be - for standard input.</span></span>

* <span data-ttu-id="f9e58-126">**--List,-l [opciones]**</span><span class="sxs-lookup"><span data-stu-id="f9e58-126">**--list, -l [Options]**</span></span>
  
  <span data-ttu-id="f9e58-127">Muestra las distribuciones.</span><span class="sxs-lookup"><span data-stu-id="f9e58-127">Lists distributions.</span></span>

  <span data-ttu-id="f9e58-128">Opciones:</span><span class="sxs-lookup"><span data-stu-id="f9e58-128">Options:</span></span>
  * <span data-ttu-id="f9e58-129">**--todos**</span><span class="sxs-lookup"><span data-stu-id="f9e58-129">**--all**</span></span>
      
    <span data-ttu-id="f9e58-130">Enumerar todas las distribuciones, incluidas las distribuciones que se están instalando o desinstalando actualmente.</span><span class="sxs-lookup"><span data-stu-id="f9e58-130">List all distributions, including distributions that are currently being installed or uninstalled.</span></span>

  * <span data-ttu-id="f9e58-131">**--en ejecución**</span><span class="sxs-lookup"><span data-stu-id="f9e58-131">**--running**</span></span>
      
    <span data-ttu-id="f9e58-132">Muestra solo las distribuciones que se están ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="f9e58-132">List only distributions that are currently running.</span></span>

* <span data-ttu-id="f9e58-133">**--set-default,-s \<distribución >**</span><span class="sxs-lookup"><span data-stu-id="f9e58-133">**--set-default, -s \<Distro>**</span></span>
  
  <span data-ttu-id="f9e58-134">Establece la distribución como valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f9e58-134">Sets the distribution as the default.</span></span>

* <span data-ttu-id="f9e58-135">**--Terminate,- \<t distribución >**</span><span class="sxs-lookup"><span data-stu-id="f9e58-135">**--terminate, -t \<Distro>**</span></span>
  
  <span data-ttu-id="f9e58-136">Finaliza la distribución especificada.</span><span class="sxs-lookup"><span data-stu-id="f9e58-136">Terminates the specified distribution.</span></span>

* <span data-ttu-id="f9e58-137">**--anular \<el registro de distribución >**</span><span class="sxs-lookup"><span data-stu-id="f9e58-137">**--unregister \<Distro>**</span></span>
  
  <span data-ttu-id="f9e58-138">Anula el registro de la distribución.</span><span class="sxs-lookup"><span data-stu-id="f9e58-138">Unregisters the distribution.</span></span>
   
* <span data-ttu-id="f9e58-139">**--Help** Mostrar información de uso.</span><span class="sxs-lookup"><span data-stu-id="f9e58-139">**--help** Display usage information.</span></span>

## <a name="additional-commands"></a><span data-ttu-id="f9e58-140">Comandos adicionales</span><span class="sxs-lookup"><span data-stu-id="f9e58-140">Additional Commands</span></span>

<span data-ttu-id="f9e58-141">También hay comandos históricos para interactuar con el subsistema de Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="f9e58-141">There are also historic commands to interact with the Windows Subsystem for Linux.</span></span> <span data-ttu-id="f9e58-142">Su funcionalidad se incluye en `wsl.exe`, pero siguen estando disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="f9e58-142">Their functionality is encompassed within `wsl.exe`, but they are still available for use.</span></span> 

### `wslconfig.exe`

<span data-ttu-id="f9e58-143">Este comando le permite configurar la distribución de WSL.</span><span class="sxs-lookup"><span data-stu-id="f9e58-143">This command lets you configure your WSL distribution.</span></span> <span data-ttu-id="f9e58-144">A continuación se muestra una lista de sus opciones.</span><span class="sxs-lookup"><span data-stu-id="f9e58-144">Below is a list of its options.</span></span>

<span data-ttu-id="f9e58-145">Utilizan`wslconfig [Argument] [Options...]`</span><span class="sxs-lookup"><span data-stu-id="f9e58-145">Using: `wslconfig [Argument] [Options...]`</span></span>

#### <a name="arguments"></a><span data-ttu-id="f9e58-146">Argumentos</span><span class="sxs-lookup"><span data-stu-id="f9e58-146">Arguments</span></span>
* <span data-ttu-id="f9e58-147">**/l,/list [opciones]**</span><span class="sxs-lookup"><span data-stu-id="f9e58-147">**/l, /list [Options]**</span></span>
  
  <span data-ttu-id="f9e58-148">Muestra las distribuciones registradas.</span><span class="sxs-lookup"><span data-stu-id="f9e58-148">Lists registered distributions.</span></span>
  
  <span data-ttu-id="f9e58-149">Opciones:</span><span class="sxs-lookup"><span data-stu-id="f9e58-149">Options:</span></span>
    * <span data-ttu-id="f9e58-150">**/All**</span><span class="sxs-lookup"><span data-stu-id="f9e58-150">**/all**</span></span>
    
      <span data-ttu-id="f9e58-151">Opcionalmente, puede enumerar todas las distribuciones, incluidas las distribuciones que se están instalando o desinstalando.</span><span class="sxs-lookup"><span data-stu-id="f9e58-151">Optionally list all distributions, including distributions that are currently being installed or uninstalled.</span></span>

    * <span data-ttu-id="f9e58-152">**/running**</span><span class="sxs-lookup"><span data-stu-id="f9e58-152">**/running**</span></span>
      
      <span data-ttu-id="f9e58-153">Muestra solo las distribuciones que se están ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="f9e58-153">List only distributions that are currently running.</span></span>

* <span data-ttu-id="f9e58-154">**/s,/setDefault \<distribución >**</span><span class="sxs-lookup"><span data-stu-id="f9e58-154">**/s, /setdefault \<Distro>**</span></span>
  
  <span data-ttu-id="f9e58-155">Establece la distribución como valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f9e58-155">Sets the distribution as the default.</span></span>

* <span data-ttu-id="f9e58-156">**/t,/Terminate. \<distribución >**</span><span class="sxs-lookup"><span data-stu-id="f9e58-156">**/t, /terminate \<Distro>**</span></span>
  
  <span data-ttu-id="f9e58-157">Finaliza la distribución.</span><span class="sxs-lookup"><span data-stu-id="f9e58-157">Terminates the distribution.</span></span>

* <span data-ttu-id="f9e58-158">**/u,/unregister \<distribución >**</span><span class="sxs-lookup"><span data-stu-id="f9e58-158">**/u, /unregister \<Distro>**</span></span>
  
  <span data-ttu-id="f9e58-159">Anula el registro de la distribución.</span><span class="sxs-lookup"><span data-stu-id="f9e58-159">Unregisters the distribution.</span></span>
   
* <span data-ttu-id="f9e58-160">**/Upgrade \<distribución >**</span><span class="sxs-lookup"><span data-stu-id="f9e58-160">**/upgrade \<Distro>**</span></span>
  
  <span data-ttu-id="f9e58-161">Actualiza la distribución al formato del sistema de archivos WslFs.</span><span class="sxs-lookup"><span data-stu-id="f9e58-161">Upgrades the distribution to the WslFs file system format.</span></span>

### `bash.exe`

<span data-ttu-id="f9e58-162">Este comando se usa para iniciar un shell de Bash.</span><span class="sxs-lookup"><span data-stu-id="f9e58-162">This command is used to start a bash shell.</span></span> <span data-ttu-id="f9e58-163">A continuación se muestran las opciones que puede usar con este comando.</span><span class="sxs-lookup"><span data-stu-id="f9e58-163">Below are the options you can use with this command.</span></span>

<span data-ttu-id="f9e58-164">Utilizan`bash [Options...]`</span><span class="sxs-lookup"><span data-stu-id="f9e58-164">Using: `bash [Options...]`</span></span>

* <span data-ttu-id="f9e58-165">**No se ha especificado ninguna opción**</span><span class="sxs-lookup"><span data-stu-id="f9e58-165">**No Option given**</span></span>
  
  <span data-ttu-id="f9e58-166">Inicia el shell de bash en el directorio actual.</span><span class="sxs-lookup"><span data-stu-id="f9e58-166">Launches the Bash shell in the current directory.</span></span> <span data-ttu-id="f9e58-167">Si el shell de Bash no se instala automáticamente, se ejecuta`lxrun /install`</span><span class="sxs-lookup"><span data-stu-id="f9e58-167">If the Bash shell is not installed automatically runs `lxrun /install`</span></span>

* **~**
  
  <span data-ttu-id="f9e58-168">`bash ~`inicia el shell de bash en el directorio principal del usuario.</span><span class="sxs-lookup"><span data-stu-id="f9e58-168">`bash ~` launches the bash shell into the user's home directory.</span></span>  <span data-ttu-id="f9e58-169">Similar a Running `cd ~`.</span><span class="sxs-lookup"><span data-stu-id="f9e58-169">Similar to running `cd ~`.</span></span>

* <span data-ttu-id="f9e58-170">**-c "\<> de comandos"**</span><span class="sxs-lookup"><span data-stu-id="f9e58-170">**-c "\<command>"**</span></span>
  
  <span data-ttu-id="f9e58-171">Ejecuta el comando, imprime la salida y vuelve a salir del símbolo del sistema de Windows.</span><span class="sxs-lookup"><span data-stu-id="f9e58-171">Runs the command, prints the output and exits back to the Windows command prompt.</span></span>
    
  <span data-ttu-id="f9e58-172">Ejemplo: `bash -c "ls"`.</span><span class="sxs-lookup"><span data-stu-id="f9e58-172">Example:  `bash -c "ls"`.</span></span>

## <a name="deprecated-commands"></a><span data-ttu-id="f9e58-173">Comandos desusados</span><span class="sxs-lookup"><span data-stu-id="f9e58-173">Deprecated Commands</span></span>

<span data-ttu-id="f9e58-174">`lxrun.exe` Fue el primer comando que se usaba para instalar y administrar el subsistema de Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="f9e58-174">The `lxrun.exe` was the first command used to install and manage the Windows Subsystem for Linux.</span></span> <span data-ttu-id="f9e58-175">Está en desuso a partir de Windows 10 1803 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="f9e58-175">It is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="f9e58-176">El comando `lxrun.exe` se puede usar para interactuar directamente con el subsistema [de Windows para Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) .</span><span class="sxs-lookup"><span data-stu-id="f9e58-176">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="f9e58-177">Estos comandos se instalan en `\Windows\System32` el directorio y se pueden ejecutar en un símbolo del sistema de Windows o en PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f9e58-177">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

| <span data-ttu-id="f9e58-178">Comando</span><span class="sxs-lookup"><span data-stu-id="f9e58-178">Command</span></span>                     | <span data-ttu-id="f9e58-179">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9e58-179">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="f9e58-180">El comando lxrun se usa para administrar la instancia de WSL.</span><span class="sxs-lookup"><span data-stu-id="f9e58-180">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="f9e58-181">Inicia el proceso de descarga e instalación.</span><span class="sxs-lookup"><span data-stu-id="f9e58-181">Starts the download and install process.</span></span> <br/> <span data-ttu-id="f9e58-182">se puede agregar **/y** para omitir todos los mensajes.</span><span class="sxs-lookup"><span data-stu-id="f9e58-182">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="f9e58-183">El mensaje de confirmación se acepta automáticamente y el usuario predeterminado se establece en root.</span><span class="sxs-lookup"><span data-stu-id="f9e58-183">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="f9e58-184">Desinstala y elimina la imagen de Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="f9e58-184">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="f9e58-185">De forma predeterminada, no se quita el directorio de inicio de Ubuntu del usuario.</span><span class="sxs-lookup"><span data-stu-id="f9e58-185">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="f9e58-186">se puede agregar **/y** para aceptar automáticamente el mensaje de confirmación.</span><span class="sxs-lookup"><span data-stu-id="f9e58-186">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="f9e58-187">**/Full** desinstala y elimina el directorio principal de Ubuntu del usuario.</span><span class="sxs-lookup"><span data-stu-id="f9e58-187">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="f9e58-188">Establece el valor predeterminado de bash en el usuario de Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="f9e58-188">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="f9e58-189">Solicitará una contraseña si el usuario especificado no existe.</span><span class="sxs-lookup"><span data-stu-id="f9e58-189">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="f9e58-190">Para obtener más información, https://aka.ms/wslusers visite:.</span><span class="sxs-lookup"><span data-stu-id="f9e58-190">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="f9e58-191">**/y** Omite promping para la contraseña.</span><span class="sxs-lookup"><span data-stu-id="f9e58-191">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="f9e58-192">El usuario se creará sin una contraseña.</span><span class="sxs-lookup"><span data-stu-id="f9e58-192">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="f9e58-193">Actualiza el índice de paquetes del subsistema.</span><span class="sxs-lookup"><span data-stu-id="f9e58-193">Updates the subsystem's package index</span></span>          |
