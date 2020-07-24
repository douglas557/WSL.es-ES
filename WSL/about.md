---
title: Sobre el Subsistema de Windows para Linux
description: Obtén información sobre el Subsistema de Windows para Linux, las diferentes versiones y las formas en que puedes usarlas.
keywords: BashOnWindows, bash, wsl, windows, subsistemawindows, gnu, linux
ms.date: 05/12/2020
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ROBOTS: NOINDEX
ms.openlocfilehash: ddc242360adf67e3c5b6cd14d35fb6c869b83b2d
ms.sourcegitcommit: 97cc93f8e26391c09a31a4ab42c4b5e9d98d1c32
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/22/2020
ms.locfileid: "86948629"
---
# <a name="what-is-the-windows-subsystem-for-linux"></a>¿Qué es el Subsistema de Windows para Linux?

El Subsistema de Windows para Linux permite a los desarrolladores ejecutar un entorno de GNU/Linux, incluida la mayoría de herramientas de línea de comandos, utilidades y aplicaciones, directamente en Windows, sin modificar y sin la sobrecarga de una máquina virtual tradicional o una configuración de arranque dual.

Se puede hacer lo siguiente:

* Elige tus distribuciones de GNU/Linux favoritas [de Microsoft Store](https://aka.ms/wslstore).
* Ejecuta herramientas comunes de línea de comandos, como `grep`, `sed`, `awk` u otros archivos binarios ELF-64.
* Ejecuta scripts de shell de Bash y aplicaciones de línea de comandos de GNU/Linux, como:  
    * Herramientas: vim, emacs, tmux.
    * Idiomas: [NodeJS](https://docs.microsoft.com/windows/nodejs/setup-on-wsl2), Javascript, [Python](https://docs.microsoft.com/windows/python/web-frameworks), Ruby, C/C++, C# & F#, Rust, Go, etc.
    * Servicios: SSHD, MySQL, Apache, lighttpd, [MongoDB](https://docs.microsoft.com/windows/nodejs/databases) y [PostgreSQL](https://docs.microsoft.com/windows/python/databases).
* Instala software adicional mediante el administrador de paquetes de distribución de GNU/Linux.
* Invoca aplicaciones de Windows mediante un shell de línea de comandos de tipo UNIX.
* Invoca aplicaciones de GNU/Linux en Windows.

## <a name="what-is-wsl-2"></a>¿Qué es WSL 2?

WSL 2 es una nueva versión de la arquitectura del Subsistema de Windows para Linux que permite que el Subsistema de Windows para Linux ejecute archivos binarios de ELF64 de Linux en Windows. Sus principales objetivos son **aumentar el rendimiento del sistema de archivos** y agregar **compatibilidad completa con las llamadas del sistema**.

Esta nueva arquitectura cambia el modo en que estos archivos binarios de Linux interactúan con Windows y con el hardware del equipo, pero proporciona la misma experiencia de usuario que en WSL 1 (la versión disponible de forma general actualmente).

Las distribuciones de Linux individuales se pueden ejecutar con la arquitectura de WSL 1 o WSL 2. Cada distribución se puede actualizar o degradar en cualquier momento, y puedes ejecutar distribuciones de WSL 1 y WSL 2 en paralelo. WSL 2 usa una arquitectura completamente nueva que aprovecha las ventajas de un kernel de Linux real.

## <a name="next-steps"></a>Pasos siguientes

* [Instalación de WSL 1 y actualización a WSL 2](./install-win10.md)

* [Comparación de WSL 2 con WSL 1](./compare-versions.md)

* [Creación de una cuenta de usuario y una contraseña para la nueva distribución de Linux](./user-support.md)

* [Lectura de las preguntas más frecuentes](./faq.md)

* [Lectura de las preguntas más frecuentes sobre WSL 2](./wsl2-faq.md)

* [Solución de problemas](./troubleshooting.md)

* [Ejecución de comandos de interoperabilidad entre Windows y Linux](./interop.md)

* [Ejecución de configuraciones y comandos de inicio](./wsl-config.md)

* [Configuración de permisos de archivo](./file-permissions.md)

* [Configuración de WSL para empresas](./enterprise.md)

* [Comandos de WSL de referencia](./reference.md)

* [Compilación de distribuciones personalizadas](./build-custom-distro.md)

* [Lectura de las notas de la versión de WSL](./release-notes.md)
