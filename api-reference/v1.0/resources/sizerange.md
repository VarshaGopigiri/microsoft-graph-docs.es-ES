---
title: Tipo de recurso sizeRange
description: Especifica los tamaños máximo y mínimo (en kilobytes) que un mensaje entrante debe tener para que una condición o excepción se aplique.
localization_priority: Normal
ms.openlocfilehash: ae754d0666185023272860864ef17f038aecff7c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27873546"
---
# <a name="sizerange-resource-type"></a><span data-ttu-id="1588c-103">Tipo de recurso sizeRange</span><span class="sxs-lookup"><span data-stu-id="1588c-103">sizeRange resource type</span></span>


<span data-ttu-id="1588c-104">Especifica los tamaños máximo y mínimo (en kilobytes) que un mensaje entrante debe tener para que una condición o excepción se aplique.</span><span class="sxs-lookup"><span data-stu-id="1588c-104">Specifies the maximum and minimum sizes (in kilobytes) that an incoming message must have in order for a condition or exception to apply.</span></span>

## <a name="properties"></a><span data-ttu-id="1588c-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1588c-105">Properties</span></span>
| <span data-ttu-id="1588c-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1588c-106">Property</span></span>     | <span data-ttu-id="1588c-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="1588c-107">Type</span></span>   |<span data-ttu-id="1588c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="1588c-108">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="1588c-109">maximumSize</span><span class="sxs-lookup"><span data-stu-id="1588c-109">maximumSize</span></span> | <span data-ttu-id="1588c-110">Int32</span><span class="sxs-lookup"><span data-stu-id="1588c-110">Int32</span></span> | <span data-ttu-id="1588c-111">Tamaño máximo (en kilobytes) que un mensaje entrante debe tener para que una condición o excepción se aplique.</span><span class="sxs-lookup"><span data-stu-id="1588c-111">The maximum size (in kilobytes) that an incoming message must have in order for a condition or exception to apply.</span></span> |
| <span data-ttu-id="1588c-112">minimumSize</span><span class="sxs-lookup"><span data-stu-id="1588c-112">minimumSize</span></span> | <span data-ttu-id="1588c-113">Int32</span><span class="sxs-lookup"><span data-stu-id="1588c-113">Int32</span></span> | <span data-ttu-id="1588c-114">Tamaño mínimo (en kilobytes) que un mensaje entrante debe tener para que una condición o excepción se aplique.</span><span class="sxs-lookup"><span data-stu-id="1588c-114">The minimum size (in kilobytes) that an incoming message must have in order for a condition or exception to apply.</span></span> |


## <a name="json-representation"></a><span data-ttu-id="1588c-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1588c-115">JSON representation</span></span>
<span data-ttu-id="1588c-116">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="1588c-116">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
   ],
  "@odata.type": "microsoft.graph.sizeRange"
}-->

```json
{
  "maximumSize": "Int32",
  "minimumSize": "Int32"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "sizeRange resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
