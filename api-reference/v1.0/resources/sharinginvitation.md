---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: SharingInvitation
localization_priority: Normal
ms.openlocfilehash: f51f08ad174c661df14b688dc111d9447708523c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27846701"
---
# <a name="sharinginvitation-resource-type"></a><span data-ttu-id="4169d-102">Tipo de recurso SharingInvitation</span><span class="sxs-lookup"><span data-stu-id="4169d-102">SharingInvitation resource type</span></span>

<span data-ttu-id="4169d-103">El recurso **SharingInvitation** agrupa los elementos de datos relacionados con la invitación en una única estructura.</span><span class="sxs-lookup"><span data-stu-id="4169d-103">The **SharingInvitation** resource groups invitation-related data items into a single structure.</span></span>

## <a name="json-representation"></a><span data-ttu-id="4169d-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4169d-104">JSON representation</span></span>

<span data-ttu-id="4169d-105">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4169d-105">Here is a JSON representation of the resource.</span></span>

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

## <a name="properties"></a><span data-ttu-id="4169d-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4169d-106">Properties</span></span>

| <span data-ttu-id="4169d-107">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="4169d-107">Property Name</span></span>  | <span data-ttu-id="4169d-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="4169d-108">Type</span></span>            | <span data-ttu-id="4169d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="4169d-109">Description</span></span>
|:---------------|:----------------|:------------------------------------------
| <span data-ttu-id="4169d-110">email</span><span class="sxs-lookup"><span data-stu-id="4169d-110">email</span></span>          | <span data-ttu-id="4169d-111">String</span><span class="sxs-lookup"><span data-stu-id="4169d-111">String</span></span>          | <span data-ttu-id="4169d-p101">Dirección de correo proporcionada para el destinatario de la invitación para compartir. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4169d-p101">The email address provided for the recipient of the sharing invitation. Read-only.</span></span>
| <span data-ttu-id="4169d-114">invitedBy</span><span class="sxs-lookup"><span data-stu-id="4169d-114">invitedBy</span></span>      | <span data-ttu-id="4169d-115">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="4169d-115">[identitySet][]</span></span> | <span data-ttu-id="4169d-p102">Proporciona información sobre quién envió la invitación que creó este permiso, si esa información está disponible. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4169d-p102">Provides information about who sent the invitation that created this permission, if that information is available. Read-only.</span></span>
| <span data-ttu-id="4169d-118">signInRequired</span><span class="sxs-lookup"><span data-stu-id="4169d-118">signInRequired</span></span> | <span data-ttu-id="4169d-119">Boolean</span><span class="sxs-lookup"><span data-stu-id="4169d-119">Boolean</span></span>         | <span data-ttu-id="4169d-p103">Si `true` el destinatario de la invitación necesita iniciar sesión para obtener acceso al elemento compartido. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4169d-p103">If `true` the recipient of the invitation needs to sign in in order to access the shared item. Read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="4169d-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4169d-122">Remarks</span></span>

<span data-ttu-id="4169d-123">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="4169d-123">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>

[DriveItem]: driveitem.md
[IdentitySet]: identityset.md

<!-- {
  "type": "#page.annotation",
  "description": "The sharing invitation facet describes details of a sharing invitation associated with a permission.",
  "keywords": "image,width,height,item,facet",
  "section": "documentation",
  "tocPath": "Facets/SharingInvitation"
} -->
