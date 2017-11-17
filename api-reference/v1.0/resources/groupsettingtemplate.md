<span data-ttu-id="17003-p102">Identificador único de la plantilla. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="17003-p102">Unique identifier for the subscription. Read-only.</span></span>| Identificador único de la plantilla. Solo lectura.|
|<span data-ttu-id="17003-131">values</span><span class="sxs-lookup"><span data-stu-id="17003-131">values</span></span>|<span data-ttu-id="17003-132">Colección de [settingTemplateValue](settingtemplatevalue.md)</span><span class="sxs-lookup"><span data-stu-id="17003-132">[settingTemplateValue](settingtemplatevalue.md) collection</span></span>| <span data-ttu-id="17003-133">Colección de settingTemplateValues que enumera el conjunto de opciones disponibles, los valores predeterminados y los tipos que forman esta plantilla.</span><span class="sxs-lookup"><span data-stu-id="17003-133">Collection of settingTemplateValues that list the set of available settings, defaults and types that make up this template.</span></span> |

## <a name="relationships"></a><span data-ttu-id="17003-134">Relaciones</span><span class="sxs-lookup"><span data-stu-id="17003-134">Relationships</span></span>

<span data-ttu-id="17003-135">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="17003-135">None.</span></span>


## <a name="json-representation"></a><span data-ttu-id="17003-136">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="17003-136">JSON representation</span></span>

<span data-ttu-id="17003-137">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="17003-137">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.groupSettingTemplate"
}-->

```json
{
  "description": "String",
  "displayName": "String",
  "id": "String (identifier)",
  "values": [{"@odata.type": "microsoft.graph.settingTemplateValue"}]
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "groupSettingTemplate resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->