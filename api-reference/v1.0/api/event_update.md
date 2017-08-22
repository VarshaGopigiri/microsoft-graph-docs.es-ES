# <a name="update-event"></a><span data-ttu-id="8efbb-101">Actualizar evento</span><span class="sxs-lookup"><span data-stu-id="8efbb-101">Update event</span></span>

<span data-ttu-id="8efbb-102">Actualice las propiedades del objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="8efbb-102">Update the properties of event object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8efbb-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8efbb-103">Prerequisites</span></span>
<span data-ttu-id="8efbb-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Calendars.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="8efbb-104">One of the following **scopes** is required to execute this API: *Calendars.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="8efbb-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8efbb-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/events/{id}
PATCH /users/{id | userPrincipalName}/events/{id}
PATCH /groups/{id}/events/{id}

PATCH /me/calendar/events/{id}
PATCH /users/{id | userPrincipalName}/calendar/events/{id}
PATCH /groups/{id}/calendar/events/{id}

PATCH /me/calendars/{id}/events/{id}
PATCH /users/{id | userPrincipalName}/calendars/{id}/events/{id}

PATCH /me/calendargroup/calendars/{id}/events/{id}
PATCH /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}

PATCH /me/calendargroups/{id}/calendars/{id}/events/{id}
PATCH /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}
```
## <a name="request-headers"></a><span data-ttu-id="8efbb-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8efbb-106">Request headers</span></span>
| <span data-ttu-id="8efbb-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="8efbb-107">Name</span></span>       | <span data-ttu-id="8efbb-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="8efbb-108">Type</span></span> | <span data-ttu-id="8efbb-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="8efbb-109">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="8efbb-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="8efbb-110">Authorization</span></span>  | <span data-ttu-id="8efbb-111">string</span><span class="sxs-lookup"><span data-stu-id="8efbb-111">string</span></span>  | <span data-ttu-id="8efbb-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8efbb-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="8efbb-114">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8efbb-114">Request body</span></span>
<span data-ttu-id="8efbb-p102">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="8efbb-p102">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="8efbb-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8efbb-118">Property</span></span>     | <span data-ttu-id="8efbb-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="8efbb-119">Type</span></span>   |<span data-ttu-id="8efbb-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="8efbb-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8efbb-121">attendees</span><span class="sxs-lookup"><span data-stu-id="8efbb-121">attendees</span></span>|[<span data-ttu-id="8efbb-122">Attendee</span><span class="sxs-lookup"><span data-stu-id="8efbb-122">Attendee</span></span>](../resources/attendee.md)|<span data-ttu-id="8efbb-123">La colección de asistentes del evento.</span><span class="sxs-lookup"><span data-stu-id="8efbb-123">The collection of attendees for the event.</span></span>|
|<span data-ttu-id="8efbb-124">body</span><span class="sxs-lookup"><span data-stu-id="8efbb-124">body</span></span>|[<span data-ttu-id="8efbb-125">ItemBody</span><span class="sxs-lookup"><span data-stu-id="8efbb-125">itemBody</span></span>](../resources/itembody.md)|<span data-ttu-id="8efbb-126">El cuerpo del mensaje asociado con el evento.</span><span class="sxs-lookup"><span data-stu-id="8efbb-126">The body of the message associated with the event.</span></span>|
|<span data-ttu-id="8efbb-127">categories</span><span class="sxs-lookup"><span data-stu-id="8efbb-127">categories</span></span>|<span data-ttu-id="8efbb-128">String</span><span class="sxs-lookup"><span data-stu-id="8efbb-128">String</span></span>|<span data-ttu-id="8efbb-129">Las categorías asociadas con el evento.</span><span class="sxs-lookup"><span data-stu-id="8efbb-129">The categories associated with the event.</span></span>|
|<span data-ttu-id="8efbb-130">end</span><span class="sxs-lookup"><span data-stu-id="8efbb-130">end</span></span>|[<span data-ttu-id="8efbb-131">DateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="8efbb-131">DateTimeTimeZone</span></span>](../resources/datetimetimezone.md)|<span data-ttu-id="8efbb-132">La fecha y hora en que finaliza el evento.</span><span class="sxs-lookup"><span data-stu-id="8efbb-132">The date and time that the event ends.</span></span><br/><br/><span data-ttu-id="8efbb-p103">De manera predeterminada, la hora de finalización está en formato UTC. Puede especificar una zona horaria opcional en EndTimeZone, expresar la hora de finalización en esa zona horaria e incluir una diferencia horaria de UTC. Tenga en cuenta que, si usa EndTimeZone, debe especificar también un valor para StartTimeZone.</span><span class="sxs-lookup"><span data-stu-id="8efbb-p103">By default, the end time is in UTC. You can specify an optional time zone in EndTimeZone, express the end time in that time zone, and include a time offset from UTC. Note that if you use EndTimeZone, you must specify a value for StartTimeZone as well.</span></span><br/><br/><span data-ttu-id="8efbb-136">En este ejemplo, se especifica el 25 de febrero de 2015, a las 9:34 p. m. en hora estándar del Pacífico: "2015-02-25T21:34:00-08:00".</span><span class="sxs-lookup"><span data-stu-id="8efbb-136">This example specifies February 25, 2015, 9:34pm in Pacific Standard Time: "2015-02-25T21:34:00-08:00".</span></span> |
|<span data-ttu-id="8efbb-137">importance</span><span class="sxs-lookup"><span data-stu-id="8efbb-137">importance</span></span>|<span data-ttu-id="8efbb-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="8efbb-138">String</span></span>|<span data-ttu-id="8efbb-p104">La importancia del evento: Baja = 0, Normal = 1, Alta = 2. Los valores posibles son: `Low`, `Normal` y `High`.</span><span class="sxs-lookup"><span data-stu-id="8efbb-p104">The importance of the event: Low = 0, Normal = 1, High = 2. Possible values are: `Low`, `Normal`, `High`.</span></span>|
|<span data-ttu-id="8efbb-141">isAllDay</span><span class="sxs-lookup"><span data-stu-id="8efbb-141">isAllDay</span></span>|<span data-ttu-id="8efbb-142">Booleano</span><span class="sxs-lookup"><span data-stu-id="8efbb-142">Boolean</span></span>|<span data-ttu-id="8efbb-143">Se establece en true si el evento dura todo el día.</span><span class="sxs-lookup"><span data-stu-id="8efbb-143">Set to true if the event lasts all day.</span></span>|
|<span data-ttu-id="8efbb-144">isReminderOn</span><span class="sxs-lookup"><span data-stu-id="8efbb-144">isReminderOn</span></span>|<span data-ttu-id="8efbb-145">Booleano</span><span class="sxs-lookup"><span data-stu-id="8efbb-145">Boolean</span></span>|<span data-ttu-id="8efbb-146">Se establece en true si se establece una alerta para recordarle el evento al usuario.</span><span class="sxs-lookup"><span data-stu-id="8efbb-146">Set to true if an alert is set to remind the user of the event.</span></span>|
|<span data-ttu-id="8efbb-147">location</span><span class="sxs-lookup"><span data-stu-id="8efbb-147">location</span></span>|[<span data-ttu-id="8efbb-148">Location</span><span class="sxs-lookup"><span data-stu-id="8efbb-148">Location</span></span>](../resources/location.md)|<span data-ttu-id="8efbb-149">La ubicación del evento.</span><span class="sxs-lookup"><span data-stu-id="8efbb-149">The location of the event.</span></span>|
|<span data-ttu-id="8efbb-150">onlineMeetingUrl</span><span class="sxs-lookup"><span data-stu-id="8efbb-150">onlineMeetingUrl</span></span>|<span data-ttu-id="8efbb-151">String</span><span class="sxs-lookup"><span data-stu-id="8efbb-151">String</span></span>|<span data-ttu-id="8efbb-152">Una dirección URL para una reunión en línea.</span><span class="sxs-lookup"><span data-stu-id="8efbb-152">A URL for an online meeting.</span></span>|
|<span data-ttu-id="8efbb-153">recurrence</span><span class="sxs-lookup"><span data-stu-id="8efbb-153">recurrence</span></span>|[<span data-ttu-id="8efbb-154">PatternedRecurrence</span><span class="sxs-lookup"><span data-stu-id="8efbb-154">PatternedRecurrence</span></span>](../resources/patternedrecurrence.md)|<span data-ttu-id="8efbb-155">El patrón de periodicidad del evento.</span><span class="sxs-lookup"><span data-stu-id="8efbb-155">The recurrence patern for the event.</span></span>|
|<span data-ttu-id="8efbb-156">reminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="8efbb-156">reminderMinutesBeforeStart</span></span>|<span data-ttu-id="8efbb-157">Int32</span><span class="sxs-lookup"><span data-stu-id="8efbb-157">Int32</span></span>|<span data-ttu-id="8efbb-158">El número de minutos antes de la hora de inicio del evento en que se producirá la alerta del recordatorio.</span><span class="sxs-lookup"><span data-stu-id="8efbb-158">The number of minutes before the event start time that the reminder alert occurs.</span></span>|
|<span data-ttu-id="8efbb-159">responseRequested</span><span class="sxs-lookup"><span data-stu-id="8efbb-159">responseRequested</span></span>|<span data-ttu-id="8efbb-160">Booleano</span><span class="sxs-lookup"><span data-stu-id="8efbb-160">Boolean</span></span>|<span data-ttu-id="8efbb-161">Se establece en true si el remitente quiere una respuesta cuando el evento se acepta o rechaza.</span><span class="sxs-lookup"><span data-stu-id="8efbb-161">Set to true if the sender would like a response when the event is accepted or declined.</span></span>|
|<span data-ttu-id="8efbb-162">sensitivity</span><span class="sxs-lookup"><span data-stu-id="8efbb-162">sensitivity</span></span>|<span data-ttu-id="8efbb-163">String</span><span class="sxs-lookup"><span data-stu-id="8efbb-163">String</span></span>| <span data-ttu-id="8efbb-164">Los valores posibles son: `Normal`, `Personal`, `Private`, `Confidential`.</span><span class="sxs-lookup"><span data-stu-id="8efbb-164">Possible values are: `Normal`, `Personal`, `Private`, `Confidential`.</span></span>|
|<span data-ttu-id="8efbb-165">showAs</span><span class="sxs-lookup"><span data-stu-id="8efbb-165">showAs</span></span>|<span data-ttu-id="8efbb-166">String</span><span class="sxs-lookup"><span data-stu-id="8efbb-166">String</span></span>|<span data-ttu-id="8efbb-p105">El estado que se mostrará: Free = 0, Tentative = 1, Busy = 2, Oof = 3, WorkingElsewhere = 4, Unknown = -1. Los valores posibles son: `Free`, `Tentative`, `Busy`, `Oof`, `WorkingElsewhere` y `Unknown`.</span><span class="sxs-lookup"><span data-stu-id="8efbb-p105">The status to show: Free = 0, Tentative = 1, Busy = 2, Oof = 3, WorkingElsewhere = 4, Unknown = -1. Possible values are: `Free`, `Tentative`, `Busy`, `Oof`, `WorkingElsewhere`, `Unknown`.</span></span>|
|<span data-ttu-id="8efbb-169">inicio</span><span class="sxs-lookup"><span data-stu-id="8efbb-169">start</span></span>|[<span data-ttu-id="8efbb-170">DateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="8efbb-170">DateTimeTimeZone</span></span>](../resources/datetimetimezone.md)|<span data-ttu-id="8efbb-171">La hora de inicio del evento.</span><span class="sxs-lookup"><span data-stu-id="8efbb-171">The start time of the event.</span></span> <br/><br/><span data-ttu-id="8efbb-p106">De manera predeterminada, la hora de inicio está en formato UTC. Puede especificar una zona horaria opcional en StartTimeZone, expresar la hora de inicio en esa zona horaria e incluir una diferencia horaria de UTC. Tenga en cuenta que, si usa StartTimeZone, debe especificar también un valor para EndTimeZone.</span><span class="sxs-lookup"><span data-stu-id="8efbb-p106">By default, the start time is in UTC. You can specify an optional time zone in StartTimeZone, express the start time in that time zone, and include a time offset from UTC. Note that if you use StartTimeZone, you must specify a value for EndTimeZone as well.</span></span><br/><br/><span data-ttu-id="8efbb-175">En este ejemplo, se especifica el 25 de febrero de 2015, a las 7:34 p. m. en hora estándar del Pacífico: "2015-02-25T19:34:00-08:00".</span><span class="sxs-lookup"><span data-stu-id="8efbb-175">This example specifies February 25, 2015, 7:34pm in Pacific Standard Time: "2015-02-25T19:34:00-08:00".</span></span>  |
|<span data-ttu-id="8efbb-176">subject</span><span class="sxs-lookup"><span data-stu-id="8efbb-176">subject</span></span>|<span data-ttu-id="8efbb-177">String</span><span class="sxs-lookup"><span data-stu-id="8efbb-177">String</span></span>|<span data-ttu-id="8efbb-178">El texto de la línea de asunto del evento.</span><span class="sxs-lookup"><span data-stu-id="8efbb-178">The text of the event's subject line.</span></span>|

<span data-ttu-id="8efbb-179">Dado que el recurso **event** admite [extensiones](../../../concepts/extensibility_overview.md), puede utilizar la operación `PATCH` para agregar, actualizar o eliminar sus propios datos específicos de la aplicación en las propiedades personalizadas de una extensión en una instancia **event** existente.</span><span class="sxs-lookup"><span data-stu-id="8efbb-179">Since the **event** resource supports [extensions](../../../concepts/extensibility_overview.md), you can use the `PATCH` operation to add, update, or delete your own app-specific data in custom properties of an extension in an existing **event** instance.</span></span>

## <a name="response"></a><span data-ttu-id="8efbb-180">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8efbb-180">Response</span></span>

<span data-ttu-id="8efbb-181">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [event](../resources/event.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8efbb-181">If successful, this method returns a `200 OK` response code and updated [event](../resources/event.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="8efbb-182">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8efbb-182">Example</span></span>
##### <a name="request"></a><span data-ttu-id="8efbb-183">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8efbb-183">Request</span></span>
<span data-ttu-id="8efbb-184">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8efbb-184">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_event"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/events/{id}
Content-type: application/json
Content-length: 285

{
  "originalStartTimeZone": "originalStartTimeZone-value",
  "originalEndTimeZone": "originalEndTimeZone-value",
  "responseStatus": {
    "response": "",
    "time": "datetime-value"
  },
  "iCalUId": "iCalUId-value",
  "reminderMinutesBeforeStart": 99,
  "isReminderOn": true
}
```
##### <a name="response"></a><span data-ttu-id="8efbb-185">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8efbb-185">Response</span></span>
<span data-ttu-id="8efbb-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8efbb-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.event"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 285

{
  "originalStartTimeZone": "originalStartTimeZone-value",
  "originalEndTimeZone": "originalEndTimeZone-value",
  "responseStatus": {
    "response": "",
    "time": "datetime-value"
  },
  "iCalUId": "iCalUId-value",
  "reminderMinutesBeforeStart": 99,
  "isReminderOn": true
}
```

## <a name="see-also"></a><span data-ttu-id="8efbb-189">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="8efbb-189">See also</span></span>

- [<span data-ttu-id="8efbb-190">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="8efbb-190">Add custom data to resources using extensions</span></span>](../../../concepts/extensibility_overview.md)
- [<span data-ttu-id="8efbb-191">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="8efbb-191">Add custom data to users using open extensions (preview)</span></span>](../../../concepts/extensibility_open_users.md)
<!--
- [Add custom data to groups using schema extensions (preview)](../../../concepts/extensibility_schema_groups.md)
-->


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update event",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
