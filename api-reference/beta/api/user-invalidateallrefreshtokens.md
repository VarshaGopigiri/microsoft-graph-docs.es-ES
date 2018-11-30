---
title: 'usuario: invalidateAllRefreshTokens'
description: Invalida todos los tokens de actualización del usuario otorgan a las aplicaciones (así como las cookies de sesión en el Explorador de un usuario), al restablecer la propiedad de usuario **refreshTokensValidFromDateTime** a la fecha y hora actual. Normalmente, esta operación se realiza (por el usuario o un administrador) si el usuario tiene un dispositivo perdido o robado.  Esta operación podría impedir el acceso a los datos de la organización tener acceso a través de aplicaciones en el dispositivo sin que el usuario que se requiere en primer lugar para iniciar sesión de nuevo. De hecho, esta operación forzará que el usuario para iniciar sesión de nuevo para todas las aplicaciones que han aceptado anteriormente, independientemente del dispositivo.
ms.openlocfilehash: 23743c4bc372193a5478d79432b7bb4e0a9ec4ce
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089891"
---
# <a name="user-invalidateallrefreshtokens"></a>usuario: invalidateAllRefreshTokens

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Invalida todos los tokens de actualización del usuario otorgan a las aplicaciones (así como las cookies de sesión en el Explorador de un usuario), al restablecer la propiedad de usuario **refreshTokensValidFromDateTime** a la fecha y hora actual. Normalmente, esta operación se realiza (por el usuario o un administrador) si el usuario tiene un dispositivo perdido o robado.  Esta operación podría impedir el acceso a los datos de la organización tener acceso a través de aplicaciones en el dispositivo sin que el usuario que se requiere en primer lugar para iniciar sesión de nuevo. De hecho, esta operación forzará que el usuario para iniciar sesión de nuevo para todas las aplicaciones que han aceptado anteriormente, independientemente del dispositivo.

Para los desarrolladores, si la aplicación intenta canjee un token de acceso delegado para este usuario mediante el uso de un token de actualización invalidada, la aplicación obtendrá un error. En este caso, necesitará adquirir un nuevo token de actualización mediante la realización de una solicitud al extremo de autorizar, lo que obliga al usuario que inicie sesión en la aplicación.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

+ De la aplicación para permitir que el firmado de usuario para invalidar las aplicaciones ha dado su consentimiento a: User.ReadWrite, Directory.ReadWrite.All, Directory.AccessAsUser.All
+ Para que una aplicación permitir que un administrador invalidar las aplicaciones de un usuario ha aceptado: Directory.ReadWrite.All, Directory.AccessAsUser.All

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /me/invalidateAllRefreshTokens
POST /users/{id | userPrincipalName}/invalidateAllRefreshTokens
```
## <a name="request-headers"></a>Encabezados de solicitud
| Encabezado       | Valor |
|:---------------|:--------|
| Authorization  | {token} de portador. Obligatorio.  |

## <a name="request-body"></a>Cuerpo de la solicitud
Esta operación no tiene ningún contenido de la solicitud.

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`.

## <a name="example"></a>Ejemplo
Aquí tiene un ejemplo de cómo llamar a esta API.
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "user_invalidateallrefreshtokens"
}-->
```http
POST https://graph.microsoft.com/beta/me/invalidateAllRefreshTokens
```

##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user: invalidateAllRefreshTokens",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
