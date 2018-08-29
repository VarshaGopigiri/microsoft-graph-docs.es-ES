# <a name="page-resource-type"></a><span data-ttu-id="27bab-101">Tipo de recurso page</span><span class="sxs-lookup"><span data-stu-id="27bab-101">page resource type</span></span>

<span data-ttu-id="27bab-102">Una página de un bloc de notas de OneNote.</span><span class="sxs-lookup"><span data-stu-id="27bab-102">A page in a OneNote notebook.</span></span>

## <a name="json-representation"></a><span data-ttu-id="27bab-103">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="27bab-103">JSON representation</span></span>

<span data-ttu-id="27bab-104">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="27bab-104">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.onenoteEntitySchemaObjectModel",
  "optionalProperties": [
    "parentNotebook",
    "parentSection"
  ],
  "isMediaEntity": true,
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
## <a name="properties"></a><span data-ttu-id="27bab-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="27bab-105">Properties</span></span>
| <span data-ttu-id="27bab-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="27bab-106">Property</span></span>     | <span data-ttu-id="27bab-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="27bab-107">Type</span></span>   |<span data-ttu-id="27bab-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="27bab-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="27bab-109">content</span><span class="sxs-lookup"><span data-stu-id="27bab-109">content</span></span>|<span data-ttu-id="27bab-110">Secuencia</span><span class="sxs-lookup"><span data-stu-id="27bab-110">Stream</span></span>|<span data-ttu-id="27bab-111">Contenido HTML de la página.</span><span class="sxs-lookup"><span data-stu-id="27bab-111">The page's HTML content.</span></span>|
|<span data-ttu-id="27bab-112">contentUrl</span><span class="sxs-lookup"><span data-stu-id="27bab-112">contentUrl</span></span>|<span data-ttu-id="27bab-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="27bab-113">String</span></span>|<span data-ttu-id="27bab-p101">Dirección URL del contenido HTML de la página.  Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="27bab-p101">The URL for the page's HTML content.  Read-only.</span></span>|
|<span data-ttu-id="27bab-116">createdByAppId</span><span class="sxs-lookup"><span data-stu-id="27bab-116">createdByAppId</span></span>|<span data-ttu-id="27bab-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="27bab-117">String</span></span>|<span data-ttu-id="27bab-p102">Identificador único de la aplicación que creó la página. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="27bab-p102">The unique identifier of the application that created the page. Read-only.</span></span>|
|<span data-ttu-id="27bab-120">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="27bab-120">createdDateTime</span></span>|<span data-ttu-id="27bab-121">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="27bab-121">DateTimeOffset</span></span>|<span data-ttu-id="27bab-p103">La fecha y la hora en que se creó la página. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="27bab-p103">The date and time when the page was created. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|
|<span data-ttu-id="27bab-126">id</span><span class="sxs-lookup"><span data-stu-id="27bab-126">id</span></span>|<span data-ttu-id="27bab-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="27bab-127">String</span></span>|<span data-ttu-id="27bab-p104">Identificador único de la página.  Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="27bab-p104">The unique identifier of the page.  Read-only.</span></span>|
|<span data-ttu-id="27bab-130">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="27bab-130">lastModifiedDateTime</span></span>|<span data-ttu-id="27bab-131">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="27bab-131">DateTimeOffset</span></span>|<span data-ttu-id="27bab-p105">La fecha y la hora en que se modificó la página por última vez. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="27bab-p105">The date and time when the page was last modified. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|
|<span data-ttu-id="27bab-136">nivel</span><span class="sxs-lookup"><span data-stu-id="27bab-136">level</span></span>|<span data-ttu-id="27bab-137">Int32</span><span class="sxs-lookup"><span data-stu-id="27bab-137">Int32</span></span>|<span data-ttu-id="27bab-p106">Nivel de sangría de la página. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="27bab-p106">The indentation level of the page. Read-only.</span></span>|
|<span data-ttu-id="27bab-140">vínculos</span><span class="sxs-lookup"><span data-stu-id="27bab-140">links</span></span>|[<span data-ttu-id="27bab-141">PageLinks</span><span class="sxs-lookup"><span data-stu-id="27bab-141">PageLinks</span></span>](pagelinks.md)|<span data-ttu-id="27bab-p107">Vínculos para abrir la página. El vínculo `oneNoteClientURL` abre la página en el cliente nativo de OneNote si está instalado. El vínculo `oneNoteWebUrl` abre la página en OneNote Online. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="27bab-p107">Links for opening the page. The `oneNoteClientURL` link opens the page in the OneNote native client if it 's installed. The `oneNoteWebUrl` link opens the page in OneNote Online. Read-only.</span></span>|
|<span data-ttu-id="27bab-146">order</span><span class="sxs-lookup"><span data-stu-id="27bab-146">order</span></span>|<span data-ttu-id="27bab-147">Int32</span><span class="sxs-lookup"><span data-stu-id="27bab-147">Int32</span></span>|<span data-ttu-id="27bab-p108">El orden de la página dentro de su sección primaria. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="27bab-p108">The order of the page within its parent section. Read-only.</span></span>|
|<span data-ttu-id="27bab-150">self</span><span class="sxs-lookup"><span data-stu-id="27bab-150">self</span></span>|<span data-ttu-id="27bab-151">Cadena</span><span class="sxs-lookup"><span data-stu-id="27bab-151">String</span></span>|<span data-ttu-id="27bab-p109">El punto de conexión donde puede obtener información detallada sobre la página. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="27bab-p109">The endpoint where you can get details about the page. Read-only.</span></span>|
|<span data-ttu-id="27bab-154">title</span><span class="sxs-lookup"><span data-stu-id="27bab-154">title</span></span>|<span data-ttu-id="27bab-155">Cadena</span><span class="sxs-lookup"><span data-stu-id="27bab-155">String</span></span>|<span data-ttu-id="27bab-156">Título de la página.</span><span class="sxs-lookup"><span data-stu-id="27bab-156">The title of the page.</span></span> |

## <a name="relationships"></a><span data-ttu-id="27bab-157">Relaciones</span><span class="sxs-lookup"><span data-stu-id="27bab-157">Relationships</span></span>
| <span data-ttu-id="27bab-158">Relación</span><span class="sxs-lookup"><span data-stu-id="27bab-158">Relationship</span></span> | <span data-ttu-id="27bab-159">Tipo</span><span class="sxs-lookup"><span data-stu-id="27bab-159">Type</span></span>   |<span data-ttu-id="27bab-160">Descripción</span><span class="sxs-lookup"><span data-stu-id="27bab-160">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="27bab-161">parentNotebook</span><span class="sxs-lookup"><span data-stu-id="27bab-161">parentNotebook</span></span>|[<span data-ttu-id="27bab-162">Notebook</span><span class="sxs-lookup"><span data-stu-id="27bab-162">Notebook</span></span>](notebook.md)|<span data-ttu-id="27bab-p110">Bloc de notas que contiene la página.  Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="27bab-p110">The notebook that contains the page.  Read-only.</span></span>|
|<span data-ttu-id="27bab-165">parentSection</span><span class="sxs-lookup"><span data-stu-id="27bab-165">parentSection</span></span>|[<span data-ttu-id="27bab-166">OnenoteSection</span><span class="sxs-lookup"><span data-stu-id="27bab-166">OnenoteSection</span></span>](section.md)|<span data-ttu-id="27bab-p111">Sección que contiene la página. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="27bab-p111">The section that contains the page. Read-only.</span></span>|

## <a name="methods"></a><span data-ttu-id="27bab-169">Métodos</span><span class="sxs-lookup"><span data-stu-id="27bab-169">Methods</span></span>

| <span data-ttu-id="27bab-170">Método</span><span class="sxs-lookup"><span data-stu-id="27bab-170">Method</span></span>           | <span data-ttu-id="27bab-171">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="27bab-171">Return Type</span></span>    |<span data-ttu-id="27bab-172">Descripción</span><span class="sxs-lookup"><span data-stu-id="27bab-172">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="27bab-173">Obtener página</span><span class="sxs-lookup"><span data-stu-id="27bab-173">Get page</span></span>](../api/page_get.md) | [<span data-ttu-id="27bab-174">Page</span><span class="sxs-lookup"><span data-stu-id="27bab-174">Page</span></span>](page.md) |<span data-ttu-id="27bab-175">Leer las propiedades y las relaciones de la página.</span><span class="sxs-lookup"><span data-stu-id="27bab-175">Read the properties and relationships of the page.</span></span>|
|[<span data-ttu-id="27bab-176">Actualizar contenido de la página</span><span class="sxs-lookup"><span data-stu-id="27bab-176">Update page content</span></span>](../api/page_update.md) | <span data-ttu-id="27bab-177">Ninguno</span><span class="sxs-lookup"><span data-stu-id="27bab-177">None</span></span> |<span data-ttu-id="27bab-178">Actualizar el contenido HTML de la página.</span><span class="sxs-lookup"><span data-stu-id="27bab-178">Update the HTML content of the page.</span></span> |
|[<span data-ttu-id="27bab-179">Eliminar página</span><span class="sxs-lookup"><span data-stu-id="27bab-179">Delete page</span></span>](../api/page_delete.md) | <span data-ttu-id="27bab-180">Ninguno</span><span class="sxs-lookup"><span data-stu-id="27bab-180">None</span></span> |<span data-ttu-id="27bab-181">Eliminar la página.</span><span class="sxs-lookup"><span data-stu-id="27bab-181">Delete the page.</span></span> |
|[<span data-ttu-id="27bab-182">copyToSection</span><span class="sxs-lookup"><span data-stu-id="27bab-182">copyToSection</span></span>](../api/page_copytosection.md)| <span data-ttu-id="27bab-183">Ninguno</span><span class="sxs-lookup"><span data-stu-id="27bab-183">None</span></span> |<span data-ttu-id="27bab-184">Copia la página en una sección específica.</span><span class="sxs-lookup"><span data-stu-id="27bab-184">Copies the page to a specific section.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "page resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->