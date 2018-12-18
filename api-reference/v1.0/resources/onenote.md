---
title: Tipo de recurso onenote
description: Punto de entrada para los recursos de OneNote.
author: Jewan-microsoft
ms.openlocfilehash: 9570b99aad96196af6d21f41352dada9f4b869b1
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27343655"
---
# <a name="onenote-resource-type"></a><span data-ttu-id="40ea9-103">Tipo de recurso onenote</span><span class="sxs-lookup"><span data-stu-id="40ea9-103">onenote resource type</span></span>

<span data-ttu-id="40ea9-104">Punto de entrada para los recursos de OneNote.</span><span class="sxs-lookup"><span data-stu-id="40ea9-104">The entry point for OneNote resources.</span></span>

<span data-ttu-id="40ea9-105">Todas las llamadas al servicio de OneNote a través de la API de Microsoft Graph utilizan esta dirección URL raíz del servicio:</span><span class="sxs-lookup"><span data-stu-id="40ea9-105">All calls to the OneNote service through the Microsoft Graph API use this service root URL:</span></span>

```
https://graph.microsoft.com/{version}/{location}/onenote/ 
```

<span data-ttu-id="40ea9-106">La ubicación puede ser el bloc de notas del usuario en Office 365 o OneDrive para el cliente, los blocs de notas de grupo o blocs de notas de grupo hospedados en un sitio de SharePoint en Office 365.</span><span class="sxs-lookup"><span data-stu-id="40ea9-106">The location can be user notebooks on Office 365 or consumer OneDrive, group notebooks or SharePoint site-hosted team notebooks on Office 365.</span></span> 

<span data-ttu-id="40ea9-107">**Blocs de notas del usuario** Para obtener acceso a los blocs de notas personales en OneDrive para el cliente o OneDrive para la Empresa, utilice una de las siguientes direcciones URL:</span><span class="sxs-lookup"><span data-stu-id="40ea9-107">**User notebooks** To access personal notebooks on consumer OneDrive or OneDrive for Business, use one of the following URLs:</span></span>

```
https://graph.microsoft.com/{version}/me/onenote/{notebooks | sections | sectionGroups | pages} 
https://graph.microsoft.com/{version}/users/{userPrincipalName}/onenote/{notebooks | sections | sectionGroups | pages} 
https://graph.microsoft.com/{version}/users/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```

<span data-ttu-id="40ea9-108">**Blocs de notas de grupo** Para obtener acceso a los blocs de notas que pertenecen a un grupo, utilice la siguiente dirección URL raíz de servicio:</span><span class="sxs-lookup"><span data-stu-id="40ea9-108">**Group notebooks** To access notebooks that are owned by a group, use the following service root URL:</span></span>

```
https://graph.microsoft.com/{version}/groups/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```
<span data-ttu-id="40ea9-109">**Blocs de notas de sitio de SharePoint** Para obtener acceso a los blocs de notas que pertenecen a un sitio de grupo de SharePoint, use la siguiente dirección URL raíz de servicio:</span><span class="sxs-lookup"><span data-stu-id="40ea9-109">**SharePoint site notebooks** To access notebooks that are owned by a SharePoint team site, use the following service root URL:</span></span>

```
https://graph.microsoft.com/{version}/sites/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```
## <a name="authorization"></a><span data-ttu-id="40ea9-110">Autorización</span><span class="sxs-lookup"><span data-stu-id="40ea9-110">Authorization</span></span>

<span data-ttu-id="40ea9-111">Para obtener información sobre los permisos necesarios para trabajar con las API de OneNote, consulte [Permisos de notas](/graph/permissions-reference#notes-permissions).</span><span class="sxs-lookup"><span data-stu-id="40ea9-111">For information about the permissions required to work with OneNote APIs, see [Notes permissions](/graph/permissions-reference#notes-permissions).</span></span>


## <a name="relationships"></a><span data-ttu-id="40ea9-112">Relaciones</span><span class="sxs-lookup"><span data-stu-id="40ea9-112">Relationships</span></span>
| <span data-ttu-id="40ea9-113">Relación</span><span class="sxs-lookup"><span data-stu-id="40ea9-113">Relationship</span></span> | <span data-ttu-id="40ea9-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="40ea9-114">Type</span></span>   |<span data-ttu-id="40ea9-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="40ea9-115">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="40ea9-116">notebooks</span><span class="sxs-lookup"><span data-stu-id="40ea9-116">notebooks</span></span>|<span data-ttu-id="40ea9-117">Colección de [notebook](notebook.md)</span><span class="sxs-lookup"><span data-stu-id="40ea9-117">[Notebook](notebook.md) collection</span></span>|<span data-ttu-id="40ea9-p101">Colección de blocs de notas de OneNote que son propiedad del usuario o grupo. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="40ea9-p101">The collection of OneNote notebooks that are owned by the user or group. Read-only. Nullable.</span></span>|
|<span data-ttu-id="40ea9-121">operations</span><span class="sxs-lookup"><span data-stu-id="40ea9-121">operations</span></span>|<span data-ttu-id="40ea9-122">Colección de [OnenoteOperation](onenoteoperation.md)</span><span class="sxs-lookup"><span data-stu-id="40ea9-122">[OnenoteOperation](onenoteoperation.md) collection</span></span> |<span data-ttu-id="40ea9-p102">El estado de las operaciones de OneNote. No se admite la obtención de una colección de operaciones, pero puede obtener el estado de las operaciones de larga duración si el encabezado `Operation-Location` se devuelve en la respuesta. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="40ea9-p102">The status of OneNote operations. Getting an operations collection is not supported, but you can get the status of long-running operations if the `Operation-Location` header is returned in the response. Read-only. Nullable.</span></span>|
|<span data-ttu-id="40ea9-127">pages</span><span class="sxs-lookup"><span data-stu-id="40ea9-127">pages</span></span>|<span data-ttu-id="40ea9-128">Colección de [OnenotePage](page.md)</span><span class="sxs-lookup"><span data-stu-id="40ea9-128">[OnenotePage](page.md) collection</span></span>|<span data-ttu-id="40ea9-p103">Páginas de todos los blocs de notas de OneNote que son propiedad del usuario o grupo.  Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="40ea9-p103">The pages in all OneNote notebooks that are owned by the user or group.  Read-only. Nullable.</span></span>|
|<span data-ttu-id="40ea9-132">resources</span><span class="sxs-lookup"><span data-stu-id="40ea9-132">resources</span></span>|<span data-ttu-id="40ea9-133">Colección de [OnenoteResource](resource.md)</span><span class="sxs-lookup"><span data-stu-id="40ea9-133">[OnenoteResource](resource.md) collection</span></span> |<span data-ttu-id="40ea9-p104">Imagen y otros recursos de archivo en páginas de OneNote. No se admite la obtención de una colección de recursos, pero puede [obtener el contenido binario de un determinado recurso](resource.md). Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="40ea9-p104">The image and other file resources in OneNote pages. Getting a resources collection is not supported, but you can [get the binary content of a specific resource](resource.md). Read-only. Nullable.</span></span>|
|<span data-ttu-id="40ea9-138">sectionGroups</span><span class="sxs-lookup"><span data-stu-id="40ea9-138">sectionGroups</span></span>|<span data-ttu-id="40ea9-139">Colección [SectionGroup](sectiongroup.md)</span><span class="sxs-lookup"><span data-stu-id="40ea9-139">[SectionGroup](sectiongroup.md) collection</span></span>|<span data-ttu-id="40ea9-p105">Grupos de secciones de todos los blocs de notas de OneNote que son propiedad del usuario o grupo.  Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="40ea9-p105">The section groups in all OneNote notebooks that are owned by the user or group.  Read-only. Nullable.</span></span>|
|<span data-ttu-id="40ea9-143">sections</span><span class="sxs-lookup"><span data-stu-id="40ea9-143">sections</span></span>|<span data-ttu-id="40ea9-144">Colección de [OnenoteSection](section.md)</span><span class="sxs-lookup"><span data-stu-id="40ea9-144">[OnenoteSection](section.md) collection</span></span>|<span data-ttu-id="40ea9-p106">Secciones de todos los blocs de notas de OneNote que son propiedad del usuario o grupo.  Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="40ea9-p106">The sections in all OneNote notebooks that are owned by the user or group.  Read-only. Nullable.</span></span>|

## <a name="methods"></a><span data-ttu-id="40ea9-148">Métodos</span><span class="sxs-lookup"><span data-stu-id="40ea9-148">Methods</span></span>

| <span data-ttu-id="40ea9-149">Método</span><span class="sxs-lookup"><span data-stu-id="40ea9-149">Method</span></span>           | <span data-ttu-id="40ea9-150">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="40ea9-150">Return Type</span></span>    |<span data-ttu-id="40ea9-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="40ea9-151">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="40ea9-152">Crear bloc de notas</span><span class="sxs-lookup"><span data-stu-id="40ea9-152">Create notebook</span></span>](../api/onenote-post-notebooks.md) |[<span data-ttu-id="40ea9-153">Notebook</span><span class="sxs-lookup"><span data-stu-id="40ea9-153">Notebook</span></span>](notebook.md)| <span data-ttu-id="40ea9-154">Crear un bloc de notas mediante su publicación en la colección de blocs de notas.</span><span class="sxs-lookup"><span data-stu-id="40ea9-154">Create a notebook by posting to the notebooks collection.</span></span>|
|[<span data-ttu-id="40ea9-155">Enumerar los blocs de notas</span><span class="sxs-lookup"><span data-stu-id="40ea9-155">List notebooks</span></span>](../api/onenote-list-notebooks.md) |<span data-ttu-id="40ea9-156">Colección de [notebook](notebook.md)</span><span class="sxs-lookup"><span data-stu-id="40ea9-156">[Notebook](notebook.md) collection</span></span>| <span data-ttu-id="40ea9-157">Obtener una colección de blocs de notas.</span><span class="sxs-lookup"><span data-stu-id="40ea9-157">Get a collection of notebooks.</span></span>|
|[<span data-ttu-id="40ea9-158">Crear página</span><span class="sxs-lookup"><span data-stu-id="40ea9-158">Create page</span></span>](../api/onenote-post-pages.md) |[<span data-ttu-id="40ea9-159">Page</span><span class="sxs-lookup"><span data-stu-id="40ea9-159">Page</span></span>](page.md)| <span data-ttu-id="40ea9-160">Crear una página mediante su publicación en la colección de páginas.</span><span class="sxs-lookup"><span data-stu-id="40ea9-160">Create a page by posting to the pages collection.</span></span>|
|[<span data-ttu-id="40ea9-161">Enumerar páginas</span><span class="sxs-lookup"><span data-stu-id="40ea9-161">List pages</span></span>](../api/onenote-list-pages.md) |<span data-ttu-id="40ea9-162">Colección de [page](page.md)</span><span class="sxs-lookup"><span data-stu-id="40ea9-162">[Page](page.md) collection</span></span>| <span data-ttu-id="40ea9-163">Obtener una colección de páginas.</span><span class="sxs-lookup"><span data-stu-id="40ea9-163">Get a collection of pages.</span></span>|
|[<span data-ttu-id="40ea9-164">Enumerar grupos de sección</span><span class="sxs-lookup"><span data-stu-id="40ea9-164">List section groups</span></span>](../api/onenote-list-sectiongroups.md) |<span data-ttu-id="40ea9-165">Colección de [SectionGroup](sectiongroup.md)</span><span class="sxs-lookup"><span data-stu-id="40ea9-165">[SectionGroup](sectiongroup.md) collection</span></span>| <span data-ttu-id="40ea9-166">Obtener una colección de grupos de secciones.</span><span class="sxs-lookup"><span data-stu-id="40ea9-166">Get a collection of section groups.</span></span>|
|[<span data-ttu-id="40ea9-167">Enumerar secciones</span><span class="sxs-lookup"><span data-stu-id="40ea9-167">List sections</span></span>](../api/onenote-list-sections.md) |<span data-ttu-id="40ea9-168">Colección de [OnenoteSection](section.md)</span><span class="sxs-lookup"><span data-stu-id="40ea9-168">[OnenoteSection](section.md) collection</span></span>| <span data-ttu-id="40ea9-169">Obtener una colección de secciones.</span><span class="sxs-lookup"><span data-stu-id="40ea9-169">Get a collection of sections.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="40ea9-170">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="40ea9-170">JSON Representation</span></span>
<span data-ttu-id="40ea9-171">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="40ea9-171">Here is a JSON representation of the resource.</span></span>
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
