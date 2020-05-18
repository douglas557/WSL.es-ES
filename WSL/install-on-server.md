---
title: Instalación del subsistema Linux en Windows Server
description: Instrucciones de instalación del subsistema Linux en Windows Server.
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, subsistemawindows, ubuntu, windows server
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 86fd7de0ef45af760f46bb2a18932f513b813609
ms.sourcegitcommit: 1b6191351bbf9e95f3c28fc67abe4bf1bcfd3336
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2020
ms.locfileid: "83270889"
---
# <a name="windows-server-installation-guide"></a>Guía de instalación de Windows Server

El Subsistema de Windows para Linux está disponible para su instalación en Windows Server 2019 (versión 1709) y versiones posteriores. En esta guía se describen los pasos necesarios para habilitar WSL en tu máquina.

## <a name="enable-the-windows-subsystem-for-linux"></a>Habilitación del Subsistema de Windows para Linux

Para poder ejecutar distribuciones de Linux en Windows, debes habilitar la característica opcional "Subsistema de Windows para Linux" y reiniciar.

Abre PowerShell como administrador y ejecuta:

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

```

**Si buscas obtener una compatibilidad completa con las llamadas del sistema y un mayor rendimiento de E/S, lee la documentación que hay a continuación para instalar WSL 2.**

WSL 2 solo está disponible en Windows 10, versión 2004, compilación 19041 o posteriores. Tendrás que [actualizar la versión de Windows](ms-settings:windowsupdate) y [unirte al programa Windows Insider](https://insider.windows.com/insidersigninboth/) en el anillo "Versión preliminar" hasta el lanzamiento de la versión pública a finales de mayo.

**Si continúas con WSL 1, reinicia la máquina cuando se te pida y sigue con la instalación [aquí](./install-on-server.md#download-a-linux-distribution)** .

## <a name="enable-the-virtual-machine-platform-optional-component"></a>Habilitación del componente opcional Plataforma de máquina virtual

Asegúrate de que el componente opcional "Plataforma de máquina virtual" esté instalado. Para hacerlo ejecuta el siguiente comando en PowerShell:

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
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
