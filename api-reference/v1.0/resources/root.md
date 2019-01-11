---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Raíz
localization_priority: Normal
ms.openlocfilehash: 4753174531517bd1b194c3023efbc31785695f5b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27862051"
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
