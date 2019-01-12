---
title: Tipo de recurso RangeFill
description: Representa el fondo de un objeto de rango.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 75aa4bd91ad6f1038fdc42460c6a3c9ab928a09d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27911822"
---
# <a name="rangefill-resource-type"></a><span data-ttu-id="c8292-103">Tipo de recurso RangeFill</span><span class="sxs-lookup"><span data-stu-id="c8292-103">RangeFill resource type</span></span>

<span data-ttu-id="c8292-104">Representa el fondo de un objeto de rango.</span><span class="sxs-lookup"><span data-stu-id="c8292-104">Represents the background of a range object.</span></span>


## <a name="methods"></a><span data-ttu-id="c8292-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="c8292-105">Methods</span></span>

| <span data-ttu-id="c8292-106">Método</span><span class="sxs-lookup"><span data-stu-id="c8292-106">Method</span></span>           | <span data-ttu-id="c8292-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8292-107">Return Type</span></span>    |<span data-ttu-id="c8292-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8292-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="c8292-109">Get RangeFill</span><span class="sxs-lookup"><span data-stu-id="c8292-109">Get RangeFill</span></span>](../api/rangefill-get.md) | [<span data-ttu-id="c8292-110">WorkbookRangeFill</span><span class="sxs-lookup"><span data-stu-id="c8292-110">WorkbookRangeFill</span></span>](rangefill.md) |<span data-ttu-id="c8292-111">Lee las propiedades y relaciones del objeto rangeFill.</span><span class="sxs-lookup"><span data-stu-id="c8292-111">Read properties and relationships of rangeFill object.</span></span>|
|[<span data-ttu-id="c8292-112">Update</span><span class="sxs-lookup"><span data-stu-id="c8292-112">Update</span></span>](../api/rangefill-update.md) | [<span data-ttu-id="c8292-113">WorkbookRangeFill</span><span class="sxs-lookup"><span data-stu-id="c8292-113">WorkbookRangeFill</span></span>](rangefill.md)   |<span data-ttu-id="c8292-114">Actualiza el objeto RangeFill.</span><span class="sxs-lookup"><span data-stu-id="c8292-114">Update RangeFill object.</span></span> |
|[<span data-ttu-id="c8292-115">Clear</span><span class="sxs-lookup"><span data-stu-id="c8292-115">Clear</span></span>](../api/rangefill-clear.md)|<span data-ttu-id="c8292-116">None</span><span class="sxs-lookup"><span data-stu-id="c8292-116">None</span></span>|<span data-ttu-id="c8292-117">Restablece el fondo del rango.</span><span class="sxs-lookup"><span data-stu-id="c8292-117">Resets the range background.</span></span>|

## <a name="properties"></a><span data-ttu-id="c8292-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c8292-118">Properties</span></span>
| <span data-ttu-id="c8292-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c8292-119">Property</span></span>     | <span data-ttu-id="c8292-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="c8292-120">Type</span></span>   |<span data-ttu-id="c8292-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8292-121">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c8292-122">color</span><span class="sxs-lookup"><span data-stu-id="c8292-122">color</span></span>|<span data-ttu-id="c8292-123">string</span><span class="sxs-lookup"><span data-stu-id="c8292-123">string</span></span>|<span data-ttu-id="c8292-124">Código de color HTML que representa el color de la línea de borde con el formato #RRGGBB (por ejemplo, "FFA500") o como un color HTML con nombre (por ejemplo, "naranja").</span><span class="sxs-lookup"><span data-stu-id="c8292-124">HTML color code representing the color of the border line, of the form #RRGGBB (e.g. "FFA500") or as a named HTML color (e.g. "orange")</span></span>|

## <a name="relationships"></a><span data-ttu-id="c8292-125">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c8292-125">Relationships</span></span>
<span data-ttu-id="c8292-126">Ninguno</span><span class="sxs-lookup"><span data-stu-id="c8292-126">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="c8292-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c8292-127">JSON representation</span></span>

<span data-ttu-id="c8292-128">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c8292-128">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookRangeFill"
}-->

```json
{
  "color": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "RangeFill resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
