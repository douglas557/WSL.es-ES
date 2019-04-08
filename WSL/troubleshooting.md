---
title: Solución de problemas de la Susbystem de Windows para Linux
description: Proporciona información detallada sobre los errores comunes y emite las personas que surgen durante la ejecución de Linux en el Susbystem de Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, ubuntu
author: scooley
ms.author: scooley
ms.date: 11/15/2017
ms.topic: article
ms.assetid: 6753f1b2-200e-49cc-93a5-4323e1117246
ms.custom: seodec18
ms.openlocfilehash: 055bdc02dcf8f078caa014abd6dd755a47c99cfe
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063303"
---
# <a name="troubleshooting-windows-subsystem-for-linux"></a>Solución de problemas de subsistema de Windows para Linux

### <a name="bash-loses-network-connectivity-once-connected-to-a-vpn"></a>Bash pierde conectividad de red una vez conectada a una VPN

Si después de conectarse a una VPN en Windows, bash pierde conectividad de red, pruebe esta solución desde dentro de bash. Esta solución, podrá anular manualmente la resolución DNS a través de `/etc/resolv.conf`.

1. Tome nota del servidor DNS de la VPN de hacerlo `ipconfig.exe /all`
2. Realizar una copia de resolv.conf existente `sudo cp /etc/resolv.conf /etc/resolv.conf.new`
3. Desvincular el resolv.con actual `sudo unlink /etc/resolv.conf`
4. `sudo mv /etc/resolv.conf.new /etc/resolv.conf`
5. Abra `/etc/resolv.conf` y <br/>
   a. Elimine la primera línea del archivo, que dice "\# este archivo se generó automáticamente mediante WSL. Para detener la generación automática de este archivo, quite esta línea. ". <br/>
   b. Agregue la entrada DNS de (1) anteriormente como la primera entrada en la lista de servidores DNS. <br/>
   c. Cierre el archivo. <br/>

Una vez que haya desconectado la conexión VPN, deberá revertir los cambios `/etc/resolv.conf`. Para ello, haga lo:
1. `cd /etc`
2. `sudo mv resolv.conf resolv.conf.new`
3. `sudo ln -s ../run/resolvconf/resolv.conf resolv.conf`

### <a name="starting-wsl-or-installing-a-distribution-returns-an-error-code"></a>A partir de WSL o instalar una distribución devuelve un código de error

Siga [estas instrucciones](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs) para recopilar registros detallados y registre un problema en nuestro GitHub.

### <a name="updating-bash-on-ubuntu-on-windows"></a>Actualización de Bash en Ubuntu en Windows

Hay dos componentes de Bash en Ubuntu en Windows que requieren la actualización. 

1. El subsistema de Windows para Linux
  
   Actualizando esta parte de Bash en Ubuntu en Windows se habilitará los contornos de correcciones de nuevo en el [notas de la versión](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes). Asegúrese de que está suscrito al programa Windows Insider y que la compilación está actualizada. Para un mayor control de nivel de detalle, incluido el restablecimiento de su Ubuntu instancia desproteger el [página de referencia de comandos](https://msdn.microsoft.com/en-us/commandline/wsl/reference).

2. Los archivos binarios de usuario de Ubuntu 

   Actualizando esta parte de Bash en Ubuntu en Windows se instalarán las actualizaciones a los archivos binarios de usuario de Ubuntu, incluidas las aplicaciones que ha instalado mediante apt-get. Para actualizar la ejecución de los siguientes comandos de Bash:
  
   1. `apt-get update`
   2. `apt-get upgrade`
  
### <a name="apt-get-upgrade-errors"></a>Errores de actualización de APT-get
Algunos paquetes usan características que aún no hemos implementado. `udev`, por ejemplo, no se admite aún y provoca que algunos `apt-get upgrade` errores.

Para solucionar problemas relacionados con `udev`, siga los pasos siguientes:

1. Escriba lo siguiente para `/usr/sbin/policy-rc.d` y guarde los cambios.
  
   ``` BASH
   #!/bin/sh
   exit 101
   ```
  
2. Agregar permisos de ejecución a `/usr/sbin/policy-rc.d`
   ``` BASH
   chmod +x /usr/sbin/policy-rc.d
   ```
  
3. Ejecute los siguientes comandos
   ``` BASH
   dpkg-divert --local --rename --add /sbin/initctl
   ln -s /bin/true /sbin/initctl
   ```
  
### <a name="error-0x80040306-on-installation"></a>"Error: 0x80040306 "en la instalación
Esto tiene que ver con el hecho de que no se admite consola heredada.
Para desactivar consola heredado:

1. Abra cmd.exe
1. A la derecha, haga clic en título de la barra -> Propiedades -> desactive la opción Usar la consola antigua
1. Haga clic en Aceptar

### <a name="error-0x80040154-after-windows-update"></a>"Error: 0 x 80040154 "después de actualización de Windows
El subsistema de Windows para Linux característica puede deshabilitarse durante una actualización de Windows. Si esto ocurre se debe volver a habilitar la característica de Windows. Instrucciones para habilitar el subsistema Windows para Linux se puede encontrar en el [Guía de instalación](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui).

### <a name="changing-the-display-language"></a>Cambiar el idioma para mostrar
Instalación WSL intentará cambiar automáticamente la configuración regional de Ubuntu para que coincida con la configuración regional de la instalación de Windows.  Si no desea este comportamiento se puede ejecutar este comando para cambiar la configuración regional de Ubuntu después de que se complete la instalación.  Tendrá que reiniciar bash.exe para que este cambio surta efecto.

El siguiente ejemplo se cambia a la configuración regional en-us:
``` BASH
sudo update-locale LANG=en_US.UTF8
```

### <a name="installation-issues-after-windows-system-restore"></a>Problemas de instalación después de la restauración del sistema de Windows
1.  Eliminar el `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux` carpeta. <br/>
  **Nota: Hacer esto si la característica opcional esté completamente instalada y funciona.**
2.  Habilitar la característica opcional de WSL (si aún no)
3.  Reiniciar
4.  lxrun /Uninstall/completa
5.  Instalar bash

### <a name="no-internet-access-in-wsl"></a>Sin acceso a internet en WSL
Algunos usuarios han informado de problemas con aplicaciones específicas de firewall bloqueando el acceso a internet en WSL.  Los firewalls notificados son:

1. Kaspersky
1. AVG
1. Avast

En algunos casos si se desactiva el firewall permite el acceso.  En algunos casos solo hecho de tener instalado el servidor de seguridad busca para bloquear el acceso.

### <a name="permission-denied-error-when-using-ping"></a>Error de permiso denegado cuando usa el comando ping
#### [<a name="anniversary-update"></a>Actualización de aniversario](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14388-to-windows-10-anniversary-update) 

Se requieren privilegios de administrador en Windows para ejecutar ping en WSL.  Para ejecutar el comando ping, ejecute Bash en Ubuntu en Windows como administrador o ejecute bash.exe desde un símbolo del sistema CMD/PowerShell con privilegios de administrador.

#### [<a name="build-14926"></a>Compilación 14926 +](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14926)
  Privilegios de administrador ya no es necesarios.

### <a name="bash-is-hung"></a>Bash se ha bloqueado
Si mientras trabaja con bash, encontrar ese bash está bloqueado (o interbloqueo) y no responde a las entradas, ayudarnos a diagnosticar el problema al recopilar e informar de un volcado de memoria. Tenga en cuenta que estos pasos se bloquearán el sistema. Hacer esto si no está familiarizado con la o guardar su trabajo antes de hacerlo.  <br/>
Para recopilar un volcado de memoria:
1. Cambie el tipo de volcado de memoria a "volcado de memoria completo". Al cambiar el tipo de volcado de memoria, tome nota del tipo actual.
2. Use la [pasos](https://blogs.technet.microsoft.com/askpfeplat/2015/04/05/how-to-force-a-diagnostic-memory-dump-when-a-computer-hangs/) para configurar el bloqueo mediante el control del teclado.
3. Reproducción el bloqueo o interbloqueo.
4. Bloquear el sistema mediante la secuencia de teclas de (2).
5. El sistema se bloquee y recopilar el volcado de memoria.
6. Una vez que el sistema se reinicia, notificar el memory.dmp a secure@microsoft.com. La ubicación predeterminada del archivo de volcado de memoria es %SystemRoot%\memory.dmp o C:\Windows\memory.dmp si C: es la unidad del sistema. En el correo electrónico, tenga en cuenta que el volcado de memoria para el WSL o Bash en el equipo de Windows.
7. Restaurar el tipo de volcado de memoria a la configuración original.

### <a name="check-your-build-number"></a>Compruebe el número de compilación

Para buscar el que número de compilación de Windows y la arquitectura de su equipo, abra  
**Configuración de** > **sistema** > **acerca de**

Busque el **compilación del sistema operativo** y **sistema tipo** campos.  
    ![Captura de pantalla de la compilación y el tipo de sistema de campos](media/system.png) 


Para buscar el número de compilación de Windows Server, ejecute lo siguiente en PowerShell:  
``` PowerShell
systeminfo | Select-String "^OS Name","^OS Version"
```

### <a name="confirm-wsl-is-enabled"></a>Confirme que está habilitado WSL
Puede confirmar que está habilitado el subsistema Windows para Linux ejecutando lo siguiente en PowerShell:  
``` PowerShell
PowerShell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

### <a name="openssh-server-connection-issues"></a>Problemas de conexión de OpenSSH-Server
Intentando conectar el servidor SSH se produjo el error siguiente: "Conexión cerrada por 127.0.0.1 puerto 22".
1. Asegúrese de que se está ejecutando el servidor de OpenSSH:
   ``` BASH
   sudo service ssh status
   ```
   y ha seguido este tutorial: https://help.ubuntu.com/lts/serverguide/openssh-server.html.en
2. Detener el servicio sshd e iniciar sshd en modo de depuración:
   ``` BASH
   sudo service ssh stop
   sudo /usr/sbin/sshd -d
   ```
3. Compruebe los registros de inicio y asegúrese de que existen las claves y no ve los mensajes de registro, como: debug1: versión sshd OpenSSH_7.2, OpenSSL 1.0.2g 1 de marzo de 2016 debug1: key_load_private: frase de contraseña incorrecta suministrado para descifrar debug1 clave privada: key_load_public : No existe tal archivo o directorio no se pudo cargar la clave de host: /etc/ssh/ssh_host_rsa_key debug1: key_load_private: Sin este tipo debug1 de archivo o directorio: key_load_public: No existe tal archivo o directorio no se pudo cargar la clave de host: /etc/ssh/ssh_host_dsa_key debug1: key_load_private: Sin este tipo debug1 de archivo o directorio: key_load_public: No existe tal archivo o directorio no se pudo cargar la clave de host: /etc/ssh/ssh_host_ecdsa_key debug1: key_load_private: Sin este tipo debug1 de archivo o directorio: key_load_public: No existe tal archivo o directorio no se pudo cargar la clave de host: /etc/ssh/ssh_host_ed25519_key

Si ve estos mensajes y faltan las claves bajo `/etc/ssh/`, tendrá que volver a generar las claves o simplemente purgar & instalar openssh-server:
```BASH
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```

