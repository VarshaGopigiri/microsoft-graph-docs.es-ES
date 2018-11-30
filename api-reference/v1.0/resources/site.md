---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Sitio
ms.openlocfilehash: db465f93f336a51d862daf6e05b1d6bc422247ea
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="site-resource"></a><span data-ttu-id="68ca2-102">Recurso site</span><span class="sxs-lookup"><span data-stu-id="68ca2-102">Site resource</span></span>

<span data-ttu-id="68ca2-103">El recurso **site** proporciona metadatos y relaciones para un sitio de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="68ca2-103">The **site** resource provides metadata and relationships for a SharePoint site.</span></span>

## <a name="tasks"></a><span data-ttu-id="68ca2-104">Tareas</span><span class="sxs-lookup"><span data-stu-id="68ca2-104">Tasks</span></span>

<span data-ttu-id="68ca2-105">Todos los ejemplos siguientes son relativos a `https://graph.microsoft.com/v1.0`.</span><span class="sxs-lookup"><span data-stu-id="68ca2-105">All examples below are relative to `https://graph.microsoft.com/v1.0`.</span></span>

| <span data-ttu-id="68ca2-106">Nombre de tarea</span><span class="sxs-lookup"><span data-stu-id="68ca2-106">Task name</span></span>                | <span data-ttu-id="68ca2-107">Solicitud de ejemplo</span><span class="sxs-lookup"><span data-stu-id="68ca2-107">Example Request</span></span>
|:-------------------------|:--------------------------------------------------
| <span data-ttu-id="68ca2-108">[Obtener sitio raíz][]</span><span class="sxs-lookup"><span data-stu-id="68ca2-108">[Get root site][]</span></span>        | <span data-ttu-id="68ca2-109">GET /sites/root</span><span class="sxs-lookup"><span data-stu-id="68ca2-109">GET /sites/root</span></span>
| <span data-ttu-id="68ca2-110">[Obtener sitio][]</span><span class="sxs-lookup"><span data-stu-id="68ca2-110">[Get site][]</span></span>             | <span data-ttu-id="68ca2-111">GET /sites/{site-id}</span><span class="sxs-lookup"><span data-stu-id="68ca2-111">GET /sites/{site-id}</span></span>
| <span data-ttu-id="68ca2-112">[Obtener sitio por su ruta de acceso][]</span><span class="sxs-lookup"><span data-stu-id="68ca2-112">[Get site by path][]</span></span>     | <span data-ttu-id="68ca2-113">GET /sites/{hostname}:/{site-path}</span><span class="sxs-lookup"><span data-stu-id="68ca2-113">GET /sites/{hostname}:/{site-path}</span></span>
| <span data-ttu-id="68ca2-114">[Obtener sitio para un grupo][]</span><span class="sxs-lookup"><span data-stu-id="68ca2-114">[Get site for a group][]</span></span> | <span data-ttu-id="68ca2-115">GET /groups/{group-id}/sites/root</span><span class="sxs-lookup"><span data-stu-id="68ca2-115">GET /groups/{group-id}/sites/root</span></span>
| <span data-ttu-id="68ca2-116">[Buscar sitios][]</span><span class="sxs-lookup"><span data-stu-id="68ca2-116">[Search for sites][]</span></span>     | <span data-ttu-id="68ca2-117">GET /sites?search={query}</span><span class="sxs-lookup"><span data-stu-id="68ca2-117">GET /sites?search={query}</span></span>

[Obtener sitio]: ../api/site_get.md
[Obtener sitio raíz]: ../api/site_get.md
[Obtener sitio por su ruta de acceso]: ../api/site_getbypath.md
[Obtener sitio para un grupo]: ../api/site_get.md
[Buscar sitios]: ../api/site_search.md

## <a name="json-representation"></a><span data-ttu-id="68ca2-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="68ca2-123">JSON representation</span></span>

<span data-ttu-id="68ca2-124">A continuación se incluye una representación JSON del recurso **site**.</span><span class="sxs-lookup"><span data-stu-id="68ca2-124">Here is a JSON representation of a **site** resource.</span></span>

<span data-ttu-id="68ca2-125">El recurso **driveItem** deriva de [**baseItem**](baseitem.md) y hereda las propiedades de ese recurso.</span><span class="sxs-lookup"><span data-stu-id="68ca2-125">The **driveItem** resource is derived from [**baseItem**](baseitem.md) and inherits properties from that resource.</span></span>

<!-- { "blockType": "resource",
       "@odata.type": "microsoft.graph.site",
       "keyProperty": "id",
       "optionalProperties": [ "root", "sharepointIds", "siteCollection", "drive", "drives", "sites" ] } -->

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
  "onenote": [ { "@odata.type": "microsoft.graph.onenote"} ],

  /* inherited from baseItem */
  "name": "string",
  "createdDateTime": "datetime",
  "description": "string",
  "eTag": "string",
  "lastModifiedDateTime": "datetime",
  "webUrl": "url"
}
```

## <a name="properties"></a><span data-ttu-id="68ca2-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="68ca2-126">Properties</span></span>

| <span data-ttu-id="68ca2-127">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="68ca2-127">Property name</span></span>            | <span data-ttu-id="68ca2-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="68ca2-128">Type</span></span>                                | <span data-ttu-id="68ca2-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="68ca2-129">Description</span></span>                                                                                    |
| :----------------------- | :---------------------------------- | :--------------------------------------------------------------------------------------------- |
| <span data-ttu-id="68ca2-130">**id**</span><span class="sxs-lookup"><span data-stu-id="68ca2-130">**id**</span></span>                   | <span data-ttu-id="68ca2-131">string</span><span class="sxs-lookup"><span data-stu-id="68ca2-131">string</span></span>                              | <span data-ttu-id="68ca2-p101">El identificador único del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="68ca2-p101">The unique identifier of the item. Read-only.</span></span>                                                  |
| <span data-ttu-id="68ca2-134">**createdDateTime**</span><span class="sxs-lookup"><span data-stu-id="68ca2-134">**createdDateTime**</span></span>      | <span data-ttu-id="68ca2-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="68ca2-135">DateTimeOffset</span></span>                      | <span data-ttu-id="68ca2-p102">La fecha y la hora de creación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="68ca2-p102">The date and time the item was created. Read-only.</span></span>                                             |
| <span data-ttu-id="68ca2-138">**description**</span><span class="sxs-lookup"><span data-stu-id="68ca2-138">**description**</span></span>          | <span data-ttu-id="68ca2-139">string</span><span class="sxs-lookup"><span data-stu-id="68ca2-139">string</span></span>                              | <span data-ttu-id="68ca2-140">Texto descriptivo del sitio.</span><span class="sxs-lookup"><span data-stu-id="68ca2-140">The descriptive text for the site.</span></span>                                                             |
| <span data-ttu-id="68ca2-141">**displayName**</span><span class="sxs-lookup"><span data-stu-id="68ca2-141">**displayName**</span></span>          | <span data-ttu-id="68ca2-142">string</span><span class="sxs-lookup"><span data-stu-id="68ca2-142">string</span></span>                              | <span data-ttu-id="68ca2-p103">El título completo del sitio. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="68ca2-p103">The full title for the site. Read-only.</span></span>                                                        |
| <span data-ttu-id="68ca2-145">**lastModifiedDateTime**</span><span class="sxs-lookup"><span data-stu-id="68ca2-145">**lastModifiedDateTime**</span></span> | <span data-ttu-id="68ca2-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="68ca2-146">DateTimeOffset</span></span>                      | <span data-ttu-id="68ca2-p104">Fecha y hora de la última modificación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="68ca2-p104">The date and time the item was last modified. Read-only.</span></span>                                       |
| <span data-ttu-id="68ca2-149">**name**</span><span class="sxs-lookup"><span data-stu-id="68ca2-149">**name**</span></span>                 | <span data-ttu-id="68ca2-150">string</span><span class="sxs-lookup"><span data-stu-id="68ca2-150">string</span></span>                              | <span data-ttu-id="68ca2-151">Nombre o título del elemento.</span><span class="sxs-lookup"><span data-stu-id="68ca2-151">The name / title of the item.</span></span>                                                                  |
| <span data-ttu-id="68ca2-152">**root**</span><span class="sxs-lookup"><span data-stu-id="68ca2-152">**root**</span></span>                 | [<span data-ttu-id="68ca2-153">root</span><span class="sxs-lookup"><span data-stu-id="68ca2-153">root</span></span>](root.md)                     | <span data-ttu-id="68ca2-p105">Si está presente, indica que se trata del sitio raíz de la colección de sitios. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="68ca2-p105">If present, indicates that this is the root site in the site collection. Read-only.</span></span>            |
| <span data-ttu-id="68ca2-156">**sharepointIds**</span><span class="sxs-lookup"><span data-stu-id="68ca2-156">**sharepointIds**</span></span>        | [<span data-ttu-id="68ca2-157">sharepointIds</span><span class="sxs-lookup"><span data-stu-id="68ca2-157">sharepointIds</span></span>](sharepointids.md)   | <span data-ttu-id="68ca2-p106">Devuelve los identificadores útiles para la compatibilidad con REST de SharePoint. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="68ca2-p106">Returns identifiers useful for SharePoint REST compatibility. Read-only.</span></span>                       |
| <span data-ttu-id="68ca2-160">**siteCollection**</span><span class="sxs-lookup"><span data-stu-id="68ca2-160">**siteCollection**</span></span>       | [<span data-ttu-id="68ca2-161">siteCollection</span><span class="sxs-lookup"><span data-stu-id="68ca2-161">siteCollection</span></span>](sitecollection.md) | <span data-ttu-id="68ca2-p107">Proporciona detalles sobre la colección de sitios del sitio. Solo disponible en el sitio raíz. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="68ca2-p107">Provides details about the site's site collection. Available only on the root site. Read-only.</span></span> |
| <span data-ttu-id="68ca2-165">**webUrl**</span><span class="sxs-lookup"><span data-stu-id="68ca2-165">**webUrl**</span></span>               | <span data-ttu-id="68ca2-166">string (url)</span><span class="sxs-lookup"><span data-stu-id="68ca2-166">string (url)</span></span>                        | <span data-ttu-id="68ca2-p108">Dirección URL que muestra el elemento en el explorador. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="68ca2-p108">URL that displays the item in the browser. Read-only.</span></span>                                          |

## <a name="relationships"></a><span data-ttu-id="68ca2-169">Relaciones</span><span class="sxs-lookup"><span data-stu-id="68ca2-169">Relationships</span></span>

| <span data-ttu-id="68ca2-170">Nombre de la relación</span><span class="sxs-lookup"><span data-stu-id="68ca2-170">Relationship name</span></span> | <span data-ttu-id="68ca2-171">Tipo</span><span class="sxs-lookup"><span data-stu-id="68ca2-171">Type</span></span>                             | <span data-ttu-id="68ca2-172">Descripción</span><span class="sxs-lookup"><span data-stu-id="68ca2-172">Description</span></span>
|:------------------|:---------------------------------|:----------------------
| <span data-ttu-id="68ca2-173">**columns**</span><span class="sxs-lookup"><span data-stu-id="68ca2-173">**columns**</span></span>       | <span data-ttu-id="68ca2-174">Collection([columnDefinition][])</span><span class="sxs-lookup"><span data-stu-id="68ca2-174">Collection([columnDefinition][])</span></span> | <span data-ttu-id="68ca2-175">La colección de definiciones de columna reutilizables en listas en este sitio.</span><span class="sxs-lookup"><span data-stu-id="68ca2-175">The collection of column definitions reusable across lists under this site.</span></span>
| <span data-ttu-id="68ca2-176">**contentTypes**</span><span class="sxs-lookup"><span data-stu-id="68ca2-176"><ContentTypes></span></span>  | <span data-ttu-id="68ca2-177">Collection([contentType][])</span><span class="sxs-lookup"><span data-stu-id="68ca2-177">Collection([contentType][])</span></span>      | <span data-ttu-id="68ca2-178">La colección de tipos de contenido definidos para este sitio.</span><span class="sxs-lookup"><span data-stu-id="68ca2-178">The collection of content types defined for this site.</span></span>
| <span data-ttu-id="68ca2-179">**drive**</span><span class="sxs-lookup"><span data-stu-id="68ca2-179">**drive**</span></span>         | <span data-ttu-id="68ca2-180">[drive][]</span><span class="sxs-lookup"><span data-stu-id="68ca2-180">[drive][]</span></span>                        | <span data-ttu-id="68ca2-181">La unidad predeterminada (biblioteca de documentos) para este sitio.</span><span class="sxs-lookup"><span data-stu-id="68ca2-181">The default drive (document library) for this site.</span></span>
| <span data-ttu-id="68ca2-182">**drives**</span><span class="sxs-lookup"><span data-stu-id="68ca2-182">**drives**</span></span>        | <span data-ttu-id="68ca2-183">Collection([drive][])</span><span class="sxs-lookup"><span data-stu-id="68ca2-183">Collection([drive][])</span></span>            | <span data-ttu-id="68ca2-184">La colección de unidades (bibliotecas de documentos) de este sitio.</span><span class="sxs-lookup"><span data-stu-id="68ca2-184">The collection of drives (document libraries) under this site.</span></span>
| <span data-ttu-id="68ca2-185">**items**</span><span class="sxs-lookup"><span data-stu-id="68ca2-185">**items**</span></span>         | <span data-ttu-id="68ca2-186">Collection([baseItem][])</span><span class="sxs-lookup"><span data-stu-id="68ca2-186">Collection([baseItem][])</span></span>         | <span data-ttu-id="68ca2-p109">Se utiliza para resolver cualquier elemento contenido en este sitio. Esta colección no se puede enumerar.</span><span class="sxs-lookup"><span data-stu-id="68ca2-p109">Used to address any item contained in this site. This collection cannot be enumerated.</span></span>
| <span data-ttu-id="68ca2-189">**lists**</span><span class="sxs-lookup"><span data-stu-id="68ca2-189">**Lists**</span></span>         | <span data-ttu-id="68ca2-190">Collection([list][])</span><span class="sxs-lookup"><span data-stu-id="68ca2-190">Collection([list][])</span></span>             | <span data-ttu-id="68ca2-191">La colección de listas en este sitio.</span><span class="sxs-lookup"><span data-stu-id="68ca2-191">The collection of the sub-sites under this site.</span></span>
| <span data-ttu-id="68ca2-192">**sites**</span><span class="sxs-lookup"><span data-stu-id="68ca2-192">**sites**</span></span>         | <span data-ttu-id="68ca2-193">Collection([site][])</span><span class="sxs-lookup"><span data-stu-id="68ca2-193">Collection([site][])</span></span>             | <span data-ttu-id="68ca2-194">La colección de subsitios de este sitio.</span><span class="sxs-lookup"><span data-stu-id="68ca2-194">The collection of the sub-sites under this site.</span></span>
| <span data-ttu-id="68ca2-195">**onenote**</span><span class="sxs-lookup"><span data-stu-id="68ca2-195">**onenote**</span></span>       | <span data-ttu-id="68ca2-196">[onenote][]</span><span class="sxs-lookup"><span data-stu-id="68ca2-196">[onenote][]</span></span>                      | <span data-ttu-id="68ca2-197">Realiza una llamada al servicio de OneNote para operaciones relacionadas con blocs de notas.</span><span class="sxs-lookup"><span data-stu-id="68ca2-197">Calls the OneNote service for notebook related operations.</span></span>

[columnDefinition]: columndefinition.md
[baseItem]: baseitem.md
[contentType]: contentType.md
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
