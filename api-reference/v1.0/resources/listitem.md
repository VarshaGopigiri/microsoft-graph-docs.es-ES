---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: ListItem
ms.openlocfilehash: 0f5afaeff29da6f3a6330975adece44731e014bc
ms.sourcegitcommit: 4bdff5fdaea824c7c1204ec7dd641abc282d32a1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/30/2018
---
# <a name="listitem-resource"></a><span data-ttu-id="41b12-102">Recurso ListItem</span><span class="sxs-lookup"><span data-stu-id="41b12-102">ListItem resource</span></span>

<span data-ttu-id="41b12-103">Este recurso representa un elemento en una **[lista][]** de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="41b12-103">This resource represents an item in a SharePoint **[list][]**.</span></span>
<span data-ttu-id="41b12-104">Los valores de columna de la lista están disponibles a través del diccionario `fieldValueSet`.</span><span class="sxs-lookup"><span data-stu-id="41b12-104">Column values in the list are available through the `fieldValueSet` dictionary.</span></span>

## <a name="tasks-on-a-listitem"></a><span data-ttu-id="41b12-105">Tareas en un recurso listItem</span><span class="sxs-lookup"><span data-stu-id="41b12-105">Tasks on a listItem</span></span>

<span data-ttu-id="41b12-106">Las tareas siguientes están disponibles para los recursos **listItem**.</span><span class="sxs-lookup"><span data-stu-id="41b12-106">The following tasks are available for **listItem** resources.</span></span>
<span data-ttu-id="41b12-107">Todos los ejemplos siguientes son relativos a una **[lista][]**, por ejemplo: `https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}`.</span><span class="sxs-lookup"><span data-stu-id="41b12-107">All examples below are relative to a **[list][]**, eg: `https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}`.</span></span>

| <span data-ttu-id="41b12-108">Tarea común</span><span class="sxs-lookup"><span data-stu-id="41b12-108">Common task</span></span>                    | <span data-ttu-id="41b12-109">Método HTTP</span><span class="sxs-lookup"><span data-stu-id="41b12-109">HTTP method</span></span>
|:-------------------------------|:------------------------
| <span data-ttu-id="41b12-110">[Obtener][]</span><span class="sxs-lookup"><span data-stu-id="41b12-110">[Get][]</span></span>                        | <span data-ttu-id="41b12-111">GET /items/{item-id}</span><span class="sxs-lookup"><span data-stu-id="41b12-111">GET /items/{item-id}</span></span>
| <span data-ttu-id="41b12-112">[Obtener valores de columna][Obtener]</span><span class="sxs-lookup"><span data-stu-id="41b12-112">[Get column values][Get]</span></span>       | <span data-ttu-id="41b12-113">GET /items/{item-id}?expand=fields</span><span class="sxs-lookup"><span data-stu-id="41b12-113">GET /items/{item-id}?expand=fields</span></span>
| <span data-ttu-id="41b12-114">[Crear][]</span><span class="sxs-lookup"><span data-stu-id="41b12-114">[Create][]</span></span>                     | <span data-ttu-id="41b12-115">POST /items</span><span class="sxs-lookup"><span data-stu-id="41b12-115">POST /items</span></span>
| <span data-ttu-id="41b12-116">[Eliminar][]</span><span class="sxs-lookup"><span data-stu-id="41b12-116">[Delete][]</span></span>                     | <span data-ttu-id="41b12-117">DELETE /items/{item-id}</span><span class="sxs-lookup"><span data-stu-id="41b12-117">DELETE /items/{item-id}</span></span>
| <span data-ttu-id="41b12-118">[Actualizar][]</span><span class="sxs-lookup"><span data-stu-id="41b12-118">[Update][]</span></span>                     | <span data-ttu-id="41b12-119">PATCH /items/{item-id}</span><span class="sxs-lookup"><span data-stu-id="41b12-119">PATCH /items/{item-id}</span></span>
| <span data-ttu-id="41b12-120">[Actualizar valores de columna][Actualizar]</span><span class="sxs-lookup"><span data-stu-id="41b12-120">[Update column values][Update]</span></span> | <span data-ttu-id="41b12-121">PATCH /items/{item-id}/fields</span><span class="sxs-lookup"><span data-stu-id="41b12-121">PATCH /items/{item-id}/fields</span></span>

[Obtener]: ../api/listItem_get.md
[Crear]: ../api/listItem_create.md
[Eliminar]: ../api/listItem_delete.md
[Actualizar]: ../api/listItem_update.md

## <a name="json-representation"></a><span data-ttu-id="41b12-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="41b12-126">JSON representation</span></span>

<span data-ttu-id="41b12-127">A continuación se incluye una representación JSON del recurso **listItem**.</span><span class="sxs-lookup"><span data-stu-id="41b12-127">Here is a JSON representation of a **listItem** resource.</span></span>

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

## <a name="properties"></a><span data-ttu-id="41b12-128">Propiedades</span><span class="sxs-lookup"><span data-stu-id="41b12-128">Properties</span></span>

<span data-ttu-id="41b12-129">El recurso **listItem** tiene las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="41b12-129">The **listItem** resource has the following properties.</span></span>

| <span data-ttu-id="41b12-130">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="41b12-130">Property name</span></span> | <span data-ttu-id="41b12-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="41b12-131">Type</span></span>                | <span data-ttu-id="41b12-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="41b12-132">Description</span></span>
|:--------------|:--------------------|:-------------------------------
| <span data-ttu-id="41b12-133">contentType</span><span class="sxs-lookup"><span data-stu-id="41b12-133">contentType</span></span>   | <span data-ttu-id="41b12-134">[contentTypeInfo][]</span><span class="sxs-lookup"><span data-stu-id="41b12-134">[contentTypeInfo][]</span></span> | <span data-ttu-id="41b12-135">El tipo de contenido de este elemento de lista</span><span class="sxs-lookup"><span data-stu-id="41b12-135">The content type of this list item</span></span>
| <span data-ttu-id="41b12-136">fields</span><span class="sxs-lookup"><span data-stu-id="41b12-136">fields</span></span>        | <span data-ttu-id="41b12-137">[fieldValueSet][]</span><span class="sxs-lookup"><span data-stu-id="41b12-137">[fieldValueSet][]</span></span>   | <span data-ttu-id="41b12-138">Los valores de las columnas establecidos en este elemento de lista.</span><span class="sxs-lookup"><span data-stu-id="41b12-138">The values of the columns set on this list item.</span></span>

<span data-ttu-id="41b12-139">Las siguientes propiedades se heredan de **[baseItem][]**.</span><span class="sxs-lookup"><span data-stu-id="41b12-139">The following properties are inherited from **[baseItem][]**.</span></span>

| <span data-ttu-id="41b12-140">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="41b12-140">Property name</span></span>        | <span data-ttu-id="41b12-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="41b12-141">Type</span></span>             | <span data-ttu-id="41b12-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="41b12-142">Description</span></span>
|:---------------------|:-----------------|:-----------------------------------
| <span data-ttu-id="41b12-143">id</span><span class="sxs-lookup"><span data-stu-id="41b12-143">id</span></span>                   | <span data-ttu-id="41b12-144">string</span><span class="sxs-lookup"><span data-stu-id="41b12-144">string</span></span>           | <span data-ttu-id="41b12-p103">El identificador único del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="41b12-p103">The unique identifier of the item. Read-only.</span></span>
| <span data-ttu-id="41b12-147">name</span><span class="sxs-lookup"><span data-stu-id="41b12-147">name</span></span>                 | <span data-ttu-id="41b12-148">string</span><span class="sxs-lookup"><span data-stu-id="41b12-148">string</span></span>           | <span data-ttu-id="41b12-149">Nombre o título del elemento.</span><span class="sxs-lookup"><span data-stu-id="41b12-149">The name / title of the item.</span></span>
| <span data-ttu-id="41b12-150">createdBy</span><span class="sxs-lookup"><span data-stu-id="41b12-150">createdBy</span></span>            | <span data-ttu-id="41b12-151">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="41b12-151">[identitySet][]</span></span>  | <span data-ttu-id="41b12-152">Identidad del creador de este elemento.</span><span class="sxs-lookup"><span data-stu-id="41b12-152">Identity of the creator of this item.</span></span> <span data-ttu-id="41b12-153">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="41b12-153">Read-only.</span></span>
| <span data-ttu-id="41b12-154">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="41b12-154">createdDateTime</span></span>      | <span data-ttu-id="41b12-155">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="41b12-155">DateTimeOffset</span></span>   | <span data-ttu-id="41b12-p105">La fecha y la hora de creación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="41b12-p105">The date and time the item was created. Read-only.</span></span>
| <span data-ttu-id="41b12-158">description</span><span class="sxs-lookup"><span data-stu-id="41b12-158">description</span></span>          | <span data-ttu-id="41b12-159">string</span><span class="sxs-lookup"><span data-stu-id="41b12-159">string</span></span>           | <span data-ttu-id="41b12-160">Texto descriptivo del elemento.</span><span class="sxs-lookup"><span data-stu-id="41b12-160">The descriptive text for the item.</span></span>
| <span data-ttu-id="41b12-161">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="41b12-161">lastModifiedBy</span></span>       | <span data-ttu-id="41b12-162">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="41b12-162">[identitySet][]</span></span>  | <span data-ttu-id="41b12-163">Identidad del usuario que modificó por última vez este elemento.</span><span class="sxs-lookup"><span data-stu-id="41b12-163">Identity of the last modifier of this item.</span></span> <span data-ttu-id="41b12-164">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="41b12-164">Read-only.</span></span>
| <span data-ttu-id="41b12-165">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="41b12-165">lastModifiedDateTime</span></span> | <span data-ttu-id="41b12-166">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="41b12-166">DateTimeOffset</span></span>   | <span data-ttu-id="41b12-p107">Fecha y hora de la última modificación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="41b12-p107">The date and time the item was last modified. Read-only.</span></span>
| <span data-ttu-id="41b12-169">webUrl</span><span class="sxs-lookup"><span data-stu-id="41b12-169">webUrl</span></span>               | <span data-ttu-id="41b12-170">string (url)</span><span class="sxs-lookup"><span data-stu-id="41b12-170">string (url)</span></span>     | <span data-ttu-id="41b12-p108">Dirección URL que muestra el elemento en el explorador. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="41b12-p108">URL that displays the item in the browser. Read-only.</span></span>

## <a name="relationships"></a><span data-ttu-id="41b12-173">Relaciones</span><span class="sxs-lookup"><span data-stu-id="41b12-173">Relationships</span></span>

 <span data-ttu-id="41b12-174">El recurso **listItem** tiene las siguientes relaciones con otros recursos.</span><span class="sxs-lookup"><span data-stu-id="41b12-174">The **listItem** resource has the following relationships to other resources.</span></span>

| <span data-ttu-id="41b12-175">Nombre de la relación</span><span class="sxs-lookup"><span data-stu-id="41b12-175">Relationship name</span></span> | <span data-ttu-id="41b12-176">Tipo</span><span class="sxs-lookup"><span data-stu-id="41b12-176">Type</span></span>                        | <span data-ttu-id="41b12-177">Descripción</span><span class="sxs-lookup"><span data-stu-id="41b12-177">Description</span></span>
|:------------------|:----------------------------|:-------------------------------
| <span data-ttu-id="41b12-178">driveItem</span><span class="sxs-lookup"><span data-stu-id="41b12-178">driveItem</span></span>         | <span data-ttu-id="41b12-179">[driveItem][]</span><span class="sxs-lookup"><span data-stu-id="41b12-179">[driveItem][]</span></span>               | <span data-ttu-id="41b12-180">Para bibliotecas de documentos, la relación **driveItem** expone el recurso listItem como un recurso **[driveItem][]**</span><span class="sxs-lookup"><span data-stu-id="41b12-180">For document libraries, the **driveItem** relationship exposes the listItem as a **[driveItem][]**</span></span>

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
