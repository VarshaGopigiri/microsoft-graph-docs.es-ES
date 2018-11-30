---
title: Tipo de recurso responseStatus
description: Estado de la respuesta de una convocatoria de reunión.
ms.openlocfilehash: 95f525bae387520888f006d6496a56dab9148145
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029503"
---
# <a name="responsestatus-resource-type"></a><span data-ttu-id="5a47c-103">Tipo de recurso responseStatus</span><span class="sxs-lookup"><span data-stu-id="5a47c-103">responseStatus resource type</span></span>

<span data-ttu-id="5a47c-104">Estado de la respuesta de una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="5a47c-104">The response status of a meeting request.</span></span>

## <a name="properties"></a><span data-ttu-id="5a47c-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5a47c-105">Properties</span></span>

| <span data-ttu-id="5a47c-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5a47c-106">Property</span></span> | <span data-ttu-id="5a47c-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="5a47c-107">Type</span></span>           | <span data-ttu-id="5a47c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="5a47c-108">Description</span></span> |
|:---------|:---------------|:------------|
| <span data-ttu-id="5a47c-109">response</span><span class="sxs-lookup"><span data-stu-id="5a47c-109">response</span></span> | <span data-ttu-id="5a47c-110">responseType</span><span class="sxs-lookup"><span data-stu-id="5a47c-110">responseType</span></span>   | <span data-ttu-id="5a47c-111">Tipo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5a47c-111">The response type.</span></span> <span data-ttu-id="5a47c-112">Los valores posibles son: `None`, `Organizer`, `TentativelyAccepted`, `Accepted`, `Declined`, `NotResponded`.</span><span class="sxs-lookup"><span data-stu-id="5a47c-112">The possible values are: `None`, `Organizer`, `TentativelyAccepted`, `Accepted`, `Declined`, `NotResponded`.</span></span>
| <span data-ttu-id="5a47c-113">time</span><span class="sxs-lookup"><span data-stu-id="5a47c-113">time</span></span>     | <span data-ttu-id="5a47c-114">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5a47c-114">DateTimeOffset</span></span> | <span data-ttu-id="5a47c-p102">Fecha y hora en que se devolvió la respuesta. Usa el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="5a47c-p102">The date and time that the response was returned. It uses ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>

## <a name="json-representation"></a><span data-ttu-id="5a47c-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5a47c-118">JSON representation</span></span>

<span data-ttu-id="5a47c-119">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="5a47c-119">Here is a JSON representation of the resource</span></span>

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
