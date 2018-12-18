---
title: Tipo de recurso ChartLegendFormat
description: Encapsula las propiedades de formato de una leyenda del gráfico.
author: lumine2008
ms.openlocfilehash: 6ef6f2d26ade1d8d93489fbc560d4e0eb511bc86
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27334380"
---
# <a name="chartlegendformat-resource-type"></a><span data-ttu-id="25d4d-103">Tipo de recurso ChartLegendFormat</span><span class="sxs-lookup"><span data-stu-id="25d4d-103">ChartLegendFormat resource type</span></span>

<span data-ttu-id="25d4d-104">Encapsula las propiedades de formato de una leyenda del gráfico.</span><span class="sxs-lookup"><span data-stu-id="25d4d-104">Encapsulates the format properties of a chart legend.</span></span>


## <a name="methods"></a><span data-ttu-id="25d4d-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="25d4d-105">Methods</span></span>
<span data-ttu-id="25d4d-106">Ninguno</span><span class="sxs-lookup"><span data-stu-id="25d4d-106">None</span></span>

## <a name="properties"></a><span data-ttu-id="25d4d-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="25d4d-107">Properties</span></span>
<span data-ttu-id="25d4d-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="25d4d-108">None</span></span>

## <a name="relationships"></a><span data-ttu-id="25d4d-109">Relaciones</span><span class="sxs-lookup"><span data-stu-id="25d4d-109">Relationships</span></span>
| <span data-ttu-id="25d4d-110">Relación</span><span class="sxs-lookup"><span data-stu-id="25d4d-110">Relationship</span></span> | <span data-ttu-id="25d4d-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="25d4d-111">Type</span></span>   |<span data-ttu-id="25d4d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="25d4d-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="25d4d-113">fill</span><span class="sxs-lookup"><span data-stu-id="25d4d-113">fill</span></span>|[<span data-ttu-id="25d4d-114">WorkbookChartFill</span><span class="sxs-lookup"><span data-stu-id="25d4d-114">WorkbookChartFill</span></span>](chartfill.md)|<span data-ttu-id="25d4d-p101">Representa el formato de relleno de un objeto, que incluye información del formato de fondo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="25d4d-p101">Represents the fill format of an object, which includes background formating information. Read-only.</span></span>|
|<span data-ttu-id="25d4d-117">font</span><span class="sxs-lookup"><span data-stu-id="25d4d-117">font</span></span>|[<span data-ttu-id="25d4d-118">WorkbookChartFont</span><span class="sxs-lookup"><span data-stu-id="25d4d-118">WorkbookChartFont</span></span>](chartfont.md)|<span data-ttu-id="25d4d-p102">Representa los atributos de fuente (por ejemplo, nombre de fuente, tamaño de fuente, color, etc.) de una leyenda del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="25d4d-p102">Represents the font attributes such as font name, font size, color, etc. of a chart legend. Read-only.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="25d4d-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="25d4d-121">JSON representation</span></span>

<span data-ttu-id="25d4d-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="25d4d-122">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookChartLegendFormat"
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
  "description": "ChartLegendFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->