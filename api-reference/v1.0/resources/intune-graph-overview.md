---
title: Usar la API de Graph de Intune
description: " No se admiten las implementaciones híbridas de Intune. "
ms.openlocfilehash: 23f6550fca708b64357b7b5132a2a42060cfa4bd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028563"
---
# <a name="working-with-intune-in-microsoft-graph"></a><span data-ttu-id="5e881-103">Trabajar con Intune en Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="5e881-103">Working with Intune in Microsoft Graph</span></span>  

> <span data-ttu-id="5e881-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune-pricing) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5e881-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune-pricing) by the customer.</span></span>

<span data-ttu-id="5e881-105">La API de Microsoft Graph para Intune permite el acceso mediante programación a la información de Intune para su espacio empresarial; la API realiza las mismas operaciones de Intune que las que están disponibles a través de **Azure Portal**.</span><span class="sxs-lookup"><span data-stu-id="5e881-105">The Microsoft Graph API for Intune enables programmatic access to Intune information for your tenant; the API performs the same Intune operations as those available through the **Azure Portal**.</span></span>  

<span data-ttu-id="5e881-106">En los escenarios de administración de dispositivos móviles (MDM), la API de Graph para Intune admite implementaciones independientes; no se admiten las [implementaciones híbridas](https://docs.microsoft.com/en-us/sccm/mdm/understand/choose-between-standalone-intune-and-hybrid-mobile-device-management) de Intune.</span><span class="sxs-lookup"><span data-stu-id="5e881-106">For mobile device management (MDM) scenarios, the Graph API for Intune supports standalone deployments; Intune [hybrid deployments](https://docs.microsoft.com/en-us/sccm/mdm/understand/choose-between-standalone-intune-and-hybrid-mobile-device-management) are not supported.</span></span> 

## <a name="using-the-intune-graph-api"></a><span data-ttu-id="5e881-107">Usar la API de Graph de Intune</span><span class="sxs-lookup"><span data-stu-id="5e881-107">Using the Intune Graph API</span></span>

<span data-ttu-id="5e881-108">Intune proporciona datos a la API de Microsoft Graph igual que lo hacen otros servicios en la nube, con navegación de relaciones e información sobre entidades enriquecida.</span><span class="sxs-lookup"><span data-stu-id="5e881-108">Intune provides data into the Microsoft Graph API in the same way as other cloud services do, with rich entity information and relationship navigation.</span></span><span data-ttu-id="5e881-109">Use la API de Microsoft Graph para combinar la información de otros servicios e Intune para crear completas aplicaciones de servicios cruzados para profesionales de TI o usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="5e881-109">  Use Microsoft Graph API to combine information from other services and Intune to build rich cross-service applications for IT professionals or end users.</span></span>     

<span data-ttu-id="5e881-110">Este es un ejemplo de cómo puede determinar si una aplicación está instalada en el dispositivo de un usuario:</span><span class="sxs-lookup"><span data-stu-id="5e881-110">Here is an example of how you can determine whether an application is installed on a user's device:</span></span> 

1. <span data-ttu-id="5e881-111">Obtenga de Azure Active Directory una lista de dispositivos registrados para un usuario:</span><span class="sxs-lookup"><span data-stu-id="5e881-111">Get from Azure Active Directory a list of devices registered to a user:</span></span> 

    https://graph.microsoft.com/users/{user}/ownedDevices 

2. <span data-ttu-id="5e881-112">A continuación, vea la lista de aplicaciones de su espacio empresarial:</span><span class="sxs-lookup"><span data-stu-id="5e881-112">Then view the list of applications for your tenant:</span></span> 

    https://graph.microsoft.com/deviceAppManagement/mobileApps  

3. <span data-ttu-id="5e881-113">Tome el identificador de la aplicación y determine el estado de instalación para la aplicación (y, por tanto, el usuario):</span><span class="sxs-lookup"><span data-stu-id="5e881-113">Take the ID from the application and determine the installation state for the application (and therefore user):</span></span>

    https://graph.microsoft.com/deviceAppManagement/mobileApps/{id}/deviceStatuses/


## <a name="using-permission-scopes"></a><span data-ttu-id="5e881-114">Usar los ámbitos de permisos</span><span class="sxs-lookup"><span data-stu-id="5e881-114">Using permission scopes</span></span>

<span data-ttu-id="5e881-115">La API de Microsoft Graph controla el acceso a los recursos que usan los ámbitos de permisos.</span><span class="sxs-lookup"><span data-stu-id="5e881-115">Microsoft Graph API controls access to resources using permission scopes.</span></span> <span data-ttu-id="5e881-116">Como desarrollador, debe especificar los ámbitos de permisos que necesita para tener acceso a los recursos de Intune.</span><span class="sxs-lookup"><span data-stu-id="5e881-116">As a developer, you must specify the permission scopes you need to access Intune resources.</span></span> <span data-ttu-id="5e881-117">Normalmente, los ámbitos de permisos se especifican en el portal de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5e881-117">Typically, you specify the permission scopes you need in the Azure Active Directory portal.</span></span> <span data-ttu-id="5e881-118">Para obtener más información, consulte [Ámbitos de permiso de Microsoft Graph](https://developer.microsoft.com/graph/docs/authorization/permission_scopes) y [Ámbitos de permisos de Intune](https://developer.microsoft.com/graph/docs/authorization/permission_scopes#permission-scopes-in-preview).</span><span class="sxs-lookup"><span data-stu-id="5e881-118">For more information, see [Microsoft Graph permission scopes](https://developer.microsoft.com/graph/docs/authorization/permission_scopes) and [Intune permission scopes](https://developer.microsoft.com/graph/docs/authorization/permission_scopes#permission-scopes-in-preview).</span></span>

## <a name="next-steps"></a><span data-ttu-id="5e881-119">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="5e881-119">Next Steps</span></span>

- <span data-ttu-id="5e881-120">Obtenga información sobre [cómo usar Azure AD](https://docs.microsoft.com/en-us/intune/intune-graph-apis) para obtener acceso a la API de Microsoft Graph para Intune.</span><span class="sxs-lookup"><span data-stu-id="5e881-120">Learn [how to use Azure AD](https://docs.microsoft.com/en-us/intune/intune-graph-apis) to access the Microsoft Graph API for Intune.</span></span>  
- <span data-ttu-id="5e881-121">Explore los [ejemplos de PowerShell Intune](https://github.com/microsoftgraph/powershell-intune-samples), que muestran cómo usar las API de gráfico para Intune en contexto de ejemplos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="5e881-121">Explore the [PowerShell Intune samples](https://github.com/microsoftgraph/powershell-intune-samples), which show how to use Graph API for Intune in context of working examples.</span></span>