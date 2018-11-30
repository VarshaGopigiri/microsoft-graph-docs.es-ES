---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: NumberColumn
ms.openlocfilehash: 27d17d3e9b9d3d1debcd20f2beb916222801ebe9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090767"
---
# <a name="numbercolumn-resource-type"></a><span data-ttu-id="d74a2-102">Tipo de recurso NumberColumn</span><span class="sxs-lookup"><span data-stu-id="d74a2-102">NumberColumn resource type</span></span>

> <span data-ttu-id="d74a2-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d74a2-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d74a2-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d74a2-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d74a2-105">El recurso **numberColumn** en un recurso [columnDefinition](columndefinition.md) indica que los valores de la columna son números.</span><span class="sxs-lookup"><span data-stu-id="d74a2-105">The **numberColumn** on a [columnDefinition](columndefinition.md) resource indicates that the column's values are numbers.</span></span>

## <a name="json-representation"></a><span data-ttu-id="d74a2-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d74a2-106">JSON representation</span></span>

<span data-ttu-id="d74a2-107">A continuación se incluye una representación JSON de un recurso **numberColumn**.</span><span class="sxs-lookup"><span data-stu-id="d74a2-107">Here is a JSON representation of a **numberColumn** resource.</span></span>
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.numberColumn" } -->

```json
{
  "decimalPlaces": "automatic | none | one | two | three | four | five",
  "displayAs": "number | percentage",
  "maximum": 10.551,
  "minimum": 99.993
}
```

## <a name="properties"></a><span data-ttu-id="d74a2-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d74a2-108">Properties</span></span>

| <span data-ttu-id="d74a2-109">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="d74a2-109">Property name</span></span>      | <span data-ttu-id="d74a2-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="d74a2-110">Type</span></span>   | <span data-ttu-id="d74a2-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d74a2-111">Description</span></span>
|:-------------------|:-------|:-----------------------------------------------
| <span data-ttu-id="d74a2-112">**decimalPlaces**</span><span class="sxs-lookup"><span data-stu-id="d74a2-112">**decimalPlaces**</span></span>  | <span data-ttu-id="d74a2-113">string</span><span class="sxs-lookup"><span data-stu-id="d74a2-113">string</span></span> | <span data-ttu-id="d74a2-114">El número de decimales que se mostrará.</span><span class="sxs-lookup"><span data-stu-id="d74a2-114">How many decimal places to display.</span></span> <span data-ttu-id="d74a2-115">Consulte a continuación para obtener información sobre los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="d74a2-115">See below for information about the possible values.</span></span>
| <span data-ttu-id="d74a2-116">**displayAs**</span><span class="sxs-lookup"><span data-stu-id="d74a2-116">**displayAs**</span></span>      | <span data-ttu-id="d74a2-117">string</span><span class="sxs-lookup"><span data-stu-id="d74a2-117">string</span></span> | <span data-ttu-id="d74a2-118">Cómo se debe presentar el valor en la experiencia de usuario.</span><span class="sxs-lookup"><span data-stu-id="d74a2-118">How the value should be presented in the UX.</span></span> <span data-ttu-id="d74a2-119">Debe ser `number` o `percentage`.</span><span class="sxs-lookup"><span data-stu-id="d74a2-119">Must be one of `number` or `percentage`.</span></span> <span data-ttu-id="d74a2-120">Si no se especifica, se trata como `number`.</span><span class="sxs-lookup"><span data-stu-id="d74a2-120">If unspecified, treated as `number`.</span></span>
| <span data-ttu-id="d74a2-121">**maximum**</span><span class="sxs-lookup"><span data-stu-id="d74a2-121">**maximum**</span></span>        | <span data-ttu-id="d74a2-122">double</span><span class="sxs-lookup"><span data-stu-id="d74a2-122">double</span></span> | <span data-ttu-id="d74a2-123">El valor máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="d74a2-123">The maximum permitted value.</span></span>
| <span data-ttu-id="d74a2-124">**minimum**</span><span class="sxs-lookup"><span data-stu-id="d74a2-124">**minimum**</span></span>        | <span data-ttu-id="d74a2-125">double</span><span class="sxs-lookup"><span data-stu-id="d74a2-125">double</span></span> | <span data-ttu-id="d74a2-126">El valor mínimo permitido.</span><span class="sxs-lookup"><span data-stu-id="d74a2-126">The minimum permitted value.</span></span>

## <a name="decimalplaces-values"></a><span data-ttu-id="d74a2-127">Valores DecimalPlaces</span><span class="sxs-lookup"><span data-stu-id="d74a2-127">DecimalPlaces values</span></span>

| <span data-ttu-id="d74a2-128">Valor</span><span class="sxs-lookup"><span data-stu-id="d74a2-128">Value</span></span>          | <span data-ttu-id="d74a2-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="d74a2-129">Description</span></span>
|:---------------|:--------------------------------------------------------------
| <span data-ttu-id="d74a2-130">**automatic**</span><span class="sxs-lookup"><span data-stu-id="d74a2-130">**automatic**</span></span>  | <span data-ttu-id="d74a2-131">Valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d74a2-131">Default.</span></span> <span data-ttu-id="d74a2-132">Se muestran decimales automáticamente según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="d74a2-132">Automatically display decimal places as needed.</span></span>
| <span data-ttu-id="d74a2-133">**none**</span><span class="sxs-lookup"><span data-stu-id="d74a2-133">**none**</span></span>       | <span data-ttu-id="d74a2-134">No se muestra ningún decimal.</span><span class="sxs-lookup"><span data-stu-id="d74a2-134">Do not display any decimal places.</span></span>
| <span data-ttu-id="d74a2-135">**one**</span><span class="sxs-lookup"><span data-stu-id="d74a2-135">**one**</span></span>        | <span data-ttu-id="d74a2-136">Se muestra siempre un decimal.</span><span class="sxs-lookup"><span data-stu-id="d74a2-136">Always display one decimal place.</span></span>
| <span data-ttu-id="d74a2-137">**two**</span><span class="sxs-lookup"><span data-stu-id="d74a2-137">**two**</span></span>        | <span data-ttu-id="d74a2-138">Se muestran siempre dos decimales.</span><span class="sxs-lookup"><span data-stu-id="d74a2-138">Always display two decimal places.</span></span>
| <span data-ttu-id="d74a2-139">**three**</span><span class="sxs-lookup"><span data-stu-id="d74a2-139">**three**</span></span>      | <span data-ttu-id="d74a2-140">Se muestran siempre tres decimales.</span><span class="sxs-lookup"><span data-stu-id="d74a2-140">Always display three decimal places.</span></span>
| <span data-ttu-id="d74a2-141">**four**</span><span class="sxs-lookup"><span data-stu-id="d74a2-141">**four**</span></span>       | <span data-ttu-id="d74a2-142">Se muestran siempre cuatro decimales.</span><span class="sxs-lookup"><span data-stu-id="d74a2-142">Always display four decimal places.</span></span>
| <span data-ttu-id="d74a2-143">**five**</span><span class="sxs-lookup"><span data-stu-id="d74a2-143">**five**</span></span>       | <span data-ttu-id="d74a2-144">Se muestran siempre cinco decimales.</span><span class="sxs-lookup"><span data-stu-id="d74a2-144">Always display five decimal places.</span></span>

<span data-ttu-id="d74a2-145">Nota: **decimalPlaces** y **displayAs** se aplican a cómo se representan los números, no a cómo se almacenan.</span><span class="sxs-lookup"><span data-stu-id="d74a2-145">Note: **decimalPlaces** and **displayAs** apply to how numbers are rendered, not stored.</span></span>
<span data-ttu-id="d74a2-146">Estas propiedades se pueden actualizar.</span><span class="sxs-lookup"><span data-stu-id="d74a2-146">These properties may be updated.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/NumberColumn"
} -->
