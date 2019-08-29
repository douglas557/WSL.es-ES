---
title: Más información sobre el subsistema de Windows para Linux
description: Obtenga más información sobre cómo funciona el subsistema de Windows para Linux.
keywords: BashOnWindows, bash, WSL, Windows, windowssubsystem, GNU, Linux
author: scooley
ms.author: scooley
ms.date: 07/11/2016
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 7c8e3b3f7ec13109485d7efa29739dadc8bfacf7
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122670"
---
# <a name="windows-subsystem-for-linux-documentation"></a><span data-ttu-id="64a36-104">Documentación de subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="64a36-104">Windows Subsystem for Linux Documentation</span></span>

<span data-ttu-id="64a36-105">El subsistema de Windows para Linux permite a los desarrolladores ejecutar un entorno de GNU/Linux, incluidas la mayoría de herramientas de línea de comandos, utilidades y aplicaciones, directamente en Windows, sin modificar, sin la sobrecarga de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="64a36-105">The Windows Subsystem for Linux lets developers run a GNU/Linux environment -- including most command-line tools, utilities, and applications -- directly on Windows, unmodified, without the overhead of a virtual machine.</span></span>  

<span data-ttu-id="64a36-106">Puede:</span><span class="sxs-lookup"><span data-stu-id="64a36-106">You can:</span></span>

1. <span data-ttu-id="64a36-107">Elija sus distribuciones de GNU/Linux favoritas [en el Microsoft Store](https://aka.ms/wslstore).</span><span class="sxs-lookup"><span data-stu-id="64a36-107">Choose your favorite GNU/Linux distributions [from the Microsoft Store](https://aka.ms/wslstore).</span></span>
1. <span data-ttu-id="64a36-108">Ejecute software gratuito de línea de comandos común, `grep`como `sed`, `awk`, u otros binarios de Elf-64.</span><span class="sxs-lookup"><span data-stu-id="64a36-108">Run common command-line free software such as `grep`, `sed`, `awk`, or other ELF-64 binaries.</span></span> 
1. <span data-ttu-id="64a36-109">Ejecutar scripts de Shell de bash y aplicaciones de línea de comandos de GNU/Linux, como:</span><span class="sxs-lookup"><span data-stu-id="64a36-109">Run Bash shell scripts and GNU/Linux command-line applications including:</span></span>  
    * <span data-ttu-id="64a36-110">Herramientas: VIM, Emacs, tmux</span><span class="sxs-lookup"><span data-stu-id="64a36-110">Tools: vim, emacs, tmux</span></span>
    * <span data-ttu-id="64a36-111">Idiomas: JavaScript/node. js, Ruby, Python, C/C++, C# & F#, oxidación, Go, etc.</span><span class="sxs-lookup"><span data-stu-id="64a36-111">Languages: Javascript/node.js, Ruby, Python, C/C++, C# & F#, Rust, Go, etc.</span></span>
    * <span data-ttu-id="64a36-112">Servicios: sshd, MySQL, Apache, lighttpd</span><span class="sxs-lookup"><span data-stu-id="64a36-112">Services: sshd, MySQL, Apache, lighttpd</span></span>
1. <span data-ttu-id="64a36-113">Instale software adicional mediante el administrador de paquetes de distribución de GNU/Linux.</span><span class="sxs-lookup"><span data-stu-id="64a36-113">Install additional software using own GNU/Linux distribution package manager.</span></span>
1. <span data-ttu-id="64a36-114">Invoque aplicaciones de Windows mediante un shell de línea de comandos de tipo UNIX.</span><span class="sxs-lookup"><span data-stu-id="64a36-114">Invoke Windows applications using a Unix-like command-line shell.</span></span>
1. <span data-ttu-id="64a36-115">Invoque aplicaciones GNU/Linux en Windows.</span><span class="sxs-lookup"><span data-stu-id="64a36-115">Invoke GNU/Linux applications on Windows.</span></span>

## <a name="getting-started"></a><span data-ttu-id="64a36-116">Introducción</span><span class="sxs-lookup"><span data-stu-id="64a36-116">Getting Started</span></span>

* [<span data-ttu-id="64a36-117">Instalación de Linux en Windows 10</span><span class="sxs-lookup"><span data-stu-id="64a36-117">Install Linux on Windows 10</span></span>](install-win10.md)
* [<span data-ttu-id="64a36-118">Visite la referencia de comandos</span><span class="sxs-lookup"><span data-stu-id="64a36-118">Visit the command reference</span></span>](reference.md)
* [<span data-ttu-id="64a36-119">Lea las preguntas más frecuentes</span><span class="sxs-lookup"><span data-stu-id="64a36-119">Read frequently asked questions</span></span>](faq.md)

## <a name="team-blogs"></a><span data-ttu-id="64a36-120">Blogs de equipo</span><span class="sxs-lookup"><span data-stu-id="64a36-120">Team Blogs</span></span>
*  [<span data-ttu-id="64a36-121">Información general post con una colección de vídeos y blogs</span><span class="sxs-lookup"><span data-stu-id="64a36-121">Overview post with a collection of videos and blogs</span></span>](https://blogs.msdn.microsoft.com/commandline/learn-about-windows-console-and-windows-subsystem-for-linux-wsl/)
* <span data-ttu-id="64a36-122">[Blog de línea de comandos](https://blogs.msdn.microsoft.com/commandline/) Active</span><span class="sxs-lookup"><span data-stu-id="64a36-122">[Command-Line blog](https://blogs.msdn.microsoft.com/commandline/) (Active)</span></span>
* <span data-ttu-id="64a36-123">[Blog de Windows Subsystem for Linux](https://blogs.msdn.microsoft.com/wsl/) Balance</span><span class="sxs-lookup"><span data-stu-id="64a36-123">[Windows Subsystem for Linux Blog](https://blogs.msdn.microsoft.com/wsl/) (Historical)</span></span>

## <a name="posts--articles"></a><span data-ttu-id="64a36-124">Publicaciones & artículos</span><span class="sxs-lookup"><span data-stu-id="64a36-124">Posts & Articles</span></span>
* [<span data-ttu-id="64a36-125">Ejecutar bash en Ubuntu en Windows</span><span class="sxs-lookup"><span data-stu-id="64a36-125">Run Bash on Ubuntu on Windows</span></span>](https://blogs.windows.com/buildingapps/2016/03/30/run-bash-on-ubuntu-on-windows/)
* [<span data-ttu-id="64a36-126">Los desarrolladores pueden ejecutar archivos binarios de bash y de Ubuntu Linux en modo de Windows 10</span><span class="sxs-lookup"><span data-stu-id="64a36-126">Developers Can Run Bash And Usermode Ubuntu Linux Binaries On Windows 10</span></span>](https://www.hanselman.com/blog/DevelopersCanRunBashShellAndUsermodeUbuntuLinuxBinariesOnWindows10.aspx)
* [<span data-ttu-id="64a36-127">Ubuntu en Windows: userspace de Ubuntu para desarrolladores de Windows</span><span class="sxs-lookup"><span data-stu-id="64a36-127">Ubuntu on Windows – The Ubuntu Userspace for Windows Developers</span></span>](https://insights.ubuntu.com/2016/03/30/ubuntu-on-windows-the-ubuntu-userspace-for-windows-developers/) 

## <a name="provide-feedback"></a><span data-ttu-id="64a36-128">Proporcionar comentarios</span><span class="sxs-lookup"><span data-stu-id="64a36-128">Provide Feedback</span></span>
* [<span data-ttu-id="64a36-129">Seguimiento de problemas de GitHub</span><span class="sxs-lookup"><span data-stu-id="64a36-129">GitHub issue tracker</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
* [<span data-ttu-id="64a36-130">Portal de UserVoice de línea de comandos</span><span class="sxs-lookup"><span data-stu-id="64a36-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
