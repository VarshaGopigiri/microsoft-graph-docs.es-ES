<span data-ttu-id="48300-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `202, Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="48300-p105">If successful, this method returns `202, Accepted` response code. It does not return anything in the response body.</span></span>
Si se ejecuta correctamente, este método devuelve el código de respuesta `202, Accepted`. No devuelve nada en el cuerpo de la respuesta.

## <span data-ttu-id="48300-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="48300-134">Example</span></span>
<a id="example" class="xliff"></a>
<span data-ttu-id="48300-135">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="48300-135">Here is an example of how to call this API.</span></span>
##### <span data-ttu-id="48300-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="48300-136">Request</span></span>
<a id="request" class="xliff"></a>
<span data-ttu-id="48300-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="48300-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "message_forward"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/messages/{id}/forward
Content-type: application/json
Content-length: 166

{
  "comment": "comment-value",
  "toRecipients": [
    {
      "emailAddress": {
        "name": "name-value",
        "address": "address-value"
      }
    }
  ]
}
```

##### <span data-ttu-id="48300-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="48300-138">Response</span></span>
<a id="response" class="xliff"></a>
##### <span data-ttu-id="48300-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="48300-139">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="48300-140">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="48300-140">Here is an example of the response.</span></span>
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
  "description": "message: forward",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
