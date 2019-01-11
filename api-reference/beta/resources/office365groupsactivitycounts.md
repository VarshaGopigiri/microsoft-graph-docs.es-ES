---
title: tipo de recurso office365GroupsActivityCounts
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: 87867071545a36f7aca1833a369f919317153bc6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27874112"
---
# <a name="office365groupsactivitycounts-resource-type"></a>tipo de recurso office365GroupsActivityCounts

## <a name="properties"></a>Propiedades

| Propiedad               | Tipo   | Description                              |
| :--------------------- | :----- | ---------------------------------------- |
| reportRefreshDate      | Fecha   | La fecha más reciente del contenido.          |
| exchangeEmailsReceived | Int64  | El número de mensajes de correo electrónico recibidos por los buzones de grupo. |
| yammerMessagesPosted   | Int64  | El número de los mensajes enviados a grupos de Yammer. |
| yammerMessagesRead     | Int64  | El número de mensajes leídos en grupos de Yammer. |
| yammerMessagesLiked    | Int64  | El número de mensajes en grupos de Yammer. |
| reportDate             | Fecha   | La fecha en la que un número de mensajes de correo electrónico se han enviado a un buzón de grupo o un número de mensajes se contabilizaron, leer o gustado en un grupo de Yammer |
| reportPeriod           | Cadena | El número de días que cubre el informe.    |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.office365GroupsActivityCounts"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "exchangeEmailsReceived": 1024, 
  "yammerMessagesPosted": 1024, 
  "yammerMessagesRead": 1024, 
  "yammerMessagesLiked": 1024, 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
