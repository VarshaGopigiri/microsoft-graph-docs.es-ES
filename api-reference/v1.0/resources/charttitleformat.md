---
title: Tipo de recurso ChartTitleFormat
description: Encapsula las propiedades de formato del título del gráfico.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 3a2c16d37d2ca86d7cafbb4047ee0bcea1ee4bde
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27977118"
---
# <a name="charttitleformat-resource-type"></a><span data-ttu-id="6ee85-103">Tipo de recurso ChartTitleFormat</span><span class="sxs-lookup"><span data-stu-id="6ee85-103">ChartTitleFormat resource type</span></span>

<span data-ttu-id="6ee85-104">Encapsula las propiedades de formato del título del gráfico.</span><span class="sxs-lookup"><span data-stu-id="6ee85-104">Encapsulates the format properties for the chart title.</span></span>


## <a name="methods"></a><span data-ttu-id="6ee85-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="6ee85-105">Methods</span></span>
<span data-ttu-id="6ee85-106">Ninguno</span><span class="sxs-lookup"><span data-stu-id="6ee85-106">None</span></span>

## <a name="properties"></a><span data-ttu-id="6ee85-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6ee85-107">Properties</span></span>
<span data-ttu-id="6ee85-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="6ee85-108">None</span></span>

## <a name="relationships"></a><span data-ttu-id="6ee85-109">Relaciones</span><span class="sxs-lookup"><span data-stu-id="6ee85-109">Relationships</span></span>
| <span data-ttu-id="6ee85-110">Relación</span><span class="sxs-lookup"><span data-stu-id="6ee85-110">Relationship</span></span> | <span data-ttu-id="6ee85-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="6ee85-111">Type</span></span>   |<span data-ttu-id="6ee85-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ee85-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6ee85-113">fill</span><span class="sxs-lookup"><span data-stu-id="6ee85-113">fill</span></span>|[<span data-ttu-id="6ee85-114">WorkbookChartFill</span><span class="sxs-lookup"><span data-stu-id="6ee85-114">WorkbookChartFill</span></span>](chartfill.md)|<span data-ttu-id="6ee85-p101">Representa el formato de relleno de un objeto, que incluye información del formato de fondo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6ee85-p101">Represents the fill format of an object, which includes background formatting information. Read-only.</span></span>|
|<span data-ttu-id="6ee85-117">font</span><span class="sxs-lookup"><span data-stu-id="6ee85-117">font</span></span>|[<span data-ttu-id="6ee85-118">WorkbookChartFont</span><span class="sxs-lookup"><span data-stu-id="6ee85-118">WorkbookChartFont</span></span>](chartfont.md)|<span data-ttu-id="6ee85-p102">Representa los atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) del objeto actual. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6ee85-p102">Represents the font attributes (font name, font size, color, etc.) for the current object. Read-only.</span></span>|



## <a name="json-representation"></a><span data-ttu-id="6ee85-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6ee85-121">JSON representation</span></span>

<span data-ttu-id="6ee85-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="6ee85-122">Here is a JSON representation of the resource.</span></span>

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
