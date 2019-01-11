---
title: tipo de recurso meetingParticipantInfo
description: Información acerca de un participante en una reunión.
author: VinodRavichandran
localization_priority: Normal
ms.openlocfilehash: d7b5ae17bd3bfb566bce0da9814b86aab98173da
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27834261"
---
# <a name="meetingparticipantinfo-resource-type"></a>tipo de recurso meetingParticipantInfo

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Información acerca de un participante en una reunión.

## <a name="properties"></a>Propiedades

| Propiedad       | Tipo                          | Description                              |
|:---------------|:------------------------------|:-----------------------------------------|
| identity       | [identitySet](identityset.md) | Información de identidad del participante. |
| UPN            | Cadena                        | Nombre principal de usuario del participante.  |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.meetingParticipantInfo"
}-->
```json
{
  "identity": {"@odata.type": "#microsoft.graph.identitySet"},
  "upn": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "meetingParticipantInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
