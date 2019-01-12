---
title: Update alert
description: Actualizar una propiedad modificable **alerta** dentro de cualquier solución integrada para mantener sincronizados estado de la alerta y las asignaciones entre las soluciones. Este método actualiza cualquier solución que tiene un registro de la alerta de que se hace referencia a identificador.
localization_priority: Normal
author: preetikr
ms.prod: security
ms.openlocfilehash: 7b218daa56f7648bc888bbc0cd25619b22799325
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27966037"
---
# <a name="update-alert"></a>Update alert

Actualizar una propiedad modificable **alerta** dentro de cualquier solución integrada para mantener sincronizados estado de la alerta y las asignaciones entre las soluciones. Este método actualiza cualquier solución que tiene un registro de la alerta de que se hace referencia a identificador.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) |   SecurityEvents.ReadWrite.All  |
|Delegado (cuenta personal de Microsoft) |  No admitida.  |
|Aplicación | SecurityEvents.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP

> **Nota:** Debe incluir el identificador de **alerta** como un parámetro y vendorInformation que contiene el `provider` y `vendor` con este método.
<!-- { "blockType": "ignored" } -->

```http
PATCH /security/alerts/{alert_id}
```

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre       | Descripción|
|:-----------|:-----------|
| Autorización  | {código} del portador. Necesario.|
|Prefer | devolver = representación |

## <a name="request-body"></a>Cuerpo de la solicitud

En el cuerpo de la solicitud, proporcionar una representación JSON de los valores para los campos relevantes que deben actualizarse. El cuerpo **debe** contener el `vendorInformation` propiedad con válido `provider` y `vendor` campos. En la siguiente tabla se enumera los campos que se pueden actualizar para una alerta. Los valores para las propiedades existentes que no se incluyen en el cuerpo de la solicitud no cambiará. Para obtener el mejor rendimiento, no incluya valores existentes que no hayan cambiado.

| Propiedad   | Tipo |Descripción|
|:---------------|:--------|:----------|
|assignedTo|Cadena|Nombre del analista de la alerta se asigna a para la evaluación de errores, investigación o corrección.|
|closedDateTime|DateTimeOffset|Hora a la que se ha cerrado la alerta. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.|
|comments|Colección String|Comentarios de los analistas de la alerta (para la administración de alertas del cliente).|
|comentarios|alertFeedback|Comentarios de analistas de la alerta. Los valores posibles son: `unknown`, `truePositive`, `falsePositive` y `benignPositive`.|
|status|alertStatus|Estado de alerta del ciclo de vida (escenario). Los valores posibles son: `unknown`, `newAlert`, `inProgress` y `resolved`.|
|de cierre|Colección String|Rótulos definidos por el usuario que se pueden aplicar a una alerta y pueden servir como condiciones de filtro (por ejemplo, "HVA", "han visto).|
|vendorInformation |[securityVendorInformation](../resources/securityvendorinformation.md)|Tipo complejo que contiene detalles sobre el proveedor del producto o servicio de seguridad, el proveedor y la subprovider (por ejemplo, proveedor = Microsoft; proveedor = Windows Defender ATP; subProvider = AppLocker). **Proveedor y proveedor campos son obligatorios.**|

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.

Si se utiliza el encabezado de solicitud opcional, el método devuelve un `200 OK` código de respuesta y el objeto actualizado de [alerta](../resources/alert.md) en el cuerpo de la respuesta.

## <a name="example-1"></a>Ejemplo 1

### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "update_alert"
}-->

```http
PATCH https://graph.microsoft.com/v1.0/security/alerts/{alert_id}
Content-type: application/json

{
  "assignedTo": "String",
  "closedDateTime": "String (timestamp)",
  "comments": ["String"],
  "feedback": "@odata.type: microsoft.graph.alertFeedback",
  "status": "@odata.type: microsoft.graph.alertStatus",
  "tags": ["String"],
  "vendorInformation":
    {
      "provider": "String",
      "vendor": "String"
    }
}
```

### <a name="response"></a>Respuesta

El siguiente es un ejemplo de una respuesta correcta.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.alert"
} -->

```http
HTTP/1.1 204 No Content
```

## <a name="example-2"></a>Ejemplo 2

### <a name="request"></a>Solicitud

En el ejemplo siguiente se muestra una solicitud que incluye el `Prefer` encabezado de solicitud.

<!-- {
  "blockType": "request",
  "name": "update_alert"
}-->

```http
PATCH https://graph.microsoft.com/v1.0/security/alerts/{alert_id}
Content-type: application/json
Prefer: return=representation

{
  "assignedTo": "String",
  "closedDateTime": "String (timestamp)",
  "comments": ["String"],
  "feedback": "@odata.type: microsoft.graph.alertFeedback",
  "status": "@odata.type: microsoft.graph.alertStatus",
  "tags": ["String"],
  "vendorInformation":
    {
      "provider": "String",
      "vendor": "String"
    }
}
```

### <a name="response"></a>Respuesta

El siguiente es un ejemplo de la respuesta cuando la opcional `Prefer: return=representation` se utiliza el encabezado de la solicitud.

>**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.alert"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "activityGroupName": "activityGroupName-value",
  "assignedTo": "assignedTo-value",
  "azureSubscriptionId": "azureSubscriptionId-value",
  "azureTenantId": "azureTenantId-value",
  "category": "category-value",
  "closedDateTime": "datetime-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update alert",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
