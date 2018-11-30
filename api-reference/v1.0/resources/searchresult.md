---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: SearchResult
ms.openlocfilehash: 120f1805196e40d652bd2fcd409f4ee3cd3203fa
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029624"
---
# <a name="searchresult-resource-type"></a><span data-ttu-id="2c9db-102">Tipo de recurso SearchResult</span><span class="sxs-lookup"><span data-stu-id="2c9db-102">SearchResult resource type</span></span>

<span data-ttu-id="2c9db-103">El recurso **SearchResult** indica que un elemento es la respuesta a una consulta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="2c9db-103">The **SearchResult** resource indicates than an item is the response to a search query.</span></span>

## <a name="json-representation"></a><span data-ttu-id="2c9db-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2c9db-104">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="2c9db-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2c9db-105">Properties</span></span>

| <span data-ttu-id="2c9db-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2c9db-106">Property</span></span>            | <span data-ttu-id="2c9db-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="2c9db-107">Type</span></span>   | <span data-ttu-id="2c9db-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c9db-108">Description</span></span>
|:--------------------|:-------|:----------------------------------------------
| <span data-ttu-id="2c9db-109">onClickTelemetryUrl</span><span class="sxs-lookup"><span data-stu-id="2c9db-109">onClickTelemetryUrl</span></span> | <span data-ttu-id="2c9db-110">String</span><span class="sxs-lookup"><span data-stu-id="2c9db-110">String</span></span> | <span data-ttu-id="2c9db-p101">Dirección URL de devolución de llamada que se puede usar para registrar información de telemetría. La aplicación debe emitir un GET en esta dirección URL si el usuario interactúa con este elemento para mejorar la calidad de los resultados.</span><span class="sxs-lookup"><span data-stu-id="2c9db-p101">A callback URL that can be used to record telemetry information. The application should issue a GET on this URL if the user interacts with this item to improve the quality of results.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c9db-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2c9db-113">Remarks</span></span> 

<span data-ttu-id="2c9db-114">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="2c9db-114">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The search result facet indicates an item is from a search.",
  "keywords": "search result facet",
  "section": "documentation",
  "tocPath": "Facets/SearchResult"
} -->
