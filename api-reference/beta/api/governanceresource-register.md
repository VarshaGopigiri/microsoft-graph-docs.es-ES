---
title: Registrar governanceResource
description: Registrar un objeto governanceResource no administrado en PIM.
localization_priority: Normal
ms.openlocfilehash: ce439d53eb9f017340f561ca509e8da43dbafbfc
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27837754"
---
# <a name="register-governanceresource"></a>Registrar governanceResource

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Registrar un objeto no administrado [governanceResource](../resources/governanceresource.md) en la administración de identidades con privilegios.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

>**Nota:** Esta API también requiere que el solicitante tiene al menos una asignación de rol activo en el recurso.

|Tipo de permiso      | Permisos              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | PrivilegedAccess.ReadWrite.AzureResources  |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | PrivilegedAccess.ReadWrite.AzureResources |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /privilegedAccess/azureResources/resources/register
```

### <a name="optional-query-parameters"></a>Parámetros de consulta opcionales
Este método **sólo** es compatible con la `$select` y `$expand` de [parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta.

### <a name="request-headers"></a>Encabezados de solicitud
| Nombre      |Descripción|
|:----------|:----------|
| Autorización  | Portador {código}|
| Tipo de contenido  | application/json|

### <a name="request-body"></a>Cuerpo de la solicitud

|Parámetros      |Tipo                 |Obligatorio |Descripción|
|:-------------|:----------------------|:--------|:----------|
|externalId    |String                 |✓        |ExternalId del recurso para poder registrarlas en PIM.|

### <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `200 OK` respuesta.

### <a name="example"></a>Ejemplo
En este ejemplo se muestra cómo registrar una suscripción de Azure Wingtip Toys - Prod.
<!-- {
  "blockType": "request",
  "name": "get_governanceresource"
}-->
##### <a name="request"></a>Solicitud
```http
POST https://graph.microsoft.com/beta/privilegedAccess/azureResources/resources/register
```
##### <a name="response"></a>Respuesta
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.governanceResource"
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Register governanceResource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
