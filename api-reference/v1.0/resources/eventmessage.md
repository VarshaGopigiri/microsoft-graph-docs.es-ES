---
title: tipo de recurso eventMessage
description: 'Un mensaje que representa una convocatoria, una cancelación o una respuesta de reunión (puede ser uno de los siguientes: aceptación, aceptación provisional o rechazo).'
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: e6effa3f97b0625786ec999f1b478c3dd8530f52
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27917730"
---
# <a name="eventmessage-resource-type"></a>tipo de recurso eventMessage

Un mensaje que representa una convocatoria, una cancelación o una respuesta de reunión (puede ser uno de los siguientes: aceptación, aceptación provisional o rechazo).

La entidad **eventMessage** se deriva de [message](message.md). La propiedad **meetingMessageType** identifica el tipo de mensaje de evento.

Cuando un organizador o aplicación envía una convocatoria de reunión, esta llega a la bandeja de entrada del asistente como instancia **eventMessage** con el **meetingMessageType** de **meetingRequest**. Además, Outlook crea automáticamente una instancia **event** en el calendario del asistente con la propiedad **showAs** como **provisional**. 

Para obtener las propiedades del evento asociado en el buzón del asistente, la aplicación puede usar la propiedad de navegación de **evento** del **eventMessage**, tal y como se muestra en este [ejemplo de obtención de un mensaje de evento](../api/eventmessage-get.md#request-2). La aplicación también puede responder al evento en nombre de los asistentes mediante programación, por [Aceptar](../api/event-accept.md), [Aceptar provisionalmente](../api/event-tentativelyaccept.md)o [Rechazar](../api/event-decline.md) el evento.

Aparte de una convocatoria de reunión, una instancia de **eventMessage** puede encontrarse en la carpeta de bandeja de entrada de un asistente como resultado de un organizador de eventos cancelar una reunión o en bandeja de entrada del organizador de la como consecuencia de un asistente que responde a la convocatoria de reunión. Una aplicación puede actuar con los mensajes de evento casi de la misma forma que con los mensajes.

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Obtener eventMessage](../api/eventmessage-get.md) | [eventMessage](eventmessage.md) |Lee las propiedades y las relaciones del objeto eventMessage.|
|[Actualizar](../api/eventmessage-update.md) | [eventMessage](eventmessage.md)  |Actualiza el objeto eventMessage. |
|[Eliminar](../api/message-delete.md) | Ninguno |Elimina el objeto eventMessage. |
|[copy](../api/message-copy.md)|[message](message.md)|Copia un mensaje a una carpeta.|
|[createForward](../api/message-createforward.md)|[message](message.md)|Crea un borrador del mensaje de reenvío. Después puede [actualizar](../api/message-update.md) o [enviar](../api/message-send.md) el borrador.|
|[createReply](../api/message-createreply.md)|[message](message.md)|Crea un borrador del mensaje de respuesta. Después puede [actualizar](../api/message-update.md) o [enviar](../api/message-send.md) el borrador.|
|[createReplyAll](../api/message-createreplyall.md)|[message](message.md)|Crea un borrador del mensaje de respuesta a todos. Después puede [actualizar](../api/message-update.md) o [enviar](../api/message-send.md) el borrador.|
|[forward](../api/message-forward.md)|Ninguno|Reenvía un mensaje. El mensaje se guarda en la carpeta Elementos enviados.|
|[move](../api/message-move.md)|[message](message.md)|Mueve un mensaje a una carpeta. Se crea una nueva copia del mensaje en la carpeta de destino.|
|[reply](../api/message-reply.md)|Ninguno|Responde al remitente de un mensaje. El mensaje se guarda en la carpeta Elementos enviados.|
|[replyAll](../api/message-replyall.md)|Ninguno|Responde a todos los remitentes de un mensaje. El mensaje se guarda en la carpeta Elementos enviados.|
|[send](../api/message-send.md)|Ninguno|Envía un borrador de mensaje creado anteriormente. El mensaje se guarda en la carpeta Elementos enviados.|
|**Datos adjuntos**| | |
|[Enumerar datos adjuntos](../api/eventmessage-list-attachments.md) |Colección de [datos adjuntos](attachment.md)| Obtiene todos los datos adjuntos en un eventMessage.|
|[Agregar datos adjuntos](../api/eventmessage-post-attachments.md) |[attachment](attachment.md)| Agrega datos adjuntos nuevos a un eventMessage al publicarlos en la colección de datos adjuntos.|
|**Extensiones abiertas**| | |
|[Crear extensión abierta](../api/opentypeextension-post-opentypeextension.md) |[openTypeExtension](opentypeextension.md)| Crea una extensión abierta y agrega propiedades personalizadas en una instancia nueva o existente de un recurso.|
|[Obtener extensión abierta](../api/opentypeextension-get.md) |Colección [openTypeExtension](opentypeextension.md)| Obtiene un objeto u objetos de extensión abierta identificados por nombre o por nombre completo.|
|**Propiedades extendidas**| | |
|[Crear propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty-post-singlevalueextendedproperties.md) |[eventMessage](eventmessage.md)  |Crea una o más propiedades extendidas de valor único en un eventMessage nuevo o existente.   |
|[Obtener eventMessage con propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty-get.md)  | [eventMessage](eventmessage.md) | Obtiene eventMessages que contienen una propiedad extendida de valor único mediante el uso de `$expand` o `$filter`. |
|[Crear propiedad extendida de varios valores](../api/multivaluelegacyextendedproperty-post-multivalueextendedproperties.md) | [eventMessage](eventmessage.md) | Crea una o más propiedades extendidas de varios valores en un eventMessage nuevo o existente.  |
|[Obtener eventMessage con propiedad extendida de varios valores](../api/multivaluelegacyextendedproperty-get.md)  | [eventMessage](eventmessage.md) | Obtiene un eventMessage que contiene una propiedad extendida de varios valores mediante el uso de `$expand`. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|bccRecipients|Colección [recipient](recipient.md)|Los destinatarios Cco: del mensaje.|
|body|[itemBody](itembody.md)|El cuerpo del mensaje. Puede mostrarse en formato de texto o HTML.|
|bodyPreview|Cadena|Los primeros 255 caracteres del cuerpo del mensaje. Se muestran en formato de texto.|
|categories|Colección String|Las categorías asociadas al mensaje.|
|ccRecipients|Colección [recipient](recipient.md)|Los destinatarios Cc: del mensaje.|
|changeKey|Cadena|La versión del mensaje.|
|conversationId|Cadena|El identificador de la conversación a la que pertenece el correo electrónico.|
|createdDateTime|DateTimeOffset|La fecha y la hora de creación del mensaje.|
|flag|[followupFlag](followupflag.md)|Valor de marca que indica el estado, la fecha de inicio, la fecha de vencimiento o la fecha de finalización del mensaje.|
|from|[recipient](recipient.md)|El propietario del buzón y el remitente del mensaje.|
|hasAttachments|Booleano|Indica si el mensaje tiene datos adjuntos.|
|id|String|Identificador único para el mensaje de evento (tenga en cuenta que si se mueve o se modifica un mensaje, puede cambiar este valor)|
|importance|String| La importancia del mensaje: `low`, `normal` y `high`.|
|inferenceClassification|Cadena| Los valores posibles son: `focused`, `other`.|
|internetMessageHeaders | Colección [internetMessageHeader](internetmessageheader.md) | Colección de encabezados de mensajes, definidos por [RFC5322](https://www.ietf.org/rfc/rfc5322.txt), que proporcionan los detalles de la ruta en la red que sigue un mensaje desde el remitente hasta el destinatario. Solo lectura.|
|internetMessageId |String |El identificador del mensaje en el formato especificado por [RFC2822](https://www.ietf.org/rfc/rfc2822.txt). |
|isDeliveryReceiptRequested|Boolean|Indica si se solicita confirmación de lectura para el mensaje.|
|isDraft|Booleano|Indica si el mensaje es un borrador. Un mensaje es un borrador si no se ha enviado todavía.|
|isRead|Booleano|Indica si se ha leído el mensaje.|
|isReadReceiptRequested|Booleano|Indica si se solicita confirmación de lectura para el mensaje.|
|lastModifiedDateTime|DateTimeOffset|La fecha y la hora de la última modificación del mensaje.|
|meetingMessageType|meetingMessageType| El tipo de mensaje de evento: `none`, `meetingRequest`, `meetingCancelled`, `meetingAccepted`, `meetingTenativelyAccepted`, `meetingDeclined`.|
|parentFolderId|Cadena|El identificador único para el mailFolder principal del mensaje.|
|receivedDateTime|DateTimeOffset|La fecha y la hora en las que se recibió el mensaje.|
|replyTo|Colección [recipient](recipient.md)|Las direcciones de correo electrónico que se utilizan al responder.|
|sender|[recipient](recipient.md)|La cuenta que se utiliza realmente para generar el mensaje.|
|sentDateTime|DateTimeOffset|La fecha y la hora de envío del mensaje.|
|subject|Cadena|El asunto del mensaje.|
|toRecipients|Colección [recipient](recipient.md)|Los destinatarios Para: del mensaje.|
|uniqueBody|[itemBody](itembody.md)|La parte del cuerpo del mensaje que es única del mensaje actual.|
|webLink|Cadena|La dirección URL para abrir el mensaje en Outlook Web App.<br><br>Puede anexar un argumento ispopout al final de la dirección URL para cambiar cómo se muestra el mensaje. Si ispopout no está presente o se establece en 1, se muestra el mensaje en una ventana emergente. Si ispopout se establece en 0, el navegador mostrará el mensaje en el panel de revisión de Outlook Web App.<br><br>El mensaje se abrirá en el navegador si está conectado a su buzón mediante Outlook Web App. Se le pedirá que inicie sesión si no la ha iniciado ya en el navegador.<br><br>Se puede acceder a esta dirección URL desde un iFrame.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|attachments|Colección de [datos adjuntos](attachment.md)| Solo lectura. Admite valores NULL.|
|evento|[event](event.md)| El evento asociado al mensaje de evento. La hipótesis de los asistentes o los recursos de la sala es que el Supervisor de calendario está configurado para actualizar el calendario automáticamente con un evento cuando lleguen mensajes de eventos de convocatoria de reunión. Propiedad de navegación.  Solo lectura.|
|extensions|Colección de [extensiones](extension.md)|La colección de extensiones abiertas definidas para el eventMessage. Solo lectura. Admite valores NULL.|
|multiValueExtendedProperties|Colección [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md)| La colección de propiedades extendidas de varios valores definidas para el eventMessage. Solo lectura. Admite valores NULL.|
|singleValueExtendedProperties|Colección [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md)| La colección de propiedades extendidas de valor único definidas para el eventMessage. Solo lectura. Admite valores NULL.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso  

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "attachments",
    "event",
    "extensions",
    "multiValueExtendedProperties",
    "singleValueExtendedProperties"
  ],
  "baseType": "microsoft.graph.message",
  "@odata.type": "microsoft.graph.eventMessage",
  "@odata.annotations": [
    {
      "property": "event",
      "capabilities": {
        "changeTracking": false,
        "deletable": false,
        "insertable": false,
        "searchable": false,
        "updatable": false
      }
    }
  ]
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
  "createdDateTime": "DateTimeOffset",
  "event": { "@odata.type": "microsoft.graph.event" },
  "flag": {"@odata.type": "microsoft.graph.followupFlag"},
  "from": {"@odata.type": "microsoft.graph.recipient"},
  "hasAttachments": true,
  "id": "string (identifier)",
  "importance": "String",
  "inferenceClassification": "String",
  "internetMessageHeaders": [{"@odata.type": "microsoft.graph.internetMessageHeader"}],
  "internetMessageId": "String",
  "isDeliveryReceiptRequested": true,
  "isDraft": true,
  "isRead": true,
  "isReadReceiptRequested": true,
  "lastModifiedDateTime": "DateTimeOffset",
  "meetingMessageType": "String",
  "parentFolderId": "string",
  "receivedDateTime": "DateTimeOffset",
  "replyTo": [{"@odata.type": "microsoft.graph.recipient"}],
  "sender": {"@odata.type": "microsoft.graph.recipient"},
  "sentDateTime": "DateTimeOffset",
  "subject": "string",
  "toRecipients": [{"@odata.type": "microsoft.graph.recipient"}],
  "uniqueBody": {"@odata.type": "microsoft.graph.itemBody"},
  "webLink": "string"
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "eventMessage resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
