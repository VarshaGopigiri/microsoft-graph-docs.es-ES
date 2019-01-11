---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Miniatura
localization_priority: Normal
ms.openlocfilehash: 9c972842515de15b726d4496f915806ca5298313
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27839616"
---
# <a name="thumbnail-resource-type"></a>Tipo de recurso thumbnail

El tipo de recurso **thumbnail** representa una miniatura de una imagen, un vídeo, un documento o cualquier elemento que tenga una representación en mapa de bits.

## <a name="json-representation"></a>Representación JSON

A continuación se incluye una representación JSON del recurso **thumbnail**.

<!--{
  "blockType": "resource",
  "optionalProperties": [
    "content",
    "height",
    "width",
    "sourceItemId"
  ],
  "@odata.type": "microsoft.graph.thumbnail"
}-->

```json
{
  "height": 1024,
  "sourceItemId": "string",
  "url": "string",
  "width": 1024,
  "content": "stream"
}
```

## <a name="properties"></a>Propiedades

| Propiedad     | Tipo   | Descripción
| :----------- | :----- | :----------------------------------------------------
| height       | Int32  | Alto de la miniatura en píxeles.
| sourceItemId | String | Identificador único del elemento que proporciona la vista en miniatura. Solo está disponible cuando se solicita la miniatura de una carpeta.
| url          | String | Dirección URL usada para recuperar el contenido de la miniatura.
| width        | Int32  | Ancho de la miniatura en píxeles.
| content      | Secuencia | La secuencia de contenido de la miniatura.

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Thumbnail resource represents a single thumbnail for an item.",
  "section": "documentation",
  "tocPath": "Resources/Thumbnail"
} -->
