---
title: Tipo de recurso onenote
description: Punto de entrada para los recursos de OneNote.
author: jewan-microsoft
localization_priority: Normal
ms.prod: onenote
ms.openlocfilehash: 2b6818ac5f9bd9bdc60d1c0d1e0cc8f80afc1f65
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27970671"
---
# <a name="onenote-resource-type"></a><span data-ttu-id="dfeb9-103">Tipo de recurso onenote</span><span class="sxs-lookup"><span data-stu-id="dfeb9-103">onenote resource type</span></span>

> <span data-ttu-id="dfeb9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="dfeb9-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="dfeb9-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="dfeb9-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="dfeb9-106">Punto de entrada para los recursos de OneNote.</span><span class="sxs-lookup"><span data-stu-id="dfeb9-106">The entry point for OneNote resources.</span></span>

<span data-ttu-id="dfeb9-107">Todas las llamadas al servicio de OneNote a través de la API de Microsoft Graph utilizan esta dirección URL raíz del servicio:</span><span class="sxs-lookup"><span data-stu-id="dfeb9-107">All calls to the OneNote service through the Microsoft Graph API use this service root URL:</span></span>

```
https://graph.microsoft.com/{version}/{location}/onenote/ 
```

<span data-ttu-id="dfeb9-108">La ubicación puede ser blocs de notas de usuario en Office 365 o consumidor OneDrive, los blocs de notas de grupo o los blocs de notas de equipo hospedada en el sitio de SharePoint en Office 365.</span><span class="sxs-lookup"><span data-stu-id="dfeb9-108">The location can be user notebooks on Office 365 or consumer OneDrive, group notebooks, or SharePoint site-hosted team notebooks on Office 365.</span></span> 

<span data-ttu-id="dfeb9-109">**Blocs de notas del usuario** Para obtener acceso a los blocs de notas personales en OneDrive para el cliente o OneDrive para la Empresa, utilice una de las siguientes direcciones URL:</span><span class="sxs-lookup"><span data-stu-id="dfeb9-109">**User notebooks** To access personal notebooks on consumer OneDrive or OneDrive for Business, use one of the following URLs:</span></span>

```
https://graph.microsoft.com/{version}/me/onenote/{notebooks | sections | sectionGroups | pages} 
https://graph.microsoft.com/{version}/users/{userPrincipalName}/onenote/{notebooks | sections | sectionGroups | pages} 
https://graph.microsoft.com/{version}/users/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```

<span data-ttu-id="dfeb9-110">**Blocs de notas de grupo** Para obtener acceso a los blocs de notas que pertenecen a un grupo, utilice la siguiente dirección URL raíz de servicio:</span><span class="sxs-lookup"><span data-stu-id="dfeb9-110">**Group notebooks** To access notebooks that are owned by a group, use the following service root URL:</span></span>

```
https://graph.microsoft.com/{version}/groups/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```
<span data-ttu-id="dfeb9-111">**Blocs de notas de sitio de SharePoint** Para obtener acceso a los blocs de notas que pertenecen a un sitio de grupo de SharePoint, use la siguiente dirección URL raíz de servicio:</span><span class="sxs-lookup"><span data-stu-id="dfeb9-111">**SharePoint site notebooks** To access notebooks that are owned by a SharePoint team site, use the following service root URL:</span></span>

```
https://graph.microsoft.com/{version}/sites/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```

## <a name="authorization"></a><span data-ttu-id="dfeb9-112">Autorización</span><span class="sxs-lookup"><span data-stu-id="dfeb9-112">Authorization</span></span>

<span data-ttu-id="dfeb9-113">Para obtener información sobre los permisos necesarios para trabajar con las API de OneNote, consulte [Permisos de notas](/graph/permissions-reference#notes-permissions).</span><span class="sxs-lookup"><span data-stu-id="dfeb9-113">For information about the permissions required to work with OneNote APIs, see [Notes permissions](/graph/permissions-reference#notes-permissions).</span></span>

## <a name="relationships"></a><span data-ttu-id="dfeb9-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="dfeb9-114">Relationships</span></span>
| <span data-ttu-id="dfeb9-115">Relación</span><span class="sxs-lookup"><span data-stu-id="dfeb9-115">Relationship</span></span> | <span data-ttu-id="dfeb9-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="dfeb9-116">Type</span></span>   |<span data-ttu-id="dfeb9-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="dfeb9-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="dfeb9-118">notebooks</span><span class="sxs-lookup"><span data-stu-id="dfeb9-118">notebooks</span></span>|<span data-ttu-id="dfeb9-119">Colección de [notebook](notebook.md)</span><span class="sxs-lookup"><span data-stu-id="dfeb9-119">[Notebook](notebook.md) collection</span></span>|<span data-ttu-id="dfeb9-p102">Colección de blocs de notas de OneNote que son propiedad del usuario o grupo. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="dfeb9-p102">The collection of OneNote notebooks that are owned by the user or group. Read-only. Nullable.</span></span>|
|<span data-ttu-id="dfeb9-123">operations</span><span class="sxs-lookup"><span data-stu-id="dfeb9-123">operations</span></span>|<span data-ttu-id="dfeb9-124">Colección de [operations](onenoteoperation.md)</span><span class="sxs-lookup"><span data-stu-id="dfeb9-124">[Operation](onenoteoperation.md) collection</span></span> |<span data-ttu-id="dfeb9-p103">El estado de las operaciones de OneNote. No se admite la obtención de una colección de operaciones, pero puede obtener el estado de las operaciones de larga duración si el encabezado `Operation-Location` se devuelve en la respuesta. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="dfeb9-p103">The status of OneNote operations. Getting an operations collection is not supported, but you can get the status of long-running operations if the `Operation-Location` header is returned in the response. Read-only. Nullable.</span></span>|
|<span data-ttu-id="dfeb9-129">pages</span><span class="sxs-lookup"><span data-stu-id="dfeb9-129">pages</span></span>|<span data-ttu-id="dfeb9-130">Colección de [page](page.md)</span><span class="sxs-lookup"><span data-stu-id="dfeb9-130">[Page](page.md) collection</span></span>|<span data-ttu-id="dfeb9-p104">Páginas de todos los blocs de notas de OneNote que son propiedad del usuario o grupo.  Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="dfeb9-p104">The pages in all OneNote notebooks that are owned by the user or group.  Read-only. Nullable.</span></span>|
|<span data-ttu-id="dfeb9-134">resources</span><span class="sxs-lookup"><span data-stu-id="dfeb9-134">resources</span></span>|<span data-ttu-id="dfeb9-135">Colección de [resources](resource.md)</span><span class="sxs-lookup"><span data-stu-id="dfeb9-135">[Resource](resource.md) collection</span></span> |<span data-ttu-id="dfeb9-p105">Imagen y otros recursos de archivo en páginas de OneNote. No se admite la obtención de una colección de recursos, pero puede [obtener el contenido binario de un determinado recurso](resource.md). Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="dfeb9-p105">The image and other file resources in OneNote pages. Getting a resources collection is not supported, but you can [get the binary content of a specific resource](resource.md). Read-only. Nullable.</span></span>|
|<span data-ttu-id="dfeb9-140">sectionGroups</span><span class="sxs-lookup"><span data-stu-id="dfeb9-140">sectionGroups</span></span>|<span data-ttu-id="dfeb9-141">Colección [SectionGroup](sectiongroup.md)</span><span class="sxs-lookup"><span data-stu-id="dfeb9-141">[SectionGroup](sectiongroup.md) collection</span></span>|<span data-ttu-id="dfeb9-p106">Grupos de secciones de todos los blocs de notas de OneNote que son propiedad del usuario o grupo.  Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="dfeb9-p106">The section groups in all OneNote notebooks that are owned by the user or group.  Read-only. Nullable.</span></span>|
|<span data-ttu-id="dfeb9-145">sections</span><span class="sxs-lookup"><span data-stu-id="dfeb9-145">sections</span></span>|<span data-ttu-id="dfeb9-146">Colección de [secciones](section.md)</span><span class="sxs-lookup"><span data-stu-id="dfeb9-146">[Section](section.md) collection</span></span>|<span data-ttu-id="dfeb9-p107">Secciones de todos los blocs de notas de OneNote que son propiedad del usuario o grupo.  Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="dfeb9-p107">The sections in all OneNote notebooks that are owned by the user or group.  Read-only. Nullable.</span></span>|

## <a name="methods"></a><span data-ttu-id="dfeb9-150">Métodos</span><span class="sxs-lookup"><span data-stu-id="dfeb9-150">Methods</span></span>

| <span data-ttu-id="dfeb9-151">Método</span><span class="sxs-lookup"><span data-stu-id="dfeb9-151">Method</span></span>           | <span data-ttu-id="dfeb9-152">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dfeb9-152">Return Type</span></span>    |<span data-ttu-id="dfeb9-153">Descripción</span><span class="sxs-lookup"><span data-stu-id="dfeb9-153">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="dfeb9-154">Crear bloc de notas</span><span class="sxs-lookup"><span data-stu-id="dfeb9-154">Create notebook</span></span>](../api/onenote-post-notebooks.md) |[<span data-ttu-id="dfeb9-155">Notebook</span><span class="sxs-lookup"><span data-stu-id="dfeb9-155">Notebook</span></span>](notebook.md)| <span data-ttu-id="dfeb9-156">Crear un bloc de notas mediante su publicación en la colección de blocs de notas.</span><span class="sxs-lookup"><span data-stu-id="dfeb9-156">Create a notebook by posting to the notebooks collection.</span></span>|
|[<span data-ttu-id="dfeb9-157">Enumerar los blocs de notas</span><span class="sxs-lookup"><span data-stu-id="dfeb9-157">List notebooks</span></span>](../api/onenote-list-notebooks.md) |<span data-ttu-id="dfeb9-158">Colección de [notebook](notebook.md)</span><span class="sxs-lookup"><span data-stu-id="dfeb9-158">[Notebook](notebook.md) collection</span></span>| <span data-ttu-id="dfeb9-159">Obtener una colección de blocs de notas.</span><span class="sxs-lookup"><span data-stu-id="dfeb9-159">Get a collection of notebooks.</span></span>|
|[<span data-ttu-id="dfeb9-160">Crear página</span><span class="sxs-lookup"><span data-stu-id="dfeb9-160">Create page</span></span>](../api/onenote-post-pages.md) |[<span data-ttu-id="dfeb9-161">Page</span><span class="sxs-lookup"><span data-stu-id="dfeb9-161">Page</span></span>](page.md)| <span data-ttu-id="dfeb9-162">Crear una página mediante su publicación en la colección de páginas.</span><span class="sxs-lookup"><span data-stu-id="dfeb9-162">Create a page by posting to the pages collection.</span></span>|
|[<span data-ttu-id="dfeb9-163">Enumerar páginas</span><span class="sxs-lookup"><span data-stu-id="dfeb9-163">List pages</span></span>](../api/onenote-list-pages.md) |<span data-ttu-id="dfeb9-164">Colección de [page](page.md)</span><span class="sxs-lookup"><span data-stu-id="dfeb9-164">[Page](page.md) collection</span></span>| <span data-ttu-id="dfeb9-165">Obtener una colección de páginas.</span><span class="sxs-lookup"><span data-stu-id="dfeb9-165">Get a collection of pages.</span></span>|
|[<span data-ttu-id="dfeb9-166">Enumerar grupos de sección</span><span class="sxs-lookup"><span data-stu-id="dfeb9-166">List section groups</span></span>](../api/onenote-list-sectiongroups.md) |<span data-ttu-id="dfeb9-167">Colección de [SectionGroup](sectiongroup.md)</span><span class="sxs-lookup"><span data-stu-id="dfeb9-167">[SectionGroup](sectiongroup.md) collection</span></span>| <span data-ttu-id="dfeb9-168">Obtener una colección de grupos de secciones.</span><span class="sxs-lookup"><span data-stu-id="dfeb9-168">Get a collection of section groups.</span></span>|
|[<span data-ttu-id="dfeb9-169">Enumerar secciones</span><span class="sxs-lookup"><span data-stu-id="dfeb9-169">List sections</span></span>](../api/onenote-list-sections.md) |<span data-ttu-id="dfeb9-170">Colección de [secciones](section.md)</span><span class="sxs-lookup"><span data-stu-id="dfeb9-170">[Section](section.md) collection</span></span>| <span data-ttu-id="dfeb9-171">Obtener una colección de secciones.</span><span class="sxs-lookup"><span data-stu-id="dfeb9-171">Get a collection of sections.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onenote resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
