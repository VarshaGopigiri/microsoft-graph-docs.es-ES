---
title: Tipo de recurso passwordProfile
description: Contiene el perfil de contraseña asociado al usuario. La propiedad **passwordProfile** de la entidad user es un objeto **passwordProfile**.
localization_priority: Normal
ms.openlocfilehash: 11930b046fafaf89f8db751891b9b7f2f72fd99d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27839007"
---
# <a name="passwordprofile-resource-type"></a>Tipo de recurso passwordProfile

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Contiene el perfil de contraseña asociado al usuario. La propiedad **passwordProfile** de la entidad [user](user.md) es un objeto **passwordProfile**.


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|forceChangePasswordNextSignIn|Boolean| Si **true**, en el siguiente inicio de sesión, el usuario debe cambiar su contraseña. Después de un cambio de contraseña, esta propiedad se restablecerá automáticamente a ***es false**. Si no se establece, el valor predeterminado es **false**. |
|forceChangePasswordNextSignInWithMfa|Booleano| Si **true**, en el siguiente inicio de sesión, el usuario debe llevar a cabo una autenticación multifactor (MFA) antes de que se ve obligado a cambiar su contraseña. El comportamiento es idéntico a **forceChangePasswordNextSignIn** , excepto en que el usuario es necesario para llevar a cabo en primer lugar una autenticación multifactor antes de cambiar la contraseña. Después de un cambio de contraseña, esta propiedad se restablecerá automáticamente en **false**. Si no se establece, el valor predeterminado es **false**. |
|password|String|Contraseña del usuario. Esta propiedad es necesaria cuando se crea un usuario. Se puede actualizar, pero el usuario deberá cambiar la contraseña en el próximo inicio de sesión. La contraseña debe cumplir los requisitos mínimos especificados por la propiedad **passwordPolicies** del usuario. De manera predeterminada, se requiere una contraseña segura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

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
