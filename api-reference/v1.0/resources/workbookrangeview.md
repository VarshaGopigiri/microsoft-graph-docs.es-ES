---
title: Tipo de recurso rangeView
description: RangeView representa un conjunto de celdas visibles del intervalo primario.
author: lumine2008
ms.openlocfilehash: 3d8530623a19eb3a5990c0e863e41c169d0b4f72
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27334135"
---
# <a name="rangeview-resource-type"></a><span data-ttu-id="25f45-103">Tipo de recurso rangeView</span><span class="sxs-lookup"><span data-stu-id="25f45-103">rangeView resource type</span></span>
<span data-ttu-id="25f45-104">RangeView representa un conjunto de celdas visibles del intervalo primario.</span><span class="sxs-lookup"><span data-stu-id="25f45-104">RangeView represents a set of visible cells of the parent range.</span></span>

## <a name="methods"></a><span data-ttu-id="25f45-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="25f45-105">Methods</span></span>

| <span data-ttu-id="25f45-106">Método</span><span class="sxs-lookup"><span data-stu-id="25f45-106">Method</span></span>           | <span data-ttu-id="25f45-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="25f45-107">Return Type</span></span>    |<span data-ttu-id="25f45-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="25f45-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="25f45-109">List rows</span><span class="sxs-lookup"><span data-stu-id="25f45-109">List rows</span></span>](../api/workbookrangeview-list-rows.md) |<span data-ttu-id="25f45-110">Colección [workbookRangeView](workbookrangeview.md)</span><span class="sxs-lookup"><span data-stu-id="25f45-110">[workbookRangeView](workbookrangeview.md) collection</span></span>| <span data-ttu-id="25f45-111">Obtenga una colección de objetos workbookRangeView.</span><span class="sxs-lookup"><span data-stu-id="25f45-111">Get a workbookRangeView object collection.</span></span>|
|[<span data-ttu-id="25f45-112">Itemat</span><span class="sxs-lookup"><span data-stu-id="25f45-112">Itemat</span></span>](../api/workbookrangeview-itemat.md)|[<span data-ttu-id="25f45-113">workbookRangeView</span><span class="sxs-lookup"><span data-stu-id="25f45-113">workbookRangeView</span></span>](workbookrangeview.md)|<span data-ttu-id="25f45-114">Obtengaun elemento de vista de rango basándose en el índice.</span><span class="sxs-lookup"><span data-stu-id="25f45-114">Get a range view item based in index.</span></span>|
|[<span data-ttu-id="25f45-115">Range</span><span class="sxs-lookup"><span data-stu-id="25f45-115">Range</span></span>](../api/workbookrangeview-range.md)|[<span data-ttu-id="25f45-116">workbookRange</span><span class="sxs-lookup"><span data-stu-id="25f45-116">workbookRange</span></span>](range.md)|<span data-ttu-id="25f45-117">Devuelve el objeto de rango asociado a la vista de rango.</span><span class="sxs-lookup"><span data-stu-id="25f45-117">Return the range object associated with the range view</span></span>|

## <a name="properties"></a><span data-ttu-id="25f45-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="25f45-118">Properties</span></span>
| <span data-ttu-id="25f45-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="25f45-119">Property</span></span>     | <span data-ttu-id="25f45-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="25f45-120">Type</span></span>   |<span data-ttu-id="25f45-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="25f45-121">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="25f45-122">cellAddresses</span><span class="sxs-lookup"><span data-stu-id="25f45-122">cellAddresses</span></span>|<span data-ttu-id="25f45-123">Json</span><span class="sxs-lookup"><span data-stu-id="25f45-123">Json</span></span>|<span data-ttu-id="25f45-124">Representa las direcciones de celda</span><span class="sxs-lookup"><span data-stu-id="25f45-124">Represents the cell addresses</span></span>
|<span data-ttu-id="25f45-125">columnCount</span><span class="sxs-lookup"><span data-stu-id="25f45-125">columnCount</span></span>|<span data-ttu-id="25f45-126">Int32</span><span class="sxs-lookup"><span data-stu-id="25f45-126">Int32</span></span>|<span data-ttu-id="25f45-p101">Devuelve el número de columnas visibles. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="25f45-p101">Returns the number of visible columns. Read-only.</span></span>|
|<span data-ttu-id="25f45-129">formulas</span><span class="sxs-lookup"><span data-stu-id="25f45-129">formulas</span></span>|<span data-ttu-id="25f45-130">Json</span><span class="sxs-lookup"><span data-stu-id="25f45-130">Json</span></span>|<span data-ttu-id="25f45-131">Representa la fórmula en notación de estilo A1.</span><span class="sxs-lookup"><span data-stu-id="25f45-131">Represents the formula in A1-style notation.</span></span> |
|<span data-ttu-id="25f45-132">formulasLocal</span><span class="sxs-lookup"><span data-stu-id="25f45-132">formulasLocal</span></span>|<span data-ttu-id="25f45-133">Json</span><span class="sxs-lookup"><span data-stu-id="25f45-133">Json</span></span>|<span data-ttu-id="25f45-p102">Representa la fórmula en notación de estilo A1, en el idioma del usuario y en la configuración regional del formato numérico. Por ejemplo, la fórmula "=SUM(A1, 1.5)" en inglés se convertiría en "=SUMME(A1; 1,5)" en alemán.</span><span class="sxs-lookup"><span data-stu-id="25f45-p102">Represents the formula in A1-style notation, in the user's language and number-formatting locale. For example, the English "=SUM(A1, 1.5)" formula would become "=SUMME(A1; 1,5)" in German.</span></span>    |
|<span data-ttu-id="25f45-136">formulasR1C1</span><span class="sxs-lookup"><span data-stu-id="25f45-136">formulasR1C1</span></span>|<span data-ttu-id="25f45-137">Json</span><span class="sxs-lookup"><span data-stu-id="25f45-137">Json</span></span>|<span data-ttu-id="25f45-138">Representa la fórmula en notación de estilo R1C1.</span><span class="sxs-lookup"><span data-stu-id="25f45-138">Represents the formula in R1C1-style notation.</span></span>   |
|<span data-ttu-id="25f45-139">index</span><span class="sxs-lookup"><span data-stu-id="25f45-139">index</span></span>|<span data-ttu-id="25f45-140">Int32</span><span class="sxs-lookup"><span data-stu-id="25f45-140">Int32</span></span>|<span data-ttu-id="25f45-141">Índice de la página.</span><span class="sxs-lookup"><span data-stu-id="25f45-141">Index of the range.</span></span>|
|<span data-ttu-id="25f45-142">numberFormat</span><span class="sxs-lookup"><span data-stu-id="25f45-142">numberFormat</span></span>|<span data-ttu-id="25f45-143">Json</span><span class="sxs-lookup"><span data-stu-id="25f45-143">Json</span></span>|<span data-ttu-id="25f45-p103">Representa el código de formato numérico de Excel para la celda especificada. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="25f45-p103">Represents Excel's number format code for the given cell. Read-only.</span></span> |
|<span data-ttu-id="25f45-146">rowCount</span><span class="sxs-lookup"><span data-stu-id="25f45-146">rowCount</span></span>|<span data-ttu-id="25f45-147">Int32</span><span class="sxs-lookup"><span data-stu-id="25f45-147">Int32</span></span>|<span data-ttu-id="25f45-p104">Devuelve el número de filas visibles. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="25f45-p104">Returns the number of visible rows. Read-only.</span></span>  |
|<span data-ttu-id="25f45-150">text</span><span class="sxs-lookup"><span data-stu-id="25f45-150">text</span></span>|<span data-ttu-id="25f45-151">Json</span><span class="sxs-lookup"><span data-stu-id="25f45-151">Json</span></span>|<span data-ttu-id="25f45-p105">Valores de texto del rango especificado. El valor Text no dependerá del ancho de la celda. La sustitución del signo # que tiene lugar en la interfaz de usuario de Excel no afectará al valor de texto devuelto por la API. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="25f45-p105">Text values of the specified range. The Text value will not depend on the cell width. The # sign substitution that happens in Excel UI will not affect the text value returned by the API. Read-only.</span></span>    |
|<span data-ttu-id="25f45-156">valueTypes</span><span class="sxs-lookup"><span data-stu-id="25f45-156">valueTypes</span></span>|<span data-ttu-id="25f45-157">Json</span><span class="sxs-lookup"><span data-stu-id="25f45-157">Json</span></span>|<span data-ttu-id="25f45-158">Representa el tipo de datos de cada celda.</span><span class="sxs-lookup"><span data-stu-id="25f45-158">Represents the type of data of each cell.</span></span> <span data-ttu-id="25f45-159">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="25f45-159">Read-only.</span></span> <span data-ttu-id="25f45-160">Los valores posibles son: desconocido, vacío, String, Integer, Double, Boolean, Error.</span><span class="sxs-lookup"><span data-stu-id="25f45-160">The possible values are: Unknown, Empty, String, Integer, Double, Boolean, Error.</span></span> |
|<span data-ttu-id="25f45-161">values</span><span class="sxs-lookup"><span data-stu-id="25f45-161">values</span></span>|<span data-ttu-id="25f45-162">Json</span><span class="sxs-lookup"><span data-stu-id="25f45-162">Json</span></span>|<span data-ttu-id="25f45-p107">Representa los valores sin formato de la vista del intervalo especificado. Los datos devueltos pueden ser de tipo cadena, número o booleano. La celda que contenga un error devolverá la cadena de error.</span><span class="sxs-lookup"><span data-stu-id="25f45-p107">Represents the raw values of the specified range view. The data returned could be of type string, number, or a boolean. Cell that contain an error will return the error string.</span></span>   |

## <a name="relationships"></a><span data-ttu-id="25f45-166">Relaciones</span><span class="sxs-lookup"><span data-stu-id="25f45-166">Relationships</span></span>
| <span data-ttu-id="25f45-167">Relación</span><span class="sxs-lookup"><span data-stu-id="25f45-167">Relationship</span></span> | <span data-ttu-id="25f45-168">Tipo</span><span class="sxs-lookup"><span data-stu-id="25f45-168">Type</span></span>   |<span data-ttu-id="25f45-169">Descripción</span><span class="sxs-lookup"><span data-stu-id="25f45-169">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="25f45-170">rows</span><span class="sxs-lookup"><span data-stu-id="25f45-170">rows</span></span>|<span data-ttu-id="25f45-171">Colección [workbookRangeView](workbookrangeview.md)</span><span class="sxs-lookup"><span data-stu-id="25f45-171">[workbookRangeView](workbookrangeview.md) collection</span></span>| <span data-ttu-id="25f45-p108">Representa una colección de vistas de intervalo asociadas a este. Solo lectura.    Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="25f45-p108">Represents a collection of range views associated with the range. Read-only.    Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="25f45-175">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="25f45-175">JSON representation</span></span>
<span data-ttu-id="25f45-176">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="25f45-176">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [  ],
  "@odata.type": "microsoft.graph.workbookRangeView"
}-->
```json
{
  "cellAddresses": "Json",
  "columnCount": 1024,
  "formulas": "Json",
  "formulasLocal": "Json",
  "formulasR1C1": "Json",
  "index": 1024,
  "numberFormat": "Json",
  "rowCount": 1024,
  "text": "Json",
  "valueTypes": "Json",
  "values": "Json"
}
```
