---
title: Tipo de recurso Worksheet
description: Una hoja de cálculo de Excel es una cuadrícula de celdas. Puede contener datos, tablas, gráficos, etc.
localization_priority: Normal
author: lumine2008
ms.prod: excel
ms.openlocfilehash: d04ebafda64f9a081096fbf0fd94461b9765a6db
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27926529"
---
# <a name="worksheet-resource-type"></a>Tipo de recurso Worksheet

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Una hoja de cálculo de Excel es una cuadrícula de celdas. Puede contener datos, tablas, gráficos, etc.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get Worksheet](../api/worksheet-get.md) | [Worksheet](worksheet.md) |Lee las propiedades y relaciones del objeto worksheet.|
|[Create Chart](../api/worksheet-post-charts.md) |[Chart](chart.md)| Cree un gráfico publicando en la colección de gráficos.|
|[List names](../api/worksheet-list-names.md) |Colección [NamedItem](nameditem.md)| Obtenga la colección del elemento con nombre asociada a la hoja de cálculo.|
|[List charts](../api/worksheet-list-charts.md) |Colección [Chart](chart.md)| Obtiene la colección de objetos Chart.|
|[Create Table](../api/worksheet-post-tables.md) |[Tabla](table.md)| Crea un Table publicándolo en la colección tables.|
|[List tables](../api/worksheet-list-tables.md) |Colección [Table](table.md)| Obtiene una colección de objetos Table.|
|[Update](../api/worksheet-update.md) | [Worksheet](worksheet.md)   |Actualiza el objeto Worksheet. |
|[Cell](../api/worksheet-cell.md)|[Range](range.md)|Obtiene el objeto de rango que contiene la celda en función de los números de fila y columna. La celda puede estar fuera de los límites del rango principal, siempre y cuando permanezca dentro de la cuadrícula de la hoja de cálculo.|
|[Range](../api/worksheet-range.md)|[Range](range.md)|Obtiene el objeto de rango especificado por la dirección o el nombre.|
|[Usedrange](../api/worksheet-usedrange.md)|[Range](range.md)|El rango usado es el rango más pequeño que abarque las celdas que tienen asignado un valor o un formato. Si la hoja de cálculo está en blanco, esta función devolverá la celda superior izquierda.|
|[Delete](../api/worksheet-delete.md)|None|Elimina la hoja de cálculo del libro.|
|[List](../api/worksheet-list.md) | Colección [Worksheet](worksheet.md) |Obtiene la colección de objetos worksheet. |
|[Add](../api/worksheetcollection-add.md)|[Worksheet](worksheet.md)|Agrega una nueva hoja de cálculo al libro. La hoja de cálculo se agregará al final de las hojas de cálculo existentes. |
|[List pivotTables](../api/workbookworksheet-list-pivottables.md) |Colección [workbookPivotTable](workbookpivottable.md)| Obtiene una colección de objetos workbookPivotTable.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|string|Devuelve un valor que identifica de forma única la hoja de cálculo de un libro determinado. El valor del identificador permanece igual, incluso cuando se cambia el nombre de la hoja de cálculo o cuando esta se mueve. Solo lectura.|
|name|string|Nombre para mostrar de la hoja de cálculo.|
|position|entero|Posición de base cero de la hoja de cálculo dentro del libro.|
|visibility|string|Visibilidad de la hoja de cálculo. Valores posibles: `Visible`, `Hidden`, `VeryHidden`.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|charts|Colección [Chart](chart.md)|Devuelve la colección de gráficos que forman parte de la hoja de cálculo. Solo lectura.|
|names|Colección [NamedItem](nameditem.md)|Devuelve la colección de los nombres asociados a la hoja de cálculo. Solo lectura.|
|pivotTables|Colección [workbookPivotTable](workbookpivottable.md)| Colección de tablas dinámicas que forman parte de la hoja de cálculo. |
|protection|[WorksheetProtection](worksheetprotection.md)|Devuelve el objeto de protección de hoja de una hoja de cálculo. Solo lectura.|
|tables|Colección [Table](table.md)|Colección de tablas que forman parte de la hoja de cálculo. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.worksheet"
}-->

```json
{
  "id": "string",
  "name": "string",
  "position": 1024,
  "visibility": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Worksheet resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
