---
title: Acerca de WSL 2
description: Acerca de WSL 2 la nueva arquitectura para el subsistema de Windows para Linux
keywords: BashOnWindows, bash, wsl, wsl2, windows, el subsistema de windows para linux, windowssubsystem, ubuntu, debian, suse, windows 10, instalar
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: b3b0b1ce0f55fed0b4cf223ccc18a509dcf81788
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038135"
---
WSL 2 es una nueva versión de la arquitectura que se utiliza en el subsistema de Windows para Linux ejecutar los archivos binarios de ELF64 Linux en Windows. Son sus objetivos principales aumentar el rendimiento del sistema de archivos, así como la adición de compatibilidad de llamadas completa del sistema. Esta nueva arquitectura cambia cómo interactúan estos archivos binarios de Linux con Windows y el hardware del equipo, pero sigue ofreciendo la misma experiencia de usuario como en WSL 1 (la versión actual de ampliamente disponible). Linux individual distribuciones se pueden ejecutar como una distribución de WSL 1, o como una distribución de WSL 2, puede ser actualizado o degradado en cualquier momento, y puede ejecutar en paralelo de distribuciones WSL 1 y 2 de WSL. WSL 2 utiliza una arquitectura totalmente nueva que usa un kernel de Linux real.

## <a name="linux-kernel-in-wsl-2"></a>Kernel de Linux en WSL 2

El kernel de Linux en WSL 2 se basa en casa de la bifurcación estable más reciente, según el origen está disponible en kernel.org. Este kernel ha sido optimizado especialmente para WSL 2. Se ha optimizado para que el tamaño y rendimiento para proporcionar una experiencia increíble de Linux en Windows y se atenderán a través de actualizaciones de Windows, lo que significa que obtendrá las últimas revisiones de seguridad y mejoras de kernel sin necesidad de administrar usted mismo.

Además, este kernel estará abierto. Puede encontrar el código fuente completo para el kernel de Linux [aquí](https://thirdpartysource.microsoft.com/download/Windows%20Subsystem%20for%20Linux%20v2/May%202019/WSLv2-Linux-Kernel-master.zip). Si desea leer más sobre este kernel pueden desproteger [esta entrada de blog](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/) escrito por el equipo que lo crearon.

## <a name="brief-overview-of-the-wsl-2-architecture"></a>Breve descripción de la arquitectura 2 de WSL

WSL 2 usa los más recientes y mejores avances en tecnología de virtualización para ejecutar el kernel de Linux dentro de una máquina virtual de utilidad ligera (VM). Sin embargo, 2 de WSL no será una experiencia de la máquina virtual tradicionales. Una experiencia de máquina virtual tradicional puede ralentizarse arrancar, está aislada, consume muchos recursos y requiere su tiempo para administrarlo. WSL 2 no tiene estos atributos. Le ofrecen las ventajas más destacable de WSL 1: Altos niveles de integración entre Windows y Linux, tiempos de arranque muy rápidas, superficie de recursos pequeña y lo mejor de todo no requerirá ninguna configuración de máquina virtual o la administración. Aunque WSL 2 usar una máquina virtual, se administra y ejecutar en segundo plano se deja con la misma experiencia de usuario como WSL 1.

## <a name="increased-file-io-performance"></a>Archivo de mayor rendimiento de E/S

Operaciones intensivas de archivo, como clonación de git, npm install, apt actualización, actualización apt y más todo será notablemente más rápido. El aumento de la velocidad real dependerá de qué aplicación está ejecutando y cómo interactúa con el sistema de archivos. Las versiones iniciales de WSL 2 ejecutan hasta 20 veces más rápido en comparación con 1 WSL desempaquetar un paquete tarball comprimido y alrededor de 2 a 5 veces más rápido cuando se usa la clonación de git, npm install y cmake en varios proyectos.

## <a name="full-system-call-compatibility"></a>Compatibilidad de llamadas completa del sistema

Los archivos binarios de Linux utilizar llamadas del sistema para realizar muchas funciones, como obtener acceso a archivos, que soliciten memoria, creación de procesos y mucho más. Mientras que 1 WSL usa una capa de traducción que se compiló el equipo de WSL, WSL 2 incluye su propio kernel de Linux con compatibilidad de llamadas completa del sistema. Esto presenta un nuevo conjunto completo de aplicaciones que se pueden ejecutar dentro de WSL, como Docker y mucho más. Además, las actualizaciones del kernel de Linux pueden ser inmediatamente listos para agregarse a su equipo, en lugar de esperar el equipo de WSL para implementar los cambios y, a continuación, tener les agregan.