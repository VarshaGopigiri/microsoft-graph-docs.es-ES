---
title: Usar la API de Graph de Intune
description: " No se admiten las implementaciones híbridas de Intune. "
ms.openlocfilehash: 2502b5209e9935fc923570947c38c0467534f4ef
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087987"
---
# <a name="working-with-intune-in-microsoft-graph"></a><span data-ttu-id="6e720-103">Trabajar con Intune en Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="6e720-103">Working with Intune in Microsoft Graph</span></span>  

> <span data-ttu-id="6e720-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6e720-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6e720-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6e720-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="6e720-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune-pricing) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6e720-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune-pricing) by the customer.</span></span>

<span data-ttu-id="6e720-107">La API de Microsoft Graph para Intune permite el acceso mediante programación a la información de Intune para su espacio empresarial; la API realiza las mismas operaciones de Intune que las que están disponibles a través de **Azure Portal**.</span><span class="sxs-lookup"><span data-stu-id="6e720-107">The Microsoft Graph API for Intune enables programmatic access to Intune information for your tenant; the API performs the same Intune operations as those available through the **Azure Portal**.</span></span>  

<span data-ttu-id="6e720-108">En los escenarios de administración de dispositivos móviles (MDM), la API de Graph para Intune admite implementaciones independientes; no se admiten las [implementaciones híbridas](https://docs.microsoft.com/en-us/sccm/mdm/understand/choose-between-standalone-intune-and-hybrid-mobile-device-management) de Intune.</span><span class="sxs-lookup"><span data-stu-id="6e720-108">For mobile device management (MDM) scenarios, the Graph API for Intune supports standalone deployments; Intune [hybrid deployments](https://docs.microsoft.com/en-us/sccm/mdm/understand/choose-between-standalone-intune-and-hybrid-mobile-device-management) are not supported.</span></span> 

## <a name="using-the-intune-graph-api"></a><span data-ttu-id="6e720-109">Usar la API de Graph de Intune</span><span class="sxs-lookup"><span data-stu-id="6e720-109">Using the Intune Graph API</span></span>

<span data-ttu-id="6e720-110">En el Microsoft Graph, Intune proporciona datos de la misma manera igual que otros servicios de nube, con la navegación de información y la relación de entidad enriquecido.</span><span class="sxs-lookup"><span data-stu-id="6e720-110">Intune provides data into the Microsoft Graph in the same way as other cloud services do, with rich entity information and relationship navigation.</span></span><span data-ttu-id="6e720-111">Utilizar Microsoft Graph para combinar la información de otros servicios y Intune para crear aplicaciones de servicio de entre completas para profesionales de TI o los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="6e720-111">  Use Microsoft Graph to combine information from other services and Intune to build rich cross-service applications for IT professionals or end users.</span></span>     

<span data-ttu-id="6e720-112">Este es un ejemplo de cómo puede determinar si una aplicación está instalada en el dispositivo de un usuario:</span><span class="sxs-lookup"><span data-stu-id="6e720-112">Here is an example of how you can determine whether an application is installed on a user's device:</span></span> 

1. <span data-ttu-id="6e720-113">Obtenga de Azure Active Directory una lista de dispositivos registrados para un usuario:</span><span class="sxs-lookup"><span data-stu-id="6e720-113">Get from Azure Active Directory a list of devices registered to a user:</span></span> 

    https://graph.microsoft.com/beta/users/{user}/ownedDevices 

2. <span data-ttu-id="6e720-114">A continuación, vea la lista de aplicaciones de su espacio empresarial:</span><span class="sxs-lookup"><span data-stu-id="6e720-114">Then view the list of applications for your tenant:</span></span> 

    https://graph.microsoft.com/beta/deviceAppManagement/mobileApps  

3. <span data-ttu-id="6e720-115">Tome el identificador de la aplicación y determine el estado de instalación para la aplicación (y, por tanto, el usuario):</span><span class="sxs-lookup"><span data-stu-id="6e720-115">Take the ID from the application and determine the installation state for the application (and therefore user):</span></span>

    https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{id}/deviceStatuses/


## <a name="using-graph-permission-scopes"></a><span data-ttu-id="6e720-116">Uso de ámbitos de permiso de gráfico</span><span class="sxs-lookup"><span data-stu-id="6e720-116">Using Graph permission scopes</span></span>

<span data-ttu-id="6e720-117">Gráfico de Microsof controla el acceso a los recursos mediante ámbitos de permisos.</span><span class="sxs-lookup"><span data-stu-id="6e720-117">Microsof Graph controls access to resources using permission scopes.</span></span> <span data-ttu-id="6e720-118">Como desarrollador, debe especificar los ámbitos de permisos que necesita para tener acceso a los recursos de Intune.</span><span class="sxs-lookup"><span data-stu-id="6e720-118">As a developer, you must specify the permission scopes you need to access Intune resources.</span></span> <span data-ttu-id="6e720-119">Normalmente, los ámbitos de permisos se especifican en el portal de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6e720-119">Typically, you specify the permission scopes you need in the Azure Active Directory portal.</span></span> <span data-ttu-id="6e720-120">Para obtener más información, consulte [Ámbitos de permiso de Microsoft Graph](https://developer.microsoft.com/graph/docs/authorization/permission_scopes) y [Ámbitos de permisos de Intune](https://developer.microsoft.com/graph/docs/authorization/permission_scopes#permission-scopes-in-preview).</span><span class="sxs-lookup"><span data-stu-id="6e720-120">For more information, see [Microsoft Graph permission scopes](https://developer.microsoft.com/graph/docs/authorization/permission_scopes) and [Intune permission scopes](https://developer.microsoft.com/graph/docs/authorization/permission_scopes#permission-scopes-in-preview).</span></span>

## <a name="to-use-the-table-of-contents-on-the-microsoft-graph-site"></a><span data-ttu-id="6e720-121">Para usar la tabla de contenido en el sitio de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="6e720-121">To use the Table of Contents on the Microsoft Graph site</span></span>
  
<span data-ttu-id="6e720-122">Puede examinar la tabla de contenido (en el panel izquierdo del sitio) para buscar los elementos de la documentación de API de gráfico Intune y recursos que desea ver.</span><span class="sxs-lookup"><span data-stu-id="6e720-122">You can browse the Table of Contents (in the left pane of the site) to find the parts of the Intune Graph API and resource documentation you want to see.</span></span>

1. <span data-ttu-id="6e720-123">Haga clic en **Referencia de /Beta** para abrir a los documentos de la versión beta.</span><span class="sxs-lookup"><span data-stu-id="6e720-123">Click **/Beta Reference** to open the beta docs.</span></span>
2. <span data-ttu-id="6e720-124">Desplácese hacia abajo y haga clic en **Intune**.</span><span class="sxs-lookup"><span data-stu-id="6e720-124">Scroll down and click **Intune**.</span></span>
3. <span data-ttu-id="6e720-125">Siga haciendo clic en subsecciones debajo **Intune** para los elementos de la API</span><span class="sxs-lookup"><span data-stu-id="6e720-125">Continue to click subsections below **Intune** for the parts of the API you</span></span> 
