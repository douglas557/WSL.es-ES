---
title: Windows Subsystem for Linux para empresas
description: Recursos e instrucciones sobre cómo usar mejor el subsistema de Windows para Linux en un entorno empresarial.
keywords: BashOnWindows, bash, WSL, Windows, subsistema de Windows para Linux, windowssubsystem, Ubuntu, Debian, SuSE, Windows 10, Enterprise, implementación, sin conexión, empaquetado, almacenamiento, distribución, instalación, instalación
ms.date: 09/04/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: c32d62267c77d87fb200cfe43b8e6f43b4e3a56d
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269861"
---
# <a name="windows-subsystem-for-linux-for-enterprise"></a><span data-ttu-id="92c8d-104">Windows Subsystem for Linux para empresas</span><span class="sxs-lookup"><span data-stu-id="92c8d-104">Windows Subsystem for Linux for Enterprise</span></span>

<span data-ttu-id="92c8d-105">El Microsoft Store para la empresa ofrece una gran variedad de soluciones a las empresas que desean implementar WSL en su empresa.</span><span class="sxs-lookup"><span data-stu-id="92c8d-105">The Microsoft Store for Business offers a variety of solutions to Enterprises who want to deploy WSL to their company.</span></span> <span data-ttu-id="92c8d-106">Los [documentos en línea](https://docs.microsoft.com/en-us/microsoft-store/) de la Microsoft Store para empresas son un excelente recurso para averiguar información general sobre la experiencia de la tienda.</span><span class="sxs-lookup"><span data-stu-id="92c8d-106">The [online docs](https://docs.microsoft.com/en-us/microsoft-store/) for the Microsoft Store for Business are a great resource to find out general information about the Store experience.</span></span>

<span data-ttu-id="92c8d-107">Si es una empresa que solo está pensando en empezar a implementar WSL, puede seguir estos pasos, que se explican en la Microsoft Store docs:</span><span class="sxs-lookup"><span data-stu-id="92c8d-107">If you’re a company that’s just looking to get set up to start deploying WSL you can follow these steps, which are explained inside of the Microsoft Store docs:</span></span>

* [<span data-ttu-id="92c8d-108">Regístrese en el Microsoft Store para empresas y empiece a trabajar</span><span class="sxs-lookup"><span data-stu-id="92c8d-108">Sign up for the Microsoft Store for Business and get started</span></span>](https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business-overview)
* <span data-ttu-id="92c8d-109">[Administre sus productos y servicios (incluyendo quién puede acceder a qué aplicaciones de su tienda privada)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview).</span><span class="sxs-lookup"><span data-stu-id="92c8d-109">[Manage your products and services (including who can access which apps in your private store)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview).</span></span> <span data-ttu-id="92c8d-110">Aquí puede Agregar WSL distribuciones a su tienda y controlar quién puede instalarlos.</span><span class="sxs-lookup"><span data-stu-id="92c8d-110">Here you can add WSL distros to your store and control who can install them</span></span>
* [<span data-ttu-id="92c8d-111">Use un método de distribución de su elección para implementar el software en su empresa.</span><span class="sxs-lookup"><span data-stu-id="92c8d-111">Use a distribution method of your choice to deploy the software to your company</span></span>](https://docs.microsoft.com/en-us/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* <span data-ttu-id="92c8d-112">Comunique a los usuarios que tienen acceso a WSL distribuciones que pueden [usar estos pasos](https://docs.microsoft.com/en-us/windows/wsl/install-win10) para instalar el distribución o distribuciones de su elección</span><span class="sxs-lookup"><span data-stu-id="92c8d-112">Communicate to users who have access to WSL distros that they can [use these steps](https://docs.microsoft.com/en-us/windows/wsl/install-win10) to install the distro or distros of their choice</span></span> 

## <a name="how-to-distribute-a-distro-offline"></a><span data-ttu-id="92c8d-113">Cómo distribuir un distribución sin conexión</span><span class="sxs-lookup"><span data-stu-id="92c8d-113">How to Distribute a Distro Offline</span></span>

<span data-ttu-id="92c8d-114">Si los equipos de su empresa no tienen acceso al Microsoft Store o al Microsoft Store para empresas, puede descargar el instalador de un distribución de Linux que tenga una licencia sin conexión siguiendo estos pasos.</span><span class="sxs-lookup"><span data-stu-id="92c8d-114">If the computers in your company don’t have access to the Microsoft Store or the Microsoft Store for Business, then you can download the installer of a Linux distro that has an offline license by following these steps.</span></span> 

### <a name="set-up-an-azure-active-directory-ad-account"></a><span data-ttu-id="92c8d-115">Configuración de una cuenta de Azure Active Directory (AD)</span><span class="sxs-lookup"><span data-stu-id="92c8d-115">Set up an Azure Active Directory (AD) Account</span></span> 

<span data-ttu-id="92c8d-116">Debe tener una cuenta de Azure AD y ser el administrador global de su organización para obtener el instalador de Microsoft Store aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="92c8d-116">You need to have an Azure AD account and be the global administrator for your organization to get the installer of Microsoft Store apps.</span></span> <span data-ttu-id="92c8d-117">Si ya tiene una cuenta, puede omitir este paso.</span><span class="sxs-lookup"><span data-stu-id="92c8d-117">If you already have an account, you can skip this step.</span></span>

<span data-ttu-id="92c8d-118">Las instrucciones para registrar una cuenta se pueden encontrar aquí: https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business</span><span class="sxs-lookup"><span data-stu-id="92c8d-118">The instructions to register an account can be found here: https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business</span></span>

### <a name="sign-into-the-store-for-business-and-go-to-the-homepage"></a><span data-ttu-id="92c8d-119">Inicie sesión en la tienda para empresas y vaya a la Página principal.</span><span class="sxs-lookup"><span data-stu-id="92c8d-119">Sign into the Store for Business and go to the homepage</span></span>
<span data-ttu-id="92c8d-120">Iniciar sesión aquí: www.microsoft.com/business-store</span><span class="sxs-lookup"><span data-stu-id="92c8d-120">Sign in here: www.microsoft.com/business-store</span></span>

![Página principal de la tienda de Microsoft para empresas](media/offlineinstallscreens/1-screen.png)

### <a name="go-to-manage-settings-and-enable-show-offline-apps"></a><span data-ttu-id="92c8d-122">Vaya a administrar-> configuración y habilite "Mostrar aplicaciones sin conexión".</span><span class="sxs-lookup"><span data-stu-id="92c8d-122">Go to Manage->Settings and enable 'Show offline apps'</span></span>

![Página de configuración de la tienda Microsoft para empresas](media/offlineinstallscreens/2-screen.png)

### <a name="go-back-to-the-main-page-by-clicking-shop-for-my-group"></a><span data-ttu-id="92c8d-124">Vuelva a la Página principal haciendo clic en "comprar para mi grupo".</span><span class="sxs-lookup"><span data-stu-id="92c8d-124">Go back to the main page by clicking 'Shop for my group'</span></span>

![Página principal de la tienda de Microsoft para empresas](media/offlineinstallscreens/1-screen.png)

### <a name="search-for-your-desired-distro-and-select-it"></a><span data-ttu-id="92c8d-126">Busque el distribución deseado y selecciónelo.</span><span class="sxs-lookup"><span data-stu-id="92c8d-126">Search for your desired distro and select it</span></span>

![Página principal de la tienda de Microsoft para empresas con búsqueda activa](media/offlineinstallscreens/3-screen.png)

### <a name="select-an-offline-license-in-the-license-type-dropdown-menu-and-click-get-the-app"></a><span data-ttu-id="92c8d-128">Seleccione una licencia "sin conexión" en el menú desplegable tipo de licencia y haga clic en "obtener la aplicación".</span><span class="sxs-lookup"><span data-stu-id="92c8d-128">Select an ‘Offline’ license in the License type dropdown menu and click ‘Get the app’</span></span>

![Página del producto de Microsoft Store for Business Ubuntu](media/offlineinstallscreens/4-screen.png)

<span data-ttu-id="92c8d-130">Tenga en cuenta que algunos distribuciones pueden optar por no tener una licencia sin conexión.</span><span class="sxs-lookup"><span data-stu-id="92c8d-130">Please note: some distros may elect not to have an offline license</span></span>

### <a name="click-the-manage-button-to-get-to-the-apps-product-page"></a><span data-ttu-id="92c8d-131">Haga clic en el botón "administrar" para ir a la página del producto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="92c8d-131">Click the ‘Manage’ button to get to the app’s product page</span></span>

![Página del producto de Microsoft Store for Business Ubuntu](media/offlineinstallscreens/5-screen.png)

### <a name="select-your-architecture-and-download-the-package-for-offline-use"></a><span data-ttu-id="92c8d-133">Seleccione la arquitectura y descargue el paquete para su uso sin conexión</span><span class="sxs-lookup"><span data-stu-id="92c8d-133">Select your architecture and download the package for offline use</span></span>

![Página de detalles del producto de Microsoft Store for Business Ubuntu](media/offlineinstallscreens/6-screen.png)

<span data-ttu-id="92c8d-135">A continuación, este instalador se puede distribuir a cualquier equipo en el que desee instalar WSL.</span><span class="sxs-lookup"><span data-stu-id="92c8d-135">This installer can then be distributed to any computer where you would like to install WSL.</span></span>