# <a name="recurrencerange-resource-type"></a>Tipo de recurso recurrenceRange

Duración de un evento.

## <a name="properties"></a>Propiedades

| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|endDate|Date|Fecha de finalización de la serie.|
|numberOfOccurrences|Int32|Número de veces que se repite el evento.|
|recurrenceTimeZone|String |Zona horaria de las propiedades **startDate** y **endDate**. |
|startDate|Date|Fecha de inicio de la tarea.|
|type|String|Intervalo de periodicidad: EndDate = 0, NoEnd = 1, Numbered = 2. Valores posibles: `EndDate`, `NoEnd`, `Numbered`.||

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.recurrencerange"
}-->

```json
{
  "endDate": "String (timestamp)",
  "numberOfOccurrences": 1024,
  "recurrenceTimeZone": "string",
  "startDate": "String (timestamp)",
  "type": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "recurrenceRange resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
