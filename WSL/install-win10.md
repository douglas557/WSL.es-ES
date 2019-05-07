---
title: Instale el subsistema de Windows para Linux (WSL) en Windows 10
description: Instrucciones de instalación para el subsistema de Windows para Linux en Windows 10.
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, windowssubsystem, ubuntu, debian, suse, windows 10, instalar
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 40bbe73acbfd0483e18ab6ff1696fdb44eaff2e4
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063293"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="52014-104">Subsistema de Windows para la Guía de instalación de Linux para Windows 10</span><span class="sxs-lookup"><span data-stu-id="52014-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="52014-105">Instale el subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="52014-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="52014-106">Antes de instalar cualquier distribuciones de Linux para WSL, debe asegurarse de que el "Windows Subsystem for Linux" está habilitada la característica opcional:</span><span class="sxs-lookup"><span data-stu-id="52014-106">Before installing any Linux distros for WSL, you must ensure that the "Windows Subsystem for Linux" optional feature is enabled:</span></span>

1. <span data-ttu-id="52014-107">Abra PowerShell como administrador y ejecute:</span><span class="sxs-lookup"><span data-stu-id="52014-107">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="52014-108">Reinicie el equipo cuando se le solicite.</span><span class="sxs-lookup"><span data-stu-id="52014-108">Restart your computer when prompted.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="52014-109">Instalar la distribución de Linux de elección</span><span class="sxs-lookup"><span data-stu-id="52014-109">Install your Linux Distribution of Choice</span></span>
<span data-ttu-id="52014-110">Para descargar e instalar su distro(s) preferida, tiene tres opciones:</span><span class="sxs-lookup"><span data-stu-id="52014-110">To download and install your preferred distro(s), you have three choices:</span></span>
1. <span data-ttu-id="52014-111">Descargar e instalar desde el Store de Windows (ver abajo)</span><span class="sxs-lookup"><span data-stu-id="52014-111">Download and install from the Windows Store (see below)</span></span>
1. <span data-ttu-id="52014-112">Descargar e instalar desde los comandos de línea o secuencia de comandos ([lea las instrucciones de instalación manual](install-manual.md))</span><span class="sxs-lookup"><span data-stu-id="52014-112">Download and install from the Command-Line/Script ([read the manual installation instructions](install-manual.md))</span></span>
1. <span data-ttu-id="52014-113">Descargue y desempaquete e instalar manualmente (para Windows Server - [estas instrucciones](install-on-server.md))</span><span class="sxs-lookup"><span data-stu-id="52014-113">Download and manually unpack and install (for Windows Server - [instructions here](install-on-server.md))</span></span>

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a><span data-ttu-id="52014-114">Windows 10 Fall Creators Update y versiones posteriores: Instalar desde la Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="52014-114">Windows 10 Fall Creators Update and later: Install from the Microsoft Store</span></span>

> <span data-ttu-id="52014-115">En esta sección es para la compilación 16215 o posterior de Windows.</span><span class="sxs-lookup"><span data-stu-id="52014-115">This section is for Windows build 16215 or later.</span></span>  <span data-ttu-id="52014-116">Siga estos pasos para [comprobar la compilación](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="52014-116">Follow these steps to [check your build](troubleshooting.md#check-your-build-number).</span></span> 

1. <span data-ttu-id="52014-117">Abra la Microsoft Store y elija la distribución de Linux favorita.</span><span class="sxs-lookup"><span data-stu-id="52014-117">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![Vista de distribuciones de Linux en la tienda Windows](media/store.png)

    <span data-ttu-id="52014-119">Los siguientes vínculos abrirá la página de la tienda Windows para cada distribución:</span><span class="sxs-lookup"><span data-stu-id="52014-119">The following links will open the Windows store page for each distribution:</span></span>

    * [<span data-ttu-id="52014-120">Ubuntu</span><span class="sxs-lookup"><span data-stu-id="52014-120">Ubuntu</span></span>](https://www.microsoft.com/store/p/ubuntu/9nblggh4msv6)
    * [<span data-ttu-id="52014-121">OpenSUSE</span><span class="sxs-lookup"><span data-stu-id="52014-121">OpenSUSE</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [<span data-ttu-id="52014-122">SLES</span><span class="sxs-lookup"><span data-stu-id="52014-122">SLES</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [<span data-ttu-id="52014-123">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="52014-123">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [<span data-ttu-id="52014-124">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="52014-124">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)

1. <span data-ttu-id="52014-125">En la página de la distribución, seleccione "Get"</span><span class="sxs-lookup"><span data-stu-id="52014-125">From the distro's page, select "Get"</span></span>

    ![Vista de distribuciones de Linux en la tienda Windows](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="52014-127">Completar la inicialización de la distribución</span><span class="sxs-lookup"><span data-stu-id="52014-127">Complete initialization of your distro</span></span>
<span data-ttu-id="52014-128">Ahora que está instalada la distribución de Linux, debe [inicializar la nueva instancia de la distribución](initialize-distro.md) una vez, antes de poder usarlo.</span><span class="sxs-lookup"><span data-stu-id="52014-128">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) once, before it can be used.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="52014-129">Solución de problemas:</span><span class="sxs-lookup"><span data-stu-id="52014-129">Troubleshooting:</span></span> 

<span data-ttu-id="52014-130">A continuación se muestran errores relacionados y correcciones sugeridas.</span><span class="sxs-lookup"><span data-stu-id="52014-130">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="52014-131">Hacer referencia a la [página de solución de problemas de WSL](troubleshooting.md) para otros errores comunes y sus soluciones.</span><span class="sxs-lookup"><span data-stu-id="52014-131">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

* <span data-ttu-id="52014-132">**Instalación con el error 0 x 80070003**</span><span class="sxs-lookup"><span data-stu-id="52014-132">**Installation failed with error 0x80070003**</span></span>
    * <span data-ttu-id="52014-133">El subsistema de Windows para Linux solo se ejecuta en la unidad del sistema (normalmente es la `C:` unidad).</span><span class="sxs-lookup"><span data-stu-id="52014-133">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="52014-134">Asegúrese de que las distribuciones se almacenan en la unidad del sistema:</span><span class="sxs-lookup"><span data-stu-id="52014-134">Make sure that distros are stored on your system drive:</span></span>  
    * <span data-ttu-id="52014-135">Abra **configuración** -> **almacenamiento** -> **más configuraciones de almacenamiento: Cambio donde se guarda el nuevo contenido**
    ![imagen de configuración del sistema para instalar aplicaciones en la unidad C:](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="52014-135">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>
