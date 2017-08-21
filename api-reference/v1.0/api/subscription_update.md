# <a name="update-subscription"></a><span data-ttu-id="52357-101">Update subscription</span><span class="sxs-lookup"><span data-stu-id="52357-101">Update subscription</span></span>

<span data-ttu-id="52357-102">Renueva una suscripción ampliando su tiempo de expiración.</span><span class="sxs-lookup"><span data-stu-id="52357-102">Renew a subscription by extending its expiry time.</span></span>

<span data-ttu-id="52357-p101">Las suscripciones a recursos caducan en fechas prohibidas por los tipos de recursos individuales.  Para no perder las notificaciones, las suscripciones deben renovarse antes de su fecha de expiración.  Consulte [subscription](../resources/subscription.md) para más información sobre fechas de expiración individuales.</span><span class="sxs-lookup"><span data-stu-id="52357-p101">Subscriptions to resources expire at dates proscribed by the individual resource types.  In order not to miss notifications, subscriptions should be renewed well in advance of their expiry date.  See [subscription](../resources/subscription.md) for individual expiry dates.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="52357-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="52357-106">Prerequisites</span></span>

<span data-ttu-id="52357-107">En la tabla siguiente se muestra el permiso propuesto que se requiere para cada recurso.</span><span class="sxs-lookup"><span data-stu-id="52357-107">The following table lists the suggested permission needed for each resource.</span></span>

| <span data-ttu-id="52357-108">Tipo de recurso o elemento</span><span class="sxs-lookup"><span data-stu-id="52357-108">Resource type / Item</span></span>        | <span data-ttu-id="52357-109">Ámbito</span><span class="sxs-lookup"><span data-stu-id="52357-109">Scope</span></span>               |
|-----------------------------|---------------------|
| <span data-ttu-id="52357-110">Contactos</span><span class="sxs-lookup"><span data-stu-id="52357-110">Contacts</span></span>                    | <span data-ttu-id="52357-111">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="52357-111">Contacts.Read</span></span>       |
| <span data-ttu-id="52357-112">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="52357-112">Conversations</span></span>               | <span data-ttu-id="52357-113">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="52357-113">Group.Read.All</span></span>      |
| <span data-ttu-id="52357-114">Eventos</span><span class="sxs-lookup"><span data-stu-id="52357-114">Events</span></span>                      | <span data-ttu-id="52357-115">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="52357-115">Calendars.Read</span></span>      |
| <span data-ttu-id="52357-116">Mensajes</span><span class="sxs-lookup"><span data-stu-id="52357-116">Messages</span></span>                    | <span data-ttu-id="52357-117">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="52357-117">Mail.Read</span></span>           |
| <span data-ttu-id="52357-118">Unidad de disco (OneDrive del usuario)</span><span class="sxs-lookup"><span data-stu-id="52357-118">Drive  (User's OneDrive)</span></span>    | <span data-ttu-id="52357-119">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="52357-119">Files.ReadWrite</span></span>     |
| <span data-ttu-id="52357-120">Unidades de disco (unidades de disco y contenido compartido de SharePoint)</span><span class="sxs-lookup"><span data-stu-id="52357-120">Drives (Sharepoint shared content and drives)</span></span> | <span data-ttu-id="52357-121">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="52357-121">Files.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="52357-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="52357-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /subscriptions/{subscriptionId}
```

## <a name="request-headers"></a><span data-ttu-id="52357-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="52357-123">Request headers</span></span>
| <span data-ttu-id="52357-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="52357-124">Name</span></span>       | <span data-ttu-id="52357-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="52357-125">Type</span></span> | <span data-ttu-id="52357-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="52357-126">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="52357-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="52357-127">Authorization</span></span>  | <span data-ttu-id="52357-128">string</span><span class="sxs-lookup"><span data-stu-id="52357-128">string</span></span>  | <span data-ttu-id="52357-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="52357-p102">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="52357-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="52357-131">Response</span></span>

<span data-ttu-id="52357-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [subscription](../resources/subscription.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="52357-132">If successful, this method returns a `200 OK` response code and [subscription](../resources/subscription.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="52357-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="52357-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="52357-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="52357-134">Request</span></span>
<span data-ttu-id="52357-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="52357-135">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="52357-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="52357-136">Response</span></span>
<span data-ttu-id="52357-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="52357-137">Here is an example of the response.</span></span>
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
