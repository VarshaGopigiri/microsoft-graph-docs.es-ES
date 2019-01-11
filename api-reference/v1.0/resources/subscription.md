---
title: tipo de recurso de suscripción
description: 'Una suscripción a permite que una aplicación de cliente recibir notificaciones sobre cambios en los datos en Microsoft Graph. Actualmente, las suscripciones están habilitadas para los siguientes recursos:'
localization_priority: Priority
ms.openlocfilehash: b70daca8eb0f7c303173945b3cacf2cf53af56ec
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27867014"
---
# <a name="subscription-resource-type"></a><span data-ttu-id="d2100-104">tipo de recurso de suscripción</span><span class="sxs-lookup"><span data-stu-id="d2100-104">subscription resource type</span></span>

<span data-ttu-id="d2100-105">Una suscripción a permite que una aplicación de cliente recibir notificaciones sobre cambios en los datos en Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="d2100-105">A subscription allows a client app to receive notifications about changes to data in Microsoft Graph.</span></span> <span data-ttu-id="d2100-106">Actualmente, las suscripciones están habilitadas para los siguientes recursos:</span><span class="sxs-lookup"><span data-stu-id="d2100-106">Currently, subscriptions are enabled for the following resources:</span></span>

- <span data-ttu-id="d2100-107">Correo, eventos y los contactos de Outlook.</span><span class="sxs-lookup"><span data-stu-id="d2100-107">Mail, events, and contacts from Outlook.</span></span>
- <span data-ttu-id="d2100-108">Conversaciones de los grupos de Office.</span><span class="sxs-lookup"><span data-stu-id="d2100-108">Conversations from Office Groups.</span></span>
- <span data-ttu-id="d2100-109">Los elementos raíz de unidad de OneDrive.</span><span class="sxs-lookup"><span data-stu-id="d2100-109">Drive root items from OneDrive.</span></span>
- <span data-ttu-id="d2100-110">Los usuarios y grupos de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d2100-110">Users and Groups from Azure Active Directory.</span></span>
- <span data-ttu-id="d2100-111">Alertas de la API de seguridad de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="d2100-111">Alerts from the Microsoft Graph Security API.</span></span>

## <a name="json-representation"></a><span data-ttu-id="d2100-112">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d2100-112">JSON representation</span></span>

<span data-ttu-id="d2100-113">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d2100-113">Here is a JSON representation of the resource.</span></span>

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

## <a name="properties"></a><span data-ttu-id="d2100-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d2100-114">Properties</span></span>

| <span data-ttu-id="d2100-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d2100-115">Property</span></span> | <span data-ttu-id="d2100-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="d2100-116">Type</span></span> | <span data-ttu-id="d2100-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2100-117">Description</span></span> |
|:---------|:-----|:------------|
| <span data-ttu-id="d2100-118">changeType</span><span class="sxs-lookup"><span data-stu-id="d2100-118">changeType</span></span> | <span data-ttu-id="d2100-119">string</span><span class="sxs-lookup"><span data-stu-id="d2100-119">string</span></span> | <span data-ttu-id="d2100-120">Necesario.</span><span class="sxs-lookup"><span data-stu-id="d2100-120">Required.</span></span> <span data-ttu-id="d2100-121">Indica el tipo de cambio en el recurso suscrito que generará una notificación.</span><span class="sxs-lookup"><span data-stu-id="d2100-121">Indicates the type of change in the subscribed resource that will raise a notification.</span></span> <span data-ttu-id="d2100-122">Los valores admitidos son: `created`, `updated`, `deleted`.</span><span class="sxs-lookup"><span data-stu-id="d2100-122">The supported values are: `created`, `updated`, `deleted`.</span></span> <span data-ttu-id="d2100-123">Se pueden combinar varios valores mediante una lista separada por comas.</span><span class="sxs-lookup"><span data-stu-id="d2100-123">Multiple values can be combined using a comma-separated list.</span></span><br><br><span data-ttu-id="d2100-124">Nota: Las notificaciones de elemento de raíz de unidad sólo son compatibles con el `updated` changeType.</span><span class="sxs-lookup"><span data-stu-id="d2100-124">Note: Drive root item notifications support only the `updated` changeType.</span></span> <span data-ttu-id="d2100-125">Admiten notificaciones de usuario y de grupo `updated` y `deleted` changeType.</span><span class="sxs-lookup"><span data-stu-id="d2100-125">User and group notifications support `updated` and `deleted` changeType.</span></span>|
| <span data-ttu-id="d2100-126">notificationUrl</span><span class="sxs-lookup"><span data-stu-id="d2100-126">notificationUrl</span></span> | <span data-ttu-id="d2100-127">string</span><span class="sxs-lookup"><span data-stu-id="d2100-127">string</span></span> | <span data-ttu-id="d2100-128">Necesario.</span><span class="sxs-lookup"><span data-stu-id="d2100-128">Required.</span></span> <span data-ttu-id="d2100-129">La dirección URL del extremo que va a recibir las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="d2100-129">The URL of the endpoint that will receive the notifications.</span></span> <span data-ttu-id="d2100-130">Esta dirección URL debe hacer uso de la HTTPS protocolo.</span><span class="sxs-lookup"><span data-stu-id="d2100-130">This URL must make use of the HTTPS protocol.</span></span> |
| <span data-ttu-id="d2100-131">resource</span><span class="sxs-lookup"><span data-stu-id="d2100-131">resource</span></span> | <span data-ttu-id="d2100-132">string</span><span class="sxs-lookup"><span data-stu-id="d2100-132">string</span></span> | <span data-ttu-id="d2100-133">Necesario.</span><span class="sxs-lookup"><span data-stu-id="d2100-133">Required.</span></span> <span data-ttu-id="d2100-134">Especifica el recurso al que se van a supervisar para que los cambios.</span><span class="sxs-lookup"><span data-stu-id="d2100-134">Specifies the resource that will be monitored for changes.</span></span> <span data-ttu-id="d2100-135">No incluya la dirección URL base (`https://graph.microsoft.com/v1.0/`).</span><span class="sxs-lookup"><span data-stu-id="d2100-135">Do not include the base URL (`https://graph.microsoft.com/v1.0/`).</span></span> |
| <span data-ttu-id="d2100-136">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="d2100-136">expirationDateTime</span></span> | [<span data-ttu-id="d2100-137">dateTime</span><span class="sxs-lookup"><span data-stu-id="d2100-137">dateTime</span></span>](https://tools.ietf.org/html/rfc3339) | <span data-ttu-id="d2100-138">Necesario.</span><span class="sxs-lookup"><span data-stu-id="d2100-138">Required.</span></span> <span data-ttu-id="d2100-139">Especifica la fecha y hora en que expira la suscripción de webhook.</span><span class="sxs-lookup"><span data-stu-id="d2100-139">Specifies the date and time when the webhook subscription expires.</span></span> <span data-ttu-id="d2100-140">La hora está en UTC y puede ser un periodo de tiempo desde la creación de la suscripción que varía para el recurso al que se está suscrito.</span><span class="sxs-lookup"><span data-stu-id="d2100-140">The time is in UTC, and can be an amount of time from subscription creation that varies for the resource subscribed to.</span></span>  <span data-ttu-id="d2100-141">Consulte la tabla siguiente para la duración máxima de la suscripción compatible.</span><span class="sxs-lookup"><span data-stu-id="d2100-141">See the table below for maximum supported subscription length of time.</span></span> |
| <span data-ttu-id="d2100-142">clientState</span><span class="sxs-lookup"><span data-stu-id="d2100-142">clientState</span></span> | <span data-ttu-id="d2100-143">string</span><span class="sxs-lookup"><span data-stu-id="d2100-143">string</span></span> | <span data-ttu-id="d2100-144">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d2100-144">Optional.</span></span> <span data-ttu-id="d2100-145">Especifica el valor de la propiedad `clientState` enviado por el servicio en cada notificación.</span><span class="sxs-lookup"><span data-stu-id="d2100-145">Specifies the value of the `clientState` property sent by the service in each notification.</span></span> <span data-ttu-id="d2100-146">Se permite una longitud máxima de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d2100-146">The maximum length is 128 characters.</span></span> <span data-ttu-id="d2100-147">El cliente puede comprobar que la notificación viene del servicio si compara el valor de la propiedad `clientState` enviado con la suscripción con el valor de la propiedad `clientState` recibido con cada notificación.</span><span class="sxs-lookup"><span data-stu-id="d2100-147">The client can check that the notification came from the service by comparing the value of the `clientState` property sent with the subscription with the value of the `clientState` property received with each notification.</span></span> |
| <span data-ttu-id="d2100-148">identificador</span><span class="sxs-lookup"><span data-stu-id="d2100-148">id</span></span> | <span data-ttu-id="d2100-149">string</span><span class="sxs-lookup"><span data-stu-id="d2100-149">string</span></span> | <span data-ttu-id="d2100-p109">Identificador único de la suscripción. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d2100-p109">Unique identifier for the subscription. Read-only.</span></span> |
| <span data-ttu-id="d2100-152">applicationId</span><span class="sxs-lookup"><span data-stu-id="d2100-152">applicationId</span></span> | <span data-ttu-id="d2100-153">string</span><span class="sxs-lookup"><span data-stu-id="d2100-153">string</span></span> | <span data-ttu-id="d2100-154">Identificador de la aplicación utilizada para crear la suscripción.</span><span class="sxs-lookup"><span data-stu-id="d2100-154">Identifier of the application used to create the subscription.</span></span> <span data-ttu-id="d2100-155">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d2100-155">Read-only.</span></span> |
| <span data-ttu-id="d2100-156">Creador de</span><span class="sxs-lookup"><span data-stu-id="d2100-156">creatorId</span></span> | <span data-ttu-id="d2100-157">string</span><span class="sxs-lookup"><span data-stu-id="d2100-157">string</span></span> | <span data-ttu-id="d2100-158">Identificador del usuario o de la entidad de seguridad de servicio que creó la suscripción.</span><span class="sxs-lookup"><span data-stu-id="d2100-158">Identifier of the user or service principal that created the subscription.</span></span> <span data-ttu-id="d2100-159">Si la aplicación usada delegado permisos para crear la suscripción, este campo contiene el identificador del usuario ha iniciado sesión de que la aplicación llama en nombre.</span><span class="sxs-lookup"><span data-stu-id="d2100-159">If the app used delegated permissions to create the subscription, this field contains the id of the signed-in user the app called on behalf of.</span></span> <span data-ttu-id="d2100-160">Si la aplicación usa los permisos de aplicación, este campo contiene el identificador de la entidad de seguridad de servicio correspondiente a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d2100-160">If the app used application permissions, this field contains the id of the service principal corresponding to the app.</span></span> <span data-ttu-id="d2100-161">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d2100-161">Read-only.</span></span> |

## <a name="maximum-length-of-subscription-per-resource-type"></a><span data-ttu-id="d2100-162">Duración máxima de la suscripción por tipo de recurso</span><span class="sxs-lookup"><span data-stu-id="d2100-162">Maximum length of subscription per resource type</span></span>

| <span data-ttu-id="d2100-163">Recurso</span><span class="sxs-lookup"><span data-stu-id="d2100-163">Resource</span></span>            | <span data-ttu-id="d2100-164">Tiempo de expiración máximo</span><span class="sxs-lookup"><span data-stu-id="d2100-164">Maximum Expiration Time</span></span>  |
|:--------------------|:-------------------------|
| <span data-ttu-id="d2100-165">Correo</span><span class="sxs-lookup"><span data-stu-id="d2100-165">Mail</span></span>                | <span data-ttu-id="d2100-166">4230 minutos (en 3 días)</span><span class="sxs-lookup"><span data-stu-id="d2100-166">4230 minutes (under 3 days)</span></span>    |
| <span data-ttu-id="d2100-167">Calendario</span><span class="sxs-lookup"><span data-stu-id="d2100-167">Calendar</span></span>            | <span data-ttu-id="d2100-168">4230 minutos (en 3 días)</span><span class="sxs-lookup"><span data-stu-id="d2100-168">4230 minutes (under 3 days)</span></span>    |
| <span data-ttu-id="d2100-169">Contactos</span><span class="sxs-lookup"><span data-stu-id="d2100-169">Contacts</span></span>            | <span data-ttu-id="d2100-170">4230 minutos (en 3 días)</span><span class="sxs-lookup"><span data-stu-id="d2100-170">4230 minutes (under 3 days)</span></span>    |
| <span data-ttu-id="d2100-171">Conversaciones de grupo</span><span class="sxs-lookup"><span data-stu-id="d2100-171">Group conversations</span></span> | <span data-ttu-id="d2100-172">4230 minutos (en 3 días)</span><span class="sxs-lookup"><span data-stu-id="d2100-172">4230 minutes (under 3 days)</span></span>    |
| <span data-ttu-id="d2100-173">Elementos raíz de la unidad</span><span class="sxs-lookup"><span data-stu-id="d2100-173">Drive root items</span></span>    | <span data-ttu-id="d2100-174">4230 minutos (en 3 días)</span><span class="sxs-lookup"><span data-stu-id="d2100-174">4230 minutes (under 3 days)</span></span>    |
| <span data-ttu-id="d2100-175">Alertas de seguridad</span><span class="sxs-lookup"><span data-stu-id="d2100-175">Security alerts</span></span>     | <span data-ttu-id="d2100-176">43200 minutos (en 30 días)</span><span class="sxs-lookup"><span data-stu-id="d2100-176">43200 minutes (under 30 days)</span></span>  |

> <span data-ttu-id="d2100-177">**Nota:** Las aplicaciones existentes y nuevas aplicaciones no deben superar el valor admitido.</span><span class="sxs-lookup"><span data-stu-id="d2100-177">**Note:** Existing applications and new applications should not exceed the supported value.</span></span> <span data-ttu-id="d2100-178">En el futuro, se producirá un error en las solicitudes para crear o renovar una suscripción más allá del valor máximo.</span><span class="sxs-lookup"><span data-stu-id="d2100-178">In the future, any requests to create or renew a subscription beyond the maximum value will fail.</span></span>

## <a name="relationships"></a><span data-ttu-id="d2100-179">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d2100-179">Relationships</span></span>

<span data-ttu-id="d2100-180">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d2100-180">None</span></span>

## <a name="methods"></a><span data-ttu-id="d2100-181">Métodos</span><span class="sxs-lookup"><span data-stu-id="d2100-181">Methods</span></span>

| <span data-ttu-id="d2100-182">Método</span><span class="sxs-lookup"><span data-stu-id="d2100-182">Method</span></span> | <span data-ttu-id="d2100-183">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d2100-183">Return Type</span></span> | <span data-ttu-id="d2100-184">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2100-184">Description</span></span> |
|:-------|:------------|:------------|
| [<span data-ttu-id="d2100-185">Crear suscripción</span><span class="sxs-lookup"><span data-stu-id="d2100-185">Create subscription</span></span>](../api/subscription-post-subscriptions.md) | [<span data-ttu-id="d2100-186">subscription</span><span class="sxs-lookup"><span data-stu-id="d2100-186">subscription</span></span>](subscription.md) | <span data-ttu-id="d2100-187">Suscripción a una aplicación de escucha para recibir notificaciones cuando cambian los datos de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="d2100-187">Subscribes a listener application to receive notifications when Microsoft Graph data changes.</span></span> |
| [<span data-ttu-id="d2100-188">Actualizar suscripción</span><span class="sxs-lookup"><span data-stu-id="d2100-188">Update subscription</span></span>](../api/subscription-update.md) | [<span data-ttu-id="d2100-189">subscription</span><span class="sxs-lookup"><span data-stu-id="d2100-189">subscription</span></span>](subscription.md) | <span data-ttu-id="d2100-190">Renueva una suscripción al actualizar su tiempo de expiración.</span><span class="sxs-lookup"><span data-stu-id="d2100-190">Renews a subscription by updating its expiration time.</span></span> |
| [<span data-ttu-id="d2100-191">Suscripciones de lista</span><span class="sxs-lookup"><span data-stu-id="d2100-191">List subscriptions</span></span>](../api/subscription-list.md) | [<span data-ttu-id="d2100-192">subscription</span><span class="sxs-lookup"><span data-stu-id="d2100-192">subscription</span></span>](subscription.md) | <span data-ttu-id="d2100-193">Listas de suscripciones activas.</span><span class="sxs-lookup"><span data-stu-id="d2100-193">Lists active subscriptions.</span></span> |
| [<span data-ttu-id="d2100-194">Obtener suscripción</span><span class="sxs-lookup"><span data-stu-id="d2100-194">Get subscription</span></span>](../api/subscription-get.md) | [<span data-ttu-id="d2100-195">subscription</span><span class="sxs-lookup"><span data-stu-id="d2100-195">subscription</span></span>](subscription.md) | <span data-ttu-id="d2100-196">Lee las propiedades y relaciones del objeto subscription.</span><span class="sxs-lookup"><span data-stu-id="d2100-196">Reads properties and relationships of subscription object.</span></span> |
| [<span data-ttu-id="d2100-197">Eliminar suscripción</span><span class="sxs-lookup"><span data-stu-id="d2100-197">Delete subscription</span></span>](../api/subscription-delete.md) | <span data-ttu-id="d2100-198">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d2100-198">None</span></span> |<span data-ttu-id="d2100-199">Elimina un objeto subscription.</span><span class="sxs-lookup"><span data-stu-id="d2100-199">Deletes a subscription object.</span></span> |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "subscription resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
