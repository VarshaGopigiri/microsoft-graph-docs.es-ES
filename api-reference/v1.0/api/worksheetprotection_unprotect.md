<span data-ttu-id="187e3-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="187e3-p103">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.

## <a name="example"></a><span data-ttu-id="187e3-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="187e3-125">Example</span></span>
<span data-ttu-id="187e3-126">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="187e3-126">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="187e3-127">Solicitud</span><span class="sxs-lookup"><span data-stu-id="187e3-127">Request</span></span>
<span data-ttu-id="187e3-128">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="187e3-128">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "worksheetprotection_unprotect"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/protection/unprotect
Content-type: application/json
Content-length: 34

{
  "password": "password-value"
}
```

##### <a name="response"></a><span data-ttu-id="187e3-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="187e3-129">Response</span></span>
<span data-ttu-id="187e3-130">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="187e3-130">Here is an example of the response.</span></span> 
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
  "description": "WorksheetProtection: unprotect",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->