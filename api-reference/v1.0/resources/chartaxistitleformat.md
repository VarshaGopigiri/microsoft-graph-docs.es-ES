---
title: Tipo de recurso ChartAxisTitleFormat
description: Representa el formato de título del eje del gráfico.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 4aa96f0a346d8b08832464097b258a92b1db44df
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27840316"
---
# <a name="chartaxistitleformat-resource-type"></a><span data-ttu-id="aad9d-103">Tipo de recurso ChartAxisTitleFormat</span><span class="sxs-lookup"><span data-stu-id="aad9d-103">ChartAxisTitleFormat resource type</span></span>

<span data-ttu-id="aad9d-104">Representa el formato de título del eje del gráfico.</span><span class="sxs-lookup"><span data-stu-id="aad9d-104">Represents the chart axis title formatting.</span></span>


## <a name="methods"></a><span data-ttu-id="aad9d-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="aad9d-105">Methods</span></span>
<span data-ttu-id="aad9d-106">Ninguno</span><span class="sxs-lookup"><span data-stu-id="aad9d-106">None</span></span>

## <a name="properties"></a><span data-ttu-id="aad9d-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aad9d-107">Properties</span></span>
<span data-ttu-id="aad9d-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="aad9d-108">None</span></span>

## <a name="relationships"></a><span data-ttu-id="aad9d-109">Relaciones</span><span class="sxs-lookup"><span data-stu-id="aad9d-109">Relationships</span></span>
| <span data-ttu-id="aad9d-110">Relación</span><span class="sxs-lookup"><span data-stu-id="aad9d-110">Relationship</span></span> | <span data-ttu-id="aad9d-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="aad9d-111">Type</span></span>   |<span data-ttu-id="aad9d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="aad9d-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="aad9d-113">font</span><span class="sxs-lookup"><span data-stu-id="aad9d-113">font</span></span>|[<span data-ttu-id="aad9d-114">WorkbookChartFont</span><span class="sxs-lookup"><span data-stu-id="aad9d-114">WorkbookChartFont</span></span>](chartfont.md)|<span data-ttu-id="aad9d-p101">Representa los atributos de fuente (por ejemplo, nombre de fuente, tamaño de fuente, color, etc.) de un objeto de título del eje del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="aad9d-p101">Represents the font attributes, such as font name, font size, color, etc. of chart axis title object. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="aad9d-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="aad9d-117">JSON representation</span></span>

<span data-ttu-id="aad9d-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="aad9d-118">Here is a JSON representation of the resource.</span></span>

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
