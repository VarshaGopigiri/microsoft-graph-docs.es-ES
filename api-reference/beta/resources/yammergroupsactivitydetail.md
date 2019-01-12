---
title: tipo de recurso yammerGroupsActivityDetail
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: 79ce924fff5d1ce9ca861c3d48589a0ecad149dc
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27939171"
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
