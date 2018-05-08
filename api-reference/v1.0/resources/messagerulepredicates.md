# <a name="messagerulepredicates-resource-type"></a>Tipo de recurso messageRulePredicates


Representa el conjunto de condiciones y excepciones que están disponibles para una regla.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
| bodyContains | Colección (String) | Representa las cadenas que deben aparecer en el cuerpo de un mensaje entrante para que se aplique la condición o excepción. |
| bodyOrSubjectContains | Colección (String) | Representa las cadenas que deben aparecer en el cuerpo o el asunto de un mensaje entrante para que se aplique la condición o excepción. |
| categories | Colección (String) | Representa las categorías con las que debe etiquetarse un mensaje entrante para que se aplique la condición o excepción. |
| fromAddresses | Colección [recipient](recipient.md) | Representa las direcciones de correo electrónico específicas de un de un mensaje entrante para que se aplique la condición o excepción. |
| hasAttachments | Boolean | Indica si un mensaje entrante debe tener datos adjuntos para que se aplique la condición o excepción. |
| headerContains | Colección (String) | Representa las cadenas que deben aparecer en los encabezados de un mensaje entrante para que se aplique la condición o excepción. |
| importance | String | Importancia que se marca en un mensaje entrante para que se aplique la condición o excepción: `low`, `normal` o `high` |
| isApprovalRequest | Boolean | Indica si un mensaje entrante debe ser una solicitud de aprobación para que se aplique la condición o excepción. |
| isAutomaticForward | Boolean | Indica si un mensaje entrante debe reenviarse automáticamente para que se aplique la condición o excepción. |
| isAutomaticReply | Boolean | Indica si un mensaje entrante debe ser una respuesta automática para que se aplique la condición o excepción. |
| isEncrypted | Boolean | Indica si un mensaje entrante debe estar cifrado para que se aplique la condición o excepción. |
| isMeetingRequest | Boolean | Indica si un mensaje entrante debe ser una convocatoria de reunión para que se aplique la condición o excepción. |
| isMeetingResponse | Boolean | Indica si un mensaje entrante debe ser una respuesta a la reunión para que se aplique la condición o excepción. |
| isNonDeliveryReport | Boolean | Indica si un mensaje entrante debe ser un informe de no entrega para que se aplique la condición o excepción. |
| isPermissionControlled | Boolean | Indica si un mensaje entrante debe estar controlado por permisos (protegido por RMS) para que se aplique la condición o excepción. |
| isReadReceipt | Boolean | Indica si un mensaje entrante debe ser una confirmación de lectura para que se aplique la condición o excepción. |
| isSigned | Boolean | Indica si un mensaje entrante debe estar firmado con S/MIME para que se aplique la condición o excepción. |
| isVoicemail | Boolean | Indica si un mensaje entrante debe ser un correo de voz para que se aplique la condición o excepción. |
| messageActionFlag | String  | Representa el valor de marca de acción que aparece en un mensaje entrante para que se aplique la condición o excepción. Los valores posibles son: `any`, `call`, `doNotForward`, `followUp`, `fyi`, `forward`, `noResponseNecessary`, `read`, `reply`, `replyToAll` y `review`. |
| notSentToMe | Boolean | Indica si el propietario del buzón no debe ser un destinatario de un mensaje entrante para que se aplique la condición o excepción. |
| recipientContains | Colección (String) | Representa las cadenas que aparecen en las propiedades **toRecipients** o **ccRecipients** de un mensaje entrante para que se aplique la condición o excepción. |
| senderContains | Colección (String) | Representa las cadenas que aparecen en la propiedad **from** de un mensaje entrante para que se aplique la condición o excepción. |
| sensitivity | String | Representa el nivel de confidencialidad que debe marcarse en un mensaje entrante para que se aplique la condición o excepción. Los valores posibles son: `normal`, `personal`, `private` y `confidential`. |
| sentCcMe | Boolean | Indica si el propietario del buzón debe estar en la propiedad **ccRecipients** de un mensaje entrante para que se aplique la condición o excepción. |
| sentOnlyToMe | Boolean | Indica si el propietario del buzón debe ser el único destinatario de un mensaje entrante para que se aplique la condición o excepción. |
| sentToAddresses | Colección [recipient](recipient.md) | Representa las direcciones de correo electrónico a las que debe enviarse un mensaje entrante para que se aplique la condición o excepción. |
| sentToMe | Boolean | Indica si el propietario del buzón debe estar en la propiedad **toRecipients** de un mensaje entrante para que se aplique la condición o excepción. |
| sentToOrCcMe | Boolean | Indica si el propietario del buzón debe estar en una propiedad **toRecipients** o **ccRecipients** de un mensaje entrante para que se aplique la condición o excepción. |
| subjectContains | Colección (String) | Representa las cadenas que aparecen en el asunto de un mensaje entrante para que se aplique la condición o excepción. |
| withinSizeRange | [sizeRange](sizerange.md) | Especifica los tamaños máximo y mínimo (en kilobytes) en que un mensaje entrante debe estar comprendido para que una condición o excepción se aplique. |



## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
   ],
  "@odata.type": "microsoft.graph.messageRulePredicates"
}-->

```json
{
  "bodyContains": ["String"],
  "bodyOrSubjectContains": ["String"],
  "categories": ["String"],
  "fromAddresses": [{"@odata.type": "microsoft.graph.recipient"}],
  "hasAttachments": "Boolean",
  "headerContains": ["String"],
  "importance": "String",
  "isApprovalRequest": "Boolean",
  "isAutomaticForward": "Boolean",
  "isAutomaticReply": "Boolean",
  "isEncrypted": "Boolean",
  "isMeetingRequest": "Boolean",
  "isMeetingResponse": "Boolean",
  "isNonDeliveryReport": "Boolean",
  "isPermissionControlled": "Boolean",
  "isReadReceipt": "Boolean",
  "isSigned": "Boolean",
  "isVoicemail": "Boolean",
  "messageActionFlag": "String",
  "notSentToMe": "Boolean",
  "recipientContains": ["String"],
  "senderContains": ["String"],
  "sensitivity": "String",
  "sentCcMe": "Boolean",
  "sentOnlyToMe": "Boolean",
  "sentToAddresses": [{"@odata.type": "microsoft.graph.recipient"}],
  "sentToMe": "Boolean",
  "sentToOrCcMe": "Boolean",
  "subjectContains": ["String"],
  "withinSizeRange": {"@odata.type": "microsoft.graph.sizeRange"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "messageRulePredicates resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->