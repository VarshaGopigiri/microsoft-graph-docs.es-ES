---
title: Tipo de recurso ChartLineFormat
description: Encapsula las opciones de formato para los elementos de línea.
author: lumine2008
ms.openlocfilehash: be9d0d3f30deb608aee9873866442e0478c0056a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27352188"
---
# <a name="chartlineformat-resource-type"></a><span data-ttu-id="ad7fc-103">Tipo de recurso ChartLineFormat</span><span class="sxs-lookup"><span data-stu-id="ad7fc-103">ChartLineFormat resource type</span></span>

> <span data-ttu-id="ad7fc-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ad7fc-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ad7fc-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ad7fc-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ad7fc-106">Encapsula las opciones de formato para los elementos de línea.</span><span class="sxs-lookup"><span data-stu-id="ad7fc-106">Enapsulates the formatting options for line elements.</span></span>


## <a name="methods"></a><span data-ttu-id="ad7fc-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="ad7fc-107">Methods</span></span>

| <span data-ttu-id="ad7fc-108">Método</span><span class="sxs-lookup"><span data-stu-id="ad7fc-108">Method</span></span>           | <span data-ttu-id="ad7fc-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad7fc-109">Return Type</span></span>    |<span data-ttu-id="ad7fc-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad7fc-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="ad7fc-111">Get ChartLineFormat</span><span class="sxs-lookup"><span data-stu-id="ad7fc-111">Get ChartLineFormat</span></span>](../api/chartlineformat-get.md) | [<span data-ttu-id="ad7fc-112">ChartLineFormat</span><span class="sxs-lookup"><span data-stu-id="ad7fc-112">ChartLineFormat</span></span>](chartlineformat.md) |<span data-ttu-id="ad7fc-113">Lee las propiedades y relaciones del objeto chartLineFormat.</span><span class="sxs-lookup"><span data-stu-id="ad7fc-113">Read properties and relationships of chartLineFormat object.</span></span>|
|[<span data-ttu-id="ad7fc-114">Actualizar</span><span class="sxs-lookup"><span data-stu-id="ad7fc-114">Update</span></span>](../api/chartlineformat-update.md) | [<span data-ttu-id="ad7fc-115">ChartLineFormat</span><span class="sxs-lookup"><span data-stu-id="ad7fc-115">ChartLineFormat</span></span>](chartlineformat.md) |<span data-ttu-id="ad7fc-116">Actualiza el objeto ChartLineFormat.</span><span class="sxs-lookup"><span data-stu-id="ad7fc-116">Update ChartLineFormat object.</span></span> |
|[<span data-ttu-id="ad7fc-117">Clear</span><span class="sxs-lookup"><span data-stu-id="ad7fc-117">Clear</span></span>](../api/chartlineformat-clear.md)|<span data-ttu-id="ad7fc-118">None</span><span class="sxs-lookup"><span data-stu-id="ad7fc-118">None</span></span>|<span data-ttu-id="ad7fc-119">Borra el formato de línea de un elemento de gráfico.</span><span class="sxs-lookup"><span data-stu-id="ad7fc-119">Clear the line format of a chart element.</span></span>|

## <a name="properties"></a><span data-ttu-id="ad7fc-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ad7fc-120">Properties</span></span>
| <span data-ttu-id="ad7fc-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ad7fc-121">Property</span></span>     | <span data-ttu-id="ad7fc-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="ad7fc-122">Type</span></span>   |<span data-ttu-id="ad7fc-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad7fc-123">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ad7fc-124">color</span><span class="sxs-lookup"><span data-stu-id="ad7fc-124">color</span></span>|<span data-ttu-id="ad7fc-125">string</span><span class="sxs-lookup"><span data-stu-id="ad7fc-125">string</span></span>|<span data-ttu-id="ad7fc-126">Código de color HTML que representa el color de las líneas del gráfico.</span><span class="sxs-lookup"><span data-stu-id="ad7fc-126">HTML color code representing the color of lines in the chart.</span></span>|

## <a name="relationships"></a><span data-ttu-id="ad7fc-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ad7fc-127">Relationships</span></span>
<span data-ttu-id="ad7fc-128">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ad7fc-128">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="ad7fc-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ad7fc-129">JSON representation</span></span>

<span data-ttu-id="ad7fc-130">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ad7fc-130">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chartLineFormat"
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
  "description": "ChartLineFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->