---
title: tipo de recurso commsNotifications
description: Lista de notificaciones usado por los servidores de comunicaciones para el envío de varias notificaciones en un único lote.
author: VinodRavichandran
localization_priority: Normal
ms.openlocfilehash: 9ce629e17c85806d7e05bce99d6a62f9fa9cbff8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27851502"
---
# <a name="commsnotifications-resource-type"></a>tipo de recurso commsNotifications

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Lista de notificaciones usado por los servidores de comunicaciones para el envío de varias notificaciones en un único lote.

## <a name="properties"></a>Propiedades

| Propiedad       | Tipo                                                 | Descripción                                   |
|:---------------|:-----------------------------------------------------|:----------------------------------------------|
| valor          | colección de [commsNotification](commsnotification.md) | La notificación de un cambio en el recurso. |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.commsNotifications"
}-->
```json
{
  "value": [ { "@odata.type": "#microsoft.graph.commsNotification" } ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "commsNotifications resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
