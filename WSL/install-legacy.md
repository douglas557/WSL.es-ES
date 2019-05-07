---
title: Instalar o quitar en Windows 10 Anniversary Update o Creators Update
description: Instrucciones de instalación y desinstalación para el heredado, la distribución beta en Windows 10 Anniversary Update o Creators Update
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, windowssubsystem, ubuntu, debian, suse, windows 10, heredado, beta, instalar, quitar, desinstalar, desinstalar, eliminación, en desuso
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: b31bb3a542b8481c723df42292e20e364680722d
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063593"
---
# <a name="guide-to-install-or-uninstall-windows-subsystem-for-linux-on-windows-10-anniversary-update-and-creators-update"></a>Guía para instalar o desinstalar el subsistema de Windows para Linux en Windows 10 Anniversary Update y Creators Update 

Si está ejecutando Windows 10 Creators Update o posterior, por favor, [siga las instrucciones de instalación de Windows 10](install-win10.md).

<strong><em><span style="color: #f28014">Las instrucciones siguientes sirven para usuarios que ejecutan Windows 10 Anniversary Update o Windows 10 Creators Update</span></em></strong>

Antes de Windows 10 Fall Creators Update (versión 1709), WSL se lanzó como característica beta e instala una sola instancia de Ubuntu cuando "Bash en Ubuntu en Windows" (o Bash.exe) se ejecuta en primer lugar.

> Aunque puede usar WSL en versiones anteriores de Windows 10, esta versión beta "distribución heredada" ahora se considera obsoleta. Se recomienda encarecidamente ejecutar la versión más reciente de Windows 10 disponibles. Cada nueva versión de Windows 10 incluye muchos cientos de correcciones y mejoras en WSL por sí solo, lo que permite más herramientas de Linux y aplicaciones se ejecuten correctamente en WSL.

Si no se puede actualizar a Fall Creators Update o posterior, siga los pasos siguientes para habilitar y usar WSL:

1. Activar el modo de desarrollador para ejecutarse WSL en Windows 10 Anniversary Update o Creators Update, debe habilitar el modo de programador:

    Abra **configuración** -> **actualización y seguridad** -> **para desarrolladores**

    Seleccione el botón de radio del modo de programador  
    ![Habilitar el modo de desarrollador](media/updateAndSecurity.png)

    > El requisito para habilitar el modo de programador era [quitado en Windows 10 Fall Creators Update](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)

1. Abra un símbolo del sistema.  Tipo `bash` y presione ENTRAR

    La primera vez que ejecuta Bash en Ubuntu en Windows, se pedirá que acepte la licencia de Canonical. Una vez accpted, WSL descargará e instalará la instancia de Ubuntu en su equipo, y se agregará un acceso directo de "Bash en Ubuntu en Windows" en el menú Inicio.

    ![Símbolo del sistema para la instalación de Ubuntu](media/bashShellInstall.png)

    La primera vez que ejecuta Bash en Ubuntu en Windows, se le indicará que cree un nombre de usuario de UNIX y una contraseña. Siga el [nuevas instrucciones de la instancia de distribución](initialize-distro.md) para completar la instalación

1. Iniciar un nuevo shell de Ubuntu, ya sea:
    * Ejecutando `bash` desde un símbolo
    * Al hacer clic en el acceso directo "Bash en Ubuntu en Windows" del menú Inicio

    
## <a name="uninstallingremoving-the-legacy-distro"></a>Desinstalando o quitando la distribución heredada
Si actualiza desde una versión anterior de Windows 10 en el que instaló WSL para Windows 10 Fall Creators Update, la distribución existente permanecerá intacta. Sin embargo, nos FUERTEMENTE recomienda instalar una distribución nueva entrega de Store ASAP y migrar los archivos necesarios, datos, etc. de su distribución heredada a la distribución nuevo.

Para quitar la distribución heredada de la máquina, ejecute lo siguiente desde una instancia de la línea de comandos o PowerShell:

```console
lxrun /uninstall /full
```

### <a name="manually-deleting-the-legacy-distro"></a>Eliminación manual de la distribución heredada
Si lo desea, puede eliminar manualmente la instancia antigua. Esto puede ser necesario si tiene problemas al desinstalar la distribución heredada utilizando `lxrun.exe`, o se está ejecutando Windows 10 Spring 2018 Update (o posterior) que no se suministran con `lxrun.exe`.

Para forzar la eliminación de la distribución WSL heredada, eliminar el `%localappdata%\lxss\` carpeta (y todos los de subcontenido) mediante el Explorador de archivos de Windows o la línea de comandos:

Con PowerShell
```powershell
rm -Recurse $env:localappdata/lxss/
```

Uso de Cmd:
```console
DEL /S %localappdata%\lxss\
```
