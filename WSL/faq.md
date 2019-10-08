---
title: Preguntas más frecuentes
description: Preguntas más frecuentes sobre el Subsistema de Windows para Linux.
keywords: BashOnWindows, bash, WSL, Windows, windowssubsystem, p + f
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.localizationpriority: high
ms.openlocfilehash: 911bde69540bb8bb7a5ee40d8a9f4d6995f4fdaa
ms.sourcegitcommit: 3f35034581456a2008aa5ed1b623715dfef64608
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/03/2019
ms.locfileid: "71934904"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a>Preguntas más frecuentes sobre el subsistema de Windows para Linux

## <a name="what-is-windows-subsystem-for-linux-wsl"></a>¿Qué es el Subsistema de Windows para Linux (WSL)?
El Subsistema de Windows para Linux (WSL) es una nueva característica de Windows 10 que te permite ejecutar herramientas de línea de comandos nativas de Linux directamente en Windows, junto con el escritorio tradicional de Windows y las aplicaciones modernas de la tienda.

Consulta la [página Acerca de](./about.md) para obtener más detalles.

## <a name="who-is-wsl-for"></a>¿Para quién es WSL?
Esta es principalmente una herramienta para desarrolladores; especialmente para desarrolladores web y para aquellos que trabajan en proyectos de código abierto o con ellos. Esto permite a aquellos que quieran o necesiten usar Bash, las herramientas comunes de Linux (`sed`, `awk`, etc.) y varias herramientas de Linux (Ruby, Python, etc.) usar su cadena de herramientas en Windows.

## <a name="what-can-i-do-with-wsl"></a>¿Qué puedo hacer con WSL?
WSL proporciona una aplicación llamada Bash.exe que, cuando se inicia, abre una consola de Windows que ejecuta el shell de Bash. Con Bash, puedes ejecutar aplicaciones y herramientas de Linux de línea de comandos. Por ejemplo, escribe `lsb_release -a` y presiona Entrar para ver los detalles de la distribución de Linux que se está ejecutando actualmente:

![Captura de pantalla de los detalles de distribución](media/distro.png)

También puedes tener obtener acceso al sistema de archivos de la máquina local desde el shell de Bash de Linux; encontrarás las unidades locales montadas en la carpeta `/mnt`. Por ejemplo, la unidad `C:` se monta en `/mnt/c`:  

![Captura de pantalla de la unidad C montada](media/ls.png)

## <a name="what-is-bash"></a>¿Qué es Bash?
[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) es un conocido shell basado en texto, que cuenta con un lenguaje de comandos. Es el shell predeterminado que está incluido en Ubuntu, en otras distribuciones de Linux y en macOS. Los usuarios pueden escribir comandos en un shell para ejecutar scripts o ejecutar comandos y herramientas para realizar varias tareas.

## <a name="how-does-this-work"></a>¿Cómo funciona?
Echa un vistazo a nuestro [blog](https://blogs.msdn.microsoft.com/wsl/); en él detallaremos la tecnología subyacente.

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a>¿Por qué debo usar WSL en lugar de Linux en una VM?
WSL necesita menos recursos (CPU, memoria y almacenamiento) que una máquina virtual completa. Asimismo, WSL también te permite ejecutar aplicaciones y herramientas de línea de comandos de Linux junto con la línea de comandos de Windows, aplicaciones de escritorio y de Store, así como la posibilidad de acceder a los archivos de Windows desde Linux. Esto te permite usar las aplicaciones de Windows y las herramientas de línea de comandos de Linux en el mismo conjunto de archivos, si así lo deseas.

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a>¿Por qué debo usar, por ejemplo, Ruby en Linux en lugar de en Windows?
Algunas herramientas multiplataforma se crearon suponiendo que el entorno en el que se ejecutan se comporta como Linux. Por ejemplo, algunas herramientas suponen que pueden obtener acceso a rutas de acceso de archivos muy largas o que existen archivos o carpetas específicos. Esto suele provocar problemas en Windows, que a menudo se comporta de forma diferente de Linux.

Muchos lenguajes como Ruby y Node a menudo se trasladan a Windows y se ejecutan de manera excelente. Sin embargo, no todos los propietarios de bibliotecas Ruby Gem o node/NPM portan sus bibliotecas para que admitan Windows, y muchas tienen dependencias específicas de Linux. Esto a menudo puede dar como resultado que los sistemas que se crearon con herramientas y bibliotecas de este tipo sufran errores de compilación y, a veces, del entorno de ejecución o tengan comportamientos no deseados en Windows.

Estos son solo algunos de los problemas que han provocado que muchas personas pidan a Microsoft que mejore las herramientas de línea de comandos de Windows, lo que nos llevó a asociarnos con Canonical para permitir que las herramientas de línea de comandos nativas de Bash y Linux se ejecuten en Windows.

## <a name="what-does-this-mean-for-powershell"></a>¿Qué significa esto para PowerShell?
Al trabajar con proyectos de OSS, existen numerosos escenarios en los que es enormemente útil usar Bash desde un símbolo del sistema de PowerShell. La compatibilidad con Bash es complementaria y fortalece el valor de la línea de comandos en Windows, permitiendo que PowerShell y la comunidad de PowerShell aprovechen otras tecnologías populares.

Puedes leer más en el blog del equipo de PowerShell: [Bash para Windows: por qué es impresionante y qué significa para PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/).

## <a name="can-i-run-all-linux-apps-in-wsl"></a>¿Puedo ejecutar TODAS las aplicaciones de Linux en WSL?
No. WSL es una herramienta destinada a permitir que los usuarios que necesitan esas aplicaciones puedan ejecutar Bash y las principales herramientas de línea de comandos de Linux en Windows. 

WSL **no** tiene como objetivo admitir aplicaciones o escritorios de GUI (por ejemplo, Gnome, KDE, etc.).  

Asimismo, aunque puedas ejecutar varias aplicaciones de servidor populares (por ejemplo, Redis), no recomendamos WSL para hospedar servicios de producción, ya que Microsoft ofrece una variedad de soluciones para ejecutar cargas de trabajo de Linux en Azure, Hyper-V y Docker. 

## <a name="what-windows-skus-is-wsl-included-in"></a>¿En qué SKU de Windows está incluido WSL?
El Subsistema de Windows para Linux está disponible en la versión de escritorio de Windows para las versiones de Actualización de aniversario de Windows 10 y Creators Update, o posteriores.

A partir de la versión de Fall Creators Update, WSL estará disponible en las SKU de escritorio y servidor de Windows.

## <a name="what-processors-does-wsl-support"></a>¿Qué procesadores admite WSL?
WSL admite las CPU x64 y ARM.

## <a name="how-do-i-access-my-c-drive"></a>¿Cómo accedo a la unidad C:?
Los puntos de montaje de los discos duros en la máquina local se crean automáticamente y proporcionan un fácil acceso al sistema de archivos de Windows. 
 
**/mnt/\<letra de unidad>/**
 
Un ejemplo de uso sería `cd /mnt/c` para acceder a c:\

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a>¿Cómo uso un archivo de Windows con una aplicación de Linux?

Uno de los beneficios de WSL es que puedes acceder a tus archivos mediante aplicaciones o herramientas de Windows y Linux. 

WSL monta las unidades fijas de la máquina que están en la carpeta `/mnt/<drive>` en tus distribuciones de Linux. Por ejemplo, la unidad `C:` se monta en `/mnt/c/` 

Si usas tus unidades montadas, puedes editar el código (por ejemplo, `C:\dev\myproj\` usando [Visual Studio](https://visualstudio.microsoft.com/vs/) / o [VS Code](https://code.visualstudio.com/)) y compilar o probar ese código en Linux accediendo a los mismos archivos a través de `/mnt/c/dev/myproj`.

> **NOTA IMPORTANTE**: Una de las limitaciones principales del uso de WSL es que no se admite el acceso o cambio directo de archivos en el sistema de archivos de tus distribuciones de Linux mediante aplicaciones o herramientas de Windows. Vea: [No cambies los archivos de Linux con las aplicaciones y herramientas de Windows](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a>¿Los archivos de la unidad de Linux son diferentes de la unidad de Windows montada?

1. Los archivos que se encuentran en la raíz de Linux (por ejemplo , `/`) se controlan mediante WSL, que imita el comportamiento específico de Linux, incluyendo, entre otros, los siguientes:
   * Archivos que contienen caracteres de nombre de archivo de Windows que no son válidos
   * Vínculos simbólicos creados para usuarios que no son administradores
   * La opción de cambiar atributos de archivo a través de chmod y chown
   * Distinción de mayúsculas y minúsculas en archivos o carpetas

2. Los archivos de las unidades montadas se controlan mediante Windows y tienen los siguientes comportamientos:
   * Compatibilidad para la distinción de mayúsculas y minúsculas
   * Todos los permisos se establecen para reflejar mejor los permisos de Windows

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a>¿Por qué hay tantos errores cuando ejecuto la actualización apt-get?
Algunos paquetes usan características que aún no se han implementado. `udev`, por ejemplo, todavía no se admite y produce varios errores de tipo `apt-get upgrade`.

Para corregir los problemas relacionados con `udev`, sigue estos pasos:

1. Escribe lo siguiente en `/usr/sbin/policy-rc.d` y guarda los cambios.

    ```bash
    #!/bin/sh
    exit 101
    ```

2. Agrega los permisos de ejecución en `/usr/sbin/policy-rc.d`.

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
2. Ejecuta los siguientes comandos:

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a>¿Cómo desinstalo una distribución de WSL?

En las compilaciones anteriores a 1709 (16299), abre un símbolo del sistema y ejecuta lo siguiente:
  ```batchfile
  lxrun /uninstall /full
  ```
  
Las distribuciones de WSL instaladas desde Store se pueden desinstalar como cualquier otra aplicación de Windows; para ello, haz clic con el botón derecho en el icono de la aplicación y haz clic en Desinstalar; también puedes desinstalarlas a través de PowerShell mediante el cmdlet [`Remove-AppxPackage`](https://technet.microsoft.com/en-us/library/hh856038.aspx).

## <a name="why-does-ping-generate-permission-denied-errors"></a>¿Por qué el ping genera errores de tipo "Permiso denegado"?
En las compilaciones de WSL anteriores a la versión 14926, el ping requería que WSL se ejecutara mediante de una consola con privilegios elevados. Este problema se corrigió en la compilación 14926 y en versiones posteriores.

## <a name="how-do-i-run-an-openssh-server"></a>¿Cómo ejecuto un servidor OpenSSH?
Se requieren privilegios de administrador en Windows para ejecutar OpenSSH en WSL. Para ejecutar un servidor OpenSSH, ejecuta Bash en Ubuntu en Windows como administrador o ejecuta Bash.exe desde un símbolo del sistema de CMD/PowerShell con privilegios de administrador.

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a>¿Por qué obtengo el mensaje "Error: 0x80040306 " cuándo intento realizar la instalación?
WSL no se puede ejecutar en una consola heredada. Para desactivar la consola heredada:

1. Abre WSL, PowerShell o CMD.
1. Haz clic con el botón derecho en barra de título -> Propiedades-> y desactiva "Usar consola heredada".
1. Haga clic en Aceptar

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a>¿Por qué obtengo el mensaje "Error: 0x80040154 "cuando ejecuto Bash.exe después de actualizar Windows?
La característica "Subsistema de Windows para Linux" puede estar deshabilitada durante una actualización de Windows. Si esto ocurre, debes volver a habilitar la característica de Windows. Las instrucciones para habilitar la característica "Subsistema de Windows para Linux" se pueden encontrar en la [guía de instalación](https://docs.microsoft.com/en-us/windows/wsl/install-win10#install-the-windows-subsystem-for-linux).

## <a name="how-do-i-change-the-display-language-of-wsl"></a>¿Cómo cambio el idioma de visualización de WSL?
La instalación de WSL intentará cambiar automáticamente la configuración regional de Ubuntu para que coincida con la configuración regional de la instalación de Windows. Si no quieres que esto pase, puedes ejecutar este comando para cambiar la configuración regional de Ubuntu una vez finalizada la instalación. Ten en cuenta que tendrás que reiniciar bash.exe para que este cambio surta efecto.

En el ejemplo siguiente se cambia la configuración regional a en-US:
```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a>¿Por qué no tengo acceso a Internet desde WSL?
Algunos usuarios han detectado problemas con aplicaciones de firewall específicas que bloquean el acceso a Internet en WSL. Los firewalls que dan error son:

1. Kaspersky
1. AVG
1. Avast

En algunos casos, si desactivas el firewall podrás acceder. En otros casos, simplemente tener instalado el firewall parece bloquear el acceso a Internet.

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a>¿Cómo obtengo acceso a un puerto desde WSL en Windows?
WSL comparte la dirección IP de Windows, ya que se ejecuta en Windows. Así pues, puedes obtener acceso a cualquier puerto en localhost; por ejemplo, si tienes contenido web en el puerto 1234, puedes obtener acceso https://localhost:1234 al explorador de Windows.

## <a name="how-can-i-back-up-my-wsl-distros"></a>¿Cómo puedo realizar una copia de seguridad de mi distribución de WSL?

La mejor manera de hacer una copia de seguridad de la distribución está disponible en la versión 1809 y en versiones posteriores de Windows. Puedes exportar toda la distribución a un tarball mediante el comando `wsl --export`. A continuación, puedes importar de nuevo esta distribución en WSL mediante el comando `wsl --import`, lo que te permitirá realizar copias de seguridad y guardar los estados de las distribuciones de WSL. 

Recuerda que los servicios de copia de seguridad tradicionales que copian los archivos de las carpetas AppData (por ejemplo, copias de seguridad de Windows) no dañarán los archivos de Linux. 



## <a name="where-can-i-provide-feedback"></a>¿Dónde puedo enviar mis comentarios?

Puedes compartir tus comentarios y formular preguntas a través de varios canales: Los comentarios y las preguntas se deben enviar a:
* Nuestro canal de [seguimiento de problemas de GitHub](https://github.com/Microsoft/BashOnWindows/issues).
* Nuestro [portal de UserVoice de línea de comandos](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top).
* Nuestro [blog del equipo de línea de comandos](https://blogs.msdn.microsoft.com/commandline/).
* A través de Twitter. Sigue [@richturn_ms](https://twitter.com/richturn_MS) en Twitter para conocer las noticias, actualizaciones, etc.
