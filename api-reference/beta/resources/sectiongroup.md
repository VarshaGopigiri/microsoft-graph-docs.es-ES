---
title: Tipo de recurso sectionGroup
description: Un grupo de secciones en un bloc de notas de OneNote. Los grupos de secciones pueden contener secciones y grupos de secciones.
localization_priority: Normal
author: jewan-microsoft
ms.prod: onenote
ms.openlocfilehash: 8ecd8633b3311459368a16477be391778087882c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27976761"
---
# <a name="sectiongroup-resource-type"></a><span data-ttu-id="b825d-104">Tipo de recurso sectionGroup</span><span class="sxs-lookup"><span data-stu-id="b825d-104">sectionGroup resource type</span></span>

> <span data-ttu-id="b825d-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b825d-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b825d-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b825d-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b825d-p103">Un grupo de secciones en un bloc de notas de OneNote. Los grupos de secciones pueden contener secciones y grupos de secciones.</span><span class="sxs-lookup"><span data-stu-id="b825d-p103">A section group in a OneNote notebook. Section groups can contain sections and section groups.</span></span>

## <a name="json-representation"></a><span data-ttu-id="b825d-109">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b825d-109">JSON representation</span></span>

<span data-ttu-id="b825d-110">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b825d-110">Here is a JSON representation of the resource.</span></span>

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
## <a name="properties"></a><span data-ttu-id="b825d-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b825d-111">Properties</span></span>
| <span data-ttu-id="b825d-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b825d-112">Property</span></span>     | <span data-ttu-id="b825d-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="b825d-113">Type</span></span>   |<span data-ttu-id="b825d-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="b825d-114">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b825d-115">createdBy</span><span class="sxs-lookup"><span data-stu-id="b825d-115">createdBy</span></span>|[<span data-ttu-id="b825d-116">identitySet</span><span class="sxs-lookup"><span data-stu-id="b825d-116">identitySet</span></span>](identityset.md)|<span data-ttu-id="b825d-p104">Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b825d-p104">Identity of the user, device, and application which created the item. Read-only.</span></span>|
|<span data-ttu-id="b825d-119">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="b825d-119">createdDateTime</span></span>|<span data-ttu-id="b825d-120">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b825d-120">DateTimeOffset</span></span>|<span data-ttu-id="b825d-p105">La fecha y la hora en que se creó el grupo de secciones. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b825d-p105">The date and time when the section group was created. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|
|<span data-ttu-id="b825d-125">id</span><span class="sxs-lookup"><span data-stu-id="b825d-125">id</span></span>|<span data-ttu-id="b825d-126">Cadena</span><span class="sxs-lookup"><span data-stu-id="b825d-126">String</span></span>|<span data-ttu-id="b825d-p106">El identificador único del grupo de secciones. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b825d-p106">The unique identifier of the section group. Read-only.</span></span>|
|<span data-ttu-id="b825d-129">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="b825d-129">lastModifiedBy</span></span>|[<span data-ttu-id="b825d-130">identitySet</span><span class="sxs-lookup"><span data-stu-id="b825d-130">identitySet</span></span>](identityset.md)|<span data-ttu-id="b825d-p107">Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b825d-p107">Identity of the user, device, and application which created the item. Read-only.</span></span>|
|<span data-ttu-id="b825d-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="b825d-133">lastModifiedDateTime</span></span>|<span data-ttu-id="b825d-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b825d-134">DateTimeOffset</span></span>|<span data-ttu-id="b825d-p108">La fecha y la hora en que se modificó por última vez el grupo de secciones. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b825d-p108">The date and time when the section group was last modified. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|
|<span data-ttu-id="b825d-139">displayName</span><span class="sxs-lookup"><span data-stu-id="b825d-139">displayName</span></span>|<span data-ttu-id="b825d-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="b825d-140">String</span></span>|<span data-ttu-id="b825d-141">El nombre del grupo de secciones.</span><span class="sxs-lookup"><span data-stu-id="b825d-141">The name of the section group.</span></span>|
|<span data-ttu-id="b825d-142">sectionGroupsUrl</span><span class="sxs-lookup"><span data-stu-id="b825d-142">sectionGroupsUrl</span></span>|<span data-ttu-id="b825d-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="b825d-143">String</span></span>|<span data-ttu-id="b825d-p109">La dirección URL de la propiedad de navegación `sectionGroups`, que devuelve todos los grupos de secciones del grupo de secciones. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b825d-p109">The URL for the `sectionGroups` navigation property, which returns all the section groups in the section group. Read-only.</span></span>|
|<span data-ttu-id="b825d-146">sectionsUrl</span><span class="sxs-lookup"><span data-stu-id="b825d-146">sectionsUrl</span></span>|<span data-ttu-id="b825d-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="b825d-147">String</span></span>|<span data-ttu-id="b825d-p110">La dirección URL de la propiedad de navegación `sections`, que devuelve todas las secciones del grupo de secciones. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b825d-p110">The URL for the `sections` navigation property, which returns all the sections in the section group. Read-only.</span></span>|
|<span data-ttu-id="b825d-150">self</span><span class="sxs-lookup"><span data-stu-id="b825d-150">self</span></span>|<span data-ttu-id="b825d-151">Cadena</span><span class="sxs-lookup"><span data-stu-id="b825d-151">String</span></span>|<span data-ttu-id="b825d-p111">El punto de conexión donde puede obtener información detallada sobre el grupo de secciones. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b825d-p111">The endpoint where you can get details about the section group. Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="b825d-154">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b825d-154">Relationships</span></span>
| <span data-ttu-id="b825d-155">Relación</span><span class="sxs-lookup"><span data-stu-id="b825d-155">Relationship</span></span> | <span data-ttu-id="b825d-156">Tipo</span><span class="sxs-lookup"><span data-stu-id="b825d-156">Type</span></span>   |<span data-ttu-id="b825d-157">Descripción</span><span class="sxs-lookup"><span data-stu-id="b825d-157">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b825d-158">parentNotebook</span><span class="sxs-lookup"><span data-stu-id="b825d-158">parentNotebook</span></span>|[<span data-ttu-id="b825d-159">Notebook</span><span class="sxs-lookup"><span data-stu-id="b825d-159">Notebook</span></span>](notebook.md)|<span data-ttu-id="b825d-p112">Bloc de notas que contiene el grupo de secciones. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b825d-p112">The notebook that contains the section group. Read-only.</span></span>|
|<span data-ttu-id="b825d-162">parentSectionGroup</span><span class="sxs-lookup"><span data-stu-id="b825d-162">parentSectionGroup</span></span>|[<span data-ttu-id="b825d-163">SectionGroup</span><span class="sxs-lookup"><span data-stu-id="b825d-163">SectionGroup</span></span>](sectiongroup.md)|<span data-ttu-id="b825d-p113">Grupo de secciones que contiene el grupo de secciones. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b825d-p113">The section group that contains the section group. Read-only.</span></span>|
|<span data-ttu-id="b825d-166">sectionGroups</span><span class="sxs-lookup"><span data-stu-id="b825d-166">sectionGroups</span></span>|<span data-ttu-id="b825d-167">Colección [SectionGroup](sectiongroup.md)</span><span class="sxs-lookup"><span data-stu-id="b825d-167">[SectionGroup](sectiongroup.md) collection</span></span>|<span data-ttu-id="b825d-p114">Grupos de secciones de la sección. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="b825d-p114">The section groups in the section. Read-only. Nullable.</span></span>|
|<span data-ttu-id="b825d-171">sections</span><span class="sxs-lookup"><span data-stu-id="b825d-171">sections</span></span>|<span data-ttu-id="b825d-172">Colección [Section](section.md)</span><span class="sxs-lookup"><span data-stu-id="b825d-172">[Section](section.md) collection</span></span>|<span data-ttu-id="b825d-p115">Secciones del grupo de secciones. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="b825d-p115">The sections in the section group. Read-only. Nullable.</span></span>|

## <a name="methods"></a><span data-ttu-id="b825d-176">Métodos</span><span class="sxs-lookup"><span data-stu-id="b825d-176">Methods</span></span>

| <span data-ttu-id="b825d-177">Método</span><span class="sxs-lookup"><span data-stu-id="b825d-177">Method</span></span>           | <span data-ttu-id="b825d-178">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b825d-178">Return Type</span></span>    |<span data-ttu-id="b825d-179">Descripción</span><span class="sxs-lookup"><span data-stu-id="b825d-179">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="b825d-180">Obtener grupo de secciones</span><span class="sxs-lookup"><span data-stu-id="b825d-180">Get section group</span></span>](../api/sectiongroup-get.md) | [<span data-ttu-id="b825d-181">SectionGroup</span><span class="sxs-lookup"><span data-stu-id="b825d-181">SectionGroup</span></span>](sectiongroup.md) |<span data-ttu-id="b825d-182">Leer las propiedades y las relaciones del grupo de secciones.</span><span class="sxs-lookup"><span data-stu-id="b825d-182">Read the properties and relationships of the section group.</span></span>|
|[<span data-ttu-id="b825d-183">Crear grupo de secciones</span><span class="sxs-lookup"><span data-stu-id="b825d-183">Create section group</span></span>](../api/sectiongroup-post-sectiongroups.md) |[<span data-ttu-id="b825d-184">SectionGroup</span><span class="sxs-lookup"><span data-stu-id="b825d-184">SectionGroup</span></span>](sectiongroup.md)| <span data-ttu-id="b825d-185">Crear un grupo de secciones publicándolo en el grupo de secciones especificado de la colección sectionGroups.</span><span class="sxs-lookup"><span data-stu-id="b825d-185">Create a section group by posting to the sectionGroups collection in the specified section group.</span></span>|
|[<span data-ttu-id="b825d-186">Enumerar grupos de secciones</span><span class="sxs-lookup"><span data-stu-id="b825d-186">List section groups</span></span>](../api/sectiongroup-list-sectiongroups.md) |<span data-ttu-id="b825d-187">Colección [SectionGroup](sectiongroup.md)</span><span class="sxs-lookup"><span data-stu-id="b825d-187">[SectionGroup](sectiongroup.md) collection</span></span>| <span data-ttu-id="b825d-188">Obtener una colección de grupos de secciones en el grupo de secciones especificado.</span><span class="sxs-lookup"><span data-stu-id="b825d-188">Get collection of section groups in the specified section group.</span></span>|
|[<span data-ttu-id="b825d-189">Crear sección</span><span class="sxs-lookup"><span data-stu-id="b825d-189">Create section</span></span>](../api/sectiongroup-post-sections.md) |[<span data-ttu-id="b825d-190">Section</span><span class="sxs-lookup"><span data-stu-id="b825d-190">Section</span></span>](section.md)| <span data-ttu-id="b825d-191">Crear una sección publicándola en el grupo de secciones especificado de la colección de secciones.</span><span class="sxs-lookup"><span data-stu-id="b825d-191">Create a section by posting to the sections collection in the specified section group.</span></span>|
|[<span data-ttu-id="b825d-192">Enumerar secciones</span><span class="sxs-lookup"><span data-stu-id="b825d-192">List sections</span></span>](../api/sectiongroup-list-sections.md) |<span data-ttu-id="b825d-193">Colección [Section](section.md)</span><span class="sxs-lookup"><span data-stu-id="b825d-193">[Section](section.md) collection</span></span>| <span data-ttu-id="b825d-194">Obtener una colección de secciones en el grupo de secciones especificado.</span><span class="sxs-lookup"><span data-stu-id="b825d-194">Get a collection of sections in the specified section group.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "sectionGroup resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
