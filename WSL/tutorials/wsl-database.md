---
title: Introducción al uso de MySQL MongoDB, PostgreSQL, SQLite, Microsoft SQL Server o Redis para configurar una base de datos en el subsistema de Windows para Linux
description: Aprenda a configurar MySQL MongoDB, PostgreSQL, SQLite, Microsoft SQL Server o Redis en el subsistema de Windows para Linux.
keywords: WSL, Windows, windowssubsystem, MySQL MongoDB, PostgreSQL, SQLite, Microsoft SQL Server, Redis, Windows 10
ms.date: 07/07/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: 561af482e245892156a02fe287b95867ef80ded1
ms.sourcegitcommit: ba3399a5ffeffd23551315acd04ea6848d30693b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/17/2020
ms.locfileid: "90719134"
---
# <a name="get-started-with-databases-on-windows-subsystem-for-linux"></a>Introducción a las bases de datos en el subsistema de Windows para Linux

Esta guía paso a paso le ayudará a comenzar a conectar el proyecto en WSL a una base de datos de. Introducción a MySQL, PostgreSQL, MongoDB, Redis, Microsoft SQL Server o SQLite.

## <a name="prerequisites"></a>Requisitos previos

- Ejecutar Windows 10, [actualizado a la versión 2004](ms-settings:windowsupdate), **compilación 19041** o posterior.
- [WSL habilitado e instalado y actualizado a WSL 2](https://docs.microsoft.com/windows/wsl/install-win10).
- [Distribución de Linux instalada](https://docs.microsoft.com/windows/wsl/install-win10#step-6---install-your-linux-distribution-of-choice) (Ubuntu 18,04 para nuestros ejemplos).
- Asegúrese de que la distribución de Ubuntu 18,04 se está [ejecutando en el modo WSL 2](https://docs.microsoft.com/windows/wsl/install-win10#set-your-distribution-version-to-wsl-1-or-wsl-2). (WSL puede ejecutar distribuciones en el modo V1 o V2). Para comprobarlo, abra PowerShell y escriba: `wsl -l -v`

## <a name="differences-between-database-systems"></a>Diferencias entre los sistemas de base de datos

Las [opciones más populares](https://insights.stackoverflow.com/survey/2019#technology-_-databases) para un sistema de base de datos incluyen:

- [MySQL](https://www.mysql.com/why-mysql/) (SQL)
- [PostgreSQL](https://www.postgresql.org/about/) (SQL)
- [Microsoft SQL Server](https://docs.microsoft.com/sql) (SQL)
- [SQLite](https://www.sqlite.org/about.html) (SQL)
- [MongoDB](https://www.mongodb.com/what-is-mongodb) (NoSQL)
- [Redis](https://redis.io/topics/introduction) (NoSQL)

**MySQL** es una base de datos relacional de SQL de código abierto que organiza los datos en una o más tablas en las que los tipos de datos se pueden relacionar entre sí. Se puede escalar verticalmente, lo que significa que una máquina Ultimate realizará el trabajo por usted. Actualmente, es la más utilizada de los cuatro sistemas de base de datos.

**PostgreSQL** (a veces conocido como Postgres) es también una base de datos relacional de SQL de código abierto con un énfasis en la extensibilidad y el cumplimiento de estándares. Ahora también puede controlar JSON, pero por lo general funciona mejor para los datos estructurados, el escalado vertical y las necesidades compatibles con ACID, como el comercio electrónico y las transacciones financieras.

**Microsoft SQL Server** incluye SQL Server en Windows, SQL Server en Linux y SQL en Azure. También se trata de sistemas de administración de bases de datos relacionales configurados en servidores con la función principal de almacenar y recuperar datos según lo soliciten las aplicaciones de software.

**SQLite** es una base de datos independiente de código abierto basada en archivos, "sin servidor", conocida por su portabilidad, confiabilidad y buen rendimiento, incluso en entornos de memoria insuficiente.

**MongoDB** es una base de datos de documentos NoSQL de código abierto diseñada para trabajar con JSON y almacenar datos sin esquemas. Se puede escalar horizontalmente, lo que significa que varias máquinas más pequeñas realizarán el trabajo por usted. Es conveniente para la flexibilidad y los datos no estructurados, y para almacenar en memoria caché el análisis en tiempo real.

**Redis** es un almacén de estructuras de datos en memoria NoSQL de código abierto. Usa pares clave-valor para el almacenamiento en lugar de documentos. Redis se conoce por su flexibilidad, rendimiento y soporte de lenguaje amplio. Es lo suficientemente flexible como para usarse como una caché o un agente de mensajes y puede usar estructuras de datos como listas, conjuntos y valores hash.

El tipo de base de datos que elijas debería depender del tipo de aplicación con la que vayas a usar la base de datos. Te recomendamos que busques las ventajas y desventajas de las bases de datos estructuradas y no estructuradas y elijas la que te vaya mejor según el caso de uso.

## <a name="install-mysql"></a>Instalar MySQL

Para instalar MySQL en WSL (Ubuntu 18,04):

1. Abre el terminal de WSL (es decir, Ubuntu 18.04).
2. Actualiza los paquetes de Ubuntu: `sudo apt update`.
3. Una vez actualizados los paquetes, instale MySQL con: `sudo apt install mysql-server`
4. Confirma la instalación y obtén el número de versión `mysql --version`.

También puede que desee ejecutar el script de seguridad incluido. Esto cambia algunas de las opciones predeterminadas menos seguras para elementos como inicios de sesión de raíz remota y usuarios de ejemplo. Para ejecutar el script de seguridad:

1. Iniciar un servidor de MySQL: `sudo /etc/init.d/mysql start`
2. Iniciar los mensajes del script de seguridad: `sudo mysql_secure_installation`
3. En el primer mensaje se le preguntará si desea configurar el complemento validar contraseña, que se puede usar para probar la seguridad de la contraseña de MySQL. A continuación, establecerá una contraseña para el usuario raíz de MySQL, decidirá si desea quitar usuarios anónimos, decidir si desea permitir que el usuario raíz inicie sesión tanto de forma local como remota, decidir si desea quitar la base de datos de prueba y, por último, decidir si desea recargar las tablas de privilegios inmediatamente.

Para abrir el símbolo del sistema de MySQL, escriba: `sudo mysql`

Para ver las bases de datos que tiene disponibles, en el símbolo del sistema de MySQL, escriba: `SHOW DATABASES;`

Para crear una nueva base de datos, escriba: `CREATE DATABASE database_name;`

Para eliminar una base de datos, escriba: ` DROP DATABASE database_name;`

Para más información sobre cómo trabajar con las bases de datos de MySQL, consulte los [documentos de MySQL](https://dev.mysql.com/doc/mysql-getting-started/en/).

Para trabajar con las bases de datos MySQL en VS Code, pruebe la [extensión MySQL](https://marketplace.visualstudio.com/items?itemName=cweijan.vscode-mysql-client2).

## <a name="install-postgresql"></a>Instalación de PostgreSQL

Para instalar PostgreSQL en WSL (Ubuntu 18,04):

1. Abre el terminal de WSL (es decir, Ubuntu 18.04).
2. Actualiza los paquetes de Ubuntu: `sudo apt update`.
3. Una vez que los paquetes se hayan actualizado, instala PostgreSQL (y el paquete -contrib que tenga algunas utilidades útiles) con: `sudo apt install postgresql postgresql-contrib`.
4. Confirma la instalación y obtén el número de versión `psql --version`.

Hay 3 comandos que debes conocer una vez instales PostgreSQL:

- `sudo service postgresql status` para comprobar el estado de la base de datos.
- `sudo service postgresql start` para empezar a ejecutar la base de datos.
- `sudo service postgresql stop` para detener la ejecución de la base de datos.

El usuario administrador predeterminado, `postgres`, necesita tener una contraseña asignada para poder conectarse a una base de datos. Para establecer una contraseña:

1. Escribe el comando: `sudo passwd postgres`.
2. Recibirás un aviso para escribir la nueva contraseña.
3. Cierra y vuelve a abrir el terminal.

Para ejecutar PostgreSQL con el shell de [psql](https://www.postgresql.org/docs/10/app-psql.html) :

1. Inicia el servicio Postgres: `sudo service postgresql start`.
2. Conéctate al servicio Postgres y abre el shell de psql: `sudo -u postgres psql`.

Una vez que hayas escrito correctamente el shell de psql, verás que el cambio de la línea de comandos tiene el siguiente aspecto: `postgres=#`.

> [!NOTE]
> Como alternativa, puedes abrir el shell de psql si cambias al usuario Postgres por `su - postgres` y, a continuación, escribes el comando `psql`.

Para salir de Postgres = # Enter: `\q` o use la tecla de método abreviado: Ctrl + D

Para ver qué cuentas de usuario se han creado en la instalación de PostgreSQL, usa `psql -c "\du"`desde el terminal WSL o simplemente `\du`, si tienes abierto el shell de psql. Este comando mostrará las columnas: nombre de usuario de la cuenta, lista de atributos de roles y miembro de los grupos de roles. Para salir y volver a la línea de comandos, escribe `q`.

Para obtener más información sobre cómo trabajar con las bases de datos de PostgreSQL, consulte los [documentos de PostgreSQL](https://www.postgresql.org/docs/13/tutorial-createdb.html).

Para trabajar con las bases de datos de PostgreSQL en VS Code, pruebe la [extensión PostgreSQL](https://marketplace.visualstudio.com/items?itemName=ms-ossdata.vscode-postgresql).

## <a name="install-mongodb"></a>Instalación de MongoDB

Para instalar MongoDB en WSL (Ubuntu 18,04):

1. Abre el terminal de WSL (es decir, Ubuntu 18.04).
2. Actualiza los paquetes de Ubuntu: `sudo apt update`.
3. Una vez actualizados los paquetes, instala MongoDB con `sudo apt-get install mongodb`.
4. Confirma la instalación y obtén el número de versión `mongod --version`.

Hay 3 comandos que debes conocer una vez instales MongoDB:

- `sudo service mongodb status` para comprobar el estado de la base de datos.
- `sudo service mongodb start` para empezar a ejecutar la base de datos.
- `sudo service mongodb stop` para detener la ejecución de la base de datos.

> [!NOTE]
> Es posible que veas que el comando `sudo systemctl status mongodb` se utiliza en tutoriales o artículos. Para mantenerse ligero, WSL no incluye `systemd` (un sistema de administración de servicios de Linux). En su lugar, usa SysVinit para iniciar los servicios en la máquina. No debías notar ninguna diferencia, pero si un tutorial recomienda usar `sudo systemctl`, usa `sudo /etc/init.d/` en su lugar. Por ejemplo, para WSL, `sudo systemctl status mongodb` sería `sudo /etc/inid.d/mongodb status`, pero también puedes usar `sudo service mongodb status`.

Para ejecutar la base de datos Mongo en un servidor local:

1. Comprobar el estado de la base de datos: `sudo service mongodb status` debería ver una respuesta [error], a menos que ya haya iniciado la base de datos.

2. Inicie la base de datos: `sudo service mongodb start` ahora debería ver una respuesta [OK].

3. Para comprobarlo, conéctese al servidor de base de datos y ejecute un comando de diagnóstico: `mongo --eval 'db.runCommand({ connectionStatus: 1 })'` esto generará la versión actual de la base de datos, la dirección del servidor y el puerto, y la salida del comando status. El valor `1` para el campo "Aceptar" en la respuesta indica que el servidor funciona.

4. Para detener la ejecución del servicio MongoDB, escribe `sudo service mongodb stop`.

> [!NOTE]
> MongoDB tiene varios parámetros predeterminados, incluido el almacenamiento de datos en /data/db y la ejecución en el puerto 27017. Así mismo, `mongod` es el demonio (proceso de host para la base de datos) y `mongo` es el shell de la línea de comandos que se conecta a una instancia específica de `mongod`.

VS Code admite el trabajo con bases de datos de MongoDB a través de la [extensión CosmosDB de Azure](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-cosmosdb), puede crear, administrar y consultar bases de datos de mongodb desde vs Code. Para obtener más información, visite el VS Code docs: [trabajar con MongoDB](https://code.visualstudio.com/docs/azure/mongodb).

Obtenga más información en los documentos de MongoDB:

- [Introducción al uso de MongoDB](https://docs.mongodb.com/manual/introduction/)
- [Creación de usuarios](https://docs.mongodb.com/manual/tutorial/create-users/)
- [Conexión a una instancia de MongoDB en un host remoto](https://docs.mongodb.com/manual/mongo/#mongodb-instance-on-a-remote-host)
- [CRUD: crear, leer, actualizar, eliminar](https://docs.mongodb.com/manual/crud/)
- [Documentos de referencia](https://docs.mongodb.com/manual/reference/)

## <a name="install-microsoft-sql-server"></a>Instalar Microsoft SQL Server

Para instalar SQL Server en WSL (Ubuntu 18,04), siga esta guía de inicio rápido: [instalación de SQL Server y creación de una base de datos en Ubuntu](https://docs.microsoft.com/sql/linux/quickstart-install-connect-ubuntu).

Para trabajar con bases de datos de Microsoft SQL Server en VS Code, pruebe la [extensión MSSQL](https://marketplace.visualstudio.com/items?itemName=ms-mssql.mssql).

## <a name="install-sqlite"></a>Instalación de SQLite

Para instalar SQLite en WSL (Ubuntu 18,04):

1. Abre el terminal de WSL (es decir, Ubuntu 18.04).
2. Actualiza los paquetes de Ubuntu: `sudo apt update`.
3. Una vez actualizados los paquetes, instale SQLite3 con: `sudo apt install sqlite3`
4. Confirma la instalación y obtén el número de versión `sqlite3 --version`.

Para crear una base de datos de prueba, denominada "example. dB", escriba: `sqlite3 example.db`

Para ver una lista de las bases de datos de SQLite, escriba: `.databases`

Para ver el estado de la base de datos, escriba: `.dbinfo ?DB?`

Para salir del aviso de SQLite, escriba: `.exit`

Para obtener más información sobre cómo trabajar con una base de datos de SQLite, consulte los [documentos de SQLite](https://www.sqlite.org/quickstart.html).

Para trabajar con las bases de datos de SQLite en VS Code, pruebe la [extensión de SQLite](https://marketplace.visualstudio.com/items?itemName=mtxr.sqltools).

## <a name="install-redis"></a>Instalación de Redis

Para instalar Redis en WSL (Ubuntu 18,04):

1. Abre el terminal de WSL (es decir, Ubuntu 18.04).
2. Actualiza los paquetes de Ubuntu: `sudo apt update`.
3. Una vez actualizados los paquetes, instale Redis con: `sudo apt install redis-server`
4. Confirma la instalación y obtén el número de versión `redis-server --version`.

Para empezar a ejecutar el servidor de Redis: `sudo service redis-server start`

Compruebe si Redis funciona (Redis-CLI es la utilidad de la interfaz de la línea de comandos para comunicarse con Redis): `redis-cli ping` debe devolver una respuesta de "pong".

Para detener la ejecución del servidor de Redis: `sudo service redis-server stop`

Para obtener más información sobre cómo trabajar con una base de datos de Redis, consulte los [documentos de Redis](https://redis.io/topics/quickstart).

Para trabajar con las bases de datos de Redis en VS Code, pruebe la [extensión Redis](https://marketplace.visualstudio.com/items?itemName=cweijan.vscode-redis-client).

## <a name="see-services-running-and-set-up-profile-aliases"></a>Ver los servicios en ejecución y configurar alias de perfil

Para ver los servicios que se están ejecutando actualmente en la distribución de WSL, escriba: `service --status-all`

Escribir `sudo service mongodb start` o `sudo service postgres start` y `sudo -u postgrest psql` puede resultar tedioso.  Sin embargo, puedes considerar la posibilidad de configurar los alias en el archivo `.profile` de WSL para que estos comandos sean más rápidos de usar y más fáciles de recordar.

Para configurar tu propio alias personalizado, o acceso directo, a fin de ejecutar estos comandos:

1. Abre el terminal de WSL y escribe `cd ~` para asegurarte de que te encuentras en el directorio raíz.
2. Abre el archivo `.profile`, que controla la configuración del terminal, con el editor de texto de terminal Nano: `sudo nano .profile`.
3. En la parte inferior del archivo (no cambies la configuración `# set PATH`), agrega lo siguiente:

    ```bash
    # My Aliases
    alias start-pg='sudo service postgresql start'
    alias run-pg='sudo -u postgres psql'
    ```

    Esto te permitirá escribir `start-pg` para empezar a ejecutar el servicio PostgreSQL y `run-pg` para abrir el shell psql. Puedes cambiar `start-pg` y `run-pg` a cualquier nombre que quieras, pero ten cuidado de no sobrescribir un comando que Postgres ya uses.

4. Una vez que hayas agregado los nuevos alias, sal del editor de texto de Nano con **Control + X**, selecciona `Y` (Sí) cuando se te pida que guardes y presiona Entrar (el nombre de archivo debe ser `.profile`).
5. Cierra y vuelve a abrir el terminal de WSL y, a continuación, prueba los nuevos comandos de alias.

## <a name="additional-resources"></a>Recursos adicionales

- [Configurar el entorno de desarrollo en Windows 10](https://docs.microsoft.com/windows/dev-environment/)
