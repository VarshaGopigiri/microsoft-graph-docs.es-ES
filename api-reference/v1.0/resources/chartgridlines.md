---
title: Tipo de recurso ChartGridlines
description: Representa las líneas de cuadrícula principales o secundarias del eje de un gráfico.
ms.openlocfilehash: 352f2ff93b899a5321787a0f44b75188e671de27
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029454"
---
# <a name="chartgridlines-resource-type"></a><span data-ttu-id="71b1f-103">Tipo de recurso ChartGridlines</span><span class="sxs-lookup"><span data-stu-id="71b1f-103">ChartGridlines resource type</span></span>

<span data-ttu-id="71b1f-104">Representa las líneas de cuadrícula principales o secundarias del eje de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="71b1f-104">Represents major or minor gridlines on a chart axis.</span></span>


## <a name="methods"></a><span data-ttu-id="71b1f-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="71b1f-105">Methods</span></span>

| <span data-ttu-id="71b1f-106">Método</span><span class="sxs-lookup"><span data-stu-id="71b1f-106">Method</span></span>           | <span data-ttu-id="71b1f-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="71b1f-107">Return Type</span></span>    |<span data-ttu-id="71b1f-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="71b1f-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="71b1f-109">Get ChartGridlines</span><span class="sxs-lookup"><span data-stu-id="71b1f-109">Get ChartGridlines</span></span>](../api/chartgridlines-get.md) | [<span data-ttu-id="71b1f-110">WorkbookChartGridlines</span><span class="sxs-lookup"><span data-stu-id="71b1f-110">WorkbookChartGridlines</span></span>](chartgridlines.md) |<span data-ttu-id="71b1f-111">Lee las propiedades y relaciones del objeto chartGridlines.</span><span class="sxs-lookup"><span data-stu-id="71b1f-111">Read properties and relationships of chartGridlines object.</span></span>|
|[<span data-ttu-id="71b1f-112">Update</span><span class="sxs-lookup"><span data-stu-id="71b1f-112">Update</span></span>](../api/chartgridlines-update.md) | [<span data-ttu-id="71b1f-113">WorkbookChartGridlines</span><span class="sxs-lookup"><span data-stu-id="71b1f-113">WorkbookChartGridlines</span></span>](chartgridlines.md)    |<span data-ttu-id="71b1f-114">Actualiza el objeto ChartGridlines.</span><span class="sxs-lookup"><span data-stu-id="71b1f-114">Update ChartGridlines object.</span></span> |

## <a name="properties"></a><span data-ttu-id="71b1f-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="71b1f-115">Properties</span></span>
| <span data-ttu-id="71b1f-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="71b1f-116">Property</span></span>     | <span data-ttu-id="71b1f-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="71b1f-117">Type</span></span>   |<span data-ttu-id="71b1f-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="71b1f-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="71b1f-119">visible</span><span class="sxs-lookup"><span data-stu-id="71b1f-119">visible</span></span>|<span data-ttu-id="71b1f-120">boolean</span><span class="sxs-lookup"><span data-stu-id="71b1f-120">boolean</span></span>|<span data-ttu-id="71b1f-121">Valor booleano que representa si las líneas de cuadrícula del eje están visibles o no.</span><span class="sxs-lookup"><span data-stu-id="71b1f-121">Boolean value representing if the axis gridlines are visible or not.</span></span>|

## <a name="relationships"></a><span data-ttu-id="71b1f-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="71b1f-122">Relationships</span></span>
| <span data-ttu-id="71b1f-123">Relación</span><span class="sxs-lookup"><span data-stu-id="71b1f-123">Relationship</span></span> | <span data-ttu-id="71b1f-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="71b1f-124">Type</span></span>   |<span data-ttu-id="71b1f-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="71b1f-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="71b1f-126">format</span><span class="sxs-lookup"><span data-stu-id="71b1f-126">format</span></span>|[<span data-ttu-id="71b1f-127">WorkbookChartGridlinesFormat</span><span class="sxs-lookup"><span data-stu-id="71b1f-127">WorkbookChartGridlinesFormat</span></span>](chartgridlinesformat.md)|<span data-ttu-id="71b1f-p101">Representa el formato de las líneas de cuadrícula del gráfico. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="71b1f-p101">Represents the formatting of chart gridlines. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="71b1f-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="71b1f-130">JSON representation</span></span>

<span data-ttu-id="71b1f-131">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="71b1f-131">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookChartGridlines"
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