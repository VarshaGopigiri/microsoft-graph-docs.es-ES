---
title: tipo de recurso mediaPrompt
description: El tipo de mediaPrompt.
ms.openlocfilehash: 1a782d391110d35b07b551e44ebd3b931dbcadba
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089246"
---
# <a name="mediaprompt-resource-type"></a><span data-ttu-id="78345-103">tipo de recurso mediaPrompt</span><span class="sxs-lookup"><span data-stu-id="78345-103">mediaPrompt resource type</span></span>

> <span data-ttu-id="78345-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="78345-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="78345-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="78345-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="78345-106">El tipo de mediaPrompt.</span><span class="sxs-lookup"><span data-stu-id="78345-106">The mediaPrompt type.</span></span>

## <a name="properties"></a><span data-ttu-id="78345-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="78345-107">Properties</span></span>

| <span data-ttu-id="78345-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="78345-108">Property</span></span>    | <span data-ttu-id="78345-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="78345-109">Type</span></span>                      | <span data-ttu-id="78345-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="78345-110">Description</span></span>                                                                     |
| :---------- | :------------------------ | :------------------------------------------------------------------------------ |
| <span data-ttu-id="78345-111">bucle</span><span class="sxs-lookup"><span data-stu-id="78345-111">loop</span></span>        | <span data-ttu-id="78345-112">Int32</span><span class="sxs-lookup"><span data-stu-id="78345-112">Int32</span></span>                     | <span data-ttu-id="78345-113">El recuento del bucle.</span><span class="sxs-lookup"><span data-stu-id="78345-113">The loop count.</span></span> <span data-ttu-id="78345-114">el valor 0 indica que el bucle indefinido.</span><span class="sxs-lookup"><span data-stu-id="78345-114">0 value indicates to loop infinitely.</span></span> <span data-ttu-id="78345-115">El valor predeterminado es `1`.</span><span class="sxs-lookup"><span data-stu-id="78345-115">The default value is `1`.</span></span> |
| <span data-ttu-id="78345-116">mediaInfo</span><span class="sxs-lookup"><span data-stu-id="78345-116">mediaInfo</span></span>   | [<span data-ttu-id="78345-117">mediaInfo</span><span class="sxs-lookup"><span data-stu-id="78345-117">mediaInfo</span></span>](mediainfo.md) | <span data-ttu-id="78345-118">La información de medios</span><span class="sxs-lookup"><span data-stu-id="78345-118">The media information</span></span>                                                           |

## <a name="json-representation"></a><span data-ttu-id="78345-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="78345-119">JSON representation</span></span>

<span data-ttu-id="78345-120">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="78345-120">The following is a JSON representation of the resource.</span></span>

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

## <a name="example"></a><span data-ttu-id="78345-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="78345-121">Example</span></span>

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
