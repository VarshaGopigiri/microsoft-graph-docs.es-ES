# <a name="working-with-webhooks-in-microsoft-graph"></a>Trabajar con webhooks en Microsoft Graph

La API de REST de Microsoft Graph utiliza un mecanismo webhook para entregar notificaciones a los clientes. Un cliente es un servicio web que configura su propia dirección URL para recibir notificaciones. Las aplicaciones cliente utilizan notificaciones para actualizar su estado cuando se producen cambios.

Mediante la API de REST de Microsoft Graph, una aplicación puede suscribirse a cambios en los siguientes recursos:

* Mensajes
* Eventos
* Contactos
* Conversaciones de grupo
* Contenido compartido en OneDrive, incluidas las unidades de disco asociadas a sitios de SharePoint
* Carpetas de OneDrive personales del usuario

Por ejemplo, puede crear una suscripción a una carpeta específica: `me/mailfolders('inbox')/messages`

O a un recurso de nivel superior: `me/messages`, `me/contacts`, `me/events`

O en una unidad de disco de SharePoint o de OneDrive para la Empresa: `/drive/root`

O a una instancia de OneDrive personal del usuario: `/drives/{id}/root`
`/drives/{id}/root/subfolder`

Microsoft Graph acepta la solicitud de suscripción y después manda las notificaciones a la dirección URL especificada en la suscripción. La aplicación actúa entonces según su lógica de negocios. Por ejemplo, recupera más datos, actualiza la caché y las vistas, etc.

Las aplicaciones deben renovar sus suscripciones antes de que expiren. El plazo actual de expiración más largo es de tres días menos 90 minutos desde el momento de su creación. Las aplicaciones tienen que renovar sus suscripciones antes de la fecha de expiración. De lo contrario tendrán que crear otra suscripción.

Las aplicaciones también pueden cancelar la suscripción en cualquier momento para dejar de recibir notificaciones.

En general, las operaciones de suscripción requieren permiso de lectura en el recurso. Por ejemplo, para obtener notificaciones en mensajes, la aplicación necesita el permiso `Mail.Read`. En el artículo sobre cómo [crear suscripciones](../api/subscription_post_subscriptions.md) se muestran los permisos necesarios para cada tipo de recurso. En la siguiente tabla aparecen los tipos de permisos que la aplicación puede solicitar para usar webhooks con tipos de recurso concretos. 

| Tipo de permiso | Tipos de recursos admitidos en v1.0 |
|:----------------|:---------------------------------|
| Delegado: cuenta profesional o educativa | [contacto](contact.md), [conversación](conversation.md), [unidad de disco](drive.md), [evento](event.md), [mensaje](message.md) |
| Delegado: cuenta personal de Microsoft | Ninguno |
| Aplicación | [contacto](contact.md), [conversación](conversation.md), [evento](event.md), [mensaje](message.md) |

## <a name="code-samples"></a>Ejemplos de código

Los siguientes ejemplos de código están disponibles en GitHub.

* [Ejemplo de webhooks de Microsoft Graph para Node.js](https://github.com/OfficeDev/Microsoft-Graph-Nodejs-Webhooks)
* [Ejemplo de webhooks de Microsoft Graph para ASP.NET](https://github.com/OfficeDev/Microsoft-Graph-ASPNET-Webhooks)

# <a name="creating-a-subscription"></a>Crear una suscripción

La creación de una suscripción es el primer paso para empezar a recibir notificaciones de un recurso. El proceso de suscripción es el siguiente:

1. El cliente envía una solicitud de suscripción (POST) a un recurso específico.
2. Microsoft Graph comprueba la solicitud.
  * Si la solicitud es válida, Microsoft Graph envía un token de validación a la dirección URL de notificación.
  * Si la solicitud no es válida, Microsoft Graph envía una respuesta de error con el código y los detalles.
3. El cliente envía el token de validación a Microsoft Graph.

El cliente debe almacenar el identificador de suscripción para establecer la correlación de una notificación con la suscripción correspondiente.

## <a name="notification-url-validation"></a>Validación de la dirección URL de notificación

Microsoft Graph valida la dirección URL de notificación en una solicitud de suscripción antes de crear la suscripción. El proceso de validación es el siguiente:

1. Microsoft Graph envía una solicitud POST a la dirección URL de notificación:

  ```
  POST https://{notificationUrl}?validationToken={TokenDefinedByMicrosoftGraph}
  ClientState: {Data sent in ClientState value in subscription request (if any)}
  ```
 
2. El cliente debe proporcionar una respuesta con las siguientes características en menos de 10 segundos:

  * Un código de estado 200 (Correcto).
  * El tipo de contenido debe ser texto/sin formato. 
  * El cuerpo debe incluir el token de validación proporcionado por Microsoft Graph.

El cliente debe descartar el token de validación después de proporcionarlo en la respuesta.

## <a name="subscription-request-example"></a>Ejemplo de solicitud de suscripción

```
POST https://graph.microsoft.com/v1.0/subscriptions
Content-Type: application/json
{
  "changeType": "created,updated",
  "notificationUrl": "https://webhook.azurewebsites.net/notificationClient",
  "resource": "/me/mailfolders('inbox')/messages",
  "expirationDateTime": "2016-03-20T11:00:00.0000000Z",
  "clientState": "SecretClientState"
}
```

Se necesitan las propiedades `changeType`, `notificationUrl`, `resource` y `expirationDateTime`. Vea las definiciones y los valores de las propiedades en [Tipo de recurso de suscripción](subscription.md). Aunque no se necesita la propiedad `clientState`, tiene que incluirla para cumplir nuestro proceso de control de notificaciones recomendado.

Si se ejecuta correctamente, Microsoft Graph devuelve un código `201 Created` y un objeto [subscription](subscription.md) en el cuerpo.

# <a name="renewing-a-subscription"></a>Renovación de una suscripción

El cliente puede renovar una suscripción con una fecha de expiración específica de hasta tres días desde el momento de la solicitud. La propiedad expirationDateTime es necesaria.

## <a name="subscription-renewal-example"></a>Ejemplo de renovación de suscripción

```
PATCH https://graph.microsoft.com/v1.0/subscriptions/{id};
Content-Type: application/json
{
  "expirationDateTime": "2016-03-22T11:00:00.0000000Z"
}
```

Si se ejecuta correctamente, Microsoft Graph devuelve un código `200 OK` y un objeto [subscription](subscription.md) en el cuerpo. El objeto de suscripción incluye el nuevo valor de expirationDateTime. 

# <a name="deleting-a-subscription"></a>Eliminación de una suscripción

El cliente puede dejar de recibir notificaciones al eliminar la suscripción con su identificador.

```
DELETE https://graph.microsoft.com/v1.0/subscriptions/{id}
```

Si se ejecuta correctamente, Microsoft Graph devuelve un código `204 No Content`.

# <a name="notifications"></a>Notificaciones

El cliente comienza a recibir notificaciones después de crear la suscripción. Microsoft Graph envía una solicitud POST a la dirección URL de notificación cuando se producen cambios en el recurso. El cliente solo recibe notificaciones según el tipo de cambio especificado, como *creado*.

## <a name="notification-properties"></a>Propiedades de la notificación

El objeto “notification” tiene las propiedades siguientes:

* subscriptionId: el id. de la suscripción a la que pertenece esta notificación.
* subscriptionExpirationDateTime: la hora de expiración de la suscripción.
* clientState: la propiedad clientState especificada en la solicitud de suscripción.
* changeType - El tipo de evento que generó la notificación. Por ejemplo, *creado* al recibir un correo o *actualizado* al marcar un mensaje como leído.
* resource - El URI del recurso que hace referencia a `https://graph.microsoft.com`. 
* resourceData - El objeto que depende del recurso al que se suscribe.  Por ejemplo, para recursos de Outlook:
  * @odata.type - El tipo de entidad OData en Microsoft Graph que describe el objeto representado.
  * @odata.id - El identificador OData del objeto.
  * @odata.etag: la etiqueta de entidad HTTP que representa una versión del objeto.
  * id: el identificador del objeto.


> Nota: El valor Id proporcionado en resourceData es válido en el momento en que se pone la notificación en cola. Algunas acciones, como mover un mensaje a otra carpeta, pueden provocar que cambie el Id de un recurso. 

## <a name="notification-example"></a>Ejemplo de notificación

Cuando el usuario recibe un correo electrónico, Microsoft Graph envía una notificación como la siguiente:

```
{
  "value":[
  {
    "subscriptionId":"<subscription_guid>",
    "subscriptionExpirationDateTime":"2016-03-19T22:11:09.952Z",
    "clientState":"SecretClientState",
    "changeType":"Created",
    "resource":"Users/{user_guid}@<tenant_guid>/Messages/{long_id_string}",
    "resourceData":
    {
      "@odata.type":"#Microsoft.Graph.Message",
      "@odata.id":"Users/{user_guid}@<tenant_guid>/Messages/{long_id_string}",
      "@odata.etag":"W/\"CQAAABYAAADkrWGo7bouTKlsgTZMr9KwAAAUWRHf\"",
      "id":"<long_id_string>"
    }
  }
  ]
}
```

Observe que el objeto de valor contiene una lista. Si hay muchas notificaciones en cola, Microsoft Graph las envía en una sola solicitud.

## <a name="processing-the-notification"></a>Procesar la notificación

La aplicación comienza a recibir notificaciones y luego debe procesarlas. Estas son las tareas mínimas que debe realizar la aplicación para procesar una notificación:

1. Valide la propiedad `clientState`. La propiedad clientState en la notificación debe coincidir con la enviada con la solicitud de suscripción.
  > Nota: Si no es así, no debe considerar la notificación como válida. También debe investigar de dónde proviene la notificación y tomar las medidas adecuadas.

2. Actualizar la aplicación según la lógica empresarial.
3. Enviar un código de estado `202 - Accepted` en la respuesta a Microsoft Graph. Si Microsoft Graph no recibe un código de clase 2xx, intentará volver a enviar la notificación varias veces.
  > Debe enviar un código de estado `202 - Accepted`, incluso si la propiedad clientState no coincide con la enviada con la solicitud de suscripción.

Repetir en otras notificaciones de la solicitud.

# <a name="additional-resources"></a>Recursos adicionales

* [Tipo de recurso de suscripción](subscription.md)
* [Obtener suscripción](../api/subscription_get.md)
* [Crear suscripción](../api/subscription_post_subscriptions.md)
* [Ejemplo de webhooks de Microsoft Graph para Node.js](https://github.com/OfficeDev/Microsoft-Graph-Nodejs-Webhooks)
* [Ejemplo de webhooks de Microsoft Graph para ASP.NET](https://github.com/OfficeDev/Microsoft-Graph-ASPNET-Webhooks)
