---
title: tipo de recurso office365ActivationsUserDetail
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 9cf0f7f841584654176c0069fb0403a86615bfd5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085318"
---
# <a name="office365activationsuserdetail-resource-type"></a><span data-ttu-id="8c7e4-103">tipo de recurso office365ActivationsUserDetail</span><span class="sxs-lookup"><span data-stu-id="8c7e4-103">office365ActivationsUserDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="8c7e4-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8c7e4-104">Properties</span></span>

| <span data-ttu-id="8c7e4-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8c7e4-105">Property</span></span>             | <span data-ttu-id="8c7e4-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="8c7e4-106">Type</span></span>                                     | <span data-ttu-id="8c7e4-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c7e4-107">Description</span></span>                              |
| :------------------- | :--------------------------------------- | ---------------------------------------- |
| <span data-ttu-id="8c7e4-108">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="8c7e4-108">reportRefreshDate</span></span>    | <span data-ttu-id="8c7e4-109">Fecha</span><span class="sxs-lookup"><span data-stu-id="8c7e4-109">Date</span></span>                                     | <span data-ttu-id="8c7e4-110">La fecha más reciente del contenido.</span><span class="sxs-lookup"><span data-stu-id="8c7e4-110">The latest date of the content.</span></span>          |
| <span data-ttu-id="8c7e4-111">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="8c7e4-111">userPrincipalName</span></span>    | <span data-ttu-id="8c7e4-112">String</span><span class="sxs-lookup"><span data-stu-id="8c7e4-112">String</span></span>                                   | <span data-ttu-id="8c7e4-113">El nombre principal de usuario (UPN) del usuario.</span><span class="sxs-lookup"><span data-stu-id="8c7e4-113">The user principal name (UPN) of the user.</span></span> <span data-ttu-id="8c7e4-114">El UPN es un nombre de inicio de sesión de estilo de Internet para el usuario según el estándar de Internet RFC 822.</span><span class="sxs-lookup"><span data-stu-id="8c7e4-114">The UPN is an Internet-style login name for the user based on the Internet standard RFC 822.</span></span> <span data-ttu-id="8c7e4-115">Por convención, esto se debe asignar al nombre de correo electrónico del usuario.</span><span class="sxs-lookup"><span data-stu-id="8c7e4-115">By convention, this should map to the user's email name.</span></span> <span data-ttu-id="8c7e4-116">El formato general es alias@domain, donde el dominio debe estar presente en la colección del inquilino de dominios verificados.</span><span class="sxs-lookup"><span data-stu-id="8c7e4-116">The general format is alias@domain, where domain must be present in the tenant’s collection of verified domains.</span></span> <span data-ttu-id="8c7e4-117">Esta propiedad es necesaria cuando se crea un usuario.</span><span class="sxs-lookup"><span data-stu-id="8c7e4-117">This property is required when a user is created.</span></span> |
| <span data-ttu-id="8c7e4-118">displayName</span><span class="sxs-lookup"><span data-stu-id="8c7e4-118">displayName</span></span>          | <span data-ttu-id="8c7e4-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="8c7e4-119">String</span></span>                                   | <span data-ttu-id="8c7e4-120">Nombre del usuario que aparece en la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="8c7e4-120">The name displayed in the address book for the user.</span></span> <span data-ttu-id="8c7e4-121">Suele ser la combinación del nombre del usuario, la inicial del segundo nombre y el apellido.</span><span class="sxs-lookup"><span data-stu-id="8c7e4-121">This is usually the combination of the user's first name, middle initial, and last name.</span></span> <span data-ttu-id="8c7e4-122">Esta propiedad es necesaria al crearse un usuario y no puede borrarse durante las actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="8c7e4-122">This property is required when a user is created and it cannot be cleared during updates.</span></span> |
| <span data-ttu-id="8c7e4-123">userActivationCounts</span><span class="sxs-lookup"><span data-stu-id="8c7e4-123">userActivationCounts</span></span> | <span data-ttu-id="8c7e4-124">colección de [userActivationCounts](../resources/useractivationcounts.md)</span><span class="sxs-lookup"><span data-stu-id="8c7e4-124">[userActivationCounts](../resources/useractivationcounts.md) collection</span></span> | <span data-ttu-id="8c7e4-125">Los recuentos de activación del producto más reciente del usuario en todas las plataformas para todos los tipos de producto asignado.</span><span class="sxs-lookup"><span data-stu-id="8c7e4-125">The user's latest product activation counts on all the platforms for all the assigned product types.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="8c7e4-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8c7e4-126">JSON representation</span></span>

<span data-ttu-id="8c7e4-127">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="8c7e4-127">The following is a JSON representation of the resource.</span></span>

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