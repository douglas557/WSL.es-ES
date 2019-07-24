---
title: Cuenta de usuario de Linux y permisos
description: Referencia de las cuentas de usuario y la administración de permisos con el subsistema de Windows para Linux.
keywords: BashOnWindows, bash, WSL, Windows, subsistema de Windows para Linux, windowssubsystem, Ubuntu, cuentas de usuario
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.openlocfilehash: 0d00b43d059e72edd4e2a5b9591c29441f461fca
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/14/2019
ms.locfileid: "67040826"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a>Cuentas de usuario y permisos para el subsistema de Windows para Linux

La creación de un usuario de Linux es el primer paso para configurar una nueva distribución de Linux en WSL.  La primera cuenta de usuario que cree se configura automáticamente con unos cuantos atributos especiales:

1. Es el usuario predeterminado: inicia sesión automáticamente en el inicio.
1. De forma predeterminada, es administrador de Linux (un miembro del grupo sudo).

Cada distribución de Linux que se ejecuta en el subsistema de Windows para Linux tiene sus propias cuentas de usuario y contraseñas de Linux.  Tendrá que configurar una cuenta de usuario de Linux cada vez que agregue una distribución, reinstale o restablezca.  Las cuentas de usuario de Linux no solo son independientes por distribución, sino que también son independientes de la cuenta de usuario de Windows.

## <a name="resetting-your-linux-password"></a>Restablecimiento de la contraseña de Linux

Si tiene acceso a su cuenta de usuario de Linux y conoce la contraseña actual, cámbiela con las herramientas de restablecimiento de contraseñas de Linux de esa `passwd`distribución, lo que es más probable.

Si no es una opción, dependiendo de la distribución, es posible que pueda restablecer la contraseña restableciendo el usuario predeterminado.

WSL ofrece una etiqueta de usuario predeterminada para identificar la cuenta de usuario que inicia sesión automáticamente al iniciar un WSL.  Dado que muchas distribuciones incluyen comandos para establecer el usuario predeterminado en raíz y también un usuario raíz sin contraseña establecida, cambiar el usuario predeterminado a raíz es una herramienta útil para cosas como el restablecimiento de contraseñas.

### <a name="for-creators-update-and-earlier"></a>Para Creators Update y versiones anteriores
Si está ejecutando Windows 10 Creators Update o una versión anterior, puede cambiar el usuario de Bash predeterminado mediante la ejecución de los siguientes comandos:

1. Cambie el usuario predeterminado a `root`:

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. Ejecute `bash.exe` para iniciar sesión ahora `root`como:

    ```console
    C:\> bash.exe
    ```

1. Restablezca la contraseña con el comando de contraseña de la distribución y cierre la consola de Linux:

    ```BASH
    $ passwd username
    $ exit
    ```

1. En Windows CMD, restablezca el usuario predeterminado de nuevo a su cuenta de usuario de Linux normal:

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a>Para Fall Creators Update y versiones posteriores
Para ver qué comandos están disponibles para una distribución determinada, ejecute `[distro.exe] /?`.
    
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

1. Abrir CMD
1. Establezca el usuario de Linux predeterminado `root`en:

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. Inicie la distribución de Linux`ubuntu`().  Iniciará sesión automáticamente como `root`:

1. Restablezca la contraseña con el `passwd` comando:

    ```BASH
    $ passwd username
    ```

1. En Windows CMD, restablezca el usuario predeterminado de nuevo a su cuenta de usuario de Linux normal.

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a>Permisos

Hay dos conceptos importantes que se deben tener en cuenta cuando se trata de permisos en WSL:

1. El modelo de permisos de Windows rige los derechos de un proceso en los recursos de Windows
2. El modelo de permisos de Linux controla los derechos de un proceso para los recursos de Linux

Al ejecutar Linux en WSL, Linux tendrá los mismos permisos de Windows que el proceso que lo inicia. Linux puede iniciarse en uno de los dos niveles de permiso:

* Normal (no elevado): Linux se ejecuta con los permisos del usuario que ha iniciado sesión
* Elevado/administrador: Linux se ejecuta con permisos elevados o de administrador de Windows

> Dado que los procesos elevados pueden tener acceso a la configuración de todo el sistema y los datos protegidos o modificarlos (y, por consiguiente, dañarlos), **Evite** el inicio de procesos elevados a menos que sea absolutamente necesario-si son aplicaciones o herramientas de Windows o Linux/ visto!

Los permisos de Windows anteriores son independientes de los permisos de una instancia de Linux: Los "privilegios raíz" de Linux solo afectan a los derechos del usuario en el entorno de Linux & sistema de archivos; no tienen ningún impacto en los privilegios de Windows concedidos. Por lo tanto, la ejecución de un proceso de Linux como `sudo`raíz (por ejemplo, Via) solo concede derechos de administrador de procesos en el entorno de Linux.

**Ejemplo:**     
Una sesión de bash con privilegios de administrador de `cd /mnt/c/Users/Administrator` Windows puede tener acceso mientras que una sesión de Bash sin privilegios de administrador verá el error "Permiso denegado".

En Linux, al `sudo cd /mnt/c/Users/Administrator` escribir no se concederá acceso al directorio del administrador, ya que Windows administra los permisos dentro de Windows.

El modelo de permisos de Linux es importante en el entorno de Linux, donde el usuario tiene permisos basados en el usuario actual de Linux.

**Ejemplo:**  
Se puede ejecutar `sudo apt update`un usuario del grupo sudo.
