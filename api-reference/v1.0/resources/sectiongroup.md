# <a name="sectiongroup-resource-type"></a><span data-ttu-id="2fd29-101">Tipo de recurso sectionGroup</span><span class="sxs-lookup"><span data-stu-id="2fd29-101">sectionGroup resource type</span></span>

<span data-ttu-id="2fd29-p101">Un grupo de secciones en un bloc de notas de OneNote. Los grupos de secciones pueden contener secciones y grupos de secciones.</span><span class="sxs-lookup"><span data-stu-id="2fd29-p101">A section group in a OneNote notebook. Section groups can contain sections and section groups.</span></span>

## <a name="json-representation"></a><span data-ttu-id="2fd29-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2fd29-104">JSON representation</span></span>

<span data-ttu-id="2fd29-105">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2fd29-105">Here is a JSON representation of the resource.</span></span>

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
## <a name="properties"></a><span data-ttu-id="2fd29-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2fd29-106">Properties</span></span>
| <span data-ttu-id="2fd29-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2fd29-107">Property</span></span>     | <span data-ttu-id="2fd29-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fd29-108">Type</span></span>   |<span data-ttu-id="2fd29-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="2fd29-109">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2fd29-110">createdBy</span><span class="sxs-lookup"><span data-stu-id="2fd29-110">createdBy</span></span>|[<span data-ttu-id="2fd29-111">identitySet</span><span class="sxs-lookup"><span data-stu-id="2fd29-111">identitySet</span></span>](identityset.md)|<span data-ttu-id="2fd29-p102">Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2fd29-p102">Identity of the user, device, and application which created the item. Read-only.</span></span>|
|<span data-ttu-id="2fd29-114">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="2fd29-114">createdDateTime</span></span>|<span data-ttu-id="2fd29-115">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2fd29-115">DateTimeOffset</span></span>|<span data-ttu-id="2fd29-p103">La fecha y la hora en que se creó el grupo de secciones. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2fd29-p103">The date and time when the section group was created. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|
|<span data-ttu-id="2fd29-120">id</span><span class="sxs-lookup"><span data-stu-id="2fd29-120">id</span></span>|<span data-ttu-id="2fd29-121">String</span><span class="sxs-lookup"><span data-stu-id="2fd29-121">String</span></span>|<span data-ttu-id="2fd29-p104">El identificador único del grupo de secciones. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2fd29-p104">The unique identifier of the section group. Read-only.</span></span>|
|<span data-ttu-id="2fd29-124">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="2fd29-124">lastModifiedBy</span></span>|[<span data-ttu-id="2fd29-125">identitySet</span><span class="sxs-lookup"><span data-stu-id="2fd29-125">identitySet</span></span>](identityset.md)|<span data-ttu-id="2fd29-p105">Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2fd29-p105">Identity of the user, device, and application which created the item. Read-only.</span></span>|
|<span data-ttu-id="2fd29-128">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="2fd29-128">lastModifiedDateTime</span></span>|<span data-ttu-id="2fd29-129">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2fd29-129">DateTimeOffset</span></span>|<span data-ttu-id="2fd29-p106">La fecha y la hora en que se modificó por última vez el grupo de secciones. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2fd29-p106">The date and time when the section group was last modified. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|
|<span data-ttu-id="2fd29-134">displayName</span><span class="sxs-lookup"><span data-stu-id="2fd29-134">displayName</span></span>|<span data-ttu-id="2fd29-135">Cadena</span><span class="sxs-lookup"><span data-stu-id="2fd29-135">String</span></span>|<span data-ttu-id="2fd29-136">El nombre del grupo de secciones.</span><span class="sxs-lookup"><span data-stu-id="2fd29-136">The name of the section group.</span></span>|
|<span data-ttu-id="2fd29-137">sectionGroupsUrl</span><span class="sxs-lookup"><span data-stu-id="2fd29-137">sectionGroupsUrl</span></span>|<span data-ttu-id="2fd29-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="2fd29-138">String</span></span>|<span data-ttu-id="2fd29-p107">La dirección URL de la propiedad de navegación `sectionGroups`, que devuelve todos los grupos de secciones del grupo de secciones. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2fd29-p107">The URL for the `sectionGroups` navigation property, which returns all the section groups in the section group. Read-only.</span></span>|
|<span data-ttu-id="2fd29-141">sectionsUrl</span><span class="sxs-lookup"><span data-stu-id="2fd29-141">sectionsUrl</span></span>|<span data-ttu-id="2fd29-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="2fd29-142">String</span></span>|<span data-ttu-id="2fd29-p108">La dirección URL de la propiedad de navegación `sections`, que devuelve todas las secciones del grupo de secciones. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2fd29-p108">The URL for the `sections` navigation property, which returns all the sections in the section group. Read-only.</span></span>|
|<span data-ttu-id="2fd29-145">self</span><span class="sxs-lookup"><span data-stu-id="2fd29-145">self</span></span>|<span data-ttu-id="2fd29-146">String</span><span class="sxs-lookup"><span data-stu-id="2fd29-146">String</span></span>|<span data-ttu-id="2fd29-p109">El punto de conexión donde puede obtener información detallada sobre el grupo de secciones. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2fd29-p109">The endpoint where you can get details about the section group. Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="2fd29-149">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2fd29-149">Relationships</span></span>
| <span data-ttu-id="2fd29-150">Relación</span><span class="sxs-lookup"><span data-stu-id="2fd29-150">Relationship</span></span> | <span data-ttu-id="2fd29-151">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fd29-151">Type</span></span>   |<span data-ttu-id="2fd29-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="2fd29-152">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2fd29-153">parentNotebook</span><span class="sxs-lookup"><span data-stu-id="2fd29-153">parentNotebook</span></span>|[<span data-ttu-id="2fd29-154">Notebook</span><span class="sxs-lookup"><span data-stu-id="2fd29-154">Notebook</span></span>](notebook.md)|<span data-ttu-id="2fd29-p110">Bloc de notas que contiene el grupo de secciones. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2fd29-p110">The notebook that contains the section group. Read-only.</span></span>|
|<span data-ttu-id="2fd29-157">parentSectionGroup</span><span class="sxs-lookup"><span data-stu-id="2fd29-157">parentSectionGroup</span></span>|[<span data-ttu-id="2fd29-158">SectionGroup</span><span class="sxs-lookup"><span data-stu-id="2fd29-158">SectionGroup</span></span>](sectiongroup.md)|<span data-ttu-id="2fd29-p111">Grupo de secciones que contiene el grupo de secciones. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2fd29-p111">The section group that contains the section group. Read-only.</span></span>|
|<span data-ttu-id="2fd29-161">sectionGroups</span><span class="sxs-lookup"><span data-stu-id="2fd29-161">sectionGroups</span></span>|<span data-ttu-id="2fd29-162">Colección [SectionGroup](sectiongroup.md)</span><span class="sxs-lookup"><span data-stu-id="2fd29-162">[SectionGroup](sectiongroup.md) collection</span></span>|<span data-ttu-id="2fd29-p112">Grupos de secciones de la sección. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="2fd29-p112">The section groups in the section. Read-only. Nullable.</span></span>|
|<span data-ttu-id="2fd29-166">sections</span><span class="sxs-lookup"><span data-stu-id="2fd29-166">sections</span></span>|<span data-ttu-id="2fd29-167">Colección [Section](section.md)</span><span class="sxs-lookup"><span data-stu-id="2fd29-167">[Section](section.md) collection</span></span>|<span data-ttu-id="2fd29-p113">Secciones del grupo de secciones. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="2fd29-p113">The sections in the section group. Read-only. Nullable.</span></span>|

## <a name="methods"></a><span data-ttu-id="2fd29-171">Métodos</span><span class="sxs-lookup"><span data-stu-id="2fd29-171">Methods</span></span>

| <span data-ttu-id="2fd29-172">Método</span><span class="sxs-lookup"><span data-stu-id="2fd29-172">Method</span></span>           | <span data-ttu-id="2fd29-173">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2fd29-173">Return Type</span></span>    |<span data-ttu-id="2fd29-174">Descripción</span><span class="sxs-lookup"><span data-stu-id="2fd29-174">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="2fd29-175">Obtener grupo de secciones</span><span class="sxs-lookup"><span data-stu-id="2fd29-175">Get section group</span></span>](../api/sectiongroup_get.md) | [<span data-ttu-id="2fd29-176">SectionGroup</span><span class="sxs-lookup"><span data-stu-id="2fd29-176">SectionGroup</span></span>](sectiongroup.md) |<span data-ttu-id="2fd29-177">Leer las propiedades y las relaciones del grupo de secciones.</span><span class="sxs-lookup"><span data-stu-id="2fd29-177">Read the properties and relationships of the section group.</span></span>|
|[<span data-ttu-id="2fd29-178">Crear grupo de secciones</span><span class="sxs-lookup"><span data-stu-id="2fd29-178">Create section group</span></span>](../api/sectiongroup_post_sectiongroups.md) |[<span data-ttu-id="2fd29-179">SectionGroup</span><span class="sxs-lookup"><span data-stu-id="2fd29-179">SectionGroup</span></span>](sectiongroup.md)| <span data-ttu-id="2fd29-180">Crear un grupo de secciones publicándolo en el grupo de secciones especificado de la colección sectionGroups.</span><span class="sxs-lookup"><span data-stu-id="2fd29-180">Create a section group by posting to the sectionGroups collection in the specified section group.</span></span>|
|[<span data-ttu-id="2fd29-181">Enumerar grupos de secciones</span><span class="sxs-lookup"><span data-stu-id="2fd29-181">List section groups</span></span>](../api/sectiongroup_list_sectiongroups.md) |<span data-ttu-id="2fd29-182">Colección [SectionGroup](sectiongroup.md)</span><span class="sxs-lookup"><span data-stu-id="2fd29-182">[SectionGroup](sectiongroup.md) collection</span></span>| <span data-ttu-id="2fd29-183">Obtener una colección de grupos de secciones en el grupo de secciones especificado.</span><span class="sxs-lookup"><span data-stu-id="2fd29-183">Get collection of section groups in the specified section group.</span></span>|
|[<span data-ttu-id="2fd29-184">Crear sección</span><span class="sxs-lookup"><span data-stu-id="2fd29-184">Create section</span></span>](../api/sectiongroup_post_sections.md) |[<span data-ttu-id="2fd29-185">Section</span><span class="sxs-lookup"><span data-stu-id="2fd29-185">Section</span></span>](section.md)| <span data-ttu-id="2fd29-186">Crear una sección publicándola en el grupo de secciones especificado de la colección de secciones.</span><span class="sxs-lookup"><span data-stu-id="2fd29-186">Create a section by posting to the sections collection in the specified section group.</span></span>|
|[<span data-ttu-id="2fd29-187">Enumerar secciones</span><span class="sxs-lookup"><span data-stu-id="2fd29-187">List sections</span></span>](../api/sectiongroup_list_sections.md) |<span data-ttu-id="2fd29-188">Colección [Section](section.md)</span><span class="sxs-lookup"><span data-stu-id="2fd29-188">[Section](section.md) collection</span></span>| <span data-ttu-id="2fd29-189">Obtener una colección de secciones en el grupo de secciones especificado.</span><span class="sxs-lookup"><span data-stu-id="2fd29-189">Get a collection of sections in the specified section group.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "sectionGroup resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
