---
title: Tipo de recurso ChartTitleFormat
description: Encapsula las propiedades de formato del título del gráfico.
ms.openlocfilehash: 7e84412adb46981a0a2b8570ed28c62d36936e36
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029457"
---
# <a name="charttitleformat-resource-type"></a><span data-ttu-id="0a9f9-103">Tipo de recurso ChartTitleFormat</span><span class="sxs-lookup"><span data-stu-id="0a9f9-103">ChartTitleFormat resource type</span></span>

<span data-ttu-id="0a9f9-104">Encapsula las propiedades de formato del título del gráfico.</span><span class="sxs-lookup"><span data-stu-id="0a9f9-104">Encapsulates the format properties for the chart title.</span></span>


## <a name="methods"></a><span data-ttu-id="0a9f9-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="0a9f9-105">Methods</span></span>
<span data-ttu-id="0a9f9-106">Ninguno</span><span class="sxs-lookup"><span data-stu-id="0a9f9-106">None</span></span>

## <a name="properties"></a><span data-ttu-id="0a9f9-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0a9f9-107">Properties</span></span>
<span data-ttu-id="0a9f9-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="0a9f9-108">None</span></span>

## <a name="relationships"></a><span data-ttu-id="0a9f9-109">Relaciones</span><span class="sxs-lookup"><span data-stu-id="0a9f9-109">Relationships</span></span>
| <span data-ttu-id="0a9f9-110">Relación</span><span class="sxs-lookup"><span data-stu-id="0a9f9-110">Relationship</span></span> | <span data-ttu-id="0a9f9-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="0a9f9-111">Type</span></span>   |<span data-ttu-id="0a9f9-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a9f9-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0a9f9-113">fill</span><span class="sxs-lookup"><span data-stu-id="0a9f9-113">fill</span></span>|[<span data-ttu-id="0a9f9-114">WorkbookChartFill</span><span class="sxs-lookup"><span data-stu-id="0a9f9-114">WorkbookChartFill</span></span>](chartfill.md)|<span data-ttu-id="0a9f9-p101">Representa el formato de relleno de un objeto, que incluye información del formato de fondo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0a9f9-p101">Represents the fill format of an object, which includes background formatting information. Read-only.</span></span>|
|<span data-ttu-id="0a9f9-117">font</span><span class="sxs-lookup"><span data-stu-id="0a9f9-117">font</span></span>|[<span data-ttu-id="0a9f9-118">WorkbookChartFont</span><span class="sxs-lookup"><span data-stu-id="0a9f9-118">WorkbookChartFont</span></span>](chartfont.md)|<span data-ttu-id="0a9f9-p102">Representa los atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) del objeto actual. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0a9f9-p102">Represents the font attributes (font name, font size, color, etc.) for the current object. Read-only.</span></span>|



## <a name="json-representation"></a><span data-ttu-id="0a9f9-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0a9f9-121">JSON representation</span></span>

<span data-ttu-id="0a9f9-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="0a9f9-122">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookChartTitleFormat"
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
  "description": "ChartAreaFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
