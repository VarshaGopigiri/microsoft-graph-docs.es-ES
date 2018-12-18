---
title: tipo de recurso teamMessagingSettings
description: La configuración de mensajería y menciones en el equipo.
author: nkramer
ms.openlocfilehash: 387c2e3ccedc6f11f17d4868b1b0d3eaf67624fa
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27304553"
---
# <a name="teammessagingsettings-resource-type"></a>tipo de recurso teamMessagingSettings



La configuración de mensajería y menciones en el [equipo](team.md).

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|allowUserEditMessages|Boolean|Si se establece en true, los usuarios puede editar sus mensajes.|
|allowUserDeleteMessages|Boolean|Si se establece en true, los usuarios puede eliminar sus mensajes.|
|allowOwnerDeleteMessages|Boolean|Si se establece en true, propietarios puede eliminar cualquier mensaje.|
|allowTeamMentions|Boolean|Si establece en true, se permiten menciones de @team.|
|allowChannelMentions|Boolean|Si establece en true, se permiten menciones de @channel.|

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
