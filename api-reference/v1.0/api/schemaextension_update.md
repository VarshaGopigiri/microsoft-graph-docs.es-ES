<span data-ttu-id="2e530-p107">Conjunto de tipos de Microsoft Graph (compatibles con extensiones) a los que se puede aplicar la extensión de esquema.  Solo se admiten cambios para agregar elementos.</span><span class="sxs-lookup"><span data-stu-id="2e530-p107">Set of Microsoft Graph types (that can support extensions) that the schema extension can be applied to.  Only additive changes are permitted.</span></span>|Conjunto de tipos de Microsoft Graph (compatibles con extensiones) a los que se puede aplicar la extensión de esquema.  Solo se admiten cambios para agregar elementos.|

## <span data-ttu-id="2e530-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2e530-142">Response</span></span>
<a id="response" class="xliff"></a>

<span data-ttu-id="2e530-143">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="2e530-143">If successful, this method returns a `204 No Content` response code.</span></span>

## <span data-ttu-id="2e530-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2e530-144">Example</span></span>
<a id="example" class="xliff"></a>

##### <span data-ttu-id="2e530-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2e530-145">Request</span></span>
<a id="request" class="xliff"></a>

<span data-ttu-id="2e530-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2e530-146">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_schemaextension"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/schemaExtensions/{id}
Content-type: application/json
Content-length: 201

{
  "properties": [
    {
      "name":"new-name-value",
      "type":"new-type-value"
    },
    {
      "name":"additional-name-value",
      "type":"additional-type-value"
    }
  ],
}
```

##### <span data-ttu-id="2e530-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2e530-147">Response</span></span>
<a id="response" class="xliff"></a>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.schemaExtension"
} -->
```http
HTTP/1.1 204 No Content
```

## <span data-ttu-id="2e530-148">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="2e530-148">See also</span></span>
<a id="see-also" class="xliff"></a>

- [<span data-ttu-id="2e530-149">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="2e530-149">Add custom data to resources using extensions</span></span>](../../../concepts/extensibility_overview.md)
- [<span data-ttu-id="2e530-150">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="2e530-150">Add custom data to groups using schema extensions</span></span>](../../../concepts/extensibility_schema_groups.md)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update schemaextension",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->