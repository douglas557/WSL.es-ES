---
title: Windows Subsystem for Linux para empresas
description: Recursos e instrucciones sobre cómo usar mejor el Subsistema de Windows para Linux en un entorno empresarial.
keywords: BashOnWindows, bash, WSL, Windows, subsistema de windows para linux, subsistemawindows, ubuntu, debian, suse, windows 10, empresa, implementación, sin conexión, empaquetado, almacenamiento, distribución, instalación, instalar
ms.date: 05/15/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: ac0025257ae70547c5b20d89535510a8b8bb006c
ms.sourcegitcommit: b15b847b87d29a40de4a1517315949bce9c7a3d5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "91413106"
---
# <a name="set-up-windows-subsystem-for-linux-for-your-enterprise-company"></a>Configuración del Subsistema de Windows para Linux para tu empresa

Microsoft Store para Empresas ofrece una gran variedad de soluciones a las empresas que buscan implementar WSL en su empresa. Los [documentos de Microsoft Store para Empresas y Educación](/microsoft-store/) son un excelente recurso para obtener información general sobre la experiencia de Store.

Si perteneces a una empresa que solo busca prepararse para empezar a implementar WSL, sigue estos pasos:

* [Regístrate en Microsoft Store para Empresas y empieza a trabajar](/microsoft-store/sign-up-microsoft-store-for-business-overview).
* [Administra tus productos y servicios (incluido quien puede acceder a cada aplicación de tu tienda privada)](/microsoft-store/manage-apps-microsoft-store-for-business-overview). Aquí puedes agregar distribuciones de WSL a tu tienda y controlar quién puede instalarlas.
* [Usa un método de distribución de tu elección para implementar el software en tu empresa](/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business).
* Comunica a los empleados de tu empresa que pueden usar este vínculo de documentación para instalar WSL: [Instalar el Subsistema de Windows para Linux](./install-win10.md)

## <a name="how-to-distribute-a-linux-distribution-on-windows-offline"></a>Instalación de una distribución de Linux en Windows sin conexión

Si los equipos de tu empresa no tienen acceso a Microsoft Store o a Microsoft Store para Empresas, puedes seguir los pasos que hay a continuación para descargar el instalador de una distribución de Linux que tenga una licencia sin conexión.

### <a name="set-up-an-azure-active-directory-account"></a>Configuración de una cuenta de Azure Active Directory

Tienes que [suscribirte para obtener una cuenta de Azure AD](/azure/active-directory/fundamentals/sign-up-organization?WT.mc_id=windows-c9-niner) y ser el administrador global de tu organización a fin de obtener el instalador de las aplicaciones de Microsoft Store. Si ya tienes una cuenta, puedes omitir este paso.

### <a name="set-up-wsl-using-your-microsoft-store-for-business-account"></a>Configuración de WSL con una cuenta de Microsoft Store para Empresas

Las instrucciones para registrar una cuenta se encuentran en el vínculo siguiente: https://docs.microsoft.com/microsoft-store/sign-up-microsoft-store-for-business

1. Inicia sesión en Store para Empresas y ve a la página principal: https://www.microsoft.com/business-store

    ![Página principal de MS Store para Empresas](media/offlineinstallscreens/1-screen.png)

2. Ve a Administrar > Configuración y habilita "Show offline apps" (Mostrar aplicaciones sin conexión).

    ![Página Configuración de MS Store para Empresas](media/offlineinstallscreens/2-screen.png)

3. Para volver a la Página principal, selecciona "Shop for my group" (Comprar para mi grupo).

    ![Página principal de MS Store para Empresas](media/offlineinstallscreens/1-screen.png)

4. Busca la distribución que quieras y selecciónala.

    ![Página principal de MS Store para Empresas con búsqueda activa](media/offlineinstallscreens/3-screen.png)

5. Selecciona una licencia "Sin conexión" en el menú desplegable Tipo de licencia y elige "Obtén la aplicación". (Es posible que algunas distribuciones de Linux no proporcionen ninguna licencia sin conexión).

    ![Selección de la licencia sin conexión de Microsoft Store para Empresas para Ubuntu](media/offlineinstallscreens/4-screen.png)

6. Selecciona el botón "Administrar" para ir a la página del producto de la aplicación.

    ![Selección de la opción Administrar de Microsoft Store para Empresas para Ubuntu](media/offlineinstallscreens/5-screen.png)

7. Selecciona la arquitectura y descarga el paquete para su uso sin conexión.

    ![Selección de la arquitectura de Microsoft Store para Empresas para Ubuntu](media/offlineinstallscreens/6-screen.png)

A continuación, este instalador se puede distribuir a cualquier equipo en el que quieras instalar WSL.
