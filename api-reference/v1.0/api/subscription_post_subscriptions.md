# <a name="create-subscription"></a><span data-ttu-id="2c8e9-101">Crear suscripción</span><span class="sxs-lookup"><span data-stu-id="2c8e9-101">Create subscription</span></span>

<span data-ttu-id="2c8e9-102">Suscripción a una aplicación de escucha para recibir notificaciones cuando cambian los datos en Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="2c8e9-102">Subscribes a listener application to receive notifications when data on the Microsoft Graph changes.</span></span>

## <a name="permissions"></a><span data-ttu-id="2c8e9-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="2c8e9-103">Permissions</span></span>

<span data-ttu-id="2c8e9-p101">La creación de una suscripción requiere un ámbito de lectura para el recurso. Por ejemplo, para obtener mensajes de notificaciones, la aplicación necesita el permiso `Mail.Read`. En la tabla siguiente se muestra el permiso propuesto que se necesita para cada recurso. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="2c8e9-p101">Creating a subscription requires read scope to the resource. For example, to get notifications messages, your app needs the `Mail.Read` permission. The following table lists the suggested permission needed for each resource. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="2c8e9-108">Tipo de recurso o elemento</span><span class="sxs-lookup"><span data-stu-id="2c8e9-108">Resource type / Item</span></span>        | <span data-ttu-id="2c8e9-109">Permiso</span><span class="sxs-lookup"><span data-stu-id="2c8e9-109">Permission</span></span>          |
|-----------------------------|---------------------|
| <span data-ttu-id="2c8e9-110">Contactos</span><span class="sxs-lookup"><span data-stu-id="2c8e9-110">Contacts</span></span>                    | <span data-ttu-id="2c8e9-111">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="2c8e9-111">Contacts.Read</span></span>       |
| <span data-ttu-id="2c8e9-112">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="2c8e9-112">Conversations</span></span>               | <span data-ttu-id="2c8e9-113">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="2c8e9-113">Group.Read.All</span></span>      |
| <span data-ttu-id="2c8e9-114">Eventos</span><span class="sxs-lookup"><span data-stu-id="2c8e9-114">Events</span></span>                      | <span data-ttu-id="2c8e9-115">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="2c8e9-115">Calendars.Read</span></span>      |
| <span data-ttu-id="2c8e9-116">Mensajes</span><span class="sxs-lookup"><span data-stu-id="2c8e9-116">Messages</span></span>                    | <span data-ttu-id="2c8e9-117">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="2c8e9-117">Mail.Read</span></span>           |
| <span data-ttu-id="2c8e9-118">Grupos</span><span class="sxs-lookup"><span data-stu-id="2c8e9-118">Groups</span></span>                      | <span data-ttu-id="2c8e9-119">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="2c8e9-119">Group.Read.All</span></span>      |
| <span data-ttu-id="2c8e9-120">Usuarios</span><span class="sxs-lookup"><span data-stu-id="2c8e9-120">Users</span></span>                       | <span data-ttu-id="2c8e9-121">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="2c8e9-121">User.Read.All</span></span>       |
| <span data-ttu-id="2c8e9-122">Unidad de disco (OneDrive del usuario)</span><span class="sxs-lookup"><span data-stu-id="2c8e9-122">Drive  (User's OneDrive)</span></span>    | <span data-ttu-id="2c8e9-123">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2c8e9-123">Files.ReadWrite</span></span>     |
| <span data-ttu-id="2c8e9-124">Unidades de disco (unidades de disco y contenido compartido de SharePoint)</span><span class="sxs-lookup"><span data-stu-id="2c8e9-124">Drives (Sharepoint shared content and drives)</span></span> | <span data-ttu-id="2c8e9-125">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2c8e9-125">Files.ReadWrite.All</span></span> |

 > <span data-ttu-id="2c8e9-126">**Nota:** El extremo /v1.0 da permisos de aplicación para la mayoría de los recursos.</span><span class="sxs-lookup"><span data-stu-id="2c8e9-126">**Note:** The /v1.0 endpoint allows application permissions for most resources.</span></span> <span data-ttu-id="2c8e9-127">Las conversaciones de un grupo y los elementos de raíz de la unidad de OneDrive no son compatibles con los permisos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2c8e9-127">Note: The /v1.0 endpoint allows Application permissions for most resources. Conversations in a Group and OneDrive drive root items are not supported with Application permissions.</span></span>

## <a name="http-request"></a><span data-ttu-id="2c8e9-128">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2c8e9-128">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /subscriptions
```

## <a name="request-headers"></a><span data-ttu-id="2c8e9-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2c8e9-129">Request headers</span></span>

| <span data-ttu-id="2c8e9-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="2c8e9-130">Name</span></span>       | <span data-ttu-id="2c8e9-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="2c8e9-131">Type</span></span> | <span data-ttu-id="2c8e9-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c8e9-132">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="2c8e9-133">Authorization</span><span class="sxs-lookup"><span data-stu-id="2c8e9-133">Authorization</span></span>  | <span data-ttu-id="2c8e9-134">cadena</span><span class="sxs-lookup"><span data-stu-id="2c8e9-134">string</span></span>  | <span data-ttu-id="2c8e9-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2c8e9-p103">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="2c8e9-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2c8e9-137">Response</span></span>

<span data-ttu-id="2c8e9-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto de [suscripción](../resources/subscription.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2c8e9-138">If successful, this method returns `201 Created` response code and a [subscription](../resources/subscription.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2c8e9-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2c8e9-139">Example</span></span>

##### <a name="request"></a><span data-ttu-id="2c8e9-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2c8e9-140">Request</span></span>

<span data-ttu-id="2c8e9-141">Este es un ejemplo de solicitud para enviar una notificación cuando el usuario recibe un nuevo correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="2c8e9-141">Here is an example of the request to send a notification when the user receives a new mail.</span></span>
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

<span data-ttu-id="2c8e9-142">En el cuerpo de la solicitud, proporcione una representación JSON del objeto de [suscripción](../resources/subscription.md).</span><span class="sxs-lookup"><span data-stu-id="2c8e9-142">In the request body, supply a JSON representation of the [Contact](../resources/subscription.md) object.</span></span>
<span data-ttu-id="2c8e9-143">El campo `clientState` es opcional.</span><span class="sxs-lookup"><span data-stu-id="2c8e9-143">The `clientState` field is optional.</span></span>

##### <a name="resources-examples"></a><span data-ttu-id="2c8e9-144">Ejemplos de recursos</span><span class="sxs-lookup"><span data-stu-id="2c8e9-144">Resources examples</span></span>

<span data-ttu-id="2c8e9-145">A continuación puede ver algunos valores válidos para la propiedad de recurso de la suscripción:</span><span class="sxs-lookup"><span data-stu-id="2c8e9-145">The following are valid values for the resource property of the subscription:</span></span>

| <span data-ttu-id="2c8e9-146">Tipo de recurso</span><span class="sxs-lookup"><span data-stu-id="2c8e9-146">Resource type</span></span> | <span data-ttu-id="2c8e9-147">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2c8e9-147">Examples</span></span> |
|:------ |:----- |
|<span data-ttu-id="2c8e9-148">Correo</span><span class="sxs-lookup"><span data-stu-id="2c8e9-148">Mail</span></span>|<span data-ttu-id="2c8e9-149">me/mailfolders("inbox")/messages</span><span class="sxs-lookup"><span data-stu-id="2c8e9-149">me/mailfolders('inbox')/messages</span></span><br /><span data-ttu-id="2c8e9-150">me/messages</span><span class="sxs-lookup"><span data-stu-id="2c8e9-150">me/messages</span></span>|
|<span data-ttu-id="2c8e9-151">Contactos</span><span class="sxs-lookup"><span data-stu-id="2c8e9-151">Contacts</span></span>|<span data-ttu-id="2c8e9-152">me/contacts</span><span class="sxs-lookup"><span data-stu-id="2c8e9-152">me/contacts</span></span>|
|<span data-ttu-id="2c8e9-153">Calendarios</span><span class="sxs-lookup"><span data-stu-id="2c8e9-153">Calendars</span></span>|<span data-ttu-id="2c8e9-154">me/events</span><span class="sxs-lookup"><span data-stu-id="2c8e9-154">me/events</span></span>|
|<span data-ttu-id="2c8e9-155">Usuarios</span><span class="sxs-lookup"><span data-stu-id="2c8e9-155">Users</span></span>|<span data-ttu-id="2c8e9-156">users</span><span class="sxs-lookup"><span data-stu-id="2c8e9-156">users</span></span>|
|<span data-ttu-id="2c8e9-157">Grupos</span><span class="sxs-lookup"><span data-stu-id="2c8e9-157">Groups</span></span>|<span data-ttu-id="2c8e9-158">grupos</span><span class="sxs-lookup"><span data-stu-id="2c8e9-158">groups</span></span>|
|<span data-ttu-id="2c8e9-159">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="2c8e9-159">Conversations</span></span>|<span data-ttu-id="2c8e9-160">groups("*{id}*")/conversations</span><span class="sxs-lookup"><span data-stu-id="2c8e9-160">groups('*{id}*')/conversations</span></span>|
|<span data-ttu-id="2c8e9-161">Unidades</span><span class="sxs-lookup"><span data-stu-id="2c8e9-161">Drives</span></span>|<span data-ttu-id="2c8e9-162">me/drive/root</span><span class="sxs-lookup"><span data-stu-id="2c8e9-162">me/drive/root</span></span>|

##### <a name="response"></a><span data-ttu-id="2c8e9-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2c8e9-163">Response</span></span>

<span data-ttu-id="2c8e9-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2c8e9-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

## <a name="notification-endpoint-validation"></a><span data-ttu-id="2c8e9-167">Validación de extremo de notificación</span><span class="sxs-lookup"><span data-stu-id="2c8e9-167">Notification endpoint validation</span></span>

<span data-ttu-id="2c8e9-168">El extremo de la notificación de suscripción (especificado en la propiedad `notificationUrl`) debe ser capaz de responder a una solicitud de validación, como se describe en [Configurar notificaciones para los cambios en los datos de usuario](../../../concepts/webhooks.md#notification-endpoint-validation).</span><span class="sxs-lookup"><span data-stu-id="2c8e9-168">The subscription notification endpoint (specified in the `notificationUrl` property) must be capable of responding to a validation request as described in [Set up notifications for changes in user data](../../../concepts/webhooks.md#notification-endpoint-validation).</span></span> <span data-ttu-id="2c8e9-169">Si se produce un error en la validación, la solicitud para crear la suscripción devuelve un error 400 de solicitud incorrecta.</span><span class="sxs-lookup"><span data-stu-id="2c8e9-169">If validation fails, the request to create the subscription returns a 400 Bad Request error.</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create subscription",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
