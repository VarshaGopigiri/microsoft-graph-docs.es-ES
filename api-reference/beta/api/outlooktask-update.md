---
title: Actualizar outlooktask
description: Cambiar las propiedades modificables de una tarea de Outlook.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: c0d2ff13f3e7971e686389709fbdde027458ef67
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27964938"
---
# <a name="update-outlooktask"></a>Actualizar outlooktask

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Cambiar las propiedades modificables de una tarea de Outlook.

La propiedad **completedDateTime** se puede establecer mediante la acción **completa** , o explícitamente mediante una operación de revisión. Si usa revisión para establecer **completedDateTime**, asegúrese de establecer el **estado** en `completed` así como.

De forma predeterminada, esta operación (y las operaciones de tarea POST, GET y [completar](../api/outlooktask-complete.md) ) devuelve propiedades relacionadas con la fecha en UTC. Puede usar el `Prefer: outlook.timezone` encabezado para que todas las propiedades relacionadas con la fecha en la respuesta representada en una zona horaria diferente a la hora UTC.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Tasks.ReadWrite    |
|Delegado (cuenta personal de Microsoft) | Tasks.ReadWrite    |
|Aplicación | No admitida. |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
PATCH /me/outlook/tasks/{id}
PATCH /users/{id|userPrincipalName}/outlook/tasks/{id}
```

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre       | Descripción|
|:-----------|:-----------|
| Authorization  | {token} de portador. Obligatorio. |
| Prefer: outlook.timezone | Especifica la zona horaria de propiedades de tiempo en la respuesta, que sería en UTC si no se especifica este encabezado. Opcional.|

## <a name="request-body"></a>Cuerpo de la solicitud

En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.

| Propiedad | Tipo | Descripción |
|:---------------|:--------|:----------|
|assignedTo|Cadena|El nombre de la persona que se le ha asignado la tarea.|
|body|[itemBody](../resources/itembody.md)|El cuerpo de la tarea que normalmente contiene información acerca de la tarea. Tenga en cuenta que sólo el tipo HTML es compatible.|
|categories|Colección String|Las categorías asociadas con la tarea.|
|changeKey|Cadena|La versión de la tarea.|
|completedDateTime|[dateTimeTimeZone](../resources/datetimetimezone.md)|La fecha en la zona horaria especificada que se ha finalizado la tarea.|
|createdDateTime|DateTimeOffset|La fecha y la hora cuando se creó la tarea. De forma predeterminada, está en UTC. Puede proporcionar una zona horaria personalizada en el encabezado de solicitud. El valor de la propiedad usa formato ISO 8601. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.|
|dueDateTime|[dateTimeTimeZone](../resources/datetimetimezone.md)|La fecha en la zona horaria especificada que se va finalizado la tarea.|
|hasAttachments|Booleano|Se establece en true si la tarea tiene datos adjuntos.|
|importance|string|Importancia del evento. Los valores posibles son: `low`, `normal` y `high`.|
|isReminderOn|Booleano|Se establece en true si se establece una alerta para recordarle al usuario de la tarea.|
|lastModifiedDateTime|DateTimeOffset|La fecha y hora de última modificación de la tarea. De forma predeterminada, está en UTC. Puede proporcionar una zona horaria personalizada en el encabezado de solicitud. El valor de la propiedad utiliza el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.|
|owner|Cadena|El nombre de la persona que creó la tarea.|
|parentFolderId|Cadena|El identificador único para la carpeta principal de la tarea.|
|periodicidad|[patternedRecurrence](../resources/patternedrecurrence.md)|El patrón de periodicidad de la tarea.|
|reminderDateTime|[dateTimeTimeZone](../resources/datetimetimezone.md)|La fecha y hora para un aviso de la tarea que se produzca.|
|sensitivity|string|Indica el nivel de privacidad para la tarea. Los valores posibles son: `normal`, `personal`, `private` y `confidential`.|
|startDateTime|[dateTimeTimeZone](../resources/datetimetimezone.md)|La fecha en la zona horaria especificada cuando la tarea que se va a comenzar.|
|status|string|Indica el estado o el progreso de la tarea. Los valores posibles son: `notStarted`, `inProgress`, `completed`, `waitingOnOthers` y `deferred`.|
|subject|Cadena|Una breve descripción o el título de la tarea.|

## <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve una `200 OK` código de respuesta y actualizada [outlookTask](../resources/outlooktask.md) objeto en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

### <a name="request"></a>Solicitud

El siguiente ejemplo se modifica la propiedad **dueDateTime** y usa el `Prefer: outlook.timezone` encabezado para especificar expresar las propiedades relacionadas con la fecha en la respuesta en la hora estándar (EST).
<!-- {
  "blockType": "request",
  "name": "update_outlooktask"
}-->

```http
PATCH https://graph.microsoft.com/beta/me/outlook/tasks('AAMkADA1MTHgwAAA=')

Prefer: outlook.timezone="Eastern Standard Time"
Content-type: application/json
Content-length: 76

{
  "dueDateTime":  {
      "dateTime": "2016-05-06T16:00:00",
      "timeZone": "Eastern Standard Time"
  }
}
```

### <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.outlookTask"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 376

{
    "id": "AAMkADA1MTHgwAAA=",
    "createdDateTime": "2016-04-22T18:19:18.9526004-04:00",
    "lastModifiedDateTime": "2016-04-22T18:38:20.5541528-04:00",
    "changeKey": "1/KC9Vmu40G3DwB6Lgs7MAAAIW9XXg==",
    "categories": [
    ],
    "assignedTo": null,
    "body": {
        "contentType": "text",
        "content": ""
    },
    "completedDateTime": null,
    "dueDateTime": {
        "dateTime": "2016-05-06T00:00:00.0000000",
        "timeZone": "Eastern Standard Time"
    },
    "hasAttachments":false,
    "importance": "normal",
    "isReminderOn": false,
    "owner": "Administrator",
    "parentFolderId": "AQMkADA1MTIBEgAAAA==",
    "recurrence": null,
    "reminderDateTime": null,
    "sensitivity": "normal",
    "startDateTime": {
        "dateTime": "2016-05-03T00:00:00.0000000",
        "timeZone": "Eastern Standard Time"
    },
    "status": "notStarted",
    "subject": "Shop for children's weekend"

}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update outlooktask",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
