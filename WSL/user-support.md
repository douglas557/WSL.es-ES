---
title: Creación y actualización de cuentas de usuario para distribuciones de WSL
description: Material de referencia para la administración de permisos y cuentas de usuario con el subsistema de Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, subsistemawindows, ubuntu, cuentas de usuario
ms.date: 01/20/2020
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 85bd8f05d041181c2cfb16f6fb55aaeea15b332c
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520584"
---
# <a name="create-and-update-user-accounts-for-wsl-distributions"></a>Creación y actualización de cuentas de usuario para distribuciones de WSL

Una vez hayas habilitado WSL e instalado una distribución de Linux de Microsoft Store, el primer paso que debes completar al abrir la distribución recién instalada de Linux es crear una cuenta que incluya un **nombre de usuario** y una **contraseña**.

- El **nombre de usuario** y la **contraseña** son específicos de la distribución de Linux y no tienen relación con tu nombre de usuario de Windows.

- Cuando hayas creado el **nombre de usuario** y la **contraseña**, la cuenta será el usuario predeterminado de la distribución e iniciará sesión automáticamente al inicio.

- Recuerda que esta cuenta se considerará el administrador de Linux y tendrá la capacidad de ejecutar comandos administrativos `sudo` (es decir, de superusuario).

- Cada distribución de Linux que se ejecuta en el subsistema de Windows para Linux tiene sus propias cuentas de usuario y contraseñas de Linux.  Tendrás que configurar una cuenta de usuario de Linux cada vez que reinstales, restablezcas o agregues una distribución.

## <a name="reset-your-linux-password"></a>Restablecimiento de la contraseña de Linux

Para cambiar la contraseña, abre la distribución de Linux (Ubuntu, por ejemplo) y escribe el siguiente comando: `passwd`.

Tendrás que escribir la contraseña actual, la contraseña nueva y, a continuación, confirmarla.

### <a name="forgot-your-password"></a>¿Olvidaste la contraseña?

Si olvidaste la contraseña de la distribución de Linux:

1. Abre PowerShell y escribe la raíz de la distribución de WSL predeterminada mediante el comando: `wsl -u root`.

\- Si necesitas actualizar la contraseña olvidada de una distribución que no es la predeterminada, usa el comando: `wsl -d Debian -u root` (recuerda que debes reemplazar `Debian` con el nombre de la distribución de destino).

2. Una vez hayas abierto la distribución de WSL en el nivel raíz en PowerShell, puedes usar este comando para actualizar la contraseña: `passwd`.

3. Tendrás que escribir una contraseña UNIX nueva y confirmarla. Cuando veas que la contraseña se ha actualizado correctamente, cierra WSL en PowerShell mediante el comando: `exit`.

> [!NOTE]
> Si estás ejecutando una versión anterior del sistema operativo Windows, como 1703 (Creators Update) o 1709 (Fall Creators Update), consulta la [versión archivada de este documento de actualización de cuentas de usuario](./user-support-archived.md).
