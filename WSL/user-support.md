---
title: Creación y actualización de cuentas de usuario para distribuciones de Linux
description: Material de referencia para la administración de permisos y cuentas de usuario con el subsistema de Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, subsistemawindows, ubuntu, cuentas de usuario
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 551cc66b1648a66717163d1d8e19a78d28bff342
ms.sourcegitcommit: 3fb40fd65b34a5eb26b213a0df6a3b2746b7a9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2020
ms.locfileid: "83235909"
---
# <a name="create-a-user-account-and-password-for-your-new-linux-distribution"></a>Creación de una cuenta de usuario y una contraseña para la nueva distribución de Linux

Una vez hayas [habilitado WSL e instalado una distribución de Linux de Microsoft Store](./install-win10.md), el primer paso que debes completar al abrir la distribución recién instalada de Linux es crear una cuenta, incluido un **nombre de usuario** y una **contraseña**.

- El **nombre de usuario** y la **contraseña** son específicos de la distribución de Linux y no tienen relación con tu nombre de usuario de Windows.

- Cuando hayas creado el **nombre de usuario** y la **contraseña**, la cuenta será el usuario predeterminado de la distribución e iniciará sesión automáticamente al inicio.

- Recuerda que esta cuenta se considerará el administrador de Linux y tendrá la capacidad de ejecutar comandos administrativos `sudo` (es decir, de superusuario).

- Cada distribución de Linux que se ejecuta en el subsistema de Windows para Linux tiene sus propias cuentas de usuario y contraseñas de Linux.  Tendrás que configurar una cuenta de usuario de Linux cada vez que reinstales, restablezcas o agregues una distribución.

![Desempaquetado de Ubuntu en la consola de Windows](media/UbuntuInstall.png)

## <a name="update-and-upgrade-packages"></a>Actualización de paquetes

La mayoría de las distribuciones incluyen un catálogo de paquetes vacío o mínimo. Te recomendamos encarecidamente que actualices periódicamente el catálogo de paquetes, así como los paquetes instalados mediante el administrador de paquetes preferido de la distribución. Para Debian y Ubuntu, usa apt:

```bash
sudo apt update && sudo apt upgrade
```

Windows no actualiza automáticamente las distribuciones de Linux. Se trata de una tarea que la mayoría de los usuarios de Linux prefieren controlar por sí mismos.

## <a name="reset-your-linux-password"></a>Restablecimiento de la contraseña de Linux

Para cambiar la contraseña, abre la distribución de Linux (Ubuntu, por ejemplo) y escribe el siguiente comando: `passwd`.

Tendrás que escribir la contraseña actual, la contraseña nueva y, a continuación, confirmarla.

## <a name="forgot-your-password"></a>¿Olvidaste la contraseña?

Si olvidaste la contraseña de la distribución de Linux:

1. Abre PowerShell y escribe la raíz de la distribución de WSL predeterminada mediante el comando: `wsl -u root`.

    > Si necesitas actualizar la contraseña olvidada de una distribución que no es la predeterminada, usa el comando `wsl -d Debian -u root` (recuerda que debes reemplazar `Debian` por el nombre de la distribución de destino).

2. Una vez hayas abierto la distribución de WSL en el nivel raíz en PowerShell, puedes usar este comando para actualizar la contraseña: `passwd`.

3. Tendrás que escribir una contraseña UNIX nueva y confirmarla. Cuando veas que la contraseña se ha actualizado correctamente, cierra WSL en PowerShell mediante el comando: `exit`.

> [!NOTE]
> Si estás ejecutando una versión anterior del sistema operativo Windows, como 1703 (Creators Update) o 1709 (Fall Creators Update), consulta la [versión archivada de este documento de actualización de cuentas de usuario](./user-support-archived.md).
