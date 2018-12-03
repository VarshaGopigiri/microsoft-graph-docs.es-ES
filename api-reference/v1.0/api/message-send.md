---
title: 'message: send'
description: Enviar un mensaje en la carpeta Borrador. El mensaje de borrador puede ser un borrador del mensaje nuevo, borrador de respuesta, borrador de responder a todos, o
ms.openlocfilehash: 8fe04db6a7fe4a469374cd54a00f308e01341274
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032215"
---
# <a name="message-send"></a>message: send

Envía un mensaje de la carpeta Borrador. El borrador del mensaje puede ser un borrador de mensaje nuevo, un borrador de respuesta, un borrador de respuesta a todos o un borrador de reenvío. El mensaje se guarda en la carpeta Elementos enviados.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Mail.Send    |
|Delegado (cuenta personal de Microsoft) | Mail.Send    |
|Aplicación | Mail.Send |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
POST /me/messages/{id}/send
POST /users/{id | userPrincipalName}/messages/{id}/send
```

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre       | Tipo | Descripción|
|:---------------|:--------|:----------|
| Authorization  | string  | {token} de portador. Obligatorio. |
| Content-Length | n?mero | 0. necesarios. |

## <a name="request-body"></a>Cuerpo de la solicitud

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve el código de respuesta `202 Accepted`. No devuelve nada en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

En el siguiente ejemplo se muestra cómo llamar a esta API.

##### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "message_send"
}-->

```http
POST https://graph.microsoft.com/v1.0/me/messages/{id}/send
```

##### <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta.
<!-- {
  "blockType": "response",
  "truncated": true
} -->

```http
HTTP/1.1 202 Accepted
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "message: send",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
