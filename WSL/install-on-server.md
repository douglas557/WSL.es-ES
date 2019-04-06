---
title: Instale el subsistema de Linux en Windows Server
description: Instrucciones de instalación para el subsistema de Linux en Windows Server.
keywords: BashOnWindows, bash, wsl, windows, el subsistema de windows para linux, windowssubsystem, ubuntu, windows server
author: scooley
ms.author: scooley
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: c0b8af08a06428ebd292b8c6b9b275726988bdbe
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063623"
---
# <a name="windows-server-installation-guide"></a>Guía de instalación de Windows Server

> Se aplica a Windows Server 2019 y versiones posteriores

En / / Build2017, Microsoft anunció que el subsistema de Windows para Linux será [disponible en Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).  Estas instrucciones se recorra ejecuta el subsistema de Windows para Linux en Windows Server 1709 y versiones posteriores.

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a>Habilitar el subsistema Windows para Linux (WSL)

Antes de poder ejecutar las distribuciones de Linux en Windows, debe habilitar la característica opcional "Subsistema de Windows para Linux" y reinicie.

1. Abra PowerShell como administrador y ejecute:
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. Reinicie el equipo cuando se le solicite. **Este reinicio es necesario** con el fin de asegurarse de que WSL puede iniciar un entorno de ejecución de confianza.

## <a name="download-a-linux-distro"></a>Descargue una distribución de Linux

Siga [estas instrucciones](install-manual.md) para descargar la distribución de Linux favorita.

## <a name="extract-and-install-a-linux-distro"></a>Extraer e instalar una distribución de Linux
Ahora que ha descargado una distribución, extraiga el contenido e instalar manualmente la distribución:

1. Extraer el `<distro>.appx` contenido del paquete, por ejemplo, mediante PowerShell:

    ```powershell
    Rename-Item ~/Ubuntu.appx ~/Ubuntu.zip
    Expand-Archive ~/Ubuntu.zip ~/Ubuntu
    ```

2. Ejecute el iniciador de distribución para completar la instalación, ejecute la aplicación de selector de distribución en la carpeta de destino, denominado `<distro>.exe`. Por ejemplo: `ubuntu.exe`, etcetera.

    ![Distribución de Ubuntu expandida en Windows Server](media/server-appx-expand.png)

    > **Solución de problemas**
    > * **Error de instalación 0x8007007e**: Este error se produce cuando el sistema no admite WSL. Asegúrese de que:
    >   * Ya está ejecutando Windows compilación 16215 o posterior. [Comprobar la compilación](troubleshooting.md#check-your-build-number).
    >   * El subsistema de Windows para el componente opcional de Linux está habilitado y ha reiniciado el equipo.  [Asegúrese de que está habilitado WSL](troubleshooting.md#confirm-wsl-is-enabled).
    
3. Agregar la ruta de acceso de distribución a la ruta de acceso de entorno de Windows (`C:\Users\Administrator\Ubuntu` en este ejemplo), por ejemplo, mediante Powershell:
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + "C:\Users\Administrator\Ubuntu", "User")
    ```
    Ahora puede iniciar la distribución de cualquier ruta de acceso escribiendo `<distro>.exe`. Por ejemplo: `ubuntu.exe`

Ahora que está instalada la distribución de Linux, debe [inicializar la nueva instancia de la distribución](initialize-distro.md) antes de usar la distribución.
