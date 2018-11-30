---
title: Tipo de recurso ChartAxisTitle
description: Representa el título del eje de un gráfico.
ms.openlocfilehash: 83d3712367b3c56b2fe30e7e1e464491b77fbee5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088342"
---
# <a name="chartaxistitle-resource-type"></a><span data-ttu-id="34c64-103">Tipo de recurso ChartAxisTitle</span><span class="sxs-lookup"><span data-stu-id="34c64-103">ChartAxisTitle resource type</span></span>

> <span data-ttu-id="34c64-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="34c64-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="34c64-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="34c64-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="34c64-106">Representa el título del eje de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="34c64-106">Represents the title of a chart axis.</span></span>


## <a name="methods"></a><span data-ttu-id="34c64-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="34c64-107">Methods</span></span>

| <span data-ttu-id="34c64-108">Método</span><span class="sxs-lookup"><span data-stu-id="34c64-108">Method</span></span>           | <span data-ttu-id="34c64-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="34c64-109">Return Type</span></span>    |<span data-ttu-id="34c64-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="34c64-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="34c64-111">Get ChartAxisTitle</span><span class="sxs-lookup"><span data-stu-id="34c64-111">Get ChartAxisTitle</span></span>](../api/chartaxistitle-get.md) | [<span data-ttu-id="34c64-112">ChartAxisTitle</span><span class="sxs-lookup"><span data-stu-id="34c64-112">ChartAxisTitle</span></span>](chartaxistitle.md) |<span data-ttu-id="34c64-113">Lee las propiedades y relaciones del objeto chartAxisTitle.</span><span class="sxs-lookup"><span data-stu-id="34c64-113">Read properties and relationships of chartAxisTitle object.</span></span>|
|[<span data-ttu-id="34c64-114">Update</span><span class="sxs-lookup"><span data-stu-id="34c64-114">Update</span></span>](../api/chartaxistitle-update.md) | [<span data-ttu-id="34c64-115">ChartAxisTitle</span><span class="sxs-lookup"><span data-stu-id="34c64-115">ChartAxisTitle</span></span>](chartaxistitle.md)    |<span data-ttu-id="34c64-116">Actualiza el objeto ChartAxisTitle.</span><span class="sxs-lookup"><span data-stu-id="34c64-116">Update ChartAxisTitle object.</span></span> |

## <a name="properties"></a><span data-ttu-id="34c64-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="34c64-117">Properties</span></span>
| <span data-ttu-id="34c64-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="34c64-118">Property</span></span>     | <span data-ttu-id="34c64-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="34c64-119">Type</span></span>   |<span data-ttu-id="34c64-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="34c64-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="34c64-121">text</span><span class="sxs-lookup"><span data-stu-id="34c64-121">text</span></span>|<span data-ttu-id="34c64-122">string</span><span class="sxs-lookup"><span data-stu-id="34c64-122">string</span></span>|<span data-ttu-id="34c64-123">Representa el título del eje.</span><span class="sxs-lookup"><span data-stu-id="34c64-123">Represents the axis title.</span></span>|
|<span data-ttu-id="34c64-124">visible</span><span class="sxs-lookup"><span data-stu-id="34c64-124">visible</span></span>|<span data-ttu-id="34c64-125">boolean</span><span class="sxs-lookup"><span data-stu-id="34c64-125">boolean</span></span>|<span data-ttu-id="34c64-126">Valor booleano que especifica la visibilidad del título de un eje.</span><span class="sxs-lookup"><span data-stu-id="34c64-126">A boolean that specifies the visibility of an axis title.</span></span>|

## <a name="relationships"></a><span data-ttu-id="34c64-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="34c64-127">Relationships</span></span>
| <span data-ttu-id="34c64-128">Relación</span><span class="sxs-lookup"><span data-stu-id="34c64-128">Relationship</span></span> | <span data-ttu-id="34c64-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="34c64-129">Type</span></span>   |<span data-ttu-id="34c64-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="34c64-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="34c64-131">format</span><span class="sxs-lookup"><span data-stu-id="34c64-131">format</span></span>|[<span data-ttu-id="34c64-132">ChartAxisTitleFormat</span><span class="sxs-lookup"><span data-stu-id="34c64-132">ChartAxisTitleFormat</span></span>](chartaxistitleformat.md)|<span data-ttu-id="34c64-p102">Representa el formato del título del eje del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="34c64-p102">Represents the formatting of chart axis title. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="34c64-135">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="34c64-135">JSON representation</span></span>

<span data-ttu-id="34c64-136">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="34c64-136">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chartAxisTitle"
}-->

```json
{
  "text": "string",
  "visible": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartAxisTitle resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->