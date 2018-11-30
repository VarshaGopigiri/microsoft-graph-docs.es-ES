---
title: Obtener directoryAudit
description: Proporciona un elemento específico de registro de auditoría de Azure Active Directory (u obtiene). Incluye los registros de auditoría generados por los distintos servicios de Azure Active Directory como usuario, aplicación, dispositivo y administración de grupo, con privilegios de administración de identidades, revisiones de Access, los términos de uso, protección de la identidad, la administración de contraseñas (SSPR y administración restablecimientos de contraseña ), Self service etcetera de administración de grupo...
ms.openlocfilehash: 98d7319f2910c29934494d74c618d284454afb58
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085885"
---
# <a name="get-directoryaudit"></a>Obtener directoryAudit
Proporciona un elemento específico de registro de auditoría de Azure Active Directory (u obtiene). Incluye los registros de auditoría generados por los distintos servicios de Azure Active Directory como usuario, aplicación, dispositivo y administración de grupo, con privilegios de administración de identidades, revisiones de Access, los términos de uso, protección de la identidad, la administración de contraseñas (SSPR y administración restablecimientos de contraseña ), Self service etcetera de administración de grupo...

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | AuditLog.Read.All |
|Delegado (cuenta personal de Microsoft) | No admitido   |
|Aplicación | AuditLog.Read.All | 

Además, las aplicaciones deben estar [registrado correctamente](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-api-prerequisites-azure-portal) a Azure AD.

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
GET /auditLogs/directoryAudits/{id}
```
## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales
Este método admite los siguientes parámetros de consulta de OData a modo de ayuda para personalizar la respuesta. Compruebe [Los parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) para el uso de estos parámetros.

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre      |Descripción|
|:----------|:----------|
| Autorización  | Portador {código}|

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.
## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `200 OK` objeto de código y [directoryAudit](../resources/directoryaudit.md) de respuesta en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "get_directoryaudit"
}-->
```http
GET https://graph.microsoft.com/beta/auditLogs/directoryAudits/{id}
```
##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryAudit"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 218
```
```json
{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#auditLogs/directoryAudits
  "value": [{
        "id": "id",
        "category": "UserManagement",
        "correlationId": "dax59xfb-5xfa-4x92-8x38-6e1fx7870e30",
        "result": "success",
        "resultReason": "Successfully added member to group",
        "activityDisplayName": "Add member to group",
        "activityDateTime": "2018-01-09T21:20:02.7215374Z",
        "loggedByService": "Core Directory",
        "initiatedBy": {
            "user": {
                "id": "72xx09ae-1x37-49x7-9xfe-e3xx964db09b",
                "displayName": "Jamie Doe",
                "userPrincipalName": "jdoe@wingtiptoysonline.com",
                "ipAddress": "127.0.0.1"
            },
            "app": null
        },
        "targetResources": [{
            "@odata.type": "#microsoft.graph.TargetResourceGroup",
            "id": "ef7x527d-6xx2-4xx4-8xxd-cxxfdxx5xx95",
            "displayName": "Lynda.com",
            "modifiedProperties": [{
                "displayName": "Action Client Name",
                "oldValue": null,
                "newValue": "DirectorySync"
            }],
            "groupType": "unifiedGroups"
        }, {
            "@odata.type": "#microsoft.graph.targetResourceUser",
            "id": "1x0exxf5-3xx1-4xxb-9xx0-d4xx572xxbb7",
            "displayName": null,
            "modifiedProperties": [],
            "userPrincipalName": "jdoe@contoso.com"
        }],
        "additionalDetails": [{
            "key": "Additional Detail Name",
            "value": "Additional Detail Value"
        }]
    }]
}
```