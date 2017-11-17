---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: SharingInvitation
ms.openlocfilehash: 75fa8212f77873b86748f6d8f63c8e62c8d6a0ca
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="sharinginvitation-resource-type"></a><span data-ttu-id="25c12-102">Tipo de recurso SharingInvitation</span><span class="sxs-lookup"><span data-stu-id="25c12-102">SharingInvitation resource type</span></span>

<span data-ttu-id="25c12-103">El recurso **SharingInvitation** agrupa en una sola estructura los elementos de datos relacionados con invitaciones.</span><span class="sxs-lookup"><span data-stu-id="25c12-103">The **SharingInvitation** resource groups invitation-related data items into a single strucutre.</span></span>

## <a name="json-representation"></a><span data-ttu-id="25c12-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="25c12-104">JSON representation</span></span>

<span data-ttu-id="25c12-105">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="25c12-105">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.sharingInvitation"
}-->

```json
{
  "email": "string",
  "invitedBy": {"@odata.type": "microsoft.graph.identitySet" },
  "signInRequired": true
}
```

## <a name="properties"></a><span data-ttu-id="25c12-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="25c12-106">Properties</span></span>

| <span data-ttu-id="25c12-107">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="25c12-107">Property Name</span></span>  | <span data-ttu-id="25c12-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="25c12-108">Type</span></span>                          | <span data-ttu-id="25c12-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="25c12-109">Description</span></span>                                                                                                                   |
|:---------------|:------------------------------|:------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25c12-110">email</span><span class="sxs-lookup"><span data-stu-id="25c12-110">email</span></span>          | <span data-ttu-id="25c12-111">String</span><span class="sxs-lookup"><span data-stu-id="25c12-111">String</span></span>                        | <span data-ttu-id="25c12-p101">Dirección de correo proporcionada para el destinatario de la invitación para compartir. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="25c12-p101">The email address provided for the recipient of the sharing invitation. Read-only.</span></span>                                          |
| <span data-ttu-id="25c12-114">invitedBy</span><span class="sxs-lookup"><span data-stu-id="25c12-114">invitedBy</span></span>      | [<span data-ttu-id="25c12-115">identitySet</span><span class="sxs-lookup"><span data-stu-id="25c12-115">identitySet</span></span>](identityset.md) | <span data-ttu-id="25c12-p102">Proporciona información sobre quién envió la invitación que creó este permiso, si esa información está disponible. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="25c12-p102">Provides information about who sent the invitation that created this permission, if that information is available. Read-only.</span></span> |
| <span data-ttu-id="25c12-118">signInRequired</span><span class="sxs-lookup"><span data-stu-id="25c12-118">signInRequired</span></span> | <span data-ttu-id="25c12-119">Boolean</span><span class="sxs-lookup"><span data-stu-id="25c12-119">Boolean</span></span>                       | <span data-ttu-id="25c12-p103">Si `true` el destinatario de la invitación necesita iniciar sesión para obtener acceso al elemento compartido. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="25c12-p103">If `true` the recipient of the invitation needs to sign in in order to access the shared item. Read-only.</span></span>                     |

## <a name="remarks"></a><span data-ttu-id="25c12-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="25c12-122">Remarks</span></span> 

<span data-ttu-id="25c12-123">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="25c12-123">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>


<!-- {
  "type": "#page.annotation",
  "description": "The sharing invitation facet describes details of a sharing invitation associated with a permission.",
  "keywords": "image,width,height,item,facet",
  "section": "documentation",
  "tocPath": "Facets/SharingInvitation"
} -->
