<span data-ttu-id="714c5-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="714c5-p101">Bearer {token}. Required.</span></span>  | {token} de portador. Obligatorio. |


## <a name="request-body"></a><span data-ttu-id="714c5-118">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="714c5-118">Request body</span></span>
<span data-ttu-id="714c5-119">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="714c5-119">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="714c5-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="714c5-120">Response</span></span>

<span data-ttu-id="714c5-121">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [thumbnailSet](../resources/thumbnailset.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="714c5-121">If successful, this method returns a `200 OK` response code and [thumbnailSet](../resources/thumbnailset.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="714c5-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="714c5-122">Example</span></span>
##### <a name="request"></a><span data-ttu-id="714c5-123">Solicitud</span><span class="sxs-lookup"><span data-stu-id="714c5-123">Request</span></span>
<span data-ttu-id="714c5-124">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="714c5-124">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_thumbnailset"
}-->
```http
GET https://graph.microsoft.com/v1.0/drive/root/thumbnails/{id}
```
##### <a name="response"></a><span data-ttu-id="714c5-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="714c5-125">Response</span></span>
<span data-ttu-id="714c5-126">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="714c5-126">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.thumbnailSet"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 456

{
  "id": "id-value",
  "large": {
    "height": 99,
    "url": "url-value",
    "width": 99
  },
  "medium": {
    "height": 99,
    "url": "url-value",
    "width": 99
  },
  "small": {
    "height": 99,
    "url": "url-value",
    "width": 99
  },
  "source": {
    "height": 99,
    "url": "url-value",
    "width": 99
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get thumbnailSet",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
