---
title: List calendarView
description: Obtenga las repeticiones, excepciones e instancias únicas de eventos en una vista de calendario definida por un intervalo de tiempo,
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: 8339809f212bcd4bcdb8700826397a5ca234bdd4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27956838"
---
# <a name="list-calendarview"></a>List calendarView

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Obtiene las repeticiones, excepciones e instancias únicas de eventos en una vista de calendario definida por un intervalo de tiempo del calendario predeterminado `(../me/calendarview)` de un usuario o grupo, o alguno de los otros calendarios del usuario.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

* Eventos en el calendario de un usuario: Calendars.Read o Calendars.ReadWrite
* Eventos de un calendario de grupo: Group.Read.All o Group.ReadWrite.All

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->Un usuario o del grupo predeterminado de [calendario](../resources/calendar.md).
```http
GET /me/calendar/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendar/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /groups/{id}/calendar/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
```

[calendar](../resources/calendar.md) de un usuario del [calendarGroup](../resources/calendargroup.md) predeterminado.
```http
GET /me/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}

GET /me/calendarGroup/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendarGroup/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
```

[calendar](../resources/calendar.md) de un usuario de un [calendarGroup](../resources/calendargroup.md) específico.
```http
GET /me/calendarGroups/{id}/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
GET /users/{id | userPrincipalName}/calendarGroups/{id}/calendars/{id}/calendarView?startDateTime={start_datetime}&endDateTime={end_datetime}
```

## <a name="query-parameters"></a>Parámetros de consulta

En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta necesarios con valores.

| Parámetro    | Tipo   |Descripción|
|:---------------|:--------|:----------|
|startDateTime|String|La fecha y hora de inicio del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T19:00:00.0000000".|
|endDateTime|String|La fecha y hora de finalización del intervalo de tiempo, representada en formato ISO 8601. Por ejemplo, "2015-11-08T20:00:00.0000000".|

Este método también admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción |
|:---------------|:--------|:--------|
| Authorization  | string | {token} de portador. Obligatorio.  |
| Prefer: outlook.timezone  | string | Se usa para especificar la zona horaria de las horas de inicio y final de la respuesta. Si no se especifican, estos valores de hora se devuelven en UTC. Opcional. |

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Event](../resources/event.md) en el cuerpo de la respuesta.
## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "get_calendarview"
}-->
```http
GET https://graph.microsoft.com/beta/me/calendar/calendarView?startDateTime=2017-01-01T19:00:00.0000000&endDateTime=2017-01-07T19:00:00.0000000
```
##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.event",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 354

{
  "value": [
    {
      "originalStartTimeZone": "originalStartTimeZone-value",
      "originalEndTimeZone": "originalEndTimeZone-value",
      "responseStatus": {
        "response": "response-value",
        "time": "2016-10-19T10:37:00Z"
      },
      "uid": "iCalUId-value",
      "reminderMinutesBeforeStart": 99,
      "isReminderOn": true
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List calendarView",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
