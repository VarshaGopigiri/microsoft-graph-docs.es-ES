<span data-ttu-id="f0473-p107">La colección de propiedades extendidas de valor único definidas para el objeto mailFolder. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="f0473-p107">The collection of single-value extended properties defined for the mailFolder. Read-only. Nullable.</span></span>| La colección de propiedades extendidas de valor único definidas para el objeto mailFolder. Solo lectura. Admite valores NULL.|


## <span data-ttu-id="f0473-200">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f0473-200">JSON representation</span></span>
<a id="json-representation" class="xliff"></a>

<span data-ttu-id="f0473-201">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="f0473-201">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "childFolders",
    "messages",
    "multiValueExtendedProperties",
    "singleValueExtendedProperties"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mailFolder"
}-->

```json
{
  "childFolderCount": 1024,
  "displayName": "string",
  "id": "string (identifier)",
  "parentFolderId": "string",
  "totalItemCount": 1024,
  "unreadItemCount": 1024,

  "childFolders": [ { "@odata.type": "microsoft.graph.mailFolder" } ],
  "messages": [ { "@odata.type": "microsoft.graph.message" } ],
  "multiValueExtendedProperties": [ { "@odata.type": "microsoft.graph.multiValueLegacyExtendedProperty" }],
  "singleValueExtendedProperties": [ { "@odata.type": "microsoft.graph.singleValueLegacyExtendedProperty" }]
}

```

## <span data-ttu-id="f0473-202">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f0473-202">See also</span></span>
<a id="see-also" class="xliff"></a>

- [<span data-ttu-id="f0473-203">Usar la consulta delta para realizar el seguimiento de los cambios en datos de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="f0473-203">Use delta query to track changes in Microsoft Graph data</span></span>](../../../concepts/delta_query_overview.md)
- [<span data-ttu-id="f0473-204">Obtener los cambios incrementales en los mensajes de una carpeta</span><span class="sxs-lookup"><span data-stu-id="f0473-204">Get incremental changes to messages in a folder</span></span>](../../../concepts/delta_query_messages.md)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mailFolder resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
