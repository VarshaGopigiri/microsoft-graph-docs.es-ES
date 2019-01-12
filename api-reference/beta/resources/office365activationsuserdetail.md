---
title: tipo de recurso office365ActivationsUserDetail
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: 3e2b7d5fb3c42db02407a187649544b2560f898a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27982858"
---
# <a name="office365activationsuserdetail-resource-type"></a><span data-ttu-id="fbcb6-103">tipo de recurso office365ActivationsUserDetail</span><span class="sxs-lookup"><span data-stu-id="fbcb6-103">office365ActivationsUserDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="fbcb6-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fbcb6-104">Properties</span></span>

| <span data-ttu-id="fbcb6-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fbcb6-105">Property</span></span>             | <span data-ttu-id="fbcb6-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="fbcb6-106">Type</span></span>                                     | <span data-ttu-id="fbcb6-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="fbcb6-107">Description</span></span>                              |
| :------------------- | :--------------------------------------- | ---------------------------------------- |
| <span data-ttu-id="fbcb6-108">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="fbcb6-108">reportRefreshDate</span></span>    | <span data-ttu-id="fbcb6-109">Fecha</span><span class="sxs-lookup"><span data-stu-id="fbcb6-109">Date</span></span>                                     | <span data-ttu-id="fbcb6-110">La fecha más reciente del contenido.</span><span class="sxs-lookup"><span data-stu-id="fbcb6-110">The latest date of the content.</span></span>          |
| <span data-ttu-id="fbcb6-111">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="fbcb6-111">userPrincipalName</span></span>    | <span data-ttu-id="fbcb6-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="fbcb6-112">String</span></span>                                   | <span data-ttu-id="fbcb6-113">El nombre principal de usuario (UPN) del usuario.</span><span class="sxs-lookup"><span data-stu-id="fbcb6-113">The user principal name (UPN) of the user.</span></span> <span data-ttu-id="fbcb6-114">El UPN es un nombre de inicio de sesión de estilo de Internet para el usuario según el estándar de Internet RFC 822.</span><span class="sxs-lookup"><span data-stu-id="fbcb6-114">The UPN is an Internet-style login name for the user based on the Internet standard RFC 822.</span></span> <span data-ttu-id="fbcb6-115">Por convención, esto se debe asignar al nombre de correo electrónico del usuario.</span><span class="sxs-lookup"><span data-stu-id="fbcb6-115">By convention, this should map to the user's email name.</span></span> <span data-ttu-id="fbcb6-116">El formato general es alias@domain, donde el dominio debe estar presente en la colección del inquilino de dominios verificados.</span><span class="sxs-lookup"><span data-stu-id="fbcb6-116">The general format is alias@domain, where domain must be present in the tenant’s collection of verified domains.</span></span> <span data-ttu-id="fbcb6-117">Esta propiedad es necesaria cuando se crea un usuario.</span><span class="sxs-lookup"><span data-stu-id="fbcb6-117">This property is required when a user is created.</span></span> |
| <span data-ttu-id="fbcb6-118">displayName</span><span class="sxs-lookup"><span data-stu-id="fbcb6-118">displayName</span></span>          | <span data-ttu-id="fbcb6-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="fbcb6-119">String</span></span>                                   | <span data-ttu-id="fbcb6-120">Nombre del usuario que aparece en la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="fbcb6-120">The name displayed in the address book for the user.</span></span> <span data-ttu-id="fbcb6-121">Suele ser la combinación del nombre del usuario, la inicial del segundo nombre y el apellido.</span><span class="sxs-lookup"><span data-stu-id="fbcb6-121">This is usually the combination of the user's first name, middle initial, and last name.</span></span> <span data-ttu-id="fbcb6-122">Esta propiedad es necesaria al crearse un usuario y no puede borrarse durante las actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="fbcb6-122">This property is required when a user is created and it cannot be cleared during updates.</span></span> |
| <span data-ttu-id="fbcb6-123">userActivationCounts</span><span class="sxs-lookup"><span data-stu-id="fbcb6-123">userActivationCounts</span></span> | <span data-ttu-id="fbcb6-124">colección de [userActivationCounts](../resources/useractivationcounts.md)</span><span class="sxs-lookup"><span data-stu-id="fbcb6-124">[userActivationCounts](../resources/useractivationcounts.md) collection</span></span> | <span data-ttu-id="fbcb6-125">Los recuentos de activación del producto más reciente del usuario en todas las plataformas para todos los tipos de producto asignado.</span><span class="sxs-lookup"><span data-stu-id="fbcb6-125">The user's latest product activation counts on all the platforms for all the assigned product types.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="fbcb6-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fbcb6-126">JSON representation</span></span>

<span data-ttu-id="fbcb6-127">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="fbcb6-127">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.office365ActivationsUserDetail"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "userPrincipalName": "String", 
  "displayName": "String", 
  "userActivationCounts": [{"@odata.type":"microsoft.graph.userActivationCounts"}]
}
```
