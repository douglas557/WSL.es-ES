---
title: Windows Subsystem for Linux para empresas
description: Recursos e instrucciones sobre cómo usar mejor el Subsistema de Windows para Linux en un entorno empresarial.
keywords: BashOnWindows, bash, WSL, Windows, subsistema de windows para linux, subsistemawindows, ubuntu, debian, suse, windows 10, empresa, implementación, sin conexión, empaquetado, almacenamiento, distribución, instalación, instalar
ms.date: 05/15/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 02f4ff41614f78c0e588f329c777a87f8b416233
ms.sourcegitcommit: 3fb40fd65b34a5eb26b213a0df6a3b2746b7a9b4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2020
ms.locfileid: "83235828"
---
# <a name="set-up-windows-subsystem-for-linux-for-your-enterprise-company"></a><span data-ttu-id="f77c2-104">Configuración del Subsistema de Windows para Linux para tu empresa</span><span class="sxs-lookup"><span data-stu-id="f77c2-104">Set up Windows Subsystem for Linux for your enterprise company</span></span>

<span data-ttu-id="f77c2-105">Microsoft Store para Empresas ofrece una gran variedad de soluciones a las empresas que buscan implementar WSL en su empresa.</span><span class="sxs-lookup"><span data-stu-id="f77c2-105">The Microsoft Store for Business offers a variety of solutions to Enterprises who want to deploy WSL to their company.</span></span> <span data-ttu-id="f77c2-106">Los [documentos de Microsoft Store para Empresas y Educación](https://docs.microsoft.com/microsoft-store/) son un excelente recurso para obtener información general sobre la experiencia de Store.</span><span class="sxs-lookup"><span data-stu-id="f77c2-106">The [Microsoft Store for Business and Education docs](https://docs.microsoft.com/microsoft-store/) are a great resource to find out general information about the Store experience.</span></span>

<span data-ttu-id="f77c2-107">Si perteneces a una empresa que solo busca prepararse para empezar a implementar WSL, sigue estos pasos:</span><span class="sxs-lookup"><span data-stu-id="f77c2-107">If you're a company that's just looking to get set up to start deploying WSL, follow these steps:</span></span>

* <span data-ttu-id="f77c2-108">[Regístrate en Microsoft Store para Empresas y empieza a trabajar](https://docs.microsoft.com/microsoft-store/sign-up-microsoft-store-for-business-overview).</span><span class="sxs-lookup"><span data-stu-id="f77c2-108">[Sign up for the Microsoft Store for Business and get started](https://docs.microsoft.com/microsoft-store/sign-up-microsoft-store-for-business-overview)</span></span>
* <span data-ttu-id="f77c2-109">[Administra tus productos y servicios (incluido quien puede acceder a cada aplicación de tu tienda privada)](https://docs.microsoft.com/microsoft-store/manage-apps-microsoft-store-for-business-overview).</span><span class="sxs-lookup"><span data-stu-id="f77c2-109">[Manage your products and services (including who can access which apps in your private store)](https://docs.microsoft.com/microsoft-store/manage-apps-microsoft-store-for-business-overview).</span></span> <span data-ttu-id="f77c2-110">Aquí puedes agregar distribuciones de WSL a tu tienda y controlar quién puede instalarlas.</span><span class="sxs-lookup"><span data-stu-id="f77c2-110">Here you can add WSL distros to your store and control who can install them</span></span>
* <span data-ttu-id="f77c2-111">[Usa un método de distribución de tu elección para implementar el software en tu empresa](https://docs.microsoft.com/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business).</span><span class="sxs-lookup"><span data-stu-id="f77c2-111">[Use a distribution method of your choice to deploy the software to your company](https://docs.microsoft.com/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)</span></span>
* <span data-ttu-id="f77c2-112">Comunica a los empleados de tu empresa que pueden usar este vínculo de documentación para instalar WSL: [Instalar el Subsistema de Windows para Linux](./install-win10.md)</span><span class="sxs-lookup"><span data-stu-id="f77c2-112">Communicate to the employees of your company that they can use this documentation link to install WSL: [Install the Windows Subsystem for Linux](./install-win10.md)</span></span>

## <a name="how-to-distribute-a-linux-distribution-on-windows-offline"></a><span data-ttu-id="f77c2-113">Instalación de una distribución de Linux en Windows sin conexión</span><span class="sxs-lookup"><span data-stu-id="f77c2-113">How to distribute a Linux distribution on Windows offline</span></span>

<span data-ttu-id="f77c2-114">Si los equipos de tu empresa no tienen acceso a Microsoft Store o a Microsoft Store para Empresas, puedes seguir los pasos que hay a continuación para descargar el instalador de una distribución de Linux que tenga una licencia sin conexión.</span><span class="sxs-lookup"><span data-stu-id="f77c2-114">If the computers in your company don't have access to the Microsoft Store or the Microsoft Store for Business, then you can download the installer of a Linux distribution that has an offline license by following these steps.</span></span>

### <a name="set-up-an-azure-active-directory-account"></a><span data-ttu-id="f77c2-115">Configuración de una cuenta de Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="f77c2-115">Set up an Azure Active Directory account</span></span>

<span data-ttu-id="f77c2-116">Tienes que [suscribirte para obtener una cuenta de Azure AD](https://docs.microsoft.com/azure/active-directory/fundamentals/sign-up-organization?WT.mc_id=windows-c9-niner) y ser el administrador global de tu organización a fin de obtener el instalador de las aplicaciones de Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="f77c2-116">You need to [sign up for an Azure AD account](https://docs.microsoft.com/azure/active-directory/fundamentals/sign-up-organization?WT.mc_id=windows-c9-niner) and be the global administrator for your organization to get the installer of Microsoft Store apps.</span></span> <span data-ttu-id="f77c2-117">Si ya tienes una cuenta, puedes omitir este paso.</span><span class="sxs-lookup"><span data-stu-id="f77c2-117">If you already have an account, you can skip this step.</span></span>

### <a name="set-up-wsl-using-your-microsoft-store-for-business-account"></a><span data-ttu-id="f77c2-118">Configuración de WSL con una cuenta de Microsoft Store para Empresas</span><span class="sxs-lookup"><span data-stu-id="f77c2-118">Set up WSL using your Microsoft Store for Business account</span></span>

<span data-ttu-id="f77c2-119">Las instrucciones para registrar una cuenta se encuentran en el vínculo siguiente: https://docs.microsoft.com/microsoft-store/sign-up-microsoft-store-for-business</span><span class="sxs-lookup"><span data-stu-id="f77c2-119">The instructions to register an account are found here: https://docs.microsoft.com/microsoft-store/sign-up-microsoft-store-for-business</span></span>

1. <span data-ttu-id="f77c2-120">Inicia sesión en Store para Empresas y ve a la página principal: https://www.microsoft.com/business-store</span><span class="sxs-lookup"><span data-stu-id="f77c2-120">Sign into the Store for Business and go to the homepage: https://www.microsoft.com/business-store</span></span>

    ![Página principal de MS Store para Empresas](media/offlineinstallscreens/1-screen.png)

2. <span data-ttu-id="f77c2-122">Ve a Administrar > Configuración y habilita "Show offline apps" (Mostrar aplicaciones sin conexión).</span><span class="sxs-lookup"><span data-stu-id="f77c2-122">Go to Manage > Settings and enable 'Show offline apps'.</span></span>

    ![Página Configuración de MS Store para Empresas](media/offlineinstallscreens/2-screen.png)

3. <span data-ttu-id="f77c2-124">Para volver a la Página principal, selecciona "Shop for my group" (Comprar para mi grupo).</span><span class="sxs-lookup"><span data-stu-id="f77c2-124">Go back to the main page by selecting 'Shop for my group'.</span></span>

    ![Página principal de MS Store para Empresas](media/offlineinstallscreens/1-screen.png)

4. <span data-ttu-id="f77c2-126">Busca la distribución que quieras y selecciónala.</span><span class="sxs-lookup"><span data-stu-id="f77c2-126">Search for your desired distribution and select it.</span></span>

    ![Página principal de MS Store para Empresas con búsqueda activa](media/offlineinstallscreens/3-screen.png)

5. <span data-ttu-id="f77c2-128">Selecciona una licencia "Sin conexión" en el menú desplegable Tipo de licencia y elige "Obtén la aplicación".</span><span class="sxs-lookup"><span data-stu-id="f77c2-128">Select an 'Offline' license in the License type dropdown menu and select 'Get the app'.</span></span> <span data-ttu-id="f77c2-129">(Es posible que algunas distribuciones de Linux no proporcionen ninguna licencia sin conexión).</span><span class="sxs-lookup"><span data-stu-id="f77c2-129">(Some Linux distributions may elect not to provide an offline license).</span></span>

    ![Página del producto de Microsoft Store para Empresas para Ubuntu](media/offlineinstallscreens/4-screen.png)

6. <span data-ttu-id="f77c2-131">Selecciona el botón "Administrar" para ir a la página del producto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f77c2-131">Select the 'Manage' button to get to the app's product page.</span></span>

    ![Página del producto de Microsoft Store para Empresas para Ubuntu](media/offlineinstallscreens/5-screen.png)

7. <span data-ttu-id="f77c2-133">Selecciona la arquitectura y descarga el paquete para su uso sin conexión.</span><span class="sxs-lookup"><span data-stu-id="f77c2-133">Select your architecture and download the package for offline use.</span></span>

    ![Página de detalles del producto de Microsoft Store para Empresas para Ubuntu](media/offlineinstallscreens/6-screen.png)

<span data-ttu-id="f77c2-135">A continuación, este instalador se puede distribuir a cualquier equipo en el que quieras instalar WSL.</span><span class="sxs-lookup"><span data-stu-id="f77c2-135">This installer can then be distributed to any computer where you would like to install WSL.</span></span>
