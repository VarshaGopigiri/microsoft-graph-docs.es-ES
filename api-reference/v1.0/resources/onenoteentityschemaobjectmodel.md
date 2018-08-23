# <a name="onenoteentityschemaobjectmodel-resource"></a><span data-ttu-id="7dc28-101">recurso onenoteEntitySchemaObjectModel</span><span class="sxs-lookup"><span data-stu-id="7dc28-101">onenoteEntitySchemaObjectModel resource</span></span>

<span data-ttu-id="7dc28-102">Este es un tipo base para las entidades de OneNote.</span><span class="sxs-lookup"><span data-stu-id="7dc28-102">This is a base type for OneNote entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="7dc28-103">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7dc28-103">JSON representation</span></span>

<span data-ttu-id="7dc28-104">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7dc28-104">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "abstract": true,
  "baseType": "microsoft.graph.onenoteEntityBaseModel",
  "optionalProperties": [
    "self"
  ],
  "@odata.type": "microsoft.graph.onenoteEntitySchemaObjectModel"
}-->

```json
{
  "createdDateTime": "String (timestamp)"
}

```
## <a name="properties"></a><span data-ttu-id="7dc28-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7dc28-105">Properties</span></span>
| <span data-ttu-id="7dc28-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7dc28-106">Property</span></span>     | <span data-ttu-id="7dc28-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="7dc28-107">Type</span></span>   |<span data-ttu-id="7dc28-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="7dc28-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7dc28-109">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="7dc28-109">createdDateTime</span></span>|<span data-ttu-id="7dc28-110">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7dc28-110">DateTimeOffset</span></span>|<span data-ttu-id="7dc28-p101">La fecha y la hora en que se creó la página. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7dc28-p101">The date and time when the page was created. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|

<!-- uuid: bfb567de-2a2a-4b81-bf47-a55626a0c166
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "page resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->