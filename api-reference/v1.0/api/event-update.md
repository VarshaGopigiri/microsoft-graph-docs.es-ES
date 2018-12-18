---
title: Actualizar evento
description: Actualizar las propiedades del objeto event.
author: angelgolfer-ms
ms.openlocfilehash: 1ea0ae20a88159f9d96a23028fa731ea04d6817b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27312449"
---
# <a name="update-event"></a><span data-ttu-id="1f5ce-103">Actualizar evento</span><span class="sxs-lookup"><span data-stu-id="1f5ce-103">Update event</span></span>

<span data-ttu-id="1f5ce-104">Actualizar las propiedades del objeto [event](../resources/event.md) .</span><span class="sxs-lookup"><span data-stu-id="1f5ce-104">Update the properties of the [event](../resources/event.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="1f5ce-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="1f5ce-105">Permissions</span></span>
<span data-ttu-id="1f5ce-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1f5ce-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1f5ce-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1f5ce-108">Permission type</span></span>      | <span data-ttu-id="1f5ce-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1f5ce-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1f5ce-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1f5ce-110">Delegated (work or school account)</span></span> | <span data-ttu-id="1f5ce-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1f5ce-111">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="1f5ce-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1f5ce-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1f5ce-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1f5ce-113">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="1f5ce-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1f5ce-114">Application</span></span> | <span data-ttu-id="1f5ce-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1f5ce-115">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="1f5ce-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1f5ce-116">HTTP request</span></span>
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
## <a name="request-headers"></a><span data-ttu-id="1f5ce-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1f5ce-117">Request headers</span></span>
| <span data-ttu-id="1f5ce-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="1f5ce-118">Name</span></span>       | <span data-ttu-id="1f5ce-119">Type</span><span class="sxs-lookup"><span data-stu-id="1f5ce-119">Type</span></span> | <span data-ttu-id="1f5ce-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f5ce-120">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="1f5ce-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="1f5ce-121">Authorization</span></span>  | <span data-ttu-id="1f5ce-122">string</span><span class="sxs-lookup"><span data-stu-id="1f5ce-122">string</span></span>  | <span data-ttu-id="1f5ce-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1f5ce-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="1f5ce-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1f5ce-125">Request body</span></span>
<span data-ttu-id="1f5ce-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="1f5ce-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="1f5ce-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1f5ce-129">Property</span></span>     | <span data-ttu-id="1f5ce-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="1f5ce-130">Type</span></span>   |<span data-ttu-id="1f5ce-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f5ce-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1f5ce-132">attendees</span><span class="sxs-lookup"><span data-stu-id="1f5ce-132">attendees</span></span>|[<span data-ttu-id="1f5ce-133">Attendee</span><span class="sxs-lookup"><span data-stu-id="1f5ce-133">Attendee</span></span>](../resources/attendee.md)|<span data-ttu-id="1f5ce-134">La colección de asistentes del evento.</span><span class="sxs-lookup"><span data-stu-id="1f5ce-134">The collection of attendees for the event.</span></span>|
|<span data-ttu-id="1f5ce-135">body</span><span class="sxs-lookup"><span data-stu-id="1f5ce-135">body</span></span>|[<span data-ttu-id="1f5ce-136">ItemBody</span><span class="sxs-lookup"><span data-stu-id="1f5ce-136">ItemBody</span></span>](../resources/itembody.md)|<span data-ttu-id="1f5ce-137">El cuerpo del mensaje asociado con el evento.</span><span class="sxs-lookup"><span data-stu-id="1f5ce-137">The body of the message associated with the event.</span></span>|
|<span data-ttu-id="1f5ce-138">categories</span><span class="sxs-lookup"><span data-stu-id="1f5ce-138">categories</span></span>|<span data-ttu-id="1f5ce-139">String</span><span class="sxs-lookup"><span data-stu-id="1f5ce-139">String</span></span>|<span data-ttu-id="1f5ce-140">Las categorías asociadas con el evento.</span><span class="sxs-lookup"><span data-stu-id="1f5ce-140">The categories associated with the event.</span></span>|
|<span data-ttu-id="1f5ce-141">end</span><span class="sxs-lookup"><span data-stu-id="1f5ce-141">end</span></span>|[<span data-ttu-id="1f5ce-142">DateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="1f5ce-142">DateTimeTimeZone</span></span>](../resources/datetimetimezone.md)|<span data-ttu-id="1f5ce-143">La fecha y hora en que finaliza el evento.</span><span class="sxs-lookup"><span data-stu-id="1f5ce-143">The date and time that the event ends.</span></span><br/><br/><span data-ttu-id="1f5ce-p104">De manera predeterminada, la hora de finalización está en formato UTC. Puede especificar una zona horaria opcional en EndTimeZone, expresar la hora de finalización en esa zona horaria e incluir una diferencia horaria de UTC. Tenga en cuenta que, si usa EndTimeZone, debe especificar también un valor para StartTimeZone.</span><span class="sxs-lookup"><span data-stu-id="1f5ce-p104">By default, the end time is in UTC. You can specify an optional time zone in EndTimeZone, express the end time in that time zone, and include a time offset from UTC. Note that if you use EndTimeZone, you must specify a value for StartTimeZone as well.</span></span><br/><br/><span data-ttu-id="1f5ce-147">En este ejemplo, se especifica el 25 de febrero de 2015, a las 9:34 p. m. en hora estándar del Pacífico: "2015-02-25T21:34:00-08:00".</span><span class="sxs-lookup"><span data-stu-id="1f5ce-147">This example specifies February 25, 2015, 9:34pm in Pacific Standard Time: "2015-02-25T21:34:00-08:00".</span></span> |
|<span data-ttu-id="1f5ce-148">importance</span><span class="sxs-lookup"><span data-stu-id="1f5ce-148">importance</span></span>|<span data-ttu-id="1f5ce-149">String</span><span class="sxs-lookup"><span data-stu-id="1f5ce-149">String</span></span>|<span data-ttu-id="1f5ce-150">Importancia del evento.</span><span class="sxs-lookup"><span data-stu-id="1f5ce-150">The importance of the event.</span></span> <span data-ttu-id="1f5ce-151">Los valores posibles son: `low`, `normal`, `high`.</span><span class="sxs-lookup"><span data-stu-id="1f5ce-151">The possible values are: `low`, `normal`, `high`.</span></span>|
|<span data-ttu-id="1f5ce-152">isAllDay</span><span class="sxs-lookup"><span data-stu-id="1f5ce-152">isAllDay</span></span>|<span data-ttu-id="1f5ce-153">Booleano</span><span class="sxs-lookup"><span data-stu-id="1f5ce-153">Boolean</span></span>|<span data-ttu-id="1f5ce-154">Se establece en true si el evento dura todo el día.</span><span class="sxs-lookup"><span data-stu-id="1f5ce-154">Set to true if the event lasts all day.</span></span>|
|<span data-ttu-id="1f5ce-155">isReminderOn</span><span class="sxs-lookup"><span data-stu-id="1f5ce-155">isReminderOn</span></span>|<span data-ttu-id="1f5ce-156">Booleano</span><span class="sxs-lookup"><span data-stu-id="1f5ce-156">Boolean</span></span>|<span data-ttu-id="1f5ce-157">Se establece en true si se establece una alerta para recordarle el evento al usuario.</span><span class="sxs-lookup"><span data-stu-id="1f5ce-157">Set to true if an alert is set to remind the user of the event.</span></span>|
|<span data-ttu-id="1f5ce-158">location</span><span class="sxs-lookup"><span data-stu-id="1f5ce-158">location</span></span>|[<span data-ttu-id="1f5ce-159">Location</span><span class="sxs-lookup"><span data-stu-id="1f5ce-159">Location</span></span>](../resources/location.md)|<span data-ttu-id="1f5ce-160">La ubicación del evento.</span><span class="sxs-lookup"><span data-stu-id="1f5ce-160">The location of the event.</span></span>|
|<span data-ttu-id="1f5ce-161">locations</span><span class="sxs-lookup"><span data-stu-id="1f5ce-161">locations</span></span>|<span data-ttu-id="1f5ce-162">Colección [location](../resources/location.md)</span><span class="sxs-lookup"><span data-stu-id="1f5ce-162">[location](../resources/location.md) collection</span></span>|<span data-ttu-id="1f5ce-163">Ubicaciones donde se celebra el evento o en las que se asiste.</span><span class="sxs-lookup"><span data-stu-id="1f5ce-163">The locations where the event is held or attended from.</span></span> <span data-ttu-id="1f5ce-164">Las propiedades **location** y **locations** siempre se corresponden entre sí.</span><span class="sxs-lookup"><span data-stu-id="1f5ce-164">The **location** and **locations** properties always correspond with each other.</span></span> <span data-ttu-id="1f5ce-165">Si se actualiza la propiedad **location**, se eliminarían las ubicaciones anteriores de la colección **locations** y se reemplazarían por el nuevo valor de **location**.</span><span class="sxs-lookup"><span data-stu-id="1f5ce-165">If you update the **location** property, any prior locations in the **locations** collection would be removed and replaced by the new **location** value.</span></span> |
|<span data-ttu-id="1f5ce-166">recurrence</span><span class="sxs-lookup"><span data-stu-id="1f5ce-166">recurrence</span></span>|[<span data-ttu-id="1f5ce-167">PatternedRecurrence</span><span class="sxs-lookup"><span data-stu-id="1f5ce-167">PatternedRecurrence</span></span>](../resources/patternedrecurrence.md)|<span data-ttu-id="1f5ce-168">El patrón de periodicidad del evento.</span><span class="sxs-lookup"><span data-stu-id="1f5ce-168">The recurrence pattern for the event.</span></span>|
|<span data-ttu-id="1f5ce-169">reminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="1f5ce-169">reminderMinutesBeforeStart</span></span>|<span data-ttu-id="1f5ce-170">Int32</span><span class="sxs-lookup"><span data-stu-id="1f5ce-170">Int32</span></span>|<span data-ttu-id="1f5ce-171">El número de minutos antes de la hora de inicio del evento en que se producirá la alerta del recordatorio.</span><span class="sxs-lookup"><span data-stu-id="1f5ce-171">The number of minutes before the event start time that the reminder alert occurs.</span></span>|
|<span data-ttu-id="1f5ce-172">responseRequested</span><span class="sxs-lookup"><span data-stu-id="1f5ce-172">responseRequested</span></span>|<span data-ttu-id="1f5ce-173">Booleano</span><span class="sxs-lookup"><span data-stu-id="1f5ce-173">Boolean</span></span>|<span data-ttu-id="1f5ce-174">Se establece en true si el remitente quiere una respuesta cuando el evento se acepta o rechaza.</span><span class="sxs-lookup"><span data-stu-id="1f5ce-174">Set to true if the sender would like a response when the event is accepted or declined.</span></span>|
|<span data-ttu-id="1f5ce-175">sensitivity</span><span class="sxs-lookup"><span data-stu-id="1f5ce-175">sensitivity</span></span>|<span data-ttu-id="1f5ce-176">String</span><span class="sxs-lookup"><span data-stu-id="1f5ce-176">String</span></span>| <span data-ttu-id="1f5ce-177">Los valores posibles son: `normal`, `personal`, `private`, `confidential`.</span><span class="sxs-lookup"><span data-stu-id="1f5ce-177">The possible values are: `normal`, `personal`, `private`, `confidential`.</span></span>|
|<span data-ttu-id="1f5ce-178">showAs</span><span class="sxs-lookup"><span data-stu-id="1f5ce-178">showAs</span></span>|<span data-ttu-id="1f5ce-179">String</span><span class="sxs-lookup"><span data-stu-id="1f5ce-179">String</span></span>|<span data-ttu-id="1f5ce-180">El estado que se mostrará.</span><span class="sxs-lookup"><span data-stu-id="1f5ce-180">The status to show.</span></span> <span data-ttu-id="1f5ce-181">Los valores posibles son: `free`, `tentative`, `busy`, `oof`, `workingElsewhere`, `unknown`.</span><span class="sxs-lookup"><span data-stu-id="1f5ce-181">The possible values are: `free`, `tentative`, `busy`, `oof`, `workingElsewhere`, `unknown`.</span></span>|
|<span data-ttu-id="1f5ce-182">start</span><span class="sxs-lookup"><span data-stu-id="1f5ce-182">start</span></span>|[<span data-ttu-id="1f5ce-183">DateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="1f5ce-183">DateTimeTimeZone</span></span>](../resources/datetimetimezone.md)|<span data-ttu-id="1f5ce-184">La hora de inicio del evento.</span><span class="sxs-lookup"><span data-stu-id="1f5ce-184">The start time of the event.</span></span> <br/><br/><span data-ttu-id="1f5ce-p108">De manera predeterminada, la hora de inicio está en formato UTC. Puede especificar una zona horaria opcional en StartTimeZone, expresar la hora de inicio en esa zona horaria e incluir una diferencia horaria de UTC. Tenga en cuenta que, si usa StartTimeZone, debe especificar también un valor para EndTimeZone.</span><span class="sxs-lookup"><span data-stu-id="1f5ce-p108">By default, the start time is in UTC. You can specify an optional time zone in StartTimeZone, express the start time in that time zone, and include a time offset from UTC. Note that if you use StartTimeZone, you must specify a value for EndTimeZone as well.</span></span><br/><br/><span data-ttu-id="1f5ce-188">En este ejemplo, se especifica el 25 de febrero de 2015, a las 7:34 p. m. en hora estándar del Pacífico: "2015-02-25T19:34:00-08:00".</span><span class="sxs-lookup"><span data-stu-id="1f5ce-188">This example specifies February 25, 2015, 7:34pm in Pacific Standard Time: "2015-02-25T19:34:00-08:00".</span></span>  |
|<span data-ttu-id="1f5ce-189">subject</span><span class="sxs-lookup"><span data-stu-id="1f5ce-189">subject</span></span>|<span data-ttu-id="1f5ce-190">String</span><span class="sxs-lookup"><span data-stu-id="1f5ce-190">String</span></span>|<span data-ttu-id="1f5ce-191">El texto de la línea de asunto del evento.</span><span class="sxs-lookup"><span data-stu-id="1f5ce-191">The text of the event's subject line.</span></span>|

<span data-ttu-id="1f5ce-192">Debido a que el recurso de **evento** es compatible con [las extensiones](/graph/extensibility-overview), puede usar el `PATCH` operación para agregar, actualizar o eliminar sus propios datos específicas de la aplicación en las propiedades personalizadas de una extensión en una instancia de **evento** existente.</span><span class="sxs-lookup"><span data-stu-id="1f5ce-192">Because the **event** resource supports [extensions](/graph/extensibility-overview), you can use the `PATCH` operation to add, update, or delete your own app-specific data in custom properties of an extension in an existing **event** instance.</span></span>  
  
<span data-ttu-id="1f5ce-193">Si el **evento** que se va a actualizar es el evento maestro de una serie periódica, contiene varios asistentes, y tiene instancias que se han actualizado por separado, los cuales se van a enviar mensajes de correo electrónico de notificación varios: uno para la serie principal y uno por cada instancia que tiene se han actualizado.</span><span class="sxs-lookup"><span data-stu-id="1f5ce-193">If the **event** you're updating is the master event of a recurring series, contains multiple attendees, and has instances that have been updated separately, multiple notification emails will be sent out: one for the master series and one per instance that has been updated.</span></span>  

## <a name="response"></a><span data-ttu-id="1f5ce-194">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1f5ce-194">Response</span></span>

<span data-ttu-id="1f5ce-195">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [event](../resources/event.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1f5ce-195">If successful, this method returns a `200 OK` response code and updated [event](../resources/event.md) object in the response body.</span></span>  

><span data-ttu-id="1f5ce-196">**Nota:** Este método puede devolver una respuesta HTTP 400 Solicitud incorrecta con un código de error de `ErrorOccurrenceCrossingBoundary` y el siguiente mensaje de error: la repetición modificada cruza o se superpone repetición adyacente.</span><span class="sxs-lookup"><span data-stu-id="1f5ce-196">**Note:** This method can return an HTTP 400 Bad Request response with an error code of `ErrorOccurrenceCrossingBoundary` and the following error message: Modified occurrence is crossing or overlapping adjacent occurrence.</span></span> <span data-ttu-id="1f5ce-197">Esto indica que la actualización infringe la siguiente restricción de Outlook en las excepciones periódicas: huérfana no se puede mover a o antes del día de la repetición anterior y no se puede mover a o después del día de la siguiente aparición.</span><span class="sxs-lookup"><span data-stu-id="1f5ce-197">This indicates that the update violates the following Outlook restriction on recurrence exceptions: an occurrence cannot be moved to or before the day of the previous occurrence, and cannot be moved to or after the day of the following occurrence.</span></span>

## <a name="example"></a><span data-ttu-id="1f5ce-198">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1f5ce-198">Example</span></span>

##### <a name="request"></a><span data-ttu-id="1f5ce-199">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1f5ce-199">Request</span></span>

<span data-ttu-id="1f5ce-200">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1f5ce-200">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="1f5ce-201">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1f5ce-201">Response</span></span>

<span data-ttu-id="1f5ce-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1f5ce-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

## <a name="see-also"></a><span data-ttu-id="1f5ce-205">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f5ce-205">See also</span></span>

- [<span data-ttu-id="1f5ce-206">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="1f5ce-206">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="1f5ce-207">Agregar datos personalizados a los usuarios mediante extensiones abiertas</span><span class="sxs-lookup"><span data-stu-id="1f5ce-207">Add custom data to users using open extensions</span></span>](/graph/extensibility-open-users)
- [<span data-ttu-id="1f5ce-208">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="1f5ce-208">Add custom data to groups using schema extensions</span></span>](/graph/extensibility-schema-groups)



<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update event",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
