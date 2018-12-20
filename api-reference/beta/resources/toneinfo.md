---
title: tipo de recurso toneInfo
description: Un único evento DTMF.
author: VinodRavichandran
ms.openlocfilehash: 0ae78a9a4721c88767ebc460a99c7cdea30f44c5
ms.sourcegitcommit: 0b3a57ac8b99871e56389f9be15e4f96e219f635
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2018
ms.locfileid: "27380341"
---
# <a name="toneinfo-resource-type"></a><span data-ttu-id="56618-103">tipo de recurso toneInfo</span><span class="sxs-lookup"><span data-stu-id="56618-103">toneInfo resource type</span></span>

> <span data-ttu-id="56618-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="56618-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="56618-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="56618-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="56618-106">Un único evento DTMF.</span><span class="sxs-lookup"><span data-stu-id="56618-106">A single DTMF event.</span></span>

## <a name="properties"></a><span data-ttu-id="56618-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="56618-107">Properties</span></span>

| <span data-ttu-id="56618-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="56618-108">Property</span></span>       | <span data-ttu-id="56618-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="56618-109">Type</span></span>    | <span data-ttu-id="56618-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="56618-110">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="56618-111">Hay</span><span class="sxs-lookup"><span data-stu-id="56618-111">sequenceId</span></span> | <span data-ttu-id="56618-112">Int64</span><span class="sxs-lookup"><span data-stu-id="56618-112">Int64</span></span> | <span data-ttu-id="56618-113">Un identificador incremental utilizado para la ordenación de eventos DTMF.</span><span class="sxs-lookup"><span data-stu-id="56618-113">An incremental identifier used for ordering DTMF events.</span></span> |
| <span data-ttu-id="56618-114">tono</span><span class="sxs-lookup"><span data-stu-id="56618-114">tone</span></span> | <span data-ttu-id="56618-115">String</span><span class="sxs-lookup"><span data-stu-id="56618-115">String</span></span> | <span data-ttu-id="56618-116">Los valores posibles son: `tone0`, `tone1`, `tone2`, `tone3`, `tone4`, `tone5`, `tone6`, `tone7`, `tone8`, `tone9`, `star`, `pound`, `a`, `b`, `c`, `d`, `flash`.</span><span class="sxs-lookup"><span data-stu-id="56618-116">Possible values are: `tone0`, `tone1`, `tone2`, `tone3`, `tone4`, `tone5`, `tone6`, `tone7`, `tone8`, `tone9`, `star`, `pound`, `a`, `b`, `c`, `d`, `flash`.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="56618-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="56618-117">JSON representation</span></span>

<span data-ttu-id="56618-118">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="56618-118">The following is a JSON representation of the resource.</span></span>

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