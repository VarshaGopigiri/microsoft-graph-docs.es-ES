---
title: Tipo de recurso ChartPoint
description: Representa un punto de una serie de un gráfico.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 3318415094a36100851b1c604cba2507de31f558
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27962509"
---
# <a name="chartpoint-resource-type"></a><span data-ttu-id="200df-103">Tipo de recurso ChartPoint</span><span class="sxs-lookup"><span data-stu-id="200df-103">ChartPoint resource type</span></span>

<span data-ttu-id="200df-104">Representa un punto de una serie de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="200df-104">Represents a point of a series in a chart.</span></span>


## <a name="methods"></a><span data-ttu-id="200df-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="200df-105">Methods</span></span>

| <span data-ttu-id="200df-106">Método</span><span class="sxs-lookup"><span data-stu-id="200df-106">Method</span></span>           | <span data-ttu-id="200df-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="200df-107">Return Type</span></span>    |<span data-ttu-id="200df-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="200df-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="200df-109">Get ChartPoint</span><span class="sxs-lookup"><span data-stu-id="200df-109">Get ChartPoint</span></span>](../api/chartpoint-get.md) | [<span data-ttu-id="200df-110">WorkbookChartPoint</span><span class="sxs-lookup"><span data-stu-id="200df-110">WorkbookChartPoint</span></span>](chartpoint.md) |<span data-ttu-id="200df-111">Lee las propiedades y relaciones del objeto chartPoint.</span><span class="sxs-lookup"><span data-stu-id="200df-111">Read properties and relationships of chartPoint object.</span></span>|
|[<span data-ttu-id="200df-112">List</span><span class="sxs-lookup"><span data-stu-id="200df-112">List</span></span>](../api/chartpoint-list.md) | <span data-ttu-id="200df-113">Colección de [WorkbookChartPoint](chartpoint.md)</span><span class="sxs-lookup"><span data-stu-id="200df-113">[WorkbookChartPoint](chartpoint.md) collection</span></span> |<span data-ttu-id="200df-114">Obtiene la colección de objetos chartPoint.</span><span class="sxs-lookup"><span data-stu-id="200df-114">Get chartPoint object collection.</span></span> |
|[<span data-ttu-id="200df-115">ItemAt</span><span class="sxs-lookup"><span data-stu-id="200df-115">ItemAt</span></span>](../api/chartpointscollection-itemat.md)|[<span data-ttu-id="200df-116">WorkbookChartPoint</span><span class="sxs-lookup"><span data-stu-id="200df-116">WorkbookChartPoint</span></span>](chartpoint.md)|<span data-ttu-id="200df-117">Recupera un punto en función de su posición dentro de la serie.</span><span class="sxs-lookup"><span data-stu-id="200df-117">Retrieve a point based on its position within the series.</span></span>|

## <a name="properties"></a><span data-ttu-id="200df-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="200df-118">Properties</span></span>
| <span data-ttu-id="200df-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="200df-119">Property</span></span>     | <span data-ttu-id="200df-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="200df-120">Type</span></span>   |<span data-ttu-id="200df-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="200df-121">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="200df-122">valor</span><span class="sxs-lookup"><span data-stu-id="200df-122">value</span></span>|<span data-ttu-id="200df-123">Json</span><span class="sxs-lookup"><span data-stu-id="200df-123">Json</span></span>|<span data-ttu-id="200df-p101">Devuelve el valor de un punto del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="200df-p101">Returns the value of a chart point. Read-only.</span></span>|
|<span data-ttu-id="200df-126">id</span><span class="sxs-lookup"><span data-stu-id="200df-126">id</span></span>|<span data-ttu-id="200df-127">string</span><span class="sxs-lookup"><span data-stu-id="200df-127">string</span></span>|<span data-ttu-id="200df-128">Identificador único</span><span class="sxs-lookup"><span data-stu-id="200df-128">unique identifier</span></span>|

## <a name="relationships"></a><span data-ttu-id="200df-129">Relaciones</span><span class="sxs-lookup"><span data-stu-id="200df-129">Relationships</span></span>
| <span data-ttu-id="200df-130">Relación</span><span class="sxs-lookup"><span data-stu-id="200df-130">Relationship</span></span> | <span data-ttu-id="200df-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="200df-131">Type</span></span>   |<span data-ttu-id="200df-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="200df-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="200df-133">format</span><span class="sxs-lookup"><span data-stu-id="200df-133">format</span></span>|[<span data-ttu-id="200df-134">WorkbookChartPointFormat</span><span class="sxs-lookup"><span data-stu-id="200df-134">WorkbookChartPointFormat</span></span>](chartpointformat.md)|<span data-ttu-id="200df-p102">Encapsula las propiedades de formato del punto del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="200df-p102">Encapsulates the format properties chart point. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="200df-137">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="200df-137">JSON representation</span></span>

<span data-ttu-id="200df-138">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="200df-138">Here is a JSON representation of the resource.</span></span>

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
