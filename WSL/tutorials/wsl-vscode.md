---
title: Introducción al uso de VS Code con el subsistema de Windows para Linux
description: Aprenda a configurar VS Code para crear y depurar código mediante el subsistema de Windows para Linux.
keywords: WSL, Windows, windowssubsystem, GNU, Linux, bash, vs Code, extensión remota, depuración, ruta de acceso, Visual Studio
ms.date: 05/28/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: b39b34644040354df44bf62ec7b878e3f5d667e6
ms.sourcegitcommit: b15b847b87d29a40de4a1517315949bce9c7a3d5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "91413346"
---
# <a name="get-started-using-visual-studio-code-with-windows-subsystem-for-linux"></a>Introducción al uso de Visual Studio Code con el subsistema de Windows para Linux

Visual Studio Code, junto con la extensión Remote-WSL, le permite usar WSL como su entorno de desarrollo a tiempo completo directamente desde VS Code. Puede:

* desarrollo en un entorno basado en Linux
* uso de utilidades y cadenas específicas de Linux
* Ejecute y Depure sus aplicaciones basadas en Linux desde la comodidad de Windows y mantenga el acceso a herramientas de productividad como Outlook y Office
* usar el terminal integrado VS Code para ejecutar la distribución de Linux de su elección
* Aproveche las ventajas de VS Code características como la [finalización del código de IntelliSense](https://code.visualstudio.com/docs/editor/intellisense), la detección de [errores, la](https://code.visualstudio.com/docs/python/linting) [compatibilidad con depuración](https://code.visualstudio.com/docs/nodejs/nodejs-debugging), [fragmentos de código](https://code.visualstudio.com/docs/editor/userdefinedsnippets)y [pruebas unitarias](https://code.visualstudio.com/docs/python/testing) .
* Administre fácilmente el control de versiones con la compatibilidad de [git](https://code.visualstudio.com/docs/editor/versioncontrol#_git-support) integrada con vs Code
* ejecutar comandos y extensiones de VS Code directamente en los proyectos de WSL
* edite archivos en el sistema de archivos de Windows de Linux o montados (por ejemplo,/mnt/c) sin preocuparse por problemas de problemas, compatibilidad binaria u otros desafíos entre sistemas operativos.

## <a name="install-vs-code-and-the-remote-wsl-extension"></a>Instalación de VS Code y la extensión WSL remota

* Visite la [página vs Code instalar](https://code.visualstudio.com/download) y seleccione el instalador de 32 o 64 bits. Instale Visual Studio Code en Windows (no en el sistema de archivos de WSL).

* Cuando se le pida que **Seleccione tareas adicionales durante la** instalación, asegúrese de activar la opción **Agregar a ruta de acceso** para que pueda abrir fácilmente una carpeta en WSL con el comando de código.

* Instale el [paquete de extensión de desarrollo remoto](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack). Este paquete de extensión incluye la extensión Remote-WSL, además de las extensiones remotas y de contenedores remotos, lo que permite abrir cualquier carpeta en un contenedor, en un equipo remoto o en WSL.

> [!IMPORTANT]
> Para instalar la extensión Remote-WSL, necesitará la versión [1,35](https://code.visualstudio.com/updates/v1_35) o posterior de vs Code. No se recomienda el uso de WSL en VS Code sin la extensión Remote-WSL, ya que se perderá la compatibilidad con Autocompletar, depuración, detección de errores, etc. Diversión: esta extensión WSL se instala en $HOME/.vscode/Extensions (escriba el comando `ls $HOME\.vscode\extensions\` en PowerShell).

## <a name="update-your-linux-distribution"></a>Actualización de la distribución de Linux

Algunas distribuciones de Linux de WSL carecen de bibliotecas requeridas por el servidor de VS Code para que se inicien. Puede agregar bibliotecas adicionales a la distribución de Linux mediante su administrador de paquetes.

Por ejemplo, para actualizar Debian o Ubuntu, use:

```bash
sudo apt-get update
```

Para agregar wget (para recuperar contenido de servidores Web) y certificados de entidad de certificación (para permitir que las aplicaciones basadas en SSL comprueben la autenticidad de las conexiones SSL), escriba:

```bash
sudo apt-get install wget ca-certificates
```

## <a name="open-a-wsl-project-in-visual-studio-code"></a>Abra un proyecto de WSL en Visual Studio Code

### <a name="from-the-command-line"></a>Desde la línea de comandos

Para abrir un proyecto desde la distribución de WSL, abra la línea de comandos de la distribución y escriba: `code .`

![Abrir el proyecto de WSL con VS Code servidor remoto](../media/wsl-open-vs-code.gif)

### <a name="from-vs-code"></a>Desde VS Code

También puede tener acceso a más VS Code opciones remotas mediante el método abreviado: `CTRL+SHIFT+P` en vs code para abrir la paleta de comandos. Si después escribe, `VSCODE-REMOTE` verá todos los vs Code opciones remotas disponibles, lo que le permite volver a abrir la carpeta en una sesión remota, especificar la distribución que desea abrir en, etc.

![Paleta de comandos de VS Code](../media/vscode-remote-command-palette.png)

## <a name="extensions-inside-of-vs-code-remote"></a>Extensiones dentro de VS Code remoto

La extensión Remote-WSL divide VS Code en una arquitectura "cliente-servidor", con el cliente (la interfaz de usuario) que se ejecuta en el equipo Windows y el servidor (el código, GIT, complementos, etc.) que se ejecuta de forma remota.

Al ejecutar VS Code remoto, al seleccionar la pestaña "extensiones" se mostrará una lista de las extensiones divididas entre el equipo local y la distribución de WSL.

La instalación de una extensión local, como un [tema](https://marketplace.visualstudio.com/search?target=VSCode&category=Themes&sortBy=Installs), solo debe instalarse una vez.

Algunas extensiones, como la [extensión de Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python) o cualquier elemento que controle cosas como la detección de errores o la depuración, deben instalarse por separado en cada distribuciones de WSL remotas. VS Code mostrará un icono de advertencia ⚠ , junto con un botón verde "instalar en WSL", si tiene instalada localmente una extensión que no está instalada en el WSL remoto.

![VS Code con extensiones remotas y extensiones locales de WSL](../media/vscode-remote-wsl-extensions.png)

Para obtener más información, consulte la VS Code docs:

* Cuando se inicia VS Code remoto en WSL, no se ejecuta ningún script de inicio de Shell. Consulte este [artículo de script de configuración de entorno avanzado](https://code.visualstudio.com/docs/remote/wsl#_advanced-environment-setup-script) para obtener más información sobre cómo ejecutar comandos adicionales o modificar el entorno.

* ¿Tiene problemas para iniciar VS Code desde la línea de comandos de WSL? Esta [Guía de solución de problemas](https://code.visualstudio.com/docs/remote/troubleshooting#_fixing-problems-with-the-code-command-not-working) incluye sugerencias para cambiar las variables de ruta de acceso, resolver errores de extensión sobre las dependencias que faltan, resolver problemas de finalización de línea de Git, instalar un VSIX local en un equipo remoto, iniciar una ventana del explorador, un puerto localhost del bloqueador, Web sockets no funciona, errores de almacenamiento de datos de extensión, etc.

## <a name="install-git-optional"></a>Instalar GIT (opcional)

Si planeas colaborar con otras personas u hospedar el proyecto en un sitio de código abierto (como GitHub), VS Code admite el [control de versiones con GIT](https://code.visualstudio.com/docs/editor/versioncontrol#_git-support). La pestaña Control de código fuente de VS Code realiza un seguimiento de todos los cambios y tiene comandos GIT comunes (agregar, confirmar, enviar cambios e incorporar cambios) integrados directamente en la interfaz de usuario.

Para instalar GIT, consulte [configuración de Git para trabajar con el subsistema de Windows para Linux](./wsl-git.md).

## <a name="install-windows-terminal-optional"></a>Instalación de Terminal Windows (opcional)

El nuevo terminal de Windows habilita varias pestañas (Cambie rápidamente entre el símbolo del sistema, PowerShell o varias distribuciones de Linux), enlaces de teclado personalizados (cree sus propias teclas de método abreviado para abrir o cerrar pestañas, copiar y pegar, etc.), emojis ☺ y temas personalizados (esquemas de colores, estilos y tamaños de fuente, imagen de fondo Obtenga más información en los [documentos de Windows terminal](/windows/terminal).

1. Obtenga [Terminal Windows en Microsoft Store](https://www.microsoft.com/store/apps/9n0dx20hk701): al instalar a través de Microsoft Store, las actualizaciones se controlan automáticamente.

2. Una vez instalado, abre Terminal Windows y selecciona **Configuración** para personalizar el terminal con el archivo `profile.json`.

## <a name="additional-resources"></a>Recursos adicionales

* [Desarrollo remoto VS Code](https://code.visualstudio.com/docs/remote/remote-overview)
* [Sugerencias y trucos de desarrollo remoto](https://code.visualstudio.com/docs/remote/troubleshooting)
* [Tutorial de desarrollo remoto con WSL](https://code.visualstudio.com/remote-tutorials/wsl/getting-started)
* [Uso de Docker con WSL 2 y VS Code](https://code.visualstudio.com/blogs/2020/03/02/docker-in-wsl2)
* [Usar C++ y WSL en VS Code](https://code.visualstudio.com/docs/cpp/config-wsl)
* [Servicio R remoto para Linux](/visualstudio/rtvs/setting-up-remote-r-service-on-linux)

Algunas de las extensiones adicionales que puedes considerar son las siguientes:

* [Keymaps from other editors](https://marketplace.visualstudio.com/search?target=VSCode&category=Keymaps&sortBy=Downloads): estas extensiones pueden ayudarte a sentirte como en casa con tu entorno en caso de que realices la transición desde otro editor de texto (como Atom, Sublime, Vim, eMacs, Notepad++, etc.).
* [Settings Sync](https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync): te permite sincronizar la configuración de VS Code entre diferentes instalaciones mediante GitHub. Si trabajas en diferentes máquinas, te ayuda a mantener el entorno coherente entre ellas.
* [Depurador para Chrome](https://code.visualstudio.com/blogs/2016/02/23/introducing-chrome-debugger-for-vs-code): una vez que haya terminado de desarrollar en el lado del servidor con Linux, deberá desarrollar y probar el lado cliente. Esta extensión integra el editor de VS Code con el servicio de depuración del explorador Chrome, lo que permite que las operaciones sean un poco más eficaces.
