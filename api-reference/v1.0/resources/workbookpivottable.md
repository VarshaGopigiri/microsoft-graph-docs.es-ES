# <a name="pivottable-resource-type"></a>Tipo de recurso PivotTable

Representa una tabla dinámica de Excel.

### <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get workbookPivotTable](../api/workbookpivottable_get.md) | [workbookPivotTable](workbookpivottable.md) |Lee las propiedades y relaciones del objeto workbookPivotTable.|
|[Refresh](../api/workbookpivottable_refresh.md)|Ninguno|Actualiza la tabla dinámica.    |
|[Refreshall](../api/workbookpivottable_refreshall.md)|Ninguno|Actualizar todas las tablas de una hoja de cálculo. Tenga en cuenta que esta acción sólo está disponible en la colección de tabla dinámica.|

### <a name="properties"></a>Propiedades
| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
|id|String| ID la tabla dinámica.    Solo lectura.|
|name|Cadena|Nombre de la tabla dinámica.    |

### <a name="relationships"></a>Relaciones
| Relación | Tipo    |Descripción|
|:---------------|:--------|:----------|
|worksheet|[worksheet](worksheet.md)| La hoja de cálculo que contiene la tabla dinámica actual. Solo lectura.    |

### <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookPivotTable"
}-->

```json
{
  "id": "String (identifier)",
  "name": "String"
}

```
