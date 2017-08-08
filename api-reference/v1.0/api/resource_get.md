<span data-ttu-id="fe9a7-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fe9a7-p101">Bearer {token}. Required.</span></span>  | {token} de portador. Obligatorio. |

## <a name="request-body"></a><span data-ttu-id="fe9a7-115">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fe9a7-115">Request body</span></span>
<span data-ttu-id="fe9a7-116">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="fe9a7-116">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="fe9a7-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fe9a7-117">Response</span></span>
<span data-ttu-id="fe9a7-118">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y los datos binarios del archivo o la imagen en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fe9a7-118">If successful, this method returns a `200 OK` response code and the image or file binary data in the response body.</span></span>

<span data-ttu-id="fe9a7-119">Nota: Las imágenes no se procesan directamente en un explorador porque requieren autorización para recuperarlas, al igual que el resto del contenido de la página.</span><span class="sxs-lookup"><span data-stu-id="fe9a7-119">Note: Images won't render directly in a browser because they require authorization to retrieve them, like the rest of the page content.</span></span>
## <a name="example"></a><span data-ttu-id="fe9a7-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fe9a7-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="fe9a7-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fe9a7-121">Request</span></span>
<span data-ttu-id="fe9a7-122">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fe9a7-122">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_resource"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/resources/{id}/content
```
##### <a name="response"></a><span data-ttu-id="fe9a7-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fe9a7-123">Response</span></span>
<span data-ttu-id="fe9a7-124">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fe9a7-124">Here is an example of the response.</span></span>
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
