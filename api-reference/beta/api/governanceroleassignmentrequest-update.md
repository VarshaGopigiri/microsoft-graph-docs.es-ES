---
title: Actualizar governanceRoleAssignmentRequests
description: Permiten a los administradores actualizar sus decisiones (`AdminApproved` o `AdminDenied`) en governanceRoleAssignmentRequests que se encuentran en estado de `PendingAdminDecision`.
ms.openlocfilehash: 0f52b810b861e18a679ae8aea4ffdf7fd2d67abd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090626"
---
# <a name="update-governanceroleassignmentrequests"></a>Actualizar governanceRoleAssignmentRequests

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Permiten a los administradores actualizar sus decisiones (`AdminApproved` o `AdminDenied`) en [governanceRoleAssignmentRequests](../resources/governanceroleassignmentrequest.md) que se encuentran en estado de `PendingAdminDecision`.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permissions              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | PrivilegedAccess.ReadWrite.AzureResources  |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | PrivilegedAccess.ReadWrite.AzureResources |

Además del ámbito de permiso, esta API requiere el solicitante puede tener al menos uno `Active` asignación de roles de administrador (`owner` o `user access administrator`) en el recurso, que pertenece el [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md) . 

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /privilegedAccess/azureResources/roleAssignmentRequests/{id}/updateRequest   
```

### <a name="request-headers"></a>Encabezados de solicitud
| Nombre           | Descripción|
|:---------------|:----------|
| Autorización  | Portador {código}|
| Tipo de contenido  | application/json|

### <a name="request-body"></a>Cuerpo de la solicitud
|Parameters      |Tipo                   |Obligatorio |Descripción|
|:-------------|:----------------------|:--------|:----------|
|motivo        |String                 |✓        |El motivo por el Administrador de su decisión.|
|toma de decisiones        |String                 |✓        |La Decisión del Administrador de la solicitud de asignación de rol. El valor debe actualizarse como `AdminApproved` o `AdminDenied`.|
|programación      |[governanceSchedule](../resources/governanceschedule.md)|        | La programación de la solicitud de asignación de rol. Para el estado de `AdminApproved`, es necesario.|
|assignmentState      |String|         | Puede ser el estado de asignación y los valores `Eligible` o `Active`. Para la toma de decisiones de `AdminApproved`, es necesario. |
### <a name="response"></a>Respuesta
Este método sólo se puede aplicar a las solicitudes que se encuentran en estado de `PendingAdminDecision`.

Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.

### <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
<!-- {
  "blockType": "request",
  "name": "updaterequest_governanceroleassignmentrequest"
}-->
```http
POST https://graph.microsoft.com/beta/privilegedAccess/azureResources/roleAssignmentRequests/7c53453e-d5a4-41e0-8eb1-32d5ec8bfdee/updateRequest
```
##### <a name="request-body"></a>Cuerpo de la solicitud
```json
{
  "reason":"approve the request to extend role assignment",
  "schedule":{
    "type":"Once",
    "startDateTime":"2018-02-20T07:31:13.451Z",
    "stopDateTime":"2018-05-21T07:31:13.451Z",
    },
  "decision":"AdminApproved",
  "assignmentState": "Eligible"
}
```

##### <a name="response"></a>Respuesta
<!-- {
  "blockType": "response",
  "@odata.type": "microsoft.graph.None"
} -->
```http
HTTP/1.1 204 No Content
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "UpdateRequest governanceRoleAssignmentRequest",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
