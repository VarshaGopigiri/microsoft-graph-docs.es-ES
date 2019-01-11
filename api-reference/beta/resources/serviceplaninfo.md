---
title: Tipo de recurso servicePlanInfo
description: Contiene información sobre un plan de servicio asociado a una SKU suscrita. La propiedad **servicePlans** de la entidad subscribedSku es una colección de **servicePlanInfo**.
localization_priority: Normal
ms.openlocfilehash: f0cb96a11b280fcda4e97a6dad30a9e5200c2e88
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27842683"
---
# <a name="serviceplaninfo-resource-type"></a><span data-ttu-id="161eb-104">Tipo de recurso servicePlanInfo</span><span class="sxs-lookup"><span data-stu-id="161eb-104">servicePlanInfo resource type</span></span>

> <span data-ttu-id="161eb-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="161eb-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="161eb-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="161eb-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="161eb-p103">Contiene información sobre un plan de servicio asociado a una SKU suscrita. La propiedad **servicePlans** de la entidad [subscribedSku](subscribedsku.md) es una colección de **servicePlanInfo**.</span><span class="sxs-lookup"><span data-stu-id="161eb-p103">Contains information about a service plan associated with a subscribed SKU. The **servicePlans** property of the [subscribedSku](subscribedsku.md) entity is a collection of **servicePlanInfo**.</span></span>


## <a name="properties"></a><span data-ttu-id="161eb-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="161eb-109">Properties</span></span>
| <span data-ttu-id="161eb-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="161eb-110">Property</span></span>     | <span data-ttu-id="161eb-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="161eb-111">Type</span></span>   |<span data-ttu-id="161eb-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="161eb-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="161eb-113">servicePlanId</span><span class="sxs-lookup"><span data-stu-id="161eb-113">servicePlanId</span></span>|<span data-ttu-id="161eb-114">Guid</span><span class="sxs-lookup"><span data-stu-id="161eb-114">Guid</span></span>|<span data-ttu-id="161eb-115">Identificador único del plan de servicio.</span><span class="sxs-lookup"><span data-stu-id="161eb-115">The unique identifier of the service plan.</span></span>|
|<span data-ttu-id="161eb-116">servicePlanName</span><span class="sxs-lookup"><span data-stu-id="161eb-116">servicePlanName</span></span>|<span data-ttu-id="161eb-117">String</span><span class="sxs-lookup"><span data-stu-id="161eb-117">String</span></span>|<span data-ttu-id="161eb-118">Nombre del plan de servicio.</span><span class="sxs-lookup"><span data-stu-id="161eb-118">The name of the service plan.</span></span>|
|<span data-ttu-id="161eb-119">provisioningStatus</span><span class="sxs-lookup"><span data-stu-id="161eb-119">provisioningStatus</span></span>|<span data-ttu-id="161eb-120">String</span><span class="sxs-lookup"><span data-stu-id="161eb-120">String</span></span>|<span data-ttu-id="161eb-p104">El estado de aprovisionamiento del plan de servicio. Valores posibles:</span><span class="sxs-lookup"><span data-stu-id="161eb-p104">The provisioning status of the service plan. Possible values:</span></span><br/><span data-ttu-id="161eb-123">“Success”: el servicio está completamente aprovisionado.</span><span class="sxs-lookup"><span data-stu-id="161eb-123">"Success" - Service is fully provisioned.</span></span><br/><span data-ttu-id="161eb-124">“Disabled”: se deshabilitó el servicio.</span><span class="sxs-lookup"><span data-stu-id="161eb-124">"Disabled" - Service has been disabled.</span></span><br/><span data-ttu-id="161eb-125">“PendingInput”: aún no se aprovisionó el servicio; esperando la confirmación del servicio.</span><span class="sxs-lookup"><span data-stu-id="161eb-125">"PendingInput" - Service is not yet provisioned; awaiting service confirmation.</span></span><br/><span data-ttu-id="161eb-126">"PendingActivation" - servicio está configurado, pero requiere la activación explícita por el administrador (por ejemplo, el plan de servicio Intune_O365).</span><span class="sxs-lookup"><span data-stu-id="161eb-126">"PendingActivation" - Service is provisioned but requires explicit activation by administrator (for example, Intune_O365 service plan).</span></span><br/><span data-ttu-id="161eb-127">“PendingProvisioning”: Microsoft agregó un nuevo servicio al SKU del producto y aún no se activó en el inquilino.</span><span class="sxs-lookup"><span data-stu-id="161eb-127">"PendingProvisioning" - Microsoft has added a new service to the product SKU and it has not been activated in the tenant, yet.</span></span>|
|<span data-ttu-id="161eb-128">appliesTo</span><span class="sxs-lookup"><span data-stu-id="161eb-128">appliesTo</span></span>|<span data-ttu-id="161eb-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="161eb-129">String</span></span>|<span data-ttu-id="161eb-p105">El objeto al que se puede asignar el plan de servicio. Valores posibles:</span><span class="sxs-lookup"><span data-stu-id="161eb-p105">The object the service plan can be assigned to. Possible values:</span></span><br/><span data-ttu-id="161eb-132">“User”: el plan de servicio se puede asignar a usuarios individuales.</span><span class="sxs-lookup"><span data-stu-id="161eb-132">"User" - service plan can be assigned to individual users.</span></span><br/><span data-ttu-id="161eb-133">“Company”: el plan de servicio se puede asignar a todo el inquilino.</span><span class="sxs-lookup"><span data-stu-id="161eb-133">"Company" - service plan can be assigned to the entire tenant.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="161eb-134">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="161eb-134">JSON representation</span></span>

<span data-ttu-id="161eb-135">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="161eb-135">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.servicePlanInfo"
}-->

```json
{
  "appliesTo": "string",
  "provisioningStatus": "string",
  "servicePlanId": "guid",
  "servicePlanName": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "servicePlanInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
