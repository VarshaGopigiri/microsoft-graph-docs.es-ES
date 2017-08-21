# <a name="get-subscription"></a><span data-ttu-id="e0462-101">Get subscription</span><span class="sxs-lookup"><span data-stu-id="e0462-101">Get subscription</span></span>

<span data-ttu-id="e0462-102">Recupera las propiedades y relaciones de un objeto subscription.</span><span class="sxs-lookup"><span data-stu-id="e0462-102">Retrieve the properties and relationships of a subscription.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e0462-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e0462-103">Prerequisites</span></span>

<span data-ttu-id="e0462-104">En la tabla siguiente se muestra el permiso propuesto que se requiere para cada recurso.</span><span class="sxs-lookup"><span data-stu-id="e0462-104">The following table lists the suggested permission needed for each resource.</span></span>

| <span data-ttu-id="e0462-105">Tipo de recurso o elemento</span><span class="sxs-lookup"><span data-stu-id="e0462-105">Resource type / Item</span></span>        | <span data-ttu-id="e0462-106">Ámbito</span><span class="sxs-lookup"><span data-stu-id="e0462-106">Scope</span></span>               |
|-----------------------------|---------------------|
| <span data-ttu-id="e0462-107">Contactos</span><span class="sxs-lookup"><span data-stu-id="e0462-107">Contacts</span></span>                    | <span data-ttu-id="e0462-108">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="e0462-108">Contacts.Read</span></span>       |
| <span data-ttu-id="e0462-109">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="e0462-109">Conversations</span></span>               | <span data-ttu-id="e0462-110">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="e0462-110">Group.Read.All</span></span>      |
| <span data-ttu-id="e0462-111">Eventos</span><span class="sxs-lookup"><span data-stu-id="e0462-111">Events</span></span>                      | <span data-ttu-id="e0462-112">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="e0462-112">Calendars.Read</span></span>      |
| <span data-ttu-id="e0462-113">Mensajes</span><span class="sxs-lookup"><span data-stu-id="e0462-113">Messages</span></span>                    | <span data-ttu-id="e0462-114">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="e0462-114">Mail.Read</span></span>           |
| <span data-ttu-id="e0462-115">Unidad de disco (OneDrive del usuario)</span><span class="sxs-lookup"><span data-stu-id="e0462-115">Drive  (User's OneDrive)</span></span>    | <span data-ttu-id="e0462-116">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e0462-116">Files.ReadWrite</span></span>     |
| <span data-ttu-id="e0462-117">Unidades de disco (unidades de disco y contenido compartido de SharePoint)</span><span class="sxs-lookup"><span data-stu-id="e0462-117">Drives (Sharepoint shared content and drives)</span></span> | <span data-ttu-id="e0462-118">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e0462-118">Files.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="e0462-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e0462-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /subscriptions/{subscriptionId}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="e0462-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="e0462-120">Optional query parameters</span></span>
<span data-ttu-id="e0462-121">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e0462-121">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="e0462-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e0462-122">Request headers</span></span>
| <span data-ttu-id="e0462-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="e0462-123">Name</span></span>       | <span data-ttu-id="e0462-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="e0462-124">Type</span></span> | <span data-ttu-id="e0462-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="e0462-125">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="e0462-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="e0462-126">Authorization</span></span>  | <span data-ttu-id="e0462-127">string</span><span class="sxs-lookup"><span data-stu-id="e0462-127">string</span></span>  | <span data-ttu-id="e0462-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e0462-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="e0462-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e0462-130">Request body</span></span>
<span data-ttu-id="e0462-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e0462-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e0462-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e0462-132">Response</span></span>

<span data-ttu-id="e0462-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [subscription](../resources/subscription.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e0462-133">If successful, this method returns a `200 OK` response code and [subscription](../resources/subscription.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="e0462-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e0462-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e0462-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e0462-135">Request</span></span>
<span data-ttu-id="e0462-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e0462-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_subscription"
}-->
```http
GET https://graph.microsoft.com/v1.0/subscriptions/{subscriptionId}
```
##### <a name="response"></a><span data-ttu-id="e0462-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e0462-137">Response</span></span>
<span data-ttu-id="e0462-138">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e0462-138">Here is an example of the response.</span></span>
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
