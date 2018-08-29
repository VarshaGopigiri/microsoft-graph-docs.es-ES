# <a name="section-resource-type"></a><span data-ttu-id="a109b-101">Tipo de recurso section</span><span class="sxs-lookup"><span data-stu-id="a109b-101">section resource type</span></span>

<span data-ttu-id="a109b-p101">Una sección en un bloc de notas de OneNote. Las secciones pueden contener páginas.</span><span class="sxs-lookup"><span data-stu-id="a109b-p101">A section in a OneNote notebook. Sections can contain pages.</span></span>

## <a name="json-representation"></a><span data-ttu-id="a109b-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a109b-104">JSON representation</span></span>

<span data-ttu-id="a109b-105">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a109b-105">Here is a JSON representation of the resource.</span></span>

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
## <a name="properties"></a><span data-ttu-id="a109b-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a109b-106">Properties</span></span>
| <span data-ttu-id="a109b-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a109b-107">Property</span></span>     | <span data-ttu-id="a109b-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="a109b-108">Type</span></span>   |<span data-ttu-id="a109b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="a109b-109">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a109b-110">createdBy</span><span class="sxs-lookup"><span data-stu-id="a109b-110">createdBy</span></span>|[<span data-ttu-id="a109b-111">identitySet</span><span class="sxs-lookup"><span data-stu-id="a109b-111">identitySet</span></span>](identityset.md)|<span data-ttu-id="a109b-p102">Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a109b-p102">Identity of the user, device, and application which created the item. Read-only.</span></span>|
|<span data-ttu-id="a109b-114">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="a109b-114">createdDateTime</span></span>|<span data-ttu-id="a109b-115">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a109b-115">DateTimeOffset</span></span>|<span data-ttu-id="a109b-p103">La fecha y la hora en que se creó la sección. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a109b-p103">The date and time when the section was created. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|
|<span data-ttu-id="a109b-120">id</span><span class="sxs-lookup"><span data-stu-id="a109b-120">id</span></span>|<span data-ttu-id="a109b-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="a109b-121">String</span></span>|<span data-ttu-id="a109b-p104">El identificador único de la sección.  Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a109b-p104">The unique identifier of the section.  Read-only.</span></span>|
|<span data-ttu-id="a109b-124">isDefault</span><span class="sxs-lookup"><span data-stu-id="a109b-124">isDefault</span></span>|<span data-ttu-id="a109b-125">Booleano</span><span class="sxs-lookup"><span data-stu-id="a109b-125">Boolean</span></span>|<span data-ttu-id="a109b-p105">Indica si se trata de la sección predeterminada del usuario. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a109b-p105">Indicates whether this is the user's default section. Read-only.</span></span>|
|<span data-ttu-id="a109b-128">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="a109b-128">lastModifiedBy</span></span>|[<span data-ttu-id="a109b-129">identitySet</span><span class="sxs-lookup"><span data-stu-id="a109b-129">identitySet</span></span>](identityset.md)|<span data-ttu-id="a109b-p106">Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a109b-p106">Identity of the user, device, and application which created the item. Read-only.</span></span>|
|<span data-ttu-id="a109b-132">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="a109b-132">lastModifiedDateTime</span></span>|<span data-ttu-id="a109b-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a109b-133">DateTimeOffset</span></span>|<span data-ttu-id="a109b-p107">La fecha y la hora en que se modificó la sección por última vez. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a109b-p107">The date and time when the section was last modified. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|
|<span data-ttu-id="a109b-138">vínculos</span><span class="sxs-lookup"><span data-stu-id="a109b-138">links</span></span>|[<span data-ttu-id="a109b-139">SectionLinks</span><span class="sxs-lookup"><span data-stu-id="a109b-139">SectionLinks</span></span>](sectionlinks.md)|<span data-ttu-id="a109b-p108">Vínculos para abrir la sección. El vínculo `oneNoteClientURL` abre la sección en el cliente nativo de OneNote si está instalado. El vínculo `oneNoteWebURL` abre la sección en OneNote Online.</span><span class="sxs-lookup"><span data-stu-id="a109b-p108">Links for opening the section. The `oneNoteClientURL` link opens the section in the OneNote native client if it's installed. The `oneNoteWebURL` link opens the section in OneNote Online.</span></span>|
|<span data-ttu-id="a109b-143">displayName</span><span class="sxs-lookup"><span data-stu-id="a109b-143">displayName</span></span>|<span data-ttu-id="a109b-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="a109b-144">String</span></span>|<span data-ttu-id="a109b-145">Nombre de la sección.</span><span class="sxs-lookup"><span data-stu-id="a109b-145">The name of the section.</span></span> |
|<span data-ttu-id="a109b-146">pagesUrl</span><span class="sxs-lookup"><span data-stu-id="a109b-146">pagesUrl</span></span>|<span data-ttu-id="a109b-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="a109b-147">String</span></span>|<span data-ttu-id="a109b-p109">El punto de conexión `pages` donde puede obtener información detallada de todas las páginas de la sección. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a109b-p109">The `pages` endpoint where you can get details for all the pages in the section. Read-only.</span></span>|
|<span data-ttu-id="a109b-150">self</span><span class="sxs-lookup"><span data-stu-id="a109b-150">self</span></span>|<span data-ttu-id="a109b-151">Cadena</span><span class="sxs-lookup"><span data-stu-id="a109b-151">String</span></span>|<span data-ttu-id="a109b-p110">El punto de conexión donde puede obtener información detallada sobre la sección. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a109b-p110">The endpoint where you can get details about the section. Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="a109b-154">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a109b-154">Relationships</span></span>
| <span data-ttu-id="a109b-155">Relación</span><span class="sxs-lookup"><span data-stu-id="a109b-155">Relationship</span></span> | <span data-ttu-id="a109b-156">Tipo</span><span class="sxs-lookup"><span data-stu-id="a109b-156">Type</span></span>   |<span data-ttu-id="a109b-157">Descripción</span><span class="sxs-lookup"><span data-stu-id="a109b-157">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a109b-158">pages</span><span class="sxs-lookup"><span data-stu-id="a109b-158">pages</span></span>|<span data-ttu-id="a109b-159">Colección de [OnenotePage](page.md)</span><span class="sxs-lookup"><span data-stu-id="a109b-159">[OnenotePage](page.md) collection</span></span>|<span data-ttu-id="a109b-p111">Colección de páginas de la sección. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="a109b-p111">The collection of pages in the section.  Read-only. Nullable.</span></span>|
|<span data-ttu-id="a109b-163">parentNotebook</span><span class="sxs-lookup"><span data-stu-id="a109b-163">parentNotebook</span></span>|[<span data-ttu-id="a109b-164">Notebook</span><span class="sxs-lookup"><span data-stu-id="a109b-164">Notebook</span></span>](notebook.md)|<span data-ttu-id="a109b-p112">Bloc de notas que contiene la sección.  Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a109b-p112">The notebook that contains the section.  Read-only.</span></span>|
|<span data-ttu-id="a109b-167">parentSectionGroup</span><span class="sxs-lookup"><span data-stu-id="a109b-167">parentSectionGroup</span></span>|[<span data-ttu-id="a109b-168">SectionGroup</span><span class="sxs-lookup"><span data-stu-id="a109b-168">SectionGroup</span></span>](sectiongroup.md)|<span data-ttu-id="a109b-p113">Grupo de secciones que contiene la sección.  Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a109b-p113">The section group that contains the section.  Read-only.</span></span>|

## <a name="methods"></a><span data-ttu-id="a109b-171">Métodos</span><span class="sxs-lookup"><span data-stu-id="a109b-171">Methods</span></span>

| <span data-ttu-id="a109b-172">Método</span><span class="sxs-lookup"><span data-stu-id="a109b-172">Method</span></span>           | <span data-ttu-id="a109b-173">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a109b-173">Return Type</span></span>    |<span data-ttu-id="a109b-174">Descripción</span><span class="sxs-lookup"><span data-stu-id="a109b-174">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="a109b-175">Obtener sección</span><span class="sxs-lookup"><span data-stu-id="a109b-175">Get section</span></span>](../api/section_get.md) | [<span data-ttu-id="a109b-176">OnenoteSection</span><span class="sxs-lookup"><span data-stu-id="a109b-176">OnenoteSection</span></span>](section.md) |<span data-ttu-id="a109b-177">Leer las propiedades y las relaciones de la sección.</span><span class="sxs-lookup"><span data-stu-id="a109b-177">Read the properties and relationships of the section.</span></span>|
|[<span data-ttu-id="a109b-178">Crear página</span><span class="sxs-lookup"><span data-stu-id="a109b-178">Create page</span></span>](../api/section_post_pages.md) |[<span data-ttu-id="a109b-179">Page</span><span class="sxs-lookup"><span data-stu-id="a109b-179">Page</span></span>](page.md)| <span data-ttu-id="a109b-180">Crear una página publicándola en la sección especificada de la colección de páginas.</span><span class="sxs-lookup"><span data-stu-id="a109b-180">Create a page by posting to the pages collection in the specified section.</span></span>|
|[<span data-ttu-id="a109b-181">Enumerar páginas</span><span class="sxs-lookup"><span data-stu-id="a109b-181">List pages</span></span>](../api/section_list_pages.md) |<span data-ttu-id="a109b-182">Colección [Page](page.md)</span><span class="sxs-lookup"><span data-stu-id="a109b-182">[Page](page.md) collection</span></span>| <span data-ttu-id="a109b-183">Obtener una colección de páginas en la sección especificada.</span><span class="sxs-lookup"><span data-stu-id="a109b-183">Get a collection of pages in the specified section.</span></span>|
|[<span data-ttu-id="a109b-184">copyToNotebook</span><span class="sxs-lookup"><span data-stu-id="a109b-184">copyToNotebook</span></span>](../api/section_copytonotebook.md)|<span data-ttu-id="a109b-185">Ninguno</span><span class="sxs-lookup"><span data-stu-id="a109b-185">None</span></span>|<span data-ttu-id="a109b-186">Copiar la sección en un bloc de notas específico.</span><span class="sxs-lookup"><span data-stu-id="a109b-186">Copy the section to a specific notebook.</span></span>|
|[<span data-ttu-id="a109b-187">copyToSectionGroup</span><span class="sxs-lookup"><span data-stu-id="a109b-187">copyToSectionGroup</span></span>](../api/section_copytosectiongroup.md)|<span data-ttu-id="a109b-188">Ninguno</span><span class="sxs-lookup"><span data-stu-id="a109b-188">None</span></span>|<span data-ttu-id="a109b-189">Copiar la sección en un grupo de secciones específico.</span><span class="sxs-lookup"><span data-stu-id="a109b-189">Copy the section to a specific section group.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onenoteSection resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
