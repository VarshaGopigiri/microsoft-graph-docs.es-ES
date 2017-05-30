# <a name="plannergroup-resource-type"></a>Tipo de recurso plannerGroup

El recurso **plannerGroup** proporciona acceso a los recursos Planner de un [grupo](group.md). No contiene ninguna propiedad utilizable.

### <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Enumerar planes](../api/plannergroup_list_plans.md) |Colección [plannerPlan](plannerplan.md)| Obtenga una colección de objetos **plannerPlan**.|

### <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|id|String| Solo lectura. Identificador del **plannerGroup**|

### <a name="relationships"></a>Relaciones
| Relación | Tipo    |Descripción|
|:---------------|:--------|:----------|
|plans|Colección [plannerPlan](plannerplan.md)| Solo lectura. Admite valores NULL. Devuelve los [plannerPlans](plannerplan.md) propiedad del grupo.|

### <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerGroup"
}-->

```json
{
  "id": "String (identifier)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerGroup resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->