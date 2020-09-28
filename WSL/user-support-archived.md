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
# <a name="wsl-user-account-updates-on-previous-windows-versions"></a><span data-ttu-id="36c4c-103">Actualizaciones de la cuenta de usuario de WSL en versiones anteriores de Windows</span><span class="sxs-lookup"><span data-stu-id="36c4c-103">WSL User Account updates on Previous Windows Versions</span></span>

<span data-ttu-id="36c4c-104">Este contenido se archiva para usuarios de versiones anteriores del sistema operativo Windows que admiten el subsistema para Linux y necesitan compatibilidad con la actualización de cuentas de usuario de Linux.</span><span class="sxs-lookup"><span data-stu-id="36c4c-104">This content is archived for users of earlier versions of Windows operating system that support the subsystem for Linux and need support with updating Linux user accounts.</span></span>

<span data-ttu-id="36c4c-105">Para obtener la documentación actual, consulte [cuentas de usuario para el subsistema de Windows para Linux](./user-support.md).</span><span class="sxs-lookup"><span data-stu-id="36c4c-105">For current documentation, see [User Accounts for Windows Subsystem for Linux](./user-support.md).</span></span>

### <a name="for-creators-update-version-of-windows-and-earlier"></a><span data-ttu-id="36c4c-106">Para la versión de Windows de Creators Update y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="36c4c-106">For Creators Update version of Windows and earlier</span></span>

<span data-ttu-id="36c4c-107">Si estás ejecutando Windows 10 Creators Update o una versión anterior, puedes cambiar el usuario de Bash predeterminado mediante la ejecución de los siguientes comandos:</span><span class="sxs-lookup"><span data-stu-id="36c4c-107">If you're running Windows 10 Creators update or earlier, you can change the default Bash user by running the following commands:</span></span>

1. <span data-ttu-id="36c4c-108">Cambia el usuario predeterminado a `root`:</span><span class="sxs-lookup"><span data-stu-id="36c4c-108">Change the default user to `root`:</span></span>

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. <span data-ttu-id="36c4c-109">Ejecuta `bash.exe` para iniciar sesión como `root`:</span><span class="sxs-lookup"><span data-stu-id="36c4c-109">Run `bash.exe` to now login as `root`:</span></span>

    ```console
    C:\> bash.exe
    ```

1. <span data-ttu-id="36c4c-110">Restablece la contraseña con el comando de contraseña de la distribución y cierra la consola de Linux:</span><span class="sxs-lookup"><span data-stu-id="36c4c-110">Reset your password using the distribution's password command, and close the Linux Console:</span></span>

    ```BASH
    $ passwd username
    $ exit
    ```

1. <span data-ttu-id="36c4c-111">Desde Windows CMD, restablece el usuario predeterminado de nuevo a la cuenta de usuario de Linux normal:</span><span class="sxs-lookup"><span data-stu-id="36c4c-111">From Windows CMD, reset your default user back to your normal Linux user account:</span></span>

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a><span data-ttu-id="36c4c-112">Para Fall Creators Update y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="36c4c-112">For Fall Creators Update and later</span></span>

<span data-ttu-id="36c4c-113">Para ver qué comandos están disponibles para una distribución determinada, ejecuta `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="36c4c-113">To see what commands are available for a particular distribution, run `[distro.exe] /?`.</span></span>
    
<span data-ttu-id="36c4c-114">Por ejemplo, con Ubuntu instalado:</span><span class="sxs-lookup"><span data-stu-id="36c4c-114">For example, with Ubuntu installed:</span></span>

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

<span data-ttu-id="36c4c-115">Instrucciones paso a paso con Ubuntu:</span><span class="sxs-lookup"><span data-stu-id="36c4c-115">Step by step instructions using Ubuntu:</span></span>

1. <span data-ttu-id="36c4c-116">Abre CMD.</span><span class="sxs-lookup"><span data-stu-id="36c4c-116">Open CMD</span></span>
1. <span data-ttu-id="36c4c-117">Establece el usuario de Linux predeterminado en `root`:</span><span class="sxs-lookup"><span data-stu-id="36c4c-117">Set the default Linux user to `root`:</span></span>

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. <span data-ttu-id="36c4c-118">Inicia la distribución de Linux (`ubuntu`).</span><span class="sxs-lookup"><span data-stu-id="36c4c-118">Launch your Linux distribution (`ubuntu`).</span></span>  <span data-ttu-id="36c4c-119">Iniciarás sesión automáticamente como `root`:</span><span class="sxs-lookup"><span data-stu-id="36c4c-119">You will automatically login as `root`:</span></span>

1. <span data-ttu-id="36c4c-120">Restablece la contraseña con el comando `passwd`:</span><span class="sxs-lookup"><span data-stu-id="36c4c-120">Reset your password using the `passwd` command:</span></span>

    ```BASH
    $ passwd username
    ```

1. <span data-ttu-id="36c4c-121">Desde Windows CMD, restablece el usuario predeterminado de nuevo a la cuenta de usuario de Linux normal.</span><span class="sxs-lookup"><span data-stu-id="36c4c-121">From Windows CMD, reset your default user back to your normal Linux user account.</span></span>

    ```console
    C:\> ubuntu config --default-user username
    ```
