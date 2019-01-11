---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: TextColumn
localization_priority: Normal
ms.openlocfilehash: 87a5e27544a49613d1d1e44cd6f3e0e3b7fcf8c4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27822571"
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
