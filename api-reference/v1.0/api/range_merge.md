<span data-ttu-id="a032e-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a032e-p103">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>
Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.

## <span data-ttu-id="a032e-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a032e-126">Example</span></span>
<a id="example" class="xliff"></a>
<span data-ttu-id="a032e-127">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="a032e-127">Here is an example of how to call this API.</span></span>
##### <span data-ttu-id="a032e-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a032e-128">Request</span></span>
<a id="request" class="xliff"></a>
<span data-ttu-id="a032e-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a032e-129">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_merge"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/merge
Content-type: application/json
Content-length: 20

{
  "across": true
}
```

##### <span data-ttu-id="a032e-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a032e-130">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="a032e-131">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a032e-131">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.none"
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Range: merge",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->