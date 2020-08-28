---
title: Instalación del subsistema Linux en Windows Server
description: Obtenga información sobre cómo instalar el subsistema Linux en Windows Server. WSL está disponible para su instalación en Windows Server 2019 (versión 1709) y versiones posteriores.
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, subsistemawindows, ubuntu, windows server
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 501bbf78c2d9f59dad945af9c30571317240b79f
ms.sourcegitcommit: fb79750bd71d6ebaed5203b3de71ba85a67227b1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2020
ms.locfileid: "88866145"
---
# <a name="windows-server-installation-guide"></a>Guía de instalación de Windows Server

El Subsistema de Windows para Linux está disponible para su instalación en Windows Server 2019 (versión 1709) y versiones posteriores. En esta guía se describen los pasos necesarios para habilitar WSL en tu máquina.

## <a name="enable-the-windows-subsystem-for-linux"></a>Habilitación del Subsistema de Windows para Linux

Para poder ejecutar distribuciones de Linux en Windows, debes habilitar la característica opcional "Subsistema de Windows para Linux" y reiniciar.

Abre PowerShell como administrador y ejecuta:

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

```

## <a name="download-a-linux-distribution"></a>Descarga de una distribución de Linux

Sigue [estas instrucciones](install-manual.md) para descargar su distribución de Linux favorita.

## <a name="extract-and-install-a-linux-distribution"></a>Extracción e instalación de una distribución de Linux

Ahora que has descargado una distribución de Linux, para extraer su contenido e instalarlo manualmente, sigue estos pasos:

1. Extrae el contenido del paquete `<distro>.appx` mediante PowerShell:

    ```powershell
    Rename-Item .\Ubuntu.appx .\Ubuntu.zip
    Expand-Archive .\Ubuntu.zip .\Ubuntu
    ```

2. Ejecuta la aplicación del iniciador de la distribución en la carpeta de destino. Normalmente, el iniciador se denomina `<distro>.exe` (por ejemplo, `ubuntu.exe`).

    ![Distribución de Ubuntu ampliada en Windows Server](media/server-appx-expand.png)

> [!CAUTION]
> **Error 0x8007007e en la instalación**: Si recibes este error, significa que tu sistema no es compatible con WSL. Asegúrate de que estás ejecutando la compilación 16215 de Windows o una posterior. [Comprueba el número de compilación](troubleshooting.md#check-your-build-number). Además, [confirma que WSL esté habilitado](troubleshooting.md#confirm-wsl-is-enabled) y que el equipo se haya reiniciado después de haber habilitado la característica.  

3. Agrega la ruta de acceso de la distribución a la variable de entorno PATH de Windows (`C:\Users\Administrator\Ubuntu` en este ejemplo) mediante PowerShell:

```powershell
$userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
[System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
```

Ahora puedes escribir `<distro>.exe` para iniciar la distribución desde cualquier ruta de acceso. Por ejemplo: `ubuntu.exe`.

Ahora que está instalada, debes [inicializar la nueva instancia de la distribución](initialize-distro.md) antes de usarla.
