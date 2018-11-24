---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: ColumnDefinition
ms.openlocfilehash: a9c715983d83a448175c2c9d4110a92ff71edbbe
ms.sourcegitcommit: ebac77d2ca32438e552831de0258fe5e86fa225a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/17/2018
ms.locfileid: "26571668"
---
# <a name="columndefinition-resource"></a><span data-ttu-id="d4936-102">Recurso ColumnDefinition</span><span class="sxs-lookup"><span data-stu-id="d4936-102">ColumnDefinition resource</span></span>

## <a name="json-representation"></a><span data-ttu-id="d4936-103">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d4936-103">JSON representation</span></span>

<span data-ttu-id="d4936-104">A continuación se incluye una representación JSON de un recurso ColumnDefinition.</span><span class="sxs-lookup"><span data-stu-id="d4936-104">Here is a JSON representation of a ColumnDefinition resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.columnDefinition"
}-->

```json
{
  "columnGroup": "string",
  "description": "description",
  "displayName": "friendly name",
  "enforceUniqueValues": "true",
  "hidden": false,
  "id": "string",
  "indexed": true,
  "name": "staticNameForApi",
  "readOnly": false,
  "required": false,
  "boolean": { "@odata.type": "microsoft.graph.booleanColumn" },
  "calculated": { "@odata.type": "microsoft.graph.calculatedColumn" },
  "choice": { "@odata.type": "microsoft.graph.choiceColumn" },
  "currency": { "@odata.type": "microsoft.graph.currencyColumn" },
  "dateTime": { "@odata.type": "microsoft.graph.dateTimeColumn" },
  "defaultValue": { "@odata.type": "microsoft.graph.defaultColumnValue" },
  "lookup": { "@odata.type": "microsoft.graph.lookupColumn" },
  "number": { "@odata.type": "microsoft.graph.numberColumn" },
  "personOrGroup": { "@odata.type": "microsoft.graph.personOrGroupColumn" },
  "text": { "@odata.type": "microsoft.graph.textColumn" }
}
```

## <a name="properties"></a><span data-ttu-id="d4936-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d4936-105">Properties</span></span>

<span data-ttu-id="d4936-106">El recurso **columnDefinition** tiene las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="d4936-106">The **columnDefinition** resource has the following properties.</span></span>

| <span data-ttu-id="d4936-107">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="d4936-107">Property name</span></span>           | <span data-ttu-id="d4936-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="d4936-108">Type</span></span>    | <span data-ttu-id="d4936-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4936-109">Description</span></span>
|:------------------------|:--------|:-----------------------------------------
| <span data-ttu-id="d4936-110">**columnGroup**</span><span class="sxs-lookup"><span data-stu-id="d4936-110">**columnGroup**</span></span>         | <span data-ttu-id="d4936-111">string</span><span class="sxs-lookup"><span data-stu-id="d4936-111">string</span></span>  | <span data-ttu-id="d4936-112">Para las columnas de sitio, el nombre del grupo al que pertenece esta columna.</span><span class="sxs-lookup"><span data-stu-id="d4936-112">For site columns, the name of the group this column belongs to.</span></span> <span data-ttu-id="d4936-113">Ayuda a organizar las columnas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d4936-113">Helps organize related columns.</span></span>
| <span data-ttu-id="d4936-114">**description**</span><span class="sxs-lookup"><span data-stu-id="d4936-114">**description**</span></span>         | <span data-ttu-id="d4936-115">string</span><span class="sxs-lookup"><span data-stu-id="d4936-115">string</span></span>  | <span data-ttu-id="d4936-116">Descripción de cara al usuario de la columna.</span><span class="sxs-lookup"><span data-stu-id="d4936-116">The user-facing description of the column.</span></span>
| <span data-ttu-id="d4936-117">**displayName**</span><span class="sxs-lookup"><span data-stu-id="d4936-117">**displayName**</span></span>         | <span data-ttu-id="d4936-118">string</span><span class="sxs-lookup"><span data-stu-id="d4936-118">string</span></span>  | <span data-ttu-id="d4936-119">Nombre de cara al usuario de la columna.</span><span class="sxs-lookup"><span data-stu-id="d4936-119">The user-facing name of the column.</span></span>
| <span data-ttu-id="d4936-120">**enforceUniqueValues**</span><span class="sxs-lookup"><span data-stu-id="d4936-120">**enforceUniqueValues**</span></span> | <span data-ttu-id="d4936-121">boolean</span><span class="sxs-lookup"><span data-stu-id="d4936-121">boolean</span></span> | <span data-ttu-id="d4936-122">Si es true, dos elementos de la lista no pueden tener el mismo valor para esta columna.</span><span class="sxs-lookup"><span data-stu-id="d4936-122">If true, no two list items may have the same value for this column.</span></span>
| <span data-ttu-id="d4936-123">**hidden**</span><span class="sxs-lookup"><span data-stu-id="d4936-123">**hidden**</span></span>              | <span data-ttu-id="d4936-124">boolean</span><span class="sxs-lookup"><span data-stu-id="d4936-124">boolean</span></span> | <span data-ttu-id="d4936-125">Especifica si la columna se muestra en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="d4936-125">Specifies whether the column is displayed in the user interface.</span></span>
| <span data-ttu-id="d4936-126">**id**</span><span class="sxs-lookup"><span data-stu-id="d4936-126">**id**</span></span>                  | <span data-ttu-id="d4936-127">string</span><span class="sxs-lookup"><span data-stu-id="d4936-127">string</span></span>  | <span data-ttu-id="d4936-128">El identificador único de la columna.</span><span class="sxs-lookup"><span data-stu-id="d4936-128">The unique identifier for the column.</span></span>
| <span data-ttu-id="d4936-129">**indexed**</span><span class="sxs-lookup"><span data-stu-id="d4936-129">**indexed**</span></span>             | <span data-ttu-id="d4936-130">boolean</span><span class="sxs-lookup"><span data-stu-id="d4936-130">boolean</span></span> | <span data-ttu-id="d4936-131">Especifica si los valores de columna se pueden usar para ordenar y buscar.</span><span class="sxs-lookup"><span data-stu-id="d4936-131">Specifies whether the column values can used for sorting and searching.</span></span>
| <span data-ttu-id="d4936-132">**name**</span><span class="sxs-lookup"><span data-stu-id="d4936-132">**name**</span></span>                | <span data-ttu-id="d4936-133">string</span><span class="sxs-lookup"><span data-stu-id="d4936-133">string</span></span>  | <span data-ttu-id="d4936-134">El nombre de cara a la API de la columna tal como aparece en [fields][] en un recurso [listItem][].</span><span class="sxs-lookup"><span data-stu-id="d4936-134">The API-facing name of the column as it appears in the [fields][] on a [listItem][].</span></span> <span data-ttu-id="d4936-135">Para el nombre de cara al usuario, consulte **displayName**.</span><span class="sxs-lookup"><span data-stu-id="d4936-135">For the user-facing name, see **displayName**.</span></span>
| <span data-ttu-id="d4936-136">**readOnly**</span><span class="sxs-lookup"><span data-stu-id="d4936-136">**readOnly**</span></span>            | <span data-ttu-id="d4936-137">bool</span><span class="sxs-lookup"><span data-stu-id="d4936-137">bool</span></span>    | <span data-ttu-id="d4936-138">Especifica si se pueden modificar los valores de columna.</span><span class="sxs-lookup"><span data-stu-id="d4936-138">Specifies whether the column values can be modified.</span></span>
| <span data-ttu-id="d4936-139">**required**</span><span class="sxs-lookup"><span data-stu-id="d4936-139">**required**</span></span>            | <span data-ttu-id="d4936-140">boolean</span><span class="sxs-lookup"><span data-stu-id="d4936-140">boolean</span></span> | <span data-ttu-id="d4936-141">Especifica si el valor de columna no es opcional.</span><span class="sxs-lookup"><span data-stu-id="d4936-141">Specifies whether the column value is not optional.</span></span>

<span data-ttu-id="d4936-142">Las columnas pueden contener datos de distintos tipos.</span><span class="sxs-lookup"><span data-stu-id="d4936-142">Columns can hold data of various types.</span></span>
<span data-ttu-id="d4936-143">Las propiedades siguientes indican qué tipo de datos almacena una columna, así como una configuración adicional para esos datos.</span><span class="sxs-lookup"><span data-stu-id="d4936-143">The following properties indicate what type of data a column stores, as well as additional settings for that data.</span></span>
<span data-ttu-id="d4936-144">Estas propiedades son mutuamente exclusivas, una columna solo puede tener uno de ellos especificados.</span><span class="sxs-lookup"><span data-stu-id="d4936-144">These properties are mutually exclusive -- a column can only have one of them specified.</span></span>

| <span data-ttu-id="d4936-145">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="d4936-145">Property name</span></span>     | <span data-ttu-id="d4936-146">Tipo</span><span class="sxs-lookup"><span data-stu-id="d4936-146">Type</span></span>                    | <span data-ttu-id="d4936-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4936-147">Description</span></span>
|:------------------|:------------------------|:-------------------------------
| <span data-ttu-id="d4936-148">**boolean**</span><span class="sxs-lookup"><span data-stu-id="d4936-148">**boolean**</span></span>       | <span data-ttu-id="d4936-149">[booleanColumn][]</span><span class="sxs-lookup"><span data-stu-id="d4936-149">[booleanColumn][]</span></span>       | <span data-ttu-id="d4936-150">Esta columna almacena valores booleanos.</span><span class="sxs-lookup"><span data-stu-id="d4936-150">This column stores boolean values.</span></span>
| <span data-ttu-id="d4936-151">**calculated**</span><span class="sxs-lookup"><span data-stu-id="d4936-151">**calculated**</span></span>    | <span data-ttu-id="d4936-152">[calculatedColumn][]</span><span class="sxs-lookup"><span data-stu-id="d4936-152">[calculatedColumn][]</span></span>    | <span data-ttu-id="d4936-153">Los datos de la columna se calculan en función de otras columnas.</span><span class="sxs-lookup"><span data-stu-id="d4936-153">This column's data is calculated based on other columns.</span></span>
| <span data-ttu-id="d4936-154">**choice**</span><span class="sxs-lookup"><span data-stu-id="d4936-154">**choice**</span></span>        | <span data-ttu-id="d4936-155">[choiceColumn][]</span><span class="sxs-lookup"><span data-stu-id="d4936-155">[choiceColumn][]</span></span>        | <span data-ttu-id="d4936-156">Esta columna almacena los datos de una lista de opciones.</span><span class="sxs-lookup"><span data-stu-id="d4936-156">This column stores data from a list of choices.</span></span>
| <span data-ttu-id="d4936-157">**currency**</span><span class="sxs-lookup"><span data-stu-id="d4936-157">**currency**</span></span>      | <span data-ttu-id="d4936-158">[currencyColumn][]</span><span class="sxs-lookup"><span data-stu-id="d4936-158">[currencyColumn][]</span></span>      | <span data-ttu-id="d4936-159">Esta columna almacena valores de moneda.</span><span class="sxs-lookup"><span data-stu-id="d4936-159">This column stores currency values.</span></span>
| <span data-ttu-id="d4936-160">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="d4936-160">**dateTime**</span></span>      | <span data-ttu-id="d4936-161">[dateTimeColumn][]</span><span class="sxs-lookup"><span data-stu-id="d4936-161">[dateTimeColumn][]</span></span>      | <span data-ttu-id="d4936-162">Esta columna almacena valores DateTime.</span><span class="sxs-lookup"><span data-stu-id="d4936-162">This column stores DateTime values.</span></span>
| <span data-ttu-id="d4936-163">**defaultValue**</span><span class="sxs-lookup"><span data-stu-id="d4936-163">**defaultValue**</span></span>  | <span data-ttu-id="d4936-164">[defaultColumnValue][]</span><span class="sxs-lookup"><span data-stu-id="d4936-164">[defaultColumnValue][]</span></span>  | <span data-ttu-id="d4936-165">El valor predeterminado de esta columna.</span><span class="sxs-lookup"><span data-stu-id="d4936-165">The default value for this column.</span></span>
| <span data-ttu-id="d4936-166">**lookup**</span><span class="sxs-lookup"><span data-stu-id="d4936-166">**lookup**</span></span>        | <span data-ttu-id="d4936-167">[lookupColumn][]</span><span class="sxs-lookup"><span data-stu-id="d4936-167">[lookupColumn][]</span></span>        | <span data-ttu-id="d4936-168">Los datos de esta columna se buscan desde otro origen en el sitio.</span><span class="sxs-lookup"><span data-stu-id="d4936-168">This column's data is looked up from another source in the site.</span></span>
| <span data-ttu-id="d4936-169">**number**</span><span class="sxs-lookup"><span data-stu-id="d4936-169">**number**</span></span>        | <span data-ttu-id="d4936-170">[numberColumn][]</span><span class="sxs-lookup"><span data-stu-id="d4936-170">[numberColumn][]</span></span>        | <span data-ttu-id="d4936-171">Esta columna almacena valores de números.</span><span class="sxs-lookup"><span data-stu-id="d4936-171">This column stores number values.</span></span>
| <span data-ttu-id="d4936-172">**personOrGroup**</span><span class="sxs-lookup"><span data-stu-id="d4936-172">**personOrGroup**</span></span> | <span data-ttu-id="d4936-173">[personOrGroupColumn][]</span><span class="sxs-lookup"><span data-stu-id="d4936-173">[personOrGroupColumn][]</span></span> | <span data-ttu-id="d4936-174">Esta columna almacena valores de personas o grupos.</span><span class="sxs-lookup"><span data-stu-id="d4936-174">This column stores Person or Group values.</span></span>
| <span data-ttu-id="d4936-175">**text**</span><span class="sxs-lookup"><span data-stu-id="d4936-175">**text**</span></span>          | <span data-ttu-id="d4936-176">[textColumn][]</span><span class="sxs-lookup"><span data-stu-id="d4936-176">[textColumn][]</span></span>          | <span data-ttu-id="d4936-177">Esta columna almacena valores de texto.</span><span class="sxs-lookup"><span data-stu-id="d4936-177">This column stores text values.</span></span>

<span data-ttu-id="d4936-178">Nota: Estas propiedades se corresponden con la enumeración [SPFieldType][] de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="d4936-178">Note: These properties correspond to SharePoint's [SPFieldType][] enumeration.</span></span>
<span data-ttu-id="d4936-179">Mientras se representan los tipos más comunes de campo anteriormente, esta API es aún faltan algunos.</span><span class="sxs-lookup"><span data-stu-id="d4936-179">While the most common field types are represented above, this API is still missing some.</span></span>
<span data-ttu-id="d4936-180">En esos casos, no se rellenará ninguna de las facetas de tipo de columna y la columna solo tendrá sus propiedades básicas.</span><span class="sxs-lookup"><span data-stu-id="d4936-180">In those cases, none of the column type facets will be populated, and the column will only have its basic properties.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4936-181">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d4936-181">Remarks</span></span>

<span data-ttu-id="d4936-182">De forma predeterminada, las ColumnDefinitions y los valores de campo de las columnas `hidden` no se muestran.</span><span class="sxs-lookup"><span data-stu-id="d4936-182">ColumnDefinitions and field values for `hidden` columns are not shown by default.</span></span>
<span data-ttu-id="d4936-183">Para verlas al enumerar las **columnDefinitions**, incluya `hidden` en su instrucción `$select`.</span><span class="sxs-lookup"><span data-stu-id="d4936-183">To see them when listing **columnDefinitions**, include `hidden` in your `$select` statement.</span></span>
<span data-ttu-id="d4936-184">Para verlas al mostrar los valores de **campo** en [listItems][listItem], incluya las columnas que quiera por nombre en su instrucción `$select`.</span><span class="sxs-lookup"><span data-stu-id="d4936-184">To see them when showing **field** values on [listItems][listItem], include the desired columns by name in your `$select` statement.</span></span>

[booleanColumn]: booleanColumn.md
[calculatedColumn]: calculatedColumn.md
[choiceColumn]: choiceColumn.md
[currencyColumn]: currencyColumn.md
[dateTimeColumn]: dateTimeColumn.md
[defaultColumnValue]: defaultColumnValue.md
[lookupColumn]: lookupColumn.md
[numberColumn]: numberColumn.md
[personOrGroupColumn]: personOrGroupColumn.md
[textColumn]: textColumn.md
[fieldValueSet]: fieldValueSet.md
[fields]: fieldvalueset.md
[listItem]: listitem.md

[SPFieldType]: https://msdn.microsoft.com/library/microsoft.sharepoint.spfieldtype.aspx

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/ColumnDefinition"
} -->
