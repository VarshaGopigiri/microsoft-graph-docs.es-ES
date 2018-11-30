---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: IdentitySet
ms.openlocfilehash: ea49f904197b2f4a661b781576f06240e41cf808
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032152"
---
# <a name="identityset-resource-type"></a><span data-ttu-id="aa749-102">Tipo de recurso IdentitySet</span><span class="sxs-lookup"><span data-stu-id="aa749-102">IdentitySet resource type</span></span>

<span data-ttu-id="aa749-p101">El recurso **IdentitySet** es una colección de claves de recursos [identity](identity.md). Se usa para representar un conjunto de identidades asociadas a diversos eventos para un elemento, como _creado por_ o _última modificación_.</span><span class="sxs-lookup"><span data-stu-id="aa749-p101">The **IdentitySet** resource is a keyed collection of [identity](identity.md) resources. It is used to represent a set of identities associated with various events for an item, such as _created by_ or _last modified by_.</span></span>

## <a name="json-representation"></a><span data-ttu-id="aa749-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="aa749-105">JSON representation</span></span>

<span data-ttu-id="aa749-106">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="aa749-106">Here is a JSON representation of the resource.</span></span>

<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.identitySet",
       "optionalProperties": ["user", "application", "device"],
       "openType": true } -->
```json
{
  "application": {"@odata.type": "microsoft.graph.identity"},
  "device": {"@odata.type": "microsoft.graph.identity"},
  "user": {"@odata.type": "microsoft.graph.identity"}
}
```

## <a name="properties"></a><span data-ttu-id="aa749-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aa749-107">Properties</span></span>

| <span data-ttu-id="aa749-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="aa749-108">Property</span></span>    | <span data-ttu-id="aa749-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="aa749-109">Type</span></span>                    | <span data-ttu-id="aa749-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa749-110">Description</span></span>                                            |
|:------------|:------------------------|:-------------------------------------------------------|
| <span data-ttu-id="aa749-111">application</span><span class="sxs-lookup"><span data-stu-id="aa749-111">application</span></span> | [<span data-ttu-id="aa749-112">Identity</span><span class="sxs-lookup"><span data-stu-id="aa749-112">Identity</span></span>](identity.md) | <span data-ttu-id="aa749-p102">Opcional. Aplicación asociada a esta acción.</span><span class="sxs-lookup"><span data-stu-id="aa749-p102">Optional. The application associated with this action.</span></span> |
| <span data-ttu-id="aa749-115">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="aa749-115">device</span></span>      | [<span data-ttu-id="aa749-116">Identity</span><span class="sxs-lookup"><span data-stu-id="aa749-116">Identity</span></span>](identity.md) | <span data-ttu-id="aa749-p103">Opcional. Dispositivo asociado a esta acción.</span><span class="sxs-lookup"><span data-stu-id="aa749-p103">Optional. The device associated with this action.</span></span>      |
| <span data-ttu-id="aa749-119">usuario</span><span class="sxs-lookup"><span data-stu-id="aa749-119">user</span></span>        | [<span data-ttu-id="aa749-120">Identity</span><span class="sxs-lookup"><span data-stu-id="aa749-120">Identity</span></span>](identity.md) | <span data-ttu-id="aa749-p104">Opcional. Usuario asociado a esta acción.</span><span class="sxs-lookup"><span data-stu-id="aa749-p104">Optional. The user associated with this action.</span></span>        |

## <a name="remarks"></a><span data-ttu-id="aa749-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aa749-123">Remarks</span></span> 

<span data-ttu-id="aa749-124">Consulte [DriveItem](driveitem.md) para obtener información sobre el uso de recursos **IdentitySet**.</span><span class="sxs-lookup"><span data-stu-id="aa749-124">See [DriveItem](driveitem.md) for usage of **IdentitySet** resources.</span></span>


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Identity set is a collection of identities",
  "section": "documentation",
  "tocPath": "Resources/IdentitySet"
} -->
