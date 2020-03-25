---
title: Instalación del subsistema Linux en Windows Server
description: Instrucciones de instalación del subsistema Linux en Windows Server.
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, subsistemawindows, ubuntu, windows server
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: 51a2e3f3443ed9b1ba3d8ab79977f22839ee0283
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269779"
---
# <a name="windows-server-installation-guide"></a>Guía de instalación de Windows Server

> Se aplica a Windows Server 2019 y versiones posteriores

En //Build2017, Microsoft anunció que el Subsistema de Windows para Linux estará [disponible en Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).  Estas instrucciones te guiarán en la ejecución del Subsistema de Windows para Linux en Windows Server 1709 y versiones posteriores.

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a>Habilitación del Subsistema de Windows para Linux (WSL)

Para poder ejecutar distribuciones de Linux en Windows, debes habilitar la característica opcional "Subsistema de Windows para Linux" y reiniciar.

1. Abre PowerShell como administrador y ejecuta:
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. Reinicia el equipo cuando se te solicite. **Este reinicio es necesario** para garantizar que WSL pueda iniciar un entorno de ejecución de confianza.

## <a name="download-a-linux-distro"></a>Descarga de un distribución de Linux

Sigue [estas instrucciones](install-manual.md) para descargar su distribución de Linux favorita.

## <a name="extract-and-install-a-linux-distro"></a>Extracción e instalación de una distribución de Linux
Ahora que has descargado una distribución, extrae su contenido e instala manualmente la distribución:

1. Extrae el contenido del paquete de `<distro>.appx`, por ejemplo, mediante PowerShell:

    ```powershell
    Rename-Item ./Ubuntu.appx ./Ubuntu.zip
    Expand-Archive ./Ubuntu.zip ./Ubuntu
    ```

2. Ejecuta el iniciador de distribuciones para completar la instalación y ejecute la aplicación del iniciador de distribuciones en la carpeta de destino, denominada `<distro>.exe`. Por ejemplo: `ubuntu.exe`, etc.

    ![Distribución de Ubuntu ampliada en Windows Server](media/server-appx-expand.png)

    > **Solución de problemas**
    > * **Error 0x8007007e en la instalación**: Este error se produce cuando el sistema no es compatible con WSL. Asegúrese de que:
    >   * Estás ejecutando la compilación 16215 de Windows o una posterior. [Comprueba el número de compilación](troubleshooting.md#check-your-build-number).
    >   * El componente opcional del subsistema de Windows para Linux está habilitado y se ha reiniciado el equipo.  [Asegúrate de que WSL está habilitado](troubleshooting.md#confirm-wsl-is-enabled).
    
3. Agrega la ruta de acceso de distribución a la variable de entorno PATH de Windows (`C:\Users\Administrator\Ubuntu` en este ejemplo), por ejemplo, mediante PowerShell:
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    Ahora puedes escribir `<distro>.exe` para iniciar la distribución desde cualquier ruta de acceso. Por ejemplo: `ubuntu.exe`

Ahora que está instalada la distribución de Linux, debes [inicializar la nueva instancia de la distribución](initialize-distro.md) antes de usarla.
