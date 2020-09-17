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
# <a name="get-started-with-databases-on-windows-subsystem-for-linux"></a><span data-ttu-id="e4e58-104">Introducción a las bases de datos en el subsistema de Windows para Linux</span><span class="sxs-lookup"><span data-stu-id="e4e58-104">Get started with databases on Windows Subsystem for Linux</span></span>

<span data-ttu-id="e4e58-105">Esta guía paso a paso le ayudará a comenzar a conectar el proyecto en WSL a una base de datos de.</span><span class="sxs-lookup"><span data-stu-id="e4e58-105">This step-by-step guide will help you get started connecting your project in WSL to a database.</span></span> <span data-ttu-id="e4e58-106">Introducción a MySQL, PostgreSQL, MongoDB, Redis, Microsoft SQL Server o SQLite.</span><span class="sxs-lookup"><span data-stu-id="e4e58-106">Get started with MySQL, PostgreSQL, MongoDB, Redis, Microsoft SQL Server, or SQLite.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e4e58-107">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e4e58-107">Prerequisites</span></span>

- <span data-ttu-id="e4e58-108">Ejecutar Windows 10, [actualizado a la versión 2004](ms-settings:windowsupdate), **compilación 19041** o posterior.</span><span class="sxs-lookup"><span data-stu-id="e4e58-108">Running Windows 10, [updated to version 2004](ms-settings:windowsupdate), **Build 19041** or higher.</span></span>
- <span data-ttu-id="e4e58-109">[WSL habilitado e instalado y actualizado a WSL 2](https://docs.microsoft.com/windows/wsl/install-win10).</span><span class="sxs-lookup"><span data-stu-id="e4e58-109">[WSL enabled and installed, and updated to WSL 2](https://docs.microsoft.com/windows/wsl/install-win10).</span></span>
- <span data-ttu-id="e4e58-110">[Distribución de Linux instalada](https://docs.microsoft.com/windows/wsl/install-win10#step-6---install-your-linux-distribution-of-choice) (Ubuntu 18,04 para nuestros ejemplos).</span><span class="sxs-lookup"><span data-stu-id="e4e58-110">[Linux distribution installed](https://docs.microsoft.com/windows/wsl/install-win10#step-6---install-your-linux-distribution-of-choice) (Ubuntu 18.04 for our examples).</span></span>
- <span data-ttu-id="e4e58-111">Asegúrese de que la distribución de Ubuntu 18,04 se está [ejecutando en el modo WSL 2](https://docs.microsoft.com/windows/wsl/install-win10#set-your-distribution-version-to-wsl-1-or-wsl-2).</span><span class="sxs-lookup"><span data-stu-id="e4e58-111">Ensure your Ubuntu 18.04 distribution is [running in WSL 2 mode](https://docs.microsoft.com/windows/wsl/install-win10#set-your-distribution-version-to-wsl-1-or-wsl-2).</span></span> <span data-ttu-id="e4e58-112">(WSL puede ejecutar distribuciones en el modo V1 o V2). Para comprobarlo, abra PowerShell y escriba: `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="e4e58-112">(WSL can run distributions in both v1 or v2 mode.) You can check this by opening PowerShell and entering: `wsl -l -v`</span></span>

## <a name="differences-between-database-systems"></a><span data-ttu-id="e4e58-113">Diferencias entre los sistemas de base de datos</span><span class="sxs-lookup"><span data-stu-id="e4e58-113">Differences between database systems</span></span>

<span data-ttu-id="e4e58-114">Las [opciones más populares](https://insights.stackoverflow.com/survey/2019#technology-_-databases) para un sistema de base de datos incluyen:</span><span class="sxs-lookup"><span data-stu-id="e4e58-114">The most [popular choices](https://insights.stackoverflow.com/survey/2019#technology-_-databases) for a database system include:</span></span>

- <span data-ttu-id="e4e58-115">[MySQL](https://www.mysql.com/why-mysql/) (SQL)</span><span class="sxs-lookup"><span data-stu-id="e4e58-115">[MySQL](https://www.mysql.com/why-mysql/) (SQL)</span></span>
- <span data-ttu-id="e4e58-116">[PostgreSQL](https://www.postgresql.org/about/) (SQL)</span><span class="sxs-lookup"><span data-stu-id="e4e58-116">[PostgreSQL](https://www.postgresql.org/about/) (SQL)</span></span>
- <span data-ttu-id="e4e58-117">[Microsoft SQL Server](https://docs.microsoft.com/sql) (SQL)</span><span class="sxs-lookup"><span data-stu-id="e4e58-117">[Microsoft SQL Server](https://docs.microsoft.com/sql) (SQL)</span></span>
- <span data-ttu-id="e4e58-118">[SQLite](https://www.sqlite.org/about.html) (SQL)</span><span class="sxs-lookup"><span data-stu-id="e4e58-118">[SQLite](https://www.sqlite.org/about.html) (SQL)</span></span>
- <span data-ttu-id="e4e58-119">[MongoDB](https://www.mongodb.com/what-is-mongodb) (NoSQL)</span><span class="sxs-lookup"><span data-stu-id="e4e58-119">[MongoDB](https://www.mongodb.com/what-is-mongodb) (NoSQL)</span></span>
- <span data-ttu-id="e4e58-120">[Redis](https://redis.io/topics/introduction) (NoSQL)</span><span class="sxs-lookup"><span data-stu-id="e4e58-120">[Redis](https://redis.io/topics/introduction) (NoSQL)</span></span>

<span data-ttu-id="e4e58-121">**MySQL** es una base de datos relacional de SQL de código abierto que organiza los datos en una o más tablas en las que los tipos de datos se pueden relacionar entre sí.</span><span class="sxs-lookup"><span data-stu-id="e4e58-121">**MySQL** is an open-source SQL relational database, organizing data into one or more tables in which data types may be related to each other.</span></span> <span data-ttu-id="e4e58-122">Se puede escalar verticalmente, lo que significa que una máquina Ultimate realizará el trabajo por usted.</span><span class="sxs-lookup"><span data-stu-id="e4e58-122">It is vertically scalable, which means one ultimate machine will do the work for you.</span></span> <span data-ttu-id="e4e58-123">Actualmente, es la más utilizada de los cuatro sistemas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="e4e58-123">It is currently the most widely used of the four database systems.</span></span>

<span data-ttu-id="e4e58-124">**PostgreSQL** (a veces conocido como Postgres) es también una base de datos relacional de SQL de código abierto con un énfasis en la extensibilidad y el cumplimiento de estándares.</span><span class="sxs-lookup"><span data-stu-id="e4e58-124">**PostgreSQL** (sometimes referred to as Postgres) is also an open-source SQL relational database with an emphasis on extensibility and standards compliance.</span></span> <span data-ttu-id="e4e58-125">Ahora también puede controlar JSON, pero por lo general funciona mejor para los datos estructurados, el escalado vertical y las necesidades compatibles con ACID, como el comercio electrónico y las transacciones financieras.</span><span class="sxs-lookup"><span data-stu-id="e4e58-125">It can handle JSON now too, but it is generally better for structured data, vertical scaling, and ACID-compliant needs like eCommerce and financial transactions.</span></span>

<span data-ttu-id="e4e58-126">**Microsoft SQL Server** incluye SQL Server en Windows, SQL Server en Linux y SQL en Azure.</span><span class="sxs-lookup"><span data-stu-id="e4e58-126">**Microsoft SQL Server** includes SQL Server on Windows, SQL Server on Linux, and SQL on Azure.</span></span> <span data-ttu-id="e4e58-127">También se trata de sistemas de administración de bases de datos relacionales configurados en servidores con la función principal de almacenar y recuperar datos según lo soliciten las aplicaciones de software.</span><span class="sxs-lookup"><span data-stu-id="e4e58-127">These are also relational database management systems set up on servers with primary function of storing and retrieving data as requested by software applications.</span></span>

<span data-ttu-id="e4e58-128">**SQLite** es una base de datos independiente de código abierto basada en archivos, "sin servidor", conocida por su portabilidad, confiabilidad y buen rendimiento, incluso en entornos de memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="e4e58-128">**SQLite** is an open-source self-contained, file-based, “serverless” database, known for its portability, reliability, and good performance even in low-memory environments.</span></span>

<span data-ttu-id="e4e58-129">**MongoDB** es una base de datos de documentos NoSQL de código abierto diseñada para trabajar con JSON y almacenar datos sin esquemas.</span><span class="sxs-lookup"><span data-stu-id="e4e58-129">**MongoDB** is an open-source NoSQL document database designed to work with JSON and store schema-free data.</span></span> <span data-ttu-id="e4e58-130">Se puede escalar horizontalmente, lo que significa que varias máquinas más pequeñas realizarán el trabajo por usted.</span><span class="sxs-lookup"><span data-stu-id="e4e58-130">It is horizontally scalable, which means multiple smaller machines will do the work for you.</span></span> <span data-ttu-id="e4e58-131">Es conveniente para la flexibilidad y los datos no estructurados, y para almacenar en memoria caché el análisis en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="e4e58-131">It's good for flexibility and unstructured data, and caching real-time analytics.</span></span>

<span data-ttu-id="e4e58-132">**Redis** es un almacén de estructuras de datos en memoria NoSQL de código abierto.</span><span class="sxs-lookup"><span data-stu-id="e4e58-132">**Redis** is is an open-source NoSQL in-memory data structure store.</span></span> <span data-ttu-id="e4e58-133">Usa pares clave-valor para el almacenamiento en lugar de documentos.</span><span class="sxs-lookup"><span data-stu-id="e4e58-133">It uses key-value pairs for storage instead of documents.</span></span> <span data-ttu-id="e4e58-134">Redis se conoce por su flexibilidad, rendimiento y soporte de lenguaje amplio.</span><span class="sxs-lookup"><span data-stu-id="e4e58-134">Redis is known for its flexibility, performance, and wide language support.</span></span> <span data-ttu-id="e4e58-135">Es lo suficientemente flexible como para usarse como una caché o un agente de mensajes y puede usar estructuras de datos como listas, conjuntos y valores hash.</span><span class="sxs-lookup"><span data-stu-id="e4e58-135">It’s flexible enough to be used as a cache or message broker and can use data structures like lists, sets, and hashes.</span></span>

<span data-ttu-id="e4e58-136">El tipo de base de datos que elijas debería depender del tipo de aplicación con la que vayas a usar la base de datos.</span><span class="sxs-lookup"><span data-stu-id="e4e58-136">The sort of database you choose should depend on the type of application you will be using the database with.</span></span> <span data-ttu-id="e4e58-137">Te recomendamos que busques las ventajas y desventajas de las bases de datos estructuradas y no estructuradas y elijas la que te vaya mejor según el caso de uso.</span><span class="sxs-lookup"><span data-stu-id="e4e58-137">We recommend that you look up the advantages and disadvantages of structured and unstructured databases and choose based on your use case.</span></span>

## <a name="install-mysql"></a><span data-ttu-id="e4e58-138">Instalar MySQL</span><span class="sxs-lookup"><span data-stu-id="e4e58-138">Install MySQL</span></span>

<span data-ttu-id="e4e58-139">Para instalar MySQL en WSL (Ubuntu 18,04):</span><span class="sxs-lookup"><span data-stu-id="e4e58-139">To install MySQL on WSL (Ubuntu 18.04):</span></span>

1. <span data-ttu-id="e4e58-140">Abre el terminal de WSL (es decir, Ubuntu 18.04).</span><span class="sxs-lookup"><span data-stu-id="e4e58-140">Open your WSL terminal (ie. Ubuntu 18.04).</span></span>
2. <span data-ttu-id="e4e58-141">Actualiza los paquetes de Ubuntu: `sudo apt update`.</span><span class="sxs-lookup"><span data-stu-id="e4e58-141">Update your Ubuntu packages: `sudo apt update`</span></span>
3. <span data-ttu-id="e4e58-142">Una vez actualizados los paquetes, instale MySQL con: `sudo apt install mysql-server`</span><span class="sxs-lookup"><span data-stu-id="e4e58-142">Once the packages have updated, install MySQL with: `sudo apt install mysql-server`</span></span>
4. <span data-ttu-id="e4e58-143">Confirma la instalación y obtén el número de versión `mysql --version`.</span><span class="sxs-lookup"><span data-stu-id="e4e58-143">Confirm installation and get the version number: `mysql --version`</span></span>

<span data-ttu-id="e4e58-144">También puede que desee ejecutar el script de seguridad incluido.</span><span class="sxs-lookup"><span data-stu-id="e4e58-144">You may also want to run the included security script.</span></span> <span data-ttu-id="e4e58-145">Esto cambia algunas de las opciones predeterminadas menos seguras para elementos como inicios de sesión de raíz remota y usuarios de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e4e58-145">This changes some of the less secure default options for things like remote root logins and sample users.</span></span> <span data-ttu-id="e4e58-146">Para ejecutar el script de seguridad:</span><span class="sxs-lookup"><span data-stu-id="e4e58-146">To run the security script:</span></span>

1. <span data-ttu-id="e4e58-147">Iniciar un servidor de MySQL: `sudo /etc/init.d/mysql start`</span><span class="sxs-lookup"><span data-stu-id="e4e58-147">Start a MySQL server: `sudo /etc/init.d/mysql start`</span></span>
2. <span data-ttu-id="e4e58-148">Iniciar los mensajes del script de seguridad: `sudo mysql_secure_installation`</span><span class="sxs-lookup"><span data-stu-id="e4e58-148">Start the security script prompts: `sudo mysql_secure_installation`</span></span>
3. <span data-ttu-id="e4e58-149">En el primer mensaje se le preguntará si desea configurar el complemento validar contraseña, que se puede usar para probar la seguridad de la contraseña de MySQL.</span><span class="sxs-lookup"><span data-stu-id="e4e58-149">The first prompt will ask whether you’d like to set up the Validate Password Plugin, which can be used to test the strength of your MySQL password.</span></span> <span data-ttu-id="e4e58-150">A continuación, establecerá una contraseña para el usuario raíz de MySQL, decidirá si desea quitar usuarios anónimos, decidir si desea permitir que el usuario raíz inicie sesión tanto de forma local como remota, decidir si desea quitar la base de datos de prueba y, por último, decidir si desea recargar las tablas de privilegios inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="e4e58-150">You will then set a password for the MySQL root user, decide whether or not to remove anonymous users, decide whether to allow the root user to login both locally and remotely, decide whether to remove the test database, and, lastly, decide whether to reload the privilege tables immediately.</span></span>

<span data-ttu-id="e4e58-151">Para abrir el símbolo del sistema de MySQL, escriba: `sudo mysql`</span><span class="sxs-lookup"><span data-stu-id="e4e58-151">To open the MySQL prompt, enter: `sudo mysql`</span></span>

<span data-ttu-id="e4e58-152">Para ver las bases de datos que tiene disponibles, en el símbolo del sistema de MySQL, escriba: `SHOW DATABASES;`</span><span class="sxs-lookup"><span data-stu-id="e4e58-152">To see what databases you have available, in the MySQL prompt, enter: `SHOW DATABASES;`</span></span>

<span data-ttu-id="e4e58-153">Para crear una nueva base de datos, escriba: `CREATE DATABASE database_name;`</span><span class="sxs-lookup"><span data-stu-id="e4e58-153">To create a new database, enter: `CREATE DATABASE database_name;`</span></span>

<span data-ttu-id="e4e58-154">Para eliminar una base de datos, escriba: ` DROP DATABASE database_name;`</span><span class="sxs-lookup"><span data-stu-id="e4e58-154">To delete a database, enter: ` DROP DATABASE database_name;`</span></span>

<span data-ttu-id="e4e58-155">Para más información sobre cómo trabajar con las bases de datos de MySQL, consulte los [documentos de MySQL](https://dev.mysql.com/doc/mysql-getting-started/en/).</span><span class="sxs-lookup"><span data-stu-id="e4e58-155">For more about working with MySQL databases, see the [MySQL docs](https://dev.mysql.com/doc/mysql-getting-started/en/).</span></span>

<span data-ttu-id="e4e58-156">Para trabajar con las bases de datos MySQL en VS Code, pruebe la [extensión MySQL](https://marketplace.visualstudio.com/items?itemName=cweijan.vscode-mysql-client2).</span><span class="sxs-lookup"><span data-stu-id="e4e58-156">To work with with MySQL databases in VS Code, try the [MySQL extension](https://marketplace.visualstudio.com/items?itemName=cweijan.vscode-mysql-client2).</span></span>

## <a name="install-postgresql"></a><span data-ttu-id="e4e58-157">Instalación de PostgreSQL</span><span class="sxs-lookup"><span data-stu-id="e4e58-157">Install PostgreSQL</span></span>

<span data-ttu-id="e4e58-158">Para instalar PostgreSQL en WSL (Ubuntu 18,04):</span><span class="sxs-lookup"><span data-stu-id="e4e58-158">To install PostgreSQL on WSL (Ubuntu 18.04):</span></span>

1. <span data-ttu-id="e4e58-159">Abre el terminal de WSL (es decir, Ubuntu 18.04).</span><span class="sxs-lookup"><span data-stu-id="e4e58-159">Open your WSL terminal (ie. Ubuntu 18.04).</span></span>
2. <span data-ttu-id="e4e58-160">Actualiza los paquetes de Ubuntu: `sudo apt update`.</span><span class="sxs-lookup"><span data-stu-id="e4e58-160">Update your Ubuntu packages: `sudo apt update`</span></span>
3. <span data-ttu-id="e4e58-161">Una vez que los paquetes se hayan actualizado, instala PostgreSQL (y el paquete -contrib que tenga algunas utilidades útiles) con: `sudo apt install postgresql postgresql-contrib`.</span><span class="sxs-lookup"><span data-stu-id="e4e58-161">Once the packages have updated, install PostgreSQL (and the -contrib package which has some helpful utilities) with: `sudo apt install postgresql postgresql-contrib`</span></span>
4. <span data-ttu-id="e4e58-162">Confirma la instalación y obtén el número de versión `psql --version`.</span><span class="sxs-lookup"><span data-stu-id="e4e58-162">Confirm installation and get the version number: `psql --version`</span></span>

<span data-ttu-id="e4e58-163">Hay 3 comandos que debes conocer una vez instales PostgreSQL:</span><span class="sxs-lookup"><span data-stu-id="e4e58-163">There are 3 commands you need to know once PostgreSQL is installed:</span></span>

- <span data-ttu-id="e4e58-164">`sudo service postgresql status` para comprobar el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="e4e58-164">`sudo service postgresql status` for checking the status of your database.</span></span>
- <span data-ttu-id="e4e58-165">`sudo service postgresql start` para empezar a ejecutar la base de datos.</span><span class="sxs-lookup"><span data-stu-id="e4e58-165">`sudo service postgresql start`  to start running your database.</span></span>
- <span data-ttu-id="e4e58-166">`sudo service postgresql stop` para detener la ejecución de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="e4e58-166">`sudo service postgresql stop` to stop running your database.</span></span>

<span data-ttu-id="e4e58-167">El usuario administrador predeterminado, `postgres`, necesita tener una contraseña asignada para poder conectarse a una base de datos.</span><span class="sxs-lookup"><span data-stu-id="e4e58-167">The default admin user, `postgres`, needs a password assigned in order to connect to a database.</span></span> <span data-ttu-id="e4e58-168">Para establecer una contraseña:</span><span class="sxs-lookup"><span data-stu-id="e4e58-168">To set a password:</span></span>

1. <span data-ttu-id="e4e58-169">Escribe el comando: `sudo passwd postgres`.</span><span class="sxs-lookup"><span data-stu-id="e4e58-169">Enter the command: `sudo passwd postgres`</span></span>
2. <span data-ttu-id="e4e58-170">Recibirás un aviso para escribir la nueva contraseña.</span><span class="sxs-lookup"><span data-stu-id="e4e58-170">You will get a prompt to enter your new password.</span></span>
3. <span data-ttu-id="e4e58-171">Cierra y vuelve a abrir el terminal.</span><span class="sxs-lookup"><span data-stu-id="e4e58-171">Close and reopen your terminal.</span></span>

<span data-ttu-id="e4e58-172">Para ejecutar PostgreSQL con el shell de [psql](https://www.postgresql.org/docs/10/app-psql.html) :</span><span class="sxs-lookup"><span data-stu-id="e4e58-172">To run PostgreSQL with [psql](https://www.postgresql.org/docs/10/app-psql.html) shell:</span></span>

1. <span data-ttu-id="e4e58-173">Inicia el servicio Postgres: `sudo service postgresql start`.</span><span class="sxs-lookup"><span data-stu-id="e4e58-173">Start your postgres service: `sudo service postgresql start`</span></span>
2. <span data-ttu-id="e4e58-174">Conéctate al servicio Postgres y abre el shell de psql: `sudo -u postgres psql`.</span><span class="sxs-lookup"><span data-stu-id="e4e58-174">Connect to the postgres service and open the psql shell: `sudo -u postgres psql`</span></span>

<span data-ttu-id="e4e58-175">Una vez que hayas escrito correctamente el shell de psql, verás que el cambio de la línea de comandos tiene el siguiente aspecto: `postgres=#`.</span><span class="sxs-lookup"><span data-stu-id="e4e58-175">Once you have successfully entered the psql shell, you will see your command line change to look like this: `postgres=#`</span></span>

> [!NOTE]
> <span data-ttu-id="e4e58-176">Como alternativa, puedes abrir el shell de psql si cambias al usuario Postgres por `su - postgres` y, a continuación, escribes el comando `psql`.</span><span class="sxs-lookup"><span data-stu-id="e4e58-176">Alternatively, you can open the psql shell by switching to the postgres user with: `su - postgres` and then entering the command: `psql`.</span></span>

<span data-ttu-id="e4e58-177">Para salir de Postgres = # Enter: `\q` o use la tecla de método abreviado: Ctrl + D</span><span class="sxs-lookup"><span data-stu-id="e4e58-177">To exit postgres=# enter: `\q` or use the shortcut key: Ctrl+D</span></span>

<span data-ttu-id="e4e58-178">Para ver qué cuentas de usuario se han creado en la instalación de PostgreSQL, usa `psql -c "\du"`desde el terminal WSL o simplemente `\du`, si tienes abierto el shell de psql.</span><span class="sxs-lookup"><span data-stu-id="e4e58-178">To see what user accounts have been created on your PostgreSQL installation, use from your WSL terminal: `psql -c "\du"` ...or just `\du` if you have the psql shell open.</span></span> <span data-ttu-id="e4e58-179">Este comando mostrará las columnas: nombre de usuario de la cuenta, lista de atributos de roles y miembro de los grupos de roles.</span><span class="sxs-lookup"><span data-stu-id="e4e58-179">This command will display columns: Account User Name, List of Roles Attributes, and Member of role group(s).</span></span> <span data-ttu-id="e4e58-180">Para salir y volver a la línea de comandos, escribe `q`.</span><span class="sxs-lookup"><span data-stu-id="e4e58-180">To exit back to the command line, enter: `q`.</span></span>

<span data-ttu-id="e4e58-181">Para obtener más información sobre cómo trabajar con las bases de datos de PostgreSQL, consulte los [documentos de PostgreSQL](https://www.postgresql.org/docs/13/tutorial-createdb.html).</span><span class="sxs-lookup"><span data-stu-id="e4e58-181">For more about working with PostgreSQL databases, see the [PostgreSQL docs](https://www.postgresql.org/docs/13/tutorial-createdb.html).</span></span>

<span data-ttu-id="e4e58-182">Para trabajar con las bases de datos de PostgreSQL en VS Code, pruebe la [extensión PostgreSQL](https://marketplace.visualstudio.com/items?itemName=ms-ossdata.vscode-postgresql).</span><span class="sxs-lookup"><span data-stu-id="e4e58-182">To work with with PostgreSQL databases in VS Code, try the [PostgreSQL extension](https://marketplace.visualstudio.com/items?itemName=ms-ossdata.vscode-postgresql).</span></span>

## <a name="install-mongodb"></a><span data-ttu-id="e4e58-183">Instalación de MongoDB</span><span class="sxs-lookup"><span data-stu-id="e4e58-183">Install MongoDB</span></span>

<span data-ttu-id="e4e58-184">Para instalar MongoDB en WSL (Ubuntu 18,04):</span><span class="sxs-lookup"><span data-stu-id="e4e58-184">To install MongoDB on WSL (Ubuntu 18.04):</span></span>

1. <span data-ttu-id="e4e58-185">Abre el terminal de WSL (es decir, Ubuntu 18.04).</span><span class="sxs-lookup"><span data-stu-id="e4e58-185">Open your WSL terminal (ie. Ubuntu 18.04).</span></span>
2. <span data-ttu-id="e4e58-186">Actualiza los paquetes de Ubuntu: `sudo apt update`.</span><span class="sxs-lookup"><span data-stu-id="e4e58-186">Update your Ubuntu packages: `sudo apt update`</span></span>
3. <span data-ttu-id="e4e58-187">Una vez actualizados los paquetes, instala MongoDB con `sudo apt-get install mongodb`.</span><span class="sxs-lookup"><span data-stu-id="e4e58-187">Once the packages have updated, install MongoDB with: `sudo apt-get install mongodb`</span></span>
4. <span data-ttu-id="e4e58-188">Confirma la instalación y obtén el número de versión `mongod --version`.</span><span class="sxs-lookup"><span data-stu-id="e4e58-188">Confirm installation and get the version number: `mongod --version`</span></span>

<span data-ttu-id="e4e58-189">Hay 3 comandos que debes conocer una vez instales MongoDB:</span><span class="sxs-lookup"><span data-stu-id="e4e58-189">There are 3 commands you need to know once MongoDB is installed:</span></span>

- <span data-ttu-id="e4e58-190">`sudo service mongodb status` para comprobar el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="e4e58-190">`sudo service mongodb status` for checking the status of your database.</span></span>
- <span data-ttu-id="e4e58-191">`sudo service mongodb start` para empezar a ejecutar la base de datos.</span><span class="sxs-lookup"><span data-stu-id="e4e58-191">`sudo service mongodb start`  to start running your database.</span></span>
- <span data-ttu-id="e4e58-192">`sudo service mongodb stop` para detener la ejecución de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="e4e58-192">`sudo service mongodb stop` to stop running your database.</span></span>

> [!NOTE]
> <span data-ttu-id="e4e58-193">Es posible que veas que el comando `sudo systemctl status mongodb` se utiliza en tutoriales o artículos.</span><span class="sxs-lookup"><span data-stu-id="e4e58-193">You might see the command `sudo systemctl status mongodb` used in tutorials or articles.</span></span> <span data-ttu-id="e4e58-194">Para mantenerse ligero, WSL no incluye `systemd` (un sistema de administración de servicios de Linux).</span><span class="sxs-lookup"><span data-stu-id="e4e58-194">In order to remain lightweight, WSL does not include `systemd` (a service management system in Linux).</span></span> <span data-ttu-id="e4e58-195">En su lugar, usa SysVinit para iniciar los servicios en la máquina.</span><span class="sxs-lookup"><span data-stu-id="e4e58-195">Instead, it uses SysVinit to start services on your machine.</span></span> <span data-ttu-id="e4e58-196">No debías notar ninguna diferencia, pero si un tutorial recomienda usar `sudo systemctl`, usa `sudo /etc/init.d/` en su lugar.</span><span class="sxs-lookup"><span data-stu-id="e4e58-196">You shouldn't notice a difference, but if a tutorial recommends using `sudo systemctl`, instead use: `sudo /etc/init.d/`.</span></span> <span data-ttu-id="e4e58-197">Por ejemplo, para WSL, `sudo systemctl status mongodb` sería `sudo /etc/inid.d/mongodb status`, pero también puedes usar `sudo service mongodb status`.</span><span class="sxs-lookup"><span data-stu-id="e4e58-197">For example, `sudo systemctl status mongodb`, for WSL would be `sudo /etc/inid.d/mongodb status` ...or you can also use `sudo service mongodb status`.</span></span>

<span data-ttu-id="e4e58-198">Para ejecutar la base de datos Mongo en un servidor local:</span><span class="sxs-lookup"><span data-stu-id="e4e58-198">To run your Mongo database in a local server:</span></span>

1. <span data-ttu-id="e4e58-199">Comprobar el estado de la base de datos: `sudo service mongodb status` debería ver una respuesta [error], a menos que ya haya iniciado la base de datos.</span><span class="sxs-lookup"><span data-stu-id="e4e58-199">Check the status of your database: `sudo service mongodb status` You should see a [Fail] response, unless you've already started your database.</span></span>

2. <span data-ttu-id="e4e58-200">Inicie la base de datos: `sudo service mongodb start` ahora debería ver una respuesta [OK].</span><span class="sxs-lookup"><span data-stu-id="e4e58-200">Start your database: `sudo service mongodb start` You should now see an [OK] response.</span></span>

3. <span data-ttu-id="e4e58-201">Para comprobarlo, conéctese al servidor de base de datos y ejecute un comando de diagnóstico: `mongo --eval 'db.runCommand({ connectionStatus: 1 })'` esto generará la versión actual de la base de datos, la dirección del servidor y el puerto, y la salida del comando status.</span><span class="sxs-lookup"><span data-stu-id="e4e58-201">Verify by connecting to the database server and running a diagnostic command: `mongo --eval 'db.runCommand({ connectionStatus: 1 })'` This will output the current database version, the server address and port, and the output of the status command.</span></span> <span data-ttu-id="e4e58-202">El valor `1` para el campo "Aceptar" en la respuesta indica que el servidor funciona.</span><span class="sxs-lookup"><span data-stu-id="e4e58-202">A value of `1` for the "ok" field in the response indicates that the server is working.</span></span>

4. <span data-ttu-id="e4e58-203">Para detener la ejecución del servicio MongoDB, escribe `sudo service mongodb stop`.</span><span class="sxs-lookup"><span data-stu-id="e4e58-203">To stop your MongoDB service from running, enter: `sudo service mongodb stop`</span></span>

> [!NOTE]
> <span data-ttu-id="e4e58-204">MongoDB tiene varios parámetros predeterminados, incluido el almacenamiento de datos en /data/db y la ejecución en el puerto 27017.</span><span class="sxs-lookup"><span data-stu-id="e4e58-204">MongoDB has several default parameters, including storing data in /data/db and running on port 27017.</span></span> <span data-ttu-id="e4e58-205">Así mismo, `mongod` es el demonio (proceso de host para la base de datos) y `mongo` es el shell de la línea de comandos que se conecta a una instancia específica de `mongod`.</span><span class="sxs-lookup"><span data-stu-id="e4e58-205">Also, `mongod` is the daemon (host process for the database) and `mongo` is the command-line shell that connects to a specific instance of `mongod`.</span></span>

<span data-ttu-id="e4e58-206">VS Code admite el trabajo con bases de datos de MongoDB a través de la [extensión CosmosDB de Azure](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-cosmosdb), puede crear, administrar y consultar bases de datos de mongodb desde vs Code.</span><span class="sxs-lookup"><span data-stu-id="e4e58-206">VS Code supports working with MongoDB databases via the [Azure CosmosDB extension](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-cosmosdb), you can create, manage and query MongoDB databases from within VS Code.</span></span> <span data-ttu-id="e4e58-207">Para obtener más información, visite el VS Code docs: [trabajar con MongoDB](https://code.visualstudio.com/docs/azure/mongodb).</span><span class="sxs-lookup"><span data-stu-id="e4e58-207">To learn more, visit the VS Code docs: [Working with MongoDB](https://code.visualstudio.com/docs/azure/mongodb).</span></span>

<span data-ttu-id="e4e58-208">Obtenga más información en los documentos de MongoDB:</span><span class="sxs-lookup"><span data-stu-id="e4e58-208">Learn more in the MongoDB docs:</span></span>

- [<span data-ttu-id="e4e58-209">Introducción al uso de MongoDB</span><span class="sxs-lookup"><span data-stu-id="e4e58-209">Introduction to using MongoDB</span></span>](https://docs.mongodb.com/manual/introduction/)
- [<span data-ttu-id="e4e58-210">Creación de usuarios</span><span class="sxs-lookup"><span data-stu-id="e4e58-210">Create users</span></span>](https://docs.mongodb.com/manual/tutorial/create-users/)
- [<span data-ttu-id="e4e58-211">Conexión a una instancia de MongoDB en un host remoto</span><span class="sxs-lookup"><span data-stu-id="e4e58-211">Connect to a MongoDB instance on a remote host</span></span>](https://docs.mongodb.com/manual/mongo/#mongodb-instance-on-a-remote-host)
- [<span data-ttu-id="e4e58-212">CRUD: crear, leer, actualizar, eliminar</span><span class="sxs-lookup"><span data-stu-id="e4e58-212">CRUD: Create, Read, Update, Delete</span></span>](https://docs.mongodb.com/manual/crud/)
- [<span data-ttu-id="e4e58-213">Documentos de referencia</span><span class="sxs-lookup"><span data-stu-id="e4e58-213">Reference Docs</span></span>](https://docs.mongodb.com/manual/reference/)

## <a name="install-microsoft-sql-server"></a><span data-ttu-id="e4e58-214">Instalar Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="e4e58-214">Install Microsoft SQL Server</span></span>

<span data-ttu-id="e4e58-215">Para instalar SQL Server en WSL (Ubuntu 18,04), siga esta guía de inicio rápido: [instalación de SQL Server y creación de una base de datos en Ubuntu](https://docs.microsoft.com/sql/linux/quickstart-install-connect-ubuntu).</span><span class="sxs-lookup"><span data-stu-id="e4e58-215">To install SQL Server on WSL (Ubuntu 18.04), follow this quickstart: [Install SQL Server and create a database on Ubuntu](https://docs.microsoft.com/sql/linux/quickstart-install-connect-ubuntu).</span></span>

<span data-ttu-id="e4e58-216">Para trabajar con bases de datos de Microsoft SQL Server en VS Code, pruebe la [extensión MSSQL](https://marketplace.visualstudio.com/items?itemName=ms-mssql.mssql).</span><span class="sxs-lookup"><span data-stu-id="e4e58-216">To work with Microsoft SQL Server databases in VS Code, try the [MSSQL extension](https://marketplace.visualstudio.com/items?itemName=ms-mssql.mssql).</span></span>

## <a name="install-sqlite"></a><span data-ttu-id="e4e58-217">Instalación de SQLite</span><span class="sxs-lookup"><span data-stu-id="e4e58-217">Install SQLite</span></span>

<span data-ttu-id="e4e58-218">Para instalar SQLite en WSL (Ubuntu 18,04):</span><span class="sxs-lookup"><span data-stu-id="e4e58-218">To install SQLite on WSL (Ubuntu 18.04):</span></span>

1. <span data-ttu-id="e4e58-219">Abre el terminal de WSL (es decir, Ubuntu 18.04).</span><span class="sxs-lookup"><span data-stu-id="e4e58-219">Open your WSL terminal (ie. Ubuntu 18.04).</span></span>
2. <span data-ttu-id="e4e58-220">Actualiza los paquetes de Ubuntu: `sudo apt update`.</span><span class="sxs-lookup"><span data-stu-id="e4e58-220">Update your Ubuntu packages: `sudo apt update`</span></span>
3. <span data-ttu-id="e4e58-221">Una vez actualizados los paquetes, instale SQLite3 con: `sudo apt install sqlite3`</span><span class="sxs-lookup"><span data-stu-id="e4e58-221">Once the packages have updated, install SQLite3 with: `sudo apt install sqlite3`</span></span>
4. <span data-ttu-id="e4e58-222">Confirma la instalación y obtén el número de versión `sqlite3 --version`.</span><span class="sxs-lookup"><span data-stu-id="e4e58-222">Confirm installation and get the version number: `sqlite3 --version`</span></span>

<span data-ttu-id="e4e58-223">Para crear una base de datos de prueba, denominada "example. dB", escriba: `sqlite3 example.db`</span><span class="sxs-lookup"><span data-stu-id="e4e58-223">To create a test database, called "example.db", enter: `sqlite3 example.db`</span></span>

<span data-ttu-id="e4e58-224">Para ver una lista de las bases de datos de SQLite, escriba: `.databases`</span><span class="sxs-lookup"><span data-stu-id="e4e58-224">To see a list of your SQLite databases, enter: `.databases`</span></span>

<span data-ttu-id="e4e58-225">Para ver el estado de la base de datos, escriba: `.dbinfo ?DB?`</span><span class="sxs-lookup"><span data-stu-id="e4e58-225">To see the status of your database, enter: `.dbinfo ?DB?`</span></span>

<span data-ttu-id="e4e58-226">Para salir del aviso de SQLite, escriba: `.exit`</span><span class="sxs-lookup"><span data-stu-id="e4e58-226">To exit the SQLite prompt, enter: `.exit`</span></span>

<span data-ttu-id="e4e58-227">Para obtener más información sobre cómo trabajar con una base de datos de SQLite, consulte los [documentos de SQLite](https://www.sqlite.org/quickstart.html).</span><span class="sxs-lookup"><span data-stu-id="e4e58-227">For more information about working with a SQLite database, see the [SQLite docs](https://www.sqlite.org/quickstart.html).</span></span>

<span data-ttu-id="e4e58-228">Para trabajar con las bases de datos de SQLite en VS Code, pruebe la [extensión de SQLite](https://marketplace.visualstudio.com/items?itemName=mtxr.sqltools).</span><span class="sxs-lookup"><span data-stu-id="e4e58-228">To work with SQLite databases in VS Code, try the [SQLite extension](https://marketplace.visualstudio.com/items?itemName=mtxr.sqltools).</span></span>

## <a name="install-redis"></a><span data-ttu-id="e4e58-229">Instalación de Redis</span><span class="sxs-lookup"><span data-stu-id="e4e58-229">Install Redis</span></span>

<span data-ttu-id="e4e58-230">Para instalar Redis en WSL (Ubuntu 18,04):</span><span class="sxs-lookup"><span data-stu-id="e4e58-230">To install Redis on WSL (Ubuntu 18.04):</span></span>

1. <span data-ttu-id="e4e58-231">Abre el terminal de WSL (es decir, Ubuntu 18.04).</span><span class="sxs-lookup"><span data-stu-id="e4e58-231">Open your WSL terminal (ie. Ubuntu 18.04).</span></span>
2. <span data-ttu-id="e4e58-232">Actualiza los paquetes de Ubuntu: `sudo apt update`.</span><span class="sxs-lookup"><span data-stu-id="e4e58-232">Update your Ubuntu packages: `sudo apt update`</span></span>
3. <span data-ttu-id="e4e58-233">Una vez actualizados los paquetes, instale Redis con: `sudo apt install redis-server`</span><span class="sxs-lookup"><span data-stu-id="e4e58-233">Once the packages have updated, install Redis with: `sudo apt install redis-server`</span></span>
4. <span data-ttu-id="e4e58-234">Confirma la instalación y obtén el número de versión `redis-server --version`.</span><span class="sxs-lookup"><span data-stu-id="e4e58-234">Confirm installation and get the version number: `redis-server --version`</span></span>

<span data-ttu-id="e4e58-235">Para empezar a ejecutar el servidor de Redis: `sudo service redis-server start`</span><span class="sxs-lookup"><span data-stu-id="e4e58-235">To start running your Redis server: `sudo service redis-server start`</span></span>

<span data-ttu-id="e4e58-236">Compruebe si Redis funciona (Redis-CLI es la utilidad de la interfaz de la línea de comandos para comunicarse con Redis): `redis-cli ping` debe devolver una respuesta de "pong".</span><span class="sxs-lookup"><span data-stu-id="e4e58-236">Check to see if redis is working (redis-cli is the command line interface utility to talk with Redis): `redis-cli ping` this should return a reply of "PONG".</span></span>

<span data-ttu-id="e4e58-237">Para detener la ejecución del servidor de Redis: `sudo service redis-server stop`</span><span class="sxs-lookup"><span data-stu-id="e4e58-237">To stop running your Redis server: `sudo service redis-server stop`</span></span>

<span data-ttu-id="e4e58-238">Para obtener más información sobre cómo trabajar con una base de datos de Redis, consulte los [documentos de Redis](https://redis.io/topics/quickstart).</span><span class="sxs-lookup"><span data-stu-id="e4e58-238">For more information about working with a Redis database, see the [Redis docs](https://redis.io/topics/quickstart).</span></span>

<span data-ttu-id="e4e58-239">Para trabajar con las bases de datos de Redis en VS Code, pruebe la [extensión Redis](https://marketplace.visualstudio.com/items?itemName=cweijan.vscode-redis-client).</span><span class="sxs-lookup"><span data-stu-id="e4e58-239">To work with Redis databases in VS Code, try the [Redis extension](https://marketplace.visualstudio.com/items?itemName=cweijan.vscode-redis-client).</span></span>

## <a name="see-services-running-and-set-up-profile-aliases"></a><span data-ttu-id="e4e58-240">Ver los servicios en ejecución y configurar alias de perfil</span><span class="sxs-lookup"><span data-stu-id="e4e58-240">See services running and set up profile aliases</span></span>

<span data-ttu-id="e4e58-241">Para ver los servicios que se están ejecutando actualmente en la distribución de WSL, escriba: `service --status-all`</span><span class="sxs-lookup"><span data-stu-id="e4e58-241">To see the services that you currently have running on your WSL distribution, enter: `service --status-all`</span></span>

<span data-ttu-id="e4e58-242">Escribir `sudo service mongodb start` o `sudo service postgres start` y `sudo -u postgrest psql` puede resultar tedioso.</span><span class="sxs-lookup"><span data-stu-id="e4e58-242">Typing out `sudo service mongodb start` or `sudo service postgres start` and `sudo -u postgrest psql` can get tedious.</span></span>  <span data-ttu-id="e4e58-243">Sin embargo, puedes considerar la posibilidad de configurar los alias en el archivo `.profile` de WSL para que estos comandos sean más rápidos de usar y más fáciles de recordar.</span><span class="sxs-lookup"><span data-stu-id="e4e58-243">However, you could consider setting up aliases in your `.profile` file on WSL to make these commands quicker to use and easier to remember.</span></span>

<span data-ttu-id="e4e58-244">Para configurar tu propio alias personalizado, o acceso directo, a fin de ejecutar estos comandos:</span><span class="sxs-lookup"><span data-stu-id="e4e58-244">To set up your own custom alias, or shortcut, for executing these commands:</span></span>

1. <span data-ttu-id="e4e58-245">Abre el terminal de WSL y escribe `cd ~` para asegurarte de que te encuentras en el directorio raíz.</span><span class="sxs-lookup"><span data-stu-id="e4e58-245">Open your WSL terminal and enter `cd ~` to be sure you're in the root directory.</span></span>
2. <span data-ttu-id="e4e58-246">Abre el archivo `.profile`, que controla la configuración del terminal, con el editor de texto de terminal Nano: `sudo nano .profile`.</span><span class="sxs-lookup"><span data-stu-id="e4e58-246">Open the `.profile` file, which controls the settings for your terminal, with the terminal text editor, Nano: `sudo nano .profile`</span></span>
3. <span data-ttu-id="e4e58-247">En la parte inferior del archivo (no cambies la configuración `# set PATH`), agrega lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e4e58-247">At the bottom of the file (don't change the `# set PATH` settings), add the following:</span></span>

    ```bash
    # My Aliases
    alias start-pg='sudo service postgresql start'
    alias run-pg='sudo -u postgres psql'
    ```

    <span data-ttu-id="e4e58-248">Esto te permitirá escribir `start-pg` para empezar a ejecutar el servicio PostgreSQL y `run-pg` para abrir el shell psql.</span><span class="sxs-lookup"><span data-stu-id="e4e58-248">This will allow you to enter `start-pg` to start running the postgresql service and `run-pg` to open the psql shell.</span></span> <span data-ttu-id="e4e58-249">Puedes cambiar `start-pg` y `run-pg` a cualquier nombre que quieras, pero ten cuidado de no sobrescribir un comando que Postgres ya uses.</span><span class="sxs-lookup"><span data-stu-id="e4e58-249">You can change `start-pg` and `run-pg` to whatever names you want, just be careful not to overwrite a command that postgres already uses!</span></span>

4. <span data-ttu-id="e4e58-250">Una vez que hayas agregado los nuevos alias, sal del editor de texto de Nano con **Control + X**, selecciona `Y` (Sí) cuando se te pida que guardes y presiona Entrar (el nombre de archivo debe ser `.profile`).</span><span class="sxs-lookup"><span data-stu-id="e4e58-250">Once you've added your new aliases, exit the Nano text editor using **Ctrl+X** -- select `Y` (Yes) when prompted to save and Enter (leaving the file name as `.profile`).</span></span>
5. <span data-ttu-id="e4e58-251">Cierra y vuelve a abrir el terminal de WSL y, a continuación, prueba los nuevos comandos de alias.</span><span class="sxs-lookup"><span data-stu-id="e4e58-251">Close and re-open your WSL terminal, then try your new alias commands.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e4e58-252">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="e4e58-252">Additional resources</span></span>

- [<span data-ttu-id="e4e58-253">Configurar el entorno de desarrollo en Windows 10</span><span class="sxs-lookup"><span data-stu-id="e4e58-253">Setting up your development environment on Windows 10</span></span>](https://docs.microsoft.com/windows/dev-environment/)
