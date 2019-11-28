---
title: Instalar el Subsistema de Windows para Linux (WSL) en Windows 10
description: Instrucciones de instalación para el Subsistema de Windows para Linux en Windows 10.
keywords: BashOnWindows, bash, wsl, wsl2, windows, subsistema de windows para linux, windowssubsystem, ubuntu, debian, suse, windows 10, instalación
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 17ca32db23b426ef1367ff9444b5924d9d7e1716
ms.sourcegitcommit: 3be576f946611cf36e27745bdb7c4c52af1b9928
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "74200234"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a>Guía de instalación del Subsistema de Windows para Linux para Windows 10

## <a name="install-the-windows-subsystem-for-linux"></a>Instalar el Subsistema de Windows para Linux

Antes de instalar cualquier distribución de Linux para WSL, debes asegurarte de que la característica opcional "Subsistema de Windows para Linux" esté habilitada:

1. Abre PowerShell como administrador y ejecuta:
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. Reinicia el equipo cuando se te solicite.

## <a name="install-your-linux-distribution-of-choice"></a>Instalación de la distribución de Linux que quieras
Para descargar e instalar las distribuciones que prefieras, tienes tres opciones:
* Descargarlas e instalarlas de Microsoft Store (ver la información que hay a continuación).
* Descargarlas e instalarlas desde la línea de comandos o el script ([lee las instrucciones de instalación del manual](install-manual.md)).
* Descargarlas y desempaquetarlas e instalarlas manualmente (para Windows Server: [aquí están las instrucciones](install-on-server.md)).

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a>Windows 10 Fall Creators Update y posteriores: Descargar desde Microsoft Store

> Esta sección es para la compilación 16215 de Windows o posterior.  Sigue estos pasos para [comprobar la compilación](troubleshooting.md#check-your-build-number). 

1. Abre Microsoft Store y elige tu distribución de Linux favorita.

    ![Vista de las distribuciones de Linux en Microsoft Store](media/store.png)

    En los vínculos siguientes se abrirá la página de Microsoft Store para cada distribución:

    * [Ubuntu 16.04 LTS](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [Ubuntu 18.04 LTS](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [OpenSUSE Leap 15](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [OpenSUSE Leap 42](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [SUSE Linux Enterprise Server 12](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [SUSE Linux Enterprise Server 15](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [Fedora Remix for WSL](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [Pengwin](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [Pengwin Enterprise](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [Alpine WSL](https://www.microsoft.com/store/apps/9p804crf0395)

1. En la página de la distribución, selecciona "Obtener".

    ![Vista de las distribuciones de Linux en Microsoft Store](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a>Completar la inicialización de la distribución
Ahora que está instalada la distribución de Linux, debes [inicializar la nueva instancia de la distribución](initialize-distro.md) una vez, antes de que se pueda usar.

## <a name="troubleshooting"></a>Solución de problemas: 

A continuación se muestran errores relacionados y las correcciones sugeridas. Consulta la [página de solución de problemas de WSL](troubleshooting.md) para ver otros errores generales y sus soluciones.

* **Error 0x80070003 en la instalación**
    * El Subsistema de Windows para Linux solo se ejecuta en la unidad del sistema (normalmente se trata de la unidad `C:`). Asegúrate de que las distribuciones se almacenan en la unidad del sistema:  
    * Abre **Configuración** -> **Almacenamiento** -> **Más opciones de almacenamiento: Cambia el lugar donde se guarda el nuevo contenido**
    ![Imagen de la configuración del sistema para instalar aplicaciones en la unidad C:](media/AppStorage.png)
    
    
 * **Error 0x8007019e de WslRegisterDistribution**   
  * El componente opcional del Subsistema de Windows para Linux no está habilitado: 
   * Abre el **Panel de control** -> **Programas y características** -> **Activa o desactiva la característica de Windows** -> Selecciona el **Subsistema de Windows para Linux** o usa el cmdlet de PowerShell mencionado al comienzo de este artículo.
