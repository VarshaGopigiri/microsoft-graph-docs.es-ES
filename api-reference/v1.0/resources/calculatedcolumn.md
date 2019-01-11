---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: CalculatedColumn
localization_priority: Normal
ms.openlocfilehash: 402ec948344931a0506026e4ad6abfaaa0ee5539
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27876933"
---
# <a name="calculatedcolumn-resource-type"></a>Tipo de recurso CalculatedColumn

El recurso **calculatedColumn** en un recurso [columnDefinition](columndefinition.md) indica que los datos de la columna se calculan en función de otras columnas en el sitio.

## <a name="json-representation"></a>Representación JSON

A continuación se incluye una representación JSON de un recurso **calculatedColumn**.
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.calculatedColumn" } -->

```json
{
  "format": "dateOnly | dateTime",
  "formula": "=[Column1]+[Column2]+[Column3]",
  "outputType": "boolean | currency | dateTime | number | text",
}
```

## <a name="properties"></a>Propiedades

| Nombre de la propiedad  | Tipo    | Descripción
|:---------------|:--------|:--------------------------------------------------
| **format**     | string  | Para tipos de salida `dateTime`, el formato del valor. Debe ser `dateOnly` o `dateTime`.
| **formula**    | string  | La fórmula usada para calcular el valor de esta columna.
| **outputType** | string  | El tipo de salida usado para dar formato a los valores de esta columna. Debe ser `boolean`, `currency`, `dateTime`, `number` o `text`.

Las fórmulas de SharePoint usan una sintaxis similar a las fórmulas de Excel.
Vea [Ejemplos de fórmulas comunes en listas de SharePoint][SPFormulas] para obtener más información.

[SPFormulas]: https://support.office.com/en-us/article/Examples-of-common-formulas-in-SharePoint-Lists-d81f5f21-2b4e-45ce-b170-bf7ebf6988b3

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/resources/calculatedcolumn.md:
      Found potential enums in resource example that weren't defined in a table:(dateOnly,dateTime) are in resource, but () are in table",
    "Warning: /api-reference/v1.0/resources/calculatedcolumn.md:
      Found potential enums in resource example that weren't defined in a table:(boolean,currency,dateTime,number,text) are in resource, but () are in table"
  ],
  "tocPath": "Resources/CalculatedColumn"
} -->
