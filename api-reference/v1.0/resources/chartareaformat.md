---
title: Tipo de recurso ChartAreaFormat
description: Encapsula las propiedades de formato del área del gráfico en general.
ms.openlocfilehash: 19f09ab735f6df4fe4cdc0ccbf13bc75a5ca834e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028929"
---
# <a name="chartareaformat-resource-type"></a><span data-ttu-id="0d36d-103">Tipo de recurso ChartAreaFormat</span><span class="sxs-lookup"><span data-stu-id="0d36d-103">ChartAreaFormat resource type</span></span>

<span data-ttu-id="0d36d-104">Encapsula las propiedades de formato del área del gráfico en general.</span><span class="sxs-lookup"><span data-stu-id="0d36d-104">Encapsulates the format properties for the overall chart area.</span></span>


## <a name="methods"></a><span data-ttu-id="0d36d-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="0d36d-105">Methods</span></span>
<span data-ttu-id="0d36d-106">Ninguno</span><span class="sxs-lookup"><span data-stu-id="0d36d-106">None</span></span>

## <a name="properties"></a><span data-ttu-id="0d36d-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0d36d-107">Properties</span></span>
<span data-ttu-id="0d36d-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="0d36d-108">None</span></span>

## <a name="relationships"></a><span data-ttu-id="0d36d-109">Relaciones</span><span class="sxs-lookup"><span data-stu-id="0d36d-109">Relationships</span></span>
| <span data-ttu-id="0d36d-110">Relación</span><span class="sxs-lookup"><span data-stu-id="0d36d-110">Relationship</span></span> | <span data-ttu-id="0d36d-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="0d36d-111">Type</span></span>   |<span data-ttu-id="0d36d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d36d-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0d36d-113">fill</span><span class="sxs-lookup"><span data-stu-id="0d36d-113">fill</span></span>|[<span data-ttu-id="0d36d-114">WorkbookChartFill</span><span class="sxs-lookup"><span data-stu-id="0d36d-114">WorkbookChartFill</span></span>](chartfill.md)|<span data-ttu-id="0d36d-p101">Representa el formato de relleno de un objeto, que incluye información del formato de fondo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0d36d-p101">Represents the fill format of an object, which includes background formatting information. Read-only.</span></span>|
|<span data-ttu-id="0d36d-117">font</span><span class="sxs-lookup"><span data-stu-id="0d36d-117">font</span></span>|[<span data-ttu-id="0d36d-118">WorkbookChartFont</span><span class="sxs-lookup"><span data-stu-id="0d36d-118">WorkbookChartFont</span></span>](chartfont.md)|<span data-ttu-id="0d36d-p102">Representa los atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) del objeto actual. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0d36d-p102">Represents the font attributes (font name, font size, color, etc.) for the current object. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="0d36d-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0d36d-121">JSON representation</span></span>

<span data-ttu-id="0d36d-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="0d36d-122">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookChartAreaFormat"
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