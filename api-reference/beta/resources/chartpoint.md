---
title: Tipo de recurso ChartPoint
description: Representa un punto de una serie de un gráfico.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 66c58e08063bd9757ad9c174e81f35328dd2722b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27912760"
---
# <a name="chartpoint-resource-type"></a><span data-ttu-id="b9fc5-103">Tipo de recurso ChartPoint</span><span class="sxs-lookup"><span data-stu-id="b9fc5-103">ChartPoint resource type</span></span>

> <span data-ttu-id="b9fc5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b9fc5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b9fc5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b9fc5-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b9fc5-106">Representa un punto de una serie de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="b9fc5-106">Represents a point of a series in a chart.</span></span>


## <a name="methods"></a><span data-ttu-id="b9fc5-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="b9fc5-107">Methods</span></span>

| <span data-ttu-id="b9fc5-108">Método</span><span class="sxs-lookup"><span data-stu-id="b9fc5-108">Method</span></span>           | <span data-ttu-id="b9fc5-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b9fc5-109">Return Type</span></span>    |<span data-ttu-id="b9fc5-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9fc5-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="b9fc5-111">Get ChartPoint</span><span class="sxs-lookup"><span data-stu-id="b9fc5-111">Get ChartPoint</span></span>](../api/chartpoint-get.md) | [<span data-ttu-id="b9fc5-112">ChartPoint</span><span class="sxs-lookup"><span data-stu-id="b9fc5-112">ChartPoint</span></span>](chartpoint.md) |<span data-ttu-id="b9fc5-113">Lee las propiedades y relaciones del objeto chartPoint.</span><span class="sxs-lookup"><span data-stu-id="b9fc5-113">Read properties and relationships of chartPoint object.</span></span>|
|[<span data-ttu-id="b9fc5-114">List</span><span class="sxs-lookup"><span data-stu-id="b9fc5-114">List</span></span>](../api/chartpoint-list.md) | <span data-ttu-id="b9fc5-115">Colección [ChartPoint](chartpoint.md)</span><span class="sxs-lookup"><span data-stu-id="b9fc5-115">[ChartPoint](chartpoint.md) collection</span></span> |<span data-ttu-id="b9fc5-116">Obtiene la colección de objetos chartPoint.</span><span class="sxs-lookup"><span data-stu-id="b9fc5-116">Get chartPoint object collection.</span></span> |
|[<span data-ttu-id="b9fc5-117">Itemat</span><span class="sxs-lookup"><span data-stu-id="b9fc5-117">Itemat</span></span>](../api/chartpointscollection-itemat.md)|[<span data-ttu-id="b9fc5-118">ChartPoint</span><span class="sxs-lookup"><span data-stu-id="b9fc5-118">ChartPoint</span></span>](chartpoint.md)|<span data-ttu-id="b9fc5-119">Recupera un punto en función de su posición dentro de la serie.</span><span class="sxs-lookup"><span data-stu-id="b9fc5-119">Retrieve a point based on its position within the series.</span></span>|

## <a name="properties"></a><span data-ttu-id="b9fc5-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b9fc5-120">Properties</span></span>
| <span data-ttu-id="b9fc5-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b9fc5-121">Property</span></span>     | <span data-ttu-id="b9fc5-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="b9fc5-122">Type</span></span>   |<span data-ttu-id="b9fc5-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9fc5-123">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b9fc5-124">valor</span><span class="sxs-lookup"><span data-stu-id="b9fc5-124">value</span></span>|<span data-ttu-id="b9fc5-125">object</span><span class="sxs-lookup"><span data-stu-id="b9fc5-125">object</span></span>|<span data-ttu-id="b9fc5-p102">Devuelve el valor de un punto del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b9fc5-p102">Returns the value of a chart point. Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="b9fc5-128">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b9fc5-128">Relationships</span></span>
| <span data-ttu-id="b9fc5-129">Relación</span><span class="sxs-lookup"><span data-stu-id="b9fc5-129">Relationship</span></span> | <span data-ttu-id="b9fc5-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="b9fc5-130">Type</span></span>   |<span data-ttu-id="b9fc5-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9fc5-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b9fc5-132">format</span><span class="sxs-lookup"><span data-stu-id="b9fc5-132">format</span></span>|[<span data-ttu-id="b9fc5-133">ChartPointFormat</span><span class="sxs-lookup"><span data-stu-id="b9fc5-133">ChartPointFormat</span></span>](chartpointformat.md)|<span data-ttu-id="b9fc5-p103">Encapsula las propiedades de formato del punto del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b9fc5-p103">Encapsulates the format properties chart point. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="b9fc5-136">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b9fc5-136">JSON representation</span></span>

<span data-ttu-id="b9fc5-137">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b9fc5-137">Here is a JSON representation of the resource.</span></span>

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
