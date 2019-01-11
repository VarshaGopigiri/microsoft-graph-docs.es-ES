---
title: Tipo de recurso RangeFont
description: Este objeto representa los atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) de un objeto.
localization_priority: Normal
ms.openlocfilehash: 32bbd29706966c4c4b15f038ebdbb872b1dd8193
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27856584"
---
# <a name="rangefont-resource-type"></a><span data-ttu-id="8bccc-103">Tipo de recurso RangeFont</span><span class="sxs-lookup"><span data-stu-id="8bccc-103">RangeFont resource type</span></span>

<span data-ttu-id="8bccc-104">Este objeto representa los atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) de un objeto.</span><span class="sxs-lookup"><span data-stu-id="8bccc-104">This object represents the font attributes (font name, font size, color, etc.) for an object.</span></span>


## <a name="methods"></a><span data-ttu-id="8bccc-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="8bccc-105">Methods</span></span>

| <span data-ttu-id="8bccc-106">Método</span><span class="sxs-lookup"><span data-stu-id="8bccc-106">Method</span></span>           | <span data-ttu-id="8bccc-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8bccc-107">Return Type</span></span>    |<span data-ttu-id="8bccc-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="8bccc-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="8bccc-109">Get RangeFont</span><span class="sxs-lookup"><span data-stu-id="8bccc-109">Get RangeFont</span></span>](../api/rangefont-get.md) | [<span data-ttu-id="8bccc-110">WorkbookRangeFont</span><span class="sxs-lookup"><span data-stu-id="8bccc-110">WorkbookRangeFont</span></span>](rangefont.md) |<span data-ttu-id="8bccc-111">Lee las propiedades y relaciones del objeto rangeFont.</span><span class="sxs-lookup"><span data-stu-id="8bccc-111">Read properties and relationships of rangeFont object.</span></span>|
|[<span data-ttu-id="8bccc-112">Update</span><span class="sxs-lookup"><span data-stu-id="8bccc-112">Update</span></span>](../api/rangefont-update.md) | [<span data-ttu-id="8bccc-113">WorkbookRangeFont</span><span class="sxs-lookup"><span data-stu-id="8bccc-113">WorkbookRangeFont</span></span>](rangefont.md)   |<span data-ttu-id="8bccc-114">Actualiza el objeto RangeFont.</span><span class="sxs-lookup"><span data-stu-id="8bccc-114">Update RangeFont object.</span></span> |

## <a name="properties"></a><span data-ttu-id="8bccc-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8bccc-115">Properties</span></span>
| <span data-ttu-id="8bccc-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8bccc-116">Property</span></span>     | <span data-ttu-id="8bccc-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="8bccc-117">Type</span></span>   |<span data-ttu-id="8bccc-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="8bccc-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8bccc-119">bold</span><span class="sxs-lookup"><span data-stu-id="8bccc-119">bold</span></span>|<span data-ttu-id="8bccc-120">boolean</span><span class="sxs-lookup"><span data-stu-id="8bccc-120">boolean</span></span>|<span data-ttu-id="8bccc-121">Representa el estado de negrita de la fuente.</span><span class="sxs-lookup"><span data-stu-id="8bccc-121">Represents the bold status of font.</span></span>|
|<span data-ttu-id="8bccc-122">color</span><span class="sxs-lookup"><span data-stu-id="8bccc-122">color</span></span>|<span data-ttu-id="8bccc-123">string</span><span class="sxs-lookup"><span data-stu-id="8bccc-123">string</span></span>|<span data-ttu-id="8bccc-p101">Representación del código de color HTML del color del texto. Por ejemplo, #FF0000 representa el rojo.</span><span class="sxs-lookup"><span data-stu-id="8bccc-p101">HTML color code representation of the text color. E.g. #FF0000 represents Red.</span></span>|
|<span data-ttu-id="8bccc-127">italic</span><span class="sxs-lookup"><span data-stu-id="8bccc-127">italic</span></span>|<span data-ttu-id="8bccc-128">boolean</span><span class="sxs-lookup"><span data-stu-id="8bccc-128">boolean</span></span>|<span data-ttu-id="8bccc-129">Representa el estado de cursiva de la fuente.</span><span class="sxs-lookup"><span data-stu-id="8bccc-129">Represents the italic status of the font.</span></span>|
|<span data-ttu-id="8bccc-130">name</span><span class="sxs-lookup"><span data-stu-id="8bccc-130">name</span></span>|<span data-ttu-id="8bccc-131">string</span><span class="sxs-lookup"><span data-stu-id="8bccc-131">string</span></span>|<span data-ttu-id="8bccc-132">Nombre de fuente (por ejemplo, "Calibri")</span><span class="sxs-lookup"><span data-stu-id="8bccc-132">Font name (e.g. "Calibri")</span></span>|
|<span data-ttu-id="8bccc-133">Tamaño</span><span class="sxs-lookup"><span data-stu-id="8bccc-133">size</span></span>|<span data-ttu-id="8bccc-134">Double</span><span class="sxs-lookup"><span data-stu-id="8bccc-134">double</span></span>|<span data-ttu-id="8bccc-135">Tamaño de fuente</span><span class="sxs-lookup"><span data-stu-id="8bccc-135">Font size.</span></span>|
|<span data-ttu-id="8bccc-136">underline</span><span class="sxs-lookup"><span data-stu-id="8bccc-136">underline</span></span>|<span data-ttu-id="8bccc-137">string</span><span class="sxs-lookup"><span data-stu-id="8bccc-137">string</span></span>|<span data-ttu-id="8bccc-138">Tipo de subrayado aplicado a la fuente.</span><span class="sxs-lookup"><span data-stu-id="8bccc-138">Type of underline applied to the font.</span></span> <span data-ttu-id="8bccc-139">Los valores posibles son: `None`, `Single`, `Double`, `SingleAccountant`, `DoubleAccountant`.</span><span class="sxs-lookup"><span data-stu-id="8bccc-139">The possible values are: `None`, `Single`, `Double`, `SingleAccountant`, `DoubleAccountant`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="8bccc-140">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8bccc-140">Relationships</span></span>
<span data-ttu-id="8bccc-141">Ninguno</span><span class="sxs-lookup"><span data-stu-id="8bccc-141">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="8bccc-142">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8bccc-142">JSON representation</span></span>

<span data-ttu-id="8bccc-143">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8bccc-143">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookRangeFont"
}-->

```json
{
  "bold": true,
  "color": "string",
  "italic": true,
  "name": "string",
  "size": 1024,
  "underline": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "RangeFont resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
