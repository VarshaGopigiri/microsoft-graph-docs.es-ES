---
title: 'outlookTask: completa'
description: 'Completar una tarea de Outlook que establece la propiedad **completedDateTime** a la fecha actual, '
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: 966f5c2a6d429169cff3bd6746ebb0bace34ad15
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27979638"
---
# <a name="outlooktask-complete"></a>outlookTask: completa

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Completar una tarea de Outlook que establece la propiedad **completedDateTime** a la fecha actual y la propiedad **status** para `completed`.

Si se está realizando una tarea en una serie periódica, en la respuesta, la colección de tareas contendrá la tarea completada en la serie y la siguiente tarea de la serie.

La propiedad **completedDateTime** representa la fecha cuando termina la tarea. La parte de **completedDateTime** la hora se establece en medianoche UTC de forma predeterminada.

De forma predeterminada, esta operación (y las operaciones de tarea de revisión, GET y POST) devuelve propiedades relacionadas con la fecha en UTC. Puede usar el `Prefer: outlook.timezone` encabezado para que todas las propiedades relacionadas con la fecha en la respuesta representada en una zona horaria diferente a la hora UTC.

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
POST /me/outlook/tasks/{id}/complete
POST /users/{id|userPrincipalName}/outlook/tasks/{id}/complete
```

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre       | Descripción|
|:---------------|:----------|
| Authorization  | {token} de portador. Obligatorio. |
| Prefer: outlook.timezone | Especifica la zona horaria de propiedades de tiempo en la respuesta, que sería en UTC si no se especifica este encabezado. Opcional.|

## <a name="request-body"></a>Cuerpo de la solicitud

No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve `200 OK` código de respuesta y el objeto [outlookTask](../resources/outlooktask.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se marca la tarea como completada especificada. Especifica la hora estándar del Pacífico (PST) en el `Prefer: outlook.timezone` encabezado.

### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "outlooktask_complete"
}-->

```http
POST https://graph.microsoft.com/beta/me/tasks('AAMkADA1MT15rfAAA=')/complete
Prefer: outlook.timezone="Pacific Standard Time"
```

### <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta. El **completedDateTime** y otras propiedades relacionadas con la fecha en la respuesta se expresan en PST.

> **Nota:** Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán desde una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.outlookTask",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 465

{
  "value": [
    {
      "id": "AAMkADA1MT15rfAAA=",
      "createdDateTime": "2016-04-21T22:44:01.2012012-07:00",
      "lastModifiedDateTime": "2016-04-22T19:28:38.5300447-07:00",
      "changeKey": "1/KC9Vmu40G3DwB6Lgs7MAAAIW9XYQ==",
      "categories": [
      ],
      "assignedTo": null,
      "body": {
          "contentType": "text",
          "content": ""
      },
      "completedDateTime": {
          "dateTime": "2016-04-22T00:00:00.0000000",
          "timeZone": "Pacific Standard Time"
      },
      "dueDateTime": {
          "dateTime": "2016-04-25T00:00:00.0000000",
          "timeZone": "Pacific Standard Time"
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
          "dateTime": "2016-04-21T00:00:00.0000000",
          "timeZone": "Pacific Standard Time"
      },
      "status": "completed",
      "subject": "Shop for dinner"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "outlookTask: complete",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
