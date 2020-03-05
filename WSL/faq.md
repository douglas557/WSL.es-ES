---
title: Preguntas más frecuentes
description: Preguntas más frecuentes sobre el Subsistema de Windows para Linux.
keywords: BashOnWindows, bash, WSL, Windows, windowssubsystem, p + f
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.localizationpriority: high
ms.openlocfilehash: 5651b0869ff97899a768985ce6efa006afa77a9b
ms.sourcegitcommit: 467b6c8e9716d1a60dbf9f7658fd9579da365b58
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/26/2020
ms.locfileid: "77624939"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a><span data-ttu-id="903dd-104">Preguntas más frecuentes sobre el subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="903dd-104">Frequently Asked Questions about Windows Subsystem for Linux</span></span>

## <a name="what-is-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="903dd-105">¿Qué es el Subsistema de Windows para Linux (WSL)?</span><span class="sxs-lookup"><span data-stu-id="903dd-105">What is Windows Subsystem for Linux (WSL)?</span></span>

<span data-ttu-id="903dd-106">El Subsistema de Windows para Linux (WSL) es una nueva característica de Windows 10 que te permite ejecutar herramientas de línea de comandos nativas de Linux directamente en Windows, junto con el escritorio tradicional de Windows y las aplicaciones modernas de la tienda.</span><span class="sxs-lookup"><span data-stu-id="903dd-106">The Windows Subsystem for Linux (WSL) is a new Windows 10 feature that enables you to run native Linux command-line tools directly on Windows, alongside your traditional Windows desktop and modern store apps.</span></span>

<span data-ttu-id="903dd-107">Consulta la [página Acerca de](./about.md) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="903dd-107">See the [about page](./about.md) for more details.</span></span>

## <a name="who-is-wsl-for"></a><span data-ttu-id="903dd-108">¿Para quién es WSL?</span><span class="sxs-lookup"><span data-stu-id="903dd-108">Who is WSL for?</span></span>

<span data-ttu-id="903dd-109">Esta es principalmente una herramienta para desarrolladores; especialmente para desarrolladores web y para aquellos que trabajan en proyectos de código abierto o con ellos.</span><span class="sxs-lookup"><span data-stu-id="903dd-109">This is primarily a tool for developers -- especially web developers and those who work on or with open source projects.</span></span> <span data-ttu-id="903dd-110">Esto permite a aquellos que quieran o necesiten usar Bash, las herramientas comunes de Linux (`sed`, `awk`, etc.) y varias herramientas de Linux (Ruby, Python, etc.) usar su cadena de herramientas en Windows.</span><span class="sxs-lookup"><span data-stu-id="903dd-110">This allows those who want/need to use Bash, common Linux tools (`sed`, `awk`, etc.) and many Linux-first tools (Ruby, Python, etc.) to use their toolchain on Windows.</span></span>

## <a name="what-can-i-do-with-wsl"></a><span data-ttu-id="903dd-111">¿Qué puedo hacer con WSL?</span><span class="sxs-lookup"><span data-stu-id="903dd-111">What can I do with WSL?</span></span>

<span data-ttu-id="903dd-112">WSL proporciona una aplicación llamada Bash.exe que, cuando se inicia, abre una consola de Windows que ejecuta el shell de Bash.</span><span class="sxs-lookup"><span data-stu-id="903dd-112">WSL provides an application called Bash.exe that, when started, opens a Windows console running the Bash shell.</span></span> <span data-ttu-id="903dd-113">Con Bash, puedes ejecutar aplicaciones y herramientas de Linux de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="903dd-113">Using Bash, you can run command-line Linux tools and apps.</span></span> <span data-ttu-id="903dd-114">Por ejemplo, escribe `lsb_release -a` y presiona Entrar para ver los detalles de la distribución de Linux que se está ejecutando actualmente:</span><span class="sxs-lookup"><span data-stu-id="903dd-114">For example, type `lsb_release -a` and hit enter; you’ll see details of the Linux distro currently running:</span></span>

![Captura de pantalla de los detalles de distribución](media/distro.png)

<span data-ttu-id="903dd-116">También puedes tener obtener acceso al sistema de archivos de la máquina local desde el shell de Bash de Linux; encontrarás las unidades locales montadas en la carpeta `/mnt`.</span><span class="sxs-lookup"><span data-stu-id="903dd-116">You can also access your local machine’s filesystem from within the Linux Bash shell – you’ll find your local drives mounted under the `/mnt` folder.</span></span> <span data-ttu-id="903dd-117">Por ejemplo, la unidad `C:` se monta en `/mnt/c`:</span><span class="sxs-lookup"><span data-stu-id="903dd-117">For example, your `C:` drive is mounted under `/mnt/c`:</span></span>  

![Captura de pantalla de la unidad C montada](media/ls.png)

## <a name="what-is-bash"></a><span data-ttu-id="903dd-119">¿Qué es Bash?</span><span class="sxs-lookup"><span data-stu-id="903dd-119">What is Bash?</span></span>

<span data-ttu-id="903dd-120">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) es un conocido shell basado en texto, que cuenta con un lenguaje de comandos.</span><span class="sxs-lookup"><span data-stu-id="903dd-120">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) is a popular text-based shell and command-language.</span></span> <span data-ttu-id="903dd-121">Es el shell predeterminado que está incluido en Ubuntu, en otras distribuciones de Linux y en macOS.</span><span class="sxs-lookup"><span data-stu-id="903dd-121">It is the default shell included within Ubuntu and other Linux distros, and in macOS.</span></span> <span data-ttu-id="903dd-122">Los usuarios pueden escribir comandos en un shell para ejecutar scripts o ejecutar comandos y herramientas para realizar varias tareas.</span><span class="sxs-lookup"><span data-stu-id="903dd-122">Users type commands into a shell to execute scripts and/or run commands and tools to accomplish many tasks.</span></span>

## <a name="how-does-this-work"></a><span data-ttu-id="903dd-123">¿Cómo funciona?</span><span class="sxs-lookup"><span data-stu-id="903dd-123">How does this work?</span></span>

<span data-ttu-id="903dd-124">Echa un vistazo a nuestro [blog](https://blogs.msdn.microsoft.com/wsl/); en él detallaremos la tecnología subyacente.</span><span class="sxs-lookup"><span data-stu-id="903dd-124">Check out our [blog](https://blogs.msdn.microsoft.com/wsl/) where we go into detail about the underlying technology.</span></span>

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a><span data-ttu-id="903dd-125">¿Por qué debo usar WSL en lugar de Linux en una VM?</span><span class="sxs-lookup"><span data-stu-id="903dd-125">Why would I use WSL rather than Linux in a VM?</span></span>

<span data-ttu-id="903dd-126">WSL necesita menos recursos (CPU, memoria y almacenamiento) que una máquina virtual completa.</span><span class="sxs-lookup"><span data-stu-id="903dd-126">WSL requires fewer resources (CPU, memory, and storage) than a full virtual machine.</span></span> <span data-ttu-id="903dd-127">Asimismo, WSL también te permite ejecutar aplicaciones y herramientas de línea de comandos de Linux junto con la línea de comandos de Windows, aplicaciones de escritorio y de Store, así como la posibilidad de acceder a los archivos de Windows desde Linux.</span><span class="sxs-lookup"><span data-stu-id="903dd-127">WSL also allows you to run Linux command-line tools and apps alongside your Windows command-line, desktop and store apps, and to access your Windows files from within Linux.</span></span> <span data-ttu-id="903dd-128">Esto te permite usar las aplicaciones de Windows y las herramientas de línea de comandos de Linux en el mismo conjunto de archivos, si así lo deseas.</span><span class="sxs-lookup"><span data-stu-id="903dd-128">This enables you to use Windows apps and Linux command-line tools on the same set of files if you wish.</span></span>

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a><span data-ttu-id="903dd-129">¿Por qué debo usar, por ejemplo, Ruby en Linux en lugar de en Windows?</span><span class="sxs-lookup"><span data-stu-id="903dd-129">Why would I use, for example, Ruby on Linux instead of on Windows?</span></span>

<span data-ttu-id="903dd-130">Algunas herramientas multiplataforma se crearon suponiendo que el entorno en el que se ejecutan se comporta como Linux.</span><span class="sxs-lookup"><span data-stu-id="903dd-130">Some cross-platform tools were built assuming that the environment in which they run behaves like Linux.</span></span> <span data-ttu-id="903dd-131">Por ejemplo, algunas herramientas suponen que pueden obtener acceso a rutas de acceso de archivos muy largas o que existen archivos o carpetas específicos.</span><span class="sxs-lookup"><span data-stu-id="903dd-131">For example, some tools assume that they are able to access very long file paths or that specific files/folders exist.</span></span> <span data-ttu-id="903dd-132">Esto suele provocar problemas en Windows, que a menudo se comporta de forma diferente de Linux.</span><span class="sxs-lookup"><span data-stu-id="903dd-132">This often causes problems on Windows which often behaves differently from Linux.</span></span>

<span data-ttu-id="903dd-133">Muchos lenguajes como Ruby y Node a menudo se trasladan a Windows y se ejecutan de manera excelente.</span><span class="sxs-lookup"><span data-stu-id="903dd-133">Many languages like Ruby and node are often ported to, and run great, on Windows.</span></span> <span data-ttu-id="903dd-134">Sin embargo, no todos los propietarios de bibliotecas Ruby Gem o node/NPM portan sus bibliotecas para que admitan Windows, y muchas tienen dependencias específicas de Linux.</span><span class="sxs-lookup"><span data-stu-id="903dd-134">However, not all of the Ruby Gem or node/NPM library owners port their libraries to support Windows, and many have Linux-specific dependencies.</span></span> <span data-ttu-id="903dd-135">Esto a menudo puede dar como resultado que los sistemas que se crearon con herramientas y bibliotecas de este tipo sufran errores de compilación y, a veces, del entorno de ejecución o tengan comportamientos no deseados en Windows.</span><span class="sxs-lookup"><span data-stu-id="903dd-135">This can often result in systems built using such tools and libraries suffering from build and sometimes runtime errors or unwanted behaviors on Windows.</span></span>

<span data-ttu-id="903dd-136">Estos son solo algunos de los problemas que han provocado que muchas personas pidan a Microsoft que mejore las herramientas de línea de comandos de Windows, lo que nos llevó a asociarnos con Canonical para permitir que las herramientas de línea de comandos nativas de Bash y Linux se ejecuten en Windows.</span><span class="sxs-lookup"><span data-stu-id="903dd-136">These are just some of issues that caused many people to ask Microsoft to improve Windows’ command-line tools and what drove us to partner with Canonical to enable native Bash and Linux command-line tools to run on Windows.</span></span>

## <a name="what-does-this-mean-for-powershell"></a><span data-ttu-id="903dd-137">¿Qué significa esto para PowerShell?</span><span class="sxs-lookup"><span data-stu-id="903dd-137">What does this mean for PowerShell?</span></span>

<span data-ttu-id="903dd-138">Al trabajar con proyectos de OSS, existen numerosos escenarios en los que es enormemente útil usar Bash desde un símbolo del sistema de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="903dd-138">While working with OSS projects, there are numerous scenarios where it’s immensely useful to drop into Bash from a PowerShell prompt.</span></span> <span data-ttu-id="903dd-139">La compatibilidad con Bash es complementaria y fortalece el valor de la línea de comandos en Windows, permitiendo que PowerShell y la comunidad de PowerShell aprovechen otras tecnologías populares.</span><span class="sxs-lookup"><span data-stu-id="903dd-139">Bash support is complementary and strengthens the value of the command-line on Windows, allowing PowerShell and the PowerShell community to leverage other popular technologies.</span></span>

<span data-ttu-id="903dd-140">Puedes leer más en el blog del equipo de PowerShell: [Bash para Windows: por qué es impresionante y qué significa para PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/).</span><span class="sxs-lookup"><span data-stu-id="903dd-140">Read more on the PowerShell team blog -- [Bash for Windows: Why it’s awesome and what it means for PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)</span></span>

## <a name="can-i-run-all-linux-apps-in-wsl"></a><span data-ttu-id="903dd-141">¿Puedo ejecutar TODAS las aplicaciones de Linux en WSL?</span><span class="sxs-lookup"><span data-stu-id="903dd-141">Can I run ALL Linux apps in WSL?</span></span>

<span data-ttu-id="903dd-142">No.</span><span class="sxs-lookup"><span data-stu-id="903dd-142">No!</span></span> <span data-ttu-id="903dd-143">WSL es una herramienta destinada a permitir que los usuarios que necesitan esas aplicaciones puedan ejecutar Bash y las principales herramientas de línea de comandos de Linux en Windows.</span><span class="sxs-lookup"><span data-stu-id="903dd-143">WSL is a tool aimed at enabling users who need them to run Bash and core Linux command-line tools on Windows.</span></span>

<span data-ttu-id="903dd-144">WSL **no** tiene como objetivo admitir aplicaciones o escritorios de GUI (por ejemplo, Gnome, KDE, etc.).</span><span class="sxs-lookup"><span data-stu-id="903dd-144">WSL does **not** aim to support GUI desktops or applications (e.g. Gnome, KDE, etc.)</span></span>  

<span data-ttu-id="903dd-145">Asimismo, aunque puedas ejecutar varias aplicaciones de servidor populares (por ejemplo, Redis), no recomendamos WSL para hospedar servicios de producción, ya que Microsoft ofrece una variedad de soluciones para ejecutar cargas de trabajo de Linux en Azure, Hyper-V y Docker.</span><span class="sxs-lookup"><span data-stu-id="903dd-145">Also, even though you will be able to run many popular server applications (e.g. Redis), we do not recommend WSL for hosting production services – Microsoft offers a variety of solutions for running production Linux workloads in Azure, Hyper-V, and Docker.</span></span> 

## <a name="what-windows-skus-is-wsl-included-in"></a><span data-ttu-id="903dd-146">¿En qué SKU de Windows está incluido WSL?</span><span class="sxs-lookup"><span data-stu-id="903dd-146">What Windows SKUs is WSL included in?</span></span>

<span data-ttu-id="903dd-147">El Subsistema de Windows para Linux está disponible en la versión de escritorio de Windows para las versiones de Actualización de aniversario de Windows 10 y Creators Update, o posteriores.</span><span class="sxs-lookup"><span data-stu-id="903dd-147">Windows Subsystem for Linux is available on the desktop version of Windows for Windows 10 Anniversary and Creators update or later.</span></span>

<span data-ttu-id="903dd-148">A partir de la versión de Fall Creators Update, WSL estará disponible en las SKU de escritorio y servidor de Windows.</span><span class="sxs-lookup"><span data-stu-id="903dd-148">Beginning in the Fall Creators update WSL will be available on both the desktop and server SKUs of Windows.</span></span>

## <a name="what-processors-does-wsl-support"></a><span data-ttu-id="903dd-149">¿Qué procesadores admite WSL?</span><span class="sxs-lookup"><span data-stu-id="903dd-149">What processors does WSL support?</span></span>

<span data-ttu-id="903dd-150">WSL admite las CPU x64 y ARM.</span><span class="sxs-lookup"><span data-stu-id="903dd-150">WSL supports x64 and ARM CPUs.</span></span>

## <a name="how-do-i-access-my-c-drive"></a><span data-ttu-id="903dd-151">¿Cómo accedo a la unidad C:?</span><span class="sxs-lookup"><span data-stu-id="903dd-151">How do I access my C: drive?</span></span>

<span data-ttu-id="903dd-152">Los puntos de montaje de los discos duros en la máquina local se crean automáticamente y proporcionan un fácil acceso al sistema de archivos de Windows.</span><span class="sxs-lookup"><span data-stu-id="903dd-152">Mount points for hard drives on the local machine are automatically created and provide easy access to the Windows filesystem.</span></span>

<span data-ttu-id="903dd-153">**/mnt/\<letra de unidad>/**</span><span class="sxs-lookup"><span data-stu-id="903dd-153">**/mnt/\<drive letter>/**</span></span>

<span data-ttu-id="903dd-154">Un ejemplo de uso sería `cd /mnt/c` para acceder a c:</span><span class="sxs-lookup"><span data-stu-id="903dd-154">Example usage would be `cd /mnt/c` to access c:</span></span>\

## <a name="how-do-i-set-up-git-credential-manager-how-do-i-use-my-windows-git-permissions-in-wsl"></a><span data-ttu-id="903dd-155">¿Qué debo hacer para instalar el Administrador de credenciales de GIT?</span><span class="sxs-lookup"><span data-stu-id="903dd-155">How do I set up Git Credential Manager?</span></span> <span data-ttu-id="903dd-156">(¿Cómo puedo usar mis permisos de GIT de Windows en WSL?)</span><span class="sxs-lookup"><span data-stu-id="903dd-156">(How do I use my Windows Git permissions in WSL?)</span></span> 

<span data-ttu-id="903dd-157">El Administrador de credenciales de GIT le permite autenticar un servidor GIT remoto, aunque tenga un patrón de autenticación complejo como Azure Active Directory o la autenticación en dos fases.</span><span class="sxs-lookup"><span data-stu-id="903dd-157">Git Credential Manager enables you to authenticate a remote Git server, even if you have a complex authentication pattern like Azure Active Directory or two-factor authentication.</span></span> <span data-ttu-id="903dd-158">El Administrador de credenciales de GIT se integra en el flujo de autenticación para servicios como GitHub y, una vez que se ha autenticado en el proveedor de hospedaje, solicita un nuevo token de autenticación.</span><span class="sxs-lookup"><span data-stu-id="903dd-158">Git Credential Manager integrates into the authentication flow for services like GitHub and, once you're authenticated to your hosting provider, requests a new authentication token.</span></span> <span data-ttu-id="903dd-159">A continuación, almacena el token de forma segura en el Administrador de credenciales de Windows.</span><span class="sxs-lookup"><span data-stu-id="903dd-159">It then stores the token securely in the Windows Credential Manager.</span></span> <span data-ttu-id="903dd-160">Después de la primera vez, puede usar GIT para comunicarse con el proveedor de hospedaje sin necesidad de volver a autenticarse.</span><span class="sxs-lookup"><span data-stu-id="903dd-160">After the first time, you can use git to talk to your hosting provider without needing to re-authenticate.</span></span> <span data-ttu-id="903dd-161">Solo accederá al token en el Administrador de credenciales de Windows.</span><span class="sxs-lookup"><span data-stu-id="903dd-161">It will just access the token in the Windows Credential Manager.</span></span>

<span data-ttu-id="903dd-162">Para configurar el Administrador de credenciales de GIT para su uso con una distribución de WSL, abra la distribución y escriba este comando:</span><span class="sxs-lookup"><span data-stu-id="903dd-162">To set up Git Credential Manager for use with a WSL distribution, open your distribution and enter this command:</span></span>

```Bash
git config --global credential.helper "/mnt/c/Program\ Files/Git/mingw64/libexec/git-core/git-credential-manager.exe"
```

<span data-ttu-id="903dd-163">Ahora, cualquier operación de GIT que realice dentro de la distribución de WSL usará el Administrador de credenciales.</span><span class="sxs-lookup"><span data-stu-id="903dd-163">Now any git operation you perform within your WSL distribution will use the credential manager.</span></span> <span data-ttu-id="903dd-164">Si ya tiene credenciales almacenadas en caché para un host, accederá a estas desde el Administrador de credenciales.</span><span class="sxs-lookup"><span data-stu-id="903dd-164">If you already have credentials cached for a host, it will access them from the credential manager.</span></span> <span data-ttu-id="903dd-165">Si no es así, recibirá una respuesta de diálogo que le solicitará sus credenciales, aunque esté en una consola Linux.</span><span class="sxs-lookup"><span data-stu-id="903dd-165">If not, you'll receive a dialog response requesting your credentials, even if you're in a Linux console.</span></span>

<span data-ttu-id="903dd-166">Esta compatibilidad se basa en la interoperabilidad de [ entre el Subsistema de Windows para Linux y Windows propiamente](https://docs.microsoft.com/windows/wsl/interop).</span><span class="sxs-lookup"><span data-stu-id="903dd-166">This support relies on the [interoperability between Windows Subsystem for Linux and Windows itself](https://docs.microsoft.com/windows/wsl/interop).</span></span>

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a><span data-ttu-id="903dd-167">¿Cómo uso un archivo de Windows con una aplicación de Linux?</span><span class="sxs-lookup"><span data-stu-id="903dd-167">How do I use a Windows file with a Linux app?</span></span>

<span data-ttu-id="903dd-168">Uno de los beneficios de WSL es que puedes acceder a tus archivos mediante aplicaciones o herramientas de Windows y Linux.</span><span class="sxs-lookup"><span data-stu-id="903dd-168">One of the benefits of WSL is being able to access your files via both Windows and Linux apps or tools.</span></span> 

<span data-ttu-id="903dd-169">WSL monta las unidades fijas de la máquina que están en la carpeta `/mnt/<drive>` en tus distribuciones de Linux.</span><span class="sxs-lookup"><span data-stu-id="903dd-169">WSL mounts your machine's fixed drives under the `/mnt/<drive>` folder in your Linux distros.</span></span> <span data-ttu-id="903dd-170">Por ejemplo, la unidad `C:` se monta en `/mnt/c/`</span><span class="sxs-lookup"><span data-stu-id="903dd-170">For example, your `C:` drive is mounted under `/mnt/c/`</span></span>

<span data-ttu-id="903dd-171">Si usas tus unidades montadas, puedes editar el código (por ejemplo, `C:\dev\myproj\` usando [Visual Studio](https://visualstudio.microsoft.com/vs/) / o [VS Code](https://code.visualstudio.com/)) y compilar o probar ese código en Linux accediendo a los mismos archivos a través de `/mnt/c/dev/myproj`.</span><span class="sxs-lookup"><span data-stu-id="903dd-171">Using your mounted drives, you can edit code in, for example, `C:\dev\myproj\` using [Visual Studio](https://visualstudio.microsoft.com/vs/) / or [VS Code](https://code.visualstudio.com/), and build/test that code in Linux by accessing the same files via `/mnt/c/dev/myproj`.</span></span>

> <span data-ttu-id="903dd-172">**NOTA IMPORTANTE**: Una de las limitaciones principales del uso de WSL es que no se admite el acceso o cambio directo de archivos en el sistema de archivos de tus distribuciones de Linux mediante aplicaciones o herramientas de Windows.</span><span class="sxs-lookup"><span data-stu-id="903dd-172">**IMPORTANT NOTE**: One of the key limitations of using WSL is that directly accessing/changing files in your Linux distros' filesystem using Windows apps or tools is not supported.</span></span> <span data-ttu-id="903dd-173">Vea: [No cambies los archivos de Linux con las aplicaciones y herramientas de Windows](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span><span class="sxs-lookup"><span data-stu-id="903dd-173">See: [Do not change Linux files using Windows apps and tools](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span></span>

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a><span data-ttu-id="903dd-174">¿Los archivos de la unidad de Linux son diferentes de la unidad de Windows montada?</span><span class="sxs-lookup"><span data-stu-id="903dd-174">Are files in the Linux drive different from the mounted Windows drive?</span></span>

1. <span data-ttu-id="903dd-175">Los archivos que se encuentran en la raíz de Linux (por ejemplo , `/`) se controlan mediante WSL, que imita el comportamiento específico de Linux, incluyendo, entre otros, los siguientes:</span><span class="sxs-lookup"><span data-stu-id="903dd-175">Files under the Linux root (i.e. `/`) are controlled by WSL which mimics Linux specific behavior, including but not limited to:</span></span>
   * <span data-ttu-id="903dd-176">Archivos que contienen caracteres de nombre de archivo de Windows que no son válidos</span><span class="sxs-lookup"><span data-stu-id="903dd-176">Files which contain invalid Windows filename characters</span></span>
   * <span data-ttu-id="903dd-177">Vínculos simbólicos creados para usuarios que no son administradores</span><span class="sxs-lookup"><span data-stu-id="903dd-177">Symlinks created for non-admin users</span></span>
   * <span data-ttu-id="903dd-178">La opción de cambiar atributos de archivo a través de chmod y chown</span><span class="sxs-lookup"><span data-stu-id="903dd-178">Changing file attributes through chmod and chown</span></span>
   * <span data-ttu-id="903dd-179">Distinción de mayúsculas y minúsculas en archivos o carpetas</span><span class="sxs-lookup"><span data-stu-id="903dd-179">File/folder case sensitivity</span></span>

2. <span data-ttu-id="903dd-180">Los archivos de las unidades montadas se controlan mediante Windows y tienen los siguientes comportamientos:</span><span class="sxs-lookup"><span data-stu-id="903dd-180">Files in mounted drives are controlled by Windows and have the following behaviors:</span></span>
   * <span data-ttu-id="903dd-181">Compatibilidad para la distinción de mayúsculas y minúsculas</span><span class="sxs-lookup"><span data-stu-id="903dd-181">Support case sensitivity</span></span>
   * <span data-ttu-id="903dd-182">Todos los permisos se establecen para reflejar mejor los permisos de Windows</span><span class="sxs-lookup"><span data-stu-id="903dd-182">All permissions are set to best reflect the Windows permissions</span></span>

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a><span data-ttu-id="903dd-183">¿Por qué hay tantos errores cuando ejecuto la actualización apt-get?</span><span class="sxs-lookup"><span data-stu-id="903dd-183">Why are there so many errors when I run apt-get upgrade?</span></span>

<span data-ttu-id="903dd-184">Algunos paquetes usan características que aún no se han implementado.</span><span class="sxs-lookup"><span data-stu-id="903dd-184">Some packages use features that we haven't implemented yet.</span></span> <span data-ttu-id="903dd-185">`udev`, por ejemplo, todavía no se admite y produce varios errores de tipo `apt-get upgrade`.</span><span class="sxs-lookup"><span data-stu-id="903dd-185">`udev`, for example, isn't supported yet and causes several `apt-get upgrade` errors.</span></span>

<span data-ttu-id="903dd-186">Para corregir los problemas relacionados con `udev`, sigue estos pasos:</span><span class="sxs-lookup"><span data-stu-id="903dd-186">To fix issues related to `udev`, follow the following steps:</span></span>

1. <span data-ttu-id="903dd-187">Escribe lo siguiente en `/usr/sbin/policy-rc.d` y guarda los cambios.</span><span class="sxs-lookup"><span data-stu-id="903dd-187">Write the following to `/usr/sbin/policy-rc.d` and save your changes.</span></span>

    ```bash
    #!/bin/sh
    exit 101
    ```

2. <span data-ttu-id="903dd-188">Agrega los permisos de ejecución en `/usr/sbin/policy-rc.d`.</span><span class="sxs-lookup"><span data-stu-id="903dd-188">Add execute permissions to `/usr/sbin/policy-rc.d`</span></span>

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
3. <span data-ttu-id="903dd-189">Ejecuta los siguientes comandos:</span><span class="sxs-lookup"><span data-stu-id="903dd-189">Run the following commands</span></span>

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a><span data-ttu-id="903dd-190">¿Cómo desinstalo una distribución de WSL?</span><span class="sxs-lookup"><span data-stu-id="903dd-190">How do I uninstall a WSL Distribution?</span></span>

<span data-ttu-id="903dd-191">En las compilaciones anteriores a 1709 (16299), abre un símbolo del sistema y ejecuta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="903dd-191">On builds prior to 1709 (16299) open a command prompt and run:</span></span>

  ```batchfile
  lxrun /uninstall /full
  ```
  
<span data-ttu-id="903dd-192">Las distribuciones de WSL instaladas desde Store se pueden desinstalar como cualquier otra aplicación de Windows; para ello, haz clic con el botón derecho en el icono de la aplicación y haz clic en Desinstalar; también puedes desinstalarlas a través de PowerShell mediante el cmdlet [`Remove-AppxPackage`](https://technet.microsoft.com/library/hh856038.aspx).</span><span class="sxs-lookup"><span data-stu-id="903dd-192">WSL distributions installed from the store can be uninstalled like any other Windows app, by right-clicking on the app tile and clicking Uninstall, or via PowerShell using the [`Remove-AppxPackage` cmdlet](https://technet.microsoft.com/library/hh856038.aspx).</span></span>

## <a name="why-does-ping-generate-permission-denied-errors"></a><span data-ttu-id="903dd-193">¿Por qué el ping genera errores de tipo "Permiso denegado"?</span><span class="sxs-lookup"><span data-stu-id="903dd-193">Why does ping generate permission denied errors?</span></span>

<span data-ttu-id="903dd-194">En las compilaciones de WSL anteriores a la versión 14926, el ping requería que WSL se ejecutara mediante de una consola con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="903dd-194">In WSL builds < 14926, ping required WSL to run via an elevated Console.</span></span> <span data-ttu-id="903dd-195">Este problema se corrigió en la compilación 14926 y en versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="903dd-195">This issue was fixed in Build 14926 and later.</span></span>

## <a name="how-do-i-run-an-openssh-server"></a><span data-ttu-id="903dd-196">¿Cómo ejecuto un servidor OpenSSH?</span><span class="sxs-lookup"><span data-stu-id="903dd-196">How do I run an OpenSSH server?</span></span>

<span data-ttu-id="903dd-197">Se requieren privilegios de administrador en Windows para ejecutar OpenSSH en WSL.</span><span class="sxs-lookup"><span data-stu-id="903dd-197">Administrator privileges in Windows are required to run OpenSSH in WSL.</span></span> <span data-ttu-id="903dd-198">Para ejecutar un servidor OpenSSH, ejecuta Bash en Ubuntu en Windows como administrador o ejecuta Bash.exe desde un símbolo del sistema de CMD/PowerShell con privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="903dd-198">To run an OpenSSH server, run Bash on Ubuntu on Windows as an administrator, or run bash.exe from a CMD/PowerShell prompt with administrator privileges.</span></span>

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a><span data-ttu-id="903dd-199">¿Por qué obtengo el mensaje "Error: 0x80040306 " cuándo intento realizar la instalación?</span><span class="sxs-lookup"><span data-stu-id="903dd-199">Why do I get "Error: 0x80040306" when I try to install?</span></span>

<span data-ttu-id="903dd-200">WSL no se puede ejecutar en una consola heredada.</span><span class="sxs-lookup"><span data-stu-id="903dd-200">WSL does not support running in a legacy console.</span></span> <span data-ttu-id="903dd-201">Para desactivar la consola heredada:</span><span class="sxs-lookup"><span data-stu-id="903dd-201">To turn off legacy console:</span></span>

1. <span data-ttu-id="903dd-202">Abre WSL, PowerShell o CMD.</span><span class="sxs-lookup"><span data-stu-id="903dd-202">Open WSL, PowerShell, or Cmd</span></span>
1. <span data-ttu-id="903dd-203">Haz clic con el botón derecho en barra de título -> Propiedades-> y desactiva "Usar consola heredada".</span><span class="sxs-lookup"><span data-stu-id="903dd-203">Right click title bar -> Properties -> Uncheck "Use legacy console"</span></span>
1. <span data-ttu-id="903dd-204">Haga clic en Aceptar</span><span class="sxs-lookup"><span data-stu-id="903dd-204">Click OK</span></span>

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a><span data-ttu-id="903dd-205">¿Por qué obtengo el mensaje "Error: 0x80040154 "cuando ejecuto Bash.exe después de actualizar Windows?</span><span class="sxs-lookup"><span data-stu-id="903dd-205">Why do I get "Error: 0x80040154" when I run bash.exe after upgrading Windows?</span></span>

<span data-ttu-id="903dd-206">La característica "Subsistema de Windows para Linux" puede estar deshabilitada durante una actualización de Windows.</span><span class="sxs-lookup"><span data-stu-id="903dd-206">The "Windows Subsystem for Linux" feature may be disabled during a Windows update.</span></span> <span data-ttu-id="903dd-207">Si esto ocurre, debes volver a habilitar la característica de Windows.</span><span class="sxs-lookup"><span data-stu-id="903dd-207">If this happens the Windows feature must be re-enabled.</span></span> <span data-ttu-id="903dd-208">Las instrucciones para habilitar la característica "Subsistema de Windows para Linux" se pueden encontrar en la [guía de instalación](https://docs.microsoft.com/windows/wsl/install-win10#install-the-windows-subsystem-for-linux).</span><span class="sxs-lookup"><span data-stu-id="903dd-208">Instructions for enabling the "Windows Subsystem for Linux" feature can be found in the [Installation Guide](https://docs.microsoft.com/windows/wsl/install-win10#install-the-windows-subsystem-for-linux).</span></span>

## <a name="how-do-i-change-the-display-language-of-wsl"></a><span data-ttu-id="903dd-209">¿Cómo cambio el idioma de visualización de WSL?</span><span class="sxs-lookup"><span data-stu-id="903dd-209">How do I change the display language of WSL?</span></span>

<span data-ttu-id="903dd-210">La instalación de WSL intentará cambiar automáticamente la configuración regional de Ubuntu para que coincida con la configuración regional de la instalación de Windows.</span><span class="sxs-lookup"><span data-stu-id="903dd-210">WSL install will try to automatically change the Ubuntu locale to match the locale of your Windows install.</span></span> <span data-ttu-id="903dd-211">Si no quieres que esto pase, puedes ejecutar este comando para cambiar la configuración regional de Ubuntu una vez finalizada la instalación.</span><span class="sxs-lookup"><span data-stu-id="903dd-211">If you do not want this behavior you can run this command to change the Ubuntu locale after install completes.</span></span> <span data-ttu-id="903dd-212">Ten en cuenta que tendrás que reiniciar bash.exe para que este cambio surta efecto.</span><span class="sxs-lookup"><span data-stu-id="903dd-212">You will have to relaunch bash.exe for this change to take effect.</span></span>

<span data-ttu-id="903dd-213">En el ejemplo siguiente se cambia la configuración regional a en-US:</span><span class="sxs-lookup"><span data-stu-id="903dd-213">The below example changes to locale to en-US:</span></span>

```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a><span data-ttu-id="903dd-214">¿Por qué no tengo acceso a Internet desde WSL?</span><span class="sxs-lookup"><span data-stu-id="903dd-214">Why do I not have internet access from WSL?</span></span>

<span data-ttu-id="903dd-215">Algunos usuarios han detectado problemas con aplicaciones de firewall específicas que bloquean el acceso a Internet en WSL.</span><span class="sxs-lookup"><span data-stu-id="903dd-215">Some users have reported issues with specific firewall applications blocking internet access in WSL.</span></span> <span data-ttu-id="903dd-216">Los firewalls que dan error son:</span><span class="sxs-lookup"><span data-stu-id="903dd-216">The firewalls reported are:</span></span>

1. <span data-ttu-id="903dd-217">Kaspersky</span><span class="sxs-lookup"><span data-stu-id="903dd-217">Kaspersky</span></span>
1. <span data-ttu-id="903dd-218">AVG</span><span class="sxs-lookup"><span data-stu-id="903dd-218">AVG</span></span>
1. <span data-ttu-id="903dd-219">Avast</span><span class="sxs-lookup"><span data-stu-id="903dd-219">Avast</span></span>

<span data-ttu-id="903dd-220">En algunos casos, si desactivas el firewall podrás acceder.</span><span class="sxs-lookup"><span data-stu-id="903dd-220">In some cases turning off the firewall allows for access.</span></span> <span data-ttu-id="903dd-221">En otros casos, simplemente tener instalado el firewall parece bloquear el acceso a Internet.</span><span class="sxs-lookup"><span data-stu-id="903dd-221">In some cases simply having the firewall installed looks to block access.</span></span>

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a><span data-ttu-id="903dd-222">¿Cómo obtengo acceso a un puerto desde WSL en Windows?</span><span class="sxs-lookup"><span data-stu-id="903dd-222">How do I access a port from WSL in Windows?</span></span>
<span data-ttu-id="903dd-223">WSL comparte la dirección IP de Windows, ya que se ejecuta en Windows.</span><span class="sxs-lookup"><span data-stu-id="903dd-223">WSL shares the IP address of Windows, as it is running on Windows.</span></span> <span data-ttu-id="903dd-224">Así pues, puedes obtener acceso a cualquier puerto en localhost; por ejemplo, si tienes contenido web en el puerto 1234, puedes obtener acceso https://localhost:1234 al explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="903dd-224">As such you can access any ports on localhost e.g. if you had web content on port 1234 you could https://localhost:1234 into your Windows browser.</span></span>

## <a name="how-can-i-back-up-my-wsl-distros"></a><span data-ttu-id="903dd-225">¿Cómo puedo realizar una copia de seguridad de mi distribución de WSL?</span><span class="sxs-lookup"><span data-stu-id="903dd-225">How can I back up my WSL distros?</span></span>

<span data-ttu-id="903dd-226">La mejor manera de hacer una copia de seguridad de la distribución está disponible en la versión 1809 y en versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="903dd-226">The best way to backup your distros is available in Windows Version 1809 and later.</span></span> <span data-ttu-id="903dd-227">Puedes exportar toda la distribución a un tarball mediante el comando `wsl --export`.</span><span class="sxs-lookup"><span data-stu-id="903dd-227">You can export your entire distribution to a tarball using the `wsl --export` command.</span></span> <span data-ttu-id="903dd-228">A continuación, puedes importar de nuevo esta distribución en WSL mediante el comando `wsl --import`, lo que te permitirá realizar copias de seguridad y guardar los estados de las distribuciones de WSL.</span><span class="sxs-lookup"><span data-stu-id="903dd-228">You can then import this distro back into WSL using the `wsl --import` command, allowing you to backup and save states of your WSL distributions.</span></span> 

<span data-ttu-id="903dd-229">Recuerda que los servicios de copia de seguridad tradicionales que copian los archivos de las carpetas AppData (por ejemplo, copias de seguridad de Windows) no dañarán los archivos de Linux.</span><span class="sxs-lookup"><span data-stu-id="903dd-229">Please note that traditional backup services that backup files in your Appdata folders (like Windows Backup) will not corrupt your Linux files.</span></span>

## <a name="where-can-i-provide-feedback"></a><span data-ttu-id="903dd-230">¿Dónde puedo enviar mis comentarios?</span><span class="sxs-lookup"><span data-stu-id="903dd-230">Where can I provide feedback?</span></span>

<span data-ttu-id="903dd-231">Puedes compartir tus comentarios y formular preguntas a través de varios canales.</span><span class="sxs-lookup"><span data-stu-id="903dd-231">You can share feedback and ask questions through multiple channels.</span></span>

<span data-ttu-id="903dd-232">Si tienes problemas técnicos o quieres solicitar nuevas características, visita nuestro seguimiento de problemas de GitHub:</span><span class="sxs-lookup"><span data-stu-id="903dd-232">If you have technical issues, or want to request new features please go to our Github issue tracker:</span></span>

* [<span data-ttu-id="903dd-233">Seguimiento de problemas de GitHub</span><span class="sxs-lookup"><span data-stu-id="903dd-233">GitHub issue tracker</span></span>](https://github.com/Microsoft/BashOnWindows/issues)

<span data-ttu-id="903dd-234">Si quieres mantenerte al día con las últimas noticias de WSL, puedes hacerlo con:</span><span class="sxs-lookup"><span data-stu-id="903dd-234">If you'd like to stay up to date with the latest WSL news you can do so with:</span></span>

* <span data-ttu-id="903dd-235">Nuestro [blog del equipo de línea de comandos](https://blogs.msdn.microsoft.com/commandline/).</span><span class="sxs-lookup"><span data-stu-id="903dd-235">Our [command-line team blog](https://blogs.msdn.microsoft.com/commandline/)</span></span>
* <span data-ttu-id="903dd-236">Twitter.</span><span class="sxs-lookup"><span data-stu-id="903dd-236">Twitter.</span></span> <span data-ttu-id="903dd-237">Sigue [@craigaloewen](https://twitter.com/craigaloewen) en Twitter para conocer las noticias, actualizaciones, etc.</span><span class="sxs-lookup"><span data-stu-id="903dd-237">Please follow [@craigaloewen](https://twitter.com/craigaloewen) on Twitter to learn of news, updates, etc.</span></span>
