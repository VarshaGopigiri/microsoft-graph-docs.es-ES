---
title: Tipo de recurso sectionGroup
description: Un grupo de secciones en un bloc de notas de OneNote. Los grupos de secciones pueden contener secciones y grupos de secciones.
localization_priority: Normal
ms.openlocfilehash: 9e955d91fa49642100694da66421665a0d67b3da
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27855429"
---
# <a name="sectiongroup-resource-type"></a><span data-ttu-id="86c89-104">Tipo de recurso sectionGroup</span><span class="sxs-lookup"><span data-stu-id="86c89-104">sectionGroup resource type</span></span>

> <span data-ttu-id="86c89-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="86c89-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="86c89-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="86c89-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="86c89-p103">Un grupo de secciones en un bloc de notas de OneNote. Los grupos de secciones pueden contener secciones y grupos de secciones.</span><span class="sxs-lookup"><span data-stu-id="86c89-p103">A section group in a OneNote notebook. Section groups can contain sections and section groups.</span></span>

## <a name="json-representation"></a><span data-ttu-id="86c89-109">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="86c89-109">JSON representation</span></span>

<span data-ttu-id="86c89-110">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="86c89-110">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "parentNotebook",
    "parentSectionGroup",
    "sectionGroups",
    "sections"
  ],
  "@odata.type": "microsoft.graph.sectiongroup"
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
## <a name="properties"></a><span data-ttu-id="86c89-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="86c89-111">Properties</span></span>
| <span data-ttu-id="86c89-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="86c89-112">Property</span></span>     | <span data-ttu-id="86c89-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="86c89-113">Type</span></span>   |<span data-ttu-id="86c89-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="86c89-114">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="86c89-115">createdBy</span><span class="sxs-lookup"><span data-stu-id="86c89-115">createdBy</span></span>|[<span data-ttu-id="86c89-116">identitySet</span><span class="sxs-lookup"><span data-stu-id="86c89-116">identitySet</span></span>](identityset.md)|<span data-ttu-id="86c89-p104">Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="86c89-p104">Identity of the user, device, and application which created the item. Read-only.</span></span>|
|<span data-ttu-id="86c89-119">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="86c89-119">createdDateTime</span></span>|<span data-ttu-id="86c89-120">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="86c89-120">DateTimeOffset</span></span>|<span data-ttu-id="86c89-p105">La fecha y la hora en que se creó el grupo de secciones. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="86c89-p105">The date and time when the section group was created. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|
|<span data-ttu-id="86c89-125">id</span><span class="sxs-lookup"><span data-stu-id="86c89-125">id</span></span>|<span data-ttu-id="86c89-126">Cadena</span><span class="sxs-lookup"><span data-stu-id="86c89-126">String</span></span>|<span data-ttu-id="86c89-p106">El identificador único del grupo de secciones. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="86c89-p106">The unique identifier of the section group. Read-only.</span></span>|
|<span data-ttu-id="86c89-129">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="86c89-129">lastModifiedBy</span></span>|[<span data-ttu-id="86c89-130">identitySet</span><span class="sxs-lookup"><span data-stu-id="86c89-130">identitySet</span></span>](identityset.md)|<span data-ttu-id="86c89-p107">Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="86c89-p107">Identity of the user, device, and application which created the item. Read-only.</span></span>|
|<span data-ttu-id="86c89-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="86c89-133">lastModifiedDateTime</span></span>|<span data-ttu-id="86c89-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="86c89-134">DateTimeOffset</span></span>|<span data-ttu-id="86c89-p108">La fecha y la hora en que se modificó por última vez el grupo de secciones. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="86c89-p108">The date and time when the section group was last modified. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|
|<span data-ttu-id="86c89-139">displayName</span><span class="sxs-lookup"><span data-stu-id="86c89-139">displayName</span></span>|<span data-ttu-id="86c89-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="86c89-140">String</span></span>|<span data-ttu-id="86c89-141">El nombre del grupo de secciones.</span><span class="sxs-lookup"><span data-stu-id="86c89-141">The name of the section group.</span></span>|
|<span data-ttu-id="86c89-142">sectionGroupsUrl</span><span class="sxs-lookup"><span data-stu-id="86c89-142">sectionGroupsUrl</span></span>|<span data-ttu-id="86c89-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="86c89-143">String</span></span>|<span data-ttu-id="86c89-p109">La dirección URL de la propiedad de navegación `sectionGroups`, que devuelve todos los grupos de secciones del grupo de secciones. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="86c89-p109">The URL for the `sectionGroups` navigation property, which returns all the section groups in the section group. Read-only.</span></span>|
|<span data-ttu-id="86c89-146">sectionsUrl</span><span class="sxs-lookup"><span data-stu-id="86c89-146">sectionsUrl</span></span>|<span data-ttu-id="86c89-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="86c89-147">String</span></span>|<span data-ttu-id="86c89-p110">La dirección URL de la propiedad de navegación `sections`, que devuelve todas las secciones del grupo de secciones. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="86c89-p110">The URL for the `sections` navigation property, which returns all the sections in the section group. Read-only.</span></span>|
|<span data-ttu-id="86c89-150">self</span><span class="sxs-lookup"><span data-stu-id="86c89-150">self</span></span>|<span data-ttu-id="86c89-151">Cadena</span><span class="sxs-lookup"><span data-stu-id="86c89-151">String</span></span>|<span data-ttu-id="86c89-p111">El punto de conexión donde puede obtener información detallada sobre el grupo de secciones. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="86c89-p111">The endpoint where you can get details about the section group. Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="86c89-154">Relaciones</span><span class="sxs-lookup"><span data-stu-id="86c89-154">Relationships</span></span>
| <span data-ttu-id="86c89-155">Relación</span><span class="sxs-lookup"><span data-stu-id="86c89-155">Relationship</span></span> | <span data-ttu-id="86c89-156">Tipo</span><span class="sxs-lookup"><span data-stu-id="86c89-156">Type</span></span>   |<span data-ttu-id="86c89-157">Descripción</span><span class="sxs-lookup"><span data-stu-id="86c89-157">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="86c89-158">parentNotebook</span><span class="sxs-lookup"><span data-stu-id="86c89-158">parentNotebook</span></span>|[<span data-ttu-id="86c89-159">Notebook</span><span class="sxs-lookup"><span data-stu-id="86c89-159">Notebook</span></span>](notebook.md)|<span data-ttu-id="86c89-p112">Bloc de notas que contiene el grupo de secciones. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="86c89-p112">The notebook that contains the section group. Read-only.</span></span>|
|<span data-ttu-id="86c89-162">parentSectionGroup</span><span class="sxs-lookup"><span data-stu-id="86c89-162">parentSectionGroup</span></span>|[<span data-ttu-id="86c89-163">SectionGroup</span><span class="sxs-lookup"><span data-stu-id="86c89-163">SectionGroup</span></span>](sectiongroup.md)|<span data-ttu-id="86c89-p113">Grupo de secciones que contiene el grupo de secciones. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="86c89-p113">The section group that contains the section group. Read-only.</span></span>|
|<span data-ttu-id="86c89-166">sectionGroups</span><span class="sxs-lookup"><span data-stu-id="86c89-166">sectionGroups</span></span>|<span data-ttu-id="86c89-167">Colección [SectionGroup](sectiongroup.md)</span><span class="sxs-lookup"><span data-stu-id="86c89-167">[SectionGroup](sectiongroup.md) collection</span></span>|<span data-ttu-id="86c89-p114">Grupos de secciones de la sección. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="86c89-p114">The section groups in the section. Read-only. Nullable.</span></span>|
|<span data-ttu-id="86c89-171">sections</span><span class="sxs-lookup"><span data-stu-id="86c89-171">sections</span></span>|<span data-ttu-id="86c89-172">Colección [Section](section.md)</span><span class="sxs-lookup"><span data-stu-id="86c89-172">[Section](section.md) collection</span></span>|<span data-ttu-id="86c89-p115">Secciones del grupo de secciones. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="86c89-p115">The sections in the section group. Read-only. Nullable.</span></span>|

## <a name="methods"></a><span data-ttu-id="86c89-176">Métodos</span><span class="sxs-lookup"><span data-stu-id="86c89-176">Methods</span></span>

| <span data-ttu-id="86c89-177">Método</span><span class="sxs-lookup"><span data-stu-id="86c89-177">Method</span></span>           | <span data-ttu-id="86c89-178">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="86c89-178">Return Type</span></span>    |<span data-ttu-id="86c89-179">Descripción</span><span class="sxs-lookup"><span data-stu-id="86c89-179">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="86c89-180">Obtener grupo de secciones</span><span class="sxs-lookup"><span data-stu-id="86c89-180">Get section group</span></span>](../api/sectiongroup-get.md) | [<span data-ttu-id="86c89-181">SectionGroup</span><span class="sxs-lookup"><span data-stu-id="86c89-181">SectionGroup</span></span>](sectiongroup.md) |<span data-ttu-id="86c89-182">Leer las propiedades y las relaciones del grupo de secciones.</span><span class="sxs-lookup"><span data-stu-id="86c89-182">Read the properties and relationships of the section group.</span></span>|
|[<span data-ttu-id="86c89-183">Crear grupo de secciones</span><span class="sxs-lookup"><span data-stu-id="86c89-183">Create section group</span></span>](../api/sectiongroup-post-sectiongroups.md) |[<span data-ttu-id="86c89-184">SectionGroup</span><span class="sxs-lookup"><span data-stu-id="86c89-184">SectionGroup</span></span>](sectiongroup.md)| <span data-ttu-id="86c89-185">Crear un grupo de secciones publicándolo en el grupo de secciones especificado de la colección sectionGroups.</span><span class="sxs-lookup"><span data-stu-id="86c89-185">Create a section group by posting to the sectionGroups collection in the specified section group.</span></span>|
|[<span data-ttu-id="86c89-186">Enumerar grupos de secciones</span><span class="sxs-lookup"><span data-stu-id="86c89-186">List section groups</span></span>](../api/sectiongroup-list-sectiongroups.md) |<span data-ttu-id="86c89-187">Colección [SectionGroup](sectiongroup.md)</span><span class="sxs-lookup"><span data-stu-id="86c89-187">[SectionGroup](sectiongroup.md) collection</span></span>| <span data-ttu-id="86c89-188">Obtener una colección de grupos de secciones en el grupo de secciones especificado.</span><span class="sxs-lookup"><span data-stu-id="86c89-188">Get collection of section groups in the specified section group.</span></span>|
|[<span data-ttu-id="86c89-189">Crear sección</span><span class="sxs-lookup"><span data-stu-id="86c89-189">Create section</span></span>](../api/sectiongroup-post-sections.md) |[<span data-ttu-id="86c89-190">Section</span><span class="sxs-lookup"><span data-stu-id="86c89-190">Section</span></span>](section.md)| <span data-ttu-id="86c89-191">Crear una sección publicándola en el grupo de secciones especificado de la colección de secciones.</span><span class="sxs-lookup"><span data-stu-id="86c89-191">Create a section by posting to the sections collection in the specified section group.</span></span>|
|[<span data-ttu-id="86c89-192">Enumerar secciones</span><span class="sxs-lookup"><span data-stu-id="86c89-192">List sections</span></span>](../api/sectiongroup-list-sections.md) |<span data-ttu-id="86c89-193">Colección [Section](section.md)</span><span class="sxs-lookup"><span data-stu-id="86c89-193">[Section](section.md) collection</span></span>| <span data-ttu-id="86c89-194">Obtener una colección de secciones en el grupo de secciones especificado.</span><span class="sxs-lookup"><span data-stu-id="86c89-194">Get a collection of sections in the specified section group.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "sectionGroup resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
