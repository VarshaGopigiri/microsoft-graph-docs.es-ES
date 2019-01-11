---
title: Update profilephoto
description: Actualizar la foto para cualquier usuario en el inquilino incluido el firmado de usuario, o el grupo especificado o el contacto. Desde allí
localization_priority: Normal
ms.openlocfilehash: e79a58d92276cc88884874c0a3339d52ac8c2847
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27850886"
---
# <a name="update-profilephoto"></a>Update profilephoto

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Actualizar la foto para cualquier usuario en el inquilino incluido el firmado de usuario, o el grupo especificado o el contacto. Puesto que actualmente no hay un límite de 4MB en el tamaño total de cada solicitud REST, esto limita el tamaño de la foto que puede agregar a menos de 4MB.

Utilice solo PUT para esta operación en la versión beta.

> **Nota** La operación de foto de actualización de beta es compatible con sólo el usuario trabajo o escuela buzones y no personal.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa)     | Fotos de perfiles de la ha iniciado sesión del **usuario**:<br/>User.ReadWrite, User.ReadWrite.All<br /><br />Para el recurso de **grupo**:<br />Group.ReadWrite.All<br /><br />Para el recurso de **contacto**:<br />Contacts.ReadWrite |
|Delegado (cuenta personal de Microsoft) | No admitida. |
|Aplicación                            | Tipo de recurso del **usuario**:<br/>User.ReadWrite.All<br /><br />Para el recurso de **grupo**:<br />Group.ReadWrite.All<br /><br />Para el recurso de **contacto**:<br />Contacts.ReadWrite |

> **Nota** Para actualizar la foto de un usuario de la organización, la aplicación debe tener el permiso de aplicación User.ReadWrite.All y llamar a esta API bajo su propia identidad, no en nombre de un usuario. Para obtener más información, consulte cómo [obtener acceso sin un usuario que ha iniciado sesión](/graph/auth-v2-service).

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
PUT /me/photo/$value
PUT /users/{id | userPrincipalName}/photo/$value
PUT /groups/{id}/photo/$value
PUT /me/contacts/{id}/photo/$value
PUT /users/{id | userPrincipalName}/contacts/{id}/photo/$value
PUT /me/contactfolders/{contactFolderId}/contacts/{id}/photo/$value
PUT /users/{id | userPrincipalName}/contactfolders/{contactFolderId}/contacts/{id}/photo/$value
```
## <a name="request-headers"></a>Encabezados de solicitud
| Encabezado       | Valor |
|:---------------|:--------|
| Authorization  | {token} de portador. Obligatorio.  |
| Content-Type  | image/jpeg. Obligatorio.  |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, incluya los datos binarios de la foto.

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK`.
## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "update_profilephoto"
}-->
```http
PUT https://graph.microsoft.com/beta/me/photo/$value
Content-type: image/jpeg

Binary data for the image

```
##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.profilePhoto"
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update profilephoto",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
