# <a name="onenote-resource-type"></a><span data-ttu-id="4ef95-101">Tipo de recurso onenote</span><span class="sxs-lookup"><span data-stu-id="4ef95-101">onenote resource type</span></span>

<span data-ttu-id="4ef95-102">Punto de entrada para los recursos de OneNote.</span><span class="sxs-lookup"><span data-stu-id="4ef95-102">The entry point for OneNote resources.</span></span>

<span data-ttu-id="4ef95-103">Todas las llamadas al servicio de OneNote a través de la API de Microsoft Graph utilizan esta dirección URL raíz del servicio:</span><span class="sxs-lookup"><span data-stu-id="4ef95-103">All calls to the OneNote service through the Microsoft Graph API use this service root URL:</span></span>

```
https://graph.microsoft.com/{version}/{location}/onenote/ 
```

<span data-ttu-id="4ef95-104">La ubicación puede ser el bloc de notas del usuario en Office 365 o OneDrive para el cliente, los blocs de notas de grupo o blocs de notas de grupo hospedados en un sitio de SharePoint en Office 365.</span><span class="sxs-lookup"><span data-stu-id="4ef95-104">The location can be user notebooks on Office 365 or consumer OneDrive, group notebooks or SharePoint site-hosted team notebooks on Office 365.</span></span> 

<span data-ttu-id="4ef95-105">**Blocs de notas del usuario** Para obtener acceso a los blocs de notas personales en OneDrive para el cliente o OneDrive para la Empresa, utilice una de las siguientes direcciones URL:</span><span class="sxs-lookup"><span data-stu-id="4ef95-105">**User notebooks** To access personal notebooks on consumer OneDrive or OneDrive for Business, use one of the following URLs:</span></span>

```
https://graph.microsoft.com/{version}/me/onenote/{notebooks | sections | sectionGroups | pages} 
https://graph.microsoft.com/{version}/users/{userPrincipalName}/onenote/{notebooks | sections | sectionGroups | pages} 
https://graph.microsoft.com/{version}/users/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```

<span data-ttu-id="4ef95-106">**Blocs de notas de grupo** Para obtener acceso a los blocs de notas que pertenecen a un grupo, utilice la siguiente dirección URL raíz de servicio:</span><span class="sxs-lookup"><span data-stu-id="4ef95-106">**Group notebooks** To access notebooks that are owned by a group, use the following service root URL:</span></span>

```
https://graph.microsoft.com/{version}/groups/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```
<span data-ttu-id="4ef95-107">**Blocs de notas de sitio de SharePoint** Para obtener acceso a los blocs de notas que pertenecen a un sitio de grupo de SharePoint, use la siguiente dirección URL raíz de servicio:</span><span class="sxs-lookup"><span data-stu-id="4ef95-107">**SharePoint site notebooks** To access notebooks that are owned by a SharePoint team site, use the following service root URL:</span></span>

```
https://graph.microsoft.com/{version}/sites/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```
## <a name="authorization"></a><span data-ttu-id="4ef95-108">Autorización</span><span class="sxs-lookup"><span data-stu-id="4ef95-108">Authorization</span></span>

<span data-ttu-id="4ef95-109">Para obtener información sobre los permisos necesarios para trabajar con las API de OneNote, consulte [Permisos de notas](../../../concepts/permissions_reference.md#notes-permissions).</span><span class="sxs-lookup"><span data-stu-id="4ef95-109">For information about the permissions required to work with OneNote APIs, see [Notes permissions](../../../concepts/permissions_reference.md#notes-permissions).</span></span>


## <a name="relationships"></a><span data-ttu-id="4ef95-110">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4ef95-110">Relationships</span></span>
| <span data-ttu-id="4ef95-111">Relación</span><span class="sxs-lookup"><span data-stu-id="4ef95-111">Relationship</span></span> | <span data-ttu-id="4ef95-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="4ef95-112">Type</span></span>   |<span data-ttu-id="4ef95-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="4ef95-113">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4ef95-114">notebooks</span><span class="sxs-lookup"><span data-stu-id="4ef95-114">notebooks</span></span>|<span data-ttu-id="4ef95-115">Colección de [notebook](notebook.md)</span><span class="sxs-lookup"><span data-stu-id="4ef95-115">[Notebook](notebook.md) collection</span></span>|<span data-ttu-id="4ef95-p101">Colección de blocs de notas de OneNote que son propiedad del usuario o grupo. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="4ef95-p101">The collection of OneNote notebooks that are owned by the user or group. Read-only. Nullable.</span></span>|
|<span data-ttu-id="4ef95-119">operations</span><span class="sxs-lookup"><span data-stu-id="4ef95-119">operations</span></span>|<span data-ttu-id="4ef95-120">Colección de [OnenoteOperation](onenoteoperation.md)</span><span class="sxs-lookup"><span data-stu-id="4ef95-120">[OnenoteOperation](onenoteoperation.md) collection</span></span> |<span data-ttu-id="4ef95-p102">El estado de las operaciones de OneNote. No se admite la obtención de una colección de operaciones, pero puede obtener el estado de las operaciones de larga duración si el encabezado `Operation-Location` se devuelve en la respuesta. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="4ef95-p102">The status of OneNote operations. Getting an operations collection is not supported, but you can get the status of long-running operations if the `Operation-Location` header is returned in the response. Read-only. Nullable.</span></span>|
|<span data-ttu-id="4ef95-125">pages</span><span class="sxs-lookup"><span data-stu-id="4ef95-125">pages</span></span>|<span data-ttu-id="4ef95-126">Colección de [OnenotePage](page.md)</span><span class="sxs-lookup"><span data-stu-id="4ef95-126">[OnenotePage](page.md) collection</span></span>|<span data-ttu-id="4ef95-p103">Páginas de todos los blocs de notas de OneNote que son propiedad del usuario o grupo.  Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="4ef95-p103">The pages in all OneNote notebooks that are owned by the user or group.  Read-only. Nullable.</span></span>|
|<span data-ttu-id="4ef95-130">resources</span><span class="sxs-lookup"><span data-stu-id="4ef95-130">resources</span></span>|<span data-ttu-id="4ef95-131">Colección de [OnenoteResource](resource.md)</span><span class="sxs-lookup"><span data-stu-id="4ef95-131">[OnenoteResource](resource.md) collection</span></span> |<span data-ttu-id="4ef95-p104">Imagen y otros recursos de archivo en páginas de OneNote. No se admite la obtención de una colección de recursos, pero puede [obtener el contenido binario de un determinado recurso](resource.md). Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="4ef95-p104">The image and other file resources in OneNote pages. Getting a resources collection is not supported, but you can [get the binary content of a specific resource](resource.md). Read-only. Nullable.</span></span>|
|<span data-ttu-id="4ef95-136">sectionGroups</span><span class="sxs-lookup"><span data-stu-id="4ef95-136">sectionGroups</span></span>|<span data-ttu-id="4ef95-137">Colección [SectionGroup](sectiongroup.md)</span><span class="sxs-lookup"><span data-stu-id="4ef95-137">[SectionGroup](sectiongroup.md) collection</span></span>|<span data-ttu-id="4ef95-p105">Grupos de secciones de todos los blocs de notas de OneNote que son propiedad del usuario o grupo.  Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="4ef95-p105">The section groups in all OneNote notebooks that are owned by the user or group.  Read-only. Nullable.</span></span>|
|<span data-ttu-id="4ef95-141">sections</span><span class="sxs-lookup"><span data-stu-id="4ef95-141">sections</span></span>|<span data-ttu-id="4ef95-142">Colección de [OnenoteSection](section.md)</span><span class="sxs-lookup"><span data-stu-id="4ef95-142">[OnenoteSection](section.md) collection</span></span>|<span data-ttu-id="4ef95-p106">Secciones de todos los blocs de notas de OneNote que son propiedad del usuario o grupo. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="4ef95-p106">The sections in all OneNote notebooks that are owned by the user or group.  Read-only. Nullable.</span></span>|

## <a name="methods"></a><span data-ttu-id="4ef95-146">Métodos</span><span class="sxs-lookup"><span data-stu-id="4ef95-146">Methods</span></span>

| <span data-ttu-id="4ef95-147">Método</span><span class="sxs-lookup"><span data-stu-id="4ef95-147">Method</span></span>           | <span data-ttu-id="4ef95-148">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4ef95-148">Return Type</span></span>    |<span data-ttu-id="4ef95-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="4ef95-149">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="4ef95-150">Crear bloc de notas</span><span class="sxs-lookup"><span data-stu-id="4ef95-150">Create notebook</span></span>](../api/onenote_post_notebooks.md) |[<span data-ttu-id="4ef95-151">Notebook</span><span class="sxs-lookup"><span data-stu-id="4ef95-151">Notebook</span></span>](notebook.md)| <span data-ttu-id="4ef95-152">Crear un bloc de notas mediante su publicación en la colección de blocs de notas.</span><span class="sxs-lookup"><span data-stu-id="4ef95-152">Create a notebook by posting to the notebooks collection.</span></span>|
|[<span data-ttu-id="4ef95-153">Enumerar los blocs de notas</span><span class="sxs-lookup"><span data-stu-id="4ef95-153">List notebooks</span></span>](../api/onenote_list_notebooks.md) |<span data-ttu-id="4ef95-154">Colección de [notebook](notebook.md)</span><span class="sxs-lookup"><span data-stu-id="4ef95-154">[Notebook](notebook.md) collection</span></span>| <span data-ttu-id="4ef95-155">Obtener una colección de blocs de notas.</span><span class="sxs-lookup"><span data-stu-id="4ef95-155">Get a collection of notebooks.</span></span>|
|[<span data-ttu-id="4ef95-156">Crear página</span><span class="sxs-lookup"><span data-stu-id="4ef95-156">Create page</span></span>](../api/onenote_post_pages.md) |[<span data-ttu-id="4ef95-157">Page</span><span class="sxs-lookup"><span data-stu-id="4ef95-157">Page</span></span>](page.md)| <span data-ttu-id="4ef95-158">Crear una página mediante su publicación en la colección de páginas.</span><span class="sxs-lookup"><span data-stu-id="4ef95-158">Create a page by posting to the pages collection.</span></span>|
|[<span data-ttu-id="4ef95-159">Enumerar páginas</span><span class="sxs-lookup"><span data-stu-id="4ef95-159">List pages</span></span>](../api/onenote_list_pages.md) |<span data-ttu-id="4ef95-160">Colección de [page](page.md)</span><span class="sxs-lookup"><span data-stu-id="4ef95-160">[Page](page.md) collection</span></span>| <span data-ttu-id="4ef95-161">Obtener una colección de páginas.</span><span class="sxs-lookup"><span data-stu-id="4ef95-161">Get a collection of pages.</span></span>|
|[<span data-ttu-id="4ef95-162">Enumerar grupos de sección</span><span class="sxs-lookup"><span data-stu-id="4ef95-162">List section groups</span></span>](../api/onenote_list_sectiongroups.md) |<span data-ttu-id="4ef95-163">Colección de [SectionGroup](sectiongroup.md)</span><span class="sxs-lookup"><span data-stu-id="4ef95-163">[SectionGroup](sectiongroup.md) collection</span></span>| <span data-ttu-id="4ef95-164">Obtener una colección de grupos de secciones.</span><span class="sxs-lookup"><span data-stu-id="4ef95-164">Get a collection of section groups.</span></span>|
|[<span data-ttu-id="4ef95-165">Enumerar secciones</span><span class="sxs-lookup"><span data-stu-id="4ef95-165">List sections</span></span>](../api/onenote_list_sections.md) |<span data-ttu-id="4ef95-166">Colección de [OnenoteSection](section.md)</span><span class="sxs-lookup"><span data-stu-id="4ef95-166">[OnenoteSection](section.md) collection</span></span>| <span data-ttu-id="4ef95-167">Obtener una colección de secciones.</span><span class="sxs-lookup"><span data-stu-id="4ef95-167">Get a collection of sections.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="4ef95-168">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4ef95-168">JSON Representation</span></span>
<span data-ttu-id="4ef95-169">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4ef95-169">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.onenote"
}-->
``` json
{
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onenote resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
