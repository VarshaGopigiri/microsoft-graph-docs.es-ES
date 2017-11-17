---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: IdentitySet
ms.openlocfilehash: 4d2bb5d92ebe06e79a68d69b949baec19a33a4c6
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="identityset-resource-type"></a><span data-ttu-id="40a6e-102">Tipo de recurso IdentitySet</span><span class="sxs-lookup"><span data-stu-id="40a6e-102">IdentitySet resource type</span></span>

<span data-ttu-id="40a6e-p101">El recurso **IdentitySet** es una colección de claves de recursos [identity](identity.md). Se usa para representar un conjunto de identidades asociadas a diversos eventos para un elemento, como _creado por_ o _última modificación_.</span><span class="sxs-lookup"><span data-stu-id="40a6e-p101">The **IdentitySet** resource is a keyed collection of [identity](identity.md) resources. It is used to represent a set of identities associated with various events for an item, such as _created by_ or _last modified by_.</span></span>

## <a name="json-representation"></a><span data-ttu-id="40a6e-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="40a6e-105">JSON representation</span></span>

<span data-ttu-id="40a6e-106">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="40a6e-106">Here is a JSON representation of the resource.</span></span>

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

## <a name="properties"></a><span data-ttu-id="40a6e-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="40a6e-107">Properties</span></span>

| <span data-ttu-id="40a6e-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="40a6e-108">Property</span></span>    | <span data-ttu-id="40a6e-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="40a6e-109">Type</span></span>                    | <span data-ttu-id="40a6e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="40a6e-110">Description</span></span>                                            |
|:------------|:------------------------|:-------------------------------------------------------|
| <span data-ttu-id="40a6e-111">application</span><span class="sxs-lookup"><span data-stu-id="40a6e-111">application</span></span> | [<span data-ttu-id="40a6e-112">Identity</span><span class="sxs-lookup"><span data-stu-id="40a6e-112">Identity</span></span>](identity.md) | <span data-ttu-id="40a6e-p102">Opcional. Aplicación asociada a esta acción.</span><span class="sxs-lookup"><span data-stu-id="40a6e-p102">Optional. The application associated with this action.</span></span> |
| <span data-ttu-id="40a6e-115">device</span><span class="sxs-lookup"><span data-stu-id="40a6e-115">device</span></span>      | [<span data-ttu-id="40a6e-116">Identity</span><span class="sxs-lookup"><span data-stu-id="40a6e-116">Identity</span></span>](identity.md) | <span data-ttu-id="40a6e-p103">Opcional. Dispositivo asociado a esta acción.</span><span class="sxs-lookup"><span data-stu-id="40a6e-p103">Optional. The device associated with this action.</span></span>      |
| <span data-ttu-id="40a6e-119">user</span><span class="sxs-lookup"><span data-stu-id="40a6e-119">user</span></span>        | [<span data-ttu-id="40a6e-120">Identity</span><span class="sxs-lookup"><span data-stu-id="40a6e-120">Identity</span></span>](identity.md) | <span data-ttu-id="40a6e-p104">Opcional. Usuario asociado a esta acción.</span><span class="sxs-lookup"><span data-stu-id="40a6e-p104">Optional. The user associated with this action.</span></span>        |

## <a name="remarks"></a><span data-ttu-id="40a6e-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="40a6e-123">Remarks</span></span> 

<span data-ttu-id="40a6e-124">Consulte [DriveItem](driveitem.md) para obtener información sobre el uso de recursos **IdentitySet**.</span><span class="sxs-lookup"><span data-stu-id="40a6e-124">See [DriveItem](driveitem.md) for usage of **IdentitySet** resources.</span></span>


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Identity set is a collection of identities",
  "section": "documentation",
  "tocPath": "Resources/IdentitySet"
} -->
