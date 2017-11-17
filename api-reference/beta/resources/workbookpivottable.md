<a id="pivottable-resource-type" class="xliff"></a>
# Tipo de recurso PivotTable

Representa una tabla dinámica de Excel.

<a id="methods" class="xliff"></a>
## Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get workbookPivotTable](../api/workbookpivottable_get.md) | [workbookPivotTable](workbookpivottable.md) |Lee las propiedades y relaciones del objeto workbookPivotTable.|
|[Refresh](../api/workbookpivottable_refresh.md)|Ninguno|Actualiza la tabla dinámica. |
|[Refreshall](../api/workbookpivottable_refreshall.md)|Ninguno|Actualizar todas las tablas de una hoja de cálculo. Tenga en cuenta que esta acción sólo está disponible en la colección de tabla dinámica.|

<a id="properties" class="xliff"></a>
## Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|Cadena| ID la tabla dinámica.   Solo lectura.|
|name|String|Nombre de la tabla dinámica.    |

<a id="relationships" class="xliff"></a>
## Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|worksheet|[worksheet](worksheet.md)| La hoja de cálculo que contiene la tabla dinámica actual. Solo lectura.   |

<a id="json-representation" class="xliff"></a>
## Representación JSON
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
