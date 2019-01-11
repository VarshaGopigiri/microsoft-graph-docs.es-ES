---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: ListItem
localization_priority: Priority
ms.openlocfilehash: bee264fb46e08d55893f41ae6be2a64edb06c3fa
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27833029"
---
# <a name="listitem-resource"></a><span data-ttu-id="73ad8-102">Recurso ListItem</span><span class="sxs-lookup"><span data-stu-id="73ad8-102">ListItem resource</span></span>

<span data-ttu-id="73ad8-103">Este recurso representa un elemento en una **[lista][]** de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="73ad8-103">This resource represents an item in a SharePoint **[list][]**.</span></span>
<span data-ttu-id="73ad8-104">Los valores de columna de la lista están disponibles a través del diccionario `fieldValueSet`.</span><span class="sxs-lookup"><span data-stu-id="73ad8-104">Column values in the list are available through the `fieldValueSet` dictionary.</span></span>

## <a name="tasks-on-a-listitem"></a><span data-ttu-id="73ad8-105">Tareas en un recurso listItem</span><span class="sxs-lookup"><span data-stu-id="73ad8-105">Tasks on a listItem</span></span>

<span data-ttu-id="73ad8-106">Las tareas siguientes están disponibles para los recursos **listItem**.</span><span class="sxs-lookup"><span data-stu-id="73ad8-106">The following tasks are available for **listItem** resources.</span></span>
<span data-ttu-id="73ad8-107">Todos los ejemplos siguientes son relativos a una **[lista][]**, por ejemplo: `https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}`.</span><span class="sxs-lookup"><span data-stu-id="73ad8-107">All examples below are relative to a **[list][]**, eg: `https://graph.microsoft.com/v1.0/sites/{site-id}/lists/{list-id}`.</span></span>

| <span data-ttu-id="73ad8-108">Tarea común</span><span class="sxs-lookup"><span data-stu-id="73ad8-108">Common task</span></span>                    | <span data-ttu-id="73ad8-109">Método HTTP</span><span class="sxs-lookup"><span data-stu-id="73ad8-109">HTTP method</span></span>
|:-------------------------------|:------------------------
| <span data-ttu-id="73ad8-110">[Obtener][]</span><span class="sxs-lookup"><span data-stu-id="73ad8-110">[Get][]</span></span>                        | <span data-ttu-id="73ad8-111">GET /items/{item-id}</span><span class="sxs-lookup"><span data-stu-id="73ad8-111">GET /items/{item-id}</span></span>
| <span data-ttu-id="73ad8-112">[Obtener valores de columna][Obtener]</span><span class="sxs-lookup"><span data-stu-id="73ad8-112">[Get column values][Get]</span></span>       | <span data-ttu-id="73ad8-113">GET /items/{item-id}?expand=fields</span><span class="sxs-lookup"><span data-stu-id="73ad8-113">GET /items/{item-id}?expand=fields</span></span>
| <span data-ttu-id="73ad8-114">[Crear][]</span><span class="sxs-lookup"><span data-stu-id="73ad8-114">[Create][]</span></span>                     | <span data-ttu-id="73ad8-115">POST /items</span><span class="sxs-lookup"><span data-stu-id="73ad8-115">POST /items</span></span>
| <span data-ttu-id="73ad8-116">[Eliminar][]</span><span class="sxs-lookup"><span data-stu-id="73ad8-116">[Delete][]</span></span>                     | <span data-ttu-id="73ad8-117">DELETE /items/{item-id}</span><span class="sxs-lookup"><span data-stu-id="73ad8-117">DELETE /items/{item-id}</span></span>
| <span data-ttu-id="73ad8-118">[Actualizar][]</span><span class="sxs-lookup"><span data-stu-id="73ad8-118">[Update][]</span></span>                     | <span data-ttu-id="73ad8-119">PATCH /items/{item-id}</span><span class="sxs-lookup"><span data-stu-id="73ad8-119">PATCH /items/{item-id}</span></span>
| <span data-ttu-id="73ad8-120">[Actualizar valores de columna][Actualizar]</span><span class="sxs-lookup"><span data-stu-id="73ad8-120">[Update column values][Update]</span></span> | <span data-ttu-id="73ad8-121">PATCH /items/{item-id}/fields</span><span class="sxs-lookup"><span data-stu-id="73ad8-121">PATCH /items/{item-id}/fields</span></span>

[Obtener]: ../api/listitem-get.md
[Get]: ../api/listitem-get.md
[Crear]: ../api/listitem-create.md
[Create]: ../api/listitem-create.md
[Eliminar]: ../api/listitem-delete.md
[Delete]: ../api/listitem-delete.md
[Actualizar]: ../api/listitem-update.md
[Update]: ../api/listitem-update.md

## <a name="json-representation"></a><span data-ttu-id="73ad8-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="73ad8-126">JSON representation</span></span>

<span data-ttu-id="73ad8-127">A continuación se incluye una representación JSON del recurso **listItem**.</span><span class="sxs-lookup"><span data-stu-id="73ad8-127">Here is a JSON representation of a **listItem** resource.</span></span>

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

## <a name="properties"></a><span data-ttu-id="73ad8-128">Propiedades</span><span class="sxs-lookup"><span data-stu-id="73ad8-128">Properties</span></span>

<span data-ttu-id="73ad8-129">El recurso **listItem** tiene las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="73ad8-129">The **listItem** resource has the following properties.</span></span>

| <span data-ttu-id="73ad8-130">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="73ad8-130">Property name</span></span> | <span data-ttu-id="73ad8-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="73ad8-131">Type</span></span>                | <span data-ttu-id="73ad8-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="73ad8-132">Description</span></span>
|:--------------|:--------------------|:-------------------------------
| <span data-ttu-id="73ad8-133">contentType</span><span class="sxs-lookup"><span data-stu-id="73ad8-133">contentType</span></span>   | <span data-ttu-id="73ad8-134">[contentTypeInfo][]</span><span class="sxs-lookup"><span data-stu-id="73ad8-134">[contentTypeInfo][]</span></span> | <span data-ttu-id="73ad8-135">El tipo de contenido de este elemento de lista</span><span class="sxs-lookup"><span data-stu-id="73ad8-135">The content type of this list item</span></span>

<span data-ttu-id="73ad8-136">Las siguientes propiedades se heredan de **[baseItem][]**.</span><span class="sxs-lookup"><span data-stu-id="73ad8-136">The following properties are inherited from **[baseItem][]**.</span></span>

| <span data-ttu-id="73ad8-137">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="73ad8-137">Property name</span></span>        | <span data-ttu-id="73ad8-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="73ad8-138">Type</span></span>              | <span data-ttu-id="73ad8-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="73ad8-139">Description</span></span>
|:---------------------|:------------------|:----------------------------------
| <span data-ttu-id="73ad8-140">id</span><span class="sxs-lookup"><span data-stu-id="73ad8-140">id</span></span>                   | <span data-ttu-id="73ad8-141">string</span><span class="sxs-lookup"><span data-stu-id="73ad8-141">string</span></span>            | <span data-ttu-id="73ad8-p103">El identificador único del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="73ad8-p103">The unique identifier of the item. Read-only.</span></span>
| <span data-ttu-id="73ad8-144">name</span><span class="sxs-lookup"><span data-stu-id="73ad8-144">name</span></span>                 | <span data-ttu-id="73ad8-145">string</span><span class="sxs-lookup"><span data-stu-id="73ad8-145">string</span></span>            | <span data-ttu-id="73ad8-146">Nombre o título del elemento.</span><span class="sxs-lookup"><span data-stu-id="73ad8-146">The name / title of the item.</span></span>
| <span data-ttu-id="73ad8-147">createdBy</span><span class="sxs-lookup"><span data-stu-id="73ad8-147">createdBy</span></span>            | <span data-ttu-id="73ad8-148">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="73ad8-148">[identitySet][]</span></span>   | <span data-ttu-id="73ad8-149">Identidad del creador de este elemento.</span><span class="sxs-lookup"><span data-stu-id="73ad8-149">Identity of the creator of this item.</span></span> <span data-ttu-id="73ad8-150">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="73ad8-150">Read-only.</span></span>
| <span data-ttu-id="73ad8-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="73ad8-151">createdDateTime</span></span>      | <span data-ttu-id="73ad8-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="73ad8-152">DateTimeOffset</span></span>    | <span data-ttu-id="73ad8-p105">La fecha y la hora de creación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="73ad8-p105">The date and time the item was created. Read-only.</span></span>
| <span data-ttu-id="73ad8-155">descripción</span><span class="sxs-lookup"><span data-stu-id="73ad8-155">description</span></span>          | <span data-ttu-id="73ad8-156">string</span><span class="sxs-lookup"><span data-stu-id="73ad8-156">string</span></span>            | <span data-ttu-id="73ad8-157">Texto descriptivo del elemento.</span><span class="sxs-lookup"><span data-stu-id="73ad8-157">The descriptive text for the item.</span></span>
| <span data-ttu-id="73ad8-158">eTag</span><span class="sxs-lookup"><span data-stu-id="73ad8-158">eTag</span></span>                 | <span data-ttu-id="73ad8-159">string</span><span class="sxs-lookup"><span data-stu-id="73ad8-159">string</span></span>            | <span data-ttu-id="73ad8-p106">ETag para el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="73ad8-p106">ETag for the item. Read-only.</span></span>                                                          |
| <span data-ttu-id="73ad8-162">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="73ad8-162">lastModifiedBy</span></span>       | <span data-ttu-id="73ad8-163">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="73ad8-163">[identitySet][]</span></span>   | <span data-ttu-id="73ad8-164">Identidad del usuario que modificó por última vez este elemento.</span><span class="sxs-lookup"><span data-stu-id="73ad8-164">Identity of the last modifier of this item.</span></span> <span data-ttu-id="73ad8-165">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="73ad8-165">Read-only.</span></span>
| <span data-ttu-id="73ad8-166">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="73ad8-166">lastModifiedDateTime</span></span> | <span data-ttu-id="73ad8-167">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="73ad8-167">DateTimeOffset</span></span>    | <span data-ttu-id="73ad8-p108">Fecha y hora de la última modificación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="73ad8-p108">The date and time the item was last modified. Read-only.</span></span>
| <span data-ttu-id="73ad8-170">parentReference</span><span class="sxs-lookup"><span data-stu-id="73ad8-170">parentReference</span></span>      | <span data-ttu-id="73ad8-171">[itemReference][]</span><span class="sxs-lookup"><span data-stu-id="73ad8-171">[itemReference][]</span></span> | <span data-ttu-id="73ad8-p109">Información primaria, si el elemento tiene un elemento primario. Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="73ad8-p109">Parent information, if the item has a parent. Read-write.</span></span>
| <span data-ttu-id="73ad8-174">sharepointIds</span><span class="sxs-lookup"><span data-stu-id="73ad8-174">sharepointIds</span></span>        | <span data-ttu-id="73ad8-175">[sharepointIds][]</span><span class="sxs-lookup"><span data-stu-id="73ad8-175">[sharepointIds][]</span></span> | <span data-ttu-id="73ad8-p110">Devuelve los identificadores útiles para la compatibilidad con REST de SharePoint. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="73ad8-p110">Returns identifiers useful for SharePoint REST compatibility. Read-only.</span></span>
| <span data-ttu-id="73ad8-178">webUrl</span><span class="sxs-lookup"><span data-stu-id="73ad8-178">webUrl</span></span>               | <span data-ttu-id="73ad8-179">string (url)</span><span class="sxs-lookup"><span data-stu-id="73ad8-179">string (url)</span></span>      | <span data-ttu-id="73ad8-p111">Dirección URL que muestra el elemento en el explorador. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="73ad8-p111">URL that displays the item in the browser. Read-only.</span></span>

## <a name="relationships"></a><span data-ttu-id="73ad8-182">Relaciones</span><span class="sxs-lookup"><span data-stu-id="73ad8-182">Relationships</span></span>

 <span data-ttu-id="73ad8-183">El recurso **listItem** tiene las siguientes relaciones con otros recursos.</span><span class="sxs-lookup"><span data-stu-id="73ad8-183">The **listItem** resource has the following relationships to other resources.</span></span>

| <span data-ttu-id="73ad8-184">Nombre de la relación</span><span class="sxs-lookup"><span data-stu-id="73ad8-184">Relationship name</span></span> | <span data-ttu-id="73ad8-185">Tipo</span><span class="sxs-lookup"><span data-stu-id="73ad8-185">Type</span></span>                           | <span data-ttu-id="73ad8-186">Descripción</span><span class="sxs-lookup"><span data-stu-id="73ad8-186">Description</span></span>
|:------------------|:-------------------------------|:-------------------------------
| <span data-ttu-id="73ad8-187">driveItem</span><span class="sxs-lookup"><span data-stu-id="73ad8-187">driveItem</span></span>         | <span data-ttu-id="73ad8-188">[driveItem][]</span><span class="sxs-lookup"><span data-stu-id="73ad8-188">[driveItem][]</span></span>                  | <span data-ttu-id="73ad8-189">Para bibliotecas de documentos, la relación **driveItem** expone el recurso listItem como un recurso **[driveItem][]**</span><span class="sxs-lookup"><span data-stu-id="73ad8-189">For document libraries, the **driveItem** relationship exposes the listItem as a **[driveItem][]**</span></span>
| <span data-ttu-id="73ad8-190">fields</span><span class="sxs-lookup"><span data-stu-id="73ad8-190">fields</span></span>            | <span data-ttu-id="73ad8-191">[fieldValueSet][]</span><span class="sxs-lookup"><span data-stu-id="73ad8-191">[fieldValueSet][]</span></span>              | <span data-ttu-id="73ad8-192">Los valores de las columnas establecidos en este elemento de lista.</span><span class="sxs-lookup"><span data-stu-id="73ad8-192">The values of the columns set on this list item.</span></span>
| <span data-ttu-id="73ad8-193">versiones</span><span class="sxs-lookup"><span data-stu-id="73ad8-193">versions</span></span>          | <span data-ttu-id="73ad8-194">colección de [listItemVersion][]</span><span class="sxs-lookup"><span data-stu-id="73ad8-194">[listItemVersion][] collection</span></span> | <span data-ttu-id="73ad8-195">La lista de las versiones anteriores del elemento de lista.</span><span class="sxs-lookup"><span data-stu-id="73ad8-195">The list of previous versions of the list item.</span></span>

[baseItem]: baseitem.md
[contentTypeInfo]: contenttypeinfo.md
[driveItem]: driveitem.md
[fieldValueSet]: fieldvalueset.md
[identitySet]: identityset.md
[itemReference]: itemreference.md
[lista]: list.md
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
