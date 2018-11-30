---
title: Tipo de recurso verifiedDomain
description: Especifica un dominio para un inquilino. La propiedad **verifiedDomains** de la entidad organization es una colección de **VerifiedDomain**.
ms.openlocfilehash: 810b5fea0fbaf82eeb452c0f5c6032679590ff49
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088433"
---
# <a name="verifieddomain-resource-type"></a><span data-ttu-id="905ba-104">Tipo de recurso verifiedDomain</span><span class="sxs-lookup"><span data-stu-id="905ba-104">verifiedDomain resource type</span></span>

> <span data-ttu-id="905ba-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="905ba-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="905ba-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="905ba-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="905ba-p103">Especifica un dominio para un inquilino. La propiedad **verifiedDomains** de la entidad [organization](organization.md) es una colección de **VerifiedDomain**.</span><span class="sxs-lookup"><span data-stu-id="905ba-p103">Specifies a domain for a tenant. The **verifiedDomains** property of the [organization](organization.md) entity is a collection of **VerifiedDomain**.</span></span>


## <a name="properties"></a><span data-ttu-id="905ba-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="905ba-109">Properties</span></span>
| <span data-ttu-id="905ba-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="905ba-110">Property</span></span>     | <span data-ttu-id="905ba-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="905ba-111">Type</span></span>   |<span data-ttu-id="905ba-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="905ba-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="905ba-113">capabilities</span><span class="sxs-lookup"><span data-stu-id="905ba-113">capabilities</span></span>|<span data-ttu-id="905ba-114">String</span><span class="sxs-lookup"><span data-stu-id="905ba-114">String</span></span>|<span data-ttu-id="905ba-115">Por ejemplo, "Email", "OfficeCommunicationsOnline".</span><span class="sxs-lookup"><span data-stu-id="905ba-115">For example, “Email”, “OfficeCommunicationsOnline”.</span></span>|
|<span data-ttu-id="905ba-116">isDefault</span><span class="sxs-lookup"><span data-stu-id="905ba-116">isDefault</span></span>|<span data-ttu-id="905ba-117">Boolean</span><span class="sxs-lookup"><span data-stu-id="905ba-117">Boolean</span></span>|                <span data-ttu-id="905ba-118">**true** si se trata del dominio predeterminado asociado al inquilino; de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="905ba-118">**true** if this is the default domain associated with the tenant; otherwise, **false**.</span></span>            |
|<span data-ttu-id="905ba-119">isInitial</span><span class="sxs-lookup"><span data-stu-id="905ba-119">isInitial</span></span>|<span data-ttu-id="905ba-120">Boolean</span><span class="sxs-lookup"><span data-stu-id="905ba-120">Boolean</span></span>|<span data-ttu-id="905ba-121">**true** si se trata del dominio inicial asociado al inquilino; de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="905ba-121">**true** if this is the initial domain associated with the tenant; otherwise, **false**</span></span>|
|<span data-ttu-id="905ba-122">name</span><span class="sxs-lookup"><span data-stu-id="905ba-122">name</span></span>|<span data-ttu-id="905ba-123">String</span><span class="sxs-lookup"><span data-stu-id="905ba-123">String</span></span>|<span data-ttu-id="905ba-124">Nombre del dominio; por ejemplo, "contoso.onmicrosoft.com".</span><span class="sxs-lookup"><span data-stu-id="905ba-124">The domain name; for example, “contoso.onmicrosoft.com”</span></span>|
|<span data-ttu-id="905ba-125">type</span><span class="sxs-lookup"><span data-stu-id="905ba-125">type</span></span>|<span data-ttu-id="905ba-126">String</span><span class="sxs-lookup"><span data-stu-id="905ba-126">String</span></span>|<span data-ttu-id="905ba-127">Por ejemplo, "Administrado".</span><span class="sxs-lookup"><span data-stu-id="905ba-127">For example, “Managed”.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="905ba-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="905ba-128">JSON representation</span></span>

<span data-ttu-id="905ba-129">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="905ba-129">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.verifieddomain"
}-->

```json
{
  "capabilities": "string",
  "isDefault": true,
  "isInitial": true,
  "name": "string",
  "type": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "verifiedDomain resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
