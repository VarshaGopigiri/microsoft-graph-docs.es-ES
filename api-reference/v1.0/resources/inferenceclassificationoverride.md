# <a name="inferenceclassificationoverride-resource-type"></a>Tipo de recurso inferenceClassificationOverride

Representa el reemplazo de un usuario sobre cómo se deben clasificar siempre los mensajes entrantes de un remitente determinado.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Update](../api/inferenceclassificationoverride_update.md) | [inferenceClassificationOverride](inferenceclassificationoverride.md)    |Cambie el campo **ClassifyAs** de un reemplazo tal y como se especifica. |
|[Delete](../api/inferenceclassificationoverride_delete.md) | None |Elimina un reemplazo especificado por su identificador. |

## <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|classifyAs|string| Especifica cómo se deben clasificar siempre los mensajes entrantes de un remitente determinado. Valores posibles: `focused`, `other`.|
|id|string| Identificador único del reemplazo. Solo lectura.|
|senderEmailAddress|[emailAddress](emailaddress.md)|Información de la dirección de correo del remitente para el que se creó el reemplazo.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.inferenceClassificationOverride"
}-->

```json
{
  "classifyAs": "string",
  "id": "string (identifier)",
  "senderEmailAddress": {"@odata.type": "microsoft.graph.emailAddress"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "inferenceClassificationOverride resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->