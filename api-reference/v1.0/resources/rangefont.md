---
title: Tipo de recurso RangeFont
description: Este objeto representa los atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) de un objeto.
localization_priority: Normal
author: lumine2008
ms.prod: excel
ms.openlocfilehash: 829b391d561aae63ae94972c55039acfdf4c48d7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27962300"
---
# <a name="rangefont-resource-type"></a><span data-ttu-id="9e28f-103">Tipo de recurso RangeFont</span><span class="sxs-lookup"><span data-stu-id="9e28f-103">RangeFont resource type</span></span>

<span data-ttu-id="9e28f-104">Este objeto representa los atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) de un objeto.</span><span class="sxs-lookup"><span data-stu-id="9e28f-104">This object represents the font attributes (font name, font size, color, etc.) for an object.</span></span>


## <a name="methods"></a><span data-ttu-id="9e28f-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="9e28f-105">Methods</span></span>

| <span data-ttu-id="9e28f-106">Método</span><span class="sxs-lookup"><span data-stu-id="9e28f-106">Method</span></span>           | <span data-ttu-id="9e28f-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9e28f-107">Return Type</span></span>    |<span data-ttu-id="9e28f-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e28f-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="9e28f-109">Get RangeFont</span><span class="sxs-lookup"><span data-stu-id="9e28f-109">Get RangeFont</span></span>](../api/rangefont-get.md) | [<span data-ttu-id="9e28f-110">WorkbookRangeFont</span><span class="sxs-lookup"><span data-stu-id="9e28f-110">WorkbookRangeFont</span></span>](rangefont.md) |<span data-ttu-id="9e28f-111">Lee las propiedades y relaciones del objeto rangeFont.</span><span class="sxs-lookup"><span data-stu-id="9e28f-111">Read properties and relationships of rangeFont object.</span></span>|
|[<span data-ttu-id="9e28f-112">Update</span><span class="sxs-lookup"><span data-stu-id="9e28f-112">Update</span></span>](../api/rangefont-update.md) | [<span data-ttu-id="9e28f-113">WorkbookRangeFont</span><span class="sxs-lookup"><span data-stu-id="9e28f-113">WorkbookRangeFont</span></span>](rangefont.md)   |<span data-ttu-id="9e28f-114">Actualiza el objeto RangeFont.</span><span class="sxs-lookup"><span data-stu-id="9e28f-114">Update RangeFont object.</span></span> |

## <a name="properties"></a><span data-ttu-id="9e28f-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9e28f-115">Properties</span></span>
| <span data-ttu-id="9e28f-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9e28f-116">Property</span></span>     | <span data-ttu-id="9e28f-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="9e28f-117">Type</span></span>   |<span data-ttu-id="9e28f-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e28f-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9e28f-119">bold</span><span class="sxs-lookup"><span data-stu-id="9e28f-119">bold</span></span>|<span data-ttu-id="9e28f-120">boolean</span><span class="sxs-lookup"><span data-stu-id="9e28f-120">boolean</span></span>|<span data-ttu-id="9e28f-121">Representa el estado de negrita de la fuente.</span><span class="sxs-lookup"><span data-stu-id="9e28f-121">Represents the bold status of font.</span></span>|
|<span data-ttu-id="9e28f-122">color</span><span class="sxs-lookup"><span data-stu-id="9e28f-122">color</span></span>|<span data-ttu-id="9e28f-123">string</span><span class="sxs-lookup"><span data-stu-id="9e28f-123">string</span></span>|<span data-ttu-id="9e28f-p101">Representación del código de color HTML del color del texto. Por ejemplo, #FF0000 representa el rojo.</span><span class="sxs-lookup"><span data-stu-id="9e28f-p101">HTML color code representation of the text color. E.g. #FF0000 represents Red.</span></span>|
|<span data-ttu-id="9e28f-127">italic</span><span class="sxs-lookup"><span data-stu-id="9e28f-127">italic</span></span>|<span data-ttu-id="9e28f-128">boolean</span><span class="sxs-lookup"><span data-stu-id="9e28f-128">boolean</span></span>|<span data-ttu-id="9e28f-129">Representa el estado de cursiva de la fuente.</span><span class="sxs-lookup"><span data-stu-id="9e28f-129">Represents the italic status of the font.</span></span>|
|<span data-ttu-id="9e28f-130">name</span><span class="sxs-lookup"><span data-stu-id="9e28f-130">name</span></span>|<span data-ttu-id="9e28f-131">string</span><span class="sxs-lookup"><span data-stu-id="9e28f-131">string</span></span>|<span data-ttu-id="9e28f-132">Nombre de fuente (por ejemplo, "Calibri")</span><span class="sxs-lookup"><span data-stu-id="9e28f-132">Font name (e.g. "Calibri")</span></span>|
|<span data-ttu-id="9e28f-133">Tamaño</span><span class="sxs-lookup"><span data-stu-id="9e28f-133">size</span></span>|<span data-ttu-id="9e28f-134">Double</span><span class="sxs-lookup"><span data-stu-id="9e28f-134">double</span></span>|<span data-ttu-id="9e28f-135">Tamaño de fuente</span><span class="sxs-lookup"><span data-stu-id="9e28f-135">Font size.</span></span>|
|<span data-ttu-id="9e28f-136">underline</span><span class="sxs-lookup"><span data-stu-id="9e28f-136">underline</span></span>|<span data-ttu-id="9e28f-137">string</span><span class="sxs-lookup"><span data-stu-id="9e28f-137">string</span></span>|<span data-ttu-id="9e28f-138">Tipo de subrayado aplicado a la fuente.</span><span class="sxs-lookup"><span data-stu-id="9e28f-138">Type of underline applied to the font.</span></span> <span data-ttu-id="9e28f-139">Los valores posibles son: `None`, `Single`, `Double`, `SingleAccountant`, `DoubleAccountant`.</span><span class="sxs-lookup"><span data-stu-id="9e28f-139">The possible values are: `None`, `Single`, `Double`, `SingleAccountant`, `DoubleAccountant`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="9e28f-140">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9e28f-140">Relationships</span></span>
<span data-ttu-id="9e28f-141">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9e28f-141">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="9e28f-142">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9e28f-142">JSON representation</span></span>

<span data-ttu-id="9e28f-143">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="9e28f-143">Here is a JSON representation of the resource.</span></span>

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
