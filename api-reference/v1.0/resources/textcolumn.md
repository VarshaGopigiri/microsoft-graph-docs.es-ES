---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: TextColumn
ms.openlocfilehash: 80e41b379b9b4ce51a3ee6c910447a22f43356c3
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
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

| Nombre de la propiedad                   | Tipo   | Descripción
|:--------------------------------|:-------|:-----------------------------------------------
| **allowMultipleLines**          | string | Si se permiten varias líneas de texto.
| **appendChangesToExistingText** | string | Si las actualizaciones de esta columna deben reemplazar el texto existente o anexarse a este.
| **linesForEditing**             | int    | El tamaño del cuadro de texto.
| **maxLength**                   | int    | El número máximo de caracteres del valor.
| **textType**                    | string | El tipo de texto que se almacena. Debe ser `plain` o `richText`

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/TextColumn"
} -->
