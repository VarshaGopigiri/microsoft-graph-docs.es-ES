---
title: Crear suscripción
description: Suscripción a una aplicación de escucha para recibir notificaciones cuando cambian los datos en Microsoft Graph.
ms.openlocfilehash: 72f9a2d97733901ea4d543045d85be60978c5e5c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030527"
---
# <a name="create-subscription"></a><span data-ttu-id="11deb-103">Crear suscripción</span><span class="sxs-lookup"><span data-stu-id="11deb-103">Create subscription</span></span>

<span data-ttu-id="11deb-104">Suscripción a una aplicación de escucha para recibir notificaciones cuando cambian los datos en Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="11deb-104">Subscribes a listener application to receive notifications when data on the Microsoft Graph changes.</span></span>

## <a name="permissions"></a><span data-ttu-id="11deb-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="11deb-105">Permissions</span></span>

<span data-ttu-id="11deb-p101">La creación de una suscripción requiere un ámbito de lectura para el recurso. Por ejemplo, para obtener mensajes de notificaciones, la aplicación necesita el permiso `Mail.Read`. En la tabla siguiente se muestra el permiso propuesto que se necesita para cada recurso. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="11deb-p101">Creating a subscription requires read scope to the resource. For example, to get notifications messages, your app needs the `Mail.Read` permission. The following table lists the suggested permission needed for each resource. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="11deb-110">Tipo de recurso o elemento</span><span class="sxs-lookup"><span data-stu-id="11deb-110">Resource type / Item</span></span>        | <span data-ttu-id="11deb-111">Permiso</span><span class="sxs-lookup"><span data-stu-id="11deb-111">Permission</span></span>          |
|-----------------------------|---------------------|
| <span data-ttu-id="11deb-112">Contactos</span><span class="sxs-lookup"><span data-stu-id="11deb-112">Contacts</span></span>                    | <span data-ttu-id="11deb-113">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="11deb-113">Contacts.Read</span></span>       |
| <span data-ttu-id="11deb-114">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="11deb-114">Conversations</span></span>               | <span data-ttu-id="11deb-115">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="11deb-115">Group.Read.All</span></span>      |
| <span data-ttu-id="11deb-116">Eventos</span><span class="sxs-lookup"><span data-stu-id="11deb-116">Events</span></span>                      | <span data-ttu-id="11deb-117">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="11deb-117">Calendars.Read</span></span>      |
| <span data-ttu-id="11deb-118">Mensajes</span><span class="sxs-lookup"><span data-stu-id="11deb-118">Messages</span></span>                    | <span data-ttu-id="11deb-119">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="11deb-119">Mail.Read</span></span>           |
| <span data-ttu-id="11deb-120">Groups</span><span class="sxs-lookup"><span data-stu-id="11deb-120">Groups</span></span>                      | <span data-ttu-id="11deb-121">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="11deb-121">Group.Read.All</span></span>      |
| <span data-ttu-id="11deb-122">Users</span><span class="sxs-lookup"><span data-stu-id="11deb-122">Users</span></span>                       | <span data-ttu-id="11deb-123">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="11deb-123">User.Read.All</span></span>       |
| <span data-ttu-id="11deb-124">Unidad de disco (OneDrive del usuario)</span><span class="sxs-lookup"><span data-stu-id="11deb-124">Drive  (User's OneDrive)</span></span>    | <span data-ttu-id="11deb-125">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="11deb-125">Files.ReadWrite</span></span>     |
| <span data-ttu-id="11deb-126">Unidades (contenido de SharePoint compartido y unidades)</span><span class="sxs-lookup"><span data-stu-id="11deb-126">Drives (SharePoint shared content and drives)</span></span> | <span data-ttu-id="11deb-127">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="11deb-127">Files.ReadWrite.All</span></span> |
|<span data-ttu-id="11deb-128">Alerta de seguridad</span><span class="sxs-lookup"><span data-stu-id="11deb-128">Security alert</span></span>| <span data-ttu-id="11deb-129">SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="11deb-129">SecurityEvents.ReadWrite.All</span></span> |

 > <span data-ttu-id="11deb-130">**Nota:** El extremo de /v1.0 permite que los permisos de aplicación para la mayoría de los recursos.</span><span class="sxs-lookup"><span data-stu-id="11deb-130">**Note:** The /v1.0 endpoint allows application permissions for most resources.</span></span> <span data-ttu-id="11deb-131">Las conversaciones de un grupo y OneDrive para la unidad raíz los elementos no son compatibles con los permisos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="11deb-131">Conversations in a Group and OneDrive drive root items are not supported with application permissions.</span></span>

## <a name="http-request"></a><span data-ttu-id="11deb-132">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="11deb-132">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /subscriptions
```

## <a name="request-headers"></a><span data-ttu-id="11deb-133">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="11deb-133">Request headers</span></span>

| <span data-ttu-id="11deb-134">Nombre</span><span class="sxs-lookup"><span data-stu-id="11deb-134">Name</span></span>       | <span data-ttu-id="11deb-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="11deb-135">Type</span></span> | <span data-ttu-id="11deb-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="11deb-136">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="11deb-137">Authorization</span><span class="sxs-lookup"><span data-stu-id="11deb-137">Authorization</span></span>  | <span data-ttu-id="11deb-138">string</span><span class="sxs-lookup"><span data-stu-id="11deb-138">string</span></span>  | <span data-ttu-id="11deb-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="11deb-p103">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="11deb-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="11deb-141">Response</span></span>

<span data-ttu-id="11deb-142">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto de [suscripción](../resources/subscription.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="11deb-142">If successful, this method returns `201 Created` response code and a [subscription](../resources/subscription.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="11deb-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="11deb-143">Example</span></span>

##### <a name="request"></a><span data-ttu-id="11deb-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="11deb-144">Request</span></span>

<span data-ttu-id="11deb-145">Este es un ejemplo de solicitud para enviar una notificación cuando el usuario recibe un nuevo correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="11deb-145">Here is an example of the request to send a notification when the user receives a new mail.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_subscription_from_subscriptions"
}-->

```http
POST https://graph.microsoft.com/v1.0/subscriptions
Content-type: application/json

{
   "changeType": "created,updated",
   "notificationUrl": "https://webhook.azurewebsites.net/api/send/myNotifyClient",
   "resource": "me/mailFolders('Inbox')/messages",
   "expirationDateTime":"2016-11-20T18:23:45.9356913Z",
   "clientState": "secretClientValue"
}
```

<span data-ttu-id="11deb-146">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto de [suscripción](../resources/subscription.md) .</span><span class="sxs-lookup"><span data-stu-id="11deb-146">In the request body, supply a JSON representation of the [subscription](../resources/subscription.md) object.</span></span>
<span data-ttu-id="11deb-147">El `clientState` campo es opcional.</span><span class="sxs-lookup"><span data-stu-id="11deb-147">The `clientState` field is optional.</span></span>

##### <a name="resources-examples"></a><span data-ttu-id="11deb-148">Ejemplos de recursos</span><span class="sxs-lookup"><span data-stu-id="11deb-148">Resources examples</span></span>

<span data-ttu-id="11deb-149">A continuación puede ver algunos valores válidos para la propiedad de recurso de la suscripción:</span><span class="sxs-lookup"><span data-stu-id="11deb-149">The following are valid values for the resource property of the subscription:</span></span>

| <span data-ttu-id="11deb-150">Tipo de recurso</span><span class="sxs-lookup"><span data-stu-id="11deb-150">Resource type</span></span> | <span data-ttu-id="11deb-151">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="11deb-151">Examples</span></span> |
|:------ |:----- |
|<span data-ttu-id="11deb-152">Correo</span><span class="sxs-lookup"><span data-stu-id="11deb-152">Mail</span></span>|<span data-ttu-id="11deb-153">me/mailfolders("inbox")/messages</span><span class="sxs-lookup"><span data-stu-id="11deb-153">me/mailfolders('inbox')/messages</span></span><br /><span data-ttu-id="11deb-154">me/messages</span><span class="sxs-lookup"><span data-stu-id="11deb-154">me/messages</span></span>|
|<span data-ttu-id="11deb-155">Contactos</span><span class="sxs-lookup"><span data-stu-id="11deb-155">Contacts</span></span>|<span data-ttu-id="11deb-156">me/contacts</span><span class="sxs-lookup"><span data-stu-id="11deb-156">me/contacts</span></span>|
|<span data-ttu-id="11deb-157">Calendarios</span><span class="sxs-lookup"><span data-stu-id="11deb-157">Calendars</span></span>|<span data-ttu-id="11deb-158">me/events</span><span class="sxs-lookup"><span data-stu-id="11deb-158">me/events</span></span>|
|<span data-ttu-id="11deb-159">Users</span><span class="sxs-lookup"><span data-stu-id="11deb-159">Users</span></span>|<span data-ttu-id="11deb-160">users</span><span class="sxs-lookup"><span data-stu-id="11deb-160">users</span></span>|
|<span data-ttu-id="11deb-161">Groups</span><span class="sxs-lookup"><span data-stu-id="11deb-161">Groups</span></span>|<span data-ttu-id="11deb-162">grupos</span><span class="sxs-lookup"><span data-stu-id="11deb-162">groups</span></span>|
|<span data-ttu-id="11deb-163">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="11deb-163">Conversations</span></span>|<span data-ttu-id="11deb-164">groups("*{id}*")/conversations</span><span class="sxs-lookup"><span data-stu-id="11deb-164">groups('*{id}*')/conversations</span></span>|
|<span data-ttu-id="11deb-165">Unidades</span><span class="sxs-lookup"><span data-stu-id="11deb-165">Drives</span></span>|<span data-ttu-id="11deb-166">me/drive/root</span><span class="sxs-lookup"><span data-stu-id="11deb-166">me/drive/root</span></span>|
|<span data-ttu-id="11deb-167">Alerta de seguridad</span><span class="sxs-lookup"><span data-stu-id="11deb-167">Security alert</span></span>|<span data-ttu-id="11deb-168">alertas de seguridad /? $filter = estado eq 'New'</span><span class="sxs-lookup"><span data-stu-id="11deb-168">security/alerts?$filter=status eq ‘New’</span></span>|

##### <a name="response"></a><span data-ttu-id="11deb-169">Respuesta</span><span class="sxs-lookup"><span data-stu-id="11deb-169">Response</span></span>

<span data-ttu-id="11deb-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="11deb-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

## <a name="notification-endpoint-validation"></a><span data-ttu-id="11deb-173">Validación de extremo de notificación</span><span class="sxs-lookup"><span data-stu-id="11deb-173">Notification endpoint validation</span></span>

<span data-ttu-id="11deb-174">El extremo de la notificación de suscripción (especificado en el `notificationUrl` (propiedad)) debe ser capaz de responder a una solicitud de validación, como se describe en [Configurar notificaciones para los cambios en los datos de usuario](/graph/webhooks#notification-endpoint-validation).</span><span class="sxs-lookup"><span data-stu-id="11deb-174">The subscription notification endpoint (specified in the `notificationUrl` property) must be capable of responding to a validation request as described in [Set up notifications for changes in user data](/graph/webhooks#notification-endpoint-validation).</span></span> <span data-ttu-id="11deb-175">Si se produce un error en la validación, la solicitud para crear la suscripción devuelve un error 400 de solicitud incorrecta.</span><span class="sxs-lookup"><span data-stu-id="11deb-175">If validation fails, the request to create the subscription returns a 400 Bad Request error.</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create subscription",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
