# <a name="daylighttimezoneoffset-resource-type"></a>Tipo de recurso daylightTimeZoneOffset

Especifica cuándo una zona horaria cambia de la hora estándar al horario de verano.

Por ejemplo, si se especifica una zona horaria con las propiedades siguientes:

- **bias** es 300.
- **daylightBias** es -100.
- **dayOccurrence** es 4.
- **dayOfWeek** es "Domingo".
- **month** es 5.
- **time** es 02:00:00 y **year** es 0. Esto significa que la hora durante el horario de verano es +300-100 = 200 minutos de antelación a UTC. La transición del horario de verano al estándar se produce todos los años a las 2:00 del cuarto domingo de mayo.


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
| daylightBias | Edm.Int32 | Diferencia horaria con respecto a la hora universal coordinada (UTC) durante el horario de verano. Este valor está en minutos.  |
| dayOccurrence | Edm.Int32 | Representa la enésima repetición del día de la semana en que se produce la transición de la hora estándar al horario de verano. |
| dayOfWeek | string | Representa el día de la semana en el que se produce la transición de la hora estándar al horario de verano. |
| month | Edm.Int32 | Representa el mes del año en el que se produce la transición de la hora estándar al horario de verano. |
| time | Edm.TimeOfDay | Representa la hora del día en la que se produce la transición de la hora estándar al horario de verano. |
| year | Edm.Int32 | Representa la frecuencia en términos de años con que se produce el cambio de la hora estándar al horario de verano. Por ejemplo, un valor 0 significa todos los años.|


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.daylightTimeZoneOffset"
}-->

```json
{
  "daylightBias": "Int32",
  "dayOccurrence": "Int32",
  "dayOfWeek": "string",
  "month": "Int32",
  "time": "TimeOfDay",
  "year": "Int32"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "daylightTimeZoneOffset resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->