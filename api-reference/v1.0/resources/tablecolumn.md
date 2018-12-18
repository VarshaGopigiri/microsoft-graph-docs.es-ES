---
title: Tipo de recurso TableColumn
description: Representa una columna en una tabla.
author: lumine2008
ms.openlocfilehash: d2d83859c15a24624d8711a7ef86e3b0c89448e1
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27315130"
---
# <a name="tablecolumn-resource-type"></a>Tipo de recurso TableColumn

Representa una columna en una tabla.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get TableColumn](../api/tablecolumn-get.md) | [WorkbookTableColumn](tablecolumn.md) |Lee las propiedades y relaciones del objeto tableColumn.|
|[Update](../api/tablecolumn-update.md) | [WorkbookTableColumn](tablecolumn.md) |Actualiza el objeto TableColumn. |
|[Databodyrange](../api/tablecolumn-databodyrange.md)|[Range](range.md)|Obtiene el objeto de rango asociado al cuerpo de datos de la columna.|
|[Headerrowrange](../api/tablecolumn-headerrowrange.md)|[Range](range.md)|Obtiene el objeto de rango asociado a la fila de encabezado de la columna.|
|[Range](../api/tablecolumn-range.md)|[Range](range.md)|Obtiene el objeto de rango asociado a toda la columna.|
|[Totalrowrange](../api/tablecolumn-totalrowrange.md)|[Range](range.md)|Obtiene el objeto de rango asociado a la fila de totales de la columna.|
|[Delete](../api/tablecolumn-delete.md)|None|Elimina la columna de la tabla.|
|[List](../api/tablecolumn-list.md) | Colección de [WorkbookTableColumn](tablecolumn.md) |Obtiene la colección de objetos tableColumn. |
|[Itemat](../api/tablecolumncollection-itemat.md)|[WorkbookTableColumn](tablecolumn.md)|Obtiene una columna en función de su posición en la colección.|
|[Add](../api/tablecolumncollection-add.md)|[WorkbookTableColumn](tablecolumn.md)|Agrega una nueva columna a la tabla.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|cadena|Devuelve una clave única que identifica la columna de la tabla. Esta propiedad debe interpretarse como un valor de cadena opaco y no se debería analizar para ningún otro tipo. Solo lectura.|
|Index|int|Devuelve el número de índice de la columna dentro de la colección de columnas de la tabla. Indizado con cero. Solo lectura.|
|name|string|Devuelve el nombre de la columna de la tabla. Solo lectura.|
|values|Json|Representa los valores sin formato del intervalo especificado. Los datos devueltos pueden ser de tipo string, number o boolean. La celda que contenga un error devolverá la cadena de error.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|filter|[WorkbookFilter](filter.md)|Recupera el filtro aplicado a la columna. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookTableColumn"
}-->

```json
{
  "id": 1024,
  "index": 1024,
  "name": "string",
  "values": "json"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "TableColumn resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
