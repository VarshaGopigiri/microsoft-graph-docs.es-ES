---
title: Tipo de recurso SortField
description: Representa una condición en una operación de ordenación.
localization_priority: Normal
ms.openlocfilehash: fc93f33f7e1c6f366986cd5d1ca82ea186ad44b9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27894281"
---
# <a name="sortfield-resource-type"></a><span data-ttu-id="cd700-103">Tipo de recurso SortField</span><span class="sxs-lookup"><span data-stu-id="cd700-103">SortField resource type</span></span>

> <span data-ttu-id="cd700-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cd700-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cd700-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cd700-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="cd700-106">Representa una condición en una operación de ordenación.</span><span class="sxs-lookup"><span data-stu-id="cd700-106">Represents a condition in a sorting operation.</span></span>

## <a name="properties"></a><span data-ttu-id="cd700-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cd700-107">Properties</span></span>
| <span data-ttu-id="cd700-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cd700-108">Property</span></span>     | <span data-ttu-id="cd700-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd700-109">Type</span></span>   |<span data-ttu-id="cd700-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd700-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="cd700-111">ascending</span><span class="sxs-lookup"><span data-stu-id="cd700-111">ascending</span></span>|<span data-ttu-id="cd700-112">boolean</span><span class="sxs-lookup"><span data-stu-id="cd700-112">boolean</span></span>|<span data-ttu-id="cd700-113">Representa si la ordenación se realiza en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="cd700-113">Represents whether the sorting is done in an ascending fashion.</span></span>|
|<span data-ttu-id="cd700-114">color</span><span class="sxs-lookup"><span data-stu-id="cd700-114">color</span></span>|<span data-ttu-id="cd700-115">string</span><span class="sxs-lookup"><span data-stu-id="cd700-115">string</span></span>|<span data-ttu-id="cd700-116">Representa el color que es el destino de la condición si la ordenación se realiza según la fuente o el color de celda.</span><span class="sxs-lookup"><span data-stu-id="cd700-116">Represents the color that is the target of the condition if the sorting is on font or cell color.</span></span>|
|<span data-ttu-id="cd700-117">dataOption</span><span class="sxs-lookup"><span data-stu-id="cd700-117">dataOption</span></span>|<span data-ttu-id="cd700-118">string</span><span class="sxs-lookup"><span data-stu-id="cd700-118">string</span></span>|<span data-ttu-id="cd700-p102">Representa opciones de ordenación adicionales para este campo. Valores posibles: `Normal`, `TextAsNumber`.</span><span class="sxs-lookup"><span data-stu-id="cd700-p102">Represents additional sorting options for this field. Possible values are: `Normal`, `TextAsNumber`.</span></span>|
|<span data-ttu-id="cd700-121">Key</span><span class="sxs-lookup"><span data-stu-id="cd700-121">key</span></span>|<span data-ttu-id="cd700-122">int</span><span class="sxs-lookup"><span data-stu-id="cd700-122">int</span></span>|<span data-ttu-id="cd700-p103">Representa la columna (o fila, según la orientación de ordenación) en que se encuentra la condición. Se representa como un desplazamiento de la primera columna (o fila).</span><span class="sxs-lookup"><span data-stu-id="cd700-p103">Represents the column (or row, depending on the sort orientation) that the condition is on. Represented as an offset from the first column (or row).</span></span>|
|<span data-ttu-id="cd700-125">sortOn</span><span class="sxs-lookup"><span data-stu-id="cd700-125">sortOn</span></span>|<span data-ttu-id="cd700-126">string</span><span class="sxs-lookup"><span data-stu-id="cd700-126">string</span></span>|<span data-ttu-id="cd700-p104">Representa el tipo de ordenación de esta condición. Valores posibles: `Value`, `CellColor`, `FontColor`, `Icon`.</span><span class="sxs-lookup"><span data-stu-id="cd700-p104">Represents the type of sorting of this condition. Possible values are: `Value`, `CellColor`, `FontColor`, `Icon`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="cd700-129">Relaciones</span><span class="sxs-lookup"><span data-stu-id="cd700-129">Relationships</span></span>
| <span data-ttu-id="cd700-130">Relación</span><span class="sxs-lookup"><span data-stu-id="cd700-130">Relationship</span></span> | <span data-ttu-id="cd700-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd700-131">Type</span></span>   |<span data-ttu-id="cd700-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd700-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="cd700-133">icono</span><span class="sxs-lookup"><span data-stu-id="cd700-133">icon</span></span>|[<span data-ttu-id="cd700-134">Icon</span><span class="sxs-lookup"><span data-stu-id="cd700-134">Icon</span></span>](icon.md)|<span data-ttu-id="cd700-135">Representa el icono que es el destino de la condición si la ordenación se realiza según el icono de la celda.</span><span class="sxs-lookup"><span data-stu-id="cd700-135">Represents the icon that is the target of the condition if the sorting is on the cell's icon.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="cd700-136">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="cd700-136">JSON representation</span></span>

<span data-ttu-id="cd700-137">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="cd700-137">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.sortField"
}-->

```json
{
  "ascending": true,
  "color": "string",
  "dataOption": "string",
  "key": 1024,
  "sortOn": "string"
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
