---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: NumberColumn
ms.openlocfilehash: 4aaff6539fc9c7ce77029463562c0f8fca57cac6
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23266509"
---
# <a name="numbercolumn-resource-type"></a><span data-ttu-id="cc59b-102">Tipo de recurso NumberColumn</span><span class="sxs-lookup"><span data-stu-id="cc59b-102">NumberColumn resource type</span></span>

<span data-ttu-id="cc59b-103">El recurso **numberColumn** en un recurso [columnDefinition](columnDefinition.md) indica que los valores de la columna son números.</span><span class="sxs-lookup"><span data-stu-id="cc59b-103">The **numberColumn** on a [columnDefinition](columnDefinition.md) resource indicates that the column's values are numbers.</span></span>

## <a name="json-representation"></a><span data-ttu-id="cc59b-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="cc59b-104">JSON representation</span></span>

<span data-ttu-id="cc59b-105">A continuación se incluye una representación JSON de un recurso **numberColumn**.</span><span class="sxs-lookup"><span data-stu-id="cc59b-105">Here is a JSON representation of a **numberColumn** resource.</span></span>
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.numberColumn" } -->

```json
{
  "decimalPlaces": "automatic | none | one | two | three | four | five",
  "displayAs": "number | percentage",
  "maximum": 10.551,
  "minimum": 99.993
}
```

## <a name="properties"></a><span data-ttu-id="cc59b-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cc59b-106">Properties</span></span>

| <span data-ttu-id="cc59b-107">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="cc59b-107">Property name</span></span>      | <span data-ttu-id="cc59b-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="cc59b-108">Type</span></span>   | <span data-ttu-id="cc59b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc59b-109">Description</span></span>
|:-------------------|:-------|:-----------------------------------------------
| <span data-ttu-id="cc59b-110">**decimalPlaces**</span><span class="sxs-lookup"><span data-stu-id="cc59b-110">**decimalPlaces**</span></span>  | <span data-ttu-id="cc59b-111">cadena</span><span class="sxs-lookup"><span data-stu-id="cc59b-111">string</span></span> | <span data-ttu-id="cc59b-112">El número de decimales que se mostrará.</span><span class="sxs-lookup"><span data-stu-id="cc59b-112">How many decimal places to display.</span></span> <span data-ttu-id="cc59b-113">Consulte a continuación para obtener información sobre los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="cc59b-113">See below for information about the possible values.</span></span>
| <span data-ttu-id="cc59b-114">**displayAs**</span><span class="sxs-lookup"><span data-stu-id="cc59b-114">**displayAs**</span></span>      | <span data-ttu-id="cc59b-115">cadena</span><span class="sxs-lookup"><span data-stu-id="cc59b-115">string</span></span> | <span data-ttu-id="cc59b-116">Cómo se debe presentar el valor en la experiencia de usuario.</span><span class="sxs-lookup"><span data-stu-id="cc59b-116">How the value should be presented in the UX.</span></span> <span data-ttu-id="cc59b-117">Debe ser `number` o `percentage`.</span><span class="sxs-lookup"><span data-stu-id="cc59b-117">Must be one of `number` or `percentage`.</span></span> <span data-ttu-id="cc59b-118">Si no se especifica, se trata como `number`.</span><span class="sxs-lookup"><span data-stu-id="cc59b-118">If unspecified, treated as `number`.</span></span>
| <span data-ttu-id="cc59b-119">**maximum**</span><span class="sxs-lookup"><span data-stu-id="cc59b-119">**maximum**</span></span>        | <span data-ttu-id="cc59b-120">doble</span><span class="sxs-lookup"><span data-stu-id="cc59b-120">double</span></span> | <span data-ttu-id="cc59b-121">El valor máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="cc59b-121">The maximum permitted value.</span></span>
| <span data-ttu-id="cc59b-122">**minimum**</span><span class="sxs-lookup"><span data-stu-id="cc59b-122">**minimum**</span></span>        | <span data-ttu-id="cc59b-123">doble</span><span class="sxs-lookup"><span data-stu-id="cc59b-123">double</span></span> | <span data-ttu-id="cc59b-124">El valor mínimo permitido.</span><span class="sxs-lookup"><span data-stu-id="cc59b-124">The minimum permitted value.</span></span>

## <a name="decimalplaces"></a><span data-ttu-id="cc59b-125">DecimalPlaces</span><span class="sxs-lookup"><span data-stu-id="cc59b-125">decimalPlaces</span></span>

| <span data-ttu-id="cc59b-126">Valor</span><span class="sxs-lookup"><span data-stu-id="cc59b-126">Value</span></span>          | <span data-ttu-id="cc59b-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc59b-127">Description</span></span>
|:---------------|:--------------------------------------------------------------
| <span data-ttu-id="cc59b-128">**automatic**</span><span class="sxs-lookup"><span data-stu-id="cc59b-128">**automatic**</span></span>  | <span data-ttu-id="cc59b-129">Valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="cc59b-129">Default.</span></span> <span data-ttu-id="cc59b-130">Se muestran decimales automáticamente según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="cc59b-130">Automatically display decimal places as needed.</span></span>
| <span data-ttu-id="cc59b-131">**none**</span><span class="sxs-lookup"><span data-stu-id="cc59b-131">**none**</span></span>       | <span data-ttu-id="cc59b-132">No se muestra ningún decimal.</span><span class="sxs-lookup"><span data-stu-id="cc59b-132">Do not display any decimal places.</span></span>
| <span data-ttu-id="cc59b-133">**one**</span><span class="sxs-lookup"><span data-stu-id="cc59b-133">**one**</span></span>        | <span data-ttu-id="cc59b-134">Se muestra siempre un decimal.</span><span class="sxs-lookup"><span data-stu-id="cc59b-134">Always display one decimal place.</span></span>
| <span data-ttu-id="cc59b-135">**two**</span><span class="sxs-lookup"><span data-stu-id="cc59b-135">**two**</span></span>        | <span data-ttu-id="cc59b-136">Se muestran siempre dos decimales.</span><span class="sxs-lookup"><span data-stu-id="cc59b-136">Always display two decimal places.</span></span>
| <span data-ttu-id="cc59b-137">**three**</span><span class="sxs-lookup"><span data-stu-id="cc59b-137">**three**</span></span>      | <span data-ttu-id="cc59b-138">Se muestran siempre tres decimales.</span><span class="sxs-lookup"><span data-stu-id="cc59b-138">Always display three decimal places.</span></span>
| <span data-ttu-id="cc59b-139">**four**</span><span class="sxs-lookup"><span data-stu-id="cc59b-139">**four**</span></span>       | <span data-ttu-id="cc59b-140">Se muestran siempre cuatro decimales.</span><span class="sxs-lookup"><span data-stu-id="cc59b-140">Always display four decimal places.</span></span>
| <span data-ttu-id="cc59b-141">**five**</span><span class="sxs-lookup"><span data-stu-id="cc59b-141">**five**</span></span>       | <span data-ttu-id="cc59b-142">Se muestran siempre cinco decimales.</span><span class="sxs-lookup"><span data-stu-id="cc59b-142">Always display five decimal places.</span></span>

<span data-ttu-id="cc59b-143">Nota: **decimalPlaces** y **displayAs** se aplican a cómo se representan los números, no a cómo se almacenan.</span><span class="sxs-lookup"><span data-stu-id="cc59b-143">Note: **decimalPlaces** and **displayAs** apply to how numbers are rendered, not stored.</span></span>
<span data-ttu-id="cc59b-144">Estas propiedades se pueden actualizar.</span><span class="sxs-lookup"><span data-stu-id="cc59b-144">These properties may be updated.</span></span>

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
