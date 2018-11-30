---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: SearchResult
ms.openlocfilehash: 7e6bd6e6ff48ae34e197955d16a3df1d539a3c05
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088467"
---
# <a name="searchresult-resource-type"></a>Tipo de recurso SearchResult

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

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
