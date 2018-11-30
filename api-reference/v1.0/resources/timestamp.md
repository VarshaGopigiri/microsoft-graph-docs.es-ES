---
title: tipo de recurso de marca de tiempo
description: Información de fecha y hora de un punto en el tiempo.
ms.openlocfilehash: 4f392e880bb165841fd8a9a31b6ed00bf2ba36fb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029326"
---
# <a name="timestamp-resource-type"></a>tipo de recurso de marca de tiempo

Información de fecha y hora de un punto en el tiempo.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.timeStamp"
}-->

```json
{
  "date": "String (timestamp)",
  "time": "String (timestamp)",
  "timeZone": "string"
}

```
## <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|date|Fecha|La parte de fecha de la marca de tiempo.|
|time|TimeOfDay|La parte de tiempo de la marca de tiempo.|
|timeZone|String|La parte de la zona horaria de la marca de tiempo, que es una de las áreas longitudinales 24 en el mundo.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "timeStamp resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->