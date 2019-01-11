---
title: Tipo de recurso servicePlanInfo
description: Contiene información sobre un plan de servicio asociado a una SKU suscrita. La propiedad **servicePlans** de la entidad subscribedSku es una colección de **servicePlanInfo**.
localization_priority: Normal
ms.openlocfilehash: 837170881c7c093d26c5b59662e20e87b399a029
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27845454"
---
# <a name="serviceplaninfo-resource-type"></a><span data-ttu-id="7a030-104">Tipo de recurso servicePlanInfo</span><span class="sxs-lookup"><span data-stu-id="7a030-104">servicePlanInfo resource type</span></span>

<span data-ttu-id="7a030-p102">Contiene información sobre un plan de servicio asociado a una SKU suscrita. La propiedad **servicePlans** de la entidad [subscribedSku](subscribedsku.md) es una colección de **servicePlanInfo**.</span><span class="sxs-lookup"><span data-stu-id="7a030-p102">Contains information about a service plan associated with a subscribed SKU. The **servicePlans** property of the [subscribedSku](subscribedsku.md) entity is a collection of **servicePlanInfo**.</span></span>


## <a name="properties"></a><span data-ttu-id="7a030-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7a030-107">Properties</span></span>
| <span data-ttu-id="7a030-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7a030-108">Property</span></span>     | <span data-ttu-id="7a030-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="7a030-109">Type</span></span>   |<span data-ttu-id="7a030-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a030-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7a030-111">servicePlanId</span><span class="sxs-lookup"><span data-stu-id="7a030-111">servicePlanId</span></span>|<span data-ttu-id="7a030-112">Guid</span><span class="sxs-lookup"><span data-stu-id="7a030-112">Guid</span></span>|<span data-ttu-id="7a030-113">Identificador único del plan de servicio.</span><span class="sxs-lookup"><span data-stu-id="7a030-113">The unique identifier of the service plan.</span></span>|
|<span data-ttu-id="7a030-114">servicePlanName</span><span class="sxs-lookup"><span data-stu-id="7a030-114">servicePlanName</span></span>|<span data-ttu-id="7a030-115">String</span><span class="sxs-lookup"><span data-stu-id="7a030-115">String</span></span>|<span data-ttu-id="7a030-116">Nombre del plan de servicio.</span><span class="sxs-lookup"><span data-stu-id="7a030-116">The name of the service plan.</span></span>|
|<span data-ttu-id="7a030-117">provisioningStatus</span><span class="sxs-lookup"><span data-stu-id="7a030-117">provisioningStatus</span></span>|<span data-ttu-id="7a030-118">String</span><span class="sxs-lookup"><span data-stu-id="7a030-118">String</span></span>|<span data-ttu-id="7a030-p103">El estado de aprovisionamiento del plan de servicio. Valores posibles:</span><span class="sxs-lookup"><span data-stu-id="7a030-p103">The provisioning status of the service plan. Possible values:</span></span><br/><span data-ttu-id="7a030-121">“Success”: el servicio está completamente aprovisionado.</span><span class="sxs-lookup"><span data-stu-id="7a030-121">"Success" - Service is fully provisioned.</span></span><br/><span data-ttu-id="7a030-122">“Disabled”: se deshabilitó el servicio.</span><span class="sxs-lookup"><span data-stu-id="7a030-122">"Disabled" - Service has been disabled.</span></span><br/><span data-ttu-id="7a030-123">“PendingInput”: aún no se aprovisionó el servicio; esperando la confirmación del servicio.</span><span class="sxs-lookup"><span data-stu-id="7a030-123">"PendingInput" - Service is not yet provisioned; awaiting service confirmation.</span></span><br/><span data-ttu-id="7a030-124">“PendingActivation”: el servicio está aprovisionado, pero necesita una activación explícita por el administrador (por ejemplo, plan de servicio de Intune_O365).</span><span class="sxs-lookup"><span data-stu-id="7a030-124">"PendingActivation" - Service is provisioned but requires explicit activation by administrator (for example, Intune_O365 service plan)</span></span><br/><span data-ttu-id="7a030-125">“PendingProvisioning”: Microsoft agregó un nuevo servicio al SKU del producto y aún no se activó en el inquilino.</span><span class="sxs-lookup"><span data-stu-id="7a030-125">"PendingProvisioning" - Microsoft has added a new service to the product SKU and it has not been activated in the tenant, yet.</span></span>|
|<span data-ttu-id="7a030-126">appliesTo</span><span class="sxs-lookup"><span data-stu-id="7a030-126">appliesTo</span></span>|<span data-ttu-id="7a030-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="7a030-127">String</span></span>|<span data-ttu-id="7a030-p104">El objeto al que se puede asignar el plan de servicio. Valores posibles:</span><span class="sxs-lookup"><span data-stu-id="7a030-p104">The object the service plan can be assigned to. Possible values:</span></span><br/><span data-ttu-id="7a030-130">“User”: el plan de servicio se puede asignar a usuarios individuales.</span><span class="sxs-lookup"><span data-stu-id="7a030-130">"User" - service plan can be assigned to individual users.</span></span><br/><span data-ttu-id="7a030-131">“Company”: el plan de servicio se puede asignar a todo el inquilino.</span><span class="sxs-lookup"><span data-stu-id="7a030-131">"Company" - service plan can be assigned to the entire tenant.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="7a030-132">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7a030-132">JSON representation</span></span>

<span data-ttu-id="7a030-133">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="7a030-133">Here is a JSON representation of the resource</span></span>

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
