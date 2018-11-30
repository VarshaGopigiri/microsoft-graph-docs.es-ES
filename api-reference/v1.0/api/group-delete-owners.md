---
title: Remove owner
description: Use esta API para quitar un propietario de un grupo de Office 365, un grupo de seguridad o un grupo de seguridad habilitado para correo a través de la propiedad de navegación owners.
ms.openlocfilehash: 08136afce038e4287a29a31408bf7a5e1ae14d91
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028778"
---
# <a name="remove-owner"></a>Remove owner
Use esta API para quitar un propietario de un grupo de Office 365, un grupo de seguridad o un grupo de seguridad habilitado para correo a través de la propiedad de navegación owners.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | Group.ReadWrite.All, Directory.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/owners/{id}/$ref
```

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción|
|:---------------|:--------|:----------|
| Authorization  | string  | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
#### <a name="request"></a>Solicitud
Este es un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "delete_owner_from_group"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/groups/{id}/owners/{id}/$ref
```
En la solicitud, especifique la `id` del objeto de directorio que quiere quitar después del segmento de $ref.

#### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta.
>**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete owner",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
