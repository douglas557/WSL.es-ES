---
title: Administrar las distribuciones de Linux
description: Hacer referencia a enumerar y configurar varias distribuciones de Linux que se ejecuta en el subsistema de Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, windowssubsystem, ubuntu, wsl.conf, wslconfig
author: scooley
ms.author: scooley
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.openlocfilehash: a4f9649805051d9c1367fd5b0a5fe541d2d1e168
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040860"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a>Administrar y configurar el subsistema de Windows para Linux

> Se aplica a Windows 10 Fall Creators Update y versiones posteriores.  Consulte nuestra actualizada [Guía de instalación](./install_guide.md) para probar nuevas características de administración y empezar a ejecutar varias distribuciones de Linux desde Microsoft Store.

## <a name="ways-to-run-wsl"></a>Formas de iniciar WSL

Hay varias maneras de ejecutar Linux con el subsistema de Windows para Linux.

1. `[distro]`, por ejemplo `ubuntu`
1. `wsl.exe` o `bash.exe`
1. `wsl [command]` o `bash -c [command]`

Qué método debe usar dependerá de lo que está haciendo.

### <a name="launch-wsl-by-distribution"></a>Iniciar WSL según la distribución

Iniciar una distribución usando su aplicación específica inicia dicha distribución en su propia ventana de consola.

![Inicie WSL desde el menú Inicio](media/start-launch.png)

Es lo mismo que hacer clic en "Iniciar" en Microsoft Store.

![Iniciar WSL desde Microsoft Store](media/store-launch.png)

También puede ejecutar la distribución desde la línea de comandos ejecutando `[distribution].exe`.

La desventaja de la ejecución de una distribución desde la línea de comandos de esta manera es, que cambiará automáticamente el directorio de trabajo desde el directorio actual al directorio principal de la distribución.

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

### <a name="wsl-and-wsl-command"></a>wsl and wsl [command]

La mejor manera de ejecutar WSL desde la línea de comandos es usando `wsl.exe`.

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

No sólo hace `wsl` mantener el directorio de trabajo actual en su lugar, sino que le permite ejecutar un comando único junto a comandos de Windows.

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


## <a name="managing-multiple-linux-distributions"></a>Administrar varias distribuciones de Linux

### <a name="windows-10-version-1903-and-later"></a>Versión de Windows 10 1903 y versiones posterior

Puede usar `wsl.exe` para administrar sus distribuciones en el subsistema de Windows para Linux (WSL), incluido listar distribuciones disponibles, establecer una distribución como predeterminada y desinstalar una de las distribuciones.

Cada distribución de Linux administra independientemente sus propias configuraciones. Para ver los comandos específicos de distribución, ejecute `[distro.exe] /?`.  Por ejemplo, `ubuntu /?`.

#### <a name="list-distributions"></a>Lista de distribuciones

`wsl -l` , `wsl --list`  
Enumera todas las distribuciones de Linux disponibles en WSL. Si se muestra una distribución, es porque está instalada y lista para usarse.

`wsl --list --all`   
Enumera todas las distribuciones, incluidas las que no están actualmente disponibles, porque estén en el proceso de instalación, desinstalación, o se encuentran en un estado interrumpido.  

`wsl --list --running`   
Enumera todas las distribuciones que se están ejecutando actualmente.

#### <a name="set-a-default-distribution"></a>Configurar una distribución predeterminada

La distribución de WSL predeterminada es la que se ejecuta cuando se ejecuta `wsl` en una línea de comandos.

`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`

Establece la distribución predeterminada a `<DistributionName>`.

**Ejemplo:**  
`wsl -s Ubuntu` establece la distribución predeterminada a Ubuntu.  Ahora cuando se ejecute `wsl npm init` se ejecutará en Ubuntu.  Si se ejecuta `wsl` abrirá una sesión de Ubuntu.

#### <a name="unregister-and-reinstall-a-distribution"></a>Anular el registro y volver a instalar una distribución

Mientras las distribuciones de Linux se pueden instalar a través de Microsoft Store, no se pueden desinstalar a través de la misma. WSL Config permite anular el registro o desinstalar distribuciones.

Anular el registro también permite que las distribuciones puedan volver a instalarse.

> **Precaución:** Una vez que se anula el registro, se perderán permanentemente todos los datos, configuraciones y software asociados con esa distribución.  Volver a instalar desde la tienda, instalará una copia limpia de la distribución.

`wsl --unregister <DistributionName>`  
Anula el registro de la distribución de WSL por lo que puede volverse a instalar.

Por ejemplo: `wsl -unregister Ubuntu` quitaría Ubuntu desde las distribuciones disponibles en WSL.  Cuando se ejecute `wsl --list` no aparecerá en la lista.

Para volver a instalar, busque la distribución en Microsoft Store y seleccione "Iniciar".

#### <a name="run-as-a-specific-user"></a>Ejecutar como un usuario específico

`wsl -u <Username>`, `wsl --user <Username>`

Ejecute WSL como el usuario especificado. Tenga en cuenta que el usuario debe existir dentro de la distribución de WSL.

#### <a name="run-a-specific-distribution"></a>Ejecutar una distribución específica

`wsl --d <DistributionName>`, `wsl --distribution <DistributionName>`

Ejecutar una distribución de WSL especificada, puede usarse para enviar comandos a una distribución específica sin tener que cambiar su valor predeterminado.

### <a name="versions-earlier-than-windows-10-version-1903"></a>Versiones anteriores a Windows 10 versión 1903

WSL Config (`wslconfig.exe`) es una herramienta de línea de comandos para administrar las distribuciones de Linux que se ejecuta en el subsistema de Windows para Linux (WSL).  Permite enumerar distribuciones disponibles, establecer una distribución de forma predeterminada y desinstalar las distribuciones.

Mientras WSL Config es útil para configurar o coordinar las distribuciones, cada distribución de Linux administra independientemente sus propias configuraciones.  Para ver los comandos específicos de distribución, ejecute `[distro.exe] /?`.  Por ejemplo, `ubuntu /?`.

Para ver todas las opciones disponibles para wslconfig, ejecute:  `wslconfig /?`

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
Enumera todas las distribuciones de Linux disponibles en WSL. Si se muestra una distribución, es porque está instalada y lista para usarse.

`wslconfig /list /all`  
Enumera todas las distribuciones, incluidas las que no están actualmente disponibles, porque estén en el proceso de instalación, desinstalación, o se encuentran en un estado interrumpido.  

#### <a name="set-a-default-distribution"></a>Configurar una distribución predeterminada

La distribución de WSL predeterminada es la que se ejecuta cuando se ejecuta `wsl` en una línea de comandos.

`wslconfig /setdefault <DistributionName>`

La distribución predeterminada se establece a `<DistributionName>`.

**Ejemplo:**  
`wslconfig /setdefault Ubuntu` establece la distribución predeterminada a Ubuntu.  Ahora cuando se ejecute `wsl npm init` se ejecutará en Ubuntu.  Si se ejecuta `wsl` abrirá una sesión de Ubuntu.

#### <a name="unregister-and-reinstall-a-distribution"></a>Anular el registro y volver a instalar una distribución
Mientras las distribuciones de Linux se pueden instalar a través de Microsoft Store, no se pueden desinstalar a través de la misma. WSL Config permite anular el registro o desinstalar distribuciones.

Anular el registro también permite que las distribuciones puedan volver a instalarse.

> **Precaución:** Una vez que se anula el registro, se perderán permanentemente todos los datos, configuraciones y software asociados con esa distribución.  Volver a instalar desde la tienda, instalará una copia limpia de la distribución.

`wslconfig /unregister <DistributionName>`  
Anula el registro de la distribución de WSL por lo que puede volverse a instalar.

Por ejemplo: `wslconfig /unregister Ubuntu` quitaría Ubuntu desde las distribuciones disponibles en WSL.  Cuando se ejecute `wslconfig /list` no aparecerá en la lista.

Para volver a instalar, busque la distribución en Microsoft Store y seleccione "Iniciar".

## <a name="set-wsl-launch-settings"></a>Establecer la configuración de inicio WSL

> **Disponible en Windows Insider compilar 17093 y versiones posteriores**

Configure ciertas funcionalidades en WSL que se aplicarán automaticamente cada vez que inicie WSL con `wsl.conf`. 

Actualmente, esto incluye las opciones de montaje automático y la configuración de red.

`wsl.conf` se encuentra en cada distribución de Linux en `/etc/wsl.conf`. Si el archivo no está allí, puede ser creado manualmente. WSL detectará la existencia del archivo y leerá su contenido. Si el archivo falta o tiene un formato incorrecto (es decir, incorrecto formato de marcado), WSL se iniciará con normalidad.

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

De acuerdo con las convenciones. ini, las claves se declaran en una sección. 

WSL admite dos secciones: `automount` y `network`.

#### <a name="automount"></a>Automount

Sección: `[automount]`


| clave        | valor                          | valor predeterminado      | notas                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| enabled    | boolean                        | true         | `true` hace que las unidades de disco (como `C:/` o `D:/`) sean montadas automáticamente con DrvFs en `/mnt`.  `false` significa que las unidades no se montan automáticamente, pero todavía puede montarlas manualmente o a través de `fstab`.                                                                                                             |
| mountFsTab | boolean                        | true         | `true` establece que `/etc/fstab` debe procesarse en el inicio de WSL. / etc/fstab es un archivo donde se pueden declarar otros sistemas de archivos, como un recurso compartido SMB. Por lo tanto, puede montar estos sistemas de archivos automáticamente al iniciar WSL.                                                                                                                |
| root       | String                         | `/mnt/`      | Establece el directorio donde se monta automáticamente las unidades de disco. Por ejemplo, si tiene un directorio en WSL en `/windir/` y lo especifica como `root`, las unidades de disco se montarán  en `/windir/c`                                                                                              |
| options    | lista de valores separada por comas | vacio | Este valor se anexa a las opciones de montaje de DrvFs predeterminadas. **Solo se pueden usar opciones de DrvFs específicas.** No se admiten las opciones que el montaje binario podría convertir directamente en un flag. Si desea especificar explícitamente estas opciones, debe incluir cada unidad para el que desea hacerlo en/etc/fstab. De forma predeterminada, WSL establece el uid y gid en el valor del usuario predeterminado (en la distribución de Ubuntu, se crea el usuario predeterminado con uid = 1000, gid = 1000). Si el usuario especifica una opción de gid o uid explícitamente a través de esta clave, se sobrescribirá el valor asociado. En caso contrario, el valor predeterminado siempre se anexará. |

**Nota:** Estas opciones se aplican como las opciones de montaje para todas las unidades montadas automáticamente. Para cambiar las opciones para solo una unidad específica, use /etc/fstab en su lugar.

#### <a name="network"></a>Red

Etiqueta de sección: `[network]`

| clave | valor | valor predeterminado | notas|
|:----|:----|:----|:----|
| generateHosts | boolean | `true` | `true` establece WSL para generar `/etc/hosts`. El archivo `hosts`contiene un mapa estático de direcciones IP correspondientes con los nombres de host. |
| generateResolvConf | boolean | `true` | `true` establece WSL para generar `/etc/resolv.conf`. El archivo `resolv.conf` contiene una lista DNS que son capaces de resolver un nombre de host especificado a su dirección IP. | 

#### <a name="interop"></a>Interoperabilidad

Etiqueta de sección: `[interop]`

Estas opciones están disponibles en Insider Build 17713 y versiones posteriores.

| clave | valor | valor predeterminado | notas|
|:----|:----|:----|:----|
| enabled | boolean | `true` | Esta clave determinará si WSL admitirá iniciar procesos de Windows. |
| appendWindowsPath | boolean | `true` | Wsta clave determinará si WSL agregará elementos de la ruta de acceso de Windows a la variable de entorno $PATH. | 
