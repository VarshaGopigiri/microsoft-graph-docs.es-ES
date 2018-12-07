---
title: Crear governanceRoleAssignmentRequest
description: Cree una solicitud de asignación de rol para representar la operación que desee en una asignación de roles. En la siguiente tabla se enumera las operaciones.
ms.openlocfilehash: 775cc8e22e7d273bfe387e5be2cc183d3d919a38
ms.sourcegitcommit: 82f9d0d10388572a3073b2dde8ca0a7b409135b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/07/2018
ms.locfileid: "27191175"
---
# <a name="create-governanceroleassignmentrequest"></a>Crear governanceRoleAssignmentRequest

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Cree una solicitud de asignación de rol para representar la operación que desee en una asignación de roles. En la siguiente tabla se enumera las operaciones.

| Operación       | Tipo | 
|:---------------|:----------|
| Asignar una asignación de roles| AdminAdd |
| Activar una asignación de rol optan| Comandos UserAdd | 
| Desactivación de una asignación de rol activada| UserRemove | 
| Quitar una asignación de roles| AdminRemove |
| Actualizar una asignación de roles| AdminUpdate |
| Solicitud para ampliar la asignación de roles| UserExtend | 
| Extender una asignación de roles| AdminExtend | 
| Solicitud para renovar la asignación de rol que han expirado| UserRenew | 
| Renovar una asignación de rol que han expirado| AdminRenew | 

 
## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | PrivilegedAccess.ReadWrite.AzureResources  |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | PrivilegedAccess.ReadWrite.AzureResources |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /privilegedAccess/azureResources/roleAssignmentRequests
```

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Descripción|
|:---------------|:----------|
| Autorización  | Portador {código}|
| Tipo de contenido  | application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcionar una representación JSON de un objeto [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md) . 

| Propiedad     | Tipo    |Obligatorio|  Descripción|
|:---------------|:--------|:----------|:----------|
|resourceId|Cadena|Sí|El identificador del recurso.|
|roleDefinitionId|Cadena|Sí|El identificador de la definición de roles.|
|///SubjectID|Cadena|Sí|El identificador del tema.|
|assignmentState|Cadena|Sí|El estado de asignación. El valor puede ser ``Eligible`` y ``Active``.|
|type|Cadena|Sí|El tipo de solicitud. El valor puede ser `AdminAdd`, `UserAdd`, `AdminUpdate`, `AdminRemove`, `UserRemove`, `UserExtend`, `UserRenew`, `AdminRenew`y `AdminExtend`.|
|motivo|String| |Necesita la razón por la que se proporcionará para la solicitud de asignación de rol para auditoría y revise el propósito.|
|programación|[governanceSchedule](../resources/governanceschedule.md)| | La programación de la solicitud de asignación de rol. Para tipo de solicitud de `UserAdd`, `AdminAdd`, `AdminUpdate`, y `AdminExtend`, es necesario.|

## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md) en el cuerpo de la respuesta.

### <a name="error-codes"></a>Códigos de error
Esta API devuelve los códigos de error HTTP estándares. Además, también devuelve los códigos de error que aparecen en la siguiente tabla.

|Código de error     | Mensaje de error              | Detalles |
|:--------------------| :---------------------|:--------------------|
| 400 BadRequest | RoleNotFound    | El `roleDefinitionId` proporcionado en la solicitud no se encuentra el cuerpo.
| 400 BadRequest | ResourceIsLocked    | El recurso proporcionado en el cuerpo de la solicitud se encuentra en estado de `Locked` y no se puede crear solicitudes de asignación de rol.
| 400 BadRequest | SubjectNotFound    | El `subjectId` proporcionado en la solicitud no se encuentra el cuerpo.
| 400 BadRequest | PendingRoleAssignmentRequest    | Ya existe una pendiente [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md) en el sistema.
| 400 BadRequest | RoleAssignmentExists    | El [governanceRoleAssignment](../resources/governanceroleassignment.md) solicitada que se va a crear ya existe en el sistema.
| 400 BadRequest | RoleAssignmentDoesNotExist    | El [governanceRoleAssignment](../resources/governanceroleassignment.md) solicitado se actualizó y ampliar no existe en el sistema.
| 400 BadRequest | RoleAssignmentRequestPolicyValidationFailed | La [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md) no cumple las políticas internas y no se puede crear.

## <a name="examples"></a>Ejemplos
Los siguientes ejemplos muestran cómo usar esta API.

### <a name="example-1"></a>Ejemplo 1
En este ejemplo, los administradores asignan nawu@fimdev.net usuario a la función de lector de facturación.

 >**Nota:** Además de los permisos, en este ejemplo se requiere que el solicitante tiene al menos una `Active` asignación de roles de administrador (`owner` o `user access administrator`) en el recurso. 

| Propiedad     | Tipo    |Obligatorio|  Valor |
|:---------------|:--------|:----------|:----------|
|resourceId|Cadena|Sí|\<resourceId\>|
|roleDefinitionId|Cadena|Sí|\<roleDefinitionId\>|
|///SubjectID|Cadena|Sí|\<///SubjectID\>|
|assignmentState|Cadena|Sí| Optan / activo|
|type|Cadena|Sí| AdminAdd|
|motivo|String| depende de la función configuración||
|programación|[governanceSchedule](../resources/governanceschedule.md)|Sí|        |
##### <a name="request"></a>Solicitud
<!-- {
  "blockType": "request",
  "name": "governanceroleassignmentrequest_post"
}-->
```http
POST https://graph.microsoft.com/beta/privilegedAccess/azureResources/roleAssignmentRequests
Content-type: application/json

{"roleDefinitionId":"ea48ad5e-e3b0-4d10-af54-39a45bbfe68d",
"resourceId":"e5e7d29d-5465-45ac-885f-4716a5ee74b5",
"subjectId":"918e54be-12c4-4f4c-a6d3-2ee0e3661c51",
"assignmentState":"Eligible",
"type":"AdminAdd",
"reason":"Assign an eligible role",
"schedule":{
  "startDateTime":"2018-05-12T23:37:43.356Z",
  "endDateTime":"2018-11-08T23:37:43.356Z",
  "type":"Once"
  }
}
```
##### <a name="response"></a>Respuesta
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.governanceRoleAssignmentRequest"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 226

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#governanceRoleAssignmentRequests/$entity",
    "id": "1232e4ea-741a-4be5-8044-5edabdd61672",
    "resourceId": "e5e7d29d-5465-45ac-885f-4716a5ee74b5",
    "roleDefinitionId": "ea48ad5e-e3b0-4d10-af54-39a45bbfe68d",
    "subjectId": "918e54be-12c4-4f4c-a6d3-2ee0e3661c51",
    "linkedEligibleRoleAssignmentId": "",
    "type": "AdminAdd",
    "assignmentState": "Eligible",
    "requestedDateTime": "0001-01-01T00:00:00Z",
    "reason": "Evaluate Only",
    "status": {
        "status": "InProgress",
        "subStatus": "Granted",
        "statusDetails": [
            {
                "key": "AdminRequestRule",
                "value": "Grant"
            },
            {
                "key": "ExpirationRule",
                "value": "Grant"
            },
            {
                "key": "MfaRule",
                "value": "Grant"
            }
        ]
    },
    "schedule": {
        "type": "Once",
        "startDateTime": "2018-05-12T23:37:43.356Z",
        "endDateTime": "2018-11-08T23:37:43.356Z",
        "duration": "PT0S"
    }
}
```

### <a name="example-2"></a>Ejemplo 2
En este ejemplo, el usuario nawu@fimdev.net activa la función de lector de facturación optan.

| Propiedad     | Tipo    |Obligatorio|  Valor |
|:---------------|:--------|:----------|:----------|
|resourceId|Cadena|Sí|\<resourceId\>|
|roleDefinitionId|Cadena|Sí|\<roleDefinitionId\>|
|///SubjectID|Cadena|Sí|\<///SubjectID\>|
|assignmentState|Cadena|Sí| Activo|
|type|Cadena|Sí| Comandos UserAdd|
|motivo|String| depende de la función configuración||
|programación|[governanceSchedule](../resources/governanceschedule.md)|Sí|        |
##### <a name="request"></a>Solicitud
<!-- {
  "blockType": "request",
  "name": "governanceroleassignmentrequest_post"
}-->
```http
POST https://graph.microsoft.com/beta/privilegedAccess/azureResources/roleAssignmentRequests
Content-type: application/json

{"roleDefinitionId":"8b4d1d51-08e9-4254-b0a6-b16177aae376",
"resourceId":"e5e7d29d-5465-45ac-885f-4716a5ee74b5",
"subjectId":"918e54be-12c4-4f4c-a6d3-2ee0e3661c51",
"assignmentState":"Active",
"type":"UserAdd",
"reason": "Activate the owner role",
"schedule":{
  "type":"Once",
  "startDateTime":"2018-05-12T23:28:43.537Z",
  "duration":"PT9H"
  },
"linkedEligibleRoleAssignmentId":"e327f4be-42a0-47a2-8579-0a39b025b394"
}
```
##### <a name="response"></a>Respuesta
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.governanceRoleAssignmentRequest"
} -->
```json
HTTP/1.1 201 Created
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#governanceRoleAssignmentRequests/$entity",
    "id": "3ad49a7c-918e-4d86-9f84-fab28f8658c0",
    "resourceId": "e5e7d29d-5465-45ac-885f-4716a5ee74b5",
    "roleDefinitionId": "8b4d1d51-08e9-4254-b0a6-b16177aae376",
    "subjectId": "918e54be-12c4-4f4c-a6d3-2ee0e3661c51",
    "linkedEligibleRoleAssignmentId": "e327f4be-42a0-47a2-8579-0a39b025b394",
    "type": "UserAdd",
    "assignmentState": "Active",
    "requestedDateTime": "0001-01-01T00:00:00Z",
    "reason": "Activate the owner role",
    "status": {
        "status": "InProgress",
        "subStatus": "Granted",
        "statusDetails": [
            {
                "key": "EligibilityRule",
                "value": "Grant"
            },
            {
                "key": "ExpirationRule",
                "value": "Grant"
            },
            {
                "key": "MfaRule",
                "value": "Grant"
            },
            {
                "key": "JustificationRule",
                "value": "Grant"
            },
            {
                "key": "ActivationDayRule",
                "value": "Grant"
            },
            {
                "key": "ApprovalRule",
                "value": "Grant"
            }
        ]
    },
    "schedule": {
        "type": "Once",
        "startDateTime": "2018-05-12T23:28:43.537Z",
        "endDateTime": "0001-01-01T00:00:00Z",
        "duration": "PT9H"
    }
}
```

### <a name="example-3"></a>Ejemplo 3
En este ejemplo, el usuario nawu@fimdev.net desactiva la función de lector de facturación activada.

| Propiedad     | Tipo    |Obligatorio|  Valor |
|:---------------|:--------|:----------|:----------|
|resourceId|Cadena|Sí|\<resourceId\>|
|roleDefinitionId|Cadena|Sí|\<roleDefinitionId\>|
|///SubjectID|Cadena|Sí|\<///SubjectID\>|
|assignmentState|Cadena|Sí| Activo|
|type|Cadena|Sí| UserRemove|
|motivo|Cadena| No||
|programación|[governanceSchedule](../resources/governanceschedule.md)|No|        |
##### <a name="request"></a>Solicitud
<!-- {
  "blockType": "request",
  "name": "governanceroleassignmentrequest_post"
}-->
```http
POST https://graph.microsoft.com/beta/privilegedAccess/azureResources/roleAssignmentRequests
Content-type: application/json

{"roleDefinitionId":"bc75b4e6-7403-4243-bf2f-d1f6990be122",
"resourceId":"fb016e3a-c3ed-4d9d-96b6-a54cd4f0b735",
"subjectId":"918e54be-12c4-4f4c-a6d3-2ee0e3661c51",
"assignmentState":"Active",
"type":"UserRemove",
"reason":"Deactivate the role",
"linkedEligibleRoleAssignmentId":"cb8a533e-02d5-42ad-8499-916b1e4822ec"
}
```
##### <a name="response"></a>Respuesta
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.governanceRoleAssignmentRequest"
} -->
```json
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 226

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#governanceRoleAssignmentRequests/$entity",
    "id": "abfcdb57-8e5d-42a0-ae67-7598b96fddb1",
    "resourceId": "fb016e3a-c3ed-4d9d-96b6-a54cd4f0b735",
    "roleDefinitionId": "bc75b4e6-7403-4243-bf2f-d1f6990be122",
    "subjectId": "918e54be-12c4-4f4c-a6d3-2ee0e3661c51",
    "linkedEligibleRoleAssignmentId": "cb8a533e-02d5-42ad-8499-916b1e4822ec",
    "type": "UserRemove",
    "assignmentState": "Active",
    "requestedDateTime": "0001-01-01T00:00:00Z",
    "reason": "Evaluate only",
    "schedule": null,
    "status": {
        "status": "Closed",
        "subStatus": "Revoked",
        "statusDetails": []
    }
}
```

### <a name="example-4"></a>Ejemplo 4
En este ejemplo, los administradores de quitar el usuario nawu@fimdev.net de la función de lector de facturación.

 >**Nota:** Además de los permisos, en este ejemplo se requiere que el solicitante tiene al menos una `Active` asignación de roles de administrador (`owner` o `user access administrator`) en el recurso.
 
| Propiedad     | Tipo    |Obligatorio|  Valor |
|:---------------|:--------|:----------|:----------|
|resourceId|Cadena|Sí|\<resourceId\>|
|roleDefinitionId|Cadena|Sí|\<roleDefinitionId\>|
|///SubjectID|Cadena|Sí|\<///SubjectID\>|
|assignmentState|Cadena|Sí| Optan / activo|
|type|Cadena|Sí| AdminRemove|
|motivo|Cadena| No||
|programación|[governanceSchedule](../resources/governanceschedule.md)|No|        |
##### <a name="request"></a>Solicitud
<!-- {
  "blockType": "request",
  "name": "governanceroleassignmentrequest_post"
}-->
```http
POST https://graph.microsoft.com/beta/privilegedAccess/azureResources/roleAssignmentRequests
Content-type: application/json

{
  "roleDefinitionId":"65bb4622-61f5-4f25-9d75-d0e20cf92019",
  "resourceId":"e5e7d29d-5465-45ac-885f-4716a5ee74b5",
  "subjectId":"74765671-9ca4-40d7-9e36-2f4a570608a6",
  "assignmentState":"Eligible",
  "type":"AdminRemove"
}
```
##### <a name="response"></a>Respuesta
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.governanceRoleAssignmentRequest"
} -->
```json
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 226

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#governanceRoleAssignmentRequests/$entity",
  "id":"c934fcb9-cf53-42ac-a8b4-6246f6726299",
  "resourceId":"e5e7d29d-5465-45ac-885f-4716a5ee74b5",
  "roleDefinitionId":"65bb4622-61f5-4f25-9d75-d0e20cf92019",
  "subjectId":"74765671-9ca4-40d7-9e36-2f4a570608a6",
  "linkedEligibleRoleAssignmentId":"",
  "type":"AdminRemove",
  "assignmentState":"Eligible",
  "requestedDateTime":"0001-01-01T00:00:00Z",
  "reason":null,
  "status":{
    "status":"Closed",
    "subStatus":"Revoked",
    "statusDetails":[]
  },
  "schedule":null
}
```

### <a name="example-5"></a>Ejemplo 5
En este ejemplo, los administradores actualizar la asignación de rol para el usuario nawu@fimdev.net al propietario.

 >**Nota:** Además de los permisos, en este ejemplo se requiere que el solicitante tiene al menos una `Active` asignación de roles de administrador (`owner` o `user access administrator`) en el recurso. 

| Propiedad     | Tipo    |Obligatorio|  Valor |
|:---------------|:--------|:----------|:----------|
|resourceId|Cadena|Sí|\<resourceId\>|
|roleDefinitionId|Cadena|Sí|\<roleDefinitionId\>|
|///SubjectID|Cadena|Sí|\<///SubjectID\>|
|assignmentState|Cadena|Sí| Optan / activo|
|type|Cadena|Sí| AdminUpdate|
|motivo|String| depende de roleSettings||
|programación|[governanceSchedule](../resources/governanceschedule.md)|Sí|        |
##### <a name="request"></a>Solicitud
<!-- {
  "blockType": "request",
  "name": "governanceroleassignmentrequest_post"
}-->
```http
POST https://graph.microsoft.com/beta/privilegedAccess/azureResources/roleAssignmentRequests
Content-type: application/json

{
  "roleDefinitionId":"70521f3e-3b95-4e51-b4d2-a2f485b02103",
  "resourceId":"e5e7d29d-5465-45ac-885f-4716a5ee74b5",
  "subjectId":"1566d11d-d2b6-444a-a8de-28698682c445",
  "assignmentState":"Eligible",
  "type":"AdminUpdate",
  "schedule":{
    "type":"Once",
    "startDateTime":"2018-03-08T05:42:45.317Z",
    "endDateTime":"2018-06-05T05:42:31.000Z"
  }
}
```
##### <a name="response"></a>Respuesta
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.governanceRoleAssignmentRequest"
} -->
```json
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 226

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#governanceRoleAssignmentRequests/$entity",
  "id":"4f6d4802-b3ac-4f5a-86d7-a6a4edd7d383",
  "resourceId":"e5e7d29d-5465-45ac-885f-4716a5ee74b5",
  "roleDefinitionId":"70521f3e-3b95-4e51-b4d2-a2f485b02103",
  "subjectId":"1566d11d-d2b6-444a-a8de-28698682c445",
  "linkedEligibleRoleAssignmentId":"",
  "type":"AdminUpdate",
  "assignmentState":"Eligible",
  "requestedDateTime":"0001-01-01T00:00:00Z",
  "reason":null,
  "status":{
    "status":"InProgress",
    "subStatus":"Granted",
    "statusDetails":[
      {
        "key":"AdminRequestRule","value":"Grant"
      },{
        "key":"ExpirationRule","value":"Grant"
      },{
        "key":"MfaRule","value":"Grant"
      }
    ]
  },
  "schedule":{
    "type":"Once",
    "startDateTime":"2018-03-08T05:42:45.317Z",
    "endDateTime":"2018-06-05T05:42:31Z",
    "duration":"PT0S"
  }
}
```

### <a name="example-6"></a>Ejemplo 6
En este ejemplo se extiende la asignación de roles a punto de expirar para usuario ANUJCUSER a la API de administración de servicio colaborador.

 >**Nota:** Aparte de los permisos, en este ejemplo se requiere que el solicitante tiene al menos una `Active` asignación de roles de administrador (`owner` o `user access administrator`) en el recurso.
 
| Propiedad     | Tipo    |Obligatorio|  Valor |
|:---------------|:--------|:----------|:----------|
|resourceId|Cadena|Sí|\<resourceId\>|
|roleDefinitionId|Cadena|Sí|\<roleDefinitionId\>|
|///SubjectID|Cadena|Sí|\<///SubjectID\>|
|assignmentState|Cadena|Sí| Optan / activo |
|type|Cadena|Sí| AdminExtend|
|motivo|String| depende de roleSettings||
|programación|[governanceSchedule](../resources/governanceschedule.md)|Sí|        |
##### <a name="request"></a>Solicitud
<!-- {
  "blockType": "request",
  "name": "governanceroleassignmentrequest_post"
}-->
```http
POST https://graph.microsoft.com/beta/privilegedAccess/azureResources/roleAssignmentRequests
Content-type: application/json

{
  "roleDefinitionId":"0e88fd18-50f5-4ee1-9104-01c3ed910065",
  "resourceId":"e5e7d29d-5465-45ac-885f-4716a5ee74b5",
  "subjectId":"74765671-9ca4-40d7-9e36-2f4a570608a6",
  "assignmentState":"Eligible",
  "type":"AdminExtend",
  "reason":"extend role assignment",
  "schedule":{
    "type":"Once",
    "startDateTime":"2018-05-12T23:53:55.327Z",
    "endDateTime":"2018-08-10T23:53:55.327Z"
  }
}
```
##### <a name="response"></a>Respuesta
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.governanceRoleAssignmentRequest"
} -->
```json
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 226

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#governanceRoleAssignmentRequests/$entity",
  "id":"486f0c05-47c8-4498-9c06-086a78c83004",
  "resourceId":"e5e7d29d-5465-45ac-885f-4716a5ee74b5",
  "roleDefinitionId":"0e88fd18-50f5-4ee1-9104-01c3ed910065",
  "subjectId":"74765671-9ca4-40d7-9e36-2f4a570608a6",
  "linkedEligibleRoleAssignmentId":"",
  "type":"AdminExtend",
  "assignmentState":"Eligible",
  "requestedDateTime":"0001-01-01T00:00:00Z",
  "reason":"extend role assignment",
  "status":{
    "status":"InProgress",
    "subStatus":"Granted",
    "statusDetails":[
      {
        "key":"AdminRequestRule","value":"Grant"
      },{
        "key":"ExpirationRule","value":"Grant"
      },{
        "key":"MfaRule","value":"Grant"
      }
    ]
  },
  "schedule":{
    "type":"Once",
    "startDateTime":"2018-05-12T23:53:55.327Z",
    "endDateTime":"2018-08-10T23:53:55.327Z",
    "duration":"PT0S"
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Post roleAssignmentRequest",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
