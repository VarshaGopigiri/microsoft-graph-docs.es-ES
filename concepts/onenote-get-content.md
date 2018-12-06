---
title: Obtener el contenido y la estructura de OneNote con Microsoft Graph
description: " Blocs de notas de empresa en Office 365"
ms.openlocfilehash: d5a1b382535988e48b5b710d3685a344c5f5a40d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092909"
---
# <a name="get-onenote-content-and-structure-with-microsoft-graph"></a><span data-ttu-id="f9a22-103">Obtener el contenido y la estructura de OneNote con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="f9a22-103">Get OneNote content and structure with Microsoft Graph</span></span>

<span data-ttu-id="f9a22-104">**Se aplica a**: Blocs de notas para consumidores de OneDrive | Blocs de notas empresariales de Office 365</span><span class="sxs-lookup"><span data-stu-id="f9a22-104">**Applies to**: Consumer notebooks on OneDrive | Enterprise notebooks on Office 365</span></span>

<span data-ttu-id="f9a22-105">Para obtener la estructura y el contenido de OneNote, envíe una solicitud GET al extremo de destino.</span><span class="sxs-lookup"><span data-stu-id="f9a22-105">To get OneNote content and structure, you send a GET request to the target endpoint.</span></span> <span data-ttu-id="f9a22-106">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="f9a22-106">For example:</span></span>

`GET ../onenote/pages/{id}`

<span data-ttu-id="f9a22-107">Si la solicitud es correcta, Microsoft Graph devuelve un código de estado HTTP 200 y las entidades o el contenido que ha solicitado.</span><span class="sxs-lookup"><span data-stu-id="f9a22-107">If the request is successful, Microsoft Graph returns a 200 HTTP status code and the entities or content that you requested.</span></span> <span data-ttu-id="f9a22-108">Las entidades de OneNote se devuelven como objetos JSON que cumplen la especificación de la versión 4.0 de OData.</span><span class="sxs-lookup"><span data-stu-id="f9a22-108">OneNote entities are returned as JSON objects that conform to the OData version 4.0 specification.</span></span>

<span data-ttu-id="f9a22-109">Puede filtrar las consultas y mejorar el rendimiento usando las opciones de la cadena de consulta.</span><span class="sxs-lookup"><span data-stu-id="f9a22-109">By using query string options, you can filter your queries and improve performance.</span></span>


<a name="request-uri"></a>

## <a name="construct-the-request-uri"></a><span data-ttu-id="f9a22-110">Crear el URI de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f9a22-110">Construct the request URI</span></span>

<span data-ttu-id="f9a22-111">Para crear el URI de la solicitud, comience con la dirección URL raíz del servicio:</span><span class="sxs-lookup"><span data-stu-id="f9a22-111">To construct the request URI, start with the service root URL:</span></span>

`https://graph.microsoft.com/v1.0/me/onenote`

<br/>

<span data-ttu-id="f9a22-112">Después, anexe el extremo del recurso que desea recuperar.</span><span class="sxs-lookup"><span data-stu-id="f9a22-112">Then append the endpoint of the resource you want to retrieve.</span></span> <span data-ttu-id="f9a22-113">([Las rutas de acceso de recursos](#resource-paths-for-get-requests) se muestran en la siguiente sección).</span><span class="sxs-lookup"><span data-stu-id="f9a22-113">([Resource paths](#resource-paths-for-get-requests) are shown in the next section.)</span></span>

<span data-ttu-id="f9a22-114">Su URI de solicitud completa tendrá un aspecto similar a uno de estos ejemplos:</span><span class="sxs-lookup"><span data-stu-id="f9a22-114">Your full request URI will look like one of these examples:</span></span>

- `https://graph.microsoft.com/v1.0/me/onenote/notebooks/{id}/sections`
- `https://graph.microsoft.com/v1.0/me/onenote/notes/pages`
- `https://graph.microsoft.com/v1.0/me/onenote/pages?select=title,self`

> <span data-ttu-id="f9a22-115">**Nota:** Obtenga más información sobre la [URL de raíz del servicio](/graph/api/resources/onenote-api-overview?view=graph-rest-1.0#root-url).</span><span class="sxs-lookup"><span data-stu-id="f9a22-115">**Note:** Learn more about the [service root URL](/graph/api/resources/onenote-api-overview?view=graph-rest-1.0#root-url).</span></span>

<a name="resource-paths"></a>

## <a name="resource-paths-for-get-requests"></a><span data-ttu-id="f9a22-116">Rutas de acceso de recursos para las solicitudes GET</span><span class="sxs-lookup"><span data-stu-id="f9a22-116">Resource paths for GET requests</span></span>

<span data-ttu-id="f9a22-117">Use las siguientes rutas de acceso de recursos para obtener páginas, secciones, grupos de secciones, blocs de notas, imágenes u otros recursos de archivos.</span><span class="sxs-lookup"><span data-stu-id="f9a22-117">Use the following resource paths to get pages, sections, section groups, notebooks, and image or file resources.</span></span>

- [<span data-ttu-id="f9a22-118">Colección de páginas</span><span class="sxs-lookup"><span data-stu-id="f9a22-118">Page collection</span></span>](#page-collection)
- [<span data-ttu-id="f9a22-119">Entidad de página</span><span class="sxs-lookup"><span data-stu-id="f9a22-119">Page entity</span></span>](#page-entity)
- [<span data-ttu-id="f9a22-120">Vista previa de la página</span><span class="sxs-lookup"><span data-stu-id="f9a22-120">Page preview</span></span>](#page-preview)
- [<span data-ttu-id="f9a22-121">Contenido HTML de la página</span><span class="sxs-lookup"><span data-stu-id="f9a22-121">Page HTML content</span></span>](#page-html-content)
- [<span data-ttu-id="f9a22-122">Colección de sección</span><span class="sxs-lookup"><span data-stu-id="f9a22-122">Section collection</span></span>](#section-collection)
- [<span data-ttu-id="f9a22-123">Entidad de sección</span><span class="sxs-lookup"><span data-stu-id="f9a22-123">Section entity</span></span>](#section-entity)
- [<span data-ttu-id="f9a22-124">Colección de SectionGroup</span><span class="sxs-lookup"><span data-stu-id="f9a22-124">SectionGroup collection</span></span>](#sectiongroup-collection)
- [<span data-ttu-id="f9a22-125">Entidad de SectionGroup</span><span class="sxs-lookup"><span data-stu-id="f9a22-125">SectionGroup entity</span></span>](#sectiongroup-entity)
- [<span data-ttu-id="f9a22-126">Colección de blocs de notas</span><span class="sxs-lookup"><span data-stu-id="f9a22-126">Notebook collection</span></span>](#notebook-collection)
- [<span data-ttu-id="f9a22-127">Entidad de bloc de notas</span><span class="sxs-lookup"><span data-stu-id="f9a22-127">Notebook entity</span></span>](#notebook-entity)
- [<span data-ttu-id="f9a22-128">Imágenes u otros recursos de archivo</span><span class="sxs-lookup"><span data-stu-id="f9a22-128">Image or other file resource</span></span>](#image-or-other-file-resource)

<a name="get-pages"></a>

### <a name="page-collection"></a><span data-ttu-id="f9a22-129">Colección de páginas</span><span class="sxs-lookup"><span data-stu-id="f9a22-129">Page collection</span></span>

<span data-ttu-id="f9a22-130">Obtenga páginas (metadatos) en todos los blocs de notas.</span><span class="sxs-lookup"><span data-stu-id="f9a22-130">Get pages (metadata) across all notebooks.</span></span>

`../pages[?filter,orderby,select,expand,top,skip,search,count]`

<br/>

<span data-ttu-id="f9a22-131">Obtenga páginas (metadatos) de una sección específica.</span><span class="sxs-lookup"><span data-stu-id="f9a22-131">Get pages (metadata) from a specific section.</span></span>

`../sections/{section-id}/pages[?filter,orderby,select,expand,top,skip,search,count,pagelevel]`

<br/>
 
<span data-ttu-id="f9a22-132">La opción de cadena de consulta `search` solo está disponible para los blocs de notas de clientes.</span><span class="sxs-lookup"><span data-stu-id="f9a22-132">The `search` query string option is available for consumer notebooks only.</span></span>

<span data-ttu-id="f9a22-133">El criterio de ordenación predeterminado para páginas es `lastModifiedTime desc`.</span><span class="sxs-lookup"><span data-stu-id="f9a22-133">The default sort order for pages is `lastModifiedTime desc`.</span></span>

<span data-ttu-id="f9a22-134">La consulta predeterminada expande la sección principal y selecciona y selecciona las propiedades `id`, `name` y `self` de la sección.</span><span class="sxs-lookup"><span data-stu-id="f9a22-134">The default query expands the parent section and selects the section's `id`, `name`, and `self` properties.</span></span>

<span data-ttu-id="f9a22-135">De forma predeterminada, solo se devuelven las 20 entradas principales para las solicitudes *GET pages*.</span><span class="sxs-lookup"><span data-stu-id="f9a22-135">By default, only the top 20 entries are returned for *GET pages* requests.</span></span> <span data-ttu-id="f9a22-136">Las solicitudes que no se especifican una opción de cadena de consulta **superior** devuelven un vínculo `@odata.nextLink` en la respuesta que puede usar para obtener las siguientes 20 entradas.</span><span class="sxs-lookup"><span data-stu-id="f9a22-136">Requests that don't specify a **top** query string option return an `@odata.nextLink` link in the response that you can use to get the next 20 entries.</span></span>

<span data-ttu-id="f9a22-137">Para la colección de páginas de una sección, use **pagelevel** para obtener el nivel de sangría de las páginas y su orden en la sección.</span><span class="sxs-lookup"><span data-stu-id="f9a22-137">For the pages collection in a section, use **pagelevel** to return the indentation level of pages and their order within the section.</span></span> 

#### <a name="example"></a><span data-ttu-id="f9a22-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f9a22-138">Example</span></span>

`GET ../sections/{section-id}/pages?pagelevel=true`



<a name="get-page"></a> 

### <a name="page-entity"></a><span data-ttu-id="f9a22-139">Entidad de página</span><span class="sxs-lookup"><span data-stu-id="f9a22-139">Page entity</span></span>

<span data-ttu-id="f9a22-140">Obtenga los metadatos de una página específica.</span><span class="sxs-lookup"><span data-stu-id="f9a22-140">Get the metadata for a specific page.</span></span> 

`../pages/{page-id}[?select,expand,pagelevel]` 

<br/>

<span data-ttu-id="f9a22-141">Las páginas pueden expandir las propiedades **parentNotebook** y **parentSection**.</span><span class="sxs-lookup"><span data-stu-id="f9a22-141">Pages can expand the **parentNotebook** and **parentSection** properties.</span></span>

<span data-ttu-id="f9a22-142">La consulta predeterminada expande la sección principal y selecciona y selecciona las propiedades `id`, `name` y `self` de la sección.</span><span class="sxs-lookup"><span data-stu-id="f9a22-142">The default query expands the parent section and selects the section's `id`, `name`, and `self` properties.</span></span>

<span data-ttu-id="f9a22-143">Use **pagelevel** para obtener el nivel de sangría de la página y su orden en la sección principal.</span><span class="sxs-lookup"><span data-stu-id="f9a22-143">Use **pagelevel** to return the indentation level of the page and its order within its parent section.</span></span> 

#### <a name="example"></a><span data-ttu-id="f9a22-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f9a22-144">Example</span></span>

`GET ../pages/{page-id}?pagelevel=true`



<a name="get-page-preview"></a> 

### <a name="page-preview"></a><span data-ttu-id="f9a22-145">Vista previa de la página</span><span class="sxs-lookup"><span data-stu-id="f9a22-145">Page preview</span></span>

<span data-ttu-id="f9a22-146">Obtenga el contenido de vista previa de texto e imágenes de una página.</span><span class="sxs-lookup"><span data-stu-id="f9a22-146">Get text and image preview content for a page.</span></span>

`../pages/{page-id}/preview`

<br/>


<span data-ttu-id="f9a22-147">La respuesta JSON contiene el contenido de la vista previa, que puede usar para ayudar a los usuarios a identificar los elementos en la página.</span><span class="sxs-lookup"><span data-stu-id="f9a22-147">The JSON response contains the preview content, which you can use to help users identify what's in the page.</span></span>

```json
{
  "@odata.context":"https://www.onenote.com/api/v1.0/$metadata#Microsoft.OneNote.Api.PagePreview",
  "previewText":"text-snippet",
  "links":{
    "previewImageUrl":{
      "href":"https://www.onenote.com/api/v1.0/resources/{id}/content?publicAuth=true&mimeType=image/png"
    }
  }
}
```

<span data-ttu-id="f9a22-148">La propiedad **previewText** contiene un fragmento de texto de la página.</span><span class="sxs-lookup"><span data-stu-id="f9a22-148">The **previewText** property contains a text snippet from the page.</span></span> <span data-ttu-id="f9a22-149">Microsoft Graph devuelve frases completas, hasta un máximo de 300 caracteres.</span><span class="sxs-lookup"><span data-stu-id="f9a22-149">Microsoft Graph returns complete phrases, up to a maximum of 300 characters.</span></span> 

<span data-ttu-id="f9a22-150">Si la página tiene una imagen que puede usarse para crear una vista previa de la interfaz de usuario, la propiedad **href** en el objeto **previewImageUrl** contiene un vínculo a un [recurso de imagen](#image-or-other-file-resource) público que ya se ha autenticado.</span><span class="sxs-lookup"><span data-stu-id="f9a22-150">If the page has an image that can be used to build a preview UI, the **href** property in the **previewImageUrl** object contains a link to a public, pre-authenticated [image resource](#image-or-other-file-resource).</span></span> <span data-ttu-id="f9a22-151">Puede usar este vínculo en HTML.</span><span class="sxs-lookup"><span data-stu-id="f9a22-151">You can use this link in HTML.</span></span> <span data-ttu-id="f9a22-152">En caso contrario, **href** devuelve un valor nulo.</span><span class="sxs-lookup"><span data-stu-id="f9a22-152">Otherwise, **href** returns null.</span></span>

#### <a name="example"></a><span data-ttu-id="f9a22-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f9a22-153">Example</span></span> 

`<img src="https://www.onenote.com/api/v1.0/resources/{id}/content?publicAuth=true&mimeType=image/png" />`


<a name="get-page-content"></a> 

### <a name="page-html-content"></a><span data-ttu-id="f9a22-154">Contenido HTML de la página</span><span class="sxs-lookup"><span data-stu-id="f9a22-154">Page HTML content</span></span>

<span data-ttu-id="f9a22-155">Obtenga el contenido HTML de una página.</span><span class="sxs-lookup"><span data-stu-id="f9a22-155">Get the HTML content of a page.</span></span>

`../pages/{page-id}/content[?includeIDs,preAuthenticated]`

<span data-ttu-id="f9a22-156">(*obtenga más información sobre [ contenido HTML devuelto](onenote-input-output-html.md)*)</span><span class="sxs-lookup"><span data-stu-id="f9a22-156">(*learn more about [returned HTML content](onenote-input-output-html.md)*)</span></span> 

<br/>

<span data-ttu-id="f9a22-157">Use la opción de cadena de consulta **includeIDs=true** para obtener ID generadas que se usan para [actualizar la página](onenote-update-page.md).</span><span class="sxs-lookup"><span data-stu-id="f9a22-157">Use the **includeIDs=true** query string option to get generated IDs used to [update the page](onenote-update-page.md).</span></span>

<span data-ttu-id="f9a22-158">Use la opción de cadena de consulta **preAuthenticated=true** para obtener las direcciones URL públicas para los [recursos de imagen](#image-or-other-file-resource) que están en la página.</span><span class="sxs-lookup"><span data-stu-id="f9a22-158">Use the **preAuthenticated=true** query string option to get public URLs to the [image resources](#image-or-other-file-resource) that are on the page.</span></span> <span data-ttu-id="f9a22-159">Las direcciones URL públicas son válidas durante una hora.</span><span class="sxs-lookup"><span data-stu-id="f9a22-159">The public URLs are valid for one hour.</span></span> 



<a name="get-sections"></a>

### <a name="section-collection"></a><span data-ttu-id="f9a22-160">Colección de sección</span><span class="sxs-lookup"><span data-stu-id="f9a22-160">Section collection</span></span>

<span data-ttu-id="f9a22-161">Obtenga todas las secciones de todos los blocs de notas que posee el usuario, incluyendo las secciones en grupos de secciones anidados.</span><span class="sxs-lookup"><span data-stu-id="f9a22-161">Get all sections from all notebooks that are owned by the user, including sections in nested section groups.</span></span>

`../sections[?filter,orderby,select,top,skip,expand,count]` 

<br/>

<span data-ttu-id="f9a22-162">Obtenga todas las secciones que están directamente en un grupo de secciones específico.</span><span class="sxs-lookup"><span data-stu-id="f9a22-162">Get all sections that are directly under a specific section group.</span></span>

`../sectionGroups/{sectiongroup-id}/sections[?filter,orderby,select,top,skip,expand,count]` 

<br/>

<span data-ttu-id="f9a22-163">Obtenga todas las secciones que están directamente en un bloc de notas específico.</span><span class="sxs-lookup"><span data-stu-id="f9a22-163">Get all sections that are directly under a specific notebook.</span></span>

`../notebooks/{notebook-id}/sections[?filter,orderby,select,top,skip,expand,count]` 

<br/>

<span data-ttu-id="f9a22-164">Las secciones pueden expandir las propiedades **parentNotebook** y **parentSectionGroup**.</span><span class="sxs-lookup"><span data-stu-id="f9a22-164">Sections can expand the **parentNotebook** and **parentSectionGroup** properties.</span></span>

<span data-ttu-id="f9a22-165">El criterio de ordenación predeterminado para secciones es `name asc`.</span><span class="sxs-lookup"><span data-stu-id="f9a22-165">The default sort order for sections is `name asc`.</span></span>

<span data-ttu-id="f9a22-166">La consulta predeterminada expande el bloc de notas principal y el grupo de secciones principal y selecciona y selecciona sus propiedades `id`, `name` y `self`.</span><span class="sxs-lookup"><span data-stu-id="f9a22-166">The default query expands the parent notebook and parent section group and selects their `id`, `name`, and `self` properties.</span></span>



<a name="get-section"></a>

### <a name="section-entity"></a><span data-ttu-id="f9a22-167">Entidad de sección</span><span class="sxs-lookup"><span data-stu-id="f9a22-167">Section entity</span></span>

<span data-ttu-id="f9a22-168">Obtenga una sección específica.</span><span class="sxs-lookup"><span data-stu-id="f9a22-168">Get a specific section.</span></span>

`../sections/{section-id}[?select,expand]` 

<br/>

<span data-ttu-id="f9a22-169">Las secciones pueden expandir las propiedades **parentNotebook** y **parentSectionGroup**.</span><span class="sxs-lookup"><span data-stu-id="f9a22-169">Sections can expand the **parentNotebook** and **parentSectionGroup** properties.</span></span>

<span data-ttu-id="f9a22-170">La consulta predeterminada expande el bloc de notas principal y el grupo de secciones principal y selecciona y selecciona sus propiedades `id`, `name` y `self`.</span><span class="sxs-lookup"><span data-stu-id="f9a22-170">The default query expands the parent notebook and parent section group and selects their `id`, `name`, and `self` properties.</span></span>



<a name="get-section-groups"></a>

### <a name="sectiongroup-collection"></a><span data-ttu-id="f9a22-171">Colección de SectionGroup</span><span class="sxs-lookup"><span data-stu-id="f9a22-171">SectionGroup collection</span></span>

<span data-ttu-id="f9a22-172">Obtenga todos los grupos de secciones de todos los blocs de notas que posee el usuario, incluyendo los grupos de secciones anidados.</span><span class="sxs-lookup"><span data-stu-id="f9a22-172">Get all section groups from all notebooks that are owned by the user, including nested section groups.</span></span>

`../sectionGroups[?filter,orderby,select,top,skip,expand,count]` 

<br/>

<span data-ttu-id="f9a22-173">Obtenga todos los grupos de secciones que están directamente en un bloc de notas específico.</span><span class="sxs-lookup"><span data-stu-id="f9a22-173">Get all section groups that are directly under a specific notebook.</span></span> 

`../notebooks/{notebook-id}/sectionGroups[?filter,orderby,select,top,skip,expand,count]` 

<br/>

<span data-ttu-id="f9a22-174">Los grupos de secciones pueden expandir las propiedades **sections**, **sectionGroups**, **parentNotebook** y **parentSectionGroup**.</span><span class="sxs-lookup"><span data-stu-id="f9a22-174">Section groups can expand the **sections**, **sectionGroups**, **parentNotebook**, and **parentSectionGroup** properties.</span></span>

<span data-ttu-id="f9a22-175">El criterio de ordenación predeterminado para grupos de secciones es `name asc`.</span><span class="sxs-lookup"><span data-stu-id="f9a22-175">The default sort order for section groups is `name asc`.</span></span>

<span data-ttu-id="f9a22-176">La consulta predeterminada expande el bloc de notas principal y el grupo de secciones principal y selecciona y selecciona sus propiedades `id`, `name` y `self`.</span><span class="sxs-lookup"><span data-stu-id="f9a22-176">The default query expands the parent notebook and parent section group and selects their `id`, `name`, and `self` properties.</span></span>



<a name="get-section-group"></a>

### <a name="sectiongroup-entity"></a><span data-ttu-id="f9a22-177">Entidad de SectionGroup</span><span class="sxs-lookup"><span data-stu-id="f9a22-177">SectionGroup entity</span></span>

<span data-ttu-id="f9a22-178">Obtenga un grupo de secciones específico.</span><span class="sxs-lookup"><span data-stu-id="f9a22-178">Get a specific section group.</span></span>

`../sectionGroups/{sectiongroup-id}[?select,expand]` 

<br/>

<span data-ttu-id="f9a22-179">Los grupos de secciones pueden expandir las propiedades **sections**, **sectionGroups**, **parentNotebook** y **parentSectionGroup**.</span><span class="sxs-lookup"><span data-stu-id="f9a22-179">Section groups can expand the **sections**, **sectionGroups**, **parentNotebook**, and **parentSectionGroup** properties.</span></span>

<span data-ttu-id="f9a22-180">La consulta predeterminada expande el bloc de notas principal y el grupo de secciones principal y selecciona y selecciona sus propiedades `id`, `name` y `self`.</span><span class="sxs-lookup"><span data-stu-id="f9a22-180">The default query expands the parent notebook and parent section group and selects their `id`, `name`, and `self` properties.</span></span>



<a name="get-notebooks"></a>

### <a name="notebook-collection"></a><span data-ttu-id="f9a22-181">Colección de blocs de notas</span><span class="sxs-lookup"><span data-stu-id="f9a22-181">Notebook collection</span></span>

<span data-ttu-id="f9a22-182">Obtenga todos los blocs de notas que posee el usuario.</span><span class="sxs-lookup"><span data-stu-id="f9a22-182">Get all the notebooks that are owned by the user.</span></span> 

`../notebooks[?filter,orderby,select,top,skip,expand,count]` 

<br/>

<span data-ttu-id="f9a22-183">Los blocs de notas pueden expandir las propiedades **sections** y **sectionGroups**.</span><span class="sxs-lookup"><span data-stu-id="f9a22-183">Notebooks can expand the **sections** and **sectionGroups** properties.</span></span>

<span data-ttu-id="f9a22-184">El criterio de ordenación predeterminado para blocs de notas es `name asc`.</span><span class="sxs-lookup"><span data-stu-id="f9a22-184">The default sort order for notebooks is `name asc`.</span></span> 



<a name="get-notebook"></a>

### <a name="notebook-entity"></a><span data-ttu-id="f9a22-185">Entidad de bloc de notas</span><span class="sxs-lookup"><span data-stu-id="f9a22-185">Notebook entity</span></span>

<span data-ttu-id="f9a22-186">Obtenga un bloc de notas específico.</span><span class="sxs-lookup"><span data-stu-id="f9a22-186">Get a specific notebook.</span></span>

`../notebooks/{notebook-id}[?select,expand]` 

<br/>

<span data-ttu-id="f9a22-187">Los blocs de notas pueden expandir las propiedades **sections** y **sectionGroups**.</span><span class="sxs-lookup"><span data-stu-id="f9a22-187">Notebooks can expand the **sections** and **sectionGroups** properties.</span></span>



<a name="get-resource"></a>

### <a name="image-or-other-file-resource"></a><span data-ttu-id="f9a22-188">Imágenes u otros recursos de archivo</span><span class="sxs-lookup"><span data-stu-id="f9a22-188">Image or other file resource</span></span>

<span data-ttu-id="f9a22-189">Acceda a los datos binarios de un recurso específico.</span><span class="sxs-lookup"><span data-stu-id="f9a22-189">Get the binary data of a specific resource.</span></span> 

`../resources/{resource-id}/$value` 

<br/>

<span data-ttu-id="f9a22-190">Puede encontrar el URI del recurso de archivo en el [resultado HTML](onenote-input-output-html.md) de la página.</span><span class="sxs-lookup"><span data-stu-id="f9a22-190">You can find the file's resource URI in the page's [output HTML](onenote-input-output-html.md).</span></span>

<span data-ttu-id="f9a22-191">Por ejemplo, una etiqueta **img** incluye extremos del recurso de imagen original en el atributo **data-fullres-src** y de la imagen optimizada en el atributo **src**.</span><span class="sxs-lookup"><span data-stu-id="f9a22-191">For example, an **img** tag includes endpoints for the original image in the **data-fullres-src** attribute and the optimized image in the **src** attribute.</span></span> 

#### <a name="example"></a><span data-ttu-id="f9a22-192">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f9a22-192">Example</span></span>

```html
<img 
    src="https://www.onenote.com/api/v1.0/me/notes/resources/{image-id}/$value"  
    data-src-type="image/png"
    data-fullres-src="https://www.onenote.com/api/v1.0/resources/{image-id}/$value"  
    data-fullres-src-type="image/png" ... />
```

<span data-ttu-id="f9a22-193">Una etiqueta **object** incluye el extremo del recurso de archivos en el atributo **data**.</span><span class="sxs-lookup"><span data-stu-id="f9a22-193">And an **object** tag includes the endpoint for the file resource in the **data** attribute.</span></span> 

#### <a name="example"></a><span data-ttu-id="f9a22-194">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f9a22-194">Example</span></span>

```html
<object
    data="https://www.onenote.com/api/v1.0/me/notes/resources/{file-id}/$value"
    data-attachment="fileName.pdf" 
    type="application/pdf" ... />
```

<span data-ttu-id="f9a22-195">Para obtener direcciones URL públicas que ya se han autenticado a los recursos de imagen en una página, incluya `preAuthenticated=true` en la cadena de consulta cuando [recupere el contenido de la página](#page-html-content) (**ejemplo:** `GET ../pages/{page-id}/content?preAuthenticated=true`).</span><span class="sxs-lookup"><span data-stu-id="f9a22-195">To get public, pre-authenticated URLs to the image resources on a page, include `preAuthenticated=true` in the query string when you [retrieve the page content](#page-html-content) (**example:**  `GET ../pages/{page-id}/content?preAuthenticated=true`).</span></span> <span data-ttu-id="f9a22-196">Las direcciones URL públicas que se devuelven en el [HTML de salida](onenote-input-output-html.md#output-html-examples-for-images) son válidas durante una hora.</span><span class="sxs-lookup"><span data-stu-id="f9a22-196">The public URLs that are returned in the [output HTML](onenote-input-output-html.md#output-html-examples-for-images) are valid for one hour.</span></span> <span data-ttu-id="f9a22-197">Sin esta etiqueta, las imágenes devueltas no se representarán directamente en un explorador porque son privadas y se necesita una autorización para recuperarlas, al igual que el contenido de la página.</span><span class="sxs-lookup"><span data-stu-id="f9a22-197">Without this flag, retrieved images won't render directly in a browser because they are private and require authorization to retrieve them, like the rest of the page contents.</span></span> 

> <span data-ttu-id="f9a22-198">**Nota:** no se admite la obtención de una colección de recursos.</span><span class="sxs-lookup"><span data-stu-id="f9a22-198">**Note:** Getting a collection of resources is not supported.</span></span> 

<span data-ttu-id="f9a22-199">Cuando obtiene un recurso de archivos, no es necesario incluir un tipo de contenido **Accept** en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f9a22-199">When you get a file resource, you don't need to include an **Accept** content type in the request.</span></span>

<span data-ttu-id="f9a22-200">Para obtener más información sobre las solicitudes GET, consulte los siguientes recursos en la referencia de la API de REST de Microsoft Graph:</span><span class="sxs-lookup"><span data-stu-id="f9a22-200">For more information about GET requests, see the following resources in the Microsoft Graph API REST reference:</span></span>

- [<span data-ttu-id="f9a22-201">GET Pages</span><span class="sxs-lookup"><span data-stu-id="f9a22-201">GET Pages</span></span>](/graph/api/page-get?view=graph-rest-1.0)
- [<span data-ttu-id="f9a22-202">GET Sections</span><span class="sxs-lookup"><span data-stu-id="f9a22-202">GET Sections</span></span>](/graph/api/section-get?view=graph-rest-1.0)
- [<span data-ttu-id="f9a22-203">GET SectionGroups</span><span class="sxs-lookup"><span data-stu-id="f9a22-203">GET SectionGroups</span></span>](/graph/api/sectiongroup-get?view=graph-rest-1.0)
- [<span data-ttu-id="f9a22-204">GET Notebooks</span><span class="sxs-lookup"><span data-stu-id="f9a22-204">GET Notebooks</span></span>](/graph/api/notebook-get?view=graph-rest-1.0) 




<a name="example"></a>

## <a name="example-get-requests"></a><span data-ttu-id="f9a22-205">Solicitudes GET de ejemplo</span><span class="sxs-lookup"><span data-stu-id="f9a22-205">Example GET requests</span></span>

<span data-ttu-id="f9a22-206">Puede consultar las entidades de OneNote y el contenido de la página de búsqueda para obtener solo la información que necesita.</span><span class="sxs-lookup"><span data-stu-id="f9a22-206">You can query for OneNote entities and search page content to get just the information you need.</span></span> <span data-ttu-id="f9a22-207">Los siguientes ejemplos muestran algunas formas en las que puede usar [opciones de cadena de consulta compatibles](#supported-odata-query-string-options) en las solicitudes GET a Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="f9a22-207">The following examples show some ways you can use [supported query string options](#supported-odata-query-string-options) in GET requests to Microsoft Graph.</span></span> 

<span data-ttu-id="f9a22-208">**Recuerde:**</span><span class="sxs-lookup"><span data-stu-id="f9a22-208">**Remember:**</span></span>

- <span data-ttu-id="f9a22-209">Todas las solicitudes GET empiezan con la [dirección URL raíz de servicio](/graph/api/resources/onenote-api-overview?view=graph-rest-1.0#root-url).</span><span class="sxs-lookup"><span data-stu-id="f9a22-209">All GET requests start with the [service root URL](/graph/api/resources/onenote-api-overview?view=graph-rest-1.0#root-url).</span></span> <br/><br/><span data-ttu-id="f9a22-210">**Ejemplos**: `https://www.onenote.com/api/v1.0/me/notes` y `https://www.onenote.com/api/v1.0/myOrganization/siteCollections/{id}/sites/{id}/notes/`</span><span class="sxs-lookup"><span data-stu-id="f9a22-210">**Examples**: `https://www.onenote.com/api/v1.0/me/notes` and `https://www.onenote.com/api/v1.0/myOrganization/siteCollections/{id}/sites/{id}/notes/`</span></span>

- <span data-ttu-id="f9a22-211">Los espacios en la cadena de consulta URL deben usar la codificación %20.</span><span class="sxs-lookup"><span data-stu-id="f9a22-211">Spaces in the URL query string must use %20 encoding.</span></span><br/><br/><span data-ttu-id="f9a22-212">**Ejemplo**: `filter=title%20eq%20'biology'`</span><span class="sxs-lookup"><span data-stu-id="f9a22-212">**Example**: `filter=title%20eq%20'biology'`</span></span>

- <span data-ttu-id="f9a22-213">Los nombres de propiedad y las comparaciones de cadenas de OData distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f9a22-213">Property names and OData string comparisons are case-sensitive.</span></span> <span data-ttu-id="f9a22-214">Se recomienda usar la función **tolower** de OData para comparaciones de cadenas.</span><span class="sxs-lookup"><span data-stu-id="f9a22-214">We recommend using the OData **tolower** function for string comparisons.</span></span><br/><br/><span data-ttu-id="f9a22-215">**Ejemplo**: `filter=tolower(name) eq 'spring'`</span><span class="sxs-lookup"><span data-stu-id="f9a22-215">**Example**: `filter=tolower(name) eq 'spring'`</span></span>
 

### <a name="search--filter"></a><span data-ttu-id="f9a22-216">search & filter</span><span class="sxs-lookup"><span data-stu-id="f9a22-216">search & filter</span></span>  

<span data-ttu-id="f9a22-217">Obtenga todas las páginas que contienen el término *receta* creadas por una aplicación específica (`search` solo está disponible para blocs de notas de cliente).</span><span class="sxs-lookup"><span data-stu-id="f9a22-217">Get all pages that contain the term *recipe* that were created by a specific app (`search` is available for consumer notebooks only).</span></span>

```
[GET] ../pages?search=recipe&filter=createdByAppId eq 'WLID-000000004C12821A'
```
 
### <a name="search--select"></a><span data-ttu-id="f9a22-218">search & select</span><span class="sxs-lookup"><span data-stu-id="f9a22-218">search & select</span></span>  

<span data-ttu-id="f9a22-219">Obtenga el título, los vínculos de cliente de OneNote y el vínculo de **contentUrl** para todas las páginas que contienen el término *golgi app* (`search` solo está disponible para blocs de notas de cliente).</span><span class="sxs-lookup"><span data-stu-id="f9a22-219">Get the title, OneNote client links, and **contentUrl** link for all pages that contain the term *golgi app* (`search` is available for consumer notebooks only).</span></span>

```
[GET] ../pages?search=golgi app&select=title,links,contentUrl
```
 
### <a name="expand"></a><span data-ttu-id="f9a22-220">expand</span><span class="sxs-lookup"><span data-stu-id="f9a22-220">expand</span></span> 

<span data-ttu-id="f9a22-221">Obtenga todos los blocs de notas y expanda sus secciones y grupos de secciones.</span><span class="sxs-lookup"><span data-stu-id="f9a22-221">Get all notebooks and expand their sections and section groups.</span></span>  

```
[GET] ../notebooks?expand=sections,sectionGroups
```

<br/>

<span data-ttu-id="f9a22-222">Obtienen un grupo de secciones específico y expanden sus secciones y grupos de secciones.</span><span class="sxs-lookup"><span data-stu-id="f9a22-222">Get a specific section group and expand its sections and section groups.</span></span>  

```
[GET] ../sectionGroups/{sectiongroup-id}?expand=sections,sectionGroups
```

<br/>

<span data-ttu-id="f9a22-223">Obtenga una página y expanda su sección principal y bloc de notas principal.</span><span class="sxs-lookup"><span data-stu-id="f9a22-223">Get a page and expand its parent section and parent notebook.</span></span>

```
[GET] ../pages/{page-id}?expand=parentSection,parentNotebook
```

### <a name="expand-multiple-levels"></a><span data-ttu-id="f9a22-224">expand (varios niveles)</span><span class="sxs-lookup"><span data-stu-id="f9a22-224">expand (multiple levels)</span></span>  

<span data-ttu-id="f9a22-225">Obtenga todos los blocs de notas y expanda sus secciones y grupos de secciones, y expanden todas las secciones en cada grupo de secciones.</span><span class="sxs-lookup"><span data-stu-id="f9a22-225">Get all notebooks and expand their sections and section groups, and expand all sections in each section group.</span></span>  

```
[GET] ../notebooks?expand=sections,sectionGroups(expand=sections)
```
 
> <span data-ttu-id="f9a22-226">**Nota:** No se admite expandir elementos primarios de entidades secundarias o expandir elementos secundarios de entidades primarias. Hacer eso crearía una referencia circular.</span><span class="sxs-lookup"><span data-stu-id="f9a22-226">**Note:** Expanding parents of child entities or expanding children of parent entities creates a circular reference and is not supported.</span></span>

 
### <a name="expand--select-multiple-levels"></a><span data-ttu-id="f9a22-227">expand & select (varios niveles)</span><span class="sxs-lookup"><span data-stu-id="f9a22-227">expand & select (multiple levels)</span></span>  

<span data-ttu-id="f9a22-228">Obtenga el nombre y el vínculo a **self** para un grupo de secciones específico, y obtenga el nombre y los vínculos a **self** para todas sus secciones.</span><span class="sxs-lookup"><span data-stu-id="f9a22-228">Get the name and **self** link for a specific section group, and get the name and **self** links for all its sections.</span></span>  

```
[GET] ../sectionGroups/{sectiongroup-id}?expand=sections(select=name,self)&select=name,self
```

<br/>

<span data-ttu-id="f9a22-229">Obtienen el nombre y el vínculo a **self** para todas las secciones, y obtienen el nombre y la hora de creación del bloc de notas primario de cada sección.</span><span class="sxs-lookup"><span data-stu-id="f9a22-229">Get the name and **self** link for all sections, and get the name and created time of each section's parent notebook.</span></span>  

```
[GET] ../sections?expand=parentNotebook(select=name,createdTime)&select=name,self
```

<br/>
 
<span data-ttu-id="f9a22-230">Obtenga el título y el identificador de todas las páginas, y obtenga el nombre de la sección principal y bloc de notas principal.</span><span class="sxs-lookup"><span data-stu-id="f9a22-230">Get the title and ID for all pages, and get the name of the parent section and parent notebook.</span></span>

```
[GET] ../pages?select=id,title&expand=parentSection(select=name),parentNotebook(select=name)
```

### <a name="expand--levels-multiple-levels"></a><span data-ttu-id="f9a22-231">expand & levels (varios niveles)</span><span class="sxs-lookup"><span data-stu-id="f9a22-231">expand & levels (multiple levels)</span></span>  

<span data-ttu-id="f9a22-232">Obtenga todos los blocs de notas, grupos de secciones y todas las secciones.</span><span class="sxs-lookup"><span data-stu-id="f9a22-232">Get all notebooks, sections, and section groups.</span></span>  

```
[GET] ../notebooks?expand=sections,sectionGroups(expand=sections,sectionGroups(levels=max;expand=sections))
```
 
### <a name="filter"></a><span data-ttu-id="f9a22-233">filter</span><span class="sxs-lookup"><span data-stu-id="f9a22-233">filter</span></span>

<span data-ttu-id="f9a22-234">Obtenga todas las secciones creadas en octubre de 2014.</span><span class="sxs-lookup"><span data-stu-id="f9a22-234">Get all sections that were created in October 2014.</span></span>

```
[GET] ../sections?filter=createdTime ge 2014-10-01 and createdTime le 2014-10-31
```

<br/>

<span data-ttu-id="f9a22-235">Obtenga todas las páginas creadas por una aplicación específica desde el 1 de enero de 2015.</span><span class="sxs-lookup"><span data-stu-id="f9a22-235">Get the pages that were created by a specific app since January 1, 2015.</span></span>

```
[GET] ../pages?filter=createdByAppId eq 'WLID-0000000048118631' and createdTime ge 2015-01-01
```

### <a name="filter--expand"></a><span data-ttu-id="f9a22-236">filter & expand</span><span class="sxs-lookup"><span data-stu-id="f9a22-236">filter & expand</span></span>  

<span data-ttu-id="f9a22-237">Obtenga todas las páginas de un bloc de notas específico.</span><span class="sxs-lookup"><span data-stu-id="f9a22-237">Get all pages in a specific notebook.</span></span> <span data-ttu-id="f9a22-238">La API devuelve 20 entradas de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f9a22-238">The API returns 20 entries by default.</span></span>

```
[GET] ../pages?filter=parentNotebook/id eq '{notebook-id}'&expand=parentNotebook
```

<br/>

<span data-ttu-id="f9a22-239">Obtenga el nombre y el vínculo a **pagesUrl** para todas las secciones del bloc de notas *Escuela*.</span><span class="sxs-lookup"><span data-stu-id="f9a22-239">Get the name and **pagesUrl** link for all sections from the *School* notebook.</span></span> <span data-ttu-id="f9a22-240">Las comparaciones de cadenas OData distinguen mayúsculas de minúsculas, por lo que se recomienda usar la función **tolower**.</span><span class="sxs-lookup"><span data-stu-id="f9a22-240">OData string comparisons are case-sensitive, so use the **tolower** function as a best practice.</span></span>

```
[GET] ../notebooks?filter=tolower(name) eq 'school'&expand=sections(select=name,pagesUrl)
```

### <a name="filter--select--orderby"></a><span data-ttu-id="f9a22-241">filter & select & orderby</span><span class="sxs-lookup"><span data-stu-id="f9a22-241">filter & select & orderby</span></span>   

<span data-ttu-id="f9a22-242">Obtenga el nombre y el vínculo a **pagesUrl** para todas las secciones que contienen el término *spring* en el nombre de la sección.</span><span class="sxs-lookup"><span data-stu-id="f9a22-242">Get the name and **pagesUrl** link for all sections that contain the term *spring* in the section name.</span></span> <span data-ttu-id="f9a22-243">Ordene las secciones por fecha de última modificación.</span><span class="sxs-lookup"><span data-stu-id="f9a22-243">Order sections by last modified date.</span></span>

```
[GET] ../sections?filter=contains(tolower(name),'spring')&select=name,pagesUrl&orderby=lastModifiedTime desc
```
 
### <a name="orderby"></a><span data-ttu-id="f9a22-244">orderby</span><span class="sxs-lookup"><span data-stu-id="f9a22-244">orderby</span></span>

<span data-ttu-id="f9a22-245">Obtenga las primeras 20 páginas ordenadas por propiedad **createdByAppId** y luego por fecha de creación más reciente.</span><span class="sxs-lookup"><span data-stu-id="f9a22-245">Get the first 20 pages ordered by **createdByAppId** property and then by most recent created time.</span></span> <span data-ttu-id="f9a22-246">La API devuelve 20 entradas de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f9a22-246">The API returns 20 entries by default.</span></span>

```
[GET] ../pages?orderby=createdByAppId,createdTime desc
```

### <a name="search--filter--top"></a><span data-ttu-id="f9a22-247">search & filter & top</span><span class="sxs-lookup"><span data-stu-id="f9a22-247">search & filter & top</span></span> 

<span data-ttu-id="f9a22-248">Obtenga las cinco páginas más recientes creadas desde el 1 de enero de 2015, que contienen la frase *división de celda*.</span><span class="sxs-lookup"><span data-stu-id="f9a22-248">Get the five newest pages created since January 1, 2015 that contain the phrase *cell division*.</span></span> <span data-ttu-id="f9a22-249">La API devuelve 20 entradas de forma predeterminada con un máximo de 100.</span><span class="sxs-lookup"><span data-stu-id="f9a22-249">The API returns 20 entries by default with a maximum of 100.</span></span> <span data-ttu-id="f9a22-250">La ordenación predeterminada para las páginas es `lastModifiedTime desc` (`search` solo está disponible para los blocs de notas de cliente).</span><span class="sxs-lookup"><span data-stu-id="f9a22-250">The default sort order for pages is `lastModifiedTime desc` (`search` is available for consumer notebooks only).</span></span>

```
[GET] ../pages?search="cell division"&filter=createdTime ge 2015-01-01&top=5
```

### <a name="search--filter--top--skip"></a><span data-ttu-id="f9a22-251">search & filter & top & skip</span><span class="sxs-lookup"><span data-stu-id="f9a22-251">search & filter & top & skip</span></span>  

<span data-ttu-id="f9a22-252">Obtenga las siguientes cinco páginas del conjunto de resultados (`search` solo está disponible para los blocs de notas de cliente).</span><span class="sxs-lookup"><span data-stu-id="f9a22-252">Get the next five pages in the result set (`search` is available for consumer notebooks only).</span></span>

```
[GET] ../pages?search=biology&filter=createdTime ge 2015-01-01&top=5&skip=5
```

<br/>

<span data-ttu-id="f9a22-253">Y las cinco siguientes (`search` solo está disponible para los blocs de notas de clientes)</span><span class="sxs-lookup"><span data-stu-id="f9a22-253">And the next five (`search` is available for consumer notebooks only).</span></span>

```
[GET] ../pages?search=biology&filter=createdTime ge 2015-01-01&top=5&skip=10
```

> <span data-ttu-id="f9a22-254">**Nota:** Si se aplican **search** y **filter** a la misma solicitud, los resultados incluyen solamente las entidades que coinciden con ambos criterios.</span><span class="sxs-lookup"><span data-stu-id="f9a22-254">**Note:** If both **search** and **filter** are applied to the same request, the results include only those entities that match both criteria.</span></span>
 
### <a name="select"></a><span data-ttu-id="f9a22-255">select</span><span class="sxs-lookup"><span data-stu-id="f9a22-255">select</span></span>

<span data-ttu-id="f9a22-256">Obtenga el nombre, la hora de creación y el vínculo a **self** para todas las secciones en los blocs de notas del usuario.</span><span class="sxs-lookup"><span data-stu-id="f9a22-256">Get the name, created time, and **self** link for all sections in the user's notebooks.</span></span>

```
[GET] ../sections?select=name,createdTime,self
```

<br/>

<span data-ttu-id="f9a22-257">Obtenga el título, la hora de creación y los vínculos a clientes de OneNote para una página específica.</span><span class="sxs-lookup"><span data-stu-id="f9a22-257">Get the title, created time, and OneNote client links for a specific page.</span></span>

```
[GET] ../pages/{page-id}?select=title,createdTime,links
```

### <a name="select--expand--filter-multiple-levels"></a><span data-ttu-id="f9a22-258">select & expand & filter (varios niveles)</span><span class="sxs-lookup"><span data-stu-id="f9a22-258">select & expand & filter (multiple levels)</span></span>  

<span data-ttu-id="f9a22-259">Obtenga el nombre y el vínculo a **pagesUrl** para todas las secciones en el bloc de notas predeterminado del usuario.</span><span class="sxs-lookup"><span data-stu-id="f9a22-259">Get the name and **pagesUrl** link for all sections in the user's default notebook.</span></span>

```
[GET] ../notebooks?select=name&expand=sections(select=name,pagesUrl)&filter=isDefault eq true
```

### <a name="top--select--orderby"></a><span data-ttu-id="f9a22-260">top & select & orderby</span><span class="sxs-lookup"><span data-stu-id="f9a22-260">top & select & orderby</span></span> 

<span data-ttu-id="f9a22-261">Obtenga el título y el vínculo **self** de las primeras 50 páginas, ordenadas alfabéticamente por título.</span><span class="sxs-lookup"><span data-stu-id="f9a22-261">Get the title and **self** link for the first 50 pages, ordered alphabetically by title.</span></span> <span data-ttu-id="f9a22-262">La API devuelve 20 entradas de forma predeterminada con un máximo de 100.</span><span class="sxs-lookup"><span data-stu-id="f9a22-262">The API returns 20 entries by default with a maximum of 100.</span></span> <span data-ttu-id="f9a22-263">El criterio de ordenación predeterminado para páginas es `lastModifiedTime desc`.</span><span class="sxs-lookup"><span data-stu-id="f9a22-263">The default sort order for pages is `lastModifiedTime desc`.</span></span>

```
[GET] ../pages?top=50&select=title,self&orderby=title
```

### <a name="skip--top--select--orderby"></a><span data-ttu-id="f9a22-264">skip & top & select & orderby</span><span class="sxs-lookup"><span data-stu-id="f9a22-264">skip & top & select & orderby</span></span>  

<span data-ttu-id="f9a22-p117">Obtenga las páginas 51 a 100. La API devuelve 20 entradas de forma predeterminada con un máximo de 100.</span><span class="sxs-lookup"><span data-stu-id="f9a22-p117">Get pages 51 to 100. The API returns 20 entries by default with a maximum of 100.</span></span>

```
[GET] ../pages?skip=50&top=50&select=title,self&orderby=title
```

> <span data-ttu-id="f9a22-267">**Note:** Las solicitudes GET para páginas que recuperan el número predeterminado de entradas (es decir, no especifican una expresión **top**) devuelven un vínculo a **@odata.nextLink** en la respuesta que puede usar para obtener las 20 entradas siguientes.</span><span class="sxs-lookup"><span data-stu-id="f9a22-267">**Note:** GET requests for pages that retrieve the default number of entries (that is, they don't specify a **top** expression) return an **@odata.nextLink** link in the response that you can use to get the next 20 entries.</span></span>
 

<a name="supported-odata-query-string-options"></a>

## <a name="supported-odata-query-string-options"></a><span data-ttu-id="f9a22-268">Opciones de cadena de consultas OData admitidas</span><span class="sxs-lookup"><span data-stu-id="f9a22-268">Supported OData query string options</span></span>

<span data-ttu-id="f9a22-269">Al enviar solicitudes GET a Microsoft Graph, puede usar las opciones de cadena de consultas OData para personalizar la consulta y obtener solo la información que necesita.</span><span class="sxs-lookup"><span data-stu-id="f9a22-269">When sending GET requests to Microsoft Graph, you can use OData query string options to customize your query and get just the information you need.</span></span> <span data-ttu-id="f9a22-270">También puede mejorar el rendimiento al reducir el número de llamadas al servicio y el tamaño de la carga de respuesta.</span><span class="sxs-lookup"><span data-stu-id="f9a22-270">They can also improve performance by reducing the number of calls to the service and the size of the response payload.</span></span>

> <span data-ttu-id="f9a22-271">**Note:** Para su legibilidad, los ejemplos de este artículo no usan la codificación porcentual de %20 que se requiere para espacios en la cadena de consulta URL: `filter=isDefault%20eq%20true`</span><span class="sxs-lookup"><span data-stu-id="f9a22-271">**Note:** For readability, the examples in this article don't use the %20 percent-encoding required for spaces in the URL query string: `filter=isDefault%20eq%20true`</span></span>
 
| <span data-ttu-id="f9a22-272">Opción de consulta</span><span class="sxs-lookup"><span data-stu-id="f9a22-272">Query option</span></span> | <span data-ttu-id="f9a22-273">Ejemplo y descripción</span><span class="sxs-lookup"><span data-stu-id="f9a22-273">Example and description</span></span> |  
|------|------|  
| <span data-ttu-id="f9a22-274">count</span><span class="sxs-lookup"><span data-stu-id="f9a22-274">count</span></span> | <p>`count=true`</p><p><span data-ttu-id="f9a22-p119">El recuento de entidades de la colección. El valor se devuelve en la propiedad **@odata.count** de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f9a22-p119">The count of entities in the collection. The value is returned in the **@odata.count** property in the response.</span></span></p> |  
| <span data-ttu-id="f9a22-277">expand</span><span class="sxs-lookup"><span data-stu-id="f9a22-277">expand</span></span> | <p>`expand=sections,sectionGroups`</p><p><span data-ttu-id="f9a22-278">Las propiedades de navegación para devolver la respuesta en línea.</span><span class="sxs-lookup"><span data-stu-id="f9a22-278">The navigation properties to return inline in the response.</span></span> <span data-ttu-id="f9a22-279">Las siguientes propiedades son compatibles con las expresiones **expand**:</span><span class="sxs-lookup"><span data-stu-id="f9a22-279">The following properties are supported for **expand** expressions:</span></span><br /> <span data-ttu-id="f9a22-280">- Páginas: **parentNotebook**, **parentSection**</span><span class="sxs-lookup"><span data-stu-id="f9a22-280">- Pages: **parentNotebook**, **parentSection**</span></span><br /> <span data-ttu-id="f9a22-281">- Secciones: **parentNotebook**, **parentSectionGroup**</span><span class="sxs-lookup"><span data-stu-id="f9a22-281">- Sections: **parentNotebook**, **parentSectionGroup**</span></span><br /> <span data-ttu-id="f9a22-282">- Grupos de secciones: **sections**, **sectionGroups**, **parentNotebook**, **parentSectionGroup**</span><span class="sxs-lookup"><span data-stu-id="f9a22-282">- Section groups: **sections**, **sectionGroups**, **parentNotebook**, **parentSectionGroup**</span></span><br /> <span data-ttu-id="f9a22-283">- Blocs de notas: **sections**, **sectionGroups**</span><span class="sxs-lookup"><span data-stu-id="f9a22-283">- Notebooks: **sections**, **sectionGroups**</span></span></p><p><span data-ttu-id="f9a22-p121">De forma predeterminada, las solicitudes GET para páginas expanden **parentSection** y seleccionan las propiedades **id**, **name** y **self** de la sección. Las solicitudes GET predeterminadas para secciones y grupos de secciones expanden tanto **parentNotebook** como **parentSectionGroup**, y seleccionan las propiedades **id**, **name** y **self** del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="f9a22-p121">By default, GET requests for pages expands **parentSection** and select the section's **id**, **name**, and **self** properties. Default GET requests for sections and section groups expand both **parentNotebook** and **parentSectionGroup**, and select the parents' **id**, **name**, and **self** properties. </span></span></p><p><span data-ttu-id="f9a22-286">Puede usarse para una única entidad o una colección.</span><span class="sxs-lookup"><span data-stu-id="f9a22-286">Can be used for a single entity or a collection.</span></span><br /><span data-ttu-id="f9a22-287">Separe las distintas propiedades mediante comas.</span><span class="sxs-lookup"><span data-stu-id="f9a22-287">Separate multiple properties with commas.</span></span><br /><span data-ttu-id="f9a22-288">Los nombres de las propiedades distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f9a22-288">Property names are case-sensitive.</span></span></p> |   
| <span data-ttu-id="f9a22-289">filter</span><span class="sxs-lookup"><span data-stu-id="f9a22-289">filter</span></span> | <p>`filter=isDefault eq true`</p><p><span data-ttu-id="f9a22-290">Una expresión booleana por si desea incluir una entrada en el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="f9a22-290">A Boolean expression for whether to include an entry in the result set.</span></span> <span data-ttu-id="f9a22-291">Es compatible con las funciones y operadores de OData siguientes:</span><span class="sxs-lookup"><span data-stu-id="f9a22-291">Supports the following OData operators and functions:</span></span><br /> <span data-ttu-id="f9a22-292">- Operadores de comparación: **eq**, **ne**, **gt**, **ge**, **lt**, **le**</span><span class="sxs-lookup"><span data-stu-id="f9a22-292">- Comparison operators: **eq**, **ne**, **gt**, **ge**, **lt**, **le**</span></span><br /> <span data-ttu-id="f9a22-293">- Operadores lógicos: **and**, **or**, **not**</span><span class="sxs-lookup"><span data-stu-id="f9a22-293">- Logical operators: **and**, **or**, **not**</span></span><br /> <span data-ttu-id="f9a22-294">- Funciones de cadena: **contains**, **endswith**, **startswith**, **length**, **indexof**, **substring**, **tolower**, **toupper**, **trim**, **concat**</span><span class="sxs-lookup"><span data-stu-id="f9a22-294">- String functions: **contains**, **endswith**, **startswith**, **length**, **indexof**, **substring**, **tolower**, **toupper**, **trim**, **concat**</span></span></p><p><span data-ttu-id="f9a22-295">[Los nombres de propiedad](#onenote-entity-properties) y las comparaciones de cadenas de OData distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f9a22-295">[Property](#onenote-entity-properties) names and OData string comparisons are case-sensitive.</span></span> <span data-ttu-id="f9a22-296">Se recomienda usar la función **tolower** de OData para comparaciones de cadenas.</span><span class="sxs-lookup"><span data-stu-id="f9a22-296">We recommend using the OData **tolower** function for string comparisons.</span></span><br /><br /><span data-ttu-id="f9a22-297">**Ejemplo**: `filter=tolower(name) eq 'spring'`</span><span class="sxs-lookup"><span data-stu-id="f9a22-297">**Example**: `filter=tolower(name) eq 'spring'`</span></span></p> |  
| <span data-ttu-id="f9a22-298">orderby</span><span class="sxs-lookup"><span data-stu-id="f9a22-298">orderby</span></span> | <p>`orderby=title,createdTime desc`</p><p><span data-ttu-id="f9a22-p124">Las [propiedades](#onenote-entity-properties) según las cuales ordenar, con un **asc** opcional (predeterminado) u orden **desc**. Puede ordenar según cualquier propiedad de la entidad en la colección solicitada.</span><span class="sxs-lookup"><span data-stu-id="f9a22-p124">The [properties](#onenote-entity-properties) to sort by, with an optional **asc** (default) or **desc** sort order. You can sort by any property of the entity in the requested collection.</span></span></p><p><span data-ttu-id="f9a22-301">El orden predeterminado para blocs de notas, secciones y grupos de secciones es `name asc`, y para páginas es `lastModifiedTime desc` (última página modificada primero).</span><span class="sxs-lookup"><span data-stu-id="f9a22-301">The default sort order for notebooks, section groups, and sections is `name asc`, and for pages is `lastModifiedTime desc` (last modified page first).</span></span></p><p><span data-ttu-id="f9a22-302">Si tiene varias propiedades, sepárelas con comas, y ordénelas de la manera en que desea que se apliquen.</span><span class="sxs-lookup"><span data-stu-id="f9a22-302">Separate multiple properties with commas, and list them in the order that you want them applied.</span></span> <span data-ttu-id="f9a22-303">Los nombres de las propiedades distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f9a22-303">Property names are case-sensitive.</span></span></p> |  
| <span data-ttu-id="f9a22-304">buscar</span><span class="sxs-lookup"><span data-stu-id="f9a22-304">search</span></span> | <p>`search=cell div`</p><p><span data-ttu-id="f9a22-305">Solo está disponible para los blocs de notas de clientes.</span><span class="sxs-lookup"><span data-stu-id="f9a22-305">Available for consumer notebooks only.</span></span></p><p><span data-ttu-id="f9a22-p126">El término o la frase para buscar en el título de la página, el cuerpo de la página, el texto alternativo de la imagen y el texto OCR de la imagen. De forma predeterminada, las consultas de búsqueda devuelven resultados ordenados por relevancia.</span><span class="sxs-lookup"><span data-stu-id="f9a22-p126">The term or phrase to search for in the page title, page body, image alt text, and image OCR text. By default, search queries return results sorted by relevance.</span></span></p><p><span data-ttu-id="f9a22-308">OneNote usa la búsqueda de texto completo de Bing para admitir búsqueda de frases, lematización, omisión ortográfica, relevancia y clasificación, separación de palabras, varios idiomas y otras características de búsqueda de texto completo.</span><span class="sxs-lookup"><span data-stu-id="f9a22-308">OneNote uses Bing full-text search to support phrase search, stemming, spelling forgiveness, relevance and ranking, word breaking, multiple languages, and other full-text search features.</span></span> <span data-ttu-id="f9a22-309">Las cadenas de búsqueda distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f9a22-309">Search strings are case-insensitive.</span></span></p><p><span data-ttu-id="f9a22-310">Solo se aplica a las páginas de los blocs de notas que posee el usuario.</span><span class="sxs-lookup"><span data-stu-id="f9a22-310">Applies only to pages in notebooks owned by the user.</span></span> <span data-ttu-id="f9a22-311">El contenido indexado es privado y solo puede acceder a él su propietario.</span><span class="sxs-lookup"><span data-stu-id="f9a22-311">Indexed content is private and can only be accessed by the owner.</span></span> <span data-ttu-id="f9a22-312">Las páginas protegidas con contraseña no están indexadas.</span><span class="sxs-lookup"><span data-stu-id="f9a22-312">Password-protected pages are not indexed.</span></span> <span data-ttu-id="f9a22-313">Solo se aplica al extremo `pages`.</span><span class="sxs-lookup"><span data-stu-id="f9a22-313">Applies only to the `pages` endpoint.</span></span></p> |  
| <span data-ttu-id="f9a22-314">select</span><span class="sxs-lookup"><span data-stu-id="f9a22-314">select</span></span> | <p>`select=id,title`</p><p><span data-ttu-id="f9a22-315">Las [propiedades](#onenote-entity-properties) que se devuelven.</span><span class="sxs-lookup"><span data-stu-id="f9a22-315">The [properties](#onenote-entity-properties) to return.</span></span> <span data-ttu-id="f9a22-316">Puede usarse para una única entidad o para una colección.</span><span class="sxs-lookup"><span data-stu-id="f9a22-316">Can be used for a single entity or for a collection.</span></span> <span data-ttu-id="f9a22-317">Separe las distintas propiedades mediante comas.</span><span class="sxs-lookup"><span data-stu-id="f9a22-317">Separate multiple properties with commas.</span></span> <span data-ttu-id="f9a22-318">Los nombres de las propiedades distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f9a22-318">Property names are case-sensitive.</span></span></p> |  
| <span data-ttu-id="f9a22-319">skip</span><span class="sxs-lookup"><span data-stu-id="f9a22-319">skip</span></span> | <p>`skip=10`</p><p><span data-ttu-id="f9a22-320">El número de entradas que se omiten del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="f9a22-320">The number of entries to skip in the result set.</span></span> <span data-ttu-id="f9a22-321">Se usa normalmente para los resultados de paginación.</span><span class="sxs-lookup"><span data-stu-id="f9a22-321">Typically used for paging results.</span></span></p> |  
| <span data-ttu-id="f9a22-322">top</span><span class="sxs-lookup"><span data-stu-id="f9a22-322">top</span></span> | <p>`top=50`</p><p><span data-ttu-id="f9a22-323">El número de entradas para devolver en el conjunto de resultados, hasta un máximo de 100.</span><span class="sxs-lookup"><span data-stu-id="f9a22-323">The number of entries to return in the result set, up to a maximum of 100.</span></span> <span data-ttu-id="f9a22-324">El valor predeterminado es 20.</span><span class="sxs-lookup"><span data-stu-id="f9a22-324">The default value is 20.</span></span></p> |  

<span data-ttu-id="f9a22-325">Microsoft Graph también proporciona la opción de cadena de consulta `pagelevel` que puede usar para obtener el nivel y el orden de las páginas en la sección principal.</span><span class="sxs-lookup"><span data-stu-id="f9a22-325">Microsoft Graph also provides the `pagelevel` query string option you can use to get the level and order of pages within the parent section.</span></span> <span data-ttu-id="f9a22-326">Solo se aplica a las consultas para las páginas de una sección específica o para una página específica.</span><span class="sxs-lookup"><span data-stu-id="f9a22-326">Applies only to queries for pages in a specific section or queries for a specific page.</span></span> 

#### <a name="examples"></a><span data-ttu-id="f9a22-327">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f9a22-327">Examples</span></span> 

- `GET ../sections/{section-id}/pages?pagelevel=true` 
- `GET ../pages/{page-id}?pagelevel=true` 

### <a name="supported-odata-operators-and-functions"></a><span data-ttu-id="f9a22-328">Operadores y funciones OData compatibles</span><span class="sxs-lookup"><span data-stu-id="f9a22-328">Supported OData operators and functions</span></span>

<span data-ttu-id="f9a22-329">Microsoft Graph admite los siguientes operadores y funciones OData en las expresiones **filter**.</span><span class="sxs-lookup"><span data-stu-id="f9a22-329">Microsoft Graph supports the following OData operators and functions in **filter** expressions.</span></span> <span data-ttu-id="f9a22-330">Al usar expresiones OData, recuerde:</span><span class="sxs-lookup"><span data-stu-id="f9a22-330">When using OData expressions, remember:</span></span>

- <span data-ttu-id="f9a22-331">Debe reemplazar los espacios en la cadena de consulta URL con la codificación `%20`.</span><span class="sxs-lookup"><span data-stu-id="f9a22-331">Spaces in the URL query string must be replaced with the `%20` encoding.</span></span><br/><br/><span data-ttu-id="f9a22-332">**Ejemplo:** `filter=isDefault%20eq%20true`</span><span class="sxs-lookup"><span data-stu-id="f9a22-332">**Example:** `filter=isDefault%20eq%20true`</span></span>

- <span data-ttu-id="f9a22-333">Los nombres de propiedad y las comparaciones de cadenas de OData distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f9a22-333">Property names and OData string comparisons are case-sensitive.</span></span> <span data-ttu-id="f9a22-334">Se recomienda usar la función **tolower** de OData para comparaciones de cadenas.</span><span class="sxs-lookup"><span data-stu-id="f9a22-334">We recommend using the OData **tolower** function for string comparisons.</span></span><br/><br/><span data-ttu-id="f9a22-335">**Ejemplo:** `filter=tolower(name) eq 'spring'`</span><span class="sxs-lookup"><span data-stu-id="f9a22-335">**Example:** `filter=tolower(name) eq 'spring'`</span></span>


| <span data-ttu-id="f9a22-336">Operador de comparación</span><span class="sxs-lookup"><span data-stu-id="f9a22-336">Comparison operator</span></span> | <span data-ttu-id="f9a22-337">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f9a22-337">Example</span></span> |  
|------|------|  
| <span data-ttu-id="f9a22-338">eq</span><span class="sxs-lookup"><span data-stu-id="f9a22-338">eq</span></span><br /><span data-ttu-id="f9a22-339">(igual a)</span><span class="sxs-lookup"><span data-stu-id="f9a22-339">(equal to)</span></span> | `createdByAppId eq '{app-id}'` |  
| <span data-ttu-id="f9a22-340">ne</span><span class="sxs-lookup"><span data-stu-id="f9a22-340">ne</span></span><br /><span data-ttu-id="f9a22-341">(no es igual a)</span><span class="sxs-lookup"><span data-stu-id="f9a22-341">(not equal to)</span></span> | `userRole ne 'Owner'` |  
| <span data-ttu-id="f9a22-342">gt</span><span class="sxs-lookup"><span data-stu-id="f9a22-342">gt</span></span><br /><span data-ttu-id="f9a22-343">(mayor que)</span><span class="sxs-lookup"><span data-stu-id="f9a22-343">(greater than)</span></span> | `createdTime gt 2014-02-23` |  
| <span data-ttu-id="f9a22-344">ge</span><span class="sxs-lookup"><span data-stu-id="f9a22-344">ge</span></span><br /><span data-ttu-id="f9a22-345">(mayor o igual que)</span><span class="sxs-lookup"><span data-stu-id="f9a22-345">(greater than or equal to)</span></span> | `lastModifiedTime ge 2014-05-05T07:00:00Z` |  
| <span data-ttu-id="f9a22-346">lt</span><span class="sxs-lookup"><span data-stu-id="f9a22-346">lt</span></span><br /><span data-ttu-id="f9a22-347">(menor que)</span><span class="sxs-lookup"><span data-stu-id="f9a22-347">(less than)</span></span> | `createdTime lt 2014-02-23` |  
| <span data-ttu-id="f9a22-348">le</span><span class="sxs-lookup"><span data-stu-id="f9a22-348">le</span></span><br /><span data-ttu-id="f9a22-349">(menor que o igual que)</span><span class="sxs-lookup"><span data-stu-id="f9a22-349">(less than or equal to)</span></span> | `lastModifiedTime le 2014-02-23` |  

<br/>

| <span data-ttu-id="f9a22-350">Operador lógico</span><span class="sxs-lookup"><span data-stu-id="f9a22-350">Logical operator</span></span> | <span data-ttu-id="f9a22-351">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f9a22-351">Example</span></span> |  
|------|------|  
| <span data-ttu-id="f9a22-352">y</span><span class="sxs-lookup"><span data-stu-id="f9a22-352">and</span></span> | `createdTime le 2014-01-30 and createdTime gt 2014-01-23` |  
| <span data-ttu-id="f9a22-353">o</span><span class="sxs-lookup"><span data-stu-id="f9a22-353">or</span></span> | `createdByAppId eq '{app-id}' or createdByAppId eq '{app-id}'` |  
| <span data-ttu-id="f9a22-354">
not</span><span class="sxs-lookup"><span data-stu-id="f9a22-354">not</span></span> | `not contains(tolower(title),'school')` |  

<br/>
  
| <span data-ttu-id="f9a22-355">Función String</span><span class="sxs-lookup"><span data-stu-id="f9a22-355">String function</span></span> | <span data-ttu-id="f9a22-356">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f9a22-356">Example</span></span> |  
|------|------|   
| <span data-ttu-id="f9a22-357">contains</span><span class="sxs-lookup"><span data-stu-id="f9a22-357">contains</span></span> | `contains(tolower(title),'spring')` |  
| <span data-ttu-id="f9a22-358">endswith</span><span class="sxs-lookup"><span data-stu-id="f9a22-358">endswith</span></span> | `endswith(tolower(title),'spring')` |  
| <span data-ttu-id="f9a22-359">startswith</span><span class="sxs-lookup"><span data-stu-id="f9a22-359">startswith</span></span> | `startswith(tolower(title),'spring')` |  
| <span data-ttu-id="f9a22-360">length</span><span class="sxs-lookup"><span data-stu-id="f9a22-360">length</span></span> | `length(title) eq 19` |  
| <span data-ttu-id="f9a22-361">indexof</span><span class="sxs-lookup"><span data-stu-id="f9a22-361">indexof</span></span> | `indexof(tolower(title),'spring') eq 1` |  
| <span data-ttu-id="f9a22-362">substring</span><span class="sxs-lookup"><span data-stu-id="f9a22-362">substring</span></span> | `substring(tolower(title),1) eq 'spring'` |  
| <span data-ttu-id="f9a22-363">tolower</span><span class="sxs-lookup"><span data-stu-id="f9a22-363">tolower</span></span> | `tolower(title) eq 'spring'` |  
| <span data-ttu-id="f9a22-364">toupper</span><span class="sxs-lookup"><span data-stu-id="f9a22-364">toupper</span></span> | `toupper(title) eq 'SPRING'` |  
| <span data-ttu-id="f9a22-365">trim</span><span class="sxs-lookup"><span data-stu-id="f9a22-365">trim</span></span> | `trim(tolower(title)) eq 'spring'` |  
| <span data-ttu-id="f9a22-366">concat</span><span class="sxs-lookup"><span data-stu-id="f9a22-366">concat</span></span> | `concat(title,'- by MyRecipesApp') eq 'Carrot Cake Recipe - by MyRecipesApp'` |  
 

<a name="properties"></a>

## <a name="onenote-entity-properties"></a><span data-ttu-id="f9a22-367">Propiedades de entidad de OneNote</span><span class="sxs-lookup"><span data-stu-id="f9a22-367">OneNote entity properties</span></span>

<span data-ttu-id="f9a22-368">Las expresiones de consulta **filter**, **select**, **expand** y **orderby** pueden incluir propiedades de las entidades de OneNote.</span><span class="sxs-lookup"><span data-stu-id="f9a22-368">The **filter**, **select**, **expand**, and **orderby** query expressions can include properties of OneNote entities.</span></span> 

#### <a name="example"></a><span data-ttu-id="f9a22-369">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f9a22-369">Example</span></span>

`../sections?filter=createdTime ge 2015-01-01&select=name,pagesUrl&orderby=lastModifiedTime desc` 

<span data-ttu-id="f9a22-370">Los nombres de las propiedades distinguen mayúsculas de minúsculas en las expresiones de consulta.</span><span class="sxs-lookup"><span data-stu-id="f9a22-370">Property names are case-sensitive in query expressions.</span></span>

<span data-ttu-id="f9a22-371">Para obtener la lista de propiedades y los tipos de propiedades, consulte los siguientes recursos en la referencia de la API de REST de Microsoft Graph:</span><span class="sxs-lookup"><span data-stu-id="f9a22-371">For the list of properties and property types, see the following resources in the Microsoft Graph API REST reference:</span></span>

- [<span data-ttu-id="f9a22-372">GET Pages</span><span class="sxs-lookup"><span data-stu-id="f9a22-372">GET Pages</span></span>](/graph/api/page-get?view=graph-rest-1.0)
- [<span data-ttu-id="f9a22-373">GET Sections</span><span class="sxs-lookup"><span data-stu-id="f9a22-373">GET Sections</span></span>](/graph/api/section-get?view=graph-rest-1.0)
- [<span data-ttu-id="f9a22-374">GET SectionGroups</span><span class="sxs-lookup"><span data-stu-id="f9a22-374">GET SectionGroups</span></span>](/graph/api/sectiongroup-get?view=graph-rest-1.0)
- [<span data-ttu-id="f9a22-375">GET Notebooks</span><span class="sxs-lookup"><span data-stu-id="f9a22-375">GET Notebooks</span></span>](/graph/api/notebook-get?view=graph-rest-1.0) 



<span data-ttu-id="f9a22-376">La opción de cadena de consulta **expand** se puede usar con las siguientes propiedades de navegación:</span><span class="sxs-lookup"><span data-stu-id="f9a22-376">The **expand** query string option can be used with the following navigation properties:</span></span>

- <span data-ttu-id="f9a22-377">Páginas: **parentNotebook**, **parentSection**</span><span class="sxs-lookup"><span data-stu-id="f9a22-377">Pages: **parentNotebook**, **parentSection**</span></span>
- <span data-ttu-id="f9a22-378">Secciones: **parentNotebook**, **parentSectionGroup**</span><span class="sxs-lookup"><span data-stu-id="f9a22-378">Sections: **parentNotebook**, **parentSectionGroup**</span></span>
- <span data-ttu-id="f9a22-379">Grupos de secciones: **sections**, **sectionGroups**, **parentNotebook**, **parentSectionGroup**</span><span class="sxs-lookup"><span data-stu-id="f9a22-379">Section groups: **sections**, **sectionGroups**, **parentNotebook**, **parentSectionGroup**</span></span>
- <span data-ttu-id="f9a22-380">Blocs de notas: **sections**, **sectionGroups**</span><span class="sxs-lookup"><span data-stu-id="f9a22-380">Notebooks: **sections**, **sectionGroups**</span></span>


<a name="request-response-info"></a>

## <a name="request-and-response-information-for-get-requests"></a><span data-ttu-id="f9a22-381">Información de la solicitud y respuesta para las solicitudes *GET*</span><span class="sxs-lookup"><span data-stu-id="f9a22-381">Request and response information for *GET* requests</span></span>

| <span data-ttu-id="f9a22-382">Datos de solicitud</span><span class="sxs-lookup"><span data-stu-id="f9a22-382">Request data</span></span> | <span data-ttu-id="f9a22-383">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9a22-383">Description</span></span> |  
|------|------|  
| <span data-ttu-id="f9a22-384">Protocolo</span><span class="sxs-lookup"><span data-stu-id="f9a22-384">Protocol</span></span> | <span data-ttu-id="f9a22-385">Todas las solicitudes usan el protocolo HTTPS SSL/TLS.</span><span class="sxs-lookup"><span data-stu-id="f9a22-385">All requests use the SSL/TLS HTTPS protocol.</span></span> |  
| <span data-ttu-id="f9a22-386">Encabezado Authorization</span><span class="sxs-lookup"><span data-stu-id="f9a22-386">Authorization header</span></span> | <p><span data-ttu-id="f9a22-387">`Bearer {token}`, donde `{token}` es un token de acceso de OAuth 2.0 válido para la aplicación registrada.</span><span class="sxs-lookup"><span data-stu-id="f9a22-387">`Bearer {token}`, where `{token}` is a valid OAuth 2.0 access token for your registered app.</span></span></p><p><span data-ttu-id="f9a22-388">Si falta o no es válido, la solicitud producirá errores con el código de estado 401.</span><span class="sxs-lookup"><span data-stu-id="f9a22-388">If missing or invalid, the request fails with a 401 status code.</span></span> <span data-ttu-id="f9a22-389">Vea [Authentication and permissions](permissions-reference.md) (Autenticación y permisos).</span><span class="sxs-lookup"><span data-stu-id="f9a22-389">See [Authentication and permissions](permissions-reference.md).</span></span></p> |  
| <span data-ttu-id="f9a22-390">Encabezado Accept</span><span class="sxs-lookup"><span data-stu-id="f9a22-390">Accept header</span></span> | <p> <span data-ttu-id="f9a22-391">`application/json` para las entidades y los conjuntos de entidades de OneNote</span><span class="sxs-lookup"><span data-stu-id="f9a22-391">`application/json` for OneNote entities and entity sets</span></span></p><p> <span data-ttu-id="f9a22-392">`text/html` para contenido de la página</span><span class="sxs-lookup"><span data-stu-id="f9a22-392">`text/html` for page content</span></span></p> | 

<br/>

| <span data-ttu-id="f9a22-393">Datos de respuesta</span><span class="sxs-lookup"><span data-stu-id="f9a22-393">Response data</span></span> | <span data-ttu-id="f9a22-394">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9a22-394">Description</span></span> |  
|------|------|  
| <span data-ttu-id="f9a22-395">Código de correcto</span><span class="sxs-lookup"><span data-stu-id="f9a22-395">Success code</span></span> | <span data-ttu-id="f9a22-396">Un código de estado HTTP 200.</span><span class="sxs-lookup"><span data-stu-id="f9a22-396">A 200 HTTP status code.</span></span> |  
| <span data-ttu-id="f9a22-397">Cuerpo de la respuesta</span><span class="sxs-lookup"><span data-stu-id="f9a22-397">Response body</span></span> | <span data-ttu-id="f9a22-398">Una representación de OData de la entidad o entidad establecida en formato JSON, el HTML de la página, o datos binarios recursos de un recurso de archivo.</span><span class="sxs-lookup"><span data-stu-id="f9a22-398">An OData representation of the entity or entity set in JSON format, the page HTML, or file resource binary data.</span></span>  |  
| <span data-ttu-id="f9a22-399">Errores</span><span class="sxs-lookup"><span data-stu-id="f9a22-399">Errors</span></span> | <span data-ttu-id="f9a22-400">Si se produce un error en la solicitud, la API devuelve [errors](onenote-error-codes.md) en el objeto **@api.diagnostics** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f9a22-400">If the request fails, the API returns [errors](onenote-error-codes.md) in the **@api.diagnostics** object in the response body.</span></span> |  
| <span data-ttu-id="f9a22-401">Encabezado X-CorrelationId</span><span class="sxs-lookup"><span data-stu-id="f9a22-401">X-CorrelationId header</span></span> | <span data-ttu-id="f9a22-402">GUID que identifica la solicitud de forma única.</span><span class="sxs-lookup"><span data-stu-id="f9a22-402">A GUID that uniquely identifies the request.</span></span> <span data-ttu-id="f9a22-403">Puede usar este valor junto con el valor del encabezado de fecha al trabajar con el soporte técnico de Microsoft para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="f9a22-403">You can use this value along with the value of the Date header when working with Microsoft support to troubleshoot issues.</span></span> |  


<a name="root-url"></a>

### <a name="constructing-the-microsoft-graph-notes-service-root-url"></a><span data-ttu-id="f9a22-404">Crear la dirección URL raíz del servicio de notas de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="f9a22-404">Constructing the Microsoft Graph notes service root URL</span></span>

<span data-ttu-id="f9a22-405">La dirección URL raíz de notas de Microsoft Graph usa el siguiente formato para todas las llamadas a las notas de Microsoft Graph:</span><span class="sxs-lookup"><span data-stu-id="f9a22-405">The Microsoft Graph notes root URL uses the following format for all calls to Microsoft Graph notes:</span></span>

`https://graph.microsoft.com/{version}/me/onenote/`  

<span data-ttu-id="f9a22-406">El segmento `version` de la URL representa la versión de Microsoft Graph que se quiere utilizar.</span><span class="sxs-lookup"><span data-stu-id="f9a22-406">The `version` segment in the URL represents the version of Microsoft Graph that you want to use.</span></span> <span data-ttu-id="f9a22-407">Use `v1.0` para código de producción estable.</span><span class="sxs-lookup"><span data-stu-id="f9a22-407">Use `v1.0` for stable production code.</span></span> <span data-ttu-id="f9a22-408">Use `beta` para probar una característica que esté en desarrollo.</span><span class="sxs-lookup"><span data-stu-id="f9a22-408">Use `beta` to try out a feature that's in development.</span></span> <span data-ttu-id="f9a22-409">Las características y la funcionalidad de la versión beta pueden cambiar, por lo que no se debe usar en el código de producción.</span><span class="sxs-lookup"><span data-stu-id="f9a22-409">Features and functionality in beta may change, so you shouldn't use it in your production code.</span></span> 

<span data-ttu-id="f9a22-410">Use `me` para contenido de OneNote al que puede obtener acceso el usuario actual (contenido compartido y del que sea propietario).</span><span class="sxs-lookup"><span data-stu-id="f9a22-410">Use `me` for OneNote content that the current user can access (owned and shared).</span></span> <span data-ttu-id="f9a22-411">Use `users/{id}` para contenido de OneNote que el usuario especificado (en la URL) compartió con el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="f9a22-411">Use `users/{id}` for OneNote content that the specified user (in the URL) has shared with the current user.</span></span> <span data-ttu-id="f9a22-412">Use [Microsoft Graph](https://graph.microsoft.com/v1.0/users) para obtener identificadores de usuario.</span><span class="sxs-lookup"><span data-stu-id="f9a22-412">Use [Microsoft Graph](https://graph.microsoft.com/v1.0/users) to get user IDs.</span></span> 


<a name="permissions"></a>

## <a name="permissions-for-get-requests"></a><span data-ttu-id="f9a22-413">Permisos de solicitudes GET</span><span class="sxs-lookup"><span data-stu-id="f9a22-413">Permissions for GET requests</span></span>

<span data-ttu-id="f9a22-414">Para obtener el contenido o la estructura de OneNote, debe solicitar los permisos adecuados.</span><span class="sxs-lookup"><span data-stu-id="f9a22-414">To get OneNote content or structure, you'll need to request appropriate permissions.</span></span> 

<span data-ttu-id="f9a22-415">Los siguientes ámbitos permiten obtener solicitudes a Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="f9a22-415">The following scopes allow GET requests to Microsoft Graph.</span></span> <span data-ttu-id="f9a22-416">Elija el nivel más bajo de permisos que necesita la aplicación para hacer su trabajo.</span><span class="sxs-lookup"><span data-stu-id="f9a22-416">Choose the lowest level of permissions that your app needs to do its work.</span></span>

<span data-ttu-id="f9a22-417">Elija entre:</span><span class="sxs-lookup"><span data-stu-id="f9a22-417">Choose from:</span></span>

- <span data-ttu-id="f9a22-418">Notes.read</span><span class="sxs-lookup"><span data-stu-id="f9a22-418">Notes.read</span></span>
- <span data-ttu-id="f9a22-419">Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f9a22-419">Notes.ReadWrite</span></span>
- <span data-ttu-id="f9a22-420">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f9a22-420">Notes.ReadWrite.All</span></span>

<span data-ttu-id="f9a22-421">Para obtener más información sobre los ámbitos de permiso y cómo funcionan, vea [Referencias de permisos de Microsoft Graph](permissions-reference.md).</span><span class="sxs-lookup"><span data-stu-id="f9a22-421">For more information about permission scopes and how they work, see [Microsoft Graph permissions reference](permissions-reference.md).</span></span>

<a name="see-also"></a>

## <a name="see-also"></a><span data-ttu-id="f9a22-422">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9a22-422">See also</span></span>

- [<span data-ttu-id="f9a22-423">HTML de entrada y salida para páginas de OneNote</span><span class="sxs-lookup"><span data-stu-id="f9a22-423">Input and output HTML for OneNote pages</span></span>](onenote-input-output-html.md)
- [<span data-ttu-id="f9a22-424">Integración con OneNote</span><span class="sxs-lookup"><span data-stu-id="f9a22-424">Integrate with OneNote</span></span>](integrate-with-onenote.md)
- [<span data-ttu-id="f9a22-425">Blog para desarrolladores de OneNote</span><span class="sxs-lookup"><span data-stu-id="f9a22-425">OneNote Developer Blog</span></span>](https://go.microsoft.com/fwlink/?LinkID=390183)
- [<span data-ttu-id="f9a22-426">Preguntas de desarrollo de OneNote en Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="f9a22-426">OneNote development questions on Stack Overflow</span></span>](https://go.microsoft.com/fwlink/?LinkID=390182)
- [<span data-ttu-id="f9a22-427">Repositorios de OneNote en GitHub</span><span class="sxs-lookup"><span data-stu-id="f9a22-427">OneNote GitHub repos</span></span>](https://go.microsoft.com/fwlink/?LinkID=390178)  
