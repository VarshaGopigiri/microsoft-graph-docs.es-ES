---
title: Actualizar evento
description: Actualizar las propiedades del objeto event.
author: angelgolfer-ms
localization_priority: Priority
ms.prod: outlook
ms.openlocfilehash: 441a135cf43226927e9a8aee074c2547b9beb23e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27972372"
---
# <a name="update-event"></a>Actualizar evento

Actualizar las propiedades del objeto [event](../resources/event.md) .
## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Calendars.ReadWrite    |
|Delegado (cuenta personal de Microsoft) | Calendars.ReadWrite    |
|Aplicación | Calendars.ReadWrite |

## <a name="http-request"></a>Solicitud HTTP
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
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción|
|:-----------|:------|:----------|
| Autorización  | string  | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.

| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|attendees|[Attendee](../resources/attendee.md)|La colección de asistentes del evento.|
|body|[ItemBody](../resources/itembody.md)|El cuerpo del mensaje asociado con el evento.|
|categories|String|Las categorías asociadas con el evento.|
|end|[DateTimeTimeZone](../resources/datetimetimezone.md)|La fecha y hora en que finaliza el evento.<br/><br/>De manera predeterminada, la hora de finalización está en formato UTC. Puede especificar una zona horaria opcional en EndTimeZone, expresar la hora de finalización en esa zona horaria e incluir una diferencia horaria de UTC. Tenga en cuenta que, si usa EndTimeZone, debe especificar también un valor para StartTimeZone.<br/><br/>En este ejemplo, se especifica el 25 de febrero de 2015, a las 9:34 p. m. en hora estándar del Pacífico: "2015-02-25T21:34:00-08:00". |
|importance|String|Importancia del evento. Los valores posibles son: `low`, `normal`, `high`.|
|isAllDay|Booleano|Se establece en true si el evento dura todo el día.|
|isReminderOn|Booleano|Se establece en true si se establece una alerta para recordarle el evento al usuario.|
|location|[Location](../resources/location.md)|La ubicación del evento.|
|locations|Colección [location](../resources/location.md)|Ubicaciones donde se celebra el evento o en las que se asiste. Las propiedades **location** y **locations** siempre se corresponden entre sí. Si se actualiza la propiedad **location**, se eliminarían las ubicaciones anteriores de la colección **locations** y se reemplazarían por el nuevo valor de **location**. |
|recurrence|[PatternedRecurrence](../resources/patternedrecurrence.md)|El patrón de periodicidad del evento.|
|reminderMinutesBeforeStart|Int32|El número de minutos antes de la hora de inicio del evento en que se producirá la alerta del recordatorio.|
|responseRequested|Booleano|Se establece en true si el remitente quiere una respuesta cuando el evento se acepta o rechaza.|
|sensitivity|Cadena| Los valores posibles son: `normal`, `personal`, `private`, `confidential`.|
|showAs|String|El estado que se mostrará. Los valores posibles son: `free`, `tentative`, `busy`, `oof`, `workingElsewhere`, `unknown`.|
|start|[DateTimeTimeZone](../resources/datetimetimezone.md)|La hora de inicio del evento. <br/><br/>De manera predeterminada, la hora de inicio está en formato UTC. Puede especificar una zona horaria opcional en StartTimeZone, expresar la hora de inicio en esa zona horaria e incluir una diferencia horaria de UTC. Tenga en cuenta que, si usa StartTimeZone, debe especificar también un valor para EndTimeZone.<br/><br/>En este ejemplo, se especifica el 25 de febrero de 2015, a las 7:34 p. m. en hora estándar del Pacífico: "2015-02-25T19:34:00-08:00".  |
|subject|Cadena|El texto de la línea de asunto del evento.|

Debido a que el recurso de **evento** es compatible con [las extensiones](/graph/extensibility-overview), puede usar el `PATCH` operación para agregar, actualizar o eliminar sus propios datos específicas de la aplicación en las propiedades personalizadas de una extensión en una instancia de **evento** existente.  
  
Si el **evento** que se va a actualizar es el evento maestro de una serie periódica, contiene varios asistentes, y tiene instancias que se han actualizado por separado, los cuales se van a enviar mensajes de correo electrónico de notificación varios: uno para la serie principal y uno por cada instancia que tiene se han actualizado.  

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [event](../resources/event.md) actualizado en el cuerpo de la respuesta.  

>**Nota:** Este método puede devolver una respuesta HTTP 400 Solicitud incorrecta con un código de error de `ErrorOccurrenceCrossingBoundary` y el siguiente mensaje de error: la repetición modificada cruza o se superpone repetición adyacente. Esto indica que la actualización infringe la siguiente restricción de Outlook en las excepciones periódicas: huérfana no se puede mover a o antes del día de la repetición anterior y no se puede mover a o después del día de la siguiente aparición.

## <a name="example"></a>Ejemplo

##### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.
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

##### <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
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

## <a name="see-also"></a>Vea también

- [Agregar datos personalizados a los recursos mediante extensiones](/graph/extensibility-overview)
- [Agregar datos personalizados a los usuarios mediante extensiones abiertas](/graph/extensibility-open-users)
- [Agregar datos personalizados a los grupos mediante extensiones de esquema](/graph/extensibility-schema-groups)



<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update event",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
