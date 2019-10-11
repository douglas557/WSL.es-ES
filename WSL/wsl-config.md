---
title: Administrar distribuciones de Linux
description: Lista de referencia y configuración de varias distribuciones de Linux que se ejecutan en el subsistema de Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, subsistemawindows, ubuntu, wsl.conf, wslconfig
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: e69810625d08baf734683ff06231f79132ce1519
ms.sourcegitcommit: e1cc2fe4de0fa03d5aea14f6b328f1bb9d0c59be
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/07/2019
ms.locfileid: "71999394"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a>Administrar y configurar el subsistema de Windows para Linux

> Se aplica a Windows 10 Fall Creators Update y posterior.  Consulta nuestra [guía de instalación](./install_guide.md) actualizada para probar nuevas características de administración y comenzar a ejecutar varias distribuciones de Linux desde Microsoft Store.

## <a name="ways-to-run-wsl"></a>Formas de ejecutar WSL

Hay muchas maneras de ejecutar Linux con el subsistema de Windows para Linux.

1. `[distro]`, por ejemplo `ubuntu`
1. `wsl.exe` o `bash.exe`
1. `wsl [command]` o `bash -c [command]`

El método que deba usar dependerá de lo que esté haciendo.

### <a name="launch-wsl-by-distribution"></a>Iniciar WSL por distribución

La ejecución de una distribución mediante su aplicación específica de distribución inicia esa distribución en su propia ventana de la consola.

![Iniciar WSL desde el menú Inicio](media/start-launch.png)

Es lo mismo que hacer clic en "Iniciar" en Microsoft Store.

![Iniciar WSL desde Microsoft Store](media/store-launch.png)

También puedes ejecutar la distribución desde la línea de comandos ejecutando `[distribution].exe`.

El inconveniente de ejecutar una distribución desde la línea de comandos de esta manera es que cambiará automáticamente el directorio de trabajo del directorio actual al directorio principal de la distribución.

**Ejemplo:**

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> ubuntu

scooley@scooley-elmer:~$ pwd
/home/scooley
scooley@scooley-elmer:~$ exit
logout

PS C:\Users\sarah>
```

### <a name="wsl-and-wsl-command"></a>wsl y wsl [command]

La mejor manera de ejecutar WSL desde la línea de comandos es usar `wsl.exe`.

**Ejemplo:**

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

`wsl` no solo mantiene el directorio de trabajo actual, sino que te permite ejecutar un único comando junto a los comandos de Windows.

**Ejemplo:**

```console
PS C:\Users\sarah> Get-Date

Sunday, March 11, 2018 7:54:05 PM

PS C:\Users\sarah> wsl
scooley@scooley-elmer:/mnt/c/Users/sarah$ date
Sun Mar 11 19:56:57 DST 2018
scooley@scooley-elmer:/mnt/c/Users/sarah$ exit
logout

PS C:\Users\sarah> wsl date
Sun Mar 11 19:55:47 DST 2018
```

**Ejemplo:**

```console
PS C:\Users\sarah> Get-VM

Name            State CPUUsage(%) MemoryAssigned(M) Uptime   Status
----            ----- ----------- ----------------- ------   ------
Server17093     Off   0           0                 00:00:00 Opera...
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
Windows         Off   0           0                 00:00:00 Opera...


PS C:\Users\sarah> Get-VM | wsl grep "Ubuntu"
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
PS C:\Users\sarah>
```


## <a name="managing-multiple-linux-distributions"></a>Administración de varias distribuciones de Linux

### <a name="windows-10-version-1903-and-later"></a>Windows 10, versión 1903 y versiones posteriores

Puedes usar `wsl.exe` para administrar las distribuciones en el subsistema de Windows para Linux (WSL), incluida la enumeración de distribuciones disponibles, la configuración de una distribución predeterminada y la desinstalación de distribuciones.

Cada distribución de Linux administra de forma independiente sus propias configuraciones. Para ver los comandos específicos de la distribución, ejecuta `[distro.exe] /?`.  Por ejemplo, `ubuntu /?`.

#### <a name="list-distributions"></a>Enumerar distribuciones

`wsl -l`, `wsl --list`  
Enumera las distribuciones de Linux disponibles para WSL.  Si se enumera una distribución, está instalada y lista para usar.

`wsl --list --all`   
Enumera todas las distribuciones, incluidas las que no se pueden usar actualmente.  Pueden encontrarse en proceso de instalación, desinstalación o tener un estado interrumpido.  

`wsl --list --running`   
Enumera todas las distribuciones que se están actualmente en ejecución.

#### <a name="set-a-default-distribution"></a>Establecer una distribución predeterminada

La distribución de WSL predeterminada es la que se ejecuta cuando se ejecuta `wsl` en una línea de comandos.

`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`

Establece la distribución predeterminada en `<DistributionName>`.

**Ejemplo:**  
`wsl -s Ubuntu` establecería la distribución predeterminada en Ubuntu.  Ahora, al ejecutar `wsl npm init`, se ejecutará en Ubuntu.  Si se ejecuta `wsl`, se abrirá una sesión de Ubuntu.

#### <a name="unregister-and-reinstall-a-distribution"></a>Anular el registro de una distribución y reinstalarla

Aunque las distribuciones de Linux se pueden instalar a través de Microsoft Store, no se pueden desinstalar a través de Store.  WSL Config permite anular el registro de las distribuciones o desinstalarlas.

La anulación del registro también permite volver a instalar las distribuciones.

> **Precaución:** Una vez que se ha anulado el registro, todos los datos, la configuración y el software asociados a esa distribución se perderán de manera permanente.  Si se vuelve a instalar desde Store, se instalará una copia limpia de la distribución.

`wsl --unregister <DistributionName>`  
Anula el registro de la distribución de WSL para que se pueda volver a instalar o limpiar.

Por ejemplo: `wsl --unregister Ubuntu` quitaría Ubuntu de las distribuciones disponibles en WSL.  Al ejecutar `wsl --list`, no aparecerá en la lista.

Para reinstalar, busque la distribución en Microsoft Store y seleccione "Iniciar".

#### <a name="run-as-a-specific-user"></a>Ejecutar como usuario específico

`wsl -u <Username>`, `wsl --user <Username>`

Ejecuta WSL como el usuario especificado. Ten en cuenta que el usuario debe existir dentro de la distribución de WSL.

#### <a name="run-a-specific-distribution"></a>Ejecutar una distribución específica

`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`

Ejecuta una distribución especificada de WSL, se puede usar para enviar comandos a una distribución específica sin tener que cambiar la predeterminada.

### <a name="versions-earlier-than-windows-10-version-1903"></a>Versiones anteriores a Windows 10, versión 1903

WSL Config (`wslconfig.exe`) es una herramienta de línea de comandos para administrar las distribuciones de Linux que se ejecutan en el subsistema de Windows para Linux (WSL).  Te permite enumerar las distribuciones disponibles, establecer una distribución predeterminada y desinstalar las distribuciones.

Si bien WSL Config es útil para las configuraciones que abarcan o coordinan las distribuciones, cada distribución de Linux administra de forma independiente sus propias configuraciones.  Para ver los comandos específicos de la distribución, ejecuta `[distro.exe] /?`.  Por ejemplo, `ubuntu /?`.

Para ver todas las opciones disponibles para wslconfig, ejecuta: `wslconfig /?`

```console
wslconfig.exe
Performs administrative operations on Windows Subsystem for Linux

Usage:
    /l, /list [/all] - Lists registered distributions.
        /all - Optionally list all distributions, including distributions that
               are currently being installed or uninstalled.
    /s, /setdefault <DistributionName> - Sets the specified distribution as the default.
    /u, /unregister <DistributionName> - Unregisters a distribution.
```

#### <a name="list-distributions"></a>Enumerar distribuciones

`wslconfig /list`  
Enumera las distribuciones de Linux disponibles para WSL.  Si se enumera una distribución, está instalada y lista para usar.

`wslconfig /list /all`  
Enumera todas las distribuciones, incluidas las que no se pueden usar actualmente.  Pueden encontrarse en proceso de instalación, desinstalación o tener un estado interrumpido.  

#### <a name="set-a-default-distribution"></a>Establecer una distribución predeterminada

La distribución de WSL predeterminada es la que se ejecuta cuando se ejecuta `wsl` en una línea de comandos.

`wslconfig /setdefault <DistributionName>`

Establece la distribución predeterminada en `<DistributionName>`.

**Ejemplo:**  
`wslconfig /setdefault Ubuntu` establecería la distribución predeterminada en Ubuntu.  Ahora, al ejecutar `wsl npm init`, se ejecutará en Ubuntu.  Si se ejecuta `wsl`, se abrirá una sesión de Ubuntu.

#### <a name="unregister-and-reinstall-a-distribution"></a>Anular el registro de una distribución y reinstalarla

Aunque las distribuciones de Linux se pueden instalar a través de Microsoft Store, no se pueden desinstalar a través de Store.  WSL Config permite anular el registro de las distribuciones o desinstalarlas.

La anulación del registro también permite volver a instalar las distribuciones.

> **Precaución:** Una vez que se ha anulado el registro, todos los datos, la configuración y el software asociados a esa distribución se perderán de manera permanente.  Si se vuelve a instalar desde Store, se instalará una copia limpia de la distribución.

`wslconfig /unregister <DistributionName>`  
Anula el registro de la distribución de WSL para que se pueda volver a instalar o limpiar.

Por ejemplo: `wslconfig /unregister Ubuntu` quitaría Ubuntu de las distribuciones disponibles en WSL.  Al ejecutar `wslconfig /list`, no aparecerá en la lista.

Para reinstalar, busque la distribución en Microsoft Store y seleccione "Iniciar".

## <a name="set-wsl-launch-settings"></a>Establecer la configuración de inicio de WSL

> **Disponible en la compilación 17093 de Windows Insider y versiones posteriores**

Configura automáticamente cierta funcionalidad en WSL que se aplicará cada vez que inicies el subsistema mediante `wsl.conf`. 

En este momento, esto incluye opciones de montaje automático y configuración de red.

`wsl.conf` se encuentra en cada distribución de Linux en `/etc/wsl.conf`. Si el archivo no está allí, puedes crearlo tú mismo. WSL detectará la existencia del archivo y leerá su contenido. Si falta el archivo o tiene un formato incorrecto (es decir, un formato de marcado incorrecto), WSL se iniciará de manera normal.

A continuación se muestra un archivo `wsl.conf` de ejemplo que puedes agregar a tus distribuciones:

```console
# Enable extra metadata options by default
[automount]
enabled = true
root = /windir/
options = "metadata,umask=22,fmask=11"
mountFsTab = false

# Enable DNS – even though these are turned on by default, we’ll specify here just to be explicit.
[network]
generateHosts = true
generateResolvConf = true
```

### <a name="configuration-options"></a>Opciones de configuración

En concordancia con las convenciones de .ini, las claves se declaran en una sección. 

WSL admite dos secciones: `automount` y `network`.

#### <a name="automount"></a>automount

Sección: `[automount]`


| key        | value                          | valor predeterminado      | notas                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| enabled    | boolean                        | true         | `true` hace que las unidades fijas (es decir, `C:/` o `D:/`) se monten automáticamente con DrvFs en `/mnt`.  `false` significa que las unidades no se montarán automáticamente, pero podrías montarlas de forma manual o a través de `fstab`.                                                                                                             |
| mountFsTab | boolean                        | true         | `true` establece `/etc/fstab` para que se procese en el inicio de WSL. /etc/fstab es un archivo donde puedes declarar otros sistemas de archivos, como un recurso compartido de SMB. Por lo tanto, puedes montar estos sistemas de archivos automáticamente en WSL en el inicio.                                                                                                                |
| root       | Cadena                         | `/mnt/`      | Establece el directorio donde se montarán automáticamente las unidades fijas. Por ejemplo, si tienes un directorio en WSL en `/windir/` y lo especificas como raíz, esperarías ver que las unidades fijas se monten en `/windir/c`                                                                                              |
| opciones    | lista de valores separados por comas | cadena vacía | Este valor se anexa a la cadena predeterminada de opciones de montaje de DrvFs. **Solo se pueden especificar opciones específicas de DrvFs.** No se admiten las opciones que el binario de montaje analizaría normalmente en una marca. Si quieres especificar explícitamente esas opciones, tienes que incluir en /etc/fstab cada unidad para la que quieras hacerlo. |

De manera predeterminada, WSL establece uid y gid en el valor del usuario predeterminado (en una distribución de Ubuntu, el usuario predeterminado se crea con uid=1000,gid=1000). Si el usuario especifica una opción gid o uid explícitamente a través de esta clave, se sobrescribirá el valor asociado. De lo contrario, siempre se anexará el valor predeterminado.

**Nota:** Estas opciones se aplican como opciones de montaje para todas las unidades montadas automáticamente. Para cambiar las opciones solo para una unidad específica, usa /etc/fstab en su lugar.

##### <a name="mount-options"></a>Opciones de montaje

Establecer diferentes opciones de montaje para las unidades de Windows (DrvFs) puede controlar cómo se calculan los permisos de archivo para los archivos de Windows. Están disponibles las opciones siguientes:

| Tecla | Descripción | Predeterminado |
|:----|:----|:----|
|uid| Id. de usuario que se usa para el propietario de todos los archivos | Id. de usuario predeterminado de su distribución WSL (en la primera instalación, el valor predeterminado es 1000)
|gid| Id. de grupo que se usa para el propietario de todos los archivos | Id. de grupo predeterminado de su distribución WSL (en la primera instalación, el valor predeterminado es 1000)
|umask | Máscara octal de permisos que se van a excluir para todos los archivos y directorios | 000
|fmask | Máscara octal de permisos que se van a excluir para todos los archivos | 000
|dmask | Máscara octal de permisos que se van a excluir para todos los directorios | 000

**Nota:** Las máscaras de permisos se colocan a través de una operación OR lógica antes de aplicarse a archivos o directorios. 

#### <a name="network"></a>red

Etiqueta de la sección: `[network]`

| key | value | valor predeterminado | notas|
|:----|:----|:----|:----|
| generateHosts | boolean | `true` | `true` establece WSL para generar `/etc/hosts`. El archivo `hosts` contiene una asignación estática de direcciones IP correspondientes a nombres de host. |
| generateResolvConf | boolean | `true` | `true` establece WSL para generar `/etc/resolv.conf`. `resolv.conf` contiene una lista de DNS que es capaz de resolver un nombre de host determinado en su dirección IP. | 

#### <a name="interop"></a>interop

Etiqueta de la sección: `[interop]`

Estas opciones están disponibles en la compilación 17713 de Insider y versiones posteriores.

| key | value | valor predeterminado | notas|
|:----|:----|:----|:----|
| enabled | boolean | `true` | La configuración de esta clave determinará si WSL admitirá el inicio de procesos de Windows. |
| appendWindowsPath | boolean | `true` | Establecer esta clave determinará si WSL agregará elementos de ruta de acceso de Windows a la variable de entorno $PATH. | 
