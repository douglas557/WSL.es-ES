---
title: Acerca de WSL 2
description: Acerca de WSL 2, la nueva arquitectura del Subsistema de Windows para Linux
keywords: BashOnWindows, bash, wsl, wsl2, windows, subsistema de windows para linux, subsistemawindows, ubuntu, debian, suse, windows 10, instalación
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 7122fcbd73e064871eba2ac80c727178aaf3ca7b
ms.sourcegitcommit: 5c92b820f84de57a04ab11faf4dd0d24fff6b320
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2019
ms.locfileid: "74161483"
---
# <a name="about-wsl-2"></a>Acerca de WSL 2

WSL 2 es una nueva versión de la arquitectura que permite que el Subsistema de Windows para Linux ejecute archivos binarios de ELF64 Linux en Windows. Sus principales objetivos son aumentar el rendimiento del sistema de archivos y agregar compatibilidad completa con las llamadas del sistema. Esta nueva arquitectura cambia el modo en que estos archivos binarios de Linux interactúan con Windows y con el hardware del equipo, pero proporciona la misma experiencia de usuario que en WSL 1 (la versión disponible de forma general actual). Los distribuciones de Linux individuales se pueden ejecutar como una distribución de WSL 1 o de WSL 2, se pueden actualizar o degradar en cualquier momento, y también se pueden ejecutar distribuciones de WSL 1 y WSL 2 en paralelo. WSL 2 usa una arquitectura completamente nueva que utiliza un kernel de Linux real.

## <a name="linux-kernel-in-wsl-2"></a>Kernel de Linux en WSL 2

El kernel de Linux en WSL 2 se ha creado de forma interna a partir de la rama estable más reciente y se basa en el origen disponible en kernel.org. Este kernel se ha ajustado especialmente para WSL 2. Se ha optimizado en tamaño y rendimiento con el fin de ofrecer una increíble experiencia de Linux en Windows y estará disponible a través de las actualizaciones de Windows, lo que significa que obtendrás las correcciones de seguridad y las mejoras de kernel más recientes sin necesidad de administrarlo tú mismo.

Además, este kernel será de código abierto. Puedes encontrar el código fuente completo del kernel de Linux [aquí](https://github.com/microsoft/WSL2-Linux-Kernel). Si deseas obtener más información sobre este kernel, puedes consultar [esta entrada de blog](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/) escrita por el equipo que lo creó.

## <a name="brief-overview-of-the-wsl-2-architecture"></a>Breve introducción a la arquitectura de WSL 2

WSL 2 usa la tecnología de virtualización mejor y más reciente para ejecutar el kernel de Linux en una máquina virtual (VM) de utilidad ligera. Sin embargo, WSL 2 no será una experiencia de VM tradicional. Una experiencia de VM tradicional puede presentar un arranque lento, aislamiento y un consumo excesivo de recursos, además de exigir tiempo para su administración. WSL 2 no tiene estos atributos. Seguirá aportando las ventajas destacadas de WSL 1: Altos niveles de integración entre Windows y Linux, tiempos de arranque extremadamente rápidos, huella de recursos reducida y, lo mejor de todo, no requerirá la administración ni la configuración de VM. Aunque WSL 2 usa una VM, se administrará y se ejecutará en segundo plano, lo que te permitirá disfrutar de la misma experiencia de usuario que WSL 1.

## <a name="increased-file-io-performance"></a>Mayor rendimiento de E/S de archivos

Las operaciones de uso intensivo de archivos, como `git clone`, `npm install`, `apt update` y `apt upgrade`, serán bastante más rápidas. El aumento de velocidad real dependerá de la aplicación que se esté ejecutando y de cómo interactúes con el sistema de archivos. Las versiones iniciales de WSL 2 se ejecutan hasta 20 veces más rápido en comparación con WSL 1 al desempaquetar un tarball comprimido, y aproximadamente de 2 a 5 veces más rápido cuando se usa `git clone`, `npm install` y `cmake` en distintos proyectos.

## <a name="full-system-call-compatibility"></a>Compatibilidad completa con las llamadas del sistema

Los archivos binarios de Linux usan llamadas del sistema para ejecutar muchas funciones, como el acceso a archivos, la solicitud de memoria, la creación de procesos, etc. Mientras que WSL 1 usaba una capa de traducción creada por el equipo de WSL, WSL 2 incluye su propio kernel de Linux con total compatibilidad con las llamadas del sistema. Presenta un nuevo y completo conjunto de aplicaciones que se pueden ejecutar en WSL, como Docker. Además, las actualizaciones del kernel de Linux pueden estar listas para agregarse inmediatamente al equipo, en lugar de tener que esperar a que el equipo de WSL implemente los cambios y, después, los agregue.