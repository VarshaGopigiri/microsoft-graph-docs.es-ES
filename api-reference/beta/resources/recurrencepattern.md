# <a name="recurrencepattern-resource-type"></a>Tipo de recurso recurrencePattern

Frecuencia de un evento.


## <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|dayOfMonth|Int32|Día del mes en que se produce el evento.|
|daysOfWeek|Colección string|Colección de los días de la semana en que se produce el evento. Valores posibles: `Sunday`, `Monday`, `Tuesday`, `Wednesday`, `Thursday`, `Friday`, `Saturday`.|
|firstDayOfWeek|String|Día de la semana en que comienza la periodicidad. Valores posibles: `Sunday`, `Monday`, `Tuesday`, `Wednesday`, `Thursday`, `Friday`, `Saturday`.|
|Index|String|Índice de la semana en que se produce la periodicidad.: `First`, `Second`, `Third`, `Fourth`, `Last`.|
|interval|Int32|Número de unidades de un tipo de periodicidad determinado entre repeticiones.|
|month|Int32|Mes en que se produce el evento.  Se trata de un número entre 1 y 12.|
|type|String|Tipo de patrón de periodicidad: `Daily`, `Weekly`, `AbsoluteMonthly`, `RelativeMonthly`, `AbsoluteYearly`, `RelativeYearly`.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.recurrencepattern"
}-->

```json
{
  "dayOfMonth": 1024,
  "daysOfWeek": ["String"],
  "firstDayOfWeek": "String",
  "index": "String",
  "interval": 1024,
  "month": 1024,
  "type": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "recurrencePattern resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->