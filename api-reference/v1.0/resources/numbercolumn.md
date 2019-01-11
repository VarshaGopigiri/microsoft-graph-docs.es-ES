---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: NumberColumn
localization_priority: Normal
ms.openlocfilehash: 25db21e6495edb6c42746c47d257ae60a4c1cc07
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27867413"
---
# <a name="numbercolumn-resource-type"></a><span data-ttu-id="a35c3-102">Tipo de recurso NumberColumn</span><span class="sxs-lookup"><span data-stu-id="a35c3-102">NumberColumn resource type</span></span>

<span data-ttu-id="a35c3-103">El recurso **numberColumn** en un recurso [columnDefinition](columndefinition.md) indica que los valores de la columna son números.</span><span class="sxs-lookup"><span data-stu-id="a35c3-103">The **numberColumn** on a [columnDefinition](columndefinition.md) resource indicates that the column's values are numbers.</span></span>

## <a name="json-representation"></a><span data-ttu-id="a35c3-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a35c3-104">JSON representation</span></span>

<span data-ttu-id="a35c3-105">A continuación se incluye una representación JSON de un recurso **numberColumn**.</span><span class="sxs-lookup"><span data-stu-id="a35c3-105">Here is a JSON representation of a **numberColumn** resource.</span></span>
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.numberColumn" } -->

```json
{
  "decimalPlaces": "automatic | none | one | two | three | four | five",
  "displayAs": "number | percentage",
  "maximum": 10.551,
  "minimum": 99.993
}
```

## <a name="properties"></a><span data-ttu-id="a35c3-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a35c3-106">Properties</span></span>

| <span data-ttu-id="a35c3-107">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="a35c3-107">Property name</span></span>      | <span data-ttu-id="a35c3-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="a35c3-108">Type</span></span>   | <span data-ttu-id="a35c3-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="a35c3-109">Description</span></span>
|:-------------------|:-------|:-----------------------------------------------
| <span data-ttu-id="a35c3-110">**decimalPlaces**</span><span class="sxs-lookup"><span data-stu-id="a35c3-110">**decimalPlaces**</span></span>  | <span data-ttu-id="a35c3-111">string</span><span class="sxs-lookup"><span data-stu-id="a35c3-111">string</span></span> | <span data-ttu-id="a35c3-112">El número de decimales que se mostrará.</span><span class="sxs-lookup"><span data-stu-id="a35c3-112">How many decimal places to display.</span></span> <span data-ttu-id="a35c3-113">Consulte a continuación para obtener información sobre los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="a35c3-113">See below for information about the possible values.</span></span>
| <span data-ttu-id="a35c3-114">**displayAs**</span><span class="sxs-lookup"><span data-stu-id="a35c3-114">**displayAs**</span></span>      | <span data-ttu-id="a35c3-115">string</span><span class="sxs-lookup"><span data-stu-id="a35c3-115">string</span></span> | <span data-ttu-id="a35c3-116">Cómo se debe presentar el valor en la experiencia de usuario.</span><span class="sxs-lookup"><span data-stu-id="a35c3-116">How the value should be presented in the UX.</span></span> <span data-ttu-id="a35c3-117">Debe ser `number` o `percentage`.</span><span class="sxs-lookup"><span data-stu-id="a35c3-117">Must be one of `number` or `percentage`.</span></span> <span data-ttu-id="a35c3-118">Si no se especifica, se trata como `number`.</span><span class="sxs-lookup"><span data-stu-id="a35c3-118">If unspecified, treated as `number`.</span></span>
| <span data-ttu-id="a35c3-119">**maximum**</span><span class="sxs-lookup"><span data-stu-id="a35c3-119">**maximum**</span></span>        | <span data-ttu-id="a35c3-120">double</span><span class="sxs-lookup"><span data-stu-id="a35c3-120">double</span></span> | <span data-ttu-id="a35c3-121">El valor máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="a35c3-121">The maximum permitted value.</span></span>
| <span data-ttu-id="a35c3-122">**minimum**</span><span class="sxs-lookup"><span data-stu-id="a35c3-122">**minimum**</span></span>        | <span data-ttu-id="a35c3-123">double</span><span class="sxs-lookup"><span data-stu-id="a35c3-123">double</span></span> | <span data-ttu-id="a35c3-124">El valor mínimo permitido.</span><span class="sxs-lookup"><span data-stu-id="a35c3-124">The minimum permitted value.</span></span>

## <a name="decimalplaces"></a><span data-ttu-id="a35c3-125">DecimalPlaces</span><span class="sxs-lookup"><span data-stu-id="a35c3-125">DecimalPlaces</span></span>

| <span data-ttu-id="a35c3-126">Valor</span><span class="sxs-lookup"><span data-stu-id="a35c3-126">Value</span></span>          | <span data-ttu-id="a35c3-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="a35c3-127">Description</span></span>
|:---------------|:--------------------------------------------------------------
| <span data-ttu-id="a35c3-128">**automatic**</span><span class="sxs-lookup"><span data-stu-id="a35c3-128">**automatic**</span></span>  | <span data-ttu-id="a35c3-129">Valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a35c3-129">Default.</span></span> <span data-ttu-id="a35c3-130">Se muestran decimales automáticamente según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="a35c3-130">Automatically display decimal places as needed.</span></span>
| <span data-ttu-id="a35c3-131">**none**</span><span class="sxs-lookup"><span data-stu-id="a35c3-131">**none**</span></span>       | <span data-ttu-id="a35c3-132">No se muestra ningún decimal.</span><span class="sxs-lookup"><span data-stu-id="a35c3-132">Do not display any decimal places.</span></span>
| <span data-ttu-id="a35c3-133">**one**</span><span class="sxs-lookup"><span data-stu-id="a35c3-133">**one**</span></span>        | <span data-ttu-id="a35c3-134">Se muestra siempre un decimal.</span><span class="sxs-lookup"><span data-stu-id="a35c3-134">Always display one decimal place.</span></span>
| <span data-ttu-id="a35c3-135">**two**</span><span class="sxs-lookup"><span data-stu-id="a35c3-135">**two**</span></span>        | <span data-ttu-id="a35c3-136">Se muestran siempre dos decimales.</span><span class="sxs-lookup"><span data-stu-id="a35c3-136">Always display two decimal places.</span></span>
| <span data-ttu-id="a35c3-137">**three**</span><span class="sxs-lookup"><span data-stu-id="a35c3-137">**three**</span></span>      | <span data-ttu-id="a35c3-138">Se muestran siempre tres decimales.</span><span class="sxs-lookup"><span data-stu-id="a35c3-138">Always display three decimal places.</span></span>
| <span data-ttu-id="a35c3-139">**four**</span><span class="sxs-lookup"><span data-stu-id="a35c3-139">**four**</span></span>       | <span data-ttu-id="a35c3-140">Se muestran siempre cuatro decimales.</span><span class="sxs-lookup"><span data-stu-id="a35c3-140">Always display four decimal places.</span></span>
| <span data-ttu-id="a35c3-141">**five**</span><span class="sxs-lookup"><span data-stu-id="a35c3-141">**five**</span></span>       | <span data-ttu-id="a35c3-142">Se muestran siempre cinco decimales.</span><span class="sxs-lookup"><span data-stu-id="a35c3-142">Always display five decimal places.</span></span>

<span data-ttu-id="a35c3-143">Nota: **decimalPlaces** y **displayAs** se aplican a cómo se representan los números, no a cómo se almacenan.</span><span class="sxs-lookup"><span data-stu-id="a35c3-143">Note: **decimalPlaces** and **displayAs** apply to how numbers are rendered, not stored.</span></span>
<span data-ttu-id="a35c3-144">Estas propiedades se pueden actualizar.</span><span class="sxs-lookup"><span data-stu-id="a35c3-144">These properties may be updated.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/resources/numbercolumn.md:
      Found potential enums in resource example that weren't defined in a table:(automatic,none,one,two,three,four,five) are in resource, but () are in table",
    "Warning: /api-reference/v1.0/resources/numbercolumn.md:
      Found potential enums in resource example that weren't defined in a table:(number,percentage) are in resource, but () are in table"
  ],
  "tocPath": "Resources/NumberColumn"
} -->
