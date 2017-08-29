# <a name="attendee-resource-type"></a><span data-ttu-id="75dba-101">Tipo de recurso attendee</span><span class="sxs-lookup"><span data-stu-id="75dba-101">attendee resource type</span></span>

<span data-ttu-id="75dba-102">Asistente a un evento.</span><span class="sxs-lookup"><span data-stu-id="75dba-102">An event attendee.</span></span>

<span data-ttu-id="75dba-103">Derivadas de [attachment](attendeebase.md).</span><span class="sxs-lookup"><span data-stu-id="75dba-103">Derived from [attendeeBase](attendeebase.md).</span></span>

## <a name="properties"></a><span data-ttu-id="75dba-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="75dba-104">Properties</span></span>
| <span data-ttu-id="75dba-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="75dba-105">Property</span></span>     | <span data-ttu-id="75dba-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="75dba-106">Type</span></span>   |<span data-ttu-id="75dba-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="75dba-107">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="75dba-108">status</span><span class="sxs-lookup"><span data-stu-id="75dba-108">status</span></span>|[<span data-ttu-id="75dba-109">ResponseStatus</span><span class="sxs-lookup"><span data-stu-id="75dba-109">ResponseStatus</span></span>](responsestatus.md)|<span data-ttu-id="75dba-110">Respuesta del asistente (ninguna, aceptada, rechazada, etc.) para el evento y fecha y hora en que se envió la respuesta.</span><span class="sxs-lookup"><span data-stu-id="75dba-110">The attendee's response (none, accepted, declined, etc.) for the event and date-time that the response was sent.</span></span>|
|<span data-ttu-id="75dba-111">type</span><span class="sxs-lookup"><span data-stu-id="75dba-111">type</span></span>|<span data-ttu-id="75dba-112">String</span><span class="sxs-lookup"><span data-stu-id="75dba-112">String</span></span>|<span data-ttu-id="75dba-113">Tipo de asistente: `Required`, `Optional`, `Resource`.</span><span class="sxs-lookup"><span data-stu-id="75dba-113">The attendee type: `Required`, `Optional`, `Resource`.</span></span>|
|<span data-ttu-id="75dba-114">emailAddress</span><span class="sxs-lookup"><span data-stu-id="75dba-114">emailAddress</span></span>|[<span data-ttu-id="75dba-115">emailAddress</span><span class="sxs-lookup"><span data-stu-id="75dba-115">emailAddress</span></span>](emailAddress.md)|<span data-ttu-id="75dba-116">Incluye el nombre y la dirección de SMTP del asistente.</span><span class="sxs-lookup"><span data-stu-id="75dba-116">Includes the name and SMTP address of the attendee.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="75dba-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="75dba-117">JSON representation</span></span>

<span data-ttu-id="75dba-118">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="75dba-118">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.attendee"
}-->

```json
{
  "status": {"@odata.type": "microsoft.graph.responseStatus"},
  "type": "String",
  "emailAddress": {"@odata.type": "microsoft.graph.emailAddress"}
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "attendee resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->