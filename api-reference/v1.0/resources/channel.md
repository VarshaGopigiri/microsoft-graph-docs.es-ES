---
title: tipo de recurso de canal
description: 'Un canal es una colección de los mensajes dentro de un equipo. '
author: nkramer
localization_priority: Priority
ms.openlocfilehash: 9a7b12646f36152bef17cec2d206e8e84abdcbbe
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27826568"
---
# <a name="channel-resource-type"></a>tipo de recurso de canal



Un canal es una colección de los mensajes dentro de un [equipo](../resources/team.md). Un canal representa un tema y, por lo tanto, un aislamiento lógico de discusión, dentro de un equipo. Ejemplos pueden ser "Viernes equipo comer" canal y canal de "Arquitectura de la discusión".


## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Canales de lista](../api/channel-list.md) | colección de [canal](channel.md) | Obtener la lista de canales en este equipo.|
|[Creación de canal](../api/channel-post.md) | [canal](channel.md) | Crear un nuevo canal si incluye el nombre para mostrar y la descripción.|
|[Obtener el canal](../api/channel-get.md) | [canal](channel.md) | Leer las propiedades y relaciones del canal.|
|[Canal de actualización](../api/channel-patch.md) | [canal](channel.md) | Actualizar las propiedades del canal.|
|[Eliminación de canal](../api/channel-delete.md) | Ninguno | Eliminar un canal.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|description|Cadena|Descripción textual opcional para el canal.|
|displayName|Cadena|Nombre de canal tal y como aparecerá para el usuario en Microsoft Teams.|
|id|Cadena|Identificador único de la de los canales. Solo lectura.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Description|
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
