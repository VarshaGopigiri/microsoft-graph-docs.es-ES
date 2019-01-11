---
title: Tipo de recurso managedAppPolicyDeploymentSummaryPerApp
description: Representa el resumen de implementación de directivas por aplicación.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 025103e40e3babde67437952fe8730b0f04410d2
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27855170"
---
# <a name="managedapppolicydeploymentsummaryperapp-resource-type"></a><span data-ttu-id="09d75-103">Tipo de recurso managedAppPolicyDeploymentSummaryPerApp</span><span class="sxs-lookup"><span data-stu-id="09d75-103">managedAppPolicyDeploymentSummaryPerApp resource type</span></span>

> <span data-ttu-id="09d75-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="09d75-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="09d75-105">Representa el resumen de implementación de directivas por aplicación.</span><span class="sxs-lookup"><span data-stu-id="09d75-105">Represents policy deployment summary per app.</span></span>
## <a name="properties"></a><span data-ttu-id="09d75-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="09d75-106">Properties</span></span>
|<span data-ttu-id="09d75-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="09d75-107">Property</span></span>|<span data-ttu-id="09d75-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="09d75-108">Type</span></span>|<span data-ttu-id="09d75-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="09d75-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="09d75-110">mobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="09d75-110">mobileAppIdentifier</span></span>|[<span data-ttu-id="09d75-111">mobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="09d75-111">mobileAppIdentifier</span></span>](../resources/intune-mam-mobileappidentifier.md)|<span data-ttu-id="09d75-112">Implementación de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="09d75-112">Deployment of an app.</span></span>|
|<span data-ttu-id="09d75-113">configurationAppliedUserCount</span><span class="sxs-lookup"><span data-stu-id="09d75-113">configurationAppliedUserCount</span></span>|<span data-ttu-id="09d75-114">Int32</span><span class="sxs-lookup"><span data-stu-id="09d75-114">Int32</span></span>|<span data-ttu-id="09d75-115">Número de usuarios a los que se aplica la directiva.</span><span class="sxs-lookup"><span data-stu-id="09d75-115">Number of users the policy is applied.</span></span>|

## <a name="relationships"></a><span data-ttu-id="09d75-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="09d75-116">Relationships</span></span>
<span data-ttu-id="09d75-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="09d75-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="09d75-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="09d75-118">JSON Representation</span></span>
<span data-ttu-id="09d75-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="09d75-119">Here is a JSON representation of the resource.</span></span>
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



