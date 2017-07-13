<span data-ttu-id="2d209-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2d209-p103">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>
Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.

## <span data-ttu-id="2d209-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2d209-130">Example</span></span>
<a id="example" class="xliff"></a>
##### <span data-ttu-id="2d209-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2d209-131">Request</span></span>
<a id="request" class="xliff"></a>
<span data-ttu-id="2d209-132">Este es un ejemplo de la solicitud para eliminar un archivo adjunto en un evento.</span><span class="sxs-lookup"><span data-stu-id="2d209-132">Here is an example of the request to delete an attachment on an event.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_attachment"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/events/{id}/attachments/{id}
```
##### <span data-ttu-id="2d209-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2d209-133">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="2d209-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2d209-134">Here is an example of the response.</span></span>
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
  "description": "Delete attachment",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
