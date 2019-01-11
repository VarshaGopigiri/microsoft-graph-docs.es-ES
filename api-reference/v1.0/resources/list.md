---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: Lista
localization_priority: Priority
ms.openlocfilehash: 121b65dcf67e847f507c24385f89324224b41a85
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27827296"
---
# <a name="list-resource"></a><span data-ttu-id="715d5-102">Recurso List</span><span class="sxs-lookup"><span data-stu-id="715d5-102">List resource</span></span>

<span data-ttu-id="715d5-103">El recurso **list** representa una lista en un [sitio][].</span><span class="sxs-lookup"><span data-stu-id="715d5-103">The **list** resource represents a list in a [site][].</span></span>
<span data-ttu-id="715d5-104">Este recurso contiene las propiedades de nivel superior de la lista, incluidas las definiciones de plantilla y campo.</span><span class="sxs-lookup"><span data-stu-id="715d5-104">This resource contains the top level properties of the list, including template and field definitions.</span></span>

## <a name="tasks-on-a-list"></a><span data-ttu-id="715d5-105">Tareas en una lista</span><span class="sxs-lookup"><span data-stu-id="715d5-105">Tasks on a list</span></span>

<span data-ttu-id="715d5-106">Las tareas siguientes están disponibles para los recursos list.</span><span class="sxs-lookup"><span data-stu-id="715d5-106">The following tasks are available for list resources.</span></span>
<span data-ttu-id="715d5-107">**Nota**: Esta versión beta solo permite navegar por listas, no permite crearlas ni actualizarlas.</span><span class="sxs-lookup"><span data-stu-id="715d5-107">**Note:** This beta only allows navigating lists, not creating or updating them.</span></span>
<span data-ttu-id="715d5-108">En cambio, puede crear o actualizar [elementos de lista][listItem].</span><span class="sxs-lookup"><span data-stu-id="715d5-108">You can, however, create or update [list items][listItem].</span></span>

<span data-ttu-id="715d5-109">Todos los ejemplos siguientes son relativos a un sitio, por ejemplo: `https://graph.microsoft.com/v1.0/sites/{site-id}`.</span><span class="sxs-lookup"><span data-stu-id="715d5-109">All examples below are relative to a site, eg: `https://graph.microsoft.com/v1.0/sites/{site-id}`.</span></span>

| <span data-ttu-id="715d5-110">Tarea común</span><span class="sxs-lookup"><span data-stu-id="715d5-110">Common task</span></span>               | <span data-ttu-id="715d5-111">Método HTTP</span><span class="sxs-lookup"><span data-stu-id="715d5-111">HTTP method</span></span>
|:--------------------------|:------------------------------
| <span data-ttu-id="715d5-112">[Obtener lista][]</span><span class="sxs-lookup"><span data-stu-id="715d5-112">[Get list][]</span></span>              | <span data-ttu-id="715d5-113">GET /lists/{list-id}</span><span class="sxs-lookup"><span data-stu-id="715d5-113">GET /lists/{list-id}</span></span>
| <span data-ttu-id="715d5-114">[Enumerar elementos de lista][]</span><span class="sxs-lookup"><span data-stu-id="715d5-114">[Enumerate list items][]</span></span>  | <span data-ttu-id="715d5-115">GET /lists/{list-id}/items</span><span class="sxs-lookup"><span data-stu-id="715d5-115">GET /lists/{list-id}/items</span></span>
| <span data-ttu-id="715d5-116">[Actualizar elemento de lista][]</span><span class="sxs-lookup"><span data-stu-id="715d5-116">[Update list item][]</span></span>      | <span data-ttu-id="715d5-117">PATCH /lists/{list-id}/items/{item-id}</span><span class="sxs-lookup"><span data-stu-id="715d5-117">PATCH /lists/{list-id}/items/{item-id}</span></span>
| <span data-ttu-id="715d5-118">[Eliminar elemento de lista][]</span><span class="sxs-lookup"><span data-stu-id="715d5-118">[Delete list item][]</span></span>      | <span data-ttu-id="715d5-119">DELETE /lists/{list-id}/items/{item-id}</span><span class="sxs-lookup"><span data-stu-id="715d5-119">DELETE /lists/{list-id}/items/{item-id}</span></span>
| <span data-ttu-id="715d5-120">[Crear elemento de lista][]</span><span class="sxs-lookup"><span data-stu-id="715d5-120">[Create list item][]</span></span>      | <span data-ttu-id="715d5-121">POST /lists/{list-id}</span><span class="sxs-lookup"><span data-stu-id="715d5-121">POST /lists/{list-id}</span></span>

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

## <a name="json-representation"></a><span data-ttu-id="715d5-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="715d5-127">JSON representation</span></span>

<span data-ttu-id="715d5-128">A continuación se incluye una representación JSON del recurso **list**.</span><span class="sxs-lookup"><span data-stu-id="715d5-128">Here is a JSON representation of a **list** resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [
    "items",
    "drive"
  ],
  "keyProperty": "id",
  "baseType": "microsoft.graph.baseItem",
  "@odata.type": "microsoft.graph.list"
}-->

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
    "template": "documentLibrary | genericList | survey | links | announcements | contacts | accessRequest ..."
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
  "parentReference": { "@odata.type": "microsoft.graph.itemReference" },
  "sharepointIds": { "@odata.type": "microsoft.graph.sharepointIds" },
  "webUrl": "url to visit the list in a browser"
}
```

## <a name="properties"></a><span data-ttu-id="715d5-129">Propiedades</span><span class="sxs-lookup"><span data-stu-id="715d5-129">Properties</span></span>

<span data-ttu-id="715d5-130">El recurso **list** tiene las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="715d5-130">The **list** resource has the following properties.</span></span>

| <span data-ttu-id="715d5-131">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="715d5-131">Property name</span></span>    | <span data-ttu-id="715d5-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="715d5-132">Type</span></span>                             | <span data-ttu-id="715d5-133">Description</span><span class="sxs-lookup"><span data-stu-id="715d5-133">Description</span></span>
|:-----------------|:---------------------------------|:---------------------------
| <span data-ttu-id="715d5-134">**displayName**</span><span class="sxs-lookup"><span data-stu-id="715d5-134">**displayName**</span></span>  | <span data-ttu-id="715d5-135">string</span><span class="sxs-lookup"><span data-stu-id="715d5-135">string</span></span>                           | <span data-ttu-id="715d5-136">El título que se puede mostrar de la lista.</span><span class="sxs-lookup"><span data-stu-id="715d5-136">The displayable title of the list.</span></span>
| <span data-ttu-id="715d5-137">**list**</span><span class="sxs-lookup"><span data-stu-id="715d5-137">**list**</span></span>         | <span data-ttu-id="715d5-138">[listInfo][]</span><span class="sxs-lookup"><span data-stu-id="715d5-138">[listInfo][]</span></span>                     | <span data-ttu-id="715d5-139">Proporciona detalles adicionales sobre la lista.</span><span class="sxs-lookup"><span data-stu-id="715d5-139">Provides additional details about the list.</span></span>
| <span data-ttu-id="715d5-140">**system**</span><span class="sxs-lookup"><span data-stu-id="715d5-140">**system**</span></span>       | <span data-ttu-id="715d5-141">[systemFacet][]</span><span class="sxs-lookup"><span data-stu-id="715d5-141">[systemFacet][]</span></span>                  | <span data-ttu-id="715d5-142">Si está presente, indica que se trata de una lista administrada por el sistema.</span><span class="sxs-lookup"><span data-stu-id="715d5-142">If present, indicates that this is a system-managed list.</span></span> <span data-ttu-id="715d5-143">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="715d5-143">Read-only.</span></span>

<span data-ttu-id="715d5-144">Las siguientes propiedades se heredan de **[baseItem][]**.</span><span class="sxs-lookup"><span data-stu-id="715d5-144">The following properties are inherited from **[baseItem][]**.</span></span>

| <span data-ttu-id="715d5-145">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="715d5-145">Property name</span></span>            | <span data-ttu-id="715d5-146">Tipo</span><span class="sxs-lookup"><span data-stu-id="715d5-146">Type</span></span>              | <span data-ttu-id="715d5-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="715d5-147">Description</span></span>
|:-------------------------|:------------------|:------------------------------
| <span data-ttu-id="715d5-148">**id**</span><span class="sxs-lookup"><span data-stu-id="715d5-148">**id**</span></span>                   | <span data-ttu-id="715d5-149">string</span><span class="sxs-lookup"><span data-stu-id="715d5-149">string</span></span>            | <span data-ttu-id="715d5-p104">El identificador único del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="715d5-p104">The unique identifier of the item. Read-only.</span></span>
| <span data-ttu-id="715d5-152">**name**</span><span class="sxs-lookup"><span data-stu-id="715d5-152">**name**</span></span>                 | <span data-ttu-id="715d5-153">string</span><span class="sxs-lookup"><span data-stu-id="715d5-153">string</span></span>            | <span data-ttu-id="715d5-154">Nombre del elemento.</span><span class="sxs-lookup"><span data-stu-id="715d5-154">The name of the item.</span></span>
| <span data-ttu-id="715d5-155">**createdBy**</span><span class="sxs-lookup"><span data-stu-id="715d5-155">**createdBy**</span></span>            | <span data-ttu-id="715d5-156">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="715d5-156">[identitySet][]</span></span>   | <span data-ttu-id="715d5-157">Identidad del creador de este elemento.</span><span class="sxs-lookup"><span data-stu-id="715d5-157">Identity of the creator of this item.</span></span> <span data-ttu-id="715d5-158">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="715d5-158">Read-only.</span></span>
| <span data-ttu-id="715d5-159">**createdDateTime**</span><span class="sxs-lookup"><span data-stu-id="715d5-159">**createdDateTime**</span></span>      | <span data-ttu-id="715d5-160">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="715d5-160">DateTimeOffset</span></span>    | <span data-ttu-id="715d5-p106">La fecha y la hora de creación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="715d5-p106">The date and time the item was created. Read-only.</span></span>
| <span data-ttu-id="715d5-163">**description**</span><span class="sxs-lookup"><span data-stu-id="715d5-163">**description**</span></span>          | <span data-ttu-id="715d5-164">string</span><span class="sxs-lookup"><span data-stu-id="715d5-164">string</span></span>            | <span data-ttu-id="715d5-165">Texto descriptivo del elemento.</span><span class="sxs-lookup"><span data-stu-id="715d5-165">The descriptive text for the item.</span></span>
| <span data-ttu-id="715d5-166">**eTag**</span><span class="sxs-lookup"><span data-stu-id="715d5-166">**eTag**</span></span>                 | <span data-ttu-id="715d5-167">string</span><span class="sxs-lookup"><span data-stu-id="715d5-167">string</span></span>            | <span data-ttu-id="715d5-p107">ETag para el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="715d5-p107">ETag for the item. Read-only.</span></span>                                                          |
| <span data-ttu-id="715d5-170">**lastModifiedBy**</span><span class="sxs-lookup"><span data-stu-id="715d5-170">**lastModifiedBy**</span></span>       | <span data-ttu-id="715d5-171">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="715d5-171">[identitySet][]</span></span>   | <span data-ttu-id="715d5-172">Identidad del usuario que modificó por última vez este elemento.</span><span class="sxs-lookup"><span data-stu-id="715d5-172">Identity of the last modifier of this item.</span></span> <span data-ttu-id="715d5-173">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="715d5-173">Read-only.</span></span>
| <span data-ttu-id="715d5-174">**lastModifiedDateTime**</span><span class="sxs-lookup"><span data-stu-id="715d5-174">**lastModifiedDateTime**</span></span> | <span data-ttu-id="715d5-175">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="715d5-175">DateTimeOffset</span></span>    | <span data-ttu-id="715d5-p109">Fecha y hora de la última modificación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="715d5-p109">The date and time the item was last modified. Read-only.</span></span>
| <span data-ttu-id="715d5-178">**parentReference**</span><span class="sxs-lookup"><span data-stu-id="715d5-178">**parentReference**</span></span>      | <span data-ttu-id="715d5-179">[itemReference][]</span><span class="sxs-lookup"><span data-stu-id="715d5-179">[itemReference][]</span></span> | <span data-ttu-id="715d5-p110">Información primaria, si el elemento tiene un elemento primario. Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="715d5-p110">Parent information, if the item has a parent. Read-write.</span></span>
| <span data-ttu-id="715d5-182">**sharepointIds**</span><span class="sxs-lookup"><span data-stu-id="715d5-182">**sharepointIds**</span></span>        | <span data-ttu-id="715d5-183">[sharepointIds][]</span><span class="sxs-lookup"><span data-stu-id="715d5-183">[sharepointIds][]</span></span> | <span data-ttu-id="715d5-p111">Devuelve los identificadores útiles para la compatibilidad con REST de SharePoint. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="715d5-p111">Returns identifiers useful for SharePoint REST compatibility. Read-only.</span></span>
| <span data-ttu-id="715d5-186">**webUrl**</span><span class="sxs-lookup"><span data-stu-id="715d5-186">**webUrl**</span></span>               | <span data-ttu-id="715d5-187">string (url)</span><span class="sxs-lookup"><span data-stu-id="715d5-187">string (url)</span></span>      | <span data-ttu-id="715d5-p112">Dirección URL que muestra el elemento en el explorador. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="715d5-p112">URL that displays the item in the browser. Read-only.</span></span>

## <a name="relationships"></a><span data-ttu-id="715d5-190">Relaciones</span><span class="sxs-lookup"><span data-stu-id="715d5-190">Relationships</span></span>

<span data-ttu-id="715d5-191">El recurso **list** tiene las siguientes relaciones con otros recursos.</span><span class="sxs-lookup"><span data-stu-id="715d5-191">The **list** resource has the following relationships to other resources.</span></span>

| <span data-ttu-id="715d5-192">Nombre de la relación</span><span class="sxs-lookup"><span data-stu-id="715d5-192">Relationship name</span></span> | <span data-ttu-id="715d5-193">Tipo</span><span class="sxs-lookup"><span data-stu-id="715d5-193">Type</span></span>                             | <span data-ttu-id="715d5-194">Descripción</span><span class="sxs-lookup"><span data-stu-id="715d5-194">Description</span></span>
|:------------------|:---------------------------------|:----------------------
| <span data-ttu-id="715d5-195">**drive**</span><span class="sxs-lookup"><span data-stu-id="715d5-195">**drive**</span></span>         | <span data-ttu-id="715d5-196">[drive][]</span><span class="sxs-lookup"><span data-stu-id="715d5-196">[drive][]</span></span>                        | <span data-ttu-id="715d5-197">Solo está presente en bibliotecas de documentos.</span><span class="sxs-lookup"><span data-stu-id="715d5-197">Only present on document libraries.</span></span> <span data-ttu-id="715d5-198">Permite el acceso a la lista como un recurso [drive][] con objetos [driveItems][driveItem].</span><span class="sxs-lookup"><span data-stu-id="715d5-198">Allows access to the list as a [drive][] resource with [driveItems][driveItem].</span></span>
| <span data-ttu-id="715d5-199">**items**</span><span class="sxs-lookup"><span data-stu-id="715d5-199">**items**</span></span>         | <span data-ttu-id="715d5-200">Collection([listItem][])</span><span class="sxs-lookup"><span data-stu-id="715d5-200">Collection([listItem][])</span></span>         | <span data-ttu-id="715d5-201">Todos los elementos que se incluyen en la lista.</span><span class="sxs-lookup"><span data-stu-id="715d5-201">All items contained in the list.</span></span>
| <span data-ttu-id="715d5-202">**columns**</span><span class="sxs-lookup"><span data-stu-id="715d5-202">**columns**</span></span>       | <span data-ttu-id="715d5-203">Collection([columnDefinition][])</span><span class="sxs-lookup"><span data-stu-id="715d5-203">Collection([columnDefinition][])</span></span> | <span data-ttu-id="715d5-204">La colección de definiciones de campo de esta lista.</span><span class="sxs-lookup"><span data-stu-id="715d5-204">The collection of field definitions for this list.</span></span>
| <span data-ttu-id="715d5-205">**contentTypes**</span><span class="sxs-lookup"><span data-stu-id="715d5-205">**contentTypes**</span></span>  | <span data-ttu-id="715d5-206">Collection([contentType][])</span><span class="sxs-lookup"><span data-stu-id="715d5-206">Collection([contentType][])</span></span>      | <span data-ttu-id="715d5-207">La colección de tipos de contenido presentes en esta lista.</span><span class="sxs-lookup"><span data-stu-id="715d5-207">The collection of content types present in this list.</span></span>

[baseItem]: baseitem.md
[contentType]: contenttype.md
[drive]: drive.md
[driveItem]: driveitem.md
[columnDefinition]: columndefinition.md
[identitySet]: identityset.md
[itemReference]: itemreference.md
[listInfo]: listinfo.md
[listItem]: listitem.md
[sharepointIds]: sharepointids.md
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
