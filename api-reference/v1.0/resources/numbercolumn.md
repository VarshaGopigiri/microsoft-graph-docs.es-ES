---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: NumberColumn
ms.openlocfilehash: 8aa366e3c4f59fc5d22f945c863bab4f91373b67
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="numbercolumn-resource-type"></a><span data-ttu-id="eec8b-102">Tipo de recurso NumberColumn</span><span class="sxs-lookup"><span data-stu-id="eec8b-102">NumberColumn resource type</span></span>

<span data-ttu-id="eec8b-103">El recurso **numberColumn** en un recurso [columnDefinition](columnDefinition.md) indica que los valores de la columna son números.</span><span class="sxs-lookup"><span data-stu-id="eec8b-103">The **numberColumn** on a [columnDefinition](columnDefinition.md) resource indicates that the column's values are numbers.</span></span>

## <a name="json-representation"></a><span data-ttu-id="eec8b-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="eec8b-104">JSON representation</span></span>

<span data-ttu-id="eec8b-105">A continuación se incluye una representación JSON de un recurso **numberColumn**.</span><span class="sxs-lookup"><span data-stu-id="eec8b-105">Here is a JSON representation of a **driveItem** resource.</span></span>
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.numberColumn" } -->

```json
{
  "decimalPlaces": "automatic | none | one | two | three | four | five",
  "displayAs": "number | percentage",
  "maximum": 10.551,
  "minimum": 99.993
}
```

## <a name="properties"></a><span data-ttu-id="eec8b-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eec8b-106">Properties</span></span>

| <span data-ttu-id="eec8b-107">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="eec8b-107">Property name</span></span>      | <span data-ttu-id="eec8b-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="eec8b-108">Type</span></span>   | <span data-ttu-id="eec8b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="eec8b-109">Description</span></span>
|:-------------------|:-------|:-----------------------------------------------
| <span data-ttu-id="eec8b-110">**decimalPlaces**</span><span class="sxs-lookup"><span data-stu-id="eec8b-110">**DecimalPlaces**</span></span>  | <span data-ttu-id="eec8b-111">string</span><span class="sxs-lookup"><span data-stu-id="eec8b-111">string</span></span> | <span data-ttu-id="eec8b-112">El número de decimales que se mostrará.</span><span class="sxs-lookup"><span data-stu-id="eec8b-112">How many decimal places to display.</span></span> <span data-ttu-id="eec8b-113">Consulte a continuación para obtener información sobre los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="eec8b-113">See below for information about the possible values.</span></span>
| <span data-ttu-id="eec8b-114">**displayAs**</span><span class="sxs-lookup"><span data-stu-id="eec8b-114">**displayAs**</span></span>      | <span data-ttu-id="eec8b-115">string</span><span class="sxs-lookup"><span data-stu-id="eec8b-115">string</span></span> | <span data-ttu-id="eec8b-116">Cómo se debe presentar el valor en la experiencia de usuario.</span><span class="sxs-lookup"><span data-stu-id="eec8b-116">How the value should be presented in the UX.</span></span> <span data-ttu-id="eec8b-117">Debe ser `number` o `percentage`.</span><span class="sxs-lookup"><span data-stu-id="eec8b-117">Must be one of `number` or `percentage`.</span></span> <span data-ttu-id="eec8b-118">Si no se especifica, se trata como `number`.</span><span class="sxs-lookup"><span data-stu-id="eec8b-118">If unspecified, treated as `number`.</span></span>
| <span data-ttu-id="eec8b-119">**maximum**</span><span class="sxs-lookup"><span data-stu-id="eec8b-119">**maximum**</span></span>        | <span data-ttu-id="eec8b-120">double</span><span class="sxs-lookup"><span data-stu-id="eec8b-120">double</span></span> | <span data-ttu-id="eec8b-121">El valor máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="eec8b-121">The maximum permitted value.</span></span>
| <span data-ttu-id="eec8b-122">**minimum**</span><span class="sxs-lookup"><span data-stu-id="eec8b-122">**minimum**</span></span>        | <span data-ttu-id="eec8b-123">double</span><span class="sxs-lookup"><span data-stu-id="eec8b-123">double</span></span> | <span data-ttu-id="eec8b-124">El valor mínimo permitido.</span><span class="sxs-lookup"><span data-stu-id="eec8b-124">The minimum permitted value.</span></span>

## <a name="decimalplaces-values"></a><span data-ttu-id="eec8b-125">Valores DecimalPlaces</span><span class="sxs-lookup"><span data-stu-id="eec8b-125">DecimalPlaces values</span></span>

| <span data-ttu-id="eec8b-126">Valor</span><span class="sxs-lookup"><span data-stu-id="eec8b-126">Value</span></span>          | <span data-ttu-id="eec8b-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="eec8b-127">Description</span></span>
|:---------------|:--------------------------------------------------------------
| <span data-ttu-id="eec8b-128">**automatic**</span><span class="sxs-lookup"><span data-stu-id="eec8b-128">**Automatic**</span></span>  | <span data-ttu-id="eec8b-129">Valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="eec8b-129">Default.</span></span> <span data-ttu-id="eec8b-130">Se muestran decimales automáticamente según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="eec8b-130">Automatically display decimal places as needed.</span></span>
| <span data-ttu-id="eec8b-131">**none**</span><span class="sxs-lookup"><span data-stu-id="eec8b-131">**None**</span></span>       | <span data-ttu-id="eec8b-132">No se muestra ningún decimal.</span><span class="sxs-lookup"><span data-stu-id="eec8b-132">Do not display any decimal places.</span></span>
| <span data-ttu-id="eec8b-133">**one**</span><span class="sxs-lookup"><span data-stu-id="eec8b-133">**One**</span></span>        | <span data-ttu-id="eec8b-134">Se muestra siempre un decimal.</span><span class="sxs-lookup"><span data-stu-id="eec8b-134">Always display one decimal place.</span></span>
| <span data-ttu-id="eec8b-135">**two**</span><span class="sxs-lookup"><span data-stu-id="eec8b-135">**Two**</span></span>        | <span data-ttu-id="eec8b-136">Se muestran siempre dos decimales.</span><span class="sxs-lookup"><span data-stu-id="eec8b-136">Always display two decimal places.</span></span>
| <span data-ttu-id="eec8b-137">**three**</span><span class="sxs-lookup"><span data-stu-id="eec8b-137">**Three**</span></span>      | <span data-ttu-id="eec8b-138">Se muestran siempre tres decimales.</span><span class="sxs-lookup"><span data-stu-id="eec8b-138">Always display three decimal places.</span></span>
| <span data-ttu-id="eec8b-139">**four**</span><span class="sxs-lookup"><span data-stu-id="eec8b-139">**Four**</span></span>       | <span data-ttu-id="eec8b-140">Se muestran siempre cuatro decimales.</span><span class="sxs-lookup"><span data-stu-id="eec8b-140">Always display four decimal places.</span></span>
| <span data-ttu-id="eec8b-141">**five**</span><span class="sxs-lookup"><span data-stu-id="eec8b-141">**five**</span></span>       | <span data-ttu-id="eec8b-142">Se muestran siempre cinco decimales.</span><span class="sxs-lookup"><span data-stu-id="eec8b-142">Always display five decimal places.</span></span>

<span data-ttu-id="eec8b-143">Nota: **decimalPlaces** y **displayAs** se aplican a cómo se representan los números, no a cómo se almacenan.</span><span class="sxs-lookup"><span data-stu-id="eec8b-143">Note: **decimalPlaces** and **displayAs** apply to how numbers are rendered, not stored.</span></span>
<span data-ttu-id="eec8b-144">Estas propiedades se pueden actualizar.</span><span class="sxs-lookup"><span data-stu-id="eec8b-144">These properties may be updated.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/NumberColumn"
} -->
