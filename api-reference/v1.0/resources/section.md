---
title: Tipo de recurso section
description: Una sección en un bloc de notas de OneNote. Las secciones pueden contener páginas.
localization_priority: Normal
ms.openlocfilehash: f9cb5a8e3ddf9cf4a045103e4ecc7909653d797c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27853238"
---
# <a name="section-resource-type"></a><span data-ttu-id="7fedf-104">Tipo de recurso section</span><span class="sxs-lookup"><span data-stu-id="7fedf-104">section resource type</span></span>

<span data-ttu-id="7fedf-p102">Una sección en un bloc de notas de OneNote. Las secciones pueden contener páginas.</span><span class="sxs-lookup"><span data-stu-id="7fedf-p102">A section in a OneNote notebook. Sections can contain pages.</span></span>

## <a name="json-representation"></a><span data-ttu-id="7fedf-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7fedf-107">JSON representation</span></span>

<span data-ttu-id="7fedf-108">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7fedf-108">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.onenoteEntityHierarchyModel",
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
## <a name="properties"></a><span data-ttu-id="7fedf-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7fedf-109">Properties</span></span>
| <span data-ttu-id="7fedf-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7fedf-110">Property</span></span>     | <span data-ttu-id="7fedf-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="7fedf-111">Type</span></span>   |<span data-ttu-id="7fedf-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="7fedf-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7fedf-113">createdBy</span><span class="sxs-lookup"><span data-stu-id="7fedf-113">createdBy</span></span>|[<span data-ttu-id="7fedf-114">identitySet</span><span class="sxs-lookup"><span data-stu-id="7fedf-114">identitySet</span></span>](identityset.md)|<span data-ttu-id="7fedf-p103">Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7fedf-p103">Identity of the user, device, and application which created the item. Read-only.</span></span>|
|<span data-ttu-id="7fedf-117">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="7fedf-117">createdDateTime</span></span>|<span data-ttu-id="7fedf-118">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7fedf-118">DateTimeOffset</span></span>|<span data-ttu-id="7fedf-p104">La fecha y la hora en que se creó la sección. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7fedf-p104">The date and time when the section was created. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|
|<span data-ttu-id="7fedf-123">id</span><span class="sxs-lookup"><span data-stu-id="7fedf-123">id</span></span>|<span data-ttu-id="7fedf-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="7fedf-124">String</span></span>|<span data-ttu-id="7fedf-p105">El identificador único de la sección.  Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7fedf-p105">The unique identifier of the section.  Read-only.</span></span>|
|<span data-ttu-id="7fedf-127">isDefault</span><span class="sxs-lookup"><span data-stu-id="7fedf-127">isDefault</span></span>|<span data-ttu-id="7fedf-128">Booleano</span><span class="sxs-lookup"><span data-stu-id="7fedf-128">Boolean</span></span>|<span data-ttu-id="7fedf-p106">Indica si se trata de la sección predeterminada del usuario. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7fedf-p106">Indicates whether this is the user's default section. Read-only.</span></span>|
|<span data-ttu-id="7fedf-131">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="7fedf-131">lastModifiedBy</span></span>|[<span data-ttu-id="7fedf-132">identitySet</span><span class="sxs-lookup"><span data-stu-id="7fedf-132">identitySet</span></span>](identityset.md)|<span data-ttu-id="7fedf-p107">Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7fedf-p107">Identity of the user, device, and application which created the item. Read-only.</span></span>|
|<span data-ttu-id="7fedf-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="7fedf-135">lastModifiedDateTime</span></span>|<span data-ttu-id="7fedf-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7fedf-136">DateTimeOffset</span></span>|<span data-ttu-id="7fedf-p108">La fecha y la hora en que se modificó la sección por última vez. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7fedf-p108">The date and time when the section was last modified. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|
|<span data-ttu-id="7fedf-141">vínculos</span><span class="sxs-lookup"><span data-stu-id="7fedf-141">links</span></span>|[<span data-ttu-id="7fedf-142">SectionLinks</span><span class="sxs-lookup"><span data-stu-id="7fedf-142">SectionLinks</span></span>](sectionlinks.md)|<span data-ttu-id="7fedf-p109">Vínculos para abrir la sección. El vínculo `oneNoteClientURL` abre la sección en el cliente nativo de OneNote si está instalado. El vínculo `oneNoteWebURL` abre la sección en OneNote Online.</span><span class="sxs-lookup"><span data-stu-id="7fedf-p109">Links for opening the section. The `oneNoteClientURL` link opens the section in the OneNote native client if it's installed. The `oneNoteWebURL` link opens the section in OneNote Online.</span></span>|
|<span data-ttu-id="7fedf-146">displayName</span><span class="sxs-lookup"><span data-stu-id="7fedf-146">displayName</span></span>|<span data-ttu-id="7fedf-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="7fedf-147">String</span></span>|<span data-ttu-id="7fedf-148">Nombre de la sección.</span><span class="sxs-lookup"><span data-stu-id="7fedf-148">The name of the section.</span></span> |
|<span data-ttu-id="7fedf-149">pagesUrl</span><span class="sxs-lookup"><span data-stu-id="7fedf-149">pagesUrl</span></span>|<span data-ttu-id="7fedf-150">Cadena</span><span class="sxs-lookup"><span data-stu-id="7fedf-150">String</span></span>|<span data-ttu-id="7fedf-p110">El punto de conexión `pages` donde puede obtener información detallada de todas las páginas de la sección. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7fedf-p110">The `pages` endpoint where you can get details for all the pages in the section. Read-only.</span></span>|
|<span data-ttu-id="7fedf-153">self</span><span class="sxs-lookup"><span data-stu-id="7fedf-153">self</span></span>|<span data-ttu-id="7fedf-154">Cadena</span><span class="sxs-lookup"><span data-stu-id="7fedf-154">String</span></span>|<span data-ttu-id="7fedf-p111">El punto de conexión donde puede obtener información detallada sobre la sección. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7fedf-p111">The endpoint where you can get details about the section. Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="7fedf-157">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7fedf-157">Relationships</span></span>
| <span data-ttu-id="7fedf-158">Relación</span><span class="sxs-lookup"><span data-stu-id="7fedf-158">Relationship</span></span> | <span data-ttu-id="7fedf-159">Tipo</span><span class="sxs-lookup"><span data-stu-id="7fedf-159">Type</span></span>   |<span data-ttu-id="7fedf-160">Descripción</span><span class="sxs-lookup"><span data-stu-id="7fedf-160">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7fedf-161">pages</span><span class="sxs-lookup"><span data-stu-id="7fedf-161">pages</span></span>|<span data-ttu-id="7fedf-162">Colección de [OnenotePage](page.md)</span><span class="sxs-lookup"><span data-stu-id="7fedf-162">[OnenotePage](page.md) collection</span></span>|<span data-ttu-id="7fedf-p112">Colección de páginas de la sección.  Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="7fedf-p112">The collection of pages in the section.  Read-only. Nullable.</span></span>|
|<span data-ttu-id="7fedf-166">parentNotebook</span><span class="sxs-lookup"><span data-stu-id="7fedf-166">parentNotebook</span></span>|[<span data-ttu-id="7fedf-167">Notebook</span><span class="sxs-lookup"><span data-stu-id="7fedf-167">Notebook</span></span>](notebook.md)|<span data-ttu-id="7fedf-p113">Bloc de notas que contiene la sección.  Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7fedf-p113">The notebook that contains the section.  Read-only.</span></span>|
|<span data-ttu-id="7fedf-170">parentSectionGroup</span><span class="sxs-lookup"><span data-stu-id="7fedf-170">parentSectionGroup</span></span>|[<span data-ttu-id="7fedf-171">SectionGroup</span><span class="sxs-lookup"><span data-stu-id="7fedf-171">SectionGroup</span></span>](sectiongroup.md)|<span data-ttu-id="7fedf-p114">Grupo de secciones que contiene la sección.  Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7fedf-p114">The section group that contains the section.  Read-only.</span></span>|

## <a name="methods"></a><span data-ttu-id="7fedf-174">Métodos</span><span class="sxs-lookup"><span data-stu-id="7fedf-174">Methods</span></span>

| <span data-ttu-id="7fedf-175">Método</span><span class="sxs-lookup"><span data-stu-id="7fedf-175">Method</span></span>           | <span data-ttu-id="7fedf-176">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7fedf-176">Return Type</span></span>    |<span data-ttu-id="7fedf-177">Descripción</span><span class="sxs-lookup"><span data-stu-id="7fedf-177">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="7fedf-178">Obtener sección</span><span class="sxs-lookup"><span data-stu-id="7fedf-178">Get section</span></span>](../api/section-get.md) | [<span data-ttu-id="7fedf-179">OnenoteSection</span><span class="sxs-lookup"><span data-stu-id="7fedf-179">OnenoteSection</span></span>](section.md) |<span data-ttu-id="7fedf-180">Leer las propiedades y las relaciones de la sección.</span><span class="sxs-lookup"><span data-stu-id="7fedf-180">Read the properties and relationships of the section.</span></span>|
|[<span data-ttu-id="7fedf-181">Crear página</span><span class="sxs-lookup"><span data-stu-id="7fedf-181">Create page</span></span>](../api/section-post-pages.md) |[<span data-ttu-id="7fedf-182">Page</span><span class="sxs-lookup"><span data-stu-id="7fedf-182">Page</span></span>](page.md)| <span data-ttu-id="7fedf-183">Crear una página publicándola en la sección especificada de la colección de páginas.</span><span class="sxs-lookup"><span data-stu-id="7fedf-183">Create a page by posting to the pages collection in the specified section.</span></span>|
|[<span data-ttu-id="7fedf-184">Enumerar páginas</span><span class="sxs-lookup"><span data-stu-id="7fedf-184">List pages</span></span>](../api/section-list-pages.md) |<span data-ttu-id="7fedf-185">Colección [Page](page.md)</span><span class="sxs-lookup"><span data-stu-id="7fedf-185">[Page](page.md) collection</span></span>| <span data-ttu-id="7fedf-186">Obtener una colección de páginas en la sección especificada.</span><span class="sxs-lookup"><span data-stu-id="7fedf-186">Get a collection of pages in the specified section.</span></span>|
|[<span data-ttu-id="7fedf-187">copyToNotebook</span><span class="sxs-lookup"><span data-stu-id="7fedf-187">copyToNotebook</span></span>](../api/section-copytonotebook.md)|<span data-ttu-id="7fedf-188">Ninguno</span><span class="sxs-lookup"><span data-stu-id="7fedf-188">None</span></span>|<span data-ttu-id="7fedf-189">Copiar la sección en un bloc de notas específico.</span><span class="sxs-lookup"><span data-stu-id="7fedf-189">Copy the section to a specific notebook.</span></span>|
|[<span data-ttu-id="7fedf-190">copyToSectionGroup</span><span class="sxs-lookup"><span data-stu-id="7fedf-190">copyToSectionGroup</span></span>](../api/section-copytosectiongroup.md)|<span data-ttu-id="7fedf-191">Ninguno</span><span class="sxs-lookup"><span data-stu-id="7fedf-191">None</span></span>|<span data-ttu-id="7fedf-192">Copiar la sección en un grupo de secciones específico.</span><span class="sxs-lookup"><span data-stu-id="7fedf-192">Copy the section to a specific section group.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onenoteSection resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
