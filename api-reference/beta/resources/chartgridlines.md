---
title: Tipo de recurso ChartGridlines
description: Representa las líneas de cuadrícula principales o secundarias del eje de un gráfico.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 7747564b2f72287ef6ec2c6cc1f912695f58218e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27807829"
---
# <a name="chartgridlines-resource-type"></a><span data-ttu-id="75d78-103">Tipo de recurso ChartGridlines</span><span class="sxs-lookup"><span data-stu-id="75d78-103">ChartGridlines resource type</span></span>

> <span data-ttu-id="75d78-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="75d78-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="75d78-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="75d78-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="75d78-106">Representa las líneas de división principales o secundarias del eje de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="75d78-106">Represents major or minor gridlines on a chart axis.</span></span>


## <a name="methods"></a><span data-ttu-id="75d78-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="75d78-107">Methods</span></span>

| <span data-ttu-id="75d78-108">Método</span><span class="sxs-lookup"><span data-stu-id="75d78-108">Method</span></span>           | <span data-ttu-id="75d78-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75d78-109">Return Type</span></span>    |<span data-ttu-id="75d78-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="75d78-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="75d78-111">Get ChartGridlines</span><span class="sxs-lookup"><span data-stu-id="75d78-111">Get ChartGridlines</span></span>](../api/chartgridlines-get.md) | [<span data-ttu-id="75d78-112">ChartGridlines</span><span class="sxs-lookup"><span data-stu-id="75d78-112">ChartGridlines</span></span>](chartgridlines.md) |<span data-ttu-id="75d78-113">Lee las propiedades y relaciones del objeto chartGridlines.</span><span class="sxs-lookup"><span data-stu-id="75d78-113">Read properties and relationships of chartGridlines object.</span></span>|
|[<span data-ttu-id="75d78-114">Update</span><span class="sxs-lookup"><span data-stu-id="75d78-114">Update</span></span>](../api/chartgridlines-update.md) | [<span data-ttu-id="75d78-115">ChartGridlines</span><span class="sxs-lookup"><span data-stu-id="75d78-115">ChartGridlines</span></span>](chartgridlines.md)    |<span data-ttu-id="75d78-116">Actualiza el objeto ChartGridlines.</span><span class="sxs-lookup"><span data-stu-id="75d78-116">Update ChartGridlines object.</span></span> |

## <a name="properties"></a><span data-ttu-id="75d78-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="75d78-117">Properties</span></span>
| <span data-ttu-id="75d78-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="75d78-118">Property</span></span>     | <span data-ttu-id="75d78-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="75d78-119">Type</span></span>   |<span data-ttu-id="75d78-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="75d78-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="75d78-121">visible</span><span class="sxs-lookup"><span data-stu-id="75d78-121">visible</span></span>|<span data-ttu-id="75d78-122">boolean</span><span class="sxs-lookup"><span data-stu-id="75d78-122">boolean</span></span>|<span data-ttu-id="75d78-123">Valor booleano que representa si las líneas de cuadrícula del eje están visibles o no.</span><span class="sxs-lookup"><span data-stu-id="75d78-123">Boolean value representing if the axis gridlines are visible or not.</span></span>|

## <a name="relationships"></a><span data-ttu-id="75d78-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="75d78-124">Relationships</span></span>
| <span data-ttu-id="75d78-125">Relación</span><span class="sxs-lookup"><span data-stu-id="75d78-125">Relationship</span></span> | <span data-ttu-id="75d78-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="75d78-126">Type</span></span>   |<span data-ttu-id="75d78-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="75d78-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="75d78-128">format</span><span class="sxs-lookup"><span data-stu-id="75d78-128">format</span></span>|[<span data-ttu-id="75d78-129">ChartGridlinesFormat</span><span class="sxs-lookup"><span data-stu-id="75d78-129">ChartGridlinesFormat</span></span>](chartgridlinesformat.md)|<span data-ttu-id="75d78-p102">Representa el formato de las líneas de cuadrícula del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="75d78-p102">Represents the formatting of chart gridlines. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="75d78-132">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="75d78-132">JSON representation</span></span>

<span data-ttu-id="75d78-133">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="75d78-133">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chartGridLines"
}-->

```json
{
  "visible": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartGridlines resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
