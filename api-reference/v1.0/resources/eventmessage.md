# <a name="eventmessage-resource-type"></a>tipo de recurso eventMessage

Un mensaje que representa una solicitud de reunión, un mensaje de cancelación de reunión, un mensaje de aceptación de reunión, un mensaje de aceptación provisional de reunión o un mensaje de rechazo de reunión.

Un EventMessage normalmente se encuentra en la carpeta Bandeja de entrada a la que llega cuando un organizador de eventos crea una reunión o cuando un asistente responde a una convocatoria de reunión. Actúe en los mensajes de evento de la misma forma que actúa en el mensaje, con algunas diferencias pequeñas descritas en la tabla siguiente.


## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Obtener eventMessage](../api/eventmessage_get.md) | [eventMessage](eventmessage.md) |Lee las propiedades y las relaciones del objeto eventMessage.|
|[Actualizar](../api/eventmessage_update.md) | [eventMessage](eventmessage.md)  |Actualiza el objeto eventMessage. |
|[Eliminar](../api/message_delete.md) | Ninguno |Elimina el objeto eventMessage. |
|[copy](../api/message_copy.md)|[Mensaje](message.md)|Copia un mensaje a una carpeta.|
|[createForward](../api/message_createforward.md)|[Mensaje](message.md)|Crea un borrador del mensaje que de reenvío. Después puede [actualizar](../api/message_update.md) o [enviar](../api/message_send.md) el borrador.|
|[createReply](../api/message_createreply.md)|[Mensaje](message.md)|Crea un borrador del mensaje de respuesta. Después puede [actualizar](../api/message_update.md) o [enviar](../api/message_send.md) el borrador.|
|[createReplyAll](../api/message_createreplyall.md)|[Mensaje](message.md)|Crea un borrador del mensaje de respuesta a todos. Después puede [actualizar](../api/message_update.md) o [enviar](../api/message_send.md) el borrador.|
|[forward](../api/message_forward.md)|Ninguno|Reenvía un mensaje. El mensaje se guarda en la carpeta Elementos enviados.|
|[move](../api/message_move.md)|[Mensaje](message.md)|Mueve un mensaje a una carpeta. Se crea una nueva copia del mensaje en la carpeta de destino.|
|[reply](../api/message_reply.md)|Ninguno|Responde al remitente de un mensaje. El mensaje se guarda en la carpeta Elementos enviados.|
|[replyAll](../api/message_replyall.md)|Ninguno|Responde a todos los remitentes de un mensaje. El mensaje se guarda en la carpeta Elementos enviados.|
|[send](../api/message_send.md)|Ninguno|Envía un borrador de mensaje creado anteriormente. El mensaje se guarda en la carpeta Elementos enviados.|
|**Datos adjuntos**| | |
|[Enumerar datos adjuntos](../api/eventmessage_list_attachments.md) |Colección [attachment](attachment.md)| Obtener todos los datos adjuntos en un eventMessage.|
|[Agregar datos adjuntos](../api/eventmessage_post_attachments.md) |[Dato adjunto](attachment.md)| Agrega un dato adjunto nuevo a un eventMessage publicándolo en la colección de datos adjuntos.|
|**Extensiones abiertas**| | |
|[Crear extensión abierta](../api/opentypeextension_post_opentypeextension.md) |[openTypeExtension](opentypeextension.md)| Crea una extensión abierta y agrega propiedades personalizadas en una instancia nueva o existente de un recurso.|
|[Obtener extensión abierta](../api/opentypeextension_get.md) |Colección [openTypeExtension](opentypeextension.md)| Obtiene un objeto u objetos de extensión abierta identificados por nombre o por nombre completo.|
|**Propiedades extendidas**| | |
|[Crear propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty_post_singlevalueextendedproperties.md) |[eventMessage](eventMessage.md)  |Crea una o más propiedades extendidas de valor único en un eventMessage nuevo o existente.   |
|[Obtener eventMessage con propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty_get.md)  | [eventMessage](eventMessage.md) | Obtiene eventMessages que contienen una propiedad extendida de valor único mediante el uso de `$expand` o `$filter`. |
|[Crear propiedad extendida de varios valores](../api/multivaluelegacyextendedproperty_post_multivalueextendedproperties.md) | [eventMessage](eventMessage.md) | Crea una o más propiedades extendidas de varios valores en un eventMessage nuevo o existente.  |
|[Obtener eventMessage con propiedad extendida de varios valores](../api/multivaluelegacyextendedproperty_get.md)  | [eventMessage](eventMessage.md) | Obtiene un eventMessage que contiene una propiedad extendida de varios valores mediante el uso de `$expand`. |


## <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|bccRecipients|Colección [recipient](recipient.md)|Los destinatarios Cco: del mensaje.|
|body|[itemBody](itembody.md)|El cuerpo del mensaje. Puede mostrarse en formato de texto o HTML.|
|bodyPreview|String|Los primeros 255 caracteres del cuerpo del mensaje. Se muestran en formato de texto.|
|categories|Colección string|Las categorías asociadas al mensaje.|
|ccRecipients|Colección [recipient](recipient.md)|Los destinatarios Cc: del mensaje.|
|changeKey|String|La versión del mensaje.|
|conversationId|String|El identificador de la conversación a la que pertenece el correo electrónico.|
|createdDateTime|DateTimeOffset|La fecha y la hora de creación del mensaje.|
|from|[recipient](recipient.md)|El propietario del buzón y el remitente del mensaje.|
|hasAttachments|Booleano|Indica si el mensaje tiene datos adjuntos.|
|id|String||
|importance|String| La importancia del mensaje: `Low`, `Normal` y `High`.|
|internetMessageId |String |El identificador del mensaje en el formato especificado por [RFC2822](http://www.ietf.org/rfc/rfc2822.txt). |
|isDeliveryReceiptRequested|Booleano|Indica si se solicita confirmación de lectura para el mensaje.|
|isDraft|Boolean|Indica si el mensaje es un borrador. Un mensaje es un borrador si no se ha enviado todavía.|
|isRead|Booleano|Indica si se ha leído el mensaje.|
|isReadReceiptRequested|Booleano|Indica si se solicita confirmación de lectura para el mensaje.|
|lastModifiedDateTime|DateTimeOffset|La fecha y la hora de la última modificación del mensaje.|
|meetingMessageType|String| El tipo de mensaje de evento: `None`, `MeetingRequest`, `MeetingCancelled`, `MeetingAccepted`, `MeetingTenativelyAccepted`, `MeetingDeclined`.|
|parentFolderId|String|El identificador único para el mailFolder principal del mensaje.|
|receivedDateTime|DateTimeOffset|La fecha y la hora en las que se recibió el mensaje.|
|replyTo|Colección [recipient](recipient.md)|Las direcciones de correo electrónico que se utilizan al responder.|
|sender|[recipient](recipient.md)|La cuenta que se utiliza realmente para generar el mensaje.|
|sentDateTime|DateTimeOffset|La fecha y la hora de envío del mensaje.|
|subject|String|El asunto del mensaje.|
|toRecipients|Colección [recipient](recipient.md)|Los destinatarios Para: del mensaje.|
|uniqueBody|[itemBody](itembody.md)|La parte del cuerpo del mensaje que es única del mensaje actual.|
|webLink|String|La dirección URL para abrir el mensaje en Outlook Web App.<br><br>Puede anexar un argumento ispopout al final de la dirección URL para cambiar cómo se muestra el mensaje. Si ispopout no está presente o se establece en 1, se muestra el mensaje en una ventana emergente. Si ispopout se establece en 0, el navegador mostrará el mensaje en el panel de revisión de Outlook Web App.<br><br>El mensaje se abrirá en el navegador si está conectado a su buzón mediante Outlook Web App. Se le pedirá que inicie sesión si no la ha iniciado ya en el navegador.<br><br>Se puede acceder a esta dirección URL desde un iFrame.|


## <a name="relationships"></a>Relaciones
| Relación | Tipo    |Descripción|
|:---------------|:--------|:----------|
|attachments|Colección [attachment](attachment.md)| Solo lectura. Admite valores NULL.|
|evento|[Evento](event.md)| El evento asociado al mensaje de evento. La hipótesis de los asistentes o los recursos de la sala es que el Supervisor de calendario está configurado para actualizar el calendario automáticamente con un evento cuando lleguen mensajes de eventos de convocatoria de reunión. Propiedad de navegación.  Solo lectura.|
|extensions|Colección [Extension](extension.md)|La colección de extensiones abiertas definidas para el eventMessage. Solo lectura. Admite valores NULL.|
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
  "@odata.type": "microsoft.graph.eventmessage"
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
  "from": {"@odata.type": "microsoft.graph.recipient"},
  "hasAttachments": true,
  "id": "string (identifier)",
  "importance": "String",
  "internetMessageId": "String",
  "isDeliveryReceiptRequested": true,
  "isDraft": true,
  "isRead": true,
  "isReadReceiptRequested": true,
  "lastModifiedDateTime": "String (timestamp)",
  "meetingMessageType": "String",
  "parentFolderId": "string",
  "receivedDateTime": "String (timestamp)",
  "replyTo": [{"@odata.type": "microsoft.graph.recipient"}],
  "sender": {"@odata.type": "microsoft.graph.recipient"},
  "sentDateTime": "String (timestamp)",
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
