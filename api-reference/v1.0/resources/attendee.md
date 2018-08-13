# <a name="attendee-resource-type"></a><span data-ttu-id="582dd-101">Tipo de recurso attendee</span><span class="sxs-lookup"><span data-stu-id="582dd-101">attendee resource type</span></span>

<span data-ttu-id="582dd-102">Asistente a un evento.</span><span class="sxs-lookup"><span data-stu-id="582dd-102">An event attendee.</span></span> <span data-ttu-id="582dd-103">Esto puede ser una persona o un recurso, como una sala de reuniones o equipamiento que se ha configurado como un recurso en el servidor Exchange del espacio empresarial.</span><span class="sxs-lookup"><span data-stu-id="582dd-103">This can be a person or resource such as a meeting room or equipment, that has been set up as a resource on the Exchange server for the tenant.</span></span>

<span data-ttu-id="582dd-104">Derivadas de [attendeeBase](attendeebase.md).</span><span class="sxs-lookup"><span data-stu-id="582dd-104">Derived from [attendeeBase](attendeebase.md).</span></span>

## <a name="properties"></a><span data-ttu-id="582dd-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="582dd-105">Properties</span></span>
| <span data-ttu-id="582dd-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="582dd-106">Property</span></span>     | <span data-ttu-id="582dd-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="582dd-107">Type</span></span>   |<span data-ttu-id="582dd-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="582dd-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="582dd-109">status</span><span class="sxs-lookup"><span data-stu-id="582dd-109">status</span></span>|[<span data-ttu-id="582dd-110">ResponseStatus</span><span class="sxs-lookup"><span data-stu-id="582dd-110">ResponseStatus</span></span>](responsestatus.md)|<span data-ttu-id="582dd-111">Respuesta del asistente (ninguna, aceptada, rechazada, etc.) para el evento y fecha y hora en que se envió la respuesta.</span><span class="sxs-lookup"><span data-stu-id="582dd-111">The attendee's response (none, accepted, declined, etc.) for the event and date-time that the response was sent.</span></span>|
|<span data-ttu-id="582dd-112">type</span><span class="sxs-lookup"><span data-stu-id="582dd-112">type</span></span>|<span data-ttu-id="582dd-113">String</span><span class="sxs-lookup"><span data-stu-id="582dd-113">String</span></span>|<span data-ttu-id="582dd-114">Tipo de asistente: `required`, `optional`, `resource`.</span><span class="sxs-lookup"><span data-stu-id="582dd-114">The attendee type: `required`, `optional`, `resource`.</span></span>|
|<span data-ttu-id="582dd-115">emailAddress</span><span class="sxs-lookup"><span data-stu-id="582dd-115">emailAddress</span></span>|[<span data-ttu-id="582dd-116">emailAddress</span><span class="sxs-lookup"><span data-stu-id="582dd-116">emailAddress</span></span>](emailaddress.md)|<span data-ttu-id="582dd-117">Incluye el nombre y la dirección de SMTP del asistente.</span><span class="sxs-lookup"><span data-stu-id="582dd-117">Includes the name and SMTP address of the attendee.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="582dd-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="582dd-118">JSON representation</span></span>

<span data-ttu-id="582dd-119">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="582dd-119">Here is a JSON representation of the resource</span></span>

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