---
title: Cancelar governanceRoleAssignmentRequest
description: Cancelar un governanceRoleAssignmentRequest.
ms.openlocfilehash: 3e83d47b94f69b124b841f99490a012f2e39a42c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085900"
---
# <a name="cancel-governanceroleassignmentrequest"></a>Cancelar governanceRoleAssignmentRequest

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Cancelar un [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md).

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permissions              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | PrivilegedAccess.ReadWrite.AzureResources  |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | PrivilegedAccess.ReadWrite.AzureResources |

## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales
Este método **no** admite los [parámetros de consulta de OData](/graph/query-parameters).

### <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /privilegedAccess/azureResources/roleAssignmentRequests/{id}/cancel
```

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Descripción|
|:---------------|:----------|
| Autorización  | Portador {código}|
| Tipo de contenido  | application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve el código de respuesta `204 NoContent`. No devuelve nada en el cuerpo de la respuesta. 

## <a name="error-codes"></a>Códigos de error
Esta API sigue el estándar de los códigos de HTTP. Además, se muestran los códigos de error personalizados.
|Código de error     | Mensaje de error              | Detalles |
|:--------------------| :---------------------|:--------------------|
| 400 BadRequest | RoleAssignmentRequestNotFound | La governanceRoleAssignmentRequest no existe en el sistema.
| 400 BadRequest | RequestCannotBeCancelled    | Sólo se solicita en el estado de `Granted`, `PendingApproval`, `PendingApprovalProvisioning` y `PendingAdminDecision` se puede cancelar.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "cancel_governanceroleassignmentrequest"
}-->
```http
POST https://graph.microsoft.com/beta/privilegedAccess/azureResources/roleAssignmentRequests/7c53453e-d5a4-41e0-8eb1-32d5ec8bfdee/cancel
```

##### <a name="response"></a>Respuesta
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.None"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Cancel governanceRoleAssignmentRequest",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->