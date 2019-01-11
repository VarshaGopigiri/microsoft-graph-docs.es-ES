---
title: tipo de recurso identityRiskEvent
description: 'Un evento de riesgo detectado por la protección de identidad de Azure Active Directory. Es el tipo base para cada tipo de evento de riesgo específico:'
author: cloudhandler
localization_priority: Normal
ms.openlocfilehash: 0735599c260fac178b54ee4ba54a17f5ea027e23
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27859000"
---
# <a name="identityriskevent-resource-type"></a><span data-ttu-id="df64b-104">tipo de recurso identityRiskEvent</span><span class="sxs-lookup"><span data-stu-id="df64b-104">identityRiskEvent resource type</span></span>

> <span data-ttu-id="df64b-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="df64b-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="df64b-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="df64b-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="df64b-107">Un evento de riesgo detectado por la [Protección de identidad de Azure Active Directory](https://azure.microsoft.com/en-us/documentation/articles/active-directory-identityprotection/).</span><span class="sxs-lookup"><span data-stu-id="df64b-107">A risk event detected by [Azure Active Directory Identity Protection](https://azure.microsoft.com/en-us/documentation/articles/active-directory-identityprotection/).</span></span> <span data-ttu-id="df64b-108">Es el tipo base para cada tipo de evento de riesgo específico:</span><span class="sxs-lookup"><span data-stu-id="df64b-108">It is the base type for each specific risk event type:</span></span>

| <span data-ttu-id="df64b-109">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="df64b-109">Event type</span></span>         | <span data-ttu-id="df64b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="df64b-110">Description</span></span>|
|:---------------|:-----------|
|[<span data-ttu-id="df64b-111">anonymousipRiskEvent</span><span class="sxs-lookup"><span data-stu-id="df64b-111">anonymousipRiskEvent</span></span>](anonymousipriskevent.md) | <span data-ttu-id="df64b-112">Inicios de sesión desde las direcciones IP anónimas.</span><span class="sxs-lookup"><span data-stu-id="df64b-112">Sign-ins from anonymous IP addresses.</span></span> |
|[<span data-ttu-id="df64b-113">malwareRiskEvent</span><span class="sxs-lookup"><span data-stu-id="df64b-113">malwareRiskEvent</span></span>](malwareriskevent.md) | <span data-ttu-id="df64b-114">Inicios de sesión desde dispositivos infectados con malware.</span><span class="sxs-lookup"><span data-stu-id="df64b-114">Sign-ins from malware-infected devices.</span></span> |
|[<span data-ttu-id="df64b-115">impossibleTravelRiskEvent</span><span class="sxs-lookup"><span data-stu-id="df64b-115">impossibleTravelRiskEvent</span></span>](impossibletravelriskevent.md) | <span data-ttu-id="df64b-116">Imposible desplazarse a ubicaciones atípicos.</span><span class="sxs-lookup"><span data-stu-id="df64b-116">Impossible travel to atypical locations.</span></span> |
|[<span data-ttu-id="df64b-117">leakedCredentialsRiskEvent</span><span class="sxs-lookup"><span data-stu-id="df64b-117">leakedCredentialsRiskEvent</span></span>](leakedcredentialsriskevent.md) | <span data-ttu-id="df64b-118">Usuarios con credenciales perdidas.</span><span class="sxs-lookup"><span data-stu-id="df64b-118">Users with leaked credentials.</span></span> |
|[<span data-ttu-id="df64b-119">suspiciousIpRiskEvent</span><span class="sxs-lookup"><span data-stu-id="df64b-119">suspiciousIpRiskEvent</span></span>](suspiciousipriskevent.md) | <span data-ttu-id="df64b-120">Inicios de sesión desde sospechosas direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="df64b-120">Sign-ins from suspicious IP addresses.</span></span> |
|[<span data-ttu-id="df64b-121">unfamiliarLocationRiskEvent</span><span class="sxs-lookup"><span data-stu-id="df64b-121">unfamiliarLocationRiskEvent</span></span>](unfamiliarlocationriskevent.md) | <span data-ttu-id="df64b-122">Inicios de sesión desde ubicaciones no están familiarizadas.</span><span class="sxs-lookup"><span data-stu-id="df64b-122">Sign-ins from unfamiliar locations.</span></span> |

<span data-ttu-id="df64b-123">Obtener información completa acerca de los eventos de riesgo puede encontrarse en la [documentación de protección de la identidad de AD de Azure](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-reporting-risk-events).</span><span class="sxs-lookup"><span data-stu-id="df64b-123">Complete information about risk events can be found in the [Azure AD Identity Protection documentation](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-reporting-risk-events).</span></span>

## <a name="methods"></a><span data-ttu-id="df64b-124">Métodos</span><span class="sxs-lookup"><span data-stu-id="df64b-124">Methods</span></span>

| <span data-ttu-id="df64b-125">Método</span><span class="sxs-lookup"><span data-stu-id="df64b-125">Method</span></span>           | <span data-ttu-id="df64b-126">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="df64b-126">Return Type</span></span>    |<span data-ttu-id="df64b-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="df64b-127">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="df64b-128">Obtener identityRiskEvent</span><span class="sxs-lookup"><span data-stu-id="df64b-128">Get identityRiskEvent</span></span>](../api/identityriskevent-get.md) | [<span data-ttu-id="df64b-129">identityRiskEvent</span><span class="sxs-lookup"><span data-stu-id="df64b-129">identityRiskEvent</span></span>](identityriskevent.md) |<span data-ttu-id="df64b-130">Leer las propiedades y las relaciones del objeto identityRiskEvent.</span><span class="sxs-lookup"><span data-stu-id="df64b-130">Read properties and relationships of identityRiskEvent object.</span></span>|

## <a name="properties"></a><span data-ttu-id="df64b-131">Propiedades</span><span class="sxs-lookup"><span data-stu-id="df64b-131">Properties</span></span>
| <span data-ttu-id="df64b-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="df64b-132">Property</span></span>     | <span data-ttu-id="df64b-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="df64b-133">Type</span></span>   |<span data-ttu-id="df64b-134">Description</span><span class="sxs-lookup"><span data-stu-id="df64b-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="df64b-135">closedDateTime</span><span class="sxs-lookup"><span data-stu-id="df64b-135">closedDateTime</span></span>|<span data-ttu-id="df64b-136">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="df64b-136">dateTimeOffset</span></span>| <span data-ttu-id="df64b-137">La fecha y hora en que se ha cerrado el evento de riesgo</span><span class="sxs-lookup"><span data-stu-id="df64b-137">The date and time that the risk event was closed</span></span>|
|<span data-ttu-id="df64b-138">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="df64b-138">createdDateTime</span></span>|<span data-ttu-id="df64b-139">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="df64b-139">dateTimeOffset</span></span>| <span data-ttu-id="df64b-140">La fecha y hora en que se creó el evento de riesgo.</span><span class="sxs-lookup"><span data-stu-id="df64b-140">The date and time that the risk event was created.</span></span> <span data-ttu-id="df64b-141">Siempre es mayor o igual que la fecha y hora del evento riesgo propio.</span><span class="sxs-lookup"><span data-stu-id="df64b-141">This is always greater than or equal to the datetime of the risk event itself.</span></span> <span data-ttu-id="df64b-142">Ésta es la propiedad correcta para utilizar como filtro al consultar los eventos de riesgo.</span><span class="sxs-lookup"><span data-stu-id="df64b-142">This is the correct property to use as a filter when querying risk events.</span></span>|
|<span data-ttu-id="df64b-143">id</span><span class="sxs-lookup"><span data-stu-id="df64b-143">id</span></span>|<span data-ttu-id="df64b-144">string</span><span class="sxs-lookup"><span data-stu-id="df64b-144">string</span></span>| <span data-ttu-id="df64b-145">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="df64b-145">Read-only</span></span>|
|<span data-ttu-id="df64b-146">riskEventDateTime</span><span class="sxs-lookup"><span data-stu-id="df64b-146">riskEventDateTime</span></span>|<span data-ttu-id="df64b-147">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="df64b-147">dateTimeOffset</span></span>| <span data-ttu-id="df64b-148">Fecha y hora en que se produjo el evento de riesgo</span><span class="sxs-lookup"><span data-stu-id="df64b-148">The date and time when the risk event occurred</span></span>|
|<span data-ttu-id="df64b-149">riskEventStatus</span><span class="sxs-lookup"><span data-stu-id="df64b-149">riskEventStatus</span></span>|<span data-ttu-id="df64b-150">string</span><span class="sxs-lookup"><span data-stu-id="df64b-150">string</span></span>| <span data-ttu-id="df64b-151">Los valores posibles son: `active`, `remediated`, `dismissedAsFixed`, `dismissedAsFalsePositive`, `dismissedAsIgnore`, `loginBlocked`, `closedMfaAuto` y `closedMultipleReasons`.</span><span class="sxs-lookup"><span data-stu-id="df64b-151">Possible values are: `active`, `remediated`, `dismissedAsFixed`, `dismissedAsFalsePositive`, `dismissedAsIgnore`, `loginBlocked`, `closedMfaAuto`, `closedMultipleReasons`.</span></span>|
|<span data-ttu-id="df64b-152">riskLevel</span><span class="sxs-lookup"><span data-stu-id="df64b-152">riskLevel</span></span>|<span data-ttu-id="df64b-153">string</span><span class="sxs-lookup"><span data-stu-id="df64b-153">string</span></span>| <span data-ttu-id="df64b-154">Los valores posibles son: `low`, `medium` y `high`.</span><span class="sxs-lookup"><span data-stu-id="df64b-154">Possible values are: `low`, `medium`, `high`.</span></span>|
|<span data-ttu-id="df64b-155">riskEventType</span><span class="sxs-lookup"><span data-stu-id="df64b-155">riskEventType</span></span>|<span data-ttu-id="df64b-156">string</span><span class="sxs-lookup"><span data-stu-id="df64b-156">string</span></span>| <span data-ttu-id="df64b-157">El tipo de riesgo</span><span class="sxs-lookup"><span data-stu-id="df64b-157">The type of risk</span></span>|
|<span data-ttu-id="df64b-158">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="df64b-158">userDisplayName</span></span>|<span data-ttu-id="df64b-159">string</span><span class="sxs-lookup"><span data-stu-id="df64b-159">string</span></span>| <span data-ttu-id="df64b-160">El nombre del usuario en riesgo</span><span class="sxs-lookup"><span data-stu-id="df64b-160">The name of the user at risk</span></span>|
|<span data-ttu-id="df64b-161">userId</span><span class="sxs-lookup"><span data-stu-id="df64b-161">userId</span></span>|<span data-ttu-id="df64b-162">string</span><span class="sxs-lookup"><span data-stu-id="df64b-162">string</span></span>| <span data-ttu-id="df64b-163">El identificador del usuario en riesgo</span><span class="sxs-lookup"><span data-stu-id="df64b-163">The id of the user at risk</span></span>|
|<span data-ttu-id="df64b-164">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="df64b-164">userPrincipalName</span></span>|<span data-ttu-id="df64b-165">string</span><span class="sxs-lookup"><span data-stu-id="df64b-165">string</span></span>| <span data-ttu-id="df64b-166">El nombre principal de usuario del usuario en riesgo</span><span class="sxs-lookup"><span data-stu-id="df64b-166">The user principal name of the user at risk</span></span>|

## <a name="relationships"></a><span data-ttu-id="df64b-167">Relaciones</span><span class="sxs-lookup"><span data-stu-id="df64b-167">Relationships</span></span>
| <span data-ttu-id="df64b-168">Relación</span><span class="sxs-lookup"><span data-stu-id="df64b-168">Relationship</span></span> | <span data-ttu-id="df64b-169">Tipo</span><span class="sxs-lookup"><span data-stu-id="df64b-169">Type</span></span>   |<span data-ttu-id="df64b-170">Description</span><span class="sxs-lookup"><span data-stu-id="df64b-170">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="df64b-171">impactedUser</span><span class="sxs-lookup"><span data-stu-id="df64b-171">impactedUser</span></span>|[<span data-ttu-id="df64b-172">user</span><span class="sxs-lookup"><span data-stu-id="df64b-172">user</span></span>](user.md)| <span data-ttu-id="df64b-p105">Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="df64b-p105">Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="df64b-175">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="df64b-175">JSON representation</span></span>

<span data-ttu-id="df64b-176">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="df64b-176">Here is a JSON representation of the resource.</span></span> 

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
