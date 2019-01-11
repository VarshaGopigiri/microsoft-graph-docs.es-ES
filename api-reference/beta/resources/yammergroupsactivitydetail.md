---
title: tipo de recurso yammerGroupsActivityDetail
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: 9e4ac61f2af69b4229c2e9c3df7c653428cc2033
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27832035"
---
# <a name="yammergroupsactivitydetail-resource-type"></a>tipo de recurso yammerGroupsActivityDetail

## <a name="properties"></a>Propiedades

| Propiedad           | Tipo    |
| :----------------- | :------ |
| reportRefreshDate  | Fecha    |
| groupDisplayName   | Cadena  |
| isDeleted          | Booleano |
| ownerPrincipalName | Cadena  |
| lastActivityDate   | Fecha    |
| groupType          | Cadena  |
| office365Connected | Booleano |
| memberCount        | Int64   |
| postedCount        | Int64   |
| readCount          | Int64   |
| likedCount         | Int64   |
| reportPeriod       | String  |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.yammerGroupsActivityDetail"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "groupDisplayName": "String", 
  "isDeleted": true, 
  "ownerPrincipalName": "String", 
  "lastActivityDate": "Date", 
  "groupType": "String", 
  "office365Connected": true, 
  "memberCount": 1024, 
  "postedCount": 1024, 
  "readCount": 1024, 
  "likedCount": 1024, 
  "reportPeriod": "String"
}
```
