---
title: Tipo de recurso ChartPoint
description: Representa un punto de una serie de un gráfico.
author: lumine2008
ms.openlocfilehash: f27017d5e6cc111fa759fc6c9728ed182e7fa624
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27358411"
---
# <a name="chartpoint-resource-type"></a><span data-ttu-id="d0d27-103">Tipo de recurso ChartPoint</span><span class="sxs-lookup"><span data-stu-id="d0d27-103">ChartPoint resource type</span></span>

> <span data-ttu-id="d0d27-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d0d27-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d0d27-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d0d27-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d0d27-106">Representa un punto de una serie de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="d0d27-106">Represents a point of a series in a chart.</span></span>


## <a name="methods"></a><span data-ttu-id="d0d27-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="d0d27-107">Methods</span></span>

| <span data-ttu-id="d0d27-108">Método</span><span class="sxs-lookup"><span data-stu-id="d0d27-108">Method</span></span>           | <span data-ttu-id="d0d27-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0d27-109">Return Type</span></span>    |<span data-ttu-id="d0d27-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0d27-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="d0d27-111">Get ChartPoint</span><span class="sxs-lookup"><span data-stu-id="d0d27-111">Get ChartPoint</span></span>](../api/chartpoint-get.md) | [<span data-ttu-id="d0d27-112">ChartPoint</span><span class="sxs-lookup"><span data-stu-id="d0d27-112">ChartPoint</span></span>](chartpoint.md) |<span data-ttu-id="d0d27-113">Lee las propiedades y relaciones del objeto chartPoint.</span><span class="sxs-lookup"><span data-stu-id="d0d27-113">Read properties and relationships of chartPoint object.</span></span>|
|[<span data-ttu-id="d0d27-114">List</span><span class="sxs-lookup"><span data-stu-id="d0d27-114">List</span></span>](../api/chartpoint-list.md) | <span data-ttu-id="d0d27-115">Colección [ChartPoint](chartpoint.md)</span><span class="sxs-lookup"><span data-stu-id="d0d27-115">[ChartPoint](chartpoint.md) collection</span></span> |<span data-ttu-id="d0d27-116">Obtiene la colección de objetos chartPoint.</span><span class="sxs-lookup"><span data-stu-id="d0d27-116">Get chartPoint object collection.</span></span> |
|[<span data-ttu-id="d0d27-117">Itemat</span><span class="sxs-lookup"><span data-stu-id="d0d27-117">Itemat</span></span>](../api/chartpointscollection-itemat.md)|[<span data-ttu-id="d0d27-118">ChartPoint</span><span class="sxs-lookup"><span data-stu-id="d0d27-118">ChartPoint</span></span>](chartpoint.md)|<span data-ttu-id="d0d27-119">Recupera un punto en función de su posición dentro de la serie.</span><span class="sxs-lookup"><span data-stu-id="d0d27-119">Retrieve a point based on its position within the series.</span></span>|

## <a name="properties"></a><span data-ttu-id="d0d27-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d0d27-120">Properties</span></span>
| <span data-ttu-id="d0d27-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d0d27-121">Property</span></span>     | <span data-ttu-id="d0d27-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="d0d27-122">Type</span></span>   |<span data-ttu-id="d0d27-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0d27-123">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d0d27-124">valor</span><span class="sxs-lookup"><span data-stu-id="d0d27-124">value</span></span>|<span data-ttu-id="d0d27-125">object</span><span class="sxs-lookup"><span data-stu-id="d0d27-125">object</span></span>|<span data-ttu-id="d0d27-p102">Devuelve el valor de un punto del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d0d27-p102">Returns the value of a chart point. Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="d0d27-128">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d0d27-128">Relationships</span></span>
| <span data-ttu-id="d0d27-129">Relación</span><span class="sxs-lookup"><span data-stu-id="d0d27-129">Relationship</span></span> | <span data-ttu-id="d0d27-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="d0d27-130">Type</span></span>   |<span data-ttu-id="d0d27-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0d27-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d0d27-132">format</span><span class="sxs-lookup"><span data-stu-id="d0d27-132">format</span></span>|[<span data-ttu-id="d0d27-133">ChartPointFormat</span><span class="sxs-lookup"><span data-stu-id="d0d27-133">ChartPointFormat</span></span>](chartpointformat.md)|<span data-ttu-id="d0d27-p103">Encapsula las propiedades de formato del punto del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d0d27-p103">Encapsulates the format properties chart point. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="d0d27-136">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d0d27-136">JSON representation</span></span>

<span data-ttu-id="d0d27-137">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d0d27-137">Here is a JSON representation of the resource.</span></span>

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