---
title: Tipo de recurso ChartSeriesFormat
description: Encapsula las propiedades de formato de la serie del gráfico.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: fd342e55524d51b6a0382df8ca9310ea162308d2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27961438"
---
# <a name="chartseriesformat-resource-type"></a><span data-ttu-id="1121e-103">Tipo de recurso ChartSeriesFormat</span><span class="sxs-lookup"><span data-stu-id="1121e-103">ChartSeriesFormat resource type</span></span>

<span data-ttu-id="1121e-104">Encapsula las propiedades de formato de la serie del gráfico.</span><span class="sxs-lookup"><span data-stu-id="1121e-104">encapsulates the format properties for the chart series</span></span>


## <a name="methods"></a><span data-ttu-id="1121e-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="1121e-105">Methods</span></span>
<span data-ttu-id="1121e-106">Ninguno</span><span class="sxs-lookup"><span data-stu-id="1121e-106">None</span></span>

## <a name="properties"></a><span data-ttu-id="1121e-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1121e-107">Properties</span></span>
<span data-ttu-id="1121e-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="1121e-108">None</span></span>

## <a name="relationships"></a><span data-ttu-id="1121e-109">Relaciones</span><span class="sxs-lookup"><span data-stu-id="1121e-109">Relationships</span></span>
| <span data-ttu-id="1121e-110">Relación</span><span class="sxs-lookup"><span data-stu-id="1121e-110">Relationship</span></span> | <span data-ttu-id="1121e-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="1121e-111">Type</span></span>   |<span data-ttu-id="1121e-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1121e-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1121e-113">fill</span><span class="sxs-lookup"><span data-stu-id="1121e-113">fill</span></span>|[<span data-ttu-id="1121e-114">WorkbookChartFill</span><span class="sxs-lookup"><span data-stu-id="1121e-114">WorkbookChartFill</span></span>](chartfill.md)|<span data-ttu-id="1121e-p101">Representa el formato de relleno de una serie del gráfico, que incluye información del formato de fondo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1121e-p101">Represents the fill format of a chart series, which includes background formating information. Read-only.</span></span>|
|<span data-ttu-id="1121e-117">line</span><span class="sxs-lookup"><span data-stu-id="1121e-117">line</span></span>|[<span data-ttu-id="1121e-118">WorkbookChartLineFormat</span><span class="sxs-lookup"><span data-stu-id="1121e-118">WorkbookChartLineFormat</span></span>](chartlineformat.md)|<span data-ttu-id="1121e-p102">Representa el formato de línea. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1121e-p102">Represents line formatting. Read-only.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="1121e-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1121e-121">JSON representation</span></span>

<span data-ttu-id="1121e-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="1121e-122">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookChartSeriesFormat"
}-->

```json
{
  "fill": {"@odata.type": "microsoft.graph.workbookChartFill"},
  "line": {"@odata.type": "microsoft.graph.workbookChartLineFormat"}
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartSeriesFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
