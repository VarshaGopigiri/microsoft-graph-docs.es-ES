---
title: Tipo de recurso provisionedPlan
description: La propiedad **provisionedPlans** de la entidad user y la entidad organization es una colección de **provisionedPlan**.
localization_priority: Normal
ms.openlocfilehash: dd8d4f5b406a2291a829d7c11d4948bd9a08d453
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27831489"
---
# <a name="provisionedplan-resource-type"></a><span data-ttu-id="ac3d8-103">Tipo de recurso provisionedPlan</span><span class="sxs-lookup"><span data-stu-id="ac3d8-103">provisionedPlan resource type</span></span>

<span data-ttu-id="ac3d8-104">La propiedad **provisionedPlans** de la entidad [user](user.md) y la entidad [organization](organization.md) es una colección de **provisionedPlan**.</span><span class="sxs-lookup"><span data-stu-id="ac3d8-104">The **provisionedPlans** property of the [user](user.md) entity and the [organization](organization.md) entity is a collection of **provisionedPlan**.</span></span>


## <a name="properties"></a><span data-ttu-id="ac3d8-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ac3d8-105">Properties</span></span>
| <span data-ttu-id="ac3d8-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ac3d8-106">Property</span></span>     | <span data-ttu-id="ac3d8-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="ac3d8-107">Type</span></span>   |<span data-ttu-id="ac3d8-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac3d8-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ac3d8-109">capabilityStatus</span><span class="sxs-lookup"><span data-stu-id="ac3d8-109">capabilityStatus</span></span>|<span data-ttu-id="ac3d8-110">String</span><span class="sxs-lookup"><span data-stu-id="ac3d8-110">String</span></span>|<span data-ttu-id="ac3d8-111">Por ejemplo, "Habilitado".</span><span class="sxs-lookup"><span data-stu-id="ac3d8-111">For example, “Enabled”.</span></span>|
|<span data-ttu-id="ac3d8-112">provisioningStatus</span><span class="sxs-lookup"><span data-stu-id="ac3d8-112">provisioningStatus</span></span>|<span data-ttu-id="ac3d8-113">String</span><span class="sxs-lookup"><span data-stu-id="ac3d8-113">String</span></span>|<span data-ttu-id="ac3d8-114">Por ejemplo, "Correcto".</span><span class="sxs-lookup"><span data-stu-id="ac3d8-114">For example, “Success”.</span></span>|
|<span data-ttu-id="ac3d8-115">service</span><span class="sxs-lookup"><span data-stu-id="ac3d8-115">service</span></span>|<span data-ttu-id="ac3d8-116">String</span><span class="sxs-lookup"><span data-stu-id="ac3d8-116">String</span></span>|<span data-ttu-id="ac3d8-117">Nombre del servicio; por ejemplo, "AccessControlS2S".</span><span class="sxs-lookup"><span data-stu-id="ac3d8-117">The name of the service; for example, “AccessControlS2S”</span></span>|

## <a name="json-representation"></a><span data-ttu-id="ac3d8-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ac3d8-118">JSON representation</span></span>

<span data-ttu-id="ac3d8-119">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="ac3d8-119">Here is a JSON representation of the resource</span></span>

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
