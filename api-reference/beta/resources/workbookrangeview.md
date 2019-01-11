---
title: Tipo de recurso rangeView
description: RangeView representa un conjunto de celdas visibles del intervalo primario.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: c356c737946dc70c6718b71c1c9aa7081069fd96
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27859006"
---
# <a name="rangeview-resource-type"></a><span data-ttu-id="a35ec-103">Tipo de recurso rangeView</span><span class="sxs-lookup"><span data-stu-id="a35ec-103">rangeView resource type</span></span>

> <span data-ttu-id="a35ec-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a35ec-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a35ec-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a35ec-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a35ec-106">RangeView representa un conjunto de celdas visibles del intervalo primario.</span><span class="sxs-lookup"><span data-stu-id="a35ec-106">RangeView represents a set of visible cells of the parent range.</span></span>

## <a name="methods"></a><span data-ttu-id="a35ec-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="a35ec-107">Methods</span></span>

| <span data-ttu-id="a35ec-108">Método</span><span class="sxs-lookup"><span data-stu-id="a35ec-108">Method</span></span>           | <span data-ttu-id="a35ec-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a35ec-109">Return Type</span></span>    |<span data-ttu-id="a35ec-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a35ec-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="a35ec-111">List rows</span><span class="sxs-lookup"><span data-stu-id="a35ec-111">List rows</span></span>](../api/workbookrangeview-list-rows.md) |<span data-ttu-id="a35ec-112">Colección [workbookRangeView](workbookrangeview.md)</span><span class="sxs-lookup"><span data-stu-id="a35ec-112">[workbookRangeView](workbookrangeview.md) collection</span></span>| <span data-ttu-id="a35ec-113">Obtenga una colección de objetos workbookRangeView.</span><span class="sxs-lookup"><span data-stu-id="a35ec-113">Get a workbookRangeView object collection.</span></span>|
|[<span data-ttu-id="a35ec-114">Itemat</span><span class="sxs-lookup"><span data-stu-id="a35ec-114">Itemat</span></span>](../api/workbookrangeview-itemat.md)|[<span data-ttu-id="a35ec-115">workbookRangeView</span><span class="sxs-lookup"><span data-stu-id="a35ec-115">workbookRangeView</span></span>](workbookrangeview.md)|<span data-ttu-id="a35ec-116">Obtengaun elemento de vista de rango basándose en el índice.</span><span class="sxs-lookup"><span data-stu-id="a35ec-116">Get a range view item based in index.</span></span>|
|[<span data-ttu-id="a35ec-117">Range</span><span class="sxs-lookup"><span data-stu-id="a35ec-117">Range</span></span>](../api/workbookrangeview-range.md)|[<span data-ttu-id="a35ec-118">workbookRange</span><span class="sxs-lookup"><span data-stu-id="a35ec-118">workbookRange</span></span>](range.md)|<span data-ttu-id="a35ec-119">Devuelve el objeto de rango asociado a la vista de rango.</span><span class="sxs-lookup"><span data-stu-id="a35ec-119">Return the range object associated with the range view</span></span>|

## <a name="properties"></a><span data-ttu-id="a35ec-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a35ec-120">Properties</span></span>
| <span data-ttu-id="a35ec-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a35ec-121">Property</span></span>     | <span data-ttu-id="a35ec-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="a35ec-122">Type</span></span>   |<span data-ttu-id="a35ec-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="a35ec-123">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a35ec-124">columnCount</span><span class="sxs-lookup"><span data-stu-id="a35ec-124">columnCount</span></span>|<span data-ttu-id="a35ec-125">Int32</span><span class="sxs-lookup"><span data-stu-id="a35ec-125">Int32</span></span>|<span data-ttu-id="a35ec-p102">Devuelve el número de columnas visibles. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a35ec-p102">Returns the number of visible columns. Read-only.</span></span>|
|<span data-ttu-id="a35ec-128">formulas</span><span class="sxs-lookup"><span data-stu-id="a35ec-128">formulas</span></span>|<span data-ttu-id="a35ec-129">Json</span><span class="sxs-lookup"><span data-stu-id="a35ec-129">Json</span></span>|<span data-ttu-id="a35ec-130">Representa la fórmula en notación de estilo A1.</span><span class="sxs-lookup"><span data-stu-id="a35ec-130">Represents the formula in A1-style notation.</span></span> |
|<span data-ttu-id="a35ec-131">formulasLocal</span><span class="sxs-lookup"><span data-stu-id="a35ec-131">formulasLocal</span></span>|<span data-ttu-id="a35ec-132">Json</span><span class="sxs-lookup"><span data-stu-id="a35ec-132">Json</span></span>|<span data-ttu-id="a35ec-p103">Representa la fórmula en notación de estilo A1, en el idioma del usuario y en la configuración regional del formato numérico. Por ejemplo, la fórmula "=SUM(A1, 1.5)" en inglés se convertiría en "=SUMME(A1; 1,5)" en alemán.</span><span class="sxs-lookup"><span data-stu-id="a35ec-p103">Represents the formula in A1-style notation, in the user's language and number-formatting locale. For example, the English "=SUM(A1, 1.5)" formula would become "=SUMME(A1; 1,5)" in German.</span></span>    |
|<span data-ttu-id="a35ec-135">formulasR1C1</span><span class="sxs-lookup"><span data-stu-id="a35ec-135">formulasR1C1</span></span>|<span data-ttu-id="a35ec-136">Json</span><span class="sxs-lookup"><span data-stu-id="a35ec-136">Json</span></span>|<span data-ttu-id="a35ec-137">Representa la fórmula en notación de estilo R1C1.</span><span class="sxs-lookup"><span data-stu-id="a35ec-137">Represents the formula in R1C1-style notation.</span></span>   |
|<span data-ttu-id="a35ec-138">index</span><span class="sxs-lookup"><span data-stu-id="a35ec-138">index</span></span>|<span data-ttu-id="a35ec-139">Int32</span><span class="sxs-lookup"><span data-stu-id="a35ec-139">Int32</span></span>|<span data-ttu-id="a35ec-140">Índice de la página.</span><span class="sxs-lookup"><span data-stu-id="a35ec-140">Index of the range.</span></span>|
|<span data-ttu-id="a35ec-141">numberFormat</span><span class="sxs-lookup"><span data-stu-id="a35ec-141">numberFormat</span></span>|<span data-ttu-id="a35ec-142">Json</span><span class="sxs-lookup"><span data-stu-id="a35ec-142">Json</span></span>|<span data-ttu-id="a35ec-p104">Representa el código de formato numérico de Excel para la celda especificada. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a35ec-p104">Represents Excel's number format code for the given cell. Read-only.</span></span> |
|<span data-ttu-id="a35ec-145">rowCount</span><span class="sxs-lookup"><span data-stu-id="a35ec-145">rowCount</span></span>|<span data-ttu-id="a35ec-146">Int32</span><span class="sxs-lookup"><span data-stu-id="a35ec-146">Int32</span></span>|<span data-ttu-id="a35ec-p105">Devuelve el número de filas visibles. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a35ec-p105">Returns the number of visible rows. Read-only.</span></span>  |
|<span data-ttu-id="a35ec-149">text</span><span class="sxs-lookup"><span data-stu-id="a35ec-149">text</span></span>|<span data-ttu-id="a35ec-150">Json</span><span class="sxs-lookup"><span data-stu-id="a35ec-150">Json</span></span>|<span data-ttu-id="a35ec-p106">Valores de texto del rango especificado. El valor Text no dependerá del ancho de la celda. La sustitución del signo # que tiene lugar en la interfaz de usuario de Excel no afectará al valor de texto devuelto por la API. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a35ec-p106">Text values of the specified range. The Text value will not depend on the cell width. The # sign substitution that happens in Excel UI will not affect the text value returned by the API. Read-only.</span></span>    |
|<span data-ttu-id="a35ec-155">valueTypes</span><span class="sxs-lookup"><span data-stu-id="a35ec-155">valueTypes</span></span>|<span data-ttu-id="a35ec-156">Json</span><span class="sxs-lookup"><span data-stu-id="a35ec-156">Json</span></span>|<span data-ttu-id="a35ec-p107">Representa el tipo de datos de cada celda. Solo lectura. Los valores posibles son: Unknown, Empty, String, Integer, Double, Boolean, Error.</span><span class="sxs-lookup"><span data-stu-id="a35ec-p107">Represents the type of data of each cell. Read-only. Possible values are: Unknown, Empty, String, Integer, Double, Boolean, Error.</span></span> |
|<span data-ttu-id="a35ec-160">values</span><span class="sxs-lookup"><span data-stu-id="a35ec-160">values</span></span>|<span data-ttu-id="a35ec-161">Json</span><span class="sxs-lookup"><span data-stu-id="a35ec-161">Json</span></span>|<span data-ttu-id="a35ec-p108">Representa los valores sin formato de la vista del intervalo especificado. Los datos devueltos pueden ser de tipo cadena, número o booleano. La celda que contenga un error devolverá la cadena de error.</span><span class="sxs-lookup"><span data-stu-id="a35ec-p108">Represents the raw values of the specified range view. The data returned could be of type string, number, or a boolean. Cell that contain an error will return the error string.</span></span>   |

## <a name="relationships"></a><span data-ttu-id="a35ec-165">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a35ec-165">Relationships</span></span>
| <span data-ttu-id="a35ec-166">Relación</span><span class="sxs-lookup"><span data-stu-id="a35ec-166">Relationship</span></span> | <span data-ttu-id="a35ec-167">Tipo</span><span class="sxs-lookup"><span data-stu-id="a35ec-167">Type</span></span>   |<span data-ttu-id="a35ec-168">Descripción</span><span class="sxs-lookup"><span data-stu-id="a35ec-168">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a35ec-169">rows</span><span class="sxs-lookup"><span data-stu-id="a35ec-169">rows</span></span>|<span data-ttu-id="a35ec-170">Colección [workbookRangeView](workbookrangeview.md)</span><span class="sxs-lookup"><span data-stu-id="a35ec-170">[workbookRangeView](workbookrangeview.md) collection</span></span>| <span data-ttu-id="a35ec-p109">Representa una colección de vistas de intervalo asociadas a este. Solo lectura.    Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a35ec-p109">Represents a collection of range views associated with the range. Read-only.    Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="a35ec-174">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a35ec-174">JSON representation</span></span>
<span data-ttu-id="a35ec-175">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a35ec-175">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
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
  "id": "String (identifier)",
  "index": 1024,
  "numberFormat": "Json",
  "rowCount": 1024,
  "text": "Json",
  "valueTypes": "Json",
  "values": "Json"
}
```
