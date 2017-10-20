---
author: daspek
ms.author: dspektor
ms.date: 09/13/2017
title: ContentTypeOrder
ms.openlocfilehash: fe7309373ded16fe2660e0c5a69773c18ffb581a
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
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
