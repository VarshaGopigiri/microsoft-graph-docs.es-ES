---
title: tipo de recurso governanceRoleAssignmentRequestStatus
description: Representa el estado de la governanceRoleAssignmentRequest.
localization_priority: Normal
ms.openlocfilehash: c5daac53661cc607d51e5bfd1ec9031cfa599fca
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27808074"
---
# <a name="governanceroleassignmentrequeststatus-resource-type"></a>tipo de recurso governanceRoleAssignmentRequestStatus

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa el estado de la [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md).


## <a name="properties"></a>Propiedades
Propiedad       | Tipo |Descripción|
|:----|:-------------|:-----|
|status |Cadena| El estado de la solicitud de asignación de rol. El valor puede ser `InProgress` o `Closed`.|
|Subestado |Cadena| El estado de sub de la solicitud de asignación de rol. Los valores pueden ser `Accepted`, `PendingEvaluation`, `Granted`, `Denied`, `PendingProvisioning`, `Provisioned`, `PendingRevocation`, `Revoked`, `Canceled`, `Failed`, `PendingApprovalProvisioning`, `PendingApproval`, `FailedAsResourceIsLocked`, `PendingAdminDecision`, `AdminApproved`, `AdminDenied`, `TimedOut`, y `ProvisioningStarted`.|
|statusDetails       |colección [keyValue](../resources/keyvalue.md)| Los detalles del estado de la solicitud de asignación de rol. Representa los resultados de la evaluación de reglas diferentes. |

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.governanceRoleAssignmentRequestStatus"
}-->


```json
{
  "status": "String",
  "subStatus": "String",
  "statusDetails": [{"@odata.type": "microsoft.graph.keyvalue"}],
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "governanceRoleAssignmentRequestStatus",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
