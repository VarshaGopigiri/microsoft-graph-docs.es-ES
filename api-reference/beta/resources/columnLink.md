---
author: daspek
ms.author: dspektor
ms.date: 09/12/2017
title: ColumnLink
ms.openlocfilehash: edb8d97094b4d26dbbcc008664bf5dfee3a4ddf9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084477"
---
# <a name="columnlink-resource-type"></a>Tipo de recurso ColumnLink

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Un recurso **columnLink** en un recurso [contentType][] adjunta el recurso **columnDefinition** de un sitio a ese tipo de contenido.

[contentType]: contenttype.md

## <a name="json-representation"></a>Representación JSON

A continuación se incluye una representación JSON de un recurso **columnLink**.
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.columnLink" } -->

```json
{
  "id": "string",
  "name": "string"
}
```

## <a name="properties"></a>Propiedades

| Nombre de propiedad | Tipo   | Descripción
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
