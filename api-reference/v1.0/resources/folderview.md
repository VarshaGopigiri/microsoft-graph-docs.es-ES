---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: FolderView
ms.openlocfilehash: e73846a18f8576af8fe3cf5949e8ca5c63891837
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032376"
---
# <a name="folderview-resource-type"></a><span data-ttu-id="cf0cc-102">Tipo de recurso FolderView</span><span class="sxs-lookup"><span data-stu-id="cf0cc-102">FolderView resource type</span></span>

<span data-ttu-id="cf0cc-103">El recurso **FolderView** proporciona o establece recomendaciones sobre la experiencia de usuario de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="cf0cc-103">The **FolderView** resource provides or sets recommendations on the user-experience of a folder.</span></span>

<span data-ttu-id="cf0cc-104">Está disponible desde la propiedad [folder][folder-facet] de los recursos [driveItem][item-resource].</span><span class="sxs-lookup"><span data-stu-id="cf0cc-104">It is available from the [folder][folder-facet] property of [driveItem][item-resource] resources.</span></span>

## <a name="json-representation"></a><span data-ttu-id="cf0cc-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="cf0cc-105">JSON representation</span></span>

<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.folderView" } -->

```json
{
  "sortBy": "default | name | type | size | takenOrCreatedDateTime | lastModifiedDateTime | sequence",
  "sortOrder": "ascending | descending",
  "viewType": "default | icons | details | thumbnails"
}
```

## <a name="properties"></a><span data-ttu-id="cf0cc-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cf0cc-106">Properties</span></span>

| <span data-ttu-id="cf0cc-107">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="cf0cc-107">Property name</span></span>         | <span data-ttu-id="cf0cc-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf0cc-108">Type</span></span>   | <span data-ttu-id="cf0cc-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf0cc-109">Description</span></span>
|:----------------------|:-------|:--------------------------------------------
| <span data-ttu-id="cf0cc-110">**sortBy**</span><span class="sxs-lookup"><span data-stu-id="cf0cc-110">**sortBy**</span></span>            | <span data-ttu-id="cf0cc-111">string</span><span class="sxs-lookup"><span data-stu-id="cf0cc-111">string</span></span> | <span data-ttu-id="cf0cc-112">El método mediante el que se ordena la carpeta.</span><span class="sxs-lookup"><span data-stu-id="cf0cc-112">The method by which the folder should be sorted.</span></span>
| <span data-ttu-id="cf0cc-113">**sortOrder**</span><span class="sxs-lookup"><span data-stu-id="cf0cc-113">**sortOrder**</span></span>         | <span data-ttu-id="cf0cc-114">string</span><span class="sxs-lookup"><span data-stu-id="cf0cc-114">string</span></span> | <span data-ttu-id="cf0cc-115">Si es True, indica que los elementos deben ordenarse en orden descendente.</span><span class="sxs-lookup"><span data-stu-id="cf0cc-115">If true, indicates that items should be sorted in descending order.</span></span> <span data-ttu-id="cf0cc-116">De otro modo, los elementos deben ordenarse en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="cf0cc-116">Otherwise, items should be sorted ascending.</span></span>
| <span data-ttu-id="cf0cc-117">**viewType**</span><span class="sxs-lookup"><span data-stu-id="cf0cc-117">**viewType**</span></span>          | <span data-ttu-id="cf0cc-118">string</span><span class="sxs-lookup"><span data-stu-id="cf0cc-118">string</span></span> | <span data-ttu-id="cf0cc-119">El tipo de vista que se debe usar para representar la carpeta.</span><span class="sxs-lookup"><span data-stu-id="cf0cc-119">The type of view that should be used to represent the folder.</span></span>

<span data-ttu-id="cf0cc-120">Puede usar la propiedad _sortBy_ para controlar el criterio de ordenación de los elementos en aplicaciones que respetan la faceta **viewType**.</span><span class="sxs-lookup"><span data-stu-id="cf0cc-120">You can use the _sortBy_ property to control the sort order of the items in applications that respect the **viewType** facet.</span></span>

### <a name="sortby-options"></a><span data-ttu-id="cf0cc-121">sortBy opciones</span><span class="sxs-lookup"><span data-stu-id="cf0cc-121">sortBy options</span></span>

<span data-ttu-id="cf0cc-122">Los siguientes valores se definen para la propiedad **sortBy**.</span><span class="sxs-lookup"><span data-stu-id="cf0cc-122">The following values are defined for the **sortBy** property.</span></span>

| <span data-ttu-id="cf0cc-123">Valor</span><span class="sxs-lookup"><span data-stu-id="cf0cc-123">Value</span></span>                    | <span data-ttu-id="cf0cc-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf0cc-124">Description</span></span>
| ------------------------ | --------------------------------------------------
| `default`                | <span data-ttu-id="cf0cc-125">El criterio de ordenación predeterminado de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cf0cc-125">The default sort order of the application.</span></span>
| `name`                   | <span data-ttu-id="cf0cc-126">Los elementos deben organizarse por la propiedad **name** de los elementos.</span><span class="sxs-lookup"><span data-stu-id="cf0cc-126">Items should be arranged by the **name** property of the items.</span></span>
| `type`                   | <span data-ttu-id="cf0cc-127">Los elementos deben organizarse por el tipo de los elementos.</span><span class="sxs-lookup"><span data-stu-id="cf0cc-127">Items should be arranged by the type of item.</span></span>
| `size`                   | <span data-ttu-id="cf0cc-128">Los elementos deben organizarse por la propiedad **size** de los elementos.</span><span class="sxs-lookup"><span data-stu-id="cf0cc-128">Items should be arranged by the **size** property of the items.</span></span>
| `takenOrCreatedDateTime` | <span data-ttu-id="cf0cc-129">Los elementos deben organizarse por la propiedad **takenDateTime** de la faceta **photo**.</span><span class="sxs-lookup"><span data-stu-id="cf0cc-129">Items should be arranged by the **takenDateTime** property of the **photo** facet.</span></span> <span data-ttu-id="cf0cc-130">Si no está disponible, debe usarse la propiedad **createdDateTime**.</span><span class="sxs-lookup"><span data-stu-id="cf0cc-130">If not available, the **createdDateTime** property should be used.</span></span>
| `lastModifiedDateTime`   | <span data-ttu-id="cf0cc-131">Los elementos deben organizarse por la propiedad **lastModifiedDateTime** de los elementos.</span><span class="sxs-lookup"><span data-stu-id="cf0cc-131">Items should be arranged by the **lastModifiedDateTime** property of the items.</span></span>
| `sequence`               | <span data-ttu-id="cf0cc-132">Los elementos siguen una secuencia personalizada especificada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="cf0cc-132">Items follow a custom sequence specified by the user.</span></span>


### <a name="sortorder-options"></a><span data-ttu-id="cf0cc-133">Opciones de sortOrder</span><span class="sxs-lookup"><span data-stu-id="cf0cc-133">sortOrder options</span></span>

<span data-ttu-id="cf0cc-134">Los siguientes valores se definen para la propiedad **sortOrder**.</span><span class="sxs-lookup"><span data-stu-id="cf0cc-134">The following values are defined for the **sortOrder** property.</span></span>

| <span data-ttu-id="cf0cc-135">Valor</span><span class="sxs-lookup"><span data-stu-id="cf0cc-135">Value</span></span>        | <span data-ttu-id="cf0cc-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf0cc-136">Description</span></span>
| ------------ | --------------------------------------------------------------
| `ascending`  | <span data-ttu-id="cf0cc-137">Los elementos deben organizarse en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="cf0cc-137">Items should be arranged in ascending order.</span></span>
| `descending` | <span data-ttu-id="cf0cc-138">Los elementos deben organizarse en orden descendente.</span><span class="sxs-lookup"><span data-stu-id="cf0cc-138">Items should be arranged in descending order.</span></span>


### <a name="viewtype-options"></a><span data-ttu-id="cf0cc-139">viewType opciones</span><span class="sxs-lookup"><span data-stu-id="cf0cc-139">viewType options</span></span>

<span data-ttu-id="cf0cc-140">Los siguientes valores se definen para la propiedad **viewType**.</span><span class="sxs-lookup"><span data-stu-id="cf0cc-140">The following values are defined for the **viewType** property.</span></span>

| <span data-ttu-id="cf0cc-141">Valor</span><span class="sxs-lookup"><span data-stu-id="cf0cc-141">Value</span></span>        | <span data-ttu-id="cf0cc-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf0cc-142">Description</span></span>
| ------------ | --------------------------------------------------------------
| `default`    | <span data-ttu-id="cf0cc-143">El tipo de vista predeterminado para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cf0cc-143">The default view type for the application.</span></span>
| `icons`      | <span data-ttu-id="cf0cc-144">Una vista que usa iconos para representar driveItems.</span><span class="sxs-lookup"><span data-stu-id="cf0cc-144">A view that uses icons to represent driveItems.</span></span>
| `details`    | <span data-ttu-id="cf0cc-145">Una vista con varias columnas que proporcionan detalles adicionales sobre cada elemento.</span><span class="sxs-lookup"><span data-stu-id="cf0cc-145">A view with multiple columns that provide additional details about each item.</span></span>
| `thumbnails` | <span data-ttu-id="cf0cc-146">Una vista que usa miniaturas más grandes de driveItems para representar los elementos.</span><span class="sxs-lookup"><span data-stu-id="cf0cc-146">A view that uses larger thumbnails of driveItems to represent the items.</span></span>


[item-resource]: driveitem.md
[folder-facet]: folder.md

<!-- {
  "type": "#page.annotation",
  "description": "The FolderView facet provides or sets recommendations on the user-experience of a folder.",
  "keywords": "view, folderview, sortby, sortorder, viewtype, coversourceid, folder",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/resources/folderview.md:
      Found potential enums in resource example that weren't defined in a table:(default,icons,details,thumbnails) are in resource, but () are in table",
    "Warning: /api-reference/v1.0/resources/folderview.md:
      Found potential enums in resource example that weren't defined in a table:(default,name,type,size,takenOrCreatedDateTime,lastModifiedDateTime,sequence) are in resource, but () are in table",
    "Warning: /api-reference/v1.0/resources/folderview.md:
      Found potential enums in resource example that weren't defined in a table:(ascending,descending) are in resource, but () are in table"
  ],
  "tocPath": "Facets/FolderView"
} -->
