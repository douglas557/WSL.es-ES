---
title: Preguntas más frecuentes sobre WSL 2
description: Encuentre respuestas a las preguntas más frecuentes (P+F) sobre el Subsistema de Windows para Linux 2, como "¿Puedo ejecutar WSL 2 en una máquina virtual?".
keywords: BashOnWindows, bash, wsl, wsl2, windows, subsistema de windows para linux, subsistemawindows, ubuntu, debian, suse, windows 10, instalación
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: a021dc3c6c3c2a14fea631f2733d2b846c6fe3ad
ms.sourcegitcommit: 910845e9b3f980b2c5b9b4968331a706720603c6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/28/2020
ms.locfileid: "89058490"
---
# <a name="wsl-2-faqs"></a>P+F sobre WSL 2

A continuación se incluye una lista de preguntas más frecuentes (P+F) sobre el Subsistema de Windows para Linux 2.

## <a name="does-wsl-2-use-hyper-v-will-it-be-available-on-windows-10-home"></a>¿WSL 2 utiliza Hyper-V? ¿Estará disponible en Windows 10 Home?

WSL 2 está disponible en todas las SKU donde WSL está disponible actualmente, incluido Windows 10 Home.

La versión más reciente de WSL usa la arquitectura de Hyper-V para habilitar su virtualización. Esta arquitectura estará disponible en el componente opcional "Plataforma de máquina virtual". Este componente opcional estará disponible en todas las SKU. Pronto podrás ver más detalles sobre esta experiencia cuando se acerque el lanzamiento de WSL 2.

## <a name="what-will-happen-to-wsl-1-will-it-be-abandoned"></a>¿Qué pasará con WSL 1? ¿Se abandonará?

Actualmente no tenemos planes para dejar en desuso WSL 1. Puedes ejecutar distribuciones de WSL 1 y WSL 2 en paralelo, y puedes actualizar y degradar cualquier distribución en cualquier momento. La adición de WSL 2 como una nueva arquitectura presenta una plataforma mejor para que el equipo de WSL entregue características que convierten WSL en un método increíble para ejecutar un entorno de Linux en Windows.

## <a name="will-i-be-able-to-run-wsl-2-and-other-3rd-party-virtualization-tools-such-as-vmware-or-virtualbox"></a>¿Podré ejecutar WSL 2 y otras herramientas de virtualización de terceros, como VMware o VirtualBox?

Algunas aplicaciones de terceros, como VMware y VirtualBox, no pueden funcionar cuando Hyper-V está en uso, lo que significa que no podrán ejecutarse mientras WSL 2 esté habilitado. Sin embargo, VirtualBox y VMware han publicado versiones compatibles con Hyper-V y WSL2 recientemente. Puede obtener más información sobre los [cambios de VirtualBox aquí][1] y sobre los [cambios de VMware aquí][4].

Trabajamos de forma constante en las soluciones para admitir la integración de terceros de Hyper-V. Por ejemplo, exponemos un conjunto de API llamado [Hypervisor Platform][2] que los proveedores de virtualización externos pueden usar para hacer que su software sea compatible con Hyper-V. Esto permite que las aplicaciones usen la arquitectura de Hyper-V para su emulación, como [Google Android Emulator][3] y VirtualBox 6 y versiones posteriores, que ahora son compatibles con Hyper-V.

## <a name="can-i-access-the-gpu-in-wsl-2-are-there-plans-to-increase-hardware-support"></a>¿Puedo acceder a la GPU en WSL 2? ¿Hay planes para aumentar la compatibilidad de hardware?

Hemos publicado compatibilidad para acceder a la GPU dentro de las distribuciones de WSL 2. Esto significa que ahora puede usar WSL para escenarios de aprendizaje automático, inteligencia artificial y ciencia de datos más fácilmente cuando hay involucrados conjuntos de macrodatos. Puede encontrar un tutorial de [introducción a la compatibilidad con GPU aquí](./tutorials/gpu-compute). A partir de ahora, WSL 2 no incluye compatibilidad de serie ni compatibilidad con dispositivos USB. Estamos investigando la mejor manera de agregar estas características.

## <a name="will-wsl-2-be-able-to-use-networking-applications"></a>¿WSL 2 podrá usar aplicaciones de redes?

Sí, en general, las aplicaciones de redes serán más rápidas y funcionarán mejor, ya que ofrecemos compatibilidad total con las llamadas del sistema. Sin embargo, la nueva arquitectura utiliza componentes de redes virtualizados. Esto significa que en las compilaciones iniciales de la versión preliminar, WSL 2 se comportará de forma más similar a una máquina virtual, por ejemplo: WSL 2 tendrá una dirección IP distinta de la del equipo host. Nos comprometemos a que WSL 2 tenga el mismo aspecto que WSL 1, lo que incluye mejorar nuestra historia de redes. 

## <a name="can-i-run-wsl-2-in-a-virtual-machine"></a>¿Puedo ejecutar WSL 2 en una máquina virtual?

Sí. Debes asegurarte de que la máquina virtual tiene habilitada la virtualización anidada. Para habilitarlo en el host de Hyper-V primario, ejecuta el siguiente comando en una ventana de PowerShell con privilegios de administrador:

`Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true`

Asegúrate de reemplazar "&lt;VMName&gt;" por el nombre de tu máquina virtual.

## <a name="can-i-use-wslconf-in-wsl-2"></a>¿Puedo usar wsl.conf en WSL 2?

WSL 2 admite el mismo archivo wsl.conf que se usa en WSL 1. Esto significa que todas las opciones de configuración que hayas establecido en una distribución de WSL 1, como el montaje automático de unidades de Windows, la habilitación o deshabilitación de la interoperabilidad, el cambio del directorio donde se montarán las unidades de Windows, etc., funcionarán en WSL 2. Puedes obtener más información sobre las opciones de configuración en WSL en la página [Administración de distribuciones](./wsl-config.md).

 [1]: https://www.virtualbox.org/wiki/Changelog-6.0
 [2]: https://docs.microsoft.com/virtualization/api/
 [3]: https://devblogs.microsoft.com/visualstudio/hyper-v-android-emulator-support/
 [4]: https://blogs.vmware.com/workstation/2020/01/vmware-workstation-tech-preview-20h1.html
