---
title: tipo de recurso oneDriveActivityUserDetail
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: 2f498c7c9507c4210f12f76d57f62729f84da578
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27820793"
---
# <a name="onedriveactivityuserdetail-resource-type"></a>tipo de recurso oneDriveActivityUserDetail

## <a name="properties"></a>Propiedades

| Propiedad                  | Tipo              |
| :------------------------ | :---------------- |
| reportRefreshDate         | Fecha              |
| userPrincipalName         | Cadena            |
| isDeleted                 | Booleano           |
| deletedDate               | Fecha              |
| lastActivityDate          | Fecha              |
| viewedOrEditedFileCount   | Int64             |
| syncedFileCount           | Int64             |
| sharedInternallyFileCount | Int64             |
| sharedExternallyFileCount | Int64             |
| assignedProducts          | Colección String |
| reportPeriod              | String            |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.oneDriveActivityUserDetail"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "userPrincipalName": "String", 
  "isDeleted": true, 
  "deletedDate": "Date", 
  "lastActivityDate": "Date", 
  "viewedOrEditedFileCount": 1024, 
  "syncedFileCount": 1024, 
  "sharedInternallyFileCount": 1024, 
  "sharedExternallyFileCount": 1024, 
  "assignedProducts": ["String"], 
  "reportPeriod": "String"
}
```
