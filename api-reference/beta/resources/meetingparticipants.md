---
title: tipo de recurso meetingParticipants
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 4f91c9198018e903eccff7e8fe07d6668d9fd2c9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090716"
---
# <a name="meetingparticipants-resource-type"></a>tipo de recurso meetingParticipants

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

## <a name="properties"></a>Propiedades

| Propiedad       | Tipo    | Descripción|
|:---------------|:--------|:----------|
| attendees | colección de [meetingParticipantInfo](meetingparticipantinfo.md) |  |
| organizador | [meetingParticipantInfo](meetingparticipantinfo.md) |  |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.meetingParticipants"
}-->
```json
{
  "attendees": [{"@odata.type": "#microsoft.graph.meetingParticipantInfo"}],
  "organizer": {"@odata.type": "#microsoft.graph.meetingParticipantInfo"}
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "meetingParticipants resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
