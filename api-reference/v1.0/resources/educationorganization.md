# <a name="educationorganization-resource-type"></a>Tipo de recurso educationOrganization

Entidad abstracta que se utiliza para modelar la uniformidad entre los diferentes tipos de organización en el sector de la educación.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|description|Cadena| Descripción de la organización.|
|displayName|Cadena| Nombre para mostrar de organización.|
|externalSource|educationExternalSource| Origen desde el que se creó esta organización. Los valores posibles son: `sis`, `manual` y `unknownFutureValue`.|

## <a name="relationships"></a>Relaciones
Ninguna.


## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "abstract": true,
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationOrganization"
}-->

```json
{
  "description": "String",
  "displayName": "String",
  "externalSource": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationOrganization resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->