---
title: Usar la API de Graph de Intune
description: " No se admiten las implementaciones híbridas de Intune. "
author: tfitzmac
localization_priority: Priority
ms.openlocfilehash: 1222f064b075c8884f5c66c101ae0e15256221c5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27830684"
---
# <a name="working-with-intune-in-microsoft-graph"></a><span data-ttu-id="be6f3-103">Trabajar con Intune en Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="be6f3-103">Working with Intune in Microsoft Graph</span></span>  

> <span data-ttu-id="be6f3-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune-pricing) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="be6f3-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune-pricing) by the customer.</span></span>

<span data-ttu-id="be6f3-105">La API de Microsoft Graph para Intune permite el acceso mediante programación a la información de Intune para su espacio empresarial; la API realiza las mismas operaciones de Intune que las que están disponibles a través de **Azure Portal**.</span><span class="sxs-lookup"><span data-stu-id="be6f3-105">The Microsoft Graph API for Intune enables programmatic access to Intune information for your tenant; the API performs the same Intune operations as those available through the **Azure Portal**.</span></span>  

<span data-ttu-id="be6f3-106">Para escenarios de administración (MDM) del dispositivo móvil, la API de Microsoft Graph para Intune admite implementaciones independientes; No se admiten Intune [implementaciones híbridas](https://docs.microsoft.com/en-us/sccm/mdm/understand/choose-between-standalone-intune-and-hybrid-mobile-device-management) .</span><span class="sxs-lookup"><span data-stu-id="be6f3-106">For mobile device management (MDM) scenarios, the Microsoft Graph API for Intune supports standalone deployments; Intune [hybrid deployments](https://docs.microsoft.com/en-us/sccm/mdm/understand/choose-between-standalone-intune-and-hybrid-mobile-device-management) are not supported.</span></span> 

## <a name="using-the-microsoft-graph-api-for-intune"></a><span data-ttu-id="be6f3-107">Uso de la API de Microsoft Graph para Intune</span><span class="sxs-lookup"><span data-stu-id="be6f3-107">Using the Microsoft Graph API for Intune</span></span>

<span data-ttu-id="be6f3-108">Intune proporciona datos a la API de Microsoft Graph igual que lo hacen otros servicios en la nube, con navegación de relaciones e información sobre entidades enriquecida.</span><span class="sxs-lookup"><span data-stu-id="be6f3-108">Intune provides data into the Microsoft Graph API in the same way as other cloud services do, with rich entity information and relationship navigation.</span></span><span data-ttu-id="be6f3-109">Usar la API de gráfico de Microsoft para combinar la información de otros servicios y Intune para crear aplicaciones de servicio de entre completas para profesionales de TI o los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="be6f3-109"> Use the Microsoft Graph API to combine information from other services and Intune to build rich cross-service applications for IT professionals or end users.</span></span>     

<span data-ttu-id="be6f3-110">En el ejemplo siguiente se muestra cómo se puede saber si una aplicación está instalada en el dispositivo del usuario:</span><span class="sxs-lookup"><span data-stu-id="be6f3-110">The following example shows how you can determine whether an application is installed on a user's device:</span></span> 

1. <span data-ttu-id="be6f3-111">Obtenga de Azure Active Directory una lista de dispositivos registrados para un usuario:</span><span class="sxs-lookup"><span data-stu-id="be6f3-111">Get from Azure Active Directory a list of devices registered to a user:</span></span> 

    https://graph.microsoft.com/users/{user}/ownedDevices 

2. <span data-ttu-id="be6f3-112">A continuación, vea la lista de aplicaciones de su espacio empresarial:</span><span class="sxs-lookup"><span data-stu-id="be6f3-112">Then view the list of applications for your tenant:</span></span> 

    https://graph.microsoft.com/deviceAppManagement/mobileApps  

3. <span data-ttu-id="be6f3-113">Tome el identificador de la aplicación y determine el estado de instalación para la aplicación (y, por tanto, el usuario):</span><span class="sxs-lookup"><span data-stu-id="be6f3-113">Take the ID from the application and determine the installation state for the application (and therefore user):</span></span>

    https://graph.microsoft.com/deviceAppManagement/mobileApps/{id}/deviceStatuses/


## <a name="using-permissions"></a><span data-ttu-id="be6f3-114">Uso de permisos</span><span class="sxs-lookup"><span data-stu-id="be6f3-114">Using permissions</span></span>

<span data-ttu-id="be6f3-115">La API de Microsoft Graph controla el acceso a recursos a través de los permisos.</span><span class="sxs-lookup"><span data-stu-id="be6f3-115">The Microsoft Graph API controls access to resources via permissions.</span></span> <span data-ttu-id="be6f3-116">Como desarrollador, debe especificar los permisos que necesita tener acceso a recursos de Intune.</span><span class="sxs-lookup"><span data-stu-id="be6f3-116">As a developer, you must specify the permissions you need to access Intune resources.</span></span> <span data-ttu-id="be6f3-117">Normalmente, especifique los permisos en el portal de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="be6f3-117">Typically, you specify the permissions in the Azure Active Directory portal.</span></span> <span data-ttu-id="be6f3-118">Para obtener más información, vea [referencia de permisos de Microsoft Graph](https://docs.microsoft.com/en-us/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="be6f3-118">For more information, see [Microsoft Graph permissions reference](https://docs.microsoft.com/en-us/graph/permissions-reference).</span></span>

## <a name="next-steps"></a><span data-ttu-id="be6f3-119">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="be6f3-119">Next Steps</span></span>

- <span data-ttu-id="be6f3-120">Obtenga información sobre [cómo usar Azure AD](https://docs.microsoft.com/en-us/intune/intune-graph-apis) para obtener acceso a la API de Microsoft Graph para Intune.</span><span class="sxs-lookup"><span data-stu-id="be6f3-120">Learn [how to use Azure AD](https://docs.microsoft.com/en-us/intune/intune-graph-apis) to access the Microsoft Graph API for Intune.</span></span>  
- <span data-ttu-id="be6f3-121">Explore los [ejemplos de PowerShell Intune](https://github.com/microsoftgraph/powershell-intune-samples), que muestran cómo usar la API de Microsoft Graph para Intune en contexto de ejemplos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="be6f3-121">Explore the [PowerShell Intune samples](https://github.com/microsoftgraph/powershell-intune-samples), which show how to use the Microsoft Graph API for Intune in context of working examples.</span></span>
