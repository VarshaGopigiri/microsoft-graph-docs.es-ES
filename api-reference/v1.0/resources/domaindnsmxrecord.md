<span data-ttu-id="356ab-p105">Valor que se debe usar al configurar la propiedad de *período de vida (ttl)* del registro MX en el host DNS. No admite valores NULL</span><span class="sxs-lookup"><span data-stu-id="356ab-p105">Value to use when configuring the *time-to-live (ttl)* property of the MX record at the DNS host. Not nullable</span></span>| Valor que se debe usar al configurar la propiedad de *período de vida (ttl)* del registro MX en el host DNS. No admite valores NULL |

## <span data-ttu-id="356ab-140">Relaciones</span><span class="sxs-lookup"><span data-stu-id="356ab-140">Relationships</span></span>
<a id="relationships" class="xliff"></a>
<span data-ttu-id="356ab-141">Ninguno</span><span class="sxs-lookup"><span data-stu-id="356ab-141">None</span></span>

## <span data-ttu-id="356ab-142">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="356ab-142">JSON representation</span></span>
<a id="json-representation" class="xliff"></a>
<span data-ttu-id="356ab-143">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="356ab-143">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.domainDnsMxRecord"
}-->

```json
{
  "canonicalName": "String",
  "id": "String (identifier)",
  "isOptional": true,
  "label": "String",
  "mailExchange": "String",
  "preference": 1024,
  "recordType": "String",
  "supportedService": "String",
  "ttl": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "domainDnsMxRecord resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->