---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: TextColumn
ms.openlocfilehash: b5c41091b9193aabc36ee04e9dcc310bfc110af1
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23264290"
---
# <a name="textcolumn-resource-type"></a>Tipo de recurso TextColumn

El recurso **TextColumn** en un recurso [columnDefinition](columnDefinition.md) indica que los valores de la columna son texto.

## <a name="json-representation"></a>Representación JSON

A continuación se incluye una representación JSON de un recurso **TextColumn**.
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.textColumn" } -->

```json
{
  "allowMultipleLines": true,
  "appendChangesToExistingText": false,
  "linesForEditing": 6,
  "maxLength": 300,
  "textType": "plain | richText"
}
```

## <a name="properties"></a>Propiedades

| Nombre de propiedad                   | Tipo    | Descripción
|:--------------------------------|:--------|:---------------------------------
| **allowMultipleLines**          | booleano | Si se permiten varias líneas de texto.
| **appendChangesToExistingText** | booleano | Si las actualizaciones de esta columna deben reemplazar el texto existente o anexarse a este.
| **linesForEditing**             | int32   | El tamaño del cuadro de texto.
| **maxLength**                   | int32   | El número máximo de caracteres del valor.
| **textType**                    | cadena  | El tipo de texto que se almacena. Debe ser `plain` o `richText`

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/resources/textcolumn.md:
      Found potential enums in resource example that weren't defined in a table:(plain,richText) are in resource, but () are in table"
  ],
  "tocPath": "Resources/TextColumn"
} -->
