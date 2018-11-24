# <a name="channel-resource-type"></a>tipo de recurso de canal



Un canal es una colección de los mensajes dentro de un [equipo](../resources/team.md). Un canal representa un tema y, por lo tanto, un aislamiento lógico de discusión, dentro de un equipo. Ejemplos pueden ser "Viernes equipo comer" canal y canal de "Arquitectura de la discusión".


## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Canales de lista](../api/channel_list.md) | colección de [canal](channel.md) | Obtener la lista de canales en este equipo.|
|[Creación de canal](../api/channel_post.md) | [canal](channel.md) | Crear un nuevo canal si incluye el nombre para mostrar y la descripción.|
|[Obtener el canal](../api/channel_get.md) | [canal](channel.md) | Leer las propiedades y relaciones del canal.|
|[Canal de actualización](../api/channel_patch.md) | [canal](channel.md) | Actualizar las propiedades del canal.|
|[Eliminación de canal](../api/channel_delete.md) | Ninguno | Eliminar un canal.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|description|String|Descripción textual opcional para el canal.|
|displayName|String|Nombre de canal tal y como aparecerá para el usuario en Microsoft Teams.|
|id|String|Identificador único de la de los canales. Solo lectura.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|fichas|colección de [teamsTab](../resources/teamstab.md)|Una colección de todas las fichas en el canal. Una propiedad de navegación.|


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "chatthreads"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.channel"
}-->

```json
{
  "description": "string",
  "displayName": "string",
  "id": "string (identifier)",
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "channel resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
