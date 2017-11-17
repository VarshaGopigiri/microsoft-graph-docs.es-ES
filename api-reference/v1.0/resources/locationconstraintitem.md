# <a name="locationconstraintitem-resource-type"></a>Tipo de recurso locationConstraintItem

Las condiciones establecidas por un cliente para la ubicación de una reunión.

Derivado de [ubicación](location.md).

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
  
  ],
  "@odata.type": "microsoft.graph.locationConstraintItem"
}-->

```json
{
  "resolveAvailability": true,
  "address": {"@odata.type": "microsoft.graph.physicalAddress"},
  "displayName": "string",
  "locationEmailAddress": "string"
}

```
## <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
| address | [physicalAddress](physicalAddress.md) |Dirección postal de la ubicación. |
| displayName  | String | Nombre asociado a la ubicación.                       |
| locationEmailAddress | String | Dirección de correo electrónico opcional en la ubicación |
| resolveAvailability | Boolean | Si se establece en verdadero y el recurso especificado está ocupado [findMeetingTimes](../api/user_findmeetingtimes.md) buscará otro recurso que esté libre. Si se establece en falso y el recurso especificado está ocupado, **findMeetingTimes** devolverá el recurso mejor puntuado en la caché del usuario sin comprobar que esté libre o no. El valor predeterminado es "true". |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "locationConstraintItem resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->