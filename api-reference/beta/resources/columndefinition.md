---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: ColumnDefinition
ms.openlocfilehash: 9b99abe78b009786d489ec7f0c0fdce1e2945b1d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083279"
---
# <a name="columndefinition-resource-type"></a><span data-ttu-id="9d81d-102">tipo de recurso columnDefinition</span><span class="sxs-lookup"><span data-stu-id="9d81d-102">columnDefinition resource type</span></span>

> <span data-ttu-id="9d81d-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9d81d-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9d81d-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9d81d-104">Use of these APIs in production applications is not supported.</span></span>

## <a name="json-representation"></a><span data-ttu-id="9d81d-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9d81d-105">JSON representation</span></span>

<span data-ttu-id="9d81d-106">Aquí es una representación JSON de un recurso columnDefinition.</span><span class="sxs-lookup"><span data-stu-id="9d81d-106">Here is a JSON representation of a columnDefinition resource.</span></span>

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
  "geolocation": { "@odata.type": "microsoft.graph.geolocationColumn" },
  "lookup": { "@odata.type": "microsoft.graph.lookupColumn" },
  "number": { "@odata.type": "microsoft.graph.numberColumn" },
  "personOrGroup": { "@odata.type": "microsoft.graph.personOrGroupColumn" },
  "text": { "@odata.type": "microsoft.graph.textColumn" }
}
```

## <a name="properties"></a><span data-ttu-id="9d81d-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9d81d-107">Properties</span></span>

<span data-ttu-id="9d81d-108">Las columnas pueden contener datos de distintos tipos.</span><span class="sxs-lookup"><span data-stu-id="9d81d-108">Columns can hold data of various types.</span></span>
<span data-ttu-id="9d81d-109">Las propiedades siguientes indican qué tipo de datos almacena una columna, así como una configuración adicional para esos datos.</span><span class="sxs-lookup"><span data-stu-id="9d81d-109">The following properties indicate what type of data a column stores, as well as additional settings for that data.</span></span>
<span data-ttu-id="9d81d-110">Las propiedades relacionadas con el tipo (boolean, calculado, elección, moneda, fecha y hora, búsqueda, número, personOrGroup, texto) son mutuamente excluyentes: una columna sólo puede tener uno de ellos especificado.</span><span class="sxs-lookup"><span data-stu-id="9d81d-110">The type-related properties (boolean, calculated, choice, currency, dateTime, lookup, number, personOrGroup, text) are mutually exclusive -- a column can only have one of them specified.</span></span>

| <span data-ttu-id="9d81d-111">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="9d81d-111">Property name</span></span>           | <span data-ttu-id="9d81d-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="9d81d-112">Type</span></span>    | <span data-ttu-id="9d81d-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d81d-113">Description</span></span>
|:------------------------|:--------|:-----------------------------------------
| <span data-ttu-id="9d81d-114">**columnGroup**</span><span class="sxs-lookup"><span data-stu-id="9d81d-114">**columnGroup**</span></span>         | <span data-ttu-id="9d81d-115">string</span><span class="sxs-lookup"><span data-stu-id="9d81d-115">string</span></span>  | <span data-ttu-id="9d81d-116">Para las columnas de sitio, el nombre del grupo al que pertenece esta columna.</span><span class="sxs-lookup"><span data-stu-id="9d81d-116">For site columns, the name of the group this column belongs to.</span></span> <span data-ttu-id="9d81d-117">Ayuda a organizar las columnas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="9d81d-117">Helps organize related columns.</span></span>
| <span data-ttu-id="9d81d-118">**description**</span><span class="sxs-lookup"><span data-stu-id="9d81d-118">**description**</span></span>         | <span data-ttu-id="9d81d-119">string</span><span class="sxs-lookup"><span data-stu-id="9d81d-119">string</span></span>  | <span data-ttu-id="9d81d-120">Descripción de cara al usuario de la columna.</span><span class="sxs-lookup"><span data-stu-id="9d81d-120">The user-facing description of the column.</span></span>
| <span data-ttu-id="9d81d-121">**displayName**</span><span class="sxs-lookup"><span data-stu-id="9d81d-121">**displayName**</span></span>         | <span data-ttu-id="9d81d-122">string</span><span class="sxs-lookup"><span data-stu-id="9d81d-122">string</span></span>  | <span data-ttu-id="9d81d-123">Nombre de cara al usuario de la columna.</span><span class="sxs-lookup"><span data-stu-id="9d81d-123">The user-facing name of the column.</span></span>
| <span data-ttu-id="9d81d-124">**enforceUniqueValues**</span><span class="sxs-lookup"><span data-stu-id="9d81d-124">**enforceUniqueValues**</span></span> | <span data-ttu-id="9d81d-125">boolean</span><span class="sxs-lookup"><span data-stu-id="9d81d-125">boolean</span></span> | <span data-ttu-id="9d81d-126">Si es true, dos elementos de la lista no pueden tener el mismo valor para esta columna.</span><span class="sxs-lookup"><span data-stu-id="9d81d-126">If true, no two list items may have the same value for this column.</span></span>
| <span data-ttu-id="9d81d-127">**hidden**</span><span class="sxs-lookup"><span data-stu-id="9d81d-127">**hidden**</span></span>              | <span data-ttu-id="9d81d-128">boolean</span><span class="sxs-lookup"><span data-stu-id="9d81d-128">boolean</span></span> | <span data-ttu-id="9d81d-129">Especifica si la columna se muestra en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="9d81d-129">Specifies whether the column is displayed in the user interface.</span></span>
| <span data-ttu-id="9d81d-130">**id**</span><span class="sxs-lookup"><span data-stu-id="9d81d-130">**id**</span></span>                  | <span data-ttu-id="9d81d-131">string</span><span class="sxs-lookup"><span data-stu-id="9d81d-131">string</span></span>  | <span data-ttu-id="9d81d-132">El identificador único de la columna.</span><span class="sxs-lookup"><span data-stu-id="9d81d-132">The unique identifier for the column.</span></span>
| <span data-ttu-id="9d81d-133">**indexed**</span><span class="sxs-lookup"><span data-stu-id="9d81d-133">**indexed**</span></span>             | <span data-ttu-id="9d81d-134">boolean</span><span class="sxs-lookup"><span data-stu-id="9d81d-134">boolean</span></span> | <span data-ttu-id="9d81d-135">Especifica si los valores de columna se pueden usar para ordenar y buscar.</span><span class="sxs-lookup"><span data-stu-id="9d81d-135">Specifies whether the column values can used for sorting and searching.</span></span>
| <span data-ttu-id="9d81d-136">**name**</span><span class="sxs-lookup"><span data-stu-id="9d81d-136">**name**</span></span>                | <span data-ttu-id="9d81d-137">string</span><span class="sxs-lookup"><span data-stu-id="9d81d-137">string</span></span>  | <span data-ttu-id="9d81d-138">El nombre de cara a la API de la columna tal como aparece en [fields][] en un recurso [listItem][].</span><span class="sxs-lookup"><span data-stu-id="9d81d-138">The API-facing name of the column as it appears in the [fields][] on a [listItem][].</span></span> <span data-ttu-id="9d81d-139">Para el nombre de cara al usuario, consulte **displayName**.</span><span class="sxs-lookup"><span data-stu-id="9d81d-139">For the user-facing name, see **displayName**.</span></span>
| <span data-ttu-id="9d81d-140">**readOnly**</span><span class="sxs-lookup"><span data-stu-id="9d81d-140">**readOnly**</span></span>            | <span data-ttu-id="9d81d-141">bool</span><span class="sxs-lookup"><span data-stu-id="9d81d-141">bool</span></span>    | <span data-ttu-id="9d81d-142">Especifica si se pueden modificar los valores de columna.</span><span class="sxs-lookup"><span data-stu-id="9d81d-142">Specifies whether the column values can be modified.</span></span>
| <span data-ttu-id="9d81d-143">**required**</span><span class="sxs-lookup"><span data-stu-id="9d81d-143">**required**</span></span>            | <span data-ttu-id="9d81d-144">boolean</span><span class="sxs-lookup"><span data-stu-id="9d81d-144">boolean</span></span> | <span data-ttu-id="9d81d-145">Especifica si el valor de columna no es opcional.</span><span class="sxs-lookup"><span data-stu-id="9d81d-145">Specifies whether the column value is not optional.</span></span>
| <span data-ttu-id="9d81d-146">**boolean**</span><span class="sxs-lookup"><span data-stu-id="9d81d-146">**boolean**</span></span>       | <span data-ttu-id="9d81d-147">[booleanColumn][]</span><span class="sxs-lookup"><span data-stu-id="9d81d-147">[booleanColumn][]</span></span>       | <span data-ttu-id="9d81d-148">Esta columna almacena valores booleanos.</span><span class="sxs-lookup"><span data-stu-id="9d81d-148">This column stores boolean values.</span></span>
| <span data-ttu-id="9d81d-149">**calculated**</span><span class="sxs-lookup"><span data-stu-id="9d81d-149">**calculated**</span></span>    | <span data-ttu-id="9d81d-150">[calculatedColumn][]</span><span class="sxs-lookup"><span data-stu-id="9d81d-150">[calculatedColumn][]</span></span>    | <span data-ttu-id="9d81d-151">Los datos de la columna se calculan en función de otras columnas.</span><span class="sxs-lookup"><span data-stu-id="9d81d-151">This column's data is calculated based on other columns.</span></span>
| <span data-ttu-id="9d81d-152">**choice**</span><span class="sxs-lookup"><span data-stu-id="9d81d-152">**choice**</span></span>        | <span data-ttu-id="9d81d-153">[choiceColumn][]</span><span class="sxs-lookup"><span data-stu-id="9d81d-153">[choiceColumn][]</span></span>        | <span data-ttu-id="9d81d-154">Esta columna almacena los datos de una lista de opciones.</span><span class="sxs-lookup"><span data-stu-id="9d81d-154">This column stores data from a list of choices.</span></span>
| <span data-ttu-id="9d81d-155">**currency**</span><span class="sxs-lookup"><span data-stu-id="9d81d-155">**currency**</span></span>      | <span data-ttu-id="9d81d-156">[currencyColumn][]</span><span class="sxs-lookup"><span data-stu-id="9d81d-156">[currencyColumn][]</span></span>      | <span data-ttu-id="9d81d-157">Esta columna almacena valores de moneda.</span><span class="sxs-lookup"><span data-stu-id="9d81d-157">This column stores currency values.</span></span>
| <span data-ttu-id="9d81d-158">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="9d81d-158">**dateTime**</span></span>      | <span data-ttu-id="9d81d-159">[dateTimeColumn][]</span><span class="sxs-lookup"><span data-stu-id="9d81d-159">[dateTimeColumn][]</span></span>      | <span data-ttu-id="9d81d-160">Esta columna almacena valores DateTime.</span><span class="sxs-lookup"><span data-stu-id="9d81d-160">This column stores DateTime values.</span></span>
| <span data-ttu-id="9d81d-161">**defaultValue**</span><span class="sxs-lookup"><span data-stu-id="9d81d-161">**defaultValue**</span></span>  | <span data-ttu-id="9d81d-162">[defaultColumnValue][]</span><span class="sxs-lookup"><span data-stu-id="9d81d-162">[defaultColumnValue][]</span></span>  | <span data-ttu-id="9d81d-163">El valor predeterminado de esta columna.</span><span class="sxs-lookup"><span data-stu-id="9d81d-163">The default value for this column.</span></span>
| <span data-ttu-id="9d81d-164">**ubicación geográfica**</span><span class="sxs-lookup"><span data-stu-id="9d81d-164">**geolocation**</span></span>   | <span data-ttu-id="9d81d-165">[geolocationColumn][]</span><span class="sxs-lookup"><span data-stu-id="9d81d-165">[geolocationColumn][]</span></span>   | <span data-ttu-id="9d81d-166">Esta columna almacena una ubicación geográfica.</span><span class="sxs-lookup"><span data-stu-id="9d81d-166">This column stores a geolocation.</span></span>
| <span data-ttu-id="9d81d-167">**lookup**</span><span class="sxs-lookup"><span data-stu-id="9d81d-167">**lookup**</span></span>        | <span data-ttu-id="9d81d-168">[lookupColumn][]</span><span class="sxs-lookup"><span data-stu-id="9d81d-168">[lookupColumn][]</span></span>        | <span data-ttu-id="9d81d-169">Los datos de esta columna se buscan desde otro origen en el sitio.</span><span class="sxs-lookup"><span data-stu-id="9d81d-169">This column's data is looked up from another source in the site.</span></span>
| <span data-ttu-id="9d81d-170">**number**</span><span class="sxs-lookup"><span data-stu-id="9d81d-170">**number**</span></span>        | <span data-ttu-id="9d81d-171">[numberColumn][]</span><span class="sxs-lookup"><span data-stu-id="9d81d-171">[numberColumn][]</span></span>        | <span data-ttu-id="9d81d-172">Esta columna almacena valores de números.</span><span class="sxs-lookup"><span data-stu-id="9d81d-172">This column stores number values.</span></span>
| <span data-ttu-id="9d81d-173">**personOrGroup**</span><span class="sxs-lookup"><span data-stu-id="9d81d-173">**personOrGroup**</span></span> | <span data-ttu-id="9d81d-174">[personOrGroupColumn][]</span><span class="sxs-lookup"><span data-stu-id="9d81d-174">[personOrGroupColumn][]</span></span> | <span data-ttu-id="9d81d-175">Esta columna almacena valores de personas o grupos.</span><span class="sxs-lookup"><span data-stu-id="9d81d-175">This column stores Person or Group values.</span></span>
| <span data-ttu-id="9d81d-176">**text**</span><span class="sxs-lookup"><span data-stu-id="9d81d-176">**text**</span></span>          | <span data-ttu-id="9d81d-177">[textColumn][]</span><span class="sxs-lookup"><span data-stu-id="9d81d-177">[textColumn][]</span></span>          | <span data-ttu-id="9d81d-178">Esta columna almacena valores de texto.</span><span class="sxs-lookup"><span data-stu-id="9d81d-178">This column stores text values.</span></span>

><span data-ttu-id="9d81d-179">**Nota:** Estas propiedades corresponden a la enumeración de [SPFieldType][] de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="9d81d-179">**Note:** These properties correspond to SharePoint's [SPFieldType][] enumeration.</span></span>
<span data-ttu-id="9d81d-180">Mientras se representan los tipos más comunes de campo en la tabla anterior, esta versión beta API aún faltan algunos.</span><span class="sxs-lookup"><span data-stu-id="9d81d-180">While the most common field types are represented in the previous table, this beta API is still missing some.</span></span>
<span data-ttu-id="9d81d-181">En esos casos, no se rellenará ninguna de las facetas de tipo de columna y la columna solo tendrá sus propiedades básicas.</span><span class="sxs-lookup"><span data-stu-id="9d81d-181">In those cases, none of the column type facets will be populated, and the column will only have its basic properties.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d81d-182">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9d81d-182">Remarks</span></span>

<span data-ttu-id="9d81d-183">De forma predeterminada, las ColumnDefinitions y los valores de campo de las columnas `hidden` no se muestran.</span><span class="sxs-lookup"><span data-stu-id="9d81d-183">ColumnDefinitions and field values for `hidden` columns are not shown by default.</span></span>
<span data-ttu-id="9d81d-184">Para verlas al enumerar las **columnDefinitions**, incluya `hidden` en su instrucción `$select`.</span><span class="sxs-lookup"><span data-stu-id="9d81d-184">To see them when listing **columnDefinitions**, include `hidden` in your `$select` statement.</span></span>
<span data-ttu-id="9d81d-185">Para verlas al mostrar los valores de **campo** en [listItems][listItem], incluya las columnas que quiera por nombre en su instrucción `$select`.</span><span class="sxs-lookup"><span data-stu-id="9d81d-185">To see them when showing **field** values on [listItems][listItem], include the desired columns by name in your `$select` statement.</span></span>

[booleanColumn]: booleancolumn.md
[calculatedColumn]: calculatedcolumn.md
[choiceColumn]: choicecolumn.md
[currencyColumn]: currencycolumn.md
[dateTimeColumn]: datetimecolumn.md
[defaultColumnValue]: defaultcolumnvalue.md
[geolocationColumn]: geolocationcolumn.md
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
