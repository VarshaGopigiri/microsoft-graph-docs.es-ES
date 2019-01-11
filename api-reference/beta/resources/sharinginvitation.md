---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: SharingInvitation
localization_priority: Normal
ms.openlocfilehash: 3ba92573aaef89b1be431ade33caa6ed465917a9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27835976"
---
# <a name="sharinginvitation-resource-type"></a><span data-ttu-id="f1805-102">Tipo de recurso SharingInvitation</span><span class="sxs-lookup"><span data-stu-id="f1805-102">SharingInvitation resource type</span></span>

> <span data-ttu-id="f1805-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f1805-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f1805-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f1805-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f1805-105">El recurso **SharingInvitation** agrupa en una sola estructura los elementos de datos relacionados con invitaciones.</span><span class="sxs-lookup"><span data-stu-id="f1805-105">The **SharingInvitation** resource groups invitation-related data items into a single strucutre.</span></span>

## <a name="json-representation"></a><span data-ttu-id="f1805-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f1805-106">JSON representation</span></span>

<span data-ttu-id="f1805-107">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="f1805-107">Here is a JSON representation of the resource</span></span>

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

## <a name="properties"></a><span data-ttu-id="f1805-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f1805-108">Properties</span></span>

| <span data-ttu-id="f1805-109">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="f1805-109">Property Name</span></span>  | <span data-ttu-id="f1805-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="f1805-110">Type</span></span>                          | <span data-ttu-id="f1805-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="f1805-111">Description</span></span>                                                                                                                   |
|:---------------|:------------------------------|:------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1805-112">email</span><span class="sxs-lookup"><span data-stu-id="f1805-112">email</span></span>          | <span data-ttu-id="f1805-113">String</span><span class="sxs-lookup"><span data-stu-id="f1805-113">String</span></span>                        | <span data-ttu-id="f1805-p102">Dirección de correo proporcionada para el destinatario de la invitación para compartir. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f1805-p102">The email address provided for the recipient of the sharing invitation. Read-only.</span></span>                                          |
| <span data-ttu-id="f1805-116">invitedBy</span><span class="sxs-lookup"><span data-stu-id="f1805-116">invitedBy</span></span>      | [<span data-ttu-id="f1805-117">identitySet</span><span class="sxs-lookup"><span data-stu-id="f1805-117">identitySet</span></span>](identityset.md) | <span data-ttu-id="f1805-p103">Proporciona información sobre quién envió la invitación que creó este permiso, si esa información está disponible. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f1805-p103">Provides information about who sent the invitation that created this permission, if that information is available. Read-only.</span></span> |
| <span data-ttu-id="f1805-120">signInRequired</span><span class="sxs-lookup"><span data-stu-id="f1805-120">signInRequired</span></span> | <span data-ttu-id="f1805-121">Boolean</span><span class="sxs-lookup"><span data-stu-id="f1805-121">Boolean</span></span>                       | <span data-ttu-id="f1805-p104">Si `true` el destinatario de la invitación necesita iniciar sesión para obtener acceso al elemento compartido. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f1805-p104">If `true` the recipient of the invitation needs to sign in in order to access the shared item. Read-only.</span></span>                     |

## <a name="remarks"></a><span data-ttu-id="f1805-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f1805-124">Remarks</span></span> 

<span data-ttu-id="f1805-125">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="f1805-125">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "The sharing invitation facet describes details of a sharing invitation associated with a permission.",
  "keywords": "image,width,height,item,facet",
  "section": "documentation",
  "tocPath": ""
}-->
