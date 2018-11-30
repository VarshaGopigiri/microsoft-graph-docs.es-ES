---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: ListItem
ms.openlocfilehash: 18ba74fd677c83da5f8bfe5d13303f7b18ed43f2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084851"
---
# <a name="listitem-resource"></a><span data-ttu-id="17808-102">Recurso ListItem</span><span class="sxs-lookup"><span data-stu-id="17808-102">ListItem resource</span></span>

> <span data-ttu-id="17808-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="17808-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="17808-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="17808-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="17808-105">Este recurso representa un elemento en una **[lista][]** de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="17808-105">This resource represents an item in a SharePoint **[list][]**.</span></span>
<span data-ttu-id="17808-106">Los valores de columna de la lista están disponibles a través del diccionario `fieldValueSet`.</span><span class="sxs-lookup"><span data-stu-id="17808-106">Column values in the list are available through the `fieldValueSet` dictionary.</span></span>

## <a name="tasks-on-a-listitem"></a><span data-ttu-id="17808-107">Tareas en un recurso listItem</span><span class="sxs-lookup"><span data-stu-id="17808-107">Tasks on a listItem</span></span>

<span data-ttu-id="17808-108">Las tareas siguientes están disponibles para los recursos **listItem**.</span><span class="sxs-lookup"><span data-stu-id="17808-108">The following tasks are available for **listItem** resources.</span></span>
<span data-ttu-id="17808-109">Todos los ejemplos siguientes son relativos a una **[lista][]**, por ejemplo: `https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}`.</span><span class="sxs-lookup"><span data-stu-id="17808-109">All examples below are relative to a **[list][]**, eg: `https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}`.</span></span>

| <span data-ttu-id="17808-110">Tarea común</span><span class="sxs-lookup"><span data-stu-id="17808-110">Common task</span></span>                    | <span data-ttu-id="17808-111">Método HTTP</span><span class="sxs-lookup"><span data-stu-id="17808-111">HTTP method</span></span>
|:-------------------------------|:------------------------
| <span data-ttu-id="17808-112">[Obtener][]</span><span class="sxs-lookup"><span data-stu-id="17808-112">[Get][]</span></span>                        | <span data-ttu-id="17808-113">GET /items/{item-id}</span><span class="sxs-lookup"><span data-stu-id="17808-113">GET /items/{item-id}</span></span>
| <span data-ttu-id="17808-114">[Obtener valores de columna][Obtener]</span><span class="sxs-lookup"><span data-stu-id="17808-114">[Get column values][Get]</span></span>       | <span data-ttu-id="17808-115">GET /items/{item-id}?expand=fields</span><span class="sxs-lookup"><span data-stu-id="17808-115">GET /items/{item-id}?expand=fields</span></span>
| <span data-ttu-id="17808-116">[Obtener análisis][]</span><span class="sxs-lookup"><span data-stu-id="17808-116">[Get analytics][]</span></span>              | <span data-ttu-id="17808-117">GET /items/ {identificador de elemento} / análisis</span><span class="sxs-lookup"><span data-stu-id="17808-117">GET /items/{item-id}/analytics</span></span>
| <span data-ttu-id="17808-118">[Obtener las actividades por intervalo][]</span><span class="sxs-lookup"><span data-stu-id="17808-118">[Get activities by interval][]</span></span> | <span data-ttu-id="17808-119">GET /items/ {identificador de elemento} / getActivitiesByInterval</span><span class="sxs-lookup"><span data-stu-id="17808-119">GET /items/{item-id}/getActivitiesByInterval</span></span>
| <span data-ttu-id="17808-120">[Crear][]</span><span class="sxs-lookup"><span data-stu-id="17808-120">[Create][]</span></span>                     | <span data-ttu-id="17808-121">POST /items</span><span class="sxs-lookup"><span data-stu-id="17808-121">POST /items</span></span>
| <span data-ttu-id="17808-122">[Eliminar][]</span><span class="sxs-lookup"><span data-stu-id="17808-122">[Delete][]</span></span>                     | <span data-ttu-id="17808-123">DELETE /items/{item-id}</span><span class="sxs-lookup"><span data-stu-id="17808-123">DELETE /items/{item-id}</span></span>
| <span data-ttu-id="17808-124">[Actualizar][]</span><span class="sxs-lookup"><span data-stu-id="17808-124">[Update][]</span></span>                     | <span data-ttu-id="17808-125">PATCH /items/{item-id}</span><span class="sxs-lookup"><span data-stu-id="17808-125">PATCH /items/{item-id}</span></span>
| <span data-ttu-id="17808-126">[Actualizar valores de columna][Actualizar]</span><span class="sxs-lookup"><span data-stu-id="17808-126">[Update column values][Update]</span></span> | <span data-ttu-id="17808-127">PATCH /items/{item-id}/fields</span><span class="sxs-lookup"><span data-stu-id="17808-127">PATCH /items/{item-id}/fields</span></span>

[Obtener]: ../api/listitem-get.md
[Get]: ../api/listitem-get.md
[Obtener análisis]: ../api/itemanalytics-get.md
[Get analytics]: ../api/itemanalytics-get.md
[Obtener las actividades por intervalo]: ../api/itemactivity-getbyinterval.md
[Get activities by interval]: ../api/itemactivity-getbyinterval.md
[Create]: ../api/listitem-create.md
[Delete]: ../api/listitem-delete.md
[Actualizar]: ../api/listitem-update.md
[Update]: ../api/listitem-update.md

## <a name="json-representation"></a><span data-ttu-id="17808-134">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="17808-134">JSON representation</span></span>

<span data-ttu-id="17808-135">A continuación se incluye una representación JSON del recurso **listItem**.</span><span class="sxs-lookup"><span data-stu-id="17808-135">Here is a JSON representation of a **listItem** resource.</span></span>

<!--{
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.baseItem",
  "@odata.type": "microsoft.graph.listItem"
}-->

```json
{
  "contentType": { "@odata.type": "microsoft.graph.contentTypeInfo" },
  "fields": { "@odata.type": "microsoft.graph.fieldValueSet" },
  "sharepointIds": { "@odata.type": "microsoft.graph.sharepointIds" },

  /* relationships */
  "activities": [{"@odata.type": "microsoft.graph.itemActivity"}],
  "analytics": { "@odata.type": "microsoft.graph.itemAnalytics" },
  "driveItem": { "@odata.type": "microsoft.graph.driveItem" },
  "versions": [{"@odata.type": "microsoft.graph.listItemVersion"}],

  /* inherited from baseItem */
  "id": "string",
  "name": "name of resource",
  "createdBy": { "@odata.type": "microsoft.graph.identitySet" },
  "createdDateTime": "timestamp",
  "description": "description of resource",
  "eTag": "string",
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "timestamp",
  "parentReference": { "@odata.type": "microsoft.graph.itemReference"},
  "webUrl": "url"
}
```

## <a name="properties"></a><span data-ttu-id="17808-136">Propiedades</span><span class="sxs-lookup"><span data-stu-id="17808-136">Properties</span></span>

<span data-ttu-id="17808-137">El recurso **listItem** tiene las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="17808-137">The **listItem** resource has the following properties.</span></span>

| <span data-ttu-id="17808-138">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="17808-138">Property name</span></span> | <span data-ttu-id="17808-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="17808-139">Type</span></span>                | <span data-ttu-id="17808-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="17808-140">Description</span></span>
|:--------------|:--------------------|:-------------------------------
| <span data-ttu-id="17808-141">contentType</span><span class="sxs-lookup"><span data-stu-id="17808-141">contentType</span></span>   | <span data-ttu-id="17808-142">[contentTypeInfo][]</span><span class="sxs-lookup"><span data-stu-id="17808-142">[contentTypeInfo][]</span></span> | <span data-ttu-id="17808-143">El tipo de contenido de este elemento de lista</span><span class="sxs-lookup"><span data-stu-id="17808-143">The content type of this list item</span></span>

<span data-ttu-id="17808-144">Las siguientes propiedades se heredan de **[baseItem][]**.</span><span class="sxs-lookup"><span data-stu-id="17808-144">The following properties are inherited from **[baseItem][]**.</span></span>

| <span data-ttu-id="17808-145">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="17808-145">Property name</span></span>        | <span data-ttu-id="17808-146">Tipo</span><span class="sxs-lookup"><span data-stu-id="17808-146">Type</span></span>              | <span data-ttu-id="17808-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="17808-147">Description</span></span>
|:---------------------|:------------------|:----------------------------------
| <span data-ttu-id="17808-148">id</span><span class="sxs-lookup"><span data-stu-id="17808-148">id</span></span>                   | <span data-ttu-id="17808-149">string</span><span class="sxs-lookup"><span data-stu-id="17808-149">string</span></span>            | <span data-ttu-id="17808-p104">El identificador único del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="17808-p104">The unique identifier of the item. Read-only.</span></span>
| <span data-ttu-id="17808-152">name</span><span class="sxs-lookup"><span data-stu-id="17808-152">name</span></span>                 | <span data-ttu-id="17808-153">string</span><span class="sxs-lookup"><span data-stu-id="17808-153">string</span></span>            | <span data-ttu-id="17808-154">Nombre o título del elemento.</span><span class="sxs-lookup"><span data-stu-id="17808-154">The name / title of the item.</span></span>
| <span data-ttu-id="17808-155">createdBy</span><span class="sxs-lookup"><span data-stu-id="17808-155">createdBy</span></span>            | <span data-ttu-id="17808-156">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="17808-156">[identitySet][]</span></span>   | <span data-ttu-id="17808-157">Identidad del creador de este elemento.</span><span class="sxs-lookup"><span data-stu-id="17808-157">Identity of the creator of this item.</span></span> <span data-ttu-id="17808-158">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="17808-158">Read-only.</span></span>
| <span data-ttu-id="17808-159">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="17808-159">createdDateTime</span></span>      | <span data-ttu-id="17808-160">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="17808-160">DateTimeOffset</span></span>    | <span data-ttu-id="17808-p106">La fecha y la hora de creación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="17808-p106">The date and time the item was created. Read-only.</span></span>
| <span data-ttu-id="17808-163">descripción</span><span class="sxs-lookup"><span data-stu-id="17808-163">description</span></span>          | <span data-ttu-id="17808-164">string</span><span class="sxs-lookup"><span data-stu-id="17808-164">string</span></span>            | <span data-ttu-id="17808-165">Texto descriptivo del elemento.</span><span class="sxs-lookup"><span data-stu-id="17808-165">The descriptive text for the item.</span></span>
| <span data-ttu-id="17808-166">eTag</span><span class="sxs-lookup"><span data-stu-id="17808-166">eTag</span></span>                 | <span data-ttu-id="17808-167">string</span><span class="sxs-lookup"><span data-stu-id="17808-167">string</span></span>            | <span data-ttu-id="17808-p107">ETag para el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="17808-p107">ETag for the item. Read-only.</span></span>                                                          |
| <span data-ttu-id="17808-170">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="17808-170">lastModifiedBy</span></span>       | <span data-ttu-id="17808-171">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="17808-171">[identitySet][]</span></span>   | <span data-ttu-id="17808-172">Identidad del usuario que modificó por última vez este elemento.</span><span class="sxs-lookup"><span data-stu-id="17808-172">Identity of the last modifier of this item.</span></span> <span data-ttu-id="17808-173">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="17808-173">Read-only.</span></span>
| <span data-ttu-id="17808-174">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="17808-174">lastModifiedDateTime</span></span> | <span data-ttu-id="17808-175">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="17808-175">DateTimeOffset</span></span>    | <span data-ttu-id="17808-p109">Fecha y hora de la última modificación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="17808-p109">The date and time the item was last modified. Read-only.</span></span>
| <span data-ttu-id="17808-178">parentReference</span><span class="sxs-lookup"><span data-stu-id="17808-178">parentReference</span></span>      | <span data-ttu-id="17808-179">[itemReference][]</span><span class="sxs-lookup"><span data-stu-id="17808-179">[itemReference][]</span></span> | <span data-ttu-id="17808-p110">Información primaria, si el elemento tiene un elemento primario. Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="17808-p110">Parent information, if the item has a parent. Read-write.</span></span>
| <span data-ttu-id="17808-182">sharepointIds</span><span class="sxs-lookup"><span data-stu-id="17808-182">sharepointIds</span></span>        | <span data-ttu-id="17808-183">[sharepointIds][]</span><span class="sxs-lookup"><span data-stu-id="17808-183">[sharepointIds][]</span></span> | <span data-ttu-id="17808-p111">Devuelve los identificadores útiles para la compatibilidad con REST de SharePoint. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="17808-p111">Returns identifiers useful for SharePoint REST compatibility. Read-only.</span></span>
| <span data-ttu-id="17808-186">webUrl</span><span class="sxs-lookup"><span data-stu-id="17808-186">webUrl</span></span>               | <span data-ttu-id="17808-187">string (url)</span><span class="sxs-lookup"><span data-stu-id="17808-187">string (url)</span></span>      | <span data-ttu-id="17808-p112">Dirección URL que muestra el elemento en el explorador. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="17808-p112">URL that displays the item in the browser. Read-only.</span></span>

## <a name="relationships"></a><span data-ttu-id="17808-190">Relaciones</span><span class="sxs-lookup"><span data-stu-id="17808-190">Relationships</span></span>

 <span data-ttu-id="17808-191">El recurso **listItem** tiene las siguientes relaciones con otros recursos.</span><span class="sxs-lookup"><span data-stu-id="17808-191">The **listItem** resource has the following relationships to other resources.</span></span>

| <span data-ttu-id="17808-192">Nombre de la relación</span><span class="sxs-lookup"><span data-stu-id="17808-192">Relationship name</span></span> | <span data-ttu-id="17808-193">Tipo</span><span class="sxs-lookup"><span data-stu-id="17808-193">Type</span></span>                           | <span data-ttu-id="17808-194">Descripción</span><span class="sxs-lookup"><span data-stu-id="17808-194">Description</span></span>
|:------------------|:-------------------------------|:-------------------------------
| <span data-ttu-id="17808-195">activities</span><span class="sxs-lookup"><span data-stu-id="17808-195">activities</span></span>        | <span data-ttu-id="17808-196">Colección [itemActivity][]</span><span class="sxs-lookup"><span data-stu-id="17808-196">[itemActivity][] collection</span></span>    | <span data-ttu-id="17808-197">Lista de actividades recientes que tuvieron lugar en este elemento.</span><span class="sxs-lookup"><span data-stu-id="17808-197">The list of recent activities that took place on this item.</span></span>
| <span data-ttu-id="17808-198">análisis</span><span class="sxs-lookup"><span data-stu-id="17808-198">analytics</span></span>         | <span data-ttu-id="17808-199">recursos de [itemAnalytics][]</span><span class="sxs-lookup"><span data-stu-id="17808-199">[itemAnalytics][] resource</span></span>     | <span data-ttu-id="17808-200">Análisis acerca de las actividades de vista que tuvieron lugar en este elemento.</span><span class="sxs-lookup"><span data-stu-id="17808-200">Analytics about the view activities that took place on this item.</span></span>
| <span data-ttu-id="17808-201">driveItem</span><span class="sxs-lookup"><span data-stu-id="17808-201">driveItem</span></span>         | <span data-ttu-id="17808-202">[driveItem][]</span><span class="sxs-lookup"><span data-stu-id="17808-202">[driveItem][]</span></span>                  | <span data-ttu-id="17808-203">Para bibliotecas de documentos, la relación **driveItem** expone el recurso listItem como un recurso **[driveItem][]**</span><span class="sxs-lookup"><span data-stu-id="17808-203">For document libraries, the **driveItem** relationship exposes the listItem as a **[driveItem][]**</span></span>
| <span data-ttu-id="17808-204">fields</span><span class="sxs-lookup"><span data-stu-id="17808-204">fields</span></span>            | <span data-ttu-id="17808-205">[fieldValueSet][]</span><span class="sxs-lookup"><span data-stu-id="17808-205">[fieldValueSet][]</span></span>              | <span data-ttu-id="17808-206">Los valores de las columnas establecidos en este elemento de lista.</span><span class="sxs-lookup"><span data-stu-id="17808-206">The values of the columns set on this list item.</span></span>
| <span data-ttu-id="17808-207">versiones</span><span class="sxs-lookup"><span data-stu-id="17808-207">versions</span></span>          | <span data-ttu-id="17808-208">colección de [listItemVersion][]</span><span class="sxs-lookup"><span data-stu-id="17808-208">[listItemVersion][] collection</span></span> | <span data-ttu-id="17808-209">La lista de las versiones anteriores del elemento de lista.</span><span class="sxs-lookup"><span data-stu-id="17808-209">The list of previous versions of the list item.</span></span>

[baseItem]: baseitem.md
[contentTypeInfo]: contenttypeinfo.md
[driveItem]: driveitem.md
[fieldValueSet]: fieldvalueset.md
[identitySet]: identityset.md
[itemActivity]: itemactivity.md
[itemAnalytics]: itemanalytics.md
[itemReference]: itemreference.md
[list]: list.md
[listItemVersion]: listitemversion.md
[sharepointIds]: sharepointids.md

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
