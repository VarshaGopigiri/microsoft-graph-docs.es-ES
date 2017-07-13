<span data-ttu-id="00c5d-p101">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="00c5d-p101">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>
En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.

| <span data-ttu-id="00c5d-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="00c5d-120">Property</span></span>     | <span data-ttu-id="00c5d-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="00c5d-121">Type</span></span>   | <span data-ttu-id="00c5d-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="00c5d-122">Description</span></span>                   |
|:-------------|:-------|:------------------------------|
| <span data-ttu-id="00c5d-123">**roles**</span><span class="sxs-lookup"><span data-stu-id="00c5d-123">**roles**</span></span>    | <span data-ttu-id="00c5d-124">String</span><span class="sxs-lookup"><span data-stu-id="00c5d-124">String</span></span> | <span data-ttu-id="00c5d-125">Matriz de tipos de permisos.</span><span class="sxs-lookup"><span data-stu-id="00c5d-125">An array of permission types.</span></span> |


## <span data-ttu-id="00c5d-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="00c5d-126">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="00c5d-127">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [permission](../resources/permission.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="00c5d-127">If successful, this method returns a `200 OK` response code and updated [permission](../resources/permission.md) object in the response body.</span></span>

## <span data-ttu-id="00c5d-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="00c5d-128">Example</span></span>
<a id="example" class="xliff"></a>

##### <span data-ttu-id="00c5d-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="00c5d-129">Request</span></span>
<a id="request" class="xliff"></a>

<span data-ttu-id="00c5d-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="00c5d-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_permission"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{item-id}/permissions/{perm-id}
Content-type: application/json

{
  "roles": [ "read" ]
}
```
##### <span data-ttu-id="00c5d-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="00c5d-131">Response</span></span>
<a id="response" class="xliff"></a>

<span data-ttu-id="00c5d-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="00c5d-132">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.permission"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "grantedTo": {
    "user": {
      "displayName": "Ryan Gregg",
      "id": "efee1b77-fb3b-4f65-99d6-274c11914d12"
    }
  },
  "id": "1",
  "roles": [ "read" ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update permission",
  "keywords": "",
  "section": "documentation",
  "tocPath": "OneDrive/Item/Update permission"
}-->
