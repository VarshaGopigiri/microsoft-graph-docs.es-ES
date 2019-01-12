---
title: tipo de recurso meetingParticipantInfo
description: Información acerca de un participante en una reunión.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 409cf7eff4b1151a0ded11674fcde36a519f0e7f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27924485"
---
# <a name="meetingparticipantinfo-resource-type"></a>tipo de recurso meetingParticipantInfo

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Información acerca de un participante en una reunión.

## <a name="properties"></a>Propiedades

| Propiedad       | Tipo                          | Descripción                              |
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
