---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Cambiar los permisos de uso compartido
ms.openlocfilehash: d6c710ca4d90bffba18cde316410480f1dde5821
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029882"
---
# <a name="update-sharing-permission"></a>Actualizar permisos de uso compartido

Actualice las propiedades de un permiso de uso compartido al aplicar revisiones al recurso del permiso.

Solo se puede modificar de esta forma la propiedad **roles**.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | Files.ReadWrite, Files.ReadWrite.All    |
|Aplicación | Files.ReadWrite.All, Sites.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
PATCH /drives/{drive-id}/items/{item-id}/permissions/{perm-id}
PATCH /groups/{group-id}/drive/items/{item-id}/permissions/{perm-id}
PATCH /me/drive/items/{item-id}/permissions/{perm-id}
PATCH /sites/{site-id}/drive/items/{item-id}/permissions/{perm-id}
PATCH /users/{user-id}/drive/items/{item-id}/permissions/{perm-id}
```

## <a name="optional-request-headers"></a>Encabezados de solicitud opcionales

| Nombre          | Tipo   | Descripción                                                                                                                                                                                       |
|:--------------|:-------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| if-match      | string | Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada no coincide con la etiqueta actual del archivo, se devuelve una respuesta `412 Precondition Failed` y el elemento no se borrará. |

## <a name="request-body"></a>Cuerpo de la solicitud

En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.

Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.
Para obtener el mejor rendimiento no debe incluir valores existentes que no hayan cambiado.

| Propiedad | Tipo              | Descripción                   |
|:---------|:------------------|:------------------------------|
| roles    | Colección String | Matriz de tipos de permisos. |

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [permission](../resources/permission.md) actualizado en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

Aquí tiene un ejemplo de la solicitud que cambia el rol en el permiso de uso compartido a solo lectura.

<!-- { "blockType": "request", "name": "update-permission", "@odata.type": "microsoft.graph.permission", "scopes": "files.readwrite", "tags": "service.graph" } -->

```http
PATCH /me/drive/items/{item-id}/permissions/{perm-id}
Content-type: application/json

{
  "roles": [ "read" ]
}
```

### <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un recurso [Permission](../resources/permission.md) en el cuerpo de la respuesta que representa el estado actualizado del permiso.

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.permission", "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "grantedTo": {
    "user": {
      "displayName": "Ryan Gregg",
      "id": "efee1b77-fb3b-4f65-99d6-274c11914d12"
    }
  },
  "id": "1",
  "roles": [ "read" ]
}
```

## <a name="error-responses"></a>Respuestas de error

Lea el tema [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.

[error-response]: /graph/errors

<!-- {
  "type": "#page.annotation",
  "description": "Update an item's sharing permissions",
  "keywords": "permission, permissions, sharing, change permissions, update permission",
  "section": "documentation",
  "tocPath": "Sharing/Update permission"
} -->
