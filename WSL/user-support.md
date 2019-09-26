---
title: Cuentas de usuario y permisos de Linux
description: Material de referencia para la administración de permisos y cuentas de usuario con el subsistema de Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, subsistemawindows, ubuntu, cuentas de usuario
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: de18c128854ef9a39a26551db2ea0aee97b8ab4f
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122684"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a>Cuentas de usuario y permisos para el subsistema de Windows para Linux

La creación de un usuario de Linux es el primer paso para configurar una nueva distribución de Linux en WSL.  La primera cuenta de usuario que se crea se configura automáticamente con unos cuantos atributos especiales:

1. Se trata del usuario predeterminado: inicia sesión automáticamente en el inicio.
1. De manera predeterminada, es administrador de Linux (un miembro del grupo sudo).

Cada distribución de Linux que se ejecuta en el subsistema de Windows para Linux tiene sus propias cuentas de usuario y contraseñas de Linux.  Tendrás que configurar una cuenta de usuario de Linux cada vez que reinstales, restablezcas o agregues una distribución.  Las cuentas de usuario de Linux no solo son independientes por distribución, sino que también son independientes de la cuenta de usuario de Windows.

## <a name="resetting-your-linux-password"></a>Restablecimiento de la contraseña de Linux

Si tienes acceso a la cuenta de usuario de Linux y conoces la contraseña actual, usa las herramientas de restablecimiento de contraseñas de Linux para cambiarla de esa distribución (que probablemente es `passwd`).

Si esto no es una opción, dependiendo de la distribución, es posible que se pueda restablecer la contraseña restableciendo el usuario predeterminado.

WSL ofrece una etiqueta de usuario predeterminada para identificar la cuenta de usuario que inicia sesión automáticamente al iniciar un WSL.  Dado que muchas distribuciones incluyen comandos para establecer el usuario predeterminado en raíz y también un usuario raíz sin contraseña establecida, cambiar el usuario predeterminado a raíz es una herramienta útil para acciones como el restablecimiento de contraseñas.

### <a name="for-creators-update-and-earlier"></a>Para la actualización Creators Update y versiones anteriores
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

## <a name="permissions"></a>Permisos

Hay dos conceptos importantes que se deben tener en cuenta cuando se trata de permisos en WSL:

1. El modelo de permisos de Windows rige los derechos de un proceso en los recursos de Windows.
2. El modelo de permisos de Linux rige los derechos de un proceso en los recursos de Linux.

Al ejecutar Linux en WSL, Linux tendrá los mismos permisos de Windows que el proceso que lo inicia. Linux puede iniciarse en uno de los dos niveles de permiso:

* Normal (no elevado): Linux se ejecuta con los permisos del usuario que ha iniciado sesión.
* Elevado/administrador: Linux se ejecuta con permisos de Windows elevados o de administrador.

> Dado que los procesos elevados pueden tener acceso a la configuración de todo el sistema y los datos protegidos o de todo el sistema y modificarlos (y ,por consiguiente, dañarlos), **EVITA** el inicio de procesos elevados a menos que sea absolutamente necesario, ya se trate de aplicaciones, herramientas o shells de Windows o Linux.

Los permisos de Windows anteriores son independientes de los permisos de una instancia de Linux: Los "privilegios raíz" de Linux solo afectan a los derechos del usuario en el sistema de archivos y entorno de Linux; no tienen ningún impacto en los privilegios de Windows concedidos. Por lo tanto, la ejecución de un proceso de Linux como raíz (por ejemplo, a través de `sudo`) solo concede derechos de administrador de procesos en el entorno de Linux.

**Ejemplo:**     
Una sesión de Bash con privilegios de administrador de Windows puede tener acceso a `cd /mnt/c/Users/Administrator`, mientras que una sesión de Bash sin privilegios de administrador verá el error "Permiso denegado".

En Linux, al escribir `sudo cd /mnt/c/Users/Administrator` no se concederá acceso al directorio del administrador, ya que Windows administra los permisos dentro de Windows.

El modelo de permisos de Linux es importante en el entorno de Linux, donde el usuario tiene permisos basados en el usuario actual de Linux.

**Ejemplo:**  
Un usuario del grupo sudo puede ejecutar `sudo apt update`.
