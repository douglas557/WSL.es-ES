---
title: Instalar el Subsistema de Windows para Linux (WSL) en Windows 10
description: Instrucciones de instalación para el Subsistema de Windows para Linux en Windows 10.
keywords: BashOnWindows, bash, wsl, wsl2, windows, subsistema de windows para linux, windowssubsystem, ubuntu, debian, suse, windows 10, instalación
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: c53c4507fb56f8e4a3456963b1d6f50ceac8ef37
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269811"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="500f2-104">Guía de instalación del Subsistema de Windows para Linux para Windows 10</span><span class="sxs-lookup"><span data-stu-id="500f2-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="500f2-105">Instalar el Subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="500f2-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="500f2-106">Antes de instalar cualquier distribución de Linux para WSL, debes asegurarte de que la característica opcional "Subsistema de Windows para Linux" esté habilitada:</span><span class="sxs-lookup"><span data-stu-id="500f2-106">Before installing any Linux distros for WSL, you must ensure that the "Windows Subsystem for Linux" optional feature is enabled:</span></span>

1. <span data-ttu-id="500f2-107">Abre PowerShell como administrador y ejecuta:</span><span class="sxs-lookup"><span data-stu-id="500f2-107">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="500f2-108">Reinicia el equipo cuando se te solicite.</span><span class="sxs-lookup"><span data-stu-id="500f2-108">Restart your computer when prompted.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="500f2-109">Instalación de la distribución de Linux que quieras</span><span class="sxs-lookup"><span data-stu-id="500f2-109">Install your Linux Distribution of Choice</span></span>
<span data-ttu-id="500f2-110">Para descargar e instalar las distribuciones que prefieras, tienes tres opciones:</span><span class="sxs-lookup"><span data-stu-id="500f2-110">To download and install your preferred distro(s), you have three choices:</span></span>
1. <span data-ttu-id="500f2-111">Descargarlas e instalarlas de Microsoft Store (ver la información que hay a continuación).</span><span class="sxs-lookup"><span data-stu-id="500f2-111">Download and install from the Microsoft Store (see below)</span></span>
1. <span data-ttu-id="500f2-112">Descargarlas e instalarlas desde la línea de comandos o el script ([lee las instrucciones de instalación del manual](install-manual.md)).</span><span class="sxs-lookup"><span data-stu-id="500f2-112">Download and install from the Command-Line/Script ([read the manual installation instructions](install-manual.md))</span></span>
1. <span data-ttu-id="500f2-113">Descargarlas y desempaquetarlas e instalarlas manualmente (para Windows Server: [aquí están las instrucciones](install-on-server.md)).</span><span class="sxs-lookup"><span data-stu-id="500f2-113">Download and manually unpack and install (for Windows Server - [instructions here](install-on-server.md))</span></span>

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a><span data-ttu-id="500f2-114">Windows 10 Fall Creators Update y posteriores: Descargar desde Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="500f2-114">Windows 10 Fall Creators Update and later: Install from the Microsoft Store</span></span>

> <span data-ttu-id="500f2-115">Esta sección es para la compilación 16215 de Windows o posterior.</span><span class="sxs-lookup"><span data-stu-id="500f2-115">This section is for Windows build 16215 or later.</span></span>  <span data-ttu-id="500f2-116">Sigue estos pasos para [comprobar la compilación](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="500f2-116">Follow these steps to [check your build](troubleshooting.md#check-your-build-number).</span></span> 

1. <span data-ttu-id="500f2-117">Abre Microsoft Store y elige tu distribución de Linux favorita.</span><span class="sxs-lookup"><span data-stu-id="500f2-117">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![Vista de las distribuciones de Linux en Microsoft Store](media/store.png)

    <span data-ttu-id="500f2-119">En los vínculos siguientes se abrirá la página de Microsoft Store para cada distribución:</span><span class="sxs-lookup"><span data-stu-id="500f2-119">The following links will open the Microsoft store page for each distribution:</span></span>

    * [<span data-ttu-id="500f2-120">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="500f2-120">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [<span data-ttu-id="500f2-121">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="500f2-121">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [<span data-ttu-id="500f2-122">OpenSUSE Leap 15</span><span class="sxs-lookup"><span data-stu-id="500f2-122">OpenSUSE Leap 15</span></span>](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [<span data-ttu-id="500f2-123">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="500f2-123">OpenSUSE Leap 42</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [<span data-ttu-id="500f2-124">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="500f2-124">SUSE Linux Enterprise Server 12</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [<span data-ttu-id="500f2-125">SUSE Linux Enterprise Server 15</span><span class="sxs-lookup"><span data-stu-id="500f2-125">SUSE Linux Enterprise Server 15</span></span>](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [<span data-ttu-id="500f2-126">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="500f2-126">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [<span data-ttu-id="500f2-127">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="500f2-127">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [<span data-ttu-id="500f2-128">Fedora Remix for WSL</span><span class="sxs-lookup"><span data-stu-id="500f2-128">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [<span data-ttu-id="500f2-129">Pengwin</span><span class="sxs-lookup"><span data-stu-id="500f2-129">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [<span data-ttu-id="500f2-130">Pengwin Enterprise</span><span class="sxs-lookup"><span data-stu-id="500f2-130">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [<span data-ttu-id="500f2-131">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="500f2-131">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

1. <span data-ttu-id="500f2-132">En la página de la distribución, selecciona "Obtener".</span><span class="sxs-lookup"><span data-stu-id="500f2-132">From the distro's page, select "Get"</span></span>

    ![Vista de las distribuciones de Linux en Microsoft Store](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="500f2-134">Completar la inicialización de la distribución</span><span class="sxs-lookup"><span data-stu-id="500f2-134">Complete initialization of your distro</span></span>
<span data-ttu-id="500f2-135">Ahora que está instalada la distribución de Linux, debes [inicializar la nueva instancia de la distribución](initialize-distro.md) una vez, antes de que se pueda usar.</span><span class="sxs-lookup"><span data-stu-id="500f2-135">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) once, before it can be used.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="500f2-136">Solución de problemas:</span><span class="sxs-lookup"><span data-stu-id="500f2-136">Troubleshooting:</span></span> 

<span data-ttu-id="500f2-137">A continuación se muestran errores relacionados y las correcciones sugeridas.</span><span class="sxs-lookup"><span data-stu-id="500f2-137">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="500f2-138">Consulta la [página de solución de problemas de WSL](troubleshooting.md) para ver otros errores generales y sus soluciones.</span><span class="sxs-lookup"><span data-stu-id="500f2-138">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

* <span data-ttu-id="500f2-139">**Error 0x80070003 en la instalación**</span><span class="sxs-lookup"><span data-stu-id="500f2-139">**Installation failed with error 0x80070003**</span></span>
    * <span data-ttu-id="500f2-140">El Subsistema de Windows para Linux solo se ejecuta en la unidad del sistema (normalmente se trata de la unidad `C:`).</span><span class="sxs-lookup"><span data-stu-id="500f2-140">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="500f2-141">Asegúrate de que las distribuciones se almacenan en la unidad del sistema:</span><span class="sxs-lookup"><span data-stu-id="500f2-141">Make sure that distros are stored on your system drive:</span></span>  
    * <span data-ttu-id="500f2-142">Abre **Configuración** -> **Almacenamiento** -> **Más opciones de almacenamiento: Cambia el lugar donde se guarda el nuevo contenido**
    ![Imagen de la configuración del sistema para instalar aplicaciones en la unidad C:](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="500f2-142">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>
    
    
 * <span data-ttu-id="500f2-143">**Error 0x8007019e de WslRegisterDistribution**</span><span class="sxs-lookup"><span data-stu-id="500f2-143">**WslRegisterDistribution failed with error 0x8007019e**</span></span>   
  * <span data-ttu-id="500f2-144">El componente opcional del Subsistema de Windows para Linux no está habilitado:</span><span class="sxs-lookup"><span data-stu-id="500f2-144">The Windows Subsystem for Linux optional component is not enabled:</span></span> 
   * <span data-ttu-id="500f2-145">Abre el **Panel de control** -> **Programas y características** -> **Activa o desactiva la característica de Windows** -> Selecciona el **Subsistema de Windows para Linux** o usa el cmdlet de PowerShell mencionado al comienzo de este artículo.</span><span class="sxs-lookup"><span data-stu-id="500f2-145">Open **Control Panel** -> **Programs and Features** -> **Turn Windows Feature on or off** -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the begining of this article.</span></span>
