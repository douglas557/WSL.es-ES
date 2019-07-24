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
ms.openlocfilehash: 465f55f8ba210cd366adc66d433f1873e295136f
ms.sourcegitcommit: ead64b13501d6cb7170adafbb5624f4984a0af16
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/21/2019
ms.locfileid: "67307656"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="85793-104">Referencia de comandos para el subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="85793-104">Command Reference for Windows Subsystem for Linux</span></span>

<span data-ttu-id="85793-105">La mejor manera de interactuar con el subsistema de Windows para Linux es usar el `wsl.exe` comando.</span><span class="sxs-lookup"><span data-stu-id="85793-105">The best way to interact with the Windows Subsystem for Linux is to use the `wsl.exe` command.</span></span> 

## `wsl.exe` 

<span data-ttu-id="85793-106">A continuación se muestra una lista con todas las `wsl.exe` opciones cuando se usa a partir de la versión 1903 de Windows.</span><span class="sxs-lookup"><span data-stu-id="85793-106">Below is a list containing all options when using `wsl.exe` as of Windows Version 1903.</span></span>

* <span data-ttu-id="85793-107">Argumentos para la ejecución de archivos binarios de Linux:</span><span class="sxs-lookup"><span data-stu-id="85793-107">Arguments for running Linux binaries:</span></span>

    * <span data-ttu-id="85793-108">Si no se proporciona ninguna línea de comandos, WSL. exe inicia el shell predeterminado.</span><span class="sxs-lookup"><span data-stu-id="85793-108">If no command line is provided, wsl.exe launches the default shell.</span></span>

    * <span data-ttu-id="85793-109">--exec,-e<CommandLine></span><span class="sxs-lookup"><span data-stu-id="85793-109">--exec, -e <CommandLine></span></span>
        * <span data-ttu-id="85793-110">Ejecute el comando especificado sin usar el shell de Linux predeterminado.</span><span class="sxs-lookup"><span data-stu-id="85793-110">Execute the specified command without using the default Linux shell.</span></span>

    * --
        * <span data-ttu-id="85793-111">Pase el resto de la línea de comandos tal y como está.</span><span class="sxs-lookup"><span data-stu-id="85793-111">Pass the remaining command line as is.</span></span>

* <span data-ttu-id="85793-112">Opciones:</span><span class="sxs-lookup"><span data-stu-id="85793-112">Options:</span></span>
    * <span data-ttu-id="85793-113">--distribución,-d<Distro></span><span class="sxs-lookup"><span data-stu-id="85793-113">--distribution, -d <Distro></span></span>
        * <span data-ttu-id="85793-114">Ejecutar la distribución especificada.</span><span class="sxs-lookup"><span data-stu-id="85793-114">Run the specified distribution.</span></span>

    * <span data-ttu-id="85793-115">--usuario,-u<UserName></span><span class="sxs-lookup"><span data-stu-id="85793-115">--user, -u <UserName></span></span>
        * <span data-ttu-id="85793-116">Ejecutar como el usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="85793-116">Run as the specified user.</span></span>

* <span data-ttu-id="85793-117">Argumentos para administrar el subsistema de Windows para Linux:</span><span class="sxs-lookup"><span data-stu-id="85793-117">Arguments for managing Windows Subsystem for Linux:</span></span>

    * <span data-ttu-id="85793-118">--exportar <Distro><FileName></span><span class="sxs-lookup"><span data-stu-id="85793-118">--export <Distro> <FileName></span></span>
        * <span data-ttu-id="85793-119">Exporta la distribución a un archivo tar.</span><span class="sxs-lookup"><span data-stu-id="85793-119">Exports the distribution to a tar file.</span></span>
        <span data-ttu-id="85793-120">El nombre de archivo puede ser-para la salida estándar.</span><span class="sxs-lookup"><span data-stu-id="85793-120">The filename can be - for standard output.</span></span>

    * <span data-ttu-id="85793-121">--Import <Distro> <InstallLocation>[opciones <FileName> ]</span><span class="sxs-lookup"><span data-stu-id="85793-121">--import <Distro> <InstallLocation> <FileName> [Options]</span></span>
        * <span data-ttu-id="85793-122">Importa el archivo tar especificado como una nueva distribución.</span><span class="sxs-lookup"><span data-stu-id="85793-122">Imports the specified tar file as a new distribution.</span></span>
        <span data-ttu-id="85793-123">El nombre de archivo puede ser-para la entrada estándar.</span><span class="sxs-lookup"><span data-stu-id="85793-123">The filename can be - for standard input.</span></span>

        * <span data-ttu-id="85793-124">Opciones:</span><span class="sxs-lookup"><span data-stu-id="85793-124">Options:</span></span>
            * <span data-ttu-id="85793-125">--version <Version> especifica la versión que se va a usar para la nueva distribución.</span><span class="sxs-lookup"><span data-stu-id="85793-125">--version <Version> Specifies the version to use for the new distribution.</span></span>

    * <span data-ttu-id="85793-126">--List,-l [opciones]</span><span class="sxs-lookup"><span data-stu-id="85793-126">--list, -l [Options]</span></span>
        * <span data-ttu-id="85793-127">Muestra las distribuciones.</span><span class="sxs-lookup"><span data-stu-id="85793-127">Lists distributions.</span></span>

        * <span data-ttu-id="85793-128">Opciones:</span><span class="sxs-lookup"><span data-stu-id="85793-128">Options:</span></span>
            * <span data-ttu-id="85793-129">--todos</span><span class="sxs-lookup"><span data-stu-id="85793-129">--all</span></span>
                * <span data-ttu-id="85793-130">Enumerar todas las distribuciones, incluidas las distribuciones que se están instalando o desinstalando actualmente.</span><span class="sxs-lookup"><span data-stu-id="85793-130">List all distributions, including distributions that are currently being installed or uninstalled.</span></span>

            * <span data-ttu-id="85793-131">--en ejecución</span><span class="sxs-lookup"><span data-stu-id="85793-131">--running</span></span>
                * <span data-ttu-id="85793-132">Muestra solo las distribuciones que se están ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="85793-132">List only distributions that are currently running.</span></span>

    * <span data-ttu-id="85793-133">--set-default,-s<Distro></span><span class="sxs-lookup"><span data-stu-id="85793-133">--set-default, -s <Distro></span></span>
        * <span data-ttu-id="85793-134">Establece la distribución como valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="85793-134">Sets the distribution as the default.</span></span>

    * <span data-ttu-id="85793-135">--set-default-version<Version></span><span class="sxs-lookup"><span data-stu-id="85793-135">--set-default-version <Version></span></span>
        * <span data-ttu-id="85793-136">Cambia la versión de instalación predeterminada para las nuevas distribuciones.</span><span class="sxs-lookup"><span data-stu-id="85793-136">Changes the default install version for new distributions.</span></span>

    * <span data-ttu-id="85793-137">--Set-version <Distro><Version></span><span class="sxs-lookup"><span data-stu-id="85793-137">--set-version <Distro> <Version></span></span>
        * <span data-ttu-id="85793-138">Cambia la versión de la distribución especificada.</span><span class="sxs-lookup"><span data-stu-id="85793-138">Changes the version of the specified distribution.</span></span>

    * <span data-ttu-id="85793-139">--finalizar,-t<Distro></span><span class="sxs-lookup"><span data-stu-id="85793-139">--terminate, -t <Distro></span></span>
        * <span data-ttu-id="85793-140">Finaliza la distribución especificada.</span><span class="sxs-lookup"><span data-stu-id="85793-140">Terminates the specified distribution.</span></span>

    * <span data-ttu-id="85793-141">--anular registro<Distro></span><span class="sxs-lookup"><span data-stu-id="85793-141">--unregister <Distro></span></span>
        * <span data-ttu-id="85793-142">Anula el registro de la distribución.</span><span class="sxs-lookup"><span data-stu-id="85793-142">Unregisters the distribution.</span></span>

    * <span data-ttu-id="85793-143">--help</span><span class="sxs-lookup"><span data-stu-id="85793-143">--help</span></span>
        * <span data-ttu-id="85793-144">Mostrar información de uso.</span><span class="sxs-lookup"><span data-stu-id="85793-144">Display usage information.</span></span>

## <a name="additional-commands"></a><span data-ttu-id="85793-145">Comandos adicionales</span><span class="sxs-lookup"><span data-stu-id="85793-145">Additional Commands</span></span>

<span data-ttu-id="85793-146">También hay comandos históricos para interactuar con el subsistema de Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="85793-146">There are also historic commands to interact with the Windows Subsystem for Linux.</span></span> <span data-ttu-id="85793-147">Su funcionalidad se incluye en `wsl.exe`, pero siguen estando disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="85793-147">Their functionality is encompassed within `wsl.exe`, but they are still available for use.</span></span> 

### `wslconfig.exe`

<span data-ttu-id="85793-148">Este comando le permite configurar la distribución de WSL.</span><span class="sxs-lookup"><span data-stu-id="85793-148">This command lets you configure your WSL distribution.</span></span> <span data-ttu-id="85793-149">A continuación se muestra una lista de sus opciones.</span><span class="sxs-lookup"><span data-stu-id="85793-149">Below is a list of its options.</span></span>

* <span data-ttu-id="85793-150">/l,/list [opción]</span><span class="sxs-lookup"><span data-stu-id="85793-150">/l, /list [Option]</span></span>
    * <span data-ttu-id="85793-151">Muestra las distribuciones registradas.</span><span class="sxs-lookup"><span data-stu-id="85793-151">Lists registered distributions.</span></span>
        * <span data-ttu-id="85793-152">/All: puede enumerar opcionalmente todas las distribuciones, incluidas las distribuciones que se instalan o desinstalan actualmente.</span><span class="sxs-lookup"><span data-stu-id="85793-152">/all - Optionally list all distributions, including distributions that       are currently being installed or uninstalled.</span></span>

        * <span data-ttu-id="85793-153">/Running: solo muestra las distribuciones que se están ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="85793-153">/running - List only distributions that are currently running.</span></span>

* <span data-ttu-id="85793-154">/s,/setDefault<DistributionName></span><span class="sxs-lookup"><span data-stu-id="85793-154">/s, /setdefault <DistributionName></span></span>
    * <span data-ttu-id="85793-155">Establece la distribución como valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="85793-155">Sets the distribution as the default.</span></span>

* <span data-ttu-id="85793-156">/t,/Terminate.<DistributionName></span><span class="sxs-lookup"><span data-stu-id="85793-156">/t, /terminate <DistributionName></span></span>
    * <span data-ttu-id="85793-157">Finaliza la distribución.</span><span class="sxs-lookup"><span data-stu-id="85793-157">Terminates the distribution.</span></span>

* <span data-ttu-id="85793-158">/u,/unregister<DistributionName></span><span class="sxs-lookup"><span data-stu-id="85793-158">/u, /unregister <DistributionName></span></span>
    * <span data-ttu-id="85793-159">Anula el registro de la distribución.</span><span class="sxs-lookup"><span data-stu-id="85793-159">Unregisters the distribution.</span></span>

### `bash.exe`

<span data-ttu-id="85793-160">Este comando se usa para iniciar un shell de Bash.</span><span class="sxs-lookup"><span data-stu-id="85793-160">This command is used to start a bash shell.</span></span> <span data-ttu-id="85793-161">A continuación se muestran las opciones que puede usar con este comando.</span><span class="sxs-lookup"><span data-stu-id="85793-161">Below are the options you can use with this command.</span></span>

* <span data-ttu-id="85793-162">No se ha especificado ninguna opción</span><span class="sxs-lookup"><span data-stu-id="85793-162">No Option given</span></span>
    * <span data-ttu-id="85793-163">Inicia el shell de bash en el directorio actual.</span><span class="sxs-lookup"><span data-stu-id="85793-163">Launches the Bash shell in the current directory.</span></span> <span data-ttu-id="85793-164">Si el shell de Bash no se instala automáticamente, se ejecuta`lxrun /install`</span><span class="sxs-lookup"><span data-stu-id="85793-164">If the Bash shell is not installed automatically runs `lxrun /install`</span></span>

* <span data-ttu-id="85793-165">Bash ~</span><span class="sxs-lookup"><span data-stu-id="85793-165">bash ~</span></span>
    * <span data-ttu-id="85793-166">Inicia el shell de bash en el directorio principal del usuario.</span><span class="sxs-lookup"><span data-stu-id="85793-166">Launches the bash shell into the user's home directory.</span></span>  <span data-ttu-id="85793-167">Similar a Running `cd ~`.</span><span class="sxs-lookup"><span data-stu-id="85793-167">Similar to running `cd ~`.</span></span>

* <span data-ttu-id="85793-168">Bash-c "&lt;comando&gt;"</span><span class="sxs-lookup"><span data-stu-id="85793-168">bash -c "&lt;command&gt;"</span></span>
    * <span data-ttu-id="85793-169">Ejecuta el comando, imprime la salida y vuelve a salir del símbolo del sistema de Windows.</span><span class="sxs-lookup"><span data-stu-id="85793-169">Runs the command, prints the output and exits back to the Windows command prompt.</span></span> <br/> <br/> <span data-ttu-id="85793-170">Ejemplo`bash -c "ls"`</span><span class="sxs-lookup"><span data-stu-id="85793-170">Example:  `bash -c "ls"`</span></span>

## <a name="deprecated-commands"></a><span data-ttu-id="85793-171">Comandos desusados</span><span class="sxs-lookup"><span data-stu-id="85793-171">Deprecated Commands</span></span>

<span data-ttu-id="85793-172">`lxrun.exe` Fue el primer comando que se usaba para instalar y administrar el subsistema de Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="85793-172">The `lxrun.exe` was the first command used to install and manage the Windows Subsystem for Linux.</span></span> <span data-ttu-id="85793-173">Está en desuso a partir de Windows 10 1803 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="85793-173">It is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="85793-174">El comando `lxrun.exe` se puede usar para interactuar directamente con el subsistema [de Windows para Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) .</span><span class="sxs-lookup"><span data-stu-id="85793-174">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="85793-175">Estos comandos se instalan en `\Windows\System32` el directorio y se pueden ejecutar en un símbolo del sistema de Windows o en PowerShell.</span><span class="sxs-lookup"><span data-stu-id="85793-175">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

| <span data-ttu-id="85793-176">Comando</span><span class="sxs-lookup"><span data-stu-id="85793-176">Command</span></span>                     | <span data-ttu-id="85793-177">Descripción</span><span class="sxs-lookup"><span data-stu-id="85793-177">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="85793-178">El comando lxrun se usa para administrar la instancia de WSL.</span><span class="sxs-lookup"><span data-stu-id="85793-178">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="85793-179">Inicia el proceso de descarga e instalación.</span><span class="sxs-lookup"><span data-stu-id="85793-179">Starts the download and install process.</span></span> <br/> <span data-ttu-id="85793-180">se puede agregar **/y** para omitir todos los mensajes.</span><span class="sxs-lookup"><span data-stu-id="85793-180">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="85793-181">El mensaje de confirmación se acepta automáticamente y el usuario predeterminado se establece en root.</span><span class="sxs-lookup"><span data-stu-id="85793-181">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="85793-182">Desinstala y elimina la imagen de Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="85793-182">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="85793-183">De forma predeterminada, no se quita el directorio de inicio de Ubuntu del usuario.</span><span class="sxs-lookup"><span data-stu-id="85793-183">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="85793-184">se puede agregar **/y** para aceptar automáticamente el mensaje de confirmación.</span><span class="sxs-lookup"><span data-stu-id="85793-184">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="85793-185">**/Full** desinstala y elimina el directorio principal de Ubuntu del usuario.</span><span class="sxs-lookup"><span data-stu-id="85793-185">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="85793-186">Establece el valor predeterminado de bash en el usuario de Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="85793-186">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="85793-187">Solicitará una contraseña si el usuario especificado no existe.</span><span class="sxs-lookup"><span data-stu-id="85793-187">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="85793-188">Para obtener más información, https://aka.ms/wslusers visite:.</span><span class="sxs-lookup"><span data-stu-id="85793-188">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="85793-189">**/y** Omite promping para la contraseña.</span><span class="sxs-lookup"><span data-stu-id="85793-189">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="85793-190">El usuario se creará sin una contraseña.</span><span class="sxs-lookup"><span data-stu-id="85793-190">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="85793-191">Actualiza el índice de paquetes del subsistema.</span><span class="sxs-lookup"><span data-stu-id="85793-191">Updates the subsystem's package index</span></span>          |
