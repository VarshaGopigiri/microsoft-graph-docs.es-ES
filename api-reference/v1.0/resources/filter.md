---
title: Tipo de recurso Filter
description: Administra el filtrado de la columna de una tabla.
ms.openlocfilehash: 272b4ea0ee91c25ea845217512a12e33b08ed7b8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030240"
---
# <a name="filter-resource-type"></a>Tipo de recurso Filter

Administra el filtrado de la columna de una tabla.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Apply](../api/filter-apply.md)|None|Aplica los criterios de filtro especificados en la columna especificada.|
|[Clear](../api/filter-clear.md)|None|Borra el filtro de la columna especificada.|

## <a name="properties"></a>Propiedades

| Nombre | Tipo   |Descripción|
|:---------------|:--------|:----------|
|criterios|[WorkbookFilterCriteria](filtercriteria.md)|Filtro aplicado actualmente en la columna especificada. Solo lectura.|

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