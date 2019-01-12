---
title: tipo de recurso callRoute
description: El tipo de callRoute.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: fd131afcdb5581a719107d9fd3a9a597979d6f21
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27933074"
---
# <a name="callroute-resource-type"></a><span data-ttu-id="7355e-103">tipo de recurso callRoute</span><span class="sxs-lookup"><span data-stu-id="7355e-103">callRoute resource type</span></span>

> <span data-ttu-id="7355e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7355e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7355e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7355e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7355e-106">El tipo de callRoute.</span><span class="sxs-lookup"><span data-stu-id="7355e-106">The callRoute type.</span></span>

## <a name="properties"></a><span data-ttu-id="7355e-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7355e-107">Properties</span></span>

| <span data-ttu-id="7355e-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7355e-108">Property</span></span>            | <span data-ttu-id="7355e-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="7355e-109">Type</span></span>                          | <span data-ttu-id="7355e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="7355e-110">Description</span></span>                                                  |
| :------------------ | :---------------------------- | :----------------------------------------------------------- |
| <span data-ttu-id="7355e-111">final</span><span class="sxs-lookup"><span data-stu-id="7355e-111">final</span></span>               | [<span data-ttu-id="7355e-112">identitySet</span><span class="sxs-lookup"><span data-stu-id="7355e-112">identitySet</span></span>](identityset.md) | <span data-ttu-id="7355e-113">La identidad que se ha resuelta para en la llamada.</span><span class="sxs-lookup"><span data-stu-id="7355e-113">The identity that was resolved to in the call.</span></span>               |
| <span data-ttu-id="7355e-114">Texto original en</span><span class="sxs-lookup"><span data-stu-id="7355e-114">original</span></span>            | [<span data-ttu-id="7355e-115">identitySet</span><span class="sxs-lookup"><span data-stu-id="7355e-115">identitySet</span></span>](identityset.md) | <span data-ttu-id="7355e-116">La identidad que se usó originalmente en la llamada.</span><span class="sxs-lookup"><span data-stu-id="7355e-116">The identity that was originally used in the call.</span></span>           |
| <span data-ttu-id="7355e-117">routingType</span><span class="sxs-lookup"><span data-stu-id="7355e-117">routingType</span></span>         | <span data-ttu-id="7355e-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="7355e-118">String</span></span>                        | <span data-ttu-id="7355e-119">Los valores posibles son: `forwarded`, `lookup` y `selfFork`.</span><span class="sxs-lookup"><span data-stu-id="7355e-119">Possible values are: `forwarded`, `lookup`, `selfFork`.</span></span>  |

## <a name="json-representation"></a><span data-ttu-id="7355e-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7355e-120">JSON representation</span></span>

<span data-ttu-id="7355e-121">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="7355e-121">The following is a JSON representation of the resource.</span></span>

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
