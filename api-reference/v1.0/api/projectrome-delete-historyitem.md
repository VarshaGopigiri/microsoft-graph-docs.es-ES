---
title: Eliminar un historyItem
description: Eliminar un elemento de historial existente para una actividad de usuario existente.
ms.openlocfilehash: 231a5dd1ffdeb09dab2ad08346b0202a1fe3d8fc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031113"
---
# <a name="delete-a-historyitem"></a>Eliminar un historyItem

Eliminar un elemento de historial existente para una actividad de usuario existente.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).


|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | UserActivity.ReadWrite.CreatedByApp    |
|Delegado (cuenta personal de Microsoft) | UserActivity.ReadWrite.CreatedByApp    |
|Aplicación | No admitida. |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
DELETE /me/activities/{id}/historyItems/{id}
```

## <a name="request-headers"></a>Encabezados de solicitud

|Nombre | Tipo | Descripción|
|:----|:-----|:-----------|
|Authorization | string | {token} de portador. Obligatorio.|

## <a name="request-body"></a>Cuerpo de la solicitud

Ningún cuerpo de la solicitud.

## <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve el `204 No Content` código de respuesta si se ha eliminado el elemento de historial.

## <a name="example"></a>Ejemplo

##### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.

<!-- {
  "blockType": "request",
  "name": "delete_historyItem"
}-->

```http
PUT https://graph.microsoft.com/v1.0/me/activities/{activity-id}/historyItems/{item-id}
```

##### <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta.

<!-- {
  "blockType": "response",
  "truncated": true,
} -->

```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2017-06-07 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete historyitem",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->