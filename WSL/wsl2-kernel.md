---
title: Actualización del kernel de Linux en WSL 2
description: Instrucciones sobre cómo actualizar el kernel de Linux en WSL 2 manualmente
keywords: wsl, windows, kernel de linux, subsistema de windows para linux, kernel
ms.date: 03/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: bef722f5653380d9f6d104f1a7c116a7599658c9
ms.sourcegitcommit: ba52d673c123fe8ae61e872a33e218cfc30a1f82
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/07/2020
ms.locfileid: "86033039"
---
# <a name="updating-the-wsl-2-linux-kernel"></a>Actualización del kernel de Linux en WSL 2

Para actualizar manualmente el kernel de Linux dentro de WSL 2, sigue estos pasos.

> [!NOTE] 
> Si el instalador no encuentra WSL 1, haz clic con el botón derecho en el instalador de actualizaciones del kernel de Linux, presiona "Desinstalar" y, luego, vuelve a ejecutar el instalador.

## <a name="download-the-linux-kernel-update-package"></a>Descarga del paquete de actualización del kernel de Linux

Descarga el paquete de actualización [más reciente del kernel de Linux en WSL 2](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) para máquinas x64.

> [!NOTE]
> Si estás usando una máquina ARM64, descarga el [paquete ARM64](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) en su lugar.

## <a name="install-the-linux-kernel-update-package"></a>Instalación del paquete de actualización del kernel de Linux

Para instalar el paquete de actualización del kernel de Linux:

  1. Ejecuta el paquete de actualización que descargaste en el paso anterior.

  2. Se te pedirán permisos elevados, selecciona "Sí" para aprobar esta instalación.

  3. Una vez que se complete la instalación, estarás listo para empezar a usar WSL2.

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a>Planes futuros para actualizar el kernel de Linux en WSL2

Para obtener más información, consulta el artículo [cambios en la actualización del kernel de Linux en WSL2](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004), disponible en el [blog de la línea de comandos de Windows](https://aka.ms/cliblog).

## <a name="troubleshooting"></a>Solucionar problemas

### <a name="this-update-only-applies-to-machines-with-the-windows-subsystem-for-linux"></a>Esta actualización solo se aplica a las máquinas con el subsistema de Windows para Linux.
Para instalar el kernel de MSI, se requiere WSL y debe habilitarse primero. Si se produce un error, verá el mensaje: `This update only applies to machines with the Windows Subsytem for Linux`. 

Hay tres posibles motivos para ver este mensaje:

1. Todavía tiene una versión antigua de Windows que no es compatible con WSL 2. Compruebe los [requisitos de WSL 2](https://docs.microsoft.com/windows/wsl/install-win10#update-to-wsl-2) y actualice para usar WSL 2. 
2. `Windows Subsystem for Linux` no está habilitado. Siga la [Guía de instalación del Subsistema de Windows para Linux](https://docs.microsoft.com/windows/wsl/install-win10).
3. Una vez que haya habilitado `Windows Subsystem for Linux`, es necesario reiniciar el equipo e intentarlo de nuevo.

### `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`

Cada vez que falta el kernel en %SystemRoot%\system32\lxss\tools\, puede que se encuentre con el error anterior.

Estas son algunas formas posibles de resolverlo:

1. Instale el kernel de Linux manualmente siguiendo las instrucciones de: https://aka.ms/wsl2kernel
2. Desinstale MSI desde "Agregar o quitar programas" e instálelo de nuevo.
