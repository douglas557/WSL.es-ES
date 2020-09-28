---
title: Actualizaciones de la cuenta de usuario de WSL en versiones anteriores de Windows
description: Referencia de las versiones anteriores de Windows para actualizar las cuentas de usuario de Linux con el subsistema de Windows para Linux.
ms.date: 01/20/2020
ms.topic: article
ROBOTS: NOINDEX
ms.openlocfilehash: 33a42c8f3bd518fa45df2874a6c59b76cd8ec80a
ms.sourcegitcommit: b15b847b87d29a40de4a1517315949bce9c7a3d5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "91413366"
---
# <a name="wsl-user-account-updates-on-previous-windows-versions"></a>Actualizaciones de la cuenta de usuario de WSL en versiones anteriores de Windows

Este contenido se archiva para usuarios de versiones anteriores del sistema operativo Windows que admiten el subsistema para Linux y necesitan compatibilidad con la actualización de cuentas de usuario de Linux.

Para obtener la documentación actual, consulte [cuentas de usuario para el subsistema de Windows para Linux](./user-support.md).

### <a name="for-creators-update-version-of-windows-and-earlier"></a>Para la versión de Windows de Creators Update y versiones anteriores

Si estás ejecutando Windows 10 Creators Update o una versión anterior, puedes cambiar el usuario de Bash predeterminado mediante la ejecución de los siguientes comandos:

1. Cambia el usuario predeterminado a `root`:

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. Ejecuta `bash.exe` para iniciar sesión como `root`:

    ```console
    C:\> bash.exe
    ```

1. Restablece la contraseña con el comando de contraseña de la distribución y cierra la consola de Linux:

    ```BASH
    $ passwd username
    $ exit
    ```

1. Desde Windows CMD, restablece el usuario predeterminado de nuevo a la cuenta de usuario de Linux normal:

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a>Para Fall Creators Update y versiones posteriores

Para ver qué comandos están disponibles para una distribución determinada, ejecuta `[distro.exe] /?`.
    
Por ejemplo, con Ubuntu instalado:

```console
C:\> ubuntu.exe /?

Launches or configures a linux distribution.

Usage:
    <no args>
      - Launches the distro's default behavior. By default, this launches your default shell.

    run <command line>
      - Run the given command line in that distro, using the default configuration.
      - Everything after `run ` is passed to the linux LaunchProcess cal

    config [setting [value]]
      - Configure certain settings for this distro.
      - Settings are any of the following (by default)
        - `--default-user <username>`: Set the default user for this distro to <username>

    clean
      - Uninstalls the distro. The appx remains on your machine. This can be
        useful for "factory resetting" your instance. This removes the linux
        filesystem from the disk, but not the app from your PC, so you don't
        need to redownload the entire tar.gz again.

    help
      - Print this usage message.
```

Instrucciones paso a paso con Ubuntu:

1. Abre CMD.
1. Establece el usuario de Linux predeterminado en `root`:

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. Inicia la distribución de Linux (`ubuntu`).  Iniciarás sesión automáticamente como `root`:

1. Restablece la contraseña con el comando `passwd`:

    ```BASH
    $ passwd username
    ```

1. Desde Windows CMD, restablece el usuario predeterminado de nuevo a la cuenta de usuario de Linux normal.

    ```console
    C:\> ubuntu config --default-user username
    ```
