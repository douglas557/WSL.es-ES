---
title: Inicialización de un nuevo distribución de WSL Linux
description: Después de instalar una distribución de Linux para WSL, complete la inicialización siguiendo estos sencillos pasos.
keywords: BashOnWindows, bash, WSL, Windows, subsistema de Windows para Linux, windowssubsystem, Ubuntu, Debian, SuSE, Windows 10
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 30cb1de0a01fd46bc434061cd36794f4ece77e4b
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499298"
---
# <a name="initializing-a-newly-installed-distro"></a>Inicialización de un distribución recién instalado
Una vez que se haya descargado e instalado el distribución, deberá completar la inicialización del nuevo distribución:

## <a name="launch-a-distro"></a>Inicio de un distribución
Para completar la inicialización del distribución recién instalado, inicie una nueva instancia de. Para ello, haga clic en el botón "iniciar" en la aplicación Microsoft Store o inicie el distribución desde el menú Inicio:

> Sugerencia: Es posible que quiera anclar el distribuciones que se usa con más frecuencia en el menú Inicio o en la barra de tareas.

![Iniciar distribuciones desde el menú Inicio](media/start-menu.png)

> En Windows Server, puede iniciar el archivo ejecutable `<distro>.exe` del iniciador de distribución desde la carpeta de instalación de distribución.

La primera vez que se ejecuta un distribución recién instalado, se abrirá una ventana de consola y se le pedirá que espere un minuto o dos para que se complete la instalación.

> Durante esta fase final de la instalación, los archivos del distribución se descomprimen y almacenan en el equipo, listos para usarse. Esto puede tardar aproximadamente un minuto o más en función del rendimiento de los dispositivos de almacenamiento de su equipo. Esta fase de instalación inicial solo es necesaria cuando un distribución está instalado sin problemas; todos los lanzamientos futuros deben tardar menos de un segundo.

## <a name="setting-up-a-new-linux-user-account"></a>Configuración de una nueva cuenta de usuario de Linux

Una vez completada la instalación, se le pedirá que cree una nueva cuenta de usuario (y su contraseña). 

![Desempaquetar Ubuntu en la consola de Windows](media/UbuntuInstall.png)

Esta cuenta de usuario es para el usuario normal sin privilegios de administrador en el que se iniciará sesión como de forma predeterminada al iniciar un distribución.

> Puede elegir cualquier nombre de usuario y contraseña que desee: no tienen ninguna relación con el nombre de usuario de Windows. 

Cuando abra una nueva instancia de distribución, no se le pedirá la contraseña, pero **si eleva un proceso mediante `sudo`, tendrá que escribir la contraseña**, por lo que debe asegurarse de elegir una contraseña que pueda recordar fácilmente. Para obtener más información, consulte la página de [soporte técnico del usuario](user-support.md) .

## <a name="update--upgrade-your-distros-packages"></a>Actualizar & actualizar los paquetes de distribución

La mayoría de distribuciones se distribuye con un catálogo de paquetes vacío o mínimo. Se recomienda encarecidamente actualizar el catálogo de paquetes y actualizar los paquetes instalados con el administrador de paquetes preferido de su distribución. En Debian/Ubuntu, se usa apt:

```bash
sudo apt update && sudo apt upgrade
```

> Windows no actualiza ni actualiza automáticamente los distribución de Linux: Se trata de una tarea que los usuarios de Linux prefieren controlar.

¡Has terminado! Disfrute con el nuevo distribución de Linux en WSL. Para obtener más información sobre WSL, revise los otros [documentos de WSL](https://aka.ms/wsldocs)o la página de recursos de aprendizaje de [WSL](https://aka.ms/learnwsl).

![Disfrute del uso de Linux en WSL](media/linux-on-wsl.png)

## <a name="troubleshooting"></a>Solución de problemas

A continuación se muestran los errores relacionados y las correcciones sugeridas. Consulte la [Página de solución de problemas de WSL](troubleshooting.md) para ver otros errores comunes y sus soluciones.

> Error **0x8007007e en la instalación** Este error se produce cuando el sistema no es compatible con Linux desde la tienda.  Asegúrese de que:
> * Está ejecutando Windows Build 16215 o posterior. [Compruebe la compilación](troubleshooting.md#check-your-build-number).
> * El componente opcional de subsistema de Windows para Linux está habilitado y el equipo se ha reiniciado.  [Asegúrese de que WSL está habilitado](troubleshooting.md#confirm-wsl-is-enabled).
