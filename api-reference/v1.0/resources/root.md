---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: "Raíz"
ms.openlocfilehash: 36d283792e25d5718b66190a5289ae4a7ff3d992
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="root-resource-type"></a>Tipo de recurso Root

La faceta **Root** indica que un objeto es el primero de su jerarquía.
La presencia (valor no NULL) del valor de la faceta indica que el objeto es la raíz.
Un valor NULL (o ausente) indica que el objeto no es la raíz.

**Nota**: Aunque actualmente esta faceta está vacía, en futuras revisiones de la API, la faceta puede rellenarse con propiedades adicionales.

## <a name="json-representation"></a>Representación JSON

<!-- { "blockType": "resource", "@type": "microsoft.graph.root" } -->

```json
{
}
```

## <a name="properties"></a>Propiedades

El recurso **Root** no tiene propiedades.


<!-- {
  "type": "#page.annotation",
  "section": "documentation",
  "tocPath": "Facets/Root"
} -->
