---
title: Inicialización de una nueva distribución de Linux en WSL
description: Después de instalar una distribución de Linux para WSL, sigue estos sencillos pasos para completar la inicialización.
keywords: BashOnWindows, bash, wsl, wsl2, windows, subsistema de windows para linux, windowssubsystem, ubuntu, debian, suse, windows 10
ms.date: 07/24/2018
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 11dc84d3a58b51241c7c63e8ca35eba94a12508b
ms.sourcegitcommit: b15b847b87d29a40de4a1517315949bce9c7a3d5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "91413216"
---
# <a name="initializing-a-newly-installed-distribution"></a>Inicialización de una distribución recién instalada

Una vez que se haya descargado e instalado la distribución, deberás completar su inicialización:

## <a name="launch-a-distribution"></a>Inicio de una distribución

Para completar la inicialización de la distribución recién instalada, inicia una nueva instancia. Para ello, haz clic en el botón "Iniciar" en la aplicación Microsoft Store, o inicia la distribución desde el menú Inicio:

> Sugerencia: Puedes anclar las distribuciones que se usan con más frecuencia en el menú Inicio o en la barra de tareas.

![Inicio de las distribuciones desde el menú Inicio](media/start-menu.png)

> En Windows Server, puedes iniciar el archivo ejecutable `<distribution>.exe` del iniciador de la distribución desde la carpeta de instalación de las distribuciones.

La primera vez que se ejecute una distribución recién instalada, se abrirá una ventana de consola y se te pedirá que esperes un minuto o dos para que se complete la instalación.

> Durante esta fase final de la instalación, los archivos de la distribución se descomprimen y almacenan en el equipo, listos para usarse. Esta acción puede tardar aproximadamente un minuto o más en función del rendimiento de los dispositivos de almacenamiento del equipo. Esta fase de instalación inicial solo es necesaria cuando una distribución se instala por primera vez; todos los inicios futuros deben tardar menos de un segundo.

## <a name="setting-up-a-new-linux-user-account"></a>Configuración de una nueva cuenta de usuario de Linux

Una vez completada la instalación, se te pedirá que crees una nueva cuenta de usuario (y su contraseña).

![Desempaquetado de Ubuntu en la consola de Windows](media/UbuntuInstall.png)

Esta cuenta de usuario es para el usuario normal sin privilegios de administrador con el que se iniciará sesión de manera predeterminada al iniciar una distribución.

> Puedes elegir cualquier nombre de usuario y contraseña: no tienen ninguna relación con el nombre de usuario de Windows.

Cuando abras una nueva instancia de la distribución, no se te pedirá la contraseña. No obstante, **si elevas un proceso mediante `sudo`, tendrás que escribir la contraseña**, por lo que debes asegurarte de elegir una contraseña que puedas recordar fácilmente. Para obtener más información, consulta la página de [Soporte del usuario](user-support.md).

## <a name="update--upgrade-your-distributions-packages"></a>Actualización de los paquetes de la distribución

La mayoría de las distribuciones incluyen un catálogo de paquetes vacío o mínimo. Se recomienda actualizar periódicamente el catálogo de paquetes, así como actualizar los paquetes instalados con el administrador de paquetes preferido de la distribución. En Debian y Ubuntu, se usa apt:

```bash
sudo apt update && sudo apt upgrade
```

> Windows no actualiza automáticamente las distribuciones de Linux: Se trata de una tarea que los usuarios de Linux prefieren controlar.

Has terminado. Disfruta con la nueva distribución de Linux en WSL. Para obtener más información sobre WSL, revisa los otros [documentos de WSL](./index.md) o la [página de recursos de aprendizaje de WSL](https://aka.ms/learnwsl).

![Disfruta del uso de Linux en WSL.](media/linux-on-wsl.png)

## <a name="troubleshooting"></a>Solucionar problemas

A continuación, se muestran errores relacionados y las correcciones sugeridas. Consulta la [página de solución de problemas de WSL](troubleshooting.md) para ver otros errores generales y sus soluciones.

> **Error 0x8007007e en la instalación**: este error se produce cuando el sistema no es compatible con Linux desde Store.  Asegúrese de que:
> * Estás ejecutando la compilación 16215 de Windows o una posterior. [Comprueba el número de compilación](troubleshooting.md#check-your-build-number).
> * El componente opcional del subsistema de Windows para Linux está habilitado y se ha reiniciado el equipo.  [Asegúrate de que WSL está habilitado](troubleshooting.md#confirm-wsl-is-enabled).