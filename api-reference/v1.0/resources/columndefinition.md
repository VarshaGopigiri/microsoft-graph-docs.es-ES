---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: ColumnDefinition
localization_priority: Normal
ms.openlocfilehash: 598a781c25dd9271be84eb3dfc16b1e5ff439298
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27862884"
---
# <a name="columndefinition-resource"></a><span data-ttu-id="3bdb2-102">Recurso ColumnDefinition</span><span class="sxs-lookup"><span data-stu-id="3bdb2-102">ColumnDefinition resource</span></span>

## <a name="json-representation"></a><span data-ttu-id="3bdb2-103">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3bdb2-103">JSON representation</span></span>

<span data-ttu-id="3bdb2-104">A continuación se incluye una representación JSON de un recurso ColumnDefinition.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-104">Here is a JSON representation of a ColumnDefinition resource.</span></span>

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

## <a name="properties"></a><span data-ttu-id="3bdb2-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3bdb2-105">Properties</span></span>

<span data-ttu-id="3bdb2-106">El recurso **columnDefinition** tiene las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-106">The **columnDefinition** resource has the following properties.</span></span>

| <span data-ttu-id="3bdb2-107">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="3bdb2-107">Property name</span></span>           | <span data-ttu-id="3bdb2-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="3bdb2-108">Type</span></span>    | <span data-ttu-id="3bdb2-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="3bdb2-109">Description</span></span>
|:------------------------|:--------|:-----------------------------------------
| <span data-ttu-id="3bdb2-110">**columnGroup**</span><span class="sxs-lookup"><span data-stu-id="3bdb2-110">**columnGroup**</span></span>         | <span data-ttu-id="3bdb2-111">string</span><span class="sxs-lookup"><span data-stu-id="3bdb2-111">string</span></span>  | <span data-ttu-id="3bdb2-112">Para las columnas de sitio, el nombre del grupo al que pertenece esta columna.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-112">For site columns, the name of the group this column belongs to.</span></span> <span data-ttu-id="3bdb2-113">Ayuda a organizar las columnas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-113">Helps organize related columns.</span></span>
| <span data-ttu-id="3bdb2-114">**description**</span><span class="sxs-lookup"><span data-stu-id="3bdb2-114">**description**</span></span>         | <span data-ttu-id="3bdb2-115">string</span><span class="sxs-lookup"><span data-stu-id="3bdb2-115">string</span></span>  | <span data-ttu-id="3bdb2-116">Descripción de cara al usuario de la columna.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-116">The user-facing description of the column.</span></span>
| <span data-ttu-id="3bdb2-117">**displayName**</span><span class="sxs-lookup"><span data-stu-id="3bdb2-117">**displayName**</span></span>         | <span data-ttu-id="3bdb2-118">string</span><span class="sxs-lookup"><span data-stu-id="3bdb2-118">string</span></span>  | <span data-ttu-id="3bdb2-119">Nombre de cara al usuario de la columna.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-119">The user-facing name of the column.</span></span>
| <span data-ttu-id="3bdb2-120">**enforceUniqueValues**</span><span class="sxs-lookup"><span data-stu-id="3bdb2-120">**enforceUniqueValues**</span></span> | <span data-ttu-id="3bdb2-121">boolean</span><span class="sxs-lookup"><span data-stu-id="3bdb2-121">boolean</span></span> | <span data-ttu-id="3bdb2-122">Si es true, dos elementos de la lista no pueden tener el mismo valor para esta columna.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-122">If true, no two list items may have the same value for this column.</span></span>
| <span data-ttu-id="3bdb2-123">**hidden**</span><span class="sxs-lookup"><span data-stu-id="3bdb2-123">**hidden**</span></span>              | <span data-ttu-id="3bdb2-124">boolean</span><span class="sxs-lookup"><span data-stu-id="3bdb2-124">boolean</span></span> | <span data-ttu-id="3bdb2-125">Especifica si la columna se muestra en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-125">Specifies whether the column is displayed in the user interface.</span></span>
| <span data-ttu-id="3bdb2-126">**id**</span><span class="sxs-lookup"><span data-stu-id="3bdb2-126">**id**</span></span>                  | <span data-ttu-id="3bdb2-127">string</span><span class="sxs-lookup"><span data-stu-id="3bdb2-127">string</span></span>  | <span data-ttu-id="3bdb2-128">El identificador único de la columna.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-128">The unique identifier for the column.</span></span>
| <span data-ttu-id="3bdb2-129">**indexed**</span><span class="sxs-lookup"><span data-stu-id="3bdb2-129">**indexed**</span></span>             | <span data-ttu-id="3bdb2-130">boolean</span><span class="sxs-lookup"><span data-stu-id="3bdb2-130">boolean</span></span> | <span data-ttu-id="3bdb2-131">Especifica si los valores de columna se pueden usar para ordenar y buscar.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-131">Specifies whether the column values can used for sorting and searching.</span></span>
| <span data-ttu-id="3bdb2-132">**name**</span><span class="sxs-lookup"><span data-stu-id="3bdb2-132">**name**</span></span>                | <span data-ttu-id="3bdb2-133">string</span><span class="sxs-lookup"><span data-stu-id="3bdb2-133">string</span></span>  | <span data-ttu-id="3bdb2-134">El nombre de cara a la API de la columna tal como aparece en [fields][] en un recurso [listItem][].</span><span class="sxs-lookup"><span data-stu-id="3bdb2-134">The API-facing name of the column as it appears in the [fields][] on a [listItem][].</span></span> <span data-ttu-id="3bdb2-135">Para el nombre de cara al usuario, consulte **displayName**.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-135">For the user-facing name, see **displayName**.</span></span>
| <span data-ttu-id="3bdb2-136">**readOnly**</span><span class="sxs-lookup"><span data-stu-id="3bdb2-136">**readOnly**</span></span>            | <span data-ttu-id="3bdb2-137">bool</span><span class="sxs-lookup"><span data-stu-id="3bdb2-137">bool</span></span>    | <span data-ttu-id="3bdb2-138">Especifica si se pueden modificar los valores de columna.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-138">Specifies whether the column values can be modified.</span></span>
| <span data-ttu-id="3bdb2-139">**required**</span><span class="sxs-lookup"><span data-stu-id="3bdb2-139">**required**</span></span>            | <span data-ttu-id="3bdb2-140">boolean</span><span class="sxs-lookup"><span data-stu-id="3bdb2-140">boolean</span></span> | <span data-ttu-id="3bdb2-141">Especifica si el valor de columna no es opcional.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-141">Specifies whether the column value is not optional.</span></span>

<span data-ttu-id="3bdb2-142">Las columnas pueden contener datos de distintos tipos.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-142">Columns can hold data of various types.</span></span>
<span data-ttu-id="3bdb2-143">Las propiedades siguientes indican qué tipo de datos almacena una columna, así como una configuración adicional para esos datos.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-143">The following properties indicate what type of data a column stores, as well as additional settings for that data.</span></span>
<span data-ttu-id="3bdb2-144">Estas propiedades son mutuamente exclusivas, una columna solo puede tener uno de ellos especificados.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-144">These properties are mutually exclusive -- a column can only have one of them specified.</span></span>

| <span data-ttu-id="3bdb2-145">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="3bdb2-145">Property name</span></span>     | <span data-ttu-id="3bdb2-146">Tipo</span><span class="sxs-lookup"><span data-stu-id="3bdb2-146">Type</span></span>                    | <span data-ttu-id="3bdb2-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="3bdb2-147">Description</span></span>
|:------------------|:------------------------|:-------------------------------
| <span data-ttu-id="3bdb2-148">**boolean**</span><span class="sxs-lookup"><span data-stu-id="3bdb2-148">**boolean**</span></span>       | <span data-ttu-id="3bdb2-149">[booleanColumn][]</span><span class="sxs-lookup"><span data-stu-id="3bdb2-149">[booleanColumn][]</span></span>       | <span data-ttu-id="3bdb2-150">Esta columna almacena valores booleanos.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-150">This column stores boolean values.</span></span>
| <span data-ttu-id="3bdb2-151">**calculated**</span><span class="sxs-lookup"><span data-stu-id="3bdb2-151">**calculated**</span></span>    | <span data-ttu-id="3bdb2-152">[calculatedColumn][]</span><span class="sxs-lookup"><span data-stu-id="3bdb2-152">[calculatedColumn][]</span></span>    | <span data-ttu-id="3bdb2-153">Los datos de la columna se calculan en función de otras columnas.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-153">This column's data is calculated based on other columns.</span></span>
| <span data-ttu-id="3bdb2-154">**choice**</span><span class="sxs-lookup"><span data-stu-id="3bdb2-154">**choice**</span></span>        | <span data-ttu-id="3bdb2-155">[choiceColumn][]</span><span class="sxs-lookup"><span data-stu-id="3bdb2-155">[choiceColumn][]</span></span>        | <span data-ttu-id="3bdb2-156">Esta columna almacena los datos de una lista de opciones.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-156">This column stores data from a list of choices.</span></span>
| <span data-ttu-id="3bdb2-157">**currency**</span><span class="sxs-lookup"><span data-stu-id="3bdb2-157">**currency**</span></span>      | <span data-ttu-id="3bdb2-158">[currencyColumn][]</span><span class="sxs-lookup"><span data-stu-id="3bdb2-158">[currencyColumn][]</span></span>      | <span data-ttu-id="3bdb2-159">Esta columna almacena valores de moneda.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-159">This column stores currency values.</span></span>
| <span data-ttu-id="3bdb2-160">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="3bdb2-160">**dateTime**</span></span>      | <span data-ttu-id="3bdb2-161">[dateTimeColumn][]</span><span class="sxs-lookup"><span data-stu-id="3bdb2-161">[dateTimeColumn][]</span></span>      | <span data-ttu-id="3bdb2-162">Esta columna almacena valores DateTime.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-162">This column stores DateTime values.</span></span>
| <span data-ttu-id="3bdb2-163">**defaultValue**</span><span class="sxs-lookup"><span data-stu-id="3bdb2-163">**defaultValue**</span></span>  | <span data-ttu-id="3bdb2-164">[defaultColumnValue][]</span><span class="sxs-lookup"><span data-stu-id="3bdb2-164">[defaultColumnValue][]</span></span>  | <span data-ttu-id="3bdb2-165">El valor predeterminado de esta columna.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-165">The default value for this column.</span></span>
| <span data-ttu-id="3bdb2-166">**lookup**</span><span class="sxs-lookup"><span data-stu-id="3bdb2-166">**lookup**</span></span>        | <span data-ttu-id="3bdb2-167">[lookupColumn][]</span><span class="sxs-lookup"><span data-stu-id="3bdb2-167">[lookupColumn][]</span></span>        | <span data-ttu-id="3bdb2-168">Los datos de esta columna se buscan desde otro origen en el sitio.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-168">This column's data is looked up from another source in the site.</span></span>
| <span data-ttu-id="3bdb2-169">**number**</span><span class="sxs-lookup"><span data-stu-id="3bdb2-169">**number**</span></span>        | <span data-ttu-id="3bdb2-170">[numberColumn][]</span><span class="sxs-lookup"><span data-stu-id="3bdb2-170">[numberColumn][]</span></span>        | <span data-ttu-id="3bdb2-171">Esta columna almacena valores de números.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-171">This column stores number values.</span></span>
| <span data-ttu-id="3bdb2-172">**personOrGroup**</span><span class="sxs-lookup"><span data-stu-id="3bdb2-172">**personOrGroup**</span></span> | <span data-ttu-id="3bdb2-173">[personOrGroupColumn][]</span><span class="sxs-lookup"><span data-stu-id="3bdb2-173">[personOrGroupColumn][]</span></span> | <span data-ttu-id="3bdb2-174">Esta columna almacena valores de personas o grupos.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-174">This column stores Person or Group values.</span></span>
| <span data-ttu-id="3bdb2-175">**text**</span><span class="sxs-lookup"><span data-stu-id="3bdb2-175">**text**</span></span>          | <span data-ttu-id="3bdb2-176">[textColumn][]</span><span class="sxs-lookup"><span data-stu-id="3bdb2-176">[textColumn][]</span></span>          | <span data-ttu-id="3bdb2-177">Esta columna almacena valores de texto.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-177">This column stores text values.</span></span>

<span data-ttu-id="3bdb2-178">Nota: Estas propiedades se corresponden con la enumeración [SPFieldType][] de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-178">Note: These properties correspond to SharePoint's [SPFieldType][] enumeration.</span></span>
<span data-ttu-id="3bdb2-179">Mientras se representan los tipos más comunes de campo anteriormente, esta API es aún faltan algunos.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-179">While the most common field types are represented above, this API is still missing some.</span></span>
<span data-ttu-id="3bdb2-180">En esos casos, no se rellenará ninguna de las facetas de tipo de columna y la columna solo tendrá sus propiedades básicas.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-180">In those cases, none of the column type facets will be populated, and the column will only have its basic properties.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bdb2-181">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3bdb2-181">Remarks</span></span>

<span data-ttu-id="3bdb2-182">De forma predeterminada, las ColumnDefinitions y los valores de campo de las columnas `hidden` no se muestran.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-182">ColumnDefinitions and field values for `hidden` columns are not shown by default.</span></span>
<span data-ttu-id="3bdb2-183">Para verlas al enumerar las **columnDefinitions**, incluya `hidden` en su instrucción `$select`.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-183">To see them when listing **columnDefinitions**, include `hidden` in your `$select` statement.</span></span>
<span data-ttu-id="3bdb2-184">Para verlas al mostrar los valores de **campo** en [listItems][listItem], incluya las columnas que quiera por nombre en su instrucción `$select`.</span><span class="sxs-lookup"><span data-stu-id="3bdb2-184">To see them when showing **field** values on [listItems][listItem], include the desired columns by name in your `$select` statement.</span></span>

[booleanColumn]: booleancolumn.md
[calculatedColumn]: calculatedcolumn.md
[choiceColumn]: choicecolumn.md
[currencyColumn]: currencycolumn.md
[dateTimeColumn]: datetimecolumn.md
[defaultColumnValue]: defaultcolumnvalue.md
[lookupColumn]: lookupcolumn.md
[numberColumn]: numbercolumn.md
[personOrGroupColumn]: personorgroupcolumn.md
[textColumn]: textcolumn.md
[fieldValueSet]: fieldvalueset.md
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
