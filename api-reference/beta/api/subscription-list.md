---
title: Suscripciones de lista
description: " Consulte los escenarios a continuación para obtener información detallada."
localization_priority: Normal
ms.openlocfilehash: 1b751b8632d82626e2ba87bf00a054b2be4f25f9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27876989"
---
# <a name="list-subscriptions"></a>Suscripciones de lista

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Recuperar una lista de las suscripciones de webhook. El contenido de la respuesta depende del contexto en el que está llamando la aplicación; Consulte los escenarios a continuación para obtener información detallada.

## <a name="permissions"></a>Permisos

Esta API admite los siguientes ámbitos de permisos; Para obtener más información, incluido cómo elegir permisos, vea [permisos](/graph/permissions-reference).

| Tipo de permiso  | Permisos (de menos a más privilegiados)  |
|:---------------- |:-------------------------------------------- |
| [Delegada](/graph/auth-v2-user) (cuenta de trabajo o escuela) | Permisos necesarios para [crear la suscripción](subscription-post-subscriptions.md) o Subscription.Read.All (vea a continuación). |
| [Delegada](/graph/auth-v2-user) (cuenta Microsoft personal) | Permisos necesarios para [crear la suscripción](subscription-post-subscriptions.md) o Subscription.Read.All (vea a continuación). |
| [Application](/graph/auth-v2-service) | Permisos necesarios para [crear la suscripción](subscription-post-subscriptions.md). |

Los resultados de la respuesta se basan en el contexto de la aplicación que llama. El siguiente es un resumen de los escenarios comunes:

### <a name="basic-scenarios"></a>Escenarios básicos

Con más frecuencia, una aplicación desea recuperar las suscripciones que creó originalmente para el usuario que ha iniciado la sesión actual, o para todos los usuarios en el directorio (las cuentas de trabajo o escuela). Estos escenarios no requieren ningún permiso especial más allá de los que la aplicación que se usó originalmente para crear sus suscripciones.

| Contexto de la aplicación que llama | Contiene la respuesta |
|:-----|:---------------- |
| Aplicación está llamando en nombre del usuario ha iniciado sesión (delegar permisos). <br/>- y -<br/>Aplicación tiene el permiso original necesario para [crear la suscripción](subscription-post-subscriptions.md).<br/><br/>Nota: Esto se aplica a las cuentas de Microsoft personal y las cuentas de trabajo o escuela. | Suscripciones creadas por **esta aplicación** para sólo el usuario ha iniciado sesión. |
| Aplicación está llamando en nombre propio (permiso a la aplicación).<br/>- y -<br/>Aplicación tiene el permiso original necesario para [crear la suscripción](subscription-post-subscriptions.md).<br/><br/>Nota: Esto se aplica sólo las cuentas de trabajo o escuela.| Suscripciones creadas por **esta aplicación** para sí o para cualquier usuario en el directorio.|

### <a name="advanced-scenarios"></a>Escenarios avanzados

En algunos casos, una aplicación desea recuperar las suscripciones creadas por otras aplicaciones. Por ejemplo, un usuario desea ver todas las suscripciones creadas por cualquier aplicación en su nombre. O bien, puede que un administrador desee ver todas las suscripciones de todas las aplicaciones en su directorio.
Para estos escenarios, se requiere un permiso delegado Subscription.Read.All.

| Contexto de la aplicación que llama | Contiene la respuesta |
|:-----|:---------------- |
| Aplicación está llamando en nombre del usuario ha iniciado sesión (delegar permisos). *El usuario es un usuario sin permisos de administrador*. <br/>- y -<br/>Aplicación tiene el permiso Subscription.Read.All<br/><br/>Nota: Esto se aplica a las cuentas de Microsoft personal y las cuentas de trabajo o escuela. | Suscripciones creadas por **cualquier aplicación** para sólo el usuario ha iniciado sesión. |
| Aplicación está llamando en nombre del usuario ha iniciado sesión (delegar permisos). *El usuario es un administrador*.<br/>- y -<br/>Aplicación tiene el permiso Subscription.Read.All<br/><br/>Nota: Esto se aplica sólo las cuentas de trabajo o escuela. | Suscripciones creadas por **cualquier aplicación** para **cualquier usuario** en el directorio.|

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
GET /subscriptions
```

## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales

Este método no es compatible con los [Parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) para ayudar a personalizar la respuesta.

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre       | Tipo | Descripción|
|:-----------|:------|:----------|
| Autorización  | string  | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud

No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una lista de objetos de [suscripción](../resources/subscription.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

##### <a name="request"></a>Solicitud

<!-- {
  "blockType": "request",
  "name": "get_subscriptions"
}-->

```http
GET https://graph.microsoft.com/beta/subscriptions
```

##### <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta. Nota: Es posible que se trunca la respuesta que se muestra aquí por razones de brevedad. Todas las propiedades se devolverán desde una llamada real.

<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.subscription",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 586

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#subscriptions",
  "value": [
    {
      "id": "0fc0d6db-0073-42e5-a186-853da75fb308",
      "resource": "Users",
      "applicationId": "24d3b144-21ae-4080-943f-7067b395b913",
      "changeType": "updated,deleted",
      "clientState": null,
      "notificationUrl": "https://webhookappexample.azurewebsites.net/api/notifications",
      "expirationDateTime": "2018-03-12T05:00:00Z",
      "creatorId": "8ee44408-0679-472c-bc2a-692812af3437"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List subscriptions",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

Cuando una solicitud devuelve varias páginas de datos, la respuesta incluye un `@odata.nextLink` (propiedad) que le ayudarán a administrar los resultados.  Para obtener más información, vea [datos de paginación Microsoft Graph en su aplicación](/graph/paging).
