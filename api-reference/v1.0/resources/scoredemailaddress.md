---
title: Tipo de recurso scoredEmailAddress
description: Representa una dirección de correo electrónico con puntuación.
ms.openlocfilehash: 9cdd33a6df9eefca0f7a00c5fe8b17832e0056d9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032670"
---
# <a name="scoredemailaddress-resource-type"></a><span data-ttu-id="3771c-103">Tipo de recurso scoredEmailAddress</span><span class="sxs-lookup"><span data-stu-id="3771c-103">scoredEmailAddress resource type</span></span>

<span data-ttu-id="3771c-104">Representa una dirección de correo electrónico con puntuación.</span><span class="sxs-lookup"><span data-stu-id="3771c-104">Represents a scored email address.</span></span>


## <a name="properties"></a><span data-ttu-id="3771c-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3771c-105">Properties</span></span>
| <span data-ttu-id="3771c-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3771c-106">Property</span></span>     | <span data-ttu-id="3771c-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="3771c-107">Type</span></span>   |<span data-ttu-id="3771c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="3771c-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3771c-109">address</span><span class="sxs-lookup"><span data-stu-id="3771c-109">address</span></span>|<span data-ttu-id="3771c-110">string</span><span class="sxs-lookup"><span data-stu-id="3771c-110">string</span></span>|<span data-ttu-id="3771c-111">La dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="3771c-111">The email address.</span></span>|
|<span data-ttu-id="3771c-112">relevanceScore</span><span class="sxs-lookup"><span data-stu-id="3771c-112">relevanceScore</span></span>|<span data-ttu-id="3771c-113">double</span><span class="sxs-lookup"><span data-stu-id="3771c-113">double</span></span>|<span data-ttu-id="3771c-p101">La puntuación de relevancia de la dirección de correo electrónico. Una puntuación de relevancia se usa como criterio de ordenación con respecto a los demás resultados devueltos. Un valor de puntuación de relevancia más alto corresponde a un resultado más relevante. La relevancia viene determinada por las relaciones empresariales y los patrones de comunicación y colaboración del usuario.</span><span class="sxs-lookup"><span data-stu-id="3771c-p101">The relevance score of the email address. A relevance score is used as a sort key, in relation to the other returned results. A higher relevance score value corresponds to a more relevant result. Relevance is determined by the user’s communication and collaboration patterns and business relationships.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="3771c-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3771c-118">JSON representation</span></span>

<span data-ttu-id="3771c-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="3771c-119">Here is a JSON representation of the resource.</span></span>

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
