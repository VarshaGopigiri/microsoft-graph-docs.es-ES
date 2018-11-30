---
title: tipo de recurso automaticRepliesMailTips
description: Sugerencias de correo electrónico acerca de las respuestas automáticas que se han configurado en un buzón de correo.
ms.openlocfilehash: 943a465671c777305e5623104c82f377ff9496dd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030587"
---
# <a name="automaticrepliesmailtips-resource-type"></a>tipo de recurso automaticRepliesMailTips


[Sugerencias de correo electrónico](../resources/mailtips.md) acerca de las respuestas automáticas que se han configurado en un buzón de correo.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:-----|:-----|:-----|
| message | String | El mensaje de respuesta automática. |
| messageLanguage | [localeInfo](../resources/localeinfo.md) | El idioma que se encuentra el mensaje de respuesta automática en. |
| scheduledEndTime | [dateTimeTimeZone](../resources/datetimetimezone.md) | La fecha y hora en que se establecen las respuestas automáticas para finalizar. |
| scheduledStartTime | [dateTimeTimeZone](../resources/datetimetimezone.md) | La fecha y hora en que se establecen las respuestas automáticas para empezar. |

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "messageLanguage",
    "scheduledEndTime",
    "scheduledStartTime"
  ],
  "@odata.type": "microsoft.graph.automaticRepliesMailTips"
}-->

```json
{
  "message": "string",
  "messageLanguage": {"@odata.type": "microsoft.graph.localeInfo"},
  "scheduledEndTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "scheduledStartTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "automaticRepliesMailTips resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->