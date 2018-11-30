---
title: tipo de recurso toneInfo
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: b4ed9667c2e2156f52703c6fa15f4937ead5cef4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090441"
---
# <a name="toneinfo-resource-type"></a><span data-ttu-id="31372-103">tipo de recurso toneInfo</span><span class="sxs-lookup"><span data-stu-id="31372-103">toneInfo resource type</span></span>

> <span data-ttu-id="31372-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="31372-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="31372-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="31372-105">Use of these APIs in production applications is not supported.</span></span>

## <a name="properties"></a><span data-ttu-id="31372-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="31372-106">Properties</span></span>

| <span data-ttu-id="31372-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="31372-107">Property</span></span>       | <span data-ttu-id="31372-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="31372-108">Type</span></span>    | <span data-ttu-id="31372-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="31372-109">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="31372-110">Hay</span><span class="sxs-lookup"><span data-stu-id="31372-110">sequenceId</span></span> | <span data-ttu-id="31372-111">Int64</span><span class="sxs-lookup"><span data-stu-id="31372-111">Int64</span></span> | <span data-ttu-id="31372-112">Un identificador incremental utilizado para la ordenación de eventos DTMF.</span><span class="sxs-lookup"><span data-stu-id="31372-112">An incremental identifier used for ordering DTMF events.</span></span> |
| <span data-ttu-id="31372-113">tono</span><span class="sxs-lookup"><span data-stu-id="31372-113">tone</span></span> | <span data-ttu-id="31372-114">String</span><span class="sxs-lookup"><span data-stu-id="31372-114">String</span></span> | <span data-ttu-id="31372-115">Los valores posibles son: `tone0`, `tone1`, `tone2`, `tone3`, `tone4`, `tone5`, `tone6`, `tone7`, `tone8`, `tone9`, `star`, `pound`, `a`, `b`, `c`, `d`, `flash`.</span><span class="sxs-lookup"><span data-stu-id="31372-115">Possible values are: `tone0`, `tone1`, `tone2`, `tone3`, `tone4`, `tone5`, `tone6`, `tone7`, `tone8`, `tone9`, `star`, `pound`, `a`, `b`, `c`, `d`, `flash`.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="31372-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="31372-116">JSON representation</span></span>

<span data-ttu-id="31372-117">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="31372-117">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.toneInfo"
}-->
```json
{
  "sequenceId": 1024,
  "tone": "tone0 | tone1 | tone2 | tone3 | tone4 | tone5 | tone6 | tone7 | tone8 | tone9 | star | pound | a | b | c | d | flash"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "toneInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->