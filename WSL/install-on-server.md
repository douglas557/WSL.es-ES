---
title: Instalación del subsistema Linux en Windows Server
description: Instrucciones de instalación para el subsistema Linux en Windows Server.
keywords: BashOnWindows, bash, WSL, Windows, subsistema de Windows para Linux, windowssubsystem, Ubuntu, Windows Server
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: 51a2e3f3443ed9b1ba3d8ab79977f22839ee0283
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269779"
---
# <a name="windows-server-installation-guide"></a>Guía de instalación de Windows Server

> Se aplica a Windows Server 2019 y versiones posteriores

En//Build2017, Microsoft anunció que el subsistema de Windows para Linux estará [disponible en Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).  Estas instrucciones le guían en la ejecución del subsistema de Windows para Linux en Windows Server 1709 y versiones posteriores.

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a>Habilitación del subsistema de Windows para Linux (WSL)

Antes de poder ejecutar Linux distribuciones en Windows, debe habilitar la característica opcional "subsistema de Windows para Linux" y reiniciar.

1. Abra PowerShell como administrador y ejecute:
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. Reinicie el equipo cuando se le solicite. **Este reinicio es necesario** para asegurarse de que WSL pueda iniciar un entorno de ejecución de confianza.

## <a name="download-a-linux-distro"></a>Descarga de un distribución de Linux

Siga [estas instrucciones](install-manual.md) para descargar su distribución de Linux favorita.

## <a name="extract-and-install-a-linux-distro"></a>Extracción e instalación de un distribución de Linux
Ahora que ha descargado un distribución, extraiga su contenido e instale manualmente el distribución:

1. Extraiga el `<distro>.appx` contenido del paquete, por ejemplo, mediante PowerShell:

    ```powershell
    Rename-Item ./Ubuntu.appx ./Ubuntu.zip
    Expand-Archive ./Ubuntu.zip ./Ubuntu
    ```

2. Ejecute el iniciador de distribución para completar la instalación, ejecute la aplicación del iniciador de distribución `<distro>.exe`en la carpeta de destino, denominada. Por ejemplo: `ubuntu.exe`, etc.

    ![Se amplió Ubuntu distribución en Windows Server](media/server-appx-expand.png)

    > **Solución de problemas**
    > * **No se pudo realizar la instalación. error 0x8007007e**: Este error se produce cuando el sistema no es compatible con WSL. Asegúrese de que:
    >   * Está ejecutando Windows Build 16215 o posterior. [Compruebe la compilación](troubleshooting.md#check-your-build-number).
    >   * El componente opcional de subsistema de Windows para Linux está habilitado y el equipo se ha reiniciado.  [Asegúrese de que WSL está habilitado](troubleshooting.md#confirm-wsl-is-enabled).
    
3. Agregue la ruta de acceso de distribución a la ruta`C:\Users\Administrator\Ubuntu` de acceso del entorno de Windows (en este ejemplo), por ejemplo, con PowerShell:
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    Ahora puede iniciar el distribución desde cualquier ruta de acceso escribiendo `<distro>.exe`. Por ejemplo: `ubuntu.exe`

Ahora que está instalado el distribución de Linux, debe [inicializar la nueva instancia de distribución](initialize-distro.md) antes de usar su distribución.
