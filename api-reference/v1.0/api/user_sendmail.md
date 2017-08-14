<span data-ttu-id="433e5-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `202, Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="433e5-p105">If successful, this method returns `202, Accepted` response code. It does not return anything in the response body.</span></span>

Si se ejecuta correctamente, este método devuelve el código de respuesta `202, Accepted`. No devuelve nada en el cuerpo de la respuesta.

## <a name="example"></a><span data-ttu-id="433e5-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="433e5-133">Example</span></span>
<span data-ttu-id="433e5-134">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="433e5-134">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="433e5-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="433e5-135">Request</span></span>
<span data-ttu-id="433e5-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="433e5-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "user_sendmail"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/sendMail
Content-type: application/json
Content-length: 512

{
  "message": {
    "subject": "Meet for lunch?",
    "body": {
      "contentType": "Text",
      "content": "The new cafeteria is open."
    },
    "toRecipients": [
      {
        "emailAddress": {
          "address": "fannyd@contoso.onmicrosoft.com"
        }
      }
    ],
    "ccRecipients": [
      {
        "emailAddress": {
          "address": "danas@contoso.onmicrosoft.com"
        }
      }
    ]
  },
  "saveToSentItems": "false"
}
```

##### <a name="response"></a><span data-ttu-id="433e5-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="433e5-137">Response</span></span>
<span data-ttu-id="433e5-138">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="433e5-138">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 202 Accepted
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user: sendMail",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
