<span data-ttu-id="8c444-p105">Valor que se debe usar al configurar la propiedad de *período de vida (ttl)* del registro SRV en el host DNS. No admite valores NULL</span><span class="sxs-lookup"><span data-stu-id="8c444-p105">Value to use when configuring the *time-to-live (ttl)* property of the SRV record at the DNS host. Not nullable</span></span>| Valor que se debe usar al configurar la propiedad de *período de vida (ttl)* del registro SRV en el host DNS. No admite valores NULL |
|<span data-ttu-id="8c444-149">weight</span><span class="sxs-lookup"><span data-stu-id="8c444-149">weight</span></span>|<span data-ttu-id="8c444-150">Int32</span><span class="sxs-lookup"><span data-stu-id="8c444-150">Int32</span></span>| <span data-ttu-id="8c444-151">Valor que se debe usar al configurar la propiedad *weight* del registro SRV en el host DNS.</span><span class="sxs-lookup"><span data-stu-id="8c444-151">Value to use when configuring the *weight* property of the SRV record at the DNS host.</span></span> |

## <span data-ttu-id="8c444-152">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8c444-152">Relationships</span></span>
<a id="relationships" class="xliff"></a>
<span data-ttu-id="8c444-153">Ninguno</span><span class="sxs-lookup"><span data-stu-id="8c444-153">None</span></span>


## <span data-ttu-id="8c444-154">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8c444-154">JSON representation</span></span>
<a id="json-representation" class="xliff"></a>
<span data-ttu-id="8c444-155">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8c444-155">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.domainDnsSrvRecord"
}-->

```json
{
  "canonicalName": "String",
  "id": "String (identifier)",
  "isOptional": true,
  "label": "String",
  "nameTarget": "String",
  "port": 1024,
  "priority": 1024,
  "protocol": "String",
  "recordType": "String",
  "service": "String",
  "supportedService": "String",
  "ttl": 1024,
  "weight": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "domainDnsSrvRecord resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->