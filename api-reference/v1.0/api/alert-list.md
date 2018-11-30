---
title: List alerts
description: Recuperar una lista de los objetos de alerta.
ms.openlocfilehash: c25784f62d37722fc997e57b9f15c9857133b964
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031365"
---
# <a name="list-alerts"></a>List alerts

Recuperar una lista de objetos de [alerta](../resources/alert.md) .

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) |  SecurityEvents.Read.All, SecurityEvents.ReadWrite.All  |
|Delegado (cuenta personal de Microsoft) |  No admitida.  |
|Aplicación | SecurityEvents.Read.All, SecurityEvents.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
GET /security/alerts
GET /security/alerts?$top=1
GET /security/alerts?$filter={property} eq '{property-value}'
GET /security/alerts?$filter={property} eq '{property-value}'&$top=5
GET /security/alerts?$filter={property} eq '{property-value}'&{property} eq '{property-value}'
```

## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales

Este método admite los siguientes [parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta:

- `$count`
- `$filter`
- `$orderby`
- `$select`
- `$skip`
- `$top`devolverá los primeros resultados agregados de cada proveedor de API de seguridad.  

Para devolver un conjunto de propiedades alternativo, utilice la OData `$select` parámetro para especificar el conjunto de propiedades de la **alerta** que desee de la consulta.  Por ejemplo, para devolver el **assignedTo**, **categoría**y propiedades de **gravedad** , agregue lo siguiente a la consulta: `$select=assignedTo,category,severity`.

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre      |Descripción|
|:----------|:----------|
| Authorization  | {código} del portador. Necesario.|

## <a name="request-body"></a>Cuerpo de la solicitud

No proporcione un cuerpo de solicitud para este método. Se pasará por alto el cuerpo de la solicitud.

## <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de **alerta** en el cuerpo de la respuesta. Si se devuelve un código de estado que no sea 2xx o 404 desde un proveedor o un proveedor de tiempo de espera, la respuesta será un `206 Partial Content` código de estado con la respuesta de proveedores en un encabezado de advertencia. Para obtener más información, vea [respuestas de error de la API de seguridad de Microsoft Graph](../resources/security-error-codes.md).

## <a name="example"></a>Ejemplo

### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "get_alerts"
}-->

```http
GET https://graph.microsoft.com/v1.0/security/alerts
```

### <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta.

>**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.alert",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "activityGroupName": "activityGroupName-value",
      "assignedTo": "assignedTo-value",
      "azureSubscriptionId": "azureSubscriptionId-value",
      "azureTenantId": "azureTenantId-value",
      "category": "category-value",
      "closedDateTime": "datetime-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List alerts",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
