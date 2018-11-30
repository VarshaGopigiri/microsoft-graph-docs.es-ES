---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Sitio
ms.openlocfilehash: d18487d9932227df0ce2de3320fcb71ce94ca735
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088907"
---
# <a name="site-resource-type"></a><span data-ttu-id="69de1-102">tipo de recurso de sitio</span><span class="sxs-lookup"><span data-stu-id="69de1-102">site resource type</span></span>

> <span data-ttu-id="69de1-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="69de1-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="69de1-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="69de1-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="69de1-105">El recurso **site** proporciona metadatos y relaciones para un sitio de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="69de1-105">The **site** resource provides metadata and relationships for a SharePoint site.</span></span>

## <a name="methods"></a><span data-ttu-id="69de1-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="69de1-106">Methods</span></span>

| <span data-ttu-id="69de1-107">Método</span><span class="sxs-lookup"><span data-stu-id="69de1-107">Method</span></span>                         | <span data-ttu-id="69de1-108">Ruta de acceso a REST</span><span class="sxs-lookup"><span data-stu-id="69de1-108">REST Path</span></span>
|:-------------------------------|:--------------------------------------------
| <span data-ttu-id="69de1-109">[Obtener sitio raíz][]</span><span class="sxs-lookup"><span data-stu-id="69de1-109">[Get root site][]</span></span>              | <span data-ttu-id="69de1-110">GET /sites/root</span><span class="sxs-lookup"><span data-stu-id="69de1-110">GET /sites/root</span></span>
| <span data-ttu-id="69de1-111">[Obtener sitio][]</span><span class="sxs-lookup"><span data-stu-id="69de1-111">[Get site][]</span></span>                   | <span data-ttu-id="69de1-112">GET /sites/{site-id}</span><span class="sxs-lookup"><span data-stu-id="69de1-112">GET /sites/{site-id}</span></span>
| <span data-ttu-id="69de1-113">[Obtener sitio por su ruta de acceso][]</span><span class="sxs-lookup"><span data-stu-id="69de1-113">[Get site by path][]</span></span>           | <span data-ttu-id="69de1-114">GET /sites/{hostname}:/{site-path}</span><span class="sxs-lookup"><span data-stu-id="69de1-114">GET /sites/{hostname}:/{site-path}</span></span>
| <span data-ttu-id="69de1-115">[Obtener sitio para un grupo][]</span><span class="sxs-lookup"><span data-stu-id="69de1-115">[Get site for a group][]</span></span>       | <span data-ttu-id="69de1-116">GET /groups/{group-id}/sites/root</span><span class="sxs-lookup"><span data-stu-id="69de1-116">GET /groups/{group-id}/sites/root</span></span>
| <span data-ttu-id="69de1-117">[Obtener análisis][]</span><span class="sxs-lookup"><span data-stu-id="69de1-117">[Get analytics][]</span></span>              | <span data-ttu-id="69de1-118">GET/Sites / {identificador de sitio} / análisis</span><span class="sxs-lookup"><span data-stu-id="69de1-118">GET /sites/{site-id}/analytics</span></span>
| <span data-ttu-id="69de1-119">[Obtener las actividades por intervalo][]</span><span class="sxs-lookup"><span data-stu-id="69de1-119">[Get activities by interval][]</span></span> | <span data-ttu-id="69de1-120">GET/Sites / {identificador de sitio} / getActivitiesByInterval</span><span class="sxs-lookup"><span data-stu-id="69de1-120">GET /sites/{site-id}/getActivitiesByInterval</span></span>
| <span data-ttu-id="69de1-121">[Enumerar páginas][]</span><span class="sxs-lookup"><span data-stu-id="69de1-121">[List pages][]</span></span>                 | <span data-ttu-id="69de1-122">GET/Sites / {identificador de sitio} / páginas</span><span class="sxs-lookup"><span data-stu-id="69de1-122">GET /sites/{site-id}/pages</span></span>
| <span data-ttu-id="69de1-123">[Enumerar los sitios raíz][]</span><span class="sxs-lookup"><span data-stu-id="69de1-123">[List root sites][]</span></span>            | <span data-ttu-id="69de1-124">/ Sites GET? filtro = raíz ne null & select = siteCollection, webUrl</span><span class="sxs-lookup"><span data-stu-id="69de1-124">GET /sites?filter=root ne null&select=siteCollection,webUrl</span></span>
| <span data-ttu-id="69de1-125">[Buscar sitios][]</span><span class="sxs-lookup"><span data-stu-id="69de1-125">[Search for sites][]</span></span>           | <span data-ttu-id="69de1-126">GET /sites?search={query}</span><span class="sxs-lookup"><span data-stu-id="69de1-126">GET /sites?search={query}</span></span>

[Obtener sitio]: ../api/site-get.md
[Get site]: ../api/site-get.md
[Obtener sitio raíz]: ../api/site-get.md
[Get root site]: ../api/site-get.md
[Obtener sitio por su ruta de acceso]: ../api/site-getbypath.md
[Get site by path]: ../api/site-getbypath.md
[Obtener sitio para un grupo]: ../api/site-get.md
[Get site for a group]: ../api/site-get.md
[Obtener análisis]: ../api/itemanalytics-get.md
[Get analytics]: ../api/itemanalytics-get.md
[Obtener las actividades por intervalo]: ../api/itemactivity-getbyinterval.md
[Get activities by interval]: ../api/itemactivity-getbyinterval.md
[Enumerar páginas]: ../api/sitepage-list.md
[List pages]: ../api/sitepage-list.md
[Enumerar los sitios raíz]: ../api/site-list.md
[List root sites]: ../api/site-list.md
[Buscar sitios]: ../api/site-search.md
[Search for sites]: ../api/site-search.md


## <a name="properties"></a><span data-ttu-id="69de1-136">Propiedades</span><span class="sxs-lookup"><span data-stu-id="69de1-136">Properties</span></span>

| <span data-ttu-id="69de1-137">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="69de1-137">Property name</span></span>            | <span data-ttu-id="69de1-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="69de1-138">Type</span></span>               | <span data-ttu-id="69de1-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="69de1-139">Description</span></span>
|:-------------------------|:-------------------|:-----------------------------
| <span data-ttu-id="69de1-140">**id**</span><span class="sxs-lookup"><span data-stu-id="69de1-140">**id**</span></span>                   | <span data-ttu-id="69de1-141">string</span><span class="sxs-lookup"><span data-stu-id="69de1-141">string</span></span>             | <span data-ttu-id="69de1-p102">El identificador único del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="69de1-p102">The unique identifier of the item. Read-only.</span></span>
| <span data-ttu-id="69de1-144">**createdDateTime**</span><span class="sxs-lookup"><span data-stu-id="69de1-144">**createdDateTime**</span></span>      | <span data-ttu-id="69de1-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="69de1-145">DateTimeOffset</span></span>     | <span data-ttu-id="69de1-p103">La fecha y la hora de creación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="69de1-p103">The date and time the item was created. Read-only.</span></span>
| <span data-ttu-id="69de1-148">**description**</span><span class="sxs-lookup"><span data-stu-id="69de1-148">**description**</span></span>          | <span data-ttu-id="69de1-149">string</span><span class="sxs-lookup"><span data-stu-id="69de1-149">string</span></span>             | <span data-ttu-id="69de1-150">Texto descriptivo del sitio.</span><span class="sxs-lookup"><span data-stu-id="69de1-150">The descriptive text for the site.</span></span>
| <span data-ttu-id="69de1-151">**eTag**</span><span class="sxs-lookup"><span data-stu-id="69de1-151">**eTag**</span></span>                 | <span data-ttu-id="69de1-152">string</span><span class="sxs-lookup"><span data-stu-id="69de1-152">string</span></span>             | <span data-ttu-id="69de1-p104">ETag para el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="69de1-p104">ETag for the item. Read-only.</span></span>                                                                  |
| <span data-ttu-id="69de1-155">**displayName**</span><span class="sxs-lookup"><span data-stu-id="69de1-155">**displayName**</span></span>          | <span data-ttu-id="69de1-156">string</span><span class="sxs-lookup"><span data-stu-id="69de1-156">string</span></span>             | <span data-ttu-id="69de1-p105">El título completo del sitio. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="69de1-p105">The full title for the site. Read-only.</span></span>
| <span data-ttu-id="69de1-159">**lastModifiedDateTime**</span><span class="sxs-lookup"><span data-stu-id="69de1-159">**lastModifiedDateTime**</span></span> | <span data-ttu-id="69de1-160">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="69de1-160">DateTimeOffset</span></span>     | <span data-ttu-id="69de1-p106">Fecha y hora de la última modificación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="69de1-p106">The date and time the item was last modified. Read-only.</span></span>
| <span data-ttu-id="69de1-163">**name**</span><span class="sxs-lookup"><span data-stu-id="69de1-163">**name**</span></span>                 | <span data-ttu-id="69de1-164">string</span><span class="sxs-lookup"><span data-stu-id="69de1-164">string</span></span>             | <span data-ttu-id="69de1-165">Nombre o título del elemento.</span><span class="sxs-lookup"><span data-stu-id="69de1-165">The name / title of the item.</span></span>
| <span data-ttu-id="69de1-166">**root**</span><span class="sxs-lookup"><span data-stu-id="69de1-166">**root**</span></span>                 | <span data-ttu-id="69de1-167">[root][]</span><span class="sxs-lookup"><span data-stu-id="69de1-167">[root][]</span></span>           | <span data-ttu-id="69de1-p107">Si está presente, indica que se trata del sitio raíz de la colección de sitios. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="69de1-p107">If present, indicates that this is the root site in the site collection. Read-only.</span></span>
| <span data-ttu-id="69de1-170">**sharepointIds**</span><span class="sxs-lookup"><span data-stu-id="69de1-170">**sharepointIds**</span></span>        | <span data-ttu-id="69de1-171">[sharepointIds][]</span><span class="sxs-lookup"><span data-stu-id="69de1-171">[sharepointIds][]</span></span>  | <span data-ttu-id="69de1-p108">Devuelve los identificadores útiles para la compatibilidad con REST de SharePoint. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="69de1-p108">Returns identifiers useful for SharePoint REST compatibility. Read-only.</span></span>
| <span data-ttu-id="69de1-174">**siteCollection**</span><span class="sxs-lookup"><span data-stu-id="69de1-174">**siteCollection**</span></span>       | <span data-ttu-id="69de1-175">[siteCollection][]</span><span class="sxs-lookup"><span data-stu-id="69de1-175">[siteCollection][]</span></span> | <span data-ttu-id="69de1-p109">Proporciona detalles sobre la colección de sitios del sitio. Solo disponible en el sitio raíz. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="69de1-p109">Provides details about the site's site collection. Available only on the root site. Read-only.</span></span>
| <span data-ttu-id="69de1-179">**webUrl**</span><span class="sxs-lookup"><span data-stu-id="69de1-179">**webUrl**</span></span>               | <span data-ttu-id="69de1-180">string (url)</span><span class="sxs-lookup"><span data-stu-id="69de1-180">string (url)</span></span>       | <span data-ttu-id="69de1-p110">Dirección URL que muestra el elemento en el explorador. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="69de1-p110">URL that displays the item in the browser. Read-only.</span></span>

## <a name="relationships"></a><span data-ttu-id="69de1-183">Relaciones</span><span class="sxs-lookup"><span data-stu-id="69de1-183">Relationships</span></span>

| <span data-ttu-id="69de1-184">Nombre de la relación</span><span class="sxs-lookup"><span data-stu-id="69de1-184">Relationship name</span></span> | <span data-ttu-id="69de1-185">Tipo</span><span class="sxs-lookup"><span data-stu-id="69de1-185">Type</span></span>                             | <span data-ttu-id="69de1-186">Descripción</span><span class="sxs-lookup"><span data-stu-id="69de1-186">Description</span></span>
|:------------------|:---------------------------------|:----------------------
| <span data-ttu-id="69de1-187">**análisis**</span><span class="sxs-lookup"><span data-stu-id="69de1-187">**analytics**</span></span>     | <span data-ttu-id="69de1-188">recursos de [itemAnalytics][]</span><span class="sxs-lookup"><span data-stu-id="69de1-188">[itemAnalytics][] resource</span></span>       | <span data-ttu-id="69de1-189">Análisis acerca de las actividades de vista que tuvieron lugar en este sitio.</span><span class="sxs-lookup"><span data-stu-id="69de1-189">Analytics about the view activities that took place in this site.</span></span>
| <span data-ttu-id="69de1-190">**columns**</span><span class="sxs-lookup"><span data-stu-id="69de1-190">**columns**</span></span>       | <span data-ttu-id="69de1-191">Collection([columnDefinition][])</span><span class="sxs-lookup"><span data-stu-id="69de1-191">Collection([columnDefinition][])</span></span> | <span data-ttu-id="69de1-192">La colección de definiciones de columna reutilizables en listas en este sitio.</span><span class="sxs-lookup"><span data-stu-id="69de1-192">The collection of column definitions reusable across lists under this site.</span></span>
| <span data-ttu-id="69de1-193">**contentTypes**</span><span class="sxs-lookup"><span data-stu-id="69de1-193">**contentTypes**</span></span>  | <span data-ttu-id="69de1-194">Collection([contentType][])</span><span class="sxs-lookup"><span data-stu-id="69de1-194">Collection([contentType][])</span></span>      | <span data-ttu-id="69de1-195">La colección de tipos de contenido definidos para este sitio.</span><span class="sxs-lookup"><span data-stu-id="69de1-195">The collection of content types defined for this site.</span></span>
| <span data-ttu-id="69de1-196">**drive**</span><span class="sxs-lookup"><span data-stu-id="69de1-196">**drive**</span></span>         | <span data-ttu-id="69de1-197">[drive][]</span><span class="sxs-lookup"><span data-stu-id="69de1-197">[drive][]</span></span>                        | <span data-ttu-id="69de1-198">La unidad predeterminada (biblioteca de documentos) para este sitio.</span><span class="sxs-lookup"><span data-stu-id="69de1-198">The default drive (document library) for this site.</span></span>
| <span data-ttu-id="69de1-199">**drives**</span><span class="sxs-lookup"><span data-stu-id="69de1-199">**drives**</span></span>        | <span data-ttu-id="69de1-200">Collection([drive][])</span><span class="sxs-lookup"><span data-stu-id="69de1-200">Collection([drive][])</span></span>            | <span data-ttu-id="69de1-201">La colección de unidades (bibliotecas de documentos) de este sitio.</span><span class="sxs-lookup"><span data-stu-id="69de1-201">The collection of drives (document libraries) under this site.</span></span>
| <span data-ttu-id="69de1-202">**items**</span><span class="sxs-lookup"><span data-stu-id="69de1-202">**items**</span></span>         | <span data-ttu-id="69de1-203">Collection([baseItem][])</span><span class="sxs-lookup"><span data-stu-id="69de1-203">Collection([baseItem][])</span></span>         | <span data-ttu-id="69de1-p111">Se utiliza para resolver cualquier elemento contenido en este sitio. Esta colección no se puede enumerar.</span><span class="sxs-lookup"><span data-stu-id="69de1-p111">Used to address any item contained in this site. This collection cannot be enumerated.</span></span>
| <span data-ttu-id="69de1-206">**lists**</span><span class="sxs-lookup"><span data-stu-id="69de1-206">**lists**</span></span>         | <span data-ttu-id="69de1-207">Collection([list][])</span><span class="sxs-lookup"><span data-stu-id="69de1-207">Collection([list][])</span></span>             | <span data-ttu-id="69de1-208">La colección de listas en este sitio.</span><span class="sxs-lookup"><span data-stu-id="69de1-208">The collection of lists under this site.</span></span>
| <span data-ttu-id="69de1-209">**páginas**</span><span class="sxs-lookup"><span data-stu-id="69de1-209">**pages**</span></span>         | <span data-ttu-id="69de1-210">Colección ([sitePage][])</span><span class="sxs-lookup"><span data-stu-id="69de1-210">Collection([sitePage][])</span></span>         | <span data-ttu-id="69de1-211">La colección de páginas en la lista SitePages en este sitio.</span><span class="sxs-lookup"><span data-stu-id="69de1-211">The collection of pages in the SitePages list in this site.</span></span>
| <span data-ttu-id="69de1-212">**sites**</span><span class="sxs-lookup"><span data-stu-id="69de1-212">**sites**</span></span>         | <span data-ttu-id="69de1-213">Collection([site][])</span><span class="sxs-lookup"><span data-stu-id="69de1-213">Collection([site][])</span></span>             | <span data-ttu-id="69de1-214">La colección de subsitios de este sitio.</span><span class="sxs-lookup"><span data-stu-id="69de1-214">The collection of the sub-sites under this site.</span></span>

[columnDefinition]: columndefinition.md
[baseItem]: baseitem.md
[contentType]: contenttype.md
[drive]: drive.md
[identitySet]: identityset.md
[itemAnalytics]: itemanalytics.md
[list]: list.md
[sitePage]: sitepage.md
[root]: root.md
[site]: site.md
[sharepointIds]: sharepointids.md
[siteCollection]: sitecollection.md

## <a name="json-representation"></a><span data-ttu-id="69de1-226">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="69de1-226">JSON representation</span></span>

<span data-ttu-id="69de1-227">A continuación se incluye una representación JSON del recurso **site**.</span><span class="sxs-lookup"><span data-stu-id="69de1-227">Here is a JSON representation of a **site** resource.</span></span>

<span data-ttu-id="69de1-228">El recurso **site** deriva de [**baseItem**](baseitem.md) y hereda sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="69de1-228">The **site** resource is derived from [**baseItem**](baseitem.md) and inherits properties from that resource.</span></span>

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
  "analytics": { "@odata.type": "microsoft.graph.itemAnalytics" },
  "contentTypes": [ { "@odata.type": "microsoft.graph.contentType" }],
  "drive": { "@odata.type": "microsoft.graph.drive" },
  "drives": [ { "@odata.type": "microsoft.graph.drive" }],
  "items": [ { "@odata.type": "microsoft.graph.baseItem" }],
  "lists": [ { "@odata.type": "microsoft.graph.list" }],
  "sites": [ { "@odata.type": "microsoft.graph.site"} ],
  "columns": [ { "@odata.type": "microsoft.graph.columnDefinition" }],

  /* inherited from baseItem */
  "name": "string",
  "createdDateTime": "datetime",
  "description": "string",
  "eTag": "string",
  "lastModifiedDateTime": "datetime",
  "webUrl": "url"
}
```

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Sites",
  "tocBookmarks": { "Resources/Site": "#" }
} -->
