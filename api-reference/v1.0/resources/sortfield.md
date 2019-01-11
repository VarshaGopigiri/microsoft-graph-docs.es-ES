---
title: Tipo de recurso SortField
description: Representa una condición en una operación de ordenación.
localization_priority: Normal
ms.openlocfilehash: 2c1b9a272fd024455d1297c5f59ca7684283e1a1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27825973"
---
# <a name="sortfield-resource-type"></a><span data-ttu-id="ef064-103">Tipo de recurso SortField</span><span class="sxs-lookup"><span data-stu-id="ef064-103">SortField resource type</span></span>

<span data-ttu-id="ef064-104">Representa una condición en una operación de ordenación.</span><span class="sxs-lookup"><span data-stu-id="ef064-104">Represents a condition in a sorting operation.</span></span>

## <a name="properties"></a><span data-ttu-id="ef064-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ef064-105">Properties</span></span>
| <span data-ttu-id="ef064-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ef064-106">Property</span></span>     | <span data-ttu-id="ef064-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="ef064-107">Type</span></span>   |<span data-ttu-id="ef064-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ef064-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ef064-109">ascending</span><span class="sxs-lookup"><span data-stu-id="ef064-109">ascending</span></span>|<span data-ttu-id="ef064-110">boolean</span><span class="sxs-lookup"><span data-stu-id="ef064-110">boolean</span></span>|<span data-ttu-id="ef064-111">Representa si la ordenación se realiza en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="ef064-111">Represents whether the sorting is done in an ascending fashion.</span></span>|
|<span data-ttu-id="ef064-112">color</span><span class="sxs-lookup"><span data-stu-id="ef064-112">color</span></span>|<span data-ttu-id="ef064-113">string</span><span class="sxs-lookup"><span data-stu-id="ef064-113">string</span></span>|<span data-ttu-id="ef064-114">Representa el color que es el destino de la condición si la ordenación se realiza según la fuente o el color de celda.</span><span class="sxs-lookup"><span data-stu-id="ef064-114">Represents the color that is the target of the condition if the sorting is on font or cell color.</span></span>|
|<span data-ttu-id="ef064-115">dataOption</span><span class="sxs-lookup"><span data-stu-id="ef064-115">dataOption</span></span>|<span data-ttu-id="ef064-116">string</span><span class="sxs-lookup"><span data-stu-id="ef064-116">string</span></span>|<span data-ttu-id="ef064-117">Representa las opciones de ordenación adicionales para este campo.</span><span class="sxs-lookup"><span data-stu-id="ef064-117">Represents additional sorting options for this field.</span></span> <span data-ttu-id="ef064-118">Los valores posibles son: `Normal`, `TextAsNumber`.</span><span class="sxs-lookup"><span data-stu-id="ef064-118">The possible values are: `Normal`, `TextAsNumber`.</span></span>|
|<span data-ttu-id="ef064-119">Key</span><span class="sxs-lookup"><span data-stu-id="ef064-119">key</span></span>|<span data-ttu-id="ef064-120">int</span><span class="sxs-lookup"><span data-stu-id="ef064-120">int</span></span>|<span data-ttu-id="ef064-p102">Representa la columna (o fila, según la orientación de ordenación) en que se encuentra la condición. Se representa como un desplazamiento de la primera columna (o fila).</span><span class="sxs-lookup"><span data-stu-id="ef064-p102">Represents the column (or row, depending on the sort orientation) that the condition is on. Represented as an offset from the first column (or row).</span></span>|
|<span data-ttu-id="ef064-123">sortOn</span><span class="sxs-lookup"><span data-stu-id="ef064-123">sortOn</span></span>|<span data-ttu-id="ef064-124">string</span><span class="sxs-lookup"><span data-stu-id="ef064-124">string</span></span>|<span data-ttu-id="ef064-125">Representa el tipo de ordenación de esta condición.</span><span class="sxs-lookup"><span data-stu-id="ef064-125">Represents the type of sorting of this condition.</span></span> <span data-ttu-id="ef064-126">Los valores posibles son: `Value`, `CellColor`, `FontColor`, `Icon`.</span><span class="sxs-lookup"><span data-stu-id="ef064-126">The possible values are: `Value`, `CellColor`, `FontColor`, `Icon`.</span></span>|
|<span data-ttu-id="ef064-127">icono</span><span class="sxs-lookup"><span data-stu-id="ef064-127">icon</span></span>|[<span data-ttu-id="ef064-128">WorkbookIcon</span><span class="sxs-lookup"><span data-stu-id="ef064-128">WorkbookIcon</span></span>](icon.md)|<span data-ttu-id="ef064-129">Representa el icono que es el destino de la condición si la ordenación se realiza según el icono de la celda.</span><span class="sxs-lookup"><span data-stu-id="ef064-129">Represents the icon that is the target of the condition if the sorting is on the cell's icon.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="ef064-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ef064-130">JSON representation</span></span>

<span data-ttu-id="ef064-131">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ef064-131">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "@odata.type": "microsoft.graph.workbookSortField"
}-->

```json
{
  "ascending": true,
  "color": "string",
  "dataOption": "string",
  "key": 1024,
  "sortOn": "string",
  "icon": { "@odata.type": "microsoft.graph.workbookIcon" }
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "SortField resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
