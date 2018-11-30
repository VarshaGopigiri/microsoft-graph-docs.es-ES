---
title: Tipo de recurso followupFlag
description: Permite establecer una marca para que el usuario realice más adelante el seguimiento en un elemento. Los elementos admitidos incluyen message y contact.
ms.openlocfilehash: a996bc05e5297149e587d7372e989580146c1fad
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087347"
---
# <a name="followupflag-resource-type"></a>Tipo de recurso followupFlag

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Permite establecer una marca para que el usuario realice más adelante el seguimiento en un elemento. Los elementos admitidos incluyen [message](message.md) y [contact](contact.md).

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|completedDateTime|[dateTimeTimeZone](datetimetimezone.md)|Fecha y hora en que se finalizó el seguimiento.|
|dueDateTime|**dateTimeTimeZone**|Fecha y hora en que se va a finalizar el seguimiento.|
|flagStatus|String|Estado del seguimiento de un elemento. Los valores posibles son: `notFlagged`, `complete` y `flagged`.|
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
