---
title: Tipo de recurso attendee
description: Asistente a un evento. Esto puede ser una persona o un recurso, como una sala de reuniones o equipamiento que se ha configurado como un recurso en el servidor Exchange del espacio empresarial.
ms.openlocfilehash: 7c9040b563840c22eec1dd7456892fc7ff83ee4f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032715"
---
# <a name="attendee-resource-type"></a>Tipo de recurso attendee

Asistente a un evento. Esto puede ser una persona o un recurso, como una sala de reuniones o equipamiento que se ha configurado como un recurso en el servidor Exchange del espacio empresarial.

Derivadas de [attendeeBase](attendeebase.md).

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|status|[ResponseStatus](responsestatus.md)|Respuesta del asistente (ninguna, aceptada, rechazada, etc.) para el evento y fecha y hora en que se envió la respuesta.|
|type|String|Tipo de asistente: `required`, `optional`, `resource`.|
|emailAddress|[emailAddress](emailaddress.md)|Incluye el nombre y la dirección de SMTP del asistente.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.attendeeBase",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.attendee"
}-->

```json
{
  "status": {"@odata.type": "microsoft.graph.responseStatus"},
  "type": "String",
  "emailAddress": {"@odata.type": "microsoft.graph.emailAddress"}
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "attendee resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->