# <a name="meetingtimesuggestion-resource-type"></a><span data-ttu-id="37bda-101">Tipo de recurso meetingTimeSuggestion</span><span class="sxs-lookup"><span data-stu-id="37bda-101">meetingTimeSuggestion resource type</span></span>

<span data-ttu-id="37bda-102">Una sugerencia de reunión que incluye información como la hora de la reunión, posibilidad de asistencia, disponibilidad personal y ubicaciones de reuniones disponibles.</span><span class="sxs-lookup"><span data-stu-id="37bda-102">A meeting suggestion that includes information like meeting time, attendance likelihood, individual availability, and available meeting locations.</span></span>

## <a name="json-representation"></a><span data-ttu-id="37bda-103">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="37bda-103">JSON representation</span></span>

<span data-ttu-id="37bda-104">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="37bda-104">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.meetingTimeSuggestion"
}-->

```json
{
  "attendeeAvailability": [{"@odata.type": "microsoft.graph.attendeeAvailability"}],
  "confidence": 100.0,
  "locations": [{"@odata.type": "microsoft.graph.location"}],
  "meetingTimeSlot": {"@odata.type": "microsoft.graph.timeSlot"},
  "organizerAvailability": "String",
  "suggestionReason": "String"
}

```
## <a name="properties"></a><span data-ttu-id="37bda-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="37bda-105">Properties</span></span>
| <span data-ttu-id="37bda-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="37bda-106">Property</span></span>     | <span data-ttu-id="37bda-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="37bda-107">Type</span></span>   |<span data-ttu-id="37bda-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="37bda-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="37bda-109">attendeeAvailability</span><span class="sxs-lookup"><span data-stu-id="37bda-109">attendeeAvailability</span></span>|<span data-ttu-id="37bda-110">colección [attendeeAvailability](attendeeavailability.md)</span><span class="sxs-lookup"><span data-stu-id="37bda-110">[attendeeAvailability](attendeeavailability.md) collection</span></span>|<span data-ttu-id="37bda-111">Una matriz que muestra el estado de disponibilidad de cada asistente para esta sugerencia de reunión.</span><span class="sxs-lookup"><span data-stu-id="37bda-111">An array that shows the availability status of each attendee for this meeting suggestion.</span></span>|
|<span data-ttu-id="37bda-112">confidence</span><span class="sxs-lookup"><span data-stu-id="37bda-112">confidence</span></span>|<span data-ttu-id="37bda-113">Doble</span><span class="sxs-lookup"><span data-stu-id="37bda-113">Double</span></span>|<span data-ttu-id="37bda-114">Un porcentaje que representa la probabilidad de que asistan todos los convocados.</span><span class="sxs-lookup"><span data-stu-id="37bda-114">A percentage that represents the likelhood of all the attendees attending.</span></span>|
|<span data-ttu-id="37bda-115">locations</span><span class="sxs-lookup"><span data-stu-id="37bda-115">locations</span></span>|<span data-ttu-id="37bda-116">colección [location](location.md)</span><span class="sxs-lookup"><span data-stu-id="37bda-116">[location](location.md) collection</span></span>|<span data-ttu-id="37bda-117">Una matriz que especifica el nombre y la ubicación geográfica de cada ubicación de reunión para esta sugerencia de reunión.</span><span class="sxs-lookup"><span data-stu-id="37bda-117">An array that specifies the name and geographic location of each meeting location for this meeting suggestion.</span></span>|
|<span data-ttu-id="37bda-118">meetingTimeSlot</span><span class="sxs-lookup"><span data-stu-id="37bda-118">meetingTimeSlot</span></span>|[<span data-ttu-id="37bda-119">timeSlot</span><span class="sxs-lookup"><span data-stu-id="37bda-119">timeSlot</span></span>](timeslot.md)|<span data-ttu-id="37bda-120">Un período de tiempo sugerido para la reunión.</span><span class="sxs-lookup"><span data-stu-id="37bda-120">A time period suggested for the meeting.</span></span>|
|<span data-ttu-id="37bda-121">organizerAvailability</span><span class="sxs-lookup"><span data-stu-id="37bda-121">organizerAvailability</span></span>|<span data-ttu-id="37bda-122">freeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="37bda-122">FreeBusyStatus</span></span>| <span data-ttu-id="37bda-123">Disponibilidad del organizador de la reunión para esta sugerencia de reunión.</span><span class="sxs-lookup"><span data-stu-id="37bda-123">Availability of the meeting organizer for this meeting suggestion. Possible values are: , , , , , .</span></span> <span data-ttu-id="37bda-124">Los valores posibles son `free`, `tentative`, `busy`, `oof`, `workingElsewhere` y `unknown`.</span><span class="sxs-lookup"><span data-stu-id="37bda-124">The possible values are `free`, `tentative`, `busy`, `oof`, `workingElsewhere`, `unknown`, , , , , , or .</span></span>|
|<span data-ttu-id="37bda-125">suggestionReason</span><span class="sxs-lookup"><span data-stu-id="37bda-125">suggestionReason</span></span>|<span data-ttu-id="37bda-126">Cadena</span><span class="sxs-lookup"><span data-stu-id="37bda-126">String</span></span>|<span data-ttu-id="37bda-127">Razón para proponer hora de la reunión.</span><span class="sxs-lookup"><span data-stu-id="37bda-127">Reason for suggesting the meeting time.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "meetingTimeSuggestion resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->