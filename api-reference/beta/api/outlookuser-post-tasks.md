---
title: Crear outlookTask
description: Crear una tarea de Outlook en el grupo de tarea predeterminado (`My Tasks`) y la carpeta de tareas predeterminada (`Tasks`) en el buzón del usuario.
localization_priority: Normal
ms.openlocfilehash: c158af6ac5125bb410bcbe57a1cb26b8cd955e28
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27853742"
---
# <a name="create-outlooktask"></a>Crear outlookTask

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Crear una tarea de Outlook en el grupo de tarea predeterminado (`My Tasks`) y la carpeta de tareas predeterminada (`Tasks`) en el buzón del usuario.

El método POST siempre omite la parte de tiempo de **startDateTime** y **dueDateTime** en el cuerpo de la solicitud y supone el tiempo para que siempre se medianoche en la zona horaria especificada.

De forma predeterminada, esta operación (y las operaciones de tarea GET, revisión y [completar](../api/outlooktask-complete.md) ) devuelve propiedades relacionadas con la fecha en UTC. Puede usar el `Prefer: outlook.timezone` encabezado para que todas las propiedades relacionadas con la fecha en la respuesta representada en una zona horaria diferente a la hora UTC.

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
POST /users/{id|userPrincipalName}/outlook/tasks
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Descripción|
|:---------------|:----------|
| Authorization  | {token} de portador. Obligatorio. |
| Prefer: outlook.timezone | Especifica la zona horaria de propiedades de tiempo en la respuesta, que sería en UTC si no se especifica este encabezado. Opcional.|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [outlookTask](../resources/outlooktask.md) .

## <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve `201 Created` objeto de código y [outlookTask](../resources/outlooktask.md) de respuesta en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
En el ejemplo siguiente se muestra el uso de la `Prefer: outlook.timezone` encabezado. Crea una tarea, expresa **startDateTime** y **dueDateTime** en la hora estándar (EST) e incluye un `Prefer` encabezado de hora estándar del Pacífico (PST).
<!-- {
  "blockType": "request",
  "name": "create_outlooktask_from_outlookuser"
}-->
```http
POST https://graph.microsoft.com/beta/me/outlook/tasks
Prefer: outlook.timezone="Pacific Standard Time"
Content-type: application/json
Content-length: 276

{
  "assignedTo": "Dana Swope",
  "subject": "Shop for children's weekend",
  "startDateTime": {
      "dateTime": "2016-05-03T09:00:00",
      "timeZone": "Eastern Standard Time"
  },
  "dueDateTime":  {
      "dateTime": "2016-05-05T16:00:00",
      "timeZone": "Eastern Standard Time"
  }
}
```
En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [outlookTask](../resources/outlooktask.md) .
##### <a name="response"></a>Respuesta
El método POST omite la parte de tiempo de **startDateTime** y **dueDateTime** en el cuerpo de la solicitud y se da por supuesto la hora a estar siempre medianoche en la zona horaria especificada (EST).

Dado que el `Prefer` encabezado especifica PST, el método POST expresa todas las propiedades relacionadas con la fecha en la respuesta en PST. En concreto, para las propiedades **startDateTime** y **dueDateTime** , el método POST convierte medianoche en EST a PST y devuelve en PST en la respuesta.

Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.outlookTask"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 576

{
  "id": "AAMkADA1MHgwAAA=",
  "createdDateTime": "2016-04-22T15:19:18.9526004-07:00",
  "lastModifiedDateTime": "2016-04-22T15:19:19.015101-07:00",
  "changeKey": "1/KC9Vmu40G3DwB6Lgs7MAAAIW9XXA==",
  "categories": [ ],
  "assignedTo": "Dana Swope",
  "body": {
    "contentType": "Text",
    "content": ""
  },
  "completedDateTime": null,
  "dueDateTime": {
    "dateTime": "2016-05-04T021:00:00.0000000",
    "timeZone": "Pacific Standard Time"
  },
  "hasAttachments":false,
  "importance": "normal",
  "isReminderOn": false,
  "owner": "Administrator",
  "parentFolderId": "AQMkADA1MTEgAAAA==",
  "recurrence": null,
  "reminderDateTime": null,
  "sensitivity": "Normal",
  "startDateTime": {
    "dateTime": "2016-05-02T21:00:00.0000000",
    "timeZone": "Pacific Standard Time"
  },
  "status": "notStarted",
  "subject": "Shop for children's weekend"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create outlookTask",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
