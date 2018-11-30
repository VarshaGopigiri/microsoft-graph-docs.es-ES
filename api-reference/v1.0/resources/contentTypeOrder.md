---
author: daspek
ms.author: dspektor
ms.date: 09/13/2017
title: ContentTypeOrder
ms.openlocfilehash: 8cb47837d8df1c38ed25fc87d3b4d7da450fed1a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028804"
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
