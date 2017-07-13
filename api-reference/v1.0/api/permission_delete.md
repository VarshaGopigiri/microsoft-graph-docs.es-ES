<span data-ttu-id="98baa-p102">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="98baa-p102">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>
Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.

## <span data-ttu-id="98baa-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="98baa-123">Example</span></span>
<a id="example" class="xliff"></a>

##### <span data-ttu-id="98baa-124">Solicitud</span><span class="sxs-lookup"><span data-stu-id="98baa-124">Request</span></span>
<a id="request" class="xliff"></a>

<span data-ttu-id="98baa-125">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="98baa-125">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_permission"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/drive/root/items/{item-id}/permissions/{perm-id}
```

##### <span data-ttu-id="98baa-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="98baa-126">Response</span></span>
<a id="response" class="xliff"></a>

<span data-ttu-id="98baa-127">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="98baa-127">Here is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": false
} -->
```http
HTTP/1.1 204 No Content
```

## <span data-ttu-id="98baa-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="98baa-128">Remarks</span></span>
<a id="remarks" class="xliff"></a>

* <span data-ttu-id="98baa-129">Los [Drives](../resources/drive.md) con un **driveType** de `personal` (OneDrive Personal) no pueden crear ni modificar permisos en la DriveItem raíz.</span><span class="sxs-lookup"><span data-stu-id="98baa-129">[Drives](../resources/drive.md) with a **driveType** of `personal` (OneDrive Personal) cannot create or modify permissions on the root DriveItem.</span></span> 

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete permission",
  "keywords": "",
  "section": "documentation",
  "tocPath": "OneDrive/Item/Delete permission"
}-->
