---
title: Tipo de recurso attendeeBase
description: El tipo de asistente.
ms.openlocfilehash: 6995ac94a600a60313ef26208b441c6ef6fdf001
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031216"
---
# <a name="attendeebase-resource-type"></a>Tipo de recurso attendeeBase

El tipo de asistente.

Derivado de [destinatario](recipient.md).

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.recipient",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.attendeeBase"
}-->

```json
{
  "type": "String",
  "emailAddress": {"@odata.type": "microsoft.graph.emailAddress"}
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|type|attendeeType| El tipo de asistente. Los valores posibles son: `required`, `optional`, `resource`. Actualmente si el asistente es una persona, [findMeetingTimes](../api/user-findmeetingtimes.md) siempre considera que es la persona de la `Required` tipo.|
|emailAddress|[emailAddress](emailaddress.md)|Incluye el nombre y la dirección de SMTP del asistente.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "attendeeBase resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
