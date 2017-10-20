---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: ChoiceColumn
ms.openlocfilehash: c266550e8918603c3ee6104818c0aa721f1281d9
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
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
  "tocPath": "Resources/ChoiceColumn"
} -->
