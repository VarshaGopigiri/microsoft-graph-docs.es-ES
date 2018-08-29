# <a name="plannerplandetails-resource-type"></a>Tipo de recurso plannerPlanDetails


El recurso **plannerPlanDetails** representa la información adicional de un plan. Cada objeto [plan](plannerplan.md) tiene un objeto details.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener plannerPlanDetails](../api/plannerplandetails_get.md) | [plannerPlanDetails](plannerplandetails.md) |Leer las propiedades y las relaciones del objeto **plannerPlanDetails**.|
|[Update](../api/plannerplandetails_update.md) | [plannerPlanDetails](plannerplandetails.md)    |Actualizar el objeto **plannerPlanDetails**. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|categoryDescriptions|[plannerCategoryDescriptions](plannercategorydescriptions.md)|Objeto que especifica las descripciones de las seis categorías que pueden estar asociadas a las tareas del plan|
|id|Cadena| Solo lectura. Identificador de los detalles del plan. Tiene 28 caracteres y distingue mayúsculas y minúsculas. [La validación de formato](planner_identifiers_disclaimer.md) se realiza en el servicio.|
|sharedWith|[plannerUserIds](planneruserids.md)|Conjunto de identificadores de usuario con el que se comparte este plan. Si está aprovechando los grupos de Office 365, use la API de grupos para administrar la pertenencia a los grupos a fin de compartir el plan del [grupo](group.md). También puede agregar los miembros existentes del grupo a esta colección, aunque no es necesario que obtengan acceso al plan propiedad del grupo. |

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.plannerPlanDetails"
}-->

```json
{
  "categoryDescriptions": {"@odata.type": "microsoft.graph.plannerCategoryDescriptions"},
  "id": "String (identifier)",
  "sharedWith": {"@odata.type": "microsoft.graph.plannerUserIds"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerPlanDetails resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->