---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Cuota
localization_priority: Normal
ms.openlocfilehash: 58969adb525736b8a665844a5fa4b48ae4ca1831
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27848415"
---
# <a name="quota-resource-type"></a>Tipo de recurso Quota

El recurso **quota** proporciona detalles sobre las limitaciones de espacio en un recurso [Drive](drive.md).

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "@odata.type": "microsoft.graph.quota"
}-->

```json
{
  "deleted": 1024,
  "remaining": 1024,
  "state": "normal | nearing | critical | exceeded",
  "total": 1024,
  "used": 1024
}
```

## <a name="properties"></a>Propiedades

| Nombre de la propiedad | Tipo   | Descripción                                                                 |
|:--------------|:-------|:----------------------------------------------------------------------------|
| total         | Int64  | Espacio total de almacenamiento permitido, en bytes. Solo lectura.                           |
| used          | Int64  | Espacio total usado, en bytes. Solo lectura.                                      |
| remaining     | Int64  | Espacio total restante antes de alcanzar el límite de cuota, en bytes. Solo lectura. |
| deleted       | Int64  | Espacio total consumido por los archivos de la Papelera de reciclaje, en bytes. Solo lectura.      |
| estado         | string | Valor de enumeración que indica el estado del espacio de almacenamiento. Solo lectura. |

## <a name="state-enumeration"></a>Enumeración de estado

| Valor      | Descripción                                                                                                                                                                 |
|:-----------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `normal`   | A la unidad le queda mucha cuota restante.                                                                                                                               |
| `nearing`  | La cuota restante es inferior al 10 % del espacio total de cuota.                                                                                                                      |
| `critical` | La cuota restante es inferior al 1 % del espacio total de cuota.                                                                                                                       |
| `exceeded` | La cuota usada ha superado la cuota total. No se pueden agregar nuevos archivos ni carpetas en la unidad hasta que esté por debajo de la cantidad total de cuota o se adquiera más espacio de almacenamiento. |

<!-- {
  "type": "#page.annotation",
  "description": "The quota facet provides information about how much space the OneDrive has available.",
  "keywords": "quota,available,remaining,used",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/resources/quota.md:
      Found potential enums in resource example that weren't defined in a table:(normal, nearing,critical,exceeded) are in resource, but () are in table"
  ],
  "tocPath": "Facets/Quota"
} -->
