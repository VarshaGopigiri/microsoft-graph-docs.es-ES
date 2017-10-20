---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: ListItem
ms.openlocfilehash: eabb88eb6ad2eee7a032b2486555aa26c557ba1a
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="listitem-resource"></a><span data-ttu-id="923b3-102">Recurso ListItem</span><span class="sxs-lookup"><span data-stu-id="923b3-102">ListItem resource</span></span>

<span data-ttu-id="923b3-103">Este recurso representa un elemento en una **[lista][]** de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="923b3-103">This resource represents an item in a SharePoint **[list][]**.</span></span>
<span data-ttu-id="923b3-104">Los valores de columna de la lista están disponibles a través del diccionario `fieldValueSet`.</span><span class="sxs-lookup"><span data-stu-id="923b3-104">Column values in the list are available through the `fieldValueSet` dictionary.</span></span>

## <a name="tasks-on-a-listitem"></a><span data-ttu-id="923b3-105">Tareas en un recurso listItem</span><span class="sxs-lookup"><span data-stu-id="923b3-105">Tasks on a listItem</span></span>

<span data-ttu-id="923b3-106">Las tareas siguientes están disponibles para los recursos **listItem**.</span><span class="sxs-lookup"><span data-stu-id="923b3-106">The following tasks are available for {type} resources.</span></span>
<span data-ttu-id="923b3-107">Todos los ejemplos siguientes son relativos a una **[lista][]**, por ejemplo: `https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}`.</span><span class="sxs-lookup"><span data-stu-id="923b3-107">All examples below are relative to a **[list][]**, eg: `https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}`.</span></span>

| <span data-ttu-id="923b3-108">Tarea común</span><span class="sxs-lookup"><span data-stu-id="923b3-108">Common task</span></span>                    | <span data-ttu-id="923b3-109">Método HTTP</span><span class="sxs-lookup"><span data-stu-id="923b3-109">HTTP method</span></span>
|:-------------------------------|:------------------------
| <span data-ttu-id="923b3-110">[Obtener][]</span><span class="sxs-lookup"><span data-stu-id="923b3-110">[Get][]</span></span>                        | <span data-ttu-id="923b3-111">GET /items/{item-id}</span><span class="sxs-lookup"><span data-stu-id="923b3-111">GET /items/{item-id}</span></span>
| <span data-ttu-id="923b3-112">[Obtener valores de columna][Obtener]</span><span class="sxs-lookup"><span data-stu-id="923b3-112">[Get column values][Get]</span></span>       | <span data-ttu-id="923b3-113">GET /items/{item-id}?expand=fields</span><span class="sxs-lookup"><span data-stu-id="923b3-113">GET /items/{item-id}?expand=fields</span></span>
| <span data-ttu-id="923b3-114">[Crear][]</span><span class="sxs-lookup"><span data-stu-id="923b3-114">[Create][]</span></span>                     | <span data-ttu-id="923b3-115">POST /items</span><span class="sxs-lookup"><span data-stu-id="923b3-115">POST /items</span></span>
| <span data-ttu-id="923b3-116">[Eliminar][]</span><span class="sxs-lookup"><span data-stu-id="923b3-116">[Delete][]</span></span>                     | <span data-ttu-id="923b3-117">DELETE /items/{item-id}</span><span class="sxs-lookup"><span data-stu-id="923b3-117">DELETE /items/{item-id}</span></span>
| <span data-ttu-id="923b3-118">[Actualizar][]</span><span class="sxs-lookup"><span data-stu-id="923b3-118">[Update][]</span></span>                     | <span data-ttu-id="923b3-119">PATCH /items/{item-id}</span><span class="sxs-lookup"><span data-stu-id="923b3-119">PATCH /items/{item-id}</span></span>
| <span data-ttu-id="923b3-120">[Actualizar valores de columna][Actualizar]</span><span class="sxs-lookup"><span data-stu-id="923b3-120">[Update column values][Update]</span></span> | <span data-ttu-id="923b3-121">PATCH /items/{item-id}/fields</span><span class="sxs-lookup"><span data-stu-id="923b3-121">PATCH /items/{item-id}/fields</span></span>

[Obtener]: ../api/listItem_get.md
[Crear]: ../api/listItem_create.md
[Eliminar]: ../api/listItem_delete.md
[Actualizar]: ../api/listItem_update.md

## <a name="json-representation"></a><span data-ttu-id="923b3-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="923b3-126">JSON representation</span></span>

<span data-ttu-id="923b3-127">A continuación se incluye una representación JSON del recurso **listItem**.</span><span class="sxs-lookup"><span data-stu-id="923b3-127">Here is a JSON representation of a **baseItem** resource.</span></span>

<!-- { "blockType": "resource", 
       "@odata.type": "microsoft.graph.listItem",
       "keyProperty": "id" } -->

```json
{
  "contentType": { "@odata.type": "microsoft.graph.contentType" },
  "fields": { "@odata.type": "microsoft.graph.fieldValueSet" },

  /* relationships */
  "driveItem": { "@odata.type": "microsoft.graph.driveItem" },

  /* inherited from baseItem */
  "id": "string",
  "name": "name of resource",
  "createdBy": { "@odata.type": "microsoft.graph.identitySet" },
  "createdDateTime": "timestamp",
  "description": "description of resource",
  "eTag": "string",
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "timestamp",
  "webUrl": "url"
}
```

## <a name="properties"></a><span data-ttu-id="923b3-128">Propiedades</span><span class="sxs-lookup"><span data-stu-id="923b3-128">Properties</span></span>

<span data-ttu-id="923b3-129">El recurso **listItem** tiene las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="923b3-129">The **listItem** resource has the following properties.</span></span>

| <span data-ttu-id="923b3-130">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="923b3-130">Property name</span></span> | <span data-ttu-id="923b3-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="923b3-131">Type</span></span>                | <span data-ttu-id="923b3-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="923b3-132">Description</span></span>
|:--------------|:--------------------|:-------------------------------
| <span data-ttu-id="923b3-133">contentType</span><span class="sxs-lookup"><span data-stu-id="923b3-133">contentType</span></span>   | <span data-ttu-id="923b3-134">[contentTypeInfo][]</span><span class="sxs-lookup"><span data-stu-id="923b3-134">[contentTypeInfo][]</span></span> | <span data-ttu-id="923b3-135">El tipo de contenido de este elemento de lista</span><span class="sxs-lookup"><span data-stu-id="923b3-135">The content type of this list item</span></span>
| <span data-ttu-id="923b3-136">fields</span><span class="sxs-lookup"><span data-stu-id="923b3-136">fields</span></span>        | <span data-ttu-id="923b3-137">[fieldValueSet][]</span><span class="sxs-lookup"><span data-stu-id="923b3-137">[fieldValueSet][]</span></span>   | <span data-ttu-id="923b3-138">Los valores de las columnas establecidos en este elemento de lista.</span><span class="sxs-lookup"><span data-stu-id="923b3-138">The values of the columns set on this list item.</span></span>

<span data-ttu-id="923b3-139">Las siguientes propiedades se heredan de **[baseItem][]**.</span><span class="sxs-lookup"><span data-stu-id="923b3-139">The following properties are inherited from **[baseItem][]**.</span></span>

| <span data-ttu-id="923b3-140">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="923b3-140">Property name</span></span>        | <span data-ttu-id="923b3-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="923b3-141">Type</span></span>             | <span data-ttu-id="923b3-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="923b3-142">Description</span></span>
|:---------------------|:-----------------|:-----------------------------------
| <span data-ttu-id="923b3-143">id</span><span class="sxs-lookup"><span data-stu-id="923b3-143">id</span></span>                   | <span data-ttu-id="923b3-144">string</span><span class="sxs-lookup"><span data-stu-id="923b3-144">string</span></span>           | <span data-ttu-id="923b3-p103">El identificador único del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="923b3-p103">The unique identifier of the item. Read-only.</span></span>
| <span data-ttu-id="923b3-147">name</span><span class="sxs-lookup"><span data-stu-id="923b3-147">name</span></span>                 | <span data-ttu-id="923b3-148">string</span><span class="sxs-lookup"><span data-stu-id="923b3-148">string</span></span>           | <span data-ttu-id="923b3-149">Nombre o título del elemento.</span><span class="sxs-lookup"><span data-stu-id="923b3-149">The name / title of the item.</span></span>
| <span data-ttu-id="923b3-150">createdBy</span><span class="sxs-lookup"><span data-stu-id="923b3-150">createdBy</span></span>            | <span data-ttu-id="923b3-151">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="923b3-151">[identitySet][]</span></span>  | <span data-ttu-id="923b3-152">Identidad del creador de este elemento.</span><span class="sxs-lookup"><span data-stu-id="923b3-152">Identity of the creator of this item.</span></span> <span data-ttu-id="923b3-153">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="923b3-153">Read-only.</span></span>
| <span data-ttu-id="923b3-154">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="923b3-154">createdDateTime</span></span>      | <span data-ttu-id="923b3-155">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="923b3-155">DateTimeOffset</span></span>   | <span data-ttu-id="923b3-p105">La fecha y la hora de creación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="923b3-p105">The date and time the item was created. Read-only.</span></span>
| <span data-ttu-id="923b3-158">descripción</span><span class="sxs-lookup"><span data-stu-id="923b3-158">description</span></span>          | <span data-ttu-id="923b3-159">string</span><span class="sxs-lookup"><span data-stu-id="923b3-159">string</span></span>           | <span data-ttu-id="923b3-160">Texto descriptivo del elemento.</span><span class="sxs-lookup"><span data-stu-id="923b3-160">The descriptive text for the site.</span></span>
| <span data-ttu-id="923b3-161">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="923b3-161">lastModifiedBy</span></span>       | <span data-ttu-id="923b3-162">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="923b3-162">[identitySet][]</span></span>  | <span data-ttu-id="923b3-163">Identidad del usuario que modificó por última vez este elemento.</span><span class="sxs-lookup"><span data-stu-id="923b3-163">Identity of the last modifier of this item.</span></span> <span data-ttu-id="923b3-164">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="923b3-164">Read-only.</span></span>
| <span data-ttu-id="923b3-165">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="923b3-165">lastModifiedDateTime</span></span> | <span data-ttu-id="923b3-166">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="923b3-166">DateTimeOffset</span></span>   | <span data-ttu-id="923b3-p107">Fecha y hora de la última modificación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="923b3-p107">The date and time the item was last modified. Read-only.</span></span>
| <span data-ttu-id="923b3-169">webUrl</span><span class="sxs-lookup"><span data-stu-id="923b3-169">webUrl</span></span>               | <span data-ttu-id="923b3-170">string (url)</span><span class="sxs-lookup"><span data-stu-id="923b3-170">string (url)</span></span>     | <span data-ttu-id="923b3-p108">Dirección URL que muestra el elemento en el explorador. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="923b3-p108">URL that displays the item in the browser. Read-only.</span></span>

## <a name="relationships"></a><span data-ttu-id="923b3-173">Relaciones</span><span class="sxs-lookup"><span data-stu-id="923b3-173">Relationships</span></span>

 <span data-ttu-id="923b3-174">El recurso **listItem** tiene las siguientes relaciones con otros recursos.</span><span class="sxs-lookup"><span data-stu-id="923b3-174">The **listItem** resource has the following relationships to other resources.</span></span>

| <span data-ttu-id="923b3-175">Nombre de la relación</span><span class="sxs-lookup"><span data-stu-id="923b3-175">Relationship name</span></span> | <span data-ttu-id="923b3-176">Tipo</span><span class="sxs-lookup"><span data-stu-id="923b3-176">Type</span></span>                        | <span data-ttu-id="923b3-177">Descripción</span><span class="sxs-lookup"><span data-stu-id="923b3-177">Description</span></span>
|:------------------|:----------------------------|:-------------------------------
| <span data-ttu-id="923b3-178">driveItem</span><span class="sxs-lookup"><span data-stu-id="923b3-178">driveItem</span></span>         | <span data-ttu-id="923b3-179">[driveItem][]</span><span class="sxs-lookup"><span data-stu-id="923b3-179">[driveItem][]</span></span>               | <span data-ttu-id="923b3-180">Para bibliotecas de documentos, la relación **driveItem** expone el recurso listItem como un recurso **[driveItem][]**</span><span class="sxs-lookup"><span data-stu-id="923b3-180">For document libraries, the **driveItem** relationship exposes the listItem as a **[driveItem][]**</span></span>

[baseItem]: baseItem.md
[contentTypeInfo]: contentTypeInfo.md
[driveItem]: driveItem.md
[fieldValueSet]: fieldValueSet.md
[identitySet]: identitySet.md
[list]: list.md

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/ListItem",
  "tocBookmarks": {
    "ListItem": "#"
  }
} -->
