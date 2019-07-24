---
title: Referencia de comandos de subsistema de Windows para Linux
description: Lista de comandos que administran el subsistema de Windows para Linux
keywords: BashOnWindows, bash, WSL, Windows, subsistema de Windows para Linux, windowssubsystem, Ubuntu
author: scooley
ms.author: scooley
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.openlocfilehash: 465f55f8ba210cd366adc66d433f1873e295136f
ms.sourcegitcommit: ead64b13501d6cb7170adafbb5624f4984a0af16
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/21/2019
ms.locfileid: "67307656"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a>Referencia de comandos para el subsistema de Windows para Linux

La mejor manera de interactuar con el subsistema de Windows para Linux es usar el `wsl.exe` comando. 

## `wsl.exe` 

A continuación se muestra una lista con todas las `wsl.exe` opciones cuando se usa a partir de la versión 1903 de Windows.

* Argumentos para la ejecución de archivos binarios de Linux:

    * Si no se proporciona ninguna línea de comandos, WSL. exe inicia el shell predeterminado.

    * --exec,-e<CommandLine>
        * Ejecute el comando especificado sin usar el shell de Linux predeterminado.

    * --
        * Pase el resto de la línea de comandos tal y como está.

* Opciones:
    * --distribución,-d<Distro>
        * Ejecutar la distribución especificada.

    * --usuario,-u<UserName>
        * Ejecutar como el usuario especificado.

* Argumentos para administrar el subsistema de Windows para Linux:

    * --exportar <Distro><FileName>
        * Exporta la distribución a un archivo tar.
        El nombre de archivo puede ser-para la salida estándar.

    * --Import <Distro> <InstallLocation>[opciones <FileName> ]
        * Importa el archivo tar especificado como una nueva distribución.
        El nombre de archivo puede ser-para la entrada estándar.

        * Opciones:
            * --version <Version> especifica la versión que se va a usar para la nueva distribución.

    * --List,-l [opciones]
        * Muestra las distribuciones.

        * Opciones:
            * --todos
                * Enumerar todas las distribuciones, incluidas las distribuciones que se están instalando o desinstalando actualmente.

            * --en ejecución
                * Muestra solo las distribuciones que se están ejecutando actualmente.

    * --set-default,-s<Distro>
        * Establece la distribución como valor predeterminado.

    * --set-default-version<Version>
        * Cambia la versión de instalación predeterminada para las nuevas distribuciones.

    * --Set-version <Distro><Version>
        * Cambia la versión de la distribución especificada.

    * --finalizar,-t<Distro>
        * Finaliza la distribución especificada.

    * --anular registro<Distro>
        * Anula el registro de la distribución.

    * --help
        * Mostrar información de uso.

## <a name="additional-commands"></a>Comandos adicionales

También hay comandos históricos para interactuar con el subsistema de Windows para Linux. Su funcionalidad se incluye en `wsl.exe`, pero siguen estando disponibles para su uso. 

### `wslconfig.exe`

Este comando le permite configurar la distribución de WSL. A continuación se muestra una lista de sus opciones.

* /l,/list [opción]
    * Muestra las distribuciones registradas.
        * /All: puede enumerar opcionalmente todas las distribuciones, incluidas las distribuciones que se instalan o desinstalan actualmente.

        * /Running: solo muestra las distribuciones que se están ejecutando actualmente.

* /s,/setDefault<DistributionName>
    * Establece la distribución como valor predeterminado.

* /t,/Terminate.<DistributionName>
    * Finaliza la distribución.

* /u,/unregister<DistributionName>
    * Anula el registro de la distribución.

### `bash.exe`

Este comando se usa para iniciar un shell de Bash. A continuación se muestran las opciones que puede usar con este comando.

* No se ha especificado ninguna opción
    * Inicia el shell de bash en el directorio actual. Si el shell de Bash no se instala automáticamente, se ejecuta`lxrun /install`

* Bash ~
    * Inicia el shell de bash en el directorio principal del usuario.  Similar a Running `cd ~`.

* Bash-c "&lt;comando&gt;"
    * Ejecuta el comando, imprime la salida y vuelve a salir del símbolo del sistema de Windows. <br/> <br/> Ejemplo`bash -c "ls"`

## <a name="deprecated-commands"></a>Comandos desusados

`lxrun.exe` Fue el primer comando que se usaba para instalar y administrar el subsistema de Windows para Linux. Está en desuso a partir de Windows 10 1803 y versiones posteriores.

El comando `lxrun.exe` se puede usar para interactuar directamente con el subsistema [de Windows para Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) .  Estos comandos se instalan en `\Windows\System32` el directorio y se pueden ejecutar en un símbolo del sistema de Windows o en PowerShell.

| Comando                     | Descripción                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | El comando lxrun se usa para administrar la instancia de WSL. |
| `lxrun /install`            | Inicia el proceso de descarga e instalación. <br/> se puede agregar **/y** para omitir todos los mensajes.  El mensaje de confirmación se acepta automáticamente y el usuario predeterminado se establece en root.          |
| `lxrun /uninstall`          | Desinstala y elimina la imagen de Ubuntu.  De forma predeterminada, no se quita el directorio de inicio de Ubuntu del usuario. <br/> se puede agregar **/y** para aceptar automáticamente el mensaje de confirmación. <br/>**/Full** desinstala y elimina el directorio principal de Ubuntu del usuario.         |
| `lxrun /setdefaultuser <userName>`     | Establece el valor predeterminado de bash en el usuario de Ubuntu. Solicitará una contraseña si el usuario especificado no existe.  Para obtener más información, https://aka.ms/wslusers visite:. <br/> **/y** Omite promping para la contraseña.  El usuario se creará sin una contraseña.|
| `lxrun /update`            | Actualiza el índice de paquetes del subsistema.          |
