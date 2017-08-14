<span data-ttu-id="4eb54-p102">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4eb54-p102">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.

## <a name="example"></a><span data-ttu-id="4eb54-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4eb54-117">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4eb54-118">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4eb54-118">Request</span></span>
<span data-ttu-id="4eb54-119">Aquí tiene un par de ejemplos de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4eb54-119">Here are a couple of examples of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_group"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/groups/{id}/acceptedSenders/$ref?$id="users/{id}"

DELETE https://graph.microsoft.com/v1.0/groups/{id}/acceptedSenders/$ref?$id="groups/{id}"
```

##### <a name="response"></a><span data-ttu-id="4eb54-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4eb54-120">Response</span></span>
<span data-ttu-id="4eb54-121">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4eb54-121">Here is an example of the response.</span></span> 
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