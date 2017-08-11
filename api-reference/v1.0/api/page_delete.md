<span data-ttu-id="10b95-p102">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="10b95-p102">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>
Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.

## <a name="example"></a><span data-ttu-id="10b95-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="10b95-118">Example</span></span>
##### <a name="request"></a><span data-ttu-id="10b95-119">Solicitud</span><span class="sxs-lookup"><span data-stu-id="10b95-119">Request</span></span>
<span data-ttu-id="10b95-120">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="10b95-120">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_page"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/onenote/pages/{id}
```
##### <a name="response"></a><span data-ttu-id="10b95-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="10b95-121">Response</span></span>
<span data-ttu-id="10b95-122">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="10b95-122">Here is an example of the response.</span></span>
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
  "description": "Delete page",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->