---
title: Tipo de recurso RangeSort
description: Administra operaciones de ordenación en objetos Range.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: c52b4c6cc50bce7d518d26798db9f3d3da49cd1c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27816432"
---
# <a name="rangesort-resource-type"></a><span data-ttu-id="81485-103">Tipo de recurso RangeSort</span><span class="sxs-lookup"><span data-stu-id="81485-103">RangeSort resource type</span></span>

<span data-ttu-id="81485-104">Administra operaciones de ordenación en objetos Range.</span><span class="sxs-lookup"><span data-stu-id="81485-104">Manages sorting operations on Range objects.</span></span>


## <a name="methods"></a><span data-ttu-id="81485-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="81485-105">Methods</span></span>

| <span data-ttu-id="81485-106">Método</span><span class="sxs-lookup"><span data-stu-id="81485-106">Method</span></span>           | <span data-ttu-id="81485-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81485-107">Return Type</span></span>    |<span data-ttu-id="81485-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="81485-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="81485-109">Apply</span><span class="sxs-lookup"><span data-stu-id="81485-109">Apply</span></span>](../api/rangesort-apply.md)|<span data-ttu-id="81485-110">None</span><span class="sxs-lookup"><span data-stu-id="81485-110">None</span></span>|<span data-ttu-id="81485-111">Realiza una operación de ordenación.</span><span class="sxs-lookup"><span data-stu-id="81485-111">Perform a sort operation.</span></span>|

## <a name="properties"></a><span data-ttu-id="81485-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="81485-112">Properties</span></span>
<span data-ttu-id="81485-113">Ninguno</span><span class="sxs-lookup"><span data-stu-id="81485-113">None</span></span>

## <a name="relationships"></a><span data-ttu-id="81485-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="81485-114">Relationships</span></span>
<span data-ttu-id="81485-115">Ninguno</span><span class="sxs-lookup"><span data-stu-id="81485-115">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="81485-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="81485-116">JSON representation</span></span>

<span data-ttu-id="81485-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="81485-117">Here is a JSON representation of the resource.</span></span>

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

##### <a name="request"></a><span data-ttu-id="81485-118">Solicitud</span><span class="sxs-lookup"><span data-stu-id="81485-118">Request</span></span>
<span data-ttu-id="81485-119">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="81485-119">Here is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "name": "range_sort"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/sort
```

##### <a name="response"></a><span data-ttu-id="81485-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="81485-120">Response</span></span>
<span data-ttu-id="81485-121">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="81485-121">Here is an example of the response.</span></span> 
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
