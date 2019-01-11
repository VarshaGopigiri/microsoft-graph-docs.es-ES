---
title: tipo de recurso callRoute
description: El tipo de callRoute.
author: VinodRavichandran
localization_priority: Normal
ms.openlocfilehash: e417a7e814b5a2a80da1fa9cd7a551f82e0c37db
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27815088"
---
# <a name="callroute-resource-type"></a><span data-ttu-id="68b93-103">tipo de recurso callRoute</span><span class="sxs-lookup"><span data-stu-id="68b93-103">callRoute resource type</span></span>

> <span data-ttu-id="68b93-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="68b93-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="68b93-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="68b93-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="68b93-106">El tipo de callRoute.</span><span class="sxs-lookup"><span data-stu-id="68b93-106">The callRoute type.</span></span>

## <a name="properties"></a><span data-ttu-id="68b93-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="68b93-107">Properties</span></span>

| <span data-ttu-id="68b93-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="68b93-108">Property</span></span>            | <span data-ttu-id="68b93-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="68b93-109">Type</span></span>                          | <span data-ttu-id="68b93-110">Description</span><span class="sxs-lookup"><span data-stu-id="68b93-110">Description</span></span>                                                  |
| :------------------ | :---------------------------- | :----------------------------------------------------------- |
| <span data-ttu-id="68b93-111">final</span><span class="sxs-lookup"><span data-stu-id="68b93-111">final</span></span>               | [<span data-ttu-id="68b93-112">identitySet</span><span class="sxs-lookup"><span data-stu-id="68b93-112">identitySet</span></span>](identityset.md) | <span data-ttu-id="68b93-113">La identidad que se ha resuelta para en la llamada.</span><span class="sxs-lookup"><span data-stu-id="68b93-113">The identity that was resolved to in the call.</span></span>               |
| <span data-ttu-id="68b93-114">Texto original en</span><span class="sxs-lookup"><span data-stu-id="68b93-114">original</span></span>            | [<span data-ttu-id="68b93-115">identitySet</span><span class="sxs-lookup"><span data-stu-id="68b93-115">identitySet</span></span>](identityset.md) | <span data-ttu-id="68b93-116">La identidad que se usó originalmente en la llamada.</span><span class="sxs-lookup"><span data-stu-id="68b93-116">The identity that was originally used in the call.</span></span>           |
| <span data-ttu-id="68b93-117">routingType</span><span class="sxs-lookup"><span data-stu-id="68b93-117">routingType</span></span>         | <span data-ttu-id="68b93-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="68b93-118">String</span></span>                        | <span data-ttu-id="68b93-119">Los valores posibles son: `forwarded`, `lookup` y `selfFork`.</span><span class="sxs-lookup"><span data-stu-id="68b93-119">Possible values are: `forwarded`, `lookup`, `selfFork`.</span></span>  |

## <a name="json-representation"></a><span data-ttu-id="68b93-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="68b93-120">JSON representation</span></span>

<span data-ttu-id="68b93-121">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="68b93-121">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.callRoute"
}-->
```json
{
  "final": {"@odata.type": "#microsoft.graph.identitySet"},
  "original": {"@odata.type": "#microsoft.graph.identitySet"},
  "routingType": "forwarded | lookup | selfFork"
}
```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "callRoute resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
