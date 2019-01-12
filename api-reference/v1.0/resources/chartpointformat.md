---
title: Tipo de recurso ChartPointFormat
description: Representa el objeto de formato para los puntos del gráfico.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 1c1b0a4a7d9076771da11061723f275079d429cb
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27976999"
---
# <a name="chartpointformat-resource-type"></a><span data-ttu-id="86e06-103">Tipo de recurso ChartPointFormat</span><span class="sxs-lookup"><span data-stu-id="86e06-103">ChartPointFormat resource type</span></span>

<span data-ttu-id="86e06-104">Representa el objeto de formato para los puntos del gráfico.</span><span class="sxs-lookup"><span data-stu-id="86e06-104">Represents formatting object for chart points.</span></span>


## <a name="methods"></a><span data-ttu-id="86e06-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="86e06-105">Methods</span></span>
<span data-ttu-id="86e06-106">Ninguno</span><span class="sxs-lookup"><span data-stu-id="86e06-106">None</span></span>

## <a name="properties"></a><span data-ttu-id="86e06-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="86e06-107">Properties</span></span>
<span data-ttu-id="86e06-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="86e06-108">None</span></span>

## <a name="relationships"></a><span data-ttu-id="86e06-109">Relaciones</span><span class="sxs-lookup"><span data-stu-id="86e06-109">Relationships</span></span>
| <span data-ttu-id="86e06-110">Relación</span><span class="sxs-lookup"><span data-stu-id="86e06-110">Relationship</span></span> | <span data-ttu-id="86e06-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="86e06-111">Type</span></span>   |<span data-ttu-id="86e06-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="86e06-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="86e06-113">fill</span><span class="sxs-lookup"><span data-stu-id="86e06-113">fill</span></span>|[<span data-ttu-id="86e06-114">WorkbookChartFill</span><span class="sxs-lookup"><span data-stu-id="86e06-114">WorkbookChartFill</span></span>](chartfill.md)|<span data-ttu-id="86e06-p101">Representa el formato de relleno de un gráfico, que incluye información del formato de fondo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="86e06-p101">Represents the fill format of a chart, which includes background formating information. Read-only.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="86e06-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="86e06-117">JSON representation</span></span>

<span data-ttu-id="86e06-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="86e06-118">Here is a JSON representation of the resource.</span></span>

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
