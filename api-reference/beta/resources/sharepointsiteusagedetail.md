---
title: tipo de recurso sharePointSiteUsageDetail
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: e0827f6b6b991136198fc174e01e7d0e1f91c259
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27959913"
---
# <a name="sharepointsiteusagedetail-resource-type"></a>tipo de recurso sharePointSiteUsageDetail

## <a name="properties"></a>Propiedades

| Propiedad                | Tipo    |
| :---------------------- | :------ |
| reportRefreshDate       | Fecha    |
| siteId                  | Guid  |
| siteUrl                 | Cadena  |
| ownerDisplayName        | Cadena  |
| isDeleted               | Booleano |
| lastActivityDate        | Fecha    |
| fileCount               | Int64   |
| activeFileCount         | Int64   |
| pageViewCount           | Int64   |
| visitedPageCount        | Int64   |
| storageUsedInBytes      | Int64   |
| storageAllocatedInBytes | Int64   |
| rootWebTemplate         | Cadena  |
| reportPeriod            | String  |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.sharePointSiteUsageDetail"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "siteId": "Guid", 
  "siteUrl": "String", 
  "ownerDisplayName": "String", 
  "isDeleted": true, 
  "lastActivityDate": "Date", 
  "fileCount": 1024, 
  "activeFileCount": 1024, 
  "pageViewCount": 1024, 
  "visitedPageCount": 1024, 
  "storageUsedInBytes": 1024, 
  "storageAllocatedInBytes": 1024, 
  "rootWebTemplate": "String", 
  "reportPeriod": "String"
}
```
