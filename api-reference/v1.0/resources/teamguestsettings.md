---
title: tipo de recurso teamGuestSettings
description: Configuración para configurar si los invitados pueden crear, actualizar o eliminar los canales en el equipo.
ms.openlocfilehash: 3c59c84e0baa9db580a81eeb72a405ec5097c478
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031257"
---
# <a name="teamguestsettings-resource-type"></a>tipo de recurso teamGuestSettings



Configuración para configurar si los invitados pueden crear, actualizar o eliminar los canales en el [equipo](team.md).

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|allowCreateUpdateChannels|Booleano|Si se establece en true, invitados puede agregar y actualizar los canales.|
|allowDeleteChannels|Booleano|Si se establece en true, invitados puede eliminar canales.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamGuestSettings"
}-->

```json
{
  "allowCreateUpdateChannels": true,
  "allowDeleteChannels": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "team's guestSettings resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
