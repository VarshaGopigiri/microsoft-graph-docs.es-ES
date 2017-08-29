# <a name="create-subscription"></a><span data-ttu-id="c2225-101">Crear suscripción</span><span class="sxs-lookup"><span data-stu-id="c2225-101">Create subscription</span></span>

<span data-ttu-id="c2225-102">Suscripción a una aplicación de escucha para recibir notificaciones cuando cambian los datos en Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="c2225-102">Subscribes a listener application to receive notifications when data on the Microsoft Graph changes.</span></span>
## <a name="permissions"></a><span data-ttu-id="c2225-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="c2225-103">Permissions</span></span>
<span data-ttu-id="c2225-p101">La creación de una suscripción requiere un ámbito de lectura para el recurso. Por ejemplo, para obtener mensajes de notificaciones, la aplicación necesita el permiso `Mail.Read`. En la tabla siguiente se muestra el permiso propuesto que se requiere para cada recurso. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c2225-p101">Creating a subscription requires read scope to the resource. For example, to get notifications messages, your app needs the `Mail.Read` permission. The following table lists the suggested permission needed for each resource. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="c2225-108">Tipo de recurso o elemento</span><span class="sxs-lookup"><span data-stu-id="c2225-108">Resource type / Item</span></span>        | <span data-ttu-id="c2225-109">Permiso</span><span class="sxs-lookup"><span data-stu-id="c2225-109">Permission</span></span>          |
|-----------------------------|---------------------|
| <span data-ttu-id="c2225-110">Contactos</span><span class="sxs-lookup"><span data-stu-id="c2225-110">Contacts</span></span>                    | <span data-ttu-id="c2225-111">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="c2225-111">Contacts.Read</span></span>       |
| <span data-ttu-id="c2225-112">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="c2225-112">Conversations</span></span>               | <span data-ttu-id="c2225-113">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="c2225-113">Group.Read.All</span></span>      |
| <span data-ttu-id="c2225-114">Eventos</span><span class="sxs-lookup"><span data-stu-id="c2225-114">Events</span></span>                      | <span data-ttu-id="c2225-115">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="c2225-115">Calendars.Read</span></span>      |
| <span data-ttu-id="c2225-116">Mensajes</span><span class="sxs-lookup"><span data-stu-id="c2225-116">Messages</span></span>                    | <span data-ttu-id="c2225-117">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="c2225-117">Mail.Read</span></span>           |
| <span data-ttu-id="c2225-118">Unidad de disco (OneDrive del usuario)</span><span class="sxs-lookup"><span data-stu-id="c2225-118">Drive  (User's OneDrive)</span></span>    | <span data-ttu-id="c2225-119">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c2225-119">Files.ReadWrite</span></span>     |
| <span data-ttu-id="c2225-120">Unidades de disco (unidades de disco y contenido compartido de SharePoint)</span><span class="sxs-lookup"><span data-stu-id="c2225-120">Drives (Sharepoint shared content and drives)</span></span> | <span data-ttu-id="c2225-121">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c2225-121">Files.ReadWrite.All</span></span> |

 <span data-ttu-id="c2225-p102">***Nota:*** El punto de conexión /v1.0 permite permisos de aplicación para la mayoría de recursos. Las conversaciones de un grupo y los elementos de raíz de unidad de OneDrive no son compatibles con los permisos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c2225-p102">One of the following scopes, depending on the target resource, are required to execute this API: Mail.Read, Calendars.Read, Contacts.Read, Group.Read.All, Files.ReadWrite or Files.ReadWrite.All. ***Note:*** The /v1.0 endpoint allows Application permissions for most resources. Conversations in a Group and OneDrive drive root items are not supported with Application permissions.</span></span>

## <a name="http-request"></a><span data-ttu-id="c2225-124">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c2225-124">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->

```http
POST /subscriptions

```

## <a name="request-headers"></a><span data-ttu-id="c2225-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c2225-125">Request headers</span></span>
| <span data-ttu-id="c2225-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="c2225-126">Name</span></span>       | <span data-ttu-id="c2225-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="c2225-127">Type</span></span> | <span data-ttu-id="c2225-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2225-128">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="c2225-129">Authorization</span><span class="sxs-lookup"><span data-stu-id="c2225-129">Authorization</span></span>  | <span data-ttu-id="c2225-130">string</span><span class="sxs-lookup"><span data-stu-id="c2225-130">string</span></span>  | <span data-ttu-id="c2225-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c2225-p103">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="c2225-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2225-133">Response</span></span>

<span data-ttu-id="c2225-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `201, Created` y un objeto de [suscripción](../resources/subscription.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c2225-134">If successful, this method returns `201, Created` response code and a [subscription](../resources/subscription.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c2225-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c2225-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c2225-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c2225-136">Request</span></span>
<span data-ttu-id="c2225-137">Este es un ejemplo de solicitud para enviar una notificación cuando el usuario recibe un nuevo correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="c2225-137">Here is an example of the request to send a notification when the user receives a new mail.</span></span>
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
   "clientState": "subscription-identifier"
}
```
<span data-ttu-id="c2225-p104">En el cuerpo de la solicitud, proporcione una representación JSON del objeto de [suscripción](../resources/subscription.md). El campo *clientState* es opcional.</span><span class="sxs-lookup"><span data-stu-id="c2225-p104">In the request body, supply a JSON representation of the [subscription](../resources/subscription.md) object. The *clientState* field is optional.</span></span>

##### <a name="resources-examples"></a><span data-ttu-id="c2225-140">Ejemplos de recursos</span><span class="sxs-lookup"><span data-stu-id="c2225-140">Resources examples</span></span>
<span data-ttu-id="c2225-141">A continuación puede ver algunos valores válidos para la propiedad de recurso de la suscripción:</span><span class="sxs-lookup"><span data-stu-id="c2225-141">The following are valid values for the resource property of the subscription:</span></span>

| <span data-ttu-id="c2225-142">Tipo de recurso</span><span class="sxs-lookup"><span data-stu-id="c2225-142">Resource type</span></span> | <span data-ttu-id="c2225-143">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c2225-143">Examples</span></span> |
|:------ |:----- |
|<span data-ttu-id="c2225-144">Correo</span><span class="sxs-lookup"><span data-stu-id="c2225-144">Mail</span></span>|<span data-ttu-id="c2225-145">me/mailfolders("inbox")/messages</span><span class="sxs-lookup"><span data-stu-id="c2225-145">me/mailfolders('inbox')/messages</span></span><br /><span data-ttu-id="c2225-146">me/messages</span><span class="sxs-lookup"><span data-stu-id="c2225-146">me/messages</span></span>|
|<span data-ttu-id="c2225-147">Contactos</span><span class="sxs-lookup"><span data-stu-id="c2225-147">Contacts</span></span>|<span data-ttu-id="c2225-148">me/contacts</span><span class="sxs-lookup"><span data-stu-id="c2225-148">me/contacts</span></span>|
|<span data-ttu-id="c2225-149">Calendarios</span><span class="sxs-lookup"><span data-stu-id="c2225-149">Calendars</span></span>|<span data-ttu-id="c2225-150">me/events</span><span class="sxs-lookup"><span data-stu-id="c2225-150">me/events</span></span>|
|<span data-ttu-id="c2225-151">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="c2225-151">Conversations</span></span>|<span data-ttu-id="c2225-152">groups("*{id}*")/conversations</span><span class="sxs-lookup"><span data-stu-id="c2225-152">groups('*{id}*')/conversations</span></span>|
|<span data-ttu-id="c2225-153">Unidades</span><span class="sxs-lookup"><span data-stu-id="c2225-153">Drives</span></span>|<span data-ttu-id="c2225-154">me/drive/root</span><span class="sxs-lookup"><span data-stu-id="c2225-154">me/drive/root</span></span>|

##### <a name="response"></a><span data-ttu-id="c2225-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2225-155">Response</span></span>
<span data-ttu-id="c2225-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c2225-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.subscription"
} -->
```http
HTTP/1.1 201 Created

{
  "id":"7f105c7d-2dc5-4530-97cd-4e7ae6534c07",
  "resource":"me/mailFolders('Inbox')/messages",
  "changeType":"created, updated",
  "clientState":"subscription-identifier",
  "notificationUrl":"https://webhook.azurewebsites.net/api/send/myNotifyClient",
  "expirationDateTime":"2016-11-20T18:23:45.9356913Z"
}
```
## <a name="subscription-validation"></a><span data-ttu-id="c2225-159">Validación de suscripciones</span><span class="sxs-lookup"><span data-stu-id="c2225-159">Subscription validation</span></span>
<span data-ttu-id="c2225-p106">Para evitar que las suscripciones equivocadas envíen notificaciones a direcciones URL arbitrarias, el extremo de la notificación de suscripción debe ser capaz de responder a una solicitud de validación. Durante el procesamiento del `POST` al extremo de `/subscriptions`, Microsoft Graph enviará una solicitud de `POST` a su `notificationUrl` de la siguiente forma:</span><span class="sxs-lookup"><span data-stu-id="c2225-p106">In order to to avoid mistaken subscriptions directing notifications to arbitrary URLs, the subscription notification endpoint must be capable of responding to a validation request. During processing of the `POST` to the `/subscriptions` endpoint, the Microsoft Graph will send a `POST` request back to your `notificationUrl` in the following form:</span></span> 
```http
POST https://webhook.azurewebsites.net/api/send/myNotifyClient?validationToken=<token>
```
<span data-ttu-id="c2225-162">El extremo de notificación debe enviar en menos de 10 segundos una respuesta 200 con el valor `<token>` como cuerpo y un tipo de contenido `text/plain`, como se muestra a continuación, o se descartará la solicitud de creación.</span><span class="sxs-lookup"><span data-stu-id="c2225-162">The notification endpoint must send a 200 response with the value of `<token>` as its body and a content type of `text/plain`, as shown below, within 10 seconds otherwise the creation request will be discarded.</span></span>
```http
HTTP/1.1 200 OK
Content-type: text/plain
Content-length: 7
<token>
```
## <a name="notification-payload"></a><span data-ttu-id="c2225-163">Carga de notificaciones</span><span class="sxs-lookup"><span data-stu-id="c2225-163">Notification payload</span></span>
<span data-ttu-id="c2225-p107">Cuando el recurso suscrito cambia, la herramienta de webhooks envía una notificación a su dirección URL de notificación con la siguiente carga.  El extremo de notificación debe enviar una respuesta 200 o 204 sin cuerpo de respuesta en menos de 30 segundos o se intentará volver a enviar la notificación en intervalos que aumentan de manera exponencial.  Los servicios que tardan constantemente 30 segundos o más pueden limitarse y recibir un conjunto de notificaciones más escaso.</span><span class="sxs-lookup"><span data-stu-id="c2225-p107">When the subscribed resource changes, the webhooks facility sends a notification to your notification URL with the following payload.  The notification endpoint must send a response of 200 or 204 with no response body within 30 seconds otherwise the notification attempt will be retried at exponentially increasing intervals.  Services that consistently take 30 seconds or more may be throttled and receive a sparser notification set.</span></span>

<span data-ttu-id="c2225-167">Los servicios también pueden devolver una respuesta 422 desde una notificación, en cuyo caso la suscripción se eliminará automáticamente y la secuencia de notificaciones se detendrá.</span><span class="sxs-lookup"><span data-stu-id="c2225-167">Services may also return a 422 response from a notification, in which case the subscription will be automatically deleted and the stream of notifications will come to a halt.</span></span>

<span data-ttu-id="c2225-168">En función del recurso suscrito, un campo resourceData adicional puede proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="c2225-168">Depending on the subscribed resource, an additional resourceData field may provide additional information.</span></span>

```http
{
   "value":[
      {
         "subscriptionId":"7f105c7d-2dc5-4530-97cd-4e7ae6534c07",
         "subscriptionExpirationDateTime":"2015-11-20T18:23:45.9356913Z",
         "clientState":"subscription-identifier",
         "changeType":"Created",
         "resource":"Users/ddfcd489-628b-7d04-b48b-20075df800e5@1717622f-1d94-c0d4-9d74-f907ad6677b4/messages/AAMkADMxZmEzMDM1LTFjODQtNGVkMC04YzY3LTBjZTRlNDFjNGE4MwBGAAAAAAAr-q_ZG7oXSaqxum7oZW5RBwCoeN6SYXGLRrvRm_CYrrfQAAAAAAEMAACoeN6SYXGLRrvRm_CYrrfQAACvtMe6AAA=",
         "resourceData":{
            "@odata.type":"#Microsoft.Graph.Message",
            "@odata.id":"Users/ddfcd489-628b-7d04-b48b-20075df800e5@1717622f-1d94-c0d4-9d74-f907ad6677b4/messages/AAMkADMxZmEzMDM1LTFjODQtNGVkMC04YzY3LTBjZTRlNDFjNGE4MwBGAAAAAAAr-q_ZG7oXSaqxum7oZW5RBwCoeN6SYXGLRrvRm_CYrrfQAAAAAAEMAACoeN6SYXGLRrvRm_CYrrfQAACvtMe6AAA=",
            "@odata.etag":"W/\"CQAAABYAAACoeN6SYXGLRrvRm+CYrrfQAACvvGdb\"",
            "Id":"AAMkADMxZmEzMDM1LTFjODQtNGVkMC04YzY3LTBjZTRlNDFjNGE4MwBGAAAAAAAr-q_ZG7oXSaqxum7oZW5RBwCoeN6SYXGLRrvRm_CYrrfQAAAAAAEMAACoeN6SYXGLRrvRm_CYrrfQAACvtMe6AAA="
         }
      }
   ]
}
```
<span data-ttu-id="c2225-p108">Al recibir notificaciones de suscripciones de unidad, el campo resourceData será NULL y se deberá llamar a la API de [delta](item_delta.md) para determinar los cambios que han ocurrido. Aquí tiene un ejemplo de notificación de unidad:</span><span class="sxs-lookup"><span data-stu-id="c2225-p108">When receiving notifications from Drive subscriptions the resourceData will be null and the [delta](item_delta.md) API should be called to determine the changes that have occured. Here is an example of a Drive notification:</span></span>
```http
{
  "subscriptionId": "aa269f87-2a92-4cff-a43e-2771878c3727",
  "clientState": "My client state",
  "changeType": "updated",
  "resource": "me/drive/root",
  "subscriptionExpirationDateTime": "2016-08-26T23:08:37.00+00:00",
  "resourceData": null
}
```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create subscription",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
