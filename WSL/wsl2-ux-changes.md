---
title: Cambios en la experiencia de usuario entre WSL 1 y WSL 2
description: Cambios en la experiencia de usuario entre WSL 1 y WSL 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, subsistema de windows para linux, subsistemawindows, ubuntu, debian, suse, windows 10
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: a8f298a69acf44f152da626a0ba571f6bba1970c
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520564"
---
# <a name="user-experience-changes-between-wsl-1-and-wsl-2"></a>Cambios en la experiencia de usuario entre WSL 1 y WSL 2

En esta página se explican las diferencias en la experiencia de usuario entre WSL 1 y la versión preliminar de WSL 2. Los principales cambios a tener en cuenta son:

- Deberás colocar los archivos a los que accederán tus aplicaciones de Linux en el sistema de archivos raíz de Linux para acelerar el rendimiento de los archivos.
- En las compilaciones iniciales de la versión preliminar de WSL 2, deberás acceder a las aplicaciones de red mediante una dirección IP y no a través de localhost.

A continuación se muestra la lista completa de los demás cambios que podrás observar:

- WSL 2 usa un [disco de hardware virtual](https://en.wikipedia.org/wiki/VHD_(file_format)) (VHD) para almacenar los archivos y, si alcanzas su tamaño máximo, puede que tengas que expandirlo.
- Al iniciarse, WSL 2 ahora usará una pequeña proporción de memoria.
- La velocidad de acceso a archivos entre sistemas operativos será más lenta en las compilaciones iniciales de la versión preliminar.

## <a name="place-your-linux-files-in-your-linux-root-file-system"></a>Colocación de los archivos de Linux en el sistema de archivos raíz de Linux
Asegúrate de colocar los archivos a los que accederás con frecuencia con las aplicaciones de Linux dentro del sistema de archivos raíz de Linux para disfrutar de las ventajas de rendimiento de los archivos. Estos archivos deben estar dentro del sistema de archivos raíz de Linux para acelerar el acceso al sistema de archivos. También hemos hecho posible que las aplicaciones de Windows tengan acceso al sistema de archivos raíz de Linux (como el Explorador de archivos. Intenta ejecutar `explorer.exe .` en el directorio de inicio de tu distribución de Linux y observa lo que sucede), lo que hará que esta transición sea mucho más fácil. 

## <a name="accessing-network-applications"></a>Acceso a aplicaciones de red
En las compilaciones iniciales de la versión preliminar de WSL 2, tendrás que acceder a cualquier servidor de Windows desde Linux mediante la dirección IP del equipo host.

### <a name="accessing-windows-applications-from-linux"></a>Acceso a aplicaciones de Windows desde Linux
Para acceder a una aplicación de red de Windows, deberás usar la dirección IP del equipo host. También puedes hacerlo con el procedimiento siguiente:

- Ejecuta el comando `cat /etc/resolv.conf` y copia la dirección IP que sigue al término `nameserver` para obtener la dirección IP del equipo host. 
- Conéctate a cualquier servidor de Windows con la dirección IP copiada.

La imagen siguiente muestra un ejemplo con la conexión a un servidor de Node.js que se ejecuta en Windows a través de curl. 

![Acceso a aplicaciones de red de Linux desde Windows](media/wsl2-network-l2w.png)

### <a name="accessing-linux-applications-from-windows"></a>Acceso a aplicaciones de Linux desde Windows

En función de la versión de Windows que utilices, es posible que tengas que recuperar la dirección IP de la máquina virtual. Si tienes la compilación 18945 o posterior, puedes usar `localhost` del modo habitual. 

#### <a name="accessing-linux-on-builds-lower-than-18945"></a>Acceso a Linux en compilaciones anteriores a [18945](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/)

Si tienes un servidor en una distribución de WSL, deberás encontrar la dirección IP de la máquina virtual que habilita la distribución y conectarla a esta con esa dirección IP. Para hacerlo, sigue estos pasos:

- Para obtener la dirección IP de la distribución, ejecuta el comando `ip addr` en tu distribución de WSL y búscala bajo el valor `inet` de la interfaz `eth0`.
   - Para encontrarla más fácilmente, filtra la salida del comando con grep, como se muestra a continuación: `ip addr | grep eth0`.
- Conéctate al servidor de Linux con la IP que has encontrado.

La imagen siguiente muestra un ejemplo con la conexión a un servidor de Node.js mediante el navegador Edge.

![Acceso a aplicaciones de red de Linux desde Windows](media/wsl2-network-w2l.jpg)

### <a name="other-networking-considerations"></a>Otras consideraciones sobre redes

#### <a name="connecting-via-remote-ip-addresses"></a>Conexión a través de direcciones IP remotas

Si se usan direcciones IP remotas para conectarse a las aplicaciones, estas se tratarán como conexiones desde la red de área local (LAN). Esto significa que tendrás que asegurarte de que la aplicación puede aceptar conexiones LAN, es decir: Es posible que debas enlazar la aplicación a `0.0.0.0` en lugar de a `127.0.0.1`. Por ejemplo, en Python con Flask, esto se puede hacer con el comando: `app.run(host='0.0.0.0')`. Ten en cuenta la seguridad al realizar estos cambios, ya que se permitirán las conexiones desde la LAN. 

#### <a name="accessing-a-wsl2-distro-from-your-local-area-network-lan"></a>Acceso a la distribución de WSL 2 desde la red de área local (LAN)

Cuando se usa un distribución de WSL 1, si el equipo está configurado para ser accesible desde la LAN, también se podrá acceder a las aplicaciones que se ejecuten en WSL en la LAN. Este no es el caso predeterminado en WSL 2, ya que WSL 2 tiene un adaptador Ethernet virtualizado que es su propia dirección IP. Actualmente, para habilitar este flujo de trabajo, tendrás que seguir los mismos pasos que para una máquina virtual normal. Estamos buscando maneras de mejorar esta experiencia.

#### <a name="ipv6-access"></a>Acceso IPv6

Actualmente, las distribuciones de WSL 2 no pueden acceder a direcciones solo IPv6. Estamos trabajando para agregar esta característica.

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a>Descripción del uso de un disco VHD por parte de WSL 2 y procedimiento en caso de alcanzar su tamaño máximo
WSL 2 almacena todos los archivos de Linux en un disco VHD que usa el sistema de archivos ext4. Este disco VHD cambia de tamaño automáticamente para satisfacer las necesidades de almacenamiento. Este disco VHD también tiene un tamaño máximo inicial de 256 GB. Si tu distribución aumenta de tamaño y supera los 256 GB, verás errores que indican que se ha agotado el espacio en disco. Para corregirlos puedes ampliar el tamaño del disco VHD. Las instrucciones sobre cómo hacerlo son las siguientes:

1. Finaliza todas las instancias de WSL mediante el comando `wsl --shutdown`.
2. Busca el nombre del paquete de instalación de la distribución "PackageFamilyName".
   - En un símbolo del sistema de PowerShell (donde "distro" es el nombre de tu distribución), escribe:
      - `Get-AppxPackage -Name "*<distro>*" | Select PackageFamilyName`
3. Busca la ruta de acceso completa del archivo VHD que se usa en tu instalación de WSL 2, que será tu "pathToVHD":
     - `%LOCALAPPDATA%\Packages\<PackageFamilyName>\LocalState\<disk>.vhdx`
4. Cambia el tamaño del disco VHD de WSL 2 mediante los comandos siguientes.
   - Abre una ventana del símbolo del sistema con privilegios de administrador y ejecuta el siguiente comando:
      - `diskpart`
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`
5. Inicia la distribución de WSL
6. Indica a WSL que puede expandir el tamaño del sistema de archivos.
   - Ejecuta estos comandos en la distribución de WSL:
      - `sudo mount -t devtmpfs none /dev`
      - `mount | grep ext4`
         - Copia el nombre de esta entrada, que tendrá el siguiente aspecto: /dev/sdXX (donde la X representa cualquier otro carácter).
      - `sudo resize2fs /dev/sdXX`
         - Asegúrate de usar el valor que copiaste anteriormente. Es posible que tengas que usar: `apt install resize2fs`.

Ten en cuenta lo siguiente: En general, no debes modificar ni mover los archivos relacionados con WSL ubicados en la carpeta AppData mediante herramientas o editores de Windows. Tampoco tienes que acceder a estos archivos. Al hacerlo, podrías dañar la distribución de Linux.

## <a name="wsl-2-will-use-some-memory-on-startup"></a>WSL 2 usará algo de memoria al iniciarse
WSL 2 usa una VM de utilidad ligera en un kernel de Linux real para ofrecer un excelente rendimiento del sistema de archivos y una compatibilidad completa con las llamadas del sistema, al tiempo que sigue siendo tan ligero, rápido, integrado y dinámico como WSL 1. Esta VM de utilidad tiene una superficie de memoria pequeña y asignará memoria reservada de direcciones virtuales al iniciarse. Está configurada para empezar con una pequeña proporción de la memoria total.

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a>La velocidad de acceso a archivos entre sistemas operativos será más lenta en las compilaciones iniciales de la versión preliminar
Observará velocidades de archivo más lentas en comparación con WSL 1 al acceder a archivos de Windows desde una aplicación de Linux o a archivos de Linux desde una aplicación de Windows. Esto se debe a los cambios en la arquitectura de WSL 2 y es algo que el equipo de WSL está investigando activamente para mejorar esta experiencia.
