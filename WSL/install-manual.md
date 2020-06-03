---
title: Descarga manual de distribuciones del Subsistema de Windows para Linux (WSL)
description: Instrucciones sobre cómo descargar manualmente distribuciones del Subsistema de Windows para Linux.
keywords: WSL, subsistema de Windows para Linux, instalación manual, instalar manualmente, Microsoft Store, Windows 10s, curl, Add-AppxPackage, servicio a largo plazo, LTSC
ms.date: 05/28/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: 621b2619d6c62e0b6c4e53f7791fc587c1c8f878
ms.sourcegitcommit: 09f5eb0f6062642e5c86deb1f34307ce3429163a
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2020
ms.locfileid: "84211721"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a>Descarga manual de paquetes de distribuciones del subsistema de Windows para Linux

Hay varios escenarios en los que quizás no podrás (o no querrás) instalar distribuciones WSL Linux a través de Microsoft Store. En concreto, es posible que estés ejecutando una SKU de sistema operativo de escritorio de Windows Server o de mantenimiento a largo plazo (LTSC) que no sea compatible Microsoft Store, o que tus administradores o directivas de red corporativa no permitan el uso de Microsoft Store en tu entorno.

En estos casos, aunque WSL esté disponible, ¿cómo se descargan e instalan las distribuciones de Linux en WSL si no se puede acceder a Microsoft Store?

> Nota: **Los entornos de shell de línea de comandos, incluidos Cmd, PowerShell y las distribuciones de Linux/WSL, no se pueden ejecutar en modo Windows 10 S**. Esta restricción existe con el fin de garantizar la integridad y los objetivos de seguridad que ofrece el modo S: Lee [esta publicación](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) para obtener más información.

## <a name="downloading-distros"></a>Descarga de distribuciones

Si la aplicación Microsoft Store no está disponible, puedes descargar e instalar manualmente distribuciones de Linux a través de estos vínculos:
* [Ubuntu 18.04](https://aka.ms/wsl-ubuntu-1804)
* [Ubuntu 18.04 ARM](https://aka.ms/wsl-ubuntu-1804-arm)
* [Ubuntu 16.04](https://aka.ms/wsl-ubuntu-1604)
* [Debian GNU/Linux](https://aka.ms/wsl-debian-gnulinux)
* [Kali Linux](https://aka.ms/wsl-kali-linux-new)
* [OpenSUSE Leap 42](https://aka.ms/wsl-opensuse-42)
* [SUSE Linux Enterprise Server 12](https://aka.ms/wsl-sles-12)
* [Fedora Remix for WSL](https://github.com/WhitewaterFoundry/WSLFedoraRemix/releases/)

Al hacerlo, los paquetes de `<distro>.appx` se descargarán en una carpeta de tu elección. Sigue las [instrucciones de instalación](#installing-your-distro) para instalar las distribuciones descargadas.

## <a name="downloading-distros-via-the-command-line"></a>Descarga de distribuciones a través de la línea de comandos
Si lo prefieres, también puedes descargar tus distribuciones preferidas a través de la línea de comandos:

 ### <a name="download-using-powershell"></a>Descarga con PowerShell
 Para descargar distribuciones con PowerShell, usa el cmdlet [Invoke-WebRequest](https://docs.microsoft.com/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-5.1). A continuación se muestra una instrucción de ejemplo para descargar Ubuntu 16.04.

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> Si la descarga tarda mucho tiempo, establece `$ProgressPreference = 'SilentlyContinue'` para desactivar la barra de progreso.

### <a name="download-using-curl"></a>Descarga mediante curl
Windows 10 Spring 2018 Update (o posterior) incluye la popular [utilidad de línea de comandos curl](https://curl.haxx.se/), con la que puedes invocar solicitudes web (como los comandos HTTP GET, POST, PUT, etc.) desde la línea de comandos. Puedes usar `curl.exe` para descargar las distribuciones anteriores:

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

En el ejemplo anterior, se ejecuta `curl.exe` (no solo `curl`) para garantizar que, en PowerShell, se invoque el ejecutable de curl real, no el alias de curl de PowerShell para [Invoke-WebRequest](https://docs.microsoft.com/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6).

> Nota: El uso de `curl` podría ser preferible si tienes que invocar o crear scripts de pasos de descarga con el shell de Cmd o los scripts `.bat` / `.cmd`.

## <a name="installing-your-distro"></a>Instalación de la distribución
Si usas Windows 10, puedes instalar la distribución con PowerShell. Solo tienes que ir a la carpeta que contiene la distribución descargada de arriba y, en ese directorio, ejecutar el siguiente comando, donde `app_name` es el nombre del archivo .appx de la distribución.  
```Powershell
Add-AppxPackage .\app_name.appx
```

Si usas Windows Server, puedes encontrar las instrucciones de instalación en la página de documentación de [Windows Server](install-on-server.md).

Una vez instalada la distribución, sigue las instrucciones normales para [actualizar a WSL 2](./install-win10.md#update-to-wsl-2) o [crear una nueva cuenta de usuario y una contraseña](./user-support.md).
