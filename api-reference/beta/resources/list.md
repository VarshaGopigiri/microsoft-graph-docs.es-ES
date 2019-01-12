---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Lista
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 419f35226c09c1bde500994b6e023f764c54b3cc
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27953619"
---
# <a name="list-resource"></a><span data-ttu-id="4be99-102">Recurso List</span><span class="sxs-lookup"><span data-stu-id="4be99-102">List resource</span></span>

> <span data-ttu-id="4be99-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4be99-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4be99-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4be99-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4be99-105">El recurso **list** representa una lista en un [sitio][].</span><span class="sxs-lookup"><span data-stu-id="4be99-105">The **list** resource represents a list in a [site][].</span></span>
<span data-ttu-id="4be99-106">Este recurso contiene las propiedades de nivel superior de la lista, incluidas las definiciones de plantilla y campo.</span><span class="sxs-lookup"><span data-stu-id="4be99-106">This resource contains the top level properties of the list, including template and field definitions.</span></span>

## <a name="tasks-on-a-list"></a><span data-ttu-id="4be99-107">Tareas en una lista</span><span class="sxs-lookup"><span data-stu-id="4be99-107">Tasks on a list</span></span>

<span data-ttu-id="4be99-108">Las tareas siguientes están disponibles para los recursos list.</span><span class="sxs-lookup"><span data-stu-id="4be99-108">The following tasks are available for list resources.</span></span>
<span data-ttu-id="4be99-109">**Nota**: Esta versión beta solo permite navegar por listas, no permite crearlas ni actualizarlas.</span><span class="sxs-lookup"><span data-stu-id="4be99-109">**Note:** This beta only allows navigating lists, not creating or updating them.</span></span>
<span data-ttu-id="4be99-110">En cambio, puede crear o actualizar [elementos de lista][listItem].</span><span class="sxs-lookup"><span data-stu-id="4be99-110">You can, however, create or update [list items][listItem].</span></span>

<span data-ttu-id="4be99-111">Todos los ejemplos siguientes son relativos a un sitio, por ejemplo: `https://graph.microsoft.com/beta/sites/{site-id}`.</span><span class="sxs-lookup"><span data-stu-id="4be99-111">All examples below are relative to a site, eg: `https://graph.microsoft.com/beta/sites/{site-id}`.</span></span>

| <span data-ttu-id="4be99-112">Tarea común</span><span class="sxs-lookup"><span data-stu-id="4be99-112">Common task</span></span>               | <span data-ttu-id="4be99-113">Método HTTP</span><span class="sxs-lookup"><span data-stu-id="4be99-113">HTTP method</span></span>
|:--------------------------|:------------------------------
| <span data-ttu-id="4be99-114">[Obtener lista][]</span><span class="sxs-lookup"><span data-stu-id="4be99-114">[Get list][]</span></span>              | <span data-ttu-id="4be99-115">GET /lists/{list-id}</span><span class="sxs-lookup"><span data-stu-id="4be99-115">GET /lists/{list-id}</span></span>
| <span data-ttu-id="4be99-116">[Enumerar elementos de lista][]</span><span class="sxs-lookup"><span data-stu-id="4be99-116">[Enumerate list items][]</span></span>  | <span data-ttu-id="4be99-117">GET /lists/{list-id}/items</span><span class="sxs-lookup"><span data-stu-id="4be99-117">GET /lists/{list-id}/items</span></span>
| <span data-ttu-id="4be99-118">[Actualizar elemento de lista][]</span><span class="sxs-lookup"><span data-stu-id="4be99-118">[Update list item][]</span></span>      | <span data-ttu-id="4be99-119">PATCH /lists/{list-id}/items/{item-id}</span><span class="sxs-lookup"><span data-stu-id="4be99-119">PATCH /lists/{list-id}/items/{item-id}</span></span>
| <span data-ttu-id="4be99-120">[Eliminar elemento de lista][]</span><span class="sxs-lookup"><span data-stu-id="4be99-120">[Delete list item][]</span></span>      | <span data-ttu-id="4be99-121">DELETE /lists/{list-id}/items/{item-id}</span><span class="sxs-lookup"><span data-stu-id="4be99-121">DELETE /lists/{list-id}/items/{item-id}</span></span>
| <span data-ttu-id="4be99-122">[Crear elemento de lista][]</span><span class="sxs-lookup"><span data-stu-id="4be99-122">[Create list item][]</span></span>      | <span data-ttu-id="4be99-123">POST /lists/{list-id}</span><span class="sxs-lookup"><span data-stu-id="4be99-123">POST /lists/{list-id}</span></span>
| <span data-ttu-id="4be99-124">[Obtener actividades recientes][]</span><span class="sxs-lookup"><span data-stu-id="4be99-124">[Get recent activities][]</span></span> | <span data-ttu-id="4be99-125">GET /lists/{list-id}/activities</span><span class="sxs-lookup"><span data-stu-id="4be99-125">GET /lists/{list-id}/activities</span></span>

[Obtener lista]: ../api/list-get.md
[Get list]: ../api/list-get.md
[Enumerar elementos de lista]: ../api/listitem-list.md
[Enumerate list items]: ../api/listitem-list.md
[Actualizar elemento de lista]: ../api/listitem-update.md
[Update list item]: ../api/listitem-update.md
[Eliminar elemento de lista]: ../api/listitem-delete.md
[Delete list item]: ../api/listitem-delete.md
[Crear elemento de lista]: ../api/listitem-create.md
[Create list item]: ../api/listitem-create.md
[Obtener actividades recientes]: ../api/activities-list.md
[Get recent activities]: ../api/activities-list.md

## <a name="json-representation"></a><span data-ttu-id="4be99-132">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4be99-132">JSON representation</span></span>

<span data-ttu-id="4be99-133">A continuación se incluye una representación JSON del recurso **list**.</span><span class="sxs-lookup"><span data-stu-id="4be99-133">Here is a JSON representation of a **list** resource.</span></span>

<!-- { "blockType": "resource", 
       "@odata.type": "microsoft.graph.list",
       "keyProperty": "id", 
       "optionalProperties": [ "items", "drive"] } -->

```json
{
  "activities": [{"@odata.type": "microsoft.graph.itemActivity"}],
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

## <a name="properties"></a><span data-ttu-id="4be99-134">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4be99-134">Properties</span></span>

<span data-ttu-id="4be99-135">El recurso **list** tiene las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="4be99-135">The **list** resource has the following properties.</span></span>

| <span data-ttu-id="4be99-136">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="4be99-136">Property name</span></span>    | <span data-ttu-id="4be99-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="4be99-137">Type</span></span>                             | <span data-ttu-id="4be99-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="4be99-138">Description</span></span>
|:-----------------|:---------------------------------|:---------------------------
| <span data-ttu-id="4be99-139">**columns**</span><span class="sxs-lookup"><span data-stu-id="4be99-139">**columns**</span></span>      | <span data-ttu-id="4be99-140">Collection([columnDefinition][])</span><span class="sxs-lookup"><span data-stu-id="4be99-140">Collection([columnDefinition][])</span></span> | <span data-ttu-id="4be99-141">La colección de definiciones de campo de esta lista.</span><span class="sxs-lookup"><span data-stu-id="4be99-141">The collection of field definitions for this list.</span></span>
| <span data-ttu-id="4be99-142">**contentTypes**</span><span class="sxs-lookup"><span data-stu-id="4be99-142">**contentTypes**</span></span> | <span data-ttu-id="4be99-143">Collection([contentType][])</span><span class="sxs-lookup"><span data-stu-id="4be99-143">Collection([contentType][])</span></span>      | <span data-ttu-id="4be99-144">La colección de tipos de contenido presentes en esta lista.</span><span class="sxs-lookup"><span data-stu-id="4be99-144">The collection of content types present in this list.</span></span>
| <span data-ttu-id="4be99-145">**displayName**</span><span class="sxs-lookup"><span data-stu-id="4be99-145">**displayName**</span></span>  | <span data-ttu-id="4be99-146">string</span><span class="sxs-lookup"><span data-stu-id="4be99-146">string</span></span>                           | <span data-ttu-id="4be99-147">El título que se puede mostrar de la lista.</span><span class="sxs-lookup"><span data-stu-id="4be99-147">The displayable title of the list.</span></span>
| <span data-ttu-id="4be99-148">**list**</span><span class="sxs-lookup"><span data-stu-id="4be99-148">**list**</span></span>         | <span data-ttu-id="4be99-149">[listInfo][]</span><span class="sxs-lookup"><span data-stu-id="4be99-149">[listInfo][]</span></span>                     | <span data-ttu-id="4be99-150">Proporciona detalles adicionales sobre la lista.</span><span class="sxs-lookup"><span data-stu-id="4be99-150">Provides additional details about the list.</span></span>
| <span data-ttu-id="4be99-151">**system**</span><span class="sxs-lookup"><span data-stu-id="4be99-151">**system**</span></span>       | <span data-ttu-id="4be99-152">[systemFacet][]</span><span class="sxs-lookup"><span data-stu-id="4be99-152">[systemFacet][]</span></span>                  | <span data-ttu-id="4be99-153">Si está presente, indica que se trata de una lista administrada por el sistema.</span><span class="sxs-lookup"><span data-stu-id="4be99-153">If present, indicates that this is a system-managed list.</span></span> <span data-ttu-id="4be99-154">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4be99-154">Read-only.</span></span>

<span data-ttu-id="4be99-155">Las siguientes propiedades se heredan de **[baseItem][]**.</span><span class="sxs-lookup"><span data-stu-id="4be99-155">The following properties are inherited from **[baseItem][]**.</span></span>

| <span data-ttu-id="4be99-156">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="4be99-156">Property name</span></span>            | <span data-ttu-id="4be99-157">Tipo</span><span class="sxs-lookup"><span data-stu-id="4be99-157">Type</span></span>             | <span data-ttu-id="4be99-158">Descripción</span><span class="sxs-lookup"><span data-stu-id="4be99-158">Description</span></span>
|:-------------------------|:-----------------|:-------------------------------
| <span data-ttu-id="4be99-159">**id**</span><span class="sxs-lookup"><span data-stu-id="4be99-159">**id**</span></span>                   | <span data-ttu-id="4be99-160">string</span><span class="sxs-lookup"><span data-stu-id="4be99-160">string</span></span>           | <span data-ttu-id="4be99-p105">El identificador único del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4be99-p105">The unique identifier of the item. Read-only.</span></span>
| <span data-ttu-id="4be99-163">**name**</span><span class="sxs-lookup"><span data-stu-id="4be99-163">**name**</span></span>                 | <span data-ttu-id="4be99-164">string</span><span class="sxs-lookup"><span data-stu-id="4be99-164">string</span></span>           | <span data-ttu-id="4be99-165">Nombre del elemento.</span><span class="sxs-lookup"><span data-stu-id="4be99-165">The name of the item.</span></span>
| <span data-ttu-id="4be99-166">**createdBy**</span><span class="sxs-lookup"><span data-stu-id="4be99-166">**createdBy**</span></span>            | <span data-ttu-id="4be99-167">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="4be99-167">[identitySet][]</span></span>  | <span data-ttu-id="4be99-168">Identidad del creador de este elemento.</span><span class="sxs-lookup"><span data-stu-id="4be99-168">Identity of the creator of this item.</span></span> <span data-ttu-id="4be99-169">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4be99-169">Read-only.</span></span>
| <span data-ttu-id="4be99-170">**createdDateTime**</span><span class="sxs-lookup"><span data-stu-id="4be99-170">**createdDateTime**</span></span>      | <span data-ttu-id="4be99-171">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4be99-171">DateTimeOffset</span></span>   | <span data-ttu-id="4be99-p107">La fecha y la hora de creación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4be99-p107">The date and time the item was created. Read-only.</span></span>
| <span data-ttu-id="4be99-174">**description**</span><span class="sxs-lookup"><span data-stu-id="4be99-174">**description**</span></span>          | <span data-ttu-id="4be99-175">string</span><span class="sxs-lookup"><span data-stu-id="4be99-175">string</span></span>           | <span data-ttu-id="4be99-176">Texto descriptivo del elemento.</span><span class="sxs-lookup"><span data-stu-id="4be99-176">The descriptive text for the item.</span></span>
| <span data-ttu-id="4be99-177">**lastModifiedBy**</span><span class="sxs-lookup"><span data-stu-id="4be99-177">**lastModifiedBy**</span></span>       | <span data-ttu-id="4be99-178">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="4be99-178">[identitySet][]</span></span>  | <span data-ttu-id="4be99-179">Identidad del usuario que modificó por última vez este elemento.</span><span class="sxs-lookup"><span data-stu-id="4be99-179">Identity of the last modifier of this item.</span></span> <span data-ttu-id="4be99-180">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4be99-180">Read-only.</span></span>
| <span data-ttu-id="4be99-181">**lastModifiedDateTime**</span><span class="sxs-lookup"><span data-stu-id="4be99-181">**lastModifiedDateTime**</span></span> | <span data-ttu-id="4be99-182">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4be99-182">DateTimeOffset</span></span>   | <span data-ttu-id="4be99-p109">Fecha y hora de la última modificación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4be99-p109">The date and time the item was last modified. Read-only.</span></span>
| <span data-ttu-id="4be99-185">**webUrl**</span><span class="sxs-lookup"><span data-stu-id="4be99-185">**webUrl**</span></span>               | <span data-ttu-id="4be99-186">string (url)</span><span class="sxs-lookup"><span data-stu-id="4be99-186">string (url)</span></span>     | <span data-ttu-id="4be99-p110">Dirección URL que muestra el elemento en el explorador. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4be99-p110">URL that displays the item in the browser. Read-only.</span></span>

## <a name="relationships"></a><span data-ttu-id="4be99-189">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4be99-189">Relationships</span></span>

<span data-ttu-id="4be99-190">El recurso **list** tiene las siguientes relaciones con otros recursos.</span><span class="sxs-lookup"><span data-stu-id="4be99-190">The **list** resource has the following relationships to other resources.</span></span>

| <span data-ttu-id="4be99-191">Nombre de la relación</span><span class="sxs-lookup"><span data-stu-id="4be99-191">Relationship name</span></span> | <span data-ttu-id="4be99-192">Tipo</span><span class="sxs-lookup"><span data-stu-id="4be99-192">Type</span></span>                        | <span data-ttu-id="4be99-193">Descripción</span><span class="sxs-lookup"><span data-stu-id="4be99-193">Description</span></span>
|:------------------|:----------------------------|:------------------------------
| <span data-ttu-id="4be99-194">**activities**</span><span class="sxs-lookup"><span data-stu-id="4be99-194">**activities**</span></span>    | <span data-ttu-id="4be99-195">Colección [itemActivity][]</span><span class="sxs-lookup"><span data-stu-id="4be99-195">[itemActivity][] collection</span></span> | <span data-ttu-id="4be99-196">Las actividades recientes que tuvieron lugar en esta lista.</span><span class="sxs-lookup"><span data-stu-id="4be99-196">The recent activities that took place within this list.</span></span>
| <span data-ttu-id="4be99-197">**drive**</span><span class="sxs-lookup"><span data-stu-id="4be99-197">**drive**</span></span>         | <span data-ttu-id="4be99-198">[drive][]</span><span class="sxs-lookup"><span data-stu-id="4be99-198">[drive][]</span></span>                   | <span data-ttu-id="4be99-199">Solo está presente en bibliotecas de documentos.</span><span class="sxs-lookup"><span data-stu-id="4be99-199">Only present on document libraries.</span></span> <span data-ttu-id="4be99-200">Permite el acceso a la lista como un recurso [drive][] con objetos [driveItems][driveItem].</span><span class="sxs-lookup"><span data-stu-id="4be99-200">Allows access to the list as a [drive][] resource with [driveItems][driveItem].</span></span>
| <span data-ttu-id="4be99-201">**items**</span><span class="sxs-lookup"><span data-stu-id="4be99-201">**items**</span></span>         | <span data-ttu-id="4be99-202">Collection([listItem][])</span><span class="sxs-lookup"><span data-stu-id="4be99-202">Collection([listItem][])</span></span>    | <span data-ttu-id="4be99-203">Todos los elementos que se incluyen en la lista.</span><span class="sxs-lookup"><span data-stu-id="4be99-203">All items contained in the list.</span></span>

[baseItem]: baseitem.md
[contentType]: contenttype.md
[drive]: drive.md
[driveItem]: driveitem.md
[columnDefinition]: columndefinition.md
[identitySet]: identityset.md
[itemActivity]: itemactivity.md
[listInfo]: listinfo.md
[listItem]: listitem.md
[site]: site.md
[systemFacet]: systemfacet.md

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
