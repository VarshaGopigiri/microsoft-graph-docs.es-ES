---
title: Tipo de recurso RangeSort
description: Administra operaciones de ordenación en objetos Range.
author: lumine2008
ms.openlocfilehash: 44aa472b218fa2c5f4f0d0db1af6f9c919283197
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27353511"
---
# <a name="rangesort-resource-type"></a><span data-ttu-id="400ab-103">Tipo de recurso RangeSort</span><span class="sxs-lookup"><span data-stu-id="400ab-103">RangeSort resource type</span></span>

<span data-ttu-id="400ab-104">Administra operaciones de ordenación en objetos Range.</span><span class="sxs-lookup"><span data-stu-id="400ab-104">Manages sorting operations on Range objects.</span></span>


## <a name="methods"></a><span data-ttu-id="400ab-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="400ab-105">Methods</span></span>

| <span data-ttu-id="400ab-106">Método</span><span class="sxs-lookup"><span data-stu-id="400ab-106">Method</span></span>           | <span data-ttu-id="400ab-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="400ab-107">Return Type</span></span>    |<span data-ttu-id="400ab-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="400ab-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="400ab-109">Apply</span><span class="sxs-lookup"><span data-stu-id="400ab-109">Apply</span></span>](../api/rangesort-apply.md)|<span data-ttu-id="400ab-110">None</span><span class="sxs-lookup"><span data-stu-id="400ab-110">None</span></span>|<span data-ttu-id="400ab-111">Realiza una operación de ordenación.</span><span class="sxs-lookup"><span data-stu-id="400ab-111">Perform a sort operation.</span></span>|

## <a name="properties"></a><span data-ttu-id="400ab-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="400ab-112">Properties</span></span>
<span data-ttu-id="400ab-113">Ninguno</span><span class="sxs-lookup"><span data-stu-id="400ab-113">None</span></span>

## <a name="relationships"></a><span data-ttu-id="400ab-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="400ab-114">Relationships</span></span>
<span data-ttu-id="400ab-115">Ninguno</span><span class="sxs-lookup"><span data-stu-id="400ab-115">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="400ab-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="400ab-116">JSON representation</span></span>

<span data-ttu-id="400ab-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="400ab-117">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookRangeSort"
}-->

```json
{
}
```

##### <a name="request"></a><span data-ttu-id="400ab-118">Solicitud</span><span class="sxs-lookup"><span data-stu-id="400ab-118">Request</span></span>
<span data-ttu-id="400ab-119">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="400ab-119">Here is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "name": "range_sort"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/sort
```

##### <a name="response"></a><span data-ttu-id="400ab-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="400ab-120">Response</span></span>
<span data-ttu-id="400ab-121">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="400ab-121">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRangeSort"
} -->
```http
HTTP/1.1 200 OK
Content-Type: application/json

{
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "RangeSort resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->