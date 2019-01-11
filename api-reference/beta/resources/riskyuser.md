---
title: tipo de recurso riskyUsers
description: Representa los usuarios de Azure AD que están en riesgo. Azure AD continuamente da como resultado el riesgo de usuario en función de diversas señales y aprendizaje de máquinas. Esta API proporciona acceso mediante programación a todos los usuarios en riesgo en su Azure AD.
author: cloudhandler
localization_priority: Normal
ms.openlocfilehash: bb1dab6461a3b235d461720a68855f1e8f3f70d8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27871557"
---
# <a name="riskyusers-resource-type"></a><span data-ttu-id="e5df7-105">tipo de recurso riskyUsers</span><span class="sxs-lookup"><span data-stu-id="e5df7-105">riskyUsers resource type</span></span>

> <span data-ttu-id="e5df7-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e5df7-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e5df7-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e5df7-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e5df7-108">Representa los usuarios de Azure AD que están en riesgo.</span><span class="sxs-lookup"><span data-stu-id="e5df7-108">Represents Azure AD users who are at risk.</span></span> <span data-ttu-id="e5df7-109">Azure AD continuamente da como resultado el riesgo de usuario en función de diversas señales y aprendizaje de máquinas.</span><span class="sxs-lookup"><span data-stu-id="e5df7-109">Azure AD continually evaluates user risk based on various signals and machine learning.</span></span> <span data-ttu-id="e5df7-110">Esta API proporciona acceso mediante programación a todos los usuarios en riesgo en su Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e5df7-110">This API provides programmatic access to all at-risk users in your Azure AD.</span></span>

> <span data-ttu-id="e5df7-111">**Nota:** Esta API requiere una licencia de P2 de Azure AD Premium.</span><span class="sxs-lookup"><span data-stu-id="e5df7-111">**Note:** This API requires an Azure AD Premium P2 license.</span></span>

<span data-ttu-id="e5df7-112">Para obtener más información acerca de los eventos de riesgo, vea [Protección de identidad de Azure Active Directory](https://azure.microsoft.com/en-us/documentation/articles/active-directory-identityprotection/).</span><span class="sxs-lookup"><span data-stu-id="e5df7-112">For more information about risk events, see [Azure Active Directory Identity Protection](https://azure.microsoft.com/en-us/documentation/articles/active-directory-identityprotection/).</span></span>

## <a name="methods"></a><span data-ttu-id="e5df7-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="e5df7-113">Methods</span></span>

| <span data-ttu-id="e5df7-114">Método</span><span class="sxs-lookup"><span data-stu-id="e5df7-114">Method</span></span>   | <span data-ttu-id="e5df7-115">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e5df7-115">Return Type</span></span>|<span data-ttu-id="e5df7-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5df7-116">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="e5df7-117">Lista riskyUsers</span><span class="sxs-lookup"><span data-stu-id="e5df7-117">List riskyUsers</span></span>](../api/riskyusers-list.md) | [<span data-ttu-id="e5df7-118">riskyUsers</span><span class="sxs-lookup"><span data-stu-id="e5df7-118">riskyUsers</span></span>](riskyuser.md) |<span data-ttu-id="e5df7-119">Los usuarios peligrosos de lista y sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="e5df7-119">List risky users and their properties.</span></span>|
|[<span data-ttu-id="e5df7-120">Obtener riskyUsers</span><span class="sxs-lookup"><span data-stu-id="e5df7-120">Get riskyUsers</span></span>](../api/riskyusers-get.md) | [<span data-ttu-id="e5df7-121">riskyUsers</span><span class="sxs-lookup"><span data-stu-id="e5df7-121">riskyUsers</span></span>](riskyuser.md)|<span data-ttu-id="e5df7-122">Obtener un usuario arriesgado específico y sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="e5df7-122">Get a specific risky user and its properties.</span></span>|

## <a name="properties"></a><span data-ttu-id="e5df7-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e5df7-123">Properties</span></span>

| <span data-ttu-id="e5df7-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e5df7-124">Property</span></span>   | <span data-ttu-id="e5df7-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="e5df7-125">Type</span></span>|<span data-ttu-id="e5df7-126">Description</span><span class="sxs-lookup"><span data-stu-id="e5df7-126">Description</span></span>|
|:---------------|:--------|:----------|
|`id`|`string`|<span data-ttu-id="e5df7-127">Identificador único del usuario en riesgo</span><span class="sxs-lookup"><span data-stu-id="e5df7-127">Unique id of the user at risk</span></span>|
|`isDeleted`|`bool`|<span data-ttu-id="e5df7-128">Indica si el usuario se elimina.</span><span class="sxs-lookup"><span data-stu-id="e5df7-128">Indicates whether the user is deleted.</span></span> <span data-ttu-id="e5df7-129">Los valores posibles son: `true`,`false`</span><span class="sxs-lookup"><span data-stu-id="e5df7-129">Possible values are: `true`, `false`</span></span>|
|`isGuest`|`bool`|<span data-ttu-id="e5df7-130">Indica si el usuario es un usuario invitado.</span><span class="sxs-lookup"><span data-stu-id="e5df7-130">Indicates whether the user is a guest user.</span></span> <span data-ttu-id="e5df7-131">Los valores posibles son: `true` y `false`.</span><span class="sxs-lookup"><span data-stu-id="e5df7-131">Possible values are: `true`, `false`.</span></span> <span data-ttu-id="e5df7-132">Es True si la identidad del usuario se encuentra fuera del inquilino en consideración.</span><span class="sxs-lookup"><span data-stu-id="e5df7-132">True if user’s identity lies outside of the tenant in consideration.</span></span> <span data-ttu-id="e5df7-133">Este usuario podría ser un B2B o un usuario B2C con identidad en Azure AD, MSA o 3ª otro proveedor de identidad.</span><span class="sxs-lookup"><span data-stu-id="e5df7-133">This user could be a B2B or a B2C user with identity in Azure AD, MSA or 3rd party identity provider.</span></span> <span data-ttu-id="e5df7-134">False si la identidad del usuario se encuentra dentro del inquilino en consideración</span><span class="sxs-lookup"><span data-stu-id="e5df7-134">False if user’s identity lies inside the tenant in consideration</span></span>|
|`riskDetail`|`riskDetail`|<span data-ttu-id="e5df7-135">Proporciona la razón de' ' detrás de un estado específico de un usuario arriesgado, inicio de sesión o un evento de riesgo.</span><span class="sxs-lookup"><span data-stu-id="e5df7-135">Provides the 'reason' behind a specific state of a risky user, sign-in or a risk event.</span></span> <span data-ttu-id="e5df7-136">Los valores posibles son: `none`, `adminGeneratedTemporaryPassword`, `userPerformedSecuredPasswordChange`, `userPerformedSecuredPasswordReset`, `adminConfirmedSigninSafe`, `aiConfirmedSigninSafe`, `userPassedMFADrivenByRiskBasedPolicy`, `adminDismissedAllRiskForUser`, `adminConfirmedSigninCompromised`, `unknownFutureValue`.</span><span class="sxs-lookup"><span data-stu-id="e5df7-136">The possible values are: `none`, `adminGeneratedTemporaryPassword`, `userPerformedSecuredPasswordChange`, `userPerformedSecuredPasswordReset`, `adminConfirmedSigninSafe`, `aiConfirmedSigninSafe`, `userPassedMFADrivenByRiskBasedPolicy`, `adminDismissedAllRiskForUser`, `adminConfirmedSigninCompromised`, `unknownFutureValue`.</span></span> <span data-ttu-id="e5df7-137">El valor `none` significa que ninguna acción se ha realizado hasta el momento en que el usuario o el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="e5df7-137">The value `none` means that no action has been performed on the user or sign-in so far.</span></span>|
|`riskLevel`|`riskLevel`|<span data-ttu-id="e5df7-138">Proporciona el nivel de riesgo global de un usuario arriesgado, inicio de sesión o un evento de riesgo.</span><span class="sxs-lookup"><span data-stu-id="e5df7-138">Provides the overall risk level of a risky user, sign-in or a risk event.</span></span> <span data-ttu-id="e5df7-139">Los valores posibles son: `none`, `low`, `medium`, `high`, `hidden`, y `unknownFutureValue`.</span><span class="sxs-lookup"><span data-stu-id="e5df7-139">The possible values are: `none`, `low`, `medium`, `high`, `hidden`, and `unknownFutureValue`.</span></span> <span data-ttu-id="e5df7-140">El valor `hidden` significa que el usuario o el inicio de sesión no se ha habilitado para protección de la identidad de AD de Azure.</span><span class="sxs-lookup"><span data-stu-id="e5df7-140">The value `hidden` means the user or sign-in was not enabled for Azure AD Identity Protection.</span></span>|
|`riskState`|`riskState`|<span data-ttu-id="e5df7-141">Proporciona el estado riesgo de un usuario arriesgado, inicio de sesión o un evento de riesgo.</span><span class="sxs-lookup"><span data-stu-id="e5df7-141">Provides the 'risk state' of a risky user, sign-in or a risk event.</span></span> <span data-ttu-id="e5df7-142">Los valores posibles son: `none`, `confirmedSafe`, `remediated`, `dismissed`, `atRisk`, `confirmedCompromised`, `unknownFutureValue`.</span><span class="sxs-lookup"><span data-stu-id="e5df7-142">The possible values are: `none`, `confirmedSafe`, `remediated`, `dismissed`, `atRisk`, `confirmedCompromised`, `unknownFutureValue`.</span></span>|
|`riskLastUpdatedDateTime`|`datetime`|<span data-ttu-id="e5df7-143">La fecha y hora en que se actualizó por última vez el usuario arriesgado</span><span class="sxs-lookup"><span data-stu-id="e5df7-143">The date and time that the risky user was last updated</span></span>|
|`userDisplayName`|`string`|<span data-ttu-id="e5df7-144">Nombre de usuario arriesgado para mostrar</span><span class="sxs-lookup"><span data-stu-id="e5df7-144">Risky user display name</span></span>|
|`userPrincipalName`|`string`|<span data-ttu-id="e5df7-145">Nombre principal de usuario arriesgado</span><span class="sxs-lookup"><span data-stu-id="e5df7-145">Risky user principal name</span></span>|

## <a name="relationships"></a><span data-ttu-id="e5df7-146">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e5df7-146">Relationships</span></span>

| <span data-ttu-id="e5df7-147">Relación</span><span class="sxs-lookup"><span data-stu-id="e5df7-147">Relationship</span></span> | <span data-ttu-id="e5df7-148">Tipo</span><span class="sxs-lookup"><span data-stu-id="e5df7-148">Type</span></span> |<span data-ttu-id="e5df7-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5df7-149">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e5df7-150">id</span><span class="sxs-lookup"><span data-stu-id="e5df7-150">id</span></span>|<span data-ttu-id="e5df7-151">UserObjectId</span><span class="sxs-lookup"><span data-stu-id="e5df7-151">UserObjectId</span></span>| <span data-ttu-id="e5df7-152">El identificador único del usuario que está asociado con un evento de riesgo determinado.</span><span class="sxs-lookup"><span data-stu-id="e5df7-152">The unique identifier of the user with which a given risk event is associated with.</span></span>|
|<span data-ttu-id="e5df7-153">isGuest</span><span class="sxs-lookup"><span data-stu-id="e5df7-153">isGuest</span></span>|<span data-ttu-id="e5df7-154">isGuest</span><span class="sxs-lookup"><span data-stu-id="e5df7-154">isGuest</span></span>| <span data-ttu-id="e5df7-155">Un usuario arriesgado podría ser un usuario de la página principal (B2E) o un usuario invitado (B2B, B2C).</span><span class="sxs-lookup"><span data-stu-id="e5df7-155">A risky user could be either a Home user (B2E) or a Guest user (B2B, B2C).</span></span>|
|<span data-ttu-id="e5df7-156">isDeleted</span><span class="sxs-lookup"><span data-stu-id="e5df7-156">isDeleted</span></span>|<span data-ttu-id="e5df7-157">isDeleted</span><span class="sxs-lookup"><span data-stu-id="e5df7-157">isDeleted</span></span>| <span data-ttu-id="e5df7-158">Un usuario puede o no puede eliminarse.</span><span class="sxs-lookup"><span data-stu-id="e5df7-158">A user may or may not be deleted.</span></span> |
|<span data-ttu-id="e5df7-159">riskState</span><span class="sxs-lookup"><span data-stu-id="e5df7-159">riskState</span></span>|<span data-ttu-id="e5df7-160">riskState</span><span class="sxs-lookup"><span data-stu-id="e5df7-160">riskState</span></span>| <span data-ttu-id="e5df7-161">Un usuario arriesgado podría existir en uno de varios Estados.</span><span class="sxs-lookup"><span data-stu-id="e5df7-161">A risky user could exist in one of multiple states.</span></span> |
|<span data-ttu-id="e5df7-162">riskDetail</span><span class="sxs-lookup"><span data-stu-id="e5df7-162">riskDetail</span></span>|<span data-ttu-id="e5df7-163">riskDetail</span><span class="sxs-lookup"><span data-stu-id="e5df7-163">riskDetail</span></span>| <span data-ttu-id="e5df7-164">Un usuario arriesgado podía estar en un estado determinado debido a varias razones.</span><span class="sxs-lookup"><span data-stu-id="e5df7-164">A risky user could be in a certain state because of multiple reasons.</span></span> |
|<span data-ttu-id="e5df7-165">riskLevel</span><span class="sxs-lookup"><span data-stu-id="e5df7-165">riskLevel</span></span>|<span data-ttu-id="e5df7-166">riskLevel</span><span class="sxs-lookup"><span data-stu-id="e5df7-166">riskLevel</span></span>| <span data-ttu-id="e5df7-167">Un usuario arriesgado podría considerarse uno de varios niveles de riesgo.</span><span class="sxs-lookup"><span data-stu-id="e5df7-167">A risky user could be considered one of multiple risk levels.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="e5df7-168">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e5df7-168">JSON representation</span></span>

<span data-ttu-id="e5df7-169">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e5df7-169">Here is a JSON representation of the resource.</span></span>

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
"riskState":  {"@odata.type": "microsoft.graph.riskState"},
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
