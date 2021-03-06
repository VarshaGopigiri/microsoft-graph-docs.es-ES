---
title: Tipo de recurso followupFlag
description: 'Permite establecer un indicador en un elemento para el usuario realizar el seguimiento más adelante. '
localization_priority: Normal
ms.openlocfilehash: 60d2e40a10c3ba5b2af9aa798b84aadaebedd57a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27885501"
---
# <a name="followupflag-resource-type"></a>Tipo de recurso followupFlag


Permite establecer un indicador en un elemento para el usuario realizar el seguimiento más adelante. 

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|completedDateTime|[dateTimeTimeZone](datetimetimezone.md)|Fecha y hora en que se finalizó el seguimiento.|
|dueDateTime|**dateTimeTimeZone**|Fecha y hora en que se va a finalizar el seguimiento.|
|flagStatus|followupFlagStatus|Estado del seguimiento de un elemento. Los valores posibles son: `notFlagged`, `complete` y `flagged`.|
|startDateTime|**dateTimeTimeZone**|Fecha y hora en que va a iniciarse el seguimiento.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.followupFlag"
}-->

```json
{
  "completedDateTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "dueDateTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "flagStatus": "String",
  "startDateTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "followupFlag resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
