---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Lista
ms.openlocfilehash: ba0c01ce1887a32bd8b671cf511104e9128b5efb
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="list-resource"></a><span data-ttu-id="749fd-102">Recurso de lista</span><span class="sxs-lookup"><span data-stu-id="749fd-102">List resource</span></span>

<span data-ttu-id="749fd-103">El recurso **list** representa una lista en un [sitio][].</span><span class="sxs-lookup"><span data-stu-id="749fd-103">The **list** resource represents a list in a [site][].</span></span>
<span data-ttu-id="749fd-104">Este recurso contiene las propiedades de nivel superior de la lista, incluidas las definiciones de plantilla y campo.</span><span class="sxs-lookup"><span data-stu-id="749fd-104">This resource contains the top level properties of the list, including template and field definitions.</span></span>

## <a name="tasks-on-a-list"></a><span data-ttu-id="749fd-105">Tareas en una lista</span><span class="sxs-lookup"><span data-stu-id="749fd-105">Tasks on a list</span></span>

<span data-ttu-id="749fd-106">Las tareas siguientes están disponibles para los recursos list.</span><span class="sxs-lookup"><span data-stu-id="749fd-106">The following tasks are available for {type} resources.</span></span>
<span data-ttu-id="749fd-107">**Nota**: Esta versión beta solo permite navegar por listas, no permite crearlas ni actualizarlas.</span><span class="sxs-lookup"><span data-stu-id="749fd-107">**Note:** This beta only allows navigating lists, not creating or updating them.</span></span>
<span data-ttu-id="749fd-108">En cambio, puede crear o actualizar [elementos de lista][listItem].</span><span class="sxs-lookup"><span data-stu-id="749fd-108">You can, however, create or update [list items][listItem].</span></span>

<span data-ttu-id="749fd-109">Todos los ejemplos siguientes son relativos a un sitio, por ejemplo: `https://graph.microsoft.com/beta/sites/{site-id}`.</span><span class="sxs-lookup"><span data-stu-id="749fd-109">All examples below are relative to a site, eg: `https://graph.microsoft.com/beta/sites/{site-id}`.</span></span>

| <span data-ttu-id="749fd-110">Tarea común</span><span class="sxs-lookup"><span data-stu-id="749fd-110">Common task</span></span>               | <span data-ttu-id="749fd-111">Método HTTP</span><span class="sxs-lookup"><span data-stu-id="749fd-111">HTTP method</span></span>
|:--------------------------|:------------------------------
| <span data-ttu-id="749fd-112">[Obtener lista][]</span><span class="sxs-lookup"><span data-stu-id="749fd-112">[Get list][]</span></span>              | <span data-ttu-id="749fd-113">GET /lists/{list-id}</span><span class="sxs-lookup"><span data-stu-id="749fd-113">GET /lists/{list-id}</span></span>
| <span data-ttu-id="749fd-114">[Enumerar elementos de lista][]</span><span class="sxs-lookup"><span data-stu-id="749fd-114">[Enumerate list items][]</span></span>  | <span data-ttu-id="749fd-115">GET /lists/{list-id}/items</span><span class="sxs-lookup"><span data-stu-id="749fd-115">GET /lists/{list-id}/items</span></span>
| <span data-ttu-id="749fd-116">[Actualizar elemento de lista][]</span><span class="sxs-lookup"><span data-stu-id="749fd-116">[Update list item][]</span></span>      | <span data-ttu-id="749fd-117">PATCH /lists/{list-id}/items/{item-id}</span><span class="sxs-lookup"><span data-stu-id="749fd-117">PATCH /lists/{list-id}/items/{item-id}</span></span>
| <span data-ttu-id="749fd-118">[Eliminar elemento de lista][]</span><span class="sxs-lookup"><span data-stu-id="749fd-118">[Delete list item][]</span></span>      | <span data-ttu-id="749fd-119">DELETE /lists/{list-id}/items/{item-id}</span><span class="sxs-lookup"><span data-stu-id="749fd-119">DELETE /lists/{list-id}/items/{item-id}</span></span>
| <span data-ttu-id="749fd-120">[Crear elemento de lista][]</span><span class="sxs-lookup"><span data-stu-id="749fd-120">[Create list item][]</span></span>      | <span data-ttu-id="749fd-121">POST /lists/{list-id}</span><span class="sxs-lookup"><span data-stu-id="749fd-121">POST /lists/{list-id}</span></span>

[Obtener lista]: ../api/list_get.md
[Enumerar elementos de lista]: ../api/listitem_list.md
[Actualizar elemento de lista]: ../api/listItem_update.md
[Eliminar elemento de lista]: ../api/listItem_delete.md
[Crear elemento de lista]: ../api/listItem_create.md

## <a name="json-representation"></a><span data-ttu-id="749fd-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="749fd-127">JSON representation</span></span>

<span data-ttu-id="749fd-128">A continuación se incluye una representación JSON del recurso **list**.</span><span class="sxs-lookup"><span data-stu-id="749fd-128">Here is a JSON representation of a **baseItem** resource.</span></span>

<!-- { "blockType": "resource", 
       "@odata.type": "microsoft.graph.list",
       "keyProperty": "id", 
       "optionalProperties": [ "items", "drive"] } -->

```json
{
  "columns": [ { "@odata.type": "microsoft.graph.columnDefinition" }],
  "contentTypes": [ { "@odata.type": "microsoft.graph.contentType" }],
  "displayName": "title of list",
  "drive": { "@odata.type": "microsoft.graph.drive" },
  "items": [ { "@odata.type": "microsoft.graph.listItem" } ],
  "list": {
    "@odata.type": "microsoft.graph.listInfo",
    "hidden": false,
    "template": "documentLibrary | genericList | survey | links | announcements | contacts ..."
  },
  "system": false,

  /* inherited from baseItem */
  "id": "string",
  "name": "name of list",
  "createdBy": { "@odata.type": "microsoft.graph.identitySet" },
  "createdDateTime": "timestamp",
  "description": "description of list",
  "eTag": "string",
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "timestamp",
  "webUrl": "url to visit the list in a browser"
}
```

## <a name="properties"></a><span data-ttu-id="749fd-129">Propiedades</span><span class="sxs-lookup"><span data-stu-id="749fd-129">Properties</span></span>

<span data-ttu-id="749fd-130">El recurso **list** tiene las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="749fd-130">The **list** resource has the following properties.</span></span>

| <span data-ttu-id="749fd-131">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="749fd-131">Property name</span></span>    | <span data-ttu-id="749fd-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="749fd-132">Type</span></span>                             | <span data-ttu-id="749fd-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="749fd-133">Description</span></span>
|:-----------------|:---------------------------------|:---------------------------
| <span data-ttu-id="749fd-134">**columns**</span><span class="sxs-lookup"><span data-stu-id="749fd-134">**columns**</span></span>      | <span data-ttu-id="749fd-135">Collection([columnDefinition][])</span><span class="sxs-lookup"><span data-stu-id="749fd-135">Collection([columnDefinition][])</span></span> | <span data-ttu-id="749fd-136">La colección de definiciones de campo de esta lista.</span><span class="sxs-lookup"><span data-stu-id="749fd-136">The collection of field definitions for this list.</span></span>
| <span data-ttu-id="749fd-137">**contentTypes**</span><span class="sxs-lookup"><span data-stu-id="749fd-137"><ContentTypes></span></span> | <span data-ttu-id="749fd-138">Collection([contentType][])</span><span class="sxs-lookup"><span data-stu-id="749fd-138">Collection([contentType][])</span></span>      | <span data-ttu-id="749fd-139">La colección de tipos de contenido presentes en esta lista.</span><span class="sxs-lookup"><span data-stu-id="749fd-139">The collection of content types present in this list.</span></span>
| <span data-ttu-id="749fd-140">**displayName**</span><span class="sxs-lookup"><span data-stu-id="749fd-140">**displayName**</span></span>  | <span data-ttu-id="749fd-141">string</span><span class="sxs-lookup"><span data-stu-id="749fd-141">string</span></span>                           | <span data-ttu-id="749fd-142">El título que se puede mostrar de la lista.</span><span class="sxs-lookup"><span data-stu-id="749fd-142">The new title of the list.</span></span>
| <span data-ttu-id="749fd-143">**list**</span><span class="sxs-lookup"><span data-stu-id="749fd-143">**list**</span></span>         | <span data-ttu-id="749fd-144">[listInfo][]</span><span class="sxs-lookup"><span data-stu-id="749fd-144">[listInfo][]</span></span>                     | <span data-ttu-id="749fd-145">Proporciona detalles adicionales sobre la lista.</span><span class="sxs-lookup"><span data-stu-id="749fd-145">Provides additional details about the list.</span></span>
| <span data-ttu-id="749fd-146">**system**</span><span class="sxs-lookup"><span data-stu-id="749fd-146">**System**</span></span>       | <span data-ttu-id="749fd-147">[systemFacet][]</span><span class="sxs-lookup"><span data-stu-id="749fd-147">[systemFacet][]</span></span>                  | <span data-ttu-id="749fd-148">Si está presente, indica que se trata de una lista administrada por el sistema.</span><span class="sxs-lookup"><span data-stu-id="749fd-148">If present, indicates that this is a system-managed list.</span></span> <span data-ttu-id="749fd-149">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="749fd-149">Read-only.</span></span>

<span data-ttu-id="749fd-150">Las siguientes propiedades se heredan de **[baseItem][]**.</span><span class="sxs-lookup"><span data-stu-id="749fd-150">The following properties are inherited from **[baseItem][]**.</span></span>

| <span data-ttu-id="749fd-151">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="749fd-151">Property name</span></span>            | <span data-ttu-id="749fd-152">Tipo</span><span class="sxs-lookup"><span data-stu-id="749fd-152">Type</span></span>             | <span data-ttu-id="749fd-153">Descripción</span><span class="sxs-lookup"><span data-stu-id="749fd-153">Description</span></span>
|:-------------------------|:-----------------|:-------------------------------
| <span data-ttu-id="749fd-154">**id**</span><span class="sxs-lookup"><span data-stu-id="749fd-154">**id**</span></span>                   | <span data-ttu-id="749fd-155">cadena</span><span class="sxs-lookup"><span data-stu-id="749fd-155">string</span></span>           | <span data-ttu-id="749fd-p104">El identificador único del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="749fd-p104">The unique identifier of the item. Read-only.</span></span>
| <span data-ttu-id="749fd-158">**name**</span><span class="sxs-lookup"><span data-stu-id="749fd-158">**name**</span></span>                 | <span data-ttu-id="749fd-159">string</span><span class="sxs-lookup"><span data-stu-id="749fd-159">string</span></span>           | <span data-ttu-id="749fd-160">Nombre del elemento.</span><span class="sxs-lookup"><span data-stu-id="749fd-160">The name of the item.</span></span>
| <span data-ttu-id="749fd-161">**createdBy**</span><span class="sxs-lookup"><span data-stu-id="749fd-161">**createdBy**</span></span>            | <span data-ttu-id="749fd-162">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="749fd-162">[identitySet][]</span></span>  | <span data-ttu-id="749fd-163">Identidad del creador de este elemento.</span><span class="sxs-lookup"><span data-stu-id="749fd-163">Identity of the creator of this item.</span></span> <span data-ttu-id="749fd-164">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="749fd-164">Read-only.</span></span>
| <span data-ttu-id="749fd-165">**createdDateTime**</span><span class="sxs-lookup"><span data-stu-id="749fd-165">**createdDateTime**</span></span>      | <span data-ttu-id="749fd-166">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="749fd-166">DateTimeOffset</span></span>   | <span data-ttu-id="749fd-p106">La fecha y la hora de creación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="749fd-p106">The date and time the item was created. Read-only.</span></span>
| <span data-ttu-id="749fd-169">**description**</span><span class="sxs-lookup"><span data-stu-id="749fd-169">**description**</span></span>          | <span data-ttu-id="749fd-170">string</span><span class="sxs-lookup"><span data-stu-id="749fd-170">string</span></span>           | <span data-ttu-id="749fd-171">Texto descriptivo del elemento.</span><span class="sxs-lookup"><span data-stu-id="749fd-171">The descriptive text for the site.</span></span>
| <span data-ttu-id="749fd-172">**lastModifiedBy**</span><span class="sxs-lookup"><span data-stu-id="749fd-172">**lastModifiedBy**</span></span>       | <span data-ttu-id="749fd-173">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="749fd-173">[identitySet][]</span></span>  | <span data-ttu-id="749fd-174">Identidad del usuario que modificó por última vez este elemento.</span><span class="sxs-lookup"><span data-stu-id="749fd-174">Identity of the last modifier of this item.</span></span> <span data-ttu-id="749fd-175">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="749fd-175">Read-only.</span></span>
| <span data-ttu-id="749fd-176">**lastModifiedDateTime**</span><span class="sxs-lookup"><span data-stu-id="749fd-176">**lastModifiedDateTime**</span></span> | <span data-ttu-id="749fd-177">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="749fd-177">DateTimeOffset</span></span>   | <span data-ttu-id="749fd-p108">Fecha y hora de la última modificación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="749fd-p108">The date and time the item was last modified. Read-only.</span></span>
| <span data-ttu-id="749fd-180">**webUrl**</span><span class="sxs-lookup"><span data-stu-id="749fd-180">**webUrl**</span></span>               | <span data-ttu-id="749fd-181">string (url)</span><span class="sxs-lookup"><span data-stu-id="749fd-181">string (url)</span></span>     | <span data-ttu-id="749fd-p109">Dirección URL que muestra el elemento en el explorador. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="749fd-p109">URL that displays the item in the browser. Read-only.</span></span>

## <a name="relationships"></a><span data-ttu-id="749fd-184">Relaciones</span><span class="sxs-lookup"><span data-stu-id="749fd-184">Relationships</span></span>

<span data-ttu-id="749fd-185">El recurso **list** tiene las siguientes relaciones con otros recursos.</span><span class="sxs-lookup"><span data-stu-id="749fd-185">The **list** resource has the following relationships to other resources.</span></span>

| <span data-ttu-id="749fd-186">Nombre de la relación</span><span class="sxs-lookup"><span data-stu-id="749fd-186">Relationship name</span></span> | <span data-ttu-id="749fd-187">Tipo</span><span class="sxs-lookup"><span data-stu-id="749fd-187">Type</span></span>                        | <span data-ttu-id="749fd-188">Descripción</span><span class="sxs-lookup"><span data-stu-id="749fd-188">Description</span></span>
|:------------------|:----------------------------|:------------------------------
| <span data-ttu-id="749fd-189">**drive**</span><span class="sxs-lookup"><span data-stu-id="749fd-189">**drive**</span></span>         | <span data-ttu-id="749fd-190">[drive][]</span><span class="sxs-lookup"><span data-stu-id="749fd-190">[drive][]</span></span>                   | <span data-ttu-id="749fd-191">Solo está presente en bibliotecas de documentos.</span><span class="sxs-lookup"><span data-stu-id="749fd-191">Only present on document libraries.</span></span> <span data-ttu-id="749fd-192">Permite el acceso a la lista como un recurso [drive][] con objetos [driveItems][driveItem].</span><span class="sxs-lookup"><span data-stu-id="749fd-192">Allows access to the list as a [drive][] resource with [driveItems][driveItem].</span></span>
| <span data-ttu-id="749fd-193">**items**</span><span class="sxs-lookup"><span data-stu-id="749fd-193">**items**</span></span>         | <span data-ttu-id="749fd-194">Collection([listItem][])</span><span class="sxs-lookup"><span data-stu-id="749fd-194">Collection([listItem][])</span></span>    | <span data-ttu-id="749fd-195">Todos los elementos que se incluyen en la lista.</span><span class="sxs-lookup"><span data-stu-id="749fd-195">All items contained in the drive.</span></span>

[baseItem]: baseItem.md
[contentType]: contentType.md
[drive]: drive.md
[driveItem]: driveItem.md
[columnDefinition]: columnDefinition.md
[identitySet]: identitySet.md
[listInfo]: listInfo.md
[listItem]: listItem.md
[site]: site.md
[systemFacet]: systemFacet.md

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/Lists",
  "tocBookmarks": {
    "Lists": "#"
  }
} -->
