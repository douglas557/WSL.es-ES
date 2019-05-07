---
title: Windows Subsystem for Linux para empresas
description: Recursos e instrucciones sobre el mejor utilizan el subsistema de Windows para Linux en un entorno empresarial.
keywords: BashOnWindows, bash, wsl, windows, subsistema de windows para linux, windowssubsystem, ubuntu, debian, suse, windows 10, enterprise, implementación, sin conexión, empaquetado, almacén, distribución, instalación, instalar
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 09/04/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 9d867654d1b66fc14b58bc5e111986a7d38ef79c
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063283"
---
# <a name="windows-subsystem-for-linux-for-enterprise"></a><span data-ttu-id="f672e-104">Windows Subsystem for Linux para empresas</span><span class="sxs-lookup"><span data-stu-id="f672e-104">Windows Subsystem for Linux for Enterprise</span></span>

<span data-ttu-id="f672e-105">La Microsoft Store para empresas ofrece una variedad de soluciones para empresas que desean implementar WSL en su empresa.</span><span class="sxs-lookup"><span data-stu-id="f672e-105">The Microsoft Store for Business offers a variety of solutions to Enterprises who want to deploy WSL to their company.</span></span> <span data-ttu-id="f672e-106">El [documentación en línea](https://docs.microsoft.com/en-us/microsoft-store/) para la Microsoft Store para empresas son un excelente recurso para obtener información general sobre la experiencia de Store.</span><span class="sxs-lookup"><span data-stu-id="f672e-106">The [online docs](https://docs.microsoft.com/en-us/microsoft-store/) for the Microsoft Store for Business are a great resource to find out general information about the Store experience.</span></span>

<span data-ttu-id="f672e-107">Si es una empresa que simplemente se desea para obtener o establecer seguridad para iniciar la implementación de WSL puede seguir estos pasos, que se explican dentro de los documentos de Microsoft Store:</span><span class="sxs-lookup"><span data-stu-id="f672e-107">If you’re a company that’s just looking to get set up to start deploying WSL you can follow these steps, which are explained inside of the Microsoft Store docs:</span></span>

* [<span data-ttu-id="f672e-108">Suscríbase a la Microsoft Store para empresas y empezar a trabajar</span><span class="sxs-lookup"><span data-stu-id="f672e-108">Sign up for the Microsoft Store for Business and get started</span></span>](https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business-overview)
* <span data-ttu-id="f672e-109">[Administrar sus productos y servicios (incluido quién tiene acceso a qué aplicaciones en su almacén privado)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview).</span><span class="sxs-lookup"><span data-stu-id="f672e-109">[Manage your products and services (including who can access which apps in your private store)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview).</span></span> <span data-ttu-id="f672e-110">Aquí puede agregar distribuciones WSL a la tienda y controlar quién puede instalarlas</span><span class="sxs-lookup"><span data-stu-id="f672e-110">Here you can add WSL distros to your store and control who can install them</span></span>
* [<span data-ttu-id="f672e-111">Usar un método de distribución que prefiera para implementar el software en su empresa</span><span class="sxs-lookup"><span data-stu-id="f672e-111">Use a distribution method of your choice to deploy the software to your company</span></span>](https://docs.microsoft.com/en-us/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* <span data-ttu-id="f672e-112">Comunique a los usuarios que tienen acceso a las distribuciones WSL pueden [siga estos pasos](https://docs.microsoft.com/en-us/windows/wsl/install-win10) para instalar la distribución o las distribuciones de su elección</span><span class="sxs-lookup"><span data-stu-id="f672e-112">Communicate to users who have access to WSL distros that they can [use these steps](https://docs.microsoft.com/en-us/windows/wsl/install-win10) to install the distro or distros of their choice</span></span> 

## <a name="how-to-distribute-a-distro-offline"></a><span data-ttu-id="f672e-113">Cómo distribuir una distribución de sin conexión</span><span class="sxs-lookup"><span data-stu-id="f672e-113">How to Distribute a Distro Offline</span></span>

<span data-ttu-id="f672e-114">Si los equipos de su empresa no tienen acceso a la Microsoft Store o la Microsoft Store para empresas, a continuación, puede descargar al instalador de una distribución de Linux que tiene una licencia sin conexión siguiendo estos pasos.</span><span class="sxs-lookup"><span data-stu-id="f672e-114">If the computers in your company don’t have access to the Microsoft Store or the Microsoft Store for Business, then you can download the installer of a Linux distro that has an offline license by following these steps.</span></span> 

### <a name="set-up-an-azure-active-directory-ad-account"></a><span data-ttu-id="f672e-115">Configurar una cuenta de Azure Active Directory (AD)</span><span class="sxs-lookup"><span data-stu-id="f672e-115">Set up an Azure Active Directory (AD) Account</span></span> 

<span data-ttu-id="f672e-116">Debe tener una cuenta de Azure AD y ser el administrador global para su organización para obtener al instalador de aplicaciones de Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="f672e-116">You need to have an Azure AD account and be the global administrator for your organization to get the installer of Microsoft Store apps.</span></span> <span data-ttu-id="f672e-117">Si ya tiene una cuenta, puede omitir este paso.</span><span class="sxs-lookup"><span data-stu-id="f672e-117">If you already have an account, you can skip this step.</span></span>

<span data-ttu-id="f672e-118">Aquí encontrará las instrucciones para registrar una cuenta: https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business</span><span class="sxs-lookup"><span data-stu-id="f672e-118">The instructions to register an account can be found here: https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business</span></span>

### <a name="sign-into-the-store-for-business-and-go-to-the-homepage"></a><span data-ttu-id="f672e-119">Inicie sesión en el Store para empresas y vaya a la página principal</span><span class="sxs-lookup"><span data-stu-id="f672e-119">Sign into the Store for Business and go to the homepage</span></span>
<span data-ttu-id="f672e-120">Iniciar sesión aquí: www.microsoft.com/business-store</span><span class="sxs-lookup"><span data-stu-id="f672e-120">Sign in here: www.microsoft.com/business-store</span></span>

![MS Store para la página principal de negocio](media/offlineinstallscreens/1-screen.png)

### <a name="go-to-manage-settings-and-enable-show-offline-apps"></a><span data-ttu-id="f672e-122">Vaya a administrar -> configuración y habilitar "Mostrar aplicaciones sin conexión"</span><span class="sxs-lookup"><span data-stu-id="f672e-122">Go to Manage->Settings and enable 'Show offline apps'</span></span>

![MS Store para la página de configuración de la empresa](media/offlineinstallscreens/2-screen.png)

### <a name="go-back-to-the-main-page-by-clicking-shop-for-my-group"></a><span data-ttu-id="f672e-124">Vuelva a la página principal, haga clic en "Comprar para mi grupo"</span><span class="sxs-lookup"><span data-stu-id="f672e-124">Go back to the main page by clicking 'Shop for my group'</span></span>

![MS Store para la página principal de negocio](media/offlineinstallscreens/1-screen.png)

### <a name="search-for-your-desired-distro-and-select-it"></a><span data-ttu-id="f672e-126">Busque la distribución deseada y selecciónelo</span><span class="sxs-lookup"><span data-stu-id="f672e-126">Search for your desired distro and select it</span></span>

![MS Store para la página principal de negocio con búsqueda activa](media/offlineinstallscreens/3-screen.png)

### <a name="select-an-offline-license-in-the-license-type-dropdown-menu-and-click-get-the-app"></a><span data-ttu-id="f672e-128">Seleccione una licencia de 'Offline' en el menú desplegable de tipo de licencia y haga clic en 'Obtener la aplicación'</span><span class="sxs-lookup"><span data-stu-id="f672e-128">Select an ‘Offline’ license in the License type dropdown menu and click ‘Get the app’</span></span>

![MS Store para la página de producto de negocio Ubuntu](media/offlineinstallscreens/4-screen.png)

<span data-ttu-id="f672e-130">Nota: algunas distribuciones pueden optar por no tener una licencia sin conexión</span><span class="sxs-lookup"><span data-stu-id="f672e-130">Please note: some distros may elect not to have an offline license</span></span>

### <a name="click-the-manage-button-to-get-to-the-apps-product-page"></a><span data-ttu-id="f672e-131">Haga clic en el botón "Administrar" para ir a página de producto de la aplicación</span><span class="sxs-lookup"><span data-stu-id="f672e-131">Click the ‘Manage’ button to get to the app’s product page</span></span>

![MS Store para la página de producto de negocio Ubuntu](media/offlineinstallscreens/5-screen.png)

### <a name="select-your-architecture-and-download-the-package-for-offline-use"></a><span data-ttu-id="f672e-133">Seleccione la arquitectura y descargue el paquete para su uso sin conexión</span><span class="sxs-lookup"><span data-stu-id="f672e-133">Select your architecture and download the package for offline use</span></span>

![MS Store para la página de detalles del producto de negocio Ubuntu](media/offlineinstallscreens/6-screen.png)

<span data-ttu-id="f672e-135">Este instalador, a continuación, se puede distribuir en cualquier equipo donde desea instalar WSL.</span><span class="sxs-lookup"><span data-stu-id="f672e-135">This installer can then be distributed to any computer where you would like to install WSL.</span></span>