---
title: Tipo de recurso ChartTitle
description: Representa un objeto de título de gráfico de un gráfico.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 6cf6a2e6355fc4bc8955899dde48f9cc843e920c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27879418"
---
# <a name="charttitle-resource-type"></a><span data-ttu-id="b8257-103">Tipo de recurso ChartTitle</span><span class="sxs-lookup"><span data-stu-id="b8257-103">ChartTitle resource type</span></span>

<span data-ttu-id="b8257-104">Representa un objeto de título de gráfico de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="b8257-104">Represents a chart title object of a chart.</span></span>


## <a name="methods"></a><span data-ttu-id="b8257-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="b8257-105">Methods</span></span>

| <span data-ttu-id="b8257-106">Método</span><span class="sxs-lookup"><span data-stu-id="b8257-106">Method</span></span>           | <span data-ttu-id="b8257-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b8257-107">Return Type</span></span>    |<span data-ttu-id="b8257-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8257-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="b8257-109">Get ChartTitle</span><span class="sxs-lookup"><span data-stu-id="b8257-109">Get ChartTitle</span></span>](../api/charttitle-get.md) | [<span data-ttu-id="b8257-110">WorkbookChartTitle</span><span class="sxs-lookup"><span data-stu-id="b8257-110">WorkbookChartTitle</span></span>](charttitle.md) |<span data-ttu-id="b8257-111">Lee las propiedades y relaciones del objeto chartTitle.</span><span class="sxs-lookup"><span data-stu-id="b8257-111">Read properties and relationships of chartTitle object.</span></span>|
|[<span data-ttu-id="b8257-112">Update</span><span class="sxs-lookup"><span data-stu-id="b8257-112">Update</span></span>](../api/charttitle-update.md) | [<span data-ttu-id="b8257-113">WorkbookChartTitle</span><span class="sxs-lookup"><span data-stu-id="b8257-113">WorkbookChartTitle</span></span>](charttitle.md)    |<span data-ttu-id="b8257-114">Actualiza el objeto ChartTitle.</span><span class="sxs-lookup"><span data-stu-id="b8257-114">Update ChartTitle object.</span></span> |

## <a name="properties"></a><span data-ttu-id="b8257-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b8257-115">Properties</span></span>
| <span data-ttu-id="b8257-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b8257-116">Property</span></span>     | <span data-ttu-id="b8257-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8257-117">Type</span></span>   |<span data-ttu-id="b8257-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8257-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b8257-119">overlay</span><span class="sxs-lookup"><span data-stu-id="b8257-119">overlay</span></span>|<span data-ttu-id="b8257-120">boolean</span><span class="sxs-lookup"><span data-stu-id="b8257-120">boolean</span></span>|<span data-ttu-id="b8257-121">Valor booleano que representa si el título del gráfico se superpondrá al gráfico o no.</span><span class="sxs-lookup"><span data-stu-id="b8257-121">Boolean value representing if the chart title will overlay the chart or not.</span></span>|
|<span data-ttu-id="b8257-122">text</span><span class="sxs-lookup"><span data-stu-id="b8257-122">text</span></span>|<span data-ttu-id="b8257-123">string</span><span class="sxs-lookup"><span data-stu-id="b8257-123">string</span></span>|<span data-ttu-id="b8257-124">Representa el texto del título de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="b8257-124">Represents the title text of a chart.</span></span>|
|<span data-ttu-id="b8257-125">visible</span><span class="sxs-lookup"><span data-stu-id="b8257-125">visible</span></span>|<span data-ttu-id="b8257-126">boolean</span><span class="sxs-lookup"><span data-stu-id="b8257-126">boolean</span></span>|<span data-ttu-id="b8257-127">Valor booleano que representa la visibilidad de un objeto de título del gráfico.</span><span class="sxs-lookup"><span data-stu-id="b8257-127">A boolean value the represents the visibility of a chart title object.</span></span>|

## <a name="relationships"></a><span data-ttu-id="b8257-128">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b8257-128">Relationships</span></span>
| <span data-ttu-id="b8257-129">Relación</span><span class="sxs-lookup"><span data-stu-id="b8257-129">Relationship</span></span> | <span data-ttu-id="b8257-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8257-130">Type</span></span>   |<span data-ttu-id="b8257-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8257-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b8257-132">format</span><span class="sxs-lookup"><span data-stu-id="b8257-132">format</span></span>|[<span data-ttu-id="b8257-133">WorkbookChartTitleFormat</span><span class="sxs-lookup"><span data-stu-id="b8257-133">WorkbookChartTitleFormat</span></span>](charttitleformat.md)|<span data-ttu-id="b8257-p101">Representa el formato de un título del gráfico, que incluye el formato de relleno y de fuente. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b8257-p101">Represents the formatting of a chart title, which includes fill and font formatting. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="b8257-136">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b8257-136">JSON representation</span></span>

<span data-ttu-id="b8257-137">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b8257-137">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookChartTitle"
}-->

```json
{
  "overlay": true,
  "text": "string",
  "visible": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartTitle resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
