<span data-ttu-id="765fe-p120">Los errores se devuelven con un código de error HTTP y un objeto de error. Los errores `code` y `message` explican el motivo del error.</span><span class="sxs-lookup"><span data-stu-id="765fe-p120">Errors are returned with an HTTP error code and an error object. An error `code` and `message` explain the reason for the error.</span></span> 

Los errores se devuelven con un código de error HTTP y un objeto de error. Los errores `code` y `message` explican el motivo del error.
 
<span data-ttu-id="765fe-277">A continuación puede ver un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="765fe-277">The following is an example.</span></span>

<!-- { "blockType": "ignored" } -->
```http
HTTP/1.1 400 Bad Request
Content-Type: application/json

{
  "error": {
    "code": "ItemAlreadyExists",
    "message": "A resource with the same name or identifier already exists.",
    "innerError": {
      "request-id": "214ca7ea-9ea4-442e-9c67-71fdda0a559c",
      "date": "2016-07-28T03:56:09"
    }
  }
}
```

