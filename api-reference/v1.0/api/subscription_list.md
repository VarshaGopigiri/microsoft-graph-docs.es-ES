# <a name="list-subscriptions"></a>Listar subscripciones

Recuperar las propiedades y relaciones de suscripciones de webhook, según el identificador de la aplicación, el usuario y el rol del usuario con un inquilino.

## <a name="permissions"></a>Permisos

Esta API admite los siguientes ámbitos de permisos; para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

| Tipo de permiso  | Permisos (de menos a más privilegiados)  |
|:---------------- |:-------------------------------------------- |
| [Delegado](../../../concepts/auth_v2_user.md) (cuenta profesional o educativa) | Rol necesario para [crear una suscripción](subscription_get.md) o para Subscriptions.Read.All (ver abajo). |
| [Delegado](../../../concepts/auth_v2_user.md) (cuenta personal de Microsoft) | Rol necesario para [crear una suscripción](./subscription_get.md) o para Subscriptions.Read.All (ver abajo). |
| [Aplicación](../../../concepts/auth_v2_service.md) | Función necesaria para [crear una suscripción](./subscription_get.md). |

Los resultados de la respuesta se basan en el contexto de la aplicación que hace la llamada. El siguiente es un resumen de las situaciones comunes:

### <a name="basic-scenarios"></a>Situaciones básicas

Normalmente, una aplicación desea recuperar las suscripciones que creó originalmente para el usuario que ha iniciado la sesión actual, o para todos los usuarios en el directorio (cuentas de trabajo o escuela). Estas situaciones no requieren ningún permiso especial más allá de los que la aplicación que se usó originalmente para crear sus suscripciones.

| Contexto de la aplicación que llama | La respuesta contiene |
|:-----|:---------------- |
| La aplicación llama en nombre del usuario que ha iniciado sesión (permiso delegado). <br/>-y-<br/>La aplicación tiene el permiso original necesario para [crear la suscripción](subscription_post_subscriptions.md).<br/><br/>Nota: Esto se aplica a las cuentas de Microsoft personales y las cuentas de trabajo o escuela. | Suscripciones creadas por **esta aplicación** solo para el usuario que ha iniciado sesión. |
| La aplicación llama en nombre propio (permiso de aplicación).<br/>-y-<br/>La aplicación tiene el permiso original necesario para [crear la suscripción](subscription_post_subscriptions.md).<br/><br/>Nota: Esto solo se aplica a cuentas de trabajo/escuela.| Suscripciones creadas por **esta aplicación** para sí misma o para cualquier usuario en el directorio.|

### <a name="advanced-scenarios"></a>Situaciones avanzadas

En algunos casos, una aplicación desea recuperar las suscripciones creadas por otras aplicaciones. Por ejemplo, un usuario desea ver todas las suscripciones creadas por cualquier aplicación en su nombre. O bien, puede que un administrador desee ver todas las suscripciones de todas las aplicaciones en su directorio.
Para estos escenarios, se requiere un permiso delegado Subscription.Read.All.

| Contexto de la aplicación que llama | La respuesta contiene |
|:-----|:---------------- |
| La aplicación llama en nombre del usuario que ha iniciado sesión (permiso delegado). *Si el usuario no es administrador*. <br/>-y-<br/>La aplicación tiene el permiso Subscription.Read.All<br/><br/>Nota: Esto se aplica a las cuentas de Microsoft personales y las cuentas de trabajo o escuela. | Suscripciones creadas por **cualquier aplicación** solo para el usuario que ha iniciado sesión. |
| La aplicación llama en nombre del usuario que ha iniciado sesión (permiso delegado). *El usuario es un administrador*.<br/>-y-<br/>La aplicación tiene el permiso Subscription.Read.All<br/><br/>Nota: Esto solo se aplica a cuentas de trabajo/escuela. | Suscripciones creadas por **cualquier aplicación** para **cualquier usuario** en el directorio.|

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
GET /subscriptions
```

## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales

Este método no es compatible con los [Parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) para ayudar a personalizar la respuesta.

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre       | Tipo | Descripción|
|:-----------|:------|:----------|
| Authorization  | cadena  | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud

No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una lista de objetos de [suscripción](../resources/subscription.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

##### <a name="request"></a>Solicitud

<!-- {
  "blockType": "request",
  "name": "get_subscriptions"
}-->

```http
GET https://graph.microsoft.com/v1.0/subscriptions
```

##### <a name="response"></a>Respuesta

Este es un ejemplo de la respuesta.  Tenga en cuenta que es posible que esté truncada por razones de brevedad.  Todas las propiedades admitidas adecuadas para la solicitud y el contexto de la llamada se devolverán de una llamada real.

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
  "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#subscriptions",
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

Cuando una solicitud devuelve varias páginas de datos, la respuesta incluye una propiedad `@odata.nextLink` que le ayudará a administrar los resultados.  Para obtener más información, vea [Paginación de datos de Microsoft Graph en su aplicación](../../../concepts/paging.md).
