---
title: Tipo de recurso ChartAxisTitle
description: Representa el título del eje de un gráfico.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: b1d212fd2fa55a01971c5d58026fcbe56f1c5116
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27822011"
---
# <a name="chartaxistitle-resource-type"></a><span data-ttu-id="388be-103">Tipo de recurso ChartAxisTitle</span><span class="sxs-lookup"><span data-stu-id="388be-103">ChartAxisTitle resource type</span></span>

<span data-ttu-id="388be-104">Representa el título del eje de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="388be-104">Represents the title of a chart axis.</span></span>


## <a name="methods"></a><span data-ttu-id="388be-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="388be-105">Methods</span></span>

| <span data-ttu-id="388be-106">Método</span><span class="sxs-lookup"><span data-stu-id="388be-106">Method</span></span>           | <span data-ttu-id="388be-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="388be-107">Return Type</span></span>    |<span data-ttu-id="388be-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="388be-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="388be-109">Get ChartAxisTitle</span><span class="sxs-lookup"><span data-stu-id="388be-109">Get ChartAxisTitle</span></span>](../api/chartaxistitle-get.md) | [<span data-ttu-id="388be-110">WorkbookChartAxisTitle</span><span class="sxs-lookup"><span data-stu-id="388be-110">WorkbookChartAxisTitle</span></span>](chartaxistitle.md) |<span data-ttu-id="388be-111">Lee las propiedades y relaciones del objeto chartAxisTitle.</span><span class="sxs-lookup"><span data-stu-id="388be-111">Read properties and relationships of chartAxisTitle object.</span></span>|
|[<span data-ttu-id="388be-112">Update</span><span class="sxs-lookup"><span data-stu-id="388be-112">Update</span></span>](../api/chartaxistitle-update.md) | [<span data-ttu-id="388be-113">WorkbookChartAxisTitle</span><span class="sxs-lookup"><span data-stu-id="388be-113">WorkbookChartAxisTitle</span></span>](chartaxistitle.md)    |<span data-ttu-id="388be-114">Actualiza el objeto ChartAxisTitle.</span><span class="sxs-lookup"><span data-stu-id="388be-114">Update ChartAxisTitle object.</span></span> |

## <a name="properties"></a><span data-ttu-id="388be-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="388be-115">Properties</span></span>
| <span data-ttu-id="388be-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="388be-116">Property</span></span>     | <span data-ttu-id="388be-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="388be-117">Type</span></span>   |<span data-ttu-id="388be-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="388be-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="388be-119">text</span><span class="sxs-lookup"><span data-stu-id="388be-119">text</span></span>|<span data-ttu-id="388be-120">string</span><span class="sxs-lookup"><span data-stu-id="388be-120">string</span></span>|<span data-ttu-id="388be-121">Representa el título del eje.</span><span class="sxs-lookup"><span data-stu-id="388be-121">Represents the axis title.</span></span>|
|<span data-ttu-id="388be-122">visible</span><span class="sxs-lookup"><span data-stu-id="388be-122">visible</span></span>|<span data-ttu-id="388be-123">boolean</span><span class="sxs-lookup"><span data-stu-id="388be-123">boolean</span></span>|<span data-ttu-id="388be-124">Valor booleano que especifica la visibilidad del título de un eje.</span><span class="sxs-lookup"><span data-stu-id="388be-124">A boolean that specifies the visibility of an axis title.</span></span>|

## <a name="relationships"></a><span data-ttu-id="388be-125">Relaciones</span><span class="sxs-lookup"><span data-stu-id="388be-125">Relationships</span></span>
| <span data-ttu-id="388be-126">Relación</span><span class="sxs-lookup"><span data-stu-id="388be-126">Relationship</span></span> | <span data-ttu-id="388be-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="388be-127">Type</span></span>   |<span data-ttu-id="388be-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="388be-128">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="388be-129">format</span><span class="sxs-lookup"><span data-stu-id="388be-129">format</span></span>|[<span data-ttu-id="388be-130">WorkbookChartAxisTitleFormat</span><span class="sxs-lookup"><span data-stu-id="388be-130">WorkbookChartAxisTitleFormat</span></span>](chartaxistitleformat.md)|<span data-ttu-id="388be-p101">Representa el formato del título del eje del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="388be-p101">Represents the formatting of chart axis title. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="388be-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="388be-133">JSON representation</span></span>

<span data-ttu-id="388be-134">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="388be-134">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [],
  "@odata.type": "microsoft.graph.workbookChartAxisTitle"
}-->

```json
{
  "text": "string",
  "visible": true,
  "format": {"@odata.type":"microsoft.graph.workbookChartAxisTitleFormat"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartAxisTitle resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
