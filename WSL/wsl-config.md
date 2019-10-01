---
title: Administrar distribuciones de Linux
description: Lista de referencia y configuración de varias distribuciones de Linux que se ejecutan en el subsistema de Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, subsistemawindows, ubuntu, wsl.conf, wslconfig
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 51099f21fe44fd8c7e8682332c939fbe6d5e5827
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269870"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a><span data-ttu-id="08507-104">Administrar y configurar el subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="08507-104">Manage and configure Windows Subsystem for Linux</span></span>

> <span data-ttu-id="08507-105">Se aplica a Windows 10 Fall Creators Update y posterior.</span><span class="sxs-lookup"><span data-stu-id="08507-105">Applies to Windows 10 Fall Creators Update and later.</span></span>  <span data-ttu-id="08507-106">Consulta nuestra [guía de instalación](./install_guide.md) actualizada para probar nuevas características de administración y comenzar a ejecutar varias distribuciones de Linux desde Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="08507-106">See our updated [installation guide](./install_guide.md) to try new management features and start running multiple Linux distributions from the Microsoft store.</span></span>

## <a name="ways-to-run-wsl"></a><span data-ttu-id="08507-107">Formas de ejecutar WSL</span><span class="sxs-lookup"><span data-stu-id="08507-107">Ways to run WSL</span></span>

<span data-ttu-id="08507-108">Hay muchas maneras de ejecutar Linux con el subsistema de Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="08507-108">There are many ways to run Linux with the Windows Subsystem for Linux.</span></span>

1. <span data-ttu-id="08507-109">`[distro]`, por ejemplo `ubuntu`</span><span class="sxs-lookup"><span data-stu-id="08507-109">`[distro]`, for example `ubuntu`</span></span>
1. <span data-ttu-id="08507-110">`wsl.exe` o `bash.exe`</span><span class="sxs-lookup"><span data-stu-id="08507-110">`wsl.exe` or `bash.exe`</span></span>
1. <span data-ttu-id="08507-111">`wsl [command]` o `bash -c [command]`</span><span class="sxs-lookup"><span data-stu-id="08507-111">`wsl [command]` or `bash -c [command]`</span></span>

<span data-ttu-id="08507-112">El método que deba usar dependerá de lo que esté haciendo.</span><span class="sxs-lookup"><span data-stu-id="08507-112">Which method you should use depends on what you're doing.</span></span>

### <a name="launch-wsl-by-distribution"></a><span data-ttu-id="08507-113">Iniciar WSL por distribución</span><span class="sxs-lookup"><span data-stu-id="08507-113">Launch WSL by distribution</span></span>

<span data-ttu-id="08507-114">La ejecución de una distribución mediante su aplicación específica de distribución inicia esa distribución en su propia ventana de la consola.</span><span class="sxs-lookup"><span data-stu-id="08507-114">Running a distribution using it's distro-specific application launches that distribution in it's own console window.</span></span>

![Iniciar WSL desde el menú Inicio](media/start-launch.png)

<span data-ttu-id="08507-116">Es lo mismo que hacer clic en "Iniciar" en Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="08507-116">It is the same as clicking "Launch" in the Microsoft store.</span></span>

![Iniciar WSL desde Microsoft Store](media/store-launch.png)

<span data-ttu-id="08507-118">También puedes ejecutar la distribución desde la línea de comandos ejecutando `[distribution].exe`.</span><span class="sxs-lookup"><span data-stu-id="08507-118">You can also run the distribution from the command line by running `[distribution].exe`.</span></span>

<span data-ttu-id="08507-119">El inconveniente de ejecutar una distribución desde la línea de comandos de esta manera es que cambiará automáticamente el directorio de trabajo del directorio actual al directorio principal de la distribución.</span><span class="sxs-lookup"><span data-stu-id="08507-119">The disadvantage of running a distribution from the command line in this way is that it will automatically change your working directory from the current directory to the distribution's home directory.</span></span>

<span data-ttu-id="08507-120">**Ejemplo:**</span><span class="sxs-lookup"><span data-stu-id="08507-120">**Example:**</span></span>

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> ubuntu

scooley@scooley-elmer:~$ pwd
/home/scooley
scooley@scooley-elmer:~$ exit
logout

PS C:\Users\sarah>
```

### <a name="wsl-and-wsl-command"></a><span data-ttu-id="08507-121">wsl y wsl [command]</span><span class="sxs-lookup"><span data-stu-id="08507-121">wsl and wsl [command]</span></span>

<span data-ttu-id="08507-122">La mejor manera de ejecutar WSL desde la línea de comandos es usar `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="08507-122">The best way to run WSL from the command line is using `wsl.exe`.</span></span>

<span data-ttu-id="08507-123">**Ejemplo:**</span><span class="sxs-lookup"><span data-stu-id="08507-123">**Example:**</span></span>

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

<span data-ttu-id="08507-124">`wsl` no solo mantiene el directorio de trabajo actual, sino que te permite ejecutar un único comando junto a los comandos de Windows.</span><span class="sxs-lookup"><span data-stu-id="08507-124">Not only does `wsl` keep the current working directory in place, it lets you run a single command along side Windows commands.</span></span>

<span data-ttu-id="08507-125">**Ejemplo:**</span><span class="sxs-lookup"><span data-stu-id="08507-125">**Example:**</span></span>

```console
PS C:\Users\sarah> Get-Date

Sunday, March 11, 2018 7:54:05 PM

PS C:\Users\sarah> wsl
scooley@scooley-elmer:/mnt/c/Users/sarah$ date
Sun Mar 11 19:56:57 DST 2018
scooley@scooley-elmer:/mnt/c/Users/sarah$ exit
logout

PS C:\Users\sarah> wsl date
Sun Mar 11 19:55:47 DST 2018
```

<span data-ttu-id="08507-126">**Ejemplo:**</span><span class="sxs-lookup"><span data-stu-id="08507-126">**Example:**</span></span>

```console
PS C:\Users\sarah> Get-VM

Name            State CPUUsage(%) MemoryAssigned(M) Uptime   Status
----            ----- ----------- ----------------- ------   ------
Server17093     Off   0           0                 00:00:00 Opera...
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
Windows         Off   0           0                 00:00:00 Opera...


PS C:\Users\sarah> Get-VM | wsl grep "Ubuntu"
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
PS C:\Users\sarah>
```


## <a name="managing-multiple-linux-distributions"></a><span data-ttu-id="08507-127">Administración de varias distribuciones de Linux</span><span class="sxs-lookup"><span data-stu-id="08507-127">Managing multiple Linux Distributions</span></span>

### <a name="windows-10-version-1903-and-later"></a><span data-ttu-id="08507-128">Windows 10, versión 1903 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="08507-128">Windows 10 Version 1903 and later</span></span>

<span data-ttu-id="08507-129">Puedes usar `wsl.exe` para administrar las distribuciones en el subsistema de Windows para Linux (WSL), incluida la enumeración de distribuciones disponibles, la configuración de una distribución predeterminada y la desinstalación de distribuciones.</span><span class="sxs-lookup"><span data-stu-id="08507-129">You can use `wsl.exe` to manage your distributions in the Windows Subsystem for Linux (WSL), including listing available distributions, setting a default distribution, and uninstalling distributions.</span></span>

<span data-ttu-id="08507-130">Cada distribución de Linux administra de forma independiente sus propias configuraciones.</span><span class="sxs-lookup"><span data-stu-id="08507-130">Each Linux distribution independently manages its own configurations.</span></span> <span data-ttu-id="08507-131">Para ver los comandos específicos de la distribución, ejecuta `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="08507-131">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="08507-132">Por ejemplo, `ubuntu /?`.</span><span class="sxs-lookup"><span data-stu-id="08507-132">For example `ubuntu /?`.</span></span>

#### <a name="list-distributions"></a><span data-ttu-id="08507-133">Enumerar distribuciones</span><span class="sxs-lookup"><span data-stu-id="08507-133">List distributions</span></span>

<span data-ttu-id="08507-134">`wsl -l`, `wsl --list`</span><span class="sxs-lookup"><span data-stu-id="08507-134">`wsl -l` , `wsl --list`</span></span>  
<span data-ttu-id="08507-135">Enumera las distribuciones de Linux disponibles para WSL.</span><span class="sxs-lookup"><span data-stu-id="08507-135">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="08507-136">Si se enumera una distribución, está instalada y lista para usar.</span><span class="sxs-lookup"><span data-stu-id="08507-136">If a distribution is listed, it's installed and ready to use.</span></span>

`wsl --list --all`   
<span data-ttu-id="08507-137">Enumera todas las distribuciones, incluidas las que no se pueden usar actualmente.</span><span class="sxs-lookup"><span data-stu-id="08507-137">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="08507-138">Pueden encontrarse en proceso de instalación, desinstalación o tener un estado interrumpido.</span><span class="sxs-lookup"><span data-stu-id="08507-138">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

`wsl --list --running`   
<span data-ttu-id="08507-139">Enumera todas las distribuciones que se están actualmente en ejecución.</span><span class="sxs-lookup"><span data-stu-id="08507-139">Lists all distributions that are currently running.</span></span>

#### <a name="set-a-default-distribution"></a><span data-ttu-id="08507-140">Establecer una distribución predeterminada</span><span class="sxs-lookup"><span data-stu-id="08507-140">Set a default distribution</span></span>

<span data-ttu-id="08507-141">La distribución de WSL predeterminada es la que se ejecuta cuando se ejecuta `wsl` en una línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="08507-141">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

<span data-ttu-id="08507-142">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="08507-142">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span></span>

<span data-ttu-id="08507-143">Establece la distribución predeterminada en `<DistributionName>`.</span><span class="sxs-lookup"><span data-stu-id="08507-143">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="08507-144">**Ejemplo:**</span><span class="sxs-lookup"><span data-stu-id="08507-144">**Example:**</span></span>  
<span data-ttu-id="08507-145">`wsl -s Ubuntu` establecería la distribución predeterminada en Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="08507-145">`wsl -s Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="08507-146">Ahora, al ejecutar `wsl npm init`, se ejecutará en Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="08507-146">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="08507-147">Si se ejecuta `wsl`, se abrirá una sesión de Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="08507-147">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="08507-148">Anular el registro de una distribución y reinstalarla</span><span class="sxs-lookup"><span data-stu-id="08507-148">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="08507-149">Aunque las distribuciones de Linux se pueden instalar a través de Microsoft Store, no se pueden desinstalar a través de Store.</span><span class="sxs-lookup"><span data-stu-id="08507-149">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="08507-150">WSL Config permite anular el registro de las distribuciones o desinstalarlas.</span><span class="sxs-lookup"><span data-stu-id="08507-150">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="08507-151">La anulación del registro también permite volver a instalar las distribuciones.</span><span class="sxs-lookup"><span data-stu-id="08507-151">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="08507-152">**Precaución:** Una vez que se ha anulado el registro, todos los datos, la configuración y el software asociados a esa distribución se perderán de manera permanente.</span><span class="sxs-lookup"><span data-stu-id="08507-152">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="08507-153">Si se vuelve a instalar desde Store, se instalará una copia limpia de la distribución.</span><span class="sxs-lookup"><span data-stu-id="08507-153">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wsl --unregister <DistributionName>`  
<span data-ttu-id="08507-154">Anula el registro de la distribución de WSL para que se pueda volver a instalar o limpiar.</span><span class="sxs-lookup"><span data-stu-id="08507-154">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="08507-155">Por ejemplo: `wsl --unregister Ubuntu` quitaría Ubuntu de las distribuciones disponibles en WSL.</span><span class="sxs-lookup"><span data-stu-id="08507-155">For example: `wsl --unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="08507-156">Al ejecutar `wsl --list`, no aparecerá en la lista.</span><span class="sxs-lookup"><span data-stu-id="08507-156">When I run `wsl --list` it will not be listed.</span></span>

<span data-ttu-id="08507-157">Para reinstalar, busque la distribución en Microsoft Store y seleccione "Iniciar".</span><span class="sxs-lookup"><span data-stu-id="08507-157">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

#### <a name="run-as-a-specific-user"></a><span data-ttu-id="08507-158">Ejecutar como usuario específico</span><span class="sxs-lookup"><span data-stu-id="08507-158">Run as a specific user</span></span>

<span data-ttu-id="08507-159">`wsl -u <Username>`, `wsl --user <Username>`</span><span class="sxs-lookup"><span data-stu-id="08507-159">`wsl -u <Username>`, `wsl --user <Username>`</span></span>

<span data-ttu-id="08507-160">Ejecuta WSL como el usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="08507-160">Run WSL as the specified user.</span></span> <span data-ttu-id="08507-161">Ten en cuenta que el usuario debe existir dentro de la distribución de WSL.</span><span class="sxs-lookup"><span data-stu-id="08507-161">Please note that user must exist inside of the WSL distribution.</span></span>

#### <a name="run-a-specific-distribution"></a><span data-ttu-id="08507-162">Ejecutar una distribución específica</span><span class="sxs-lookup"><span data-stu-id="08507-162">Run a specific distribution</span></span>

<span data-ttu-id="08507-163">`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="08507-163">`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`</span></span>

<span data-ttu-id="08507-164">Ejecuta una distribución especificada de WSL, se puede usar para enviar comandos a una distribución específica sin tener que cambiar la predeterminada.</span><span class="sxs-lookup"><span data-stu-id="08507-164">Run a specified distribution of WSL, can be used to send commands to a specific distribution without having to change your default.</span></span>

### <a name="versions-earlier-than-windows-10-version-1903"></a><span data-ttu-id="08507-165">Versiones anteriores a Windows 10, versión 1903</span><span class="sxs-lookup"><span data-stu-id="08507-165">Versions Earlier than Windows 10 Version 1903</span></span>

<span data-ttu-id="08507-166">WSL Config (`wslconfig.exe`) es una herramienta de línea de comandos para administrar las distribuciones de Linux que se ejecutan en el subsistema de Windows para Linux (WSL).</span><span class="sxs-lookup"><span data-stu-id="08507-166">WSL Config (`wslconfig.exe`) is a command-line tool for managing Linux distributions running on the Windows Subsystem for Linux (WSL).</span></span>  <span data-ttu-id="08507-167">Te permite enumerar las distribuciones disponibles, establecer una distribución predeterminada y desinstalar las distribuciones.</span><span class="sxs-lookup"><span data-stu-id="08507-167">It lets you list available distributions, set a default distribution, and uninstall distributions.</span></span>

<span data-ttu-id="08507-168">Si bien WSL Config es útil para las configuraciones que abarcan o coordinan las distribuciones, cada distribución de Linux administra de forma independiente sus propias configuraciones.</span><span class="sxs-lookup"><span data-stu-id="08507-168">While WSL Config is helpful for settings that span or coordinate distributions, each Linux distribution independently manages its own configurations.</span></span>  <span data-ttu-id="08507-169">Para ver los comandos específicos de la distribución, ejecuta `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="08507-169">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="08507-170">Por ejemplo, `ubuntu /?`.</span><span class="sxs-lookup"><span data-stu-id="08507-170">For example `ubuntu /?`.</span></span>

<span data-ttu-id="08507-171">Para ver todas las opciones disponibles para wslconfig, ejecuta: `wslconfig /?`</span><span class="sxs-lookup"><span data-stu-id="08507-171">To see all available options for wslconfig, run:  `wslconfig /?`</span></span>

```console
wslconfig.exe
Performs administrative operations on Windows Subsystem for Linux

Usage:
    /l, /list [/all] - Lists registered distributions.
        /all - Optionally list all distributions, including distributions that
               are currently being installed or uninstalled.
    /s, /setdefault <DistributionName> - Sets the specified distribution as the default.
    /u, /unregister <DistributionName> - Unregisters a distribution.
```

#### <a name="list-distributions"></a><span data-ttu-id="08507-172">Enumerar distribuciones</span><span class="sxs-lookup"><span data-stu-id="08507-172">List distributions</span></span>

`wslconfig /list`  
<span data-ttu-id="08507-173">Enumera las distribuciones de Linux disponibles para WSL.</span><span class="sxs-lookup"><span data-stu-id="08507-173">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="08507-174">Si se enumera una distribución, está instalada y lista para usar.</span><span class="sxs-lookup"><span data-stu-id="08507-174">If a distribution is listed, it's installed and ready to use.</span></span>

`wslconfig /list /all`  
<span data-ttu-id="08507-175">Enumera todas las distribuciones, incluidas las que no se pueden usar actualmente.</span><span class="sxs-lookup"><span data-stu-id="08507-175">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="08507-176">Pueden encontrarse en proceso de instalación, desinstalación o tener un estado interrumpido.</span><span class="sxs-lookup"><span data-stu-id="08507-176">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

#### <a name="set-a-default-distribution"></a><span data-ttu-id="08507-177">Establecer una distribución predeterminada</span><span class="sxs-lookup"><span data-stu-id="08507-177">Set a default distribution</span></span>

<span data-ttu-id="08507-178">La distribución de WSL predeterminada es la que se ejecuta cuando se ejecuta `wsl` en una línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="08507-178">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

`wslconfig /setdefault <DistributionName>`

<span data-ttu-id="08507-179">Establece la distribución predeterminada en `<DistributionName>`.</span><span class="sxs-lookup"><span data-stu-id="08507-179">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="08507-180">**Ejemplo:**</span><span class="sxs-lookup"><span data-stu-id="08507-180">**Example:**</span></span>  
<span data-ttu-id="08507-181">`wslconfig /setdefault Ubuntu` establecería la distribución predeterminada en Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="08507-181">`wslconfig /setdefault Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="08507-182">Ahora, al ejecutar `wsl npm init`, se ejecutará en Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="08507-182">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="08507-183">Si se ejecuta `wsl`, se abrirá una sesión de Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="08507-183">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="08507-184">Anular el registro de una distribución y reinstalarla</span><span class="sxs-lookup"><span data-stu-id="08507-184">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="08507-185">Aunque las distribuciones de Linux se pueden instalar a través de Microsoft Store, no se pueden desinstalar a través de Store.</span><span class="sxs-lookup"><span data-stu-id="08507-185">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="08507-186">WSL Config permite anular el registro de las distribuciones o desinstalarlas.</span><span class="sxs-lookup"><span data-stu-id="08507-186">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="08507-187">La anulación del registro también permite volver a instalar las distribuciones.</span><span class="sxs-lookup"><span data-stu-id="08507-187">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="08507-188">**Precaución:** Una vez que se ha anulado el registro, todos los datos, la configuración y el software asociados a esa distribución se perderán de manera permanente.</span><span class="sxs-lookup"><span data-stu-id="08507-188">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="08507-189">Si se vuelve a instalar desde Store, se instalará una copia limpia de la distribución.</span><span class="sxs-lookup"><span data-stu-id="08507-189">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wslconfig /unregister <DistributionName>`  
<span data-ttu-id="08507-190">Anula el registro de la distribución de WSL para que se pueda volver a instalar o limpiar.</span><span class="sxs-lookup"><span data-stu-id="08507-190">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="08507-191">Por ejemplo: `wslconfig /unregister Ubuntu` quitaría Ubuntu de las distribuciones disponibles en WSL.</span><span class="sxs-lookup"><span data-stu-id="08507-191">For example: `wslconfig /unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="08507-192">Al ejecutar `wslconfig /list`, no aparecerá en la lista.</span><span class="sxs-lookup"><span data-stu-id="08507-192">When I run `wslconfig /list` it will not be listed.</span></span>

<span data-ttu-id="08507-193">Para reinstalar, busque la distribución en Microsoft Store y seleccione "Iniciar".</span><span class="sxs-lookup"><span data-stu-id="08507-193">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

## <a name="set-wsl-launch-settings"></a><span data-ttu-id="08507-194">Establecer la configuración de inicio de WSL</span><span class="sxs-lookup"><span data-stu-id="08507-194">Set WSL launch settings</span></span>

> <span data-ttu-id="08507-195">**Disponible en la compilación 17093 de Windows Insider y versiones posteriores**</span><span class="sxs-lookup"><span data-stu-id="08507-195">**Available in Windows Insider Build 17093 and later**</span></span>

<span data-ttu-id="08507-196">Configura automáticamente cierta funcionalidad en WSL que se aplicará cada vez que inicies el subsistema mediante `wsl.conf`.</span><span class="sxs-lookup"><span data-stu-id="08507-196">Automatically configure certain functionality in WSL that will be applied every time you launch the subsystem using `wsl.conf`.</span></span> 

<span data-ttu-id="08507-197">En este momento, esto incluye opciones de montaje automático y configuración de red.</span><span class="sxs-lookup"><span data-stu-id="08507-197">Right now, this includes automount options and network configuration.</span></span>

<span data-ttu-id="08507-198">`wsl.conf` se encuentra en cada distribución de Linux en `/etc/wsl.conf`.</span><span class="sxs-lookup"><span data-stu-id="08507-198">`wsl.conf` is located in each Linux distribution in `/etc/wsl.conf`.</span></span> <span data-ttu-id="08507-199">Si el archivo no está allí, puedes crearlo tú mismo.</span><span class="sxs-lookup"><span data-stu-id="08507-199">If the file is not there, you can create it yourself.</span></span> <span data-ttu-id="08507-200">WSL detectará la existencia del archivo y leerá su contenido.</span><span class="sxs-lookup"><span data-stu-id="08507-200">WSL will detect the existence of the file and will read its contents.</span></span> <span data-ttu-id="08507-201">Si falta el archivo o tiene un formato incorrecto (es decir, un formato de marcado incorrecto), WSL se iniciará de manera normal.</span><span class="sxs-lookup"><span data-stu-id="08507-201">If the file is missing or malformed (that is, improper markup formatting), WSL will continue to launch as normal.</span></span>

<span data-ttu-id="08507-202">A continuación se muestra un archivo `wsl.conf` de ejemplo que puedes agregar a tus distribuciones:</span><span class="sxs-lookup"><span data-stu-id="08507-202">Here is a sample `wsl.conf` file you could add into your distros:</span></span>

```console
# Enable extra metadata options by default
[automount]
enabled = true
root = /windir/
options = "metadata,umask=22,fmask=11"
mountFsTab = false

# Enable DNS – even though these are turned on by default, we’ll specify here just to be explicit.
[network]
generateHosts = true
generateResolvConf = true
```

### <a name="configuration-options"></a><span data-ttu-id="08507-203">Opciones de configuración</span><span class="sxs-lookup"><span data-stu-id="08507-203">Configuration Options</span></span>

<span data-ttu-id="08507-204">En concordancia con las convenciones de .ini, las claves se declaran en una sección.</span><span class="sxs-lookup"><span data-stu-id="08507-204">In keeping with .ini conventions, keys are declared under a section.</span></span> 

<span data-ttu-id="08507-205">WSL admite dos secciones: `automount` y `network`.</span><span class="sxs-lookup"><span data-stu-id="08507-205">WSL supports two sections: `automount` and `network`.</span></span>

#### <a name="automount"></a><span data-ttu-id="08507-206">automount</span><span class="sxs-lookup"><span data-stu-id="08507-206">automount</span></span>

<span data-ttu-id="08507-207">Sección: `[automount]`</span><span class="sxs-lookup"><span data-stu-id="08507-207">Section: `[automount]`</span></span>


| <span data-ttu-id="08507-208">key</span><span class="sxs-lookup"><span data-stu-id="08507-208">key</span></span>        | <span data-ttu-id="08507-209">value</span><span class="sxs-lookup"><span data-stu-id="08507-209">value</span></span>                          | <span data-ttu-id="08507-210">valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="08507-210">default</span></span>      | <span data-ttu-id="08507-211">notas</span><span class="sxs-lookup"><span data-stu-id="08507-211">notes</span></span>                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08507-212">enabled</span><span class="sxs-lookup"><span data-stu-id="08507-212">enabled</span></span>    | <span data-ttu-id="08507-213">boolean</span><span class="sxs-lookup"><span data-stu-id="08507-213">boolean</span></span>                        | <span data-ttu-id="08507-214">true</span><span class="sxs-lookup"><span data-stu-id="08507-214">true</span></span>         | <span data-ttu-id="08507-215">`true` hace que las unidades fijas (es decir,</span><span class="sxs-lookup"><span data-stu-id="08507-215">`true` causes fixed drives (i.e</span></span> <span data-ttu-id="08507-216">`C:/` o `D:/`) se monten automáticamente con DrvFs en `/mnt`.</span><span class="sxs-lookup"><span data-stu-id="08507-216">`C:/` or `D:/`) to be automatically mounted with DrvFs under `/mnt`.</span></span>  <span data-ttu-id="08507-217">`false` significa que las unidades no se montarán automáticamente, pero podrías montarlas de forma manual o a través de `fstab`.</span><span class="sxs-lookup"><span data-stu-id="08507-217">`false` means drives won’t be mounted automatically, but you could still mount them manually or via `fstab`.</span></span>                                                                                                             |
| <span data-ttu-id="08507-218">mountFsTab</span><span class="sxs-lookup"><span data-stu-id="08507-218">mountFsTab</span></span> | <span data-ttu-id="08507-219">boolean</span><span class="sxs-lookup"><span data-stu-id="08507-219">boolean</span></span>                        | <span data-ttu-id="08507-220">true</span><span class="sxs-lookup"><span data-stu-id="08507-220">true</span></span>         | <span data-ttu-id="08507-221">`true` establece `/etc/fstab` para que se procese en el inicio de WSL.</span><span class="sxs-lookup"><span data-stu-id="08507-221">`true` sets `/etc/fstab` to be processed on WSL start.</span></span> <span data-ttu-id="08507-222">/etc/fstab es un archivo donde puedes declarar otros sistemas de archivos, como un recurso compartido de SMB.</span><span class="sxs-lookup"><span data-stu-id="08507-222">/etc/fstab is a file where you can declare other filesystems, like an SMB share.</span></span> <span data-ttu-id="08507-223">Por lo tanto, puedes montar estos sistemas de archivos automáticamente en WSL en el inicio.</span><span class="sxs-lookup"><span data-stu-id="08507-223">Thus, you can mount these filesystems automatically in WSL on start up.</span></span>                                                                                                                |
| <span data-ttu-id="08507-224">root</span><span class="sxs-lookup"><span data-stu-id="08507-224">root</span></span>       | <span data-ttu-id="08507-225">Cadena</span><span class="sxs-lookup"><span data-stu-id="08507-225">String</span></span>                         | `/mnt/`      | <span data-ttu-id="08507-226">Establece el directorio donde se montarán automáticamente las unidades fijas.</span><span class="sxs-lookup"><span data-stu-id="08507-226">Sets the directory where fixed drives will be automatically mounted.</span></span> <span data-ttu-id="08507-227">Por ejemplo, si tienes un directorio en WSL en `/windir/` y lo especificas como raíz, esperarías ver que las unidades fijas se monten en `/windir/c`</span><span class="sxs-lookup"><span data-stu-id="08507-227">For example, if you have a directory in WSL at `/windir/` and you specify that as the root, you would expect to see your fixed drives mounted at `/windir/c`</span></span>                                                                                              |
| <span data-ttu-id="08507-228">opciones</span><span class="sxs-lookup"><span data-stu-id="08507-228">options</span></span>    | <span data-ttu-id="08507-229">lista de valores separados por comas</span><span class="sxs-lookup"><span data-stu-id="08507-229">comma-separated list of values</span></span> | <span data-ttu-id="08507-230">cadena vacía</span><span class="sxs-lookup"><span data-stu-id="08507-230">empty string</span></span> | <span data-ttu-id="08507-231">Este valor se anexa a la cadena predeterminada de opciones de montaje de DrvFs.</span><span class="sxs-lookup"><span data-stu-id="08507-231">This value is appended to the default DrvFs mount options string.</span></span> <span data-ttu-id="08507-232">**Solo se pueden especificar opciones específicas de DrvFs.**</span><span class="sxs-lookup"><span data-stu-id="08507-232">**Only DrvFs-specific options can be specified.**</span></span> <span data-ttu-id="08507-233">No se admiten las opciones que el binario de montaje analizaría normalmente en una marca.</span><span class="sxs-lookup"><span data-stu-id="08507-233">Options that the mount binary would normally parse into a flag are not supported.</span></span> <span data-ttu-id="08507-234">Si quieres especificar explícitamente esas opciones, tienes que incluir en /etc/fstab cada unidad para la que quieras hacerlo.</span><span class="sxs-lookup"><span data-stu-id="08507-234">If you want to explicitly specify those options, you must include every drive for which you want to do so in /etc/fstab.</span></span> |

<span data-ttu-id="08507-235">De manera predeterminada, WSL establece uid y gid en el valor del usuario predeterminado (en una distribución de Ubuntu, el usuario predeterminado se crea con uid=1000,gid=1000).</span><span class="sxs-lookup"><span data-stu-id="08507-235">By default, WSL sets the uid and gid to the value of the default user (in Ubuntu distro, the default user is created with uid=1000,gid=1000).</span></span> <span data-ttu-id="08507-236">Si el usuario especifica una opción gid o uid explícitamente a través de esta clave, se sobrescribirá el valor asociado.</span><span class="sxs-lookup"><span data-stu-id="08507-236">If the user specifies a gid or uid option explicitly via this key, the associated value will be overwritten.</span></span> <span data-ttu-id="08507-237">De lo contrario, siempre se anexará el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="08507-237">Otherwise, the default value will always be appended.</span></span>

<span data-ttu-id="08507-238">**Nota:** Estas opciones se aplican como opciones de montaje para todas las unidades montadas automáticamente.</span><span class="sxs-lookup"><span data-stu-id="08507-238">**Note:** These options are applied as the mount options for all automatically mounted drives.</span></span> <span data-ttu-id="08507-239">Para cambiar las opciones solo para una unidad específica, usa /etc/fstab en su lugar.</span><span class="sxs-lookup"><span data-stu-id="08507-239">To change the options for a specific drive only, use /etc/fstab instead.</span></span>

#### <a name="network"></a><span data-ttu-id="08507-240">red</span><span class="sxs-lookup"><span data-stu-id="08507-240">network</span></span>

<span data-ttu-id="08507-241">Etiqueta de la sección: `[network]`</span><span class="sxs-lookup"><span data-stu-id="08507-241">Section label: `[network]`</span></span>

| <span data-ttu-id="08507-242">key</span><span class="sxs-lookup"><span data-stu-id="08507-242">key</span></span> | <span data-ttu-id="08507-243">value</span><span class="sxs-lookup"><span data-stu-id="08507-243">value</span></span> | <span data-ttu-id="08507-244">valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="08507-244">default</span></span> | <span data-ttu-id="08507-245">notas</span><span class="sxs-lookup"><span data-stu-id="08507-245">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="08507-246">generateHosts</span><span class="sxs-lookup"><span data-stu-id="08507-246">generateHosts</span></span> | <span data-ttu-id="08507-247">boolean</span><span class="sxs-lookup"><span data-stu-id="08507-247">boolean</span></span> | `true` | <span data-ttu-id="08507-248">`true` establece WSL para generar `/etc/hosts`.</span><span class="sxs-lookup"><span data-stu-id="08507-248">`true` sets WSL to generate `/etc/hosts`.</span></span> <span data-ttu-id="08507-249">El archivo `hosts` contiene una asignación estática de direcciones IP correspondientes a nombres de host.</span><span class="sxs-lookup"><span data-stu-id="08507-249">The `hosts` file contains a static map of hostnames corresponding IP address.</span></span> |
| <span data-ttu-id="08507-250">generateResolvConf</span><span class="sxs-lookup"><span data-stu-id="08507-250">generateResolvConf</span></span> | <span data-ttu-id="08507-251">boolean</span><span class="sxs-lookup"><span data-stu-id="08507-251">boolean</span></span> | `true` | <span data-ttu-id="08507-252">`true` establece WSL para generar `/etc/resolv.conf`.</span><span class="sxs-lookup"><span data-stu-id="08507-252">`true` set WSL to generate `/etc/resolv.conf`.</span></span> <span data-ttu-id="08507-253">`resolv.conf` contiene una lista de DNS que es capaz de resolver un nombre de host determinado en su dirección IP.</span><span class="sxs-lookup"><span data-stu-id="08507-253">The `resolv.conf` contains a DNS list that are capable of resolving a given hostname to its IP address.</span></span> | 

#### <a name="interop"></a><span data-ttu-id="08507-254">interop</span><span class="sxs-lookup"><span data-stu-id="08507-254">interop</span></span>

<span data-ttu-id="08507-255">Etiqueta de la sección: `[interop]`</span><span class="sxs-lookup"><span data-stu-id="08507-255">Section label: `[interop]`</span></span>

<span data-ttu-id="08507-256">Estas opciones están disponibles en la compilación 17713 de Insider y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="08507-256">These options are available in Insider Build 17713 and later.</span></span>

| <span data-ttu-id="08507-257">key</span><span class="sxs-lookup"><span data-stu-id="08507-257">key</span></span> | <span data-ttu-id="08507-258">value</span><span class="sxs-lookup"><span data-stu-id="08507-258">value</span></span> | <span data-ttu-id="08507-259">valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="08507-259">default</span></span> | <span data-ttu-id="08507-260">notas</span><span class="sxs-lookup"><span data-stu-id="08507-260">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="08507-261">enabled</span><span class="sxs-lookup"><span data-stu-id="08507-261">enabled</span></span> | <span data-ttu-id="08507-262">boolean</span><span class="sxs-lookup"><span data-stu-id="08507-262">boolean</span></span> | `true` | <span data-ttu-id="08507-263">La configuración de esta clave determinará si WSL admitirá el inicio de procesos de Windows.</span><span class="sxs-lookup"><span data-stu-id="08507-263">Setting this key will determine whether WSL will support launching Windows processes.</span></span> |
| <span data-ttu-id="08507-264">appendWindowsPath</span><span class="sxs-lookup"><span data-stu-id="08507-264">appendWindowsPath</span></span> | <span data-ttu-id="08507-265">boolean</span><span class="sxs-lookup"><span data-stu-id="08507-265">boolean</span></span> | `true` | <span data-ttu-id="08507-266">Establecer esta clave determinará si WSL agregará elementos de ruta de acceso de Windows a la variable de entorno $PATH.</span><span class="sxs-lookup"><span data-stu-id="08507-266">Setting this key will determine whether WSL will add Windows path elements to the $PATH environment variable.</span></span> | 
