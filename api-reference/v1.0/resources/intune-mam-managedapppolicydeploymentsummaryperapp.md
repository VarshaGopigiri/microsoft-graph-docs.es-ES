---
title: Tipo de recurso managedAppPolicyDeploymentSummaryPerApp
description: Representa el resumen de implementación de directivas por aplicación.
author: tfitzmac
ms.openlocfilehash: 95c05696f6c080f90b9de61c309a577924e599b1
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27354344"
---
# <a name="managedapppolicydeploymentsummaryperapp-resource-type"></a><span data-ttu-id="b12f2-103">Tipo de recurso managedAppPolicyDeploymentSummaryPerApp</span><span class="sxs-lookup"><span data-stu-id="b12f2-103">managedAppPolicyDeploymentSummaryPerApp resource type</span></span>

> <span data-ttu-id="b12f2-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b12f2-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b12f2-105">Representa el resumen de implementación de directivas por aplicación.</span><span class="sxs-lookup"><span data-stu-id="b12f2-105">Represents policy deployment summary per app.</span></span>
## <a name="properties"></a><span data-ttu-id="b12f2-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b12f2-106">Properties</span></span>
|<span data-ttu-id="b12f2-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b12f2-107">Property</span></span>|<span data-ttu-id="b12f2-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="b12f2-108">Type</span></span>|<span data-ttu-id="b12f2-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b12f2-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b12f2-110">mobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="b12f2-110">mobileAppIdentifier</span></span>|[<span data-ttu-id="b12f2-111">mobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="b12f2-111">mobileAppIdentifier</span></span>](../resources/intune-mam-mobileappidentifier.md)|<span data-ttu-id="b12f2-112">Implementación de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="b12f2-112">Deployment of an app.</span></span>|
|<span data-ttu-id="b12f2-113">configurationAppliedUserCount</span><span class="sxs-lookup"><span data-stu-id="b12f2-113">configurationAppliedUserCount</span></span>|<span data-ttu-id="b12f2-114">Int32</span><span class="sxs-lookup"><span data-stu-id="b12f2-114">Int32</span></span>|<span data-ttu-id="b12f2-115">Número de usuarios a los que se aplica la directiva.</span><span class="sxs-lookup"><span data-stu-id="b12f2-115">Number of users the policy is applied.</span></span>|

## <a name="relationships"></a><span data-ttu-id="b12f2-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b12f2-116">Relationships</span></span>
<span data-ttu-id="b12f2-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="b12f2-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="b12f2-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b12f2-118">JSON Representation</span></span>
<span data-ttu-id="b12f2-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b12f2-119">Here is a JSON representation of the resource.</span></span>
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



