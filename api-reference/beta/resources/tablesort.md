---
title: Tipo de recurso TableSort
description: Administra operaciones de ordenación en objetos Table.
ms.openlocfilehash: 02ee1f72bc53a3097c76cf9bab62a165fe3c56f8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27091064"
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