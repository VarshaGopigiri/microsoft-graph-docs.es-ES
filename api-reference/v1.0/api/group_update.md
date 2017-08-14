<span data-ttu-id="67e21-p110">Solo un subconjunto de la API de grupo relativa a la administración de grupos básicos admite permisos delegados y de aplicación. Todos los demás miembros de la API de grupo, incluida la actualización **autoSubscribeNewMembers**, son compatible solo con los permisos delegados. Vea [problemas conocidos](https://developer.microsoft.com/en-us/graph/docs/overview/release_notes#group-permission-scopes) para obtener ejemplos.</span><span class="sxs-lookup"><span data-stu-id="67e21-p110">Only a subset of the group API pertaining to core group administration and management support application and delegated permissions. All other members of the group API, including updating  **autoSubscribeNewMembers**, support only delegated permissions. See [known issues](https://developer.microsoft.com/en-us/graph/docs/overview/release_notes#group-permission-scopes) for examples.</span></span>
- Solo un subconjunto de la API de grupo relativa a la administración de grupos básicos admite permisos delegados y de aplicación. Todos los demás miembros de la API de grupo, incluida la actualización **autoSubscribeNewMembers**, son compatible solo con los permisos delegados. Vea [problemas conocidos](https://developer.microsoft.com/en-us/graph/docs/overview/release_notes#group-permission-scopes) para obtener ejemplos.

## <a name="response"></a><span data-ttu-id="67e21-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="67e21-162">Response</span></span>

<span data-ttu-id="67e21-163">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="67e21-163">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="67e21-164">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="67e21-164">Example</span></span>

##### <a name="request"></a><span data-ttu-id="67e21-165">Solicitud</span><span class="sxs-lookup"><span data-stu-id="67e21-165">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "update_group"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/groups/{id}
Content-type: application/json
Content-length: 211

{
  "description": "description-value",
  "displayName": "displayName-value",
  "groupTypes": [
    "groupTypes-value"
  ],
  "mail": "mail-value",
  "mailEnabled": true,
  "mailNickname": "mailNickname-value"
}
```

##### <a name="response"></a><span data-ttu-id="67e21-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="67e21-166">Response</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.group"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update group",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->