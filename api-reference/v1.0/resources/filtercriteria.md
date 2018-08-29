# <a name="filtercriteria-resource-type"></a>Tipo de recurso FilterCriteria

Representa los criterios de filtrado que se aplican a una columna.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookFilterCriteria"
}-->

```json
{
  "color": "string",
  "criterion1": "string",
  "criterion2": "string",
  "dynamicCriteria": "string",
  "filterOn": "string",
  "icon": {"@odata.type": "microsoft.graph.workbookIcon"},
  "values": {"@odata.type": "microsoft.graph.Json"}
}

```

<!-- {
  "type": "#page.annotation",
  "suppressions": [
    "Warning: /api-reference/v1.0/resources/filtercriteria.md:
      Property 'color' found in resource definition for 'microsoft.graph.workbookFilterCriteria', but not described in markdown table.",
    "Warning: /api-reference/v1.0/resources/filtercriteria.md:
      Property 'criterion1' found in resource definition for 'microsoft.graph.workbookFilterCriteria', but not described in markdown table.",
    "Warning: /api-reference/v1.0/resources/filtercriteria.md:
      Property 'criterion2' found in resource definition for 'microsoft.graph.workbookFilterCriteria', but not described in markdown table.",
    "Warning: /api-reference/v1.0/resources/filtercriteria.md:
      Property 'dynamicCriteria' found in resource definition for 'microsoft.graph.workbookFilterCriteria', but not described in markdown table.",
    "Warning: /api-reference/v1.0/resources/filtercriteria.md:
      Property 'filterOn' found in resource definition for 'microsoft.graph.workbookFilterCriteria', but not described in markdown table.",
    "Warning: /api-reference/v1.0/resources/filtercriteria.md:
      Property 'icon' found in resource definition for 'microsoft.graph.workbookFilterCriteria', but not described in markdown table.",
    "Warning: /api-reference/v1.0/resources/filtercriteria.md:
      Property 'values' found in resource definition for 'microsoft.graph.workbookFilterCriteria', but not described in markdown table."
  ]
} -->