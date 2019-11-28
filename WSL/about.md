---
title: Más información sobre el subsistema de Windows para Linux
description: Obtén más información sobre el funcionamiento del subsistema de Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, subsistemawindows, gnu, linux
ms.date: 07/11/2016
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: fbb1ce5cf5d5c83e25d0a6a0cece7b70537a44a1
ms.sourcegitcommit: 3be576f946611cf36e27745bdb7c4c52af1b9928
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "74200197"
---
# <a name="windows-subsystem-for-linux-documentation"></a><span data-ttu-id="28981-104">Documentación del subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="28981-104">Windows Subsystem for Linux Documentation</span></span>

<span data-ttu-id="28981-105">El subsistema de Windows para Linux permite a los desarrolladores ejecutar un entorno de GNU/Linux, incluida la mayoría de herramientas de línea de comandos, utilidades y aplicaciones, directamente en Windows, sin modificar y sin la sobrecarga de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="28981-105">The Windows Subsystem for Linux lets developers run a GNU/Linux environment -- including most command-line tools, utilities, and applications -- directly on Windows, unmodified, without the overhead of a virtual machine.</span></span>  

<span data-ttu-id="28981-106">Se puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="28981-106">You can:</span></span>

1. <span data-ttu-id="28981-107">Elige tus distribuciones de GNU/Linux favoritas [de Microsoft Store](https://aka.ms/wslstore).</span><span class="sxs-lookup"><span data-stu-id="28981-107">Choose your favorite GNU/Linux distributions [from the Microsoft Store](https://aka.ms/wslstore).</span></span>
1. <span data-ttu-id="28981-108">Ejecuta software gratuito de línea de comandos común, como `grep`, `sed`, `awk` u otros archivos binarios ELF-64.</span><span class="sxs-lookup"><span data-stu-id="28981-108">Run common command-line free software such as `grep`, `sed`, `awk`, or other ELF-64 binaries.</span></span> 
1. <span data-ttu-id="28981-109">Ejecuta scripts de shell de Bash y aplicaciones de línea de comandos de GNU/Linux, como:</span><span class="sxs-lookup"><span data-stu-id="28981-109">Run Bash shell scripts and GNU/Linux command-line applications including:</span></span>  
    * <span data-ttu-id="28981-110">Herramientas: vim, emacs, tmux.</span><span class="sxs-lookup"><span data-stu-id="28981-110">Tools: vim, emacs, tmux</span></span>
    * <span data-ttu-id="28981-111">Idiomas: Javascript/node.js, Ruby, Python, C/C++, C# & F#, Rust, Go, etc.</span><span class="sxs-lookup"><span data-stu-id="28981-111">Languages: Javascript/node.js, Ruby, Python, C/C++, C# & F#, Rust, Go, etc.</span></span>
    * <span data-ttu-id="28981-112">Servicios: sshd, MySQL, Apache, lighttpd.</span><span class="sxs-lookup"><span data-stu-id="28981-112">Services: sshd, MySQL, Apache, lighttpd</span></span>
1. <span data-ttu-id="28981-113">Instala software adicional mediante el administrador de paquetes de distribución de GNU/Linux.</span><span class="sxs-lookup"><span data-stu-id="28981-113">Install additional software using own GNU/Linux distribution package manager.</span></span>
1. <span data-ttu-id="28981-114">Invoca aplicaciones de Windows mediante un shell de línea de comandos de tipo UNIX.</span><span class="sxs-lookup"><span data-stu-id="28981-114">Invoke Windows applications using a Unix-like command-line shell.</span></span>
1. <span data-ttu-id="28981-115">Invoca aplicaciones de GNU/Linux en Windows.</span><span class="sxs-lookup"><span data-stu-id="28981-115">Invoke GNU/Linux applications on Windows.</span></span>

## <a name="getting-started"></a><span data-ttu-id="28981-116">Introducción</span><span class="sxs-lookup"><span data-stu-id="28981-116">Getting Started</span></span>

* [<span data-ttu-id="28981-117">Instalación de Linux en Windows 10</span><span class="sxs-lookup"><span data-stu-id="28981-117">Install Linux on Windows 10</span></span>](install-win10.md)
* [<span data-ttu-id="28981-118">Visita a la referencia de comandos</span><span class="sxs-lookup"><span data-stu-id="28981-118">Visit the command reference</span></span>](reference.md)
* [<span data-ttu-id="28981-119">Preguntas más frecuentes</span><span class="sxs-lookup"><span data-stu-id="28981-119">Read frequently asked questions</span></span>](faq.md)

## <a name="team-blogs"></a><span data-ttu-id="28981-120">Blogs del equipo</span><span class="sxs-lookup"><span data-stu-id="28981-120">Team Blogs</span></span>
*  [<span data-ttu-id="28981-121">Publicación de información general con una colección de vídeos y blogs</span><span class="sxs-lookup"><span data-stu-id="28981-121">Overview post with a collection of videos and blogs</span></span>](https://blogs.msdn.microsoft.com/commandline/learn-about-windows-console-and-windows-subsystem-for-linux-wsl/)
* <span data-ttu-id="28981-122">[Blog de línea de comandos](https://blogs.msdn.microsoft.com/commandline/) (activo)</span><span class="sxs-lookup"><span data-stu-id="28981-122">[Command-Line blog](https://blogs.msdn.microsoft.com/commandline/) (Active)</span></span>
* <span data-ttu-id="28981-123">[Blog del subsistema de Windows para Linux](https://blogs.msdn.microsoft.com/wsl/) (historial)</span><span class="sxs-lookup"><span data-stu-id="28981-123">[Windows Subsystem for Linux Blog](https://blogs.msdn.microsoft.com/wsl/) (Historical)</span></span>

## <a name="posts--articles"></a><span data-ttu-id="28981-124">Publicaciones y artículos</span><span class="sxs-lookup"><span data-stu-id="28981-124">Posts & Articles</span></span>
* [<span data-ttu-id="28981-125">Ejecución de Bash en Ubuntu en Windows</span><span class="sxs-lookup"><span data-stu-id="28981-125">Run Bash on Ubuntu on Windows</span></span>](https://blogs.windows.com/buildingapps/2016/03/30/run-bash-on-ubuntu-on-windows/)
* [<span data-ttu-id="28981-126">Los desarrolladores pueden ejecutar archivos binarios de Linux de Ubuntu en modo de usuario y Bash en Windows 10</span><span class="sxs-lookup"><span data-stu-id="28981-126">Developers Can Run Bash And Usermode Ubuntu Linux Binaries On Windows 10</span></span>](https://www.hanselman.com/blog/DevelopersCanRunBashShellAndUsermodeUbuntuLinuxBinariesOnWindows10.aspx)
* [<span data-ttu-id="28981-127">Ubuntu en Windows: espacio de usuarios de Ubuntu para desarrolladores de Windows</span><span class="sxs-lookup"><span data-stu-id="28981-127">Ubuntu on Windows – The Ubuntu Userspace for Windows Developers</span></span>](https://insights.ubuntu.com/2016/03/30/ubuntu-on-windows-the-ubuntu-userspace-for-windows-developers/) 

## <a name="provide-feedback"></a><span data-ttu-id="28981-128">Proporcionar comentarios</span><span class="sxs-lookup"><span data-stu-id="28981-128">Provide Feedback</span></span>
* [<span data-ttu-id="28981-129">Seguimiento de problemas de GitHub</span><span class="sxs-lookup"><span data-stu-id="28981-129">GitHub issue tracker</span></span>](https://github.com/Microsoft/BashOnWindows/issues)

