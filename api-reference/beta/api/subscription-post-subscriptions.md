---
title: Crear suscripción
description: Se suscribe a una aplicación de agente de escucha para recibir notificaciones cuando cambian los datos en un recurso de Microsoft Graph.
ms.openlocfilehash: f524213871f8a9216ad7f7ec8da4ffb521a4a2aa
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090652"
---
# <a name="create-subscription"></a><span data-ttu-id="91036-103">Crear suscripción</span><span class="sxs-lookup"><span data-stu-id="91036-103">Create subscription</span></span>

> <span data-ttu-id="91036-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="91036-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="91036-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="91036-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="91036-106">Se suscribe a una aplicación de agente de escucha para recibir notificaciones cuando cambian los datos en un recurso de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="91036-106">Subscribes a listener application to receive notifications when data on a Microsoft Graph resource changes.</span></span>

## <a name="permissions"></a><span data-ttu-id="91036-107">Permissions</span><span class="sxs-lookup"><span data-stu-id="91036-107">Permissions</span></span>

<span data-ttu-id="91036-108">Creación de una suscripción requiere permiso de lectura para el recurso para el que la aplicación va a recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="91036-108">Creating a subscription requires read permission to the resource for which the app will receive notifications.</span></span> <span data-ttu-id="91036-109">Por ejemplo, para obtener las notificaciones sobre los mensajes, la aplicación necesita la `Mail.Read` permiso.</span><span class="sxs-lookup"><span data-stu-id="91036-109">For example, to get notifications about Messages, your app needs the `Mail.Read` permission.</span></span> <span data-ttu-id="91036-110">En la tabla siguiente se muestra el permiso propuesto que se requiere para cada recurso.</span><span class="sxs-lookup"><span data-stu-id="91036-110">The following table lists the suggested permission needed for each resource.</span></span> <span data-ttu-id="91036-111">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="91036-111">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="91036-112">Tipo de recurso o elemento</span><span class="sxs-lookup"><span data-stu-id="91036-112">Resource type / Item</span></span>        | <span data-ttu-id="91036-113">Permiso</span><span class="sxs-lookup"><span data-stu-id="91036-113">Permission</span></span>          |
|-----------------------------|---------------------|
| <span data-ttu-id="91036-114">Contactos</span><span class="sxs-lookup"><span data-stu-id="91036-114">Contacts</span></span>                    | <span data-ttu-id="91036-115">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="91036-115">Contacts.Read</span></span>       |
| <span data-ttu-id="91036-116">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="91036-116">Conversations</span></span>               | <span data-ttu-id="91036-117">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="91036-117">Group.Read.All</span></span>      |
| <span data-ttu-id="91036-118">Eventos</span><span class="sxs-lookup"><span data-stu-id="91036-118">Events</span></span>                      | <span data-ttu-id="91036-119">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="91036-119">Calendars.Read</span></span>      |
| <span data-ttu-id="91036-120">Mensajes</span><span class="sxs-lookup"><span data-stu-id="91036-120">Messages</span></span>                    | <span data-ttu-id="91036-121">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="91036-121">Mail.Read</span></span>           |
| <span data-ttu-id="91036-122">Groups</span><span class="sxs-lookup"><span data-stu-id="91036-122">Groups</span></span>                      | <span data-ttu-id="91036-123">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="91036-123">Group.Read.All</span></span>      |
| <span data-ttu-id="91036-124">Users</span><span class="sxs-lookup"><span data-stu-id="91036-124">Users</span></span>                       | <span data-ttu-id="91036-125">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="91036-125">User.Read.All</span></span>       |
| <span data-ttu-id="91036-126">Unidad de disco (OneDrive del usuario)</span><span class="sxs-lookup"><span data-stu-id="91036-126">Drive  (User's OneDrive)</span></span>    | <span data-ttu-id="91036-127">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="91036-127">Files.ReadWrite</span></span>     |
| <span data-ttu-id="91036-128">Unidades (contenido de SharePoint compartido y unidades)</span><span class="sxs-lookup"><span data-stu-id="91036-128">Drives (SharePoint shared content and drives)</span></span> | <span data-ttu-id="91036-129">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="91036-129">Files.ReadWrite.All</span></span> |
| <span data-ttu-id="91036-130">Alerta de seguridad</span><span class="sxs-lookup"><span data-stu-id="91036-130">Security alert</span></span>              | <span data-ttu-id="91036-131">SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="91036-131">SecurityEvents.ReadWrite.All</span></span> |

> <span data-ttu-id="91036-132">**Nota:** El extremo de /beta permite que los permisos de aplicación para la mayoría de los recursos.</span><span class="sxs-lookup"><span data-stu-id="91036-132">**Note:** The /beta endpoint allows application permissions for most resources.</span></span> <span data-ttu-id="91036-133">Las conversaciones de un grupo y OneDrive para la unidad raíz los elementos no son compatibles con los permisos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="91036-133">Conversations in a Group and OneDrive drive root items are not supported with application permissions.</span></span>

## <a name="http-request"></a><span data-ttu-id="91036-134">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="91036-134">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /subscriptions
```

## <a name="request-headers"></a><span data-ttu-id="91036-135">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="91036-135">Request headers</span></span>

| <span data-ttu-id="91036-136">Nombre</span><span class="sxs-lookup"><span data-stu-id="91036-136">Name</span></span>       | <span data-ttu-id="91036-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="91036-137">Type</span></span> | <span data-ttu-id="91036-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="91036-138">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="91036-139">Authorization</span><span class="sxs-lookup"><span data-stu-id="91036-139">Authorization</span></span>  | <span data-ttu-id="91036-140">string</span><span class="sxs-lookup"><span data-stu-id="91036-140">string</span></span>  | <span data-ttu-id="91036-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="91036-p104">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="91036-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="91036-143">Response</span></span>

<span data-ttu-id="91036-144">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto de [suscripción](../resources/subscription.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="91036-144">If successful, this method returns `201 Created` response code and a [subscription](../resources/subscription.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="91036-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="91036-145">Example</span></span>

##### <a name="request"></a><span data-ttu-id="91036-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="91036-146">Request</span></span>

<span data-ttu-id="91036-147">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto de [suscripción](../resources/subscription.md) .</span><span class="sxs-lookup"><span data-stu-id="91036-147">In the request body, supply a JSON representation of the [subscription](../resources/subscription.md) object.</span></span>
<span data-ttu-id="91036-148">El `clientState` campo es opcional.</span><span class="sxs-lookup"><span data-stu-id="91036-148">The `clientState` field is optional.</span></span>

<span data-ttu-id="91036-149">En este ejemplo de solicitud crea una suscripción para las notificaciones de nuevo correo recibido por el usuario actualmente iniciado.</span><span class="sxs-lookup"><span data-stu-id="91036-149">This sample request creates a subscription for notifications about new mail received by the currently signed in user.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_subscription_from_subscriptions"
}-->

```http
POST https://graph.microsoft.com/beta/subscriptions
Content-type: application/json

{
   "changeType": "created,updated",
   "notificationUrl": "https://webhook.azurewebsites.net/api/send/myNotifyClient",
   "resource": "me/mailFolders('Inbox')/messages",
   "expirationDateTime":"2016-11-20T18:23:45.9356913Z",
   "clientState": "secretClientValue"
}
```

<span data-ttu-id="91036-150">Las siguientes son valores válidos para la propiedad de recurso:</span><span class="sxs-lookup"><span data-stu-id="91036-150">The following are valid values for the resource property:</span></span>

| <span data-ttu-id="91036-151">Tipo de recurso</span><span class="sxs-lookup"><span data-stu-id="91036-151">Resource type</span></span> | <span data-ttu-id="91036-152">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="91036-152">Examples</span></span> |
|:------ |:----- |
|<span data-ttu-id="91036-153">Correo</span><span class="sxs-lookup"><span data-stu-id="91036-153">Mail</span></span>|<span data-ttu-id="91036-154">me/mailfolders("inbox")/messages</span><span class="sxs-lookup"><span data-stu-id="91036-154">me/mailfolders('inbox')/messages</span></span><br /><span data-ttu-id="91036-155">me/messages</span><span class="sxs-lookup"><span data-stu-id="91036-155">me/messages</span></span>|
|<span data-ttu-id="91036-156">Contactos</span><span class="sxs-lookup"><span data-stu-id="91036-156">Contacts</span></span>|<span data-ttu-id="91036-157">me/contacts</span><span class="sxs-lookup"><span data-stu-id="91036-157">me/contacts</span></span>|
|<span data-ttu-id="91036-158">Calendarios</span><span class="sxs-lookup"><span data-stu-id="91036-158">Calendars</span></span>|<span data-ttu-id="91036-159">me/events</span><span class="sxs-lookup"><span data-stu-id="91036-159">me/events</span></span>|
|<span data-ttu-id="91036-160">Users</span><span class="sxs-lookup"><span data-stu-id="91036-160">Users</span></span>|<span data-ttu-id="91036-161">users</span><span class="sxs-lookup"><span data-stu-id="91036-161">users</span></span>|
|<span data-ttu-id="91036-162">Groups</span><span class="sxs-lookup"><span data-stu-id="91036-162">Groups</span></span>|<span data-ttu-id="91036-163">grupos</span><span class="sxs-lookup"><span data-stu-id="91036-163">groups</span></span>|
|<span data-ttu-id="91036-164">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="91036-164">Conversations</span></span>|<span data-ttu-id="91036-165">groups("*{id}*")/conversations</span><span class="sxs-lookup"><span data-stu-id="91036-165">groups('*{id}*')/conversations</span></span>|
|<span data-ttu-id="91036-166">Unidades</span><span class="sxs-lookup"><span data-stu-id="91036-166">Drives</span></span>|<span data-ttu-id="91036-167">me/drive/root</span><span class="sxs-lookup"><span data-stu-id="91036-167">me/drive/root</span></span>|
|<span data-ttu-id="91036-168">Alerta de seguridad</span><span class="sxs-lookup"><span data-stu-id="91036-168">Security alert</span></span>|<span data-ttu-id="91036-169">alertas de seguridad /? $filter = estado eq 'New'</span><span class="sxs-lookup"><span data-stu-id="91036-169">security/alerts?$filter=status eq ‘New’</span></span>|

##### <a name="response"></a><span data-ttu-id="91036-170">Respuesta</span><span class="sxs-lookup"><span data-stu-id="91036-170">Response</span></span>

<span data-ttu-id="91036-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="91036-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.subscription"
} -->

```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 252

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#subscriptions/$entity",
  "id": "7f105c7d-2dc5-4530-97cd-4e7ae6534c07",
  "resource": "me/mailFolders('Inbox')/messages",
  "applicationId": "24d3b144-21ae-4080-943f-7067b395b913",
  "changeType": "created,updated",
  "clientState": "secretClientValue",
  "notificationUrl": "https://webhook.azurewebsites.net/api/send/myNotifyClient",
  "expirationDateTime": "2016-11-20T18:23:45.9356913Z",
  "creatorId": "8ee44408-0679-472c-bc2a-692812af3437"
}
```

## <a name="notification-endpoint-validation"></a><span data-ttu-id="91036-174">Validación de extremo de notificación</span><span class="sxs-lookup"><span data-stu-id="91036-174">Notification endpoint validation</span></span>

<span data-ttu-id="91036-175">El extremo de la notificación de suscripción (especificado en el `notificationUrl` (propiedad)) debe ser capaz de responder a una solicitud de validación, como se describe en [Configurar notificaciones para los cambios en los datos de usuario](/graph/webhooks#notification-endpoint-validation).</span><span class="sxs-lookup"><span data-stu-id="91036-175">The subscription notification endpoint (specified in the `notificationUrl` property) must be capable of responding to a validation request as described in [Set up notifications for changes in user data](/graph/webhooks#notification-endpoint-validation).</span></span> <span data-ttu-id="91036-176">Si se produce un error en la validación, la solicitud para crear la suscripción devuelve un error 400 de solicitud incorrecta.</span><span class="sxs-lookup"><span data-stu-id="91036-176">If validation fails, the request to create the subscription returns a 400 Bad Request error.</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create subscription",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
