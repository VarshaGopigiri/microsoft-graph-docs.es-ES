---
title: tipo de recurso governanceRoleAssignmentRequestStatus
description: Representa el estado de la governanceRoleAssignmentRequest.
ms.openlocfilehash: 06b0f17513d5d796d3fe71cbd3888963bc4a34ca
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084775"
---
# <a name="governanceroleassignmentrequeststatus-resource-type"></a><span data-ttu-id="efb1e-103">tipo de recurso governanceRoleAssignmentRequestStatus</span><span class="sxs-lookup"><span data-stu-id="efb1e-103">governanceRoleAssignmentRequestStatus resource type</span></span>

> <span data-ttu-id="efb1e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="efb1e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="efb1e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="efb1e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="efb1e-106">Representa el estado de la [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md).</span><span class="sxs-lookup"><span data-stu-id="efb1e-106">Represents the status of the [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md).</span></span>


## <a name="properties"></a><span data-ttu-id="efb1e-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="efb1e-107">Properties</span></span>
<span data-ttu-id="efb1e-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="efb1e-108">Property</span></span>       | <span data-ttu-id="efb1e-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="efb1e-109">Type</span></span> |<span data-ttu-id="efb1e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="efb1e-110">Description</span></span>|
|:----|:-------------|:-----|
|<span data-ttu-id="efb1e-111">status</span><span class="sxs-lookup"><span data-stu-id="efb1e-111">status</span></span> |<span data-ttu-id="efb1e-112">String</span><span class="sxs-lookup"><span data-stu-id="efb1e-112">String</span></span>| <span data-ttu-id="efb1e-113">El estado de la solicitud de asignación de rol.</span><span class="sxs-lookup"><span data-stu-id="efb1e-113">The status of the role assignment request.</span></span> <span data-ttu-id="efb1e-114">El valor puede ser `InProgress` o `Closed`.</span><span class="sxs-lookup"><span data-stu-id="efb1e-114">The value can be `InProgress` or `Closed`.</span></span>|
|<span data-ttu-id="efb1e-115">Subestado</span><span class="sxs-lookup"><span data-stu-id="efb1e-115">subStatus</span></span> |<span data-ttu-id="efb1e-116">String</span><span class="sxs-lookup"><span data-stu-id="efb1e-116">String</span></span>| <span data-ttu-id="efb1e-117">El estado de sub de la solicitud de asignación de rol.</span><span class="sxs-lookup"><span data-stu-id="efb1e-117">The sub status of the role assignment request.</span></span> <span data-ttu-id="efb1e-118">Los valores pueden ser `Accepted`, `PendingEvaluation`, `Granted`, `Denied`, `PendingProvisioning`, `Provisioned`, `PendingRevocation`, `Revoked`, `Canceled`, `Failed`, `PendingApprovalProvisioning`, `PendingApproval`, `FailedAsResourceIsLocked`, `PendingAdminDecision`, `AdminApproved`, `AdminDenied`, `TimedOut`, y `ProvisioningStarted`.</span><span class="sxs-lookup"><span data-stu-id="efb1e-118">The values can be `Accepted`, `PendingEvaluation`, `Granted`, `Denied`, `PendingProvisioning`, `Provisioned`, `PendingRevocation`, `Revoked`, `Canceled`, `Failed`, `PendingApprovalProvisioning`, `PendingApproval`, `FailedAsResourceIsLocked`, `PendingAdminDecision`, `AdminApproved`, `AdminDenied`, `TimedOut`, and `ProvisioningStarted`.</span></span>|
|<span data-ttu-id="efb1e-119">statusDetails</span><span class="sxs-lookup"><span data-stu-id="efb1e-119">statusDetails</span></span>       |<span data-ttu-id="efb1e-120">colección [keyValue](../resources/keyvalue.md)</span><span class="sxs-lookup"><span data-stu-id="efb1e-120">[keyValue](../resources/keyvalue.md) collection</span></span>| <span data-ttu-id="efb1e-121">Los detalles del estado de la solicitud de asignación de rol.</span><span class="sxs-lookup"><span data-stu-id="efb1e-121">The details of the status of the role assignment request.</span></span> <span data-ttu-id="efb1e-122">Representa los resultados de la evaluación de reglas diferentes.</span><span class="sxs-lookup"><span data-stu-id="efb1e-122">It represents the evaluation results of different rules.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="efb1e-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="efb1e-123">JSON representation</span></span>

<span data-ttu-id="efb1e-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="efb1e-124">Here is a JSON representation of the resource.</span></span>

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