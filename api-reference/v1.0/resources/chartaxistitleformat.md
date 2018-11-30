---
title: Tipo de recurso ChartAxisTitleFormat
description: Representa el formato de título del eje del gráfico.
ms.openlocfilehash: 417c594096ae19c0a223eaeaa543827f91306e8c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031215"
---
# <a name="chartaxistitleformat-resource-type"></a><span data-ttu-id="e6262-103">Tipo de recurso ChartAxisTitleFormat</span><span class="sxs-lookup"><span data-stu-id="e6262-103">ChartAxisTitleFormat resource type</span></span>

<span data-ttu-id="e6262-104">Representa el formato de título del eje del gráfico.</span><span class="sxs-lookup"><span data-stu-id="e6262-104">Represents the chart axis title formatting.</span></span>


## <a name="methods"></a><span data-ttu-id="e6262-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="e6262-105">Methods</span></span>
<span data-ttu-id="e6262-106">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e6262-106">None</span></span>

## <a name="properties"></a><span data-ttu-id="e6262-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e6262-107">Properties</span></span>
<span data-ttu-id="e6262-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e6262-108">None</span></span>

## <a name="relationships"></a><span data-ttu-id="e6262-109">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e6262-109">Relationships</span></span>
| <span data-ttu-id="e6262-110">Relación</span><span class="sxs-lookup"><span data-stu-id="e6262-110">Relationship</span></span> | <span data-ttu-id="e6262-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="e6262-111">Type</span></span>   |<span data-ttu-id="e6262-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6262-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e6262-113">font</span><span class="sxs-lookup"><span data-stu-id="e6262-113">font</span></span>|[<span data-ttu-id="e6262-114">WorkbookChartFont</span><span class="sxs-lookup"><span data-stu-id="e6262-114">WorkbookChartFont</span></span>](chartfont.md)|<span data-ttu-id="e6262-p101">Representa los atributos de fuente (por ejemplo, nombre de fuente, tamaño de fuente, color, etc.) de un objeto de título del eje del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e6262-p101">Represents the font attributes, such as font name, font size, color, etc. of chart axis title object. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="e6262-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e6262-117">JSON representation</span></span>

<span data-ttu-id="e6262-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e6262-118">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookChartAxisTitleFormat"
}-->

```json
{
  "font": {"@odata.type": "microsoft.graph.workbookChartFont"}
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartAxisTitleFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->