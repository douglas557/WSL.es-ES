---
title: Compilación de una distribución de Linux personalizada para WSL
description: Obtenga información sobre cómo crear una distribución de Linux personalizada para el subsistema de Windows para Linux.
keywords: BashOnWindows, bash, WSL, Windows, subsistema de Windows, distribución, personalizado
ms.date: 09/15/2020
ms.topic: article
ms.openlocfilehash: 2882cccac6c34cd52529dbf7e42c8d35907d8241
ms.sourcegitcommit: 69fc9d3ca22cf3f07622db4cdf80c8ec751fe620
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/19/2020
ms.locfileid: "90818707"
---
# <a name="creating-a-custom-linux-distribution-for-wsl"></a>Creación de una distribución de Linux personalizada para WSL

Use nuestro ejemplo de WSL de código abierto para compilar paquetes de WSL distribución para el Microsoft Store y/o para crear paquetes de Linux distribución personalizados para la instalación de prueba. Puede encontrar el [repositorio del iniciador de distribución](https://github.com/Microsoft/WSL-DistroLauncher) en github.

Este proyecto permite:

- Mantenimiento de la distribución de Linux para empaquetar y enviar una distribución de Linux como un appx que se ejecuta en WSL
- Desarrolladores para crear distribuciones de Linux personalizadas que se pueden transferir en su equipo de desarrollo

## <a name="background"></a>Fondo

Distribuimos distribuciones de Linux para WSL como aplicaciones de UWP a través de la Microsoft Store. Puede instalar las aplicaciones que se ejecutarán en WSL: el subsistema que se encuentra en el kernel de Windows. Este mecanismo de entrega tiene muchas ventajas, como se describe en una [entrada de blog anterior](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/).

## <a name="sideloading-a-custom-linux-distro-package"></a>Instalación de prueba de un paquete personalizado de distribución de Linux

Puede crear un paquete de distribución de Linux personalizado como aplicación para transferir localmente en su equipo personal. Tenga en cuenta que el paquete personalizado no se distribuirá a través del Microsoft Store a menos que lo envíe como mantenedor de distribución.
Para configurar la máquina para la instalación de prueba de aplicaciones, tendrá que habilitarla en la configuración del sistema en "para desarrolladores".  Asegúrese de tener el modo de desarrollador o de transferir localmente aplicaciones seleccionadas

## <a name="for-linux-distro-maintainers"></a>Para los mantenedores de distribución de Linux

Para enviarlo a la tienda, tendrá que trabajar con nosotros para recibir la aprobación de la publicación. Si es un propietario de la distribución de Linux interesado en agregar su distribución al Microsoft Store, póngase en contacto con wslpartners@microsoft.com .

## <a name="getting-started"></a>Introducción

Siga las instrucciones del [repositorio de github del iniciador de distribución](https://github.com/Microsoft/WSL-DistroLauncher) para crear un paquete de distribución de Linux personalizado.

## <a name="team-blogs"></a>Blogs del equipo

-  [Abra el aprovisionamiento de un ejemplo de WSL para los mantenedores de distribución de Linux y las distribuciones de Linux personalizadas de instalación de prueba](https://blogs.msdn.microsoft.com/commandline/2018/03/26/wsl-distro-launcher/)
- [Blog de línea de comandos](https://blogs.msdn.microsoft.com/commandline/)

## <a name="provide-feedback"></a>Envío de comentarios

- [Repositorio de GitHub del iniciador de distribución](https://github.com/Microsoft/WSL-DistroLauncher)
- [Seguimiento de problemas de GitHub para WSL](https://github.com/Microsoft/BashOnWindows/issues)
