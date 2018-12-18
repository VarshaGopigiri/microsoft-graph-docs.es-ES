---
title: Usar la API de Graph de Intune
description: " No se admiten las implementaciones híbridas de Intune. "
author: tfitzmac
ms.openlocfilehash: cecce61dba0ddfc044c2e06e0e16d68401fcafb5
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27357249"
---
# <a name="working-with-intune-in-microsoft-graph"></a><span data-ttu-id="c94b5-103">Trabajar con Intune en Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="c94b5-103">Working with Intune in Microsoft Graph</span></span>  

> <span data-ttu-id="c94b5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c94b5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c94b5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c94b5-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c94b5-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune-pricing) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c94b5-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune-pricing) by the customer.</span></span>

<span data-ttu-id="c94b5-107">La API de Microsoft Graph para Intune permite el acceso mediante programación a la información de Intune para su espacio empresarial; la API realiza las mismas operaciones de Intune que las que están disponibles a través de **Azure Portal**.</span><span class="sxs-lookup"><span data-stu-id="c94b5-107">The Microsoft Graph API for Intune enables programmatic access to Intune information for your tenant; the API performs the same Intune operations as those available through the **Azure Portal**.</span></span>  

<span data-ttu-id="c94b5-108">Para escenarios de administración (MDM) del dispositivo móvil, la API de Microsoft Graph para Intune admite implementaciones independientes; No se admiten Intune [implementaciones híbridas](https://docs.microsoft.com/en-us/sccm/mdm/understand/choose-between-standalone-intune-and-hybrid-mobile-device-management) .</span><span class="sxs-lookup"><span data-stu-id="c94b5-108">For mobile device management (MDM) scenarios, the Microsoft Graph API for Intune supports standalone deployments; Intune [hybrid deployments](https://docs.microsoft.com/en-us/sccm/mdm/understand/choose-between-standalone-intune-and-hybrid-mobile-device-management) are not supported.</span></span> 

## <a name="using-the-microsoft-graph-api-for-intune"></a><span data-ttu-id="c94b5-109">Uso de la API de Microsoft Graph para Intune</span><span class="sxs-lookup"><span data-stu-id="c94b5-109">Using the Microsoft Graph API for Intune</span></span>

<span data-ttu-id="c94b5-110">En Microsoft Graph, Intune proporciona datos de la misma manera igual que otros servicios de nube, con la navegación de información y la relación de entidad enriquecido.</span><span class="sxs-lookup"><span data-stu-id="c94b5-110">Intune provides data into Microsoft Graph in the same way as other cloud services do, with rich entity information and relationship navigation.</span></span><span data-ttu-id="c94b5-111">Utilizar Microsoft Graph para combinar la información de otros servicios y Intune para crear aplicaciones de servicio de entre completas para profesionales de TI o los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="c94b5-111"> Use Microsoft Graph to combine information from other services and Intune to build rich cross-service applications for IT professionals or end users.</span></span>     

<span data-ttu-id="c94b5-112">En el ejemplo siguiente se muestra cómo se puede saber si una aplicación está instalada en el dispositivo del usuario:</span><span class="sxs-lookup"><span data-stu-id="c94b5-112">The following example shows how you can determine whether an application is installed on a user's device:</span></span> 

1. <span data-ttu-id="c94b5-113">Obtenga de Azure Active Directory una lista de dispositivos registrados para un usuario:</span><span class="sxs-lookup"><span data-stu-id="c94b5-113">Get from Azure Active Directory a list of devices registered to a user:</span></span> 

    https://graph.microsoft.com/beta/users/{user}/ownedDevices 

2. <span data-ttu-id="c94b5-114">A continuación, vea la lista de aplicaciones de su espacio empresarial:</span><span class="sxs-lookup"><span data-stu-id="c94b5-114">Then view the list of applications for your tenant:</span></span> 

    https://graph.microsoft.com/beta/deviceAppManagement/mobileApps  

3. <span data-ttu-id="c94b5-115">Tome el identificador de la aplicación y determine el estado de instalación para la aplicación (y, por tanto, el usuario):</span><span class="sxs-lookup"><span data-stu-id="c94b5-115">Take the ID from the application and determine the installation state for the application (and therefore user):</span></span>

    https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{id}/deviceStatuses/


## <a name="using-microsoft-graph-permissions"></a><span data-ttu-id="c94b5-116">Uso de permisos de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="c94b5-116">Using Microsoft Graph permissions</span></span>

<span data-ttu-id="c94b5-117">Gráfico de Microsof controla el acceso a recursos a través de los permisos.</span><span class="sxs-lookup"><span data-stu-id="c94b5-117">Microsof Graph controls access to resources via permissions.</span></span> <span data-ttu-id="c94b5-118">Como desarrollador, debe especificar los permisos que necesita tener acceso a recursos de Intune.</span><span class="sxs-lookup"><span data-stu-id="c94b5-118">As a developer, you must specify the permissions you need to access Intune resources.</span></span> <span data-ttu-id="c94b5-119">Normalmente, especifique los permisos en el portal de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c94b5-119">Typically, you specify the permissions in the Azure Active Directory portal.</span></span> <span data-ttu-id="c94b5-120">Para obtener más información, vea [referencia de permisos de Microsoft Graph](https://docs.microsoft.com/en-us/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c94b5-120">For more information, see [Microsoft Graph permissions reference](https://docs.microsoft.com/en-us/graph/permissions-reference).</span></span>

## <a name="next-steps"></a><span data-ttu-id="c94b5-121">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="c94b5-121">Next Steps</span></span>

- <span data-ttu-id="c94b5-122">Obtenga información sobre [cómo usar Azure AD](https://docs.microsoft.com/en-us/intune/intune-graph-apis) para obtener acceso a la API de Microsoft Graph para Intune.</span><span class="sxs-lookup"><span data-stu-id="c94b5-122">Learn [how to use Azure AD](https://docs.microsoft.com/en-us/intune/intune-graph-apis) to access the Microsoft Graph API for Intune.</span></span>  
- <span data-ttu-id="c94b5-123">Explore los [ejemplos de PowerShell Intune](https://github.com/microsoftgraph/powershell-intune-samples), que muestran cómo usar la API de Microsoft Graph para Intune en contexto de ejemplos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="c94b5-123">Explore the [PowerShell Intune samples](https://github.com/microsoftgraph/powershell-intune-samples), which show how to use the Microsoft Graph API for Intune in context of working examples.</span></span>

