# <a name="update-subscription"></a><span data-ttu-id="4834f-101">Update subscription</span><span class="sxs-lookup"><span data-stu-id="4834f-101">Update subscription</span></span>

<span data-ttu-id="4834f-102">Renueva una suscripción ampliando su tiempo de expiración.</span><span class="sxs-lookup"><span data-stu-id="4834f-102">Renew a subscription by extending its expiry time.</span></span>

<span data-ttu-id="4834f-p101">Las suscripciones a recursos caducan en fechas prohibidas por los tipos de recursos individuales.  Para no perder las notificaciones, las suscripciones deben renovarse antes de su fecha de expiración.  Consulte [subscription](../resources/subscription.md) para más información sobre fechas de expiración individuales.</span><span class="sxs-lookup"><span data-stu-id="4834f-p101">Subscriptions to resources expire at dates proscribed by the individual resource types.  In order not to miss notifications, subscriptions should be renewed well in advance of their expiry date.  See [subscription](../resources/subscription.md) for individual expiry dates.</span></span>

## <a name="permissions"></a><span data-ttu-id="4834f-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="4834f-106">Permissions</span></span>

<span data-ttu-id="4834f-p102">En la tabla siguiente se muestra el permiso propuesto que se requiere para cada recurso. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="4834f-p102">The following table lists the suggested permission needed for each resource. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="4834f-109">Tipo de recurso o elemento</span><span class="sxs-lookup"><span data-stu-id="4834f-109">Resource type / Item</span></span>        | <span data-ttu-id="4834f-110">Permiso</span><span class="sxs-lookup"><span data-stu-id="4834f-110">Permission</span></span>          |
|-----------------------------|---------------------|
| <span data-ttu-id="4834f-111">Contactos</span><span class="sxs-lookup"><span data-stu-id="4834f-111">Contacts</span></span>                    | <span data-ttu-id="4834f-112">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="4834f-112">Contacts.Read</span></span>       |
| <span data-ttu-id="4834f-113">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="4834f-113">Conversations</span></span>               | <span data-ttu-id="4834f-114">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="4834f-114">Group.Read.All</span></span>      |
| <span data-ttu-id="4834f-115">Eventos</span><span class="sxs-lookup"><span data-stu-id="4834f-115">Events</span></span>                      | <span data-ttu-id="4834f-116">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="4834f-116">Calendars.Read</span></span>      |
| <span data-ttu-id="4834f-117">Mensajes</span><span class="sxs-lookup"><span data-stu-id="4834f-117">Messages</span></span>                    | <span data-ttu-id="4834f-118">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="4834f-118">Mail.Read</span></span>           |
| <span data-ttu-id="4834f-119">Unidad de disco (OneDrive del usuario)</span><span class="sxs-lookup"><span data-stu-id="4834f-119">Drive  (User's OneDrive)</span></span>    | <span data-ttu-id="4834f-120">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4834f-120">Files.ReadWrite</span></span>     |
| <span data-ttu-id="4834f-121">Unidades de disco (unidades de disco y contenido compartido de SharePoint)</span><span class="sxs-lookup"><span data-stu-id="4834f-121">Drives (Sharepoint shared content and drives)</span></span> | <span data-ttu-id="4834f-122">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4834f-122">Files.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="4834f-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4834f-123">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /subscriptions/{subscriptionId}
```

## <a name="request-headers"></a><span data-ttu-id="4834f-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4834f-124">Request headers</span></span>
| <span data-ttu-id="4834f-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="4834f-125">Name</span></span>       | <span data-ttu-id="4834f-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="4834f-126">Type</span></span> | <span data-ttu-id="4834f-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="4834f-127">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="4834f-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="4834f-128">Authorization</span></span>  | <span data-ttu-id="4834f-129">string</span><span class="sxs-lookup"><span data-stu-id="4834f-129">string</span></span>  | <span data-ttu-id="4834f-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4834f-p103">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="4834f-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4834f-132">Response</span></span>

<span data-ttu-id="4834f-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [subscription](../resources/subscription.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4834f-133">If successful, this method returns a `200 OK` response code and [subscription](../resources/subscription.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="4834f-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4834f-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4834f-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4834f-135">Request</span></span>
<span data-ttu-id="4834f-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4834f-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_subscription"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/subscriptions/{subscriptionId}
Content-type: application/json

{
   "expirationDateTime":"2016-11-22T18:23:45.9356913Z"
}
```

##### <a name="response"></a><span data-ttu-id="4834f-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4834f-137">Response</span></span>
<span data-ttu-id="4834f-138">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4834f-138">Here is an example of the response.</span></span>
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
  "changeType":"created,updated",
  "clientState":"subscription-identifier",
  "notificationUrl":"https://webhook.azurewebsites.net/api/send/myNotifyClient",
  "expirationDateTime":"2016-11-22T18:23:45.9356913Z"
}
```


<!-- {
  "type": "#page.annotation",
  "description": "Update subscription",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
