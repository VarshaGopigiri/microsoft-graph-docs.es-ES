---
title: Crear privilegedRoleAssignmentRequest
description: Crear un objeto privilegedroleassignmentrequest.
localization_priority: Normal
ms.openlocfilehash: 3f1b88415e5671e38ad557cc28200569a42a9630
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27847776"
---
# <a name="create-privilegedroleassignmentrequest"></a>Crear privilegedRoleAssignmentRequest

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Crear un objeto [privilegedroleassignmentrequest](../resources/privilegedroleassignmentrequest.md) .

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso                        | Permisos (de menos a más privilegiados)              |
|:--------------------------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | PrivilegedAccess.ReadWrite.AzureAD, Directory.AccessAsUser.All    |
|Delegado (cuenta personal de Microsoft) | No admitida. |
|Aplicación                            | No admitida. |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /privilegedRoleAssignmentRequests
```

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre      |Descripción|
|:----------|:----------|
| Authorization  | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [privilegedroleassignmentrequest](../resources/privilegedroleassignmentrequest.md) . 

| Propiedad     | Tipo    |  Description|
|:---------------|:--------|:----------|
|identificador de función|Cadena|El identificador de la función. Obligatorio.|
|type|Cadena|Representa el tipo de la operación en la asignación de roles. El valor puede ser `AdminAdd`: administradores agregar usuarios a funciones; `UserAdd`: Los usuarios agregar las asignaciones de roles. Necesario.|
|assignmentState|Cadena|El estado de la asignación. El valor puede ser `Eligible` para asignación optan `Active` - si está asignada directamente `Active` por los administradores, o activado en una asignación optan por los usuarios. Los valores posibles son: ``NotStarted``, `Completed`, `RequestedApproval`, `Scheduled`, `Approved`, `ApprovalDenied`, `ApprovalAborted`, `Cancelling`, `Cancelled`, `Revoked` y `RequestExpired`. Necesario.|
|motivo|Cadena|Necesita la razón por la que se proporcionará para la solicitud de asignación de rol para auditoría y revise el propósito.|
|programación|[governanceSchedule](../resources/governanceschedule.md)|La programación de la solicitud de asignación de rol.|

## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [privilegedRoleAssignmentRequest](../resources/privilegedroleassignmentrequest.md) en el cuerpo de la respuesta.

### <a name="error-codes"></a>Códigos de error
Esta API devuelve ese estándar de códigos de error HTTP. Además, puede devolver los códigos de error que aparecen en la siguiente tabla.

|Código de error     | Mensaje de error              | 
|:--------------------| :---------------------|
| 400 BadRequest | Propiedad RoleAssignmentRequest es NULL. |
| 400 BadRequest | No se puede deserializar roleAssignmentRequest objeto. |
| 400 BadRequest | Se requiere el identificador de función. |
| 400 BadRequest | Fecha de inicio de la programación debe especificarse y debe ser mayor que este momento. |
| 400 BadRequest | Ya existe una programación para este tipo de usuario, la función y la programación. |
| 400 BadRequest | Una aprobación pendiente ya existe para este tipo de usuario, la función y la aprobación. |
| 400 BadRequest | Falta la razón del solicitante. |
| 400 BadRequest | Razón del solicitante debe ser inferior a 500 caracteres. |
| 400 BadRequest | Duración de elevación debe estar entre 0,5 y {desde configuración}. |
| 400 BadRequest | Hay una superposición entre la activación programada y la solicitud. |
| 400 BadRequest | La función ya está activada. |
| 400 BadRequest | GenericElevateUserToRoleAssignments: Tickting información es necesaria y no se proporciona en el proceso de activación. |
| 400 BadRequest | Hay una superposición entre la activación programada y la solicitud. |
| 403 no autorizado | Elevación requiere autenticación multifactor. |
| 403 no autorizado | No se permite en nombre de elevación. |

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "post_privilegedroleassignmentrequest"
}-->
```http
POST https://graph.microsoft.com/beta/privilegedRoleAssignmentRequests
Content-type: application/json

{
    "duration": "2",
    "reason": "Activate the role for business purpose",
    "ticketNumber": "234",
    "ticketSystem": "system",
    "schedule": {
        "startDateTime": "2018-02-08T02:35:17.903Z"
    },
    "evaluateOnly": false,
    "type": "UserAdd",
    "assignmentState": "Active",
    "roleId": "88d8e3e3-8f55-4a1e-953a-9b9898b8876b"
}
```
##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán desde una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.privilegedRoleAssignmentRequest"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 304


{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#privilegedRoleAssignmentRequests/$entity",
    "schedule": {
        "type": "activation",
        "startDateTime": "2018-02-08T02:35:17.903Z",
        "endDateTime": null,
        "duration" : null
    },
    "id": "e13ef8a0-c1cb-4d03-aaae-9cd1c8ede2d1",
    "evaluateOnly": false,
    "type": "UserAdd",
    "assignmentState": "Active",
    "requestedDateTime": "2018-02-08T02:35:42.9137335Z",
    "status": "NotStarted",
    "duration": "2",
    "reason": "Activate the role for business purpose",
    "ticketNumber": "234",
    "ticketSystem": "system",
    "userId": "Self"，
    "roleId": "88d8e3e3-8f55-4a1e-953a-9b9898b8876b"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Post privilegedRoleAssignmentRequest",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
