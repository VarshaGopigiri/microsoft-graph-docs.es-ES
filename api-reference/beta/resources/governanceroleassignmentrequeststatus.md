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
# <a name="governanceroleassignmentrequeststatus-resource-type"></a><span data-ttu-id="a9323-103">tipo de recurso governanceRoleAssignmentRequestStatus</span><span class="sxs-lookup"><span data-stu-id="a9323-103">governanceRoleAssignmentRequestStatus resource type</span></span>

> <span data-ttu-id="a9323-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a9323-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a9323-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a9323-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a9323-106">Representa el estado de la [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md).</span><span class="sxs-lookup"><span data-stu-id="a9323-106">Represents the status of the [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md).</span></span>


## <a name="properties"></a><span data-ttu-id="a9323-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a9323-107">Properties</span></span>
<span data-ttu-id="a9323-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a9323-108">Property</span></span>       | <span data-ttu-id="a9323-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="a9323-109">Type</span></span> |<span data-ttu-id="a9323-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9323-110">Description</span></span>|
|:----|:-------------|:-----|
|<span data-ttu-id="a9323-111">status</span><span class="sxs-lookup"><span data-stu-id="a9323-111">status</span></span> |<span data-ttu-id="a9323-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="a9323-112">String</span></span>| <span data-ttu-id="a9323-113">El estado de la solicitud de asignación de rol.</span><span class="sxs-lookup"><span data-stu-id="a9323-113">The status of the role assignment request.</span></span> <span data-ttu-id="a9323-114">El valor puede ser `InProgress` o `Closed`.</span><span class="sxs-lookup"><span data-stu-id="a9323-114">The value can be `InProgress` or `Closed`.</span></span>|
|<span data-ttu-id="a9323-115">Subestado</span><span class="sxs-lookup"><span data-stu-id="a9323-115">subStatus</span></span> |<span data-ttu-id="a9323-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="a9323-116">String</span></span>| <span data-ttu-id="a9323-117">El estado de sub de la solicitud de asignación de rol.</span><span class="sxs-lookup"><span data-stu-id="a9323-117">The sub status of the role assignment request.</span></span> <span data-ttu-id="a9323-118">Los valores pueden ser `Accepted`, `PendingEvaluation`, `Granted`, `Denied`, `PendingProvisioning`, `Provisioned`, `PendingRevocation`, `Revoked`, `Canceled`, `Failed`, `PendingApprovalProvisioning`, `PendingApproval`, `FailedAsResourceIsLocked`, `PendingAdminDecision`, `AdminApproved`, `AdminDenied`, `TimedOut`, y `ProvisioningStarted`.</span><span class="sxs-lookup"><span data-stu-id="a9323-118">The values can be `Accepted`, `PendingEvaluation`, `Granted`, `Denied`, `PendingProvisioning`, `Provisioned`, `PendingRevocation`, `Revoked`, `Canceled`, `Failed`, `PendingApprovalProvisioning`, `PendingApproval`, `FailedAsResourceIsLocked`, `PendingAdminDecision`, `AdminApproved`, `AdminDenied`, `TimedOut`, and `ProvisioningStarted`.</span></span>|
|<span data-ttu-id="a9323-119">statusDetails</span><span class="sxs-lookup"><span data-stu-id="a9323-119">statusDetails</span></span>       |<span data-ttu-id="a9323-120">colección [keyValue](../resources/keyvalue.md)</span><span class="sxs-lookup"><span data-stu-id="a9323-120">[keyValue](../resources/keyvalue.md) collection</span></span>| <span data-ttu-id="a9323-121">Los detalles del estado de la solicitud de asignación de rol.</span><span class="sxs-lookup"><span data-stu-id="a9323-121">The details of the status of the role assignment request.</span></span> <span data-ttu-id="a9323-122">Representa los resultados de la evaluación de reglas diferentes.</span><span class="sxs-lookup"><span data-stu-id="a9323-122">It represents the evaluation results of different rules.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="a9323-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a9323-123">JSON representation</span></span>

<span data-ttu-id="a9323-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a9323-124">Here is a JSON representation of the resource.</span></span>

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
