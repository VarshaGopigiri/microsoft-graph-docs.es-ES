---
author: rahmit
ms.author: rahmit
ms.date: 03/15/2018
title: SitePage
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: a756929212dbca04f16e9e4701e34bbd8d4de28f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27939241"
---
# <a name="sitepage-resource"></a><span data-ttu-id="be7ed-102">recursos de sitePage</span><span class="sxs-lookup"><span data-stu-id="be7ed-102">sitePage resource</span></span>

> <span data-ttu-id="be7ed-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="be7ed-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="be7ed-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="be7ed-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="be7ed-105">Este recurso representa una página en la [lista][]de SitePages.</span><span class="sxs-lookup"><span data-stu-id="be7ed-105">This resource represents a page in the SitePages [list][].</span></span>
<span data-ttu-id="be7ed-106">Contiene una colección de [webPart][], diseño y el título.</span><span class="sxs-lookup"><span data-stu-id="be7ed-106">It contains the title, layout, and a collection of [webPart][]s.</span></span>

## <a name="tasks-on-a-page"></a><span data-ttu-id="be7ed-107">Tareas de una página</span><span class="sxs-lookup"><span data-stu-id="be7ed-107">Tasks on a page</span></span>

<span data-ttu-id="be7ed-108">Las siguientes tareas están disponibles para los recursos de **sitePage** .</span><span class="sxs-lookup"><span data-stu-id="be7ed-108">The following tasks are available for **sitePage** resources.</span></span>
<span data-ttu-id="be7ed-109">Todos los ejemplos siguientes son con respecto a un [sitio][], por ejemplo: `https://graph.microsoft.com/{api-version}/sites/{site-id}`.</span><span class="sxs-lookup"><span data-stu-id="be7ed-109">All examples below are relative to a [site][], eg: `https://graph.microsoft.com/{api-version}/sites/{site-id}`.</span></span>

| <span data-ttu-id="be7ed-110">Tarea común</span><span class="sxs-lookup"><span data-stu-id="be7ed-110">Common task</span></span>                     | <span data-ttu-id="be7ed-111">Método HTTP</span><span class="sxs-lookup"><span data-stu-id="be7ed-111">HTTP method</span></span>
|:--------------------------------|:------------------------------
| <span data-ttu-id="be7ed-112">[Enumerar páginas][]</span><span class="sxs-lookup"><span data-stu-id="be7ed-112">[List pages][]</span></span>                  | <span data-ttu-id="be7ed-113">OBTENER /pages</span><span class="sxs-lookup"><span data-stu-id="be7ed-113">GET /pages</span></span>
| <span data-ttu-id="be7ed-114">[Obtener página][]</span><span class="sxs-lookup"><span data-stu-id="be7ed-114">[Get page][]</span></span>                    | <span data-ttu-id="be7ed-115">OBTENER /pages/ {página-id}</span><span class="sxs-lookup"><span data-stu-id="be7ed-115">GET /pages/{page-id}</span></span>
| <span data-ttu-id="be7ed-116">[Create][]</span><span class="sxs-lookup"><span data-stu-id="be7ed-116">[Create][]</span></span>                      | <span data-ttu-id="be7ed-117">POST /pages</span><span class="sxs-lookup"><span data-stu-id="be7ed-117">POST /pages</span></span>
| <span data-ttu-id="be7ed-118">[Delete][]</span><span class="sxs-lookup"><span data-stu-id="be7ed-118">[Delete][]</span></span>                      | <span data-ttu-id="be7ed-119">ELIMINAR /pages/ {página-id}</span><span class="sxs-lookup"><span data-stu-id="be7ed-119">DELETE /pages/{page-id}</span></span>
| <span data-ttu-id="be7ed-120">[Publish][]</span><span class="sxs-lookup"><span data-stu-id="be7ed-120">[Publish][]</span></span>                     | <span data-ttu-id="be7ed-121">REGISTRAR /pages/ {página-id} / publicar</span><span class="sxs-lookup"><span data-stu-id="be7ed-121">POST /pages/{page-id}/publish</span></span>

[Enumerar páginas]: ../api/sitepage-list.md
[List pages]: ../api/sitepage-list.md
[Obtener página]: ../api/sitepage-get.md
[Get page]: ../api/sitepage-get.md
[Create]: ../api/sitepage-create.md
[Delete]: ../api/sitepage-delete.md
[Publish]: ../api/sitepage-publish.md

## <a name="json-representation"></a><span data-ttu-id="be7ed-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="be7ed-127">JSON representation</span></span>

<span data-ttu-id="be7ed-128">Aquí es una representación JSON de un recurso de **sitePage** .</span><span class="sxs-lookup"><span data-stu-id="be7ed-128">Here is a JSON representation of a **sitePage** resource.</span></span>

<!--{
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.baseItem",
  "@odata.type": "microsoft.graph.sitePage"
}-->

```json
{
  "contentType": { "@odata.type": "microsoft.graph.contentTypeInfo" },

  /* page content */
  "title": "string",
  "pageLayout": "Article",
  "webParts": [{ "@odata.type": "microsoft.graph.sitePageWebParts" }],

  /* authoring metadata */
  "publishingState": { "@odata.type": "microsoft.graph.publicationFacet" },

  /* inherited from baseItem */
  "id": "string",
  "name": "string",
  "createdBy": { "@odata.type": "microsoft.graph.identitySet" },
  "eTag": "string",
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "datetime",
  "parentReference": { "@odata.type": "microsoft.graph.itemReference" },
  "webUrl": "url"
}
```

## <a name="properties"></a><span data-ttu-id="be7ed-129">Propiedades</span><span class="sxs-lookup"><span data-stu-id="be7ed-129">Properties</span></span>

<span data-ttu-id="be7ed-130">El recurso **sitePage** tiene las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="be7ed-130">The **sitePage** resource has the following properties.</span></span>

| <span data-ttu-id="be7ed-131">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="be7ed-131">Property name</span></span>    | <span data-ttu-id="be7ed-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="be7ed-132">Type</span></span>                         | <span data-ttu-id="be7ed-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="be7ed-133">Description</span></span>
|:-----------------|:-----------------------------|:---------------------------
| <span data-ttu-id="be7ed-134">contentType</span><span class="sxs-lookup"><span data-stu-id="be7ed-134">contentType</span></span>      | <span data-ttu-id="be7ed-135">[contentTypeInfo][]</span><span class="sxs-lookup"><span data-stu-id="be7ed-135">[contentTypeInfo][]</span></span>          | <span data-ttu-id="be7ed-136">El tipo de contenido de la página.</span><span class="sxs-lookup"><span data-stu-id="be7ed-136">The content type of the page.</span></span>

## <a name="page-content"></a><span data-ttu-id="be7ed-137">Contenido de la página</span><span class="sxs-lookup"><span data-stu-id="be7ed-137">Page Content</span></span>

<span data-ttu-id="be7ed-138">El recurso **sitePage** tiene los siguientes campos de contenido.</span><span class="sxs-lookup"><span data-stu-id="be7ed-138">The **sitePage** resource has the following content fields.</span></span>

| <span data-ttu-id="be7ed-139">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="be7ed-139">Property name</span></span>      | <span data-ttu-id="be7ed-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="be7ed-140">Type</span></span>                       | <span data-ttu-id="be7ed-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="be7ed-141">Description</span></span>
|:-------------------|:---------------------------|:---------------------------
| <span data-ttu-id="be7ed-142">title</span><span class="sxs-lookup"><span data-stu-id="be7ed-142">title</span></span>              | <span data-ttu-id="be7ed-143">string</span><span class="sxs-lookup"><span data-stu-id="be7ed-143">string</span></span>                     | <span data-ttu-id="be7ed-144">El título de la página.</span><span class="sxs-lookup"><span data-stu-id="be7ed-144">The title of the page.</span></span>
| <span data-ttu-id="be7ed-145">pageLayout</span><span class="sxs-lookup"><span data-stu-id="be7ed-145">pageLayout</span></span>         | <span data-ttu-id="be7ed-146">string</span><span class="sxs-lookup"><span data-stu-id="be7ed-146">string</span></span>                     | <span data-ttu-id="be7ed-147">El nombre del diseño de página de la página.</span><span class="sxs-lookup"><span data-stu-id="be7ed-147">The name of the page layout of the page.</span></span>
| <span data-ttu-id="be7ed-148">elementos Web</span><span class="sxs-lookup"><span data-stu-id="be7ed-148">webParts</span></span>           | <span data-ttu-id="be7ed-149">[elemento Web][]</span><span class="sxs-lookup"><span data-stu-id="be7ed-149">[webPart][]</span></span>                | <span data-ttu-id="be7ed-150">Los elementos web en la página.</span><span class="sxs-lookup"><span data-stu-id="be7ed-150">The web parts on the page.</span></span>

## <a name="authoring-metadata"></a><span data-ttu-id="be7ed-151">Creación de metadatos</span><span class="sxs-lookup"><span data-stu-id="be7ed-151">Authoring Metadata</span></span>

<span data-ttu-id="be7ed-152">El recurso **sitePage** tiene los siguientes metadatos relacionados con la creación.</span><span class="sxs-lookup"><span data-stu-id="be7ed-152">The **sitePage** resource has the following authoring-related metadata.</span></span> <span data-ttu-id="be7ed-153">La propiedad publishingState reflejará el estado desprotegido like o publicado de creación de páginas.</span><span class="sxs-lookup"><span data-stu-id="be7ed-153">The publishingState property will reflect the page authoring state like checked out or published.</span></span>

| <span data-ttu-id="be7ed-154">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="be7ed-154">Property name</span></span>          | <span data-ttu-id="be7ed-155">Tipo</span><span class="sxs-lookup"><span data-stu-id="be7ed-155">Type</span></span>                   | <span data-ttu-id="be7ed-156">Descripción</span><span class="sxs-lookup"><span data-stu-id="be7ed-156">Description</span></span>
|:-----------------------|:-----------------------|:---------------------------
| <span data-ttu-id="be7ed-157">publishingState</span><span class="sxs-lookup"><span data-stu-id="be7ed-157">publishingState</span></span>        | <span data-ttu-id="be7ed-158">[publicationFacet][]</span><span class="sxs-lookup"><span data-stu-id="be7ed-158">[publicationFacet][]</span></span>   | <span data-ttu-id="be7ed-159">El estado de publicación y la versión MM.mm de la página.</span><span class="sxs-lookup"><span data-stu-id="be7ed-159">The publishing status and the MM.mm version of the page.</span></span>

<span data-ttu-id="be7ed-160">Las siguientes propiedades se heredan de **[baseItem][]**.</span><span class="sxs-lookup"><span data-stu-id="be7ed-160">The following properties are inherited from **[baseItem][]**.</span></span>

| <span data-ttu-id="be7ed-161">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="be7ed-161">Property name</span></span>        | <span data-ttu-id="be7ed-162">Tipo</span><span class="sxs-lookup"><span data-stu-id="be7ed-162">Type</span></span>              | <span data-ttu-id="be7ed-163">Descripción</span><span class="sxs-lookup"><span data-stu-id="be7ed-163">Description</span></span>
|:---------------------|:------------------|:----------------------------------
| <span data-ttu-id="be7ed-164">id</span><span class="sxs-lookup"><span data-stu-id="be7ed-164">id</span></span>                   | <span data-ttu-id="be7ed-165">string</span><span class="sxs-lookup"><span data-stu-id="be7ed-165">string</span></span>            | <span data-ttu-id="be7ed-p105">El identificador único del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="be7ed-p105">The unique identifier of the item. Read-only.</span></span>
| <span data-ttu-id="be7ed-168">name</span><span class="sxs-lookup"><span data-stu-id="be7ed-168">name</span></span>                 | <span data-ttu-id="be7ed-169">string</span><span class="sxs-lookup"><span data-stu-id="be7ed-169">string</span></span>            | <span data-ttu-id="be7ed-170">Nombre o título del elemento.</span><span class="sxs-lookup"><span data-stu-id="be7ed-170">The name / title of the item.</span></span>
| <span data-ttu-id="be7ed-171">createdBy</span><span class="sxs-lookup"><span data-stu-id="be7ed-171">createdBy</span></span>            | <span data-ttu-id="be7ed-172">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="be7ed-172">[identitySet][]</span></span>   | <span data-ttu-id="be7ed-173">Identidad del creador de este elemento.</span><span class="sxs-lookup"><span data-stu-id="be7ed-173">Identity of the creator of this item.</span></span> <span data-ttu-id="be7ed-174">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="be7ed-174">Read-only.</span></span>
| <span data-ttu-id="be7ed-175">eTag</span><span class="sxs-lookup"><span data-stu-id="be7ed-175">eTag</span></span>                 | <span data-ttu-id="be7ed-176">string</span><span class="sxs-lookup"><span data-stu-id="be7ed-176">string</span></span>            | <span data-ttu-id="be7ed-p107">ETag para el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="be7ed-p107">ETag for the item. Read-only.</span></span>
| <span data-ttu-id="be7ed-179">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="be7ed-179">lastModifiedBy</span></span>       | <span data-ttu-id="be7ed-180">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="be7ed-180">[identitySet][]</span></span>   | <span data-ttu-id="be7ed-181">Identidad del usuario que modificó por última vez este elemento.</span><span class="sxs-lookup"><span data-stu-id="be7ed-181">Identity of the last modifier of this item.</span></span> <span data-ttu-id="be7ed-182">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="be7ed-182">Read-only.</span></span>
| <span data-ttu-id="be7ed-183">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="be7ed-183">lastModifiedDateTime</span></span> | <span data-ttu-id="be7ed-184">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="be7ed-184">DateTimeOffset</span></span>    | <span data-ttu-id="be7ed-p109">Fecha y hora de la última modificación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="be7ed-p109">The date and time the item was last modified. Read-only.</span></span>
| <span data-ttu-id="be7ed-187">parentReference</span><span class="sxs-lookup"><span data-stu-id="be7ed-187">parentReference</span></span>      | <span data-ttu-id="be7ed-188">[itemReference][]</span><span class="sxs-lookup"><span data-stu-id="be7ed-188">[itemReference][]</span></span> | <span data-ttu-id="be7ed-p110">Fecha y hora de la última modificación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="be7ed-p110">The date and time the item was last modified. Read-only.</span></span>
| <span data-ttu-id="be7ed-191">webUrl</span><span class="sxs-lookup"><span data-stu-id="be7ed-191">webUrl</span></span>               | <span data-ttu-id="be7ed-192">string (url)</span><span class="sxs-lookup"><span data-stu-id="be7ed-192">string (url)</span></span>      | <span data-ttu-id="be7ed-p111">Dirección URL que muestra el elemento en el explorador. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="be7ed-p111">URL that displays the item in the browser. Read-only.</span></span>

## <a name="relationships"></a><span data-ttu-id="be7ed-195">Relaciones</span><span class="sxs-lookup"><span data-stu-id="be7ed-195">Relationships</span></span>

<span data-ttu-id="be7ed-196">El recurso **sitePage** no tiene relaciones con otros recursos.</span><span class="sxs-lookup"><span data-stu-id="be7ed-196">The **sitePage** resource does not have relationships to other resources.</span></span>

[baseItem]: baseitem.md
[contentTypeInfo]: contenttypeinfo.md
[columnDefinition]: columndefinition.md
[identitySet]: identityset.md
[itemReference]: itemreference.md
[lista]: list.md
[list]: list.md
[listInfo]: listinfo.md
[listItem]: listitem.md
[publicationFacet]: publicationfacet.md
[site]: site.md
[elemento Web]: webpart.md
[webPart]: webpart.md

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/Page",
  "tocBookmarks": {
    "Page": "#"
  }
} -->

<!--
TODO:
* Define {page-id}
* Update examples
    * Be consistent with other URLs in the documentation.
    * Try to use the same site, library, etc.
    * Add the URL to the underlying list item resource in the API
* PATCH for list item patches /item/{item-id}/fields.
-->
