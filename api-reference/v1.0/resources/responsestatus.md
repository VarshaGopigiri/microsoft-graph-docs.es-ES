# <a name="responsestatus-resource-type"></a><span data-ttu-id="2ad91-101">Tipo de recurso responseStatus</span><span class="sxs-lookup"><span data-stu-id="2ad91-101">responseStatus resource type</span></span>

<span data-ttu-id="2ad91-102">Estado de la respuesta de una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="2ad91-102">The response status of a meeting request.</span></span>

## <a name="properties"></a><span data-ttu-id="2ad91-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2ad91-103">Properties</span></span>

| <span data-ttu-id="2ad91-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2ad91-104">Property</span></span> | <span data-ttu-id="2ad91-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="2ad91-105">Type</span></span>           | <span data-ttu-id="2ad91-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ad91-106">Description</span></span> |
|:---------|:---------------|:------------|
| <span data-ttu-id="2ad91-107">response</span><span class="sxs-lookup"><span data-stu-id="2ad91-107">response</span></span> | <span data-ttu-id="2ad91-108">responseType</span><span class="sxs-lookup"><span data-stu-id="2ad91-108">ResponseType</span></span>   | <span data-ttu-id="2ad91-109">Tipo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2ad91-109">The response type.</span></span> <span data-ttu-id="2ad91-110">Los valores posibles son `None`, `Organizer`, `TentativelyAccepted`, `Accepted`, `Declined` y `NotResponded`.</span><span class="sxs-lookup"><span data-stu-id="2ad91-110">The possible values are `None`, `Organizer`, `TentativelyAccepted`, `Accepted`, `Declined`, `NotResponded`, , , , , , or .</span></span>
| <span data-ttu-id="2ad91-111">time</span><span class="sxs-lookup"><span data-stu-id="2ad91-111">time</span></span>     | <span data-ttu-id="2ad91-112">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2ad91-112">DateTimeOffset</span></span> | <span data-ttu-id="2ad91-p102">Fecha y hora en que se devolvió la respuesta. Usa el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="2ad91-p102">The date and time that the response was returned. It uses ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>

## <a name="json-representation"></a><span data-ttu-id="2ad91-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2ad91-116">JSON representation</span></span>

<span data-ttu-id="2ad91-117">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="2ad91-117">Here is a JSON representation of the resource</span></span>

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
