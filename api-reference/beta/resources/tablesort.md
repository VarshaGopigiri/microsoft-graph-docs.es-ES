---
title: Tipo de recurso TableSort
description: Administra operaciones de ordenación en objetos Table.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 5e5e93fb1cccb420e8da08015109c81dc45ae688
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27966492"
---
# <a name="tablesort-resource-type"></a>Tipo de recurso TableSort

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Administra operaciones de ordenación en objetos Table.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get TableSort](../api/tablesort-get.md) | [TableSort](tablesort.md) |Lee las propiedades y relaciones del objeto tableSort.|
|[Apply](../api/tablesort-apply.md)|None|Realiza una operación de ordenación.|
|[Clear](../api/tablesort-clear.md)|None|Borra la ordenación que se aplica actualmente en la tabla. Aunque esto no modifica la ordenación de la tabla, borra el estado de los botones de encabezado.|
|[Reapply](../api/tablesort-reapply.md)|None|Vuelve a aplicar los parámetros de ordenación actuales a la tabla.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|matchCase|boolean|Indica si última ordenación de la tabla distinguía mayúsculas de minúsculas. Solo lectura.|
|method|string|Representa el método de ordenación de caracteres chinos usado por última vez para ordenar la tabla. Valores posibles: `PinYin`, `StrokeCount`. Solo lectura.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|fields|[SortField](sortfield.md)|Representa las condiciones actuales que se usaron por última vez para ordenar la tabla. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.tableSort"
}-->

```json
{
  "matchCase": true,
  "method": "string"
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
