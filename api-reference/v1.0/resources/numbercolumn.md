---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: NumberColumn
ms.openlocfilehash: 3bc5ef0c2764fc941959a69ae58402ce3717e7b3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031861"
---
# <a name="numbercolumn-resource-type"></a>Tipo de recurso NumberColumn

El recurso **numberColumn** en un recurso [columnDefinition](columndefinition.md) indica que los valores de la columna son números.

## <a name="json-representation"></a>Representación JSON

A continuación se incluye una representación JSON de un recurso **numberColumn**.
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.numberColumn" } -->

```json
{
  "decimalPlaces": "automatic | none | one | two | three | four | five",
  "displayAs": "number | percentage",
  "maximum": 10.551,
  "minimum": 99.993
}
```

## <a name="properties"></a>Propiedades

| Nombre de la propiedad      | Tipo   | Descripción
|:-------------------|:-------|:-----------------------------------------------
| **decimalPlaces**  | string | El número de decimales que se mostrará. Consulte a continuación para obtener información sobre los valores posibles.
| **displayAs**      | string | Cómo se debe presentar el valor en la experiencia de usuario. Debe ser `number` o `percentage`. Si no se especifica, se trata como `number`.
| **maximum**        | double | El valor máximo permitido.
| **minimum**        | double | El valor mínimo permitido.

## <a name="decimalplaces"></a>DecimalPlaces

| Valor          | Descripción
|:---------------|:--------------------------------------------------------------
| **automatic**  | Valor predeterminado. Se muestran decimales automáticamente según sea necesario.
| **none**       | No se muestra ningún decimal.
| **one**        | Se muestra siempre un decimal.
| **two**        | Se muestran siempre dos decimales.
| **three**      | Se muestran siempre tres decimales.
| **four**       | Se muestran siempre cuatro decimales.
| **five**       | Se muestran siempre cinco decimales.

Nota: **decimalPlaces** y **displayAs** se aplican a cómo se representan los números, no a cómo se almacenan.
Estas propiedades se pueden actualizar.

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/resources/numbercolumn.md:
      Found potential enums in resource example that weren't defined in a table:(automatic,none,one,two,three,four,five) are in resource, but () are in table",
    "Warning: /api-reference/v1.0/resources/numbercolumn.md:
      Found potential enums in resource example that weren't defined in a table:(number,percentage) are in resource, but () are in table"
  ],
  "tocPath": "Resources/NumberColumn"
} -->
