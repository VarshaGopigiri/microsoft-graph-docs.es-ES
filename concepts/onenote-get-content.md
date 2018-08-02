# <a name="get-onenote-content-and-structure-with-microsoft-graph"></a><span data-ttu-id="c7ac4-101">Obtener el contenido y la estructura de OneNote con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="c7ac4-101">Get OneNote content and structure with Microsoft Graph</span></span>

<span data-ttu-id="c7ac4-102">**Se aplica a**: Blocs de notas para consumidores de OneDrive | Blocs de notas empresariales de Office 365</span><span class="sxs-lookup"><span data-stu-id="c7ac4-102">**Applies to:** Consumer notebooks on OneDrive | Enterprise notebooks on Office 365</span></span>

<span data-ttu-id="c7ac4-103">Para obtener la estructura y el contenido de OneNote, envíe una solicitud GET al extremo de destino.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-103">To get OneNote content and structure, you send a GET request to the target endpoint.</span></span> <span data-ttu-id="c7ac4-104">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c7ac4-104">For example:</span></span>

`GET ../onenote/pages/{id}`

<span data-ttu-id="c7ac4-105">Si la solicitud es correcta, Microsoft Graph devuelve un código de estado HTTP 200 y las entidades o el contenido que ha solicitado.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-105">If the request is successful, Microsoft Graph returns a 200 HTTP status code and the entities or content that you requested.</span></span> <span data-ttu-id="c7ac4-106">Las entidades de OneNote se devuelven como objetos JSON que cumplen la especificación de la versión 4.0 de OData.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-106">OneNote entities are returned as JSON objects that conform to the OData version 4.0 specification.</span></span>

<span data-ttu-id="c7ac4-107">Puede filtrar las consultas y mejorar el rendimiento usando las opciones de la cadena de consulta.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-107">By using query string options, you can filter your queries and improve performance.</span></span>


<a name="request-uri"></a>

## <a name="construct-the-request-uri"></a><span data-ttu-id="c7ac4-108">Crear el URI de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c7ac4-108">Construct the request URI</span></span>

<span data-ttu-id="c7ac4-109">Para crear el URI de la solicitud, comience con la dirección URL raíz del servicio:</span><span class="sxs-lookup"><span data-stu-id="c7ac4-109">To construct the request URI, start with the service root URL:</span></span>

`https://graph.microsoft.com/v1.0/me/onenote`

<br/>

<span data-ttu-id="c7ac4-110">Después, anexe el extremo del recurso que desea recuperar.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-110">Then append the endpoint of the resource you want to retrieve.</span></span> <span data-ttu-id="c7ac4-111">([Las rutas de acceso de recursos](#resource-paths-for-get-requests) se muestran en la siguiente sección).</span><span class="sxs-lookup"><span data-stu-id="c7ac4-111">([Resource paths](#resource-paths-for-get-requests) are shown in the next section.)</span></span>

<span data-ttu-id="c7ac4-112">Su URI de solicitud completa tendrá un aspecto similar a uno de estos ejemplos:</span><span class="sxs-lookup"><span data-stu-id="c7ac4-112">Your full request URI will look like one of these examples:</span></span>

- `https://graph.microsoft.com/v1.0/me/onenote/notebooks/{id}/sections`
- `https://graph.microsoft.com/v1.0/me/onenote/notes/pages`
- `https://graph.microsoft.com/v1.0/me/onenote/pages?select=title,self`

> <span data-ttu-id="c7ac4-113">**Nota:** Obtenga más información sobre la [URL de raíz del servicio](../api-reference/v1.0/resources/onenote-api-overview.md#root-url).</span><span class="sxs-lookup"><span data-stu-id="c7ac4-113">**Note:** Learn more about the [service root URL](../api-reference/v1.0/resources/onenote-api-overview.md#root-url).</span></span>

<a name="resource-paths"></a>

## <a name="resource-paths-for-get-requests"></a><span data-ttu-id="c7ac4-114">Rutas de acceso de recursos para las solicitudes GET</span><span class="sxs-lookup"><span data-stu-id="c7ac4-114">Resource paths for GET requests</span></span>

<span data-ttu-id="c7ac4-115">Use las siguientes rutas de acceso de recursos para obtener páginas, secciones, grupos de secciones, blocs de notas, imágenes u otros recursos de archivos.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-115">Use the following resource paths to get pages, sections, section groups, notebooks, and image or file resources.</span></span>

- [<span data-ttu-id="c7ac4-116">Colección de páginas</span><span class="sxs-lookup"><span data-stu-id="c7ac4-116">Page collection</span></span>](#page-collection)
- [<span data-ttu-id="c7ac4-117">Entidad de página</span><span class="sxs-lookup"><span data-stu-id="c7ac4-117">Page entity</span></span>](#page-entity)
- [<span data-ttu-id="c7ac4-118">Vista previa de la página</span><span class="sxs-lookup"><span data-stu-id="c7ac4-118">Page preview</span></span>](#page-preview)
- [<span data-ttu-id="c7ac4-119">Contenido HTML de la página</span><span class="sxs-lookup"><span data-stu-id="c7ac4-119">Page HTML content</span></span>](#page-html-content)
- [<span data-ttu-id="c7ac4-120">Colección de sección</span><span class="sxs-lookup"><span data-stu-id="c7ac4-120">Section collection</span></span>](#section-collection)
- [<span data-ttu-id="c7ac4-121">Entidad de sección</span><span class="sxs-lookup"><span data-stu-id="c7ac4-121">Section entity</span></span>](#section-entity)
- [<span data-ttu-id="c7ac4-122">Colección de SectionGroup</span><span class="sxs-lookup"><span data-stu-id="c7ac4-122">SectionGroup collection</span></span>](#sectiongroup-collection)
- [<span data-ttu-id="c7ac4-123">Entidad de SectionGroup</span><span class="sxs-lookup"><span data-stu-id="c7ac4-123">SectionGroup entity</span></span>](#sectiongroup-entity)
- [<span data-ttu-id="c7ac4-124">Colección de blocs de notas</span><span class="sxs-lookup"><span data-stu-id="c7ac4-124">Notebook collection</span></span>](#notebook-collection)
- [<span data-ttu-id="c7ac4-125">Entidad de bloc de notas</span><span class="sxs-lookup"><span data-stu-id="c7ac4-125">Notebook entity</span></span>](#notebook-entity)
- [<span data-ttu-id="c7ac4-126">Imágenes u otros recursos de archivo</span><span class="sxs-lookup"><span data-stu-id="c7ac4-126">Image or other file resource</span></span>](#image-or-other-file-resource)

<a name="get-pages"></a>

### <a name="page-collection"></a><span data-ttu-id="c7ac4-127">Colección de páginas</span><span class="sxs-lookup"><span data-stu-id="c7ac4-127">Page collection</span></span>

<span data-ttu-id="c7ac4-128">Obtenga páginas (metadatos) en todos los blocs de notas.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-128">Get pages (metadata) across all notebooks</span></span>

`../pages[?filter,orderby,select,expand,top,skip,search,count]`

<br/>

<span data-ttu-id="c7ac4-129">Obtenga páginas (metadatos) de una sección específica.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-129">Get pages (metadata) from a specific section</span></span>

`../sections/{section-id}/pages[?filter,orderby,select,expand,top,skip,search,count,pagelevel]`

<br/>
 
<span data-ttu-id="c7ac4-130">La opción de cadena de consulta `search` solo está disponible para los blocs de notas de clientes.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-130">The `search` query string option is available for consumer notebooks only.</span></span>

<span data-ttu-id="c7ac4-131">El criterio de ordenación predeterminado para páginas es `lastModifiedTime desc`.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-131">The default sort order for pages is `lastModifiedTime desc`.</span></span>

<span data-ttu-id="c7ac4-132">La consulta predeterminada expande la sección principal y selecciona y selecciona las propiedades `id`, `name` y `self` de la sección.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-132">The default query expands the parent section and selects the section's `id`, `name`, and `self` properties.</span></span>

<span data-ttu-id="c7ac4-133">De forma predeterminada, solo se devuelven las 20 entradas principales para las solicitudes *GET pages*.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-133">By default, only the top 20 entries are returned for *GET pages* requests.</span></span> <span data-ttu-id="c7ac4-134">Las solicitudes que no se especifican una opción de cadena de consulta **superior** devuelven un vínculo `@odata.nextLink` en la respuesta que puede usar para obtener las siguientes 20 entradas.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-134">Requests that don't specify a **top** query string option return an `@odata.nextLink` link in the response that you can use to get the next 20 entries.</span></span>

<span data-ttu-id="c7ac4-135">Para la colección de páginas de una sección, use **pagelevel** para obtener el nivel de sangría de las páginas y su orden en la sección.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-135">For the pages collection in a section, use **pagelevel** to return the indentation level of pages and their order within the section.</span></span> 

#### <a name="example"></a><span data-ttu-id="c7ac4-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c7ac4-136">Example</span></span>

`GET ../sections/{section-id}/pages?pagelevel=true`



<a name="get-page"></a> 

### <a name="page-entity"></a><span data-ttu-id="c7ac4-137">Entidad de página</span><span class="sxs-lookup"><span data-stu-id="c7ac4-137">Page entity</span></span>

<span data-ttu-id="c7ac4-138">Obtenga los metadatos de una página específica.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-138">Get the metadata for a specific page.</span></span> 

`../pages/{page-id}[?select,expand,pagelevel]` 

<br/>

<span data-ttu-id="c7ac4-139">Las páginas pueden expandir las propiedades **parentNotebook** y **parentSection**.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-139">Pages can expand the **parentNotebook** and **parentSection** properties.</span></span>

<span data-ttu-id="c7ac4-140">La consulta predeterminada expande la sección principal y selecciona y selecciona las propiedades `id`, `name` y `self` de la sección.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-140">The default query expands the parent section and selects the section's `id`, `name`, and `self` properties.</span></span>

<span data-ttu-id="c7ac4-141">Use **pagelevel** para obtener el nivel de sangría de la página y su orden en la sección principal.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-141">Use **pagelevel** to return the indentation level of the page and its order within its parent section.</span></span> 

#### <a name="example"></a><span data-ttu-id="c7ac4-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c7ac4-142">Example</span></span>

`GET ../pages/{page-id}?pagelevel=true`



<a name="get-page-preview"></a> 

### <a name="page-preview"></a><span data-ttu-id="c7ac4-143">Vista previa de la página</span><span class="sxs-lookup"><span data-stu-id="c7ac4-143">Page preview</span></span>

<span data-ttu-id="c7ac4-144">Obtenga el contenido de vista previa de texto e imágenes de una página.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-144">Get text and image preview content for a page</span></span>

`../pages/{page-id}/preview`

<br/>


<span data-ttu-id="c7ac4-145">La respuesta JSON contiene el contenido de la vista previa, que puede usar para ayudar a los usuarios a identificar los elementos en la página.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-145">The JSON response contains the preview content, which you can use to help users identify what's in the page.</span></span>

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

<span data-ttu-id="c7ac4-146">La propiedad **previewText** contiene un fragmento de texto de la página.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-146">The **previewText** property contains a text snippet from the page.</span></span> <span data-ttu-id="c7ac4-147">Microsoft Graph devuelve frases completas, hasta un máximo de 300 caracteres.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-147">Microsoft Graph returns complete phrases, up to a maximum of 300 characters.</span></span> 

<span data-ttu-id="c7ac4-148">Si la página tiene una imagen que puede usarse para crear una vista previa de la interfaz de usuario, la propiedad **href** en el objeto **previewImageUrl** contiene un vínculo a un [recurso de imagen](#image-or-other-file-resource) público que ya se ha autenticado.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-148">If the page has an image that can be used to build a preview UI, the **href** property in the **previewImageUrl** object contains a link to a public, pre-authenticated [image resource](#image-or-other-file-resource).</span></span> <span data-ttu-id="c7ac4-149">Puede usar este vínculo en HTML.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-149">You can use this link in HTML,</span></span> <span data-ttu-id="c7ac4-150">En caso contrario, **href** devuelve un valor nulo.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-150">Otherwise, **href** returns null.</span></span>

#### <a name="example"></a><span data-ttu-id="c7ac4-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c7ac4-151">Example</span></span> 

`<img src="https://www.onenote.com/api/v1.0/resources/{id}/content?publicAuth=true&mimeType=image/png" />`


<a name="get-page-content"></a> 

### <a name="page-html-content"></a><span data-ttu-id="c7ac4-152">Contenido HTML de la página</span><span class="sxs-lookup"><span data-stu-id="c7ac4-152">Page HTML content</span></span>

<span data-ttu-id="c7ac4-153">Obtenga el contenido HTML de una página.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-153">Get the HTML content of a page </span></span>

`../pages/{page-id}/content[?includeIDs,preAuthenticated]`

<span data-ttu-id="c7ac4-154">(*obtenga más información sobre [ contenido HTML devuelto](onenote_input_output_html.md)*)</span><span class="sxs-lookup"><span data-stu-id="c7ac4-154">(*learn more about [returned HTML content](onenote_input_output_html.md)*)</span></span> 

<br/>

<span data-ttu-id="c7ac4-155">Use la opción de cadena de consulta **includeIDs=true** para obtener ID generadas que se usan para [actualizar la página](onenote_update_page.md).</span><span class="sxs-lookup"><span data-stu-id="c7ac4-155">Use the **includeIDs=true** query string option to get generated IDs used to [update the page](onenote_update_page.md).</span></span>

<span data-ttu-id="c7ac4-156">Use la opción de cadena de consulta **preAuthenticated=true** para obtener las direcciones URL públicas para los [recursos de imagen](#image-or-other-file-resource) que están en la página.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-156">Use the **preAuthenticated=true** query string option to get public URLs to the [image resources](#image-or-other-file-resource) that are on the page.</span></span> <span data-ttu-id="c7ac4-157">Las direcciones URL públicas son válidas durante una hora.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-157">The public URLs are valid for one hour.</span></span> 



<a name="get-sections"></a>

### <a name="section-collection"></a><span data-ttu-id="c7ac4-158">Colección de sección</span><span class="sxs-lookup"><span data-stu-id="c7ac4-158">Section collection</span></span>

<span data-ttu-id="c7ac4-159">Obtenga todas las secciones de todos los blocs de notas que posee el usuario, incluyendo las secciones en grupos de secciones anidados.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-159">Get all sections from all notebooks that are owned by the user, including sections in nested section groups </span></span>

`../sections[?filter,orderby,select,top,skip,expand,count]` 

<br/>

<span data-ttu-id="c7ac4-160">Obtenga todas las secciones que están directamente en un grupo de secciones específico.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-160">Get all sections that are directly under a specific section group</span></span>

`../sectionGroups/{sectiongroup-id}/sections[?filter,orderby,select,top,skip,expand,count]` 

<br/>

<span data-ttu-id="c7ac4-161">Obtenga todas las secciones que están directamente en un bloc de notas específico.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-161">Get all sections that are directly under a specific notebook </span></span>

`../notebooks/{notebook-id}/sections[?filter,orderby,select,top,skip,expand,count]` 

<br/>

<span data-ttu-id="c7ac4-162">Las secciones pueden expandir las propiedades **parentNotebook** y **parentSectionGroup**.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-162">Sections can expand the **parentNotebook** and **parentSectionGroup** properties.</span></span>

<span data-ttu-id="c7ac4-163">El criterio de ordenación predeterminado para secciones es `name asc`.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-163">The default sort order for sections is `name asc`.</span></span>

<span data-ttu-id="c7ac4-164">La consulta predeterminada expande el bloc de notas principal y el grupo de secciones principal y selecciona y selecciona sus propiedades `id`, `name` y `self`.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-164">The default query expands the parent notebook and parent section group and selects their `id`, `name`, and `self` properties.</span></span>



<a name="get-section"></a>

### <a name="section-entity"></a><span data-ttu-id="c7ac4-165">Entidad de sección</span><span class="sxs-lookup"><span data-stu-id="c7ac4-165">Section entity</span></span>

<span data-ttu-id="c7ac4-166">Obtenga una sección específica.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-166">Get a specific section</span></span>

`../sections/{section-id}[?select,expand]` 

<br/>

<span data-ttu-id="c7ac4-167">Las secciones pueden expandir las propiedades **parentNotebook** y **parentSectionGroup**.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-167">Sections can expand the **parentNotebook** and **parentSectionGroup** properties.</span></span>

<span data-ttu-id="c7ac4-168">La consulta predeterminada expande el bloc de notas principal y el grupo de secciones principal y selecciona y selecciona sus propiedades `id`, `name` y `self`.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-168">The default query expands the parent notebook and parent section group and selects their `id`, `name`, and `self` properties.</span></span>



<a name="get-section-groups"></a>

### <a name="sectiongroup-collection"></a><span data-ttu-id="c7ac4-169">Colección de SectionGroup</span><span class="sxs-lookup"><span data-stu-id="c7ac4-169">SectionGroup collection</span></span>

<span data-ttu-id="c7ac4-170">Obtenga todos los grupos de secciones de todos los blocs de notas que posee el usuario, incluyendo los grupos de secciones anidados.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-170">Get all section groups from all notebooks that are owned by the user, including nested section groups</span></span>

`../sectionGroups[?filter,orderby,select,top,skip,expand,count]` 

<br/>

<span data-ttu-id="c7ac4-171">Obtenga todos los grupos de secciones que están directamente en un bloc de notas específico.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-171">Get all section groups that are directly under a specific notebook</span></span> 

`../notebooks/{notebook-id}/sectionGroups[?filter,orderby,select,top,skip,expand,count]` 

<br/>

<span data-ttu-id="c7ac4-172">Los grupos de secciones pueden expandir las propiedades **sections**, **sectionGroups**, **parentNotebook** y **parentSectionGroup**.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-172">Section groups can expand the **sections**, **sectionGroups**, **parentNotebook**, and **parentSectionGroup** properties.</span></span>

<span data-ttu-id="c7ac4-173">El criterio de ordenación predeterminado para grupos de secciones es `name asc`.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-173">The default sort order for section groups is `name asc`.</span></span>

<span data-ttu-id="c7ac4-174">La consulta predeterminada expande el bloc de notas principal y el grupo de secciones principal y selecciona y selecciona sus propiedades `id`, `name` y `self`.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-174">The default query expands the parent notebook and parent section group and selects their `id`, `name`, and `self` properties.</span></span>



<a name="get-section-group"></a>

### <a name="sectiongroup-entity"></a><span data-ttu-id="c7ac4-175">Entidad de SectionGroup</span><span class="sxs-lookup"><span data-stu-id="c7ac4-175">SectionGroup entity</span></span>

<span data-ttu-id="c7ac4-176">Obtenga un grupo de secciones específico.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-176">Get a specific section group</span></span>

`../sectionGroups/{sectiongroup-id}[?select,expand]` 

<br/>

<span data-ttu-id="c7ac4-177">Los grupos de secciones pueden expandir las propiedades **sections**, **sectionGroups**, **parentNotebook** y **parentSectionGroup**.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-177">Section groups can expand the **sections**, **sectionGroups**, **parentNotebook**, and **parentSectionGroup** properties.</span></span>

<span data-ttu-id="c7ac4-178">La consulta predeterminada expande el bloc de notas principal y el grupo de secciones principal y selecciona y selecciona sus propiedades `id`, `name` y `self`.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-178">The default query expands the parent notebook and parent section group and selects their `id`, `name`, and `self` properties.</span></span>



<a name="get-notebooks"></a>

### <a name="notebook-collection"></a><span data-ttu-id="c7ac4-179">Colección de blocs de notas</span><span class="sxs-lookup"><span data-stu-id="c7ac4-179">Notebook collection</span></span>

<span data-ttu-id="c7ac4-180">Obtenga todos los blocs de notas que posee el usuario.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-180">Get all the notebooks that are owned by the user</span></span> 

`../notebooks[?filter,orderby,select,top,skip,expand,count]` 

<br/>

<span data-ttu-id="c7ac4-181">Los blocs de notas pueden expandir las propiedades **sections** y **sectionGroups**.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-181">Notebooks can expand the **sections** and **sectionGroups** properties.</span></span>

<span data-ttu-id="c7ac4-182">El criterio de ordenación predeterminado para blocs de notas es `name asc`.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-182">The default sort order for notebooks is `name asc`.</span></span> 



<a name="get-notebook"></a>

### <a name="notebook-entity"></a><span data-ttu-id="c7ac4-183">Entidad de bloc de notas</span><span class="sxs-lookup"><span data-stu-id="c7ac4-183">Notebook entity</span></span>

<span data-ttu-id="c7ac4-184">Obtenga un bloc de notas específico.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-184">Get a specific notebook </span></span>

`../notebooks/{notebook-id}[?select,expand]` 

<br/>

<span data-ttu-id="c7ac4-185">Los blocs de notas pueden expandir las propiedades **sections** y **sectionGroups**.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-185">Notebooks can expand the **sections** and **sectionGroups** properties.</span></span>



<a name="get-resource"></a>

### <a name="image-or-other-file-resource"></a><span data-ttu-id="c7ac4-186">Imágenes u otros recursos de archivo</span><span class="sxs-lookup"><span data-stu-id="c7ac4-186">Image or other file resource</span></span>

<span data-ttu-id="c7ac4-187">Acceda a los datos binarios de un recurso específico.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-187">Get the binary data of a specific resource</span></span> 

`../resources/{resource-id}/$value` 

<br/>

<span data-ttu-id="c7ac4-188">Puede encontrar el URI del recurso de archivo en el [resultado HTML](onenote_input_output_html.md) de la página.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-188">You can find the file's resource URI in the page's [output HTML](onenote_input_output_html.md).</span></span>

<span data-ttu-id="c7ac4-189">Por ejemplo, una etiqueta **img** incluye extremos del recurso de imagen original en el atributo **data-fullres-src** y de la imagen optimizada en el atributo **src**.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-189">For example, an **img** tag includes endpoints for the original image in the **data-fullres-src** attribute and the optimized image in the **src** attribute.</span></span> 

#### <a name="example"></a><span data-ttu-id="c7ac4-190">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c7ac4-190">Example</span></span>

```html
<img 
    src="https://www.onenote.com/api/v1.0/me/notes/resources/{image-id}/$value"  
    data-src-type="image/png"
    data-fullres-src="https://www.onenote.com/api/v1.0/resources/{image-id}/$value"  
    data-fullres-src-type="image/png" ... />
```

<span data-ttu-id="c7ac4-191">Una etiqueta **object** incluye el extremo del recurso de archivos en el atributo **data**.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-191">And an **object** tag includes the endpoint for the file resource in the **data** attribute.</span></span> 

#### <a name="example"></a><span data-ttu-id="c7ac4-192">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c7ac4-192">Example</span></span>

```html
<object
    data="http://www.onenote.com/api/v1.0/me/notes/resources/{file-id}/$value"
    data-attachment="fileName.pdf" 
    type="application/pdf" ... />
```

<span data-ttu-id="c7ac4-193">Para obtener direcciones URL públicas que ya se han autenticado a los recursos de imagen en una página, incluya `preAuthenticated=true` en la cadena de consulta cuando [recupere el contenido de la página](#page-html-content) (**ejemplo:** `GET ../pages/{page-id}/content?preAuthenticated=true`).</span><span class="sxs-lookup"><span data-stu-id="c7ac4-193">To get public, pre-authenticated URLs to the image resources on a page, include `preAuthenticated=true` in the query string when you [retrieve the page content](#page-html-content) (**example:**  `GET ../pages/{page-id}/content?preAuthenticated=true`).</span></span> <span data-ttu-id="c7ac4-194">Las direcciones URL públicas que se devuelven en el [HTML de salida](onenote_input_output_html.md#output-html-examples-for-images) son válidas durante una hora.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-194">The public URLs that are returned in the [output HTML](onenote_input_output_html.md#output-html-examples-for-images) are valid for one hour.</span></span> <span data-ttu-id="c7ac4-195">Sin esta etiqueta, las imágenes devueltas no se representarán directamente en un explorador porque son privadas y se necesita una autorización para recuperarlas, al igual que el contenido de la página.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-195">Without this flag, retrieved images won't render directly in a browser because they are private and require authorization to retrieve them, like the rest of the page contents.</span></span> 

> <span data-ttu-id="c7ac4-196">**Nota:** no se admite la obtención de una colección de recursos.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-196">**Note:** Getting a collection of resources is not supported.</span></span> 

<span data-ttu-id="c7ac4-197">Cuando obtiene un recurso de archivos, no es necesario incluir un tipo de contenido **Accept** en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-197">When you get a file resource, you don't need to include an **Accept** content type in the request.</span></span>

<span data-ttu-id="c7ac4-198">Para obtener más información sobre las solicitudes GET, consulte los siguientes recursos en la referencia de la API de REST de Microsoft Graph:</span><span class="sxs-lookup"><span data-stu-id="c7ac4-198">For more information about GET requests, see the following resources in the Microsoft Graph API REST reference:</span></span>

- [<span data-ttu-id="c7ac4-199">GET Pages</span><span class="sxs-lookup"><span data-stu-id="c7ac4-199">GET Pages</span></span>](../api-reference/v1.0/api/page_get.md)
- [<span data-ttu-id="c7ac4-200">GET Sections</span><span class="sxs-lookup"><span data-stu-id="c7ac4-200">GET Sections</span></span>](../api-reference/v1.0/api/section_get.md)
- [<span data-ttu-id="c7ac4-201">GET SectionGroups</span><span class="sxs-lookup"><span data-stu-id="c7ac4-201">GET SectionGroups</span></span>](../api-reference/v1.0/api/sectiongroup_get.md)
- [<span data-ttu-id="c7ac4-202">GET Notebooks</span><span class="sxs-lookup"><span data-stu-id="c7ac4-202">GET Notebooks</span></span>](../api-reference/v1.0/api/notebook_get.md) 




<a name="example"></a>

## <a name="example-get-requests"></a><span data-ttu-id="c7ac4-203">Solicitudes GET de ejemplo</span><span class="sxs-lookup"><span data-stu-id="c7ac4-203">Example GET requests</span></span>

<span data-ttu-id="c7ac4-204">Puede consultar las entidades de OneNote y el contenido de la página de búsqueda para obtener solo la información que necesita.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-204">You can query for OneNote entities and search page content to get just the information you need.</span></span> <span data-ttu-id="c7ac4-205">Los siguientes ejemplos muestran algunas formas en las que puede usar [opciones de cadena de consulta compatibles](#supported-odata-query-string-options) en las solicitudes GET a Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-205">The following examples show some ways you can use [supported query string options](#supported-odata-query-string-options) in GET requests to Microsoft Graph.</span></span> 

<span data-ttu-id="c7ac4-206">**Recuerde:**</span><span class="sxs-lookup"><span data-stu-id="c7ac4-206">**Remember:**</span></span>

- <span data-ttu-id="c7ac4-207">Todas las solicitudes GET empiezan con la [dirección URL raíz de servicio](../api-reference/v1.0/resources/onenote-api-overview.md#root-url).</span><span class="sxs-lookup"><span data-stu-id="c7ac4-207">All GET requests start with the [service root URL](../api-reference/v1.0/resources/onenote-api-overview.md#root-url).</span></span> <br/><br/><span data-ttu-id="c7ac4-208">**Ejemplos**: `https://www.onenote.com/api/v1.0/me/notes` y `https://www.onenote.com/api/v1.0/myOrganization/siteCollections/{id}/sites/{id}/notes/`</span><span class="sxs-lookup"><span data-stu-id="c7ac4-208">**Examples**: `https://www.onenote.com/api/v1.0/me/notes` and `https://www.onenote.com/api/v1.0/myOrganization/siteCollections/{id}/sites/{id}/notes/`</span></span>

- <span data-ttu-id="c7ac4-209">Los espacios en la cadena de consulta URL deben usar la codificación %20.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-209">Spaces in the URL query string must use %20 encoding.</span></span><br/><br/><span data-ttu-id="c7ac4-210">**Ejemplo**: `filter=title%20eq%20'biology'`</span><span class="sxs-lookup"><span data-stu-id="c7ac4-210">Example: </span></span>

- <span data-ttu-id="c7ac4-211">Los nombres de propiedad y las comparaciones de cadenas de OData distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-211">Property names and OData string comparisons are case sensitive.</span></span> <span data-ttu-id="c7ac4-212">Se recomienda usar la función **tolower** de OData para comparaciones de cadenas.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-212">We recommend using the OData **tolower** function for string comparisons.</span></span><br/><br/><span data-ttu-id="c7ac4-213">**Ejemplo**: `filter=tolower(name) eq 'spring'`</span><span class="sxs-lookup"><span data-stu-id="c7ac4-213">Example: </span></span>
 

### <a name="search--filter"></a><span data-ttu-id="c7ac4-214">search & filter</span><span class="sxs-lookup"><span data-stu-id="c7ac4-214">search & filter</span></span>  

<span data-ttu-id="c7ac4-215">Obtenga todas las páginas que contienen el término *receta* creadas por una aplicación específica (`search` solo está disponible para blocs de notas de cliente).</span><span class="sxs-lookup"><span data-stu-id="c7ac4-215">Get all pages that contain the term *recipe* that were created by a specific app.</span></span>

```
[GET] ../pages?search=recipe&filter=createdByAppId eq 'WLID-000000004C12821A'
```
 
### <a name="search--select"></a><span data-ttu-id="c7ac4-216">search & select</span><span class="sxs-lookup"><span data-stu-id="c7ac4-216">search & select</span></span>  

<span data-ttu-id="c7ac4-217">Obtenga el título, los vínculos de cliente de OneNote y el vínculo de **contentUrl** para todas las páginas que contienen el término *golgi app* (`search` solo está disponible para blocs de notas de cliente).</span><span class="sxs-lookup"><span data-stu-id="c7ac4-217">Get the title, OneNote client links, and **contentUrl** link for all pages that contain the term *golgi app*.</span></span>

```
[GET] ../pages?search=golgi app&select=title,links,contentUrl
```
 
### <a name="expand"></a><span data-ttu-id="c7ac4-218">expand</span><span class="sxs-lookup"><span data-stu-id="c7ac4-218">expand</span></span> 

<span data-ttu-id="c7ac4-219">Obtenga todos los blocs de notas y expanda sus secciones y grupos de secciones.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-219">Get all notebooks and expand their sections and section groups.</span></span>  

```
[GET] ../notebooks?expand=sections,sectionGroups
```

<br/>

<span data-ttu-id="c7ac4-220">Obtienen un grupo de secciones específico y expanden sus secciones y grupos de secciones.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-220">Get a specific section group and expand its sections and section groups.</span></span>  

```
[GET] ../sectionGroups/{sectiongroup-id}?expand=sections,sectionGroups
```

<br/>

<span data-ttu-id="c7ac4-221">Obtenga una página y expanda su sección principal y bloc de notas principal.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-221">Get a page and expand its parent section and parent notebook.</span></span>

```
[GET] ../pages/{page-id}?expand=parentSection,parentNotebook
```

### <a name="expand-multiple-levels"></a><span data-ttu-id="c7ac4-222">expand (varios niveles)</span><span class="sxs-lookup"><span data-stu-id="c7ac4-222">expand (multiple levels)</span></span>  

<span data-ttu-id="c7ac4-223">Obtenga todos los blocs de notas y expanda sus secciones y grupos de secciones, y expanden todas las secciones en cada grupo de secciones.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-223">Get all notebooks and expand their sections and section groups, and expand all sections in each section group.</span></span>  

```
[GET] ../notebooks?expand=sections,sectionGroups(expand=sections)
```
 
> <span data-ttu-id="c7ac4-224">**Nota:** No se admite expandir elementos primarios de entidades secundarias o expandir elementos secundarios de entidades primarias. Hacer eso crearía una referencia circular.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-224">Expanding parents of child entities or expanding children of parent entities creates a circular reference and is not supported.</span></span>

 
### <a name="expand--select-multiple-levels"></a><span data-ttu-id="c7ac4-225">expand & select (varios niveles)</span><span class="sxs-lookup"><span data-stu-id="c7ac4-225">expand & select (multiple levels)</span></span>  

<span data-ttu-id="c7ac4-226">Obtenga el nombre y el vínculo a **self** para un grupo de secciones específico, y obtenga el nombre y los vínculos a **self** para todas sus secciones.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-226">Get the name and **self** link for a specific section group, and get the name and **self** links for all its sections.</span></span>  

```
[GET] ../sectionGroups/{sectiongroup-id}?expand=sections(select=name,self)&select=name,self
```

<br/>

<span data-ttu-id="c7ac4-227">Obtienen el nombre y el vínculo a **self** para todas las secciones, y obtienen el nombre y la hora de creación del bloc de notas primario de cada sección.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-227">Get the name and **self** link for all sections, and get the name and created time of each section's parent notebook.</span></span>  

```
[GET] ../sections?expand=parentNotebook(select=name,createdTime)&select=name,self
```

<br/>
 
<span data-ttu-id="c7ac4-228">Obtenga el título y el identificador de todas las páginas, y obtenga el nombre de la sección principal y bloc de notas principal.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-228">Get the title and ID for all pages, and get the name of the parent section and parent notebook.</span></span>

```
[GET] ../pages?select=id,title&expand=parentSection(select=name),parentNotebook(select=name)
```

### <a name="expand--levels-multiple-levels"></a><span data-ttu-id="c7ac4-229">expand & levels (varios niveles)</span><span class="sxs-lookup"><span data-stu-id="c7ac4-229">expand & levels (multiple levels)</span></span>  

<span data-ttu-id="c7ac4-230">Obtenga todos los blocs de notas, grupos de secciones y todas las secciones.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-230">Get all notebooks, sections, and section groups.</span></span>  

```
[GET] ../notebooks?expand=sections,sectionGroups(expand=sections,sectionGroups(levels=max;expand=sections))
```
 
### <a name="filter"></a><span data-ttu-id="c7ac4-231">filter</span><span class="sxs-lookup"><span data-stu-id="c7ac4-231">filter</span></span>

<span data-ttu-id="c7ac4-232">Obtenga todas las secciones creadas en octubre de 2014.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-232">Get all sections that were created in October 2014.</span></span>

```
[GET] ../sections?filter=createdTime ge 2014-10-01 and createdTime le 2014-10-31
```

<br/>

<span data-ttu-id="c7ac4-233">Obtenga todas las páginas creadas por una aplicación específica desde el 1 de enero de 2015.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-233">Get the pages that were created by a specific app since January 1, 2015.</span></span>

```
[GET] ../pages?filter=createdByAppId eq 'WLID-0000000048118631' and createdTime ge 2015-01-01
```

### <a name="filter--expand"></a><span data-ttu-id="c7ac4-234">filter & expand</span><span class="sxs-lookup"><span data-stu-id="c7ac4-234">filter & expand</span></span>  

<span data-ttu-id="c7ac4-235">Obtenga todas las páginas de un bloc de notas específico.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-235">Get all pages in a specific notebook.</span></span> <span data-ttu-id="c7ac4-236">La API devuelve 20 entradas de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-236">The API returns 20 entries by default.</span></span>

```
[GET] ../pages?filter=parentNotebook/id eq '{notebook-id}'&expand=parentNotebook
```

<br/>

<span data-ttu-id="c7ac4-237">Obtenga el nombre y el vínculo a **pagesUrl** para todas las secciones del bloc de notas *Escuela*.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-237">Get the name and **pagesUrl** link for all sections from the *School* notebook.</span></span> <span data-ttu-id="c7ac4-238">Las comparaciones de cadenas OData distinguen mayúsculas de minúsculas, por lo que se recomienda usar la función **tolower**.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-238">OData string comparisons are case sensitive, so use the **tolower** function as a best practice.</span></span>

```
[GET] ../notebooks?filter=tolower(name) eq 'school'&expand=sections(select=name,pagesUrl)
```

### <a name="filter--select--orderby"></a><span data-ttu-id="c7ac4-239">filter & select & orderby</span><span class="sxs-lookup"><span data-stu-id="c7ac4-239">filter & select & orderby</span></span>   

<span data-ttu-id="c7ac4-240">Obtenga el nombre y el vínculo a **pagesUrl** para todas las secciones que contienen el término *spring* en el nombre de la sección.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-240">Get the name and **pagesUrl** link for all sections that contain the term *spring* in the section name.</span></span> <span data-ttu-id="c7ac4-241">Ordene las secciones por fecha de última modificación.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-241">Order sections by last modified date.</span></span>

```
[GET] ../sections?filter=contains(tolower(name),'spring')&select=name,pagesUrl&orderby=lastModifiedTime desc
```
 
### <a name="orderby"></a><span data-ttu-id="c7ac4-242">orderby</span><span class="sxs-lookup"><span data-stu-id="c7ac4-242">orderby</span></span>

<span data-ttu-id="c7ac4-243">Obtenga las primeras 20 páginas ordenadas por propiedad **createdByAppId** y luego por fecha de creación más reciente.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-243">Get the first 20 pages ordered by **createdByAppId** property and then by most recent created time.</span></span> <span data-ttu-id="c7ac4-244">La API devuelve 20 entradas de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-244">The API returns 20 entries by default.</span></span>

```
[GET] ../pages?orderby=createdByAppId,createdTime desc
```

### <a name="search--filter--top"></a><span data-ttu-id="c7ac4-245">search & filter & top</span><span class="sxs-lookup"><span data-stu-id="c7ac4-245">search & filter & top</span></span> 

<span data-ttu-id="c7ac4-246">Obtenga las cinco páginas más recientes creadas desde el 1 de enero de 2015, que contienen la frase *división de celda*.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-246">Get the five newest pages created since January 1, 2015 that contain the phrase *cell division*.</span></span> <span data-ttu-id="c7ac4-247">La API devuelve 20 entradas de forma predeterminada con un máximo de 100.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-247">The API returns 20 entries by default with a maximum of 100.</span></span> <span data-ttu-id="c7ac4-248">La ordenación predeterminada para las páginas es `lastModifiedTime desc` (`search` solo está disponible para los blocs de notas de cliente).</span><span class="sxs-lookup"><span data-stu-id="c7ac4-248">The default sort order for pages is `lastModifiedTime desc` (`search` is available for consumer notebooks only).</span></span>

```
[GET] ../pages?search="cell division"&filter=createdTime ge 2015-01-01&top=5
```

### <a name="search--filter--top--skip"></a><span data-ttu-id="c7ac4-249">search & filter & top & skip</span><span class="sxs-lookup"><span data-stu-id="c7ac4-249">search & filter & top & skip</span></span>  

<span data-ttu-id="c7ac4-250">Obtenga las siguientes cinco páginas del conjunto de resultados (`search` solo está disponible para los blocs de notas de cliente).</span><span class="sxs-lookup"><span data-stu-id="c7ac4-250">Get the next five pages in the result set (`search` is available for consumer notebooks only).</span></span>

```
[GET] ../pages?search=biology&filter=createdTime ge 2015-01-01&top=5&skip=5
```

<br/>

<span data-ttu-id="c7ac4-251">Y las cinco siguientes (`search` solo está disponible para los blocs de notas de clientes)</span><span class="sxs-lookup"><span data-stu-id="c7ac4-251">And the next five (`search` is available for consumer notebooks only).</span></span>

```
[GET] ../pages?search=biology&filter=createdTime ge 2015-01-01&top=5&skip=10
```

> <span data-ttu-id="c7ac4-252">**Nota:** Si se aplican **search** y **filter** a la misma solicitud, los resultados incluyen solamente las entidades que coinciden con ambos criterios.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-252">**Note:** If both **search** and **filter** are applied to the same request, the results include only those entities that match both criteria.</span></span>
 
### <a name="select"></a><span data-ttu-id="c7ac4-253">select</span><span class="sxs-lookup"><span data-stu-id="c7ac4-253">select</span></span>

<span data-ttu-id="c7ac4-254">Obtenga el nombre, la hora de creación y el vínculo a **self** para todas las secciones en los blocs de notas del usuario.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-254">Get the name, created time, and **self** link for all sections in the user's notebooks.</span></span>

```
[GET] ../sections?select=name,createdTime,self
```

<br/>

<span data-ttu-id="c7ac4-255">Obtenga el título, la hora de creación y los vínculos a clientes de OneNote para una página específica.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-255">Get the title, created time, and OneNote client links for a specific page.</span></span>

```
[GET] ../pages/{page-id}?select=title,createdTime,links
```

### <a name="select--expand--filter-multiple-levels"></a><span data-ttu-id="c7ac4-256">select & expand & filter (varios niveles)</span><span class="sxs-lookup"><span data-stu-id="c7ac4-256">select & expand & filter (multiple levels)</span></span>  

<span data-ttu-id="c7ac4-257">Obtenga el nombre y el vínculo a **pagesUrl** para todas las secciones en el bloc de notas predeterminado del usuario.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-257">Get the name and **pagesUrl** link for all sections in the user's default notebook.</span></span>

```
[GET] ../notebooks?select=name&expand=sections(select=name,pagesUrl)&filter=isDefault eq true
```

### <a name="top--select--orderby"></a><span data-ttu-id="c7ac4-258">top & select & orderby</span><span class="sxs-lookup"><span data-stu-id="c7ac4-258">top & select & orderby</span></span> 

<span data-ttu-id="c7ac4-259">Obtenga el título y el vínculo **self** de las primeras 50 páginas, ordenadas alfabéticamente por título.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-259">Get the title and **self** link for the first 50 pages, ordered alphabetically by title.</span></span> <span data-ttu-id="c7ac4-260">La API devuelve 20 entradas de forma predeterminada con un máximo de 100.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-260">The API returns 20 entries by default with a maximum of 100.</span></span> <span data-ttu-id="c7ac4-261">El criterio de ordenación predeterminado para páginas es `lastModifiedTime desc`.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-261">The default sort order for pages is `lastModifiedTime desc`.</span></span>

```
[GET] ../pages?top=50&select=title,self&orderby=title
```

### <a name="skip--top--select--orderby"></a><span data-ttu-id="c7ac4-262">skip & top & select & orderby</span><span class="sxs-lookup"><span data-stu-id="c7ac4-262">skip & top & select & orderby</span></span>  

<span data-ttu-id="c7ac4-p117">Obtenga las páginas 51 a 100. La API devuelve 20 entradas de forma predeterminada con un máximo de 100.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-p117">Get pages 51 to 100. The API returns 20 entries by default with a maximum of 100.</span></span>

```
[GET] ../pages?skip=50&top=50&select=title,self&orderby=title
```

> <span data-ttu-id="c7ac4-265">**Note:** Las solicitudes GET para páginas que recuperan el número predeterminado de entradas (es decir, no especifican una expresión **top**) devuelven un vínculo a **@odata.nextLink** en la respuesta que puede usar para obtener las 20 entradas siguientes.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-265">**Note:** GET requests for pages that retrieve the default number of entries (that is, they don't specify a **top** expression) return an **@odata.nextLink** link in the response that you can use to get the next 20 entries.</span></span>
 

<a name="supported-odata-query-string-options"></a>

## <a name="supported-odata-query-string-options"></a><span data-ttu-id="c7ac4-266">Opciones de cadena de consultas OData admitidas</span><span class="sxs-lookup"><span data-stu-id="c7ac4-266">Supported OData query string options</span></span>

<span data-ttu-id="c7ac4-267">Al enviar solicitudes GET a Microsoft Graph, puede usar las opciones de cadena de consultas OData para personalizar la consulta y obtener solo la información que necesita.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-267">When sending GET requests to Microsoft Graph, you can use OData query string options to customize your query and get just the information you need.</span></span> <span data-ttu-id="c7ac4-268">También puede mejorar el rendimiento al reducir el número de llamadas al servicio y el tamaño de la carga de respuesta.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-268">They can also improve performance by reducing the number of calls to the service and the size of the response payload.</span></span>

> <span data-ttu-id="c7ac4-269">**Note:** Para su legibilidad, los ejemplos de este artículo no usan la codificación porcentual de %20 que se requiere para espacios en la cadena de consulta URL: `filter=isDefault%20eq%20true`</span><span class="sxs-lookup"><span data-stu-id="c7ac4-269">**Note:** For readability, the examples in this article don't use the %20 percent-encoding required for spaces in the URL query string: `filter=isDefault%20eq%20true`</span></span>
 
| <span data-ttu-id="c7ac4-270">Opción de consulta</span><span class="sxs-lookup"><span data-stu-id="c7ac4-270">Query option</span></span> | <span data-ttu-id="c7ac4-271">Ejemplo y descripción</span><span class="sxs-lookup"><span data-stu-id="c7ac4-271">Example and description</span></span> |  
|------|------|  
| <span data-ttu-id="c7ac4-272">count</span><span class="sxs-lookup"><span data-stu-id="c7ac4-272">count</span></span> | <p>`count=true`</p><p><span data-ttu-id="c7ac4-p119">El recuento de entidades de la colección. El valor se devuelve en la propiedad **@odata.count** de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-p119">The count of entities in the collection. The value is returned in the **@odata.count** property in the response.</span></span></p> |  
| <span data-ttu-id="c7ac4-275">expand</span><span class="sxs-lookup"><span data-stu-id="c7ac4-275">expand</span></span> | <p>`expand=sections,sectionGroups`</p><p><span data-ttu-id="c7ac4-276">Las propiedades de navegación para devolver la respuesta en línea.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-276">The navigation properties to return inline in the response.</span></span> <span data-ttu-id="c7ac4-277">Las siguientes propiedades son compatibles con las expresiones **expand**:</span><span class="sxs-lookup"><span data-stu-id="c7ac4-277">The following properties are supported for **expand** expressions:</span></span><br /> <span data-ttu-id="c7ac4-278">- Páginas: **parentNotebook**, **parentSection**</span><span class="sxs-lookup"><span data-stu-id="c7ac4-278">- Pages: **parentNotebook**, **parentSection**</span></span><br /> <span data-ttu-id="c7ac4-279">- Secciones: **parentNotebook**, **parentSectionGroup**</span><span class="sxs-lookup"><span data-stu-id="c7ac4-279">- Sections: **parentNotebook**, **parentSectionGroup**</span></span><br /> <span data-ttu-id="c7ac4-280">- Grupos de secciones: **sections**, **sectionGroups**, **parentNotebook**, **parentSectionGroup**</span><span class="sxs-lookup"><span data-stu-id="c7ac4-280">- Section groups: **sections**, **sectionGroups**, **parentNotebook**, **parentSectionGroup**</span></span><br /> <span data-ttu-id="c7ac4-281">- Blocs de notas: **sections**, **sectionGroups**</span><span class="sxs-lookup"><span data-stu-id="c7ac4-281">- Notebooks: **sections**, **sectionGroups**</span></span></p><p><span data-ttu-id="c7ac4-p121">De forma predeterminada, las solicitudes GET para páginas expanden **parentSection** y seleccionan las propiedades **id**, **name** y **self** de la sección. Las solicitudes GET predeterminadas para secciones y grupos de secciones expanden tanto **parentNotebook** como **parentSectionGroup**, y seleccionan las propiedades **id**, **name** y **self** del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-p121">By default, GET requests for pages expands **parentSection** and select the section's **id**, **name**, and **self** properties. Default GET requests for sections and section groups expand both **parentNotebook** and **parentSectionGroup**, and select the parents' **id**, **name**, and **self** properties. </span></span></p><p><span data-ttu-id="c7ac4-284">Puede usarse para una única entidad o una colección.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-284">Can be used for a single entity or a collection.</span></span><br /><span data-ttu-id="c7ac4-285">Separe las distintas propiedades mediante comas.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-285">Separate multiple properties with commas.</span></span><br /><span data-ttu-id="c7ac4-286">Los nombres de las propiedades distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-286">Property names are not case-sensitive</span></span></p> |   
| <span data-ttu-id="c7ac4-287">filter</span><span class="sxs-lookup"><span data-stu-id="c7ac4-287">filter</span></span> | <p>`filter=isDefault eq true`</p><p><span data-ttu-id="c7ac4-288">Una expresión booleana por si desea incluir una entrada en el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-288">A Boolean expression for whether to include an entry in the result set.</span></span> <span data-ttu-id="c7ac4-289">Es compatible con las funciones y operadores de OData siguientes:</span><span class="sxs-lookup"><span data-stu-id="c7ac4-289">Supports the following OData operators and functions:</span></span><br /> <span data-ttu-id="c7ac4-290">- Operadores de comparación: **eq**, **ne**, **gt**, **ge**, **lt**, **le**</span><span class="sxs-lookup"><span data-stu-id="c7ac4-290">- Comparison operators: **eq**, **ne**, **gt**, **ge**, **lt**, **le**</span></span><br /> <span data-ttu-id="c7ac4-291">- Operadores lógicos: **and**, **or**, **not**</span><span class="sxs-lookup"><span data-stu-id="c7ac4-291">- Logical operators: **and**, **or**, **not**</span></span><br /> <span data-ttu-id="c7ac4-292">- Funciones de cadena: **contains**, **endswith**, **startswith**, **length**, **indexof**, **substring**, **tolower**, **toupper**, **trim**, **concat**</span><span class="sxs-lookup"><span data-stu-id="c7ac4-292">- String functions: **contains**, **endswith**, **startswith**, **length**, **indexof**, **substring**, **tolower**, **toupper**, **trim**, **concat**</span></span></p><p><span data-ttu-id="c7ac4-293">[Los nombres de propiedad](#onenote-entity-properties) y las comparaciones de cadenas de OData distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-293">[Property](#onenote-entity-properties) names and OData string comparisons are case sensitive.</span></span> <span data-ttu-id="c7ac4-294">Se recomienda usar la función **tolower** de OData para comparaciones de cadenas.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-294">We recommend using the OData **tolower** function for string comparisons.</span></span><br /><br /><span data-ttu-id="c7ac4-295">**Ejemplo**: `filter=tolower(name) eq 'spring'`</span><span class="sxs-lookup"><span data-stu-id="c7ac4-295">Example: </span></span></p> |  
| <span data-ttu-id="c7ac4-296">orderby</span><span class="sxs-lookup"><span data-stu-id="c7ac4-296">orderby</span></span> | <p>`orderby=title,createdTime desc`</p><p><span data-ttu-id="c7ac4-p124">Las [propiedades](#onenote-entity-properties) según las cuales ordenar, con un **asc** opcional (predeterminado) u orden **desc**. Puede ordenar según cualquier propiedad de la entidad en la colección solicitada.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-p124">The [properties](#onenote-entity-properties) to sort by, with an optional **asc** (default) or **desc** sort order. You can sort by any property of the entity in the requested collection.</span></span></p><p><span data-ttu-id="c7ac4-299">El orden predeterminado para blocs de notas, secciones y grupos de secciones es `name asc`, y para páginas es `lastModifiedTime desc` (última página modificada primero).</span><span class="sxs-lookup"><span data-stu-id="c7ac4-299">The default sort order for notebooks, section groups, and sections is `name asc`, and for pages is `lastModifiedTime desc` (last modified page first).</span></span></p><p><span data-ttu-id="c7ac4-300">Si tiene varias propiedades, sepárelas con comas, y ordénelas de la manera en que desea que se apliquen.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-300">Separate multiple properties with commas, and list them in the order that you want them applied.</span></span> <span data-ttu-id="c7ac4-301">Los nombres de las propiedades distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-301">Property names are not case-sensitive</span></span></p> |  
| <span data-ttu-id="c7ac4-302">buscar</span><span class="sxs-lookup"><span data-stu-id="c7ac4-302">search</span></span> | <p>`search=cell div`</p><p><span data-ttu-id="c7ac4-303">Solo está disponible para los blocs de notas de clientes.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-303">Available for consumer notebooks only.</span></span></p><p><span data-ttu-id="c7ac4-p126">El término o la frase para buscar en el título de la página, el cuerpo de la página, el texto alternativo de la imagen y el texto OCR de la imagen. De forma predeterminada, las consultas de búsqueda devuelven resultados ordenados por relevancia.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-p126">The term or phrase to search for in the page title, page body, image alt text, and image OCR text. By default, search queries return results sorted by relevance.</span></span></p><p><span data-ttu-id="c7ac4-306">OneNote usa la búsqueda de texto completo de Bing para admitir búsqueda de frases, lematización, omisión ortográfica, relevancia y clasificación, separación de palabras, varios idiomas y otras características de búsqueda de texto completo.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-306">OneNote uses Bing full-text search to support phrase search, stemming, spelling forgiveness, relevance and ranking, word breaking, multiple languages, and other full-text search features.</span></span> <span data-ttu-id="c7ac4-307">Las cadenas de búsqueda distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-307">Search strings are case-insensitive.</span></span></p><p><span data-ttu-id="c7ac4-308">Solo se aplica a las páginas de los blocs de notas que posee el usuario.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-308">Applies only to pages in notebooks owned by the user (not shared with the user).</span></span> <span data-ttu-id="c7ac4-309">El contenido indexado es privado y solo puede acceder a él su propietario.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-309">Indexed content is private and can only be accessed by the owner.</span></span> <span data-ttu-id="c7ac4-310">Las páginas protegidas con contraseña no están indexadas.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-310">Password-protected pages are not indexed.</span></span> <span data-ttu-id="c7ac4-311">Solo se aplica al extremo `pages`.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-311">Applies only to the `pages` endpoint.</span></span></p> |  
| <span data-ttu-id="c7ac4-312">select</span><span class="sxs-lookup"><span data-stu-id="c7ac4-312">select</span></span> | <p>`select=id,title`</p><p><span data-ttu-id="c7ac4-313">Las [propiedades](#onenote-entity-properties) que se devuelven.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-313">The [properties](#onenote-entity-properties) to return.</span></span> <span data-ttu-id="c7ac4-314">Puede usarse para una única entidad o para una colección.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-314">Can be used for a single entity or for a collection.</span></span> <span data-ttu-id="c7ac4-315">Separe las distintas propiedades mediante comas.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-315">Separate multiple properties with commas.</span></span> <span data-ttu-id="c7ac4-316">Los nombres de las propiedades distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-316">Property names are not case-sensitive</span></span></p> |  
| <span data-ttu-id="c7ac4-317">skip</span><span class="sxs-lookup"><span data-stu-id="c7ac4-317">skip</span></span> | <p>`skip=10`</p><p><span data-ttu-id="c7ac4-318">El número de entradas que se omiten del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-318">The number of entries to skip in the result set.</span></span> <span data-ttu-id="c7ac4-319">Se usa normalmente para los resultados de paginación.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-319">Typically used for paging results.</span></span></p> |  
| <span data-ttu-id="c7ac4-320">top</span><span class="sxs-lookup"><span data-stu-id="c7ac4-320">top</span></span> | <p>`top=50`</p><p><span data-ttu-id="c7ac4-321">El número de entradas para devolver en el conjunto de resultados, hasta un máximo de 100.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-321">The number of entries to return in the result set, up to a maximum of 100.</span></span> <span data-ttu-id="c7ac4-322">El valor predeterminado es 20.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-322">The default value is 20.</span></span></p> |  

<span data-ttu-id="c7ac4-323">Microsoft Graph también proporciona la opción de cadena de consulta `pagelevel` que puede usar para obtener el nivel y el orden de las páginas en la sección principal.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-323">Microsoft Graph also provides the `pagelevel` query string option you can use to get the level and order of pages within the parent section.</span></span> <span data-ttu-id="c7ac4-324">Solo se aplica a las consultas para las páginas de una sección específica o para una página específica.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-324">Applies only to queries for pages in a specific section or queries for a specific page.</span></span> 

#### <a name="examples"></a><span data-ttu-id="c7ac4-325">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c7ac4-325">Examples</span></span> 

- `GET ../sections/{section-id}/pages?pagelevel=true` 
- `GET ../pages/{page-id}?pagelevel=true` 

### <a name="supported-odata-operators-and-functions"></a><span data-ttu-id="c7ac4-326">Operadores y funciones OData compatibles</span><span class="sxs-lookup"><span data-stu-id="c7ac4-326">Supported OData operators and functions</span></span>

<span data-ttu-id="c7ac4-327">Microsoft Graph admite los siguientes operadores y funciones OData en las expresiones **filter**.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-327">Microsoft Graph supports the following OData operators and functions in **filter** expressions.</span></span> <span data-ttu-id="c7ac4-328">Al usar expresiones OData, recuerde:</span><span class="sxs-lookup"><span data-stu-id="c7ac4-328">When using OData expressions, remember:</span></span>

- <span data-ttu-id="c7ac4-329">Debe reemplazar los espacios en la cadena de consulta URL con la codificación `%20`.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-329">Spaces in the URL query string must be replaced with the `%20` encoding.</span></span><br/><br/><span data-ttu-id="c7ac4-330">**Ejemplo:** `filter=isDefault%20eq%20true`</span><span class="sxs-lookup"><span data-stu-id="c7ac4-330">**Example:** `filter=isDefault%20eq%20true`</span></span>

- <span data-ttu-id="c7ac4-331">Los nombres de propiedad y las comparaciones de cadenas de OData distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-331">Property names and OData string comparisons are case sensitive.</span></span> <span data-ttu-id="c7ac4-332">Se recomienda usar la función **tolower** de OData para comparaciones de cadenas.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-332">We recommend using the OData **tolower** function for string comparisons.</span></span><br/><br/><span data-ttu-id="c7ac4-333">**Ejemplo:** `filter=tolower(name) eq 'spring'`</span><span class="sxs-lookup"><span data-stu-id="c7ac4-333">**Example:** `filter=tolower(name) eq 'spring'`</span></span>


| <span data-ttu-id="c7ac4-334">Operador de comparación</span><span class="sxs-lookup"><span data-stu-id="c7ac4-334">Comparison operator</span></span> | <span data-ttu-id="c7ac4-335">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c7ac4-335">Example</span></span> |  
|------|------|  
| <span data-ttu-id="c7ac4-336">eq</span><span class="sxs-lookup"><span data-stu-id="c7ac4-336">eq</span></span><br /><span data-ttu-id="c7ac4-337">(igual a)</span><span class="sxs-lookup"><span data-stu-id="c7ac4-337">(equal to)</span></span> | `createdByAppId eq '{app-id}'` |  
| <span data-ttu-id="c7ac4-338">ne</span><span class="sxs-lookup"><span data-stu-id="c7ac4-338">ne</span></span><br /><span data-ttu-id="c7ac4-339">(no es igual a)</span><span class="sxs-lookup"><span data-stu-id="c7ac4-339">(not equal to)</span></span> | `userRole ne 'Owner'` |  
| <span data-ttu-id="c7ac4-340">gt</span><span class="sxs-lookup"><span data-stu-id="c7ac4-340">gt</span></span><br /><span data-ttu-id="c7ac4-341">(mayor que)</span><span class="sxs-lookup"><span data-stu-id="c7ac4-341">(greater than)</span></span> | `createdTime gt 2014-02-23` |  
| <span data-ttu-id="c7ac4-342">ge</span><span class="sxs-lookup"><span data-stu-id="c7ac4-342">ge</span></span><br /><span data-ttu-id="c7ac4-343">(mayor o igual que)</span><span class="sxs-lookup"><span data-stu-id="c7ac4-343">(greater than or equal to)</span></span> | `lastModifiedTime ge 2014-05-05T07:00:00Z` |  
| <span data-ttu-id="c7ac4-344">lt</span><span class="sxs-lookup"><span data-stu-id="c7ac4-344">lt</span></span><br /><span data-ttu-id="c7ac4-345">(menor que)</span><span class="sxs-lookup"><span data-stu-id="c7ac4-345">(less than)</span></span> | `createdTime lt 2014-02-23` |  
| <span data-ttu-id="c7ac4-346">le</span><span class="sxs-lookup"><span data-stu-id="c7ac4-346">le</span></span><br /><span data-ttu-id="c7ac4-347">(menor que o igual que)</span><span class="sxs-lookup"><span data-stu-id="c7ac4-347">(less than or equal to)</span></span> | `lastModifiedTime le 2014-02-23` |  

<br/>

| <span data-ttu-id="c7ac4-348">Operador lógico</span><span class="sxs-lookup"><span data-stu-id="c7ac4-348">Logical operator</span></span> | <span data-ttu-id="c7ac4-349">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c7ac4-349">Example</span></span> |  
|------|------|  
| <span data-ttu-id="c7ac4-350">y</span><span class="sxs-lookup"><span data-stu-id="c7ac4-350">and</span></span> | `createdTime le 2014-01-30 and createdTime gt 2014-01-23` |  
| <span data-ttu-id="c7ac4-351">o</span><span class="sxs-lookup"><span data-stu-id="c7ac4-351">or</span></span> | `createdByAppId eq '{app-id}' or createdByAppId eq '{app-id}'` |  
| <span data-ttu-id="c7ac4-352">
not</span><span class="sxs-lookup"><span data-stu-id="c7ac4-352">not</span></span> | `not contains(tolower(title),'school')` |  

<br/>
  
| <span data-ttu-id="c7ac4-353">Función String</span><span class="sxs-lookup"><span data-stu-id="c7ac4-353">String function</span></span> | <span data-ttu-id="c7ac4-354">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c7ac4-354">Example</span></span> |  
|------|------|   
| <span data-ttu-id="c7ac4-355">contains</span><span class="sxs-lookup"><span data-stu-id="c7ac4-355">contains</span></span> | `contains(tolower(title),'spring')` |  
| <span data-ttu-id="c7ac4-356">endswith</span><span class="sxs-lookup"><span data-stu-id="c7ac4-356">endswith</span></span> | `endswith(tolower(title),'spring')` |  
| <span data-ttu-id="c7ac4-357">startswith</span><span class="sxs-lookup"><span data-stu-id="c7ac4-357">startswith</span></span> | `startswith(tolower(title),'spring')` |  
| <span data-ttu-id="c7ac4-358">length</span><span class="sxs-lookup"><span data-stu-id="c7ac4-358">length</span></span> | `length(title) eq 19` |  
| <span data-ttu-id="c7ac4-359">indexof</span><span class="sxs-lookup"><span data-stu-id="c7ac4-359">indexof</span></span> | `indexof(tolower(title),'spring') eq 1` |  
| <span data-ttu-id="c7ac4-360">substring</span><span class="sxs-lookup"><span data-stu-id="c7ac4-360">substring</span></span> | `substring(tolower(title),1) eq 'spring'` |  
| <span data-ttu-id="c7ac4-361">tolower</span><span class="sxs-lookup"><span data-stu-id="c7ac4-361">tolower</span></span> | `tolower(title) eq 'spring'` |  
| <span data-ttu-id="c7ac4-362">toupper</span><span class="sxs-lookup"><span data-stu-id="c7ac4-362">toupper</span></span> | `toupper(title) eq 'SPRING'` |  
| <span data-ttu-id="c7ac4-363">trim</span><span class="sxs-lookup"><span data-stu-id="c7ac4-363">trim</span></span> | `trim(tolower(title)) eq 'spring'` |  
| <span data-ttu-id="c7ac4-364">concat</span><span class="sxs-lookup"><span data-stu-id="c7ac4-364">concat</span></span> | `concat(title,'- by MyRecipesApp') eq 'Carrot Cake Recipe - by MyRecipesApp'` |  
 

<a name="properties"></a>

## <a name="onenote-entity-properties"></a><span data-ttu-id="c7ac4-365">Propiedades de entidad de OneNote</span><span class="sxs-lookup"><span data-stu-id="c7ac4-365">OneNote entity properties</span></span>

<span data-ttu-id="c7ac4-366">Las expresiones de consulta **filter**, **select**, **expand** y **orderby** pueden incluir propiedades de las entidades de OneNote.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-366">The **filter**, **select**, **expand**, and **orderby** query expressions can include properties of OneNote entities.</span></span> 

#### <a name="example"></a><span data-ttu-id="c7ac4-367">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c7ac4-367">Example</span></span>

`../sections?filter=createdTime ge 2015-01-01&select=name,pagesUrl&orderby=lastModifiedTime desc` 

<span data-ttu-id="c7ac4-368">Los nombres de las propiedades distinguen mayúsculas de minúsculas en las expresiones de consulta.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-368">Property names are case sensitive in query expressions.</span></span>

<span data-ttu-id="c7ac4-369">Para obtener la lista de propiedades y los tipos de propiedades, consulte los siguientes recursos en la referencia de la API de REST de Microsoft Graph:</span><span class="sxs-lookup"><span data-stu-id="c7ac4-369">For the list of properties and property types, see the following resources in the Microsoft Graph API REST reference:</span></span>

- [<span data-ttu-id="c7ac4-370">GET Pages</span><span class="sxs-lookup"><span data-stu-id="c7ac4-370">GET Pages</span></span>](../api-reference/v1.0/api/page_get.md)
- [<span data-ttu-id="c7ac4-371">GET Sections</span><span class="sxs-lookup"><span data-stu-id="c7ac4-371">GET Sections</span></span>](../api-reference/v1.0/api/section_get.md)
- [<span data-ttu-id="c7ac4-372">GET SectionGroups</span><span class="sxs-lookup"><span data-stu-id="c7ac4-372">GET SectionGroups</span></span>](../api-reference/v1.0/api/sectiongroup_get.md)
- [<span data-ttu-id="c7ac4-373">GET Notebooks</span><span class="sxs-lookup"><span data-stu-id="c7ac4-373">GET Notebooks</span></span>](../api-reference/v1.0/api/notebook_get.md) 



<span data-ttu-id="c7ac4-374">La opción de cadena de consulta **expand** se puede usar con las siguientes propiedades de navegación:</span><span class="sxs-lookup"><span data-stu-id="c7ac4-374">The **expand** query string option can be used with the following navigation properties:</span></span>

- <span data-ttu-id="c7ac4-375">Páginas: **parentNotebook**, **parentSection**</span><span class="sxs-lookup"><span data-stu-id="c7ac4-375">Pages: **parentNotebook**, **parentSection**</span></span>
- <span data-ttu-id="c7ac4-376">Secciones: **parentNotebook**, **parentSectionGroup**</span><span class="sxs-lookup"><span data-stu-id="c7ac4-376">Sections: **parentNotebook**, **parentSectionGroup**</span></span>
- <span data-ttu-id="c7ac4-377">Grupos de secciones: **sections**, **sectionGroups**, **parentNotebook**, **parentSectionGroup**</span><span class="sxs-lookup"><span data-stu-id="c7ac4-377">Section groups: **sections**, **sectionGroups**, **parentNotebook**, **parentSectionGroup**</span></span>
- <span data-ttu-id="c7ac4-378">Blocs de notas: **sections**, **sectionGroups**</span><span class="sxs-lookup"><span data-stu-id="c7ac4-378">Notebooks: **sections**, **sectionGroups**</span></span>


<a name="request-response-info"></a>

## <a name="request-and-response-information-for-get-requests"></a><span data-ttu-id="c7ac4-379">Información de la solicitud y respuesta para las solicitudes *GET*</span><span class="sxs-lookup"><span data-stu-id="c7ac4-379">Request and response information for *GET* requests</span></span>

| <span data-ttu-id="c7ac4-380">Datos de solicitud</span><span class="sxs-lookup"><span data-stu-id="c7ac4-380">Request data</span></span> | <span data-ttu-id="c7ac4-381">Descripción</span><span class="sxs-lookup"><span data-stu-id="c7ac4-381">Description</span></span> |  
|------|------|  
| <span data-ttu-id="c7ac4-382">Protocolo</span><span class="sxs-lookup"><span data-stu-id="c7ac4-382">Protocol</span></span> | <span data-ttu-id="c7ac4-383">Todas las solicitudes usan el protocolo HTTPS SSL/TLS.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-383">All requests use the SSL/TLS HTTPS protocol.</span></span> |  
| <span data-ttu-id="c7ac4-384">Encabezado Authorization</span><span class="sxs-lookup"><span data-stu-id="c7ac4-384">Authorization header</span></span> | <p><span data-ttu-id="c7ac4-385">`Bearer {token}`, donde `{token}` es un token de acceso de OAuth 2.0 válido para la aplicación registrada.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-385">`Bearer {token}`, where `{token}` is a valid OAuth 2.0 access token for your registered app.</span></span></p><p><span data-ttu-id="c7ac4-386">Si falta o no es válido, la solicitud producirá errores con el código de estado 401.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-386">If missing or invalid, the request fails with a 401 status code.</span></span> <span data-ttu-id="c7ac4-387">Vea [Authentication and permissions](permissions_reference.md) (Autenticación y permisos).</span><span class="sxs-lookup"><span data-stu-id="c7ac4-387">See [Authentication and permissions](permissions_reference.md).</span></span></p> |  
| <span data-ttu-id="c7ac4-388">Encabezado Accept</span><span class="sxs-lookup"><span data-stu-id="c7ac4-388">Accept header</span></span> | <p> <span data-ttu-id="c7ac4-389">`application/json` para las entidades y los conjuntos de entidades de OneNote</span><span class="sxs-lookup"><span data-stu-id="c7ac4-389">`application/json` for OneNote entities and entity sets</span></span></p><p> <span data-ttu-id="c7ac4-390">`text/html` para contenido de la página</span><span class="sxs-lookup"><span data-stu-id="c7ac4-390">`text/html` for page content</span></span></p> | 

<br/>

| <span data-ttu-id="c7ac4-391">Datos de respuesta</span><span class="sxs-lookup"><span data-stu-id="c7ac4-391">Response data</span></span> | <span data-ttu-id="c7ac4-392">Descripción</span><span class="sxs-lookup"><span data-stu-id="c7ac4-392">Description</span></span> |  
|------|------|  
| <span data-ttu-id="c7ac4-393">Código de correcto</span><span class="sxs-lookup"><span data-stu-id="c7ac4-393">Success code</span></span> | <span data-ttu-id="c7ac4-394">Un código de estado HTTP 200.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-394">A 200 HTTP status code.</span></span> |  
| <span data-ttu-id="c7ac4-395">Cuerpo de la respuesta</span><span class="sxs-lookup"><span data-stu-id="c7ac4-395">Response body</span></span> | <span data-ttu-id="c7ac4-396">Una representación de OData de la entidad o entidad establecida en formato JSON, el HTML de la página, o datos binarios recursos de un recurso de archivo.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-396">An OData representation of the entity or entity set in JSON format, the page HTML, or file resource binary data.</span></span>  |  
| <span data-ttu-id="c7ac4-397">Errores</span><span class="sxs-lookup"><span data-stu-id="c7ac4-397">Errors</span></span> | <span data-ttu-id="c7ac4-398">Si se produce un error en la solicitud, la API devuelve [errors](onenote_error_codes.md) en el objeto **@api.diagnostics** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-398">If the request fails, the API returns [errors](onenote_error_codes.md) in the **@api.diagnostics** object in the response body.</span></span> |  
| <span data-ttu-id="c7ac4-399">Encabezado X-CorrelationId</span><span class="sxs-lookup"><span data-stu-id="c7ac4-399">X-CorrelationId header</span></span> | <span data-ttu-id="c7ac4-400">GUID que identifica la solicitud de forma única.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-400">A GUID that uniquely identifies the request.</span></span> <span data-ttu-id="c7ac4-401">Puede usar este valor junto con el valor del encabezado de fecha al trabajar con el soporte técnico de Microsoft para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-401">You can use this value along with the value of the Date header when working with Microsoft support to troubleshoot issues.</span></span> |  


<a name="root-url"></a>

### <a name="constructing-the-microsoft-graph-notes-service-root-url"></a><span data-ttu-id="c7ac4-402">Crear la dirección URL raíz del servicio de notas de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="c7ac4-402">Constructing the Microsoft Graph notes service root URL</span></span>

<span data-ttu-id="c7ac4-403">La dirección URL raíz de notas de Microsoft Graph usa el siguiente formato para todas las llamadas a las notas de Microsoft Graph:</span><span class="sxs-lookup"><span data-stu-id="c7ac4-403">The Microsoft Graph notes root URL uses the following format for all calls to Microsoft Graph notes.</span></span>

`https://graph.microsoft.com/{version}/me/onenote/`  

<span data-ttu-id="c7ac4-404">El segmento `version` de la URL representa la versión de Microsoft Graph que se quiere utilizar.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-404">The `version` segment in the URL represents the version of Microsoft Graph that you want to use.</span></span> <span data-ttu-id="c7ac4-405">Use `v1.0` para código de producción estable.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-405">Use `v1.0` for stable production code.</span></span> <span data-ttu-id="c7ac4-406">Use `beta` para probar una característica que esté en desarrollo.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-406">Use `beta` to try out a feature that's in development.</span></span> <span data-ttu-id="c7ac4-407">Las características y la funcionalidad de la versión beta pueden cambiar, por lo que no se debe usar en el código de producción.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-407">Features and functionality in beta may change, so you shouldn't use it in your production code.</span></span> 

<span data-ttu-id="c7ac4-408">Use `me` para contenido de OneNote al que puede obtener acceso el usuario actual (contenido compartido y del que sea propietario).</span><span class="sxs-lookup"><span data-stu-id="c7ac4-408">Use `me` for OneNote content that the current user can access (owned and shared).</span></span> <span data-ttu-id="c7ac4-409">Use `users/{id}` para contenido de OneNote que el usuario especificado (en la URL) compartió con el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-409">Use `users/{id}` for OneNote content that the specified user (in the URL) has shared with the current user.</span></span> <span data-ttu-id="c7ac4-410">Use [Microsoft Graph](https://graph.microsoft.com/v1.0/users) para obtener identificadores de usuario.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-410">Use the [Microsoft Graph](https://graph.microsoft.com/v1.0/users) to get user IDs.</span></span> 


<a name="permissions"></a>

## <a name="permissions-for-get-requests"></a><span data-ttu-id="c7ac4-411">Permisos de solicitudes GET</span><span class="sxs-lookup"><span data-stu-id="c7ac4-411">Permissions for GET requests</span></span>

<span data-ttu-id="c7ac4-412">Para obtener el contenido o la estructura de OneNote, debe solicitar los permisos adecuados.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-412">To get OneNote content or structure, you'll need to request appropriate permissions.</span></span> 

<span data-ttu-id="c7ac4-413">Los siguientes ámbitos permiten obtener solicitudes a Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-413">The following scopes allow GET requests to Microsoft Graph.</span></span> <span data-ttu-id="c7ac4-414">Elija el nivel más bajo de permisos que necesita la aplicación para hacer su trabajo.</span><span class="sxs-lookup"><span data-stu-id="c7ac4-414">Choose the lowest level of permissions that your app needs to do its work.</span></span>

<span data-ttu-id="c7ac4-415">Elija entre:</span><span class="sxs-lookup"><span data-stu-id="c7ac4-415">Choose from:</span></span>

- <span data-ttu-id="c7ac4-416">Notes.read</span><span class="sxs-lookup"><span data-stu-id="c7ac4-416">Notes.read</span></span>
- <span data-ttu-id="c7ac4-417">Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c7ac4-417">Notes.ReadWrite</span></span>
- <span data-ttu-id="c7ac4-418">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c7ac4-418">Notes.ReadWrite.All</span></span>

<span data-ttu-id="c7ac4-419">Para obtener más información sobre los ámbitos de permiso y cómo funcionan, vea [Referencias de permisos de Microsoft Graph](permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c7ac4-419">For more information about permission scopes and how they work, see [Microsoft Graph permissions reference](permissions_reference.md).</span></span>

<a name="see-also"></a>

## <a name="see-also"></a><span data-ttu-id="c7ac4-420">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7ac4-420">See also</span></span>

- [<span data-ttu-id="c7ac4-421">HTML de entrada y salida para páginas de OneNote</span><span class="sxs-lookup"><span data-stu-id="c7ac4-421">Input and output HTML for OneNote pages</span></span>](onenote_input_output_html.md)
- [<span data-ttu-id="c7ac4-422">Integración con OneNote</span><span class="sxs-lookup"><span data-stu-id="c7ac4-422">Integrate with OneNote</span></span>](integrate_with_onenote.md)
- [<span data-ttu-id="c7ac4-423">Blog para desarrolladores de OneNote</span><span class="sxs-lookup"><span data-stu-id="c7ac4-423">OneNote Developer Blog</span></span>](http://go.microsoft.com/fwlink/?LinkID=390183)
- [<span data-ttu-id="c7ac4-424">Preguntas de desarrollo de OneNote en Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="c7ac4-424">OneNote development questions on Stack Overflow</span></span>](http://go.microsoft.com/fwlink/?LinkID=390182)
- [<span data-ttu-id="c7ac4-425">Repositorios de OneNote en GitHub</span><span class="sxs-lookup"><span data-stu-id="c7ac4-425">OneNote GitHub repos</span></span>](http://go.microsoft.com/fwlink/?LinkID=390178)  
