# <a name="delete-calendar"></a>Eliminar calendario

Elimine un calendario que no sea el predeterminado.
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Calendars.ReadWrite*
## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
Un [calendar](../resources/calendar.md) de usuario que no sea el calendario predeterminado del [calendarGroup](../resources/calendargroup.md) predeterminado.
```http
DELETE /me/calendars/{id}
DELETE /users/{id | userPrincipalName}/calendars/{id}

DELETE /me/calendarGroup/calendars/{id}
DELETE /users/{id | userPrincipalName}/calendarGroup/calendars/{id}
```
Un [calendar](../resources/calendar.md) que no sea el calendario predeterminado de un [calendarGroup](../resources/calendargroup.md) específico.
```http
DELETE /me/calendarGroups/{id}/calendars/{id}
DELETE /users/{id | userPrincipalName}/calendarGroups/{id}/calendars/{id}
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre           |  Tipo    | Descripción|
|:---------------|:---------|:----------|
| Authorization  |  string  | {token} de portador. Necesario. |

## <a name="request-body"></a>Cuerpo de solicitud
No proporcione un cuerpo de solicitud para este método.


## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "delete_calendar"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/calendar
```
##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete calendar",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
