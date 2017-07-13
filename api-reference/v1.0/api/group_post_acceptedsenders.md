<span data-ttu-id="fc4cb-p102">{token} de portador. Necesario.</span><span class="sxs-lookup"><span data-stu-id="fc4cb-p102">Bearer token. Required.</span></span>  | {token} de portador. Necesario.  |

## <span data-ttu-id="fc4cb-115">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fc4cb-115">Request body</span></span>
<a id="request-body" class="xliff"></a>
<span data-ttu-id="fc4cb-116">En el cuerpo de la solicitud, proporcione el identificador de un objeto de usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="fc4cb-116">In the request body, supply the id of a user or group object.</span></span>


## <span data-ttu-id="fc4cb-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fc4cb-117">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="fc4cb-118">Este método devuelve el código de respuesta `204, No Content` y ningún cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fc4cb-118">This method returns `204, No Content` response code and no response body.</span></span>

## <span data-ttu-id="fc4cb-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fc4cb-119">Example</span></span>
<a id="example" class="xliff"></a>
##### <span data-ttu-id="fc4cb-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fc4cb-120">Request</span></span>
<a id="request" class="xliff"></a>
<span data-ttu-id="fc4cb-121">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fc4cb-121">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_group"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/acceptedSenders/$ref
Content-type: application/json
Content-length: 30

{
  "@odata.id":"https://graph.microsoft.com/v1.0/users/alexd@contoso.com"
}
```
##### <span data-ttu-id="fc4cb-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fc4cb-122">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="fc4cb-123">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fc4cb-123">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create acceptedSender",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
