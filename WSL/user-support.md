---
title: Creación y actualización de cuentas de usuario para distribuciones de WSL
description: Material de referencia para la administración de permisos y cuentas de usuario con el subsistema de Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, subsistemawindows, ubuntu, cuentas de usuario
ms.date: 01/20/2020
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 30dea11adb68639f645ca800a695b0404661845a
ms.sourcegitcommit: e5fb773dd44abab7bcf289340da00f59528b88f7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2020
ms.locfileid: "76973685"
---
# <a name="create-and-update-user-accounts-for-wsl-distributions"></a><span data-ttu-id="fba4b-104">Creación y actualización de cuentas de usuario para distribuciones de WSL</span><span class="sxs-lookup"><span data-stu-id="fba4b-104">Create and update user accounts for WSL distributions</span></span>

<span data-ttu-id="fba4b-105">Una vez hayas habilitado WSL e instalado una distribución de Linux de Microsoft Store, el primer paso que debes completar al abrir la distribución recién instalada de Linux es crear una cuenta que incluya un **nombre de usuario** y una **contraseña**.</span><span class="sxs-lookup"><span data-stu-id="fba4b-105">Once you have enabled WSL and installed a Linux distribution from the Microsoft Store, the first step you will be asked to complete when opening your newly installed Linux distribution is to create an account, including a **User Name** and **Password**.</span></span>

- <span data-ttu-id="fba4b-106">El **nombre de usuario** y la **contraseña** son específicos de la distribución de Linux y no tienen relación con tu nombre de usuario de Windows.</span><span class="sxs-lookup"><span data-stu-id="fba4b-106">This **User Name** and **Password** is specific to your Linux distribution and has no bearing on your Windows user name.</span></span>

- <span data-ttu-id="fba4b-107">Cuando hayas creado el **nombre de usuario** y la **contraseña**, la cuenta será el usuario predeterminado de la distribución e iniciará sesión automáticamente al inicio.</span><span class="sxs-lookup"><span data-stu-id="fba4b-107">Once you create this **User Name** and **Password**, the account will be your default user for the distribution and automatically sign-in on launch.</span></span>

- <span data-ttu-id="fba4b-108">Recuerda que esta cuenta se considerará el administrador de Linux y tendrá la capacidad de ejecutar comandos administrativos `sudo` (es decir, de superusuario).</span><span class="sxs-lookup"><span data-stu-id="fba4b-108">This account will be considered the Linux administrator, with the ability to run `sudo` (Super User Do) administrative commands.</span></span>

- <span data-ttu-id="fba4b-109">Cada distribución de Linux que se ejecuta en el subsistema de Windows para Linux tiene sus propias cuentas de usuario y contraseñas de Linux.</span><span class="sxs-lookup"><span data-stu-id="fba4b-109">Each Linux distribution running on the Windows Subsystem for Linux has its own Linux user accounts and passwords.</span></span>  <span data-ttu-id="fba4b-110">Tendrás que configurar una cuenta de usuario de Linux cada vez que reinstales, restablezcas o agregues una distribución.</span><span class="sxs-lookup"><span data-stu-id="fba4b-110">You will have to configure a Linux user account every time you add a distribution, reinstall, or reset.</span></span>

## <a name="reset-your-linux-password"></a><span data-ttu-id="fba4b-111">Restablecimiento de la contraseña de Linux</span><span class="sxs-lookup"><span data-stu-id="fba4b-111">Reset your Linux password</span></span>

<span data-ttu-id="fba4b-112">Para cambiar la contraseña, abre la distribución de Linux (Ubuntu, por ejemplo) y escribe el siguiente comando: `passwd`.</span><span class="sxs-lookup"><span data-stu-id="fba4b-112">To change your password, open your Linux distribution (Ubuntu for example) and enter the command: `passwd`</span></span>

<span data-ttu-id="fba4b-113">Tendrás que escribir la contraseña actual, la contraseña nueva y, a continuación, confirmarla.</span><span class="sxs-lookup"><span data-stu-id="fba4b-113">You will be asked to enter your current password, then asked to enter your new password, and then to confirm your new password.</span></span>

### <a name="forgot-your-password"></a><span data-ttu-id="fba4b-114">¿Olvidaste la contraseña?</span><span class="sxs-lookup"><span data-stu-id="fba4b-114">Forgot your password</span></span>

<span data-ttu-id="fba4b-115">Si olvidaste la contraseña de la distribución de Linux:</span><span class="sxs-lookup"><span data-stu-id="fba4b-115">If you forgot the password for your Linux distribution:</span></span>

1. <span data-ttu-id="fba4b-116">Abre PowerShell y escribe la raíz de la distribución de WSL predeterminada mediante el comando: `wsl -u root`.</span><span class="sxs-lookup"><span data-stu-id="fba4b-116">Open PowerShell and enter the root of your default WSL distribution using the command: `wsl -u root`</span></span>

> <span data-ttu-id="fba4b-117">Si necesitas actualizar la contraseña olvidada de una distribución que no es la predeterminada, usa el comando `wsl -d Debian -u root` (recuerda que debes reemplazar `Debian` por el nombre de la distribución de destino).</span><span class="sxs-lookup"><span data-stu-id="fba4b-117">If you need to update the forgotten password on a distribution that is not your default, use the command: `wsl -d Debian -u root`, replacing `Debian` with the name of your targeted distribution.</span></span>

2. <span data-ttu-id="fba4b-118">Una vez hayas abierto la distribución de WSL en el nivel raíz en PowerShell, puedes usar este comando para actualizar la contraseña: `passwd`.</span><span class="sxs-lookup"><span data-stu-id="fba4b-118">Once your WSL distribution has been opened at the root level inside PowerShell, you can use this command to update your password: `passwd`</span></span>

3. <span data-ttu-id="fba4b-119">Tendrás que escribir una contraseña UNIX nueva y confirmarla.</span><span class="sxs-lookup"><span data-stu-id="fba4b-119">You will be prompted to enter a new UNIX password and then confirm that password.</span></span> <span data-ttu-id="fba4b-120">Cuando veas que la contraseña se ha actualizado correctamente, cierra WSL en PowerShell mediante el comando: `exit`.</span><span class="sxs-lookup"><span data-stu-id="fba4b-120">Once you're told that the password has updated successfully, close WSL inside of PowerShell using the command: `exit`</span></span>

> [!NOTE]
> <span data-ttu-id="fba4b-121">Si estás ejecutando una versión anterior del sistema operativo Windows, como 1703 (Creators Update) o 1709 (Fall Creators Update), consulta la [versión archivada de este documento de actualización de cuentas de usuario](./user-support-archived.md).</span><span class="sxs-lookup"><span data-stu-id="fba4b-121">If you are running an early version of Windows operating system, like 1703 (Creators Update) or 1709 (Fall Creators Update), see the [archived version of this user account update doc](./user-support-archived.md).</span></span>
