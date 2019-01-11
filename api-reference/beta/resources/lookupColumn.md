---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: LookupColumn
localization_priority: Normal
ms.openlocfilehash: 1c7ab364777e1e3f82bb78d8e0940cf4f85576a0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27885711"
---
# <a name="lookupcolumn-resource-type"></a>Tipo de recurso LookupColumn

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

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
