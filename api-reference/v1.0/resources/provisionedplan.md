---
title: Tipo de recurso provisionedPlan
description: La propiedad **provisionedPlans** de la entidad user y la entidad organization es una colección de **provisionedPlan**.
ms.openlocfilehash: 7808e3a17e471123f702381fb52535e53682e276
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031225"
---
# <a name="provisionedplan-resource-type"></a><span data-ttu-id="b26c3-103">Tipo de recurso provisionedPlan</span><span class="sxs-lookup"><span data-stu-id="b26c3-103">provisionedPlan resource type</span></span>

<span data-ttu-id="b26c3-104">La propiedad **provisionedPlans** de la entidad [user](user.md) y la entidad [organization](organization.md) es una colección de **provisionedPlan**.</span><span class="sxs-lookup"><span data-stu-id="b26c3-104">The **provisionedPlans** property of the [user](user.md) entity and the [organization](organization.md) entity is a collection of **provisionedPlan**.</span></span>


## <a name="properties"></a><span data-ttu-id="b26c3-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b26c3-105">Properties</span></span>
| <span data-ttu-id="b26c3-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b26c3-106">Property</span></span>     | <span data-ttu-id="b26c3-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="b26c3-107">Type</span></span>   |<span data-ttu-id="b26c3-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="b26c3-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b26c3-109">capabilityStatus</span><span class="sxs-lookup"><span data-stu-id="b26c3-109">capabilityStatus</span></span>|<span data-ttu-id="b26c3-110">String</span><span class="sxs-lookup"><span data-stu-id="b26c3-110">String</span></span>|<span data-ttu-id="b26c3-111">Por ejemplo, "Habilitado".</span><span class="sxs-lookup"><span data-stu-id="b26c3-111">For example, “Enabled”.</span></span>|
|<span data-ttu-id="b26c3-112">provisioningStatus</span><span class="sxs-lookup"><span data-stu-id="b26c3-112">provisioningStatus</span></span>|<span data-ttu-id="b26c3-113">String</span><span class="sxs-lookup"><span data-stu-id="b26c3-113">String</span></span>|<span data-ttu-id="b26c3-114">Por ejemplo, "Correcto".</span><span class="sxs-lookup"><span data-stu-id="b26c3-114">For example, “Success”.</span></span>|
|<span data-ttu-id="b26c3-115">service</span><span class="sxs-lookup"><span data-stu-id="b26c3-115">service</span></span>|<span data-ttu-id="b26c3-116">String</span><span class="sxs-lookup"><span data-stu-id="b26c3-116">String</span></span>|<span data-ttu-id="b26c3-117">Nombre del servicio; por ejemplo, "AccessControlS2S".</span><span class="sxs-lookup"><span data-stu-id="b26c3-117">The name of the service; for example, “AccessControlS2S”</span></span>|

## <a name="json-representation"></a><span data-ttu-id="b26c3-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b26c3-118">JSON representation</span></span>

<span data-ttu-id="b26c3-119">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="b26c3-119">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.provisionedPlan"
}-->

```json
{
  "capabilityStatus": "string",
  "provisioningStatus": "string",
  "service": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "provisionedPlan resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->