---
title: tipo de recurso synchronizationSecretKeyStringValuePair
description: 'Representa un único valor secreto. '
localization_priority: Normal
ms.openlocfilehash: 55cbd6b19ddf6c6f622ad7daddea569558e31f0d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27818735"
---
# <a name="synchronizationsecretkeystringvaluepair-resource-type"></a><span data-ttu-id="f6125-103">tipo de recurso synchronizationSecretKeyStringValuePair</span><span class="sxs-lookup"><span data-stu-id="f6125-103">synchronizationSecretKeyStringValuePair resource type</span></span>

> <span data-ttu-id="f6125-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f6125-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f6125-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f6125-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f6125-106">Representa un único valor secreto.</span><span class="sxs-lookup"><span data-stu-id="f6125-106">Represents a single secret value.</span></span> 

## <a name="properties"></a><span data-ttu-id="f6125-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f6125-107">Properties</span></span>
| <span data-ttu-id="f6125-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f6125-108">Property</span></span>     | <span data-ttu-id="f6125-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="f6125-109">Type</span></span>   |<span data-ttu-id="f6125-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6125-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f6125-111">Key</span><span class="sxs-lookup"><span data-stu-id="f6125-111">key</span></span>|<span data-ttu-id="f6125-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="f6125-112">String</span></span>| <span data-ttu-id="f6125-113">Los valores posibles son: `None`, `UserName`, `Password`, `SecretToken`, `AppKey`, `BaseAddress`, `ClientIdentifier`, `ClientSecret`, `SingleSignOnType`, `Sandbox`, `Url`, `Domain`, `ConsumerKey`, `ConsumerSecret`, `TokenKey`, `TokenExpiration`, `Oauth2AccessToken`, `Oauth2AccessTokenCreationTime`, `Oauth2RefreshToken` , `SyncAll`, `InstanceName`, `Oauth2ClientId`, `Oauth2ClientSecret`, `CompanyId`, `UpdateKeyOnSoftDelete`, `SynchronizationSchedule`, `SystemOfRecord`, `SandboxName`, `EnforceDomain`, `SyncNotificationSettings`, `Server`, `PerformInboundEntitlementGrants`, `HardDeletesEnabled`, `SyncAgentCompatibilityKey`, `SyncAgentADContainer`, `ValidateDomain`, `TestReferences`.</span><span class="sxs-lookup"><span data-stu-id="f6125-113">Possible values are: `None`, `UserName`, `Password`, `SecretToken`, `AppKey`, `BaseAddress`, `ClientIdentifier`, `ClientSecret`, `SingleSignOnType`, `Sandbox`, `Url`, `Domain`, `ConsumerKey`, `ConsumerSecret`, `TokenKey`, `TokenExpiration`, `Oauth2AccessToken`, `Oauth2AccessTokenCreationTime`, `Oauth2RefreshToken`, `SyncAll`, `InstanceName`, `Oauth2ClientId`, `Oauth2ClientSecret`, `CompanyId`, `UpdateKeyOnSoftDelete`, `SynchronizationSchedule`, `SystemOfRecord`, `SandboxName`, `EnforceDomain`, `SyncNotificationSettings`, `Server`, `PerformInboundEntitlementGrants`, `HardDeletesEnabled`, `SyncAgentCompatibilityKey`, `SyncAgentADContainer`, `ValidateDomain`, `TestReferences`.</span></span>|
|<span data-ttu-id="f6125-114">valor</span><span class="sxs-lookup"><span data-stu-id="f6125-114">value</span></span>|<span data-ttu-id="f6125-115">String</span><span class="sxs-lookup"><span data-stu-id="f6125-115">String</span></span>|<span data-ttu-id="f6125-116">El valor del secreto.</span><span class="sxs-lookup"><span data-stu-id="f6125-116">The value of the secret.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="f6125-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f6125-117">JSON representation</span></span>

<span data-ttu-id="f6125-118">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="f6125-118">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.synchronizationSecretKeyStringValuePair"
}-->

```json
{
  "key": "String",
  "value": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "synchronizationSecretKeyStringValuePair resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
