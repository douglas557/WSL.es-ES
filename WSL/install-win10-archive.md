---
title: Instrucciones de WSL archivadas
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ROBOTS: NOINDEX
ms.openlocfilehash: 1de614dccbbb8d0ef1b9ac070f6ec90281339858
ms.sourcegitcommit: 16ffb1a096a4a7fbb77c58f92258051930cc82da
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2020
ms.locfileid: "86157961"
---
# <a name="archived-instructions"></a>Instrucciones archivadas

La siguiente guía recorrerá los pasos necesarios para instalar el Subsistema de Windows para Linux (WSL) en un equipo que ejecuta Windows 10.

## <a name="enable-the-windows-subsystem-for-linux-optional-feature"></a>Habilitación de la característica opcional Subsistema de Windows para Linux

Antes de instalar una distribución de Linux, debes habilitar la característica opcional "Subsistema de Windows para Linux" en Windows 10:

1. Abre PowerShell como administrador y escribe este script:

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

1. Reinicia el equipo cuando se te solicite.

## <a name="install-a-linux-distribution"></a>Instalación de una distribución de Linux

Existen tres maneras de descargar e instalar tus distribuciones de Linux preferidas:

- Descargarlas e instalarlas de Microsoft Store (ver la información que hay a continuación).
- [Descargarlas e instalarlas manualmente desde la línea de comandos](install-manual.md)
- [Instalar en Windows Server](install-on-server.md)

### <a name="install-from-the-microsoft-store"></a>Descargar desde Microsoft Store

Las distribuciones de Linux se pueden instalar desde Microsoft Store en Windows 10 (compilación 16215 y posteriores).

> [!NOTE]
> Sigue estos pasos para [comprobar el número de compilación de Windows 10](troubleshooting.md#check-your-build-number).

1. Abre Microsoft Store y elige tu distribución de Linux favorita.

    ![Vista de las distribuciones de Linux en Microsoft Store](media/store.png)

    En los vínculos siguientes se abrirá la página de Microsoft Store para cada distribución:

    - [Ubuntu 16.04 LTS](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [Ubuntu 18.04 LTS](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [OpenSUSE Leap 15](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    - [OpenSUSE Leap 42](https://www.microsoft.com/store/apps/9njvjts82tjx)
    - [SUSE Linux Enterprise Server 12](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    - [SUSE Linux Enterprise Server 15](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    - [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [Fedora Remix for WSL](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [Pengwin](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [Pengwin Enterprise](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [Alpine WSL](https://www.microsoft.com/store/apps/9p804crf0395)

1. Selecciona "Obtener" y, una vez finalizada la descarga de la distribución, selecciona "Iniciar".

    ![Vista de las distribuciones de Linux en Microsoft Store](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a>Completar la inicialización de la distribución

Después de iniciar la distribución de Linux, sigue las instrucciones en pantalla para inicializarla.

> [!NOTE]
> En Windows Server, inicia la distribución mediante el archivo ejecutable (`<distro>.exe`) en la carpeta de instalación.

La primera vez que se ejecute una distribución recién instalada, se abrirá una ventana de consola y se te pedirá que esperes un minuto o dos para que se complete la instalación. Durante esta fase final de la instalación, los archivos de la distribución se descomprimen y almacenan en el equipo, listos para usarse. Esta acción puede tardar aproximadamente un minuto o más en función del rendimiento de los dispositivos de almacenamiento del equipo. Esta fase de instalación inicial solo es necesaria cuando una distribución se instala sin problemas; todos los inicios futuros deben tardar menos de un segundo.

## <a name="set-up-a-new-linux-user-account"></a>Configuración de una nueva cuenta de usuario de Linux

Una vez completada la instalación, se te pedirá que crees una nueva cuenta de usuario (y su contraseña).

![Desempaquetado de Ubuntu en la consola de Windows](media/UbuntuInstall.png)

Esta cuenta de usuario es para el usuario normal sin privilegios de administrador con el que se iniciará sesión de manera predeterminada al iniciar una distribución. Puedes elegir cualquier nombre de usuario y contraseña: no tienen ninguna relación con el nombre de usuario de Windows.

Cuando abras una nueva instancia de distribución, no se te pedirá la contraseña, pero, **si elevas un proceso mediante `sudo`, tendrás que escribir la contraseña**, por lo que debes asegurarte de elegir una contraseña que puedas recordar fácilmente. Para obtener más información, consulta la página de [Soporte del usuario](user-support.md).

## <a name="update--upgrade-packages"></a>Actualización de paquetes

La mayoría de las distribuciones incluyen un catálogo de paquetes vacío o mínimo. Se recomienda encarecidamente actualizar periódicamente el catálogo de paquetes, así como actualizar los paquetes instalados con tu administrador de paquetes preferido de la distribución. Para Debian y Ubuntu, usa apt:

```bash
sudo apt update && sudo apt upgrade
```

Windows no actualiza automáticamente las distribuciones de Linux. Se trata de una tarea que la mayoría de los usuarios de Linux prefieren controlar por sí mismos.

Disfruta con la nueva distribución de Linux en WSL.

## <a name="troubleshooting"></a>Solucionar problemas

A continuación, se muestran errores de instalación relacionados y las correcciones sugeridas. Consulta la [página de solución de problemas de WSL](troubleshooting.md) para ver otros errores generales y sus soluciones.

### <a name="installation-failed-with-error-0x8007007e"></a>Error 0x8007007e en la instalación

Este error se produce cuando el sistema no es compatible con Linux de Store.  Asegúrese de que:

- Estás ejecutando la compilación 16215 de Windows o una posterior. [Comprueba el número de compilación](troubleshooting.md#check-your-build-number).
- El componente opcional del subsistema de Windows para Linux está habilitado y se ha reiniciado el equipo.  [Asegúrate de que WSL está habilitado](troubleshooting.md#confirm-wsl-is-enabled).

### <a name="installation-failed-with-error-0x80070003"></a>Error 0x80070003 en la instalación

El Subsistema de Windows para Linux solo se ejecuta en la unidad del sistema (normalmente se trata de la unidad `C:`). Asegúrate de que las distribuciones se almacenan en la unidad del sistema:

- Abre **Configuración** -> **Almacenamiento** -> **Más opciones de almacenamiento: Cambia la ubicación en que se guarda el nuevo contenido**
  
    ![Imagen de la configuración del sistema para instalar aplicaciones en la unidad C:](media/AppStorage.png)

### <a name="wslregisterdistribution-failed-with-error-0x8007019e"></a>Error 0x8007019e de WslRegisterDistribution

El componente opcional del Subsistema de Windows para Linux no está habilitado:

- Abre el **Panel de control** -> **Programas y características** -> **Activa o desactiva la característica de Windows** -> Selecciona el **Subsistema de Windows para Linux** o usa el cmdlet de PowerShell mencionado al comienzo de este artículo.
