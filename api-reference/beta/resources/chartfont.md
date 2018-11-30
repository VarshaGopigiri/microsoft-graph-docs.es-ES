---
title: Tipo de recurso ChartFont
description: Este objeto representa los atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) de un objeto de gráfico.
ms.openlocfilehash: a0aa3150cb6ad31b4ad635253fd6ae35647b5ff7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087062"
---
# <a name="chartfont-resource-type"></a><span data-ttu-id="b906f-103">Tipo de recurso ChartFont</span><span class="sxs-lookup"><span data-stu-id="b906f-103">ChartFont resource type</span></span>

> <span data-ttu-id="b906f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b906f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b906f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b906f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b906f-106">Este objeto representa los atributos de fuente (nombre de fuente, tamaño de fuente, color, etc.) de un objeto de gráfico.</span><span class="sxs-lookup"><span data-stu-id="b906f-106">This object represents the font attributes (font name, font size, color, etc.) for a chart object.</span></span>


## <a name="methods"></a><span data-ttu-id="b906f-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="b906f-107">Methods</span></span>

| <span data-ttu-id="b906f-108">Método</span><span class="sxs-lookup"><span data-stu-id="b906f-108">Method</span></span>           | <span data-ttu-id="b906f-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b906f-109">Return Type</span></span>    |<span data-ttu-id="b906f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b906f-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="b906f-111">Get ChartFont</span><span class="sxs-lookup"><span data-stu-id="b906f-111">Get ChartFont</span></span>](../api/chartfont-get.md) | [<span data-ttu-id="b906f-112">ChartFont</span><span class="sxs-lookup"><span data-stu-id="b906f-112">ChartFont</span></span>](chartfont.md) |<span data-ttu-id="b906f-113">Lee las propiedades y relaciones del objeto chartFont.</span><span class="sxs-lookup"><span data-stu-id="b906f-113">Read properties and relationships of chartFont object.</span></span>|
|[<span data-ttu-id="b906f-114">Update</span><span class="sxs-lookup"><span data-stu-id="b906f-114">Update</span></span>](../api/chartfont-update.md) | [<span data-ttu-id="b906f-115">ChartFont</span><span class="sxs-lookup"><span data-stu-id="b906f-115">ChartFont</span></span>](chartfont.md)   |<span data-ttu-id="b906f-116">Actualiza el objeto ChartFont.</span><span class="sxs-lookup"><span data-stu-id="b906f-116">Update ChartFont object.</span></span> |

## <a name="properties"></a><span data-ttu-id="b906f-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b906f-117">Properties</span></span>
| <span data-ttu-id="b906f-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b906f-118">Property</span></span>     | <span data-ttu-id="b906f-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="b906f-119">Type</span></span>   |<span data-ttu-id="b906f-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="b906f-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b906f-121">bold</span><span class="sxs-lookup"><span data-stu-id="b906f-121">bold</span></span>|<span data-ttu-id="b906f-122">boolean</span><span class="sxs-lookup"><span data-stu-id="b906f-122">boolean</span></span>|<span data-ttu-id="b906f-123">Representa el estado de negrita de la fuente.</span><span class="sxs-lookup"><span data-stu-id="b906f-123">Represents the bold status of font.</span></span>|
|<span data-ttu-id="b906f-124">color</span><span class="sxs-lookup"><span data-stu-id="b906f-124">color</span></span>|<span data-ttu-id="b906f-125">string</span><span class="sxs-lookup"><span data-stu-id="b906f-125">string</span></span>|<span data-ttu-id="b906f-p102">Representación del código de color HTML del color del texto. Por ejemplo, #FF0000 representa el rojo.</span><span class="sxs-lookup"><span data-stu-id="b906f-p102">HTML color code representation of the text color. E.g. #FF0000 represents Red.</span></span>|
|<span data-ttu-id="b906f-129">italic</span><span class="sxs-lookup"><span data-stu-id="b906f-129">italic</span></span>|<span data-ttu-id="b906f-130">boolean</span><span class="sxs-lookup"><span data-stu-id="b906f-130">boolean</span></span>|<span data-ttu-id="b906f-131">Representa el estado de cursiva de la fuente.</span><span class="sxs-lookup"><span data-stu-id="b906f-131">Represents the italic status of the font.</span></span>|
|<span data-ttu-id="b906f-132">name</span><span class="sxs-lookup"><span data-stu-id="b906f-132">name</span></span>|<span data-ttu-id="b906f-133">string</span><span class="sxs-lookup"><span data-stu-id="b906f-133">string</span></span>|<span data-ttu-id="b906f-134">Nombre de fuente (por ejemplo, "Calibri")</span><span class="sxs-lookup"><span data-stu-id="b906f-134">Font name (e.g. "Calibri")</span></span>|
|<span data-ttu-id="b906f-135">Tamaño</span><span class="sxs-lookup"><span data-stu-id="b906f-135">size</span></span>|<span data-ttu-id="b906f-136">Double</span><span class="sxs-lookup"><span data-stu-id="b906f-136">double</span></span>|<span data-ttu-id="b906f-137">Tamaño de la fuente (por ejemplo, 11).</span><span class="sxs-lookup"><span data-stu-id="b906f-137">Size of the font (e.g. 11)</span></span>|
|<span data-ttu-id="b906f-138">underline</span><span class="sxs-lookup"><span data-stu-id="b906f-138">underline</span></span>|<span data-ttu-id="b906f-139">string</span><span class="sxs-lookup"><span data-stu-id="b906f-139">string</span></span>|<span data-ttu-id="b906f-p103">Tipo de subrayado aplicado a la fuente. Valores posibles: `None`, `Single`.</span><span class="sxs-lookup"><span data-stu-id="b906f-p103">Type of underline applied to the font. Possible values are: `None`, `Single`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="b906f-142">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b906f-142">Relationships</span></span>
<span data-ttu-id="b906f-143">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b906f-143">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="b906f-144">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b906f-144">JSON representation</span></span>

<span data-ttu-id="b906f-145">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b906f-145">Here is a JSON representation of the resource.</span></span>

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