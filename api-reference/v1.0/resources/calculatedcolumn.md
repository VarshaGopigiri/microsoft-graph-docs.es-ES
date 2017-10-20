---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: CalculatedColumn
ms.openlocfilehash: 44700ba7606243002798ec0ec84c3be30d38ef1f
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="calculatedcolumn-resource-type"></a>Tipo de recurso CalculatedColumn

El recurso **calculatedColumn** en un recurso [columnDefinition](columnDefinition.md) indica que los datos de la columna se calculan en función de otras columnas en el sitio.

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
  "tocPath": "Resources/CalculatedColumn"
} -->
