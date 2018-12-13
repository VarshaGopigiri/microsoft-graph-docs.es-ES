---
title: tipo de recurso riskyUsers
description: Representa los usuarios de Azure AD que están en riesgo. Azure AD continuamente da como resultado el riesgo de usuario en función de diversas señales y aprendizaje de máquinas. Esta API proporciona acceso mediante programación a todos los usuarios en riesgo en su Azure AD.
ms.openlocfilehash: 47856ab28a52046f19087e0f59745efb9855e81a
ms.sourcegitcommit: ba6b1d1a12dcb54916b4d3e529c856f6514e01e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2018
ms.locfileid: "27241065"
---
# <a name="riskyusers-resource-type"></a>tipo de recurso riskyUsers

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa los usuarios de Azure AD que están en riesgo. Azure AD continuamente da como resultado el riesgo de usuario en función de diversas señales y aprendizaje de máquinas. Esta API proporciona acceso mediante programación a todos los usuarios en riesgo en su Azure AD.

> **Nota:** Esta API requiere una licencia de P2 de Azure AD Premium.

Para obtener más información acerca de los eventos de riesgo, vea [Protección de identidad de Azure Active Directory](https://azure.microsoft.com/en-us/documentation/articles/active-directory-identityprotection/).

## <a name="methods"></a>Métodos

| Método   | Tipo de valor devuelto|Descripción|
|:---------------|:--------|:----------|
|[Lista riskyUsers](../api/riskyusers-list.md) | [riskyUsers](riskyuser.md) |Los usuarios peligrosos de lista y sus propiedades.|
|[Obtener riskyUsers](../api/riskyusers-get.md) | [riskyUsers](riskyuser.md)|Obtener un usuario arriesgado específico y sus propiedades.|

## <a name="properties"></a>Propiedades

| Propiedad   | Tipo|Descripción|
|:---------------|:--------|:----------|
|`id`|`string`|Identificador único del usuario en riesgo|
|`isDeleted`|`bool`|Indica si el usuario se elimina. Los valores posibles son: `true`,`false`|
|`isGuest`|`bool`|Indica si el usuario es un usuario invitado. Los valores posibles son: `true` y `false`. Es True si la identidad del usuario se encuentra fuera del inquilino en consideración. Este usuario podría ser un B2B o un usuario B2C con identidad en Azure AD, MSA o 3ª otro proveedor de identidad. False si la identidad del usuario se encuentra dentro del inquilino en consideración|
|`riskDetail`|`riskDetail`|Proporciona la razón de' ' detrás de un estado específico de un usuario arriesgado, inicio de sesión o un evento de riesgo. Los valores posibles son: `none`, `adminGeneratedTemporaryPassword`, `userPerformedSecuredPasswordChange`, `userPerformedSecuredPasswordReset`, `adminConfirmedSigninSafe`, `aiConfirmedSigninSafe`, `userPassedMFADrivenByRiskBasedPolicy`, `adminDismissedAllRiskForUser`, `adminConfirmedSigninCompromised`, `unknownFutureValue`. El valor `none` significa que ninguna acción se ha realizado hasta el momento en que el usuario o el inicio de sesión.|
|`riskLevel`|`riskLevel`|Proporciona el nivel de riesgo global de un usuario arriesgado, inicio de sesión o un evento de riesgo. Los valores posibles son: `none`, `low`, `medium`, `high`, `hidden`, y `unknownFutureValue`. El valor `hidden` significa que el usuario o el inicio de sesión no se ha habilitado para protección de la identidad de AD de Azure.|
|`riskState`|`riskState`|Proporciona el estado riesgo de un usuario arriesgado, inicio de sesión o un evento de riesgo. Los valores posibles son: `none`, `confirmedSafe`, `remediated`, `dismissed`, `atRisk`, `confirmedCompromised`, `unknownFutureValue`.|
|`riskLastUpdatedDateTime`|`datetime`|La fecha y hora en que se actualizó por última vez el usuario arriesgado|
|`userDisplayName`|`string`|Nombre de usuario arriesgado para mostrar|
|`userPrincipalName`|`string`|Nombre principal de usuario arriesgado|

## <a name="relationships"></a>Relaciones

| Relación | Tipo |Descripción|
|:---------------|:--------|:----------|
|id|UserObjectId| El identificador único del usuario que está asociado con un evento de riesgo determinado.|
|isGuest|isGuest| Un usuario arriesgado podría ser un usuario de la página principal (B2E) o un usuario invitado (B2B, B2C).|
|isDeleted|isDeleted| Un usuario puede o no puede eliminarse. |
|riskState|riskState| Un usuario arriesgado podría existir en uno de varios Estados. |
|riskDetail|riskDetail| Un usuario arriesgado podía estar en un estado determinado debido a varias razones. |
|riskLevel|riskLevel| Un usuario arriesgado podría considerarse uno de varios niveles de riesgo. |

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.riskyusers"
}-->

```json
{
"id": "string",
"riskLastUpdatedDateTime": "dateTimeOffset",
"isGuest": "boolean",
"isDeleted": "boolean",
"riskDetail":  {"@odata.type": "microsoft.graph.riskDetail"},
"riskLevel":  {"@odata.type": "microsoft.graph.riskLevel"},
"riskState":  {"@odata.type": "microsoft.graph.riskState"}
"userDisplayName": "string",
"userPrincipalName": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "riskyusers resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
