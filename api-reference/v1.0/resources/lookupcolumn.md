---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: LookupColumn
localization_priority: Normal
ms.openlocfilehash: 41e643019d842a365c333efa3c3a6861c51a7fc7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27892103"
---
# <a name="lookupcolumn-resource-type"></a>Tipo de recurso LookupColumn

El recurso **lookupColumn** en un recurso [columnDefinition](columndefinition.md) indica que los valores de la columna se buscan desde otro origen en el sitio.

## <a name="json-representation"></a>Representación JSON

A continuación se incluye una representación JSON de un recurso **LookupColumn**.
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.lookupColumn" } -->

```json
{
  "allowMultipleValues": true,
  "allowUnlimitedLength": false,
  "columnName": "string",
  "listId": "string",
  "primaryLookupColumnId": "string"
}
```

## <a name="properties"></a>Propiedades

| Nombre de la propiedad             | Tipo    | Descripción
|:--------------------------|:--------|:---------------------------------------
| **allowMultipleValues**   | boolean | Indica si se pueden seleccionar varios valores desde el origen.
| **allowUnlimitedLength**  | boolean | Indica si los valores de la columna deben poder superar el límite estándar de 255 caracteres.
| **columnName**            | string  | El nombre de la columna de origen de búsqueda.
| **listId**                | string  | El identificador único de la lista de origen de búsqueda.
| **primaryLookupColumnId** | string  | Si se especifica, esta columna es una *búsqueda secundaria*, que extrae un campo adicional del elemento de lista devuelto por la *búsqueda principal*. Use el elemento de lista buscado en la búsqueda *principal* como origen de la columna indicada aquí.

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/LookupColumn"
} -->
