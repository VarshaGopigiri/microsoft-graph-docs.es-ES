# <a name="planner-resource-type"></a>Tipo de recurso planner

El recurso **planner** es el punto de entrada para el modelo de objetos de Planner. Devuelve un recurso **planner** singleton.  No contiene ninguna propiedad utilizable.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Crear plannerBucket](../api/planner_post_buckets.md) |[plannerBucket](plannerbucket.md)| Crear un nuevo **plannerBucket** publicándolo en la colección de depósitos.|
|[Crear plannerPlan](../api/planner_post_plans.md) |[plannerPlan](plannerplan.md)| Crear un nuevo **plannerPlan** publicándolo en la colección de planes.|
|[Crear plannerTask](../api/planner_post_tasks.md) |[plannerTask](plannertask.md)| Crea una nueva **plannerTask** publicándola en la colección de tareas.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|buckets|Colección [plannerBucket](plannerbucket.md)| Solo lectura. Admite valores NULL. Devuelve una colección de los depósitos especificados|
|plans|Colección [plannerPlan](plannerplan.md)| Solo lectura. Admite valores NULL. Devuelve una colección de los planes especificados|
|tasks|Colección [plannerTask](plannertask.md)| Solo lectura. Admite valores NULL. Devuelve una colección de las tareas especificadas|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.planner"
}-->

```json
{
}
```

## <a name="example"></a>Ejemplo

El recurso **planner** está disponible en la raíz del gráfico.

<!--{
  "blockType": "request"
}-->
```http
GET https://graph.microsoft.com/v1.0/planner
```

<!--{
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.planner"
}-->
```json
HTTP/1.1 200 OK
Content-type: application/json

{
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