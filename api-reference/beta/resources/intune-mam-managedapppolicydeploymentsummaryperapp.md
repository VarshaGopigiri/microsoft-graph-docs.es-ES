---
title: Tipo de recurso managedAppPolicyDeploymentSummaryPerApp
description: Representa el resumen de implementación de directivas por aplicación.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 23966e2017780d3dcfde592d7159576403fe3192
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27829753"
---
# <a name="managedapppolicydeploymentsummaryperapp-resource-type"></a><span data-ttu-id="402b5-103">Tipo de recurso managedAppPolicyDeploymentSummaryPerApp</span><span class="sxs-lookup"><span data-stu-id="402b5-103">managedAppPolicyDeploymentSummaryPerApp resource type</span></span>

> <span data-ttu-id="402b5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="402b5-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="402b5-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="402b5-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="402b5-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="402b5-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="402b5-107">Representa el resumen de implementación de directivas por aplicación.</span><span class="sxs-lookup"><span data-stu-id="402b5-107">Represents policy deployment summary per app.</span></span>
## <a name="properties"></a><span data-ttu-id="402b5-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="402b5-108">Properties</span></span>
|<span data-ttu-id="402b5-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="402b5-109">Property</span></span>|<span data-ttu-id="402b5-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="402b5-110">Type</span></span>|<span data-ttu-id="402b5-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="402b5-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="402b5-112">mobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="402b5-112">mobileAppIdentifier</span></span>|[<span data-ttu-id="402b5-113">mobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="402b5-113">mobileAppIdentifier</span></span>](../resources/intune-mam-mobileappidentifier.md)|<span data-ttu-id="402b5-114">Implementación de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="402b5-114">Deployment of an app.</span></span>|
|<span data-ttu-id="402b5-115">configurationAppliedUserCount</span><span class="sxs-lookup"><span data-stu-id="402b5-115">configurationAppliedUserCount</span></span>|<span data-ttu-id="402b5-116">Int32</span><span class="sxs-lookup"><span data-stu-id="402b5-116">Int32</span></span>|<span data-ttu-id="402b5-117">Número de usuarios a los que se aplica la directiva.</span><span class="sxs-lookup"><span data-stu-id="402b5-117">Number of users the policy is applied.</span></span>|

## <a name="relationships"></a><span data-ttu-id="402b5-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="402b5-118">Relationships</span></span>
<span data-ttu-id="402b5-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="402b5-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="402b5-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="402b5-120">JSON Representation</span></span>
<span data-ttu-id="402b5-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="402b5-121">Here is a JSON representation of the resource.</span></span>
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





