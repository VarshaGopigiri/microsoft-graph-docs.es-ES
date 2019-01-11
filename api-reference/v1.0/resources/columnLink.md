---
author: daspek
ms.author: dspektor
ms.date: 09/12/2017
title: ColumnLink
localization_priority: Normal
ms.openlocfilehash: 435696cc596f73830104ea8ec0619bf40a462d62
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27834534"
---
# <a name="columnlink-resource-type"></a>Tipo de recurso ColumnLink

Un recurso **columnLink** en un recurso [contentType][] adjunta el recurso **columnDefinition** de un sitio a ese tipo de contenido.

[contentType]: contenttype.md

## <a name="json-representation"></a>Representación JSON

A continuación se incluye una representación JSON de un recurso **columnLink**.
<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.columnLink" } -->

```json
{
  "id": "string",
  "name": "string"
}
```

## <a name="properties"></a>Propiedades

| Nombre de la propiedad | Tipo   | Descripción
|:--------------|:-------|:----------------------------------------------------
| **id**        | string | El identificador único de la columna.
| **name**      | string | El nombre de la columna de este tipo de contenido.

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/ColumnLink"
} -->
