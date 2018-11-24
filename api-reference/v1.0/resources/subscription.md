# <a name="subscription-resource-type"></a><span data-ttu-id="c1ed9-101">tipo de recurso de suscripción</span><span class="sxs-lookup"><span data-stu-id="c1ed9-101">subscription resource type</span></span>

<span data-ttu-id="c1ed9-102">Una suscripción a permite que una aplicación de cliente recibir notificaciones sobre cambios en los datos en Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-102">A subscription allows a client app to receive notifications about changes to data in Microsoft Graph.</span></span> <span data-ttu-id="c1ed9-103">Actualmente, las suscripciones están habilitadas para los siguientes recursos:</span><span class="sxs-lookup"><span data-stu-id="c1ed9-103">Currently, subscriptions are enabled for the following resources:</span></span>

- <span data-ttu-id="c1ed9-104">Correo, eventos y los contactos de Outlook.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-104">Mail, events, and contacts from Outlook.</span></span>
- <span data-ttu-id="c1ed9-105">Conversaciones de los grupos de Office.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-105">Conversations from Office Groups.</span></span>
- <span data-ttu-id="c1ed9-106">Los elementos raíz de unidad de OneDrive.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-106">Drive root items from OneDrive.</span></span>
- <span data-ttu-id="c1ed9-107">Los usuarios y grupos de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-107">Users and Groups from Azure Active Directory.</span></span>
- <span data-ttu-id="c1ed9-108">Alertas de la API de seguridad de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-108">Alerts from the Microsoft Graph Security API.</span></span>

## <a name="json-representation"></a><span data-ttu-id="c1ed9-109">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c1ed9-109">JSON representation</span></span>

<span data-ttu-id="c1ed9-110">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-110">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.subscription",
  "@odata.annotations": [
    {
      "capabilities": {
        "skippable": false,
        "toppable": false,
        "countable": false,
        "expandable": false,
        "filterable": false,
        "referenceable": false,
        "selectable": false,
        "sortable": false
      }
    }
  ]
}-->

```json
{
  "changeType": "string",
  "notificationUrl": "string",
  "resource": "string",
  "applicationId" : "string",
  "expirationDateTime": "String (timestamp)",
  "id": "string (identifier)",
  "clientState": "string",
  "creatorId": "string"
}
```

## <a name="properties"></a><span data-ttu-id="c1ed9-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c1ed9-111">Properties</span></span>

| <span data-ttu-id="c1ed9-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c1ed9-112">Property</span></span> | <span data-ttu-id="c1ed9-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="c1ed9-113">Type</span></span> | <span data-ttu-id="c1ed9-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1ed9-114">Description</span></span> |
|:---------|:-----|:------------|
| <span data-ttu-id="c1ed9-115">changeType</span><span class="sxs-lookup"><span data-stu-id="c1ed9-115">changeType</span></span> | <span data-ttu-id="c1ed9-116">string</span><span class="sxs-lookup"><span data-stu-id="c1ed9-116">string</span></span> | <span data-ttu-id="c1ed9-117">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-117">Required.</span></span> <span data-ttu-id="c1ed9-118">Indica el tipo de cambio en el recurso suscrito que generará una notificación.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-118">Indicates the type of change in the subscribed resource that will raise a notification.</span></span> <span data-ttu-id="c1ed9-119">Los valores admitidos son: `created`, `updated`, `deleted`.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-119">The supported values are: `created`, `updated`, `deleted`.</span></span> <span data-ttu-id="c1ed9-120">Se pueden combinar varios valores mediante una lista separada por comas.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-120">Multiple values can be combined using a comma-separated list.</span></span><br><br><span data-ttu-id="c1ed9-121">Nota: Las notificaciones de elemento de raíz de unidad sólo son compatibles con el `updated` changeType.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-121">Note: Drive root item notifications support only the `updated` changeType.</span></span> <span data-ttu-id="c1ed9-122">Admiten notificaciones de usuario y de grupo `updated` y `deleted` changeType.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-122">User and group notifications support `updated` and `deleted` changeType.</span></span>|
| <span data-ttu-id="c1ed9-123">notificationUrl</span><span class="sxs-lookup"><span data-stu-id="c1ed9-123">notificationUrl</span></span> | <span data-ttu-id="c1ed9-124">string</span><span class="sxs-lookup"><span data-stu-id="c1ed9-124">string</span></span> | <span data-ttu-id="c1ed9-125">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-125">Required.</span></span> <span data-ttu-id="c1ed9-126">La dirección URL del extremo que va a recibir las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-126">The URL of the endpoint that will receive the notifications.</span></span> <span data-ttu-id="c1ed9-127">Esta dirección URL debe hacer uso de la HTTPS protocolo.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-127">This URL must make use of the HTTPS protocol.</span></span> |
| <span data-ttu-id="c1ed9-128">resource</span><span class="sxs-lookup"><span data-stu-id="c1ed9-128">resource</span></span> | <span data-ttu-id="c1ed9-129">string</span><span class="sxs-lookup"><span data-stu-id="c1ed9-129">string</span></span> | <span data-ttu-id="c1ed9-130">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-130">Required.</span></span> <span data-ttu-id="c1ed9-131">Especifica el recurso al que se van a supervisar para que los cambios.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-131">Specifies the resource that will be monitored for changes.</span></span> <span data-ttu-id="c1ed9-132">No incluya la dirección URL base (`https://graph.microsoft.com/v1.0/`).</span><span class="sxs-lookup"><span data-stu-id="c1ed9-132">Do not include the base URL (`https://graph.microsoft.com/v1.0/`).</span></span> |
| <span data-ttu-id="c1ed9-133">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="c1ed9-133">expirationDateTime</span></span> | [<span data-ttu-id="c1ed9-134">dateTime</span><span class="sxs-lookup"><span data-stu-id="c1ed9-134">dateTime</span></span>](https://tools.ietf.org/html/rfc3339) | <span data-ttu-id="c1ed9-135">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-135">Required.</span></span> <span data-ttu-id="c1ed9-136">Especifica la fecha y hora en que expira la suscripción de webhook.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-136">Specifies the date and time when the webhook subscription expires.</span></span> <span data-ttu-id="c1ed9-137">La hora está en UTC y puede ser un periodo de tiempo desde la creación de la suscripción que varía para el recurso al que se está suscrito.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-137">The time is in UTC, and can be an amount of time from subscription creation that varies for the resource subscribed to.</span></span>  <span data-ttu-id="c1ed9-138">Consulte la tabla siguiente para la duración máxima de la suscripción compatible.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-138">See the table below for maximum supported subscription length of time.</span></span> |
| <span data-ttu-id="c1ed9-139">clientState</span><span class="sxs-lookup"><span data-stu-id="c1ed9-139">clientState</span></span> | <span data-ttu-id="c1ed9-140">string</span><span class="sxs-lookup"><span data-stu-id="c1ed9-140">string</span></span> | <span data-ttu-id="c1ed9-141">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-141">Optional.</span></span> <span data-ttu-id="c1ed9-142">Especifica el valor de la propiedad `clientState` enviado por el servicio en cada notificación.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-142">Specifies the value of the `clientState` property sent by the service in each notification.</span></span> <span data-ttu-id="c1ed9-143">Se permite una longitud máxima de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-143">The maximum length is 128 characters.</span></span> <span data-ttu-id="c1ed9-144">El cliente puede comprobar que la notificación viene del servicio si compara el valor de la propiedad `clientState` enviado con la suscripción con el valor de la propiedad `clientState` recibido con cada notificación.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-144">The client can check that the notification came from the service by comparing the value of the `clientState` property sent with the subscription with the value of the `clientState` property received with each notification.</span></span> |
| <span data-ttu-id="c1ed9-145">identificador</span><span class="sxs-lookup"><span data-stu-id="c1ed9-145">id</span></span> | <span data-ttu-id="c1ed9-146">string</span><span class="sxs-lookup"><span data-stu-id="c1ed9-146">string</span></span> | <span data-ttu-id="c1ed9-p108">Identificador único de la suscripción. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-p108">Unique identifier for the subscription. Read-only.</span></span> |
| <span data-ttu-id="c1ed9-149">applicationId</span><span class="sxs-lookup"><span data-stu-id="c1ed9-149">applicationId</span></span> | <span data-ttu-id="c1ed9-150">string</span><span class="sxs-lookup"><span data-stu-id="c1ed9-150">string</span></span> | <span data-ttu-id="c1ed9-151">Identificador de la aplicación utilizada para crear la suscripción.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-151">Identifier of the application used to create the subscription.</span></span> <span data-ttu-id="c1ed9-152">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-152">Read-only.</span></span> |
| <span data-ttu-id="c1ed9-153">Creador de</span><span class="sxs-lookup"><span data-stu-id="c1ed9-153">creatorId</span></span> | <span data-ttu-id="c1ed9-154">string</span><span class="sxs-lookup"><span data-stu-id="c1ed9-154">string</span></span> | <span data-ttu-id="c1ed9-155">Identificador del usuario o de la entidad de seguridad de servicio que creó la suscripción.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-155">Identifier of the user or service principal that created the subscription.</span></span> <span data-ttu-id="c1ed9-156">Si la aplicación usada delegado permisos para crear la suscripción, este campo contiene el identificador del usuario ha iniciado sesión de que la aplicación llama en nombre.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-156">If the app used delegated permissions to create the subscription, this field contains the id of the signed-in user the app called on behalf of.</span></span> <span data-ttu-id="c1ed9-157">Si la aplicación usa los permisos de aplicación, este campo contiene el identificador de la entidad de seguridad de servicio correspondiente a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-157">If the app used application permissions, this field contains the id of the service principal corresponding to the app.</span></span> <span data-ttu-id="c1ed9-158">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-158">Read-only.</span></span> |

## <a name="maximum-length-of-subscription-per-resource-type"></a><span data-ttu-id="c1ed9-159">Duración máxima de la suscripción por tipo de recurso</span><span class="sxs-lookup"><span data-stu-id="c1ed9-159">Maximum length of subscription per resource type</span></span>

| <span data-ttu-id="c1ed9-160">Recurso</span><span class="sxs-lookup"><span data-stu-id="c1ed9-160">Resource</span></span>            | <span data-ttu-id="c1ed9-161">Tiempo de expiración máximo</span><span class="sxs-lookup"><span data-stu-id="c1ed9-161">Maximum Expiration Time</span></span>  |
|:--------------------|:-------------------------|
| <span data-ttu-id="c1ed9-162">Correo</span><span class="sxs-lookup"><span data-stu-id="c1ed9-162">Mail</span></span>                | <span data-ttu-id="c1ed9-163">4230 minutos (en 3 días)</span><span class="sxs-lookup"><span data-stu-id="c1ed9-163">4230 minutes (under 3 days)</span></span>    |
| <span data-ttu-id="c1ed9-164">Calendario</span><span class="sxs-lookup"><span data-stu-id="c1ed9-164">Calendar</span></span>            | <span data-ttu-id="c1ed9-165">4230 minutos (en 3 días)</span><span class="sxs-lookup"><span data-stu-id="c1ed9-165">4230 minutes (under 3 days)</span></span>    |
| <span data-ttu-id="c1ed9-166">Contactos</span><span class="sxs-lookup"><span data-stu-id="c1ed9-166">Contacts</span></span>            | <span data-ttu-id="c1ed9-167">4230 minutos (en 3 días)</span><span class="sxs-lookup"><span data-stu-id="c1ed9-167">4230 minutes (under 3 days)</span></span>    |
| <span data-ttu-id="c1ed9-168">Conversaciones de grupo</span><span class="sxs-lookup"><span data-stu-id="c1ed9-168">Group conversations</span></span> | <span data-ttu-id="c1ed9-169">4230 minutos (en 3 días)</span><span class="sxs-lookup"><span data-stu-id="c1ed9-169">4230 minutes (under 3 days)</span></span>    |
| <span data-ttu-id="c1ed9-170">Elementos raíz de la unidad</span><span class="sxs-lookup"><span data-stu-id="c1ed9-170">Drive root items</span></span>    | <span data-ttu-id="c1ed9-171">4230 minutos (en 3 días)</span><span class="sxs-lookup"><span data-stu-id="c1ed9-171">4230 minutes (under 3 days)</span></span>    |
| <span data-ttu-id="c1ed9-172">Alertas de seguridad</span><span class="sxs-lookup"><span data-stu-id="c1ed9-172">Security alerts</span></span>     | <span data-ttu-id="c1ed9-173">43200 minutos (en 30 días)</span><span class="sxs-lookup"><span data-stu-id="c1ed9-173">43200 minutes (under 30 days)</span></span>  |

> <span data-ttu-id="c1ed9-174">**Nota:** Las aplicaciones existentes y nuevas aplicaciones no deben superar el valor admitido.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-174">**Note:** Existing applications and new applications should not exceed the supported value.</span></span> <span data-ttu-id="c1ed9-175">En el futuro, se producirá un error en las solicitudes para crear o renovar una suscripción más allá del valor máximo.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-175">In the future, any requests to create or renew a subscription beyond the maximum value will fail.</span></span>

## <a name="relationships"></a><span data-ttu-id="c1ed9-176">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c1ed9-176">Relationships</span></span>

<span data-ttu-id="c1ed9-177">Ninguno</span><span class="sxs-lookup"><span data-stu-id="c1ed9-177">None</span></span>

## <a name="methods"></a><span data-ttu-id="c1ed9-178">Métodos</span><span class="sxs-lookup"><span data-stu-id="c1ed9-178">Methods</span></span>

| <span data-ttu-id="c1ed9-179">Método</span><span class="sxs-lookup"><span data-stu-id="c1ed9-179">Method</span></span> | <span data-ttu-id="c1ed9-180">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c1ed9-180">Return Type</span></span> | <span data-ttu-id="c1ed9-181">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1ed9-181">Description</span></span> |
|:-------|:------------|:------------|
| [<span data-ttu-id="c1ed9-182">Crear suscripción</span><span class="sxs-lookup"><span data-stu-id="c1ed9-182">Create subscription</span></span>](../api/subscription_post_subscriptions.md) | [<span data-ttu-id="c1ed9-183">subscription</span><span class="sxs-lookup"><span data-stu-id="c1ed9-183">subscription</span></span>](subscription.md) | <span data-ttu-id="c1ed9-184">Suscripción a una aplicación de escucha para recibir notificaciones cuando cambian los datos de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-184">Subscribes a listener application to receive notifications when Microsoft Graph data changes.</span></span> |
| [<span data-ttu-id="c1ed9-185">Actualizar suscripción</span><span class="sxs-lookup"><span data-stu-id="c1ed9-185">Update subscription</span></span>](../api/subscription_update.md) | [<span data-ttu-id="c1ed9-186">subscription</span><span class="sxs-lookup"><span data-stu-id="c1ed9-186">subscription</span></span>](subscription.md) | <span data-ttu-id="c1ed9-187">Renueva una suscripción al actualizar su tiempo de expiración.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-187">Renews a subscription by updating its expiration time.</span></span> |
| [<span data-ttu-id="c1ed9-188">Suscripciones de lista</span><span class="sxs-lookup"><span data-stu-id="c1ed9-188">List subscriptions</span></span>](../api/subscription_list.md) | [<span data-ttu-id="c1ed9-189">subscription</span><span class="sxs-lookup"><span data-stu-id="c1ed9-189">subscription</span></span>](subscription.md) | <span data-ttu-id="c1ed9-190">Listas de suscripciones activas.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-190">Lists active subscriptions.</span></span> |
| [<span data-ttu-id="c1ed9-191">Obtener suscripción</span><span class="sxs-lookup"><span data-stu-id="c1ed9-191">Get subscription</span></span>](../api/subscription_get.md) | [<span data-ttu-id="c1ed9-192">subscription</span><span class="sxs-lookup"><span data-stu-id="c1ed9-192">subscription</span></span>](subscription.md) | <span data-ttu-id="c1ed9-193">Lee las propiedades y relaciones del objeto subscription.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-193">Reads properties and relationships of subscription object.</span></span> |
| [<span data-ttu-id="c1ed9-194">Eliminar suscripción</span><span class="sxs-lookup"><span data-stu-id="c1ed9-194">Delete subscription</span></span>](../api/subscription_delete.md) | <span data-ttu-id="c1ed9-195">Ninguno</span><span class="sxs-lookup"><span data-stu-id="c1ed9-195">None</span></span> |<span data-ttu-id="c1ed9-196">Elimina un objeto subscription.</span><span class="sxs-lookup"><span data-stu-id="c1ed9-196">Deletes a subscription object.</span></span> |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "subscription resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
