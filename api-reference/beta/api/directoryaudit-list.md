---
title: Lista directoryAudits
description: Proporciona la lista de los registros de auditoría generados por Azure Active Directory. Incluye los registros de auditoría generados por los distintos servicios de Azure Active Directory como usuario, aplicación, dispositivo y administración de grupo, con privilegios de administración de identidades, revisiones de Access, los términos de uso, protección de la identidad, la administración de contraseñas (SSPR y administración restablecimientos de contraseña ), Self service etcetera de administración de grupo...
ms.openlocfilehash: e607d866443a07f1405260b02a630276951ce310
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083027"
---
# <a name="list-directoryaudits"></a>Lista directoryAudits

Proporciona la lista de los registros de auditoría generados por Azure Active Directory. Incluye los registros de auditoría generados por los distintos servicios de Azure Active Directory como usuario, aplicación, dispositivo y administración de grupo, con privilegios de administración de identidades, revisiones de Access, los términos de uso, protección de la identidad, la administración de contraseñas (SSPR y administración restablecimientos de contraseña ), Self service etcetera de administración de grupo...

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
GET /auditLogs/directoryAudits
```
## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales
Este método admite los siguientes parámetros de consulta de OData a modo de ayuda para personalizar la respuesta. Compruebe [Los parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) para el uso de estos parámetros.

|Nombre     |Descripción                            |Ejemplo|
|:--------------------|----------------|------------------------------------------------------------------------|
|[$filter](/graph/query-parameters#filter-parameter)|Filtra los resultados (filas). |/`auditLogs/directoryAudits?&$filter=createdDateTime le 2018-01-24`
|[$top](/graph/query-parameters#top-parameter)|Establece el tamaño de la página de resultados.|`/auditLogs/directoryAudits?$top=1`|
|[$skiptoken](/graph/query-parameters#skiptoken-parameter)|Recupera que la siguiente página de resultados de resultado establece que abarcan varias páginas.|`auditLogs/directoryAudits?$skiptoken=01fa0e77c60c2d3d63226c8e3294c860__1`|

### <a name="list-of-attributes-supported-by-filter-parameter"></a>Lista de atributos admitidos por el parámetro $filter
|Nombre del atributo |Operadores admitidos|
|:----------------|:------|
|activityDisplayName| EQ, startswith|
|activityDateTime| EQ, ge, le|
|loggedByService|eq|
|initiatedBy/usuario/Id.|eq|
|displayName, initiatedBy/usuario| eq|
|usuario/initiatedBy/userPrincipalName| EQ, startswith|
|aplicación/initiatedBy/appId| eq|
|aplicación/initiatedBy/appDisplayName| eq|
|targetResources/any(t: t/id)| eq|
|targetResources/any(t:t/displayName)| EQ, startswith|
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre      |Descripción|
|:----------|:----------|
| Autorización  | Portador {código}|

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.
## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [directoryAudit](../resources/directoryaudit.md) en el cuerpo de la respuesta.
## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "get_directoryaudits"
}-->
```http
GET https://graph.microsoft.com/beta/auditLogs/directoryAudits
```
##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryAudit",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 271
```
```json
{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#auditLogs/directoryAudits
  "value": [{
        "id": "id",
        "category": "UserManagement",
        "correlationId": "da159bfb-54fa-4092-8a38-6e1fa7870e30",
        "result": "success",
        "resultReason": "Successfully added member to group",
        "activityDisplayName": "Add member to group",
        "activityDateTime": "2018-01-09T21:20:02.7215374Z",
        "loggedByService": "Core Directory",
        "initiatedBy": {
            "user": {
                "id": "7283X9ae-1a37-4937-9aex-e35d964db09b",
                "displayName": "Jamie Doe",
                "userPrincipalName": "jdoe@wingtiptoysonline.com",
                "ipAddress": "127.0.0.1"
            },
            "app": null
        },
        "targetResources": [{
            "@odata.type": "#microsoft.graph.TargetResourceGroup",
            "id": "ef7x527d-6x92-42x4-8x6d-cfxfdfx57f95",
            "displayName": "Lynda.com",
            "modifiedProperties": [{
                "displayName": "Action Client Name",
                "oldValue": null,
                "newValue": "DirectorySync"
            }],
            "groupType": "unifiedGroups"
        }, {
            "@odata.type": "#microsoft.graph.targetResourceUser",
            "id": "1f0ex8f5-3x61-4x6b-9x50-d4xx572f2bb7",
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

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List directoryAudits",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->