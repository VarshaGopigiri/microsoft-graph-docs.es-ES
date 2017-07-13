<span data-ttu-id="ca45f-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `202, Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ca45f-p105">If successful, this method returns `202, Accepted` response code. It does not return anything in the response body.</span></span>
Si se ejecuta correctamente, este método devuelve el código de respuesta `202, Accepted`. No devuelve nada en el cuerpo de la respuesta.

## <span data-ttu-id="ca45f-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ca45f-131">Example</span></span>
<a id="example" class="xliff"></a>
<span data-ttu-id="ca45f-132">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="ca45f-132">Here is an example of how to call this API.</span></span>
##### <span data-ttu-id="ca45f-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ca45f-133">Request</span></span>
<a id="request" class="xliff"></a>
<span data-ttu-id="ca45f-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ca45f-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "message_replyall"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/messages/{id}/replyAll
Content-type: application/json
Content-length: 32

{
  "comment": "comment-value"
}
```


##### <span data-ttu-id="ca45f-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ca45f-135">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="ca45f-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ca45f-136">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "message: replyAll",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
