---
title: Windows Subsystem for Linux para empresas
description: Recursos e instrucciones sobre cómo usar mejor el subsistema de Windows para Linux en un entorno empresarial.
keywords: BashOnWindows, bash, WSL, Windows, subsistema de Windows para Linux, windowssubsystem, Ubuntu, Debian, SuSE, Windows 10, Enterprise, implementación, sin conexión, empaquetado, almacenamiento, distribución, instalación, instalación
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 09/04/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 9d867654d1b66fc14b58bc5e111986a7d38ef79c
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/14/2019
ms.locfileid: "59063283"
---
# <a name="windows-subsystem-for-linux-for-enterprise"></a>Windows Subsystem for Linux para empresas

El Microsoft Store para la empresa ofrece una gran variedad de soluciones a las empresas que desean implementar WSL en su empresa. Los [documentos en línea](https://docs.microsoft.com/en-us/microsoft-store/) de la Microsoft Store para empresas son un excelente recurso para averiguar información general sobre la experiencia de la tienda.

Si es una empresa que solo está pensando en empezar a implementar WSL, puede seguir estos pasos, que se explican en la Microsoft Store docs:

* [Regístrese en el Microsoft Store para empresas y empiece a trabajar](https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business-overview)
* [Administre sus productos y servicios (incluyendo quién puede acceder a qué aplicaciones de su tienda privada)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview). Aquí puede Agregar WSL distribuciones a su tienda y controlar quién puede instalarlos.
* [Use un método de distribución de su elección para implementar el software en su empresa.](https://docs.microsoft.com/en-us/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* Comunique a los usuarios que tienen acceso a WSL distribuciones que pueden [usar estos pasos](https://docs.microsoft.com/en-us/windows/wsl/install-win10) para instalar el distribución o distribuciones de su elección 

## <a name="how-to-distribute-a-distro-offline"></a>Cómo distribuir un distribución sin conexión

Si los equipos de su empresa no tienen acceso al Microsoft Store o al Microsoft Store para empresas, puede descargar el instalador de un distribución de Linux que tenga una licencia sin conexión siguiendo estos pasos. 

### <a name="set-up-an-azure-active-directory-ad-account"></a>Configuración de una cuenta de Azure Active Directory (AD) 

Debe tener una cuenta de Azure AD y ser el administrador global de su organización para obtener el instalador de Microsoft Store aplicaciones. Si ya tiene una cuenta, puede omitir este paso.

Las instrucciones para registrar una cuenta se pueden encontrar aquí: https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business

### <a name="sign-into-the-store-for-business-and-go-to-the-homepage"></a>Inicie sesión en la tienda para empresas y vaya a la Página principal.
Iniciar sesión aquí: www.microsoft.com/business-store

![Página principal de la tienda de Microsoft para empresas](media/offlineinstallscreens/1-screen.png)

### <a name="go-to-manage-settings-and-enable-show-offline-apps"></a>Vaya a administrar-> configuración y habilite "Mostrar aplicaciones sin conexión".

![Página de configuración de la tienda Microsoft para empresas](media/offlineinstallscreens/2-screen.png)

### <a name="go-back-to-the-main-page-by-clicking-shop-for-my-group"></a>Vuelva a la Página principal haciendo clic en "comprar para mi grupo".

![Página principal de la tienda de Microsoft para empresas](media/offlineinstallscreens/1-screen.png)

### <a name="search-for-your-desired-distro-and-select-it"></a>Busque el distribución deseado y selecciónelo.

![Página principal de la tienda de Microsoft para empresas con búsqueda activa](media/offlineinstallscreens/3-screen.png)

### <a name="select-an-offline-license-in-the-license-type-dropdown-menu-and-click-get-the-app"></a>Seleccione una licencia "sin conexión" en el menú desplegable tipo de licencia y haga clic en "obtener la aplicación".

![Página del producto de Microsoft Store for Business Ubuntu](media/offlineinstallscreens/4-screen.png)

Tenga en cuenta que algunos distribuciones pueden optar por no tener una licencia sin conexión.

### <a name="click-the-manage-button-to-get-to-the-apps-product-page"></a>Haga clic en el botón "administrar" para ir a la página del producto de la aplicación.

![Página del producto de Microsoft Store for Business Ubuntu](media/offlineinstallscreens/5-screen.png)

### <a name="select-your-architecture-and-download-the-package-for-offline-use"></a>Seleccione la arquitectura y descargue el paquete para su uso sin conexión

![Página de detalles del producto de Microsoft Store for Business Ubuntu](media/offlineinstallscreens/6-screen.png)

A continuación, este instalador se puede distribuir a cualquier equipo en el que desee instalar WSL.