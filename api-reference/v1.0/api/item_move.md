<span data-ttu-id="4b787-p103">**Nota:** Al mover elementos a la raíz de un OneDrive, no puede usar la sintaxis `"id:" "root"`. Tendrá que usar el identificador real de la carpeta raíz o usar `{"path": "/drive/root"}` para la referencia primaria.</span><span class="sxs-lookup"><span data-stu-id="4b787-p103">**Note:** When moving items to the root of a OneDrive you cannot use the `"id:" "root"` syntax. You either need to use the real ID of the root folder, or use `{"path": "/drive/root"}` for the parent reference.</span></span>

**Nota:** Al mover elementos a la raíz de un OneDrive, no puede usar la sintaxis `"id:" "root"`. Tendrá que usar el identificador real de la carpeta raíz o usar `{"path": "/drive/root"}` para la referencia primaria.

## <span data-ttu-id="4b787-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4b787-125">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="4b787-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el recurso [DriveItem](../resources/driveitem.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4b787-126">If successful, this method returns a `200 OK` response code and updated [DriveItem](../resources/driveitem.md) resource in the response body.</span></span>

## <span data-ttu-id="4b787-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4b787-127">Example</span></span>
<a id="example" class="xliff"></a>
<span data-ttu-id="4b787-128">En este ejemplo, se mueve un elemento especificado mediante {item-id} a la carpeta **Documentos** del OneDrive del usuario.</span><span class="sxs-lookup"><span data-stu-id="4b787-128">This example moves an item specified by {item-id} into the **Documents** folder in the user's OneDrive.</span></span>

<!-- {
  "blockType": "request",
  "name": "update_item"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{item-id}
Content-type: application/json

{
    "name": "new-item-name",
    "parentReference" : {"path": "/drive/root:/Documents"}
}
```

## <span data-ttu-id="4b787-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4b787-129">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="4b787-130">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4b787-130">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.driveItem"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "id": "0123456789abc",
    "name": "new-item-name",
    "folder": { "childCount": 3 },
  "parentReference": {
    "id": "507DE6D5-0201-496A-AA87-5E2563247982",
    "path": "/drive/root:/Documents"
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Move item",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
