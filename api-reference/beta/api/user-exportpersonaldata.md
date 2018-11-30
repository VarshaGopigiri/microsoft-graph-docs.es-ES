---
title: 'usuario: exportPersonalData'
description: Envía una solicitud de operación de la directiva de datos, realizada por un administrador de la compañía para exportar datos de un usuario organizativa.
ms.openlocfilehash: aceab65992bde3092676a2bfa144498f07f06095
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089362"
---
# <a name="user-exportpersonaldata"></a>usuario: exportPersonalData

Envía una solicitud de operación de la directiva de datos, realizada por un administrador de la compañía para exportar datos de un usuario organizativa.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) |  User.Export.All  |
|Delegado (cuenta personal de Microsoft) |  No disponible  |
|Aplicación | User.Export.All |

>Nota: Exportación sólo puede realizarse por un administrador de la compañía cuando se usa el permiso delegado.

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /users/<id>/exportPersonalData

```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Descripción|
|:---------------|:----------|
| Autorización  | Bearer {token}|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.

| Parámetro    | Tipo   |Descripción|
|:---------------|:--------|:----------|
|storageLocation|String|Esto es una dirección URL de firma (SAS) de acceso compartido a una cuenta de almacenamiento de Azure, para que se deben exportar los datos.|

## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
<!-- {
  "blockType": "request",
  "name": "user_exportpersonaldata"
}-->
```http
POST https://graph.microsoft.com/beta/users/{id}/exportPersonalData
Content-type: application/json
Content-length: 48

{
  "storageLocation": "storageLocation-value"
}
```

##### <a name="response"></a>Respuesta
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.none"
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user: exportPersonalData",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
