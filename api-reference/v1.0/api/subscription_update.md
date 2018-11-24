# <a name="update-subscription"></a><span data-ttu-id="a7eab-101">Update subscription</span><span class="sxs-lookup"><span data-stu-id="a7eab-101">Update subscription</span></span>

<span data-ttu-id="a7eab-102">Renueva una suscripción ampliando su tiempo de expiración.</span><span class="sxs-lookup"><span data-stu-id="a7eab-102">Renew a subscription by extending its expiry time.</span></span>

<span data-ttu-id="a7eab-103">Las suscripciones caducan después de un período de tiempo que varía en función del tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="a7eab-103">Subscriptions expire after a length of time that varies by resource type.</span></span> <span data-ttu-id="a7eab-104">Con el fin de evitar la pérdida de notificaciones, una aplicación debe renovar sus suscripciones antes de su fecha de expiración.</span><span class="sxs-lookup"><span data-stu-id="a7eab-104">In order to avoid missing notifications, an app should renew its subscriptions well in advance of their expiry date.</span></span> <span data-ttu-id="a7eab-105">Vea la [suscripción](../resources/subscription.md) para la longitud máxima de una suscripción para cada tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="a7eab-105">See [subscription](../resources/subscription.md) for maximum length of a subscription for each resource type.</span></span>

## <a name="permissions"></a><span data-ttu-id="a7eab-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="a7eab-106">Permissions</span></span>

<span data-ttu-id="a7eab-p102">En la tabla siguiente se muestra el permiso propuesto que se requiere para cada recurso. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a7eab-p102">The following table lists the suggested permission needed for each resource. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="a7eab-109">Tipo de recurso o elemento</span><span class="sxs-lookup"><span data-stu-id="a7eab-109">Resource type / Item</span></span>        | <span data-ttu-id="a7eab-110">Permiso</span><span class="sxs-lookup"><span data-stu-id="a7eab-110">Permission</span></span>          |
|-----------------------------|---------------------|
| <span data-ttu-id="a7eab-111">Contactos</span><span class="sxs-lookup"><span data-stu-id="a7eab-111">Contacts</span></span>                    | <span data-ttu-id="a7eab-112">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="a7eab-112">Contacts.Read</span></span>       |
| <span data-ttu-id="a7eab-113">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="a7eab-113">Conversations</span></span>               | <span data-ttu-id="a7eab-114">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="a7eab-114">Group.Read.All</span></span>      |
| <span data-ttu-id="a7eab-115">Eventos</span><span class="sxs-lookup"><span data-stu-id="a7eab-115">Events</span></span>                      | <span data-ttu-id="a7eab-116">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="a7eab-116">Calendars.Read</span></span>      |
| <span data-ttu-id="a7eab-117">Mensajes</span><span class="sxs-lookup"><span data-stu-id="a7eab-117">Messages</span></span>                    | <span data-ttu-id="a7eab-118">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="a7eab-118">Mail.Read</span></span>           |
| <span data-ttu-id="a7eab-119">Groups</span><span class="sxs-lookup"><span data-stu-id="a7eab-119">Groups</span></span>                      | <span data-ttu-id="a7eab-120">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="a7eab-120">Group.Read.All</span></span>      |
| <span data-ttu-id="a7eab-121">Users</span><span class="sxs-lookup"><span data-stu-id="a7eab-121">Users</span></span>                       | <span data-ttu-id="a7eab-122">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="a7eab-122">User.Read.All</span></span>       |
| <span data-ttu-id="a7eab-123">Unidad de disco (OneDrive del usuario)</span><span class="sxs-lookup"><span data-stu-id="a7eab-123">Drive  (User's OneDrive)</span></span>    | <span data-ttu-id="a7eab-124">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a7eab-124">Files.ReadWrite</span></span>     |
| <span data-ttu-id="a7eab-125">Unidades (contenido de SharePoint compartido y unidades)</span><span class="sxs-lookup"><span data-stu-id="a7eab-125">Drives (SharePoint shared content and drives)</span></span> | <span data-ttu-id="a7eab-126">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a7eab-126">Files.ReadWrite.All</span></span> |
|<span data-ttu-id="a7eab-127">Alerta de seguridad</span><span class="sxs-lookup"><span data-stu-id="a7eab-127">Security alert</span></span>| <span data-ttu-id="a7eab-128">SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a7eab-128">SecurityEvents.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="a7eab-129">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a7eab-129">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PATCH /subscriptions/{id}
```

## <a name="request-headers"></a><span data-ttu-id="a7eab-130">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a7eab-130">Request headers</span></span>

| <span data-ttu-id="a7eab-131">Nombre</span><span class="sxs-lookup"><span data-stu-id="a7eab-131">Name</span></span>       | <span data-ttu-id="a7eab-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="a7eab-132">Type</span></span> | <span data-ttu-id="a7eab-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7eab-133">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="a7eab-134">Authorization</span><span class="sxs-lookup"><span data-stu-id="a7eab-134">Authorization</span></span>  | <span data-ttu-id="a7eab-135">string</span><span class="sxs-lookup"><span data-stu-id="a7eab-135">string</span></span>  | <span data-ttu-id="a7eab-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a7eab-p103">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="a7eab-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a7eab-138">Response</span></span>

<span data-ttu-id="a7eab-139">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [subscription](../resources/subscription.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a7eab-139">If successful, this method returns a `200 OK` response code and [subscription](../resources/subscription.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a7eab-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a7eab-140">Example</span></span>

##### <a name="request"></a><span data-ttu-id="a7eab-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a7eab-141">Request</span></span>

<span data-ttu-id="a7eab-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a7eab-142">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_subscription"
}-->

```http
PATCH https://graph.microsoft.com/v1.0/subscriptions/{id}
Content-type: application/json

{
   "expirationDateTime":"2016-11-22T18:23:45.9356913Z"
}
```

##### <a name="response"></a><span data-ttu-id="a7eab-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a7eab-143">Response</span></span>

<span data-ttu-id="a7eab-144">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a7eab-144">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.subscription"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 252

{
  "id":"7f105c7d-2dc5-4530-97cd-4e7ae6534c07",
  "resource":"me/messages",
  "applicationId": "24d3b144-21ae-4080-943f-7067b395b913",
  "changeType":"created,updated",
  "clientState":"subscription-identifier",
  "notificationUrl":"https://webhook.azurewebsites.net/api/send/myNotifyClient",
  "expirationDateTime":"2016-11-22T18:23:45.9356913Z",
  "creatorId": "8ee44408-0679-472c-bc2a-692812af3437"
}
```

<!-- {
  "type": "#page.annotation",
  "description": "Update subscription",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
