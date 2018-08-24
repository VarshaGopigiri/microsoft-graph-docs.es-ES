# <a name="reminder-resource-type"></a><span data-ttu-id="f4e54-101">Tipo de recurso reminder</span><span class="sxs-lookup"><span data-stu-id="f4e54-101">reminder resource type</span></span>

<span data-ttu-id="f4e54-102">Un aviso para un [evento](event.md) en un [calendario](calendar.md)de usuario.</span><span class="sxs-lookup"><span data-stu-id="f4e54-102">A reminder for an [event](event.md) in a user [calendar](calendar.md).</span></span>

## <a name="properties"></a><span data-ttu-id="f4e54-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f4e54-103">Properties</span></span>
| <span data-ttu-id="f4e54-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f4e54-104">Property</span></span>     | <span data-ttu-id="f4e54-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="f4e54-105">Type</span></span>   |<span data-ttu-id="f4e54-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4e54-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f4e54-107">changeKey</span><span class="sxs-lookup"><span data-stu-id="f4e54-107">changeKey</span></span>|<span data-ttu-id="f4e54-108">Cadena</span><span class="sxs-lookup"><span data-stu-id="f4e54-108">String</span></span>|<span data-ttu-id="f4e54-p101">Identifica la versión del aviso. Cada vez que cambia el aviso, cambia también **changeKey**. Permite que Exchange aplique los cambios a la versión correcta del objeto.</span><span class="sxs-lookup"><span data-stu-id="f4e54-p101">Identifies the version of the reminder. Every time the reminder is changed, **changeKey** changes as well. This allows Exchange to apply changes to the correct version of the object.</span></span>|
|<span data-ttu-id="f4e54-112">eventEndTime</span><span class="sxs-lookup"><span data-stu-id="f4e54-112">eventEndTime</span></span>|[<span data-ttu-id="f4e54-113">DateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="f4e54-113">DateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="f4e54-114">Fecha, hora y zona horaria en que finaliza el evento.</span><span class="sxs-lookup"><span data-stu-id="f4e54-114">The date, time and time zone that the event ends.</span></span>|
|<span data-ttu-id="f4e54-115">eventId</span><span class="sxs-lookup"><span data-stu-id="f4e54-115">eventId</span></span>|<span data-ttu-id="f4e54-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="f4e54-116">String</span></span>|<span data-ttu-id="f4e54-p102">Identificador único del evento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f4e54-p102">The unique ID of the event. Read only.</span></span>|
|<span data-ttu-id="f4e54-119">eventLocation</span><span class="sxs-lookup"><span data-stu-id="f4e54-119">eventLocation</span></span>|[<span data-ttu-id="f4e54-120">Ubicación</span><span class="sxs-lookup"><span data-stu-id="f4e54-120">Location</span></span>](location.md)|<span data-ttu-id="f4e54-121">Ubicación del evento.</span><span class="sxs-lookup"><span data-stu-id="f4e54-121">The location of the event.</span></span>|
|<span data-ttu-id="f4e54-122">eventStartTime</span><span class="sxs-lookup"><span data-stu-id="f4e54-122">eventStartTime</span></span>|[<span data-ttu-id="f4e54-123">DateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="f4e54-123">DateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="f4e54-124">Fecha, hora y zona horaria en que comienza el evento.</span><span class="sxs-lookup"><span data-stu-id="f4e54-124">The date, time, and time zone that the event starts.</span></span>|
|<span data-ttu-id="f4e54-125">eventSubject</span><span class="sxs-lookup"><span data-stu-id="f4e54-125">eventSubject</span></span>|<span data-ttu-id="f4e54-126">Cadena</span><span class="sxs-lookup"><span data-stu-id="f4e54-126">String</span></span>|<span data-ttu-id="f4e54-127">Texto de la línea de asunto del evento.</span><span class="sxs-lookup"><span data-stu-id="f4e54-127">The text of the event's subject line.</span></span>|
|<span data-ttu-id="f4e54-128">eventWebLink</span><span class="sxs-lookup"><span data-stu-id="f4e54-128">eventWebLink</span></span>|<span data-ttu-id="f4e54-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="f4e54-129">String</span></span>|<span data-ttu-id="f4e54-130">Dirección URL para abrir el evento en Outlook en la web.</span><span class="sxs-lookup"><span data-stu-id="f4e54-130">The URL to open the event in Outlook on the web.</span></span><br/><br/><span data-ttu-id="f4e54-p103">El evento se abrirá en el navegador si está conectado a su buzón mediante Outlook en la web. Se le pedirá que inicie sesión si no la ha iniciado ya en el navegador.</span><span class="sxs-lookup"><span data-stu-id="f4e54-p103">The event will open in the browser if you are logged in to your mailbox via Outlook on the web. You will be prompted to login if you are not already logged in with the browser.</span></span><br/><br/><span data-ttu-id="f4e54-133">Se puede acceder a esta dirección URL desde un iFrame.</span><span class="sxs-lookup"><span data-stu-id="f4e54-133">This URL can be accessed from within an iFrame.</span></span>|
|<span data-ttu-id="f4e54-134">reminderFireTime</span><span class="sxs-lookup"><span data-stu-id="f4e54-134">reminderFireTime</span></span>|[<span data-ttu-id="f4e54-135">DateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="f4e54-135">DateTimeTimeZone</span></span>](datetimetimezone.md)|<span data-ttu-id="f4e54-136">Fecha, hora y zona horaria en que se establece que se produzca el aviso.</span><span class="sxs-lookup"><span data-stu-id="f4e54-136">The date, time, and time zone that the reminder is set to occur.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="f4e54-137">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f4e54-137">JSON representation</span></span>

<span data-ttu-id="f4e54-138">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="f4e54-138">Here is a JSON representation of the resource</span></span>

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