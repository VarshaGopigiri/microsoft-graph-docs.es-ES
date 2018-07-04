# <a name="set-up-notifications-for-changes-in-user-data"></a><span data-ttu-id="63b67-101">Configurar las notificaciones de cambios en los datos de usuario</span><span class="sxs-lookup"><span data-stu-id="63b67-101">Set up notifications for changes in user data</span></span>

<span data-ttu-id="63b67-p101">La API de Microsoft Graph utiliza un mecanismo webhook para entregar notificaciones a los clientes. Un cliente es un servicio web que configura su propia dirección URL para recibir notificaciones. Las aplicaciones cliente utilizan notificaciones para actualizar su estado cuando se producen cambios.</span><span class="sxs-lookup"><span data-stu-id="63b67-p101">The Microsoft Graph REST API uses a webhook mechanism to deliver notifications to clients. A client is a web service that configures its own URL to receive notifications. Client apps use notifications to update their state upon changes.</span></span>

<span data-ttu-id="63b67-105">Microsoft Graph acepta la solicitud de suscripción y después envía las notificaciones a la dirección URL especificada en la suscripción.</span><span class="sxs-lookup"><span data-stu-id="63b67-105">After Microsoft Graph accepts the subscription request, it pushes notifications to the URL specified in the subscription. The app then takes action according to its business logic. For example, it fetches more data, updates cache and views, etc.</span></span> <span data-ttu-id="63b67-106">La aplicación actúa entonces según su lógica de negocios.</span><span class="sxs-lookup"><span data-stu-id="63b67-106">The app then takes action according to its business logic.</span></span> <span data-ttu-id="63b67-107">Por ejemplo, captura más datos, actualiza la caché y las vistas, etc.</span><span class="sxs-lookup"><span data-stu-id="63b67-107">For example, it fetches more data, updates its cache and views, etc.</span></span>

## <a name="supported-resources"></a><span data-ttu-id="63b67-108">Recursos admitidos</span><span class="sxs-lookup"><span data-stu-id="63b67-108">Supported resources</span></span>

<span data-ttu-id="63b67-109">Mediante la API de Microsoft Graph, una aplicación puede suscribirse a cambios en los siguientes recursos:</span><span class="sxs-lookup"><span data-stu-id="63b67-109">Using the Microsoft Graph REST API, an app can subscribe to changes on the following resources:</span></span>

- <span data-ttu-id="63b67-110">Mensajes</span><span class="sxs-lookup"><span data-stu-id="63b67-110">Messages</span></span>
- <span data-ttu-id="63b67-111">Eventos</span><span class="sxs-lookup"><span data-stu-id="63b67-111">Events</span></span>
- <span data-ttu-id="63b67-112">Contacts</span><span class="sxs-lookup"><span data-stu-id="63b67-112">Contacts</span></span>
- <span data-ttu-id="63b67-113">Usuarios</span><span class="sxs-lookup"><span data-stu-id="63b67-113">Users</span></span>
- <span data-ttu-id="63b67-114">Grupos</span><span class="sxs-lookup"><span data-stu-id="63b67-114">Groups</span></span>
- <span data-ttu-id="63b67-115">Conversaciones de grupo</span><span class="sxs-lookup"><span data-stu-id="63b67-115">Group conversations</span></span>
- <span data-ttu-id="63b67-116">Contenido compartido en OneDrive, incluidas las unidades de disco asociadas a sitios de SharePoint</span><span class="sxs-lookup"><span data-stu-id="63b67-116">Content shared on OneDrive including drives associated with SharePoint sites</span></span>
- <span data-ttu-id="63b67-117">Carpetas de OneDrive personales del usuario</span><span class="sxs-lookup"><span data-stu-id="63b67-117">User's personal OneDrive folders</span></span>

<span data-ttu-id="63b67-118">Por ejemplo, puede crear una suscripción a una carpeta de correo específica: `me/mailFolders('inbox')/messages`</span><span class="sxs-lookup"><span data-stu-id="63b67-118">For instance, you can create a subscription to a specific folder: `me/mailFolders('inbox')/messages`</span></span>

<span data-ttu-id="63b67-119">O a un recurso de nivel superior: `me/messages`, `me/contacts`, `me/events`, `users` o `groups`</span><span class="sxs-lookup"><span data-stu-id="63b67-119">Or to a top-level resource: `me/messages`, `me/contacts`, `me/events`, `users`, or `groups`</span></span>

<span data-ttu-id="63b67-120">O a una instancia de recurso específica: `users/{id}`, `groups/{id}`, `groups/{id}/conversations`</span><span class="sxs-lookup"><span data-stu-id="63b67-120">Or to a specific resource instance: `users/{id}`, `groups/{id}`, `groups/{id}/conversations`</span></span>

<span data-ttu-id="63b67-121">O a una unidad de disco de SharePoint o de OneDrive para la Empresa: `/drive/root`</span><span class="sxs-lookup"><span data-stu-id="63b67-121">Or to a SharePoint/OneDrive for Business drive: `/drive/root`</span></span>

<span data-ttu-id="63b67-122">O a una instancia de OneDrive personal del usuario: `/drives/{id}/root`
`/drives/{id}/root/subfolder`</span><span class="sxs-lookup"><span data-stu-id="63b67-122">Or on a user's personal OneDrive: `/drives/{id}/root`
`/drives/{id}/root/subfolder`</span></span>

### <a name="azure-ad-resource-limitations"></a><span data-ttu-id="63b67-123">Limitaciones de los recursos de Azure AD</span><span class="sxs-lookup"><span data-stu-id="63b67-123">Azure AD Resource Limitations</span></span>

<span data-ttu-id="63b67-124">Se aplican ciertos límites a los recursos basados en Azure AD (usuarios y grupos), y es posible que se generen algunos errores si se supera lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="63b67-124">Certain limits apply to Azure AD based resources (users, groups) and may generate errors when exceeded:</span></span>

- <span data-ttu-id="63b67-125">Cuotas de suscripción permitidas:</span><span class="sxs-lookup"><span data-stu-id="63b67-125">Maximum subscription quotas:</span></span>

  - <span data-ttu-id="63b67-126">Por aplicación: 50 000 suscripciones en total</span><span class="sxs-lookup"><span data-stu-id="63b67-126">Per App: 50,000 total subscriptions</span></span>
  - <span data-ttu-id="63b67-127">Por espacio empresarial: 35 suscripciones en total en todas las aplicaciones</span><span class="sxs-lookup"><span data-stu-id="63b67-127">Per Tenant: 35 total subscriptions across all apps</span></span>
  - <span data-ttu-id="63b67-128">Por aplicación y espacio empresarial: 7 suscripciones en total</span><span class="sxs-lookup"><span data-stu-id="63b67-128">Per App and Tenant combination: 7 total subscriptions</span></span>

- <span data-ttu-id="63b67-129">No se admiten los espacios empresariales de Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="63b67-129">Azure AD B2C tenants are not supported</span></span>

- <span data-ttu-id="63b67-130">No se admiten notificaciones de entidades de usuario en cuentas Microsoft personales.</span><span class="sxs-lookup"><span data-stu-id="63b67-130">Notification for user entities are not supported for personal Microsoft accounts.</span></span>

## <a name="subscription-lifetime"></a><span data-ttu-id="63b67-131">Duración de la suscripción</span><span class="sxs-lookup"><span data-stu-id="63b67-131">Subscription lifetime</span></span>

<span data-ttu-id="63b67-132">Las suscripciones tienen una duración limitada.</span><span class="sxs-lookup"><span data-stu-id="63b67-132">Subscriptions have a limited lifetime.</span></span> <span data-ttu-id="63b67-133">Las aplicaciones tienen que renovar sus suscripciones antes de la fecha de expiración.</span><span class="sxs-lookup"><span data-stu-id="63b67-133">Apps need to renew their subscriptions before the expiration time.</span></span> <span data-ttu-id="63b67-134">De lo contrario tendrán que crear otra suscripción.</span><span class="sxs-lookup"><span data-stu-id="63b67-134">Otherwise, they need to create a new subscription.</span></span> <span data-ttu-id="63b67-135">Para obtener una lista de las fechas de expiración máximas, consulte [Duración máxima de la suscripción por tipo de recurso](../api-reference/v1.0/resources/subscription.md#maximum-length-of-subscription-per-resource-type).</span><span class="sxs-lookup"><span data-stu-id="63b67-135">For a list of maximum expiration times, see [Maximum length of subscription per resource type](../api-reference/v1.0/resources/subscription.md#maximum-length-of-subscription-per-resource-type).</span></span>

<span data-ttu-id="63b67-136">Las aplicaciones también pueden cancelar la suscripción en cualquier momento para dejar de recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="63b67-136">Apps can also unsubscribe at any time to stop getting notifications.</span></span>

## <a name="managing-subscriptions"></a><span data-ttu-id="63b67-137">Administrar suscripciones</span><span class="sxs-lookup"><span data-stu-id="63b67-137">Managing subscriptions</span></span>

<span data-ttu-id="63b67-138">Los clientes pueden crear suscripciones, renovar suscripciones y eliminar suscripciones.</span><span class="sxs-lookup"><span data-stu-id="63b67-138">Clients can create subscriptions, renew subscriptions, and delete subscriptions.</span></span>

### <a name="creating-a-subscription"></a><span data-ttu-id="63b67-139">Crear una suscripción</span><span class="sxs-lookup"><span data-stu-id="63b67-139">Creating a subscription</span></span>

<span data-ttu-id="63b67-p104">La creación de una suscripción es el primer paso para empezar a recibir notificaciones de un recurso. El proceso de suscripción es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="63b67-p104">Creating a subscription is the first step to start receiving notifications for a resource. The subscription process is as follows:</span></span>

1. <span data-ttu-id="63b67-142">El cliente envía una solicitud de suscripción (POST) a un recurso específico.</span><span class="sxs-lookup"><span data-stu-id="63b67-142">The client sends a subscription (POST) request for a specific resource.</span></span>

1. <span data-ttu-id="63b67-143">Microsoft Graph comprueba la solicitud.</span><span class="sxs-lookup"><span data-stu-id="63b67-143">Microsoft Graph verifies the request.</span></span>

    - <span data-ttu-id="63b67-144">Si la solicitud es válida, Microsoft Graph envía un token de validación a la dirección URL de notificación.</span><span class="sxs-lookup"><span data-stu-id="63b67-144">If the request is valid, Microsoft Graph sends a validation token to the notification URL.</span></span>
    - <span data-ttu-id="63b67-145">Si la solicitud no es válida, Microsoft Graph envía una respuesta de error con el código y los detalles.</span><span class="sxs-lookup"><span data-stu-id="63b67-145">If the request is invalid, Microsoft Graph sends an error response with code and details.</span></span>

1. <span data-ttu-id="63b67-146">El cliente envía el token de validación a Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="63b67-146">The client sends the validation token back to Microsoft Graph.</span></span>

1. <span data-ttu-id="63b67-147">Microsoft Graph envía una respuesta al cliente.</span><span class="sxs-lookup"><span data-stu-id="63b67-147">The Microsoft Graph sends a response back to the client.</span></span>

<span data-ttu-id="63b67-148">El cliente debe almacenar el identificador de suscripción para establecer la correlación de las notificaciones con la suscripción.</span><span class="sxs-lookup"><span data-stu-id="63b67-148">Client must store the subscription ID to correlate a notification with the corresponding subscription.</span></span>

#### <a name="subscription-request-example"></a><span data-ttu-id="63b67-149">Ejemplo de solicitud de suscripción</span><span class="sxs-lookup"><span data-stu-id="63b67-149">Subscription request example</span></span>

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

<span data-ttu-id="63b67-150">Se necesitan las propiedades `changeType`, `notificationUrl`, `resource` y `expirationDateTime`.</span><span class="sxs-lookup"><span data-stu-id="63b67-150">The `changeType`, `notificationUrl`, `resource` and `expirationDateTime` properties are required while the rest are optional.</span></span> <span data-ttu-id="63b67-151">Vea las definiciones y los valores de las propiedades en [Tipo de recurso de suscripción](../api-reference/v1.0/resources/subscription.md).</span><span class="sxs-lookup"><span data-stu-id="63b67-151">See [subscription resource type](../api-reference/v1.0/resources/subscription.md) for property definitions and values.</span></span>

<span data-ttu-id="63b67-152">Aunque `clientState` no se necesita, tiene que incluirse para cumplir nuestro proceso de control de notificaciones recomendado.</span><span class="sxs-lookup"><span data-stu-id="63b67-152">The , , , and  properties are required. See subscription resource type for property definitions and values. Although `clientState` is not required, you must include it to comply with our recommended notification handling process.</span></span> <span data-ttu-id="63b67-153">El establecimiento de esta propiedad le permitirá confirmar que las notificaciones que recibe proceden del servicio de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="63b67-153">Setting this property will allow you to confirm that notifications you receive originate from the Microsoft Graph service.</span></span> <span data-ttu-id="63b67-154">Por eso, el valor de la propiedad debe permanecer secreto y ser conocido solo por la aplicación y el servicio de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="63b67-154">For this reason, the value of the property should remain secret and known only to your application and the Microsoft Graph service.</span></span>

<span data-ttu-id="63b67-155">Si se ejecuta correctamente, Microsoft Graph muestra un código `201 Created` y un objeto [subscription](../api-reference/v1.0/resources/subscription.md) en el cuerpo.</span><span class="sxs-lookup"><span data-stu-id="63b67-155">If successful, Microsoft Graph returns a `201 Created` code and a [subscription](../api-reference/v1.0/resources/subscription.md) object in the body.</span></span>

#### <a name="notification-endpoint-validation"></a><span data-ttu-id="63b67-156">Validación de extremo de notificación</span><span class="sxs-lookup"><span data-stu-id="63b67-156">Notification endpoint validation</span></span>

<span data-ttu-id="63b67-157">Microsoft Graph valida el extremo de notificación indicado en la propiedad `notificationUrl` de la solicitud de suscripción antes de crear la suscripción.</span><span class="sxs-lookup"><span data-stu-id="63b67-157">Microsoft Graph validates the notification endpoint provided in the `notificationUrl` property of the subscription request before creating the subscription.</span></span> <span data-ttu-id="63b67-158">El proceso de validación es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="63b67-158">The filtering process in a dashboard occurs as follows:</span></span>

1. <span data-ttu-id="63b67-159">Microsoft Graph envía una solicitud POST a la dirección URL de notificación:</span><span class="sxs-lookup"><span data-stu-id="63b67-159">Microsoft Graph sends a POST request to the notification URL:</span></span>

  ``` http
  POST https://{notificationUrl}?validationToken={TokenDefinedByMicrosoftGraph}
  ```

1. <span data-ttu-id="63b67-160">El cliente debe proporcionar una respuesta con las siguientes características en menos de 10 segundos:</span><span class="sxs-lookup"><span data-stu-id="63b67-160">The client must provide a response with the following characteristics within 10 seconds:</span></span>

    - <span data-ttu-id="63b67-161">Un código de estado 200 (Correcto).</span><span class="sxs-lookup"><span data-stu-id="63b67-161">A 200 (OK) status code.</span></span>
    - <span data-ttu-id="63b67-162">El tipo de contenido debe ser `text/plain`.</span><span class="sxs-lookup"><span data-stu-id="63b67-162">The content type must be text/plain.</span></span>
    - <span data-ttu-id="63b67-163">El cuerpo debe incluir el token de validación proporcionado por Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="63b67-163">The body must include the validation token provided by Microsoft Graph.</span></span>

<span data-ttu-id="63b67-164">El cliente debe descartar el token de validación después de incluirlo en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="63b67-164">The client should discard the validation token after providing it in the response.</span></span>

### <a name="renewing-a-subscription"></a><span data-ttu-id="63b67-165">Renovar una suscripción</span><span class="sxs-lookup"><span data-stu-id="63b67-165">Renewing a subscription</span></span>

<span data-ttu-id="63b67-166">El cliente puede renovar una suscripción con una fecha de expiración específica de hasta tres días desde el momento de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="63b67-166">The client can renew a subscription with a specific expiration date of up to three days from the time of request. The expirationDateTime property is required.</span></span> <span data-ttu-id="63b67-167">La propiedad `expirationDateTime` es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="63b67-167">The `expirationDateTime` property is required.</span></span>

#### <a name="subscription-renewal-example"></a><span data-ttu-id="63b67-168">Ejemplo de renovación de la suscripción</span><span class="sxs-lookup"><span data-stu-id="63b67-168">Subscription renewal example</span></span>

```http
PATCH https://graph.microsoft.com/v1.0/subscriptions/{id}
Content-Type: application/json

{
  "expirationDateTime": "2016-03-22T11:00:00.0000000Z"
}
```

<span data-ttu-id="63b67-169">Si se ejecuta correctamente, Microsoft Graph muestra un código `200 OK` y un objeto [subscription](../api-reference/v1.0/resources/subscription.md) en el cuerpo.</span><span class="sxs-lookup"><span data-stu-id="63b67-169">If successful, Microsoft Graph returns a `200 OK` code and a [subscription](../api-reference/v1.0/resources/subscription.md) object in the body.</span></span> <span data-ttu-id="63b67-170">El objeto "suscription" incluye el nuevo valor de `expirationDateTime`.</span><span class="sxs-lookup"><span data-stu-id="63b67-170">The subscription object includes the new `expirationDateTime` value.</span></span>

### <a name="deleting-a-subscription"></a><span data-ttu-id="63b67-171">Eliminar una suscripción</span><span class="sxs-lookup"><span data-stu-id="63b67-171">Deleting a subscription</span></span>

<span data-ttu-id="63b67-172">El cliente puede dejar de recibir notificaciones al eliminar la suscripción con su identificador.</span><span class="sxs-lookup"><span data-stu-id="63b67-172">The client can stop receiving notifications by deleting the subscription using its ID.</span></span>

```http
DELETE https://graph.microsoft.com/v1.0/subscriptions/{id}
```

<span data-ttu-id="63b67-173">Si se ejecuta correctamente, Microsoft Graph devuelve un código `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="63b67-173">If successful, Microsoft Graph returns a `204 No Content` code.</span></span>

## <a name="notifications"></a><span data-ttu-id="63b67-174">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="63b67-174">Notifications</span></span>

<span data-ttu-id="63b67-175">El cliente comienza a recibir notificaciones después de crear la suscripción.</span><span class="sxs-lookup"><span data-stu-id="63b67-175">The client starts receiving notifications after creating the subscription.</span></span> <span data-ttu-id="63b67-176">Microsoft Graph envía una solicitud POST a la dirección URL de notificación cuando cambia el recurso.</span><span class="sxs-lookup"><span data-stu-id="63b67-176">Microsoft Graph sends a POST request to the notification URL:</span></span> <span data-ttu-id="63b67-177">Las notificaciones solo se envían para los cambios del tipo especificado en la suscripción, por ejemplo, `created`.</span><span class="sxs-lookup"><span data-stu-id="63b67-177">Notification are sent only for the changes of the type specified in the subscription, for example, `created`.</span></span>

> <span data-ttu-id="63b67-178">**Nota:** Cuando se utilizan varias suscripciones que supervisan el mismo tipo de recurso y usan la misma dirección URL de notificación, se puede enviar una solicitud POST que contenga varias notificaciones con distintos identificadores de suscripción.</span><span class="sxs-lookup"><span data-stu-id="63b67-178">**Note:** When using multiple subscriptions that monitor the same resource type and use the same notification URL, a POST can be sent that will contain multiple notifications with different subscription IDs.</span></span> <span data-ttu-id="63b67-179">No hay ninguna garantía de que todas las notificaciones de la solicitud POST pertenezcan a una única suscripción.</span><span class="sxs-lookup"><span data-stu-id="63b67-179">There is no guarantee that all notifications in the POST will belong to a single subscription.</span></span>

### <a name="notification-properties"></a><span data-ttu-id="63b67-180">Propiedades de la notificación</span><span class="sxs-lookup"><span data-stu-id="63b67-180">Notification properties</span></span>

<span data-ttu-id="63b67-181">El objeto "notification" tiene las propiedades siguientes:</span><span class="sxs-lookup"><span data-stu-id="63b67-181">The notification object has the following properties:</span></span>

| <span data-ttu-id="63b67-182">Propiedad</span><span class="sxs-lookup"><span data-stu-id="63b67-182">Property</span></span> | <span data-ttu-id="63b67-183">Tipo</span><span class="sxs-lookup"><span data-stu-id="63b67-183">Type</span></span> | <span data-ttu-id="63b67-184">Descripción</span><span class="sxs-lookup"><span data-stu-id="63b67-184">Description</span></span> |
|:---------|:-----|:------------|
| <span data-ttu-id="63b67-185">subscriptionId</span><span class="sxs-lookup"><span data-stu-id="63b67-185">subscriptionId</span></span> | <span data-ttu-id="63b67-186">string</span><span class="sxs-lookup"><span data-stu-id="63b67-186">string</span></span> | <span data-ttu-id="63b67-187">Identificador de la suscripción que generó la notificación.</span><span class="sxs-lookup"><span data-stu-id="63b67-187">The ID of the subscription that generated the notification.</span></span> |
| <span data-ttu-id="63b67-188">subscriptionExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="63b67-188">SubscriptionExpirationDateTime</span></span> | [<span data-ttu-id="63b67-189">dateTime</span><span class="sxs-lookup"><span data-stu-id="63b67-189">dateTime</span></span>](http://tools.ietf.org/html/rfc3339) | <span data-ttu-id="63b67-190">Fecha de expiración de la suscripción.</span><span class="sxs-lookup"><span data-stu-id="63b67-190">: The expiration time for the subscription.</span></span> |
| <span data-ttu-id="63b67-191">clientState</span><span class="sxs-lookup"><span data-stu-id="63b67-191">clientState</span></span> | <span data-ttu-id="63b67-192">string</span><span class="sxs-lookup"><span data-stu-id="63b67-192">string</span></span> | <span data-ttu-id="63b67-193">Propiedad `clientState` especificada en la solicitud de suscripción (en su caso).</span><span class="sxs-lookup"><span data-stu-id="63b67-193">The `clientState` property specified in the subscription request (if any).</span></span> |
| <span data-ttu-id="63b67-194">changeType</span><span class="sxs-lookup"><span data-stu-id="63b67-194">changeType</span></span> | <span data-ttu-id="63b67-195">string</span><span class="sxs-lookup"><span data-stu-id="63b67-195">string</span></span> | <span data-ttu-id="63b67-196">Tipo de evento que generó la notificación.</span><span class="sxs-lookup"><span data-stu-id="63b67-196">The event type that caused the notification.</span></span> <span data-ttu-id="63b67-197">Por ejemplo, `created` al recibir un correo o `updated` al marcar un mensaje como leído.</span><span class="sxs-lookup"><span data-stu-id="63b67-197">changeType - The event type that caused the notification. For example, `created` on mail receive, or `updated` on marking a message read.</span></span> |
| <span data-ttu-id="63b67-198">resource</span><span class="sxs-lookup"><span data-stu-id="63b67-198">resource</span></span> | <span data-ttu-id="63b67-199">string</span><span class="sxs-lookup"><span data-stu-id="63b67-199">string</span></span> | <span data-ttu-id="63b67-200">URI del recurso relativo a `https://graph.microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="63b67-200">resource - The URI of the resource relative to `https://graph.microsoft.com`.</span></span> |
| <span data-ttu-id="63b67-201">resourceData</span><span class="sxs-lookup"><span data-stu-id="63b67-201">ResourceData</span></span> | <span data-ttu-id="63b67-202">object</span><span class="sxs-lookup"><span data-stu-id="63b67-202">object</span></span> | <span data-ttu-id="63b67-203">El contenido de esta propiedad depende del tipo de recurso al que se suscriba.</span><span class="sxs-lookup"><span data-stu-id="63b67-203">The content of this property depends on the type of resource being subscribed to.</span></span> |

<span data-ttu-id="63b67-204">Por ejemplo, para recursos de Outlook, `resourceData` contiene los siguientes campos:</span><span class="sxs-lookup"><span data-stu-id="63b67-204">For example, for Outlook resources, `resourceData` contains the following fields:</span></span>

| <span data-ttu-id="63b67-205">Propiedad</span><span class="sxs-lookup"><span data-stu-id="63b67-205">Property</span></span> | <span data-ttu-id="63b67-206">Tipo</span><span class="sxs-lookup"><span data-stu-id="63b67-206">Type</span></span> | <span data-ttu-id="63b67-207">Descripción</span><span class="sxs-lookup"><span data-stu-id="63b67-207">Description</span></span> |
|:---------|:-----|:------------|
| <span data-ttu-id="63b67-208">@odata.type</span><span class="sxs-lookup"><span data-stu-id="63b67-208">@odata.type</span></span> | <span data-ttu-id="63b67-209">string</span><span class="sxs-lookup"><span data-stu-id="63b67-209">string</span></span> | <span data-ttu-id="63b67-210">Tipo de entidad OData en Microsoft Graph que describe el objeto representado.</span><span class="sxs-lookup"><span data-stu-id="63b67-210">@odata.type - The OData entity type in Microsoft Graph that describes the represented object.</span></span> |
| <span data-ttu-id="63b67-211">@odata.id</span><span class="sxs-lookup"><span data-stu-id="63b67-211">@odata.id</span></span> | <span data-ttu-id="63b67-212">string</span><span class="sxs-lookup"><span data-stu-id="63b67-212">string</span></span> | <span data-ttu-id="63b67-213">Identificador OData del objeto.</span><span class="sxs-lookup"><span data-stu-id="63b67-213">@odata.id - The OData identifier of the object.</span></span> |
| <span data-ttu-id="63b67-214">@odata.etag</span><span class="sxs-lookup"><span data-stu-id="63b67-214">@odata.etag</span></span> | <span data-ttu-id="63b67-215">string</span><span class="sxs-lookup"><span data-stu-id="63b67-215">string</span></span> | <span data-ttu-id="63b67-216">Etiqueta de entidad HTTP que representa una versión del objeto.</span><span class="sxs-lookup"><span data-stu-id="63b67-216">@odata.etag - The HTTP entity tag that represents a version of the object.</span></span> |
| <span data-ttu-id="63b67-217">id</span><span class="sxs-lookup"><span data-stu-id="63b67-217">id</span></span> | <span data-ttu-id="63b67-218">string</span><span class="sxs-lookup"><span data-stu-id="63b67-218">string</span></span> | <span data-ttu-id="63b67-219">Identificador del objeto.</span><span class="sxs-lookup"><span data-stu-id="63b67-219">Id - The identifier of the object.</span></span> |

> <span data-ttu-id="63b67-220">**Nota:** El valor `id` proporcionado en `resourceData` es válido en el momento en que se genera la notificación.</span><span class="sxs-lookup"><span data-stu-id="63b67-220">**Note:** The `id` value provided in `resourceData` is valid at the time the notification was generated.</span></span> <span data-ttu-id="63b67-221">Algunas acciones, como mover un mensaje a otra carpeta, pueden dar lugar a que el `id` ya no sea válido cuando se procese la notificación.</span><span class="sxs-lookup"><span data-stu-id="63b67-221">Some actions, such as moving a message to another folder, may result in the `id` no longer being valid when the notification is processed.</span></span>

### <a name="notification-example"></a><span data-ttu-id="63b67-222">Ejemplo de notificación</span><span class="sxs-lookup"><span data-stu-id="63b67-222">Notification example</span></span>

<span data-ttu-id="63b67-223">Cuando el usuario recibe un correo electrónico, Microsoft Graph envía una notificación como la siguiente:</span><span class="sxs-lookup"><span data-stu-id="63b67-223">When the user receives an email, Microsoft Graph sends a notification like the following:</span></span>

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

<span data-ttu-id="63b67-224">Tenga en cuenta que el campo `value` es una matriz de objetos.</span><span class="sxs-lookup"><span data-stu-id="63b67-224">Note the `value` field is an array of objects.</span></span> <span data-ttu-id="63b67-225">Si hay muchas notificaciones en cola, puede que Microsoft Graph envíe varios elementos en una sola solicitud.</span><span class="sxs-lookup"><span data-stu-id="63b67-225">When there are many queued notifications, Microsoft Graph may send multiple items in a single request.</span></span> <span data-ttu-id="63b67-226">Pueden incluirse notificaciones de distintas suscripciones en una misma solicitud de notificación.</span><span class="sxs-lookup"><span data-stu-id="63b67-226">Notifications from different subscriptions can be included in the same notification request.</span></span>

### <a name="processing-the-notification"></a><span data-ttu-id="63b67-227">Procesar la notificación</span><span class="sxs-lookup"><span data-stu-id="63b67-227">Processing the notification</span></span>

<span data-ttu-id="63b67-228">Cada notificación que reciba la aplicación debe procesarse.</span><span class="sxs-lookup"><span data-stu-id="63b67-228">Each notification received by your app should be processed.</span></span> <span data-ttu-id="63b67-229">Estas son las tareas mínimas que debe realizar la aplicación para procesar una notificación:</span><span class="sxs-lookup"><span data-stu-id="63b67-229">After your application starts receiving notifications it must process them. The following are the minimum tasks that your app must perform to process a notification:</span></span>

1. <span data-ttu-id="63b67-230">Validar la propiedad `clientState`.</span><span class="sxs-lookup"><span data-stu-id="63b67-230">Validate the `clientState` property.</span></span> <span data-ttu-id="63b67-231">Debe coincidir con el valor enviado originalmente con la solicitud de creación de suscripción.</span><span class="sxs-lookup"><span data-stu-id="63b67-231">It must match the value originally submitted with the subscription creation request.</span></span>

    > <span data-ttu-id="63b67-232">**Nota:** Si no es así, no debe considerar la notificación como válida.</span><span class="sxs-lookup"><span data-stu-id="63b67-232">**Note:** If this isn't true, you should not consider this a valid notification.</span></span> <span data-ttu-id="63b67-233">Es posible que la notificación no se haya originado en Microsoft Graph y que haya sido enviada por un actor no autorizado.</span><span class="sxs-lookup"><span data-stu-id="63b67-233">It is possible that the notification has not originated from Microsoft Graph and may have been sent by a rogue actor.</span></span> <span data-ttu-id="63b67-234">También debe investigar de dónde proviene la notificación y tomar las medidas adecuadas.</span><span class="sxs-lookup"><span data-stu-id="63b67-234">Note: If this isn't true, you shouldn't consider this a valid notification. You should also investigate where the notification comes from and take appropriate action.</span></span>

1. <span data-ttu-id="63b67-235">Actualizar la aplicación según la lógica empresarial.</span><span class="sxs-lookup"><span data-stu-id="63b67-235">Update your application based on your business logic.</span></span>

1. <span data-ttu-id="63b67-236">Enviar un código de estado `202 - Accepted` en la respuesta a Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="63b67-236">Send a `202 - Accepted` status code in your response to Microsoft Graph.</span></span> <span data-ttu-id="63b67-237">Si Microsoft Graph no recibe un código de clase 2xx, intentará volver a enviar la notificación varias veces.</span><span class="sxs-lookup"><span data-stu-id="63b67-237">Send a  status code in your response to Microsoft Graph. If Microsoft Graph doesn't receive a 2xx class code, it will retry resending the notification a number of times.</span></span>

    > <span data-ttu-id="63b67-238">**Nota:** Debe enviar un código de estado `202 - Accepted`, aunque la propiedad `clientState` no coincida con la enviada en la solicitud de suscripción.</span><span class="sxs-lookup"><span data-stu-id="63b67-238">You should send a  status code even if the clientState property doesn't match the one submitted with the subscription request.</span></span> <span data-ttu-id="63b67-239">Esto es recomendable, ya que evita que un posible actor no autorizado descubra que tal vez usted no confíe en sus notificaciones y usar esta información para adivinar el valor de la propiedad `clientState`.</span><span class="sxs-lookup"><span data-stu-id="63b67-239">This is a good practice as it prevents a potential rogue actor from discovering the fact that you may not trust their notifications, and perhaps using that information to guess the value of the `clientState` property.</span></span>

<span data-ttu-id="63b67-240">Repita esto para otras notificaciones de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="63b67-240">Repeat for other notifications in the request.</span></span>

## <a name="code-samples"></a><span data-ttu-id="63b67-241">Ejemplos de código</span><span class="sxs-lookup"><span data-stu-id="63b67-241">Code samples</span></span>

<span data-ttu-id="63b67-242">Los siguientes ejemplos de código están disponibles en GitHub.</span><span class="sxs-lookup"><span data-stu-id="63b67-242">The following code samples are available on GitHub.</span></span>

- [<span data-ttu-id="63b67-243">Ejemplo de webhooks de Microsoft Graph para Node.js</span><span class="sxs-lookup"><span data-stu-id="63b67-243">Microsoft Graph Webhooks Sample for Node.js</span></span>](https://github.com/OfficeDev/Microsoft-Graph-Nodejs-Webhooks)
- [<span data-ttu-id="63b67-244">Ejemplo de webhooks de Microsoft Graph para ASP.NET</span><span class="sxs-lookup"><span data-stu-id="63b67-244">Microsoft Graph Webhooks Sample for ASP.NET</span></span>](https://github.com/OfficeDev/Microsoft-Graph-ASPNET-Webhooks)
- [<span data-ttu-id="63b67-245">Ejemplo de webhooks de usuario de Microsoft Graph con WebJobs SDK</span><span class="sxs-lookup"><span data-stu-id="63b67-245">Microsoft Graph User Webhooks Sample using WebJobs SDK</span></span>](https://github.com/microsoftgraph/webjobs-webhooks-sample)

## <a name="see-also"></a><span data-ttu-id="63b67-246">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="63b67-246">See also</span></span>

- [<span data-ttu-id="63b67-247">Tipo de recurso de suscripción</span><span class="sxs-lookup"><span data-stu-id="63b67-247">Subscription resource type</span></span>](../api-reference/v1.0/resources/subscription.md)
- [<span data-ttu-id="63b67-248">Obtener suscripción</span><span class="sxs-lookup"><span data-stu-id="63b67-248">Get subscription</span></span>](../api-reference/v1.0/api/subscription_get.md)
- [<span data-ttu-id="63b67-249">Crear suscripción</span><span class="sxs-lookup"><span data-stu-id="63b67-249">Create subscription</span></span>](../api-reference/v1.0/api/subscription_post_subscriptions.md)

[contact]: ../api-reference/v1.0/resources/contact.md
[conversation]: ../api-reference/v1.0/resources/conversation.md
[drive]: ../api-reference/v1.0/resources/drive.md
[event]: ../api-reference/v1.0/resources/event.md
[message]: ../api-reference/v1.0/resources/message.md
