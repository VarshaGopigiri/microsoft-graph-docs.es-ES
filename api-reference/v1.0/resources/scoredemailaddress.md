---
title: Tipo de recurso scoredEmailAddress
description: Representa una dirección de correo electrónico con puntuación.
localization_priority: Normal
ms.openlocfilehash: 740173e7d5f93dc875c08508bf73100727fdf415
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27819477"
---
# <a name="scoredemailaddress-resource-type"></a><span data-ttu-id="96c85-103">Tipo de recurso scoredEmailAddress</span><span class="sxs-lookup"><span data-stu-id="96c85-103">scoredEmailAddress resource type</span></span>

<span data-ttu-id="96c85-104">Representa una dirección de correo electrónico con puntuación.</span><span class="sxs-lookup"><span data-stu-id="96c85-104">Represents a scored email address.</span></span>


## <a name="properties"></a><span data-ttu-id="96c85-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="96c85-105">Properties</span></span>
| <span data-ttu-id="96c85-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="96c85-106">Property</span></span>     | <span data-ttu-id="96c85-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="96c85-107">Type</span></span>   |<span data-ttu-id="96c85-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="96c85-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="96c85-109">address</span><span class="sxs-lookup"><span data-stu-id="96c85-109">address</span></span>|<span data-ttu-id="96c85-110">string</span><span class="sxs-lookup"><span data-stu-id="96c85-110">string</span></span>|<span data-ttu-id="96c85-111">La dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="96c85-111">The email address.</span></span>|
|<span data-ttu-id="96c85-112">relevanceScore</span><span class="sxs-lookup"><span data-stu-id="96c85-112">relevanceScore</span></span>|<span data-ttu-id="96c85-113">double</span><span class="sxs-lookup"><span data-stu-id="96c85-113">double</span></span>|<span data-ttu-id="96c85-p101">La puntuación de relevancia de la dirección de correo electrónico. Una puntuación de relevancia se usa como criterio de ordenación con respecto a los demás resultados devueltos. Un valor de puntuación de relevancia más alto corresponde a un resultado más relevante. La relevancia viene determinada por las relaciones empresariales y los patrones de comunicación y colaboración del usuario.</span><span class="sxs-lookup"><span data-stu-id="96c85-p101">The relevance score of the email address. A relevance score is used as a sort key, in relation to the other returned results. A higher relevance score value corresponds to a more relevant result. Relevance is determined by the user’s communication and collaboration patterns and business relationships.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="96c85-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="96c85-118">JSON representation</span></span>

<span data-ttu-id="96c85-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="96c85-119">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.scoredEmailAddress"
}-->

```json
{
  "address": "string",
  "relevanceScore": 1024.0
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "scoredEmailAddress resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
