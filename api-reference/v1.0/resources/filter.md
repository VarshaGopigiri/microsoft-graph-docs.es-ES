# <a name="filter-resource-type"></a>Tipo de recurso Filter

Administra el filtrado de la columna de una tabla.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Apply](../api/filter_apply.md)|Ninguno|Aplica los criterios de filtro especificados en la columna especificada.|
|[Clear](../api/filter_clear.md)|Ninguno|Borra el filtro de la columna especificada.|

## <a name="properties"></a>Propiedades

| Nombre | Tipo   |Descripción|
|:---------------|:--------|:----------|
|criteria|[WorkbookFilterCriteria](filtercriteria.md)|Filtro aplicado actualmente en la columna especificada. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookFilter"
}-->

```json
{
  "criteria": {"@odata.type": "microsoft.graph.workbookFilterCriteria" }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Filter resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->