---
title: tipo de recurso stringKeyLongValuePair
description: Representa un par de clave y valor donde la clave es una cadena y el valor es un valor Int64.
ms.openlocfilehash: 0ceafbc4ab683469e616e068c0abc00804578908
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089756"
---
# <a name="stringkeylongvaluepair-resource-type"></a><span data-ttu-id="33bb0-103">tipo de recurso stringKeyLongValuePair</span><span class="sxs-lookup"><span data-stu-id="33bb0-103">stringKeyLongValuePair resource type</span></span>

> <span data-ttu-id="33bb0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="33bb0-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="33bb0-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="33bb0-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="33bb0-106">Representa un par de clave y valor donde la clave es una cadena y el valor es un valor Int64.</span><span class="sxs-lookup"><span data-stu-id="33bb0-106">Represents a key-value pair where the key is a string and the value is an Int64.</span></span>

## <a name="properties"></a><span data-ttu-id="33bb0-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="33bb0-107">Properties</span></span>
| <span data-ttu-id="33bb0-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="33bb0-108">Property</span></span>     | <span data-ttu-id="33bb0-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="33bb0-109">Type</span></span>   |<span data-ttu-id="33bb0-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="33bb0-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="33bb0-111">Key</span><span class="sxs-lookup"><span data-stu-id="33bb0-111">key</span></span>|<span data-ttu-id="33bb0-112">String</span><span class="sxs-lookup"><span data-stu-id="33bb0-112">String</span></span>|<span data-ttu-id="33bb0-113">Clave.</span><span class="sxs-lookup"><span data-stu-id="33bb0-113">Key.</span></span>|
|<span data-ttu-id="33bb0-114">valor</span><span class="sxs-lookup"><span data-stu-id="33bb0-114">value</span></span>|<span data-ttu-id="33bb0-115">Int64</span><span class="sxs-lookup"><span data-stu-id="33bb0-115">Int64</span></span>|<span data-ttu-id="33bb0-116">Valor.</span><span class="sxs-lookup"><span data-stu-id="33bb0-116">Value.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="33bb0-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="33bb0-117">JSON representation</span></span>

<span data-ttu-id="33bb0-118">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="33bb0-118">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.stringKeyLongValuePair"
}-->

```json
{
  "key": "String",
  "value": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "stringKeyLongValuePair resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->