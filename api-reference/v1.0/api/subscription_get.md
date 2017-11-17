# <a name="get-subscription"></a><span data-ttu-id="6d05c-101">Get subscription</span><span class="sxs-lookup"><span data-stu-id="6d05c-101">Get subscription</span></span>

<span data-ttu-id="6d05c-102">Recupera las propiedades y relaciones de una suscripción.</span><span class="sxs-lookup"><span data-stu-id="6d05c-102">Retrieve the properties and relationships of a subscription.</span></span>
## <a name="permissions"></a><span data-ttu-id="6d05c-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="6d05c-103">Permissions</span></span>

<span data-ttu-id="6d05c-p101">En la tabla siguiente se muestra el permiso propuesto que se requiere para cada recurso. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="6d05c-p101">The following table lists the suggested permission needed for each resource. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="6d05c-106">Tipo de recurso o elemento</span><span class="sxs-lookup"><span data-stu-id="6d05c-106">Resource type / Item</span></span>        | <span data-ttu-id="6d05c-107">Permiso</span><span class="sxs-lookup"><span data-stu-id="6d05c-107">Permission</span></span>          |
|-----------------------------|---------------------|
| <span data-ttu-id="6d05c-108">Contactos</span><span class="sxs-lookup"><span data-stu-id="6d05c-108">Contacts</span></span>                    | <span data-ttu-id="6d05c-109">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="6d05c-109">Contacts.Read</span></span>       |
| <span data-ttu-id="6d05c-110">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="6d05c-110">Conversations</span></span>               | <span data-ttu-id="6d05c-111">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="6d05c-111">Group.Read.All</span></span>      |
| <span data-ttu-id="6d05c-112">Eventos</span><span class="sxs-lookup"><span data-stu-id="6d05c-112">Events</span></span>                      | <span data-ttu-id="6d05c-113">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="6d05c-113">Calendars.Read</span></span>      |
| <span data-ttu-id="6d05c-114">Mensajes</span><span class="sxs-lookup"><span data-stu-id="6d05c-114">Messages</span></span>                    | <span data-ttu-id="6d05c-115">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="6d05c-115">Mail.Read</span></span>           |
| <span data-ttu-id="6d05c-116">Unidad de disco (OneDrive del usuario)</span><span class="sxs-lookup"><span data-stu-id="6d05c-116">Drive  (User's OneDrive)</span></span>    | <span data-ttu-id="6d05c-117">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6d05c-117">Files.ReadWrite</span></span>     |
| <span data-ttu-id="6d05c-118">Unidades de disco (unidades de disco y contenido compartido de SharePoint)</span><span class="sxs-lookup"><span data-stu-id="6d05c-118">Drives (Sharepoint shared content and drives)</span></span> | <span data-ttu-id="6d05c-119">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6d05c-119">Files.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="6d05c-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6d05c-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /subscriptions/{subscriptionId}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="6d05c-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="6d05c-121">Optional query parameters</span></span>
<span data-ttu-id="6d05c-122">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6d05c-122">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="6d05c-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6d05c-123">Request headers</span></span>
| <span data-ttu-id="6d05c-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="6d05c-124">Name</span></span>       | <span data-ttu-id="6d05c-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="6d05c-125">Type</span></span> | <span data-ttu-id="6d05c-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="6d05c-126">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="6d05c-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="6d05c-127">Authorization</span></span>  | <span data-ttu-id="6d05c-128">string</span><span class="sxs-lookup"><span data-stu-id="6d05c-128">string</span></span>  | <span data-ttu-id="6d05c-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6d05c-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6d05c-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6d05c-131">Request body</span></span>
<span data-ttu-id="6d05c-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6d05c-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6d05c-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6d05c-133">Response</span></span>

<span data-ttu-id="6d05c-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [subscription](../resources/subscription.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6d05c-134">If successful, this method returns a `200 OK` response code and [subscription](../resources/subscription.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="6d05c-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6d05c-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6d05c-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6d05c-136">Request</span></span>
<span data-ttu-id="6d05c-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6d05c-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_subscription"
}-->
```http
GET https://graph.microsoft.com/v1.0/subscriptions/{subscriptionId}
```
##### <a name="response"></a><span data-ttu-id="6d05c-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6d05c-138">Response</span></span>
<span data-ttu-id="6d05c-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6d05c-139">Here is an example of the response.</span></span>
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
  "expirationDateTime":"2016-11-20T18:23:45.9356913Z"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get subscription",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
