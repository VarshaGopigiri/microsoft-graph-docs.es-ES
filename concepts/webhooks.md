---
title: Configurar las notificaciones de cambios en los datos de usuario
description: La API de Microsoft Graph utiliza un mecanismo webhook para entregar notificaciones a los clientes. Un cliente es un servicio web que configura su propia dirección URL para recibir notificaciones. Las aplicaciones cliente utilizan notificaciones para actualizar su estado cuando se producen cambios.
ms.openlocfilehash: faaa1be8330118f1cbebf5362903f0e114816b67
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092928"
---
# <a name="set-up-notifications-for-changes-in-user-data"></a>Configurar las notificaciones de cambios en los datos de usuario

La API de Microsoft Graph utiliza un mecanismo webhook para entregar notificaciones a los clientes. Un cliente es un servicio web que configura su propia dirección URL para recibir notificaciones. Las aplicaciones cliente utilizan notificaciones para actualizar su estado cuando se producen cambios.

Microsoft Graph acepta la solicitud de suscripción y después envía las notificaciones a la dirección URL especificada en la suscripción. La aplicación actúa entonces según su lógica de negocios. Por ejemplo, captura más datos, actualiza la caché y las vistas, etc.

## <a name="supported-resources"></a>Recursos admitidos

Mediante la API de Microsoft Graph, una aplicación puede suscribirse a cambios en los siguientes recursos:

- Mensajes
- Eventos
- Contacts
- Usuarios
- Grupos
- Conversaciones de grupo
- Contenido compartido en OneDrive, incluidas las unidades de disco asociadas a sitios de SharePoint
- Carpetas de OneDrive personales del usuario
- Alertas de seguridad

Por ejemplo, puede crear una suscripción a una carpeta de correo específica: `me/mailFolders('inbox')/messages`

O a un recurso de nivel superior: `me/messages`, `me/contacts`, `me/events`, `users` o `groups`

O a una instancia de recurso específica: `users/{id}`, `groups/{id}`, `groups/{id}/conversations`

O a una unidad de disco de SharePoint o de OneDrive para la Empresa: `/drive/root`

O a una instancia de OneDrive personal del usuario: `/drives/{id}/root`
`/drives/{id}/root/subfolder`

O a una nueva [alerta de API de seguridad](security-concept-overview.md): `/security/alerts?$filter=status eq ‘New’`, `/security/alerts?$filter=vendorInformation/provider eq ‘ASC’`

### <a name="azure-ad-resource-limitations"></a>Limitaciones de los recursos de Azure AD

Se aplican ciertos límites a los recursos basados en Azure AD (usuarios y grupos), y es posible que se generen algunos errores si se supera lo siguiente:

- Cuotas de suscripción permitidas:

  - Por aplicación: 50 000 suscripciones en total
  - Por espacio empresarial: 35 suscripciones en total en todas las aplicaciones
  - Por aplicación y espacio empresarial: 7 suscripciones en total

- No se admiten los espacios empresariales de Azure AD B2C.

- No se admiten notificaciones de entidades de usuario en cuentas Microsoft personales.

## <a name="subscription-lifetime"></a>Duración de la suscripción

Las suscripciones tienen una duración limitada. Las aplicaciones tienen que renovar sus suscripciones antes de la fecha de expiración. De lo contrario tendrán que crear otra suscripción. Para obtener una lista de las fechas de expiración máximas, consulte [Duración máxima de la suscripción por tipo de recurso](/graph/api/resources/subscription?view=graph-rest-1.0#maximum-length-of-subscription-per-resource-type).

Las aplicaciones también pueden cancelar la suscripción en cualquier momento para dejar de recibir notificaciones.

## <a name="managing-subscriptions"></a>Administrar suscripciones

Los clientes pueden crear suscripciones, renovar suscripciones y eliminar suscripciones.

### <a name="creating-a-subscription"></a>Crear una suscripción

La creación de una suscripción es el primer paso para empezar a recibir notificaciones de un recurso. El proceso de suscripción es el siguiente:

1. El cliente envía una solicitud de suscripción (POST) a un recurso específico.

1. Microsoft Graph comprueba la solicitud.

    - Si la solicitud es válida, Microsoft Graph envía un token de validación a la dirección URL de notificación.
    - Si la solicitud no es válida, Microsoft Graph envía una respuesta de error con el código y los detalles.

1. El cliente envía el token de validación a Microsoft Graph.

1. Microsoft Graph envía una respuesta al cliente.

El cliente debe almacenar el identificador de suscripción para establecer la correlación de las notificaciones con la suscripción.

#### <a name="subscription-request-example"></a>Ejemplo de solicitud de suscripción

```http
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

Se necesitan las propiedades `changeType`, `notificationUrl`, `resource` y `expirationDateTime`. Vea las definiciones y los valores de las propiedades en [Tipo de recurso de suscripción](/graph/api/resources/subscription?view=graph-rest-1.0).

Aunque `clientState` no se necesita, tiene que incluirse para cumplir nuestro proceso de control de notificaciones recomendado. El establecimiento de esta propiedad le permitirá confirmar que las notificaciones que recibe proceden del servicio de Microsoft Graph. Por eso, el valor de la propiedad debe permanecer secreto y ser conocido solo por la aplicación y el servicio de Microsoft Graph.

Si se ejecuta correctamente, Microsoft Graph muestra un código `201 Created` y un objeto [subscription](/graph/api/resources/subscription?view=graph-rest-1.0) en el cuerpo.

#### <a name="notification-endpoint-validation"></a>Validación de extremo de notificación

Microsoft Graph valida el extremo de notificación indicado en la propiedad `notificationUrl` de la solicitud de suscripción antes de crear la suscripción. El proceso de validación es el siguiente:

1. Microsoft Graph envía una solicitud POST a la dirección URL de notificación:

    ``` http
    POST https://{notificationUrl}?validationToken={opaqueTokenCreatedByMicrosoftGraph}
    ```

    > **Importante:** Como el `validationToken` es un parámetro de consulta, el cliente debe descodificarlo correctamente, según las prácticas de codificación de HTTP. Si el cliente no descodifica el token y usa en su lugar el valor codificado en el paso siguiente (respuesta), se producirá un error de validación. Además, el cliente debe tratar el valor de token como opaco, ya que el formato de token puede cambiar en el futuro, sin aviso.

1. El cliente debe proporcionar una respuesta con las siguientes características en menos de 10 segundos:

    - Un código de estado 200 (Correcto).
    - El tipo de contenido debe ser `text/plain`.
    - El cuerpo debe incluir el token de validación proporcionado por Microsoft Graph.

El cliente debe descartar el token de validación después de incluirlo en la respuesta.

### <a name="renewing-a-subscription"></a>Renovar una suscripción

El cliente puede renovar una suscripción con una fecha de expiración específica de hasta tres días desde el momento de la solicitud. La propiedad `expirationDateTime` es obligatoria.

#### <a name="subscription-renewal-example"></a>Ejemplo de renovación de la suscripción

```http
PATCH https://graph.microsoft.com/v1.0/subscriptions/{id}
Content-Type: application/json

{
  "expirationDateTime": "2016-03-22T11:00:00.0000000Z"
}
```

Si se ejecuta correctamente, Microsoft Graph muestra un código `200 OK` y un objeto [subscription](/graph/api/resources/subscription?view=graph-rest-1.0) en el cuerpo. El objeto "suscription" incluye el nuevo valor de `expirationDateTime`.

### <a name="deleting-a-subscription"></a>Eliminar una suscripción

El cliente puede dejar de recibir notificaciones al eliminar la suscripción con su identificador.

```http
DELETE https://graph.microsoft.com/v1.0/subscriptions/{id}
```

Si se ejecuta correctamente, Microsoft Graph devuelve un código `204 No Content`.

## <a name="notifications"></a>Notificaciones

El cliente comienza a recibir notificaciones después de crear la suscripción. Microsoft Graph envía una solicitud POST a la dirección URL de notificación cuando cambia el recurso. Las notificaciones solo se envían para los cambios del tipo especificado en la suscripción, por ejemplo, `created`.

> **Nota:** Cuando se utilizan varias suscripciones que supervisan el mismo tipo de recurso y usan la misma dirección URL de notificación, se puede enviar una solicitud POST que contenga varias notificaciones con distintos identificadores de suscripción. No hay ninguna garantía de que todas las notificaciones de la solicitud POST pertenezcan a una única suscripción.

### <a name="notification-properties"></a>Propiedades de la notificación

El objeto "notification" tiene las propiedades siguientes:

| Propiedad | Tipo | Descripción |
|:---------|:-----|:------------|
| subscriptionId | string | Identificador de la suscripción que generó la notificación. |
| subscriptionExpirationDateTime | [dateTime](https://tools.ietf.org/html/rfc3339) | Fecha de expiración de la suscripción. |
| clientState | string | Propiedad `clientState` especificada en la solicitud de suscripción (en su caso). |
| changeType | string | Tipo de evento que generó la notificación. Por ejemplo, `created` al recibir un correo o `updated` al marcar un mensaje como leído. |
| resource | string | URI del recurso relativo a `https://graph.microsoft.com`. |
| resourceData | object | El contenido de esta propiedad depende del tipo de recurso al que se suscriba. |

Por ejemplo, para recursos de Outlook, `resourceData` contiene los siguientes campos:

| Propiedad | Tipo | Descripción |
|:---------|:-----|:------------|
| @odata.type | string | Tipo de entidad OData en Microsoft Graph que describe el objeto representado. |
| @odata.id | string | Identificador OData del objeto. |
| @odata.etag | string | Etiqueta de entidad HTTP que representa una versión del objeto. |
| id | string | Identificador del objeto. |

> **Nota:** El valor `id` proporcionado en `resourceData` es válido en el momento en que se genera la notificación. Algunas acciones, como mover un mensaje a otra carpeta, pueden dar lugar a que el `id` ya no sea válido cuando se procese la notificación.

### <a name="notification-example"></a>Ejemplo de notificación

Cuando el usuario recibe un correo electrónico, Microsoft Graph envía una notificación como la siguiente:

```json
{
  "value": [
    {
      "subscriptionId":"<subscription_guid>",
      "subscriptionExpirationDateTime":"2016-03-19T22:11:09.952Z",
      "clientState":"secretClientValue",
      "changeType":"created",
      "resource":"users/{user_guid}@<tenant_guid>/messages/{long_id_string}",
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

Tenga en cuenta que el campo `value` es una matriz de objetos. Si hay muchas notificaciones en cola, puede que Microsoft Graph envíe varios elementos en una sola solicitud. Pueden incluirse notificaciones de distintas suscripciones en una misma solicitud de notificación.

### <a name="processing-the-notification"></a>Procesar la notificación

Cada notificación que reciba la aplicación debe procesarse. Estas son las tareas mínimas que debe realizar la aplicación para procesar una notificación:

1. Validar la propiedad `clientState`. Debe coincidir con el valor enviado originalmente con la solicitud de creación de suscripción.

    > **Nota:** Si no es así, no debe considerar la notificación como válida. Es posible que la notificación no se haya originado en Microsoft Graph y que haya sido enviada por un actor no autorizado. También debe investigar de dónde proviene la notificación y tomar las medidas adecuadas.

1. Actualizar la aplicación según la lógica empresarial.

1. Enviar un código de estado `202 - Accepted` en la respuesta a Microsoft Graph. Si Microsoft Graph no recibe un código de clase 2xx, intentará volver a enviar la notificación varias veces.

    > **Nota:** Debe enviar un código de estado `202 - Accepted`, aunque la propiedad `clientState` no coincida con la enviada en la solicitud de suscripción. Esto es recomendable, ya que evita que un posible actor no autorizado descubra que tal vez usted no confíe en sus notificaciones y usar esta información para adivinar el valor de la propiedad `clientState`.

Repita esto para otras notificaciones de la solicitud.

## <a name="code-samples"></a>Ejemplos de código

Los siguientes ejemplos de código están disponibles en GitHub.

- [Ejemplo de webhooks de Microsoft Graph para Node.js](https://github.com/OfficeDev/Microsoft-Graph-Nodejs-Webhooks)
- [Ejemplo de webhooks de Microsoft Graph para ASP.NET](https://github.com/OfficeDev/Microsoft-Graph-ASPNET-Webhooks)
- [Ejemplo de webhooks de usuario de Microsoft Graph con WebJobs SDK](https://github.com/microsoftgraph/webjobs-webhooks-sample)

## <a name="see-also"></a>Recursos adicionales

- [Tipo de recurso de suscripción](/graph/api/resources/subscription?view=graph-rest-1.0)
- [Obtener suscripción](/graph/api/subscription-get?view=graph-rest-1.0)
- [Crear suscripción](/graph/api/subscription-post-subscriptions?view=graph-rest-1.0)

[contact]: /graph/api/resources/contact?view=graph-rest-1.0
[conversation]: /graph/api/resources/conversation?view=graph-rest-1.0
[drive]: /graph/api/resources/drive?view=graph-rest-1.0
[event]: /graph/api/resources/event?view=graph-rest-1.0
[message]: /graph/api/resources/message?view=graph-rest-1.0
