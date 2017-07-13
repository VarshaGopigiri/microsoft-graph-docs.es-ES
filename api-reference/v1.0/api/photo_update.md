<span data-ttu-id="ea527-p102">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="ea527-p102">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>
En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.

| <span data-ttu-id="ea527-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ea527-118">Property</span></span>     | <span data-ttu-id="ea527-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="ea527-119">Type</span></span>   |<span data-ttu-id="ea527-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea527-120">Description</span></span>|
|:---------------|:--------|:----------|

## <span data-ttu-id="ea527-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea527-121">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="ea527-122">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [photo](../resources/photo.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ea527-122">If successful, this method returns a `200 OK` response code and updated [photo](../resources/photo.md) object in the response body.</span></span>
## <span data-ttu-id="ea527-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ea527-123">Example</span></span>
<a id="example" class="xliff"></a>
##### <span data-ttu-id="ea527-124">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ea527-124">Request</span></span>
<a id="request" class="xliff"></a>
<span data-ttu-id="ea527-125">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ea527-125">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_photo"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/users/{id|userPrincipalName}/photo
Content-type: application/json
Content-length: 53

{
  "height": 99,
  "width": 99,
  "id": "id-value"
}
```
##### <span data-ttu-id="ea527-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea527-126">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="ea527-127">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ea527-127">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.profilePhoto"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 53

{
  "height": 99,
  "width": 99,
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update photo",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
