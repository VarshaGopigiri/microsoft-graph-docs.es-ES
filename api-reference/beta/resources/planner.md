# Tipo de recurso planner
<a id="planner-resource-type" class="xliff"></a>

El recurso **planner** es el punto de entrada para el modelo de objetos de Planner. Devuelve un recurso **planner** singleton.  No contiene ninguna propiedad utilizable.


## Métodos
<a id="methods" class="xliff"></a>

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Crear plannerBucket](../api/planner_post_buckets.md) |[plannerBucket](plannerbucket.md)| Crear un nuevo **plannerBucket** publicándolo en la colección de depósitos.|
|[Crear plannerPlan](../api/planner_post_plans.md) |[plannerPlan](plannerplan.md)| Crear un nuevo **plannerPlan** publicándolo en la colección de planes.|
|[Crear plannerTask](../api/planner_post_tasks.md) |[plannerTask](plannertask.md)| Crear una nueva **plannerTask** publicándola en la colección de tareas.|

## Propiedades
<a id="properties" class="xliff"></a>
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|Cadena| Solo lectura. Identificador del recurso **planner**.|

## Relaciones
<a id="relationships" class="xliff"></a>
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|buckets|Colección [plannerBucket](plannerbucket.md)| Solo lectura. Admite valores NULL. Devuelve una colección de los depósitos especificados|
|plans|Colección [plannerPlan](plannerplan.md)| Solo lectura. Admite valores NULL. Devuelve una colección de los planes especificados|
|tasks|Colección [plannerTask](plannertask.md)| Solo lectura. Admite valores NULL. Devuelve una colección de las tareas especificadas|

## Representación JSON
<a id="json-representation" class="xliff"></a>
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.planner"
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
  "description": "planner resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->