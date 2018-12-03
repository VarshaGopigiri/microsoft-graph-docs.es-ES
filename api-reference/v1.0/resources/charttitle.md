---
title: Tipo de recurso ChartTitle
description: Representa un objeto de título de gráfico de un gráfico.
ms.openlocfilehash: 44777d939e67d2e8b5563cf3edb0b5bfddeeef9a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029595"
---
# <a name="charttitle-resource-type"></a><span data-ttu-id="c865c-103">Tipo de recurso ChartTitle</span><span class="sxs-lookup"><span data-stu-id="c865c-103">ChartTitle resource type</span></span>

<span data-ttu-id="c865c-104">Representa un objeto de título de gráfico de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="c865c-104">Represents a chart title object of a chart.</span></span>


## <a name="methods"></a><span data-ttu-id="c865c-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="c865c-105">Methods</span></span>

| <span data-ttu-id="c865c-106">Método</span><span class="sxs-lookup"><span data-stu-id="c865c-106">Method</span></span>           | <span data-ttu-id="c865c-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c865c-107">Return Type</span></span>    |<span data-ttu-id="c865c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="c865c-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="c865c-109">Get ChartTitle</span><span class="sxs-lookup"><span data-stu-id="c865c-109">Get ChartTitle</span></span>](../api/charttitle-get.md) | [<span data-ttu-id="c865c-110">WorkbookChartTitle</span><span class="sxs-lookup"><span data-stu-id="c865c-110">WorkbookChartTitle</span></span>](charttitle.md) |<span data-ttu-id="c865c-111">Lee las propiedades y relaciones del objeto chartTitle.</span><span class="sxs-lookup"><span data-stu-id="c865c-111">Read properties and relationships of chartTitle object.</span></span>|
|[<span data-ttu-id="c865c-112">Update</span><span class="sxs-lookup"><span data-stu-id="c865c-112">Update</span></span>](../api/charttitle-update.md) | [<span data-ttu-id="c865c-113">WorkbookChartTitle</span><span class="sxs-lookup"><span data-stu-id="c865c-113">WorkbookChartTitle</span></span>](charttitle.md)    |<span data-ttu-id="c865c-114">Actualiza el objeto ChartTitle.</span><span class="sxs-lookup"><span data-stu-id="c865c-114">Update ChartTitle object.</span></span> |

## <a name="properties"></a><span data-ttu-id="c865c-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c865c-115">Properties</span></span>
| <span data-ttu-id="c865c-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c865c-116">Property</span></span>     | <span data-ttu-id="c865c-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="c865c-117">Type</span></span>   |<span data-ttu-id="c865c-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="c865c-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c865c-119">overlay</span><span class="sxs-lookup"><span data-stu-id="c865c-119">overlay</span></span>|<span data-ttu-id="c865c-120">boolean</span><span class="sxs-lookup"><span data-stu-id="c865c-120">boolean</span></span>|<span data-ttu-id="c865c-121">Valor booleano que representa si el título del gráfico se superpondrá al gráfico o no.</span><span class="sxs-lookup"><span data-stu-id="c865c-121">Boolean value representing if the chart title will overlay the chart or not.</span></span>|
|<span data-ttu-id="c865c-122">text</span><span class="sxs-lookup"><span data-stu-id="c865c-122">text</span></span>|<span data-ttu-id="c865c-123">string</span><span class="sxs-lookup"><span data-stu-id="c865c-123">string</span></span>|<span data-ttu-id="c865c-124">Representa el texto del título de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="c865c-124">Represents the title text of a chart.</span></span>|
|<span data-ttu-id="c865c-125">visible</span><span class="sxs-lookup"><span data-stu-id="c865c-125">visible</span></span>|<span data-ttu-id="c865c-126">boolean</span><span class="sxs-lookup"><span data-stu-id="c865c-126">boolean</span></span>|<span data-ttu-id="c865c-127">Valor booleano que representa la visibilidad de un objeto de título del gráfico.</span><span class="sxs-lookup"><span data-stu-id="c865c-127">A boolean value the represents the visibility of a chart title object.</span></span>|

## <a name="relationships"></a><span data-ttu-id="c865c-128">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c865c-128">Relationships</span></span>
| <span data-ttu-id="c865c-129">Relación</span><span class="sxs-lookup"><span data-stu-id="c865c-129">Relationship</span></span> | <span data-ttu-id="c865c-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="c865c-130">Type</span></span>   |<span data-ttu-id="c865c-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="c865c-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c865c-132">format</span><span class="sxs-lookup"><span data-stu-id="c865c-132">format</span></span>|[<span data-ttu-id="c865c-133">WorkbookChartTitleFormat</span><span class="sxs-lookup"><span data-stu-id="c865c-133">WorkbookChartTitleFormat</span></span>](charttitleformat.md)|<span data-ttu-id="c865c-p101">Representa el formato de un título del gráfico, que incluye el formato de relleno y de fuente. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c865c-p101">Represents the formatting of a chart title, which includes fill and font formatting. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="c865c-136">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c865c-136">JSON representation</span></span>

<span data-ttu-id="c865c-137">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c865c-137">Here is a JSON representation of the resource.</span></span>

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