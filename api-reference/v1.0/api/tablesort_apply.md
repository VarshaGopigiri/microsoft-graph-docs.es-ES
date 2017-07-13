<span data-ttu-id="993cc-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="993cc-p104">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>
Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.

## <span data-ttu-id="993cc-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="993cc-133">Example</span></span>
<a id="example" class="xliff"></a>
<span data-ttu-id="993cc-134">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="993cc-134">Here is an example of how to call this API.</span></span>
##### <span data-ttu-id="993cc-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="993cc-135">Request</span></span>
<a id="request" class="xliff"></a>
<span data-ttu-id="993cc-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="993cc-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "tablesort_apply"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/sort/apply
Content-type: application/json
Content-length: 298

{
  "fields": [
    {
      "key": 99,
      "sortOn": "sortOn-value",
      "ascending": true,
      "color": "color-value",
      "dataOption": "dataOption-value",
      "icon": {
        "set": "set-value",
        "index": 99
      }
    }
  ],
  "matchCase": true,
  "method": "method-value"
}
```

##### <span data-ttu-id="993cc-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="993cc-137">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="993cc-138">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="993cc-138">Here is an example of the response.</span></span> 
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
  "description": "TableSort: apply",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->