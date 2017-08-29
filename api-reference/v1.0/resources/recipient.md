# <a name="recipient-resource-type"></a>Tipo de recurso recipient

Representa información sobre un usuario en la finalización del envío o la recepción de un evento, un mensaje o una publicación de grupo. 

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|emailAddress|[EmailAddress](emailaddress.md)|Dirección de correo del destinatario.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.recipient"
}-->

```json
{
  "emailAddress": {"@odata.type": "microsoft.graph.emailAddress"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "recipient resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->