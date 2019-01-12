---
title: Tipo de recurso managedAppPolicyDeploymentSummaryPerApp
description: Representa el resumen de implementación de directivas por aplicación.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 211b40c397ec7e3fb4000c8f4459056edec2a6f1
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27972204"
---
# <a name="managedapppolicydeploymentsummaryperapp-resource-type"></a><span data-ttu-id="fbd9c-103">Tipo de recurso managedAppPolicyDeploymentSummaryPerApp</span><span class="sxs-lookup"><span data-stu-id="fbd9c-103">managedAppPolicyDeploymentSummaryPerApp resource type</span></span>

> <span data-ttu-id="fbd9c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fbd9c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fbd9c-105">Representa el resumen de implementación de directivas por aplicación.</span><span class="sxs-lookup"><span data-stu-id="fbd9c-105">Represents policy deployment summary per app.</span></span>
## <a name="properties"></a><span data-ttu-id="fbd9c-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fbd9c-106">Properties</span></span>
|<span data-ttu-id="fbd9c-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fbd9c-107">Property</span></span>|<span data-ttu-id="fbd9c-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="fbd9c-108">Type</span></span>|<span data-ttu-id="fbd9c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="fbd9c-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fbd9c-110">mobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="fbd9c-110">mobileAppIdentifier</span></span>|[<span data-ttu-id="fbd9c-111">mobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="fbd9c-111">mobileAppIdentifier</span></span>](../resources/intune-mam-mobileappidentifier.md)|<span data-ttu-id="fbd9c-112">Implementación de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="fbd9c-112">Deployment of an app.</span></span>|
|<span data-ttu-id="fbd9c-113">configurationAppliedUserCount</span><span class="sxs-lookup"><span data-stu-id="fbd9c-113">configurationAppliedUserCount</span></span>|<span data-ttu-id="fbd9c-114">Int32</span><span class="sxs-lookup"><span data-stu-id="fbd9c-114">Int32</span></span>|<span data-ttu-id="fbd9c-115">Número de usuarios a los que se aplica la directiva.</span><span class="sxs-lookup"><span data-stu-id="fbd9c-115">Number of users the policy is applied.</span></span>|

## <a name="relationships"></a><span data-ttu-id="fbd9c-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="fbd9c-116">Relationships</span></span>
<span data-ttu-id="fbd9c-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="fbd9c-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="fbd9c-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fbd9c-118">JSON Representation</span></span>
<span data-ttu-id="fbd9c-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="fbd9c-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.managedAppPolicyDeploymentSummaryPerApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppPolicyDeploymentSummaryPerApp",
  "mobileAppIdentifier": {
    "@odata.type": "microsoft.graph.mobileAppIdentifier"
  },
  "configurationAppliedUserCount": 1024
}
```



