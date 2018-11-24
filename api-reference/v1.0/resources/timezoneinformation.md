# <a name="timezoneinformation-resource-type"></a>Tipo de recurso timeZoneInformation


Representa una zona horaria. El formato admitido es Windows y, cuando se corrija el problema conocido actual, también se admitirá el formato de [zona horaria Internet Assigned Numbers Authority (IANA)](https://www.iana.org/time-zones) (también conocida como "zona horaria Olson").

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|alias|string|Identificador de la zona horaria.|
|displayName|string|Cadena de visualización que representa la zona horaria.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.timeZoneInformation"
}-->

```json
{
  "alias": "string",
  "displayName": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "timeZoneInformation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->