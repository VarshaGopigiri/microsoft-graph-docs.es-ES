---
title: tipo de recurso de canal
description: 'Un canal es una colección de chatMessages dentro de un equipo. '
author: nkramer
ms.openlocfilehash: 18a3293b757e641eab98b166a43ce023762ccc6d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27326778"
---
# <a name="channel-resource-type"></a>tipo de recurso de canal

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Un canal es una colección de [chatMessages](chatmessage.md) dentro de un [equipo](../resources/team.md). Un canal representa un tema y, por lo tanto, un aislamiento lógico de discusión, dentro de un equipo. Ejemplos pueden ser "Viernes equipo comer" canal y canal de "Arquitectura de la discusión".


## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Canales de lista](../api/channel-list.md) | colección de [canal](channel.md) | Obtener la lista de canales en este equipo.|
|[Creación de canal](../api/channel-post.md) | [canal](channel.md) | Crear un nuevo canal si incluye el nombre para mostrar y la descripción.|
|[Obtener el canal](../api/channel-get.md) | [canal](channel.md) | Leer las propiedades y relaciones del canal.|
|[Canal de actualización](../api/channel-patch.md) | [canal](channel.md) | Actualizar las propiedades del canal.|
|[Eliminación de canal](../api/channel-delete.md) | Ninguno | Eliminar un canal.|
|[Mensajes del canal de lista](../api/channel-list-messages.md)  | [chatMessage](../resources/chatmessage.md) | Obtener los mensajes en un canal |
|[Crear un subproceso de chat](../api/channel-post-chatthreads.md) | colección de [chatThread](chatthread.md)| Crear un subproceso de chat en el canal especificado.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|description|String|Descripción textual opcional para el canal.|
|displayName|String|Nombre de canal tal y como aparecerá para el usuario en Microsoft Teams.|
|id|String|Identificador único de la de los canales. Solo lectura.|
|isFavoriteByDefault|Boolean|Si el canal automáticamente se debe marcar 'favorito' para todos los miembros del equipo. Valor predeterminado: `false`.|
|email|Boolean| La dirección de correo electrónico para el envío de mensajes para el canal. Solo lectura.|
|webUrl|String|Un hipervínculo que se desplazará el canal en Microsoft Teams. Esta es la URL que se obtiene cuando haga clic en un canal en Microsoft Teams y seleccione vínculo Get a canal. Esta dirección URL debe se trata como un objeto binario opaco y no puede analizar. Solo lectura.|


## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|messages|colección de [chatMessage](chatmessage.md)|Una colección de todos los mensajes en el canal. Una propiedad de navegación. Admite valores NULL. Actualmente esta API sólo admite operaciones de lectura, pero finalmente será compatible con los mensajes de escritura demasiado.|
|chatThreads|colección de [chatThread](chatthread.md)|(Esto se están quedando obsoletas en favor de la propiedad de los mensajes) chatThreads admite la creación de nuevos mensajes, pero no leer mensajes. ChatThreads es una propiedad de navegación y es Nullable.|
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
