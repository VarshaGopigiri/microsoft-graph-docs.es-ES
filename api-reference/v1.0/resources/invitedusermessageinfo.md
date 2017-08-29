# <a name="configuring-the-invitation-message"></a>Configurar el mensaje de invitación

El objeto invitedUserMessageInfo le permite configurar el mensaje de [invitación](invitation.md).


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|ccRecipients|[Recipient](recipient.md)|Destinatarios adicionales a los que se debe enviar el mensaje de invitación. Actualmente se admite solo 1 destinatario adicional.|
|customizedMessageBody|String|Cuerpo del mensaje personalizado que quiere enviar si no quiere el mensaje predeterminado.|
|messageLanguage|String|El idioma en el que quiere enviar el mensaje predeterminado. Si se especifica el customizedMessageBody, esta propiedad se omite y el mensaje se envía con el customizedMessageBody. El formato de idioma debe estar en ISO 639. El valor predeterminado es en-US.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso

<!-- {"blockType": "resource", "@odata.type": "microsoft.graph.invitedUserMessageInfo"} -->
```json
{
  "ccRecipients": [ {"@odata.type": "microsoft.graph.recipient"} ],
  "customizedMessageBody": "string",
  "messageLanguage": "string"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2016-22-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "invitedUserMessageInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
