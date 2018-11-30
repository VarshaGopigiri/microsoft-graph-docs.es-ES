---
title: Tipo de recurso section
description: Una sección en un bloc de notas de OneNote. Las secciones pueden contener páginas.
ms.openlocfilehash: c07f8f2e5c9f9f9d367cbc1186983c0870b2e979
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083830"
---
# <a name="section-resource-type"></a><span data-ttu-id="b2721-104">Tipo de recurso section</span><span class="sxs-lookup"><span data-stu-id="b2721-104">section resource type</span></span>

> <span data-ttu-id="b2721-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b2721-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b2721-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b2721-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b2721-p103">Una sección en un bloc de notas de OneNote. Las secciones pueden contener páginas.</span><span class="sxs-lookup"><span data-stu-id="b2721-p103">A section in a OneNote notebook. Sections can contain pages.</span></span>

## <a name="json-representation"></a><span data-ttu-id="b2721-109">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b2721-109">JSON representation</span></span>

<span data-ttu-id="b2721-110">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b2721-110">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "pages",
    "parentNotebook",
    "parentSectionGroup"
  ],
  "@odata.type": "microsoft.graph.onenoteSection"
}-->

```json
{
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "createdDateTime": "String (timestamp)",
  "id": "string (identifier)",
  "isDefault": true,
  "lastModifiedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "lastModifiedDateTime": "String (timestamp)",
  "links": {"@odata.type": "microsoft.graph.sectionLinks"},
  "displayName": "string",
  "pagesUrl": "string",
  "self": "string"
}

```
## <a name="properties"></a><span data-ttu-id="b2721-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b2721-111">Properties</span></span>
| <span data-ttu-id="b2721-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b2721-112">Property</span></span>     | <span data-ttu-id="b2721-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="b2721-113">Type</span></span>   |<span data-ttu-id="b2721-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2721-114">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b2721-115">createdBy</span><span class="sxs-lookup"><span data-stu-id="b2721-115">createdBy</span></span>|[<span data-ttu-id="b2721-116">identitySet</span><span class="sxs-lookup"><span data-stu-id="b2721-116">identitySet</span></span>](identityset.md)|<span data-ttu-id="b2721-p104">Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b2721-p104">Identity of the user, device, and application which created the item. Read-only.</span></span>|
|<span data-ttu-id="b2721-119">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="b2721-119">createdDateTime</span></span>|<span data-ttu-id="b2721-120">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b2721-120">DateTimeOffset</span></span>|<span data-ttu-id="b2721-p105">La fecha y la hora en que se creó la sección. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b2721-p105">The date and time when the section was created. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|
|<span data-ttu-id="b2721-125">id</span><span class="sxs-lookup"><span data-stu-id="b2721-125">id</span></span>|<span data-ttu-id="b2721-126">String</span><span class="sxs-lookup"><span data-stu-id="b2721-126">String</span></span>|<span data-ttu-id="b2721-p106">El identificador único de la sección.  Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b2721-p106">The unique identifier of the section.  Read-only.</span></span>|
|<span data-ttu-id="b2721-129">isDefault</span><span class="sxs-lookup"><span data-stu-id="b2721-129">isDefault</span></span>|<span data-ttu-id="b2721-130">Booleano</span><span class="sxs-lookup"><span data-stu-id="b2721-130">Boolean</span></span>|<span data-ttu-id="b2721-p107">Indica si se trata de la sección predeterminada del usuario. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b2721-p107">Indicates whether this is the user's default section. Read-only.</span></span>|
|<span data-ttu-id="b2721-133">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="b2721-133">lastModifiedBy</span></span>|[<span data-ttu-id="b2721-134">identitySet</span><span class="sxs-lookup"><span data-stu-id="b2721-134">identitySet</span></span>](identityset.md)|<span data-ttu-id="b2721-p108">Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b2721-p108">Identity of the user, device, and application which created the item. Read-only.</span></span>|
|<span data-ttu-id="b2721-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="b2721-137">lastModifiedDateTime</span></span>|<span data-ttu-id="b2721-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b2721-138">DateTimeOffset</span></span>|<span data-ttu-id="b2721-p109">La fecha y la hora en que se modificó la sección por última vez. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b2721-p109">The date and time when the section was last modified. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|
|<span data-ttu-id="b2721-143">vínculos</span><span class="sxs-lookup"><span data-stu-id="b2721-143">links</span></span>|[<span data-ttu-id="b2721-144">SectionLinks</span><span class="sxs-lookup"><span data-stu-id="b2721-144">SectionLinks</span></span>](sectionlinks.md)|<span data-ttu-id="b2721-p110">Vínculos para abrir la sección. El vínculo `oneNoteClientURL` abre la sección en el cliente nativo de OneNote si está instalado. El vínculo `oneNoteWebURL` abre la sección en OneNote Online.</span><span class="sxs-lookup"><span data-stu-id="b2721-p110">Links for opening the section. The `oneNoteClientURL` link opens the section in the OneNote native client if it's installed. The `oneNoteWebURL` link opens the section in OneNote Online.</span></span>|
|<span data-ttu-id="b2721-148">displayName</span><span class="sxs-lookup"><span data-stu-id="b2721-148">displayName</span></span>|<span data-ttu-id="b2721-149">String</span><span class="sxs-lookup"><span data-stu-id="b2721-149">String</span></span>|<span data-ttu-id="b2721-150">Nombre de la sección.</span><span class="sxs-lookup"><span data-stu-id="b2721-150">The name of the section.</span></span> |
|<span data-ttu-id="b2721-151">pagesUrl</span><span class="sxs-lookup"><span data-stu-id="b2721-151">pagesUrl</span></span>|<span data-ttu-id="b2721-152">Cadena</span><span class="sxs-lookup"><span data-stu-id="b2721-152">String</span></span>|<span data-ttu-id="b2721-p111">El punto de conexión `pages` donde puede obtener información detallada de todas las páginas de la sección. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b2721-p111">The `pages` endpoint where you can get details for all the pages in the section. Read-only.</span></span>|
|<span data-ttu-id="b2721-155">self</span><span class="sxs-lookup"><span data-stu-id="b2721-155">self</span></span>|<span data-ttu-id="b2721-156">String</span><span class="sxs-lookup"><span data-stu-id="b2721-156">String</span></span>|<span data-ttu-id="b2721-p112">El punto de conexión donde puede obtener información detallada sobre la sección. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b2721-p112">The endpoint where you can get details about the section. Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="b2721-159">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b2721-159">Relationships</span></span>
| <span data-ttu-id="b2721-160">Relación</span><span class="sxs-lookup"><span data-stu-id="b2721-160">Relationship</span></span> | <span data-ttu-id="b2721-161">Tipo</span><span class="sxs-lookup"><span data-stu-id="b2721-161">Type</span></span>   |<span data-ttu-id="b2721-162">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2721-162">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b2721-163">pages</span><span class="sxs-lookup"><span data-stu-id="b2721-163">pages</span></span>|<span data-ttu-id="b2721-164">Colección [Page](page.md)</span><span class="sxs-lookup"><span data-stu-id="b2721-164">[Page](page.md) collection</span></span>|<span data-ttu-id="b2721-p113">Colección de páginas de la sección.  Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="b2721-p113">The collection of pages in the section.  Read-only. Nullable.</span></span>|
|<span data-ttu-id="b2721-168">parentNotebook</span><span class="sxs-lookup"><span data-stu-id="b2721-168">parentNotebook</span></span>|[<span data-ttu-id="b2721-169">Notebook</span><span class="sxs-lookup"><span data-stu-id="b2721-169">Notebook</span></span>](notebook.md)|<span data-ttu-id="b2721-p114">Bloc de notas que contiene la sección.  Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b2721-p114">The notebook that contains the section.  Read-only.</span></span>|
|<span data-ttu-id="b2721-172">parentSectionGroup</span><span class="sxs-lookup"><span data-stu-id="b2721-172">parentSectionGroup</span></span>|[<span data-ttu-id="b2721-173">SectionGroup</span><span class="sxs-lookup"><span data-stu-id="b2721-173">SectionGroup</span></span>](sectiongroup.md)|<span data-ttu-id="b2721-p115">Grupo de secciones que contiene la sección.  Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b2721-p115">The section group that contains the section.  Read-only.</span></span>|

## <a name="methods"></a><span data-ttu-id="b2721-176">Métodos</span><span class="sxs-lookup"><span data-stu-id="b2721-176">Methods</span></span>

| <span data-ttu-id="b2721-177">Método</span><span class="sxs-lookup"><span data-stu-id="b2721-177">Method</span></span>           | <span data-ttu-id="b2721-178">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b2721-178">Return Type</span></span>    |<span data-ttu-id="b2721-179">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2721-179">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="b2721-180">Obtener sección</span><span class="sxs-lookup"><span data-stu-id="b2721-180">Get section</span></span>](../api/section-get.md) | [<span data-ttu-id="b2721-181">Section</span><span class="sxs-lookup"><span data-stu-id="b2721-181">Section</span></span>](section.md) |<span data-ttu-id="b2721-182">Leer las propiedades y las relaciones de la sección.</span><span class="sxs-lookup"><span data-stu-id="b2721-182">Read the properties and relationships of the section.</span></span>|
|[<span data-ttu-id="b2721-183">Crear página</span><span class="sxs-lookup"><span data-stu-id="b2721-183">Create page</span></span>](../api/section-post-pages.md) |[<span data-ttu-id="b2721-184">Page</span><span class="sxs-lookup"><span data-stu-id="b2721-184">Page</span></span>](page.md)| <span data-ttu-id="b2721-185">Crear una página publicándola en la sección especificada de la colección de páginas.</span><span class="sxs-lookup"><span data-stu-id="b2721-185">Create a page by posting to the pages collection in the specified section.</span></span>|
|[<span data-ttu-id="b2721-186">Enumerar páginas</span><span class="sxs-lookup"><span data-stu-id="b2721-186">List pages</span></span>](../api/section-list-pages.md) |<span data-ttu-id="b2721-187">Colección [Page](page.md)</span><span class="sxs-lookup"><span data-stu-id="b2721-187">[Page](page.md) collection</span></span>| <span data-ttu-id="b2721-188">Obtener una colección de páginas en la sección especificada.</span><span class="sxs-lookup"><span data-stu-id="b2721-188">Get a collection of pages in the specified section.</span></span>|
|[<span data-ttu-id="b2721-189">copyToNotebook</span><span class="sxs-lookup"><span data-stu-id="b2721-189">copyToNotebook</span></span>](../api/section-copytonotebook.md)|<span data-ttu-id="b2721-190">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b2721-190">None</span></span>|<span data-ttu-id="b2721-191">Copiar la sección en un bloc de notas específico.</span><span class="sxs-lookup"><span data-stu-id="b2721-191">Copy the section to a specific notebook.</span></span>|
|[<span data-ttu-id="b2721-192">copyToSectionGroup</span><span class="sxs-lookup"><span data-stu-id="b2721-192">copyToSectionGroup</span></span>](../api/section-copytosectiongroup.md)|<span data-ttu-id="b2721-193">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b2721-193">None</span></span>|<span data-ttu-id="b2721-194">Copiar la sección en un grupo de secciones específico.</span><span class="sxs-lookup"><span data-stu-id="b2721-194">Copy the section to a specific section group.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onenoteSection resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
