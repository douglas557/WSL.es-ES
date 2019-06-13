---
title: Cambios de la experiencia de usuario entre WSL 1 y 2 de WSL
description: Cambios de la experiencia de usuario entre WSL 1 y 2 de WSL
keywords: BashOnWindows, bash, wsl, wsl2, windows, el subsistema de windows para linux, windowssubsystem, ubuntu, debian, suse, windows 10
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 0660f9f726811008685de9f1ff457e7515add67a
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038105"
---
# <a name="user-experience-changes-between-wsl-1-and-wsl-2"></a>Cambios de la experiencia de usuario entre WSL 1 y 2 de WSL

Esta página se va a través de las diferencias de experiencia de usuario entre el 1 de WSL y la versión preliminar de WSL 2. Los cambios clave a tener en cuenta son:

- Coloque los archivos que tendrá acceso las aplicaciones de Linux en el sistema de archivos raíz de Linux para mayor velocidad de rendimiento de archivo
- En compilaciones iniciales de preview 2 WSL deberá tener acceso a aplicaciones de red mediante una dirección IP y no usa localhost

Y, a continuación es la lista completa de otros cambios que es posible que tenga en cuenta:

- WSL 2 usa un disco duro virtual para almacenar los archivos y si alcanza su tamaño máximo es posible que necesite expandirlo
- Cuando se inicia, WSL 2, ahora se usarán una pequeña proporción de memoria
- Entre el sistema operativo, velocidad de acceso del archivo será más lento en las compilaciones de versión preliminar inicial

## <a name="place-your-linux-files-in-your-linux-root-file-system"></a>Ponga los archivos de Linux en el sistema de archivos de la raíz de Linux
Asegúrese de que los archivos que se accederá a menudo con Linux aplicaciones dentro de su Linux raíz del sistema de archivos para disfrutar de las ventajas de rendimiento de archivo. Estos archivos deben estar en el sistema de archivos raíz de Linux para tener acceso al sistema de archivos más rápido. También hemos realizado lo posible para las aplicaciones de Windows tener acceso al sistema de archivos de Linux raíz (por ejemplo, el Explorador de archivos. Intente ejecutar: `explorer.exe /` en el shell de bash y vea lo que ocurre) que facilitarán esta transición significativamente. 

## <a name="accessing-network-applications"></a>Obtener acceso a aplicaciones de red
En las compilaciones iniciales de la versión preliminar de WSL 2, necesita tener acceso a cualquier servidor Linux desde Windows con la dirección IP de la distribución de Linux y cualquier servidor de Windows de Linux con la dirección IP de la máquina host. Esto es algo que es temporal y muy alto en nuestra lista de prioridad para corregir.

### <a name="accessing-linux-applications-from-windows"></a>Acceso a las aplicaciones de Linux desde Windows
Si tiene un servidor en una distribución de WSL, deberá encontrar la dirección IP de la máquina virtual fortalecer su distribución y conectarse a ella con esa dirección IP. Puede hacerlo siguiendo estos pasos:

- Obtener la dirección IP de su distribución, ejecute el comando `ip addr` dentro de la distribución WSL y buscar en el `inet` valor de la `eth0` interfaz.
   - Puede encontrarlo más fácilmente mediante el filtrado de la salida del comando con grep así: `ip addr | grep eth0`.
- Conéctese a su servidor Linux con la dirección IP que se encuentra por encima.

La siguiente imagen muestra un ejemplo de esto mediante la conexión a un servidor de nodeJS con el explorador Microsoft Edge.

![Acceso a aplicaciones de red de Linux desde Windows](media/wsl2-network-w2l.jpg)

### <a name="accessing-windows-applications-from-linux"></a>Obtener acceso a aplicaciones de Windows de Linux
Para obtener acceso a una aplicación de red de Windows, deberá usar la dirección IP de la máquina host. Puede hacerlo con estos pasos:

- Obtener la dirección IP de su equipo host, ejecute el comando `cat /etc/resolv.conf` y copiar la dirección IP siguiendo el término `nameserver`. 
- Conectarse a cualquier servidor de Windows con la dirección IP copiada.

La siguiente imagen muestra un ejemplo de esto mediante la conexión a un servidor de python que se ejecuta en Windows mediante curl. 

![Acceso a aplicaciones de red de Linux desde Windows](media/wsl2-network-l2w.png)

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a>Descripción de WSL 2 usa un disco duro virtual y qué hacer si se alcanza su tamaño máximo
2 de WSL almacena todos los archivos de Linux dentro de un disco duro virtual que usa el sistema de archivos ext4. Este disco duro virtual cambia automáticamente de tamaño para satisfacer las necesidades de almacenamiento. Este disco duro virtual también tiene un tamaño inicial máximo de 256GB. Si la distribución aumenta de tamaño es superior a 256GB, verá errores que indica que se ha quedado espacio en disco. Puede corregir estos expandiendo el tamaño de disco duro virtual. Instrucciones sobre cómo hacerlo son los siguientes:

1. Finalizar todas las instancias WSL utilizando el `wsl --shutdown` comando
2. Cambiar el tamaño de su disco duro virtual de WSL 2 completando los siguientes comandos
   - Abra una ventana de línea de comandos con privilegios de administrador y ejecute los siguientes comandos:
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`
3. Inicie la distribución WSL
4. Asegúrese de WSL, tenga en cuenta que puede expandir el tamaño de su sistema de archivos
   - Ejecute estos comandos en la distribución WSL:
      - `sudo mount -t devtmpfs none /dev`
      - `mount | grep ext4`
         - Copie el nombre de esta entrada, que tendrá el siguiente aspecto: / dev/sdXX (con la X que representa cualquier otro carácter)
      - `sudo resize2fs /dev/sdXX`
         - Asegúrese de utilizar el valor que copió anteriormente y es posible que deba usar: `apt install resize2fs`.

## <a name="wsl-2-will-use-some-memory-on-startup"></a>2 de WSL utilizará algo de memoria al inicio
WSL 2 utiliza una utilidad ligera de máquina virtual en un kernel de Linux real para proporcionar el rendimiento del sistema de archivos de gran y completa sistema llamada compatibilidad mientras sigue siendo igual que la luz, rápidas y integrado y capacidad de respuesta que WSL 1. Esta utilidad de la máquina virtual tiene una superficie de memoria pequeña y asignará memoria de direcciones virtuales de seguridad en el inicio. Se está configurado para iniciarse con una pequeña proporción de la memoria total.

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a>Entre el sistema operativo, velocidad del archivo será más lento en las compilaciones de versión preliminar inicial
Observará velocidades de archivo más lentas en comparación con 1 WSL al tener acceso a los archivos de Windows desde una aplicación de Linux, o tener acceso a archivos de Linux desde una aplicación de Windows. Este es el resultado de los cambios de arquitectura en WSL 2 y es algo que el equipo de WSL activamente se investiga sobre cómo podemos mejorar esta experiencia.