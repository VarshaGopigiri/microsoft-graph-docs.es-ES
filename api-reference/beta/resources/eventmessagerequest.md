---
title: tipo de recurso eventMessageRequest
description: Un mensaje que representa una convocatoria de reunión.
ms.openlocfilehash: b63778d868000c57d8a900b67d0554c6f6bef2bd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089065"
---
# <a name="eventmessagerequest-resource-type"></a>tipo de recurso eventMessageRequest

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Un mensaje que representa una convocatoria de reunión.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "attachments",
    "event",
    "extensions",
    "previousLocation",
    "previousStartDateTime",
    "previousEndDateTime"
  ],
  "@odata.type": "microsoft.graph.eventMessageRequest"
}-->

```json
{
  "bccRecipients": [{"@odata.type": "microsoft.graph.recipient"}],
  "body": {"@odata.type": "microsoft.graph.itemBody"},
  "bodyPreview": "string",
  "categories": ["string"],
  "ccRecipients": [{"@odata.type": "microsoft.graph.recipient"}],
  "changeKey": "string",
  "conversationId": "string",
  "createdDateTime": "String (timestamp)",
  "endDateTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "from": {"@odata.type": "microsoft.graph.recipient"},
  "hasAttachments": true,
  "id": "string (identifier)",
  "importance": "String",
  "inferenceClassification": "String",
  "isDeliveryReceiptRequested": true,
  "isDraft": true,
  "isOutOfDate": "Boolean",
  "isRead": true,
  "isReadReceiptRequested": true,
  "lastModifiedDateTime": "String (timestamp)",
  "location": {"@odata.type": "microsoft.graph.location"},
  "meetingMessageType": "microsoft.graph.meetingMessageType",
  "parentFolderId": "string",
  "previousEndDateTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "previousLocation": {"@odata.type": "microsoft.graph.location"},
  "previousStartDateTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "receivedDateTime": "String (timestamp)",
  "recurrence": {"@odata.type": "microsoft.graph.patternedRecurrence"},
  "replyTo": [{"@odata.type": "microsoft.graph.recipient"}],
  "sender": {"@odata.type": "microsoft.graph.recipient"},
  "sentDateTime": "String (timestamp)",
  "startDateTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "subject": "string",
  "toRecipients": [{"@odata.type": "microsoft.graph.recipient"}],
  "type": "string",
  "uniqueBody": {"@odata.type": "microsoft.graph.itemBody"},
  "webLink": "string"
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|bccRecipients|Colección [recipient](recipient.md)|Los destinatarios Cco: del mensaje.|
|body|[itemBody](itembody.md)|El cuerpo del mensaje.|
|bodyPreview|String|Los primeros 255 caracteres del cuerpo del mensaje.|
|categories|Colección String|Las categorías asociadas al mensaje.|
|ccRecipients|Colección [recipient](recipient.md)|Los destinatarios Cc: del mensaje.|
|changeKey|String|La versión del mensaje.|
|conversationId|String|El identificador de la conversación a la que pertenece el correo electrónico.|
|createdDateTime|DateTimeOffset|La fecha y la hora de creación del mensaje.|
|endDateTime|[DateTimeTimeZone](datetimetimezone.md)|La hora de finalización de la reunión solicitada.|
|from|[recipient](recipient.md)|El propietario del buzón y el remitente del mensaje.|
|hasAttachments|Booleano|Indica si el mensaje tiene datos adjuntos.|
|id|String|Solo lectura.|
|importance|String| La importancia del mensaje: `Low`, `Normal` y `High`.|
|inferenceClassification|String| Los valores posibles son: `Focused` y `Other`.|
|isDeliveryReceiptRequested|Booleano|Indica si se solicita confirmación de lectura para el mensaje.|
|isDraft|Booleano|Indica si el mensaje es un borrador. Un mensaje es un borrador si no se ha enviado todavía.|
|isOutOfDate|Booleano|Indica si esta solicitud de reunión se ha realizado obsoleta por una solicitud más reciente.|
|isRead|Booleano|Indica si se ha leído el mensaje.|
|isReadReceiptRequested|Booleano|Indica si se solicita confirmación de lectura para el mensaje.|
|lastModifiedDateTime|DateTimeOffset|La fecha y la hora de la última modificación del mensaje.|
|location|[Location](location.md)|La ubicación de la reunión solicitada.|
|meetingMessageType|String| El tipo de mensaje de evento: `None`, `MeetingRequest`, `MeetingCancelled`, `MeetingAccepted`, `MeetingTenativelyAccepted`, `MeetingDeclined`.|
|parentFolderId|String|El identificador único para el mailFolder principal del mensaje.|
|previousEndDateTime|[DateTimeTimeZone](datetimetimezone.md)|La hora de finalización anterior de la reunión solicitada.|
|previousLocation|[Ubicación](location.md)|La ubicación anterior de la reunión solicitada.|
|previousStartDateTime|[DateTimeTimeZone](datetimetimezone.md)|La hora de inicio anterior de la reunión solicitada.|
|receivedDateTime|DateTimeOffset|La fecha y la hora en las que se recibió el mensaje.|
|recurrence|[PatternedRecurrence](patternedrecurrence.md)|El patrón de periodicidad de la reunión solicitada.|
|replyTo|Colección [recipient](recipient.md)|Las direcciones de correo electrónico que se utilizan al responder.|
|sender|[recipient](recipient.md)|La cuenta que se utiliza realmente para generar el mensaje.|
|sentDateTime|DateTimeOffset|La fecha y la hora de envío del mensaje.|
|startDateTime|[DateTimeTimeZone](datetimetimezone.md)|La hora de inicio de la reunión solicitada.|
|subject|String|El asunto del mensaje.|
|toRecipients|Colección [recipient](recipient.md)|Los destinatarios Para: del mensaje.|
|type|String|El tipo de reunión solicitada: `singleInstance`, `occurence`, `exception`, `seriesMaster`.|
|uniqueBody|[itemBody](itembody.md)|La parte del cuerpo del mensaje que es única del mensaje actual.|
|webLink|String|La dirección URL para abrir el mensaje en Outlook Web App.<br><br>Puede anexar un argumento ispopout al final de la dirección URL para cambiar cómo se muestra el mensaje. Si ispopout no está presente o se establece en 1, se muestra el mensaje en una ventana emergente. Si ispopout se establece en 0, el navegador mostrará el mensaje en el panel de revisión de Outlook Web App.<br><br>El mensaje se abrirá en el navegador si está conectado a su buzón mediante Outlook Web App. Se le pedirá que inicie sesión si no la ha iniciado ya en el navegador.<br><br>Se puede acceder a esta dirección URL desde un iFrame.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|attachments|Colección [attachment](attachment.md)| Solo lectura. Admite valores NULL.|
|evento|[Evento](event.md)| El evento asociado al mensaje de evento. La hipótesis de los asistentes o los recursos de la sala es que el Supervisor de calendario está configurado para actualizar el calendario automáticamente con un evento cuando lleguen mensajes de eventos de convocatoria de reunión. Propiedad de navegación.  Solo lectura.|
|extensions|Colección [Extension](extension.md)| Solo lectura. Admite valores NULL.|

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener eventMessage](../api/eventmessage-get.md) | [eventMessage](eventmessage.md) |Lee las propiedades y las relaciones del objeto eventMessage.|
|[Crear datos adjuntos](../api/eventmessage-post-attachments.md) |[Dato adjunto](attachment.md)| Crea un dato adjunto nuevo publicándolo en la colección de datos adjuntos.|
|[Enumerar datos adjuntos](../api/eventmessage-list-attachments.md) |Colección [attachment](attachment.md)| Obtiene una colección de objetos de datos adjuntos.|
|[Actualizar](../api/eventmessage-update.md) | [eventMessage](eventmessage.md)  |Actualiza el objeto eventMessage. |
|[Eliminar](../api/eventmessage-delete.md) | Ninguno |Elimina el objeto eventMessage. |
|[copy](../api/message-copy.md)|[Mensaje](message.md)||
|[createForward](../api/message-createforward.md)|[Mensaje](message.md)||
|[createReply](../api/message-createreply.md)|[Mensaje](message.md)||
|[createReplyAll](../api/message-createreplyall.md)|[Mensaje](message.md)||
|[forward](../api/message-forward.md)|Ninguno|Reenvía un mensaje. A continuación, se guarda el mensaje en la carpeta Elementos enviados.|
|[move](../api/message-move.md)|[Mensaje](message.md)|Mover el mensaje a un mailFolder.|
|[reply](../api/message-reply.md)|Ninguno|Respuestas al remitente de un mensaje. A continuación, se guarda el mensaje en la carpeta Elementos enviados.|
|[replyAll](../api/message-replyall.md)|Ninguno|Responde a todos los remitentes de un mensaje. El mensaje se guarda en la carpeta Elementos enviados.|
|[send](../api/message-send.md)|Ninguno|Envía un borrador de mensaje creado anteriormente. El mensaje se guarda en la carpeta Elementos enviados.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "eventMessageRequest resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
