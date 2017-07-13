<span data-ttu-id="2da8f-p106">Si se ejecuta correctamente, este método devuelve un código de respuesta `202 Accepted` y un encabezado `Operation-Location`. Sondee el extremo de Operation-Location para [obtener el estado de la operación de copia](onenoteOperation_get.md).</span><span class="sxs-lookup"><span data-stu-id="2da8f-p106">If successful, this method returns a `202 Accepted` response code and an `Operation-Location` header. Poll the Operation-Location endpoint to [get the status of the copy operation](onenoteOperation_get.md).</span></span>
Si se ejecuta correctamente, este método devuelve un código de respuesta `202 Accepted` y un encabezado `Operation-Location`. Sondee el extremo de Operation-Location para [obtener el estado de la operación de copia](onenoteOperation_get.md).

## <span data-ttu-id="2da8f-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2da8f-136">Example</span></span>
<a id="example" class="xliff"></a>
<span data-ttu-id="2da8f-137">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="2da8f-137">Here is an example of how to call this API.</span></span>
##### <span data-ttu-id="2da8f-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2da8f-138">Request</span></span>
<a id="request" class="xliff"></a>
<span data-ttu-id="2da8f-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2da8f-139">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "notebook_copynotebook"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/onenote/notebooks/{id}/copyNotebook
Content-type: application/json
Content-length: 108

{
  "groupId": "groupId-value",
  "renameAs": "renameAs-value"
}
```

##### <span data-ttu-id="2da8f-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2da8f-140">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="2da8f-141">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2da8f-141">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.onenoteOperation"
} -->
```http
HTTP/1.1 202 Accepted
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "notebook: copyNotebook",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
