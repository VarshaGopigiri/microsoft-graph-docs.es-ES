---
title: Tipo de recurso ChartGridlinesFormat
description: Encapsula las propiedades de formato de las líneas de cuadrícula del gráfico.
ms.openlocfilehash: 8286cd1a03188e9f6267b0e4731689c18b868083
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031595"
---
# <a name="chartgridlinesformat-resource-type"></a><span data-ttu-id="d925a-103">Tipo de recurso ChartGridlinesFormat</span><span class="sxs-lookup"><span data-stu-id="d925a-103">ChartGridlinesFormat resource type</span></span>

<span data-ttu-id="d925a-104">Encapsula las propiedades de formato de las líneas de cuadrícula del gráfico.</span><span class="sxs-lookup"><span data-stu-id="d925a-104">Encapsulates the format properties for chart gridlines.</span></span>


## <a name="methods"></a><span data-ttu-id="d925a-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="d925a-105">Methods</span></span>
<span data-ttu-id="d925a-106">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d925a-106">None</span></span>

## <a name="properties"></a><span data-ttu-id="d925a-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d925a-107">Properties</span></span>
<span data-ttu-id="d925a-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d925a-108">None</span></span>

## <a name="relationships"></a><span data-ttu-id="d925a-109">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d925a-109">Relationships</span></span>
| <span data-ttu-id="d925a-110">Relación</span><span class="sxs-lookup"><span data-stu-id="d925a-110">Relationship</span></span> | <span data-ttu-id="d925a-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="d925a-111">Type</span></span>   |<span data-ttu-id="d925a-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="d925a-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d925a-113">line</span><span class="sxs-lookup"><span data-stu-id="d925a-113">line</span></span>|[<span data-ttu-id="d925a-114">WorkbookChartLineFormat</span><span class="sxs-lookup"><span data-stu-id="d925a-114">WorkbookChartLineFormat</span></span>](chartlineformat.md)|<span data-ttu-id="d925a-p101">Representa el formato de línea de gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d925a-p101">Represents chart line formatting. Read-only.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="d925a-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d925a-117">JSON representation</span></span>

<span data-ttu-id="d925a-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d925a-118">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookChartGridlinesFormat"
}-->

```json
{
  "line": {"@odata.type": "microsoft.graph.workbookChartLineFormat"}
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartGridlinesFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->