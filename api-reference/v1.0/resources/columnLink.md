---
author: daspek
ms.author: dspektor
ms.date: 09/12/2017
title: ColumnLink
ms.openlocfilehash: cdae360afb6e626ee481a7e98ed5f90e657203b2
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23265123"
---
# <a name="columnlink-resource-type"></a>Tipo de recurso ColumnLink

Un recurso **columnLink** en un recurso [contentType][] adjunta el recurso **columnDefinition** de un sitio a ese tipo de contenido.

[contentType]: contentType.md

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

| Nombre de propiedad | Tipo   | Descripción
|:--------------|:-------|:----------------------------------------------------
| **id**        | cadena | El identificador único de la columna.
| **name**      | string | El nombre de la columna de este tipo de contenido.

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/ColumnLink"
} -->
