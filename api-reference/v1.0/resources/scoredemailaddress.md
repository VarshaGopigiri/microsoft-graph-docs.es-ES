# <a name="scoredemailaddress-resource-type"></a>Tipo de recurso scoredEmailAddress

Representa una dirección de correo electrónico con puntuación.


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|address|string|La dirección de correo electrónico.|
|relevanceScore|double|La puntuación de relevancia de la dirección de correo electrónico. Una puntuación de relevancia se usa como criterio de ordenación con respecto a los demás resultados devueltos. Un valor de puntuación de relevancia más alto corresponde a un resultado más relevante. La relevancia viene determinada por las relaciones empresariales y los patrones de comunicación y colaboración del usuario. |

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.scoredEmailAddress"
}-->

```json
{
  "address": "string",
  "relevanceScore": 1024
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "scoredEmailAddress resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
