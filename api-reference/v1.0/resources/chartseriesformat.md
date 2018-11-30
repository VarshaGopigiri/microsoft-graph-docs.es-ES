---
title: Tipo de recurso ChartSeriesFormat
description: Encapsula las propiedades de formato de la serie del gráfico.
ms.openlocfilehash: 81b79331580c2d7edbc52f19d1c4c9cfd57db0cf
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029988"
---
# <a name="chartseriesformat-resource-type"></a><span data-ttu-id="40984-103">Tipo de recurso ChartSeriesFormat</span><span class="sxs-lookup"><span data-stu-id="40984-103">ChartSeriesFormat resource type</span></span>

<span data-ttu-id="40984-104">Encapsula las propiedades de formato de la serie del gráfico.</span><span class="sxs-lookup"><span data-stu-id="40984-104">encapsulates the format properties for the chart series</span></span>


## <a name="methods"></a><span data-ttu-id="40984-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="40984-105">Methods</span></span>
<span data-ttu-id="40984-106">Ninguno</span><span class="sxs-lookup"><span data-stu-id="40984-106">None</span></span>

## <a name="properties"></a><span data-ttu-id="40984-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="40984-107">Properties</span></span>
<span data-ttu-id="40984-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="40984-108">None</span></span>

## <a name="relationships"></a><span data-ttu-id="40984-109">Relaciones</span><span class="sxs-lookup"><span data-stu-id="40984-109">Relationships</span></span>
| <span data-ttu-id="40984-110">Relación</span><span class="sxs-lookup"><span data-stu-id="40984-110">Relationship</span></span> | <span data-ttu-id="40984-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="40984-111">Type</span></span>   |<span data-ttu-id="40984-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="40984-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="40984-113">fill</span><span class="sxs-lookup"><span data-stu-id="40984-113">fill</span></span>|[<span data-ttu-id="40984-114">WorkbookChartFill</span><span class="sxs-lookup"><span data-stu-id="40984-114">WorkbookChartFill</span></span>](chartfill.md)|<span data-ttu-id="40984-p101">Representa el formato de relleno de una serie del gráfico, que incluye información del formato de fondo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="40984-p101">Represents the fill format of a chart series, which includes background formating information. Read-only.</span></span>|
|<span data-ttu-id="40984-117">line</span><span class="sxs-lookup"><span data-stu-id="40984-117">line</span></span>|[<span data-ttu-id="40984-118">WorkbookChartLineFormat</span><span class="sxs-lookup"><span data-stu-id="40984-118">WorkbookChartLineFormat</span></span>](chartlineformat.md)|<span data-ttu-id="40984-p102">Representa el formato de línea. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="40984-p102">Represents line formatting. Read-only.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="40984-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="40984-121">JSON representation</span></span>

<span data-ttu-id="40984-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="40984-122">Here is a JSON representation of the resource.</span></span>

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