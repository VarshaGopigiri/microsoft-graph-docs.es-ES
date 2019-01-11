---
title: Actualizar approleassignment
description: Actualizar las propiedades del objeto approleassignment.
localization_priority: Normal
ms.openlocfilehash: 3d0f95e5413354a28e7b9b26e9b440f147c45931
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27809635"
---
# <a name="update-approleassignment"></a>Actualizar approleassignment

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Actualizar las propiedades del objeto approleassignment.
## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Directory.AccessAsUser.All   |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | No admitida. |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
PATCH /users/{id | userPrincipalName}/appRoleAssignments/{id}
PATCH /servicePrincipals/{id}/appRoleAssignedTo
PATCH /groups/{id}/appRoleAssignments/{id}
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción|
|:-----------|:------|:----------|
| Autorización  | string  | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.

| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|creationTimestamp|DateTimeOffset|La hora de creación de la concesión.|
|id|Guid|El identificador de rol que se asignó a la entidad de seguridad.  Esta función se debe declarar por el de aplicación de destino recursos **resourceId** en su propiedad **appRoles** . Donde el recurso no declarar los permisos, debe especificarse un identificador predeterminado (identificador GUID cero).                            **Notas**: No admite valores NULL.            |
|principalDisplayName|Cadena|El nombre para mostrar de la entidad de seguridad que se ha concedido el acceso.|
|principalId|Guid|El identificador único (**objectId**) para la entidad de seguridad que se van a conceder el acceso.                            **Notas**: necesarios.            |
|principalType|Cadena|El tipo de entidad de seguridad.  Esto puede ser "User", "ServicePrincipal" o "Grupo".|
|resourceDisplayName|Cadena|El nombre para mostrar del recurso al que se realizó la asignación.|
|resourceId|Guid|El identificador único (**objectId**) para el recurso de destino (entidad de seguridad de servicio) para el que se realizó la asignación.|

## <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve una `200 OK` código de respuesta y actualizada [appRoleAssignment](../resources/approleassignment.md) objeto en el cuerpo de la respuesta.
## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "update_approleassignment"
}-->
```http
PATCH https://graph.microsoft.com/beta/appRoleAssignments/{id}
Content-type: application/json
Content-length: 233

{
  "creationTimestamp": "2016-10-19T10:37:00Z",
  "principalDisplayName": "principalDisplayName-value",
  "principalId": "principalId-value",
  "principalType": "principalType-value",
  "resourceDisplayName": "resourceDisplayName-value"
}
```
##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.approleassignment"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 253

{
  "creationTimestamp": "2016-10-19T10:37:00Z",
  "id": "id-value",
  "principalDisplayName": "principalDisplayName-value",
  "principalId": "principalId-value",
  "principalType": "principalType-value",
  "resourceDisplayName": "resourceDisplayName-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update approleassignment",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
