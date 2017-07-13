<span data-ttu-id="48340-p103">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="48340-p103">Nature of the data in the body of an entity. Required.</span></span>  | Naturaleza de los datos en el cuerpo de una entidad. Obligatorio. |

## <span data-ttu-id="48340-122">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="48340-122">Request body</span></span>
<a id="request-body" class="xliff"></a>
<span data-ttu-id="48340-123">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="48340-123">In the request body, supply a JSON representation of [attachment](../resources/attachment.md) object.</span></span>


## <span data-ttu-id="48340-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="48340-124">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="48340-125">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="48340-125">If successful, this method returns `201, Created` response code and [attachment](../resources/attachment.md) object in the response body.</span></span>

## <span data-ttu-id="48340-126">Ejemplo (datos adjuntos del archivo)</span><span class="sxs-lookup"><span data-stu-id="48340-126">Example (file attachment)</span></span>
<a id="example-file-attachment" class="xliff"></a>

##### <span data-ttu-id="48340-127">Solicitud</span><span class="sxs-lookup"><span data-stu-id="48340-127">Request</span></span>
<a id="request" class="xliff"></a>
<span data-ttu-id="48340-128">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="48340-128">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_file_attachment_from_event"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/events('AAMkAGI1AAAt9AHjAAA=')/attachments 
Content-type: application/json
Content-length: 151

{
    "@odata.type": "#microsoft.graph.fileAttachment",
    "name": "menu.txt",
    "contentBytes": "bWFjIGFuZCBjaGVlc2UgdG9kYXk="   
}
```

<span data-ttu-id="48340-129">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="48340-129">In the request body, supply a JSON representation of [attachment](../resources/attachment.md) object.</span></span>

##### <span data-ttu-id="48340-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="48340-130">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="48340-131">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="48340-131">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.attachment"
} -->
```http
HTTP 201 Created
Content-Length: 735

{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('cd209b0b-3f83-4c35-82d2-d88a61820480')/events('AAMkAGI1AAAt9AHjAAA%3D')/attachments/$entity",
    "@odata.type":"#microsoft.graph.fileAttachment",
    "id":"AAMkAGI1AAAt9AHjAAABEgAQAEdBogju-MJEu6Ngg-1_W0g=",
    "lastModifiedDateTime":"2017-04-15T03:21:49Z",
    "name":"menu.txt",
    "contentType":"text/plain",
    "size":178,
    "isInline":false,
    "contentId":null,
    "contentLocation":null,
    "contentBytes":"bWFjIGFuZCBjaGVlc2UgdG9kYXk="
}
```

## <span data-ttu-id="48340-132">Ejemplo (datos adjuntos del elemento)</span><span class="sxs-lookup"><span data-stu-id="48340-132">Example (item attachment)</span></span>
<a id="example-item-attachment" class="xliff"></a>

##### <span data-ttu-id="48340-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="48340-133">Request</span></span>
<a id="request" class="xliff"></a>

<span data-ttu-id="48340-134">Este es un ejemplo que adjunta un evento con otro evento como datos adjuntos del elemento.</span><span class="sxs-lookup"><span data-stu-id="48340-134">Here is an example which attaches an event with another event as an item attachment.</span></span>

<!-- {
  "blockType": "request",
  "name": "create_item_attachment_from_event"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/events/{AAMkAGI1AAAt9AHjAAA=}/attachments
Content-type: application/json
Content-length: 600

{
  "@odata.type": "#microsoft.graph.itemAttachment",
  "name": "Holiday event", 
  "item": {
        "@odata.type": "microsoft.graph.event",
        "subject": "Discuss gifts for children",
        "body": {
            "contentType": "HTML",
            "content": "Let's look for funding!"
         },
         "start": {
             "dateTime": "2016-12-02T18:00:00",
             "timeZone": "Pacific Standard Time"
          },
          "end": {
             "dateTime": "2016-12-02T19:00:00",
             "timeZone": "Pacific Standard Time"
          }
    }
}
```

##### <span data-ttu-id="48340-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="48340-135">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="48340-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="48340-136">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.attachment"
} -->
```http
HTTP 201 Created
Content-type: application/json
Content-length: 162

{
    "@odata.context":"https://graph.microsoft.com/api/v1.0/$metadata#me/events('AAMkAGI1AAAt9AHjAAA=')/attachments/$entity",
    "@odata.type":"#microsoft.graph.itemAttachment",
    "@odata.id":"https://graph.microsoft.com/api/v1.0/users('fdcbcf34-2505-4d07-be5b-0a55b699d157@41a5b830-45ac-4f1b-9bfc-baafa3b7db2e')/events('AAMkAGI1AAAt9AHjAAA=')/attachments('AAMkADNkN2Jp5JVnQIe9r0=')",
    "id":"AAMkADNkNJp5JVnQIe9r0=",
    "lastModifiedDateTime":"2016-12-01T22:27:13Z",
    "name":"Holiday event",
    "contentType":null,
    "size":2473,
    "isInline":false
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Attachment",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
