---
title: Introducción al uso de Git en el subsistema de Windows para Linux
description: Obtenga información sobre cómo configurar git para el control de versiones en el subsistema de Windows para Linux.
keywords: WSL, Windows, windowssubsystem, GNU, Linux, bash, GIT, GitHub, control de versiones
ms.date: 06/04/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: 94166371fc0928d6be3b3cfd6cb595c6fac76608
ms.sourcegitcommit: d95bdbc2fea991ba14a4c9ec53ee0ec19d6bbdb4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/05/2020
ms.locfileid: "84457797"
---
# <a name="get-started-using-git-on-windows-subsystem-for-linux"></a>Introducción al uso de Git en el subsistema de Windows para Linux

Git es el sistema de control de versiones que se usa con más frecuencia. Con git, puede realizar un seguimiento de los cambios que realice en los archivos, por lo que tiene un registro de lo que se ha hecho y tiene la capacidad de revertir a versiones anteriores de los archivos si es necesario. Git también facilita la colaboración, lo que permite combinar varios usuarios en un solo origen.

## <a name="git-can-be-installed-on-windows-and-on-wsl"></a>GIT se puede instalar en Windows y en WSL

Una consideración importante: al habilitar WSL e instalar una distribución de Linux, está instalando un nuevo sistema de archivos, separado de Windows NTFS C:\. en el equipo. En Linux, las unidades no tienen letras. Se les proporcionan puntos de montaje. La raíz del sistema de archivos `/` es el punto de montaje de la partición raíz, o carpeta, en el caso de WSL. No todo lo `/` que hay en es la misma unidad. Por ejemplo, en mi portátil, he instalado dos versiones de Ubuntu (20,04 y 18,01), así como Debian. Si abro esas distribuciones, selecciona el directorio raíz con el comando `cd ~` y, a continuación, escribe el comando `explorer.exe .` , se abrirá el explorador de archivos de Windows y se mostrará la ruta de acceso del directorio para esa distribución.

| Distribución de Linux | Ruta de acceso de Windows para acceder a la carpeta principal |
| ----------- | ----------- |
| Ubuntu 20.04 | `\\wsl$\Ubuntu-20.04\home\username` |
| Ubuntu 18,01 | `\\wsl$\Ubuntu-18.04\home\username` |
| Debian | `\\wsl$\Debian\home\username` |
| Windows PowerShell | `C:\Users\username` |

> [!TIP]
> Si está buscando tener acceso al directorio de archivos de Windows desde la línea de comandos de distribución de WSL, en lugar de `C:\Users\username` , se puede obtener acceso al directorio mediante `/mnt/c/Users/username` , ya que la distribución de Linux visualiza el sistema de archivos de Windows como una unidad montada.

Deberá instalar git en cada sistema de archivos con el que quiera usarlo.

![Mostrar las versiones de Git por distribución](../media/git-versions.gif)

## <a name="installing-git"></a>Installing Git

Git ya está instalado con la mayoría de las distribuciones del subsistema de Windows para Linux. sin embargo, es posible que quiera actualizar a la versión más reciente y que tendrá que configurar el archivo de configuración de Git.

Para instalar GIT, consulte el sitio [de descarga de Git para Linux](https://git-scm.com/download/linux) . Cada distribución de Linux tiene su propio administrador de paquetes e comando de instalación. Por ejemplo, para instalar git en la distribución Alpine, use: `apk add git` . También puede que desee [instalar git para Windows](https://git-scm.com/download/win) si aún no lo ha hecho.

## <a name="git-config-file-setup"></a>Configuración del archivo de configuración de Git

Para configurar el archivo de configuración de Git, abra una línea de comandos para la distribución en la que está trabajando y escriba: `git config --global user.name "Your Name"` y, después, `git config --global user.email "youremail@domain.com"` . Reemplazar el contenido entre comillas por el nombre y la dirección de correo electrónico que usó para crear su cuenta de Git.

> [!TIP]
> Si aún no tienes una cuenta de GIT, puedes [registrarte para crear una en GitHub](https://github.com/join). Si nunca has trabajado con GIT, las [guías de GitHub](https://guides.github.com/) pueden resultarte de ayuda para empezar. Si tienes que editar la configuración de GIT, puedes hacerlo con un editor de texto integrado como nano: `nano ~/.gitconfig`.

Le recomendamos que [Proteja su cuenta con la autenticación en dos fases (2FA)](https://help.github.com/en/github/authenticating-to-github/securing-your-account-with-two-factor-authentication-2fa).

## <a name="git-credential-manager-setup"></a>Instalación del administrador de credenciales de Git

El administrador de credenciales de Git le permite autenticar un servidor GIT remoto, incluso si tiene un patrón de autenticación complejo como la autenticación en dos fases, Azure Active Directory o el uso de direcciones URL remotas SSH que requieren una contraseña de clave SSH para cada extracción de Git. El Administrador de credenciales de GIT se integra en el flujo de autenticación para servicios como GitHub y, una vez que se ha autenticado en el proveedor de hospedaje, solicita un nuevo token de autenticación. A continuación, almacena el token de forma segura en el [Administrador de credenciales de Windows](https://support.microsoft.com/help/4026814/windows-accessing-credential-manager). Después de la primera vez, puede usar GIT para comunicarse con el proveedor de hospedaje sin necesidad de volver a autenticarse. Solo accederá al token en el Administrador de credenciales de Windows.

Para configurar el Administrador de credenciales de GIT para su uso con una distribución de WSL, abra la distribución y escriba este comando:

```Bash
git config --global credential.helper "/mnt/c/Program\ Files/Git/mingw64/libexec/git-core/git-credential-manager.exe"
```

Ahora, cualquier operación de GIT que realice dentro de la distribución de WSL usará el Administrador de credenciales. Si ya tiene credenciales almacenadas en caché para un host, accederá a estas desde el Administrador de credenciales. Si no es así, recibirá una respuesta de diálogo que le solicitará sus credenciales, aunque esté en una consola Linux.

## <a name="adding-a-git-ignore-file"></a>Agregar un archivo de omisión de Git

Se recomienda agregar un [archivo. gitignore](https://help.github.com/en/articles/ignoring-files) a los proyectos. GitHub ofrece [una colección de plantillas. gitignore útiles con las](https://github.com/github/gitignore) configuraciones de archivos. gitignore recomendadas organizadas según el caso de uso.

Si decide [crear un nuevo repositorio mediante el sitio web de github](https://help.github.com/articles/create-a-repo), hay casillas disponibles para inicializar el repositorio con un archivo Léame, el archivo. gitignore configurado para el tipo de proyecto específico y las opciones para agregar una licencia, si es necesario.

## <a name="git-and-vs-code"></a>Git y VS Code

Visual Studio Code incluye compatibilidad integrada con git, incluida una pestaña de control de código fuente que mostrará los cambios y controle una variedad de comandos de Git. Más información sobre [la compatibilidad de Git de vs Code](https://code.visualstudio.com/docs/editor/versioncontrol#_git-support).

## <a name="git-line-endings"></a>Fin de línea de Git

Si está trabajando con la misma carpeta de repositorio entre Windows, WSL o un contenedor, asegúrese de configurar finales de línea coherentes.

Dado que Windows y Linux usan distintos finales de línea predeterminados, GIT puede informar de un gran número de archivos modificados que no tienen ninguna diferencia con respecto a los finales de línea. Para evitar que esto suceda, puede deshabilitar la conversión de final de línea mediante un `.gitattributes` archivo o globalmente en el lado de Windows. Vea este [vs Code documento sobre cómo resolver problemas de finalización de línea de Git](https://code.visualstudio.com/docs/remote/troubleshooting#_resolving-git-line-ending-issues-in-containers-resulting-in-many-modified-files).

## <a name="additional-resources"></a>Recursos adicionales

* [& WSL VS Code](./wsl-vscode.md)
* [Laboratorio de aprendizaje de GitHub: cursos en línea](https://lab.github.com/)
* [Herramienta de visualización de Git](http://git-school.github.io/visualizing-git/)
* [Herramientas de git: almacenamiento de credenciales](https://git-scm.com/book/it/v2/Git-Tools-Credential-Storage)
