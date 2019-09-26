---
title: Preguntas más frecuentes sobre WSL 2
description: Preguntas más frecuentes sobre el subsistema de Windows para Linux 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, subsistema de windows para linux, subsistemawindows, ubuntu, debian, suse, windows 10, instalación
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: c4a8c02db6563d7ad572917578c1a49d419f1756
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269572"
---
# <a name="wsl-2-faq"></a>PREGUNTAS MÁS FRECUENTES SOBRE WSL 2

A continuación se muestra una lista de preguntas más frecuentes (p + f) sobre el subsistema de Windows para Linux 2.

## <a name="does-wsl-2-use-hyper-v-will-it-be-available-on-windows-10-home"></a>¿Usa Hyper-V WSL 2? ¿Estará disponible en Windows 10 Home?

WSL 2 estará disponible en todas las SKU donde WSL está disponible actualmente, incluido Windows 10 Home.

La versión más reciente de WSL usa la arquitectura de Hyper-V para habilitar su virtualización. Esta arquitectura estará disponible en el componente opcional "plataforma de máquina virtual". Este componente opcional estará disponible en todas las SKU. Pronto podrá ver más detalles sobre esta experiencia cuando se acerque a la versión WSL 2.

## <a name="what-will-happen-to-wsl-1-will-it-be-abandoned"></a>¿Qué pasará con WSL 1? ¿Se abandonará?

Actualmente no tenemos planes para dejar de usar WSL 1. Puede ejecutar WSL 1 y WSL 2 distribuciones en paralelo, y puede actualizar y degradar cualquier distribución en cualquier momento. Agregar WSL 2 como una nueva arquitectura presenta una plataforma mejor para que el equipo de WSL entregue características que hacen WSL una forma sorprendente de ejecutar un entorno de Linux en Windows.

## <a name="will-i-be-able-to-run-wsl-2-and-other-3rd-party-virtualization-tools-such-as-vmware-or-virtualbox"></a>¿Podré ejecutar WSL 2 y otras herramientas de virtualización de terceros como VMware o VirtualBox?

Algunas aplicaciones de terceros no pueden funcionar cuando se usa Hyper-V, lo que significa que no podrán ejecutarse cuando se habilita WSL 2. Desafortunadamente, esto incluye VMware, y las versiones de VirtualBox anteriores a VirtualBox 6 (VirtualBox 6.0.0 publicadas en diciembre 2018 [ahora admite Hyper-V como núcleo de ejecución de reserva en un host de Windows][1]).

Estamos investigando maneras de ayudar a resolver este problema. Por ejemplo, se expone un conjunto de API llamada [plataforma de hipervisor][2] que los proveedores de virtualización de terceros pueden usar para que el software sea compatible con Hyper-V. Esto permite que las aplicaciones usen la arquitectura de Hyper-V para su emulación, como [Google Android Emulator][3]y VirtualBox 6 y versiones posteriores, que ahora son compatibles con Hyper-V.

## <a name="can-i-access-the-gpu-in-wsl-2-are-there-plans-to-increase-hardware-support"></a>¿Puedo acceder a la GPU en WSL 2? ¿Hay planes para aumentar la compatibilidad de hardware?

En las versiones iniciales de, la compatibilidad con el acceso al hardware de WSL 2 será limitada; por ejemplo, no podrá acceder a la GPU, en serie o en USBs. Sin embargo, agregar mejor compatibilidad con dispositivos es alto en nuestro trabajo pendiente, ya que se abren muchos más casos de uso para los desarrolladores que quieren interactuar con estos dispositivos. Mientras tanto, siempre puede usar WSL 1, que tiene el puerto serie y el acceso USB. Manténgase atento a este blog y WSL a los miembros del equipo en Twitter para mantenerse informado sobre las características más recientes que llegan a las compilaciones de Insider y ponerse en contacto con nosotros para enviarnos sus comentarios sobre los dispositivos con los que le gustaría interactuar.

## <a name="will-wsl-2-be-able-to-use-networking-applications"></a>¿WSL 2 podrá usar aplicaciones de red?

Sí, en las aplicaciones de red generales serán más rápidas y funcionarán mejor, ya que tenemos compatibilidad total con llamadas del sistema. Sin embargo, la nueva arquitectura utiliza componentes de red virtualizados. Esto significa que en la versión preliminar inicial, WSL 2 se comportará de forma más similar a una máquina virtual, por ejemplo: WSL 2 tendrá una dirección IP distinta de la del equipo host. Nos comprometemos a que WSL 2 tenga el mismo aspecto que WSL 1 y eso incluye mejorar nuestro caso de red. Esperamos agregar mejoras tan rápidamente como sea posible, como tener acceso a todas las aplicaciones de red desde Linux o Windows con localhost. Publicaremos más detalles sobre nuestra historia de redes y mejoras a medida que se aproxima al lanzamiento de WSL 2.

## <a name="can-i-run-wsl-2-in-a-virtual-machine"></a>¿Puedo ejecutar WSL 2 en una máquina virtual?

Sí. Debe asegurarse de que la máquina virtual tiene habilitada la virtualización anidada. Para habilitarlo en el host de Hyper-V primario, ejecute el siguiente comando en una ventana de PowerShell con privilegios de administrador:

`Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true`

Asegúrese de reemplazar "&lt;VMName&gt;" por el nombre de la máquina virtual.

## <a name="can-i-use-wslconf-in-wsl-2"></a>¿Puedo usar WSL. conf en WSL 2?

WSL 2 admite el mismo archivo WSL. conf que usa WSL 1. Esto significa que todas las opciones de configuración que haya establecido en un distribución de WSL 1, como el montaje automático de unidades de Windows, la habilitación o deshabilitación de la interoperabilidad, el cambio del directorio donde se montarán las unidades de Windows, etc. funcionarán en WSL 2. Puede obtener más información sobre las opciones de configuración en WSL en la página de [Administración de distribución](./wsl-config.md) . 

 [1]: https://www.virtualbox.org/wiki/Changelog-6.0
 [2]: https://docs.microsoft.com/en-us/virtualization/api/
 [3]: https://devblogs.microsoft.com/visualstudio/hyper-v-android-emulator-support/
