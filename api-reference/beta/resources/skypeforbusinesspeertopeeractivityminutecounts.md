---
title: tipo de recurso skypeForBusinessPeerToPeerActivityMinuteCounts
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 5377e8d8f2ec145f5aee590409206de75e915d9f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089990"
---
# <a name="skypeforbusinesspeertopeeractivityminutecounts-resource-type"></a>tipo de recurso skypeForBusinessPeerToPeerActivityMinuteCounts

## <a name="properties"></a>Propiedades

| Propiedad          | Tipo   |
| :---------------- | :----- |
| audio             | Int64  |
| video             | Int64  |
| reportRefreshDate | Fecha   |
| reportDate        | Fecha   |
| reportPeriod      | String |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.skypeForBusinessPeerToPeerActivityMinuteCounts"
} -->

```json
{
  "audio": 1024, 
  "video": 1024, 
  "reportRefreshDate": "Date", 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
