---
title: Tipo de recurso verifiedDomain
description: Especifica un dominio para un inquilino. La propiedad **verifiedDomains** de la entidad organization es una colección de **VerifiedDomain**.
localization_priority: Normal
ms.openlocfilehash: 6eb6490ce8dac29f2617b7873230fad7c7b5c536
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27876499"
---
# <a name="verifieddomain-resource-type"></a><span data-ttu-id="6cf91-104">Tipo de recurso verifiedDomain</span><span class="sxs-lookup"><span data-stu-id="6cf91-104">verifiedDomain resource type</span></span>

<span data-ttu-id="6cf91-p102">Especifica un dominio para un inquilino. La propiedad **verifiedDomains** de la entidad [organization](organization.md) es una colección de **VerifiedDomain**.</span><span class="sxs-lookup"><span data-stu-id="6cf91-p102">Specifies a domain for a tenant. The **verifiedDomains** property of the [organization](organization.md) entity is a collection of **VerifiedDomain**.</span></span>


## <a name="properties"></a><span data-ttu-id="6cf91-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6cf91-107">Properties</span></span>
| <span data-ttu-id="6cf91-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6cf91-108">Property</span></span>     | <span data-ttu-id="6cf91-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="6cf91-109">Type</span></span>   |<span data-ttu-id="6cf91-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6cf91-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6cf91-111">capabilities</span><span class="sxs-lookup"><span data-stu-id="6cf91-111">capabilities</span></span>|<span data-ttu-id="6cf91-112">String</span><span class="sxs-lookup"><span data-stu-id="6cf91-112">String</span></span>|<span data-ttu-id="6cf91-113">Por ejemplo, "Email", "OfficeCommunicationsOnline".</span><span class="sxs-lookup"><span data-stu-id="6cf91-113">For example, “Email”, “OfficeCommunicationsOnline”.</span></span>|
|<span data-ttu-id="6cf91-114">isDefault</span><span class="sxs-lookup"><span data-stu-id="6cf91-114">isDefault</span></span>|<span data-ttu-id="6cf91-115">Boolean</span><span class="sxs-lookup"><span data-stu-id="6cf91-115">Boolean</span></span>|                <span data-ttu-id="6cf91-116">**true** si se trata del dominio predeterminado asociado al inquilino; de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="6cf91-116">**true** if this is the default domain associated with the tenant; otherwise, **false**.</span></span>            |
|<span data-ttu-id="6cf91-117">isInitial</span><span class="sxs-lookup"><span data-stu-id="6cf91-117">isInitial</span></span>|<span data-ttu-id="6cf91-118">Boolean</span><span class="sxs-lookup"><span data-stu-id="6cf91-118">Boolean</span></span>|<span data-ttu-id="6cf91-119">**true** si se trata del dominio inicial asociado al inquilino; de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="6cf91-119">**true** if this is the initial domain associated with the tenant; otherwise, **false**</span></span>|
|<span data-ttu-id="6cf91-120">name</span><span class="sxs-lookup"><span data-stu-id="6cf91-120">name</span></span>|<span data-ttu-id="6cf91-121">String</span><span class="sxs-lookup"><span data-stu-id="6cf91-121">String</span></span>|<span data-ttu-id="6cf91-122">Nombre del dominio; por ejemplo, "contoso.onmicrosoft.com".</span><span class="sxs-lookup"><span data-stu-id="6cf91-122">The domain name; for example, “contoso.onmicrosoft.com”</span></span>|
|<span data-ttu-id="6cf91-123">type</span><span class="sxs-lookup"><span data-stu-id="6cf91-123">type</span></span>|<span data-ttu-id="6cf91-124">String</span><span class="sxs-lookup"><span data-stu-id="6cf91-124">String</span></span>|<span data-ttu-id="6cf91-125">Por ejemplo, "Administrado".</span><span class="sxs-lookup"><span data-stu-id="6cf91-125">For example, “Managed”.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="6cf91-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6cf91-126">JSON representation</span></span>

<span data-ttu-id="6cf91-127">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="6cf91-127">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.verifiedDomain"
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
