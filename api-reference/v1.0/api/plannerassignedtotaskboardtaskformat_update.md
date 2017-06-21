# <a name="update-plannerassignedtotaskboardtaskformat"></a>Actualizar plannerAssignedToTaskBoardTaskFormat

Actualizar las propiedades del objeto **plannerAssignedToTaskBoardTaskFormat**.
### <a name="prerequisites"></a>Requisitos previos
Se requieren los siguientes **ámbitos** para ejecutar esta API: 

*Group.ReadWrite.All*

### <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
PATCH /planner/tasks/<id>/assignedToTaskBoardFormat
```
### <a name="optional-request-headers"></a>Encabezados de solicitud opcionales
| Nombre       | Descripción|
|:-----------|:-----------|
| Authorization  | {token} de portador. Obligatorio. |
| If-Match  | Último valor ETag conocido para que se actualice **plannerAssignedToTaskBoardTaskFormat**. Obligatorio.|

### <a name="request-body"></a>Cuerpo de solicitud
En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.

| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|orderHintsByAssignee|[plannerOrderHintsByAssignee](..\resources\plannerOrderHintsByAssignee.md)|Diccionario de sugerencias usadas para ordenar las tareas en la vista AsignadoA del panel de tareas. La clave de cada entrada es uno de los usuarios a los que se ha asignado la tarea, mientras que el valor es la sugerencia de orden. El formato de cada valor se define tal como se describe [aquí](../resources/planner_order_hint_format.md).|
|unassignedOrderHint|String|Valor de sugerencia usado para ordenar la tarea en la vista AsignadoA del panel de tareas si la tarea no está asignada a nadie, o si el diccionario orderHintsByAssignee no proporciona ninguna sugerencia de orden para el usuario al que se ha asignado la tarea. El formato se define tal como se describe [aquí](../resources/planner_order_hint_format.md).|

### <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [plannerAssignedToTaskBoardTaskFormat](../resources/plannerassignedtotaskboardtaskformat.md) actualizado en el cuerpo de la respuesta.

Este método puede devolver cualquiera de los [códigos de estado HTTP](../../../concepts/errors.md). Los errores más comunes que deben controlar las aplicaciones de este método son las respuestas 400, 403, 404, 409 y 412. Para obtener más información sobre estos errores, vea [Common Planner error conditions](../resources/planner_overview.md#common-planner-error-conditions) (Condiciones de error habituales de Planner).

### <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "update_plannerassignedtotaskboardtaskformat"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/planner/tasks/01gzSlKkIUSUl6DF_EilrmQAKDhh/assignedToTaskBoardFormat
Content-type: application/json
Content-length: 96
If-Match: W/"JzEtVGFzayAgQEBAQEBAQEBAQEBAQEBAWCc="

{
  "orderHintsByAssignee": {
    "aaa27244-1db4-476a-a5cb-004607466324": "8566473P 957764Jk!"
  }
}
```
##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.plannerAssignedToTaskBoardTaskFormat"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 225

{
  "unassignedOrderHint": "RWk1",
  "orderHintsByAssignee": {
    "6463a5ce-2119-4198-9f2a-628761df4a62":"85752723360752+",
    "aaa27244-1db4-476a-a5cb-004607466324":"90057581;"
  },
  "id": "01gzSlKkIUSUl6DF_EilrmQAKDhh"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update plannerassignedtotaskboardtaskformat",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->