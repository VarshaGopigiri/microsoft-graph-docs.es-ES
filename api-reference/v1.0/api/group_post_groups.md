<span data-ttu-id="ea31b-p107">Aquí tiene un ejemplo de la respuesta. Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Se devolverán más propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ea31b-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. More properties will be returned from an actual call.</span></span>
Aquí tiene un ejemplo de la respuesta. Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Se devolverán más propiedades de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.group"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 244

{
  "description": "Self help community for library",
  "displayName": "Library Assist",
  "groupTypes": [
    "Unified"
  ],
  "mail": "library@contoso.onmicrosoft.com",
  "mailEnabled": true,
  "mailNickname": "library",
  "securityEnabled": false
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create group",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
