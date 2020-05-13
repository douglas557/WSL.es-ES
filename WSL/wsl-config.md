---
title: Administrar distribuciones de Linux
description: Lista de referencia y configuración de varias distribuciones de Linux que se ejecutan en el subsistema de Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, subsistemawindows, ubuntu, wsl.conf, wslconfig
ms.date: 05/12/2020
ms.topic: article
ms.openlocfilehash: 59419919be138a20ab57e1a6d26a411e1531bf9f
ms.sourcegitcommit: 3fb40fd65b34a5eb26b213a0df6a3b2746b7a9b4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2020
ms.locfileid: "83235903"
---
# <a name="wsl-commands-and-launch-configurations"></a>Comandos WSL y configuraciones de inicio

## <a name="ways-to-run-wsl"></a>Formas de ejecutar WSL

Hay varias maneras de ejecutar una distribución de Linux con WSL una vez [instalado](install-win10.md).

1. Abra la distribución de Linux; para ello, vaya al menú Inicio de Windows y escriba el nombre de las distribuciones instaladas. Por ejemplo: "Ubuntu".
2. En el símbolo del sistema de Windows o PowerShell, escriba el nombre de la distribución instalada. Por ejemplo: `ubuntu`
3. Desde el símbolo del sistema de Windows o PowerShell, para abrir la distribución de Linux predeterminada dentro de la línea de comandos actual, escriba: `wsl.exe` .
4. Desde el símbolo del sistema de Windows o PowerShell, para abrir la distribución de Linux predeterminada dentro de la línea de comandos actual, escriba: `wsl [command]` .

El método que deba usar dependerá de lo que esté haciendo. Si ha abierto una línea de comandos de WSL en un símbolo del sistema de Windows o en una ventana de PowerShell y desea salir, escriba el comando: `exit` .

## <a name="launch-wsl-by-distribution"></a>Iniciar WSL por distribución

La ejecución de una distribución mediante su aplicación específica de distribución inicia esa distribución en su propia ventana de la consola.

![Iniciar WSL desde el menú Inicio](media/start-launch.png)

Es lo mismo que hacer clic en "Iniciar" en Microsoft Store.

![Iniciar WSL desde Microsoft Store](media/store-launch.png)

También puedes ejecutar la distribución desde la línea de comandos ejecutando `[distribution].exe`.

El inconveniente de ejecutar una distribución desde la línea de comandos de esta manera es que cambiará automáticamente el directorio de trabajo del directorio actual al directorio principal de la distribución.

**Ejemplo: (con PowerShell)**

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

**Ejemplo: (con PowerShell)**

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

**Ejemplo: (con PowerShell)**

```console
PS C:\Users\sarah> Get-Date

Sunday, March 11, 2018 7:54:05 PM

PS C:\Users\sarah> wsl
scooley@scooley-elmer:/mnt/c/Users/sarah$ date
Sun Mar 11 19:55:47 DST 2018
scooley@scooley-elmer:/mnt/c/Users/sarah$ exit
logout

PS C:\Users\sarah> wsl date
Sun Mar 11 19:56:57 DST 2018
```

**Ejemplo: (con PowerShell)**

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

En Windows 10 versión 1903 [y versiones posteriores](ms-settings:windowsupdate), puede usar `wsl.exe` para administrar las distribuciones en el subsistema de Windows para Linux (WSL), incluida la lista de distribuciones disponibles, la configuración de una distribución predeterminada y la desinstalación de distribuciones.

Cada distribución de Linux administra de forma independiente sus propias configuraciones. Para ver los comandos específicos de la distribución, ejecuta `[distro.exe] /?`.  Por ejemplo, `ubuntu /?`.

## <a name="list-distributions"></a>Enumerar distribuciones

`wsl -l` , `wsl --list`  
Enumera las distribuciones de Linux disponibles para WSL.  Si se enumera una distribución, está instalada y lista para usar.

`wsl --list --all`Muestra todas las distribuciones, incluidas las que no se pueden usar actualmente.  Pueden encontrarse en proceso de instalación, desinstalación o tener un estado interrumpido.  

`wsl --list --running`Muestra todas las distribuciones que se están ejecutando actualmente.

## <a name="set-a-default-distribution"></a>Establecer una distribución predeterminada

La distribución de WSL predeterminada es la que se ejecuta cuando se ejecuta `wsl` en una línea de comandos.

`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`

Establece la distribución predeterminada en `<DistributionName>`.

**Ejemplo: (con PowerShell)**  
`wsl -s Ubuntu` establecería la distribución predeterminada en Ubuntu.  Ahora, al ejecutar `wsl npm init`, se ejecutará en Ubuntu.  Si se ejecuta `wsl`, se abrirá una sesión de Ubuntu.

## <a name="unregister-and-reinstall-a-distribution"></a>Anular el registro de una distribución y reinstalarla

Aunque las distribuciones de Linux se pueden instalar a través de Microsoft Store, no se pueden desinstalar a través de Store.  WSL Config permite anular el registro de las distribuciones o desinstalarlas.

La anulación del registro también permite volver a instalar las distribuciones.

> **PRECAUCIÓN:** Una vez que se ha anulado el registro, todos los datos, la configuración y el software asociados a esa distribución se perderán de forma permanente.  Si se vuelve a instalar desde Store, se instalará una copia limpia de la distribución.

`wsl --unregister <DistributionName>`  
Anula el registro de la distribución de WSL para que se pueda volver a instalar o limpiar.

Por ejemplo: `wsl --unregister Ubuntu` quitaría Ubuntu de las distribuciones disponibles en WSL.  Al ejecutar `wsl --list`, no aparecerá en la lista.

Para reinstalar, busque la distribución en Microsoft Store y seleccione "Iniciar".

## <a name="run-as-a-specific-user"></a>Ejecutar como usuario específico

`wsl -u <Username>`, `wsl --user <Username>`

Ejecuta WSL como el usuario especificado. Ten en cuenta que el usuario debe existir dentro de la distribución de WSL.

## <a name="run-a-specific-distribution"></a>Ejecutar una distribución específica

`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`

Ejecuta una distribución especificada de WSL, se puede usar para enviar comandos a una distribución específica sin tener que cambiar la predeterminada.

## <a name="managing-multiple-linux-distributions-in-earlier-windows-versions"></a>Administración de varias distribuciones de Linux en versiones anteriores de Windows

En Windows 10 anterior a la versión 1903, `wslconfig.exe` se debe usar la herramienta de línea de comandos WSL config () para administrar las distribuciones de Linux que se ejecutan en el subsistema de Windows para Linux (WSL).  Te permite enumerar las distribuciones disponibles, establecer una distribución predeterminada y desinstalar las distribuciones.

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

Para enumerar las distribuciones, use:

`wslconfig /list`  
Enumera las distribuciones de Linux disponibles para WSL.  Si se enumera una distribución, está instalada y lista para usar.

`wslconfig /list /all`  
Enumera todas las distribuciones, incluidas las que no se pueden usar actualmente.  Pueden encontrarse en proceso de instalación, desinstalación o tener un estado interrumpido.  

Para establecer una distribución predeterminada que se ejecuta cuando se ejecuta `wsl` en una línea de comandos:

`wslconfig /setdefault <DistributionName>`Establece la distribución predeterminada en `<DistributionName>` .

**Ejemplo: (con PowerShell)**  
`wslconfig /setdefault Ubuntu` establecería la distribución predeterminada en Ubuntu.  Ahora, al ejecutar `wsl npm init`, se ejecutará en Ubuntu.  Si se ejecuta `wsl`, se abrirá una sesión de Ubuntu.

Para anular el registro y reinstalar una distribución:

`wslconfig /unregister <DistributionName>`  
Anula el registro de la distribución de WSL para que se pueda volver a instalar o limpiar.

Por ejemplo: `wslconfig /unregister Ubuntu` quitaría Ubuntu de las distribuciones disponibles en WSL.  Al ejecutar `wslconfig /list`, no aparecerá en la lista.

Para reinstalar, busque la distribución en Microsoft Store y seleccione "Iniciar".

## <a name="configure-per-distro-launch-settings-with-wslconf"></a>Configurar por configuración de inicio de distribución con wslconf

> **Disponible en Windows Build 17093 y versiones posteriores**

Configura automáticamente cierta funcionalidad en WSL que se aplicará cada vez que inicies el subsistema mediante `wsl.conf`.

En este momento, esto incluye opciones de montaje automático y configuración de red.

`wsl.conf` se encuentra en cada distribución de Linux en `/etc/wsl.conf`. Si el archivo no está allí, puedes crearlo tú mismo. WSL detectará la existencia del archivo y leerá su contenido. Si falta el archivo o tiene un formato incorrecto (es decir, un formato de marcado incorrecto), WSL se iniciará de manera normal.

A continuación se muestra un archivo de ejemplo `wsl.conf` que se puede Agregar a las distribuciones:

```console
# Enable extra metadata options by default
[automount]
enabled = true
root = /windir/
options = "metadata,umask=22,fmask=11"
mountFsTab = false

# Enable DNS – even though these are turned on by default, we'll specify here just to be explicit.
[network]
generateHosts = true
generateResolvConf = true
```

### <a name="configuration-options"></a>Opciones de configuración

En concordancia con las convenciones de .ini, las claves se declaran en una sección. 

WSL admite dos secciones: `automount` y `network`.

#### <a name="automount"></a>automount

Sección: `[automount]`

| key        | value                          | default      | HDInsight                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| enabled    | boolean                        | true         | `true` hace que las unidades fijas (es decir, `C:/` o `D:/`) se monten automáticamente con DrvFs en `/mnt`.  `false`significa que las unidades no se montarán automáticamente, pero podría montarlas de forma manual o a través de `fstab` .                                                                                                             |
| mountFsTab | boolean                        | true         | `true` establece `/etc/fstab` para que se procese en el inicio de WSL. /etc/fstab es un archivo donde puedes declarar otros sistemas de archivos, como un recurso compartido de SMB. Por lo tanto, puedes montar estos sistemas de archivos automáticamente en WSL en el inicio.                                                                                                                |
| root       | String                         | `/mnt/`      | Establece el directorio donde se montarán automáticamente las unidades fijas. Por ejemplo, si tienes un directorio en WSL en `/windir/` y lo especificas como raíz, esperarías ver que las unidades fijas se monten en `/windir/c`                                                                                              |
| opciones    | lista de valores separados por comas | cadena vacía | Este valor se anexa a la cadena predeterminada de opciones de montaje de DrvFs. **Solo se pueden especificar opciones específicas de DrvFs.** No se admiten las opciones que el binario de montaje analizaría normalmente en una marca. Si quieres especificar explícitamente esas opciones, tienes que incluir en /etc/fstab cada unidad para la que quieras hacerlo. |

De manera predeterminada, WSL establece uid y gid en el valor del usuario predeterminado (en una distribución de Ubuntu, el usuario predeterminado se crea con uid=1000,gid=1000). Si el usuario especifica una opción gid o uid explícitamente a través de esta clave, se sobrescribirá el valor asociado. De lo contrario, siempre se anexará el valor predeterminado.

**Nota:** Estas opciones se aplican como opciones de montaje para todas las unidades montadas automáticamente. Para cambiar las opciones solo para una unidad específica, usa /etc/fstab en su lugar.

#### <a name="mount-options"></a>Opciones de montaje

Establecer diferentes opciones de montaje para las unidades de Windows (DrvFs) puede controlar cómo se calculan los permisos de archivo para los archivos de Windows. Están disponibles las siguientes opciones:

| Clave | Descripción | Default |
|:----|:----|:----|
|uid| Id. de usuario que se usa para el propietario de todos los archivos | Id. de usuario predeterminado de su distribución WSL (en la primera instalación, el valor predeterminado es 1000)
|gid| Id. de grupo que se usa para el propietario de todos los archivos | Id. de grupo predeterminado de su distribución WSL (en la primera instalación, el valor predeterminado es 1000)
|umask | Máscara octal de permisos que se van a excluir para todos los archivos y directorios | 000
|fmask | Máscara octal de permisos que se van a excluir para todos los archivos | 000
|dmask | Máscara octal de permisos que se van a excluir para todos los directorios | 000

**Nota:** Las máscaras de permisos se colocan a través de una operación OR lógica antes de aplicarse a archivos o directorios. 

#### <a name="network"></a>red

Etiqueta de la sección: `[network]`

| key | value | default | HDInsight|
|:----|:----|:----|:----|
| generateHosts | boolean | `true` | `true` establece WSL para generar `/etc/hosts`. El archivo `hosts` contiene una asignación estática de direcciones IP correspondientes a nombres de host. |
| generateResolvConf | boolean | `true` | `true` establece WSL para generar `/etc/resolv.conf`. `resolv.conf` contiene una lista de DNS que es capaz de resolver un nombre de host determinado en su dirección IP. | 

#### <a name="interop"></a>interop

Etiqueta de la sección: `[interop]`

Estas opciones están disponibles en la compilación 17713 de Insider y versiones posteriores.

| key | value | default | HDInsight|
|:----|:----|:----|:----|
| enabled | boolean | `true` | La configuración de esta clave determinará si WSL admitirá el inicio de procesos de Windows. |
| appendWindowsPath | boolean | `true` | Establecer esta clave determinará si WSL agregará elementos de ruta de acceso de Windows a la variable de entorno $PATH. |

#### <a name="user"></a>usuario

Etiqueta de la sección: `[user]`

Estas opciones están disponibles en la compilación 18980 y versiones posteriores.

| key | value | default | HDInsight|
|:----|:----|:----|:----|
| default | string | El nombre de usuario inicial creado en la primera ejecución | Al establecer esta clave, se especifica el usuario que se debe ejecutar como cuando se inicia por primera vez una sesión de WSL. |

## <a name="configure-global-options-with-wslconfig"></a>Configurar opciones globales con. wslconfig

> **Disponible en Windows Build 19041 y versiones posteriores**

Puede configurar las opciones de WSL globales colocando un `.wslconfig` archivo en el directorio raíz de la carpeta de los usuarios: `C:\Users\<yourUserName>\.wslconfig` . Este archivo puede contener las siguientes opciones:

### <a name="wsl-2-settings"></a>Configuración de WSL 2

Esta configuración afecta a la máquina virtual que alimenta cualquier distribución de WSL 2. 

| key | value | default | HDInsight|
|:----|:----|:----|:----|
| kernel | string | Bandeja de entrada proporcionada por el kernel de Microsoft | Una ruta de acceso de Windows absoluta a un kernel de Linux personalizado. |
| memoria | tamaño | 80% de la memoria total en Windows | Cantidad de memoria que se va a asignar a la máquina virtual WSL 2. |
| procesadores | number | El mismo número de procesadores en Windows | El número de procesadores que se asignan a la máquina virtual WSL 2. |
| localhostForwarding | boolean | `true` | Valor booleano que especifica si los puertos enlazados a un carácter comodín o localhost en la máquina virtual WSL 2 deben poder conectarse desde el host a través de localhost: Port. |
| kernelCommandLine | string | En blanco | Argumentos adicionales de la línea de comandos del kernel. |
| swap | tamaño | 25% de tamaño de memoria en Windows redondeado a los GB más cercanos | Cantidad de espacio de intercambio que se va a agregar a la máquina virtual WSL 2, 0 para ningún archivo de intercambio. |
| Intercambio | tamaño | %USERPROFILE%\AppData\Local\Temp\swap.vhdx | Una ruta de acceso de Windows absoluta al disco duro virtual de intercambio. |

Las entradas con el `path` valor deben ser rutas de acceso de Windows con barras diagonales inversas de escape; por ejemplo:`C:\\Temp\\myCustomKernel`

Las entradas con el `size` valor deben ser de un tamaño seguido de una unidad, por ejemplo, `8GB` o `512MB` .