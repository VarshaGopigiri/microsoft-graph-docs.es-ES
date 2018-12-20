---
title: tipo de recurso callRoute
description: El tipo de callRoute.
author: VinodRavichandran
ms.openlocfilehash: 9538fb8f27f60e869c19edc7bd19d7f6b29e8fff
ms.sourcegitcommit: 0b3a57ac8b99871e56389f9be15e4f96e219f635
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2018
ms.locfileid: "27380159"
---
# <a name="callroute-resource-type"></a><span data-ttu-id="d6e37-103">tipo de recurso callRoute</span><span class="sxs-lookup"><span data-stu-id="d6e37-103">callRoute resource type</span></span>

> <span data-ttu-id="d6e37-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d6e37-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d6e37-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d6e37-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d6e37-106">El tipo de callRoute.</span><span class="sxs-lookup"><span data-stu-id="d6e37-106">The callRoute type.</span></span>

## <a name="properties"></a><span data-ttu-id="d6e37-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d6e37-107">Properties</span></span>

| <span data-ttu-id="d6e37-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d6e37-108">Property</span></span>            | <span data-ttu-id="d6e37-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6e37-109">Type</span></span>                          | <span data-ttu-id="d6e37-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6e37-110">Description</span></span>                                                  |
| :------------------ | :---------------------------- | :----------------------------------------------------------- |
| <span data-ttu-id="d6e37-111">final</span><span class="sxs-lookup"><span data-stu-id="d6e37-111">final</span></span>               | [<span data-ttu-id="d6e37-112">identitySet</span><span class="sxs-lookup"><span data-stu-id="d6e37-112">identitySet</span></span>](identityset.md) | <span data-ttu-id="d6e37-113">La identidad que se ha resuelta para en la llamada.</span><span class="sxs-lookup"><span data-stu-id="d6e37-113">The identity that was resolved to in the call.</span></span>               |
| <span data-ttu-id="d6e37-114">Texto original en</span><span class="sxs-lookup"><span data-stu-id="d6e37-114">original</span></span>            | [<span data-ttu-id="d6e37-115">identitySet</span><span class="sxs-lookup"><span data-stu-id="d6e37-115">identitySet</span></span>](identityset.md) | <span data-ttu-id="d6e37-116">La identidad que se usó originalmente en la llamada.</span><span class="sxs-lookup"><span data-stu-id="d6e37-116">The identity that was originally used in the call.</span></span>           |
| <span data-ttu-id="d6e37-117">routingType</span><span class="sxs-lookup"><span data-stu-id="d6e37-117">routingType</span></span>         | <span data-ttu-id="d6e37-118">String</span><span class="sxs-lookup"><span data-stu-id="d6e37-118">String</span></span>                        | <span data-ttu-id="d6e37-119">Los valores posibles son: `forwarded`, `lookup` y `selfFork`.</span><span class="sxs-lookup"><span data-stu-id="d6e37-119">Possible values are: `forwarded`, `lookup`, `selfFork`.</span></span>  |

## <a name="json-representation"></a><span data-ttu-id="d6e37-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d6e37-120">JSON representation</span></span>

<span data-ttu-id="d6e37-121">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d6e37-121">The following is a JSON representation of the resource.</span></span>

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
