---
title: Tipo de recurso responseStatus
description: Estado de la respuesta de una convocatoria de reunión.
localization_priority: Normal
ms.openlocfilehash: b337422615e2c34791cd5181a446c25201c183e6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27843032"
---
# <a name="responsestatus-resource-type"></a><span data-ttu-id="db100-103">Tipo de recurso responseStatus</span><span class="sxs-lookup"><span data-stu-id="db100-103">responseStatus resource type</span></span>

> <span data-ttu-id="db100-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="db100-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="db100-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="db100-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="db100-106">Estado de la respuesta de una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="db100-106">The response status of a meeting request.</span></span>

## <a name="properties"></a><span data-ttu-id="db100-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="db100-107">Properties</span></span>

| <span data-ttu-id="db100-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="db100-108">Property</span></span> | <span data-ttu-id="db100-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="db100-109">Type</span></span>           | <span data-ttu-id="db100-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="db100-110">Description</span></span> |
|:---------|:---------------|:------------|
| <span data-ttu-id="db100-111">response</span><span class="sxs-lookup"><span data-stu-id="db100-111">response</span></span> | <span data-ttu-id="db100-112">String</span><span class="sxs-lookup"><span data-stu-id="db100-112">String</span></span>         | <span data-ttu-id="db100-113">Tipo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="db100-113">The response type.</span></span> <span data-ttu-id="db100-114">Los valores posibles son: `None`, `Organizer`, `TentativelyAccepted`, `Accepted`, `Declined` y `NotResponded`.</span><span class="sxs-lookup"><span data-stu-id="db100-114">Possible values are: `None`, `Organizer`, `TentativelyAccepted`, `Accepted`, `Declined`, `NotResponded`.</span></span>
| <span data-ttu-id="db100-115">time</span><span class="sxs-lookup"><span data-stu-id="db100-115">time</span></span>     | <span data-ttu-id="db100-116">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="db100-116">DateTimeOffset</span></span> | <span data-ttu-id="db100-p103">Fecha y hora en que se devolvió la respuesta. Usa el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="db100-p103">The date and time that the response was returned. It uses ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>

## <a name="json-representation"></a><span data-ttu-id="db100-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="db100-120">JSON representation</span></span>

<span data-ttu-id="db100-121">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="db100-121">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.responseStatus"
}-->

```json
{
  "response": "String",
  "time": "String (timestamp)"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "responseStatus resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
