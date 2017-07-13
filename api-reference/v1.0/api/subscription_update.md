<span data-ttu-id="f8773-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f8773-p102">Bearer token. Required.</span></span>  | {token} de portador. Obligatorio. |

## <span data-ttu-id="f8773-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f8773-117">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="f8773-118">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [subscription](../resources/subscription.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f8773-118">If successful, this method returns a `200 OK` response code and [subscription](../resources/subscription.md) object in the response body.</span></span>
## <span data-ttu-id="f8773-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f8773-119">Example</span></span>
<a id="example" class="xliff"></a>
##### <span data-ttu-id="f8773-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f8773-120">Request</span></span>
<a id="request" class="xliff"></a>
<span data-ttu-id="f8773-121">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f8773-121">Here is an example of the request.</span></span>
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

##### <span data-ttu-id="f8773-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f8773-122">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="f8773-123">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f8773-123">Here is an example of the response.</span></span>
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
