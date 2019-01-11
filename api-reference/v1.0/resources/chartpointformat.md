---
title: Tipo de recurso ChartPointFormat
description: Representa el objeto de formato para los puntos del gráfico.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 5923252a9fce47eedc58751def301b6515560ddd
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27883345"
---
# <a name="chartpointformat-resource-type"></a><span data-ttu-id="bb891-103">Tipo de recurso ChartPointFormat</span><span class="sxs-lookup"><span data-stu-id="bb891-103">ChartPointFormat resource type</span></span>

<span data-ttu-id="bb891-104">Representa el objeto de formato para los puntos del gráfico.</span><span class="sxs-lookup"><span data-stu-id="bb891-104">Represents formatting object for chart points.</span></span>


## <a name="methods"></a><span data-ttu-id="bb891-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="bb891-105">Methods</span></span>
<span data-ttu-id="bb891-106">Ninguno</span><span class="sxs-lookup"><span data-stu-id="bb891-106">None</span></span>

## <a name="properties"></a><span data-ttu-id="bb891-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bb891-107">Properties</span></span>
<span data-ttu-id="bb891-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="bb891-108">None</span></span>

## <a name="relationships"></a><span data-ttu-id="bb891-109">Relaciones</span><span class="sxs-lookup"><span data-stu-id="bb891-109">Relationships</span></span>
| <span data-ttu-id="bb891-110">Relación</span><span class="sxs-lookup"><span data-stu-id="bb891-110">Relationship</span></span> | <span data-ttu-id="bb891-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="bb891-111">Type</span></span>   |<span data-ttu-id="bb891-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb891-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bb891-113">fill</span><span class="sxs-lookup"><span data-stu-id="bb891-113">fill</span></span>|[<span data-ttu-id="bb891-114">WorkbookChartFill</span><span class="sxs-lookup"><span data-stu-id="bb891-114">WorkbookChartFill</span></span>](chartfill.md)|<span data-ttu-id="bb891-p101">Representa el formato de relleno de un gráfico, que incluye información del formato de fondo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bb891-p101">Represents the fill format of a chart, which includes background formating information. Read-only.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="bb891-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="bb891-117">JSON representation</span></span>

<span data-ttu-id="bb891-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="bb891-118">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookChartPointFormat"
}-->

```json
{
  "fill": {"@odata.type": "microsoft.graph.workbookChartFill"}
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartPointFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
