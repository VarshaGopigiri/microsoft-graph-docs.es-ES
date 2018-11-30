---
title: Tipo de recurso rangeView
description: RangeView representa un conjunto de celdas visibles del intervalo primario.
ms.openlocfilehash: 84ff9d315a6bfa8c4b03fad1b8f05670cb2b155c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089949"
---
# <a name="rangeview-resource-type"></a><span data-ttu-id="ab315-103">Tipo de recurso rangeView</span><span class="sxs-lookup"><span data-stu-id="ab315-103">rangeView resource type</span></span>

> <span data-ttu-id="ab315-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ab315-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ab315-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ab315-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ab315-106">RangeView representa un conjunto de celdas visibles del intervalo primario.</span><span class="sxs-lookup"><span data-stu-id="ab315-106">RangeView represents a set of visible cells of the parent range.</span></span>

## <a name="methods"></a><span data-ttu-id="ab315-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="ab315-107">Methods</span></span>

| <span data-ttu-id="ab315-108">Método</span><span class="sxs-lookup"><span data-stu-id="ab315-108">Method</span></span>           | <span data-ttu-id="ab315-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ab315-109">Return Type</span></span>    |<span data-ttu-id="ab315-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab315-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="ab315-111">List rows</span><span class="sxs-lookup"><span data-stu-id="ab315-111">List rows</span></span>](../api/workbookrangeview-list-rows.md) |<span data-ttu-id="ab315-112">Colección [workbookRangeView](workbookrangeview.md)</span><span class="sxs-lookup"><span data-stu-id="ab315-112">[workbookRangeView](workbookrangeview.md) collection</span></span>| <span data-ttu-id="ab315-113">Obtenga una colección de objetos workbookRangeView.</span><span class="sxs-lookup"><span data-stu-id="ab315-113">Get a workbookRangeView object collection.</span></span>|
|[<span data-ttu-id="ab315-114">Itemat</span><span class="sxs-lookup"><span data-stu-id="ab315-114">Itemat</span></span>](../api/workbookrangeview-itemat.md)|[<span data-ttu-id="ab315-115">workbookRangeView</span><span class="sxs-lookup"><span data-stu-id="ab315-115">workbookRangeView</span></span>](workbookrangeview.md)|<span data-ttu-id="ab315-116">Obtengaun elemento de vista de rango basándose en el índice.</span><span class="sxs-lookup"><span data-stu-id="ab315-116">Get a range view item based in index.</span></span>|
|[<span data-ttu-id="ab315-117">Range</span><span class="sxs-lookup"><span data-stu-id="ab315-117">Range</span></span>](../api/workbookrangeview-range.md)|[<span data-ttu-id="ab315-118">workbookRange</span><span class="sxs-lookup"><span data-stu-id="ab315-118">workbookRange</span></span>](range.md)|<span data-ttu-id="ab315-119">Devuelve el objeto de rango asociado a la vista de rango.</span><span class="sxs-lookup"><span data-stu-id="ab315-119">Return the range object associated with the range view</span></span>|

## <a name="properties"></a><span data-ttu-id="ab315-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ab315-120">Properties</span></span>
| <span data-ttu-id="ab315-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ab315-121">Property</span></span>     | <span data-ttu-id="ab315-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="ab315-122">Type</span></span>   |<span data-ttu-id="ab315-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab315-123">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ab315-124">columnCount</span><span class="sxs-lookup"><span data-stu-id="ab315-124">columnCount</span></span>|<span data-ttu-id="ab315-125">Int32</span><span class="sxs-lookup"><span data-stu-id="ab315-125">Int32</span></span>|<span data-ttu-id="ab315-p102">Devuelve el número de columnas visibles. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ab315-p102">Returns the number of visible columns. Read-only.</span></span>|
|<span data-ttu-id="ab315-128">formulas</span><span class="sxs-lookup"><span data-stu-id="ab315-128">formulas</span></span>|<span data-ttu-id="ab315-129">Json</span><span class="sxs-lookup"><span data-stu-id="ab315-129">Json</span></span>|<span data-ttu-id="ab315-130">Representa la fórmula en notación de estilo A1.</span><span class="sxs-lookup"><span data-stu-id="ab315-130">Represents the formula in A1-style notation.</span></span> |
|<span data-ttu-id="ab315-131">formulasLocal</span><span class="sxs-lookup"><span data-stu-id="ab315-131">formulasLocal</span></span>|<span data-ttu-id="ab315-132">Json</span><span class="sxs-lookup"><span data-stu-id="ab315-132">Json</span></span>|<span data-ttu-id="ab315-p103">Representa la fórmula en notación de estilo A1, en el idioma del usuario y en la configuración regional del formato numérico. Por ejemplo, la fórmula "=SUM(A1, 1.5)" en inglés se convertiría en "=SUMME(A1; 1,5)" en alemán.</span><span class="sxs-lookup"><span data-stu-id="ab315-p103">Represents the formula in A1-style notation, in the user's language and number-formatting locale. For example, the English "=SUM(A1, 1.5)" formula would become "=SUMME(A1; 1,5)" in German.</span></span>    |
|<span data-ttu-id="ab315-135">formulasR1C1</span><span class="sxs-lookup"><span data-stu-id="ab315-135">formulasR1C1</span></span>|<span data-ttu-id="ab315-136">Json</span><span class="sxs-lookup"><span data-stu-id="ab315-136">Json</span></span>|<span data-ttu-id="ab315-137">Representa la fórmula en notación de estilo R1C1.</span><span class="sxs-lookup"><span data-stu-id="ab315-137">Represents the formula in R1C1-style notation.</span></span>   |
|<span data-ttu-id="ab315-138">index</span><span class="sxs-lookup"><span data-stu-id="ab315-138">index</span></span>|<span data-ttu-id="ab315-139">Int32</span><span class="sxs-lookup"><span data-stu-id="ab315-139">Int32</span></span>|<span data-ttu-id="ab315-140">Índice de la página.</span><span class="sxs-lookup"><span data-stu-id="ab315-140">Index of the range.</span></span>|
|<span data-ttu-id="ab315-141">numberFormat</span><span class="sxs-lookup"><span data-stu-id="ab315-141">numberFormat</span></span>|<span data-ttu-id="ab315-142">Json</span><span class="sxs-lookup"><span data-stu-id="ab315-142">Json</span></span>|<span data-ttu-id="ab315-p104">Representa el código de formato numérico de Excel para la celda especificada. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ab315-p104">Represents Excel's number format code for the given cell. Read-only.</span></span> |
|<span data-ttu-id="ab315-145">rowCount</span><span class="sxs-lookup"><span data-stu-id="ab315-145">rowCount</span></span>|<span data-ttu-id="ab315-146">Int32</span><span class="sxs-lookup"><span data-stu-id="ab315-146">Int32</span></span>|<span data-ttu-id="ab315-p105">Devuelve el número de filas visibles. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ab315-p105">Returns the number of visible rows. Read-only.</span></span>  |
|<span data-ttu-id="ab315-149">text</span><span class="sxs-lookup"><span data-stu-id="ab315-149">text</span></span>|<span data-ttu-id="ab315-150">Json</span><span class="sxs-lookup"><span data-stu-id="ab315-150">Json</span></span>|<span data-ttu-id="ab315-p106">Valores de texto del rango especificado. El valor Text no dependerá del ancho de la celda. La sustitución del signo # que tiene lugar en la interfaz de usuario de Excel no afectará al valor de texto devuelto por la API. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ab315-p106">Text values of the specified range. The Text value will not depend on the cell width. The # sign substitution that happens in Excel UI will not affect the text value returned by the API. Read-only.</span></span>    |
|<span data-ttu-id="ab315-155">valueTypes</span><span class="sxs-lookup"><span data-stu-id="ab315-155">valueTypes</span></span>|<span data-ttu-id="ab315-156">Json</span><span class="sxs-lookup"><span data-stu-id="ab315-156">Json</span></span>|<span data-ttu-id="ab315-p107">Representa el tipo de datos de cada celda. Solo lectura. Los valores posibles son: Unknown, Empty, String, Integer, Double, Boolean, Error.</span><span class="sxs-lookup"><span data-stu-id="ab315-p107">Represents the type of data of each cell. Read-only. Possible values are: Unknown, Empty, String, Integer, Double, Boolean, Error.</span></span> |
|<span data-ttu-id="ab315-160">values</span><span class="sxs-lookup"><span data-stu-id="ab315-160">values</span></span>|<span data-ttu-id="ab315-161">Json</span><span class="sxs-lookup"><span data-stu-id="ab315-161">Json</span></span>|<span data-ttu-id="ab315-p108">Representa los valores sin formato de la vista del intervalo especificado. Los datos devueltos pueden ser de tipo cadena, número o booleano. La celda que contenga un error devolverá la cadena de error.</span><span class="sxs-lookup"><span data-stu-id="ab315-p108">Represents the raw values of the specified range view. The data returned could be of type string, number, or a boolean. Cell that contain an error will return the error string.</span></span>   |

## <a name="relationships"></a><span data-ttu-id="ab315-165">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ab315-165">Relationships</span></span>
| <span data-ttu-id="ab315-166">Relación</span><span class="sxs-lookup"><span data-stu-id="ab315-166">Relationship</span></span> | <span data-ttu-id="ab315-167">Tipo</span><span class="sxs-lookup"><span data-stu-id="ab315-167">Type</span></span>   |<span data-ttu-id="ab315-168">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab315-168">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ab315-169">rows</span><span class="sxs-lookup"><span data-stu-id="ab315-169">rows</span></span>|<span data-ttu-id="ab315-170">Colección [workbookRangeView](workbookrangeview.md)</span><span class="sxs-lookup"><span data-stu-id="ab315-170">[workbookRangeView](workbookrangeview.md) collection</span></span>| <span data-ttu-id="ab315-p109">Representa una colección de vistas de intervalo asociadas a este. Solo lectura.    Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ab315-p109">Represents a collection of range views associated with the range. Read-only.    Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="ab315-174">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ab315-174">JSON representation</span></span>
<span data-ttu-id="ab315-175">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ab315-175">Here is a JSON representation of the resource.</span></span>
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