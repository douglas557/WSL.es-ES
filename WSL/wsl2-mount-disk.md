---
title: Introducción al montaje de un disco de Linux en WSL 2 (versión preliminar)
description: Obtenga información sobre cómo configurar un montaje de disco en WSL 2 y cómo obtener acceso a él.
keywords: WSL, Windows, windowssubsystem, GNU, Linux, bash, Disk, ext4, filesystem, Mount
ms.date: 06/08/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: 8c67b0f34dcde925bb91979e9153049fdd474db3
ms.sourcegitcommit: dee2bf22c0c9f5725122a155d2876fcb2b7427d0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "92211739"
---
# <a name="get-started-mounting-a-linux-disk-in-wsl-2-preview"></a>Introducción al montaje de un disco de Linux en WSL 2 (versión preliminar)

Si desea tener acceso a un formato de disco de Linux que no es compatible con Windows, puede usar WSL 2 para montar el disco y acceder a su contenido.

En este tutorial se explican los pasos para identificar el disco y la partición que se van a adjuntar a WSL2, cómo montarlos y cómo obtener acceso a ellos.

> [!NOTE]
> Se requiere acceso de administrador para conectar un disco a WSL 2.

## <a name="identify-the-disk"></a>Identificar el disco

Para enumerar los discos disponibles en Windows, ejecute:

```powershell
wmic diskdrive list brief
```

Las rutas de acceso de los discos están disponibles en las columnas ' DeviceID '. Normalmente en el `\\.\PHYSICALDRIVE*` formato.

## <a name="list-and-select-the-partitions-to-mount-in-wsl-2"></a>Lista y selección de las particiones que se van a montar en WSL 2

Una vez que se identifica el disco, ejecute:

```powershell
wsl --mount <DiskPath> --bare
```

Esto hará que el disco esté disponible en WSL 2.

Una vez conectado, la partición se puede enumerar mediante la ejecución del siguiente comando en WSL 2:

```powershell
lsblk
```

Se mostrarán los dispositivos de bloque y sus particiones disponibles.

En Linux, un dispositivo de bloque se identifica como  `/dev/<Device><Partition>` . Por ejemplo,/dev/sdb3, es la partición número 3 del disco `sdb` .

Salida de ejemplo:

```powershell
NAME   MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
sdb      8:16   0    1G  0 disk
├─sdb2   8:18   0   50M  0 part
├─sdb3   8:19   0  873M  0 part
└─sdb1   8:17   0  100M  0 part
sdc      8:32   0  256G  0 disk /
sda      8:0    0  256G  0 disk
```

## <a name="identifying-the-filesystem-type"></a>Identificación del tipo de sistema de archivos

Si no conoce el tipo de sistema de archivos de un disco o una partición, puede usar este comando:

```powershell
blkid <BlockDevice>
```

Se generará el tipo de sistema de archivos detectado (con el `TYPE="<Filesystem>"` formato).

## <a name="mount-the-selected-partitions"></a>Montar las particiones seleccionadas

Una vez que haya identificado las particiones que desea montar, ejecute este comando en cada partición: 

```powershell
wsl --mount <DiskPath> --partition <PartitionNumber> --type <Filesystem>
```

> [!NOTE]
> Si desea montar todo el disco como un solo volumen (es decir, si el disco no tiene particiones), `--partition` se puede omitir.
> 
> Si se omite, el tipo de sistema de archivos predeterminado es "ext4".

## <a name="access-the-disk-content"></a>Acceder al contenido del disco

Una vez montado, se puede acceder al disco bajo la ruta de acceso indicada por el valor de configuración: `automount.root` . El valor predeterminado es `/mnt/wsl`.

Desde Windows, se puede tener acceso al disco desde el explorador de archivos. para ello, vaya a: `\\wsl$\\<Distro>\\<Mountpoint>` (Seleccione cualquier distribución de Linux).

## <a name="unmount-the-disk"></a>Desmontaje de los discos

Si desea desmontar y desasociar el disco de WSL 2, ejecute:

```powershell
wsl --unmount <DiskPath>
```

## <a name="command-line-reference"></a>Referencia de línea de comandos

### <a name="mouting-a-specific-filesystem"></a>Mouting un sistema de archivos específico

De forma predeterminada, WSL 2 intentará montar el dispositivo como ext4. Para especificar otro sistema de archivos, ejecute:

```powershell
wsl --mount <DiskPath> -t <FileSystem>
```

Por ejemplo, para montar un disco como FAT, ejecute:

```
wsl --mount <Diskpath> -t vfat
```

> [!NOTE]
> Para enumerar los sistemas de archivos disponibles en WSL2, ejecute: `cat /proc/filesystems`

### <a name="mouting-a-specific-partition"></a>Mouting una partición específica

De forma predeterminada, WSL 2 intenta montar todo el disco. Para montar una partición específica, ejecute:

```
wsl --mount <Diskpath> -p <PartitionIndex>
```

Esto solo funciona si el disco es MBR (registro de arranque maestro) o GPT (tabla de particiones GUID). [Lea acerca de los estilos de partición: MBR y GPT](/windows-server/storage/disk-management/initialize-new-disks#about-partition-styles---gpt-and-mbr).

### <a name="specifying-mount-options"></a>Especificar opciones de montaje

Para especificar las opciones de montaje, ejecute:

```powershell
wsl --mount <DiskPath> -o <MountOptions>
```

Ejemplo:

```powershell
wsl --mount <DiskPath> -o "data=ordered"
```

> [!NOTE]
> En este momento solo se admiten las opciones específicas del sistema de archivos. `ro, rw, noatime, ...`No se admiten opciones genéricas como.

### <a name="attaching-the-disk-without-mounting-it"></a>Conexión del disco sin montarlo

Si el esquema de disco no es compatible con ninguna de las opciones anteriores, puede adjuntar el disco a WSL 2 sin montarlo mediante la ejecución de:

```powershell
wsl --mount <DiskPath> --bare
```

Esto hará que el dispositivo de bloque esté disponible dentro de WSL 2, por lo que se puede montar manualmente desde allí. Use `lsblk` para enumerar los dispositivos de bloque disponibles dentro de WSL 2.

### <a name="detaching-a-disk"></a>Desconexión de un disco

Para desasociar un disco de WSL 2, ejecute:

```powershell
wsl --unmount [DiskPath]
```

Si `Diskpath` se omite, todos los discos conectados se desmontan y se desasocian.

> [!NOTE]
> Si se produce un error al desmontar un disco, se puede forzar la salida de WSL 2 mediante `wsl --shutdown` la ejecución de, que desasociará el disco.

## <a name="limitations"></a>Limitaciones

- En este momento, solo se pueden adjuntar discos completos a WSL 2, lo que significa que no es posible adjuntar solo una partición. Concretamente, esto significa que no es posible usar `wsl --mount` para leer una partición en el dispositivo de arranque, porque ese dispositivo no se puede desasociar de Windows.

- Las unidades flash USB no se admiten en este momento y no se pueden asociar a WSL 2. No obstante, se admiten discos USB.

- Solo los sistemas de archivos que se admiten de forma nativa en el kernel se pueden montar con `wsl --mount` . Esto significa que no es posible usar controladores de sistema de archivos instalados (por ejemplo, NTFS-3G) mediante una llamada a `wsl --mount` .
