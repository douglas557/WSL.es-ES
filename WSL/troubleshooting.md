---
title: Solución de problemas del subsistema de Windows para Linux
description: Proporciona información detallada sobre los errores comunes y los problemas que se producen en las personas que se ejecutan en Linux en el subsistema de Windows para Linux.
keywords: BashOnWindows, bash, WSL, Windows, windowssubsystem, Ubuntu
author: scooley
ms.author: scooley
ms.date: 11/15/2017
ms.topic: article
ms.assetid: 6753f1b2-200e-49cc-93a5-4323e1117246
ms.custom: seodec18
ms.openlocfilehash: 0c84fb710eca1b0ffabe437f98d5c17edbd6ea39
ms.sourcegitcommit: ead64b13501d6cb7170adafbb5624f4984a0af16
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/21/2019
ms.locfileid: "67307647"
---
# <a name="troubleshooting-windows-subsystem-for-linux"></a>Solución de problemas del subsistema de Windows para Linux

### <a name="bash-loses-network-connectivity-once-connected-to-a-vpn"></a>Bash pierde la conectividad de red una vez conectado a una VPN

Si después de conectarse a una VPN en Windows, bash pierde la conectividad de red, pruebe esta solución desde dentro de Bash. Esta solución le permitirá invalidar manualmente la resolución DNS a través `/etc/resolv.conf`de.

1. Tome nota del servidor DNS de la VPN.`ipconfig.exe /all`
2. Haga una copia del resolv. conf existente`sudo cp /etc/resolv.conf /etc/resolv.conf.new`
3. Desvincular el resolv actual. con`sudo unlink /etc/resolv.conf`
4. `sudo mv /etc/resolv.conf.new /etc/resolv.conf`
5. Abrir `/etc/resolv.conf` y <br/>
   a. Elimine la primera línea del archivo, que indica "\# este archivo fue generado automáticamente por WSL. Para detener la generación automática de este archivo, quite esta línea ". <br/>
   b. Agregue la entrada DNS de (1) anterior como la primera entrada de la lista de servidores DNS. <br/>
   c. Cierre el archivo. <br/>

Una vez que haya desconectado la VPN, tendrá que revertir los cambios a `/etc/resolv.conf`. Para ello, haga lo siguiente:
1. `cd /etc`
2. `sudo mv resolv.conf resolv.conf.new`
3. `sudo ln -s ../run/resolvconf/resolv.conf resolv.conf`

### <a name="starting-wsl-or-installing-a-distribution-returns-an-error-code"></a>Al iniciar WSL o al instalar una distribución, se devuelve un código de error

Siga [estas instrucciones](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs) para recopilar registros detallados y registrar un problema en github.

### <a name="updating-bash-on-ubuntu-on-windows"></a>Actualización de bash en Ubuntu en Windows

Hay dos componentes de bash en Ubuntu en Windows que pueden requerir actualización. 

1. El subsistema de Windows para Linux
  
   La actualización de esta parte de bash en Ubuntu en Windows habilitará las nuevas correcciones en las notas de la [versión](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes). Asegúrese de que está suscrito al programa Windows Insider y que la compilación está actualizada. Para un control granular más preciso, incluido el restablecimiento de la instancia de Ubuntu, consulte la [Página de referencia de comandos](https://msdn.microsoft.com/en-us/commandline/wsl/reference).

2. Los archivos binarios de usuario de Ubuntu 

   Al actualizar esta parte de bash en Ubuntu en Windows, se instalarán las actualizaciones de los archivos binarios de usuario de Ubuntu, incluidas las aplicaciones que se hayan instalado a través de apt-get. Para actualizar, ejecute los siguientes comandos en bash:
  
   1. `apt-get update`
   2. `apt-get upgrade`
  
### <a name="apt-get-upgrade-errors"></a>Apt: obtención de errores de actualización
Algunos paquetes usan características que aún no se han implementado. `udev`, por ejemplo, todavía no se admite y produce `apt-get upgrade` varios errores.

Para corregir los problemas relacionados `udev`con, siga estos pasos:

1. Escriba lo siguiente en `/usr/sbin/policy-rc.d` y guarde los cambios.
  
   ``` BASH
   #!/bin/sh
   exit 101
   ```
  
2. Agregar permisos de ejecución a`/usr/sbin/policy-rc.d`
   ``` BASH
   chmod +x /usr/sbin/policy-rc.d
   ```
  
3. Ejecute los siguientes comandos
   ``` BASH
   dpkg-divert --local --rename --add /sbin/initctl
   ln -s /bin/true /sbin/initctl
   ```
  
### <a name="error-0x80040306-on-installation"></a>"Error: 0x80040306 "en la instalación
Esto tiene que hacer con el hecho de que no se admite la consola heredada.
Para desactivar la consola heredada:

1. Abra cmd. exe
1. Haga clic con el botón derecho en barra de título-> Propiedades-> desactive usar consola heredada
1. Haga clic en Aceptar

### <a name="error-0x80040154-after-windows-update"></a>"Error: 0x80040154 "después de Windows Update
La característica subsistema de Windows para Linux puede estar deshabilitada durante una actualización de Windows. Si esto ocurre, se debe volver a habilitar la característica de Windows. Puede encontrar instrucciones para habilitar el subsistema de Windows para Linux en la [Guía de instalación](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui)de.

### <a name="changing-the-display-language"></a>Cambiar el idioma para mostrar
La instalación de WSL intentará cambiar automáticamente la configuración regional de Ubuntu para que coincida con la configuración regional de la instalación de Windows.  Si no desea este comportamiento, puede ejecutar este comando para cambiar la configuración regional de Ubuntu una vez finalizada la instalación.  Tendrá que reiniciar bash. exe para que este cambio surta efecto.

En el ejemplo siguiente se cambia a configuración regional a en-US:
``` BASH
sudo update-locale LANG=en_US.UTF8
```

### <a name="installation-issues-after-windows-system-restore"></a>Problemas de instalación después de restaurar sistema de Windows
1.  Elimine `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux` la carpeta. <br/>
  **Nota: No lo haga si su característica opcional está completamente instalada y en funcionamiento.**
2.  Habilitar la característica opcional WSL (si aún no lo está)
3.  Reiniciar
4.  lxrun/Uninstall/Full
5.  Instalación de Bash

### <a name="no-internet-access-in-wsl"></a>Sin acceso a Internet en WSL
Algunos usuarios han detectado problemas con aplicaciones de Firewall específicas que bloquean el acceso a Internet en WSL.  Los firewalls que se indican son:

1. Kaspersky
1. LATENCIA
1. Avast

En algunos casos, desactivar el Firewall permite el acceso.  En algunos casos, simplemente tener instalado el Firewall parece bloquear el acceso.

### <a name="permission-denied-error-when-using-ping"></a>Error de Permiso denegado al usar ping
#### <a name="anniversary-updatehttpsmsdnmicrosoftcomen-uscommandlinewslreleasenotesbuild-14388-to-windows-10-anniversary-update"></a>[Actualización de aniversario](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14388-to-windows-10-anniversary-update) 

Se requieren privilegios de administrador en Windows para ejecutar ping en WSL.  Para ejecutar ping, ejecute bash en Ubuntu en Windows como administrador o ejecute bash. exe desde un símbolo del sistema de CMD/PowerShell con privilegios de administrador.

#### <a name="build-14926httpsmsdnmicrosoftcomen-uscommandlinewslreleasenotesbuild-14926"></a>[Compilar 14926 +](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14926)
  Ya no se necesitan privilegios de administrador.

### <a name="bash-is-hung"></a>Bash está bloqueado
Si mientras trabaja con bash, observa que Bash está bloqueado (o interbloqueado) y no responde a las entradas, ayúdenos a diagnosticar el problema mediante la recopilación y la generación de informes de un volcado de memoria. Tenga en cuenta que en estos pasos se bloqueará el sistema. No lo haga si no está familiarizado con eso o guarde el trabajo antes de hacerlo.  <br/>
Para recopilar un volcado de memoria:
1. Cambie el tipo de volcado de memoria a "completar volcado de memoria". Al cambiar el tipo de volcado, tome nota del tipo actual.
2. Siga los [pasos](https://blogs.technet.microsoft.com/askpfeplat/2015/04/05/how-to-force-a-diagnostic-memory-dump-when-a-computer-hangs/) para configurar el bloqueo mediante el control de teclado.
3. Reproducir el bloqueo o el interbloqueo.
4. Bloquee el sistema con la secuencia de claves de (2).
5. El sistema se bloqueará y recopilará el volcado de memoria.
6. Una vez que se reinicie el sistema, informe de Memory. secure@microsoft.comDMP en. La ubicación predeterminada del archivo de volcado es%SystemRoot%\memory.dmp o C:\Windows\memory.dmp si C: es la unidad del sistema. En el correo electrónico, tenga en cuenta que el volcado de memoria es para el equipo de WSL o bash en Windows.
7. Restaure el tipo de volcado de memoria a la configuración original.

### <a name="check-your-build-number"></a>Comprobar el número de compilación

Para encontrar la arquitectura de su PC y el número de compilación de Windows, abra  
**Configuración** >  **del**sistema > 

Busque los campos **compilación de SO** y **tipo de sistema** .  
    ![Captura de pantalla de los campos de tipo de sistema y compilación](media/system.png) 


Para encontrar el número de compilación de Windows Server, ejecute lo siguiente en PowerShell:  
``` PowerShell
systeminfo | Select-String "^OS Name","^OS Version"
```

### <a name="confirm-wsl-is-enabled"></a>Confirmar que WSL está habilitado
Puede confirmar que el subsistema de Windows para Linux está habilitado mediante la ejecución de lo siguiente en PowerShell:  
``` PowerShell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

### <a name="openssh-server-connection-issues"></a>OpenSSH: problemas de conexión de servidor
Se produjo el siguiente error al intentar conectar el servidor SSH: "Conexión cerrada por el puerto 127.0.0.1 22".
1. Asegúrese de que el servidor OpenSSH se esté ejecutando:
   ``` BASH
   sudo service ssh status
   ```
   y ha seguido este tutorial: https://help.ubuntu.com/lts/serverguide/openssh-server.html.en
2. Detenga el servicio sshd e inicie sshd en modo de depuración:
   ``` BASH
   sudo service ssh stop
   sudo /usr/sbin/sshd -d
   ```
3. Compruebe los registros de inicio y asegúrese de que HostKeys estén disponibles y de que no vea los mensajes de registro como:
   ```
   debug1: sshd version OpenSSH_7.2, OpenSSL 1.0.2g  1 Mar 2016
   debug1: key_load_private: incorrect passphrase supplied to decrypt private key
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_rsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_dsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_ecdsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_ed25519_key
   ```

Si ve estos mensajes y faltan las claves en `/etc/ssh/`, tendrá que volver a generar las claves o simplemente purgar & instalar OpenSSH-Server:
```BASH
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```

