---
title: Enumerar mensajes
description: Obtenga los mensajes del buzón del usuario que ha iniciado sesión (incluidas las carpetas Elementos eliminados y Otros correos).
localization_priority: Priority
author: dkershaw10
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 5bc831c952f13dbf67b4e7d3de6ccfd5aa28f0b1
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27976026"
---
# <a name="list-messages"></a>Enumerar mensajes

Obtenga los mensajes del buzón del usuario que ha iniciado sesión (incluidas las carpetas Elementos eliminados y Otros correos).

Actualmente, esta operación devuelve los cuerpos de los mensajes solo en formato HTML.

Hay dos escenarios donde una aplicación puede obtener los mensajes en la carpeta de correo de otro usuario:

* Si la aplicación tiene permisos de aplicación, o bien,
* Si la aplicación tiene la adecuada delega [los permisos](#permissions) de un usuario y otro usuario ha compartido una carpeta de correo con ese usuario o, se le concede acceso delegado a ese usuario. Consulte los [Detalles y un ejemplo](/graph/outlook-share-messages-folders).

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Mail.Read, Mail.ReadWrite    |
|Delegado (cuenta personal de Microsoft) | Mail.Read, Mail.ReadWrite    |
|Aplicación | Mail.Read, Mail.ReadWrite |

## <a name="http-request"></a>Solicitud HTTP

Para obtener todos los mensajes del buzón de un usuario:

<!-- { "blockType": "ignored" } -->
```http
GET /me/messages
GET /users/{id | userPrincipalName}/messages
```

Para obtener los mensajes de una carpeta específica del buzón del usuario:

<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/{id}/messages
GET /users/{id | userPrincipalName}/mailFolders/{id}/messages
```

## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales
Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción|
|:-----------|:------|:----------|
| Authorization  | string  | {token} de portador. Obligatorio. |
| Prefer: outlook.body-content-type | string | Formato de las propiedades **body** y **uniqueBody** que se devolverá. Los valores pueden ser "text" o "html". Si no se especifica el encabezado, las propiedades **body** y **uniqueBody** se devuelven en formato HTML. Opcional. |


## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Message](../resources/message.md) en el cuerpo de la respuesta.

El tamaño de página predeterminada para esta solicitud es de 10 mensajes.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "get_messages"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/messages
```
##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 317

{
  "value": [
    {
      "receivedDateTime": "datetime-value",
      "sentDateTime": "datetime-value",
      "hasAttachments": true,
      "subject": "subject-value",
      "body": {
        "contentType": "",
        "content": "content-value"
      },
      "bodyPreview": "bodyPreview-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List messages",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
