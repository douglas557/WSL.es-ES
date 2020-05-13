---
title: Administrar distribuciones de Linux
description: Lista de referencia y configuración de varias distribuciones de Linux que se ejecutan en el subsistema de Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, subsistemawindows, ubuntu, wsl.conf, wslconfig
ms.date: 05/12/2020
ms.topic: article
ms.openlocfilehash: e72822bdec0ef5788bd384a5795a91d746428800
ms.sourcegitcommit: e6e888f2b88a2d9c105cee46e5ab5b70aa43dd80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2020
ms.locfileid: "83343903"
---
# <a name="wsl-commands-and-launch-configurations"></a><span data-ttu-id="4da81-104">Comandos WSL y configuraciones de inicio</span><span class="sxs-lookup"><span data-stu-id="4da81-104">WSL commands and launch configurations</span></span>

## <a name="ways-to-run-wsl"></a><span data-ttu-id="4da81-105">Formas de ejecutar WSL</span><span class="sxs-lookup"><span data-stu-id="4da81-105">Ways to run WSL</span></span>

<span data-ttu-id="4da81-106">Hay varias maneras de ejecutar una distribución de Linux con WSL una vez [instalado](install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="4da81-106">There are several ways to run a Linux distribution with WSL once it's [installed](install-win10.md).</span></span>

1. <span data-ttu-id="4da81-107">Abra la distribución de Linux; para ello, vaya al menú Inicio de Windows y escriba el nombre de las distribuciones instaladas.</span><span class="sxs-lookup"><span data-stu-id="4da81-107">Open your Linux distribution by visiting the Windows Start menu and typing the name of your installed distributions.</span></span> <span data-ttu-id="4da81-108">Por ejemplo: "Ubuntu".</span><span class="sxs-lookup"><span data-stu-id="4da81-108">For example: "Ubuntu".</span></span>
2. <span data-ttu-id="4da81-109">En el símbolo del sistema de Windows o PowerShell, escriba el nombre de la distribución instalada.</span><span class="sxs-lookup"><span data-stu-id="4da81-109">From Windows Command Prompt or PowerShell, enter the name of your installed distribution.</span></span> <span data-ttu-id="4da81-110">Por ejemplo: `ubuntu`</span><span class="sxs-lookup"><span data-stu-id="4da81-110">For example: `ubuntu`</span></span>
3. <span data-ttu-id="4da81-111">Desde el símbolo del sistema de Windows o PowerShell, para abrir la distribución de Linux predeterminada dentro de la línea de comandos actual, escriba: `wsl.exe` .</span><span class="sxs-lookup"><span data-stu-id="4da81-111">From Windows Command Prompt or PowerShell, to open your default Linux distribution inside your current command line, enter: `wsl.exe`.</span></span>
4. <span data-ttu-id="4da81-112">Desde el símbolo del sistema de Windows o PowerShell, para abrir la distribución de Linux predeterminada dentro de la línea de comandos actual, escriba: `wsl [command]` .</span><span class="sxs-lookup"><span data-stu-id="4da81-112">From Windows Command Prompt or PowerShell, to open your default Linux distribution inside your current command line, enter:`wsl [command]`.</span></span>

<span data-ttu-id="4da81-113">El método que deba usar dependerá de lo que esté haciendo.</span><span class="sxs-lookup"><span data-stu-id="4da81-113">Which method you should use depends on what you're doing.</span></span> <span data-ttu-id="4da81-114">Si ha abierto una línea de comandos de WSL en un símbolo del sistema de Windows o en una ventana de PowerShell y desea salir, escriba el comando: `exit` .</span><span class="sxs-lookup"><span data-stu-id="4da81-114">If you've opened a WSL command line within a Windows Prompt or PowerShell window and want to exit, enter the command: `exit`.</span></span>

## <a name="launch-wsl-by-distribution"></a><span data-ttu-id="4da81-115">Iniciar WSL por distribución</span><span class="sxs-lookup"><span data-stu-id="4da81-115">Launch WSL by distribution</span></span>

<span data-ttu-id="4da81-116">La ejecución de una distribución mediante su aplicación específica de distribución inicia esa distribución en su propia ventana de la consola.</span><span class="sxs-lookup"><span data-stu-id="4da81-116">Running a distribution using it's distro-specific application launches that distribution in it's own console window.</span></span>

![Iniciar WSL desde el menú Inicio](media/start-launch.png)

<span data-ttu-id="4da81-118">Es lo mismo que hacer clic en "Iniciar" en Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="4da81-118">It is the same as clicking "Launch" in the Microsoft store.</span></span>

![Iniciar WSL desde Microsoft Store](media/store-launch.png)

<span data-ttu-id="4da81-120">También puedes ejecutar la distribución desde la línea de comandos ejecutando `[distribution].exe`.</span><span class="sxs-lookup"><span data-stu-id="4da81-120">You can also run the distribution from the command line by running `[distribution].exe`.</span></span>

<span data-ttu-id="4da81-121">El inconveniente de ejecutar una distribución desde la línea de comandos de esta manera es que cambiará automáticamente el directorio de trabajo del directorio actual al directorio principal de la distribución.</span><span class="sxs-lookup"><span data-stu-id="4da81-121">The disadvantage of running a distribution from the command line in this way is that it will automatically change your working directory from the current directory to the distribution's home directory.</span></span>

<span data-ttu-id="4da81-122">**Ejemplo: (con PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="4da81-122">**Example: (using PowerShell)**</span></span>

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

### <a name="wsl-and-wsl-command"></a><span data-ttu-id="4da81-123">wsl y wsl [command]</span><span class="sxs-lookup"><span data-stu-id="4da81-123">wsl and wsl [command]</span></span>

<span data-ttu-id="4da81-124">La mejor manera de ejecutar WSL desde la línea de comandos es usar `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="4da81-124">The best way to run WSL from the command line is using `wsl.exe`.</span></span>

<span data-ttu-id="4da81-125">**Ejemplo: (con PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="4da81-125">**Example: (using PowerShell)**</span></span>

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

<span data-ttu-id="4da81-126">`wsl` no solo mantiene el directorio de trabajo actual, sino que te permite ejecutar un único comando junto a los comandos de Windows.</span><span class="sxs-lookup"><span data-stu-id="4da81-126">Not only does `wsl` keep the current working directory in place, it lets you run a single command along side Windows commands.</span></span>

<span data-ttu-id="4da81-127">**Ejemplo: (con PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="4da81-127">**Example: (using PowerShell)**</span></span>

```console
PS C:\Users\sarah> Get-Date

Sunday, March 11, 2018 7:54:05 PM

PS C:\Users\sarah> wsl
scooley@scooley-elmer:/mnt/c/Users/sarah$ date
Sun Mar 11 19:55:47 DST 2018
scooley@scooley-elmer:/mnt/c/Users/sarah$ exit
logout

PS C:\Users\sarah> wsl date
Sun Mar 11 19:56:57 DST 2018
```

<span data-ttu-id="4da81-128">**Ejemplo: (con PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="4da81-128">**Example: (using PowerShell)**</span></span>

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

## <a name="managing-multiple-linux-distributions"></a><span data-ttu-id="4da81-129">Administración de varias distribuciones de Linux</span><span class="sxs-lookup"><span data-stu-id="4da81-129">Managing multiple Linux Distributions</span></span>

<span data-ttu-id="4da81-130">En Windows 10 versión 1903 [y versiones posteriores](ms-settings:windowsupdate), puede usar `wsl.exe` para administrar las distribuciones en el subsistema de Windows para Linux (WSL), incluida la lista de distribuciones disponibles, la configuración de una distribución predeterminada y la desinstalación de distribuciones.</span><span class="sxs-lookup"><span data-stu-id="4da81-130">In Windows 10 Version 1903 [and later](ms-settings:windowsupdate), you can use `wsl.exe` to manage your distributions in the Windows Subsystem for Linux (WSL), including listing available distributions, setting a default distribution, and uninstalling distributions.</span></span>

<span data-ttu-id="4da81-131">Cada distribución de Linux administra de forma independiente sus propias configuraciones.</span><span class="sxs-lookup"><span data-stu-id="4da81-131">Each Linux distribution independently manages its own configurations.</span></span> <span data-ttu-id="4da81-132">Para ver los comandos específicos de la distribución, ejecuta `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="4da81-132">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="4da81-133">Por ejemplo, `ubuntu /?`.</span><span class="sxs-lookup"><span data-stu-id="4da81-133">For example `ubuntu /?`.</span></span>

## <a name="list-distributions"></a><span data-ttu-id="4da81-134">Enumerar distribuciones</span><span class="sxs-lookup"><span data-stu-id="4da81-134">List distributions</span></span>

<span data-ttu-id="4da81-135">`wsl -l` , `wsl --list`</span><span class="sxs-lookup"><span data-stu-id="4da81-135">`wsl -l` , `wsl --list`</span></span>  
<span data-ttu-id="4da81-136">Enumera las distribuciones de Linux disponibles para WSL.</span><span class="sxs-lookup"><span data-stu-id="4da81-136">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="4da81-137">Si se enumera una distribución, está instalada y lista para usar.</span><span class="sxs-lookup"><span data-stu-id="4da81-137">If a distribution is listed, it's installed and ready to use.</span></span>

<span data-ttu-id="4da81-138">`wsl --list --all`Muestra todas las distribuciones, incluidas las que no se pueden usar actualmente.</span><span class="sxs-lookup"><span data-stu-id="4da81-138">`wsl --list --all` Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="4da81-139">Pueden encontrarse en proceso de instalación, desinstalación o tener un estado interrumpido.</span><span class="sxs-lookup"><span data-stu-id="4da81-139">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

<span data-ttu-id="4da81-140">`wsl --list --running`Muestra todas las distribuciones que se están ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="4da81-140">`wsl --list --running` Lists all distributions that are currently running.</span></span>

## <a name="set-a-default-distribution"></a><span data-ttu-id="4da81-141">Establecer una distribución predeterminada</span><span class="sxs-lookup"><span data-stu-id="4da81-141">Set a default distribution</span></span>

<span data-ttu-id="4da81-142">La distribución de WSL predeterminada es la que se ejecuta cuando se ejecuta `wsl` en una línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="4da81-142">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

<span data-ttu-id="4da81-143">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="4da81-143">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span></span>

<span data-ttu-id="4da81-144">Establece la distribución predeterminada en `<DistributionName>`.</span><span class="sxs-lookup"><span data-stu-id="4da81-144">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="4da81-145">**Ejemplo: (con PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="4da81-145">**Example: (using PowerShell)**</span></span>  
<span data-ttu-id="4da81-146">`wsl -s Ubuntu` establecería la distribución predeterminada en Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="4da81-146">`wsl -s Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="4da81-147">Ahora, al ejecutar `wsl npm init`, se ejecutará en Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="4da81-147">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="4da81-148">Si se ejecuta `wsl`, se abrirá una sesión de Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="4da81-148">If I run `wsl` it will open an Ubuntu session.</span></span>

## <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="4da81-149">Anular el registro de una distribución y reinstalarla</span><span class="sxs-lookup"><span data-stu-id="4da81-149">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="4da81-150">Aunque las distribuciones de Linux se pueden instalar a través de Microsoft Store, no se pueden desinstalar a través de Store.</span><span class="sxs-lookup"><span data-stu-id="4da81-150">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="4da81-151">WSL Config permite anular el registro de las distribuciones o desinstalarlas.</span><span class="sxs-lookup"><span data-stu-id="4da81-151">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="4da81-152">La anulación del registro también permite volver a instalar las distribuciones.</span><span class="sxs-lookup"><span data-stu-id="4da81-152">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="4da81-153">**PRECAUCIÓN:** Una vez que se ha anulado el registro, todos los datos, la configuración y el software asociados a esa distribución se perderán de forma permanente.</span><span class="sxs-lookup"><span data-stu-id="4da81-153">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="4da81-154">Si se vuelve a instalar desde Store, se instalará una copia limpia de la distribución.</span><span class="sxs-lookup"><span data-stu-id="4da81-154">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wsl --unregister <DistributionName>`  
<span data-ttu-id="4da81-155">Anula el registro de la distribución de WSL para que se pueda volver a instalar o limpiar.</span><span class="sxs-lookup"><span data-stu-id="4da81-155">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="4da81-156">Por ejemplo: `wsl --unregister Ubuntu` quitaría Ubuntu de las distribuciones disponibles en WSL.</span><span class="sxs-lookup"><span data-stu-id="4da81-156">For example: `wsl --unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="4da81-157">Al ejecutar `wsl --list`, no aparecerá en la lista.</span><span class="sxs-lookup"><span data-stu-id="4da81-157">When I run `wsl --list` it will not be listed.</span></span>

<span data-ttu-id="4da81-158">Para reinstalar, busque la distribución en Microsoft Store y seleccione "Iniciar".</span><span class="sxs-lookup"><span data-stu-id="4da81-158">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

## <a name="run-as-a-specific-user"></a><span data-ttu-id="4da81-159">Ejecutar como usuario específico</span><span class="sxs-lookup"><span data-stu-id="4da81-159">Run as a specific user</span></span>

<span data-ttu-id="4da81-160">`wsl -u <Username>`, `wsl --user <Username>`</span><span class="sxs-lookup"><span data-stu-id="4da81-160">`wsl -u <Username>`, `wsl --user <Username>`</span></span>

<span data-ttu-id="4da81-161">Ejecuta WSL como el usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="4da81-161">Run WSL as the specified user.</span></span> <span data-ttu-id="4da81-162">Ten en cuenta que el usuario debe existir dentro de la distribución de WSL.</span><span class="sxs-lookup"><span data-stu-id="4da81-162">Please note that user must exist inside of the WSL distribution.</span></span>

## <a name="change-the-default-user-for-a-distribution"></a><span data-ttu-id="4da81-163">Cambiar el usuario predeterminado para una distribución</span><span class="sxs-lookup"><span data-stu-id="4da81-163">Change the default user for a distribution</span></span>

`<DistributionName> config --default-user <Username>`

<span data-ttu-id="4da81-164">Cambie el usuario predeterminado para el inicio de sesión de distribución.</span><span class="sxs-lookup"><span data-stu-id="4da81-164">Change the default user that for your distribution log-in.</span></span> <span data-ttu-id="4da81-165">El usuario ya debe existir dentro de la distribución para convertirse en el usuario predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4da81-165">The user has to already exist inside the distribution in order to become the default user.</span></span> 

<span data-ttu-id="4da81-166">Por ejemplo: `ubuntu config --default-user johndoe` cambiaría el usuario predeterminado de la distribución de Ubuntu al usuario "\ \ \".</span><span class="sxs-lookup"><span data-stu-id="4da81-166">For example: `ubuntu config --default-user johndoe` would change the default user for the Ubuntu distribution to the "johndoe" user.</span></span>

> [!NOTE]
> <span data-ttu-id="4da81-167">Si tiene problemas para averiguar el nombre de la distribución, consulte [lista de distribuciones](https://docs.microsoft.com/windows/wsl/wsl-config#list-distributions) para que el comando muestre el nombre oficial de las distribuciones instaladas.</span><span class="sxs-lookup"><span data-stu-id="4da81-167">If you are having trouble figuring out the name of your distribution, see [List distributions](https://docs.microsoft.com/windows/wsl/wsl-config#list-distributions) for the command to list the official name of the installed distributions.</span></span> 

## <a name="run-a-specific-distribution"></a><span data-ttu-id="4da81-168">Ejecutar una distribución específica</span><span class="sxs-lookup"><span data-stu-id="4da81-168">Run a specific distribution</span></span>

<span data-ttu-id="4da81-169">`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="4da81-169">`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`</span></span>

<span data-ttu-id="4da81-170">Ejecuta una distribución especificada de WSL, se puede usar para enviar comandos a una distribución específica sin tener que cambiar la predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4da81-170">Run a specified distribution of WSL, can be used to send commands to a specific distribution without having to change your default.</span></span>

## <a name="managing-multiple-linux-distributions-in-earlier-windows-versions"></a><span data-ttu-id="4da81-171">Administración de varias distribuciones de Linux en versiones anteriores de Windows</span><span class="sxs-lookup"><span data-stu-id="4da81-171">Managing multiple Linux Distributions in earlier Windows versions</span></span>

<span data-ttu-id="4da81-172">En Windows 10 anterior a la versión 1903, `wslconfig.exe` se debe usar la herramienta de línea de comandos WSL config () para administrar las distribuciones de Linux que se ejecutan en el subsistema de Windows para Linux (WSL).</span><span class="sxs-lookup"><span data-stu-id="4da81-172">In Windows 10 prior to version 1903, the WSL Config (`wslconfig.exe`) command-line tool should be used to manage Linux distributions running on the Windows Subsystem for Linux (WSL).</span></span>  <span data-ttu-id="4da81-173">Te permite enumerar las distribuciones disponibles, establecer una distribución predeterminada y desinstalar las distribuciones.</span><span class="sxs-lookup"><span data-stu-id="4da81-173">It lets you list available distributions, set a default distribution, and uninstall distributions.</span></span>

<span data-ttu-id="4da81-174">Si bien WSL Config es útil para las configuraciones que abarcan o coordinan las distribuciones, cada distribución de Linux administra de forma independiente sus propias configuraciones.</span><span class="sxs-lookup"><span data-stu-id="4da81-174">While WSL Config is helpful for settings that span or coordinate distributions, each Linux distribution independently manages its own configurations.</span></span>  <span data-ttu-id="4da81-175">Para ver los comandos específicos de la distribución, ejecuta `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="4da81-175">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="4da81-176">Por ejemplo, `ubuntu /?`.</span><span class="sxs-lookup"><span data-stu-id="4da81-176">For example `ubuntu /?`.</span></span>

<span data-ttu-id="4da81-177">Para ver todas las opciones disponibles para wslconfig, ejecuta: `wslconfig /?`</span><span class="sxs-lookup"><span data-stu-id="4da81-177">To see all available options for wslconfig, run:  `wslconfig /?`</span></span>

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

<span data-ttu-id="4da81-178">Para enumerar las distribuciones, use:</span><span class="sxs-lookup"><span data-stu-id="4da81-178">To list distributions, use:</span></span>

`wslconfig /list`  
<span data-ttu-id="4da81-179">Enumera las distribuciones de Linux disponibles para WSL.</span><span class="sxs-lookup"><span data-stu-id="4da81-179">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="4da81-180">Si se enumera una distribución, está instalada y lista para usar.</span><span class="sxs-lookup"><span data-stu-id="4da81-180">If a distribution is listed, it's installed and ready to use.</span></span>

`wslconfig /list /all`  
<span data-ttu-id="4da81-181">Enumera todas las distribuciones, incluidas las que no se pueden usar actualmente.</span><span class="sxs-lookup"><span data-stu-id="4da81-181">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="4da81-182">Pueden encontrarse en proceso de instalación, desinstalación o tener un estado interrumpido.</span><span class="sxs-lookup"><span data-stu-id="4da81-182">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

<span data-ttu-id="4da81-183">Para establecer una distribución predeterminada que se ejecuta cuando se ejecuta `wsl` en una línea de comandos:</span><span class="sxs-lookup"><span data-stu-id="4da81-183">To set a default distribution that runs when you run `wsl` on a command line:</span></span>

<span data-ttu-id="4da81-184">`wslconfig /setdefault <DistributionName>`Establece la distribución predeterminada en `<DistributionName>` .</span><span class="sxs-lookup"><span data-stu-id="4da81-184">`wslconfig /setdefault <DistributionName>` Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="4da81-185">**Ejemplo: (con PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="4da81-185">**Example: (using PowerShell)**</span></span>  
<span data-ttu-id="4da81-186">`wslconfig /setdefault Ubuntu` establecería la distribución predeterminada en Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="4da81-186">`wslconfig /setdefault Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="4da81-187">Ahora, al ejecutar `wsl npm init`, se ejecutará en Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="4da81-187">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="4da81-188">Si se ejecuta `wsl`, se abrirá una sesión de Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="4da81-188">If I run `wsl` it will open an Ubuntu session.</span></span>

<span data-ttu-id="4da81-189">Para anular el registro y reinstalar una distribución:</span><span class="sxs-lookup"><span data-stu-id="4da81-189">To unregister and reinstall a distribution:</span></span>

`wslconfig /unregister <DistributionName>`  
<span data-ttu-id="4da81-190">Anula el registro de la distribución de WSL para que se pueda volver a instalar o limpiar.</span><span class="sxs-lookup"><span data-stu-id="4da81-190">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="4da81-191">Por ejemplo: `wslconfig /unregister Ubuntu` quitaría Ubuntu de las distribuciones disponibles en WSL.</span><span class="sxs-lookup"><span data-stu-id="4da81-191">For example: `wslconfig /unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="4da81-192">Al ejecutar `wslconfig /list`, no aparecerá en la lista.</span><span class="sxs-lookup"><span data-stu-id="4da81-192">When I run `wslconfig /list` it will not be listed.</span></span>

<span data-ttu-id="4da81-193">Para reinstalar, busque la distribución en Microsoft Store y seleccione "Iniciar".</span><span class="sxs-lookup"><span data-stu-id="4da81-193">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

## <a name="configure-per-distro-launch-settings-with-wslconf"></a><span data-ttu-id="4da81-194">Configurar por configuración de inicio de distribución con wslconf</span><span class="sxs-lookup"><span data-stu-id="4da81-194">Configure per distro launch settings with wslconf</span></span>

> <span data-ttu-id="4da81-195">**Disponible en Windows Build 17093 y versiones posteriores**</span><span class="sxs-lookup"><span data-stu-id="4da81-195">**Available in Windows Build 17093 and later**</span></span>

<span data-ttu-id="4da81-196">Configura automáticamente cierta funcionalidad en WSL que se aplicará cada vez que inicies el subsistema mediante `wsl.conf`.</span><span class="sxs-lookup"><span data-stu-id="4da81-196">Automatically configure certain functionality in WSL that will be applied every time you launch the subsystem using `wsl.conf`.</span></span>

<span data-ttu-id="4da81-197">En este momento, esto incluye opciones de montaje automático y configuración de red.</span><span class="sxs-lookup"><span data-stu-id="4da81-197">Right now, this includes automount options and network configuration.</span></span>

<span data-ttu-id="4da81-198">`wsl.conf` se encuentra en cada distribución de Linux en `/etc/wsl.conf`.</span><span class="sxs-lookup"><span data-stu-id="4da81-198">`wsl.conf` is located in each Linux distribution in `/etc/wsl.conf`.</span></span> <span data-ttu-id="4da81-199">Si el archivo no está allí, puedes crearlo tú mismo.</span><span class="sxs-lookup"><span data-stu-id="4da81-199">If the file is not there, you can create it yourself.</span></span> <span data-ttu-id="4da81-200">WSL detectará la existencia del archivo y leerá su contenido.</span><span class="sxs-lookup"><span data-stu-id="4da81-200">WSL will detect the existence of the file and will read its contents.</span></span> <span data-ttu-id="4da81-201">Si falta el archivo o tiene un formato incorrecto (es decir, un formato de marcado incorrecto), WSL se iniciará de manera normal.</span><span class="sxs-lookup"><span data-stu-id="4da81-201">If the file is missing or malformed (that is, improper markup formatting), WSL will continue to launch as normal.</span></span>

<span data-ttu-id="4da81-202">A continuación se muestra un archivo de ejemplo `wsl.conf` que se puede Agregar a las distribuciones:</span><span class="sxs-lookup"><span data-stu-id="4da81-202">Here is a sample `wsl.conf` file you could add into your distributions:</span></span>

```console
# Enable extra metadata options by default
[automount]
enabled = true
root = /windir/
options = "metadata,umask=22,fmask=11"
mountFsTab = false

# Enable DNS – even though these are turned on by default, we'll specify here just to be explicit.
[network]
generateHosts = true
generateResolvConf = true
```

### <a name="configuration-options"></a><span data-ttu-id="4da81-203">Opciones de configuración</span><span class="sxs-lookup"><span data-stu-id="4da81-203">Configuration Options</span></span>

<span data-ttu-id="4da81-204">En concordancia con las convenciones de .ini, las claves se declaran en una sección.</span><span class="sxs-lookup"><span data-stu-id="4da81-204">In keeping with .ini conventions, keys are declared under a section.</span></span> 

<span data-ttu-id="4da81-205">WSL admite dos secciones: `automount` y `network`.</span><span class="sxs-lookup"><span data-stu-id="4da81-205">WSL supports two sections: `automount` and `network`.</span></span>

#### <a name="automount"></a><span data-ttu-id="4da81-206">automount</span><span class="sxs-lookup"><span data-stu-id="4da81-206">automount</span></span>

<span data-ttu-id="4da81-207">Sección: `[automount]`</span><span class="sxs-lookup"><span data-stu-id="4da81-207">Section: `[automount]`</span></span>

| <span data-ttu-id="4da81-208">key</span><span class="sxs-lookup"><span data-stu-id="4da81-208">key</span></span>        | <span data-ttu-id="4da81-209">value</span><span class="sxs-lookup"><span data-stu-id="4da81-209">value</span></span>                          | <span data-ttu-id="4da81-210">default</span><span class="sxs-lookup"><span data-stu-id="4da81-210">default</span></span>      | <span data-ttu-id="4da81-211">notas</span><span class="sxs-lookup"><span data-stu-id="4da81-211">notes</span></span>                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4da81-212">enabled</span><span class="sxs-lookup"><span data-stu-id="4da81-212">enabled</span></span>    | <span data-ttu-id="4da81-213">boolean</span><span class="sxs-lookup"><span data-stu-id="4da81-213">boolean</span></span>                        | <span data-ttu-id="4da81-214">true</span><span class="sxs-lookup"><span data-stu-id="4da81-214">true</span></span>         | <span data-ttu-id="4da81-215">`true` hace que las unidades fijas (es decir,</span><span class="sxs-lookup"><span data-stu-id="4da81-215">`true` causes fixed drives (i.e</span></span> <span data-ttu-id="4da81-216">`C:/` o `D:/`) se monten automáticamente con DrvFs en `/mnt`.</span><span class="sxs-lookup"><span data-stu-id="4da81-216">`C:/` or `D:/`) to be automatically mounted with DrvFs under `/mnt`.</span></span>  <span data-ttu-id="4da81-217">`false`significa que las unidades no se montarán automáticamente, pero podría montarlas de forma manual o a través de `fstab` .</span><span class="sxs-lookup"><span data-stu-id="4da81-217">`false` means drives won't be mounted automatically, but you could still mount them manually or via `fstab`.</span></span>                                                                                                             |
| <span data-ttu-id="4da81-218">mountFsTab</span><span class="sxs-lookup"><span data-stu-id="4da81-218">mountFsTab</span></span> | <span data-ttu-id="4da81-219">boolean</span><span class="sxs-lookup"><span data-stu-id="4da81-219">boolean</span></span>                        | <span data-ttu-id="4da81-220">true</span><span class="sxs-lookup"><span data-stu-id="4da81-220">true</span></span>         | <span data-ttu-id="4da81-221">`true` establece `/etc/fstab` para que se procese en el inicio de WSL.</span><span class="sxs-lookup"><span data-stu-id="4da81-221">`true` sets `/etc/fstab` to be processed on WSL start.</span></span> <span data-ttu-id="4da81-222">/etc/fstab es un archivo donde puedes declarar otros sistemas de archivos, como un recurso compartido de SMB.</span><span class="sxs-lookup"><span data-stu-id="4da81-222">/etc/fstab is a file where you can declare other filesystems, like an SMB share.</span></span> <span data-ttu-id="4da81-223">Por lo tanto, puedes montar estos sistemas de archivos automáticamente en WSL en el inicio.</span><span class="sxs-lookup"><span data-stu-id="4da81-223">Thus, you can mount these filesystems automatically in WSL on start up.</span></span>                                                                                                                |
| <span data-ttu-id="4da81-224">root</span><span class="sxs-lookup"><span data-stu-id="4da81-224">root</span></span>       | <span data-ttu-id="4da81-225">Cadena</span><span class="sxs-lookup"><span data-stu-id="4da81-225">String</span></span>                         | `/mnt/`      | <span data-ttu-id="4da81-226">Establece el directorio donde se montarán automáticamente las unidades fijas.</span><span class="sxs-lookup"><span data-stu-id="4da81-226">Sets the directory where fixed drives will be automatically mounted.</span></span> <span data-ttu-id="4da81-227">Por ejemplo, si tienes un directorio en WSL en `/windir/` y lo especificas como raíz, esperarías ver que las unidades fijas se monten en `/windir/c`</span><span class="sxs-lookup"><span data-stu-id="4da81-227">For example, if you have a directory in WSL at `/windir/` and you specify that as the root, you would expect to see your fixed drives mounted at `/windir/c`</span></span>                                                                                              |
| <span data-ttu-id="4da81-228">opciones</span><span class="sxs-lookup"><span data-stu-id="4da81-228">options</span></span>    | <span data-ttu-id="4da81-229">lista de valores separados por comas</span><span class="sxs-lookup"><span data-stu-id="4da81-229">comma-separated list of values</span></span> | <span data-ttu-id="4da81-230">cadena vacía</span><span class="sxs-lookup"><span data-stu-id="4da81-230">empty string</span></span> | <span data-ttu-id="4da81-231">Este valor se anexa a la cadena predeterminada de opciones de montaje de DrvFs.</span><span class="sxs-lookup"><span data-stu-id="4da81-231">This value is appended to the default DrvFs mount options string.</span></span> <span data-ttu-id="4da81-232">**Solo se pueden especificar opciones específicas de DrvFs.**</span><span class="sxs-lookup"><span data-stu-id="4da81-232">**Only DrvFs-specific options can be specified.**</span></span> <span data-ttu-id="4da81-233">No se admiten las opciones que el binario de montaje analizaría normalmente en una marca.</span><span class="sxs-lookup"><span data-stu-id="4da81-233">Options that the mount binary would normally parse into a flag are not supported.</span></span> <span data-ttu-id="4da81-234">Si quieres especificar explícitamente esas opciones, tienes que incluir en /etc/fstab cada unidad para la que quieras hacerlo.</span><span class="sxs-lookup"><span data-stu-id="4da81-234">If you want to explicitly specify those options, you must include every drive for which you want to do so in /etc/fstab.</span></span> |

<span data-ttu-id="4da81-235">De manera predeterminada, WSL establece uid y gid en el valor del usuario predeterminado (en una distribución de Ubuntu, el usuario predeterminado se crea con uid=1000,gid=1000).</span><span class="sxs-lookup"><span data-stu-id="4da81-235">By default, WSL sets the uid and gid to the value of the default user (in Ubuntu distro, the default user is created with uid=1000,gid=1000).</span></span> <span data-ttu-id="4da81-236">Si el usuario especifica una opción gid o uid explícitamente a través de esta clave, se sobrescribirá el valor asociado.</span><span class="sxs-lookup"><span data-stu-id="4da81-236">If the user specifies a gid or uid option explicitly via this key, the associated value will be overwritten.</span></span> <span data-ttu-id="4da81-237">De lo contrario, siempre se anexará el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4da81-237">Otherwise, the default value will always be appended.</span></span>

<span data-ttu-id="4da81-238">**Nota:** Estas opciones se aplican como opciones de montaje para todas las unidades montadas automáticamente.</span><span class="sxs-lookup"><span data-stu-id="4da81-238">**Note:** These options are applied as the mount options for all automatically mounted drives.</span></span> <span data-ttu-id="4da81-239">Para cambiar las opciones solo para una unidad específica, usa /etc/fstab en su lugar.</span><span class="sxs-lookup"><span data-stu-id="4da81-239">To change the options for a specific drive only, use /etc/fstab instead.</span></span>

#### <a name="mount-options"></a><span data-ttu-id="4da81-240">Opciones de montaje</span><span class="sxs-lookup"><span data-stu-id="4da81-240">Mount options</span></span>

<span data-ttu-id="4da81-241">Establecer diferentes opciones de montaje para las unidades de Windows (DrvFs) puede controlar cómo se calculan los permisos de archivo para los archivos de Windows.</span><span class="sxs-lookup"><span data-stu-id="4da81-241">Setting different mount options for Windows drives (DrvFs) can control how file permissions are calculated for Windows files.</span></span> <span data-ttu-id="4da81-242">Están disponibles las opciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="4da81-242">The following options are available:</span></span>

| <span data-ttu-id="4da81-243">Clave</span><span class="sxs-lookup"><span data-stu-id="4da81-243">Key</span></span> | <span data-ttu-id="4da81-244">Descripción</span><span class="sxs-lookup"><span data-stu-id="4da81-244">Description</span></span> | <span data-ttu-id="4da81-245">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="4da81-245">Default</span></span> |
|:----|:----|:----|
|<span data-ttu-id="4da81-246">uid</span><span class="sxs-lookup"><span data-stu-id="4da81-246">uid</span></span>| <span data-ttu-id="4da81-247">Id. de usuario que se usa para el propietario de todos los archivos</span><span class="sxs-lookup"><span data-stu-id="4da81-247">The User ID used for the owner of all files</span></span> | <span data-ttu-id="4da81-248">Id. de usuario predeterminado de su distribución WSL (en la primera instalación, el valor predeterminado es 1000)</span><span class="sxs-lookup"><span data-stu-id="4da81-248">The default User ID of your WSL distro (On first installation this defaults to 1000)</span></span>
|<span data-ttu-id="4da81-249">gid</span><span class="sxs-lookup"><span data-stu-id="4da81-249">gid</span></span>| <span data-ttu-id="4da81-250">Id. de grupo que se usa para el propietario de todos los archivos</span><span class="sxs-lookup"><span data-stu-id="4da81-250">The Group ID used for the owner of all files</span></span> | <span data-ttu-id="4da81-251">Id. de grupo predeterminado de su distribución WSL (en la primera instalación, el valor predeterminado es 1000)</span><span class="sxs-lookup"><span data-stu-id="4da81-251">The default group ID of your WSL distro (On first installation this defaults to 1000)</span></span>
|<span data-ttu-id="4da81-252">umask</span><span class="sxs-lookup"><span data-stu-id="4da81-252">umask</span></span> | <span data-ttu-id="4da81-253">Máscara octal de permisos que se van a excluir para todos los archivos y directorios</span><span class="sxs-lookup"><span data-stu-id="4da81-253">An octal mask of permissions to exclude for all files and directories</span></span> | <span data-ttu-id="4da81-254">000</span><span class="sxs-lookup"><span data-stu-id="4da81-254">000</span></span>
|<span data-ttu-id="4da81-255">fmask</span><span class="sxs-lookup"><span data-stu-id="4da81-255">fmask</span></span> | <span data-ttu-id="4da81-256">Máscara octal de permisos que se van a excluir para todos los archivos</span><span class="sxs-lookup"><span data-stu-id="4da81-256">An octal mask of permissions to exclude for all files</span></span> | <span data-ttu-id="4da81-257">000</span><span class="sxs-lookup"><span data-stu-id="4da81-257">000</span></span>
|<span data-ttu-id="4da81-258">dmask</span><span class="sxs-lookup"><span data-stu-id="4da81-258">dmask</span></span> | <span data-ttu-id="4da81-259">Máscara octal de permisos que se van a excluir para todos los directorios</span><span class="sxs-lookup"><span data-stu-id="4da81-259">An octal mask of permissions to exclude for all directories</span></span> | <span data-ttu-id="4da81-260">000</span><span class="sxs-lookup"><span data-stu-id="4da81-260">000</span></span>

<span data-ttu-id="4da81-261">**Nota:** Las máscaras de permisos se colocan a través de una operación OR lógica antes de aplicarse a archivos o directorios.</span><span class="sxs-lookup"><span data-stu-id="4da81-261">**Note:** The permission masks are put through a logical OR operation before being applied to files or directories.</span></span> 

#### <a name="network"></a><span data-ttu-id="4da81-262">red</span><span class="sxs-lookup"><span data-stu-id="4da81-262">network</span></span>

<span data-ttu-id="4da81-263">Etiqueta de la sección: `[network]`</span><span class="sxs-lookup"><span data-stu-id="4da81-263">Section label: `[network]`</span></span>

| <span data-ttu-id="4da81-264">key</span><span class="sxs-lookup"><span data-stu-id="4da81-264">key</span></span> | <span data-ttu-id="4da81-265">value</span><span class="sxs-lookup"><span data-stu-id="4da81-265">value</span></span> | <span data-ttu-id="4da81-266">default</span><span class="sxs-lookup"><span data-stu-id="4da81-266">default</span></span> | <span data-ttu-id="4da81-267">notas</span><span class="sxs-lookup"><span data-stu-id="4da81-267">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="4da81-268">generateHosts</span><span class="sxs-lookup"><span data-stu-id="4da81-268">generateHosts</span></span> | <span data-ttu-id="4da81-269">boolean</span><span class="sxs-lookup"><span data-stu-id="4da81-269">boolean</span></span> | `true` | <span data-ttu-id="4da81-270">`true` establece WSL para generar `/etc/hosts`.</span><span class="sxs-lookup"><span data-stu-id="4da81-270">`true` sets WSL to generate `/etc/hosts`.</span></span> <span data-ttu-id="4da81-271">El archivo `hosts` contiene una asignación estática de direcciones IP correspondientes a nombres de host.</span><span class="sxs-lookup"><span data-stu-id="4da81-271">The `hosts` file contains a static map of hostnames corresponding IP address.</span></span> |
| <span data-ttu-id="4da81-272">generateResolvConf</span><span class="sxs-lookup"><span data-stu-id="4da81-272">generateResolvConf</span></span> | <span data-ttu-id="4da81-273">boolean</span><span class="sxs-lookup"><span data-stu-id="4da81-273">boolean</span></span> | `true` | <span data-ttu-id="4da81-274">`true` establece WSL para generar `/etc/resolv.conf`.</span><span class="sxs-lookup"><span data-stu-id="4da81-274">`true` set WSL to generate `/etc/resolv.conf`.</span></span> <span data-ttu-id="4da81-275">`resolv.conf` contiene una lista de DNS que es capaz de resolver un nombre de host determinado en su dirección IP.</span><span class="sxs-lookup"><span data-stu-id="4da81-275">The `resolv.conf` contains a DNS list that are capable of resolving a given hostname to its IP address.</span></span> | 

#### <a name="interop"></a><span data-ttu-id="4da81-276">interop</span><span class="sxs-lookup"><span data-stu-id="4da81-276">interop</span></span>

<span data-ttu-id="4da81-277">Etiqueta de la sección: `[interop]`</span><span class="sxs-lookup"><span data-stu-id="4da81-277">Section label: `[interop]`</span></span>

<span data-ttu-id="4da81-278">Estas opciones están disponibles en la compilación 17713 de Insider y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4da81-278">These options are available in Insider Build 17713 and later.</span></span>

| <span data-ttu-id="4da81-279">key</span><span class="sxs-lookup"><span data-stu-id="4da81-279">key</span></span> | <span data-ttu-id="4da81-280">value</span><span class="sxs-lookup"><span data-stu-id="4da81-280">value</span></span> | <span data-ttu-id="4da81-281">default</span><span class="sxs-lookup"><span data-stu-id="4da81-281">default</span></span> | <span data-ttu-id="4da81-282">notas</span><span class="sxs-lookup"><span data-stu-id="4da81-282">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="4da81-283">enabled</span><span class="sxs-lookup"><span data-stu-id="4da81-283">enabled</span></span> | <span data-ttu-id="4da81-284">boolean</span><span class="sxs-lookup"><span data-stu-id="4da81-284">boolean</span></span> | `true` | <span data-ttu-id="4da81-285">La configuración de esta clave determinará si WSL admitirá el inicio de procesos de Windows.</span><span class="sxs-lookup"><span data-stu-id="4da81-285">Setting this key will determine whether WSL will support launching Windows processes.</span></span> |
| <span data-ttu-id="4da81-286">appendWindowsPath</span><span class="sxs-lookup"><span data-stu-id="4da81-286">appendWindowsPath</span></span> | <span data-ttu-id="4da81-287">boolean</span><span class="sxs-lookup"><span data-stu-id="4da81-287">boolean</span></span> | `true` | <span data-ttu-id="4da81-288">Establecer esta clave determinará si WSL agregará elementos de ruta de acceso de Windows a la variable de entorno $PATH.</span><span class="sxs-lookup"><span data-stu-id="4da81-288">Setting this key will determine whether WSL will add Windows path elements to the $PATH environment variable.</span></span> |

#### <a name="user"></a><span data-ttu-id="4da81-289">usuario</span><span class="sxs-lookup"><span data-stu-id="4da81-289">user</span></span>

<span data-ttu-id="4da81-290">Etiqueta de la sección: `[user]`</span><span class="sxs-lookup"><span data-stu-id="4da81-290">Section label: `[user]`</span></span>

<span data-ttu-id="4da81-291">Estas opciones están disponibles en la compilación 18980 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4da81-291">These options are available in Build 18980 and later.</span></span>

| <span data-ttu-id="4da81-292">key</span><span class="sxs-lookup"><span data-stu-id="4da81-292">key</span></span> | <span data-ttu-id="4da81-293">value</span><span class="sxs-lookup"><span data-stu-id="4da81-293">value</span></span> | <span data-ttu-id="4da81-294">default</span><span class="sxs-lookup"><span data-stu-id="4da81-294">default</span></span> | <span data-ttu-id="4da81-295">HDInsight</span><span class="sxs-lookup"><span data-stu-id="4da81-295">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="4da81-296">default</span><span class="sxs-lookup"><span data-stu-id="4da81-296">default</span></span> | <span data-ttu-id="4da81-297">string</span><span class="sxs-lookup"><span data-stu-id="4da81-297">string</span></span> | <span data-ttu-id="4da81-298">El nombre de usuario inicial creado en la primera ejecución</span><span class="sxs-lookup"><span data-stu-id="4da81-298">The initial username created on first run</span></span> | <span data-ttu-id="4da81-299">Al establecer esta clave, se especifica el usuario que se debe ejecutar como cuando se inicia por primera vez una sesión de WSL.</span><span class="sxs-lookup"><span data-stu-id="4da81-299">Setting this key specifies which user to run as when first starting a WSL session.</span></span> |

## <a name="configure-global-options-with-wslconfig"></a><span data-ttu-id="4da81-300">Configurar opciones globales con. wslconfig</span><span class="sxs-lookup"><span data-stu-id="4da81-300">Configure global options with .wslconfig</span></span>

> <span data-ttu-id="4da81-301">**Disponible en Windows Build 19041 y versiones posteriores**</span><span class="sxs-lookup"><span data-stu-id="4da81-301">**Available in Windows Build 19041 and later**</span></span>

<span data-ttu-id="4da81-302">Puede configurar las opciones de WSL globales colocando un `.wslconfig` archivo en el directorio raíz de la carpeta de los usuarios: `C:\Users\<yourUserName>\.wslconfig` .</span><span class="sxs-lookup"><span data-stu-id="4da81-302">You can configure global WSL options by placing a `.wslconfig` file into the root directory of your users folder: `C:\Users\<yourUserName>\.wslconfig`.</span></span> <span data-ttu-id="4da81-303">Este archivo puede contener las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="4da81-303">This file can contain the following options:</span></span>

### <a name="wsl-2-settings"></a><span data-ttu-id="4da81-304">Configuración de WSL 2</span><span class="sxs-lookup"><span data-stu-id="4da81-304">WSL 2 Settings</span></span>

<span data-ttu-id="4da81-305">Esta configuración afecta a la máquina virtual que alimenta cualquier distribución de WSL 2.</span><span class="sxs-lookup"><span data-stu-id="4da81-305">These settings affect the VM that powers any WSL 2 distribution.</span></span> 

| <span data-ttu-id="4da81-306">key</span><span class="sxs-lookup"><span data-stu-id="4da81-306">key</span></span> | <span data-ttu-id="4da81-307">value</span><span class="sxs-lookup"><span data-stu-id="4da81-307">value</span></span> | <span data-ttu-id="4da81-308">default</span><span class="sxs-lookup"><span data-stu-id="4da81-308">default</span></span> | <span data-ttu-id="4da81-309">HDInsight</span><span class="sxs-lookup"><span data-stu-id="4da81-309">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="4da81-310">kernel</span><span class="sxs-lookup"><span data-stu-id="4da81-310">kernel</span></span> | <span data-ttu-id="4da81-311">string</span><span class="sxs-lookup"><span data-stu-id="4da81-311">string</span></span> | <span data-ttu-id="4da81-312">Bandeja de entrada proporcionada por el kernel de Microsoft</span><span class="sxs-lookup"><span data-stu-id="4da81-312">The Microsoft built kernel provided inbox</span></span> | <span data-ttu-id="4da81-313">Una ruta de acceso de Windows absoluta a un kernel de Linux personalizado.</span><span class="sxs-lookup"><span data-stu-id="4da81-313">An absolute Windows path to a custom Linux kernel.</span></span> |
| <span data-ttu-id="4da81-314">memoria</span><span class="sxs-lookup"><span data-stu-id="4da81-314">memory</span></span> | <span data-ttu-id="4da81-315">tamaño</span><span class="sxs-lookup"><span data-stu-id="4da81-315">size</span></span> | <span data-ttu-id="4da81-316">80% de la memoria total en Windows</span><span class="sxs-lookup"><span data-stu-id="4da81-316">80% of your total memory on Windows</span></span> | <span data-ttu-id="4da81-317">Cantidad de memoria que se va a asignar a la máquina virtual WSL 2.</span><span class="sxs-lookup"><span data-stu-id="4da81-317">How much memory to assign to the WSL 2 VM.</span></span> |
| <span data-ttu-id="4da81-318">procesadores</span><span class="sxs-lookup"><span data-stu-id="4da81-318">processors</span></span> | <span data-ttu-id="4da81-319">number</span><span class="sxs-lookup"><span data-stu-id="4da81-319">number</span></span> | <span data-ttu-id="4da81-320">El mismo número de procesadores en Windows</span><span class="sxs-lookup"><span data-stu-id="4da81-320">The same number of processors on Windows</span></span> | <span data-ttu-id="4da81-321">El número de procesadores que se asignan a la máquina virtual WSL 2.</span><span class="sxs-lookup"><span data-stu-id="4da81-321">How many processors to assign ot the WSL 2 VM.</span></span> |
| <span data-ttu-id="4da81-322">localhostForwarding</span><span class="sxs-lookup"><span data-stu-id="4da81-322">localhostForwarding</span></span> | <span data-ttu-id="4da81-323">boolean</span><span class="sxs-lookup"><span data-stu-id="4da81-323">boolean</span></span> | `true` | <span data-ttu-id="4da81-324">Valor booleano que especifica si los puertos enlazados a un carácter comodín o localhost en la máquina virtual WSL 2 deben poder conectarse desde el host a través de localhost: Port.</span><span class="sxs-lookup"><span data-stu-id="4da81-324">Boolean specifying if ports bound to wildcard or localhost in the WSL 2 VM should be connectable from the host via localhost:port.</span></span> |
| <span data-ttu-id="4da81-325">kernelCommandLine</span><span class="sxs-lookup"><span data-stu-id="4da81-325">kernelCommandLine</span></span> | <span data-ttu-id="4da81-326">string</span><span class="sxs-lookup"><span data-stu-id="4da81-326">string</span></span> | <span data-ttu-id="4da81-327">En blanco</span><span class="sxs-lookup"><span data-stu-id="4da81-327">Blank</span></span> | <span data-ttu-id="4da81-328">Argumentos adicionales de la línea de comandos del kernel.</span><span class="sxs-lookup"><span data-stu-id="4da81-328">Additional kernel command line arguments.</span></span> |
| <span data-ttu-id="4da81-329">swap</span><span class="sxs-lookup"><span data-stu-id="4da81-329">swap</span></span> | <span data-ttu-id="4da81-330">tamaño</span><span class="sxs-lookup"><span data-stu-id="4da81-330">size</span></span> | <span data-ttu-id="4da81-331">25% de tamaño de memoria en Windows redondeado a los GB más cercanos</span><span class="sxs-lookup"><span data-stu-id="4da81-331">25% of memory size on Windows rounded up to the nearest GB</span></span> | <span data-ttu-id="4da81-332">Cantidad de espacio de intercambio que se va a agregar a la máquina virtual WSL 2, 0 para ningún archivo de intercambio.</span><span class="sxs-lookup"><span data-stu-id="4da81-332">How much swap space to add to the WSL 2 VM, 0 for no swap file.</span></span> |
| <span data-ttu-id="4da81-333">Intercambio</span><span class="sxs-lookup"><span data-stu-id="4da81-333">swapFile</span></span> | <span data-ttu-id="4da81-334">tamaño</span><span class="sxs-lookup"><span data-stu-id="4da81-334">size</span></span> | <span data-ttu-id="4da81-335">%USERPROFILE%\AppData\Local\Temp\swap.vhdx</span><span class="sxs-lookup"><span data-stu-id="4da81-335">%USERPROFILE%\AppData\Local\Temp\swap.vhdx</span></span> | <span data-ttu-id="4da81-336">Una ruta de acceso de Windows absoluta al disco duro virtual de intercambio.</span><span class="sxs-lookup"><span data-stu-id="4da81-336">An absolute Windows path to the swap virtual hard disk.</span></span> |

<span data-ttu-id="4da81-337">Las entradas con el `path` valor deben ser rutas de acceso de Windows con barras diagonales inversas de escape; por ejemplo:`C:\\Temp\\myCustomKernel`</span><span class="sxs-lookup"><span data-stu-id="4da81-337">Entries with the `path` value must be Windows paths with escaped backslashes, e.g: `C:\\Temp\\myCustomKernel`</span></span>

<span data-ttu-id="4da81-338">Las entradas con el `size` valor deben ser de un tamaño seguido de una unidad, por ejemplo, `8GB` o `512MB` .</span><span class="sxs-lookup"><span data-stu-id="4da81-338">Entries with the `size` value must be a size followed by a unit, for example `8GB` or `512MB`.</span></span>