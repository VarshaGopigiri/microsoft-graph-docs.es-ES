---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: ChoiceColumn
ms.openlocfilehash: 659ece2eab255fe7b55a258b0980eda4e7bde5b2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083160"
---
# <a name="choicecolumn-resource-type"></a>Tipo de recurso ChoiceColumn

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

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
  "tocPath": "Resources/ChoiceColumn"
} -->
