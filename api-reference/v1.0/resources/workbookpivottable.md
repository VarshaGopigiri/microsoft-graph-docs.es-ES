---
title: Tipo de recurso PivotTable
description: Representa una tabla dinámica de Excel.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 5f6360ce1eacc313f1bcc8a9f59b44b216a87b84
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27958743"
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
|name|Cadena|Nombre de la tabla dinámica.    |

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
