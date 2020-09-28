---
title: Introducción al uso de contenedores de Docker con el subsistema de Windows para Linux
description: Aprenda a configurar contenedores de Docker en el subsistema de Windows para Linux.
keywords: WSL, Windows, windowssubsystem, Windows 10, Docker, contenedores
ms.date: 08/28/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: 5a1187336341d73f662b7e9f27b19df4fd0e1e73
ms.sourcegitcommit: b15b847b87d29a40de4a1517315949bce9c7a3d5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "91413336"
---
# <a name="get-started-with-docker-remote-containers-on-wsl-2"></a>Introducción a los contenedores remotos de Docker en WSL 2

Esta guía paso a paso le ayudará a empezar a desarrollar con los contenedores remotos mediante la **configuración de Docker Desktop para Windows con WSL 2** (subsistema de Windows para Linux, versión 2).

Docker Desktop para Windows está disponible de forma gratuita y proporciona un entorno de desarrollo para compilar, enviar y ejecutar aplicaciones de ha aplicado Docker. Al habilitar el motor basado en WSL 2, puede ejecutar contenedores de Linux y Windows en Docker Desktop en el mismo equipo.

## <a name="overview-of-docker-containers"></a>Introducción a los contenedores de Docker

Docker es una herramienta que se usa para crear, implementar y ejecutar aplicaciones mediante contenedores. Los contenedores permiten a los desarrolladores empaquetar una aplicación con todas las partes que necesita (bibliotecas, marcos de trabajo, dependencias, etc.) y enviar todo como un paquete. El uso de un contenedor garantiza que la aplicación se ejecutará de la misma forma, independientemente de la configuración personalizada o de las bibliotecas instaladas anteriormente en el equipo en el que se ejecute, que podría diferir del equipo que se usó para escribir y probar el código de la aplicación. Esto permite a los desarrolladores centrarse en la escritura de código sin preocuparse por el sistema en el que se ejecutará el código.

Los contenedores de Docker son similares a las máquinas virtuales, pero no crean un sistema operativo virtual completo. En su lugar, Docker permite a la aplicación usar el mismo kernel de Linux que el sistema en el que se ejecuta. Esto permite que el paquete de la aplicación solo requiera partes que aún no existen en el equipo host, lo que reduce el tamaño del paquete y mejora el rendimiento.

La disponibilidad continua, mediante el uso de contenedores de Docker con herramientas como [Kubernetes](/azure/aks/), es otro motivo para la popularidad de los contenedores. Esto permite crear varias versiones del contenedor de la aplicación en momentos diferentes. En lugar de tener que deshacer todo el sistema para las actualizaciones o el mantenimiento, cada contenedor y sus microservicios específicos se pueden reemplazar sobre la marcha. Puedes preparar un nuevo contenedor con todas las actualizaciones, configurar el contenedor para producción y simplemente apuntar al nuevo contenedor una vez que esté listo. También puedes archivar versiones diferentes de la aplicación mediante contenedores y mantenerlas en ejecución como reserva de seguridad si es necesario.

Para obtener más información, consulte la [Introducción a los contenedores de Docker](/learn/modules/intro-to-docker-containers/) en Microsoft Learn.

## <a name="prerequisites"></a>Requisitos previos

- Asegúrese de que el equipo ejecuta Windows 10, [actualizado a la versión 2004](ms-settings:windowsupdate), **compilación 18362** o posterior.
- [Habilite WSL, instale una distribución de Linux y actualice a WSL 2](../install-win10.md).
- [Descargue e instale el paquete de actualización del kernel de Linux](/windows/wsl/wsl2-kernel).
- [Instale Visual Studio Code](https://code.visualstudio.com/download) *(opcional)*. Esto proporcionará la mejor experiencia, incluida la capacidad de codificar y depurar dentro de un contenedor de Docker remoto y conectarse a la distribución de Linux.
- [Instale Windows terminal](/windows/terminal/get-started) *(opcional)*. Esto proporcionará la mejor experiencia, incluida la capacidad de personalizar y abrir varios terminales en la misma interfaz (como Ubuntu, Debian, PowerShell, CLI de Azure o cualquier cosa que prefiera usar).
- [Regístrese para obtener un ID. de Docker en Docker Hub](https://hub.docker.com/signup) *(opcional)*.

> [!NOTE]
> WSL puede ejecutar distribuciones en el modo WSL versión 1 o WSL 2. Para comprobarlo, abra PowerShell y escriba: `wsl -l -v` . Asegúrese de que la distribución está configurada para usar WSL 2; para ello, escriba: `wsl --set-version  <distro> 2` . Reemplace `<distro>` por el nombre de distribución (por ejemplo, Ubuntu 18,04).
> 
> En la versión 1 de WSL, debido a las diferencias fundamentales entre Windows y Linux, el motor de Docker no se pudo ejecutar directamente dentro de WSL, por lo que el equipo de Docker desarrolló una solución alternativa con máquinas virtuales de Hyper-V y LinuxKit. Sin embargo, como WSL 2 se ejecuta ahora en un kernel de Linux con capacidad de llamada completa del sistema, Docker puede ejecutarse por completo en WSL 2. Esto significa que los contenedores de Linux se pueden ejecutar de forma nativa sin emulación, lo que da como resultado un mejor rendimiento e interoperabilidad entre las herramientas de Windows y Linux.

## <a name="install-docker-desktop"></a>Instalación de Docker Desktop

Con el back-end de WSL 2 compatible con Docker Desktop para Windows, puede trabajar en un entorno de desarrollo basado en Linux y compilar contenedores basados en Linux, mientras usa Visual Studio Code para la edición y depuración de código, y para ejecutar el contenedor en el explorador Microsoft Edge en Windows.

Para instalar Docker (después de [instalar WSL 2](../install-win10.md)):

1. Descargue [Docker Desktop](https://docs.docker.com/docker-for-windows/wsl/#download) y siga las instrucciones de instalación.

2. Una vez instalado, inicie Docker Desktop desde el menú Inicio de Windows y, a continuación, seleccione el icono de Docker en el menú iconos ocultos de la barra de tareas. Haga clic con el botón derecho en el icono para que se muestre el menú de comandos de Docker y seleccione "configuración".
    ![Icono de panel de escritorio de Docker](../media/docker-starting.png)

3. Asegúrese de que la opción "usar el motor basado en WSL 2" está activada en la **configuración**  >  **General**.
    ![Configuración general de Docker Desktop](../media/docker-running.png)

4. Seleccione en las distribuciones instaladas de WSL 2 en las que desea habilitar la integración de Docker; para ello, vaya a: **configuración**  >  **recursos**  >  **WSL integración**.
    ![Configuración de recursos de escritorio de Docker](../media/docker-dashboard.png)

5. Para confirmar que se ha instalado Docker, abra una distribución de WSL (por ejemplo, Ubuntu) y muestre la versión y el número de compilación. para ello, escriba: `docker --version`

6. Compruebe que la instalación funciona correctamente mediante la ejecución de una imagen de Docker integrada simple mediante: `docker run hello-world`

> [!TIP]
> Estos son algunos comandos útiles de Docker que debe conocer:
>
> - Enumerar los comandos disponibles en la CLI de Docker, para lo que debes escribir: `docker`
> - Enumerar información de un comando específico con: `docker <COMMAND> --help`
> - Enumerar las imágenes de Docker en el equipo (que es simplemente la imagen de Hola mundo en este momento), con: `docker image ls --all`
> - Enumerar los contenedores del equipo, con: `docker container ls --all` o `docker ps -a` (sin la marca-a mostrar todo, solo se mostrarán los contenedores en ejecución)
> - Muestra información de todo el sistema relacionada con la instalación de Docker, incluidas las estadísticas y los recursos (CPU & memoria) disponibles en el contexto de WSL 2, con: `docker info`

## <a name="develop-in-remote-containers-using-vs-code"></a>Desarrollo en contenedores remotos con VS Code

Para empezar a desarrollar aplicaciones mediante Docker con WSL 2, se recomienda usar VS Code, junto con la extensión Remote-WSL y la extensión de Docker.

- [Instale la extensión vs Code Remote-WSL](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl). Esta extensión permite abrir el proyecto de Linux que se ejecuta en WSL en VS Code (no es necesario preocuparse de los problemas relacionados con la acción, la compatibilidad binaria u otros desafíos entre OS).

- [Instale la extensión de contenedores remotos de vs Code](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers). Esta extensión permite abrir la carpeta del proyecto o el repositorio dentro de un contenedor, aprovechando el conjunto completo de características de Visual Studio Code para realizar el trabajo de desarrollo en el contenedor.

- [Instale la extensión de Docker de vs Code](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker). Esta extensión agrega la funcionalidad para compilar, administrar e implementar aplicaciones en contenedores desde VS Code. (Necesita la extensión de contenedor remoto para usar realmente el contenedor como su entorno de desarrollo).

Vamos a usar Docker para crear un contenedor de desarrollo para un proyecto de aplicación existente.

1. En este ejemplo, usaré el código fuente del tutorial de [Hola mundo para Django](/windows/python/web-frameworks#hello-world-tutorial-for-django) en el entorno de desarrollo de Python configurar docs. Puede omitir este paso si prefiere usar su propio código fuente del proyecto. Para descargar mi aplicación web HelloWorld-Django desde GitHub, abra un terminal de WSL (por ejemplo, Ubuntu) y escriba: `git clone https://github.com/mattwojo/helloworld-django.git`

    > [!NOTE]
    > Almacene siempre el código en el mismo sistema de archivos en el que está usando las herramientas de. Esto dará lugar a un rendimiento de acceso a archivos más rápido. En este ejemplo, se usa un distribución de Linux (Ubuntu) y se quieren almacenar los archivos de proyecto en el sistema de archivos WSL `\\wsl\` . El almacenamiento de archivos de proyecto en el sistema de archivos de Windows ralentizaría considerablemente el uso de las herramientas de Linux en WSL para tener acceso a esos archivos.

2. En el terminal WSL, cambie los directorios a la carpeta de código fuente de este proyecto:

    ```bash
    cd helloworld-django
    ```

3. Abra el proyecto en VS Code que se ejecuta en el servidor de extensión local-WSL. para ello, escriba:

    ```bash
    code .
    ```

    Confirme que está conectado a WSL Linux distribución. para ello, compruebe el indicador remoto verde en la esquina inferior izquierda de la instancia de VS Code.

    ![VS Code indicador remoto de WSL](../media/vscode-remote-indicator.png)

4. En el comando VS Code paleta (Ctrl + Mayús + P), escriba: **contenedores remotos: abrir carpeta en contenedor...** Si este comando no aparece cuando empieza a escribirlo, asegúrese de que ha instalado la extensión de contenedor remoto vinculada anteriormente.

    ![VS Code comando de contenedor remoto](../media/docker-extension.png)

5. Seleccione la carpeta del proyecto que desea incluir en el contenedor. En mi caso, esto es `\\wsl\Ubuntu-20.04\home\mattwojo\repos\helloworld-django\`

    ![VS Code carpeta de contenedores remotos](../media/docker-extension2.png)

6. Se mostrará una lista de definiciones de contenedor, ya que todavía no hay ninguna configuración de DevContainer en la carpeta del proyecto (repositorio). La lista de definiciones de configuración de contenedor que aparece se filtra según el tipo de proyecto. En mi proyecto de Django, seleccionaremos Python 3.

    ![VS Code definiciones de configuración de contenedor remoto](../media/docker-extension3.png)

7. Se abrirá una nueva instancia de VS Code, comenzará a compilar la nueva imagen y, una vez completada la compilación, iniciará el contenedor. Verá que aparece una nueva `.devcontainer` carpeta con información de configuración de contenedor en un `Dockerfile` archivo y `devcontainer.json` .  

    ![VS Code carpeta. devcontainer](../media/docker-extension4.png)

8. Para confirmar que el proyecto sigue conectado a WSL y dentro de un contenedor, abra el VS Code terminal integrado (Ctrl + Mayús + ~). Compruebe el sistema operativo escribiendo: `uname` y la versión de Python con: `python3 --version` . Puede ver que uname llegó como "Linux", por lo que sigue conectado al motor de WSL 2 y el número de versión de Python se basará en la configuración del contenedor que puede diferir de la versión de Python instalada en la distribución de WSL.

9. Para ejecutar y depurar la aplicación dentro del contenedor mediante Visual Studio Code, primero abra el menú **Ejecutar** (Ctrl + Mayús + D o seleccione la pestaña en la barra de menús de la izquierda). A continuación, seleccione **Ejecutar y depurar** para seleccionar una configuración de depuración y elija la configuración que mejor se adapte a su proyecto (en mi ejemplo, será "Django"). Se creará un `launch.json` archivo en la `.vscode` carpeta del proyecto con instrucciones sobre cómo ejecutar la aplicación.

    ![VS Code ejecutar la configuración de depuración](../media/vscode-run-config.png)

10. Desde dentro vs Code, seleccione **Ejecutar**  >  **iniciar depuración** (o simplemente presione la tecla **F5** ). Se abrirá un terminal dentro de VS Code y verá un resultado que indica algo parecido a: "iniciando el servidor de desarrollo en http://127.0.0.1:8000/ salir del servidor con control-C". Mantenga presionada la tecla control y seleccione la dirección que se muestra para abrir la aplicación en el explorador Web predeterminado y vea el proyecto que se ejecuta dentro de su contenedor.

    ![VS Code de ejecución de un contenedor de Docker](../media/vscode-running-in-container.png)

Ahora ha configurado correctamente un contenedor de desarrollo remoto mediante Docker Desktop, basado en el back-end de WSL 2, que puede codificar en, compilar, ejecutar, implementar o depurar mediante VS Code.

## <a name="troubleshooting"></a>Solución de problemas

### <a name="wsl-docker-context-deprecated"></a>Contexto de Docker de WSL desusado

Si usaba una versión preliminar técnica temprana de Docker para WSL, puede tener un contexto de Docker llamado "WSL" que ahora está en desuso y ya no se usa. Puede comprobar con el comando: `docker context ls` . Puede quitar este contexto "WSL" para evitar errores con el comando: `docker context rm wsl` como desea usar el contexto predeterminado para Windows y WSL2.

Entre los posibles errores que se pueden encontrar con este contexto de WSL en desuso se incluyen los siguientes: `docker wsl open //./pipe/docker_wsl: The system cannot find the file specified.` o `error during connect: Get http://%2F%2F.%2Fpipe%2Fdocker_wsl/v1.40/images/json?all=1: open //./pipe/docker_wsl: The system cannot find the file specified.`

Para obtener más información sobre este problema, consulte [configuración de Docker en el sistema Windows para Linux (WSL2) en Windows 10](https://www.hanselman.com/blog/HowToSetUpDockerWithinWindowsSystemForLinuxWSL2OnWindows10.aspx).

### <a name="trouble-finding-docker-image-storage-folder"></a>Problemas al buscar la carpeta de almacenamiento de imágenes de Docker

Docker crea dos carpetas distribución para almacenar los datos:
- \\WSL $ \docker-Desktop
- \\WSL $ \docker-Desktop-Data

Para encontrar estas carpetas, abra la distribución de WSL Linux y escriba: `explorer.exe .` para ver la carpeta en el explorador de archivos de Windows. Entrar: `\\wsl\<distro name>\mnt\wsl` reemplace `<distro name>` por el nombre de la distribución (es decir, Ubuntu-20,04) para ver estas carpetas.

Obtenga más información sobre la ubicación de las ubicaciones de almacenamiento de Docker en WSL, consulte este [problema desde el repositorio WSL](https://github.com/microsoft/WSL/issues/4176) o esta [publicación StackOverlow](https://stackoverflow.com/questions/62380124/where-docker-image-is-stored-with-docker-desktop-for-windows).

Para obtener más ayuda con los problemas generales de solución de problemas de WSL, consulte el documento de [solución de problemas](../troubleshooting.md) .

## <a name="additional-resources"></a>Recursos adicionales

- [Documentos de Docker: procedimientos recomendados para el escritorio de Docker con WSL 2](https://docs.docker.com/docker-for-windows/wsl/#best-practices)
- [Comentarios de Docker Desktop para Windows: archivo de un problema](https://github.com/docker/for-win/issues)
- [Blog de VS Code: directrices para elegir un entorno de desarrollo](https://code.visualstudio.com/docs/containers/choosing-dev-environment#_guidelines-for-choosing-a-development-environment)
- [Blog de VS Code: uso de Docker en WSL 2](https://code.visualstudio.com/blogs/2020/03/02/docker-in-wsl2)
- [Blog de VS Code: uso de contenedores remotos en WSL 2](https://code.visualstudio.com/blogs/2020/07/01/containers-wsl)
- [Hanselminutes podcast: creación de Docker adorable para desarrolladores con Simon Ferquel](https://hanselminutes.com/736/making-docker-lovely-for-developers-with-simon-ferquel)