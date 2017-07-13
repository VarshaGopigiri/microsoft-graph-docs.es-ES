<span data-ttu-id="fe57f-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `202, Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fe57f-p105">If successful, this method returns `202, Accepted` response code. It does not return anything in the response body.</span></span>
Si se ejecuta correctamente, este método devuelve el código de respuesta `202, Accepted`. No devuelve nada en el cuerpo de la respuesta.

## <span data-ttu-id="fe57f-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fe57f-135">Example</span></span>
<a id="example" class="xliff"></a>
<span data-ttu-id="fe57f-136">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="fe57f-136">Here is an example of how to call this API.</span></span>
##### <span data-ttu-id="fe57f-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fe57f-137">Request</span></span>
<a id="request" class="xliff"></a>
<span data-ttu-id="fe57f-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fe57f-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "event_tentativelyaccept"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/events/{id}/tentativelyAccept
Content-type: application/json
Content-length: 56

{
  "comment": "comment-value",
  "sendResponse": true
}
```

##### <span data-ttu-id="fe57f-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fe57f-139">Response</span></span>
<a id="response" class="xliff"></a>
##### <span data-ttu-id="fe57f-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fe57f-140">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="fe57f-141">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fe57f-141">Here is an example of the response.</span></span>
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
  "description": "event: tentativelyAccept",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
