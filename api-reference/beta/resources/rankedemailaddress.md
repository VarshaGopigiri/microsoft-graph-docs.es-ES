---
title: tipo de recurso rankedEmailAddress
description: Representa una dirección de correo electrónico clasificados.
localization_priority: Normal
ms.openlocfilehash: bb3b906929bddcb52a57a478647000e7e16fa0be
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27818518"
---
# <a name="rankedemailaddress-resource-type"></a><span data-ttu-id="f6caa-103">tipo de recurso rankedEmailAddress</span><span class="sxs-lookup"><span data-stu-id="f6caa-103">rankedEmailAddress resource type</span></span>

> <span data-ttu-id="f6caa-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f6caa-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f6caa-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f6caa-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f6caa-106">Representa una dirección de correo electrónico clasificados.</span><span class="sxs-lookup"><span data-stu-id="f6caa-106">Represents a ranked email address.</span></span>


## <a name="properties"></a><span data-ttu-id="f6caa-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f6caa-107">Properties</span></span>
| <span data-ttu-id="f6caa-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f6caa-108">Property</span></span>     | <span data-ttu-id="f6caa-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="f6caa-109">Type</span></span>   |<span data-ttu-id="f6caa-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6caa-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f6caa-111">address</span><span class="sxs-lookup"><span data-stu-id="f6caa-111">address</span></span>|<span data-ttu-id="f6caa-112">string</span><span class="sxs-lookup"><span data-stu-id="f6caa-112">string</span></span>|<span data-ttu-id="f6caa-113">La dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f6caa-113">The email address.</span></span>|
|<span data-ttu-id="f6caa-114">rank</span><span class="sxs-lookup"><span data-stu-id="f6caa-114">rank</span></span>|<span data-ttu-id="f6caa-115">double</span><span class="sxs-lookup"><span data-stu-id="f6caa-115">double</span></span>|<span data-ttu-id="f6caa-116">La clasificación de la dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f6caa-116">The rank of the email address.</span></span> <span data-ttu-id="f6caa-117">Una clasificación se usa como criterio de ordenación, en relación con los otros resultados devueltos.</span><span class="sxs-lookup"><span data-stu-id="f6caa-117">A rank is used as a sort key, in relation to the other returned results.</span></span> <span data-ttu-id="f6caa-118">Un valor de rango más alto corresponde a un resultado más relevante.</span><span class="sxs-lookup"><span data-stu-id="f6caa-118">A higher rank value corresponds to a more relevant result.</span></span> <span data-ttu-id="f6caa-119">La relevancia viene determinada por la comunicación, colaboración y las señales de relación empresarial.</span><span class="sxs-lookup"><span data-stu-id="f6caa-119">Relevance is determined by communication, collaboration, and business relationship signals.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="f6caa-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f6caa-120">JSON representation</span></span>

<span data-ttu-id="f6caa-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f6caa-121">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.rankedEmailAddress"
}-->

```json
{
  "address": "string",
  "rank": 1024
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "rankedEmailAddress resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
