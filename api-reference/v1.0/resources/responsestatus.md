# <a name="responsestatus-resource-type"></a><span data-ttu-id="6afc8-101">Tipo de recurso responseStatus</span><span class="sxs-lookup"><span data-stu-id="6afc8-101">responseStatus resource type</span></span>

<span data-ttu-id="6afc8-102">Estado de la respuesta de una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="6afc8-102">The response status of a meeting request.</span></span>

## <a name="properties"></a><span data-ttu-id="6afc8-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6afc8-103">Properties</span></span>

| <span data-ttu-id="6afc8-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6afc8-104">Property</span></span> | <span data-ttu-id="6afc8-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="6afc8-105">Type</span></span>           | <span data-ttu-id="6afc8-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="6afc8-106">Description</span></span> |
|:---------|:---------------|:------------|
| <span data-ttu-id="6afc8-107">response</span><span class="sxs-lookup"><span data-stu-id="6afc8-107">response</span></span> | <span data-ttu-id="6afc8-108">String</span><span class="sxs-lookup"><span data-stu-id="6afc8-108">String</span></span>         | <span data-ttu-id="6afc8-109">Tipo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6afc8-109">The response type.</span></span> <span data-ttu-id="6afc8-110">Los valores posibles son: `None`, `Organizer`, `TentativelyAccepted`, `Accepted`, `Declined` y `NotResponded`.</span><span class="sxs-lookup"><span data-stu-id="6afc8-110">Possible values are: `None`, `Organizer`, `TentativelyAccepted`, `Accepted`, `Declined`, `NotResponded`.</span></span>
| <span data-ttu-id="6afc8-111">time</span><span class="sxs-lookup"><span data-stu-id="6afc8-111">time</span></span>     | <span data-ttu-id="6afc8-112">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6afc8-112">DateTimeOffset</span></span> | <span data-ttu-id="6afc8-113">Fecha y hora en que se devolvió la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6afc8-113">The date and time that the response was returned.</span></span> <span data-ttu-id="6afc8-114">Usa el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="6afc8-114">It uses ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="6afc8-115">Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="6afc8-115">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'` Read-only.</span></span>

## <a name="json-representation"></a><span data-ttu-id="6afc8-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6afc8-116">JSON representation</span></span>

<span data-ttu-id="6afc8-117">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="6afc8-117">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.responseStatus"
}-->

```json
{
  "response": "String",
  "time": "String (timestamp)"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "responseStatus resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
