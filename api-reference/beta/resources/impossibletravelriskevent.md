---
title: tipo de recurso impossibleTravelRiskEvent
description: Un evento de riesgo detectado por Azure Active Directory protección de identidad donde se producen inicios de sesión de cuenta dos desde ubicaciones atípicos para el usuario y sería imposible de viajes entre las ubicaciones de la duración entre la información de inicio de sesión complementos. completa acerca de eventos de riesgo pueden encontrarse en la documentación de protección de la identidad de AD de Azure.
ms.openlocfilehash: 38e61927121f520e79fd1fec8b8e6443fa8b76e7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083453"
---
# <a name="impossibletravelriskevent-resource-type"></a><span data-ttu-id="88241-103">tipo de recurso impossibleTravelRiskEvent</span><span class="sxs-lookup"><span data-stu-id="88241-103">impossibleTravelRiskEvent resource type</span></span>

> <span data-ttu-id="88241-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="88241-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="88241-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="88241-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="88241-106">Un evento de riesgo detectado por la [Protección de identidad de Azure Active Directory](https://azure.microsoft.com/en-us/documentation/articles/active-directory-identityprotection/) donde se producen inicios de sesión de cuenta dos desde ubicaciones atípicos para el usuario y sería imposible de viajes entre las ubicaciones de la duración entre el completo de inicio de sesión complementos. puede encontrar información acerca de los eventos de riesgo en la [documentación de protección de la identidad de Azure AD](https://azure.microsoft.com/en-us/documentation/articles/active-directory-identityprotection-risk-events-types/).</span><span class="sxs-lookup"><span data-stu-id="88241-106">A risk event detected by [Azure Active Directory Identity Protection](https://azure.microsoft.com/en-us/documentation/articles/active-directory-identityprotection/) where two account sign-ins occur from locations atypical for the user and it would be impossible to travel between the locations in the duration between the sign-ins. Complete information about risk events can be found in the [Azure AD Identity Protection documentation](https://azure.microsoft.com/en-us/documentation/articles/active-directory-identityprotection-risk-events-types/).</span></span>


## <a name="methods"></a><span data-ttu-id="88241-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="88241-107">Methods</span></span>

| <span data-ttu-id="88241-108">Método</span><span class="sxs-lookup"><span data-stu-id="88241-108">Method</span></span>           | <span data-ttu-id="88241-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="88241-109">Return Type</span></span>    |<span data-ttu-id="88241-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="88241-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="88241-111">Obtener impossibleTravelRiskEvent</span><span class="sxs-lookup"><span data-stu-id="88241-111">Get impossibleTravelRiskEvent</span></span>](../api/impossibletravelriskevent-get.md) | [<span data-ttu-id="88241-112">impossibleTravelRiskEvent</span><span class="sxs-lookup"><span data-stu-id="88241-112">impossibleTravelRiskEvent</span></span>](impossibletravelriskevent.md) |<span data-ttu-id="88241-113">Leer las propiedades y las relaciones del objeto impossibleTravelRiskEvent.</span><span class="sxs-lookup"><span data-stu-id="88241-113">Read properties and relationships of impossibleTravelRiskEvent object.</span></span>|

## <a name="properties"></a><span data-ttu-id="88241-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="88241-114">Properties</span></span>
| <span data-ttu-id="88241-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="88241-115">Property</span></span>     | <span data-ttu-id="88241-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="88241-116">Type</span></span>   |<span data-ttu-id="88241-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="88241-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="88241-118">closedDateTime</span><span class="sxs-lookup"><span data-stu-id="88241-118">closedDateTime</span></span>|<span data-ttu-id="88241-119">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="88241-119">dateTimeOffset</span></span>| <span data-ttu-id="88241-120">La fecha y hora en que se ha cerrado el evento de riesgo</span><span class="sxs-lookup"><span data-stu-id="88241-120">The date and time that the risk event was closed</span></span>|
|<span data-ttu-id="88241-121">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="88241-121">createdDateTime</span></span>|<span data-ttu-id="88241-122">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="88241-122">dateTimeOffset</span></span>| <span data-ttu-id="88241-123">La fecha y hora en que se creó el evento de riesgo.</span><span class="sxs-lookup"><span data-stu-id="88241-123">The date and time that the risk event was created.</span></span> <span data-ttu-id="88241-124">Siempre es mayor o igual que la fecha y hora del evento riesgo propio.</span><span class="sxs-lookup"><span data-stu-id="88241-124">This is always greater than or equal to the datetime of the risk event itself.</span></span> <span data-ttu-id="88241-125">Ésta es la propiedad correcta para utilizar como filtro al consultar los eventos de riesgo.</span><span class="sxs-lookup"><span data-stu-id="88241-125">This is the correct property to use as a filter when querying risk events.</span></span>|
|<span data-ttu-id="88241-126">deviceInformation</span><span class="sxs-lookup"><span data-stu-id="88241-126">deviceInformation</span></span>|<span data-ttu-id="88241-127">string</span><span class="sxs-lookup"><span data-stu-id="88241-127">string</span></span>| <span data-ttu-id="88241-128">Información sobre el dispositivo</span><span class="sxs-lookup"><span data-stu-id="88241-128">Information about the device</span></span>|
|<span data-ttu-id="88241-129">id</span><span class="sxs-lookup"><span data-stu-id="88241-129">id</span></span>|<span data-ttu-id="88241-130">string</span><span class="sxs-lookup"><span data-stu-id="88241-130">string</span></span>| <span data-ttu-id="88241-131">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="88241-131">Read-only</span></span>|
|<span data-ttu-id="88241-132">ipAddress</span><span class="sxs-lookup"><span data-stu-id="88241-132">ipAddress</span></span>|<span data-ttu-id="88241-133">string</span><span class="sxs-lookup"><span data-stu-id="88241-133">string</span></span>| <span data-ttu-id="88241-134">La dirección IP del segundo inicio de sesión de</span><span class="sxs-lookup"><span data-stu-id="88241-134">The IP address of the second sign-in</span></span>|
|<span data-ttu-id="88241-135">isAtypicalLocation</span><span class="sxs-lookup"><span data-stu-id="88241-135">isAtypicalLocation</span></span>|<span data-ttu-id="88241-136">boolean</span><span class="sxs-lookup"><span data-stu-id="88241-136">boolean</span></span>| <span data-ttu-id="88241-137">Si una de las ubicaciones es atípica para el usuario</span><span class="sxs-lookup"><span data-stu-id="88241-137">If one of the locations is atypical for the user</span></span>|
|<span data-ttu-id="88241-138">location</span><span class="sxs-lookup"><span data-stu-id="88241-138">location</span></span>|<span data-ttu-id="88241-139">string</span><span class="sxs-lookup"><span data-stu-id="88241-139">string</span></span>| <span data-ttu-id="88241-140">La ubicación que se adjunta a la dirección IP del segundo inicio de sesión de</span><span class="sxs-lookup"><span data-stu-id="88241-140">The location attached to the IP address of the second sign-in</span></span>|
|<span data-ttu-id="88241-141">previousIPAddress</span><span class="sxs-lookup"><span data-stu-id="88241-141">previousIPAddress</span></span>|<span data-ttu-id="88241-142">string</span><span class="sxs-lookup"><span data-stu-id="88241-142">string</span></span>| <span data-ttu-id="88241-143">La dirección IP del primer inicio de sesión de</span><span class="sxs-lookup"><span data-stu-id="88241-143">The IP address of the first sign-in</span></span>|
|<span data-ttu-id="88241-144">previousLocation</span><span class="sxs-lookup"><span data-stu-id="88241-144">previousLocation</span></span>|<span data-ttu-id="88241-145">string</span><span class="sxs-lookup"><span data-stu-id="88241-145">string</span></span>| <span data-ttu-id="88241-146">La ubicación que se adjunta a la dirección IP del primer inicio de sesión de</span><span class="sxs-lookup"><span data-stu-id="88241-146">The location attached to the IP address of the first sign-in</span></span>|
|<span data-ttu-id="88241-147">previousSigninDateTime</span><span class="sxs-lookup"><span data-stu-id="88241-147">previousSigninDateTime</span></span>|<span data-ttu-id="88241-148">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="88241-148">dateTimeOffset</span></span>| <span data-ttu-id="88241-149">La fecha y hora de inicio de sesión de la primera vez</span><span class="sxs-lookup"><span data-stu-id="88241-149">The date and time of the first sign-in</span></span>|
|<span data-ttu-id="88241-150">riskEventDateTime</span><span class="sxs-lookup"><span data-stu-id="88241-150">riskEventDateTime</span></span>|<span data-ttu-id="88241-151">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="88241-151">dateTimeOffset</span></span>| <span data-ttu-id="88241-152">La fecha y hora de inicio de sesión de la segunda vez</span><span class="sxs-lookup"><span data-stu-id="88241-152">The date and time of the second sign-in</span></span>|
|<span data-ttu-id="88241-153">riskEventStatus</span><span class="sxs-lookup"><span data-stu-id="88241-153">riskEventStatus</span></span>|<span data-ttu-id="88241-154">string</span><span class="sxs-lookup"><span data-stu-id="88241-154">string</span></span>| <span data-ttu-id="88241-155">Los valores posibles son: `active`, `remediated`, `dismissedAsFixed`, `dismissedAsFalsePositive`, `dismissedAsIgnore`, `loginBlocked`, `closedMfaAuto` y `closedMultipleReasons`.</span><span class="sxs-lookup"><span data-stu-id="88241-155">Possible values are: `active`, `remediated`, `dismissedAsFixed`, `dismissedAsFalsePositive`, `dismissedAsIgnore`, `loginBlocked`, `closedMfaAuto`, `closedMultipleReasons`.</span></span>|
|<span data-ttu-id="88241-156">riskLevel</span><span class="sxs-lookup"><span data-stu-id="88241-156">riskLevel</span></span>|<span data-ttu-id="88241-157">string</span><span class="sxs-lookup"><span data-stu-id="88241-157">string</span></span>| <span data-ttu-id="88241-158">Los valores posibles son: `low`, `medium` y `high`.</span><span class="sxs-lookup"><span data-stu-id="88241-158">Possible values are: `low`, `medium`, `high`.</span></span>|
|<span data-ttu-id="88241-159">riskEventType</span><span class="sxs-lookup"><span data-stu-id="88241-159">riskEventType</span></span>|<span data-ttu-id="88241-160">string</span><span class="sxs-lookup"><span data-stu-id="88241-160">string</span></span>| <span data-ttu-id="88241-161">El tipo de riesgo</span><span class="sxs-lookup"><span data-stu-id="88241-161">The type of risk</span></span>|
|<span data-ttu-id="88241-162">userAgent</span><span class="sxs-lookup"><span data-stu-id="88241-162">userAgent</span></span>|<span data-ttu-id="88241-163">string</span><span class="sxs-lookup"><span data-stu-id="88241-163">string</span></span>| <span data-ttu-id="88241-164">Cadena del agente de usuario del explorador</span><span class="sxs-lookup"><span data-stu-id="88241-164">The browser's user agent string</span></span>|
|<span data-ttu-id="88241-165">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="88241-165">userDisplayName</span></span>|<span data-ttu-id="88241-166">string</span><span class="sxs-lookup"><span data-stu-id="88241-166">string</span></span>| <span data-ttu-id="88241-167">El nombre del usuario en riesgo</span><span class="sxs-lookup"><span data-stu-id="88241-167">The name of the user at risk</span></span>|
|<span data-ttu-id="88241-168">userId</span><span class="sxs-lookup"><span data-stu-id="88241-168">userId</span></span>|<span data-ttu-id="88241-169">string</span><span class="sxs-lookup"><span data-stu-id="88241-169">string</span></span>| <span data-ttu-id="88241-170">El identificador del usuario en riesgo</span><span class="sxs-lookup"><span data-stu-id="88241-170">The id of the user at risk</span></span>|
|<span data-ttu-id="88241-171">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="88241-171">userPrincipalName</span></span>|<span data-ttu-id="88241-172">string</span><span class="sxs-lookup"><span data-stu-id="88241-172">string</span></span>| <span data-ttu-id="88241-173">El nombre principal de usuario del usuario en riesgo</span><span class="sxs-lookup"><span data-stu-id="88241-173">The user principal name of the user at risk</span></span>|

## <a name="relationships"></a><span data-ttu-id="88241-174">Relaciones</span><span class="sxs-lookup"><span data-stu-id="88241-174">Relationships</span></span>
| <span data-ttu-id="88241-175">Relación</span><span class="sxs-lookup"><span data-stu-id="88241-175">Relationship</span></span> | <span data-ttu-id="88241-176">Tipo</span><span class="sxs-lookup"><span data-stu-id="88241-176">Type</span></span>   |<span data-ttu-id="88241-177">Descripción</span><span class="sxs-lookup"><span data-stu-id="88241-177">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="88241-178">impactedUser</span><span class="sxs-lookup"><span data-stu-id="88241-178">impactedUser</span></span>|[<span data-ttu-id="88241-179">user</span><span class="sxs-lookup"><span data-stu-id="88241-179">user</span></span>](user.md)| <span data-ttu-id="88241-p103">Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="88241-p103">Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="88241-182">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="88241-182">JSON representation</span></span>

<span data-ttu-id="88241-183">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="88241-183">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.impossibleTravelRiskEvent"
}-->

```json
{
  "closedDateTime": "String (timestamp)",
  "createdDateTime": "String (timestamp)",
  "deviceInformation": "string",
  "id": "string (identifier)",
  "ipAddress": "string",
  "isAtypicalLocation": true,
  "location": "string",
  "previousIPAddress": "string",
  "previousLocation": "string",
  "previousSigninDateTime": "String (timestamp)",
  "riskEventDateTime": "String (timestamp)",
  "riskEventStatus": "string",
  "riskLevel": "string",
  "riskType": "string",
  "userAgent": "string",
  "userDisplayName": "string",
  "userId": "string",
  "userPrincipalName": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "impossibleTravelRiskEvent resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->