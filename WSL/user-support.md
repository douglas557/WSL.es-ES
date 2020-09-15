---
title: Creación y actualización de cuentas de usuario para distribuciones de Linux
description: Material de referencia para la administración de permisos y cuentas de usuario con el subsistema de Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, subsistemawindows, ubuntu, cuentas de usuario
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: cdb510b8195f18f89ea475889c34850234b7c0e8
ms.sourcegitcommit: 6ff046993e9f196cdfa04f5f91130e0e4ff1e7fa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/03/2020
ms.locfileid: "89427192"
---
# <a name="create-a-user-account-and-password-for-your-new-linux-distribution"></a><span data-ttu-id="d7d8f-104">Creación de una cuenta de usuario y una contraseña para la nueva distribución de Linux</span><span class="sxs-lookup"><span data-stu-id="d7d8f-104">Create a user account and password for your new Linux distribution</span></span>

<span data-ttu-id="d7d8f-105">Una vez hayas [habilitado WSL e instalado una distribución de Linux de Microsoft Store](./install-win10.md), el primer paso que debes completar al abrir la distribución recién instalada de Linux es crear una cuenta, incluido un **nombre de usuario** y una **contraseña**.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-105">Once you have [enabled WSL and installed a Linux distribution from the Microsoft Store](./install-win10.md), the first step you will be asked to complete when opening your newly installed Linux distribution is to create an account, including a **User Name** and **Password**.</span></span>

- <span data-ttu-id="d7d8f-106">El **nombre de usuario** y la **contraseña** son específicos de la distribución de Linux y no tienen relación con tu nombre de usuario de Windows.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-106">This **User Name** and **Password** is specific to your Linux distribution and has no bearing on your Windows user name.</span></span>

- <span data-ttu-id="d7d8f-107">Cuando hayas creado el **nombre de usuario** y la **contraseña**, la cuenta será el usuario predeterminado de la distribución e iniciará sesión automáticamente al inicio.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-107">Once you create this **User Name** and **Password**, the account will be your default user for the distribution and automatically sign-in on launch.</span></span>

- <span data-ttu-id="d7d8f-108">Recuerda que esta cuenta se considerará el administrador de Linux y tendrá la capacidad de ejecutar comandos administrativos `sudo` (es decir, de superusuario).</span><span class="sxs-lookup"><span data-stu-id="d7d8f-108">This account will be considered the Linux administrator, with the ability to run `sudo` (Super User Do) administrative commands.</span></span>

- <span data-ttu-id="d7d8f-109">Cada distribución de Linux que se ejecuta en el subsistema de Windows para Linux tiene sus propias cuentas de usuario y contraseñas de Linux.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-109">Each Linux distribution running on the Windows Subsystem for Linux has its own Linux user accounts and passwords.</span></span>  <span data-ttu-id="d7d8f-110">Tendrás que configurar una cuenta de usuario de Linux cada vez que reinstales, restablezcas o agregues una distribución.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-110">You will have to configure a Linux user account every time you add a distribution, reinstall, or reset.</span></span>

![Desempaquetado de Ubuntu en la consola de Windows](media/UbuntuInstall.png)

## <a name="update-and-upgrade-packages"></a><span data-ttu-id="d7d8f-112">Actualización de paquetes</span><span class="sxs-lookup"><span data-stu-id="d7d8f-112">Update and upgrade packages</span></span>

<span data-ttu-id="d7d8f-113">La mayoría de las distribuciones incluyen un catálogo de paquetes vacío o mínimo.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-113">Most distributions ship with an empty or minimal package catalog.</span></span> <span data-ttu-id="d7d8f-114">Te recomendamos encarecidamente que actualices periódicamente el catálogo de paquetes, así como los paquetes instalados mediante el administrador de paquetes preferido de la distribución.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-114">We strongly recommend regularly updating your package catalog and upgrading your installed packages using your distribution's preferred package manager.</span></span> <span data-ttu-id="d7d8f-115">Para Debian y Ubuntu, usa apt:</span><span class="sxs-lookup"><span data-stu-id="d7d8f-115">For Debian/Ubuntu, use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

<span data-ttu-id="d7d8f-116">Windows no actualiza automáticamente las distribuciones de Linux.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-116">Windows does not automatically update or upgrade your Linux distribution(s).</span></span> <span data-ttu-id="d7d8f-117">Se trata de una tarea que la mayoría de los usuarios de Linux prefieren controlar por sí mismos.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-117">This is a task that the most Linux users prefer to control themselves.</span></span>

## <a name="reset-your-linux-password"></a><span data-ttu-id="d7d8f-118">Restablecimiento de la contraseña de Linux</span><span class="sxs-lookup"><span data-stu-id="d7d8f-118">Reset your Linux password</span></span>

<span data-ttu-id="d7d8f-119">Para cambiar la contraseña, abre la distribución de Linux (Ubuntu, por ejemplo) y escribe el siguiente comando: `passwd`.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-119">To change your password, open your Linux distribution (Ubuntu for example) and enter the command: `passwd`</span></span>

<span data-ttu-id="d7d8f-120">Tendrás que escribir la contraseña actual, la contraseña nueva y, a continuación, confirmarla.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-120">You will be asked to enter your current password, then asked to enter your new password, and then to confirm your new password.</span></span>

## <a name="forgot-your-password"></a><span data-ttu-id="d7d8f-121">¿Olvidaste la contraseña?</span><span class="sxs-lookup"><span data-stu-id="d7d8f-121">Forgot your password</span></span>

<span data-ttu-id="d7d8f-122">Si olvidaste la contraseña de la distribución de Linux:</span><span class="sxs-lookup"><span data-stu-id="d7d8f-122">If you forgot the password for your Linux distribution:</span></span>

1. <span data-ttu-id="d7d8f-123">Abre PowerShell y escribe la raíz de la distribución de WSL predeterminada mediante el comando: `wsl -u root`.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-123">Open PowerShell and enter the root of your default WSL distribution using the command: `wsl -u root`</span></span>

    > <span data-ttu-id="d7d8f-124">Si necesitas actualizar la contraseña olvidada de una distribución que no es la predeterminada, usa el comando `wsl -d Debian -u root` (recuerda que debes reemplazar `Debian` por el nombre de la distribución de destino).</span><span class="sxs-lookup"><span data-stu-id="d7d8f-124">If you need to update the forgotten password on a distribution that is not your default, use the command: `wsl -d Debian -u root`, replacing `Debian` with the name of your targeted distribution.</span></span>

2. <span data-ttu-id="d7d8f-125">Una vez abierta la distribución de WSL en el nivel raíz en PowerShell, puede usar este comando para actualizar la contraseña: `passwd <WSLUsername>` donde `<WSLUsername>` es el nombre de usuario de la cuenta en la distribución cuya contraseña ha olvidado.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-125">Once your WSL distribution has been opened at the root level inside PowerShell, you can use this command to update your password: `passwd <WSLUsername>` where `<WSLUsername>` is the username of the account in the DISTRO whose password you've forgotten.</span></span>

3. <span data-ttu-id="d7d8f-126">Tendrás que escribir una contraseña UNIX nueva y confirmarla.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-126">You will be prompted to enter a new UNIX password and then confirm that password.</span></span> <span data-ttu-id="d7d8f-127">Cuando veas que la contraseña se ha actualizado correctamente, cierra WSL en PowerShell mediante el comando: `exit`.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-127">Once you're told that the password has updated successfully, close WSL inside of PowerShell using the command: `exit`</span></span>

> [!NOTE]
> <span data-ttu-id="d7d8f-128">Si estás ejecutando una versión anterior del sistema operativo Windows, como 1703 (Creators Update) o 1709 (Fall Creators Update), consulta la [versión archivada de este documento de actualización de cuentas de usuario](./user-support-archived.md).</span><span class="sxs-lookup"><span data-stu-id="d7d8f-128">If you are running an early version of Windows operating system, like 1703 (Creators Update) or 1709 (Fall Creators Update), see the [archived version of this user account update doc](./user-support-archived.md).</span></span>
