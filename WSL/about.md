---
title: Obtenga información sobre el subsistema Windows para Linux
description: Más información sobre cómo funciona el subsistema Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, gnu, linux
author: scooley
ms.author: scooley
ms.date: 07/11/2016
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: High
ms.openlocfilehash: f2df3c06d6c56aa8bc5a41ea9f075635b70c8685
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040809"
---
# <a name="windows-subsystem-for-linux-documentation"></a><span data-ttu-id="eb92b-104">Subsistema de Windows para la documentación de Linux</span><span class="sxs-lookup"><span data-stu-id="eb92b-104">Windows Subsystem for Linux Documentation</span></span>

<span data-ttu-id="eb92b-105">El subsistema de Windows para Linux permite a los desarrolladores ejecutar entorno GNU/Linux, incluidas herramientas, utilidades y aplicaciones de línea de comandos más--directamente en Windows, sin modificar, sin la sobrecarga de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="eb92b-105">The Windows Subsystem for Linux lets developers run GNU/Linux environment -- including most command-line tools, utilities, and applications -- directly on Windows, unmodified, without the overhead of a virtual machine.</span></span>  

<span data-ttu-id="eb92b-106">Se puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="eb92b-106">You can:</span></span>

1. <span data-ttu-id="eb92b-107">Elija sus distribuciones favoritas de GNU/Linux [desde el Store Windows](https://aka.ms/wslstore).</span><span class="sxs-lookup"><span data-stu-id="eb92b-107">Choose your favorite GNU/Linux distributions [from the Windows Store](https://aka.ms/wslstore).</span></span>
1. <span data-ttu-id="eb92b-108">Ejecute el software gratuito de línea de comandos comunes, como `grep`, `sed`, `awk`, o en otros archivos binarios de ELF-64.</span><span class="sxs-lookup"><span data-stu-id="eb92b-108">Run common command-line free software such as `grep`, `sed`, `awk`, or other ELF-64 binaries.</span></span> 
1. <span data-ttu-id="eb92b-109">Ejecutar scripts de shell de Bash y aplicaciones de línea de comandos de GNU/Linux incluidas:</span><span class="sxs-lookup"><span data-stu-id="eb92b-109">Run Bash shell scripts and GNU/Linux command-line applications including:</span></span>  
    * <span data-ttu-id="eb92b-110">Herramientas: vim, emacs, tmux</span><span class="sxs-lookup"><span data-stu-id="eb92b-110">Tools: vim, emacs, tmux</span></span>
    * <span data-ttu-id="eb92b-111">Idiomas: JavaScript/Node.js, Ruby, Python, C o C++, C# & F#, confiar, vaya, etcetera.</span><span class="sxs-lookup"><span data-stu-id="eb92b-111">Languages: Javascript/node.js, Ruby, Python, C/C++, C# & F#, Rust, Go, etc.</span></span>
    * <span data-ttu-id="eb92b-112">Servicios: sshd, MySQL, Apache, lighttpd</span><span class="sxs-lookup"><span data-stu-id="eb92b-112">Services: sshd, MySQL, Apache, lighttpd</span></span>
1. <span data-ttu-id="eb92b-113">Instalar software adicional mediante el propio administrador de paquetes de distribución de GNU/Linux.</span><span class="sxs-lookup"><span data-stu-id="eb92b-113">Install additional software using own GNU/Linux distribution package manager.</span></span>
1. <span data-ttu-id="eb92b-114">Invocar las aplicaciones de Windows con el shell de línea de comandos similares a Unix.</span><span class="sxs-lookup"><span data-stu-id="eb92b-114">Invoke Windows applications using a Unix-like command-line shell.</span></span>
1. <span data-ttu-id="eb92b-115">Invocar las aplicaciones de GNU/Linux en Windows.</span><span class="sxs-lookup"><span data-stu-id="eb92b-115">Invoke GNU/Linux applications on Windows.</span></span>

## <a name="getting-started"></a><span data-ttu-id="eb92b-116">Introducción</span><span class="sxs-lookup"><span data-stu-id="eb92b-116">Getting Started</span></span>

* [<span data-ttu-id="eb92b-117">Instalación de Linux en Windows 10</span><span class="sxs-lookup"><span data-stu-id="eb92b-117">Install Linux on Windows 10</span></span>](install-win10.md)
* [<span data-ttu-id="eb92b-118">Visite la referencia de comandos</span><span class="sxs-lookup"><span data-stu-id="eb92b-118">Visit the command reference</span></span>](reference.md)
* [<span data-ttu-id="eb92b-119">Preguntas más frecuentes de lectura</span><span class="sxs-lookup"><span data-stu-id="eb92b-119">Read frequently asked questions</span></span>](faq.md)

## <a name="team-blogs"></a><span data-ttu-id="eb92b-120">Blogs del equipo</span><span class="sxs-lookup"><span data-stu-id="eb92b-120">Team Blogs</span></span>
*  [<span data-ttu-id="eb92b-121">Información general sobre post con una colección de vídeos y blogs</span><span class="sxs-lookup"><span data-stu-id="eb92b-121">Overview post with a collection of videos and blogs</span></span>](https://blogs.msdn.microsoft.com/commandline/learn-about-windows-console-and-windows-subsystem-for-linux-wsl/)
* <span data-ttu-id="eb92b-122">[Blog de línea de comandos](https://blogs.msdn.microsoft.com/commandline/) (activo)</span><span class="sxs-lookup"><span data-stu-id="eb92b-122">[Command-Line blog](https://blogs.msdn.microsoft.com/commandline/) (Active)</span></span>
* <span data-ttu-id="eb92b-123">[Subsistema de Windows para Linux Blog](https://blogs.msdn.microsoft.com/wsl/) (historial)</span><span class="sxs-lookup"><span data-stu-id="eb92b-123">[Windows Subsystem for Linux Blog](https://blogs.msdn.microsoft.com/wsl/) (Historical)</span></span>

## <a name="posts--articles"></a><span data-ttu-id="eb92b-124">Artículos y publicaciones</span><span class="sxs-lookup"><span data-stu-id="eb92b-124">Posts & Articles</span></span>
* [<span data-ttu-id="eb92b-125">Ejecución de Bash en Ubuntu en Windows</span><span class="sxs-lookup"><span data-stu-id="eb92b-125">Run Bash on Ubuntu on Windows</span></span>](https://blogs.windows.com/buildingapps/2016/03/30/run-bash-on-ubuntu-on-windows/)
* [<span data-ttu-id="eb92b-126">Los desarrolladores pueden ejecutar Bash y archivos binarios de Usermode Ubuntu Linux en Windows 10</span><span class="sxs-lookup"><span data-stu-id="eb92b-126">Developers Can Run Bash And Usermode Ubuntu Linux Binaries On Windows 10</span></span>](https://www.hanselman.com/blog/DevelopersCanRunBashShellAndUsermodeUbuntuLinuxBinariesOnWindows10.aspx)
* [<span data-ttu-id="eb92b-127">Ubuntu en Windows: el Ubuntu Userspace para desarrolladores de Windows</span><span class="sxs-lookup"><span data-stu-id="eb92b-127">Ubuntu on Windows – The Ubuntu Userspace for Windows Developers</span></span>](https://insights.ubuntu.com/2016/03/30/ubuntu-on-windows-the-ubuntu-userspace-for-windows-developers/) 

## <a name="provide-feedback"></a><span data-ttu-id="eb92b-128">Proporcionar comentarios</span><span class="sxs-lookup"><span data-stu-id="eb92b-128">Provide Feedback</span></span>
* [<span data-ttu-id="eb92b-129">Rastreador de problemas de GitHub</span><span class="sxs-lookup"><span data-stu-id="eb92b-129">GitHub issue tracker</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
* [<span data-ttu-id="eb92b-130">Portal de UserVoice de línea de comandos</span><span class="sxs-lookup"><span data-stu-id="eb92b-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
