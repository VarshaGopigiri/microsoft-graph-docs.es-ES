---
title: Tipo de recurso ChartFont
description: Este objeto representa los atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) de un objeto de gráfico.
localization_priority: Normal
author: lumine2008
ms.prod: excel
ms.openlocfilehash: 4187d2837835520864ec3a1ef5c47b578b3d3da4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27920950"
---
# <a name="chartfont-resource-type"></a><span data-ttu-id="3f7c5-103">Tipo de recurso ChartFont</span><span class="sxs-lookup"><span data-stu-id="3f7c5-103">ChartFont resource type</span></span>

> <span data-ttu-id="3f7c5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3f7c5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3f7c5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3f7c5-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3f7c5-106">Este objeto representa los atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) de un objeto de gráfico.</span><span class="sxs-lookup"><span data-stu-id="3f7c5-106">This object represents the font attributes (font name, font size, color, etc.) for a chart object.</span></span>


## <a name="methods"></a><span data-ttu-id="3f7c5-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="3f7c5-107">Methods</span></span>

| <span data-ttu-id="3f7c5-108">Método</span><span class="sxs-lookup"><span data-stu-id="3f7c5-108">Method</span></span>           | <span data-ttu-id="3f7c5-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f7c5-109">Return Type</span></span>    |<span data-ttu-id="3f7c5-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f7c5-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="3f7c5-111">Get ChartFont</span><span class="sxs-lookup"><span data-stu-id="3f7c5-111">Get ChartFont</span></span>](../api/chartfont-get.md) | [<span data-ttu-id="3f7c5-112">ChartFont</span><span class="sxs-lookup"><span data-stu-id="3f7c5-112">ChartFont</span></span>](chartfont.md) |<span data-ttu-id="3f7c5-113">Lee las propiedades y relaciones del objeto chartFont.</span><span class="sxs-lookup"><span data-stu-id="3f7c5-113">Read properties and relationships of chartFont object.</span></span>|
|[<span data-ttu-id="3f7c5-114">Update</span><span class="sxs-lookup"><span data-stu-id="3f7c5-114">Update</span></span>](../api/chartfont-update.md) | [<span data-ttu-id="3f7c5-115">ChartFont</span><span class="sxs-lookup"><span data-stu-id="3f7c5-115">ChartFont</span></span>](chartfont.md)   |<span data-ttu-id="3f7c5-116">Actualiza el objeto ChartFont.</span><span class="sxs-lookup"><span data-stu-id="3f7c5-116">Update ChartFont object.</span></span> |

## <a name="properties"></a><span data-ttu-id="3f7c5-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3f7c5-117">Properties</span></span>
| <span data-ttu-id="3f7c5-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3f7c5-118">Property</span></span>     | <span data-ttu-id="3f7c5-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="3f7c5-119">Type</span></span>   |<span data-ttu-id="3f7c5-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f7c5-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3f7c5-121">bold</span><span class="sxs-lookup"><span data-stu-id="3f7c5-121">bold</span></span>|<span data-ttu-id="3f7c5-122">boolean</span><span class="sxs-lookup"><span data-stu-id="3f7c5-122">boolean</span></span>|<span data-ttu-id="3f7c5-123">Representa el estado de negrita de la fuente.</span><span class="sxs-lookup"><span data-stu-id="3f7c5-123">Represents the bold status of font.</span></span>|
|<span data-ttu-id="3f7c5-124">color</span><span class="sxs-lookup"><span data-stu-id="3f7c5-124">color</span></span>|<span data-ttu-id="3f7c5-125">string</span><span class="sxs-lookup"><span data-stu-id="3f7c5-125">string</span></span>|<span data-ttu-id="3f7c5-p102">Representación del código de color HTML del color del texto. Por ejemplo, #FF0000 representa el rojo.</span><span class="sxs-lookup"><span data-stu-id="3f7c5-p102">HTML color code representation of the text color. E.g. #FF0000 represents Red.</span></span>|
|<span data-ttu-id="3f7c5-129">italic</span><span class="sxs-lookup"><span data-stu-id="3f7c5-129">italic</span></span>|<span data-ttu-id="3f7c5-130">boolean</span><span class="sxs-lookup"><span data-stu-id="3f7c5-130">boolean</span></span>|<span data-ttu-id="3f7c5-131">Representa el estado de cursiva de la fuente.</span><span class="sxs-lookup"><span data-stu-id="3f7c5-131">Represents the italic status of the font.</span></span>|
|<span data-ttu-id="3f7c5-132">name</span><span class="sxs-lookup"><span data-stu-id="3f7c5-132">name</span></span>|<span data-ttu-id="3f7c5-133">string</span><span class="sxs-lookup"><span data-stu-id="3f7c5-133">string</span></span>|<span data-ttu-id="3f7c5-134">Nombre de fuente (por ejemplo, "Calibri")</span><span class="sxs-lookup"><span data-stu-id="3f7c5-134">Font name (e.g. "Calibri")</span></span>|
|<span data-ttu-id="3f7c5-135">Tamaño</span><span class="sxs-lookup"><span data-stu-id="3f7c5-135">size</span></span>|<span data-ttu-id="3f7c5-136">Double</span><span class="sxs-lookup"><span data-stu-id="3f7c5-136">double</span></span>|<span data-ttu-id="3f7c5-137">Tamaño de la fuente (por ejemplo, 11).</span><span class="sxs-lookup"><span data-stu-id="3f7c5-137">Size of the font (e.g. 11)</span></span>|
|<span data-ttu-id="3f7c5-138">underline</span><span class="sxs-lookup"><span data-stu-id="3f7c5-138">underline</span></span>|<span data-ttu-id="3f7c5-139">string</span><span class="sxs-lookup"><span data-stu-id="3f7c5-139">string</span></span>|<span data-ttu-id="3f7c5-p103">Tipo de subrayado aplicado a la fuente. Valores posibles: `None`, `Single`.</span><span class="sxs-lookup"><span data-stu-id="3f7c5-p103">Type of underline applied to the font. Possible values are: `None`, `Single`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="3f7c5-142">Relaciones</span><span class="sxs-lookup"><span data-stu-id="3f7c5-142">Relationships</span></span>
<span data-ttu-id="3f7c5-143">Ninguno</span><span class="sxs-lookup"><span data-stu-id="3f7c5-143">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="3f7c5-144">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3f7c5-144">JSON representation</span></span>

<span data-ttu-id="3f7c5-145">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="3f7c5-145">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chartFont"
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
