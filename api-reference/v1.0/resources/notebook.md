---
title: Tipo de recurso notebook
description: Bloc de notas de OneNote.
author: Jewan-microsoft
ms.openlocfilehash: 2e435a208395e34e9c10474e3df15f1ad16f3996
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27335584"
---
# <a name="notebook-resource-type"></a><span data-ttu-id="9a180-103">Tipo de recurso notebook</span><span class="sxs-lookup"><span data-stu-id="9a180-103">notebook resource type</span></span>

<span data-ttu-id="9a180-104">Bloc de notas de OneNote.</span><span class="sxs-lookup"><span data-stu-id="9a180-104">A OneNote notebook.</span></span>

## <a name="json-representation"></a><span data-ttu-id="9a180-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9a180-105">JSON representation</span></span>

<span data-ttu-id="9a180-106">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="9a180-106">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.onenoteEntityHierarchyModel",
  "optionalProperties": [
    "sectionGroups",
    "sections"
  ],
  "@odata.type": "microsoft.graph.notebook"
}-->

```json
{
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "createdDateTime": "String (timestamp)",
  "id": "string (identifier)",
  "isDefault": true,
  "isShared": true,
  "lastModifiedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "lastModifiedDateTime": "String (timestamp)",
  "links": {"@odata.type": "microsoft.graph.notebookLinks"},
  "displayName": "string",
  "sectionGroupsUrl": "string",
  "sectionsUrl": "string",
  "self": "string",
  "userRole": "String"
}

```
## <a name="properties"></a><span data-ttu-id="9a180-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9a180-107">Properties</span></span>
| <span data-ttu-id="9a180-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9a180-108">Property</span></span>     | <span data-ttu-id="9a180-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="9a180-109">Type</span></span>   |<span data-ttu-id="9a180-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a180-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9a180-111">createdBy</span><span class="sxs-lookup"><span data-stu-id="9a180-111">createdBy</span></span>|[<span data-ttu-id="9a180-112">identitySet</span><span class="sxs-lookup"><span data-stu-id="9a180-112">identitySet</span></span>](identityset.md)|<span data-ttu-id="9a180-p101">Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9a180-p101">Identity of the user, device, and application which created the item. Read-only.</span></span>|
|<span data-ttu-id="9a180-115">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="9a180-115">createdDateTime</span></span>|<span data-ttu-id="9a180-116">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9a180-116">DateTimeOffset</span></span>|<span data-ttu-id="9a180-p102">La fecha y la hora en que se creó el bloc de notas. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9a180-p102">The date and time when the notebook was created. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|
|<span data-ttu-id="9a180-121">id</span><span class="sxs-lookup"><span data-stu-id="9a180-121">id</span></span>|<span data-ttu-id="9a180-122">String</span><span class="sxs-lookup"><span data-stu-id="9a180-122">String</span></span>|<span data-ttu-id="9a180-p103">El identificador único del bloc de notas. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9a180-p103">The unique identifier of the notebook. Read-only.</span></span>|
|<span data-ttu-id="9a180-125">isDefault</span><span class="sxs-lookup"><span data-stu-id="9a180-125">isDefault</span></span>|<span data-ttu-id="9a180-126">Booleano</span><span class="sxs-lookup"><span data-stu-id="9a180-126">Boolean</span></span>|<span data-ttu-id="9a180-p104">Indica si se trata del bloc de notas predeterminado del usuario. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9a180-p104">Indicates whether this is the user's default notebook. Read-only.</span></span>|
|<span data-ttu-id="9a180-129">isShared</span><span class="sxs-lookup"><span data-stu-id="9a180-129">isShared</span></span>|<span data-ttu-id="9a180-130">Booleano</span><span class="sxs-lookup"><span data-stu-id="9a180-130">Boolean</span></span>|<span data-ttu-id="9a180-p105">Indica si se comparte el bloc de notas. Si es true, además del propietario, otros usuarios pueden ver el contenido del bloc de notas. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9a180-p105">Indicates whether the notebook is shared. If true, the contents of the notebook can be seen by people other than the owner. Read-only.</span></span>|
|<span data-ttu-id="9a180-134">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="9a180-134">lastModifiedBy</span></span>|[<span data-ttu-id="9a180-135">identitySet</span><span class="sxs-lookup"><span data-stu-id="9a180-135">identitySet</span></span>](identityset.md)|<span data-ttu-id="9a180-p106">Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9a180-p106">Identity of the user, device, and application which created the item. Read-only.</span></span>|
|<span data-ttu-id="9a180-138">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="9a180-138">lastModifiedDateTime</span></span>|<span data-ttu-id="9a180-139">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9a180-139">DateTimeOffset</span></span>|<span data-ttu-id="9a180-p107">La fecha y la hora en que se modificó por última vez el bloc de notas. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9a180-p107">The date and time when the notebook was last modified. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|
|<span data-ttu-id="9a180-144">links</span><span class="sxs-lookup"><span data-stu-id="9a180-144">links</span></span>|[<span data-ttu-id="9a180-145">NotebookLinks</span><span class="sxs-lookup"><span data-stu-id="9a180-145">NotebookLinks</span></span>](notebooklinks.md)|<span data-ttu-id="9a180-p108">Vínculos para abrir el bloc de notas. El vínculo `oneNoteClientURL` abre el bloc de notas en el cliente nativo de OneNote si está instalado. El vínculo `oneNoteWebURL` abre el bloc de notas en OneNote Online.</span><span class="sxs-lookup"><span data-stu-id="9a180-p108">Links for opening the notebook. The `oneNoteClientURL` link opens the notebook in the OneNote native client if it's installed. The `oneNoteWebURL` link opens the notebook in OneNote Online.</span></span>|
|<span data-ttu-id="9a180-149">displayName</span><span class="sxs-lookup"><span data-stu-id="9a180-149">displayName</span></span>|<span data-ttu-id="9a180-150">String</span><span class="sxs-lookup"><span data-stu-id="9a180-150">String</span></span>|<span data-ttu-id="9a180-151">El nombre del bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="9a180-151">The name of the notebook.</span></span>|
|<span data-ttu-id="9a180-152">sectionGroupsUrl</span><span class="sxs-lookup"><span data-stu-id="9a180-152">sectionGroupsUrl</span></span>|<span data-ttu-id="9a180-153">String</span><span class="sxs-lookup"><span data-stu-id="9a180-153">String</span></span>|<span data-ttu-id="9a180-p109">La dirección URL de la propiedad de navegación `sectionGroups`, que devuelve todos los grupos de secciones del bloc de notas. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9a180-p109">The URL for the `sectionGroups` navigation property, which returns all the section groups in the notebook. Read-only.</span></span>|
|<span data-ttu-id="9a180-156">sectionsUrl</span><span class="sxs-lookup"><span data-stu-id="9a180-156">sectionsUrl</span></span>|<span data-ttu-id="9a180-157">String</span><span class="sxs-lookup"><span data-stu-id="9a180-157">String</span></span>|<span data-ttu-id="9a180-p110">La dirección URL de la propiedad de navegación `sections`, que devuelve todas las secciones del bloc de notas. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9a180-p110">The URL for the `sections` navigation property, which returns all the sections in the notebook. Read-only.</span></span>|
|<span data-ttu-id="9a180-160">self</span><span class="sxs-lookup"><span data-stu-id="9a180-160">self</span></span>|<span data-ttu-id="9a180-161">String</span><span class="sxs-lookup"><span data-stu-id="9a180-161">String</span></span>|<span data-ttu-id="9a180-p111">El punto de conexión donde puede obtener información detallada sobre el bloc de notas. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9a180-p111">The endpoint where you can get details about the notebook. Read-only.</span></span>|
|<span data-ttu-id="9a180-164">userRole</span><span class="sxs-lookup"><span data-stu-id="9a180-164">userRole</span></span>|<span data-ttu-id="9a180-165">onenoteUserRole</span><span class="sxs-lookup"><span data-stu-id="9a180-165">onenoteUserRole</span></span>|<span data-ttu-id="9a180-p112">Los valores posibles son `Owner`, `Contributor`, `Reader` y `None`. Owner representa el acceso de nivel de propietario al bloc de notas. Contributor representa el acceso de lectura/escritura al bloc de notas. Reader representa el acceso de solo lectura al bloc de notas. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9a180-p112">Possible values are: `Owner`, `Contributor`, `Reader`, `None`. Owner represents owner-level access to the notebook. Contributor represents read/write access to the notebook. Reader represents read-only access to the notebook. Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="9a180-171">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9a180-171">Relationships</span></span>
| <span data-ttu-id="9a180-172">Relación</span><span class="sxs-lookup"><span data-stu-id="9a180-172">Relationship</span></span> | <span data-ttu-id="9a180-173">Tipo</span><span class="sxs-lookup"><span data-stu-id="9a180-173">Type</span></span>   |<span data-ttu-id="9a180-174">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a180-174">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9a180-175">sectionGroups</span><span class="sxs-lookup"><span data-stu-id="9a180-175">sectionGroups</span></span>|<span data-ttu-id="9a180-176">Colección [SectionGroup](sectiongroup.md)</span><span class="sxs-lookup"><span data-stu-id="9a180-176">[SectionGroup](sectiongroup.md) collection</span></span>|<span data-ttu-id="9a180-p113">Los grupos de secciones del bloc de notas. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="9a180-p113">The section groups in the notebook. Read-only. Nullable.</span></span>|
|<span data-ttu-id="9a180-180">sections</span><span class="sxs-lookup"><span data-stu-id="9a180-180">sections</span></span>|<span data-ttu-id="9a180-181">Colección de [OnenoteSection](section.md)</span><span class="sxs-lookup"><span data-stu-id="9a180-181">[OnenoteSection](section.md) collection</span></span>|<span data-ttu-id="9a180-p114">Secciones del bloc de notas. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="9a180-p114">The sections in the notebook. Read-only. Nullable.</span></span>|

## <a name="methods"></a><span data-ttu-id="9a180-185">Métodos</span><span class="sxs-lookup"><span data-stu-id="9a180-185">Methods</span></span>

| <span data-ttu-id="9a180-186">Método</span><span class="sxs-lookup"><span data-stu-id="9a180-186">Method</span></span>           | <span data-ttu-id="9a180-187">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a180-187">Return Type</span></span>    |<span data-ttu-id="9a180-188">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a180-188">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="9a180-189">Obtener bloc de notas</span><span class="sxs-lookup"><span data-stu-id="9a180-189">Get notebook</span></span>](../api/notebook-get.md) | [<span data-ttu-id="9a180-190">Notebook</span><span class="sxs-lookup"><span data-stu-id="9a180-190">Notebook</span></span>](notebook.md) |<span data-ttu-id="9a180-191">Leer las propiedades y las relaciones del bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="9a180-191">Read the properties and relationships of the notebook.</span></span>|
|[<span data-ttu-id="9a180-192">getRecentNotebooks</span><span class="sxs-lookup"><span data-stu-id="9a180-192">getRecentNotebooks</span></span>](../api/notebook-getrecentnotebooks.md) | <span data-ttu-id="9a180-193">Colección [recentNotebook](recentnotebook.md)</span><span class="sxs-lookup"><span data-stu-id="9a180-193">[recentNotebook](recentnotebook.md) collection</span></span> | <span data-ttu-id="9a180-194">Obtener una colección de los blocs de notas a los que ha tenido acceso más recientemente el usuario.</span><span class="sxs-lookup"><span data-stu-id="9a180-194">Get a collection of the most recently accessed notebooks for the user.</span></span> |
|[<span data-ttu-id="9a180-195">Crear grupo de secciones</span><span class="sxs-lookup"><span data-stu-id="9a180-195">Create section group</span></span>](../api/notebook-post-sectiongroups.md) |[<span data-ttu-id="9a180-196">SectionGroup</span><span class="sxs-lookup"><span data-stu-id="9a180-196">SectionGroup</span></span>](sectiongroup.md)| <span data-ttu-id="9a180-197">Crear un grupo de secciones publicándolo en el bloc de notas especificado de la colección sectionGroups.</span><span class="sxs-lookup"><span data-stu-id="9a180-197">Create a section group by posting to the sectionGroups collection in the specified notebook.</span></span>|
|[<span data-ttu-id="9a180-198">Enumerar grupos de secciones</span><span class="sxs-lookup"><span data-stu-id="9a180-198">List section groups</span></span>](../api/notebook-list-sectiongroups.md) |<span data-ttu-id="9a180-199">Colección [SectionGroup](sectiongroup.md)</span><span class="sxs-lookup"><span data-stu-id="9a180-199">[SectionGroup](sectiongroup.md) collection</span></span>| <span data-ttu-id="9a180-200">Obtener una colección de grupos de secciones en el bloc de notas especificado.</span><span class="sxs-lookup"><span data-stu-id="9a180-200">Get a collection of section groups in the specified notebook.</span></span>|
|[<span data-ttu-id="9a180-201">Crear sección</span><span class="sxs-lookup"><span data-stu-id="9a180-201">Create section</span></span>](../api/notebook-post-sections.md) |[<span data-ttu-id="9a180-202">OnenoteSection</span><span class="sxs-lookup"><span data-stu-id="9a180-202">OnenoteSection</span></span>](section.md)| <span data-ttu-id="9a180-203">Crear una sección publicándola en el bloc de notas especificado de la colección de secciones.</span><span class="sxs-lookup"><span data-stu-id="9a180-203">Create a section by posting to the sections collection in the specified notebook.</span></span>|
|[<span data-ttu-id="9a180-204">Enumerar secciones</span><span class="sxs-lookup"><span data-stu-id="9a180-204">List sections</span></span>](../api/notebook-list-sections.md) |<span data-ttu-id="9a180-205">Colección de [OnenoteSection](section.md)</span><span class="sxs-lookup"><span data-stu-id="9a180-205">[OnenoteSection](section.md) collection</span></span>| <span data-ttu-id="9a180-206">Obtener una colección de secciones en el bloc de notas especificado.</span><span class="sxs-lookup"><span data-stu-id="9a180-206">Get a collection of sections in the specified notebook.</span></span>|
|[<span data-ttu-id="9a180-207">copyNotebook</span><span class="sxs-lookup"><span data-stu-id="9a180-207">copyNotebook</span></span>](../api/notebook-copynotebook.md)| <span data-ttu-id="9a180-208">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9a180-208">None</span></span> | <span data-ttu-id="9a180-209">Copia un bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="9a180-209">Copies a notebook.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "notebook resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
