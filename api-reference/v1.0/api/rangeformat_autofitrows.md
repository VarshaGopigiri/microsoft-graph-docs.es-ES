<span data-ttu-id="b33be-p102">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b33be-p102">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.

## <a name="example"></a><span data-ttu-id="b33be-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b33be-117">Example</span></span>
<span data-ttu-id="b33be-118">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="b33be-118">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="b33be-119">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b33be-119">Request</span></span>
<span data-ttu-id="b33be-120">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b33be-120">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "rangeformat_autofitrows"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/format/autofitRows
```

##### <a name="response"></a><span data-ttu-id="b33be-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b33be-121">Response</span></span>
<span data-ttu-id="b33be-122">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b33be-122">Here is an example of the response.</span></span> 
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
  "description": "RangeFormat: autofitRows",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->