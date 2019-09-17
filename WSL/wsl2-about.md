---
title: Acerca de WSL 2
description: Acerca de WSL 2 la nueva arquitectura para el subsistema de Windows para Linux
keywords: BashOnWindows, bash, wsl, wsl2, windows, subsistema de windows para linux, subsistemawindows, ubuntu, debian, suse, windows 10, instalación
author: craigloewen-msft
ms.author: crloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 983699c26a21af7b81ba31067316ba3bbf1601af
ms.sourcegitcommit: ed5cf72d5ceb92edd50cf9260ac31fd4d95a02c8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "71020932"
---
# <a name="about-wsl-2"></a>Acerca de WSL 2

WSL 2 es una nueva versión de la arquitectura que permite que el subsistema de Windows para Linux ejecute archivos binarios de ELF64 Linux en Windows. Sus principales objetivos son aumentar el rendimiento del sistema de archivos, así como agregar compatibilidad completa con llamadas del sistema. Esta nueva arquitectura cambia el modo en que estos archivos binarios de Linux interactúan con Windows y el hardware del equipo, pero proporciona la misma experiencia de usuario que en WSL 1 (la versión de disponibilidad generalizada actual). Los distribuciones de Linux individuales se pueden ejecutar como WSL 1 distribución, o como WSL 2 distribución, se pueden actualizar o degradar en cualquier momento, y puede ejecutar WSL 1 y WSL 2 distribuciones en paralelo. WSL 2 usa una arquitectura completamente nueva que usa un kernel de Linux real.

## <a name="linux-kernel-in-wsl-2"></a>Kernel de Linux en WSL 2

El kernel de Linux en WSL 2 se ha creado a partir de la rama estable más reciente, en función del origen disponible en kernel.org. Este kernel se ajustó especialmente para WSL 2. Se ha optimizado para el tamaño y el rendimiento con el fin de ofrecer una increíble experiencia de Linux en Windows y se prestará servicio a través de actualizaciones de Windows, lo que significa que obtendrá las correcciones de seguridad y las mejoras de kernel más recientes sin necesidad de administrarla usted mismo.

Además, este kernel será de código abierto. [Aquí](https://github.com/microsoft/WSL2-Linux-Kernel)puede encontrar el código fuente completo del kernel de Linux. Si desea obtener más información sobre este kernel, puede consultar [esta entrada de blog](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/) escrita por el equipo que la creó.

## <a name="brief-overview-of-the-wsl-2-architecture"></a>Breve introducción a la arquitectura de WSL 2

WSL 2 usa la tecnología de virtualización más reciente y más actualizada para ejecutar el kernel de Linux en una máquina virtual de utilidad ligera (VM). Sin embargo, WSL 2 no será una experiencia de máquina virtual tradicional. Una experiencia de máquina virtual tradicional puede ser lenta de arrancar, estar aislada, consume muchos recursos y requiere su tiempo para administrarla. WSL 2 no tiene estos atributos. Seguirá aportando las ventajas más destacadas de WSL 1: Los altos niveles de integración entre Windows y Linux, los tiempos de arranque extremadamente rápidos, la superficie de recursos pequeña y el mejor de todos no requerirán la administración ni la configuración de la máquina virtual. Aunque WSL 2 usa una máquina virtual, se administrará y se ejecutará en segundo plano, lo que le permitirá disfrutar de la misma experiencia de usuario que WSL 1.

## <a name="increased-file-io-performance"></a>Mayor rendimiento de e/s de archivos

Las operaciones con un uso intensivo de archivos como git clone, NPM install, apt Update, apt upgrade y more serán cada vez más rápidas. El aumento de velocidad real dependerá de la aplicación que se esté ejecutando y de cómo interactúe con el sistema de archivos. Las versiones iniciales de WSL 2 se ejecutan hasta 20x más rápido en comparación con WSL 1 al desempaquetar un tarball comprimido y aproximadamente de 2 a 5 veces más rápido al usar git clone, NPM install y CMake en varios proyectos.

## <a name="full-system-call-compatibility"></a>Compatibilidad completa con llamadas del sistema

Los archivos binarios de Linux usan llamadas del sistema para realizar muchas funciones como el acceso a archivos, la solicitud de memoria, la creación de procesos, etc. Mientras que WSL 1 usaba una capa de traducción creada por el equipo de WSL, WSL 2 incluye su propio kernel de Linux con plena compatibilidad con las llamadas del sistema. Esto incluye un nuevo conjunto completo de aplicaciones que se pueden ejecutar dentro de WSL, como Docker y mucho más. Además, las actualizaciones del kernel de Linux pueden estar listas para agregarse inmediatamente al equipo, en lugar de esperar a que el equipo de WSL implemente los cambios y, después, los agregue.