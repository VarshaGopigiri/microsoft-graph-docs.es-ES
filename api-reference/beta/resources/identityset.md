---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: IdentitySet
ms.openlocfilehash: 71620da04ea9d7f67d69422ce175182d406d44f5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086245"
---
# <a name="identityset-resource-type"></a><span data-ttu-id="dcbfa-102">tipo de recurso identitySet</span><span class="sxs-lookup"><span data-stu-id="dcbfa-102">identitySet resource type</span></span>

<span data-ttu-id="dcbfa-p101">El recurso **IdentitySet** es una colección de claves de recursos [identity](identity.md). Se usa para representar un conjunto de identidades asociadas a diversos eventos para un elemento, como _creado por_ o _última modificación_.</span><span class="sxs-lookup"><span data-stu-id="dcbfa-p101">The **IdentitySet** resource is a keyed collection of [identity](identity.md) resources. It is used to represent a set of identities associated with various events for an item, such as _created by_ or _last modified by_.</span></span>

## <a name="json-representation"></a><span data-ttu-id="dcbfa-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="dcbfa-105">JSON representation</span></span>

<span data-ttu-id="dcbfa-106">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="dcbfa-106">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.identitySet",
  "optionalProperties": [
    "application",
    "applicationInstance",
    "device",
    "encrypted",
    "guest",
    "phone",
    "user"
  ],
  "openType": true
} -->
```json
{
  "application": {"@odata.type": "#microsoft.graph.identity"},
  "applicationInstance": {"@odata.type": "#microsoft.graph.identity"},
  "device": {"@odata.type": "#microsoft.graph.identity"},
  "encrypted": {"@odata.type": "#microsoft.graph.identity"},
  "guest": {"@odata.type": "#microsoft.graph.identity"},
  "phone": {"@odata.type": "#microsoft.graph.identity"},
  "user": {"@odata.type": "#microsoft.graph.identity"}
}
```

## <a name="properties"></a><span data-ttu-id="dcbfa-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dcbfa-107">Properties</span></span>

| <span data-ttu-id="dcbfa-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dcbfa-108">Property</span></span>    | <span data-ttu-id="dcbfa-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="dcbfa-109">Type</span></span>                    | <span data-ttu-id="dcbfa-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="dcbfa-110">Description</span></span>                                             |
|:------------|:------------------------|:--------------------------------------------------------|
| <span data-ttu-id="dcbfa-111">application</span><span class="sxs-lookup"><span data-stu-id="dcbfa-111">application</span></span> | [<span data-ttu-id="dcbfa-112">Identity</span><span class="sxs-lookup"><span data-stu-id="dcbfa-112">Identity</span></span>](identity.md) | <span data-ttu-id="dcbfa-p102">Opcional. Aplicación asociada a esta acción.</span><span class="sxs-lookup"><span data-stu-id="dcbfa-p102">Optional. The application associated with this action.</span></span>  |
| <span data-ttu-id="dcbfa-115">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="dcbfa-115">device</span></span>      | [<span data-ttu-id="dcbfa-116">Identity</span><span class="sxs-lookup"><span data-stu-id="dcbfa-116">Identity</span></span>](identity.md) | <span data-ttu-id="dcbfa-p103">Opcional. Dispositivo asociado a esta acción.</span><span class="sxs-lookup"><span data-stu-id="dcbfa-p103">Optional. The device associated with this action.</span></span>       |
| <span data-ttu-id="dcbfa-119">phone</span><span class="sxs-lookup"><span data-stu-id="dcbfa-119">phone</span></span>       | [<span data-ttu-id="dcbfa-120">identity</span><span class="sxs-lookup"><span data-stu-id="dcbfa-120">identity</span></span>](identity.md) | <span data-ttu-id="dcbfa-121">Opcional.</span><span class="sxs-lookup"><span data-stu-id="dcbfa-121">Optional.</span></span> <span data-ttu-id="dcbfa-122">El número de teléfono asociado con esta acción.</span><span class="sxs-lookup"><span data-stu-id="dcbfa-122">The phone number associated with this action.</span></span> |
| <span data-ttu-id="dcbfa-123">usuario</span><span class="sxs-lookup"><span data-stu-id="dcbfa-123">user</span></span>        | [<span data-ttu-id="dcbfa-124">Identity</span><span class="sxs-lookup"><span data-stu-id="dcbfa-124">Identity</span></span>](identity.md) | <span data-ttu-id="dcbfa-p105">Opcional. Usuario asociado a esta acción.</span><span class="sxs-lookup"><span data-stu-id="dcbfa-p105">Optional. The user associated with this action.</span></span>         |

## <a name="remarks"></a><span data-ttu-id="dcbfa-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dcbfa-127">Remarks</span></span> 

<span data-ttu-id="dcbfa-128">Vea la [llamada](call.md) para el uso de recursos de **IdentitySet** .</span><span class="sxs-lookup"><span data-stu-id="dcbfa-128">See [Call](call.md) for usage of **IdentitySet** resources.</span></span>


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Identity set is a collection of identities",
  "section": "documentation",
  "tocPath": "Resources/IdentitySet"
} -->