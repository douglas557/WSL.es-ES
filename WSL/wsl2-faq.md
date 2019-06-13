---
title: Preguntas más frecuentes de WSL 2
description: Preguntas más frecuentes sobre el subsistema Windows para Linux 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, el subsistema de windows para linux, windowssubsystem, ubuntu, debian, suse, windows 10, instalar
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 84805278abaeb6334c662e1dfab1bced3e0ddb0b
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038095"
---
# <a name="wsl-2-faq"></a>PREGUNTAS MÁS FRECUENTES DE WSL 2

A continuación es una lista de las preguntas más frecuentes (P+F) sobre el subsistema Windows para Linux 2.

## <a name="does-wsl-2-use-hyper-v-will-it-be-available-on-windows-10-home"></a>¿2 WSL usa Hyper-V? ¿Estará disponible en Windows 10 Home?

WSL 2 estará disponible en todas las SKU que está disponible actualmente, incluido Windows 10 Home WSL.

La versión más reciente de WSL usa la arquitectura Hyper-V para habilitar la virtualización. Esta arquitectura estará disponible en un componente opcional que es un subconjunto de la característica de Hyper-V. Este componente opcional estará disponible en todas las SKU. Puede esperar ver más detalles sobre esta experiencia pronto conforme nos acercamos a la versión 2 de WSL.

## <a name="what-will-happen-to-wsl-1-will-it-be-abandoned"></a>¿Qué sucederá en WSL 1? ¿Se lo abandonará?

Actualmente no tenemos pensado para dejar de utilizar WSL 1. Puede ejecutar WSL 1 y 2 de WSL distribuciones en paralelo y puede actualizar y degradar cualquier distribución en cualquier momento. Adición de WSL 2 como una nueva arquitectura presenta una mejor plataforma para el equipo WSL proporcionar características que hacen que WSL una forma increíble para ejecutar un entorno de Linux en Windows.

## <a name="will-i-be-able-to-run-wsl-2-and-other-3rd-party-virtualization-tools-such-as-vmware-or-virtualbox"></a>¿Podré ejecutar WSL 2 y otras herramientas de virtualización de terceros 3rd como VMware, VirtualBox?

Algunas aplicaciones de terceros 3rd no pueden funcionar cuando Hyper-V está en uso, lo que significa que no podrá ejecutar cuando se habilita WSL 2. Lamentablemente, esto incluye VMware y las versiones de VirtualBox antes del 6 de VirtualBox (VirtualBox 6.0.0 publicada en diciembre de 2018 [ahora es compatible con Hyper-V como un núcleo de ejecución reserva en un host de Windows] [ 1]!)

Estamos investigando maneras de ayudar a resolver este problema. Por ejemplo, se exponen un conjunto de API denominado [plataforma del hipervisor] [ 2] que pueden usar los proveedores de virtualización de terceros para que su software sea compatible con Hyper-V Esto permite a las aplicaciones usar, como la arquitectura de Hyper-V para la emulación de su [Google Android Emulator][3], VirtualBox, 6 y por encima del cual se ahora es compatible con Hyper-V y.

## <a name="can-i-access-the-gpu-in-wsl-2-are-there-plans-to-increase-hardware-support"></a>¿Puedo tener acceso a la GPU en WSL 2? ¿Existen planes para aumentar la compatibilidad de hardware?

En las versiones iniciales de acceso al hardware de WSL 2 soporte se limitará, p. ej.: no será posible acceder a la GPU, serie o USB. Sin embargo, agregar una mejor compatibilidad de dispositivo es alta en el trabajo pendiente, tal como se abrirá muchos más casos de uso para los desarrolladores que deseen interactuar con estos dispositivos. Mientras tanto, siempre puede usar 1 WSL que tiene acceso USB de puerto serie. Por favor, esté atento a este blog y los miembros del equipo en Twitter para mantenerse informado sobre las características más recientes a insider WSL compilaciones y llegar al proporcionarnos sus comentarios sobre los dispositivos que le gustaría interactuar con!

## <a name="will-wsl-2-be-able-to-use-networking-applications"></a>¿2 WSL podrá usar las aplicaciones de red?

Sí, aplicaciones de redes en general se más rápido y funcionan mejor, puesto que tenemos todo el sistema llame a la compatibilidad. Sin embargo, la nueva arquitectura utiliza los componentes de red virtualizados. Esto significa que, en versión preliminar inicial se basa WSL 2 se comportará de forma más parecida a una máquina virtual, p. ej.: WSL 2 tendrán una dirección IP diferente que el equipo host. Estamos comprometidos con la que hace WSL 2 siente igual a 1 WSL y que incluye mejorar nuestra historia de la red. Esperamos poder agregar mejoras tan pronto como podemos, como el acceso a todas las aplicaciones de red de Linux o Windows con localhost. Publicaremos más detalles sobre nuestra historia y mejoras de redes tal como nos acercamos al lanzamiento de WSL 2.

## <a name="can-i-run-wsl-2-in-a-virtual-machine"></a>¿Puedo ejecutar WSL 2 en una máquina virtual?

¡Sí! Deberá asegurarse de que la máquina virtual tiene anidados virtualización habilitada. Esto se puede habilitar en Hyper-V ejecutando el siguiente comando en una ventana de PowerShell con privilegios de administrador:

`Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true`

No olvide reemplazar '&lt;VMName&gt;' con el nombre de la máquina virtual.

 [1]: https://www.virtualbox.org/wiki/Changelog-6.0
 [2]: https://docs.microsoft.com/en-us/virtualization/api/
 [3]: https://devblogs.microsoft.com/visualstudio/hyper-v-android-emulator-support/