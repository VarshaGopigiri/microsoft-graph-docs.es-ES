---
title: 'group: renew'
description: Renueva la expiración de un grupo. Cuando se renueva un grupo, la expiración del grupo se amplía por el número de días definidos en la directiva.
ms.openlocfilehash: 82cbc4f982b5636cc53436091a40492d7ad83afa
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030541"
---
# <a name="group-renew"></a>group: renew

Renueva la expiración de un grupo. Cuando se renueva un grupo, la expiración del grupo se amplía por el número de días definidos en la directiva.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).
 

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Group.ReadWrite.All o Directory.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | No admitido |
|Aplicación | Group.ReadWrite.All o Directory.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/renew
```

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Descripción|
|:---------------|:----------|
| Autorización  | Bearer {token} |


## <a name="request-body"></a>Cuerpo de la solicitud

No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

##### <a name="request"></a>Solicitud

<!-- {
  "blockType": "request",
  "name": "group_renew"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/renew
```

##### <a name="response"></a>Respuesta
Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Boolean"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "group: renew",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->