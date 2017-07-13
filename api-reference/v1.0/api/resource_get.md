<span data-ttu-id="6ffa9-p101">{token} de portador. Necesario.</span><span class="sxs-lookup"><span data-stu-id="6ffa9-p101">Bearer token. Required.</span></span>  | {token} de portador. Necesario. |

## <span data-ttu-id="6ffa9-115">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="6ffa9-115">Request body</span></span>
<a id="request-body" class="xliff"></a>
<span data-ttu-id="6ffa9-116">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6ffa9-116">Do not supply a request body for this method.</span></span>
## <span data-ttu-id="6ffa9-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ffa9-117">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="6ffa9-118">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y los datos binarios del archivo o la imagen en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6ffa9-118">If successful, this method returns a `200 OK` response code and the image or file binary data in the response body.</span></span>

<span data-ttu-id="6ffa9-119">Nota: Las imágenes no se procesan directamente en un explorador porque requieren autorización para recuperarlas, al igual que el resto del contenido de la página.</span><span class="sxs-lookup"><span data-stu-id="6ffa9-119">Note: Images won't render directly in a browser because they require authorization to retrieve them, like the rest of the page content.</span></span>
## <span data-ttu-id="6ffa9-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6ffa9-120">Example</span></span>
<a id="example" class="xliff"></a>
##### <span data-ttu-id="6ffa9-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6ffa9-121">Request</span></span>
<a id="request" class="xliff"></a>
<span data-ttu-id="6ffa9-122">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6ffa9-122">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_resource"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/resources/{id}/content
```
##### <span data-ttu-id="6ffa9-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ffa9-123">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="6ffa9-124">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6ffa9-124">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->
```http
HTTP/1.1 200 OK

...binary data...
```
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.onenoteResource"
} -->

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
