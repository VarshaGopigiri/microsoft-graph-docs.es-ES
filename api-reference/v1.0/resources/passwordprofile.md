---
title: Tipo de recurso passwordProfile
description: Contiene el perfil de contraseña asociado al usuario. La propiedad **passwordProfile** de la entidad user es un objeto **passwordProfile**.
localization_priority: Priority
ms.openlocfilehash: 80d774906fb4897f57b943af827cfbc32e90511f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27819666"
---
# <a name="passwordprofile-resource-type"></a><span data-ttu-id="3ff55-104">Tipo de recurso passwordProfile</span><span class="sxs-lookup"><span data-stu-id="3ff55-104">passwordProfile resource type</span></span>

<span data-ttu-id="3ff55-p102">Contiene el perfil de contraseña asociado al usuario. La propiedad **passwordProfile** de la entidad [user](user.md) es un objeto **passwordProfile**.</span><span class="sxs-lookup"><span data-stu-id="3ff55-p102">Contains the password profile associated with a user. The **passwordProfile** property of the [user](user.md) entity is a **passwordProfile** object.</span></span>


## <a name="properties"></a><span data-ttu-id="3ff55-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3ff55-107">Properties</span></span>
| <span data-ttu-id="3ff55-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3ff55-108">Property</span></span>     | <span data-ttu-id="3ff55-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="3ff55-109">Type</span></span>   |<span data-ttu-id="3ff55-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ff55-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3ff55-111">forceChangePasswordNextSignIn</span><span class="sxs-lookup"><span data-stu-id="3ff55-111">forceChangePasswordNextSignIn</span></span>|<span data-ttu-id="3ff55-112">Boolean</span><span class="sxs-lookup"><span data-stu-id="3ff55-112">Boolean</span></span>| <span data-ttu-id="3ff55-113">**true** si el usuario debe cambiar su contraseña en el próximo inicio de sesión; en caso contrario **false**.</span><span class="sxs-lookup"><span data-stu-id="3ff55-113">**true** if the user must change her password on the next login; otherwise **false**.</span></span> |
|<span data-ttu-id="3ff55-114">password</span><span class="sxs-lookup"><span data-stu-id="3ff55-114">password</span></span>|<span data-ttu-id="3ff55-115">String</span><span class="sxs-lookup"><span data-stu-id="3ff55-115">String</span></span>|<span data-ttu-id="3ff55-p103">Contraseña del usuario. Esta propiedad es necesaria cuando se crea un usuario. Se puede actualizar, pero el usuario deberá cambiar la contraseña en el próximo inicio de sesión. La contraseña debe cumplir los requisitos mínimos especificados por la propiedad **passwordPolicies** del usuario. De manera predeterminada, se requiere una contraseña segura.</span><span class="sxs-lookup"><span data-stu-id="3ff55-p103">The password for the user. This property is required when a user is created. It can be updated, but the user will be required to change the password on the next login. The password must satisfy minimum requirements as specified by the user’s **passwordPolicies** property. By default, a strong password is required.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="3ff55-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3ff55-121">JSON representation</span></span>

<span data-ttu-id="3ff55-122">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="3ff55-122">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.passwordProfile"
}-->

```json
{
  "forceChangePasswordNextSignIn": true,
  "password": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "passwordProfile resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
