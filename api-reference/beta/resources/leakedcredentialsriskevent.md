---
title: tipo de recurso leakedCredentialsRiskEvent
description: Un evento de riesgo detectado por Azure Active Directory identidad protección donde se han detectado credenciales de la cuenta en la naturaleza. Obtener información completa acerca de los eventos de riesgo puede encontrarse en la documentación de protección de la identidad de AD de Azure.
localization_priority: Normal
ms.openlocfilehash: 7a8f2a8cf72b713fab30887fcc4d81b8a88e71ae
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27815984"
---
# <a name="leakedcredentialsriskevent-resource-type"></a><span data-ttu-id="e0724-104">tipo de recurso leakedCredentialsRiskEvent</span><span class="sxs-lookup"><span data-stu-id="e0724-104">leakedCredentialsRiskEvent resource type</span></span>

> <span data-ttu-id="e0724-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e0724-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e0724-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e0724-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e0724-107">Un evento de riesgo detectado por la [Protección de identidad de Azure Active Directory](https://azure.microsoft.com/en-us/documentation/articles/active-directory-identityprotection/) donde se han detectado credenciales de la cuenta en la naturaleza.</span><span class="sxs-lookup"><span data-stu-id="e0724-107">A risk event detected by [Azure Active Directory Identity Protection](https://azure.microsoft.com/en-us/documentation/articles/active-directory-identityprotection/) where an account's credentials have been detected in the wild.</span></span> <span data-ttu-id="e0724-108">Obtener información completa acerca de los eventos de riesgo puede encontrarse en la [documentación de protección de la identidad de AD de Azure](https://azure.microsoft.com/en-us/documentation/articles/active-directory-identityprotection-risk-events-types/).</span><span class="sxs-lookup"><span data-stu-id="e0724-108">Complete information about risk events can be found in the [Azure AD Identity Protection documentation](https://azure.microsoft.com/en-us/documentation/articles/active-directory-identityprotection-risk-events-types/).</span></span>


## <a name="methods"></a><span data-ttu-id="e0724-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="e0724-109">Methods</span></span>

| <span data-ttu-id="e0724-110">Método</span><span class="sxs-lookup"><span data-stu-id="e0724-110">Method</span></span>           | <span data-ttu-id="e0724-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0724-111">Return Type</span></span>    |<span data-ttu-id="e0724-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e0724-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="e0724-113">Obtener leakedCredentialsRiskEvent</span><span class="sxs-lookup"><span data-stu-id="e0724-113">Get leakedCredentialsRiskEvent</span></span>](../api/leakedcredentialsriskevent-get.md) | [<span data-ttu-id="e0724-114">leakedCredentialsRiskEvent</span><span class="sxs-lookup"><span data-stu-id="e0724-114">leakedCredentialsRiskEvent</span></span>](leakedcredentialsriskevent.md) |<span data-ttu-id="e0724-115">Leer las propiedades y las relaciones del objeto leakedCredentialsRiskEvent.</span><span class="sxs-lookup"><span data-stu-id="e0724-115">Read properties and relationships of leakedCredentialsRiskEvent object.</span></span>|

## <a name="properties"></a><span data-ttu-id="e0724-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e0724-116">Properties</span></span>
| <span data-ttu-id="e0724-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e0724-117">Property</span></span>     | <span data-ttu-id="e0724-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="e0724-118">Type</span></span>   |<span data-ttu-id="e0724-119">Description</span><span class="sxs-lookup"><span data-stu-id="e0724-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e0724-120">closedDateTime</span><span class="sxs-lookup"><span data-stu-id="e0724-120">closedDateTime</span></span>|<span data-ttu-id="e0724-121">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e0724-121">dateTimeOffset</span></span>| <span data-ttu-id="e0724-122">La fecha y hora en que se ha cerrado el evento de riesgo</span><span class="sxs-lookup"><span data-stu-id="e0724-122">The date and time that the risk event was closed</span></span>|
|<span data-ttu-id="e0724-123">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="e0724-123">createdDateTime</span></span>|<span data-ttu-id="e0724-124">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e0724-124">dateTimeOffset</span></span>| <span data-ttu-id="e0724-125">La fecha y hora en que se creó el evento de riesgo.</span><span class="sxs-lookup"><span data-stu-id="e0724-125">The date and time that the risk event was created.</span></span> <span data-ttu-id="e0724-126">Siempre es mayor o igual que la fecha y hora del evento riesgo propio.</span><span class="sxs-lookup"><span data-stu-id="e0724-126">This is always greater than or equal to the datetime of the risk event itself.</span></span> <span data-ttu-id="e0724-127">Ésta es la propiedad correcta para utilizar como filtro al consultar los eventos de riesgo.</span><span class="sxs-lookup"><span data-stu-id="e0724-127">This is the correct property to use as a filter when querying risk events.</span></span>|
|<span data-ttu-id="e0724-128">id</span><span class="sxs-lookup"><span data-stu-id="e0724-128">id</span></span>|<span data-ttu-id="e0724-129">string</span><span class="sxs-lookup"><span data-stu-id="e0724-129">string</span></span>| <span data-ttu-id="e0724-130">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="e0724-130">Read-only</span></span>|
|<span data-ttu-id="e0724-131">riskEventDateTime</span><span class="sxs-lookup"><span data-stu-id="e0724-131">riskEventDateTime</span></span>|<span data-ttu-id="e0724-132">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e0724-132">dateTimeOffset</span></span>| <span data-ttu-id="e0724-133">Fecha y hora en que se produjo el evento de riesgo</span><span class="sxs-lookup"><span data-stu-id="e0724-133">The date and time when the risk event occurred</span></span>|
|<span data-ttu-id="e0724-134">riskEventStatus</span><span class="sxs-lookup"><span data-stu-id="e0724-134">riskEventStatus</span></span>|<span data-ttu-id="e0724-135">string</span><span class="sxs-lookup"><span data-stu-id="e0724-135">string</span></span>| <span data-ttu-id="e0724-136">Los valores posibles son: `active`, `remediated`, `dismissedAsFixed`, `dismissedAsFalsePositive`, `dismissedAsIgnore`, `loginBlocked`, `closedMfaAuto` y `closedMultipleReasons`.</span><span class="sxs-lookup"><span data-stu-id="e0724-136">Possible values are: `active`, `remediated`, `dismissedAsFixed`, `dismissedAsFalsePositive`, `dismissedAsIgnore`, `loginBlocked`, `closedMfaAuto`, `closedMultipleReasons`.</span></span>|
|<span data-ttu-id="e0724-137">riskLevel</span><span class="sxs-lookup"><span data-stu-id="e0724-137">riskLevel</span></span>|<span data-ttu-id="e0724-138">string</span><span class="sxs-lookup"><span data-stu-id="e0724-138">string</span></span>| <span data-ttu-id="e0724-139">Los valores posibles son: `low`, `medium` y `high`.</span><span class="sxs-lookup"><span data-stu-id="e0724-139">Possible values are: `low`, `medium`, `high`.</span></span>|
|<span data-ttu-id="e0724-140">riskEventType</span><span class="sxs-lookup"><span data-stu-id="e0724-140">riskEventType</span></span>|<span data-ttu-id="e0724-141">string</span><span class="sxs-lookup"><span data-stu-id="e0724-141">string</span></span>| <span data-ttu-id="e0724-142">El tipo de riesgo</span><span class="sxs-lookup"><span data-stu-id="e0724-142">The type of risk</span></span>|
|<span data-ttu-id="e0724-143">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="e0724-143">userDisplayName</span></span>|<span data-ttu-id="e0724-144">string</span><span class="sxs-lookup"><span data-stu-id="e0724-144">string</span></span>| <span data-ttu-id="e0724-145">El nombre del usuario en riesgo</span><span class="sxs-lookup"><span data-stu-id="e0724-145">The name of the user at risk</span></span>|
|<span data-ttu-id="e0724-146">userId</span><span class="sxs-lookup"><span data-stu-id="e0724-146">userId</span></span>|<span data-ttu-id="e0724-147">string</span><span class="sxs-lookup"><span data-stu-id="e0724-147">string</span></span>| <span data-ttu-id="e0724-148">El identificador del usuario en riesgo</span><span class="sxs-lookup"><span data-stu-id="e0724-148">The id of the user at risk</span></span>|
|<span data-ttu-id="e0724-149">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="e0724-149">userPrincipalName</span></span>|<span data-ttu-id="e0724-150">string</span><span class="sxs-lookup"><span data-stu-id="e0724-150">string</span></span>| <span data-ttu-id="e0724-151">El nombre principal de usuario del usuario en riesgo</span><span class="sxs-lookup"><span data-stu-id="e0724-151">The user principal name of the user at risk</span></span>|

## <a name="relationships"></a><span data-ttu-id="e0724-152">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e0724-152">Relationships</span></span>
| <span data-ttu-id="e0724-153">Relación</span><span class="sxs-lookup"><span data-stu-id="e0724-153">Relationship</span></span> | <span data-ttu-id="e0724-154">Tipo</span><span class="sxs-lookup"><span data-stu-id="e0724-154">Type</span></span>   |<span data-ttu-id="e0724-155">Description</span><span class="sxs-lookup"><span data-stu-id="e0724-155">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e0724-156">impactedUser</span><span class="sxs-lookup"><span data-stu-id="e0724-156">impactedUser</span></span>|[<span data-ttu-id="e0724-157">user</span><span class="sxs-lookup"><span data-stu-id="e0724-157">user</span></span>](user.md)| <span data-ttu-id="e0724-p105">Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="e0724-p105">Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="e0724-160">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e0724-160">JSON representation</span></span>

<span data-ttu-id="e0724-161">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e0724-161">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.leakedCredentialsRiskEvent"
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
  "description": "leakedCredentialsRiskEvent resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
