# <a name="update-event"></a><span data-ttu-id="11574-101">Update event</span><span class="sxs-lookup"><span data-stu-id="11574-101">Update event</span></span>

<span data-ttu-id="11574-102">Actualiza las propiedades del objeto [event](../resources/event.md).</span><span class="sxs-lookup"><span data-stu-id="11574-102">Update the properties of event object.</span></span>
## <a name="permissions"></a><span data-ttu-id="11574-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="11574-103">Permissions</span></span>
<span data-ttu-id="11574-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="11574-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="11574-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="11574-106">Permission type</span></span>      | <span data-ttu-id="11574-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="11574-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="11574-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="11574-108">Delegated (work or school account)</span></span> | <span data-ttu-id="11574-109">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="11574-109">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="11574-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="11574-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="11574-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="11574-111">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="11574-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="11574-112">Application</span></span> | <span data-ttu-id="11574-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="11574-113">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="11574-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="11574-114">HTTP request</span></span>
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
## <a name="request-headers"></a><span data-ttu-id="11574-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="11574-115">Request headers</span></span>
| <span data-ttu-id="11574-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="11574-116">Name</span></span>       | <span data-ttu-id="11574-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="11574-117">Type</span></span> | <span data-ttu-id="11574-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="11574-118">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="11574-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="11574-119">Authorization</span></span>  | <span data-ttu-id="11574-120">cadena</span><span class="sxs-lookup"><span data-stu-id="11574-120">string</span></span>  | <span data-ttu-id="11574-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="11574-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="11574-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="11574-123">Request body</span></span>
<span data-ttu-id="11574-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="11574-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="11574-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="11574-127">Property</span></span>     | <span data-ttu-id="11574-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="11574-128">Type</span></span>   |<span data-ttu-id="11574-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="11574-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="11574-130">attendees</span><span class="sxs-lookup"><span data-stu-id="11574-130">attendees</span></span>|[<span data-ttu-id="11574-131">Asistente</span><span class="sxs-lookup"><span data-stu-id="11574-131">Attendee</span></span>](../resources/attendee.md)|<span data-ttu-id="11574-132">La colección de asistentes del evento.</span><span class="sxs-lookup"><span data-stu-id="11574-132">The collection of attendees for the event.</span></span>|
|<span data-ttu-id="11574-133">body</span><span class="sxs-lookup"><span data-stu-id="11574-133">body</span></span>|[<span data-ttu-id="11574-134">ItemBody</span><span class="sxs-lookup"><span data-stu-id="11574-134">ItemBody</span></span>](../resources/itembody.md)|<span data-ttu-id="11574-135">El cuerpo del mensaje asociado con el evento.</span><span class="sxs-lookup"><span data-stu-id="11574-135">The body of the message associated with the event.</span></span>|
|<span data-ttu-id="11574-136">categories</span><span class="sxs-lookup"><span data-stu-id="11574-136">categories</span></span>|<span data-ttu-id="11574-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="11574-137">String</span></span>|<span data-ttu-id="11574-138">Las categorías asociadas con el evento.</span><span class="sxs-lookup"><span data-stu-id="11574-138">The categories associated with the event.</span></span>|
|<span data-ttu-id="11574-139">end</span><span class="sxs-lookup"><span data-stu-id="11574-139">end</span></span>|[<span data-ttu-id="11574-140">DateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="11574-140">DateTimeTimeZone</span></span>](../resources/datetimetimezone.md)|<span data-ttu-id="11574-141">La fecha y hora en que finaliza el evento.</span><span class="sxs-lookup"><span data-stu-id="11574-141">The date and time that the event ends.</span></span><br/><br/><span data-ttu-id="11574-p104">De manera predeterminada, la hora de finalización está en formato UTC. Puede especificar una zona horaria opcional en EndTimeZone, expresar la hora de finalización en esa zona horaria e incluir una diferencia horaria de UTC. Tenga en cuenta que, si usa EndTimeZone, debe especificar también un valor para StartTimeZone.</span><span class="sxs-lookup"><span data-stu-id="11574-p104">By default, the end time is in UTC. You can specify an optional time zone in EndTimeZone, express the end time in that time zone, and include a time offset from UTC. Note that if you use EndTimeZone, you must specify a value for StartTimeZone as well.</span></span><br/><br/><span data-ttu-id="11574-145">En este ejemplo, se especifica el 25 de febrero de 2015, a las 9:34 p. m. en hora estándar del Pacífico: "2015-02-25T21:34:00-08:00".</span><span class="sxs-lookup"><span data-stu-id="11574-145">This example specifies February 25, 2015, 9:34pm in Pacific Standard Time: "2015-02-25T21:34:00-08:00".</span></span> |
|<span data-ttu-id="11574-146">importance</span><span class="sxs-lookup"><span data-stu-id="11574-146">importance</span></span>|<span data-ttu-id="11574-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="11574-147">String</span></span>|<span data-ttu-id="11574-148">Importancia del evento.</span><span class="sxs-lookup"><span data-stu-id="11574-148">The importance of the event.</span></span> <span data-ttu-id="11574-149">The possible values are: `low`, `normal`, `high`.</span><span class="sxs-lookup"><span data-stu-id="11574-149">The possible values are `low`, `normal`, `high`, , , , , , , , , or .</span></span>|
|<span data-ttu-id="11574-150">isAllDay</span><span class="sxs-lookup"><span data-stu-id="11574-150">isAllDay</span></span>|<span data-ttu-id="11574-151">Booleano</span><span class="sxs-lookup"><span data-stu-id="11574-151">Boolean</span></span>|<span data-ttu-id="11574-152">Se establece en true si el evento dura todo el día.</span><span class="sxs-lookup"><span data-stu-id="11574-152">Set to true if the event lasts all day.</span></span>|
|<span data-ttu-id="11574-153">isReminderOn</span><span class="sxs-lookup"><span data-stu-id="11574-153">isReminderOn</span></span>|<span data-ttu-id="11574-154">Booleano</span><span class="sxs-lookup"><span data-stu-id="11574-154">Boolean</span></span>|<span data-ttu-id="11574-155">Se establece en true si se establece una alerta para recordarle el evento al usuario.</span><span class="sxs-lookup"><span data-stu-id="11574-155">Set to true if an alert is set to remind the user of the event.</span></span>|
|<span data-ttu-id="11574-156">location</span><span class="sxs-lookup"><span data-stu-id="11574-156">location</span></span>|[<span data-ttu-id="11574-157">Ubicación</span><span class="sxs-lookup"><span data-stu-id="11574-157">Location</span></span>](../resources/location.md)|<span data-ttu-id="11574-158">La ubicación del evento.</span><span class="sxs-lookup"><span data-stu-id="11574-158">The location of the event.</span></span>|
|<span data-ttu-id="11574-159">locations</span><span class="sxs-lookup"><span data-stu-id="11574-159">locations</span></span>|<span data-ttu-id="11574-160">Colección [location](../resources/location.md)</span><span class="sxs-lookup"><span data-stu-id="11574-160">[location](../resources/location.md) collection</span></span>|<span data-ttu-id="11574-161">Ubicaciones donde se celebra el evento o en las que se asiste.</span><span class="sxs-lookup"><span data-stu-id="11574-161">The locations where the event is held or attended from.</span></span> <span data-ttu-id="11574-162">Las propiedades **location** y **locations** siempre se corresponden entre sí.</span><span class="sxs-lookup"><span data-stu-id="11574-162">The **location** and **locations** properties always correspond with each other.</span></span> <span data-ttu-id="11574-163">Si se actualiza la propiedad **location**, se eliminarían las ubicaciones anteriores de la colección **locations** y se reemplazarían por el nuevo valor de **location**.</span><span class="sxs-lookup"><span data-stu-id="11574-163">If you update the **location** property, any prior locations in the **locations** collection would be removed and replaced by the new **location** value.</span></span> |
|<span data-ttu-id="11574-164">recurrence</span><span class="sxs-lookup"><span data-stu-id="11574-164">recurrence</span></span>|[<span data-ttu-id="11574-165">PatternedRecurrence</span><span class="sxs-lookup"><span data-stu-id="11574-165">PatternedRecurrence</span></span>](../resources/patternedrecurrence.md)|<span data-ttu-id="11574-166">El patrón de periodicidad del evento.</span><span class="sxs-lookup"><span data-stu-id="11574-166">The recurrence pattern for the event.</span></span>|
|<span data-ttu-id="11574-167">reminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="11574-167">reminderMinutesBeforeStart</span></span>|<span data-ttu-id="11574-168">Int32</span><span class="sxs-lookup"><span data-stu-id="11574-168">Int32</span></span>|<span data-ttu-id="11574-169">El número de minutos antes de la hora de inicio del evento en que se producirá la alerta del recordatorio.</span><span class="sxs-lookup"><span data-stu-id="11574-169">The number of minutes before the event start time that the reminder alert occurs.</span></span>|
|<span data-ttu-id="11574-170">responseRequested</span><span class="sxs-lookup"><span data-stu-id="11574-170">responseRequested</span></span>|<span data-ttu-id="11574-171">Booleano</span><span class="sxs-lookup"><span data-stu-id="11574-171">Boolean</span></span>|<span data-ttu-id="11574-172">Se establece en true si el remitente quiere una respuesta cuando el evento se acepta o rechaza.</span><span class="sxs-lookup"><span data-stu-id="11574-172">Set to true if the sender would like a response when the event is accepted or declined.</span></span>|
|<span data-ttu-id="11574-173">sensitivity</span><span class="sxs-lookup"><span data-stu-id="11574-173">sensitivity</span></span>|<span data-ttu-id="11574-174">Cadena</span><span class="sxs-lookup"><span data-stu-id="11574-174">String</span></span>| <span data-ttu-id="11574-175">Los valores posibles son: `normal`, `personal`, `private` y `confidential`.</span><span class="sxs-lookup"><span data-stu-id="11574-175">The possible values are `normal`, `personal`, `private`, `confidential`, , , , , , , , or .</span></span>|
|<span data-ttu-id="11574-176">showAs</span><span class="sxs-lookup"><span data-stu-id="11574-176">showAs</span></span>|<span data-ttu-id="11574-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="11574-177">String</span></span>|<span data-ttu-id="11574-178">El estado que se mostrará.</span><span class="sxs-lookup"><span data-stu-id="11574-178">The status to show.</span></span> <span data-ttu-id="11574-179">The possible values are: `free`, `tentative`, `busy`, `oof`, `workingElsewhere`, `unknown`.</span><span class="sxs-lookup"><span data-stu-id="11574-179">The possible values are `free`, `tentative`, `busy`, `oof`, `workingElsewhere`, `unknown`, , , , , , or .</span></span>|
|<span data-ttu-id="11574-180">start</span><span class="sxs-lookup"><span data-stu-id="11574-180">start</span></span>|[<span data-ttu-id="11574-181">DateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="11574-181">DateTimeTimeZone</span></span>](../resources/datetimetimezone.md)|<span data-ttu-id="11574-182">La hora de inicio del evento.</span><span class="sxs-lookup"><span data-stu-id="11574-182">The start time of the event.</span></span> <br/><br/><span data-ttu-id="11574-p108">De manera predeterminada, la hora de inicio está en formato UTC. Puede especificar una zona horaria opcional en StartTimeZone, expresar la hora de inicio en esa zona horaria e incluir una diferencia horaria de UTC. Tenga en cuenta que, si usa StartTimeZone, debe especificar también un valor para EndTimeZone.</span><span class="sxs-lookup"><span data-stu-id="11574-p108">By default, the start time is in UTC. You can specify an optional time zone in StartTimeZone, express the start time in that time zone, and include a time offset from UTC. Note that if you use StartTimeZone, you must specify a value for EndTimeZone as well.</span></span><br/><br/><span data-ttu-id="11574-186">En este ejemplo, se especifica el 25 de febrero de 2015, a las 7:34 p. m. en hora estándar del Pacífico: "2015-02-25T19:34:00-08:00".</span><span class="sxs-lookup"><span data-stu-id="11574-186">This example specifies February 25, 2015, 7:34pm in Pacific Standard Time: "2015-02-25T19:34:00-08:00".</span></span>  |
|<span data-ttu-id="11574-187">subject</span><span class="sxs-lookup"><span data-stu-id="11574-187">subject</span></span>|<span data-ttu-id="11574-188">Cadena</span><span class="sxs-lookup"><span data-stu-id="11574-188">String</span></span>|<span data-ttu-id="11574-189">Texto de la línea de asunto del evento.</span><span class="sxs-lookup"><span data-stu-id="11574-189">The text of the event's subject line.</span></span>|

<span data-ttu-id="11574-190">Dado que el recurso **event** admite [extensiones](../../../concepts/extensibility_overview.md), puede utilizar la operación `PATCH` para agregar, actualizar o eliminar sus propios datos específicos de la aplicación en las propiedades personalizadas de una extensión en una instancia **event** existente.</span><span class="sxs-lookup"><span data-stu-id="11574-190">Since the **event** resource supports [extensions](../../../concepts/extensibility_overview.md), you can use the `PATCH` operation to add, update, or delete your own app-specific data in custom properties of an extension in an existing **event** instance.</span></span>  
  
<span data-ttu-id="11574-191">Si el **evento** que se va a actualizar es el evento principal de una serie periódica, contiene varios asistentes, y tiene instancias que se han actualizado por separado, se enviarán múltiples mensajes de correo electrónico de notificación: uno para la serie principal y uno por cada instancia que se haya actualizado.</span><span class="sxs-lookup"><span data-stu-id="11574-191">If the **event** you're updating is the master event of a recurring series, contains multiple attendees, and has instances that have been updated separately, multiple notification emails will be sent out: one for the master series and one per instance that has been updated.</span></span>  

## <a name="response"></a><span data-ttu-id="11574-192">Respuesta</span><span class="sxs-lookup"><span data-stu-id="11574-192">Response</span></span>

<span data-ttu-id="11574-193">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [event](../resources/event.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="11574-193">If successful, this method returns a `200 OK` response code and updated [event](../resources/event.md) object in the response body.</span></span>  

><span data-ttu-id="11574-194">**Nota:** Este método puede devolver una respuesta HTTP 400 Solicitud incorrecta con un código de error de `ErrorOccurrenceCrossingBoundary` y el siguiente mensaje de error: La repetición modificada cruza o se superpone a una repetición adyacente.</span><span class="sxs-lookup"><span data-stu-id="11574-194">**Note:** This method can return an HTTP 400 Bad Request response with an error code of `ErrorOccurrenceCrossingBoundary` and the following error message: Modified occurrence is crossing or overlapping adjacent occurrence.</span></span> <span data-ttu-id="11574-195">Esto indica que la actualización infringe la siguiente restricción de Outlook en las excepciones periódicas: un evento no se puede mover a o antes del día del evento anterior y no se puede mover a o después del día del siguiente evento.</span><span class="sxs-lookup"><span data-stu-id="11574-195">This indicates that the update violates the following Outlook restriction on recurrence exceptions: an occurrence cannot be moved to or before the day of the previous occurrence, and cannot be moved to or after the day of the following occurrence.</span></span>

## <a name="example"></a><span data-ttu-id="11574-196">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="11574-196">Example</span></span>

##### <a name="request"></a><span data-ttu-id="11574-197">Solicitud</span><span class="sxs-lookup"><span data-stu-id="11574-197">Request</span></span>

<span data-ttu-id="11574-198">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="11574-198">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="11574-199">Respuesta</span><span class="sxs-lookup"><span data-stu-id="11574-199">Response</span></span>

<span data-ttu-id="11574-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="11574-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

## <a name="see-also"></a><span data-ttu-id="11574-203">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="11574-203">See also</span></span>

- [<span data-ttu-id="11574-204">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="11574-204">Add custom data to resources using extensions</span></span>](../../../concepts/extensibility_overview.md)
- [<span data-ttu-id="11574-205">Agregar datos personalizados a los usuarios mediante extensiones abiertas</span><span class="sxs-lookup"><span data-stu-id="11574-205">Add custom data to users using open extensions</span></span>](../../../concepts/extensibility_open_users.md)
- [<span data-ttu-id="11574-206">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="11574-206">Add custom data to groups using schema extensions</span></span>](../../../concepts/extensibility_schema_groups.md)



<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update event",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
