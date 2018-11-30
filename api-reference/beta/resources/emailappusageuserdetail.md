---
title: tipo de recurso emailAppUsageUserDetail
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 951d53f7491ff7f2b7721b14ed354d770cfd1730
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083758"
---
# <a name="emailappusageuserdetail-resource-type"></a>tipo de recurso emailAppUsageUserDetail

## <a name="properties"></a>Propiedades

| Propiedad          | Tipo              |
| :---------------- | :---------------- |
| reportRefreshDate | Fecha              |
| userPrincipalName | String            |
| displayName       | String            |
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
