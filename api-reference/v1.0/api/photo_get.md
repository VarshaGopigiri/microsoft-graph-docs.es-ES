<span data-ttu-id="e6ef1-p101">{token} de portador. Necesario.</span><span class="sxs-lookup"><span data-stu-id="e6ef1-p101">Bearer token. Required.</span></span>  | {token} de portador. Necesario. |

## <span data-ttu-id="e6ef1-117">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="e6ef1-117">Request body</span></span>
<a id="request-body" class="xliff"></a>
<span data-ttu-id="e6ef1-118">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e6ef1-118">Do not supply a request body for this method.</span></span>
## <span data-ttu-id="e6ef1-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6ef1-119">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="e6ef1-120">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [photo](../resources/photo.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e6ef1-120">If successful, this method returns a `200 OK` response code and [photo](../resources/photo.md) object in the response body.</span></span>
## <span data-ttu-id="e6ef1-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e6ef1-121">Example</span></span>
<a id="example" class="xliff"></a>
##### <span data-ttu-id="e6ef1-122">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e6ef1-122">Request</span></span>
<a id="request" class="xliff"></a>
<span data-ttu-id="e6ef1-123">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e6ef1-123">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_photo"
}-->
```http
GET https://graph.microsoft.com/v1.0/users/{id|userPrincipalName}/photo
```
##### <span data-ttu-id="e6ef1-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6ef1-124">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="e6ef1-125">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e6ef1-125">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.profilePhoto"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 53

{
  "height": 99,
  "width": 99,
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get photo",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
