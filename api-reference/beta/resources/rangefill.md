---
title: Tipo de recurso RangeFill
description: Representa el fondo de un objeto de rango.
author: lumine2008
ms.openlocfilehash: 21d40b1ec65ad49241af30912c3c05e114c7008d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27323712"
---
# <a name="rangefill-resource-type"></a><span data-ttu-id="afbe8-103">Tipo de recurso RangeFill</span><span class="sxs-lookup"><span data-stu-id="afbe8-103">RangeFill resource type</span></span>

> <span data-ttu-id="afbe8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="afbe8-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="afbe8-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="afbe8-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="afbe8-106">Representa el fondo de un objeto de rango.</span><span class="sxs-lookup"><span data-stu-id="afbe8-106">Represents the background of a range object.</span></span>


## <a name="methods"></a><span data-ttu-id="afbe8-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="afbe8-107">Methods</span></span>

| <span data-ttu-id="afbe8-108">Método</span><span class="sxs-lookup"><span data-stu-id="afbe8-108">Method</span></span>           | <span data-ttu-id="afbe8-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="afbe8-109">Return Type</span></span>    |<span data-ttu-id="afbe8-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="afbe8-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="afbe8-111">Get RangeFill</span><span class="sxs-lookup"><span data-stu-id="afbe8-111">Get RangeFill</span></span>](../api/rangefill-get.md) | [<span data-ttu-id="afbe8-112">RangeFill</span><span class="sxs-lookup"><span data-stu-id="afbe8-112">RangeFill</span></span>](rangefill.md) |<span data-ttu-id="afbe8-113">Lee las propiedades y relaciones del objeto rangeFill.</span><span class="sxs-lookup"><span data-stu-id="afbe8-113">Read properties and relationships of rangeFill object.</span></span>|
|[<span data-ttu-id="afbe8-114">Actualizar</span><span class="sxs-lookup"><span data-stu-id="afbe8-114">Update</span></span>](../api/rangefill-update.md) | [<span data-ttu-id="afbe8-115">RangeFill</span><span class="sxs-lookup"><span data-stu-id="afbe8-115">RangeFill</span></span>](rangefill.md)   |<span data-ttu-id="afbe8-116">Actualiza el objeto RangeFill.</span><span class="sxs-lookup"><span data-stu-id="afbe8-116">Update RangeFill object.</span></span> |
|[<span data-ttu-id="afbe8-117">Clear</span><span class="sxs-lookup"><span data-stu-id="afbe8-117">Clear</span></span>](../api/rangefill-clear.md)|<span data-ttu-id="afbe8-118">None</span><span class="sxs-lookup"><span data-stu-id="afbe8-118">None</span></span>|<span data-ttu-id="afbe8-119">Restablece el fondo del rango.</span><span class="sxs-lookup"><span data-stu-id="afbe8-119">Resets the range background.</span></span>|

## <a name="properties"></a><span data-ttu-id="afbe8-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="afbe8-120">Properties</span></span>
| <span data-ttu-id="afbe8-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="afbe8-121">Property</span></span>     | <span data-ttu-id="afbe8-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="afbe8-122">Type</span></span>   |<span data-ttu-id="afbe8-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="afbe8-123">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="afbe8-124">color</span><span class="sxs-lookup"><span data-stu-id="afbe8-124">color</span></span>|<span data-ttu-id="afbe8-125">string</span><span class="sxs-lookup"><span data-stu-id="afbe8-125">string</span></span>|<span data-ttu-id="afbe8-126">Código de color HTML que representa el color de la línea de borde con el formato #RRGGBB (por ejemplo, "FFA500") o como un color HTML con nombre (por ejemplo, "naranja").</span><span class="sxs-lookup"><span data-stu-id="afbe8-126">HTML color code representing the color of the border line, of the form #RRGGBB (e.g. "FFA500") or as a named HTML color (e.g. "orange")</span></span>|

## <a name="relationships"></a><span data-ttu-id="afbe8-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="afbe8-127">Relationships</span></span>
<span data-ttu-id="afbe8-128">Ninguno</span><span class="sxs-lookup"><span data-stu-id="afbe8-128">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="afbe8-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="afbe8-129">JSON representation</span></span>

<span data-ttu-id="afbe8-130">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="afbe8-130">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.rangeFill"
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