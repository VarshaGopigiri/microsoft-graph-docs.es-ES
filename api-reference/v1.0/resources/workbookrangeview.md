---
title: Tipo de recurso rangeView
description: RangeView representa un conjunto de celdas visibles del intervalo primario.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 0fae95999de35b5bac42716a4c9ec8b16a5b1158
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27810083"
---
# <a name="rangeview-resource-type"></a><span data-ttu-id="2631a-103">Tipo de recurso rangeView</span><span class="sxs-lookup"><span data-stu-id="2631a-103">rangeView resource type</span></span>
<span data-ttu-id="2631a-104">RangeView representa un conjunto de celdas visibles del intervalo primario.</span><span class="sxs-lookup"><span data-stu-id="2631a-104">RangeView represents a set of visible cells of the parent range.</span></span>

## <a name="methods"></a><span data-ttu-id="2631a-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="2631a-105">Methods</span></span>

| <span data-ttu-id="2631a-106">Método</span><span class="sxs-lookup"><span data-stu-id="2631a-106">Method</span></span>           | <span data-ttu-id="2631a-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2631a-107">Return Type</span></span>    |<span data-ttu-id="2631a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="2631a-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="2631a-109">List rows</span><span class="sxs-lookup"><span data-stu-id="2631a-109">List rows</span></span>](../api/workbookrangeview-list-rows.md) |<span data-ttu-id="2631a-110">Colección [workbookRangeView](workbookrangeview.md)</span><span class="sxs-lookup"><span data-stu-id="2631a-110">[workbookRangeView](workbookrangeview.md) collection</span></span>| <span data-ttu-id="2631a-111">Obtenga una colección de objetos workbookRangeView.</span><span class="sxs-lookup"><span data-stu-id="2631a-111">Get a workbookRangeView object collection.</span></span>|
|[<span data-ttu-id="2631a-112">Itemat</span><span class="sxs-lookup"><span data-stu-id="2631a-112">Itemat</span></span>](../api/workbookrangeview-itemat.md)|[<span data-ttu-id="2631a-113">workbookRangeView</span><span class="sxs-lookup"><span data-stu-id="2631a-113">workbookRangeView</span></span>](workbookrangeview.md)|<span data-ttu-id="2631a-114">Obtengaun elemento de vista de rango basándose en el índice.</span><span class="sxs-lookup"><span data-stu-id="2631a-114">Get a range view item based in index.</span></span>|
|[<span data-ttu-id="2631a-115">Range</span><span class="sxs-lookup"><span data-stu-id="2631a-115">Range</span></span>](../api/workbookrangeview-range.md)|[<span data-ttu-id="2631a-116">workbookRange</span><span class="sxs-lookup"><span data-stu-id="2631a-116">workbookRange</span></span>](range.md)|<span data-ttu-id="2631a-117">Devuelve el objeto de rango asociado a la vista de rango.</span><span class="sxs-lookup"><span data-stu-id="2631a-117">Return the range object associated with the range view</span></span>|

## <a name="properties"></a><span data-ttu-id="2631a-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2631a-118">Properties</span></span>
| <span data-ttu-id="2631a-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2631a-119">Property</span></span>     | <span data-ttu-id="2631a-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="2631a-120">Type</span></span>   |<span data-ttu-id="2631a-121">Description</span><span class="sxs-lookup"><span data-stu-id="2631a-121">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2631a-122">cellAddresses</span><span class="sxs-lookup"><span data-stu-id="2631a-122">cellAddresses</span></span>|<span data-ttu-id="2631a-123">Json</span><span class="sxs-lookup"><span data-stu-id="2631a-123">Json</span></span>|<span data-ttu-id="2631a-124">Representa las direcciones de celda</span><span class="sxs-lookup"><span data-stu-id="2631a-124">Represents the cell addresses</span></span>
|<span data-ttu-id="2631a-125">columnCount</span><span class="sxs-lookup"><span data-stu-id="2631a-125">columnCount</span></span>|<span data-ttu-id="2631a-126">Int32</span><span class="sxs-lookup"><span data-stu-id="2631a-126">Int32</span></span>|<span data-ttu-id="2631a-p101">Devuelve el número de columnas visibles. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2631a-p101">Returns the number of visible columns. Read-only.</span></span>|
|<span data-ttu-id="2631a-129">formulas</span><span class="sxs-lookup"><span data-stu-id="2631a-129">formulas</span></span>|<span data-ttu-id="2631a-130">Json</span><span class="sxs-lookup"><span data-stu-id="2631a-130">Json</span></span>|<span data-ttu-id="2631a-131">Representa la fórmula en notación de estilo A1.</span><span class="sxs-lookup"><span data-stu-id="2631a-131">Represents the formula in A1-style notation.</span></span> |
|<span data-ttu-id="2631a-132">formulasLocal</span><span class="sxs-lookup"><span data-stu-id="2631a-132">formulasLocal</span></span>|<span data-ttu-id="2631a-133">Json</span><span class="sxs-lookup"><span data-stu-id="2631a-133">Json</span></span>|<span data-ttu-id="2631a-p102">Representa la fórmula en notación de estilo A1, en el idioma del usuario y en la configuración regional del formato numérico. Por ejemplo, la fórmula "=SUM(A1, 1.5)" en inglés se convertiría en "=SUMME(A1; 1,5)" en alemán.</span><span class="sxs-lookup"><span data-stu-id="2631a-p102">Represents the formula in A1-style notation, in the user's language and number-formatting locale. For example, the English "=SUM(A1, 1.5)" formula would become "=SUMME(A1; 1,5)" in German.</span></span>    |
|<span data-ttu-id="2631a-136">formulasR1C1</span><span class="sxs-lookup"><span data-stu-id="2631a-136">formulasR1C1</span></span>|<span data-ttu-id="2631a-137">Json</span><span class="sxs-lookup"><span data-stu-id="2631a-137">Json</span></span>|<span data-ttu-id="2631a-138">Representa la fórmula en notación de estilo R1C1.</span><span class="sxs-lookup"><span data-stu-id="2631a-138">Represents the formula in R1C1-style notation.</span></span>   |
|<span data-ttu-id="2631a-139">index</span><span class="sxs-lookup"><span data-stu-id="2631a-139">index</span></span>|<span data-ttu-id="2631a-140">Int32</span><span class="sxs-lookup"><span data-stu-id="2631a-140">Int32</span></span>|<span data-ttu-id="2631a-141">Índice de la página.</span><span class="sxs-lookup"><span data-stu-id="2631a-141">Index of the range.</span></span>|
|<span data-ttu-id="2631a-142">numberFormat</span><span class="sxs-lookup"><span data-stu-id="2631a-142">numberFormat</span></span>|<span data-ttu-id="2631a-143">Json</span><span class="sxs-lookup"><span data-stu-id="2631a-143">Json</span></span>|<span data-ttu-id="2631a-p103">Representa el código de formato numérico de Excel para la celda especificada. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2631a-p103">Represents Excel's number format code for the given cell. Read-only.</span></span> |
|<span data-ttu-id="2631a-146">rowCount</span><span class="sxs-lookup"><span data-stu-id="2631a-146">rowCount</span></span>|<span data-ttu-id="2631a-147">Int32</span><span class="sxs-lookup"><span data-stu-id="2631a-147">Int32</span></span>|<span data-ttu-id="2631a-p104">Devuelve el número de filas visibles. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2631a-p104">Returns the number of visible rows. Read-only.</span></span>  |
|<span data-ttu-id="2631a-150">text</span><span class="sxs-lookup"><span data-stu-id="2631a-150">text</span></span>|<span data-ttu-id="2631a-151">Json</span><span class="sxs-lookup"><span data-stu-id="2631a-151">Json</span></span>|<span data-ttu-id="2631a-p105">Valores de texto del rango especificado. El valor Text no dependerá del ancho de la celda. La sustitución del signo # que tiene lugar en la interfaz de usuario de Excel no afectará al valor de texto devuelto por la API. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2631a-p105">Text values of the specified range. The Text value will not depend on the cell width. The # sign substitution that happens in Excel UI will not affect the text value returned by the API. Read-only.</span></span>    |
|<span data-ttu-id="2631a-156">valueTypes</span><span class="sxs-lookup"><span data-stu-id="2631a-156">valueTypes</span></span>|<span data-ttu-id="2631a-157">Json</span><span class="sxs-lookup"><span data-stu-id="2631a-157">Json</span></span>|<span data-ttu-id="2631a-158">Representa el tipo de datos de cada celda.</span><span class="sxs-lookup"><span data-stu-id="2631a-158">Represents the type of data of each cell.</span></span> <span data-ttu-id="2631a-159">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2631a-159">Read-only.</span></span> <span data-ttu-id="2631a-160">Los valores posibles son: desconocido, vacío, String, Integer, Double, Boolean, Error.</span><span class="sxs-lookup"><span data-stu-id="2631a-160">The possible values are: Unknown, Empty, String, Integer, Double, Boolean, Error.</span></span> |
|<span data-ttu-id="2631a-161">values</span><span class="sxs-lookup"><span data-stu-id="2631a-161">values</span></span>|<span data-ttu-id="2631a-162">Json</span><span class="sxs-lookup"><span data-stu-id="2631a-162">Json</span></span>|<span data-ttu-id="2631a-p107">Representa los valores sin formato de la vista del intervalo especificado. Los datos devueltos pueden ser de tipo cadena, número o booleano. La celda que contenga un error devolverá la cadena de error.</span><span class="sxs-lookup"><span data-stu-id="2631a-p107">Represents the raw values of the specified range view. The data returned could be of type string, number, or a boolean. Cell that contain an error will return the error string.</span></span>   |

## <a name="relationships"></a><span data-ttu-id="2631a-166">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2631a-166">Relationships</span></span>
| <span data-ttu-id="2631a-167">Relación</span><span class="sxs-lookup"><span data-stu-id="2631a-167">Relationship</span></span> | <span data-ttu-id="2631a-168">Tipo</span><span class="sxs-lookup"><span data-stu-id="2631a-168">Type</span></span>   |<span data-ttu-id="2631a-169">Descripción</span><span class="sxs-lookup"><span data-stu-id="2631a-169">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2631a-170">rows</span><span class="sxs-lookup"><span data-stu-id="2631a-170">rows</span></span>|<span data-ttu-id="2631a-171">Colección [workbookRangeView](workbookrangeview.md)</span><span class="sxs-lookup"><span data-stu-id="2631a-171">[workbookRangeView](workbookrangeview.md) collection</span></span>| <span data-ttu-id="2631a-p108">Representa una colección de vistas de intervalo asociadas a este. Solo lectura.    Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2631a-p108">Represents a collection of range views associated with the range. Read-only.    Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="2631a-175">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2631a-175">JSON representation</span></span>
<span data-ttu-id="2631a-176">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2631a-176">Here is a JSON representation of the resource.</span></span>
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
