<span data-ttu-id="aa35e-p106">Conjunto de tipos de Microsoft Graph (compatibles con extensiones) a los que se puede aplicar la extensión de esquema. Seleccione **contact**, **device**, **event**, **group**, **message**, **organization**, **post** o **user**.</span><span class="sxs-lookup"><span data-stu-id="aa35e-p106">Set of Microsoft Graph types (that can support extensions) that the schema extension can be applied to. Select from **contact**, **device**, **event**, **group**, **message**, **organization**, **post**, or **user**.</span></span>|Conjunto de tipos de Microsoft Graph (compatibles con extensiones) a los que se puede aplicar la extensión de esquema. Seleccione **contact**, **device**, **event**, **group**, **message**, **organization**, **post** o **user**.|

## <span data-ttu-id="aa35e-166">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="aa35e-166">JSON representation</span></span>
<a id="json-representation" class="xliff"></a>

<span data-ttu-id="aa35e-167">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="aa35e-167">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.schemaExtension"
}-->

```json
{
  "description": "String",
  "id": "String (identifier)",
  "owner": "String",
  "properties": [{"@odata.type": "microsoft.graph.extensionSchemaProperty"}],
  "status": "String",
  "targetTypes": ["String"]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "schemaExtension resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->