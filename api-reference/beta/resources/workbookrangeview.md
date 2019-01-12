---
title: Tipo de recurso rangeView
description: RangeView representa un conjunto de celdas visibles del intervalo primario.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 9476b3f4a085f70be51d81a9da667c07db3b9232
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27983719"
---
# <a name="rangeview-resource-type"></a><span data-ttu-id="b6c66-103">Tipo de recurso rangeView</span><span class="sxs-lookup"><span data-stu-id="b6c66-103">rangeView resource type</span></span>

> <span data-ttu-id="b6c66-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b6c66-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b6c66-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b6c66-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b6c66-106">RangeView representa un conjunto de celdas visibles del intervalo primario.</span><span class="sxs-lookup"><span data-stu-id="b6c66-106">RangeView represents a set of visible cells of the parent range.</span></span>

## <a name="methods"></a><span data-ttu-id="b6c66-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="b6c66-107">Methods</span></span>

| <span data-ttu-id="b6c66-108">Método</span><span class="sxs-lookup"><span data-stu-id="b6c66-108">Method</span></span>           | <span data-ttu-id="b6c66-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b6c66-109">Return Type</span></span>    |<span data-ttu-id="b6c66-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6c66-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="b6c66-111">List rows</span><span class="sxs-lookup"><span data-stu-id="b6c66-111">List rows</span></span>](../api/workbookrangeview-list-rows.md) |<span data-ttu-id="b6c66-112">Colección [workbookRangeView](workbookrangeview.md)</span><span class="sxs-lookup"><span data-stu-id="b6c66-112">[workbookRangeView](workbookrangeview.md) collection</span></span>| <span data-ttu-id="b6c66-113">Obtenga una colección de objetos workbookRangeView.</span><span class="sxs-lookup"><span data-stu-id="b6c66-113">Get a workbookRangeView object collection.</span></span>|
|[<span data-ttu-id="b6c66-114">Itemat</span><span class="sxs-lookup"><span data-stu-id="b6c66-114">Itemat</span></span>](../api/workbookrangeview-itemat.md)|[<span data-ttu-id="b6c66-115">workbookRangeView</span><span class="sxs-lookup"><span data-stu-id="b6c66-115">workbookRangeView</span></span>](workbookrangeview.md)|<span data-ttu-id="b6c66-116">Obtengaun elemento de vista de rango basándose en el índice.</span><span class="sxs-lookup"><span data-stu-id="b6c66-116">Get a range view item based in index.</span></span>|
|[<span data-ttu-id="b6c66-117">Range</span><span class="sxs-lookup"><span data-stu-id="b6c66-117">Range</span></span>](../api/workbookrangeview-range.md)|[<span data-ttu-id="b6c66-118">workbookRange</span><span class="sxs-lookup"><span data-stu-id="b6c66-118">workbookRange</span></span>](range.md)|<span data-ttu-id="b6c66-119">Devuelve el objeto de rango asociado a la vista de rango.</span><span class="sxs-lookup"><span data-stu-id="b6c66-119">Return the range object associated with the range view</span></span>|

## <a name="properties"></a><span data-ttu-id="b6c66-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b6c66-120">Properties</span></span>
| <span data-ttu-id="b6c66-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b6c66-121">Property</span></span>     | <span data-ttu-id="b6c66-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="b6c66-122">Type</span></span>   |<span data-ttu-id="b6c66-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6c66-123">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b6c66-124">columnCount</span><span class="sxs-lookup"><span data-stu-id="b6c66-124">columnCount</span></span>|<span data-ttu-id="b6c66-125">Int32</span><span class="sxs-lookup"><span data-stu-id="b6c66-125">Int32</span></span>|<span data-ttu-id="b6c66-p102">Devuelve el número de columnas visibles. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b6c66-p102">Returns the number of visible columns. Read-only.</span></span>|
|<span data-ttu-id="b6c66-128">formulas</span><span class="sxs-lookup"><span data-stu-id="b6c66-128">formulas</span></span>|<span data-ttu-id="b6c66-129">Json</span><span class="sxs-lookup"><span data-stu-id="b6c66-129">Json</span></span>|<span data-ttu-id="b6c66-130">Representa la fórmula en notación de estilo A1.</span><span class="sxs-lookup"><span data-stu-id="b6c66-130">Represents the formula in A1-style notation.</span></span> |
|<span data-ttu-id="b6c66-131">formulasLocal</span><span class="sxs-lookup"><span data-stu-id="b6c66-131">formulasLocal</span></span>|<span data-ttu-id="b6c66-132">Json</span><span class="sxs-lookup"><span data-stu-id="b6c66-132">Json</span></span>|<span data-ttu-id="b6c66-p103">Representa la fórmula en notación de estilo A1, en el idioma del usuario y en la configuración regional del formato numérico. Por ejemplo, la fórmula "=SUM(A1, 1.5)" en inglés se convertiría en "=SUMME(A1; 1,5)" en alemán.</span><span class="sxs-lookup"><span data-stu-id="b6c66-p103">Represents the formula in A1-style notation, in the user's language and number-formatting locale. For example, the English "=SUM(A1, 1.5)" formula would become "=SUMME(A1; 1,5)" in German.</span></span>    |
|<span data-ttu-id="b6c66-135">formulasR1C1</span><span class="sxs-lookup"><span data-stu-id="b6c66-135">formulasR1C1</span></span>|<span data-ttu-id="b6c66-136">Json</span><span class="sxs-lookup"><span data-stu-id="b6c66-136">Json</span></span>|<span data-ttu-id="b6c66-137">Representa la fórmula en notación de estilo R1C1.</span><span class="sxs-lookup"><span data-stu-id="b6c66-137">Represents the formula in R1C1-style notation.</span></span>   |
|<span data-ttu-id="b6c66-138">index</span><span class="sxs-lookup"><span data-stu-id="b6c66-138">index</span></span>|<span data-ttu-id="b6c66-139">Int32</span><span class="sxs-lookup"><span data-stu-id="b6c66-139">Int32</span></span>|<span data-ttu-id="b6c66-140">Índice de la página.</span><span class="sxs-lookup"><span data-stu-id="b6c66-140">Index of the range.</span></span>|
|<span data-ttu-id="b6c66-141">numberFormat</span><span class="sxs-lookup"><span data-stu-id="b6c66-141">numberFormat</span></span>|<span data-ttu-id="b6c66-142">Json</span><span class="sxs-lookup"><span data-stu-id="b6c66-142">Json</span></span>|<span data-ttu-id="b6c66-p104">Representa el código de formato numérico de Excel para la celda especificada. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b6c66-p104">Represents Excel's number format code for the given cell. Read-only.</span></span> |
|<span data-ttu-id="b6c66-145">rowCount</span><span class="sxs-lookup"><span data-stu-id="b6c66-145">rowCount</span></span>|<span data-ttu-id="b6c66-146">Int32</span><span class="sxs-lookup"><span data-stu-id="b6c66-146">Int32</span></span>|<span data-ttu-id="b6c66-p105">Devuelve el número de filas visibles. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b6c66-p105">Returns the number of visible rows. Read-only.</span></span>  |
|<span data-ttu-id="b6c66-149">text</span><span class="sxs-lookup"><span data-stu-id="b6c66-149">text</span></span>|<span data-ttu-id="b6c66-150">Json</span><span class="sxs-lookup"><span data-stu-id="b6c66-150">Json</span></span>|<span data-ttu-id="b6c66-p106">Valores de texto del rango especificado. El valor Text no dependerá del ancho de la celda. La sustitución del signo # que tiene lugar en la interfaz de usuario de Excel no afectará al valor de texto devuelto por la API. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b6c66-p106">Text values of the specified range. The Text value will not depend on the cell width. The # sign substitution that happens in Excel UI will not affect the text value returned by the API. Read-only.</span></span>    |
|<span data-ttu-id="b6c66-155">valueTypes</span><span class="sxs-lookup"><span data-stu-id="b6c66-155">valueTypes</span></span>|<span data-ttu-id="b6c66-156">Json</span><span class="sxs-lookup"><span data-stu-id="b6c66-156">Json</span></span>|<span data-ttu-id="b6c66-p107">Representa el tipo de datos de cada celda. Solo lectura. Los valores posibles son: Unknown, Empty, String, Integer, Double, Boolean, Error.</span><span class="sxs-lookup"><span data-stu-id="b6c66-p107">Represents the type of data of each cell. Read-only. Possible values are: Unknown, Empty, String, Integer, Double, Boolean, Error.</span></span> |
|<span data-ttu-id="b6c66-160">values</span><span class="sxs-lookup"><span data-stu-id="b6c66-160">values</span></span>|<span data-ttu-id="b6c66-161">Json</span><span class="sxs-lookup"><span data-stu-id="b6c66-161">Json</span></span>|<span data-ttu-id="b6c66-p108">Representa los valores sin formato de la vista del intervalo especificado. Los datos devueltos pueden ser de tipo cadena, número o booleano. La celda que contenga un error devolverá la cadena de error.</span><span class="sxs-lookup"><span data-stu-id="b6c66-p108">Represents the raw values of the specified range view. The data returned could be of type string, number, or a boolean. Cell that contain an error will return the error string.</span></span>   |

## <a name="relationships"></a><span data-ttu-id="b6c66-165">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b6c66-165">Relationships</span></span>
| <span data-ttu-id="b6c66-166">Relación</span><span class="sxs-lookup"><span data-stu-id="b6c66-166">Relationship</span></span> | <span data-ttu-id="b6c66-167">Tipo</span><span class="sxs-lookup"><span data-stu-id="b6c66-167">Type</span></span>   |<span data-ttu-id="b6c66-168">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6c66-168">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b6c66-169">rows</span><span class="sxs-lookup"><span data-stu-id="b6c66-169">rows</span></span>|<span data-ttu-id="b6c66-170">Colección [workbookRangeView](workbookrangeview.md)</span><span class="sxs-lookup"><span data-stu-id="b6c66-170">[workbookRangeView](workbookrangeview.md) collection</span></span>| <span data-ttu-id="b6c66-p109">Representa una colección de vistas de intervalo asociadas a este. Solo lectura.    Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b6c66-p109">Represents a collection of range views associated with the range. Read-only.    Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="b6c66-174">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b6c66-174">JSON representation</span></span>
<span data-ttu-id="b6c66-175">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b6c66-175">Here is a JSON representation of the resource.</span></span>
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
