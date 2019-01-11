---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: FolderView
localization_priority: Normal
ms.openlocfilehash: 717dd93d82f109926cabf0168e4e176d7c68cd35
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27861540"
---
# <a name="folderview-resource-type"></a><span data-ttu-id="291c0-102">Tipo de recurso FolderView</span><span class="sxs-lookup"><span data-stu-id="291c0-102">FolderView resource type</span></span>

> <span data-ttu-id="291c0-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="291c0-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="291c0-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="291c0-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="291c0-105">El recurso **FolderView** proporciona o establece recomendaciones sobre la experiencia de usuario de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="291c0-105">The **FolderView** resource provides or sets recommendations on the user-experience of a folder.</span></span>

<span data-ttu-id="291c0-106">Está disponible desde la propiedad [folder][folder-facet] de los recursos [driveItem][item-resource].</span><span class="sxs-lookup"><span data-stu-id="291c0-106">It is available from the [folder][folder-facet] property of [driveItem][item-resource] resources.</span></span>

## <a name="json-representation"></a><span data-ttu-id="291c0-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="291c0-107">JSON representation</span></span>

<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.folderView" } -->

```json
{
  "sortBy": "default | name | type | size | takenOrCreatedDateTime | lastModifiedDateTime | sequence",
  "sortDescending": "ascending | descending",
  "viewType": "default | icons | details | thumbnails"
}
```

## <a name="properties"></a><span data-ttu-id="291c0-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="291c0-108">Properties</span></span>

| <span data-ttu-id="291c0-109">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="291c0-109">Property name</span></span>         | <span data-ttu-id="291c0-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="291c0-110">Type</span></span>   | <span data-ttu-id="291c0-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="291c0-111">Description</span></span>
|:----------------------|:-------|:--------------------------------------------
| <span data-ttu-id="291c0-112">**sortBy**</span><span class="sxs-lookup"><span data-stu-id="291c0-112">**sortBy**</span></span>            | <span data-ttu-id="291c0-113">string</span><span class="sxs-lookup"><span data-stu-id="291c0-113">string</span></span> | <span data-ttu-id="291c0-114">El método mediante el que se ordena la carpeta.</span><span class="sxs-lookup"><span data-stu-id="291c0-114">The method by which the folder should be sorted.</span></span>
| <span data-ttu-id="291c0-115">**sortOrder**</span><span class="sxs-lookup"><span data-stu-id="291c0-115">**sortOrder**</span></span>         | <span data-ttu-id="291c0-116">string</span><span class="sxs-lookup"><span data-stu-id="291c0-116">string</span></span> | <span data-ttu-id="291c0-117">Si es True, indica que los elementos deben ordenarse en orden descendente.</span><span class="sxs-lookup"><span data-stu-id="291c0-117">If true, indicates that items should be sorted in descending order.</span></span> <span data-ttu-id="291c0-118">De otro modo, los elementos deben ordenarse en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="291c0-118">Otherwise, items should be sorted ascending.</span></span>
| <span data-ttu-id="291c0-119">**viewType**</span><span class="sxs-lookup"><span data-stu-id="291c0-119">**viewType**</span></span>          | <span data-ttu-id="291c0-120">string</span><span class="sxs-lookup"><span data-stu-id="291c0-120">string</span></span> | <span data-ttu-id="291c0-121">El tipo de vista que se debe usar para representar la carpeta.</span><span class="sxs-lookup"><span data-stu-id="291c0-121">The type of view that should be used to represent the folder.</span></span>

<span data-ttu-id="291c0-122">Puede usar la propiedad _sortBy_ para controlar el criterio de ordenación de los elementos en aplicaciones que respetan la faceta **viewType**.</span><span class="sxs-lookup"><span data-stu-id="291c0-122">You can use the _sortBy_ property to control the sort order of the items in applications that respect the **viewType** facet.</span></span>

### <a name="sortby-values"></a><span data-ttu-id="291c0-123">Valores sortBy</span><span class="sxs-lookup"><span data-stu-id="291c0-123">sortBy values</span></span>

<span data-ttu-id="291c0-124">Los siguientes valores se definen para la propiedad **sortBy**.</span><span class="sxs-lookup"><span data-stu-id="291c0-124">The following values are defined for the **sortBy** property.</span></span>

| <span data-ttu-id="291c0-125">Valor</span><span class="sxs-lookup"><span data-stu-id="291c0-125">Value</span></span>                    | <span data-ttu-id="291c0-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="291c0-126">Description</span></span>
| ------------------------ | --------------------------------------------------
| `default`                | <span data-ttu-id="291c0-127">El criterio de ordenación predeterminado de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="291c0-127">The default sort order of the application.</span></span>
| `name`                   | <span data-ttu-id="291c0-128">Los elementos deben organizarse por la propiedad **name** de los elementos.</span><span class="sxs-lookup"><span data-stu-id="291c0-128">Items should be arranged by the **name** property of the items.</span></span>
| `type`                   | <span data-ttu-id="291c0-129">Los elementos deben organizarse por el tipo de los elementos.</span><span class="sxs-lookup"><span data-stu-id="291c0-129">Items should be arranged by the type of item.</span></span>
| `size`                   | <span data-ttu-id="291c0-130">Los elementos deben organizarse por la propiedad **size** de los elementos.</span><span class="sxs-lookup"><span data-stu-id="291c0-130">Items should be arranged by the **size** property of the items.</span></span>
| `takenOrCreatedDateTime` | <span data-ttu-id="291c0-131">Los elementos deben organizarse por la propiedad **takenDateTime** de la faceta **photo**.</span><span class="sxs-lookup"><span data-stu-id="291c0-131">Items should be arranged by the **takenDateTime** property of the **photo** facet.</span></span> <span data-ttu-id="291c0-132">Si no está disponible, debe usarse la propiedad **createdDateTime**.</span><span class="sxs-lookup"><span data-stu-id="291c0-132">If not available, the **createdDateTime** property should be used.</span></span>
| `lastModifiedDateTime`   | <span data-ttu-id="291c0-133">Los elementos deben organizarse por la propiedad **lastModifiedDateTime** de los elementos.</span><span class="sxs-lookup"><span data-stu-id="291c0-133">Items should be arranged by the **lastModifiedDateTime** property of the items.</span></span>
| `sequence`               | <span data-ttu-id="291c0-134">Los elementos siguen una secuencia personalizada especificada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="291c0-134">Items follow a custom sequence specified by the user.</span></span>


### <a name="sortorder-values"></a><span data-ttu-id="291c0-135">Valores sortOrder</span><span class="sxs-lookup"><span data-stu-id="291c0-135">sortOrder values</span></span>

<span data-ttu-id="291c0-136">Los siguientes valores se definen para la propiedad **sortOrder**.</span><span class="sxs-lookup"><span data-stu-id="291c0-136">The following values are defined for the **sortOrder** property.</span></span>

| <span data-ttu-id="291c0-137">Valor</span><span class="sxs-lookup"><span data-stu-id="291c0-137">Value</span></span>        | <span data-ttu-id="291c0-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="291c0-138">Description</span></span>
| ------------ | --------------------------------------------------------------
| `ascending`  | <span data-ttu-id="291c0-139">Los elementos deben organizarse en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="291c0-139">Items should be arranged in ascending order.</span></span>
| `descending` | <span data-ttu-id="291c0-140">Los elementos deben organizarse en orden descendente.</span><span class="sxs-lookup"><span data-stu-id="291c0-140">Items should be arranged in descending order.</span></span>


### <a name="viewtype-values"></a><span data-ttu-id="291c0-141">Valores viewType</span><span class="sxs-lookup"><span data-stu-id="291c0-141">viewType values</span></span>

<span data-ttu-id="291c0-142">Los siguientes valores se definen para la propiedad **viewType**.</span><span class="sxs-lookup"><span data-stu-id="291c0-142">The following values are defined for the **viewType** property.</span></span>

| <span data-ttu-id="291c0-143">Valor</span><span class="sxs-lookup"><span data-stu-id="291c0-143">Value</span></span>        | <span data-ttu-id="291c0-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="291c0-144">Description</span></span>
| ------------ | --------------------------------------------------------------
| `default`    | <span data-ttu-id="291c0-145">El tipo de vista predeterminado para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="291c0-145">The default view type for the application.</span></span>
| `icons`      | <span data-ttu-id="291c0-146">Una vista que usa iconos para representar driveItems.</span><span class="sxs-lookup"><span data-stu-id="291c0-146">A view that uses icons to represent driveItems.</span></span>
| `details`    | <span data-ttu-id="291c0-147">Una vista con varias columnas que proporcionan detalles adicionales sobre cada elemento.</span><span class="sxs-lookup"><span data-stu-id="291c0-147">A view with multiple columns that provide additional details about each item.</span></span>
| `thumbnails` | <span data-ttu-id="291c0-148">Una vista que usa miniaturas más grandes de driveItems para representar los elementos.</span><span class="sxs-lookup"><span data-stu-id="291c0-148">A view that uses larger thumbnails of driveItems to represent the items.</span></span>


[item-resource]: driveitem.md
[folder-facet]: folder.md

<!-- uuid: f9e446fd-190b-4692-a605-bb60e78f1f19
2017-05-03 02:34:40 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "folderView resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
