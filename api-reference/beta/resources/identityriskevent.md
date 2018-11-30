---
title: tipo de recurso identityRiskEvent
description: 'Un evento de riesgo detectado por la protección de identidad de Azure Active Directory. Es el tipo base para cada tipo de evento de riesgo específico:'
ms.openlocfilehash: e61f5e0dc2dae2c055636e3fd3737e16b2558458
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084835"
---
# <a name="identityriskevent-resource-type"></a><span data-ttu-id="61bf2-104">tipo de recurso identityRiskEvent</span><span class="sxs-lookup"><span data-stu-id="61bf2-104">identityRiskEvent resource type</span></span>

> <span data-ttu-id="61bf2-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="61bf2-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="61bf2-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="61bf2-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="61bf2-107">Un evento de riesgo detectado por la [Protección de identidad de Azure Active Directory](https://azure.microsoft.com/en-us/documentation/articles/active-directory-identityprotection/).</span><span class="sxs-lookup"><span data-stu-id="61bf2-107">A risk event detected by [Azure Active Directory Identity Protection](https://azure.microsoft.com/en-us/documentation/articles/active-directory-identityprotection/).</span></span> <span data-ttu-id="61bf2-108">Es el tipo base para cada tipo de evento de riesgo específico:</span><span class="sxs-lookup"><span data-stu-id="61bf2-108">It is the base type for each specific risk event type:</span></span>

| <span data-ttu-id="61bf2-109">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="61bf2-109">Event type</span></span>         | <span data-ttu-id="61bf2-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="61bf2-110">Description</span></span>|
|:---------------|:-----------|
|[<span data-ttu-id="61bf2-111">anonymousipRiskEvent</span><span class="sxs-lookup"><span data-stu-id="61bf2-111">anonymousipRiskEvent</span></span>](anonymousipriskevent.md) | <span data-ttu-id="61bf2-112">Inicios de sesión desde las direcciones IP anónimas.</span><span class="sxs-lookup"><span data-stu-id="61bf2-112">Sign-ins from anonymous IP addresses.</span></span> |
|[<span data-ttu-id="61bf2-113">malwareRiskEvent</span><span class="sxs-lookup"><span data-stu-id="61bf2-113">malwareRiskEvent</span></span>](malwareriskevent.md) | <span data-ttu-id="61bf2-114">Inicios de sesión desde dispositivos infectados con malware.</span><span class="sxs-lookup"><span data-stu-id="61bf2-114">Sign-ins from malware-infected devices.</span></span> |
|[<span data-ttu-id="61bf2-115">impossibleTravelRiskEvent</span><span class="sxs-lookup"><span data-stu-id="61bf2-115">impossibleTravelRiskEvent</span></span>](impossibletravelriskevent.md) | <span data-ttu-id="61bf2-116">Imposible desplazarse a ubicaciones atípicos.</span><span class="sxs-lookup"><span data-stu-id="61bf2-116">Impossible travel to atypical locations.</span></span> |
|[<span data-ttu-id="61bf2-117">leakedCredentialsRiskEvent</span><span class="sxs-lookup"><span data-stu-id="61bf2-117">leakedCredentialsRiskEvent</span></span>](leakedcredentialsriskevent.md) | <span data-ttu-id="61bf2-118">Usuarios con credenciales perdidas.</span><span class="sxs-lookup"><span data-stu-id="61bf2-118">Users with leaked credentials.</span></span> |
|[<span data-ttu-id="61bf2-119">suspiciousIpRiskEvent</span><span class="sxs-lookup"><span data-stu-id="61bf2-119">suspiciousIpRiskEvent</span></span>](suspiciousipriskevent.md) | <span data-ttu-id="61bf2-120">Inicios de sesión desde sospechosas direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="61bf2-120">Sign-ins from suspicious IP addresses.</span></span> |
|[<span data-ttu-id="61bf2-121">unfamiliarLocationRiskEvent</span><span class="sxs-lookup"><span data-stu-id="61bf2-121">unfamiliarLocationRiskEvent</span></span>](unfamiliarlocationriskevent.md) | <span data-ttu-id="61bf2-122">Inicios de sesión desde ubicaciones no están familiarizadas.</span><span class="sxs-lookup"><span data-stu-id="61bf2-122">Sign-ins from unfamiliar locations.</span></span> |

<span data-ttu-id="61bf2-123">Obtener información completa acerca de los eventos de riesgo puede encontrarse en la [documentación de protección de la identidad de AD de Azure](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-reporting-risk-events).</span><span class="sxs-lookup"><span data-stu-id="61bf2-123">Complete information about risk events can be found in the [Azure AD Identity Protection documentation](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-reporting-risk-events).</span></span>

## <a name="methods"></a><span data-ttu-id="61bf2-124">Métodos</span><span class="sxs-lookup"><span data-stu-id="61bf2-124">Methods</span></span>

| <span data-ttu-id="61bf2-125">Método</span><span class="sxs-lookup"><span data-stu-id="61bf2-125">Method</span></span>           | <span data-ttu-id="61bf2-126">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61bf2-126">Return Type</span></span>    |<span data-ttu-id="61bf2-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="61bf2-127">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="61bf2-128">Obtener identityRiskEvent</span><span class="sxs-lookup"><span data-stu-id="61bf2-128">Get identityRiskEvent</span></span>](../api/identityriskevent-get.md) | [<span data-ttu-id="61bf2-129">identityRiskEvent</span><span class="sxs-lookup"><span data-stu-id="61bf2-129">identityRiskEvent</span></span>](identityriskevent.md) |<span data-ttu-id="61bf2-130">Leer las propiedades y las relaciones del objeto identityRiskEvent.</span><span class="sxs-lookup"><span data-stu-id="61bf2-130">Read properties and relationships of identityRiskEvent object.</span></span>|

## <a name="properties"></a><span data-ttu-id="61bf2-131">Propiedades</span><span class="sxs-lookup"><span data-stu-id="61bf2-131">Properties</span></span>
| <span data-ttu-id="61bf2-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="61bf2-132">Property</span></span>     | <span data-ttu-id="61bf2-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="61bf2-133">Type</span></span>   |<span data-ttu-id="61bf2-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="61bf2-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="61bf2-135">closedDateTime</span><span class="sxs-lookup"><span data-stu-id="61bf2-135">closedDateTime</span></span>|<span data-ttu-id="61bf2-136">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="61bf2-136">dateTimeOffset</span></span>| <span data-ttu-id="61bf2-137">La fecha y hora en que se ha cerrado el evento de riesgo</span><span class="sxs-lookup"><span data-stu-id="61bf2-137">The date and time that the risk event was closed</span></span>|
|<span data-ttu-id="61bf2-138">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="61bf2-138">createdDateTime</span></span>|<span data-ttu-id="61bf2-139">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="61bf2-139">dateTimeOffset</span></span>| <span data-ttu-id="61bf2-140">La fecha y hora en que se creó el evento de riesgo.</span><span class="sxs-lookup"><span data-stu-id="61bf2-140">The date and time that the risk event was created.</span></span> <span data-ttu-id="61bf2-141">Siempre es mayor o igual que la fecha y hora del evento riesgo propio.</span><span class="sxs-lookup"><span data-stu-id="61bf2-141">This is always greater than or equal to the datetime of the risk event itself.</span></span> <span data-ttu-id="61bf2-142">Ésta es la propiedad correcta para utilizar como filtro al consultar los eventos de riesgo.</span><span class="sxs-lookup"><span data-stu-id="61bf2-142">This is the correct property to use as a filter when querying risk events.</span></span>|
|<span data-ttu-id="61bf2-143">id</span><span class="sxs-lookup"><span data-stu-id="61bf2-143">id</span></span>|<span data-ttu-id="61bf2-144">string</span><span class="sxs-lookup"><span data-stu-id="61bf2-144">string</span></span>| <span data-ttu-id="61bf2-145">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="61bf2-145">Read-only</span></span>|
|<span data-ttu-id="61bf2-146">riskEventDateTime</span><span class="sxs-lookup"><span data-stu-id="61bf2-146">riskEventDateTime</span></span>|<span data-ttu-id="61bf2-147">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="61bf2-147">dateTimeOffset</span></span>| <span data-ttu-id="61bf2-148">Fecha y hora en que se produjo el evento de riesgo</span><span class="sxs-lookup"><span data-stu-id="61bf2-148">The date and time when the risk event occurred</span></span>|
|<span data-ttu-id="61bf2-149">riskEventStatus</span><span class="sxs-lookup"><span data-stu-id="61bf2-149">riskEventStatus</span></span>|<span data-ttu-id="61bf2-150">string</span><span class="sxs-lookup"><span data-stu-id="61bf2-150">string</span></span>| <span data-ttu-id="61bf2-151">Los valores posibles son: `active`, `remediated`, `dismissedAsFixed`, `dismissedAsFalsePositive`, `dismissedAsIgnore`, `loginBlocked`, `closedMfaAuto` y `closedMultipleReasons`.</span><span class="sxs-lookup"><span data-stu-id="61bf2-151">Possible values are: `active`, `remediated`, `dismissedAsFixed`, `dismissedAsFalsePositive`, `dismissedAsIgnore`, `loginBlocked`, `closedMfaAuto`, `closedMultipleReasons`.</span></span>|
|<span data-ttu-id="61bf2-152">riskLevel</span><span class="sxs-lookup"><span data-stu-id="61bf2-152">riskLevel</span></span>|<span data-ttu-id="61bf2-153">string</span><span class="sxs-lookup"><span data-stu-id="61bf2-153">string</span></span>| <span data-ttu-id="61bf2-154">Los valores posibles son: `low`, `medium` y `high`.</span><span class="sxs-lookup"><span data-stu-id="61bf2-154">Possible values are: `low`, `medium`, `high`.</span></span>|
|<span data-ttu-id="61bf2-155">riskEventType</span><span class="sxs-lookup"><span data-stu-id="61bf2-155">riskEventType</span></span>|<span data-ttu-id="61bf2-156">string</span><span class="sxs-lookup"><span data-stu-id="61bf2-156">string</span></span>| <span data-ttu-id="61bf2-157">El tipo de riesgo</span><span class="sxs-lookup"><span data-stu-id="61bf2-157">The type of risk</span></span>|
|<span data-ttu-id="61bf2-158">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="61bf2-158">userDisplayName</span></span>|<span data-ttu-id="61bf2-159">string</span><span class="sxs-lookup"><span data-stu-id="61bf2-159">string</span></span>| <span data-ttu-id="61bf2-160">El nombre del usuario en riesgo</span><span class="sxs-lookup"><span data-stu-id="61bf2-160">The name of the user at risk</span></span>|
|<span data-ttu-id="61bf2-161">userId</span><span class="sxs-lookup"><span data-stu-id="61bf2-161">userId</span></span>|<span data-ttu-id="61bf2-162">string</span><span class="sxs-lookup"><span data-stu-id="61bf2-162">string</span></span>| <span data-ttu-id="61bf2-163">El identificador del usuario en riesgo</span><span class="sxs-lookup"><span data-stu-id="61bf2-163">The id of the user at risk</span></span>|
|<span data-ttu-id="61bf2-164">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="61bf2-164">userPrincipalName</span></span>|<span data-ttu-id="61bf2-165">string</span><span class="sxs-lookup"><span data-stu-id="61bf2-165">string</span></span>| <span data-ttu-id="61bf2-166">El nombre principal de usuario del usuario en riesgo</span><span class="sxs-lookup"><span data-stu-id="61bf2-166">The user principal name of the user at risk</span></span>|

## <a name="relationships"></a><span data-ttu-id="61bf2-167">Relaciones</span><span class="sxs-lookup"><span data-stu-id="61bf2-167">Relationships</span></span>
| <span data-ttu-id="61bf2-168">Relación</span><span class="sxs-lookup"><span data-stu-id="61bf2-168">Relationship</span></span> | <span data-ttu-id="61bf2-169">Tipo</span><span class="sxs-lookup"><span data-stu-id="61bf2-169">Type</span></span>   |<span data-ttu-id="61bf2-170">Descripción</span><span class="sxs-lookup"><span data-stu-id="61bf2-170">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="61bf2-171">impactedUser</span><span class="sxs-lookup"><span data-stu-id="61bf2-171">impactedUser</span></span>|[<span data-ttu-id="61bf2-172">user</span><span class="sxs-lookup"><span data-stu-id="61bf2-172">user</span></span>](user.md)| <span data-ttu-id="61bf2-p105">Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="61bf2-p105">Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="61bf2-175">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="61bf2-175">JSON representation</span></span>

<span data-ttu-id="61bf2-176">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="61bf2-176">Here is a JSON representation of the resource.</span></span> 

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.identityRiskEvent"
}-->

```json
{
  "closedDateTime": "String (timestamp)",
  "createdDateTime": "String (timestamp)",
  "id": "string (identifier)",
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
  "description": "identityRiskEvent resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->