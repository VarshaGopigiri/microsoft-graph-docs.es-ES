---
title: tipo de recurso suspiciousIpRiskEvent
description: Un evento de riesgo detectado por Azure Active Directory identidad protección donde un inicio de sesión de cuenta se intentó desde una dirección IP sospechosa. Obtener información completa acerca de los eventos de riesgo puede encontrarse en la documentación de protección de la identidad de AD de Azure.
ms.openlocfilehash: 5d5b2da25c926a88eb7b589d562e6fa9ec914338
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089141"
---
# <a name="suspiciousipriskevent-resource-type"></a><span data-ttu-id="7c53e-104">tipo de recurso suspiciousIpRiskEvent</span><span class="sxs-lookup"><span data-stu-id="7c53e-104">suspiciousIpRiskEvent resource type</span></span>

> <span data-ttu-id="7c53e-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7c53e-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7c53e-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7c53e-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7c53e-107">Un evento de riesgo detectado por la [Protección de identidad de Azure Active Directory](https://azure.microsoft.com/en-us/documentation/articles/active-directory-identityprotection/) donde un inicio de sesión de cuenta se intentó desde una dirección IP sospechosa.</span><span class="sxs-lookup"><span data-stu-id="7c53e-107">A risk event detected by [Azure Active Directory Identity Protection](https://azure.microsoft.com/en-us/documentation/articles/active-directory-identityprotection/) where an account sign-in is attempted from a suspicious IP address.</span></span> <span data-ttu-id="7c53e-108">Obtener información completa acerca de los eventos de riesgo puede encontrarse en la [documentación de protección de la identidad de AD de Azure](https://azure.microsoft.com/en-us/documentation/articles/active-directory-identityprotection-risk-events-types/).</span><span class="sxs-lookup"><span data-stu-id="7c53e-108">Complete information about risk events can be found in the [Azure AD Identity Protection documentation](https://azure.microsoft.com/en-us/documentation/articles/active-directory-identityprotection-risk-events-types/).</span></span>


## <a name="methods"></a><span data-ttu-id="7c53e-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="7c53e-109">Methods</span></span>

| <span data-ttu-id="7c53e-110">Método</span><span class="sxs-lookup"><span data-stu-id="7c53e-110">Method</span></span>           | <span data-ttu-id="7c53e-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c53e-111">Return Type</span></span>    |<span data-ttu-id="7c53e-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c53e-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="7c53e-113">Obtener suspiciousIpRiskEvent</span><span class="sxs-lookup"><span data-stu-id="7c53e-113">Get suspiciousIpRiskEvent</span></span>](../api/suspiciousipriskevent-get.md) | [<span data-ttu-id="7c53e-114">suspiciousIpRiskEvent</span><span class="sxs-lookup"><span data-stu-id="7c53e-114">suspiciousIpRiskEvent</span></span>](suspiciousipriskevent.md) |<span data-ttu-id="7c53e-115">Leer las propiedades y las relaciones del objeto suspiciousIpRiskEvent.</span><span class="sxs-lookup"><span data-stu-id="7c53e-115">Read properties and relationships of suspiciousIpRiskEvent object.</span></span>|

## <a name="properties"></a><span data-ttu-id="7c53e-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7c53e-116">Properties</span></span>
| <span data-ttu-id="7c53e-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7c53e-117">Property</span></span>     | <span data-ttu-id="7c53e-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="7c53e-118">Type</span></span>   |<span data-ttu-id="7c53e-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c53e-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7c53e-120">closedDateTime</span><span class="sxs-lookup"><span data-stu-id="7c53e-120">closedDateTime</span></span>|<span data-ttu-id="7c53e-121">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7c53e-121">dateTimeOffset</span></span>| <span data-ttu-id="7c53e-122">La fecha y hora en que se ha cerrado el evento de riesgo</span><span class="sxs-lookup"><span data-stu-id="7c53e-122">The date and time that the risk event was closed</span></span>|
|<span data-ttu-id="7c53e-123">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="7c53e-123">createdDateTime</span></span>|<span data-ttu-id="7c53e-124">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7c53e-124">dateTimeOffset</span></span>| <span data-ttu-id="7c53e-125">La fecha y hora en que se creó el evento de riesgo.</span><span class="sxs-lookup"><span data-stu-id="7c53e-125">The date and time that the risk event was created.</span></span> <span data-ttu-id="7c53e-126">Siempre es mayor o igual que la fecha y hora del evento riesgo propio.</span><span class="sxs-lookup"><span data-stu-id="7c53e-126">This is always greater than or equal to the datetime of the risk event itself.</span></span> <span data-ttu-id="7c53e-127">Ésta es la propiedad correcta para utilizar como filtro al consultar los eventos de riesgo.</span><span class="sxs-lookup"><span data-stu-id="7c53e-127">This is the correct property to use as a filter when querying risk events.</span></span>|
|<span data-ttu-id="7c53e-128">id</span><span class="sxs-lookup"><span data-stu-id="7c53e-128">id</span></span>|<span data-ttu-id="7c53e-129">string</span><span class="sxs-lookup"><span data-stu-id="7c53e-129">string</span></span>| <span data-ttu-id="7c53e-130">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="7c53e-130">Read-only</span></span>|
|<span data-ttu-id="7c53e-131">ipAddress</span><span class="sxs-lookup"><span data-stu-id="7c53e-131">ipAddress</span></span>|<span data-ttu-id="7c53e-132">string</span><span class="sxs-lookup"><span data-stu-id="7c53e-132">string</span></span>| <span data-ttu-id="7c53e-133">La dirección IP de inicio de sesión de</span><span class="sxs-lookup"><span data-stu-id="7c53e-133">The IP address of the sign-in</span></span>|
|<span data-ttu-id="7c53e-134">location</span><span class="sxs-lookup"><span data-stu-id="7c53e-134">location</span></span>|<span data-ttu-id="7c53e-135">string</span><span class="sxs-lookup"><span data-stu-id="7c53e-135">string</span></span>| <span data-ttu-id="7c53e-136">La ubicación que se adjunta a la dirección IP de inicio de sesión de</span><span class="sxs-lookup"><span data-stu-id="7c53e-136">The location attached to the IP address of the sign-in</span></span>|
|<span data-ttu-id="7c53e-137">riskEventDateTime</span><span class="sxs-lookup"><span data-stu-id="7c53e-137">riskEventDateTime</span></span>|<span data-ttu-id="7c53e-138">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7c53e-138">dateTimeOffset</span></span>| <span data-ttu-id="7c53e-139">Fecha y hora en que se produjo el evento de riesgo</span><span class="sxs-lookup"><span data-stu-id="7c53e-139">The date and time when the risk event occurred</span></span>|
|<span data-ttu-id="7c53e-140">riskEventStatus</span><span class="sxs-lookup"><span data-stu-id="7c53e-140">riskEventStatus</span></span>|<span data-ttu-id="7c53e-141">string</span><span class="sxs-lookup"><span data-stu-id="7c53e-141">string</span></span>| <span data-ttu-id="7c53e-142">Los valores posibles son: `active`, `remediated`, `dismissedAsFixed`, `dismissedAsFalsePositive`, `dismissedAsIgnore`, `loginBlocked`, `closedMfaAuto` y `closedMultipleReasons`.</span><span class="sxs-lookup"><span data-stu-id="7c53e-142">Possible values are: `active`, `remediated`, `dismissedAsFixed`, `dismissedAsFalsePositive`, `dismissedAsIgnore`, `loginBlocked`, `closedMfaAuto`, `closedMultipleReasons`.</span></span>|
|<span data-ttu-id="7c53e-143">riskLevel</span><span class="sxs-lookup"><span data-stu-id="7c53e-143">riskLevel</span></span>|<span data-ttu-id="7c53e-144">string</span><span class="sxs-lookup"><span data-stu-id="7c53e-144">string</span></span>| <span data-ttu-id="7c53e-145">Los valores posibles son: `low`, `medium` y `high`.</span><span class="sxs-lookup"><span data-stu-id="7c53e-145">Possible values are: `low`, `medium`, `high`.</span></span>|
|<span data-ttu-id="7c53e-146">riskEventType</span><span class="sxs-lookup"><span data-stu-id="7c53e-146">riskEventType</span></span>|<span data-ttu-id="7c53e-147">string</span><span class="sxs-lookup"><span data-stu-id="7c53e-147">string</span></span>| <span data-ttu-id="7c53e-148">El tipo de riesgo</span><span class="sxs-lookup"><span data-stu-id="7c53e-148">The type of risk</span></span>|
|<span data-ttu-id="7c53e-149">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="7c53e-149">userDisplayName</span></span>|<span data-ttu-id="7c53e-150">string</span><span class="sxs-lookup"><span data-stu-id="7c53e-150">string</span></span>| <span data-ttu-id="7c53e-151">El nombre del usuario en riesgo</span><span class="sxs-lookup"><span data-stu-id="7c53e-151">The name of the user at risk</span></span>|
|<span data-ttu-id="7c53e-152">userId</span><span class="sxs-lookup"><span data-stu-id="7c53e-152">userId</span></span>|<span data-ttu-id="7c53e-153">string</span><span class="sxs-lookup"><span data-stu-id="7c53e-153">string</span></span>| <span data-ttu-id="7c53e-154">El identificador del usuario en riesgo</span><span class="sxs-lookup"><span data-stu-id="7c53e-154">The id of the user at risk</span></span>|
|<span data-ttu-id="7c53e-155">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="7c53e-155">userPrincipalName</span></span>|<span data-ttu-id="7c53e-156">string</span><span class="sxs-lookup"><span data-stu-id="7c53e-156">string</span></span>| <span data-ttu-id="7c53e-157">El nombre principal de usuario del usuario en riesgo</span><span class="sxs-lookup"><span data-stu-id="7c53e-157">The user principal name of the user at risk</span></span>|

## <a name="relationships"></a><span data-ttu-id="7c53e-158">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7c53e-158">Relationships</span></span>
| <span data-ttu-id="7c53e-159">Relación</span><span class="sxs-lookup"><span data-stu-id="7c53e-159">Relationship</span></span> | <span data-ttu-id="7c53e-160">Tipo</span><span class="sxs-lookup"><span data-stu-id="7c53e-160">Type</span></span>   |<span data-ttu-id="7c53e-161">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c53e-161">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7c53e-162">impactedUser</span><span class="sxs-lookup"><span data-stu-id="7c53e-162">impactedUser</span></span>|[<span data-ttu-id="7c53e-163">user</span><span class="sxs-lookup"><span data-stu-id="7c53e-163">user</span></span>](user.md)| <span data-ttu-id="7c53e-p105">Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="7c53e-p105">Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="7c53e-166">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7c53e-166">JSON representation</span></span>

<span data-ttu-id="7c53e-167">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7c53e-167">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.suspiciousIpRiskEvent"
}-->

```json
{
  "closedDateTime": "String (timestamp)",
  "createdDateTime": "String (timestamp)",
  "id": "string (identifier)",
  "ipAddress": "string",
  "location": "string",
  "riskEventDateTime": "String (timestamp)",
  "riskEventStatus": "string",
  "riskLevel": "string",
  "riskType": "string",
  "userDisplayName": "string",
  "userId": "string",
  "userPrincipalName": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "suspiciousIpRiskEvent resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->