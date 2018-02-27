# <a name="update-event"></a><span data-ttu-id="9ac89-101">Actualizar evento</span><span class="sxs-lookup"><span data-stu-id="9ac89-101">Update event</span></span>

<span data-ttu-id="9ac89-102">Actualiza las propiedades del objeto evento.</span><span class="sxs-lookup"><span data-stu-id="9ac89-102">Update the properties of event object.</span></span>
## <a name="permissions"></a><span data-ttu-id="9ac89-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="9ac89-103">Permissions</span></span>
<span data-ttu-id="9ac89-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9ac89-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="9ac89-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9ac89-106">Permission type</span></span>      | <span data-ttu-id="9ac89-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9ac89-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9ac89-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9ac89-108">Delegated (work or school account)</span></span> | <span data-ttu-id="9ac89-109">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9ac89-109">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="9ac89-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9ac89-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9ac89-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9ac89-111">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="9ac89-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9ac89-112">Application</span></span> | <span data-ttu-id="9ac89-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9ac89-113">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="9ac89-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9ac89-114">HTTP request</span></span>
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
## <a name="request-headers"></a><span data-ttu-id="9ac89-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9ac89-115">Request headers</span></span>
| <span data-ttu-id="9ac89-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="9ac89-116">Name</span></span>       | <span data-ttu-id="9ac89-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="9ac89-117">Type</span></span> | <span data-ttu-id="9ac89-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="9ac89-118">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="9ac89-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="9ac89-119">Authorization</span></span>  | <span data-ttu-id="9ac89-120">string</span><span class="sxs-lookup"><span data-stu-id="9ac89-120">string</span></span>  | <span data-ttu-id="9ac89-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9ac89-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="9ac89-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9ac89-123">Request body</span></span>
<span data-ttu-id="9ac89-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="9ac89-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="9ac89-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9ac89-127">Property</span></span>     | <span data-ttu-id="9ac89-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="9ac89-128">Type</span></span>   |<span data-ttu-id="9ac89-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="9ac89-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9ac89-130">attendees</span><span class="sxs-lookup"><span data-stu-id="9ac89-130">attendees</span></span>|[<span data-ttu-id="9ac89-131">Attendee</span><span class="sxs-lookup"><span data-stu-id="9ac89-131">Attendee</span></span>](../resources/attendee.md)|<span data-ttu-id="9ac89-132">La colección de asistentes del evento.</span><span class="sxs-lookup"><span data-stu-id="9ac89-132">The collection of attendees for the event.</span></span>|
|<span data-ttu-id="9ac89-133">body</span><span class="sxs-lookup"><span data-stu-id="9ac89-133">body</span></span>|[<span data-ttu-id="9ac89-134">ItemBody</span><span class="sxs-lookup"><span data-stu-id="9ac89-134">ItemBody</span></span>](../resources/itembody.md)|<span data-ttu-id="9ac89-135">El cuerpo del mensaje asociado con el evento.</span><span class="sxs-lookup"><span data-stu-id="9ac89-135">The body of the message associated with the event.</span></span>|
|<span data-ttu-id="9ac89-136">categories</span><span class="sxs-lookup"><span data-stu-id="9ac89-136">categories</span></span>|<span data-ttu-id="9ac89-137">String</span><span class="sxs-lookup"><span data-stu-id="9ac89-137">String</span></span>|<span data-ttu-id="9ac89-138">Las categorías asociadas con el evento.</span><span class="sxs-lookup"><span data-stu-id="9ac89-138">The categories associated with the event.</span></span>|
|<span data-ttu-id="9ac89-139">end</span><span class="sxs-lookup"><span data-stu-id="9ac89-139">end</span></span>|[<span data-ttu-id="9ac89-140">DateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="9ac89-140">DateTimeTimeZone</span></span>](../resources/datetimetimezone.md)|<span data-ttu-id="9ac89-141">La fecha y hora en que finaliza el evento.</span><span class="sxs-lookup"><span data-stu-id="9ac89-141">The date and time that the event ends.</span></span><br/><br/><span data-ttu-id="9ac89-p104">De manera predeterminada, la hora de finalización está en formato UTC. Puede especificar una zona horaria opcional en EndTimeZone, expresar la hora de finalización en esa zona horaria e incluir una diferencia horaria de UTC. Tenga en cuenta que, si usa EndTimeZone, debe especificar también un valor para StartTimeZone.</span><span class="sxs-lookup"><span data-stu-id="9ac89-p104">By default, the end time is in UTC. You can specify an optional time zone in EndTimeZone, express the end time in that time zone, and include a time offset from UTC. Note that if you use EndTimeZone, you must specify a value for StartTimeZone as well.</span></span><br/><br/><span data-ttu-id="9ac89-145">En este ejemplo, se especifica el 25 de febrero de 2015, a las 9:34 p. m. en hora estándar del Pacífico: "2015-02-25T21:34:00-08:00".</span><span class="sxs-lookup"><span data-stu-id="9ac89-145">This example specifies February 25, 2015, 9:34pm in Pacific Standard Time: "2015-02-25T21:34:00-08:00".</span></span> |
|<span data-ttu-id="9ac89-146">importance</span><span class="sxs-lookup"><span data-stu-id="9ac89-146">importance</span></span>|<span data-ttu-id="9ac89-147">String</span><span class="sxs-lookup"><span data-stu-id="9ac89-147">String</span></span>|<span data-ttu-id="9ac89-148">Importancia del evento.</span><span class="sxs-lookup"><span data-stu-id="9ac89-148">The importance of the message: , , .</span></span> <span data-ttu-id="9ac89-149">Los valores posibles son: `Low`, `Normal` y `High`.</span><span class="sxs-lookup"><span data-stu-id="9ac89-149">Possible values are: `Low`, `Normal`, `High`.</span></span>|
|<span data-ttu-id="9ac89-150">isAllDay</span><span class="sxs-lookup"><span data-stu-id="9ac89-150">isAllDay</span></span>|<span data-ttu-id="9ac89-151">Booleano</span><span class="sxs-lookup"><span data-stu-id="9ac89-151">Boolean</span></span>|<span data-ttu-id="9ac89-152">Se establece en true si el evento dura todo el día.</span><span class="sxs-lookup"><span data-stu-id="9ac89-152">Set to true if the event lasts all day.</span></span>|
|<span data-ttu-id="9ac89-153">isReminderOn</span><span class="sxs-lookup"><span data-stu-id="9ac89-153">isReminderOn</span></span>|<span data-ttu-id="9ac89-154">Booleano</span><span class="sxs-lookup"><span data-stu-id="9ac89-154">Boolean</span></span>|<span data-ttu-id="9ac89-155">Se establece en true si se establece una alerta para recordarle el evento al usuario.</span><span class="sxs-lookup"><span data-stu-id="9ac89-155">Set to true if an alert is set to remind the user of the event.</span></span>|
|<span data-ttu-id="9ac89-156">location</span><span class="sxs-lookup"><span data-stu-id="9ac89-156">location</span></span>|[<span data-ttu-id="9ac89-157">Location</span><span class="sxs-lookup"><span data-stu-id="9ac89-157">Location</span></span>](../resources/location.md)|<span data-ttu-id="9ac89-158">La ubicación del evento.</span><span class="sxs-lookup"><span data-stu-id="9ac89-158">The location of the event.</span></span>|
|<span data-ttu-id="9ac89-159">onlineMeetingUrl</span><span class="sxs-lookup"><span data-stu-id="9ac89-159">onlineMeetingUrl</span></span>|<span data-ttu-id="9ac89-160">String</span><span class="sxs-lookup"><span data-stu-id="9ac89-160">String</span></span>|<span data-ttu-id="9ac89-161">Una dirección URL para una reunión en línea.</span><span class="sxs-lookup"><span data-stu-id="9ac89-161">A URL for an online meeting.</span></span>|
|<span data-ttu-id="9ac89-162">recurrence</span><span class="sxs-lookup"><span data-stu-id="9ac89-162">recurrence</span></span>|[<span data-ttu-id="9ac89-163">PatternedRecurrence</span><span class="sxs-lookup"><span data-stu-id="9ac89-163">PatternedRecurrence</span></span>](../resources/patternedrecurrence.md)|<span data-ttu-id="9ac89-164">El patrón de periodicidad del evento.</span><span class="sxs-lookup"><span data-stu-id="9ac89-164">The recurrence pattern for the event.</span></span>|
|<span data-ttu-id="9ac89-165">reminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="9ac89-165">reminderMinutesBeforeStart</span></span>|<span data-ttu-id="9ac89-166">Int32</span><span class="sxs-lookup"><span data-stu-id="9ac89-166">Int32</span></span>|<span data-ttu-id="9ac89-167">El número de minutos antes de la hora de inicio del evento en que se producirá la alerta del recordatorio.</span><span class="sxs-lookup"><span data-stu-id="9ac89-167">The number of minutes before the event start time that the reminder alert occurs.</span></span>|
|<span data-ttu-id="9ac89-168">responseRequested</span><span class="sxs-lookup"><span data-stu-id="9ac89-168">responseRequested</span></span>|<span data-ttu-id="9ac89-169">Booleano</span><span class="sxs-lookup"><span data-stu-id="9ac89-169">Boolean</span></span>|<span data-ttu-id="9ac89-170">Se establece en true si el remitente quiere una respuesta cuando el evento se acepta o rechaza.</span><span class="sxs-lookup"><span data-stu-id="9ac89-170">Set to true if the sender would like a response when the event is accepted or declined.</span></span>|
|<span data-ttu-id="9ac89-171">sensitivity</span><span class="sxs-lookup"><span data-stu-id="9ac89-171">sensitivity</span></span>|<span data-ttu-id="9ac89-172">String</span><span class="sxs-lookup"><span data-stu-id="9ac89-172">String</span></span>| <span data-ttu-id="9ac89-173">Los valores posibles son: `Normal`, `Personal`, `Private`, `Confidential`.</span><span class="sxs-lookup"><span data-stu-id="9ac89-173">Possible values are: `Normal`, `Personal`, `Private`, `Confidential`.</span></span>|
|<span data-ttu-id="9ac89-174">showAs</span><span class="sxs-lookup"><span data-stu-id="9ac89-174">showAs</span></span>|<span data-ttu-id="9ac89-175">String</span><span class="sxs-lookup"><span data-stu-id="9ac89-175">String</span></span>|<span data-ttu-id="9ac89-176">El estado que se mostrará.</span><span class="sxs-lookup"><span data-stu-id="9ac89-176">The status to show.</span></span> <span data-ttu-id="9ac89-177">Los valores posibles son: `Free`, `Tentative`, `Busy`, `Oof`, `WorkingElsewhere` y `Unknown`.</span><span class="sxs-lookup"><span data-stu-id="9ac89-177">Possible values are: `Free`, `Tentative`, `Busy`, `Oof`, `WorkingElsewhere`, `Unknown`.</span></span>|
|<span data-ttu-id="9ac89-178">start</span><span class="sxs-lookup"><span data-stu-id="9ac89-178">start</span></span>|[<span data-ttu-id="9ac89-179">DateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="9ac89-179">DateTimeTimeZone</span></span>](../resources/datetimetimezone.md)|<span data-ttu-id="9ac89-180">La hora de inicio del evento.</span><span class="sxs-lookup"><span data-stu-id="9ac89-180">The start time of the event.</span></span> <br/><br/><span data-ttu-id="9ac89-p107">De manera predeterminada, la hora de inicio está en formato UTC. Puede especificar una zona horaria opcional en StartTimeZone, expresar la hora de inicio en esa zona horaria e incluir una diferencia horaria de UTC. Tenga en cuenta que, si usa StartTimeZone, debe especificar también un valor para EndTimeZone.</span><span class="sxs-lookup"><span data-stu-id="9ac89-p107">By default, the start time is in UTC. You can specify an optional time zone in StartTimeZone, express the start time in that time zone, and include a time offset from UTC. Note that if you use StartTimeZone, you must specify a value for EndTimeZone as well.</span></span><br/><br/><span data-ttu-id="9ac89-184">En este ejemplo, se especifica el 25 de febrero de 2015, a las 7:34 p. m. en hora estándar del Pacífico: "2015-02-25T19:34:00-08:00".</span><span class="sxs-lookup"><span data-stu-id="9ac89-184">This example specifies February 25, 2015, 7:34pm in Pacific Standard Time: "2015-02-25T19:34:00-08:00".</span></span>  |
|<span data-ttu-id="9ac89-185">subject</span><span class="sxs-lookup"><span data-stu-id="9ac89-185">subject</span></span>|<span data-ttu-id="9ac89-186">String</span><span class="sxs-lookup"><span data-stu-id="9ac89-186">String</span></span>|<span data-ttu-id="9ac89-187">El texto de la línea de asunto del evento.</span><span class="sxs-lookup"><span data-stu-id="9ac89-187">The text of the event's subject line.</span></span>|

<span data-ttu-id="9ac89-188">Dado que el recurso **event** admite [extensiones](../../../concepts/extensibility_overview.md), puede utilizar la operación `PATCH` para agregar, actualizar o eliminar sus propios datos específicos de la aplicación en las propiedades personalizadas de una extensión en una instancia **event** existente.</span><span class="sxs-lookup"><span data-stu-id="9ac89-188">Since the **event** resource supports [extensions](../../../concepts/extensibility_overview.md), you can use the `PATCH` operation to add, update, or delete your own app-specific data in custom properties of an extension in an existing **event** instance.</span></span>

## <a name="response"></a><span data-ttu-id="9ac89-189">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9ac89-189">Response</span></span>

<span data-ttu-id="9ac89-190">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [event](../resources/event.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9ac89-190">If successful, this method returns a `200 OK` response code and updated [event](../resources/event.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9ac89-191">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9ac89-191">Example</span></span>

##### <a name="request"></a><span data-ttu-id="9ac89-192">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9ac89-192">Request</span></span>

<span data-ttu-id="9ac89-193">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9ac89-193">Here is an example of the request.</span></span>
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
  "recurrence": null,
  "iCalUId": "iCalUId-value",
  "reminderMinutesBeforeStart": 99,
  "isReminderOn": true
}
```

##### <a name="response"></a><span data-ttu-id="9ac89-194">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9ac89-194">Response</span></span>

<span data-ttu-id="9ac89-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9ac89-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "recurrence": null,  
  "iCalUId": "iCalUId-value",
  "reminderMinutesBeforeStart": 99,
  "isReminderOn": true
}
```

## <a name="see-also"></a><span data-ttu-id="9ac89-198">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="9ac89-198">See also</span></span>

- [<span data-ttu-id="9ac89-199">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="9ac89-199">Add custom data to resources using extensions</span></span>](../../../concepts/extensibility_overview.md)
- [<span data-ttu-id="9ac89-200">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="9ac89-200">Add custom data to users using open extensions (preview)</span></span>](../../../concepts/extensibility_open_users.md)
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
