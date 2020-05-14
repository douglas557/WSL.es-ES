---
title: Introducción al Subsistema de Windows para Linux
description: Obtén información sobre el Subsistema de Windows para Linux, las diferentes versiones y las formas en que puedes usarlas.
keywords: BashOnWindows, bash, wsl, windows, subsistemawindows, gnu, linux
ms.date: 05/12/2020
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.localizationpriority: high
ms.openlocfilehash: 90a661c408cacbef95a869ac896a40381120d52e
ms.sourcegitcommit: 1b6191351bbf9e95f3c28fc67abe4bf1bcfd3336
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2020
ms.locfileid: "83270799"
---
# <a name="what-is-the-windows-subsystem-for-linux"></a><span data-ttu-id="7c639-104">¿Qué es el Subsistema de Windows para Linux?</span><span class="sxs-lookup"><span data-stu-id="7c639-104">What is the Windows Subsystem for Linux?</span></span>

<span data-ttu-id="7c639-105">El subsistema de Windows para Linux permite a los desarrolladores ejecutar un entorno de GNU/Linux, incluida la mayoría de herramientas de línea de comandos, utilidades y aplicaciones, directamente en Windows, sin modificar y sin la sobrecarga de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7c639-105">The Windows Subsystem for Linux lets developers run a GNU/Linux environment -- including most command-line tools, utilities, and applications -- directly on Windows, unmodified, without the overhead of a virtual machine.</span></span>

<span data-ttu-id="7c639-106">Se puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="7c639-106">You can:</span></span>

* <span data-ttu-id="7c639-107">Elige tus distribuciones de GNU/Linux favoritas [de Microsoft Store](https://aka.ms/wslstore).</span><span class="sxs-lookup"><span data-stu-id="7c639-107">Choose your favorite GNU/Linux distributions [from the Microsoft Store](https://aka.ms/wslstore).</span></span>
* <span data-ttu-id="7c639-108">Ejecuta herramientas comunes de línea de comandos, como `grep`, `sed`, `awk` u otros archivos binarios ELF-64.</span><span class="sxs-lookup"><span data-stu-id="7c639-108">Run common command-line tools such as `grep`, `sed`, `awk`, or other ELF-64 binaries.</span></span>
* <span data-ttu-id="7c639-109">Ejecuta scripts de shell de Bash y aplicaciones de línea de comandos de GNU/Linux, como:</span><span class="sxs-lookup"><span data-stu-id="7c639-109">Run Bash shell scripts and GNU/Linux command-line applications including:</span></span>  
    * <span data-ttu-id="7c639-110">Herramientas: vim, emacs y tmux. \*Lenguajes: [NodeJS](https://docs.microsoft.com/windows/nodejs/setup-on-wsl2), Javascript, [Python](https://docs.microsoft.com/windows/python/web-frameworks), Ruby, C/C++, C# & F#, Rust, Go, etc. \*Servicios: SSHD, MySQL, Apache, lighttpd, [MongoDB](https://docs.microsoft.com/windows/nodejs/databases) y [PostgreSQL](https://docs.microsoft.com/windows/python/databases).</span><span class="sxs-lookup"><span data-stu-id="7c639-110">Tools: vim, emacs, tmux \*Languages: [NodeJS](https://docs.microsoft.com/windows/nodejs/setup-on-wsl2), Javascript, [Python](https://docs.microsoft.com/windows/python/web-frameworks), Ruby, C/C++, C# & F#, Rust, Go, etc. \*Services: SSHD, MySQL, Apache, lighttpd, [MongoDB](https://docs.microsoft.com/windows/nodejs/databases), [PostgreSQL](https://docs.microsoft.com/windows/python/databases).</span></span>
* <span data-ttu-id="7c639-111">Instala software adicional mediante el administrador de paquetes de distribución de GNU/Linux.</span><span class="sxs-lookup"><span data-stu-id="7c639-111">Install additional software using own GNU/Linux distribution package manager.</span></span>
* <span data-ttu-id="7c639-112">Invoca aplicaciones de Windows mediante un shell de línea de comandos de tipo UNIX.</span><span class="sxs-lookup"><span data-stu-id="7c639-112">Invoke Windows applications using a Unix-like command-line shell.</span></span>
* <span data-ttu-id="7c639-113">Invoca aplicaciones de GNU/Linux en Windows.</span><span class="sxs-lookup"><span data-stu-id="7c639-113">Invoke GNU/Linux applications on Windows.</span></span>

## <a name="what-is-wsl-2"></a><span data-ttu-id="7c639-114">¿Qué es WSL 2?</span><span class="sxs-lookup"><span data-stu-id="7c639-114">What is WSL 2?</span></span>

<span data-ttu-id="7c639-115">WSL 2 es una nueva versión de la arquitectura del Subsistema de Windows para Linux que permite que el Subsistema de Windows para Linux ejecute archivos binarios de ELF64 de Linux en Windows.</span><span class="sxs-lookup"><span data-stu-id="7c639-115">WSL 2 is a new version of the Windows Subsystem for Linux architecture that powers the Windows Subsystem for Linux to run ELF64 Linux binaries on Windows.</span></span> <span data-ttu-id="7c639-116">Sus principales objetivos son **aumentar el rendimiento del sistema de archivos** y agregar **compatibilidad completa con las llamadas del sistema**.</span><span class="sxs-lookup"><span data-stu-id="7c639-116">Its primary goals are to **increase file system performance**, as well as adding **full system call compatibility**.</span></span>

<span data-ttu-id="7c639-117">Esta nueva arquitectura cambia el modo en que estos archivos binarios de Linux interactúan con Windows y con el hardware del equipo, pero proporciona la misma experiencia de usuario que en WSL 1 (la versión disponible de forma general actualmente).</span><span class="sxs-lookup"><span data-stu-id="7c639-117">This new architecture changes how these Linux binaries interact with Windows and your computer's hardware, but still provides the same user experience as in WSL 1 (the current widely available version).</span></span>

<span data-ttu-id="7c639-118">Las distribuciones de Linux individuales se pueden ejecutar con la arquitectura de WSL 1 o WSL 2.</span><span class="sxs-lookup"><span data-stu-id="7c639-118">Individual Linux distributions can be run with either the WSL 1 or WSL 2 architecture.</span></span> <span data-ttu-id="7c639-119">Cada distribución se puede actualizar o degradar en cualquier momento, y puedes ejecutar distribuciones de WSL 1 y WSL 2 en paralelo.</span><span class="sxs-lookup"><span data-stu-id="7c639-119">Each distribution can be upgraded or downgraded at any time and you can run WSL 1 and WSL 2 distributions side by side.</span></span> <span data-ttu-id="7c639-120">WSL 2 usa una arquitectura completamente nueva que aprovecha las ventajas de un kernel de Linux real.</span><span class="sxs-lookup"><span data-stu-id="7c639-120">WSL 2 uses an entirely new architecture that benefits from running a real Linux kernel.</span></span>

## <a name="next-steps"></a><span data-ttu-id="7c639-121">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="7c639-121">Next steps</span></span>

* [<span data-ttu-id="7c639-122">Instalación de WSL 1 y actualización a WSL 2</span><span class="sxs-lookup"><span data-stu-id="7c639-122">Install WSL 1 and update to WSL 2</span></span>](./install-win10.md)

* [<span data-ttu-id="7c639-123">Comparación de WSL 2 con WSL 1</span><span class="sxs-lookup"><span data-stu-id="7c639-123">Compare WSL 2 and WSL 1</span></span>](./compare-versions.md)

* [<span data-ttu-id="7c639-124">Creación de una cuenta de usuario y una contraseña para la nueva distribución de Linux</span><span class="sxs-lookup"><span data-stu-id="7c639-124">Create a user account and password for your new Linux distribution</span></span>](./user-support.md)

* [<span data-ttu-id="7c639-125">Lectura de las preguntas más frecuentes</span><span class="sxs-lookup"><span data-stu-id="7c639-125">Read Frequently Asked Questions</span></span>](./faq.md)

* [<span data-ttu-id="7c639-126">Lectura de las preguntas más frecuentes sobre WSL 2</span><span class="sxs-lookup"><span data-stu-id="7c639-126">Read Frequently Asked Questions about WSL 2</span></span>](./wsl2-faq.md)

* [<span data-ttu-id="7c639-127">Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="7c639-127">Troubleshooting</span></span>](./troubleshooting.md)

* [<span data-ttu-id="7c639-128">Ejecución de comandos de interoperabilidad entre Windows y Linux</span><span class="sxs-lookup"><span data-stu-id="7c639-128">Run interoperability commands between Windows and Linux</span></span>](./interop.md)

* [<span data-ttu-id="7c639-129">Ejecución de configuraciones y comandos de inicio</span><span class="sxs-lookup"><span data-stu-id="7c639-129">Run launch commands and configurations</span></span>](./wsl-config.md)

* [<span data-ttu-id="7c639-130">Configuración de permisos de archivo</span><span class="sxs-lookup"><span data-stu-id="7c639-130">Set up file permissions</span></span>](./file-permissions.md)

* [<span data-ttu-id="7c639-131">Configuración de WSL para empresas</span><span class="sxs-lookup"><span data-stu-id="7c639-131">Set up WSL for Enterprise</span></span>](./enterprise.md)

* [<span data-ttu-id="7c639-132">Comandos de WSL de referencia</span><span class="sxs-lookup"><span data-stu-id="7c639-132">Reference WSL commands</span></span>](./reference.md)

* [<span data-ttu-id="7c639-133">Compilación de distribuciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="7c639-133">Build a custom distributions</span></span>](./build-custom-distro.md)

* [<span data-ttu-id="7c639-134">Lectura de las notas de la versión de WSL</span><span class="sxs-lookup"><span data-stu-id="7c639-134">Read the WSL Release Notes</span></span>](./release-notes.md)
