---
title: Preguntas más frecuentes
description: Preguntas más frecuentes sobre el subsistema de Windows para Linux.
keywords: BashOnWindows, bash, WSL, Windows, windowssubsystem, p + f
author: taraj
ms.author: taraj
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.localizationpriority: high
ms.openlocfilehash: e3376f8dff83262577bc52fb3ac368b70b21d922
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122765"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a>Preguntas más frecuentes sobre el subsistema de Windows para Linux

## <a name="what-is-windows-subsystem-for-linux-wsl"></a>¿Qué es el subsistema de Windows para Linux (WSL)?
El subsistema de Windows para Linux (WSL) es una nueva característica de Windows 10 que le permite ejecutar herramientas de línea de comandos nativas de Linux directamente en Windows, junto con el escritorio tradicional de Windows y las aplicaciones de la tienda modernas.

Vea la [página acerca](./about.md) de para obtener más detalles.

## <a name="who-is-wsl-for"></a>¿A quién está WSL?
Esta es principalmente una herramienta para desarrolladores, especialmente desarrolladores web y aquellos que trabajan en proyectos de código abierto o con ellos. Esto permite que los usuarios deseen usar Bash, herramientas comunes de Linux (`sed`, `awk`, etc.) y muchas herramientas de Linux (Ruby, Python, etc.) para usar su cadena de herramientas en Windows.

## <a name="what-can-i-do-with-wsl"></a>¿Qué puedo hacer con WSL?
WSL proporciona una aplicación llamada bash. exe que, cuando se inicia, abre una consola de Windows que ejecuta el shell de Bash. Con bash, puede ejecutar aplicaciones y herramientas de Linux de línea de comandos. Por ejemplo, escriba `lsb_release -a` y presione Entrar; verá los detalles del distribución de Linux que se está ejecutando actualmente:

![Captura de pantalla de detalles de distribución](media/distro.png)

También puede tener acceso al sistema de archivos de la máquina local desde el shell de bash de Linux: encontrará las unidades locales montadas en la `/mnt` carpeta. Por ejemplo, la `C:` unidad se monta en `/mnt/c`:  

![Captura de pantalla de la unidad C montada](media/ls.png)

## <a name="what-is-bash"></a>¿Qué es Bash?
[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) es un conocido Shell basado en texto y un lenguaje de comandos. Es el shell predeterminado incluido en Ubuntu y otros distribuciones de Linux y en macOS. Los usuarios escriben comandos en un shell para ejecutar scripts y/o ejecutar comandos y herramientas para realizar muchas tareas.

## <a name="how-does-this-work"></a>¿Cómo funciona esto?
Eche un vistazo a nuestro [blog](https://blogs.msdn.microsoft.com/wsl/) en el que vamos a profundizar en la tecnología subyacente.

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a>¿Por qué debo usar WSL en lugar de Linux en una máquina virtual?
WSL requiere menos recursos (CPU, memoria y almacenamiento) que una máquina virtual completa. WSL también permite ejecutar aplicaciones y herramientas de línea de comandos de Linux junto con la línea de comandos de Windows, aplicaciones de escritorio y de la tienda, así como acceder a los archivos de Windows desde Linux. Esto le permite usar las aplicaciones de Windows y las herramientas de línea de comandos de Linux en el mismo conjunto de archivos si lo desea.

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a>¿Por qué debo usar, por ejemplo, Ruby en Linux en lugar de en Windows?
Algunas herramientas multiplataforma se crearon suponiendo que el entorno en el que se ejecuta se comporta como Linux. Por ejemplo, algunas herramientas suponen que pueden tener acceso a rutas de acceso de archivo muy largas o que existen archivos o carpetas específicos. Esto suele provocar problemas en Windows, que a menudo se componen de forma diferente de Linux.

Muchos lenguajes como Ruby y node a menudo se trasladan a Windows y se ejecutan de manera excelente. Sin embargo, no todos los propietarios de la biblioteca de nodo/NPM de Ruby o node/NPM portan sus bibliotecas para admitir Windows y muchas de ellas tienen dependencias específicas de Linux. A menudo, esto puede dar lugar a sistemas compilados con tales herramientas y bibliotecas que sufren la compilación y, en ocasiones, errores en tiempo de ejecución o comportamientos no deseados en Windows.

Estos son solo algunos de los problemas que han provocado que muchas personas pidan a Microsoft que mejore las herramientas de línea de comandos de Windows y lo que nos llevó a asociarse con Canonical para permitir que las herramientas de línea de comandos de bash y Linux nativas se ejecuten en Windows.

## <a name="what-does-this-mean-for-powershell"></a>¿Qué significa esto para PowerShell?
Al trabajar con proyectos de OSS, hay numerosos escenarios en los que es enormemente útil colocarlos en bash desde un símbolo del sistema de PowerShell. La compatibilidad con bash es complementaria y fortalece el valor de la línea de comandos en Windows, lo que permite que PowerShell y la comunidad de PowerShell aprovechen otras tecnologías populares.

Obtenga más información en el blog del equipo de [PowerShell: Bash para Windows: ¿Por qué es increíble y qué significa PowerShell?](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)

## <a name="can-i-run-all-linux-apps-in-wsl"></a>¿Puedo ejecutar todas las aplicaciones de Linux en WSL?
¡No! WSL es una herramienta destinada a permitir a los usuarios que necesitan ejecutar herramientas de línea de comandos de Linux y bash en Windows. 

WSL no pretende admitir aplicaciones o escritorios de GUI (por ejemplo, GNOME, KDE, etc.).  

Además, aunque podrá ejecutar muchas aplicaciones de servidor conocidas (por ejemplo, Redis), no recomendamos WSL para hospedar servicios de producción. Microsoft ofrece una variedad de soluciones para ejecutar cargas de trabajo de Linux de producción en Azure, Hyper-V y Docker. 

## <a name="what-windows-skus-is-wsl-included-in"></a>¿En qué SKU de Windows está incluida WSL?
El subsistema de Windows para Linux está disponible en la versión de escritorio de Windows para Windows 10 aniversario y Creators Update o posterior.

A partir de la actualización de Fall Creators Update WSL estará disponible en las SKU de escritorio y de servidor de Windows.

## <a name="what-processors-does-wsl-support"></a>¿Qué procesadores admite WSL?
WSL admite CPU x64 y ARM.

## <a name="how-do-i-access-my-c-drive"></a>Cómo tener acceso a la unidad C:
Los puntos de montaje de las unidades de disco duro del equipo local se crean automáticamente y proporcionan un acceso fácil al sistema de archivos de Windows. 
 
**>\<letra de unidad/mnt//**
 
Ejemplo `cd /mnt/c` de uso sería para obtener acceso a c:\

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a>¿Cómo usar un archivo de Windows con una aplicación de Linux?

Una de las ventajas de WSL es poder acceder a los archivos a través de aplicaciones de Windows y Linux, o bien de herramientas. 

WSL monta las unidades fijas del equipo en la `/mnt/<drive>` carpeta del distribuciones de Linux. Por ejemplo, la `C:` unidad se monta en`/mnt/c/` 

Con las unidades montadas, puede editar el código en, por ejemplo `C:\dev\myproj\` , con [Visual Studio](https://visualstudio.microsoft.com/vs/) o [vs Code](https://code.visualstudio.com/), y compilar o probar ese código en Linux mediante el acceso a los `/mnt/c/dev/myproj`mismos archivos a través de.

> **NOTA IMPORTANTE**: Una de las limitaciones principales del uso de WSL es que no se admite el acceso directo o el cambio de archivos en el sistema de archivos de Linux distribuciones con aplicaciones o herramientas de Windows. Vea: [No cambie los archivos de Linux con las herramientas y aplicaciones de Windows](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a>¿Son los archivos de la unidad Linux distintos de la unidad de Windows montada?

1. Los archivos que se encuentran en la raíz `/`de Linux (es decir,) se controlan mediante WSL, que imita el comportamiento específico de Linux, incluidos, entre otros, los siguientes:
   * Archivos que contienen caracteres de nombre de archivo de Windows no válidos
   * Vínculos simbólicos creados para usuarios que no son administradores
   * Cambiar atributos de archivo a través de chmod y chown
   * Distinción de mayúsculas y minúsculas en archivos o carpetas

2. Los archivos de las unidades montadas se controlan mediante Windows y tienen los siguientes comportamientos:
   * Distinción entre mayúsculas y minúsculas
   * Todos los permisos se establecen para reflejar mejor los permisos de Windows

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a>¿Por qué hay muchos errores cuando ejecuto la actualización apt-get?
Algunos paquetes usan características que aún no se han implementado. `udev`, por ejemplo, todavía no se admite y produce `apt-get upgrade` varios errores.

Para corregir los problemas relacionados `udev`con, siga estos pasos:

1. Escriba lo siguiente en `/usr/sbin/policy-rc.d` y guarde los cambios.

    ```bash
    #!/bin/sh
    exit 101
    ```

2. Agregar permisos de ejecución a`/usr/sbin/policy-rc.d`

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
2. Ejecute los siguientes comandos

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a>Cómo desinstalar una distribución de WSL?

En las compilaciones anteriores a 1709 (16299), abra un símbolo del sistema y ejecute:
  ```batchfile
  lxrun /uninstall /full
  ```
  
Las distribuciones de WSL instaladas desde la tienda se pueden desinstalar como cualquier otra aplicación de Windows; para ello, haga clic con el botón derecho en el icono de la aplicación y haga clic en desinstalar, o bien a través de PowerShell mediante el [ `Remove-AppxPackage` cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx).

## <a name="why-does-ping-generate-permission-denied-errors"></a>¿Por qué el ping genera errores de Permiso denegado?
En WSL crea < 14926, ping requiere WSL para ejecutarse a través de una consola con privilegios elevados. Este problema se corrigió en la compilación 14926 y versiones posteriores.

## <a name="how-do-i-run-an-openssh-server"></a>Cómo ejecutar un servidor OpenSSH?
Se requieren privilegios de administrador en Windows para ejecutar OpenSSH en WSL. Para ejecutar un servidor OpenSSH, ejecute bash en Ubuntu en Windows como administrador o ejecute bash. exe desde un símbolo del sistema de CMD/PowerShell con privilegios de administrador.

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a>¿Por qué obtengo "error: 0x80040306 "¿Cuándo intento instalar?
WSL no admite la ejecución en una consola heredada. Para desactivar la consola heredada:

1. Abra WSL, PowerShell o CMD.
1. Haga clic con el botón derecho en barra de título-> Propiedades-> desactive "usar consola heredada".
1. Haga clic en Aceptar

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a>¿Por qué obtengo "error: 0x80040154 "cuando ejecuto bash. exe después de actualizar Windows?
La característica "subsistema de Windows para Linux" puede estar deshabilitada durante una actualización de Windows. Si esto ocurre, se debe volver a habilitar la característica de Windows. Las instrucciones para habilitar la característica "subsistema de Windows para Linux" se pueden encontrar en la [Guía de instalación](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui)de.

## <a name="how-do-i-change-the-display-language-of-wsl"></a>Cómo cambiar el idioma de visualización de WSL?
La instalación de WSL intentará cambiar automáticamente la configuración regional de Ubuntu para que coincida con la configuración regional de la instalación de Windows. Si no desea este comportamiento, puede ejecutar este comando para cambiar la configuración regional de Ubuntu una vez finalizada la instalación. Tendrá que reiniciar bash. exe para que este cambio surta efecto.

En el ejemplo siguiente se cambia a configuración regional a en-US:
```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a>¿Por qué no tengo acceso a Internet desde WSL?
Algunos usuarios han detectado problemas con aplicaciones de Firewall específicas que bloquean el acceso a Internet en WSL. Los firewalls que se indican son:

1. Kaspersky
1. LATENCIA
1. Avast

En algunos casos, desactivar el Firewall permite el acceso. En algunos casos, simplemente tener instalado el Firewall parece bloquear el acceso.

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a>Cómo acceso a un puerto desde WSL en Windows?
WSL comparte la dirección IP de Windows, ya que se ejecuta en Windows. Como tal, puede tener acceso a cualquier puerto en localhost; por ejemplo, si tiene contenido web en el https://localhost:1234 puerto 1234, puede acceder al explorador de Windows.

## <a name="how-can-i-back-up-my-wsl-distros"></a>¿Cómo puedo realizar una copia de seguridad de mi WSL distribuciones?

La mejor manera de hacer una copia de seguridad de distribuciones está disponible en la versión 1809 y posteriores de Windows. Puede exportar toda la distribución a un tarball mediante el `wsl --export` comando. Después, puede importar de nuevo este distribución en WSL con `wsl --import` el comando, lo que le permite realizar copias de seguridad y guardar los Estados de las distribuciones de WSL. 

Tenga en cuenta que los servicios de copia de seguridad tradicionales que copian los archivos de las carpetas AppData (por ejemplo, copias de seguridad de Windows) no dañarán los archivos de Linux. 



## <a name="where-can-i-provide-feedback"></a>¿Dónde puedo proporcionar comentarios?

Puede compartir sus comentarios y formular preguntas a través de varios canales: Los comentarios y las preguntas se deben dirigir a:
* Nuestro [seguimiento de problemas de github](https://github.com/Microsoft/BashOnWindows/issues)
* Nuestro [portal de UserVoice de línea de comandos](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)
* Nuestro [blog del equipo de línea de comandos](https://blogs.msdn.microsoft.com/commandline/)
* A través de Twitter. Siga [@richturn_ms](https://twitter.com/richturn_MS) en Twitter para conocer las noticias, las actualizaciones, etc.
