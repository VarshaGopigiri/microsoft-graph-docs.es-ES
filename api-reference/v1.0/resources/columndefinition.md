---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: ColumnDefinition
ms.openlocfilehash: e5942ddee4b505243cb64121862ce9e89e52d245
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="columndefinition-resource"></a><span data-ttu-id="95c13-102">Recurso ColumnDefinition</span><span class="sxs-lookup"><span data-stu-id="95c13-102">ColumnDefinition resource</span></span>

## <a name="json-representation"></a><span data-ttu-id="95c13-103">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="95c13-103">JSON representation</span></span>

<span data-ttu-id="95c13-104">A continuación se incluye una representación JSON de un recurso ColumnDefinition.</span><span class="sxs-lookup"><span data-stu-id="95c13-104">Here is a JSON representation of a {type} resource.</span></span>

<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.columnDefinition",
       "keyProperty": "id", "optionalProperties": [ ] } -->

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

## <a name="properties"></a><span data-ttu-id="95c13-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="95c13-105">Properties</span></span>

<span data-ttu-id="95c13-106">El recurso **columnDefinition** tiene las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="95c13-106">The **columnDefinition** resource has the following properties.</span></span>

| <span data-ttu-id="95c13-107">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="95c13-107">Property name</span></span>           | <span data-ttu-id="95c13-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="95c13-108">Type</span></span>    | <span data-ttu-id="95c13-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="95c13-109">Description</span></span>
|:------------------------|:--------|:-----------------------------------------
| <span data-ttu-id="95c13-110">**columnGroup**</span><span class="sxs-lookup"><span data-stu-id="95c13-110">**columnGroup**</span></span>         | <span data-ttu-id="95c13-111">string</span><span class="sxs-lookup"><span data-stu-id="95c13-111">string</span></span>  | <span data-ttu-id="95c13-112">Para las columnas de sitio, el nombre del grupo al que pertenece esta columna.</span><span class="sxs-lookup"><span data-stu-id="95c13-112">For site columns, the name of the group this column belongs to.</span></span> <span data-ttu-id="95c13-113">Ayuda a organizar las columnas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="95c13-113">Helps organize related columns.</span></span>
| <span data-ttu-id="95c13-114">**description**</span><span class="sxs-lookup"><span data-stu-id="95c13-114">**description**</span></span>         | <span data-ttu-id="95c13-115">string</span><span class="sxs-lookup"><span data-stu-id="95c13-115">string</span></span>  | <span data-ttu-id="95c13-116">Descripción de cara al usuario de la columna.</span><span class="sxs-lookup"><span data-stu-id="95c13-116">The user-facing description of the column.</span></span>
| <span data-ttu-id="95c13-117">**displayName**</span><span class="sxs-lookup"><span data-stu-id="95c13-117">**displayName**</span></span>         | <span data-ttu-id="95c13-118">string</span><span class="sxs-lookup"><span data-stu-id="95c13-118">string</span></span>  | <span data-ttu-id="95c13-119">Nombre de cara al usuario de la columna.</span><span class="sxs-lookup"><span data-stu-id="95c13-119">The user-facing name of the column.</span></span>
| <span data-ttu-id="95c13-120">**enforceUniqueValues**</span><span class="sxs-lookup"><span data-stu-id="95c13-120">**enforceUniqueValues**</span></span> | <span data-ttu-id="95c13-121">boolean</span><span class="sxs-lookup"><span data-stu-id="95c13-121">boolean</span></span> | <span data-ttu-id="95c13-122">Si es true, dos elementos de la lista no pueden tener el mismo valor para esta columna.</span><span class="sxs-lookup"><span data-stu-id="95c13-122">If true, no two list items may have the same value for this column.</span></span>
| <span data-ttu-id="95c13-123">**hidden**</span><span class="sxs-lookup"><span data-stu-id="95c13-123">**hidden**</span></span>              | <span data-ttu-id="95c13-124">boolean</span><span class="sxs-lookup"><span data-stu-id="95c13-124">boolean</span></span> | <span data-ttu-id="95c13-125">Especifica si la columna se muestra en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="95c13-125">Specifies whether the column is displayed in the user interface.</span></span>
| <span data-ttu-id="95c13-126">**id**</span><span class="sxs-lookup"><span data-stu-id="95c13-126">**id**</span></span>                  | <span data-ttu-id="95c13-127">string</span><span class="sxs-lookup"><span data-stu-id="95c13-127">string</span></span>  | <span data-ttu-id="95c13-128">El identificador único de la columna.</span><span class="sxs-lookup"><span data-stu-id="95c13-128">The unique identifier for the column.</span></span>
| <span data-ttu-id="95c13-129">**indexed**</span><span class="sxs-lookup"><span data-stu-id="95c13-129">**Indexed**</span></span>             | <span data-ttu-id="95c13-130">boolean</span><span class="sxs-lookup"><span data-stu-id="95c13-130">boolean</span></span> | <span data-ttu-id="95c13-131">Especifica si los valores de columna se pueden usar para ordenar y buscar.</span><span class="sxs-lookup"><span data-stu-id="95c13-131">Specifies whether the column values can used for sorting and searching.</span></span>
| <span data-ttu-id="95c13-132">**name**</span><span class="sxs-lookup"><span data-stu-id="95c13-132">**name**</span></span>                | <span data-ttu-id="95c13-133">string</span><span class="sxs-lookup"><span data-stu-id="95c13-133">string</span></span>  | <span data-ttu-id="95c13-134">El nombre de cara a la API de la columna tal como aparece en [fields][] en un recurso [listItem][].</span><span class="sxs-lookup"><span data-stu-id="95c13-134">The API-facing name of the column as it appears in the [fields][] on a [listItem][].</span></span> <span data-ttu-id="95c13-135">Para el nombre de cara al usuario, consulte **displayName**.</span><span class="sxs-lookup"><span data-stu-id="95c13-135">For the user-facing name, see **displayName**.</span></span>
| <span data-ttu-id="95c13-136">**readOnly**</span><span class="sxs-lookup"><span data-stu-id="95c13-136">**Read-only.**</span></span>            | <span data-ttu-id="95c13-137">bool</span><span class="sxs-lookup"><span data-stu-id="95c13-137">bool</span></span>    | <span data-ttu-id="95c13-138">Especifica si se pueden modificar los valores de columna.</span><span class="sxs-lookup"><span data-stu-id="95c13-138">Specifies whether the column values can be modified.</span></span>
| <span data-ttu-id="95c13-139">**required**</span><span class="sxs-lookup"><span data-stu-id="95c13-139">**Required**</span></span>            | <span data-ttu-id="95c13-140">boolean</span><span class="sxs-lookup"><span data-stu-id="95c13-140">boolean</span></span> | <span data-ttu-id="95c13-141">Especifica si el valor de columna no es opcional.</span><span class="sxs-lookup"><span data-stu-id="95c13-141">Specifies whether the column value is not optional.</span></span>

<span data-ttu-id="95c13-142">Las columnas pueden contener datos de distintos tipos.</span><span class="sxs-lookup"><span data-stu-id="95c13-142">Columns can hold data of various types.</span></span>
<span data-ttu-id="95c13-143">Las propiedades siguientes indican qué tipo de datos almacena una columna, así como una configuración adicional para esos datos.</span><span class="sxs-lookup"><span data-stu-id="95c13-143">The following properties indicate what type of data a column stores, as well as additional settings for that data.</span></span>
<span data-ttu-id="95c13-144">Estas propiedades son mutuamente exclusivas, una columna solo puede tener uno de ellos especificados.</span><span class="sxs-lookup"><span data-stu-id="95c13-144">These properties are mutually exclusive -- a column can only have one of them specified.</span></span>

| <span data-ttu-id="95c13-145">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="95c13-145">Property name</span></span>     | <span data-ttu-id="95c13-146">Tipo</span><span class="sxs-lookup"><span data-stu-id="95c13-146">Type</span></span>                    | <span data-ttu-id="95c13-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="95c13-147">Description</span></span>
|:------------------|:------------------------|:-------------------------------
| <span data-ttu-id="95c13-148">**boolean**</span><span class="sxs-lookup"><span data-stu-id="95c13-148">**Boolean**</span></span>       | <span data-ttu-id="95c13-149">[booleanColumn][]</span><span class="sxs-lookup"><span data-stu-id="95c13-149">[booleanColumn][]</span></span>       | <span data-ttu-id="95c13-150">Esta columna almacena valores booleanos.</span><span class="sxs-lookup"><span data-stu-id="95c13-150">This column stores boolean values.</span></span>
| <span data-ttu-id="95c13-151">**calculated**</span><span class="sxs-lookup"><span data-stu-id="95c13-151">**Calculated**</span></span>    | <span data-ttu-id="95c13-152">[calculatedColumn][]</span><span class="sxs-lookup"><span data-stu-id="95c13-152">[calculatedColumn][]</span></span>    | <span data-ttu-id="95c13-153">Los datos de la columna se calculan en función de otras columnas.</span><span class="sxs-lookup"><span data-stu-id="95c13-153">This column's data is calculated based on other columns.</span></span>
| <span data-ttu-id="95c13-154">**choice**</span><span class="sxs-lookup"><span data-stu-id="95c13-154">**choice**</span></span>        | <span data-ttu-id="95c13-155">[choiceColumn][]</span><span class="sxs-lookup"><span data-stu-id="95c13-155">[choiceColumn][]</span></span>        | <span data-ttu-id="95c13-156">Esta columna almacena los datos de una lista de opciones.</span><span class="sxs-lookup"><span data-stu-id="95c13-156">This column stores data from a list of choices.</span></span>
| <span data-ttu-id="95c13-157">**currency**</span><span class="sxs-lookup"><span data-stu-id="95c13-157">**Currency**</span></span>      | <span data-ttu-id="95c13-158">[currencyColumn][]</span><span class="sxs-lookup"><span data-stu-id="95c13-158">[currencyColumn][]</span></span>      | <span data-ttu-id="95c13-159">Esta columna almacena valores de moneda.</span><span class="sxs-lookup"><span data-stu-id="95c13-159">This column stores currency values.</span></span>
| <span data-ttu-id="95c13-160">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="95c13-160">**DateTime**</span></span>      | <span data-ttu-id="95c13-161">[dateTimeColumn][]</span><span class="sxs-lookup"><span data-stu-id="95c13-161">[dateTimeColumn][]</span></span>      | <span data-ttu-id="95c13-162">Esta columna almacena valores DateTime.</span><span class="sxs-lookup"><span data-stu-id="95c13-162">This column stores DateTime values.</span></span>
| <span data-ttu-id="95c13-163">**defaultValue**</span><span class="sxs-lookup"><span data-stu-id="95c13-163">**DefaultValue**</span></span>  | <span data-ttu-id="95c13-164">[defaultColumnValue][]</span><span class="sxs-lookup"><span data-stu-id="95c13-164">[defaultColumnValue][]</span></span>  | <span data-ttu-id="95c13-165">El valor predeterminado de esta columna.</span><span class="sxs-lookup"><span data-stu-id="95c13-165">The default value for this column.</span></span>
| <span data-ttu-id="95c13-166">**lookup**</span><span class="sxs-lookup"><span data-stu-id="95c13-166">**Lookup**</span></span>        | <span data-ttu-id="95c13-167">[lookupColumn][]</span><span class="sxs-lookup"><span data-stu-id="95c13-167">[lookupColumn][]</span></span>        | <span data-ttu-id="95c13-168">Los datos de esta columna se buscan desde otro origen en el sitio.</span><span class="sxs-lookup"><span data-stu-id="95c13-168">This column's data is looked up from another source in the site.</span></span>
| <span data-ttu-id="95c13-169">**number**</span><span class="sxs-lookup"><span data-stu-id="95c13-169">**number**</span></span>        | <span data-ttu-id="95c13-170">[numberColumn][]</span><span class="sxs-lookup"><span data-stu-id="95c13-170">[numberColumn][]</span></span>        | <span data-ttu-id="95c13-171">Esta columna almacena valores de números.</span><span class="sxs-lookup"><span data-stu-id="95c13-171">This column stores number values.</span></span>
| <span data-ttu-id="95c13-172">**personOrGroup**</span><span class="sxs-lookup"><span data-stu-id="95c13-172">**personOrGroup**</span></span> | <span data-ttu-id="95c13-173">[personOrGroupColumn][]</span><span class="sxs-lookup"><span data-stu-id="95c13-173">[personOrGroupColumn][]</span></span> | <span data-ttu-id="95c13-174">Esta columna almacena valores de personas o grupos.</span><span class="sxs-lookup"><span data-stu-id="95c13-174">This column stores Person or Group values.</span></span>
| <span data-ttu-id="95c13-175">**text**</span><span class="sxs-lookup"><span data-stu-id="95c13-175">**text**</span></span>          | <span data-ttu-id="95c13-176">[textColumn][]</span><span class="sxs-lookup"><span data-stu-id="95c13-176">[textColumn][]</span></span>          | <span data-ttu-id="95c13-177">Esta columna almacena valores de texto.</span><span class="sxs-lookup"><span data-stu-id="95c13-177">This column stores text values.</span></span>

<span data-ttu-id="95c13-178">Nota: Estas propiedades se corresponden con la enumeración [SPFieldType][] de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="95c13-178">Note: These properties correspond to SharePoint's [SPFieldType][] enumeration.</span></span>
<span data-ttu-id="95c13-179">Aunque los tipos más comunes de campo están representados en la tabla anterior, aún faltan algunos en esta API de versión beta.</span><span class="sxs-lookup"><span data-stu-id="95c13-179">While the most common field types are represented above, this beta API is still missing some.</span></span>
<span data-ttu-id="95c13-180">En esos casos, no se rellenará ninguna de las facetas de tipo de columna y la columna solo tendrá sus propiedades básicas.</span><span class="sxs-lookup"><span data-stu-id="95c13-180">In those cases, none of the column type facets will be populated, and the column will only have its basic properties.</span></span>

## <a name="remarks"></a><span data-ttu-id="95c13-181">Comentarios</span><span class="sxs-lookup"><span data-stu-id="95c13-181">Remarks</span></span>

<span data-ttu-id="95c13-182">De forma predeterminada, las ColumnDefinitions y los valores de campo de las columnas `hidden` no se muestran.</span><span class="sxs-lookup"><span data-stu-id="95c13-182">ColumnDefinitions and field values for `hidden` columns are not shown by default.</span></span>
<span data-ttu-id="95c13-183">Para verlas al enumerar las **columnDefinitions**, incluya `hidden` en su instrucción `$select`.</span><span class="sxs-lookup"><span data-stu-id="95c13-183">To see them when listing **columnDefinitions**, include `hidden` in your `$select` statement.</span></span>
<span data-ttu-id="95c13-184">Para verlas al mostrar los valores de **campo** en [listItems][listItem], incluya las columnas que quiera por nombre en su instrucción `$select`.</span><span class="sxs-lookup"><span data-stu-id="95c13-184">To see them when showing **field** values on [listItems][listItem], include the desired columns by name in your `$select` statement.</span></span>

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

[SPFieldType]: https://msdn.microsoft.com/en-us/library/microsoft.sharepoint.spfieldtype.aspx

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/ColumnDefinition"
} -->
