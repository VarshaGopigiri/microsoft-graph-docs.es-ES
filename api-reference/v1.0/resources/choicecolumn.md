---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: ChoiceColumn
ms.openlocfilehash: 9feb49fc9c581a4518f63a0367087d54de32cff4
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23264073"
---
# <a name="choicecolumn-resource-type"></a>Tipo de recurso ChoiceColumn

El recurso **choiceColumn** en un recurso [columnDefinition](columnDefinition.md) indica que se pueden seleccionar los valores de la columna de una lista de opciones.

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

| Nombre de propiedad      | Tipo               | Descripción
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
