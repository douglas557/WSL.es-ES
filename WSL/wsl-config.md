---
title: Administración de distribuciones de Linux
description: Haga una lista de las distintas distribuciones de Linux que se ejecutan en el subsistema de Windows para Linux.
keywords: BashOnWindows, bash, WSL, Windows, subsistema de Windows para Linux, windowssubsystem, Ubuntu, WSL. conf, wslconfig
author: scooley
ms.author: scooley
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.openlocfilehash: 0c9f9315b17d5156aa111e7619ee25534653b27e
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499278"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a>Administrar y configurar el subsistema de Windows para Linux

> Se aplica a Windows 10 Fall Creators Update y versiones posteriores.  Consulte nuestra [Guía de instalación](./install_guide.md) actualizada para probar nuevas características de administración y comenzar a ejecutar varias distribuciones de Linux desde Microsoft Store.

## <a name="ways-to-run-wsl"></a>Formas de iniciar WSL

Hay varias maneras de ejecutar Linux con el subsistema de Windows para Linux.

1. `[distro]`, por ejemplo`ubuntu`
1. `wsl.exe` o `bash.exe`
1. `wsl [command]` o `bash -c [command]`

El método que debe usar dependerá de lo que está haciendo.

### <a name="launch-wsl-by-distribution"></a>Iniciar WSL por distribución

Si se inicia una distribución usando su aplicación específica, se inicia dicha distribución en su propia ventana de consola.

![Iniciar WSL desde el menú Inicio](media/start-launch.png)

Es lo mismo que hacer clic en "iniciar" en Microsoft Store.

![Inicio de WSL desde Microsoft Store](media/store-launch.png)

También puede ejecutar la distribución desde la línea de comandos ejecutando `[distribution].exe`.

La desventaja de la ejecución de una distribución desde la línea de comandos de esta manera es que cambiará automáticamente el directorio de trabajo desde el directorio actual al directorio principal de la distribución.

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

### <a name="wsl-and-wsl-command"></a>WSL y WSL [comando]

La mejor manera de ejecutar WSL desde la línea de comandos es usando  `wsl.exe`.

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

Con `wsl` no solo puede mantener el directorio de trabajo actual implementado, sino que además le permite ejecutar un comando único junto a comandos de Windows.

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

### <a name="windows-10-version-1903-and-later"></a>Windows 10 versión 1903 y versiones posteriores

Puede usar `wsl.exe` para administrar sus distribuciones en el subsistema de Windows para Linux (WSL), incluido enumerar las distribuciones disponibles, establecer una distribución como predeterminada y desinstalar distribuciones.

Cada distribución de Linux administra independientemente sus propias configuraciones. Para ver los comandos específicos de distribución, ejecute `[distro.exe] /?`.  Por ejemplo, `ubuntu /?`.

#### <a name="list-distributions"></a>Lista de distribuciones

`wsl -l` , `wsl --list`  
Enumera todas las distribuciones de Linux disponibles en WSL.  Si se muestra una distribución, es porque está instalada y lista para usarse.

`wsl --list --all`   
Muestra todas las distribuciones, incluidas las que no se pueden usar actualmente.  Pueden encontrarse en el proceso de instalación, desinstalación o en un estado interrumpido.  

`wsl --list --running`   
Muestra todas las distribuciones que se están ejecutando actualmente.

#### <a name="set-a-default-distribution"></a>Establecer una distribución predeterminada

La distribución WSL predeterminada es la que se ejecuta cuando se ejecuta `wsl` en una línea de comandos.

`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`

Establece la distribución predeterminada en `<DistributionName>`.

**Ejemplo:**  
`wsl -s Ubuntu` establece la distribución predeterminada en Ubuntu.  Ahora cuando se ejecute`wsl npm init` , se ejecutará en Ubuntu.  Si ejecuto `wsl` , se abrirá una sesión de Ubuntu.

#### <a name="unregister-and-reinstall-a-distribution"></a>Anular el registro y reinstalar una distribución

Aunque las distribuciones de Linux se pueden instalar a través de Microsoft Store, no se pueden desinstalar a través de la tienda.  WSL Config permite anular el registro o desinstalar distribuciones.

Al anular el registro, también se permite que las distribuciones puedan volver a instalarse.

> **Atención:** Una vez que se anule el registro, se perderán permanentemente todos los datos, configuraciones y software asociados con esa distribución.  Si se vuelve a instalar desde la tienda, se instalará una copia limpia de la distribución.

`wsl --unregister <DistributionName>`  
Anula el registro de la distribución de WSL para que se pueda volver a instalar y limpiar.

Por ejemplo: `wsl --unregister Ubuntu` quitaría Ubuntu de las distribuciones disponibles en WSL.  Cuando se ejecute `wsl --list` no aparecerá en la lista.

Para volver a instalar, busque la distribución en Microsoft Store y seleccione "iniciar".

#### <a name="run-as-a-specific-user"></a>Ejecutar como un usuario específico

`wsl -u <Username>`, `wsl --user <Username>`

Ejecute WSL como el usuario especificado. Tenga en cuenta que el usuario debe existir dentro de la distribución de WSL.

#### <a name="run-a-specific-distribution"></a>Ejecutar una distribución específica

`wsl --d <DistributionName>`, `wsl --distribution <DistributionName>`

Ejecutar una distribución especificada de WSL, se puede usar para enviar comandos a una distribución específica sin tener que cambiar el valor predeterminado.

### <a name="versions-earlier-than-windows-10-version-1903"></a>Versiones anteriores a la versión 1903 de Windows 10

WSL Config (`wslconfig.exe`) es una herramienta de línea de comandos para administrar las distribuciones de Linux y que se ejecuta en el subsistema de Windows para Linux (WSL).  Permite enumerar las distribuciones disponibles, establecer una distribución predeterminada y desinstalar distribuciones.

Mientras que WSL Config resulta útil para la configuración que se relaciona con las distribuciones o las coordina, cada distribución de Linux administra independientemente sus propias configuraciones.  Para ver los comandos específicos de distribución, ejecute `[distro.exe] /?`.  Por ejemplo, `ubuntu /?`.

Para ver todas las opciones disponibles para wslconfig, ejecute:`wslconfig /?`

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

#### <a name="list-distributions"></a>Lista de distribuciones

`wslconfig /list`  
Enumera todas las distribuciones de Linux disponibles en WSL.  Si se muestra una distribución, es porque está instalada y lista para usarse.

`wslconfig /list /all`  
Muestra todas las distribuciones, incluidas las que no se pueden usar actualmente.  Pueden encontrarse en el proceso de instalación, desinstalación o en un estado interrumpido.  

#### <a name="set-a-default-distribution"></a>Establecer una distribución predeterminada

La distribución WSL predeterminada es la que se ejecuta cuando se ejecuta `wsl` en una línea de comandos.

`wslconfig /setdefault <DistributionName>`

Establece la distribución predeterminada en `<DistributionName>`.

**Ejemplo:**  
`wslconfig /setdefault Ubuntu` establece la distribución predeterminada en Ubuntu.  Ahora cuando se ejecute`wsl npm init` , se ejecutará en Ubuntu.  Si ejecuto `wsl` , se abrirá una sesión de Ubuntu.

#### <a name="unregister-and-reinstall-a-distribution"></a>Anular el registro y reinstalar una distribución

Aunque las distribuciones de Linux se pueden instalar a través de Microsoft Store, no se pueden desinstalar a través de la tienda.  WSL Config permite anular el registro o desinstalar distribuciones.

Al anular el registro, también se permite que las distribuciones puedan volver a instalarse.

> **Atención:** Una vez que se anule el registro, se perderán permanentemente todos los datos, configuraciones y software asociados con esa distribución.  Si se vuelve a instalar desde la tienda, se instalará una copia limpia de la distribución.

`wslconfig /unregister <DistributionName>`  
Anula el registro de la distribución de WSL para que se pueda volver a instalar y limpiar.

Por ejemplo: `wslconfig /unregister Ubuntu` quitaría Ubuntu de las distribuciones disponibles en WSL.  Cuando se ejecute `wslconfig /list` no aparecerá en la lista.

Para volver a instalar, busque la distribución en Microsoft Store y seleccione "iniciar".

## <a name="set-wsl-launch-settings"></a>Establecimiento de la configuración de inicio de WSL

> **Disponible en Windows Insider Build 17093 y versiones posteriores**

Configure automáticamente ciertas funcionalidades en WSL que se aplicarán cada vez que inicie el subsistema con`wsl.conf`. 

Actualmente, esto incluye las opciones de montaje automático y la configuración de red.

`wsl.conf`se encuentra en cada distribución de Linux `/etc/wsl.conf`en. Si el archivo no está allí, puede crearse manualmente. WSL detectará la existencia del archivo y leerá su contenido. Si el archivo falta o tiene un formato incorrecto (es decir, el formato de marcado es incorrecto), WSL se iniciará con normalidad de todos modos.

Este es un archivo de ejemplo `wsl.conf` que puede agregar a sus distribuciones:

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

En el mantenimiento de las convenciones de. ini, las claves se declaran en una sección. 

WSL admite dos secciones: `automount` y `network`.

#### <a name="automount"></a>Automount

Transversal`[automount]`


| clave        | valor                          | valor predeterminado      | notas                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| enabled    | booleano                        | true         | `true`hace que las unidades fijas (es decir, `C:/`o `D:/`) que se va a montar automáticamente con `/mnt`DrvFs en.  `false`significa que las unidades no se montarán automáticamente, pero podría montarlas de forma `fstab`manual o a través de.                                                                                                             |
| mountFsTab | booleano                        | true         | `true`conjuntos `/etc/fstab` que se van a procesar en el inicio de WSL. /etc/fstab es un archivo donde puede declarar otros sistemas de archivos, como un recurso compartido de SMB. Por lo tanto, puede montar estos sistemas de archivos automáticamente en WSL en el inicio.                                                                                                                |
| raíces       | Cadena                         | `/mnt/`      | Establece el directorio donde se montarán automáticamente las unidades fijas. Por ejemplo, si tiene un directorio en WSL en `/windir/` y especifica que como raíz, esperaría ver las unidades fijas montadas en`/windir/c`                                                                                              |
| opciones    | lista de valores separados por comas | cadena vacía | Este valor se anexa a la cadena predeterminada de opciones de montaje de DrvFs. **Solo se pueden especificar opciones específicas de DrvFs.** No se admiten las opciones que el binario de montaje analizaría normalmente en una marca. Si desea especificar explícitamente esas opciones, debe incluir cada unidad para la que desee hacerlo en/etc/fstab. |

De forma predeterminada, WSL establece UID y GID en el valor del usuario predeterminado (en Ubuntu distribución, el usuario predeterminado se crea con UID = 1000, gid = 1000). Si el usuario especifica una opción GID o UID explícitamente a través de esta clave, se sobrescribirá el valor asociado. De lo contrario, siempre se anexará el valor predeterminado.

**Nota:** Estas opciones se aplican como opciones de montaje para todas las unidades montadas automáticamente. Para cambiar las opciones para solo una unidad específica, use /etc/fstab en su lugar.

#### <a name="network"></a>network

Etiqueta de la sección:`[network]`

| clave | valor | valor predeterminado | notas|
|:----|:----|:----|:----|
| generateHosts | booleano | `true` | `true` hace que WSL genere `/etc/hosts`. El archivo`hosts` contiene un mapa estático de direcciones IP correspondientes con los nombres de host. |
| generateResolvConf | booleano | `true` | `true` hace que WSL genere `/etc/resolv.conf`. El archivo`resolv.conf` contiene una lista de DNS que son capaces de resolver un nombre de host especificado a su dirección IP. | 

#### <a name="interop"></a>opera

Etiqueta de la sección:`[interop]`

Estas opciones están disponibles en la compilación 17713 de Insider y las versiones posteriores.

| clave | valor | valor predeterminado | notas|
|:----|:----|:----|:----|
| enabled | booleano | `true` | El establecimiento de esta clave determinará si WSL admite el inicio de procesos de Windows. |
| appendWindowsPath | booleano | `true` | El establecimiento de esta clave determinará si WSL agregará elementos de la ruta de acceso de Windows a la variable de entorno $PATH. | 
