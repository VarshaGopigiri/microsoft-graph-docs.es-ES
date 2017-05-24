# <a name="planneruser-resource-type"></a>Tipo de recurso plannerUser

El recurso **plannerUser** proporciona acceso a los recursos Planner de un [usuario](user.md). No contiene ninguna propiedad utilizable.


### <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Enumerar planes](../api/planneruser_list_plans.md) |Colección [plannerPlan](plannerplan.md)| Obtenga una colección de objetos **plannerPlan**.|
|[Enumerar tareas](../api/planneruser_list_tasks.md) |Colección [plannerTask](plannertask.md)| Obtenga una colección de objetos **plannerTask**.|

### <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|id|Cadena| Solo lectura. Identificador del planenrUser|

### <a name="relationships"></a>Relaciones
| Relación | Tipo    |Descripción|
|:---------------|:--------|:----------|
|plans|Colección [plannerPlan](plannerplan.md)| Solo lectura. Admite valores NULL. Devuelve las [plannerTasks](plannertask.md) asignadas al usuario.|
|tasks|Colección [plannerTask](plannertask.md)| Solo lectura. Admite valores NULL. Devuelve los [plannerPlans](plannerplan.md) compartidos con el usuario.|

### <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerUser"
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
  "description": "plannerUser resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->