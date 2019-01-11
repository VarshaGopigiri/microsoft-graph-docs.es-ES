---
title: Tipo de recurso RangeFill
description: Representa el fondo de un objeto de rango.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: d1dc1bda19d725999f9a49644bee1e4cb1126ec2
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27877192"
---
# <a name="rangefill-resource-type"></a><span data-ttu-id="ee576-103">Tipo de recurso RangeFill</span><span class="sxs-lookup"><span data-stu-id="ee576-103">RangeFill resource type</span></span>

<span data-ttu-id="ee576-104">Representa el fondo de un objeto de rango.</span><span class="sxs-lookup"><span data-stu-id="ee576-104">Represents the background of a range object.</span></span>


## <a name="methods"></a><span data-ttu-id="ee576-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="ee576-105">Methods</span></span>

| <span data-ttu-id="ee576-106">Método</span><span class="sxs-lookup"><span data-stu-id="ee576-106">Method</span></span>           | <span data-ttu-id="ee576-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ee576-107">Return Type</span></span>    |<span data-ttu-id="ee576-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee576-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="ee576-109">Get RangeFill</span><span class="sxs-lookup"><span data-stu-id="ee576-109">Get RangeFill</span></span>](../api/rangefill-get.md) | [<span data-ttu-id="ee576-110">WorkbookRangeFill</span><span class="sxs-lookup"><span data-stu-id="ee576-110">WorkbookRangeFill</span></span>](rangefill.md) |<span data-ttu-id="ee576-111">Lee las propiedades y relaciones del objeto rangeFill.</span><span class="sxs-lookup"><span data-stu-id="ee576-111">Read properties and relationships of rangeFill object.</span></span>|
|[<span data-ttu-id="ee576-112">Update</span><span class="sxs-lookup"><span data-stu-id="ee576-112">Update</span></span>](../api/rangefill-update.md) | [<span data-ttu-id="ee576-113">WorkbookRangeFill</span><span class="sxs-lookup"><span data-stu-id="ee576-113">WorkbookRangeFill</span></span>](rangefill.md)   |<span data-ttu-id="ee576-114">Actualiza el objeto RangeFill.</span><span class="sxs-lookup"><span data-stu-id="ee576-114">Update RangeFill object.</span></span> |
|[<span data-ttu-id="ee576-115">Clear</span><span class="sxs-lookup"><span data-stu-id="ee576-115">Clear</span></span>](../api/rangefill-clear.md)|<span data-ttu-id="ee576-116">None</span><span class="sxs-lookup"><span data-stu-id="ee576-116">None</span></span>|<span data-ttu-id="ee576-117">Restablece el fondo del rango.</span><span class="sxs-lookup"><span data-stu-id="ee576-117">Resets the range background.</span></span>|

## <a name="properties"></a><span data-ttu-id="ee576-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ee576-118">Properties</span></span>
| <span data-ttu-id="ee576-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ee576-119">Property</span></span>     | <span data-ttu-id="ee576-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="ee576-120">Type</span></span>   |<span data-ttu-id="ee576-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee576-121">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ee576-122">color</span><span class="sxs-lookup"><span data-stu-id="ee576-122">color</span></span>|<span data-ttu-id="ee576-123">string</span><span class="sxs-lookup"><span data-stu-id="ee576-123">string</span></span>|<span data-ttu-id="ee576-124">Código de color HTML que representa el color de la línea de borde con el formato #RRGGBB (por ejemplo, "FFA500") o como un color HTML con nombre (por ejemplo, "naranja").</span><span class="sxs-lookup"><span data-stu-id="ee576-124">HTML color code representing the color of the border line, of the form #RRGGBB (e.g. "FFA500") or as a named HTML color (e.g. "orange")</span></span>|

## <a name="relationships"></a><span data-ttu-id="ee576-125">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ee576-125">Relationships</span></span>
<span data-ttu-id="ee576-126">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ee576-126">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="ee576-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ee576-127">JSON representation</span></span>

<span data-ttu-id="ee576-128">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ee576-128">Here is a JSON representation of the resource.</span></span>

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
