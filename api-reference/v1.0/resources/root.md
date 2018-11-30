---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Raíz
ms.openlocfilehash: 23e81891956ea656c0f31920318f249916d3defa
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031503"
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
