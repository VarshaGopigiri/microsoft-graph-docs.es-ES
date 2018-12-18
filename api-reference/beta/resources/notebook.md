---
title: Tipo de recurso notebook
description: Bloc de notas de OneNote.
author: Jewan-microsoft
ms.openlocfilehash: b6301e53d1cc616897055df0185601400f87de54
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27362219"
---
# <a name="notebook-resource-type"></a><span data-ttu-id="bb214-103">Tipo de recurso notebook</span><span class="sxs-lookup"><span data-stu-id="bb214-103">notebook resource type</span></span>

> <span data-ttu-id="bb214-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bb214-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bb214-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bb214-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="bb214-106">Bloc de notas de OneNote.</span><span class="sxs-lookup"><span data-stu-id="bb214-106">A OneNote notebook.</span></span>

## <a name="json-representation"></a><span data-ttu-id="bb214-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="bb214-107">JSON representation</span></span>

<span data-ttu-id="bb214-108">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="bb214-108">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
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
## <a name="properties"></a><span data-ttu-id="bb214-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bb214-109">Properties</span></span>
| <span data-ttu-id="bb214-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bb214-110">Property</span></span>     | <span data-ttu-id="bb214-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="bb214-111">Type</span></span>   |<span data-ttu-id="bb214-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb214-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bb214-113">createdBy</span><span class="sxs-lookup"><span data-stu-id="bb214-113">createdBy</span></span>|[<span data-ttu-id="bb214-114">identitySet</span><span class="sxs-lookup"><span data-stu-id="bb214-114">identitySet</span></span>](identityset.md)|<span data-ttu-id="bb214-p102">Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bb214-p102">Identity of the user, device, and application which created the item. Read-only.</span></span>|
|<span data-ttu-id="bb214-117">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="bb214-117">createdDateTime</span></span>|<span data-ttu-id="bb214-118">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bb214-118">DateTimeOffset</span></span>|<span data-ttu-id="bb214-p103">La fecha y la hora en que se creó el bloc de notas. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bb214-p103">The date and time when the notebook was created. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|
|<span data-ttu-id="bb214-123">id</span><span class="sxs-lookup"><span data-stu-id="bb214-123">id</span></span>|<span data-ttu-id="bb214-124">String</span><span class="sxs-lookup"><span data-stu-id="bb214-124">String</span></span>|<span data-ttu-id="bb214-p104">El identificador único del bloc de notas. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bb214-p104">The unique identifier of the notebook. Read-only.</span></span>|
|<span data-ttu-id="bb214-127">isDefault</span><span class="sxs-lookup"><span data-stu-id="bb214-127">isDefault</span></span>|<span data-ttu-id="bb214-128">Booleano</span><span class="sxs-lookup"><span data-stu-id="bb214-128">Boolean</span></span>|<span data-ttu-id="bb214-p105">Indica si se trata del bloc de notas predeterminado del usuario. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bb214-p105">Indicates whether this is the user's default notebook. Read-only.</span></span>|
|<span data-ttu-id="bb214-131">isShared</span><span class="sxs-lookup"><span data-stu-id="bb214-131">isShared</span></span>|<span data-ttu-id="bb214-132">Booleano</span><span class="sxs-lookup"><span data-stu-id="bb214-132">Boolean</span></span>|<span data-ttu-id="bb214-p106">Indica si se comparte el bloc de notas. Si es true, además del propietario, otros usuarios pueden ver el contenido del bloc de notas. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bb214-p106">Indicates whether the notebook is shared. If true, the contents of the notebook can be seen by people other than the owner. Read-only.</span></span>|
|<span data-ttu-id="bb214-136">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="bb214-136">lastModifiedBy</span></span>|[<span data-ttu-id="bb214-137">identitySet</span><span class="sxs-lookup"><span data-stu-id="bb214-137">identitySet</span></span>](identityset.md)|<span data-ttu-id="bb214-p107">Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bb214-p107">Identity of the user, device, and application which created the item. Read-only.</span></span>|
|<span data-ttu-id="bb214-140">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="bb214-140">lastModifiedDateTime</span></span>|<span data-ttu-id="bb214-141">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bb214-141">DateTimeOffset</span></span>|<span data-ttu-id="bb214-p108">La fecha y la hora en que se modificó por última vez el bloc de notas. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bb214-p108">The date and time when the notebook was last modified. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|
|<span data-ttu-id="bb214-146">links</span><span class="sxs-lookup"><span data-stu-id="bb214-146">links</span></span>|[<span data-ttu-id="bb214-147">NotebookLinks</span><span class="sxs-lookup"><span data-stu-id="bb214-147">NotebookLinks</span></span>](notebooklinks.md)|<span data-ttu-id="bb214-p109">Vínculos para abrir el bloc de notas. El vínculo `oneNoteClientURL` abre el bloc de notas en el cliente nativo de OneNote si está instalado. El vínculo `oneNoteWebURL` abre el bloc de notas en OneNote Online.</span><span class="sxs-lookup"><span data-stu-id="bb214-p109">Links for opening the notebook. The `oneNoteClientURL` link opens the notebook in the OneNote native client if it's installed. The `oneNoteWebURL` link opens the notebook in OneNote Online.</span></span>|
|<span data-ttu-id="bb214-151">displayName</span><span class="sxs-lookup"><span data-stu-id="bb214-151">displayName</span></span>|<span data-ttu-id="bb214-152">String</span><span class="sxs-lookup"><span data-stu-id="bb214-152">String</span></span>|<span data-ttu-id="bb214-153">El nombre del bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="bb214-153">The name of the notebook.</span></span>|
|<span data-ttu-id="bb214-154">sectionGroupsUrl</span><span class="sxs-lookup"><span data-stu-id="bb214-154">sectionGroupsUrl</span></span>|<span data-ttu-id="bb214-155">String</span><span class="sxs-lookup"><span data-stu-id="bb214-155">String</span></span>|<span data-ttu-id="bb214-p110">La dirección URL de la propiedad de navegación `sectionGroups`, que devuelve todos los grupos de secciones del bloc de notas. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bb214-p110">The URL for the `sectionGroups` navigation property, which returns all the section groups in the notebook. Read-only.</span></span>|
|<span data-ttu-id="bb214-158">sectionsUrl</span><span class="sxs-lookup"><span data-stu-id="bb214-158">sectionsUrl</span></span>|<span data-ttu-id="bb214-159">String</span><span class="sxs-lookup"><span data-stu-id="bb214-159">String</span></span>|<span data-ttu-id="bb214-p111">La dirección URL de la propiedad de navegación `sections`, que devuelve todas las secciones del bloc de notas. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bb214-p111">The URL for the `sections` navigation property, which returns all the sections in the notebook. Read-only.</span></span>|
|<span data-ttu-id="bb214-162">self</span><span class="sxs-lookup"><span data-stu-id="bb214-162">self</span></span>|<span data-ttu-id="bb214-163">String</span><span class="sxs-lookup"><span data-stu-id="bb214-163">String</span></span>|<span data-ttu-id="bb214-p112">El punto de conexión donde puede obtener información detallada sobre el bloc de notas. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bb214-p112">The endpoint where you can get details about the notebook. Read-only.</span></span>|
|<span data-ttu-id="bb214-166">userRole</span><span class="sxs-lookup"><span data-stu-id="bb214-166">userRole</span></span>|<span data-ttu-id="bb214-167">String</span><span class="sxs-lookup"><span data-stu-id="bb214-167">String</span></span>|<span data-ttu-id="bb214-p113">Los valores posibles son `Owner`, `Contributor`, `Reader` y `None`. Owner representa el acceso de nivel de propietario al bloc de notas. Contributor representa el acceso de lectura/escritura al bloc de notas. Reader representa el acceso de solo lectura al bloc de notas. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bb214-p113">Possible values are: `Owner`, `Contributor`, `Reader`, `None`. Owner represents owner-level access to the notebook. Contributor represents read/write access to the notebook. Reader represents read-only access to the notebook. Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="bb214-173">Relaciones</span><span class="sxs-lookup"><span data-stu-id="bb214-173">Relationships</span></span>
| <span data-ttu-id="bb214-174">Relación</span><span class="sxs-lookup"><span data-stu-id="bb214-174">Relationship</span></span> | <span data-ttu-id="bb214-175">Tipo</span><span class="sxs-lookup"><span data-stu-id="bb214-175">Type</span></span>   |<span data-ttu-id="bb214-176">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb214-176">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bb214-177">sectionGroups</span><span class="sxs-lookup"><span data-stu-id="bb214-177">sectionGroups</span></span>|<span data-ttu-id="bb214-178">Colección [SectionGroup](sectiongroup.md)</span><span class="sxs-lookup"><span data-stu-id="bb214-178">[SectionGroup](sectiongroup.md) collection</span></span>|<span data-ttu-id="bb214-p114">Los grupos de secciones del bloc de notas. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="bb214-p114">The section groups in the notebook. Read-only. Nullable.</span></span>|
|<span data-ttu-id="bb214-182">sections</span><span class="sxs-lookup"><span data-stu-id="bb214-182">sections</span></span>|<span data-ttu-id="bb214-183">Colección [Section](section.md)</span><span class="sxs-lookup"><span data-stu-id="bb214-183">[Section](section.md) collection</span></span>|<span data-ttu-id="bb214-p115">Secciones del bloc de notas. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="bb214-p115">The sections in the notebook. Read-only. Nullable.</span></span>|

## <a name="methods"></a><span data-ttu-id="bb214-187">Métodos</span><span class="sxs-lookup"><span data-stu-id="bb214-187">Methods</span></span>

| <span data-ttu-id="bb214-188">Método</span><span class="sxs-lookup"><span data-stu-id="bb214-188">Method</span></span>           | <span data-ttu-id="bb214-189">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb214-189">Return Type</span></span>    |<span data-ttu-id="bb214-190">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb214-190">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="bb214-191">Obtener bloc de notas</span><span class="sxs-lookup"><span data-stu-id="bb214-191">Get notebook</span></span>](../api/notebook-get.md) | [<span data-ttu-id="bb214-192">Notebook</span><span class="sxs-lookup"><span data-stu-id="bb214-192">Notebook</span></span>](notebook.md) |<span data-ttu-id="bb214-193">Leer las propiedades y las relaciones del bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="bb214-193">Read the properties and relationships of the notebook.</span></span>|
|[<span data-ttu-id="bb214-194">getRecentNotebooks</span><span class="sxs-lookup"><span data-stu-id="bb214-194">getRecentNotebooks</span></span>](../api/notebook-getrecentnotebooks.md) | <span data-ttu-id="bb214-195">Colección [recentNotebook](recentnotebook.md)</span><span class="sxs-lookup"><span data-stu-id="bb214-195">[recentNotebook](recentnotebook.md) collection</span></span> | <span data-ttu-id="bb214-196">Obtener una colección de los blocs de notas a los que ha tenido acceso más recientemente el usuario.</span><span class="sxs-lookup"><span data-stu-id="bb214-196">Get a collection of the most recently accessed notebooks for the user.</span></span> |
|[<span data-ttu-id="bb214-197">Crear grupo de secciones</span><span class="sxs-lookup"><span data-stu-id="bb214-197">Create section group</span></span>](../api/notebook-post-sectiongroups.md) |[<span data-ttu-id="bb214-198">SectionGroup</span><span class="sxs-lookup"><span data-stu-id="bb214-198">SectionGroup</span></span>](sectiongroup.md)| <span data-ttu-id="bb214-199">Crear un grupo de secciones publicándolo en el bloc de notas especificado de la colección sectionGroups.</span><span class="sxs-lookup"><span data-stu-id="bb214-199">Create a section group by posting to the sectionGroups collection in the specified notebook.</span></span>|
|[<span data-ttu-id="bb214-200">Enumerar grupos de secciones</span><span class="sxs-lookup"><span data-stu-id="bb214-200">List section groups</span></span>](../api/notebook-list-sectiongroups.md) |<span data-ttu-id="bb214-201">Colección [SectionGroup](sectiongroup.md)</span><span class="sxs-lookup"><span data-stu-id="bb214-201">[SectionGroup](sectiongroup.md) collection</span></span>| <span data-ttu-id="bb214-202">Obtener una colección de grupos de secciones en el bloc de notas especificado.</span><span class="sxs-lookup"><span data-stu-id="bb214-202">Get a collection of section groups in the specified notebook.</span></span>|
|[<span data-ttu-id="bb214-203">Crear sección</span><span class="sxs-lookup"><span data-stu-id="bb214-203">Create section</span></span>](../api/notebook-post-sections.md) |[<span data-ttu-id="bb214-204">Section</span><span class="sxs-lookup"><span data-stu-id="bb214-204">Section</span></span>](section.md)| <span data-ttu-id="bb214-205">Crear una sección publicándola en el bloc de notas especificado de la colección de secciones.</span><span class="sxs-lookup"><span data-stu-id="bb214-205">Create a section by posting to the sections collection in the specified notebook.</span></span>|
|[<span data-ttu-id="bb214-206">Enumerar secciones</span><span class="sxs-lookup"><span data-stu-id="bb214-206">List sections</span></span>](../api/notebook-list-sections.md) |<span data-ttu-id="bb214-207">Colección [Section](section.md)</span><span class="sxs-lookup"><span data-stu-id="bb214-207">[Section](section.md) collection</span></span>| <span data-ttu-id="bb214-208">Obtener una colección de secciones en el bloc de notas especificado.</span><span class="sxs-lookup"><span data-stu-id="bb214-208">Get a collection of sections in the specified notebook.</span></span>|
|[<span data-ttu-id="bb214-209">copyNotebook</span><span class="sxs-lookup"><span data-stu-id="bb214-209">copyNotebook</span></span>](../api/notebook-copynotebook.md)| <span data-ttu-id="bb214-210">Ninguno</span><span class="sxs-lookup"><span data-stu-id="bb214-210">None</span></span> | <span data-ttu-id="bb214-211">Copia un bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="bb214-211">Copies a notebook.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "notebook resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
