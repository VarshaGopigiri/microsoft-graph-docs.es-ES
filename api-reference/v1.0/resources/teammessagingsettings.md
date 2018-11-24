# <a name="teammessagingsettings-resource-type"></a>tipo de recurso teamMessagingSettings



La configuración de mensajería y menciones en el [equipo](team.md).

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|allowUserEditMessages|Booleano|Si se establece en true, los usuarios puede editar sus mensajes.|
|allowUserDeleteMessages|Booleano|Si se establece en true, los usuarios puede eliminar sus mensajes.|
|allowOwnerDeleteMessages|Booleano|Si se establece en true, propietarios puede eliminar cualquier mensaje.|
|allowTeamMentions|Booleano|Si establece en true, se permiten menciones de @team.|
|allowChannelMentions|Booleano|Si establece en true, se permiten menciones de @channel.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamMessagingSettings"
}-->

```json
{
  "allowUserEditMessages": true,
  "allowUserDeleteMessages": true,
  "allowOwnerDeleteMessages": true,
  "allowTeamMentions": true,
  "allowChannelMentions": true    
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "team's messagingSettings resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
