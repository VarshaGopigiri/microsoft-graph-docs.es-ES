---
title: Tipo de recurso TableSort
description: Administra operaciones de ordenación en objetos Table.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: be607832be82b99853b4cd44cfa5b60449a2c432
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27929476"
---
# <a name="tablesort-resource-type"></a>Tipo de recurso TableSort

Administra operaciones de ordenación en objetos Table.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get TableSort](../api/tablesort-get.md) | [WorkbookTableSort](tablesort.md) |Lee las propiedades y relaciones del objeto tableSort.|
|[Apply](../api/tablesort-apply.md)|None|Realiza una operación de ordenación.|
|[Clear](../api/tablesort-clear.md)|None|Borra la ordenación que se aplica actualmente en la tabla. Aunque esto no modifica la ordenación de la tabla, borra el estado de los botones de encabezado.|
|[Reapply](../api/tablesort-reapply.md)|None|Vuelve a aplicar los parámetros de ordenación actuales a la tabla.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|fields|Colección de [WorkbookSortField](sortfield.md)|Representa las condiciones actuales que se usaron por última vez para ordenar la tabla. Solo lectura.|
|matchCase|boolean|Indica si última ordenación de la tabla distinguía mayúsculas de minúsculas. Solo lectura.|
|method|string|Representa el método utilizado por última vez para ordenar la tabla de orden de los caracteres chinos. Los valores posibles son: `PinYin`, `StrokeCount`. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookTableSort"
}-->

```json
{
  "matchCase": true,
  "method": "string",
  "fields": [{ "@odata.type": "microsoft.graph.workbookSortField" }]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "TableSort resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
