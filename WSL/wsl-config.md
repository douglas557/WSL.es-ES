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
ms.openlocfilehash: c806552750f413fcb75f989d868a57cc939af64a
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063503"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a>Administrar y configurar el subsistema de Windows para Linux

> Se aplica a Windows 10 Fall Creators Update y versiones posteriores.  Consulte nuestro actualizada [Guía de instalación](./install_guide.md) para probar nuevas características de administración y empezar a ejecutar varias distribuciones de Linux desde el Store de Windows.

## <a name="ways-to-run-wsl"></a>Modos de ejecutar WSL

Hay muchas maneras de ejecutar Linux con el subsistema de Windows para Linux.

1. `[distro]` ie `ubuntu`
1. `wsl.exe` o bien `bash.exe`
1. `wsl [command]` o bien `bash -c [command]`

Qué método debe usar depende de lo que está haciendo.

### <a name="launch-wsl-by-distribution"></a>Iniciar WSL según la distribución

Distribución en su propia ventana de consola inicia ejecutando una distribución mediante su aplicación específica de cada distribución.

![Inicie WSL desde el menú Inicio](media/start-launch.png)

Es el mismo que al hacer clic en "Iniciar" en el Store de Windows.

![Iniciar WSL desde el Store de Windows](media/store-launch.png)

También puede ejecutar la distribución de la línea de comandos ejecutando `[distribution].exe`.

La desventaja de la ejecución de una distribución de la línea de comandos de esta manera es que cambiará automáticamente el directorio de trabajo desde el directorio actual al directorio principal de la distribución.

**Por ejemplo:**

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

La mejor manera de ejecutar WSL desde la línea de comandos usa `wsl.exe`.

**Por ejemplo:**

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

No sólo hace `wsl` mantener el directorio de trabajo actual en su lugar, le permite ejecutar un comando único a lo largo de los comandos de Windows de lado.

**Por ejemplo:**

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

**Por ejemplo:**

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

Puede usar `wsl.exe` para administrar sus distribuciones en el subsistema de Windows para Linux (WSL), incluidos listado distribuciones disponibles, el establecimiento de una distribución de forma predeterminada y desinstalación de las distribuciones.

Cada distribución de Linux independiente administra sus propias configuraciones. Para ver los comandos específicos de distribución, ejecute `[distro.exe] /?`.  Por ejemplo, `ubuntu /?`.

#### <a name="list-distributions"></a>Distribuciones de lista

`wsl -l` , `wsl --list`  
Listas disponibles distribuciones de Linux disponibles en WSL.  Si se muestra una distribución, se instala y está lista para usarse.

`wsl --list --all`   
Enumera todas las distribuciones, las que no están actualmente utilizable incluidas.  Se puede estar en el proceso de instalar, desinstalar, o se encuentran en un estado interrumpido.  

`wsl --list --running`   
Enumera todas las distribuciones que se están ejecutando actualmente.

#### <a name="set-a-default-distribution"></a>Configurar una distribución predeterminada

La distribución de WSL predeterminada es la que se ejecuta cuando se ejecuta `wsl` en una línea de comandos.

`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`

La distribución predeterminada se establece en `<DistributionName>`.

**Por ejemplo:**  
`wsl -s Ubuntu` establecer la distribución de forma predeterminada en Ubuntu.  Ahora cuando ejecuto `wsl npm init` se ejecutará en Ubuntu.  Si ejecuto `wsl` abrirá una sesión de Ubuntu.

#### <a name="unregister-and-reinstall-a-distribution"></a>Anular el registro y volver a instalar una distribución

Mientras Linux distribuciones pueden instalarse a través de la Windows almacén, no se puede desinstalar a través de la tienda.  WSL Config permite distribuciones se anula el registro o desinstalado.

Al anular el registro también permite que las distribuciones deben volver a instalar.

> **Precaución:** Una vez que se anula el registro, se perderán permanentemente todos los datos, configuraciones y asociadas con esa distribución de software.  Volver a instalar desde el almacén se instalará una copia limpia de la distribución.

`wsl --unregister <DistributionName>`  
Anula el registro de la distribución de WSL por lo que puede volver a instalar o limpiado.

Por ejemplo: `wsl -unregister Ubuntu` quitarían Ubuntu desde las distribuciones disponibles en WSL.  Cuando ejecuto `wsl --list` no se mostrará.

Para volver a instalar, busque la distribución en el Store de Windows y seleccione "Iniciar".

#### <a name="run-as-a-specific-user"></a>Ejecutar como un usuario específico

`wsl -u <Username>`, `wsl --user <Username>`

Ejecute WSL como el usuario especificado. Tenga en cuenta que el usuario debe existir dentro de la distribución de WSL.

#### <a name="run-a-specific-distribution"></a>Ejecutar una distribución específica

`wsl --d <DistributionName>`, `wsl --distribution <DistributionName>`

Ejecutar una distribución de WSL especificada, puede usarse para enviar comandos a una distribución específica sin tener que cambiar su valor predeterminado.

### <a name="versions-earlier-than-windows-10-version-1903"></a>Versiones anteriores a Windows 10 versión 1903

Configuración de WSL (`wslconfig.exe`) es una herramienta de línea de comandos para administrar las distribuciones de Linux que se ejecuta en el subsistema de Windows para Linux (WSL).  Permite enumerar distribuciones disponibles, establecer una distribución de forma predeterminada y desinstalar las distribuciones.

Mientras WSL configuración es útil para los valores que abarcan o coordinan las distribuciones, cada distribución de Linux independiente administra sus propias configuraciones.  Para ver los comandos específicos de distribución, ejecute `[distro.exe] /?`.  Por ejemplo, `ubuntu /?`.

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

#### <a name="list-distributions"></a>Distribuciones de lista

`wslconfig /list`  
Listas disponibles distribuciones de Linux disponibles en WSL.  Si se muestra una distribución, se instala y está lista para usarse.

`wslconfig /list /all`  
Enumera todas las distribuciones, las que no están actualmente utilizable incluidas.  Se puede estar en el proceso de instalar, desinstalar, o se encuentran en un estado interrumpido.  

#### <a name="set-a-default-distribution"></a>Configurar una distribución predeterminada

La distribución de WSL predeterminada es la que se ejecuta cuando se ejecuta `wsl` en una línea de comandos.

`wslconfig /setdefault <DistributionName>`

La distribución predeterminada se establece en `<DistributionName>`.

**Por ejemplo:**  
`wslconfig /setdefault Ubuntu` establecer la distribución de forma predeterminada en Ubuntu.  Ahora cuando ejecuto `wsl npm init` se ejecutará en Ubuntu.  Si ejecuto `wsl` abrirá una sesión de Ubuntu.

#### <a name="unregister-and-reinstall-a-distribution"></a>Anular el registro y volver a instalar una distribución

Mientras Linux distribuciones pueden instalarse a través de la Windows almacén, no se puede desinstalar a través de la tienda.  WSL Config permite distribuciones se anula el registro o desinstalado.

Al anular el registro también permite que las distribuciones deben volver a instalar.

> **Precaución:** Una vez que se anula el registro, se perderán permanentemente todos los datos, configuraciones y asociadas con esa distribución de software.  Volver a instalar desde el almacén se instalará una copia limpia de la distribución.

`wslconfig /unregister <DistributionName>`  
Anula el registro de la distribución de WSL por lo que puede volver a instalar o limpiado.

Por ejemplo: `wslconfig /unregister Ubuntu` quitarían Ubuntu desde las distribuciones disponibles en WSL.  Cuando ejecuto `wslconfig /list` no se mostrará.

Para volver a instalar, busque la distribución en el Store de Windows y seleccione "Iniciar".

## <a name="set-wsl-launch-settings"></a>Establecer la configuración de inicio WSL

> **Disponible en Windows Insider compilar 17093 y versiones posteriores**

Configurar automáticamente cierta funcionalidad en WSL que se aplicarán cada vez que inicie el subsistema con `wsl.conf`. 

Derecha ahora, esto incluye las opciones de montaje automático y la configuración de red.

`wsl.conf` se encuentra en cada distribución de Linux en `/etc/wsl.conf`. Si el archivo no está allí, puede crearla usted. WSL detectará la existencia del archivo y leerá su contenido. Si el archivo falta o tiene un formato incorrecto (es decir, incorrecto marcado formato), continuará WSL iniciar con normalidad.

Este es un ejemplo `wsl.conf` archivo puede agregar a sus distribuciones:

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

#### <a name="automount"></a>Montaje automático

Sección: `[automount]`


| key        | value                          | valor predeterminado      | Notas de la                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| enabled    | boolean                        | true         | `true` hace que se ha corregido las unidades (como) `C:/` o `D:/`) que se monte automáticamente con DrvFs en `/mnt`.  `false` significa que las unidades no se montan automáticamente, pero todavía puede montarlas manualmente o a través de `fstab`.                                                                                                             |
| mountFsTab | boolean                        | true         | `true` establece `/etc/fstab` procesarse en el inicio de WSL. / etc/fstab es un archivo donde se pueden declarar otros sistemas de archivos, como un recurso compartido SMB. Por lo tanto, puede montar estos sistemas de archivos automáticamente en WSL inicio de la seguridad.                                                                                                                |
| root       | Cadena                         | `/mnt/`      | Establece el directorio de unidades de disco duro donde se monta automáticamente. Por ejemplo, si tiene un directorio en WSL en `/windir/` y especifique que como la raíz, esperaría ver las unidades de disco fijos montados en `/windir/c`                                                                                              |
| opciones    | lista separada por comas de valores | Cadena vacía | Este valor se anexa a la cadena de opciones de montaje de DrvFs predeterminada. **Se pueden especificar solo las opciones de DrvFs específicas.** No se admiten las opciones que el montaje binario podría analizar normalmente en una marca. Si desea especificar explícitamente estas opciones, debe incluir cada unidad para el que desea hacerlo en/etc/fstab. |

De forma predeterminada, WSL establece el uid y gid en el valor del usuario predeterminado (en la distribución de Ubuntu, se crea el usuario predeterminado con uid = 1000, gid = 1000). Si el usuario especifica una opción de gid o uid explícitamente a través de esta clave, se sobrescribirá el valor asociado. En caso contrario, el valor predeterminado siempre se anexará.

**Nota:** Estas opciones se aplican como las opciones de montaje para todas las unidades montadas automáticamente. Para cambiar las opciones para solo una unidad específica, use/etc/fstab en su lugar.

#### <a name="network"></a>red

Etiqueta de sección: `[network]`

| key | value | valor predeterminado | Notas de la|
|:----|:----|:----|:----|
| generateHosts | boolean | `true` | `true` establece WSL para generar `/etc/hosts`. El `hosts` archivo contiene un mapa estático de direcciones IP correspondientes de los nombres de host. |
| generateResolvConf | boolean | `true` | `true` establecer WSL para generar `/etc/resolv.conf`. El `resolv.conf` contiene una lista DNS que son capaces de resolver un nombre de host especificado en su dirección IP. | 

#### <a name="interop"></a>Interoperabilidad

Etiqueta de sección: `[interop]`

Estas opciones están disponibles en Insider 17713 de compilación y versiones posteriores.

| key | value | valor predeterminado | Notas de la|
|:----|:----|:----|:----|
| enabled | boolean | `true` | Al definir esta clave determinará si WSL admitirá al iniciar los procesos de Windows. |
| appendWindowsPath | boolean | `true` | Al definir esta clave determinará si WSL agregará elementos de la ruta de acceso de Windows a la variable de entorno $PATH. | 
