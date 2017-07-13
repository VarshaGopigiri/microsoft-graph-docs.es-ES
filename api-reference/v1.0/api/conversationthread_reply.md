<span data-ttu-id="9d97c-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `202, Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9d97c-p104">If successful, this method returns `202, Accepted` response code. It does not return anything in the response body.</span></span>
Si se ejecuta correctamente, este método devuelve el código de respuesta `202, Accepted`. No devuelve nada en el cuerpo de la respuesta.

## <span data-ttu-id="9d97c-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9d97c-127">Example</span></span>
<a id="example" class="xliff"></a>
<span data-ttu-id="9d97c-128">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="9d97c-128">Here is an example of how to call this API.</span></span>
##### <span data-ttu-id="9d97c-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9d97c-129">Request</span></span>
<a id="request" class="xliff"></a>
<span data-ttu-id="9d97c-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9d97c-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "conversationthread_reply"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/threads/{id}/reply
Content-type: application/json
Content-length: 1131

{
  "post": {
    "body": {
      "contentType": "",
      "content": "content-value"
    }
  }
}
```

##### <span data-ttu-id="9d97c-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9d97c-131">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="9d97c-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9d97c-132">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 202 Accepted
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "conversationThread: reply",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
