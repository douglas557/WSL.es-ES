---
title: Comparación de WSL 2 con WSL 1
description: 'Compare la versión 1 y la versión 2 del Subsistema de Windows para Linux. Conozca las novedades de WSL 2: kernel de Linux real, velocidad más rápida, compatibilidad completa con las llamadas del sistema. WSL 1 funciona mejor si almacena archivos en los sistemas de archivos operativos. Puede ampliar el tamaño del disco de hardware virtual (VHD) de WSL 2.'
keywords: BashOnWindows, bash, wsl, windows, subsistemawindows, gnu, linux, ubuntu, debian, suse, windows 10, cambios en la experiencia de usuario, WSL 2, kernel de linux, aplicaciones de red, localhost, IPv6, disco de hardware virtual, VHD, limitaciones de VHD, error de VHD
ms.date: 09/15/2020
ms.topic: conceptual
ms.localizationpriority: high
ms.custom: contperfq1
ms.openlocfilehash: e8a8fc2c5e844ae5b6a62b2a4f7844e674bdcfd9
ms.sourcegitcommit: 69fc9d3ca22cf3f07622db4cdf80c8ec751fe620
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/19/2020
ms.locfileid: "90818747"
---
# <a name="comparing-wsl-1-and-wsl-2"></a>Comparación de WSL 1 con WSL 2

La diferencia y los motivos principales para actualizar el Subsistema de Windows para Linux de WSL 1 a WSL 2 son:

- **Aumento del rendimiento del sistema de archivos**.
- **Compatibilidad completa con las llamadas del sistema**.

WSL 2 usa la tecnología de virtualización más reciente y óptima para ejecutar un kernel de Linux en una máquina virtual (VM) de utilidad ligera. Sin embargo, WSL 2 no es una experiencia de VM tradicional.

> [!div class="nextstepaction"]
> [Instalación de WSL 1 y actualización a WSL 2](install-win10.md)

## <a name="comparing-features"></a>Comparación de características

Característica | WSL 1 | WSL 2
--- | --- | ---
 Integración entre Windows y Linux| ✅|✅
 Tiempos de arranque rápidos| ✅ | ✅
 Superficie de recursos pequeña| ✅ |✅
 Se ejecuta con las versiones actuales de VMWare y VirtualBox| ✅ | ✅
 VM administradas| ❌ | ✅
 Kernel de Linux completo| ❌ |✅
 Compatibilidad completa con las llamadas del sistema| ❌ | ✅
 Rendimiento entre sistemas de archivos del sistema operativo| ✅ | ❌

Como puede ver en la tabla de comparación anterior, la arquitectura de WSL 2 supera a la de WSL 1 de varias maneras, con la excepción del rendimiento en los sistemas de archivos del sistema operativo.

## <a name="performance-across-os-file-systems"></a>Rendimiento entre sistemas de archivos del sistema operativo

Se recomienda no trabajar en los sistemas operativos con los archivos, a menos que tenga una razón específica para hacerlo. Para lograr la máxima velocidad de rendimiento, almacene los archivos en el sistema de archivos de WSL si está trabajando en una línea de comandos de Linux (Ubuntu, OpenSUSE, etc.). Si trabaja en una línea de comandos de Windows (PowerShell, símbolo del sistema), almacene los archivos en el sistema de archivos de Windows.

Por ejemplo, al almacenar los archivos de proyecto de WSL, haz lo siguiente:

- Usa el directorio raíz del sistema de archivos de Linux: `\\wsl$\Ubuntu-18.04\home\<user name>\Project`
- No uses el directorio raíz del sistema de archivos de Windows: `C:\Users\<user name>\Project`

Puedes acceder al sistema de archivos raíz de Linux con las aplicaciones y herramientas de Windows, como el Explorador de archivos. Intenta abrir una distribución de Linux (como Ubuntu). Para asegurarte de que estás en el directorio principal de Linux, escribe este comando: `cd ~`. Después, abre el sistema de archivos de Linux en el Explorador de archivos. Para ello, escribe *(no olvides el punto al final)* : `explorer.exe .`

WSL 2 solo está disponible en Windows 10, versión 1903, compilación 18362 o superior. Para comprobar la versión de Windows, selecciona la **tecla del logotipo de Windows + R**, escribe **winver** y selecciona **Aceptar**. (También puedes escribir el comando `ver` en el símbolo del sistema de Windows). Es posible que tengas que [actualizar a la versión más reciente de Windows](ms-settings:windowsupdate). En el caso de las compilaciones inferiores a 18362, no se admite WSL en absoluto.

> [!NOTE]
> WSL 2 funcionará con [VMWare 15.5.5 y versiones posteriores](https://blogs.vmware.com/workstation/2020/05/vmware-workstation-now-supports-hyper-v-mode.html) y [VirtualBox 6 y versiones posteriores](https://www.virtualbox.org/wiki/Changelog-6.0). Obtenga más información en las [preguntas más frecuentes sobre WSL 2](./wsl2-faq.md#will-i-be-able-to-run-wsl-2-and-other-3rd-party-virtualization-tools-such-as-vmware-or-virtualbox).

## <a name="whats-new-in-wsl-2"></a>Novedades de WSL 2

WSL 2 es una revisión importante de la arquitectura subyacente y usa tecnología de virtualización y un kernel de Linux para habilitar las nuevas características. Los principales objetivos de esta actualización son aumentar el rendimiento del sistema de archivos y agregar compatibilidad completa con las llamadas del sistema.

- [Requisitos del sistema de VSL 2](./install-win10.md#step-2---update-to-wsl-2)
- [Actualización de WSL 1 a WSL 2](./install-win10.md#step-2---update-to-wsl-2)
- [Preguntas más frecuentes sobre WSL 2](./wsl2-faq.md)

### <a name="wsl-2-architecture"></a>Arquitectura de WSL 2

Una experiencia de VM tradicional puede presentar un arranque lento, aislamiento y un consumo excesivo de recursos, además de exigir tiempo para su administración. WSL 2 no tiene estos atributos.

WSL 2 ofrece las ventajas de WSL 1, incluida una integración perfecta entre Windows y Linux, tiempos de arranque más breves y una superficie de recursos pequeña. Además, no requiere ninguna configuración ni administración de las VM. Aunque WSL 2 usa una VM, se administra y se ejecuta en segundo plano, lo que te permite disfrutar de la misma experiencia de usuario que WSL 1.

### <a name="full-linux-kernel"></a>Kernel de Linux completo

Microsoft ha creado el kernel de Linux en WSL 2 a partir de la rama estable más reciente. Para ello, se basó en el origen disponible en kernel.org. Este kernel se ha ajustado especialmente para WSL 2, y se ha optimizado su tamaño y rendimiento para ofrecer una increíble experiencia de Linux en Windows. El kernel recibirá actualizaciones de Windows, lo que significa que obtendrás las correcciones de seguridad y las mejoras del kernel más recientes sin que debas administrarlo por tu cuenta.

El [kernel de Linux para WSL 2 es de código abierto](https://github.com/microsoft/WSL2-Linux-Kernel). Si quieres obtener más información, consulta la entrada de blog [Envío de un kernel de Linux con Windows](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/), escrita por el equipo que lo creó.

### <a name="increased-file-io-performance"></a>Mayor rendimiento de E/S de archivos

Las operaciones de uso intensivo de archivos, como git clone, npm install, apt update, apt upgrade y otras, son considerablemente más rápidas con WSL 2.

El aumento de la velocidad real dependerá de la aplicación que se esté ejecutando y de cómo interactúes con el sistema de archivos. Las versiones iniciales de WSL 2 se ejecutan hasta 20 veces más rápido en comparación con WSL 1 al desempaquetar un archivo tarball comprimido, y aproximadamente entre 2y 5 veces más rápido cuando se usan git clone, npm install y cmake en distintos proyectos.

### <a name="full-system-call-compatibility"></a>Compatibilidad completa con las llamadas del sistema

Los archivos binarios de Linux usan llamadas del sistema para ejecutar funciones, como el acceso a archivos, la solicitud de memoria, la creación de procesos, etc. Mientras que WSL 1 usaba una capa de traducción creada por el equipo de WSL, WSL 2 incluye su propio kernel de Linux con total compatibilidad con las llamadas del sistema. Entre las ventajas se incluyen las siguientes:

- Un conjunto de aplicaciones nuevo y completo que se pueden ejecutar en WSL, como **[Docker](tutorials/wsl-containers.md)** , entre otros.

- Todas las actualizaciones del kernel de Linux están listas para su uso inmediato. (No tienes que esperar a que el equipo de WSL implemente actualizaciones y agregue los cambios).

### <a name="wsl-2-uses-a-smaller-amount-of-memory-on-startup"></a>WSL 2 usa una cantidad menor de memoria en el inicio

WSL 2 usa una VM de utilidad ligera en un kernel de Linux real con una superficie de memoria pequeña. La utilidad asignará memoria respaldada por direcciones virtuales al iniciarse. Está configurada para empezar con una pequeña proporción de la memoria total que se necesitaba para WSL 1.

## <a name="exceptions-for-using-wsl-1-rather-than-wsl-2"></a>Excepciones para usar WSL 1 en lugar de WSL 2

Te recomendamos que uses WSL 2, ya que ofrece un rendimiento mayor y compatibilidad completa con las llamadas del sistema. Sin embargo, hay algunos escenarios específicos en los que podrías preferir el uso de WSL 1. Considera el uso de WSL 1 en los casos siguientes:

- Los archivos de proyecto se deben almacenar en el sistema de archivos de Windows. WSL 1 ofrece un acceso más rápido a los archivos montados desde Windows.
  - Si vas a usar tu distribución de WSL para Linux para acceder a los archivos de proyecto en el sistema de archivos de Windows, y estos archivos no se pueden almacenar en el sistema de archivos de Linux, obtendrás un mayor rendimiento en los sistemas de archivos del sistema operativo mediante WSL 1.
- Un proyecto requiere la compilación cruzada con las herramientas de Windows y Linux en los mismos archivos.
  - El rendimiento de los archivos en los sistemas operativos Windows y Linux es mayor en WSL 1 que en WSL 2, por lo que, si usas aplicaciones Windows para acceder a archivos de Linux, obtendrás un mayor rendimiento con WSL 1.

> [!NOTE]
> Considera la posibilidad de probar la [extensión Remote WSL](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl) de VS Code para poder almacenar los archivos de proyecto en el sistema de archivos de Linux, mediante las herramientas de línea de comandos de Linux, pero también con VS Code en Windows para crear, editar, depurar o ejecutar el proyecto en un explorador de Internet, sin experimentar las ralentizaciones de rendimiento asociadas con el trabajo en los sistemas de archivos de Windows. [Más información](tutorials/wsl-vscode.md).

## <a name="accessing-network-applications"></a>Acceso a aplicaciones de red

### <a name="accessing-linux-networking-apps-from-windows-localhost"></a>Acceso a las aplicaciones de red de Linux desde Windows (localhost)

Si vas a crear una aplicación de red (por ejemplo, una aplicación que se ejecute en NodeJS o SQL Server) en la distribución de Linux, puedes acceder a ella desde una aplicación de Windows (como el explorador de Internet Edge o Chrome) mediante `localhost` (como lo harías de manera habitual).

Sin embargo, si ejecutas una versión anterior de Windows (compilación 18945 o anterior), tendrás que obtener la dirección IP de la VM host de Linux (o [actualizar a la versión más reciente de Windows](ms-settings:windowsupdate)).

Para buscar la dirección IP de la máquina virtual que habilita tu distribución de Linux:

- Desde la distribución de WSL (por ejemplo, Ubuntu), ejecuta el comando: `ip addr`
- Busca la dirección en el valor `inet` de la interfaz `eth0` y cópiala.
- Si tienes instalada la herramienta grep, puedes buscarla más fácilmente filtrando el resultado con el comando: `ip addr | grep eth0`
- Conéctate al servidor de Linux con esta dirección IP.

La imagen siguiente muestra un ejemplo con la conexión a un servidor de Node.js mediante el navegador Edge.

![Conexión al servidor de NodeJS con Edge](media/wsl2-network-w2l.jpg)

### <a name="accessing-windows-networking-apps-from-linux-host-ip"></a>Acceso a aplicaciones de red de Windows desde Linux (dirección IP del host)

Si quieres acceder a una aplicación de red que se ejecuta en Windows (por ejemplo, una aplicación que se ejecuta en NodeJS o SQL Server) desde tu distribución de Linux (por ejemplo, Ubuntu), debes usar la dirección IP de la máquina host. Aunque no se trata de un escenario común, puedes seguir estos pasos para que funcione.
    - Para obtener la dirección IP de la máquina host, ejecuta este comando desde la distribución de Linux: `cat /etc/resolv.conf`
    - Copia la dirección IP que sigue al término: `nameserver`.
    - Conéctate a cualquier servidor de Windows con la dirección IP copiada.

La imagen siguiente muestra un ejemplo con la conexión a un servidor de Node.js que se ejecuta en Windows a través de curl.

![Conexión al servidor de NodeJS en Windows a través de cURL](media/wsl2-network-l2w.png)

### <a name="additional-networking-considerations"></a>Consideraciones adicionales sobre redes

#### <a name="connecting-via-remote-ip-addresses"></a>Conexión a través de direcciones IP remotas

Si se usan direcciones IP remotas para conectarse a las aplicaciones, estas se tratarán como conexiones desde la red de área local (LAN). Esto significa que tendrás que asegurarte de que la aplicación puede aceptar conexiones LAN.

Por ejemplo, es posible que tengas que enlazar la aplicación a `0.0.0.0` en lugar de a `127.0.0.1`. En el ejemplo de una aplicación de Python que usa Flask, esto se puede hacer con el comando `app.run(host='0.0.0.0')`. Ten en cuenta la seguridad al hacer estos cambios, ya que se permitirán las conexiones desde la LAN.

#### <a name="accessing-a-wsl-2-distribution-from-your-local-area-network-lan"></a>Acceso a la distribución de WSL 2 desde la red de área local (LAN)

Al usar una distribución de WSL 1, si el equipo está configurado para ser accesible desde la LAN, también se podrá acceder a las aplicaciones que se ejecuten en WSL en la LAN.

Esto no ocurre de forma predeterminada en WSL 2. WSL 2 tiene un adaptador Ethernet virtualizado con su propia dirección IP única. Actualmente, para habilitar este flujo de trabajo, tendrás que seguir los mismos pasos que para una máquina virtual normal. (Estamos buscando maneras de mejorar esta experiencia).

Este es un ejemplo de un comando de PowerShell para agregar un proxy de puerto que realiza escuchas en el puerto 4000 del host y lo conecta al puerto 4000 de la máquina virtual WSL 2 con la dirección IP 192.168.101.100.

```powershell
netsh interface portproxy add v4tov4 listenport=4000 listenaddress=0.0.0.0 connectport=4000 connectaddress=192.168.101.100
```

#### <a name="ipv6-access"></a>Acceso IPv6

Actualmente, las distribuciones de WSL 2 no pueden acceder a direcciones solo de IPv6. Estamos trabajando para agregar esta característica.

## <a name="expanding-the-size-of-your-wsl-2-virtual-hardware-disk"></a>Ampliación del tamaño del disco de hardware virtual de WSL 2

WSL 2 usa un disco de hardware virtual (VHD) para almacenar los archivos de Linux. Si alcanzas su tamaño máximo, puede que tengas que expandirlo.

El VHD de WSL 2 usa el sistema de archivos ext4. Este VHD cambia de tamaño automáticamente para satisfacer tus necesidades de almacenamiento y tiene un tamaño máximo inicial de 256 GB. Si tu distribución aumenta de tamaño y supera los 256 GB, verás errores que indicarán que se ha agotado el espacio en disco. Para corregir estos errores, puedes ampliar el tamaño del VHD.

Para ampliar el tamaño máximo del VHD más allá de 256 GB:

1. Finaliza todas las instancias de WSL mediante el comando `wsl --shutdown`.

2. Busca el nombre del paquete de instalación de la distribución ("PackageFamilyName").
    - En PowerShell (en que "distro" es el nombre de tu distribución), escribe el comando siguiente:
    - `Get-AppxPackage -Name "*<distro>*" | Select PackageFamilyName`

3. Busca el archivo VHD `fullpath` que se usa en tu instalación de WSL 2, que será tu valor de `pathToVHD`:
     - `%LOCALAPPDATA%\Packages\<PackageFamilyName>\LocalState\<disk>.vhdx`

4. Cambia el tamaño del VHD de WSL 2 mediante los comandos siguientes:
   - Abre el símbolo del sistema de Windows con privilegios de administrador y escribe:
      - `diskpart`
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`

5. Inicia la distribución de WSL (Ubuntu, por ejemplo).

6. Para indicar a WSL que puede expandir el tamaño del sistema de archivos, ejecuta estos comandos desde la línea de comandos de tu distribución de Linux:
    - `sudo mount -t devtmpfs none /dev`
    - `mount | grep ext4`
    - Copia el nombre de esta entrada, que tendrá el siguiente aspecto: `/dev/sdXX` (en que la X representa cualquier otro carácter).
    - `sudo resize2fs /dev/sdXX`
    - Usa el valor que copiaste antes. También puede que necesites instalar resize2fs: `apt install resize2fs`

> [!NOTE]
> En general, no debes modificar ni mover los archivos relacionados con WSL ubicados en la carpeta AppData mediante herramientas o editores de Windows. Tampoco tienes que acceder a estos archivos. Al hacerlo, podrías dañar tu distribución de Linux.
