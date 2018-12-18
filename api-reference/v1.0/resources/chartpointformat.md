---
title: Tipo de recurso ChartPointFormat
description: Representa el objeto de formato para los puntos del gráfico.
author: lumine2008
ms.openlocfilehash: 94ba58eb60f80cf704de3d8a44e6e96f010429a7
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27311315"
---
# <a name="chartpointformat-resource-type"></a><span data-ttu-id="7e2bd-103">Tipo de recurso ChartPointFormat</span><span class="sxs-lookup"><span data-stu-id="7e2bd-103">ChartPointFormat resource type</span></span>

<span data-ttu-id="7e2bd-104">Representa el objeto de formato para los puntos del gráfico.</span><span class="sxs-lookup"><span data-stu-id="7e2bd-104">Represents formatting object for chart points.</span></span>


## <a name="methods"></a><span data-ttu-id="7e2bd-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="7e2bd-105">Methods</span></span>
<span data-ttu-id="7e2bd-106">Ninguno</span><span class="sxs-lookup"><span data-stu-id="7e2bd-106">None</span></span>

## <a name="properties"></a><span data-ttu-id="7e2bd-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7e2bd-107">Properties</span></span>
<span data-ttu-id="7e2bd-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="7e2bd-108">None</span></span>

## <a name="relationships"></a><span data-ttu-id="7e2bd-109">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7e2bd-109">Relationships</span></span>
| <span data-ttu-id="7e2bd-110">Relación</span><span class="sxs-lookup"><span data-stu-id="7e2bd-110">Relationship</span></span> | <span data-ttu-id="7e2bd-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="7e2bd-111">Type</span></span>   |<span data-ttu-id="7e2bd-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e2bd-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7e2bd-113">fill</span><span class="sxs-lookup"><span data-stu-id="7e2bd-113">fill</span></span>|[<span data-ttu-id="7e2bd-114">WorkbookChartFill</span><span class="sxs-lookup"><span data-stu-id="7e2bd-114">WorkbookChartFill</span></span>](chartfill.md)|<span data-ttu-id="7e2bd-p101">Representa el formato de relleno de un gráfico, que incluye información del formato de fondo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7e2bd-p101">Represents the fill format of a chart, which includes background formating information. Read-only.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="7e2bd-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7e2bd-117">JSON representation</span></span>

<span data-ttu-id="7e2bd-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7e2bd-118">Here is a JSON representation of the resource.</span></span>

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