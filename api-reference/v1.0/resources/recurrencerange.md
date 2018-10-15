# <a name="recurrencerange-resource-type"></a>Tipo de recurso recurrenceRange

Describe un intervalo de fechas durante el que se repite un [evento](event.md) periódico. 

Puede especificar el intervalo de fechas para un evento periódico de tres maneras según su situación. Aunque siempre debe especificar un valor **startDate** para el intervalo de fechas, puede especificar un evento periódico que finaliza en una fecha específica, que no termina o que finaliza tras un número específico de repeticiones. Tenga en cuenta que las repeticiones reales dentro del intervalo de fechas siempre seguirán el patrón de periodicidad que especifique para el evento periódico. Un evento periódico siempre se define por su valor [recurrencePattern](recurrencepattern.md) (con qué frecuencia se repite el evento) y su valor **recurrenceRange** (durante cuánto tiempo se repite el evento).

## <a name="properties"></a>Propiedades

| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|endDate|Fecha|Fecha en la que se detiene la aplicación del patrón de periodicidad. Según el patrón de periodicidad del evento, la última repetición de la reunión no puede ser esta fecha. Se requiere si **type** es `endDate`.|
|numberOfOccurrences|Int32|Número de veces que se repite el evento. Se requiere y debe ser positivo si **type** es `numbered`.|
|recurrenceTimeZone|Cadena |Zona horaria de las propiedades **startDate** y **endDate**. Opcional. Si no se especifica, se usa la zona horaria del evento.|
|startDate|Fecha|Fecha en la que se inicia la aplicación del patrón de periodicidad. La primera repetición de la reunión puede ser esta fecha o una posterior, en función del patrón de periodicidad del evento. Debe ser el mismo valor que la propiedad **start** del [evento](event.md) periódico. Obligatorio.|
|type|recurrenceRangeType|Intervalo de periodicidad. Los valores posibles son: `endDate`, `noEnd` y `numbered`. Obligatorio.|

Use la propiedad **type** para especificar los diferentes tipos de **recurrenceRange**. Tenga en cuenta las propiedades necesarias para cada tipo, tal como se describe en la tabla siguiente.

| Propiedad type  | Tipo de intervalo de frecuencia | Descripción | Ejemplo | Propiedades requeridas |
|:-------|:---------------|:--------|:--------|:--------|
|`endDate` |Rango con fecha final | El evento se repetirá durante todos los días que formen parte del patrón de frecuencia correspondiente, entre los valores **startDate** y **endDate**, ambos incluidos. | Repite el evento en el intervalo de fechas entre el 1 de junio de 2017 y el 15 de junio de 2017. | **type**, **startDate**, **endDate** | 
|`noEnd`  |Intervalo sin fecha final | El evento se repetirá todos los días que formen parte del patrón de frecuencia correspondiente, que empieza el **startDate**. | Repite indefinidamente el evento en el intervalo de fechas a partir del 1 de junio de 2017. | **type**, **startDate** |
|`numbered`|Intervalo con un número de repeticiones concreto | El evento se repite según el valor **numberOfOccurrences**, que se basa en el patrón de frecuencia que empieza en el momento especificado en **startDate**. | Repita el evento 10 veces en el intervalo de fechas a partir del 1 de junio de 2017.  | **type**, **startDate**, **numberOfOccurrences** |


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.recurrenceRange"
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
  "suppressions": [
      "Warning: /api-reference/v1.0/resources/recurrencerange.md:
      Failed to parse any rows out of table with headers: | type property  | Type of recurrence range | Description | Example | Required properties |"
  ],
  "tocPath": ""
}-->
