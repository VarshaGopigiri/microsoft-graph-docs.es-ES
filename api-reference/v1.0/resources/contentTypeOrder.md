---
author: daspek
ms.author: dspektor
ms.date: 09/13/2017
title: ContentTypeOrder
localization_priority: Normal
ms.openlocfilehash: ccea5804c3f4eddb02b5d4163302362f29b5fbc8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27890499"
---
# <a name="contenttypeorder-resource-type"></a>Tipo de recurso ContentTypeOrder

El recurso **contentTypeOrder** especifica el orden en el que aparecerá el tipo de contenido en la interfaz de usuario de selección.

## <a name="json-representation"></a>Representación JSON

A continuación se incluye una representación JSON de un recurso **contentTypeOrder**.
<!-- { "blockType": "resource", "@type": "microsoft.graph.contentTypeOrder", "@type.aka": "oneDrive.contentTypeOrderFacet" } -->

```json
{
  "default": true,
  "position": 2
}
```

## <a name="properties"></a>Propiedades

| Nombre de la propiedad | Tipo    | Descripción
|:--------------|:--------|:----------------------------------------------------
| **default**   | boolean | Si este es el tipo de contenido predeterminado
| **position**  | Int32   | Especifica la posición en la que aparece el tipo de contenido en la interfaz de usuario de selección.

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/ContentTypeOrder"
} -->
