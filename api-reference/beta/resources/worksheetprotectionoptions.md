---
title: Tipo de recurso WorksheetProtectionOptions
description: Representa las opciones de protección de hoja.
author: lumine2008
ms.openlocfilehash: 772c8b5eca7e9754a6bbc00e43cac102680974a1
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27348576"
---
# <a name="worksheetprotectionoptions-resource-type"></a>Tipo de recurso WorksheetProtectionOptions

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

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
  "@odata.type": "microsoft.graph.worksheetProtectionOptions"
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