---
title: Preguntas más frecuentes
description: Preguntas más frecuentes sobre el subsistema Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, faq
author: taraj
ms.author: taraj
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.openlocfilehash: 80675d8452b626ebe1d235774167c5ff27e4b44d
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063273"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a>Preguntas más frecuentes sobre el subsistema de Windows para Linux

## <a name="what-is-windows-subsystem-for-linux-wsl"></a>¿Qué es el subsistema de Windows para Linux (WSL)?
El subsistema de Windows para Linux (WSL) es una nueva característica de Windows 10 que permite ejecutar las herramientas de línea de comandos de Linux nativas directamente en Windows, junto con el escritorio de Windows tradicionales y modernas aplicaciones de la tienda.

Consulte la [acerca de la página](./about.md) para obtener más detalles.

## <a name="who-is-wsl-for"></a>¿Quién es WSL para?
Esto es principalmente una herramienta para desarrolladores, especialmente los desarrolladores web y los que trabajan en o con proyectos de código abierto. Esto permite que los usuarios que desea o necesita usar Bash, herramientas comunes de Linux (`sed`, `awk`, etc.) y muchas herramientas de Linux en primer lugar (Ruby, Python, etc.) para usar su cadena de herramientas en Windows.

## <a name="what-can-i-do-with-wsl"></a>¿Qué puedo hacer con WSL?
WSL proporciona que una aplicación denominada Bash.exe que, cuando se inicia, se abre una consola de Windows que se ejecute el shell de Bash. Con Bash, puede ejecutar aplicaciones y herramientas de línea de comandos de Linux. Por ejemplo, escriba `lsb_release -a` y presione ENTRAR; podrá ver los detalles de la distribución de Linux que se está ejecutando actualmente:

![Captura de pantalla de detalles de distribución](media/distro.png)

También puede acceder a sistema de archivos del equipo local desde dentro del shell de Linux Bash: encontrará las unidades de disco locales montados en el `/mnt` carpeta. Por ejemplo, su `C:` unidad se monta en `/mnt/c`:  

![Captura de pantalla de la unidad montada de C](media/ls.png)

## <a name="what-is-bash"></a>¿Qué es Bash?
[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) es un shell basado en texto popular y lenguaje de comandos. Es el shell predeterminado en Ubuntu y otras distribuciones de Linux y macOS incluido. Los usuarios escribir comandos en el shell para ejecutar secuencias de comandos o ejecutar comandos y herramientas para llevar a cabo muchas tareas.

## <a name="how-does-this-work"></a>¿Cómo funciona esto?
Visite nuestro [blog](https://blogs.msdn.microsoft.com/wsl/) donde entraremos en detalles sobre la tecnología subyacente.

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a>¿Por qué debo utilizar WSL en lugar de Linux en una máquina virtual?
WSL requiere menos recursos (CPU, memoria y almacenamiento) que una máquina virtual completa. WSL también le permite ejecutar las herramientas de línea de comandos de Linux y las aplicaciones junto con sus aplicaciones de escritorio y tienda de la línea de comandos, Windows y acceder a los archivos de Windows desde dentro de Linux. Esto le permite usar aplicaciones de Windows y las herramientas de línea de comandos de Linux en el mismo conjunto de archivos, si lo desea.

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a>¿Por qué debo utilizar, por ejemplo, Ruby en Linux en lugar de en Windows?
Suponiendo que se comporta el entorno en que se ejecutan como Linux, se han creado algunas herramientas multiplataforma. Por ejemplo, algunas herramientas se suponen que son capaces de obtener acceso a las rutas de acceso muy largo o que existan los archivos o carpetas específicos. Esto a menudo causa problemas en Windows, que a menudo se comporta de forma diferente de Linux.

Muchos lenguajes como Ruby y nodo son a menudo portar a y ejecutar muy bien, en Windows. Sin embargo, no todos los gema Ruby o propietarios de la biblioteca de nodo/NPM portar sus bibliotecas para admitir Windows y muchos tienen dependencias específicas de Linux. A menudo, esto puede producir en los sistemas creados con estas herramientas y bibliotecas que se presenta una compilación y a veces los errores en tiempo de ejecución o los comportamientos no deseados en Windows.

Estos son sólo algunos de los problemas que causaron mucha gente a pedir a Microsoft a mejorar las herramientas de línea de comandos de Windows y lo que nos volvimos para ser asociado de Canonical para habilitar las herramientas de línea de comandos Bash y Linux nativas para ejecutarse en Windows.

## <a name="what-does-this-mean-for-powershell"></a>¿Qué significa esto para PowerShell?
Mientras se trabaja con proyectos de OSS, existen numerosos escenarios donde resulta muy útil colocar en Bash desde un PowerShell símbolo del sistema. Bash soporte es complementario y refuerza el valor de la línea de comandos en Windows, lo que permite aprovechar otras tecnologías populares PowerShell y la Comunidad de PowerShell.

Lea más en el blog del equipo de PowerShell-- [Bash para Windows: ¿Por qué es impresionante y lo que significa para PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)

## <a name="can-i-run-all-linux-apps-in-wsl"></a>¿Puedo ejecutar aplicaciones Linux todas en WSL?
¡No! WSL es una herramienta destinada a permitir a los usuarios que necesiten ejecutar Bash y herramientas de línea de comandos de Linux en Windows core. 

WSL **no** ser capaz de admitir escritorios de GUI o aplicaciones (por ejemplo, Gnome, KDE, etcetera.)  

Además, aunque podrá ejecutar muchas aplicaciones de servidor conocidos (por ejemplo, Redis), no se recomienda WSL para hospedar servicios de producción: Microsoft ofrece una variedad de soluciones para ejecutar cargas de trabajo de Linux de producción en Azure, Hyper-V y Docker. 

## <a name="what-windows-skus-is-wsl-included-in"></a>¿Qué SKU de Windows se incluye WSL?
Subsistema de Windows para Linux está disponible en la versión de escritorio de Windows para Windows 10 Anniversary Edition y Creators update o posterior.

A partir de la Fall Creators update WSL estarán disponible en el escritorio y el servidor las SKU de Windows.

## <a name="what-processors-does-wsl-support"></a>¿Qué procesadores admite WSL?
WSL admite x64 y CPU de ARM.

## <a name="how-do-i-access-my-c-drive"></a>¿Cómo accedo a mi unidad C:?
Puntos de montaje para unidades de disco duro en el equipo local se crean automáticamente y proporcionan un acceso fácil para el sistema de archivos de Windows. 
 
**/ mnt /\<letra de unidad > /**
 
Uso de ejemplo sería `cd /mnt/c` para tener acceso a c:\

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a>¿Cómo se puede usar un archivo de Windows con una aplicación de Linux?

Una de las ventajas de WSL es poder acceder a los archivos a través de herramientas o de aplicaciones de Windows y Linux. 

WSL monta las unidades fijas de su equipo bajo el `/mnt/<drive>` carpeta en sus distribuciones de Linux. Por ejemplo, su `C:` unidad se monta en `/mnt/c/` 

Con las unidades montadas, puede editar código, por ejemplo, `C:\dev\myproj\` mediante [Visual Studio](https://visualstudio.microsoft.com/vs/) / o [VS Code](https://code.visualstudio.com/)y compilar/probar ese código en Linux mediante el acceso a los mismos archivos a través de `\mnt\c\dev\myproj`.

> **NOTA IMPORTANTE**: Una de las limitaciones más importantes del uso de WSL es que no es posible obtener acceso a/cambiar directamente los archivos del sistema de archivos de sus distribuciones de Linux con las aplicaciones de Windows o herramientas. Vea: [No cambie los archivos de Linux con las herramientas y aplicaciones de Windows](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a>¿Son los archivos en la unidad de Linux diferente de la unidad montada de Windows?

1. Los archivos bajo la raíz de Linux (es decir, `/`) se controlan mediante WSL que imita el comportamiento específico de Linux, incluidas sin limitación:
   * Archivos que contienen caracteres no válidos de nombre de archivo de Windows
   * Vínculos simbólicos para los usuarios sin derechos administrativos
   * Cambiar los atributos de archivo a través de chmod y chown
   * Mayúsculas y minúsculas de archivo o carpeta

2. Archivos en las unidades montadas se controlan mediante Windows y tienen los siguientes comportamientos:
   * Compatibilidad con mayúsculas y minúsculas
   * Todos los permisos se establecen para reflejar mejor los permisos de Windows

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a>¿Por qué hay tantos errores cuando se ejecuta la actualización de apt-get?
Algunos paquetes usan características que aún no hemos implementado. `udev`, por ejemplo, no se admite aún y provoca que algunos `apt-get upgrade` errores.

Para solucionar problemas relacionados con `udev`, siga los pasos siguientes:

1. Escriba lo siguiente para `/usr/sbin/policy-rc.d` y guarde los cambios.

    ```bash
    #!/bin/sh
    exit 101
    ```

2. Agregar permisos de ejecución a `/usr/sbin/policy-rc.d`

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
2. Ejecute los siguientes comandos

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a>¿Cómo se puede desinstalar una distribución de WSL?

En compilaciones anteriores a 1709 (16299) abra un símbolo del sistema y ejecute:
  ```batchfile
  lxrun /uninstall /full
  ```
  
Se pueden desinstalar las distribuciones de WSL instaladas desde la tienda como cualquier otra aplicación de Windows, con el botón secundario en el icono de la aplicación y haciendo clic en desinstalar o a través de PowerShell mediante el [ `Remove-AppxPackage` cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx).

## <a name="why-does-ping-generate-permission-denied-errors"></a>¿Por qué genera ping permiso denegado errores?
En WSL compilaciones < 14926, ping necesario WSL para ejecutarse a través de una consola con privilegios elevados. Este problema se ha corregido en compilación 14926 y versiones posteriores.

## <a name="how-do-i-run-an-openssh-server"></a>¿Cómo se puede ejecutar un servidor de OpenSSH?
Se requieren privilegios de administrador en Windows para ejecutar OpenSSH en WSL. Para ejecutar un servidor de OpenSSH, ejecutar Bash en Ubuntu en Windows como administrador o ejecute bash.exe desde un símbolo del sistema CMD/PowerShell con privilegios de administrador.

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a>¿Por qué obtiene "Error: ¿0x80040306 "cuando intento instalar?
WSL no admite que se ejecuta en una consola heredada. Para desactivar consola heredado:

1. Abra WSL, PowerShell o Cmd
1. A la derecha haga clic en el título de la barra -> Propiedades -> desactive la casilla "Use la consola heredada"
1. Haga clic en Aceptar

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a>¿Por qué obtiene "Error: ¿0 x 80040154 "cuando ejecuto bash.exe después de actualizar a Windows?
Se puede deshabilitar la característica "Subsistema de Windows para Linux" durante una actualización de Windows. Si esto ocurre se debe volver a habilitar la característica de Windows. Puede encontrar instrucciones para habilitar la característica "Subsistema de Windows para Linux" en el [Guía de instalación](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui).

## <a name="how-do-i-change-the-display-language-of-wsl"></a>¿Cómo se puede cambiar el idioma para mostrar de WSL?
Instalación WSL intentará cambiar automáticamente la configuración regional de Ubuntu para que coincida con la configuración regional de la instalación de Windows. Si no desea este comportamiento se puede ejecutar este comando para cambiar la configuración regional de Ubuntu después de que se complete la instalación. Tendrá que reiniciar bash.exe para que este cambio surta efecto.

El siguiente ejemplo se cambia a la configuración regional en-us:
```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a>¿Por qué no tengo acceso a internet desde WSL?
Algunos usuarios han informado de problemas con aplicaciones específicas de firewall bloqueando el acceso a internet en WSL. Los firewalls notificados son:

1. Kaspersky
1. AVG
1. Avast

En algunos casos si se desactiva el firewall permite el acceso. En algunos casos solo hecho de tener instalado el servidor de seguridad busca para bloquear el acceso.

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a>¿Cómo accedo a un puerto de WSL en Windows?
WSL comparte la dirección IP de Windows, tal y como se ejecuta en Windows. Por lo tanto puede tener acceso a ningún puerto en el host local, por ejemplo, si tenía contenido web en el puerto 1234 podría https://localhost:1234 en el Explorador de Windows.

## <a name="where-can-i-provide-feedback"></a>¿Dónde puedo proporcionar comentarios?

Puede compartir sus comentarios y preguntas a través de varios canales: Sus comentarios y preguntas se deben dirigir a:
* Nuestro [Rastreador de problemas de GitHub](https://github.com/Microsoft/BashOnWindows/issues)
* Nuestro [portal de UserVoice de línea de comandos](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)
* Nuestro [blog del equipo de línea de comandos](https://blogs.msdn.microsoft.com/commandline/)
* Via Twitter. Siga [ @richturn_ms ](https://twitter.com/richturn_MS) en Twitter para obtener información de noticias, actualizaciones, etcetera.
