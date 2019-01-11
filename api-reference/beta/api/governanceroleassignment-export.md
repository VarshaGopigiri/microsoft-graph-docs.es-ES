---
title: Exportar governanceRoleAssignmentRequests
description: Recuperar una colección de governanceRoleAssignmentRequests en el formato `application/octet-stream`, que se puede analizar como un archivo .csv en el explorador.
localization_priority: Normal
ms.openlocfilehash: 10fd7c720bf7b6f162a4d8c2189e81a9205e53ff
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27828731"
---
# <a name="export-governanceroleassignmentrequests"></a>Exportar governanceRoleAssignmentRequests

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Recuperar una colección de [governanceRoleAssignmentRequests](../resources/governanceroleassignmentrequest.md) en el formato `application/octet-stream`, que se puede analizar como un archivo .csv en el explorador.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | PrivilegedAccess.ReadWrite.AzureResources  |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | PrivilegedAccess.ReadWrite.AzureResources |


## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->Exportar un conjunto de [governanceRoleAssignmentRequests](../resources/governanceroleassignmentrequest.md) en un recurso
    
>**Nota:** Además el ámbito de permiso, esta solicitud requiere que el solicitante puede tener al menos una asignación de funciones en el recurso. 
    
```http
GET /privilegedAccess/azureResources/roleAssignments/export?$filter=resourceId+eq+'{resourceId}'
```

Exportar un conjunto de [governanceRoleAssignmentRequests](../resources/governanceroleassignmentrequest.md) mío
```http
GET /privilegedAccess/azureResources/roleAssignments/export?$filter=subjectId+eq+'{myId}'
```
## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales
Este método es compatible con los [parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta.

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre      |Descripción|
|:----------|:----------|
| Autorización  | Portador {código}|

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `200 OK` código de respuesta y el contenido de tipo `application/octet-stream`.

## <a name="example"></a>Ejemplo
En este ejemplo se guarda todas las asignaciones de funciones como un archivo .csv en la suscripción Wingtip Toys - Prod. 

##### <a name="request"></a>Solicitud
```http
GET https://graph.microsoft.com/beta/privilegedAccess/azureResources/roleAssignments/export?filter=resourceId+eq+'85dfe48a-55d3-49fc-8f36-ee14b7f6f720'
```
##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. 
```http
HTTP/1.1 200 OK
Content-Type:application/octet-stream
Content-Length:126

77u/77u/QXNzaWdubWVudCBMZXZlbCxVc2VyIEdyb3VwIE5hbWUsUm9sZSBOYW1lLEVtYWlsLEFzc2lnbm1lbnQgVHlwZSxBc3NpZ25tZW43IFN0YXJ0IFRpbWUgKFVUQyksQXNzaWdubWVudCBFbmQgVGltZdAoVVRDKQ0K

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Export governanceRoleAssignmentRequests",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
