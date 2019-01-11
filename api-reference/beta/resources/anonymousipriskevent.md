---
title: tipo de recurso anonymousIpRiskEvent
description: Un evento de riesgo detectado por Azure Active Directory identidad protección donde un inicio de sesión de cuenta se intentó desde una dirección IP que aparece para ser anónimos. Obtener información completa acerca de los eventos de riesgo puede encontrarse en la documentación de protección de la identidad de AD de Azure.
localization_priority: Normal
ms.openlocfilehash: 9c170e234116ca76e4dabe021c0aa7949d1a66ca
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27848303"
---
# <a name="anonymousipriskevent-resource-type"></a><span data-ttu-id="de1d9-104">tipo de recurso anonymousIpRiskEvent</span><span class="sxs-lookup"><span data-stu-id="de1d9-104">anonymousIpRiskEvent resource type</span></span>

> <span data-ttu-id="de1d9-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="de1d9-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="de1d9-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="de1d9-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="de1d9-107">Un evento de riesgo detectado por la [Protección de identidad de Azure Active Directory](https://azure.microsoft.com/en-us/documentation/articles/active-directory-identityprotection/) donde un inicio de sesión de cuenta se intentó desde una dirección IP que aparece para ser anónimos.</span><span class="sxs-lookup"><span data-stu-id="de1d9-107">A risk event detected by [Azure Active Directory Identity Protection](https://azure.microsoft.com/en-us/documentation/articles/active-directory-identityprotection/) where an account sign-in is attempted from an IP address that appears to be anonymous.</span></span> <span data-ttu-id="de1d9-108">Obtener información completa acerca de los eventos de riesgo puede encontrarse en la [documentación de protección de la identidad de AD de Azure](https://azure.microsoft.com/en-us/documentation/articles/active-directory-identityprotection-risk-events-types/).</span><span class="sxs-lookup"><span data-stu-id="de1d9-108">Complete information about risk events can be found in the [Azure AD Identity Protection documentation](https://azure.microsoft.com/en-us/documentation/articles/active-directory-identityprotection-risk-events-types/).</span></span>


## <a name="methods"></a><span data-ttu-id="de1d9-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="de1d9-109">Methods</span></span>

| <span data-ttu-id="de1d9-110">Método</span><span class="sxs-lookup"><span data-stu-id="de1d9-110">Method</span></span>           | <span data-ttu-id="de1d9-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="de1d9-111">Return Type</span></span>    |<span data-ttu-id="de1d9-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="de1d9-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="de1d9-113">Obtener anonymousIpRiskEvent</span><span class="sxs-lookup"><span data-stu-id="de1d9-113">Get anonymousIpRiskEvent</span></span>](../api/anonymousipriskevent-get.md) | [<span data-ttu-id="de1d9-114">anonymousIpRiskEvent</span><span class="sxs-lookup"><span data-stu-id="de1d9-114">anonymousIpRiskEvent</span></span>](anonymousipriskevent.md) |<span data-ttu-id="de1d9-115">Leer las propiedades y las relaciones del objeto anonymousIpRiskEvent.</span><span class="sxs-lookup"><span data-stu-id="de1d9-115">Read properties and relationships of anonymousIpRiskEvent object.</span></span>|

## <a name="properties"></a><span data-ttu-id="de1d9-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="de1d9-116">Properties</span></span>
| <span data-ttu-id="de1d9-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="de1d9-117">Property</span></span>     | <span data-ttu-id="de1d9-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="de1d9-118">Type</span></span>   |<span data-ttu-id="de1d9-119">Description</span><span class="sxs-lookup"><span data-stu-id="de1d9-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="de1d9-120">closedDateTime</span><span class="sxs-lookup"><span data-stu-id="de1d9-120">closedDateTime</span></span>|<span data-ttu-id="de1d9-121">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="de1d9-121">dateTimeOffset</span></span>| <span data-ttu-id="de1d9-122">La fecha y hora en que se ha cerrado el evento de riesgo</span><span class="sxs-lookup"><span data-stu-id="de1d9-122">The date and time that the risk event was closed</span></span>|
|<span data-ttu-id="de1d9-123">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="de1d9-123">createdDateTime</span></span>|<span data-ttu-id="de1d9-124">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="de1d9-124">dateTimeOffset</span></span>| <span data-ttu-id="de1d9-125">La fecha y hora en que se creó el evento de riesgo.</span><span class="sxs-lookup"><span data-stu-id="de1d9-125">The date and time that the risk event was created.</span></span> <span data-ttu-id="de1d9-126">Siempre es mayor o igual que la fecha y hora del evento riesgo propio.</span><span class="sxs-lookup"><span data-stu-id="de1d9-126">This is always greater than or equal to the datetime of the risk event itself.</span></span> <span data-ttu-id="de1d9-127">Ésta es la propiedad correcta para utilizar como filtro al consultar los eventos de riesgo.</span><span class="sxs-lookup"><span data-stu-id="de1d9-127">This is the correct property to use as a filter when querying risk events.</span></span>|
|<span data-ttu-id="de1d9-128">id</span><span class="sxs-lookup"><span data-stu-id="de1d9-128">id</span></span>|<span data-ttu-id="de1d9-129">string</span><span class="sxs-lookup"><span data-stu-id="de1d9-129">string</span></span>| <span data-ttu-id="de1d9-130">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="de1d9-130">Read-only</span></span>|
|<span data-ttu-id="de1d9-131">ipAddress</span><span class="sxs-lookup"><span data-stu-id="de1d9-131">ipAddress</span></span>|<span data-ttu-id="de1d9-132">string</span><span class="sxs-lookup"><span data-stu-id="de1d9-132">string</span></span>| <span data-ttu-id="de1d9-133">La dirección IP de inicio de sesión de</span><span class="sxs-lookup"><span data-stu-id="de1d9-133">The IP address of the sign-in</span></span>|
|<span data-ttu-id="de1d9-134">location</span><span class="sxs-lookup"><span data-stu-id="de1d9-134">location</span></span>|<span data-ttu-id="de1d9-135">string</span><span class="sxs-lookup"><span data-stu-id="de1d9-135">string</span></span>| <span data-ttu-id="de1d9-136">La ubicación que se adjunta a la dirección IP de inicio de sesión de</span><span class="sxs-lookup"><span data-stu-id="de1d9-136">The location attached to the IP address of the sign-in</span></span>|
|<span data-ttu-id="de1d9-137">riskEventDateTime</span><span class="sxs-lookup"><span data-stu-id="de1d9-137">riskEventDateTime</span></span>|<span data-ttu-id="de1d9-138">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="de1d9-138">dateTimeOffset</span></span>| <span data-ttu-id="de1d9-139">Fecha y hora en que se produjo el evento de riesgo</span><span class="sxs-lookup"><span data-stu-id="de1d9-139">The date and time when the risk event occurred</span></span>|
|<span data-ttu-id="de1d9-140">riskEventStatus</span><span class="sxs-lookup"><span data-stu-id="de1d9-140">riskEventStatus</span></span>|<span data-ttu-id="de1d9-141">string</span><span class="sxs-lookup"><span data-stu-id="de1d9-141">string</span></span>| <span data-ttu-id="de1d9-142">Los valores posibles son: `active`, `remediated`, `dismissedAsFixed`, `dismissedAsFalsePositive`, `dismissedAsIgnore`, `loginBlocked`, `closedMfaAuto` y `closedMultipleReasons`.</span><span class="sxs-lookup"><span data-stu-id="de1d9-142">Possible values are: `active`, `remediated`, `dismissedAsFixed`, `dismissedAsFalsePositive`, `dismissedAsIgnore`, `loginBlocked`, `closedMfaAuto`, `closedMultipleReasons`.</span></span>|
|<span data-ttu-id="de1d9-143">riskLevel</span><span class="sxs-lookup"><span data-stu-id="de1d9-143">riskLevel</span></span>|<span data-ttu-id="de1d9-144">string</span><span class="sxs-lookup"><span data-stu-id="de1d9-144">string</span></span>| <span data-ttu-id="de1d9-145">Los valores posibles son: `low`, `medium` y `high`.</span><span class="sxs-lookup"><span data-stu-id="de1d9-145">Possible values are: `low`, `medium`, `high`.</span></span>|
|<span data-ttu-id="de1d9-146">riskEventType</span><span class="sxs-lookup"><span data-stu-id="de1d9-146">riskEventType</span></span>|<span data-ttu-id="de1d9-147">string</span><span class="sxs-lookup"><span data-stu-id="de1d9-147">string</span></span>| <span data-ttu-id="de1d9-148">El tipo de riesgo</span><span class="sxs-lookup"><span data-stu-id="de1d9-148">The type of risk</span></span>|
|<span data-ttu-id="de1d9-149">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="de1d9-149">userDisplayName</span></span>|<span data-ttu-id="de1d9-150">string</span><span class="sxs-lookup"><span data-stu-id="de1d9-150">string</span></span>| <span data-ttu-id="de1d9-151">El nombre del usuario en riesgo</span><span class="sxs-lookup"><span data-stu-id="de1d9-151">The name of the user at risk</span></span>|
|<span data-ttu-id="de1d9-152">userId</span><span class="sxs-lookup"><span data-stu-id="de1d9-152">userId</span></span>|<span data-ttu-id="de1d9-153">string</span><span class="sxs-lookup"><span data-stu-id="de1d9-153">string</span></span>| <span data-ttu-id="de1d9-154">El identificador del usuario en riesgo</span><span class="sxs-lookup"><span data-stu-id="de1d9-154">The id of the user at risk</span></span>|
|<span data-ttu-id="de1d9-155">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="de1d9-155">userPrincipalName</span></span>|<span data-ttu-id="de1d9-156">string</span><span class="sxs-lookup"><span data-stu-id="de1d9-156">string</span></span>| <span data-ttu-id="de1d9-157">El nombre principal de usuario del usuario en riesgo</span><span class="sxs-lookup"><span data-stu-id="de1d9-157">The user principal name of the user at risk</span></span>|

## <a name="relationships"></a><span data-ttu-id="de1d9-158">Relaciones</span><span class="sxs-lookup"><span data-stu-id="de1d9-158">Relationships</span></span>
| <span data-ttu-id="de1d9-159">Relación</span><span class="sxs-lookup"><span data-stu-id="de1d9-159">Relationship</span></span> | <span data-ttu-id="de1d9-160">Tipo</span><span class="sxs-lookup"><span data-stu-id="de1d9-160">Type</span></span>   |<span data-ttu-id="de1d9-161">Description</span><span class="sxs-lookup"><span data-stu-id="de1d9-161">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="de1d9-162">impactedUser</span><span class="sxs-lookup"><span data-stu-id="de1d9-162">impactedUser</span></span>|[<span data-ttu-id="de1d9-163">user</span><span class="sxs-lookup"><span data-stu-id="de1d9-163">user</span></span>](user.md)| <span data-ttu-id="de1d9-p105">Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="de1d9-p105">Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="de1d9-166">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="de1d9-166">JSON representation</span></span>

<span data-ttu-id="de1d9-167">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="de1d9-167">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.anonymousIpRiskEvent"
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
  "description": "anonymousIpRiskEvent resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
