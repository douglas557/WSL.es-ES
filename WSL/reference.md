---
title: Subsistema de Windows para la referencia de comandos de Linux
description: Lista de comandos que administran el subsistema Windows para Linux
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, windowssubsystem, ubuntu
author: scooley
ms.author: scooley
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.openlocfilehash: 978a35d593e37877949c24cbd833a519888d54bf
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063583"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a>Referencia de comandos para el subsistema de Windows para Linux

> `lxrun.exe` está en desuso a partir de Windows 10 1803 y versiones posteriores.

El comando `lxrun.exe` se puede usar para interactuar con el [subsistema Windows para Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directamente.  Estos comandos se instalan en el `\Windows\System32` directorio y se pueden ejecutar en un símbolo del sistema de Windows o en PowerShell.

* `lxrun.exe` se usa para administrar WSL.  Este comando se puede usar para instalar o desinstalar la imagen de Ubuntu.


| Comando                     | Descripción                     |
|:----------------------------|:---------------------------|
| `bash`                      | Inicia el shell de Bash en el directorio actual.  Si no se instala automáticamente el shell de Bash se ejecuta `lxrun /install` |
| `bash ~`                    | Inicia el shell de bash al directorio particular de Ubuntu del usuario.  Similar a la ejecución de cd ~            |
| `bash -c "<command>"`       | Ejecuta el comando, imprime la salida y se cierra la vuelta a la línea de comandos de Windows. <br/> <br/> Ejemplo: **bash -c "ls"** |

<p>

| Comando                     | Descripción                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | El comando lxrun se usa para administrar la instancia WSL. |
| `lxrun /install`            | Inicia la descarga y el proceso de instalación. <br/> **/y** pueden agregarse a omitir todas las solicitudes.  El mensaje de confirmación se acepta automáticamente y el usuario predeterminado se establece en la raíz.          |
| `lxrun /uninstall`          | Desinstala y elimina la imagen de Ubuntu.  De forma predeterminada no elimina el directorio del usuario Ubuntu principal. <br/> **/y** pueden agregarse a Aceptar automáticamente el mensaje de confirmación <br/>**completo** desinstala y elimina el directorio particular de Ubuntu del usuario         |
| `lxrun /setdefaultuser <userName>`     | Establece el valor predeterminado de Bash en Ubuntu usuario. Se le pedirá una contraseña si el usuario especificado no existe.  Para obtener más información, visite: https://aka.ms/wslusers. <br/> **/y** promping omisiones para la contraseña.  El usuario se creará sin una contraseña.|
| `lxrun /update`            | Actualiza el índice de paquetes del subsistema          |
