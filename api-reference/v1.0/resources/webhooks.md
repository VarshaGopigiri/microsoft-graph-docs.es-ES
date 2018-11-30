# <a name="working-with-webhooks-in-microsoft-graph"></a><span data-ttu-id="9c9b0-101">Trabajar con webhooks en Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="9c9b0-101">Working with Webhooks in Microsoft Graph</span></span>

<span data-ttu-id="9c9b0-p101">La API de REST de Microsoft Graph utiliza un mecanismo webhook para entregar notificaciones a los clientes. Un cliente es un servicio web que configura su propia dirección URL para recibir notificaciones. Las aplicaciones cliente utilizan notificaciones para actualizar su estado cuando se producen cambios.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-p101">The Microsoft Graph REST API uses a webhook mechanism to deliver notifications to clients. A client is a web service that configures its own URL to receive notifications. Client apps use notifications to update their state upon changes.</span></span>

<span data-ttu-id="9c9b0-105">Mediante la API de REST de Microsoft Graph, una aplicación puede suscribirse a cambios en los siguientes recursos:</span><span class="sxs-lookup"><span data-stu-id="9c9b0-105">Using the Microsoft Graph REST API, an app can subscribe to changes on the following resources:</span></span>

* <span data-ttu-id="9c9b0-106">Mensajes</span><span class="sxs-lookup"><span data-stu-id="9c9b0-106">Messages</span></span>
* <span data-ttu-id="9c9b0-107">Eventos</span><span class="sxs-lookup"><span data-stu-id="9c9b0-107">Events</span></span>
* <span data-ttu-id="9c9b0-108">Contactos</span><span class="sxs-lookup"><span data-stu-id="9c9b0-108">Contacts</span></span>
* <span data-ttu-id="9c9b0-109">Conversaciones de grupo</span><span class="sxs-lookup"><span data-stu-id="9c9b0-109">Group conversations</span></span>
* <span data-ttu-id="9c9b0-110">Contenido compartido en OneDrive, incluidas las unidades de disco asociadas a sitios de SharePoint</span><span class="sxs-lookup"><span data-stu-id="9c9b0-110">Content shared on OneDrive including drives associated with SharePoint sites</span></span>
* <span data-ttu-id="9c9b0-111">Carpetas de OneDrive personales del usuario</span><span class="sxs-lookup"><span data-stu-id="9c9b0-111">User's personal OneDrive folders</span></span>

<span data-ttu-id="9c9b0-112">Por ejemplo, puede crear una suscripción a una carpeta específica: `me/mailfolders('inbox')/messages`</span><span class="sxs-lookup"><span data-stu-id="9c9b0-112">You can create a subscription to a specific folder: `me/mailfolders('inbox')/messages`</span></span>

<span data-ttu-id="9c9b0-113">O a un recurso de nivel superior: `me/messages`, `me/contacts`, `me/events`</span><span class="sxs-lookup"><span data-stu-id="9c9b0-113">Or to a top-level resource: `me/messages`</span></span>

<span data-ttu-id="9c9b0-114">O en una unidad de disco de SharePoint o de OneDrive para la Empresa: `/drive/root`</span><span class="sxs-lookup"><span data-stu-id="9c9b0-114">Or on a Sharepoint / OneDrive for Business drive: `/drive/root`</span></span>

<span data-ttu-id="9c9b0-115">O a una instancia de OneDrive personal del usuario: `/drives/{id}/root`
`/drives/{id}/root/subfolder`</span><span class="sxs-lookup"><span data-stu-id="9c9b0-115">Or on a user's personal OneDrive: `/drives/{id}/root`
`/drives/{id}/root/subfolder`</span></span>

<span data-ttu-id="9c9b0-p102">Microsoft Graph acepta la solicitud de suscripción y después manda las notificaciones a la dirección URL especificada en la suscripción. La aplicación actúa entonces según su lógica de negocios. Por ejemplo, recupera más datos, actualiza la caché y las vistas, etc.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-p102">After Microsoft Graph accepts the subscription request, it pushes notifications to the URL specified in the subscription. The app then takes action according to its business logic. For example, it fetches more data, updates cache and views, etc.</span></span>

<span data-ttu-id="9c9b0-p103">Las aplicaciones deben renovar sus suscripciones antes de que expiren. El plazo actual de expiración más largo es de tres días menos 90 minutos desde el momento de su creación. Las aplicaciones tienen que renovar sus suscripciones antes de la fecha de expiración. De lo contrario tendrán que crear otra suscripción.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-p103">Subscriptions expire. The current longest expiration time is three days minus 90 minutes (4230 in total) from the time of creation. Apps need to renew their subscriptions before the expiration time. Otherwise they'll need to create a new subscription.</span></span>

<span data-ttu-id="9c9b0-123">Las aplicaciones también pueden cancelar la suscripción en cualquier momento para dejar de recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-123">Apps should renew their subscriptions before they expire. They can also unsubscribe at any time to stop getting notifications.</span></span>

<span data-ttu-id="9c9b0-p104">En general, las operaciones de suscripción requieren permiso de lectura en el recurso. Por ejemplo, para obtener notificaciones en mensajes, la aplicación necesita el permiso `Mail.Read`. En el artículo sobre cómo [crear suscripciones](../api/subscription_post_subscriptions.md) se muestran los permisos necesarios para cada tipo de recurso. En la siguiente tabla aparecen los tipos de permisos que la aplicación puede solicitar para usar webhooks con tipos de recurso concretos.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-p104">In general, subscription operations require read permission to the resource. For example, to get notifications for messages, your app needs the `Mail.Read` permission. The [create subscription](../api/subscription_post_subscriptions.md) article lists permissions needed for each resource type. The following table lists the types of permissions your app can request to use webhooks for specific resource types.</span></span> 

| <span data-ttu-id="9c9b0-128">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9c9b0-128">Permission type</span></span> | <span data-ttu-id="9c9b0-129">Tipos de recursos admitidos en v1.0</span><span class="sxs-lookup"><span data-stu-id="9c9b0-129">Supported resource types in v1.0</span></span> |
|:----------------|:---------------------------------|
| <span data-ttu-id="9c9b0-130">Delegado: cuenta profesional o educativa</span><span class="sxs-lookup"><span data-stu-id="9c9b0-130">Delegated - work or school account</span></span> | [<span data-ttu-id="9c9b0-131">contacto](contact.md), [conversación](conversation.md), [unidad de disco](drive.md), [evento](event.md), [mensaje</span><span class="sxs-lookup"><span data-stu-id="9c9b0-131">contact](contact.md), [conversation](conversation.md), [drive](drive.md), [event](event.md), [message</span></span>](message.md) |
| <span data-ttu-id="9c9b0-132">Delegado: cuenta personal de Microsoft</span><span class="sxs-lookup"><span data-stu-id="9c9b0-132">Delegated - personal Microsoft account</span></span> | <span data-ttu-id="9c9b0-133">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9c9b0-133">None</span></span> |
| <span data-ttu-id="9c9b0-134">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9c9b0-134">Application</span></span> | [<span data-ttu-id="9c9b0-135">contacto](contact.md), [conversación](conversation.md), [evento](event.md), [mensaje</span><span class="sxs-lookup"><span data-stu-id="9c9b0-135">contact](contact.md), [conversation](conversation.md), [event](event.md), [message</span></span>](message.md) |

## <a name="code-samples"></a><span data-ttu-id="9c9b0-136">Ejemplos de código</span><span class="sxs-lookup"><span data-stu-id="9c9b0-136">Code samples</span></span>

<span data-ttu-id="9c9b0-137">Los siguientes ejemplos de código están disponibles en GitHub.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-137">The following samples are available on GitHub in the OneDrive organization.</span></span>

* [<span data-ttu-id="9c9b0-138">Ejemplo de webhooks de Microsoft Graph para Node.js</span><span class="sxs-lookup"><span data-stu-id="9c9b0-138">Microsoft Graph Webhooks Sample for Node.js</span></span>](https://github.com/OfficeDev/Microsoft-Graph-Nodejs-Webhooks)
* [<span data-ttu-id="9c9b0-139">Ejemplo de webhooks de Microsoft Graph para ASP.NET</span><span class="sxs-lookup"><span data-stu-id="9c9b0-139">Microsoft Graph Webhooks Sample for ASP.NET</span></span>](https://github.com/OfficeDev/Microsoft-Graph-ASPNET-Webhooks)

# <a name="creating-a-subscription"></a><span data-ttu-id="9c9b0-140">Crear una suscripción</span><span class="sxs-lookup"><span data-stu-id="9c9b0-140">Creating a subscription</span></span>

<span data-ttu-id="9c9b0-p105">La creación de una suscripción es el primer paso para empezar a recibir notificaciones de un recurso. El proceso de suscripción es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="9c9b0-p105">Creating a subscription is the first step to start receiving notifications for a resource. The subscription process is as follows:</span></span>

1. <span data-ttu-id="9c9b0-143">El cliente envía una solicitud de suscripción (POST) a un recurso específico.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-143">The client sends a subscription (POST) request for a specific resource.</span></span>
2. <span data-ttu-id="9c9b0-144">Microsoft Graph comprueba la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-144">Microsoft Graph verifies the request.</span></span>
  * <span data-ttu-id="9c9b0-145">Si la solicitud es válida, Microsoft Graph envía un token de validación a la dirección URL de notificación.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-145">If the request is valid, Microsoft Graph sends a validation token to the notification URL.</span></span>
  * <span data-ttu-id="9c9b0-146">Si la solicitud no es válida, Microsoft Graph envía una respuesta de error con el código y los detalles.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-146">If the request is invalid, Microsoft Graph sends an error response with code and details.</span></span>
3. <span data-ttu-id="9c9b0-147">El cliente envía el token de validación a Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-147">The client sends the validation token back to Microsoft Graph.</span></span>

<span data-ttu-id="9c9b0-148">El cliente debe almacenar el identificador de suscripción para establecer la correlación de una notificación con la suscripción correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-148">Client must store the subscription ID to correlate a notification with the corresponding subscription.</span></span>

## <a name="notification-url-validation"></a><span data-ttu-id="9c9b0-149">Validación de la dirección URL de notificación</span><span class="sxs-lookup"><span data-stu-id="9c9b0-149">Notification URL validation</span></span>

<span data-ttu-id="9c9b0-p106">Microsoft Graph valida la dirección URL de notificación en una solicitud de suscripción antes de crear la suscripción. El proceso de validación es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="9c9b0-p106">Microsoft Graph validates the notification URL in a subscription request before creating the subscription. The validation process occurs as follows:</span></span>

1. <span data-ttu-id="9c9b0-152">Microsoft Graph envía una solicitud POST a la dirección URL de notificación:</span><span class="sxs-lookup"><span data-stu-id="9c9b0-152">Microsoft Graph sends a POST request to the notification URL:</span></span>

  ```
  POST https://{notificationUrl}?validationToken={TokenDefinedByMicrosoftGraph}
  ClientState: {Data sent in ClientState value in subscription request (if any)}
  ```
 
2. <span data-ttu-id="9c9b0-153">El cliente debe proporcionar una respuesta con las siguientes características en menos de 10 segundos:</span><span class="sxs-lookup"><span data-stu-id="9c9b0-153">The client must provide a response with the following characteristics within 10 seconds:</span></span>

  * <span data-ttu-id="9c9b0-154">Un código de estado 200 (Correcto).</span><span class="sxs-lookup"><span data-stu-id="9c9b0-154">An 200 (OK) status code.</span></span>
  * <span data-ttu-id="9c9b0-155">El tipo de contenido debe ser texto/sin formato.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-155">The content type must be text/plain.</span></span> 
  * <span data-ttu-id="9c9b0-156">El cuerpo debe incluir el token de validación proporcionado por Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-156">The body must include the validation token provided by Microsoft Graph.</span></span>

<span data-ttu-id="9c9b0-157">El cliente debe descartar el token de validación después de proporcionarlo en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-157">The client should discard the validation token after providing it in the response.</span></span>

## <a name="subscription-request-example"></a><span data-ttu-id="9c9b0-158">Ejemplo de solicitud de suscripción</span><span class="sxs-lookup"><span data-stu-id="9c9b0-158">Subscription request example</span></span>

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

<span data-ttu-id="9c9b0-p107">Se necesitan las propiedades `changeType`, `notificationUrl`, `resource` y `expirationDateTime`. Vea las definiciones y los valores de las propiedades en [Tipo de recurso de suscripción](subscription.md). Aunque no se necesita la propiedad `clientState`, tiene que incluirla para cumplir nuestro proceso de control de notificaciones recomendado.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-p107">The `changeType`, `notificationUrl`, `resource`, and `expirationDateTime` properties are required. See [subscription resource type](subscription.md) for property definitions and values. Although `clientState` is not required, you must include it to comply with our recommended notification handling process.</span></span>

<span data-ttu-id="9c9b0-162">Si se ejecuta correctamente, Microsoft Graph devuelve un código `201 Created` y un objeto [subscription](subscription.md) en el cuerpo.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-162">If successful, Microsoft Graph returns a `201 Created` code and a [subscription](subscription.md) object in the body.</span></span>

# <a name="renewing-a-subscription"></a><span data-ttu-id="9c9b0-163">Renovación de una suscripción</span><span class="sxs-lookup"><span data-stu-id="9c9b0-163">Renewing a subscription</span></span>

<span data-ttu-id="9c9b0-p108">El cliente puede renovar una suscripción con una fecha de expiración específica de hasta tres días desde el momento de la solicitud. La propiedad expirationDateTime es necesaria.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-p108">The client can renew a subscription with a specific expiration date of up to three days from the time of request. The expirationDateTime property is required.</span></span>

## <a name="subscription-renewal-example"></a><span data-ttu-id="9c9b0-166">Ejemplo de renovación de suscripción</span><span class="sxs-lookup"><span data-stu-id="9c9b0-166">Subscription renewal example</span></span>

```
PATCH https://graph.microsoft.com/v1.0/subscriptions/{id};
Content-Type: application/json
{
  "expirationDateTime": "2016-03-22T11:00:00.0000000Z"
}
```

<span data-ttu-id="9c9b0-p109">Si se ejecuta correctamente, Microsoft Graph devuelve un código `200 OK` y un objeto [subscription](subscription.md) en el cuerpo. El objeto de suscripción incluye el nuevo valor de expirationDateTime.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-p109">If successful, Microsoft Graph returns a `200 OK` code and a [subscription](subscription.md) object in the body. The subscription object includes the new expirationDateTime value.</span></span> 

# <a name="deleting-a-subscription"></a><span data-ttu-id="9c9b0-169">Eliminación de una suscripción</span><span class="sxs-lookup"><span data-stu-id="9c9b0-169">Deleting a subscription</span></span>

<span data-ttu-id="9c9b0-170">El cliente puede dejar de recibir notificaciones al eliminar la suscripción con su identificador.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-170">The client can stop receiving notifications by deleting the subscription using its ID.</span></span>

```
DELETE https://graph.microsoft.com/v1.0/subscriptions/{id}
```

<span data-ttu-id="9c9b0-171">Si se ejecuta correctamente, Microsoft Graph devuelve un código `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-171">If successful, Microsoft Graph returns a `204 No Content` code.</span></span>

# <a name="notifications"></a><span data-ttu-id="9c9b0-172">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="9c9b0-172">Notifications</span></span>

<span data-ttu-id="9c9b0-p110">El cliente comienza a recibir notificaciones después de crear la suscripción. Microsoft Graph envía una solicitud POST a la dirección URL de notificación cuando se producen cambios en el recurso. El cliente solo recibe notificaciones según el tipo de cambio especificado, como *creado*.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-p110">The client starts receiving notifications after creating the subscription. Microsoft Graph sends a POST request to the notification URL when changes happen to the resource. The client only gets notifications according to the specified change type, such as *created*.</span></span>

## <a name="notification-properties"></a><span data-ttu-id="9c9b0-176">Propiedades de la notificación</span><span class="sxs-lookup"><span data-stu-id="9c9b0-176">Notification properties</span></span>

<span data-ttu-id="9c9b0-177">El objeto “notification” tiene las propiedades siguientes:</span><span class="sxs-lookup"><span data-stu-id="9c9b0-177">The notification object has the following properties:</span></span>

* <span data-ttu-id="9c9b0-178">subscriptionId: el id. de la suscripción a la que pertenece esta notificación.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-178">subscriptionId - The ID for the subscription to which this notification belongs.</span></span>
* <span data-ttu-id="9c9b0-179">subscriptionExpirationDateTime: la hora de expiración de la suscripción.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-179">subscriptionExpirationDateTime - The expiration time for the subscription.</span></span>
* <span data-ttu-id="9c9b0-180">clientState: la propiedad clientState especificada en la solicitud de suscripción.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-180">clientState - The clientState property specified in the subscription request.</span></span>
* <span data-ttu-id="9c9b0-p111">changeType - El tipo de evento que generó la notificación. Por ejemplo, *creado* al recibir un correo o *actualizado* al marcar un mensaje como leído.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-p111">changeType - The event type that caused the notification. For example, *created* on mail receive, or *updated* on marking a message read.</span></span>
* <span data-ttu-id="9c9b0-183">resource - El URI del recurso que hace referencia a `https://graph.microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-183">resource - The URI of the resource relative to `https://graph.microsoft.com`.</span></span> 
* <span data-ttu-id="9c9b0-p112">resourceData - El objeto que depende del recurso al que se suscribe.  Por ejemplo, para recursos de Outlook:</span><span class="sxs-lookup"><span data-stu-id="9c9b0-p112">resourceData - The object dependent on the resource being subscribed to.  For example, for Outlook resources:</span></span>
  * <span data-ttu-id="9c9b0-186">@odata.type - El tipo de entidad OData en Microsoft Graph que describe el objeto representado.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-186">@odata.type - The OData entity type in Microsoft Graph that describes the represented object.</span></span>
  * <span data-ttu-id="9c9b0-187">@odata.id - El identificador OData del objeto.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-187">@odata.id - The OData identifier of the object.</span></span>
  * <span data-ttu-id="9c9b0-188">@odata.etag: la etiqueta de entidad HTTP que representa una versión del objeto.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-188">@odata.etag - The HTTP entity tag that represents a version of the object.</span></span>
  * <span data-ttu-id="9c9b0-189">id: el identificador del objeto.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-189">id - The identifier of the object.</span></span>


> <span data-ttu-id="9c9b0-p113">Nota: El valor Id proporcionado en resourceData es válido en el momento en que se pone la notificación en cola. Algunas acciones, como mover un mensaje a otra carpeta, pueden provocar que cambie el Id de un recurso.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-p113">Note: The Id value provided in resourceData is valid at the time the notification was queued. Some actions, such as moving a message to another folder, may result in a resource's Id being changed.</span></span> 

## <a name="notification-example"></a><span data-ttu-id="9c9b0-192">Ejemplo de notificación</span><span class="sxs-lookup"><span data-stu-id="9c9b0-192">Notification example</span></span>

<span data-ttu-id="9c9b0-193">Cuando el usuario recibe un correo electrónico, Microsoft Graph envía una notificación como la siguiente:</span><span class="sxs-lookup"><span data-stu-id="9c9b0-193">When the user receives an email, Microsoft Graph sends a notification like the following:</span></span>

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

<span data-ttu-id="9c9b0-p114">Observe que el objeto de valor contiene una lista. Si hay muchas notificaciones en cola, Microsoft Graph las envía en una sola solicitud.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-p114">Note that the value object contains a list. If there are many queued notifications, Microsoft Graph sends them in a single request.</span></span>

## <a name="processing-the-notification"></a><span data-ttu-id="9c9b0-196">Procesar la notificación</span><span class="sxs-lookup"><span data-stu-id="9c9b0-196">Processing the notification</span></span>

<span data-ttu-id="9c9b0-p115">La aplicación comienza a recibir notificaciones y luego debe procesarlas. Estas son las tareas mínimas que debe realizar la aplicación para procesar una notificación:</span><span class="sxs-lookup"><span data-stu-id="9c9b0-p115">After your application starts receiving notifications it must process them. The following are the minimum tasks that your app must perform to process a notification:</span></span>

1. <span data-ttu-id="9c9b0-p116">Valide la propiedad `clientState`. La propiedad clientState en la notificación debe coincidir con la enviada con la solicitud de suscripción.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-p116">Validate the `clientState` property. The clientState property in the notification must match the one submitted with the subscription request.</span></span>
  > <span data-ttu-id="9c9b0-p117">Nota: Si no es así, no debe considerar la notificación como válida. También debe investigar de dónde proviene la notificación y tomar las medidas adecuadas.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-p117">Note: If this isn't true, you shouldn't consider this a valid notification. You should also investigate where the notification comes from and take appropriate action.</span></span>

2. <span data-ttu-id="9c9b0-203">Actualizar la aplicación según la lógica empresarial.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-203">Update your application based on your business logic.</span></span>
3. <span data-ttu-id="9c9b0-p118">Enviar un código de estado `202 - Accepted` en la respuesta a Microsoft Graph. Si Microsoft Graph no recibe un código de clase 2xx, intentará volver a enviar la notificación varias veces.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-p118">Send a `202 - Accepted` status code in your response to Microsoft Graph. If Microsoft Graph doesn't receive a 2xx class code, it will retry resending the notification a number of times.</span></span>
  > <span data-ttu-id="9c9b0-206">Debe enviar un código de estado `202 - Accepted`, incluso si la propiedad clientState no coincide con la enviada con la solicitud de suscripción.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-206">You should send a `202 - Accepted` status code even if the clientState property doesn't match the one submitted with the subscription request.</span></span>

<span data-ttu-id="9c9b0-207">Repetir en otras notificaciones de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-207">Repeat for other notifications in the request.</span></span>

# <a name="additional-resources"></a><span data-ttu-id="9c9b0-208">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="9c9b0-208">Additional resources</span></span>

* [<span data-ttu-id="9c9b0-209">Tipo de recurso de suscripción</span><span class="sxs-lookup"><span data-stu-id="9c9b0-209">Subscription resource type</span></span>](subscription.md)
* [<span data-ttu-id="9c9b0-210">Obtener suscripción</span><span class="sxs-lookup"><span data-stu-id="9c9b0-210">Get subscription</span></span>](../api/subscription_get.md)
* [<span data-ttu-id="9c9b0-211">Crear suscripción</span><span class="sxs-lookup"><span data-stu-id="9c9b0-211">Create subscription</span></span>](../api/subscription_post_subscriptions.md)
* [<span data-ttu-id="9c9b0-212">Ejemplo de webhooks de Microsoft Graph para Node.js</span><span class="sxs-lookup"><span data-stu-id="9c9b0-212">Microsoft Graph Webhooks Sample for Node.js</span></span>](https://github.com/OfficeDev/Microsoft-Graph-Nodejs-Webhooks)
* [<span data-ttu-id="9c9b0-213">Ejemplo de webhooks de Microsoft Graph para ASP.NET</span><span class="sxs-lookup"><span data-stu-id="9c9b0-213">Microsoft Graph Webhooks Sample for ASP.NET</span></span>](https://github.com/OfficeDev/Microsoft-Graph-ASPNET-Webhooks)
