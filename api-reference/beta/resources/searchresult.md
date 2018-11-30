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
# <a name="searchresult-resource-type"></a><span data-ttu-id="ce73d-102">Tipo de recurso SearchResult</span><span class="sxs-lookup"><span data-stu-id="ce73d-102">SearchResult resource type</span></span>

> <span data-ttu-id="ce73d-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ce73d-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ce73d-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ce73d-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ce73d-105">El recurso **SearchResult** indica que un elemento es la respuesta a una consulta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ce73d-105">The **SearchResult** resource indicates than an item is the response to a search query.</span></span>

## <a name="json-representation"></a><span data-ttu-id="ce73d-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ce73d-106">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="ce73d-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ce73d-107">Properties</span></span>

| <span data-ttu-id="ce73d-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ce73d-108">Property</span></span>            | <span data-ttu-id="ce73d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="ce73d-109">Type</span></span>   | <span data-ttu-id="ce73d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce73d-110">Description</span></span>
|:--------------------|:-------|:----------------------------------------------
| <span data-ttu-id="ce73d-111">onClickTelemetryUrl</span><span class="sxs-lookup"><span data-stu-id="ce73d-111">onClickTelemetryUrl</span></span> | <span data-ttu-id="ce73d-112">String</span><span class="sxs-lookup"><span data-stu-id="ce73d-112">String</span></span> | <span data-ttu-id="ce73d-p102">Dirección URL de devolución de llamada que se puede usar para registrar información de telemetría. La aplicación debe emitir un GET en esta dirección URL si el usuario interactúa con este elemento para mejorar la calidad de los resultados.</span><span class="sxs-lookup"><span data-stu-id="ce73d-p102">A callback URL that can be used to record telemetry information. The application should issue a GET on this URL if the user interacts with this item to improve the quality of results.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce73d-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ce73d-115">Remarks</span></span> 

<span data-ttu-id="ce73d-116">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="ce73d-116">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The search result facet indicates an item is from a search.",
  "keywords": "search result facet",
  "section": "documentation",
  "tocPath": "Facets/SearchResult"
} -->
