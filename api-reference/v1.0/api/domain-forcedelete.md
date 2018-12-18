---
title: Forzar la eliminación de dominio
description: Elimina un dominio mediante una operación asincrónica de larga duración.
author: lleonard-msft
ms.openlocfilehash: 85839d8bf7d36925661d0202c053574288763dc6
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27309117"
---
# <a name="force-domain-deletion"></a>Forzar la eliminación de dominio

Elimina un dominio mediante una operación asincrónica de larga duración.

Como parte de esta operación, se realizan las siguientes acciones:

* Actualizaciones de la `userPrincipalName`, `mail`, y `proxyAddresses` propiedades de `users` con referencias al dominio eliminado que se va a usar el dominio onmicrosoft.com inicial.

* Actualizaciones de la `mail` (propiedad) de `groups` con referencias al dominio eliminado que se va a usar el dominio onmicrosoft.com inicial.

* Actualizaciones de la `identifierUris` (propiedad) de `applications` con referencias al dominio eliminado que se va a usar el dominio onmicrosoft.com inicial.

* Si el número de objetos que se puede cambiar el nombre es mayor que 1000, se devuelve un error.

* Si uno de los `applications` se cambia el nombre es una aplicación de varios inquilino, se devuelve un error.

Una vez completada la eliminación del dominio, las operaciones de API para el dominio eliminado devolverá un código de estado de error 404 de HTTP. Para comprobar la eliminación de un dominio, puede realizar una operación [get de dominio](domain-get.md) .

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Directory.AccessAsUser.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | Domain.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
POST /domains/{id}/forceDelete
```

> En {id}, especifique el dominio con su nombre completo.

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre | Descripción |
|:---------------|:----------|
| Authorization  | {token} de portador. Obligatorio.|
| Content-Type  | application/json |

## <a name="request-body"></a>Cuerpo de la solicitud

En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.

| Parámetro | Type | Descripción |
|:---------------|:--------|:----------|
|`disableUserAccounts`|`Boolean`| Opción para deshabilitar las cuentas de usuario que han cambiado de nombre. Si una cuenta de usuario está deshabilitada, el usuario no podrá iniciar sesión. Si establece en **true** la `users` actualizados tal como parte de esta operación se deshabilitará.  Valor predeterminado es **true**. |

## <a name="response-body"></a>Cuerpo de la respuesta

Si tiene éxito, este método devuelve `HTTP/1.1 204 OK` código de estado.

## <a name="example"></a>Ejemplo

### <a name="request"></a>Solicitud

<!-- {
  "blockType": "request",
  "name": "domain_forcedelete"
}-->

```http
POST https://graph.microsoft.com/beta/domains/{id}/forceDelete
Content-type: application/json
Content-length: 33

{
  "disableUserAccounts": true
}
```

### <a name="response"></a>Respuesta

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.None"
} -->

```http
HTTP/1.1 204 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "domain: forcedelete",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->