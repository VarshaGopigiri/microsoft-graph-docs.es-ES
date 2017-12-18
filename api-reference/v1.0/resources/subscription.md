# <a name="subscription-resource-type"></a><span data-ttu-id="28090-101">Tipo de recurso Subscription</span><span class="sxs-lookup"><span data-stu-id="28090-101">Subscription Resource Type</span></span>
<span data-ttu-id="28090-102">Una suscripción permite que una aplicación cliente reciba notificaciones sobre los datos de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="28090-102">A subscription allows a client app to receive notifications about data on the Microsoft Graph. Currently subscriptions are enabled for the following datasets:</span></span> <span data-ttu-id="28090-103">Actualmente las suscripciones están habilitadas para los conjuntos de datos siguientes:</span><span class="sxs-lookup"><span data-stu-id="28090-103">Currently, subscriptions are enabled for the following datasets:</span></span>

1. <span data-ttu-id="28090-104">Correo, eventos y contactos de Outlook</span><span class="sxs-lookup"><span data-stu-id="28090-104">Mail, events, and contacts from Outlook</span></span>
1. <span data-ttu-id="28090-105">Conversaciones de los grupos de Office.</span><span class="sxs-lookup"><span data-stu-id="28090-105">Conversations from Office Groups.</span></span>
1. <span data-ttu-id="28090-106">Elementos raíz de la unidad de OneDrive</span><span class="sxs-lookup"><span data-stu-id="28090-106">Drive root items from OneDrive</span></span> 


## <a name="json-representation"></a><span data-ttu-id="28090-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="28090-107">JSON representation</span></span>

<span data-ttu-id="28090-108">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="28090-108">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.subscription"
}-->

```json
{
  "changeType": "string",
  "notificationUrl": "string",
  "resource": "string",
  "expirationDateTime": "string (timestamp)",
  "id": "string (identifier)",
  "clientState": "string"
}

```
## <a name="properties"></a><span data-ttu-id="28090-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="28090-109">Properties</span></span>
| <span data-ttu-id="28090-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="28090-110">Property</span></span>     | <span data-ttu-id="28090-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="28090-111">Type</span></span>   |<span data-ttu-id="28090-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="28090-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="28090-113">changeType</span><span class="sxs-lookup"><span data-stu-id="28090-113">changeType</span></span>|<span data-ttu-id="28090-114">string</span><span class="sxs-lookup"><span data-stu-id="28090-114">string</span></span>|<span data-ttu-id="28090-115">Indica el tipo de cambio en el recurso suscrito que generará una notificación.</span><span class="sxs-lookup"><span data-stu-id="28090-115">Indicates the type of change in the subscribed resource that will raise a notification. The supported values are: , , . Multiple values can be combined using a comma-separated list.</span></span> <span data-ttu-id="28090-116">Los valores admitidos son: `created`, `updated`, `deleted`.</span><span class="sxs-lookup"><span data-stu-id="28090-116">The supported values are: `created`, `updated`, `deleted`.</span></span> <span data-ttu-id="28090-117">Se pueden combinar varios valores mediante una lista separada por comas.</span><span class="sxs-lookup"><span data-stu-id="28090-117">Multiple values can be combined using a comma-separated list.</span></span>|
|<span data-ttu-id="28090-118">notificationUrl</span><span class="sxs-lookup"><span data-stu-id="28090-118">notificationUrl</span></span>|<span data-ttu-id="28090-119">string</span><span class="sxs-lookup"><span data-stu-id="28090-119">string</span></span>|<span data-ttu-id="28090-p103">La dirección URL del extremo que recibirá las notificaciones. Esta dirección URL tiene que usar el protocolo HTTPS.</span><span class="sxs-lookup"><span data-stu-id="28090-p103">The URL of the endpoint that will receive the notifications. This URL has to make use of the HTTPS protocol.</span></span>|
|<span data-ttu-id="28090-122">recurso</span><span class="sxs-lookup"><span data-stu-id="28090-122">resource</span></span>|<span data-ttu-id="28090-123">string</span><span class="sxs-lookup"><span data-stu-id="28090-123">string</span></span>|<span data-ttu-id="28090-p104">Especifica el recurso al que se le supervisarán los cambios. No incluya la dirección URL base ("https://graph.microsoft.com/v1.0/").</span><span class="sxs-lookup"><span data-stu-id="28090-p104">Specifies the resource that will be monitored for changes. Do not include the base URL ("https://graph.microsoft.com/v1.0/").</span></span>|
|<span data-ttu-id="28090-126">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="28090-126">expirationDateTime</span></span>|[<span data-ttu-id="28090-127">dateTime</span><span class="sxs-lookup"><span data-stu-id="28090-127">dateTime</span></span>](http://tools.ietf.org/html/rfc3339)|<span data-ttu-id="28090-128">Especifica la fecha y hora en que expira la suscripción de webhook.</span><span class="sxs-lookup"><span data-stu-id="28090-128">Specifies the date and time when the webhook subscription expires.</span></span> <span data-ttu-id="28090-129">La hora está en UTC y puede ser un periodo de tiempo desde la creación de la suscripción que varía para el recurso al que se está suscrito.</span><span class="sxs-lookup"><span data-stu-id="28090-129">Specifies the date and time when the webhook subscription expires. The time is in UTC, and can be an amount of time from subscription creation that varies for the resource subscribed to.  See the table below for maximum values.</span></span>  <span data-ttu-id="28090-130">Consulte la tabla siguiente para la duración máxima de la suscripción compatible.</span><span class="sxs-lookup"><span data-stu-id="28090-130">See the table below for maximum supported subscription length of time.</span></span> |
|<span data-ttu-id="28090-131">clientState</span><span class="sxs-lookup"><span data-stu-id="28090-131">clientState</span></span>|<span data-ttu-id="28090-132">string</span><span class="sxs-lookup"><span data-stu-id="28090-132">string</span></span>|<span data-ttu-id="28090-133">Especifica el valor de la propiedad `clientState` enviado por el servicio en cada notificación.</span><span class="sxs-lookup"><span data-stu-id="28090-133">Specifies the value of the `clientState` property sent by the service in each notification.</span></span> <span data-ttu-id="28090-134">Se permite una longitud máxima de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="28090-134">The maximum length is 255 characters.</span></span> <span data-ttu-id="28090-135">El cliente puede comprobar que la notificación viene del servicio si compara el valor de la propiedad `clientState` enviado con la suscripción con el valor de la propiedad `clientState` recibido con cada notificación.</span><span class="sxs-lookup"><span data-stu-id="28090-135">Specifies the value of the  property sent by the service in each notification. The maximum length is 128 characters. The client can check that the notification came from the service by comparing the value of the `clientState` property sent with the subscription with the value of the `clientState` property received with each notification.</span></span>|
|<span data-ttu-id="28090-136">identificador</span><span class="sxs-lookup"><span data-stu-id="28090-136">id</span></span>|<span data-ttu-id="28090-137">string</span><span class="sxs-lookup"><span data-stu-id="28090-137">string</span></span>|<span data-ttu-id="28090-p107">Identificador único de la suscripción. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="28090-p107">Unique identifier for the subscription. Read-only.</span></span>|

## <a name="maximum-length-of-subscription-per-resource-type"></a><span data-ttu-id="28090-140">Duración máxima de la suscripción por tipo de recurso</span><span class="sxs-lookup"><span data-stu-id="28090-140">Maximum length of subscription per resource type</span></span>
| <span data-ttu-id="28090-141">Recurso</span><span class="sxs-lookup"><span data-stu-id="28090-141">Resource</span></span> | <span data-ttu-id="28090-142">Tiempo de expiración máximo</span><span class="sxs-lookup"><span data-stu-id="28090-142">Maximum Expiration Time</span></span> |
|:---------------------|:--------------------|
|<span data-ttu-id="28090-143">Correo</span><span class="sxs-lookup"><span data-stu-id="28090-143">Mail</span></span>| <span data-ttu-id="28090-144">4230 minutos.</span><span class="sxs-lookup"><span data-stu-id="28090-144">4230 minutes.</span></span>|
|<span data-ttu-id="28090-145">Calendario</span><span class="sxs-lookup"><span data-stu-id="28090-145">Calendar</span></span>| <span data-ttu-id="28090-146">4230 minutos.</span><span class="sxs-lookup"><span data-stu-id="28090-146">4230 minutes.</span></span>|
|<span data-ttu-id="28090-147">Contactos</span><span class="sxs-lookup"><span data-stu-id="28090-147">Contacts</span></span>| <span data-ttu-id="28090-148">4230 minutos.</span><span class="sxs-lookup"><span data-stu-id="28090-148">4230 minutes.</span></span>|
|<span data-ttu-id="28090-149">Conversaciones de grupo</span><span class="sxs-lookup"><span data-stu-id="28090-149">Group conversations</span></span>| <span data-ttu-id="28090-150">4230 minutos.</span><span class="sxs-lookup"><span data-stu-id="28090-150">4230 minutes.</span></span>|
|<span data-ttu-id="28090-151">Elementos raíz de la unidad</span><span class="sxs-lookup"><span data-stu-id="28090-151">Drive root items</span></span>| <span data-ttu-id="28090-152">43 200 minutos.</span><span class="sxs-lookup"><span data-stu-id="28090-152">43200 minutes.</span></span> <span data-ttu-id="28090-153">Las nuevas aplicaciones y las aplicaciones existentes no deben superar el valor admitido.</span><span class="sxs-lookup"><span data-stu-id="28090-153">Existing applications and new applications should not exceed the supported value.</span></span> <span data-ttu-id="28090-154">En las próximas versiones no se permitirán valores superiores.</span><span class="sxs-lookup"><span data-stu-id="28090-154">Higher values won't be permitted in upcoming releases.</span></span> |

## <a name="relationships"></a><span data-ttu-id="28090-155">Relaciones</span><span class="sxs-lookup"><span data-stu-id="28090-155">Relationships</span></span>
<span data-ttu-id="28090-156">Ninguno</span><span class="sxs-lookup"><span data-stu-id="28090-156">None</span></span>


## <a name="methods"></a><span data-ttu-id="28090-157">Métodos</span><span class="sxs-lookup"><span data-stu-id="28090-157">Methods</span></span>

| <span data-ttu-id="28090-158">Método</span><span class="sxs-lookup"><span data-stu-id="28090-158">Method</span></span>           | <span data-ttu-id="28090-159">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28090-159">Return Type</span></span>    |<span data-ttu-id="28090-160">Descripción</span><span class="sxs-lookup"><span data-stu-id="28090-160">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="28090-161">Crear suscripción</span><span class="sxs-lookup"><span data-stu-id="28090-161">Create subscription</span></span>](../api/subscription_post_subscriptions.md) | [<span data-ttu-id="28090-162">subscription</span><span class="sxs-lookup"><span data-stu-id="28090-162">subscription</span></span>](subscription.md) |<span data-ttu-id="28090-163">Suscripción a una aplicación de escucha para recibir notificaciones cuando cambian los datos de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="28090-163">Subscribes a listener application to receive notifications when Microsoft Graph data changes.</span></span>|
|[<span data-ttu-id="28090-164">Actualizar suscripción</span><span class="sxs-lookup"><span data-stu-id="28090-164">Update subscription</span></span>](../api/subscription_update.md) | [<span data-ttu-id="28090-165">subscription</span><span class="sxs-lookup"><span data-stu-id="28090-165">subscription</span></span>](subscription.md) |<span data-ttu-id="28090-166">Renueva una suscripción al actualizar su tiempo de expiración.</span><span class="sxs-lookup"><span data-stu-id="28090-166">Renews a subscription by updating its expiration time.</span></span>|
|[<span data-ttu-id="28090-167">Obtener suscripción</span><span class="sxs-lookup"><span data-stu-id="28090-167">Get subscription</span></span>](../api/subscription_get.md) | [<span data-ttu-id="28090-168">subscription</span><span class="sxs-lookup"><span data-stu-id="28090-168">subscription</span></span>](subscription.md) |<span data-ttu-id="28090-169">Lee las propiedades y relaciones del objeto subscription.</span><span class="sxs-lookup"><span data-stu-id="28090-169">Reads properties and relationships of subscription object.</span></span>|
|[<span data-ttu-id="28090-170">Eliminar suscripción</span><span class="sxs-lookup"><span data-stu-id="28090-170">Delete subscription</span></span>](../api/subscription_delete.md) | <span data-ttu-id="28090-171">Ninguno</span><span class="sxs-lookup"><span data-stu-id="28090-171">None</span></span> |<span data-ttu-id="28090-172">Elimina un objeto subscription.</span><span class="sxs-lookup"><span data-stu-id="28090-172">Deletes a subscription object.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "subscription resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
