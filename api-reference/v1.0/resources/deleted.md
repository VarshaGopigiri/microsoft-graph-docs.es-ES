---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Eliminados
ms.openlocfilehash: 1d45219b2ef26bdc96c46e386d66d91874f9bc0b
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="deleted-facet"></a>Faceta Deleted

El recurso **Deleted** indica que el elemento se ha eliminado.
En esta versión de la API, la presencia (no null) del valor de recurso indica que el archivo se eliminó.
Un valor null (o ausente) indica que el archivo no se elimina.

Consulte el artículo sobre cómo [ver los cambios de un elemento](../api/driveitem_delta.md) para obtener más información sobre el seguimiento de los cambios y la búsqueda de elementos eliminados.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
  "state"
  ],
  "@odata.type": "microsoft.graph.deleted"
}-->
```json
{
  "state": "string"
}
```
## <a name="properties"></a>Propiedades

| Propiedad | Tipo   | Descripción                               |
|:---------|:-------|:------------------------------------------|
| state    | String | Representa el estado del elemento eliminado. |

## <a name="remarks"></a>Comentarios 

Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).

<!-- {
  "type": "#page.annotation",
  "description": "The deleted facet providers properties about deleted items",
  "keywords": "deleted,delete,item,facet",
  "section": "documentation",
  "tocPath": "Facets/Deleted"
} -->
