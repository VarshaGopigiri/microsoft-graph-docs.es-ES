---
title: Configurar las notificaciones de cambios en los datos de usuario
description: La API de Microsoft Graph utiliza un mecanismo webhook para entregar notificaciones a los clientes. Un cliente es un servicio web que configura su propia dirección URL para recibir notificaciones. Las aplicaciones cliente utilizan notificaciones para actualizar su estado cuando se producen cambios.
author: piotrci
ms.openlocfilehash: 6af6f3c54a7956d6a505c88bfc82fc8233dccdad
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27337047"
---
# <a name="set-up-notifications-for-changes-in-user-data"></a><span data-ttu-id="074b7-105">Configurar las notificaciones de cambios en los datos de usuario</span><span class="sxs-lookup"><span data-stu-id="074b7-105">Set up notifications for changes in user data</span></span>

<span data-ttu-id="074b7-p102">La API de Microsoft Graph utiliza un mecanismo webhook para entregar notificaciones a los clientes. Un cliente es un servicio web que configura su propia dirección URL para recibir notificaciones. Las aplicaciones cliente utilizan notificaciones para actualizar su estado cuando se producen cambios.</span><span class="sxs-lookup"><span data-stu-id="074b7-p102">The Microsoft Graph API uses a webhook mechanism to deliver notifications to clients. A client is a web service that configures its own URL to receive notifications. Client apps use notifications to update their state upon changes.</span></span>

<span data-ttu-id="074b7-109">Microsoft Graph acepta la solicitud de suscripción y después envía las notificaciones a la dirección URL especificada en la suscripción.</span><span class="sxs-lookup"><span data-stu-id="074b7-109">After Microsoft Graph accepts the subscription request, it pushes notifications to the URL specified in the subscription.</span></span> <span data-ttu-id="074b7-110">La aplicación actúa entonces según su lógica de negocios.</span><span class="sxs-lookup"><span data-stu-id="074b7-110">The app then takes action according to its business logic.</span></span> <span data-ttu-id="074b7-111">Por ejemplo, captura más datos, actualiza la caché y las vistas, etc.</span><span class="sxs-lookup"><span data-stu-id="074b7-111">For example, it fetches more data, updates its cache and views, etc.</span></span>

## <a name="supported-resources"></a><span data-ttu-id="074b7-112">Recursos admitidos</span><span class="sxs-lookup"><span data-stu-id="074b7-112">Supported resources</span></span>

<span data-ttu-id="074b7-113">Mediante la API de Microsoft Graph, una aplicación puede suscribirse a cambios en los siguientes recursos:</span><span class="sxs-lookup"><span data-stu-id="074b7-113">Using the Microsoft Graph API, an app can subscribe to changes on the following resources:</span></span>

- <span data-ttu-id="074b7-114">Mensajes</span><span class="sxs-lookup"><span data-stu-id="074b7-114">Messages</span></span>
- <span data-ttu-id="074b7-115">Eventos</span><span class="sxs-lookup"><span data-stu-id="074b7-115">Events</span></span>
- <span data-ttu-id="074b7-116">Contacts</span><span class="sxs-lookup"><span data-stu-id="074b7-116">Contacts</span></span>
- <span data-ttu-id="074b7-117">Usuarios</span><span class="sxs-lookup"><span data-stu-id="074b7-117">Users</span></span>
- <span data-ttu-id="074b7-118">Grupos</span><span class="sxs-lookup"><span data-stu-id="074b7-118">Groups</span></span>
- <span data-ttu-id="074b7-119">Conversaciones de grupo</span><span class="sxs-lookup"><span data-stu-id="074b7-119">Group conversations</span></span>
- <span data-ttu-id="074b7-120">Contenido compartido en OneDrive, incluidas las unidades de disco asociadas a sitios de SharePoint</span><span class="sxs-lookup"><span data-stu-id="074b7-120">Content shared on OneDrive including drives associated with SharePoint sites</span></span>
- <span data-ttu-id="074b7-121">Carpetas de OneDrive personales del usuario</span><span class="sxs-lookup"><span data-stu-id="074b7-121">User's personal OneDrive folders</span></span>
- <span data-ttu-id="074b7-122">Alertas de seguridad</span><span class="sxs-lookup"><span data-stu-id="074b7-122">Security Alerts</span></span>

<span data-ttu-id="074b7-123">Por ejemplo, puede crear una suscripción a una carpeta de correo específica: `me/mailFolders('inbox')/messages`</span><span class="sxs-lookup"><span data-stu-id="074b7-123">For instance, you can create a subscription to a specific mail folder: `me/mailFolders('inbox')/messages`</span></span>

<span data-ttu-id="074b7-124">O a un recurso de nivel superior: `me/messages`, `me/contacts`, `me/events`, `users` o `groups`</span><span class="sxs-lookup"><span data-stu-id="074b7-124">Or to a top-level resource: `me/messages`, `me/contacts`, `me/events`, `users`, or `groups`</span></span>

<span data-ttu-id="074b7-125">O a una instancia de recurso específica: `users/{id}`, `groups/{id}`, `groups/{id}/conversations`</span><span class="sxs-lookup"><span data-stu-id="074b7-125">Or to a specific resource instance: `users/{id}`, `groups/{id}`, `groups/{id}/conversations`</span></span>

<span data-ttu-id="074b7-126">O a una unidad de disco de SharePoint o de OneDrive para la Empresa: `/drive/root`</span><span class="sxs-lookup"><span data-stu-id="074b7-126">Or to a SharePoint/OneDrive for Business drive: `/drive/root`</span></span>

<span data-ttu-id="074b7-127">O a una instancia de OneDrive personal del usuario: `/drives/{id}/root`
`/drives/{id}/root/subfolder`</span><span class="sxs-lookup"><span data-stu-id="074b7-127">Or to a user's personal OneDrive: `/drives/{id}/root`
`/drives/{id}/root/subfolder`</span></span>

<span data-ttu-id="074b7-128">O a una nueva [alerta de API de seguridad](security-concept-overview.md): `/security/alerts?$filter=status eq ‘New’`, `/security/alerts?$filter=vendorInformation/provider eq ‘ASC’`</span><span class="sxs-lookup"><span data-stu-id="074b7-128">Or to a new [Security API alert](security-concept-overview.md): `/security/alerts?$filter=status eq ‘New’`, `/security/alerts?$filter=vendorInformation/provider eq ‘ASC’`</span></span>

### <a name="azure-ad-resource-limitations"></a><span data-ttu-id="074b7-129">Limitaciones de los recursos de Azure AD</span><span class="sxs-lookup"><span data-stu-id="074b7-129">Azure AD resource limitations</span></span>

<span data-ttu-id="074b7-130">Se aplican ciertos límites a los recursos basados en Azure AD (usuarios y grupos), y es posible que se generen algunos errores si se supera lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="074b7-130">Certain limits apply to Azure AD based resources (users, groups) and may generate errors when exceeded:</span></span>

- <span data-ttu-id="074b7-131">Cuotas de suscripción permitidas:</span><span class="sxs-lookup"><span data-stu-id="074b7-131">Maximum subscription quotas:</span></span>

  - <span data-ttu-id="074b7-132">Por aplicación: 50 000 suscripciones en total</span><span class="sxs-lookup"><span data-stu-id="074b7-132">Per app: 50,000 total subscriptions</span></span>
  - <span data-ttu-id="074b7-133">Por espacio empresarial: 35 suscripciones en total en todas las aplicaciones</span><span class="sxs-lookup"><span data-stu-id="074b7-133">Per tenant: 35 total subscriptions across all apps</span></span>
  - <span data-ttu-id="074b7-134">Por aplicación y espacio empresarial: 7 suscripciones en total</span><span class="sxs-lookup"><span data-stu-id="074b7-134">Per app and tenant combination: 7 total subscriptions</span></span>

- <span data-ttu-id="074b7-135">No se admiten los espacios empresariales de Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="074b7-135">Azure AD B2C tenants are not supported.</span></span>

- <span data-ttu-id="074b7-136">No se admiten notificaciones de entidades de usuario en cuentas Microsoft personales.</span><span class="sxs-lookup"><span data-stu-id="074b7-136">Notification for user entities are not supported for personal Microsoft accounts.</span></span>

## <a name="subscription-lifetime"></a><span data-ttu-id="074b7-137">Duración de la suscripción</span><span class="sxs-lookup"><span data-stu-id="074b7-137">Subscription lifetime</span></span>

<span data-ttu-id="074b7-138">Las suscripciones tienen una duración limitada.</span><span class="sxs-lookup"><span data-stu-id="074b7-138">Subscriptions have a limited lifetime.</span></span> <span data-ttu-id="074b7-139">Las aplicaciones tienen que renovar sus suscripciones antes de la fecha de expiración.</span><span class="sxs-lookup"><span data-stu-id="074b7-139">Apps need to renew their subscriptions before the expiration time.</span></span> <span data-ttu-id="074b7-140">De lo contrario tendrán que crear otra suscripción.</span><span class="sxs-lookup"><span data-stu-id="074b7-140">Otherwise, they need to create a new subscription.</span></span> <span data-ttu-id="074b7-141">Para obtener una lista de las fechas de expiración máximas, consulte [Duración máxima de la suscripción por tipo de recurso](/graph/api/resources/subscription?view=graph-rest-1.0#maximum-length-of-subscription-per-resource-type).</span><span class="sxs-lookup"><span data-stu-id="074b7-141">For a list of maximum expiration times, see [Maximum length of subscription per resource type](/graph/api/resources/subscription?view=graph-rest-1.0#maximum-length-of-subscription-per-resource-type).</span></span>

<span data-ttu-id="074b7-142">Las aplicaciones también pueden cancelar la suscripción en cualquier momento para dejar de recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="074b7-142">Apps can also unsubscribe at any time to stop getting notifications.</span></span>

## <a name="managing-subscriptions"></a><span data-ttu-id="074b7-143">Administrar suscripciones</span><span class="sxs-lookup"><span data-stu-id="074b7-143">Managing subscriptions</span></span>

<span data-ttu-id="074b7-144">Los clientes pueden crear suscripciones, renovar suscripciones y eliminar suscripciones.</span><span class="sxs-lookup"><span data-stu-id="074b7-144">Clients can create subscriptions, renew subscriptions, and delete subscriptions.</span></span>

### <a name="creating-a-subscription"></a><span data-ttu-id="074b7-145">Crear una suscripción</span><span class="sxs-lookup"><span data-stu-id="074b7-145">Creating a subscription</span></span>

<span data-ttu-id="074b7-p105">La creación de una suscripción es el primer paso para empezar a recibir notificaciones de un recurso. El proceso de suscripción es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="074b7-p105">Creating a subscription is the first step to start receiving notifications for a resource. The subscription process is as follows:</span></span>

1. <span data-ttu-id="074b7-148">El cliente envía una solicitud de suscripción (POST) a un recurso específico.</span><span class="sxs-lookup"><span data-stu-id="074b7-148">The client sends a subscription (POST) request for a specific resource.</span></span>

1. <span data-ttu-id="074b7-149">Microsoft Graph comprueba la solicitud.</span><span class="sxs-lookup"><span data-stu-id="074b7-149">Microsoft Graph verifies the request.</span></span>

    - <span data-ttu-id="074b7-150">Si la solicitud es válida, Microsoft Graph envía un token de validación a la dirección URL de notificación.</span><span class="sxs-lookup"><span data-stu-id="074b7-150">If the request is valid, Microsoft Graph sends a validation token to the notification URL.</span></span>
    - <span data-ttu-id="074b7-151">Si la solicitud no es válida, Microsoft Graph envía una respuesta de error con el código y los detalles.</span><span class="sxs-lookup"><span data-stu-id="074b7-151">If the request is invalid, Microsoft Graph sends an error response with code and details.</span></span>

1. <span data-ttu-id="074b7-152">El cliente envía el token de validación a Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="074b7-152">The client sends the validation token back to Microsoft Graph.</span></span>

1. <span data-ttu-id="074b7-153">Microsoft Graph envía una respuesta al cliente.</span><span class="sxs-lookup"><span data-stu-id="074b7-153">The Microsoft Graph sends a response back to the client.</span></span>

<span data-ttu-id="074b7-154">El cliente debe almacenar el identificador de suscripción para establecer la correlación de las notificaciones con la suscripción.</span><span class="sxs-lookup"><span data-stu-id="074b7-154">The client must store the subscription ID to correlate notifications with the subscription.</span></span>

#### <a name="subscription-request-example"></a><span data-ttu-id="074b7-155">Ejemplo de solicitud de suscripción</span><span class="sxs-lookup"><span data-stu-id="074b7-155">Subscription request example</span></span>

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

<span data-ttu-id="074b7-156">Se necesitan las propiedades `changeType`, `notificationUrl`, `resource` y `expirationDateTime`.</span><span class="sxs-lookup"><span data-stu-id="074b7-156">The `changeType`, `notificationUrl`, `resource`, and `expirationDateTime` properties are required.</span></span> <span data-ttu-id="074b7-157">Vea las definiciones y los valores de las propiedades en [Tipo de recurso de suscripción](/graph/api/resources/subscription?view=graph-rest-1.0).</span><span class="sxs-lookup"><span data-stu-id="074b7-157">See [subscription resource type](/graph/api/resources/subscription?view=graph-rest-1.0) for property definitions and values.</span></span>

<span data-ttu-id="074b7-158">La propiedad `resource` Especifica el recurso al que se le supervisarán los cambios.</span><span class="sxs-lookup"><span data-stu-id="074b7-158">The `resource` property specifies the resource that will be monitored for changes.</span></span> <span data-ttu-id="074b7-159">Por ejemplo, puede crear una suscripción a una carpeta de correo específica: `me/mailFolders('inbox')/messages` o en representación de otro usuario dado por el consentimiento de un administrador: `users/john.doe@onmicrosoft.com/mailFolders('inbox')/messages`.</span><span class="sxs-lookup"><span data-stu-id="074b7-159">For example, you can create a subscription to a specific mail folder: `me/mailFolders('inbox')/messages` or on behalf of a user given by an administrator  consent: `users/john.doe@onmicrosoft.com/mailFolders('inbox')/messages`.</span></span>

<span data-ttu-id="074b7-160">Aunque `clientState` no se necesita, tiene que incluirse para cumplir nuestro proceso de control de notificaciones recomendado.</span><span class="sxs-lookup"><span data-stu-id="074b7-160">Although `clientState` is not required, you must include it to comply with our recommended notification handling process.</span></span> <span data-ttu-id="074b7-161">El establecimiento de esta propiedad le permitirá confirmar que las notificaciones que recibe proceden del servicio de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="074b7-161">Setting this property will allow you to confirm that notifications you receive originate from the Microsoft Graph service.</span></span> <span data-ttu-id="074b7-162">Por eso, el valor de la propiedad debe permanecer secreto y ser conocido solo por la aplicación y el servicio de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="074b7-162">For this reason, the value of the property should remain secret and known only to your application and the Microsoft Graph service.</span></span>

<span data-ttu-id="074b7-163">Si se ejecuta correctamente, Microsoft Graph muestra un código `201 Created` y un objeto [subscription](/graph/api/resources/subscription?view=graph-rest-1.0) en el cuerpo.</span><span class="sxs-lookup"><span data-stu-id="074b7-163">If successful, Microsoft Graph returns a `201 Created` code and a [subscription](/graph/api/resources/subscription?view=graph-rest-1.0) object in the body.</span></span>

#### <a name="notification-endpoint-validation"></a><span data-ttu-id="074b7-164">Validación de extremo de notificación</span><span class="sxs-lookup"><span data-stu-id="074b7-164">Notification endpoint validation</span></span>

<span data-ttu-id="074b7-165">Microsoft Graph valida el extremo de notificación indicado en la propiedad `notificationUrl` de la solicitud de suscripción antes de crear la suscripción.</span><span class="sxs-lookup"><span data-stu-id="074b7-165">Microsoft Graph validates the notification endpoint provided in the `notificationUrl` property of the subscription request before creating the subscription.</span></span> <span data-ttu-id="074b7-166">El proceso de validación es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="074b7-166">The validation process occurs as follows:</span></span>

1. <span data-ttu-id="074b7-167">Microsoft Graph envía una solicitud POST a la dirección URL de notificación:</span><span class="sxs-lookup"><span data-stu-id="074b7-167">Microsoft Graph sends a POST request to the notification URL:</span></span>

    ``` http
    POST https://{notificationUrl}?validationToken={opaqueTokenCreatedByMicrosoftGraph}
    ```

    > <span data-ttu-id="074b7-168">**Importante:** Como el `validationToken` es un parámetro de consulta, el cliente debe descodificarlo correctamente, según las prácticas de codificación de HTTP.</span><span class="sxs-lookup"><span data-stu-id="074b7-168">**Important:** Since the `validationToken` is a query parameter it must be properly decoded by the client, as per HTTP coding practices.</span></span> <span data-ttu-id="074b7-169">Si el cliente no descodifica el token y usa en su lugar el valor codificado en el paso siguiente (respuesta), se producirá un error de validación.</span><span class="sxs-lookup"><span data-stu-id="074b7-169">If the client does not decode the token, and instead uses the encoded value in the next step (response), validation will fail.</span></span> <span data-ttu-id="074b7-170">Además, el cliente debe tratar el valor de token como opaco, ya que el formato de token puede cambiar en el futuro, sin aviso.</span><span class="sxs-lookup"><span data-stu-id="074b7-170">Also, the client should treat the token value as opaque since the token format may change in the future, without notice.</span></span>

1. <span data-ttu-id="074b7-171">El cliente debe proporcionar una respuesta con las siguientes características en menos de 10 segundos:</span><span class="sxs-lookup"><span data-stu-id="074b7-171">The client must provide a response with the following characteristics within 10 seconds:</span></span>

    - <span data-ttu-id="074b7-172">Un código de estado 200 (Correcto).</span><span class="sxs-lookup"><span data-stu-id="074b7-172">A 200 (OK) status code.</span></span>
    - <span data-ttu-id="074b7-173">El tipo de contenido debe ser `text/plain`.</span><span class="sxs-lookup"><span data-stu-id="074b7-173">The content type must be `text/plain`.</span></span>
    - <span data-ttu-id="074b7-174">El cuerpo debe incluir el token de validación proporcionado por Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="074b7-174">The body must include the validation token provided by Microsoft Graph.</span></span>

<span data-ttu-id="074b7-175">El cliente debe descartar el token de validación después de incluirlo en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="074b7-175">The client should discard the validation token after providing it in the response.</span></span>

### <a name="renewing-a-subscription"></a><span data-ttu-id="074b7-176">Renovar una suscripción</span><span class="sxs-lookup"><span data-stu-id="074b7-176">Renewing a subscription</span></span>

<span data-ttu-id="074b7-177">El cliente puede renovar una suscripción con una fecha de expiración específica de hasta tres días desde el momento de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="074b7-177">The client can renew a subscription with a specific expiration date of up to three days from the time of request.</span></span> <span data-ttu-id="074b7-178">La propiedad `expirationDateTime` es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="074b7-178">The `expirationDateTime` property is required.</span></span>

#### <a name="subscription-renewal-example"></a><span data-ttu-id="074b7-179">Ejemplo de renovación de la suscripción</span><span class="sxs-lookup"><span data-stu-id="074b7-179">Subscription renewal example</span></span>

```http
PATCH https://graph.microsoft.com/v1.0/subscriptions/{id}
Content-Type: application/json

{
  "expirationDateTime": "2016-03-22T11:00:00.0000000Z"
}
```

<span data-ttu-id="074b7-180">Si se ejecuta correctamente, Microsoft Graph muestra un código `200 OK` y un objeto [subscription](/graph/api/resources/subscription?view=graph-rest-1.0) en el cuerpo.</span><span class="sxs-lookup"><span data-stu-id="074b7-180">If successful, Microsoft Graph returns a `200 OK` code and a [subscription](/graph/api/resources/subscription?view=graph-rest-1.0) object in the body.</span></span> <span data-ttu-id="074b7-181">El objeto "suscription" incluye el nuevo valor de `expirationDateTime`.</span><span class="sxs-lookup"><span data-stu-id="074b7-181">The subscription object includes the new `expirationDateTime` value.</span></span>

### <a name="deleting-a-subscription"></a><span data-ttu-id="074b7-182">Eliminar una suscripción</span><span class="sxs-lookup"><span data-stu-id="074b7-182">Deleting a subscription</span></span>

<span data-ttu-id="074b7-183">El cliente puede dejar de recibir notificaciones al eliminar la suscripción con su identificador.</span><span class="sxs-lookup"><span data-stu-id="074b7-183">The client can stop receiving notifications by deleting the subscription using its ID.</span></span>

```http
DELETE https://graph.microsoft.com/v1.0/subscriptions/{id}
```

<span data-ttu-id="074b7-184">Si se ejecuta correctamente, Microsoft Graph devuelve un código `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="074b7-184">If successful, Microsoft Graph returns a `204 No Content` code.</span></span>

## <a name="notifications"></a><span data-ttu-id="074b7-185">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="074b7-185">Notifications</span></span>

<span data-ttu-id="074b7-186">El cliente comienza a recibir notificaciones después de crear la suscripción.</span><span class="sxs-lookup"><span data-stu-id="074b7-186">The client starts receiving notifications after creating the subscription.</span></span> <span data-ttu-id="074b7-187">Microsoft Graph envía una solicitud POST a la dirección URL de notificación cuando cambia el recurso.</span><span class="sxs-lookup"><span data-stu-id="074b7-187">Microsoft Graph sends a POST request to the notification URL when the resource changes.</span></span> <span data-ttu-id="074b7-188">Las notificaciones solo se envían para los cambios del tipo especificado en la suscripción, por ejemplo, `created`.</span><span class="sxs-lookup"><span data-stu-id="074b7-188">Notification are sent only for the changes of the type specified in the subscription, for example, `created`.</span></span>

> <span data-ttu-id="074b7-189">**Nota:** Cuando se utilizan varias suscripciones que supervisan el mismo tipo de recurso y usan la misma dirección URL de notificación, se puede enviar una solicitud POST que contenga varias notificaciones con distintos identificadores de suscripción.</span><span class="sxs-lookup"><span data-stu-id="074b7-189">**Note:** When using multiple subscriptions that monitor the same resource type and use the same notification URL, a POST can be sent that will contain multiple notifications with different subscription IDs.</span></span> <span data-ttu-id="074b7-190">No hay ninguna garantía de que todas las notificaciones de la solicitud POST pertenezcan a una única suscripción.</span><span class="sxs-lookup"><span data-stu-id="074b7-190">There is no guarantee that all notifications in the POST will belong to a single subscription.</span></span>

### <a name="notification-properties"></a><span data-ttu-id="074b7-191">Propiedades de la notificación</span><span class="sxs-lookup"><span data-stu-id="074b7-191">Notification properties</span></span>

<span data-ttu-id="074b7-192">El objeto "notification" tiene las propiedades siguientes:</span><span class="sxs-lookup"><span data-stu-id="074b7-192">The notification object has the following properties:</span></span>

| <span data-ttu-id="074b7-193">Propiedad</span><span class="sxs-lookup"><span data-stu-id="074b7-193">Property</span></span> | <span data-ttu-id="074b7-194">Tipo</span><span class="sxs-lookup"><span data-stu-id="074b7-194">Type</span></span> | <span data-ttu-id="074b7-195">Descripción</span><span class="sxs-lookup"><span data-stu-id="074b7-195">Description</span></span> |
|:---------|:-----|:------------|
| <span data-ttu-id="074b7-196">subscriptionId</span><span class="sxs-lookup"><span data-stu-id="074b7-196">subscriptionId</span></span> | <span data-ttu-id="074b7-197">string</span><span class="sxs-lookup"><span data-stu-id="074b7-197">string</span></span> | <span data-ttu-id="074b7-198">Identificador de la suscripción que generó la notificación.</span><span class="sxs-lookup"><span data-stu-id="074b7-198">The ID of the subscription that generated the notification.</span></span> |
| <span data-ttu-id="074b7-199">subscriptionExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="074b7-199">subscriptionExpirationDateTime</span></span> | [<span data-ttu-id="074b7-200">dateTime</span><span class="sxs-lookup"><span data-stu-id="074b7-200">dateTime</span></span>](https://tools.ietf.org/html/rfc3339) | <span data-ttu-id="074b7-201">Fecha de expiración de la suscripción.</span><span class="sxs-lookup"><span data-stu-id="074b7-201">The expiration time for the subscription.</span></span> |
| <span data-ttu-id="074b7-202">clientState</span><span class="sxs-lookup"><span data-stu-id="074b7-202">clientState</span></span> | <span data-ttu-id="074b7-203">string</span><span class="sxs-lookup"><span data-stu-id="074b7-203">string</span></span> | <span data-ttu-id="074b7-204">Propiedad `clientState` especificada en la solicitud de suscripción (en su caso).</span><span class="sxs-lookup"><span data-stu-id="074b7-204">The `clientState` property specified in the subscription request (if any).</span></span> |
| <span data-ttu-id="074b7-205">changeType</span><span class="sxs-lookup"><span data-stu-id="074b7-205">changeType</span></span> | <span data-ttu-id="074b7-206">string</span><span class="sxs-lookup"><span data-stu-id="074b7-206">string</span></span> | <span data-ttu-id="074b7-207">Tipo de evento que generó la notificación.</span><span class="sxs-lookup"><span data-stu-id="074b7-207">The event type that caused the notification.</span></span> <span data-ttu-id="074b7-208">Por ejemplo, `created` al recibir un correo o `updated` al marcar un mensaje como leído.</span><span class="sxs-lookup"><span data-stu-id="074b7-208">For example, `created` on mail receive, or `updated` on marking a message read.</span></span> |
| <span data-ttu-id="074b7-209">resource</span><span class="sxs-lookup"><span data-stu-id="074b7-209">resource</span></span> | <span data-ttu-id="074b7-210">string</span><span class="sxs-lookup"><span data-stu-id="074b7-210">string</span></span> | <span data-ttu-id="074b7-211">URI del recurso relativo a `https://graph.microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="074b7-211">The URI of the resource relative to `https://graph.microsoft.com`.</span></span> |
| <span data-ttu-id="074b7-212">resourceData</span><span class="sxs-lookup"><span data-stu-id="074b7-212">resourceData</span></span> | <span data-ttu-id="074b7-213">object</span><span class="sxs-lookup"><span data-stu-id="074b7-213">object</span></span> | <span data-ttu-id="074b7-214">El contenido de esta propiedad depende del tipo de recurso al que se suscriba.</span><span class="sxs-lookup"><span data-stu-id="074b7-214">The content of this property depends on the type of resource being subscribed to.</span></span> |

<span data-ttu-id="074b7-215">Por ejemplo, para recursos de Outlook, `resourceData` contiene los siguientes campos:</span><span class="sxs-lookup"><span data-stu-id="074b7-215">For example, for Outlook resources, `resourceData` contains the following fields:</span></span>

| <span data-ttu-id="074b7-216">Propiedad</span><span class="sxs-lookup"><span data-stu-id="074b7-216">Property</span></span> | <span data-ttu-id="074b7-217">Tipo</span><span class="sxs-lookup"><span data-stu-id="074b7-217">Type</span></span> | <span data-ttu-id="074b7-218">Descripción</span><span class="sxs-lookup"><span data-stu-id="074b7-218">Description</span></span> |
|:---------|:-----|:------------|
| <span data-ttu-id="074b7-219">@odata.type</span><span class="sxs-lookup"><span data-stu-id="074b7-219">@odata.type</span></span> | <span data-ttu-id="074b7-220">string</span><span class="sxs-lookup"><span data-stu-id="074b7-220">string</span></span> | <span data-ttu-id="074b7-221">Tipo de entidad OData en Microsoft Graph que describe el objeto representado.</span><span class="sxs-lookup"><span data-stu-id="074b7-221">The OData entity type in Microsoft Graph that describes the represented object.</span></span> |
| <span data-ttu-id="074b7-222">@odata.id</span><span class="sxs-lookup"><span data-stu-id="074b7-222">@odata.id</span></span> | <span data-ttu-id="074b7-223">string</span><span class="sxs-lookup"><span data-stu-id="074b7-223">string</span></span> | <span data-ttu-id="074b7-224">Identificador OData del objeto.</span><span class="sxs-lookup"><span data-stu-id="074b7-224">The OData identifier of the object.</span></span> |
| <span data-ttu-id="074b7-225">@odata.etag</span><span class="sxs-lookup"><span data-stu-id="074b7-225">@odata.etag</span></span> | <span data-ttu-id="074b7-226">string</span><span class="sxs-lookup"><span data-stu-id="074b7-226">string</span></span> | <span data-ttu-id="074b7-227">Etiqueta de entidad HTTP que representa una versión del objeto.</span><span class="sxs-lookup"><span data-stu-id="074b7-227">The HTTP entity tag that represents the version of the object.</span></span> |
| <span data-ttu-id="074b7-228">id</span><span class="sxs-lookup"><span data-stu-id="074b7-228">id</span></span> | <span data-ttu-id="074b7-229">string</span><span class="sxs-lookup"><span data-stu-id="074b7-229">string</span></span> | <span data-ttu-id="074b7-230">Identificador del objeto.</span><span class="sxs-lookup"><span data-stu-id="074b7-230">The identifier of the object.</span></span> |

> <span data-ttu-id="074b7-231">**Nota:** El valor `id` proporcionado en `resourceData` es válido en el momento en que se genera la notificación.</span><span class="sxs-lookup"><span data-stu-id="074b7-231">**Note:** The `id` value provided in `resourceData` is valid at the time the notification was generated.</span></span> <span data-ttu-id="074b7-232">Algunas acciones, como mover un mensaje a otra carpeta, pueden dar lugar a que el `id` ya no sea válido cuando se procese la notificación.</span><span class="sxs-lookup"><span data-stu-id="074b7-232">Some actions, such as moving a message to another folder, may result in the `id` no longer being valid when the notification is processed.</span></span>

### <a name="notification-example"></a><span data-ttu-id="074b7-233">Ejemplo de notificación</span><span class="sxs-lookup"><span data-stu-id="074b7-233">Notification example</span></span>

<span data-ttu-id="074b7-234">Cuando el usuario recibe un correo electrónico, Microsoft Graph envía una notificación como la siguiente:</span><span class="sxs-lookup"><span data-stu-id="074b7-234">When the user receives an email, Microsoft Graph sends a notification like the following:</span></span>

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

<span data-ttu-id="074b7-235">Tenga en cuenta que el campo `value` es una matriz de objetos.</span><span class="sxs-lookup"><span data-stu-id="074b7-235">Note the `value` field is an array of objects.</span></span> <span data-ttu-id="074b7-236">Si hay muchas notificaciones en cola, puede que Microsoft Graph envíe varios elementos en una sola solicitud.</span><span class="sxs-lookup"><span data-stu-id="074b7-236">When there are many queued notifications, Microsoft Graph may send multiple items in a single request.</span></span> <span data-ttu-id="074b7-237">Pueden incluirse notificaciones de distintas suscripciones en una misma solicitud de notificación.</span><span class="sxs-lookup"><span data-stu-id="074b7-237">Notifications from different subscriptions can be included in the same notification request.</span></span>

### <a name="processing-the-notification"></a><span data-ttu-id="074b7-238">Procesar la notificación</span><span class="sxs-lookup"><span data-stu-id="074b7-238">Processing the notification</span></span>

<span data-ttu-id="074b7-239">Cada notificación que reciba la aplicación debe procesarse.</span><span class="sxs-lookup"><span data-stu-id="074b7-239">Each notification received by your app should be processed.</span></span> <span data-ttu-id="074b7-240">Estas son las tareas mínimas que debe realizar la aplicación para procesar una notificación:</span><span class="sxs-lookup"><span data-stu-id="074b7-240">The following are the minimum tasks that your app must perform to process a notification:</span></span>

1. <span data-ttu-id="074b7-241">Validar la propiedad `clientState`.</span><span class="sxs-lookup"><span data-stu-id="074b7-241">Validate the `clientState` property.</span></span> <span data-ttu-id="074b7-242">Debe coincidir con el valor enviado originalmente con la solicitud de creación de suscripción.</span><span class="sxs-lookup"><span data-stu-id="074b7-242">It must match the value originally submitted with the subscription creation request.</span></span>

    > <span data-ttu-id="074b7-243">**Nota:** Si no es así, no debe considerar la notificación como válida.</span><span class="sxs-lookup"><span data-stu-id="074b7-243">**Note:** If this isn't true, you should not consider this a valid notification.</span></span> <span data-ttu-id="074b7-244">Es posible que la notificación no se haya originado en Microsoft Graph y que haya sido enviada por un actor no autorizado.</span><span class="sxs-lookup"><span data-stu-id="074b7-244">It is possible that the notification has not originated from Microsoft Graph and may have been sent by a rogue actor.</span></span> <span data-ttu-id="074b7-245">También debe investigar de dónde proviene la notificación y tomar las medidas adecuadas.</span><span class="sxs-lookup"><span data-stu-id="074b7-245">You should also investigate where the notification comes from and take appropriate action.</span></span>

1. <span data-ttu-id="074b7-246">Actualizar la aplicación según la lógica empresarial.</span><span class="sxs-lookup"><span data-stu-id="074b7-246">Update your application based on your business logic.</span></span>

1. <span data-ttu-id="074b7-247">Enviar un código de estado `202 - Accepted` en la respuesta a Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="074b7-247">Send a `202 - Accepted` status code in your response to Microsoft Graph.</span></span> <span data-ttu-id="074b7-248">Si Microsoft Graph no recibe un código de clase 2xx, intentará volver a enviar la notificación varias veces.</span><span class="sxs-lookup"><span data-stu-id="074b7-248">If Microsoft Graph doesn't receive a 2xx class code, it will retry the notification a number of times.</span></span>

    > <span data-ttu-id="074b7-249">**Nota:** Debe enviar un código de estado `202 - Accepted`, aunque la propiedad `clientState` no coincida con la enviada en la solicitud de suscripción.</span><span class="sxs-lookup"><span data-stu-id="074b7-249">**Note:** You should send a `202 - Accepted` status code even if the `clientState` property doesn't match the one submitted with the subscription request.</span></span> <span data-ttu-id="074b7-250">Esto es recomendable, ya que evita que un posible actor no autorizado descubra que tal vez usted no confíe en sus notificaciones y usar esta información para adivinar el valor de la propiedad `clientState`.</span><span class="sxs-lookup"><span data-stu-id="074b7-250">This is a good practice as it prevents a potential rogue actor from discovering the fact that you may not trust their notifications, and perhaps using that information to guess the value of the `clientState` property.</span></span>

<span data-ttu-id="074b7-251">Repita esto para otras notificaciones de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="074b7-251">Repeat for other notifications in the request.</span></span>

## <a name="code-samples"></a><span data-ttu-id="074b7-252">Ejemplos de código</span><span class="sxs-lookup"><span data-stu-id="074b7-252">Code samples</span></span>

<span data-ttu-id="074b7-253">Los siguientes ejemplos de código están disponibles en GitHub.</span><span class="sxs-lookup"><span data-stu-id="074b7-253">The following code samples are available on GitHub.</span></span>

- [<span data-ttu-id="074b7-254">Ejemplo de webhooks de Microsoft Graph para Node.js</span><span class="sxs-lookup"><span data-stu-id="074b7-254">Microsoft Graph Webhooks Sample for Node.js</span></span>](https://github.com/OfficeDev/Microsoft-Graph-Nodejs-Webhooks)
- [<span data-ttu-id="074b7-255">Ejemplo de webhooks de Microsoft Graph para ASP.NET</span><span class="sxs-lookup"><span data-stu-id="074b7-255">Microsoft Graph Webhooks Sample for ASP.NET</span></span>](https://github.com/OfficeDev/Microsoft-Graph-ASPNET-Webhooks)
- [<span data-ttu-id="074b7-256">Ejemplo de webhooks de usuario de Microsoft Graph con WebJobs SDK</span><span class="sxs-lookup"><span data-stu-id="074b7-256">Microsoft Graph User Webhooks Sample using WebJobs SDK</span></span>](https://github.com/microsoftgraph/webjobs-webhooks-sample)

## <a name="see-also"></a><span data-ttu-id="074b7-257">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="074b7-257">See also</span></span>

- [<span data-ttu-id="074b7-258">Tipo de recurso de suscripción</span><span class="sxs-lookup"><span data-stu-id="074b7-258">Subscription resource type</span></span>](/graph/api/resources/subscription?view=graph-rest-1.0)
- [<span data-ttu-id="074b7-259">Obtener suscripción</span><span class="sxs-lookup"><span data-stu-id="074b7-259">Get subscription</span></span>](/graph/api/subscription-get?view=graph-rest-1.0)
- [<span data-ttu-id="074b7-260">Crear suscripción</span><span class="sxs-lookup"><span data-stu-id="074b7-260">Create subscription</span></span>](/graph/api/subscription-post-subscriptions?view=graph-rest-1.0)

[contact]: /graph/api/resources/contact?view=graph-rest-1.0
[conversation]: /graph/api/resources/conversation?view=graph-rest-1.0
[drive]: /graph/api/resources/drive?view=graph-rest-1.0
[event]: /graph/api/resources/event?view=graph-rest-1.0
[message]: /graph/api/resources/message?view=graph-rest-1.0
