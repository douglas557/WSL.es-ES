---
title: Subsistema de Windows para la referencia de comandos de Linux
description: Lista de comandos que administran el subsistema Windows para Linux
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, windowssubsystem, ubuntu
author: scooley
ms.author: scooley
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.openlocfilehash: 978a35d593e37877949c24cbd833a519888d54bf
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063583"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="7c801-104">Referencia de comandos para el subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="7c801-104">Command Reference for Windows Subsystem for Linux</span></span>

> `lxrun.exe` <span data-ttu-id="7c801-105">está en desuso a partir de Windows 10 1803 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="7c801-105">is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="7c801-106">El comando `lxrun.exe` se puede usar para interactuar con el [subsistema Windows para Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directamente.</span><span class="sxs-lookup"><span data-stu-id="7c801-106">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="7c801-107">Estos comandos se instalan en el `\Windows\System32` directorio y se pueden ejecutar en un símbolo del sistema de Windows o en PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7c801-107">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

* `lxrun.exe` <span data-ttu-id="7c801-108">se usa para administrar WSL.</span><span class="sxs-lookup"><span data-stu-id="7c801-108">is used to manage WSL.</span></span>  <span data-ttu-id="7c801-109">Este comando se puede usar para instalar o desinstalar la imagen de Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="7c801-109">This command can be used to install or uninstall the Ubuntu image.</span></span>


| <span data-ttu-id="7c801-110">Comando</span><span class="sxs-lookup"><span data-stu-id="7c801-110">Command</span></span>                     | <span data-ttu-id="7c801-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c801-111">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `bash`                      | <span data-ttu-id="7c801-112">Inicia el shell de Bash en el directorio actual.</span><span class="sxs-lookup"><span data-stu-id="7c801-112">Launches the Bash shell in the current directory.</span></span>  <span data-ttu-id="7c801-113">Si no se instala automáticamente el shell de Bash se ejecuta</span><span class="sxs-lookup"><span data-stu-id="7c801-113">If the Bash shell is not installed automatically runs</span></span> `lxrun /install` |
| `bash ~`                    | <span data-ttu-id="7c801-114">Inicia el shell de bash al directorio particular de Ubuntu del usuario.</span><span class="sxs-lookup"><span data-stu-id="7c801-114">Launches the bash shell into the user's Ubuntu home directory.</span></span>  <span data-ttu-id="7c801-115">Similar a la ejecución de cd ~</span><span class="sxs-lookup"><span data-stu-id="7c801-115">Similar to running cd ~</span></span>            |
| `bash -c "<command>"`       | <span data-ttu-id="7c801-116">Ejecuta el comando, imprime la salida y se cierra la vuelta a la línea de comandos de Windows.</span><span class="sxs-lookup"><span data-stu-id="7c801-116">Runs the command, prints the output and exits back to the Windows command prompt.</span></span> <br/> <br/> <span data-ttu-id="7c801-117">Ejemplo: **bash -c "ls"**</span><span class="sxs-lookup"><span data-stu-id="7c801-117">Example:  **bash -c "ls"**</span></span> |

<p>

| <span data-ttu-id="7c801-118">Comando</span><span class="sxs-lookup"><span data-stu-id="7c801-118">Command</span></span>                     | <span data-ttu-id="7c801-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c801-119">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="7c801-120">El comando lxrun se usa para administrar la instancia WSL.</span><span class="sxs-lookup"><span data-stu-id="7c801-120">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="7c801-121">Inicia la descarga y el proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="7c801-121">Starts the download and install process.</span></span> <br/> <span data-ttu-id="7c801-122">**/y** pueden agregarse a omitir todas las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="7c801-122">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="7c801-123">El mensaje de confirmación se acepta automáticamente y el usuario predeterminado se establece en la raíz.</span><span class="sxs-lookup"><span data-stu-id="7c801-123">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="7c801-124">Desinstala y elimina la imagen de Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="7c801-124">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="7c801-125">De forma predeterminada no elimina el directorio del usuario Ubuntu principal.</span><span class="sxs-lookup"><span data-stu-id="7c801-125">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="7c801-126">**/y** pueden agregarse a Aceptar automáticamente el mensaje de confirmación</span><span class="sxs-lookup"><span data-stu-id="7c801-126">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="7c801-127">**completo** desinstala y elimina el directorio particular de Ubuntu del usuario</span><span class="sxs-lookup"><span data-stu-id="7c801-127">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="7c801-128">Establece el valor predeterminado de Bash en Ubuntu usuario.</span><span class="sxs-lookup"><span data-stu-id="7c801-128">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="7c801-129">Se le pedirá una contraseña si el usuario especificado no existe.</span><span class="sxs-lookup"><span data-stu-id="7c801-129">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="7c801-130">Para obtener más información, visite: https://aka.ms/wslusers.</span><span class="sxs-lookup"><span data-stu-id="7c801-130">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="7c801-131">**/y** promping omisiones para la contraseña.</span><span class="sxs-lookup"><span data-stu-id="7c801-131">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="7c801-132">El usuario se creará sin una contraseña.</span><span class="sxs-lookup"><span data-stu-id="7c801-132">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="7c801-133">Actualiza el índice de paquetes del subsistema</span><span class="sxs-lookup"><span data-stu-id="7c801-133">Updates the subsystem's package index</span></span>          |
