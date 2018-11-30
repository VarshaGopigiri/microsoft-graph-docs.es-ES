---
title: Activar directoryRole
description: Active un rol de directorio. Para leer un rol de directorio o actualizar sus miembros, debe activarse primero en el inquilino. Solo se activan de manera predeterminada los administradores de la empresa y los roles del directorio de usuarios implícitos. Para acceder y asignar miembros a otro rol de directorio, primero debe activarlo con la plantilla de rol de directorio correspondiente (directoryRoleTemplate).
ms.openlocfilehash: 2d2f51aab33520c95bda88eab8f98af12af36083
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031580"
---
# <a name="activate-directoryrole"></a>Activar directoryRole

Active un rol de directorio. Para leer un rol de directorio o actualizar sus miembros, debe activarse primero en el inquilino. Solo se activan de manera predeterminada los administradores de la empresa y los roles del directorio de usuarios implícitos. Para acceder y asignar miembros a otro rol de directorio, primero debe activarlo con la plantilla de rol de directorio correspondiente ([directoryRoleTemplate](../resources/directoryroletemplate.md)).

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Directory.ReadWrite.All, Directory.AccessAsUser.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | Directory.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /directoryRoles

```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción|
|:---------------|:--------|:----------|
| Authorization  | string  | {token} de portador. Obligatorio. |
| Content-Type  | string  | application/json  |

## <a name="request-body"></a>Cuerpo de solicitud
En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryRole](../resources/directoryrole.md).

En la tabla siguiente, se muestran las propiedades necesarias al activar un rol de directorio.

|Parámetro | Tipo | Descripción|
|:---------|:---------|:---------|
|roleTemplateId | string | Obligatorio. El identificador de [directoryRoleTemplate](../resources/directoryroletemplate.md) que se basa el rol. Esta es la única propiedad que se puede especificar en la solicitud.|

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [directoryRole](../resources/directoryrole.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud

<!-- {
  "blockType": "request",
  "name": "create_directoryrole_from_directoryroles"
}-->
```http
POST https://graph.microsoft.com/v1.0/directoryRoles
Content-type: application/json

{
  "roleTemplateId": "roleTemplateId-value"
}
```
En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryRole](../resources/directoryrole.md).
##### <a name="response"></a>Respuesta
Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryRole"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "description": "description-value",
  "displayName": "displayName-value",
  "roleTemplateId": "roleTemplateId-value",
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create directoryRole",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
