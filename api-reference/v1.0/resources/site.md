---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Sitio
ms.openlocfilehash: ae8962dfa38c3c6f3e06ccb687eb42a4a8262f1a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032702"
---
# <a name="site-resource"></a><span data-ttu-id="87776-102">Recurso site</span><span class="sxs-lookup"><span data-stu-id="87776-102">Site resource</span></span>

<span data-ttu-id="87776-103">El recurso **site** proporciona metadatos y relaciones para un sitio de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="87776-103">The **site** resource provides metadata and relationships for a SharePoint site.</span></span>

## <a name="tasks"></a><span data-ttu-id="87776-104">Tareas</span><span class="sxs-lookup"><span data-stu-id="87776-104">Tasks</span></span>

<span data-ttu-id="87776-105">Todos los ejemplos siguientes son relativos a `https://graph.microsoft.com/v1.0`.</span><span class="sxs-lookup"><span data-stu-id="87776-105">All examples below are relative to `https://graph.microsoft.com/v1.0`.</span></span>

| <span data-ttu-id="87776-106">Nombre de tarea</span><span class="sxs-lookup"><span data-stu-id="87776-106">Task name</span></span>                | <span data-ttu-id="87776-107">Solicitud de ejemplo</span><span class="sxs-lookup"><span data-stu-id="87776-107">Example Request</span></span>
|:-------------------------|:--------------------------------------------------
| <span data-ttu-id="87776-108">[Obtener sitio raíz][]</span><span class="sxs-lookup"><span data-stu-id="87776-108">[Get root site][]</span></span>        | <span data-ttu-id="87776-109">GET /sites/root</span><span class="sxs-lookup"><span data-stu-id="87776-109">GET /sites/root</span></span>
| <span data-ttu-id="87776-110">[Obtener sitio][]</span><span class="sxs-lookup"><span data-stu-id="87776-110">[Get site][]</span></span>             | <span data-ttu-id="87776-111">GET /sites/{site-id}</span><span class="sxs-lookup"><span data-stu-id="87776-111">GET /sites/{site-id}</span></span>
| <span data-ttu-id="87776-112">[Obtener sitio por su ruta de acceso][]</span><span class="sxs-lookup"><span data-stu-id="87776-112">[Get site by path][]</span></span>     | <span data-ttu-id="87776-113">GET /sites/{hostname}:/{site-path}</span><span class="sxs-lookup"><span data-stu-id="87776-113">GET /sites/{hostname}:/{site-path}</span></span>
| <span data-ttu-id="87776-114">[Obtener sitio para un grupo][]</span><span class="sxs-lookup"><span data-stu-id="87776-114">[Get site for a group][]</span></span> | <span data-ttu-id="87776-115">GET /groups/{group-id}/sites/root</span><span class="sxs-lookup"><span data-stu-id="87776-115">GET /groups/{group-id}/sites/root</span></span>
| <span data-ttu-id="87776-116">[Buscar sitios][]</span><span class="sxs-lookup"><span data-stu-id="87776-116">[Search for sites][]</span></span>     | <span data-ttu-id="87776-117">GET /sites?search={query}</span><span class="sxs-lookup"><span data-stu-id="87776-117">GET /sites?search={query}</span></span>

[Obtener sitio]: ../api/site-get.md
[Get site]: ../api/site-get.md
[Obtener sitio raíz]: ../api/site-get.md
[Get root site]: ../api/site-get.md
[Obtener sitio por su ruta de acceso]: ../api/site-getbypath.md
[Get site by path]: ../api/site-getbypath.md
[Obtener sitio para un grupo]: ../api/site-get.md
[Get site for a group]: ../api/site-get.md
[Buscar sitios]: ../api/site-search.md
[Search for sites]: ../api/site-search.md

## <a name="json-representation"></a><span data-ttu-id="87776-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="87776-123">JSON representation</span></span>

<span data-ttu-id="87776-124">A continuación se incluye una representación JSON del recurso **site**.</span><span class="sxs-lookup"><span data-stu-id="87776-124">Here is a JSON representation of a **site** resource.</span></span>

<span data-ttu-id="87776-125">El recurso **site** deriva de [**baseItem**](baseitem.md) y hereda sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="87776-125">The **site** resource is derived from [**baseItem**](baseitem.md) and inherits properties from that resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [
    "root",
    "sharepointIds",
    "siteCollection",
    "drive",
    "drives",
    "sites"
  ],
  "keyProperty": "id",
  "baseType": "microsoft.graph.baseItem",
  "@odata.type": "microsoft.graph.site"
}-->

```json
{
  "id": "string",
  "root": { "@odata.type": "microsoft.graph.root" },
  "sharepointIds": { "@odata.type": "microsoft.graph.sharepointIds" },
  "siteCollection": {"@odata.type": "microsoft.graph.siteCollection"},
  "displayName": "string",

  /* relationships */
  "contentTypes": [ { "@odata.type": "microsoft.graph.contentType" }],
  "drive": { "@odata.type": "microsoft.graph.drive" },
  "drives": [ { "@odata.type": "microsoft.graph.drive" }],
  "items": [ { "@odata.type": "microsoft.graph.baseItem" }],
  "lists": [ { "@odata.type": "microsoft.graph.list" }],
  "sites": [ { "@odata.type": "microsoft.graph.site"} ],
  "columns": [ { "@odata.type": "microsoft.graph.columnDefinition" }],
  "onenote": { "@odata.type": "microsoft.graph.onenote"},

  /* inherited from baseItem */
  "name": "string",
  "createdDateTime": "datetime",
  "description": "string",
  "eTag": "string",
  "lastModifiedDateTime": "datetime",
  "webUrl": "url"
}
```

## <a name="properties"></a><span data-ttu-id="87776-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="87776-126">Properties</span></span>

| <span data-ttu-id="87776-127">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="87776-127">Property name</span></span>            | <span data-ttu-id="87776-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="87776-128">Type</span></span>                                | <span data-ttu-id="87776-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="87776-129">Description</span></span>                                                                                    |
| :----------------------- | :---------------------------------- | :--------------------------------------------------------------------------------------------- |
| <span data-ttu-id="87776-130">**id**</span><span class="sxs-lookup"><span data-stu-id="87776-130">**id**</span></span>                   | <span data-ttu-id="87776-131">string</span><span class="sxs-lookup"><span data-stu-id="87776-131">string</span></span>                              | <span data-ttu-id="87776-p101">El identificador único del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="87776-p101">The unique identifier of the item. Read-only.</span></span>                                                  |
| <span data-ttu-id="87776-134">**createdDateTime**</span><span class="sxs-lookup"><span data-stu-id="87776-134">**createdDateTime**</span></span>      | <span data-ttu-id="87776-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="87776-135">DateTimeOffset</span></span>                      | <span data-ttu-id="87776-p102">La fecha y la hora de creación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="87776-p102">The date and time the item was created. Read-only.</span></span>                                             |
| <span data-ttu-id="87776-138">**description**</span><span class="sxs-lookup"><span data-stu-id="87776-138">**description**</span></span>          | <span data-ttu-id="87776-139">string</span><span class="sxs-lookup"><span data-stu-id="87776-139">string</span></span>                              | <span data-ttu-id="87776-140">Texto descriptivo del sitio.</span><span class="sxs-lookup"><span data-stu-id="87776-140">The descriptive text for the site.</span></span>                                                             |
| <span data-ttu-id="87776-141">**displayName**</span><span class="sxs-lookup"><span data-stu-id="87776-141">**displayName**</span></span>          | <span data-ttu-id="87776-142">string</span><span class="sxs-lookup"><span data-stu-id="87776-142">string</span></span>                              | <span data-ttu-id="87776-p103">El título completo del sitio. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="87776-p103">The full title for the site. Read-only.</span></span>                                                        |
| <span data-ttu-id="87776-145">**eTag**</span><span class="sxs-lookup"><span data-stu-id="87776-145">**eTag**</span></span>                 | <span data-ttu-id="87776-146">string</span><span class="sxs-lookup"><span data-stu-id="87776-146">string</span></span>                              | <span data-ttu-id="87776-p104">ETag para el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="87776-p104">ETag for the item. Read-only.</span></span>                                                                  |
| <span data-ttu-id="87776-149">**lastModifiedDateTime**</span><span class="sxs-lookup"><span data-stu-id="87776-149">**lastModifiedDateTime**</span></span> | <span data-ttu-id="87776-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="87776-150">DateTimeOffset</span></span>                      | <span data-ttu-id="87776-p105">Fecha y hora de la última modificación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="87776-p105">The date and time the item was last modified. Read-only.</span></span>                                       |
| <span data-ttu-id="87776-153">**name**</span><span class="sxs-lookup"><span data-stu-id="87776-153">**name**</span></span>                 | <span data-ttu-id="87776-154">string</span><span class="sxs-lookup"><span data-stu-id="87776-154">string</span></span>                              | <span data-ttu-id="87776-155">Nombre o título del elemento.</span><span class="sxs-lookup"><span data-stu-id="87776-155">The name / title of the item.</span></span>                                                                  |
| <span data-ttu-id="87776-156">**root**</span><span class="sxs-lookup"><span data-stu-id="87776-156">**root**</span></span>                 | [<span data-ttu-id="87776-157">root</span><span class="sxs-lookup"><span data-stu-id="87776-157">root</span></span>](root.md)                     | <span data-ttu-id="87776-p106">Si está presente, indica que se trata del sitio raíz de la colección de sitios. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="87776-p106">If present, indicates that this is the root site in the site collection. Read-only.</span></span>            |
| <span data-ttu-id="87776-160">**sharepointIds**</span><span class="sxs-lookup"><span data-stu-id="87776-160">**sharepointIds**</span></span>        | [<span data-ttu-id="87776-161">sharepointIds</span><span class="sxs-lookup"><span data-stu-id="87776-161">sharepointIds</span></span>](sharepointids.md)   | <span data-ttu-id="87776-p107">Devuelve los identificadores útiles para la compatibilidad con REST de SharePoint. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="87776-p107">Returns identifiers useful for SharePoint REST compatibility. Read-only.</span></span>                       |
| <span data-ttu-id="87776-164">**siteCollection**</span><span class="sxs-lookup"><span data-stu-id="87776-164">**siteCollection**</span></span>       | [<span data-ttu-id="87776-165">siteCollection</span><span class="sxs-lookup"><span data-stu-id="87776-165">siteCollection</span></span>](sitecollection.md) | <span data-ttu-id="87776-p108">Proporciona detalles sobre la colección de sitios del sitio. Solo disponible en el sitio raíz. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="87776-p108">Provides details about the site's site collection. Available only on the root site. Read-only.</span></span> |
| <span data-ttu-id="87776-169">**webUrl**</span><span class="sxs-lookup"><span data-stu-id="87776-169">**webUrl**</span></span>               | <span data-ttu-id="87776-170">string (url)</span><span class="sxs-lookup"><span data-stu-id="87776-170">string (url)</span></span>                        | <span data-ttu-id="87776-p109">Dirección URL que muestra el elemento en el explorador. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="87776-p109">URL that displays the item in the browser. Read-only.</span></span>                                          |

## <a name="relationships"></a><span data-ttu-id="87776-173">Relaciones</span><span class="sxs-lookup"><span data-stu-id="87776-173">Relationships</span></span>

| <span data-ttu-id="87776-174">Nombre de la relación</span><span class="sxs-lookup"><span data-stu-id="87776-174">Relationship name</span></span> | <span data-ttu-id="87776-175">Tipo</span><span class="sxs-lookup"><span data-stu-id="87776-175">Type</span></span>                             | <span data-ttu-id="87776-176">Descripción</span><span class="sxs-lookup"><span data-stu-id="87776-176">Description</span></span>
|:------------------|:---------------------------------|:----------------------
| <span data-ttu-id="87776-177">**columns**</span><span class="sxs-lookup"><span data-stu-id="87776-177">**columns**</span></span>       | <span data-ttu-id="87776-178">Collection([columnDefinition][])</span><span class="sxs-lookup"><span data-stu-id="87776-178">Collection([columnDefinition][])</span></span> | <span data-ttu-id="87776-179">La colección de definiciones de columna reutilizables en listas en este sitio.</span><span class="sxs-lookup"><span data-stu-id="87776-179">The collection of column definitions reusable across lists under this site.</span></span>
| <span data-ttu-id="87776-180">**contentTypes**</span><span class="sxs-lookup"><span data-stu-id="87776-180">**contentTypes**</span></span>  | <span data-ttu-id="87776-181">Collection([contentType][])</span><span class="sxs-lookup"><span data-stu-id="87776-181">Collection([contentType][])</span></span>      | <span data-ttu-id="87776-182">La colección de tipos de contenido definidos para este sitio.</span><span class="sxs-lookup"><span data-stu-id="87776-182">The collection of content types defined for this site.</span></span>
| <span data-ttu-id="87776-183">**drive**</span><span class="sxs-lookup"><span data-stu-id="87776-183">**drive**</span></span>         | <span data-ttu-id="87776-184">[drive][]</span><span class="sxs-lookup"><span data-stu-id="87776-184">[drive][]</span></span>                        | <span data-ttu-id="87776-185">La unidad predeterminada (biblioteca de documentos) para este sitio.</span><span class="sxs-lookup"><span data-stu-id="87776-185">The default drive (document library) for this site.</span></span>
| <span data-ttu-id="87776-186">**drives**</span><span class="sxs-lookup"><span data-stu-id="87776-186">**drives**</span></span>        | <span data-ttu-id="87776-187">Collection([drive][])</span><span class="sxs-lookup"><span data-stu-id="87776-187">Collection([drive][])</span></span>            | <span data-ttu-id="87776-188">La colección de unidades (bibliotecas de documentos) de este sitio.</span><span class="sxs-lookup"><span data-stu-id="87776-188">The collection of drives (document libraries) under this site.</span></span>
| <span data-ttu-id="87776-189">**items**</span><span class="sxs-lookup"><span data-stu-id="87776-189">**items**</span></span>         | <span data-ttu-id="87776-190">Collection([baseItem][])</span><span class="sxs-lookup"><span data-stu-id="87776-190">Collection([baseItem][])</span></span>         | <span data-ttu-id="87776-p110">Se utiliza para resolver cualquier elemento contenido en este sitio. Esta colección no se puede enumerar.</span><span class="sxs-lookup"><span data-stu-id="87776-p110">Used to address any item contained in this site. This collection cannot be enumerated.</span></span>
| <span data-ttu-id="87776-193">**lists**</span><span class="sxs-lookup"><span data-stu-id="87776-193">**lists**</span></span>         | <span data-ttu-id="87776-194">Collection([list][])</span><span class="sxs-lookup"><span data-stu-id="87776-194">Collection([list][])</span></span>             | <span data-ttu-id="87776-195">La colección de listas en este sitio.</span><span class="sxs-lookup"><span data-stu-id="87776-195">The collection of lists under this site.</span></span>
| <span data-ttu-id="87776-196">**sites**</span><span class="sxs-lookup"><span data-stu-id="87776-196">**sites**</span></span>         | <span data-ttu-id="87776-197">Collection([site][])</span><span class="sxs-lookup"><span data-stu-id="87776-197">Collection([site][])</span></span>             | <span data-ttu-id="87776-198">La colección de subsitios de este sitio.</span><span class="sxs-lookup"><span data-stu-id="87776-198">The collection of the sub-sites under this site.</span></span>
| <span data-ttu-id="87776-199">**onenote**</span><span class="sxs-lookup"><span data-stu-id="87776-199">**onenote**</span></span>       | <span data-ttu-id="87776-200">[onenote][]</span><span class="sxs-lookup"><span data-stu-id="87776-200">[onenote][]</span></span>                      | <span data-ttu-id="87776-201">Realiza una llamada al servicio de OneNote para operaciones relacionadas con blocs de notas.</span><span class="sxs-lookup"><span data-stu-id="87776-201">Calls the OneNote service for notebook related operations.</span></span>

[columnDefinition]: columndefinition.md
[baseItem]: baseitem.md
[contentType]: contenttype.md
[drive]: drive.md
[identitySet]: identityset.md
[list]: list.md
[site]: site.md
[onenote]: onenote.md

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Sites",
  "tocBookmarks": { "Resources/Site": "#" }
} -->
