<span data-ttu-id="d33a7-p102">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d33a7-p102">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.

## <span data-ttu-id="d33a7-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d33a7-119">Example</span></span>
<a id="example" class="xliff"></a>

##### <span data-ttu-id="d33a7-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d33a7-120">Request</span></span>
<a id="request" class="xliff"></a>

<span data-ttu-id="d33a7-121">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d33a7-121">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_directoryobject_from_directoryrole"
}-->

```http
DELETE https://graph.microsoft.com/v1.0/directoryroles/{id}/members/{id}/$ref
```

##### <span data-ttu-id="d33a7-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d33a7-122">Response</span></span>
<a id="response" class="xliff"></a>

<span data-ttu-id="d33a7-123">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d33a7-123">Here is an example of the response.</span></span> 
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
  "description": "Delete a member",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->