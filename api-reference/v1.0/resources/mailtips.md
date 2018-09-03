# <a name="mailtips-resource-type"></a>Tipo de recurso mailTips

Mensajes informativos acerca de un destinatario, que se muestran a los usuarios mientras que redactan un mensaje. Por ejemplo, un mensaje de fuera de la oficina como una respuesta automática para un destinatario del mensaje.


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
| automaticReplies | [automaticRepliesMailTips](../resources/automaticrepliesmailtips.md) | Sugerencias por correo para la respuesta automática si el destinatario lo ha configurado. |
| customMailTip | Cadena | Una sugerencia de correo personalizada que se puede configurar en el buzón del destinatario. |
| deliveryRestricted| Booleano | Si el buzón del destinatario está restringido, por ejemplo, si solo acepta mensajes de una lista predefinida de remitentes, rechaza mensajes de una lista predefinida de remitentes o acepta mensajes de solo remitentes autenticados. |
| emailAddress | [emailAddress](../resources/emailaddress.md) | La dirección de correo electrónico del destinatario para recibir sugerencias de correo. |
| error | [mailTipsError](../resources/mailtipserror.md) | Errores que ocurren durante la acción [GetMailTips](../api/user_getmailtips.md). |
| externalMemberCount | Int32 | La cantidad de miembros externos si el destinatario es una lista de distribución. |
| isModerated |Booleano  | Si el envío de mensajes al destinatario requiere aprobación. Por ejemplo, si el destinatario es una gran lista de distribución y se ha configurado un moderador para aprobar los mensajes enviados a esa lista de distribución, o si el envío de mensajes a un destinatario requiere la aprobación del administrador del destinatario. |
| mailboxFull | Booleano | El estado de lleno del buzón del destinatario. |
| maxMessageSize | Int32 | El tamaño máximo de mensaje que se ha configurado para la organización o el buzón del destinatario. |
| recipientScope | Cadena | El ámbito del destinatario. Los valores posibles son: `none`, `internal`, `external`, `externalPartner` y `externalNonParther`. Por ejemplo, un administrador puede establecer que otra organización sea su "socio". El ámbito es útil si un administrador desea que ciertas sugerencias de correo sean accesibles para ciertos ámbitos. También es útil para los remitentes, para informarles de que su mensaje puede salir de la organización y ayudarles a tomar las decisiones correctas sobre la redacción, el tono y el contenido.|
| recipientSuggestions | Colección [recipient](../resources/recipient.md) | Destinatarios sugeridos basados ​​en contextos anteriores donde aparecen en el mismo mensaje. |
| totalMemberCount | Int32 | La cantidad de miembros si el destinatario es una lista de distribución. |

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "automaticReplies",
    "customMailTip",
    "deliveryRestricted",
    "emailAddress",
    "error",
    "externalMemberCount",
    "isModerated",
    "mailboxFull",
    "maxMessageSize",
    "recipientScope",
    "recipientSuggestions",
    "totalMemberCount"
  ],
  "@odata.type": "microsoft.graph.mailTips"
}-->

```json
{
  "automaticReplies": {"@odata.type": "microsoft.graph.automaticRepliesMailTips"},
  "customMailTip": "string",
  "deliveryRestricted": "boolean",
  "emailAddress": {"@odata.type": "microsoft.graph.emailAddress"},
  "error": {"@odata.type": "microsoft.graph.mailTipsError"},
  "externalMemberCount": 1024,
  "isModerated": "boolean",
  "mailboxFull": "boolean",
  "maxMessageSize": 1024,
  "recipientScope": "string",
  "recipientSuggestions": [{"@odata.type": "microsoft.graph.recipient"}],
  "totalMemberCount": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mailtips resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->