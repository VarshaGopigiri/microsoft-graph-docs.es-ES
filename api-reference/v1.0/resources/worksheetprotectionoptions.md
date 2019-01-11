---
title: Tipo de recurso WorksheetProtectionOptions
description: Representa las opciones de protección de hoja.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: c1e9b9510e56d240175fc5aa9d5631a962458af4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27890142"
---
# <a name="worksheetprotectionoptions-resource-type"></a>Tipo de recurso WorksheetProtectionOptions

Representa las opciones de protección de hoja.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|allowAutoFilter|boolean|Representa la opción de protección de la hoja de cálculo que permite usar la característica de filtro automático.|
|allowDeleteColumns|boolean|Representa la opción de protección de la hoja de cálculo que permite eliminar columnas.|
|allowDeleteRows|boolean|Representa la opción de protección de la hoja de cálculo que permite eliminar filas.|
|allowFormatCells|boolean|Representa la opción de protección de la hoja de cálculo que permite aplicar formato a celdas.|
|allowFormatColumns|boolean|Representa la opción de protección de la hoja de cálculo que permite aplicar formato a columnas.|
|allowFormatRows|boolean|Representa la opción de protección de la hoja de cálculo que permite aplicar formato a filas.|
|allowInsertColumns|boolean|Representa la opción de protección de la hoja de cálculo que permite insertar columnas.|
|allowInsertHyperlinks|boolean|Representa la opción de protección de la hoja de cálculo que permite insertar hipervínculos.|
|allowInsertRows|boolean|Representa la opción de protección de la hoja de cálculo que permite insertar filas.|
|allowPivotTables|boolean|Representa la opción de protección de la hoja de cálculo que permite usar la característica de tabla dinámica.|
|allowSort|boolean|Representa la opción de protección de la hoja de cálculo que permite usar la característica de ordenación.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookWorksheetProtectionOptions"
}-->

```json
{
  "allowAutoFilter": true,
  "allowDeleteColumns": true,
  "allowDeleteRows": true,
  "allowFormatCells": true,
  "allowFormatColumns": true,
  "allowFormatRows": true,
  "allowInsertColumns": true,
  "allowInsertHyperlinks": true,
  "allowInsertRows": true,
  "allowPivotTables": true,
  "allowSort": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "WorksheetProtectionOptions resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
