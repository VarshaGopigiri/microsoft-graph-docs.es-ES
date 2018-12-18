---
title: Tipo de recurso RangeFill
description: Representa el fondo de un objeto de rango.
author: lumine2008
ms.openlocfilehash: 6ddd039190af0e86067dfda651b2bc387b4cf74f
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27303566"
---
# <a name="rangefill-resource-type"></a><span data-ttu-id="306cd-103">Tipo de recurso RangeFill</span><span class="sxs-lookup"><span data-stu-id="306cd-103">RangeFill resource type</span></span>

<span data-ttu-id="306cd-104">Representa el fondo de un objeto de rango.</span><span class="sxs-lookup"><span data-stu-id="306cd-104">Represents the background of a range object.</span></span>


## <a name="methods"></a><span data-ttu-id="306cd-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="306cd-105">Methods</span></span>

| <span data-ttu-id="306cd-106">Método</span><span class="sxs-lookup"><span data-stu-id="306cd-106">Method</span></span>           | <span data-ttu-id="306cd-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="306cd-107">Return Type</span></span>    |<span data-ttu-id="306cd-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="306cd-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="306cd-109">Get RangeFill</span><span class="sxs-lookup"><span data-stu-id="306cd-109">Get RangeFill</span></span>](../api/rangefill-get.md) | [<span data-ttu-id="306cd-110">WorkbookRangeFill</span><span class="sxs-lookup"><span data-stu-id="306cd-110">WorkbookRangeFill</span></span>](rangefill.md) |<span data-ttu-id="306cd-111">Lee las propiedades y relaciones del objeto rangeFill.</span><span class="sxs-lookup"><span data-stu-id="306cd-111">Read properties and relationships of rangeFill object.</span></span>|
|[<span data-ttu-id="306cd-112">Actualizar</span><span class="sxs-lookup"><span data-stu-id="306cd-112">Update</span></span>](../api/rangefill-update.md) | [<span data-ttu-id="306cd-113">WorkbookRangeFill</span><span class="sxs-lookup"><span data-stu-id="306cd-113">WorkbookRangeFill</span></span>](rangefill.md)   |<span data-ttu-id="306cd-114">Actualiza el objeto RangeFill.</span><span class="sxs-lookup"><span data-stu-id="306cd-114">Update RangeFill object.</span></span> |
|[<span data-ttu-id="306cd-115">Clear</span><span class="sxs-lookup"><span data-stu-id="306cd-115">Clear</span></span>](../api/rangefill-clear.md)|<span data-ttu-id="306cd-116">None</span><span class="sxs-lookup"><span data-stu-id="306cd-116">None</span></span>|<span data-ttu-id="306cd-117">Restablece el fondo del rango.</span><span class="sxs-lookup"><span data-stu-id="306cd-117">Resets the range background.</span></span>|

## <a name="properties"></a><span data-ttu-id="306cd-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="306cd-118">Properties</span></span>
| <span data-ttu-id="306cd-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="306cd-119">Property</span></span>     | <span data-ttu-id="306cd-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="306cd-120">Type</span></span>   |<span data-ttu-id="306cd-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="306cd-121">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="306cd-122">color</span><span class="sxs-lookup"><span data-stu-id="306cd-122">color</span></span>|<span data-ttu-id="306cd-123">string</span><span class="sxs-lookup"><span data-stu-id="306cd-123">string</span></span>|<span data-ttu-id="306cd-124">Código de color HTML que representa el color de la línea de borde con el formato #RRGGBB (por ejemplo, "FFA500") o como un color HTML con nombre (por ejemplo, "naranja").</span><span class="sxs-lookup"><span data-stu-id="306cd-124">HTML color code representing the color of the border line, of the form #RRGGBB (e.g. "FFA500") or as a named HTML color (e.g. "orange")</span></span>|

## <a name="relationships"></a><span data-ttu-id="306cd-125">Relaciones</span><span class="sxs-lookup"><span data-stu-id="306cd-125">Relationships</span></span>
<span data-ttu-id="306cd-126">Ninguno</span><span class="sxs-lookup"><span data-stu-id="306cd-126">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="306cd-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="306cd-127">JSON representation</span></span>

<span data-ttu-id="306cd-128">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="306cd-128">Here is a JSON representation of the resource.</span></span>

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