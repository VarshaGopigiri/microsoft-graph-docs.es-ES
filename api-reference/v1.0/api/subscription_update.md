# <a name="update-subscription"></a><span data-ttu-id="d9f51-101">Actualizar suscripción</span><span class="sxs-lookup"><span data-stu-id="d9f51-101">Update subscription</span></span>

<span data-ttu-id="d9f51-102">Renovar una suscripción ampliando su tiempo de expiración.</span><span class="sxs-lookup"><span data-stu-id="d9f51-102">Renew a subscription by extending its expiry time.</span></span>

<span data-ttu-id="d9f51-103">Las suscripciones expiran después de un período de tiempo que varía en función del tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="d9f51-103">Subscriptions expire after a length of time that varies by resource type.</span></span> <span data-ttu-id="d9f51-104">Con el fin de evitar la pérdida de notificaciones, una aplicación debe renovar sus suscripciones antes de su fecha de expiración.</span><span class="sxs-lookup"><span data-stu-id="d9f51-104">In order to avoid missing notifications, an app should renew its subscriptions well in advance of their expiry date.</span></span> <span data-ttu-id="d9f51-105">Vea [suscripción](../resources/subscription.md) para conocer la longitud máxima de una suscripción para cada tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="d9f51-105">See [subscription](../resources/subscription.md) for maximum length of a subscription for each resource type.</span></span>

## <a name="permissions"></a><span data-ttu-id="d9f51-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="d9f51-106">Permissions</span></span>

<span data-ttu-id="d9f51-p102">En la tabla siguiente se muestra el permiso propuesto que se requiere para cada recurso. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d9f51-p102">The following table lists the suggested permission needed for each resource. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="d9f51-109">Tipo de recurso o elemento</span><span class="sxs-lookup"><span data-stu-id="d9f51-109">Resource type / Item</span></span>        | <span data-ttu-id="d9f51-110">Permiso</span><span class="sxs-lookup"><span data-stu-id="d9f51-110">Permission</span></span>          |
|-----------------------------|---------------------|
| <span data-ttu-id="d9f51-111">Contactos</span><span class="sxs-lookup"><span data-stu-id="d9f51-111">Contacts</span></span>                    | <span data-ttu-id="d9f51-112">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="d9f51-112">Contacts.Read</span></span>       |
| <span data-ttu-id="d9f51-113">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="d9f51-113">Conversations</span></span>               | <span data-ttu-id="d9f51-114">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="d9f51-114">Group.Read.All</span></span>      |
| <span data-ttu-id="d9f51-115">Eventos</span><span class="sxs-lookup"><span data-stu-id="d9f51-115">Events</span></span>                      | <span data-ttu-id="d9f51-116">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="d9f51-116">Calendars.Read</span></span>      |
| <span data-ttu-id="d9f51-117">Mensajes</span><span class="sxs-lookup"><span data-stu-id="d9f51-117">Messages</span></span>                    | <span data-ttu-id="d9f51-118">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="d9f51-118">Mail.Read</span></span>           |
| <span data-ttu-id="d9f51-119">Grupos</span><span class="sxs-lookup"><span data-stu-id="d9f51-119">Groups</span></span>                      | <span data-ttu-id="d9f51-120">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="d9f51-120">Group.Read.All</span></span>      |
| <span data-ttu-id="d9f51-121">Usuarios</span><span class="sxs-lookup"><span data-stu-id="d9f51-121">Users</span></span>                       | <span data-ttu-id="d9f51-122">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="d9f51-122">User.Read.All</span></span>       |
| <span data-ttu-id="d9f51-123">Unidad de disco (OneDrive del usuario)</span><span class="sxs-lookup"><span data-stu-id="d9f51-123">Drive  (User's OneDrive)</span></span>    | <span data-ttu-id="d9f51-124">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d9f51-124">Files.ReadWrite</span></span>     |
| <span data-ttu-id="d9f51-125">Unidades de disco (unidades de disco y contenido compartido de SharePoint)</span><span class="sxs-lookup"><span data-stu-id="d9f51-125">Drives (Sharepoint shared content and drives)</span></span> | <span data-ttu-id="d9f51-126">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d9f51-126">Files.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="d9f51-127">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d9f51-127">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PATCH /subscriptions/{id}
```

## <a name="request-headers"></a><span data-ttu-id="d9f51-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d9f51-128">Request headers</span></span>

| <span data-ttu-id="d9f51-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="d9f51-129">Name</span></span>       | <span data-ttu-id="d9f51-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="d9f51-130">Type</span></span> | <span data-ttu-id="d9f51-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9f51-131">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="d9f51-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="d9f51-132">Authorization</span></span>  | <span data-ttu-id="d9f51-133">cadena</span><span class="sxs-lookup"><span data-stu-id="d9f51-133">string</span></span>  | <span data-ttu-id="d9f51-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d9f51-p103">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="d9f51-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d9f51-136">Response</span></span>

<span data-ttu-id="d9f51-137">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [subscription](../resources/subscription.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d9f51-137">If successful, this method returns a `200 OK` response code and [subscription](../resources/subscription.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d9f51-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d9f51-138">Example</span></span>

##### <a name="request"></a><span data-ttu-id="d9f51-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d9f51-139">Request</span></span>

<span data-ttu-id="d9f51-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d9f51-140">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="d9f51-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d9f51-141">Response</span></span>

<span data-ttu-id="d9f51-142">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d9f51-142">Here is an example of the response.</span></span>
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
