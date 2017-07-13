<span data-ttu-id="eb86a-p103">Conjunto de identificadores de usuario con el que se comparte este plan. Si está aprovechando los grupos de Office 365, use la API de grupos para administrar la pertenencia a los grupos a fin de compartir el plan del [grupo](group.md). También puede agregar los miembros existentes del grupo a esta colección, aunque no es necesario que obtengan acceso al plan propiedad del grupo.</span><span class="sxs-lookup"><span data-stu-id="eb86a-p103">Set of user ids that this plan is shared with. If you are leveraging Office 365 Groups, use the Groups API to manage group membership to share the [group's](group.md) plan. You can also add existing members of the group to this collection though it is not required for them to access the plan owned by the group.</span></span>|Conjunto de identificadores de usuario con el que se comparte este plan. Si está aprovechando los grupos de Office 365, use la API de grupos para administrar la pertenencia a los grupos a fin de compartir el plan del [grupo](group.md). También puede agregar los miembros existentes del grupo a esta colección, aunque no es necesario que obtengan acceso al plan propiedad del grupo. |

## <span data-ttu-id="eb86a-132">Relaciones</span><span class="sxs-lookup"><span data-stu-id="eb86a-132">Relationships</span></span>
<a id="relationships" class="xliff"></a>
<span data-ttu-id="eb86a-133">Ninguno</span><span class="sxs-lookup"><span data-stu-id="eb86a-133">None</span></span>


## <span data-ttu-id="eb86a-134">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="eb86a-134">JSON representation</span></span>
<a id="json-representation" class="xliff"></a>
<span data-ttu-id="eb86a-135">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="eb86a-135">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerPlanDetails"
}-->

```json
{
  "categoryDescriptions": {"@odata.type": "microsoft.graph.plannerCategoryDescriptions"},
  "id": "String (identifier)",
  "sharedWith": {"@odata.type": "microsoft.graph.plannerUserIds"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerPlanDetails resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->