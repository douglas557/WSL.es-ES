---
title: Cambios de la experiencia de usuario entre WSL 1 y WSL 2
description: Cambios de experiencia del usuario entre WSL 1 y WSL 2
keywords: BashOnWindows, bash, WSL, wsl2, Windows, subsistema de Windows para Linux, windowssubsystem, Ubuntu, Debian, SuSE, Windows 10
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: a6c8f4fbbf21b4295e69fe3de2ecf0922ab20bbe
ms.sourcegitcommit: 6086126c35a5518a7110935fa13592b5ed9dd6b7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2019
ms.locfileid: "67891782"
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
Asegúrese de colocar los archivos a los que va a acceder con frecuencia con las aplicaciones de Linux dentro del sistema de archivos raíz de Linux para disfrutar de las ventajas de rendimiento de los archivos. Estos archivos deben estar dentro del sistema de archivos raíz de Linux para tener un acceso más rápido al sistema de archivos. También hemos hecho posible que las aplicaciones de Windows tengan acceso al sistema de archivos raíz de Linux (como el explorador de archivos). Pruebe a ejecutar `explorer.exe .` : en el directorio principal de su distribución de Linux y vea lo que sucede), lo que hará que esta transición sea mucho más fácil. 

## <a name="accessing-network-applications"></a>Acceso a aplicaciones de red
En las compilaciones iniciales de la versión preliminar de WSL 2, tendrá que acceder a cualquier servidor Linux desde Windows mediante la dirección IP de su distribución Linux y cualquier servidor Windows Server desde Linux mediante la dirección IP del equipo host. Esto es algo que es temporal y muy alto en nuestra lista de prioridades para corregirlo.

### <a name="accessing-linux-applications-from-windows"></a>Acceder a las aplicaciones de Linux desde Windows
Si tiene un servidor en un distribución de WSL, debe buscar la dirección IP de la máquina virtual que enciende su distribución y conectarse a él con esa dirección IP. Para ello, siga estos pasos:

- Para obtener la dirección IP de su distribución, ejecute el `ip addr` comando dentro de la distribución de WSL y busque en `inet` el valor de `eth0` la interfaz.
   - Puede buscarlo más fácilmente si filtra la salida del comando mediante grep como el siguiente: `ip addr | grep eth0`.
- Conéctese al servidor Linux mediante la dirección IP que ha encontrado anteriormente.

En la imagen siguiente se muestra un ejemplo de esto mediante la conexión a un servidor node. js con el explorador Edge.

![Acceso a aplicaciones de red Linux desde Windows](media/wsl2-network-w2l.jpg)

### <a name="accessing-windows-applications-from-linux"></a>Acceso a aplicaciones Windows desde Linux
Para tener acceso a una aplicación de red de Windows, deberá usar la dirección IP del equipo host. Puede hacerlo con estos pasos:

- Obtenga la dirección IP de la máquina host ejecutando el comando `cat /etc/resolv.conf` y copiando la dirección IP que sigue al término. `nameserver` 
- Conéctese a cualquier servidor de Windows mediante la dirección IP copiada.

En la imagen siguiente se muestra un ejemplo de esto mediante la conexión a un servidor node. js que se ejecuta en Windows a través de rizo. 

![Acceso a aplicaciones de red Linux desde Windows](media/wsl2-network-l2w.png)

### <a name="other-networking-considerations"></a>Otras consideraciones sobre redes

Cuando se usan direcciones IP remotas para conectarse a las aplicaciones, se tratarán como conexiones desde la red de área local (LAN). Esto significa que tendrá que asegurarse de que la aplicación puede aceptar conexiones LAN, es decir: Es posible que deba enlazar su aplicación `0.0.0.0` a en lugar `127.0.0.1`de a. Por ejemplo, en Python con el frasco, esto se puede hacer con `app.run(host='0.0.0.0')`el comando:. Tenga en cuenta la seguridad al realizar estos cambios, ya que esto permitirá las conexiones desde la LAN. 

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a>Entender WSL 2 usa un disco duro virtual y qué hacer si alcanza su tamaño máximo
WSL 2 almacena todos los archivos de Linux en un disco duro virtual que usa el sistema de archivos ext4. Este disco duro virtual cambia de tamaño automáticamente para satisfacer sus necesidades de almacenamiento. Este VHD también tiene un tamaño máximo inicial de 256 GB. Si el distribución aumenta de tamaño para que sea mayor que 256 GB, verá errores que indican que se ha agotado el espacio en disco. Puede corregirlos expandiendo el tamaño del disco duro virtual. A continuación se proporcionan instrucciones sobre cómo hacerlo:

1. Finalizar todas las instancias de WSL `wsl --shutdown` mediante el comando
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

Ten en cuenta que: En general, no modifique, mueva ni acceda a los archivos relacionados con WSL ubicados dentro de la carpeta AppData mediante herramientas o editores de Windows. Esto podría hacer que el distribución de Linux esté dañado.

## <a name="wsl-2-will-use-some-memory-on-startup"></a>WSL 2 usará memoria en el inicio
WSL 2 usa una máquina virtual de utilidad ligera en un kernel de Linux real para ofrecer un rendimiento de sistema de archivos excelente y una compatibilidad completa con llamadas al sistema, al tiempo que sigue siendo tan ligero, rápido, integrado y con capacidad de respuesta como WSL 1. Esta máquina virtual tiene una superficie de memoria pequeña y asignará memoria reservada de direcciones virtuales en el inicio. Está configurado para empezar con una pequeña proporción de la memoria total.

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a>La velocidad del archivo Cross OS será más lenta en las compilaciones de vista previa inicial
Observará velocidades de archivo más lentas en comparación con WSL 1 al acceder a archivos de Windows desde una aplicación de Linux o a archivos de Linux desde una aplicación de Windows. Esto se debe a los cambios arquitectónicos en WSL 2 y es algo que el equipo de WSL está investigando activamente cómo podemos mejorar esta experiencia.
