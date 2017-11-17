# <a name="reminder-resource-type"></a><span data-ttu-id="561e0-101">Tipo de recurso reminder</span><span class="sxs-lookup"><span data-stu-id="561e0-101">reminder resource type</span></span>



## <a name="properties"></a><span data-ttu-id="561e0-102">Propiedades</span><span class="sxs-lookup"><span data-stu-id="561e0-102">Properties</span></span>
| <span data-ttu-id="561e0-103">Propiedad</span><span class="sxs-lookup"><span data-stu-id="561e0-103">Property</span></span>     | <span data-ttu-id="561e0-104">Tipo</span><span class="sxs-lookup"><span data-stu-id="561e0-104">Type</span></span>   |<span data-ttu-id="561e0-105">Descripción</span><span class="sxs-lookup"><span data-stu-id="561e0-105">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="561e0-106">changeKey</span><span class="sxs-lookup"><span data-stu-id="561e0-106">changeKey</span></span>|<span data-ttu-id="561e0-107">String</span><span class="sxs-lookup"><span data-stu-id="561e0-107">String</span></span>|<span data-ttu-id="561e0-p101">Identifica la versión del aviso. Cada vez que cambia el aviso, cambia también **changeKey**. Permite que Exchange aplique los cambios a la versión correcta del objeto.</span><span class="sxs-lookup"><span data-stu-id="561e0-p101">Identifies the version of the reminder. Every time the reminder is changed, **changeKey** changes as well. This allows Exchange to apply changes to the correct version of the object.</span></span>|
|<span data-ttu-id="561e0-111">eventEndTime</span><span class="sxs-lookup"><span data-stu-id="561e0-111">eventEndTime</span></span>|[<span data-ttu-id="561e0-112">DateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="561e0-112">DateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="561e0-113">Fecha, hora y zona horaria en que finaliza el evento.</span><span class="sxs-lookup"><span data-stu-id="561e0-113">The date, time and time zone that the event ends.</span></span>|
|<span data-ttu-id="561e0-114">eventId</span><span class="sxs-lookup"><span data-stu-id="561e0-114">eventId</span></span>|<span data-ttu-id="561e0-115">String</span><span class="sxs-lookup"><span data-stu-id="561e0-115">String</span></span>|<span data-ttu-id="561e0-p102">Identificador único del evento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="561e0-p102">The unique ID of the event. Read only.</span></span>|
|<span data-ttu-id="561e0-118">eventLocation</span><span class="sxs-lookup"><span data-stu-id="561e0-118">eventLocation</span></span>|[<span data-ttu-id="561e0-119">Location</span><span class="sxs-lookup"><span data-stu-id="561e0-119">Location</span></span>](location.md)|<span data-ttu-id="561e0-120">Ubicación del evento.</span><span class="sxs-lookup"><span data-stu-id="561e0-120">The location of the event.</span></span>|
|<span data-ttu-id="561e0-121">eventStartTime</span><span class="sxs-lookup"><span data-stu-id="561e0-121">eventStartTime</span></span>|[<span data-ttu-id="561e0-122">DateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="561e0-122">DateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="561e0-123">Fecha, hora y zona horaria en que comienza el evento.</span><span class="sxs-lookup"><span data-stu-id="561e0-123">The date, time, and time zone that the event starts.</span></span>|
|<span data-ttu-id="561e0-124">eventSubject</span><span class="sxs-lookup"><span data-stu-id="561e0-124">eventSubject</span></span>|<span data-ttu-id="561e0-125">String</span><span class="sxs-lookup"><span data-stu-id="561e0-125">String</span></span>|<span data-ttu-id="561e0-126">Texto de la línea de asunto del evento.</span><span class="sxs-lookup"><span data-stu-id="561e0-126">The text of the event's subject line.</span></span>|
|<span data-ttu-id="561e0-127">eventWebLink</span><span class="sxs-lookup"><span data-stu-id="561e0-127">eventWebLink</span></span>|<span data-ttu-id="561e0-128">String</span><span class="sxs-lookup"><span data-stu-id="561e0-128">String</span></span>|<span data-ttu-id="561e0-129">Dirección URL para abrir el evento en Outlook en la web.</span><span class="sxs-lookup"><span data-stu-id="561e0-129">The URL to open the event in Outlook on the web.</span></span><br/><br/><span data-ttu-id="561e0-p103">El evento se abrirá en el navegador si está conectado a su buzón mediante Outlook en la web. Se le pedirá que inicie sesión si no la ha iniciado ya en el navegador.</span><span class="sxs-lookup"><span data-stu-id="561e0-p103">The event will open in the browser if you are logged in to your mailbox via Outlook on the web. You will be prompted to login if you are not already logged in with the browser.</span></span><br/><br/><span data-ttu-id="561e0-132">Se puede acceder a esta dirección URL desde un iFrame.</span><span class="sxs-lookup"><span data-stu-id="561e0-132">This URL can be accessed from within an iFrame.</span></span>|
|<span data-ttu-id="561e0-133">reminderFireTime</span><span class="sxs-lookup"><span data-stu-id="561e0-133">reminderFireTime</span></span>|[<span data-ttu-id="561e0-134">DateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="561e0-134">DateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="561e0-135">Fecha, hora y zona horaria en que se establece que se produzca el aviso.</span><span class="sxs-lookup"><span data-stu-id="561e0-135">The date, time, and time zone that the reminder is set to occur.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="561e0-136">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="561e0-136">JSON representation</span></span>

<span data-ttu-id="561e0-137">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="561e0-137">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.reminder"
}-->

```json
{
  "changeKey": "string",
  "eventEndTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "eventId": "string",
  "eventLocation": {"@odata.type": "microsoft.graph.location"},
  "eventStartTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "eventSubject": "string",
  "eventWebLink": "string",
  "reminderFireTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "reminder resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->