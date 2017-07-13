<span data-ttu-id="83a3d-p103">Establece el tipo de vista previa que aparece en la tarea. Los valores posibles son `automatic`, `noPreview`, `checklist`, `description` y `reference`. Si se establece en `automatic`, la aplicación que visualiza la tarea elige la vista previa mostrada.</span><span class="sxs-lookup"><span data-stu-id="83a3d-p103">This sets the type of preview that shows up on the task. Possible values are: `automatic`, `noPreview`, `checklist`, `description`, `reference`. When set to `automatic` the displayed preview is chosen by the app viewing the task.</span></span>|Establece el tipo de vista previa que aparece en la tarea. Los valores posibles son `automatic`, `noPreview`, `checklist`, `description` y `reference`. Si se establece en `automatic`, la aplicación que visualiza la tarea elige la vista previa mostrada.|
|<span data-ttu-id="83a3d-135">references</span><span class="sxs-lookup"><span data-stu-id="83a3d-135">references</span></span>|[<span data-ttu-id="83a3d-136">plannerExternalReferences</span><span class="sxs-lookup"><span data-stu-id="83a3d-136">plannerExternalReferences</span></span>](plannerexternalreferences.md)|<span data-ttu-id="83a3d-137">La colección de referencias de la tarea.</span><span class="sxs-lookup"><span data-stu-id="83a3d-137">The collection of references on the task.</span></span>|

## <span data-ttu-id="83a3d-138">Relaciones</span><span class="sxs-lookup"><span data-stu-id="83a3d-138">Relationships</span></span>
<a id="relationships" class="xliff"></a>
<span data-ttu-id="83a3d-139">Ninguno</span><span class="sxs-lookup"><span data-stu-id="83a3d-139">None</span></span>


## <span data-ttu-id="83a3d-140">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="83a3d-140">JSON representation</span></span>
<a id="json-representation" class="xliff"></a>
<span data-ttu-id="83a3d-141">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="83a3d-141">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerTaskDetails"
}-->

```json
{
  "checklist": {"@odata.type": "microsoft.graph.plannerChecklistItems"},
  "description": "String",
  "id": "String (identifier)",
  "previewType": "string",
  "references": {"@odata.type": "microsoft.graph.plannerExternalReferences"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerTaskDetails resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->