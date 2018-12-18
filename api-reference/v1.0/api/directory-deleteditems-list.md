---
title: Enumerar elementos eliminados
description: Recuperar una lista de elementos eliminados recientemente de elementos eliminados.
author: lleonard-msft
ms.openlocfilehash: 4c972ca554f7a073ddfb5b3472784240c691c973
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27314283"
---
# <a name="list-deleted-items"></a>Enumerar elementos eliminados

Recuperar una lista de elementos eliminados recientemente de [elementos eliminados](../resources/directory.md).

Actualmente, la funcionalidad de elementos eliminados solo es compatible con los recursos [group](../resources/group.md) y [user](../resources/user.md).

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

### <a name="for-users"></a>Para los usuarios:

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All |
|Delegado (cuenta personal de Microsoft) | No admitida. |
|Aplicación | User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All |

### <a name="for-groups"></a>Para los grupos:

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Group.Read.All, Group.ReadWrite.All, Directory.Read.All, Directory.AccessAsUser.All |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | Group.Read.All, Group.ReadWrite.All, Directory.Read.All |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http 
GET /directory/deletedItems/microsoft.graph.group
GET /directory/deletedItems/microsoft.graph.user
```

Actualmente, esta API admite la recuperación de tipos de objeto de grupos (microsoft.graph.group) o de usuarios (microsoft.graph.user) de los elementos eliminados. El tipo se especifica como parte necesaria del URI. Llamar a GET/directory/deletedItems sin un tipo no es compatible.

## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales
Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre      |Descripción|
|:----------|:----------|
| Authorization  | &lt;Código&gt; de portador *necesario*|
| Accept  | application/json |

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.
## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud

<!-- {
  "blockType": "request",
  "name": "get_deleteditems"
}-->
```http
GET https://graph.microsoft.com/v1.0/directory/deletedItems/microsoft.graph.group
```
##### <a name="response"></a>Respuesta
Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#groups",
  "value": [
    {
      "id":"46cc6179-19d0-473e-97ad-6ff84347bbbb",
      "displayName":"SampleGroup",
      "groupTypes":["Unified"],
      "mail":"example@contoso.com",
      "mailEnabled":true,
      "mailNickname":"Example",
      "securityEnabled":false,
      "visibility":"Public"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List deleteditems",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->