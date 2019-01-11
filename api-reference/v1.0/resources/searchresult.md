---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: SearchResult
localization_priority: Normal
ms.openlocfilehash: 5e8bcbc18975758586b012ee32fb32ce15313517
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27876604"
---
# <a name="searchresult-resource-type"></a>Tipo de recurso SearchResult

El recurso **SearchResult** indica que un elemento es la respuesta a una consulta de búsqueda.

## <a name="json-representation"></a>Representación JSON

<!-- {
  "blockType": "resource",
  "optionalProperties": [ "onClickTelemtryUrl" ],
  "@odata.type": "microsoft.graph.searchResult"
}-->

```json
{
  "onClickTelemetryUrl": "url"
}
```

## <a name="properties"></a>Propiedades

| Propiedad            | Tipo   | Descripción
|:--------------------|:-------|:----------------------------------------------
| onClickTelemetryUrl | String | Dirección URL de devolución de llamada que se puede usar para registrar información de telemetría. La aplicación debe emitir un GET en esta dirección URL si el usuario interactúa con este elemento para mejorar la calidad de los resultados.

## <a name="remarks"></a>Comentarios 

Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).

<!-- {
  "type": "#page.annotation",
  "description": "The search result facet indicates an item is from a search.",
  "keywords": "search result facet",
  "section": "documentation",
  "tocPath": "Facets/SearchResult"
} -->
