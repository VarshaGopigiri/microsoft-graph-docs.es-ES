---
title: Tipo de recurso ChartPoint
description: Representa un punto de una serie de un gráfico.
author: lumine2008
ms.openlocfilehash: b2d1fab0c76100aae1a5606690772a0aa3854f42
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27316229"
---
# <a name="chartpoint-resource-type"></a><span data-ttu-id="5727a-103">Tipo de recurso ChartPoint</span><span class="sxs-lookup"><span data-stu-id="5727a-103">ChartPoint resource type</span></span>

<span data-ttu-id="5727a-104">Representa un punto de una serie de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="5727a-104">Represents a point of a series in a chart.</span></span>


## <a name="methods"></a><span data-ttu-id="5727a-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="5727a-105">Methods</span></span>

| <span data-ttu-id="5727a-106">Método</span><span class="sxs-lookup"><span data-stu-id="5727a-106">Method</span></span>           | <span data-ttu-id="5727a-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5727a-107">Return Type</span></span>    |<span data-ttu-id="5727a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="5727a-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="5727a-109">Get ChartPoint</span><span class="sxs-lookup"><span data-stu-id="5727a-109">Get ChartPoint</span></span>](../api/chartpoint-get.md) | [<span data-ttu-id="5727a-110">WorkbookChartPoint</span><span class="sxs-lookup"><span data-stu-id="5727a-110">WorkbookChartPoint</span></span>](chartpoint.md) |<span data-ttu-id="5727a-111">Lee las propiedades y relaciones del objeto chartPoint.</span><span class="sxs-lookup"><span data-stu-id="5727a-111">Read properties and relationships of chartPoint object.</span></span>|
|[<span data-ttu-id="5727a-112">List</span><span class="sxs-lookup"><span data-stu-id="5727a-112">List</span></span>](../api/chartpoint-list.md) | <span data-ttu-id="5727a-113">Colección de [WorkbookChartPoint](chartpoint.md)</span><span class="sxs-lookup"><span data-stu-id="5727a-113">[WorkbookChartPoint](chartpoint.md) collection</span></span> |<span data-ttu-id="5727a-114">Obtiene la colección de objetos chartPoint.</span><span class="sxs-lookup"><span data-stu-id="5727a-114">Get chartPoint object collection.</span></span> |
|[<span data-ttu-id="5727a-115">ItemAt</span><span class="sxs-lookup"><span data-stu-id="5727a-115">ItemAt</span></span>](../api/chartpointscollection-itemat.md)|[<span data-ttu-id="5727a-116">WorkbookChartPoint</span><span class="sxs-lookup"><span data-stu-id="5727a-116">WorkbookChartPoint</span></span>](chartpoint.md)|<span data-ttu-id="5727a-117">Recupera un punto en función de su posición dentro de la serie.</span><span class="sxs-lookup"><span data-stu-id="5727a-117">Retrieve a point based on its position within the series.</span></span>|

## <a name="properties"></a><span data-ttu-id="5727a-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5727a-118">Properties</span></span>
| <span data-ttu-id="5727a-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5727a-119">Property</span></span>     | <span data-ttu-id="5727a-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="5727a-120">Type</span></span>   |<span data-ttu-id="5727a-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="5727a-121">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5727a-122">valor</span><span class="sxs-lookup"><span data-stu-id="5727a-122">value</span></span>|<span data-ttu-id="5727a-123">Json</span><span class="sxs-lookup"><span data-stu-id="5727a-123">Json</span></span>|<span data-ttu-id="5727a-p101">Devuelve el valor de un punto del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5727a-p101">Returns the value of a chart point. Read-only.</span></span>|
|<span data-ttu-id="5727a-126">id</span><span class="sxs-lookup"><span data-stu-id="5727a-126">id</span></span>|<span data-ttu-id="5727a-127">string</span><span class="sxs-lookup"><span data-stu-id="5727a-127">string</span></span>|<span data-ttu-id="5727a-128">Identificador único</span><span class="sxs-lookup"><span data-stu-id="5727a-128">unique identifier</span></span>|

## <a name="relationships"></a><span data-ttu-id="5727a-129">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5727a-129">Relationships</span></span>
| <span data-ttu-id="5727a-130">Relación</span><span class="sxs-lookup"><span data-stu-id="5727a-130">Relationship</span></span> | <span data-ttu-id="5727a-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="5727a-131">Type</span></span>   |<span data-ttu-id="5727a-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="5727a-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5727a-133">format</span><span class="sxs-lookup"><span data-stu-id="5727a-133">format</span></span>|[<span data-ttu-id="5727a-134">WorkbookChartPointFormat</span><span class="sxs-lookup"><span data-stu-id="5727a-134">WorkbookChartPointFormat</span></span>](chartpointformat.md)|<span data-ttu-id="5727a-p102">Encapsula las propiedades de formato del punto del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5727a-p102">Encapsulates the format properties chart point. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="5727a-137">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5727a-137">JSON representation</span></span>

<span data-ttu-id="5727a-138">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5727a-138">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookChartPoint"
}-->

```json
{
  "value": "string",
  "id": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartPoint resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->