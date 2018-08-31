# <a name="filterdatetime-resource-type"></a>Tipo de recurso FilterDatetime

Representa cómo se filtra una fecha cuando se filtran valores.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|date|cadena|La fecha en formato ISO8601 usada para filtrar los datos.|
|specificity|cadena|Cómo de específica tiene que ser la fecha para mantener los datos. Por ejemplo, si la fecha es 02/04/2005 y el specifity se establece en "mes", la operación de filtrado mantendrá todas las filas con una fecha en el mes de abril de 2009. Los valores posibles son `Year`, `Monday`, `Day`, `Hour`, `Minute` y `Second`.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookFilterDateTime"
}-->

```json
{
  "date": "string",
  "specificity": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "FilterDatetime resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->