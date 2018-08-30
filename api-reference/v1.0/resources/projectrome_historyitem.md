# <a name="historyitem-resource-type"></a>tipo de recurso historyItem

Representa un elemento de historial para una [actividad](projectrome_activity.md) en una aplicación. Las actividades de usuario representan un destino único dentro de la aplicación, por ejemplo, un programa de TV, un documento o una campaña actual de un videojuego. Cuando un usuario interactúa con dicha actividad, la interacción se captura como un elemento de historial que indica la hora de inicio y final de esa actividad. Cuando el usuario vuelve a interactuar con esa actividad a lo largo del tiempo, se registran varios elementos de historial para una única actividad de usuario.

Cuando una aplicación crea una sesión, se debe agregar un objeto **historyItem** al objeto **activity** para reflejar el período de interactuación de usuario. Cada vez que un usuario vuelve a intercatuar con una actividad, se agrega un nuevo **historyItem** a la actividad para acumular interactuaciones de usuario.

## <a name="methods"></a>Métodos

|Método | Tipo de valor devuelto | Descripción|
|:------|:------------|:-----------|
|[Crear o reemplazar un historyItem](../api/projectrome_put_historyitem.md) | [historyItem](projectrome_historyitem.md) | Crea o reemplaza un **historyItem** existente para esa actividad (upsert). El id. debe ser un GUID.|
|[Eliminar un historyItem](../api/projectrome_delete_historyitem.md) | Sin contenido | Elimina el **historyItem** especificado para esa actividad.|

## <a name="properties"></a>Propiedades

|Nombre | Tipo | Descripción|
|:----|:-----|:-----------|
|status | status | Establecido por el servidor. Un código de estado que se usa para identificar objetos válidos. Valores: activo, actualizado, eliminado, ignorado.|
|userTimezone | Cadena | Opcional. La zona horaria en la que se encuentra el dispositivo del usuario utilizado para generar la actividad cuando se crea. Valores proporcionados como identificadores Olson con el fin de admitir la representación multiplataforma.|
|createdDateTime | DateTimeOffset | Establecida por el servidor. Fecha y hora en UTC en la que se creó el objeto en el servidor.|
|lastModifiedDateTime | DateTimeOffset | Establecida por el servidor. Fecha y hora en UTC en la que se modificó el objeto en el servidor.|
|id | Cadena | Obligatorio. GUID del conjunto de clientes para el objeto **historyItem**.|
|startedDateTime | DateTimeOffset | Obligatorio. Fecha y hora en UTC en la que se inició el **historyItem** (sesión de actividad). Requerida para el historial de escala de tiempo.|
|lastActiveDateTime | DateTimeOffset | Opcional. Fecha y hora en UTC en la que el **historyItem** (sesión de actividad) se entiende por última vez como activo o terminado; si es nulo, el estado del **historyItem** debería ser Ongoing (en curso).|
|expirationDateTime | DateTimeOffset | Opcional. Fecha y hora en UTC en la que el **historyItem** experimentará una eliminación permanente. Puede ser establecida por el cliente.|
|activeDurationSeconds | int | Opcional. La duración de la interactuación del usuario activo. si no se proporciona, esta se calcula a partir de la **startedDateTime** y la **lastActiveDateTime**.|

## <a name="relationships"></a>Relaciones

|Relación | Tipo | Descripción|
|:------------|:-----|:-----------|
|activity| [userActivity](../resources/projectrome_activity.md) | Opcional. NavigationProperty/Containment; propiedad de navegación para la actividad asociada.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "userTimezone",
    "lastActiveDateTime",
    "activeDurationSeconds"
  ],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.activityHistoryItem",
  "@odata.annotations": [
    {
      "capabilities": {
        "skippable": false,
        "countable": false,
        "selectable": false
      }
    }
  ]
}-->

```json
{
    "status": "active | updated | deleted | ignored",
    "createdDateTime": "DateTimeOffset",
    "lastModifiedDateTime": "DateTimeOffset",
    "id": "String",
    "expirationDateTime": "DateTimeOffset",
    "startedDateTime": "DateTimeOffset",
    "userTimezone": "String",
    "lastActiveDateTime": "DateTimeOffset",
    "activeDurationSeconds":"int"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2017-06-07 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "historyitem resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
