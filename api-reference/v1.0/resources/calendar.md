<span data-ttu-id="737d7-p111">La colección de propiedades extendidas de valor único definidas para el calendario. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="737d7-p111">The collection of single-value extended properties defined for the calendar. Read-only. Nullable.</span></span>| La colección de propiedades extendidas de valor único definidas para el calendario. Solo lectura. Admite valores NULL.|

## <span data-ttu-id="737d7-206">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="737d7-206">JSON representation</span></span>
<a id="json-representation" class="xliff"></a>

<span data-ttu-id="737d7-207">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="737d7-207">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "calendarView",
    "events",
    "multiValueExtendedProperties",
    "singleValueExtendedProperties"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.calendar"
}-->

```json
{
  "canEdit": "boolean",
  "canShare": "boolean",
  "canViewPrivateItems": "boolean",
  "changeKey": "string",
  "color": "String",
  "id": "string (identifier)",
  "name": "string",
  "owner": {"@odata.type": "microsoft.graph.emailAddress"}
}

```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "calendar resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
