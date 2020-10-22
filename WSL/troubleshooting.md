---
title: Solucionar problemas del subsistema de Windows para Linux
description: Proporciona información detallada sobre los errores comunes y los problemas que se presentan a las personas cuando ejecutan Linux en el subsistema de Windows para Linux.
keywords: BashOnWindows, bash, wsl, windows, subsistemawindows, ubuntu
ms.date: 01/20/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: c3becde51cf16b95f96222a08a2fe7249cd936c1
ms.sourcegitcommit: dee2bf22c0c9f5725122a155d2876fcb2b7427d0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "92211759"
---
# <a name="troubleshooting-windows-subsystem-for-linux"></a>Solucionar problemas del subsistema de Windows para Linux

Para obtener ayuda para solucionar problemas relacionados con WSL, consulte nuestro [repositorio del producto WSL en GitHub](https://github.com/Microsoft/wsl/issues).

## <a name="search-for-any-existing-issues-related-to-your-problem"></a>Búsqueda de cualquier problema existente relacionado con tu problema

Si tiene problemas técnicos, use el [repositorio de productos](https://github.com/Microsoft/wsl/issues).

Si tiene problemas relacionados con el contenido de esta documentación, use el [repositorio de documentos](https://github.com/MicrosoftDocs/wsl/issues).

## <a name="submit-a-bug-report"></a>Envío de un informe de error

Para obtener información sobre errores relacionados con las funciones o características de WSL, presenta los detalles del problema en el repositorio del producto: https://github.com/Microsoft/wsl/issues.

## <a name="submit-a-feature-request"></a>Envío de una solicitud de característica

Para solicitar una nueva característica relacionada con la funcionalidad o compatibilidad de WSL, [presente los detalles del problema en el repositorio del producto](https://github.com/Microsoft/wsl/issues).

## <a name="contribute-to-the-docs"></a>Contribuir a los documentos

Para contribuir a la documentación de WSL, envía una solicitud de incorporación de cambios en el repositorio de documentos: https://github.com/MicrosoftDocs/wsl/issues.

## <a name="terminal-or-command-line"></a>Terminal o línea de comandos

Por último, si tu problema está relacionado con el Terminal Windows, la consola de Windows o la interfaz de usuario de la línea de comandos, usa el repositorio del Terminal Windows: https://github.com/microsoft/terminal.

## <a name="common-issues"></a>Problemas comunes

### <a name="im-on-windows-10-version-1903-and-i-still-do-not-see-options-for-wsl-2"></a>Tengo la versión 1903 de Windows 10 y sigo sin ver las opciones de WSL 2

Probablemente, se debe a que la máquina aún no ha adquirido la adaptación para WSL 2. La forma más sencilla de resolverlo es dirigirse a Configuración de Windows y hacer clic en "Buscar actualizaciones" para instalar las actualizaciones más recientes en el sistema. Consulte las [instrucciones completas sobre cómo adquirir la adaptación](https://devblogs.microsoft.com/commandline/wsl-2-support-is-coming-to-windows-10-versions-1903-and-1909/#how-do-i-get-it).

Si pulsa "Buscar actualizaciones" y sigue sin recibir la actualización, puede [instalar KB KB4566116 manualmente](https://www.catalog.update.microsoft.com/Search.aspx?q=KB4566116).  

### <a name="error-0x1bc-when-wsl---set-default-version-2"></a>Error: 0x1bc cuando `wsl --set-default-version 2`

Puede ocurrir cuando el valor de "Mostrar idioma" o "Configuración regional del sistema" no es Inglés.

```powershell
wsl --set-default-version 2
Error: 0x1bc
For information on key differences with WSL 2 please visit https://aka.ms/wsl2
```

El error real de `0x1bc` es:

```powershell
WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel
```

Para obtener más información, consulte el problema [5749](https://github.com/microsoft/WSL/issues/5749).

### <a name="cannot-access-wsl-files-from-windows"></a>No se puede acceder a los archivos WSL desde Windows

Un servidor de archivos de protocolo 9P proporciona el servicio en el lado de Linux para permitir que Windows tenga acceso al sistema de archivos de Linux. Si no puede acceder a WSL con `\\wsl$` en Windows, podría deberse a que 9P no se inició correctamente.

Para comprobarlo, puede consultar los registros de inicio mediante: `dmesg |grep 9p`, lo que le mostrará los errores. Una salida correcta se parece a la siguiente:

```bash
[    0.363323] 9p: Installing v9fs 9p2000 file system support
[    0.363336] FS-Cache: Netfs '9p' registered for caching
[    0.398989] 9pnet: Installing 9P2000 support
```

Consulte [este subproceso de Github](https://github.com/microsoft/wsl/issues/5307) para más explicaciones sobre este problema.

### <a name="cant-start-wsl-2-distribution-and-only-see-wsl-2-in-output"></a>No se puede iniciar la distribución WSL 2 y solo se ve "WSL 2" en la salida

Si el idioma para mostrar no es el inglés, es posible que vea una versión truncada de un texto de error.

```powershell
C:\Users\me>wsl
WSL 2
```

Para resolver este problema, visite `https://aka.ms/wsl2kernel` e instale el kernel manualmente siguiendo las instrucciones de esa página de documentación. 

### <a name="command-not-found-when-executing-windows-exe-in-linux"></a>Se muestra el mensaje `command not found` al ejecutar un archivo .exe de Windows en Linux

Los usuarios pueden ejecutar archivos ejecutables de Windows como notepad.exe directamente desde Linux. A veces, puede que se encuentre con el mensaje "comando no encontrado", como en el siguiente ejemplo: 

```Bash
$ notepad.exe
-bash: notepad.exe: command not found
```

Si no hay ninguna ruta de acceso Win32 en el parámetro $PATH, interop no encontrará el archivo .exe.
Para comprobarlo, puede ejecutar `echo $PATH` en Linux. Se espera que aparezca una ruta de acceso Win32 (por ejemplo, /mnt/c/Windows) en la salida.
Si no se muestra ninguna ruta de acceso de Windows, lo más probable es que el shell de Linux haya sobrescrito el parámetro PATH. 

A continuación se muestra un ejemplo en el que la ruta /etc/profile en Debian contribuyó al problema:

```Bash
if [ "`id -u`" -eq 0 ]; then
  PATH="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
else
  PATH="/usr/local/bin:/usr/bin:/bin:/usr/local/games:/usr/games"
fi
```

La manera correcta de hacerlo en Debian consiste en quitar las líneas anteriores.
También puede anexar el parámetro $PATH durante la asignación, como se indica a continuación. No obstante, esto genera [otros problemas](https://salsa.debian.org/debian/WSL/-/commit/7611edba482fd0b3f67143aa0fc1e2cc1d4100a6) con WSL y VSCode.

Si quiere obtener más información, consulte las incidencias [5296](https://github.com/microsoft/WSL/issues/5296) y [5779](https://github.com/microsoft/WSL/issues/5779).

### <a name="please-enable-the-virtual-machine-platform-windows-feature-and-ensure-virtualization-is-enabled-in-the-bios"></a>Habilite la característica de Windows de la plataforma de máquina virtual y asegúrese de que la virtualización esté habilitada en el BIOS.

Habilite la característica de Windows de plataforma de máquina virtual y asegúrese de que la virtualización esté habilitada en el BIOS.

1. Consulte [Requisitos de sistema de Hyper-V](/windows-server/virtualization/hyper-v/system-requirements-for-hyper-v-on-windows#:~:text=on%20Windows%20Server.-,General%20requirements,the%20processor%20must%20have%20SLAT.).

2. Si el equipo es una máquina virtual, habilite la [virtualización anidada](./wsl2-faq.md#can-i-run-wsl-2-in-a-virtual-machine) de forma manual. Inicie PowerShell como administrador y ejecute:

    ```powershell
    Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true
    ```

3. Siga las instrucciones del fabricante del equipo sobre cómo habilitar la virtualización. En general, esto puede implicar el uso del BIOS del sistema para asegurarse de que estas características se habilitan en la CPU. Las instrucciones para este proceso pueden variar de un equipo a otro. Consulte [este artículo](https://www.bleepingcomputer.com/tutorials/how-to-enable-cpu-virtualization-in-your-computer-bios/) de Bleeping Computer para ver un ejemplo.

4. Reinicie el equipo después de habilitar el componente opcional `Virtual Machine Platform`.

### <a name="bash-loses-network-connectivity-once-connected-to-a-vpn"></a>Bash pierde la conectividad de red una vez que se conecta a una VPN

Si después de conectarte a una VPN en Windows, Bash pierde la conectividad de red, prueba esta solución desde dentro de Bash. Esta solución alternativa te permitirá invalidar manualmente la resolución de DNS a través de `/etc/resolv.conf`.

1. Toma nota del servidor DNS de la VPN con `ipconfig.exe /all`
2. Haz una copia del resolv.conf existente `sudo cp /etc/resolv.conf /etc/resolv.conf.new`
3. Desvincula el elemento resolv.com actual `sudo unlink /etc/resolv.conf`
4. `sudo mv /etc/resolv.conf.new /etc/resolv.conf`
5. Abre `/etc/resolv.conf` y <br/>
   a. Elimina la primera línea del archivo, que indica "\# This file was automatically generated by WSL. To stop automatic generation of this file, remove this line" (WSL generó este archivo automáticamente. Para detener la generación automática de este archivo, quita esta línea). <br/>
   b. Agrega la entrada de DNS de (1) anterior como primera entrada de la lista de servidores DNS. <br/>
   c. Cierra el archivo. <br/>

Una vez que hayas desconectado la VPN, tendrás que revertir los cambios a `/etc/resolv.conf`. Para ello, haz lo siguiente:

1. `cd /etc`
2. `sudo mv resolv.conf resolv.conf.new`
3. `sudo ln -s ../run/resolvconf/resolv.conf resolv.conf`

### <a name="starting-wsl-or-installing-a-distribution-returns-an-error-code"></a>Iniciar WSL o instalar una distribución devuelve un código de error

Sigue [estas instrucciones](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs) para recopilar registros detallados y registrar un problema en GitHub.

### <a name="updating-bash-on-ubuntu-on-windows"></a>Actualizar Bash en Ubuntu en Windows

Hay dos componentes de Bash en Ubuntu en Windows que pueden requerir actualización.

1. El subsistema de Windows para Linux
  
   La actualización de esta parte de Bash en Ubuntu en Windows habilitará las nuevas correcciones en las [notas de la versión](./release-notes.md). Asegúrate de estar suscrito al Programa Windows Insider y de que la compilación esté actualizada. Para un control más preciso, incluido el restablecimiento de la instancia de Ubuntu, consulte la [página de referencia de comandos](./reference.md).

2. Los archivos binarios de usuario de Ubuntu

   Al actualizar esta parte de Bash en Ubuntu en Windows, se instalarán las actualizaciones de los archivos binarios de usuario de Ubuntu, incluidas las aplicaciones que se hayan instalado a través de apt-get. Para actualizar, ejecuta los comandos siguientes en Bash:
  
   1. `apt-get update`
   2. `apt-get upgrade`
  
### <a name="apt-get-upgrade-errors"></a>Errores de actualización de apt-get

Algunos paquetes usan características que aún no se han implementado. `udev`, por ejemplo, todavía no se admite y produce varios errores de tipo `apt-get upgrade`.

Para corregir los problemas relacionados con `udev`, sigue estos pasos:

1. Escribe lo siguiente en `/usr/sbin/policy-rc.d` y guarda los cambios.
  
   ```bash
   #!/bin/sh
   exit 101
   ```
  
2. Agrega los permisos de ejecución en `/usr/sbin/policy-rc.d`:

   ```bash
   chmod +x /usr/sbin/policy-rc.d
   ```
  
3. Ejecute los siguientes comandos:

   ```bash
   dpkg-divert --local --rename --add /sbin/initctl
   ln -s /bin/true /sbin/initctl
   ```
  
### <a name="error-0x80040306-on-installation"></a>"Error: 0x80040306" en la instalación

Esto se relaciona con el hecho de que no se admite la consola heredada.
Para desactivar la consola heredada:

1. Abre cmd.exe.
1. Haz clic con el botón derecho en barra de título -> Propiedades-> desactiva Usar consola heredada.
1. Haga clic en Aceptar

### <a name="error-0x80040154-after-windows-update"></a>"Error: 0x80040154" después de una actualización de Windows

La característica Subsistema de Windows para Linux puede deshabilitarse durante una actualización de Windows. Si esto ocurre, debes volver a habilitar la característica de Windows. Las instrucciones para habilitar el subsistema de Windows para Linux se pueden encontrar en la [guía de instalación](./install-win10.md).

### <a name="changing-the-display-language"></a>Cambiar el idioma de visualización

La instalación de WSL intentará cambiar automáticamente la configuración regional de Ubuntu para que coincida con la configuración regional de la instalación de Windows.  Si no quieres que esto pase, puedes ejecutar este comando para cambiar la configuración regional de Ubuntu una vez finalizada la instalación.  Ten en cuenta que tendrás que reiniciar bash.exe para que este cambio surta efecto.

En el ejemplo siguiente se cambia la configuración regional a en-US:

```bash
sudo update-locale LANG=en_US.UTF8
```

### <a name="installation-issues-after-windows-system-restore"></a>Problemas de instalación después de una restauración del sistema de Windows

1. Elimina la carpeta `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux`. <br/>
  **Nota: No lo hagas si tu característica opcional está completamente instalada y en funcionamiento.**
2. Habilitar la característica opcional WSL (si aún no lo está)
3. Reiniciar
4. lxrun /uninstall /full
5. Instala bash.

### <a name="no-internet-access-in-wsl"></a>Sin acceso a Internet en WSL

Algunos usuarios han informado de problemas con aplicaciones de firewall específicas que bloquean el acceso a Internet en WSL.  Los firewalls que dan error son:

1. Kaspersky
2. AVG
3. Avast

En algunos casos, si desactivas el firewall podrás acceder.  En otros casos, simplemente tener instalado el firewall parece bloquear el acceso a Internet.

### <a name="permission-denied-error-when-using-ping"></a>Error de permiso denegado al usar ping

En cuanto a la [Actualización de aniversario de Windows (versión 1607)](./release-notes.md#build-14388-to-windows-10-anniversary-update), es necesario tener **privilegios de administrador** en Windows para ejecutar ping en WSL.  Para ejecutar ping, ejecuta Bash en Ubuntu en Windows como administrador o ejecuta bash.exe desde un símbolo del sistema de CMD/PowerShell con privilegios de administrador.

Para versiones posteriores de Windows ([compilación 14926+](./release-notes.md#build-14926)) ya no es necesario tener privilegios de administrador.

### <a name="bash-is-hung"></a>Bash se bloquea

Si mientras trabajas con Bash, ves que Bash se bloquea (o interbloquea) y no responde a las entradas, ayúdanos a diagnosticar el problema mediante la recopilación y la generación de informes de un volcado de memoria. Ten en cuenta que con estos pasos se bloqueará tu sistema. No lo hagas si no te sientes cómodo al hacerlo o guarda el trabajo antes de hacerlo.

Para recopilar un volcado de memoria

1. Cambia el tipo de volcado de memoria a "volcado de memoria completa". Al cambiar el tipo de volcado, toma nota del tipo actual.

2. Sigue los [pasos](https://techcommunity.microsoft.com/t5/Core-Infrastructure-and-Security/How-to-Force-a-Diagnostic-Memory-Dump-When-a-Computer-Hangs/ba-p/257809) para configurar el bloqueo mediante el control de teclado.

3. Reproduce el bloqueo o interbloqueo.

4. Bloquea el sistema con la secuencia de claves de (2).

5. El sistema se bloqueará y recopilará el volcado de memoria.

6. Una vez que se reinicie el sistema, informa memory.dmp a secure@microsoft.com. La ubicación predeterminada del archivo de volcado es %SystemRoot%\memory.dmp o C:\Windows\memory.dmp si C: es la unidad del sistema. En el correo electrónico, indica que el volcado de memoria es para el equipo de WSL o de Bash en Windows.

7. Restaura el tipo de volcado de memoria a la configuración original.

### <a name="check-your-build-number"></a>Comprobar el número de compilación

Para encontrar la arquitectura de tu PC y el número de compilación de Windows, abre:  
**Configuración** > **Sistema** > **Acerca de**

Busca los campos **Compilación del SO** y **Tipo de sistema**.  
    ![Captura de pantalla de los campos Compilación del SO y Tipo de sistema](media/system.png)

Para encontrar el número de compilación de Windows Server, ejecuta lo siguiente en PowerShell:  

``` PowerShell
systeminfo | Select-String "^OS Name","^OS Version"
```

### <a name="confirm-wsl-is-enabled"></a>Confirmar que WSL está habilitado

Puedes confirmar que el subsistema de Windows para Linux está habilitado mediante la ejecución de lo siguiente en PowerShell:  

``` PowerShell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

### <a name="openssh-server-connection-issues"></a>Problemas de conexión del servidor de OpenSSH

Al intentar conectarte al servidor SSH se produce el error siguiente: "Connection closed by 127.0.0.1 port 22" (Conexión cerrada por 127.0.0.1 puerto 22).

1. Asegúrate de que el servidor OpenSSH esté en ejecución:

   ```bash
   sudo service ssh status
   ```

   y que has seguido este tutorial: https://help.ubuntu.com/lts/serverguide/openssh-server.html.en

2. Detén el servicio sshd e inicia sshd en modo de depuración:

   ```bash
   sudo service ssh stop
   sudo /usr/sbin/sshd -d
   ```

3. Comprueba los registros de inicio y asegúrate de que HostKeys estén disponibles y de no ver mensajes de registro como:

   ```BASH
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

Si ves estos mensajes y faltan las claves en `/etc/ssh/`, tendrás que volver a generar las claves o simplemente purgar e instalar el servidor OpenSSH:

```BASH
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```

### <a name="the-referenced-assembly-could-not-be-found-when-enabling-the-wsl-optional-feature"></a>"No se pudo encontrar el ensamblado al que se hace referencia". al habilitar la característica opcional WSL

Este error está relacionado con un estado de instalación incorrecta. Complete los pasos siguientes para intentar corregir este problema:

- Si estás ejecutando el comando para habilitar la característica WSL desde PowerShell, intenta usar la GUI en su lugar desde el menú Inicio: busca "activar o desactivar las características de Windows" y, a continuación, en la lista, selecciona "Subsistema de Windows para Linux", lo que instalará el componente opcional.

- Actualiza la versión de Windows. Para ello, ve a Configuración, Actualizaciones y haz clic en "Buscar actualizaciones".

- Si se produce un error en ambos casos y necesitas acceder a WSL, considera la posibilidad de realizar una actualización local. Para ello, vuelve a instalar Windows 10 con los medios de instalación y selecciona "Conservar todo" para asegurarte de que las aplicaciones y los archivos se conservan. Puedes encontrar instrucciones sobre cómo hacerlo en la página [Reinstalar Windows 10](https://support.microsoft.com/help/4000735/windows-10-reinstall).

### <a name="correct-ssh-related-permission-errors"></a>Corrección de errores de permisos (relacionados con SSH)

Si ves este error:

```bash
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@         WARNING: UNPROTECTED PRIVATE KEY FILE!          @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
Permissions 0777 for '/home/artur/.ssh/private-key.pem' are too open.
```

Para corregirlo, anexa lo siguiente al archivo ```/etc/wsl.conf```:

```bash
[automount]
enabled = true
options = metadata,uid=1000,gid=1000,umask=0022
```

Ten en cuenta que, al agregar este comando, se incluirán metadatos y se modificarán los permisos de archivo en los archivos de Windows que se muestran en WSL. Para obtener más información, consulta los [Permisos del sistema de archivos](./file-permissions.md).
