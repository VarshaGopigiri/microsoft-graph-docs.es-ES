---
title: Tipo de recurso ChartAxisFormat
description: Encapsula las propiedades de formato del eje del gráfico.
ms.openlocfilehash: 38679d8f6d70c336f17aa5c17c9a20e80204cfb2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032712"
---
# <a name="chartaxisformat-resource-type"></a><span data-ttu-id="16f7b-103">Tipo de recurso ChartAxisFormat</span><span class="sxs-lookup"><span data-stu-id="16f7b-103">ChartAxisFormat resource type</span></span>

<span data-ttu-id="16f7b-104">Encapsula las propiedades de formato del eje del gráfico.</span><span class="sxs-lookup"><span data-stu-id="16f7b-104">Encapsulates the format properties for the chart axis.</span></span>


## <a name="methods"></a><span data-ttu-id="16f7b-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="16f7b-105">Methods</span></span>
<span data-ttu-id="16f7b-106">Ninguno</span><span class="sxs-lookup"><span data-stu-id="16f7b-106">None</span></span>
## <a name="properties"></a><span data-ttu-id="16f7b-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="16f7b-107">Properties</span></span>
<span data-ttu-id="16f7b-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="16f7b-108">None</span></span>

## <a name="relationships"></a><span data-ttu-id="16f7b-109">Relaciones</span><span class="sxs-lookup"><span data-stu-id="16f7b-109">Relationships</span></span>
| <span data-ttu-id="16f7b-110">Relación</span><span class="sxs-lookup"><span data-stu-id="16f7b-110">Relationship</span></span> | <span data-ttu-id="16f7b-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="16f7b-111">Type</span></span>   |<span data-ttu-id="16f7b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="16f7b-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="16f7b-113">font</span><span class="sxs-lookup"><span data-stu-id="16f7b-113">font</span></span>|[<span data-ttu-id="16f7b-114">WorkbookChartFont</span><span class="sxs-lookup"><span data-stu-id="16f7b-114">WorkbookChartFont</span></span>](chartfont.md)|<span data-ttu-id="16f7b-p101">Representa los atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) de un elemento del eje del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="16f7b-p101">Represents the font attributes (font name, font size, color, etc.) for a chart axis element. Read-only.</span></span>|
|<span data-ttu-id="16f7b-117">line</span><span class="sxs-lookup"><span data-stu-id="16f7b-117">line</span></span>|[<span data-ttu-id="16f7b-118">WorkbookChartLineFormat</span><span class="sxs-lookup"><span data-stu-id="16f7b-118">WorkbookChartLineFormat</span></span>](chartlineformat.md)|<span data-ttu-id="16f7b-p102">Representa el formato de línea de gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="16f7b-p102">Represents chart line formatting. Read-only.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="16f7b-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="16f7b-121">JSON representation</span></span>

<span data-ttu-id="16f7b-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="16f7b-122">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookChartAxisFormat"
}-->

```json
{
  "font": {"@odata.type": "microsoft.graph.workbookChartFont"},
  "line": {"@odata.type": "microsoft.graph.workbookChartLineFormat"}
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartAxisFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->