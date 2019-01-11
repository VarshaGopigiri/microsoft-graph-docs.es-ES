---
title: tipo de recurso chatThread
description: Una chatThread es una colección de chatMessages en Microsoft Teams.
localization_priority: Priority
ms.openlocfilehash: 5060d7ea846f5aedec5551aaf247642a36f73c1c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27833246"
---
# <a name="chatthread-resource-type"></a>tipo de recurso chatThread

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Una chatThread es una colección de [chatMessages](chatmessage.md) en Microsoft Teams.

> En la actualidad, chatThreads puede ser [creado en los canales](../api/channel-post-chatthreads.md).  API de futuras versiones admitirá chatThreads existente, así como lectura/escritura de chats directas entre los usuarios que están fuera del ámbito de un equipo o un canal de lectura.

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Crear hilo](../api/channel-post-chatthreads.md) | [chatThread](chatthread.md) |Iniciar un nuevo subproceso en el canal especificado, que proporciona el primer mensaje.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|Cadena| Solo lectura.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Description|
|:---------------|:--------|:----------|
|rootMessage|[chatMessage](chatmessage.md)| Admite valores NULL.|
|chatMessages|colección de [chatMessage](chatmessage.md)| Admite valores NULL.|

> Actualmente estas relaciones existe implícitamente, pero no se puede leer o escribir.  Versiones beta futuras API admitirá esto.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "posts"
  ],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.chatThread"
}-->

```json
{
  "id": "string (identifier)",
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "chatThread resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
