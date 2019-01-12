---
title: Tipo de recurso ChartAxisTitleFormat
description: Representa el formato de título del eje del gráfico.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 26d305d8bd4a0059123f77bd86cbbf5fd01dcea7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27959485"
---
# <a name="chartaxistitleformat-resource-type"></a><span data-ttu-id="4e554-103">Tipo de recurso ChartAxisTitleFormat</span><span class="sxs-lookup"><span data-stu-id="4e554-103">ChartAxisTitleFormat resource type</span></span>

<span data-ttu-id="4e554-104">Representa el formato de título del eje del gráfico.</span><span class="sxs-lookup"><span data-stu-id="4e554-104">Represents the chart axis title formatting.</span></span>


## <a name="methods"></a><span data-ttu-id="4e554-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="4e554-105">Methods</span></span>
<span data-ttu-id="4e554-106">Ninguno</span><span class="sxs-lookup"><span data-stu-id="4e554-106">None</span></span>

## <a name="properties"></a><span data-ttu-id="4e554-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4e554-107">Properties</span></span>
<span data-ttu-id="4e554-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="4e554-108">None</span></span>

## <a name="relationships"></a><span data-ttu-id="4e554-109">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4e554-109">Relationships</span></span>
| <span data-ttu-id="4e554-110">Relación</span><span class="sxs-lookup"><span data-stu-id="4e554-110">Relationship</span></span> | <span data-ttu-id="4e554-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="4e554-111">Type</span></span>   |<span data-ttu-id="4e554-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="4e554-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4e554-113">font</span><span class="sxs-lookup"><span data-stu-id="4e554-113">font</span></span>|[<span data-ttu-id="4e554-114">WorkbookChartFont</span><span class="sxs-lookup"><span data-stu-id="4e554-114">WorkbookChartFont</span></span>](chartfont.md)|<span data-ttu-id="4e554-p101">Representa los atributos de fuente (por ejemplo, nombre de fuente, tamaño de fuente, color, etc.) de un objeto de título del eje del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4e554-p101">Represents the font attributes, such as font name, font size, color, etc. of chart axis title object. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="4e554-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4e554-117">JSON representation</span></span>

<span data-ttu-id="4e554-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4e554-118">Here is a JSON representation of the resource.</span></span>

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
