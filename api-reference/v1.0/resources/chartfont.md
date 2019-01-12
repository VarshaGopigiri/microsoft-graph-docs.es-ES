---
title: Tipo de recurso ChartFont
description: Este objeto representa los atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) de un objeto de gráfico.
localization_priority: Normal
author: lumine2008
ms.prod: excel
ms.openlocfilehash: 85a11d59e58d6968154a4ede12fa978b1f061de1
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27972792"
---
# <a name="chartfont-resource-type"></a><span data-ttu-id="20252-103">Tipo de recurso ChartFont</span><span class="sxs-lookup"><span data-stu-id="20252-103">ChartFont resource type</span></span>

<span data-ttu-id="20252-104">Este objeto representa los atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) de un objeto de gráfico.</span><span class="sxs-lookup"><span data-stu-id="20252-104">This object represents the font attributes (font name, font size, color, etc.) for a chart object.</span></span>


## <a name="methods"></a><span data-ttu-id="20252-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="20252-105">Methods</span></span>

| <span data-ttu-id="20252-106">Método</span><span class="sxs-lookup"><span data-stu-id="20252-106">Method</span></span>           | <span data-ttu-id="20252-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="20252-107">Return Type</span></span>    |<span data-ttu-id="20252-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="20252-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="20252-109">Get ChartFont</span><span class="sxs-lookup"><span data-stu-id="20252-109">Get ChartFont</span></span>](../api/chartfont-get.md) | [<span data-ttu-id="20252-110">WorkbookChartFont</span><span class="sxs-lookup"><span data-stu-id="20252-110">WorkbookChartFont</span></span>](chartfont.md) |<span data-ttu-id="20252-111">Lee las propiedades y relaciones del objeto chartFont.</span><span class="sxs-lookup"><span data-stu-id="20252-111">Read properties and relationships of chartFont object.</span></span>|
|[<span data-ttu-id="20252-112">Update</span><span class="sxs-lookup"><span data-stu-id="20252-112">Update</span></span>](../api/chartfont-update.md) | [<span data-ttu-id="20252-113">WorkbookChartFont</span><span class="sxs-lookup"><span data-stu-id="20252-113">WorkbookChartFont</span></span>](chartfont.md)   |<span data-ttu-id="20252-114">Actualiza el objeto ChartFont.</span><span class="sxs-lookup"><span data-stu-id="20252-114">Update ChartFont object.</span></span> |

## <a name="properties"></a><span data-ttu-id="20252-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="20252-115">Properties</span></span>
| <span data-ttu-id="20252-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="20252-116">Property</span></span>     | <span data-ttu-id="20252-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="20252-117">Type</span></span>   |<span data-ttu-id="20252-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="20252-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="20252-119">bold</span><span class="sxs-lookup"><span data-stu-id="20252-119">bold</span></span>|<span data-ttu-id="20252-120">boolean</span><span class="sxs-lookup"><span data-stu-id="20252-120">boolean</span></span>|<span data-ttu-id="20252-121">Representa el estado de negrita de la fuente.</span><span class="sxs-lookup"><span data-stu-id="20252-121">Represents the bold status of font.</span></span>|
|<span data-ttu-id="20252-122">color</span><span class="sxs-lookup"><span data-stu-id="20252-122">color</span></span>|<span data-ttu-id="20252-123">string</span><span class="sxs-lookup"><span data-stu-id="20252-123">string</span></span>|<span data-ttu-id="20252-p101">Representación del código de color HTML del color del texto. Por ejemplo, #FF0000 representa el rojo.</span><span class="sxs-lookup"><span data-stu-id="20252-p101">HTML color code representation of the text color. E.g. #FF0000 represents Red.</span></span>|
|<span data-ttu-id="20252-127">italic</span><span class="sxs-lookup"><span data-stu-id="20252-127">italic</span></span>|<span data-ttu-id="20252-128">boolean</span><span class="sxs-lookup"><span data-stu-id="20252-128">boolean</span></span>|<span data-ttu-id="20252-129">Representa el estado de cursiva de la fuente.</span><span class="sxs-lookup"><span data-stu-id="20252-129">Represents the italic status of the font.</span></span>|
|<span data-ttu-id="20252-130">name</span><span class="sxs-lookup"><span data-stu-id="20252-130">name</span></span>|<span data-ttu-id="20252-131">string</span><span class="sxs-lookup"><span data-stu-id="20252-131">string</span></span>|<span data-ttu-id="20252-132">Nombre de fuente (por ejemplo, "Calibri")</span><span class="sxs-lookup"><span data-stu-id="20252-132">Font name (e.g. "Calibri")</span></span>|
|<span data-ttu-id="20252-133">Tamaño</span><span class="sxs-lookup"><span data-stu-id="20252-133">size</span></span>|<span data-ttu-id="20252-134">Double</span><span class="sxs-lookup"><span data-stu-id="20252-134">double</span></span>|<span data-ttu-id="20252-135">Tamaño de la fuente (por ejemplo, 11).</span><span class="sxs-lookup"><span data-stu-id="20252-135">Size of the font (e.g. 11)</span></span>|
|<span data-ttu-id="20252-136">underline</span><span class="sxs-lookup"><span data-stu-id="20252-136">underline</span></span>|<span data-ttu-id="20252-137">string</span><span class="sxs-lookup"><span data-stu-id="20252-137">string</span></span>|<span data-ttu-id="20252-138">Tipo de subrayado aplicado a la fuente.</span><span class="sxs-lookup"><span data-stu-id="20252-138">Type of underline applied to the font.</span></span> <span data-ttu-id="20252-139">Los valores posibles son: `None`, `Single`.</span><span class="sxs-lookup"><span data-stu-id="20252-139">The possible values are: `None`, `Single`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="20252-140">Relaciones</span><span class="sxs-lookup"><span data-stu-id="20252-140">Relationships</span></span>
<span data-ttu-id="20252-141">Ninguno</span><span class="sxs-lookup"><span data-stu-id="20252-141">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="20252-142">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="20252-142">JSON representation</span></span>

<span data-ttu-id="20252-143">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="20252-143">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [],
  "@odata.type": "microsoft.graph.workbookChartFont"
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
  "description": "ChartFont resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
