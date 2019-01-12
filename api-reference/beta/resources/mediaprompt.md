---
title: tipo de recurso mediaPrompt
description: El tipo de mediaPrompt.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 1ff6150ef453f421a7a68c468abc123373f20891
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27965463"
---
# <a name="mediaprompt-resource-type"></a><span data-ttu-id="35503-103">tipo de recurso mediaPrompt</span><span class="sxs-lookup"><span data-stu-id="35503-103">mediaPrompt resource type</span></span>

> <span data-ttu-id="35503-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="35503-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="35503-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="35503-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="35503-106">El tipo de mediaPrompt.</span><span class="sxs-lookup"><span data-stu-id="35503-106">The mediaPrompt type.</span></span>

## <a name="properties"></a><span data-ttu-id="35503-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="35503-107">Properties</span></span>

| <span data-ttu-id="35503-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="35503-108">Property</span></span>    | <span data-ttu-id="35503-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="35503-109">Type</span></span>                      | <span data-ttu-id="35503-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="35503-110">Description</span></span>                                                                     |
| :---------- | :------------------------ | :------------------------------------------------------------------------------ |
| <span data-ttu-id="35503-111">bucle</span><span class="sxs-lookup"><span data-stu-id="35503-111">loop</span></span>        | <span data-ttu-id="35503-112">Int32</span><span class="sxs-lookup"><span data-stu-id="35503-112">Int32</span></span>                     | <span data-ttu-id="35503-113">El recuento del bucle.</span><span class="sxs-lookup"><span data-stu-id="35503-113">The loop count.</span></span> <span data-ttu-id="35503-114">el valor 0 indica que el bucle indefinido.</span><span class="sxs-lookup"><span data-stu-id="35503-114">0 value indicates to loop infinitely.</span></span> <span data-ttu-id="35503-115">El valor predeterminado es `1`.</span><span class="sxs-lookup"><span data-stu-id="35503-115">The default value is `1`.</span></span> |
| <span data-ttu-id="35503-116">mediaInfo</span><span class="sxs-lookup"><span data-stu-id="35503-116">mediaInfo</span></span>   | [<span data-ttu-id="35503-117">mediaInfo</span><span class="sxs-lookup"><span data-stu-id="35503-117">mediaInfo</span></span>](mediainfo.md) | <span data-ttu-id="35503-118">La información de medios</span><span class="sxs-lookup"><span data-stu-id="35503-118">The media information</span></span>                                                           |

## <a name="json-representation"></a><span data-ttu-id="35503-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="35503-119">JSON representation</span></span>

<span data-ttu-id="35503-120">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="35503-120">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.mediaPrompt"
}-->

```json
{
  "loop": 1024,
  "mediaInfo": { "@odata.type": "#microsoft.graph.mediaInfo" }
}
```

## <a name="example"></a><span data-ttu-id="35503-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="35503-121">Example</span></span>

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.mediaPrompt"
}-->
```json
{
  "mediaInfo": {
    "uri": "https://cdn.contoso.com/beep.wav",
    "resourceId": "1D6DE2D4-CD51-4309-8DAA-70768651088E"
  },
  "loop": 5
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mediaPrompt resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
