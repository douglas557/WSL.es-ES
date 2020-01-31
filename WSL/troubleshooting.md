---
title: Solucionar problemas del subsistema de Windows para Linux
description: Proporciona información detallada sobre los errores comunes y los problemas que se presentan a las personas cuando ejecutan Linux en el subsistema de Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, subsistemawindows, ubuntu
ms.date: 01/20/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: ec456c314ac4a1588ccb5c1aa35e22a2d33a39b0
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520534"
---
# <a name="troubleshooting-windows-subsystem-for-linux"></a><span data-ttu-id="430cd-104">Solucionar problemas del subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="430cd-104">Troubleshooting Windows Subsystem for Linux</span></span>

<span data-ttu-id="430cd-105">Para obtener ayuda para solucionar problemas relacionados con WSL, consulta nuestro repositorio de GitHub:</span><span class="sxs-lookup"><span data-stu-id="430cd-105">For support with issues related to WSL, please see our GitHub repo:</span></span>

## <a name="search-for-any-existing-issues-related-to-your-problem"></a><span data-ttu-id="430cd-106">Búsqueda de cualquier problema existente relacionado con tu problema</span><span class="sxs-lookup"><span data-stu-id="430cd-106">Search for any existing issues related to your problem</span></span>

<span data-ttu-id="430cd-107">Si tienes problemas técnicos, usa el repositorio de productos: https://github.com/Microsoft/wsl/issues.</span><span class="sxs-lookup"><span data-stu-id="430cd-107">For technical issues, use the product repo: https://github.com/Microsoft/wsl/issues</span></span>

<span data-ttu-id="430cd-108">Si tienes problemas relacionados con el contenido de esta documentación, usa el repositorio de documentos: https://github.com/MicrosoftDocs/wsl/issues.</span><span class="sxs-lookup"><span data-stu-id="430cd-108">For issues related to the contents of this documentation, use the docs repo: https://github.com/MicrosoftDocs/wsl/issues</span></span>

## <a name="submit-a-bug-report"></a><span data-ttu-id="430cd-109">Envío de un informe de error</span><span class="sxs-lookup"><span data-stu-id="430cd-109">Submit a bug report</span></span>

<span data-ttu-id="430cd-110">Para obtener información sobre errores relacionados con las funciones o características de WSL, presenta los detalles del problema en el repositorio del producto: https://github.com/Microsoft/wsl/issues.</span><span class="sxs-lookup"><span data-stu-id="430cd-110">For bugs related to WSL functions or features, file an issue in the product repo: https://github.com/Microsoft/wsl/issues</span></span>

## <a name="submit-a-feature-request"></a><span data-ttu-id="430cd-111">Envío de una solicitud de característica</span><span class="sxs-lookup"><span data-stu-id="430cd-111">Submit a feature request</span></span>

<span data-ttu-id="430cd-112">Para solicitar una nueva característica relacionada con la funcionalidad o compatibilidad de WSL, presenta los detalles del problema en el repositorio del producto: https://github.com/Microsoft/wsl/issues.</span><span class="sxs-lookup"><span data-stu-id="430cd-112">To request a new feature related to WSL functionality or compatibility, file an issue in the product repo: https://github.com/Microsoft/wsl/issues</span></span>

## <a name="contribute-to-the-docs"></a><span data-ttu-id="430cd-113">Contribuir a los documentos</span><span class="sxs-lookup"><span data-stu-id="430cd-113">Contribute to the docs</span></span>

<span data-ttu-id="430cd-114">Para contribuir a la documentación de WSL, envía una solicitud de incorporación de cambios en el repositorio de documentos: https://github.com/MicrosoftDocs/wsl/issues.</span><span class="sxs-lookup"><span data-stu-id="430cd-114">To contribute to the WSL documentation, submit a pull request in the docs repo: https://github.com/MicrosoftDocs/wsl/issues</span></span>

## <a name="terminal-or-command-line"></a><span data-ttu-id="430cd-115">Terminal o línea de comandos</span><span class="sxs-lookup"><span data-stu-id="430cd-115">Terminal or Command Line</span></span>

<span data-ttu-id="430cd-116">Por último, si tu problema está relacionado con el Terminal Windows, la consola de Windows o la interfaz de usuario de la línea de comandos, usa el repositorio del Terminal Windows: https://github.com/microsoft/terminal.</span><span class="sxs-lookup"><span data-stu-id="430cd-116">Lastly, if your issue is related to the Windows Terminal, Windows Console, or the command-line UI, use the Windows terminal repo: https://github.com/microsoft/terminal</span></span>

## <a name="common-issues"></a><span data-ttu-id="430cd-117">Problemas comunes</span><span class="sxs-lookup"><span data-stu-id="430cd-117">Common issues</span></span>

### <a name="bash-loses-network-connectivity-once-connected-to-a-vpn"></a><span data-ttu-id="430cd-118">Bash pierde la conectividad de red una vez que se conecta a una VPN</span><span class="sxs-lookup"><span data-stu-id="430cd-118">Bash loses network connectivity once connected to a VPN</span></span>

<span data-ttu-id="430cd-119">Si después de conectarte a una VPN en Windows, Bash pierde la conectividad de red, prueba esta solución desde dentro de Bash.</span><span class="sxs-lookup"><span data-stu-id="430cd-119">If after connecting to a VPN on Windows, bash loses network connectivity, try this workaround from within bash.</span></span> <span data-ttu-id="430cd-120">Esta solución alternativa te permitirá invalidar manualmente la resolución de DNS a través de `/etc/resolv.conf`.</span><span class="sxs-lookup"><span data-stu-id="430cd-120">This workaround will allow you to manually override the DNS resolution through `/etc/resolv.conf`.</span></span>

1. <span data-ttu-id="430cd-121">Toma nota del servidor DNS de la VPN con `ipconfig.exe /all`</span><span class="sxs-lookup"><span data-stu-id="430cd-121">Take a note of the DNS server of the VPN from doing `ipconfig.exe /all`</span></span>
2. <span data-ttu-id="430cd-122">Haz una copia del resolv.conf existente `sudo cp /etc/resolv.conf /etc/resolv.conf.new`</span><span class="sxs-lookup"><span data-stu-id="430cd-122">Make a copy of the existing resolv.conf `sudo cp /etc/resolv.conf /etc/resolv.conf.new`</span></span>
3. <span data-ttu-id="430cd-123">Desvincula el elemento resolv.com actual `sudo unlink /etc/resolv.conf`</span><span class="sxs-lookup"><span data-stu-id="430cd-123">Unlink the current resolv.conf `sudo unlink /etc/resolv.conf`</span></span>
4. `sudo mv /etc/resolv.conf.new /etc/resolv.conf`
5. <span data-ttu-id="430cd-124">Abre `/etc/resolv.conf` y</span><span class="sxs-lookup"><span data-stu-id="430cd-124">Open `/etc/resolv.conf` and</span></span> <br/>
   <span data-ttu-id="430cd-125">a.</span><span class="sxs-lookup"><span data-stu-id="430cd-125">a.</span></span> <span data-ttu-id="430cd-126">Elimina la primera línea del archivo, que indica "\# This file was automatically generated by WSL.</span><span class="sxs-lookup"><span data-stu-id="430cd-126">Delete the first line from the file, which says "\# This file was automatically generated by WSL.</span></span> <span data-ttu-id="430cd-127">To stop automatic generation of this file, remove this line" (WSL generó este archivo automáticamente. Para detener la generación automática de este archivo, quita esta línea).</span><span class="sxs-lookup"><span data-stu-id="430cd-127">To stop automatic generation of this file, remove this line.".</span></span> <br/>
   <span data-ttu-id="430cd-128">b.</span><span class="sxs-lookup"><span data-stu-id="430cd-128">b.</span></span> <span data-ttu-id="430cd-129">Agrega la entrada de DNS de (1) anterior como primera entrada de la lista de servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="430cd-129">Add the DNS entry from (1) above as the very first entry in the list of DNS servers.</span></span> <br/>
   <span data-ttu-id="430cd-130">c.</span><span class="sxs-lookup"><span data-stu-id="430cd-130">c.</span></span> <span data-ttu-id="430cd-131">Cierra el archivo.</span><span class="sxs-lookup"><span data-stu-id="430cd-131">Close the file.</span></span> <br/>

<span data-ttu-id="430cd-132">Una vez que hayas desconectado la VPN, tendrás que revertir los cambios a `/etc/resolv.conf`.</span><span class="sxs-lookup"><span data-stu-id="430cd-132">Once you have disconnected the VPN, you will have to revert the changes to `/etc/resolv.conf`.</span></span> <span data-ttu-id="430cd-133">Para ello, haz lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="430cd-133">To do this, do:</span></span>

1. `cd /etc`
2. `sudo mv resolv.conf resolv.conf.new`
3. `sudo ln -s ../run/resolvconf/resolv.conf resolv.conf`

### <a name="starting-wsl-or-installing-a-distribution-returns-an-error-code"></a><span data-ttu-id="430cd-134">Iniciar WSL o instalar una distribución devuelve un código de error</span><span class="sxs-lookup"><span data-stu-id="430cd-134">Starting WSL or installing a distribution returns an error code</span></span>

<span data-ttu-id="430cd-135">Sigue [estas instrucciones](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs) para recopilar registros detallados y registrar un problema en GitHub.</span><span class="sxs-lookup"><span data-stu-id="430cd-135">Follow [these instructions](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs) to collect detailed logs and file an issue on our GitHub.</span></span>

### <a name="updating-bash-on-ubuntu-on-windows"></a><span data-ttu-id="430cd-136">Actualizar Bash en Ubuntu en Windows</span><span class="sxs-lookup"><span data-stu-id="430cd-136">Updating Bash on Ubuntu on Windows</span></span>

<span data-ttu-id="430cd-137">Hay dos componentes de Bash en Ubuntu en Windows que pueden requerir actualización.</span><span class="sxs-lookup"><span data-stu-id="430cd-137">There are two components of Bash on Ubuntu on Windows that can require updating.</span></span>

1. <span data-ttu-id="430cd-138">El subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="430cd-138">The Windows Subsystem for Linux</span></span>
  
   <span data-ttu-id="430cd-139">La actualización de esta parte de Bash en Ubuntu en Windows habilitará las nuevas correcciones en las [notas de la versión](./release-notes.md).</span><span class="sxs-lookup"><span data-stu-id="430cd-139">Upgrading this portion of Bash on Ubuntu on Windows will enable any new fixes outlines in the [release notes](./release-notes.md).</span></span> <span data-ttu-id="430cd-140">Asegúrate de estar suscrito al Programa Windows Insider y de que la compilación esté actualizada.</span><span class="sxs-lookup"><span data-stu-id="430cd-140">Ensure that you are subscribed to the Windows Insider Program and that your build is up to date.</span></span> <span data-ttu-id="430cd-141">Para un control más preciso, incluido el restablecimiento de la instancia de Ubuntu, consulte la [página de referencia de comandos](./reference.md).</span><span class="sxs-lookup"><span data-stu-id="430cd-141">For finer grain control including resetting your Ubuntu instance check out the [command reference page](./reference.md).</span></span>

2. <span data-ttu-id="430cd-142">Los archivos binarios de usuario de Ubuntu</span><span class="sxs-lookup"><span data-stu-id="430cd-142">The Ubuntu user binaries</span></span>

   <span data-ttu-id="430cd-143">Al actualizar esta parte de Bash en Ubuntu en Windows, se instalarán las actualizaciones de los archivos binarios de usuario de Ubuntu, incluidas las aplicaciones que se hayan instalado a través de apt-get.</span><span class="sxs-lookup"><span data-stu-id="430cd-143">Upgrading this portion of Bash on Ubuntu on Windows will install any updates to the Ubuntu user binaries including applications that you have installed via apt-get.</span></span> <span data-ttu-id="430cd-144">Para actualizar, ejecuta los comandos siguientes en Bash:</span><span class="sxs-lookup"><span data-stu-id="430cd-144">To update run the following commands in Bash:</span></span>
  
   1. `apt-get update`
   2. `apt-get upgrade`
  
### <a name="apt-get-upgrade-errors"></a><span data-ttu-id="430cd-145">Errores de actualización de apt-get</span><span class="sxs-lookup"><span data-stu-id="430cd-145">Apt-get upgrade errors</span></span>

<span data-ttu-id="430cd-146">Algunos paquetes usan características que aún no se han implementado.</span><span class="sxs-lookup"><span data-stu-id="430cd-146">Some packages use features that we haven't implemented yet.</span></span> <span data-ttu-id="430cd-147">`udev`, por ejemplo, todavía no se admite y produce varios errores de tipo `apt-get upgrade`.</span><span class="sxs-lookup"><span data-stu-id="430cd-147">`udev`, for example, isn't supported yet and causes several `apt-get upgrade` errors.</span></span>

<span data-ttu-id="430cd-148">Para corregir los problemas relacionados con `udev`, sigue estos pasos:</span><span class="sxs-lookup"><span data-stu-id="430cd-148">To fix issues related to `udev`, follow the following steps:</span></span>

1. <span data-ttu-id="430cd-149">Escribe lo siguiente en `/usr/sbin/policy-rc.d` y guarda los cambios.</span><span class="sxs-lookup"><span data-stu-id="430cd-149">Write the following to `/usr/sbin/policy-rc.d` and save your changes.</span></span>
  
   ``` BASH
   #!/bin/sh
   exit 101
   ```
  
2. <span data-ttu-id="430cd-150">Agrega los permisos de ejecución en `/usr/sbin/policy-rc.d`:</span><span class="sxs-lookup"><span data-stu-id="430cd-150">Add execute permissions to `/usr/sbin/policy-rc.d`:</span></span>

   ``` BASH
   chmod +x /usr/sbin/policy-rc.d
   ```
  
3. <span data-ttu-id="430cd-151">Ejecute los siguientes comandos:</span><span class="sxs-lookup"><span data-stu-id="430cd-151">Run the following commands:</span></span>

   ``` BASH
   dpkg-divert --local --rename --add /sbin/initctl
   ln -s /bin/true /sbin/initctl
   ```
  
### <a name="error-0x80040306-on-installation"></a><span data-ttu-id="430cd-152">"Error: 0x80040306" en la instalación</span><span class="sxs-lookup"><span data-stu-id="430cd-152">"Error: 0x80040306" on installation</span></span>

<span data-ttu-id="430cd-153">Esto se relaciona con el hecho de que no se admite la consola heredada.</span><span class="sxs-lookup"><span data-stu-id="430cd-153">This has to do with the fact that we do not support legacy console.</span></span>
<span data-ttu-id="430cd-154">Para desactivar la consola heredada:</span><span class="sxs-lookup"><span data-stu-id="430cd-154">To turn off legacy console:</span></span>

1. <span data-ttu-id="430cd-155">Abre cmd.exe.</span><span class="sxs-lookup"><span data-stu-id="430cd-155">Open cmd.exe</span></span>
1. <span data-ttu-id="430cd-156">Haz clic con el botón derecho en barra de título -> Propiedades-> desactiva Usar consola heredada.</span><span class="sxs-lookup"><span data-stu-id="430cd-156">Right click title bar -> Properties -> Uncheck Use legacy console</span></span>
1. <span data-ttu-id="430cd-157">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="430cd-157">Click OK</span></span>

### <a name="error-0x80040154-after-windows-update"></a><span data-ttu-id="430cd-158">"Error: 0x80040154" después de una actualización de Windows</span><span class="sxs-lookup"><span data-stu-id="430cd-158">"Error: 0x80040154" after Windows update</span></span>

<span data-ttu-id="430cd-159">La característica Subsistema de Windows para Linux puede deshabilitarse durante una actualización de Windows.</span><span class="sxs-lookup"><span data-stu-id="430cd-159">The Windows Subsystem for Linux feature may be disabled during a Windows update.</span></span> <span data-ttu-id="430cd-160">Si esto ocurre, debes volver a habilitar la característica de Windows.</span><span class="sxs-lookup"><span data-stu-id="430cd-160">If this happens the Windows feature must be re-enabled.</span></span> <span data-ttu-id="430cd-161">Las instrucciones para habilitar el subsistema de Windows para Linux se pueden encontrar en la [guía de instalación](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="430cd-161">Instructions for enabling the Windows Subsystem for Linux can be found in the [Installation Guide](./install-win10.md).</span></span>

### <a name="changing-the-display-language"></a><span data-ttu-id="430cd-162">Cambiar el idioma de visualización</span><span class="sxs-lookup"><span data-stu-id="430cd-162">Changing the display language</span></span>

<span data-ttu-id="430cd-163">La instalación de WSL intentará cambiar automáticamente la configuración regional de Ubuntu para que coincida con la configuración regional de la instalación de Windows.</span><span class="sxs-lookup"><span data-stu-id="430cd-163">WSL install will try to automatically change the Ubuntu locale to match the locale of your Windows install.</span></span>  <span data-ttu-id="430cd-164">Si no quieres que esto pase, puedes ejecutar este comando para cambiar la configuración regional de Ubuntu una vez finalizada la instalación.</span><span class="sxs-lookup"><span data-stu-id="430cd-164">If you do not want this behavior you can run this command to change the Ubuntu locale after install completes.</span></span>  <span data-ttu-id="430cd-165">Ten en cuenta que tendrás que reiniciar bash.exe para que este cambio surta efecto.</span><span class="sxs-lookup"><span data-stu-id="430cd-165">You will have to relaunch bash.exe for this change to take effect.</span></span>

<span data-ttu-id="430cd-166">En el ejemplo siguiente se cambia la configuración regional a en-US:</span><span class="sxs-lookup"><span data-stu-id="430cd-166">The below example changes to locale to en-US:</span></span>

``` BASH
sudo update-locale LANG=en_US.UTF8
```

### <a name="installation-issues-after-windows-system-restore"></a><span data-ttu-id="430cd-167">Problemas de instalación después de una restauración del sistema de Windows</span><span class="sxs-lookup"><span data-stu-id="430cd-167">Installation issues after Windows system restore</span></span>

1. <span data-ttu-id="430cd-168">Elimina la carpeta `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux`.</span><span class="sxs-lookup"><span data-stu-id="430cd-168">Delete the `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux` folder.</span></span> <br/>
  <span data-ttu-id="430cd-169">**Nota: No lo hagas si tu característica opcional está completamente instalada y en funcionamiento.**</span><span class="sxs-lookup"><span data-stu-id="430cd-169">**Note: Do not do this if your optional feature is fully installed and working.**</span></span>
2. <span data-ttu-id="430cd-170">Habilitar la característica opcional WSL (si aún no lo está)</span><span class="sxs-lookup"><span data-stu-id="430cd-170">Enable the WSL optional feature (if not already)</span></span>
3. <span data-ttu-id="430cd-171">Reiniciar</span><span class="sxs-lookup"><span data-stu-id="430cd-171">Reboot</span></span>
4. <span data-ttu-id="430cd-172">lxrun /uninstall /full</span><span class="sxs-lookup"><span data-stu-id="430cd-172">lxrun /uninstall /full</span></span>
5. <span data-ttu-id="430cd-173">Instala bash.</span><span class="sxs-lookup"><span data-stu-id="430cd-173">Install bash</span></span>

### <a name="no-internet-access-in-wsl"></a><span data-ttu-id="430cd-174">Sin acceso a Internet en WSL</span><span class="sxs-lookup"><span data-stu-id="430cd-174">No internet access in WSL</span></span>

<span data-ttu-id="430cd-175">Algunos usuarios han informado de problemas con aplicaciones de firewall específicas que bloquean el acceso a Internet en WSL.</span><span class="sxs-lookup"><span data-stu-id="430cd-175">Some users have reported issues with specific firewall applications blocking internet access in WSL.</span></span>  <span data-ttu-id="430cd-176">Los firewalls que dan error son:</span><span class="sxs-lookup"><span data-stu-id="430cd-176">The firewalls reported are:</span></span>

1. <span data-ttu-id="430cd-177">Kaspersky</span><span class="sxs-lookup"><span data-stu-id="430cd-177">Kaspersky</span></span>
2. <span data-ttu-id="430cd-178">AVG</span><span class="sxs-lookup"><span data-stu-id="430cd-178">AVG</span></span>
3. <span data-ttu-id="430cd-179">Avast</span><span class="sxs-lookup"><span data-stu-id="430cd-179">Avast</span></span>

<span data-ttu-id="430cd-180">En algunos casos, si desactivas el firewall podrás acceder.</span><span class="sxs-lookup"><span data-stu-id="430cd-180">In some cases turning off the firewall allows for access.</span></span>  <span data-ttu-id="430cd-181">En otros casos, simplemente tener instalado el firewall parece bloquear el acceso a Internet.</span><span class="sxs-lookup"><span data-stu-id="430cd-181">In some cases simply having the firewall installed looks to block access.</span></span>

### <a name="permission-denied-error-when-using-ping"></a><span data-ttu-id="430cd-182">Error de permiso denegado al usar ping</span><span class="sxs-lookup"><span data-stu-id="430cd-182">Permission Denied error when using ping</span></span>

<span data-ttu-id="430cd-183">En cuanto a la [Actualización de aniversario de Windows (versión 1607)](./release-notes.md#build-14388-to-windows-10-anniversary-update), es necesario tener **privilegios de administrador** en Windows para ejecutar ping en WSL.</span><span class="sxs-lookup"><span data-stu-id="430cd-183">For [Windows Anniversary Update, version 1607](./release-notes.md#build-14388-to-windows-10-anniversary-update), **administrator privileges** in Windows are required to run ping in WSL.</span></span>  <span data-ttu-id="430cd-184">Para ejecutar ping, ejecuta Bash en Ubuntu en Windows como administrador o ejecuta bash.exe desde un símbolo del sistema de CMD/PowerShell con privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="430cd-184">To run ping, run Bash on Ubuntu on Windows as an administrator, or run bash.exe from a CMD/PowerShell prompt with administrator privileges.</span></span>

<span data-ttu-id="430cd-185">Para versiones posteriores de Windows ([compilación 14926+](./release-notes.md#build-14926)) ya no es necesario tener privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="430cd-185">For later versions of Windows, [Build 14926+](./release-notes.md#build-14926), administrator privileges are no longer required.</span></span>

### <a name="bash-is-hung"></a><span data-ttu-id="430cd-186">Bash se bloquea</span><span class="sxs-lookup"><span data-stu-id="430cd-186">Bash is hung</span></span>

<span data-ttu-id="430cd-187">Si mientras trabajas con Bash, ves que Bash se bloquea (o interbloquea) y no responde a las entradas, ayúdanos a diagnosticar el problema mediante la recopilación y la generación de informes de un volcado de memoria.</span><span class="sxs-lookup"><span data-stu-id="430cd-187">If while working with bash, you find that bash is hung (or deadlocked) and not responding to inputs, help us diagnose the issue by collecting and reporting a memory dump.</span></span> <span data-ttu-id="430cd-188">Ten en cuenta que con estos pasos se bloqueará tu sistema.</span><span class="sxs-lookup"><span data-stu-id="430cd-188">Note that these steps will crash your system.</span></span> <span data-ttu-id="430cd-189">No lo hagas si no te sientes cómodo al hacerlo o guarda el trabajo antes de hacerlo.</span><span class="sxs-lookup"><span data-stu-id="430cd-189">Do not do this if you are not comfortable with that or save your work prior to doing this.</span></span>

<span data-ttu-id="430cd-190">Para recopilar un volcado de memoria</span><span class="sxs-lookup"><span data-stu-id="430cd-190">To collect a memory dump</span></span>

1. <span data-ttu-id="430cd-191">Cambia el tipo de volcado de memoria a "volcado de memoria completa".</span><span class="sxs-lookup"><span data-stu-id="430cd-191">Change the memory dump type to "complete memory dump".</span></span> <span data-ttu-id="430cd-192">Al cambiar el tipo de volcado, toma nota del tipo actual.</span><span class="sxs-lookup"><span data-stu-id="430cd-192">While changing the dump type, take a note of your current type.</span></span>

2. <span data-ttu-id="430cd-193">Sigue los [pasos](https://techcommunity.microsoft.com/t5/Core-Infrastructure-and-Security/How-to-Force-a-Diagnostic-Memory-Dump-When-a-Computer-Hangs/ba-p/257809) para configurar el bloqueo mediante el control de teclado.</span><span class="sxs-lookup"><span data-stu-id="430cd-193">Use the [steps](https://techcommunity.microsoft.com/t5/Core-Infrastructure-and-Security/How-to-Force-a-Diagnostic-Memory-Dump-When-a-Computer-Hangs/ba-p/257809) to configure crash using keyboard control.</span></span>

3. <span data-ttu-id="430cd-194">Reproduce el bloqueo o interbloqueo.</span><span class="sxs-lookup"><span data-stu-id="430cd-194">Repro the hang or deadlock.</span></span>

4. <span data-ttu-id="430cd-195">Bloquea el sistema con la secuencia de claves de (2).</span><span class="sxs-lookup"><span data-stu-id="430cd-195">Crash the system using the key sequence from (2).</span></span>

5. <span data-ttu-id="430cd-196">El sistema se bloqueará y recopilará el volcado de memoria.</span><span class="sxs-lookup"><span data-stu-id="430cd-196">The system will crash and collect the memory dump.</span></span>

6. <span data-ttu-id="430cd-197">Una vez que se reinicie el sistema, informa memory.dmp a secure@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="430cd-197">Once the system reboots, report the memory.dmp to secure@microsoft.com.</span></span> <span data-ttu-id="430cd-198">La ubicación predeterminada del archivo de volcado es %SystemRoot%\memory.dmp o C:\Windows\memory.dmp si C: es la unidad del sistema.</span><span class="sxs-lookup"><span data-stu-id="430cd-198">The default location of the dump file is %SystemRoot%\memory.dmp or C:\Windows\memory.dmp if C: is the system drive.</span></span> <span data-ttu-id="430cd-199">En el correo electrónico, indica que el volcado de memoria es para el equipo de WSL o de Bash en Windows.</span><span class="sxs-lookup"><span data-stu-id="430cd-199">In the email, note that the dump is for the WSL or Bash on Windows team.</span></span>

7. <span data-ttu-id="430cd-200">Restaura el tipo de volcado de memoria a la configuración original.</span><span class="sxs-lookup"><span data-stu-id="430cd-200">Restore the memory dump type to the original setting.</span></span>

### <a name="check-your-build-number"></a><span data-ttu-id="430cd-201">Comprobar el número de compilación</span><span class="sxs-lookup"><span data-stu-id="430cd-201">Check your build number</span></span>

<span data-ttu-id="430cd-202">Para encontrar la arquitectura de tu PC y el número de compilación de Windows, abre:</span><span class="sxs-lookup"><span data-stu-id="430cd-202">To find your PC's architecture and Windows build number, open</span></span>  
<span data-ttu-id="430cd-203">**Configuración** > **Sistema** > **Acerca de**</span><span class="sxs-lookup"><span data-stu-id="430cd-203">**Settings** > **System** > **About**</span></span>

<span data-ttu-id="430cd-204">Busca los campos **Compilación del SO** y **Tipo de sistema**.</span><span class="sxs-lookup"><span data-stu-id="430cd-204">Look for the **OS Build** and **System Type** fields.</span></span>  
    <span data-ttu-id="430cd-205">![Captura de pantalla de los campos Compilación del SO y Tipo de sistema](media/system.png)</span><span class="sxs-lookup"><span data-stu-id="430cd-205">![Screenshot of Build and System Type fields](media/system.png)</span></span>

<span data-ttu-id="430cd-206">Para encontrar el número de compilación de Windows Server, ejecuta lo siguiente en PowerShell:</span><span class="sxs-lookup"><span data-stu-id="430cd-206">To find your Windows Server build number, run the following in PowerShell:</span></span>  

``` PowerShell
systeminfo | Select-String "^OS Name","^OS Version"
```

### <a name="confirm-wsl-is-enabled"></a><span data-ttu-id="430cd-207">Confirmar que WSL está habilitado</span><span class="sxs-lookup"><span data-stu-id="430cd-207">Confirm WSL is enabled</span></span>

<span data-ttu-id="430cd-208">Puedes confirmar que el subsistema de Windows para Linux está habilitado mediante la ejecución de lo siguiente en PowerShell:</span><span class="sxs-lookup"><span data-stu-id="430cd-208">You can confirm that the Windows Subsystem for Linux is enabled by running the following in PowerShell:</span></span>  

``` PowerShell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

### <a name="openssh-server-connection-issues"></a><span data-ttu-id="430cd-209">Problemas de conexión del servidor de OpenSSH</span><span class="sxs-lookup"><span data-stu-id="430cd-209">OpenSSH-Server connection issues</span></span>

<span data-ttu-id="430cd-210">Al intentar conectarte al servidor SSH se produce el error siguiente: "Connection closed by 127.0.0.1 port 22" (Conexión cerrada por 127.0.0.1 puerto 22).</span><span class="sxs-lookup"><span data-stu-id="430cd-210">Trying to connect your SSH server is failed with the following error: "Connection closed by 127.0.0.1 port 22".</span></span>

1. <span data-ttu-id="430cd-211">Asegúrate de que el servidor OpenSSH esté en ejecución:</span><span class="sxs-lookup"><span data-stu-id="430cd-211">Make sure your OpenSSH Server is running:</span></span>

   ``` BASH
   sudo service ssh status
   ```

   <span data-ttu-id="430cd-212">y que has seguido este tutorial: https://help.ubuntu.com/lts/serverguide/openssh-server.html.en</span><span class="sxs-lookup"><span data-stu-id="430cd-212">and you've followed this tutorial: https://help.ubuntu.com/lts/serverguide/openssh-server.html.en</span></span>

2. <span data-ttu-id="430cd-213">Detén el servicio sshd e inicia sshd en modo de depuración:</span><span class="sxs-lookup"><span data-stu-id="430cd-213">Stop the sshd service and start sshd in debug mode:</span></span>

   ``` BASH
   sudo service ssh stop
   sudo /usr/sbin/sshd -d
   ```

3. <span data-ttu-id="430cd-214">Comprueba los registros de inicio y asegúrate de que HostKeys estén disponibles y de no ver mensajes de registro como:</span><span class="sxs-lookup"><span data-stu-id="430cd-214">Check the startup logs and make sure HostKeys are available and you don't see log messages such as:</span></span>

   ```BASH
   debug1: sshd version OpenSSH_7.2, OpenSSL 1.0.2g  1 Mar 2016
   debug1: key_load_private: incorrect passphrase supplied to decrypt private key
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_rsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_dsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_ecdsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_ed25519_key
   ```

<span data-ttu-id="430cd-215">Si ves estos mensajes y faltan las claves en `/etc/ssh/`, tendrás que volver a generar las claves o simplemente purgar e instalar el servidor OpenSSH:</span><span class="sxs-lookup"><span data-stu-id="430cd-215">If you do see such messages and the keys are missing under `/etc/ssh/`, you will have to regenerate the keys or just purge&install openssh-server:</span></span>

```BASH
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```

### <a name="the-referenced-assembly-could-not-be-found-when-enabling-the-wsl-optional-feature"></a><span data-ttu-id="430cd-216">"No se pudo encontrar el ensamblado al que se hace referencia".</span><span class="sxs-lookup"><span data-stu-id="430cd-216">"The referenced assembly could not be found."</span></span> <span data-ttu-id="430cd-217">al habilitar la característica opcional WSL</span><span class="sxs-lookup"><span data-stu-id="430cd-217">when enabling the WSL optional feature</span></span>

<span data-ttu-id="430cd-218">Este error está relacionado con un estado de instalación incorrecta.</span><span class="sxs-lookup"><span data-stu-id="430cd-218">This error is related to being in a bad install state.</span></span> <span data-ttu-id="430cd-219">Complete los pasos siguientes para intentar corregir este problema:</span><span class="sxs-lookup"><span data-stu-id="430cd-219">Please complete the following steps to try and fix this issue:</span></span>

- <span data-ttu-id="430cd-220">Si estás ejecutando el comando para habilitar la característica WSL desde PowerShell, intenta usar la GUI en su lugar desde el menú Inicio: busca "activar o desactivar las características de Windows" y, a continuación, en la lista, selecciona "Subsistema de Windows para Linux", lo que instalará el componente opcional.</span><span class="sxs-lookup"><span data-stu-id="430cd-220">If you are running the enable WSL feature command from PowerShell, try using the GUI instead by opening the start menu, searching for 'Turn Windows features on or off' and then in the list select 'Windows Subsystem for Linux' which will install the optional component.</span></span>

- <span data-ttu-id="430cd-221">Actualiza la versión de Windows. Para ello, ve a Configuración, Actualizaciones y haz clic en "Buscar actualizaciones".</span><span class="sxs-lookup"><span data-stu-id="430cd-221">Update your version of Windows by going to Settings, Updates, and clicking 'Check for Updates'</span></span>

- <span data-ttu-id="430cd-222">Si se produce un error en ambos casos y necesitas acceder a WSL, considera la posibilidad de realizar una actualización local. Para ello, vuelve a instalar Windows 10 con los medios de instalación y selecciona "Conservar todo" para asegurarte de que las aplicaciones y los archivos se conservan.</span><span class="sxs-lookup"><span data-stu-id="430cd-222">If both of those fail and you need to access WSL please consider upgrading in place by reinstalling Windows 10 using installation media and selecting 'Keep Everything' to ensure your apps and files are preserved.</span></span> <span data-ttu-id="430cd-223">Puedes encontrar instrucciones sobre cómo hacerlo en la página [Reinstalar Windows 10](https://support.microsoft.com/help/4000735/windows-10-reinstall).</span><span class="sxs-lookup"><span data-stu-id="430cd-223">You can find instructions on how to do so at the [Reinstall Windows 10 page](https://support.microsoft.com/help/4000735/windows-10-reinstall).</span></span>
