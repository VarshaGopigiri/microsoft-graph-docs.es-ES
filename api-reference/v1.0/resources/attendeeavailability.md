# <a name="attendeeavailability-resource-type"></a><span data-ttu-id="0fc9f-101">Tipo de recurso attendeeAvailability</span><span class="sxs-lookup"><span data-stu-id="0fc9f-101">attendeeAvailability resource type</span></span>

<span data-ttu-id="0fc9f-102">El tipo y la disponibilidad de un asistente.</span><span class="sxs-lookup"><span data-stu-id="0fc9f-102">The type and availability of an attendee.</span></span>

## <a name="json-representation"></a><span data-ttu-id="0fc9f-103">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0fc9f-103">JSON representation</span></span>

<span data-ttu-id="0fc9f-104">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="0fc9f-104">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.attendeeAvailability"
}-->

```json
{
  "attendee": {"@odata.type": "microsoft.graph.attendeeBase"},
  "availability": "String"
}

```
## <a name="properties"></a><span data-ttu-id="0fc9f-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0fc9f-105">Properties</span></span>
| <span data-ttu-id="0fc9f-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0fc9f-106">Property</span></span>     | <span data-ttu-id="0fc9f-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="0fc9f-107">Type</span></span>   |<span data-ttu-id="0fc9f-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="0fc9f-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0fc9f-109">attendee</span><span class="sxs-lookup"><span data-stu-id="0fc9f-109">attendee</span></span>|[<span data-ttu-id="0fc9f-110">AttendeeBase</span><span class="sxs-lookup"><span data-stu-id="0fc9f-110">AttendeeBase</span></span>](attendeebase.md)|<span data-ttu-id="0fc9f-111">El tipo de asistente, ya sea una persona o un recurso, y en caso de ser una persona, si es obligatorio u opcional.</span><span class="sxs-lookup"><span data-stu-id="0fc9f-111">The type of attendee - whether it's a person or a resource, and whether required or optional if it's a person.</span></span>|
|<span data-ttu-id="0fc9f-112">availability</span><span class="sxs-lookup"><span data-stu-id="0fc9f-112">availability</span></span>|<span data-ttu-id="0fc9f-113">freeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="0fc9f-113">FreeBusyStatus</span></span>| <span data-ttu-id="0fc9f-114">El estado de disponibilidad del asistente.</span><span class="sxs-lookup"><span data-stu-id="0fc9f-114">The availability status of the attendee. Possible values are: , , , , , .</span></span> <span data-ttu-id="0fc9f-115">Los valores posibles son `free`, `tentative`, `busy`, `oof`, `workingElsewhere` y `unknown`.</span><span class="sxs-lookup"><span data-stu-id="0fc9f-115">The possible values are `free`, `tentative`, `busy`, `oof`, `workingElsewhere`, `unknown`, , , , , , or .</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "attendeeAvailability resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
