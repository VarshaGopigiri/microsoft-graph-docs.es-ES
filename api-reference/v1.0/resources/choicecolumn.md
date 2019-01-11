---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: ChoiceColumn
localization_priority: Normal
ms.openlocfilehash: 3640e68902485215dda575cc93407f019007ee18
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27826582"
---
# <a name="choicecolumn-resource-type"></a>Tipo de recurso ChoiceColumn

El recurso **choiceColumn** en un recurso [columnDefinition](columndefinition.md) indica que se pueden seleccionar los valores de la columna de una lista de opciones.

## <a name="json-representation"></a>Representación JSON

A continuación se incluye una representación JSON de un recurso **ChoiceColumn**.
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.choiceColumn" } -->

```json
{
  "allowTextEntry": true,
  "choices": ["red", "blue", "green"],
  "displayAs": "checkBoxes | dropDownMenu | radioButtons"
}
```

## <a name="properties"></a>Propiedades

| Nombre de la propiedad      | Tipo               | Descripción
|:-------------------|:-------------------|:----------------------------------------------
| **allowTextEntry** | boolean            | Si es true, permite valores personalizados que no están en las opciones configuradas.
| **choices**        | collection(string) | La lista de valores disponibles para esta columna.
| **displayAs**      | string             | Cómo se deben mostrar las opciones en la experiencia de usuario. Debe ser `checkBoxes`, `dropDownMenu` o `radioButtons`


<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/resources/choicecolumn.md:
      Found potential enums in resource example that weren't defined in a table:(checkBoxes,dropDownMenu,radioButtons) are in resource, but () are in table"
  ],
  "tocPath": "Resources/ChoiceColumn"
} -->
