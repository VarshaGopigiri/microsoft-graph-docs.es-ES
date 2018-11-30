---
title: tipo de recurso locatedRiskEvent
description: 'Un evento de riesgo detectado por Azure Active Directory protección de identidad que se basa en datos de ubicación. Tipos de eventos de riesgo encuentra incluyen:'
ms.openlocfilehash: e84cff5985905977b6b1eeb75a9ef9703a2a2078
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086066"
---
# <a name="locatedriskevent-resource-type"></a><span data-ttu-id="d0374-104">tipo de recurso locatedRiskEvent</span><span class="sxs-lookup"><span data-stu-id="d0374-104">locatedRiskEvent resource type</span></span>

> <span data-ttu-id="d0374-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d0374-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d0374-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d0374-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d0374-107">Un evento de riesgo detectado por la [Protección de identidad de Azure Active Directory](https://azure.microsoft.com/en-us/documentation/articles/active-directory-identityprotection/) que se basa en datos de ubicación.</span><span class="sxs-lookup"><span data-stu-id="d0374-107">A risk event detected by [Azure Active Directory Identity Protection](https://azure.microsoft.com/en-us/documentation/articles/active-directory-identityprotection/) that is based on location data.</span></span> <span data-ttu-id="d0374-108">Tipos de eventos de riesgo encuentra incluyen:</span><span class="sxs-lookup"><span data-stu-id="d0374-108">Located risk event types include:</span></span>
* [<span data-ttu-id="d0374-109">inicios de sesión desde las direcciones IP anónimas</span><span class="sxs-lookup"><span data-stu-id="d0374-109">sign-ins from anonymous IP addresses</span></span>](anonymousipriskevent.md)
* [<span data-ttu-id="d0374-110">inicios de sesión desde dispositivos infectados con malware</span><span class="sxs-lookup"><span data-stu-id="d0374-110">sign-ins from malware-infected devices</span></span>](malwareriskevent.md)
* [<span data-ttu-id="d0374-111">Imposible desplazarse a ubicaciones atípicos</span><span class="sxs-lookup"><span data-stu-id="d0374-111">impossible travel to atypical locations</span></span>](impossibletravelriskevent.md)
* [<span data-ttu-id="d0374-112">inicios de sesión desde sospechosas direcciones IP</span><span class="sxs-lookup"><span data-stu-id="d0374-112">sign-ins from suspicious IP addresses</span></span>](suspiciousipriskevent.md)
* <span data-ttu-id="d0374-113">[inicios de sesión desde ubicaciones familiarizadas](unfamiliarlocationriskevent.md) Obtener información completa acerca de los eventos de riesgo puede encontrarse en la [documentación de protección de la identidad de AD de Azure](https://azure.microsoft.com/en-us/documentation/articles/active-directory-identityprotection-risk-events-types/).</span><span class="sxs-lookup"><span data-stu-id="d0374-113">[sign-ins from unfamiliar locations](unfamiliarlocationriskevent.md) Complete information about risk events can be found in the [Azure AD Identity Protection documentation](https://azure.microsoft.com/en-us/documentation/articles/active-directory-identityprotection-risk-events-types/).</span></span>


## <a name="methods"></a><span data-ttu-id="d0374-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="d0374-114">Methods</span></span>

| <span data-ttu-id="d0374-115">Método</span><span class="sxs-lookup"><span data-stu-id="d0374-115">Method</span></span>           | <span data-ttu-id="d0374-116">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0374-116">Return Type</span></span>    |<span data-ttu-id="d0374-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0374-117">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="d0374-118">Obtener locatedRiskEvent</span><span class="sxs-lookup"><span data-stu-id="d0374-118">Get locatedRiskEvent</span></span>](../api/locatedriskevent-get.md) | [<span data-ttu-id="d0374-119">locatedRiskEvent</span><span class="sxs-lookup"><span data-stu-id="d0374-119">locatedRiskEvent</span></span>](locatedriskevent.md) |<span data-ttu-id="d0374-120">Leer las propiedades y las relaciones del objeto locatedRiskEvent.</span><span class="sxs-lookup"><span data-stu-id="d0374-120">Read properties and relationships of locatedRiskEvent object.</span></span>|

## <a name="properties"></a><span data-ttu-id="d0374-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d0374-121">Properties</span></span>
| <span data-ttu-id="d0374-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d0374-122">Property</span></span>     | <span data-ttu-id="d0374-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="d0374-123">Type</span></span>   |<span data-ttu-id="d0374-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0374-124">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d0374-125">closedDateTime</span><span class="sxs-lookup"><span data-stu-id="d0374-125">closedDateTime</span></span>|<span data-ttu-id="d0374-126">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d0374-126">dateTimeOffset</span></span>| <span data-ttu-id="d0374-127">La fecha y hora en que se ha cerrado el evento de riesgo</span><span class="sxs-lookup"><span data-stu-id="d0374-127">The date and time that the risk event was closed</span></span>|
|<span data-ttu-id="d0374-128">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="d0374-128">createdDateTime</span></span>|<span data-ttu-id="d0374-129">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d0374-129">dateTimeOffset</span></span>| <span data-ttu-id="d0374-130">La fecha y hora en que se creó el evento de riesgo.</span><span class="sxs-lookup"><span data-stu-id="d0374-130">The date and time that the risk event was created.</span></span> <span data-ttu-id="d0374-131">Siempre es mayor o igual que la fecha y hora del evento riesgo propio.</span><span class="sxs-lookup"><span data-stu-id="d0374-131">This is always greater than or equal to the datetime of the risk event itself.</span></span> <span data-ttu-id="d0374-132">Ésta es la propiedad correcta para utilizar como filtro al consultar los eventos de riesgo.</span><span class="sxs-lookup"><span data-stu-id="d0374-132">This is the correct property to use as a filter when querying risk events.</span></span>|
|<span data-ttu-id="d0374-133">id</span><span class="sxs-lookup"><span data-stu-id="d0374-133">id</span></span>|<span data-ttu-id="d0374-134">string</span><span class="sxs-lookup"><span data-stu-id="d0374-134">string</span></span>| <span data-ttu-id="d0374-135">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0374-135">Read-only</span></span>|
|<span data-ttu-id="d0374-136">ipAddress</span><span class="sxs-lookup"><span data-stu-id="d0374-136">ipAddress</span></span>|<span data-ttu-id="d0374-137">string</span><span class="sxs-lookup"><span data-stu-id="d0374-137">string</span></span>| <span data-ttu-id="d0374-138">La dirección IP de inicio de sesión de</span><span class="sxs-lookup"><span data-stu-id="d0374-138">The IP address of the sign-in</span></span>|
|<span data-ttu-id="d0374-139">location</span><span class="sxs-lookup"><span data-stu-id="d0374-139">location</span></span>|<span data-ttu-id="d0374-140">string</span><span class="sxs-lookup"><span data-stu-id="d0374-140">string</span></span>| <span data-ttu-id="d0374-141">La ubicación que se adjunta a la dirección IP de inicio de sesión de</span><span class="sxs-lookup"><span data-stu-id="d0374-141">The location attached to the IP address of the sign-in</span></span>|
|<span data-ttu-id="d0374-142">riskEventDateTime</span><span class="sxs-lookup"><span data-stu-id="d0374-142">riskEventDateTime</span></span>|<span data-ttu-id="d0374-143">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d0374-143">dateTimeOffset</span></span>| <span data-ttu-id="d0374-144">Fecha y hora en que se produjo el evento de riesgo</span><span class="sxs-lookup"><span data-stu-id="d0374-144">The date and time when the risk event occurred</span></span>|
|<span data-ttu-id="d0374-145">riskEventStatus</span><span class="sxs-lookup"><span data-stu-id="d0374-145">riskEventStatus</span></span>|<span data-ttu-id="d0374-146">string</span><span class="sxs-lookup"><span data-stu-id="d0374-146">string</span></span>| <span data-ttu-id="d0374-147">Los valores posibles son: `active`, `remediated`, `dismissedAsFixed`, `dismissedAsFalsePositive`, `dismissedAsIgnore`, `loginBlocked`, `closedMfaAuto` y `closedMultipleReasons`.</span><span class="sxs-lookup"><span data-stu-id="d0374-147">Possible values are: `active`, `remediated`, `dismissedAsFixed`, `dismissedAsFalsePositive`, `dismissedAsIgnore`, `loginBlocked`, `closedMfaAuto`, `closedMultipleReasons`.</span></span>|
|<span data-ttu-id="d0374-148">riskLevel</span><span class="sxs-lookup"><span data-stu-id="d0374-148">riskLevel</span></span>|<span data-ttu-id="d0374-149">string</span><span class="sxs-lookup"><span data-stu-id="d0374-149">string</span></span>| <span data-ttu-id="d0374-150">Los valores posibles son: `low`, `medium` y `high`.</span><span class="sxs-lookup"><span data-stu-id="d0374-150">Possible values are: `low`, `medium`, `high`.</span></span>|
|<span data-ttu-id="d0374-151">riskEventType</span><span class="sxs-lookup"><span data-stu-id="d0374-151">riskEventType</span></span>|<span data-ttu-id="d0374-152">string</span><span class="sxs-lookup"><span data-stu-id="d0374-152">string</span></span>| <span data-ttu-id="d0374-153">El tipo de riesgo</span><span class="sxs-lookup"><span data-stu-id="d0374-153">The type of risk</span></span>|
|<span data-ttu-id="d0374-154">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="d0374-154">userDisplayName</span></span>|<span data-ttu-id="d0374-155">string</span><span class="sxs-lookup"><span data-stu-id="d0374-155">string</span></span>| <span data-ttu-id="d0374-156">El nombre del usuario en riesgo</span><span class="sxs-lookup"><span data-stu-id="d0374-156">The name of the user at risk</span></span>|
|<span data-ttu-id="d0374-157">userId</span><span class="sxs-lookup"><span data-stu-id="d0374-157">userId</span></span>|<span data-ttu-id="d0374-158">string</span><span class="sxs-lookup"><span data-stu-id="d0374-158">string</span></span>| <span data-ttu-id="d0374-159">El identificador del usuario en riesgo</span><span class="sxs-lookup"><span data-stu-id="d0374-159">The id of the user at risk</span></span>|
|<span data-ttu-id="d0374-160">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d0374-160">userPrincipalName</span></span>|<span data-ttu-id="d0374-161">string</span><span class="sxs-lookup"><span data-stu-id="d0374-161">string</span></span>| <span data-ttu-id="d0374-162">El nombre principal de usuario del usuario en riesgo</span><span class="sxs-lookup"><span data-stu-id="d0374-162">The user principal name of the user at risk</span></span>|

## <a name="relationships"></a><span data-ttu-id="d0374-163">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d0374-163">Relationships</span></span>
| <span data-ttu-id="d0374-164">Relación</span><span class="sxs-lookup"><span data-stu-id="d0374-164">Relationship</span></span> | <span data-ttu-id="d0374-165">Tipo</span><span class="sxs-lookup"><span data-stu-id="d0374-165">Type</span></span>   |<span data-ttu-id="d0374-166">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0374-166">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d0374-167">impactedUser</span><span class="sxs-lookup"><span data-stu-id="d0374-167">impactedUser</span></span>|[<span data-ttu-id="d0374-168">user</span><span class="sxs-lookup"><span data-stu-id="d0374-168">user</span></span>](user.md)| <span data-ttu-id="d0374-p105">Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="d0374-p105">Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="d0374-171">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d0374-171">JSON representation</span></span>

<span data-ttu-id="d0374-172">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d0374-172">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.locatedRiskEvent"
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
  "description": "locatedRiskEvent resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->