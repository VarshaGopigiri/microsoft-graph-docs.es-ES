---
title: Tipo de recurso messageRuleActions
description: Representa el conjunto de acciones que están disponibles para una regla.
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: f6a78442dc82cade6b7e6d9a793fb6e49b3a1beb
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27889044"
---
# <a name="messageruleactions-resource-type"></a>Tipo de recurso messageRuleActions

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

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
| markImportance | String | Establece la importancia del mensaje, que puede ser: `low`, `normal` o `high`. |
| moveToFolder |  String| Identificador de la carpeta a la que se moverá un mensaje. |
| permanentDelete | Boolean | Indica si un mensaje se debe eliminar permanentemente sin guardarse en la carpeta Elementos eliminados. |
| redirectTo | [recipient](recipient.md) | Dirección de correo electrónico a la que se debe redirigir un mensaje. |
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
  "redirectTo": {"@odata.type": "microsoft.graph.recipient"},
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
