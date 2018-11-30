---
title: Tipo de recurso sectionGroup
description: Un grupo de secciones en un bloc de notas de OneNote. Los grupos de secciones pueden contener secciones y grupos de secciones.
ms.openlocfilehash: 4714d0d163e9ddd01373f50bf38fa0971da0609b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031050"
---
# <a name="sectiongroup-resource-type"></a><span data-ttu-id="39497-104">Tipo de recurso sectionGroup</span><span class="sxs-lookup"><span data-stu-id="39497-104">sectionGroup resource type</span></span>

<span data-ttu-id="39497-p102">Un grupo de secciones en un bloc de notas de OneNote. Los grupos de secciones pueden contener secciones y grupos de secciones.</span><span class="sxs-lookup"><span data-stu-id="39497-p102">A section group in a OneNote notebook. Section groups can contain sections and section groups.</span></span>

## <a name="json-representation"></a><span data-ttu-id="39497-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="39497-107">JSON representation</span></span>

<span data-ttu-id="39497-108">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="39497-108">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.onenoteEntityHierarchyModel",
  "optionalProperties": [
    "parentNotebook",
    "parentSectionGroup",
    "sectionGroups",
    "sections"
  ],
  "@odata.type": "microsoft.graph.sectionGroup"
}-->

```json
{
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "createdDateTime": "String (timestamp)",
  "id": "string (identifier)",
  "lastModifiedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "lastModifiedDateTime": "String (timestamp)",
  "displayName": "string",
  "sectionGroupsUrl": "string",
  "sectionsUrl": "string",
  "self": "string"
}

```
## <a name="properties"></a><span data-ttu-id="39497-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="39497-109">Properties</span></span>
| <span data-ttu-id="39497-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="39497-110">Property</span></span>     | <span data-ttu-id="39497-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="39497-111">Type</span></span>   |<span data-ttu-id="39497-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="39497-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="39497-113">createdBy</span><span class="sxs-lookup"><span data-stu-id="39497-113">createdBy</span></span>|[<span data-ttu-id="39497-114">identitySet</span><span class="sxs-lookup"><span data-stu-id="39497-114">identitySet</span></span>](identityset.md)|<span data-ttu-id="39497-p103">Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="39497-p103">Identity of the user, device, and application which created the item. Read-only.</span></span>|
|<span data-ttu-id="39497-117">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="39497-117">createdDateTime</span></span>|<span data-ttu-id="39497-118">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="39497-118">DateTimeOffset</span></span>|<span data-ttu-id="39497-p104">La fecha y la hora en que se creó el grupo de secciones. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="39497-p104">The date and time when the section group was created. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|
|<span data-ttu-id="39497-123">id</span><span class="sxs-lookup"><span data-stu-id="39497-123">id</span></span>|<span data-ttu-id="39497-124">String</span><span class="sxs-lookup"><span data-stu-id="39497-124">String</span></span>|<span data-ttu-id="39497-p105">El identificador único del grupo de secciones. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="39497-p105">The unique identifier of the section group. Read-only.</span></span>|
|<span data-ttu-id="39497-127">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="39497-127">lastModifiedBy</span></span>|[<span data-ttu-id="39497-128">identitySet</span><span class="sxs-lookup"><span data-stu-id="39497-128">identitySet</span></span>](identityset.md)|<span data-ttu-id="39497-p106">Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="39497-p106">Identity of the user, device, and application which created the item. Read-only.</span></span>|
|<span data-ttu-id="39497-131">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="39497-131">lastModifiedDateTime</span></span>|<span data-ttu-id="39497-132">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="39497-132">DateTimeOffset</span></span>|<span data-ttu-id="39497-p107">La fecha y la hora en que se modificó por última vez el grupo de secciones. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="39497-p107">The date and time when the section group was last modified. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|
|<span data-ttu-id="39497-137">displayName</span><span class="sxs-lookup"><span data-stu-id="39497-137">displayName</span></span>|<span data-ttu-id="39497-138">String</span><span class="sxs-lookup"><span data-stu-id="39497-138">String</span></span>|<span data-ttu-id="39497-139">El nombre del grupo de secciones.</span><span class="sxs-lookup"><span data-stu-id="39497-139">The name of the section group.</span></span>|
|<span data-ttu-id="39497-140">sectionGroupsUrl</span><span class="sxs-lookup"><span data-stu-id="39497-140">sectionGroupsUrl</span></span>|<span data-ttu-id="39497-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="39497-141">String</span></span>|<span data-ttu-id="39497-p108">La dirección URL de la propiedad de navegación `sectionGroups`, que devuelve todos los grupos de secciones del grupo de secciones. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="39497-p108">The URL for the `sectionGroups` navigation property, which returns all the section groups in the section group. Read-only.</span></span>|
|<span data-ttu-id="39497-144">sectionsUrl</span><span class="sxs-lookup"><span data-stu-id="39497-144">sectionsUrl</span></span>|<span data-ttu-id="39497-145">Cadena</span><span class="sxs-lookup"><span data-stu-id="39497-145">String</span></span>|<span data-ttu-id="39497-p109">La dirección URL de la propiedad de navegación `sections`, que devuelve todas las secciones del grupo de secciones. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="39497-p109">The URL for the `sections` navigation property, which returns all the sections in the section group. Read-only.</span></span>|
|<span data-ttu-id="39497-148">self</span><span class="sxs-lookup"><span data-stu-id="39497-148">self</span></span>|<span data-ttu-id="39497-149">String</span><span class="sxs-lookup"><span data-stu-id="39497-149">String</span></span>|<span data-ttu-id="39497-p110">El punto de conexión donde puede obtener información detallada sobre el grupo de secciones. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="39497-p110">The endpoint where you can get details about the section group. Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="39497-152">Relaciones</span><span class="sxs-lookup"><span data-stu-id="39497-152">Relationships</span></span>
| <span data-ttu-id="39497-153">Relación</span><span class="sxs-lookup"><span data-stu-id="39497-153">Relationship</span></span> | <span data-ttu-id="39497-154">Tipo</span><span class="sxs-lookup"><span data-stu-id="39497-154">Type</span></span>   |<span data-ttu-id="39497-155">Descripción</span><span class="sxs-lookup"><span data-stu-id="39497-155">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="39497-156">parentNotebook</span><span class="sxs-lookup"><span data-stu-id="39497-156">parentNotebook</span></span>|[<span data-ttu-id="39497-157">Notebook</span><span class="sxs-lookup"><span data-stu-id="39497-157">Notebook</span></span>](notebook.md)|<span data-ttu-id="39497-p111">Bloc de notas que contiene el grupo de secciones. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="39497-p111">The notebook that contains the section group. Read-only.</span></span>|
|<span data-ttu-id="39497-160">parentSectionGroup</span><span class="sxs-lookup"><span data-stu-id="39497-160">parentSectionGroup</span></span>|[<span data-ttu-id="39497-161">SectionGroup</span><span class="sxs-lookup"><span data-stu-id="39497-161">SectionGroup</span></span>](sectiongroup.md)|<span data-ttu-id="39497-p112">Grupo de secciones que contiene el grupo de secciones. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="39497-p112">The section group that contains the section group. Read-only.</span></span>|
|<span data-ttu-id="39497-164">sectionGroups</span><span class="sxs-lookup"><span data-stu-id="39497-164">sectionGroups</span></span>|<span data-ttu-id="39497-165">Colección [SectionGroup](sectiongroup.md)</span><span class="sxs-lookup"><span data-stu-id="39497-165">[SectionGroup](sectiongroup.md) collection</span></span>|<span data-ttu-id="39497-p113">Grupos de secciones de la sección. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="39497-p113">The section groups in the section. Read-only. Nullable.</span></span>|
|<span data-ttu-id="39497-169">sections</span><span class="sxs-lookup"><span data-stu-id="39497-169">sections</span></span>|<span data-ttu-id="39497-170">Colección de [OnenoteSection](section.md)</span><span class="sxs-lookup"><span data-stu-id="39497-170">[OnenoteSection](section.md) collection</span></span>|<span data-ttu-id="39497-p114">Secciones del grupo de secciones. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="39497-p114">The sections in the section group. Read-only. Nullable.</span></span>|

## <a name="methods"></a><span data-ttu-id="39497-174">Métodos</span><span class="sxs-lookup"><span data-stu-id="39497-174">Methods</span></span>

| <span data-ttu-id="39497-175">Método</span><span class="sxs-lookup"><span data-stu-id="39497-175">Method</span></span>           | <span data-ttu-id="39497-176">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39497-176">Return Type</span></span>    |<span data-ttu-id="39497-177">Descripción</span><span class="sxs-lookup"><span data-stu-id="39497-177">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="39497-178">Obtener grupo de secciones</span><span class="sxs-lookup"><span data-stu-id="39497-178">Get section group</span></span>](../api/sectiongroup-get.md) | [<span data-ttu-id="39497-179">SectionGroup</span><span class="sxs-lookup"><span data-stu-id="39497-179">SectionGroup</span></span>](sectiongroup.md) |<span data-ttu-id="39497-180">Leer las propiedades y las relaciones del grupo de secciones.</span><span class="sxs-lookup"><span data-stu-id="39497-180">Read the properties and relationships of the section group.</span></span>|
|[<span data-ttu-id="39497-181">Crear grupo de secciones</span><span class="sxs-lookup"><span data-stu-id="39497-181">Create section group</span></span>](../api/sectiongroup-post-sectiongroups.md) |[<span data-ttu-id="39497-182">SectionGroup</span><span class="sxs-lookup"><span data-stu-id="39497-182">SectionGroup</span></span>](sectiongroup.md)| <span data-ttu-id="39497-183">Crear un grupo de secciones publicándolo en el grupo de secciones especificado de la colección sectionGroups.</span><span class="sxs-lookup"><span data-stu-id="39497-183">Create a section group by posting to the sectionGroups collection in the specified section group.</span></span>|
|[<span data-ttu-id="39497-184">Enumerar grupos de secciones</span><span class="sxs-lookup"><span data-stu-id="39497-184">List section groups</span></span>](../api/sectiongroup-list-sectiongroups.md) |<span data-ttu-id="39497-185">Colección [SectionGroup](sectiongroup.md)</span><span class="sxs-lookup"><span data-stu-id="39497-185">[SectionGroup](sectiongroup.md) collection</span></span>| <span data-ttu-id="39497-186">Obtener una colección de grupos de secciones en el grupo de secciones especificado.</span><span class="sxs-lookup"><span data-stu-id="39497-186">Get collection of section groups in the specified section group.</span></span>|
|[<span data-ttu-id="39497-187">Crear sección</span><span class="sxs-lookup"><span data-stu-id="39497-187">Create section</span></span>](../api/sectiongroup-post-sections.md) |[<span data-ttu-id="39497-188">OnenoteSection</span><span class="sxs-lookup"><span data-stu-id="39497-188">OnenoteSection</span></span>](section.md)| <span data-ttu-id="39497-189">Crear una sección publicándola en el grupo de secciones especificado de la colección de secciones.</span><span class="sxs-lookup"><span data-stu-id="39497-189">Create a section by posting to the sections collection in the specified section group.</span></span>|
|[<span data-ttu-id="39497-190">Enumerar secciones</span><span class="sxs-lookup"><span data-stu-id="39497-190">List sections</span></span>](../api/sectiongroup-list-sections.md) |<span data-ttu-id="39497-191">Colección de [OnenoteSection](section.md)</span><span class="sxs-lookup"><span data-stu-id="39497-191">[OnenoteSection](section.md) collection</span></span>| <span data-ttu-id="39497-192">Obtener una colección de secciones en el grupo de secciones especificado.</span><span class="sxs-lookup"><span data-stu-id="39497-192">Get a collection of sections in the specified section group.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "sectionGroup resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
