<span data-ttu-id="5a0aa-p122">La colección de propiedades extendidas de valor único definidas para el mensaje. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="5a0aa-p122">The collection of single-value extended properties defined for the message. Read-only. Nullable.</span></span>| La colección de propiedades extendidas de valor único definidas para el mensaje. Solo lectura. Admite valores NULL.|


## <span data-ttu-id="5a0aa-330">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5a0aa-330">JSON representation</span></span>
<a id="json-representation" class="xliff"></a>

<span data-ttu-id="5a0aa-331">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="5a0aa-331">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "attachments",
    "extensions",
    "singleValueExtendedProperties",
    "multiValueExtendedProperties"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.message"
}-->

```json
{
  "bccRecipients": [{"@odata.type": "microsoft.graph.recipient"}],
  "body": {"@odata.type": "microsoft.graph.itemBody"},
  "bodyPreview": "string",
  "categories": ["string"],
  "ccRecipients": [{"@odata.type": "microsoft.graph.recipient"}],
  "changeKey": "string",
  "conversationId": "string",
  "createdDateTime": "String (timestamp)",
  "from": {"@odata.type": "microsoft.graph.recipient"},
  "hasAttachments": true,
  "id": "string (identifier)",
  "importance": "String",
  "inferenceClassification": "String",
  "internetMessageId": "String",
  "isDeliveryReceiptRequested": true,
  "isDraft": true,
  "isRead": true,
  "isReadReceiptRequested": true,
  "lastModifiedDateTime": "String (timestamp)",
  "parentFolderId": "string",
  "receivedDateTime": "String (timestamp)",
  "replyTo": [{"@odata.type": "microsoft.graph.recipient"}],
  "sender": {"@odata.type": "microsoft.graph.recipient"},
  "sentDateTime": "String (timestamp)",
  "subject": "string",
  "toRecipients": [{"@odata.type": "microsoft.graph.recipient"}],
  "uniqueBody": {"@odata.type": "microsoft.graph.itemBody"},
  "webLink": "string"
}

```

## <span data-ttu-id="5a0aa-332">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a0aa-332">See also</span></span>
<a id="see-also" class="xliff"></a>

- [<span data-ttu-id="5a0aa-333">Obtener configuración del buzón</span><span class="sxs-lookup"><span data-stu-id="5a0aa-333">Get mailbox settings</span></span>](../api/user_get_mailboxsettings.md) 
- [<span data-ttu-id="5a0aa-334">Actualizar configuración del buzón</span><span class="sxs-lookup"><span data-stu-id="5a0aa-334">Update mailbox settings</span></span>](../api/user_update_mailboxsettings.md)
- [<span data-ttu-id="5a0aa-335">Usar la consulta delta para realizar el seguimiento de los cambios en datos de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="5a0aa-335">Use delta query to track changes in Microsoft Graph data</span></span>](../../../concepts/delta_query_overview.md)
- [<span data-ttu-id="5a0aa-336">Obtener los cambios incrementales en los mensajes de una carpeta</span><span class="sxs-lookup"><span data-stu-id="5a0aa-336">Get incremental changes to messages in a folder</span></span>](../../../concepts/delta_query_messages.md)
- [<span data-ttu-id="5a0aa-337">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="5a0aa-337">Add custom data to resources using extensions</span></span>](../../../concepts/extensibility_overview.md)
- [<span data-ttu-id="5a0aa-338">Agregar datos personalizados a los usuarios mediante extensiones abiertas</span><span class="sxs-lookup"><span data-stu-id="5a0aa-338">Add custom data to users using open extensions</span></span>](../../../concepts/extensibility_open_users.md)
- [<span data-ttu-id="5a0aa-339">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="5a0aa-339">Add custom data to groups using schema extensions</span></span>](../../../concepts/extensibility_schema_groups.md)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "message resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
