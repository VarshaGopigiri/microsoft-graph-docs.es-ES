# <a name="get-onenote-content-and-structure-with-microsoft-graph"></a><span data-ttu-id="3a599-101">Obtener el contenido y la estructura de OneNote con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="3a599-101">Get OneNote content and structure with Microsoft Graph</span></span>

<span data-ttu-id="3a599-102">*__Se aplica a:__ blocs de notas para consumidores de OneDrive | blocs de notas para empresa de Office 365*</span><span class="sxs-lookup"><span data-stu-id="3a599-102">*__Applies to:__ Consumer notebooks on OneDrive | Enterprise notebooks on Office 365*</span></span>

<span data-ttu-id="3a599-103">Para obtener la estructura y el contenido de OneNote, envíe una solicitud GET al extremo de destino.</span><span class="sxs-lookup"><span data-stu-id="3a599-103">To get OneNote content and structure, you send a GET request to the target endpoint.</span></span> <span data-ttu-id="3a599-104">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="3a599-104">For example:</span></span>

`GET ../onenote/pages/{id}`</p>

<span data-ttu-id="3a599-105">Si la solicitud es correcta, Microsoft Graph devuelve un código de estado HTTP 200 y las entidades o el contenido que ha solicitado.</span><span class="sxs-lookup"><span data-stu-id="3a599-105">If the request is successful, Microsoft Graph returns a 200 HTTP status code and the entities or content that you requested.</span></span> <span data-ttu-id="3a599-106">Las entidades de OneNote se devuelven como objetos JSON que cumplen la especificación de la versión 4.0 de OData.</span><span class="sxs-lookup"><span data-stu-id="3a599-106">OneNote entities are returned as JSON objects that conform to the OData version 4.0 specification.</span></span>

<span data-ttu-id="3a599-107">Puede filtrar las consultas y mejorar el rendimiento usando las opciones de la cadena de consulta.</span><span class="sxs-lookup"><span data-stu-id="3a599-107">By using query string options, you can filter your queries and improve performance.</span></span>


<a name="request-uri"></a>
## <a name="construct-the-request-uri"></a><span data-ttu-id="3a599-108">Crear el URI de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3a599-108">Construct the request</span></span>

<span data-ttu-id="3a599-109">Para crear el URI de la solicitud, comience con la dirección URL raíz del servicio:</span><span class="sxs-lookup"><span data-stu-id="3a599-109">To construct the request URI, start with the service root URL:</span></span>

`https://graph.microsoft.com/v1.0/me/onenote`

<span data-ttu-id="3a599-110">Después, anexe el extremo del recurso que desea recuperar.</span><span class="sxs-lookup"><span data-stu-id="3a599-110">Then append the endpoint of the resource you want to retrieve.</span></span> <span data-ttu-id="3a599-111">([Las rutas de acceso de recursos](#resource-paths-for-get-requests) se muestran en la siguiente sección).</span><span class="sxs-lookup"><span data-stu-id="3a599-111">([Resource paths](#resource-paths-for-get-requests) are shown in the next section.)</span></span>


<span data-ttu-id="3a599-112">Su URI de solicitud completa tendrá un aspecto similar a uno de estos ejemplos:</span><span class="sxs-lookup"><span data-stu-id="3a599-112">Your full request URI will look like one of these examples:</span></span>
- `https://graph.microsoft.com/v1.0/me/onenote/notebooks/{id}/sections`</p>
- `https://graph.microsoft.com/v1.0/me/onenote/notes/pages`</p>
- `https://graph.microsoft.com/v1.0/me/onenote/pages?select=title,self`</p>

> <span data-ttu-id="3a599-113">**Nota:** Obtenga más información sobre la [URL de raíz del servicio](../api-reference/v1.0/resources/onenote-api-overview.md#root-url).</span><span class="sxs-lookup"><span data-stu-id="3a599-113">**Note:** Learn more about the [service root URL](../api-reference/v1.0/resources/onenote-api-overview.md#root-url).</span></span>

<a name="resource-paths"></a>
## <a name="resource-paths-for-get-requests"></a><span data-ttu-id="3a599-114">Rutas de acceso de recursos para las solicitudes GET</span><span class="sxs-lookup"><span data-stu-id="3a599-114">Resource paths for GET requests</span></span>

<span data-ttu-id="3a599-115">Use las siguientes rutas de acceso de recursos para obtener páginas, secciones, grupos de secciones, blocs de notas, imágenes u otros recursos de archivos.</span><span class="sxs-lookup"><span data-stu-id="3a599-115">Use the following resource paths to get pages, sections, section groups, notebooks, and image or file resources.</span></span>

<span data-ttu-id="3a599-116">[Colección de páginas](#page-collection)&nbsp;&nbsp;|&nbsp;&nbsp;[Entidad de página](#page-entity)&nbsp;&nbsp;|&nbsp;&nbsp;[Vista previa de página](#page-preview)&nbsp;&nbsp;|&nbsp;&nbsp;[Contenido HTML de página](#page-html-content)&nbsp;&nbsp;|&nbsp;&nbsp; [Colección de secciones](#section-collection)&nbsp;&nbsp;|&nbsp;&nbsp;[Entidad de sección](#section-entity)&nbsp;&nbsp;|&nbsp;&nbsp;[Colección de SectionGroup](#sectiongroup-collection)&nbsp;&nbsp;|&nbsp;&nbsp; [Entidad de SectionGroup](#sectiongroup-entity)&nbsp;&nbsp;|&nbsp;&nbsp;[Colección de blocs de notas](#notebook-collection)&nbsp;&nbsp;|&nbsp;&nbsp;[Entidad de bloc de notas](#notebook-entity)&nbsp;&nbsp;|&nbsp;&nbsp; [Imagen u otro recurso de archivo](#image-or-other-file-resource)</span><span class="sxs-lookup"><span data-stu-id="3a599-116">[Page collection](#page-collection)&nbsp;&nbsp;|&nbsp;&nbsp;[Page entity](#page-entity)&nbsp;&nbsp;|&nbsp;&nbsp;[Page preview](#page-preview)&nbsp;&nbsp;|&nbsp;&nbsp;[Page HTML content](#page-html-content)&nbsp;&nbsp;|&nbsp;&nbsp; [Section collection](#section-collection)&nbsp;&nbsp;|&nbsp;&nbsp;[Section entity](#section-entity)&nbsp;&nbsp;|&nbsp;&nbsp;[SectionGroup collection](#sectiongroup-collection)&nbsp;&nbsp;|&nbsp;&nbsp; [SectionGroup entity](#sectiongroup-entity)&nbsp;&nbsp;|&nbsp;&nbsp;[Notebook collection](#notebook-collection)&nbsp;&nbsp;|&nbsp;&nbsp;[Notebook entity](#notebook-entity)&nbsp;&nbsp;|&nbsp;&nbsp; [Image or other file resource](#image-or-other-file-resource)</span></span>

<a name="get-pages"></a>
### <a name="page-collection"></a><span data-ttu-id="3a599-117">Colección de páginas</span><span class="sxs-lookup"><span data-stu-id="3a599-117">Page collection</span></span>

<span data-ttu-id="3a599-118">Obtener páginas (metadatos) en todos los blocs de notas</span><span class="sxs-lookup"><span data-stu-id="3a599-118">Get pages (metadata) across all notebooks</span></span>

`../pages[?filter,orderby,select,expand,top,skip,search,count]`

<span data-ttu-id="3a599-119">Obtener páginas (metadatos) de una sección específica</span><span class="sxs-lookup"><span data-stu-id="3a599-119">Get pages (metadata) from a specific section</span></span>

`../sections/{section-id}/pages[?filter,orderby,select,expand,top,skip,search,count,pagelevel]`

 
<span data-ttu-id="3a599-120">La opción de cadena de consulta `search` solo está disponible para los blocs de notas de clientes.</span><span class="sxs-lookup"><span data-stu-id="3a599-120">The `search` query string option is available for consumer notebooks only.</span></span>

<span data-ttu-id="3a599-121">El criterio de ordenación predeterminado para páginas es `lastModifiedTime desc`.</span><span class="sxs-lookup"><span data-stu-id="3a599-121">The default sort order is `lastModifiedTime desc`.</span></span>

<span data-ttu-id="3a599-122">La consulta predeterminada expande la sección principal y selecciona y selecciona las propiedades `id`, `name` y `self` de la sección.</span><span class="sxs-lookup"><span data-stu-id="3a599-122">The default query expands the parent section and selects the section's `id`, `name`, and `self` properties.</span></span>

<span data-ttu-id="3a599-123">De forma predeterminada, solo se devuelven las 20 entradas principales para las solicitudes *GET pages*.</span><span class="sxs-lookup"><span data-stu-id="3a599-123">By default, only the top 20 entries are returned for *GET pages* requests.</span></span> <span data-ttu-id="3a599-124">Las solicitudes que no se especifican una opción de cadena de consulta **superior** devuelven un vínculo **@odata.nextLink** en la respuesta que puede usar para obtener las siguientes 20 entradas.</span><span class="sxs-lookup"><span data-stu-id="3a599-124">GET requests for pages that retrieve the default number of entries (that is, they don’t specify a top expression) return an @odata.nextLink link in the response that you can use to get the next 20 entries.</span></span>

<span data-ttu-id="3a599-125">Para la colección de páginas de una sección, use **pagelevel** para obtener el nivel de sangría de las páginas y su orden en la sección.</span><span class="sxs-lookup"><span data-stu-id="3a599-125">For the pages collection in a section, use **pagelevel** to return the indentation level of pages and their order within the section.</span></span> 

<span data-ttu-id="3a599-126">**Ejemplo:** `GET ../sections/{section-id}/pages?pagelevel=true`.  </span><span class="sxs-lookup"><span data-stu-id="3a599-126">Example</span></span>

- - -

<a name="get-page"></a> 
### <a name="page-entity"></a><span data-ttu-id="3a599-127">Entidad de página</span><span class="sxs-lookup"><span data-stu-id="3a599-127">Page entity</span></span>

<span data-ttu-id="3a599-128">Obtenga los metadatos de una página específica.</span><span class="sxs-lookup"><span data-stu-id="3a599-128">Get the metadata for a folder.</span></span> 

`../pages/{page-id}[?select,expand,pagelevel]` 


<span data-ttu-id="3a599-129">Las páginas pueden expandir las propiedades **parentNotebook** y **parentSection**.</span><span class="sxs-lookup"><span data-stu-id="3a599-129">Pages can expand the **parentNotebook** and **parentSection** properties.</span></span>

<span data-ttu-id="3a599-130">La consulta predeterminada expande la sección principal y selecciona y selecciona las propiedades `id`, `name` y `self` de la sección.</span><span class="sxs-lookup"><span data-stu-id="3a599-130">The default query expands the parent section and selects the section's `id`, `name`, and `self` properties.</span></span>

<span data-ttu-id="3a599-131">Use **pagelevel** para obtener el nivel de sangría de la página y el su orden en la sección principal.</span><span class="sxs-lookup"><span data-stu-id="3a599-131">Use **pagelevel** to return the indentation level of the page and its order within its parent section.</span></span> <span data-ttu-id="3a599-132">Ejemplo: `GET ../pages/{page-id}?pagelevel=true`.</span><span class="sxs-lookup"><span data-stu-id="3a599-132">Example: `GET ../pages/{page-id}?pagelevel=true`.</span></span>

- - -

<a name="get-page-preview"></a> 
### <a name="page-preview"></a><span data-ttu-id="3a599-133">Vista previa de la página</span><span class="sxs-lookup"><span data-stu-id="3a599-133">Page break preview.</span></span>

<span data-ttu-id="3a599-134">Obtener el contenido de vista previa de texto e imágenes de una página</span><span class="sxs-lookup"><span data-stu-id="3a599-134">Get text and image preview content for a page</span></span>

`../pages/{page-id}/preview`


<span data-ttu-id="3a599-135">La respuesta JSON contiene el contenido de la vista previa, que puede usar para ayudar a los usuarios a identificar los elementos en la página.</span><span class="sxs-lookup"><span data-stu-id="3a599-135">The JSON response contains the preview content, which you can use to help users identify what's in the page.</span></span>

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

<span data-ttu-id="3a599-136">La propiedad **previewText** contiene un fragmento de texto de la página.</span><span class="sxs-lookup"><span data-stu-id="3a599-136">The **previewText** property contains a text snippet from the page.</span></span> <span data-ttu-id="3a599-137">Microsoft Graph devuelve frases completas, hasta un máximo de 300 caracteres.</span><span class="sxs-lookup"><span data-stu-id="3a599-137">Microsoft Graph returns complete phrases, up to a maximum of 300 characters.</span></span> 

<span data-ttu-id="3a599-138">Si la página tiene una imagen que puede usarse para crear una vista previa de la interfaz de usuario, la propiedad **href** en el objeto **previewImageUrl** contiene un vínculo a un [recurso de imagen](#image-or-other-file-resource) público que ya se ha autenticado.</span><span class="sxs-lookup"><span data-stu-id="3a599-138">If the page has an image that can be used to build a preview UI, the **href** property in the **previewImageUrl** object contains a link to a public, pre-authenticated [image resource](#image-or-other-file-resource).</span></span> <span data-ttu-id="3a599-139">Puede usar este vínculo en HTML,</span><span class="sxs-lookup"><span data-stu-id="3a599-139">You can use this link in HTML,</span></span>

<span data-ttu-id="3a599-140">**Ejemplo:** `<img src="https://www.onenote.com/api/v1.0/resources/{id}/content?publicAuth=true&mimeType=image/png" />`.</span><span class="sxs-lookup"><span data-stu-id="3a599-140">Example</span></span> <span data-ttu-id="3a599-141">En caso contrario, **href** devuelve un valor nulo.</span><span class="sxs-lookup"><span data-stu-id="3a599-141">Otherwise, **href** returns null.</span></span>

- - -

<a name="get-page-content"></a> 
### <a name="page-html-content"></a><span data-ttu-id="3a599-142">Contenido HTML de página</span><span class="sxs-lookup"><span data-stu-id="3a599-142">Page HTML content</span></span>

<span data-ttu-id="3a599-143">Obtener el contenido HTML de una página `../pages/{page-id}/content[?includeIDs,preAuthenticated]`</span><span class="sxs-lookup"><span data-stu-id="3a599-143">Get the HTML content of a page `../pages/{page-id}/content[?includeIDs,preAuthenticated]`</span></span>

<span data-ttu-id="3a599-144">(*obtenga más información sobre [ contenido HTML devuelto](onenote_input_output_html.md)*)</span><span class="sxs-lookup"><span data-stu-id="3a599-144">(*learn more about [returned HTML content](onenote_input_output_html.md)*)</span></span> 

 
<span data-ttu-id="3a599-145">Use la opción de cadena de consulta **includeIDs=true** para obtener ID generadas que se usan para [actualizar la página](onenote_update_page.md).</span><span class="sxs-lookup"><span data-stu-id="3a599-145">Use the **includeIDs=true** query string option to get generated IDs used to [update the page](onenote_update_page.md).</span></span>

<span data-ttu-id="3a599-146">Use la opción de cadena de consulta **preAuthenticated=true** para obtener las direcciones URL públicas para los [recursos de imagen](#image-or-other-file-resource) que están en la página.</span><span class="sxs-lookup"><span data-stu-id="3a599-146">Use the **preAuthenticated=true** query string option to get public URLs to the [image resources](#image-or-other-file-resource) that are on the page.</span></span> <span data-ttu-id="3a599-147">Las direcciones URL públicas son válidas durante una hora.</span><span class="sxs-lookup"><span data-stu-id="3a599-147">The public URLs that are returned are valid for one hour.</span></span> 

- - -

<a name="get-sections"></a>
### <a name="section-collection"></a><span data-ttu-id="3a599-148">Colección de sitios</span><span class="sxs-lookup"><span data-stu-id="3a599-148">Section collection</span></span>

<span data-ttu-id="3a599-149">Obtener todas las secciones de todos los blocs de notas que posee el usuario, incluyendo las secciones en grupos de secciones anidados `../sections[?filter,orderby,select,top,skip,expand,count]`</span><span class="sxs-lookup"><span data-stu-id="3a599-149">Get all sections from all notebooks that are owned by the user, including sections in nested section groups `../sections[?filter,orderby,select,top,skip,expand,count]`</span></span> 

<span data-ttu-id="3a599-150">Obtener todas las secciones que están directamente en un grupo de secciones específico</span><span class="sxs-lookup"><span data-stu-id="3a599-150">Get all sections that are directly under a specific section group</span></span>

`../sectionGroups/{sectiongroup-id}/sections[?filter,orderby,select,top,skip,expand,count]` 

<span data-ttu-id="3a599-151">Obtener todas las secciones que están directamente en un bloc de notas específico `../notebooks/{notebook-id}/sections[?filter,orderby,select,top,skip,expand,count]`</span><span class="sxs-lookup"><span data-stu-id="3a599-151">Get all sections that are directly under a specific notebook `../notebooks/{notebook-id}/sections[?filter,orderby,select,top,skip,expand,count]`</span></span> 

 
<span data-ttu-id="3a599-152">Las secciones pueden expandir las propiedades **parentNotebook** y **parentSectionGroup**.</span><span class="sxs-lookup"><span data-stu-id="3a599-152">Sections can expand the **parentNotebook** and **parentSectionGroup** properties.</span></span>

<span data-ttu-id="3a599-153">El criterio de ordenación predeterminado para secciones es `name asc`.</span><span class="sxs-lookup"><span data-stu-id="3a599-153">The default sort order is `name asc`.</span></span>

<span data-ttu-id="3a599-154">La consulta predeterminada expande el bloc de notas principal y el grupo de secciones principal y selecciona y selecciona sus propiedades `id`, `name` y `self`.</span><span class="sxs-lookup"><span data-stu-id="3a599-154">The default query expands the parent notebook and parent section group and selects their `id`, `name`, and `self` properties.</span></span>

- - -

<a name="get-section"></a>
### <a name="section-entity"></a><span data-ttu-id="3a599-155">Entidad de sección</span><span class="sxs-lookup"><span data-stu-id="3a599-155">Section entity</span></span>

<span data-ttu-id="3a599-156">Obtener una sección específica</span><span class="sxs-lookup"><span data-stu-id="3a599-156">Get a specific entity</span></span>

`../sections/{section-id}[?select,expand]` 

 
<span data-ttu-id="3a599-157">Las secciones pueden expandir las propiedades **parentNotebook** y **parentSectionGroup**.</span><span class="sxs-lookup"><span data-stu-id="3a599-157">Sections can expand the **parentNotebook** and **parentSectionGroup** properties.</span></span>

<span data-ttu-id="3a599-158">La consulta predeterminada expande el bloc de notas principal y el grupo de secciones principal y selecciona y selecciona sus propiedades `id`, `name` y `self`.</span><span class="sxs-lookup"><span data-stu-id="3a599-158">The default query expands the parent notebook and parent section group and selects their `id`, `name`, and `self` properties.</span></span>

- - -

<a name="get-section-groups"></a>
### <a name="sectiongroup-collection"></a><span data-ttu-id="3a599-159">Colección de SectionGroup</span><span class="sxs-lookup"><span data-stu-id="3a599-159">SectionGroup collection</span></span>

<span data-ttu-id="3a599-160">Obtener todos los grupos secciones de todos los blocs de notas que posee el usuario, incluyendo los grupos de secciones anidados</span><span class="sxs-lookup"><span data-stu-id="3a599-160">Get all section groups from all notebooks that are owned by the user, including nested section groups</span></span>

`../sectionGroups[?filter,orderby,select,top,skip,expand,count]` 

<span data-ttu-id="3a599-161">Obtener todos los grupos de secciones que están directamente en un bloc de notas específico</span><span class="sxs-lookup"><span data-stu-id="3a599-161">Get all section groups that are directly under a specific notebook</span></span> 

`../notebooks/{notebook-id}/sectionGroups[?filter,orderby,select,top,skip,expand,count]` 

<span data-ttu-id="3a599-162">Los grupos de secciones pueden expandir las propiedades **sections**, **sectionGroups**, **parentNotebook** y **parentSectionGroup**.</span><span class="sxs-lookup"><span data-stu-id="3a599-162">Section groups can expand the **sections**, **sectionGroups**, **parentNotebook**, and **parentSectionGroup** properties.</span></span>

<span data-ttu-id="3a599-163">El criterio de ordenación predeterminado para grupos de secciones es `name asc`.</span><span class="sxs-lookup"><span data-stu-id="3a599-163">The default sort order for section groups is `name asc`.</span></span>

<span data-ttu-id="3a599-164">La consulta predeterminada expande el bloc de notas principal y el grupo de secciones principal y selecciona y selecciona sus propiedades `id`, `name` y `self`.</span><span class="sxs-lookup"><span data-stu-id="3a599-164">The default query expands the parent notebook and parent section group and selects their `id`, `name`, and `self` properties.</span></span>

- - -

<a name="get-section-group"></a>
### <a name="sectiongroup-entity"></a><span data-ttu-id="3a599-165">Entidad de SectionGroup</span><span class="sxs-lookup"><span data-stu-id="3a599-165">SectionGroup entity</span></span>

<span data-ttu-id="3a599-166">Obtener un grupo de secciones específico</span><span class="sxs-lookup"><span data-stu-id="3a599-166">Get a specific section group and expand its sections and section groups.</span></span>

`../sectionGroups/{sectiongroup-id}[?select,expand]` 


<span data-ttu-id="3a599-167">Los grupos de secciones pueden expandir las propiedades **sections**, **sectionGroups**, **parentNotebook** y **parentSectionGroup**.</span><span class="sxs-lookup"><span data-stu-id="3a599-167">Section groups can expand the **sections**, **sectionGroups**, **parentNotebook**, and **parentSectionGroup** properties.</span></span>

<span data-ttu-id="3a599-168">La consulta predeterminada expande el bloc de notas principal y el grupo de secciones principal y selecciona y selecciona sus propiedades `id`, `name` y `self`.</span><span class="sxs-lookup"><span data-stu-id="3a599-168">The default query expands the parent notebook and parent section group and selects their `id`, `name`, and `self` properties.</span></span>

- - -

<a name="get-notebooks"></a>
### <a name="notebook-collection"></a><span data-ttu-id="3a599-169">Colección de blocs de notas</span><span class="sxs-lookup"><span data-stu-id="3a599-169">notebook collection</span></span>

<span data-ttu-id="3a599-170">Obtener todos los blocs de notas que posee el usuario</span><span class="sxs-lookup"><span data-stu-id="3a599-170">Get all the notebooks that are owned by the user</span></span> 

`../notebooks[?filter,orderby,select,top,skip,expand,count]` 

 
<span data-ttu-id="3a599-171">Los blocs de notas pueden expandir las propiedades **sections** y **sectionGroups**.</span><span class="sxs-lookup"><span data-stu-id="3a599-171">Notebooks can expand the **sections** and **sectionGroups** properties.</span></span>

<span data-ttu-id="3a599-172">El criterio de ordenación predeterminado para blocs de notas es `name asc`.</span><span class="sxs-lookup"><span data-stu-id="3a599-172">The default sort order is `name asc`.</span></span> 

- - -

<a name="get-notebook"></a>
### <a name="notebook-entity"></a><span data-ttu-id="3a599-173">Entidad de bloc de notas</span><span class="sxs-lookup"><span data-stu-id="3a599-173">Notebook entity</span></span>

<span data-ttu-id="3a599-174">Obtener un bloc de notas específico `../notebooks/{notebook-id}[?select,expand]`</span><span class="sxs-lookup"><span data-stu-id="3a599-174">Get a specific notebook `../notebooks/{notebook-id}[?select,expand]`</span></span> 


<span data-ttu-id="3a599-175">Los blocs de notas pueden expandir las propiedades **sections** y **sectionGroups**.</span><span class="sxs-lookup"><span data-stu-id="3a599-175">Notebooks can expand the **sections** and **sectionGroups** properties.</span></span>

- - -

<a name="get-resource"></a>
### <a name="image-or-other-file-resource"></a><span data-ttu-id="3a599-176">Imágenes u otros recursos de archivo</span><span class="sxs-lookup"><span data-stu-id="3a599-176">Image or other file resource</span></span>

<span data-ttu-id="3a599-177">Acceder a los datos binarios de un recurso específico</span><span class="sxs-lookup"><span data-stu-id="3a599-177">Get the binary data of a specific resource by sending a GET request to the resource's  endpoint:</span></span> 

`../resources/{resource-id}/$value` 


<span data-ttu-id="3a599-178">Puede encontrar el URI del recurso de archivo en el [resultado HTML](onenote_input_output_html.md) de la página.</span><span class="sxs-lookup"><span data-stu-id="3a599-178">You can find the file's resource URI in the page's [output HTML](onenote_input_output_html.md).</span></span>

<span data-ttu-id="3a599-179">Por ejemplo, una etiqueta **img** incluye extremos del recurso de imagen original en el atributo **data-fullres-src** y de la imagen optimizada en el atributo **src**.</span><span class="sxs-lookup"><span data-stu-id="3a599-179">In the page HTML, an **** tag includes endpoints for the original image resource in the **** attribute and the optimized image in the **** attribute:</span></span> 

<span data-ttu-id="3a599-180">**Ejemplo:**</span><span class="sxs-lookup"><span data-stu-id="3a599-180">**Example**</span></span>

```
<img 
    src="https://www.onenote.com/api/v1.0/me/notes/resources/{image-id}/$value"  
    data-src-type="image/png"
    data-fullres-src="https://www.onenote.com/api/v1.0/resources/{image-id}/$value"  
    data-fullres-src-type="image/png" ... />
```

<span data-ttu-id="3a599-181">Una etiqueta **object** incluye el extremo del recurso de archivos en el atributo **data**.</span><span class="sxs-lookup"><span data-stu-id="3a599-181">And an **object** tag includes the endpoint for the file resource in the **data** attribute.</span></span> 

<span data-ttu-id="3a599-182">**Ejemplo:**</span><span class="sxs-lookup"><span data-stu-id="3a599-182">**Example**</span></span>

```
<object
    data="http://www.onenote.com/api/v1.0/me/notes/resources/{file-id}/$value"
    data-attachment="fileName.pdf" 
    type="application/pdf" ... />
```

<span data-ttu-id="3a599-183">Para obtener direcciones URL públicas que ya se han autenticado a los recursos de imagen en una página, incluya **preAuthenticated=true** en la cadena de consulta cuando [recupere el contenido de la página](#page-html-content) (**ejemplo:** `GET ../pages/{page-id}/content?preAuthenticated=true`).</span><span class="sxs-lookup"><span data-stu-id="3a599-183">To get public URLs to the image resources on a page, include preAuthenticated=true in the query string when you retrieve the page content (example: ).</span></span> <span data-ttu-id="3a599-184">Las direcciones URL públicas que se devuelven en el [HTML de salida](onenote_input_output_html.md#output-html-examples-for-images) son válidas durante una hora.</span><span class="sxs-lookup"><span data-stu-id="3a599-184">The public URLs that are returned are valid for one hour.</span></span> <span data-ttu-id="3a599-185">Sin esta etiqueta, las imágenes devueltas no se representarán directamente en un explorador porque son privadas y se necesita una autorización para recuperarlas, al igual que el contenido de la página.</span><span class="sxs-lookup"><span data-stu-id="3a599-185">By default, images won't render directly in a browser because they are private and require authorization to retrieve them, like the rest of the page contents.</span></span> 

> <span data-ttu-id="3a599-186">**Nota:** no se admite la obtención de una colección de recursos.</span><span class="sxs-lookup"><span data-stu-id="3a599-186">**Note:** Getting a collection of resources is not supported.</span></span> 

<span data-ttu-id="3a599-187">Cuando obtiene un recurso de archivos, no es necesario incluir un tipo de contenido **Accept** en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3a599-187">When you get a file resource, you don't need to include an **Accept** content type in the request.</span></span>

<span data-ttu-id="3a599-188">Para obtener más información sobre las solicitudes GET, consulte:</span><span class="sxs-lookup"><span data-stu-id="3a599-188">For more information about GET requests, see:</span></span> 
- [<span data-ttu-id="3a599-189">GET Pages</span><span class="sxs-lookup"><span data-stu-id="3a599-189">Get pages</span></span>](../api-reference/v1.0/api/page_get.md)
- [<span data-ttu-id="3a599-190">GET Sections</span><span class="sxs-lookup"><span data-stu-id="3a599-190">GET sections</span></span>](../api-reference/v1.0/api/section_get.md)
- [<span data-ttu-id="3a599-191">GET SectionGroups</span><span class="sxs-lookup"><span data-stu-id="3a599-191">GET sectiongroups</span></span>](../api-reference/v1.0/api/sectiongroup_get.md)
- [<span data-ttu-id="3a599-192">GET Notebooks</span><span class="sxs-lookup"><span data-stu-id="3a599-192">GET notebooks</span></span>](../api-reference/v1.0/api/notebook_get.md) 

<span data-ttu-id="3a599-193">en la referencia de la API de REST de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="3a599-193">in the Microsoft Graph API REST reference.</span></span>


<a name="example"></a>
## <a name="example-get-requests"></a><span data-ttu-id="3a599-194">Solicitudes GET de ejemplo</span><span class="sxs-lookup"><span data-stu-id="3a599-194">Example GET requests</span></span>
<span data-ttu-id="3a599-195">Puede consultar las entidades de OneNote y el contenido de la página de búsqueda para obtener solo la información que necesita.</span><span class="sxs-lookup"><span data-stu-id="3a599-195">You can query for OneNote entities and search page content to get just the information you need.</span></span> <span data-ttu-id="3a599-196">Los siguientes ejemplos muestran algunas formas en las que puede usar [opciones de cadena de consulta compatibles](#supported-odata-query-string-options) en las solicitudes GET a Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="3a599-196">The following examples show some ways you can use [supported query string options](#supported-odata-query-string-options) in GET requests to Microsoft Graph.</span></span> 

<span data-ttu-id="3a599-197">**Recuerde:**</span><span class="sxs-lookup"><span data-stu-id="3a599-197">**Remember:**</span></span>

- <span data-ttu-id="3a599-198">Todas las solicitudes GET empiezan con la [dirección URL raíz de servicio](../api-reference/v1.0/resources/onenote-api-overview.md#root-url).</span><span class="sxs-lookup"><span data-stu-id="3a599-198">All GET requests start with the service root URL, for example:</span></span>

  <span data-ttu-id="3a599-199">**Ejemplos:**</span><span class="sxs-lookup"><span data-stu-id="3a599-199">**Examples**</span></span> 
  - `https://www.onenote.com/api/v1.0/me/notes`
  - `https://www.onenote.com/api/v1.0/myOrganization/siteCollections/{id}/sites/{id}/notes/`

- <span data-ttu-id="3a599-200">Los espacios en la cadena de consulta URL deben usar la codificación %20.</span><span class="sxs-lookup"><span data-stu-id="3a599-200">Spaces in the URL query string must be replaced with  the %20 encoding. Example:  filter=isDefault%20eq%20true</span></span>

<span data-ttu-id="3a599-201">Ejemplo: `filter=title%20eq%20'biology'`</span><span class="sxs-lookup"><span data-stu-id="3a599-201">Example: `filter=title%20eq%20'biology'`</span></span>

- <span data-ttu-id="3a599-202">Los nombres de propiedad y las comparaciones de cadenas de OData distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3a599-202">Property names and OData string comparisons are case sensitive.</span></span> <span data-ttu-id="3a599-203">Se recomienda usar la función **tolower** de OData para comparaciones de cadenas.</span><span class="sxs-lookup"><span data-stu-id="3a599-203">Property names and OData string comparisons are case sensitive. We recommend using the OData **tolower** function for string comparisons. Example: filter=tolower(name) eq 'spring'</span></span>

   <span data-ttu-id="3a599-204">Ejemplo: `filter=tolower(name) eq 'spring'`</span><span class="sxs-lookup"><span data-stu-id="3a599-204">Example: `filter=tolower(name) eq 'spring'`</span></span>
 

<span data-ttu-id="3a599-205">**search & filter**</span><span class="sxs-lookup"><span data-stu-id="3a599-205">**search & filter**</span></span>  

<span data-ttu-id="3a599-206">Obtienen todas las páginas que contienen el término *receta* creadas por una aplicación específica.</span><span class="sxs-lookup"><span data-stu-id="3a599-206">Get all pages that contain the term *recipe* that were created by a specific app.</span></span>  <span data-ttu-id="3a599-207">(`search` solo está disponible para los blocs de notas de clientes)</span><span class="sxs-lookup"><span data-stu-id="3a599-207">(`search` is available for consumer notebooks only)</span></span>

```
[GET] ../pages?search=recipe&filter=createdByAppId eq 'WLID-000000004C12821A'
```
 
<span data-ttu-id="3a599-208">**search & select**</span><span class="sxs-lookup"><span data-stu-id="3a599-208">**search & select**</span></span>  

<span data-ttu-id="3a599-209">Obtienen el título, los vínculos de cliente de OneNote y el vínculo de **contentUrl** para todas las páginas que contienen el término *golgi app*.</span><span class="sxs-lookup"><span data-stu-id="3a599-209">Get the title, oncshort client links, and contentUrl link for all pages that contain the term golgi app.</span></span>  <span data-ttu-id="3a599-210">(`search` solo está disponible para los blocs de notas de clientes)</span><span class="sxs-lookup"><span data-stu-id="3a599-210">(`search` is available for consumer notebooks only)</span></span>

```
[GET] ../pages?search=golgi app&select=title,links,contentUrl
```
 
<span data-ttu-id="3a599-211">**expand**</span><span class="sxs-lookup"><span data-stu-id="3a599-211">**expand**</span></span>  

<span data-ttu-id="3a599-212">Obtienen todos los blocs de notas y expanden sus secciones y grupos de secciones.</span><span class="sxs-lookup"><span data-stu-id="3a599-212">Get all notebooks and expand their sections and section groups.</span></span>  

```
[GET] ../notebooks?expand=sections,sectionGroups
```
 
<span data-ttu-id="3a599-213">Obtienen un grupo de secciones específico y expanden sus secciones y grupos de secciones.</span><span class="sxs-lookup"><span data-stu-id="3a599-213">Get a specific section group and expand its sections and section groups.</span></span>  

```
[GET] ../sectionGroups/{sectiongroup-id}?expand=sections,sectionGroups
```

<span data-ttu-id="3a599-214">Obtienen una página y expanden su sección principal y bloc de notas principal.</span><span class="sxs-lookup"><span data-stu-id="3a599-214">Get a page and expand its parent section and parent notebook.</span></span>

```
[GET] ../pages/{page-id}?expand=parentSection,parentNotebook
```

<span data-ttu-id="3a599-215">**expand** (varios niveles)</span><span class="sxs-lookup"><span data-stu-id="3a599-215">expand (multiple levels)</span></span>  

<span data-ttu-id="3a599-216">Obtienen todos los blocs de notas y expanden sus secciones y grupos de secciones, y expanden todas las secciones en cada grupo de secciones.</span><span class="sxs-lookup"><span data-stu-id="3a599-216">Get all notebooks and expand their sections and section groups, and expand all sections in each section group.</span></span>  

```
[GET] ../notebooks?expand=sections,sectionGroups(expand=sections)
```
 
><span data-ttu-id="3a599-217">No se admite expandir elementos primarios de entidades secundarias o expandir elementos secundarios de entidades primarias. Hacer eso crearía una referencia circular.</span><span class="sxs-lookup"><span data-stu-id="3a599-217">Expanding parents of child entities or expanding children of parent entities creates a circular reference and  is not supported.</span></span>

 
<span data-ttu-id="3a599-218">**expand & select** (varios niveles)</span><span class="sxs-lookup"><span data-stu-id="3a599-218">expand & select (multiple levels)</span></span>  

<span data-ttu-id="3a599-219">Obtienen el nombre y el vínculo a **self** para un grupo de secciones específico, y obtienen el nombre y los vínculos a **self** para todas sus secciones.</span><span class="sxs-lookup"><span data-stu-id="3a599-219">Get the name and **self** link for a specific section group, and get the name and self links for all its sections.</span></span>  

```
[GET] ../sectionGroups/{sectiongroup-id}?expand=sections(select=name,self)&select=name,self
```
 
<span data-ttu-id="3a599-220">Obtienen el nombre y el vínculo a **self** para todas las secciones, y obtienen el nombre y la hora de creación del bloc de notas primario de cada sección.</span><span class="sxs-lookup"><span data-stu-id="3a599-220">Get the name and **self** link for all sections, and get the name and created time of its parent notebook.</span></span>  

```
[GET] ../sections?expand=parentNotebook(select=name,createdTime)&select=name,self
```
 
<span data-ttu-id="3a599-221">Obtienen el título y el identificador de todas las páginas, y obtienen el nombre de la sección principal y bloc de notas principal.</span><span class="sxs-lookup"><span data-stu-id="3a599-221">Get the title and ID for all pages, and get the name of the parent section and parent notebook.</span></span>

```
[GET] ../pages?select=id,title&expand=parentSection(select=name),parentNotebook(select=name)
```

<span data-ttu-id="3a599-222">**expand & levels** (varios niveles)</span><span class="sxs-lookup"><span data-stu-id="3a599-222">expand & levels (multiple levels)</span></span>  

<span data-ttu-id="3a599-223">Obtienen todos los blocs de notas, grupos de secciones y todas las secciones.</span><span class="sxs-lookup"><span data-stu-id="3a599-223">Get all notebooks, sections, and section groups.</span></span>  

```
[GET] ../notebooks?expand=sections,sectionGroups(expand=sections,sectionGroups(levels=max;expand=sections))
```
 
<span data-ttu-id="3a599-224">**filter**</span><span class="sxs-lookup"><span data-stu-id="3a599-224">**filter**</span></span>  

<span data-ttu-id="3a599-225">Obtienen todas las secciones creadas en octubre de 2014.</span><span class="sxs-lookup"><span data-stu-id="3a599-225">Get all sections that were created in October 2014.</span></span>

```
[GET] ../sections?filter=createdTime ge 2014-10-01 and createdTime le 2014-10-31
```

<span data-ttu-id="3a599-226">Obtienen todas las páginas creadas por una aplicación específica desde el 1 de enero de 2015.</span><span class="sxs-lookup"><span data-stu-id="3a599-226">Get the pages that were created by a specific app since January 1, 2015.</span></span>

```
[GET] ../pages?filter=createdByAppId eq 'WLID-0000000048118631' and createdTime ge 2015-01-01
```

<span data-ttu-id="3a599-227">**filter & expand**</span><span class="sxs-lookup"><span data-stu-id="3a599-227">**filter & expand**</span></span>  

<span data-ttu-id="3a599-228">Obtienen todas las páginas de un bloc de notas específico.</span><span class="sxs-lookup"><span data-stu-id="3a599-228">Get all pages in a specific notebook.</span></span> <span data-ttu-id="3a599-229">La API devuelve 20 entradas de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3a599-229">The API returns 20 entries by default.</span></span>

```
[GET] ../pages?filter=parentNotebook/id eq '{notebook-id}'&expand=parentNotebook
```

<span data-ttu-id="3a599-230">Obtienen el nombre y el vínculo a **pagesUrl** para todas las secciones del bloc de notas *Escuela*.</span><span class="sxs-lookup"><span data-stu-id="3a599-230">Get the name and pagesUrl link for all sections in the user's default  notebook.</span></span> <span data-ttu-id="3a599-231">Las comparaciones de cadenas OData distinguen mayúsculas de minúsculas, por lo que se recomienda usar la función **tolower**.</span><span class="sxs-lookup"><span data-stu-id="3a599-231">Get the name and **pagesUrl** link for all sections from the School notebook.  OData string comparisons are case sensitive, so use the tolower function as a best practice.</span></span>

```
[GET] ../notebooks?filter=tolower(name) eq 'school'&expand=sections(select=name,pagesUrl)
```

<span data-ttu-id="3a599-232">**filter & select & orderby**</span><span class="sxs-lookup"><span data-stu-id="3a599-232">**filter & select & orderby**</span></span>   

<span data-ttu-id="3a599-233">Obtienen el nombre y el vínculo a **pagesUrl** para todas las secciones que contienen el término *spring* en el nombre de la sección.</span><span class="sxs-lookup"><span data-stu-id="3a599-233">Get the name and **pagesUrl** link for  all sections that contain the term *spring* in the section name. Order sections by last modified date.</span></span> <span data-ttu-id="3a599-234">Ordenan las secciones por fecha de última modificación.</span><span class="sxs-lookup"><span data-stu-id="3a599-234">Order sections by last modified date.</span></span>

```
[GET] ../sections?filter=contains(tolower(name),'spring')&select=name,pagesUrl&orderby=lastModifiedTime desc
```
 
<span data-ttu-id="3a599-235">**orderby**</span><span class="sxs-lookup"><span data-stu-id="3a599-235">**orderby**</span></span>  

<span data-ttu-id="3a599-236">Obtienen las primeras 20 páginas ordenadas por propiedad **createdByAppId** y luego por fecha de creación más reciente.</span><span class="sxs-lookup"><span data-stu-id="3a599-236">Get the first  20 pages ordered by **createdByAppId** property and then by most recent created time. The API returns 20 pages by default.</span></span> <span data-ttu-id="3a599-237">La API devuelve 20 entradas de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3a599-237">The API returns 20 entries by default.</span></span>

```
[GET] ../pages?orderby=createdByAppId,createdTime desc
```

<span data-ttu-id="3a599-238">**search & filter & top**</span><span class="sxs-lookup"><span data-stu-id="3a599-238">**search & filter & top**</span></span>  

<span data-ttu-id="3a599-239">Obtienen las cinco páginas más recientes creadas desde el 1 de enero de 2015, que contienen la frase *división de celda*.</span><span class="sxs-lookup"><span data-stu-id="3a599-239">Get the five  newest pages  created since January 1, 2015 that contain the phrase *cell division. The API returns 20 pages by default with a maximum of 100. The default sort order for pages lastModifiedTime desc*.</span></span> <span data-ttu-id="3a599-240">La API devuelve 20 entradas de forma predeterminada con un máximo de 100.</span><span class="sxs-lookup"><span data-stu-id="3a599-240">Get pages 51 to 100. The API returns 20 entries by default with a maximum of 100.</span></span> <span data-ttu-id="3a599-241">El criterio de ordenación predeterminado para páginas es `lastModifiedTime desc`.</span><span class="sxs-lookup"><span data-stu-id="3a599-241">The default sort order is `lastModifiedTime desc`.</span></span> <span data-ttu-id="3a599-242">(`search` solo está disponible para los blocs de notas de clientes)</span><span class="sxs-lookup"><span data-stu-id="3a599-242">(`search` is available for consumer notebooks only)</span></span>

```
[GET] ../pages?search="cell division"&filter=createdTime ge 2015-01-01&top=5
```

<span data-ttu-id="3a599-243">**search & filter & top & skip**</span><span class="sxs-lookup"><span data-stu-id="3a599-243">**search & filter & top & skip**</span></span>  

<span data-ttu-id="3a599-244">Obtienen las cinco páginas siguientes en el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="3a599-244">Get the next five  pages  in the result set.</span></span> <span data-ttu-id="3a599-245">(`search` solo está disponible para los blocs de notas de clientes)</span><span class="sxs-lookup"><span data-stu-id="3a599-245">(`search` is available for consumer notebooks only)</span></span>

```
[GET] ../pages?search=biology&filter=createdTime ge 2015-01-01&top=5&skip=5
```

<span data-ttu-id="3a599-246">Y las cinco siguientes.</span><span class="sxs-lookup"><span data-stu-id="3a599-246">And the next five.</span></span> <span data-ttu-id="3a599-247">(`search` solo está disponible para los blocs de notas de clientes)</span><span class="sxs-lookup"><span data-stu-id="3a599-247">(`search` is available for consumer notebooks only)</span></span>

```
[GET] ../pages?search=biology&filter=createdTime ge 2015-01-01&top=5&skip=10
```

> <span data-ttu-id="3a599-248">**Nota:** Si se aplican **search** y **filter** a la misma solicitud, los resultados incluyen solamente las entidades que coinciden con ambos criterios.</span><span class="sxs-lookup"><span data-stu-id="3a599-248">If both **search** and **filter** are applied to the same request, the results include only those entities that match both criteria.</span></span>
 
<span data-ttu-id="3a599-249">**select**</span><span class="sxs-lookup"><span data-stu-id="3a599-249">**select**</span></span>  

<span data-ttu-id="3a599-250">Obtienen el nombre, la hora de creación y el vínculo a **self** para todas las secciones en los blocs de notas del usuario.</span><span class="sxs-lookup"><span data-stu-id="3a599-250">Get the name, created time, and **self** link for all sections in the user's notebooks.</span></span>

```
[GET] ../sections?select=name,createdTime,self
```

<span data-ttu-id="3a599-251">Obtienen el título, la hora de creación y los vínculos a clientes de OneNote para una página específica.</span><span class="sxs-lookup"><span data-stu-id="3a599-251">Get the title, created time, and oncshort client links for a specific page.</span></span>

```
[GET] ../pages/{page-id}?select=title,createdTime,links
```

<span data-ttu-id="3a599-252">**select & expand & filter** (varios niveles)</span><span class="sxs-lookup"><span data-stu-id="3a599-252">select & expand & filter (multiple levels)</span></span>  

<span data-ttu-id="3a599-253">Obtienen el nombre y el vínculo a **pagesUrl** para todas las secciones en el bloc de notas predeterminado del usuario.</span><span class="sxs-lookup"><span data-stu-id="3a599-253">Get the name and **pagesUrl** link for all sections in the user's default  notebook.</span></span>

```
[GET] ../notebooks?select=name&expand=sections(select=name,pagesUrl)&filter=isDefault eq true
```

<span data-ttu-id="3a599-254">**top & select & orderby**</span><span class="sxs-lookup"><span data-stu-id="3a599-254">**top & select & orderby**</span></span>  

<span data-ttu-id="3a599-255">Obtienen el título y el vínculo **self** de las primeras 50 páginas, ordenadas alfabéticamente por título.</span><span class="sxs-lookup"><span data-stu-id="3a599-255">Get the title and **self** link for the first 50 pages, ordered alphabetically by title. The API returns 20 entries by default with a maximum of 100. The default sort order for pages lastModifiedTime desc.</span></span> <span data-ttu-id="3a599-256">La API devuelve 20 entradas de forma predeterminada con un máximo de 100.</span><span class="sxs-lookup"><span data-stu-id="3a599-256">Get pages 51 to 100. The API returns 20 entries by default with a maximum of 100.</span></span> <span data-ttu-id="3a599-257">El criterio de ordenación predeterminado para páginas es `lastModifiedTime desc`.</span><span class="sxs-lookup"><span data-stu-id="3a599-257">The default sort order is `lastModifiedTime desc`.</span></span>

```
[GET] ../pages?top=50&select=title,self&orderby=title
```

<span data-ttu-id="3a599-258">**skip & top & select & orderby**</span><span class="sxs-lookup"><span data-stu-id="3a599-258">**skip & top & select & orderby**</span></span>  

<span data-ttu-id="3a599-p123">Obtienen las páginas 51 a 100. La API devuelve 20 entradas de forma predeterminada con un máximo de 100.</span><span class="sxs-lookup"><span data-stu-id="3a599-p123">Get pages 51 to 100. The API returns 20 entries by default with a maximum of 100.</span></span>

```
[GET] ../pages?skip=50&top=50&select=title,self&orderby=title
```

> <span data-ttu-id="3a599-261">**Note:** Las solicitudes GET para páginas que recuperan el número predeterminado de entradas (es decir, no especifican una expresión **top**) devuelven un vínculo a **@odata.nextLink** en la respuesta que puede usar para obtener las 20 entradas siguientes.</span><span class="sxs-lookup"><span data-stu-id="3a599-261">GET requests for **pages** that retrieve the default number of entries (that is, they don’t specify a **top** expression) return an @odata.nextLink link in the response that you can use to get the next 20 entries.</span></span>
 

<a name="query-options"></a>
## <a name="supported-odata-query-string-options"></a><span data-ttu-id="3a599-262">Opciones de cadena de consultas OData admitidas</span><span class="sxs-lookup"><span data-stu-id="3a599-262">Supported OData query string options</span></span>

<span data-ttu-id="3a599-263">Al enviar solicitudes GET a Microsoft Graph, puede usar las opciones de cadena de consultas OData para personalizar la consulta y obtener solo la información que necesita.</span><span class="sxs-lookup"><span data-stu-id="3a599-263">When sending GET requests to the onnvshort API, you can use OData query string options to customize your query and get just the information you need. They can also improve performance by reducing the number of calls to the service and the size of the response payload.</span></span> <span data-ttu-id="3a599-264">También puede mejorar el rendimiento al reducir el número de llamadas al servicio y el tamaño de la carga de respuesta.</span><span class="sxs-lookup"><span data-stu-id="3a599-264">When sending GET requests to the onnvshort API, you can use OData query string options to customize your query and get just the information you need. They can also improve performance by reducing the number of calls to the service and the size of the response payload.</span></span>

> <span data-ttu-id="3a599-265">**Note:** Para su legibilidad, los ejemplos de este artículo no usan la codificación porcentual de %20 que se requiere para espacios en la cadena de consulta URL: `filter=isDefault%20eq%20true`</span><span class="sxs-lookup"><span data-stu-id="3a599-265">For readability, the examples in this article don't use the  %20`filter=isDefault%20eq%20true` percent-encoding required for spaces in the URL query string. Example:  filter=isDefault%20eq%20true</span></span>
 
| <span data-ttu-id="3a599-266">Opción de consulta</span><span class="sxs-lookup"><span data-stu-id="3a599-266">Query option</span></span> | <span data-ttu-id="3a599-267">Ejemplo y descripción</span><span class="sxs-lookup"><span data-stu-id="3a599-267">Example and description</span></span> |  
|------|------|  
| <span data-ttu-id="3a599-268">count</span><span class="sxs-lookup"><span data-stu-id="3a599-268">count</span></span> | <p>`count=true`</p><p><span data-ttu-id="3a599-269">El recuento de entidades de la colección.</span><span class="sxs-lookup"><span data-stu-id="3a599-269">The count of entities in the collection.</span></span> <span data-ttu-id="3a599-270">El valor se devuelve en la propiedad **@odata.count** de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3a599-270">The count of entities in the collection. The value is returned in the **@odata.count** property in the response.</span></span></p> |  
| <span data-ttu-id="3a599-271">expand</span><span class="sxs-lookup"><span data-stu-id="3a599-271">expand</span></span> | <p>`expand=sections,sectionGroups`</p><p><span data-ttu-id="3a599-272">Las propiedades de navegación para devolver la respuesta en línea.</span><span class="sxs-lookup"><span data-stu-id="3a599-272">The navigation properties to return inline  in the response. The following properties are supported for expand expressions:</span></span> <span data-ttu-id="3a599-273">Las siguientes propiedades son compatibles con las expresiones **expand**:</span><span class="sxs-lookup"><span data-stu-id="3a599-273">The navigation properties to return inline  in the response. The following properties are supported for **expand** expressions:</span></span><br /> <span data-ttu-id="3a599-274">- Páginas: **parentNotebook**, **parentSection**</span><span class="sxs-lookup"><span data-stu-id="3a599-274">Pages: 
**parentNotebook**, **parentSection**</span></span><br /> <span data-ttu-id="3a599-275">- Secciones: **parentNotebook**, **parentSectionGroup**</span><span class="sxs-lookup"><span data-stu-id="3a599-275">Sections: 
**parentNotebook**, **parentSectionGroup**</span></span><br /> <span data-ttu-id="3a599-276">- Grupos de secciones: **sections**, **sectionGroups**, **parentNotebook**, **parentSectionGroup**</span><span class="sxs-lookup"><span data-stu-id="3a599-276">Section groups: 
**sections**, **sectionGroups**, **parentNotebook**, **parentSectionGroup**</span></span><br /> <span data-ttu-id="3a599-277">- Blocs de notas: **sections**, **sectionGroups**</span><span class="sxs-lookup"><span data-stu-id="3a599-277">Notebooks: **sections**, **sectionGroups**</span></span></p><p><span data-ttu-id="3a599-278">De forma predeterminada, las solicitudes GET de páginas expanden **parentSection** y seleccionan las propiedades **id**, **name** y **self** de la sección.</span><span class="sxs-lookup"><span data-stu-id="3a599-278">By default, GET requests for pages expands **parentSection** and select the section's **id**, **name**, and **self** properties. Default GET requests for sections and section groups expand both parentNotebook and parentSectionGroup, and select the parents' id, name, and self properties.</span></span> <span data-ttu-id="3a599-279">Las solicitudes GET predeterminadas para secciones y grupos de secciones expanden tanto **parentNotebook** como **parentSectionGroup**, y seleccionan las propiedades **id**, **name** y **self** del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="3a599-279">By default, GET requests for sections and section groups expand both **parentNotebook** and **parentSectionGroup**, and select the parents' **id**, **name**, and **self** properties.</span></span> </p><p><span data-ttu-id="3a599-280">Puede usarse para una única entidad o una colección.</span><span class="sxs-lookup"><span data-stu-id="3a599-280">Can be used  for a single  entity or a collection. Separate  multiple properties with commas. Property names are case sensitive.</span></span> <span data-ttu-id="3a599-281">Separe las distintas propiedades mediante comas.</span><span class="sxs-lookup"><span data-stu-id="3a599-281">Separate multiple properties with commas.</span></span> <span data-ttu-id="3a599-282">Los nombres de las propiedades distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3a599-282">Property names are case sensitive.</span></span></p> |   
| <span data-ttu-id="3a599-283">filter</span><span class="sxs-lookup"><span data-stu-id="3a599-283">filter</span></span> | <p>`filter=isDefault eq true`</p><p><span data-ttu-id="3a599-284">Una expresión booleana por si desea incluir una entrada en el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="3a599-284">A Boolean expression for whether to include an entry in the result set.</span></span> <span data-ttu-id="3a599-285">Es compatible con las funciones y operadores de OData siguientes:</span><span class="sxs-lookup"><span data-stu-id="3a599-285">Supports the following OData operators and functions:</span></span><br /> <span data-ttu-id="3a599-286">- Operadores de comparación: **eq**, **ne**, **gt**, **ge**, **lt**, **le**</span><span class="sxs-lookup"><span data-stu-id="3a599-286">- Comparison operators: **eq**, **ne**, **gt**, **ge**, **lt**, **le**</span></span><br /> <span data-ttu-id="3a599-287">- Operadores lógicos: **and**, **or**, **not**</span><span class="sxs-lookup"><span data-stu-id="3a599-287">- Logical operators: **and**, **or**, **not**</span></span><br /> <span data-ttu-id="3a599-288">- Funciones de cadena: **contains**, **endswith**, **startswith**, **length**, **indexof**, **substring**, **tolower**, **toupper**, **trim**, **concat**</span><span class="sxs-lookup"><span data-stu-id="3a599-288">- String functions: **contains**, **endswith**, **startswith**, **length**, **indexof**, **substring**, **tolower**, **toupper**, **trim**, **concat**</span></span></p><p><span data-ttu-id="3a599-289">[Los nombres de propiedad](#onenote-entity-properties) y las comparaciones de cadenas de OData distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3a599-289">[Property](#onenote-entity-properties) names and OData string comparisons are case sensitive.</span></span> <span data-ttu-id="3a599-290">Se recomienda usar la función **tolower** de OData para comparaciones de cadenas.</span><span class="sxs-lookup"><span data-stu-id="3a599-290">Property names and OData string comparisons are case sensitive. We recommend using the OData **tolower** function for string comparisons. Example: filter=tolower(name) eq 'spring'</span></span> <span data-ttu-id="3a599-291">Ejemplo: `filter=tolower(name) eq 'spring'`</span><span class="sxs-lookup"><span data-stu-id="3a599-291">Example: `filter=tolower(name) eq 'spring'`</span></span></p> |  
| <span data-ttu-id="3a599-292">orderby</span><span class="sxs-lookup"><span data-stu-id="3a599-292">orderby</span></span> | <p>`orderby=title,createdTime desc`</p><p><span data-ttu-id="3a599-293">Las [propiedades](#onenote-entity-properties) por las que se va a ordenar, con un criterio de ordenación **asc** (predeterminado) o **desc** opcional.</span><span class="sxs-lookup"><span data-stu-id="3a599-293">The [properties](#onenote-entity-properties) to sort by, with an optional **asc** (default) or **desc** sort order. You can sort by any property of the entity in the requested collection.</span></span> <span data-ttu-id="3a599-294">Puede ordenar por cualquier propiedad de la entidad en la colección solicitada.</span><span class="sxs-lookup"><span data-stu-id="3a599-294">The properties to sort by, with an optional asc (default) or desc sort order. You can sort by any property of the entity in the requested collection.</span></span></p><p><span data-ttu-id="3a599-295">El orden predeterminado para blocs de notas, secciones y grupos de secciones es `name asc`, y para páginas es `lastModifiedTime desc` (última página modificada primero).</span><span class="sxs-lookup"><span data-stu-id="3a599-295">The default sort order for notebooks, section groups, and sections is name asc`name asc`, and for pages is lastModifiedTime desc`lastModifiedTime desc` (last modified page first).</span></span></p><p><span data-ttu-id="3a599-296">Si tiene varias propiedades, sepárelas con comas, y ordénelas con el orden en que desea que se apliquen.</span><span class="sxs-lookup"><span data-stu-id="3a599-296">Separate  multiple properties with commas, and list them in the order that you want them applied. Property names are case sensitive.</span></span> <span data-ttu-id="3a599-297">Los nombres de las propiedades distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3a599-297">Property names are case sensitive.</span></span></p> |  
| <span data-ttu-id="3a599-298">buscar</span><span class="sxs-lookup"><span data-stu-id="3a599-298">search</span></span> | <p>`search=cell div`</p><p><span data-ttu-id="3a599-299">Solo está disponible para los blocs de notas de clientes.</span><span class="sxs-lookup"><span data-stu-id="3a599-299">Available for consumer notebooks only.</span></span></p><p><span data-ttu-id="3a599-300">El término o la frase para buscar en el título de la página, el cuerpo de la página, el texto alternativo de la imagen y el texto OCR de la imagen.</span><span class="sxs-lookup"><span data-stu-id="3a599-300">
The term or phrase to search for in the page title, page body, image alt text, and image OCR text. By default, search queries return results sorted by relevance.</span></span> <span data-ttu-id="3a599-301">De forma predeterminada, las consultas de búsqueda devuelven resultados ordenados por relevancia.</span><span class="sxs-lookup"><span data-stu-id="3a599-301">By default, search queries return results sorted by relevance.</span></span></p><p><span data-ttu-id="3a599-302">OneNote usa la búsqueda de texto completo de Bing para admitir búsqueda de frases, lematización, omisión ortográfica, relevancia y clasificación, separación de palabras, varios idiomas y otras características de búsqueda de texto completo.</span><span class="sxs-lookup"><span data-stu-id="3a599-302">onnvshort uses Bing full text search to support phrase search, stemming, spelling forgiveness, relevance and ranking, word breaking, multiple languages, and other full-text search features. Search strings are case insensitive.</span></span> <span data-ttu-id="3a599-303">Las cadenas de búsqueda distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3a599-303">Search strings are case insensitive.</span></span></p><p><span data-ttu-id="3a599-304">Solo se aplica a las páginas de los blocs de notas que posee el usuario (no a los que se comparten con el usuario).</span><span class="sxs-lookup"><span data-stu-id="3a599-304">Applies only to pages in notebooks owned by the user (not shared with the user).</span></span> <span data-ttu-id="3a599-305">El contenido indexado es privado y solo puede acceder a él su propietario.</span><span class="sxs-lookup"><span data-stu-id="3a599-305">Indexed content is private and can only be accessed by the owner.</span></span> <span data-ttu-id="3a599-306">Las páginas protegidas con contraseña no están indexadas.</span><span class="sxs-lookup"><span data-stu-id="3a599-306">Password-protected pages are not indexed.</span></span> <span data-ttu-id="3a599-307">Solo se aplica al extremo `pages`.</span><span class="sxs-lookup"><span data-stu-id="3a599-307">Applies only to the `pages` endpoint.</span></span></p> |  
| <span data-ttu-id="3a599-308">select</span><span class="sxs-lookup"><span data-stu-id="3a599-308">select</span></span> | <p>`select=id,title`</p><p><span data-ttu-id="3a599-309">Las [propiedades](#onenote-entity-properties) que se devuelven.</span><span class="sxs-lookup"><span data-stu-id="3a599-309">The [properties](#onenote-entity-properties) to return.</span></span> <span data-ttu-id="3a599-310">Puede usarse para una única entidad o para una colección.</span><span class="sxs-lookup"><span data-stu-id="3a599-310">Can be used  for  a single  entity or for a collection. Separate  multiple properties with commas. Property names are case sensitive.</span></span> <span data-ttu-id="3a599-311">Separe las distintas propiedades mediante comas.</span><span class="sxs-lookup"><span data-stu-id="3a599-311">Separate multiple properties with commas.</span></span> <span data-ttu-id="3a599-312">Los nombres de las propiedades distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3a599-312">Property names are case sensitive.</span></span></p> |  
| <span data-ttu-id="3a599-313">skip</span><span class="sxs-lookup"><span data-stu-id="3a599-313">skip</span></span> | <p>`skip=10`</p><p><span data-ttu-id="3a599-314">El número de entradas que se omiten del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="3a599-314">The number of entries  to skip in the result set. Typically used for paging results.</span></span> <span data-ttu-id="3a599-315">Se usa normalmente para los resultados de paginación.</span><span class="sxs-lookup"><span data-stu-id="3a599-315">Typically used for paging results.</span></span></p> |  
| <span data-ttu-id="3a599-316">top</span><span class="sxs-lookup"><span data-stu-id="3a599-316">top</span></span> | <p>`top=50`</p><p><span data-ttu-id="3a599-317">El número de entradas para devolver en el conjunto de resultados, hasta un máximo de 100.</span><span class="sxs-lookup"><span data-stu-id="3a599-317">The number of entries to return in the result set, up to a maximum of 100. The default value for pages is 20.</span></span> <span data-ttu-id="3a599-318">El valor predeterminado es 20.</span><span class="sxs-lookup"><span data-stu-id="3a599-318">The default value is 20.</span></span></p> |  

<span data-ttu-id="3a599-319">Microsoft Graph también proporciona la opción de cadena de consulta `pagelevel` que puede usar para obtener el nivel y el orden de las páginas en la sección principal.</span><span class="sxs-lookup"><span data-stu-id="3a599-319">Microsoft Graph also provides the `pagelevel` query string option you can use to get the level and order of pages within the parent section.</span></span> <span data-ttu-id="3a599-320">Solo se aplica a las consultas para las páginas de una sección específica o para una página específica.</span><span class="sxs-lookup"><span data-stu-id="3a599-320">Applies only to queries for pages in a specific section or queries for a specific page.</span></span> 

<span data-ttu-id="3a599-321">**Ejemplo:**</span><span class="sxs-lookup"><span data-stu-id="3a599-321">**Example**</span></span> 

- `GET ../sections/{section-id}/pages?pagelevel=true` 
- `GET ../pages/{page-id}?pagelevel=true` 

### <a name="supported-odata-operators-and-functions"></a><span data-ttu-id="3a599-322">Operadores y funciones OData compatibles</span><span class="sxs-lookup"><span data-stu-id="3a599-322">Supported OData operators and functions</span></span>

<span data-ttu-id="3a599-323">Microsoft Graph admite los siguientes operadores y funciones OData en las expresiones **filter**.</span><span class="sxs-lookup"><span data-stu-id="3a599-323">Microsoft Graph supports the following OData operators and functions in **filter** expressions.</span></span> <span data-ttu-id="3a599-324">Al usar expresiones OData, recuerde:</span><span class="sxs-lookup"><span data-stu-id="3a599-324">When using OData expressions, remember:</span></span>  
- <span data-ttu-id="3a599-325">Debe reemplazar los espacios en la cadena de consulta URL con la codificación `%20`.</span><span class="sxs-lookup"><span data-stu-id="3a599-325">Spaces in the URL query string must be replaced with  the %20`%20` encoding. Example:  filter=isDefault%20eq%20true</span></span>

   <span data-ttu-id="3a599-326">**Ejemplo:** `filter=isDefault%20eq%20true`</span><span class="sxs-lookup"><span data-stu-id="3a599-326">Example</span></span>
- <span data-ttu-id="3a599-327">Los nombres de propiedad y las comparaciones de cadenas de OData distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3a599-327">Property names and OData string comparisons are case sensitive.</span></span> <span data-ttu-id="3a599-328">Se recomienda usar la función **tolower** de OData para comparaciones de cadenas.</span><span class="sxs-lookup"><span data-stu-id="3a599-328">Property names and OData string comparisons are case sensitive. We recommend using the OData **tolower** function for string comparisons. Example: filter=tolower(name) eq 'spring'</span></span>
   
   <span data-ttu-id="3a599-329">**Ejemplo:** `filter=tolower(name) eq 'spring'`</span><span class="sxs-lookup"><span data-stu-id="3a599-329">Example</span></span>

| <span data-ttu-id="3a599-330">Operador de comparación</span><span class="sxs-lookup"><span data-stu-id="3a599-330">comparison operator</span></span> | <span data-ttu-id="3a599-331">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3a599-331">Example</span></span> |  
|------|------|  
| <span data-ttu-id="3a599-332">eq</span><span class="sxs-lookup"><span data-stu-id="3a599-332">eq</span></span><br /><span data-ttu-id="3a599-333">(igual a)</span><span class="sxs-lookup"><span data-stu-id="3a599-333">(equal to)</span></span> | `createdByAppId eq '{app-id}'` |  
| <span data-ttu-id="3a599-334">ne</span><span class="sxs-lookup"><span data-stu-id="3a599-334">ne</span></span><br /><span data-ttu-id="3a599-335">(no es igual a)</span><span class="sxs-lookup"><span data-stu-id="3a599-335">(not equal to)</span></span> | `userRole ne 'Owner'` |  
| <span data-ttu-id="3a599-336">gt</span><span class="sxs-lookup"><span data-stu-id="3a599-336">gt</span></span><br /><span data-ttu-id="3a599-337">(mayor que)</span><span class="sxs-lookup"><span data-stu-id="3a599-337">(greater than)</span></span> | `createdTime gt 2014-02-23` |  
| <span data-ttu-id="3a599-338">ge</span><span class="sxs-lookup"><span data-stu-id="3a599-338">ge</span></span><br /><span data-ttu-id="3a599-339">(mayor o igual que)</span><span class="sxs-lookup"><span data-stu-id="3a599-339">(greater than or equal to)</span></span> | `lastModifiedTime ge 2014-05-05T07:00:00Z` |  
| <span data-ttu-id="3a599-340">lt</span><span class="sxs-lookup"><span data-stu-id="3a599-340">lt</span></span><br /><span data-ttu-id="3a599-341">(menor que)</span><span class="sxs-lookup"><span data-stu-id="3a599-341">(less than)</span></span> | `createdTime lt 2014-02-23` |  
| <span data-ttu-id="3a599-342">le</span><span class="sxs-lookup"><span data-stu-id="3a599-342">le</span></span><br /><span data-ttu-id="3a599-343">(menor que o igual que)</span><span class="sxs-lookup"><span data-stu-id="3a599-343">(less than or equal to)</span></span> | `lastModifiedTime le 2014-02-23` |  
 
| <span data-ttu-id="3a599-344">Operador lógico</span><span class="sxs-lookup"><span data-stu-id="3a599-344">Logical operator</span></span> | <span data-ttu-id="3a599-345">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3a599-345">Example</span></span> |  
|------|------|  
| <span data-ttu-id="3a599-346">y</span><span class="sxs-lookup"><span data-stu-id="3a599-346">and</span></span> | `createdTime le 2014-01-30 and createdTime gt 2014-01-23` |  
| <span data-ttu-id="3a599-347">o</span><span class="sxs-lookup"><span data-stu-id="3a599-347">or</span></span> | `createdByAppId eq '{app-id}' or createdByAppId eq '{app-id}'` |  
| <span data-ttu-id="3a599-348">
not</span><span class="sxs-lookup"><span data-stu-id="3a599-348">NOT</span></span> | `not contains(tolower(title),'school')` |  
 
| <span data-ttu-id="3a599-349">Función String</span><span class="sxs-lookup"><span data-stu-id="3a599-349">String Function</span></span> | <span data-ttu-id="3a599-350">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3a599-350">Example</span></span> |  
|------|------|   
| <span data-ttu-id="3a599-351">contains</span><span class="sxs-lookup"><span data-stu-id="3a599-351">contains</span></span> | `contains(tolower(title),'spring')` |  
| <span data-ttu-id="3a599-352">endswith</span><span class="sxs-lookup"><span data-stu-id="3a599-352">endswith</span></span> | `endswith(tolower(title),'spring')` |  
| <span data-ttu-id="3a599-353">startswith</span><span class="sxs-lookup"><span data-stu-id="3a599-353">startswith</span></span> | `startswith(tolower(title),'spring')` |  
| <span data-ttu-id="3a599-354">length</span><span class="sxs-lookup"><span data-stu-id="3a599-354">length</span></span> | `length(title) eq 19` |  
| <span data-ttu-id="3a599-355">indexof</span><span class="sxs-lookup"><span data-stu-id="3a599-355">indexof</span></span> | `indexof(tolower(title),'spring') eq 1` |  
| <span data-ttu-id="3a599-356">substring</span><span class="sxs-lookup"><span data-stu-id="3a599-356">substring</span></span> | `substring(tolower(title),1) eq 'spring'` |  
| <span data-ttu-id="3a599-357">tolower</span><span class="sxs-lookup"><span data-stu-id="3a599-357">tolower</span></span> | `tolower(title) eq 'spring'` |  
| <span data-ttu-id="3a599-358">toupper</span><span class="sxs-lookup"><span data-stu-id="3a599-358">toupper</span></span> | `toupper(title) eq 'SPRING'` |  
| <span data-ttu-id="3a599-359">trim</span><span class="sxs-lookup"><span data-stu-id="3a599-359">trim</span></span> | `trim(tolower(title)) eq 'spring'` |  
| <span data-ttu-id="3a599-360">concat</span><span class="sxs-lookup"><span data-stu-id="3a599-360">concat</span></span> | `concat(title,'- by MyRecipesApp') eq 'Carrot Cake Recipe - by MyRecipesApp'` |  
 

<a name="properties"></a>
## <a name="onenote-entity-properties"></a><span data-ttu-id="3a599-361">Propiedades de entidad de OneNote</span><span class="sxs-lookup"><span data-stu-id="3a599-361">OneNote entity properties</span></span>

<span data-ttu-id="3a599-362">Las expresiones de consulta **filter**, **select**, **expand** y **orderby** pueden incluir propiedades de las entidades de OneNote.</span><span class="sxs-lookup"><span data-stu-id="3a599-362">The **filter**, **select**, **expand**, and **orderby** query expressions can include properties of OneNote entities.</span></span> 

<span data-ttu-id="3a599-363">**Ejemplo:**</span><span class="sxs-lookup"><span data-stu-id="3a599-363">**Example**</span></span>

`../sections?filter=createdTime ge 2015-01-01&select=name,pagesUrl&orderby=lastModifiedTime desc` 

<span data-ttu-id="3a599-364">Los nombres de las propiedades distinguen mayúsculas de minúsculas en las expresiones de consulta.</span><span class="sxs-lookup"><span data-stu-id="3a599-364">Property names are case sensitive in query expressions.</span></span>

<span data-ttu-id="3a599-365">Para la lista de propiedades y tipos de propiedades, consulte:</span><span class="sxs-lookup"><span data-stu-id="3a599-365">For the list of properties and property types, see:</span></span>

- [<span data-ttu-id="3a599-366">GET Pages</span><span class="sxs-lookup"><span data-stu-id="3a599-366">Get pages</span></span>](../api-reference/v1.0/api/page_get.md)
- [<span data-ttu-id="3a599-367">GET Sections</span><span class="sxs-lookup"><span data-stu-id="3a599-367">GET sections</span></span>](../api-reference/v1.0/api/section_get.md)
- [<span data-ttu-id="3a599-368">GET SectionGroups</span><span class="sxs-lookup"><span data-stu-id="3a599-368">GET sectiongroups</span></span>](../api-reference/v1.0/api/sectiongroup_get.md)
- [<span data-ttu-id="3a599-369">GET Notebooks</span><span class="sxs-lookup"><span data-stu-id="3a599-369">GET notebooks</span></span>](../api-reference/v1.0/api/notebook_get.md) 

<span data-ttu-id="3a599-370">en la referencia de la API de REST de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="3a599-370">in the Microsoft Graph API REST reference.</span></span>

<span data-ttu-id="3a599-371">La opción de cadena de consulta **expand** se puede usar con las siguientes propiedades de navegación:</span><span class="sxs-lookup"><span data-stu-id="3a599-371">The **expand** query string option can be used with the following navigation properties:</span></span>

- <span data-ttu-id="3a599-372">Páginas: **parentNotebook**, **parentSection**</span><span class="sxs-lookup"><span data-stu-id="3a599-372">Pages: 
**parentNotebook**, **parentSection**</span></span>
- <span data-ttu-id="3a599-373">Secciones: **parentNotebook**, **parentSectionGroup**</span><span class="sxs-lookup"><span data-stu-id="3a599-373">Sections: 
**parentNotebook**, **parentSectionGroup**</span></span>
- <span data-ttu-id="3a599-374">Grupos de secciones: **sections**, **sectionGroups**, **parentNotebook**, **parentSectionGroup**</span><span class="sxs-lookup"><span data-stu-id="3a599-374">Section groups: 
**sections**, **sectionGroups**, **parentNotebook**, **parentSectionGroup**</span></span>
- <span data-ttu-id="3a599-375">Blocs de notas: **sections**, **sectionGroups**</span><span class="sxs-lookup"><span data-stu-id="3a599-375">Notebooks: **sections**, **sectionGroups**</span></span>


<a name="request-response-info"></a>
## <a name="request-and-response-information-for-get-requests"></a><span data-ttu-id="3a599-376">Información de la solicitud y respuesta para las solicitudes *GET*</span><span class="sxs-lookup"><span data-stu-id="3a599-376">Request and response information for *GET* requests</span></span>

| <span data-ttu-id="3a599-377">Datos de solicitud</span><span class="sxs-lookup"><span data-stu-id="3a599-377">Request data</span></span> | <span data-ttu-id="3a599-378">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a599-378">Description</span></span> |  
|------|------|  
| <span data-ttu-id="3a599-379">Protocolo</span><span class="sxs-lookup"><span data-stu-id="3a599-379">Protocol</span></span> | <span data-ttu-id="3a599-380">Todas las solicitudes usan el protocolo HTTPS SSL/TLS.</span><span class="sxs-lookup"><span data-stu-id="3a599-380">All requests use the SSL/TLS HTTPS protocol.</span></span> |  
| <span data-ttu-id="3a599-381">Encabezado Authorization</span><span class="sxs-lookup"><span data-stu-id="3a599-381">Authorization header</span></span> | <p><span data-ttu-id="3a599-382">`Bearer {token}`, donde *{token}* es un token de acceso de OAuth 2.0 válido para la aplicación registrada.</span><span class="sxs-lookup"><span data-stu-id="3a599-382">`Bearer {token}`, where *{token}* is a valid OAuth 2.0 access token for your registered app.</span></span></p><p><span data-ttu-id="3a599-383">Si falta o no es válido, se produce un error en la solicitud con un código de estado 401.</span><span class="sxs-lookup"><span data-stu-id="3a599-383">If missing or invalid, the request fails with a 401 status code.</span></span> <span data-ttu-id="3a599-384">Vea [Authentication and permissions](permissions_reference.md) (Autenticación y permisos).</span><span class="sxs-lookup"><span data-stu-id="3a599-384">See [Authentication and permissions](permissions_reference.md).</span></span></p> |  
| <span data-ttu-id="3a599-385">Encabezado Accept</span><span class="sxs-lookup"><span data-stu-id="3a599-385">accept header</span></span> | <p><span data-ttu-id="3a599-386">- `application/json` para las entidades y los conjuntos de entidades de OneNote</span><span class="sxs-lookup"><span data-stu-id="3a599-386">- `application/json` for OneNote entities and entity sets</span></span></p><p><span data-ttu-id="3a599-387">- `text/html` para contenido de la página</span><span class="sxs-lookup"><span data-stu-id="3a599-387">- `text/html` for page content</span></span></p> | 

| <span data-ttu-id="3a599-388">Datos de respuesta</span><span class="sxs-lookup"><span data-stu-id="3a599-388">Response data</span></span> | <span data-ttu-id="3a599-389">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a599-389">Description</span></span> |  
|------|------|  
| <span data-ttu-id="3a599-390">Código de correcto</span><span class="sxs-lookup"><span data-stu-id="3a599-390">Success code</span></span> | <span data-ttu-id="3a599-391">Un código de estado HTTP 200.</span><span class="sxs-lookup"><span data-stu-id="3a599-391">A 200 (OK) status code.</span></span> |  
| <span data-ttu-id="3a599-392">Cuerpo de la respuesta</span><span class="sxs-lookup"><span data-stu-id="3a599-392">Response body</span></span> | <span data-ttu-id="3a599-393">Una representación de OData de la entidad o entidad establecida en formato JSON, el HTML de la página, o datos binarios recursos de un recurso de archivo.</span><span class="sxs-lookup"><span data-stu-id="3a599-393">An OData representation of the entity or entity set in JSON format, the page HTML, or file resource binary data.</span></span>  |  
| <span data-ttu-id="3a599-394">Errores</span><span class="sxs-lookup"><span data-stu-id="3a599-394">Errors</span></span> | <span data-ttu-id="3a599-395">Si se produce un error en la solicitud, la API devuelve [errors](onenote_error_codes.md) en el objeto **@api.diagnostics** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3a599-395">If the update request fails, the API returns errors in the **api.diagnostics** object in the response body. The request will fail if:</span></span> |  
| <span data-ttu-id="3a599-396">Encabezado X-CorrelationId</span><span class="sxs-lookup"><span data-stu-id="3a599-396">X-CorrelationId header</span></span> | <span data-ttu-id="3a599-397">GUID que identifica la solicitud de manera única.</span><span class="sxs-lookup"><span data-stu-id="3a599-397">A GUID that uniquely identifies the request.</span></span> <span data-ttu-id="3a599-398">Puede usar este valor junto con el valor del encabezado de fecha al trabajar con el soporte técnico de Microsoft para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="3a599-398">You can use this value along with the value of the Date header when working with Microsoft support to troubleshoot issues.</span></span> |  


<a name="root-url"></a>
### <a name="constructing-the-microsoft-graph-notes-service-root-url"></a><span data-ttu-id="3a599-399">Crear la dirección URL raíz del servicio de notas de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="3a599-399">Constructing the Microsoft Graph notes service root URL</span></span>

<span data-ttu-id="3a599-400">La dirección URL raíz de notas de Microsoft Graph usa el siguiente formato para todas las llamadas a las notas de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="3a599-400">The Microsoft Graph notes root URL uses the following format for all calls to Microsoft Graph notes.</span></span> <span data-ttu-id="3a599-401">`https://graph.microsoft.com/{version}/me/onenote/` El segmento `version` de la dirección URL representa la versión de Microsoft Graph que desea usar.</span><span class="sxs-lookup"><span data-stu-id="3a599-401">`https://graph.microsoft.com/{version}/me/onenote/`  The `version` segment in the URL represents the version of Microsoft Graph that you want to use.</span></span> <span data-ttu-id="3a599-402">Use `v1.0` para el código de producción estable.</span><span class="sxs-lookup"><span data-stu-id="3a599-402">Use `v1.0` for stable production code.</span></span> <span data-ttu-id="3a599-403">Use `beta` para probar una característica que se encuentra en desarrollo.</span><span class="sxs-lookup"><span data-stu-id="3a599-403">Use `beta` to try out a feature that's in development.</span></span> <span data-ttu-id="3a599-404">Las características y la funcionalidad de la versión beta pueden cambiar, por lo que no se debe usar en el código de producción.</span><span class="sxs-lookup"><span data-stu-id="3a599-404">Features and functionality in beta may change, so you shouldn't use it in your production code.</span></span> <span data-ttu-id="3a599-405">Use `me` para contenido de OneNote al que pueda acceder el usuario actual (de su propiedad y compartido).</span><span class="sxs-lookup"><span data-stu-id="3a599-405">Use `me` for OneNote content that the current user can access (owned and shared).</span></span> <span data-ttu-id="3a599-406">Use `users/{id}` para contenido de OneNote que el usuario especificado (en la dirección URL) ha compartido con el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="3a599-406">Use `users/{id}` for OneNote content that the specified user (in the URL) has shared with the current user.</span></span> <span data-ttu-id="3a599-407">Use [Microsoft Graph](https://graph.microsoft.com/v1.0/users) para obtener los identificadores de usuario.</span><span class="sxs-lookup"><span data-stu-id="3a599-407">Use the [Microsoft Graph](https://graph.microsoft.com/v1.0/users) to get user IDs.</span></span> 


<a name="permissions"></a>
## <a name="permissions-for-get-requests"></a><span data-ttu-id="3a599-408">Permisos de solicitudes GET</span><span class="sxs-lookup"><span data-stu-id="3a599-408">Permissions for GET requests</span></span>

<span data-ttu-id="3a599-409">Para obtener el contenido o la estructura de OneNote, debe solicitar los permisos adecuados.</span><span class="sxs-lookup"><span data-stu-id="3a599-409">To get OneNote content or structure, you'll need to request appropriate permissions.</span></span> 

<span data-ttu-id="3a599-410">Los siguientes ámbitos permiten obtener solicitudes a Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="3a599-410">The following scopes allow GET requests to Microsoft Graph.</span></span> <span data-ttu-id="3a599-411">Elija el nivel más bajo de permisos que necesita la aplicación para hacer su trabajo.</span><span class="sxs-lookup"><span data-stu-id="3a599-411">Choose the lowest level of permissions that your app needs to do its work.</span></span>

<span data-ttu-id="3a599-412">Elija entre:</span><span class="sxs-lookup"><span data-stu-id="3a599-412">Choose from:</span></span> 
- <span data-ttu-id="3a599-413">Notes.read</span><span class="sxs-lookup"><span data-stu-id="3a599-413">Notes.Read</span></span>
- <span data-ttu-id="3a599-414">Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3a599-414">Notes.ReadWrite</span></span>
- <span data-ttu-id="3a599-415">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3a599-415">Notes.ReadWrite.All</span></span>


<span data-ttu-id="3a599-416">Para obtener más información sobre los ámbitos de permiso y cómo funcionan, consulte [Referencia de permisos de Microsoft Graph](permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="3a599-416">For more information about permission scopes and how they work, see [Microsoft Graph permissions reference](permissions_reference.md).</span></span>

<a name="see-also"></a>
## <a name="additional-resources"></a><span data-ttu-id="3a599-417">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="3a599-417">Additional resources</span></span>

- [<span data-ttu-id="3a599-418">HTML de entrada y salida para páginas de OneNote</span><span class="sxs-lookup"><span data-stu-id="3a599-418">Input and output HTML for OneNote pages</span></span>](onenote_input_output_html.md)
- [<span data-ttu-id="3a599-419">Integración con OneNote</span><span class="sxs-lookup"><span data-stu-id="3a599-419">Integrate with OneNote</span></span>](integrate_with_onenote.md)
- [<span data-ttu-id="3a599-420">Blog para desarrolladores de OneNote</span><span class="sxs-lookup"><span data-stu-id="3a599-420">OneNote Developer Blog</span></span>](http://go.microsoft.com/fwlink/?LinkID=390183)
- [<span data-ttu-id="3a599-421">Preguntas de desarrollo de OneNote en Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="3a599-421">OneNote development questions on Stack Overflow</span></span>](http://go.microsoft.com/fwlink/?LinkID=390182)
- [<span data-ttu-id="3a599-422">Repositorios de OneNote en GitHub</span><span class="sxs-lookup"><span data-stu-id="3a599-422">OneNote GitHub repos</span></span>](http://go.microsoft.com/fwlink/?LinkID=390178)  
