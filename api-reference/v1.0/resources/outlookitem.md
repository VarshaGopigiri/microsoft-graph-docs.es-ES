# <a name="outlookitem-resource-type"></a><span data-ttu-id="28c8b-101">Tipo de recurso outlookItem</span><span class="sxs-lookup"><span data-stu-id="28c8b-101">outlookItem resource type</span></span>



## <a name="json-representation"></a><span data-ttu-id="28c8b-102">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="28c8b-102">JSON representation</span></span>

<span data-ttu-id="28c8b-103">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="28c8b-103">Here is a JSON representation of the resource</span></span>

<!--{
  "blockType": "resource",
  "abstract": true,
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.outlookItem"
}-->

```json
{
  "categories": ["string"],
  "changeKey": "string",
  "createdDateTime": "String (timestamp)",
  "id": "string (identifier)",
  "lastModifiedDateTime": "String (timestamp)"
}

```
## <a name="properties"></a><span data-ttu-id="28c8b-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="28c8b-104">Properties</span></span>
| <span data-ttu-id="28c8b-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="28c8b-105">Property</span></span>     | <span data-ttu-id="28c8b-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="28c8b-106">Type</span></span>   |<span data-ttu-id="28c8b-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="28c8b-107">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="28c8b-108">categories</span><span class="sxs-lookup"><span data-stu-id="28c8b-108">categories</span></span>|<span data-ttu-id="28c8b-109">Colección String</span><span class="sxs-lookup"><span data-stu-id="28c8b-109">String collection</span></span>|<span data-ttu-id="28c8b-110">Las categorías asociadas al elemento</span><span class="sxs-lookup"><span data-stu-id="28c8b-110">The categories associated with the message.</span></span>|
|<span data-ttu-id="28c8b-111">changeKey</span><span class="sxs-lookup"><span data-stu-id="28c8b-111">changeKey</span></span>|<span data-ttu-id="28c8b-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="28c8b-112">String</span></span>|<span data-ttu-id="28c8b-113">Identifica la versión del elemento.</span><span class="sxs-lookup"><span data-stu-id="28c8b-113">Identifies the version of the contact.</span></span> <span data-ttu-id="28c8b-114">Cada vez que se cambia el contacto, también cambia changeKey.</span><span class="sxs-lookup"><span data-stu-id="28c8b-114">Every time the contact is changed, ChangeKey  changes as well.</span></span> <span data-ttu-id="28c8b-115">Esto permite que Exchange aplique cambios a la versión correcta del objeto.</span><span class="sxs-lookup"><span data-stu-id="28c8b-115">Identifies the version of the reminder. Every time the reminder is changed, changeKey changes as well. This allows Exchange to apply changes to the correct version of the object.</span></span> <span data-ttu-id="28c8b-116">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="28c8b-116">Read-only.</span></span>|
|<span data-ttu-id="28c8b-117">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="28c8b-117">createdDateTime</span></span>|<span data-ttu-id="28c8b-118">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="28c8b-118">DateTimeOffset</span></span>|<span data-ttu-id="28c8b-p102">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="28c8b-p102">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="28c8b-121">id</span><span class="sxs-lookup"><span data-stu-id="28c8b-121">id</span></span>|<span data-ttu-id="28c8b-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="28c8b-122">String</span></span>| <span data-ttu-id="28c8b-123">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="28c8b-123">Read-only.</span></span>|
|<span data-ttu-id="28c8b-124">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="28c8b-124">lastModifiedDateTime</span></span>|<span data-ttu-id="28c8b-125">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="28c8b-125">DateTimeOffset</span></span>|<span data-ttu-id="28c8b-p103">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="28c8b-p103">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|

## <a name="relationships"></a><span data-ttu-id="28c8b-128">Relaciones</span><span class="sxs-lookup"><span data-stu-id="28c8b-128">Relationships</span></span>
<span data-ttu-id="28c8b-129">Ninguna</span><span class="sxs-lookup"><span data-stu-id="28c8b-129">None</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "outlookItem resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
