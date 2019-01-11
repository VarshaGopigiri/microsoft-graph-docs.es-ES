---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Raíz
localization_priority: Normal
ms.openlocfilehash: 017a4571288839d8d92f182a3a1a44023c4737e2
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27866139"
---
# <a name="root-resource-type"></a>Tipo de recurso Root

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

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
