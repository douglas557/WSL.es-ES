---
title: Subsistema de Windows para Linux para Enterprise
description: Recursos e instrucciones sobre el mejor utilizan el subsistema de Windows para Linux en un entorno empresarial.
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, windowssubsystem, ubuntu, debian, suse, windows 10, enterprise, implementación, sin conexión, empaquetado, almacén, distribución, instalación, instalar
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 09/04/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 9d867654d1b66fc14b58bc5e111986a7d38ef79c
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063283"
---
# <a name="windows-subsystem-for-linux-for-enterprise"></a>Subsistema de Windows para Linux para Enterprise

La Microsoft Store para empresas ofrece una variedad de soluciones para empresas que desean implementar WSL en su empresa. El [documentación en línea](https://docs.microsoft.com/en-us/microsoft-store/) para la Microsoft Store para empresas son un excelente recurso para obtener información general sobre la experiencia de Store.

Si es una empresa que simplemente se desea para obtener o establecer seguridad para iniciar la implementación de WSL puede seguir estos pasos, que se explican dentro de los documentos de Microsoft Store:

* [Suscríbase a la Microsoft Store para empresas y empezar a trabajar](https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business-overview)
* [Administrar sus productos y servicios (incluido quién tiene acceso a qué aplicaciones en su almacén privado)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview). Aquí puede agregar distribuciones WSL a la tienda y controlar quién puede instalarlas
* [Usar un método de distribución que prefiera para implementar el software en su empresa](https://docs.microsoft.com/en-us/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* Comunique a los usuarios que tienen acceso a las distribuciones WSL pueden [siga estos pasos](https://docs.microsoft.com/en-us/windows/wsl/install-win10) para instalar la distribución o las distribuciones de su elección 

## <a name="how-to-distribute-a-distro-offline"></a>Cómo distribuir una distribución de sin conexión

Si los equipos de su empresa no tienen acceso a la Microsoft Store o la Microsoft Store para empresas, a continuación, puede descargar al instalador de una distribución de Linux que tiene una licencia sin conexión siguiendo estos pasos. 

### <a name="set-up-an-azure-active-directory-ad-account"></a>Configurar una cuenta de Azure Active Directory (AD) 

Debe tener una cuenta de Azure AD y ser el administrador global para su organización para obtener al instalador de aplicaciones de Microsoft Store. Si ya tiene una cuenta, puede omitir este paso.

Aquí encontrará las instrucciones para registrar una cuenta: https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business

### <a name="sign-into-the-store-for-business-and-go-to-the-homepage"></a>Inicie sesión en el Store para empresas y vaya a la página principal
Iniciar sesión aquí: www.microsoft.com/business-store

![MS Store para la página principal de negocio](media/offlineinstallscreens/1-screen.png)

### <a name="go-to-manage-settings-and-enable-show-offline-apps"></a>Vaya a administrar -> configuración y habilitar "Mostrar aplicaciones sin conexión"

![MS Store para la página de configuración de la empresa](media/offlineinstallscreens/2-screen.png)

### <a name="go-back-to-the-main-page-by-clicking-shop-for-my-group"></a>Vuelva a la página principal, haga clic en "Comprar para mi grupo"

![MS Store para la página principal de negocio](media/offlineinstallscreens/1-screen.png)

### <a name="search-for-your-desired-distro-and-select-it"></a>Busque la distribución deseada y selecciónelo

![MS Store para la página principal de negocio con búsqueda activa](media/offlineinstallscreens/3-screen.png)

### <a name="select-an-offline-license-in-the-license-type-dropdown-menu-and-click-get-the-app"></a>Seleccione una licencia de 'Offline' en el menú desplegable de tipo de licencia y haga clic en 'Obtener la aplicación'

![MS Store para la página de producto de negocio Ubuntu](media/offlineinstallscreens/4-screen.png)

Nota: algunas distribuciones pueden optar por no tener una licencia sin conexión

### <a name="click-the-manage-button-to-get-to-the-apps-product-page"></a>Haga clic en el botón "Administrar" para ir a página de producto de la aplicación

![MS Store para la página de producto de negocio Ubuntu](media/offlineinstallscreens/5-screen.png)

### <a name="select-your-architecture-and-download-the-package-for-offline-use"></a>Seleccione la arquitectura y descargue el paquete para su uso sin conexión

![MS Store para la página de detalles del producto de negocio Ubuntu](media/offlineinstallscreens/6-screen.png)

Este instalador, a continuación, se puede distribuir en cualquier equipo donde desea instalar WSL.