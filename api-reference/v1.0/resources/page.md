# <a name="page-resource-type"></a><span data-ttu-id="08900-101">Tipo de recurso page</span><span class="sxs-lookup"><span data-stu-id="08900-101">page resource type</span></span>

<span data-ttu-id="08900-102">Una página de un bloc de notas de OneNote.</span><span class="sxs-lookup"><span data-stu-id="08900-102">A page in a OneNote notebook.</span></span>

## <a name="json-representation"></a><span data-ttu-id="08900-103">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="08900-103">JSON representation</span></span>

<span data-ttu-id="08900-104">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="08900-104">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "parentNotebook",
    "parentSection"
  ],
  "@odata.type": "microsoft.graph.onenotePage"
}-->

```json
{
  "content": "stream",
  "contentUrl": "string",
  "createdByAppId": "string",
  "createdDateTime": "String (timestamp)",
  "id": "string (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "level": 1024,
  "links": {"@odata.type": "microsoft.graph.pageLinks"},
  "order": 1024,
  "self": "string",
  "title": "string"
}

```
## <a name="properties"></a><span data-ttu-id="08900-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="08900-105">Properties</span></span>
| <span data-ttu-id="08900-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="08900-106">Property</span></span>     | <span data-ttu-id="08900-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="08900-107">Type</span></span>   |<span data-ttu-id="08900-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="08900-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="08900-109">content</span><span class="sxs-lookup"><span data-stu-id="08900-109">content</span></span>|<span data-ttu-id="08900-110">Secuencia</span><span class="sxs-lookup"><span data-stu-id="08900-110">Stream</span></span>|<span data-ttu-id="08900-111">Contenido HTML de la página.</span><span class="sxs-lookup"><span data-stu-id="08900-111">The page's HTML content.</span></span>|
|<span data-ttu-id="08900-112">contentUrl</span><span class="sxs-lookup"><span data-stu-id="08900-112">contentUrl</span></span>|<span data-ttu-id="08900-113">String</span><span class="sxs-lookup"><span data-stu-id="08900-113">String</span></span>|<span data-ttu-id="08900-p101">Dirección URL del contenido HTML de la página.  Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="08900-p101">The URL for the page's HTML content.  Read-only.</span></span>|
|<span data-ttu-id="08900-116">createdByAppId</span><span class="sxs-lookup"><span data-stu-id="08900-116">createdByAppId</span></span>|<span data-ttu-id="08900-117">String</span><span class="sxs-lookup"><span data-stu-id="08900-117">String</span></span>|<span data-ttu-id="08900-p102">Identificador único de la aplicación que creó la página. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="08900-p102">The unique identifier of the application that created the page. Read-only.</span></span>|
|<span data-ttu-id="08900-120">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="08900-120">createdDateTime</span></span>|<span data-ttu-id="08900-121">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="08900-121">DateTimeOffset</span></span>|<span data-ttu-id="08900-p103">La fecha y la hora en que se creó la página. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="08900-p103">The date and time when the page was created. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|
|<span data-ttu-id="08900-126">id</span><span class="sxs-lookup"><span data-stu-id="08900-126">id</span></span>|<span data-ttu-id="08900-127">String</span><span class="sxs-lookup"><span data-stu-id="08900-127">String</span></span>|<span data-ttu-id="08900-p104">Identificador único de la página.  Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="08900-p104">The unique identifier of the page.  Read-only.</span></span>|
|<span data-ttu-id="08900-130">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="08900-130">lastModifiedDateTime</span></span>|<span data-ttu-id="08900-131">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="08900-131">DateTimeOffset</span></span>|<span data-ttu-id="08900-p105">La fecha y la hora en que se modificó la página por última vez. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="08900-p105">The date and time when the page was last modified. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|
|<span data-ttu-id="08900-136">nivel</span><span class="sxs-lookup"><span data-stu-id="08900-136">level</span></span>|<span data-ttu-id="08900-137">Int32</span><span class="sxs-lookup"><span data-stu-id="08900-137">Int32</span></span>|<span data-ttu-id="08900-p106">Nivel de sangría de la página. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="08900-p106">The indentation level of the page. Read-only.</span></span>|
|<span data-ttu-id="08900-140">vínculos</span><span class="sxs-lookup"><span data-stu-id="08900-140">links</span></span>|[<span data-ttu-id="08900-141">PageLinks</span><span class="sxs-lookup"><span data-stu-id="08900-141">PageLinks</span></span>](pagelinks.md)|<span data-ttu-id="08900-p107">Vínculos para abrir la página. El vínculo `oneNoteClientURL` abre la página en el cliente nativo de OneNote si está instalado. El vínculo `oneNoteWebUrl` abre la página en OneNote Online. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="08900-p107">Links for opening the page. The `oneNoteClientURL` link opens the page in the OneNote native client if it 's installed. The `oneNoteWebUrl` link opens the page in OneNote Online. Read-only.</span></span>|
|<span data-ttu-id="08900-146">order</span><span class="sxs-lookup"><span data-stu-id="08900-146">order</span></span>|<span data-ttu-id="08900-147">Int32</span><span class="sxs-lookup"><span data-stu-id="08900-147">Int32</span></span>|<span data-ttu-id="08900-p108">El orden de la página dentro de su sección primaria. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="08900-p108">The order of the page within its parent section. Read-only.</span></span>|
|<span data-ttu-id="08900-150">self</span><span class="sxs-lookup"><span data-stu-id="08900-150">self</span></span>|<span data-ttu-id="08900-151">String</span><span class="sxs-lookup"><span data-stu-id="08900-151">String</span></span>|<span data-ttu-id="08900-p109">El punto de conexión donde puede obtener información detallada sobre la página. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="08900-p109">The endpoint where you can get details about the page. Read-only.</span></span>|
|<span data-ttu-id="08900-154">title</span><span class="sxs-lookup"><span data-stu-id="08900-154">title</span></span>|<span data-ttu-id="08900-155">Cadena</span><span class="sxs-lookup"><span data-stu-id="08900-155">String</span></span>|<span data-ttu-id="08900-156">Título de la página.</span><span class="sxs-lookup"><span data-stu-id="08900-156">The title of the page.</span></span> |

## <a name="relationships"></a><span data-ttu-id="08900-157">Relaciones</span><span class="sxs-lookup"><span data-stu-id="08900-157">Relationships</span></span>
| <span data-ttu-id="08900-158">Relación</span><span class="sxs-lookup"><span data-stu-id="08900-158">Relationship</span></span> | <span data-ttu-id="08900-159">Tipo</span><span class="sxs-lookup"><span data-stu-id="08900-159">Type</span></span>   |<span data-ttu-id="08900-160">Descripción</span><span class="sxs-lookup"><span data-stu-id="08900-160">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="08900-161">parentNotebook</span><span class="sxs-lookup"><span data-stu-id="08900-161">parentNotebook</span></span>|[<span data-ttu-id="08900-162">Notebook</span><span class="sxs-lookup"><span data-stu-id="08900-162">Notebook</span></span>](notebook.md)|<span data-ttu-id="08900-p110">Bloc de notas que contiene la página.  Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="08900-p110">The notebook that contains the page.  Read-only.</span></span>|
|<span data-ttu-id="08900-165">parentSection</span><span class="sxs-lookup"><span data-stu-id="08900-165">parentSection</span></span>|[<span data-ttu-id="08900-166">Section</span><span class="sxs-lookup"><span data-stu-id="08900-166">Section</span></span>](section.md)|<span data-ttu-id="08900-p111">Sección que contiene la página. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="08900-p111">The section that contains the page. Read-only.</span></span>|

## <a name="methods"></a><span data-ttu-id="08900-169">Métodos</span><span class="sxs-lookup"><span data-stu-id="08900-169">Methods</span></span>

| <span data-ttu-id="08900-170">Método</span><span class="sxs-lookup"><span data-stu-id="08900-170">Method</span></span>           | <span data-ttu-id="08900-171">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="08900-171">Return Type</span></span>    |<span data-ttu-id="08900-172">Descripción</span><span class="sxs-lookup"><span data-stu-id="08900-172">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="08900-173">Obtener página</span><span class="sxs-lookup"><span data-stu-id="08900-173">Get page</span></span>](../api/page_get.md) | [<span data-ttu-id="08900-174">Page</span><span class="sxs-lookup"><span data-stu-id="08900-174">Page</span></span>](page.md) |<span data-ttu-id="08900-175">Leer las propiedades y las relaciones de la página.</span><span class="sxs-lookup"><span data-stu-id="08900-175">Read the properties and relationships of the page.</span></span>|
|[<span data-ttu-id="08900-176">Actualizar contenido de la página</span><span class="sxs-lookup"><span data-stu-id="08900-176">Update page content</span></span>](../api/page_update.md) | <span data-ttu-id="08900-177">Ninguno</span><span class="sxs-lookup"><span data-stu-id="08900-177">None</span></span> |<span data-ttu-id="08900-178">Actualizar el contenido HTML de la página.</span><span class="sxs-lookup"><span data-stu-id="08900-178">Update the HTML content of the page.</span></span> |
|[<span data-ttu-id="08900-179">Eliminar página</span><span class="sxs-lookup"><span data-stu-id="08900-179">Delete page</span></span>](../api/page_delete.md) | <span data-ttu-id="08900-180">Ninguno</span><span class="sxs-lookup"><span data-stu-id="08900-180">None</span></span> |<span data-ttu-id="08900-181">Eliminar la página.</span><span class="sxs-lookup"><span data-stu-id="08900-181">Delete the page.</span></span> |
|[<span data-ttu-id="08900-182">copyToSection</span><span class="sxs-lookup"><span data-stu-id="08900-182">copyToSection</span></span>](../api/page_copytosection.md)| <span data-ttu-id="08900-183">Ninguno</span><span class="sxs-lookup"><span data-stu-id="08900-183">None</span></span> |<span data-ttu-id="08900-184">Copia la página en una sección específica.</span><span class="sxs-lookup"><span data-stu-id="08900-184">Copies the page to a specific section.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "page resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->