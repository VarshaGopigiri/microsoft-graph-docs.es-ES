---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: DateTimeColumn
localization_priority: Normal
ms.openlocfilehash: ea6298428062aa537ec25945aed339738f432762
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27820849"
---
# <a name="datetimecolumn-resource-type"></a>Tipo de recurso DateTimeColumn

El recurso **dateTimeColumn** en un recurso [columnDefinition](columndefinition.md) indica que los valores de la columna son fechas u horas.

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

| Nombre de la propiedad      | Tipo               | Descripción
|:-------------------|:-------------------|:----------------------------------------------
| **displayAs**      | string             | Cómo se debe presentar el valor en la experiencia de usuario. Debe ser `default`, `friendly` o `standard`. Vea lo que se muestra a continuación para obtener más detalles. Si no se especifica, se trata como `default`.
| **format**         | string             | Indica si el valor debe presentarse solo como una fecha o como fecha y hora. Debe ser `dateOnly` o `dateTime`

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
