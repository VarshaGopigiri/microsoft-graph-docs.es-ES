---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: TextColumn
localization_priority: Normal
ms.openlocfilehash: d064253cfad141d5879afb52451ca28fa2aeca67
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27860882"
---
# <a name="textcolumn-resource-type"></a>Tipo de recurso TextColumn

El recurso **TextColumn** en un recurso [columnDefinition](columndefinition.md) indica que los valores de la columna son texto.

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

| Nombre de la propiedad                   | Tipo    | Descripción
|:--------------------------------|:--------|:---------------------------------
| **allowMultipleLines**          | boolean | Si se permiten varias líneas de texto.
| **appendChangesToExistingText** | boolean | Si las actualizaciones de esta columna deben reemplazar el texto existente o anexarse a este.
| **linesForEditing**             | int32   | El tamaño del cuadro de texto.
| **maxLength**                   | int32   | El número máximo de caracteres del valor.
| **textType**                    | string  | El tipo de texto que se almacena. Debe ser `plain` o `richText`

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
