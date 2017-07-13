<span data-ttu-id="428ed-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="428ed-p103">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>
Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.

## <span data-ttu-id="428ed-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="428ed-129">Example</span></span>
<a id="example" class="xliff"></a>
<span data-ttu-id="428ed-130">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="428ed-130">Here is an example of how to call this API.</span></span>
##### <span data-ttu-id="428ed-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="428ed-131">Request</span></span>
<a id="request" class="xliff"></a>
<span data-ttu-id="428ed-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="428ed-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "event_snoozereminder"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/events/{id}/snoozeReminder
Content-type: application/json
Content-length: 97

{
  "newReminderTime": {
    "dateTime": "dateTime-value",
    "timeZone": "timeZone-value"
  }
}
```

##### <span data-ttu-id="428ed-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="428ed-133">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="428ed-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="428ed-134">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "event: snoozeReminder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
