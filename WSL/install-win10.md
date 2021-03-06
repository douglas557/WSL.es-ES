---
title: Instalar el Subsistema de Windows para Linux (WSL) en Windows 10
description: Obtenga información sobre cómo instalar distribuciones de Linux en la máquina Windows 10, con un terminal Bash, como Ubuntu, Debian, SUSE, Kali, Fedora, Pengwin y Alpine.
keywords: BashOnWindows, bash, wsl, wsl2, windows, subsistema de windows para linux, subsistemawindows, ubuntu, debian, suse, windows 10, instalación, instalar, habilitación, habilitar, WSL2, versión 2
ms.date: 09/15/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: cf349615dc40f1912fdb4dff3f5593627fa246e6
ms.sourcegitcommit: dee2bf22c0c9f5725122a155d2876fcb2b7427d0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "92211779"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a>Guía de instalación del Subsistema de Windows para Linux para Windows 10

## <a name="install-windows-subsystem-for-linux"></a>Instalación del Subsistema de Windows para Linux

El Subsistema de Windows para Linux tiene dos versiones diferentes entre las que elegir durante el proceso de instalación. WSL 2 presenta un mejor rendimiento general y se recomienda usarlo. Si el sistema no es compatible con WSL 2, o si tiene una situación específica que requiere el almacenamiento de archivos entre sistemas, es posible que desee seguir con WSL 1. Obtén más información sobre la [Comparación de WSL 2 con WSL 1](./compare-versions.md).

## <a name="step-1---enable-the-windows-subsystem-for-linux"></a>Paso 1: Habilitación del Subsistema de Windows para Linux

Antes de instalar distribuciones de Linux en Windows, debe habilitar la característica opcional "Subsistema de Windows para Linux".

Abre PowerShell como administrador y ejecuta:

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

Ahora se recomienda continuar con el paso 2, Actualización a WSL 2, pero si solo quiere instalar WSL 1, ahora puede **reiniciar** el equipo y dirigirse al [Paso 6: Instalación de la distribución de Linux que quiera](./install-win10.md#step-6---install-your-linux-distribution-of-choice). Para actualizar a WSL 2, **espere para reiniciar** la máquina y continúe con el paso siguiente.

## <a name="step-2---update-to-wsl-2"></a>Paso 2: Actualización a WSL 2

Para actualizar a WSL 2, debe ejecutar Windows 10.

### <a name="requirements"></a>Requisitos

- Para sistemas x64: La **versión 1903** o posterior, con la **compilación 18362** o posterior.
- Para sistemas ARM64: La **versión 2004** o posterior, con la **compilación 19041** o posterior.
- Las compilaciones anteriores a 18362 no admiten WSL 2. Use el [Asistente para Windows Update](https://www.microsoft.com/software-download/windows10) para actualizar su versión de Windows.

Para comprobar la versión y el número de compilación, seleccione la **tecla del logotipo de Windows + R**, escriba **winver** y seleccione **Aceptar**. (También puedes escribir el comando `ver` en el símbolo del sistema de Windows). [Actualice a la versión más reciente de Windows](ms-settings:windowsupdate) en el menú Configuración.

> [!NOTE]
> Si está ejecutando Windows 10, versión 1903 o 1909, abra "Configuración" en el menú de Windows, vaya a "Actualización y seguridad" y seleccione "Buscar actualizaciones". El número de compilación debe ser 18362.1049 o posterior o 18363.1049 o posterior, con la compilación secundaria posterior a .1049. Leer más: [La compatibilidad con WSL 2 estará disponible en breve para las versiones 1903 y 1909 de Windows 10](https://devblogs.microsoft.com/commandline/wsl-2-support-is-coming-to-windows-10-versions-1903-and-1909/). Consulte las [instrucciones de solución de problemas](./troubleshooting.md#im-on-windows-10-version-1903-and-i-still-do-not-see-options-for-wsl-2).

## <a name="step-3---enable-virtual-machine-feature"></a>Paso 3: Habilitación de la característica Máquina virtual

Antes de instalar WSL 2, debe habilitar la característica opcional **Plataforma de máquina virtual**.

Abre PowerShell como administrador y ejecuta:

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

**Reinicia** la máquina para completar la instalación de WSL y la actualización a WSL 2.

## <a name="step-4---download-the-linux-kernel-update-package"></a>Paso 4: Descarga del paquete de actualización del kernel de Linux

1. Descargue la versión más reciente:
    - [Paquete de actualización del kernel de Linux en WSL 2 para máquinas x64](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)

    > [!NOTE]
    > Si estás usando una máquina ARM64, descarga el [paquete ARM64](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) en su lugar. Si no está seguro de qué tipo de máquina tiene, abra el símbolo del sistema o PowerShell y escriba: `systeminfo | find "System Type"`.

2. Ejecuta el paquete de actualización que descargaste en el paso anterior. (Haga doble clic para ejecutarlo. Se le pedirán permisos elevados. Seleccione "Sí" para aprobar esta instalación).

Una vez completada la instalación, vaya al paso siguiente: configuración de WSL 2 como versión predeterminada al instalar nuevas distribuciones de Linux. (Omita este paso si quiere que las nuevas instalaciones de Linux se establezcan en WSL 1).

> [!NOTE]
> Para obtener más información, consulta el artículo [cambios en la actualización del kernel de Linux en WSL2](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004), disponible en el [blog de la línea de comandos de Windows](https://aka.ms/cliblog).

## <a name="step-5---set-wsl-2-as-your-default-version"></a>Paso 5: Definición de WSL 2 como versión predeterminada

Abra PowerShell y ejecute este comando para establecer WSL 2 como versión predeterminada al instalar una nueva distribución de Linux:

```powershell
wsl --set-default-version 2
```

> [!NOTE]
> La actualización de WSL 1 a WSL 2 puede tardar varios minutos en completarse, en función del tamaño de la distribución de destino. Si ejecuta una instalación anterior (heredada) de WSL 1 de la Actualización de aniversario de Windows 10 o de Creators Update, es posible que se produzca un error de actualización. Siga estas instrucciones para [desinstalar y quitar las distribuciones heredadas](./install-legacy.md#uninstallingremoving-the-legacy-distro).
>
> Si `wsl --set-default-version` resulta en un comando no válido, especifique `wsl --help`. Si `--set-default-version` no aparece, significa que el sistema operativo no lo admite y debe actualizar a la versión 1903, compilación 18362 o posterior.
>
> Es posible que vea este mensaje después de ejecutar el comando: `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`. Aún debe instalar el paquete MSI de actualización del kernel de Linux.

## <a name="step-6---install-your-linux-distribution-of-choice"></a>Paso 6: Instalación de la distribución de Linux que quiera

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

## <a name="step-7---set-up-a-new-distribution"></a>Paso 7: Configuración de una nueva distribución

La primera vez que inicies una distribución de Linux recién instalada, se abrirá una ventana de la consola y se te pedirá que esperes un minuto o dos para que los archivos se descompriman y se almacenen en tu equipo. Todos los inicios posteriores deberían tardar menos de un segundo en completarse.

Tendrás que [crear una cuenta de usuario y una contraseña para la nueva distribución de Linux](./user-support.md).

![Desempaquetado de Ubuntu en la consola de Windows](media/UbuntuInstall.png)

**ENHORABUENA. Ha instalado y configurado correctamente una distribución de Linux completamente integrada con el sistema operativo Windows.**

## <a name="install-windows-terminal-optional"></a>Instalación de Terminal Windows (opcional)

Terminal Windows permite habilitar varias pestañas (cambiar rápidamente entre varias líneas de comandos de Linux, el símbolo del sistema de Windows, PowerShell, la CLI de Azure, etc.), crear enlaces de teclado personalizados (teclas de método abreviado para abrir o cerrar pestañas, copiar y pegar, etc.), usar la característica de búsqueda y configurar temas personalizados (esquemas de colores, estilos y tamaños de fuente, imagen de fondo/desenfoque/transparencia). [Más información.](/windows/terminal)

[Instalación de Terminal Windows](/windows/terminal/get-started).

  ![Terminal Windows](media/terminal.png)

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
  - Abra **Configuración** -> **Sistema --> **Almacenamiento** -> **Más configuraciones de almacenamiento: Cambia el lugar donde se guarda el nuevo contenido**
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
  - En este perfil de distribución de Linux, debe haber una carpeta denominada LocalState. Haga clic con el botón derecho en ella para mostrar un menú de opciones. Seleccione Propiedades > Opciones avanzadas y, a continuación, asegúrese de que las casillas "Comprimir contenido para ahorrar espacio en disco" y "Cifrar contenido para proteger datos" no estén seleccionadas (activadas). Si se le pregunta si quiere aplicar esto solo a la carpeta actual o a todas las subcarpetas y archivos, seleccione "solo esta carpeta", ya que solo quiere borrar la marca de compresión. A continuación, el comando `wsl --set-version` debería funcionar.

![Captura de pantalla de la configuración de la propiedad de distribución de WSL](media/troubleshooting-virtualdisk-compress.png)

> [!NOTE]
> En mi caso, la carpeta LocalState de la distribución de Ubuntu 18.04 se encontraba en C:\Users\<my-user-name>\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu18.04onWindows_79rhkp1fndgsc.
>
> Consulte el [subproceso n.º 4103 de la documentación sobre WSL en GitHub](https://github.com/microsoft/WSL/issues/4103), en el que se realiza el seguimiento de este problema para obtener información actualizada.

- **El término 'wsl' no se reconoce como nombre de cmdlet, función, archivo de script o programa ejecutable.**
  - Asegúrate de que el [componente opcional del Subsistema de Windows para Linux esté instalado](./install-win10.md#step-3---enable-virtual-machine-feature). Además, si usa un dispositivo ARM64 y ejecuta este comando desde PowerShell, recibirá este error. En su lugar, ejecuta `wsl.exe` desde [PowerShell Core](/powershell/scripting/install/installing-powershell-core-on-windows) o el símbolo del sistema.

- **Error: Esta actualización solo se aplica a las máquinas con el Subsistema de Windows para Linux.**
  - Para instalar el paquete MSI de actualización del kernel de Linux, WSL es necesario y debe habilitarse primero. Si se produce un error, verá el mensaje: `This update only applies to machines with the Windows Subsystem for Linux`.
  - Hay tres posibles motivos para ver este mensaje:

  1. Todavía tiene una versión antigua de Windows que no es compatible con WSL 2. Consulte el paso 2 para conocer los requisitos de la versión y los vínculos de la actualización.

  2. WSL no está habilitado. Tendrá que volver al paso 1 y asegurarse de que la característica WSL opcional está habilitada en la máquina.

  3. Después de habilitar WSL, es necesario un reinicio para que surta efecto. Reinicie la máquina e inténtelo de nuevo.

- **Error: WSL 2 requiere una actualización en su componente de kernel. Para obtener más información, visite https://aka.ms/wsl2kernel.**
  - Si falta el paquete del kernel de Linux en la carpeta %SystemRoot%\system32\lxss\tools, se mostrará este error. Para resolverlo, instale el paquete MSI de actualización del kernel de Linux en del paso 4 de estas instrucciones de instalación. Es posible que deba desinstalar el paquete MSI desde ["Agregar o quitar programas"](ms-settings:appsfeatures-app) e instalarlo de nuevo.
