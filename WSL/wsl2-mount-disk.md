---
title: Introducción al montaje de un disco de Linux en WSL 2 (versión preliminar)
description: Obtenga información sobre cómo configurar un montaje de disco en WSL 2 y cómo obtener acceso a él.
keywords: WSL, Windows, windowssubsystem, GNU, Linux, bash, Disk, ext4, filesystem, Mount
ms.date: 06/08/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: 5ea7d7adae42a44b040408575e7345c456f3acac
ms.sourcegitcommit: b15b847b87d29a40de4a1517315949bce9c7a3d5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "91413286"
---
# <a name="get-started-mounting-a-linux-disk-in-wsl-2-preview"></a><span data-ttu-id="37b3b-104">Introducción al montaje de un disco de Linux en WSL 2 (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="37b3b-104">Get started mounting a linux disk in WSL 2 (preview)</span></span>

<span data-ttu-id="37b3b-105">Si desea tener acceso a un formato de disco de Linux que no es compatible con Windows, puede usar WSL 2 para montar el disco y acceder a su contenido.</span><span class="sxs-lookup"><span data-stu-id="37b3b-105">If you want to access a Linux disk format that isn't supported by Windows, you can use WSL 2 to mount your disk and access its content.</span></span>

<span data-ttu-id="37b3b-106">En este tutorial se explican los pasos para identificar el disco y la partición que se van a adjuntar a WSL2, cómo montarlos y cómo obtener acceso a ellos.</span><span class="sxs-lookup"><span data-stu-id="37b3b-106">This tutorial will cover the steps to identify the disk and partition to attach to WSL2, how to mount them, and how to access them.</span></span>

> [!NOTE]
> <span data-ttu-id="37b3b-107">Se requiere acceso de administrador para conectar un disco a WSL 2.</span><span class="sxs-lookup"><span data-stu-id="37b3b-107">Administrator access is required to attach a disk to WSL 2.</span></span>

## <a name="identify-the-disk"></a><span data-ttu-id="37b3b-108">Identificar el disco</span><span class="sxs-lookup"><span data-stu-id="37b3b-108">Identify the disk</span></span>

<span data-ttu-id="37b3b-109">Para enumerar los discos disponibles en Windows, ejecute:</span><span class="sxs-lookup"><span data-stu-id="37b3b-109">To list the available disks in Windows, run:</span></span>

```powershell
wmic diskdrive list brief
```

<span data-ttu-id="37b3b-110">Las rutas de acceso de los discos están disponibles en las columnas ' DeviceID '.</span><span class="sxs-lookup"><span data-stu-id="37b3b-110">The disks paths are available under the 'DeviceID' columns.</span></span> <span data-ttu-id="37b3b-111">Normalmente en el `\\.\PHYSICALDRIVE*` formato.</span><span class="sxs-lookup"><span data-stu-id="37b3b-111">Usually under the `\\.\PHYSICALDRIVE*` format.</span></span>

## <a name="list-and-select-the-partitions-to-mount-in-wsl-2"></a><span data-ttu-id="37b3b-112">Lista y selección de las particiones que se van a montar en WSL 2</span><span class="sxs-lookup"><span data-stu-id="37b3b-112">List and select the partitions to mount in WSL 2</span></span>

<span data-ttu-id="37b3b-113">Una vez que se identifica el disco, ejecute:</span><span class="sxs-lookup"><span data-stu-id="37b3b-113">Once the disk is identified, run:</span></span>

```powershell
wsl --mount <DiskPath> --bare
```

<span data-ttu-id="37b3b-114">Esto hará que el disco esté disponible en WSL 2.</span><span class="sxs-lookup"><span data-stu-id="37b3b-114">This will make the disk available in WSL 2.</span></span>

<span data-ttu-id="37b3b-115">Una vez conectado, la partición se puede enumerar mediante la ejecución del siguiente comando en WSL 2:</span><span class="sxs-lookup"><span data-stu-id="37b3b-115">Once attached, the partition can be listed by running the following command inside WSL 2:</span></span>

```powershell
lsblk
```

<span data-ttu-id="37b3b-116">Se mostrarán los dispositivos de bloque y sus particiones disponibles.</span><span class="sxs-lookup"><span data-stu-id="37b3b-116">This will display the available block devices and their partitions.</span></span>

<span data-ttu-id="37b3b-117">En Linux, un dispositivo de bloque se identifica como  `/dev/<Device><Partition>` .</span><span class="sxs-lookup"><span data-stu-id="37b3b-117">Inside Linux, a block device is identified as  `/dev/<Device><Partition>`.</span></span> <span data-ttu-id="37b3b-118">Por ejemplo,/dev/sdb3, es la partición número 3 del disco `sdb` .</span><span class="sxs-lookup"><span data-stu-id="37b3b-118">For example, /dev/sdb3, is the partition number 3 of disk `sdb`.</span></span>

<span data-ttu-id="37b3b-119">Salida de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="37b3b-119">Example output:</span></span>

```powershell
NAME   MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
sdb      8:16   0    1G  0 disk
├─sdb2   8:18   0   50M  0 part
├─sdb3   8:19   0  873M  0 part
└─sdb1   8:17   0  100M  0 part
sdc      8:32   0  256G  0 disk /
sda      8:0    0  256G  0 disk
```

## <a name="identifying-the-filesystem-type"></a><span data-ttu-id="37b3b-120">Identificación del tipo de sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="37b3b-120">Identifying the filesystem type</span></span>

<span data-ttu-id="37b3b-121">Si no conoce el tipo de sistema de archivos de un disco o una partición, puede usar este comando:</span><span class="sxs-lookup"><span data-stu-id="37b3b-121">If you don't know the type of filesystem of a disk or partition, you can use this command:</span></span>

```powershell
blkid <BlockDevice>
```

<span data-ttu-id="37b3b-122">Se generará el tipo de sistema de archivos detectado (con el `TYPE="<Filesystem>"` formato).</span><span class="sxs-lookup"><span data-stu-id="37b3b-122">This will output the detected filesystem type (under the `TYPE="<Filesystem>"` format).</span></span>

## <a name="mount-the-selected-partitions"></a><span data-ttu-id="37b3b-123">Montar las particiones seleccionadas</span><span class="sxs-lookup"><span data-stu-id="37b3b-123">Mount the selected partitions</span></span>

<span data-ttu-id="37b3b-124">Una vez que haya identificado las particiones que desea montar, ejecute este comando en cada partición:</span><span class="sxs-lookup"><span data-stu-id="37b3b-124">Once you have identified the partitions you want to mount, run this command on each partition:</span></span> 

```powershell
wsl --mount <DiskPath> --partition <PartitionNumber> --type <Filesystem>
```

> [!NOTE]
> <span data-ttu-id="37b3b-125">Si desea montar todo el disco como un solo volumen (es decir, si el disco no tiene particiones), `--partition` se puede omitir.</span><span class="sxs-lookup"><span data-stu-id="37b3b-125">If you wish to mount the entire disk as a single volume (i.e. if the disk isn't partitioned), `--partition` can be omitted.</span></span>
> 
> <span data-ttu-id="37b3b-126">Si se omite, el tipo de sistema de archivos predeterminado es "ext4".</span><span class="sxs-lookup"><span data-stu-id="37b3b-126">If omitted, the default filesystem type is "ext4".</span></span>

## <a name="access-the-disk-content"></a><span data-ttu-id="37b3b-127">Acceder al contenido del disco</span><span class="sxs-lookup"><span data-stu-id="37b3b-127">Access the disk content</span></span>

<span data-ttu-id="37b3b-128">Una vez montado, se puede acceder al disco bajo la ruta de acceso indicada por el valor de configuración: `automount.root` .</span><span class="sxs-lookup"><span data-stu-id="37b3b-128">Once mounted, the disk can be accessed under the path pointed to by the config value: `automount.root`.</span></span> <span data-ttu-id="37b3b-129">El valor predeterminado es `/mnt/wsl`.</span><span class="sxs-lookup"><span data-stu-id="37b3b-129">The default value is `/mnt/wsl`.</span></span>

<span data-ttu-id="37b3b-130">Desde Windows, se puede tener acceso al disco desde el explorador de archivos. para ello, vaya a: `\\wsl$\\<Distro>\\<Mountpoint>` (Seleccione cualquier distribución de Linux).</span><span class="sxs-lookup"><span data-stu-id="37b3b-130">From Windows, the disk can be accessed from File Explorer by navigating to: `\\wsl$\\<Distro>\\<Mountpoint>` (pick any Linux distribution).</span></span>

## <a name="unmount-the-disk"></a><span data-ttu-id="37b3b-131">Desmontaje de los discos</span><span class="sxs-lookup"><span data-stu-id="37b3b-131">Unmount the disk</span></span>

<span data-ttu-id="37b3b-132">Si desea desmontar y desasociar el disco de WSL 2, ejecute:</span><span class="sxs-lookup"><span data-stu-id="37b3b-132">If you want to unmount and detach the disk from WSL 2, run:</span></span>

```powershell
wsl --unmount <DiskPath>
```

## <a name="command-line-reference"></a><span data-ttu-id="37b3b-133">Referencia de línea de comandos</span><span class="sxs-lookup"><span data-stu-id="37b3b-133">Command line reference</span></span>

### <a name="mouting-a-specific-filesystem"></a><span data-ttu-id="37b3b-134">Mouting un sistema de archivos específico</span><span class="sxs-lookup"><span data-stu-id="37b3b-134">Mouting a specific filesystem</span></span>

<span data-ttu-id="37b3b-135">De forma predeterminada, WSL 2 intentará montar el dispositivo como ext4.</span><span class="sxs-lookup"><span data-stu-id="37b3b-135">By default, WSL 2 will attempt to mount the device as ext4.</span></span> <span data-ttu-id="37b3b-136">Para especificar otro sistema de archivos, ejecute:</span><span class="sxs-lookup"><span data-stu-id="37b3b-136">To specify another filesystem, run:</span></span>

```powershell
wsl --mount <DiskPath> -t <FileSystem>
```

<span data-ttu-id="37b3b-137">Por ejemplo, para montar un disco como FAT, ejecute:</span><span class="sxs-lookup"><span data-stu-id="37b3b-137">For example, to mount a disk as fat, run:</span></span>

```
wsl --mount <Diskpath> -t vfat
```

> [!NOTE]
> <span data-ttu-id="37b3b-138">Para enumerar los sistemas de archivos disponibles en WSL2, ejecute: `cat /proc/filesystems`</span><span class="sxs-lookup"><span data-stu-id="37b3b-138">To list the available filesystems in WSL2, run: `cat /proc/filesystems`</span></span>

### <a name="mouting-a-specific-partition"></a><span data-ttu-id="37b3b-139">Mouting una partición específica</span><span class="sxs-lookup"><span data-stu-id="37b3b-139">Mouting a specific partition</span></span>

<span data-ttu-id="37b3b-140">De forma predeterminada, WSL 2 intenta montar todo el disco.</span><span class="sxs-lookup"><span data-stu-id="37b3b-140">By default, WSL 2 attempts to mount the entire disk.</span></span> <span data-ttu-id="37b3b-141">Para montar una partición específica, ejecute:</span><span class="sxs-lookup"><span data-stu-id="37b3b-141">To mount a specific partition, run:</span></span>

```
wsl --mount <Diskpath> -p <PartitionIndex>
```

<span data-ttu-id="37b3b-142">Esto solo funciona si el disco es MBR (registro de arranque maestro) o GPT (tabla de particiones GUID).</span><span class="sxs-lookup"><span data-stu-id="37b3b-142">This only works if the disk is either MBR (Master Boot Record) or GPT (GUID Partition Table).</span></span> <span data-ttu-id="37b3b-143">[Lea acerca de los estilos de partición: MBR y GPT](/windows-server/storage/disk-management/initialize-new-disks#about-partition-styles---gpt-and-mbr).</span><span class="sxs-lookup"><span data-stu-id="37b3b-143">[Read about partition styles - MBR and GPT](/windows-server/storage/disk-management/initialize-new-disks#about-partition-styles---gpt-and-mbr).</span></span>

### <a name="specifying-mount-options"></a><span data-ttu-id="37b3b-144">Especificar opciones de montaje</span><span class="sxs-lookup"><span data-stu-id="37b3b-144">Specifying mount options</span></span>

<span data-ttu-id="37b3b-145">Para especificar las opciones de montaje, ejecute:</span><span class="sxs-lookup"><span data-stu-id="37b3b-145">To specify mount options, run:</span></span>

```powershell
wsl --mount <DiskPath> -o <MountOptions>
```

<span data-ttu-id="37b3b-146">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="37b3b-146">Example:</span></span>

```powershell
wsl --mount <DiskPath> -o "data=ordered"
```

> [!NOTE]
> <span data-ttu-id="37b3b-147">En este momento solo se admiten las opciones específicas del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="37b3b-147">Only filesystem specific options are supported at this time.</span></span> <span data-ttu-id="37b3b-148">`ro, rw, noatime, ...`No se admiten opciones genéricas como.</span><span class="sxs-lookup"><span data-stu-id="37b3b-148">Generic options such as `ro, rw, noatime, ...` are not supported.</span></span>

### <a name="attaching-the-disk-without-mounting-it"></a><span data-ttu-id="37b3b-149">Conexión del disco sin montarlo</span><span class="sxs-lookup"><span data-stu-id="37b3b-149">Attaching the disk without mounting it</span></span>

<span data-ttu-id="37b3b-150">Si el esquema de disco no es compatible con ninguna de las opciones anteriores, puede adjuntar el disco a WSL 2 sin montarlo mediante la ejecución de:</span><span class="sxs-lookup"><span data-stu-id="37b3b-150">If the disk scheme isn't supported by any of the above options, you can attach the disk to WSL 2 without mounting it by running:</span></span>

```powershell
wsl --mount <DiskPath> --bare
```

<span data-ttu-id="37b3b-151">Esto hará que el dispositivo de bloque esté disponible dentro de WSL 2, por lo que se puede montar manualmente desde allí.</span><span class="sxs-lookup"><span data-stu-id="37b3b-151">This will make the block device available inside WSL 2 so it can be mounted manually from there.</span></span> <span data-ttu-id="37b3b-152">Use `lsblk` para enumerar los dispositivos de bloque disponibles dentro de WSL 2.</span><span class="sxs-lookup"><span data-stu-id="37b3b-152">Use `lsblk` to list the available block devices inside WSL 2.</span></span>

### <a name="detaching-a-disk"></a><span data-ttu-id="37b3b-153">Desconexión de un disco</span><span class="sxs-lookup"><span data-stu-id="37b3b-153">Detaching a disk</span></span>

<span data-ttu-id="37b3b-154">Para desasociar un disco de WSL 2, ejecute:</span><span class="sxs-lookup"><span data-stu-id="37b3b-154">To detach a disk from WSL 2, run:</span></span>

```powershell
wsl --unmount [DiskPath]
```

<span data-ttu-id="37b3b-155">Si `Diskpath` se omite, todos los discos conectados se desmontan y se desasocian.</span><span class="sxs-lookup"><span data-stu-id="37b3b-155">If `Diskpath` is omitted, all attached disks are unmounted and detached.</span></span>

> [!NOTE]
> <span data-ttu-id="37b3b-156">Si se produce un error al desmontar un disco, se puede forzar la salida de WSL 2 mediante `wsl --shutdown` la ejecución de, que desasociará el disco.</span><span class="sxs-lookup"><span data-stu-id="37b3b-156">If one disk fails to unmount, WSL 2 can be forced to exit by running `wsl --shutdown`, which will detach the disk.</span></span>

## <a name="limitations"></a><span data-ttu-id="37b3b-157">Limitaciones</span><span class="sxs-lookup"><span data-stu-id="37b3b-157">Limitations</span></span>

- <span data-ttu-id="37b3b-158">En este momento, solo se pueden adjuntar discos completos a WSL 2, lo que significa que no es posible adjuntar solo una partición.</span><span class="sxs-lookup"><span data-stu-id="37b3b-158">At this time, only entire disks can be attached to WSL 2, meaning that it's not possible to attach only a partition.</span></span> <span data-ttu-id="37b3b-159">Concretamente, esto significa que no es posible usar `wsl --mount` para leer una partición en el dispositivo de arranque, porque ese dispositivo no se puede desasociar de Windows.</span><span class="sxs-lookup"><span data-stu-id="37b3b-159">Concretely, this means that it's not possible to use `wsl --mount` to read a partition on the boot device, because that device can't be detached from Windows.</span></span>

- <span data-ttu-id="37b3b-160">Las unidades flash USB no se admiten en este momento y no se pueden asociar a WSL 2.</span><span class="sxs-lookup"><span data-stu-id="37b3b-160">USB flash drives are not supported at this time and will fail to attach to WSL 2.</span></span> <span data-ttu-id="37b3b-161">No obstante, se admiten discos USB.</span><span class="sxs-lookup"><span data-stu-id="37b3b-161">USB disks are supported though.</span></span>

- <span data-ttu-id="37b3b-162">Solo los sistemas de archivos que se admiten de forma nativa en el kernel se pueden montar con `wsl --mount` .</span><span class="sxs-lookup"><span data-stu-id="37b3b-162">Only filesystems that are natively supported in the kernel can be mounted by `wsl --mount`.</span></span> <span data-ttu-id="37b3b-163">Esto significa que no es posible usar controladores de sistema de archivos instalados (por ejemplo, NTFS-3G) mediante una llamada a `wsl --mount` .</span><span class="sxs-lookup"><span data-stu-id="37b3b-163">This means that it's not possible to use installed filesystem drivers (such as ntfs-3g for example) by calling `wsl --mount`.</span></span>