---
title: tipo de recurso de riesgo
description: Agrega el nivel de riesgo, el estado de riesgo y detalle de riesgo para el usuario arriesgado, inicie sesión en o evento de riesgos.
ms.openlocfilehash: bc8ea5c30f78560ae8750e7750596f282feb4825
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085750"
---
# <a name="risk-resource-type"></a><span data-ttu-id="53bf4-103">tipo de recurso de riesgo</span><span class="sxs-lookup"><span data-stu-id="53bf4-103">risk resource type</span></span>

> <span data-ttu-id="53bf4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="53bf4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="53bf4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="53bf4-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="53bf4-106">Agrega el nivel de riesgo, el estado de riesgo y detalle de riesgo para el usuario arriesgado, inicie sesión en o evento de riesgos.</span><span class="sxs-lookup"><span data-stu-id="53bf4-106">Aggregates the risk level, risk state and risk detail for the risky user, sign in, or risk event.</span></span>

## <a name="properties"></a><span data-ttu-id="53bf4-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="53bf4-107">Properties</span></span>

| <span data-ttu-id="53bf4-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="53bf4-108">Property</span></span>   | <span data-ttu-id="53bf4-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="53bf4-109">Type</span></span>|<span data-ttu-id="53bf4-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="53bf4-110">Description</span></span>|
|:---------------|:--------|:----------|
|`stateDetail`|<span data-ttu-id="53bf4-111">riskDetail</span><span class="sxs-lookup"><span data-stu-id="53bf4-111">riskDetail</span></span>|<span data-ttu-id="53bf4-112">Proporciona la razón de' ' detrás de un estado específico de un usuario arriesgado, inicio de sesión o un evento de riesgo.</span><span class="sxs-lookup"><span data-stu-id="53bf4-112">Provides the 'reason' behind a specific state of a risky user, sign-in or a risk event.</span></span> <span data-ttu-id="53bf4-113">Los valores posibles son: `none`, `adminGeneratedTemporaryPassword`, `userPerformedSecuredPasswordChange`, `userPerformedSecuredPasswordReset`, `adminConfirmedSigninSafe`, `aiConfirmedSigninSafe`, `userPassedMFADrivenByRiskBasedPolicy`, `adminDismissedAllRiskForUser`, `adminConfirmedSigninCompromised`, `unknownFutureValue`.</span><span class="sxs-lookup"><span data-stu-id="53bf4-113">The possible values are: `none`, `adminGeneratedTemporaryPassword`, `userPerformedSecuredPasswordChange`, `userPerformedSecuredPasswordReset`, `adminConfirmedSigninSafe`, `aiConfirmedSigninSafe`, `userPassedMFADrivenByRiskBasedPolicy`, `adminDismissedAllRiskForUser`, `adminConfirmedSigninCompromised`, `unknownFutureValue`.</span></span> <span data-ttu-id="53bf4-114">El valor `none` significa que ninguna acción se ha realizado hasta el momento en que el usuario o el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="53bf4-114">The value `none` means that no action has been performed on the user or sign-in so far.</span></span> |
|`riskLevelAggregated`|<span data-ttu-id="53bf4-115">riskLevel</span><span class="sxs-lookup"><span data-stu-id="53bf4-115">riskLevel</span></span>|<span data-ttu-id="53bf4-116">Proporciona el nivel de riesgo global de un usuario arriesgado, inicio de sesión o un evento de riesgo.</span><span class="sxs-lookup"><span data-stu-id="53bf4-116">Provides the overall risk level of a risky user, sign-in or a risk event.</span></span> <span data-ttu-id="53bf4-117">Los valores posibles son: `none`, `low`, `medium`, `high`, `hidden`, y `unknownFutureValue`.</span><span class="sxs-lookup"><span data-stu-id="53bf4-117">The possible values are: `none`, `low`, `medium`, `high`, `hidden`, and `unknownFutureValue`.</span></span> <span data-ttu-id="53bf4-118">El valor `hidden` significa que el usuario o el inicio de sesión no se ha habilitado para protección de la identidad de AD de Azure.</span><span class="sxs-lookup"><span data-stu-id="53bf4-118">The value `hidden` means the user or sign-in was not enabled for Azure AD Identity Protection.</span></span>|
|`riskLevelDuringSignIn`|<span data-ttu-id="53bf4-119">riskLeve</span><span class="sxs-lookup"><span data-stu-id="53bf4-119">riskLeve</span></span>|<span data-ttu-id="53bf4-120">Proporciona el nivel de riesgo de un inicio de sesión durante el inicio de sesión (es decir, basándose en los eventos de riesgo en tiempo real).</span><span class="sxs-lookup"><span data-stu-id="53bf4-120">Provides the risk level of a sign-in during the sign-in (i.e. based on the real-time risk events).</span></span> <span data-ttu-id="53bf4-121">Los valores posibles son: `none`, `low`, `medium`, `high`, `hidden`, y `unknownFutureValue`.</span><span class="sxs-lookup"><span data-stu-id="53bf4-121">The possible values are: `none`, `low`, `medium`, `high`, `hidden`, and `unknownFutureValue`.</span></span> <span data-ttu-id="53bf4-122">El valor `hidden` en el inicio de sesión no se ha habilitado para protección de la identidad de AD de Azure.</span><span class="sxs-lookup"><span data-stu-id="53bf4-122">The value `hidden` means the sign-in was not enabled for Azure AD Identity Protection.</span></span>|
|`state`|<span data-ttu-id="53bf4-123">riskState</span><span class="sxs-lookup"><span data-stu-id="53bf4-123">riskState</span></span>|<span data-ttu-id="53bf4-124">Proporciona el estado riesgo de un usuario arriesgado, inicio de sesión o un evento de riesgo.</span><span class="sxs-lookup"><span data-stu-id="53bf4-124">Provides the 'risk state' of a risky user, sign-in or a risk event.</span></span> <span data-ttu-id="53bf4-125">Los valores posibles son: `none`, `confirmedSafe`, `remediated`, `dismissed`, `atRisk`, `confirmedCompromised`, `unknownFutureValue`.</span><span class="sxs-lookup"><span data-stu-id="53bf4-125">The possible values are: `none`, `confirmedSafe`, `remediated`, `dismissed`, `atRisk`, `confirmedCompromised`, `unknownFutureValue`.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="53bf4-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="53bf4-126">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.identityRiskEvent"
}-->

```json
{
    "stateDetail":  {"@odata.type": "microsoft.graph.riskDetail"},
    "riskLevelAggregated":  {"@odata.type": "microsoft.graph.riskLevel"},
    "riskLevelDuringSignIn":  {"@odata.type": "microsoft.graph.riskLevel"},
    "state":  {"@odata.type": "microsoft.graph.riskState"}
  }
  ```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "identityRiskEvent resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
