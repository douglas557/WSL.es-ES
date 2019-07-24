---
title: Instalar o quitar en la actualización de aniversario de Windows 10 o en Creators Update
description: Instrucciones de instalación y desinstalación de la versión de distribución de la actualización de aniversario de Windows 10
keywords: BashOnWindows, bash, WSL, Windows, subsistema de Windows para Linux, windowssubsystem, Ubuntu, Debian, SuSE, Windows 10, heredado, beta, instalar, quitar, desinstalar, desinstalar, eliminar, desusado
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 0d8fdabd61fadbfc58549a220ead23585a3d3656
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499265"
---
# <a name="guide-to-install-or-uninstall-windows-subsystem-for-linux-on-windows-10-anniversary-update-and-creators-update"></a>Guía para instalar o desinstalar el subsistema de Windows para Linux en la actualización de aniversario de Windows 10 y Creators Update 

Si está ejecutando Windows 10 Creators Update o una versión posterior, [siga las instrucciones de instalación de Windows 10](install-win10.md).

<strong><em><span style="color: #f28014">Las siguientes instrucciones son para los usuarios que ejecutan la actualización de aniversario de Windows 10 o Windows 10 Creators Update.</span></em></strong>

Antes de Windows 10 Fall Creators Update (versión 1709), WSL se lanzó como una característica beta e instaló una única instancia de Ubuntu cuando se ejecutó por primera vez "bash en Ubuntu en Windows" (o bash. exe).

> Aunque puede usar WSL en versiones anteriores de Windows 10, esta versión beta "Legacy distribución" ahora se considera obsoleta. Le recomendamos encarecidamente que ejecute la versión más reciente de Windows 10 disponible. Cada nueva versión de Windows 10 incluye muchos cientos de correcciones y mejoras en WSL por sí solo, lo que permite que haya más aplicaciones y herramientas de Linux que se ejecuten correctamente en WSL.

Si no puede actualizar a Fall Creators Update o posterior, siga estos pasos para habilitar y usar WSL:

1. Activar el modo de desarrollador para ejecutar WSL en la actualización de aniversario de Windows 10 o en Creators Update, debe habilitar el modo de Desarrollador:

    Abrir **configuración** -> **actualizar y seguridad** -> **para desarrolladores**

    Seleccionar el botón de radio modo de desarrollador  
    ![Habilitar el modo de desarrollador](media/updateAndSecurity.png)

    > El requisito de habilitar el modo de desarrollador se [quitó en Windows 10 Fall Creators Update](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)

1. Abra un símbolo del sistema.  Escriba `bash` y presione Entrar

    La primera vez que ejecute bash en Ubuntu en Windows, se le pedirá que acepte la licencia de Canonical. Una vez aceptado, WSL descargará e instalará la instancia de Ubuntu en el equipo y se agregará un acceso directo "Bash on Ubuntu on Windows" al menú Inicio.

    ![Preguntar para instalar Ubuntu](media/bashShellInstall.png)

    La primera vez que ejecute bash en Ubuntu en Windows, se le pedirá que cree un nombre de usuario y una contraseña de UNIX. Siga las [instrucciones de la nueva instancia de distribución](initialize-distro.md) para completar la instalación.

1. Inicie un nuevo shell de Ubuntu:
    * Ejecutar `bash` desde un símbolo del sistema
    * Hacer clic en el acceso directo del menú Inicio "Bash on Ubuntu on Windows"

    
## <a name="uninstallingremoving-the-legacy-distro"></a>Desinstalación/eliminación del distribución heredado
Si actualiza a Windows 10 Fall Creators Update desde una versión anterior de Windows 10 en la que instaló WSL, el distribución existente permanecerá intacto. Sin embargo, le recomendamos ENCARECIdamente que instale una nueva tienda (distribución ASAP) y migre los archivos, los datos, etc. que sean necesarios de su distribución heredado a la nueva distribución.

Para quitar el distribución heredado de la máquina, ejecute lo siguiente desde una línea de comandos o una instancia de PowerShell:

```console
wsl --unregister Legacy
```

Si no usa la versión 1903 o posterior de Windows, es posible que deba ejecutar `wslconfig /u Legacy` o `lxrun /uninstall /full` en su lugar. 

### <a name="manually-deleting-the-legacy-distro"></a>Eliminar manualmente el distribución heredado
Si lo desea, puede eliminar manualmente la instancia heredada. Esto puede ser necesario si se producen problemas al desinstalar el distribución heredado `lxrun.exe`mediante o si se ejecuta Windows 10 Spring 2018 Update (o una versión posterior) que no `lxrun.exe`se distribuyen con.

Para forzar la eliminación de la distribución de WSL heredada, elimine la `%localappdata%\lxss\` carpeta (y todo su subcontenido) mediante el explorador de archivos de Windows o la línea de comandos:

Con PowerShell
```powershell
rm -Recurse $env:localappdata/lxss/
```

Mediante cmd:
```console
DEL /S %localappdata%\lxss\
```
