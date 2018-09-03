# <a name="subscription-resource-type"></a><span data-ttu-id="e795b-101">Tipo de recurso subscription</span><span class="sxs-lookup"><span data-stu-id="e795b-101">Subscription resource type</span></span>

<span data-ttu-id="e795b-102">Una suscripción permite que una aplicación cliente reciba notificaciones sobre cambios en datos de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="e795b-102">A subscription allows a client app to receive notifications about data on the Microsoft Graph.</span></span> <span data-ttu-id="e795b-103">Actualmente, las suscripciones están habilitadas para los siguientes recursos:</span><span class="sxs-lookup"><span data-stu-id="e795b-103">Currently, subscriptions are enabled for the following datasets:</span></span>

- <span data-ttu-id="e795b-104">Correo, eventos y contactos de Outlook</span><span class="sxs-lookup"><span data-stu-id="e795b-104">Mail, events, and contacts from Outlook</span></span>
- <span data-ttu-id="e795b-105">Conversaciones de los grupos de Office</span><span class="sxs-lookup"><span data-stu-id="e795b-105">Conversations from Office Groups.</span></span>
- <span data-ttu-id="e795b-106">Elementos raíz de la unidad de OneDrive</span><span class="sxs-lookup"><span data-stu-id="e795b-106">Drive root items from OneDrive</span></span>
- <span data-ttu-id="e795b-107">Usuarios y grupos de Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="e795b-107">Users and Groups from Azure Active Directory</span></span>

## <a name="json-representation"></a><span data-ttu-id="e795b-108">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e795b-108">JSON representation</span></span>

<span data-ttu-id="e795b-109">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e795b-109">Here is a JSON representation of the resource.</span></span>

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

## <a name="properties"></a><span data-ttu-id="e795b-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e795b-110">Properties</span></span>

| <span data-ttu-id="e795b-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e795b-111">Property</span></span> | <span data-ttu-id="e795b-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="e795b-112">Type</span></span> | <span data-ttu-id="e795b-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="e795b-113">Description</span></span> |
|:---------|:-----|:------------|
| <span data-ttu-id="e795b-114">changeType</span><span class="sxs-lookup"><span data-stu-id="e795b-114">changeType</span></span> | <span data-ttu-id="e795b-115">cadena</span><span class="sxs-lookup"><span data-stu-id="e795b-115">string</span></span> | <span data-ttu-id="e795b-116">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e795b-116">Required.</span></span> <span data-ttu-id="e795b-117">Indica el tipo de cambio en el recurso suscrito que generará una notificación.</span><span class="sxs-lookup"><span data-stu-id="e795b-117">Indicates the type of change in the subscribed resource that will raise a notification.</span></span> <span data-ttu-id="e795b-118">Los valores admitidos son: `created`, `updated`, `deleted`.</span><span class="sxs-lookup"><span data-stu-id="e795b-118">The supported values are: `created`, `updated`, `deleted`.</span></span> <span data-ttu-id="e795b-119">Se pueden combinar varios valores mediante una lista separada por comas.</span><span class="sxs-lookup"><span data-stu-id="e795b-119">Multiple values can be combined using a comma-separated list.</span></span><br><br><span data-ttu-id="e795b-120">Nota: Las notificaciones de elemento de raíz de unidad solo son compatibles con `updated` changeType.</span><span class="sxs-lookup"><span data-stu-id="e795b-120">Note: Drive root item notifications support only the `updated` changeType.</span></span> <span data-ttu-id="e795b-121">Las notificaciones de usuario y de grupo admiten `updated` y `deleted` changeType.</span><span class="sxs-lookup"><span data-stu-id="e795b-121">User and group notifications support `updated` and `deleted` changeType.</span></span>|
| <span data-ttu-id="e795b-122">notificationUrl</span><span class="sxs-lookup"><span data-stu-id="e795b-122">notificationUrl</span></span> | <span data-ttu-id="e795b-123">cadena</span><span class="sxs-lookup"><span data-stu-id="e795b-123">string</span></span> | <span data-ttu-id="e795b-124">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e795b-124">Required.</span></span> <span data-ttu-id="e795b-125">La dirección URL del extremo que va a recibir las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="e795b-125">The URL of the application that will receive the push notifications.</span></span> <span data-ttu-id="e795b-126">Esta dirección URL debe hacer uso del protocolo HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e795b-126">This URL must make use of the HTTPS protocol.</span></span> |
| <span data-ttu-id="e795b-127">resource</span><span class="sxs-lookup"><span data-stu-id="e795b-127">resource</span></span> | <span data-ttu-id="e795b-128">cadena</span><span class="sxs-lookup"><span data-stu-id="e795b-128">string</span></span> | <span data-ttu-id="e795b-129">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e795b-129">Required.</span></span> <span data-ttu-id="e795b-130">Especifica el recurso del que se supervisarán los cambios.</span><span class="sxs-lookup"><span data-stu-id="e795b-130">Specifies the resource that will be monitored for changes. Do not include the base URL ("https://graph.microsoft.com/v1.0/").</span></span> <span data-ttu-id="e795b-131">No incluya la dirección URL base (`https://graph.microsoft.com/v1.0/`).</span><span class="sxs-lookup"><span data-stu-id="e795b-131">Do not include the base URL (`https://graph.microsoft.com/v1.0/`).</span></span> |
| <span data-ttu-id="e795b-132">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="e795b-132">expirationDateTime</span></span> | [<span data-ttu-id="e795b-133">dateTime</span><span class="sxs-lookup"><span data-stu-id="e795b-133">dateTime</span></span>](http://tools.ietf.org/html/rfc3339) | <span data-ttu-id="e795b-134">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e795b-134">Required.</span></span> <span data-ttu-id="e795b-135">Especifica la fecha y hora en que expira la suscripción de webhook.</span><span class="sxs-lookup"><span data-stu-id="e795b-135">Specifies the date and time when the webhook subscription expires.</span></span> <span data-ttu-id="e795b-136">La hora está en UTC y puede ser un periodo de tiempo desde la creación de la suscripción que varía para el recurso al que se está suscrito.</span><span class="sxs-lookup"><span data-stu-id="e795b-136">The time is in UTC, and can be an amount of time from subscription creation that varies for the resource subscribed to.</span></span>  <span data-ttu-id="e795b-137">Consulte la tabla siguiente para la duración máxima de la suscripción compatible.</span><span class="sxs-lookup"><span data-stu-id="e795b-137">See the table below for maximum supported subscription length of time.</span></span> |
| <span data-ttu-id="e795b-138">clientState</span><span class="sxs-lookup"><span data-stu-id="e795b-138">clientState</span></span> | <span data-ttu-id="e795b-139">cadena</span><span class="sxs-lookup"><span data-stu-id="e795b-139">string</span></span> | <span data-ttu-id="e795b-140">Opcional.</span><span class="sxs-lookup"><span data-stu-id="e795b-140">Optional.</span></span> <span data-ttu-id="e795b-141">Especifica el valor de la propiedad `clientState` enviado por el servicio en cada notificación.</span><span class="sxs-lookup"><span data-stu-id="e795b-141">Specifies the value of the `clientState` property sent by the service in each notification.</span></span> <span data-ttu-id="e795b-142">Se permite una longitud máxima de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="e795b-142">The maximum length is 128 characters.</span></span> <span data-ttu-id="e795b-143">El cliente puede comprobar que la notificación viene del servicio si compara el valor de la propiedad `clientState` enviado con la suscripción con el valor de la propiedad `clientState` recibido con cada notificación.</span><span class="sxs-lookup"><span data-stu-id="e795b-143">The client can check that the notification came from the service by comparing the value of the `clientState` property sent with the subscription with the value of the `clientState` property received with each notification.</span></span> |
| <span data-ttu-id="e795b-144">identificador</span><span class="sxs-lookup"><span data-stu-id="e795b-144">id</span></span> | <span data-ttu-id="e795b-145">cadena</span><span class="sxs-lookup"><span data-stu-id="e795b-145">string</span></span> | <span data-ttu-id="e795b-p108">Identificador único de la suscripción. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e795b-p108">Unique identifier for the subscription. Read-only.</span></span> |
| <span data-ttu-id="e795b-148">applicationId</span><span class="sxs-lookup"><span data-stu-id="e795b-148">applicationId</span></span> | <span data-ttu-id="e795b-149">cadena</span><span class="sxs-lookup"><span data-stu-id="e795b-149">string</span></span> | <span data-ttu-id="e795b-150">Identificador de la aplicación utilizada para crear la suscripción.</span><span class="sxs-lookup"><span data-stu-id="e795b-150">Identifier of the application used to create the subscription.</span></span> <span data-ttu-id="e795b-151">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e795b-151">Read-only.</span></span> |
| <span data-ttu-id="e795b-152">creatorId</span><span class="sxs-lookup"><span data-stu-id="e795b-152">creatorId</span></span> | <span data-ttu-id="e795b-153">cadena</span><span class="sxs-lookup"><span data-stu-id="e795b-153">string</span></span> | <span data-ttu-id="e795b-154">Identificador del usuario o de la entidad de seguridad de servicio que creó la suscripción.</span><span class="sxs-lookup"><span data-stu-id="e795b-154">Identifier of the user or service principal that created the subscription.</span></span> <span data-ttu-id="e795b-155">Si la aplicación usada ha delegado permisos para crear la suscripción, este campo contiene el identificador del usuario que ha iniciado sesión en cuyo nombre llama la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e795b-155">If the app used delegated permissions to create the subscription, this field contains the id of the signed-in user the app called on behalf of.</span></span> <span data-ttu-id="e795b-156">Si la aplicación usa los permisos de aplicación, este campo contiene el identificador de la entidad de seguridad de servicio correspondiente a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e795b-156">If the app used application permissions, this field contains the id of the service principal corresponding to the app.</span></span> <span data-ttu-id="e795b-157">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e795b-157">Read-only.</span></span> |

## <a name="maximum-length-of-subscription-per-resource-type"></a><span data-ttu-id="e795b-158">Duración máxima de la suscripción por tipo de recurso</span><span class="sxs-lookup"><span data-stu-id="e795b-158">Maximum length of subscription per resource type</span></span>

| <span data-ttu-id="e795b-159">Recurso</span><span class="sxs-lookup"><span data-stu-id="e795b-159">Resource</span></span>            | <span data-ttu-id="e795b-160">Tiempo de expiración máximo</span><span class="sxs-lookup"><span data-stu-id="e795b-160">Maximum Expiration Time</span></span>  |
|:--------------------|:-------------------------|
| <span data-ttu-id="e795b-161">Correo</span><span class="sxs-lookup"><span data-stu-id="e795b-161">Mail</span></span>                | <span data-ttu-id="e795b-162">4320 minutos (3 días)</span><span class="sxs-lookup"><span data-stu-id="e795b-162">4320 minutes (3 days)</span></span>    |
| <span data-ttu-id="e795b-163">Calendario</span><span class="sxs-lookup"><span data-stu-id="e795b-163">Calendar</span></span>            | <span data-ttu-id="e795b-164">4320 minutos (3 días)</span><span class="sxs-lookup"><span data-stu-id="e795b-164">4320 minutes (3 days)</span></span>    |
| <span data-ttu-id="e795b-165">Contactos</span><span class="sxs-lookup"><span data-stu-id="e795b-165">Contacts</span></span>            | <span data-ttu-id="e795b-166">4320 minutos (3 días)</span><span class="sxs-lookup"><span data-stu-id="e795b-166">4320 minutes (3 days)</span></span>    |
| <span data-ttu-id="e795b-167">Conversaciones de grupo</span><span class="sxs-lookup"><span data-stu-id="e795b-167">Group conversations</span></span> | <span data-ttu-id="e795b-168">4320 minutos (3 días)</span><span class="sxs-lookup"><span data-stu-id="e795b-168">4320 minutes (3 days)</span></span>    |
| <span data-ttu-id="e795b-169">Elementos raíz de la unidad</span><span class="sxs-lookup"><span data-stu-id="e795b-169">Drive root items</span></span>    | <span data-ttu-id="e795b-170">4320 minutos (3 días)</span><span class="sxs-lookup"><span data-stu-id="e795b-170">4320 minutes (3 days)</span></span> |

> <span data-ttu-id="e795b-171">**Nota:** Las nuevas aplicaciones y las aplicaciones existentes no deben superar el valor admitido.</span><span class="sxs-lookup"><span data-stu-id="e795b-171">Existing applications and new applications should not exceed the supported value.</span></span> <span data-ttu-id="e795b-172">En el futuro, se producirá un error en las solicitudes para crear o renovar una suscripción más allá del valor máximo.</span><span class="sxs-lookup"><span data-stu-id="e795b-172">In the future, any requests to create or renew a subscription beyond the maximum value will fail.</span></span>

## <a name="relationships"></a><span data-ttu-id="e795b-173">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e795b-173">Relationships</span></span>

<span data-ttu-id="e795b-174">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e795b-174">None</span></span>

## <a name="methods"></a><span data-ttu-id="e795b-175">Métodos</span><span class="sxs-lookup"><span data-stu-id="e795b-175">Methods</span></span>

| <span data-ttu-id="e795b-176">Método</span><span class="sxs-lookup"><span data-stu-id="e795b-176">Method</span></span> | <span data-ttu-id="e795b-177">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e795b-177">Return Type</span></span> | <span data-ttu-id="e795b-178">Descripción</span><span class="sxs-lookup"><span data-stu-id="e795b-178">Description</span></span> |
|:-------|:------------|:------------|
| [<span data-ttu-id="e795b-179">Crear suscripción</span><span class="sxs-lookup"><span data-stu-id="e795b-179">Create subscription</span></span>](../api/subscription_post_subscriptions.md) | [<span data-ttu-id="e795b-180">subscription</span><span class="sxs-lookup"><span data-stu-id="e795b-180">subscription</span></span>](subscription.md) | <span data-ttu-id="e795b-181">Suscripción a una aplicación de escucha para recibir notificaciones cuando cambian los datos de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="e795b-181">Subscribes a listener application to receive notifications when Microsoft Graph data changes.</span></span> |
| [<span data-ttu-id="e795b-182">Actualizar suscripción</span><span class="sxs-lookup"><span data-stu-id="e795b-182">Update subscription</span></span>](../api/subscription_update.md) | [<span data-ttu-id="e795b-183">subscription</span><span class="sxs-lookup"><span data-stu-id="e795b-183">subscription</span></span>](subscription.md) | <span data-ttu-id="e795b-184">Renueva una suscripción al actualizar su tiempo de expiración.</span><span class="sxs-lookup"><span data-stu-id="e795b-184">Renews a subscription by updating its expiration time.</span></span> |
| [<span data-ttu-id="e795b-185">Listar subscripciones</span><span class="sxs-lookup"><span data-stu-id="e795b-185">List subscriptions</span></span>](../api/subscription_list.md) | [<span data-ttu-id="e795b-186">subscription</span><span class="sxs-lookup"><span data-stu-id="e795b-186">subscription</span></span>](subscription.md) | <span data-ttu-id="e795b-187">Listas de suscripciones activas.</span><span class="sxs-lookup"><span data-stu-id="e795b-187">Lists active subscriptions.</span></span> |
| [<span data-ttu-id="e795b-188">Obtener suscripción</span><span class="sxs-lookup"><span data-stu-id="e795b-188">Get subscription</span></span>](../api/subscription_get.md) | [<span data-ttu-id="e795b-189">subscription</span><span class="sxs-lookup"><span data-stu-id="e795b-189">subscription</span></span>](subscription.md) | <span data-ttu-id="e795b-190">Lee las propiedades y relaciones del objeto subscription.</span><span class="sxs-lookup"><span data-stu-id="e795b-190">Reads properties and relationships of subscription object.</span></span> |
| [<span data-ttu-id="e795b-191">Eliminar suscripción</span><span class="sxs-lookup"><span data-stu-id="e795b-191">Delete subscription</span></span>](../api/subscription_delete.md) | <span data-ttu-id="e795b-192">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e795b-192">None</span></span> |<span data-ttu-id="e795b-193">Elimina un objeto subscription.</span><span class="sxs-lookup"><span data-stu-id="e795b-193">Deletes a subscription object.</span></span> |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "subscription resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
