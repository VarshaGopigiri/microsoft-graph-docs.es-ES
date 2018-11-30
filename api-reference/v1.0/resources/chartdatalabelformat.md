---
title: Tipo de recurso ChartDataLabelFormat
description: Encapsula las propiedades de formato de las etiquetas de datos del gráfico.
ms.openlocfilehash: ec81523dc09c17cd8c7fb9d543c2214377201260
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029596"
---
# <a name="chartdatalabelformat-resource-type"></a><span data-ttu-id="e4a8e-103">Tipo de recurso ChartDataLabelFormat</span><span class="sxs-lookup"><span data-stu-id="e4a8e-103">ChartDataLabelFormat resource type</span></span>

<span data-ttu-id="e4a8e-104">Encapsula las propiedades de formato de las etiquetas de datos del gráfico.</span><span class="sxs-lookup"><span data-stu-id="e4a8e-104">Encapsulates the format properties for the chart data labels.</span></span>


## <a name="methods"></a><span data-ttu-id="e4a8e-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="e4a8e-105">Methods</span></span>
<span data-ttu-id="e4a8e-106">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e4a8e-106">None</span></span>

## <a name="properties"></a><span data-ttu-id="e4a8e-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e4a8e-107">Properties</span></span>
<span data-ttu-id="e4a8e-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e4a8e-108">None</span></span>

## <a name="relationships"></a><span data-ttu-id="e4a8e-109">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e4a8e-109">Relationships</span></span>
| <span data-ttu-id="e4a8e-110">Relación</span><span class="sxs-lookup"><span data-stu-id="e4a8e-110">Relationship</span></span> | <span data-ttu-id="e4a8e-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4a8e-111">Type</span></span>   |<span data-ttu-id="e4a8e-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4a8e-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e4a8e-113">fill</span><span class="sxs-lookup"><span data-stu-id="e4a8e-113">fill</span></span>|[<span data-ttu-id="e4a8e-114">WorkbookChartFill</span><span class="sxs-lookup"><span data-stu-id="e4a8e-114">WorkbookChartFill</span></span>](chartfill.md)|<span data-ttu-id="e4a8e-p101">Representa el formato de relleno de la etiqueta de datos del gráfico actual. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e4a8e-p101">Represents the fill format of the current chart data label. Read-only.</span></span>|
|<span data-ttu-id="e4a8e-117">font</span><span class="sxs-lookup"><span data-stu-id="e4a8e-117">font</span></span>|[<span data-ttu-id="e4a8e-118">WorkbookChartFont</span><span class="sxs-lookup"><span data-stu-id="e4a8e-118">WorkbookChartFont</span></span>](chartfont.md)|<span data-ttu-id="e4a8e-p102">Representa los atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) de una etiqueta de datos del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e4a8e-p102">Represents the font attributes (font name, font size, color, etc.) for a chart data label. Read-only.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="e4a8e-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e4a8e-121">JSON representation</span></span>

<span data-ttu-id="e4a8e-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e4a8e-122">Here is a JSON representation of the resource.</span></span>

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