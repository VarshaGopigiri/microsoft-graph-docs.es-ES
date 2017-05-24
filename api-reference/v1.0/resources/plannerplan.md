# <a name="plannerplan-resource-type"></a>Tipo de recurso plannerPlan

El recurso **plannerPlan** representa un plan de Office 365. Un plan puede ser propiedad de un [grupo](group.md) y contiene una colección de [plannerTasks](plannerTask.md). También puede tener una colección de [plannerBuckets](plannerBucket.md). Cada objeto plan tiene un objeto [details](plannerPlanDetails.md), que puede contener más información sobre el plan. Vea [Resumen](planner_overview.md) para obtener más información sobre las relaciones entre group, plan y task.



### <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener plannerPlan](../api/plannerplan_get.md) | [plannerPlan](plannerplan.md) |Leer las propiedades y las relaciones del objeto **plannerPlan**.|
|[Enumerar depósitos](../api/plannerplan_list_buckets.md) |Colección [plannerBucket](plannerbucket.md)| Obtenga una colección de objetos **plannerBucket**.|
|[Enumerar tareas](../api/plannerplan_list_tasks.md) |Colección [plannerTask](plannertask.md)| Obtenga una colección de objetos **plannerTask**.|
|[Update](../api/plannerplan_update.md) | [plannerPlan](plannerplan.md)    |Actualizar el objeto **plannerPlan**. |

### <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|createdDateTime|DateTimeOffset|Solo lectura. Fecha y hora en que se creó el plan. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|id|Cadena| Solo lectura. Id. del plan. Tiene 28 caracteres y distingue entre mayúsculas y minúsculas. La [validación del formato](planner_identifiers_disclaimer.md) se efectúa en el servicio.|
|owner|Cadena|Id. del [grupo](group.md) que tiene el plan. Para poder establecer este campo, debe existir un grupo válido. Una vez establecido, solo lo puede actualizar el propietario.|
|title|Cadena|Obligatorio. Título del plan.|
|createdBy|[identitySet](identityset.md)|Solo lectura. Usuario que creó el plan|

### <a name="relationships"></a>Relaciones
| Relación | Tipo    |Descripción|
|:---------------|:--------|:----------|
|buckets|Colección [plannerBucket](plannerbucket.md)| Solo lectura. Admite valores NULL. Colección de depósitos del plan.|
|details|[plannerPlanDetails](plannerplandetails.md)| Solo lectura. Admite valores NULL. Detalles adicionales sobre el plan.|
|tasks|Colección [plannerTask](plannertask.md)| Solo lectura. Admite valores NULL. Colección de tareas en el plan.|

### <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerPlan"
}-->

```json
{
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "createdDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "owner": "String",
  "title": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerPlan resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->