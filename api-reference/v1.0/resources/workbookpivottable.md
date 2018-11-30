---
title: Tipo de recurso PivotTable
description: Representa una tabla dinámica de Excel.
ms.openlocfilehash: b4ddd0c1bb9e4ee13aaf3d1b4472c4e750e3a755
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029258"
---
# <a name="pivottable-resource-type"></a>Tipo de recurso PivotTable

Representa una tabla dinámica de Excel.

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get workbookPivotTable](../api/workbookpivottable-get.md) | [workbookPivotTable](workbookpivottable.md) |Lee las propiedades y relaciones del objeto workbookPivotTable.|
|[Refresh](../api/workbookpivottable-refresh.md)|Ninguno|Actualiza la tabla dinámica. |
|[Refreshall](../api/workbookpivottable-refreshall.md)|Ninguno|Actualizar todas las tablas de una hoja de cálculo. Tenga en cuenta que esta acción sólo está disponible en la colección de tabla dinámica.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|Cadena| ID la tabla dinámica.   Solo lectura.|
|name|String|Nombre de la tabla dinámica.    |

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|worksheet|[WorkbookWorksheet](worksheet.md)| La hoja de cálculo que contiene la tabla dinámica actual. Solo lectura.   |

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
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
