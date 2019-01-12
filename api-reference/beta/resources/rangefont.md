---
title: Tipo de recurso RangeFont
description: Este objeto representa los atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) de un objeto.
localization_priority: Normal
author: lumine2008
ms.prod: excel
ms.openlocfilehash: e6f448df142ffdc0c20e39045b4cd77a6c224a6f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27912781"
---
# <a name="rangefont-resource-type"></a><span data-ttu-id="78208-103">Tipo de recurso RangeFont</span><span class="sxs-lookup"><span data-stu-id="78208-103">RangeFont resource type</span></span>

> <span data-ttu-id="78208-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="78208-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="78208-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="78208-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="78208-106">Este objeto representa los atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) de un objeto.</span><span class="sxs-lookup"><span data-stu-id="78208-106">This object represents the font attributes (font name, font size, color, etc.) for an object.</span></span>


## <a name="methods"></a><span data-ttu-id="78208-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="78208-107">Methods</span></span>

| <span data-ttu-id="78208-108">Método</span><span class="sxs-lookup"><span data-stu-id="78208-108">Method</span></span>           | <span data-ttu-id="78208-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="78208-109">Return Type</span></span>    |<span data-ttu-id="78208-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="78208-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="78208-111">Get RangeFont</span><span class="sxs-lookup"><span data-stu-id="78208-111">Get RangeFont</span></span>](../api/rangefont-get.md) | [<span data-ttu-id="78208-112">RangeFont</span><span class="sxs-lookup"><span data-stu-id="78208-112">RangeFont</span></span>](rangefont.md) |<span data-ttu-id="78208-113">Lee las propiedades y relaciones del objeto rangeFont.</span><span class="sxs-lookup"><span data-stu-id="78208-113">Read properties and relationships of rangeFont object.</span></span>|
|[<span data-ttu-id="78208-114">Update</span><span class="sxs-lookup"><span data-stu-id="78208-114">Update</span></span>](../api/rangefont-update.md) | [<span data-ttu-id="78208-115">RangeFont</span><span class="sxs-lookup"><span data-stu-id="78208-115">RangeFont</span></span>](rangefont.md)   |<span data-ttu-id="78208-116">Actualiza el objeto RangeFont.</span><span class="sxs-lookup"><span data-stu-id="78208-116">Update RangeFont object.</span></span> |

## <a name="properties"></a><span data-ttu-id="78208-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="78208-117">Properties</span></span>
| <span data-ttu-id="78208-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="78208-118">Property</span></span>     | <span data-ttu-id="78208-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="78208-119">Type</span></span>   |<span data-ttu-id="78208-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="78208-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="78208-121">bold</span><span class="sxs-lookup"><span data-stu-id="78208-121">bold</span></span>|<span data-ttu-id="78208-122">boolean</span><span class="sxs-lookup"><span data-stu-id="78208-122">boolean</span></span>|<span data-ttu-id="78208-123">Representa el estado de negrita de la fuente.</span><span class="sxs-lookup"><span data-stu-id="78208-123">Represents the bold status of font.</span></span>|
|<span data-ttu-id="78208-124">color</span><span class="sxs-lookup"><span data-stu-id="78208-124">color</span></span>|<span data-ttu-id="78208-125">string</span><span class="sxs-lookup"><span data-stu-id="78208-125">string</span></span>|<span data-ttu-id="78208-p102">Representación del código de color HTML del color del texto. Por ejemplo, #FF0000 representa el rojo.</span><span class="sxs-lookup"><span data-stu-id="78208-p102">HTML color code representation of the text color. E.g. #FF0000 represents Red.</span></span>|
|<span data-ttu-id="78208-129">italic</span><span class="sxs-lookup"><span data-stu-id="78208-129">italic</span></span>|<span data-ttu-id="78208-130">boolean</span><span class="sxs-lookup"><span data-stu-id="78208-130">boolean</span></span>|<span data-ttu-id="78208-131">Representa el estado de cursiva de la fuente.</span><span class="sxs-lookup"><span data-stu-id="78208-131">Represents the italic status of the font.</span></span>|
|<span data-ttu-id="78208-132">name</span><span class="sxs-lookup"><span data-stu-id="78208-132">name</span></span>|<span data-ttu-id="78208-133">string</span><span class="sxs-lookup"><span data-stu-id="78208-133">string</span></span>|<span data-ttu-id="78208-134">Nombre de fuente (por ejemplo, "Calibri")</span><span class="sxs-lookup"><span data-stu-id="78208-134">Font name (e.g. "Calibri")</span></span>|
|<span data-ttu-id="78208-135">Tamaño</span><span class="sxs-lookup"><span data-stu-id="78208-135">size</span></span>|<span data-ttu-id="78208-136">Double</span><span class="sxs-lookup"><span data-stu-id="78208-136">double</span></span>|<span data-ttu-id="78208-137">Tamaño de fuente</span><span class="sxs-lookup"><span data-stu-id="78208-137">Font size.</span></span>|
|<span data-ttu-id="78208-138">underline</span><span class="sxs-lookup"><span data-stu-id="78208-138">underline</span></span>|<span data-ttu-id="78208-139">string</span><span class="sxs-lookup"><span data-stu-id="78208-139">string</span></span>|<span data-ttu-id="78208-p103">Tipo de subrayado aplicado a la fuente. Valores posibles: `None`, `Single`, `Double`, `SingleAccountant`, `DoubleAccountant`.</span><span class="sxs-lookup"><span data-stu-id="78208-p103">Type of underline applied to the font. Possible values are: `None`, `Single`, `Double`, `SingleAccountant`, `DoubleAccountant`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="78208-142">Relaciones</span><span class="sxs-lookup"><span data-stu-id="78208-142">Relationships</span></span>
<span data-ttu-id="78208-143">Ninguno</span><span class="sxs-lookup"><span data-stu-id="78208-143">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="78208-144">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="78208-144">JSON representation</span></span>

<span data-ttu-id="78208-145">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="78208-145">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.rangeFont"
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
