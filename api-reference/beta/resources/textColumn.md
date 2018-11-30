---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: TextColumn
ms.openlocfilehash: 5ff280b6c969d9832e2f81f77dc32237f9905aad
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086638"
---
# <a name="textcolumn-resource-type"></a>Tipo de recurso TextColumn

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

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

| Nombre de propiedad                   | Tipo   | Descripción
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
