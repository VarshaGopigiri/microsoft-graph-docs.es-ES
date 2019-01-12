---
title: Tipo de recurso ChartDataLabelFormat
description: Encapsula las propiedades de formato de las etiquetas de datos del gráfico.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 645267fd595a4b8e83090d9d6b2179e8c6112a78
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27951995"
---
# <a name="chartdatalabelformat-resource-type"></a><span data-ttu-id="1c491-103">Tipo de recurso ChartDataLabelFormat</span><span class="sxs-lookup"><span data-stu-id="1c491-103">ChartDataLabelFormat resource type</span></span>

<span data-ttu-id="1c491-104">Encapsula las propiedades de formato de las etiquetas de datos del gráfico.</span><span class="sxs-lookup"><span data-stu-id="1c491-104">Encapsulates the format properties for the chart data labels.</span></span>


## <a name="methods"></a><span data-ttu-id="1c491-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="1c491-105">Methods</span></span>
<span data-ttu-id="1c491-106">Ninguno</span><span class="sxs-lookup"><span data-stu-id="1c491-106">None</span></span>

## <a name="properties"></a><span data-ttu-id="1c491-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1c491-107">Properties</span></span>
<span data-ttu-id="1c491-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="1c491-108">None</span></span>

## <a name="relationships"></a><span data-ttu-id="1c491-109">Relaciones</span><span class="sxs-lookup"><span data-stu-id="1c491-109">Relationships</span></span>
| <span data-ttu-id="1c491-110">Relación</span><span class="sxs-lookup"><span data-stu-id="1c491-110">Relationship</span></span> | <span data-ttu-id="1c491-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="1c491-111">Type</span></span>   |<span data-ttu-id="1c491-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c491-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1c491-113">fill</span><span class="sxs-lookup"><span data-stu-id="1c491-113">fill</span></span>|[<span data-ttu-id="1c491-114">WorkbookChartFill</span><span class="sxs-lookup"><span data-stu-id="1c491-114">WorkbookChartFill</span></span>](chartfill.md)|<span data-ttu-id="1c491-p101">Representa el formato de relleno de la etiqueta de datos del gráfico actual. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1c491-p101">Represents the fill format of the current chart data label. Read-only.</span></span>|
|<span data-ttu-id="1c491-117">font</span><span class="sxs-lookup"><span data-stu-id="1c491-117">font</span></span>|[<span data-ttu-id="1c491-118">WorkbookChartFont</span><span class="sxs-lookup"><span data-stu-id="1c491-118">WorkbookChartFont</span></span>](chartfont.md)|<span data-ttu-id="1c491-p102">Representa los atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) de una etiqueta de datos del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1c491-p102">Represents the font attributes (font name, font size, color, etc.) for a chart data label. Read-only.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="1c491-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1c491-121">JSON representation</span></span>

<span data-ttu-id="1c491-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="1c491-122">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookChartDataLabelFormat"
}-->

```json
{
  "fill": {"@odata.type": "microsoft.graph.workbookChartFill"},
  "font": {"@odata.type": "microsoft.graph.workbookChartFont"}
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartDataLabelFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
