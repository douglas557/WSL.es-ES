---
title: Interoperabilidad de Windows con Linux
description: Describe la interoperabilidad de Windows con distribuciones de Linux que se ejecutan en el subsistema de Windows para Linux.
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 8e3568e4ca94f9b381b7827a237c2b637b97ae57
ms.sourcegitcommit: b15b847b87d29a40de4a1517315949bce9c7a3d5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "91413076"
---
# <a name="windows-interoperability-with-linux"></a>Interoperabilidad de Windows con Linux

El subsistema de Windows para Linux (WSL) está mejorando continuamente la integración entre Windows y Linux.  Se puede hacer lo siguiente:

* Ejecuta las herramientas de Windows (por ejemplo, notepad.exe) desde una línea de comandos de Linux (por ejemplo, Ubuntu).
* Ejecuta herramientas de Linux (por ejemplo, grep) desde una línea de comandos de Windows (por ejemplo, PowerShell).
* Comparte las variables de entorno entre Linux y Windows. (Compilación 17063 o posterior)

> [!NOTE]
> Si ejecutas Creators Update (octubre de 2017, compilación 16299) o la Actualización de aniversario (agosto de 2016, compilación 14393), ve a las [versiones anteriores de Windows 10](#earlier-versions-of-windows-10).

## <a name="run-linux-tools-from-a-windows-command-line"></a>Ejecución de herramientas de Linux desde una línea de comandos de Windows

Ejecuta los archivos binarios de Linux desde el símbolo del sistema de Windows (CMD) o PowerShell mediante `wsl <command>` (o `wsl.exe <command>`).

Por ejemplo:

```powershell
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

Los archivos binarios se invocan de esta manera:

* Usan el mismo directorio de trabajo que el símbolo del sistema actual de CMD o PowerShell.
* Se ejecutan como usuario predeterminado de WSL.
* Tienen los mismos derechos administrativos de Windows que el terminal y el proceso de llamada.

El comando de Linux que sigue a `wsl` (o `wsl.exe`) se controla como cualquier comando que se ejecute en WSL.  Funcionan cosas como sudo, canalizaciones y redireccionamientos de archivos.

Ejemplo de uso de sudo para actualizar la distribución de Linux predeterminada:

```powershell
C:\temp> wsl sudo apt-get update
```

Después de ejecutar este comando, se mostrará el nombre de usuario predeterminado de la distribución de Linux y se te pedirá la contraseña. Después de escribir la contraseña correctamente, la distribución descargará las actualizaciones.

## <a name="mixing-linux-and-windows-commands"></a>Combinación de comandos de Windows y Linux

Estos son algunos ejemplos de la combinación de comandos de Linux y Windows mediante PowerShell.

Para usar el comando de Linux `ls -la` para enumerar archivos y el comando de PowerShell `findstr` para filtrar los resultados de las palabras que contienen "git", combina los comandos siguientes:

```powershell
wsl ls -la | findstr "git"
```

Para usar el comando de PowerShell `dir` para enumerar archivos y el comando de Linux `grep` para filtrar los resultados de las palabras que contienen "git", combina los comandos siguientes:

```powershell
C:\temp> dir | wsl grep git
```

Para usar el comando de Linux `ls -la` para enumerar archivos y el comando de PowerShell `> out.txt` para imprimir esa lista en un archivo de texto denominado "out.txt", combina los comandos siguientes:

```powershell
C:\temp> wsl ls -la > out.txt
```

Los comandos pasados a `wsl.exe` se reenvían al proceso de WSL sin modificaciones.  Las rutas de acceso de archivo deben especificarse en el formato de WSL.

Para usar el comando de Linux `ls -la` para enumerar los archivos de la ruta de acceso del sistema de archivos de Linux `/proc/cpuinfo` mediante PowerShell, utiliza el siguiente comando:

```powershell
C:\temp> wsl ls -la /proc/cpuinfo
```

Para usar el comando de Linux `ls -la` para enumerar los archivos de la ruta de acceso del sistema de archivos de Windows `C:\Program Files` mediante PowerShell, utiliza el siguiente comando:

```powershell
C:\temp> wsl ls -la "/mnt/c/Program Files"
```

## <a name="run-windows-tools-from-linux"></a>Ejecución de herramientas de Windows desde Linux

WSL puede ejecutar herramientas de Windows directamente desde la línea de comandos de WSL mediante `[tool-name].exe`.  Por ejemplo, `notepad.exe`.

<!-- Craig - could you help add a section with an example here to explain this scenario: "To access your Linux files using a Windows tool, use `\\wsl$\<distroName>\'` as the file path." Currently it I can just enter `notepad.exe foo.txt` and it seems to work fine, so explaining a situation where the file path is needed would be helpful. -->

Las aplicaciones que se ejecutan de esta manera tienen las siguientes propiedades:

* Conservan el directorio de trabajo como el símbolo del sistema de WSL (en la mayoría de los casos; las excepciones se explican a continuación).
* Tienen los mismos derechos de permiso que el proceso de WSL.
* Se ejecutan como el usuario activo de Windows.
* Aparecen en el administrador de tareas de Windows como si se ejecutaran directamente desde el símbolo del sistema de CMD.

Los archivos ejecutables de Windows que se ejecutan en WSL se administran de forma similar a los ejecutables nativos de Linux; las canalizaciones, los redireccionamientos e incluso los procesos en segundo plano funcionan según lo previsto.

Para ejecutar la herramientas de Windows `ipconfig.exe`, usa la herramienta de Linux `grep` para filtrar los resultados de "IPv4", y usa la herramienta de Linux `cut` para quitar los campos de columna. Desde una distribución de Linux (por ejemplo, Ubuntu), escribe lo siguiente:

```bash
ipconfig.exe | grep IPv4 | cut -d: -f2
```

Vamos a probar un ejemplo de combinación de comandos de Windows y Linux. Abre tu distribución de Linux (por ejemplo, Ubuntu) y crea el archivo de texto `touch foo.txt`. Ahora usa el comando de Linux `ls -la` para enumerar los archivos directos y sus detalles de creación, además de la herramienta de Windows PowerShell `findstr.exe` para filtrar los resultados, de modo que solo se muestre el archivo `foo.txt` en los resultados:

```bash
ls -la | findstr.exe foo.txt
```

Las herramientas de Windows deben incluir la extensión de archivo, coincidir con el caso del archivo y ser ejecutables.  Los no ejecutables, incluidos los scripts por lotes y  comandos nativos de CMD como `dir`, se pueden ejecutar con el comando `cmd.exe /C`.

Por ejemplo, para enumerar el contenido del directorio C:\ del sistema de archivos de Windows, escribe:

```bash
cmd.exe /C dir
```

O bien usa el comando `ping` para enviar una solicitud de eco al sitio web microsoft.com:

```bash
ping.exe www.microsoft.com
```

Los parámetros se pasan al archivo binario de Windows sin modificar. Por ejemplo, el siguiente comando abrirá `C:\temp\foo.txt` en `notepad.exe`:

```bash
notepad.exe "C:\temp\foo.txt"
```

También funcionará lo siguiente:

```bash
notepad.exe C:\\temp\\foo.txt
```

## <a name="share-environment-variables-between-windows-and-wsl"></a>Uso compartido de variables de entorno entre Windows y WSL

WSL y Windows comparten `WSLENV`, una variable de entorno especial creada para unir las distribuciones de Windows y Linux que se ejecutan en WSL.

Propiedades de la variable `WSLENV`:

* Se comparte; existe en entornos de Windows y WSL.
* Se trata de una lista de variables de entorno que se pueden compartir entre Windows y WSL.
* Puede formatear variables de entorno para que funcionen correctamente en Windows y WSL.
* Puede ayudar en el flujo entre WSL y Win32.

> [!NOTE]
> Antes de la versión 17063, la única variable de entorno de Windows a la que podía tener acceso WSL era `PATH`, por lo que se podían iniciar ejecutables de Win32 desde WSL. A partir de 17063, `WSLENV` comienza a ser compatible.
> WSLENV distingue entre mayúsculas y minúsculas.

## <a name="wslenv-flags"></a>Marcas de WSLENV

Hay cuatro marcas disponibles en `WSLENV` que pueden influir en la forma en que se traduce la variable de entorno.

Marcas `WSLENV`:

* `/p`: traduce la ruta de acceso entre las rutas de acceso de estilo de WSL/Linux y las rutas de acceso de Win32.
* `/l`: indica que la variable de entorno es una lista de rutas de acceso.
* `/u`: indica que esta variable de entorno solo debe incluirse al ejecutar WSL desde Win32.
* `/w`: indica que esta variable de entorno solo debe incluirse al ejecutar Win32 desde WSL.

Las marcas se pueden combinar según sea necesario.

[Obtenga más información sobre WSLENV](https://devblogs.microsoft.com/commandline/share-environment-vars-between-wsl-and-windows/), incluidas las preguntas más frecuentes y ejemplos de configuración del valor de WSLENV en una concatenación de otras variables de entorno predefinidas, cada una con una barra diagonal como sufijo seguida de marcas para especificar cómo se debe traducir el valor y pasar las variables con un script. En este artículo también se incluye un ejemplo para configurar un entorno de desarrollo con el [lenguaje de programación Go](https://golang.org/), configurado para compartir una variable GOPATH entre WSL y Win32.

## <a name="disable-interoperability"></a>Deshabilitación de la interoperabilidad

Los usuarios pueden deshabilitar la capacidad de ejecutar herramientas de Windows para una única sesión de WSL mediante la ejecución del siguiente comando como raíz:

```bash
echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

Para volver a habilitar los archivos binarios de Windows, sal de todas las sesiones de WSL y vuelve a ejecutar bash.exe o ejecuta el siguiente comando como raíz:

```bash
echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

La deshabilitación de la interoperabilidad no se conservará entre sesiones de WSL: la interoperabilidad se habilitará de nuevo cuando se inicie una nueva sesión.

## <a name="earlier-versions-of-windows-10"></a>Versiones anteriores de Windows 10

Hay varias diferencias para los comandos de interoperabilidad en las versiones anteriores de Windows 10. Si ejecutas una versión de Creators Update (octubre de 2017, compilación 16299) o la Actualización de aniversario (agosto de 2016, compilación 14393) de Windows 10, te recomendamos [actualizar a la versión más reciente de Windows](ms-settings:windowsupdate). Pero si esto no es posible, a continuación describimos algunas de las diferencias en la interoperabilidad.

Resumen:

* `bash.exe` se ha reemplazado por `wsl.exe`.
* La opción `-c` para ejecutar un único comando no es necesaria con `wsl.exe`.
* La ruta de acceso de Windows se incluye en `$PATH` de WSL.
* El proceso para deshabilitar la interoperabilidad no ha cambiado.

Los comandos de Linux se pueden ejecutar desde el símbolo del sistema de Windows o desde PowerShell, pero para las primeras versiones de Windows, puede que tengas que usar el comando `bash`. Por ejemplo:

```powershell
C:\temp> bash -c "ls -la"
```

Cosas como las entradas, las canalizaciones y los redireccionamientos de archivos funcionan según lo esperado.

Los comandos de WSL pasados a `bash -c` se reenvían al proceso de WSL sin modificaciones.  Las rutas de acceso de archivo deben especificarse en el formato de WSL y se debe tener cuidado al escapar caracteres relevantes. Ejemplo:

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
```

O bien...

```powershell
C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
```

Al llamar a una herramienta de Windows desde una distribución de WSL en una versión anterior de Windows 10, deberás especificar la ruta de acceso del directorio. Por ejemplo, desde la línea de comandos de WSL, escribe:

```bash
/mnt/c/Windows/System32/notepad.exe
```

En WSL, estos ejecutables se tratan de forma similar a los ejecutables nativos de Linux.  Esto significa que la adición de directorios a la ruta de acceso de Linux y la canalización entre comandos funciona según lo previsto.  Por ejemplo:

```bash
export PATH=$PATH:/mnt/c/Windows/System32
```
O bien

```bash
ipconfig.exe | grep IPv4 | cut -d: -f2
```

El archivo binario de Windows debe incluir la extensión de archivo, coincidir con el caso del archivo y ser ejecutable.  Los no ejecutables, incluidos los scripts por lotes y comandos como `dir`, se pueden ejecutar con el comando `/mnt/c/Windows/System32/cmd.exe /C`. Por ejemplo:

```bash
/mnt/c/Windows/System32/cmd.exe /C dir
```

## <a name="additional-resources"></a>Recursos adicionales

* [Entrada de blog de WSL sobre la interoperabilidad, de 2016](/archive/blogs/wsl/windows-and-ubuntu-interoperability)