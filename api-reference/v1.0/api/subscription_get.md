<span data-ttu-id="7b207-p101">{token} de portador. Necesario.</span><span class="sxs-lookup"><span data-stu-id="7b207-p101">Bearer token. Required.</span></span>  | {token} de portador. Necesario. |

## <span data-ttu-id="7b207-116">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="7b207-116">Request body</span></span>
<a id="request-body" class="xliff"></a>
<span data-ttu-id="7b207-117">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7b207-117">Do not supply a request body for this method.</span></span>
## <span data-ttu-id="7b207-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7b207-118">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="7b207-119">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [subscription](../resources/subscription.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7b207-119">If successful, this method returns a `200 OK` response code and [subscription](../resources/subscription.md) object in the response body.</span></span>
## <span data-ttu-id="7b207-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7b207-120">Example</span></span>
<a id="example" class="xliff"></a>
##### <span data-ttu-id="7b207-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7b207-121">Request</span></span>
<a id="request" class="xliff"></a>
<span data-ttu-id="7b207-122">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7b207-122">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_subscription"
}-->
```http
GET https://graph.microsoft.com/v1.0/subscriptions/{subscriptionId}
```
##### <span data-ttu-id="7b207-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7b207-123">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="7b207-124">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7b207-124">Here is an example of the response.</span></span>
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
