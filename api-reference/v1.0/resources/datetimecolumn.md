---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: DateTimeColumn
ms.openlocfilehash: 6f2c14d5fa67fa80c869c20081250bfa55e0f5e4
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23267832"
---
# <a name="datetimecolumn-resource-type"></a>Tipo de recurso DateTimeColumn

El recurso **dateTimeColumn** en un recurso [columnDefinition](columnDefinition.md) indica que los valores de la columna son fechas u horas.

## <a name="json-representation"></a>Representación JSON

A continuación se incluye una representación JSON de un recurso **dateTimeColumn**.
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.dateTimeColumn" } -->

```json
{
  "displayAs": "default | friendly | standard",
  "format": "dateOnly | dateTime"
}
```

## <a name="properties"></a>Propiedades

| Nombre de propiedad      | Tipo               | Descripción
|:-------------------|:-------------------|:----------------------------------------------
| **displayAs**      | cadena             | Cómo se debe presentar el valor en la experiencia de usuario. Debe ser `default`, `friendly` o `standard`. Vea lo que se muestra a continuación para obtener más detalles. Si no se especifica, se trata como `default`.
| **format**         | cadena             | Indica si el valor debe presentarse solo como una fecha o como fecha y hora. Debe ser `dateOnly` o `dateTime`

## <a name="displayas-options"></a>Opciones de displayAs

| Valor        | Descripción
|:-------------|:--------------------------------------------------------------
| **default**  | Usa la representación predeterminada de la experiencia de usuario.
| **friendly** | Usa una representación relativa descriptiva (p. ej., "hoy a las 3:00 p. m.")
| **standard** | Usa la representación absoluta estándar (p. ej. "5/10/2017 3:20 p. m.")


<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/resources/choicecolumn.md:
      Found potential enums in resource example that weren't defined in a table:(checkBoxes,dropDownMenu,radioButtons) are in resource, but () are in table",
    "Warning: /api-reference/v1.0/resources/datetimecolumn.md:
      Found potential enums in resource example that weren't defined in a table:(default,friendly,standard) are in resource, but () are in table",
    "Warning: /api-reference/v1.0/resources/datetimecolumn.md:
      Found potential enums in resource example that weren't defined in a table:(dateOnly,dateTime) are in resource, but () are in table"
  ],
  "tocPath": "Resources/DateTimeColumn"
} -->
