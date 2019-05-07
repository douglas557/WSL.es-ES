---
title: Crear una distribución de Linux personalizada para WSL
description: Obtenga información sobre cómo crear una distribución de Linux personalizada para el subsistema de Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, el subsistema de windows, distribución, personalizado
author: taraj
ms.author: taraj
ms.date: 03/27/2018
ms.topic: article
ms.assetid: a5095219-0c82-4ce5-9a6d-5c2fc00835a3
ms.custom: seodec18
ms.openlocfilehash: b98101c19d7d450548531521c3f8ee15ce62f9f1
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063263"
---
# <a name="creating-a-custom-linux-distro-for-wsl"></a>Creación de una distribución de Linux personalizada para WSL

Utilice nuestro ejemplo WSL de código abierto para crear paquetes de distribución WSL para la Microsoft Store o crear paquetes personalizados de distribución de Linux para la instalación de prueba. Puede encontrar el [repositorio de distribución del iniciador](https://github.com/Microsoft/WSL-DistroLauncher) en GitHub.

Este proyecto permite:
* Mantenedores de distribución de Linux para empaquetar y enviar una distribución de Linux como un appx que se ejecuta en WSL
* A los desarrolladores crear distribuciones de Linux personalizadas que pueden transferir localmente en su equipo de desarrollo

## <a name="background"></a>Background
Distribuimos distribuciones de Linux para WSL como aplicaciones para UWP a través de la Microsoft Store. Puede instalar las aplicaciones que se ejecutarán en WSL - el subsistema que se encuentra en el kernel de Windows. Este mecanismo de entrega tiene muchas ventajas, como se describe en una entrada de blog anterior.

## <a name="sideloading-a-custom-linux-distro-package"></a>Instalación de prueba un paquete de distribución de Linux personalizada
Puede crear un paquete personalizado de distribución de Linux como una aplicación para transferir localmente en su equipo personal. Tenga en cuenta que el paquete personalizado no se distribuyen a través de la Microsoft Store a menos que se envía como un mantenedor de distribución.
Para configurar el equipo para agregar o quitar aplicaciones, deberá habilitarla en la configuración del sistema en "Para desarrolladores".  Asegúrese de contar con modo de programador, o bien agregar o quitar aplicaciones seleccionadas

## <a name="for-linux-distro-maintainers"></a>Para los mantenedores de distribución de Linux
Para enviar a la Store, deberá trabajar con nosotros para recibir la aprobación de publicación. Si es un propietario de la distribución de Linux interesado en agregar su distribución a la Microsoft Store, póngase en contacto con wslpartners@microsoft.com.

## <a name="getting-started"></a>Introducción
Siga las instrucciones de la [repositorio de GitHub de distribución del iniciador](https://github.com/Microsoft/WSL-DistroLauncher) para crear un paquete personalizado de distribución de Linux.

 
## <a name="team-blogs"></a>Blogs del equipo
*  [Abra el abastecimiento de un ejemplo WSL para los mantenedores de distribución de Linux y las distribuciones de Linux personalizada de la instalación de prueba](https://blogs.msdn.microsoft.com/commandline/2018/03/26/wsl-distro-launcher/)
* [Blog de línea de comandos](https://blogs.msdn.microsoft.com/commandline/)

## <a name="provide-feedback"></a>Proporcionar comentarios
* [Repositorio de Github del iniciador de distribución](https://github.com/Microsoft/WSL-DistroLauncher)
* [Seguimiento de problemas de GitHub de WSL](https://github.com/Microsoft/BashOnWindows/issues)
* [Portal de UserVoice de línea de comandos](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
