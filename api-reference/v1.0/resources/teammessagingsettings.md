---
title: tipo de recurso teamMessagingSettings
description: La configuración de mensajería y menciones en el equipo.
ms.openlocfilehash: 6d1ca12b473f2773d4f56e12405b17e21b0bd0ca
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029783"
---
# <a name="teammessagingsettings-resource-type"></a>tipo de recurso teamMessagingSettings



La configuración de mensajería y menciones en el [equipo](team.md).

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|allowUserEditMessages|Booleano|Si se establece en true, los usuarios puede editar sus mensajes.|
|allowUserDeleteMessages|Booleano|Si se establece en true, los usuarios puede eliminar sus mensajes.|
|allowOwnerDeleteMessages|Booleano|Si se establece en true, propietarios puede eliminar cualquier mensaje.|
|allowTeamMentions|Booleano|Si establece en true, se permiten menciones de @team.|
|allowChannelMentions|Booleano|Si establece en true, se permiten menciones de @channel.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamMessagingSettings"
}-->

```json
{
  "allowUserEditMessages": true,
  "allowUserDeleteMessages": true,
  "allowOwnerDeleteMessages": true,
  "allowTeamMentions": true,
  "allowChannelMentions": true    
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "team's messagingSettings resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
