---
title: 'usuario: findRoomLists'
description: Obtener las listas de salas definidas en un inquilino.
author: dkershaw10
localization_priority: Priority
ms.openlocfilehash: 55ff393e828d324035050e33cf194cb49d302080
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27855737"
---
# <a name="user-findroomlists"></a>usuario: findRoomLists

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Obtener las listas de salas definidas en un inquilino.

Los inquilinos pueden organizar las salas de reuniones en listas de las salas. Cada sala de reuniones y la lista de salas está representada por una instancia de [emailAddress](../resources/emailaddress.md) .
Puede obtener todas las listas de sala en el inquilino, [obtener todas las salas](user-findrooms.md) en el inquilino u [obtener todas las salas](user-findrooms.md) en una lista de salas específicas.


## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).


|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | User.ReadBasic.All, User.Read.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | User.Read.All |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
GET /me/findRoomLists
GET /users/<id>/findRoomLists

```

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción |
|:---------------|:----------|:----------|
| Autorización  | string  | {token} de portador. Obligatorio. |
| Content-Type  | string  | application/json. Obligatorio. |


## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve una `200 OK` objeto de colección de respuesta [emailAddress](../resources/emailaddress.md) y de código en el cuerpo de la respuesta.

Si no hay listas definidas en el inquilino, se devuelve una matriz vacía.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.

<!-- {
  "blockType": "request",
  "name": "user_get_room_lists"
}-->
```http
GET https://graph.microsoft.com/beta/me/findRoomLists
```

##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. 

Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "name": "user_get_room_lists",
  "truncated": true,
  "@odata.type": "microsoft.graph.emailAddress",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.emailAddress)",
    "value": [
        {
            "name": "Building 1 Rooms",
            "address": "Building1Rooms@contoso.onmicrosoft.com"
        },
        {
            "name": "Building 2 Rooms",
            "address": "Building2Rooms@contoso.onmicrosoft.com"
        }
    ]
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user: findRoomLists",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
