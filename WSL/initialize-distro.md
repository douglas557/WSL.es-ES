---
title: Inicializar una nueva distribución de Linux de WSL
description: Después de instalar una distribución de Linux para WSL, completar la inicialización siguiendo estos sencillos pasos
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, windowssubsystem, ubuntu, debian, suse, windows 10
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 7f1ce521b248c873fa7f81c6363eb506c0363fed
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2019
ms.locfileid: "59902052"
---
# <a name="initializing-a-newly-installed-distro"></a>Inicializar una distribución recién instalada
Una vez que se ha descargado e instalado la distribución, deberá completar la inicialización de la distribución de nuevo:

## <a name="launch-a-distro"></a>Iniciar una distribución
Para completar la inicialización de la distribución recién instalada, inicie una nueva instancia. Puede hacerlo haciendo clic con el botón "iniciar" en la aplicación de Windows Store o iniciando la distribución en el menú Inicio:

> Sugerencia: Es posible que desea anclar sus distribuciones utilizadas con frecuencia al menú Inicio o en la barra de tareas.

![Iniciar distribuciones desde el menú Inicio](media/start-menu.png)

> En Windows Server, puede iniciar el selector de la distribución ejecutable `<distro>.exe` desde la carpeta de instalación de distribución.

La primera vez que ejecuta una distribución recién instalada, una consola se abrirá la ventana, y le pedirá que espere un minuto o dos para que se complete la instalación.

> Durante esta fase final de la instalación, los archivos de la distribución están anular comprimidos y almacenados en su PC, listo para su uso. Esta operación puede tardar alrededor de un minuto o más dependiendo del rendimiento de los dispositivos de almacenamiento de su PC. Esta fase inicial de la instalación sólo es necesario cuando una distribución es la instalación completa de todas las versiones futuras tardará menos de un segundo.

## <a name="setting-up-a-new-linux-user-account"></a>Configurar una nueva cuenta de usuario de Linux

Una vez completada la instalación, se le pedirá que cree una nueva cuenta de usuario (y su contraseña). 

![Ubuntu desempaquetar en la consola de Windows](media/UbuntuInstall.png)

Esta cuenta de usuario es para el usuario no administrador normal que se convertirá ha iniciado sesión como de forma predeterminada al iniciar una distribución.

> Puede elegir cualquier nombre de usuario y contraseña que desee: no tiene ningún efecto en su nombre de usuario de Windows. 

Cuando se abre una nueva instancia de la distribución, no se le pedirán la contraseña, pero **si elevar un proceso usando `sudo`, tendrá que escribir la contraseña**, por lo que asegúrese de que elige una contraseña que pueda recordar fácilmente! Consulte la [soporte técnico de usuario](user-support.md) página para obtener más información.

## <a name="update--upgrade-your-distros-packages"></a>Actualizar & actualizar los paquetes de la distribución

La mayoría de las distribuciones se distribuyen con un catálogo de paquete mínimo/vacío. Se recomienda encarecidamente actualizar con regularidad el catálogo de paquetes y actualizar los paquetes instalados con el Administrador de paquetes preferido de su distribución. En Debian y Ubuntu, usa apt:

```bash
sudo apt update && sudo apt upgrade
```

> Windows no actualizar automáticamente ni actualizar su distro(s) Linux: Esta es una tarea que prefieren los usuarios de Linux para controlar a sí mismos.

¡Has terminado! Disfrute de uso de la nueva distribución de Linux en WSL. Para obtener más información acerca de WSL, revise el otro [docs WSL](https://aka.ms/wsldocs), o el [WSL página de recursos de aprendizaje](https://aka.ms/learnwsl).

![Disfrute con Linux en WSL](media/linux-on-wsl.png)

## <a name="troubleshooting"></a>Solución de problemas

A continuación se muestran errores relacionados y correcciones sugeridas. Hacer referencia a la [página de solución de problemas de WSL](troubleshooting.md) para otros errores comunes y sus soluciones.

> **Error de instalación 0x8007007e** este error se produce cuando el sistema no es compatible con Linux desde el almacén.  Asegúrese de que:
> * Ya está ejecutando Windows compilación 16215 o posterior. [Comprobar la compilación](troubleshooting.md#check-your-build-number).
> * El subsistema de Windows para el componente opcional de Linux está habilitado y ha reiniciado el equipo.  [Asegúrese de que está habilitado WSL](troubleshooting.md#confirm-wsl-is-enabled).
