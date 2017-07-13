<span data-ttu-id="bcfcf-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bcfcf-p103">Bearer {token}. Required.</span></span> | {token} de portador. Obligatorio. |


## <span data-ttu-id="bcfcf-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bcfcf-128">Request body</span></span>
<a id="request-body" class="xliff"></a>
<span data-ttu-id="bcfcf-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bcfcf-129">Do not supply a request body for this method.</span></span>

## <span data-ttu-id="bcfcf-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bcfcf-130">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="bcfcf-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [driveItem](../resources/driveitem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bcfcf-131">If successful, this method returns a `200 OK` response code and a [driveItem](../resources/driveitem.md) object in the response body.</span></span>

## <span data-ttu-id="bcfcf-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bcfcf-132">Example</span></span>
<a id="example" class="xliff"></a>

##### <span data-ttu-id="bcfcf-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bcfcf-133">Request</span></span>
<a id="request" class="xliff"></a>
<span data-ttu-id="bcfcf-134">Aquí tiene un ejemplo de la solicitud de las unidades del usuario.</span><span class="sxs-lookup"><span data-stu-id="bcfcf-134">Here is an example of the request for the user's drives.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_drive_special"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/special/{name}
```

##### <span data-ttu-id="bcfcf-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bcfcf-135">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="bcfcf-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bcfcf-136">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.driveItem"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "folder": { },
  "id": "s!lkjqwlkj124912049an",
  "name": "Photos",
  "specialFolder": { "name": "photos" },
  "webUrl": "https://contoso-my.sharepoint.com/personal/rgregg_contoso_com/Documents/Photos",
}
```

## <span data-ttu-id="bcfcf-137">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bcfcf-137">Remarks</span></span>
<a id="remarks" class="xliff"></a>

<span data-ttu-id="bcfcf-138">Para solicitar los elementos secundarios de una carpeta especial, puede solicitar la colección `children` o usar la opción [expand](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) para expandir la colección de elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="bcfcf-138">To request the children of a special folder, you can request the `children` collection or use the [expand](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) option to expand the children collection.</span></span>


<!-- {
  "type": "#page.annotation",
  "description": "List drives",
  "keywords": "",
  "section": "documentation",
  "tocPath": "OneDrive/Drive/Get special folder"
}-->
