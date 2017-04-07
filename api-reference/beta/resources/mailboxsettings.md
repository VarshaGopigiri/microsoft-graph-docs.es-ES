# <a name="mailboxsettings-resource-type"></a>Tipo de recurso mailboxSettings

Configuración del buzón principal del usuario que inició sesión.


## <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|automaticRepliesSetting|[automaticRepliesSetting](automaticrepliessetting.md)|Opciones de configuración para notificar de forma automática al remitente de un mensaje de correo entrante con un mensaje del usuario que ha iniciado sesión.|
|language|[localeInfo](localeinfo.md)|Representación de la configuración regional del usuario, como el idioma preferido y el país o región.|
|timeZone|string|Zona horaria predeterminada para el buzón del usuario.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.mailboxSettings"
}-->

```json
{
  "automaticRepliesSetting": {"@odata.type": "microsoft.graph.automaticRepliesSetting"},
  "language": {"@odata.type": "microsoft.graph.localeInfo"},
  "timeZone": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mailboxSettings resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->