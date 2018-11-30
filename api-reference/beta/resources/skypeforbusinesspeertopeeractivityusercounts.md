---
title: tipo de recurso skypeForBusinessPeerToPeerActivityUserCounts
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: ad3b409f3abc4cc9e7476825f9dbf5b7c2120d92
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088145"
---
# <a name="skypeforbusinesspeertopeeractivityusercounts-resource-type"></a>tipo de recurso skypeForBusinessPeerToPeerActivityUserCounts

## <a name="properties"></a>Propiedades

| Propiedad          | Tipo   |
| :---------------- | :----- |
| mensajería instantánea                | Int64  |
| audio             | Int64  |
| video             | Int64  |
| uso compartido de aplicaciones        | Int64  |
| fileTransfer      | Int64  |
| reportRefreshDate | Fecha   |
| reportDate        | Fecha   |
| reportPeriod      | String |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.skypeForBusinessPeerToPeerActivityUserCounts"
} -->

```json
{
  "im": 1024, 
  "audio": 1024, 
  "video": 1024, 
  "appSharing": 1024, 
  "fileTransfer": 1024, 
  "reportRefreshDate": "Date", 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
