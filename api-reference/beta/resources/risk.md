---
title: tipo de recurso de riesgo
description: Agrega el nivel de riesgo, el estado de riesgo y detalle de riesgo para el usuario arriesgado, inicie sesión en o evento de riesgos.
localization_priority: Normal
ms.openlocfilehash: da198ba27ca6cd0b762f322863f8c9bfd56a5cb7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27810671"
---
# <a name="risk-resource-type"></a>tipo de recurso de riesgo

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Agrega el nivel de riesgo, el estado de riesgo y detalle de riesgo para el usuario arriesgado, inicie sesión en o evento de riesgos.

## <a name="properties"></a>Propiedades

| Propiedad   | Tipo|Description|
|:---------------|:--------|:----------|
|`stateDetail`|riskDetail|Proporciona la razón de' ' detrás de un estado específico de un usuario arriesgado, inicio de sesión o un evento de riesgo. Los valores posibles son: `none`, `adminGeneratedTemporaryPassword`, `userPerformedSecuredPasswordChange`, `userPerformedSecuredPasswordReset`, `adminConfirmedSigninSafe`, `aiConfirmedSigninSafe`, `userPassedMFADrivenByRiskBasedPolicy`, `adminDismissedAllRiskForUser`, `adminConfirmedSigninCompromised`, `unknownFutureValue`. El valor `none` significa que ninguna acción se ha realizado hasta el momento en que el usuario o el inicio de sesión. |
|`riskLevelAggregated`|riskLevel|Proporciona el nivel de riesgo global de un usuario arriesgado, inicio de sesión o un evento de riesgo. Los valores posibles son: `none`, `low`, `medium`, `high`, `hidden`, y `unknownFutureValue`. El valor `hidden` significa que el usuario o el inicio de sesión no se ha habilitado para protección de la identidad de AD de Azure.|
|`riskLevelDuringSignIn`|riskLeve|Proporciona el nivel de riesgo de un inicio de sesión durante el inicio de sesión (es decir, basándose en los eventos de riesgo en tiempo real). Los valores posibles son: `none`, `low`, `medium`, `high`, `hidden`, y `unknownFutureValue`. El valor `hidden` en el inicio de sesión no se ha habilitado para protección de la identidad de AD de Azure.|
|`state`|riskState|Proporciona el estado riesgo de un usuario arriesgado, inicio de sesión o un evento de riesgo. Los valores posibles son: `none`, `confirmedSafe`, `remediated`, `dismissed`, `atRisk`, `confirmedCompromised`, `unknownFutureValue`. |

## <a name="json-representation"></a>Representación JSON

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
