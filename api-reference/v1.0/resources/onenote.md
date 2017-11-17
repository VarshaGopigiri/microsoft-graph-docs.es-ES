# <a name="onenote-resource-type"></a><span data-ttu-id="15c2a-101">Tipo de recurso onenote</span><span class="sxs-lookup"><span data-stu-id="15c2a-101">onenote resource type</span></span>

<span data-ttu-id="15c2a-102">Punto de entrada para los recursos de OneNote.</span><span class="sxs-lookup"><span data-stu-id="15c2a-102">The entry point for OneNote resources.</span></span>

<span data-ttu-id="15c2a-103">Todas las llamadas al servicio de OneNote a través de la API de Microsoft Graph utilizan esta dirección URL raíz del servicio:</span><span class="sxs-lookup"><span data-stu-id="15c2a-103">All calls to the OneNote service through the Microsoft Graph API use this service root URL:</span></span>

```
https://graph.microsoft.com/{version}/{location}/onenote/ 
```

<span data-ttu-id="15c2a-104">La ubicación puede ser el bloc de notas del usuario en Office 365 o OneDrive para el cliente, los blocs de notas de grupo o blocs de notas de grupo hospedados en un sitio de SharePoint en Office 365.</span><span class="sxs-lookup"><span data-stu-id="15c2a-104">The location can be user notebooks on Office 365 or consumer OneDrive, group notebooks or SharePoint site-hosted team notebooks on Office 365.</span></span> 

<span data-ttu-id="15c2a-105">**Blocs de notas del usuario** Para obtener acceso a los blocs de notas personales en OneDrive para el cliente o OneDrive para la Empresa, utilice una de las siguientes direcciones URL:</span><span class="sxs-lookup"><span data-stu-id="15c2a-105">**User notebooks** To access personal notebooks on consumer OneDrive or OneDrive for Business, use one of the following URLs:</span></span>

```
https://graph.microsoft.com/{version}/me/onenote/{notebooks | sections | sectionGroups | pages} 
https://graph.microsoft.com/{version}/users/{userPrincipalName}/onenote/{notebooks | sections | sectionGroups | pages} 
https://graph.microsoft.com/{version}/users/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```

<span data-ttu-id="15c2a-106">**Blocs de notas de grupo** Para obtener acceso a los blocs de notas que pertenecen a un grupo, utilice la siguiente dirección URL raíz de servicio:</span><span class="sxs-lookup"><span data-stu-id="15c2a-106">**Group notebooks** To access notebooks that are owned by a group, use the following service root URL:</span></span>

```
https://graph.microsoft.com/{version}/groups/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```
<span data-ttu-id="15c2a-107">**Blocs de notas de sitio de SharePoint** Para obtener acceso a los blocs de notas que pertenecen a un sitio de grupo de SharePoint, use la siguiente dirección URL raíz de servicio:</span><span class="sxs-lookup"><span data-stu-id="15c2a-107">**SharePoint site notebooks** To access notebooks that are owned by a SharePoint team site, use the following service root URL:</span></span>

```
https://graph.microsoft.com/{version}/sites/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```
## <a name="authorization"></a><span data-ttu-id="15c2a-108">Autorización</span><span class="sxs-lookup"><span data-stu-id="15c2a-108">Authorization</span></span>

<span data-ttu-id="15c2a-109">Para obtener información sobre los permisos necesarios para trabajar con las API de OneNote, consulte [Permisos de notas](../../../concepts/permissions_reference.md#notes-permissions).</span><span class="sxs-lookup"><span data-stu-id="15c2a-109">For information about the permissions required to work with OneNote APIs, see [Notes permissions](../../../concepts/permissions_reference.md#notes-permissions).</span></span>


## <a name="relationships"></a><span data-ttu-id="15c2a-110">Relaciones</span><span class="sxs-lookup"><span data-stu-id="15c2a-110">Relationships</span></span>
| <span data-ttu-id="15c2a-111">Relación</span><span class="sxs-lookup"><span data-stu-id="15c2a-111">Relationship</span></span> | <span data-ttu-id="15c2a-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="15c2a-112">Type</span></span>   |<span data-ttu-id="15c2a-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="15c2a-113">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="15c2a-114">notebooks</span><span class="sxs-lookup"><span data-stu-id="15c2a-114">notebooks</span></span>|<span data-ttu-id="15c2a-115">Colección de [notebook](notebook.md)</span><span class="sxs-lookup"><span data-stu-id="15c2a-115">[Notebook](notebook.md) collection</span></span>|<span data-ttu-id="15c2a-p101">Colección de blocs de notas de OneNote que son propiedad del usuario o grupo. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="15c2a-p101">The collection of OneNote notebooks that are owned by the user or group. Read-only. Nullable.</span></span>|
|<span data-ttu-id="15c2a-119">operations</span><span class="sxs-lookup"><span data-stu-id="15c2a-119">operations</span></span>|<span data-ttu-id="15c2a-120">Colección de [operations](onenoteoperation.md)</span><span class="sxs-lookup"><span data-stu-id="15c2a-120">[Operation](onenoteoperation.md) collection</span></span> |<span data-ttu-id="15c2a-p102">El estado de las operaciones de OneNote. No se admite la obtención de una colección de operaciones, pero puede obtener el estado de las operaciones de larga duración si el encabezado `Operation-Location` se devuelve en la respuesta. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="15c2a-p102">The status of OneNote operations. Getting an operations collection is not supported, but you can get the status of long-running operations if the `Operation-Location` header is returned in the response. Read-only. Nullable.</span></span>|
|<span data-ttu-id="15c2a-125">pages</span><span class="sxs-lookup"><span data-stu-id="15c2a-125">pages</span></span>|<span data-ttu-id="15c2a-126">Colección de [page](page.md)</span><span class="sxs-lookup"><span data-stu-id="15c2a-126">[Page](page.md) collection</span></span>|<span data-ttu-id="15c2a-p103">Páginas de todos los blocs de notas de OneNote que son propiedad del usuario o grupo.  Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="15c2a-p103">The pages in all OneNote notebooks that are owned by the user or group.  Read-only. Nullable.</span></span>|
|<span data-ttu-id="15c2a-130">resources</span><span class="sxs-lookup"><span data-stu-id="15c2a-130">resources</span></span>|<span data-ttu-id="15c2a-131">Colección de [resources](resource.md)</span><span class="sxs-lookup"><span data-stu-id="15c2a-131">[Resource](resource.md) collection</span></span> |<span data-ttu-id="15c2a-p104">Imagen y otros recursos de archivo en páginas de OneNote. No se admite la obtención de una colección de recursos, pero puede [obtener el contenido binario de un determinado recurso](resource.md). Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="15c2a-p104">The image and other file resources in OneNote pages. Getting a resources collection is not supported, but you can [get the binary content of a specific resource](resource.md). Read-only. Nullable.</span></span>|
|<span data-ttu-id="15c2a-136">sectionGroups</span><span class="sxs-lookup"><span data-stu-id="15c2a-136">sectionGroups</span></span>|<span data-ttu-id="15c2a-137">Colección [SectionGroup](sectiongroup.md)</span><span class="sxs-lookup"><span data-stu-id="15c2a-137">[SectionGroup](sectiongroup.md) collection</span></span>|<span data-ttu-id="15c2a-p105">Grupos de secciones de todos los blocs de notas de OneNote que son propiedad del usuario o grupo.  Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="15c2a-p105">The section groups in all OneNote notebooks that are owned by the user or group.  Read-only. Nullable.</span></span>|
|<span data-ttu-id="15c2a-141">sections</span><span class="sxs-lookup"><span data-stu-id="15c2a-141">sections</span></span>|<span data-ttu-id="15c2a-142">Colección de [secciones](section.md)</span><span class="sxs-lookup"><span data-stu-id="15c2a-142">[Section](section.md) collection</span></span>|<span data-ttu-id="15c2a-p106">Secciones de todos los blocs de notas de OneNote que son propiedad del usuario o grupo.  Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="15c2a-p106">The sections in all OneNote notebooks that are owned by the user or group.  Read-only. Nullable.</span></span>|

## <a name="methods"></a><span data-ttu-id="15c2a-146">Métodos</span><span class="sxs-lookup"><span data-stu-id="15c2a-146">Methods</span></span>

| <span data-ttu-id="15c2a-147">Método</span><span class="sxs-lookup"><span data-stu-id="15c2a-147">Method</span></span>           | <span data-ttu-id="15c2a-148">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="15c2a-148">Return Type</span></span>    |<span data-ttu-id="15c2a-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="15c2a-149">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="15c2a-150">Crear bloc de notas</span><span class="sxs-lookup"><span data-stu-id="15c2a-150">Create notebook</span></span>](../api/onenote_post_notebooks.md) |[<span data-ttu-id="15c2a-151">Notebook</span><span class="sxs-lookup"><span data-stu-id="15c2a-151">Notebook</span></span>](notebook.md)| <span data-ttu-id="15c2a-152">Crear un bloc de notas mediante su publicación en la colección de blocs de notas.</span><span class="sxs-lookup"><span data-stu-id="15c2a-152">Create a notebook by posting to the notebooks collection.</span></span>|
|[<span data-ttu-id="15c2a-153">Enumerar los blocs de notas</span><span class="sxs-lookup"><span data-stu-id="15c2a-153">List notebooks</span></span>](../api/onenote_list_notebooks.md) |<span data-ttu-id="15c2a-154">Colección de [notebook](notebook.md)</span><span class="sxs-lookup"><span data-stu-id="15c2a-154">[Notebook](notebook.md) collection</span></span>| <span data-ttu-id="15c2a-155">Obtener una colección de blocs de notas.</span><span class="sxs-lookup"><span data-stu-id="15c2a-155">Get a collection of notebooks.</span></span>|
|[<span data-ttu-id="15c2a-156">Crear página</span><span class="sxs-lookup"><span data-stu-id="15c2a-156">Create page</span></span>](../api/onenote_post_pages.md) |[<span data-ttu-id="15c2a-157">Page</span><span class="sxs-lookup"><span data-stu-id="15c2a-157">Page</span></span>](page.md)| <span data-ttu-id="15c2a-158">Crear una página mediante su publicación en la colección de páginas.</span><span class="sxs-lookup"><span data-stu-id="15c2a-158">Create a page by posting to the pages collection.</span></span>|
|[<span data-ttu-id="15c2a-159">Enumerar páginas</span><span class="sxs-lookup"><span data-stu-id="15c2a-159">List pages</span></span>](../api/onenote_list_pages.md) |<span data-ttu-id="15c2a-160">Colección de [page](page.md)</span><span class="sxs-lookup"><span data-stu-id="15c2a-160">[Page](page.md) collection</span></span>| <span data-ttu-id="15c2a-161">Obtener una colección de páginas.</span><span class="sxs-lookup"><span data-stu-id="15c2a-161">Get a collection of pages.</span></span>|
|[<span data-ttu-id="15c2a-162">Enumerar grupos de sección</span><span class="sxs-lookup"><span data-stu-id="15c2a-162">List section groups</span></span>](../api/onenote_list_sectiongroups.md) |<span data-ttu-id="15c2a-163">Colección de [SectionGroup](sectiongroup.md)</span><span class="sxs-lookup"><span data-stu-id="15c2a-163">[SectionGroup](sectiongroup.md) collection</span></span>| <span data-ttu-id="15c2a-164">Obtener una colección de grupos de secciones.</span><span class="sxs-lookup"><span data-stu-id="15c2a-164">Get a collection of section groups.</span></span>|
|[<span data-ttu-id="15c2a-165">Enumerar secciones</span><span class="sxs-lookup"><span data-stu-id="15c2a-165">List sections</span></span>](../api/onenote_list_sections.md) |<span data-ttu-id="15c2a-166">Colección de [secciones](section.md)</span><span class="sxs-lookup"><span data-stu-id="15c2a-166">[Section](section.md) collection</span></span>| <span data-ttu-id="15c2a-167">Obtener una colección de secciones.</span><span class="sxs-lookup"><span data-stu-id="15c2a-167">Get a collection of sections.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onenote resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
