# <a name="locationconstraint-resource-type"></a>Tipo de recurso locationConstraint

Las condiciones establecidas por un cliente para la ubicación de una reunión.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.locationconstraint"
}-->

```json
{
  "isRequired": true,
  "locations": [{"@odata.type": "microsoft.graph.locationConstraintItem"}],
  "suggestLocation": true
}

```
## <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|isRequired|Boolean|El cliente solicita que el servicio incluya en la respuesta una ubicación para la reunión. Si esto es verdadero y todos los recursos están ocupados, [findMeetingTimes](../api/user_findmeetingtimes.md) no devolverá ninguna sugerencia de fecha de reunión. Si esto es falso y todos los recursos están ocupados, **findMeetingTimes** buscará igual fechas de reunión sin ubicación. |
|ubicaciones|Colección [locationConstraintItem](locationconstraintitem.md)|Información de restricciones para una o más ubicaciones que el cliente solicita para la reunión.|
|suggestLocation|Booleano|El cliente solicita al servicio que sugiera una o más ubicaciones de reunión.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "locationConstraint resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->