# <a name="messagerule-resource-type"></a>Tipo de recurso messageRule


Regla que se aplica a los mensajes de la Bandeja de entrada de un usuario.

En Outlook, puede establecer reglas de los mensajes entrantes en la Bandeja de entrada para llevar a cabo acciones específicas en determinadas condiciones. 

Mediante programación, tiene acceso a las reglas a través de la propiedad de navegación **messageRules** de la [carpeta](mailfolder.md) Bandeja de entrada. Cada regla se representa mediante este recurso **messageRule**, las acciones de regla disponibles se representan mediante el tipo complejo [messageRuleActions](messageruleactions.md) y las condiciones de regla disponibles se representan mediante el tipo complejo [messageRulePredicates](messagerulepredicates.md).


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
| actions | [messageRuleActions](messageruleactions.md) | Acciones que se van a realizar en un mensaje cuando se cumplan las condiciones correspondientes. |
| conditions | [messageRulePredicates](messagerulepredicates.md) | Condiciones que, cuando se cumplan, activarán las acciones correspondientes a esa regla. |
| displayName | String | Nombre para mostrar de la regla. |
| exceptions | [messageRulePredicates](messagerulepredicates.md) | Condiciones de excepción de la regla. |
| hasError | Boolean | Indica si la regla es una condición de error. Solo lectura. |
| id |String|Identificador único de la regla. Solo lectura.|
| isEnabled | Boolean | Indica si la regla está habilitada para que se aplique a los mensajes. |
| isReadOnly | Boolean | Indica si la regla es de solo lectura y la API de REST de reglas no la puede modificar ni eliminar. |
| sequence | Int32 | Indica el orden en que se ejecuta la regla entre otras reglas. |


## <a name="json-representation"></a>Representación JSON
Esta es una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
   ],
  "@odata.type": "microsoft.graph.messageRule"
}-->

```json
{
  "actions": {"@odata.type": "microsoft.graph.messageRuleActions"},
  "conditions": {"@odata.type": "microsoft.graph.messageRulePredicates"},
  "displayName": "String",
  "exceptions": {"@odata.type": "microsoft.graph.messageRulePredicates"},
  "hasError": "Boolean",
  "id": "String",
  "isEnabled": "Boolean",
  "isReadOnly": "Boolean",
  "sequence": "Int32"
}

```

## <a name="methods"></a>Métodos
| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Enumerar reglas](../api/mailfolder_list_messagerules.md) | Colección [messageRule](messagerule.md) |Obtener todos los objetos **messageRule** definidos para la Bandeja de entrada del usuario.|
|[Obtener regla](../api/messagerule_get.md) | [messageRule](messagerule.md) |Leer las propiedades y relaciones de un objeto **messageRule**.|
|[Crear](../api/mailfolder_post_messagerules.md) | [messageRule](messagerule.md) |Crear un objeto **messageRule** especificando un conjunto de condiciones y acciones.|
|[Actualizar](../api/messagerule_update.md) | [messageRule](messagerule.md) |Cambie las propiedades modificables en un objeto **messageRule** y guarde los cambios. |
|[Eliminar](../api/messagerule_delete.md) | Ninguno |Eliminar el objeto **messageRule** especificado. |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "messageRule resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->