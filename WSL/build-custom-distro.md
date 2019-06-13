---
title: Crear una distribución de Linux personalizada para WSL
description: Obtenga información sobre cómo crear una distribución de Linux personalizada para el subsistema de Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, el subsistema de windows, distribución, personalizado
author: taraj
ms.author: taraj
ms.date: 03/27/2018
ms.topic: article
ms.assetid: a5095219-0c82-4ce5-9a6d-5c2fc00835a3
ms.custom: seodec18
ms.openlocfilehash: 4072df5fa81f65fd9a3ff875ab887c03b234bce1
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040775"
---
# <a name="creating-a-custom-linux-distro-for-wsl"></a><span data-ttu-id="72bdf-104">Creación de una distribución de Linux personalizada para WSL</span><span class="sxs-lookup"><span data-stu-id="72bdf-104">Creating a Custom Linux Distro for WSL</span></span>

<span data-ttu-id="72bdf-105">Utilice nuestro ejemplo WSL de código abierto para crear paquetes de distribución WSL para la Microsoft Store o crear paquetes personalizados de distribución de Linux para la instalación de prueba.</span><span class="sxs-lookup"><span data-stu-id="72bdf-105">Use our open source WSL sample to build WSL distro packages for the Microsoft Store and/or to create custom Linux distro packages for sideloading.</span></span> <span data-ttu-id="72bdf-106">Puede encontrar el [repositorio de distribución del iniciador](https://github.com/Microsoft/WSL-DistroLauncher) en GitHub.</span><span class="sxs-lookup"><span data-stu-id="72bdf-106">You can find the [distro launcher repo](https://github.com/Microsoft/WSL-DistroLauncher) on GitHub.</span></span>

<span data-ttu-id="72bdf-107">Este proyecto permite:</span><span class="sxs-lookup"><span data-stu-id="72bdf-107">This project enables:</span></span>
* <span data-ttu-id="72bdf-108">Mantenedores de distribución de Linux para empaquetar y enviar una distribución de Linux como un appx que se ejecuta en WSL</span><span class="sxs-lookup"><span data-stu-id="72bdf-108">Linux distribution maintainers to package and submit a Linux distribution as an appx that runs on WSL</span></span>
* <span data-ttu-id="72bdf-109">A los desarrolladores crear distribuciones de Linux personalizadas que pueden transferir localmente en su equipo de desarrollo</span><span class="sxs-lookup"><span data-stu-id="72bdf-109">Developers to create custom Linux distributions that can be sideloaded onto their dev machine</span></span>

## <a name="background"></a><span data-ttu-id="72bdf-110">Background</span><span class="sxs-lookup"><span data-stu-id="72bdf-110">Background</span></span>
<span data-ttu-id="72bdf-111">Distribuimos distribuciones de Linux para WSL como aplicaciones para UWP a través de la Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="72bdf-111">We distribute Linux distros for WSL as UWP applications through the Microsoft Store.</span></span> <span data-ttu-id="72bdf-112">Puede instalar las aplicaciones que se ejecutarán en WSL - el subsistema que se encuentra en el kernel de Windows.</span><span class="sxs-lookup"><span data-stu-id="72bdf-112">You can install those applications that will then run on WSL - the subsystem that sits in the Windows kernel.</span></span> <span data-ttu-id="72bdf-113">Este mecanismo de entrega tiene muchas ventajas, como se describe en un [anteriores de blog](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/).</span><span class="sxs-lookup"><span data-stu-id="72bdf-113">This delivery mechanism has many benefits as discussed in an [earlier blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/).</span></span>

## <a name="sideloading-a-custom-linux-distro-package"></a><span data-ttu-id="72bdf-114">Instalación de prueba un paquete de distribución de Linux personalizada</span><span class="sxs-lookup"><span data-stu-id="72bdf-114">Sideloading a Custom Linux Distro Package</span></span>
<span data-ttu-id="72bdf-115">Puede crear un paquete personalizado de distribución de Linux como una aplicación para transferir localmente en su equipo personal.</span><span class="sxs-lookup"><span data-stu-id="72bdf-115">You can create a custom Linux distro package as an application to sideload on your personal machine.</span></span> <span data-ttu-id="72bdf-116">Tenga en cuenta que el paquete personalizado no se distribuyen a través de la Microsoft Store a menos que se envía como un mantenedor de distribución.</span><span class="sxs-lookup"><span data-stu-id="72bdf-116">Please note that your custom package would not be distributed through the Microsoft Store unless you submit as a distribution maintainer.</span></span>
<span data-ttu-id="72bdf-117">Para configurar el equipo para agregar o quitar aplicaciones, deberá habilitarla en la configuración del sistema en "Para desarrolladores".</span><span class="sxs-lookup"><span data-stu-id="72bdf-117">To set up your machine to sideload apps, you will need to enable this in the system settings under “For Developers”.</span></span>  <span data-ttu-id="72bdf-118">Asegúrese de contar con modo de programador, o bien agregar o quitar aplicaciones seleccionadas</span><span class="sxs-lookup"><span data-stu-id="72bdf-118">Be sure to either have developer mode, or sideload apps selected</span></span>

## <a name="for-linux-distro-maintainers"></a><span data-ttu-id="72bdf-119">Para los mantenedores de distribución de Linux</span><span class="sxs-lookup"><span data-stu-id="72bdf-119">For Linux Distro Maintainers</span></span>
<span data-ttu-id="72bdf-120">Para enviar a la Store, deberá trabajar con nosotros para recibir la aprobación de publicación.</span><span class="sxs-lookup"><span data-stu-id="72bdf-120">To submit to the Store, you will need to work with us to receive publishing approval.</span></span> <span data-ttu-id="72bdf-121">Si es un propietario de la distribución de Linux interesado en agregar su distribución a la Microsoft Store, póngase en contacto con wslpartners@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="72bdf-121">If you are a Linux distribution owner interested in adding your distribution to the Microsoft Store, please contact wslpartners@microsoft.com.</span></span>

## <a name="getting-started"></a><span data-ttu-id="72bdf-122">Introducción</span><span class="sxs-lookup"><span data-stu-id="72bdf-122">Getting Started</span></span>
<span data-ttu-id="72bdf-123">Siga las instrucciones de la [repositorio de GitHub de distribución del iniciador](https://github.com/Microsoft/WSL-DistroLauncher) para crear un paquete personalizado de distribución de Linux.</span><span class="sxs-lookup"><span data-stu-id="72bdf-123">Follow the instructions on the [Distro Launcher GitHub repo](https://github.com/Microsoft/WSL-DistroLauncher) to create a custom Linux distro package.</span></span>

 
## <a name="team-blogs"></a><span data-ttu-id="72bdf-124">Blogs del equipo</span><span class="sxs-lookup"><span data-stu-id="72bdf-124">Team Blogs</span></span>
*  [<span data-ttu-id="72bdf-125">Abra el abastecimiento de un ejemplo WSL para los mantenedores de distribución de Linux y las distribuciones de Linux personalizada de la instalación de prueba</span><span class="sxs-lookup"><span data-stu-id="72bdf-125">Open Sourcing a WSL Sample for Linux Distribution Maintainers and Sideloading Custom Linux Distributions</span></span>](https://blogs.msdn.microsoft.com/commandline/2018/03/26/wsl-distro-launcher/)
* [<span data-ttu-id="72bdf-126">Blog de línea de comandos</span><span class="sxs-lookup"><span data-stu-id="72bdf-126">Command-Line blog</span></span>](https://blogs.msdn.microsoft.com/commandline/)

## <a name="provide-feedback"></a><span data-ttu-id="72bdf-127">Proporcionar comentarios</span><span class="sxs-lookup"><span data-stu-id="72bdf-127">Provide Feedback</span></span>
* [<span data-ttu-id="72bdf-128">Repositorio de GitHub del iniciador de distribución</span><span class="sxs-lookup"><span data-stu-id="72bdf-128">Distro Launcher GitHub repo</span></span>](https://github.com/Microsoft/WSL-DistroLauncher)
* [<span data-ttu-id="72bdf-129">Seguimiento de problemas de GitHub de WSL</span><span class="sxs-lookup"><span data-stu-id="72bdf-129">GitHub issue tracker for WSL</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
* [<span data-ttu-id="72bdf-130">Portal de UserVoice de línea de comandos</span><span class="sxs-lookup"><span data-stu-id="72bdf-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
