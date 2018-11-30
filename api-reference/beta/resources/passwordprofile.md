---
title: Tipo de recurso passwordProfile
description: Contiene el perfil de contraseña asociado al usuario. La propiedad **passwordProfile** de la entidad user es un objeto **passwordProfile**.
ms.openlocfilehash: 71a91f0848ba8218d16a59c9e1f867d14e5cad9b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090995"
---
# <a name="passwordprofile-resource-type"></a><span data-ttu-id="d34f0-104">Tipo de recurso passwordProfile</span><span class="sxs-lookup"><span data-stu-id="d34f0-104">passwordProfile resource type</span></span>

> <span data-ttu-id="d34f0-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d34f0-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d34f0-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d34f0-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d34f0-p103">Contiene el perfil de contraseña asociado al usuario. La propiedad **passwordProfile** de la entidad [user](user.md) es un objeto **passwordProfile**.</span><span class="sxs-lookup"><span data-stu-id="d34f0-p103">Contains the password profile associated with a user. The **passwordProfile** property of the [user](user.md) entity is a **passwordProfile** object.</span></span>


## <a name="properties"></a><span data-ttu-id="d34f0-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d34f0-109">Properties</span></span>
| <span data-ttu-id="d34f0-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d34f0-110">Property</span></span>     | <span data-ttu-id="d34f0-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="d34f0-111">Type</span></span>   |<span data-ttu-id="d34f0-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="d34f0-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d34f0-113">forceChangePasswordNextSignIn</span><span class="sxs-lookup"><span data-stu-id="d34f0-113">forceChangePasswordNextSignIn</span></span>|<span data-ttu-id="d34f0-114">Boolean</span><span class="sxs-lookup"><span data-stu-id="d34f0-114">Boolean</span></span>| <span data-ttu-id="d34f0-115">Si **true**, en el siguiente inicio de sesión, el usuario debe cambiar su contraseña.</span><span class="sxs-lookup"><span data-stu-id="d34f0-115">If **true**, at next sign-in, the user must change their password.</span></span> <span data-ttu-id="d34f0-116">Después de un cambio de contraseña, esta propiedad se restablecerá automáticamente a \***es false**.</span><span class="sxs-lookup"><span data-stu-id="d34f0-116">After a password change, this property will be automatically reset to \***false**.</span></span> <span data-ttu-id="d34f0-117">Si no se establece, el valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="d34f0-117">If not set, default is **false**.</span></span> |
|<span data-ttu-id="d34f0-118">forceChangePasswordNextSignInWithMfa</span><span class="sxs-lookup"><span data-stu-id="d34f0-118">forceChangePasswordNextSignInWithMfa</span></span>|<span data-ttu-id="d34f0-119">Booleano</span><span class="sxs-lookup"><span data-stu-id="d34f0-119">Boolean</span></span>| <span data-ttu-id="d34f0-120">Si **true**, en el siguiente inicio de sesión, el usuario debe llevar a cabo una autenticación multifactor (MFA) antes de que se ve obligado a cambiar su contraseña.</span><span class="sxs-lookup"><span data-stu-id="d34f0-120">If **true**, at next sign-in, the user must perform a multi-factor authentication (MFA) before being forced to change their password.</span></span> <span data-ttu-id="d34f0-121">El comportamiento es idéntico a **forceChangePasswordNextSignIn** , excepto en que el usuario es necesario para llevar a cabo en primer lugar una autenticación multifactor antes de cambiar la contraseña.</span><span class="sxs-lookup"><span data-stu-id="d34f0-121">The behavior is identical to **forceChangePasswordNextSignIn** except that the user is required to first perform a multi-factor authentication before password change.</span></span> <span data-ttu-id="d34f0-122">Después de un cambio de contraseña, esta propiedad se restablecerá automáticamente en **false**.</span><span class="sxs-lookup"><span data-stu-id="d34f0-122">After a password change, this property will be automatically reset to **false**.</span></span> <span data-ttu-id="d34f0-123">Si no se establece, el valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="d34f0-123">If not set, default is **false**.</span></span> |
|<span data-ttu-id="d34f0-124">password</span><span class="sxs-lookup"><span data-stu-id="d34f0-124">password</span></span>|<span data-ttu-id="d34f0-125">String</span><span class="sxs-lookup"><span data-stu-id="d34f0-125">String</span></span>|<span data-ttu-id="d34f0-p106">Contraseña del usuario. Esta propiedad es necesaria cuando se crea un usuario. Se puede actualizar, pero el usuario deberá cambiar la contraseña en el próximo inicio de sesión. La contraseña debe cumplir los requisitos mínimos especificados por la propiedad **passwordPolicies** del usuario. De manera predeterminada, se requiere una contraseña segura.</span><span class="sxs-lookup"><span data-stu-id="d34f0-p106">The password for the user. This property is required when a user is created. It can be updated, but the user will be required to change the password on the next login. The password must satisfy minimum requirements as specified by the user’s **passwordPolicies** property. By default, a strong password is required.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="d34f0-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d34f0-131">JSON representation</span></span>

<span data-ttu-id="d34f0-132">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d34f0-132">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.passwordprofile"
}-->

```json
{
  "forceChangePasswordNextSignIn": true,
  "forceChangePasswordNextSignInWithMfa": false,
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