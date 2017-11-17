<span data-ttu-id="580bd-p104">Nombre para mostrar de SKU único. Es igual al skuPartNumber en el objeto [SubscribedSku](subscribedsku.md) relacionado; por ejemplo: "AAD_Premium". Solo lectura</span><span class="sxs-lookup"><span data-stu-id="580bd-p104">Unique SKU display name. Equal to the skuPartNumber on the related [SubscribedSku](subscribedsku.md) object; for example: "AAD_Premium". Read-only</span></span>| Nombre para mostrar de SKU único. Es igual al skuPartNumber en el objeto [SubscribedSku](subscribedsku.md) relacionado; por ejemplo: "AAD_Premium". Solo lectura |

## <span data-ttu-id="580bd-132">Relaciones</span><span class="sxs-lookup"><span data-stu-id="580bd-132">Relationships</span></span>
<a id="relationships" class="xliff"></a>
<span data-ttu-id="580bd-133">Ninguno</span><span class="sxs-lookup"><span data-stu-id="580bd-133">None</span></span>

## <span data-ttu-id="580bd-134">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="580bd-134">JSON representation</span></span>
<a id="json-representation" class="xliff"></a>
<span data-ttu-id="580bd-135">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="580bd-135">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.licenseDetails"
}-->

```json
{
  "id": "String (identifier)",
  "servicePlans": [{"@odata.type": "microsoft.graph.servicePlanInfo"}],
  "skuId": "Guid",
  "skuPartNumber": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "licenseDetails resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->