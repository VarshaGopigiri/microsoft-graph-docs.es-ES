---
title: Tipo de recurso messageRuleActions
description: Representa el conjunto de acciones que están disponibles para una regla.
ms.openlocfilehash: bc9051d5857d25e2e163b3ed1d737072fe16b8bc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030907"
---
# <a name="messageruleactions-resource-type"></a>Tipo de recurso messageRuleActions


Representa el conjunto de acciones que están disponibles para una regla.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
| assignCategories | Colección String | Lista de categorías que se asignarán a un mensaje. |
| copyToFolder | String | Identificador de la carpeta donde se va a copiar un mensaje. |
| delete | Boolean | Indica si un mensaje se debe mover a la carpeta Elementos eliminados. |
| forwardAsAttachmentTo | Colección [recipient](recipient.md) | Direcciones de correo electrónico de los destinatarios a los que se debe reenviar un mensaje como datos adjuntos. |
| forwardTo | Colección [recipient](recipient.md) | Direcciones de correo electrónico de los destinatarios a los que se debe reenviar un mensaje. |
| markAsRead | Boolean | Indica si un mensaje debe marcarse como leído. |
| markImportance | importance | Establece la importancia del mensaje, que puede ser: `low`, `normal` o `high`. |
| moveToFolder |  String| Identificador de la carpeta a la que se moverá un mensaje. |
| permanentDelete | Boolean | Indica si un mensaje se debe eliminar permanentemente sin guardarse en la carpeta Elementos eliminados. |
| redirectTo | Colección [recipient](recipient.md) | Las direcciones de correo electrónico a la que se debe redirigir un mensaje. |
| stopProcessingRules | Boolean | Indica si se deben evaluar las reglas siguientes. |

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
   ],
  "@odata.type": "microsoft.graph.messageRuleActions"
}-->

```json
{
  "assignCategories": ["String"],
  "copyToFolder": "String",
  "delete": "Boolean",
  "forwardAsAttachmentTo": [{"@odata.type": "microsoft.graph.recipient"}],
  "forwardTo": [{"@odata.type": "microsoft.graph.recipient"}],
  "markAsRead": "Boolean",
  "markImportance": "String",
  "moveToFolder": "String",
  "permanentDelete": "Boolean",
  "redirectTo": [{"@odata.type": "microsoft.graph.recipient"}],
  "stopProcessingRules": "Boolean"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "messageRuleActions resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->