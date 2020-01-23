---
title: Permisos de archivo
description: Descripción de cómo WSL determina los permisos de archivo en Windows
keywords: BashOnWindows, bash, WSL, wsl2, Windows, subsistema de Windows para Linux, windowssubsystem, Ubuntu, Debian, SuSE, Windows 10, archivo, permisos
ms.date: 01/14/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 4566fc86cf14df986bde80cf3a6cfb9267b23308
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520864"
---
# <a name="file-permissions-for-wsl"></a><span data-ttu-id="3cb1b-104">Permisos de archivo para WSL</span><span class="sxs-lookup"><span data-stu-id="3cb1b-104">File Permissions for WSL</span></span>

<span data-ttu-id="3cb1b-105">En esta página se detalla cómo se interpretan los permisos de archivo de Linux en el subsistema de Windows para Linux, especialmente cuando se tiene acceso a recursos dentro de Windows en el sistema de archivos NT.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-105">This page details how Linux file permissions are interpreted across the Windows Subsystem for Linux, especially when accessing resources inside of Windows on the NT file system.</span></span> <span data-ttu-id="3cb1b-106">En esta documentación se supone un conocimiento básico de la [estructura de permisos del sistema de archivos de Linux](https://wiki.archlinux.org/index.php/File_permissions_and_attributes) .</span><span class="sxs-lookup"><span data-stu-id="3cb1b-106">This documentation assumes a basic understanding of the [Linux file system permissions structure](https://wiki.archlinux.org/index.php/File_permissions_and_attributes)</span></span> <!--TODO: Double check that it's okay to add these links--> <span data-ttu-id="3cb1b-107">y el [comando umask](https://en.wikipedia.org/wiki/Umask).</span><span class="sxs-lookup"><span data-stu-id="3cb1b-107">and the [umask command](https://en.wikipedia.org/wiki/Umask).</span></span>

<span data-ttu-id="3cb1b-108">Al acceder a los archivos de Windows desde WSL, los permisos de archivo se calculan a partir de los permisos de Windows o se leen de los metadatos que WSL ha agregado al archivo.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-108">When accessing Windows files from WSL the file permissions are either calculated from Windows permissions, or are read from metadata that has been added to the file by WSL.</span></span> <span data-ttu-id="3cb1b-109">Estos metadatos no están habilitados de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-109">This metadata is not enabled by default.</span></span> 

## <a name="wsl-metadata-on-windows-files"></a><span data-ttu-id="3cb1b-110">Metadatos de WSL en archivos de Windows</span><span class="sxs-lookup"><span data-stu-id="3cb1b-110">WSL metadata on Windows files</span></span>

<span data-ttu-id="3cb1b-111">Cuando se habilitan los metadatos como una opción de montaje en WSL, se pueden agregar e interpretar atributos extendidos en archivos de Windows NT para proporcionar los permisos del sistema de archivos de Linux.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-111">When metadata is enabled as a mount option in WSL, extended attributes on Windows NT files can be added and interpreted to supply Linux file system permissions.</span></span> 

<span data-ttu-id="3cb1b-112">WSL puede agregar cuatro atributos extendidos NTFS:</span><span class="sxs-lookup"><span data-stu-id="3cb1b-112">WSL can add four NTFS extended attributes:</span></span>

| <span data-ttu-id="3cb1b-113">Nombre de atributo</span><span class="sxs-lookup"><span data-stu-id="3cb1b-113">Attribute Name</span></span> | <span data-ttu-id="3cb1b-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="3cb1b-114">Description</span></span> |
| --- | --- |
| <span data-ttu-id="3cb1b-115">$LXUID</span><span class="sxs-lookup"><span data-stu-id="3cb1b-115">$LXUID</span></span> | <span data-ttu-id="3cb1b-116">IDENTIFICADOR del propietario del usuario</span><span class="sxs-lookup"><span data-stu-id="3cb1b-116">User Owner ID</span></span> |
| <span data-ttu-id="3cb1b-117">$LXGID</span><span class="sxs-lookup"><span data-stu-id="3cb1b-117">$LXGID</span></span> | <span data-ttu-id="3cb1b-118">IDENTIFICADOR del propietario del grupo</span><span class="sxs-lookup"><span data-stu-id="3cb1b-118">Group Owner ID</span></span> |
| <span data-ttu-id="3cb1b-119">$LXMOD</span><span class="sxs-lookup"><span data-stu-id="3cb1b-119">$LXMOD</span></span> | <span data-ttu-id="3cb1b-120">Modo de archivo (permisos de sistema de archivos octales y tipo; por ejemplo: 0777)</span><span class="sxs-lookup"><span data-stu-id="3cb1b-120">File mode (File systems permission octals and type, e.g: 0777)</span></span> |
| <span data-ttu-id="3cb1b-121">$LXDEV</span><span class="sxs-lookup"><span data-stu-id="3cb1b-121">$LXDEV</span></span> | <span data-ttu-id="3cb1b-122">Dispositivo, si es un archivo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="3cb1b-122">Device, if it is a device file</span></span> |

<span data-ttu-id="3cb1b-123">Además, cualquier archivo que no sea un archivo o directorio normal (por ejemplo, vínculos simbólicos, FIFO, dispositivos de bloque, sockets de UNIX y dispositivos de caracteres) también tiene un [punto de análisis](https://docs.microsoft.com/en-us/windows/win32/fileio/reparse-points)de NTFS.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-123">Additionally, any file that is not a regular file or directory (e.g: symlinks, FIFOs, block devices, unix sockets, and character devices) also have an NTFS [reparse point](https://docs.microsoft.com/en-us/windows/win32/fileio/reparse-points).</span></span> <span data-ttu-id="3cb1b-124">Esto hace que sea mucho más rápido determinar el tipo de archivo en un directorio determinado sin tener que consultar sus atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-124">This makes it much faster to determine the kind of file in a given directory without having to query its extended attributes.</span></span> 
<!-- TODO: For the blog include ONeDrive detail -->

## <a name="file-access-scenarios"></a><span data-ttu-id="3cb1b-125">Escenarios de acceso a archivos</span><span class="sxs-lookup"><span data-stu-id="3cb1b-125">File Access Scenarios</span></span>

<span data-ttu-id="3cb1b-126">A continuación se muestra una descripción de cómo se determinan los permisos al obtener acceso a los archivos de diferentes maneras con el subsistema de Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-126">Below is a description of how permissions are determined when accessing files in different ways using the Windows Subsystem for Linux.</span></span>

### <a name="accessing-files-in-the-windows-drive-file-system-drvfs-from-linux"></a><span data-ttu-id="3cb1b-127">Acceso a archivos en el sistema de archivos de unidad de Windows (DrvFS) desde Linux</span><span class="sxs-lookup"><span data-stu-id="3cb1b-127">Accessing Files in the Windows drive file system (DrvFS) from Linux</span></span>

<span data-ttu-id="3cb1b-128">Estos escenarios se producen cuando se accede a los archivos de Windows desde WSL, lo que es más probable a través de `/mnt/c`.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-128">These scenarios occur when you are accessing your Windows files from WSL, most likely via `/mnt/c`.</span></span> 

#### <a name="reading-file-permissions-from-an-existing-windows-file"></a><span data-ttu-id="3cb1b-129">Leer los permisos de archivo de un archivo de Windows existente</span><span class="sxs-lookup"><span data-stu-id="3cb1b-129">Reading file permissions from an existing Windows file</span></span>

<span data-ttu-id="3cb1b-130">El resultado depende de si el archivo ya tiene metadatos existentes.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-130">The result depends on if the file already has existing metadata.</span></span>

##### <a name="the-file-does-not-have-metadata-default"></a><span data-ttu-id="3cb1b-131">**El archivo no tiene metadatos (valor predeterminado)**</span><span class="sxs-lookup"><span data-stu-id="3cb1b-131">**The file does not have metadata (default)**</span></span>

<span data-ttu-id="3cb1b-132">Si el archivo no tiene metadatos asociados a él, trasladaremos los permisos vigentes del usuario de Windows a los bits de lectura/escritura/ejecución y los establecería como el mismo valor para usuario, grupo y otros.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-132">If the file has no metadata associated with it then we translate the effective permissions of the Windows user to read/write/execute bits and set them to the this as the same value for user, group, and other.</span></span> <span data-ttu-id="3cb1b-133">Por ejemplo, si su cuenta de usuario de Windows tiene acceso de lectura y ejecución pero no tiene acceso de escritura al archivo, se mostrará como `r-x` para usuario, grupo y otros.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-133">For example, if your Windows user account has read and execute access but not write access to the file then this will be shown as `r-x` for user, group and other.</span></span> <span data-ttu-id="3cb1b-134">Si el archivo tiene el atributo "solo lectura" establecido en Windows, no se concede acceso de escritura en Linux.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-134">If the file has the 'Read Only' attribute set in Windows then we do not grant write access in Linux.</span></span>

##### <a name="the-file-has-metadata"></a><span data-ttu-id="3cb1b-135">El archivo tiene metadatos</span><span class="sxs-lookup"><span data-stu-id="3cb1b-135">The file has metadata</span></span>

<span data-ttu-id="3cb1b-136">Si el archivo tiene metadatos, simplemente usamos esos valores de metadatos en lugar de traducir los permisos efectivos del usuario de Windows.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-136">If the file has metadata present, we simply use those metadata values instead of translating effective permissions of the Windows user.</span></span>

#### <a name="changing-file-permissions-on-an-existing-windows-file-using-chmod"></a><span data-ttu-id="3cb1b-137">Cambiar los permisos de archivo en un archivo de Windows existente con chmod</span><span class="sxs-lookup"><span data-stu-id="3cb1b-137">Changing file permissions on an existing Windows file using chmod</span></span>

<span data-ttu-id="3cb1b-138">El resultado depende de si el archivo ya tiene metadatos existentes.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-138">The result depends on if the file already has existing metadata.</span></span>

##### <a name="the-file-does-not-have-metadata-default"></a><span data-ttu-id="3cb1b-139">**El archivo no tiene metadatos (valor predeterminado)**</span><span class="sxs-lookup"><span data-stu-id="3cb1b-139">**The file does not have metadata (default)**</span></span>

<span data-ttu-id="3cb1b-140">Chmod solo tendrá un efecto, si quita todos los atributos de escritura de un archivo, se establecerá el atributo ' Read Only ' en el archivo de Windows, ya que se trata del mismo comportamiento que CIFS (sistema de archivos de Internet común), que es el cliente SMB (bloque de mensajes del servidor) en Linux.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-140">Chmod will only have one effect, if you remove all the write attributes of a file then the 'read only' attribute on the Windows file will be set, since this is the same behaviour as CIFS (Common Internet File System) which is the SMB (Server Message Block) client in Linux.</span></span>

##### <a name="the-file-has-metadata"></a><span data-ttu-id="3cb1b-141">El archivo tiene metadatos</span><span class="sxs-lookup"><span data-stu-id="3cb1b-141">The file has metadata</span></span>

<span data-ttu-id="3cb1b-142">Chmod cambiará o agregará metadatos en función de los metadatos ya existentes del archivo.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-142">Chmod will change or add metadata depending on the file's already existing metadata.</span></span> 

<span data-ttu-id="3cb1b-143">Tenga en cuenta que no puede dar más acceso a lo que tiene en Windows, aunque los metadatos indiquen que es el caso.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-143">Please keep in mind that you cannot give yourself more access than what you have on Windows, even if the metadata says that is the case.</span></span> <span data-ttu-id="3cb1b-144">Por ejemplo, puede establecer los metadatos para mostrar que tiene permisos de escritura en un archivo mediante `chmod 777`, pero si intentó tener acceso a ese archivo, todavía no podrá escribir en él.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-144">For example, you could set the metadata to display that you have write permissions to a file using `chmod 777`, but if you tried to access that file you would still not be able to write to it.</span></span> <span data-ttu-id="3cb1b-145">Esto se debe a la interoperabilidad, ya que los comandos de lectura o escritura de los archivos de Windows se enrutan a través de los permisos de usuario de Windows.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-145">This is thanks to interopability, as any read or write commands to Windows files are routed through your Windows user permissions.</span></span>

#### <a name="creating-a-file-in-drivefs"></a><span data-ttu-id="3cb1b-146">Crear un archivo en DriveFS</span><span class="sxs-lookup"><span data-stu-id="3cb1b-146">Creating a file in DriveFS</span></span>

<span data-ttu-id="3cb1b-147">El resultado depende de si se habilitan los metadatos.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-147">The result depends on if metadata is enabled.</span></span>

##### <a name="metadata-is-not-enabled-default"></a><span data-ttu-id="3cb1b-148">Los metadatos no están habilitados (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="3cb1b-148">Metadata is not enabled (default)</span></span>

<span data-ttu-id="3cb1b-149">Los permisos de Windows del archivo recién creado serán los mismos que si creara el archivo en Windows sin un descriptor de seguridad específico, heredará los permisos del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-149">The Windows permissions of the newly created file will be the same as if you created the file in Windows without a specific security descriptor, it will inherit the parent's permissions.</span></span> 

##### <a name="metadata-is-enabled"></a><span data-ttu-id="3cb1b-150">Los metadatos están habilitados</span><span class="sxs-lookup"><span data-stu-id="3cb1b-150">Metadata is enabled</span></span>

<span data-ttu-id="3cb1b-151">Los bits de permiso del archivo se establecen para seguir los umask de Linux y el archivo se guardará con metadatos.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-151">The file's permission bits are set to follow the Linux umask, and the file will be saved with metadata.</span></span>

#### <a name="which-linux-user-and-linux-group-owns-the-file"></a><span data-ttu-id="3cb1b-152">¿Qué grupo de usuarios de Linux y Linux posee el archivo?</span><span class="sxs-lookup"><span data-stu-id="3cb1b-152">Which Linux user and Linux group owns the file?</span></span> 

<span data-ttu-id="3cb1b-153">El resultado depende de si el archivo ya tiene metadatos existentes.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-153">The result depends on if the file already has existing metadata.</span></span>

##### <a name="the-file-does-not-have-metadata-default"></a><span data-ttu-id="3cb1b-154">**El archivo no tiene metadatos (valor predeterminado)**</span><span class="sxs-lookup"><span data-stu-id="3cb1b-154">**The file does not have metadata (default)**</span></span>
<span data-ttu-id="3cb1b-155">En el escenario predeterminado, al montar las unidades de Windows de forma predeterminada, especificamos que el identificador de usuario (UID) de cualquier archivo se establece en el identificador de usuario del usuario de WSL y el identificador de grupo (GID) se establece en el identificador de grupo principal del usuario de WSL.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-155">In the default scenario, when automounting Windows drives, we specify that the user ID (UID) for any file is set to the user ID of your WSL user and the group ID (GID) is set to the principal group ID of your WSL user.</span></span> 

##### <a name="the-file-has-metadata"></a><span data-ttu-id="3cb1b-156">El archivo tiene metadatos</span><span class="sxs-lookup"><span data-stu-id="3cb1b-156">The file has metadata</span></span>

<span data-ttu-id="3cb1b-157">El UID y el GID especificados en los metadatos se aplican como el propietario del usuario y el propietario del grupo del archivo.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-157">The UID and GID specified in the metadata is applied as the user owner and group owner of the file.</span></span> 

### <a name="accessing-linux-files-from-windows-using-wsl"></a><span data-ttu-id="3cb1b-158">Acceso a archivos de Linux desde Windows con `\\wsl$`</span><span class="sxs-lookup"><span data-stu-id="3cb1b-158">Accessing Linux files from Windows using `\\wsl$`</span></span>

<span data-ttu-id="3cb1b-159">El acceso a los archivos de Linux a través de `\\wsl$` usará el usuario predeterminado de su WSL distribución.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-159">Accessing Linux files via `\\wsl$` will use the default user of your WSL distro.</span></span> <span data-ttu-id="3cb1b-160">Por lo tanto, cualquier aplicación de Windows que tenga acceso a archivos de Linux tendrá los mismos permisos que el usuario predeterminado.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-160">Therefore any Windows app accessing Linux files will have the same permissions as the default user.</span></span>

#### <a name="creating-a-new-file"></a><span data-ttu-id="3cb1b-161">Crear un nuevo archivo</span><span class="sxs-lookup"><span data-stu-id="3cb1b-161">Creating a new file</span></span>

<span data-ttu-id="3cb1b-162">El valor predeterminado de umask se aplica al crear un nuevo archivo dentro de un distribución de WSL desde Windows.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-162">The default umask is applied when creating a new file inside of a WSL distro from Windows.</span></span> <span data-ttu-id="3cb1b-163">El valor predeterminado de umask es `022`, o en otras palabras permite todos los permisos excepto los permisos de escritura para grupos y otros.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-163">The default umask is `022`, or in other words it allows all permissions except write permissions to groups and others.</span></span> 

### <a name="accessing-files-in-the-linux-root-file-system-from-linux"></a><span data-ttu-id="3cb1b-164">Acceso a los archivos del sistema de archivos raíz de Linux desde Linux</span><span class="sxs-lookup"><span data-stu-id="3cb1b-164">Accessing files in the Linux root file system from Linux</span></span>

<span data-ttu-id="3cb1b-165">Los archivos creados, modificados o a los que se tiene acceso en el sistema de archivos raíz de Linux siguen las convenciones estándar de Linux, como la aplicación de umask a un archivo recién creado.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-165">Any files created, modified, or accessed in the Linux root file system follow standard Linux conventions, such as applying the umask to a newly created file.</span></span>

## <a name="configuring-file-permissions"></a><span data-ttu-id="3cb1b-166">Configuración de permisos de archivo</span><span class="sxs-lookup"><span data-stu-id="3cb1b-166">Configuring file permissions</span></span>

<span data-ttu-id="3cb1b-167">Puede configurar los permisos de archivo dentro de las unidades de Windows mediante las opciones de montaje de WSL. conf.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-167">You can configure your file permissions inside of your Windows drives using the mount options in wsl.conf.</span></span> <span data-ttu-id="3cb1b-168">Las opciones de montaje permiten establecer `umask`, `dmask` y `fmask` las máscaras de permisos.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-168">The mount options allow you to set `umask`, `dmask` and `fmask` permissions masks.</span></span> <span data-ttu-id="3cb1b-169">El `umask` se aplica a todos los archivos, el `dmask` se aplica solo a los directorios y el `fmask` se aplica solo a los archivos.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-169">The `umask` is applied to all files, the `dmask` is applied just to directories and the `fmask` is applied just to files.</span></span> <span data-ttu-id="3cb1b-170">Estas máscaras de permisos se colocan a continuación a través de una operación OR lógica cuando se aplican a archivos, por ejemplo: Si tiene un valor `umask` de `023` y un valor `fmask` de `022`, se `023`la máscara de permisos resultante para los archivos.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-170">These permission masks are then put through a logical OR operation when being applied to files, e.g: If you have a `umask` value of `023` and an `fmask` value of `022` then the resulting permissions mask for files will be `023`.</span></span> 

<span data-ttu-id="3cb1b-171">Consulte la página del documento sobre la [Administración de distribuciones de Linux](./wsl-config.md) para obtener instrucciones sobre cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="3cb1b-171">Please see the ['Manage Linux Distributions'](./wsl-config.md) document page for instructions on how to do this.</span></span>
<!-- TODO: Add # to the link-->

