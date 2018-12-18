---
title: Tipo de recurso ChartLineFormat
description: Encapsula las opciones de formato para los elementos de línea.
author: lumine2008
ms.openlocfilehash: 1940b5dfe09c2895fbf1b8eb6bf4e5227194367c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27357305"
---
# <a name="chartlineformat-resource-type"></a><span data-ttu-id="3edda-103">Tipo de recurso ChartLineFormat</span><span class="sxs-lookup"><span data-stu-id="3edda-103">ChartLineFormat resource type</span></span>

<span data-ttu-id="3edda-104">Encapsula las opciones de formato para los elementos de línea.</span><span class="sxs-lookup"><span data-stu-id="3edda-104">Enapsulates the formatting options for line elements.</span></span>


## <a name="methods"></a><span data-ttu-id="3edda-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="3edda-105">Methods</span></span>

| <span data-ttu-id="3edda-106">Método</span><span class="sxs-lookup"><span data-stu-id="3edda-106">Method</span></span>           | <span data-ttu-id="3edda-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3edda-107">Return Type</span></span>    |<span data-ttu-id="3edda-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="3edda-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="3edda-109">Get ChartLineFormat</span><span class="sxs-lookup"><span data-stu-id="3edda-109">Get ChartLineFormat</span></span>](../api/chartlineformat-get.md) | [<span data-ttu-id="3edda-110">WorkbookChartLineFormat</span><span class="sxs-lookup"><span data-stu-id="3edda-110">WorkbookChartLineFormat</span></span>](chartlineformat.md) |<span data-ttu-id="3edda-111">Lee las propiedades y relaciones del objeto chartLineFormat.</span><span class="sxs-lookup"><span data-stu-id="3edda-111">Read properties and relationships of chartLineFormat object.</span></span>|
|[<span data-ttu-id="3edda-112">Actualizar</span><span class="sxs-lookup"><span data-stu-id="3edda-112">Update</span></span>](../api/chartlineformat-update.md) | [<span data-ttu-id="3edda-113">WorkbookChartLineFormat</span><span class="sxs-lookup"><span data-stu-id="3edda-113">WorkbookChartLineFormat</span></span>](chartlineformat.md) |<span data-ttu-id="3edda-114">Actualiza el objeto ChartLineFormat.</span><span class="sxs-lookup"><span data-stu-id="3edda-114">Update ChartLineFormat object.</span></span> |
|[<span data-ttu-id="3edda-115">Clear</span><span class="sxs-lookup"><span data-stu-id="3edda-115">Clear</span></span>](../api/chartlineformat-clear.md)|<span data-ttu-id="3edda-116">None</span><span class="sxs-lookup"><span data-stu-id="3edda-116">None</span></span>|<span data-ttu-id="3edda-117">Borra el formato de línea de un elemento de gráfico.</span><span class="sxs-lookup"><span data-stu-id="3edda-117">Clear the line format of a chart element.</span></span>|

## <a name="properties"></a><span data-ttu-id="3edda-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3edda-118">Properties</span></span>
| <span data-ttu-id="3edda-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3edda-119">Property</span></span>     | <span data-ttu-id="3edda-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="3edda-120">Type</span></span>   |<span data-ttu-id="3edda-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="3edda-121">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3edda-122">color</span><span class="sxs-lookup"><span data-stu-id="3edda-122">color</span></span>|<span data-ttu-id="3edda-123">string</span><span class="sxs-lookup"><span data-stu-id="3edda-123">string</span></span>|<span data-ttu-id="3edda-124">Código de color HTML que representa el color de las líneas del gráfico.</span><span class="sxs-lookup"><span data-stu-id="3edda-124">HTML color code representing the color of lines in the chart.</span></span>|

## <a name="relationships"></a><span data-ttu-id="3edda-125">Relaciones</span><span class="sxs-lookup"><span data-stu-id="3edda-125">Relationships</span></span>
<span data-ttu-id="3edda-126">Ninguno</span><span class="sxs-lookup"><span data-stu-id="3edda-126">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="3edda-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3edda-127">JSON representation</span></span>

<span data-ttu-id="3edda-128">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="3edda-128">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [],
  "@odata.type": "microsoft.graph.workbookChartLineFormat"
}-->

```json
{
  "color": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartLineFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->