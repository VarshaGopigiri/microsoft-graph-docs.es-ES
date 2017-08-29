# <a name="alternativesecurityid-resource-type"></a>Tipo de recurso alternativeSecurityId

Contiene un identificador de seguridad alternativo asociado a un dispositivo. La propiedad **alternativeSecurityIds** de la entidad [Device](device.md) es una colección de **alternativeSecurityId**.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|identityProvider|String|            |
|key|Binary|            |
|type|Int32|            |

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.alternativeSecurityId"
}-->

```json
{
  "identityProvider": "string",
  "key": "binary",
  "type": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "alternativeSecurityId resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
