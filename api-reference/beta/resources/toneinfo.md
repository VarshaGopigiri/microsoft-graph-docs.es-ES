---
title: tipo de recurso toneInfo
description: Un único evento DTMF.
author: VinodRavichandran
localization_priority: Normal
ms.openlocfilehash: b9be7e0e69be8d127df92f717ab462021f9684b7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27817111"
---
# <a name="toneinfo-resource-type"></a><span data-ttu-id="99712-103">tipo de recurso toneInfo</span><span class="sxs-lookup"><span data-stu-id="99712-103">toneInfo resource type</span></span>

> <span data-ttu-id="99712-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="99712-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="99712-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="99712-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="99712-106">Un único evento DTMF.</span><span class="sxs-lookup"><span data-stu-id="99712-106">A single DTMF event.</span></span>

## <a name="properties"></a><span data-ttu-id="99712-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="99712-107">Properties</span></span>

| <span data-ttu-id="99712-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="99712-108">Property</span></span>       | <span data-ttu-id="99712-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="99712-109">Type</span></span>    | <span data-ttu-id="99712-110">Description</span><span class="sxs-lookup"><span data-stu-id="99712-110">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="99712-111">Hay</span><span class="sxs-lookup"><span data-stu-id="99712-111">sequenceId</span></span> | <span data-ttu-id="99712-112">Int64</span><span class="sxs-lookup"><span data-stu-id="99712-112">Int64</span></span> | <span data-ttu-id="99712-113">Un identificador incremental utilizado para la ordenación de eventos DTMF.</span><span class="sxs-lookup"><span data-stu-id="99712-113">An incremental identifier used for ordering DTMF events.</span></span> |
| <span data-ttu-id="99712-114">tono</span><span class="sxs-lookup"><span data-stu-id="99712-114">tone</span></span> | <span data-ttu-id="99712-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="99712-115">String</span></span> | <span data-ttu-id="99712-116">Los valores posibles son: `tone0`, `tone1`, `tone2`, `tone3`, `tone4`, `tone5`, `tone6`, `tone7`, `tone8`, `tone9`, `star`, `pound`, `a`, `b`, `c`, `d`, `flash`.</span><span class="sxs-lookup"><span data-stu-id="99712-116">Possible values are: `tone0`, `tone1`, `tone2`, `tone3`, `tone4`, `tone5`, `tone6`, `tone7`, `tone8`, `tone9`, `star`, `pound`, `a`, `b`, `c`, `d`, `flash`.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="99712-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="99712-117">JSON representation</span></span>

<span data-ttu-id="99712-118">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="99712-118">The following is a JSON representation of the resource.</span></span>

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
