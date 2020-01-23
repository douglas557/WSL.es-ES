---
title: Cambios de la experiencia de usuario entre WSL 1 y WSL 2
description: Cambios de experiencia del usuario entre WSL 1 y WSL 2
keywords: BashOnWindows, bash, WSL, wsl2, Windows, subsistema de Windows para Linux, windowssubsystem, Ubuntu, Debian, SuSE, Windows 10
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: a8f298a69acf44f152da626a0ba571f6bba1970c
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520564"
---
# <a name="user-experience-changes-between-wsl-1-and-wsl-2"></a>Cambios de experiencia del usuario entre WSL 1 y WSL 2

Esta página supera las diferencias de experiencia del usuario entre WSL 1 y WSL 2 Preview. Los cambios clave que se deben tener en cuenta son:

- Coloque los archivos a los que tendrán acceso las aplicaciones de Linux en el sistema de archivos raíz de Linux para agilizar la velocidad de rendimiento de los archivos
- En las compilaciones iniciales de la versión preliminar de WSL 2, tendrá que acceder a las aplicaciones de red mediante una dirección IP y no usar localhost

Y a continuación se muestra la lista completa de otros cambios que puede observar:

- WSL 2 usa un [disco de hardware virtual](https://en.wikipedia.org/wiki/VHD_(file_format)) (VHD) para almacenar los archivos y, si alcanza su tamaño máximo, puede que tenga que expandirlo
- Al iniciarse, WSL 2 usará ahora una pequeña proporción de memoria.
- La velocidad de acceso a archivos entre so será más lenta en las compilaciones de vista previa inicial

## <a name="place-your-linux-files-in-your-linux-root-file-system"></a>Coloque los archivos de Linux en el sistema de archivos raíz de Linux
Asegúrese de colocar los archivos a los que va a acceder con frecuencia con las aplicaciones de Linux dentro del sistema de archivos raíz de Linux para disfrutar de las ventajas de rendimiento de los archivos. Estos archivos deben estar dentro del sistema de archivos raíz de Linux para tener un acceso más rápido al sistema de archivos. También hemos hecho posible que las aplicaciones de Windows tengan acceso al sistema de archivos raíz de Linux (como el explorador de archivos). Intente ejecutar: `explorer.exe .` en el directorio particular de su distribución de Linux y ver lo que sucede), lo que hará que esta transición sea mucho más fácil. 

## <a name="accessing-network-applications"></a>Acceso a aplicaciones de red
En las compilaciones iniciales de la versión preliminar de WSL 2, tendrá que acceder a cualquier servidor de Windows desde Linux mediante la dirección IP del equipo host.

### <a name="accessing-windows-applications-from-linux"></a>Acceso a aplicaciones Windows desde Linux
Para tener acceso a una aplicación de red de Windows, deberá usar la dirección IP del equipo host. Puede hacerlo con estos pasos:

- Para obtener la dirección IP de la máquina host, ejecute el comando `cat /etc/resolv.conf` y copie la dirección IP que sigue al término `nameserver`. 
- Conéctese a cualquier servidor de Windows mediante la dirección IP copiada.

En la imagen siguiente se muestra un ejemplo de esto mediante la conexión a un servidor node. js que se ejecuta en Windows a través de cURL. 

![Acceso a aplicaciones de red Linux desde Windows](media/wsl2-network-l2w.png)

### <a name="accessing-linux-applications-from-windows"></a>Acceder a las aplicaciones de Linux desde Windows

En función de la versión de Windows que use, es posible que necesite recuperar la dirección IP de la máquina virtual. Si la compilación es 18945 o una versión posterior, puede usar `localhost` como normal. 

#### <a name="accessing-linux-on-builds-lower-than-18945httpsblogswindowscomwindowsexperience20190726announcing-windows-10-insider-preview-build-18945"></a>Acceder a Linux en compilaciones inferiores a [18945](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/)

Si tiene un servidor en un distribución de WSL, debe buscar la dirección IP de la máquina virtual que enciende su distribución y conectarse a él con esa dirección IP. Para ello, siga estos pasos:

- Obtenga la dirección IP de su distribución ejecutando el comando `ip addr` dentro de la distribución de WSL y buscándola en el valor `inet` de la interfaz `eth0`.
   - Puede buscarlo más fácilmente si filtra la salida del comando mediante grep, como por ejemplo: `ip addr | grep eth0`.
- Conéctese al servidor Linux mediante la dirección IP que ha encontrado anteriormente.

En la imagen siguiente se muestra un ejemplo de esto mediante la conexión a un servidor node. js con el explorador Edge.

![Acceso a aplicaciones de red Linux desde Windows](media/wsl2-network-w2l.jpg)

### <a name="other-networking-considerations"></a>Otras consideraciones sobre redes

#### <a name="connecting-via-remote-ip-addresses"></a>Conexión a través de direcciones IP remotas

Cuando se usan direcciones IP remotas para conectarse a las aplicaciones, se tratarán como conexiones desde la red de área local (LAN). Esto significa que debe asegurarse de que la aplicación puede aceptar conexiones LAN, es decir, es posible que deba enlazar la aplicación a `0.0.0.0` en lugar de `127.0.0.1`. Por ejemplo, en Python con el frasco, esto se puede hacer con el comando: `app.run(host='0.0.0.0')`. Tenga en cuenta la seguridad al realizar estos cambios, ya que esto permitirá las conexiones desde la LAN. 

#### <a name="accessing-a-wsl2-distro-from-your-local-area-network-lan"></a>Acceso a WSL2 distribución desde la red de área local (LAN)

Cuando se usa un distribución de WSL1, si se configuró el equipo para que sea accesible a través de la LAN, también se puede acceder a las aplicaciones que se ejecutan en WSL en la LAN. Este no es el caso predeterminado en WSL2, ya que WSL2 tiene un adaptador Ethernet virtualizado con su propia dirección IP. Actualmente, para habilitar este flujo de trabajo, tendrá que seguir los mismos pasos que para una máquina virtual normal. Estamos buscando formas de mejorar esta experiencia.

#### <a name="ipv6-access"></a>Acceso IPv6

WSL2 distribuciones actualmente no puede acceder a direcciones solo IPv6. Estamos trabajando para agregar esta característica.

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a>Entender WSL 2 usa un disco duro virtual y qué hacer si alcanza su tamaño máximo
WSL 2 almacena todos los archivos de Linux en un disco duro virtual que usa el sistema de archivos ext4. Este disco duro virtual cambia de tamaño automáticamente para satisfacer sus necesidades de almacenamiento. Este VHD también tiene un tamaño máximo inicial de 256 GB. Si el distribución aumenta de tamaño para que sea mayor que 256 GB, verá errores que indican que se ha agotado el espacio en disco. Puede corregirlos expandiendo el tamaño del disco duro virtual. A continuación se proporcionan instrucciones sobre cómo hacerlo:

1. Finalizar todas las instancias de WSL mediante el comando `wsl --shutdown`
2. Busque el nombre del paquete de instalación de distribución ' PackageFamilyName '
   - En un símbolo del sistema de PowerShell (donde "distribución" es el nombre de distribución), escriba:
      - `Get-AppxPackage -Name "*<distro>*" | Select PackageFamilyName`
3. Busque el archivo VHD FullPath usado por la instalación de WSL 2, que será su ' pathToVHD ':
     - `%LOCALAPPDATA%\Packages\<PackageFamilyName>\LocalState\<disk>.vhdx`
4. Cambie el tamaño del disco duro virtual de WSL 2; para ello, complete los siguientes comandos
   - Abra una ventana del símbolo del sistema con privilegios de administrador y ejecute los siguientes comandos:
      - `diskpart`
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`
5. Inicie WSL distribución
6. Hacer que WSL tenga en cuenta que puede expandir el tamaño del sistema de archivos
   - Ejecute estos comandos en el WSL distribución:
      - `sudo mount -t devtmpfs none /dev`
      - `mount | grep ext4`
         - Copie el nombre de esta entrada, que tendrá el siguiente aspecto:/dev/sdXX (con la X que representa cualquier otro carácter)
      - `sudo resize2fs /dev/sdXX`
         - Asegúrese de usar el valor que copió anteriormente y puede que tenga que usar: `apt install resize2fs`.

Tenga en cuenta que, en general, no modifique, mueva ni acceda a los archivos relacionados con WSL ubicados dentro de la carpeta AppData mediante herramientas o editores de Windows. Esto podría hacer que el distribución de Linux esté dañado.

## <a name="wsl-2-will-use-some-memory-on-startup"></a>WSL 2 usará memoria en el inicio
WSL 2 usa una máquina virtual de utilidad ligera en un kernel de Linux real para ofrecer un rendimiento de sistema de archivos excelente y una compatibilidad completa con llamadas al sistema, al tiempo que sigue siendo tan ligero, rápido, integrado y con capacidad de respuesta como WSL 1. Esta máquina virtual tiene una superficie de memoria pequeña y asignará memoria reservada de direcciones virtuales en el inicio. Está configurado para empezar con una pequeña proporción de la memoria total.

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a>La velocidad del archivo Cross OS será más lenta en las compilaciones de vista previa inicial
Observará velocidades de archivo más lentas en comparación con WSL 1 al acceder a archivos de Windows desde una aplicación de Linux o a archivos de Linux desde una aplicación de Windows. Esto se debe a los cambios arquitectónicos en WSL 2 y es algo que el equipo de WSL está investigando activamente cómo podemos mejorar esta experiencia.
