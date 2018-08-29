# <a name="attendeebase-resource-type"></a><span data-ttu-id="f0e2d-101">Tipo de recurso attendeeBase</span><span class="sxs-lookup"><span data-stu-id="f0e2d-101">attendeeBase resource type</span></span>

<span data-ttu-id="f0e2d-102">El tipo de asistente.</span><span class="sxs-lookup"><span data-stu-id="f0e2d-102">The type of attendee.</span></span>

<span data-ttu-id="f0e2d-103">Derivado de [destinatario](recipient.md).</span><span class="sxs-lookup"><span data-stu-id="f0e2d-103">Derived from [recipient](recipient.md).</span></span>

## <a name="json-representation"></a><span data-ttu-id="f0e2d-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f0e2d-104">JSON representation</span></span>

<span data-ttu-id="f0e2d-105">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="f0e2d-105">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.recipient",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.attendeeBase"
}-->

```json
{
  "type": "String",
  "emailAddress": {"@odata.type": "microsoft.graph.emailAddress"}
}

```
## <a name="properties"></a><span data-ttu-id="f0e2d-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f0e2d-106">Properties</span></span>
| <span data-ttu-id="f0e2d-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f0e2d-107">Property</span></span>     | <span data-ttu-id="f0e2d-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="f0e2d-108">Type</span></span>   |<span data-ttu-id="f0e2d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f0e2d-109">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f0e2d-110">type</span><span class="sxs-lookup"><span data-stu-id="f0e2d-110">type</span></span>|<span data-ttu-id="f0e2d-111">attendeeType</span><span class="sxs-lookup"><span data-stu-id="f0e2d-111">AttendeeType</span></span>| <span data-ttu-id="f0e2d-112">El tipo de asistente.</span><span class="sxs-lookup"><span data-stu-id="f0e2d-112">The type of attendee.</span></span> <span data-ttu-id="f0e2d-113">Los valores posibles son: `required`, `optional` y `resource`.</span><span class="sxs-lookup"><span data-stu-id="f0e2d-113">The possible values are `required`, `optional`, `resource`, , , , , , , , , or .</span></span> <span data-ttu-id="f0e2d-114">Nota: si el asistente es una persona, [findMeetingTimes](../api/user_findmeetingtimes.md) siempre considera que la persona es del tipo `Required`.</span><span class="sxs-lookup"><span data-stu-id="f0e2d-114">The type of attendee. Possible values are: , , . Currently if the attendee is a person, [findMeetingTimes](../api/user_findmeetingtimes.md) always considers the person is of the `Required` type.</span></span>|
|<span data-ttu-id="f0e2d-115">emailAddress</span><span class="sxs-lookup"><span data-stu-id="f0e2d-115">emailAddress</span></span>|[<span data-ttu-id="f0e2d-116">emailAddress</span><span class="sxs-lookup"><span data-stu-id="f0e2d-116">emailAddress</span></span>](emailAddress.md)|<span data-ttu-id="f0e2d-117">Incluye el nombre y la dirección de SMTP del asistente.</span><span class="sxs-lookup"><span data-stu-id="f0e2d-117">Includes the name and SMTP address of the attendee.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "attendeeBase resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
