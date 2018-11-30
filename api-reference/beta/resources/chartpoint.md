---
title: Tipo de recurso ChartPoint
description: Representa un punto de una serie de un gráfico.
ms.openlocfilehash: 3d1bcc26fdc78bd7b844c870d40346a5f1f0496f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087852"
---
# <a name="chartpoint-resource-type"></a><span data-ttu-id="a1dbe-103">Tipo de recurso ChartPoint</span><span class="sxs-lookup"><span data-stu-id="a1dbe-103">ChartPoint resource type</span></span>

> <span data-ttu-id="a1dbe-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a1dbe-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a1dbe-106">Representa un punto de una serie de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-106">Represents a point of a series in a chart.</span></span>


## <a name="methods"></a><span data-ttu-id="a1dbe-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="a1dbe-107">Methods</span></span>

| <span data-ttu-id="a1dbe-108">Método</span><span class="sxs-lookup"><span data-stu-id="a1dbe-108">Method</span></span>           | <span data-ttu-id="a1dbe-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a1dbe-109">Return Type</span></span>    |<span data-ttu-id="a1dbe-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1dbe-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="a1dbe-111">Get ChartPoint</span><span class="sxs-lookup"><span data-stu-id="a1dbe-111">Get ChartPoint</span></span>](../api/chartpoint-get.md) | [<span data-ttu-id="a1dbe-112">ChartPoint</span><span class="sxs-lookup"><span data-stu-id="a1dbe-112">ChartPoint</span></span>](chartpoint.md) |<span data-ttu-id="a1dbe-113">Lee las propiedades y relaciones del objeto chartPoint.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-113">Read properties and relationships of chartPoint object.</span></span>|
|[<span data-ttu-id="a1dbe-114">List</span><span class="sxs-lookup"><span data-stu-id="a1dbe-114">List</span></span>](../api/chartpoint-list.md) | <span data-ttu-id="a1dbe-115">Colección [ChartPoint](chartpoint.md)</span><span class="sxs-lookup"><span data-stu-id="a1dbe-115">[ChartPoint](chartpoint.md) collection</span></span> |<span data-ttu-id="a1dbe-116">Obtiene la colección de objetos chartPoint.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-116">Get chartPoint object collection.</span></span> |
|[<span data-ttu-id="a1dbe-117">Itemat</span><span class="sxs-lookup"><span data-stu-id="a1dbe-117">Itemat</span></span>](../api/chartpointscollection-itemat.md)|[<span data-ttu-id="a1dbe-118">ChartPoint</span><span class="sxs-lookup"><span data-stu-id="a1dbe-118">ChartPoint</span></span>](chartpoint.md)|<span data-ttu-id="a1dbe-119">Recupera un punto en función de su posición dentro de la serie.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-119">Retrieve a point based on its position within the series.</span></span>|

## <a name="properties"></a><span data-ttu-id="a1dbe-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a1dbe-120">Properties</span></span>
| <span data-ttu-id="a1dbe-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a1dbe-121">Property</span></span>     | <span data-ttu-id="a1dbe-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="a1dbe-122">Type</span></span>   |<span data-ttu-id="a1dbe-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1dbe-123">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a1dbe-124">valor</span><span class="sxs-lookup"><span data-stu-id="a1dbe-124">value</span></span>|<span data-ttu-id="a1dbe-125">object</span><span class="sxs-lookup"><span data-stu-id="a1dbe-125">object</span></span>|<span data-ttu-id="a1dbe-p102">Devuelve el valor de un punto del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-p102">Returns the value of a chart point. Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="a1dbe-128">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a1dbe-128">Relationships</span></span>
| <span data-ttu-id="a1dbe-129">Relación</span><span class="sxs-lookup"><span data-stu-id="a1dbe-129">Relationship</span></span> | <span data-ttu-id="a1dbe-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="a1dbe-130">Type</span></span>   |<span data-ttu-id="a1dbe-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1dbe-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a1dbe-132">format</span><span class="sxs-lookup"><span data-stu-id="a1dbe-132">format</span></span>|[<span data-ttu-id="a1dbe-133">ChartPointFormat</span><span class="sxs-lookup"><span data-stu-id="a1dbe-133">ChartPointFormat</span></span>](chartpointformat.md)|<span data-ttu-id="a1dbe-p103">Encapsula las propiedades de formato del punto del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-p103">Encapsulates the format properties chart point. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="a1dbe-136">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a1dbe-136">JSON representation</span></span>

<span data-ttu-id="a1dbe-137">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-137">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chartPoint"
}-->

```json
{
  "value": "string"
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