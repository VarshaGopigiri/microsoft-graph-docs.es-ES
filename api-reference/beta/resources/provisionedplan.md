---
title: Tipo de recurso provisionedPlan
description: La propiedad **provisionedPlans** de la entidad user y la entidad organization es una colección de **provisionedPlan**.
ms.openlocfilehash: efaf4dc2916189e2bf6a8078a693059369f7cb2b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086728"
---
# <a name="provisionedplan-resource-type"></a><span data-ttu-id="5ebad-103">Tipo de recurso provisionedPlan</span><span class="sxs-lookup"><span data-stu-id="5ebad-103">provisionedPlan resource type</span></span>

> <span data-ttu-id="5ebad-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5ebad-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5ebad-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5ebad-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5ebad-106">La propiedad **provisionedPlans** de la entidad [user](user.md) y la entidad [organization](organization.md) es una colección de **provisionedPlan**.</span><span class="sxs-lookup"><span data-stu-id="5ebad-106">The **provisionedPlans** property of the [user](user.md) entity and the [organization](organization.md) entity is a collection of **provisionedPlan**.</span></span>


## <a name="properties"></a><span data-ttu-id="5ebad-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5ebad-107">Properties</span></span>
| <span data-ttu-id="5ebad-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5ebad-108">Property</span></span>     | <span data-ttu-id="5ebad-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="5ebad-109">Type</span></span>   |<span data-ttu-id="5ebad-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ebad-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5ebad-111">capabilityStatus</span><span class="sxs-lookup"><span data-stu-id="5ebad-111">capabilityStatus</span></span>|<span data-ttu-id="5ebad-112">String</span><span class="sxs-lookup"><span data-stu-id="5ebad-112">String</span></span>|<span data-ttu-id="5ebad-113">Por ejemplo, "Habilitado".</span><span class="sxs-lookup"><span data-stu-id="5ebad-113">For example, “Enabled”.</span></span>|
|<span data-ttu-id="5ebad-114">provisioningStatus</span><span class="sxs-lookup"><span data-stu-id="5ebad-114">provisioningStatus</span></span>|<span data-ttu-id="5ebad-115">String</span><span class="sxs-lookup"><span data-stu-id="5ebad-115">String</span></span>|<span data-ttu-id="5ebad-116">Por ejemplo, "Correcto".</span><span class="sxs-lookup"><span data-stu-id="5ebad-116">For example, “Success”.</span></span>|
|<span data-ttu-id="5ebad-117">service</span><span class="sxs-lookup"><span data-stu-id="5ebad-117">service</span></span>|<span data-ttu-id="5ebad-118">String</span><span class="sxs-lookup"><span data-stu-id="5ebad-118">String</span></span>|<span data-ttu-id="5ebad-119">Nombre del servicio; por ejemplo, "AccessControlS2S".</span><span class="sxs-lookup"><span data-stu-id="5ebad-119">The name of the service; for example, “AccessControlS2S”</span></span>|

## <a name="json-representation"></a><span data-ttu-id="5ebad-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5ebad-120">JSON representation</span></span>

<span data-ttu-id="5ebad-121">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="5ebad-121">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.provisionedplan"
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