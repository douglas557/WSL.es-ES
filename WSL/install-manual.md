---
title: Descargar manualmente el subsistema de Windows para las distribuciones de Linux (WSL)
description: Instrucciones sobre cómo descargar manualmente el subsistema de Windows para las distribuciones de Linux.
keywords: BashOnWindows, bash, wsl, windows, el subsistema de windows para linux, WSL, subsistema de windows, distribución, ubuntu, openSUSE, SLES, debian, kali
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: be1c1331183317d4f970696464110b9968208d21
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063573"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a>Descargar manualmente el subsistema de Windows para los paquetes de distribución de Linux

Hay varios escenarios en los que puede no ser capaz de (o desee) para instalar las distribuciones de Linux de WSL a través de la Microsoft Store. En concreto, puede que esté ejecutando un servidor de Windows o la SKU del sistema operativo que no es compatible con Microsoft Store, o sus directivas de red corporativa y/o los administradores para no permitir el uso de Microsoft Store en su entorno de escritorio de mantenimiento a largo plazo (LTSB/LTSC).

En estos casos, mientras que WSL sí está disponible, ¿cómo descargar e instalar distribuciones de Linux en WSL si no se puede obtener acceso al almacén?

> Nota: **Entornos de shell de línea de comandos, incluidos las distribuciones de Linux/WSL, Cmd y PowerShell no se pueden ejecutar en modo de Windows 10 S**. Esta restricción existe con el fin de garantizar los objetivos de integridad y seguridad que ofrece el modo S: Lectura [esta publicación](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) para obtener más información.

## <a name="downloading-distros"></a>Descarga de distribuciones

Si la aplicación de Microsoft Store no está disponible, puede descargar e instalar manualmente las distribuciones de Linux, haga clic en estos vínculos:
* [Ubuntu 18.04](https://aka.ms/wsl-ubuntu-1804)
* [Ubuntu 18.04 ARM](https://aka.ms/wsl-ubuntu-1804-arm)
* [Ubuntu 16.04](https://aka.ms/wsl-ubuntu-1604)
* [Debian GNU/Linux](https://aka.ms/wsl-debian-gnulinux)
* [Kali Linux](https://aka.ms/wsl-kali-linux)
* [OpenSUSE](https://aka.ms/wsl-opensuse-42)
* [SLES](https://aka.ms/wsl-sles-12)

Esto hará que el `<distro>.appx` paquetes para descargar en una carpeta de su elección. Siga el [las instrucciones de instalación](#installing-your-distro) para instalar su distro(s) descargado.

## <a name="downloading-distros-via-the-command-line"></a>Distribuciones de descarga a través de la línea de comandos
Si lo prefiere, también puede descargar el distro(s) preferida a través de la línea de comandos:

 ### <a name="download-using-powershell"></a>Descargar mediante PowerShell
 Para descargar las distribuciones con PowerShell, use el [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) cmdlet. Aquí es una instrucción de ejemplo para descargar Ubuntu 16.04.

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> Si la descarga tarda mucho tiempo, desactive la barra de progreso estableciendo `$ProgressPreference = 'SilentlyContinue'`

### <a name="download-using-curl"></a>Descargar mediante curl
Actualización de Windows 10 Spring 2018 (o posterior) incluye el popular [curl utilidad de línea de comandos](https://curl.haxx.se/) con el que puede invocar las solicitudes de web (es decir, HTTP GET, POST, PUT, comandos etc.) desde la línea de comandos. Puede usar `curl.exe` para descargar las distribuciones anteriores:

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

En el ejemplo anterior, `curl.exe` se ejecuta (no solo `curl`) garantizar que, en PowerShell, el archivo ejecutable de curl real se invoca, no la curl de PowerShell alias de [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)

> Nota: Uso de `curl` podría ser preferible si tiene que invocar comandos o mediante el shell de Cmd de pasos de descarga o `.bat`  /  `.cmd` secuencias de comandos.

## <a name="installing-your-distro"></a>Instalación de la distribución
Para obtener instrucciones sobre cómo instalar su distro(s) descargado, consulte el [Windows Desktop](install-win10.md) o [Windows Server](install-on-server.md) instrucciones de instalación.
