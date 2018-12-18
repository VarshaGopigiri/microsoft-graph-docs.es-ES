---
title: Actualizar evento
description: Actualizar las propiedades del objeto event.
author: angelgolfer-ms
ms.openlocfilehash: 05612f50b038f491598b98c5661fac17238419df
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27330677"
---
# <a name="update-event"></a><span data-ttu-id="5aa28-103">Actualizar evento</span><span class="sxs-lookup"><span data-stu-id="5aa28-103">Update event</span></span>

> <span data-ttu-id="5aa28-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5aa28-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5aa28-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5aa28-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5aa28-106">Actualizar las propiedades del objeto [event](../resources/event.md) .</span><span class="sxs-lookup"><span data-stu-id="5aa28-106">Update the properties of the [event](../resources/event.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="5aa28-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="5aa28-107">Permissions</span></span>
<span data-ttu-id="5aa28-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5aa28-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5aa28-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5aa28-110">Permission type</span></span>      | <span data-ttu-id="5aa28-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5aa28-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5aa28-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5aa28-112">Delegated (work or school account)</span></span> | <span data-ttu-id="5aa28-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5aa28-113">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="5aa28-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5aa28-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5aa28-115">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5aa28-115">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="5aa28-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5aa28-116">Application</span></span> | <span data-ttu-id="5aa28-117">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5aa28-117">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="5aa28-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5aa28-118">HTTP request</span></span>
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
## <a name="request-headers"></a><span data-ttu-id="5aa28-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5aa28-119">Request headers</span></span>
| <span data-ttu-id="5aa28-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="5aa28-120">Name</span></span>       | <span data-ttu-id="5aa28-121">Type</span><span class="sxs-lookup"><span data-stu-id="5aa28-121">Type</span></span> | <span data-ttu-id="5aa28-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="5aa28-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="5aa28-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="5aa28-123">Authorization</span></span>  | <span data-ttu-id="5aa28-124">string</span><span class="sxs-lookup"><span data-stu-id="5aa28-124">string</span></span>  | <span data-ttu-id="5aa28-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5aa28-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="5aa28-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5aa28-127">Request body</span></span>
<span data-ttu-id="5aa28-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="5aa28-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="5aa28-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5aa28-131">Property</span></span>       | <span data-ttu-id="5aa28-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="5aa28-132">Type</span></span>    | <span data-ttu-id="5aa28-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="5aa28-133">Description</span></span> |
|:---------------|:--------|:------------|
| <span data-ttu-id="5aa28-134">attendees</span><span class="sxs-lookup"><span data-stu-id="5aa28-134">attendees</span></span>|<span data-ttu-id="5aa28-135">Attendee</span><span class="sxs-lookup"><span data-stu-id="5aa28-135">Attendee</span></span>|<span data-ttu-id="5aa28-136">La colección de asistentes del evento.</span><span class="sxs-lookup"><span data-stu-id="5aa28-136">The collection of attendees for the event.</span></span>|
| <span data-ttu-id="5aa28-137">body</span><span class="sxs-lookup"><span data-stu-id="5aa28-137">body</span></span>|<span data-ttu-id="5aa28-138">ItemBody</span><span class="sxs-lookup"><span data-stu-id="5aa28-138">ItemBody</span></span>|<span data-ttu-id="5aa28-139">El cuerpo del mensaje asociado con el evento.</span><span class="sxs-lookup"><span data-stu-id="5aa28-139">The body of the message associated with the event.</span></span>|
| <span data-ttu-id="5aa28-140">categories</span><span class="sxs-lookup"><span data-stu-id="5aa28-140">categories</span></span>|<span data-ttu-id="5aa28-141">String</span><span class="sxs-lookup"><span data-stu-id="5aa28-141">String</span></span>|<span data-ttu-id="5aa28-142">Las categorías asociadas con el evento.</span><span class="sxs-lookup"><span data-stu-id="5aa28-142">The categories associated with the event.</span></span>|
| <span data-ttu-id="5aa28-143">end</span><span class="sxs-lookup"><span data-stu-id="5aa28-143">end</span></span>|<span data-ttu-id="5aa28-144">DateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="5aa28-144">DateTimeTimeZone</span></span>|<span data-ttu-id="5aa28-145">La fecha y hora en que finaliza el evento.</span><span class="sxs-lookup"><span data-stu-id="5aa28-145">The date and time that the event ends.</span></span><br/><br/><span data-ttu-id="5aa28-p105">De manera predeterminada, la hora de finalización está en formato UTC. Puede especificar una zona horaria opcional en EndTimeZone, expresar la hora de finalización en esa zona horaria e incluir una diferencia horaria de UTC. Tenga en cuenta que, si usa EndTimeZone, debe especificar también un valor para StartTimeZone.</span><span class="sxs-lookup"><span data-stu-id="5aa28-p105">By default, the end time is in UTC. You can specify an optional time zone in EndTimeZone, express the end time in that time zone, and include a time offset from UTC. Note that if you use EndTimeZone, you must specify a value for StartTimeZone as well.</span></span><br/><br/><span data-ttu-id="5aa28-149">En este ejemplo, se especifica el 25 de febrero de 2015, a las 9:34 p. m. en hora estándar del Pacífico: "2015-02-25T21:34:00-08:00".</span><span class="sxs-lookup"><span data-stu-id="5aa28-149">This example specifies February 25, 2015, 9:34pm in Pacific Standard Time: "2015-02-25T21:34:00-08:00".</span></span> |
| <span data-ttu-id="5aa28-150">importance</span><span class="sxs-lookup"><span data-stu-id="5aa28-150">importance</span></span>|<span data-ttu-id="5aa28-151">String</span><span class="sxs-lookup"><span data-stu-id="5aa28-151">String</span></span>|<span data-ttu-id="5aa28-152">Importancia del evento.</span><span class="sxs-lookup"><span data-stu-id="5aa28-152">The importance of the event.</span></span> <span data-ttu-id="5aa28-153">Los valores posibles son: `low`, `normal` y `high`.</span><span class="sxs-lookup"><span data-stu-id="5aa28-153">Possible values are: `low`, `normal`, `high`.</span></span>|
| <span data-ttu-id="5aa28-154">isAllDay</span><span class="sxs-lookup"><span data-stu-id="5aa28-154">isAllDay</span></span>|<span data-ttu-id="5aa28-155">Booleano</span><span class="sxs-lookup"><span data-stu-id="5aa28-155">Boolean</span></span>|<span data-ttu-id="5aa28-156">Se establece en true si el evento dura todo el día.</span><span class="sxs-lookup"><span data-stu-id="5aa28-156">Set to true if the event lasts all day.</span></span>|
| <span data-ttu-id="5aa28-157">isReminderOn</span><span class="sxs-lookup"><span data-stu-id="5aa28-157">isReminderOn</span></span>|<span data-ttu-id="5aa28-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="5aa28-158">Boolean</span></span>|<span data-ttu-id="5aa28-159">Se establece en true si se establece una alerta para recordarle el evento al usuario.</span><span class="sxs-lookup"><span data-stu-id="5aa28-159">Set to true if an alert is set to remind the user of the event.</span></span>|
| <span data-ttu-id="5aa28-160">location</span><span class="sxs-lookup"><span data-stu-id="5aa28-160">location</span></span>|<span data-ttu-id="5aa28-161">Location</span><span class="sxs-lookup"><span data-stu-id="5aa28-161">Location</span></span>|<span data-ttu-id="5aa28-162">La ubicación del evento.</span><span class="sxs-lookup"><span data-stu-id="5aa28-162">The location of the event.</span></span>|
|<span data-ttu-id="5aa28-163">locations</span><span class="sxs-lookup"><span data-stu-id="5aa28-163">locations</span></span>|<span data-ttu-id="5aa28-164">Colección de [ubicación](../resources/location.md)</span><span class="sxs-lookup"><span data-stu-id="5aa28-164">[Location](../resources/location.md) collection</span></span>|<span data-ttu-id="5aa28-165">Ubicaciones donde se celebra el evento o en las que se asiste.</span><span class="sxs-lookup"><span data-stu-id="5aa28-165">The locations where the event is held or attended from.</span></span> <span data-ttu-id="5aa28-166">Las propiedades **location** y **locations** siempre se corresponden entre sí.</span><span class="sxs-lookup"><span data-stu-id="5aa28-166">The **location** and **locations** properties always correspond with each other.</span></span> <span data-ttu-id="5aa28-167">Si se actualiza la propiedad **location**, se eliminarían las ubicaciones anteriores de la colección **locations** y se reemplazarían por el nuevo valor de **location**.</span><span class="sxs-lookup"><span data-stu-id="5aa28-167">If you update the **location** property, any prior locations in the **locations** collection would be removed and replaced by the new **location** value.</span></span> |
| <span data-ttu-id="5aa28-168">recurrence</span><span class="sxs-lookup"><span data-stu-id="5aa28-168">recurrence</span></span>|<span data-ttu-id="5aa28-169">PatternedRecurrence</span><span class="sxs-lookup"><span data-stu-id="5aa28-169">PatternedRecurrence</span></span>|<span data-ttu-id="5aa28-170">El patrón de periodicidad del evento.</span><span class="sxs-lookup"><span data-stu-id="5aa28-170">The recurrence pattern for the event.</span></span>|
| <span data-ttu-id="5aa28-171">reminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="5aa28-171">reminderMinutesBeforeStart</span></span>|<span data-ttu-id="5aa28-172">Int32</span><span class="sxs-lookup"><span data-stu-id="5aa28-172">Int32</span></span>|<span data-ttu-id="5aa28-173">El número de minutos antes de la hora de inicio del evento en que se producirá la alerta del recordatorio.</span><span class="sxs-lookup"><span data-stu-id="5aa28-173">The number of minutes before the event start time that the reminder alert occurs.</span></span>|
| <span data-ttu-id="5aa28-174">responseRequested</span><span class="sxs-lookup"><span data-stu-id="5aa28-174">responseRequested</span></span>|<span data-ttu-id="5aa28-175">Booleano</span><span class="sxs-lookup"><span data-stu-id="5aa28-175">Boolean</span></span>|<span data-ttu-id="5aa28-176">Se establece en true si el remitente quiere una respuesta cuando el evento se acepta o rechaza.</span><span class="sxs-lookup"><span data-stu-id="5aa28-176">Set to true if the sender would like a response when the event is accepted or declined.</span></span>|
| <span data-ttu-id="5aa28-177">sensitivity</span><span class="sxs-lookup"><span data-stu-id="5aa28-177">sensitivity</span></span>|<span data-ttu-id="5aa28-178">String</span><span class="sxs-lookup"><span data-stu-id="5aa28-178">String</span></span>| <span data-ttu-id="5aa28-179">Los valores posibles son: `normal`, `personal`, `private`, `confidential`.</span><span class="sxs-lookup"><span data-stu-id="5aa28-179">Possible values are: `normal`, `personal`, `private`, `confidential`.</span></span>|
| <span data-ttu-id="5aa28-180">showAs</span><span class="sxs-lookup"><span data-stu-id="5aa28-180">showAs</span></span>|<span data-ttu-id="5aa28-181">String</span><span class="sxs-lookup"><span data-stu-id="5aa28-181">String</span></span>|<span data-ttu-id="5aa28-182">El estado que se mostrará.</span><span class="sxs-lookup"><span data-stu-id="5aa28-182">The status to show.</span></span> <span data-ttu-id="5aa28-183">Los valores posibles son: `free` , `tentative`, `busy`, `oof`, `workingElsewhere`, `unknown`.</span><span class="sxs-lookup"><span data-stu-id="5aa28-183">Possible values are: `free` , `tentative`, `busy`, `oof`, `workingElsewhere`, `unknown`.</span></span>|
| <span data-ttu-id="5aa28-184">start</span><span class="sxs-lookup"><span data-stu-id="5aa28-184">start</span></span>|<span data-ttu-id="5aa28-185">DateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="5aa28-185">DateTimeTimeZone</span></span>|<span data-ttu-id="5aa28-186">La hora de inicio del evento.</span><span class="sxs-lookup"><span data-stu-id="5aa28-186">The start time of the event.</span></span> <br/><br/><span data-ttu-id="5aa28-p109">De manera predeterminada, la hora de inicio está en formato UTC. Puede especificar una zona horaria opcional en StartTimeZone, expresar la hora de inicio en esa zona horaria e incluir una diferencia horaria de UTC. Tenga en cuenta que, si usa StartTimeZone, debe especificar también un valor para EndTimeZone.</span><span class="sxs-lookup"><span data-stu-id="5aa28-p109">By default, the start time is in UTC. You can specify an optional time zone in StartTimeZone, express the start time in that time zone, and include a time offset from UTC. Note that if you use StartTimeZone, you must specify a value for EndTimeZone as well.</span></span><br/><br/><span data-ttu-id="5aa28-190">En este ejemplo, se especifica el 25 de febrero de 2015, a las 7:34 p. m. en hora estándar del Pacífico: "2015-02-25T19:34:00-08:00".</span><span class="sxs-lookup"><span data-stu-id="5aa28-190">This example specifies February 25, 2015, 7:34pm in Pacific Standard Time: "2015-02-25T19:34:00-08:00".</span></span>  |
| <span data-ttu-id="5aa28-191">subject</span><span class="sxs-lookup"><span data-stu-id="5aa28-191">subject</span></span>|<span data-ttu-id="5aa28-192">String</span><span class="sxs-lookup"><span data-stu-id="5aa28-192">String</span></span>|<span data-ttu-id="5aa28-193">El texto de la línea de asunto del evento.</span><span class="sxs-lookup"><span data-stu-id="5aa28-193">The text of the event's subject line.</span></span>|

<span data-ttu-id="5aa28-194">Debido a que el recurso de **evento** es compatible con [las extensiones](/graph/extensibility-overview), puede usar el `PATCH` operación para agregar, actualizar o eliminar sus propios datos específicas de la aplicación en las propiedades personalizadas de una extensión en una instancia de **evento** existente.</span><span class="sxs-lookup"><span data-stu-id="5aa28-194">Because the **event** resource supports [extensions](/graph/extensibility-overview), you can use the `PATCH` operation to add, update, or delete your own app-specific data in custom properties of an extension in an existing **event** instance.</span></span>

<span data-ttu-id="5aa28-195">Si el **evento** que se va a actualizar es el evento maestro de una serie periódica, contiene varios asistentes, y tiene instancias que se han actualizado por separado, los cuales se van a enviar mensajes de correo electrónico de notificación varios: uno para la serie principal y uno por cada instancia que tiene se han actualizado.</span><span class="sxs-lookup"><span data-stu-id="5aa28-195">If the **event** you're updating is the master event of a recurring series, contains multiple attendees, and has instances that have been updated separately, multiple notification emails will be sent out: one for the master series and one per instance that has been updated.</span></span>

## <a name="response"></a><span data-ttu-id="5aa28-196">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5aa28-196">Response</span></span>

<span data-ttu-id="5aa28-197">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [event](../resources/event.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5aa28-197">If successful, this method returns a `200 OK` response code and updated [event](../resources/event.md) object in the response body.</span></span>

><span data-ttu-id="5aa28-198">**Nota:** Este método puede devolver una respuesta HTTP 400 Solicitud incorrecta con un código de error de `ErrorOccurrenceCrossingBoundary` y el siguiente mensaje de error: la repetición modificada cruza o se superpone repetición adyacente.</span><span class="sxs-lookup"><span data-stu-id="5aa28-198">**Note:** This method can return an HTTP 400 Bad Request response with an error code of `ErrorOccurrenceCrossingBoundary` and the following error message: Modified occurrence is crossing or overlapping adjacent occurrence.</span></span> <span data-ttu-id="5aa28-199">Esto indica que la actualización infringe la siguiente restricción de Outlook en las excepciones periódicas: huérfana no se puede mover a o antes del día de la repetición anterior y no se puede mover a o después del día de la siguiente aparición.</span><span class="sxs-lookup"><span data-stu-id="5aa28-199">This indicates that the update violates the following Outlook restriction on recurrence exceptions: an occurrence cannot be moved to or before the day of the previous occurrence, and cannot be moved to or after the day of the following occurrence.</span></span>

## <a name="example"></a><span data-ttu-id="5aa28-200">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5aa28-200">Example</span></span>

##### <a name="request"></a><span data-ttu-id="5aa28-201">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5aa28-201">Request</span></span>

<span data-ttu-id="5aa28-202">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5aa28-202">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_event"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/events/{id}
Content-type: application/json
Content-length: 285

{
  "originalStartTimeZone": "originalStartTimeZone-value",
  "originalEndTimeZone": "originalEndTimeZone-value",
  "responseStatus": {
    "response": "",
    "time": "2016-10-19T10:37:00Z"
  },
  "recurrence": null,
  "uid": "iCalUId-value",
  "reminderMinutesBeforeStart": 99,
  "isReminderOn": true
}
```

##### <a name="response"></a><span data-ttu-id="5aa28-203">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5aa28-203">Response</span></span>
<span data-ttu-id="5aa28-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5aa28-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
    "time": "2016-10-19T10:37:00Z"
  },
  "recurrence": null,
  "uid": "iCalUId-value",
  "reminderMinutesBeforeStart": 99,
  "isReminderOn": true
}
```


## <a name="see-also"></a><span data-ttu-id="5aa28-207">Vea también</span><span class="sxs-lookup"><span data-stu-id="5aa28-207">See also</span></span>

- [<span data-ttu-id="5aa28-208">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="5aa28-208">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="5aa28-209">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="5aa28-209">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)
- [<span data-ttu-id="5aa28-210">Agregar datos personalizados a grupos mediante extensiones de esquema (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="5aa28-210">Add custom data to groups using schema extensions (preview)</span></span>](/graph/extensibility-schema-groups)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update event",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
