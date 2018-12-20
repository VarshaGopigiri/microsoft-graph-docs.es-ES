---
title: tipo de recurso serviceHostedMediaConfig
description: El tipo de serviceHostedMediaConfig.
author: VinodRavichandran
ms.openlocfilehash: 544c1d3bce934064092e0f9c74b888686e49d426
ms.sourcegitcommit: 0b3a57ac8b99871e56389f9be15e4f96e219f635
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2018
ms.locfileid: "27380320"
---
# <a name="servicehostedmediaconfig-resource-type"></a><span data-ttu-id="d0d36-103">tipo de recurso serviceHostedMediaConfig</span><span class="sxs-lookup"><span data-stu-id="d0d36-103">serviceHostedMediaConfig resource type</span></span>

> <span data-ttu-id="d0d36-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d0d36-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d0d36-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d0d36-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d0d36-106">El tipo de serviceHostedMediaConfig.</span><span class="sxs-lookup"><span data-stu-id="d0d36-106">The serviceHostedMediaConfig type.</span></span>

## <a name="properties"></a><span data-ttu-id="d0d36-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d0d36-107">Properties</span></span>

| <span data-ttu-id="d0d36-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d0d36-108">Property</span></span>                    | <span data-ttu-id="d0d36-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="d0d36-109">Type</span></span>                                                        | <span data-ttu-id="d0d36-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0d36-110">Description</span></span>                                       |
| :-------------------------- | :---------------------------------------------------------- | :-------------------------------------------------|
| <span data-ttu-id="d0d36-111">preFetchMedia</span><span class="sxs-lookup"><span data-stu-id="d0d36-111">preFetchMedia</span></span>               | <span data-ttu-id="d0d36-112">colección de [mediaInfo](mediainfo.md)</span><span class="sxs-lookup"><span data-stu-id="d0d36-112">[mediaInfo](mediainfo.md) collection</span></span>                        | <span data-ttu-id="d0d36-113">La lista de medios para recuperar previamente.</span><span class="sxs-lookup"><span data-stu-id="d0d36-113">The list of media to pre-fetch.</span></span>                   |
| <span data-ttu-id="d0d36-114">removeFromDefaultAudioGroup</span><span class="sxs-lookup"><span data-stu-id="d0d36-114">removeFromDefaultAudioGroup</span></span> | <span data-ttu-id="d0d36-115">Booleano</span><span class="sxs-lookup"><span data-stu-id="d0d36-115">Boolean</span></span>                                                     | <span data-ttu-id="d0d36-116">Quitar a participante automática de grupo de audio predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d0d36-116">Remove self participant from default audio group.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="d0d36-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d0d36-117">JSON representation</span></span>

<span data-ttu-id="d0d36-118">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d0d36-118">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "preFetchMedia"
  ],
  "@odata.type": "microsoft.graph.serviceHostedMediaConfig"
}-->
```json
{
  "preFetchMedia": [ { "@odata.type": "#microsoft.graph.mediaInfo" } ],
  "removeFromDefaultAudioGroup": true
}
```

## <a name="example"></a><span data-ttu-id="d0d36-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d0d36-119">Example</span></span>

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.serviceHostedMediaConfig"
}-->
```json
{
  "preFetchMedia": [
    {
      "uri": "https://cdn.contoso.com/beep.wav",
      "resourceId": "1D6DE2D4-CD51-4309-8DAA-70768651088E"
    },
    {
      "uri": "https://cdn.contoso.com/cool.wav",
      "resourceId": "1D6DE2D4-CD51-4309-8DAA-70768651088F"
    }
  ],
  "removeFromDefaultAudioGroup": false
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "serviceHostedMediaConfig resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
