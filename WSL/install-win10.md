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
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063293"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a>Subsistema de Windows para la Guía de instalación de Linux para Windows 10

## <a name="install-the-windows-subsystem-for-linux"></a>Instale el subsistema de Windows para Linux

Antes de instalar cualquier distribuciones de Linux para WSL, debe asegurarse de que el "Windows Subsystem for Linux" está habilitada la característica opcional:

1. Abra PowerShell como administrador y ejecute:
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. Reinicie el equipo cuando se le solicite.

## <a name="install-your-linux-distribution-of-choice"></a>Instalar la distribución de Linux de elección
Para descargar e instalar su distro(s) preferida, tiene tres opciones:
1. Descargar e instalar desde el Store de Windows (ver abajo)
1. Descargar e instalar desde los comandos de línea o secuencia de comandos ([lea las instrucciones de instalación manual](install-manual.md))
1. Descargue y desempaquete e instalar manualmente (para Windows Server - [estas instrucciones](install-on-server.md))

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a>Windows 10 Fall Creators Update y versiones posteriores: Instalar desde la Microsoft Store

> En esta sección es para la compilación 16215 o posterior de Windows.  Siga estos pasos para [comprobar la compilación](troubleshooting.md#check-your-build-number). 

1. Abra la Microsoft Store y elija la distribución de Linux favorita.

    ![Vista de distribuciones de Linux en la tienda Windows](media/store.png)

    Los siguientes vínculos abrirá la página de la tienda Windows para cada distribución:

    * [Ubuntu](https://www.microsoft.com/store/p/ubuntu/9nblggh4msv6)
    * [OpenSUSE](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [SLES](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)

1. En la página de la distribución, seleccione "Get"

    ![Vista de distribuciones de Linux en la tienda Windows](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a>Completar la inicialización de la distribución
Ahora que está instalada la distribución de Linux, debe [inicializar la nueva instancia de la distribución](initialize-distro.md) una vez, antes de poder usarlo.

## <a name="troubleshooting"></a>Solución de problemas: 

A continuación se muestran errores relacionados y correcciones sugeridas. Hacer referencia a la [página de solución de problemas de WSL](troubleshooting.md) para otros errores comunes y sus soluciones.

* **Instalación con el error 0 x 80070003**
    * El subsistema de Windows para Linux solo se ejecuta en la unidad del sistema (normalmente es la `C:` unidad). Asegúrese de que las distribuciones se almacenan en la unidad del sistema:  
    * Abra **configuración** -> **almacenamiento** -> **más configuraciones de almacenamiento: Cambio donde se guarda el nuevo contenido**
    ![imagen de configuración del sistema para instalar aplicaciones en la unidad C:](media/AppStorage.png)
