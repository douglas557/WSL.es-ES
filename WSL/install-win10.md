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
ms.openlocfilehash: 82b5c0ccba7a444f13f186a2e33f210ac2cf48da
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499285"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a>Guía de instalación del subsistema de Windows para Linux para Windows 10

## <a name="install-the-windows-subsystem-for-linux"></a>Instalar el subsistema de Windows para Linux

Antes de instalar cualquier distribuciones de Linux para WSL, debe asegurarse de que la característica opcional "subsistema de Windows para Linux" esté habilitada:

1. Abra PowerShell como administrador y ejecute:
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. Reinicie el equipo cuando se le solicite.

## <a name="install-your-linux-distribution-of-choice"></a>Instalación de la distribución de Linux de su elección
Para descargar e instalar los distribución preferidos, tiene tres opciones:
1. Descargar e instalar desde el Microsoft Store (ver más abajo)
1. Descargar e instalar desde la línea de comandos/script ([Lea las instrucciones de instalación manual](install-manual.md))
1. Descargar y desempaquetar e instalar manualmente (para Windows Server- [instrucciones aquí](install-on-server.md))

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a>Windows 10 Fall Creators Update y versiones posteriores: Instalar desde el Microsoft Store

> Esta sección es para Windows Build 16215 o posterior.  Siga estos pasos para [comprobar la compilación](troubleshooting.md#check-your-build-number). 

1. Abra el Microsoft Store y elija su distribución de Linux favorita.

    ![Vista de distribuciones de Linux en el Microsoft Store](media/store.png)

    En los vínculos siguientes se abrirá la página de Microsoft Store para cada distribución:

    * [Ubuntu 16,04 LTS](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [Ubuntu 18,04 LTS](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [OpenSUSE Leap 15](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [OpenSUSE Leap 42](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [SUSE Linux Enterprise Server 12](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [SUSE Linux Enterprise Server 15](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [Fedora Remix WSL](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [Pengwin](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [Pengwin Enterprise](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [Alpine WSL](https://www.microsoft.com/store/apps/9p804crf0395)

1. En la página de distribución, seleccione "obtener".

    ![Vista de distribuciones de Linux en Microsoft Store](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a>Completar la inicialización de distribución
Ahora que está instalado el distribución de Linux, debe [inicializar la nueva instancia de distribución](initialize-distro.md) una vez, antes de que se pueda usar.

## <a name="troubleshooting"></a>Solución de problemas: 

A continuación se muestran los errores relacionados y las correcciones sugeridas. Consulte la [Página de solución de problemas de WSL](troubleshooting.md) para ver otros errores comunes y sus soluciones.

* **Error de instalación con el error 0x80070003**
    * El subsistema de Windows para Linux solo se ejecuta en la unidad del sistema (normalmente `C:` se trata de la unidad). Asegúrese de que distribuciones se almacenan en la unidad del sistema:  
    * Abra **configuración** ->  almacenamiento -> más opciones de almacenamiento: ** Cambiar dónde se guarda**
    ![el nuevo contenido imagen de la configuración del sistema para instalar aplicaciones en la unidad C:](media/AppStorage.png)
    
    
 * **Error de WslRegisterDistribution con 0x8007019e**   
  * El componente opcional de subsistema de Windows para Linux no está habilitado: 
   * Abra **Panel** -> de control**programas y características** -> * * activar o desactivar las características de Windows * *-> comprobar el subsistema **de Windows para Linux** o usar el cmdlet de PowerShell que se menciona al principio de este artículo.
