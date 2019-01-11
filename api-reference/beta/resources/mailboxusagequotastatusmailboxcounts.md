---
title: tipo de recurso mailboxUsageQuotaStatusMailboxCounts
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: b87bb1ce91626f9151d294e2243bba72ba72346b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27835227"
---
# <a name="mailboxusagequotastatusmailboxcounts-resource-type"></a>tipo de recurso mailboxUsageQuotaStatusMailboxCounts

## <a name="properties"></a>Propiedades

| Propiedad              | Tipo   |
| :-------------------- | :----- |
| reportRefreshDate     | Fecha   |
| underLimit            | Int64  |
| warningIssued         | Int64  |
| sendProhibited        | Int64  |
| sendReceiveProhibited | Int64  |
| indeterminado         | Int64  |
| reportDate            | Fecha   |
| reportPeriod          | String |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mailboxUsageQuotaStatusMailboxCounts"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "underLimit": 1024, 
  "warningIssued": 1024, 
  "sendProhibited": 1024, 
  "sendReceiveProhibited": 1024, 
  "indeterminate": 1024, 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
