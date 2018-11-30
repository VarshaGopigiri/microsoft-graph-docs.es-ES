---
title: Tipo de recurso TableRow
description: Representa una fila de una tabla.
ms.openlocfilehash: ca363f8202d61364c609144eaa2fc136ab8b2928
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087220"
---
# <a name="tablerow-resource-type"></a>Tipo de recurso TableRow

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa una fila de una tabla.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get TableRow](../api/tablerow-get.md) | [TableRow](tablerow.md) |Lee las propiedades y relaciones del objeto tableRow.|
|[Update](../api/tablerow-update.md) | [TableRow](tablerow.md)  |Actualiza el objeto TableRow. |
|[Range](../api/tablerow-range.md)|[Range](range.md)|Devuelve el objeto de rango asociado a toda la fila.|
|[Delete](../api/tablerow-delete.md)|None|Elimina la fila de la tabla.|
|[List](../api/tablerow-list.md) | Colección [TableRow](tablerow.md) |Obtiene la colección de objetos tableRow. |
|[Itemat](../api/tablerowcollection-itemat.md)|[TableRow](tablerow.md)|Obtiene una fila en función de su posición en la colección.|
|[Add](../api/tablerowcollection-add.md)|[TableRow](tablerow.md)|Agrega una nueva fila a la tabla.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|index|int|Devuelve el número de índice de la fila dentro de la colección de filas de la tabla. Indizado con cero. Solo lectura.|
|values|json|Representa los valores sin formato del intervalo especificado. Los datos devueltos pueden ser de tipo string, number o boolean. La celda que contenga un error devolverá la cadena de error.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.tableRow"
}-->

```json
{
  "index": 1024,
  "values": "json"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "TableRow resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->