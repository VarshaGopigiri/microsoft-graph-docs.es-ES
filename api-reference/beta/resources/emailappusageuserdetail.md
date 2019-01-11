---
title: tipo de recurso emailAppUsageUserDetail
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: 9f1748d6ae3b313fd9f3a87cc211858b5b876b9a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27858950"
---
# <a name="emailappusageuserdetail-resource-type"></a>tipo de recurso emailAppUsageUserDetail

## <a name="properties"></a>Propiedades

| Propiedad          | Tipo              |
| :---------------- | :---------------- |
| reportRefreshDate | Fecha              |
| userPrincipalName | Cadena            |
| displayName       | Cadena            |
| isDeleted         | Booleano           |
| deletedDate       | Fecha              |
| lastActivityDate  | Fecha              |
| mailForMac        | Colección String |
| outlookForMac     | Colección String |
| outlookForWindows | Colección String |
| outlookForMobile  | Colección String |
| otherForMobile    | Colección String |
| outlookForWeb     | Colección String |
| pop3App           | Colección String |
| imap4App          | Colección String |
| smtpApp           | Colección String |
| reportPeriod      | String            |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.emailAppUsageUserDetail"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "userPrincipalName": "String", 
  "displayName": "String", 
  "isDeleted": true, 
  "deletedDate": "Date", 
  "lastActivityDate": "Date", 
  "mailForMac": ["String"], 
  "outlookForMac": ["String"], 
  "outlookForWindows": ["String"], 
  "outlookForMobile": ["String"], 
  "otherForMobile": ["String"], 
  "outlookForWeb": ["String"], 
  "pop3App": ["String"], 
  "imap4App": ["String"], 
  "smtpApp": ["String"], 
  "reportPeriod": "String"
}
```
