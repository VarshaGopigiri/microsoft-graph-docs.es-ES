# <a name="localeinfo-resource-type"></a>Tipo de recurso localeInfo

Información sobre la configuración regional, como el idioma preferido y el país o región del usuario que inició sesión.


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|configuración regional|string|Representación de la configuración regional del usuario, que incluye el idioma preferido y el país o región del usuario. Por ejemplo, "es-es". El componente de idioma sigue códigos de dos letras, tal y como se define en [ISO 639-1](https://www.iso.org/iso/home/standards/language_codes.htm), y el componente de país sigue códigos de dos letras, tal y como se define en [ISO 3166-1 alpha-2](https://www.iso.org/iso/country_codes.htm).|
|displayName|string|Nombre que representa la configuración regional del usuario en lenguaje natural, por ejemplo, "Inglés (Estados Unidos)".|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.localeInfo"
}-->

```json
{
  "locale": "string",
  "displayName": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "localeInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->