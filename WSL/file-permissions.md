---
title: Permisos de archivo
description: Descripción de cómo WSL determina los permisos de archivo en Windows
keywords: BashOnWindows, bash, wsl, wsl2, windows, subsistema de windows para linux, subsistemawindows, ubuntu, debian, suse, windows 10, archivo, permisos
ms.date: 01/14/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.localizationpriority: high
ms.openlocfilehash: 81d4cfa1ae57cdd077ba8cbd614111881724718a
ms.sourcegitcommit: f1b049a1276782d4f2754f46a8d2025b598a0784
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/24/2020
ms.locfileid: "85336078"
---
# <a name="file-permissions-for-wsl"></a><span data-ttu-id="d4246-104">Permisos de archivo para WSL</span><span class="sxs-lookup"><span data-stu-id="d4246-104">File Permissions for WSL</span></span>

<span data-ttu-id="d4246-105">En esta página se detalla cómo se interpretan los permisos de archivo de Linux en el Subsistema de Windows para Linux, en especial al acceder a recursos dentro de Windows en el sistema de archivos NT.</span><span class="sxs-lookup"><span data-stu-id="d4246-105">This page details how Linux file permissions are interpreted across the Windows Subsystem for Linux, especially when accessing resources inside of Windows on the NT file system.</span></span> <span data-ttu-id="d4246-106">En esta documentación se supone que tienes un conocimiento básico de la [estructura de permisos del sistema de archivos de Linux](https://wiki.archlinux.org/index.php/File_permissions_and_attributes) y del [comando umask](https://en.wikipedia.org/wiki/Umask).</span><span class="sxs-lookup"><span data-stu-id="d4246-106">This documentation assumes a basic understanding of the [Linux file system permissions structure](https://wiki.archlinux.org/index.php/File_permissions_and_attributes) and the [umask command](https://en.wikipedia.org/wiki/Umask).</span></span>

<span data-ttu-id="d4246-107">Al acceder a los archivos de Windows desde WSL, los permisos de archivo se calculan a partir de los permisos de Windows o se leen de los metadatos que WSL ha agregado al archivo.</span><span class="sxs-lookup"><span data-stu-id="d4246-107">When accessing Windows files from WSL the file permissions are either calculated from Windows permissions, or are read from metadata that has been added to the file by WSL.</span></span> <span data-ttu-id="d4246-108">Estos metadatos no están habilitados de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d4246-108">This metadata is not enabled by default.</span></span>

## <a name="wsl-metadata-on-windows-files"></a><span data-ttu-id="d4246-109">Metadatos de WSL en archivos de Windows</span><span class="sxs-lookup"><span data-stu-id="d4246-109">WSL metadata on Windows files</span></span>

<span data-ttu-id="d4246-110">Cuando los metadatos están habilitados como opción de montaje en WSL, se pueden agregar e interpretar atributos extendidos en archivos de Windows NT para proporcionar los permisos del sistema de archivos de Linux.</span><span class="sxs-lookup"><span data-stu-id="d4246-110">When metadata is enabled as a mount option in WSL, extended attributes on Windows NT files can be added and interpreted to supply Linux file system permissions.</span></span>

<span data-ttu-id="d4246-111">WSL puede agregar cuatro atributos extendidos de NTFS:</span><span class="sxs-lookup"><span data-stu-id="d4246-111">WSL can add four NTFS extended attributes:</span></span>

| <span data-ttu-id="d4246-112">Nombre del atributo</span><span class="sxs-lookup"><span data-stu-id="d4246-112">Attribute Name</span></span> | <span data-ttu-id="d4246-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4246-113">Description</span></span> |
| --- | --- |
| <span data-ttu-id="d4246-114">$LXUID</span><span class="sxs-lookup"><span data-stu-id="d4246-114">$LXUID</span></span> | <span data-ttu-id="d4246-115">Id. del propietario del usuario</span><span class="sxs-lookup"><span data-stu-id="d4246-115">User Owner ID</span></span> |
| <span data-ttu-id="d4246-116">$LXGID</span><span class="sxs-lookup"><span data-stu-id="d4246-116">$LXGID</span></span> | <span data-ttu-id="d4246-117">Id. del propietario del grupo</span><span class="sxs-lookup"><span data-stu-id="d4246-117">Group Owner ID</span></span> |
| <span data-ttu-id="d4246-118">$LXMOD</span><span class="sxs-lookup"><span data-stu-id="d4246-118">$LXMOD</span></span> | <span data-ttu-id="d4246-119">Modo de archivo (octales y tipo de permisos de sistemas de archivos; por ejemplo: 0777)</span><span class="sxs-lookup"><span data-stu-id="d4246-119">File mode (File systems permission octals and type, e.g: 0777)</span></span> |
| <span data-ttu-id="d4246-120">$LXDEV</span><span class="sxs-lookup"><span data-stu-id="d4246-120">$LXDEV</span></span> | <span data-ttu-id="d4246-121">Dispositivo, si es un archivo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="d4246-121">Device, if it is a device file</span></span> |

<span data-ttu-id="d4246-122">Además, cualquier archivo que no sea un archivo o directorio normal (por ejemplo, vínculos simbólicos, FIFO [PEPS], dispositivos de bloques, sockets de UNIX y dispositivos de caracteres) también tiene un [punto de repetición de análisis](https://docs.microsoft.com/windows/win32/fileio/reparse-points) de NTFS.</span><span class="sxs-lookup"><span data-stu-id="d4246-122">Additionally, any file that is not a regular file or directory (e.g: symlinks, FIFOs, block devices, unix sockets, and character devices) also have an NTFS [reparse point](https://docs.microsoft.com/windows/win32/fileio/reparse-points).</span></span> <span data-ttu-id="d4246-123">De este modo, es mucho más rápido determinar el tipo de archivo en un directorio específico sin tener que consultar sus atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="d4246-123">This makes it much faster to determine the kind of file in a given directory without having to query its extended attributes.</span></span>

## <a name="file-access-scenarios"></a><span data-ttu-id="d4246-124">Escenarios de acceso a archivos</span><span class="sxs-lookup"><span data-stu-id="d4246-124">File Access Scenarios</span></span>

<span data-ttu-id="d4246-125">A continuación, se muestra una descripción de cómo se determinan los permisos al acceder a los archivos de diferentes maneras con el Subsistema de Windows para Linux.</span><span class="sxs-lookup"><span data-stu-id="d4246-125">Below is a description of how permissions are determined when accessing files in different ways using the Windows Subsystem for Linux.</span></span>

### <a name="accessing-files-in-the-windows-drive-file-system-drvfs-from-linux"></a><span data-ttu-id="d4246-126">Acceso a archivos en el sistema de archivos de la unidad de Windows (DrvFS) desde Linux</span><span class="sxs-lookup"><span data-stu-id="d4246-126">Accessing Files in the Windows drive file system (DrvFS) from Linux</span></span>

<span data-ttu-id="d4246-127">Estos escenarios se producen cuando accedes a los archivos de Windows desde WSL, más probablemente a través de `/mnt/c`.</span><span class="sxs-lookup"><span data-stu-id="d4246-127">These scenarios occur when you are accessing your Windows files from WSL, most likely via `/mnt/c`.</span></span>

#### <a name="reading-file-permissions-from-an-existing-windows-file"></a><span data-ttu-id="d4246-128">Lectura de los permisos de un archivo de Windows existente</span><span class="sxs-lookup"><span data-stu-id="d4246-128">Reading file permissions from an existing Windows file</span></span>

<span data-ttu-id="d4246-129">El resultado depende de si el archivo ya tiene metadatos.</span><span class="sxs-lookup"><span data-stu-id="d4246-129">The result depends on if the file already has existing metadata.</span></span>

##### <a name="drvfs-file-does-not-have-metadata-default"></a><span data-ttu-id="d4246-130">El archivo DrvFS no tiene metadatos (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="d4246-130">DrvFS file does not have metadata (default)</span></span>

<span data-ttu-id="d4246-131">Si el archivo no tiene metadatos asociados, convertimos los permisos vigentes del usuario de Windows en bits de lectura, escritura o ejecución, y los establecemos en el mismo valor para el usuario, el grupo y otros.</span><span class="sxs-lookup"><span data-stu-id="d4246-131">If the file has no metadata associated with it then we translate the effective permissions of the Windows user to read/write/execute bits and set them to the this as the same value for user, group, and other.</span></span> <span data-ttu-id="d4246-132">Por ejemplo, si tu cuenta de usuario de Windows tiene acceso de lectura y ejecución, pero no tiene acceso de escritura al archivo, se mostrará como `r-x` para el usuario, el grupo y otros.</span><span class="sxs-lookup"><span data-stu-id="d4246-132">For example, if your Windows user account has read and execute access but not write access to the file then this will be shown as `r-x` for user, group and other.</span></span> <span data-ttu-id="d4246-133">Si el archivo tiene el atributo "Solo lectura" establecido en Windows, no concederemos el acceso de escritura en Linux.</span><span class="sxs-lookup"><span data-stu-id="d4246-133">If the file has the 'Read Only' attribute set in Windows then we do not grant write access in Linux.</span></span>

##### <a name="the-file-has-metadata"></a><span data-ttu-id="d4246-134">El archivo tiene metadatos</span><span class="sxs-lookup"><span data-stu-id="d4246-134">The file has metadata</span></span>

<span data-ttu-id="d4246-135">Si el archivo tiene metadatos, simplemente usamos esos valores de metadatos en lugar de convertir los permisos vigentes del usuario de Windows.</span><span class="sxs-lookup"><span data-stu-id="d4246-135">If the file has metadata present, we simply use those metadata values instead of translating effective permissions of the Windows user.</span></span>

#### <a name="changing-file-permissions-on-an-existing-windows-file-using-chmod"></a><span data-ttu-id="d4246-136">Cambio de los permisos de archivo de un archivo de Windows existente mediante chmod</span><span class="sxs-lookup"><span data-stu-id="d4246-136">Changing file permissions on an existing Windows file using chmod</span></span>

<span data-ttu-id="d4246-137">El resultado depende de si el archivo ya tiene metadatos existentes.</span><span class="sxs-lookup"><span data-stu-id="d4246-137">The result depends on if the file already has existing metadata.</span></span>

##### <a name="chmod-file-does-not-have-metadata-default"></a><span data-ttu-id="d4246-138">El archivo chmod no tiene metadatos (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="d4246-138">chmod file does not have metadata (default)</span></span>

<span data-ttu-id="d4246-139">Chmod solo tendrá un efecto. Si quitas todos los atributos de escritura de un archivo, se establecerá el atributo "Solo lectura" en el archivo de Windows, ya que se trata del mismo comportamiento de CIFS (Sistema de archivos de Internet común), que es el cliente SMB (Bloque de mensajes del servidor) en Linux.</span><span class="sxs-lookup"><span data-stu-id="d4246-139">Chmod will only have one effect, if you remove all the write attributes of a file then the 'read only' attribute on the Windows file will be set, since this is the same behaviour as CIFS (Common Internet File System) which is the SMB (Server Message Block) client in Linux.</span></span>

##### <a name="chmod-file-has-metadata"></a><span data-ttu-id="d4246-140">El archivo chmod tiene metadatos</span><span class="sxs-lookup"><span data-stu-id="d4246-140">chmod file has metadata</span></span>

<span data-ttu-id="d4246-141">Chmod cambiará o agregará metadatos en función de los metadatos ya existentes del archivo.</span><span class="sxs-lookup"><span data-stu-id="d4246-141">Chmod will change or add metadata depending on the file's already existing metadata.</span></span> 

<span data-ttu-id="d4246-142">Ten en cuenta que no puedes concederte un mayor acceso del que tienes en Windows, aunque los metadatos indiquen lo contrario.</span><span class="sxs-lookup"><span data-stu-id="d4246-142">Please keep in mind that you cannot give yourself more access than what you have on Windows, even if the metadata says that is the case.</span></span> <span data-ttu-id="d4246-143">Por ejemplo, podrías establecer los metadatos para mostrar que tienes permisos de escritura en un archivo mediante `chmod 777`, pero si intentas acceder a ese archivo, tampoco podrás escribir en él.</span><span class="sxs-lookup"><span data-stu-id="d4246-143">For example, you could set the metadata to display that you have write permissions to a file using `chmod 777`, but if you tried to access that file you would still not be able to write to it.</span></span> <span data-ttu-id="d4246-144">Esto se debe a la interoperabilidad, ya que los comandos de lectura o escritura en los archivos de Windows se enrutan a través de los permisos de usuario de Windows.</span><span class="sxs-lookup"><span data-stu-id="d4246-144">This is thanks to interopability, as any read or write commands to Windows files are routed through your Windows user permissions.</span></span>

#### <a name="creating-a-file-in-drivefs"></a><span data-ttu-id="d4246-145">Creación de un archivo en DriveFS</span><span class="sxs-lookup"><span data-stu-id="d4246-145">Creating a file in DriveFS</span></span>

<span data-ttu-id="d4246-146">El resultado depende de si los metadatos están habilitados.</span><span class="sxs-lookup"><span data-stu-id="d4246-146">The result depends on if metadata is enabled.</span></span>

##### <a name="metadata-is-not-enabled-default"></a><span data-ttu-id="d4246-147">Los metadatos no están habilitados (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="d4246-147">Metadata is not enabled (default)</span></span>

<span data-ttu-id="d4246-148">Los permisos de Windows del archivo recién creado serán los mismos que si creas el archivo en Windows sin un descriptor de seguridad específico. Este heredará los permisos del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="d4246-148">The Windows permissions of the newly created file will be the same as if you created the file in Windows without a specific security descriptor, it will inherit the parent's permissions.</span></span>

##### <a name="metadata-is-enabled"></a><span data-ttu-id="d4246-149">Los metadatos están habilitados</span><span class="sxs-lookup"><span data-stu-id="d4246-149">Metadata is enabled</span></span>

<span data-ttu-id="d4246-150">Los bits de permiso del archivo se establecen para seguir el comando umask de Linux, y el archivo se guardará con metadatos.</span><span class="sxs-lookup"><span data-stu-id="d4246-150">The file's permission bits are set to follow the Linux umask, and the file will be saved with metadata.</span></span>

#### <a name="which-linux-user-and-linux-group-owns-the-file"></a><span data-ttu-id="d4246-151">¿Qué usuario y grupo de Linux son propietarios del archivo?</span><span class="sxs-lookup"><span data-stu-id="d4246-151">Which Linux user and Linux group owns the file?</span></span> 

<span data-ttu-id="d4246-152">El resultado depende de si el archivo ya tiene metadatos existentes.</span><span class="sxs-lookup"><span data-stu-id="d4246-152">The result depends on if the file already has existing metadata.</span></span>

##### <a name="user-file-does-not-have-metadata-default"></a><span data-ttu-id="d4246-153">El archivo de usuario no tiene metadatos (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="d4246-153">User file does not have metadata (default)</span></span>

<span data-ttu-id="d4246-154">En el escenario predeterminado, al montar las unidades de Windows de forma automática, especificamos que el identificador de usuario (UID) de cualquier archivo se establece en el identificador del usuario de WSL, y el identificador de grupo (GID) se establece en el identificador de grupo principal del usuario de WSL.</span><span class="sxs-lookup"><span data-stu-id="d4246-154">In the default scenario, when automounting Windows drives, we specify that the user ID (UID) for any file is set to the user ID of your WSL user and the group ID (GID) is set to the principal group ID of your WSL user.</span></span>

##### <a name="user-file-has-metadata"></a><span data-ttu-id="d4246-155">El archivo de usuario tiene metadatos</span><span class="sxs-lookup"><span data-stu-id="d4246-155">User file has metadata</span></span>

<span data-ttu-id="d4246-156">El UID y el GID especificados en los metadatos se aplican como propietario del usuario y del grupo del archivo.</span><span class="sxs-lookup"><span data-stu-id="d4246-156">The UID and GID specified in the metadata is applied as the user owner and group owner of the file.</span></span>

### <a name="accessing-linux-files-from-windows-using-wsl"></a><span data-ttu-id="d4246-157">Acceso a archivos de Linux desde Windows mediante `\\wsl$`</span><span class="sxs-lookup"><span data-stu-id="d4246-157">Accessing Linux files from Windows using `\\wsl$`</span></span>

<span data-ttu-id="d4246-158">El acceso a los archivos de Linux a través de `\\wsl$` usará el usuario predeterminado de la distribución de WSL.</span><span class="sxs-lookup"><span data-stu-id="d4246-158">Accessing Linux files via `\\wsl$` will use the default user of your WSL distribution.</span></span> <span data-ttu-id="d4246-159">Por lo tanto, cualquier aplicación de Windows que acceda a archivos de Linux tendrá los mismos permisos que el usuario predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d4246-159">Therefore any Windows app accessing Linux files will have the same permissions as the default user.</span></span>

#### <a name="creating-a-new-file"></a><span data-ttu-id="d4246-160">Creación de un archivo nuevo</span><span class="sxs-lookup"><span data-stu-id="d4246-160">Creating a new file</span></span>

<span data-ttu-id="d4246-161">El valor de umask predeterminado se aplica al crear un nuevo archivo dentro de una distribución de WSL desde Windows.</span><span class="sxs-lookup"><span data-stu-id="d4246-161">The default umask is applied when creating a new file inside of a WSL distribution from Windows.</span></span> <span data-ttu-id="d4246-162">Dicho valor es `022` o, en otras palabras, permite todos los permisos excepto los de escritura para grupos y otros.</span><span class="sxs-lookup"><span data-stu-id="d4246-162">The default umask is `022`, or in other words it allows all permissions except write permissions to groups and others.</span></span> 

### <a name="accessing-files-in-the-linux-root-file-system-from-linux"></a><span data-ttu-id="d4246-163">Acceso a archivos en el sistema de archivos raíz de Linux desde Linux</span><span class="sxs-lookup"><span data-stu-id="d4246-163">Accessing files in the Linux root file system from Linux</span></span>

<span data-ttu-id="d4246-164">Los archivos creados, modificados o a los que se accede en el sistema de archivos raíz de Linux siguen las convenciones estándar de Linux, como la aplicación de umask a un archivo recién creado.</span><span class="sxs-lookup"><span data-stu-id="d4246-164">Any files created, modified, or accessed in the Linux root file system follow standard Linux conventions, such as applying the umask to a newly created file.</span></span>

## <a name="configuring-file-permissions"></a><span data-ttu-id="d4246-165">Configuración de permisos de archivo</span><span class="sxs-lookup"><span data-stu-id="d4246-165">Configuring file permissions</span></span>

<span data-ttu-id="d4246-166">Puedes configurar los permisos de archivo dentro de las unidades de Windows mediante las opciones de montaje de wsl.conf.</span><span class="sxs-lookup"><span data-stu-id="d4246-166">You can configure your file permissions inside of your Windows drives using the mount options in wsl.conf.</span></span> <span data-ttu-id="d4246-167">Las opciones de montaje te permiten establecer las máscaras de permisos `umask`, `dmask` y `fmask`.</span><span class="sxs-lookup"><span data-stu-id="d4246-167">The mount options allow you to set `umask`, `dmask` and `fmask` permissions masks.</span></span> <span data-ttu-id="d4246-168">`umask` se aplica a todos los archivos, `dmask` se aplica solo a los directorios y `fmask` se aplica solo a los archivos.</span><span class="sxs-lookup"><span data-stu-id="d4246-168">The `umask` is applied to all files, the `dmask` is applied just to directories and the `fmask` is applied just to files.</span></span> <span data-ttu-id="d4246-169">Luego, estas máscaras de permisos se someten a una operación OR lógica cuando se aplican a archivos, por ejemplo: Si tienes un valor de `umask` de `023` y uno de `fmask` de `022`, la máscara de permisos resultante para los archivos será `023`.</span><span class="sxs-lookup"><span data-stu-id="d4246-169">These permission masks are then put through a logical OR operation when being applied to files, e.g: If you have a `umask` value of `023` and an `fmask` value of `022` then the resulting permissions mask for files will be `023`.</span></span>

<span data-ttu-id="d4246-170">Consulte el artículo [Configuración de las opciones de inicio por distribución con wslconf](./wsl-config.md#configure-per-distro-launch-settings-with-wslconf) para obtener instrucciones sobre cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="d4246-170">Please see the [Configure per distro launch settings with wslconf](./wsl-config.md#configure-per-distro-launch-settings-with-wslconf) article for instructions on how to do this.</span></span>
