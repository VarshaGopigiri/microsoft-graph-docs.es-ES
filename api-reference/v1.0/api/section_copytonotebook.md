<span data-ttu-id="45c88-p105">Si se ejecuta correctamente, este método devuelve un código de respuesta `202 Accepted` y un encabezado `Operation-Location`. Sondee el extremo de Operation-Location para [obtener el estado de la operación de copia](onenoteoperation_get.md).</span><span class="sxs-lookup"><span data-stu-id="45c88-p105">If successful, this method returns a `202 Accepted` response code and an `Operation-Location` header. Poll the Operation-Location endpoint to [get the status of the copy operation](onenoteoperation_get.md).</span></span>
Si se ejecuta correctamente, este método devuelve un código de respuesta `202 Accepted` y un encabezado `Operation-Location`. Sondee el extremo de Operation-Location para [obtener el estado de la operación de copia](onenoteoperation_get.md).

## <span data-ttu-id="45c88-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="45c88-138">Example</span></span>
<a id="example" class="xliff"></a>
<span data-ttu-id="45c88-139">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="45c88-139">Here is an example of how to call this API.</span></span>
##### <span data-ttu-id="45c88-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="45c88-140">Request</span></span>
<a id="request" class="xliff"></a>
<span data-ttu-id="45c88-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="45c88-141">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "section_copytonotebook"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/onenote/sections/{id}/copyToNotebook
Content-type: application/json
Content-length: 84

{
  "id": "id-value",
  "groupId": "groupId-value",
  "renameAs": "renameAs-value"
}
```

##### <span data-ttu-id="45c88-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="45c88-142">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="45c88-143">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="45c88-143">Here is an example of the response.</span></span>
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
  "description": "section: copyToNotebook",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->