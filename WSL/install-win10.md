---
title: Instalar el subsistema de Windows para Linux (WSL) en Windows 10
description: Instrucciones de instalación para el subsistema de Windows para Linux en Windows 10.
keywords: BashOnWindows, bash, WSL, Windows, subsistema de Windows para Linux, windowssubsystem, Ubuntu, Debian, SuSE, Windows 10, instalación
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 218e3e652d0849f944e8aaceef3fb954294222be
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122777"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="b4f92-104">Guía de instalación del subsistema de Windows para Linux para Windows 10</span><span class="sxs-lookup"><span data-stu-id="b4f92-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="b4f92-105">Instalar el subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="b4f92-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="b4f92-106">Antes de instalar cualquier distribuciones de Linux para WSL, debe asegurarse de que la característica opcional "subsistema de Windows para Linux" esté habilitada:</span><span class="sxs-lookup"><span data-stu-id="b4f92-106">Before installing any Linux distros for WSL, you must ensure that the "Windows Subsystem for Linux" optional feature is enabled:</span></span>

1. <span data-ttu-id="b4f92-107">Abra PowerShell como administrador y ejecute:</span><span class="sxs-lookup"><span data-stu-id="b4f92-107">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="b4f92-108">Reinicie el equipo cuando se le solicite.</span><span class="sxs-lookup"><span data-stu-id="b4f92-108">Restart your computer when prompted.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="b4f92-109">Instalación de la distribución de Linux de su elección</span><span class="sxs-lookup"><span data-stu-id="b4f92-109">Install your Linux Distribution of Choice</span></span>
<span data-ttu-id="b4f92-110">Para descargar e instalar los distribución preferidos, tiene tres opciones:</span><span class="sxs-lookup"><span data-stu-id="b4f92-110">To download and install your preferred distro(s), you have three choices:</span></span>
1. <span data-ttu-id="b4f92-111">Descargar e instalar desde el Microsoft Store (ver más abajo)</span><span class="sxs-lookup"><span data-stu-id="b4f92-111">Download and install from the Microsoft Store (see below)</span></span>
1. <span data-ttu-id="b4f92-112">Descargar e instalar desde la línea de comandos/script ([Lea las instrucciones de instalación manual](install-manual.md))</span><span class="sxs-lookup"><span data-stu-id="b4f92-112">Download and install from the Command-Line/Script ([read the manual installation instructions](install-manual.md))</span></span>
1. <span data-ttu-id="b4f92-113">Descargar y desempaquetar e instalar manualmente (para Windows Server- [instrucciones aquí](install-on-server.md))</span><span class="sxs-lookup"><span data-stu-id="b4f92-113">Download and manually unpack and install (for Windows Server - [instructions here](install-on-server.md))</span></span>

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a><span data-ttu-id="b4f92-114">Windows 10 Fall Creators Update y versiones posteriores: Instalar desde el Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="b4f92-114">Windows 10 Fall Creators Update and later: Install from the Microsoft Store</span></span>

> <span data-ttu-id="b4f92-115">Esta sección es para Windows Build 16215 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b4f92-115">This section is for Windows build 16215 or later.</span></span>  <span data-ttu-id="b4f92-116">Siga estos pasos para [comprobar la compilación](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="b4f92-116">Follow these steps to [check your build](troubleshooting.md#check-your-build-number).</span></span> 

1. <span data-ttu-id="b4f92-117">Abra el Microsoft Store y elija su distribución de Linux favorita.</span><span class="sxs-lookup"><span data-stu-id="b4f92-117">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![Vista de distribuciones de Linux en el Microsoft Store](media/store.png)

    <span data-ttu-id="b4f92-119">En los vínculos siguientes se abrirá la página de Microsoft Store para cada distribución:</span><span class="sxs-lookup"><span data-stu-id="b4f92-119">The following links will open the Microsoft store page for each distribution:</span></span>

    * [<span data-ttu-id="b4f92-120">Ubuntu 16,04 LTS</span><span class="sxs-lookup"><span data-stu-id="b4f92-120">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [<span data-ttu-id="b4f92-121">Ubuntu 18,04 LTS</span><span class="sxs-lookup"><span data-stu-id="b4f92-121">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [<span data-ttu-id="b4f92-122">OpenSUSE Leap 15</span><span class="sxs-lookup"><span data-stu-id="b4f92-122">OpenSUSE Leap 15</span></span>](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [<span data-ttu-id="b4f92-123">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="b4f92-123">OpenSUSE Leap 42</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [<span data-ttu-id="b4f92-124">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="b4f92-124">SUSE Linux Enterprise Server 12</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [<span data-ttu-id="b4f92-125">SUSE Linux Enterprise Server 15</span><span class="sxs-lookup"><span data-stu-id="b4f92-125">SUSE Linux Enterprise Server 15</span></span>](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [<span data-ttu-id="b4f92-126">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="b4f92-126">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [<span data-ttu-id="b4f92-127">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="b4f92-127">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [<span data-ttu-id="b4f92-128">Fedora Remix WSL</span><span class="sxs-lookup"><span data-stu-id="b4f92-128">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [<span data-ttu-id="b4f92-129">Pengwin</span><span class="sxs-lookup"><span data-stu-id="b4f92-129">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [<span data-ttu-id="b4f92-130">Pengwin Enterprise</span><span class="sxs-lookup"><span data-stu-id="b4f92-130">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [<span data-ttu-id="b4f92-131">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="b4f92-131">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

1. <span data-ttu-id="b4f92-132">En la página de distribución, seleccione "obtener".</span><span class="sxs-lookup"><span data-stu-id="b4f92-132">From the distro's page, select "Get"</span></span>

    ![Vista de distribuciones de Linux en Microsoft Store](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="b4f92-134">Completar la inicialización de distribución</span><span class="sxs-lookup"><span data-stu-id="b4f92-134">Complete initialization of your distro</span></span>
<span data-ttu-id="b4f92-135">Ahora que está instalado el distribución de Linux, debe [inicializar la nueva instancia de distribución](initialize-distro.md) una vez, antes de que se pueda usar.</span><span class="sxs-lookup"><span data-stu-id="b4f92-135">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) once, before it can be used.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="b4f92-136">Solución de problemas:</span><span class="sxs-lookup"><span data-stu-id="b4f92-136">Troubleshooting:</span></span> 

<span data-ttu-id="b4f92-137">A continuación se muestran los errores relacionados y las correcciones sugeridas.</span><span class="sxs-lookup"><span data-stu-id="b4f92-137">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="b4f92-138">Consulte la [Página de solución de problemas de WSL](troubleshooting.md) para ver otros errores comunes y sus soluciones.</span><span class="sxs-lookup"><span data-stu-id="b4f92-138">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

* <span data-ttu-id="b4f92-139">**Error de instalación con el error 0x80070003**</span><span class="sxs-lookup"><span data-stu-id="b4f92-139">**Installation failed with error 0x80070003**</span></span>
    * <span data-ttu-id="b4f92-140">El subsistema de Windows para Linux solo se ejecuta en la unidad del sistema (normalmente `C:` se trata de la unidad).</span><span class="sxs-lookup"><span data-stu-id="b4f92-140">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="b4f92-141">Asegúrese de que distribuciones se almacenan en la unidad del sistema:</span><span class="sxs-lookup"><span data-stu-id="b4f92-141">Make sure that distros are stored on your system drive:</span></span>  
    * <span data-ttu-id="b4f92-142">Abra **configuración** -> almacenamiento -> más opciones de almacenamiento: \*\* Cambiar dónde se guarda\*\*
    ![el nuevo contenido imagen de la configuración del sistema para instalar aplicaciones en la unidad C:](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="b4f92-142">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>
    
    
 * <span data-ttu-id="b4f92-143">**Error de WslRegisterDistribution con 0x8007019e**</span><span class="sxs-lookup"><span data-stu-id="b4f92-143">**WslRegisterDistribution failed with error 0x8007019e**</span></span>   
  * <span data-ttu-id="b4f92-144">El componente opcional de subsistema de Windows para Linux no está habilitado:</span><span class="sxs-lookup"><span data-stu-id="b4f92-144">The Windows Subsystem for Linux optional component is not enabled:</span></span> 
   * <span data-ttu-id="b4f92-145">Abra **Panel** -> de control**programas y características** -> **activar o desactivar** las características de Windows > el subsistema **de Windows para Linux** o con el cmdlet de PowerShell que se menciona al principio de este artículo.</span><span class="sxs-lookup"><span data-stu-id="b4f92-145">Open **Control Panel** -> **Programs and Features** -> **Turn Windows Feature on or off** -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the begining of this article.</span></span>
