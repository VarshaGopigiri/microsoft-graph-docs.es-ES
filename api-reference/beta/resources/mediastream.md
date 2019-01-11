---
title: tipo de recurso mediaStream
description: El tipo de mediaStream.
author: VinodRavichandran
localization_priority: Normal
ms.openlocfilehash: 7e56448c2c6d284e7a5904f1b0af414166782907
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27889617"
---
# <a name="mediastream-resource-type"></a><span data-ttu-id="46150-103">tipo de recurso mediaStream</span><span class="sxs-lookup"><span data-stu-id="46150-103">mediaStream resource type</span></span>

> <span data-ttu-id="46150-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="46150-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="46150-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="46150-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="46150-106">El tipo de mediaStream.</span><span class="sxs-lookup"><span data-stu-id="46150-106">The mediaStream type.</span></span>

## <a name="properties"></a><span data-ttu-id="46150-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="46150-107">Properties</span></span>

| <span data-ttu-id="46150-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="46150-108">Property</span></span>    | <span data-ttu-id="46150-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="46150-109">Type</span></span>    | <span data-ttu-id="46150-110">Description</span><span class="sxs-lookup"><span data-stu-id="46150-110">Description</span></span>                                                                                                   |
| :---------- | :------ | :------------------------------------------------------------------------------------------------------------ |
| <span data-ttu-id="46150-111">dirección</span><span class="sxs-lookup"><span data-stu-id="46150-111">direction</span></span>   | <span data-ttu-id="46150-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="46150-112">String</span></span>  | <span data-ttu-id="46150-113">La dirección.</span><span class="sxs-lookup"><span data-stu-id="46150-113">The direction.</span></span> <span data-ttu-id="46150-114">Los valores posibles son `inactive`, `sendOnly`, `receiveOnly`, `sendReceive`.</span><span class="sxs-lookup"><span data-stu-id="46150-114">The possible values are `inactive`, `sendOnly`, `receiveOnly`, `sendReceive`.</span></span>                  |
| <span data-ttu-id="46150-115">label</span><span class="sxs-lookup"><span data-stu-id="46150-115">label</span></span>       | <span data-ttu-id="46150-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="46150-116">String</span></span>  | <span data-ttu-id="46150-117">La etiqueta de secuencia de medios.</span><span class="sxs-lookup"><span data-stu-id="46150-117">The media stream label.</span></span>                                                                                       |
| <span data-ttu-id="46150-118">mediaType</span><span class="sxs-lookup"><span data-stu-id="46150-118">mediaType</span></span>   | <span data-ttu-id="46150-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="46150-119">String</span></span>  | <span data-ttu-id="46150-120">El tipo de medios.</span><span class="sxs-lookup"><span data-stu-id="46150-120">The media type.</span></span> <span data-ttu-id="46150-121">Los valores posibles son `unknown`, `audio`, `video`, `videoBasedScreenSharing`, `data`.</span><span class="sxs-lookup"><span data-stu-id="46150-121">The possible value are `unknown`, `audio`, `video`, `videoBasedScreenSharing`, `data`.</span></span>        |
| <span data-ttu-id="46150-122">serverMuted</span><span class="sxs-lookup"><span data-stu-id="46150-122">serverMuted</span></span> | <span data-ttu-id="46150-123">Booleano</span><span class="sxs-lookup"><span data-stu-id="46150-123">Boolean</span></span> | <span data-ttu-id="46150-124">Si se desactiva la multimedia por el servidor.</span><span class="sxs-lookup"><span data-stu-id="46150-124">If the media is muted by the server.</span></span>                                                                          |
| <span data-ttu-id="46150-125">sourceId</span><span class="sxs-lookup"><span data-stu-id="46150-125">sourceId</span></span>    | <span data-ttu-id="46150-126">Cadena</span><span class="sxs-lookup"><span data-stu-id="46150-126">String</span></span>  | <span data-ttu-id="46150-127">El identificador de origen.</span><span class="sxs-lookup"><span data-stu-id="46150-127">The source ID.</span></span>                                                                                                |

## <a name="json-representation"></a><span data-ttu-id="46150-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="46150-128">JSON representation</span></span>

<span data-ttu-id="46150-129">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="46150-129">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "serverMuted"
  ],
  "@odata.type": "microsoft.graph.mediaStream"
}-->
```json
{
  "direction": "inactive | sendOnly | receiveOnly | sendReceive",
  "label": "String",
  "mediaType": "unknown | audio | video | videoBasedScreenSharing | data",
  "serverMuted": true,
  "sourceId": "String"
}
```

## <a name="example"></a><span data-ttu-id="46150-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="46150-130">Example</span></span>

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.mediaStream"
}-->
```json
{
  "direction": "sendReceive",
  "label": "main-audio",
  "mediaType": "audio",
  "serverMuted": false,
  "sourceId": "1024"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mediaStream resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
