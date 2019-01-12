---
title: Tipo de recurso Table
description: Representa una tabla de Excel.
author: lumine2008
localization_priority: Priority
ms.prod: excel
ms.openlocfilehash: 97755052a1f0e5cf91fb45987870b498832ee735
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27967857"
---
# <a name="table-resource-type"></a>Tipo de recurso Table

Representa una tabla de Excel.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get Table](../api/table-get.md) | [WorkbookTable](table.md) |Lee las propiedades y relaciones del objeto table.|
|[Create TableColumn](../api/table-post-columns.md) |[WorkbookTableColumn](tablecolumn.md)| Crea un TableColumn publicándolo en la colección columns.|
|[List columns](../api/table-list-columns.md) |Colección de [WorkbookTableColumn](tablecolumn.md)| Obtiene una colección de objetos TableColumn.|
|[Create TableRow](../api/table-post-rows.md) |[WorkbookTableRow](tablerow.md)| Crea un TableRow publicándolo en la colección rows.|
|[List rows](../api/table-list-rows.md) |Colección de [WorkbookTableRow](tablerow.md)| Obtiene una colección de objetos TableRow.|
|[Update](../api/table-update.md) | [WorkbookTable](table.md)   |Actualiza el objeto Table. |
|[Databodyrange](../api/table-databodyrange.md)|[Range](range.md)|Obtiene el objeto de rango asociado al cuerpo de datos de la tabla.|
|[Headerrowrange](../api/table-headerrowrange.md)|[Range](range.md)|Obtiene el objeto de rango asociado a la fila de encabezado de la tabla.|
|[Range](../api/table-range.md)|[Range](range.md)|Obtiene el objeto de rango asociado a toda la tabla.|
|[Totalrowrange](../api/table-totalrowrange.md)|[Range](range.md)|Obtiene el objeto de rango asociado a la fila de totales de la tabla.|
|[Clearfilters](../api/table-clearfilters.md)|None|Borra todos los filtros aplicados actualmente en la tabla.|
|[Converttorange](../api/table-converttorange.md)|[Range](range.md)|Convierte la tabla en un rango de celdas normal. Se conservan todos los datos.|
|[Delete](../api/table-delete.md)|None|Elimina la tabla.|
|[Reapplyfilters](../api/table-reapplyfilters.md)|None|Vuelve a aplicar todos los filtros aplicados actualmente en la tabla.|
|[List](../api/table-list.md) | Colección de [WorkbookTable](table.md) |Obtener la colección de objetos table. |
|[Add](../api/tablecollection-add.md)|[WorkbookTable](table.md)|Crea una tabla nueva. La dirección de origen del rango determina la hoja de cálculo en la que se agregará la tabla. Si no se puede agregar la tabla (por ejemplo, porque la dirección no es válida o porque la tabla se superpondría con otra tabla), se producirá un error.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|cadena|Devuelve un valor que identifica de forma única la tabla de un libro determinado. El valor del identificador permanece igual, incluso cuando se cambia el nombre de la tabla. Esta propiedad debe interpretarse como un valor de cadena opaco y no se debería analizar para ningún otro tipo. Solo lectura.|
|name|string|Nombre de la tabla.|
|showHeaders|boolean|Indica si la fila de encabezado está visible o no. Este valor puede establecerse para que muestre o quite la fila de encabezado.|
|showTotals|boolean|Indica si la fila de totales está visible o no. Este valor puede establecerse para que muestre o quite la fila de totales.|
|style|string|Valor constante que representa el estilo de tabla. Los valores posibles son: TableStyleLight1 a través de TableStyleLight21, TableStyleMedium1 a través de TableStyleMedium28, TableStyleStyleDark1 a través de TableStyleStyleDark11. También se puede especificar un personalizadas definidas por el usuario estilo presente en el libro.|
|highlightFirstColumn|Booleano|Indica si la primera columna contiene un formato especial.   |
|highlightLastColumn|Booleano|Indica si la última columna contiene un formato especial. |
|showBandedColumns|Booleano|Indica si las columnas muestran un formato con bandas en el que las columnas impares están resaltadas de manera diferente que las pares para facilitar la lectura de la tabla.   |
|showBandedRows|Booleano|Indica si las filas muestran un formato con bandas en el que las filas impares están resaltadas de manera diferente que las pares para facilitar la lectura de la tabla.    |
|showFilterButton|Booleano|Indica si los botones de filtro son visibles en la parte superior de cada encabezado de columna. Esta configuración solo se permite si la tabla contiene una fila de encabezado.   |
|legacyId|String|Identificador heredado usado en clientes anteriores de Excel. El valor del identificador permanece igual, incluso cuando se cambia el nombre de la tabla. Esta propiedad debe interpretarse como un valor de cadena opaco y no se debería analizar para ningún otro tipo. Solo lectura.   |

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|columns|Colección de [WorkbookTableColumn](tablecolumn.md)|Representa una colección de todas las columnas de la tabla. Solo lectura.|
|rows|Colección de [WorkbookTableRow](tablerow.md)|Representa una colección de todas las filas de la tabla. Solo lectura.|
|sort|[WorkbookTableSort](tablesort.md)|Representa la ordenación de la tabla. Solo lectura.|
|worksheet|[WorkbookWorksheet](worksheet.md)|Hoja de cálculo que contiene la tabla actual. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "optionalProperties": [
     "legacyId"
  ],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookTable"
}-->

```json
{
  "highlightFirstColumn": true,
  "highlightLastColumn": true,
  "id": "String (identifier)",
  "name": "String",
  "showBandedColumns": true,
  "showBandedRows": true,
  "showFilterButton": true,
  "showHeaders": true,
  "showTotals": true,
  "style": "String",
  "legacyId": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Table resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
