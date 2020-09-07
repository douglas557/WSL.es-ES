---
title: Instalar el Subsistema de Windows para Linux (WSL) en Windows 10
description: Obtenga información sobre cómo instalar el Subsistema de Windows para Linux en Windows 10. Windows 10 debe actualizarse a la versión 2004, compilación 19041 o posterior.
keywords: BashOnWindows, bash, wsl, wsl2, windows, subsistema de windows para linux, subsistemawindows, ubuntu, debian, suse, windows 10, instalación, instalar, habilitación, habilitar, WSL2, versión 2
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 14e1697d1f2ac7a1efa17368be830a5c22973bc6
ms.sourcegitcommit: 910845e9b3f980b2c5b9b4968331a706720603c6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/28/2020
ms.locfileid: "89058500"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a>Guía de instalación del Subsistema de Windows para Linux para Windows 10

## <a name="install-the-windows-subsystem-for-linux"></a>Instalar el Subsistema de Windows para Linux

Antes de instalar distribuciones de Linux en Windows, debes habilitar la característica opcional "Subsistema de Windows para Linux".

Abre PowerShell como administrador y ejecuta:

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

Para instalar solo WSL 1, debes reiniciar la máquina ahora y pasar a la sección [Instalación de la distribución de Linux que quieras](./install-win10.md#install-your-linux-distribution-of-choice). De lo contrario, espera a que se reinicie y avanza para actualizar a WSL 2. Obtén más información sobre la [Comparación de WSL 2 con WSL 1](./compare-versions.md).

## <a name="update-to-wsl-2"></a>Actualización a WSL 2

Para actualizar a WSL 2, debe cumplir los siguientes criterios:

- Ejecutar Windows 10, [actualizado a la versión 1903 o posterior](ms-settings:windowsupdate), **compilación 18362** o posterior para sistemas x64.
- Ejecutar Windows 10, actualizado a la versión 2004 o posterior, **compilación 19041**, para sistemas ARM64.
- Tenga en cuenta que, si se encuentra en Windows 10, versión 1903 o 1909, deberá asegurarse de que tiene la corrección compatible adecuada. Se pueden encontrar instrucciones [aquí](https://devblogs.microsoft.com/commandline/wsl-2-support-is-coming-to-windows-10-versions-1903-and-1909/#how-do-i-get-it). 

- Para comprobar la versión de Windows, selecciona la **tecla del logotipo de Windows + R**, escribe **winver** y selecciona **Aceptar**. (También puedes escribir el comando `ver` en el símbolo del sistema de Windows). [Actualice a la versión más reciente de Windows](ms-settings:windowsupdate) si su compilación es anterior a la 18361. [Obtén el Asistente de Windows Update](https://www.microsoft.com/software-download/windows10).

### <a name="enable-the-virtual-machine-platform-optional-component"></a>Habilitación del componente opcional "Plataforma de máquina virtual"

Antes de instalar WSL 2, tienes que habilitar la característica opcional "Plataforma de máquina virtual".

Abre PowerShell como administrador y ejecuta:

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

**Reinicia** la máquina para completar la instalación de WSL y la actualización a WSL 2.

### <a name="set-wsl-2-as-your-default-version"></a>Definición de WSL 2 como versión predeterminada

Abra PowerShell como Administrador y ejecute este comando para establecer WSL 2 como versión predeterminada al instalar una nueva distribución de Linux:

```powershell
wsl --set-default-version 2
```

Es posible que vea este mensaje después de ejecutar el comando: `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`. Siga el vínculo ([https://aka.ms/wsl2kernel](https://aka.ms/wsl2kernel)) e instale MSI desde esa página en nuestra documentación para instalar un kernel de Linux en la máquina para que lo use WSL 2. Una vez instalado el kernel, vuelva a ejecutar el comando, que debería completarse correctamente sin mostrar el mensaje. 

> [!NOTE]
> La actualización de WSL 1 a WSL 2 puede tardar varios minutos en completarse, en función del tamaño de la distribución de destino. Si ejecuta una instalación anterior (heredada) de WSL 1 de la Actualización de aniversario de Windows 10 o de Creators Update, es posible que se produzca un error de actualización. Siga estas instrucciones para [desinstalar y quitar las distribuciones heredadas](https://docs.microsoft.com/windows/wsl/install-legacy#uninstallingremoving-the-legacy-distro). 
>
> Si `wsl --set-default-version` resulta en un comando no válido, especifique `wsl --help`. Si `--set-default-version` no aparece, significa que el sistema operativo no lo admite y debe actualizar a la versión 1903, compilación 18362 o posterior.

## <a name="install-your-linux-distribution-of-choice"></a>Instalación de la distribución de Linux que quieras

1. Abre [Microsoft Store](https://aka.ms/wslstore) y selecciona tu distribución de Linux favorita.

    ![Vista de las distribuciones de Linux en Microsoft Store](media/store.png)

    En los vínculos siguientes se abrirá la página de Microsoft Store para cada distribución:

    - [Ubuntu 16.04 LTS](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [Ubuntu 18.04 LTS](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [Ubuntu 20.04 LTS](https://www.microsoft.com/store/apps/9n6svws3rx71)
    - [OpenSUSE Leap 15.1](https://www.microsoft.com/store/apps/9NJFZK00FGKV)
    - [SUSE Linux Enterprise Server 12 SP5](https://www.microsoft.com/store/apps/9MZ3D1TRP8T1)
    - [SUSE Linux Enterprise Server 15 SP1](https://www.microsoft.com/store/apps/9PN498VPMF3Z)
    - [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [Fedora Remix for WSL](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [Pengwin](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [Pengwin Enterprise](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [Alpine WSL](https://www.microsoft.com/store/apps/9p804crf0395)

2. En la página de la distribución, selecciona "Obtener".

    ![Distribuciones de Linux en Microsoft Store](media/UbuntuStore.png)

## <a name="set-up-a-new-distribution"></a>Configuración de una nueva distribución

La primera vez que inicies una distribución de Linux recién instalada, se abrirá una ventana de la consola y se te pedirá que esperes un minuto o dos para que los archivos se descompriman y se almacenen en tu equipo. Todos los inicios posteriores deberían tardar menos de un segundo en completarse.

Tendrás que [crear una cuenta de usuario y una contraseña para la nueva distribución de Linux](./user-support.md).

![Desempaquetado de Ubuntu en la consola de Windows](media/UbuntuInstall.png)

## <a name="set-your-distribution-version-to-wsl-1-or-wsl-2"></a>Definición de la versión de la distribución en WSL 1 o WSL 2

Para comprobar la versión de WSL asignada a cada una de las distribuciones de Linux que tienes instaladas, abre la línea de comandos de PowerShell y escribe el comando (solo disponible en [Windows, compilación 18362 o posterior](ms-settings:windowsupdate)): `wsl -l -v`.

```powershell
wsl --list --verbose
```

Para establecer que una distribución esté respaldada por una de las dos versiones de WSL, ejecuta:

```powershell
wsl --set-version <distribution name> <versionNumber>
```

Asegúrate de reemplazar `<distribution name>` por el nombre real de tu distribución, y `<versionNumber>` por el número "1" o "2". Puedes volver a cambiar a WSL 1 en cualquier momento; para ello, ejecuta el mismo comando que antes, pero reemplaza "2" por "1".

Además, si quieres que WSL 2 sea la arquitectura predeterminada, puedes hacerlo con este comando:

```powershell
wsl --set-default-version 2
```

De este modo, se establecerá la versión de cualquier nueva distribución instalada en WSL 2.

## <a name="troubleshooting-installation"></a>Solución de problemas de instalación

A continuación, se muestran errores relacionados y las correcciones sugeridas. Consulta la [página de solución de problemas de WSL](troubleshooting.md) para ver otros errores generales y sus soluciones.

- **Error 0x80070003 en la instalación**
  - El Subsistema de Windows para Linux solo se ejecuta en la unidad del sistema (normalmente se trata de la unidad `C:`). Asegúrate de que las distribuciones estén almacenadas en la unidad del sistema:  
  - Abre **Configuración** -> **Almacenamiento** -> **Más opciones de almacenamiento: Cambia el lugar donde se guarda el nuevo contenido**
    ![Imagen de la configuración del sistema para instalar aplicaciones en la unidad C:](media/AppStorage.png)

- **Error 0x8007019e de WslRegisterDistribution**
  - El componente opcional del Subsistema de Windows para Linux no está habilitado:
  - Abre el **Panel de control** -> **Programas y características** -> **Activa o desactiva la característica de Windows** -> Selecciona **Subsistema de Windows para Linux** o usa el cmdlet de PowerShell mencionado al comienzo de este artículo.

- **Error en la instalación 0x80070003 o 0x80370102**
  - Asegúrate de que la virtualización está habilitada dentro del BIOS del equipo. Las instrucciones sobre cómo hacerlo variarán de un equipo a otro y lo más probable es que esta característica esté en opciones relacionadas con la CPU.

- **Error al intentar actualizar: `Invalid command line option: wsl --set-version Ubuntu 2`**
  - Asegúrese de que tiene el Subsistema de Windows para Linux habilitado y de que usa la compilación 18362 de Windows o posterior. Para habilitar WSL, ejecute este comando en un símbolo del sistema de PowerShell con privilegios de administrador: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.

- **La operación solicitada no se pudo completar debido a una limitación del sistema de disco virtual. Los archivos de disco duro virtual deben estar sin comprimir y sin cifrar y no deben ser dispersos.**
  - Anule la selección de la casilla "Compress contents" ("Comprimir contenido") (y también la de "Cifrar los contenidos" si está activada). Para ello, abra la carpeta de perfil de la distribución de Linux. Debe encontrarse en una carpeta del sistema de archivos de Windows, como `USERPROFILE%\AppData\Local\Packages\CanonicalGroupLimited...`.
  - En este perfil de distribución de Linux, debe haber una carpeta denominada LocalState. Haga clic con el botón derecho en ella para mostrar un menú de opciones. Seleccione Propiedades > Opciones avanzadas y, a continuación, asegúrese de que las casillas "Comprimir contenido para ahorrar espacio en disco" y "Cifrar contenido para proteger datos" no estén seleccionadas (activadas). Si se le pregunta si quiere aplicar esto solo a la carpeta actual o a todas las subcarpetas y archivos, seleccione "solo esta carpeta", ya que solo quiere borrar la marca de compresión. A continuación, el comando `wsl –set-version` debería funcionar.

![Captura de pantalla de la configuración de la propiedad de distribución de WSL](media/troubleshooting-virtualdisk-compress.png)

> [!NOTE]
> En mi caso, la carpeta LocalState de la distribución de Ubuntu 18.04 se encontraba en C:\Users\<my-user-name>\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu18.04onWindows_79rhkp1fndgsc.
>
> Consulte el [subproceso n.º 4103 de la documentación sobre WSL en GitHub](https://github.com/microsoft/WSL/issues/4103), en el que se realiza el seguimiento de este problema para obtener información actualizada.

- **El término 'wsl' no se reconoce como nombre de cmdlet, función, archivo de script o programa ejecutable.**
  - Asegúrate de que el [componente opcional del Subsistema de Windows para Linux esté instalado](./install-win10.md#enable-the-virtual-machine-platform-optional-component). Además, si usa un dispositivo ARM64 y ejecuta este comando desde PowerShell, recibirá este error. En su lugar, ejecuta `wsl.exe` desde [PowerShell Core](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6) o el símbolo del sistema.
