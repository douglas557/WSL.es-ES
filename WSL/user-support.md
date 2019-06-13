---
title: Permisos y la cuenta de usuario de Linux
description: Referencia de las cuentas de usuario y la administración de permisos con el subsistema de Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, windowssubsystem, ubuntu, cuentas de usuario
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.openlocfilehash: 0d00b43d059e72edd4e2a5b9591c29441f461fca
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040826"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a>Las cuentas de usuario y los permisos para el subsistema de Windows para Linux

Creación de su usuario de Linux es el primer paso para configurar una nueva distribución de Linux en WSL.  La primera cuenta de usuario que cree se configura automáticamente con unos cuantos atributos especiales:

1. Es el usuario de forma predeterminada, inicia sesión automáticamente en el inicio.
1. Es el Administrador de Linux (un miembro del grupo de sudo) de forma predeterminada.

Cada distribución de Linux que se ejecuta en el subsistema de Windows para Linux tiene sus propias cuentas de usuario de Linux y las contraseñas.  Tendrá que configurar cada vez que agregue una distribución, vuelva a instalar o restablecimiento de una cuenta de usuario de Linux.  Cuentas de usuario de Linux no sólo son independientes por cada distribución, también son independientes de la cuenta de usuario de Windows.

## <a name="resetting-your-linux-password"></a>Al restablecer la contraseña de Linux

Si conoce la contraseña actual, cambiarla y tener acceso a su cuenta de usuario de Linux con Linux de restablecimiento de contraseña herramientas de distribución--probablemente `passwd`.

Si es no es una opción, dependiendo de la distribución, puede restablecer la contraseña, restablecer el usuario predeterminado.

WSL proporciona una etiqueta de usuario predeterminada para identificar automáticamente la cuenta de usuario que inicia sesión cuando se inicia un WSL.  Puesto que muchas distribuciones incluyen los comandos para establecer el usuario predeterminado en la raíz y también un usuario raíz con ninguna contraseña establecida, cambiar el usuario predeterminado para la raíz es una herramienta útil para tareas como el restablecimiento de contraseña.

### <a name="for-creators-update-and-earlier"></a>Creators Update y versiones anteriores
Si está ejecutando Windows 10 Creators update o versiones anteriores, puede cambiar el usuario de Bash predeterminado mediante la ejecución de los siguientes comandos:

1. Cambiar el usuario predeterminado para `root`:

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. Ejecute `bash.exe` para iniciar sesión ahora como `root`:

    ```console
    C:\> bash.exe
    ```

1. Restablecer su contraseña mediante el comando de contraseña de la distribución y cierre la consola de Linux:

    ```BASH
    $ passwd username
    $ exit
    ```

1. Desde CMD de Windows, restablecer el usuario predeterminado en su cuenta de usuario de Linux normal:

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a>Para la actualización Fall Creators Update y versiones posteriores
Para ver qué comandos están disponibles para una distribución particular, ejecute `[distro.exe] /?`.
    
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

1. Abra CMD
1. Establece el usuario de Linux de forma predeterminada en `root`:

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. Inicie la distribución de Linux (`ubuntu`).  Configurará automáticamente como el inicio de sesión `root`:

1. Restablecer su contraseña mediante el `passwd` comando:

    ```BASH
    $ passwd username
    ```

1. Desde CMD de Windows, restablecer el usuario predeterminado a su cuenta de usuario de Linux normal.

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a>Permisos

Hay dos conceptos importantes a tener en cuenta cuando se trata de permisos en WSL:

1. El modelo de permisos de Windows controla los derechos de un proceso a los recursos de Windows
2. El modelo de permisos de Linux controla los derechos de un proceso a los recursos de Linux

Cuando se ejecuta Linux en WSL, Linux tendrán los mismos permisos de Windows que el proceso que lo inicia. Linux se puede iniciar en uno de dos niveles de permisos:

* Normal (sin privilegios elevados): Linux se ejecuta con los permisos del usuario que inició sesión
* Administración/con privilegios elevados: Linux se ejecuta con permisos de administrador con permisos elevados/Windows

> Porque los procesos elevados pueden acceso o modificar (y, por tanto, dañar)-wide y proteger el sistema de datos y la configuración de todo el sistema **Evite** iniciar procesos con privilegios elevados a menos que sea absolutamente necesario - ya sean Windows o Linux ¡aplicaciones/tools/shells!

Los permisos de Windows anteriores son independientes de los permisos dentro de una instancia de Linux: "Privilegios de raíz" de Linux afecten solo a los derechos del usuario dentro del entorno de Linux & del sistema de archivos; no tienen ningún impacto en los privilegios de Windows concedidos. Por lo tanto, que se ejecuta un proceso de Linux como raíz (por ejemplo, mediante `sudo`) solo concede que procesan los derechos de administrador en el entorno de Linux.

**Ejemplo:**     
Puede tener acceso una sesión de Bash con privilegios de administrador de Windows `cd /mnt/c/Users/Administrator` mientras una sesión de Bash sin privilegios de Administrador vería un error "Permiso denegado".

En Linux, escriba `sudo cd /mnt/c/Users/Administrator` no concederá acceso al directorio del administrador porque los permisos dentro de Windows administrados por Windows.

El modelo de permisos de Linux es importante cuando se encuentra dentro del entorno de Linux donde el usuario tenga permisos en función del usuario actual de Linux.

**Ejemplo:**  
Puede ejecutar un usuario en el grupo de sudo `sudo apt update`.
